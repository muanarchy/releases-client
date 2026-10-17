# MuAnarchy Client mod releases

Download-only repository: releases are published here by the build pipeline; there is no source code.

## Latest: v0.0.30 (2026-10-17)

- [Everything for players (main-full.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main-full.zip)
- [Main.dll only (main.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main.zip)

[Release page](https://github.com/muanarchy/releases-client/releases/tag/v0.0.30) · [all versions](https://github.com/muanarchy/releases-client/releases). Every release lists the SHA-256 of its files.

## Windows warns about the download?

New or rarely downloaded files get a SmartScreen / browser warning ("isn't commonly downloaded") because they are not code-signed yet. It does not mean the file is bad:

- Browser: keep / "Keep anyway". SmartScreen: **More info** then **Run anyway**.
- Check the file if you like: its SHA-256 is in `version.txt` on the release page.
- The launcher updates itself and the mod afterwards, so this only happens on the first download.

## Change log of v0.0.30

#### Main v0.0.30

Commit 6b0ff75. Players: unzip `main-full.zip` into the game folder (samples, docs, INSTALL.txt). The launcher uses `main.zip` (Main.dll only).

#### Changes since v0.0.29
- docs: OPENFORMATS.md stage 3 (as built, height / light hook evidence, verified statically and against the reference world files, real-client checklist), DIAG / RE-NAMES rows, ini sample, INSTALL, package note, CLAUDE pointer (6b0ff75)
- OpenFormats stage 3: world files before EncTerrain .att / .map / .obj (call-site hooks fed through the in-memory feed, client checks re-run before feeding), TerrainHeight.OZB.png fed to 0x5E7690, TerrainLight.OZJ.png replaces the 0x62BE00 call (caeb601)
- OpenFormats stage 3: world encoder (pure: JSON + grey PNG planes -> exact .att / .map / .obj bytes, client attribute check, height image, light fill, hook-site guards), fixtures, host tests (26ced2f)

