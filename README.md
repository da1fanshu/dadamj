# 达达麻将最完整的麻将游戏

#### 介绍
达达麻将是一款主要以麻将玩法为主的游戏，使用了cocoscreater作为游戏引擎，nodeJS开发服务端，mysql存储数据，是一款功能完整可直接运行的游戏项目！

### 欢迎加入棋牌游戏开发QQ群852101542，里面都是资深棋牌游戏开发者，一起打造更优秀的棋牌游戏！一起赚钱创业，合作必胜！

#### 软件架构

软件架构说明
数据库：MySQL：5.7
服务端：Node.js：6.11.0
游戏开发引擎：CocosCreator：1.6.2

### 美术图片资源

![输入图片说明](https://images.gitee.com/uploads/images/2019/0417/100744_0b69395e_4917846.png "20190131154038447.png")
![输入图片说明](https://images.gitee.com/uploads/images/2019/0417/100755_c90af0f5_4917846.png "20190131154052628.png")
![输入图片说明](https://images.gitee.com/uploads/images/2019/0417/100806_39d64491_4917846.png "20190131154137547.png")
![输入图片说明](https://images.gitee.com/uploads/images/2019/0417/100821_17e71872_4917846.png "20190131154152420.png")
![输入图片说明](https://images.gitee.com/uploads/images/2019/0417/100830_3b891f02_4917846.png "ajNVdqHZLLC671Vbm73icv9RAMwibArwG8Cd9Aj52pIwsicbEyORGTfTagUzbrwSy9g6BibibNBgUVj0.png")


#### 安装教程

完整的搭建文章 [达达麻将最新安装环境和步骤](http://blog.csdn.net/qq_34405062/article/details/89350510)

一、服务器环境搭建
1、安装MySql数据库(百度)
2、登录MySql: mysql –u用户名 –p密码 (登录成功提示符：mysql>)
3、创建数据库: mysql> create database youlin; （本例中所用数据库名为youlin。注意：mysql命令后都要有分号;）
4、选择数据库: mysql> use youlin;
5、导入sql文件: mysql> source d:/db_babykylin.sql; （sql文件原路径为server/sql/db_babykylin.sql，因目录层次太多，所以拷贝到D盘根目录。windows上路径符使用 /）

二、服务器配置修改
1、修改server/configs_win.js文件，因为服务器是本机，所以把HALL_IP改为：127.0.0.1，然后在mysql字段中填上自己的mysql配置（地址、用户名、密码、数据库名、端口），如以下示例：
exports.mysql = function(){
return {
HOST:'127.0.0.1',
USER:'root',
PSWD:'xxxxxx',
DB:'youlin',
PORT:3306,
}
}

三、启动服务器
1、进入server目录，用终端依次启动以下三个服务器：
node ./account_server/app.js ../configs_win.js
node ./hall_server/app.js ../configs_win.js
node ./game_server/app.js ../configs_win.js

四、客户端配置修改
1、修改client/assets/scripts/HTTP.js，把URL字段改为account_server所在服务器的地址，本例中仍为本机：127.0.0.1；

五、启动客户端
1、用Creator打开client目录，运行启动；
注：如果连接不上服务器，通常是服务器的IP或MySQL数据库配置错误；

#### 使用说明

1. xxxx
2. xxxx
3. xxxx

#### 参与贡献

 **

### 大家的参与和贡献是我前进的动力，一定会打造更游戏的游戏给大家使用，谢谢！
** 


1. Fork 本仓库
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request


#### 码云特技

1. 使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2. 码云官方博客 [blog.gitee.com](https://blog.gitee.com)
3. 你可以 [https://gitee.com/explore](https://gitee.com/explore) 这个地址来了解码云上的优秀开源项目
4. [GVP](https://gitee.com/gvp) 全称是码云最有价值开源项目，是码云综合评定出的优秀开源项目
5. 码云官方提供的使用手册 [https://gitee.com/help](https://gitee.com/help)
6. 码云封面人物是一档用来展示码云会员风采的栏目 [https://gitee.com/gitee-stars/](https://gitee.com/gitee-stars/)