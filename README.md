# Death Rally Vita 
An optimized performance and control fork of **Death Rally** for the PlayStation Vita.

## 👥 Credits & Acknowledgments
This project is a performance-focused fork and would not be possible without the incredible work of the original developers:
* **Original PS Vita Port:** Developed by **Enrique Somolinos** ([@enriquesomolinos](https://github.com/enriquesomolinos/dRally-vita))).
* **Open Source Engine:** Based on the source code reconstruction by **urxp** ([/dRally](https://github.com/urxp/dRally).

---

### 🎮 Installation Guide

#### Step 1: Install the Game App
* Download and install the **.vpk** file on your PlayStation Vita using VitaShell.

#### Step 2: Prepare the Data Files
* Download `death rally data template.zip` from the **Releases** section.
* Extract it and copy the `data` folder directly into the root of your **ux0:** partition. 
* This automatically creates the path `ux0:data/DERA00002/DATA/` with the pre-configured `cdrom.ini`.

#### Step 3: Copy Steam Game Files
* Open your **Death Rally** installation folder on your PC (via Steam).
* Copy all the game files from your PC.
* Paste them directly inside `ux0:data/DERA00002/DATA/` on your Vita.

#### Step 4: Move the Cinematic Files
* Inside the **DATA** folder on your Vita, locate the 3 files ending in **.HAF**.
* Move those 3 **.HAF** files into the **CINEM** folder.

### 📂 Folder Structure Reference
Your Vita directory must look exactly like this:

```text
ux0:data/
└── DERA00002/
    └── DATA/
    |--ENGINE.BPA
    |--IBFILES.BPA
    |--MENU.BPA
    |--MUSICS.BPA
    |--TR[0-9].BPA
    |--CDROM.INI
        ├── CINEM/
        ├── ENDANI.HAF
			ENDANI0.HAF
			SANIM.HAF
```
	
# Controls
```
D-Pad/LEFT analog: steering
R Trigger: Accelerate.
L Trigger: Brake / Reverse.
X (Cross): Nitro / Turbo (Also acts as Keypad-Enter for general menu navigation).
Square (□): Shoot main weapons. Native Exit Shortcut (Sends 'Y' key to instantly quit races in the pause overlay
Circle (○): Drop mines.
Triangle (△): Horn / "space"
```

## 📋 How to bypass the Name / Save Profile screens
Since the native Vita OS keyboard cannot bind to this specific DOS emulator layout, follow these simple steps to easily bypass the profile creation or save-game text fields:

1. When the game prompts you to type a name, press **Triangle (△)** (this injects a character/space into the empty text box).
2. Press **X (Cross)** to accept and confirm (sends `Keypad-Enter`).
3. Your profile or save slot will be instantly created or updated without needing a physical keyboard.


---

## 📦 Required Original Game Files (Legal Notice)
This VPK does not contain any copyrighted game assets (graphics, music, or levels). To play, you must provide the original MS-DOS game files legally. 



🛠️

Changelog / Implemented Improvements:True Vertical Fullscreen (Letterbox Removed): Completely removed the legacy MS-DOS -DDR_LETTERBOX flag. Races now utilize the full vertical height of the PS Vita screen through automatic hardware scaling (960x544), eliminating the top and bottom black bars.Vectorized Math Optimizations (NEON Instructions): Compiled using aggressive performance flags (-Ofast, -mfpu=neon, and -mcpu=cortex-a9). This forces the Vita's ARM CPU to compute vehicle physics, rotation, and missile trajectories vectorially and simultaneously, stabilizing frame pacing.Input Lag Elimination (MS-DOS Delays Removed): Disabled legacy artificial frame timers (SDL_Delay) within the main update loop (__GET_FRAME_COUNTER). The CPU now processes frame rendering freely, ensuring buttons and direction inputs respond instantly to touch.Fluent & Continuous D-Pad Steering Fix: Completely rewrote the horizontal axis tracking logic inside events.c. This permanently fixes the native bug that caused the car to only "tap-steer" short distances. Vehicles now drift and turn smoothly and continuously as long as the D-Pad direction is held down.Ergonomic Control Remapping:Associated the MS-DOS Y (Yes) key to the Square (□) button as a dual action during races. This provides an immediate shortcut to accept race retirement inside the pause overlay, preventing players from getting trapped in that screen.Modern Code Toolchain Compatibility (C23 Standard): Fixed a syntactic conflict in db_ipx.c by removing a redundant boolean redefinition (typedef int bool), adapting the codebase flawlessly to the latest VitaSDK toolchain revisions.
