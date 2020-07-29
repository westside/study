## UI
* image management: https://github.com/bumptech/glide
* Material Drawer: https://github.com/mikepenz/MaterialDrawer
* Icons: https://github.com/mikepenz/Android-Iconics
* Animation with AA: https://github.com/airbnb/lottie-android



## Chart library
* Audio visualization: https://github.com/Yalantis/Horizon
* https://github.com/ABTSoftware/SciChart.Android.Examples

## Audio processing
* https://github.com/bewantbe/audio-analyzer-for-android
* https://github.com/paramsen/noise
* java audio processing: https://github.com/JorenSix/TarsosDSP
* https://github.com/gilpanal/FFTSpectralAnalyzer


## Android Visualizer 
* WaveInApp : https://github.com/Cleveroad/WaveInApp
* android-audio-visualizer : https://github.com/GautamChibde/android-audio-visualizer
* audio-visualizer-android : https://github.com/gauravk95/audio-visualizer-android

### Visualizer 한계점
* fft bin size 1024가 맥스임 (s6, s7에서 테스트) 
* galaxy s6기준으로 0.1 마다 한번씩 데이터가 들어옴 (Visualize이외의 프로세싱으로 쓰기에는 불충분)

## Music Player  참고 앱
* 뮤직 DNA : https://github.com/harjot-oberai/MusicDNA

## MediaPlayer with decoder 
* https://github.com/drcarter/AudioStreamPlayer/tree/master/AudioStreamPlayer
* 관련 링크: https://drcarter.tistory.com/162
* https://github.com/Cookizz/AudioTrackMp3Player
* MediaExtractor: https://developer.android.com/reference/android/media/MediaExtractor


## Android Media API관련 : 오디오 처리
### [MediaCodec](https://developer.android.com/reference/android/media/MediaCodec)
![image](https://user-images.githubusercontent.com/1837913/62116040-77039a80-b2f4-11e9-85ad-7ed501bcac73.png)
* 코덱은 인풋과 아웃풋이 있고, 인풋에 MediaExtractor를, 아웃풋을 AudioTrack과 연결 시키면 된다.
* Surface는 비디오 포맷에서 사용

### [MediaExtractor](https://developer.android.com/reference/android/media/MediaExtractor)






