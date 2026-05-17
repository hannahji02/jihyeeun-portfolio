# Vercel 배포 가이드

## 파일 구성

```
portfolio-site/
├── index.html      ← 메인 페이지
└── profile.jpg     ← 프로필 사진
```

이 두 파일을 같은 폴더 안에 두면 끝. 다른 파일 추가 불필요.

---

## 1단계: 로컬에서 확인 (선택)

배포 전에 본인이 직접 결과물 확인하고 싶으면:

1. `portfolio-site` 폴더를 적당한 위치(예: 바탕화면)로 다운로드
2. 폴더 안 `index.html` 파일을 더블클릭
3. 기본 브라우저에서 사이트가 열림
4. 다크모드 토글, 카드 클릭 등 기능 확인

문제 없으면 다음 단계로.

---

## 2단계: Vercel 가입

1. https://vercel.com 접속
2. 우측 상단 **"Sign Up"** 클릭
3. **"Continue with Email"** 선택 (GitHub 연동 피하기)
4. 이메일 입력 → 인증 메일 확인 → 가입 완료

---

## 3단계: 새 프로젝트 배포

1. Vercel 대시보드 좌측 상단 **"Add New..."** 클릭 → **"Project"** 선택
2. 가운데 영역에 **"Deploy from a folder"** 또는 **"Drag and drop"** 옵션 보임
   - 만약 GitHub 연동만 보이면, 페이지 어딘가 **"Deploy a template"** 또는 **"Upload"** 옵션을 찾기
3. **`portfolio-site` 폴더 전체를 드래그**해서 업로드
4. Project Name 입력란에 **`jihyeeun`** 입력 (도메인이 `jihyeeun.vercel.app`이 됨)
5. **"Deploy"** 버튼 클릭
6. 1-2분 대기 → 배포 완료

---

## 4단계: 도메인 확인

배포 완료되면 Vercel이 도메인 자동 발급:
- **`https://jihyeeun.vercel.app`**

브라우저에서 접속해서 정상 작동 확인.

---

## 5단계: 게시

리멤버·이력서·이메일 서명 등에 링크 추가:

### 리멤버 "웹사이트·블로그" 필드
```
https://jihyeeun.vercel.app
```

### 리멤버 구직용 자기소개 마지막에 추가 (선택)
```
포트폴리오: https://jihyeeun.vercel.app
```

### 이메일 서명
```
지혜은 · Hyeeun Ji
hyeeunji02@gmail.com
Portfolio: jihyeeun.vercel.app
```

---

## 수정이 필요할 때

`index.html` 파일 내용을 수정한 뒤:

### 방법 A. Vercel 웹에서 재배포
1. Vercel 대시보드 → 본인 프로젝트 클릭
2. 우측 상단 **"..."** → **"Redeploy"**
3. 수정된 폴더 다시 드래그

### 방법 B. Vercel CLI 사용 (선택, 더 빠름)
- 터미널 익숙하면 `vercel` CLI 설치 후 명령어 한 줄로 배포 가능
- 지금은 방법 A로 충분

---

## 문제 발생 시

| 증상 | 해결 |
|---|---|
| 사진이 안 보임 | `profile.jpg`가 `index.html`과 같은 폴더에 있는지 확인 |
| 폰트가 깨짐 | 인터넷 연결 상태 확인 (Google Fonts 로드 필요) |
| 모바일에서 깨짐 | 모바일 브라우저 캐시 클리어 후 재접속 |
| 배포 실패 | Vercel 대시보드 → Deployments 탭에서 에러 로그 확인 |

---

## 사이트 구성 (참고)

| 섹션 | 내용 |
|---|---|
| **Hero** | 정체성 + 정량 어필 + 프로필 사진 |
| **Metrics** | EX 등급, 92.22점, 4.7/5, 운영 인프라 13건+ |
| **Career** | 박물관→콴다 Timeline + 서사 |
| **4 Phases** | 4단계 카드 (클릭하면 펼침) |
| **Evaluation** | 평가 카드 3개 + 정량 바 차트 |
| **Environment** | 일하고 싶은 환경 3가지 + 보충 |
| **Contact** | 이메일 CTA |

### 기능
- 라이트/다크 토글 (우측 상단 버튼)
- 카드 클릭 시 상세 펼침/접기
- 스크롤 시 요소 등장 애니메이션
- 반응형 (데스크탑·태블릿·모바일)

---

## 다음 액션

1. 위 5단계 따라 배포
2. `jihyeeun.vercel.app` 접속해서 정상 작동 확인
3. 리멤버 등에 링크 게시
