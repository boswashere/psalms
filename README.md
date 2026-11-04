# Psalms source snapshot

Archived Lua/Luau source retrieved on **2026-11-04**. The main script is [`psalms.lua`](psalms.lua), the remote script selected by the recovered Luraph `input.lua` loader.

The main script was already readable on its upstream server. The deobfuscation work recovered the original loader, not the source of this entire script.

## Files

| File | Purpose | Bytes | Lines |
| --- | --- | ---: | ---: |
| [`psalms.lua`](psalms.lua) | Main targeting, player overlays, movement, visuals and settings | 190,141 | 5,966 |
| [`dependencies/psalms-bootstrap.lua`](dependencies/psalms-bootstrap.lua) | Adonis detection/debug hook bypass attempt | 1,370 | 60 |
| [`dependencies/ui-fallback.lua`](dependencies/ui-fallback.lua) | UI framework selected for some executors | 144,450 | 4,423 |
| [`dependencies/cursor.lua`](dependencies/cursor.lua) | Animated crosshair | 3,965 | 117 |

All four Lua files are byte-for-byte copies of the downloaded sources. [`sources.json`](sources.json) records their upstream URLs, retrieval results and SHA-256 hashes.

## Dependencies and limits

`psalms.lua` still loads its original remote dependencies; this archive does not rewrite it to use the local copies. Executor-name checks select either the Pastebin UI at `https://pastebin.com/raw/LixdnWjB` or the archived Gist UI. The Pastebin source returned **HTTP 403** during inspection and is not included.

The other Firebase `Build` entries are separate scripts and are not part of this repository. The Firebase authentication token and original authenticated loader are intentionally excluded.

Downloaded Lua was **not executed**. Hashes establish consistency with the saved sources, not safety, compatibility or successful operation. This snapshot does not grant a new license to the upstream code; authorship remains with its original authors.
