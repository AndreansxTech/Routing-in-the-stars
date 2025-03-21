## I am going to write a curated tutorial, on how to step by step make L3 functions work on a Brocade FLS648 switch, based on what I found on different places on the internet and what I learned myself


### ❗️ For archival purposes in this folder I am sharing the firmware files for the Brocade FastIron LS648/STK. I do not own these files, but if someday the current mirror of these files go down, I think it is better to have a backup of them since I have that switch❗️

There seems to be no link to the ZIP folder on the Fohdeesha docs website, it is only in a post on Reddit posted around 10 years ago. 


# Brocade FastIron LS648-STK – L3 Lite Firmware Activation Guide

![Status](https://img.shields.io/badge/status-working-success?style=for-the-badge)
![Hardware](https://img.shields.io/badge/hardware-FLS648--STK-blue?style=for-the-badge)
![License Hack](https://img.shields.io/badge/license-hardware%20EEPROM-lightgrey?style=for-the-badge)

This guide walks you through the process of enabling L3 Lite functionality on the **Brocade FastIron LS648-STK** switch -- using only firmware and a bit of EEPROM trickery. No license purchase required.

---

## Why this matters

These switches are cheap, powerful and surprisingly capable, but often misunderstood. By default, they run L2-only firmware. However, with the right firmware and EEPROM configuration, they unlock **static routing**, **RIP**, and other L3 Lite features.

---

## What you need

- A **Brocade FastIron LS648-STK** switch
- Serial connection (RJ45 to USB, e.g. FTDI)
- TFTP server (e.g. `tftpd64`, `tftpd-hpa`)
- Firmware file: `FGSL07202r.bin`
- Terminal emulator (e.g. PuTTY, minicom)
- (Optional) EEPROM hex viewer like HxD

---

## Firmware versions

| File Name          | Year | Feature Level | Description             |
|--------------------|------|----------------|-------------------------|
| `FGS07202a.bin`    | 2011 | L2             | Default switching only |
| `FGSL07202r.bin`   | 2015 | L3 Lite        | Basic routing (static, RIP) |
| `FGSR07202r.bin`   | 2015 | Full L3        | Advanced L3 (needs license) |

---

## Step-by-step tutorial

### 1. Connect to serial

- Use a terminal at `9600 8N1` or `115200 8N1` (depends on your bootloader version).
- Power on the switch.
- When boot output appears, press:
  ```
  Ctrl+Y, then Ctrl+M, then Enter
  ```
- You should enter:
  ```
  FLS-Monitor>
  ```

---

### 2. Inject the "license" into EEPROM

This switch uses a legacy hardware license stored in EEPROM at address `0x40`. Type the following:

```bash
i2cWriteByte 40 0 fe
i2cWriteByte 40 1 ed
i2cWriteByte 40 2 fa
i2cWriteByte 40 3 ce
i2cWriteByte 40 4 1
i2cWriteByte 40 5 0
i2cWriteByte 40 6 1
i2cWriteByte 40 7 0
```

This fakes a valid L3 Lite license.

> Tip: Use `i2cReadByte` to back up your original values.

---

### 3. Flash the L3 Lite firmware

- Place `FGSL07202r.bin` in your TFTP root folder.
- On the switch, type:

```bash
copy tftp flash <your TFTP server IP> FGSL07202r.bin primary
```

- Wait for the transfer to complete and reboot the switch.

---

### 4. Verify

After booting, confirm you're now using the L3 image:

```bash
show version
```

You should see:
```
SW: Version 07.2.02rT7e1
...
```

Now try L3 commands like:

```bash
ip route
ip routing
```

If they work -- you're in business.

---

## Notes about FGSR (Full L3)

- `FGSR07202r.bin` **will not load** with this EEPROM config.
- It returns:
  ```
  File Type Check failed
  TFTP to Flash error - code 8
  ```
- Likely requires a **different EEPROM license pattern** (currently unknown).

---

## FAQ

**Q: Can I brick my switch doing this?**  
A: Unlikely, as long as you don’t overwrite or corrupt bootloader flash. EEPROM edits are low-risk and reversible.

**Q: What does the license string mean?**  
A: No official docs. It's likely a feature bitmask interpreted at boot.

**Q: Can this enable full L3 (FGSR)?**  
A: Not yet -- further EEPROM reverse engineering needed.

---

## Credits

- Based on real hardware testing with the LS648-STK
- Firmware mirrors originally from Fohdeesha’s archive
- Guide assembled by AndreansxTech

---

## Screenshot examples

> TODO: Insert CLI output, EEPROM dump, serial session, web GUI if available

---
