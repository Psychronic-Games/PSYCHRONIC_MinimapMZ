# PSYCHRONIC_MinimapMZ

**RPG Maker MZ Plugin**

Mini Map MZ

## What It Does

PSYCHRONIC_MinimapMZ.js.

## Plugin File

- `PSYCHRONIC_MinimapMZ.js`
- Version: `0.6`
- Target: RPG Maker MZ
- Author: Psychronic
- URL: https://psychronic.itch.io

## Plugin Commands

### Show Minimap

- Command: `showMinimap`
- Description: Shows the minimap.

### Hide Minimap

- Command: `hideMinimap`
- Description: Hides the minimap.

### Toggle Minimap

- Command: `toggleMinimap`
- Description: Toggles the minimap visibility.

### Refresh Minimap

- Command: `refreshMinimap`
- Description: Refreshes the minimap parallax layers. Use after dynamically adding/removing parallaxes.

### Enable Toggle

- Command: `enableToggle`
- Description: Enables the minimap toggle key functionality.

### Disable Toggle

- Command: `disableToggle`
- Description: Disables the minimap toggle key functionality (minimap can only be controlled via plugin commands).

## Parameter Summary

- minimapWidth: Width of the minimap in pixels.
- minimapHeight: Height of the minimap in pixels.
- minimapX: X position of the minimap on screen.
- minimapY: Y position of the minimap on screen.
- frameImage: Optional frame/background image for the minimap (from img/pictures/).
- markerColor: Color of the event markers in hex format.
- playerColor: Color of the player marker in hex format.
- minimapOpacity: Opacity of the minimap (0-255).
- defaultVisible: Whether the minimap is visible by default.
- stretchToFit: If true, stretches the map to fill the entire minimap frame (may distort aspect ratio).
- toggleKey: Key to toggle the minimap. Default is M (77).
- toggleEnabled: Whether the player can toggle the minimap with the toggle key.
- customMarkers: Define custom marker styles with names and images.
- playerMarkerImage: Custom image for player marker (from img/system/). Leave blank to use default dot.
- showInMenu: Whether to show the minimap in the main menu.
- menuMinimapWidth: Width of the minimap in the menu (in pixels).
- menuMinimapHeight: Height of the minimap in the menu (in pixels).
- menuMinimapX: X position of the minimap in the menu.
- menuMinimapY: Y position of the minimap in the menu.
- menuFrameImage: Optional frame/background image for the menu minimap (from img/pictures/).
- menuSelectionHidesMap: If true, minimap hides when entering submenus (Equipment, Status, etc.) and reappears when returning to main menu.
- hideOnCharacterSelection: Disables the minimap toggle key functionality (minimap can only be controlled via plugin commands).

## Installation

1. Download `PSYCHRONIC_MinimapMZ.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.
4. Configure any plugin parameters or commands listed below.

## Full Plugin Help

PSYCHRONIC_MinimapMZ.js

This plugin adds a minimap to your game that displays the current map
with all visual elements including:
- Default RPG Maker parallax backgrounds (including fixed "!" parallaxes)
- Multi-parallax plugin layers (if using PSYCHRONIC_MultiParallaxMZ)
- All map tile layers
- Pictures displayed on the map
- All events rendered as tiny sprites (they move in real-time!)
- Custom marker icons for events
- Player position marker

Press the configured toggle key (default "M") to toggle the minimap on/off.

Optional: Display the minimap in the main menu with its own size,
position, and frame by enabling "Show in Menu" in the plugin parameters.
You can also control whether the minimap hides when entering submenus
(Equipment, Status, etc.) with the "Menu Selection Hides Map" option,
and whether it hides during character selection with "Hide On Character Selection".

Event Tags:
Add <MM-SHOW> to an event's note OR in a comment on an event page to show default marker.
Add <MM-SHOW: MarkerName> to use a custom marker style.
Page comments take priority over event notes, allowing different markers per page!

Example: <MM-SHOW: Entrance-Up> will use the "Entrance-Up" marker style.

Use Cases:
- Put <MM-SHOW: QuestAvailable> in Page 1 comments (quest not started)
- Put <MM-SHOW: QuestActive> in Page 2 comments (quest in progress)
- Put no tag in Page 3 (quest completed - marker disappears!)

Plugin Commands:
- showMinimap: Show the minimap
- hideMinimap: Hide the minimap
- toggleMinimap: Toggle minimap visibility
- refreshMinimap: Refresh all layers (use after adding/removing parallaxes or pictures)
- enableToggle: Enable minimap toggle key
- disableToggle: Disable minimap toggle key

Compatibility:
Works with PSYCHRONIC_MultiParallaxMZ - automatically refreshes when parallaxes change.
Supports default RPG Maker MZ parallax backgrounds.
Shows pictures displayed via "Show Picture" events.

## Source

This standalone repository is generated from the latest PSYCHRONIC plugin source in the RPG Reactor Complex template.

## License

MIT. See `LICENSE`.
