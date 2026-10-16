# MuAnarchy Client mod releases

Download-only repository: releases are published here by the build pipeline; there is no source code.

## Latest: v0.0.27 (2026-10-16)

- [Everything for players (main-full.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main-full.zip)
- [Main.dll only (main.zip)](https://github.com/muanarchy/releases-client/releases/latest/download/main.zip)

[Release page](https://github.com/muanarchy/releases-client/releases/tag/v0.0.27) · [all versions](https://github.com/muanarchy/releases-client/releases). Every release lists the SHA-256 of its files.

## Windows warns about the download?

New or rarely downloaded files get a SmartScreen / browser warning ("isn't commonly downloaded") because they are not code-signed yet. It does not mean the file is bad:

- Browser: keep / "Keep anyway". SmartScreen: **More info** then **Run anyway**.
- Check the file if you like: its SHA-256 is in `version.txt` on the release page.
- The launcher updates itself and the mod afterwards, so this only happens on the first download.

## Change log of v0.0.27

#### Main v0.0.27

Commit a14c3eb. Players: unzip `main-full.zip` into the game folder (samples, docs, INSTALL.txt). The launcher uses `main.zip` (Main.dll only).

#### Changes since v0.0.26
- minimap tests: the sample ships Enabled=1 (a14c3eb)
- docs: OPENFORMATS.md (stage 0 as built, how to add a loader hook, verified vs real client), CLAUDE pointer, DIAG openformats kind, RE-NAMES CRT / allocator rows; release ships the sample and the doc (341f6c3)
- OpenFormats stage 0: client side (index walk of the Data folders, Main.exe allocator, in-memory file feed with CRT shims and a guarded call-site installer, EVT kind=openformats, Fault switch-off); OpenFormatsLoad after MinimapLoad and Texture.Load, no loader hooked (d5985b4)
- OpenFormats stage 0: pure headers (openformats.ini, path keys, open-file index, picture / sibling names, feed state, virtual file, CRT / allocator / image loader guards), host tests, openformats.ini.sample (Enabled=0) (d509b83)
- PETS-CLIENT: stock client Dark Raven/Horse analysis (A7 senders, A8/A9 handlers, client-side raven), RE-NAMES rows (1794d63)
- minimap: ship enabled by default (244d3a4)
- Minimap notices: the message window lines drawn at the top left (chat / message window line methods, guarded vtable slots) move above the bottom-left list (059802d)
- Minimap: title under the map, MapSize 160 / OffsetX 12; stock top-left message list moved to the bottom left above the chat (NoticePlacement, guarded hook of its line draw) (b031f1d)
- minimap tests: layout expectations for the 2,2 default offset (5968e94)
- minimap: default offset 2,2 (hugs the top left corner) (ac0a140)
- Minimap: title without the black strip (blend on for the stock text box), toggle key from the keyboard hook (one action per press, ignored while typing), visible=0/1 events (56255c6)
- Minimap: top-left by default (Corner, OffsetX/Y), map diamond only (no panel), semi-transparent with a gold border, outlined title, click-through outside the diamond (da5bf7b)
- Minimap: corner panel with the world picture (stock OZT loader, <= 256), hero arrow, party/NPC/monster dots, wheel zoom, drag, minimap.ini (shipped off) (50e2279)

