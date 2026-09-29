<nav align="center" aria-label="README 언어 선택">
  <a href="../../README.md">English</a> ·
  <a href="README_ZH.md">简体中文</a> ·
  <a href="README_ZH_TW.md">繁體中文</a> ·
  <a href="README_JA.md">日本語</a> ·
  <strong>한국어</strong> ·
  <a href="README_ES.md">Español</a>
</nav>

<h1 align="center">
  Compositor
  <br />
  <sub>커뮤니티 다국어 버전</sub>
</h1>

<p align="center">
  <a href="https://github.com/MJorgin/Compositor-i18n/releases/latest"><strong>DMG 다운로드</strong></a>
  ·
  <a href="https://github.com/robbietilton/Compositor">공식 Compositor</a>
</p>

Compositor는 macOS용 무료 네이티브 이미지 편집기입니다. 이 커뮤니티 버전은 **Compositor 1.3.7**을 기반으로 6개 인터페이스 언어, 앱 내 언어 전환기, 사전 빌드된 DMG를 제공합니다.

## 주요 정보

- 6개 인터페이스 언어: 영어, 간체 중국어, 번체 중국어, 일본어, 한국어, 스페인어
- 각 번역 언어에 715개 UI 문자열
- 시스템 언어를 따르거나 앱 내에서 수동으로 전환 가능
- 커뮤니티 DMG는 ad-hoc 서명되었지만 **Apple 공증을 받지 않아** 첫 실행 시 추가 확인이 필요
- 기존 이미지와 `.comp` 프로젝트는 App 외부에 저장되며 App을 교체해도 변경되지 않음

## 언어 지원

| 언어 | 코드 | 지원 범위 | 유지보수 |
|---|---|---|---|
| English | `en` | 원본 언어 | 공식 |
| 简体中文 | `zh-Hans` | 완료, 715개 문자열 | 커뮤니티 |
| 繁體中文 | `zh-Hant` | 완료, 715개 문자열 | 커뮤니티 |
| 日本語 | `ja` | 완료, 715개 문자열 | 커뮤니티 |
| 한국어 | `ko` | 완료, 715개 문자열 | 커뮤니티 |
| Español | `es` | 완료, 715개 문자열 | 커뮤니티 |

## 처음 설치하기

1. [최신 릴리스](https://github.com/MJorgin/Compositor-i18n/releases/latest)에서 `Compositor-1.3.7-multilingual.dmg`를 다운로드합니다.
2. DMG를 열고 **Compositor**를 '응용 프로그램'으로 드래그합니다.
3. 처음에는 App을 오른쪽 버튼으로 클릭하고 '열기'를 선택한 뒤, 다시 '열기'를 클릭합니다.
4. macOS가 차단하면 '시스템 설정 → 개인 정보 보호 및 보안 → 그래도 열기'로 이동합니다.

## 공식 버전 교체하기

1. 공식 Compositor를 종료합니다.
2. 커뮤니티 DMG를 열고 Compositor를 '응용 프로그램'으로 드래그합니다.
3. macOS 확인 창에서 '대체'를 선택합니다.
4. 교체한 앱을 처음 실행할 때는 오른쪽 버튼으로 클릭하고 '열기'를 선택합니다.

설치된 공식 App 내부 문자열을 직접 편집하지 마세요. 서명된 App의 리소스를 변경하면 서명이 무효화되고 Gatekeeper 동작이 혼란스러워질 수 있습니다. 완전한 커뮤니티 빌드로 교체하는 것이 더 간단합니다.

공식 버전으로 돌아가려면 [업스트림 프로젝트](https://github.com/robbietilton/Compositor)에서 다시 다운로드하세요.

## 언어 전환하기

Compositor 메뉴 → **Language…** → '시스템 언어 따르기', English, 简体中文, 繁體中文, 日本語, 한국어, Español 중에서 선택합니다. App을 재시작하면 적용됩니다.

## 소스에서 빌드하기

macOS 26.5 이상과 Xcode 26 이상이 필요합니다.

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # 그다음 ⌘R로 실행
```

## 번역 참여하기

모든 문자열은 `Compositor/Localizable.xcstrings`에 있습니다. 번역은 간결한 UI 표현을 사용하고, 해당 언어 Photoshop 용어에 맞추며, 유창한 사용자가 검토해야 합니다. AI로 초안을 준비할 수 있지만, 교정하지 않은 기계 번역을 제출하면 안 됩니다.

```text
당신은 네이티브 macOS 이미지 편집기를 【대상 언어】로 현지화하고 있습니다. 첨부된 String Catalog 항목을 번역하고 %@, %lld, %% 등 모든 자리 표시자를 그대로 유지하세요. 간결한 UI 표현을 사용하고 【대상 언어】版 Photoshop 용어(레이어, 마스크, 가장자리 흐리게, 레벨, 곡선, 내용 인식 채우기, 축소, 확장 등)에 맞추세요. 원문에 없는 설명이나 문장 부호를 추가하지 마세요. 용어가 영어로 흔히 쓰인다면 영어를 유지하고 별도로 나열하세요. 병합 가능한 JSON만 반환하세요.
```

AI 초안 후 자연스러운 표현과 단축키를 확인하고, 자리 표시자를 검증하며, App을 빌드한 뒤 Pull Request를 여세요.

## 업스트림과의 관계

간체 중국어 현지화는 업스트림에 PR #113으로 제안되었습니다. 프로젝트 초기 단계이고 1인이 유지보수하는 프로젝트라 아직 다국어를 지속적으로 관리하기 어렵다는 설명을 들었습니다. 이 Fork는 기존 기능을 유지하고 언어 계층을 추가했으며, 업스트림을 계속 추적합니다. 원작자에게 감사드립니다.
