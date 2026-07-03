# 기여 가이드 · 코드 컨벤션

팀 카트라이더 전 레포 공통 규칙. 새 작업 전에 반드시 읽는다.

## 1. 브랜치 전략

- `main` — 항상 배포/시연 가능한 안정 상태. 직접 push 금지, PR로만 병합.
- `develop` — (선택) 통합 브랜치.
- 작업 브랜치: `<type>/<간단한-설명>` 예) `feat/cart-qr-scan`, `fix/sse-reconnect`

## 2. 커밋 컨벤션 (Conventional Commits)

```
<type>: <제목 (한국어 가능, 50자 이내)>

<본문 (선택): 무엇을·왜 바꿨는지>
```

| type | 용도 |
|------|------|
| `feat` | 새 기능 |
| `fix` | 버그 수정 |
| `docs` | 문서 |
| `style` | 포맷팅 (동작 변화 없음) |
| `refactor` | 리팩터링 |
| `test` | 테스트 |
| `chore` | 빌드·설정·기타 |

예) `feat: 카트 연결 화면 QR 스캔 구현`

## 3. Pull Request

- 제목은 커밋 컨벤션과 동일 형식.
- PR 템플릿을 채운다 (변경 내용·테스트·스크린샷).
- 최소 1인 리뷰 승인 후 병합. **Squash merge** 권장.
- CI(있는 경우)가 통과해야 병합.

## 4. 프론트엔드 코드 컨벤션 (React Native + Expo)

- **TypeScript strict** 모드. `any` 지양.
- 컴포넌트: 함수형 + Hooks. 파일명 `PascalCase.tsx`, 훅 `useXxx.ts`.
- 상태관리: Context + useReducer. **Zustand/Redux/TanStack Query 금지.**
- 통신: 실시간은 **SSE만** (WebSocket 금지), 능동 액션은 REST(custom fetch wrapper).
- **폰트 크기·색상 하드코딩 금지** → `theme[mode]` 토큰에서 읽는다.
- 접근성: 노약자 모드 값(18pt+/56px/대비 AA) 준수. 화면 컴포넌트는 모드별로 복제하지 않는다.
- 포매터/린터: Prettier + ESLint. 커밋 전 통과.

## 5. 백엔드 코드 컨벤션

- Java(Spring Boot): Google Java Style 기준. 패키지·클래스 네이밍 표준 준수.
- Python(FastAPI): PEP 8 / Black 포매팅.
- 결제 단계는 멱등 설계. 시크릿/자격증명은 절대 커밋하지 않는다(`.env`는 gitignore).

## 6. 리뷰 원칙

- 정확성 우선, 그다음 단순화·재사용. 사소한 취향은 nit으로 표시.
- 각 스프린트/작업은 담당자 확인 후 다음으로 진행한다.
