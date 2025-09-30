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

  - **模型方面**：实现按业务领域模型划分的 Multi-Agent 层级架构，结合Prompt工程、Query改写、长短期记忆与多轮对话、GraphRAG 等方法减少模型幻觉，通过回放功能解决稳定性问题，模型识别准确率提升至97%。

  - **工具方面**：通过搭建工具管理平台解耦模型与工具调用，规范工具定义，解决SOP调用链路硬编码问题，目前管理SPI、SLS及Local工具70+，通过HSF泛化调用业务方工具，业务方接入、调试耗时降到30min。

  - **工程方面**：使用消息队列、分布式锁、退避算法、缓存优化向量索引建立过程，解决模型限流问题，使用线程池、多模型并行解析、任务拆分等方法将模型平均RT压缩至2s。


2. **订单业务开发**：

  - **业务需求**：完成下单、改派、状态机服务的技改与业务需求，完成包括国际化接入悦行包车、备胎改派场景下取消子单逻辑优化、秒送备注字段优化等业务需求，做好灰度上线验证与监控大盘观测。


  - **复杂性治理**：参与团队插件化架构改造，基于泛型、注解、反射在应用启动时加载本地插件、结合配置中心加载远程插件、在主流程的扩展点以同步异步并行的方式执行满足业务身份的所有插件、实现功能复⽤和业务隔离。


  - **稳定性排查**：参与排查下单流程强/弱依赖耦合导致的线上稳定性问题，本地消息堆积导致的频繁Full GC，RPC超时时间不生效导致的成功率下跌问题，形成防御性编程意识。



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

