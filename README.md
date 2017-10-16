# 需求规格说明书


## 目录
##  1、 引言
###  1.2 项目简介
###  1.3 功能范围
###  1.4 参考资料
## 2、总体描述
### 2.1 项目背景：
### 2.2 项目目标：
### 2.3 典型用户场景：
### 2.4 典型用户需求：
### 2.5 运行环境要求：
## 3、 前提与假设	
## 4、 界面原型设计	
## 5、 系统功能描述验收标准	
### 5.1 质量要求
### 5.2 验收准则
<br><br><br><br>
## 1、引言：
### 1.1编写目的：
   本说明书旨在说明系统的需求，界定系统的范围，指导系统的设计及编程，使用户更清楚该系统的功能。
### 1.2 项目简介：
   项目名称：课程群组系统
   目标用户：面向武汉大学全体教师与学生。
   开发团队：软件工程Java Team
### 1.3 功能范围：
  教师模块：可以开设自己的课程、对每个课程的群组、群组成员、发布的任务和讨论信息进行管理。<br>
  学生模块：可以选课、查看课表、加入课程群组、获取各个课程老师发布的任务信息并在群组中与其他同学或者老师交流讨论。<br>
  附加功能：如果项目完成后时间有余，会增加更多实用的功能，比如：增加类似于QQ的私信聊天、添加表情、从网页再转移到移动app版等等。<br>
### 1.4 参考资料：
  《构建之法》(第二版)，邹欣。<br>
  博客、文档。
## 2、总体描述：
### 2.1 项目背景：
  根据武汉大学课堂上教师和学生的现实需求，他们期待有一个可以不依赖QQ、微信建群加群的方式，能有一个专门的可以帮助他们更便捷的、更高效的、更统一的完成发布任务、交流讨论的类似于QQ群组功能的系统。
### 2.2 项目目标：
  完成本需求规格说明书中说明的要实现的基本功能，如果时间有余，完成附加功能逐步完善系统。
### 2.3 典型用户场景：
|教师|	何老师|
|----|-----|
|课程|高级软件工程|
|学生|本课程所有学生|
|地点|武汉大学计算机学院|
<br>
何老师在课程群组系统上开设了《高级软件工程》课程，学生选择课程并加入了该课程群组。每周二何老师下课后将课程PPT、学习资料、博客链接发到本课程群组里，在学生端可以随时下载这些资料，并与老师和其他同学进行交流讨论。
假如何老师开设了有多门课程，则何老师可以很方便的在此系统上进行管理各个课程群组及相关信息。
假如学生选择了多门课程，也可以很方便的查看每门课程的群组信息，类似于将QQ群组单独从QQ软件中抽离出来结合博客的功能，独立完成目标用户的基本需求和扩展需求。
<br>

### 2.4 典型用户需求说明：
  外观上界面要简洁、易操作。功能上要满足以上描述的基本需要。其他方面要系统稳定、数据安全等等。<br>
### 2.5 运行环境要求：

软件环境|版本
---------------|--------------
操作系统|Windows10 （64位）
数据库|MySQL 5.7
应用平台|Chrome/IE
开发语言|Java
开发环境|Eclipse

## 3、前提与假设：
前提:所有项目构建环境都已准备好。<br>
    假设：目前数据库已经存在所有学生和教师的基本信息，并且教师所开设的课程是选课超过一定人数通过学校审批的课程。<br>
## 4、界面原型设计：
  本页面只是用方框代替，具体页面展示还在设计中。
<br>
![image](https://github.com/WHUSE2017/Java-Team/tree/master/document/image/1.png)
<br>
![image](https://github.com/WHUSE2017/Java-Team/tree/master/document/image/2.png)
<br>
![image](https://github.com/WHUSE2017/Java-Team/tree/master/document/image/3.png)
## 5、系统功能描述验收标准：
### 5.1 质量要求：
用户标准：要界面简洁、易操作，系统稳定安全，满足基本需求。<br>
团队标准：工作有计划的进行；客观地验证项目产品和工作是否遵循恰当的标准、步骤和需求；保证项目进度及结果通知给相关团队成员；全面测试工作来保证系统质量。
### 5.2 验收准则：

|功能测试|功能模块|实现功能|测试用例|测试结果|
|-------|-------|-------|-------|-------|
|	|教师|登录|教工号：001 密码：1111|登录成功|
|	|	|申请开课|点击“申请开设课程”，输入《高级软件工程》|申请成功，产生本课程的群组|
|	|	|查看已开设课程|点击“查看已开课程”|页面内列出所有此教师的所有开设的课程|
|	|	|查看课程群组|点击“查看课程群组”|页面列出所有课程群组|
|	|	|管理任务|在课程群组中发布、修改、删除课程任务|在数据库和学生端都能看到本次任务|
|	|	|参与讨论|在讨论区输入内容|在数据库和学生端都可以看到此内容|
|	|	|管理群组|增加、删除学生|数据库、学生端都会显示|
|	|学生|登录|学生号：2017111密码：2222|登录成功|
|	|	|选课|选择《高级软件工程》|选课成功并加入本课程群组|
|	|	|查看个人课表|点击“查看个人课表”|列出此学生的课程表|
|	|	|查看群组|点击“查看群组”|列出所有课程群组|
|	|	|下载任务|在课程群组中下载任务|下载到本地或者只做浏览|
|	|	|参与讨论|在讨论区输入内容|在数据库和教师端都能看到信息|
<br>
### 业务流程测试：
   对系统项目的业务流程进行测试。<br>
### 非功能测试（包括容错性测试、安全性测试、易用性测试）：
   对用户常用的误操作、删除信息、非法输入等是否进行提示；权限是否安全；各个模块界面风格是否一致；<br>
### 文档测试：
   需求规格说明书、系统设计说明书、操作文档等所需文档是否齐全；文档描述信息是否正确；<br>
* 优秀：
   通过以上功能测试、业务流程测试、非功能测试、文档测试，测试用例不通过数的比例<3%；完成部分附加功能。<br>
* 良好：
    通过以上功能测试、业务流程测试、非功能测试、文档测试，测试用例不通过数的比例<10%；存在小问题，但不影响系统的使用。<br>
* 不合格：
   功能测试、业务流程测试的测试用例不通过率>10%，没有完成基本需求。<br>
      
