# LIFEMEAL FREEZE LAB — 동결건조 연구 미션 게임

- 플레이: https://miraclead2026.github.io/freeze-lab-game/
- `index.html` : 이미지·폰트가 인라인된 단일 파일 빌드 (`npm run build:single` 결과)
- `freeze-lab-game-src.zip` : React + TypeScript 소스 프로젝트 (수정 후 다시 빌드해 index.html 교체)
- 마지막 화면 QR/버튼 링크: `src/config/gameConfig.ts` → `REWARD_URL`
- 게임 밸런스(물방울 개수 등): `src/config/gameConfig.ts` / 배치 좌표: `src/config/layout.ts`
- 단계 진입 후킹 멘트("얼려라!!" 등): 각 `src/components/steps/*Step.tsx` 의 `<StepBriefing hook=...>`
- 테마(ICE RESEARCH LAB): `src/styles/theme-lab.css` — 인트로·FREEZE·BLEND 배경 이미지는 Higgsfield 생성본(CDN URL). 영구 보관하려면 이미지를 `public/assets/freeze-lab/`에 내려받고 `--bg-lab` / `--bg-food` 경로를 바꾸면 됩니다.
- `index_v4.html`: 이전 바닐라 JS 버전 백업 (현재 배포본과 무관)

## 두 가지 빌드
- `index.html` — 모바일용 (배포 링크). 마지막 화면 "혜택 받으러 가기" 버튼 → `REWARD_URL`
- `kiosk/freeze-lab-kiosk.html` — 현장 32" 터치 모니터(LG 32U889SA-W, 세로)용. 마지막 화면 QR, 75초 무조작 시 처음으로.
  빌드: `VITE_FORCE_MODE=kiosk npm run build:single`
- `kiosk/`: PC 연결 런처(.bat/.command), webOS 앱 `appinfo.json`(ipk는 `ares-package`), 운영 README
- 음성 파일은 미사용 (원본은 `assets/audio/`, 재생 코드는 `src/audio/sfx.ts`의 `sample()`에 남아 있음)
