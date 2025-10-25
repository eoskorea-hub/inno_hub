# 이노허브 예약 시스템 🏫

재학생을 위한 클래스룸 예약 시스템 - Google Sheets 백엔드 + GitHub Pages 호스팅

**🌐 Live Demo**: `https://eoskorea-hub.github.io/inno_hub/`

---

## 📦 완성된 파일 목록

### 🚀 배포용 (중요!)
1. **[index.html](computer:///mnt/user-data/outputs/index.html)** ⭐ - **GitHub Pages에 바로 배포 가능한 완전한 HTML 파일**
   - React 없이 순수 HTML/CSS/JavaScript
   - Tailwind CSS 사용
   - 모바일 반응형
   - 당신의 저장소 정보로 설정 완료

2. **[GITHUB_PAGES_DEPLOY.md](computer:///mnt/user-data/outputs/GITHUB_PAGES_DEPLOY.md)** ⭐ - **배포 완벽 가이드**
   - 단계별 배포 방법
   - 문제 해결
   - 이미지 설정
   - 당신의 저장소(`eoskorea-hub/inno_hub`) 기준으로 작성됨

### 📚 백엔드
3. **[Code.gs](computer:///mnt/user-data/outputs/Code.gs)** - Google Apps Script 백엔드 코드
4. **[SETUP_GUIDE.md](computer:///mnt/user-data/outputs/SETUP_GUIDE.md)** - 스프레드시트 설정 가이드
5. **[API_DOCUMENTATION.md](computer:///mnt/user-data/outputs/API_DOCUMENTATION.md)** - API 문서

### 🎨 개발용
6. **[innohub-improved.jsx](computer:///mnt/user-data/outputs/innohub-improved.jsx)** - 개선된 React 컴포넌트
7. **[innohub-with-github-images.jsx](computer:///mnt/user-data/outputs/innohub-with-github-images.jsx)** - 이미지 설정 포함 버전

### 📖 문서
8. **[GITHUB_IMAGE_SETUP.md](computer:///mnt/user-data/outputs/GITHUB_IMAGE_SETUP.md)** - 이미지 설정 가이드
9. **[README.md](computer:///mnt/user-data/outputs/README.md)** - 이 문서

---

## 🚀 빠른 시작 (5분!)

### 방법 1: GitHub Pages 배포 (추천)

```bash
# 1. 저장소 클론
git clone https://github.com/eoskorea-hub/inno_hub.git
cd inno_hub

# 2. index.html 복사
cp /path/to/index.html ./

# 3. 이미지 폴더 생성 (선택사항)
mkdir -p images
# 이미지 파일들을 images/ 폴더에 복사

# 4. Git에 추가
git add .
git commit -m "Add InnoHub booking system"
git push

# 5. 완료! 1-5분 후 접속
# https://eoskorea-hub.github.io/inno_hub/
```

**자세한 내용**: [GITHUB_PAGES_DEPLOY.md](computer:///mnt/user-data/outputs/GITHUB_PAGES_DEPLOY.md) 참조

### 방법 2: 로컬 테스트

```bash
# index.html을 브라우저로 열기
open index.html
# 또는
python -m http.server 8000
# http://localhost:8000 접속
```

---

## 📁 필요한 프로젝트 구조

```
inno_hub/
├── index.html              ← 메인 파일 (이미 설정 완료)
├── images/                 ← 방 이미지들 (선택사항)
│   ├── green-room.jpg
│   ├── orange-room.jpg
│   ├── cozy-zone.jpg
│   ├── esports.jpg
│   └── duolingo.jpg
└── README.md
```

**중요**: 이미지가 없어도 작동합니다! Placeholder 자동 표시됨.

---

## ✨ 주요 기능

### 📋 학생용
- ✅ 5개 클래스룸 예약 (Green, Orange, Cozy, E-sports, Duolingo)
- ✅ 부스별 독립 예약 (Green: GR1-4, E-sports: PC1-3, Duolingo: 부스1-2)
- ✅ 실시간 예약 가능 시간 확인
- ✅ 이메일로 내 예약 조회
- ✅ 예약 취소 (3시간 전까지)
- ✅ 그룹 예약 지원
- ✅ 모바일 반응형

### 👨‍💼 관리자용
- ✅ 예약 승인/거절
- ✅ 노쇼 처리
- ✅ 날짜별 필터링
- ✅ 실시간 대시보드

---

## 🔧 설정

### 1. Google 스프레드시트 백엔드 (10분)

1. 새 구글 스프레드시트 생성
2. [SETUP_GUIDE.md](computer:///mnt/user-data/outputs/SETUP_GUIDE.md) 따라하기
3. Apps Script에 [Code.gs](computer:///mnt/user-data/outputs/Code.gs) 복사
4. 웹 앱으로 배포
5. URL을 `index.html`의 `API_URL`에 입력

**현재 설정된 API URL**:
```javascript
const API_URL = 'https://script.google.com/macros/s/AKfycbyVfV9mMCNzC03Hu_epgD1C2csWyIWWXOi0R3DDx9DxeATIdfb_9oRt1FUxVRwqDM4/exec';
```

### 2. 이미지 설정 (선택사항)

**옵션 A: Placeholder 사용 (현재 설정)**
- 이미지 없이 바로 사용 가능
- 자동으로 색상별 placeholder 표시

**옵션 B: 실제 이미지 추가**
```bash
mkdir -p images
# 이미지 파일 복사
git add images/
git push
```

자세한 내용: [GITHUB_IMAGE_SETUP.md](computer:///mnt/user-data/outputs/GITHUB_IMAGE_SETUP.md)

---

## 🖼️ 필요한 이미지

```
images/
├── green-room.jpg      (Green Room)
├── orange-room.jpg     (Orange Room)
├── cozy-zone.jpg       (Cozy Talk Zone)
├── esports.jpg         (E-sports)
└── duolingo.jpg        (Duolingo Booth)
```

**권장 사양**:
- 크기: 800x600px (4:3 비율)
- 형식: JPG or PNG
- 용량: 각 500KB 이하

---

## 📊 데이터 구조

### Google 스프레드시트 시트:
1. **예약목록** - 모든 예약 저장
2. **사용자정보** - 학생 정보 및 노쇼 기록
3. **노쇼기록** - 노쇼 이력
4. **설정** - 시스템 설정값

---

## 🔐 보안

- ✅ Google Apps Script로 안전한 백엔드
- ✅ 이메일 기반 간단 인증
- ✅ CORS 자동 처리
- ✅ HTTPS 강제 가능 (GitHub Pages)

---

## 📱 지원 플랫폼

- ✅ 데스크톱 (Chrome, Firefox, Safari, Edge)
- ✅ 모바일 (iOS Safari, Android Chrome)
- ✅ 태블릿

---

## 🐛 문제 해결

### 사이트가 안 열려요
→ [GITHUB_PAGES_DEPLOY.md](computer:///mnt/user-data/outputs/GITHUB_PAGES_DEPLOY.md) 문제 해결 섹션 참조

### 예약이 안 돼요
→ API URL 확인 (index.html 파일 내)
→ Google Apps Script 웹 앱 배포 확인

### 이미지가 안 보여요
→ 정상입니다! Placeholder 자동 사용됨
→ 실제 이미지 추가 방법: [GITHUB_IMAGE_SETUP.md](computer:///mnt/user-data/outputs/GITHUB_IMAGE_SETUP.md)

---

## 📚 문서 목록

| 파일 | 설명 |
|------|------|
| **GITHUB_PAGES_DEPLOY.md** | ⭐ GitHub Pages 배포 가이드 (당신의 저장소 기준) |
| **SETUP_GUIDE.md** | Google 스프레드시트 백엔드 설정 |
| **API_DOCUMENTATION.md** | API 엔드포인트 문서 |
| **GITHUB_IMAGE_SETUP.md** | 이미지 설정 방법 |

---

## 🎯 배포 체크리스트

- [ ] `index.html`을 저장소 루트에 복사
- [ ] (선택) `images/` 폴더에 이미지 추가
- [ ] Git push 완료
- [ ] GitHub Pages 설정 확인
- [ ] `https://eoskorea-hub.github.io/inno_hub/` 접속 테스트
- [ ] Google 스프레드시트 백엔드 설정
- [ ] API URL 연결 확인
- [ ] 예약 테스트
- [ ] 관리자 패널 테스트
- [ ] 모바일에서 테스트

---

## 🎉 완료!

모든 설정이 완료되었습니다!

**Live URL**: `https://eoskorea-hub.github.io/inno_hub/`

### 다음 단계:
1. `index.html`을 GitHub에 push
2. 1-5분 기다리기
3. URL 접속
4. 테스트 예약 만들기
5. 관리자 패널에서 승인
6. 완료! 🚀

---

## 📞 지원

문제가 있으면:
1. 관련 문서 확인 (위 문서 목록 참조)
2. 브라우저 개발자 도구 Console 확인
3. GitHub Actions 탭에서 배포 로그 확인

---

## 📄 라이선스

이 프로젝트는 재학생 예약 시스템으로 자유롭게 사용 및 수정 가능합니다.

---

**Made with ❤️ for Elite Open School**

*Last Updated: 2025-10-25*
