<div align="center">

<img src="mark-color-512.png" alt="CartrAIder" width="120" />

# 팀 카트라이더 · CartrAIder

### 스마트 AI 카트 기반 셀프 스캔 결제 시스템

**계산대 대기를 없애는 실시간 쇼핑 솔루션**

카트에 담는 순간 AI가 상품을 인식하고, 스마트폰 앱에서 실시간으로 장바구니를
확인·수정한 뒤 계산대를 거치지 않고 결제합니다.

![AI Cart](https://img.shields.io/badge/AI-상품인식-2563EB)
![Realtime](https://img.shields.io/badge/실시간-SSE-16A34A)
![Checkout-free](https://img.shields.io/badge/계산대-없는_결제-F59E0B)

</div>

---

## 🧩 레포지토리

| 레포 | 설명 | 스택 |
|------|------|------|
| [**frontend**](https://github.com/CartrAIder/frontend) | 고객용 모바일 앱 | React Native · Expo · TypeScript |
| [**quickPass**](https://github.com/CartrAIder/quickPass) | 백엔드 서버 | Spring Boot · MySQL · Redis · MQTT |
| [**.github**](https://github.com/CartrAIder/.github) | 조직 공통 설정 | 코드 컨벤션 · 이슈/PR 템플릿 |

## 🔭 시스템 한눈에 보기

```
  카트(엣지)              서버 파이프라인                     고객 앱
┌───────────┐   MQTT   ┌──────────────────────┐   SSE    ┌────────────┐
│ 라즈베리파이 │ ───────▶ │ Spring Boot(quickPass) │ ───────▶ │  모바일 앱   │
│  + 카메라   │  스캔    │  + MySQL · Redis        │ 실시간   │ (React      │
│  AI 인식    │          │  주문 · 결제 · 세션       │ 장바구니 │  Native)    │
└───────────┘          └──────────────────────┘   REST   └────────────┘
                                                   결제/주문
```

## ✨ 핵심 기능

- 🔐 **회원 인증** — 이메일 인증 가입, 모바일 토큰 로그인, 자동 재발급, 세션 만료 자동 로그아웃
- 🛒 **실시간 장바구니** — QR 카트 연결, SSE로 담긴 상품·합계 즉시 반영, 재접속 동기화
- 💳 **간편 결제** — 토스페이먼츠 결제창 → 주문 승인 → QR 영수증(이미지 저장)
- 🗺 **매장·상품** — 상품 검색·상세·매대 지도, 관리자 상품/매장 관리
- ♿ **접근성** — 일반인 / 노약자 2가지 모드 (글자·터치·대비·음성 안내)

## 👥 팀

**팀 카트라이더** · 프론트엔드(최수환 · 김도영) / 백엔드 파트

<div align="center">
<sub>2026 창의공학설계</sub>
</div>
