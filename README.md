# 옥컷 · Okcut

완성된 영상을 **원하는 조각 개수로 균등하게 나누는** 로컬 영상 커터입니다.

예를 들어 87초 영상을 3개로 나누면 약 29초씩 저장합니다. M4V·MP4·MOV 파일을 열고 조각별 시작·끝 시간을 조정하거나 필요한 조각만 선택할 수 있습니다.

## 다운로드

**[옥컷 0.2.0 다운로드 및 설치 안내](https://github.com/okdaejang-art/okcut-releases/releases/tag/v0.2.0)**

| 운영체제 | 다운로드 |
| --- | --- |
| macOS 13 이상 · Apple Silicon / 인텔 공용 | [맥 통합판 DMG](https://github.com/okdaejang-art/okcut-releases/releases/download/v0.2.0/Okcut-0.2.0-mac-universal.dmg) |
| Windows 10/11 · 64비트(x64) | [윈도우 ZIP](https://github.com/okdaejang-art/okcut-releases/releases/download/v0.2.0/Okcut-0.2.0-windows-x64.zip) |

맥은 앱을 **응용 프로그램**으로 옮기고, 윈도우는 **압축을 모두 풀어 옥컷.exe**를 실행하세요. 영상 처리에 필요한 도구가 포함되어 있어 별도 설치가 필요 없습니다.

## 저장 방식

- **빠른 무손실:** 원본 화질을 유지하며 빠르게 저장합니다. 키프레임 위치에 따라 실제 길이와 경계가 달라질 수 있습니다.
- **정확한 길이 · 고화질:** 프레임 단위로 구간 길이를 맞춰 H.264/AAC로 다시 저장합니다. SDR 8비트 영상용이며 무손실은 아닙니다.

원본 파일을 변경하지 않고 새로운 결과 폴더를 만들며, 모든 출력 조각의 재생 오류를 검사합니다. 여러 오디오 트랙은 함께 보존하고 표지 이미지·자막·별도 데이터 트랙은 제외합니다.

## 첫 실행 안내

현재 배포판은 **정식 배포 인증서 서명·Apple 공증 전 버전**이므로 처음 실행할 때 보안 확인 창이 나타날 수 있습니다. 자세한 안내는 릴리스 페이지와 동봉된 `INSTALL-ko.txt`를 확인하세요.

## 검증 상태

인텔 맥에서 실제 M4V 분할과 재생 검사를 완료했습니다. Windows용 영상 처리 실행 파일은 Wine 호환 환경에서 검증했으며, Windows 화면 코드는 macOS의 Electron 검증 앱에서 확인했습니다. **Apple Silicon 맥과 Windows PC에서의 실기 검증은 아직 진행하지 못한 첫 공개 테스트 배포판입니다.**

## 구성과 라이선스

이 저장소는 옥컷의 **배포 파일과 설치 안내**를 제공합니다. GitHub가 자동으로 표시하는 `Source code` 다운로드에는 실행 앱이 들어 있지 않습니다.

FFmpeg·x264의 라이선스, 해당 실행 파일의 전체 소스와 빌드 설정은 맥 앱의 `Contents/Resources/ThirdParty`, 윈도우 앱의 `resources/ThirdParty` 폴더에 포함되어 있습니다. Node.js 및 Electron 등의 라이선스도 배포판에 동봉되어 있습니다.
