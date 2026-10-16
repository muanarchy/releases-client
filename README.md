# MuAnarchy Client mod releases

Download-only repository: releases are published here by the build pipeline; there is no source code.

## Latest: v0.0.29 (2026-10-16)

- [Everything for players (main-full.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main-full.zip)
- [Main.dll only (main.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main.zip)

[Release page](https://github.com/muanarchy/releases-client/releases/tag/v0.0.29) · [all versions](https://github.com/muanarchy/releases-client/releases). Every release lists the SHA-256 of its files.

## Windows warns about the download?

New or rarely downloaded files get a SmartScreen / browser warning ("isn't commonly downloaded") because they are not code-signed yet. It does not mean the file is bad:

- Browser: keep / "Keep anyway". SmartScreen: **More info** then **Run anyway**.
- Check the file if you like: its SHA-256 is in `version.txt` on the release page.
- The launcher updates itself and the mod afterwards, so this only happens on the first download.

## Change log of v0.0.29

#### Main v0.0.29

Commit 31f2ff5. Players: unzip `main-full.zip` into the game folder (samples, docs, INSTALL.txt). The launcher uses `main.zip` (Main.dll only).

#### Changes since v0.0.28
- docs: OPENFORMATS.md stage 2 (as built, verified statically and against the reference tables, real-client checklist), DIAG / RE-NAMES rows, ini sample, INSTALL, package note, CLAUDE pointer (31f2ff5)
- OpenFormats stage 2: JSON before the twelve table .bmd (call-site hooks fed through the in-memory file feed) (9ca9a00)
- OpenFormats stage 2: strict JSON reader, table layouts and the JSON -> stock .bmd encoder (pure), fixtures, host tests (0d18ddf)

