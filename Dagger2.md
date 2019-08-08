### Dagger2는 DI 라이브러리 
* (Java기반/Android)

### 간단 용어 정리
* Dependency제공을 위한 것 @Module, @Provides
* Dependency 사용을 위한 것 @Inject 
* 둘간의 연결 @Component

### 우선 Module
* method로 의존성을 제공하는 클래스
* 각각의 method는 @Provide를 쓴다. 즉 모듈안에 여러개의 Provides가 들어가는거임
```java
@Module
public class CoffeeMakerModule {
    @Provides
    Heater provideHeater(){
        return new A_Heater();
    }

    @Provides
    Pump providePump(Heater heater){
        return new A_Pump(heater);
    }
}
```

### Component
```

```

### REFERENCE 
* https://jakewharton.com/dependency-injection-with-dagger-2/
* https://faith-developer.tistory.com/148
