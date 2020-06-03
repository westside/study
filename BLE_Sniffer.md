## 우선 nrfSniffer v1 (1.0.1)으로 함 (현재 Version2가 나옴)
* 스니퍼 링크 : https://www.nordicsemi.com/Software-and-Tools/Development-Tools/nRF-Sniffer/Download#infotabs
* 사용한 하드웨어: https://www.adafruit.com/product/2269
* 관련 가이드 문서: https://learn.adafruit.com/introducing-the-adafruit-bluefruit-le-sniffer/nordic-nrfsniffer
* wireshark는 1.12.1을 쓴다. : https://www.wireshark.org/download/win64/all-versions/
* 프레임간 시간 확인 방법: 
   * frame.time_delta > 0.03
   * https://osqa-ask.wireshark.org/questions/21101/how-to-view-all-frames-who-have-delay-for-more-than-or-less-than-5-ms
   
   
* 간단하게필요한건: sniffer: 1.0.1, driver(시리얼통신용), wireshark 1.12.1   



## Win as beacon
* 소스코드: https://github.com/huysentruitw/win-beacon

## 브로드캐스팅
* nrf 예제: https://github.com/NordicPlayground/nRF51-multi-role-conn-observer-advertiser
* 데이터 포맷: https://www.silabs.com/community/wireless/bluetooth/knowledge-base.entry.html/2017/02/10/bluetooth_advertisin-hGsf

* 기본 개념 정리 https://stackoverflow.com/questions/53342122/is-it-possible-to-send-data-with-ble-broadcast-mode
