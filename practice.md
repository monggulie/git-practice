# Git 실습 순서

## 1. 현재 상태 확인

저장소 디렉터리에서 다음 명령어를 실행합니다.

```bash
git status
git log --oneline
```

## 2. 문서 수정

`git-basics.md`에서 복습할 내용을 한 문장 추가한 뒤 저장합니다.

```bash
git diff -- git-basics.md
git add git-basics.md
git diff --cached
git commit -m "docs: Git 기본 개념 복습 내용 추가"
```

`git diff --cached`로 개인정보와 의도하지 않은 변경이 없는지 확인한 후
커밋합니다. 커밋 메시지에는 변경 목적을 구체적으로 적습니다.

## 3. 원격 저장소 연결 및 업로드

GitHub에서 이름이 `git-practice`인 공개 저장소를 만듭니다.
아래의 `YOUR_USERNAME`은 본인 GitHub 사용자명으로 바꿉니다.

```bash
git remote add origin https://github.com/YOUR_USERNAME/git-practice.git
git push -u origin main
```

이미 `origin`이 연결되어 있다면 `git remote -v`로 주소를 확인합니다.

## 4. 결과 확인

```bash
git ls-files
git rev-list --count HEAD
git status
```

GitHub에서도 파일 목록, 커밋 이력, Public 표시를 확인합니다.
과제 제출 제목에는 `https://github.com/YOUR_USERNAME/git-practice` 형식의
전체 저장소 주소를 입력합니다.
