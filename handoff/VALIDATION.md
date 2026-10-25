# H3 preservation validation

Environment: Xcode 27.0 (27A266a), 25 October 2026. Unmodified H3 archive extracted into isolated temporary storage.

- Swift source parsing: PASS.
- `QA/verify_build28.py`, locked art and tutorial-control/source contracts: PASS.
- Standard `bash verify_on_mac.sh`: FAIL at command-input test compilation, after seven suites passed. `CommandInputTests.swift:40`: `CGPoint` equality unavailable because the test lacks `import CoreGraphics`. Initial sandbox cache-access failure was resolved by directing module caches to `/tmp`.
- The remaining six suites were run separately using their original commands: PASS. Total: 13 passed suites and one compile-failing suite, not a fully passing standard verification command.
- Unsigned generic iOS Simulator build: PASS, using `xcodebuild -project EmpiresOfElysia.xcodeproj -scheme EmpiresOfElysia -configuration Debug -sdk iphonesimulator -destination 'generic/platform=iOS Simulator' -derivedDataPath /tmp/elysia-h3-derived -jobs 2 CODE_SIGNING_ALLOWED=NO build`.
- Simulator launch, UI/gameplay acceptance and physical iPhone testing: NOT_RUN for H3. The separate active H2/V1672 test was not interrupted.
- Historical versions were preserved and scanned, not all rebuilt.

The 13 passed suites cover four systems, Survival lifecycle, Survival navigation, match setup, tutorial, navigation, combat, army/age planning, arena, economy, progress/Hall, last-session persistence, and legacy systems/roster.

No source/test fixes were made. Build outputs and machine-specific build logs are kept locally rather than included in source history.
