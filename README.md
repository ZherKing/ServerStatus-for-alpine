# ServerStatus-for-alpine 

在 ServerStatus-Hotaru 的基础上更改完成 → [原帖](https://github.com/CokeMine/ServerStatus-Hotaru)

示例网站 → [点击进入](https://status.mclzyun.com)
### 使用说明
ServerStatus used for alpine
这是根据 alpine 系统改造而成的ServerStatus Client（不是服务端）

### 在使用本程序前你需要有以下环境：

- python3
- psutil
- python-dev
- gcc
- musl-dev
- linux-headers

### 你可以输入以下命令直接安装：

```
apk update
apk add python3 gcc musl-dev linux-headers python3-dev
```

安装 pip

```
apk add curl
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
```
安装 psutil

```
pip install --no-binary :all: psutil
```
下载目录下的status-client-alpine.py

```
mkdir -p /usr/local/ServerStatus/client
cd /usr/local/ServerStatus/client/
wget https://github.com/ZherKing/ServerStatus-for-alpine/raw/main/status-client-alpine.py
```

设置开机自启

```
cd /etc/init.d/
wget https://github.com/ZherKing/ServerStatus-for-alpine/raw/main/status-client-apline.alpine
chmod 777 status-client-apline.alpine
rc-update add status-client-apline.alpine boot
```

输入用户信息等

```
vim /usr/local/ServerStatus/client/status-client-alpine.py
```

启动

```
service status-client-apline.alpine restart
```
