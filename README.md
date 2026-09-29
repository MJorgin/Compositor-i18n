# Compositor — Community Multilingual Edition

**[English](#english)** · [简体中文](#简体中文) · [繁體中文](#繁體中文) · [日本語](#日本語) · [한국어](#한국어) · [Español](#español)

## 六语简介 / Six-language overview

### 繁體中文

Compositor 是 macOS 上免費、原生的影像編輯器。這個社群版本基於官方 1.3.7，完整提供英文、簡中、繁中、日文、韓文與西文介面。已安裝官方版的使用者，只要先結束 App、開啟 DMG，並在系統詢問時選擇「取代」即可；圖片和 `.comp` 專案不會被變更。

### 日本語

Compositor は macOS 向けの無料でネイティブな画像編集アプリです。このコミュニティ版は公式 1.3.7 をベースに、英語、簡体字中国語、繁体字中国語、日本語、韓国語、スペイン語の UI を備えています。すでに公式版を使っている場合は、アプリを終了して DMG を開き、確認画面で「置換」を選んでください。画像や `.comp` プロジェクトは変更されません。

### 한국어

Compositor는 macOS용 무료 네이티브 이미지 편집기입니다. 이 커뮤니티 버전은 공식 1.3.7을 기반으로 영어, 간체 중국어, 번체 중국어, 일본어, 한국어, 스페인어 인터페이스를 제공합니다. 이미 공식 버전을 사용 중이라면 앱을 종료하고 DMG를 연 뒤 확인 창에서 ‘대체’를 선택하세요. 이미지와 `.comp` 프로젝트는 변경되지 않습니다.

### Español

Compositor es un editor de imágenes nativo y gratuito para macOS. Esta edición comunitaria, basada en la versión oficial 1.3.7, incluye interfaces en inglés, chino simplificado, chino tradicional, japonés, coreano y español. Si ya usas la versión oficial, cierra la app, abre el DMG y elige **Reemplazar** cuando macOS lo pregunte. Tus imágenes y proyectos `.comp` no se modifican.

Detailed instructions below are provided in English and Simplified Chinese; the app itself is fully localized.

## English

A free, native macOS image editor — a community multilingual edition of [Compositor](https://github.com/robbietilton/Compositor). The app follows your system language and can also be switched manually. This edition is currently based on upstream Compositor **1.3.7** and includes six interface languages.

- **English** — source language, always complete
- **简体中文** — all 715 interface strings translated; terminology aligned with Simplified Chinese Photoshop
- **繁體中文** — all 715 interface strings translated; terminology aligned with Traditional Chinese Photoshop
- **日本語** — all 715 interface strings translated; terminology aligned with Japanese Photoshop
- **한국어** — all 715 interface strings translated; terminology aligned with Korean Photoshop
- **Español** — all 715 interface strings translated; terminology aligned with Spanish Photoshop

Anything untranslated falls back to English, so the app is always fully usable.

> **Already using official Compositor?** Quit the app, open the community DMG, and choose **Replace** when macOS asks. Your images and `.comp` projects are stored outside the app and stay untouched.

### Quick install (community DMG, no Xcode)

1. Download `Compositor-1.3.7-multilingual.dmg` from the latest GitHub Release.
2. Open the DMG and drag **Compositor** into **Applications**.
3. The first time, right-click the app and choose **Open**, then choose **Open** again.
4. If macOS blocks it, go to **System Settings → Privacy & Security → Open Anyway**.

This community DMG is ad-hoc signed but not Apple-notarized. It therefore asks for one extra confirmation; it does not require Xcode.

### Replacing the official release

If you already installed the official Compositor, quit it, install this community DMG, and replace the app when macOS asks. Your image files and `.comp` projects are stored outside the app and are not changed. To return to the official build, simply download it again from upstream.

Please do not manually edit strings inside the already-installed official app: changing a signed app's resources invalidates its signature and can make Gatekeeper behavior confusing. Replacing it with this complete community build is simpler.

### Build and run

This fork ships source and a community DMG. The signed, notarized DMG on the upstream repo is produced with the original author's Apple Developer certificate, which this fork does not have; the community DMG therefore uses an ad-hoc signature.

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # then Run (⌘R)
```

Requires **macOS 26.5+** and **Xcode 26+**.

### Switching language

Compositor menu (top-left) → **Language…** → Follow System / English / 简体中文 / 繁體中文 / 日本語 / 한국어 / Español. Applies after restarting.

### Contributing a language

All strings live in one String Catalog: `Compositor/Localizable.xcstrings`.

1. Add your language in Xcode.
2. Translate — align technical terms with the localized Photoshop for your language.
3. Please do not submit machine translation; a fluent speaker should review UI strings.
4. Open a PR and add yourself to the table below.

AI can prepare a useful first draft, but it should not be the final review. A good prompt is:

```text
You are localizing a native macOS image editor into [target language]. Translate the attached String Catalog entries while preserving every placeholder, including %@, %lld, and %%. Use concise UI wording and align technical terms with [target language] Photoshop, such as Layer, Mask, Feather, Levels, Curves, Content-Aware Fill, Contract, and Expand. Do not add explanations or punctuation that is not in the source. If a term is commonly left in English, keep it and list it separately. Return mergeable JSON only.
```

After that, a fluent speaker should check naturalness and shortcuts, run the placeholder validation, and build the app.

| Language | Code | Coverage | Maintainer(s) |
|---|---|---|---|
| English | `en` | 100% (source) | upstream |
| 简体中文 | `zh-Hans` | complete (715 strings) | community |
| 繁體中文 | `zh-Hant` | complete (715 strings) | community |
| 日本語 | `ja` | complete (715 strings) | community |
| 한국어 | `ko` | complete (715 strings) | community |
| Español | `es` | complete (715 strings) | community |

### Relation to upstream

A Simplified Chinese localization was offered upstream as PR #113. The maintainer explained that, early in a solo-maintained project, ongoing multi-language upkeep is not feasible yet, so the PR was closed. This fork keeps the **same features**, adds the language layer, and continues tracking upstream (currently 1.3.7). Many thanks to the original author.

---

## 简体中文

一个免费、原生的 macOS 图像编辑器，是 [Compositor](https://github.com/robbietilton/Compositor) 的**社区多语言版**：界面跟随系统语言，也可在应用内手动切换。当前已同步官方 Compositor **1.3.7**，提供 6 种界面语言。

- **简体中文 / 繁體中文** —— 全部 715 条界面文案已翻译，术语分别对齐简中 / 繁中版 Photoshop
- **日本語 / 한국어 / Español** —— 全部 715 条界面文案已翻译，术语分别对齐日文、韩文、西文版 Photoshop
- **English** —— 源语言，始终完整

当前简中条目无缺失；未来新增界面若暂未翻译，会自动回退英文，不影响使用。

> **已经安装官方版？** 先退出 Compositor，打开社区 DMG，在系统询问时选择「替换」。图片和 `.comp` 项目文件不在 App 包内，不会被改动。

### 快速安装（社区 DMG，无需 Xcode）

1. 从最新 GitHub Release 下载 `Compositor-1.3.7-multilingual.dmg`
2. 打开 DMG，把 **Compositor** 拖到「应用程序」
3. 第一次启动时，右键 App 选择「打开」，再点一次「打开」
4. 如果被系统拦截，到「系统设置 → 隐私与安全性 → 仍要打开」

这个社区 DMG 使用本机临时签名，但没有 Apple 公证，因此会多一次确认；用户不需要安装 Xcode。

### 已安装官方正式版怎么办

如果你已经安装官方 Compositor，先退出，再安装这个社区 DMG；系统询问时选择替换。图片和 `.comp` 项目文件不在 App 包内，不会被改动。以后想回到官方版，重新下载上游官方版本即可。

不建议直接修改已安装官方 App 包里的文案：这会破坏原有签名，也容易让 Gatekeeper 的提示变得混乱。直接替换为完整的社区多语言版更简单。

### 构建与运行

本仓库提供源码和社区 DMG。官方那种无额外确认的签名安装包，是作者用他自己的 Apple 开发者证书签名并公证的，本仓库没有该证书；社区 DMG 使用本机临时签名，因此首次打开需要多确认一次。

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # 然后按 ⌘R 运行
```

需要 **macOS 26.5 或更高版本** 与 **Xcode 26 或更高版本**。本地构建的 App 自己使用完全没问题。

### 切换语言

屏幕左上角 Compositor 菜单 → **Language… / 语言…** → 跟随系统 / English / 简体中文 / 繁體中文 / 日本語 / 한국어 / Español。选择后重新启动 Compositor 生效。

### 参与翻译

所有文案集中在同一个 String Catalog：`Compositor/Localizable.xcstrings`。

1. 在 Xcode 里添加你的语言
2. 翻译时请对齐**该语言版 Photoshop** 的术语
3. 请不要提交机器翻译——界面文案应由母语者审校
4. 提交 PR，并在下表中加上自己

可以让 AI 先做初译，但不能把 AI 结果直接当成终稿。可以这样对 AI 说：

```text
你正在把一个原生 macOS 图像编辑器本地化为【目标语言】。请翻译附件中的 String Catalog 条目，完整保留 %@、%lld、%% 等占位符。界面文案要简短，并对齐【目标语言】版 Photoshop 的术语，例如图层、蒙版、羽化、色阶、曲线、内容感知填充、收缩、扩展。不要添加原文没有的解释或标点；如果某个术语在当地 Photoshop 中通常保留英文，请保留英文并单独列出。只输出可合并的 JSON。
```

AI 初译后，还需要母语者检查语气和快捷键，跑占位符校验，并实际构建 App。

| 语言 | 代码 | 完成度 | 维护者 |
|---|---|---|---|
| English | `en` | 100%（源语言） | 上游 |
| 简体中文 | `zh-Hans` | 完整（715 条） | 社区 |
| 繁體中文 | `zh-Hant` | 完整（715 条） | 社区 |
| 日本語 | `ja` | 完整（715 条） | 社区 |
| 한국어 | `ko` | 完整（715 条） | 社区 |
| Español | `es` | 完整（715 条） | 社区 |

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
