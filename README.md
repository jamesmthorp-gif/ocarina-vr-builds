# Ocarina VR Builds

Windows x64 downloads for **two different editions of The Legend of Zelda: Ocarina of Time**. These are unofficial VR modifications; the underlying emulator, PC port and games are credited to their respective creators.

**[Latest downloads and detailed update notes](https://github.com/jamesmthorp-gif/ocarina-vr-builds/releases/latest)**

| Download | Your own game data | What it does |
| --- | --- | --- |
| [Lichii 3D Cinema — build 341](https://github.com/jamesmthorp-gif/ocarina-vr-builds/releases/download/v1.2.0/Lichii.3D.Cinema.Build341.zip) | Compatible Switch 2 remake dump | Depth-based stereo on the included virtual cinema screen, retaining the original third-person camera. 1440p eye images are scaled to 3840 × 2160 cinema textures per eye. |
| [Ship of Harkinian VR](https://github.com/jamesmthorp-gif/ocarina-vr-builds/releases/download/v1.2.0/Ship.of.Harkinian.VR.zip) | Supported dump of the original N64 game | The independent native third-person OpenXR mod built on [Ship of Harkinian by Harbour Masters](https://github.com/HarbourMasters/Shipwright). Includes VR and desktop launch modes. |

The correct project name is **Ship of Harkinian**, not “Arcanian.” The original PC port was created by **Harbour Masters**, not this uploader. These downloads use different game data and are not interchangeable.

## New in v1.2.0

Lichii is updated from build 316 to **build 341**, with repairs for missed stereo captures, camera selection, additional field/scale output paths, overlapping text and close-up foreground fringes. Stereo separation remains **48 mm / 0.048 game units at one unit per meter**. A new close-up limit caps each eye's displacement at 0.75% of screen width, 1.5% total, reducing extreme doubled edges. Nearby objects can therefore appear less exaggerated than in the old uncapped build.

The original camera/framing, 4K cinema output, room/lighting presets and numpad bindings are preserved. **Frame generation is disabled.** A 60 FPS cap is configured, but actual performance depends on scene and hardware. One matched RTX 3090 / 32 GiB test measured 46.28 guest FPS for the repair versus 46.78 FPS for the preceding unrepaired build 341; no speed increase is claimed. The measured gameplay and camera exercise retained stereo.

Ship of Harkinian VR is the **same approved ZIP as v1.1.0**, without new Ship code changes. See the release notes and archive READMEs for verification details and limitations.

## Start Lichii 3D Cinema — Switch 2 remake

1. Extract the entire Lichii ZIP to a writable folder. Install the [Microsoft Visual C++ x64 runtime](https://aka.ms/vc14/vc_redist.x64.exe), start SteamVR and make it the active OpenXR runtime.
2. Open Lichii/lichii.exe, configure your controller and provide your own compatible game dump, keys and required firmware from your own system. Close the emulator after setup.
3. Run Start-Lichii-3D-Cinema.cmd, select your remake dump and enter gameplay. Menus/loading screens without usable depth can appear flat.

With **Num Lock on**, **Num 1** toggles the SteamVR dashboard, **Num 3** recenters the cinema and **Num 8** toggles stereo. Num 4/5 adjust brightness, Num 6 cycles lighting, Num 7 changes screen size and Num 0 recenters the SteamVR tracking origin. Ctrl+Alt+R also recenters the screen. The archive README lists all controls and troubleshooting steps.

For updates, close both apps and back up your own saves/configuration first. Extract to a new folder and deliberately migrate your own emulator data/save location. Selecting an old NAND folder can make progress appear older. No saves are bundled.

## Start Ship of Harkinian VR — original N64 game

1. Extract the entire Ship ZIP. Keep assets and the included application resource pack soh.o2r beside soh.exe.
2. Run ShipVRLauncher.exe in desktop mode first. When prompted, supply a supported ROM dump made from your own copy. The extractor generates oot.o2r or oot-mq.o2r locally. Supported hashes are documented in the included source archive.
3. Close the game, connect a gamepad, start your active OpenXR runtime and choose **Play in VR**. DirectX 11 and the approved controller/VR settings are included.

## Contents, limits and credits

Neither download includes a game ROM/dump, generated game archive, keys, firmware, personal saves, logs, credentials or shader cache. You supply your own compatible game data. Each application ZIP includes setup instructions, applicable source materials and license notices. SHA256SUMS.txt on the release page checks both ZIPs.

Lichii cinema stereo uses depth reprojection. It cannot recover the true appearance of surfaces hidden in the original image, and some colored/translucent UI remains approximate. Missing/untrusted scene data may safely fall back to flat output. Automated geometry and routing checks do not establish physical lens comfort, every area/cutscene or long-session stability.

Upstream: [Lichii](https://github.com/zortos293/Lichii), [Eglantine](https://github.com/Djihads80/Eglantine), and [Harbour Masters / Shipwright](https://github.com/HarbourMasters/Shipwright).

Download the **named application ZIPs under Assets**. GitHub's automatic “Source code” ZIP/tar files contain this download-index repository, not the emulator distribution. Full source materials are inside the application archives. [Older releases](https://github.com/jamesmthorp-gif/ocarina-vr-builds/releases) remain available for existing links.
