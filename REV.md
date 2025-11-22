# REV 2026 Beta 1

## REVLib

[REVLib 2026.0.0-beta-1](https://github.com/REVrobotics/REV-Software-Binaries/releases/tag/revlib-2026.0.0-beta-1)

## REV Hardware Client 2

REV Hardware Client 2 (RHC2) is a separate application from REV Hardware Client (RHC) and can be installed on Windows, MacOS, and Linux.

[Install the latest version here](https://beta.rhc2.revrobotics.com/download/download.html) 

## Updating firmware

The latest firmwares for SPARK Flex, SPARK MAX, Power Distribution Hub, Servo Hub, and Pneumatic Hub will be available to download and install after installing RHC2 and adding the following the code in the "Downloads" tab:

```txt
2026beta
```

> [!NOTE]
> For first time use, you will need to update at least one device via recovery mode to be able to use it with RHC2. You will then be able to use that device as the bridge device to use and update your other devices via CAN.

> [!NOTE]
> All hubs must be updated via recovery mode to update its CAN bootloader. Once updated, the device can be updated via CAN.
