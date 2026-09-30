3proxy on pfsense 2.8.1
---
[![Upstream](https://img.shields.io/badge/Upstream-3proxy-blue?logo=github)](https://github.com/3proxy/3proxy)
___
>[!NOTE]
>The binary is built with the following options:
>
>-D3PROXY_USE_OPENSSL=ON — enables SSL support.
>
>-D3PROXY_USE_PCRE2=OFF — disables regular expression support.
```
Diagnostics - Command Prompt
```
```
pkg search git
```
> [!TIP]
> Shell Output - pkg search git
> ```text
> git-2.47.1                     Distributed source code management tool
> py311-gitdb-4.0.11_1           Git Object Database
> py311-gitpython-3.1.43         Python library used to interact with Git repositories
> ```
```
pkg install -y git
```
```
git clone https://github.com/rzagthb/pfsense-3proxy.git
```
```
fetch -o ./pfsense-3proxy/ https://github.com/rzagthb/pfsense-3proxy/releases/latest/download/3proxy
```
```
mkdir -p /usr/local/etc/3proxy
```
```
cp ./pfsense-3proxy/3proxy.cfg /usr/local/etc/3proxy/3proxy.cfg
```
```
cp ./pfsense-3proxy/passwd /usr/local/etc/3proxy/passwd
```
```
chmod +x ./pfsense-3proxy/3proxy
```
```
cp ./pfsense-3proxy/3proxy /usr/local/bin/3proxy
```
```
/usr/local/bin/3proxy /usr/local/etc/3proxy/3proxy.cfg
```
