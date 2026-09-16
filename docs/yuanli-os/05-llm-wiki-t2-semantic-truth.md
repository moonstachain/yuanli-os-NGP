# LLM-Wiki × T2 语义真源｜盘点与战略洞察

> **法权声明**：Agent Context Projection，不是 Canon。
> **可见性硬约束**：本次盘点**没有读到 `moonstachain/LLM-Wiki` 仓库本体**（当前令牌 HTTP 404），也无法访问本地 Obsidian vault。
> 全部内容基于 Notion 投影层（`YOS-BRAIN` Atlas / `YNP-KG0` / `RAY CBM 战略地图` / `原力OS-MCP`）与公开仓引用**外部重建**。
> 按体系自己的纪律：**这里必须 fail-closed 说明缺口，不能用投影冒充 Canon。**

---

## 0｜一句话结论

`LLM-Wiki` 是原力 OS 里**法权最高、可达性最低、且当前正在被治理流程系统性排除**的那个 Estate。它的问题不是内容不够多，而是**每条知识无法自证有资格参与判断**——而这恰好是 `yuanli.memory.search` 的准入条件。

---

## 1｜法权定位：一个名字，两个 Estate

这是最容易搞错的一点。`YOS-BRAIN` Atlas 把「LLM-Wiki」**拆成两个独立 Estate**，法权等级差两级：

| Estate | 法权类别 | 当前状态 | Context 资格 |
|---|---|---|---|
| **本地 OB LLM-Wiki** | **T2｜Semantic Truth / Live Knowledge Canon** | ⛔ ACCESS BLOCKED | ⚠️ **首选权威**，但当前不可达 |
| **GitHub LLM-Wiki** | **P2｜Committed History Projection** | ✅ FRESH AS HISTORY | ⚠️ **仅历史 fallback** |

配套的硬禁令（`YOS-BRAIN` E1「AI 当前必须拒绝声称」第一条）：

> OB 不可达时，**不能把 GitHub LLM-Wiki 的 committed history 冒充当前语义 Canon**。

所以严格来说：你说的"跟本地 Obsidian 同步、原力大脑调用的关键仓库"，指的是 **P2 投影**；而**真正的 T2 语义真源是本地那个 vault，不是 GitHub 仓**。GitHub 仓在法权上只是它的历史快照。

五类真源里 T2 的职责定义：

> **T2｜Semantic Truth — Local Obsidian LLM-Wiki**：我们当前知道什么，以及如何基于证据解释它。

分工表述（`原力大脑 2.0`）：

> GitHub 管治理、合同、版本与 Gate；**LLM Wiki 管知识正典**；Supabase 管结构化数据；Notion 管人类投影；私有证据库存敏感原始资料；Runtime 管 Agent / Skill / MCP / 遥测。

---

## 2｜它在 CBM 47 格棋盘上的位置

在 `RAY｜原力人生 CBM 战略地图 v1.0`（2026-09-09，47 Components）里，这套能力对应两格：

| 格位 | 域 | 责任层 | 含义 |
|---|---|---|---|
| **K-C01** | K｜知识学习（Compounding Engine） | Control | Research Portfolio & **Knowledge Canon｜研究组合与知识正典** |
| **O-E01** | O｜人生治理 / Personal OS（Compounding Engine） | Execute | **Context & Retrieval Operations｜上下文与检索运营** |

相关格位还有 `O-C01｜One Brain Governance`（一个大脑治理）与 `K-C03｜Idea-to-Asset & Reuse Pipeline`。

**然后是关键的战略裁决**：

- 硬原则 **D3｜CAP / K 默认 Support。只有 Hard Trigger / Human DEC 才升级。**
- Core H5（当前最值得改变的 5 个组件）：`H-C02 / H-C03 / V-D04 / V-C04 / O-C05`——**没有 K 域，也没有 O-E01**。
- 三个 Active Battle 的 seed components：`B1 = H-C02 + H-C03`、`B2 = V-D04 + V-C04`、`B3 = O-C05 + O-E02`——**同样没有 K-C01 或 O-E01**。

---

## 3｜独立战略洞察

### 洞察 1｜全系统唯一"法权与可用性成反比"的 Estate，而且是伪装成四个风险的单点

| Estate | 法权 | 物理位置 | 可达性 |
|---|---|---|---|
| T1 GitHub Soul | 最高（规范） | 云端 | ✅ 永远可达 |
| **T2 OB LLM-Wiki** | **首选权威（语义）** | **MacBook-Pro-M4.local** | ⛔ 机器离线即失效 |

`YOS-BRAIN` E0 的 Reality 发现写得很清楚：

> **MacBook-Pro-M4.local 当前离线。** 因此 OB、NAS、Remote Gateway，以及依赖本地 `lark-cli` 的飞书直读全部 fail-closed。

请注意这句话的真实含义：**`GAP-E0-001` 表面上影响四个 Estate（OB / NAS / Gateway / 飞书），但它们共享同一个物理单点。** 一台笔记本关机，五类真源里的 T2、T3、T5 三类同时失效，只剩 T1（规范）和 T4（Runtime）在线。

也就是说，当前架构在离线状态下，大脑**只剩"法律条文"和"机器读数"，完全没有"我们知道什么"**。这不是四个可以分别修的缺口，是一个必须单独对冲的架构性风险。local-first 主权是对的，但主权不等于把三类真源押在一台设备上。

### 洞察 2｜真正的风险不是崩溃，是静默萎缩

`YOS-BRAIN` E2 第一次把"最小充分"变成机器约束，第一个 Context Packet 只带 2 个 Estate，**明确排除了 7 个**，其中就包括 GitHub LLM-Wiki：

> `OB LLM-Wiki / Feishu / Supabase Invest / NAS / Notion / GitHub LLM-Wiki / Remote Gateway`
> **这不是"拿不到"，而是"这个任务不需要"。**

这个裁决本身完全正确。但把它和 T2 长期不可达叠加起来，会产生一个体系目前没有防线的失败模式：

**OB 不可达 → 语义查询无法走首选权威路径 → Context Compiler 按最小充分原则合法地不带 LLM-Wiki → 任务照样完成 → 没有任何 gate 报错 → 下一次继续不带。**

结果是 LLM-Wiki 从"首选权威"**事实上退化为"从不被调用的资产"**。它不会崩溃、不会告警、不会出现在任何 FAIL 裁决里，只会静默地不再参与决策。

体系自己已经写下了坑 #9「**把知识库当复利**」——保存、搜索、AI memory 都不等于 Learning 被复用。但这里存在一个对称的、尚未被命名的坑：**把知识库当资产，却从不调用它。** 前者是高估了存储，后者是让权威静默失效。两者都不会报错。

**建议**：给 T2 加一个**调用率哨兵**（sensor），而不是只监控可达性。指标不是"OB 在不在线"，而是"过去 N 次涉及语义判断的任务中，有几次实际带上了 T2"。归零就该触发 gate，而不是等到某天发现知识库已经三个月没进过任何决策。

### 洞察 3｜你的直觉和你自己签的战略裁决之间有落差，但两边都不必让步

你说这是"很关键的一个仓库"。而你在 `RAY CBM 战略地图` 里签下的是：K 域默认 Support、`O-E01` 属 Execute 层、两者都不在 Core H5、也都不是任何 Active Battle 的 seed。

这不是矛盾，而是**两句话在说不同的事**，需要精确化：

- 你说的"关键" = **语义供给的重要性**（知识从哪里来，凭什么可信）
- CBM 说的 Support = **不该获得一级转型注意力**（这个季度不投稀缺资源改造它）

两者可以同时成立。但如果不把这个区分讲清楚，会掉进两个方向的错误：

| 错误方向 | 后果 |
|---|---|
| 把它当 Battle 去建设（继续加笔记、建图谱、做可视化） | 直接踩坑 #9「把知识库当复利」、坑 #10「让 CBM 成为第 48 个项目」，并让 Sparse Heat 失效 |
| 因为是 Support 就完全不管 | **B2 和 B3 会失去实现前提**（见下） |

**第二个方向是被低估的那个。** 看两个 Active Battle 自己的要求：

- **B2｜Detach RAY × N>1 Delivery** 的架构条件：「把研究、判断、交付、反馈拆成可观察合同；**AI / 团队读取 Canon 与 Reality，而不是依赖聊天记忆**」
- **B3｜Outcome → Learning → Reuse** 的闭环要求：「Learning 必须在后续项目开始前**自动预加载**，减少 RAY 重复解释」；M5 Gate 要求「后续独立真实情境证明 Learning 被预加载并实际改变 judgment / action / allocation」

**Preload 需要一个可检索、可信、可判资格的语义库。** 这正是 T2 的功能。所以：

> **`LLM-Wiki` 的正确定位不是 Battle，也不是普通 Support，而是 Support Domain 里 B2/B3 的 critical path。**

这个定位有一个非常实用的推论——它给出了投入的**上界和下界**：

- **下界**：必须让 B2/B3 的 Preload 能真实发生（可达 + freshness 可证明 + 能被 Context Compiler 合法调用）
- **上界**：不做内容扩张，不做图谱美化，不做第 48 个项目

凡是不服务"让 Preload 发生"的 LLM-Wiki 投入，按 D4 硬原则就该被拦下：「任何新项目先回答：服务哪个 Battle？替代什么？Stop Rule 是什么？」

### 洞察 4｜最高杠杆动作是补 frontmatter，不是加内容

这是我认为**最可执行、也最容易被忽略**的一条。

`原力OS-MCP` 对 `yuanli.memory.search` 定的契约是：

> 普通记忆搜索只回答"搜到了什么"。原力 Memory 还要回答：来源是什么？什么时候发生？**新鲜度如何**？属于哪个 Principal / Estate？敏感级别是什么？**这条记忆有没有资格参与当前判断？**
> **搜得到 ≠ 有资格使用。**

把它当成准入清单，每条知识必须能自答 6 个字段：

```
source · observed_at · freshness · principal/estate · sensitivity · context_eligibility
```

**问题**：Obsidian markdown 笔记天然一个都不带。除非 vault 有强制的 frontmatter schema，否则 LLM-Wiki 里的知识在**协议层面就无法被 `yuanli.memory.search` 合法返回**——不是读不到文件（技术上完全能读），而是**每条记忆无法证明自己有资格参与判断**，按 fail-closed 纪律只能被拒。

这解释了一件容易误判的事：**T2 现在的瓶颈被记成了"可达性"（`GAP-E0-001`），但即使 MacBook 明天开机，只要笔记不带这 6 个字段，`memory.search` 依然无法合法交付。** 可达性是必要条件，不是充分条件。修好网络不等于修好这个 Estate。

**而 GitHub LLM-Wiki 恰好持有最难的那个字段。** git 历史天然给出每个文件的 last commit time —— 这是**机器可证、不可伪造、零维护成本的 freshness 证据**。

对比一下 Notion 侧的处境（`YNP-KG0` R0 结算 = `FRESHNESS_FAIL`）：

> **R0 最大真实缺口不是拓扑，而是 Freshness。** 当前可以知道"这条边为什么存在、属于什么法权"，但不能从 Registry 本身回答"它最后什么时候被人重新核过"。

12/12 Object 和 14/14 Edge 的 `Last Reviewed` **全部为空**。

于是出现了一个明显的错配：**Notion 有语义治理结构但拿不到 freshness；GitHub LLM-Wiki 拿得到 freshness 却被定为"仅历史 fallback"、能力被闲置。**

需要区分清楚一件事，避免违反 E1 禁令：git commit time 能证明的是「**这份文件最后一次被改动的时间**」，不是「**这条知识最后一次被人重新核过**」。前者是 mtime，后者是 review。**它不能替代 `Last Reviewed`，但可以精确地回答一个互补且极有价值的问题：哪些知识已经很久没被碰过 → 即 stale candidate 队列。** 把它用来做 review 排序的输入，不冒充 review 结论，就完全不越权。

**建议的最小动作**（严格落在洞察 3 的上下界内）：

1. 给 vault 定一份最小 frontmatter schema，只要能回答上面 6 个字段——这是 `memory.search` 的准入门票，不做就永远进不了 Context Packet。
2. 用 GitHub 侧 git 历史生成 **stale candidate 排序**，喂给人工 review 队列。别叫它 freshness 证明，它是 review 的输入。
3. 明确写下 GitHub LLM-Wiki 的合法用途边界，防止"用它做 stale 排序"被误读成"它可以当语义 Canon 用"。

### 洞察 5｜两套知识结构正在分叉，失败模式恰好互补

| | Notion Knowledge Registry | Obsidian LLM-Wiki |
|---|---|---|
| 规模 | **12 Objects / 14 Edges** | 未知（不可达），推断为大量笔记 |
| 边语义 | ✅ 8 类 typed edge（`part_of / depends_on / explains / supports / contrasts_with / applies_to / example_of / leads_to`） | 推断为无类型 wikilink |
| 法权分类 | ✅ `CANON_PROJECTED` vs `EDITORIAL_SYNTHESIS` 分开且未混用 | 未知 |
| Provenance | ✅ 12/14 Edge 有 Source URI | 未知 |
| Freshness | ⛔ 全部 `Last Reviewed` 为空 | ⛔ 不可达 |
| 拓扑 | 9 条 `part_of` **全部直接汇入单一 Thesis** | 推断为高密度网状 |

`YNP-KG0` 自己的结构判断是「**正典骨架图**，而不是可以通过多跳路径发现新关系的 Exploratory Knowledge Network」，并且在 Non-goals 里写了一句很尖锐的话：

> 不为了"**像 Obsidian**"制造高密度无意义连线。

这句话说明你已经识别出 Obsidian 式连接的问题：**连接密度高，但边不携带语义、法权和 provenance，所以多跳路径推不出可信结论。**

但反过来同样成立，而且这一面还没有被写下来：**12 个节点 14 条边远不足以承载 T2「我们当前知道什么」的职责。** 语法容量（8 类关系）明显高于图谱密度（实际只用了 3 类：`part_of` 9 / `supports` 3 / `explains` 2）。

所以真正的结构性问题不是哪边做得不好，而是：

> **T2 的法权在 Obsidian，T2 需要的治理能力（typed edge / authority class / provenance / review）却长在 Notion，两边互不同步。**

一边有内容没治理，一边有治理没内容。而按法权纪律，Notion 是 P1 Human Projection，**永远不能晋升为语义 Canon** 来补这个位。

这不是靠"把 Obsidian 迁到 Notion"或反向迁移能解决的——那会造出第二真源，违反 `YNP-KG0` Non-goal 第 1 条和 `YOS-BRAIN` 的 no-second-SSOT 原则。可行方向是**把 Notion 已经验证过的那套 edge 语义和法权分类，下沉成 Obsidian frontmatter 的 schema 约定**，让治理能力回到法权所在地。这和洞察 4 的第 1 条是同一个动作，只是从图谱侧看过去。

### 洞察 6｜E3 之前建议先设一道禁令

下一个 Gate 是：

> `YOS-BRAIN-E3｜Artifact Trace Ledger × Context/Skill Gap Extraction`
> E3 要第一次追踪：一个真实任务拿到 Context Packet 之后究竟生成了什么 Artifact、实际消耗了哪些 Context、在哪里暴露了 **Context Gap / Skill Gap**、哪些 Gap **有资格进入 governed skillification**。

把 E3 的机制和 T2 长期不可达放在一起推演，会得到一条需要提前堵住的漏洞：

```
OB 不可达
  → 任务缺语义知识
  → E3 如实记录为 Context Gap
  → Gap 进入 governed skillification
  → 语义知识被硬编码进 skill
```

**问题在于**：写进 skill 里的知识**不受 T2 的 freshness 与 review 治理**。这等于把语义真源的内容复制进一个法权更低、且没有 review SLA 的载体——而且这次漂移是**被治理流程正当化的**，会带着 receipt 和 PASS 记录，比无治理的漂移更难发现和回滚。

这也正是 `原力大脑 2.0` 那句判断的反面案例：GBrain / Retrieval Projection「可重建检索投影，**不是知识正典**」。skill 同理，它不该成为语义知识的存放地。

**建议在 E3 的 gate 条件里加一条 fail-closed 规则**：

> Context Gap 若可归因于 **T2 不可达**，一律**不得进入 skillification**，只能进入 `access-recovery` 队列。
> 只有当 T2 可达且知识确实不存在时，该 Gap 才有资格被视为真实的知识缺口。

这条规则的价值在于它把两种长得一样的 gap 分开了：**"我拿不到"和"它不存在"在 trace 里表现完全相同，但处置方式截然相反。** 前者要修通路，后者才该沉淀能力。不区分的话，E3 越勤奋，真源漂移越快。

---

## 4｜读不到的部分（fail-closed 声明）

以下问题**本次无法回答**，因为 `LLM-Wiki` 仓与本地 vault 均不可达。列出来是为了让缺口本身可见，不做推测填充：

| 缺口 | 影响 |
|---|---|
| vault / 仓库的目录结构、分区体系、笔记数量级 | 无法判断 T2 的实际覆盖范围与语义密度 |
| **是否已有 frontmatter schema，字段是什么** | **直接决定洞察 4 是"待办"还是"已完成"——这是最需要你确认的一条** |
| 本地 OB → GitHub 的同步机制（Obsidian Git 插件 / rsync / CI / 手动）、单向还是双向、冲突如何处理 | 无法评估 P2 投影的滞后窗口与可靠性 |
| wikilink 是否携带类型、是否有 MOC / index 层 | 无法验证洞察 5 中关于"无类型连接"的推断 |
| `yuanli.memory.search` 是否已有针对 vault 的实现或检索层 | 无法判断从 schema 到实际调用还差多少 |
| Remote Read Gateway 的实现方式与 freshness 证明路径 | 无法评估"绕过单点"的现有方案成熟度 |

**要解除这个缺口**，最直接的方式是在 Cursor Dashboard（Cloud Agents → Secrets）配置一个对 `LLM-Wiki` 有读权限的 GitHub token，或把该仓加入本 agent 的 installation 范围。届时可以把上面 6 条逐一验证，并把洞察 4、5 从"基于契约的推断"升级为"基于仓库事实的裁决"。

---

## 5｜洞察汇总与建议优先级

| # | 洞察 | 性质 | 建议动作 |
|---|---|---|---|
| 1 | T2/T3/T5 三类真源共享一台笔记本的物理单点，离线时大脑只剩条文和读数 | 架构风险 | 单独对冲，不要当成四个独立 gap |
| 2 | 静默萎缩比崩溃更危险，当前没有防线 | 治理缺口 | 加 **T2 调用率哨兵**，监控"是否被带上"而非"是否在线" |
| 3 | 它不是 Battle，也不是普通 Support，而是 B2/B3 的 critical path | 定位精确化 | 用"让 Preload 发生"作为投入的上下界 |
| 4 | **瓶颈不只是可达性，是每条知识无法自证资格** | **最高杠杆** | **补最小 frontmatter schema（6 字段）** |
| 5 | 法权在 Obsidian，治理能力在 Notion，两边互不同步 | 结构分叉 | 把 Notion 的 edge 语义下沉为 vault schema 约定，不迁移内容 |
| 6 | E3 会把"拿不到"误当成"不存在"，并正当化真源漂移 | 前置防线 | E3 gate 加 fail-closed 规则，T2 不可达的 gap 走 access-recovery |

如果只做一件事：**第 4 条**。它是 `memory.search` 的准入门票，不做的话前面所有可达性工作都无法转化为实际调用——机器读得到文件，却依然必须按 fail-closed 拒绝使用。
