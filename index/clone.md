# Clone

본격적으로`clone`을 배우기전에  
**git**이 어떻게 돌아가는 지부터 알아봅시다.
## Repository
>Repository란 저장소를 의미합니다.

우리가 Github에 만든 repository를 `외부저장소(remote repository)` 라고 합니다.  
외부저장소는 각각의 `지역저장소(local repository)` 의 결과물들이 저장되는 곳입니다.

### Local repository
여러분들의 컴퓨터에 있는 `지역저장소`는 다시 세 가지 영역으로 분류됩니다.
1. **Working directory**
>파일이 실제로 변경, 저장되는 곳입니다.
2. **Index**
>준비 영역(Staging area) 이라고도 하며 add를 통해 파일들을 Index에 추가합니다.
3. **Head**
>Staging area에 있는 파일들을 commit을 통해 최종 확정짓는 곳입니다.

이렇게 지역저장소에서 **최종 확정본(commit)** 을 외부저장소에 보냄으로서 공동개발자들과 함께 개발할 수 있는 것입니다. 

---
## Clone
>`clone`은 외부저장소를 복제하는 명령어입니다.

외부저장소에 있는 파일 전부를 복제해서 내 지역저장소로 가져오고 싶을 때 `clone`을 사용합니다.
```
git clone (원격저장소 주소)
```
    >지역저장소의 복제는 원격저장소 주소 자리에 지역저장소의 주소를 입력하면 됩니다.

---
## 다음 챕터
### [Add & Commit](addCommit.md)
