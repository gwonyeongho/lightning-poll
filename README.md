# ⚡ 번개 투표

링크 하나로 누구나 참여하는 실시간 투표. 로그인도, 앱 설치도, 서버 운영도 필요 없습니다.

**사이트:** https://gwonyeongho.github.io/lightning-poll/

## 어떻게 동작하나요

- 질문과 선택지는 **링크 자체**(URL 해시, base64)에 담깁니다. 그래서 데이터베이스 없이 링크만 공유하면 됩니다.
- 표 수는 공개 카운터 서비스 [Abacus](https://abacus.jasoncameron.dev)에 `lightning-poll-<투표ID>/opt<번호>` 키로 저장됩니다. 누구나 읽고, 1씩 올릴 수만 있습니다.
- 한 기기에서 한 번만 투표할 수 있도록 브라우저 저장소(localStorage)에 기록합니다. 완벽한 중복 방지는 아니지만 가벼운 투표에는 충분합니다.
- 결과는 6초마다 자동 갱신되며, 투표하거나 「결과만 볼래요」를 누르면 보입니다.

## 파일

- `index.html` — 페이지 전체(HTML, CSS, JS). 의존성은 Google Fonts와 QR 코드 생성 라이브러리(cdnjs)뿐입니다.

## 직접 띄우기

이 저장소를 포크한 뒤 Settings → Pages에서 `main` 브랜치의 `/ (root)`를 선택하면 끝입니다.
