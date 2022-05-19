> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [dev.koal.com](https://dev.koal.com/wiki/index.php/StudyGuide#.E7.BC.96.E7.A8.8B)

本文档的目的
------

本文档的主要读者是刚参加工作不久的研发岗位人员，也适合新加入公司的高级研发人员。

本文档的目的是为了系统地展现部门研发所需的技能图谱，并列出关键的知识点和学习方向，希望这份文档能为读者提供以下帮助：

*   尽快地了解日常工作可能涉及的理论和知识。
*   便于进行中长期的职业规划。

如何使用本文档
-------

本文档的几个大章节之间并无依赖关系，可以从任何一个开始或并行阅读。

建议的学习过程如下：

*   阅读——根据每章节中列出的知识点和书目，进行广泛的阅读，要让自己的学习节奏比学校阶段更快而不是更慢。对于还未承担家庭责任的员工，建议一年至少看完 20 本书——每两周一本或更多。
    *   学会 google 而不是 baidu。
    *   学会找到真正的好书并读完。
    *   如果对一门知识还没有系统地学习过，优先看书而不是看网页。
*   实践——阅读实际项目的代码和自己动手都是很好的实践方法，也能帮你更快地吸收上一阶段的精华。
*   重构——尝试把自己的理解完整地写下来，甚至是对其他人进行一次培训或讲解，都能帮助你上升到一个更高的阶段。只靠一支笔和白板把一项技术讲清楚的时候，才是真正掌握的时候。

能获得哪些外部帮助？
----------

*   部门的每个其他同事都是你的老师，但如果你问的东西他也不会，也不用惊讶，每个人都有自己的长处，学习是长期持续的事情。
*   公司工作多年的老员工都是你的学习对象，可能他们由于手头的事情比较多一时不能详细回答你的问题，但多试几次你不会空手而回的。
*   如果你觉得某一本书很有价值，也希望推荐给部门其他人看，请果断买下并找部门经理报销费用。

技能图谱
----

目前本部门研发涉及的技能可以归结为以下 4 个方面：

*   方法论——包括自我管理，团队协作等。
*   网络——尤其是链路层以上部分的网络。
*   安全——尤其是 PKI 相关的安全。
*   编程——尤其是 C/C++/Java 相关的编程。

每个方面都有完整的技能树，学无止境，本文档只能覆盖比较适合入门者的部分，更高级的部分需要每个人根据自己的特点和职业规划自行确定。

在此仅列出对技术工作有价值的方法。

自我管理
----

### 知识管理

推荐使用 OneNote，Evernote 或类似的笔记软件来对自己的技术知识进行管理，包括有价值网页的收藏和日常工作的心得和记录，比如一次程序崩溃的截屏，一段奇怪的日志或抓包结果，一套很不容易完成的配置，一个开源程序的编译安装过程：

知识管理是一项日积月累的工作，但持续时间越长，你的职业生涯收益就越多。

### 时间管理

时间管理比知识管理更难做到，但随着你承担的事情越来越多，你的时间就越不够用。不过分地说，养成良好的时间管理习惯可以决定你的生活质量。

*   高大上的介绍：[http://baike.baidu.com/view/102959.htm](http://baike.baidu.com/view/102959.htm) -
*   更实际的说法：[http://meroa.com/about-gtd/](http://meroa.com/about-gtd/)
*   个人推荐：[https://github.com/lifesinger/lifesinger.github.com/issues/120](https://github.com/lifesinger/lifesinger.github.com/issues/120)
*   简单的实施办法：[http://baike.baidu.com/view/5259318.htm](http://baike.baidu.com/view/5259318.htm)

时间管理没有固定的方法，选择适合自己的方法并坚持下来就是正确的。

团队协作
----

编程可以视作你与计算机之间的沟通，但产品和系统不是由你一个人完成的，所以还必须习惯在团队中的沟通。有关团队协作的文章和观点非常丰富，在这篇文档里只重点指出下面 3 条：

### 学会提问

提问并不代表你的能力比对方差，问出一个好的问题，对于回答者也是非常有收获的。

*   学会如何问问题：[http://coolshell.cn/articles/3713.html](http://coolshell.cn/articles/3713.html)

### 学会理解别人的想法

理解别人的想法很难，这个世界本身就存在很多无法沟通的事实，但多下点功夫在这上面，对自己的和别人都有好处。

### 学会表达自己的想法

了解并理解他人的想法不是一件简单的事，因为你很难预测和控制其他人，所以能准确，合理地表达自己的想法是一件非常重要的事。

以下这些情况，都有表达的必要。

*   任务完不成了。
*   我觉得应该 / 不应该做某件事。
*   我打算如何实现这个功能。
*   我认为这个设计非常糟糕，无法赞同。
*   和我原先的设想有偏差，我得换一种方法了。
*   我忙不过来了。
*   我没法理解这个想法，听不懂。

下面都是在公司项目中实际发生过的真实事件：

*   在一个项目的后期，TeamLeader 自认为工作非常辛苦，但其他人都不知道他在干什么，也不知道自己该干什么。
*   某程序员花了一周时间，实现了一个现有项目中公共类已经实现的功能。

表达的时候，需要注意这几点原则：

*   自己表达得是否完整，准确？——如果是比较复杂的设计或方案，建议自己先列一个基本的提纲，或者用思维导图整理一下思路；如果是面对多个听众的，不妨自己先试讲一遍；
*   按照对方的能力和掌握的知识，能听懂吗——适当地停顿，问一下对方的看法；如果需要讲的东西内容比较长，建议先说结论，再说中心思想，最后进行细节展开。
*   是口头表达好，还是书面表达或者画图好？
*   纸笔或白板是最好的工具。
*   学会使用思维导图工具，比如 freemind。
*   已经成型的设计，可以用 Visio 绘制包含细节的图。
*   熟练地使用 Word。
*   必要时学一点 Excel 和 Powerpoint。

公司目前产品在信息安全领域主要侧重于身份认证与访问控制，理论基础是密码学与 PKI。其他常见的安全技术比如 Web 渗透，防病毒，入侵检测等在现有产品中涉及不多。

PKI 这个领域的书籍不多，比较系统的仍然是《应用密码学》中公钥密码相关的部分。建议结合书本和实践逐步掌握以下概念和理论：

*   理解 “密钥” 与日常应用中 “密码” 的区别。
*   对称算法：DES，AES，RC4，理解分组密码算法和序列密码在使用上的区别。
*   非对称算法：RSA，ECC。
*   摘要算法：MD5，SHA1。
*   掌握 RSA 数字签名和信封的具体原理。
*   掌握 X509 数字证书的结构，签发原理，生命周期管理。
*   理解双证书的概念。
*   商用密码算法 SM1，SM2，SM3，SM4。
*   证书黑名单，LDAP 和 OCSP。

*   有关 PKI 比较全面的视频教程可以学习公司 2016 年的 PKI 体系培训资料 > \\debian.koal.com6_培训资料 (2016)
*   除了这些概念外，SSL 协议是目前产品技术中最重要的协议，需要深入理解，包括所有握手过程的数据包内容，处理机制等。

```
有关SSL相关技术的深入学习可以参考这篇索引：http://git.koal.com/training/gw-training/wikis/openssl


```

推荐阅读
----

*   《应用密码学》[http://book.douban.com/subject/1088180/](http://book.douban.com/subject/1088180/)
*   《信息安全工程》[http://book.douban.com/subject/1088180/](http://book.douban.com/subject/1088180/)
*   公司 Wiki 中 SSL 相关的几本书籍 [http://wiki.koal.com/wiki/index.php/%E5%88%86%E7%B1%BB:OpenSSL-DEV](http://wiki.koal.com/wiki/index.php/%E5%88%86%E7%B1%BB:OpenSSL-DEV)
*   A Layman's Guide to a Subset of ASN.1, BER, and DER [http://infosec.pku.edu.cn/~tly/courses/0C606/layman.pdf](http://infosec.pku.edu.cn/~tly/courses/0C606/layman.pdf)
*   TLS 1.2 协议规范 http://tools.ietf.org/html/rfc5246
*   X509 标准 [http://tools.ietf.org/html/rfc5280](http://tools.ietf.org/html/rfc5280)
*   OpenSSL 源代码
*   Golang 中 TLS 相关代码
*   BouncyCastle 代码
*   SSL 握手协议详解 smb://debian.koal.com/upload/chenzhefeng/ssl_training/SSL 握手协议详解

推荐的实践（略简单，因为复杂的实践会大量在项目和产品开发中涉及）
--------------------------------

*   使用 OpenSSL 命令行工具搭建一个 CA 并签发一张用户证书，要求其中 5 项与公司证书完全相同（序列号，系列号，起始有效期，终止有效期，公钥）。
*   使用 OpenSSL 命令提供的功能，手动解密公司的加密邮件。
*   使用 OpenSSL 库函数或 Bouncycastle 实现上面的功能。
*   基于 OpenSSL 库或 Bouncycastle 实现一个自定义的数字信封（不必封装为 PKCS#7 格式）。
*   编程实现 LDAP 方式的 CRL 下载（使用公司证书对应的 CRL 发布点）。
*   使用 Wireshark 分析 IE 与 Chrome 访问公司 CRM 时 SSL 握手过程的区别。
*   修改一下 OpenSSL，使其能利用 Heartbleed 漏洞，获取远端服务器的内存信息。
*   尝试自己根据规范实现一下 SM3 或 SM4 算法。

目前部门的主要研发工作主要是侧重于应用层的，因此对于通信网络比如 GSM/CDMA 等基本不涉及。我们目前主要的工作重点在 4 部分：

*   SSL 及相关的应用层代理实现，尤其是 HTTP/HTTPS。
*   Linux 内核对 TCP/IP 的处理，包括路由，NAT 等。
*   经常涉及的一些协议，比如 ARP/RARP，DNS，FTP，NTP，SNMP 等。
*   其他安全相关的协议，比如 802.1x，IPSEC。

推荐阅读
----

*   《深入理解计算机系统》 [http://book.douban.com/subject/1230413/](http://book.douban.com/subject/1230413/)
*   《计算机网络》[http://book.douban.com/subject/10510747/](http://book.douban.com/subject/10510747/)
*   《TCP/IP 详解卷 1：协议》[http://book.douban.com/subject/1088054/](http://book.douban.com/subject/1088054/)
*   《深入理解 LINUX 网络内幕》[http://book.douban.com/subject/1834459/](http://book.douban.com/subject/1834459/)
*   《Linux 网络安全技术与实现》 [http://book.douban.com/subject/10577937/](http://book.douban.com/subject/10577937/)
*   《TCP/IP 协议族》 [http://book.douban.com/subject/5386194/](http://book.douban.com/subject/5386194/)
*   《UNIX 网络编程》[http://book.douban.com/subject/1231567/](http://book.douban.com/subject/1231567/)
*   《HTTP 权威指南》[http://book.douban.com/subject/10746113/](http://book.douban.com/subject/10746113/)
*   《HTTPS 权威指南》[https://book.douban.com/subject/26869219/](https://book.douban.com/subject/26869219/)
*   Berkeley 的《Web Architecture》课程（没有录像，但是有幻灯片和作业）：
*   [http://courses.ischool.berkeley.edu/i253/f11/](http://courses.ischool.berkeley.edu/i253/f11/)
*   [http://jblomo.github.io/webarch253/](http://jblomo.github.io/webarch253/)
*   HTTP 协议标准 [http://tools.ietf.org/html/rfc2616](http://tools.ietf.org/html/rfc2616)
*   WEB 相关入门教程 [http://www.w3school.com.cn/](http://www.w3school.com.cn/)
*   Linux 内核 TCP/IP 栈相关代码，netfilter 相关代码。
*   Apache HTTP Server 源代码。

需要掌握的工具和技能
----------

*   wireshark/tcpdump，HttpWatch，以及 IE/Firefox/Chrome 等自带的 HTTP 调试。
*   ping/host/curl/iproute2/iptables
*   Linux 下 strace 和 lsof 工具的使用
*   Linux 下的 SYSLOG 机制（发送，接收，过滤，转发）
*   常见 WebServer（httpd/nginx/IIS/tomcat）的配置
*   使用 python 模拟 HTTP 服务端和客户端

### 推荐的实践：

*   使用 Wireshark 分析一种应用层协议的数据包（比如：结合 NTP 协议的相关文档，分析 Windows 时间同步的数据包）。
*   使用 Linux 搭建一个基于静态路由的网络，网段数目大于 3 个（练习永远使用 iproute2 配置路由，而不是用 route 命令来配置）。
*   理解并配置 NAT（包括 SNAT/DNAT），对公司 DNS 进行端口映射。
*   配置 Linux 上的 Brigde 和 Bonding。
*   阅读 Linux 内核代码中对应 Socket 调用 send 部分的实现代码。
*   基于开源软件搭建各种 VPN（包括 IPSEC，PPP，L2TP 等）并分析其原理。
*   找一台 CISCO 或华为的设备配置 VLAN 和 NAT，有条件的话，可以尝试一下 802.1x。
*   使用 simpletun 或其他的隧道技术将公司机器路由到别处，比如家里的电脑。
*   实践各操作系统与高端网卡上的协议卸载机制，比如微软 TCP 烟囱卸载。
*   为 Linux 实现一个类似交换机的镜像端口机制。
*   使用 sysctl 配置内核网络相关项配置，如 timestamp，arp_ignore，tcp_fin_timeout，tcp_tw_recycle，tcp_tw_reuse。
*   尝试搞清楚 netstat ?s 中各项的由来，尤其是 TCP 相关的。
*   理解网卡驱动的功能参数配置及含义，用 ethool 折腾一下。
*   尝试使用以下这些工具获取系统的状态：sysstat，iostat，vmstat。有兴趣可以看一下代码实现。
*   阅读 wget 或 curl 源代码中关于 HTTP Header 处理的实现代码。
*   使用 Apache 或 Nginx 搭建反向代理，代理 wiki.koal.com 并正确处理 302 重定向。
*   编程模拟访问一个需要登录的网站页面（比如 weibo，CSDN，github，公司 CRM），可以采用 python，php 等语言。

部门主要用的编程语言比较广泛，首选仍然是 C/C++ 和 Java，但一般都会有辅助类的其他语言如 PHP，Python 等。当然还有一些比较新的语言如 Go，Ruby，Erlang 等在实际产品中还没有用到，有兴趣的话了解一下也很好。

*   BASH：不解释
*   C：OpenSSL，Apache，Nginx，Linux Kernel 的开发语言
*   C++：Windows 开发必备
*   Java：Web 相关产品及 API 中使用
*   JavaScript：在我部门的业务中，经常需要处理 HTTP 及相关的 WEB 页面，JavaScript 也是无法绕开的一门语言。
*   Pascal：客户端安装包打包程序 InnoSetup 使用的内置脚本语言
*   PHP：部门服务端产品使用的 WEB 管理界面开发语言，PHP 与 Apache，OpenSSL 有千丝万缕的联系，是我们绕不开的一门语言。
*   Python：客户端经常使用的粘合性语言，我部门使用不多，但其他部门使用比较广泛，从提高客户端开发效率上来说，这也是一门必备的语言。
*   Golang：部门服务端产品常用的开发语言

关于这些语言的相关书籍和技术资料非常丰富，不在此累述。掌握 2-3 门语言的开发能力，对拓展设计思路非常有帮助，对语言的掌握深度决定了程序员的表达能力，能帮助你准确、快速实现各种技术想法。

NewPP limit report Cached time: 20220519053636 Cache expiry: 86400 Dynamic content: false CPU time usage: 0.012 seconds Real time usage: 0.012 seconds Preprocessor visited node count: 82/1000000 Preprocessor generated node count: 88/1000000 Post‐expand include size: 0/2097152 bytes Template argument size: 0/2097152 bytes Highest expansion depth: 2/40 Expensive parser function count: 0/100

Transclusion expansion time report (%,ms,calls,template) 100.00% 0.000 1 -total

Saved in parser cache with key koalwikidb-wk_:pcache:idhash:3042-0!*!*!!zh-cn!*!* and timestamp 20220519053636 and revision id 12945