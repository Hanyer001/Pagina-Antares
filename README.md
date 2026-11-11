# Antares product website

Presentation and download website for Antares, with Windows and Android Beta downloads and development information for Rust, Leptos, macOS and web/iPhone.

[Visit the website](https://hanyer001.github.io/Pagina-Antares/) · [Application source](https://github.com/Hanyer001/Antares) · [Published releases](https://github.com/Hanyer001/antares-actualizaciones/releases)

## Platform information

| Platform | Status shown on the website |
| --- | --- |
| Windows x64 | Published stable 0.3.3. Download metadata follows GitHub Releases. |
| Android ARM 32/64 | Published 0.3.3 Beta 1, Android 7.0+. APK points to its prerelease tag. |
| macOS Apple Silicon | Source and local QA. The Mac action opens the build/validation guide. |
| iPhone / web | Experimental PWA and iOS source adaptation. The PWA needs a hosted Rust API. |
| Linux / Fedora | Experimental source adaptation linked from the platform section. |

The development sections describe the current source tree. Download cards describe published packages. New source changes become downloadable updates after new release packages are built and published.

Search and audio extraction in the current application use Rust, InnerTube and the patched `rusty_ytdl` fallback. Shared rules and preference migrations compile to Wasm. Leptos renders application components while JavaScript adapters connect browser and native APIs. The product page itself uses static HTML, CSS and JavaScript.

## Repository structure

| Path | Purpose |
| --- | --- |
| `index.html` | Production page with inline styles and scripts. |
| `landing-antares/index.html` | Synchronized working copy of the production page. |
| `landing-antares/docs/` | Product and design context for maintenance. |

GitHub Pages serves the root of `main`. Keep both HTML copies identical. Application source lives in `Hanyer001/Antares`; published installers live in `Hanyer001/antares-actualizaciones`.

## Preview and verification

The page has no dependency installation or build step. Use a local static server, for example Python's standard development server.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open [the local preview](http://127.0.0.1:8000/). Verify Windows and Android downloads, Mac and iPhone actions, release metadata, navigation and the mobile layout before publishing. Confirm the deployed page after the push to `main`.

The published Windows installer and Android APK have separate channels. Preserve those release links when updating development information. The Windows file size shown by the page refers to its published installer.
