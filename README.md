# git_tutorial
Git tutorial 과 Git을 사용하면서 발생한 이슈들을 troubleshooting 한 기록들을 모아놓은 곳.

## tracked && Staged

- Git은 파일을 add 시키면 그 순간 추적(track)함과 동시에 파일을 staging 한다. add 시킨 이후에 다시 파일을 수정한 이후 커밋을 했을 때, add 이후 수정 된 부분은 Unstaged 상태가 되므로 커밋 내용에 반영이 되지 않으므로 다시 add - commit 단계를 거쳐서 staged 상태에 올려 두어야 한다.

## Git - 리비전 조회하기

### git reflog
- Git은 자동으로 `Branch`와 `HEAD`가 지난 몇 달 동안에 가리켰던 커밋을 모두 기록한다. 이 기록은 `git reflog` 명령어를 실행하여 얻을 수 있다.

- 특정 시점의 Head로 옮겨 가고 싶다면, `git reset --hard HEAD@{number}` 명령어로 유실된 파일을 빠르게 복구할 수 있는 장점이 있다.

- @{number} 규칙을 사용해서 바로 이전 번호의 head가 가리키는 목록을 조회 할 수 있다.
```
$ git show HEAD@{5}
```
- 순서 뿐 아니라, 시간도 사용할 수 있는데 어제의 master 브랜치를 보고 싶다면 다음과 같이 명령어를 써주면 된다.
```
$ git show master@{yesterday}
```
