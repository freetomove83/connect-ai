# Git 저장소 동기화 문제 해결 안내

## 1. Remotes 확인
먼저 Git remotes가 올바르게 설정되어 있는지 확인합니다.
```bash
git remote -v
```

## 2. Branch 이름 확인
`main` branch가 존재하는지 확인합니다.
```bash
git branch
```

## 3. Repository URL 확인
현재 설정된 repository의 URL이 올바른지 확인합니다.
```bash
git remote get-url origin
```

## 4. Remotes 리셋 및 추가
Remotes가 잘못 등록되어 있는 경우, `git remote rm <remote_name>` 명령어를 사용하여 제거하고, 다시 추가할 수 있습니다.
```bash
git remote remove origin
git remote add origin <correct-repository-url>
```

## 5. 결과 검증
다시 Git pull을 시도합니다.
```bash
git pull
```