# 2026 ThriftyBot Beta Software


## ThriftyLib API (v2026.0.0)

### Installation
To use the 2026 Beta, use following URL:

**Vendor JSON URL:**
```
https://docs.home.thethriftybot.com/ThriftyLib-2026.0.0-beta-1.json
```

### Migration Guide (v2025 → v2026)

#### 1. PID Units Change (Breaking)
The most significant change is the move to **Rotational Units**. 
- **Position:** Now uses **Rotations** instead of raw ticks.
- **Velocity:** Now uses **Rotations per Second** instead of ticks per 100ms.

**Example Update:**
```java
// Old (v2025)
motor.setPosition(4096); // Move 1 rotation on SRX Mag

// New (v2026)
motor.setPosition(1.0); // Move 1 rotation regardless of encoder
```

#### 2. Package Reorganization
Update your imports to reflect the new structure:
- `com.thethriftybot.devices.ThriftyNova`
- `com.thethriftybot.util.Conversion`

#### 3. New Configuration Pattern
We recommend using the new `ThriftyNovaConfig` class for cleaner initialization:
```java
ThriftyNovaConfig config = new ThriftyNovaConfig();
config.brakeMode = true;
config.maxCurrent = 40.0;
motor.applyConfig(config);
```

## ThriftyConfig App (v2.0.0-beta.3)
[Download for Windows](https://docs.home.thethriftybot.com/software/app/ThriftyConfig+Setup+2.0.0-beta.3.exe)

**Key Features:**
- Swerve Project Generator
- Multi-controller Graphing and control  
- Nova Configuration over CAN

## Nova Firmware (v1.2.0-beta.1)
[Download Firmware](https://docs.home.thethriftybot.com/software/firmware/nova/beta/Nova-Firmware-v1.2.0-beta1.TBFW)
*Required for 2026 API and App features.*


## System Requirements

- Windows 10 or later (64-bit)
- macOS support is planned for a future release

## Additional Resources

- ThriftyConfig Documentation: [https://docs.home.thethriftybot.com/ThriftyConfig.html](https://docs.home.thethriftybot.com/ThriftyConfig.html)
- Nova Firmware Releases: [https://docs.home.thethriftybot.com/NovaFirmware.html](https://docs.home.thethriftybot.com/NovaFirmware.html)
- ThriftyConfig Releases: [https://docs.home.thethriftybot.com/ThriftyConfig.html](https://docs.home.thethriftybot.com/ThriftyConfig.html)

