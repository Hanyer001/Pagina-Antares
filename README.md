# Antares — Product Website

The presentation and download website for **Antares**, a music player for Windows and Android.

**[Visit the website](https://hanyer001.github.io/Pagina-Antares/)** · [Application source](https://github.com/Hanyer001/Antares) · [Releases](https://github.com/Hanyer001/antares-actualizaciones/releases)

## Purpose

This repository contains the static product page, separate from the application source and release artifacts. It presents features, platform availability and installation links.

- **Windows:** stable 0.3.3, distributed through the latest stable release channel.
- **Android:** 0.3.3 Beta 1, Android 7.0+ on 32-bit and 64-bit ARM.
- Download buttons choose the Android APK or Windows installer based on the visitor's platform.
- Public GitHub release metadata supplies the Windows version and installer size, with configured fallback values.

Android remains a beta. Its download points to a specific prerelease tag and does not replace the Windows stable channel. Automatic in-app update notifications on Android are not yet implemented.

## Run locally

Requires Python 3 for a static server; there is no npm build step.

```sh
git clone https://github.com/Hanyer001/Pagina-Antares.git
cd Pagina-Antares
python3 -m http.server 8000 --bind 127.0.0.1
```

Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/). On Windows, `py` can replace `python3`.

## Structure and publishing

| Path | Purpose |
| --- | --- |
| `index.html` | Production page, including styles and JavaScript. |
| `landing-antares/index.html` | Working copy of the same page. |
| `landing-antares/docs/` | Product and design notes in Spanish. |

GitHub Pages serves the root of `main`. Keep both HTML copies synchronized when editing. The [working-directory README](landing-antares/README.md) summarizes maintenance.

Before publishing, check the release tag, Windows package size, fallback metadata and both platform download links. Verify the mobile layout and published page after deployment. Downloads are hosted as GitHub Release assets in `antares-actualizaciones`, rather than stored in this website repository.
