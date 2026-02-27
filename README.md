# group5-project2-enterprise-eda
기업 데이터를 활용해 주요 패턴, 핵심 요인, 인사이트를 도출하는 탐색적 데이터 분석(EDA) 프로젝트.


## 팀원

| GitHub | Profile | Name |
|--|---|------|
| leedhroxx | @leedhroxx| 김민하  |
| rusidian | @rusidian | 장한재  |
| rshyun24| @rshyun24 | 배재현  |
| yoonha315 | @yoonha315 | 전윤하  |
| soll07 | @soll07 | 정다솔  |
| Gloveman | @Gloveman | 이창우  |

---

## 개발 규칙
### 변수 네이밍
- 변수: `snake_case`
- 클래스: `PascalCase`
- 상수: `UPPER_CASE`
- DataFrame: 접미사 `_df`
  - 예: `user_df`, `sample_df`

---

## 폴더 구조

```text
project/
|
├── data/
├── KimMinHa/
├── JangHanJae/
├── BaeJaeHyun/
├── JeonYoonHa/
├── JungDaSol/
├── LeeChangWoo/
├── requirements.txt
├── LICENSE
├── .gitignore
└── README.md
```
## 작업 방식
- PyCharm 프로젝트는 **프로젝트 폴더의 루트 경로(project/)** 로 열어서 작업합니다.
- 개인 작업 공간(본인 폴더)에는 **`.md`와 `.ipynb`만** 두도록 합니다.

---

## Git

### 커밋 메시지 작성 규칙
- 본 프로젝트는 Conventional Commits 형식을 따릅니다.
- 커밋 제목(head)은 **반드시 영어로** 작성합니다.
- 커밋 타입은 **소문자**(`feat`, `fix`, `chore`, `docs`, `refactor` 등)를 사용합니다.
- 제목은 **72자 이내**로 간결하게 작성합니다.
- 필요할 경우 커밋 본문(body)에 **한국어 설명**을 추가할 수 있습니다.
- 이슈가 있는 경우 커밋 메시지에 **이슈 번호**를 함께 명시합니다. (예: `#12`)
- 이슈 제목은 **한국어로 작성해도 무방합니다.**

### 커밋 메시지 형식

(type)(scope): 간단한 요약

예시:
```git

git commit -m "docs(readme): add development and git conventions

- README에 변수 네이밍/폴더 구조/커밋 규칙을 정리함

Refs: #1
```

### 커밋 type
- `feat`: 새로운 기능
- `fix`: 버그 수정
- `chore`: 설정 변경
- `docs`: 문서 수정
- `refactor`: 코드 구조 개선(기능 변경 없음)

### 커밋 Scope

Conventional Commits의 `scope`는  
변경이 영향을 주는 **범위(모듈/기능/도메인/폴더)** 를 짧게 요약한 라벨입니다.

> 형식: `type(scope): subject`  
> 예: `feat(preprocess): add missing value imputer`

---

### Scope 작성 원칙
- **변경 범위를 한 단어(또는 짧은 단어 조합)** 로 표현합니다.
- **팀에서 자주 쓰는 범위는 고정된 단어**로 통일합니다.
- 애매하거나 범위가 너무 넓으면 **scope는 생략 가능**합니다.
  - 예: `docs: update README`

---

### Scope 목록

- `readme` : README 및 프로젝트 설명 문서
- `docs` : 기타 문서(가이드, 규칙, 회의록 등)
- `data` : 데이터 파일/데이터 적재/데이터 스키마 관련
- `preprocess` : 전처리(결측치/인코딩/스케일링 등)
- `eda` : EDA 분석 코드, 통계/패턴 분석
- `viz` : 시각화(플롯, 차트 함수, 스타일)
- `feature` : 피처 엔지니어링/파생변수 생성
- `model` : 모델링/학습/평가 코드(필요 시)
- `report` : 결과 리포트/결과 정리(노트북 결과 포함)
- `config` : 설정 파일, 경로, 환경 변수 등
- `deps` : 라이브러리/requirements 등 의존성

---

### 예시
- `docs(readme): add project rules`
- `feat(preprocess): add outlier handling`
- `fix(data): handle invalid date formats`
- `refactor(viz): simplify plotting utilities`
- `chore(deps): update pandas and numpy`
- `docs: reorganize contribution guide`  *(scope 생략 예시)*

---

### Scope 선택 팁
- “**어떤 파일을 고쳤나?**”가 아니라  
  “**무엇을 위한 변경인가? (어디 범위인가?)**”를 기준으로 고릅니다.
- 여러 범위를 동시에 크게 건드렸다면
  - 커밋을 나누거나,
  - scope를 생략하고 `type: ...`로만 작성하는 것도 괜찮습니다.

---

### Issue 작성 규칙

본 프로젝트에서는 개발을 시작하기 전에  
반드시 작업 내용을 Issue로 먼저 작성합니다.

Issue는 작업의 목적과 범위를 명확히 하기 위한 용도이며,  
커밋 및 PR은 해당 Issue를 기준으로 연결합니다.

Issue 작성자는 기본적으로 Author를 작성합니다.  
Assignee는 무조건 지정합니다.

#### 양식
```markdown
## 작업 내용
- 무엇을 할 것인지 간단히 설명

## 목적
- 이 작업이 왜 필요한지

## 완료 기준
- [ ] 어떤 상태가 되면 완료인지

Author: @github_name
```
---

### Pull Request
PR을 하시기 전에 무조건 `sync`를 진행한 이후에 요청을 보냅니다.   
또한 PR 중에서 파일이 겹치는 경우에는 PR을 요청하지 마세요.

---