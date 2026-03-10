# CPC 월간 리포트 생성기

Excel 파일을 업로드하여 자동으로 CPC 광고 운영 리포트를 생성하는 웹 애플리케이션입니다.

## 기능

- 📊 Excel/CSV 파일 업로드
- 📈 자동 데이터 분석 및 시각화
- 💾 PNG/PDF 다운로드 기능
- 🎨 깔끔한 리포트 디자인

## 기술 스택

- **Backend**: FastAPI, Python 3.11
- **Frontend**: HTML, CSS, JavaScript
- **Data Processing**: Pandas, openpyxl
- **Deployment**: Render.com

## 배포

### Render.com 배포
```bash
# render.yaml 설정으로 자동 배포
# URL: https://cpc-report-monthly.onrender.com
```

## 최근 업데이트

### 2026-03-10
- ✅ **UI 개선**: 불필요한 텍스트 제거
  - 상단 "CPC 운영리포트" 텍스트 제거
  - "예산 분석" 섹션 제거
  - "주간 분석 및 발견" 섹션 제거
  - 리포트가 더 깔끔하고 집중적인 디자인으로 개선됨

- ✅ **배포 최적화**
  - Railway → Render.com으로 전환 (안정적인 배포)
  - openpyxl 3.1.5로 업데이트 (Pandas 호환성)
  - Dockerfile 최적화 (이미지 크기 약 60MB 감소)
  - .dockerignore 추가 (빌드 속도 개선)

- ✅ **Vercel 지원 추가**
  - Mangum을 통한 서버리스 함수 지원
  - vercel.json 설정 추가

## 개발 환경 설정

```bash
# 가상환경 생성
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# 패키지 설치
pip install -r requirements.txt

# 로컬 서버 실행
python main.py
```

## 파일 구조

```
.
├── main.py              # FastAPI 서버
├── index.html           # 메인 페이지
├── app.js              # 프론트엔드 로직
├── styles.css          # 스타일시트
├── Dockerfile          # Docker 설정
├── render.yaml         # Render 배포 설정
├── vercel.json         # Vercel 배포 설정
└── requirements.txt    # Python 패키지
```

## 라이센스

MIT License
