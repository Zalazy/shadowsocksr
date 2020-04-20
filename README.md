# 开始安装

```
git clone https://github.com/Zalazy/ShadowsocksR.git
```
```
cd shadowsocksr
```
```
./setup_cymysql.sh
```
```
./initcfg.sh
```
# 安装进程守护
```
cd /root
```
```
apt-get -y install supervisor
```
```
nano /etc/supervisor/conf.d/ssr.conf
```
```
[program:ssr]
command = python /root/shadowsocksr/server.py 
autorestart = true
autostart = true
user = root
startsecs = 5
```
```
ulimit -n 1024000
```
