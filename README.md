# DIscontinued since [they added in-built support to ReVanced Extended](https://github.com/j-hc/revanced-magisk-module/commit/faaf5589e2b57ba6069f165fc052f7e458929ab3), here is a new repo that uses this new in-built support since they don't build ReVanced Extended yet.
https://github.com/MatadorProBr/revanced-extended-magisk-module

#### ⚠️ Do not download modules from 3rd party sources like random websites you found on Google. Only use this repository. I am not responsible for anything they may contain.

# ReVanced Extended Magisk Module
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/rvxc_magisk)
[![Build Modules](https://github.com/MatadorProBr/revanced-extended-magisk-module/actions/workflows/build.yml/badge.svg)](https://github.com/MatadorProBr/revanced-extended-magisk-module/actions/workflows/build.yml)
[![CI](https://github.com/MatadorProBr/revanced-extended-magisk-module/actions/workflows/ci.yml/badge.svg?event=schedule)](https://github.com/MatadorProBr/revanced-extended-magisk-module/actions/workflows/ci.yml)

You can get the [latest CI release from here](https://github.com/MatadorProBr/revanced-extended-magisk-module/releases).

The [**mindetach module**](https://github.com/j-hc/mindetach-magisk) in the releases section detaches YouTube and YouTube Music from Play Store and blocks it from updating them.

## Features
 * Can build Magisk modules and non-root APKs
 * Support all present and future ReVanced Extended apps
 * Updated every hour with the latest versions of apps and patches in accordance with your configuration
 * Cleans APKs from unneeded libs to make them smaller
 * Fully open-source, every binary or APK is compiled without human intervention
 * Modules
     * recompile invalidated odex for YouTube and Music apps for faster usage
     * receive updates from Magisk app
     * do not break SafetyNet or trigger root detections used by certain apps
     * handle installation of the correct version of the stock app and all that
     * mount the patched app immediately without needing to reboot

#### **Note that the [CI workflow](../../actions/workflows/ci.yml) is scheduled to build the modules and APKs every hour using GitHub Actions if there is a change in ReVanced Extended patches. [You may want to disable it](./.github/workflows/ci.yml).**

## To include/exclude patches
[**See the list of patches**](https://github.com/inotia00/revanced-patches/tree/revanced-extended#-patches)

 * Star the repo :eyes:
 * [Fork the repo](https://github.com/MatadorProBr/revanced-extended-magisk-module/fork) or use it as a template
 * Edit the options in [`config.toml`](./config.toml)
 * Run the build [workflow](../../actions/workflows/build.yml)
 * Grab your modules and APKs from [releases](../../releases)

To add more ReVanced Extended apps or get to know more about `config.toml`, read here [`CONFIG.md`](./CONFIG.md)

To be able to use non-root variants of YT and YT Music, install [Vanced Extended MicroG](https://github.com/inotia00/VancedMicroG/releases) (recommended) or [Vanced MicroG](https://github.com/TeamVanced/VancedMicroG/releases).

## Sync the repository (only applies to forks)
The [Sync with Upstream workflow](../../actions/workflows/sync_upstream.yml) is scheduled to check for changes on this repository every 12 hours using GitHub Actions. [You may want to disable it](./.github/workflows/sync_upstream.yml).

# Building Locally
Make sure you have JDK 17 installed. Then run:

```console
$ git clone --recurse-submodules https://github.com/MatadorProBr/revanced-extended-magisk-module
$ cd revanced-extended-magisk-module
$ ./build.sh
```