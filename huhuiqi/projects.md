---
layout: page
title: 项目系统
---

# 智能数据管理工具
## （1） 数据库实时同步工具DB-Sync：
基于消息队列kafka中间层的上下游数据库同步程序。

##   (2)  Text2SQL智能报表
# 智能数据系统内核：


# 数据库系统内核：
## <font style="color:#DF2A3F;">（1） DaseX：内存查询计算引擎</font>
![](https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716816072-48eef1e4-7cad-4964-bc3f-b9e56fd33174.png)

仿照DuckDB写的，性能是DuckDB的1/3左右。项目已经停止，但积累了很多执行引擎前沿技术。



## （2）PG-RAC：基于PostgreSQL实现的多写可扩展共享缓存数据库
Share-storage/Share-memory的分布式数据库

+ 集群中任何节点访问数据库共享缓冲区，典型代表系统:Oracle RAC、DB2，核心技术问题:跨节点事务与数据冲突处理

## ![](https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716529616-9df97551-4df5-43f8-89a6-2ef7d0261553.png)
性能： 4节点下9:1读写负载近3.5X的扩展性，1:1读写负载，近2X的扩展性

<font style="color:rgb(0,0,0);">论文：PostgreSQL的共享缓存多写事务处理数据库 软件学报 2024</font>

## （3）Cedar：基于分布式LSM-tree的分布式数据库
![](https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716301996-ddb9f695-f4a6-4868-ac8d-e500ce059798.png)

数据学院数据库系统团队长期从事分布式数据库系统方面的研发工作。团队研发的分布式数据库系统 Cedar 具备高通量、高性能、高可用等特性，解决了大型银行、电信等行业的互联网级关键核心业务对数据库系统的需求。研发团队对分布式数据库系统的架构、功能和实施方案进行了重新思考。为了满足关键核心业务互联网化对系统扩展性和数据一致性的双重要求，Cedar 采用了读写分离的高并行系统架构，并在此架构的基础之上重新设计和实现了数据库的查询处理和事务处理功能。针对关键业务的高可用需求，Cedar 系统在读写分离的架构上又引入一主多备的多活架构, 创新成果发表在 SIGMOD，VLDB，ICDE，TKDE，ATC 等数据库与系统领域的顶级学术会议与期刊。

论文：[<font style="color:#000000;">Tao Zhu</font>](https://dblp.org/pid/21/2742.html)<font style="color:#000000;">, </font>[<font style="color:#000000;">Zhuoyue Zhao</font>](https://dblp.org/pid/181/5702.html)<font style="color:#000000;">, </font>[<font style="color:#000000;">Feifei Li</font>](https://dblp.org/pid/l/FeifeiLi.html)<font style="color:#000000;">, </font>[<font style="color:#000000;">Weining Qian</font>](https://dblp.org/pid/55/3364.html)<font style="color:#000000;">, </font>[<font style="color:#000000;">Aoying Zhou</font>](https://dblp.org/pid/z/AoyingZhou.html)<font style="color:#000000;">, </font>[<font style="color:#000000;">Dong Xie</font>](https://dblp.org/pid/20/6977-1.html)<font style="color:#000000;">, </font>[<font style="color:#000000;">Ryan Stutsman</font>](https://dblp.org/pid/02/1650.html)<font style="color:#000000;">, </font>[<font style="color:#000000;">HaiNing Li</font>](https://dblp.org/pid/202/3523.html)<font style="color:#000000;">, Huiqi Hu: Solar: Towards a Shared-Everything Database on Distributed Log-Structured Storage. </font>[<font style="color:#000000;">USENIX Annual Technical Conference 2018</font>](https://dblp.org/db/conf/usenix/usenix2018.html#ZhuZ0QZ0SLH18)<font style="color:#000000;">: 795-807</font>

[Ta](https://dblp.org/pid/21/2742.html)o Zhu, Zhuoyue Zhao, Feifei Li, Weining Qian, Aoying Zhou, Dong Xie, Ryan Stutsman, HaiNing Li, Huiqi Hu: SolarDB: Toward a Shared-Everything Database on Distributed Log-Structured Storage. ACM Trans. Storage 15(2): 11:1-11:26 (2019)

## （4）SlimStore：基于对象存储的数据库备份系统
云备份正成为用户灾难恢复的首选方式。除了其便利性外，用户更关注在大规模备份数据面前如何降低存储成本。数据去重是备份存储的有效方法，但当前的去重方法缺乏利用云资源为用户提供可扩展的备份服务，并不能满足不同备份版本的偏好。对于新的备份版本，用户希望更高的去重和恢复速度以减少等待时间。相反，减少存储成本对于旧备份版本更为必要。基于这些需求，SLIMSTORE提出了一种基于云的去重架构，将系统分解为存储层和计算层，支持弹性利用云资源。SLIMSTORE提出了两种不同设计重点的处理节点，以满足基于云的备份需求。L节点利用局部性和相似性，并采用历史感知策略提供快速的在线去重服务。L节点还优化了在线恢复，实现了高恢复效率。同时，G节点为旧版本提供精确的离线去重，并通过优化它们的物理存储来提高新版本的恢复性能。SLIMSTORE与一些最先进的去重和恢复方法进行了比较。实验结果表明，SLIMSTORE可以实现快速去重、高效恢复和有效的空间减少。此外，SLIMSTORE实现了可扩展的去重和恢复。

![](https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716929361-823ddd2e-c7bb-4d62-b0d0-f989430bd29c.png)

论文： Zihao Zhang, Huiqi Hu, Zhihui Xue, Changcheng Chen, Yang Yu, Cuiyun Fu, Xuan Zhou, Feifei Li:SLIMSTORE: A Cloud-based Deduplication System for Multi-version Backups. ICDE 2021: 1841-1846



## （5）Hockey：基于CK和傲腾持久内存改写的列存数据库
为了考虑成本和性能问题，分析数据库的存储引擎正在开并并融合不同设备使用。作为一种新颖的存储设备，Persistent Memory(PMem)也为混合存储提供了一个新的有前途的选择。Hockey是一种专为混合PMem-SSD存储而设计的高效列存储引擎。该系统的设计介绍了数据和元数据在PMem上的结构和访问方式，并阐述了系统在混合存储上数据放置策略。对于查询性能，Hockey在SSB上表现优异，相比其他存储引擎具有明显优势。

![](https://cdn.nlark.com/yuque/0/2024/png/43022042/1721717337946-9437d45d-3df5-43af-8919-6a334d220dc3.png)

性能：是普通SSD数据访问性能的5倍以上

论文： [Yuhang Jia](https://dblp.org/pid/129/4283.html), Huiqi Hu, [Xuan Zhou](https://dblp.org/pid/32/3943-1.html), [Weining Qian](https://dblp.org/pid/55/3364.html): Hockey: A Hybrid PMem-SSD Storage Engine for Analytical Database. [CIKM 2022](https://dblp.org/db/conf/cikm/cikm2022.html#JiaH0Q22) 

# 项目支持
自然科学基金面上		2024

科技部重点研发-子课题	2023

科技部重点研发-子课题	2023

上海市自然科学基金面上	2022

科技部重点研发-子课题	2017

自然科学基金青年基金	        2017

上海市扬帆青年基金		2017

# 智能数据管理工具与项目

每个项目以卡片形式展示：标题、图片（若有）、简短描述与论文/报告引用。

<div class="content-card">
	<h3>数据库实时同步工具 — DB-Sync</h3>
	<p>基于消息队列 Kafka 的上下游数据库实时同步程序，支持异构数据库之间的数据复制与一致性策略。</p>
	<p class="muted">（项目示例）</p>
</div>

<div class="content-card">
	<h3>Text2SQL 智能报表</h3>
	<p>面向业务用户的自然语言到 SQL 转换工具，支持智能报表自动生成与查询模板化。</p>
</div>

<div class="content-card">
	<h3>内核类项目概览</h3>
	<p>以下为数据库系统内核类研究与实现项目的概要介绍。</p>
</div>

<div class="content-card">
	<h3>DaseX：内存查询计算引擎</h3>
	<img src="https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716816072-48eef1e4-7cad-4964-bc3f-b9e56fd33174.png" alt="DaseX diagram">
	<p>仿照 DuckDB 开发的内存查询引擎，性能约为 DuckDB 的 1/3。项目虽已停止，但积累了丰富的执行引擎技术与经验。</p>
</div>

<div class="content-card">
	<h3>PG-RAC：基于 PostgreSQL 的多写可扩展共享缓存数据库</h3>
	<img src="https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716529616-9df97551-4df5-43f8-89a6-2ef7d0261553.png" alt="PG-RAC">
	<p>Share-storage / Share-memory 的分布式数据库原型。支持跨节点访问共享缓冲区，关注跨节点事务与数据冲突处理。</p>
	<p class="muted">性能（4 节点，9:1 读写负载）：近 3.5× 扩展性；（1:1 读写）近 2× 扩展性。</p>
	<p class="citation">论文：PostgreSQL 的共享缓存多写事务处理数据库（软件学报，2024）</p>
</div>

<div class="content-card">
	<h3>Cedar：基于分布式 LSM-tree 的分布式数据库</h3>
	<img src="https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716301996-ddb9f695-f4a6-4868-ac8d-e500ce059798.png" alt="Cedar">
	<p>Cedar 是一个面向互联网级关键业务的高通量、高可用分布式数据库系统。采用读写分离的高并行架构，并针对查询与事务处理做了重新设计。</p>
	<p class="citation">相关论文：SolarDB / Solar: Towards a Shared-Everything Database on Distributed Log-Structured Storage（USENIX ATC 2018；ACM Trans. Storage 2019）</p>
</div>

<div class="content-card">
	<h3>SlimStore：基于对象存储的数据库备份系统</h3>
	<img src="https://cdn.nlark.com/yuque/0/2024/png/43022042/1721716929361-823ddd2e-c7bb-4d62-b0d0-f989430bd29c.png" alt="SlimStore">
	<p>针对云备份与多版本备份的去重与恢复问题，提出分层的云备份架构与在线/离线去重节点设计，实现快速去重与高效恢复。</p>
	<p class="citation">论文：SLIMSTORE: A Cloud-based Deduplication System for Multi-version Backups. ICDE 2021</p>
</div>

<div class="content-card">
	<h3>Hockey：混合 PMem-SSD 列存引擎</h3>
	<img src="https://cdn.nlark.com/yuque/0/2024/png/43022042/1721717337946-9437d45d-3df5-43af-8919-6a334d220dc3.png" alt="Hockey">
	<p>为混合 PMem-SSD 存储优化的列存引擎，展示了在分析查询上显著的性能提升（在 SSB 基准上对比普通 SSD 达到 5 倍以上）。</p>
	<p class="citation">论文：Hockey: A Hybrid PMem-SSD Storage Engine for Analytical Database. CIKM 2022</p>
</div>

# 项目支持

- 自然科学基金面上 — 2024
- 科技部重点研发（子课题） — 2023
- 上海市自然科学基金面上 — 2022
- 科技部重点研发（子课题） — 2017
- 国家自然科学基金（青年基金） — 2017
- 上海市扬帆青年基金 — 2017
-  其他企业合作：阿里、蚂蚁、华为、中兴、美团、中远、电网等