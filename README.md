<!-- Header -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,100:1E3A8A&height=220&section=header&text=Yunseo%20Nam&fontSize=60&fontColor=F8FAFC&fontAlignY=38&desc=Frontend%20Developer%20%40%20HanaLoop&descSize=18&descAlignY=58&animation=fadeIn" width="100%"/>

<p align="center">
  탄소회계 SaaS의 프론트엔드를 만들고 있습니다.<br/>
  <b>왜 느린지, 왜 깜빡이는지, 왜 이 구조인지</b>를 끝까지 파고드는 걸 좋아합니다.
</p>

<p align="center">
  <a href="mailto:ysnam0123@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://velog.io/@ysnam0123"><img src="https://img.shields.io/badge/Velog-20C997?style=for-the-badge&logo=velog&logoColor=white"/></a>
  <a href="https://hana.eco"><img src="https://img.shields.io/badge/hana.eco-1E3A8A?style=for-the-badge&logoColor=white"/></a>
</p>

<br/>

## 🌤️ Atlas — 미국 주식 "시장 날씨" 비서

> 미국장이 끝나면 시장·섹터·내 종목을 자동으로 분석해서,<br/>
> 출근길에 **한 화면으로 "오늘 할 일"** 을 알려주는 직장인용 개인 앱

<p>
  <a href="https://github.com/ysnam0123/atlas_stock_weather"><img src="https://img.shields.io/badge/Repository-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
  <img src="https://img.shields.io/badge/Built_with-Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white"/>
</p>

<!-- 스크린샷 넣으면 훨씬 좋아짐 -->
<!-- <img src="./assets/atlas.png" width="100%"/> -->

| | 기능 | 내용 |
|:---:|---|---|
| ☀️ | **시장 날씨 판정** | 시장 폭·상승추세 비율·섹터 순위를 종합해 **맑음 / 흐림 / 비**와 권장 주식 비중을 매일 계산. 상승추세 **845일**, 섹터 순위 **562일** 이력을 흐름 차트·히트맵으로 시각화 |
| 📌 | **내 종목 관리** | 미국 종목 **약 11,800개** 검색(약 5,900개는 한글명 검색). 보유 종목마다 손절가 3종(비율형·변동성형·차트형) 제안, 손절가까지 남은 거리와 열린 위험을 매일 안내 |
| 🤖 | **AI와 대결** | 차트 스캐너가 매일 **약 1,600개** 종목을 스캔(약 5분). 규칙 기반 AI가 모의 계좌로 매매하며 신호와 판단 근거(체크리스트 6개) 공개. 내 실제 매매의 수익률·승률·최대 낙폭을 **S&P 500**과 비교 |

**Architecture**

```
Next.js 16 (App Router)  ──▶  NestJS API  ──▶  PostgreSQL (Prisma, Docker)
                                  │
                                  └── Worker ── 정해진 시각에 Python 분석 엔진(uv) 실행
```

**설계 원칙**
- **주문 기능 없음**: 판단만 돕고, 매매는 증권사 앱에서
- **점수는 정해진 스크립트로만 계산**: 같은 입력이면 같은 결과
- **모든 시각은 한국 시간 기준**

`Next.js 16` `TypeScript` `Tailwind CSS v4` `TanStack Query` `NestJS` `Prisma` `PostgreSQL` `Docker` `Python` `uv`

> 기획 → 설계 문서 → 구현 → 테스트까지 **Claude Code와 페어 프로그래밍**으로 진행했습니다.

<br/>

## 🏎️ AfterLap

> F1 일정·결과를 한눈에 보는 웹앱

<p>
  <a href="https://afterlap.vercel.app/"><img src="https://img.shields.io/badge/Live_Demo-000000?style=for-the-badge&logo=vercel&logoColor=white"/></a>
  <a href="https://github.com/ysnam0123/AfterLap"><img src="https://img.shields.io/badge/Repository-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
</p>

<!-- 스크린샷 넣으면 훨씬 좋아짐 -->
<!-- <img src="./assets/afterlap.png" width="100%"/> -->

| 문제 | 해결 | 결과 |
|---|---|---|
| 첫 화면 로딩이 지나치게 느림 | 대형 SVG → WebP, 폰트 TTF → woff2, Dynamic import, 서버 컴포넌트에서 `Promise.all` 병렬 fetch 후 hydration | **LCP 25.7s → 3.2s** |
| 로그인 상태 판별 시 레이아웃 깜빡임 | React Context 인증 → **Middleware 기반 인증** | Layout shift 제거 |
| 외부 F1 API 호출 비용·지연 | **BFF**(Route Handler) + **Cache Aside / Ensure 패턴** | 외부 의존 최소화 |
| 조인이 복잡한 세션 결과 조회 | Supabase **SQL View**로 조회 로직을 DB로 이동 | 클라이언트 쿼리 단순화 |

<br/>

## 🛠️ Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,react,nextjs,tailwind,nestjs,prisma,postgres,supabase,docker,python,vercel&theme=dark" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white"/>
  <img src="https://img.shields.io/badge/Zustand-443E38?style=flat-square&logo=react&logoColor=white"/>
</p>

<br/>

## 📍 Background

- 🎓 한양대학교 ERICA — 영미언어문화 · 미디어테크놀로지 복수전공
- 💻 프로그래머스 프론트엔드 데브코스 4기 (2025.02 – 2025.08)
- 🏅 RISE 제5회 디지털 창업경진대회 장려상 (2025)

<!-- Footer -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1E3A8A,100:0F172A&height=120&section=footer" width="100%"/>
