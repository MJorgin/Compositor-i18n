# Compositor — Community Multilingual Edition

> A free, native macOS image editor (see the [official repository](https://github.com/robbietilton/Compositor)). This community fork adds a **multilingual interface** built on an Xcode String Catalog: the app follows your system language and lets you switch manually.

- **简体中文** — Chinese (Simplified) · 界面已完整翻译，术语对齐简体中文版 Photoshop
- **English** — source language, always complete

Other languages can be added by contributing translations — see [Contributing a language](#contributing-a-language). Anything untranslated automatically falls back to English, so the app stays fully usable.

## Build and run

This fork ships **source only**. The upstream app's signed, notarized DMG is produced with the original author's Apple Developer certificate, which we do not have — so there is no one-click installer here.

To build it yourself:

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # then Run (⌘R)
```

Requires **macOS 26.5 or later** and **Xcode 26 or later**. A locally built app runs fine for personal use; macOS may ask you to confirm opening it.

If you only want Chinese on your own machine, building once from source is enough.

## Switching language

Compositor menu (top-left) → **Language…**:

- **Follow System** (default)
- **English**
- **简体中文**

The choice applies after restarting Compositor.

## Language status

| Language | Code | Coverage | Maintainer(s) |
|---|---|---|---|
| English | `en` | 100% (source) | upstream |
| 简体中文 | `zh-Hans` | core complete | community |

Coverage is tracked per language. Missing strings simply show English.

## Contributing a language

All translations live in one String Catalog: `Compositor/Localizable.xcstrings`.

1. Open the catalog and add your language (or pick an existing one).
2. Translate the strings; please align technical terms with the localized Adobe Photoshop in your language.
3. Leave machine translation out — a fluent native speaker should review UI strings.
4. Open a PR and add yourself to the table above.

To see what changed upstream, run the extractor under the localizer skill to list any new keys; new keys stay English until translated.

## Relation to upstream

A Simplified Chinese localization was submitted as PR #113. The maintainer explained that, as a solo developer early in the project's life, taking on ongoing multi-language upkeep isn't feasible yet, so the PR was closed. This fork keeps the **same features**, adds the language layer, and continues to track upstream. Many thanks to the original author for open-sourcing the app.

---

# Compositor (upstream README)


Adobe Photoshop costs too much and tools like GIMP don’t feel familiar enough for me to stay in flow. That’s why I built Compositor.

The goal was to create a full-featured image editor that is completely free and open source. I use Photoshop for compositing and post-processing, so Compositor is built around that workflow - with the tools needed to create a pixel-perfect final image.

Because it’s open source, you can download the Xcode project and add, remove, or modify any feature to fit your workflow.

## Features

### Layers
- Layers and folders, with opacity and Photoshop's full set of blend modes in its order — a folder's opacity dims everything inside it
- Layer masks: paint, fill, invert, blur and feather them; link or unlink them to transform a mask on its own
- Clipping masks and folder masks
- Adjustment layers: Hue/Saturation, Levels, Curves, Exposure, Gradient Map, Grain, Black & White, Color Balance, Invert, Gaussian Blur, Motion Blur and Noise
- Layer effects: Stroke, Drop Shadow, Color Overlay, Inner Shadow, Outer Glow and Inner Glow, rendered on the GPU and editable at any time
- Merge Down, Merge Layers and Merge Group (⌘E)
- Duplicate, rename inline, reorder and nest by drag and drop; Option-drag to duplicate; a right-click menu in the Layers panel
- Copy and paste whole layers and folders (⌘C/⌘V with no selection), within a project or between projects, or drag them between projects

### Transform
- Non-destructive move, scale, rotate and flip — images keep their full resolution however small you make them
- Free distort (⌘-drag a handle), with Shift to lock to an axis
- Transform several layers, or a whole folder, together
- Snapping to canvas and layer edges and centers, with guides
- Exact values for position, size, scale and angle, stepped with the arrow keys
- Flip Layer and Flip Canvas, horizontal and vertical

### Selections
- Rectangle and Ellipse Marquee, Freehand and Polygonal Lasso, and the Magic tool — Wand selects by color, Object traces whatever you click (Tab switches)
- Select Subject, and Expand, Contract and Feather on any selection
- Add to and subtract from selections, move the outline, or move and duplicate the pixels inside
- Load a layer's pixels or a mask as a selection
- Content-Aware Fill, which can also extend an image past its edges

### Painting and retouching
- Brush with size, hardness, opacity and smoothing, in Paint or Erase mode (B and E), and Shift for straight lines
- Spot Healing Brush (content-aware)
- Clone Stamp, aligned or not, sampling one layer or all of them
- Blur tool, on pixels or masks
- Gradient tool and Shape tool (rectangles, rounded rectangles, ellipses and lines), which stay editable rather than being rasterized
- Type tool (T): inline multiline editing in draggable, resizable paragraph boxes; font, size, color, alignment and spacing in the tool header; transform text and use it as a clipping mask
- Eyedropper and a full color picker

### Adjustments and filters
- Camera Raw filter: light, color, curves, color mixer, color grading, detail, optics and geometry, in a panel beside the canvas
- Levels (with Auto), Curves, Hue/Saturation, Exposure, Gradient Map, Grain, Black & White, Color Balance and Invert
- Gaussian Blur and Motion Blur that spread past a layer's edges
- Add Noise, Vignette, Bloom / Glow, Tonal Contrast, Lens Correction and Remove Background
- Live previews, limited to the selection when there is one

### Canvas and files
- Multiple projects in tabs
- Rulers (⌘R), guides dragged from them, a layout grid, and Snap To for guides, grid, layers and document bounds
- Crop with snapping, ratios including 3:4 and 9:16, and Option for symmetric cropping; with a selection, the crop starts at it
- Canvas Size, Image Size and Trim
- Sharp high-quality downsampling when zoomed out, and a pixel grid when zoomed in
- Import JPEG, PNG, HEIC, TIFF, camera RAW (with a develop step first) and Photoshop PSD and PSB (8-bit RGB; not CMYK). Photoshop folders, masks, blend modes, fill rectangles/ellipses, and simple horizontal text stay editable; other vectors and vertical text become pixels. A conversion report is shown before anything is applied.
- Large documents: the memory budget scales with your Mac
- Export JPEG with a live preview (⇧⌥⌘S); Copy Merged
- Photoshop-style keyboard shortcuts throughout, remappable in Edit > Keyboard Shortcuts
- Automatic updates, signed and notarized

## Requirements

- macOS 26.5 or later
- Xcode 26 or later (to build from source)

## Building

Open `Compositor.xcodeproj` and run the **Compositor** scheme.

## Releasing

`scripts/release.sh` builds a Release version, signs it with Developer ID, notarizes and staples it, and packages it into `dist/Compositor-<version>.dmg`.

It needs, all kept outside this repository:

- a **Developer ID Application** certificate in the login keychain
- notarization credentials saved with `xcrun notarytool store-credentials "compositor-notary" …`
- [`create-dmg`](https://github.com/create-dmg/create-dmg) (`brew install create-dmg`)

## License

MIT — see [LICENSE](LICENSE).
