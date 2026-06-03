# 📶 WiFi QR Generator

A single-file HTML tool that generates universally compatible WiFi QR codes — no app, no backend, no dependencies beyond a CDN-loaded QR library.

Scan the QR with any modern phone camera and connect instantly, no password typing needed.

## Demo

Open `wifi-qr.html` in any browser. That's it.

## Compatibility

Works natively with the built-in camera app on:

- iOS 11+
- Android 10+
- Samsung, Xiaomi / MIUI, Huawei, Google Pixel

No third-party QR scanner app required.

## Why does this work when others don't?

Many QR generators produce codes that fail on certain phones due to:

- Missing the double `;;` terminator at the end of the WiFi string
- Not escaping special characters (` \ ; , " : `) in the SSID or password
- Using low error correction levels that fail under poor lighting or on small screens

This tool uses the correct `WIFI:T:WPA;S:...;P:...;;` format, escapes all special characters automatically, and sets error correction to **Q level** (25% damage tolerance).

## Features

- WPA / WPA2 / WPA3, WEP, and open network support
- Hidden SSID option
- Download as PNG
- Print-friendly output page

## Usage

1. Download `wifi-qr.html`
2. Open it in a browser
3. Enter your network name and password
4. Click **Generate**
5. Print or share the QR image

## License

MIT
