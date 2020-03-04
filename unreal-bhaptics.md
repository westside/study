### 플러그인 

### LNK 2019 
* https://dawnarc.com/2018/10/ue4lnk2019-unresolved-external-symbol-getprivatestaticclass/ 내경우엔 이거 PrivateStaticClass에서 에러가 남
* 기본적으로 구현체가 없을 때 나는 경우가 많은데 UE에서는 자기가 구현체를 새로 만들다보니 뭐지 싶은 에러가 발생하는 듯 https://vaert.tistory.com/5




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

*  알고보니 MarketPlace/Plugins 랑 Project의 Plugins랑 같은게 있는데, Project Plugins를 바꿔야하는데 엉뚱한걸 바꿔서 몰랐음 ㅠ

* 리빌드할때는 프로젝트만 리빌드 하면 됨

![image](https://user-images.githubusercontent.com/1837913/69769679-2a0fd200-11c9-11ea-9811-f912234d6df4.png)




### UE 4.23부터는 include Engine이렇게 하는게 아니고 쪼개서 인클루드를 하게 되어 있음 
* 아래 참조: https://github.com/bhaptics/TactUnrealEngine4/commit/c68da35b8013208dec02ad5c08756b038c948e23

```
#include "Components/StaticMeshComponent.h"
#include "Materials/MaterialInstanceDynamic.h"
```



### Quest 연동 방법 
* 이게 다라고? 

![image](https://user-images.githubusercontent.com/1837913/69779127-48d29080-11ea-11ea-8ad5-9d78bb82ed97.png)

* 문서: https://developer.oculus.com/documentation/quest/latest/concepts/unreal-engine/




### Open Level할때 에러 
* 해당 레벨을 설정에 추가 해야 함 https://answers.unrealengine.com/questions/667710/why-my-level-cant-be-opened-on-android.html

### 모바일 디폴트 조이스틱 끄기 혹은 바꾸기
* https://forums.unrealengine.com/development-discussion/android-development/103685-change-touch-interface-at-runtime



### Android에서 크래시
* 아직 원인을 못찾음 UI위젯 관련한건데..  이미지를 작은것으로 바꾸니 없어짐...ㅠㅠ 4.22 

```
2019-12-26 08:59:42.116 3846-4006/? E/InputDispatcher: channel '2c15ab5 com.bhaptics.SampleProject4_22/com.epicgames.ue4.GameActivity (server)' ~ Channel is unrecoverably broken and will be disposed!
2019-12-26 08:59:42.171 4147-4158/? E/BtGatt.ContextMap: remove() - removed: 14
2019-12-26 08:59:42.171 4147-4175/? E/BtGatt.ContextMap: Context not found for ID 14
2019-12-26 08:59:42.172 3846-3880/? E/WindowManager: RemoteException occurs on reporting focusChanged, w=Window{2c15ab5 u0 com.bhaptics.SampleProject4_22/com.epicgames.ue4.GameActivity EXITING}
    android.os.DeadObjectException
        at android.os.BinderProxy.transactNative(Native Method)
        at android.os.BinderProxy.transact(Binder.java:1145)
        at android.view.IWindow$Stub$Proxy.windowFocusChanged(IWindow.java:500)
        at com.android.server.wm.WindowState.reportFocusChangedSerialized(WindowState.java:3920)
        at com.android.server.wm.WindowManagerService$H.handleMessage(WindowManagerService.java:5456)
        at android.os.Handler.dispatchMessage(Handler.java:106)
        at android.os.Looper.loop(Looper.java:214)
        at android.os.HandlerThread.run(HandlerThread.java:65)
        at com.android.server.ServiceThread.run(ServiceThread.java:44)
```


### Android deploy error : Attempt to construct staged filesystem reference from absolute path 걍 지운다 UE4Game 폴더를

https://forums.unrealengine.com/development-discussion/android-development/1566545-error-system-argumentexception-attempt-to-construct-staged-filesystem-reference-from-absolute-path
