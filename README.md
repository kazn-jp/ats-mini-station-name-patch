# Manual Station Name Assignment Patch for ATS-MINI
> This is a small, Japan-specific patch for ATS-MINI v2.30, shared as a patch file only.
> All credit for the original ATS-MINI project goes to its author.

This is a personal modification for the ATS-MINI project (v2.30),
intended for Japan-specific broadcast conditions.

In Japan:
- MW (AM) stations are not covered by the EiBi database
- FM stations do not support RDS

As a result, station names cannot be displayed automatically.
This patch allows manual assignment of station names via a web browser.

## Features

- Tune stations using the ATS-MINI dial as usual
- Assign station names and comments via a web browser
- Station information is stored locally in JSON format
- No dependency on EiBi or RDS

## How to apply this patch

This patch is based on ATS-MINI v2.30.

```bash
git clone https://github.com/esp32-si4732/ats-mini.git
cd ats-mini
git checkout v2.30
git apply my-station-name.patch
```

## Build

```bash
arduino-cli compile --clean -e -u -p COMx ats-mini
```

## Note

If the ESP32 tool download times out:
```bash
arduino-cli config set network.connection_timeout 1200s
```

## Disclaimer

This patch is not an official feature of ATS-MINI.
It is a personal modification created for educational and experimental purposes.

All credit for the original project goes to the ATS-MINI author.

---

## Screenshots

### ATS-MINI Screen
<img src="images/ATS-Mini_screen.png" width="300">

### Web UI
<img src="images/Web_UI.png" width="300">

