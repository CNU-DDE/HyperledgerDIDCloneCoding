# Hyperledger Indy Agent ์ค๋ช

๐ https://github.com/swcurran/education/tree/master/LFS171x

์ด ํด๋์๋ ๊ธฐ๋ณธ Hyperledger Indy Agent์ ๋ฐ๋ชจ๊ฐ ํฌํจ๋์ด ์์ต๋๋ค. ์์ด์ ํธ๋ ์น ๋ธ๋ผ์ฐ์  ์ธํฐํ์ด์ค๋ฅผ ์ ๊ณตํ์ฌ ์์ด์ ํธ ๊ฐ์ ๊ด๊ณ ์ค์ , ๊ฒ์ฆ ๊ฐ๋ฅํ ์๊ฒฉ ์ฆ๋ช ๋ฐ๊ธ ๋ฐ ๊ฒ์ฆ ๊ฐ๋ฅํ ์๊ฒฉ ์ฆ๋ช์ ํด๋ ์์ ์ฆ๋ชํฉ๋๋ค.

> **์ด ๋ฐ๋ชจ๋ ์๋ก์ด ๊ตฌํ์ ๊ธฐ์ด๋ก ์ฌ์ฉํ๊ฑฐ๋ ์์ด์ ํธ ๊ตฌํ์ ์ํ ์ฐธ์กฐ๋ก ์ฌ์ฉํด์๋ _NOT_ ์ผ๋ถ ์ด๊ธฐ Indy ์์ด์ ํธ ์ฝ๋๋ฅผ ๊ธฐ๋ฐ์ผ๋ก ํฉ๋๋ค. ์ด ๋ฐ๋ชจ๊ฐ ๊ฐ๋ฐ๋ ์ดํ๋ก Indy(๋ฐ Aries) ์ปค๋ฎค๋ํฐ๋ ์์ด์ ํธ์ ๊ฐ๋์ ํฌ๊ฒ ๋ฐ์ ์์ผฐ๊ณ  ์ด ์ฝ๋ ๊ธฐ๋ฐ์ ๋ฒ๋ ค์ก์ต๋๋ค. ์์ด์ ํธ๊ฐ ํผ์์ ์ธ ์์ค์์ ์๋ํ๋ ๋ฐฉ์์ ์ดํดํ๋ ๋ฐ ์ฌ์ ํ ์ข์ ๋ฐ๋ชจ์๋๋ค -- ์๊ฒฉ ์ฆ๋ช์ ์ฐ๊ฒฐํ๊ณ  ๊ตํํ๋ ์์ด์ ํธ์ ๊ฐ๋. ๊ทธ๋ฌ๋ ์ต์  Indy/Aries ์ฝ๋๋ฅผ ๊ธฐ๋ฐ์ผ๋ก ๊ตฌ์ถํ๋ ๋ฐ ๊ด์ฌ์ด ์๋ ๊ฒฝ์ฐ, [Aries project](https://github.com/hyperledger/aries), [Aries Cloud Agent - Python](https://github.com/hyperledger/aries-cloudagent-python) ๋ฐ ๊ธฐํ ์ํธ ์ด์ฉ ๊ฐ๋ฅํ ๊ตฌ์ฑ ์์๋ฅผ ์ดํด๋ด์ผ ํฉ๋๋ค. ๊ฐ๋ฐ์(๋๋ ์ง๋ง์)์ธ ๊ฒฝ์ฐ ์ด [Becoming an Indy/Aries Developer](https://github.com/hyperledger/aries-cloudagent-python/tree/master/docs/GettingStartedAriesDev) ๊ฐ์ด๋๋ฅผ ํ์ธํ์ธ์.**

Hyperledger Indy์ ๋ํด ๋ ๋ฐฐ์ฐ๊ณ  ์ถ์ผ๋ฉด, ์ด ํ๋ก์ ํธ๋ฅผ ์ฐธ๊ณ ํ์ธ์ ! - https://wiki.hyperledger.org/display/indy.

์ด ๋ฐ๋ชจ๋ Hyperledger ํ๋ก์ ํธ์ EdX๋ฅผ ์ฌ์ฉํ๋ ์ฌ๋๋ค์ ์ํ ์ฐ์ต์ผ๋ก ์ฌ์ฉ๋ฉ๋๋ค. [Blockchain for Business](https://www.edx.org/course/blockchain-business-introduction-linuxfoundationx-lfs171x-0) ๊ณผ์ ์ด๋ค.

๋๊ฐ ๋ฐ๋ชจ๋ฅผ ์์ํ ๋, ์ด๊ฒ์ **[Agent Demo Script](AgentDemoScript.md)** Alice๊ฐ Hyperledger Indy๋ฅผ ์ฌ์ฉํ์ฌ Faber College์์ ์ฑ์ ํ๋ฅผ ๋ฐ์ ๋ค์ ์ด๋ฅผ ์ฌ์ฉํ์ฌ Acme Corp์ ์ง์ํ๋ ์๋๋ฆฌ์ค๋ฅผ ์๋ดํฉ๋๋ค.

๋ฐ๋ชจ์ ๊ฐ๋จํ ๋น๋์ค ํ๋ฉด ๋นํ๋ฅผ ๋ณด๊ธฐ ์ํด์ [ํด๋ฆญํ์ธ์.](https://youtu.be/9WZxlrGMA3s).

## Credits

์ด ๋ฐ๋ชจ์ ์ฝ๋๋ ์ฒ์์ Spencer Holman ๊ทธ๋ฆฌ๊ณ  Brigham Young University์ ์๋ Matthew Hailstone์ ์ํด ์ฐ์ฌ์ก์ต๋๋ค. Carol Howard ์ด ๋ฌธ์์ ์ค๋ช์ ๋ง๋ค์์ต๋๋ค.

## ๋์ Browser ๋๋ Local Machine์ ์๋์ํค๊ธฐ

์ด ๋ฐ๋ชจ๋ ๋ธ๋ผ์ฐ์ ๋ง ์ฌ์ฉํ์ฌ ํฐ๋ฏธ๋์์ ์คํํ  ์ ์์ต๋๋ค , ๋๋ ๊ธฐ์ ์ ์ธ ๊ฒฝํฅ์ด ์๋ ๊ฒฝ์ฐ, ๋๋ ๋์ local machine์์ ์๋ ์ํฌ ์ ์์ต๋๋ค. ๋ค์ ์น์์์ ๋ฐ๋ชจ๋ฅผ ์คํํ๋ ค๋ ๋ฐฉ๋ฒ์ ๋ฐ๋ผ `In Browser` ๊ทธ๋ฆฌ๊ณ  `Local Machine`์ ๋ํ ํ์ ์น์์ด ์์ต๋๋ค.

## Prerequisites(์ ์ ์กฐ๊ฑด)

### ๋ธ๋ผ์ฐ์  ๋ด

์ ์ ์กฐ๊ฑด์ [Docker Hub](https://hub.docker.com)๊ณ์ ์ ์ฌ์ฉํ๋ ์กฐ๊ฑด์๋๋ค. ๋์ปค ํ๋ธ๋ [Docker](https://docker.com)์ํ๊ณ์์ 'ํ๋ ์ด ์คํ ์ด'๊ฐ์ ์กด์ฌ์๋๋ค.

### Local Machine

๋ก์ปฌ ๋จธ์ ์์ ์ด Indy Agent ๋ฐ๋ชจ๋ฅผ ์คํํ๊ธฐ ์ํด์๋ ๋ค์์ด ์ค์น๋์ด ์์ด์ผ ํฉ๋๋ค!

- ๋์ปค, (Docker Compose๋ฅผ ํฌํจํ) - Community Edition๋ ๊ด์ฐฎ์ต๋๋ค.
  - ๋ง์ฝ ๋์ปค๊ฐ ์ค์น๋์ด ์์ง ์์ ๊ฒฝ์ฐ, [this link](https://docs.docker.com/install/#supported-platforms) ์ฌ๊ธฐ ๋งํฌ๋ฅผ ํตํด ํ๋ซํผ์ ์ค์นํฉ๋๋ค!
  - ๋ค์ํ ๋์ปค ์ปดํฌ์งํธ๋ฅผ ์ค์นํ๋ ๋ฐฉ๋ฒ์ ์ฌ๊ธฐ๋ฅผ ์ฐธ๊ณ ํ์ธ์! [here](https://docs.docker.com/compose/install/).
- git
  - [This link](https://www.linode.com/docs/development/version-control/how-to-install-git-on-linux-mac-and-windows/) ํด๋น ๋งํฌ์์๋ MAC, Linux ๊ทธ๋ฆฌ๊ณ  virtualBox๋ฅผ ์ฌ์ฉํ์ฌ Linux๋ฅผ ์ฑํํ๋ ๊ฒฝ์ฐ๋ฅผ ํฌํจํด์ ์ค์น ๋ฐฉ๋ฒ์ ์ ๊ณตํฉ๋๋ค.

## Installing the Demonstration

### ๋ธ๋ผ์ฐ์  ๋ด

[Play with Docker](https://labs.play-with-docker.com/)๋ก ์ด๋ํฉ๋๋ค. ๊ทธ๋ฆฌ๊ณ  ํ์ํ๋ค๋ฉด ๋ก๊ทธ์ธ์ ์งํํฉ๋๋ค. ํด๋น ์ฌ์ดํธ๋ Docker์ ๋ํด ํ์ตํ๋ ๊ฐ๋ฐ์๋ฅผ ์ํด ์ด์๋๋ ์ฌ์ดํธ ์๋๋ค.

> ๋ง์ฝ `Play with Docker` ํ๊ฒฝ์ ๋ํด ๋ฐฐ์ฐ๊ณ  ์ถ๋ค๋ฉด, [About](https://training.play-with-docker.com/about/) ์ฌ๊ธฐ๋ฅผ ์ฐธ๊ณ ํ์ธ์! [Training Site](https://training.play-with-docker.com)๋ Docker Labs์ ์ฐ์ต ์ฌ์ดํธ ์๋๋ค.

์์ ๋ฒํผ์ ํด๋ฆญํ์ฌ ๋ฐ๋ชจ ์คํ์ ์ฌ์ฉํ  ์ ์๋ ๋์ปค ์๋๋ฐ์ค๋ฅผ ์์ํฉ๋๋ค. ๊ทธ๋ฆฌ๊ณ  +ADD an Ianstance ๋งํฌ๋ฅผ ํด๋ฆญํ์ฌ ๋ธ๋ผ์ฐ์ ์์ ํฐ๋ฏธ๋์ ์์ํ๊ณ  ๋ค์ ๋ช๋ น์ด๋ฅผ ์คํผํฉ๋๋ค:

- `git clone https://github.com/hyperledger/education`

> **Tip**: ํฐ๋ฏธํธ์์ ๋ถ์ฌ๋ฃ์ ๋ ๋ง์ฐ์ค ์ค๋ฅธ์ชฝ ํด๋ฆญ์ ํ ๋ค `paste`๋ฅผ ๋๋ฌ์ฃผ์ธ์!

- ๋ค์ ๋ช๋ น์ด๋ฅผ ์คํํ์ฌ ์ฝ๋ ์์น๋ก ์ด๋ํฉ๋๋ค:
  - `cd education/LFS171x/indy-material/nodejs`

### Local Machine

๋ก์ปฌ ๋จธ์ ์ ๋ฐ๋ชจ๋ฅผ ์ค์นํ๋ ค๋ฉด EdX Blockchain for Business์ git ์ ์ฅ์๋ฅผ cloneํด์ผ ํฉ๋๋ค:

- ์๋์ฐ ํฐ๋ฏธ๋์ ์ด์ด ์คํ ์  ํ๊ฒฝ์ ์ธํํ๊ฒฝ์ ํ์ธํฉ๋๋ค:
  - Run `git --version`, `git version 2.17.1`์ธ์ง ํ์ธํฉ๋๋ค.
  - Run `docker --version`, `Docker version 18.06.1-ce, build e68fc7a`์ธ์ง ํ์ธํฉ๋๋ค.
  - Run `docker-compose --version`, `docker-compose version 1.22.0, build f46880fe`์ธ์ง ํ์ธํฉ๋๋ค.
  - ๋ฒ์ ์ ์ ๋ฒ์ ๋ณด๋ค ๊ฐ๊ฑฐ๋ ํฌ๋ฉด ์๊ด ์์ต๋๋ค.
- ํฐ๋ฏธ๋์ ์ด์ด ์์ค์ฝ๋๋ฅผ ์ค์นํ  ๊ฒฝ๋ก๋ก ์ด๋ํฉ๋๋ค.
- Run the command: `git clone https://github.com/hyperledger/education/`
  - ์ ์ฝ๋๋ฅผ ์คํํ๋ฉด ์์ค์ฝ๋๊ฐ ์ ์์ ์ผ๋ก ์์ํ์ ์ ์ฅ๋ฉ๋๋ค.
- ๋ค์ ๋ช๋ น์ด๋ฅผ ํตํด ์ฝ๋ ์์น๋ก ์ด๋ํฉ๋๋ค:
  - `cd education/LFS171x/indy-material/nodejs`

## Starting the Demonstration

<!-- The steps for runnning the demonstration are similar for the `In Browser` and `Local Machine` scenarios: -->

๋ฐ๋ชจ๋ฅผ ์คํ์ํค๊ธฐ ์ํ ๋จ๊ณ๋ `๋ธ๋ผ์ฐ์  ํ๊ฒฝ`์์์ ๋ฐ๋ชจ์ `๋ก์ปฌ ํ๊ฒฝ`์์์ ๋ฐ๋ชจ ๋ชจ๋ ๋์ผํฉ๋๋ค:

<!-- - Run the command `./manage build` to build the components of the software -->

- `./manage build` ๋ช๋ น์ด๋ฅผ ํตํด ์ปดํฌ๋ํธ๋ค์ ๋น๋ํ  ์ ์์ต๋๋ค.
<!-- - Run the command `./manage up` to run the components -->
- `./manage up` ๋ช๋ น์ด๋ฅผ ํตํด ์ปดํฌ๋ํธ๋ค์ ์คํ์ํฌ ์ ์์ต๋๋ค.

<!-- It takes a while for the demo to start - lots of things are happening. The logs for all of the containers will display in the terminal window. Logs show the output of both the Blockchain Ledger nodes communicating, and the Indy Agents starting up and communicating with the Ledger. -->

๋ฐ๋ชจ๋ฅผ ์์ํ๋ ๋ฐ์๋ ์กฐ๊ธ ์๊ฐ์ด ๊ฑธ๋ฆด ์๋ ์์ต๋๋ค - ์์ฒญ๋๊ฒ ๋ง์ ์ผ๋ค์ด ์ผ์ด๋๊ณ  ์๊ฑฐ๋ ์. ๋ชจ๋  ์ปจํ์ด๋๋ค์ ๋ก๊ทธ๊ฐ ํฐ๋ฏธ๋ ์ฝ์์ฐฝ์ ์ถ๋ ฅ๋  ๊ฒ์๋๋ค. ๋ก๊ทธ์๋ ๋ธ๋ก์ฒด์ธ ๋ ์  ๋ธ๋ ์์ชฝ์ด ์ํตํ๋ ๊ณผ์ ๊ณผ, ์ธ๋ ์์ด์ ํธ๋ค์ด ์คํ๋๊ณ  ๋ธ๋ก์ฒด์ธ ๋ ์ ์ ์ํตํ๋ ๊ณผ์ ์ด ์ถ๋ ฅ๋  ๊ฒ์๋๋ค.

<!-- Things to watch for as the demo starts up: -->

๋ฐ๋ชจ๊ฐ ์์๋ ๋ ๋์ฌ๊ฒจ๋ด์ผํ  ์ ๋ค์ ์ด๊ฒ๋ค์๋๋ค:

<!-- * You should periodically see things like "Listening on port 3001", which indicates an Agent is up and running. -->

- "Listening on port 3001" ๊ณผ ๊ฐ์ ๋ฌธ๊ตฌ๋ค์ด ์์ฃผ ๋ณด์ผ ๊ฒ์๋๋ค. ์ด๊ฒ์ ์ธ๋ ์์ด์ ํธ๋ค์ด ํ์ฑํ๋์ด ์คํ๋๊ณ  ์๋ค๋ ๋ป์๋๋ค.
<!-- * You should **not** see a stack trace error in the code - that would indicate a problem. -->
- ์๋ฌ๊ฐ ๋ฌ๋ค๋ฉด ์ด๊ฒ์ ๋ฌธ์ ๊ฐ ์๋ค๋ ๋ป์ด๊ธฐ ๋๋ฌธ์ ์๋ฌ๋ค์ ๋ณด์ฌ์๋ **์๋ฉ๋๋ค**.
<!-- * You should **not** see any "Container exiting" messages, indicating containers not starting up properly. -->
- "Container exiting" ๊ณผ ๊ฐ์ ๋ฌธ๊ตฌ ๋ํ ๋ณด์ฌ์๋ **์๋ฉ๋๋ค**. ์ด๊ฒ์ ์ปจํ์ด๋๋ค์ด ์ ๋๋ก ์คํ๋์ง ์์๋ค๋ ๊ฒ์ ๋ปํ๊ธฐ ๋๋ฌธ์๋๋ค.
<!-- * There should be 10 docker containers running. You can hit `ctrl-c` to exit the log viewer and run the command `docker ps` to see all of the containers running. Run `./manage logs` if you want to see the logs again. -->
- ์ด ๋ฐ๋ชจ์๋ 10๊ฐ์ ์ปจํ์ด๋๊ฐ ์๋๋์ด์ผ๋ง ํฉ๋๋ค. `ctrl-c` ๋ฅผ ๋๋ฌ ๋ก๊ทธ ์ถ๋ ฅ์ฐฝ์ ์ข๋ฃํ ํ `docker ps` ๋ช๋ น์ด๋ฅผ ํตํด ์คํ๋๊ณ  ์๋ ์ปจํ์ด๋๋ค์ ๋ณผ ์ ์์ต๋๋ค. ๋ค์ ๋ก๊ทธ ์ถ๋ ฅ์ฐฝ์ ๋ณด๊ธธ ์ํ๋ค๋ฉด, `./manage logs` ๋ช๋ น์ด๋ฅผ ์๋ ฅํ๋ฉด ๋ฉ๋๋ค.
<!-- * Once the output slows significantly and you only see messages from the nodes (the containers running the ledger), everything should be working. -->
- ๋ก๊ทธ๊ฐ ์ถ๋ ฅ๋๋ ์๋๊ฐ ํ์ ํ ๋๋ ค์ง๊ณ  ๋ธ๋ (๋ธ๋ก์ฒด์ธ ๋ ์ ๋ฅผ ๊ตฌ๋์ํค๋ ์ปจํ์ด๋๋ค) ๋ค์ด ์ถ๋ ฅํ๋ ๋ฉ์์ง๋ค๋ง์ด ๋ณด์ธ๋ค๋ฉด, ๋ชจ๋  ๊ฒ์ด ์๋ฒฝํ๊ฒ ์๋ํ์ฌ์ผ๋ง ํฉ๋๋ค.

<!-- ### Access the ledger and agents in a web browser: -->

### ์น ๋ธ๋ผ์ฐ์ ๋ฅผ ํตํด ๋ธ๋ก์ฒด์ธ ๋ ์ ์ ์ธ๋ ์์ด์ ํธ๋ค์๊ฒ ์ ๊ทผํ๊ธฐ:

<!-- ### In Browser -->

### ๋ธ๋ผ์ฐ์  ํ๊ฒฝ์์ ๋ฐ๋ชจ๋ฅผ ์งํํ๋ ๊ฒฝ์ฐ

<!-- As the demo starts up, a series of 4 digit numbers will appear above the terminal. Those are the exposed ports of the running containers and the numbers are links to start a Browser tab accessing that port. -->

๋ฐ๋ชจ๊ฐ ์์๋๊ณ  ๋ ๋ค์๋, ํฐ๋ฏธ๋ ์ฝ์์ฐฝ์ 4์๋ฆฌ์ ์ซ์๋ค์ด ๋ณด์ผ ๊ฒ์๋๋ค. ์ด๊ฒ๋ค์ ์๋์ค์ธ ์ปจํ์ด๋๋ค์ด ์ธ๋ถ๋ก ๊ณต๊ฐ์์ผ๋์ ํฌํธ๋ค์ด๊ณ  ๊ฐ๊ฐ์ ์ซ์๋ค์ ํด๋น ํฌํธ์ ์ ๊ทผํ  ์ ์๋ ๋ธ๋ผ์ฐ์  ํญ์ ์ฌ๋ ๋งํฌ์๋๋ค.

<!-- To go through the demonstration, click the following numbers from the list: -->

๋ฐ๋ชจ๋ฅผ ์งํํ๊ธฐ ์ํด, ๋ชฉ๋ก์์ ๋ค์์ ๋ฒํธ๋ค์ ํด๋ฆญํ์ธ์:

<!-- * **3000** for Alice -->

- **3000** ๋ฒ์ 'Alice' ์๋๋ค.
<!-- * **3002** for Faber College -->
- **3002** ๋ฒ์ 'Faber College' ์๋๋ค.
<!-- * **3003** for Acme Corporation -->
- **3003** ๋ฒ์ 'Acme Corporation' ์๋๋ค.

<!-- If you click the links before the Agent is active, you might get a `Connection reset by peer` error messages. Monitor the logs and wait longer and then try again. -->

์ธ๋ ์์ด์ ํธ๊ฐ ํ์ฑํ๋๊ธฐ ์ ์ ๋งํฌ๋ฅผ ๋๋ฅธ๋ค๋ฉด, ์๋ง `Connection reset by peer` ๋ผ๋ ์๋ฌ๊ฐ ๋ฐ ๊ฒ์๋๋ค. ๋ก๊ทธ ์ถ๋ ฅ์ฐฝ์ ํ์ธํ๋ฉด์ ์กฐ๊ธ ๋ ๊ธฐ๋ค๋ ค ๋ณธ ๋ค ๋ค์ ์๋ํด ๋ณด์ธ์.

<!-- The instructions for walking through the demonstration script are here: **[Agent Demo Script](AgentDemoScript.md)** -->

๋ฐ๋ชจ๋ฅผ ๋ฐ๋ผํ๊ธฐ ์ํ ๊ฐ์ด๋๋ ์ฌ๊ธฐ์ ์์ต๋๋ค: **[Agent Demo Script](AgentDemoScript.md)**

<!-- You can also open in a browser a Blockchain Ledger Explorer: -->

๋ธ๋ก์ฒด์ธ ๋ ์  ํ์๊ธฐ ๋ํ ๋ธ๋ผ์ฐ์  ์์์ ์ด ์ ์์ต๋๋ค:

- **9000**

<!-- Although we don't talk about them in the demo overview, there are two additional Agents running that you can access: -->

๋ฐ๋ชจ ์ค๋ฒ๋ทฐ์์๋ ๋ค๋ฃจ์ง ์๊ฒ ์ง๋ง, ์ ๊ทผํ  ์ ์๋ ์ธ๋ ์์ด์ ํธ๋ ๋๊ฐ ๋ ์์ต๋๋ค:

<!-- * **3001** for Bob. -->

- **3001** ๋ฒ์ 'Bob' ์๋๋ค.
<!-- * **3004** for Thrift Bank. -->
- **3004** ๋ฒ์ 'Thrift Bank' ์๋๋ค.

<!-- > The remainder of the numbers (ports - 9701-9708) are the ports to the Blockchain Ledger nodes - two per node. -->

> ๋จ์ ๋ฒํธ๋ค (9701 ~ 9708 ๋ฒ) ์ ๋ธ๋ก์ฒด์ธ ๋ ์  ๋ธ๋๋ค์ ์ํ ํฌํธ์๋๋ค - ๋ธ๋ ํ๋๋น ๋๊ฐ์ฉ์ ํฌํธ๊ฐ ํ ๋น๋์ด ์์ต๋๋ค.

<!-- ## Local Machine -->

### ๋ก์ปฌ ํ๊ฒฝ์์ ๋ฐ๋ชจ๋ฅผ ์งํํ๋ ๊ฒฝ์ฐ

<!-- To go through the demonstration, open the following links in new browser tabs: -->

๋ฐ๋ชจ๋ฅผ ์งํํ๊ธฐ ์ํด ๋ธ๋ผ์ฐ์  ํญ์์ ๋ค์์ ๋งํฌ๋ค์ ์ฌ์ธ์.

<!-- * [http://localhost:3000](http://localhost:3000) for Alice -->

- [http://localhost:3000](http://localhost:3000) ๋ 'Alice' ๋ฅผ ์ํ ๊ฒ์๋๋ค.
<!-- * [http://localhost:3002](http://localhost:3002) for Faber College -->
- [http://localhost:3002](http://localhost:3002) ๋ 'Faber College' ๋ฅผ ์ํ ๊ฒ์๋๋ค.
<!-- * [http://localhost:3003](http://localhost:3003) for Acme Corporation -->
- [http://localhost:3003](http://localhost:3003) ๋ 'Acme Corporation' ๋ฅผ ์ํ ๊ฒ์๋๋ค.

<!-- If you click the links before the Agent is active, you might get a `Connection reset by peer` error messages. Monitor the logs and wait longer and then try again. -->

์ธ๋ ์์ด์ ํธ๊ฐ ํ์ฑํ๋๊ธฐ ์ ์ ๋งํฌ๋ฅผ ๋๋ฅธ๋ค๋ฉด, ์๋ง `Connection reset by peer` ๋ผ๋ ์๋ฌ๊ฐ ๋ฐ ๊ฒ์๋๋ค. ๋ก๊ทธ ์ถ๋ ฅ์ฐฝ์ ํ์ธํ๋ฉด์ ์กฐ๊ธ ๋ ๊ธฐ๋ค๋ ค ๋ณธ ๋ค ๋ค์ ์๋ํด ๋ณด์ธ์.

<!-- The instructions for walking through the demonstration script are here: **[Agent Demo Script](AgentDemoScript.md)** -->

๋ฐ๋ชจ๋ฅผ ๋ฐ๋ผํ๊ธฐ ์ํ ๊ฐ์ด๋๋ ์ฌ๊ธฐ์ ์์ต๋๋ค: **[Agent Demo Script](AgentDemoScript.md)**

<!-- You can also open in a browser a Ledger Explorer: -->

๋ธ๋ก์ฒด์ธ ๋ ์  ํ์๊ธฐ ๋ํ ๋ธ๋ผ์ฐ์  ์์์ ์ด ์ ์์ต๋๋ค:

- [http://localhost:9000](http://localhost:9000)

<!-- Although we don't talk about them in the demo overview, there are two additional Agents running that you can access: -->

๋ฐ๋ชจ ์ค๋ฒ๋ทฐ์์๋ ๋ค๋ฃจ์ง ์๊ฒ ์ง๋ง, ์ ๊ทผํ  ์ ์๋ ์ธ๋ ์์ด์ ํธ๋ ๋๊ฐ ๋ ์์ต๋๋ค:

<!-- * [http://localhost:3001](http://localhost:3001) for Bob -->

- [http://localhost:3001](http://localhost:3001) ์ 'Bob' ์ ์ํ ๊ฒ์๋๋ค.
<!-- * [http://localhost:3004](http://localhost:3004) for Thrift Bank -->
- [http://localhost:3004](http://localhost:3004) ์ 'Thrift Bank' ์ ์ํ ๊ฒ์๋๋ค.

<!-- ## Stopping the Demo -->

## ๋ฐ๋ชจ ๊ทธ๋ง ํ๊ธฐ

<!-- ### In Browser -->

### ๋ธ๋ผ์ฐ์  ํ๊ฒฝ์์ ๋ฐ๋ชจ๋ฅผ ์งํํ๋ ๊ฒฝ์ฐ

<!-- To stop the demo, go to the browser tab where you ran `docker-compose up` and close the browser tab. Note that if you don't close the tab, the terminal session will expire 4 hours after you started it. -->

๋ฐ๋ชจ๋ฅผ ๊ทธ๋งํ๊ธฐ ์ํด์๋, `docker-compose up` ๋ช๋ น์ด๋ฅผ ์๋ ฅํ๋ ๋ธ๋ผ์ฐ์  ํญ์ ๋ซ์ผ์ธ์. ๋ง์ผ ๋ธ๋ผ์ฐ์  ํญ์ ๋ซ์ง ์๋๋ค๋ฉด, ํฐ๋ฏธ๋ ์ธ์์ ์์๋์ง 4์๊ฐ ๋ค์ ๋ง๋ฃ๋๋ค๋ ๊ฒ์ ๊ธฐ์ตํ์ธ์.

<!-- ### Local Machine -->

### ๋ก์ปฌ ํ๊ฒฝ์์ ๋ฐ๋ชจ๋ฅผ ์งํํ๋ ๊ฒฝ์ฐ

<!-- To stop the demo, go to the terminal window where you ran `docker-compose up`. If the logs are scrolling and/or you are not at the command prompt, hit `Ctrl-C`. Run the command `./manage down`.  You should see a `Done` message as each of the 10 containers stops.  Run the command `docker ps` to see that the containers have stopped. -->

๋ฐ๋ชจ๋ฅผ ๊ทธ๋งํ๊ธฐ ์ํด์๋, `docker-compose up` ๋ช๋ น์ด๋ฅผ ์๋ ฅํ๋ ํฐ๋ฏธ๋ ์ฐฝ์ผ๋ก ๊ฐ์ธ์. ๋ก๊ทธ๊ฐ ๊ณ์ ์ถ๋ ฅ๋๊ณ  ์๊ฑฐ๋ ๋ช๋ น ์๋ ฅ์ฐฝ์ด ๋ณด์ด์ง ์๋ ๊ฒฝ์ฐ์๋, `ctrl-c` ๋ฅผ ๋๋ฅด์ธ์. ๊ทธ ๋ค์์๋ `./manage down` ๋ช๋ น์ด๋ฅผ ์๋ ฅํ์ธ์. 1๊ฐ์ ์ปจํ์ด๋๊ฐ ์ข๋ฃ๋  ๋๋ง๋ค `Done` ์ด๋ผ๋ ๋ฉ์ธ์ง๊ฐ ๋ณด์ฌ์ผ๋ง ํ๊ณ , ์ด 10๊ฐ์ ์ปจํ์ด๋๊ฐ ์ข๋ฃ๋  ๊ฒ์๋๋ค. `docker ps` ๋ช๋ น์ด๋ฅผ ์๋ ฅํ์ฌ ๋ชจ๋  ์ปจํ์ด๋๋ค์ด ์ข๋ฃ๋์๋์ง ํ์ธํ์ธ์.

<!-- # Trouble Shooting -->

# ๋ฌธ์  ํด๊ฒฐํ๊ธฐ

<!-- > As issues are discovered by users of this demo, we'll add more troubleshooting instructions here. -->

> ์ด ๋ฐ๋ชจ์ ๋ฌธ์ ๊ฐ ์ ์ ๋ค์ ์ํด ๋ฐํ์ง ๋๋ง๋ค, ์ ํฌ๋ ์ด๊ณณ์ ๋ฌธ์  ํด๊ฒฐ ๋ฐฉ๋ฒ์ ๊ณ์ ์ถ๊ฐํ  ๊ฒ ์๋๋ค.

<!-- * The "validate" of the Government ID Credential for each of the Identities is often failing - displaying a large red "X". We're still investigating why that is happening in some cases but not others. -->

- ๊ฐ๊ฐ์ธ์ ์ ๋ถ ID ์ฆ๋ช์ ๊ฒ์ฆํ๋ ๊ฒ์ ์ด๋ฐ๊ธ์ฉ ์คํจํฉ๋๋ค - ์ปค๋ค๋๊ณ  ๋นจ๊ฐ X ํ์๋ฅผ ์ถ๋ ฅํ๋ฉด์ ๋ง์ด์ฃ . ์ ํฌ๋ ์ ์ด๋ค ๊ฒฝ์ฐ์๋ ๋๊ณ  ์ด๋ค ๊ฒฝ์ฐ์๋ ๋์ง ์๋์ง ๊ณ์ ์กฐ์ฌ์ค์๋๋ค.
