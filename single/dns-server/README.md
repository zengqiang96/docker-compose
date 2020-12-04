# dns 服务

用于开发中区分测试环境、预生产、显示环境的域名解析

镜像使用 [https://hub.docker.com/r/andyshinn/dnsmasq](https://hub.docker.com/r/andyshinn/dnsmasq)

首先配置上行的真正的dns服务器地址，毕竟你只是个本地代理，不了解外部规则。创建文件：

```
vim /etc/resolv.dnsmasq
```

添加内容：

```
nameserver 114.114.114.114
nameserver 8.8.8.8
```

配置本地解析规则，这才是我们的真实目的。新建配置文件

```
vim /etc/dnsmasqhosts
```

添加解析规则

```
192.168.0.199 minio.wemeng.com
192.168.0.199 api.wemeng.com
192.168.0.199 etcd.wemeng.com
192.168.0.199 xconf.wemeng.com
192.168.0.199 gitlab.wemeng.com
```

修改dnsmasq配置文件，指定使用上述两个我们自定义的配置文件

```
vim /etc/dnsmasq.conf
```


修改下述两个配置

```
resolv-file=/etc/resolv.dnsmasq
addn-hosts=/etc/dnsmasqhosts
```

最后启动就行

```
docker-compose -f docker-compose.yml up
```

## 优点
1. 可以省去频繁的修改本地hosts文件
2. 可统一公司内部人员的域名解析一致
