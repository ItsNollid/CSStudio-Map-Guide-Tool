# CS|Studio — Map Guide Tool

A browser-based editor for CS2 KV3 annotation files. Create, edit, and manage in-game guide overlays for Counter-Strike 2 workshop maps — no server, no build step, no account required.

## Features

- **KV3 Parser & Serializer** — Load and export CS2 annotation files with full KV3 format fidelity
- **Auto-Processing Pipeline** — Automatically apply colors, throw types, tag cleanup, text merging, and case normalization in one click
- **Interactive Map View** — Plot nodes on official radar images with pan, zoom, filtering, group highlighting, and drag-to-edit
- **Dual Guide Mode** — Work on CT-side and T-side guides simultaneously with tabbed navigation
- **Node Editor** — Expand any node to edit all properties: position, angles, colors, grenade type, title, description, and more
- **Drag Reorder** — Rearrange lineup order with drag-and-drop, reflected in the exported file
- **Undo/Redo** — Full undo stack with autosave to localStorage
- **Customizable Settings** — Color schemes, typography, throw type mappings, tag prefixes, and custom node icons
- **Format Codes** — Share and apply setting presets via compact `MGT_` encoded strings
- **Teleport Commands** — One-click copy of `setpos`/`setang` console commands to test lineups in-game
- **Theme System** — Multiple dark themes with full CSS custom property support
- **20 Built-in Maps** — Radar images for all official Active Duty and Reserve maps, plus SimpleRadar support
- **Dev Console** — Power-user command interface with 35+ commands

## Quick Start

1. Visit the [live tool](https://itsnollid.github.io/CSStudio-Map-Guide-Tool/)
2. Drag and drop a CS2 KV3 annotation `.txt` file onto the drop zone
3. Click **Process** to auto-format colors, throw types, and tags
4. Edit nodes, reorder lineups, and verify positions on the map view
5. Click **Export** to download the cleaned, game-ready file

## How It Works

The tool reads CS2's KV3 annotation format — the same format used by the in-game workshop annotation system. Annotation files contain nodes representing grenade lineups, positions, spots, text labels, and connection lines, each with world coordinates, view angles, and display properties.

The processing pipeline applies a standardized color scheme, extracts throw type information, strips recording tags, merges text nodes, and normalizes casing — turning raw recorded data into a polished guide file ready for workshop submission.

## Browser Compatibility

Works in all modern browsers (Chrome, Firefox, Edge, Safari). Everything runs client-side — your files never leave your computer.

## In-Game Recording

To create annotation files for use with this tool:

1. Load a map in CS2 with `sv_cheats 1`
2. Use `annotation_create grenade`, `annotation_create position`, `annotation_create spot`, etc. to record nodes
3. Export with `annotation_export` to get the KV3 `.txt` file
4. Load the file into the Map Guide Tool for processing and editing

See the built-in **Help** page for detailed recording instructions and console commands.

## License

[MIT](LICENSE) — Copyright 2024-2026 Nollid

## AI Assistance Disclosure

This project was developed with the assistance of AI tools.

The application architecture, feature design, workflow systems, and development direction were created and directed by **Nollid**. AI (Claude) was used as a programming assistant to help generate portions of the codebase during development.

All implementation decisions, feature specifications, debugging, testing, and final integration were performed and overseen by the project author.

AI assistance functioned as a **coding accelerator**, similar to a pair-programming tool, while overall design, functionality, and project direction remain human-led.

That doesn't mean it's a good job. I'm using this as a learning experience and totally open for citisism and tweaks. I've spent several weeks working on this and I want it to be a super funcitonal and easy to use tool that creators love to use, not just some slop tool.


## Credits

Built by **Nollid** ([@NollidOfficial](https://youtube.com/@NollidOfficial))

Part of the **CS|Studio** suite of tools for CS2 content creators.
