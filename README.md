# Gateway OS Plugin Releases

Binary-only Gateway OS plugin releases.

This repository is for sharing compiled plugin zip assets only. It does not contain the Gateway OS source code, build files, project files, or development history.

## Latest Public Plugin Release

- Version: Gateway OS V1.1.0
- Format: macOS AU/VST3 and Windows VST3 zip assets
- AU identity: `aufx G100 SMfo`
- macOS package: `GatewayOS-V1.1.0-macOS-AU-VST3.zip`
- macOS SHA256: `46CD30DEF19D75B278B3BE22786990634C88EE0415FE2593E93BF3519D4DF9AA`
- Windows package: `GatewayOSPresetV4-Windows-VST3-x64.zip`
- Windows SHA256: `D135D89270E16118C67AF098CB241BF51CF7C0E06FFAF8C5ECF198A87AA8EBFE`

Download the zip for your platform from the V1.1.0 release page.

## Preset System

Gateway OS V1.1.0 adds a 31-slot preset system.

- Preset slots range from `0` to `30`.
- Click `-` or `+` to move through presets.
- Slot navigation wraps around: `0` goes back to `30`, and `30` goes forward to `0`.
- Click the number field to type a preset number.
- Click the circular save/overwrite button to save the current plugin state into the active slot.
- Saving overwrites only the selected slot.
- Switching slots immediately recalls that slot.
- Unused slots load the default Gateway OS state.

Each preset stores the capture/model, IR, EQ, noise gate, input/output controls, slim setting, oversampling, multicore mode, calibration controls, output mode, color/theme settings, and active preset number.

DAW project recall stores the full preset bank so sessions reopen with the same settings that were saved.
