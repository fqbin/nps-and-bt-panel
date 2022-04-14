### 本指南将帮助您在 安装有宝塔面板的Debian 上使用nps ###

------

### 首先，您应该确保您具有 root 访问权限，以便执行以下步骤。

------

## 1.安装所需软件

0.新建一个文件夹

```
mkdir /your folder name/
```

1.进入文件夹，并访问发布页[下载](https://github.com/ehang-io/nps/releases)对应的系统版本的服务端解压即可

```
#e.g.
cd /your folder name/
wget https://github.com/ehang-io/nps/releases/download/v0.26.10/linux_amd64_server.tar.gz
tar -zcvf /your folder name/linux_amd64_server.tar.gz
```

2.执行安装命令

```
sudo ./nps install
```

3.修改默认端口

- 默认端口

nps默认配置文件使用了80，443，8080，8024端口

80与443端口为域名解析模式默认端口

8080为web管理访问端口

8024为网桥端口，用于客户端与服务器通信

因为安装了宝塔面板所以80和443端口被占用

```
vi /nps/conf/nps.conf
```

修改http、https_proxy_port

4.启动nps

```
sudo nps start
```

5.享受你的nps

- 访问服务端ip:web服务端口（默认为8080）
- 使用用户名和密码登陆（默认admin/123，正式使用一定要更改）
- 创建客户端
