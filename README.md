# 🎮 Prospero TC

## Total Conversion: Steam Deck → PS5 Experience

__Prospero TC__ is a complete Steam Deck transformation project that brings the PlayStation 5 interface, audio, and user experience to Valve's handheld. It's not just a theme—it's a total conversion that replaces the UI, adds PS5-inspired audio, and creates a seamless, immersive experience. The project exists because CSSLoader-based approaches can be fragile and break over time, so Prospero TC aims for deeper UI integration that is more stable and more immersive. When complete, it aims to deliver the PS5 dashboard feel while allowing end users to provide their own assets, with a royalty-free alternative theme available for those without a PS5 or a legal way to unpack PS5UPDATE.PUP.

## 📋 Table of Contents

1. Overview
2. Features
3. Project Philosophy
4. Architecture
5. Installation
6. Configuration
7. Modules
8. Themes
9. Sound Packs
10. Controller Support
11. PIN Lock Screen
12. Recovery Mode
13. Legal Disclaimer
14. Credits
15. License

## Overview

Prospero TC transforms the Steam Deck into a device that feels, sounds, and behaves like a PlayStation 5. The project is named after **Prospero**, the PS5's internal codename, honoring Sony's Shakespearean naming tradition.

__Key Philosophy:__ We bring the PS5 experience to Steam Deck without pretending to be Sony. This is a fan-made conversion that respects the original design while making it accessible on an open platform.

## Features

### 🎨 UI Overhaul

* Complete PS5-inspired interface
* Clean, modern design language
* Smooth animations and transitions
* Card-based notifications replacing traditional menus
* Unified settings area

### 🔊 Audio System

* Steam Deck golden master UI sounds (converted to OGG)
* PS5-inspired synthesized audio
* Custom EDM ambiance track (default)
* Optional PS5 audio pack support
* Keyboard and trophy sounds

### 🎮 Controller Support

* Full PS5-style controller assignment
* Player number LED indicators
* Lightbar color support for supported controllers
* DS3, DS4, DualSense, Xbox, Switch, Steam Controller detection
* Controller icon adaptation

### 🧩 Module System

* Built-in module loader
* Heroic Games Launcher integration
* ProtonDB Optimizer
* SteamGridDB artwork integration
* KMenu application integration
* Decky Loader compatibility layer

### 🔐 Security

* PS5-style PIN lock screen
* Account selection with security code
* 4-digit PIN entry (DTMF layout)
* Auto-submit on 4th digit
* Forgot passcode option

### 🛡️ Recovery Mode

* 4-beep error system
* Recovery menu with:
* Update Decky Loader
* Update Prospero TC
* System Software Update
* Reset (Keep Games & Settings)
* Reset (Delete Everything)
* Safe Mode
* Restart System
* 800p resolution (1280x800)
* Pure black + white aesthetic (unthemable)

### 🎨 Theme System

* .theme directory support
* Theme switching via symlink
* Custom controller icons
* Wallpaper support (4K, 1440p, 1200p, 1080p, 720p, 800p)
* UI element theming

### 📦 Sound Pack System

* .pack directory support
* Symlink-based pack switching
* Steam golden master sounds (default)
* PS5 audio pack support
* Custom pack creation

## Project Philosophy

### Why Prospero TC?

The PS5 has a beautiful UI, but it's locked behind Sony's walled garden. Prospero TC liberates that experience and brings it to the Steam Deck—an open platform that respects user freedom.

### What We Stand For

* __Privacy:__ No tracking, no telemetry, no data collection
* __Freedom:__ Open platform, open source, user control
* __Resistance:__ Against corporate overreach and surveillance
* __Community:__ Built by gamers, for gamers
* __Excellence:__ Quality that rivals the original

### What We Reject

* Age verification bullshit
* Corporate data harvesting
* Government surveillance
* Locked ecosystems
* "*You need to prove you're not a minor*" nonsense

## Architecture

```text
📁 prospero-tc/
├── 📁 src/                                  # Source code
│   ├── 📁 core/                             # Core systems
│   ├── 📁 audio/                            # Audio system
│   ├── 📁 ui/                               # UI components
│   ├── 📁 system/                           # System integration
│   ├── 📁 modules/                          # Module definitions
│   └── 📁 utils/                            # Utilities
├── 📁 assets/                               # Assets
│   ├── 📁 sounds/                           # Sound packs
│   │   ├── 📁 default/ → 📁 default.pack/   # Selected pack symlink
│   │   ├── 📁 default.pack/                 # Default pack
│   │   ├── 📁 ps5.pack/                     # PS5 pack (optional)
│   │   └── 📁 custom.pack/                  # Custom packs
│   ├── 📁 fonts/                            # Fonts
│   │   └── 📁 SST/                          # SST font (optional)
│   └── 📁 themes/                           # Themes
│       ├── 📁 default/ → 📁 default.theme/  # Selected theme symlink
│       ├── 📁 default.theme/                # Default theme
│       ├── 📁 ps5.theme/                    # PS5 theme (optional)
│       └── 📁 custom.theme/                 # Custom themes
├── 📁 dist/                                 # Build output
│   └── 📁 downloads/                        # Downloaded content
├── 📁 scripts/                              # Installation scripts
└── 📁 docs/                                 # Documentation
```

## Installation

### Prerequisites

- [Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader)
- Basic terminal knowledge

### Quick Install

```bash
# Clone the repository
git clone https://github.com/yourusername/prospero-tc.git
cd prospero-tc

# Run the installer
./scripts/install.sh
```

### Manual Installation

1. Download __Prospero TC__ from the releases page
2. Extract it to `/home/deck/homebrew/plugins/prospero-tc/`
3. Run `./scripts/install.sh`
4. Restart Decky Loader

### Post-Installation

1. Press the `...` button and open Decky Loader
2. Find Prospero TC in the plugin list
3. Enable the plugin
4. Enjoy your PS5-inspired experience!

## Configuration

### Theme Switching

```bash
# Switch to a different theme
cd /home/deck/prospero-tc/assets/themes/
ln -sf ps5.theme default
```

### Sound Pack Switching

```bash
# Switch to a different sound pack
cd /home/deck/prospero-tc/assets/sounds/
ln -sf ps5.pack default
```

### Font Installation

Place SST font files in:

```text
/home/deck/prospero-tc/assets/fonts/SST/
```

Required files:

- `SST-Regular.ttf`
- `SST-Bold.ttf`
- `SST-Light.ttf`

### PS5 Audio Pack

Place PS5 sound files in:

```text
/home/deck/prospero-tc/assets/sounds/ps5.pack/
```

Required files:

- `boot.ogg` (PS5 startup chime)
- `ptc_navigation.ogg`
- `ptc_select.ogg`
- `ptc_ambiance.ogg`
- `ptc_*.ogg`

> See [AUDIO.md](docs/AUDIO.md) for full details.

## Modules

### Core Modules

|        Module      |                  Description                  |
|--------------------|-----------------------------------------------|
| Heroic Loader      | Epic Games, GOG, and Prime Gaming integration |
| ProtonDB Optimizer | Auto game optimization using ProtonDB data    |
| SteamGridDB Integration | Beautiful game artwork
| KMenu Loader | KDE application integration |
| Decky Compat | Backward compatibility for Decky plugins |

### Module Installation

```bash
# Install a module
/home/deck/prospero-tc/bin/prospero module install heroic-loader
```

### Enable/disable a module

```bash
/home/deck/prospero-tc/bin/prospero module enable heroic-loader
/home/deck/prospero-tc/bin/prospero module disable heroic-loader
```

### List installed modules

```bash
/home/deck/prospero-tc/bin/prospero module list
```

## Themes

### Theme Structure

```text
🎨 default.theme/
├── 📄 manifest.json           # Theme metadata
├── 📄 theme.css               # Theme styles
├── 📄 theme.js                # Theme behavior
├── 📦 pack.tar.zst            # Optional sound pack payload
├── 📁 icons/                  # Themed icons
│   ├── 📁 controller/         # Controller icons
│   │   ├── 📁 ds3/            # PlayStation 3 controller icons
│   │   ├── 📁 ds4/            # PlayStation 4 controller icons
│   │   ├── 📁 dualsense/      # PlayStation 5 controller icons
│   │   ├── 📁 generic/        # Generic gamepad icons
│   │   ├── 📁 switch/         # Switch controller icons
│   │   └── 📁 xinput/         # XInput controller icons
│   ├── 📁 modules/            # Module icons
│   ├── 📁 platform/           # Platform icons
│   └── 📁 settings/           # Settings icons
├── 📁 ui/                     # Theme artwork
│   ├── 📁 backgrounds/        # Background artwork
│   ├── 📁 buttons/            # Control artwork
│   └── 📁 overlays/           # Card artwork
└── 📁 wallpapers/             # Selectable wallpapers
    ├── 📁 4k/                 # 3840x2160 wallpapers (16:9)
    ├── 📁 1440p/              # 2560x1440 wallpapers (16:9)
    ├── 📁 1200p/              # 1920x1200 wallpapers (8:5, used by DeckHD)
    ├── 📁 1080p/              # 1920x1080 wallpapers (16:9)
    ├── 📁 900p/               # 1600x900 wallpapers (16:9)
    ├── 📁 800p/               # 1280x800 wallpapers (8:5, Steam Deck)
    ├── 📁 768p/               # 1280x768 wallpapers (5:3, seen on some laptops and TV panels)
    └── 📁 720p/               # 1280x720 wallpapers (16:9)
```

Common wallpaper resolutions to support include 720p, 768p, 800p, 900p, 1080p, 1200p, 1440p, and 4K, which covers most handheld and desktop targets.

### Creating a Theme

1. Copy an existing theme
2. Edit `manifest.json` to define its metadata and behavior
3. Replace assets such as icons, UI artwork, and wallpapers
4. Switch to your theme

> __Note__: a theme may include a sound pack payload called `pack.tar.zst`, which is optional. As the project develops, the metadata format and its documentation will become more detailed and expressive.

## Sound Packs

### Pack Structure

> The keyboard pack includes four core sounds to mirror the four primary interactions in Sony's own on-screen keyboard: typing, backspace, enter, and selection.

```text
🔊 default.pack/
├── 📄 manifest.json              # Pack metadata
├── 🔊 boot.ogg                   # Boot sound
├── 🔊 ptc_dashboard_startup.ogg  # Dashboard appears on startup
├── 🔊 ptc_keyboard_typing.ogg    # Keyboard typing sound
├── 🔊 ptc_keyboard_backspace.ogg # Keyboard backspace sound
├── 🔊 ptc_keyboard_enter.ogg     # Keyboard enter sound
├── 🔊 ptc_keyboard_select.ogg    # On-screen keyboard selection sound
├── 🔊 ptc_notify.ogg             # Notification toast sound
├── 🔊 ptc_navigation.ogg         # UI navigation
├── 🔊 ptc_select.ogg             # UI selection
├── 🔊 ptc_launch.ogg             # Game launch
├── 🔊 ptc_ambiance.ogg           # Ambiance track
└── 🔊 ptc_*.ogg                  # Other sounds
```

## Creating a Sound Pack

### Create a .pack directory

1. Add a `manifest.json` to describe the pack metadata
2. Add your `.ogg` files for the sound experience
3. Switch to your pack

> __Note__: the metadata structure for packs will continue to evolve as the format is refined and documented in greater detail.

## Controller Support

### Supported Controllers

| Controller        | Type       | LED Support         |
|-------------------|------------|---------------------|
| DualShock 3 (PS3) | Controller | 4 LEDs (player 1-8) |
| DualShock 4 (PS4) | Controller | Lightbar            |
| DualSense (PS5)   | Controller | Lightbar + 4 LEDs   |
| Steam Controller  | Controller | None                |
| Steam Deck        | Controller | None                |
| Xbox 360          | Controller | 4 LEDs              |
| Xbox One/Series   | Controller | None                |
| Switch Pro        | Controller | 4 LEDs              |
| Switch Joy-Con    | Controller | LED strip           |
| Keyboard/Mouse    | Accessory  | None                |

### Player Colors

| Player | Color | Type |
| --- | --- | --- |
| 1 | Blue | Controller |
| 2 | Red | Controller |
| 3 | Green | Controller |
| 4 | Purple | Controller |
| 5 | Yellow | Accessory |
| 6 | Orange | Accessory |
| 7 | Magenta | Accessory |
| 8 | Cyan | Accessory |
| Unassigned | Gray | Waiting |

## PIN Lock Screen

### PIN Mapping (DTMF Layout)

| Button | Number |
| --- | --- |
| ← | 1 |
| ↑ | 2 |
| → | 3 |
| ↓ | 4 |
| RB | 5 |
| RT | 6 |
| LB | 7 |
| LT | 8 |
| Y | 9 |
| X | 0 |

Options/Start = Forgot Passcode

B/Circle = Clear (Backspace)

### Behavior

* 4-digit PIN entry
* Auto-submit on 4th digit
* 5 attempts before lock
* Forgot passcode option
* Clear via B/Circle button

> __Note__: The actual PS5 lock screen has no clear button and is less secure because it is on a game console. we added one because this is on a PC.

### Button Mapping

| Button | Playstation 3 | Playstation 4 | Playstation 5 | Switch   | XInput |
|--------|---------------|---------------|---------------|----------|--------|
| ↑      | ↑             | ↑             | ↑             | ↑        | ↑      |
| ↓      | ↓             | ↓             | ↓             | ↓        | ↓      |
| ←      | ←             | ←             | ←             | ←        | ←      |
| →      | →             | →             | →             | →        | →      |
| LS     | L3            | L3            | L3            | L◉       | LS     |
| RS     | R3            | R3            | R3            | R◉       | RS     |
| L1     | L1            | L1            | L1            | L        | LB     |
| R1     | R1            | R1            | R1            | R        | RB     |
| L2     | L2            | L2            | L2            | ZL       | LT     |
| R2     | R2            | R2            | R2            | ZR       | RT     |
| L3     | N/A           | N/A           | N/A           | SL left  | N/A    |
| L4     | N/A           | N/A           | N/A           | SR left  | N/A    |
| R3     | N/A           | N/A           | N/A           | SR right | N/A    |
| R4     | N/A           | N/A           | N/A           | SL right | N/A    |
| TL     | N/A           | ▢            | ▢            | N/A      | N/A    |
| TR     | N/A           | N/A           | N/A           | N/A      | N/A    |
| screen | N/A           | N/A           | N/A           | screen   | N/A    |
| A      | <span style="color: #e60012;">✕</span> | <span style="color: #e60012;">✕</span> | <span style="color: #e60012;">✕</span> | B        | A      |
| B      | <span style="color: #00a651;">○</span> | <span style="color: #00a651;">○</span> | <span style="color: #00a651;">○</span> | A        | B      |
| X      | <span style="color: #0051ba;">□</span> | <span style="color: #0051ba;">□</span> | <span style="color: #0051ba;">□</span> | Y        | X      |
| Y      | <span style="color: #7b2cbf;">△</span> | <span style="color: #7b2cbf;">△</span> | <span style="color: #7b2cbf;">△</span> | X        | Y      |

## Recovery Mode

### Trigger Conditions

* 3+ consecutive crashes
* Corrupted installation
* Failed update
* Manual entry (hold ESC during boot)

> __Note__: on playstation consoles, you had to hold the power button until the unit powered off, then hold it a gain and wait for 1 then 2 more beeps and release. That cannot be emulated here so we used ESC.

### Recovery Menu

1. Update Decky Loader → Latest version
2. Update Prospero TC → Latest version
3. System Software Update → SteamOS update
4. Reset → Reset PTC only
5. Factory Reset → Wipes Deck
6. Safe Mode → Boot without Decky + PTC
7. Restart System → Normal restart

Beep Codes
Beeps	Meaning
1	Normal startup
2	Warning / Non-critical
3	Critical error / Improper shutdown
4	Recovery mode / Catastrophic error
5	System panic

## Legal Disclaimer

> Prospero TC does NOT distribute copyrighted material.
> Fonts: SST is a commercial font owned by Sony/Monotype. Users must obtain it legally.
> Sounds: All sound effects are property of their respective owners. Users must source them legally.
> PS5 Assets: Any PS5 assets are user-provided. Prospero TC does not include them.

## User Responsibility

> Ensure you have the right to use any assets you provide
> Comply with all applicable laws
> Respect intellectual property rights
> Use at your own risk

## Credits

### Design

+ PS5 UI design: Sony Interactive Entertainment
+ SST Font: Akira Kobayashi / Monotype Design Studio
+ Prospero TC: Community project

### Development

+ Core System: Prospero TC Team
+ Audio System: Prospero TC Team
+ Module System: Prospero TC Team
+ Theme System: Prospero TC Team

### Community

+ Steam Deck Homebrew community
+ ProtonDB contributors
+ SteamGridDB contributors
+ Decky Loader team

## License

Prospero TC is licensed under the MIT License.

### MIT License

    Copyright (c) 2024 Prospero TC Team

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
    
## Contributing

We welcome contributions! See [CONTRIBUTING.md](doc/CONTRIBUTING.md) for guidelines.

## Development Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/prospero-tc.git
cd prospero-tc

# Install dependencies
npm install

# Build the project
npm run build

# Run in development mode
npm run dev
```

## Support

+ GitHub Issues: [here](https://github.com/kramlat/Prospero-TC/issues)
+ Discord: [Join our Discord](changeme)
+ Wiki: [Documentation](https://github.com/kramlat/Prospero-TC/wiki)

Made with ❤️ by the Prospero TC Community

__Prospero TC__: Because great UI should be for everyone, not just those who bought the right hardware. 🎮✊
