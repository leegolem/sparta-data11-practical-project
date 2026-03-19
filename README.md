# 내일배움캠프 `sparta-data11-practical-project`

데이터 분석 및 머신러닝 실전 프로젝트 저장소입니다.

## 프로젝트 개요

- 프로젝트명: 데이터 분석 및 머신러닝 실전 프로젝트
- 프로젝트 기간: 2026.03.18 ~ 2026.03.31

## 작업 환경

- Python: 3.13
- 가상환경 및 패키지 관리: `uv`
- 주요 작업 도구: VSCode, Jupyter Notebook

## 협업 규칙 필독
[RULES.md](./RULES.md)

## 환경 구축 방법
```
# 저장소 클론
git clone https://github.com/leegolem/sparta-data11-practical-project.git
cd sparta-data11-practical-project

# 가상환경 생성 및 패키지 설치
uv sync

# 가상환경 활성화
source .venv/Scripts/activate
.venv\Scripts\Activate.ps1

# 가상환경이 정상적으로 활성화되면 터미널 앞에
(sparta-data11-practical-project) 또는 (.venv) 와 같은 표시가 나타날 수 있습니다.
```
이후 Git 관리자에게 GitHub ID 또는 이메일을 전달하여 저장소 초대를 받습니다.
초대 수락 후 아래 순서로 연결을 확인합니다.

```
1. git pull
2. 본인이 배정받은 member 폴더에서 테스트 파일 생성 또는 수정
3. 필요한 파일만 개별적으로 git add
4. git commit
5. git push

```

---

## 주의사항

- `git add .` 사용 금지  
  → 필요한 파일만 개별적으로 `git add` 해주세요.
- 대용량 파일 업로드 금지  
- 공용 저장소에는 코드, 문서, 설정 파일 위주로 관리하고  
  대용량 데이터 및 산출물은 구글 드라이브에서 관리합니다.

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
