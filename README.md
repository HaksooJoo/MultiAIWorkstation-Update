# MultiAI Workstation — Public Update Channel

이 저장소는 **MultiAI Workstation의 공개 바이너리 업데이트 전용**입니다.

- 프로그램 소스 코드는 별도의 **비공개 개발 저장소**에서 관리합니다.
- Windows x64 공식 배포 ZIP과 외부 `SHA256.txt`만 GitHub Releases에 게시합니다.
- 사용자는 GitHub 계정이나 Personal Access Token 없이 업데이트를 확인하고 다운로드할 수 있습니다.
- 다운로드된 ZIP은 크기·SHA-256·Windows PE 형식·압축 구조를 검사한 뒤에만 준비됩니다.
- `data/`, 로그인 프로필, 쿠키, 계정 토큰, 비밀번호 파일은 배포 ZIP에 포함하지 않습니다.
- 기존 앱에서 업데이트 시 반드시 `data/`를 백업하고 유지하세요.

## Releases

- 최신 정식 버전: [v0.0.25 — WebView2 채팅 입력 포커스 복구](https://github.com/HaksooJoo/MultiAIWorkstation-Update/releases/tag/v0.0.25)
- Windows x64 포터블 ZIP 및 외부 SHA-256 검증 파일을 릴리스에 함께 제공합니다.
- v0.0.25: 이전에 폐기한 웹뷰 클릭 시 메인 창 강제 활성화 기능을 제거했습니다. 실제 Windows 채팅 입력/IME 테스트는 사용자 환경에서 추가 확인해야 합니다.

[공개 업데이트 릴리스 확인](https://github.com/HaksooJoo/MultiAIWorkstation-Update/releases)

태그와 ZIP 이름은 다음 형식으로 통일합니다.

- Git tag: `v0.0.24` (이후에도 `vMAJOR.MINOR.PATCH`)
- ZIP: `MultiAI-Workstation-v0.0.24-Windows-portable.zip`
- 체크섬: `SHA256.txt` (ZIP의 SHA-256, 별도 Release asset)

이 저장소가 비어 있거나 릴리스가 없을 때는 업데이트를 받을 수 없습니다. 첫 공개 배포 후 최신 버전 확인이 정상화됩니다.

## Release 운영

개발 저장소의 Windows 빌드·Rust 테스트·보안 회귀·ZIP 검증이 모두 성공해야 합니다.
검증된 실행 파일과 DLL만 공개 저장소에 게시하며, **비공개 소스나 개인 정보는 업로드하지 않습니다.**

비공개 개발 저장소의 Actions secret `MULTIAI_UPDATE_PUBLISH_TOKEN`에는 이 공개 저장소에만 범위를 한정한 Fine-grained PAT (`Contents: Read and write`)을 등록합니다. 이 토큰은 개발용 배포 자동화에서만 사용하며 **사용자 앱에는 절대로 포함하지 않습니다**.

> 참고: 현재 URL은 이 GitHub 저장소에 연결되어 있습니다. 이 업데이트 저장소 자체를 다른 계정으로 옮기는 경우, 고정 도메인 또는 호환성 리다이렉션을 따로 설계해야 합니다.
