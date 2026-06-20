# Gateway OS V1.2.8 macOS AU

Binary-only macOS Audio Unit release.

## Included

macOS:

- `Gateway OS V1.2.8.component`

The AU component is packaged in `GatewayOS-V1.2.8-macOS-AU.zip`.

SHA256:

`D3D81B5C7A4752870F7035DADECAB8B4450D09D411AA905850C74C73851B2B8F`

## AU Identity

- Type: `aufx`
- Subtype: `G128`
- Manufacturer: `SMfo`
- Bundle identifier: `com.SlamminMofo.audiounit.GatewayOSV128`
- Audio Unit version: `0x00010208`
- Version integer: `66056`
- Architectures: `x86_64 arm64`

## Logic Close/Reopen Fix

This hotfix addresses a Logic Pro AU lifecycle crash reported after closing the Gateway OS plug-in window and reopening it.

The AU wrapper now closes the iPlug editor when the host detaches/removes the AU view, not only when the Cocoa view is deallocated. This prevents stale editor state from surviving after Logic closes the plug-in window and allows a fresh editor to be opened safely.

## Validation

- Built on GitHub Actions in a private macOS source/build repository.
- Fixed AU editor geometry verified at `600x400`.
- AU close/reopen lifecycle hooks verified in the build.
- Staged AU bundle passed `codesign --verify --deep --strict`.
- Universal binary check confirmed `x86_64 arm64`.
- Apple AU validation passed with `auval -v aufx G128 SMfo`.
- AU validation render tests passed.

## Notes

V1.2.8 uses a new AU subtype and bundle identifier so Logic treats it as a distinct Audio Unit from V1.2.7.
