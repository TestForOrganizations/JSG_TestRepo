# 📡 IRC 소켓 프로그램

IRC 기반의 실시간 소켓 통신 프로그램입니다.  
효율적인 협업과 관리를 위해 일관된 작성 규칙을 따릅니다.

---

## 📌 마일스톤 작성 가이드

### ✅ 마일스톤 작성 원칙
본 프로젝트는 **총 5단계 마일스톤**을 통해 점진적으로 개발됩니다.  
각 단계는 의미 있는 기능 단위를 기준으로 설정되며, 다음과 같은 형식을 권장합니다.

### 🏷️ 마일스톤 제목 예시

1단계 : 콘솔 기반 채팅 시스템 (WinSock2)
2단계 : Win32 GUI + 메시지 루프 이해
3단계 : DirectX 기반 텍스트 UI 렌더링
4단계 : 비동기 소켓 이벤트 처리 (WSAAsyncSelect)
5단계 : 기능 확장 및 고도화

---

## 📝 이슈 작성 가이드

**모든 작업은 이슈를 생성한 후 진행해 주세요.**  
아래 형식을 참고하여 이슈를 명확하게 작성합니다.

### ✏️ 이슈 작성 형식

### ISSUE

- labels: [작업 타입 예: feat, fix, chore]  
- Detail: 작업 상세 설명을 서술합니다.

### TODO

- [ ] 작업 1  
- [ ] 작업 2  
- [ ] 작업 3

### 🧩 이슈 작성 예시

### ISSUE

- labels: feat  
- Detail: C++ 플레이어가 선택한 맵에 대한 `.umap`과 `datatable`을 요청하는 HTTP API 작성

### TODO

- [ ] HTTP 요청 함수 셋업  
- [ ] 요청할 맵 식별자(id) 전달 구현  
- [ ] 서버 측 rep 함수 선언

---

## 🌿 브랜치 명명 규칙

브랜치는 작업 내용을 대표하는 **기능 단위 이름**으로 작성해 주세요.  
가능한 경우 **PascalCase** 사용을 권장합니다.

### ✅ 브랜치 예시

- `socket listen`
- `client server connect`

---

## 💬 커밋 컨벤션

# Commit 메세지 가이드

> 우리 프로젝트는 [Conventional Commits 1.0.0](https://www.conventionalcommits.org/ko/v1.0.0/)의 구조와 사용 방식을 차용했습니다.


## 기본 구조

```bash
<type>[optional scope][!]: <description>

[optional body]

[optional footer(s)]
```

---

## 타입(객찰) 목록 & 설명

| 타입 (type)         | 의미           | 설명                                         |
| ----------------- | ------------ | ------------------------------------------ |
| `feat`            | 기능 추가        | 사용자에게 영향을 주는 새로운 기능 추가 시 사용                |
| `fix`             | 버그 수정        | 사용자에게 영향을 주는 버그(오류) 수정 시 사용                |
| `BREAKING CHANGE` | API 등 파괴적 변경 | 함수가 호환되지 않게 변경된 경우 사용                      |
| `docs`            | 문서 변경        | 코드 변경 없이 문서(`README`, `CHANGELOG` 등)만 수정   |
| `style`           | 코드 스타일 변경    | 의미 없는 드래귀, 세미켓, 커드 포맷 등만 수정                |
| `refactor`        | 코드 리파터리닝     | 기능 변화 없이 구조만 감정한 경우                        |
| `perf`            | 성능 효율 감소     | 성능 최적화 관련 변경                               |
| `test`            | 테스트 추가/수정    | 테스트 관련 코드만 변경한 경우                          |
| `build`           | 빌드 시스템 관련 변경 | `webpack`, `npm`, `gulp` 등 빌드 도구 설정 변경     |
| `ci`              | CI 구성 관련 변경  | `GitHub Actions`, `Travis`, `Jenkins` 등 변경 |
| `chore`           | 기타 자비성 작업    | 의연성 업데이트, 폴더 정리 등                          |
| `revert`          | 컨미티 되돌림      | 이전 컨미티를 되돌린다는 의미. `Refs:`로 SHA 가래 명시가 권장됨  |

---

## 단절적 변경 (BREAKING CHANGE)

두 가지 방식이 있습니다.

### 1. `!` 통합

```bash
feat!: 사용자의 로그인 방식 변경
```

### 2. footer 대안

```bash
BREAKING CHANGE: 기존 설정 방식이 더 이상 지원되지 않음.
```

---

## scope(적용 범위) 포함 예

```bash
fix(parser): 공백 파싱 오류 수정
```

> 많은 프리젝트에서 컨텐츠 간 제목의 개수가 많을 때 용존한 관리가 가능해지고 있습니다.

---

## description(각정 선출) 필수

```bash
fix: 로그인 신고 오류 수정
```

---

## body(복서) 예

```bash
feat: 이메일 보내기 기능 추가

개인의 주민에게 주민정보가 보내지가 되는 기능.
메일 템플릿과 스\uucf00줄러를 함께 구성했습니다.
```

---

## footer(꼬마리) 예

```bash
BREAKING CHANGE: 설정 파일 포맷이 변경되어서 호환되지 않습니다
Refs: #123
Reviewed-by: alice
```

---

## 예제 포함

```bash
feat(lang): 폴란드어 추가
```

```bash
docs: correct spelling of CHANGELOG
```

```bash
chore!: Node 6 지원 삭제

BREAKING CHANGE: use JavaScript features not available in Node 6.
```

---

## 🧹 코드 컨벤션

> 추후 확정 예정입니다.

- 변수 및 함수 명명 방식  
- 들여쓰기 스타일 (예: 4칸 스페이스)  
- 헤더 및 소스 파일 구조 등  

---

## ✅ 작업 순서 요약

1. 마일스톤 등록  
2. 이슈 작성 및 할당  
3. 브랜치 생성 (`기능명`)  
4. 커밋 컨벤션 준수하여 작업  
5. PR 생성 및 코드 리뷰  
6. 머지 및 이슈/마일스톤 정리

---

> 이 문서는 팀의 협업과 유지보수를 위한 표준입니다.  
> 모든 기여자는 본 README를 반드시 숙지하고 준수해 주세요.




