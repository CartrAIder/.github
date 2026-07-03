# 팀 카트라이더 (CartrAIder)

> 스마트 AI 카트 기반 셀프 스캔 결제 시스템 — 계산 대기를 제거하는 실시간 쇼핑 솔루션

고객이 상품을 카트에 담는 순간 AI가 인식하고, 스마트폰 앱에서 실시간으로 장바구니를
확인·수정한 뒤 계산대를 거치지 않고 결제한다.

## 레포지토리

| 레포 | 설명 |
|------|------|
| [frontend](https://github.com/CartrAIder/frontend) | 고객용 모바일 앱 (React Native + Expo) |
| [backend](https://github.com/CartrAIder/backend) | 서버 (Spring Boot · FastAPI · Kafka · Redis · MySQL) |
| [.github](https://github.com/CartrAIder/.github) | 조직 공통 설정 (코드 컨벤션·템플릿) |

## 시스템 한눈에 보기

```
카트(엣지)          →  서버(파이프라인)              →  클라이언트
라즈베리파이 → FastAPI(AI) → Kafka → Spring Boot → Redis/MySQL → 앱(SSE)
```

## 팀

팀 카트라이더 · 프론트엔드(최수환·김도영) / 백엔드 파트
