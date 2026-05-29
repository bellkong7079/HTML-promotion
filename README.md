# 굿즈 무료 나눔 홍보 페이지

QR 코드로 접근하는 다국어 굿즈 나눔 홍보 랜딩 페이지

**배포 URL:** https://promotion-lake-ten.vercel.app

---

## 지원 언어

🇮🇩 인도네시아어 · 🇺🇸 영어 · 🇰🇷 한국어 · 🇯🇵 일본어 · 🇨🇳 중국어

---

## 파일 구조

```
promotion/
├── index.html   ← 페이지 구조 + 번역 데이터 + 카운트다운 JS
└── style.css    ← 스타일 (모바일 전용)
```

---

## 내용 수정 방법

`index.html` 안의 `TRANSLATIONS` 객체에서 `// ✏️ 수정` 주석이 달린 부분을 고치면 됩니다.
5개 언어 모두 같은 항목을 각각 수정해야 합니다.

### 날짜 수정

```js
// 각 언어별로 수정
startDate:    '2025년 6월 1일 (일)',
endDate:      '2025년 6월 7일 (토) 자정',
announceDate: '2025년 6월 9일 (월)',
```

### 카운트다운 마감일 수정

```js
// 월은 0부터 시작 (6월 = 5)
const DEADLINE = new Date(2025, 5, 7, 23, 59, 59);
```

### 굿즈 이름/설명 수정

```js
goods1Name: '굿즈 이름 1',
goods1Desc: '간단한 설명',
// goods2 ~ goods4 동일하게 수정
```

### 인스타그램 링크 수정

```html
<a href="https://instagram.com/여기에_아이디_입력" ...>
```

### 주최자 닉네임 수정

```html
<p class="footer-name">by <strong>@닉네임</strong></p>
```

---

## 재배포 방법

내용 수정 후 터미널에서 실행:

```bash
cd "c:\Users\jb733\OneDrive\바탕 화면\promotion"
vercel --prod
```

---

## QR 코드 생성

배포 URL을 복사해서 [qrcode-monkey.com](https://qrcode-monkey.com) 에 붙여넣으면 무료로 생성됩니다.
