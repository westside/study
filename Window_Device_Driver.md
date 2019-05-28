## 개발 환경 셋업
### 깔기 https://docs.microsoft.com/ko-kr/windows-hardware/drivers/download-the-wdk
* Step 1: Install Visual Studio
* Step 2: Install WDK for Windows 10, version 1903
* step3 : EWDK (Enterprise WDK) 설치 - visual studio 없어도 됨 , 나는 안깔아도 되겠구나. 
    * 디바이스 드라이버 납품해서 빌드하려고 할때 (개발환경 없이 가능함)
    * https://github.com/microsoft/Windows-driver-samples 이거 하려면 필요한듯 
### WDK 7600 (도움말 + 샘플 보기 위해서 설치하는듯) 
* 샘플 + 도움말만 설치


### 설치 파일 예제
* https://github.com/birdstargit/windows_driver_inf


### WDK 7600에서 샘플을 WDK10으로 가져오기 
* WDM프로젝트로 만들기
* inf 파일 복사: https://github.com/birdstargit/windows_driver_inf

* 소스 복사 (헤더파일 없으면 sources 파일을 보면 된다)


* https://www.youtube.com/watch?v=kBzk4KyM7LA

### TIP (프로젝트 속성)
* INF2CAT -> UseLocalTime: yes로 
* 하위 os로 동작 시키려면? DriverSettings에 Target OS버전을 바꾸면 됨

### 디버깅 
* https://www.youtube.com/watch?v=MFJ2LeZjxEE


## 레퍼런스
### Tutorials 
* official: https://docs.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/writing-a-very-small-kmdf--driver
* https://github.com/Microsoft/Windows-driver-samples/tree/master/audio/sysvad
* https://www.youtube.com/watch?v=D9NncWmVDz0
   * https://www.youtube.com/watch?v=kBzk4KyM7LA

* https://woounnan.tistory.com/1
* https://seolis.tistory.com/entry/%EC%9C%88%EB%8F%84%EC%9A%B0%EC%A6%88-%EB%94%94%EB%B0%94%EC%9D%B4%EC%8A%A4-%EB%93%9C%EB%9D%BC%EC%9D%B4%EB%B2%84-%EA%B0%9C%EB%B0%9C-%EB%B0%A9%EB%B2%95-%ED%8E%8C
