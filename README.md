耗时大约三个星期不到的时间，把这个论坛项目基本上算是完成了，做这个项目最主要的目的是熟悉SpringBoot的使用，然后通过整个项目了解了BootStrap、Thymeleaf、editor.md等等工具的使用
项目的一些东西我都放在了我的csdn博客上，大家可以去看看，包括如何跑起来等等


## 数据库建表语句：
#### user
```$user建表语句
CREATE TABLE `user` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(45) NOT NULL,
  `password` varchar(45) NOT NULL,
  `token` varchar(45) NOT NULL,
  PRIMARY KEY (`id`)
)
```

#### question
```$question建表语句
CREATE TABLE `question` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(50) NOT NULL,
  `description` text NOT NULL,
  `createid` int(11) NOT NULL,
  `comment_count` int(11) NOT NULL DEFAULT '0',
  `view_count` int(11) NOT NULL DEFAULT '0',
  `like_count` int(11) NOT NULL DEFAULT '0',
  `tag` varchar(250) NOT NULL,
  `createtime` bigint(20) NOT NULL,
  PRIMARY KEY (`id`)
) 
```
#### comment
```$user建表语句
CREATE TABLE `comment` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `parent_id` int(11) NOT NULL,
  `type` int(11) NOT NULL,
  `commentor` int(11) DEFAULT NULL,
  `createtime` bigint(20) DEFAULT NULL,
  `like_count` int(11) DEFAULT '0',
  `content` varchar(200) NOT NULL,
  `commentcount` int(11) DEFAULT '0',
  PRIMARY KEY (`id`)
) 
```
#### notification
```$notification建表语句
CREATE TABLE `notification` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `notifier` int(11) NOT NULL,
  `receiver` int(11) NOT NULL,
  `outerid` int(11) NOT NULL,
  `type` int(11) NOT NULL,
  `createtime` bigint(20) NOT NULL,
  `status` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`id`)
) 
```

## thymeleaf官方文档
```
https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html
```
## BootStrap官方文档
```
https://v3.bootcss.com/components/
```
## Editor.md官网
```
http://editor.md.ipandao.com/
```
