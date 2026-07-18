# Meditor — Releases

A distraction-free markdown editor with a built-in Medium publish pipeline.

This repository contains **compiled release packages only**. Source code is
maintained in a separate private repository and is not published here.

## Downloads

| Platform | Package | Architecture |
|----------|---------|--------------|
| macOS    | `meditor_0.1.0_aarch64.dmg` | Apple Silicon (M1 / M2 / M3) |

> Linux (`.deb` / AppImage) packages are distributed separately.

## macOS install

1. Download `releases/meditor_0.1.0_aarch64.dmg`.
2. Open the `.dmg` and drag **Meditor** to Applications (or run it directly
   from the mounted volume).
3. Because this build is **not yet signed or notarized**, macOS will show a
   Gatekeeper warning ("app is from an unidentified developer"). To run it:
   - **Right-click** the app → **Open**, then click **Open** again, **or**
   - System Settings → Privacy & Security → allow Meditor under
     *"Developer was not identified"*.

## Notes

- Apple Silicon only. Intel Macs require a separate `x86_64` build.
- The app stores your Medium integration token in the OS keyring — no
  plaintext secrets are written to disk.
- Feedback and issues can be reported to the maintainer directly.
