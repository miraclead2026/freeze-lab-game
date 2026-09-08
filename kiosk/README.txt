FREEZE LAB 키오스크 (LG 스마트 모니터 스윙 32U889SA-W, 세로 9:16)

freeze-lab-kiosk.html = 현장 모니터 전용 빌드. 마지막 화면 QR, 75초 무조작 시 처음으로, 첫 터치에서 전체화면 요청.
모니터용 주소: https://miraclead2026.github.io/freeze-lab-game/kiosk/freeze-lab-kiosk.html
모바일용(배포 링크): https://miraclead2026.github.io/freeze-lab-game/  (마지막 화면 "혜택 받으러 가기" 버튼)

모니터 세팅
- 스탠드를 피벗해서 세로로 세운다. 게임은 세로 화면 기준.
- 설정 > 절전/화면 끄기 자동 종료를 끈다.

방법 A. 모니터 웹브라우저 (장비 없음)
- 와이파이 연결 > webOS 웹브라우저 > 위 모니터용 주소 입력 > 첫 터치 시 전체화면.

방법 B. 노트북/미니PC USB-C 연결 (가장 안정적)
- 32U889SA-W는 USB-C 한 줄로 영상+터치+충전. Chrome을 --kiosk 옵션으로 실행 (런처 .bat/.command 는 배포 패키지 zip 참고).

방법 C. webOS 앱 설치 (모니터 단독)
- LG 개발자 계정 > 모니터에 Developer Mode 앱 > npm i -g @webos-tools/cli > ares-setup-device > ares-install <ipk> > ares-launch com.lifemeal.freezelab
- Developer Mode는 50시간마다 연장 필요.

배경 사진 3장은 온라인 주소를 참조하므로 인터넷이 없으면 단색 배경으로 대체됨.
