# DualBootPatcherRefreshed

[![Build DualBootPatcherRefreshed APK](https://github.com/KodiGamingYT/DualBootPatcherRefreshed/actions/workflows/build-apk.yml/badge.svg)](https://github.com/KodiGamingYT/DualBootPatcherRefreshed/actions/workflows/build-apk.yml)
[![GitHub Release](https://img.shields.io/github/v/release/KodiGamingYT/DualBootPatcherRefreshed?include_prereleases&label=Release)](https://github.com/KodiGamingYT/DualBootPatcherRefreshed/releases)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)

**DualBootPatcherRefreshed** is a revived, community-maintained fork of the classic **DualBootPatcher** originally created by [chenxiaolong](https://github.com/chenxiaolong/DualBootPatcher).

This fork brings updated build toolchains, automated GitHub Actions CI/CD pipelines, modern Android SDK/NDK compatibility fixes, and ongoing improvements for legacy and custom ROM multi-booting setups.

---

## Features & Goals of This Fork

- **Automated Cloud Builds:** Ready-to-install APKs compiled automatically via GitHub Actions without needing an old local build environment.
- **Toolchain Modernization:** Updated CMake, Ninja, Gradle, and NDK (`r19c+`) configurations to compile cleanly on modern Linux runners.
- **Multi-ROM Booting:** Patch ZIPs (ROMs, GApps, kernels, Magisk/root packages) to install and boot multiple Android systems side-by-side on supported devices.
- **In-App ROM Management:** Switch active ROMs, share apps/data between slots, and manage boot images directly from Android.

---

## Downloads

- **Latest Builds (GitHub Releases):** Download the newest compiled APK from the [Releases](https://github.com/KodiGamingYT/DualBootPatcherRefreshed/releases) page.
- **Development Builds (Artifacts):** Grab the latest automated build directly from the [GitHub Actions](https://github.com/KodiGamingYT/DualBootPatcherRefreshed/actions/workflows/build-apk.yml) tab.
- **Legacy Original Releases:** Historical builds by `chenxiaolong` remain archived on [SourceForge](https://sourceforge.net/projects/dualbootpatcher/files/).

---

## Device Compatibility & Technical Notes

- **Classic Partition Layout (`system`, `vendor`, `boot`):** Works out of the box on devices with traditional non-dynamic partition tables.
- **System-as-Root (Android 9.0+) & Dynamic Partitions (`dm-linear` / `super`):** Devices shipping with mandatory system-as-root without boot ramdisk support or `dm-linear` dynamic partitions require device-specific patches and kernel/ramdisk workarounds. Check the issue tracker or device definitions before flashing.

> **Disclaimer:** Modifying boot images and partitions carries inherent risk. Always make a full backup (TWRP / OrangeFox / EFS) before patching or flashing ROMs.

---

## Compiling from Source

### Automated Build (GitHub Actions)
1. Fork this repository.
2. Go to **Actions** -> **Build DualBootPatcherRefreshed APK** -> **Run workflow**.
3. Download the generated APK from the workflow **Artifacts** section.

### Local Build
See the [`docs/build/`](docs/build) directory for detailed instructions on configuring CMake, Android NDK, and dependencies for Linux, Windows, and Android targets.

---

## Credits & Upstream History

- **Original Author:** [chenxiaolong](https://github.com/chenxiaolong) — creator of DualBootPatcher, `libmbbootimg`, and `libmbsystrace`.
- **Refreshed Maintainer:** [KodiGamingYT](https://github.com/KodiGamingYT)

---

## License

DualBootPatcherRefreshed is licensed under the **GNU General Public License v3.0 or later (GPLv3+)** — see the [`LICENSE`](LICENSE) file for full details.  
Third-party libraries and components remain under their respective licenses, available in the [`licenses/`](licenses/) directory.
