# Mac.apk — App Compatibility

_64 apps · 48 playable · 64 render · updated 2026-10-01_

**Legend:** ✅ works · ⚠️ partial · ❌ no · — untested

| App | Bundle | Engine | Native path | Version | Icon | Sound | Renders | Playable | Notes |
|:----|:-------|:-------|:------------|:--------|:----:|:-----:|:-------:|:--------:|:------|
| 1010! Klooni | `dev.lonami.klooni` | libGDX/arc | Stage-6 arm64 | 0.8.6 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (1,371 colours), render 6.4 s warm, 4.3 s cold. |
| Aegis | `com.beemdevelopment.aegis` | plain Android (Java/Kotlin) | Stage-6 arm64 | 3.4.2 | ✅ | — | ✅ | ⚠️ | 09-28: warm TINTED (554 colours). Intro screen renders (dark UI, 92% background at full-screen size). Camera access does not work. Photo access can pick a gile but not process it. |
| Alto's Adventure | `com.noodlecake.altosadventure` | Unity/il2cpp | Stage-6 arm64 | 1.8.27 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (37,321 colours), render 3.9 s warm, 8.4 s cold. |
| Among Us | `com.innersloth.spacemafia` | Unity/il2cpp | Stage-6 arm64 | 2026.6.5 | ✅ | ✅ | ✅ | ✅ | 09-28: warm SPARSE (3,433 colours), render 8.5 s warm, 22.0 s cold. |
| Anarch RE | `dev.serwin.AnarchRE` | plain Android (Java/Kotlin) | Stage-6 arm64 | 4 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (34 colours), render 6.9 s warm, 7.2 s cold. |
| AnkiDroid | `com.ichi2.anki` | plain Android (Java/Kotlin) | Stage-6 arm64 | 2.24.0 | ✅ | — | ✅ | ❌ | 09-28: warm CONTENT (1,974 colours), render 2.6 s warm, 7.0 s cold. / Needs permissions fixed |
| AntennaPod | `de.danoeh.antennapod` | plain Android (Java/Kotlin) | Stage-6 arm64 | 3.11.4 | ✅ | ✅ | ✅ | ✅ | 09-28: warm SPARSE (909 colours), render 3.6 s warm. Now playing does not render right. |
| Anuto TD | `ch.logixisland.anuto` | plain Android (Java/Kotlin) | Java only | 0.13 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (14,110 colours), render 3.4 s warm, 4.0 s cold. |
| Apple Flinger | `com.gitlab.ardash.appleflinger.android` | libGDX/arc | Stage-6 arm64 | 1.6.1 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (82,253 colours), render 4.5 s warm, 7.7 s cold. |
| Aurora Store | `com.aurora.store` | pure-Java/Compose | Stage-6 arm64 | 4.8.4 | ✅ | — | ✅ | ✅ | 09-28: warm RICH (58,869 colours), render 7.6 s warm, 14.9 s cold. |
| BobBall | `org.bobstuff.bobball` | plain Android (Java/Kotlin) | Java only | 1.17 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (306 colours), render 1.2 s warm, 2.1 s cold. |
| Calculator (Google) | `com.google.android.calculator` | plain Android (Java/Kotlin) | Java only | 9.1 (886477075) | ✅ | — | ✅ | ✅ | 09-28: warm CONTENT (1,291 colours), render 3.6 s warm, 5.0 s cold. |
| Calculator (OpenCalc) | `com.darkempire78.opencalculator` | plain Android (Java/Kotlin) | Java only | 3.2.0 | ✅ | — | ✅ | ✅ | 09-28: warm CONTENT (1,050 colours), render 1.8 s warm, 2.9 s cold. |
| Candy Crush Saga | `com.king.candycrushsaga` | pure-Java/Compose | Stage-6 arm64 | 1.323.0.1 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (7,470 colours), render 2.1 s warm, 9.7 s cold. |
| Clock | `com.best.deskclock` | plain Android (Java/Kotlin) | Java only | 2.31 | ✅ | ✅ | ✅ | ⚠️ | 09-28: warm SPARSE (645 colours), render 1.8 s warm, 3.2 s cold. Cannot add a new clock |
| Crossy Road | `com.yodo1.crossyroad` | Unity/il2cpp | Stage-6 arm64 | 7.11.1 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (23,736 colours), render 13.2 s warm. v1.0.1657: game clock fixed (Time.unscaledTime 2.19e6 s -> 65 s). Unity reads black to screen capture. |
| Dumb Ways To Die | `com.popreach.dumbways` | Unity/il2cpp | Stage-6 arm64 | 36.1.22 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (3,969 colours), render 2.8 s warm, 7.2 s cold. |
| Duolingo | `com.duolingo` | Unity/il2cpp | Stage-6 arm64 | 6.82.3 | ✅ | — | ✅ | ⚠️ | 09-28: warm CONTENT (1,908 colours), render 5.7 s warm, 18.5 s cold. Cant make a new account or log in |
| Efteling | `nl.efteling.android` | — | — | 5.24.0 | ✅ | — | ✅ | ❌ | 09-28: warm none (0 colours). Stuck on welcome screen. |
| F-Droid | `org.fdroid.fdroid` | pure-Java/Compose | Stage-6 arm64 | 1.23.2 | ✅ | — | ✅ | ✅ | 09-28: warm CONTENT (1,262 colours), render 4.1 s warm, 8.2 s cold. Owner 09-28: updating Mindustry from F-Droid and then opening it from F-Droid WORKS (install + cross-app launch). |
| Feudal Tactics | `de.sesu8642.feudaltactics` | libGDX/arc | Stage-6 arm64 | 1.5.2 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (3,544 colours), render 8.9 s warm, 10.4 s cold. |
| Flappy Bird | `com.dotgears.flappybird` | AndEngine | ARM32 (arm32rc) | 1.3 | ✅ | ✅ | ✅ | ❌ | 09-28: warm CONTENT (698 colours), render 7.7 s warm. Touch input INOP |
| Frozen Bubble | `org.jfedor.frozenbubble` | plain Android (Java/Kotlin) | Stage-6 arm64 | 4.4 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (39,765 colours), render 1.5 s warm, 3.0 s cold. |
| Fruit Ninja | `com.halfbrick.fruitninjafree` | Unity/il2cpp | Stage-6 arm64 | 3.95.5 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (970,953 colours), render 12.5 s warm, 24.8 s cold. |
| Gallery | `org.fossify.gallery` | pure-Java/Compose | Stage-6 arm64 | 1.13.1 | ✅ | — | ✅ | ❌ | 09-28: warm SPARSE (749 colours), render 2.6 s warm, 6.3 s cold. needs file permissions fixed. |
| Geometry Dash Lite | `com.robtopx.geometryjumplite` | cocos2d-x v2 | Stage-6 arm64 | 2.2.11 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (88,943 colours), render 7.9 s warm, 10.3 s cold. Plays with sound through its own org.fmod.AudioDevice at 24 kHz (v1.0.1655). |
| Geometry Dash Meltdown | `com.robtopx.geometrydashmeltdown` | cocos2d-x v2 | Stage-6 arm64 | 2.2.147 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (81,799 colours), render 4.0 s warm, 13.2 s cold. |
| Hill Climb Racing | `com.fingersoft.hillclimb` | plain Android (Java/Kotlin) | Stage-6 arm64 | 1.43.0 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (3,846 colours), render 7.5 s warm, 11.0 s cold. |
| Hill Climb Racing | `com.fingersoft.hillclimb` | pure-Java/Compose | Stage-6 arm64 | 1.68.1 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (6,975 colours), render 8.3 s warm, 9.0 s cold. |
| Hill Climb Racing | `com.fingersoft.hillclimb` | plain Android (Java/Kotlin) | ARM32 (arm32rc) | 1.8.1 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (61,485 colours), render 7.1 s warm. |
| Instagram | `com.instagram.android` | — | Stage-6 arm64 | 445.0.0.45.83 | ✅ | — | ✅ | ⚠️ | 09-28: warm RICH (212,012 colours), render 7.5 s warm. Renders RICH on the installed app; Weird layout issues. Video Choppy and sound inop |
| Jetpack 2 | `com.halfbrick.superjetpack` | plain Android (Java/Kotlin) | Stage-6 arm64 | 0.1.60 | ✅ | — | ✅ | ❌ | 09-28: warm CONTENT (32,223 colours), render 7.9 s warm, 12.4 s cold. Stuck loading at 59% |
| Jetpack Joyride | `com.halfbrick.jetpackjoyride` | plain Android (Java/Kotlin) | ARM32 (arm32rc) | 1.3.5 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (30,653 colours), render 9.0 s warm, 10.8 s cold |
| Mastodon | `org.joinmastodon.android` | plain Android (Java/Kotlin) | Java only | 2.13.1 | ✅ | ✅ | ✅ | ⚠️ | 09-28: warm RICH (23,339 colours), render 1.7 s warm, 3.9 s cold. Only shows one post |
| Mindustry | `io.anuke.mindustry` | plain Android (Java/Kotlin) | Stage-6 arm64 | 8-fdroid-158 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (9,325 colours), render 6.9 s warm, 3.7 s cold. Online multiplayer currently inop |
| Minecraft | `com.mojang.minecraftpe` | AGDK+bgfx (RenderDragon) | Stage-6 arm64 | 1.26.45.1 | ✅ | ✅ | ✅ | ✅ | Boots, renders and Xbox sign-in works (v1.0.1569/1572); RICH 20,621 on the installed app at v1.0.1656. |
| NewPipe | `org.schabi.newpipe` | pure-Java/Compose | Stage-6 arm64 | 0.29.0 | ✅ | ✅ | ✅ | ⚠️ | 09-28: warm RICH (222,746 colours), render 3.6 s warm, 9.0 s cold. some Videos play with sound only and buffer constantly |
| Now in Android | `com.google.samples.apps.nowinandroid.demo.debug` | pure-Java/Compose | Stage-6 arm64 | 0.1.2 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (5,720 colours), render 3.7 s warm, 13.0 s cold. |
| Open Sudoku | `org.moire.opensudoku` | plain Android (Java/Kotlin) | Java only | 4.7.0 | ✅ | — | ✅ | ✅ | 09-28: warm RICH (11,581 colours), render 1.5 s warm, 2.6 s cold. Weird menu glitches and numbers cannot be inputted. Icon shows in dock but not app drawer. |
| OpenGD | `com.opengdteam.opengd` | plain Android (Java/Kotlin) | Stage-6 arm64 | 1.0 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (133,402 colours), render 1.6 s warm, 5.8 s cold. |
| OpenTTD | `org.openttd.fdroid` | plain Android (Java/Kotlin) | Stage-6 arm64 | 14.1.rev128 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (2,762 colours), render 3.2 s warm, 2.3 s cold. Touch input seems inoperable but loads to main menu |
| Organic Maps | `app.organicmaps` | plain Android (Java/Kotlin) | Stage-6 arm64 | 2026.07.23-6-FDroid | ✅ | ✅ | ✅ | ✅ | 09-28: warm TINTED (481 colours). Needs locations permissions fixed |
| Pekka Kana 2 | `org.pgnapps.pk2` | plain Android (Java/Kotlin) | Stage-6 arm64 | 1.4.5 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (38,865 colours), render 6.8 s warm, 9.1 s cold. |
| PianOli | `com.nicobrailo.pianoli` | plain Android (Java/Kotlin) | Java only | 1.27 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (124 colours), render 1.5 s warm, 3.2 s cold. Settings dont open |
| Plague Inc. | `com.miniclip.plagueinc` | plain Android (Java/Kotlin) | Stage-6 arm64 | 1.24.4 | ✅ | ⚠️ | ✅ | ⚠️ | 09-28: warm RICH (73,895 colours), render 7.0 s warm, 15.7 s cold. INSANE VOLUME be WARNED. news doesnt work |
| Puzzles | `name.boyle.chris.sgtpuzzles` | pure-Java/Compose | Stage-6 arm64 | 2025-09-12-1919-23762278-fdroid | ✅ | — | ✅ | ✅ | 09-28: warm RICH (14,251 colours), render 2.1 s warm, 3.5 s cold. |
| Reddit | `com.reddit.frontpage` | pure-Java/Compose | Stage-6 arm64 | 2026.21.0 | ✅ | ✅ | ✅ | ⚠️ | 09-28: warm TINTED (2,670 colours). Cannot log in via google. Needs zoomed out when in full screen. Scrolling is odd. |
| Rocks 'n' Diamonds | `org.artsoft.rocksndiamonds` | plain Android (Java/Kotlin) | Stage-6 arm64 | 4.2.2.0 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (43,109 colours), render 7.5 s warm, 7.8 s cold. |
| Shattered Pixel Dungeon | `com.shatteredpixel.shatteredpixeldungeon` | libGDX/arc | Stage-6 arm64 | 3.3.8 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (7,638 colours), render 3.4 s warm, 6.4 s cold. |
| Signal | `org.thoughtcrime.securesms` | pure-Java/Compose | Stage-6 arm64 | 8.20.4 | ✅ | — | ✅ | ✅ | 09-28: warm CONTENT (21,484 colours), render 4.9 s warm, 15.1 s cold. |
| Simple Solitaire Collection | `de.tobiasbielefeld.solitaire` | plain Android (Java/Kotlin) | Java only | 3.13 | ✅ | — | ✅ | ✅ | 09-28: warm RICH (56,166 colours), render 2.1 s warm, 3.0 s cold. |
| Smash Hit | `com.mediocre.smashhit` | plain Android (Java/Kotlin) | Stage-6 arm64 | 1.5.14 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (276,922 colours), render 7.1 s warm, 8.3 s cold. |
| SolitaireCG | `net.sourceforge.solitaire_cg` | plain Android (Java/Kotlin) | Java only | 4.1 | ✅ | — | ✅ | ✅ | 09-28: warm BLANK (170 colours). |
| Subway Surf | `com.kiloo.subwaysurf` | Unity/il2cpp | Stage-6 arm64 | 3.62.0 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (530,442 colours), render 4.1 s warm. |
| Super Retro Mega Wars | `com.serwylo.retrowars` | libGDX/arc | Stage-6 arm64 | 0.32.5 | ✅ | ✅ | ✅ | ✅ | 09-28: warm CONTENT (183,837 colours), render 6.5 s warm, 6.3 s cold. |
| Telegram | `org.telegram.messenger.web` | plain Android (Java/Kotlin) | Stage-6 arm64 | 12.9.1 | ✅ | — | ✅ | ✅ | 09-28: warm SPARSE (1,734 colours), render 2.9 s warm, 14.2 s cold. |
| Temple Run 2 | `com.imangi.templerun2` | Unity/il2cpp | Stage-6 arm64 | 1.133.0 | ✅ | ✅ | ✅ | ⚠️ | 09-28: warm RICH (14,377 colours), render 7.4 s warm, 13.4 s cold. PLayable but crashes |
| Thunderbird | `net.thunderbird.android` | pure-Java/Compose | Stage-6 arm64 | 21.0 | ✅ | — | ✅ | ⚠️ | 09-28: warm TINTED (4,550 colours). Sign in with google works but log in to thunderbird fails. |
| TIC-80 | `com.nesbox.tic` | plain Android (Java/Kotlin) | Stage-6 arm64 | 1.01.00 | ✅ | ✅ | ✅ | ✅ | 09-28: warm TINTED (16 colours). |
| Unciv | `com.unciv.app` | libGDX/arc | Stage-6 arm64 | 4.20.10 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (26,892 colours), render 7.5 s warm, 10.8 s cold. |
| Unit Converter Ultimate | `com.physphil.android.unitconverterultimate` | plain Android (Java/Kotlin) | Java only | 5.7.3 | ✅ | — | ✅ | ✅ | 09-28: warm SPARSE (754 colours), render 3.4 s warm, 5.7 s cold. |
| Vector Pinball | `com.dozingcatsoftware.bouncy` | libGDX/arc | Stage-6 arm64 | 1.15.2 | ✅ | ✅ | ✅ | ✅ | 09-28: warm RICH (5,978 colours), render 3.6 s warm, 5.4 s cold. |
| VLC | `org.videolan.vlc` | plain Android (Java/Kotlin) | Stage-6 arm64 | 3.7.1 | ✅ | — | ✅ | ❌ | 09-28: warm none (0 colours). Window opens, no frame within 45 s. crahes when attempting to grant permissions. |
| Wikipedia | `org.wikipedia` | pure-Java/Compose | Stage-6 arm64 | 50591-r-2026-06-02 | ✅ | — | ✅ | ✅ | 09-28: warm CONTENT (278,222 colours), render 3.5 s warm, 7.5 s cold. Night mode bugs. |

<sub>Generated by websites/app-compat/index.html</sub>
