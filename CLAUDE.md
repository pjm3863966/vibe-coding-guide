# 바이브 코딩 가이드

코딩 입문자를 위한 AI 활용 개발 로드맵 — 단일 페이지 정적 사이트.

## Tech Stack

- 순수 HTML + CSS + JavaScript (빌드 도구 없음)
- GitHub Pages 호스팅 (main 브랜치)
- 단일 파일: `index.html` (~2000줄, CSS/JS 인라인)

## 구조

```
index.html          # 전체 사이트 (HTML + CSS + JS)
images/             # 스크린샷 이미지 (PNG)
```

### index.html 섹션 순서

Hero → Intro → 전체 흐름 다이어그램 → AI 학습법 → Phase 1 (생활코딩) → Phase 2 (AI 도구) → Phase 3 (실전 프로젝트) → Phase 4 (사업 적용) → Summary → CTA → Footer → TOC nav + Scroll Spy JS

### CSS 변수

`:root`에 정의된 커스텀 프로퍼티 사용. 브랜드 컬러: `--accent: #4f46e5`. Phase별 컬러: `--green`(1), `--blue`(2), `--amber`(3), `--rose`(4).

## 컨벤션

- 한국어 콘텐츠 (타겟: 코딩 제로 입문자)
- 쉬운 말로 설명 — 기술 용어 쓸 때 반드시 "쉽게 말하면" 설명 포함
- 프롬프트 예시: `.prompt-box` > `.prompt-label` + `.prompt-content`
- 학습 항목: `.learn-item` > `h4` + `p`
- 이미지: `loading="lazy"`, `width`/`height` 속성 필수
- WCAG AA 준수: 텍스트 대비 4.5:1 이상 (`--text-muted: #525252`)

## 배포

- `git push origin main` → GitHub Pages 자동 배포 (1~2분)
- URL: https://pjm3863966.github.io/vibe-coding-guide/
- 빌드 단계 없음, push = 배포

## 스크린샷 촬영

```bash
npx playwright screenshot --viewport-size=1280,900 "URL" images/파일명.png
```

## 주의사항

- Phase 번호와 다이어그램 태그는 항상 동기화 유지
- TOC nav (`<nav class="toc-nav">`)의 섹션 순서도 본문과 일치해야 함
- 섹션 이동/추가 시 넘버링(detail-number) 재정렬 필요
- `index.html`이 크므로 Read 시 `offset`/`limit` 사용
