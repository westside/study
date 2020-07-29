* https://deno.land/

### 특징: 3, 4, 5전쯤이 장점인데.. 이게 다른 불편함을 상쇄할만한 것인가  
* Secure by default. No file, network, or environment access, unless explicitly enabled.
* Supports TypeScript out of the box.
* Ships only a single executable file.
* Has built-in utilities like a dependency inspector (deno info) and a code formatter (deno fmt).
* Has a set of reviewed (audited) standard modules that are guaranteed to work with Deno: deno.land/std

### 아직은 모르겠다.
* 우선 Rust로 빌드를 한다고 하니 node와는 호환이 조금 다른 면들이 있는듯하다
* npm을 안쓴다.



### 데탑앱 만드는건 아닌듯, 아직
* electron이랑은 안된대.. 근데 다른 방법들이 있기는 함. 안정적일까? 


### 디노를 GCP에서 돌리기
* 도커로 도커라이징 해서 돌린다. 
* https://medium.com/google-cloud/deno-on-cloud-run-89ae64d1664d

### FIREBASE functions에서는 잘 안돌아갈듯? 
* https://github.com/denoland/deno/issues/3177


### REF
* 보일러플레이트: https://github.com/richg0ld/richg0ld-deno-boilerplate
* 보일러플레이트2: https://dev.to/lampewebdev/deno-the-node-replacement-bonus-i-created-a-boilerplate-for-deno-2g25
