# 내일배움캠프 `sparta-data11-practical-project`
데이터 분석 및 머신러닝 실전 프로젝트 저장소입니다.

## 프로젝트 개요
- 프로젝트명: 데이터 분석 및 머신러닝 실전 프로젝트
- 프로젝트 기간: 2026.03.18 ~ 2026.03.31

본 프로젝트는 스타벅스 고객 정보, 프로모션 오퍼 정보, 거래 및 이벤트 로그 데이터를 활용해\
프로모션이 고객 반응과 구매 행동에 어떤 영향을 미치는지 분석하고,\
그 결과를 KPI 중심의 Tableau 대시보드로 시각화하는 CRM/마케팅 데이터 분석 프로젝트입니다.
> 미정

### 프로젝트 배경
스타벅스는 다양한 고객에게 여러 유형의 프로모션을 여러 채널을 통해 제공하고 있습니다.\
하지만 모든 고객이 동일하게 반응하는 것은 아니며, 오퍼 유형·전달 채널·고객 특성에 따라 반응과 구매 행동은 달라질 수 있습니다.\

본 프로젝트에서는 스타벅스 데이터를 활용해\
고객, 오퍼, 이벤트 로그를 종합적으로 살펴보고 프로모션 반응과 구매 행동의 차이를 분석하고자 합니다.
> 미정

### 프로젝트 목표
본 프로젝트의 세부 분석 주제는 초기 EDA와 문제 정의 과정을 통해 구체화할 예정이며,\
현재는 스타벅스 고객·오퍼·거래 로그 데이터를 기반으로\
프로모션 반응, 고객 행동, 채널 효과를 다각도로 탐색하는 것을 1차 목표로 합니다.

이후 데이터 탐색 결과를 바탕으로 핵심 문제를 구체화하고,\
적절한 KPI를 설정한 뒤 Tableau 대시보드로 인사이트를 시각화할 예정입니다.
> 미정

### 프로젝트 과정
1. 문제 정의
   - 분석 목적과 핵심 비즈니스 문제를 설정
2. KPI 설정
   - 반응률, 전환률, 구매 관련 지표 정의
3. 데이터 이해 및 전처리
   - 고객, 오퍼, 이벤트 로그 데이터 구조 파악 및 정리
4. 분석 수행
   - 고객/오퍼/채널 관점의 EDA 및 인사이트 도출
5. 대시보드 제작
   - KPI 중심의 Tableau 시각화 구성
6. 마케팅 전략 제안
   - 분석 결과를 바탕으로 실행 가능한 방향 제시
> 미정

---
## 작업 환경
- Python: 3.13
- 가상환경 및 패키지 관리: `uv`
- 주요 작업 도구: VSCode, Jupyter Notebook

### 설치된 주요 패키지
- 데이터 처리
  - pandas
  - numpy

- 시각화
  - matplotlib
  - seaborn
  - plotly

- 통계
  - scipy
  - statsmodels
  - pingouin

- 머신러닝
  - scikit-learn
  - xgboost
  - lightgbm
  - catboost


## 협업 규칙
자세한 협업 규칙은 아래 문서를 확인해주세요.
- [RULES.md](./RULES.md)

---
## 환경 구축 방법
### 1. 저장소 초대 받기
Git 관리자에게 **GitHub ID 또는 이메일**을 전달한 뒤, 저장소 초대를 수락합니다.

### 2. 저장소 클론 및 환경 설정
```
# 저장소 클론
git clone https://github.com/leegolem/sparta-data11-practical-project.git
cd sparta-data11-practical-project

# 가상환경 생성 및 패키지 설치
uv sync

# 가상환경 활성화

## Git Bash 사용 시
source .venv/Scripts/activate

## PowerShell 사용 시
.venv\Scripts\Activate.ps1

# 가상환경이 정상적으로 활성화되면 터미널 앞에
(sparta-data11-practical-project) 또는 (.venv) 와 같은 표시가 나타날 수 있습니다.
```
### 3. 연결 확인 방법
초대 수락 및 환경 설정이 끝난 뒤, 아래 순서로 정상 연결 여부를 확인합니다.
```
1. git pull
2. 본인이 배정받은 member 폴더에서 테스트 파일 생성 또는 수정
3. git add "본인폴더명"
4. git commit -m "test: OOO 작업 환경 연결 확인"
5. git push
```
---
## 주의사항

- `git add .` 사용 금지  
  → 필요한 파일만 개별적으로 `git add` 해주세요.
- 대용량 파일 업로드 금지
- 공용 저장소에는 코드, 문서, 설정 파일 위주로 관리하고\
  대용량 데이터 및 산출물은 구글 드라이브[🔗](https://drive.google.com/drive/folders/1GnmR5mnsTjVaTYijMxV99tGETrJBbVLo?usp=sharing)에서 관리합니다.\

---
## 전체 폴더 구조 설명
```
sparta-data11-practical-project/
├─ integrated/                    # 공용 통합 작업 폴더
│  ├─ data/                       # 공동 데이터 (원본, 수정 금지)
│  └─ integrated_analysis.ipynb   # 공용 통합 분석 파일
│
├─ member1/                       # 개인 작업 공간
├─ member2/
├─ member3/
├─ member4/
├─ member5/
│
├─ pyproject.toml
├─ uv.lock
├─ README.md
└─ .gitignore
```

폴더 역할 정리
- integrated/
    - 팀 공용 데이터 및 통합 분석 파일을 관리하는 폴더
    - data/에는 원본 데이터만 보관
    - 원본 데이터 직접 수정 금지
    - 공용으로 반영할 코드/노트북만 관리

- member1~5/
    - 각자 전처리 / 시각화 / 실험용 노트북 작성 공간
    - 개인 작업물은 본인 폴더에만 커밋
    - 공용 반영이 필요한 내용만 협의 후 integrated/에 반영
