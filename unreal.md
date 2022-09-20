### keywords for ue4 
* level editor 
   * sub level for collabration
* unreal dev grant  : https://www.unrealengine.com/en-US/unrealdevgrants
* material 
   * base color 
   * metalic : !!
   * specular
   * roughness : !!
* swarm agent : build farm for lightening
* reflection capture : https://docs.unrealengine.com/latest/INT/Resources/ContentExamples/Reflections/1_4/
* mesh paint : https://docs.unrealengine.com/latest/INT/Engine/UI/LevelEditor/Modes/MeshPaintMode/VertexColor/
* post process effect (https://docs.unrealengine.com/latest/INT/Engine/Rendering/PostProcessEffects/) !!
   * expose
   * blur - like lazer
* LUT Map (color correction like using photoshop) 
   * https://docs.unrealengine.com/latest/INT/Engine/Rendering/PostProcessEffects/ColorGrading/
* Exponential Height Fog : https://docs.unrealengine.com/latest/INT/Engine/Actors/FogEffects/HeightFog/
* Lightmass Importance Volume : https://docs.unrealengine.com/latest/INT/Engine/Rendering/LightingAndShadows/Lightmass/Basics/
   * indirect lightening cache
   *  light baking을 동적인 오브젝트에 넣을 때.. (시각화 탭..)
* asset migration, blueprint break point, nav mesh
* datasmith (https://www.unrealengine.com/en-US/beta) 
   * migration tool from 3ds max etc.
   
###  optimization
   * 액터 머징 (드로콜) 액터 병합
   * 쉐이더 복잡도 모드  - 빨간거면 무거운거.. 
   * 라이트 맵 해상도 
   * 컬디스턴스 
   * texture LOD bias..—  texture 파일 줄이는거
   
### 텍스쳐를 캐릭터가 아닌 머티리얼 위주로 개발 것이 더 좋음 (채널맵)

### VR
   * vray(https://www.fxguide.com/quicktakes/v-ray-in-ue4/) - vray is rendering tool
   * forward rendering is better in VR than deferred rendering 
   
### JNI- Andorid - https://github.com/Hydrafox/JarTuto
   

### 공부 
* pawn : https://docs.unrealengine.com/en-US/Gameplay/Framework/Pawn/index.html 


### Pluguin 관련 정리
* UPARAM
```
UCompositingElementOutput* CreateNewOutputPass(FName PassName, UPARAM(meta = (AllowAbstract = "false"))TSubclassOf<UCompositingElementOutput> OutputType);
```

* BlueprintNativeCodeGenUtils.cpp
```
UNiagaraScriptConversionContextInput* CreateScriptInputEnum
```


### UserDefinedEnum



## 레퍼런스
* UI관련 문서 정리가 잘되어 있는 곳 https://benui.ca/unreal/uproperty/
* 가이드 북: https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/string-conversions
