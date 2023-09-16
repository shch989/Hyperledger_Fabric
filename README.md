# Hyperledger Fabric Prerequisites Setup

Hyperledger Fabric를 설치하기 전에 필요한 전제 조건을 설정하는 방법을 안내합니다.

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
sudo tar -xvf go1.13.4.linux-amd64.tar.gz
```

**Step 4:** 이제 Downloads 폴더 아래에 "go" 폴더가 새로 생성된 것을 볼 수 있어야 합니다. 확인하려면 "ls" 명령을 실행합니다.

**Step 5:** 다음 단계는 "go" 폴더를 Downloads 폴더에서 /usr/local 폴더로 이동하는 것입니다. 아래 명령을 사용하여 이동합니다.
```
$ sudo mv go /usr/local
```
**Step 6:** 다음 단계는 몇 가지 변수를 설정하고 PATH 변수를 업데이트하는 것입니다. 이 작업을 수행하는 두 가지 방법이 있습니다.

첫 번째 방법은 일시적으로 변수를 설정하는 방법이며, 두 번째 방법은 영구적인 변수를 설정하여 반복해서 동일한 단계를 수행하지 않도록 하는 방법입니다.

첫 번째 방법을 선택하려면 다음 단계를 따릅니다.

```
$ export GOROOT=/usr/local/go
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
GOROOT=/usr/local/go
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
$ sudo apt-get install python-pip
$ pip --version
$ sudo pip install docker-compose
```

Docker Compose의 설치를 확인하고 버전을 확인하려면 아래 명령을 실행합니다.

```
$ docker-compose version
```

Hyperledger Fabric를 설치하고 설정하기 위해 필요한 모든 전제 조건이 설정되었습니다.