# JSON Mindmap Viewer v1.0.2.αΩ

This repository contains a **self‑contained, offline viewer** for inspecting and sharing mindmaps stored in a simple JSON format. It does **not** include any actual maps—only the viewer itself. The tool was designed for maps exported from [Obsidian Canvas](https://obsidian.md) but will work with any JSON that includes `nodes` and `edges` arrays. You can use it to load your own exported files and explore them interactively.

## Purpose

The viewer was created to help visualise complex project plans and relationships contained in JSON mindmaps. It makes it easy to:

- **Load** any mindmap JSON exported from your favourite editor (for example, Obsidian Canvas or your own tool);
- **Pan and zoom** across the canvas for comfortable navigation;
- **Drag and reposition** nodes to tidy up the layout on the fly;
- **Highlight connections**, with curved arrows and labels rendered on top of groups;
- **Render Markdown** inside node bodies (including headings, lists, bold/italic, and links) for clear formatting; and
- **Export** the current view to a PNG image for sharing or presentation.

This repository stores **only the viewer**. Keeping it separate from your maps makes it easy to keep your plans private while still sharing the tool with collaborators.

## Features

- **Self‑contained** single‑file HTML—no external dependencies or network access required.
- Uses a built‑in copy of the [Marked](https://github.com/markedjs/marked) library to render Markdown text within nodes.
- Supports both regular nodes and grouped areas for organising your map.
- Adjustable colour tags for nodes (the left border is coloured, and groups can be tinted via a colour key).
- **Load JSON** button with an inline editor so you can paste new map data without reloading the page.
- **Fit** and **Reset** controls to centre the map or return to the default zoom.
- **Export PNG** functionality to capture your current layout as an image.

## Getting Started

1. **Clone or download** this repository to your local machine.
2. Open the file `mindmap_viewer.html` in a modern browser. No internet connection is required.
3. Click **Load JSON** and paste your mindmap export (containing `nodes` and `edges` arrays). Press **Apply** to load it.
4. Use your mouse or trackpad to pan and zoom around the canvas. Drag node headers to reposition individual nodes.
5. Use the **Export PNG** button if you need a snapshot of your current view.

### Keyboard/Mouse Controls

- **Pan:** click and drag on the background.
- **Zoom:** scroll your mouse wheel or trackpad, or pinch on a touchpad.
- **Drag nodes:** click and drag the header of a node to move it.
- **Fit:** re‑centres the content to fit within the viewport.
- **Reset:** resets the zoom and pan to the default starting position.

## Customising

The viewer has been designed to be easily tweakable:

- **Colours:** the CSS variables at the top of the `<style>` block set the theme; adjust these to change background, text, and accent colours.
- **Markdown renderer:** the bundled version of Marked is minified for offline use. Replace it with a newer version if you need additional Markdown features.
- **Default map:** by default the viewer loads an empty map. You can embed a default map by editing the `mapData` variable near the top of the `<script>` and adding your JSON contents.
- **Grouping layers:** edges now render on top of group boxes to improve clarity. If you wish to change layering, adjust the `z-index` or DOM order in the HTML.

## Repository Contents

- `mindmap_viewer.html` – The self‑contained viewer with all styling, script, and Markdown rendering included.
- `README.md` – This document.

No map files are stored in this repo; you should keep your JSON mindmap exports separately. That way you remain in full control of your data.

## License

This project is released under the MIT License. See the `LICENSE` file for full details.
