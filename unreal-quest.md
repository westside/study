### Unreal Integration: https://developer.oculus.com/downloads/package/unreal-engine-4-integration/

### 시작 설정
* https://developer.oculus.com/documentation/unreal/unreal-quick-start-guide-quest/#developing-applications-with-the-ue4-editor

### 나는 VR에서 이 이슈 있었는데 (Input 못찾는.. ) 해결 방법 아직 못찾음
* https://forums.unrealengine.com/development-discussion/blueprint-visual-scripting/1643057-lost-input-actions-and-input-axis-for-motion-controller-blueprint


## UE4.25부터 codeworks 버린듯. ndk버전이 낮아서 아래 링크 보고 ndk만 따로 우선 설정해서 해결 
https://www.unrealengine.com/en-US/tech-blog/updates-to-required-setup-for-android-ndk-21-in-unreal-engine-4-25


## Android에서 Launch로 할때 저런 에러들은 지우고 다시 깔면 해결
* UE폴더를 지워야 함 https://answers.unrealengine.com/questions/811194/android-manifest-bug-prevents-launching-on-device.html?sort=oldest
```
Attempt to construct staged filesystem reference from absolute path (/AndroidUI/setting/dark/setting_banner.uasset)
```
