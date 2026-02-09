# 🎨 AI 릴레이 동화 만들기

어린이를 위한 AI 동화 생성 웹 애플리케이션

## 🚀 Vercel 배포 방법

### 1단계: GitHub에 업로드

```bash
# Git 초기화
git init

# 파일 추가
git add .

# 커밋
git commit -m "Initial commit"

# GitHub 리포지토리 연결
git remote add origin https://github.com/your-username/your-repo-name.git

# 푸시
git push -u origin main
```

### 2단계: Vercel에 배포

1. [Vercel](https://vercel.com) 접속 및 로그인
2. "Add New..." → "Project" 클릭
3. GitHub 리포지토리 선택
4. **Environment Variables 설정** (매우 중요!)
   - Key: `ANTHROPIC_API_KEY`
   - Value: `sk-ant-api03-...` (당신의 Anthropic API 키)
5. "Deploy" 클릭

### 3단계: 완료!

배포가 완료되면 Vercel이 제공하는 URL로 접속하면 됩니다.
예: `https://your-project-name.vercel.app`

## 📁 프로젝트 구조

```
.
├── api/
│   └── generate.js         # Serverless function (API 프록시)
├── public/
│   └── index.html          # 웹 페이지
├── package.json            # 프로젝트 설정
├── vercel.json             # Vercel 설정
├── .env.example            # 환경변수 예시
├── .gitignore              # Git 무시 파일
└── README.md               # 이 파일
```

## ⚙️ 로컬 개발 환경

```bash
# 패키지 설치
npm install

# 개발 서버 실행
npm run dev
```

브라우저에서 `http://localhost:3000` 접속

**주의**: 로컬 개발시 `.env` 파일을 만들고 API 키를 추가하세요:
```
ANTHROPIC_API_KEY=sk-ant-api03-...
```

## ⚠️ 중요 사항

- **절대로 API 키를 코드에 직접 넣지 마세요!**
- API 키는 Vercel의 Environment Variables에만 설정하세요
- `.env` 파일은 절대 GitHub에 업로드하지 마세요 (`.gitignore`에 포함됨)

## 🎯 사용 방법

1. 주인공 정하기 테이블에서 A팀과 B팀의 정보 입력
2. 키워드 정하기 테이블에서 각 팀의 키워드 5개 입력
3. 원하는 팀의 "동화 생성하기" 버튼 클릭
4. AI가 자동으로 동화와 삽화 생성!

## 🛠 기술 스택

- Frontend: React (via CDN)
- Backend: Vercel Serverless Functions
- AI: Anthropic Claude API
- Deployment: Vercel

## 📝 라이선스

MIT
