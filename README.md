## 1&0 - 客制化代码生成项目

### 项目介绍

一个有趣又实用的项目，基于React + SpringBoot + Vert.x 响应式编程的客制化代码生成项目,

初步把这个项目分为3个阶段，

1. 第一阶段，会制作一个本地的代码生成器，是一个 基于命令行的脚手架 ，能够根据用户的交互式输入快速生成特定代码。考查了一下网上的大多数项目，也只是到这个地步。
2. 第二阶段，上升一个层次，开发制作代码生成器的工具 。比如用户有一段常用的项目代码，使用该工具，可以快速把项目代码制作为代码生成器，这将是提高效率的大杀器！
3. 第三阶段，再上升一个层次，开发在线代码生成器平台 ！用户可以在平台上制作发布自己的代码生成器，还可以在线使用别人的代码生成器，甚至可以共享协作！

之所以拆分是因为所构想的这个项目比较庞大，目前以我的能力，可能只可以做到第二个层次，但是我可以带着目标去学习更高级的知识和优化的技巧。

为什么要做这个项目呢？这应该也是一个需求分析的过程，我觉得这样做才有做项目的意义，并且能够解决问题，搞出实际的应用

### 项目意义

1. 别人写代码，而我想做的是生产代码的脚手架、工具和平台来提高效能
2. 区别于传统的增删改查项目，专科阶段的时候就已经接触过许多传统的Web项目，而该项目我想涉及的是命令行应用、响应式编程、性能优化的入门
3. 网上现有的项目模板，基本上都是只能按作者的要求生成，不太符合我对客制化的设想
4. 如果能够很好的完成这个项目，也可以给简历增添不错的竞争力

### 解决问题

1. 代码生成器本身的作用就是自动生成常见、重复性的代码片段，解决重复编码、效率低下的问题。
2. 虽然网上有很多代码生成器，但都是别人制作封装好的，很多时候还是无法满足实际开发的客制化需求(比如要在每个类上增加特定的注解和注释)。这也是为什么明明有代码生成器，很多开发者还是会抱怨自己的工作总是复制粘贴、编写重复的代码、天天CRUD(增删改查)。如果能够有一个工具帮助开发者快速定制属于自己的代码生成器，那么将进一步提高开发效率。
3. 在团队开发中，要生成的代码可能是需要频繁变化和持续更新维护的。如果有一个线上平台来维护多个不同的代码生成器，支持在线编辑和共享生成器，在提高开发效率的同时、将有利于协作共建，打造更高质量的代码生成器。

### 实际应用

通过本项目我想进行解决：

1. 做算法题目的时候，可能需要一套Java ACM代码输入模板，能够支持多种不同输入模式(比如单次读取和循环)。
2. 开发新项目的时候，可能需要一套初始化项目模板代码，比如一键生成Controller层代码（替换其中的对象)、整合Redis和 MySQL依赖等。
3. 甚至可以制作项目“换皮”工具，支持一键给网络热门项目换皮(比如替换项目的名称、Logo等)

### 初步调研

网上有一些代码生成器项目，比如前端Ant Design Pro 中后台项目脚手架，能够让用户交互式地创建指定的项目；还有后端MyBatisX插件，能够让用户通过界面来创建 CRUD重复代码。但这些项目都是开发者提前制作好了代码生成器，然后让你根据他们设置好的规则生成代码(或者拉取特定位置的代码)，生成后的代码通常还要再自己二次修改，不够灵活。

还有很多所谓的代码生成项目，其实本质上是一个现成的项目模板，让你通过编写对应的配置文件来使用项目，或者还是基于预设的程序来生成特定代码。

这和我要做的事情不同，我的目标是升级一个层次！打造一个帮助用户快速制作代码生成器的工具，也就是“造轮子的轮子”。

然后再升级一个层次！允许用户像发布应用一样，在平台上发布和管理代码生成器，便于共享和协作!

### 技术选型

暂定核心技术如下，具体实现中可能会引入新技术来解决所遇到的困难

##### 前端

- React 开发框架 + 组件库 + 代码编辑器
- 前端工程化:ESLint + Prettier + TypeScript

##### 后端

- Java Spring Boot + MySQL + MyBatis Plus
- Java命令行应用开发
- FreeMarker模板引擎
- Vert.x响应式编程
- Caffeine + Redis 多级缓存
- 分布式任务调度系统
- 多种设计模式
- 多种系统设计的巧思
- 对象存储

理想总是丰满的，而现实却是骨感的，为自己加油！