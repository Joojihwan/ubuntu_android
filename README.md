# ubuntu_android
Make a App in Ubuntu with Android Studio (Ubuntu)


## 우분투 안드로이드 스튜디오 설치 과정 (약간의 에러를 해결하면서)
  **java sdk 설치 여부 확인 (java -version)**  
  미설치시 설치, 최초 9.0 설치 된것으로 확인됨

1. Ctrl + Alt + T 로 터미널 띄우기  

2. 안드로이드 스튜디오 설치 PPA 저장소 추가하기  
    ```
    sudo add-apt-repository ppa:maarten-fonville/android-studio  
    ```
    
3. apt 업데이트  
    ``` 
    sudo apt update  
    sudo apt-get update  
    ```
  
4. 안드로이드 스튜디오 설치  
    ```
    sudo apt-get install android-studio  
    ```
    4-1. 의존성 문제 생길 수 있음  
      해결법 : 
        cmd 창에서 제시하는 sudo apt-get -f install 시도  
        새로운 문제 발생 , 대충 openjdk-9-jdk 를 설치할 수 없음, openjdk-9-jdk-headless 에 이미 포함되어 덮어씌워야한다는 내용의 문제 발생  
        ```
        sudo apt-get -o Dpkg::Options::="--force-overwrite" install openjdk-9-jdk
        ```  
        위의 명령어로 강제로 덮어쓰기하며 설치  
        더 이상 문제가 발생하지 않았고 4번 명령어로 다시 설치하였음  

5. 안드로이드 스튜디오 최초 실행 (로컬 설치)  
  ```
  /opt/android-studio/bin/studio.sh
  ```
    
  5-1. 로컬 설치  
    -> 기본 설정을 아무것도 건드리지 않고 dark 모드만 설정

99. NNStreamer를 활용한 물체인식 자동 촬영 예제 어플
	```
	 - https://github.com/Joojihwan/nnstreamer-example/tree/master/android/example_app/nnstreamer-ssd-autocapture
	```

참고페이지  
    - https://coding-factory.tistory.com/503 (기본 설치과정 참고)  
    - https://askubuntu.com/questions/769467/can-not-install-openjdk-9-jdk-because-it-tries-to-overwrite-file-aready-includ (에러 해결 참고)

	

