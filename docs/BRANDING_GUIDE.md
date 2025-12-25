# Branding & Licensing Guide

This project is licensed under the MIT License. You can add your own branding while keeping the original copyright notice intact. The steps below outline how to refresh the visuals and add your own notice without removing the existing one.

## Keep the MIT License Intact
- Do **not** delete the existing [`LICENSE`](../LICENSE) file. The upstream notice must remain.
- To add your own copyright, append a new line with your name or organization beneath the existing notice. Example:
  ```
  Copyright (c) 2025 Your Name or Company
  ```

## Swap in Your Brand Assets
Update the assets in `client/public/assets` to change the visible branding:
- **Logo:** Replace `client/public/assets/logo.svg` with your logo.
- **Icons:** Swap the PWA/browser icons to match your brand:
  - `client/public/assets/favicon-16x16.png`
  - `client/public/assets/favicon-32x32.png`
  - `client/public/assets/apple-touch-icon-180x180.png`
  - `client/public/assets/icon-192x192.png`
- **Audio stub (optional):** If you change the `assets/silence.mp3` file used for autoplay compatibility, keep the same filename so the app can find it.

## Refresh On-Screen Text
If you want the UI to display your product name in place of "LibreChat":
- Search for `LibreChat` in `client/src` and update the strings that represent product names or captions (most are in the localization files under `client/src/locales/`).
- Leave references that describe protocol support or upstream credits as-is to keep documentation accurate.

## Regenerate Build Artifacts
After updating assets and strings, rebuild the client so the new branding is bundled:
```bash
npm install
npm run build:client
```

Keeping these steps in mind lets you present your own branding while honoring the upstream MIT License requirements.
