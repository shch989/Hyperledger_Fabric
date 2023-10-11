# Hyperledger Fabric Prerequisites Setup

Hyperledger Fabric를 설치하기 전에 필요한 전제 조건을 설정하는 방법을 안내합니다. (Ubuntu-20.04 환경)

## Curl 설치

Curl 설치

아래 명령을 실행하여 Curl을 설치합니다.

```
$ sudo apt-get install curl
```

설치를 확인하고 Curl의 버전을 확인하려면 아래 명령을 실행합니다.

```
$ curl --version
```

## NodeJs 설치

NodeJs 설치

터미널 창을 열고 아래 명령을 사용하여 NodeJs 파일을 다운로드하고 실행합니다.

```
$ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash –
```

설치를 확인하고 Curl의 버전을 확인하려면 아래 명령을 실행합니다.

```
$ sudo apt-get update
```

NodeJs를 설치하려면 아래 명령을 실행합니다.

```
$ sudo apt-get install nodejs
```

NodeJs가 성공적으로 설치되었는지 확인하려면 아래 명령을 실행합니다. 이 명령은 NodeJs의 버전을 반환해야 합니다.

```
$ node --version
```

## Git 설치

Git 설치

터미널 창을 열고 아래 명령을 실행하여 Git을 설치합니다.

```
$ sudo apt-get install git
```

Git이 성공적으로 설치되었는지 확인하려면 아래 명령을 실행합니다. 이 명령은 Git의 버전을 반환해야 합니다.

```
$ git --version
```

## Python3 설치

Python3 설치

터미널 창에서 아래 명령을 실행하여 Python을 설치합니다.

```
$ sudo apt-get install python3
```

Python 설치를 확인하려면 아래 명령을 실행합니다. 이 명령은 Python의 버전을 반환해야 합니다.

```
$ python3 --version
```

## Go 언어 설치

Go 언어 설정

다음 단계를 따릅니다.

**Step 1:** 먼저 설치 프로그램을 다운로드해야 합니다. 이를 위해 [https://golang.org/](https://golang.org/) 사이트에 접속합니다. "Go 다운로드" 버튼을 클릭하면 다음 페이지로 이동합니다.

**Step 2:** Linux tar 파일인 Linux 설치 파일을 클릭하여 설치 프로그램을 다운로드합니다.

**Step 3:** 먼저 다운로드한 파일을 압축 해제해야 합니다. 파일은 Downloads 폴더에 다운로드되므로 먼저 해당 폴더로 이동한 다음 다음 명령을 실행합니다.

```
cd Downloads
sudo tar -xvf go1.21.1.linux-amd64.tar.gz
```

**Step 4:** 이제 Downloads 폴더 아래에 "go" 폴더가 새로 생성된 것을 볼 수 있어야 합니다. 확인하려면 "ls" 명령을 실행합니다.

**Step 5:** 다음 단계는 "go" 폴더를 Downloads 폴더에서 $HOME/go 폴더로 이동하는 것입니다. 아래 명령을 사용하여 이동합니다.
```
$ sudo mv go /usr/local
```
**Step 6:** 다음 단계는 몇 가지 변수를 설정하고 PATH 변수를 업데이트하는 것입니다. 이 작업을 수행하는 두 가지 방법이 있습니다.

첫 번째 방법은 일시적으로 변수를 설정하는 방법이며, 두 번째 방법은 영구적인 변수를 설정하여 반복해서 동일한 단계를 수행하지 않도록 하는 방법입니다.

첫 번째 방법을 선택하려면 다음 단계를 따릅니다.

```
$ export GOROOT=$HOME/go
$ cd $HOME
$ mkdir goProject
$ export GOPATH=$HOME/goProject
$ export PATH=$PATH:$GOROOT/bin
$ export PATH=$PATH:$GOPATH/bin
```

두 번째 방법을 선택하려면 다음 단계를 따릅니다.

홈 위치로 이동하고 "ctrl+H"를 눌러 숨겨진 파일을 표시합니다.
.profile 파일을 열고 아래 항목을 추가합니다.

```
GOROOT=$HOME/go
GOPATH=$HOME/goProject
```

PATH 변수를 업데이트하여 GOROOT 및 GOPATH bin 폴더를 추가합니다. PATH 변수는 다음과 같아야 합니다.
```
PATH="$HOME/bin:$HOME/.local/bin:/usr/local/go/bin:$HOME/goProject/bin:$PATH"
```

**Step 7:** 시스템에 Go 언어가 성공적으로 설치되었는지 확인하려면 아래 명령을 실행합니다. 이 명령은 설치된 Go 언어의 버전을 반환해야 합니다.

```
$ go version
```

## Libtool 설치

Libtool 설치

아래 명령을 사용하여 Libtool을 설치합니다.

```
$ sudo apt-get install libltdl-dev
```

## Docker CE (Community Edition) 설치

Docker CE 설치

먼저 Docker CE를 다운로드한 다음 아래 명령을 사용하여 설치합니다.

```
$ wget https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/docker-ce_17.06.2~ce-0~ubuntu_amd64.deb
$ sudo dpkg -i docker-ce_17.06.2~ce-0~ubuntu_amd64.deb
```

Docker의 버전을 확인하려면 아래 명령을 실행합니다.

```
$ docker --version
```

## Docker Compose 설치

Docker Compose 설치

Docker Compose를 설정하려면 아래 명령을 실행합니다.

```
$ sudo apt-get install python3-pip
$ pip --version
$ sudo pip install docker-compose
```

Docker Compose의 설치를 확인하고 버전을 확인하려면 아래 명령을 실행합니다.

```
$ docker-compose version
```

Hyperledger Fabric를 설치하고 설정하기 위해 필요한 모든 전제 조건이 설정되었습니다.

## Hyperledger Fabric 설치

**단계 1:** Fabric을 다운로드하고 설정하기 위해 아래 명령어를 실행하세요.
```
$ curl -sSL https://bit.ly/2ysbOFE | bash -s
$ curl -sSL https://bit.ly/2ysbOFE | bash -s -- 2.0.1
```

위 명령어를 실행할 때 다음과 같은 문제가 발생할 수 있습니다.

```
failed to get default registry endpoint from daemon (Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock:
```

이 문제를 해결하려면 다음 명령어를 실행하세요.

```
$ sudo chmod 666 /var/run/docker.sock
```

이 명령어를 실행한 후, 단계 3에서 언급한 명령어를 다시 실행하면 시스템에 다운로드 및 설정할 수 있습니다.

## Fabric-Samples 폴더에 Chaincode 폴더가 없을 경우

 https://hyperledger-fabric.readthedocs.io/en/latest/install.html 해당 링크의 지시대로 Fabric-Samples을 불러온다

## Docker 사용
```
$ cd fabric-samples
$ cd chaincode-docker-devmode
$ docker-compose -f docker-compose-simple.yaml up
```

## Fabric-Samples Docker 이미지 및 바이너리 다운로드

### 작업 디렉터리 생성 (임의의 폴더 생성 가능)
```
$ mkdir -p $HOME/goProject/github.com/<your_github_userid>
$ cd $HOME/goProject/github.com/<your_github_userid>
```

### 설치 스크립트 
```
$ $ curl -sSLO https://raw.githubusercontent.com/hyperledger/fabric/main/scripts/install-fabric.sh && chmod +x install-fabric.sh
```

### -h 옵션을 보기
```
$ ./install-fabric.sh -h
Usage: ./install-fabric.sh [-f|--fabric-version <arg>] [-c|--ca-version <arg>] <comp-1> [<comp-2>] ... [<comp-n>] ...
        <comp>: Component to install one or more of  d[ocker]|b[inary]|s[amples]. If none specified, all will be installed
        -f, --fabric-version: FabricVersion (default: '2.5.4')
        -c, --ca-version: Fabric CA Version (default: '1.5.7')
```

### Docker 컨테이너를 가져오고 샘플 저장소를 복제
```
$ ./install-fabric.sh docker samples binary
or
$ ./install-fabric.sh d s b
```

### 버전 선택 (선택사항)
```
$ ./install-fabric.sh --fabric-version 2.5.0 binary
```

# Start & Stop test-network

### 단계 1: 아래 명령을 사용하여 fabric-samples 폴더로 이동합니다.
```
$ cd fabric-samples
```

### 단계 2: 아래 명령을 사용하여 test-network 폴더로 이동합니다.
```
$ cd test-network
```

### 단계 3: 아래 명령을 실행하여 테스트 네트워크를 시작합니다.
```
$ sudo ./network.sh up
```

이렇게 하면 네트워크가 시작되며, 다음 명령을 실행하여 도커 컨테이너를 확인할 수 있습니다.

```
$ sudo docker ps
```

이 명령은 다음과 같은 세 가지 도커 컨테이너를 표시합니다.

- Org1 피어 노드 하나
- Org2 피어 노드 하나
- Orderer 하나

네트워크를 시작하면 기본적으로 어떤 채널도 생성되지 않습니다. 다음 명령을 사용하여 현재 채널 상태를 확인할 수 있습니다.

```
$ docker exec peer0.org1.example.com peer channel list
```

이 명령은 채널이 아직 생성되지 않았음을 보여줍니다.

### 단계 4: 아래 명령을 사용하여 새로운 채널을 생성합니다.
```
$ sudo ./network.sh createChannel -c testchannel
```

이렇게 하면 testchannel이라는 이름의 새로운 채널이 생성됩니다.

이 채널 생성을 확인하려면 두 개의 피어에서 다음 명령을 실행하세요.

```
$ sudo docker exec peer0.org1.example.com peer channel list
$ sudo docker exec peer0.org2.example.com peer channel list
```

### 단계 5: 네트워크를 중지하려면 다음 명령을 실행하세요.
```
$ sudo ./network.sh down
```

# Start & Stop test-network with CouchDB

### 단계 1: 아래 명령을 사용하여 fabric-samples 폴더로 이동합니다.
```
$ cd fabric-samples
```

### 단계 2: 아래 명령을 사용하여 test-network 폴더로 이동합니다.
```
$ cd test-network
```

### 단계 3:  아래 명령을 실행하여 네트워크를 시작하고 CouchDB 컨테이너를 생성합니다.
```
$ sudo ./network.sh up -s couchdb
```

이 명령은 네트워크를 시작하고 각 피어에 대해 CouchDB 컨테이너를 생성합니다.

### 단계 4: 아래 명령을 사용하여 새로운 채널을 생성합니다.
```
$ sudo ./network.sh createChannel -c testchannel1
```

이 명령은 testchannel1이라는 이름의 새로운 채널을 생성합니다.

### 단계 5: 네트워크를 중지하려면 다음 명령을 실행하세요.
```
$ sudo ./network.sh down
```

# Start & Stop test-network with CA

### 단계 1: 아래 명령을 사용하여 fabric-samples 폴더로 이동합니다.
```
$ cd fabric-samples
```

### 단계 2: 아래 명령을 사용하여 test-network 폴더로 이동합니다.
```
$ cd test-network
```

### 단계 3: 아래 명령을 실행하여 테스트 네트워크를 시작하고 각 조직마다 CA 컨테이너를 생성합니다 (orderer, org1 피어, org2 피어 각각에 대한 하나).
```
$ sudo ./network.sh up -ca
```

이 명령은 네트워크를 시작하고 각 조직에 대한 CA 컨테이너를 생성합니다.

### 단계 4: 아래 명령을 사용하여 새로운 채널을 생성합니다.

```
$ sudo ./network.sh createChannel -c testchannel2
```

이 명령은 testchannel2라는 이름의 새로운 채널을 생성합니다.

### 단계 5: 네트워크를 중지하려면 다음 명령을 실행하세요.
```
$ sudo ./network.sh down
```

#  Start & Stop test-network with all containers

### 단계 1: 아래 명령을 사용하여 fabric-samples 폴더로 이동합니다.
```
$ cd fabric-samples
```

### 단계 2: 아래 명령을 사용하여 test-network 폴더로 이동합니다.
```
$ cd test-network
```

### 단계 3: 아래 명령을 실행하여 모든 컨테이너 (2개의 피어, 오더러, 3개의 CA, 2개의 CouchDB)를 가진 테스트 네트워크를 시작합니다.
```
$ sudo ./network.sh up -ca -s couchdb
```

이 명령은 모든 컨테이너를 포함하여 테스트 네트워크를 시작합니다.

### 단계 4: 아래 명령을 사용하여 testchannel3라는 이름의 새로운 채널을 생성합니다.
```
$ sudo ./network.sh createChannel -c testchannel3
```

### 단계 5: 네트워크를 중지하려면 다음 명령을 실행하세요.
```
$ sudo ./network.sh down
```

