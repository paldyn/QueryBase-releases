# QueryBase

macOS·Windows·Linux용 데스크톱 데이터베이스 클라이언트입니다. 이 저장소에는 소스 코드가 없고, 설치 파일과 릴리스 노트만 [Releases](https://github.com/paldyn/QueryBase-releases/releases)로 배포합니다.

[English](#english)

## 다운로드

아래 링크로 항상 최신 버전을 받을 수 있습니다.

| 플랫폼              | 파일                                                                                                                              |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| macOS Apple silicon | [QueryBase-mac-arm64.dmg](https://github.com/paldyn/QueryBase-releases/releases/latest/download/QueryBase-mac-arm64.dmg)                 |
| macOS Intel         | [QueryBase-mac-x64.dmg](https://github.com/paldyn/QueryBase-releases/releases/latest/download/QueryBase-mac-x64.dmg)                     |
| Windows x64         | [QueryBase-win-x64.exe](https://github.com/paldyn/QueryBase-releases/releases/latest/download/QueryBase-win-x64.exe)                     |
| Windows arm64       | [QueryBase-win-arm64.exe](https://github.com/paldyn/QueryBase-releases/releases/latest/download/QueryBase-win-arm64.exe)                 |
| Linux x64           | [QueryBase-linux-x86_64.AppImage](https://github.com/paldyn/QueryBase-releases/releases/latest/download/QueryBase-linux-x86_64.AppImage) |
| Linux arm64         | [QueryBase-linux-arm64.AppImage](https://github.com/paldyn/QueryBase-releases/releases/latest/download/QueryBase-linux-arm64.AppImage)   |

이전 버전과 버전별 릴리스 노트는 [Releases](https://github.com/paldyn/QueryBase-releases/releases)에 있습니다.

- macOS: DMG를 열고 QueryBase를 응용 프로그램 폴더로 끌어다 놓습니다.
- Windows: 설치 프로그램에서 현재 사용자 또는 모든 사용자 설치와 설치 폴더를 고릅니다. 설치 파일은 Authenticode 코드 서명을 하지 않으므로, 처음 실행하면 Microsoft Defender SmartScreen이 **Windows의 PC 보호** 창을 띄웁니다. **추가 정보 → 실행**을 누르면 설치가 시작됩니다. 모든 사용자 설치를 고르면 사용자 계정 컨트롤 창에 게시자가 알 수 없음으로 표시됩니다. Smart App Control을 켠 Windows 11에서는 이 선택지 없이 막힐 수 있습니다.
- Linux: 실행 권한을 주고(`chmod +x`) 실행합니다.

## 시스템 요구 사항

- macOS 13 이상(Apple silicon, Intel)
- Windows 10 이상(x64, arm64)
- Linux x64, arm64. AppImage는 정적 런타임을 써서 `libfuse2`가 필요 없습니다. FUSE를 쓸 수 없으면 `APPIMAGE_EXTRACT_AND_RUN=1`로 실행합니다.
- 데이터베이스 연결에는 별도 클라이언트가 필요 없습니다(Oracle도 Thin 모드).

## 자동 업데이트

- 설치한 앱은 시작 30초 뒤와 24시간마다, 또는 **도움말 → 업데이트 확인…**에서 새 버전을 확인합니다.
- 내려받기 전과 다시 시작하기 전에 매번 묻습니다. 다시 시작하기 전에는 저장하지 않은 SQL과 커밋하지 않은 트랜잭션을 확인합니다.
- 안정 버전만 받고, 이전 버전으로 되돌리지 않습니다.
- 모든 업데이트는 앱에 들어 있는 공개 키로 Ed25519 서명과 파일의 SHA-512 체크섬을 검증하고, macOS에서는 운영체제 코드 서명으로 한 번 더 검증합니다.
- github.com과 GitHub의 릴리스 다운로드 서버에만 연결하며, 고정 식별자를 보내지 않습니다. GitHub에는 IP 주소와 앱 버전이 보입니다.
- 시스템 프록시 설정을 따릅니다.

## 릴리스 노트

버전별 변경 사항은 [Releases](https://github.com/paldyn/QueryBase-releases/releases)에 있습니다.

## 버그 신고

[Issues](https://github.com/paldyn/QueryBase-releases/issues/new/choose)에서 **버그 신고** 양식을 사용해 주세요.

- 비밀번호, 연결 문자열, 호스트 이름, 키, 실제 데이터는 절대 넣지 마세요.
- 로그는 **도움말 → 로그 폴더 열기**에 있습니다. 첨부하기 전에 비밀 정보를 지우세요.

## 보안 문제 신고

보안 문제는 공개 Issue로 올리지 말고 [support@paldyn.com](mailto:support@paldyn.com)으로 보내 주세요.

## 다운로드 확인(선택)

변경할 수 없는(immutable) 릴리스로 배포하므로, [GitHub CLI](https://cli.github.com/)로 받은 파일이 이 저장소의 릴리스와 같은지 확인할 수 있습니다.

```sh
gh release verify-asset QueryBase-mac-arm64.dmg -R paldyn/QueryBase-releases
```

## 제품 약관

QueryBase는 개인과 업무 용도 모두 무료로 쓸 수 있습니다. 설치하거나 사용하면 [최종 사용자 라이선스 계약](EULA.ko.md)([English](EULA.en.md))에 동의하는 것이며, 이 계약은 앱의 **도움말 → 이용약관…**에서도 볼 수 있습니다. 두 언어본이 다르면 한국어본이 우선합니다.

QueryBase는 독점 소프트웨어입니다. 함께 배포하는 오픈 소스 구성 요소의 고지는 앱의 **도움말 → 오픈 소스 라이선스…**에서 볼 수 있습니다.

## English

QueryBase is a desktop database client for macOS, Windows and Linux. This repository holds no source code; installers and release notes are published as [Releases](https://github.com/paldyn/QueryBase-releases/releases).

### Download

The links in the [download table](#다운로드) above always serve the newest version: `QueryBase-mac-arm64.dmg` (Apple silicon), `QueryBase-mac-x64.dmg` (Intel), `QueryBase-win-x64.exe`, `QueryBase-win-arm64.exe`, `QueryBase-linux-x86_64.AppImage` and `QueryBase-linux-arm64.AppImage`. Older versions and release notes are on the [Releases](https://github.com/paldyn/QueryBase-releases/releases) page.

The Windows installers are not Authenticode code-signed. On first run, Microsoft Defender SmartScreen shows **Windows protected your PC**; choose **More info → Run anyway** to start the installer. An all-users installation shows an unknown publisher in the User Account Control prompt. With Smart App Control on, Windows 11 can block it without that choice.

### Requirements

macOS 13 or later; Windows 10 or later (x64, arm64); Linux x64 or arm64 (static AppImage runtime, no `libfuse2`; use `APPIMAGE_EXTRACT_AND_RUN=1` without FUSE). No separate database client is needed.

### Updates

QueryBase checks 30 seconds after it starts, every 24 hours and from **Help → Check for Updates…**. It asks before downloading and before restarting, installs stable versions only and never downgrades. Each update is verified against the Ed25519 public key built into the app and its SHA-512 checksum, and on macOS also by the operating system's code signature. The app contacts only github.com and GitHub's release download servers and sends no persistent identifier (GitHub sees the IP address and app version). It follows the system proxy settings.

### Bug reports

Use the **Bug report** form in [Issues](https://github.com/paldyn/QueryBase-releases/issues/new/choose). Never include passwords, connection strings, host names, keys or real data. Logs are under **Help → Open Logs Folder**; remove secrets first.

### Security reports

Do not open public issues for security problems; email [support@paldyn.com](mailto:support@paldyn.com) instead.

### Product terms

QueryBase is free for personal and business use. Installing or using it means accepting the [End User License Agreement](EULA.en.md), which the app also shows under **Help → License Agreement…**; if it differs from the [Korean original](EULA.ko.md), the Korean version prevails. QueryBase is proprietary software. Notices for the open source components it ships are in the app under **Help → Third-party Licenses…**.
