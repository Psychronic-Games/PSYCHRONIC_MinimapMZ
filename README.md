# PSYCHRONIC_MinimapMZ

**RPG Maker MZ Plugin**

Mini Map MZ

## What It Does

This plugin adds a minimap to your game that displays the current map with all visual elements including.

## Plugin File

- `PSYCHRONIC_MinimapMZ.js`
- Version: `0.6`
- Target: RPG Maker MZ
- Author: Psychronic
- URL: https://psychronic.itch.io

## Plugin Commands

- `showMinimap`
- `hideMinimap`
- `toggleMinimap`
- `refreshMinimap`
- `enableToggle`
- `disableToggle`

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
- toggleKey
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
- hideOnCharacterSelection: If true, minimap also hides during character selection screens (when choosing which actor for Equipment, Status, etc.).
- name: The name to use in event notes (e.g., "Triangle" for <MM-SHOW: Triangle>)
- image: The image file to use for this marker (from img/system/)

## Installation

1. Download `PSYCHRONIC_MinimapMZ.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.
4. Configure any plugin parameters or commands listed below.

## Full Plugin Help

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

@param minimapWidth
@text Minimap Width
@type number
@min 50
@max 2000
@default 200
@desc Width of the minimap in pixels.

@param minimapHeight
@text Minimap Height
@type number
@min 50
@max 2000
@default 150
@desc Height of the minimap in pixels.

@param minimapX
@text Minimap X Position
@type number
@min 0
@max 2000
@default 20
@desc X position of the minimap on screen.

@param minimapY
@text Minimap Y Position
@type number
@min 0
@max 2000
@default 20
@desc Y position of the minimap on screen.

@param frameImage
@text Frame Image
@type file
@dir img/pictures/
@default
@desc Optional frame/background image for the minimap (from img/pictures/).

@param markerColor
@text Marker Color
@type string
@default #00FF00
@desc Color of the event markers in hex format.

@param playerColor
@text Player Color
@type string
@default #FF0000
@desc Color of the player marker in hex format.

@param minimapOpacity
@text Minimap Opacity
@type number
@min 0
@max 255
@default 200
@desc Opacity of the minimap (0-255).

@param defaultVisible
@text Default Visible
@type boolean
@default true
@desc Whether the minimap is visible by default.

@param stretchToFit
@text Stretch to Fit
@type boolean
@default false
@desc If true, stretches the map to fill the entire minimap frame (may distort aspect ratio).

@param toggleKey
@text Toggle Key
@type select
@option Q
@value 81
@option W
@value 87
@option E
@value 69
@option R
@value 82
@option T
@value 84
@option A
@value 65
@option S
@value 83
@option D
@value 68
@option F
@value 70
@option G
@value 71
@option H
@value 72
@option J
@value 74
@option K
@value 75
@option L
@value 76
@option Z
@value 90
@option X
@value 88
@option C
@value 67
@option V
@value 86
@option B
@value 66
@option N
@value 78
@option M
@value 77
@option Tab
@value 9
@option Space
@value 32
@default 77
@desc Key to toggle the minimap. Default is M (77).

@param toggleEnabled
@text Toggle Enabled
@type boolean
@default true
@desc Whether the player can toggle the minimap with the toggle key.

@param customMarkers
@text Custom Markers
@type struct<MarkerStyle>[]
@default []
@desc Define custom marker styles with names and images.

@param playerMarkerImage
@text Player Marker Image
@type file
@dir img/system/
@default
@desc Custom image for player marker (from img/system/). Leave blank to use default dot.

@param showInMenu
@text Show in Menu
@type boolean
@default false
@desc Whether to show the minimap in the main menu.

@param menuMinimapWidth
@text Menu Minimap Width
@type number
@min 50
@max 2000
@default 150
@desc Width of the minimap in the menu (in pixels).

@param menuMinimapHeight
@text Menu Minimap Height
@type number
@min 50
@max 2000
@default 150
@desc Height of the minimap in the menu (in pixels).

@param menuMinimapX
@text Menu Minimap X Position
@type number
@min 0
@max 2000
@default 500
@desc X position of the minimap in the menu.

@param menuMinimapY
@text Menu Minimap Y Position
@type number
@min 0
@max 2000
@default 100
@desc Y position of the minimap in the menu.

@param menuFrameImage
@text Menu Frame Image
@type file
@dir img/pictures/
@default
@desc Optional frame/background image for the menu minimap (from img/pictures/).

@param menuSelectionHidesMap
@text Menu Selection Hides Map
@type boolean
@default false
@desc If true, minimap hides when entering submenus (Equipment, Status, etc.) and reappears when returning to main menu.

@param hideOnCharacterSelection
@text Hide On Character Selection
@type boolean
@default false
@desc If true, minimap also hides during character selection screens (when choosing which actor for Equipment, Status, etc.).

@command showMinimap
@text Show Minimap
@desc Shows the minimap.

@command hideMinimap
@text Hide Minimap
@desc Hides the minimap.

@command toggleMinimap
@text Toggle Minimap
@desc Toggles the minimap visibility.

@command refreshMinimap
@text Refresh Minimap
@desc Refreshes the minimap parallax layers. Use after dynamically adding/removing parallaxes.

@command enableToggle
@text Enable Toggle
@desc Enables the minimap toggle key functionality.

@command disableToggle
@text Disable Toggle
@desc Disables the minimap toggle key functionality (minimap can only be controlled via plugin commands).

## Source

This standalone repository is generated from the latest PSYCHRONIC plugin source in the RPG Reactor Complex template.

## License

MIT. See `LICENSE`.
