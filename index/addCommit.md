# Add & Commit
앞에서 원격저장소와 지역저장소에 대한 얘기를 했습니다.  
`add`와 `commit` 모두 지역저장소 내부에서 파일을 추가하는 역할을 하는데 어떤 차이가 있는지 알아봅시다.

## 1. add
`add`는 **working directory** 에서 변경된 내용을 **Index(staging area)** 에 추가하는 역할을 합니다.
```
git add [-option] [filename]
```
`add` 뒤에는 `filename`이 올수도 있고 `option`을 지정해 줄 수도 있습니다.
```
git add .
```
위와 같이 `filename`으로 `.`을 사용하면 모든 하위 디렉토리를 의미하며 하위 디렉토리에 있는 모든 파일을 stage하게 됩니다.  
**단, 삭제된 파일은 반영되지 않습니다.**
```
git add -A
```
`option`으로 `-A`를 줬을 경우에는, `.`와 마찬가지로 하위 디렉토리에 있는 모들 파일을 stage하게 됩니다.  
**`.`와 다른 점은 삭제된 파일도 반영됩니다.**

## 2. commit
우리가 `add`를 통해 변경된 파일들을 stage했지만  
아직 이 변경내용들을 확정짓지는 않았습니다.

최종 확정을 위해서는 `commit`을 통해 **Staging area** 에 있는 파일들을 **HEAD**에 추가해 줘야합니다.

```
git commit [-m "(decription)"]
```
`-m` option을 줬을 경우 변경된 내용에 대한 설명을 붙일 수 있습니다.

이렇게 **working directory**의 변경 내용들을 최종 확정본으로 만들었지만 아직 여전히 외부저장소에는 반영되지 않았습니다.

다음 챕터에서는 어떻게 내 지역저장소의 변경 내용을 외부저장소에 반영하는지 알아봅시다.

---
## 다음 챕터
### [Push & Pull](pushPull.md)