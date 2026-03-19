# 프로젝트 규칙

## 작업 시작 루틴
- 작업 시작 전 반드시 `git pull`을 실행합니다.
- 원격 저장소(GitHub)에 올라온 최신 작업물을 먼저 로컬에 동기화한 뒤 작업합니다.

---
## 라이브러리 추가 규칙 (`uv`)
새 라이브러리를 추가한 경우 아래 순서를 따릅니다.


### 추가한 사람
1. `uv add 패키지명` 실행
2. 변경된 `pyproject.toml`, `uv.lock` 파일을 함께 커밋
3. push까지 반영

### 다른 팀원
1. `git pull`
2. `uv sync`
---

## 작업물 받기 (조원이 해야 할 일)
기본적으로 아래 명령어를 먼저 실행합니다.
```
git pull
- 아래 중 하나라도 해당하면 추가로 실행:
    - pyproject.toml 변경됨
    - uv.lock 변경됨
    - import 에러 발생 / 라이브러리가 없다는 에러가 뜸
- 이 경우:
    - uv sync
```

## 커밋 규칙 !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
- 개인 작업물 커밋 시 `git add .` 사용 금지
- 반드시 아래처럼 **본인 폴더만** add 합니다.
```powershell
git add "본인폴더명"
```
- 공용 파일 수정 시
    - 수정한 파일만 명시적으로 add 합니다.
    - 커밋 메시지에는 어떤 파일을 어떻게 수정했는지 드러나도록 작성합니다.

- 만약 `git pull` 하기전에 커밋을 해 오류가 발생한 경우
    1. `git pull --rebase origin main`으로 최신 내용을 먼저 반영합니다.
    2. 충돌이 발생하면 충돌 내용을 수정합니다.
    3.  `git add 수정한파일` -> `git rebase --continue` 순서로 진행합니다.
    4. `git push --force`는 팀 협의 없이 사용하지 않습니다.

### 파일 및 데이터 관리 규칙
- 대용량 파일은 GitHub에 업로드하지 않습니다.
- 원본 데이터는 integrated/data/에만 보관합니다.
- 공용 반영이 필요한 내용만 협의 후 integrated/에 반영합니다.


# 프로젝트 파일 구성
```
sparta-data11-practical-project/
├─ integrated/                    # 공용 통합 작업 폴더
│  ├─ data/                       # 공동 데이터 (원본, 수정 금지)
│  └─ integrated_analysis.ipynb   # 공용 통합 분석 파일
│
├─ notebooks/
│  ├─ member1/            # 개인 작업물
│  ├─ member2/
│  ├─ member3/
│  ├─ member4/
│  └─ member5/
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