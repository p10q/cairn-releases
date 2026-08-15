# cairn/ — Sparkle update feed

GitHub Pages serves this repo at `https://updates.p10q.com/`, so files here
are reachable under `https://updates.p10q.com/cairn/`.

The app's `SUFeedURL` is `https://updates.p10q.com/cairn/appcast.xml`, and the
appcast's download URLs resolve to `https://updates.p10q.com/cairn/<DMG>`.

## Publishing a release

1. In the main `cairn` checkout: bump `BRAND_VERSION` / `BRAND_BUILD_NUMBER`,
   then `./scripts/release-macos.sh` (produces `dist/cairn/updates/appcast.xml`
   + `Cairn-<version>.dmg`, EdDSA-signed).
2. Copy `dist/cairn/updates/appcast.xml` and the new `Cairn-<version>.dmg` into
   this folder.
3. Keep every released DMG here so `appcast.xml` can list the full version
   history. Commit and push; Pages redeploys automatically.

Do not use Git LFS for the DMGs — GitHub Pages serves LFS pointer files, not
the binaries.
