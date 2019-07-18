## z-fighting (textture flicking in android)
* https://www.unity3dtips.com/unity-z-fighting-solutions/


## Profiling 관련 
```
Don’t make photorealistic games
Avoid using post-processing [guide]
Adjust [Unity specific] project settings
Toggle GPU instancing on materials
Combine your meshes [suggested tool]
Consider using Google Seurat [video guide, binaries for Seurat]
Use Amplify Imposters tool [suggested tool]
Use static lightning [video guide]
Set up occlusion culling [video guide]
Be ready to remove detail to stay performant
Use More Effective Coroutines tool (if your project uses a lot of coroutines) [suggested tool]
Profile often [video guide]
Start learning Unity’s C# job system [video guide]
Use texture atlasing [video guide]
```

### Google's Seurat 
* 코드 : https://github.com/googlevr/seurat
* 캡쳐 볼륨이랑 같이쓰면!! https://www.youtube.com/watch?v=FTI_79f02Lg
* seurat-pipeline-msvc2017-x64.exe 빌드파일은 https://github.com/ddiakopoulos/seurat/releases
* unity plugin: https://github.com/googlevr/seurat-unity-plugin

### texture atlasing
* 이건 여러개 텍스쳐 묶어서 드로콜 줄이는거


### 레퍼런스
* https://www.roadtovr.com/vr-game-optimization-for-oculus-quest-mobile-hardware/

## Unity with android native 
* https://github.com/Real-Serious-Games/Unity-Android-Plugin-Example
* BLE sample https://www.programcreek.com/java-api-examples/?code=rlatkdgus500/UnityBluetoothPlugin/UnityBluetoothPlugin-master/Assets/Scripts/Bluetooth/AndroidJavaFile/BluetoothPlugin.java#

* c++ in windows? https://github.com/wm4n/unity-cpp-lib
* c++ in windows and android https://github.com/Meach/UnitySimpleNativeLibrary

* android ndk https://github.com/googlesamples/android-ndk/tree/master-ndkbuild
* android aar sample with so https://github.com/forexample/android-aar-simple
* Difference between static and shared libraries?  https://stackoverflow.com/questions/2649334/difference-between-static-and-shared-libraries
* unity tutorial https://docs.unity3d.com/Manual/AndroidNativePlugins.html
* tutorial codelabs https://codelabs.developers.google.com/codelabs/android-studio-cmake/#2
* tutorial on android dev https://developer.android.com/studio/projects/gradle-external-native-builds

* unity android c (korean) 
    * https://m.blog.naver.com/PostView.nhn?blogId=callsonda&logNo=220934040935&proxyReferer=https%3A%2F%2Fwww.google.co.kr%2F
    * http://duzi077.tistory.com/134
    * https://developer.android.com/studio/projects/add-native-code?hl=ko#download-ndk

* android cmake https://github.com/taka-no-me/android-cmake


## Websocekt Library
* Good Tutorial!!! https://channel9.msdn.com/Blogs/2p-start/Combining-Windows-10-features-with-Unity-games-in-your-own-plugin
* websocket sharp with UWP : 
    * https://github.com/green-coder/unity3d-ddp-client/blob/dev/unity-project/Assets/Moulin/DDP/websocket/WebSocketUWP.cs

## Json Library
* JSON NET - based on Newton Json  https://assetstore.unity.com/packages/tools/input-management/json-net-for-unity-11347
    * ISSUE : https://stackoverflow.com/questions/31069962/newtonsoft-json-jsonserializationexception-unable-to-find-constructor-to-use-fo

## Windows MR example 
   * https://github.com/Microsoft/MixedRealityToolkit-Unity

## Effect관련 Tutorial
* riffle effect : https://github.com/keijiro/RippleEffect
* wave effect 
   * shader : https://www.youtube.com/watch?v=WJrQ_bgWqvw 
   * code http://pastebin.com/WC5giTZC
* glowing effect 
   * https://www.youtube.com/watch?v=ppYZsPHI234

* effect pack : https://www.youtube.com/watch?v=Wqj7hXePTn8 좋은 것 많음
   * 매뉴얼 없는듯 : https://www.youtube.com/watch?v=tm33_ckaY5w&feature=youtu.be 참고..

* fireball 같은 느낌 
   * https://www.youtube.com/watch?v=RO8hQC-_zBo
   
   
## assets

* 무기 https://www.assetstore.unity3d.com/kr/#!/content/19365
* 자동차 https://www.assetstore.unity3d.com/kr/#!/content/51082
* 캐쥬얼 게임 https://www.assetstore.unity3d.com/kr/#!/content/43863
* 자동차 https://www.assetstore.unity3d.com/kr/#!/content/34404
* 탁구 받기 https://www.assetstore.unity3d.com/kr/#!/content/47894
* 비행기 https://www.assetstore.unity3d.com/kr/#!/content/50239 
* 캐쥬얼 게임 https://www.assetstore.unity3d.com/kr/#!/content/31172
* 비행기 https://www.assetstore.unity3d.com/kr/#!/content/44792
* 레이싱 https://www.assetstore.unity3d.com/kr/#!/content/22615
* infinite runner https://www.assetstore.unity3d.com/kr/#!/content/51328
* VR 컨텐츠 (심플) https://www.assetstore.unity3d.com/kr/#!/content/64131

## Visual Studio setting in Unity 5.3
* https://docs.microsoft.com/en-us/visualstudio/cross-platform/using-visual-studio-tools-for-unity?view=vs-2017


## Panorimic View concept
* http://talesfromtherift.com/use-a-360-degree-panorama-as-a-skybox/

## Unity editor 
* how to use with generic list : https://answers.unity.com/questions/682932/using-generic-list-with-serializedproperty-inspect.html
* sample : https://gist.github.com/rutcreate/d550aa1ae4052e0a0b37
* guideline: https://www.linkedin.com/pulse/8-secrets-building-custom-unity-editors-charlie-silver/

