<nav align="center" aria-label="選擇 README 語言">
  <a href="../../README.md">English</a> ·
  <a href="README_ZH.md">简体中文</a> ·
  <strong>繁體中文</strong> ·
  <a href="README_JA.md">日本語</a> ·
  <a href="README_KO.md">한국어</a> ·
  <a href="README_ES.md">Español</a>
</nav>

<h1 align="center">
  Compositor
  <br />
  <sub>社群多語言版</sub>
</h1>

<p align="center">
  <a href="https://github.com/MJorgin/Compositor-i18n/releases/latest"><strong>下載 DMG</strong></a>
  ·
  <a href="https://github.com/robbietilton/Compositor">官方 Compositor</a>
</p>

Compositor 是 macOS 上免費、原生的影像編輯器。這個社群版本基於 **Compositor 1.3.7**，提供六種介面語言、App 內語言切換器，以及可直接安裝的 DMG。

## 快速瞭解

- 六種介面語言：英文、簡體中文、繁體中文、日文、韓文和西班牙文
- 每種翻譯語言包含 715 條介面文案
- 預設跟隨系統語言，也可以在 App 內手動切換
- 社群 DMG 使用 ad-hoc 簽章，但**未經 Apple 公證**，第一次啟動時需要多確認一次
- 現有圖片和 `.comp` 專案儲存在 App 外部，取代 App 時不會被改動

## 語言支援

| 語言 | 程式碼 | 涵蓋範圍 | 維護方 |
|---|---|---|---|
| English | `en` | 來源語言 | 官方 |
| 简体中文 | `zh-Hans` | 完整，715 條文案 | 社群 |
| 繁體中文 | `zh-Hant` | 完整，715 條文案 | 社群 |
| 日本語 | `ja` | 完整，715 條文案 | 社群 |
| 한국어 | `ko` | 完整，715 條文案 | 社群 |
| Español | `es` | 完整，715 條文案 | 社群 |

## 第一次安裝

1. 從 [最新 Release](https://github.com/MJorgin/Compositor-i18n/releases/latest) 下載 `Compositor-1.3.7-multilingual.dmg`。
2. 開啟 DMG，把 **Compositor** 拖到「應用程式」。
3. 第一次啟動時，右鍵 App 選擇「打開」，再點一次「打開」。
4. 如果被系統攔截，到「系統設定 → 隱私權與安全性 → 仍要打開」。

## 取代官方正式版

1. 先結束官方 Compositor。
2. 開啟社群 DMG，把 Compositor 拖到「應用程式」。
3. 系統詢問時選擇「取代」。
4. 第一次啟動取代後的 App 時，右鍵選擇「打開」。

不建議直接修改已安裝官方 App 包裡的文案：這會破壞原有簽章，也容易讓 Gatekeeper 的提示變得混亂。直接取代為完整的社群多語言版更簡單。

如果想回到官方版，重新從[上游專案](https://github.com/robbietilton/Compositor)下載即可。

## 切換語言

Compositor 選單 → **Language… / 語言…** → 選擇跟隨系統、English、简体中文、繁體中文、日本語、한국어 或 Español。重新啟動 App 後生效。

## 從原始碼建置

需要 macOS 26.5 或更高版本，以及 Xcode 26 或更高版本。

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # 然後按 ⌘R 執行
```

## 參與翻譯

所有文案集中在 `Compositor/Localizable.xcstrings`。翻譯應保持介面簡短，術語對齊對應語言版 Photoshop，並由母語者審校。可以讓 AI 先做初譯，但不要提交未經校對的機器翻譯。

```text
你正在把一個原生 macOS 影像編輯器本地化為【目標語言】。請翻譯附件中的 String Catalog 條目，完整保留 %@、%lld、%% 等佔位符。介面文案要簡短，並對齊【目標語言】版 Photoshop 的術語，例如圖層、遮色片、羽化、色階、曲線、內容感知填滿、收縮、擴展。不要加入原文沒有的解釋或標點；如果某個術語在當地 Photoshop 中通常保留英文，請保留英文並單獨列出。只輸出可合併的 JSON。
```

AI 初譯後，需要檢查語氣和快捷鍵，校驗佔位符，實際建置 App，再提交 Pull Request。

## 與官方版本的關係

簡體中文化曾以 PR #113 提交給上游。作者說明專案早期由一人維護，暫時無法承擔多語言的持續追蹤。本 Fork 保持原有功能，只增加語言層，並持續追蹤上游。感謝原作者開源這款工具。
