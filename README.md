这是我在做ETL工具集成开发的笔记，仅供个人记录使用

## 章节：

1. [kettle系列之一 基础知识](kettle-01-basicKnowledge.md)

   PDI基础知识，包括简介，环境搭建和一些基础名词

2. [kettle系列之二 工具使用](kettle-02-basicJobDesign.md)

   PDI基础模型设计，包括简单的数据库交换，占位符和变量，循环，定时，日志输出，事务控制

3. [kettle系列之三 数据库资源库分析](kettle-03-databaseAnalysis.md)

   PDI的数据库表，基于数据库资源库，一些简单的表结构分析

4. [kettle系列之四 linux下使用kettle执行和调度](kettle-04-linux-kettle.md)

   linux环境下PDI的安装，基于数据库资源库，执行Job

5. [kettle系列之五kettle远程执行和调度](kettle-05-Cluster.md)

   PDI的集群安装，远程执行Job

6. [SpringBoot集成kettle](kettle-05-intergrateWithJava.md)

   PDI的Java集成，集成设计(文件库和资源库)，密码加密方式，本地执行和远程执行，Job启动和停止，日志设计

## todo: 

1. 思考如何使用API，关联本地数据库资源库和远端数据库资源库
2. 或者使用文件资源库，上传文件资源库，然后直接调用
3. 快速复制作业，只切换数据库，比如从A库搬到B库，改成从A库搬到C库，提高设计效率

