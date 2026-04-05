你好。我们要拆解的公司是 **Snowflake Inc. (Ticker: SNOW)**。

在企业软件（Enterprise Software）的浩瀚星空中，Snowflake 曾经是那颗最耀眼的“妖股”。它打破了软件史上最大 IPO 纪录，甚至让巴菲特打破“不投科技股IPO”的惯例。

但如今，光环褪去，市场回归理性。作为买方分析师，我们需要剥离掉“云原生”、“数据湖仓”这些Buzzwords，看看它的底裤到底是什么。

---

### 第一部分：核心画像与赚钱逻辑 (The Business & The Model)

**1. 定位与差异化：云端数据的“瑞士”**

一句话定义：**Snowflake 是企业云端数据的“中央处理系统”和“中立国”。**

- **卖什么？** 它卖的不是简单的存储空间，而是**算力（Compute）**。企业把数据扔进去，查询、分析、共享数据所消耗的计算资源，才是Snowflake真正收费的核心。
    
- **解决什么痛点？**
    
    - **过去（Legacy）：** Oracle 或 Teradata 的本地部署太贵、太慢、扩容难。
        
    - **云初（Gen 1 Cloud）：** 亚马逊 Redshift 早期虽然在云上，但算力和存储绑定，你想存更多数据就得买更多算力，哪怕你不用来计算，这叫资源浪费。
        
    - **Snowflake的解法：** **存储与计算分离（Separation of Storage and Compute）**。存数据极其便宜（Pass-through cost），只有当你跑查询（Query）的那一秒，才开始计费。
        
- **护城河（Moat）：**
    
    - **多云中立性（Multi-Cloud Neutrality）：** 这是它最硬的牌。大企业不会把灵魂完全卖给 AWS 或 Azure，他们需要一个跨云的层。Snowflake 可以在 AWS、Azure、GCP 上无缝运行，充当了“数据瑞士”，避免了单一云厂商的 **Vendor Lock-in**。
        
    - **数据网络效应（Data Network Effect）：** 它的 "Data Sharing" 功能让公司 A 可以直接把数据权限开给公司 B，而不需要传统的 ETL 搬运。用的人越多，在这个网上流动的数据越有价值。
        

**2. 行业地位：从“颠覆者”到“守擂者”**

Snowflake 已经过了挑战者的阶段，它是目前**现代数据栈（Modern Data Stack）**事实上的 **Gold Standard（金标准）**。

但在 AI 时代，它正面临来自 **Databricks** 的猛烈进攻。如果说 Snowflake 是“把数据整得井井有条的图书馆（Data Warehouse）”，Databricks 就是“搞乱七八糟数据挖掘的实验室（Data Lakehouse）”。现在两家都在往对方的领地渗透，战况焦灼。

**3. 单位经济模型：Consumption-based 的双刃剑**

Snowflake 不像 Salesforce 那样按“人头”收 SaaS 订阅费，它是 **Consumption-based（按用量付费）**。

- **赚钱公式：** `Revenue = Data Storage (低毛利) + Compute Credits (高毛利核心)`
    
- **逻辑：**
    
    - **优点：** 门槛低（Land），客户用得爽了会自动扩容（Expand）。**Net Revenue Retention (NRR)** 曾常年保持在 150%+ 的变态水平（虽然现在降到了 120%+ 区间，但依然健康）。
        
    - **缺点：** 经济下行时，CFO 一勒紧裤腰带，砍掉非必要的查询，Snowflake 的收入会**即时**掉下来。相比 SaaS 订阅，它的收入预测（Visibility）更难，波动性更大。
        
- **LTV/CAC：** 极高。一旦企业把核心数据迁入 Snowflake，**数据引力（Data Gravity）** 会产生极高的转换成本。想搬走？脱层皮。
    

---

### 第二部分：关键进化史 (How We Got Here)

Snowflake 的发家史，是一部精准打击巨头软肋的教科书。

**1. 0-1 阶段：Oracle 叛军的复仇 (2012-2018)**

创始人 Benoit Dageville 和 Thierry Cruanes 是 Oracle 的顶级架构师。他们看透了老东家架构的僵化，却在内部推不动改革，于是拉上荷兰人 Marcin Zukowski 出来单干。

- **切入点：** 彻底重写代码库，针对**云（Cloud Native）**设计。
    
- **核心创新：** 也就是前面提到的“存算分离”。这在当时是反直觉的，因为传统观点认为存算在一起才快。但他们利用云的无限带宽证明了：分开更灵活，且够快。
    

**2. 关键转折点 (Turning Points)**

- **Slootman 时代与 IPO (2019-2024)：** 董事会请来了硅谷传奇 CEO **Frank Slootman**。这人是个冷酷的“销售机器”。他把 Snowflake 从一家技术极客公司变成了一支纪律严明的销售铁军。2020年的 IPO 更是将市场情绪推向高潮。
    
- **Data Cloud 转型：** 以前只叫“数据仓库”，后来重新定位为“Data Cloud”。这不只是改名，而是战略上强调**数据流通和交易**，试图打造数据界的 App Store。
    
- **AI 恐慌与换帅 (2024)：** 生成式 AI 爆发，市场担心 Snowflake 的结构化数据架构不适合跑大模型（LLM）。股价承压。Slootman 退休，换上了前 Google 广告高管、AI 专家 **Sridhar Ramaswamy**。
    
    - _Signal：_ 这标志着 Snowflake 承认：光靠卖数据库不行了，必须全力切入 AI 和应用层。
        

**3. 管理层基因**

- **过去：** 极致的工程 + 极致的销售（Slootman effect）。
    
- **现在：** Sridhar 代表着 **Product & AI First**。他不仅要守住数据，还要让客户在 Snowflake 上直接训练和部署 AI 模型（Cortex, Snowpark）。这是一个巨大的赌注，旨在证明 Snowflake 不会在 AI 时代被边缘化。
    

---

### 第三部分：产品与生态流转 (Ecosystem & Value Chain)

**1. 核心产品矩阵**

- **Cash Cow（现金牛）：** **Data Warehouse**。传统的 SQL 查询，报表分析。这是底盘，虽然增速放缓，但贡献绝大部分现金流。
    
- **Star（明星）：** **Snowpark**。允许开发者用 Python、Java 而不只是 SQL 来操作数据。这是为了抢 Databricks 的地盘，吸引数据科学家。
    
- **Bet（赌注）：** **Cortex / AI**。完全托管的 AI 服务，让企业在不把数据移出的情况下，用 LLM 跑文档分析、客服机器人等。
    

**2. 上下游生态：微妙的“友敌”关系**

Snowflake 处在一个非常尴尬但又精妙的生态位：

- **上游（Suppliers/Frenemies）：** **AWS, Azure, GCP**。
    
    - _风险点：_ Snowflake 建立在这些巨头的基建之上，要把收入的很大一部分作为 **COGS（销货成本）** 支付给云厂商。而且，这些云厂商自己也有竞品（AWS Redshift, Google BigQuery）。
        
    - _制衡：_ 云厂商虽然恨它抢生意，但又不得不爱它带来的巨大底层消耗（Compute/Storage consumption）。
        
- **下游（Customers）：** Global 2000 企业。
    
    - 决策者通常是 CIO（首席信息官）或 CDO（首席数据官）。
        
    - 由于是按量付费，Snowflake 必须不断讨好开发者和数据分析师，让他们觉得“好用”，从而跑更多的 Query。
        

**3. 竞争态势：三方混战**

- **头号死敌：Databricks**。
    
    - _Databricks 优势：_ 处理非结构化数据（图片、视频、文本）起家，AI 基因极强，深受数据科学家喜爱。
        
    - _Snowflake 优势：_ 简单易用，SQL 基础深厚，深受商业分析师（Business Analyst）喜爱，数据治理和安全性更好。
        
    - _战况：_ Databricks 在搞 "Data Warehouse"，Snowflake 在搞 "AI/Python"，双方都在攻入对方腹地。
        
- **隐形杀手：Open Table Formats (Iceberg)**。
    
    - 现在流行一种趋势：数据以开源格式（Apache Iceberg）存储，不再锁死在 Snowflake 的私有格式里。这可能导致 Snowflake 的“护城河”变浅——如果存储变得通用，计算层（Compute）的竞争将更加血腥（Commoditization）。
        

### 总结与下一步

Snowflake 是一家**商业模式极其性感（高转换成本+网络效应），但估值逻辑正在重构**的公司。

它不再是那个“闭着眼买”的高增长神话。目前的它，正处在从“存储逻辑”向“AI 计算逻辑”惊险一跃的半空中。如果 Sridhar 能成功让企业在 Snowflake 上跑通 AI 应用，它的 TAM（潜在市场规模）将翻倍；如果输给 Databricks，它将退化为一个昂贵的传统数仓。

**Next Step for You:**

你想让我深入对比一下 **Snowflake 和 Databricks 的最新财报核心数据（如 NRR, Revenue Growth, RPO）**，还是想看一看 **华尔街对它 AI 产品（Cortex）的具体落地反馈**？

![[截屏2026-01-28 21.45.05.png]]