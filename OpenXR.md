### OpenXR
현재의 VR/AR/MR의 fragmentation을 해결하기 위한 표준 API


#### Fragmentation 해결
![image](https://user-images.githubusercontent.com/1837913/79086655-cf41d600-7d77-11ea-82e6-c28a66a79c6a.png)




#### 과연 잘 될까? 

* 참여 회사 

![image](https://user-images.githubusercontent.com/1837913/79086563-7bcf8800-7d77-11ea-9a3a-ccc1052672e8.png)

* 그룹에서 active한 표준

![image](https://user-images.githubusercontent.com/1837913/79086922-b685f000-7d78-11ea-91d1-6f97768c7b9c.png)

#### 링크
* OpenXR홈페이지 https://www.khronos.org/openxr/
   * header file: https://github.com/KhronosGroup/OpenXR-SDK/blob/master/include/openxr/openxr.h
* 소스코드: https://github.com/KhronosGroup/OpenXR-SDK



#### 실제 명확한 구현에 대한 이해가 안됨 (실제 진행은 되고 있는건지..)
그래서 다른 자료 Oculus Connect에 개발자가 발표했던 영상 찾아봄( 2019 9월)
* https://www.youtube.com/watch?v=QckZyZyvlsM

* 런터임을 고르는 방식
![image](https://user-images.githubusercontent.com/1837913/78954999-d7500a80-7b18-11ea-9381-afd4c5e0befd.png)

* 인풋을 핸들링 하는 방식 
![image](https://user-images.githubusercontent.com/1837913/78955053-08c8d600-7b19-11ea-8c94-44037543a9a1.png)

* openxr이 UE4.23에서는 정식으로 지원 된다고 함
https://youtu.be/QckZyZyvlsM?t=667



### OpenVR 
#### 링크들
* 깃헙: https://github.com/ValveSoftware/openvr
* 헤더API https://github.com/ValveSoftware/openvr/tree/master/headers
* Doc: https://github.com/ValveSoftware/openvr/wiki/API-Documentation

* Valve에서 만든 SteamVR을 사용하기 위한 API (표준 아님) https://www.steamvr.com/en/
  * 하지만 openxr과 유사. (정확히는 openvr의 usecase를 openxr이 많이 차용했을듯)
  
#### 언제 쓸 수 있을까?  
* 기기지원 (Vive같은 새로운 VR기기를 만들고, 이를 Steam게임과 연동 할때) (Driver API)
* VR어플리케이션 개발 (게임들) : Scene Application
* 다양한 설정을 지원하는 Overlay Application
     * 컨트롤러가 VR에서 기본으로 보이는데 이것들도 Overlay를 활용한 것
     * 우리가 활용하고 싶은 건 이 레이어 

#### Input handling방식
* openxr에서 제공하는 방식과 유사. (표준 X)
https://github.com/ValveSoftware/openvr/commit/60eb187801956ad277f1cae6680e3a410ee0873b
* 관련 문서: https://github.com/ValveSoftware/openvr/wiki/Input-Profiles

* SteamVR앱에서 steamapps\common\SteamVR\drivers\oculus\resources\input
![image](https://user-images.githubusercontent.com/1837913/78971162-ea2d0400-7b45-11ea-95c2-d0184a36fec8.png)


![image](https://user-images.githubusercontent.com/1837913/78955286-c8b62300-7b19-11ea-88ae-841a5affbf1d.png)


#### 살펴볼만한 example: OpenVr-Advanced Setting 
https://github.com/matzman666/OpenVR-AdvancedSettings

* 샤프론 (보호영역) 설정 변경
* 오디오 기기 설정 변경 등등등등

![image](https://user-images.githubusercontent.com/1837913/79091560-b857af80-7d88-11ea-87ff-d52d0cee8433.png)


#### Oculus에서 사용하려면.. 
* https://steamcommunity.com/sharedfiles/filedetails/?id=1590630273  근데 안되던데 ㅠ 


#### 데모 
* https://github.com/westside/openvr_sample



