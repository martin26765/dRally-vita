# dRally Vita 

* Base on work of urpx : https://github.com/urxp/dRally

# Instalation for PSVITA

* Install the vpk file under releases
* Copy all the original game assets under ux0:data/DERA00002/DATA
* Copy the DR.CFG file under ux0:data/DERA00002/DATA

# Controls
D-Pad: Smooth and continuous steering (fixed the legacy tap-steering bug).
R Trigger: Accelerate.
L Trigger: Brake / Reverse.
X (Cross): Nitro / Turbo (Also acts as Keypad-Enter for general menu navigation).
Square (□): Shoot main weapons. Native Exit Shortcut (Sends 'Y' key to instantly quit races in the pause overlay
Circle (○): Drop mines.
Triangle (△): Horn / "space"
  
## 📋 How to bypass the Name / Save Profile screens
Since the native Vita OS keyboard cannot bind to this specific DOS emulator layout, follow these simple steps to easily bypass the profile creation or save-game text fields:

1. When the game prompts you to type a name, press **Triangle (△)** (this injects a character/space into the empty text box).
2. Press **X (Cross)** to accept and confirm (sends `Keypad-Enter`).
3. Your profile or save slot will be instantly created or updated without needing a physical keyboard.


# dRally

The main goal of this project is to create a port of Death Rally (1996) running natively on Linux and BSD based operating systems.

#### Linux requirements
* GCC/Clang C compiler
* GNU/Make
* SDL2

#### You need original game assets

    dRally
    |--CINEM
    |  |--DR.IDF
    |  |--ENDANI.HAF
    |  |--ENDANI0.HAF
    |  |--SANIM.HAF
	|--CDROM.INI        [1]
    |--ENGINE.BPA
    |--IBFILES.BPA
    |--MENU.BPA
    |--MUSICS.BPA
    |--TR[0-9].BPA

    Make sure these file/dir names in dRally directory are in uppercase.

    [1] CDROM.INI contains relative location of CINEM directory (./CINEM)
		Create it if it doesnt exits, Type this inside: ux0:data/DERA00002/DATA/dRally/CINEM 
		


