# Push & Pull

이제까지 지역저장소에서 변경된 내역들을 확정짓는 법을 알아봤습니다.

자, 그럼 이제 확정된 내용을 외부저장소에 반영해 반영해봅시다.

## push
`push`는 **HEAD** 에 있는 내용을 **외부저장소**에 보내는 역할을 합니다
```
git push origin master
```
**git**에서는 처음 외부저장소를 만들시 자동으로 `origin`과 `master`를 만들어줍니다.
>`origin`이란 외부저장소의 주소를 의미합니다.  
>`master`는 branch를 의미합니다.

`git remote -v` 를 이용해 현재 저장되었는 외부저장소 주소들을 확인 할 수 있습니다.
```
root@goorm:/workspace/gitExam/git/(master)# git remote -v
origin https://github.com/KNUjun/git.git (fetch)
origin https://github.com/KNUjun/git.git (push)
```

`origin` 주소를 통하여 `fetch`를 했을 때와 `push`를 했을 때 사용될 주소를 출력해주고 있습니다.  

`fetch`는 `pull`에서, `master`는 `branch`에서 다루겠습니다.

## pull
`pull`은 `push`와 반대되는 개념으로 **외부저장소의 변경내용**을 **지역저장소**로 반영하는 역할을 합니다.

`commit`과 다른 점이라면, `commit`은 외부저장소의 **모든 내용**을 복사해서 가져오는 반면  
`pull`은 지역저장소와 외부저장소를 비교해 외부저장소의 **변경내용**을 지역저장소로 가져오는 역할을 합니다.
>`commit`은 모든내용을, `pull`은 변경내용을

```
git pull
```
`pull` 입력 시 자동으로 `origin` 주소의 외부저장소에서 변경내용을 가져옵니다.

`fetch`는 `pull`과는 조금 다른 성격을 가졌는데  
`pull`이 **가져와서 저장하기**라면 `fetch`는 **가져오기**입니다.  

`fetch`를 하더라도 내 지역저장소가 바뀌는 것이 아니라 변경내용들을 확인한 후 반영할 수 있습니다.  
이렇게 반영까지 하면 `pull`과 동일한 역할을 수행한 것입니다.

---
## 다음 챕터
### [Branch & Merge](branchMerge.md)
