<nav align="center" aria-label="README の言語を選択">
  <a href="../../README.md">English</a> ·
  <a href="README_ZH.md">简体中文</a> ·
  <a href="README_ZH_TW.md">繁體中文</a> ·
  <strong>日本語</strong> ·
  <a href="README_KO.md">한국어</a> ·
  <a href="README_ES.md">Español</a>
</nav>

<h1 align="center">
  Compositor
  <br />
  <sub>コミュニティ多言語版</sub>
</h1>

<p align="center">
  <a href="https://github.com/MJorgin/Compositor-i18n/releases/latest"><strong>DMG をダウンロード</strong></a>
  ·
  <a href="https://github.com/robbietilton/Compositor">公式 Compositor</a>
</p>

Compositor は、macOS 向けの無料でネイティブな画像編集アプリです。このコミュニティ版は **Compositor 1.3.7** をベースに、6 つのインターフェイス言語、アプリ内言語切り替え、および事前ビルド済み DMG を追加しています。

## 概要

- 6 つの UI 言語：英語、簡体字中国語、繁体字中国語、日本語、韓国語、スペイン語
- 各翻訳言語に 715 件の UI 文字列
- システム言語に従うか、アプリ内で手動切り替え可能
- コミュニティ DMG は ad-hoc 署名されていますが、**Apple 公証は未取得**のため、初回起動時に追加の確認が必要
- 既存の画像と `.comp` プロジェクトは App の外部に保存され、App を置き換えても変更されません

## 言語サポート

| 言語 | コード | 対応状況 | 保守 |
|---|---|---|---|
| English | `en` | ソース言語 | 公式 |
| 简体中文 | `zh-Hans` | 完備、715 文字列 | コミュニティ |
| 繁體中文 | `zh-Hant` | 完備、715 文字列 | コミュニティ |
| 日本語 | `ja` | 完備、715 文字列 | コミュニティ |
| 한국어 | `ko` | 完備、715 文字列 | コミュニティ |
| Español | `es` | 完備、715 文字列 | コミュニティ |

## 初めてインストールする

1. [最新リリース](https://github.com/MJorgin/Compositor-i18n/releases/latest) から `Compositor-1.3.7-multilingual.dmg` をダウンロードします。
2. DMG を開き、**Compositor** を「アプリケーション」にドラッグします。
3. 初回は App を右クリックして「開く」を選び、もう一度「開く」をクリックします。
4. macOS にブロックされた場合は、「システム設定 → プライバシーとセキュリティ → それでも開く」に進みます。

## 公式版を置き換える

1. 公式 Compositor を終了します。
2. コミュニティ DMG を開き、Compositor を「アプリケーション」にドラッグします。
3. macOS の確認画面で「置換」を選びます。
4. 置き換え後の App を初めて起動するときは、右クリックして「開く」を選びます。

インストール済みの公式 App 内の文字列を直接編集しないでください。署名済み App のリソースを変更すると署名が無効になり、Gatekeeper の動作が分かりにくくなります。完全なコミュニティビルドに置き換える方が簡単です。

公式版に戻すには、[上流プロジェクト](https://github.com/robbietilton/Compositor)から再度ダウンロードしてください。

## 言語を切り替える

Compositor メニュー → **Language…** → 「システムに合わせる」、English、简体中文、繁體中文、日本語、한국어、Español から選びます。App を再起動すると反映されます。

## ソースからビルドする

macOS 26.5 以降と Xcode 26 以降が必要です。

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # その後、⌘R で実行
```

## 翻訳に参加する

すべての文字列は `Compositor/Localizable.xcstrings` にあります。翻訳は簡潔な UI 表現を使用し、ローカライズ版 Photoshop の用語と一致させ、流暢な話者がレビューする必要があります。AI で下書きを準備できますが、未編集の機械翻訳は提出しないでください。

```text
あなたは、ネイティブ macOS 画像編集アプリを【対象言語】にローカライズしています。添付された String Catalog のエントリを翻訳し、%@、%lld、%% などすべてのプレースホルダを保持してください。簡潔な UI 表現を使い、【対象言語】版 Photoshop の用語（レイヤー、マスク、境界線をぼかす、レベル補正、トーンカーブ、コンテンツに応じた塗りつぶし、縮小、拡張など）に合わせてください。原文にない説明や句読点を追加しないでください。用語が英語のまま一般的に使われている場合は英語を保持し、別途リストアップしてください。マージ可能な JSON のみを返してください。
```

AI による下書きの後、自然な表現とショートカットを確認し、プレースホルダを検証し、App をビルドしてからプルリクエストを開いてください。

## 上流プロジェクトとの関係

簡体字中国語ローカライズは、上流に PR #113 として提案されました。メンテナーは、初期段階の個人開発プロジェクトでは多言語の継続的な保守がまだ難しいと説明しています。この Fork は同じ機能を維持し、言語レイヤーを追加し、上流を追跡します。オリジナルの作者に感謝します。
