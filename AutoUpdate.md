# AUTO 업데이트 관련 라이브러리들 정리

### Squirrel
* https://github.com/Squirrel/Squirrel.Windows: 
* 가장 많이 쓰이기는 하는데 커스텀 하기 조금 곤란, 그런데 installer같은 형식이 아니고 알아서 깔리는 형태이기 때문에 선호하는듯

### 클릭원스(ClickOnce) 
* 윈도우가 제공하는 기본 툴
* https://docs.microsoft.com/en-us/visualstudio/deployment/publishing-clickonce-applications?view=vs-2015&redirectedfrom=MSDN
* 커스텀 하려면 이쪽을 봐야할듯: https://docs.microsoft.com/en-us/dotnet/api/system.deployment.application?view=netframework-4.8

* 튜토리얼: https://www.youtube.com/watch?v=W8Qu4qMJyh4
* 디플로이 방법이 제한적인데, 이걸 내가 모르는거겠지.. 

### Onova
* https://github.com/Tyrrrz/Onova
* 개발자가 코딩을 깔끔하게 잘하네
* 업데이트 툴킷 라이브러리의 느낌 (필요한 함수들이랑 인터페이스 정의를 잘해둠) 
* 근데 base가 net core 3라서 쓰는게 맞나 싶.

### AutoUpdater.NET 
* https://github.com/ravibpatel/AutoUpdater.NET
* 걍 무난.


### https://github.com/dbforge/nUpdate 
* 괜찮아 보였으나.. 이건 안쓰는게 나을듯. 
