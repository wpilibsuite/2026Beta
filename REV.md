# REV 2026 Beta 2

Beta 2 focuses on updates to RHC2, primarily introducing motor control capabilities on the Telemetry tab for tuning and prototyping. See the changelog for 0.3.0 below for more details.

## REVLib

[REVLib 2026.0.0-beta-1](https://github.com/REVrobotics/REV-Software-Binaries/releases/tag/revlib-2026.0.0-beta-1)

## REV Hardware Client 2

REV Hardware Client 2 (RHC2) is a separate application from REV Hardware Client (RHC) and can be installed on Windows, MacOS, and Linux.

[Install the latest version here](https://beta.rhc2.revrobotics.com/download/download.html).

If it is already installed, it should update automatically, or you can update it manually from the "About" tab.

<details>
<summary>Changelog</summary>

### 0.3.0

- Adds support for running SPARK on telemetry page
- Adds support for running SPARK in control types other than duty cycle
- Improves PDH channels card to resemble the physical layout of the channels
- Improves SPARK Run UI to enhance PID tuning experience
- Improves performance of SPARK UI
- Improves device drawer UI
  - Makes better use of white space
  - Keeps header fixed at the top when content is scrollable
- Improves scrolling experience in SPARK Configuration and Utilities pages
- Fixes issue where the app locks up when trying to close on Mac and Linux
- Fixes issue with telemetry signals between different devices being out of sync
- Fixes issue where adding signals to AScope would sometimes not work
- Fixes telemetry page resetting and losing all progress when switching tabs

### 0.2.2

- Fixes issue with DFU updating on Ubuntu
- Fixes UI crash when opening a device with no available releases
- Fixes rendering issues when resizing/moving the window
- Fixes links opening in another chromium window
- Fixes error when clicking support email
- Fixes issue where SPARK MAX bulk updates would not continue past updating the bridge device
- Fixes image and naming of roboRIO in device list
- Fixes inability to undo reset safe parameters on a SPARK
- Adds units to applicable parameters in SPARK configuration page
- Improves speed of fetching all parameters from a SPARK
- Improves download page
- Improves about page
- Ignores devices from other vendors in device list. This will be re-enabled in the future once they can be enumerated and displayed properly.

#### Known Issues

- No clear indication to the user that the application is loading devices when connected to a large CAN bus
- Signals on SPARK summary page pop in and out if the corresponding status frame period is high enough
- roboRIO pops in and out of the device list

### v0.2.1

- Fixes AdvantageScope theming not syncing with rest of app
- Fixes app not loading past splash screen on macOS
- Fixes DFU updating not working on macOS

</details>

## Updating firmware

The latest firmwares for SPARK Flex, SPARK MAX, Power Distribution Hub, Servo Hub, and Pneumatic Hub will be available to download and install after installing RHC2 and adding the following the code in the "Downloads" tab:

```txt
2026beta
```

> [!NOTE]
> For first time use, you will need to update at least one device via recovery mode to be able to use it with RHC2. You will then be able to use that device as the bridge device to use and update your other devices via CAN.

> [!NOTE]
> All hubs must be updated via recovery mode to update its CAN bootloader. Once updated, the device can be updated via CAN.
