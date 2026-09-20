# Mac.apk

**Run Android apps natively on Apple Silicon Macs. No emulator, no virtual machine, no Linux underneath.**

[![Latest release](https://img.shields.io/github/v/release/kksimp/Mac.apk-Releases?label=latest&color=6c5ce7)](../../releases/latest)
[![License: Personal Use](https://img.shields.io/badge/license-Personal%20Use-blue)](LICENSE)
[![Signed and notarized](https://img.shields.io/badge/signed-notarized%20by%20Apple-000000)](#installation)

---

**Alpha.** Mac.apk is early software under active development. Some apps run
beautifully, some run partially, and some do not run yet. It is stable enough to use
and interesting enough to explore, and it improves with every build.

## What it is

Mac.apk runs Android apps directly on Apple Silicon. Apps launch as ordinary macOS
processes, draw through the Mac's GPU, and execute on the CPU at native speed. They
appear in your Dock, get their own windows, and behave like Mac apps because that
is what they become.

There is no emulator here, and no virtual machine. Nothing boots Android in the
background, there is no Linux kernel running underneath, and nothing is being
interpreted instruction-by-instruction. Mac.apk implements the Android application
environment on top of macOS directly, so an Android app's code runs on your
processor rather than on a simulated one.

The practical consequence is speed and integration: no VM to start, no disk image
to manage, no separate desktop to switch into.

## System requirements

| | |
|---|---|
| **macOS 26.4 (Tahoe) or newer** | Required, not recommended |
| **Apple Silicon** | M1, M2, M3, M4 or newer |
| **Disk** | ~240 MB for Mac.apk and its runtime. Apps need considerably more than their APK. See below |

**A note on disk space.** Mac.apk prepares each Android app the first time you
install it, and keeps that prepared form so subsequent launches are fast. The
result is that an installed app takes noticeably more room than its APK did: a
large 3D game can occupy several hundred megabytes, occasionally more. If you are
installing a lot of big games, budget accordingly. Uninstalling an app from the
Mac.apk control panel reclaims all of it.

**macOS 26.4 is a hard floor and Mac.apk will not work around it.** Running Android
apps that contain native code requires a platform capability that Apple introduced
in macOS 26.4. On earlier versions that capability simply does not exist, and native
Android code would misbehave in ways that are silent and very difficult to diagnose
and failures would be intermittent and misleading rather than obvious. Rather than
ship that,
Mac.apk checks for the capability at runtime and refuses to run native Android code
without it.

Intel Macs are not supported and will not be. Mac.apk runs Android's ARM code
directly on your ARM processor, which is not something an Intel chip can do.

---

## Installation

Four steps, once. After that you can install Android apps by double-clicking them.

### 1. Install Mac.apk

Download the disk image from the [Releases page](../../releases/latest), open it,
and drag **Mac.apk** into your **Applications** folder. The disk image gives you an
Applications shortcut to drop it on.

Mac.apk is signed with an Apple Developer ID and notarized by Apple, so it opens
normally, with no right-click-to-open, no "unidentified developer" warning, and no
trip to System Settings.

### 2. Open Mac.apk

Launch it from Applications. You will get the Mac.apk control panel: a window with a
drop zone, your installed Android apps, and a **Runtime:** indicator in the top left.

### 3. Install the runtime

In the top left, next to **Runtime:**, click **Install**.

This unpacks the Android runtime that your apps will actually execute. It is a
one-time, per-user step, it does not need your password, and it takes a few seconds.
The indicator will change to **Runtime: Installed**.

If you skip this step, Mac.apk installs the runtime for you the first time you try to
install an Android app. Doing it deliberately here just means you see it happen rather
than wondering what the pause was.

### 4. Make Mac.apk the default for APK files

Open **Settings** (the gear icon at the top right of the control panel), find
**File types**, and click **Make Default**.

macOS will ask you to confirm. This is a system prompt, and macOS reserves that
choice for you rather than letting an app take it silently. Approve it, and from
then on `.apk` files, plus the `.apkm`, `.xapk`, `.apks` and `.apkx` split-bundle
formats, belong to Mac.apk.

**You are done.** From here, installing an Android app is a double-click.

---

## Installing Android apps

**The first launch of any app is slow.** Mac.apk prepares the app the first time you
install or open it, which can take up to a minute for a large one. It is doing work,
not hanging, and it only happens once, and later launches are fast. Please don't report
the first launch as a freeze.

### Double-click an APK

Once step 4 is done, double-clicking any `.apk` in Finder hands it to Mac.apk, which
walks you through installing it. Split bundles (`.apkm`, `.xapk`, `.apks` and
`.apkx`) work the same way and are merged for you automatically.

### Drag and drop

Drag an APK onto the Mac.apk window. Same result, useful when Mac.apk is already open.

### Install from an app store, inside Mac.apk

This is the part people tend not to expect: **Android app stores run on Mac.apk, and
they can install apps.** You do not have to find APK files yourself.

#### F-Droid

[F-Droid](https://f-droid.org) is the open-source Android app catalog. Install the
F-Droid APK once, open it in Mac.apk, and browse and install from its whole catalog
the way you would on a phone. Browsing, downloading and installing all work.

#### Aurora Store

[Aurora Store](https://auroraoss.com) is an open-source client for the Google Play
catalog, the same apps you would find on a phone. It runs on Mac.apk and installs
from that catalog, so between it and F-Droid most of what you would want is a search
away rather than a file you have to go hunting for.

It needs **one setup step** first, and it will not download anything until you do it:

> [!IMPORTANT]
> Aurora Store will not download anything until you give it a device profile. This is
> a one-time setup step, inside Aurora itself.

Mac.apk reports itself honestly: it tells apps it is a Mac.apk device, because
pretending to be a specific certified Android handset is not something this project
does. Google's servers, however, only serve app downloads to a device they recognise,
so Aurora needs to be told which device to ask as. Aurora has this built in.

1. Open **Aurora Store** in Mac.apk
2. Tap **More** (top right of the catalogue), then **Spoof manager**, then **Device**
3. Select **Pixel Tablet**
4. Restart Aurora Store when it prompts you
5. **Sign in again, Anonymous.** This step is required, not optional. The device
   profile is sent to Google only at sign-in, so changing it without a fresh login
   silently does nothing at all.

**Use the Pixel Tablet profile specifically.** Aurora bundles more than twenty, but
Pixel Tablet is the one whose architecture matches Mac.apk exactly, so the app builds
Google serves you are the ones that actually run here, rather than builds for a
different kind of chip. It is also the profile we test against, and the first thing we
will ask about if you report a problem with a store-installed app.

This is a normal Aurora Store feature that Aurora ships for exactly this purpose, and
it affects only which catalog Google shows you.

### Installs from inside an app ask for Touch ID

When F-Droid or Aurora Store installs or removes something, macOS asks you to
authenticate first with Touch ID or your password. That is deliberate and cannot be
turned off. An Android app running on your Mac should never be able to install or
delete software without you personally approving it, so the approval is enforced
outside the Android app entirely. Expect the prompt; it is not a bug.

**A note on what stores can and cannot do:** you can browse, download, install and
uninstall. Updating through a store is not something we have tested, so treat it as
unproven rather than broken. You cannot make purchases. See
[For developers and publishers](#for-developers-and-publishers) below for why that
is deliberate.

### Managing what you have installed

Installing an Android app gives it a real place on your Mac. It gets its own entry
in your **Applications** folder, under its own name and with its own icon, so
"Crossy Road" is a Mac app called Crossy Road, launchable from the Dock, Spotlight
or Launchpad, and pinnable like anything else. You do not have to open Mac.apk
first, and you do not go through a launcher every time.

**An Android app's saved data lives inside its own `.app`**, the same way the app
itself does. That keeps everything self-contained: one app, one bundle, nothing
scattered around your home folder. It has one consequence worth knowing.

> [!WARNING]
> Dragging an Android app to the Trash takes its saved data with it. Uninstall from
> the Mac.apk control panel instead.

Because the saves live inside the bundle, moving the app to the Trash yourself
destroys them, and nothing warns you, because as far as macOS is concerned you just
deleted an app.

Uninstalling from the Mac.apk control panel does the right thing instead. It shows you
how much saved data there is, sets that data aside before removing the app, and
reinstalling the same version puts it back where it was. If you would rather the data
were destroyed too, there is a checkbox for that in the confirmation.

One detail: kept data is matched **per version**. Reinstalling the exact version you
removed restores your saves; installing a different version starts fresh and leaves
the old data waiting for its own version.

The Mac.apk control panel is the place to see everything you have installed and to
remove things, and it names exactly what is about to go before it does anything.

---

## Compatibility

Mac.apk is in alpha, and honesty serves you better than a marketing number here.

- **Many apps run well.** Utilities, readers, tools, open-source apps and a good
  number of games run properly, including apps with substantial native code.
- **Some apps run partially.** They start and are usable, but something is wrong:
  a visual glitch, a feature that does not respond, audio that does not play.
- **Some apps do not run yet.** Usually something specific is missing, and usually
  it gets fixed.
- **Anything that requires Google Play Services** in a meaningful way (sign-in with
  Google, Play Billing, push notifications, Play Integrity) will not work. Mac.apk
  is not a Google-certified Android device and does not claim to be.

The compatible set grows with every release. If an app you care about does not work,
tell us. That is genuinely how the list gets shorter.

---

## Advanced: flags and settings

Most people never need any of this. Every app installs and runs with the defaults, and
the Mac.apk window's Settings cover the everyday choices (window size, orientation,
logging). But the runtime also reads a set of environment variables and command-line
flags, and a few of them are worth knowing when something needs adjusting or when you
are gathering a bug report.

**Where to set them**

- **In the Mac.apk window.** Settings has a **Default environment** editor whose
  key=value lines apply to every app you launch from the window, and each app's
  **Get Info** sheet has its own editor for that one app (it wins over the default).
  These apply to launches started from the Mac.apk window.
- **From Terminal, for an installed app.** Pass the variable on the `open` command,
  which hands it to the app's own process:

  ```
  open --env MACAPK_LOG_LEVEL=7 -a "/Applications/Crossy Road.app"
  ```

  Or run the app's executable directly with the variable in front of it:
  `MACAPK_LOG_LEVEL=7 "/Applications/Crossy Road.app/Contents/MacOS/Crossy Road"`.

**The ones worth knowing**

| Flag | What it does |
|---|---|
| `MACAPK_FOLLOW_SYSTEM_APPEARANCE=0` | Forces light mode regardless of the Mac's appearance. Unset (the default) follows macOS's light/dark setting. |
| `MACAPK_LOG_LEVEL=<0-7>` | How much the app's log records. Unset is the normal amount (Android's INFO floor). `7` records everything, which is what a bug report wants. |
| `MACAPK_FULLSCREEN=1` (or `--fullscreen`) | Runs the app in a fullscreen window instead of a titled one. |
| `MACAPK_HIDE_DOCK_ICON=1` (or `--hide-dock-icon`) | Hides the app's Dock icon for that launch. |
| `--orientation auto\|portrait\|landscape` | Window orientation. `auto` reads the app's own declared orientation and otherwise picks portrait. Also a picker in Settings. |
| `--width N --height N` | An explicit window size in pixels instead of the orientation's default. Also a picker in Settings. |
| `MACAPK_ANDROID_ROOT=<dir>` (or `--android-root`) | Where the runtime keeps the Android filesystem it presents to the app. An installed app always uses the folder inside its own bundle; this matters only when running an APK directly. |
| `MACAPK_FORCE_ABI=armeabi-v7a` (or `--force-abi`) | Runs the app's 32-bit ARM native code (through the recompiler) even when it ships 64-bit code. For diagnosis; also the "Force ARM32" toggle in the Mac.apk window's developer menu. |
| `MACAPK_DEV_TRACE=1` (or `--dev-trace`) | Turns on the broad diagnostic trace. Expect about one frame per second in a big game while it is on. Also the "Verbose trace" toggle in the developer menu. |
| `MACAPK_INSTALL_NOUI=1` | Skips the install confirmation dialog, for scripted installs: `open --env MACAPK_INSTALL_NOUI=1 -a /Applications/Mac.apk.app <apk>`. |
| `MACAPK_EXTRACT_ASSETS=1` | Restores the older behaviour of copying an app's assets out onto disk instead of reading them from the installed APK in place. Only worth trying if an app that used to work stops finding its own files. |
| `MACAPK_ALLOW_UNSAFE_X18=1` | Lets an app with 64-bit native code load even when the macOS 26.4 check for it fails. Diagnosis only; it does not make an unsupported macOS work. |

The runtime has a few hundred more, nearly all of them diagnostic switches and bisect
gates for developers. Every one of them, with its default, its accepted values and
what it does, is listed in [FLAGS.md](FLAGS.md).

---

## For developers and publishers

Mac.apk runs your Android app on macOS, but two things that work on Android do not
work here: advertising SDKs and in-app purchases. This is by design, not an oversight,
and we want to explain why.

Ad networks require apps to be distributed through approved channels and to run on attested
Android devices. Their terms of service prohibit ad serving in modified runtimes, and
their fraud-detection systems are aggressive about flagging traffic that doesn't match
a real Android device fingerprint. Attempting to serve real ads through Mac.apk would
risk getting your AdMob account terminated for facilitating fraud, which would harm
you, not help you. So Mac.apk reaches no ad backend at all: an ad request initializes
normally and then returns **no fill**, exactly as a real device with no reachable ad
configuration does. No impression, click, or paid event is ever fabricated. Apps keep
running; ads simply don't display.

In-app purchases are blocked for the same structural reasons. Google Play Billing
requires a connection to Google Play Services and an attested device, neither of which
Mac.apk provides. We stub the billing SDK so apps don't crash on init, but purchase
flows will fail gracefully rather than complete. Users cannot buy anything through
Mac.apk, and you receive no revenue from Mac.apk users through the standard Android
monetization paths.

We recognize this means Mac.apk users currently play your game for free. We don't want
this to be the long-term answer. If your app is running on Mac.apk and you'd like to be
compensated for it, we're genuinely interested in working out a partnership. Possible
structures include:

- A licensed Mac distribution where users purchase a one-time unlock through a payment
  flow you control, with you keeping the majority of revenue
- A subscription or storefront model where Mac.apk acts as a sanctioned distribution
  channel for your catalog on Mac
- A revenue share on a developer-specific in-app currency or premium content unlock
- Whatever structure makes sense for your business. We're flexible.

We'd rather build a small number of real publisher relationships than run an unlicensed
pile of your games. If you publish an Android app that runs on Mac.apk, please reach out
to Kaleb@voltare.us. Even if a partnership doesn't materialize, we want to know which
developers are paying attention.

If you'd prefer your app not run on Mac.apk, also reach out and we'll add it to a
runtime block list. We'd rather honor that request than fight about it.

---

## Reporting problems

Bug reports are useful to us, and the alpha is the point at which they matter most.

A good report includes:

- **The Mac.apk version.** Mac.apk → About Mac.apk. (Or select Mac.apk in
  Applications and press ⌘I.)
- **Your macOS version.** Apple menu, then About This Mac. Or run
  `sw_vers -productVersion` in Terminal.
- **Which app**, including where you got it and its version.
- **What happened**, and what you expected instead. A screenshot is worth a lot.
- **The app's log**, which is the single most useful attachment. Logs live in
  `~/Library/Logs/macapk/`, one per app, named
  `app_<package>_<version>.log`. In Finder, press ⇧⌘G and paste that path.

Send it to Kaleb@voltare.us or [open an issue](../../issues/new).

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

## Links

- **Project page:** https://projects.voltare.us/macapk
- **Commercial licensing:** Kaleb@voltare.us
- **Bug reports:** Kaleb@voltare.us or [open an issue](../../issues/new)
