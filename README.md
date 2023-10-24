# 宿舍选择系统

> **Team members: **
>
> 陈越航 12012826	王浩羽 11911612	王贵正 12011425	钟日涵 12011422	刘一予 12112011
>

## Abstract-摘要

为解决南科大学生自由选择宿舍、管理人员合理分配宿舍的需求，本项目旨在为南科大学生提供网页应用服务，让学生能够方便、快捷地依据个人偏好完成舍友和宿舍的选择；同时提供配套的管理端网页应用服务，让管理人员能够发布、整合学生宿舍相关信息，进行有关业务操作。

## Motivation-动机

南科大给予学生最大程度的自由，希望更加人性化地管理学生的校内住宿，因此需要为全体学生提供在线宿舍选择系统。然而，现有系统存在功能简陋、选择与分配机制单一等诸多问题。实际场景中有些用户甚至不愿意选择使用。为解决此问题，我们需要开发一个既方便学生使用，又方便辅导员管理的宿舍系统，提供系统化管理、合理的业务机制、多功能应用。

## Features-功能描述

### User "Stories"

- #### 学生端：

  学生登录系统之后，学生能够看到管理员所放的通知，也可以去查看学生自己的个人档案也可以对自己的个人档案进行修改。学生端很重要的一个功能是可以进行队伍信息的查看，学生可以通过查看其他同学的信息并对其他同学进行组队邀请，同样的也可以接受其他同学对自己的组队邀请，在某些情况也可以进行队伍的退出。在宿舍方面，学生首先可以进行宿舍信息的查询并且以队伍为单位对心仪的宿舍进行收藏，既可以通过宿舍信息查询来了解宿舍也能够通过论坛进行对宿舍的评论以及查看其他人的评论。最终在正选阶段进行抢宿舍。

  ![student](https://github.com/0Ohh/proposal/assets/90323400/fe1b31c1-fd2b-4298-8215-7e0a8c5a6258)

- #### 管理端：

  辅导员在登录系统之后，能够对学生信息进行批量或单个的增删查改，可以以管理员身份进行发布所有人都能看到的网页通知。在宿舍信息管理方面，管理员可以对宿舍进行批量或单个的增删查改。在宿舍分配管理方面，辅导员可以对选宿舍阶段的时间进行设置，从组队时间到预选时间再到正选时间。以及在学生选完宿舍之后，为未选上宿舍的同学及队伍进行管理调配。并且宿舍信息和学生信息可以按照年级等信息进行批量导出。除此之外有一个顶级管理员，可以对普通管理员账号进行增删查改。

  ![admin](https://github.com/0Ohh/proposal/assets/90323400/dad94601-9a33-4cfd-8a9c-3b5ed1a332ab)


### 功能性需求

#### 管理端功能

##### 管理员账号管理

- 系统有一个顶级管理员账号，该顶级管理员账号可以增删一般管理员账号
- 一般管理员账号可以进行宿舍管理和学生账号管理

##### 宿舍管理

- 系统提供增加、删除单个房间，以及修改房间信息的功能
- 系统提供批量增加宿舍功能。例如：在二期宿舍-11栋-2层至12层每层增加20个房间，并且自动编号
- 可以设置宿舍面向的对象（如限定性别、学位、入学年份）
- 可以设置宿舍开放选取的时间
- 提供导出宿舍信息功能

##### 学生账号管理

- 管理员可以对单个学生账号进行增加、删除和修改操作
- 管理员可以上传excel表格并从表格中批量导入信息并创建学生账号

##### 发布通知

- 管理员可以发布通知，以便向学生和管理人员传达重要信息。

#### 学生端功能

##### 登陆

- 学生可以使用自己的账号登陆到宿舍选择系统中。

##### 个人档案

- 个人档案包含基本信息以及和选宿舍相关的重要信息（如作息时间、卫生接受程度）
- 学生可查看和修改个人档案

##### 查看房间信息

- 学生可以查看宿舍列表、某宿舍的详细信息（区域、楼号、层数、房间号等）
- 学生可以收藏宿舍，收藏后的宿舍会得到优先展示

##### 宿舍选择

- 提供推荐舍友功能，系统会根据学生的个人档案为学生推荐合适的舍友

- 组队阶段：提供邀请制组队功能
- 预选阶段：提供收藏房间、预选房间功能
- 正选阶段：根据管理员设置的开始时间，以队伍为单位选取，先到先得制度

#### 高级功能

- 平面图展示：系统可以展示宿舍楼、房间和床位的平面图，并提供预览功能。
- 错峰选择设计：系统可以区分男生和女生、博士生和研究生的选宿舍时间，并展示候补选择时间和房型信息。
- 宿舍调换功能：学生可以在平台上申请宿舍调换。
- 部署至服务器

### 非功能性需求

- 高并发处理：系统支持高并发情况下的抢宿舍操作。
- 防作弊系统：系统限制脚本的使用，并仅允许用户单一登录，以防止作弊行为；同时，防止自动脚本用户抢宿舍对服务器资源的消耗。
- 元素关联性：加入南科大相关的元素
- 快速响应：各功能在前端可以快速显示出结果（4s内）
- 结果准确：提供准确的结果
- 便捷性：前端设计贴合用户需求，让用户拥有简洁、快捷、方便的使用体验。

## Architecture

- 核心业务——宿舍选择业务的泳道图（跨职能流程图）

![flow](https://github.com/0Ohh/proposal/assets/90323400/bc7f0082-77c0-4c71-b2ef-ae084360dded)

## Timeline

我们预计每人每周花费至少12h用于该项目，尝试在尽量早的时间完成开发，留下足够时间作为备用。

后端计划：

![back-end-time](https://github.com/0Ohh/proposal/assets/90323400/50d94efa-9a07-41f8-a65e-ab7fa1b8b7f4)


前端计划：

![front-end-time](https://github.com/0Ohh/proposal/assets/90323400/1e38127a-0533-4be1-bcdc-fd0d0fc39283)


## APIs and Dependencies

### 后端：
- 框架：SpringBoot
- 持久层框架：MybatisPlus,
- 数据库：Postgresql

### 前端：

- 框架：Vue.js
- 路由：Vue Router
- 网络请求：Axios
- 组件库：Element Plus
- 图表：Echarts

### 部署：

- 使用nginx作为前端服务器
- 利用docker及docker stack技术进行部署


