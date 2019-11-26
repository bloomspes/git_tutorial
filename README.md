# git_tutorial
Git tutorial 과 Git을 사용하면서 발생한 이슈들을 troubleshooting 한 기록들을 모아놓은 곳.

## tracked && Staged

- Git은 파일을 add 시키면 그 순간 추적(track)함과 동시에 파일을 staging 한다. add 시킨 이후에 다시 파일을 수정한 이후 커밋을 했을 때, add 이후 수정 된 부분은 Unstaged 상태가 되므로 커밋 내용에 반영이 되지 않으므로 다시 add - commit 단계를 거쳐서 staged 상태에 올려 두어야 한다.

