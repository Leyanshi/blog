---
title: 雨云服务器搭建自用 New API 纪实
date: 2026-08-26 18:00:00
tags: [vibecoding, ai, agents, api]
category: ai
cover: https://photos.leyanshi.me/agents-working-20260529.png
---

## 起因
由于本人薅羊毛太多（PS: AgentRouter给的额度真多啊，夯爆了），电脑里 CC Switch 里的中转站开始堆积如山了，不知道用哪一个好。刚好发零花钱，买个服务器搭个自用中转吧。

## 经过
### 买服务器
[雨云](https://www.rainyun.com/default_)官网注册登录，进控制台，选云服务器，香港 IIJ 区（我对速度要求不高，有需要的童鞋们可以用其他区，这个区便宜哈哈）
配置不用太高，1H1G就行，如图，一共 22.4￥

![](https://photos.leyanshi.me/260826/hk-qu.png)
![](https://photos.leyanshi.me/260826/product-pz.png)
还有就是，这里可以很便捷的预装 Docker，不要忘了勾选

![](https://photos.leyanshi.me/260826/system-docker.png)

### 配置安装
买完服务器直接SSH连。
命令如下：
```shell
git clone https://github.com/QuantumNous/new-api.git
cd new-api
```
然后配置数据库：
```shell
nano docker-compose.yml
# 或者
# vim docker-compose.yml
```
然后启动：
```shell
docker compose up -d
```

然后访问服务器的 IP，配置 Roto User 的用户名和密码。
配置完后一直点下一步即可。

### 必要步骤
![](https://photos.leyanshi.me/260826/ziyongmode.png)

