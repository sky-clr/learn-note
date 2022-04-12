> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [blog.csdn.net](https://blog.csdn.net/ThinkWon/article/details/103592572)

> 更新于2019-12-15 10:38:00本人从事Java开发已多年，平时有记录问题解决方案和总结知识点的习惯，整理了一些有关Java的知识体系，这不是最终版，会不定期的更新。也算是记录自己在从事编程工作的成长足迹，通过博客可以促进博主与阅读者的共同进步，结交更多志同道合的朋友。特此分享给大家，本人见识有限，写的博客难免有错误或者疏忽的地方，还望各位大佬指点，在此表示感激不尽。文章目录...

> 更新于 2021-08-13 22:55:12

欢迎关注微信公众号【技术人成长之路】

**【技术人成长之路】**，助力技术人成长！更多精彩文章第一时间在公众号发布哦！  
![](https://img-blog.csdnimg.cn/7426075944a74deeb3ef3a3c264ed86b.jpg#pic_center)

**本人从事 Java 开发已多年，平时有记录问题解决方案和总结知识点的习惯，整理了一些有关 Java 的知识体系，这不是最终版，会不定期的更新**。也算是记录自己在从事编程工作的成长足迹，通过博客可以促进博主与阅读者的共同进步，结交更多志同道合的朋友。**特此分享给大家，本人见识有限，写的博客难免有错误或者疏忽的地方，还望各位大佬指点，在此表示感激不尽**。

整理的 Java 知识体系主要包括**基础知识，工具，并发编程，数据结构与算法，数据库，JVM，架构设计，应用框架，中间件，微服务架构，分布式架构，程序员的一些思考，团队与项目管理，运维，权限，推荐书籍，云计算，区块链**等，包含了作为一个 Java 工程师在开发工作学习中需要用到或者可能用到的绝大部分知识。**千里之行始于足下**，希望大家根据自己的薄弱点，查缺补漏，根据自己感兴趣的方面多学习，学的精通一点，从现在开始行动起来。**路漫漫其修远兮，吾将上下而求索，不管编程开发的路有多么难走，多么艰辛，我们都将百折不挠，不遗余力地去追求和探索**。

![](https://img-blog.csdnimg.cn/2019121810082198.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly90aGlua3dvbi5ibG9nLmNzZG4ubmV0,size_16,color_FFFFFF,t_70)

### 文章目录

*   *   [Java 面试总结](#Java_16)
    *   [基础知识](#_44)
    *   *   [Java 概述](#Java_46)
        *   [基础语法](#_60)
        *   [面向对象](#_107)
        *   [集合框架](#_123)
        *   [IO 流](#IO_138)
        *   [网络编程](#_152)
        *   [常用 API](#API_182)
        *   *   [日期时间 API](#API_190)
        *   [常用工具类库](#_201)
        *   [单元测试](#_214)
        *   [异常](#_220)
        *   [日志](#_233)
        *   [Java8 新特性](#Java8_249)
    *   [工具](#_261)
    *   *   [IDEA](#IDEA_263)
        *   [Eclipse & STS](#Eclipse__STS_273)
        *   [Maven](#Maven_281)
        *   [Docker](#Docker_294)
        *   [Git](#Git_307)
        *   [GitLab](#GitLab_320)
        *   [GitKraken](#GitKraken_324)
        *   [Navicat](#Navicat_328)
    *   [并发编程](#_332)
    *   *   [基础知识](#_334)
        *   [并发理论](#_345)
        *   [并发关键字](#_356)
        *   [Lock 体系](#Lock_366)
        *   [并发容器](#_391)
        *   [线程池](#_405)
        *   [原子操作类](#_416)
        *   [并发工具](#_424)
        *   [并发实践](#_433)
    *   [数据结构与算法](#_443)
    *   *   [数据结构](#_445)
        *   [算法](#_472)
        *   *   [排序算法](#_495)
        *   [LeetCode](#LeetCode_513)
    *   [数据库](#_532)
    *   *   [Oracle](#Oracle_534)
        *   [MySQL](#MySQL_538)
        *   *   [数据库基础知识](#_540)
            *   [数据类型](#_552)
            *   [引擎](#_554)
            *   [索引](#_556)
            *   [三大范式](#_558)
            *   [常用 SQL 语句](#SQL_560)
            *   [存储过程与函数](#_562)
            *   [视图](#_564)
            *   [MySQL 优化](#MySQL_566)
            *   [事务](#_568)
            *   [数据备份与还原](#_570)
        *   [Redis](#Redis_574)
    *   [Java 虚拟机](#Java_595)
    *   *   [深入理解 Java 虚拟机](#Java_597)
    *   [架构设计](#_610)
    *   *   [设计模式](#_622)
        *   *   [创建型模式](#_643)
            *   [结构型模式](#_655)
            *   [行为型模式](#_670)
            *   [J2EE 模式](#J2EE_689)
            *   [实践应用](#_704)
    *   [应用框架](#_714)
    *   *   [Spring](#Spring_787)
        *   *   [《Spring 实战》读书笔记](#Spring_798)
        *   [Spring MVC](#Spring_MVC_812)
        *   [MyBatis](#MyBatis_816)
        *   *   [MyBatis 源码分析](#MyBatis__838)
        *   [Quartz](#Quartz_852)
        *   [Hibernate](#Hibernate_861)
        *   [Shiro](#Shiro_865)
        *   [Spring Security](#Spring_Security_867)
        *   [Netty](#Netty_871)
        *   [搜索引擎](#_875)
        *   *   [Lucene/Solr](#LuceneSolr_877)
            *   [Elasticsearch](#Elasticsearch_879)
            *   [ELK](#ELK_881)
    *   [中间件](#_885)
    *   *   [消息中间件](#_887)
        *   *   [RabbitMQ](#RabbitMQ_889)
            *   [RocketMQ](#RocketMQ_891)
            *   [ActiveMQ](#ActiveMQ_893)
            *   [Kafka](#Kafka_895)
        *   [远程过程调用中间件](#_899)
        *   *   [Dubbo](#Dubbo_901)
        *   [数据访问中间件](#_905)
        *   [Web 应用服务器](#Web_913)
        *   *   [Tomcat](#Tomcat_915)
            *   [Nginx](#Nginx_931)
        *   [缓存](#_935)
        *   [其他](#_947)
        *   *   [Zookeeper](#Zookeeper_949)
    *   [微服务与分布式](#_953)
    *   *   [Spring Boot](#Spring_Boot_955)
        *   [Spring Cloud](#Spring_Cloud_964)
        *   [服务注册发现](#_991)
        *   [服务配置](#_993)
        *   [负载均衡](#_995)
        *   [服务调用](#_997)
        *   [服务限流](#_999)
        *   [熔断降级](#_1001)
        *   [网关路由](#_1003)
        *   [服务权限](#_1005)
        *   [链路追踪](#_1007)
        *   [分布式事务](#_1009)
        *   [分布式缓存](#_1011)
        *   [分布式会话](#_1013)
        *   [日志收集](#_1015)
        *   [服务监控](#_1017)
        *   [消息驱动](#_1019)
        *   [数据处理流](#_1021)
        *   [自动化测试与部署](#_1023)
        *   [第三方支持](#_1025)
        *   [分布式协调服务 Zookeeper](#Zookeeper_1027)
    *   [程序员的一些思考](#_1031)
    *   [团队与项目管理](#_1041)
    *   *   [需求调研](#_1043)
        *   [项目管理](#_1047)
        *   [代码管理](#_1055)
        *   [文档管理](#_1059)
        *   [测试](#_1068)
    *   [Python](#Python_1072)
    *   [运维](#_1083)
    *   [操作系统](#_1105)
    *   *   [CentOS8](#CentOS8_1117)
    *   [推荐书籍](#_1129)
    *   [读书笔记](#_1138)
    *   [云计算](#_1156)
    *   [搜索引擎](#_1162)
    *   [权限管理](#_1168)
    *   [区块链](#_1174)

Java 面试总结
---------

Java 面试总结汇总，整理了包括 Java 基础知识，集合容器，并发编程，JVM，常用开源框架 Spring，MyBatis，数据库，中间件等，包含了作为一个 Java 工程师在面试中需要用到或者可能用到的绝大部分知识。欢迎大家阅读，本人见识有限，写的博客难免有错误或者疏忽的地方，还望各位大佬指点，在此表示感激不尽。文章持续更新中…

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java 基础知识面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104390612">https://thinkwon.blog.csdn.net/article/details/104390612</a></td></tr><tr><td>2</td><td>Java 集合容器面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104588551">https://thinkwon.blog.csdn.net/article/details/104588551</a></td></tr><tr><td>3</td><td>Java 异常面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104390689">https://thinkwon.blog.csdn.net/article/details/104390689</a></td></tr><tr><td>4</td><td>并发编程面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104863992">https://thinkwon.blog.csdn.net/article/details/104863992</a></td></tr><tr><td>5</td><td>JVM 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104390752">https://thinkwon.blog.csdn.net/article/details/104390752</a></td></tr><tr><td>6</td><td>Spring 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104397516">https://thinkwon.blog.csdn.net/article/details/104397516</a></td></tr><tr><td>7</td><td>Spring MVC 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104397427">https://thinkwon.blog.csdn.net/article/details/104397427</a></td></tr><tr><td>8</td><td>Spring Boot 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104397299">https://thinkwon.blog.csdn.net/article/details/104397299</a></td></tr><tr><td>9</td><td>Spring Cloud 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104397367">https://thinkwon.blog.csdn.net/article/details/104397367</a></td></tr><tr><td>10</td><td>MyBatis 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101292950">https://thinkwon.blog.csdn.net/article/details/101292950</a></td></tr><tr><td>11</td><td>Redis 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103522351">https://thinkwon.blog.csdn.net/article/details/103522351</a></td></tr><tr><td>12</td><td>MySQL 数据库面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104778621">https://thinkwon.blog.csdn.net/article/details/104778621</a></td></tr><tr><td>13</td><td>消息中间件 MQ 与 RabbitMQ 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104588612">https://thinkwon.blog.csdn.net/article/details/104588612</a></td></tr><tr><td>14</td><td>Dubbo 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104390006">https://thinkwon.blog.csdn.net/article/details/104390006</a></td></tr><tr><td>15</td><td>Linux 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104588679">https://thinkwon.blog.csdn.net/article/details/104588679</a></td></tr><tr><td>16</td><td>Tomcat 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104397665">https://thinkwon.blog.csdn.net/article/details/104397665</a></td></tr><tr><td>17</td><td>ZooKeeper 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104397719">https://thinkwon.blog.csdn.net/article/details/104397719</a></td></tr><tr><td>18</td><td>Netty 面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/104391081">https://thinkwon.blog.csdn.net/article/details/104391081</a></td></tr><tr><td>19</td><td>架构设计 &amp; 分布式 &amp; 数据结构与算法面试题（2020 最新版）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/105870730">https://thinkwon.blog.csdn.net/article/details/105870730</a></td></tr></tbody></table>

基础知识
----

### Java 概述

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94353575">https://thinkwon.blog.csdn.net/article/details/94353575</a></td></tr><tr><td>2</td><td>Java 发展历程</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94353653">https://thinkwon.blog.csdn.net/article/details/94353653</a></td></tr><tr><td>3</td><td>Java 语言特点</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94354013">https://thinkwon.blog.csdn.net/article/details/94354013</a></td></tr><tr><td>4</td><td>JDK 安装与环境变量配置</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94353907">https://thinkwon.blog.csdn.net/article/details/94353907</a></td></tr><tr><td>5</td><td>JVM、JRE 和 JDK 的关系</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101369973">https://thinkwon.blog.csdn.net/article/details/101369973</a></td></tr><tr><td>6</td><td>Java 是编译型还是解释型语言</td><td><a href="https://thinkwon.blog.csdn.net/article/details/108678327">https://thinkwon.blog.csdn.net/article/details/108678327</a></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

### 基础语法

大部分已完成

待整理：

Java 开发必会的反编译知识（附支持对 Lambda 进行反编译的工具）

一文读懂什么是 Java 中的自动拆装箱

Java 的枚举类型用法介绍

类、枚举、接口、数组、可变参数

泛型、序列化

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java 标识符</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101637454">https://thinkwon.blog.csdn.net/article/details/101637454</a></td></tr><tr><td>2</td><td>Java 关键字 (Java 8 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101642385">https://thinkwon.blog.csdn.net/article/details/101642385</a></td></tr><tr><td>3</td><td>Java 注释</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101643185">https://thinkwon.blog.csdn.net/article/details/101643185</a></td></tr><tr><td>4</td><td>Java 访问修饰符</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101643412">https://thinkwon.blog.csdn.net/article/details/101643412</a></td></tr><tr><td>5</td><td>Java 分隔符</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101643617">https://thinkwon.blog.csdn.net/article/details/101643617</a></td></tr><tr><td>6</td><td>Java 转义字符</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101643769">https://thinkwon.blog.csdn.net/article/details/101643769</a></td></tr><tr><td>7</td><td>Java 进制</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101643936">https://thinkwon.blog.csdn.net/article/details/101643936</a></td></tr><tr><td>8</td><td>Java 流程控制语句</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101645978">https://thinkwon.blog.csdn.net/article/details/101645978</a></td></tr><tr><td>9</td><td>Java 流程控制语句 - 顺序结构</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101644820">https://thinkwon.blog.csdn.net/article/details/101644820</a></td></tr><tr><td>10</td><td>Java 流程控制语句 - 分支结构</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101645224">https://thinkwon.blog.csdn.net/article/details/101645224</a></td></tr><tr><td>11</td><td>Java 流程控制语句 - 循环结构</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101645757">https://thinkwon.blog.csdn.net/article/details/101645757</a></td></tr><tr><td>12</td><td>Java 表达式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101648114">https://thinkwon.blog.csdn.net/article/details/101648114</a></td></tr><tr><td>13</td><td>Java 运算符</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101649002">https://thinkwon.blog.csdn.net/article/details/101649002</a></td></tr><tr><td>14</td><td>Java 变量</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101649292">https://thinkwon.blog.csdn.net/article/details/101649292</a></td></tr><tr><td>15</td><td>Java 常量</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101649446">https://thinkwon.blog.csdn.net/article/details/101649446</a></td></tr><tr><td>16</td><td>Java 数据类型</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101649568">https://thinkwon.blog.csdn.net/article/details/101649568</a></td></tr><tr><td>17</td><td>Java 反射</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100128361">https://thinkwon.blog.csdn.net/article/details/100128361</a></td></tr><tr><td>18</td><td>Java 语法糖</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100103689">https://thinkwon.blog.csdn.net/article/details/100103689</a></td></tr><tr><td>19</td><td>Java 注解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100178709">https://thinkwon.blog.csdn.net/article/details/100178709</a></td></tr><tr><td>20</td><td>JSON 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100642585">https://thinkwon.blog.csdn.net/article/details/100642585</a></td></tr><tr><td>21</td><td>Properties 类简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100667783">https://thinkwon.blog.csdn.net/article/details/100667783</a></td></tr><tr><td>22</td><td>XML 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100642425">https://thinkwon.blog.csdn.net/article/details/100642425</a></td></tr><tr><td>23</td><td>YML 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100642870">https://thinkwon.blog.csdn.net/article/details/100642870</a></td></tr><tr><td>24</td><td>Java8 新特性 - Lambda 表达式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100642932">https://thinkwon.blog.csdn.net/article/details/100642932</a></td></tr><tr><td>25</td><td>Java 基础语法</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94354151">https://thinkwon.blog.csdn.net/article/details/94354151</a></td></tr></tbody></table>

### 面向对象

待整理：

抽象

继承、封装、多态

接口、抽象类、内部类

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>什么是面向对象</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100667386">https://thinkwon.blog.csdn.net/article/details/100667386</a></td></tr></tbody></table>

### 集合框架

迭代器、增强 for、泛型

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java 集合框架总结</td><td><a href="https://thinkwon.blog.csdn.net/article/details/98844796">https://thinkwon.blog.csdn.net/article/details/98844796</a></td></tr><tr><td>2</td><td>ArrayList(JDK1.8) 源码解析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/98845119">https://thinkwon.blog.csdn.net/article/details/98845119</a></td></tr><tr><td>3</td><td>HashMap(JDK1.8) 源码解析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/98845487">https://thinkwon.blog.csdn.net/article/details/98845487</a></td></tr><tr><td>4</td><td>LinkedHashMap(JDK1.8) 源码解析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102574293">https://thinkwon.blog.csdn.net/article/details/102574293</a></td></tr><tr><td>5</td><td>LinkedList(JDK1.8) 源码解析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102573923">https://thinkwon.blog.csdn.net/article/details/102573923</a></td></tr><tr><td>6</td><td>TreeMap(JDK1.8) 源码解析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102571883">https://thinkwon.blog.csdn.net/article/details/102571883</a></td></tr></tbody></table>

### IO 流

待整理：

File、递归

字节流、字节缓冲流

编码表、编码方式、转换流、序列化、序列化流、打印流、commons-io

### 网络编程

网络概述、网络模型

Socket 原理机制

UDP

TCP/IP

协议、OSI 七层协议、HTTP、HTTP2.0、HTTPS

网络安全

​ XSS、CSRF、SQL 注入、Hash Dos、脚本注入、漏洞扫描工具、验证码

​ DDoS 防范、用户隐私信息保护、序列化漏洞

​ 加密解密、对称加密、哈希算法、非对称加密

​ 服务安全、数据安全、数据备份

​ 网络隔离、登录跳板机、非外网分离

​ 认证、授权

### 常用 API

String、StringBuffer、StringBuilder、正则表达式

Number、Radom、Math、System、包装类

Arrays、Collections

#### 日期时间 API

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java7 日期时间 API</td><td><a href="https://thinkwon.blog.csdn.net/article/details/110777654">https://thinkwon.blog.csdn.net/article/details/110777654</a></td></tr><tr><td>2</td><td>史上最全 Java7 日期时间工具类</td><td><a href="https://thinkwon.blog.csdn.net/article/details/110779441">https://thinkwon.blog.csdn.net/article/details/110779441</a></td></tr><tr><td>3</td><td>Java8 日期时间 API</td><td><a href="https://thinkwon.blog.csdn.net/article/details/111087199">https://thinkwon.blog.csdn.net/article/details/111087199</a></td></tr><tr><td>4</td><td>史上最全 Java8 日期时间工具类</td><td><a href="https://thinkwon.blog.csdn.net/article/details/111116600">https://thinkwon.blog.csdn.net/article/details/111116600</a></td></tr></tbody></table>

### 常用工具类库

待整理：OkHttp、commons-lang3

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>HttpClient 工具类</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101391489">https://thinkwon.blog.csdn.net/article/details/101391489</a></td></tr><tr><td>2</td><td>WGS84 地球坐标系，GCJ02 火星坐标系，BD09 百度坐标系简介与转换</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101392187">https://thinkwon.blog.csdn.net/article/details/101392187</a></td></tr><tr><td>3</td><td>Lombok 简介、使用、工作原理、优缺点</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101392808">https://thinkwon.blog.csdn.net/article/details/101392808</a></td></tr><tr><td>4</td><td>Java 几种常用 JSON 库性能比较</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94354358">https://thinkwon.blog.csdn.net/article/details/94354358</a></td></tr></tbody></table>

### 单元测试

JUnit

### 异常

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java 异常总结</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94346911">https://thinkwon.blog.csdn.net/article/details/94346911</a></td></tr><tr><td>2</td><td>Java 异常架构与异常关键字</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101676779">https://thinkwon.blog.csdn.net/article/details/101676779</a></td></tr><tr><td>3</td><td>Java 异常处理流程</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101677638">https://thinkwon.blog.csdn.net/article/details/101677638</a></td></tr><tr><td>4</td><td>如何选择异常类型</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94346911">https://thinkwon.blog.csdn.net/article/details/94346911</a></td></tr><tr><td>5</td><td>Java 异常常见面试题</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101681073">https://thinkwon.blog.csdn.net/article/details/101681073</a></td></tr><tr><td>6</td><td>Java 异常处理最佳实践</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94347002">https://thinkwon.blog.csdn.net/article/details/94347002</a></td></tr></tbody></table>

### 日志

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>常用日志框架 Log4j，Logback，Log4j2 性能比较与日志门面 SLF4J 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101621135">https://thinkwon.blog.csdn.net/article/details/101621135</a></td></tr><tr><td>2</td><td>日志作用</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101619725">https://thinkwon.blog.csdn.net/article/details/101619725</a></td></tr><tr><td>3</td><td>Apache Log4j2 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/95043111">https://thinkwon.blog.csdn.net/article/details/95043111</a></td></tr><tr><td>4</td><td>Log4j2 同步日志，混合日志和异步日志配置详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101625124">https://thinkwon.blog.csdn.net/article/details/101625124</a></td></tr><tr><td>5</td><td>Log4j2 配置文件详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101629302">https://thinkwon.blog.csdn.net/article/details/101629302</a></td></tr><tr><td>6</td><td>Log4j2 的 Appenders 配置详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101625820">https://thinkwon.blog.csdn.net/article/details/101625820</a></td></tr><tr><td>7</td><td>Log4j2 的 Filters 配置详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101627162">https://thinkwon.blog.csdn.net/article/details/101627162</a></td></tr><tr><td>8</td><td>Log4j2 的 Policy 触发策略与 Strategy 滚动策略配置详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101628222">https://thinkwon.blog.csdn.net/article/details/101628222</a></td></tr><tr><td>9</td><td>Log4j2 的 Loggers 配置详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101628736">https://thinkwon.blog.csdn.net/article/details/101628736</a></td></tr></tbody></table>

### Java8 新特性

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java8 新特性 - Lambda 表达式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/113764085">https://thinkwon.blog.csdn.net/article/details/113764085</a></td></tr><tr><td>2</td><td>Java8 新特性 - Optional</td><td><a href="https://thinkwon.blog.csdn.net/article/details/113791796">https://thinkwon.blog.csdn.net/article/details/113791796</a></td></tr><tr><td>3</td><td>Java8 新特性 - Stream</td><td><a href="https://thinkwon.blog.csdn.net/article/details/113798096">https://thinkwon.blog.csdn.net/article/details/113798096</a></td></tr><tr><td>4</td><td>Java8 新特性 - Base64</td><td><a href="https://thinkwon.blog.csdn.net/article/details/113798575">https://thinkwon.blog.csdn.net/article/details/113798575</a></td></tr><tr><td>5</td><td>Java8 新特性 - 日期时间 API</td><td><a href="https://thinkwon.blog.csdn.net/article/details/111087199">https://thinkwon.blog.csdn.net/article/details/111087199</a></td></tr></tbody></table>

工具
--

### IDEA

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>IDEA 常用配置和常用插件</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101020481">https://thinkwon.blog.csdn.net/article/details/101020481</a></td></tr><tr><td>2</td><td>IDEA 中 Maven 依赖下载失败解决方案</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101312918">https://thinkwon.blog.csdn.net/article/details/101312918</a></td></tr><tr><td>3</td><td>在 IDEA 中使用 Linux 命令</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106320360">https://thinkwon.blog.csdn.net/article/details/106320360</a></td></tr></tbody></table>

### Eclipse & STS

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Eclipse &amp; Spring Tool Suite 常用配置</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101025543">https://thinkwon.blog.csdn.net/article/details/101025543</a></td></tr></tbody></table>

### Maven

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Maven 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94346090">https://thinkwon.blog.csdn.net/article/details/94346090</a></td></tr><tr><td>2</td><td>Maven 安装与配置</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94346569">https://thinkwon.blog.csdn.net/article/details/94346569</a></td></tr><tr><td>3</td><td>Maven 依赖冲突</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101483020">https://thinkwon.blog.csdn.net/article/details/101483020</a></td></tr><tr><td>4</td><td>手动安装 Maven 依赖</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101483478">https://thinkwon.blog.csdn.net/article/details/101483478</a></td></tr><tr><td>5</td><td>Maven 部署 jar 包到远程仓库</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101483769">https://thinkwon.blog.csdn.net/article/details/101483769</a></td></tr><tr><td>6</td><td>Maven 私服 Nexus 安装与使用</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94346681">https://thinkwon.blog.csdn.net/article/details/94346681</a></td></tr></tbody></table>

### Docker

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>使用 Docker 安装 GitLab</td><td><a href="https://thinkwon.blog.csdn.net/article/details/95042797">https://thinkwon.blog.csdn.net/article/details/95042797</a></td></tr><tr><td>2</td><td>虚拟机和容器有什么不同</td><td><a href="https://thinkwon.blog.csdn.net/article/details/107476886">https://thinkwon.blog.csdn.net/article/details/107476886</a></td></tr><tr><td>3</td><td>Docker 从入门到实践系列一 - 什么是 Docker</td><td><a href="https://thinkwon.blog.csdn.net/article/details/107477065">https://thinkwon.blog.csdn.net/article/details/107477065</a></td></tr><tr><td>4</td><td>Docker 从入门到实践系列二 - Docker 安装</td><td><a href="https://thinkwon.blog.csdn.net/article/details/117638107">https://thinkwon.blog.csdn.net/article/details/117638107</a></td></tr><tr><td>5</td><td>Docker 从入门到实践系列三 - Docker 常用命令</td><td><a href="https://thinkwon.blog.csdn.net/article/details/117638128">https://thinkwon.blog.csdn.net/article/details/117638128</a></td></tr><tr><td>6</td><td>Docker 从入门到实践系列四 - Docker 容器编排利器 Docker Compose</td><td><a href="https://thinkwon.blog.csdn.net/article/details/119511551">https://thinkwon.blog.csdn.net/article/details/119511551</a></td></tr></tbody></table>

### Git

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Git 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/94346816">https://thinkwon.blog.csdn.net/article/details/94346816</a></td></tr><tr><td>2</td><td>版本控制</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101449228">https://thinkwon.blog.csdn.net/article/details/101449228</a></td></tr><tr><td>3</td><td>Git 忽略文件. gitignore 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101447866">https://thinkwon.blog.csdn.net/article/details/101447866</a></td></tr><tr><td>4</td><td>Git 与 SVN 的区别</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101449611">https://thinkwon.blog.csdn.net/article/details/101449611</a></td></tr><tr><td>5</td><td>常用 Git 命令</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101450420">https://thinkwon.blog.csdn.net/article/details/101450420</a></td></tr><tr><td>6</td><td>Git，GitHub 与 GitLab 的区别</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101470086">https://thinkwon.blog.csdn.net/article/details/101470086</a></td></tr></tbody></table>

### GitLab

### GitKraken

### Navicat

并发编程
----

### 基础知识

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>并发编程的优缺点</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102020811">https://thinkwon.blog.csdn.net/article/details/102020811</a></td></tr><tr><td>2</td><td>线程的状态和基本操作</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102027115">https://thinkwon.blog.csdn.net/article/details/102027115</a></td></tr><tr><td>3</td><td>进程和线程的区别 (超详细)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102021274">https://thinkwon.blog.csdn.net/article/details/102021274</a></td></tr><tr><td>4</td><td>创建线程的四种方式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102021143">https://thinkwon.blog.csdn.net/article/details/102021143</a></td></tr></tbody></table>

### 并发理论

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java 内存模型</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102073578">https://thinkwon.blog.csdn.net/article/details/102073578</a></td></tr><tr><td>2</td><td>重排序与数据依赖性</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102073858">https://thinkwon.blog.csdn.net/article/details/102073858</a></td></tr><tr><td>3</td><td>as-if-serial 规则和 happens-before 规则的区别</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102074107">https://thinkwon.blog.csdn.net/article/details/102074107</a></td></tr><tr><td>4</td><td>Java 并发理论总结</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102074440">https://thinkwon.blog.csdn.net/article/details/102074440</a></td></tr></tbody></table>

### 并发关键字

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Java 并发关键字 - synchronized</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102243189">https://thinkwon.blog.csdn.net/article/details/102243189</a></td></tr><tr><td>2</td><td>Java 并发关键字 - volatile</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102243670">https://thinkwon.blog.csdn.net/article/details/102243670</a></td></tr><tr><td>3</td><td>Java 并发关键字 - final</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102244477">https://thinkwon.blog.csdn.net/article/details/102244477</a></td></tr></tbody></table>

### Lock 体系

待整理：

公平锁 & 非公平锁

乐观锁 & 悲观锁

可重入锁 & 不可重入锁

互斥锁 & 共享锁

死锁

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Lock 简介与初识 AQS</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102468837">https://thinkwon.blog.csdn.net/article/details/102468837</a></td></tr><tr><td>2</td><td>AQS(AbstractQueuedSynchronizer) 详解与源码分析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102469112">https://thinkwon.blog.csdn.net/article/details/102469112</a></td></tr><tr><td>3</td><td>ReentrantLock(重入锁) 实现原理与公平锁非公平锁区别</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102469388">https://thinkwon.blog.csdn.net/article/details/102469388</a></td></tr><tr><td>4</td><td>读写锁 ReentrantReadWriteLock 源码分析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102469598">https://thinkwon.blog.csdn.net/article/details/102469598</a></td></tr><tr><td>5</td><td>Condition 源码分析与等待通知机制</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102469889">https://thinkwon.blog.csdn.net/article/details/102469889</a></td></tr><tr><td>6</td><td>LockSupport 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102469993">https://thinkwon.blog.csdn.net/article/details/102469993</a></td></tr></tbody></table>

### 并发容器

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>并发容器之 ConcurrentHashMap 详解 (JDK1.8 版本) 与源码分析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102506447">https://thinkwon.blog.csdn.net/article/details/102506447</a></td></tr><tr><td>2</td><td>并发容器之 ConcurrentLinkedQueue 详解与源码分析</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102508089">https://thinkwon.blog.csdn.net/article/details/102508089</a></td></tr><tr><td>3</td><td>并发容器之 CopyOnWriteArrayList 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102508258">https://thinkwon.blog.csdn.net/article/details/102508258</a></td></tr><tr><td>4</td><td>并发容器之 ThreadLocal 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102508381">https://thinkwon.blog.csdn.net/article/details/102508381</a></td></tr><tr><td>5</td><td>ThreadLocal 内存泄漏分析与解决方案</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102508721">https://thinkwon.blog.csdn.net/article/details/102508721</a></td></tr><tr><td>6</td><td>并发容器之 BlockingQueue 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102508901">https://thinkwon.blog.csdn.net/article/details/102508901</a></td></tr><tr><td>7</td><td>并发容器之 ArrayBlockingQueue 与 LinkedBlockingQueue 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102508971">https://thinkwon.blog.csdn.net/article/details/102508971</a></td></tr></tbody></table>

### 线程池

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>线程池 ThreadPoolExecutor 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102541900">https://thinkwon.blog.csdn.net/article/details/102541900</a></td></tr><tr><td>2</td><td>Executors 类创建四种常见线程池</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102541990">https://thinkwon.blog.csdn.net/article/details/102541990</a></td></tr><tr><td>3</td><td>线程池之 ScheduledThreadPoolExecutor 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102542299">https://thinkwon.blog.csdn.net/article/details/102542299</a></td></tr><tr><td>4</td><td>FutureTask 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102542404">https://thinkwon.blog.csdn.net/article/details/102542404</a></td></tr></tbody></table>

### 原子操作类

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>原子操作类总结</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102556910">https://thinkwon.blog.csdn.net/article/details/102556910</a></td></tr></tbody></table>

### 并发工具

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>并发工具之 CountDownLatch 与 CyclicBarrier</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102556958">https://thinkwon.blog.csdn.net/article/details/102556958</a></td></tr><tr><td>2</td><td>并发工具之 Semaphore 与 Exchanger</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102557034">https://thinkwon.blog.csdn.net/article/details/102557034</a></td></tr></tbody></table>

### 并发实践

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>实现生产者消费者的三种方式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102557126">https://thinkwon.blog.csdn.net/article/details/102557126</a></td></tr></tbody></table>

数据结构与算法
-------

### 数据结构

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>红黑树详细分析 (图文详解)，看了都说好</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102571535">https://thinkwon.blog.csdn.net/article/details/102571535</a></td></tr></tbody></table>

```
1、数组
2、栈
3、队列
4、链表
5、树
	二叉树
    完全二叉树
    平衡二叉树
    二叉查找树（BST）
    红黑树
    B，B+，B*树
    LSM 树

字段是不是数据结构


```

### 算法

语言只是编程工具，算法才是编程之魂！

```
1、排序算法：快速排序、归并排序、计数排序
2、搜索算法：回溯、递归、剪枝
3、图论：最短路径、最小生成树、网络流建模
4、动态规划：背包问题、最长子序列、计数问题
5、基础技巧：分治、倍增、二分法、贪心算法

宽度优先搜索
深度优先搜索
广度优先
双指针
扫描线

朴素贝叶斯
推荐算法


```

#### 排序算法

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>史上最全经典排序算法总结 (Java 实现)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/95616819">https://thinkwon.blog.csdn.net/article/details/95616819</a></td></tr><tr><td>2</td><td>冒泡排序（Bubble Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101534473">https://thinkwon.blog.csdn.net/article/details/101534473</a></td></tr><tr><td>3</td><td>选择排序（Selection Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101534721">https://thinkwon.blog.csdn.net/article/details/101534721</a></td></tr><tr><td>4</td><td>插入排序（Insertion Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101537804">https://thinkwon.blog.csdn.net/article/details/101537804</a></td></tr><tr><td>5</td><td>希尔排序（Shell Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101538166">https://thinkwon.blog.csdn.net/article/details/101538166</a></td></tr><tr><td>6</td><td>归并排序（Merge Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101538756">https://thinkwon.blog.csdn.net/article/details/101538756</a></td></tr><tr><td>7</td><td>快速排序（Quick Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101543580">https://thinkwon.blog.csdn.net/article/details/101543580</a></td></tr><tr><td>8</td><td>堆排序（Heap Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101543941">https://thinkwon.blog.csdn.net/article/details/101543941</a></td></tr><tr><td>9</td><td>计数排序（Counting Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101544159">https://thinkwon.blog.csdn.net/article/details/101544159</a></td></tr><tr><td>10</td><td>桶排序（Bucket Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101544356">https://thinkwon.blog.csdn.net/article/details/101544356</a></td></tr><tr><td>11</td><td>基数排序（Radix Sort）</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101545529">https://thinkwon.blog.csdn.net/article/details/101545529</a></td></tr></tbody></table>

### LeetCode

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>LeetCode 第 1 题 两数之和 (Two Sum)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113049">https://thinkwon.blog.csdn.net/article/details/103113049</a></td></tr><tr><td>2</td><td>LeetCode 第 3 题 无重复字符的最长子串 (Longest Substring Without Repeating Characters)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113969">https://thinkwon.blog.csdn.net/article/details/103113969</a></td></tr><tr><td>3</td><td>LeetCode 第 7 题 整数反转 (Reverse Integer)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113167">https://thinkwon.blog.csdn.net/article/details/103113167</a></td></tr><tr><td>4</td><td>LeetCode 第 9 题 回文数 (Palindrome Number)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113151">https://thinkwon.blog.csdn.net/article/details/103113151</a></td></tr><tr><td>5</td><td>LeetCode 第 13 题 罗马数字转整数 (Roman to Integer)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113519">https://thinkwon.blog.csdn.net/article/details/103113519</a></td></tr><tr><td>6</td><td>LeetCode 第 14 题 最长公共前缀 (Longest Common Prefix)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113700">https://thinkwon.blog.csdn.net/article/details/103113700</a></td></tr><tr><td>7</td><td>LeetCode 第 20 题 有效的括号 (Valid Parentheses)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113848">https://thinkwon.blog.csdn.net/article/details/103113848</a></td></tr><tr><td>8</td><td>LeetCode 第 26 题 删除排序数组中的重复项 (Remove Duplicates from Sorted Array)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103113097">https://thinkwon.blog.csdn.net/article/details/103113097</a></td></tr></tbody></table>

数据库
---

### Oracle

### MySQL

#### 数据库基础知识

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>MySQL 语句分类</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106610851">https://thinkwon.blog.csdn.net/article/details/106610851</a></td></tr><tr><td>2</td><td>MySQL 插入语句 insert into,insert ignore into,insert into … on duplicate key update,replace into - 解决唯一键约束</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106610789">https://thinkwon.blog.csdn.net/article/details/106610789</a></td></tr><tr><td>3</td><td>MySQL 复制表的三种方式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106610810">https://thinkwon.blog.csdn.net/article/details/106610810</a></td></tr><tr><td>4</td><td>MySQL 删除表的三种方式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106610831">https://thinkwon.blog.csdn.net/article/details/106610831</a></td></tr><tr><td>5</td><td>MySQL 中 count(字段) ，count(主键 id) ，count(1) 和 count(*) 的区别</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106610859">https://thinkwon.blog.csdn.net/article/details/106610859</a></td></tr></tbody></table>

#### 数据类型

#### 引擎

#### 索引

#### 三大范式

#### 常用 SQL 语句

#### 存储过程与函数

#### 视图

#### MySQL 优化

#### 事务

#### 数据备份与还原

### Redis

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Redis 总结</td><td><a href="https://thinkwon.blog.csdn.net/article/details/99999584">https://thinkwon.blog.csdn.net/article/details/99999584</a></td></tr><tr><td>2</td><td>Redis 使用场景</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101521497">https://thinkwon.blog.csdn.net/article/details/101521497</a></td></tr><tr><td>3</td><td>Redis 数据类型</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101521724">https://thinkwon.blog.csdn.net/article/details/101521724</a></td></tr><tr><td>4</td><td>Redis 持久化</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101522209">https://thinkwon.blog.csdn.net/article/details/101522209</a></td></tr><tr><td>5</td><td>Redis 过期键的删除策略</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101522970">https://thinkwon.blog.csdn.net/article/details/101522970</a></td></tr><tr><td>6</td><td>Redis 数据淘汰策略</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101530624">https://thinkwon.blog.csdn.net/article/details/101530624</a></td></tr><tr><td>7</td><td>Redis 与 Memcached 的区别</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101530406">https://thinkwon.blog.csdn.net/article/details/101530406</a></td></tr><tr><td>8</td><td>Redis 常见面试题 (精简版)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103522351">https://thinkwon.blog.csdn.net/article/details/103522351</a></td></tr><tr><td>9</td><td>Redis 中缓存雪崩、缓存穿透等问题的解决方案</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103402008">https://thinkwon.blog.csdn.net/article/details/103402008</a></td></tr><tr><td>10</td><td>阿里云 Redis 开发规范学习总结</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103400250">https://thinkwon.blog.csdn.net/article/details/103400250</a></td></tr><tr><td>11</td><td>Redis 开发常用规范</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103401781">https://thinkwon.blog.csdn.net/article/details/103401781</a></td></tr><tr><td>12</td><td>这可能是最中肯的 Redis 规范了</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103401978">https://thinkwon.blog.csdn.net/article/details/103401978</a></td></tr></tbody></table>

Java 虚拟机
--------

### 深入理解 Java 虚拟机

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>深入理解 Java 虚拟机 - 走近 Java</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103804387">https://thinkwon.blog.csdn.net/article/details/103804387</a></td></tr><tr><td>2</td><td>深入理解 Java 虚拟机 - Java 内存区域与内存溢出异常</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103827387">https://thinkwon.blog.csdn.net/article/details/103827387</a></td></tr><tr><td>3</td><td>深入理解 Java 虚拟机 - 垃圾回收器与内存分配策略</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103831676">https://thinkwon.blog.csdn.net/article/details/103831676</a></td></tr><tr><td>4</td><td>深入理解 Java 虚拟机 - 虚拟机执行子系统</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103835168">https://thinkwon.blog.csdn.net/article/details/103835168</a></td></tr><tr><td>5</td><td>深入理解 Java 虚拟机 - 程序编译与代码优化</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103835883">https://thinkwon.blog.csdn.net/article/details/103835883</a></td></tr><tr><td>6</td><td>深入理解 Java 虚拟机 - 高效并发</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103836167">https://thinkwon.blog.csdn.net/article/details/103836167</a></td></tr></tbody></table>

架构设计
----

高可用架构

高并发架构

可伸缩架构

集群

### 设计模式

常用设计模式

创建型：  
单例模式、工厂模式、抽象工厂模式

结构型：  
适配器模式、外观模式、代理模式、装饰器模式

行为型：  
观察者模式、策略模式、模板模式

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>设计模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/96829572">https://thinkwon.blog.csdn.net/article/details/96829572</a></td></tr></tbody></table>

#### 创建型模式

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>抽象工厂模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382584">https://thinkwon.blog.csdn.net/article/details/101382584</a></td></tr><tr><td>2</td><td>单例模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382855">https://thinkwon.blog.csdn.net/article/details/101382855</a></td></tr><tr><td>3</td><td>工厂模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383285">https://thinkwon.blog.csdn.net/article/details/101383285</a></td></tr><tr><td>4</td><td>建造者模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383401">https://thinkwon.blog.csdn.net/article/details/101383401</a></td></tr><tr><td>5</td><td>原型模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383491">https://thinkwon.blog.csdn.net/article/details/101383491</a></td></tr></tbody></table>

#### 结构型模式

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>代理模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384436">https://thinkwon.blog.csdn.net/article/details/101384436</a></td></tr><tr><td>2</td><td>过滤器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384514">https://thinkwon.blog.csdn.net/article/details/101384514</a></td></tr><tr><td>3</td><td>桥接模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384584">https://thinkwon.blog.csdn.net/article/details/101384584</a></td></tr><tr><td>4</td><td>适配器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384619">https://thinkwon.blog.csdn.net/article/details/101384619</a></td></tr><tr><td>5</td><td>外观模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384676">https://thinkwon.blog.csdn.net/article/details/101384676</a></td></tr><tr><td>6</td><td>享元模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384716">https://thinkwon.blog.csdn.net/article/details/101384716</a></td></tr><tr><td>7</td><td>装饰器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384753">https://thinkwon.blog.csdn.net/article/details/101384753</a></td></tr><tr><td>8</td><td>组合模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384786">https://thinkwon.blog.csdn.net/article/details/101384786</a></td></tr></tbody></table>

#### 行为型模式

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>备忘录模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383582">https://thinkwon.blog.csdn.net/article/details/101383582</a></td></tr><tr><td>2</td><td>策略模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383647">https://thinkwon.blog.csdn.net/article/details/101383647</a></td></tr><tr><td>3</td><td>迭代器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383722">https://thinkwon.blog.csdn.net/article/details/101383722</a></td></tr><tr><td>4</td><td>访问者模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383780">https://thinkwon.blog.csdn.net/article/details/101383780</a></td></tr><tr><td>5</td><td>观察者模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383872">https://thinkwon.blog.csdn.net/article/details/101383872</a></td></tr><tr><td>6</td><td>解释器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101383930">https://thinkwon.blog.csdn.net/article/details/101383930</a></td></tr><tr><td>7</td><td>空对象模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384001">https://thinkwon.blog.csdn.net/article/details/101384001</a></td></tr><tr><td>8</td><td>命令模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384090">https://thinkwon.blog.csdn.net/article/details/101384090</a></td></tr><tr><td>9</td><td>模板模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384138">https://thinkwon.blog.csdn.net/article/details/101384138</a></td></tr><tr><td>10</td><td>责任链模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384195">https://thinkwon.blog.csdn.net/article/details/101384195</a></td></tr><tr><td>11</td><td>中介者模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384251">https://thinkwon.blog.csdn.net/article/details/101384251</a></td></tr><tr><td>12</td><td>状态模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101384315">https://thinkwon.blog.csdn.net/article/details/101384315</a></td></tr></tbody></table>

#### J2EE 模式

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>MVC 模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101381701">https://thinkwon.blog.csdn.net/article/details/101381701</a></td></tr><tr><td>2</td><td>传输对象模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382134">https://thinkwon.blog.csdn.net/article/details/101382134</a></td></tr><tr><td>3</td><td>服务定位器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382179">https://thinkwon.blog.csdn.net/article/details/101382179</a></td></tr><tr><td>4</td><td>拦截过滤器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382210">https://thinkwon.blog.csdn.net/article/details/101382210</a></td></tr><tr><td>5</td><td>前端控制器模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382247">https://thinkwon.blog.csdn.net/article/details/101382247</a></td></tr><tr><td>6</td><td>数据访问对象模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382287">https://thinkwon.blog.csdn.net/article/details/101382287</a></td></tr><tr><td>7</td><td>业务代表模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382356">https://thinkwon.blog.csdn.net/article/details/101382356</a></td></tr><tr><td>8</td><td>组合实体模式</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101382390">https://thinkwon.blog.csdn.net/article/details/101382390</a></td></tr></tbody></table>

#### 实践应用

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>业务复杂 = if else？刚来的大神竟然用策略 + 工厂彻底干掉了他们！</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102924813">https://thinkwon.blog.csdn.net/article/details/102924813</a></td></tr></tbody></table>

应用框架
----

如何学习一个框架或者技术

*   是什么，简介，概述
    
*   有什么用，用途，使用场景
    
*   怎么用，在实际开发中的应用，注意事项
    
*   优缺点
    
*   框架原理，工作流程，工作原理
    
*   常见面试题
    
*   源码分析，核心类，核心方法，设计模式
    
*   发布博客，在开发和实践中，博客反馈中持续改进
    
*   与同事朋友交流，技术论坛，技术分享中持续丰富知识
    

常用框架

*   集成开发工具（IDE）：Eclipse、MyEclipse、Spring Tool Suite（STS）、Intellij IDEA、NetBeans、JBuilder、JCreator
    
*   JAVA 服务器：tomcat、jboss、websphere、weblogic、resin、jetty、apusic、apache
    
*   负载均衡：nginx、lvs
    
*   web 层框架：Spring MVC、Struts2、Struts1、Google Web Toolkit（GWT）、JQWEB
    
*   服务层框架：Spring、EJB
    
*   持久层框架：Hibernate、MyBatis、JPA、TopLink
    
*   数据库：Oracle、MySql、MSSQL、Redis
    
*   项目构建：maven、ant
    
*   持续集成：Jenkins
    
*   版本控制：SVN、CVS、VSS、GIT
    
*   私服：Nexus
    
*   消息组件：IBM MQ、RabbitMQ、ActiveMQ、RocketMq
    
*   日志框架：Commons Logging、log4j 、slf4j、IOC
    
*   缓存框架：memcache、redis、ehcache、jboss cache
    
*   RPC 框架：Hessian、Dubbo
    
*   规则引擎：Drools
    
*   工作流：Activiti
    
*   批处理：Spring Batch
    
*   通用查询框架：Query DSL
    
*   JAVA 安全框架：shiro、Spring Security
    
*   代码静态检查工具：FindBugs、PMD
    
*   Linux 操作系统：CentOS、Ubuntu、SUSE Linux、
    
*   常用工具：PLSQL Developer（Oracle）、Navicat（MySql）、FileZilla（FTP）、Xshell（SSH）、putty（SSH）、SecureCRT（SSH）、jd-gui（反编译）
    

### Spring

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Spring 简介、设计理念、优缺点、应用场景</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102810748">https://thinkwon.blog.csdn.net/article/details/102810748</a></td></tr><tr><td>2</td><td>Spring 模块组成 (框架组成、整体架构、体系架构、体系结构)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102810819">https://thinkwon.blog.csdn.net/article/details/102810819</a></td></tr><tr><td>3</td><td>Spring 容器中 bean 的生命周期</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102866432">https://thinkwon.blog.csdn.net/article/details/102866432</a></td></tr><tr><td>4</td><td>控制反转 (IoC) 与依赖注入 (DI) 详解</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102912332">https://thinkwon.blog.csdn.net/article/details/102912332</a></td></tr></tbody></table>

#### 《Spring 实战》读书笔记

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>《Spring 实战》读书笔记 - 第 1 章 Spring 之旅</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103097364">https://thinkwon.blog.csdn.net/article/details/103097364</a></td></tr><tr><td>2</td><td>《Spring 实战》读书笔记 - 第 2 章 装配 Bean</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103527675">https://thinkwon.blog.csdn.net/article/details/103527675</a></td></tr><tr><td>3</td><td>《Spring 实战》读书笔记 - 第 3 章 高级装配</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103536621">https://thinkwon.blog.csdn.net/article/details/103536621</a></td></tr><tr><td>4</td><td>《Spring 实战》读书笔记 - 第 4 章 面向切面的 Spring</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103541166">https://thinkwon.blog.csdn.net/article/details/103541166</a></td></tr><tr><td>5</td><td>《Spring 实战》读书笔记 - 第 5 章 构建 Spring Web 应用程序</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103550083">https://thinkwon.blog.csdn.net/article/details/103550083</a></td></tr><tr><td>6</td><td>《Spring 实战》读书笔记 - 第 6 章 渲染 Web 视图</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103559672">https://thinkwon.blog.csdn.net/article/details/103559672</a></td></tr><tr><td>7</td><td>《Spring 实战》读书笔记 - 第 7 章 Spring MVC 的高级技术</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103562467">https://thinkwon.blog.csdn.net/article/details/103562467</a></td></tr></tbody></table>

### Spring MVC

### MyBatis

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>MyBatis 官方文档</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887995">https://thinkwon.blog.csdn.net/article/details/100887995</a></td></tr><tr><td>2</td><td>MyBatis 官方文档 - 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887076">https://thinkwon.blog.csdn.net/article/details/100887076</a></td></tr><tr><td>3</td><td>MyBatis 官方文档 - 入门</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887176">https://thinkwon.blog.csdn.net/article/details/100887176</a></td></tr><tr><td>4</td><td>MyBatis 官方文档 - XML 配置</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887349">https://thinkwon.blog.csdn.net/article/details/100887349</a></td></tr><tr><td>5</td><td>MyBatis 官方文档 - XML 映射文件</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887478">https://thinkwon.blog.csdn.net/article/details/100887478</a></td></tr><tr><td>6</td><td>MyBatis 官方文档 - 动态 SQL</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887702">https://thinkwon.blog.csdn.net/article/details/100887702</a></td></tr><tr><td>7</td><td>MyBatis 官方文档 - Java API</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887746">https://thinkwon.blog.csdn.net/article/details/100887746</a></td></tr><tr><td>8</td><td>MyBatis 官方文档 - SQL 语句构建器类</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887821">https://thinkwon.blog.csdn.net/article/details/100887821</a></td></tr><tr><td>9</td><td>MyBatis 官方文档 - 日志</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100887951">https://thinkwon.blog.csdn.net/article/details/100887951</a></td></tr><tr><td>10</td><td>MyBatis 功能架构</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101295025">https://thinkwon.blog.csdn.net/article/details/101295025</a></td></tr><tr><td>11</td><td>MyBatis 工作原理</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101293609">https://thinkwon.blog.csdn.net/article/details/101293609</a></td></tr><tr><td>12</td><td>MyBatis 核心类</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101293216">https://thinkwon.blog.csdn.net/article/details/101293216</a></td></tr><tr><td>13</td><td>MyBatis 面试宝典</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101292950">https://thinkwon.blog.csdn.net/article/details/101292950</a></td></tr><tr><td>14</td><td>MyBatis 实现一对一，一对多关联查询</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101322334">https://thinkwon.blog.csdn.net/article/details/101322334</a></td></tr><tr><td>15</td><td>MyBatis 缓存</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101351212">https://thinkwon.blog.csdn.net/article/details/101351212</a></td></tr></tbody></table>

#### MyBatis 源码分析

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>MyBatis 源码分析 - MyBatis 入门</td><td><a href="https://thinkwon.blog.csdn.net/article/details/114808852">https://thinkwon.blog.csdn.net/article/details/114808852</a></td></tr><tr><td>2</td><td>MyBatis 源码分析 - 配置文件解析过程</td><td><a href="https://thinkwon.blog.csdn.net/article/details/114808962">https://thinkwon.blog.csdn.net/article/details/114808962</a></td></tr><tr><td>3</td><td>MyBatis 源码分析 - 映射文件解析过程</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115423167">https://thinkwon.blog.csdn.net/article/details/115423167</a></td></tr><tr><td>4</td><td>MyBatis 源码分析 - SQL 的执行过程</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115603376">https://thinkwon.blog.csdn.net/article/details/115603376</a></td></tr><tr><td>5</td><td>MyBatis 源码分析 - 内置数据源</td><td><a href="https://thinkwon.blog.csdn.net/article/details/116331419">https://thinkwon.blog.csdn.net/article/details/116331419</a></td></tr><tr><td>6</td><td>MyBatis 源码分析 - 缓存原理</td><td><a href="https://thinkwon.blog.csdn.net/article/details/116809942">https://thinkwon.blog.csdn.net/article/details/116809942</a></td></tr><tr><td>7</td><td>MyBatis 源码分析 - 插件机制</td><td><a href="https://thinkwon.blog.csdn.net/article/details/116809961">https://thinkwon.blog.csdn.net/article/details/116809961</a></td></tr></tbody></table>

### Quartz

<table><thead><tr><th align="left">序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td align="left">1</td><td>Quartz 简介</td><td><a href="https://thinkwon.blog.csdn.net/article/details/109936696">https://thinkwon.blog.csdn.net/article/details/109936696</a></td></tr><tr><td align="left"></td><td></td><td></td></tr></tbody></table>

### Hibernate

### Shiro

### Spring Security

### Netty

### 搜索引擎

#### Lucene/Solr

#### Elasticsearch

#### ELK

中间件
---

### 消息中间件

#### RabbitMQ

#### RocketMQ

#### ActiveMQ

#### Kafka

### 远程过程调用中间件

#### Dubbo

### 数据访问中间件

Sharding JDBC

MyCat

### Web 应用服务器

#### Tomcat

待整理：Tomcat 各组件作用 Tomcat 集群 Tomcat 面试题

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Win10 安装 Tomcat 服务器与配置环境变量</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102622905">https://thinkwon.blog.csdn.net/article/details/102622905</a></td></tr><tr><td>2</td><td>Linux(CentOS7) 安装 Tomcat 与设置 Tomcat 为开机启动项</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102717537">https://thinkwon.blog.csdn.net/article/details/102717537</a></td></tr><tr><td>3</td><td>Tomcat 与 JDK 版本对应关系，Tomcat 各版本特性</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102622738">https://thinkwon.blog.csdn.net/article/details/102622738</a></td></tr><tr><td>4</td><td>Tomcat 目录结构</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102619466">https://thinkwon.blog.csdn.net/article/details/102619466</a></td></tr><tr><td>5</td><td>Tomcat 乱码与端口占用的解决方案</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102622824">https://thinkwon.blog.csdn.net/article/details/102622824</a></td></tr><tr><td>6</td><td>Tomcat 系统架构与请求处理流程</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102676442">https://thinkwon.blog.csdn.net/article/details/102676442</a></td></tr><tr><td>7</td><td>史上最强 Tomcat8 性能优化</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102744033">https://thinkwon.blog.csdn.net/article/details/102744033</a></td></tr></tbody></table>

#### Nginx

### 缓存

本地缓存

客户端缓存

服务端缓存

​ web 缓存，Redis，Memcached，Ehcache

### 其他

#### Zookeeper

微服务与分布式
-------

### Spring Boot

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>application.yml 与 bootstrap.yml 的区别</td><td><a href="https://thinkwon.blog.csdn.net/article/details/100007093">https://thinkwon.blog.csdn.net/article/details/100007093</a></td></tr><tr><td>2</td><td>一分钟了解约定优于配置</td><td><a href="https://thinkwon.blog.csdn.net/article/details/101703815">https://thinkwon.blog.csdn.net/article/details/101703815</a></td></tr></tbody></table>

### Spring Cloud

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Spring Cloud 入门 - 十分钟了解 Spring Cloud</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103715146">https://thinkwon.blog.csdn.net/article/details/103715146</a></td></tr><tr><td>2</td><td>Spring Cloud 入门 - Eureka 服务注册与发现 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103726655">https://thinkwon.blog.csdn.net/article/details/103726655</a></td></tr><tr><td>3</td><td>Spring Cloud 入门 - Ribbon 服务消费者 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103729080">https://thinkwon.blog.csdn.net/article/details/103729080</a></td></tr><tr><td>4</td><td>Spring Cloud 入门 - Hystrix 断路器 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103732497">https://thinkwon.blog.csdn.net/article/details/103732497</a></td></tr><tr><td>5</td><td>Spring Cloud 入门 - Hystrix Dashboard 与 Turbine 断路器监控 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103734664">https://thinkwon.blog.csdn.net/article/details/103734664</a></td></tr><tr><td>6</td><td>Spring Cloud 入门 - OpenFeign 服务消费者 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103735751">https://thinkwon.blog.csdn.net/article/details/103735751</a></td></tr><tr><td>7</td><td>Spring Cloud 入门 - Zuul 服务网关 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103738851">https://thinkwon.blog.csdn.net/article/details/103738851</a></td></tr><tr><td>8</td><td>Spring Cloud 入门 - Config 分布式配置中心 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103739628">https://thinkwon.blog.csdn.net/article/details/103739628</a></td></tr><tr><td>9</td><td>Spring Cloud 入门 - Bus 消息总线 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103753372">https://thinkwon.blog.csdn.net/article/details/103753372</a></td></tr><tr><td>10</td><td>Spring Cloud 入门 - Sleuth 服务链路跟踪 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103753896">https://thinkwon.blog.csdn.net/article/details/103753896</a></td></tr><tr><td>11</td><td>Spring Cloud 入门 - Consul 服务注册发现与配置中心 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103756139">https://thinkwon.blog.csdn.net/article/details/103756139</a></td></tr><tr><td>12</td><td>Spring Cloud 入门 - Gateway 服务网关 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103757927">https://thinkwon.blog.csdn.net/article/details/103757927</a></td></tr><tr><td>13</td><td>Spring Cloud 入门 - Admin 服务监控中心 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103758697">https://thinkwon.blog.csdn.net/article/details/103758697</a></td></tr><tr><td>14</td><td>Spring Cloud 入门 - Oauth2 授权的使用 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103761687">https://thinkwon.blog.csdn.net/article/details/103761687</a></td></tr><tr><td>15</td><td>Spring Cloud 入门 - Oauth2 授权之 JWT 集成 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103763364">https://thinkwon.blog.csdn.net/article/details/103763364</a></td></tr><tr><td>16</td><td>Spring Cloud 入门 - Oauth2 授权之基于 JWT 完成单点登录 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103766368">https://thinkwon.blog.csdn.net/article/details/103766368</a></td></tr><tr><td>17</td><td>Spring Cloud 入门 - Nacos 实现注册和配置中心 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103769680">https://thinkwon.blog.csdn.net/article/details/103769680</a></td></tr><tr><td>18</td><td>Spring Cloud 入门 - Sentinel 实现服务限流、熔断与降级 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103770879">https://thinkwon.blog.csdn.net/article/details/103770879</a></td></tr><tr><td>19</td><td>Spring Cloud 入门 - Seata 处理分布式事务问题 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103786102">https://thinkwon.blog.csdn.net/article/details/103786102</a></td></tr><tr><td>20</td><td>Spring Cloud 入门 - 汇总篇 (Hoxton 版本)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103786588">https://thinkwon.blog.csdn.net/article/details/103786588</a></td></tr></tbody></table>

### 服务注册发现

### 服务配置

### 负载均衡

### 服务调用

### 服务限流

### 熔断降级

### 网关路由

### 服务权限

### 链路追踪

### 分布式事务

### 分布式缓存

### 分布式会话

### 日志收集

### 服务监控

### 消息驱动

### 数据处理流

### 自动化测试与部署

### 第三方支持

### 分布式协调服务 Zookeeper

程序员的一些思考
--------

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>程序员写个人技术博客的价值与意义</td><td><a href="https://thinkwon.blog.csdn.net/article/details/102980571">https://thinkwon.blog.csdn.net/article/details/102980571</a></td></tr><tr><td>2</td><td>Java 知识体系最强总结 (2020 版)</td><td><a href="https://thinkwon.blog.csdn.net/article/details/103592572">https://thinkwon.blog.csdn.net/article/details/103592572</a></td></tr><tr><td>3</td><td>博客之星，有你的鼓励更精彩</td><td><a href="https://thinkwon.blog.csdn.net/article/details/112517796">https://thinkwon.blog.csdn.net/article/details/112517796</a></td></tr></tbody></table>

团队与项目管理
-------

### 需求调研

### 项目管理

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Worktile、Teambition 与 Tower 项目管理软件对比</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106064807">https://thinkwon.blog.csdn.net/article/details/106064807</a></td></tr></tbody></table>

### 代码管理

### 文档管理

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>几款常见接口管理平台对比</td><td><a href="https://thinkwon.blog.csdn.net/article/details/106064883">https://thinkwon.blog.csdn.net/article/details/106064883</a></td></tr><tr><td>2</td><td>Swagger2 常用注解说明</td><td><a href="https://thinkwon.blog.csdn.net/article/details/107477801">https://thinkwon.blog.csdn.net/article/details/107477801</a></td></tr></tbody></table>

### 测试

Python
------

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>Win10 安装 Python3.9</td><td><a href="https://thinkwon.blog.csdn.net/article/details/112411897">https://thinkwon.blog.csdn.net/article/details/112411897</a></td></tr><tr><td>2</td><td>Anaconda 安装</td><td><a href="https://thinkwon.blog.csdn.net/article/details/112412165">https://thinkwon.blog.csdn.net/article/details/112412165</a></td></tr><tr><td>3</td><td>PyCharm2020.3.2 安装</td><td><a href="https://thinkwon.blog.csdn.net/article/details/112412497">https://thinkwon.blog.csdn.net/article/details/112412497</a></td></tr><tr><td>4</td><td>PyCharm 常用配置和常用插件</td><td><a href="https://thinkwon.blog.csdn.net/article/details/112412783">https://thinkwon.blog.csdn.net/article/details/112412783</a></td></tr></tbody></table>

运维
--

常规监控

APM

持续集成 (CI/CD)：Jenkins，环境分离

自动化运维：Ansible，puppet，chef

测试：TDD 理论，单元测试，压力测试，全链路压测，A/B 、灰度、蓝绿测试

虚拟化：KVM，Xen，OpenVZ

容器技术：Docker

云技术：OpenStack

DevOps

操作系统
----

计算机操作系统

计算机原理

Linux

CPU

进程，线程，协程

### CentOS8

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>VMware Workstation Pro 16 搭建 CentOS8 虚拟机集群</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115058171">https://thinkwon.blog.csdn.net/article/details/115058171</a></td></tr><tr><td>2</td><td>CentOS8 安装 Docker</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115056214">https://thinkwon.blog.csdn.net/article/details/115056214</a></td></tr><tr><td>3</td><td>CentOS8 搭建 Nacos1.4.0 集群</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115056401">https://thinkwon.blog.csdn.net/article/details/115056401</a></td></tr><tr><td>4</td><td>CentOS8 安装 GitLab13.7.2</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115056528">https://thinkwon.blog.csdn.net/article/details/115056528</a></td></tr><tr><td>5</td><td>CentOS8 安装 MySQL8</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115055934">https://thinkwon.blog.csdn.net/article/details/115055934</a></td></tr></tbody></table>

推荐书籍
----

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>读书清单 - 计算机</td><td><a href="https://thinkwon.blog.csdn.net/article/details/108077754">https://thinkwon.blog.csdn.net/article/details/108077754</a></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

读书笔记
----

<table><thead><tr><th>序号</th><th>内容</th><th>链接地址</th></tr></thead><tbody><tr><td>1</td><td>高效休息法 - 读书笔记</td><td><a href="https://thinkwon.blog.csdn.net/article/details/118638191">https://thinkwon.blog.csdn.net/article/details/118638191</a></td></tr><tr><td>2</td><td>斯坦福高效睡眠法 - 读书笔记</td><td><a href="https://thinkwon.blog.csdn.net/article/details/108349844">https://thinkwon.blog.csdn.net/article/details/108349844</a></td></tr><tr><td>3</td><td>高效能人士的七个习惯 - 读书笔记</td><td><a href="https://thinkwon.blog.csdn.net/article/details/108941111">https://thinkwon.blog.csdn.net/article/details/108941111</a></td></tr><tr><td>4</td><td>富爸爸穷爸爸 - 读书笔记</td><td><a href="https://thinkwon.blog.csdn.net/article/details/109261723">https://thinkwon.blog.csdn.net/article/details/109261723</a></td></tr><tr><td>5</td><td>如何阅读一本书 - 读书笔记</td><td><a href="https://thinkwon.blog.csdn.net/article/details/115422659">https://thinkwon.blog.csdn.net/article/details/115422659</a></td></tr><tr><td>6</td><td>人性的弱点 - 读书笔记</td><td><a href="https://thinkwon.blog.csdn.net/article/details/116809824">https://thinkwon.blog.csdn.net/article/details/116809824</a></td></tr><tr><td>7</td><td>麦肯锡极简工作法 - 读书笔记</td><td><a href="https://thinkwon.blog.csdn.net/article/details/118638191">https://thinkwon.blog.csdn.net/article/details/118638191</a></td></tr><tr><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

云计算
---

IaaS、SaaS、PaaS、虚拟化技术、openstack、Serverlsess

搜索引擎
----

Solr、Lucene、Nutch、Elasticsearch

权限管理
----

Shiro、Spring Security

区块链
---

哈希算法、Merkle 树、公钥密码算法、共识算法、Raft 协议、Paxos 算法与 Raft 算法、拜占庭问题与算法、消息认证码与数字签名