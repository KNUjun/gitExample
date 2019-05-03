# Push & Pull

이제까지 지역저장소에서 변경된 내역들을 확정짓는 법을 알아봤습니다.

자, 그럼 이제 확정된 내용을 외부저장소에 반영해 반영해봅시다.

## push
`push`는 **HEAD** 에 있는 내용을 외부저장소에 보내는 역할을 합니다
```
git push origin master
```
`origin`이란 외부저장소의 주소를 의미합니다.
```
root@goorm:/workspace/gitExam/git/(master)# git remote -v
origin https://github.com/KNUjun/git.git (fetch)
origin https://github.com/KNUjun/git.git (push)
```
위 코드를 쳐보면 현재 저장되어 있는 외부저장소 주소들을 출력해 줍니다.

`master`는 branch를 의미합니다.

**git**에서는 처음으로 외부저장소를 만들시 자동으로 `origin`과 `master`를 만들어줍니다.