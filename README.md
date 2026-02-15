# Themes for the Windows Terminal

![Fallout Terminal Sample](./animation.gif)

Updated for 2026.

## Prerequisites

1. **Install Windows Terminal** from the [Microsoft Store](https://aka.ms/terminal) or from [GitHub](https://github.com/microsoft/terminal).
2. Open Windows Terminal.

## How to Install a Theme

There are two ways to apply a theme:

### Option A: Using the Settings UI

1. Open Windows Terminal and press `Ctrl` + `,` to open **Settings**.
2. In the bottom-left corner, click **Open JSON file** to open `settings.json` in your default editor.
3. Follow the theme-specific instructions below to add the profile settings and color scheme to the JSON file.
4. Save the file — Windows Terminal will automatically reload with your new theme.

### Option B: Direct JSON Editing

1. Open the `settings.json` file directly at:
   ```
   %localappdata%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json
   ```
2. Follow the theme-specific instructions below to add the profile settings and color scheme.
3. Save the file.

> **Tip:** If you make a JSON syntax error, Windows Terminal will show a warning and revert to the previous valid settings.

---

## Theme 1: Fallout

A Fallout-inspired green terminal with a CRT retro effect and custom background.

### Background Image Setup

Download the terminal background image (or use any you find). Here is the one included in this repo:

![Fallout Terminal Background](./background.png)

1. Save `background.png` to:
   ```
   %localappdata%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState
   ```

### Profile Settings

Under `"profiles"` → `"list"`, add or update your profile (e.g. `PowerShell`, `Ubuntu`, `Command Prompt`):

```json
{
    "guid": "{xxxxxxx-xxxx-xxxx-xxxx-xxxxxxx}",
    "hidden": false,
    "name": "PowerShell",
    "source": "Windows.Terminal.PowershellCore",
    "fontFace": "Lucida Sans Typewriter Regular",
    "experimental.retroTerminalEffect": true,
    "colorScheme": "Fallout",
    "backgroundImage": "ms-appdata:///roaming/background.png",
    "backgroundImageOpacity": 0.5,
    "backgroundImageStretchMode": "fill"
}
```

> Replace `guid`, `name`, and `source` with values matching your own profile.

### Color Scheme

Under `"schemes"`, add:

```json
{
    "name": "Fallout",
    "cursorColor": "#FFFFFF",
    "background": "#0C0C0C",
    "foreground": "#26E476",
    "selectionBackground": "#0C0C0C",
    "black": "#0C0C0C",
    "blue": "#26E476",
    "cyan": "#26E476",
    "green": "#022000",
    "purple": "#26E476",
    "red": "#26E476",
    "white": "#26E476",
    "yellow": "#26E476",
    "brightBlack": "#767676",
    "brightBlue": "#26E476",
    "brightCyan": "#26E476",
    "brightGreen": "#26E476",
    "brightPurple": "#26E476",
    "brightRed": "#26E476",
    "brightWhite": "#26E476",
    "brightYellow": "#26E476"
}
```

---

## Theme 2: Retro Command Prompt

A classic green-on-black CRT terminal inspired by the [Microsoft Terminal Retro Command Prompt](https://learn.microsoft.com/en-us/windows/terminal/custom-terminal-gallery/retro-command-prompt). Uses the experimental retro terminal effect for scan lines and CRT glow.

### Profile Settings

Under `"profiles"` → `"list"`, add or update your profile:

```json
{
    "name": "Command Prompt",
    "commandline": "cmd.exe",
    "cursorColor": "#FFFFFF",
    "cursorShape": "filledBox",
    "colorScheme": "Retro",
    "fontSize": 16,
    "padding": "5, 5, 5, 5",
    "tabTitle": "Command Prompt",
    "fontFace": "PxPlus IBM VGA8",
    "experimental.retroTerminalEffect": true
}
```

> **Font note:** The `PxPlus IBM VGA8` font gives the most authentic retro look. You can download it from [int10h.org](https://int10h.org/oldschool-pc-fonts/). If you don't want to install a custom font, replace `"fontFace"` with `"Consolas"` or `"Cascadia Mono"`.

### Color Scheme

Under `"schemes"`, add:

```json
{
    "name": "Retro",
    "background": "#000000",
    "foreground": "#00ff00",
    "cursorColor": "#FFFFFF",
    "black": "#00ff00",
    "blue": "#00ff00",
    "brightBlack": "#00ff00",
    "brightBlue": "#00ff00",
    "brightCyan": "#00ff00",
    "brightGreen": "#00ff00",
    "brightPurple": "#00ff00",
    "brightRed": "#00ff00",
    "brightWhite": "#00ff00",
    "brightYellow": "#00ff00",
    "cyan": "#00ff00",
    "green": "#00ff00",
    "purple": "#00ff00",
    "red": "#00ff00",
    "white": "#00ff00",
    "yellow": "#00ff00"
}
```

---

## About `experimental.retroTerminalEffect`

Setting `"experimental.retroTerminalEffect": true` in a profile enables a CRT-style visual effect that adds:
- **Scan lines** across the terminal
- **Screen glow / bloom** around text
- A subtle **screen curvature** distortion

This works with any color scheme and can be toggled off by setting the value to `false`.

You should be good to go!
