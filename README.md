# Mac.apk

**Run Android apps natively on Apple Silicon Macs. No emulator, no virtual machine, no Linux underneath.**

[![Latest release](https://img.shields.io/github/v/release/kksimp/Mac.apk-Releases?label=latest&color=6c5ce7)](../../releases/latest)
[![License: Personal Use](https://img.shields.io/badge/license-Personal%20Use-blue)](LICENSE)
[![Signed and notarized](https://img.shields.io/badge/signed-notarized%20by%20Apple-000000)](https://github.com/kksimp/Mac.apk-Releases/wiki/Installation)

### 📱 [Which apps work? See the compatibility list →](COMPATIBILITY.md)

[![Apps tested: 65](https://img.shields.io/badge/apps%20tested-65-6c5ce7)](COMPATIBILITY.md) [![Fully playable: 51](https://img.shields.io/badge/fully%20playable-51-2ea44f)](COMPATIBILITY.md) [![Partly works: 11](https://img.shields.io/badge/partly%20works-11-dfb317)](COMPATIBILITY.md) [![Not yet: 3](https://img.shields.io/badge/not%20yet-3-e05d44)](COMPATIBILITY.md)

---

**Alpha.** Mac.apk is early software under active development. Some apps run
beautifully, some run partially, and some do not run yet. It is stable enough to use
and interesting enough to explore, and it improves with every build.

## What it is

Mac.apk runs Android apps directly on Apple Silicon. Apps launch as ordinary macOS
processes, draw through the Mac's GPU, and execute on the CPU at native speed. They
appear in your Dock, get their own windows with a back button next to the traffic
lights, resize and rotate like any Mac window, and switch between light and dark
along with your Mac.

There is no emulator here, and no virtual machine. Nothing boots Android in the
background, there is no Linux kernel running underneath, and nothing is interpreted
instruction-by-instruction. Mac.apk implements the Android application environment
on top of macOS directly. [How it works →](https://github.com/kksimp/Mac.apk-Releases/wiki/How-Mac.apk-Works)

## 📖 [Read the wiki →](https://github.com/kksimp/Mac.apk-Releases/wiki)

| | |
|---|---|
| **Getting started** | [Installation](https://github.com/kksimp/Mac.apk-Releases/wiki/Installation) · [Installing apps](https://github.com/kksimp/Mac.apk-Releases/wiki/Installing-Apps) (including F-Droid and Aurora Store) · [Using apps](https://github.com/kksimp/Mac.apk-Releases/wiki/Using-Apps) · [Managing apps](https://github.com/kksimp/Mac.apk-Releases/wiki/Managing-Apps) |
| **Reference** | [Google accounts and Play Services](https://github.com/kksimp/Mac.apk-Releases/wiki/Google-Accounts-and-Play-Services) · [Known issues](https://github.com/kksimp/Mac.apk-Releases/wiki/Known-Issues) · [Troubleshooting](https://github.com/kksimp/Mac.apk-Releases/wiki/Troubleshooting) · [Reporting problems](https://github.com/kksimp/Mac.apk-Releases/wiki/Reporting-Problems) |
| **Flags and advanced settings** | [Flags](https://github.com/kksimp/Mac.apk-Releases/wiki/Flags) · [Flags reference](https://github.com/kksimp/Mac.apk-Releases/wiki/Flags-Reference) · [Developer menu](https://github.com/kksimp/Mac.apk-Releases/wiki/Developer-Menu) |
| **Behind the scenes** | [How Mac.apk works](https://github.com/kksimp/Mac.apk-Releases/wiki/How-Mac.apk-Works) · [Design decisions](https://github.com/kksimp/Mac.apk-Releases/wiki/Design-Decisions) · [For developers and publishers](https://github.com/kksimp/Mac.apk-Releases/wiki/For-Developers-and-Publishers) |

## System requirements

| | |
|---|---|
| **macOS 26.4 (Tahoe) or newer** | Required. macOS 27 works from v1.0.1702 |
| **Apple Silicon** | M1, M2, M3, M4 or newer. Intel Macs are not supported |
| **Disk** | ~280 MB for Mac.apk. Each installed app takes roughly 1.5 to 3 times its APK size |

## Quick start

1. Download the disk image from the [Releases page](../../releases/latest) and drag
   **Mac.apk** into **Applications**. It is signed and notarized by Apple, so it opens
   normally.
2. Open Mac.apk and click **Install** next to **Runtime:** in the top left.
3. Open **Settings** (the gear), find **File types**, click **Make Default**, and
   approve the macOS prompt.
4. Double-click any `.apk` (or `.apkm`, `.xapk`, `.apks`, `.apkx`), or drag it onto
   the Mac.apk window.

**The first launch of any app is slow** (up to a minute for a large one) while
Mac.apk prepares it. Later launches are fast. Full details, updating, and the app
stores are in the [Installation](https://github.com/kksimp/Mac.apk-Releases/wiki/Installation) and
[Installing apps](https://github.com/kksimp/Mac.apk-Releases/wiki/Installing-Apps) pages.

> [!WARNING]
> An Android app's saved data lives inside its own `.app`. Dragging the app to the
> Trash deletes its saves; uninstall from the Mac.apk control panel instead.
> [More →](https://github.com/kksimp/Mac.apk-Releases/wiki/Managing-Apps)

## Known issues in v1.0.1732

See [Known issues](https://github.com/kksimp/Mac.apk-Releases/wiki/Known-Issues) for this release, and the
[compatibility list](COMPATIBILITY.md) for every app tested by hand.

## Reporting problems

Send the Mac.apk version, your macOS version, the app and where you got it, what
happened, and the app's log from `~/Library/Logs/macapk/` to Kaleb@voltare.us or
[open an issue](../../issues/new). Look the log over before posting it publicly.
[What to include →](https://github.com/kksimp/Mac.apk-Releases/wiki/Reporting-Problems)

## Developers and publishers

Mac.apk serves no ads and supports no in-app purchases, by design. If you publish an
app that runs on Mac.apk and want to talk about a partnership, or would rather it
not run here, email Kaleb@voltare.us. [Details →](https://github.com/kksimp/Mac.apk-Releases/wiki/For-Developers-and-Publishers)

## License

Mac.apk is **free for personal, non-commercial use**. Commercial use, redistribution,
white-labeling, bundling, or distribution requires a separate license agreement.

By downloading and installing Mac.apk, you agree to the
[End User License Agreement](EULA.md). The full legal text is in [LICENSE](LICENSE).

## Disclaimer

Mac.apk is provided "as is", with no warranty of any kind. You are responsible for the
Android apps you choose to load, and Voltare cannot test, audit, or vouch for any
third-party APK. Voltare is not liable for damages, data loss, malware, security
incidents, copyright disputes, or any other consequence of code that runs through
Mac.apk.

**Only install APKs you trust.** An Android app running under Mac.apk runs as ordinary
native code with your macOS user account's permissions. There is no phone-style app
sandbox around it: it can read and write your files the same way any Mac app you run
can. Treat an APK exactly as you would any program you download and run yourself, and
get it from a source you trust.

## Third-party software

Mac.apk bundles several open-source components (ANGLE, MoltenVK and the Vulkan loader,
Capstone, libpng, libvpx, stb_vorbis, Bouncy Castle, a JRE built from OpenJDK together
with the libraries its font and image code uses, such as FreeType, HarfBuzz and GLib,
and the Android platform resources built from AOSP source). Each is used under its own
licence; the full notices are in [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt),
and a copy ships inside the app at `Contents/Resources/THIRD_PARTY_NOTICES.txt`.

Two of them, GLib and GNU gettext's libintl, are licensed under the LGPL. Their
complete source for the exact versions in each release (upstream source, patches and
build recipe) is attached to that release on the
[Releases page](https://github.com/kksimp/Mac.apk-Releases/releases), with
`LGPL-SOURCE-README.txt` explaining how to use a modified build.

## Links

- **Project page:** https://projects.voltare.us/macapk
- **Wiki:** https://github.com/kksimp/Mac.apk-Releases/wiki
- **Commercial licensing:** Kaleb@voltare.us
- **Bug reports:** Kaleb@voltare.us or [open an issue](../../issues/new)
