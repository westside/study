### 기사 정리 (Unity의 경우)

* Rift에서 쓰던 에셋을 그냥 Unity 기본 세팅대로 쓰면 된다 (근데 못미더움) 
* 걍 quality를 high나 midium으로 놓고 최적화 시작해라 

* 그냥 texture가 blurry하게 보였는데, GPU native 포맷 이미지 (RGBA 32-bit 같은) 썼더니 해결 되더라  
* 폴리곤 줄이는거보다는 object갯수 줄이는게 효과적이다 (drawcall)

* UI Sprite썼는데 텍스쳐 최대한 재사용하고 이미지는 512보다 같거나 작게 - 다만 가까이서 깨지는 거 막기 위해서 Mipmapping은 끔
* 하지만 다른 texture의 경우에는 mipmapping 켬

* 꼭 필요한거 빼고는 light baking해라 


### REF
* https://uploadvr.com/quest-optimization-share/
* 밉맵: https://ko.wikipedia.org/wiki/%EB%B0%89%EB%A7%B5
* unity mipmapping: https://ozlael.tistory.com/45

