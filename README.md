# NoABS Eagle BOM Manager

A browser-based BOM manager for Autodesk Eagle schematics. No install, no server, no bullshit.

Access tool [HERE](https://noabs-eagle.github.io/EagleBOM/).

Open a `.sch` file, edit your BOM, export back to Eagle.

## What it does

- Parses Eagle `.sch` files — simple and hierarchical schemas
- Resolves library-level attribute defaults (the ones Eagle doesn't show you in the part instance)
- Groups components by full attribute fingerprint, highlights duplicate groups
- Inline editing of attributes — changes propagate to all refs in the group
- Merge duplicate groups with conflict resolution
- Add custom attribute columns (e.g. `ALT` for alternative parts)
- Import warehouse/ERP data from CSV by matching on a common field
- Export `.scr` — Eagle script that writes attributes back into the schematic, handles multi-sheet and hierarchical designs
- Export `.xlsx` with assembly variant support
- Undo

## How to use

Drop a `.sch` file onto the page, or paste a raw file URL.

To open a specific schematic directly:
```
https://noabs-eagle.github.io/EagleBOM/index.html?url=https://raw.githubusercontent.com/j3qq4hch/kotleta/refs/heads/master/KOTLETA.sch
```

## Deploy

This is a static site — no build step, no dependencies to install. Just put it on GitHub Pages and it works.

SheetJS is bundled locally (`js/xlsx.full.min.js`). No CDN calls, works fully offline.

## Why

Eagle was almost a proper EDA tool in 2016. Then Autodesk bought it.

Part of the [NoABS](https://github.com/NoABS-Eagle) initiative — open EDA tools that actually work.
