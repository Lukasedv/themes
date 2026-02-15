# Fallout Theme for the Windows Terminal

![Fallout Terminal Sample](./animation.gif)

Updated for 2026.

## Installation
You can download Windows Terminal here: https://github.com/microsoft/terminal

First download the terminal background image, you can use any you find. Here is the one I am using: 

![Fallout Terminal Background](./background.png)

1. Save `background.png` to `%localappdata%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState`.
2. Open Windows Terminal settings (`Ctrl` + `,`) and open the JSON file.
3. Under your profile (`PowerShell`, `Ubuntu`, `Command Prompt`, etc.), add:

    {
        "guid": "{xxxxxxx-xxxx-xxxx-xxxx-xxxxxxx}", //Replace this with yours
        "hidden": false,
        "name": "PowerShell", //Replace this with your tab
        "source": "Windows.Terminal.PowershellCore", //This one too
        "fontFace": "Lucida Sans Typewriter Regular",
        "experimental.retroTerminalEffect": true,
        "colorScheme": "Fallout",
        "backgroundImage" : "ms-appdata:///roaming/background.png", //or whatever your background file is named
        "backgroundImageOpacity" : 0.5,
        "backgroundImageStretchMode" : "fill"
    }

4. Under `"schemes"`, add:

    {
        "name" : "Fallout",
        "cursorColor": "#FFFFFF",
        "background" : "#0C0C0C",
        "foreground" : "#26E476",
        "selectionBackground": "#0C0C0C",
        "black" : "#0C0C0C",
        "blue" : "#26E476",
        "cyan" : "#26E476",
        "green" : "#022000",
        "purple" : "#26E476",
        "red" : "#26E476",
        "white" : "#26E476",
        "yellow" : "#26E476",
        "brightBlack" : "#767676",
        "brightBlue" : "#26E476",
        "brightCyan" : "#26E476",
        "brightGreen" : "#26E476",
        "brightPurple" : "#26E476",
        "brightRed" : "#26E476",
        "brightWhite" : "#26E476",
        "brightYellow" : "#26E476"
    }
        
You should be good to go!
