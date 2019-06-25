## 톨리노 비전2 루팅하며 배운 것

1. [Android Platform Tools](https://developer.android.com/studio/releases/platform-tools?hl=ES#downloads) 설치

- adb: android debug bridge, Unix shell을 제공
- fastboot: 안드로이드 기기의 플래시 메모리에 직접 데이터를 쓰는 툴


2. Device Manager에 정상적으로 잡히고 톨리노 sd카드가 읽혀야 함 - 만약 잡히지 않으면 디바이스 매니저에서 장치 제거하고 윈도우 종료 후 재시작(전원 버튼 길게), 톨리노도 리부팅


3. 톨리노 종료 후 fastboot 모드 진입 (전원 버튼 + 라이트 버튼 함께 누름)

- 기기 연결 유무 확인

  ```
  $ fastboot devices
  ```
- adb가 열려있는 이미지로 부팅
  
  ```
  $ fastboot boot boot.img(adb가 열려있는 이미지)
  ```


4. adb 모드
- 기기 연결 유무 확인
    
    ```
    $ adb devices
    ```
- [Kingoroot](https://kingoapp.com)으로 루팅
- 필요한 앱 설치
  ```
  $ adb install [FILENAME].apk 
  ```
- 재부팅
  ```
  $ adb reboot
  ```

---
## 그밖에 유용한 명령어 

### fastboot 재부팅
시스템(ROM)으로 부팅
```
$ fastboot reboot
```
부트로더로 재부팅
```
$ fastboot reboot-bootloader
```
리커버리로 재부팅 (톨리노의 경우 전원+라이트+홈버튼 길게 눌러 부팅하는 것과 같은 모드)
```
$ fastboot reboot recovery
```

### fastboot 앱 인스톨 옵션
앱 설치
```
adb install [FILENAME].apk
```
설치된 앱 재설치(단 데이터 삭제는 불가)
```
adb install -r [FILENAME].apk
```
메모리카드에 설치
```
adb install -s [FILENAME].apk
```



