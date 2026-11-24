# 基于SpringBoot+Vue的学生竞赛管理系统

![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Vue3](https://img.shields.io/badge/-Vue3-grey?style=flat-square) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![MyBatis](https://img.shields.io/badge/-MyBatis-000000?style=flat-square&logo=mybatis&logoColor=white) 

## 项目介绍

本系统是一款面向高校学生与竞赛管理教师的学科竞赛组织与成果认定平台，针对竞赛信息分散难查、报名资格核验靠人工、跨学院组队匹配困难、作品提交与评审流程割裂、获奖证书难归档等问题，把竞赛大厅浏览报名、组队广场招募、作品在线提交、报名审核与作品评审、获奖榜单与电子证书、公告资讯以及管理端数据看板整合到同一套前后端分离工程中，形成“发布—报名—组队—作品—评审—获奖”的闭环。

系统采用 SpringBoot + Vue 架构，区分学生与管理员：学生端浏览竞赛与公告、提交个人/团队报名、创建或加入队伍、上传参赛作品并查看获奖成果；管理端维护竞赛分类与项目、审核报名与组队、评审作品、登记奖项并发布通知。封面与证书等静态资源本地 uploads 映射访问，学院报名分布与获奖等级统计可看板可视化，适合作为毕设、课设与高校第二课堂竞赛管理学习参考。

## 主要功能模块

- **统一登录与角色分流**：学生与管理员统一入口登录注册，JWT 鉴权；按 USER/ADMIN 自动进入学生竞赛大厅或管理后台，路由与接口双重隔离
- **学生首页与快捷入口**：展示开放报名赛事、个人报名/组队/作品/获奖档案指标，图片背景英雄区引导进入竞赛大厅、组队广场与作品提交
- **竞赛大厅与详情报名**：按分类筛选浏览竞赛海报、章程、赛程与奖项设置，在线提交个人赛或团队赛报名并上传学籍证明材料
- **组队广场**：创建队伍、邀请码加入、成员分工与指导教师信息维护，团队赛报名前完成组队锁定
- **报名审核**：管理员审核报名资格，支持通过/驳回并填写审核意见，学生端可查看审核状态与理由
- **作品提交与评审**：参赛者上传作品封面与材料附件，管理员打分评语并回写评审结果
- **获奖成果与电子证书**：登记特等/一/二/三等及优秀奖，生成证书编号与证书图，获奖榜单公开展示
- **公告资讯中心**：发布报名通知、获奖公示、论文指南与学分认定办法等置顶公告，学生端列表与详情阅读
- **管理数据看板**：竞赛项目数、待审报名、组队数、待评作品、已认定获奖等 KPI，以及各学院报名分布、竞赛级别构成与获奖等级 ECharts 统计
- **竞赛分类与项目管理**：维护程序设计、数学建模、电子设计、创新创业、人文外语等分类，发布校级/省级/国家级赛事并控制报名状态
- **用户与资料中心**：学生维护学院专业班级头像与简介；管理员启停账号并管理系统用户
- **本地文件上传映射**：竞赛封面、作品图、证书、公告配图与证明附件统一落盘 uploads，对外以 /api/uploads/** 相对路径访问

## 技术架构

- **后端**：Spring Boot 2.7 + MyBatis-Plus + JWT + Hutool
- **前端**：Vue 3 + TypeScript + Vue Router + Pinia + Element Plus + Vite + ECharts
- **数据库**：MySQL 8.0

<!-- screenshots-start -->
## 系统截图

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E7%99%BB%E5%BD%95%E9%A1%B5%E9%9D%A2.png" alt="登录页面" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E5%AD%A6%E7%94%9F%E9%A6%96%E9%A1%B5.png" alt="学生首页" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E7%AB%9E%E8%B5%9B%E5%A4%A7%E5%8E%85.png" alt="竞赛大厅" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E7%BB%84%E9%98%9F%E5%B9%BF%E5%9C%BA.png" alt="组队广场" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E4%BD%9C%E5%93%81%E6%8F%90%E4%BA%A4.png" alt="作品提交" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E6%8A%A5%E5%90%8D%E5%AE%A1%E6%A0%B8.png" alt="报名审核" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E4%BD%9C%E5%93%81%E8%AF%84%E5%AE%A1.png" alt="作品评审" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E7%AE%A1%E7%90%86%E5%91%98%E6%95%B0%E6%8D%AE%E7%9C%8B%E6%9D%BF.png" alt="管理员数据看板" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E8%AE%BA%E6%96%87%E5%9B%BE1.png" alt="论文图1" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/%E8%AE%BA%E6%96%87%E5%9B%BE2.png" alt="论文图2" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/studentcompetition/UML%E5%9B%BE%E5%88%97%E8%A1%A8.png" alt="UML图列表" width="600" />

<!-- screenshots-end -->

---

## 接毕业设计和论文

### 作者微信：vvsgxmn  (支持修改、 部署调试、 支持代做毕设)

### 接网站建设、小程序

### 选题+开题报告+任务书+程序定制+安装调试+论文+答辩ppt 都可以做

### 购买地址：[https://www.vvxx.love](https://www.vvxx.love)（vv毕设网）

### 支持 **一键生成 UML 图**：上传项目压缩包即可自动产出功能模块图、用例图、流程图、E-R 图、时序图等全套毕设图表。

### 提供 **免费配套软件下载 + 安装说明 + 部署教程**

![vv毕设网 - 一键画图](https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/uml-draw.png)

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/image-20260825133349317.png" alt="image-20260825133349317" />

⚠️ Bug添加微信**免费修复**，免费修复。其他平台的私信一律不管（微信方便发送文件）
