## 简介

pentaho-kettle是一款开源的ETL工具，官方名称是Pentaho Data Integration，主要是用来做数据库迁移等，支持面很强大，易学难精。

支持在windows和linux下使用，但是linux下不一定有图形界面，本来作为服务器一般都不会有图形界面的，所以设计工作主要在windows环境下完成。

源代码使用Java编写。

## 基础环境搭建

前提，版本8.1

有2种搭建方式，推荐第一种

### 直接在官网下载安装包，解压即可用

步骤1，下载JDK1.8及以上，并安装

步骤2，下载PDI编译后的安装包，解压

下载链接：https://sourceforge.net/projects/pentaho/files/

![1538920265987](E:\03_笔记\99_work\01_kettle\assets\1538920265987.png)

也可以下载7.1稳定版本

![1538920325297](E:\03_笔记\99_work\01_kettle\assets\1538920325297.png)

### 下载官方源码，本地编译打包

官方开源地址：

https://github.com/pentaho/pentaho-kettle/tree/8.1.0.5

编译过程直接参考官方文档：注意maven要配置pentaho的仓库

![1538920441906](E:\03_笔记\99_work\01_kettle\assets\1538920441906.png)

使用maven打包，生产zip文件夹，直接解压就可以使用

### 启动

windows下双击spoon.bat即可启动PDI的图形界面

文件夹下的samples下面是官方的demo，建议搞懂每一个例子，大部分的需求都是这些官方demo排列组合就可以完成的。

### 概念

#### 文件扩展名：

kjb: job，作业

ktr: transformation，转换

作业可以包裹多个转换和作业

强烈建议：不要直接执行转换，用一个作业来包裹转换，执行作业，以便统一管理。

#### 资源库：

资源库分2种，参考https://www.cnblogs.com/zigewb/p/4502938.html

文件资源库，把job/transformation保存为kjb/ktr结尾的文件，调用的时候传入路径和文件名。

数据库资源库，默认账号admin/admin，把job/transformation保存到数据库中。

选择哪一种资源库，基于需求决定，数据库容易统一管理，但是没有版本控制，文件库可以使用svn等版本控制工具控制版本。

#### 工具：

PDI解压之后，有提供以下几个工具

Spoon，完整的带图形界面的设计/执行工具

Pan，用来执行转换的命令行工具

Kitchen，用来执行作业的命令行工具

Carte，用来开启一个服务器，可以远程调用作业或者转换，基于命令行，主要用于搭建集群的PDI环境





