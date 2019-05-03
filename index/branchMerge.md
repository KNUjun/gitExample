# Branch & Merge

파일을 변경하고 git에서 어떻게 지역저장소, 외부저장소로 반영하는지에 대해 알아보았습니다.

이제 `branch`와 `merge`에 대해서 알아봅시다.

## 1. branch
>`brach`의 사전적 의미는 **가지**를 의미합니다.

`branch`는 개발을 진행할 때 원본파일은 안전하게 놔두고 싶을 때 사용합니다.  
그러고 개발이 완료되면 다시 원래의 가지로 돌아와 병합(`merge`)시키면 됩니다.

git에서 새로운 repository를 만들면 자동으로 `master`란 가지를 만들어줍니다.  
구름IDE에서 현재 디렉토리뒤에 적혀 있던 (`master`)가 바로 현재 어느 `branch`에 있는지를 의미합니다.
```
root@goorm:/workspace/gitExam/git(master)#
```

#### branch 만들기  

먼저 'apple' 이라는 `branch`를 만들어 봅시다.

```
root@goorm:/workspace/gitExam/git(master)# git branch apple
root@goorm:/workspace/gitExam/git(master)# git branch
    apple
  * master
```
아무 옵션없이 `git branch`를 했을 경우에는 전체 `branch` 목록을 확인 할 수 있습니다.  
`branch` 이름 앞에 `*`표시가 있는 가지가 현재 `branch`입니다.

#### branch 전환하기
repository를 처음 만들면 자동으로 `master` 가지를 만들고 그 가지에 위치시킨다고 앞에서 설명드렸습니다.  
그럼 이제 `branch`를 변경해봅시다.

`branch`의 변경은 `git checkout <branchName>`을 사용합니다.
```
root@goorm:/workspace/gitExam/git(master)# git checkout apple
Switched to branch 'apple'
root@goorm:/workspace/gitExam/git(apple)#
```
터미널 뒤의 ()에 있는 내용이 `master`에서 `apple`로 바뀐 것을 확인했을 겁니다.  
이것이 바로 `branch`가 변경되었다는 것을 의미합니다.

`branch`의 생성과 전환을 한번에 할 수도 있습니다.
```
root@goorm:/workspace/gitExam/git(apple)# git checkout -b banana
Switched to a new branch 'banana'
root@goorm:/workspace/gitExam/git(banana)#
```
#### branch 삭제하기
위에서 만든 `apple` 가지와 `banana` 가지를 삭제해 봅시다.

`branch`의 삭제는 `git branch -d <branch>`를 이용합니다.
```
root@goorm:/workspace/gitExam/git(banana)# git checkout master
Switche to branch 'master'
root@goorm:/workspace/gitExam/git(master)# git branch -d apple
Deleted branch apple (was 95aa559)
root@goorm:/workspace/gitExam/git(master)# git branch -d banana
Deleted branch banana (was 95aa559)
```
## 2. merge
`merge`는 이렇게 나뉜 `branch`들을 병합하는 역할을 수행합니다.