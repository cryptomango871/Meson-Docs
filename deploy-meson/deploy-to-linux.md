# 리눅스에 배포하기

## 이 문서에서는 여러분이 40기가의 용량 및 포트가 열려있는 서버를 이미 보유하고 있다고 가정합니다.

\[ 코드 예시: [https://meson.network/terminals](https://meson.network/terminals) \]

### Command 1, Meson의 다운로드 및 설치

```text
$ wget 'https://assets.meson.network:10443/static/terminal/v2.5.1/meson-linux-amd64.tar.gz'
```

> 만약 "-bash: wget: command not found" 와 같은 결과가 출력되어 wget을 사용할 수 없는 상황이라면, `wget`을 먼저 설치해주세요. "**sudo apt-get install wget**" 명령어를 통하여 설치할 수 있습니다.

### Command 2, 패키지를 압축 해제

```text
$ tar -zxf meson-linux-amd64.tar.gz
```

### Command 3, Meson을 서비스로 설치 및 등록

```text
$ ./meson-linux-amd64 && sudo ./meson service-install
```

**토큰, 포트, 그리고 사용하실 용량을 인자 \(Parameter\) 로 아래의 지침을 통해 등록합니다:**

**1, 토큰** —— [https://meson.network/terminals](https://meson.network/terminals) 에서 확인하실 수 있습니다.

![&#xB2F9;&#xC2E0;&#xC758; &#xD1A0;&#xD070;&#xC744; &#xC774;&#xACF3;&#xC5D0; &#xC785;&#xB825;&#xD558;&#xC138;&#xC694;. &#xC774;&#xAC83;&#xC774; &#xB2F9;&#xC2E0;&#xC758; ID&#xC785;&#xB2C8;&#xB2E4;.](../.gitbook/assets/image%20%288%29.png)

**2, 포트** —— 방화벽에서 포트 \(default:19091\) 를 열어주세요.

아래는 GCP를 사용하실 경우의 예시입니다.

![](../.gitbook/assets/image%20%285%29.png)

![](../.gitbook/assets/image%20%283%29.png)

**3. 용량** —— 적어도 Meson을 구동하기 위하여 40GB 이상의 용량이 제공되어야 합니다.

많은 용량과 높은 대역폭을 제공할 수록 많은 보상을 얻게됩니다. 자세한 사항은 [https://meson.network/miningrules](https://meson.network/miningrules) 을 참고하세요.

### Command 4, Meson 서비스를 시작

```text
$ sudo ./meson service-start
```

### Command 5, 서비스가 제대로 동작하는지 체크하는 것을 잊지마세요

위의 Command 4 명령어 실행 후 약 1분 정도 기다리세요.

```text
$ sudo ./meson service-status
```

약 2-3 분이 지나면, 새로운 터미널 기록을 [https://meson.network/terminals](https://meson.network/terminals) 에서 확인하실 수 있습니다.

### **혹시 필요할지 모를 다른 명령어들**

```text
$ sudo ./meson service-stop                # Meson Network 서비스를 중단
단
$ sudo ./meson service-remove              # Meson Network 어플리케이션을 서비스에서 제거
```

또한, Meson이 설치된 폴더를 단순히 이동함으로써 설치 경로를 바꿀 수 있습니다.

## 일반적인 작동 방식

### 1, 어떻게 **포트를 변경** 할 수 있나요?

Meson 설치 경로에 있는 **config.txt** 를 변경하세요.

### 2, 어떻게 **용량을 변경** 할 수 있나요?

Meson 설치 경로에 있는 **config.txt** 를 변경하세요.

### 3, **포트 포워딩 규칙을 설정** 했는지 확인해주세요.

이 내용은 만약 개인용 컴퓨터에서 Meson을 실행할 경우 중요한 내용입니다.

클라우드 서버 \(GCP, AWS, Azure, Alibaba, etc.\) 를 사용하는 것이 더 쉽고 안정적이므로 권장됩니다. 만약 여전히 집에서 네트워크 라우터 \(공유기 등...\) 를 이용하여 채굴을 하시는 경우, 아래의 내용을 유튜브/구글 등지에서 검색하실 수 있습니다.

**"Port Forwarding" + \[Your Router Brand\]**

라우터의 설정을 변경하여 당신의 PC와 연결된 IP를 Meson이 라우터를 타고 서버를 찾을 수 있도록 하기 위함입니다.

