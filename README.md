# Hyperledger Indy Agent Demonstration

This folder contains a demonstration of basic Hyperledger Indy Agents. The agents provide a web browser interface to show establishing relationships between agents, issuing Verifiable Credentials, and proving claims from Verifiable Credentials.

> **This demonstration is based on some early Indy Agent code that should *NOT* be used as the basis of new implementations or as a reference for implementing an agent. Since  this demonstration was developed the Indy (and Aries) community has evolved the notion of Agents significantly and this code base has been abandoned. It is still a good demo for understanding how agents work on a superficial level -- the concepts of agents connecting and exchanging credentials. However, if you are interested in building on the latest Indy/Aries code, you should look at the [Aries project](https://github.com/hyperledger/aries), the [Aries Cloud Agent - Python](https://github.com/hyperledger/aries-cloudagent-python) and other interoperable components. If you are a developer (or wannabe), check out this [Becoming an Indy/Aries Developer](https://github.com/hyperledger/aries-cloudagent-python/tree/master/docs/GettingStartedAriesDev) guide.**

To learn more about Hyperledger Indy, see the project wiki - https://wiki.hyperledger.org/display/indy.

This demo is used as an exercise for those taking the Hyperledger Project's EdX  [Blockchain for Business](https://www.edx.org/course/blockchain-business-introduction-linuxfoundationx-lfs171x-0) course.

Once you have the demo started, this **[Agent Demo Script](AgentDemoScript.md)** guides you through the scenario of Alice using Hyperledger Indy to get her transcripts from Faber College and then using them to apply for a job with Acme Corp.

[Click here](https://youtu.be/9WZxlrGMA3s) to view a short screencast of the demo.

## Credits

The code for this demonstration was initially written by Spencer Holman and Matthew Hailstone of Brigham Young University. Carol Howard created the documentation for the demonstration.

## Running in your Browser or on Local Machine

This demo can be run in a terminal using just a browser , or if you are more technically inclined, you can run it on your local machine. In the following sections, there is a sub-section for `In Browser` and `Local Machine`, depending on how you want to run the demo.

## Prerequisites

### In Browser

The only prequisite (other than a browser) is an account with [Docker Hub](https://hub.docker.com). Docker Hub is the "Play Store" for the [Docker](https://docker.com) ecosystem.

### Local Machine

To run this Indy Agent demonstration on your local machine, you must have the following installed:

* Docker, including Docker Compose - Community Edition is fine.
  * If you do not already have Docker installed, open [this link](https://docs.docker.com/install/#supported-platforms) and then click the link for the installation instructions for your platform.
  * Instructions for installing docker-compose for a variety of platforms can be found [here](https://docs.docker.com/compose/install/).
* git
  * [This link](https://www.linode.com/docs/development/version-control/how-to-install-git-on-linux-mac-and-windows/) provides installation instructions for Mac, Linux (including if you are running Linux using VirtualBox) and native Windows (without VirtualBox).

## Installing the Demonstration

### In Browser

Go to the [Play with Docker](https://labs.play-with-docker.com/) and (if necessary) login. This site is operated by Docker to support developers learning about Docker.

> If you want to learn more about the `Play with Docker` environment, look at the [About](https://training.play-with-docker.com/about/) and the Docker related tutorials at the Docker Labs [Training Site](https://training.play-with-docker.com).

Click the "Start" button to start a Docker sandbox you can use to run the demo, and then click the `+Add an Instance` link to start a terminal in your browser. Within the browser, run the following command:

- `git clone https://github.com/hyperledger/education`

> **Tip**: To paste text in the terminal window, right-click on the window and choose `paste`

- Navigate to the location of the code by running the command:
  - `cd education/LFS171x/indy-material/nodejs`

### Local Machine

To install the demonstration on your local machine you need to clone the git repository for the EdX Blockchain for Business course. To do that:

* Install the prerequisites listed above and make sure they are functioning on your system. To verify, open a terminal window and:
    * Run `git --version`, which should return something like: `git version 2.17.1`
    * Run `docker --version`, which should return something like: `Docker version 18.06.1-ce, build e68fc7a`
    * Run `docker-compose --version`, which should return something like: `docker-compose version 1.22.0, build f46880fe`
    * Your version numbers should be the same or higher.
* Open a terminal session and navigate to where you want to install the source code.
* Run the command: `git clone https://github.com/hyperledger/education/`
  * That will download the repository containing the source code onto your system.
* Navigate to the location of the code by running the command:
  * `cd education/LFS171x/indy-material/nodejs`

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
* "Listening on port 3001" 과 같은 문구들이 자주 보일 것입니다. 이것은 인디 에이전트들이 활성화되어 실행되고 있다는 뜻입니다.
<!-- * You should **not** see a stack trace error in the code - that would indicate a problem. -->
* 에러가 뜬다면 이것은 문제가 있다는 뜻이기 때문에 에러들은 보여서는 **안됩니다**.
<!-- * You should **not** see any "Container exiting" messages, indicating containers not starting up properly. -->
* "Container exiting" 과 같은 문구 또한 보여서는 **안됩니다**. 이것은 컨테이너들이 제대로 실행되지 않았다는 것을 뜻하기 때문입니다.
<!-- * There should be 10 docker containers running. You can hit `ctrl-c` to exit the log viewer and run the command `docker ps` to see all of the containers running. Run `./manage logs` if you want to see the logs again. -->
* 이 데모에는 10개의 컨테이너가 작동되어야만 합니다. `ctrl-c` 를 눌러 로그 출력창을 종료한 후 `docker ps` 명령어를 통해 실행되고 있는 컨테이너들을 볼 수 있습니다. 다시 로그 출력창을 보길 원한다면, `./manage logs` 명령어를 입력하면 됩니다.
<!-- * Once the output slows significantly and you only see messages from the nodes (the containers running the ledger), everything should be working. -->
* 로그가 출력되는 속도가 현저히 느려지고 노드 (블록체인 레저를 구동시키는 컨테이너들) 들이 출력하는 메시지들만이 보인다면, 모든 것이 완벽하게 작동하여야만 합니다.

<!-- ### Access the ledger and agents in a web browser: -->
### 웹 브라우저를 통해 블록체인 레저와 인디 에이전트들에게 접근하기:

<!-- ### In Browser -->
### 브라우저 환경에서 데모를 진행하는 경우

<!-- As the demo starts up, a series of 4 digit numbers will appear above the terminal. Those are the exposed ports of the running containers and the numbers are links to start a Browser tab accessing that port. -->
데모가 시작되고 난 뒤에는, 터미널 콘솔창에 4자리의 숫자들이 보일 것입니다. 이것들은 작동중인 컨테이너들이 외부로 공개시켜놓은 포트들이고 각각의 숫자들은 해당 포트에 접근할 수 있는 브라우저 탭을 여는 링크입니다.

<!-- To go through the demonstration, click the following numbers from the list: -->
데모를 진행하기 위해, 목록에서 다음의 번호들을 클릭하세요:

<!-- * **3000** for Alice -->
* **3000** 번은 'Alice' 입니다.
<!-- * **3002** for Faber College -->
* **3002** 번은 'Faber College' 입니다.
<!-- * **3003** for Acme Corporation -->
* **3003** 번은 'Acme Corporation' 입니다.

<!-- If you click the links before the Agent is active, you might get a `Connection reset by peer` error messages. Monitor the logs and wait longer and then try again. -->
인디 에이전트가 활성화되기 전에 링크를 누른다면, 아마 `Connection reset by peer` 라는 에러가 뜰 것입니다. 로그 출력창을 확인하면서 조금 더 기다려 본 뒤 다시 시도해 보세요.

<!-- The instructions for walking through the demonstration script are here: **[Agent Demo Script](AgentDemoScript.md)** -->
데모를 따라하기 위한 가이드는 여기에 있습니다: **[Agent Demo Script](AgentDemoScript.md)**

<!-- You can also open in a browser a Blockchain Ledger Explorer: -->
블록체인 레저 탐색기 또한 브라우저 상에서 열 수 있습니다:
* **9000**

<!-- Although we don't talk about them in the demo overview, there are two additional Agents running that you can access: -->
데모 오버뷰에서는 다루지 않겠지만, 접근할 수 있는 인디 에이전트는 두개 더 있습니다:
<!-- * **3001** for Bob. -->
* **3001** 번은 'Bob' 입니다.
<!-- * **3004** for Thrift Bank. -->
* **3004** 번은 'Thrift Bank' 입니다.

<!-- > The remainder of the numbers (ports - 9701-9708) are the ports to the Blockchain Ledger nodes - two per node. -->
> 남은 번호들 (9701 ~ 9708 번) 은 블록체인 레저 노드들을 위한 포트입니다 - 노드 하나당 두개씩의 포트가 할당되어 있습니다.

<!-- ## Local Machine -->
### 로컬 환경에서 데모를 진행하는 경우

<!-- To go through the demonstration, open the following links in new browser tabs: -->
데모를 진행하기 위해 브라우저 탭에서 다음의 링크들을 여세요.
<!-- * [http://localhost:3000](http://localhost:3000) for Alice -->
* [http://localhost:3000](http://localhost:3000) 는 'Alice' 를 위한 것입니다.
<!-- * [http://localhost:3002](http://localhost:3002) for Faber College -->
* [http://localhost:3002](http://localhost:3002) 는 'Faber College' 를 위한 것입니다.
<!-- * [http://localhost:3003](http://localhost:3003) for Acme Corporation -->
* [http://localhost:3003](http://localhost:3003) 는 'Acme Corporation' 를 위한 것입니다.

<!-- If you click the links before the Agent is active, you might get a `Connection reset by peer` error messages. Monitor the logs and wait longer and then try again. -->
인디 에이전트가 활성화되기 전에 링크를 누른다면, 아마 `Connection reset by peer` 라는 에러가 뜰 것입니다. 로그 출력창을 확인하면서 조금 더 기다려 본 뒤 다시 시도해 보세요.

<!-- The instructions for walking through the demonstration script are here: **[Agent Demo Script](AgentDemoScript.md)** -->
데모를 따라하기 위한 가이드는 여기에 있습니다: **[Agent Demo Script](AgentDemoScript.md)**

<!-- You can also open in a browser a Ledger Explorer: -->
블록체인 레저 탐색기 또한 브라우저 상에서 열 수 있습니다:
* [http://localhost:9000](http://localhost:9000)

<!-- Although we don't talk about them in the demo overview, there are two additional Agents running that you can access: -->
데모 오버뷰에서는 다루지 않겠지만, 접근할 수 있는 인디 에이전트는 두개 더 있습니다:
<!-- * [http://localhost:3001](http://localhost:3001) for Bob -->
* [http://localhost:3001](http://localhost:3001) 은 'Bob' 을 위한 것입니다.
<!-- * [http://localhost:3004](http://localhost:3004) for Thrift Bank -->
* [http://localhost:3004](http://localhost:3004) 은 'Thrift Bank' 을 위한 것입니다.

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
* 개개인의 정부 ID 증명을 검증하는 것은 이따금씩 실패합니다 - 커다랗고 빨간 X 표시를 출력하면서 말이죠. 저희는 왜 어떤 경우에는 되고 어떤 경우에는 되지 않는지 계속 조사중입니다.
