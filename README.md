# Meditor — Releases

**A markdown editor that publishes straight to Medium — write, preview, and ship without leaving the app.**

Meditor is a cross-platform desktop editor (Linux, macOS, Windows) built with
**Tauri 2 + Svelte 5**. It pairs a clean markdown writing experience with a
live, Medium-style preview, then publishes your post directly to your Medium
profile.

This repository contains **compiled release packages only**. Source code is
maintained in a separate private repository and is not published here.

## Downloads

| Platform | Package | Architecture | Notes |
|----------|---------|--------------|-------|
| Linux (Debian/Ubuntu) | `meditor_0.1.0_amd64.deb` | x86_64 | Published in the main v0.1.0-beta release |
| Linux (portable) | `meditor_0.1.0_amd64.AppImage` | x86_64 | Needs FUSE |
| macOS | `meditor_0.1.0_aarch64.dmg` | Apple Silicon (M1/M2/M3) | Attached to the macOS release |

## Install

- **Debian/Ubuntu:** `sudo dpkg -i meditor_0.1.0_amd64.deb`
- **Portable (any Linux):** download the `.AppImage`, `chmod +x`, and run it.
- **macOS (Apple Silicon):**
  1. Download `releases/meditor_0.1.0_aarch64.dmg`.
  2. Open the `.dmg` and drag **Meditor** to Applications (or run it directly
     from the mounted volume).
  3. Because this build is **not yet signed or notarized**, macOS will show a
     Gatekeeper warning ("app is from an unidentified developer"). To run it:
     - **Right-click** the app → **Open**, then click **Open** again, **or**
     - System Settings → Privacy & Security → allow Meditor under
       *"Developer was not identified"*.

## Notes for testers

- The Medium integration token is **write-only**: it can publish, but can't
  pull your existing posts back for editing. Edit locally and republish to
  revise.
- S3 image hosting isn't wired up yet — use Imgur or Cloudinary for now.
- The AppImage needs FUSE to run (standard for AppImages; Arch users may need
  `fusermount` from `fuse2`).
- `.deb` is for Debian/Ubuntu. Arch users: an AppImage is provided, and a
  PKGBUILD is on the way.
- **macOS:** Apple Silicon only. Intel Macs require a separate `x86_64` build
  (not yet provided). The macOS build is currently unsigned — see the macOS
  install steps above to bypass Gatekeeper.

## Feedback

This is an early beta and we'd love your input. Found a bug, or want a feature?
Reach out to the maintainer directly — it shapes what gets built next.
