# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Landing page: a single static HTML file with inline CSS and JS, no heavy dependencies (user requirement). The product itself is a Tauri 2 app (Rust backend, shared Rust/Wasm core, Leptos components and browser adapters) in `Antares/`.

## Users

General public: people who want to listen to music on their Windows PC without ads or a browser tab, and who care about a polished, customizable player. Spanish-speaking (the app and its installer are in Spanish).

## Product Purpose

Antares is a desktop music player. You search a song or paste a link and it plays only the audio, with a Spotify-like queue, synced lyrics, a 10-band equalizer, playlists, personalized home shelves and a local recommender. Visitors should understand the player, choose a published download or inspect development status for their platform.

## Positioning

- Plays audio only, no browser and no ads; lightweight native app (Tauri + Rust).
- Recommender runs locally from your own listening stats, and every recommendation says why it is there.
- Deep personalization: themes including one that takes the color of the playing artwork, 12 typefaces, layouts, player bar styles, profiles.
- Import playlists from YouTube, YouTube Music, Spotify, Deezer, Apple Music, plain text or CSV.
- Desktop data uses local per-user files and automatic backups. The experimental PWA stores libraries on its configured server.

## Operating Context

Windows desktop (installer `Antares_<version>_x64-setup.exe`, per-user, no admin rights). Media keys, Windows media panel, taskbar thumbnail buttons, system tray, global shortcuts, mini player.

## Capabilities and Constraints

- Current version: 0.3.3 (tauri.conf.json). Installer 0.3.3 is 25,656,066 bytes (25.7 MB / 24.5 MiB), with the signed updater integrated.
- Android has a published 0.3.3 Beta 1 for ARM 32/64 and Android 7.0+. Keep its APK on the explicit Android prerelease channel.
- macOS Apple Silicon has a source adaptation and local QA. Distribution signing and a public Mac installer remain pending.
- iPhone/web have an experimental PWA and an iOS player adaptation. The PWA needs a separately hosted Rust API. Linux/Fedora support is experimental from source.
- The current code searches YouTube / YouTube Music and resolves audio with Rust. InnerTube is the first desktop resolution path; patched rusty_ytdl is the fallback. Search, imports and audio resolution run without yt-dlp or an external Python runtime.
- Leptos components and shared Wasm logic are migrating the application toward Rust. Browser/native adapters still use JavaScript. Keep source progress separate from the binaries already published.
- Source code: public at https://github.com/Hanyer001/Antares. Windows releases: https://github.com/Hanyer001/antares-actualizaciones/releases/latest.
- Updates: checks at startup and every six hours while open when enabled; asks before installation and verifies its signature. Older installations without the updater need one manual installation.
- Undecided / missing: social links, price (none found; app appears free).

## Brand Commitments

- Name: Antares. Logo: `Antares/assets/branding/icon.svg` (letter A with a sound wave crossing it; #0E1116 tile, #93B4DD stroke, #E0533D wave).
- Typeface: Inter (bundled in the app).
- Accent: steel blue hsl(213 49% 71%) = #93B4DD, which in the app shifts to the dominant color of the playing artwork.
- Voice: plain, concrete Spanish; the README explains features in everyday terms.

## Evidence on Hand

- Feature list and technical details: `Antares/README.md`.
- No real screenshots of the current UI. The landing recreates the interface from the app code.
- Local benchmarks and their scope are recorded in the source repository's macOS/Windows validation notes. Avoid converting backend or Wasm microbenchmarks into promises about network latency or every device.

## Product Principles

- Honest claims only: every feature on the landing maps to code.
- The music is the protagonist; the interface stays out of the way.
- Personal library and customization with storage and access described for each platform.

## Accessibility & Inclusion

The app ships a high-contrast theme, interface zoom 90-140 %, reduced motion options and rebindable shortcuts. The landing must respect prefers-reduced-motion, keyboard navigation and WCAG AA contrast.

## Version 0.3.3

Spotify pagination above 100 tracks (up to 500), full albums in order, compact artist view with five principal tracks and usual continuation, and explicit Solo este artista for the full queue.
