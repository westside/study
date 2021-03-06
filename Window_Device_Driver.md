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


## WHQL 인증  
* 튜토리얼 링크: https://www.youtube.com/watch?v=3dIp_-adDQ4
* VeriSign인증서 필요 (EV인증서 - 확장유효성검사용)
* 대행
   * https://crosscert.com/
   * https://www.certkorea.co.kr/
* Extended Validation (EV) for Microsoft® 
  * https://www.websecurity.symantec.com/code-signing
  * 연에 대략 700불정도
  * 업로드할 때 프로그램이 필요: https://knowledge.digicert.com/generalinformation/INFO1982.html
  
* windows7 용으로 인증서를 받는게 나음 (보통은 호환성이 있기 때문에)   
* WHCK 는 Window 7, 8에 대한 인증
* WHLK는 Windows 10에 대한 인증에 해당  
  
1. 윈도우 대시보드 가입 
2. 등록 
  * https://partner.microsoft.com/ko-KR/dashboard/registration/hardware
  
* https://docs.microsoft.com/en-us/windows-hardware/test/hlk/getstarted/windows-hlk-getting-started

* http://blog.dramancompany.com/2015/12/%EC%B2%98%EC%9D%8C-windows-%EC%84%A4%EC%B9%98-%ED%8C%8C%EC%9D%BC%EC%9D%84-%EB%B0%B0%ED%8F%AC%ED%95%98%EB%8A%94-%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%93%A4%EC%9D%84-%EC%9C%84%ED%95%98%EC%97%AC/

## WINDBG 사용법 
* https://www.youtube.com/watch?v=2jM5obr3Shc
