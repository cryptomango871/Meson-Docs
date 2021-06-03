---
description: GCP를 이용하여 Meson을 채굴하기
---

# 구글 클라우드 플랫폼

### **자원을 효율적으로 이용하기 위해서는 유휴 터미널을 사용하여 Meson 프로젝트를 배포하는 것이 좋습니다.** 

### **그래도, GCP를 이용하고자 하신다면, 아래의 지침을 따라주세요. Meson을 채굴하는 동시 GCP에 회원가입하고, 프로젝트를 생성하여 프로젝트를 시작할 수 있습니다.**

## Step1, 회원 가입

구글 클라우드 플랫폼 (GCP) 웹사이트에 방문합니다. [https://cloud.google.com/](https://cloud.google.com/)

![https://cloud.google.com/](https://lh3.googleusercontent.com/BFEuYjyKdigUxh6uosA1V-lniOLOosWFKzpLn0uy8zC-EVnSKHKKB-mNT1ncu9GhKIIcbDgGoQbfVtDGfFqXVBcNdYg8HEnHNWSfcVbxzl5f9bY_9Q9nPLYeT3ZrTsLEwZj4C005)

지침을 따라 전화번호와 신용카드 (마스터카드 혹은 Visa) 를 입력하면 90일동안 사용할 수 있는 $300의 시험 크레딧을 얻게 됩니다.

## Step2, 인스턴스 템플릿 생성

1. 탐색 메뉴 열기 -> "Compute Engine" 클릭 -> "인스턴스 템플릿" 클릭

![](https://lh4.googleusercontent.com/VrX5H6dPh9GP2eXCVUHo9BQO4s1g7FQ5YCjwjak6x-uUeRT6WM4rgMMM1T3qERVtcwLF7wh-A7JVicL6Y9oIh9s096UnNVCGuEcG5j9b2AmouJS4iMFpm38gsLgLbrrTyAtqjR8q)

1. 인스턴스 템플릿 만들기

![](https://lh6.googleusercontent.com/TWIvG7PKv5You3pCiAa9G8CoExQVBV9xp59Xd90zqNeXf7ZRMFGuQ5_QdMqGmHQnwGqrjDCOTHMZ0NtbvkjDP98wtttcHbPrDfgaeXTXu37uxOdpYGOpBd40EkZ13a-MznmQ2LSu)

![](https://lh5.googleusercontent.com/e0_M_kKDB2G5mojHWBAEDuHKUmuS0EZDVTgegkgufxdvNzMT4yIdqtHCOjqPjbbaJaXK_DvGl3LDl8hqXDtuSavTAGphQVItesA5_SXlp0va8cOAZeRmYbGQ8hJn--e3PABx0XFk)

2. 디스크의 용량을 최소 50 GB로 변경

![](https://lh3.googleusercontent.com/c0iDFahZjwvU_8CYaiPQeLcw0iFwxwrHX-An5aAud3QJ5aMQwaRuArE9hgI_BTp4oQ3SOmZPp6z6PAhH41pKe9ZmGXiCVNJOrBpO08WC7pL9zJoaBU0WEroWeTi3_nGY_HLjG0IL)

`변경` 버튼을 눌러 디스크의 용량을 50 GB 이상으로 늘려주세요. 서비스를 실행하기 위해서는 40 GB 이상의 용량이 필요합니다.

![](https://lh6.googleusercontent.com/SGPt4I2QDDafSoTxgnHhcKlfDUYqpcNxwEya0cflHOnx_ziE2gQRPzZL6ailVwqvtd2PgyoBrcY_5NI2C3eCzmX4BC7WeVzKEGDVqqWfA8UVKxSW79Pq2niLx3wHIsu6G3le3t2a)

3. Meson 네트워크에서 사용할 포트를 열기 위해서 네트워크 태그 "meson" 을 추가합니다.

![](https://lh6.googleusercontent.com/s8YM9_0mUK4y9hOZUUSMZr9-ZR8qOADnYorAsvNWXPrqVCAkpVWjZSRILo3xTNNCC6Q3eLDsuvaJyDpACTSA5A71-oUw6qbtQ4_jaPYlaPNiaao1J01o7w5IiYh4-jio3BksSAZm)

![](https://lh5.googleusercontent.com/rMOfc7HfnnRL6F1ErpICXYdDboLaHdgHdXiJRwhqW-qVskIzBNkDS665cdGBCvuqbL5NAZC12d4tN4K40aQ2nVrhZco1wf8K-wy-AlfZwGjCSEk5pUpBDjDoN4Buf7PcuRgzgVdy)

## Step3, 방금 추가한 네트워크 태그 "meson" 을 설정합니다.

![](https://lh5.googleusercontent.com/MH0t9dGPi5qtpjPMa0_N93xtajemPXMPs4skjf3FRwzUCSKH42wtdHtmzp9uUrE8A0DUJhD-DMS7EtLRsgrKGVVH-lzSH2m03SqwNPpwd8MlwfLQ7hNRtPsdxSm514XzK-SD-Om7)

![](https://lh5.googleusercontent.com/B8TdJTapBkzNYcbO0NJH8sALWdjvSij6PLebmx52VLspqvdjeEgcPvBeESJrDuvNi-R5bsvL4v1SNy3yxCMcT16Y1XuWuicrrFeNDhD3czqyv8-_T-AjZcVyN0f1HGNHIQTWVBBP)

![](https://lh5.googleusercontent.com/bKiMdxpc7ezMiCGDHQiNNIsRrPAE32tJ6Rrg0rL_4OxAef4MLfSNBsraAD8QxefO4acLV_KtkB89nj6vpHpQG_6WhMze_W0q70vNZWz7om2F7M1QU8j3k97rywJZITmg-aB7iA0g)

상단의 스크린샷을 참고하여 TCP 연결에 대해 19091 포트를 열도록 설정합니다.

## Step4, meson-template 인스턴스 템플릿으로부터 VM 인스턴스 생성하기

![](https://lh4.googleusercontent.com/e0gnXfoaQipEkDhrdGJgtEBw8xHB0Q47OEz12vzstfp_FH9Blz4dZUrwAtjYfK7wnkX01RrbqkzxdkHjNQ7kNnUILrqo-FizjjSbgi0fgn1XM4kQbeB_t7iVgbPV-SB4bNDF3YPq)

![](https://lh4.googleusercontent.com/3EjV9Ya5WpNBWMqv_qej2kCZ0DgHU-zJI10Ebs5S0bwtqmSU-9a2pH16tXh-lT7PNqAcfreQ-7ddC9PjuJm_7FxDx4Za62uxXwzxKCCszPJXo1nnWLspkOOzFWA-H_JeZjM98E2V)

![](https://lh4.googleusercontent.com/BL66Ysp9weNgSD2PZrcMlJKX4ta6tUxq2y3TucHMEBzFSXedUz3_SVSdVeNW0NvR33p1kBf_kBmBgy2CwxJXZqQQrMyX843wT-vBsOS60yhthdGd8SHwn3PLwVqm1MsWGJKWgPHs)

위에서 이미 인스턴스 템플릿을 만들었기 때문에, 단순히 "만들기" 버튼만 클릭하면 됩니다.

![](https://lh3.googleusercontent.com/yoUY9GMIjSvUAIl6VwjNZHVm9UNpsQCKyBiprgkrrj7JhIMYEZY5ldzGIMtDUmRpwaAZFcQgs2-LNK39Hv3bwRyyf3slJu93F4yI_-Rytiebw9Rfhdgq2UtIWQlbH2OPFVDB02Lo)

## Step5, 배포를 마무리하기 위해 SSH를 클릭하여 서버에 연결하세요

![](https://lh3.googleusercontent.com/YY7tAWPzRPOziSZ21redgIeD0CtEN-r8UgBYq-zVulssJn-Eis8hn9N9yrK478AusT48jAUHeGddQimAKLNrkGkwpnt0gxvmFCWIrk6ECeRqFKc2wIRn-V1relc87R18gIyAs3ez)

당신의 서버를 Meson 터미널로 배포하기 위해 아래 링크의 지침을 따라하세요.

“[https://meson.network/terminals](https://meson.network/terminals)”

```text
####### 튜토리얼: 리눅스 서버에서 채굴자 터미널을 설치하고 구동하기 #######
당신이 사용하는 포트가 방화벽에서 열려있어야 하며, "sudo" 권한이 사용 가능해야 합니다.

# Step.1 터미널 패키지 다운로드
$ wget 'https://assets.meson.network:10443/static/terminal/v2.5.1/meson-linux-amd64.tar.gz'
# Step.2 패키지 압축풀기
$ tar -zxf meson-linux-amd64.tar.gz
# Step.3 App을 서비스로 등록
$ cd ./meson-linux-amd64
$ sudo ./meson service-install
# Step.4 토큰, 사용할 포트, 제공할 용량 입력
# Step.5 App 구동
$ sudo ./meson service-start
# Step.6 1분 정도 대기하여 상태를 체크
$ sudo ./meson service-status
약 2-3분 후 새로운 터미널 레코드를 생성하게 됩니다.
# Step.7 채굴 수익 확인
### 다른 명령어들 ###
app 구동 정지: "sudo ./meson service-stop"
app 삭제: "sudo ./meson service-remove"

( 이것은 현재 (2021/05/27) 리눅스 64비트 서버 기준으로 작성되었습니다. )
```

그리고 현재 배포한 서버가 Meson Note로 작동되고 있음을 확인할 수 있습니다.

![](https://lh6.googleusercontent.com/By_Vwucqe-qFyQMgZATpLMVwqNYj4m8GneRri8t-iKOTV1TOKrV5Gm1lbcHcorImeHu6JEmGCmRqjNA26I63MUqiK3d2N7c7KlSCyqFWIvXn8HyxApi7rwTdWvbwJbEQCz5BBetb)

여기까지 도달하셨다면 축하드립니다!

## 다른 질문이 있나요?

웹사이트: [https://meson.network/](https://meson.network/)

디스코드: [https://discord.com/invite/z6YfSHDkmS](https://discord.com/invite/z6YfSHDkmS)

텔레그램: [https://t.me/mesonnetwork](https://t.me/mesonnetwork)

## 무료 체험 이후 요금이 발생할 수도 있으니 유의바랍니다.

[https://cloud.google.com/vpc/network-pricing](https://cloud.google.com/vpc/network-pricing)

![](https://lh4.googleusercontent.com/qV1oYOUUh4zbxAlhnQ5WfXWruCxT9l9pWoOAMc6m1aEfuedpY7XYDY9HBD6sLjQPMU8mla_BzkSAMIrk4laX1kzPMMO5DnsKFGWQaXjUtsLMfNYyrLP9VJhj_iob-5jqqF8f3Xjs)

![](https://lh6.googleusercontent.com/plsuqeH1aLPmcznSK8u_3yx3OjPukzSZmRGnrelsCoX7qqn_XbK5jxal5_QCa007Ot45JzhPyH0wkQmS2ClzUdNmqWmCX138nVl5xAeJ4qJ2dENkwKYA64GLeglEJ5QA2zE2wrCG)
