
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


# Useful screenshots
<img width="4576" height="2089" alt="problem2" src="https://github.com/user-attachments/assets/bd3c1f55-3957-4441-b5f1-0a2d2ee79708" />
<img width="2361" height="4142" alt="P_20260224_195658_1" src="https://github.com/user-attachments/assets/e416a22f-305a-4e45-867a-52d552451741" />
<img width="3887" height="1602" alt="P_20260225_200122_1" src="https://github.com/user-attachments/assets/fd26c89f-d5fa-4e36-8607-7234970c3e91" />
<img width="4576" height="3432" alt="MDP-P9064" src="https://github.com/user-attachments/assets/bf143e2e-9440-4f4c-8abc-12fed9c7540f" />
<img width="4576" height="3432" alt="MDP-P9065" src="https://github.com/user-attachments/assets/92014963-5eff-4b15-a5cb-e2df7967e702" />
<img width="1638" height="975" alt="MDP-P9066" src="https://github.com/user-attachments/assets/86ca0639-1a7e-49cf-b155-7cb4f8613e49" />
