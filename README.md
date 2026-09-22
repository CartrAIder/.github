# CartrAIder · .github

팀 카트라이더 조직 공통 설정 레포. 조직 내 모든 레포에 기본 적용되는 문서·템플릿을 관리한다.

## 구성

```
profile/
  README.md                            # 조직 프로필 (org 첫 화면에 노출)
  lockup-color.svg · mark-color-512.png  # 로고
  media/                               # 프로필에 들어가는 시연 영상 · 화면 · 다이어그램
    demo-full.mp4                      #   부스 발표 시연 영상 (3분)
    demo-scan.gif · demo-stop.gif      #   바코드 스캔 / 바닥선 정지 시연
    architecture.svg                   #   시스템 구성도
    realtime-sequence.svg              #   스캔 → MQTT → SSE 시퀀스
    deploy-architecture.png            #   배포 구성 (Docker Host)
    app-*.png · admin-*.png            #   앱 · 관리자 화면
    hw-*.jpg · ai-detection.jpg        #   하드웨어 사진 · AI 검출 결과
CONTRIBUTING.md                        # 코드 컨벤션 · 브랜치 · 커밋 규칙
.github/PULL_REQUEST_TEMPLATE.md       # PR 템플릿
.github/ISSUE_TEMPLATE/
  bug_report.yml                       # 버그 리포트
  feature_request.yml                  # 기능/작업
  config.yml                           # 이슈 템플릿 설정
```

`profile/media/`의 원본은 최종 발표자료(`CartrAIder_최종.pptx`, `붙임 7_판넬`)와 부스 시연 영상,
그리고 `frontend` 레포의 `assets/diagrams/`입니다. 발표자료가 바뀌면 여기도 같이 갱신합니다.

이 레포의 이슈/PR 템플릿과 커뮤니티 문서는 조직 내 다른 레포에서 자체 파일이 없을 때
기본값으로 적용된다.
