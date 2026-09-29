<nav align="center" aria-label="Choose README language">
  <strong>English</strong> ·
  <a href="docs/lang/README_ZH.md">简体中文</a> ·
  <a href="docs/lang/README_ZH_TW.md">繁體中文</a> ·
  <a href="docs/lang/README_JA.md">日本語</a> ·
  <a href="docs/lang/README_KO.md">한국어</a> ·
  <a href="docs/lang/README_ES.md">Español</a>
</nav>

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

## Install for the first time

1. Download `Compositor-1.3.7-multilingual.dmg` from the [latest Release](https://github.com/MJorgin/Compositor-i18n/releases/latest).
2. Open the DMG and drag **Compositor** into **Applications**.
3. The first time, right-click the app and choose **Open**, then choose **Open** again.
4. If macOS blocks it, go to **System Settings → Privacy & Security → Open Anyway**.

## Replace the official release

1. Quit the official Compositor.
2. Open the community DMG and drag Compositor to Applications.
3. Choose **Replace** when macOS asks.
4. Right-click the replacement app and choose **Open** on the first launch.

Do not edit strings directly inside the installed official app. Changing a signed app's resources invalidates its signature and can make Gatekeeper behavior confusing. Replacing it with this complete community build is simpler.

To return to the official build, download it again from the [upstream project](https://github.com/robbietilton/Compositor).

## Switch language

Compositor menu → **Language…** → choose Follow System, English, 简体中文, 繁體中文, 日本語, 한국어, or Español. Restart the app to apply.

## Build from source

Requires macOS 26.5+ and Xcode 26+.

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # then Run (⌘R)
```

## Contribute a language

All strings live in `Compositor/Localizable.xcstrings`. Translations should use concise UI wording, align terminology with the localized Photoshop, and be reviewed by a fluent speaker. AI can prepare a first draft, but unedited machine output should not be submitted.

```text
You are localizing a native macOS image editor into [target language]. Translate the attached String Catalog entries while preserving every placeholder, including %@, %lld, and %%. Use concise UI wording and align technical terms with [target language] Photoshop, such as Layer, Mask, Feather, Levels, Curves, Content-Aware Fill, Contract, and Expand. Do not add explanations or punctuation that is not in the source. If a term is commonly left in English, keep it and list it separately. Return mergeable JSON only.
```

After the AI draft, check naturalness and shortcuts, validate placeholders, build the app, and open a pull request.

## Relation to upstream

A Simplified Chinese localization was offered upstream as PR #113. The maintainer explained that ongoing multi-language maintenance is not feasible yet for this early-stage, solo-maintained project. This fork keeps the same features, adds the language layer, and tracks upstream. Many thanks to the original author.
