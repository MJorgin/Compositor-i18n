# Compositor — Community Multilingual Edition

**English** · [简体中文](#简体中文)

## English

A free, native macOS image editor — a community multilingual edition of [Compositor](https://github.com/robbietilton/Compositor). The app follows your system language and can also be switched manually. This edition is currently based on upstream Compositor **1.3.7**.

- **English** — source language, always complete
- **简体中文** — Simplified Chinese, all 715 interface strings translated, terminology aligned with Simplified Chinese Photoshop

Anything untranslated falls back to English, so the app is always fully usable.

### Build and run

This fork ships source only. The signed, notarized DMG on the upstream repo is produced with the original author's Apple Developer certificate, which this fork does not have.

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # then Run (⌘R)
```

Requires **macOS 26.5+** and **Xcode 26+**.

### Switching language

Compositor menu (top-left) → **Language…** → Follow System / English / 简体中文. Applies after restarting.

### Contributing a language

All strings live in one String Catalog: `Compositor/Localizable.xcstrings`.

1. Add your language in Xcode.
2. Translate — align technical terms with the localized Photoshop for your language.
3. Please do not submit machine translation; a fluent speaker should review UI strings.
4. Open a PR and add yourself to the table below.

| Language | Code | Coverage | Maintainer(s) |
|---|---|---|---|
| English | `en` | 100% (source) | upstream |
| 简体中文 | `zh-Hans` | complete (715 strings) | community |

### Relation to upstream

A Simplified Chinese localization was offered upstream as PR #113. The maintainer explained that, early in a solo-maintained project, ongoing multi-language upkeep is not feasible yet, so the PR was closed. This fork keeps the **same features**, adds the language layer, and continues tracking upstream (currently 1.3.7). Many thanks to the original author.

---

## 简体中文

一个免费、原生的 macOS 图像编辑器，是 [Compositor](https://github.com/robbietilton/Compositor) 的**社区多语言版**：界面跟随系统语言，也可在应用内手动切换。当前已同步官方 Compositor **1.3.7**。

- **简体中文** —— 全部 715 条界面文案已翻译，术语对齐简体中文版 Photoshop（图层 / 蒙版 / 羽化 / 色阶 / 曲线 / 内容感知填充）
- **English** —— 源语言，始终完整

当前简中条目无缺失；未来新增界面若暂未翻译，会自动回退英文，不影响使用。

### 构建与运行

本仓库只提供源码。官方那种「下载即用」的签名安装包，是作者用他自己的 Apple 开发者证书签名并公证的，本仓库没有该证书，因此不提供安装包。

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # 然后按 ⌘R 运行
```

需要 **macOS 26.5 或更高版本** 与 **Xcode 26 或更高版本**。本地构建的 App 自己使用完全没问题。

### 切换语言

屏幕左上角 Compositor 菜单 → **Language… / 语言…** → 跟随系统 / English / 简体中文。选择后重新启动 Compositor 生效。

### 参与翻译

所有文案集中在同一个 String Catalog：`Compositor/Localizable.xcstrings`。

1. 在 Xcode 里添加你的语言
2. 翻译时请对齐**该语言版 Photoshop** 的术语
3. 请不要提交机器翻译——界面文案应由母语者审校
4. 提交 PR，并在下表中加上自己

| 语言 | 代码 | 完成度 | 维护者 |
|---|---|---|---|
| English | `en` | 100%（源语言） | 上游 |
| 简体中文 | `zh-Hans` | 完整（715 条） | 社区 |

### 与官方版本的关系

简体中文化曾以 PR #113 提交给上游。作者说明：项目早期由一人维护，暂时无法承担多语言的持续跟进，因此关闭了该 PR。本仓库**功能与官方版一致**，仅增加语言层，并持续跟进上游（当前为 1.3.7）。感谢原作者开源如此优秀的工具。

---

# Compositor (upstream README)


Adobe Photoshop costs too much and tools like GIMP don’t feel familiar enough for me to stay in flow. That’s why I built Compositor.

The goal was to create a full-featured image editor that is completely free and open source. I use Photoshop for compositing and post-processing, so Compositor is built around that workflow - with the tools needed to create a pixel-perfect final image.

Because it’s open source, you can download the Xcode project and add, remove, or modify any feature to fit your workflow.

## Installation

### Download
Get Compositor from [robbietilton.com/compositor](https://robbietilton.com/compositor), or download the latest release directly from [GitHub Releases](https://github.com/robbietilton/Compositor/releases/latest).

### Homebrew

```sh
brew install --cask robbietilton-compositor
```

## Features

### Layers
- Layers and folders, with opacity and Photoshop's full set of blend modes in its order — a folder's opacity dims everything inside it
- Layer masks: paint, fill, invert, blur and feather them anywhere on the canvas, past the layer's own pixels; link or unlink them to transform a mask on its own
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
- Rulers (⌘R), guides dragged from them, a layout grid with adjustable spacing and subdivisions, and Snap To for guides, grid, layers and document bounds
- Crop with snapping, ratios including 3:4 and 9:16, and Option for symmetric cropping; with a selection, the crop starts at it
- Canvas Size, Image Size and Trim
- Sharp high-quality downsampling when zoomed out, and a pixel grid when zoomed in
- Import JPEG, PNG, HEIC, TIFF, SVG, camera RAW (with a develop step first) and Photoshop PSD and PSB (8-bit RGB; not CMYK). Photoshop folders, masks, blend modes, fill rectangles/ellipses, and simple horizontal text stay editable; other vectors and vertical text become pixels. A conversion report is shown before anything is applied.
- Large documents: the memory budget scales with your Mac, and a Photoshop file too big to open has its layers cropped to the canvas instead
- Export JPEG with a live preview (⇧⌥⌘S); Copy Merged
- Keep working while a project saves
- Photoshop-style keyboard shortcuts throughout, remappable in Edit > Keyboard Shortcuts
- Drag a number's label to scrub its value, as in Photoshop
- Automatic updates, signed and notarized

### Works with AI agents
- AI agents and scripts can build and edit projects directly: a `.comp` is a folder of PNG layers and a manifest, and an open project updates live as it's written. See [Writing Compositor projects](docs/writing-comp-files.md)

## Requirements

- macOS 26.0 or later on a Mac with Apple silicon
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
