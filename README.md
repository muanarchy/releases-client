# MuAnarchy Client mod releases

Download-only repository: releases are published here by the build pipeline; there is no source code.

## Latest: v0.0.24 (2026-10-15)

- [Everything for players (main-full.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main-full.zip)
- [Main.dll only (main.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main.zip)

[Release page](https://github.com/muanarchy/releases-client/releases/tag/v0.0.24) · [all versions](https://github.com/muanarchy/releases-client/releases). Every release lists the SHA-256 of its files.

## Windows warns about the download?

New or rarely downloaded files get a SmartScreen / browser warning ("isn't commonly downloaded") because they are not code-signed yet. It does not mean the file is bad:

- Browser: keep / "Keep anyway". SmartScreen: **More info** then **Run anyway**.
- Check the file if you like: its SHA-256 is in `version.txt` on the release page.
- The launcher updates itself and the mod afterwards, so this only happens on the first download.

## Change log of v0.0.24

#### Main v0.0.24

Commit aadd77c. Players: unzip `main-full.zip` into the game folder (samples, docs, INSTALL.txt). The launcher uses `main.zip` (Main.dll only).

#### Changes since v0.0.23
- Modal test: 794x599 golden y (aadd77c)
- Modal: log the frame on open, golden test for a 794x599 client (cccd106)

