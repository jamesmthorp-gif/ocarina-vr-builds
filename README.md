# Ocarina VR Builds

Windows x64 downloads for two different editions of Ocarina of Time. These are unofficial VR modifications; the underlying emulator, PC port and games belong to their respective creators.

[Latest downloads and detailed update notes](../../releases/latest)

| Download | Game you supply | Experience |
| --- | --- | --- |
| [Lichii 3D Cinema — build 386](../../releases/download/v1.3.0/Lichii.3D.Cinema.Build386.zip) | Your own compatible Switch 2 remake dump | Depth-reprojected stereo on the included virtual cinema screen, preserving the original third-person camera. 2560 × 1440 eye transport is scaled to 3840 × 2160 theater textures per eye. |
| [Ship of Harkinian VR](../../releases/download/v1.3.0/Ship.of.Harkinian.VR.zip) | Your own supported original N64 ROM dump | Separate native third-person OpenXR VR mod built on [Ship of Harkinian by Harbour Masters](https://github.com/HarbourMasters/Shipwright), with VR and desktop modes. |

## New in v1.3.0

Lichii now uses build 386, with immutable per-draw camera snapshots, same-frame/crop flat fallback, depth-aware silhouette filtering and the upstream emulator fixes. The player confirmed depth working in the current build. Three post-restart camera sweeps did not reproduce an earlier Forest Temple session issue; the precise cause of that earlier issue was not established.

Preserves 48 mm producer separation, the 1.5% total close-up disparity cap, original camera, 4K theater textures, room/lighting presets and numpad controls. Screen distance is 3.0 m at 4.5 m width. Frame generation remains off. Uses zero frames ahead, render follower off and shader precompile Always. Startup requires at least 18 GiB free RAM and 34 GiB available Windows commitment, which includes paging capacity.

Audio uses SDL3, stereo and Windows default output so it follows the default instead of remaining pinned to a disconnected physical endpoint. Select your headset output in Windows before launch. Physical unplug/replug recovery was not deliberately tested. Ship of Harkinian is the same previously approved ZIP, with no new Ship changes.

## Start Lichii 3D Cinema — Switch 2 remake

1. Extract the entire ZIP to a writable folder. Install the [Microsoft Visual C++ x64 runtime](https://aka.ms/vc14/vc_redist.x64.exe), start SteamVR and make it the active OpenXR runtime.
2. Open Lichii/lichii.exe, configure your controller and supply your own compatible game dump, keys and any required firmware from your own system. Close Lichii after setup.
3. Run Start-Lichii-3D-Cinema.cmd, select your remake dump and continue into gameplay. First shader preparation can take several minutes. Menus/loading screens can be flat.
4. Num Lock on: Num 1 toggles the SteamVR dashboard; Num 3 or Ctrl+Alt+R recenters the cinema; Num 8 toggles stereo. Num 4/5 adjust brightness, Num 6 cycles lighting, Num 7 changes screen size and Num 0 recenters the tracking origin.

Back up your saves/configuration before an update, then deliberately migrate your own emulator data. Selecting an old NAND location can make progress appear older. Do not overwrite the modified executable with the stock emulator: that removes this integration. No saves are supplied.

## Start Ship of Harkinian VR — original N64 game

The correct name is **Ship of Harkinian**, by **Harbour Masters**, not Arcanian. The underlying native PC port was not made by this uploader. This download requires original N64 game data, not the Switch 2 remake.

1. Extract the entire Ship ZIP; keep assets and the application resource pack soh.o2r beside soh.exe.
2. Run ShipVRLauncher.exe in desktop mode first. Supply a supported ROM dump made from your own copy; the extractor creates oot.o2r or oot-mq.o2r locally. Supported hashes are documented in the included source materials.
3. Close the game, connect a gamepad, start your OpenXR runtime and choose Play in VR. The included README covers DirectX 11, render scale, stereo strength and optional mods.

## Contents, verification and limits

Both ZIPs include setup instructions, source materials and license notices. Games, keys, firmware, saves, generated game archives, game-derived caches, private handoffs, diagnostic captures, logs and credentials are excluded. SHA256SUMS-v1.3.0.txt on the release page verifies both downloads.

Local CPU/GPU fixtures and selected automated gameplay checks passed; portable-launcher checks are offline. A separate full public-package gameplay/headset test was not performed. Heavy areas remain CPU limited; a 60 FPS cap does not guarantee 60 FPS. Reprojection cannot reconstruct surfaces hidden from the original camera, and translucent UI remains approximate. No exhaustive dungeon/cutscene, long-session stability or physical lens-comfort claim is made.

Credits: [Lichii](https://github.com/zortos293/Lichii), [Eglantine](https://github.com/Djihads80/Eglantine), [Harbour Masters / Shipwright](https://github.com/HarbourMasters/Shipwright). Download the named application ZIPs under Assets. GitHub automatic Source code archives contain this download-index repository; application source is inside the application ZIPs. Older releases and existing download URLs remain available.
