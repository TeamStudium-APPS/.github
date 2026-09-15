# 기여 가이드

## 기본 브랜치

- `main`은 배포 가능한 안정 버전을 관리합니다.
- `develop`은 다음 배포에 포함할 작업을 통합합니다.
- `main`과 `develop`에는 직접 커밋하거나 push하지 않습니다.
- 작업 브랜치는 최신 `develop`에서 생성하고 `develop`으로 Pull Request를 엽니다.
- 배포할 준비가 끝나면 `develop`에서 `main`으로 Pull Request를 엽니다.

## 브랜치 이름

브랜치 이름은 `작업 유형/간단한-영문-설명` 형식으로 작성하며 이슈 번호는 포함하지 않습니다.

| 유형 | 용도 | 예시 |
| --- | --- | --- |
| `feature` | 기능 추가 | `feature/checker-result-page` |
| `fix` | 오류 수정 | `fix/form-submit` |
| `refactor` | 기능 변화 없는 구조 개선 | `refactor/api-client` |
| `docs` | 문서 작업 | `docs/git-rule` |
| `chore` | 설정 및 환경 작업 | `chore/ci-config` |

## 커밋 메시지

커밋 메시지는 `유형: 한글 설명` 형식으로 작성합니다.

```text
feat: 체커 결과 페이지 구현
fix: 폼 중복 제출 오류 수정
refactor: API 오류 처리 구조 개선
docs: 브랜치 규칙 문서화
test: URL 검증 테스트 추가
chore: CI 설정 정리
note: refreshToken 흐름 주석 추가
```

| 유형 | 용도 |
| --- | --- |
| `feat` | 기능 추가 |
| `fix` | 오류 수정 |
| `refactor` | 기능 변화 없는 구조 개선 및 서식 정리 |
| `docs` | 문서 변경 |
| `test` | 테스트 추가 및 수정 |
| `chore` | 의존성, 도구, 설정 변경 |
| `note` | 코드 주석 추가 및 수정 |

`style`은 별도 유형으로 사용하지 않고 `refactor`로 처리합니다. 커밋 제목은 짧고 명확하게 작성하며 끝에 마침표를 붙이지 않습니다. 서로 관련 없는 변경은 커밋을 나눕니다.

## Pull Request

- 하나의 Pull Request에는 한 가지 목적의 변경만 포함합니다.
- Pull Request 제목은 브랜치 이름을 그대로 사용합니다.
- 관련 이슈는 본문에 `Closes #이슈번호` 형식으로 연결합니다.
- 리뷰 승인을 받은 후 병합합니다.
- 특정 merge 방식은 강제하지 않습니다.
- 병합된 작업 브랜치는 삭제합니다.
