<nav align="center" aria-label="选择 README 语言">
  <a href="../../README.md">English</a> ·
  <strong>简体中文</strong> ·
  <a href="README_ZH_TW.md">繁體中文</a> ·
  <a href="README_JA.md">日本語</a> ·
  <a href="README_KO.md">한국어</a> ·
  <a href="README_ES.md">Español</a>
</nav>

<h1 align="center">
  Compositor
  <br />
  <sub>社区多语言版</sub>
</h1>

<p align="center">
  <a href="https://github.com/MJorgin/Compositor-i18n/releases/latest"><strong>下载 DMG</strong></a>
  ·
  <a href="https://github.com/robbietilton/Compositor">官方 Compositor</a>
</p>

Compositor 是 macOS 上免费、原生的图像编辑器。这个社区版本基于 **Compositor 1.3.7**，提供六种界面语言、应用内语言切换器，以及可直接安装的 DMG。

## 快速了解

- 六种界面语言：英文、简体中文、繁体中文、日文、韩文和西班牙文
- 每种翻译语言包含 715 条界面文案
- 默认跟随系统语言，也可以在应用内手动切换
- 社区 DMG 使用 ad-hoc 签名，但**未经 Apple 公证**，第一次启动时需要多确认一次
- 现有图片和 `.comp` 项目保存在 App 外部，替换应用时不会被改动

## 语言支持

| 语言 | 代码 | 覆盖范围 | 维护方 |
|---|---|---|---|
| English | `en` | 源语言 | 官方 |
| 简体中文 | `zh-Hans` | 完整，715 条文案 | 社区 |
| 繁體中文 | `zh-Hant` | 完整，715 条文案 | 社区 |
| 日本語 | `ja` | 完整，715 条文案 | 社区 |
| 한국어 | `ko` | 完整，715 条文案 | 社区 |
| Español | `es` | 完整，715 条文案 | 社区 |

## 第一次安装

1. 从 [最新 Release](https://github.com/MJorgin/Compositor-i18n/releases/latest) 下载 `Compositor-1.3.7-multilingual.dmg`。
2. 打开 DMG，把 **Compositor** 拖到「应用程序」。
3. 第一次启动时，右键 App 选择「打开」，再点一次「打开」。
4. 如果被系统拦截，到「系统设置 → 隐私与安全性 → 仍要打开」。

## 替换官方正式版

1. 先退出官方 Compositor。
2. 打开社区 DMG，把 Compositor 拖到「应用程序」。
3. 系统询问时选择「替换」。
4. 第一次启动替换后的 App 时，右键选择「打开」。

不建议直接修改已安装官方 App 包里的文案：这会破坏原有签名，也容易让 Gatekeeper 的提示变得混乱。直接替换为完整的社区多语言版更简单。

如果想回到官方版，重新从[上游项目](https://github.com/robbietilton/Compositor)下载即可。

## 切换语言

Compositor 菜单 → **Language… / 语言…** → 选择跟随系统、English、简体中文、繁體中文、日本語、한국어 或 Español。重新启动 App 后生效。

## 从源码构建

需要 macOS 26.5 或更高版本，以及 Xcode 26 或更高版本。

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # 然后按 ⌘R 运行
```

## 参与翻译

所有文案集中在 `Compositor/Localizable.xcstrings`。翻译应保持界面简短，术语对齐对应语言版 Photoshop，并由母语者审校。可以让 AI 先做初译，但不要提交未经校对的机器翻译。

```text
你正在把一个原生 macOS 图像编辑器本地化为【目标语言】。请翻译附件中的 String Catalog 条目，完整保留 %@、%lld、%% 等占位符。界面文案要简短，并对齐【目标语言】版 Photoshop 的术语，例如图层、蒙版、羽化、色阶、曲线、内容感知填充、收缩、扩展。不要添加原文没有的解释或标点；如果某个术语在当地 Photoshop 中通常保留英文，请保留英文并单独列出。只输出可合并的 JSON。
```

AI 初译后，需要检查语气和快捷键，校验占位符，实际构建 App，再提交 Pull Request。

## 与官方版本的关系

简体中文化曾以 PR #113 提交给上游。作者说明项目早期由一人维护，暂时无法承担多语言的持续跟进。本 Fork 保持原有功能，只增加语言层，并持续跟进上游。感谢原作者开源这款工具。
