# PDF++ Modified

This is a personally modified version of [PDF++](https://github.com/RyotaUshio/obsidian-pdf-plus), an Obsidian plugin originally created by [Ryota Ushio](https://github.com/RyotaUshio).

The original plugin is described as:

> The most Obsidian-native PDF annotation tool ever.

This repository keeps the core behavior of PDF++ while adding several workflow fixes and interaction improvements for PDF highlighting, annotation editing, and plugin compatibility.

## Relationship To The Original Project

This is not the official PDF++ release and is not published by the original author.

- Original project: [https://github.com/RyotaUshio/obsidian-pdf-plus](https://github.com/RyotaUshio/obsidian-pdf-plus)
- Original author: [Ryota Ushio](https://github.com/RyotaUshio)
- Base plugin version: `0.40.31`
- Original license: MIT License

For official documentation, stable releases, and upstream issues, please refer to the original repository.

## Changes In This Version

Compared with the original PDF++ release, this modified version includes the following changes:

1. Changed PDF edit mode behavior so selecting text does not immediately write a highlight.
3. Preserved the visible text selection until the user clicks a color button.
4. Reduced full-page refreshes after writing highlights into PDF files.
5. Made newly created highlights visible immediately in the current PDF view.
6. Added immediate left-click controls for newly created highlights.
7. Restored quick actions for newly created highlights: copy reference, edit, and delete.
8. Synchronized highlight edits and deletions in the current view without relying on a full PDF reload.

## Intended Use

This version is useful if you:

- Read and annotate PDFs directly inside Obsidian.
- Use PDF++ together with Markdown note-taking workflows.
- Frequently use PDF++'s PDF editing mode.
- Want highlight creation, reference copying, editing, and deletion to feel less disruptive.
- Use BookNote and PDF++ in the same vault.

## Installation

Manual installation:

1. Download this plugin folder.
2. Copy it into your Obsidian vault:

   ```text
   .obsidian/plugins/pdf-plus/
   ```
3. Make sure the folder contains at least:

   ```text
   main.js
   manifest.json
   styles.css
   ```
4. Open Obsidian settings.
5. Go to **Community plugins**.
6. Disable restricted mode if needed.
7. Enable **PDF++**.
8. Reload the plugin or restart Obsidian if PDF++ was already enabled.

## Usage Notes

In PDF edit mode:

1. Select text in a PDF.
2. Click a color button in the PDF++ toolbar.
3. The highlight is written into the PDF file.
4. The highlight should appear immediately without a full-page refresh.
5. Left-click the highlight to open quick actions.
6. Use the quick actions to copy a reference, edit the annotation, or delete it.

## Notes And Caveats

- This modified version patches the built `main.js` file directly. It is not rebuilt from the full TypeScript source tree.
- PDF++ depends on Obsidian and PDF.js internals, so future Obsidian updates may require additional fixes.
- Back up important PDF files before doing large-scale annotation work.
- `data.json` contains personal plugin settings and is usually not suitable for publishing.
- If you publish your own fork, please keep clear attribution to the original author and project.

## Recommended Files For GitHub

Recommended:

```text
main.js
manifest.json
styles.css
README.md
```

Not recommended:

```text
data.json
```

`data.json` may include personal settings such as author name, colors, copy templates, auto-focus behavior, and other vault-specific preferences.

## Credits

All credit for the original PDF++ plugin goes to [Ryota Ushio](https://github.com/RyotaUshio).

This modified version is a personal workflow-oriented patch built on top of the original PDF++ plugin.

## License

The original project is licensed under the MIT License. Any redistribution of this modified version should comply with the original license and preserve the original copyright and license information.