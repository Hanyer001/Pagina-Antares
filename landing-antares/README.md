# Antares Website — Working Copy

This directory holds a working copy of the Antares product page and its product/design notes. The production page is served from the repository root.

See the [main README](../README.md) for setup, platform support and publishing instructions.

## Editing rules

- Keep `index.html` in this directory synchronized with `../index.html`.
- Check the current Windows release, installer size and configured fallback values before updating version copy.
- Keep Android labeled as a beta and link its APK to the intended Android prerelease tag.
- Windows download links follow the stable release channel; Android releases must not replace that channel.
- Confirm both platform buttons and the responsive layout after deployment.

Product and design context is available in [PRODUCT.md](docs/PRODUCT.md) and [DESIGN.md](docs/DESIGN.md), currently in Spanish.

## Current source information

Development sections now describe the shared Rust/Wasm core, Leptos, Rust search and extraction, macOS QA and experimental web/iPhone support. Mac visitors open the macOS guide; iPhone visitors open the platform status section. Published downloads retain their own release versions.

Keep technical descriptions aligned with the source README and validation record. Update the product notes whenever platform status changes.
