> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [git.koal.com](http://git.koal.com/idaas/docs/id/-/wikis/%E8%84%9A%E6%9C%AC%E8%BD%AC%E6%8D%A2%E5%AF%BC%E5%87%BA%E5%B7%A5%E5%85%B7%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E)

> 身份中心概要设计

Last edited by [![](http://git.koal.com/assets/no_avatar-849f9c04a3a0d0cea2424ae97b27447dc64a7dbfae83c036c45b403392f0e8ba.png) **王满满**](http://git.koal.com/wangmanman) 20 hours ago

该工具由罗鑫余提供
   
导出开发环境 id_t_identity_ext 表，MYSQL,DM,KB 三种格式脚本

```
java -jar sql-compare.jar --action=EXPORT --db-type=MYSQL --s1=root:Koal@123456@10.0.249.133:3306/idaas --script-db-type=MYSQL,DM,KB --tables=id_t_identity_ext
```



工具使用及参数信息：

java -jar sql-compare.jar  
--action=COMPARE  
--db-type=MYSQL  
--s1=root:123456@10.4.67.222:3306/lxy_test  
--s2=root:123456@10.4.67.222:3306/chl_test  
--changes-for=s1 --script-db-type=MYSQL

```
action 操作类型（必选）
格式：
        action=<COMPARE | EXPORT | EXPORT-DATA | EXPORT-ALL>
        COMPARE：进行对比操作.  必要参数：action，db-type，s1，s2；选填参数：changes-for
        EXPORT：导出表结构操作.  必要参数：action，db-type，s1
        EXPORT-DATA：导出表数据操作.  必要参数：action，db-type，s1
        EXPORT-ALL：导出表结构+表数据操作.  必要参数：action，db-type，s1

db-type 数据库类型（必选）
格式：
        db-type=<MYSQL| DM | KB>

s1 数据库连接信息（必选）
格式：
        s1=<username>:<password>@<ip>:<port>/<db_name>
        username ：数据库用户名
        password ： 数据库密码
        ip ： 数据库ip地址
        port ： 数据库端口
        db_name ： 数据库名
eg:
        s1=root:123456@10.4.67.222:3306/lxy_test

s2 数据库连接信息（非必选）
格式：同s1

changes-for 以指定数据库为对比基准（非必选，默认s1）
格式：
        changes-for=<空 | s1 | s2>

script-db-type 导出数据库类型（非必选，默认为db-type）
格式：
        script-db-type=<空 | MYSQL | DM | KB | ALL>
参数说明：
        1. 空 ：默认使用db-typ的值
        2. MYSQL | DM | KB ：导出对应数据库脚本
        3. ALL ：导出所用数据库脚本
eg:
        1. script-db-type=【导出默认类型数据库脚本】
        2. script-db-type=MYSQL【导出MYSQL数据库脚本】
        3. script-db-type=MYSQL,DM【导出MYSQL,DM数据库脚本】
        4. script-db-type=ALL【导出目前支持的所有数据库脚本】

tables 需要对比或者导出的表，多个使用逗号隔开，为空导出或者对比全库，默认为空
格式：
        tables=<空 | app_t_app| app_t_app,app_t_exclude_policy, app_t_gw_proxy_policy>
参数说明：
        1. 空 ：导出或者对比全库
        2. app_t_app ：导出或者对比该表
        3. app_t_app,app_t_exclude_policy, app_t_gw_proxy_policy ：导出或者对比该表
eg:
        1. tables=【导出或者对比全库】
        2. tables=app_t_app【导出或者对比该表】
        3. tables=app_t_app,app_t_exclude_policy, app_t_gw_proxy_policy【导出或者对比该表】

is-print-sql-logger 是否打印SQL日志，默认为空
格式：
        is-print-sql-logger=<空 | YES | Y | NO | N>
参数说明：
        1. 空 ：不打印
        2. YES | Y ：打印
        3. NO | N ：不打印

table-prefix 需要对比或者导出的表前缀，多个使用逗号隔开，为空导出或者对比全库，默认为空 (不能和tables 同时使用)
格式：
        table-prefix=<空 | pc_t_ | pc_t_ , app_t_>
参数说明：
        1. 空 导出或者对比全库
        2. pc_t_  导出以pc_t_为前缀的表

1. 对比操作
    --action=COMPARE --db-type=DM --s1=SYSDBA:SYSDBA@127.0.0.1:5236/IDAAS_COPY --s2=SYSDBA:SYSDBA@127.0.0.1:5236/IDAAS --changes-for=s1 --script-db-type=ALL

2. 导出操作
    --action=EXPORT --db-type=KB --s1=system:Koal@123456@10.0.249.36:54321/idaas_lxy --script-db-type=ALL
```
