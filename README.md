# ServerStatus-for-alpine 

### 使用说明
ServerStatus used for alpine
这是根据 alpine 系统改造而成的ServerStatus Client

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
apk add gcc musl-dev linux-headers python3-dev
```

安装 pip

```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
```
安装 psutil

```
pip install --no-binary :all: psutil
```
下载目录下的status-client-alpine.py

输入用户信息等 启动

```
python status-client-alpine.py
```
