# discord-devly

[devly](https://discord.gg/) 디스코드 서버 운영 자산 (public).

## 구성

- `avatars/` — 출처별 아바타 이미지 (Discord webhook 발행 시 raw URL로 참조)
- `core/` — 봇 로직 + 설정 (private submodule, 인증 필요)

## Avatars

각 출처의 webhook 아바타로 사용되는 이미지.  
파일명 규칙: `<source_id>.jpg` (예: `yogiyo.jpg`, `channeltalk.jpg`).

raw URL 형식:
```
https://raw.githubusercontent.com/<USERNAME>/discord-devly/main/avatars/<source_id>.jpg
```

## Core (private)

봇 로직 / 출처 설정 / state는 별도 private repo에 있음.  
clone 시 submodule 까지 받으려면:

```bash
git clone --recursive git@github.com:<USERNAME>/discord-devly.git
# 이미 clone한 뒤라면
git submodule update --init --recursive
```
