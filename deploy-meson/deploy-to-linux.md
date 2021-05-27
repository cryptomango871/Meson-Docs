# Deploy to Linux

## Having reached this part, we assume that you already have a server with 40+GB space and an opened port.

Code reference: [https://meson.network/terminals](https://meson.network/terminals)

```text
#Step.1 download the terminal package
$ wget 'https://assets.meson.network:10443/static/terminal/v2.5.1/meson-linux-amd64.tar.gz'

#Step.2 unzip the package
$ tar -zxf meson-linux-amd64.tar.gz

#Step.3 install the app as service
$ cd ./meson-linux-amd64
$ sudo ./meson service-install

#Step.4 input your token, port and space provide

#Step.5 start the app
$ sudo ./meson service-start

#Step.6 wait about 1 minutes and check status
$ sudo ./meson service-status
after 2-3 minutes you will have a new terminal record

#Step.7 check your earnings


### Other commands ###
"sudo ./meson service-stop" to stop app
"sudo ./meson service-remove" to remove app
```















