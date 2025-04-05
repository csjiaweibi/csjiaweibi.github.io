---
title: '我所理解的Java（更新版）'
date: 2025-04-05
permalink: /posts/2025/04/blog-post-1/
tags:
  - JAVA SE
---

这篇博客将分享我在学习Java SE中的心得，并根据2025年4月5日的最新信息进行更新。

## 学习建议
- **多敲代码**：实践是掌握编程的最佳方式，通过运行代码直观地加深记忆。
- **多读源码**：阅读Java源码是难点，未来我会分享更多读源码的经验。
- **关注最新版本**：Java 24（2025年3月18日发布）引入了新特性，如虚拟线程和KDF API，建议了解这些更新。

本文参考《Java核心技术》、《深入理解Java虚拟机》、《Java并发编程之美》。

## Java 重点内容

Java语言以简单、强大的库、健壮的检查机制、跨平台性和可移植性著称。它是半编译语言（字节码+运行时解释或JIT编译），具有动态性。

深入学习Java需要：
- 阅读源码
- 深入理解JVM和JUC（Java Util Concurrency）
- 注解+反射+设计模式共同构成了Java框架。

### 基础知识
- 基本数据类型 + 包装类型 + 大数 + 异常 + 泛型 + 注解 + 反射 + Lambda表达式 + 字节流 + 序列化 + I/O + 动态代理（方法拦截与增强） + Stream

### 面向对象
- 单继承 + 接口 + 多态 + 封装 + 修饰符 + 抽象类 + 内部类

### 重点类
- Object类 + Class类 + String类

### 容器
- ArrayList类 + LinkedList类 + HashMap类 + PriorityQueue类

### JVM
- 类加载子系统
- 运行时数据区（堆、运行时常量池、本地方法栈、程序计数器、Java虚拟机栈、方法区）
- 垃圾收集器（GC）
- 执行引擎（包括解释器和JIT编译器）
- 本地方法接口（JNI）和本地方法库

### JRE和JDK
- JRE = JVM + 强大的库
- JDK = JRE + 编译器 + 调试器 + 开发工具

### JUC（Java Util Concurrency）
- 多线程 + 线程池 + AQS + ConcurrentHashMap + AbstractQueuedSynchronizer + ConditionObject + CopyOnWriteArrayList + 阻塞队列 + 内存泄露 + 死锁 + 线程安全 + ThreadLocal + CAS + ReentrantLock + Atomic + 线程安全的集合
- 新增：Java 24引入轻量级锁机制（JEP 444），默认使用LM_LIGHTWEIGHT模式，改善并发性能。

### 锁
- 死锁 + 锁的升级 + 锁的状态

### 实用工具
- IDEA + jconsole + VisualVM（用于性能分析）

## 知识点

- **对象的创建方式**：new关键字、反射、克隆、序列化等。
- **反射的原理**：通过Class对象操作类、方法、字段，动态调用。
- **动态代理的使用场景**：AOP、RPC框架，如Spring中的事务管理。
- **类加载过程**：
  - 加载、链接（验证、准备、解析）、初始化。
- **类加载器类型**：
  - 启动类加载器（加载核心库）
  - 扩展类加载器（加载扩展库）
  - 应用程序类加载器（加载用户自定义库）
  - 自定义类加载器（开发者自定义逻辑）
- **运行时数据区**：
  - 程序计数器：记录当前线程执行的字节码指令。
  - Java虚拟机栈：存储局部变量、操作数栈、方法调用和返回。
  - 本地方法栈：执行native方法（C/C++编写）。
  - 堆：存储对象实例和数组，分为年轻代（Eden区和Survivor区）和老年代，含字符串常量池。
  - 方法区：存储类信息、常量池、静态变量、即时编译代码（HotSpot中由元空间实现）。
  - 运行时常量池：方法区的一部分，存储字面量和符号引用。
- **垃圾回收**：
  - 算法：标记-清除、复制、标记-整理、分代收集。
  - 引用类型：强引用、弱引用、软引用、虚引用。
  - 垃圾收集器：CMS、G1、Serial、ParNew，Java 24新增实验性Generational Shenandoah GC。
- **对象的内存布局**：
  - 对象头（MarkWord和元数据指针）、实例数据、对齐填充。
  - MarkWord记录哈希码、GC分代年龄、锁状态等。
- **如何创建一个线程**：
  - 继承Thread类、实现Runnable接口、使用ExecutorService。

## 难点
- 构造一个好的类：使用设计模式（如单例、工厂模式）提高质量。
- 重构代码：遵循《重构：改善既有代码的设计》原则，优化结构。
- 代码具有良好的可读性：遵循Oracle Java编码规范，使用有意义的变量名和注释。
- 让并发串行执行：使用synchronized、ReentrantLock或CountDownLatch。
