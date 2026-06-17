# Gateway OS V1.1.0

Public binary-only plugin release.

## Included

macOS:

- `Gateway OS V1.1.0.component`
- `Gateway OS V1.1.0.vst3`

Both macOS formats are packaged in `GatewayOS-V1.1.0-macOS-AU-VST3.zip`.

Windows:

- `Gateway OS Preset V4.vst3`

The Windows VST3 is packaged in `GatewayOSPresetV4-Windows-VST3-x64.zip`.

macOS SHA256:

`46CD30DEF19D75B278B3BE22786990634C88EE0415FE2593E93BF3519D4DF9AA`

Windows SHA256:

`D135D89270E16118C67AF098CB241BF51CF7C0E06FFAF8C5ECF198A87AA8EBFE`

## Preset Function

- Preset slots range from `0` through `30`.
- Click `-` to move to the previous preset. Slot `0` wraps around to slot `30`.
- Click `+` to move to the next preset. Slot `30` wraps around to slot `0`.
- Click the number field to type a preset number from `0` to `30`.
- Click the circular save/overwrite control to save the current plugin state into the displayed slot.
- Saving overwrites the selected slot only.
- Switching to another slot immediately recalls that slot.
- Unsaved slots recall the default Gateway OS state.

## Preset Contents

Each slot stores the full plugin state:

- Capture/model path.
- IR path.
- Input and output levels.
- Noise gate threshold and on/off state.
- EQ bass, middle, treble, on/off state, and pre/post routing.
- Slim setting.
- Oversampling setting.
- Multicore setting.
- Input calibration on/off and calibration value.
- Output raw/normalized/calibrated mode.
- Theme color and intensity.
- Active preset number.

DAW project recall embeds the full 31-slot preset bank. Gateway OS also keeps a local external preset bank so saved slots can be used in a new session.

## Validation

- macOS CI build completed successfully.
- ARM64-aware bundle lint passed.
- AU validation passed with `auval -v aufx G100 SMfo`.
- AU version reports `1.1.0 (0x10100)`.
- Windows VST3 x64 package hash verified.
