# 권오성 · 카카오 AI 루키 캠프 포트폴리오

ComputeDefend의 개발 동기, 문제 해결 과정, 소통 경험과 프로그래밍 경험을 소개하는 정적 랜딩 페이지입니다.

## 로컬 미리보기

저장소 루트에서 실행합니다. Python 외에 별도 패키지 설치나 빌드는 필요하지 않습니다.

```powershell
python -m http.server 8765 --bind 127.0.0.1 --directory portfolio
```

브라우저에서 <http://127.0.0.1:8765>를 엽니다. 종료는 `Ctrl+C`입니다. 소개용 페이지이며 실제 프로세스 제어 API를 호출하지 않습니다.

## 파일 구성

```text
portfolio/
├── index.html                   # 지원 항목별 본문
├── style.css                    # 반응형 레이아웃과 스타일
├── README.md
└── assets/
    ├── fonts/PretendardVariable.woff2
    └── images/
        ├── process-list.png     # 앱 목록 (히어로)
        └── api-key-entry.png    # API 키 입력 (프로젝트)
```

## 반영 내용 (2026-11-17)

- `../docs/howToUse.md`를 바탕으로 비용 부담에서 시작한 동기, 작은 기능부터 구현한 과정, 학원 선생님과의 의견 교환, AI 활용 경험을 반영했습니다.
- 비전·협업·마무리의 자리표시자를 제공된 경험으로 교체했습니다.
- `../docs/images/`의 원본 2장을 위 파일명으로 복사했습니다. 이미지에 대체 텍스트, 원본 보기 링크, 설명을 제공합니다. API 키 값은 원본에서 마스킹되어 있습니다.
- 기존 청록색·초록색 디자인과 한국어 로컬 폰트를 유지했습니다. 이미지 비율을 보존하고 모바일에서는 한 열로 배치합니다.
- 현재 소스 기준으로 HTTP 폴링, Fetch API, SSE, Upstash Redis와 로컬 메모리 저장소를 설명합니다. SSE 갱신은 구현된 기능으로 옮겼습니다.
- `.hallmark/` 검수 산출물은 Git에서 제외합니다.

## 내용 수정 기준

`index.html`의 `#vision`, `#problem`, `#teamwork`, `#coding`, `#project`를 수정합니다. 색상과 간격은 `style.css`의 `:root`에서 관리합니다. 이미지 교체 시 `src`, `width`, `height`, `alt`, 캡션도 함께 갱신합니다.

개발 기록인 `docs/howToUse.md`의 Supabase/PostgreSQL 설명과 현재 코드의 Upstash Redis 구현은 다릅니다. 현재 동작은 `src/Web/BackEnd/main.py`와 `src/Web/FrontEnd/main.js`를 기준으로 확인합니다.

이번 작업은 저장소 소스 반영 범위입니다. 포트폴리오 호스팅 URL은 아직 지정하지 않았습니다. 제출 전에 학생 본인이 이름·학교·경험·표현을 검토하고, 실제 제출할 URL의 화면을 확인해야 합니다.
