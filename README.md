## Dubbo ecosystem

## Dubbo
Dubbo是一个高性能、可扩展的分布式服务框架，基于RPC，支持多种协议调用、服务监控和治理，同时是去中心化的框架，对应用侵入性小。

![](http://static.oschina.net/uploads/img/201110/30093737_2LhG.jpg)
- [官方网站](http://dubbo.apache.org)
- [GitHub源码](https://github.com/apache/incubator-dubbo)
- [官方文档](http://dubbo.apache.org)
- [官方Wiki](https://github.com/apache/incubator-dubbo/wiki)

## dubbox

Dubbox的功能目前已经合并到Dubbo核心代码仓库中。

https://github.com/dangdangdotcom/dubbox
来自dangdang网，主要是实现了基于JBoss RestEasy的rest支持，升级了spring、zk、json等依赖库，并且一直在维护。目前已经release的版本到2.8.4了。
文档资料：
- [在Dubbo中开发REST风格的远程调用（RESTful Remoting）](https://dangdangdotcom.github.io/dubbox/rest.html)
- [在Dubbo中使用高效的Java序列化（Kryo和FST）](https://dangdangdotcom.github.io/dubbox/serialization.html)
- [使用JavaConfig方式配置dubbox](https://dangdangdotcom.github.io/dubbox/java-config.html)
- [Dubbo Jackson序列化使用说明](https://dangdangdotcom.github.io/dubbox/jackson.html)
- [Demo应用简单运行指南](https://dangdangdotcom.github.io/dubbox/demo.html)
- [Dubbox@InfoQ](http://www.infoq.com/cn/news/2014/10/dubbox-open-source)
- [Dubbox Wiki](https://github.com/dangdangdotcom/dubbox/wiki) （由社区志愿者自由编辑的）

## Dubbo原理和设计相关材料

[Service_Framework_Practices.pdf](https://github.com/dubbo/awesome-dubbo/raw/master/slides/Service_Framework_Practices.pdf)

[High_Performance_Remoting.pdf](https://github.com/dubbo/awesome-dubbo/raw/master/slides/High_Performance_Remoting.pdf)

[Framework_Design_Principles.pdf](https://github.com/dubbo/awesome-dubbo/raw/master/slides/Framework_Design_Principles.pdf)

[Dubbo_RPC_Features.pdf](https://github.com/dubbo/awesome-dubbo/raw/master/slides/Dubbo_RPC_Features.pdf)

[Dubbo_Framework_Extensions.pdf](https://github.com/dubbo/awesome-dubbo/raw/master/slides/Dubbo_Framework_Extensions.pdf)

## Dubbo PPT

[Dubbo 开源现状与未来规划](https://github.com/dubbo/awesome-dubbo/raw/master/slides/dubbo-present-and-future.pdf)


## spring-boot-starter-dubbo

官方starter(maintained by mercyblitz)：
- [https://github.com/apache/incubator-dubbo-spring-boot-project](https://github.com/apache/incubator-dubbo-spring-boot-project)

已有的可用starter:
 - [https://github.com/cyzaoj/spring-boot-dubbo-starter](https://github.com/cyzaoj/spring-boot-dubbo-starter) 可以配置protocol、registry、provider
 - [https://github.com/linking12/spring-boot-starter-dubbo](https://github.com/linking12/spring-boot-starter-dubbo) 可以自动配置、暴露服务
 - [https://github.com/tbud/spring-boot-starter-dubbo](https://github.com/tbud/spring-boot-starter-dubbo) 加了log

## dubbokeeper(dubbo-admin)
https://github.com/dubboclub/dubbokeeper

dubbokeeper是一个开源版本基于spring mvc开发的社区版dubboadmin，同时修复了官方admin存在的一些问题，以及添加了一下必要的功能 例如服务统计，依赖关系等图表展示功能，当前dubbokeeper还属于开发阶段。最终dubbokeeper会集成服务管理以及服务监控一体的DUBBO服务管理系统。注意是增强了配置管理和服务监控。

![image](http://img0.tuicool.com/rIFVZz6.jpg!web)

使用说明：[http://www.cnblogs.com/yyssyh213/p/6031453.html](http://www.cnblogs.com/yyssyh213/p/6031453.html)
几种工具的配置：[http://www.tuicool.com/articles/u6Jzim6](http://www.tuicool.com/articles/u6Jzim6)

## dubbo monitor(bootstrap)
http://git.oschina.net/handu/dubbo-monitor

Dubbo Monitor是针对Dubbo开发的监控系统，基于dubbo-monitor-simple改进而成，可以理解为其演化版本。该系统用关系型数据库（MySQL）记录日志的方式替代了dubbo-monitor-simple写文件的方式。注：亦可改为其他Relational Database（关系型数据库）。
PS: 项目目前依赖的是dubbox的2.8.4版本，但是dubbox并没有修改过监控相关的代码，因此理论上也可以支持dubbo的最新版本。
来自韩都衣舍，最新版本已经支持MongoDB了。感觉可以合并到dubbox，作为monitor的基础骨架来发展。

![image](https://raw.githubusercontent.com/wiki/handuyishe/dubbo-monitor/images/screenshot.png)

## dubbox demos

最简单的例子:
- [https://github.com/kimmking/dubbox-demos](https://github.com/kimmking/dubbox-demos)
- [webservice demo](https://github.com/dubbo/dubbo-ws-demo)

## J2EE DEMO APP
http://git.oschina.net/vmaps/dubbo-app

dubbo-app 是J2EE分布式开发基础平台，使用经典技术组合（dubbo、zookeeper、Spring、SpringMVC、MyBatis、Shiro、redis、quartz、activiti、easyui），包括核心模块如：角色用户、权限授权、工作流等。
对新手来说，是个很好的从quick start到on action。

![image](http://img.blog.csdn.net/20170510223912807?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvS2ltbUtpbmc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## dubbo rest proxy

https://git.oschina.net/wuyu15255872976/dubbo-rpc-proxy

这是一个神奇的小项目，直接把服务转换为rest接口，参数都加到url后面。接口方式太粗暴，for fun。

## dubbo-plus

https://git.oschina.net/bieber/dubbo-plus

提供服务降级控制、增强cache等功能，这块东西感觉可以合并到dubbo或dubbox的。

## dubbo + zipkin

分布式调用链追踪:dubbo+zipkin:
https://github.com/jiangmin168168/jim-framework

原理：[dubbo+zipkin调用链监控](http://www.cnblogs.com/ASPNET2008/p/6709900.html)


## 整合了dubbo及多个常见框架的脚手架项目

https://gitee.com/hackempire/emsite-parent

## 使用jmeter做dubbo接口压力测试的插件

https://github.com/ningyu1/jmeter-plugins-dubbo

## 其他事宜

2017年10月份以来，继续维护了。

v1.2
