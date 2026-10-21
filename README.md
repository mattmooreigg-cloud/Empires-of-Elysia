# Empires of Elysia

An iOS real-time strategy game built with SwiftUI and SpriteKit, featuring fantasy and historical civilizations, base building, tactical combat, and Standard, Survival, and Tutorial modes.

Development prioritizes game balance, replayability, and an uncluttered interface, with Survival improvements first and Standard improvements second.

## Current baseline

The initial source import is **v1.6.5, Build 26**. Matt's playtest acceptance is pending. This is a source-development repository, not an App Store or TestFlight release.

The complete Xcode project and its original art are in `EmpiresOfElysia/`. Open `EmpiresOfElysia/EmpiresOfElysia.xcodeproj` in Xcode. See the project's original README and `RELEASE_NOTES_v165_build26.md` for build and playtest details.

## Validation

Run `bash verify_on_mac.sh` from `EmpiresOfElysia/` on a Mac with Xcode installed. The macOS validation workflow runs the existing Swift rule suites and builds for iOS Simulator without signing.

Native compilation, simulator launch, physical iPhone testing, and gameplay acceptance are separate checks. A successful CI build does not establish device or gameplay acceptance. Consult the workflow run and its evidence for the exact commit tested.

## Production

Matt retains final authority. The production manager coordinates specialist agents, accepts candidate work against documented criteria, and provides a consolidated playtest handoff. Routine changes use isolated branches and reviewable pull requests. New game modes, material balance changes, and locked-art redesigns require Matt's approval.

The daily playtest handoff target is 09:30 Asia/Shanghai. A scheduled workflow validates committed source; it does not itself develop new gameplay or guarantee a new accepted version every day.
