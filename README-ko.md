# Alphade

Mac에서 내 동영상의 반투명 워터마크, 로고, 텍스트 오버레이를 지웁니다. Alphade는 흐리게 덮는 대신 그 아래에 있던 원래 화면을 되살립니다.

[English](README.md) | [Deutsch](README-de.md) | [Español](README-es.md) | [Français](README-fr.md) | [日本語](README-ja.md) | 한국어 | [繁體中文](README-zh_TW.md)

![원본과 처리 후 화면을 나란히 비교하는 Alphade](images/compare.png)

## 하는 일

워터마크 주위에 상자를 그리기만 하면 됩니다. Alphade는 동영상 전체를 분석해 워터마크가 어떻게 합성되었는지 알아낸 다음, 모든 프레임에서 이를 거꾸로 계산해 원래대로 되돌립니다. 불투명한 워터마크가 단순한 배경 위에 있으면 주변 배경으로 매끄럽게 채웁니다.

- **흐리게 하지 않고 복원**: 반투명 워터마크를 화면에서 걷어 내므로 그 아래 있던 내용이 다시 보입니다.
- **내보내기 전에 결과를 알려 줌**: 분석이 끝나면 워터마크가 '깔끔하게 제거 가능', '제거 가능(배경으로 채움)', '제거 후 흐려짐' 중 어디에 해당하는지 알려 줍니다.
- **모든 프레임 확인**: 한 프레임씩 넘겨 보고, 원본과 나란히 비교하고, 원하는 지점부터 재생할 수 있습니다.
- **상자 안만 바뀜**: 원본 해상도 그대로 또는 1080p, 720p로 줄여 H.264나 HEVC로 내보냅니다. 오디오는 그대로 복사합니다.
- **개인 정보 보호**: 모든 처리는 Mac에서 이루어집니다. 동영상을 업로드하지 않고 계정도 필요 없으며, Alphade는 네트워크에 연결하지 않고 어떤 데이터도 수집하지 않습니다.
- **무료**.

## 설치

macOS 26 이상이 필요합니다. Apple 실리콘 Mac에서 테스트했습니다. Alphade는 Developer ID로 서명되었고 Apple의 공증을 받았습니다.

### 다운로드

1. [최신 릴리스](../../releases/latest)에서 [`Alphade.zip`](../../releases/latest/download/Alphade.zip)을 다운로드합니다.
2. zip을 열고 **Alphade**를 '응용 프로그램' 폴더로 드래그합니다.
3. Alphade를 엽니다. 인터넷에서 다운로드한 앱을 열지 macOS가 물으면 '열기'를 클릭합니다.

제거하려면 Alphade를 휴지통으로 드래그합니다. 설정과 임시 파일은 `~/Library/Containers/app.vulcanshen.alphade`에 있으며 함께 삭제해도 됩니다.

### Homebrew

```sh
brew install --cask vulcanshen/tap/alphade
```

업데이트는 `brew upgrade --cask alphade`, 제거는 `brew uninstall --cask alphade`입니다. `--zap`을 붙이면 설정과 임시 파일도 함께 삭제합니다.

## 빠른 시작

1. **동영상 선택…**을 클릭합니다(동영상을 창에 끌어다 놓아도 됩니다).
2. 워터마크 주위에 네 변 모두 약간 여유를 두고 상자를 드래그합니다.
3. **분석**을 클릭합니다.
4. **원본**, **처리 후**, **비교**로 결과를 확인합니다.
5. **내보내기…**를 클릭하고 저장할 위치를 고릅니다. 파일 이름은 `<원래 이름>_nowm.mp4`로 채워져 있습니다.

인터페이스는 시스템 언어를 따릅니다(English, Deutsch, Español, Français, 日本語, 한국어, 繁體中文). 설정에서 바꿀 수도 있습니다.

## 키보드

| 키 | 동작 |
|---|---|
| ⌘O | 동영상 열기 |
| ⌘E | 내보내기 |
| ⌘1 / ⌘2 / ⌘3 | 원본 / 처리 후 / 비교 |
| ← / → | 이전 프레임 / 다음 프레임 |
| 스페이스 바 | 재생 또는 일시 정지(음소거) |
| O 누르고 있기 | 누르고 있는 동안 원본 표시 |
| ⌘+ / ⌘− | 확대 / 축소(상자를 그린 뒤) |
| ⌘, | 설정(언어) |

## 잘 맞는 경우

- 동영상 내내 같은 자리에 있는 반투명 워터마크, 로고, 텍스트
- 단색, 그라데이션, 슬라이드처럼 단순한 배경 위의 불투명 로고
- 8비트(SDR) MP4, MOV, M4V 동영상

## 지원하지 않는 경우

- 움직이거나 위치가 바뀌는 워터마크
- 디테일이 많은 배경이나 실사 영상 위의 불투명 워터마크(그 부분이 흐려집니다)
- 10비트 및 HDR 동영상

## 내 동영상에만 사용하세요

내가 소유했거나 수정 권한을 받은 동영상만 편집하세요. 다른 사람의 워터마크를 지우면 거주 지역의 저작권법을 위반할 수 있으며, Alphade를 어떻게 사용하는지는 사용자 본인의 책임입니다.

## 피드백

문제나 아이디어는 [Issues](../../issues)에 남겨 주세요. 소스 코드는 공개하지 않습니다.

## 기여자

<a href="https://github.com/vulcanshen"><img src="https://github.com/vulcanshen.png" width="48" alt="Vulcan Shen"></a>
<a href="https://github.com/claude"><img src="https://github.com/claude.png" width="48" alt="Claude"></a>

[Vulcan Shen](https://github.com/vulcanshen)과 [Claude](https://github.com/claude)가 Claude Code로 만들었습니다.

## 라이선스

Alphade는 무료로 다운로드하고 사용할 수 있습니다. © 2026 Vulcan Shen. All rights reserved. Alphade는 '있는 그대로' 제공되며 어떠한 종류의 보증도 하지 않습니다.
