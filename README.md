# Waydroid builds for LoongArch64

[简体中文](README_zh-CN.md) | English

Experimental LineageOS 23.2 / Android 16 images for running Waydroid on
LoongArch64 Linux hosts.

This repository is the distribution point for tested binary releases. See the
[Releases](https://github.com/factfinding/waydroid-loongarch64-builds/releases)
page for downloads, version-specific installation instructions, checksums, and
known issues.

## Current status

- Waydroid boots to an interactive Android desktop.
- LoongArch64 Android applications are supported.
- Chromium WebView and host audio are available.
- ARM64 application translation is available through an experimental Native
  Bridge and remains incomplete.
- Graphics acceleration is usable, but translated applications and games may
  be slow or expose compatibility issues.

## Host requirements

The current releases target:

- AOSC OS on LoongArch64;
- a 16 KiB page-size kernel with binder/binderfs support;
- a Wayland desktop session;
- the patched Waydroid and LXC packages supplied with the release.

The stock AOSC LXC package used during development disabled seccomp on
LoongArch64 and cannot be substituted for the release package unless that
packaging difference has been fixed upstream.

## Installation

Download all required files from a single release and follow the instructions
in its release notes. A complete release is expected to contain:

- `system.img.zst`;
- `vendor.img.zst`;
- a patched Waydroid host package;
- an AOSC LXC package with seccomp enabled;
- `SHA256SUMS`.

Do not mix Android images or host packages from different releases. Back up an
existing Waydroid installation before replacing images.

## Project scope

These builds are intended for testing and development. They are not official
Waydroid, LineageOS, AOSP, AOSC, or Loongson releases.

## License

Repository material is licensed under GPL-3.0; see [LICENSE](LICENSE). Binary
release contents include upstream projects under their respective licenses.
