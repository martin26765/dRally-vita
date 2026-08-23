# dRally Vita 

* Base on work of urpx : https://github.com/urxp/dRally

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





		


