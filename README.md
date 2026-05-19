# MacDroid

**Run Android apps natively on Apple Silicon Macs. No emulator, no virtualization, no VM.**

[![Latest release](https://img.shields.io/github/v/release/kksimp/MacDroid-Releases?label=latest&color=6c5ce7)](../../releases/latest)
[![License: Personal Use](https://img.shields.io/badge/license-Personal%20Use-blue)](LICENSE)

---

## What it is

MacDroid runs Android APKs directly on Apple Silicon Macs at full native speed. Apps launch as ordinary macOS processes, render with the Mac's GPU, and use the CPU at its native speed.

Not an emulator. Not a virtual machine. No Linux running underneath, no Docker, no Rosetta, no Wine.

## Download

Grab the latest build from the [Releases page](../../releases/latest).

## System requirements

- macOS 14 Sonoma or later
- Apple Silicon (M1, M2, M3, or M4)

## Installation

1. Download the latest `MacDroid.dmg` from the Releases page.
2. Open the disk image and drag MacDroid to your Applications folder.
3. On first launch, approve MacDroid in System Settings under Privacy & Security if prompted.
4. Load an APK and run it.

## Compatibility

MacDroid is in early access. Some Android apps run fully, others run partially, and the compatible set expands with each release. Try your favorite APK and see what happens. The runtime keeps improving with every build.

## For developers and publishers

MacDroid runs your Android app on macOS, but two things that work on Android do not work here: advertising SDKs and in-app purchases. This is by design, not an oversight, and we want to explain why.

Ad networks (Google AdMob, Unity Ads, AppLovin, IronSource, Vungle, and others) require apps to be distributed through approved channels and to run on attested Android devices. Their terms of service prohibit ad serving in modified runtimes, and their fraud-detection systems are aggressive about flagging traffic that doesn't match a real Android device fingerprint. Attempting to serve real ads through MacDroid would risk getting your AdMob account terminated for facilitating fraud, which would harm you, not help you. So we stub ad SDKs as no-ops. Apps continue running normally; ads simply don't display.

In-app purchases are blocked for the same structural reasons. Google Play Billing requires a connection to Google Play Services and an attested device, neither of which MacDroid provides. We stub the billing SDK so apps don't crash on init, but purchase flows will fail gracefully rather than complete. Users cannot buy anything through MacDroid, and you receive no revenue from MacDroid users through the standard Android monetization paths.

We recognize this means MacDroid users currently play your game for free. We don't want this to be the long-term answer. If your app is running on MacDroid and you'd like to be compensated for it, we're genuinely interested in working out a partnership. Possible structures include:

- A licensed Mac distribution where users purchase a one-time unlock through a payment flow you control, with you keeping the majority of revenue
- A subscription or storefront model where MacDroid acts as a sanctioned distribution channel for your catalog on Mac
- A revenue share on a developer-specific in-app currency or premium content unlock
- Whatever structure makes sense for your business. We're flexible.

We'd rather build a small number of real publisher relationships than run an unlicensed pile of your games. If you publish an Android app that runs on MacDroid (whether it's in our compatibility list or you've tested it yourself), please reach out to Kaleb@voltare.us. Even if a partnership doesn't materialize, we want to know which developers are paying attention.

If you'd prefer your app not run on MacDroid, also reach out and we'll add it to a runtime block list. We'd rather honor that request than fight about it.

## License

MacDroid is **free for personal, non-commercial use**. Commercial use, redistribution, white-labeling, bundling, or distribution requires a separate license agreement.

By downloading and installing MacDroid, you agree to the [End User License Agreement](EULA.md). The full legal text is in [LICENSE](LICENSE).

## Disclaimer

MacDroid is provided "as is", with no warranty of any kind. You are responsible for the Android apps you choose to load, and Voltare cannot test, audit, or vouch for any third-party APK. Voltare is not liable for damages, data loss, malware, security incidents, copyright disputes, or any other consequence of code that runs through MacDroid.

## Links

- **Project page:** https://projects.voltare.us/macdroid.html
- **Commercial licensing:** Kaleb@voltare.us
- **Bug reports:** Kaleb@voltare.us or [open an issue](../../issues/new)
