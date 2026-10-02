# Mac.apk App Compatibility

Which Android apps run on Mac.apk, and how well. Updated 2026-10-01.

![apps tested: 64](https://img.shields.io/badge/apps%20tested-64-6c5ce7) ![fully playable: 48](https://img.shields.io/badge/fully%20playable-48-2ea44f) ![partly works: 10](https://img.shields.io/badge/partly%20works-10-dfb317) ![not yet: 6](https://img.shields.io/badge/not%20yet-6-e05d44) ![renders: 64 of 64](https://img.shields.io/badge/renders-64%20of%2064-0a7bbb)

**Legend:** ✅ yes · ⚠️ partly · ❌ no · ❔ not tested yet. Apps are grouped by whether they are playable; Sound is whether in-app audio works.

## ✅ Works (48)

| App | Sound | Notes |
|:----|:-----:|:------|
| **1010! Klooni** | ✅ |  |
| **Alto's Adventure** | ✅ |  |
| **Among Us** | ✅ |  |
| **Anarch RE** | ✅ |  |
| **AntennaPod** | ✅ | Now playing does not render right. |
| **Anuto TD** | ✅ |  |
| **Apple Flinger** | ✅ |  |
| **Aurora Store** | ❔ |  |
| **BobBall** | ✅ |  |
| **Calculator (Google)** | ❔ |  |
| **Calculator (OpenCalc)** | ❔ |  |
| **Candy Crush Saga** | ✅ |  |
| **Crossy Road** | ✅ |  |
| **Dumb Ways to Die** | ✅ |  |
| **F-Droid** | ❔ | Updating Mindustry from F-Droid and then opening it from F-Droid WORKS (install + cross-app launch). |
| **Feudal Tactics** | ✅ |  |
| **Frozen Bubble** | ✅ |  |
| **Fruit Ninja** | ✅ |  |
| **Geometry Dash Lite** | ✅ |  |
| **Geometry Dash Meltdown** | ✅ |  |
| **Hill Climb Racing**<br><sub>1.8.1</sub> | ✅ |  |
| **Hill Climb Racing**<br><sub>1.43.0</sub> | ✅ |  |
| **Hill Climb Racing**<br><sub>1.68.1</sub> | ✅ |  |
| **Jetpack Joyride** | ✅ |  |
| **Mindustry** | ✅ | Online multiplayer currently inop |
| **Minecraft** | ✅ | Boots, renders and Xbox sign-in works. |
| **Now in Android** | ✅ |  |
| **Open Sudoku** | ❔ |  |
| **OpenGD** | ✅ |  |
| **OpenTTD** | ✅ |  |
| **Organic Maps** | ✅ | Needs location permissions fixed |
| **Pekka Kana 2** | ✅ |  |
| **PianOli** | ✅ | Settings don't open |
| **Puzzles** | ❔ |  |
| **Rocks 'n' Diamonds** | ✅ |  |
| **Shattered Pixel Dungeon** | ✅ |  |
| **Signal** | ❔ |  |
| **Simple Solitaire Collection** | ❔ |  |
| **Smash Hit** | ✅ |  |
| **SolitaireCG** | ❔ |  |
| **Subway Surfers** | ✅ |  |
| **Super Retro Mega Wars** | ✅ |  |
| **Telegram** | ❔ |  |
| **TIC-80** | ✅ |  |
| **Unciv** | ✅ |  |
| **Unit Converter Ultimate** | ❔ |  |
| **Vector Pinball** | ✅ |  |
| **Wikipedia** | ❔ | Night mode bugs. |

## ⚠️ Partly works (10)

| App | Sound | Notes |
|:----|:-----:|:------|
| **Aegis** | ❔ | Camera access does not work. Photo access can pick a file but not process it. |
| **Clock** | ✅ | Cannot add a new clock |
| **Duolingo** | ❔ | Can't make a new account or log in |
| **Instagram** | ❔ | Weird layout issues. Video choppy and sound inop |
| **Mastodon** | ✅ | Only shows one post |
| **NewPipe** | ✅ | Some videos play with sound only and buffer constantly |
| **Plague Inc.** | ⚠️ | INSANE VOLUME, be WARNED. News doesn't work |
| **Reddit** | ✅ | Cannot log in via Google. Needs zoomed out when in full screen. Scrolling is odd. |
| **Temple Run 2** | ✅ | Playable but crashes |
| **Thunderbird** | ❔ | Sign in with Google works but log in to Thunderbird fails. |

## ❌ Does not work yet (6)

| App | Sound | Notes |
|:----|:-----:|:------|
| **AnkiDroid** | ❔ | Needs permissions fixed |
| **Efteling** | ❔ | Stuck on welcome screen. |
| **Flappy Bird** | ✅ | Touch input INOP |
| **Gallery** | ❔ | Needs file permissions fixed. |
| **Jetpack 2** | ❔ | Stuck loading at 59% |
| **VLC** | ❔ | Crashes when attempting to grant permissions. |

<details>
<summary><b>Technical details</b> (package, engine, native path, version, measurements)</summary>

Measurements come from the automated test run: render verdict, colour count, and seconds to first frame (warm and cold).

| App | Package | Icon | Renders | Measured |
|:----|:--------|:----:|:-------:|:---------|
| **1010! Klooni**<br><sub>0.8.6</sub> | `dev.lonami.klooni`<br><sub>libGDX/arc · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (1,371 colours), render 6.4 s warm, 4.3 s cold. |
| **Aegis**<br><sub>3.4.2</sub> | `com.beemdevelopment.aegis`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm TINTED (554 colours). Intro screen renders (dark UI, 92% background at full-screen size). |
| **Alto's Adventure**<br><sub>1.8.27</sub> | `com.noodlecake.altosadventure`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (37,321 colours), render 3.9 s warm, 8.4 s cold. |
| **Among Us**<br><sub>2026.6.5</sub> | `com.innersloth.spacemafia`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm SPARSE (3,433 colours), render 8.5 s warm, 22.0 s cold. |
| **Anarch RE**<br><sub>4</sub> | `dev.serwin.AnarchRE`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (34 colours), render 6.9 s warm, 7.2 s cold. |
| **AnkiDroid**<br><sub>2.24.0</sub> | `com.ichi2.anki`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (1,974 colours), render 2.6 s warm, 7.0 s cold. |
| **AntennaPod**<br><sub>3.11.4</sub> | `de.danoeh.antennapod`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm SPARSE (909 colours), render 3.6 s warm. |
| **Anuto TD**<br><sub>0.13</sub> | `ch.logixisland.anuto`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm RICH (14,110 colours), render 3.4 s warm, 4.0 s cold. |
| **Apple Flinger**<br><sub>1.6.1</sub> | `com.gitlab.ardash.appleflinger.android`<br><sub>libGDX/arc · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (82,253 colours), render 4.5 s warm, 7.7 s cold. |
| **Aurora Store**<br><sub>4.8.4</sub> | `com.aurora.store`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (58,869 colours), render 7.6 s warm, 14.9 s cold. |
| **BobBall**<br><sub>1.17</sub> | `org.bobstuff.bobball`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm CONTENT (306 colours), render 1.2 s warm, 2.1 s cold. |
| **Calculator (Google)**<br><sub>9.1 (886477075)</sub> | `com.google.android.calculator`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm CONTENT (1,291 colours), render 3.6 s warm, 5.0 s cold. |
| **Calculator (OpenCalc)**<br><sub>3.2.0</sub> | `com.darkempire78.opencalculator`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm CONTENT (1,050 colours), render 1.8 s warm, 2.9 s cold. |
| **Candy Crush Saga**<br><sub>1.323.0.1</sub> | `com.king.candycrushsaga`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (7,470 colours), render 2.1 s warm, 9.7 s cold. |
| **Clock**<br><sub>2.31</sub> | `com.best.deskclock`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm SPARSE (645 colours), render 1.8 s warm, 3.2 s cold. |
| **Crossy Road**<br><sub>7.11.1</sub> | `com.yodo1.crossyroad`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (23,736 colours), render 13.2 s warm. v1.0.1657: game clock fixed (Time.unscaledTime 2.19e6 s -> 65 s). Unity reads black to screen capture. |
| **Dumb Ways to Die**<br><sub>36.1.22</sub> | `com.popreach.dumbways`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (3,969 colours), render 2.8 s warm, 7.2 s cold. |
| **Duolingo**<br><sub>6.82.3</sub> | `com.duolingo`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (1,908 colours), render 5.7 s warm, 18.5 s cold. |
| **Efteling**<br><sub>5.24.0</sub> | `nl.efteling.android` | ✅ | ✅ | 09-28: warm none (0 colours). |
| **F-Droid**<br><sub>1.23.2</sub> | `org.fdroid.fdroid`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (1,262 colours), render 4.1 s warm, 8.2 s cold. |
| **Feudal Tactics**<br><sub>1.5.2</sub> | `de.sesu8642.feudaltactics`<br><sub>libGDX/arc · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (3,544 colours), render 8.9 s warm, 10.4 s cold. |
| **Flappy Bird**<br><sub>1.3</sub> | `com.dotgears.flappybird`<br><sub>AndEngine · ARM32 (arm32rc)</sub> | ✅ | ✅ | 09-28: warm CONTENT (698 colours), render 7.7 s warm. |
| **Frozen Bubble**<br><sub>4.4</sub> | `org.jfedor.frozenbubble`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (39,765 colours), render 1.5 s warm, 3.0 s cold. |
| **Fruit Ninja**<br><sub>3.95.5</sub> | `com.halfbrick.fruitninjafree`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (970,953 colours), render 12.5 s warm, 24.8 s cold. |
| **Gallery**<br><sub>1.13.1</sub> | `org.fossify.gallery`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm SPARSE (749 colours), render 2.6 s warm, 6.3 s cold. |
| **Geometry Dash Lite**<br><sub>2.2.11</sub> | `com.robtopx.geometryjumplite`<br><sub>cocos2d-x v2 · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (88,943 colours), render 7.9 s warm, 10.3 s cold. Plays with sound through its own org.fmod.AudioDevice at 24 kHz (v1.0.1655). |
| **Geometry Dash Meltdown**<br><sub>2.2.147</sub> | `com.robtopx.geometrydashmeltdown`<br><sub>cocos2d-x v2 · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (81,799 colours), render 4.0 s warm, 13.2 s cold. |
| **Hill Climb Racing**<br><sub>1.8.1</sub> | `com.fingersoft.hillclimb`<br><sub>plain Android (Java/Kotlin) · ARM32 (arm32rc)</sub> | ✅ | ✅ | 09-28: warm RICH (61,485 colours), render 7.1 s warm. |
| **Hill Climb Racing**<br><sub>1.43.0</sub> | `com.fingersoft.hillclimb`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (3,846 colours), render 7.5 s warm, 11.0 s cold. |
| **Hill Climb Racing**<br><sub>1.68.1</sub> | `com.fingersoft.hillclimb`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (6,975 colours), render 8.3 s warm, 9.0 s cold. |
| **Instagram**<br><sub>445.0.0.45.83</sub> | `com.instagram.android`<br><sub>Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (212,012 colours), render 7.5 s warm. Renders RICH on the installed app. |
| **Jetpack 2**<br><sub>0.1.60</sub> | `com.halfbrick.superjetpack`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (32,223 colours), render 7.9 s warm, 12.4 s cold. |
| **Jetpack Joyride**<br><sub>1.3.5</sub> | `com.halfbrick.jetpackjoyride`<br><sub>plain Android (Java/Kotlin) · ARM32 (arm32rc)</sub> | ✅ | ✅ | 09-28: warm RICH (30,653 colours), render 9.0 s warm, 10.8 s cold |
| **Mastodon**<br><sub>2.13.1</sub> | `org.joinmastodon.android`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm RICH (23,339 colours), render 1.7 s warm, 3.9 s cold. |
| **Mindustry**<br><sub>8-fdroid-158</sub> | `io.anuke.mindustry`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (9,325 colours), render 6.9 s warm, 3.7 s cold. |
| **Minecraft**<br><sub>1.26.45.1</sub> | `com.mojang.minecraftpe`<br><sub>AGDK+bgfx (RenderDragon) · Stage-6 arm64</sub> | ✅ | ✅ | Boots, renders and Xbox sign-in works (v1.0.1569/1572); RICH 20,621 on the installed app at v1.0.1656. |
| **NewPipe**<br><sub>0.29.0</sub> | `org.schabi.newpipe`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (222,746 colours), render 3.6 s warm, 9.0 s cold. |
| **Now in Android**<br><sub>0.1.2</sub> | `com.google.samples.apps.nowinandroid.demo.debug`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (5,720 colours), render 3.7 s warm, 13.0 s cold. |
| **Open Sudoku**<br><sub>4.7.0</sub> | `org.moire.opensudoku`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm RICH (11,581 colours), render 1.5 s warm, 2.6 s cold. |
| **OpenGD**<br><sub>1.0</sub> | `com.opengdteam.opengd`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (133,402 colours), render 1.6 s warm, 5.8 s cold. |
| **OpenTTD**<br><sub>14.1.rev128</sub> | `org.openttd.fdroid`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (2,762 colours), render 3.2 s warm, 2.3 s cold. |
| **Organic Maps**<br><sub>2026.07.23-6-FDroid</sub> | `app.organicmaps`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm TINTED (481 colours). |
| **Pekka Kana 2**<br><sub>1.4.5</sub> | `org.pgnapps.pk2`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (38,865 colours), render 6.8 s warm, 9.1 s cold. |
| **PianOli**<br><sub>1.27</sub> | `com.nicobrailo.pianoli`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm CONTENT (124 colours), render 1.5 s warm, 3.2 s cold. |
| **Plague Inc.**<br><sub>1.24.4</sub> | `com.miniclip.plagueinc`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (73,895 colours), render 7.0 s warm, 15.7 s cold. |
| **Puzzles**<br><sub>2025-09-12-1919-23762278-fdroid</sub> | `name.boyle.chris.sgtpuzzles`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (14,251 colours), render 2.1 s warm, 3.5 s cold. |
| **Reddit**<br><sub>2026.21.0</sub> | `com.reddit.frontpage`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm TINTED (2,670 colours). |
| **Rocks 'n' Diamonds**<br><sub>4.2.2.0</sub> | `org.artsoft.rocksndiamonds`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (43,109 colours), render 7.5 s warm, 7.8 s cold. |
| **Shattered Pixel Dungeon**<br><sub>3.3.8</sub> | `com.shatteredpixel.shatteredpixeldungeon`<br><sub>libGDX/arc · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (7,638 colours), render 3.4 s warm, 6.4 s cold. |
| **Signal**<br><sub>8.20.4</sub> | `org.thoughtcrime.securesms`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (21,484 colours), render 4.9 s warm, 15.1 s cold. |
| **Simple Solitaire Collection**<br><sub>3.13</sub> | `de.tobiasbielefeld.solitaire`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm RICH (56,166 colours), render 2.1 s warm, 3.0 s cold. |
| **Smash Hit**<br><sub>1.5.14</sub> | `com.mediocre.smashhit`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (276,922 colours), render 7.1 s warm, 8.3 s cold. |
| **SolitaireCG**<br><sub>4.1</sub> | `net.sourceforge.solitaire_cg`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm BLANK (170 colours). |
| **Subway Surfers**<br><sub>3.62.0</sub> | `com.kiloo.subwaysurf`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (530,442 colours), render 4.1 s warm. |
| **Super Retro Mega Wars**<br><sub>0.32.5</sub> | `com.serwylo.retrowars`<br><sub>libGDX/arc · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (183,837 colours), render 6.5 s warm, 6.3 s cold. |
| **Telegram**<br><sub>12.9.1</sub> | `org.telegram.messenger.web`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm SPARSE (1,734 colours), render 2.9 s warm, 14.2 s cold. |
| **Temple Run 2**<br><sub>1.133.0</sub> | `com.imangi.templerun2`<br><sub>Unity/il2cpp · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (14,377 colours), render 7.4 s warm, 13.4 s cold. |
| **Thunderbird**<br><sub>21.0</sub> | `net.thunderbird.android`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm TINTED (4,550 colours). |
| **TIC-80**<br><sub>1.01.00</sub> | `com.nesbox.tic`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm TINTED (16 colours). |
| **Unciv**<br><sub>4.20.10</sub> | `com.unciv.app`<br><sub>libGDX/arc · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (26,892 colours), render 7.5 s warm, 10.8 s cold. |
| **Unit Converter Ultimate**<br><sub>5.7.3</sub> | `com.physphil.android.unitconverterultimate`<br><sub>plain Android (Java/Kotlin) · Java only</sub> | ✅ | ✅ | 09-28: warm SPARSE (754 colours), render 3.4 s warm, 5.7 s cold. |
| **Vector Pinball**<br><sub>1.15.2</sub> | `com.dozingcatsoftware.bouncy`<br><sub>libGDX/arc · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm RICH (5,978 colours), render 3.6 s warm, 5.4 s cold. |
| **VLC**<br><sub>3.7.1</sub> | `org.videolan.vlc`<br><sub>plain Android (Java/Kotlin) · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm none (0 colours). Window opens, no frame within 45 s. |
| **Wikipedia**<br><sub>50591-r-2026-06-02</sub> | `org.wikipedia`<br><sub>pure-Java/Compose · Stage-6 arm64</sub> | ✅ | ✅ | 09-28: warm CONTENT (278,222 colours), render 3.5 s warm, 7.5 s cold. |

</details>

<sub>Generated by websites/app-compat/index.html</sub>
