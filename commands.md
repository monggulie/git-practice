# Git 명령어 정리

| 명령어 | 역할 |
| --- | --- |
| `git init -b main` | 기본 브랜치를 main으로 지정해 저장소 초기화 |
| `git status` | 작업 디렉터리와 스테이징 상태 확인 |
| `git add README.md` | 특정 파일의 현재 내용을 스테이징 |
| `git diff` | 아직 스테이징하지 않은 변경 확인 |
| `git diff --cached` | 다음 커밋에 들어갈 변경 확인 |
| `git commit -m "docs: 소개 추가"` | 스테이징한 변경 기록 |
| `git log --oneline` | 커밋 이력을 간단히 확인 |
| `git ls-files` | Git이 추적하는 파일 목록 확인 |
| `git mv old.md new.md` | 파일 이름 변경 및 변경 사항 스테이징 |
| `git restore --staged notes.md` | 파일 내용은 유지하고 스테이징 취소 |
| `git remote -v` | 원격 저장소 주소 확인 |
| `git push -u origin main` | main 브랜치를 업로드하고 추적 관계 설정 |

## 주의해서 사용하는 명령어

- `git rm <파일>`은 작업 디렉터리에서도 파일을 삭제합니다.
- `git rm --cached <파일>`은 로컬 파일을 남기고 추적 대상에서 제거합니다.
- `git restore <파일>`은 커밋하지 않은 수정 내용을 버릴 수 있습니다.

위 명령어는 먼저 `git status`와 `git diff`로 상태를 확인한 뒤 사용합니다.
파일 추적 해제는 과거 커밋에서 해당 내용을 지우는 작업과 다릅니다.

## 인증 정보 관리

GitHub 인증에는 안전하게 관리되는 인증 수단을 사용합니다.
토큰을 파일, 커밋 메시지, 원격 저장소 URL에 직접 적지 않습니다.
