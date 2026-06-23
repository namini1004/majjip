# 오늘 점심 추천 페이지

## GitHub + Vercel 배포 방법

### 1단계 — GitHub 저장소 생성

1. [github.com/new](https://github.com/new) 접속
2. Repository name: `lunch-recommendation` (원하는 이름)
3. Public 또는 Private 선택 후 **Create repository**

### 2단계 — 파일 업로드

```bash
# 로컬에서 진행하는 경우
git init
git add .
git commit -m "첫 배포"
git remote add origin https://github.com/[내 계정]/lunch-recommendation.git
git push -u origin main
```

또는 GitHub 웹에서 `index.html` + `vercel.json` 두 파일을 직접 드래그 업로드해도 됩니다.

### 3단계 — Vercel 연동

1. [vercel.com](https://vercel.com) 접속 → GitHub 계정으로 로그인
2. **Add New Project** → 방금 만든 저장소 선택
3. Framework Preset: **Other** (자동 감지됨)
4. **Deploy** 클릭

→ 약 10~20초 후 `https://[프로젝트명].vercel.app` URL 발급

### 이후 업데이트

GitHub에 파일을 push하면 Vercel이 자동으로 재배포합니다.

## 파일 구조

```
lunch-recommendation/
├── index.html   # 메인 페이지
├── vercel.json  # Vercel 배포 설정
└── README.md    # 이 파일
```
