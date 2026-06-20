# Gateway OS Plugin Releases

Binary-only Gateway OS plugin releases.

This repository is for sharing compiled plugin zip assets only. It does not contain the Gateway OS source code, build files, project files, or development history.

## Latest Public Plugin Release

- Version: Gateway OS V1.2.7
- Format: macOS AU component zip
- AU identity: `aufx G127 SMfo`
- Bundle identifier: `com.SlamminMofo.audiounit.GatewayOSV127`
- macOS package: `GatewayOS-V1.2.7-macOS-AU.zip`
- macOS SHA256: `D58323403A619352191FC4EE026AA9650163423994CA28C92F0CF8CE68DD8F36`
- Architectures: `x86_64 arm64`

Download the zip from the V1.2.7 release page.

## Validation

Gateway OS V1.2.7 macOS AU was built in a private macOS CI builder and released here as a binary-only plugin asset.

- Fixed AU editor geometry verified at `600x400`.
- Universal Mach-O binary verified with `x86_64` and `arm64` slices.
- Codesign verification passed on the staged AU bundle.
- Apple AU validation passed with `auval -v aufx G127 SMfo`.
- The V1.1.8 Logic AU window sizing issue was addressed by matching the AU XIB size to the plugin editor size and preventing host-side AU view stretching.

## Preset System

Gateway OS includes a 31-slot preset system.

- Preset slots range from `0` to `30`.
- Click `-` or `+` to move through presets.
- Slot navigation wraps around: `0` goes back to `30`, and `30` goes forward to `0`.
- Click the number field to type a preset number.
- Click the circular save/overwrite button to save the current plugin state into the active slot.
- Saving overwrites only the selected slot.
- Switching slots immediately recalls that slot.
- Unused slots load the default Gateway OS state.

Each preset stores the capture/model, IR, EQ, noise gate, input/output controls, slim setting, live/offline oversampling settings, Live HQ mode, multicore mode, calibration controls, output mode, color/theme settings, and active preset number.

DAW project recall stores the full preset bank so sessions reopen with the same settings that were saved.
