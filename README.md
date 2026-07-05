# RISU/MANUAL

RisuAI 비공식 가이드 사이트. 순수 HTML/CSS 정적 사이트라 빌드 단계 없음.

## 구조
```
risuai-guide/
├── index.html          # 랜딩 + 허브 페이지
├── assets/
│   └── style.css        # 전체 스타일
└── README.md
```

## 로컬 확인
그냥 `index.html`을 브라우저로 열면 됨. (VS Code Live Server 써도 됨)

## 깃허브 → 버셀 배포

1. 이 폴더 내용 그대로 새 깃허브 레포에 push
   ```
   git init
   git add .
   git commit -m "init: risuai guide site"
   git branch -M main
   git remote add origin <레포주소>
   git push -u origin main
   ```
2. https://vercel.com → **Add New → Project** → 방금 만든 레포 선택
3. Framework Preset: **Other** (정적 HTML이라 빌드 커맨드 없음, Output Directory는 루트 `.`)
4. Deploy 누르면 끝. 이후 `main` 브랜치에 push할 때마다 자동 재배포됨.

## 다음에 붙일 것 (가이드 목차 06개 항목)
`index.html`의 `#guides` 섹션 카드들이 지금은 전부 `href="#"`로 비어있음.
페이지를 늘릴 거면 `/guide/01-install.html` 식으로 폴더 만들어서 각 항목 링크만 갈아끼우면 됨 — 레이아웃/스타일은 재사용 가능하게 짜놨음.
