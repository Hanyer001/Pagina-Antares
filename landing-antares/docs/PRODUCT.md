# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Landing page: a single static HTML file with inline CSS and JS, no heavy dependencies (user requirement). The product itself is a Tauri 2 app (Rust backend, vanilla HTML/CSS/JS frontend) in `Antares/`.

## Users

General public: people who want to listen to music on their Windows PC without ads or a browser tab, and who care about a polished, customizable player. Spanish-speaking (the app and its installer are in Spanish).

## Product Purpose

Antares is a desktop music player. You search a song or paste a link and it plays only the audio, with a Spotify-like queue, synced lyrics, a 10-band equalizer, playlists, personalized home shelves and a local recommender. Success for the landing: visitors understand what it does differently and download the Windows installer.

## Positioning

- Plays audio only, no browser and no ads; lightweight native app (Tauri + Rust).
- Recommender runs locally from your own listening stats, and every recommendation says why it is there.
- Deep personalization: themes including one that takes the color of the playing artwork, 12 typefaces, layouts, player bar styles, profiles.
- Import playlists from YouTube, YouTube Music, Spotify, Deezer, Apple Music, plain text or CSV.
- All user data lives on the user's PC; incognito mode; automatic local backups.

## Operating Context

Windows desktop (installer `Antares_<version>_x64-setup.exe`, per-user, no admin rights). Media keys, Windows media panel, taskbar thumbnail buttons, system tray, global shortcuts, mini player.

## Capabilities and Constraints

- Current version: 0.3.0 (tauri.conf.json). Installer 0.3.0 is about 21.7 MB.
- Android: an APK build exists in the codebase, but per the user it will ship in a future update. Present it as "coming soon", never as available.
- macOS, Linux, iOS and web: not supported. Do not claim them.
- Music source: YouTube / YouTube Music (yt-dlp on desktop). User wants this mentioned discreetly (technical section and FAQ only, not hero or feature headlines).
- Source code: will be public on GitHub soon. No URL yet; "Ver en GitHub" stays as a marked placeholder.
- Undecided / missing: download URLs, GitHub URL, social links, price (none found; app appears free).

## Brand Commitments

- Name: Antares. Logo: `Antares/app-icon.svg` (letter A with a sound wave crossing it; #0E1116 tile, #93B4DD stroke, #E0533D wave).
- Typeface: Inter (bundled in the app).
- Accent: steel blue hsl(213 49% 71%) = #93B4DD, which in the app shifts to the dominant color of the playing artwork.
- Voice: plain, concrete Spanish; the README explains features in everyday terms.

## Evidence on Hand

- Feature list and technical details: `Antares/README.md`.
- No real screenshots of the current UI (the PNGs in `Claude outputs/` are of an old prototype). UI must be recreated from the real code.
- No testimonials, download counts, GitHub stars, or benchmarks. Do not fabricate any.

## Product Principles

- Honest claims only: every feature on the landing maps to code.
- The music is the protagonist; the interface stays out of the way.
- Everything is yours: local data, local recommender, full customization.

## Accessibility & Inclusion

The app ships a high-contrast theme, interface zoom 90-140 %, reduced motion options and rebindable shortcuts. The landing must respect prefers-reduced-motion, keyboard navigation and WCAG AA contrast.
