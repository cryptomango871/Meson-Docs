# Deploy to Linux

## Having reached this part, we assume that you already have a server with 40+GB space and an opened port.

\[ Code reference: [https://meson.network/terminals](https://meson.network/terminals) \]

### Command 1, Download and Install Meson

```text
$ wget 'https://assets.meson.network:10443/static/terminal/v2.5.1/meson-linux-amd64.tar.gz'
```

> If you get notifications like "-bash: wget: command not found" telling that you can't use this command, please install wget by using "**sudo apt-get install wget**" first.

### Command 2, Unzip this package

```text
$ tar -zxf meson-linux-amd64.tar.gz
```

### Command 3, Install Meson as a service

```text
$ ./meson-linux-amd64 && sudo ./meson service-install
```

**Token, Port, and Space are parameter you need to input here:**

**1, Token** —— from [https://meson.network/terminals](https://meson.network/terminals)

![Please input your own Token. This is your ID.](../.gitbook/assets/image%20%288%29.png)

**2, Port** —— Please open a port \(default:19091\) from the firewall

The below is an example of what to do in GCP:

![](../.gitbook/assets/image%20%285%29.png)

![](../.gitbook/assets/image%20%283%29.png)

**3. Space** —— At least please offer 40+GB space for Meson.

High Space and Bandwidth for High Earning. please check [https://meson.network/miningrules](https://meson.network/miningrules) for details.

### Command 4, Start the service of Meson

```text
$ sudo ./meson service-start
```

### Command 5, Please remember to check if it runs well

Please wait about 1 minute after the above one.

```text
$ sudo ./meson service-status
```

After 2-3 minutes, you will have a new terminal record at [https://meson.network/terminals](https://meson.network/terminals).

### **Other Commands For Your Information**

```text
$ sudo ./meson service-stop                #To Stop Meson Network Service

$ sudo ./meson service-remove              #To Remove Meson Network Application
```

You could just move the folder of Meson to change the install position.

## Common Attentions

### 1, How to **Change the Port**?

Please modify **config.txt at** the folder of Meson.

### 2, How to **Change the Space**?

Please modify **config.txt at** the folder of Meson.

### 3, Be sure to **Set up the Port Forwarding Rules**

This step is important for your own personal computer to run Meson.

It's much recommended to use Cloud Servers\(GCP, AWS, Azure, Alibaba, etc.\) which are easier and more stable. But if you still want to try to mine on your own PC at home with the network router... You could search —— 

**"Port Forwarding" + \[Your Router Brand\]**                          at YouTube/Google/etc...

That is to change the configuration to tell your router this IP is connected with your PC so that Meson could find your device\(server\) through your router.

