# STUDY

<details>
<summary>Docker</summary>

- Docker?
  - Docker는 애플리케이션을 개발, 배포 및 실행하기 위한 플랫폼 및 도구 모음입니다.
  - 주요 목적은 소프트웨어를 컨테이너라고 불리는 표준화된 유닛 내에서 패키징
  - 코드가 일관된 환경에서 실행될 수 있도록 하는 것입니다.
- 특징
  - 컨테이너
    - Docker 컨테이너는 애플리케이션과 그 애플리케이션이 의존하는 라이브러리 및 기타 요소들을 함께 묶는 경령화된 실행 환경입니다.
    - 컨테이너는 각각 독립된 환경을 제공하기 때문에 다른 애플리케이션 또는 시스템 설정과 충돌없이 실행됩니다.
  - 이식성
      - Docker 컨테이너는 어디서나 동일하게 작동합니다, 개발자의 장비에서 작동하는 컨테이너는 클라우드나 서버 환경에서도 똑같이 작동합니다.
      - 이는 한 번 빌드하면, 어디서든 실행되는 이점을 제공합니다.
  - 경령화 및 빠른 시작
    - Docker 컨테이너는 가상머신보다 훨씬 가볍고 빠르게 시작됩니다.
    - Docker가 호스트 OS의 커널을 공유하고, 전체 운영체제를 가상화하지 않기 때문입니다.
  - Docker 이미지
    - Docker 컨테이너는 이미지에서 생성됩니다. 이 이미지는 애플리케이션의 실행에 필요한 모든 것을 포함하는 템플릿 역할을 합니다.
    - 이미지는 레이어로 구성되어 있으며, 이 레이어들은 읽기 전용입니다. 컨테이너가 시작되면, 이미지 위에 쓰기 가능한 레이어가 추가됩니다.
  - Docker Hub 및 레지스트리
    - Docker Hub는 공개적으로 사용할 수 있는 Docker 이미지들을 저장하는 중앙집중식 서비스입니다.
    - 사용자는 자신의 이미지를 Docker Hub에 업로드하거나 다른 사람이 만든 이미지를 다운로드할 수 있습니다.
  - 개발 및 배포 단순화
    - Docker는 개발부터 테스트, 그리고 프로덕션에 이르기까지 소프트웨어 배포의 복잡성을 줄여줍니다.

- Window 환경에서 설치
1. 요구사항 확인
   - Docker Desktop은 기본적으로 Hyper -V기능을 사용하기 때문에 Home을 제외한 Pro, Enterprise, Education에서 사용가능합니다.
   - 따라서 모든 버전에서 사용할 수 있도록 window에서 리눅스를 사용할 수 있도록 도와주는 WSL2를 활성화 해야합니다.
2. WSL2 설치 및 활성화
   - Docker는 리눅스를 기반으로 동작하기 때문에 윈도우 환경에서 리눅스를 사용할 수 있도록 도와주는 WSL2를 활성화 해야합니다.
   - 관리자 권한으로 Windows PowerShell 실행 후 명령어 입력
    ```
   # Windows SubSystem Linux를 활성화시키는 명령어
   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
   
    # VirtualMachinePlatform 기능을 활성화시키는 명령어 : WSL2 버전에 필요한 명령어
    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
    ```
   - microsoft Store에서 ubuntu 설치 후 실행
   - 다시 Windows PowerShell에서 wls 입력
3. Docker Desktop for windows 설치
   - https://docs.docker.com/desktop/setup/install/windows-install/
</details>

<details>
<summary>Http vs Socket</summary>

- Http
    - HyperText Transfer Protocol의 약자로 HTML 파일을 전송하는 프로토콜
    - 초기에는 HTML 파일을 전송하려는 목적으로 만들어졌으나 현재는 JSON, image 파일 등르 전송
    - 클라이언트에서 요청을 보내고 서버는 응답을 하는 형식으로 통신이 이루어진다.
      - 응답에는 클라이언트의 요청에 따른 결과를 반환한다.
      - 클라이언트의 요청이 있을 때만 서버가 응답하며, 단방향 통신이다.
    - 기본적으로 Http Protocol은 비연결성의 특징을 가지고 있으므로 실시간 통신을 하기에 적합하지 않다.
      - 옛날에 사용한 실시간 방식
        - Polling
          - 브라우저가 일정한 주기마다 서버에 HTTP 요청을 보내는 방식
          - 주기가 짧을수록 실시간성은 높아지지만 서버 및 네트워크 부하가 높아지는 trade-off가 발생한다.
          - ex) 실시간 야구 문자 중계는 10초 주기로 업데이트,페북 친구 리스트의 온라인 상태 확인, 약 1분 주기
          - ![img.png](img.png)
        - Long polling
          - polling 방식의 단점인 서버 부하를 줄이면서 실시간성을 높이기 위한 방식이다.
          - HTTP 요청이 서버로 들어올 때 Polling 방식과 달리 요청에 대한 응답을 보내고 연결을 바로 끊는 것(stateless 방식)이 아닌 일정시간 대기한다.
          - 대기 시간 중 데이터 업데이트(변경)이 일어났으면 바로 클라이언트에 응답을 보낸다. 응답을 받은 클라이언트는 바로 서버에 다시 요청을 보낸다.
          - ex) 웹 1:1 채팅, 10명 이하의 단체 채팅
          - ![img_1.png](img_1.png)
        - Streaming
          - 스트리밍 방식에서는 서버는 요청을 받으면 요청에 대한 응답을 완료하지 않은 상태에서 데이터를 계속 보내도록 한다.
          - 클라이언트는 응답을 받더라도 연결을 끊고 다시 요청을 보내는 과정없이 계속 응답을 받아 처리한다.
          - 서버는 무한정 혹은 일정 시간동안 요청을 대기시키고, chuncked 메시지를 이용하여 연결을 계속 유지하는 방식
          - ![img_2.png](img_2.png)
    - websocket 처럼 소켓을 사용하지만 7계층의 소켓을 사용
- Websocket
  - 하나의 TCP접속에 전이중 통신 채널을 제공하는 컴퓨터 통신 프로토콜이다.
  - 서버와 클라이언트 사이에 양방향 연결이 이루어
  - 클라이언트도 서버에게 요청을 보낼 수 있고, 서버도 클라이언트에게 요청을 보낼 수 있다.

</details>