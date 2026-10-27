<div align="center">

<img src="icon-512.png" alt="AeroTRC logo" width="140" />

# AeroTRC

### Smooth arrivals, every flight.

A fast, installable web app that helps airline ground crew run a clean aircraft arrival, from touchdown to chocks on and the final worksheet.

[**Open the app**](https://aerotrc.vercel.app/) · [Report a bug](https://aerotrc.vercel.app/) · [Request a feature](https://aerotrc.vercel.app/)

![PWA](https://img.shields.io/badge/PWA-installable-d11a5b?style=for-the-badge)
![Offline](https://img.shields.io/badge/Works-offline-8f0f3d?style=for-the-badge)
![Hosted on Vercel](https://img.shields.io/badge/Hosted%20on-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Supabase](https://img.shields.io/badge/Backend-Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)

</div>

---

## Overview

**AeroTRC** is a mobile-first arrival console built for the pressure of a real arrival. It keeps the flight worksheet, coach details, history and team tools in one place. It runs in the browser, installs like a native app, and keeps working when the signal drops.

## Features

| | |
|---|---|
| **Turnaround worksheet** | Flight details, sectors, registration and coach-wise entries in a single flow |
| **Coach management** | Add, edit and review coaches quickly with smart input helpers |
| **Flight history** | Save finished flights and look back at earlier turnarounds |
| **Connect** | Sign in with your employee ID and PIN, and use the team and leaderboard features |
| **Admin tools** | Manage users, including settings resets, from an admin panel |
| **Signature support** | Auto-signature option for completed worksheets |
| **Themes** | Many colour palettes, plus Light, Dark, Auto, Black (AMOLED) and Sunlight modes |
| **Haptic feedback** | Optional vibration on key actions |
| **Offline ready** | A service worker keeps the app shell available without a connection |
| **Installable** | Add to the home screen on Android and iOS, or package it as an APK |

## Install the app

**Android (Chrome)**
1. Open <https://aerotrc.vercel.app/>
2. Tap **Install** in the app, or open the browser menu and choose **Install app**.

**iPhone (Safari)**
1. Tap the **Share** button.
2. Choose **Add to Home Screen**.

**Build an APK**
1. Go to [pwabuilder.com](https://www.pwabuilder.com/).
2. Paste `https://aerotrc.vercel.app/` and choose **Android**.
3. Download the package. The manifest and icons in this repo are used automatically.

## Project structure

```
.
├── index.html        # The whole app (UI, logic, styles)
├── manifest.json     # PWA manifest (name, colours, icons)
├── sw.js             # Service worker (offline support)
├── vercel.json       # Vercel cache and content-type rules
├── robots.txt        # Search engine rules
├── sitemap.xml       # Sitemap for search engines
├── og-image.png      # Link preview image (1200x630)
├── icon-192.png      # App icon
└── icon-512.png      # App icon (store size)
```

## Deploy on Vercel

1. Put every file above in one folder, with `index.html` at the top level.
2. Run `vercel --prod` in the folder, or import the project at vercel.com.
3. Open the site over `https://`. Installing as an app needs a secure connection.
4. Reload once so the service worker activates.

> **Tip:** after an update, bump the version in `sw.js` (for example `aerotrc-v4` to `aerotrc-v5`) so phones fetch the new files instead of the cached ones.

## Tech stack

- **Frontend:** HTML, CSS and vanilla JavaScript in a single page
- **Styling:** Tailwind CSS with a custom Material-style theme system
- **Icons:** Lucide
- **Backend:** Supabase for sign-in and team data
- **PWA:** Web App Manifest and a service worker
- **Hosting:** Vercel

## Troubleshooting

| Problem | What to try |
|---|---|
| Install button only shows instructions | Use Chrome over `https://`, and make sure `manifest.json`, `sw.js` and both icons are uploaded |
| Old version still showing | Reload twice, or clear the site data in Chrome |
| "Cannot reach the server" at sign-in | Check your connection, and make sure the Supabase project is not paused |
| "Wrong employee ID or PIN" | Check the ID and PIN, or use **Forgot PIN** |
| Theme looks different after an update | Choose your palette and mode again in the settings |

## Search engine setup

1. Add the site to [Google Search Console](https://search.google.com/search-console).
2. Submit `https://aerotrc.vercel.app/sitemap.xml`.

## Contributing

Ideas and fixes are welcome. Open an issue to describe the change, or send a pull request with a short note on what it does and how you tested it.

## License

All rights reserved. Contact the owner before reusing the code, name or logo.

---

<div align="center">

Built for the people who keep flights on time.

</div>
