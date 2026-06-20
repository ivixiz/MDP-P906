# MDP-P906 DFU Recovery Guide

## Problem

After a firmware update, the MDP-P906 becomes stuck in DFU mode.

### Symptoms

* Firmware files are accepted:

  * `.ADDR` → `.USE`
  * `.BIN` → `.RDY`
* After reboot, the display shows:

  ```
  Serial
  DFU V4.04
  ```
* No buttons respond.
* Reinstalling firmware (v1.32, v1.33, v3.01) does not help.

### Cause

The bootloader remains in DFU mode and does not start the application firmware.

---

## Recovery

### 1. Flash Firmware via ST-Link

Connect an ST-Link to the rear programming connector and flash:

```
MDP-P906_v3.01.rdy
```

to:

```
0x08008000
```

(the address specified in the `.ADDR` file).

After flashing, reboot the device.

---

## Calibration Fix

If the device boots but voltage/current regulation behaves incorrectly (for example, 0.240 V setpoint produces 30 V output), recalibrate the unit:

1. Backup `XXXXXXXX.CFG` and `XXXXXXXX.PRM`.
2. Delete both files from the P906 USB drive.
3. Rename them to:

   ```
   CONFIG.TXT
   PARAM.TXT
   ```
4. Copy the renamed files back to the USB drive.
5. Reboot the device.
6. When **CALIBRATE MODE** appears, hold **SET** and restart again.
7. After calibration completes, restore the original `.CFG` and `.PRM` files.

The power supply should now operate normally.
