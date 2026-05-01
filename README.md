# Personal Homepage — Yeonjun Hwang

GitHub Pages용 개인 홈페이지입니다.

## 📁 폴더 구조

레포지토리에는 아래 두 파일만 있으면 됩니다:

```
your-repo/
├── index.html      ← 홈페이지 본체
└── profile.jpg     ← 본인 사진 (직접 추가)
```

## 🖼 사진 넣기

1. 본인 사진을 **`profile.jpg`** 라는 이름으로 저장합니다 (세로 인물 비율 권장).
2. `index.html`과 같은 폴더에 둡니다.
3. `index.html`을 열어 `<!-- ====== PROFILE PHOTO GOES HERE ====== -->` 주석을 찾아서:
   - `<div class="photo-placeholder">...</div>` 블록을 **삭제**하고
   - 그 아래 `<!-- <img src="profile.jpg" alt="Yeonjun Hwang"> -->` 줄에서 `<!--`, `-->` 주석 기호를 **제거**합니다.

> 다른 파일명이나 폴더(예: `images/profile.jpg`)를 쓰고 싶으면 `<img src="...">`의 경로만 그에 맞춰 바꾸면 됩니다.

## 🚀 GitHub Pages 배포 방법

### 방법 1 — 사용자 사이트로 배포 (`username.github.io`)

이 방법이 가장 깔끔합니다. URL이 `https://username.github.io` 가 됩니다.

1. GitHub에 새 레포지토리를 만듭니다. **레포지토리 이름은 반드시 `본인깃허브아이디.github.io`** (예: `yeonjun.github.io`).
2. 이 폴더의 파일들(`index.html`, `profile.jpg`)을 그 레포에 push 합니다.
   ```bash
   git init
   git add .
   git commit -m "init homepage"
   git branch -M main
   git remote add origin https://github.com/본인아이디/본인아이디.github.io.git
   git push -u origin main
   ```
3. 1~2분 뒤 `https://본인아이디.github.io` 에 접속하면 홈페이지가 보입니다.

### 방법 2 — 프로젝트 사이트로 배포 (아무 레포명)

레포 이름을 자유롭게 쓰고 싶을 때 (URL이 `https://username.github.io/레포이름` 형태가 됩니다).

1. 아무 이름으로 레포를 만들고 파일을 push.
2. GitHub 레포 페이지 → **Settings** → 좌측 **Pages** 메뉴.
3. **Source**를 `Deploy from a branch`로, **Branch**를 `main` / `/ (root)`로 선택 후 **Save**.
4. 1~2분 뒤 URL이 표시되면 접속.

## ✏️ 내용 수정

`index.html`을 텍스트 에디터로 열어 직접 수정하면 됩니다. 주요 섹션:

- **HERO** (`<header class="hero">`): 이름, 한줄 소개, 연락처
- **About** (`<section id="about">`): 자기소개
- **Education** (`<section id="education">`): 학력
- **Publications** (`<section id="publications">`): 논문 (Under Review / Published / Preprint 그룹)
- **Beyond Research** (`<section id="more">`): 수상, 강의, 학회 활동

## 🎨 색상 변경

상단 `<style>` 안의 `:root` 변수만 바꾸면 전체 톤이 바뀝니다:

```css
--accent: #1d4ed8;       /* 메인 액센트 컬러 (지금: 푸른색) */
--accent-deep: #14306e;  /* 어두운 액센트 */
```
