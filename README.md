# Hyperledger Indy Agent 설명

🎈 https://github.com/swcurran/education/tree/master/LFS171x

이 폴더에는 기본 Hyperledger Indy Agent의 데모가 포함되어 있습니다. 에이전트는 웹 브라우저 인터페이스를 제공하여 에이전트 간의 관계 설정, 검증 가능한 자격 증명 발급 및 검증 가능한 자격 증명의 클레임을 증명합니다.

> **이 데모는 새로운 구현의 기초로 사용하거나 에이전트 구현을 위한 참조로 사용해서는 _NOT_ 일부 초기 Indy 에이전트 코드를 기반으로 합니다. 이 데모가 개발된 이후로 Indy(및 Aries) 커뮤니티는 에이전트의 개념을 크게 발전시켰고 이 코드 기반은 버려졌습니다. 에이전트가 피상적인 수준에서 작동하는 방식을 이해하는 데 여전히 좋은 데모입니다 -- 자격 증명을 연결하고 교환하는 에이전트의 개념. 그러나 최신 Indy/Aries 코드를 기반으로 구축하는 데 관심이 있는 경우, [Aries project](https://github.com/hyperledger/aries), [Aries Cloud Agent - Python](https://github.com/hyperledger/aries-cloudagent-python) 및 기타 상호 운용 가능한 구성 요소를 살펴봐야 합니다. 개발자(또는 지망생)인 경우 이 [Becoming an Indy/Aries Developer](https://github.com/hyperledger/aries-cloudagent-python/tree/master/docs/GettingStartedAriesDev) 가이드를 확인하세요.**

Hyperledger Indy에 대해 더 배우고 싶으면, 이 프로젝트를 참고하세요 ! - https://wiki.hyperledger.org/display/indy.

이 데모는 Hyperledger 프로젝트의 EdX를 사용하는 사람들을 위한 연습으로 사용됩니다. [Blockchain for Business](https://www.edx.org/course/blockchain-business-introduction-linuxfoundationx-lfs171x-0) 과정이다.

너가 데모를 시작할때, 이것은 **[Agent Demo Script](AgentDemoScript.md)** Alice가 Hyperledger Indy를 사용하여 Faber College에서 성적표를 받은 다음 이를 사용하여 Acme Corp에 지원하는 시나리오를 안내합니다.

데모의 간단한 비디오 화면 녹화를 보기 위해서 [클릭하세요.](https://youtu.be/9WZxlrGMA3s).

## Credits

이 데모의 코드는 처음에 Spencer Holman 그리고 Brigham Young University에 있는 Matthew Hailstone에 의해 쓰여졌습니다. Carol Howard 이 문서의 설명을 만들었습니다.

## 너의 Browser 또는 Local Machine에 작동시키기

이 데모는 브라우저만 사용하여 터미널에서 실행할 수 있습니다 , 또는 기술적인 경향이 있는 경우, 너는 너의 local machine에서 작동 시킬 수 있습니다. 다음 섹션에서 데모를 실행하려는 방법에 따라 `In Browser` 그리고 `Local Machine`에 대한 하위 섹션이 있습니다.

## Prerequisites(전제조건)

### 브라우저 내

전제조건은 [Docker Hub](https://hub.docker.com)계정을 사용한는 조건입니다. 도커 허브는 [Docker](https://docker.com)생태계에서 '플레이 스토어'같은 존재입니다.

### Local Machine

로컬 머신에서 이 Indy Agent 데모를 실행하기 위해서는 다음이 설치되어 있어야 합니다!

- 도커, (Docker Compose를 포함한) - Community Edition도 괜찮습니다.
  - 만약 도커가 설치되어 있지 않은 경우, [this link](https://docs.docker.com/install/#supported-platforms) 여기 링크를 통해 플랫폼을 설치합니다!
  - 다양한 도커 컴포지트를 설치하는 방법은 여기를 참고하세요! [here](https://docs.docker.com/compose/install/).
- git
  - [This link](https://www.linode.com/docs/development/version-control/how-to-install-git-on-linux-mac-and-windows/) 해당 링크에서는 MAC, Linux 그리고 virtualBox를 사용하여 Linux를 싱행하는 경우를 포함해서 설치 방법을 제공합니다.

## Installing the Demonstration

### 브라우저 내

[Play with Docker](https://labs.play-with-docker.com/)로 이동합니다. 그리고 필요하다면 로그인을 진행합니다. 해당 사이트는 Docker에 대해 학습하는 개발자를 위해 운영되는 사이트 입니다.

> 만약 `Play with Docker` 환경에 대해 배우고 싶다면, [About](https://training.play-with-docker.com/about/) 여기를 참고하세요! [Training Site](https://training.play-with-docker.com)는 Docker Labs의 연습 사이트 입니다.

시작 버튼을 클릭하여 데모 실행에 사용할 수 있는 도커 샌드박스를 시작합니다. 그리고 +ADD an Ianstance 링크를 클릭하여 브라우저에서 터미널을 시작하고 다음 명령어를 실핼합니다:

- `git clone https://github.com/hyperledger/education`

> **Tip**: 터미털에서 붙여넣을 떄 마우스 오른쪽 클릭을 한 뒤 `paste`를 눌러주세요!

- 다음 명령어를 실행하여 코드 위치로 이동합니다:
  - `cd education/LFS171x/indy-material/nodejs`

### Local Machine

로컬 머신에 데모를 설치하려면 EdX Blockchain for Business의 git 저장소를 clone해야 합니다:

- 윈도우 터미널을 열어 실행 전 환경을 세팅환경을 확인합니다:
  - Run `git --version`, `git version 2.17.1`인지 확인합니다.
  - Run `docker --version`, `Docker version 18.06.1-ce, build e68fc7a`인지 확인합니다.
  - Run `docker-compose --version`, `docker-compose version 1.22.0, build f46880fe`인지 확인합니다.
  - 버전은 위 버전보다 같거나 크면 상관 없습니다.
- 터미널을 열어 소스코드를 설치할 경로로 이동합니다.
- Run the command: `git clone https://github.com/hyperledger/education/`
  - 위 코드를 실행하면 소스코드가 정상적으로 시시템에 저장됩니다.
- 다음 명령어를 통해 코드 위치로 이동합니다:
  - `cd education/LFS171x/indy-material/nodejs`

## Starting the Demonstration

<!-- The steps for runnning the demonstration are similar for the `In Browser` and `Local Machine` scenarios: -->

데모를 실행시키기 위한 단계는 `브라우저 환경`에서의 데모와 `로컬 환경`에서의 데모 모두 동일합니다:

<!-- - Run the command `./manage build` to build the components of the software -->

- `./manage build` 명령어를 통해 컴포넌트들을 빌드할 수 있습니다.
<!-- - Run the command `./manage up` to run the components -->
- `./manage up` 명령어를 통해 컴포넌트들을 실행시킬 수 있습니다.

<!-- It takes a while for the demo to start - lots of things are happening. The logs for all of the containers will display in the terminal window. Logs show the output of both the Blockchain Ledger nodes communicating, and the Indy Agents starting up and communicating with the Ledger. -->

데모를 시작하는 데에는 조금 시간이 걸릴 수도 있습니다 - 엄청나게 많은 일들이 일어나고 있거든요. 모든 컨테이너들의 로그가 터미널 콘솔창에 출력될 것입니다. 로그에는 블록체인 레저 노드 양쪽이 소통하는 과정과, 인디 에이전트들이 실행되고 블록체인 레저와 소통하는 과정이 출력될 것입니다.

<!-- Things to watch for as the demo starts up: -->

데모가 시작될때 눈여겨봐야할 점들은 이것들입니다:

<!-- * You should periodically see things like "Listening on port 3001", which indicates an Agent is up and running. -->

- "Listening on port 3001" 과 같은 문구들이 자주 보일 것입니다. 이것은 인디 에이전트들이 활성화되어 실행되고 있다는 뜻입니다.
<!-- * You should **not** see a stack trace error in the code - that would indicate a problem. -->
- 에러가 뜬다면 이것은 문제가 있다는 뜻이기 때문에 에러들은 보여서는 **안됩니다**.
<!-- * You should **not** see any "Container exiting" messages, indicating containers not starting up properly. -->
- "Container exiting" 과 같은 문구 또한 보여서는 **안됩니다**. 이것은 컨테이너들이 제대로 실행되지 않았다는 것을 뜻하기 때문입니다.
<!-- * There should be 10 docker containers running. You can hit `ctrl-c` to exit the log viewer and run the command `docker ps` to see all of the containers running. Run `./manage logs` if you want to see the logs again. -->
- 이 데모에는 10개의 컨테이너가 작동되어야만 합니다. `ctrl-c` 를 눌러 로그 출력창을 종료한 후 `docker ps` 명령어를 통해 실행되고 있는 컨테이너들을 볼 수 있습니다. 다시 로그 출력창을 보길 원한다면, `./manage logs` 명령어를 입력하면 됩니다.
<!-- * Once the output slows significantly and you only see messages from the nodes (the containers running the ledger), everything should be working. -->
- 로그가 출력되는 속도가 현저히 느려지고 노드 (블록체인 레저를 구동시키는 컨테이너들) 들이 출력하는 메시지들만이 보인다면, 모든 것이 완벽하게 작동하여야만 합니다.

<!-- ### Access the ledger and agents in a web browser: -->

### 웹 브라우저를 통해 블록체인 레저와 인디 에이전트들에게 접근하기:

<!-- ### In Browser -->

### 브라우저 환경에서 데모를 진행하는 경우

<!-- As the demo starts up, a series of 4 digit numbers will appear above the terminal. Those are the exposed ports of the running containers and the numbers are links to start a Browser tab accessing that port. -->

데모가 시작되고 난 뒤에는, 터미널 콘솔창에 4자리의 숫자들이 보일 것입니다. 이것들은 작동중인 컨테이너들이 외부로 공개시켜놓은 포트들이고 각각의 숫자들은 해당 포트에 접근할 수 있는 브라우저 탭을 여는 링크입니다.

<!-- To go through the demonstration, click the following numbers from the list: -->

데모를 진행하기 위해, 목록에서 다음의 번호들을 클릭하세요:

<!-- * **3000** for Alice -->

- **3000** 번은 'Alice' 입니다.
<!-- * **3002** for Faber College -->
- **3002** 번은 'Faber College' 입니다.
<!-- * **3003** for Acme Corporation -->
- **3003** 번은 'Acme Corporation' 입니다.

<!-- If you click the links before the Agent is active, you might get a `Connection reset by peer` error messages. Monitor the logs and wait longer and then try again. -->

인디 에이전트가 활성화되기 전에 링크를 누른다면, 아마 `Connection reset by peer` 라는 에러가 뜰 것입니다. 로그 출력창을 확인하면서 조금 더 기다려 본 뒤 다시 시도해 보세요.

<!-- The instructions for walking through the demonstration script are here: **[Agent Demo Script](AgentDemoScript.md)** -->

데모를 따라하기 위한 가이드는 여기에 있습니다: **[Agent Demo Script](AgentDemoScript.md)**

<!-- You can also open in a browser a Blockchain Ledger Explorer: -->

블록체인 레저 탐색기 또한 브라우저 상에서 열 수 있습니다:

- **9000**

<!-- Although we don't talk about them in the demo overview, there are two additional Agents running that you can access: -->

데모 오버뷰에서는 다루지 않겠지만, 접근할 수 있는 인디 에이전트는 두개 더 있습니다:

<!-- * **3001** for Bob. -->

- **3001** 번은 'Bob' 입니다.
<!-- * **3004** for Thrift Bank. -->
- **3004** 번은 'Thrift Bank' 입니다.

<!-- > The remainder of the numbers (ports - 9701-9708) are the ports to the Blockchain Ledger nodes - two per node. -->

> 남은 번호들 (9701 ~ 9708 번) 은 블록체인 레저 노드들을 위한 포트입니다 - 노드 하나당 두개씩의 포트가 할당되어 있습니다.

<!-- ## Local Machine -->

### 로컬 환경에서 데모를 진행하는 경우

<!-- To go through the demonstration, open the following links in new browser tabs: -->

데모를 진행하기 위해 브라우저 탭에서 다음의 링크들을 여세요.

<!-- * [http://localhost:3000](http://localhost:3000) for Alice -->

- [http://localhost:3000](http://localhost:3000) 는 'Alice' 를 위한 것입니다.
<!-- * [http://localhost:3002](http://localhost:3002) for Faber College -->
- [http://localhost:3002](http://localhost:3002) 는 'Faber College' 를 위한 것입니다.
<!-- * [http://localhost:3003](http://localhost:3003) for Acme Corporation -->
- [http://localhost:3003](http://localhost:3003) 는 'Acme Corporation' 를 위한 것입니다.

<!-- If you click the links before the Agent is active, you might get a `Connection reset by peer` error messages. Monitor the logs and wait longer and then try again. -->

인디 에이전트가 활성화되기 전에 링크를 누른다면, 아마 `Connection reset by peer` 라는 에러가 뜰 것입니다. 로그 출력창을 확인하면서 조금 더 기다려 본 뒤 다시 시도해 보세요.

<!-- The instructions for walking through the demonstration script are here: **[Agent Demo Script](AgentDemoScript.md)** -->

데모를 따라하기 위한 가이드는 여기에 있습니다: **[Agent Demo Script](AgentDemoScript.md)**

<!-- You can also open in a browser a Ledger Explorer: -->

블록체인 레저 탐색기 또한 브라우저 상에서 열 수 있습니다:

- [http://localhost:9000](http://localhost:9000)

<!-- Although we don't talk about them in the demo overview, there are two additional Agents running that you can access: -->

데모 오버뷰에서는 다루지 않겠지만, 접근할 수 있는 인디 에이전트는 두개 더 있습니다:

<!-- * [http://localhost:3001](http://localhost:3001) for Bob -->

- [http://localhost:3001](http://localhost:3001) 은 'Bob' 을 위한 것입니다.
<!-- * [http://localhost:3004](http://localhost:3004) for Thrift Bank -->
- [http://localhost:3004](http://localhost:3004) 은 'Thrift Bank' 을 위한 것입니다.

<!-- ## Stopping the Demo -->

## 데모 그만 하기

<!-- ### In Browser -->

### 브라우저 환경에서 데모를 진행하는 경우

<!-- To stop the demo, go to the browser tab where you ran `docker-compose up` and close the browser tab. Note that if you don't close the tab, the terminal session will expire 4 hours after you started it. -->

데모를 그만하기 위해서는, `docker-compose up` 명령어를 입력했던 브라우저 탭을 닫으세요. 만일 브라우저 탭을 닫지 않는다면, 터미널 세션은 시작된지 4시간 뒤에 만료된다는 것을 기억하세요.

<!-- ### Local Machine -->

### 로컬 환경에서 데모를 진행하는 경우

<!-- To stop the demo, go to the terminal window where you ran `docker-compose up`. If the logs are scrolling and/or you are not at the command prompt, hit `Ctrl-C`. Run the command `./manage down`.  You should see a `Done` message as each of the 10 containers stops.  Run the command `docker ps` to see that the containers have stopped. -->

데모를 그만하기 위해서는, `docker-compose up` 명령어를 입력했던 터미널 창으로 가세요. 로그가 계속 출력되고 있거나 명령 입력창이 보이지 않는 경우에는, `ctrl-c` 를 누르세요. 그 다음에는 `./manage down` 명령어를 입력하세요. 1개의 컨테이너가 종료될 때마다 `Done` 이라는 메세지가 보여야만 하고, 총 10개의 컨테이너가 종료될 것입니다. `docker ps` 명령어를 입력하여 모든 컨테이너들이 종료되었는지 확인하세요.

<!-- # Trouble Shooting -->

# 문제 해결하기

<!-- > As issues are discovered by users of this demo, we'll add more troubleshooting instructions here. -->

> 이 데모의 문제가 유저들에 의해 밝혀질 때마다, 저희는 이곳에 문제 해결 방법을 계속 추가할 것 입니다.

<!-- * The "validate" of the Government ID Credential for each of the Identities is often failing - displaying a large red "X". We're still investigating why that is happening in some cases but not others. -->

- 개개인의 정부 ID 증명을 검증하는 것은 이따금씩 실패합니다 - 커다랗고 빨간 X 표시를 출력하면서 말이죠. 저희는 왜 어떤 경우에는 되고 어떤 경우에는 되지 않는지 계속 조사중입니다.
