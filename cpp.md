### STATIC VS SHARED
* Shared Library File Extensions:
  * Windows: .dll
  * Mac OS X: .dylib
  * Linux: .so

* Static Library File Extensions:
  * Windows: .lib
  * Mac OS X: .a
  * Linux: .a
  
* about visibility: http://gcc.gnu.org/wiki/Visibility
* generate shared file: http://gernotklingler.com/blog/creating-using-shared-libraries-different-compilers-different-operating-systems/
  
## CPP LIBS
* https://en.cppreference.com/w/cpp/links/libs
* websocket: https://github.com/zaphoyd/websocketpp

### CMAKE 
* https://cmake.org/cmake-tutorial/
* Start Point: https://cgold.readthedocs.io/en/latest/overview.html
* Good toturial: https://tuannguyen68.gitbooks.io/learning-cmake-a-beginner-s-guide/content/chap1/chap1.html
* tutorial from clion: https://www.jetbrains.com/help/clion/quick-cmake-tutorial.html
* reddit: https://www.reddit.com/r/cpp/comments/7sr4h1/cross_platform_c_library_android_ios_windows/
* 한글 문서
   * https://gist.github.com/luncliff/6e2d4eb7ca29a0afd5b592f72b80cb5c
   * https://www.tuwlab.com/27270
* cross-platform-cmake: https://atomheartother.github.io/c++/2018/07/12/CPPDynLib.html
   * cmake toolchain 잘 모아놓음: https://github.com/ruslo/polly
   * cpp를 다른 언어로 변환 약간 Mac전용 느낌: https://github.com/dropbox/djinni  
* other projects based on cmake
   * opencv : https://github.com/opencv/opencv
   * libsourcery (network lib): https://github.com/sourcey/libsourcey
* bast practice
```
// Be careful to be overwritten
set(VARIABLE "${VARIABLE} Flag1 Flag2")


// MAKE ERROR
if(Boost_FOUND)
    message("Boost Found")
else()
    error("Boost Not Found")
endif()

```


### IL2CPP
* https://blogs.unity3d.com/kr/2015/09/22/kr-csharp-compile-il2cpp/
* openvr wrapping example: https://github.com/ValveSoftware/openvr/blob/master/headers/openvr_api.cs


### CPP to CSharp
* Object creation example: https://tansanc.tistory.com/526
* user lib file: managed wrapper만드는 방법: http://tom-shelton.net/index.php/2008/12/11/creating-a-managed-wrapper-for-a-lib-file/


### TROUBLE SHOOTING
* NMAKE: fatal error u1073: Dont know how to make (WIN)
   * https://stackoverflow.com/questions/1941443/cmake-linking-against-shared-library-on-windows-error-about-not-finding-lib-fi
   * when there is no dllexport


### REF
* CPP project template for clion: https://github.com/TimothyHelton/cpp_project_template
* How to setup project in clion: https://medium.com/@TimothyHelton/c-projects-with-cmake-google-test-and-doxygen-using-clion-d508f6f4ad05
* https://medium.com/@onur.dundar1/cmake-tutorial-585dd180109b
* https://libsora.so/posts/csharp-cpp-dll/
* https://www.codementor.io/a_hathon/building-and-using-dlls-in-c-d7rrd4caz
* https://github.com/3F/DllExport
