---
permalink: /
title: "Jiawei Bi's Personal Homepage"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

我目前是一名学生，正在寻找能够解决现实世界问题并具有理论意义的解决方案。

## 教育背景

### 同济大学 (985), 上海
*2023年9月 - 至今*  
**电子信息硕士学位**  
GPA: 4.5/5.0  
预计毕业时间: 2026年6月

### 上海大学 (211), 上海
*2019年9月 - 2023年6月*  
**通信工程学士学位**  
GPA: 3.7/4.0

## 专业经验

**2025.6 - 2025.9**

**阿里巴巴-高德地图**

**共享出行业务中心**

**服务端研发-订单业务**

- **背景：** 高德打车团队订单业务开发以及针对订单领域舆情处理与问题定位场景，搭建打车机器人Agent

- **技术栈：** Spring + HSF + Diamond + Tair + MetaQ + OceanBase + Lindorm + VIPServer + EagleEye
1. **订单系统Agent提效**：

  - 实现按业务领域模型划分的 Multi-Agent 层次架构，结合Prompt工程、Query泛化、建立同义相似问题簇、长短期记忆与多轮对话、GraphRAG 等方法减少模型幻觉，通过定时任务回放验证新功能，**模型识别准确率提升至97%**。

  - 使用消息队列、分布式锁、退避算法优化向量索引建立过程，解决模型限流、重复消费、消费幂等问题，使用线程池、多模型并行解析、任务拆分等方法将**模型平均RT压缩至2s**。

  - 通过搭建工具管理平台解耦模型与工具调用，规范工具定义，解决SOP调用链路硬编码问题，目前管理**SPI、SLS及Local工具70+**，实现通过HSF泛化调用业务方工具，业务方接入、调试耗时降到**30min**。


2. **订单业务开发**：

  - 完成下单、改派、状态机服务的技改与业务需求，业务**下单平均耗时 251ms**,完成包括国际化接入悦行包车、备胎改派场景下取消子单逻辑优化、秒送备注字段优化等业务需求，做好灰度上线验证与监控大盘观测。


  - 参与设计并实现业务通用组件依赖包，构建支持定制化、可扩展的**插件化**框架，基于泛型、注解、反射在应用启动时自动发现并加载本地插件、结合配置中心实现远程插件的按需加载与热更新、在主流程的扩展点以同步异步并行的方式执行满足业务身份的所有插件、实现功能与业务逻辑的高度解耦，并完成下单主流程助老券参数校验插件的实现。


  - 参与排查下单流程**强/弱依赖**耦合导致的线上稳定性问题，本地**消息堆积**导致的频繁Full GC，RPC**超时时间**不生效导致的成功率下跌问题，**DNS**解析异常等问题，形成**防御性编程**意识。



### 蔚来软件科技有限公司
*2024年11月 - 2025年1月*  
**性能平台后端开发工程师**

- **背景：** 汽车测试资源管理平台，支撑万级测试设备可统一管理、可监控、可测试、可诊断、可远程升级的能力。

- **技术栈：** Django + MySQL + Redis + Kafka + Vue + gRPC +  Docker

主要贡献：
  - 通过工厂、模版、策略、代理、责任链等**设计模式**分层解耦，解决由于硬件协议不同导致的的设备管理的标准性和拓展性问题，加快新设备接入速度。
 
  - 通过Python、Shell脚本完成台架资源的监控，帮助业务方实现个性化需求，同时挖掘共性需求形成**模版配置**。

  - 优化测试资源的状态监听策略，将设备端定时轮询策略改为通过消息队列的**长链接**和基于推模型的设备端长轮询兜底相结合的方案，问题报警时间**缩短至1s**，节约机器、带宽、日志、维护成本。

  - 通过优化索引和慢查询提高数据库查询效率，使用**乐观锁**完成缓存数据一致性实现。

## 项目经验

### 极星云小程序
*2023年9月 - 2025年3月*  
**后端开发工程师，同济大学哔哩工作室编程组**

**技术栈:** SpringBoot, MySQL, Mybatis, Redis, Vue, Kafka, Druid

一个基于微服务架构的校园综合服务平台，集成了校园生活场景（信息论坛、项目组队、二手交易、配送服务等），连接学生组织（B端）与个人用户（C端）。

主要贡献：
- 完成了**二手交易**、**信息论坛**和**校园高德地图**模块的开发
- 实现了**分布式锁**，确保团队操作互斥并保证接口幂等性
- 部署了**布隆过滤器**，缓存热门数据，降低数据库穿透风险
- 利用**前缀树算法**进行敏感词过滤，并使用**Dijkstra算法**进行路径规划
- 集成了**Deepseek**，构建校园智能代理

### MIT 6.5824
*2024年9月 - 2024年11月*  
**研究生课程项目**

**技术栈:** Raft算法、分片存储、MapReduce、多节点容错

主要贡献：
- 基于**Raft共识算法**实现了分布式容错，支持分片存储和数据一致性
- 设计了一个**MapReduce**并行计算框架，协调10+个工作节点，将任务完成效率提高30%

## 技术技能

- **编程语言:** Java（熟练/ Spring生态系统）、Python（Django/AI）、Go（Beego）
- **数据库:** MySQL（索引优化、事务管理）、Redis（缓存设计、分布式锁）
- **系统设计:** 分布式架构（微服务、云原生）、高并发（JUC、JVM调优）
- **工具与框架:** Linux, SpringBoot, Django, Kafka, Docker

## 沟通与领导力

- 产品经理，同济大学Offer青年校园公众号
- 部门负责人，同济大学学生会（跨部门协作）

## 荣誉与奖项

### 技术奖项
- 大唐杯省级比赛二等奖（无线算法）
- 上海大学电子设计大赛二等奖（嵌入式系统开发）

### 综合奖项
- 上海优秀毕业生（前3%）
- 同济大学优秀学业奖学金（两次）
- 上海大学优秀学业奖学金（三次）
- 上海大学优秀学生（三次）
- 上海大学创新与创业奖学金
- 同济大学社会活动奖学金



<!-- # Jiawei Bi -->
I’m now studying as a student, searching for solutions that can address real-world problems and make theoretical sense.

## Education

### Tongji University (985), Shanghai
*September 2023 - Present*  
**Master's Degree in Electronic Information**  
GPA: 4.5/5.0  
Expected Graduation: June 2026

### Shanghai University (211), Shanghai
*September 2019 - June 2023*  
**Bachelor's Degree in Communication Engineering**  
GPA: 3.7/4.0

## Professional Experience

### NIO Software Technology Co., Ltd.
*November 2024 - January 2025*  
**Backend Developer, Performance Platform**

Developed a test bench resource management platform for automotive development environments using **Django+MySQL** for core business logic, **Celery+Redis** for scheduled tasks and cache management, and **RPC** for inter-service communication, managing thousands of test bench resources.

Key Contributions:
- Developed **points system and reservation system** modules to improve test bench utilization and achieve fine-grained management
- Built **diagnostic middleware** based on UDS protocol, separating business logic from underlying hardware protocols to reduce system coupling
- Implemented **database migration** using Canal to accommodate growing data volumes
- Conducted test bench **log analysis** and fault monitoring using Python with machine learning techniques
- Authored 8 **technical documents** on Feishu, provided technical support 30+ times, and reported 40+ issues

## Projects

### Jixing Cloud Mini Program
*September 2023 - March 2025*  
**Backend Developer, Tongji University Bibi Studio Programming Group**

**Tech Stack:** SpringBoot, MySQL, Mybatis, Redis, Vue, Kafka, Druid

A comprehensive campus service platform based on microservice architecture, integrating campus life scenarios (information forums, project teaming, second-hand transactions, delivery services, etc.) connecting student organizations (B-end) with individual users (C-end).

Key Contributions:
- Completed development of **second-hand transactions**, **information forum**, and **campus Gaode map** modules
- Implemented **distributed locks** to ensure mutual exclusion in team operations and guarantee interface idempotence
- Deployed **Bloom filters** to cache hot data and reduce database penetration risks
- Utilized **prefix tree** algorithms for sensitive word filtering and **Dijkstra's algorithm** for path planning
- Integrated **Deepseek** to build campus intelligent agents

### MIT 6.5824
*September 2024 - November 2024*  
**Graduate Course Project**

**Tech Stack:** Raft Algorithm, Sharded Storage, MapReduce, Multi-node Fault Tolerance

Key Contributions:
- Implemented distributed fault tolerance based on the **Raft consensus algorithm**, supporting sharded storage and data consistency
- Designed a **MapReduce** parallel computing framework coordinating 10+ worker nodes, improving task completion efficiency by 30%

## Technical Skills

- **Programming Languages:** Java (Proficient/Spring Ecosystem), Python (Django/AI), Go (Beego)
- **Databases:** MySQL (Index Optimization, Transaction Management), Redis (Cache Design, Distributed Locks)
- **System Design:** Distributed Architecture (Microservices, Cloud Native), High Concurrency (JUC, JVM Tuning)
- **Tools & Frameworks:** Linux, SpringBoot, Django, Kafka, Docker

## Communication & Leadership

- Product Manager, TJ Offer Youth Campus Public Account
- Department Head, Tongji University School Student Union (Cross-department Collaboration)

## Honors & Awards

### Technical Awards
- Datang Cup Provincial Competition Second Prize (Wireless Algorithm)
- Shanghai University Electronic Design Competition Second Prize (Embedded System Development)

### Comprehensive Awards
- Shanghai Outstanding Graduate (Top 3%)
- Tongji University Outstanding Academic Scholarship (Twice)
- Shanghai University Outstanding Academic Scholarship (Three Times)
- Shanghai University Outstanding Student (Three Times)
- Shanghai University Innovation and Entrepreneurship Scholarship
- Tongji University Social Activities Scholarship
