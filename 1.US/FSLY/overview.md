以下是关于 **Fastly (NYSE: FSLY)** 的深度研报简析。

---

# Fastly (FSLY): 被误解的“管道工”，开发者手中的“法拉利”

### 第一部分：核心画像与赚钱逻辑（ The Business & The Model ）

**1. 定位与差异化：不是搬运数据的“管道”，是边缘的可编程计算机**

用一句人话讲：Fastly 表面上是做 CDN（内容分发网络）的，就是帮你把网站图片、视频加速传给用户的；但它的骨子里，卖的是“边缘侧的控制权”。

- **痛点解决：** 传统 CDN（如 Akamai）是黑盒，配置改动要等很久才生效，且难以定制逻辑。Fastly 解决了现代互联网公司（尤其是流媒体、电商）对**即时性**和**可编程性**的变态需求。
    
- **核心护城河 (Moat)：**
    
    - **技术架构 (Instant Purge)：** 这是它的杀手锏。别的 CDN 清除缓存可能要几分钟甚至几十分钟，Fastly 可以在 **150 毫秒**内完成。这对于甚至需要根据库存实时显示页面的电商（如 Shopify）或突发新闻媒体（如 NYT）是刚需。
        
    - **开发者生态 (Developer Love)：** Fastly 允许开发者通过 Varnish 配置语言 (VCL) 或 WebAssembly (Wasm) 直接在边缘节点写代码。这不是简单的“缓存”，而是把服务器的逻辑推到了离用户最近的地方。这种**“高转换成本”**极高，一旦工程师在 Fastly 上写了复杂的边缘逻辑，很难迁移。
        

**2. 行业地位：高端市场的“特种部队”**

在 CDN 和边缘计算江湖里：

- **Akamai** 是老迈的帝国（Market Leader，规模大但笨重）；
    
- **Cloudflare** 是覆盖全网的防暴警察（主打安全、免费/低价策略通吃中小微）；
    
- **Fastly** 则是装备精良的**特种部队**。它不追求客户数量的绝对值，而是死磕Enterprise（大企业）客户。它的客户名单很少，但全是“大鱼”：Stripe, Shopify, Spotify, GitHub, New York Times。
    

**3. 单位经济模型 (Unit Economics)**

Fastly 的赚钱逻辑是典型的 **Usage-Based（按量付费） + Enterprise SaaS**：

- **收入公式：** $Revenue = (Traffic Volume \times Bandwidth Rate) + (Security Subscription) + (Compute Requests)$
    
- **核心矛盾：** 它的 Gross Margin（毛利）常年在 50%-60% 左右徘徊，远低于纯软件 SaaS 公司（80%+）。因为它是重资产模式，需要买服务器、付带宽费（COGS 高）。
    
- **流转逻辑：** 早期靠 CDN 流量（低毛利）作为**Hook（钩子）**获客，切入大客户的核心架构，然后通过 Upsell **安全产品（Signal Sciences）**和**边缘计算（Compute@Edge）**来拉升毛利和 LTV（生命周期价值）。目前的战略重点就是：**用安全产品给流量业务“输血”和“提纯”。**
    

---

### 第二部分：关键进化史（ How We Got Here ）

**1. 0-1阶段：程序员的怒火**

Fastly 的诞生源于创始人 **Artur Bergman** 的愤怒。作为 Wikia 的前 CTO，他受够了传统 CDN 的“慢”——改个配置要等 30 分钟。于是他基于开源项目 **Varnish** 搞出了一套能在边缘实时编程的系统。

- **切入点：** 既然打不过 Akamai 的规模，就打它“慢”；既然打不过 AWS 的全面，就打它“不好用”。Fastly 直接切入对技术要求最苛刻的**DevOps**群体，这奠定了它“For Developers”的硬核基因。
    

**2. 关键转折点 (Turning Points)**

- **IPO (2019) 与“TikTok 危机” (2020)：**
    
    上市初期风光无限，但在 2020 年遭遇黑天鹅。当时 TikTok 是 Fastly 最大的单一客户（贡献了约 12% 的营收）。由于特朗普政府的禁令威胁，Fastly 被迫剥离 TikTok 流量。
    
    - _Insight:_ 这是一次痛苦的 **Customer Concentration（客户集中度）** 风险教育，逼迫 Fastly 必须多元化，不能只靠几个巨头流量过日子。
        
- **收购 Signal Sciences (2020)：**
    
    这是 Fastly 历史上最重要的一步棋。它花大价钱买下了这家下一代 WAF（Web应用防火墙）公司。
    
    - _为什么关键？_ 纯 CDN 业务是“Race to the bottom”的价格战泥潭。Signal Sciences 带来了**高毛利的 Subscription 收入**，让 Fastly 从单一的“送水工”变成了“带保镖的送水工”。
        
- **管理层换血 (2022)：Todd Nightingale 入局**
    
    创始人 Artur 是典型的极客，更适合搞技术。公司在运营效率和销售上一直被华尔街诟病。2022 年，来自 Cisco 的 **Todd Nightingale** 出任 CEO。
    
    - _影响:_ Todd 带来了“成人监管”。他砍掉了不必要的实验性项目，专注于 **Go-To-Market (GTM)** 效率和降低 Burn rate。他的任务很明确：把这家技术牛逼但在商业上“偏科”的公司，变成一台能够盈利的机器。
        

---

### 第三部分：产品与生态流转（ Ecosystem & Value Chain ）

**1. 核心产品/服务矩阵**

- **Cash Cow（现金牛）—— Network Delivery (CDN)：**
    
    虽然毛利低，但是流量入口。负责让网页秒开、视频不卡。这是基石，没有这个就没有数据流。
    
- **Star（明星业务）—— Network Security (Next-Gen WAF):**
    
    基于 Signal Sciences 的技术。不同于传统防火墙靠“规则库”（容易误杀），它是靠算法动态识别攻击。这是目前提升 **Net Retention Rate (NRR)** 的主力。
    
- **Potential（潜力股）—— Compute@Edge:**
    
    这是 Fastly 的未来赌注。它允许客户把后端代码（比如用户身份验证、个性化推荐、A/B测试）直接部署在 Fastly 的节点上，而不用回源到 AWS 或 Google Cloud。
    
    - _逻辑：_ 只要 Compute@Edge 起来了，Fastly 就不再是管道，而是**全球分布式的 Serverless 平台**。
        

**2. 上下游生态与流转**

- **上游 (Supply Chain)：**
    
    - **数据中心与硬件：** Fastly 不像 hyperscalers 那样自建庞大的 DC，而是租用 Colocation (Co-lo) 空间，部署自己定制的高性能服务器（全是 SSD，大内存）。
        
    - **带宽供应商：** 也就是 ISP。Fastly 需要向一级运营商买带宽，这是它最大的成本项。
        
- **下游 (Customers)：**
    
    - **谁在买单？** 主要是**Best-of-breed** 策略的科技公司。他们通常已经用了 AWS，但觉得 AWS 的 CloudFront 不够灵活，或者太贵，所以把边缘层单独剥离给 Fastly。
        
    - **流转逻辑：**
        
        `原材料(内容/代码)` -> `源站(AWS/GCP)` -> **`Fastly Edge (缓存/计算/安全过滤)`** -> `最终用户`
        
        Fastly 卡在**云**和**人**之间。它做的越好，回源站的请求就越少，客户付给 AWS 的钱就越少（Egress cost saving），这也是客户愿意付钱给 Fastly 的原因之一。
        

**3. 竞争态势：三方混战**

- **Vs. Cloudflare (NET):**
    
    - 这是最直接的对手。Cloudflare 是“小米模式”，生态极广，免费起家，从下往上打；Fastly 是“苹果模式”（早期），专攻高端，从上往下打。
        
    - _劣势：_ Fastly 的销售团队规模和营销声量远不如 Cloudflare，产品迭代速度感觉也慢半拍。
        
- **Vs. Akamai (AKAM):**
    
    - Akamai 胜在规模和政企关系，但在敏捷性和开发者体验上完败给 Fastly。Fastly 正在一点点蚕食 Akamai 的高端媒体客户。
        
- **Vs. Hyperscalers (AWS CloudFront):**
    
    - AWS 的优势是“捆绑销售”。但 AWS 的 CDN 只是一个 Feature，不是 Product。对于只需简单加速的客户，AWS 够用了；但对于需要复杂边缘逻辑的，Fastly 依然不可替代。
        

### 总结：投资人视角的“感性认识”

Fastly 是一家“工程师浓度极高”的公司。它的技术栈（Varnish, Wasm）在圈内备受推崇，产品确实能打。

但在商业上，它一直处于一种“叫好不叫座”的尴尬境地：技术比 Cloudflare 还要硬核（在某些方面），但市值却被远远甩开。它目前的挣扎在于：如何从一个“昂贵的各种高性能工具库”，进化成一个“通用且高效的边缘云平台”，并证明自己在烧了这么多年钱后，能够实现真正的 GAAP 盈利。

如果你相信未来的互联网是**去中心化**的，逻辑处理会从云端下沉到边缘，且不仅是简单的缓存，而是复杂的计算，那么 Fastly 占据着极其关键的生态位。

---

**Would you like me to compare Fastly's financial metrics (Gross Margin, NRR, valuation multiples) directly against Cloudflare to see the valuation gap?**

![[截屏2026-01-28 21.00.09.png]]