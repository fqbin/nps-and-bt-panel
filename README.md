### This guide will help you to use nps on Debian with bt panel installed.

------

### To begin with, you should ensure that you have got root access in order to do the following steps.

------

#### 1.Install required softwares

0.new folder

1.Enter the folder and visit the release page [download](https://github.com/ehang-io/nps/releases) to decompress the server of the corresponding system version

```
#e.g.
cd /your folder name/
wget https://github.com/ehang-io/nps/releases/download/v0.26.10/linux_amd64_server.tar.gz
tar -zcvf /your folder name/linux_amd64_server.tar.gz
```

2.To install

```
sudo ./nps install
```

3.Edit the default port

- Default port

The nps default configuration file uses ports 80, 443, 8080, and 8024

Ports 80 and 443 are the default ports in domain name resolution mode

8080 is the web management access port

8024 is the bridge port for client-server communication

Ports 80 and 443 are occupied because the bt panel is installed

```
vi /nps/conf/nps.conf
```

edit http、https_proxy_port

4.start nps

```
sudo nps start
```

5.enjoy your nps

- Access server IP:web service port (default is 8080).
- Login with username and password (default is admin/123, must be modified when officially used).
- Create a client.

