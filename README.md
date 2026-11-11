# Battery Monitor - Official Downloads

Battery Monitor is a lightweight, local-only Windows tray app for real-time
battery telemetry, health diagnostics, session history, and HTML/JSON reports.

**This repository contains release downloads only. It does not contain the
application source code.**

## Download

Open the [latest release](https://github.com/Fahad-FullStackDeveloper/battery-monitor-download/releases/latest)
and download `BatteryMonitor-Setup-1.8.1.exe`.

- Single-file installer, no source folder required
- Per-user install: `%LOCALAPPDATA%\Programs\BatteryMonitor`
- No administrator rights required
- Adds Desktop and Start Menu shortcuts and enables Start with Windows
- Right-click the tray icon for Pause/Resume, Refresh Interval
  (5/10/15/20/30 seconds), dashboard, and quit options

## Install

1. Download `BatteryMonitor-Setup-1.8.1.exe`.
2. Double-click it.
3. If Windows SmartScreen appears, choose **More info -> Run anyway**.
   The build is currently unsigned.
4. Wait for `Installation complete`; the tray icon starts automatically
   (it may be in the hidden-icons overflow).

To uninstall, open the Start Menu folder **Battery Monitor** and run
**Uninstall Battery Monitor**. Battery data is preserved in
`Documents\BatteryMonitor-Data-<timestamp>` unless the purge option is used.

## Features

- Real-time percentage, charging state, voltage, power, and temperature
- Battery health and degradation tracking with persistent history
- AccuBattery-style charge/discharge sessions and daily summaries
- Live HTML dashboard with charts and session tables
- Tray alerts for low and critical battery
- Local-only operation: no account, no cloud, no telemetry

## Privacy

All battery data stays on your PC. The app does not upload telemetry or
personal data. Reports are generated locally.

## Verify the download

Use `SHA256SUMS.txt` from this repository:

```powershell
Get-FileHash .\BatteryMonitor-Setup-1.8.1.exe -Algorithm SHA256
```

Expected SHA-256 for v1.8.1:

```text
00D52B41868004A2724975C2AAC8AE4C59B7E78CB44284BDCE646E78AB2281E6
```

## Requirements

- Windows 10 or Windows 11
- PowerShell 5.1 or later (already included with Windows)
- Battery temperature readings may require running as administrator;
  percentage, status, power, and history work without it

## License

MIT. See `LICENSE`.