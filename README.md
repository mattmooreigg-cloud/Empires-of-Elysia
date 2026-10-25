# Empires of Elysia

An iOS real-time strategy game built with SwiftUI and SpriteKit.

## Latest recovered source

**v1.6.7 build 28 H3 — Autosave / Continue**, from the 23 October 2026 development handoff. This includes continue-game/tutorial, periodic and lifecycle autosaving, collapsed tutorial minimap behavior, and larger control tap targets. No gameplay changes were made for this source-preservation task.

[Download the source preservation release](https://github.com/mattmooreigg-cloud/Empires-of-Elysia/releases/tag/source-handoff-2026-10-25).

The game source and intended art are published as the release's **named assets**:

- `EmpiresOfElysia-v1.6.7-build28-H3-source.zip`: latest complete source. Extract it and open `EmpiresOfElysia.xcodeproj` in Xcode.
- `Empires-of-Elysia-source-history.bundle`: complete recovered source history with 80 provenance tags, including older ZIPs, local folder variants, corrected H2 source and art archives.
- `MANIFEST.md`, `source-manifest.json`, `VALIDATION.md`, `SHA256SUMS.txt`: inventory, original archive hashes, snapshot commits, exclusions, build checks and asset checksums.

The `main` branch is the publication index; the game tree and historical `source-import/` tags are **inside the bundle**, not installed as remote GitHub branches/tags. GitHub's automatic "Source code" downloads for the preservation-release tag contain this index, so use the named H3 ZIP or bundle above.

```sh
git clone Empires-of-Elysia-source-history.bundle Empires-of-Elysia-source
cd Empires-of-Elysia-source
git tag
# Inspect a preserved version:
git checkout source-import/library/empiresofelysia-v1.6.7-build28-h3-autosave-continue-xcode
```

These are source archives, not installable iPhone binaries. Import commits reconstruct preservation snapshots; they are not original development history. The original repository initialization commit remains preserved. Some filenames disagree with their Xcode version settings; both are recorded in the manifest.

## Validation and limits

H3 unsigned iOS Simulator compilation passed on Xcode 27.0. Source/asset checks and 13 of 14 rule suites passed; the unchanged command-input test fails because `CommandInputTests.swift` lacks `import CoreGraphics`. H3 Simulator playtesting, physical-device testing and gameplay acceptance were not performed in this handoff.

[Full inventory](handoff/MANIFEST.md) · [Validation](handoff/VALIDATION.md) · [Exact provenance](handoff/source-manifest.json)

No v1.6.1 source was found. v1.6.8 had not been built. Two Documents copies could not be fully read; upstream source archives and the complete corrected H2 source recovered from its temporary validation folder are preserved. One extracted v0.2 folder is incomplete; its original ZIP is complete. No claim is made that every historical version exists.

Original files and active development were left intact. Provisioning profiles, signing credentials, compiled apps, machine logs, user settings and unrelated private files were excluded. No credentials or security settings were created or changed.

Matt retains final authority over gameplay and acceptance. This publication does not schedule development or imply a daily build automation exists.
