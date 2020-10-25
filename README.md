# docker-compose
一些基础服务的docker-compose配置文件，方便在一台新电脑上快速开始工作

不必输入一长串docker命令来启动对应服务，并且可以做到持久化。



## 列表

| 名称 | 备注 |
|:----| :----|
| [etcd3](etcd3) | etcd是一个开源的、分布式的键值对数据存储系统，提供共享配置、服务的注册和发现 |
| [kong](kong) | Kong是一个可扩展的开源API层(也称为API网关或API中间件)。它运行在任何RESTful API之前，并可通过官网提供的插件进行扩展，也可自定义插件进行用户定制的功能扩展。通过插件，可使其提供超出核心平台之外的功能和服务，譬如使用统计，用户身份验证，API授权等。 |
| [mysql](mysql) | MySQL是一个关系型数据库管理系统，由瑞典MySQL AB 公司开发，目前属于 Oracle 旗下产品 |
| [redis](redis) | Redis是一个开源的使用ANSI C语言编写、支持网络、可基于内存亦可持久化的日志型、Key-Value数据库，并提供多种语言的API。 |
| [jumpserver](jumpserver) | Jumpserver是全球首款完全开源的堡垒机，是符合 4A 的专业运维审计系统。 |
| [soar-web](soar-web) | SOAR(SQL Optimizer And Rewriter)是一个对SQL进行优化和改写的自动化工具。 由小米人工智能与云平台的数据库团队开发与维护。 |
| [Yearning](Yearning) | Mysql web端sql审核平台 |
| [KeyDB](keydb) | KeyDB项目是从redis fork出来的分支。众所周知redis是一个单线程的kv内存存储系统，而KeyDB在100%兼容redis API的情况下将redis改造成多线程 |
| [jaegertracing](jaegertracing) | Jaeger 是Uber推出的一款开源分布式追踪系统，兼容OpenTracing API。分布式追踪系统用于记录请求范围内的信息。 |
| [prometheus](prometheus) | 普罗米修斯监控系统 |
| [gitlab](gitlab)| GitLab 是由 GitLab Inc.开发，一款基于 Git 的完全集成的软件开发平台（fully integrated software development platform）。 另外，GitLab 且具有wiki以及在线编辑、issue跟踪功能、CI/CD 等功能。
| [nexus](nexus) | Nexus是Maven仓库管理器，也可以叫Maven的私服。
| [zookeeper](zookeeper) |  Apache ZooKeeper是Apache软件基金会的一个软件项目，它为大型分布式计算提供开源的分布式配置服务、同步服务和命名注册。ZooKeeper曾经是Hadoop的一个子项目，但现在是一个独立的顶级项目。

## 备注

### docker-compose常用命令

1.编译docker镜像

```
docker build -t name .
```

2.使用docker-compose 执行新建容器组

```
docker-compose up

docker-compose up --force-recreate // 强制新建
```

3.启动容器组

```
docker-compose start
```

4.停止容器组

```
docker-compose stop
```

5.查询容器组所有容器状态

```
docker-compose ps
```

6.删除容器组

```
docker-compose down
```

