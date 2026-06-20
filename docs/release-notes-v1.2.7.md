# Gateway OS V1.2.7 macOS AU

Binary-only macOS Audio Unit release.

## Included

macOS:

- `Gateway OS V1.2.7.component`

The AU component is packaged in `GatewayOS-V1.2.7-macOS-AU.zip`.

SHA256:

`D58323403A619352191FC4EE026AA9650163423994CA28C92F0CF8CE68DD8F36`

## AU Identity

- Type: `aufx`
- Subtype: `G127`
- Manufacturer: `SMfo`
- Bundle identifier: `com.SlamminMofo.audiounit.GatewayOSV127`
- Audio Unit version: `0x00010207`
- Version integer: `66055`
- Architectures: `x86_64 arm64`

## Validation

- Built on GitHub Actions `macos-15-arm64` in a private source/build repository.
- Fixed AU editor geometry verified at `600x400`.
- Staged AU bundle passed `codesign --verify --deep --strict`.
- Universal binary check confirmed `x86_64 arm64`.
- Apple AU validation passed with `auval -v aufx G127 SMfo`.
- AU validation render tests passed.

## Logic GUI Fix

This build addresses the V1.1.8 Logic AU window issue where the plugin UI could appear in a larger black host window and controls could become unresponsive.

The AU editor XIB now matches the plugin editor size, and the AU view bridge forces the fixed plugin editor size instead of accepting host-side preferred-size stretching.

## Oversampling And Presets

Gateway OS V1.2.7 includes the live/offline oversampling model used by the Windows VST3 V1.2.7 build, including separate live/offline oversampling settings and Live HQ mode. The preset state stores the added oversampling mode data.
