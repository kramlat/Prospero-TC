# 🎮 Prospero TC

## Total Conversion: Steam Deck → PS5 Experience

__Prospero TC__ is a complete Steam Deck transformation project that brings the PlayStation 5 interface, audio, and user experience to Valve's handheld. It's not just a theme—it's a total conversion that replaces the UI, adds PS5-inspired audio, and creates a seamless, immersive experience.

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

<table style="background: #aaa; border-spacing 0px; align: left;">
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-top: 1px solid #000; border-left: 1px solid #000; padding: 0px; border-spacing 0px;"><b>🗀 prospero-tc</b> </td>
    <td style="border-top: 1px solid #000; border-right: 1px solid #000; padding: 0px; border-spacing 0px;"></td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗀 src</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Source code </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 core</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Core systems </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 audio</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Audio system </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 ui</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> UI components </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 system</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> System integration </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
   <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 modules</b> </td>
   <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Module definitions </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
   <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 utils</b> </td>
   <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Utilities </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗀 assets</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Assets </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 sounds</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Sound packs </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 <i>default</b></i> <font color="#007f00">→</font> <b>🗀 default.pack</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"></td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├──  <b>🗀 default.pack</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Default pack </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 ps5.pack</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> PS5 pack (optional) </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 custom.pack</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Custom packs </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 fonts</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Fonts </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 SST</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> SST font (optional) </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└──  <b>🗀 themes</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Themes </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 <i>default</b></i> <font color="#007f00">→</font> <b>🗀 default.theme</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"></td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 default.theme</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Default theme </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 ps5.theme</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> PS5 theme (optional) </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 custom.theme</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Custom themes </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗀 dist</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Build output </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 downloads</b>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Downloaded content </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗀 scripts</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Installation scripts </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; border-bottom: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;└── <b>🗀 docs</b> </td>
    <td style="border-right: 1px solid #000; border-bottom: 1px solid #000; padding: 0px; border-spacing 0px;"> Documentation </td>
  </tr>
</table>

## Installation

### Prerequisites

- [Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader)
- Basic terminal knowledge

### Quick Install

<div style="border: 1px solid #7f7f7f; color: #afafaf; background: #000;">
    
    # Clone the repository
    git clone https://github.com/yourusername/prospero-tc.git
    cd prospero-tc
    
    # Run the installer
    ./scripts/install.sh
    
</div>

### Manual Installation

1. Download __Prospero TC__ from the releases page
2. Extract to <span style="background: #afafaf;">/home/deck/homebrew/plugins/prospero-tc/</span>
3. Run <span style="background: #afafaf;">./scripts/install.sh</span>
4. Restart Decky Loader

### Post-Installation

1. Press the <span style="background: #afafaf;">...</span> button and open Decky Loader
2. Find Prospero TC in the plugin list
3. Enable the plugin
4. Enjoy your PS5-inspired experience!

## Configuration

### Theme Switching

<div style="border: 1px solid #7f7f7f; color: #afafaf; background: #000;">
    # Switch to a different theme<br>
    cd /home/deck/prospero-tc/assets/themes/<br>
    ln -sf ps5.theme default
</div>

### Sound Pack Switching

<div style="border: 1px solid #7f7f7f; color: #afafaf; background: #000;">
    # Switch to a different sound pack<br>
    cd /home/deck/prospero-tc/assets/sounds/<br>
    ln -sf ps5.pack default
</div>

### Font Installation

Place SST font files in:

<div style="background: #afafaf;">
    /home/deck/prospero-tc/assets/fonts/SST/
</div>
<br>
Required files:

- <b>🗋 SST-Regular.ttf </b>
- <b>🗋 SST-Bold.ttf </b>
- <b>🗋 SST-Light.ttf </b>

### PS5 Audio Pack

Place PS5 sound files in:

<div style="background: #afafaf;">
    /home/deck/prospero-tc/assets/sounds/ps5.pack/
</div>
<br>
Required files:

- <b>🗋 boot.ogg (PS5 startup chime) </b>
- <b>🗋 ptc_navigation.ogg </b>
- <b>🗋 ptc_select.ogg </b>
- <b>🗋 ptc_ambiance.ogg </b>
- <b>🗋 ptc_*.ogg </b>

> See [🗋 AUDIO.md](docs/AUDIO.md) for full details.

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

<div style="border: 1px solid #7f7f7f; color: #afafaf; background: #000;">
    # Install a module
    /home/deck/prospero-tc/bin/prospero module install heroic-loader
</div>

### Enable/disable a module
<div style="border: 1px solid #7f7f7f; color: #afafaf; background: #000;">
    /home/deck/prospero-tc/bin/prospero module enable heroic-loader<br>
    /home/deck/prospero-tc/bin/prospero module disable heroic-loader
</div>

### List installed modules
<div style="border: 1px solid #7f7f7f; color: #afafaf; background: #000;">
/home/deck/prospero-tc/bin/prospero module list
</div>

## Themes

### Theme Structure

<table style="background: #aaa; border-spacing 0px; align: left;">
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-top: 1px solid #000; border-left: 1px solid #000; padding: 0px; border-spacing 0px;"><b>🗀 default.theme</b></td>
    <td style="border-top: 1px solid #000; border-right: 1px solid #000; padding: 0px; border-spacing 0px;"></td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 manifest.json</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Theme metadata </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 theme.css</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Theme styles </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 theme.js</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Theme behavior </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 pack.tar.zst</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Optional sound pack that goes with the theme </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗀 icons</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Themed icons </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 controller</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Controller icons </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 ds3</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Playstation 3 controller icons </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
<td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 ds4</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Playstation 4 controller icons </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 dualsense</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Playstation 5 controller icons </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 generic</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Generic gamepad icons </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 switch</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Switch Pro Controller and JoyCon icons (Switch 2 included) </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 xinput</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> XInput controller (usually XBox, but always compatible) icons </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 modules</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Module icons (fallback to icons within module's package if they dont exist here) </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 platform</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Platform icons (system ui icons) </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 settings</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Settings icons (used in settings menu) </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗀 ui</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Theme artwork </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 backgrounds</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Style artwork used for drawing the background </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 buttons</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Style artwork used for drawing controls, butons, switches, and sliders </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 overlays</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Style artwork used for cards </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;└── <b>🗀 wallpapers</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Each resolution has pre-setup selectable wallpapers usable by theme </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 4k</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> The wallpapers at 4k (2160p) size, 16:9 </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 1440p</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> The wallpapers at 2k (1440p) size, 16:9 </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 1200p</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> The wallpapers at DeckHD (1200p) size, 8:5 </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 1080p</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> The wallpapers at FHD (1080p) size, 16:9 </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <b>🗀 800p</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> The wallpapers at Steam Deck factory resolution (800p), 8:5 </td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; border-bottom: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <b>🗀 720p</b> </td>
    <td style="border-right: 1px solid #000; border-bottom: 1px solid #000; padding: 0px; border-spacing 0px;"> The wallpapers at HD (720p) size, 16:9 </td>
  </tr>
</table>

### Creating a Theme

1. Copy an existing theme
2. Edit <span style="background: #afafaf;">manifest.json</span>
3. Replace assets
4. Switch to your theme

> __Note__: a theme may have a sound pack payload that it can install called <span style="background: #afafaf;">pack.tar.zst</span>, but that is optional.

## Sound Packs

### Pack Structure

<table style="background: #aaa; border-spacing 0px; align: left;">
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-top: 1px solid #000; border-left: 1px solid #000; padding: 0px; border-spacing 0px;"><b>🗀 default.pack</b></td>
    <td style="border-top: 1px solid #000; border-right: 1px solid #000; padding: 0px; border-spacing 0px;"></td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 manifest.json</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Pack metadata</td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 boot.ogg</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Boot sound</td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 ptc_navigation.ogg</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> UI navigation</td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 ptc_select.ogg</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> UI selection</td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 ptc_launch.ogg</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Game launch</td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;├── <b>🗋 ptc_ambiance.ogg</b> </td>
    <td style="border-right: 1px solid #000; padding: 0px; border-spacing 0px;"> Ambiance track</td>
  </tr>
  <tr style="padding: 0px; border-spacing 0px;">
    <td style="border-left: 1px solid #000; border-bottom: 1px solid #000; padding: 0px; border-spacing 0px;">&nbsp;└── <b>🗋 ptc_*.ogg</b> </td>
    <td style="border-right: 1px solid #000; border-bottom: 1px solid #000; padding: 0px; border-spacing 0px;"> Other sounds </td>
  </tr>
</table>

## Creating a Sound Pack

### Create a .pack directory

1. Add a manifest.json
2. Add your .ogg files
3. Switch to your pack

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

<table">
  <tr><th style="background:#afafaf; border-right:#fff 1px solid;">Player</th><th style="background:#afafaf; border-right:#fff 1px solid;">Color</th><th style="background:#afafaf;">Type</th></tr>
  <tr><td>1</td><td style="background: #06c;">&nbsp;</td><td>Controller</td></tr>
  <tr><td>2</td><td style="background: #c00;">&nbsp;</td><td>Controller</td></tr>
  <tr><td>3</td><td style="background: #0c6;">&nbsp;</td><td>Controller</td></tr>
  <tr><td>4</td><td style="background: #c6c;">&nbsp;</td><td>Controller</td></tr>
  <tr><td>5</td><td style="background: #fc0;">&nbsp;</td><td>Accessory</td></tr>
  <tr><td>6</td><td style="background: #f60;">&nbsp;</td><td>Accessory</td></tr>
  <tr><td>7</td><td style="background: #f0f;">&nbsp;</td><td>Accessory</td></tr>
  <tr><td>8</td><td style="background: #0ff;">&nbsp;</td><td>Accessory</td></tr>
  <tr><td>Unassigned</td><td style="background: #eee;">&nbsp;</td><td>Waiting</td></tr>
</table>

## PIN Lock Screen

### PIN Mapping (DTMF Layout)

<table>
  <tr><th colspan="4">CONTROLLER BUTTON → NUMBER</th></tr>
  <tr><td>←  = 1</td><td>↑  = 2</td><td>→  = 3</td><td>↓  = 4</td></tr>
  <tr><td>RB = 5</td><td>RT = 6</td><td>LB = 7</td><td>LT = 8</td></tr>
  <tr><td>Y  = 9</td><td>X  = 0</td><td>&nbsp;</td><td>&nbsp;</td></tr>
  <tr><td colspan="4">Options/Start = Forgot Passcode</td></tr>
  <tr><td colspan="4">B/Circle = Clear (Backspace)</td></tr>
</table>

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
| A      | ✕             | ✕             | ✕             | B        | A      |
| B      | ○             | ○             | ○             | A        | B      |
| X      | □             | □             | □             | Y        | X      |
| Y      | △            | △            | △            | X        | Y      |

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

<div style="border: 1px solid #7f7f7f; color: #afafaf; background: #000;">
    
    # Clone the repository
    git clone https://github.com/yourusername/prospero-tc.git
    cd prospero-tc
    
    # Install dependencies<br>
    npm install<br>
    
    # Build the project
    npm run build
    
    # Run in development mode
    npm run dev
</div>

## Support

+ GitHub Issues: [here](https://github.com/kramlat/Prospero-TC/issues)
+ Discord: [Join our Discord](changeme)
+ Wiki: [Documentation](https://github.com/kramlat/Prospero-TC/wiki)

Made with ❤️ by the Prospero TC Community

__Prospero TC__: Because great UI should be for everyone, not just those who bought the right hardware. 🎮✊
