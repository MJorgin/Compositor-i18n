<p align="center">
  <strong>English</strong> ·
  <a href="#简体中文">简体中文</a> ·
  <a href="#繁體中文">繁體中文</a> ·
  <a href="#日本語">日本語</a> ·
  <a href="#한국어">한국어</a> ·
  <a href="#español">Español</a>
</p>

<h1 align="center">
  Compositor
  <br />
  <sub>Community Multilingual Edition</sub>
</h1>

<p align="center">
  <a href="https://github.com/MJorgin/Compositor-i18n/releases/latest"><strong>Download DMG</strong></a>
  ·
  <a href="https://github.com/robbietilton/Compositor">Official Compositor</a>
</p>

A free, native macOS image editor. This community edition is based on **Compositor 1.3.7** and adds six interface languages, an in-app language switcher, and a prebuilt DMG.

## Quick facts

- 6 interface languages: English, Simplified Chinese, Traditional Chinese, Japanese, Korean, and Spanish
- 715 interface strings for each translated language
- Follows the system language, or can be switched manually inside the app
- Community DMG is ad-hoc signed but **not Apple-notarized**, so the first launch needs one extra confirmation
- Existing images and `.comp` projects are stored outside the app and are not changed when replacing it

## Language support

| Language | Code | Coverage | Maintainer |
|---|---|---|---|
| English | `en` | source language | upstream |
| 简体中文 | `zh-Hans` | complete, 715 strings | community |
| 繁體中文 | `zh-Hant` | complete, 715 strings | community |
| 日本語 | `ja` | complete, 715 strings | community |
| 한국어 | `ko` | complete, 715 strings | community |
| Español | `es` | complete, 715 strings | community |

## Six-language overview

### English

Compositor is a free, native image editor for macOS. This community build is based on official version 1.3.7 and includes English, Simplified Chinese, Traditional Chinese, Japanese, Korean, and Spanish interfaces. If you already use the official app, quit it, open the DMG, and choose **Replace**; your images and `.comp` projects are not changed.

### 简体中文

Compositor 是 macOS 上免费、原生的图像编辑器。这个社区版本基于官方 1.3.7，提供英文、简体中文、繁体中文、日文、韩文和西班牙文界面。已经安装官方版的用户，请先退出 App、打开 DMG，并在系统询问时选择「替换」；图片和 `.comp` 项目不会被改动。

### 繁體中文

Compositor 是 macOS 上免費、原生的影像編輯器。這個社群版本基於官方 1.3.7，提供英文、簡中、繁中、日文、韓文與西文介面。已安裝官方版的使用者，請先結束 App、開啟 DMG，並在系統詢問時選擇「取代」；圖片和 `.comp` 專案不會被變更。

### 日本語

Compositor は macOS 向けの無料でネイティブな画像編集アプリです。このコミュニティ版は公式 1.3.7 をベースに、英語、簡体字中国語、繁体字中国語、日本語、韓国語、スペイン語の UI を備えています。すでに公式版を使用している場合は、アプリを終了して DMG を開き、確認画面で「置換」を選んでください。画像や `.comp` プロジェクトは変更されません。

### 한국어

Compositor는 macOS용 무료 네이티브 이미지 편집기입니다. 이 커뮤니티 버전은 공식 1.3.7을 기반으로 영어, 간체 중국어, 번체 중국어, 일본어, 한국어, 스페인어 인터페이스를 제공합니다. 이미 공식 버전을 사용 중이라면 앱을 종료하고 DMG를 연 뒤 확인 창에서 ‘대체’를 선택하세요. 이미지와 `.comp` 프로젝트는 변경되지 않습니다.

### Español

Compositor es un editor de imágenes nativo y gratuito para macOS. Esta edición comunitaria, basada en la versión oficial 1.3.7, incluye interfaces en inglés, chino simplificado, chino tradicional, japonés, coreano y español. Si ya usas la versión oficial, cierra la app, abre el DMG y elige **Reemplazar** cuando macOS lo pregunte. Tus imágenes y proyectos `.comp` no se modifican.

---

## English guide

### Install for the first time

1. Download `Compositor-1.3.7-multilingual.dmg` from the [latest Release](https://github.com/MJorgin/Compositor-i18n/releases/latest).
2. Open the DMG and drag **Compositor** into **Applications**.
3. The first time, right-click the app and choose **Open**, then choose **Open** again.
4. If macOS blocks it, go to **System Settings → Privacy & Security → Open Anyway**.

### Replace the official release

1. Quit the official Compositor.
2. Open the community DMG and drag Compositor to Applications.
3. Choose **Replace** when macOS asks.
4. Right-click the replacement app and choose **Open** on the first launch.

Do not edit strings directly inside the installed official app. Changing a signed app's resources invalidates its signature and can make Gatekeeper behavior confusing. Replacing it with this complete community build is simpler.

To return to the official build, download it again from the [upstream project](https://github.com/robbietilton/Compositor).

### Switch language

Compositor menu → **Language…** → choose Follow System, English, 简体中文, 繁體中文, 日本語, 한국어, or Español. Restart the app to apply.

### Build from source

Requires macOS 26.5+ and Xcode 26+.

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # then Run (⌘R)
```

### Contribute a language

All strings live in `Compositor/Localizable.xcstrings`. Translations should use concise UI wording, align terminology with the localized Photoshop, and be reviewed by a fluent speaker. AI can prepare a first draft, but unedited machine output should not be submitted.

```text
You are localizing a native macOS image editor into [target language]. Translate the attached String Catalog entries while preserving every placeholder, including %@, %lld, and %%. Use concise UI wording and align technical terms with [target language] Photoshop, such as Layer, Mask, Feather, Levels, Curves, Content-Aware Fill, Contract, and Expand. Do not add explanations or punctuation that is not in the source. If a term is commonly left in English, keep it and list it separately. Return mergeable JSON only.
```

After the AI draft, check naturalness and shortcuts, validate placeholders, build the app, and open a pull request.

### Relation to upstream

A Simplified Chinese localization was offered upstream as PR #113. The maintainer explained that ongoing multi-language maintenance is not feasible yet for this early-stage, solo-maintained project. This fork keeps the same features, adds the language layer, and tracks upstream. Many thanks to the original author.

---

## 简体中文指南

### 第一次安装

1. 从 [最新 Release](https://github.com/MJorgin/Compositor-i18n/releases/latest) 下载 `Compositor-1.3.7-multilingual.dmg`
2. 打开 DMG，把 **Compositor** 拖到「应用程序」
3. 第一次启动时，右键 App 选择「打开」，再点一次「打开」
4. 如果被系统拦截，到「系统设置 → 隐私与安全性 → 仍要打开」

### 替换官方正式版

1. 先退出官方 Compositor
2. 打开社区 DMG，把 Compositor 拖到「应用程序」
3. 系统询问时选择「替换」
4. 第一次启动替换后的 App 时，右键选择「打开」

不建议直接修改已安装官方 App 包里的文案：这会破坏原有签名，也容易让 Gatekeeper 的提示变得混乱。直接替换为完整的社区多语言版更简单。

如果想回到官方版，重新从[上游项目](https://github.com/robbietilton/Compositor)下载即可。

### 切换语言

Compositor 菜单 → **Language… / 语言…** → 选择跟随系统、English、简体中文、繁體中文、日本語、한국어或 Español。重新启动 App 后生效。

### 从源码构建

需要 macOS 26.5 或更高版本，以及 Xcode 26 或更高版本。

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # 然后按 ⌘R 运行
```

### 参与翻译

所有文案集中在 `Compositor/Localizable.xcstrings`。翻译应保持界面简短，术语对齐对应语言版 Photoshop，并由母语者审校。可以让 AI 先做初译，但不要提交未经校对的机器翻译。

```text
你正在把一个原生 macOS 图像编辑器本地化为【目标语言】。请翻译附件中的 String Catalog 条目，完整保留 %@、%lld、%% 等占位符。界面文案要简短，并对齐【目标语言】版 Photoshop 的术语，例如图层、蒙版、羽化、色阶、曲线、内容感知填充、收缩、扩展。不要添加原文没有的解释或标点；如果某个术语在当地 Photoshop 中通常保留英文，请保留英文并单独列出。只输出可合并的 JSON。
```

AI 初译后，需要检查语气和快捷键，校验占位符，实际构建 App，再提交 Pull Request。

### 与官方版本的关系

简体中文化曾以 PR #113 提交给上游。作者说明项目早期由一人维护，暂时无法承担多语言的持续跟进。本仓库功能与官方版一致，仅增加语言层，并持续跟进上游。感谢原作者开源如此优秀的工具。
