---
title: "docker相关"
---

修改国内镜像地址
```bash
# cat /etc/docker/daemon.json 
{
    "registry-mirrors": ["https://registry.docker-cn.com"],
    "insecure-registries": ["10.0.0.12:5000"]
}
```

docker 启动

```bash
docker run -it -v /data/db:/mongodata --name mongodb -d mongo
```
`-v`表示地址映射，把容器地址和实际宿主地址建立映射

```bash
sudo docker run -it -v /Users/apple/db/mongoData:/data/db -p 27017:27017  --name mongodb -d mongo
```
|选项	|选项简写|	说明|
|--|--|--|
|–detach|	-d|	在后台运行容器，并且打印容器id。|
|–interactive|	-i|	即使没有连接，也要保持标准输入保持打开状态，一般与 -t 连用。|
|–tty|	-t|	分配一个伪tty，一般与 -i 连用。|