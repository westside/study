### 플러그인 

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
* Build/ 랑 Intermidiate/  지우자.. !! 

```
LogPlayLevel: Error:     C:/Program Files/Epic Games/UE_4.23/Engine/Source/Runtime/CoreUObject/Public\UObject/UObjectBaseUtility.h(483,14) 
LogPlayLevel: Error:     C:/Program Files/Epic Games/UE_4.23/Engine/Source/Runtime/CoreUObject/Public\UObject/UObjectBaseUtility.h(483,15)

```

### C++ 프로젝트로 바꾸려면 
* 프로젝트에 C++  추가 

![image](https://user-images.githubusercontent.com/1837913/69768822-8a047980-11c5-11ea-85eb-5569f2942a68.png)

* uproject 우클릭 -> generate visual studio files
  * 아래와 같은 에러 발생 

```
Running C:/Program Files/Epic Games/UE_4.23/Engine/Binaries/DotNET/UnrealBuildTool.exe  -projectfiles -project="C:/Users/westside/Documents/Unreal Projects/BuildTest/BuildTest.uproject" -game -rocket -progress -log="C:\Users\westside\Documents\Unreal Projects\BuildTest/Saved/Logs/UnrealVersionSelector-2019.11.28-10.00.27.log"
Discovering modules, targets and source code for project...
While compiling C:\Users\westside\Documents\Unreal Projects\BuildTest\Intermediate\Build\BuildRules\BuildTestModuleRules.dll:
c:\Users\westside\Documents\Unreal Projects\BuildTest\Intermediate\Source\BuildTest.Build.cs(3,14) : error CS0101: 
ERROR: Unable to compile source files.
```

* 리빌드할때는 프로젝트만 리빌드 하면 됨
![image](https://user-images.githubusercontent.com/1837913/69769679-2a0fd200-11c9-11ea-9811-f912234d6df4.png)




### from 4.23부터는 include Engine이렇게 하는게 아니고 쪼개서 인클루드를 하게 되어 있음 
* 아래 참조: https://github.com/bhaptics/TactUnrealEngine4/commit/c68da35b8013208dec02ad5c08756b038c948e23

```
#include "Components/StaticMeshComponent.h"
#include "Materials/MaterialInstanceDynamic.h"
```

