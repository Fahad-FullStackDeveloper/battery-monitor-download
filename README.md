# Real Battery Health Monitor - Official Downloads

Real Battery Health Monitor is a lightweight, local-only Windows tray app for
real-time battery telemetry, health diagnostics, session history, and
HTML/JSON reports.

**This repository contains release downloads only. It does not contain the
application source code.**

## Download

Open the [latest release](https://github.com/Fahad-FullStackDeveloper/battery-monitor-download/releases/latest)
and download `RealBatteryHealthMonitor-Setup-1.8.2.exe`.

- Single-file installer, no source folder required
- Per-user install: `%LOCALAPPDATA%\Programs\BatteryMonitor`
- No administrator rights required
- Adds Desktop and Start Menu shortcuts and enables Start with Windows
- Right-click the tray icon for Pause/Resume, Refresh Interval
  (5/10/15/20/30 seconds), dashboard, and quit options

## Install

1. Download `RealBatteryHealthMonitor-Setup-1.8.2.exe`.
2. Double-click it.
3. If Windows SmartScreen appears, choose **More info -> Run anyway**.
   The build is currently unsigned.
4. Wait for `Installation complete`; the tray icon starts automatically
   (it may be in the hidden-icons overflow).

To uninstall, open the Start Menu folder **Real Battery Health Monitor** and run
**Uninstall Real Battery Health Monitor**. Battery data is preserved in
`Documents\BatteryMonitor-Data-<timestamp>` unless the purge option is used.

## Features

- Real-time percentage, charging state, voltage, power, and temperature
- Battery health and degradation tracking with persistent history
- AccuBattery-style charge/discharge sessions and daily summaries
- Live HTML dashboard with charts and session tables
- **Complete hardware inventory:** battery name, device ID, design voltage,
  manufacturer, serial, chemistry, and cycle count
- **Full system specifications:** CPU cores/threads/clock/cache/socket,
  RAM module count and slot usage (for example 8 GB x 2 vs a single 16 GB
  module), per-module type/speed/form factor/part number, maximum supported
  RAM, every SSD/HDD/USB storage device with size, bus, health, serial, and
  volumes, all GPUs with VRAM, motherboard, BIOS, OS install date, and uptime
- The same data appears in the CLI monitor, the HTML dashboard, and
  `Battery_Full_Report.json`
- Works generically on any Windows laptop or desktop through WMI/CIM and
  Storage cmdlets; no fixed hardware template
- Tray alerts for low and critical battery
- Local-only operation: no account, no cloud, no telemetry

## Privacy

All battery data stays on your PC. The app does not upload telemetry or
personal data. Reports are generated locally.

## Verify the download

Use `SHA256SUMS.txt` from this repository:

```powershell
Get-FileHash .\RealBatteryHealthMonitor-Setup-1.8.2.exe -Algorithm SHA256
```

Expected SHA-256 for v1.8.2:

```text
6B2ABA67747C15B62C151F5F40825DA1F073474741577A33F9E2CB32B27C4B1A
```

## What changed in v1.8.2

- Renamed the user-facing app to **Real Battery Health Monitor** (tray menu,
  tooltip, shortcuts, installer, dashboard, and docs). Existing installs
  upgrade in place and legacy shortcuts are migrated automatically.
- Expanded hardware and system specifications with the full RAM layout,
  every storage device, all GPUs, motherboard, BIOS, OS details, and battery
  hardware details listed above.
- JSON export now includes a `System` section with memory modules, storage
  devices, and GPU arrays.
- Cleaner upgrades: stale script copies from older versions are removed, and
  uninstalling from the Start Menu removes the installed folder correctly.

## Requirements

- Windows 10 or Windows 11
- PowerShell 5.1 or later (already included with Windows)
- Battery temperature readings may require running as administrator;
  percentage, status, power, and history work without it

## License

MIT. See `LICENSE`.
