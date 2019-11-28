### Setting up Android 
* Android 환경 설정할땐 CodeWorks 프로그램 이용해서 설치하는게 편한듯 아래 위치에 있음
```
Epic Games\UE_4.23\Engine\Extras\AndroidWorks\Win64\CodeWorksforAndroid-1R7u1-windows.exe
```
* 빌드 에러 난게 이거 잘못한것과 연관 있었음 

### UI Designer
* https://docs.unrealengine.com/en-US/Engine/UMG/HowTo/index.html


### Widget 
* https://docs.unrealengine.com/en-US/Engine/UMG/UserGuide/CreatingWidgets/index.html


### 4.21에서 빌드될걸 4.23 에서 사용할 때 
* 비쥬얼 스튜디오에서 빌드를 다시 해야함 

```
LogPlayLevel: Error:     C:/Program Files/Epic Games/UE_4.23/Engine/Source/Runtime/CoreUObject/Public\UObject/UObjectBaseUtility.h(483,14) 
LogPlayLevel: Error:     C:/Program Files/Epic Games/UE_4.23/Engine/Source/Runtime/CoreUObject/Public\UObject/UObjectBaseUtility.h(483,15)

```

### C++ 프로젝트로 바꾸려면 
* 프로젝트에 C++  추가 

![image](https://user-images.githubusercontent.com/1837913/69768822-8a047980-11c5-11ea-85eb-5569f2942a68.png)

* uproject 우클릭 -> generate visual studio files
