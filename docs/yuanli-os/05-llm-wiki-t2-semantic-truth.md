# LLM-Wiki × T2 语义真源｜盘点与战略洞察

> **法权声明**：Agent Context Projection，不是 Canon。
> **可见性硬约束**：**没有读到 `moonstachain/LLM-Wiki` 仓库本体**（令牌 HTTP 404），也无法访问本地 Obsidian vault。
> 结构与机制部分基于 **90 个公开仓的全库检索**重建（LLM-Wiki 相关 408 行匹配、Obsidian 772 行）；
> 法权与状态部分基于 Notion 投影层（`YOS-BRAIN` Atlas / `YNP-KG0` / `RAY CBM 战略地图` / `原力OS-MCP`）。
> 按体系自己的纪律：**必须 fail-closed 说明缺口，不能用投影冒充 Canon。** 仍未解答的问题见第 7 节。

---

## 0｜一句话结论

`LLM-Wiki` 的架构设计成熟度远高于它的**数据合规度**：4 层写权限白名单、typed-edge schema、lint 工具链、单向镜像同步都已实现，但 **1078 条 concepts 至今"按目录推断"而非填写 frontmatter**，且 schema 缺 3 个法权字段。结果是——机器读得到文件，每条知识却无法自证有资格参与判断，而这正是 `yuanli.memory.search` 的准入条件。

体系自己给了一句最好的定位：

> **LLM Wiki 负责记住；GBrain 负责想起。**

---

## 1｜法权定位：一个名字，两个 Estate

`YOS-BRAIN` Atlas 把「LLM-Wiki」**拆成两个独立 Estate**，法权等级差两级：

| Estate | 法权类别 | 当前状态 | Context 资格 |
|---|---|---|---|
| **本地 OB LLM-Wiki** | **T2｜Semantic Truth / Live Knowledge Canon** | ⛔ ACCESS BLOCKED | ⚠️ **首选权威**，但当前不可达 |
| **GitHub `llm-wiki`**（私有镜像） | **P2｜Committed History Projection** | ✅ FRESH AS HISTORY | ⚠️ **仅历史 fallback** |

配套硬禁令（`YOS-BRAIN` E1「AI 当前必须拒绝声称」第一条）：

> OB 不可达时，**不能把 GitHub LLM-Wiki 的 committed history 冒充当前语义 Canon**。

**这一点在公开仓有硬证据**，不只是 Notion 投影。`yuanli-strategy-web/src/data/estate.ts` 是一份公开可读的 estate 数据：

```
id: 'llm-wiki'
fullName: 'moonstachain/llm-wiki'
primaryRole: 'committed_knowledge_history_projection'
upstream: ['local://obsidian/llm-wiki']
downstream: ['GBrain rebuild', 'EVD']
semanticStatus: 'PROJECTION_OF_KNOWLEDGE_CANON'
notes: ['LLM Wiki 负责记住；GBrain 负责想起。', 'GitHub projection 不等于 Local Canon。']
```

同文件把 C2 的 repo 标为 `local LLM Wiki + GitHub projection`，GBrain 标为 `REBUILDABLE_RUNTIME`。

**Live master 的物理位置**：`/Users/liming/Documents/LLM-Wiki/`（多个公开仓硬编码）。

**三层分工**（与 T1 的边界，公开表述）：

| 层 | 载体 | 管什么 |
|---|---|---|
| T1 Normative | `yuanli-strategy-soul` | 允许 / 禁止 / 版本 / Admission |
| **T2 Semantic** | **本地 OB LLM-Wiki** | **当前知道什么、如何基于证据解释它** |
| T2 Projection | `moonstachain/llm-wiki` | committed history，非 live Canon |
| Serving | GBrain / Vector / Graph | 可重建检索投影，**不得反写 Canon** |

`yuanli-strategy-trilogy/books/03-原力OS/最小闭环.md` 有一句很精确的双源标注：`真源：LLM-Wiki/concepts/mvp-closure.md + 原力OS canon`——**概念在 T2，规范在 Soul。**

---

## 2｜实际结构（公开仓可重建部分）

### 2.1 规模

| 项 | 数量 | 口径 |
|---|---|---|
| `sources/` | **约 6108 文件** | `yuanli-os-company-brain-skill/references/three-circles-protocol.md` |
| `concepts/` | **约 1078 页** | 同上（2026-05 口径） |

### 2.2 结构 A｜Company Brain 4-Layer（agent 读写治理视图）

来源：`os-yuanli-share-max/profiles/yuanli-full/sample-wiki/_schema.md`

```
Layer 1 · Raw Sources     sources/{articles,papers,books,transcripts}/ + artifacts/
                          ★ 只读，LLM 只读不改
Layer 2 · Wiki Pages      entities/{people,companies,projects}/ · concepts/
                          comparisons/ · syntheses/ · operations/{clones,skills,runs}/
                          ★ 可写
Layer 3 · Human Insights  insights/
                          ★ 人类专属，LLM 永不修改（铁边界）
Layer 4 · Metabolism      _factory/ · _staging/ · _feedback/
```

**写权限白名单**（明确列出，不在名单内即禁写）：

```
concepts/ · entities/ · syntheses/ · comparisons/ · operations/ · dashboards/ · _factory/ · _staging/
```

这里最值得注意的是 **Layer 3 铁边界**：`insights/` 是人类专属，AI 永不写。这条设计非常强——它保证了最高价值的人类洞察不会被 AI 生成内容污染。AI 想让洞察进入 T2，必须走 Layer 4 `_factory/` / `_staging/` 代谢层再经人审，路径闭合。

`_factory/` 的四个子目录 `lessons/ evolutions/ skills/ patterns/` 恰好对应 `04-method-stack.md` 里信息 5 层的固化落点——`patterns/` 就是 L5「单 / 框架」的归档地。

### 2.3 结构 B｜绿皮书 14 域（组织归档视图）

来源：`yuanli-os-greenbook/附录-工具卡/A06-LLM-Wiki-14域索引.md`

```
LLM-Wiki/
├── _factory/    lessons/ evolutions/ skills/ patterns/
├── domains/     01-charity/ … 14-family-office/
├── personal/    [姓名]/{first-week,notes,projects}/
└── public/      orange-book/ green-book/ glossary/
```

命名约定：`domains/[域编号]-[域名]/[域编号]-[年月日]-[类型]-[简述].md`

**这两套结构不是两个仓库，是同一 vault 的两套索引 / MOC**：4-layer 面向 agent 读写治理，14 域面向「八万四千管培」的组织归档。

### 2.4 根目录关键文件

从 `os-yuanli-share-max/profiles/yuanli-full/wiki-adapter.md` 的路径替换表反推：

```
_schema.md                              schema 定义
_index.md                               总索引
_ai-entry.md + _hot.md                  Karpathy 入口层，~20–30× token 压缩
_bridge-log.jsonl                       桥接日志
dashboards/metabolism-dashboard.md      代谢看板
scripts/close_task_hook.py              任务关闭 hook（opt-in）
```

### 2.5 Frontmatter schema 现状

sample 版 7 个字段：

```yaml
title · type · sources · related · created · updated · audience
```

**但存量数据没有填。** `three-circles-protocol.md` 写得很直白：

> **Phase 2 不强制 frontmatter 全填**：1078 wiki concepts 仍按目录推断

### 2.6 六个 ontology lens

`feishu-expert-brain-architect/references/architecture-card.md`：

```
yuanli-juexing · yuanli-chuangye · yuanli-caifu · lianghua-touzi · yuanli-longxia · greenbook
```

MOC 保留名 `moc-greenbook` → `concepts/playbook-*`；concept body 强制 quote + wikilinks。

---

## 3｜同步机制：本地 OB → GitHub 私有镜像

实现完全公开：`yuanli-os-company-brain-skill/scripts/wiki_git_mirror_sync.sh`

```
git add -A → commit → git fetch origin $BRANCH → git rebase（禁止 force）→ git push
```

| 项 | 内容 |
|---|---|
| 调度 | **launchd 每日 2 次**（`com.example.wiki-mirror-sync.plist.template`） |
| 方向 | **单向** OB → GitHub |
| 冲突处理 | rebase 失败 → **自动 abort，exit 1，需人工介入**（不自动合并） |
| 四重门 | 私有仓断言 / leak-guard / never-force / 单实例锁 |
| 环境变量 | `WIKI_DIR` `REPO_SLUG` `LEAK_GUARD` `BRANCH` `GH_HTTPS_PUSH` |

**一条容易混淆的界定**（`wiki-github-mirror-sync.md`）：

> 镜像是 **backup**，不是三圈 **promotion**；二者不得混淆。

单向纪律（`multiplatform-projection-protocol.md`）：

> 真相层 = 本地 vault … 投影层 = git 远端 / RAG … **绝不反向手改**
> 回写 = 任何入口新知识 → **人审蒸馏** → 进真相层 → 再投影

**没有用 Obsidian Git 插件，也没有 CI Action**——是 vault 内 git + bash + launchd。

其他通道：

| 通道 | 状态 |
|---|---|
| 飞书 mature 概念 → LLM-Wiki | **明确未实现，等 v1**；v1 前人工在 Obsidian 另写 concept |
| `gbrain sync` | vault → GBrain DB，属 Serving 层投影，与 git mirror **不同层** |
| GitHub Actions 同步 | 90 个公开仓零匹配 |

---

## 4｜调用链：三条路径，一次代际更替

### 路径 A｜历史 skill 栈（KB-first，实现在本机）

`os-yuanli-share-max/README.md`：

> On any non-trivial task, invoke `/knowledge-liming "<topic>"` first to fetch relevant Wiki context before acting.

| Skill | 角色 | 公开仓状态 |
|---|---|---|
| `knowledge-liming` | 跨项目只读检索 | 仅引用，`local:~/.claude/skills/` |
| `llm-wiki-operator` | Wiki 内 CRUD | 同上 |
| `knowledge-orchestrator` | 多源编排 | 同上 |

`yuanli-research-max` 的 P1 阶段强制先跑 `knowledge-liming`。这是 2026-07 归档批次之前的主路径。

### 路径 B｜GBrain MCP（quickstart 当前主推）

`yuanli-os-quickstart/05-怎么喂养它.md`：`gbrain capture` / `gbrain query`，MCP 端点 `127.0.0.1:3131`。

`gbrain-yuanli` 是**公开完整实现**：PGLite + embedding + hybrid search + `graph-query` + `gbrain serve`。它把 markdown vault 当 source repo 同步进 `~/.gbrain`，检索走投影层，**不是 T2 法权写入点**。

### 路径 C｜Company Brain skill（vault 原生全套）

`yuanli-os-company-brain-skill`，首次现场测试 2026-05-01/02 就在 LLM-Wiki vault 上：

| 组件 | 作用 |
|---|---|
| `brain_surface.py` / `brain_surface_hook.py` | 右时召回（UserPromptSubmit hook） |
| `relationship_graph.py` | typed edges 图遍历 |
| `embed_sources.py` | sources 向量化 |
| `refresh_hot_static.py` | 重建 `_hot.md` |
| **`wiki_lint_l10.py`** | **relationships frontmatter lint** |

### 路径 D｜飞书专家大脑

agent `cd` 到 vault 直接读写 `concepts/<slug>.md`——LLM-Wiki 是 concept 正文的唯一源。

### `yuanli.memory.search` 的实现状态

**公开仓无 server 实现。** MCP 六接口目前只到 `YOS-MCP1-G0` 契约冻结，下一 Gate 是 G1 synthetic server。`yuanli-os-NGP`（本仓）是 MCP 平台候选，**不是** `memory.search` 的实现仓。

---

## 5｜它在 CBM 47 格棋盘上的位置

`RAY｜原力人生 CBM 战略地图 v1.0`（2026-09-09，47 Components）：

| 格位 | 域 | 责任层 | 含义 |
|---|---|---|---|
| **K-C01** | K｜知识学习（Compounding Engine） | Control | Research Portfolio & **Knowledge Canon｜知识正典** |
| **O-E01** | O｜人生治理 / Personal OS | Execute | **Context & Retrieval Operations｜上下文与检索运营** |

相关格位：`O-C01｜One Brain Governance`、`K-C03｜Idea-to-Asset & Reuse Pipeline`。

**战略裁决**：

- 硬原则 **D3｜CAP / K 默认 Support。只有 Hard Trigger / Human DEC 才升级。**
- Core H5：`H-C02 / H-C03 / V-D04 / V-C04 / O-C05`——**没有 K 域，也没有 O-E01**
- 三个 Active Battle 的 seed：`B1 = H-C02+H-C03`、`B2 = V-D04+V-C04`、`B3 = O-C05+O-E02`——**同样没有**

---

## 6｜独立战略洞察

### 洞察 1｜T2/T3/T5 共享一个物理单点，而绕过它的方案没有公开实现

| Estate | 法权 | 物理位置 | 可达性 |
|---|---|---|---|
| T1 GitHub Soul | 最高（规范） | 云端 | ✅ 永远可达 |
| **T2 OB LLM-Wiki** | **首选权威（语义）** | **MacBook-Pro-M4.local** | ⛔ 机器离线即失效 |

`YOS-BRAIN` E0：

> **MacBook-Pro-M4.local 当前离线。** 因此 OB、NAS、Remote Gateway，以及依赖本地 `lark-cli` 的飞书直读全部 fail-closed。

`GAP-E0-001` 表面影响四个 Estate，但它们共享同一台笔记本。一台机器关机，五类真源里 **T2、T3、T5 三类同时失效**，只剩 T1（规范条文）和 T4（Runtime 读数）。也就是说离线状态下，大脑**完全没有"我们知道什么"**。

**新证据强化了这条判断**：`Remote Read Gateway` 在 90 个公开仓里**零匹配**。而名字最像的 `moonstachain-yuanli-reader-gateway` 其实是 **USB 设备控制网关（YOS-READER0）**，和 wiki 远程读取完全无关——**不要把这两个混为一谈**。

所以「绕过物理单点」目前**没有任何公开实现证据**，只在 Notion 侧被登记为 `⛔ ACCESS BLOCKED` 的 P2 Estate。这是一个还没有解法的架构风险，不是一个待部署的方案。

### 洞察 2｜真正的风险不是崩溃，是静默萎缩

E2 第一个 Context Packet 只带 2 个 Estate，**明确排除 7 个**，含 GitHub LLM-Wiki：

> **这不是"拿不到"，而是"这个任务不需要"。**

裁决正确。但叠加 T2 长期不可达，会产生一个没有防线的失败模式：

```
OB 不可达 → 语义查询走不了首选权威路径 → Context Compiler 按最小充分合法地不带它
→ 任务照样完成 → 没有 gate 报错 → 下一次继续不带
```

结果是 LLM-Wiki 从"首选权威"**事实上退化为"从不被调用的资产"**——不崩溃、不告警、不出现在任何 FAIL 裁决里。

体系已经写下坑 #9「**把知识库当复利**」（保存、搜索、AI memory 都不等于 Learning 被复用）。但存在一个对称的、尚未命名的坑：**把知识库当资产却从不调用它。** 前者高估存储，后者让权威静默失效，两者都不报错。

**而这里有个反讽**：GitHub 侧的投影其实**相当健康**——launchd 每日 2 次同步意味着滞后最多约 12 小时，rebase 冲突还会 fail-closed 停下等人。这是一条维护良好的通路。问题不在管道，在**没有任何机制检查这条通路是否真的被用于决策**。

**建议**：加**调用率哨兵**（sensor），指标不是"OB 在不在线"，而是"过去 N 次涉及语义判断的任务中，有几次实际带上了 T2"。归零就触发 gate。

### 洞察 3｜它不是 Battle，也不是普通 Support，而是 B2/B3 的 critical path

你说这是"很关键的一个仓库"，而你在 CBM 地图里签下的是：K 域默认 Support、`O-E01` 属 Execute、两者都不在 Core H5 也不是任何 Battle 的 seed。

这不矛盾，是两句话在说不同的事：

- 你说的"关键" = **语义供给的重要性**（知识从哪来、凭什么可信）
- CBM 说的 Support = **不该获得一级转型注意力**（这季度不投稀缺资源改造它）

不把这个区分讲清楚，会掉进两个方向的错误：

| 错误方向 | 后果 |
|---|---|
| 当 Battle 去建设（加笔记、建图谱、做可视化） | 踩坑 #9「把知识库当复利」、坑 #10「让 CBM 成为第 48 个项目」，Sparse Heat 失效 |
| 因为是 Support 就完全不管 | **B2 / B3 失去实现前提** |

第二个方向被低估了。看两个 Battle 自己的条件：

- **B2｜Detach RAY × N>1 Delivery**：「**AI / 团队读取 Canon 与 Reality，而不是依赖聊天记忆**」
- **B3｜Outcome → Learning → Reuse**：「Learning 必须在后续项目开始前**自动预加载**」；M5 Gate 要求后续独立真实情境证明 Learning 被预加载并改变 judgment / action / allocation

**Preload 需要一个可检索、可信、可判资格的语义库**，这正是 T2 的功能。所以：

> **正确定位不是 Battle，也不是普通 Support，而是 Support Domain 里 B2/B3 的 critical path。**

这个定位直接给出投入的**上下界**：

- **下界**：让 B2/B3 的 Preload 能真实发生（可达 + freshness 可证 + 能被 Context Compiler 合法调用）
- **上界**：不做内容扩张，不做图谱美化，不做第 48 个项目

不服务"让 Preload 发生"的投入，按硬原则 D4 就该被拦下。

### 洞察 4｜瓶颈不是"没有 schema"，是 1078 条存量没填 + schema 缺 3 个法权字段

**这条修正了我上一轮的判断。** 我原先说"Obsidian markdown 天然不带这些字段，需要从零建 schema"——不准确。schema 已经存在，工具链也已经存在。真实缺口比那个更具体、也更容易动手。

`yuanli.memory.search` 的准入契约（`原力OS-MCP`）：

> 原力 Memory 还要回答：来源是什么？什么时候发生？**新鲜度如何**？属于哪个 **Principal / Estate**？**敏感级别**是什么？**这条记忆有没有资格参与当前判断**？
> **搜得到 ≠ 有资格使用。**

把现有 schema 逐字段对照这份清单：

| memory.search 要求 | 现有 frontmatter | 状态 |
|---|---|---|
| source | `sources` | ✅ 有 |
| observed_at | `created` | ✅ 有 |
| freshness | `updated` | ⚠️ 有，但是 mtime 不是 review |
| **principal / estate** | — | ❌ **缺**（`audience` 不等于 estate 法权） |
| **sensitivity** | — | ❌ **缺** |
| **context_eligibility** | — | ❌ **缺** |

**7 个字段是内容型 schema，缺的 3 个恰好全是法权型字段。** 这不是疏忽，而是 schema 设计目标不同——它为知识组织服务，不为法权判定服务。要接 MCP 就必须补这一层。

**更硬的一击**：即使 schema 完整，存量数据也没填。

> **Phase 2 不强制 frontmatter 全填**：1078 wiki concepts 仍按目录推断

「按目录推断」在知识组织场景下是合理的省事做法，但在 fail-closed 的法权判定下**等于无法自证**——`memory.search` 不能因为一个文件在 `concepts/` 目录里就认定它有资格参与某次判断。

**所以真实结论要比我上轮说的更精确**：T2 的瓶颈不是"缺 schema"，而是

```
schema 缺 3 个法权字段  +  1078 条存量按目录推断而非填写
```

**这两个缺口都有现成的工具可以接**——`wiki_lint_l10.py` 已经在做 relationships frontmatter lint，扩展它覆盖 3 个法权字段是增量工作，不是从零造轮子。

同时要注意：**这个缺口和可达性是相互独立的。** 即使 MacBook 明天开机，1078 条按目录推断的 concepts 依然无法被 `memory.search` 合法交付。修网络不等于修这个 Estate——现在 `GAP-E0-001` 只记了可达性，这一层缺口在 gap 清单里没有对应条目。

**另一个被这条串起来的问题**：Layer 2 `concepts/` 是 AI 可写的，Layer 3 `insights/` 是人类专属。这条铁边界在**目录层面**很清晰，但如果 concepts 不带 frontmatter，AI 生成内容和人类蒸馏内容在**单条记忆层面**就无法区分。补字段时应该一起加上 `authored_by`，否则 Layer 3 的铁边界只在目录粒度成立，进不了 Context Packet 的资格判定。

**建议的最小动作**（严格落在洞察 3 的上下界内）：

1. schema 扩 3 个法权字段 + `authored_by`
2. 扩展 `wiki_lint_l10.py` 覆盖新字段，把它变成准入门
3. 用 GitHub 侧 git 历史生成 **stale candidate 排序**，给 1078 条回填排优先级——先回填最近动过的高频概念，不追求一次全量

第 3 条有一个必须守住的边界：git commit time 证明的是「**文件最后被改动**」，不是「**知识最后被人核过**」。它**不能**替代 review，但可以精确回答互补问题——哪些知识很久没被碰过。做 review 排序的输入，不冒充 review 结论，就不越权。

对照 Notion 侧的处境（`YNP-KG0` R0 = `FRESHNESS_FAIL`，12/12 Object 与 14/14 Edge 的 `Last Reviewed` **全部为空**），会看到一个明显错配：**GitHub LLM-Wiki 拿得到机器可证的 freshness 却被定为"仅历史 fallback"闲置着；Notion 有完整语义治理结构却拿不到 freshness。**

### 洞察 5｜不是"缺治理"，是三套 typed-edge 语义并存且互不兼容

**这条也修正了我上一轮的判断，而且情况比我说的更严重。** 我原先说"治理能力在 Notion，法权在 Obsidian，一边有一边没有"——错了。**Obsidian 侧早就有自己的 typed-edge schema**，问题是它和另外两套不兼容。

三套边语义同时存在：

| 来源 | 关系类型 | 数量 |
|---|---|---|
| **Notion** Knowledge Edge Registry | `part_of` `depends_on` `explains` `supports` `contrasts_with` `applies_to` `example_of` `leads_to` | 8 类 |
| **Wiki** Company Brain G2 | `commits-to` `owns` `blocks` `derives-from` `supersedes` `supports` | 6 类 |
| **GBrain** runtime graph | `attended` `works_at` `invested_in` `founded` `advises` `wikilink` `wikilink_basename` … | 7+ 类 |

**三套里只有 `supports` 一个重叠。**

而且 Wiki 侧的边有**两个来源**：显式 frontmatter `relationships:`，以及 `relationship_graph.py` 从 `decisions/` 四元组自动 derive——所以实际上是第四种语义入口。

体系已经正确地区分了其中两套：Wiki G2 是治理 schema，GBrain runtime graph 是检索投影，且明确 GBrain 不得反向覆盖知识正典。但 **Notion Knowledge Edge Registry 的 8 类关系与 Wiki G2 的 6 类之间没有任何 crosswalk**（公开仓也没有 `Edge Registry` 独立 schema 文件）。

这解释了 `YNP-KG0` Non-goals 里那句话的真正含义：

> 不为了"**像 Obsidian**"制造高密度无意义连线。

它不是在说 Obsidian 没有 typed edge，而是在说**不要引入 wikilink 那种无类型连接**。这个判断是对的。但反过来的一面还没写下来：

**两套 typed-edge 体系都极度稀疏。** Notion 是 12 节点 / 14 边，8 类语法只实际用了 3 类（`part_of` 9、`supports` 3、`explains` 2）。Wiki 侧的闭环标准是「typed edges 总数 **≥ 20**（explicit + derived）」——对照 1078 条 concepts，这个门槛意味着约 **2%** 的连接覆盖率。

所以真正的结构性问题不是哪边做得不好，而是：

> **同一套知识资产上跑着三套互不翻译的边语义，每一套都稀疏到无法支撑多跳推理，而它们之间没有 crosswalk。**

可行方向不是迁移内容（那会造第二真源，违反 `YNP-KG0` Non-goal 第 1 条与 no-second-SSOT 原则），而是**先做一份 8×6 的边语义 crosswalk，确定哪些可映射、哪些必须保持分离**。在此之前给任何一套加边，都是在加深分叉。

### 洞察 6｜E3 之前建议先设一道禁令

下一个 Gate：

> `YOS-BRAIN-E3｜Artifact Trace Ledger × Context/Skill Gap Extraction`
> 追踪任务拿到 Context Packet 后生成了什么 Artifact、消耗了哪些 Context、暴露了哪些 **Context Gap / Skill Gap**、哪些 Gap **有资格进入 governed skillification**。

把 E3 机制和 T2 长期不可达叠加，会得到一条需要提前堵住的漏洞：

```
OB 不可达 → 任务缺语义知识 → E3 如实记录为 Context Gap
→ Gap 进入 governed skillification → 语义知识被硬编码进 skill
```

**问题**：写进 skill 的知识**不受 T2 的 freshness 与 review 治理**。这等于把语义真源内容复制进一个法权更低、且没有 review SLA 的载体——而且这次漂移是**被治理流程正当化的**，会带着 receipt 和 PASS 记录，比无治理的漂移更难发现和回滚。

这也正是「GBrain / Retrieval Projection 可重建，**不是知识正典**」的反面案例：skill 同理，不该成为语义知识的存放地。

**建议在 E3 gate 加一条 fail-closed 规则**：

> Context Gap 若可归因于 **T2 不可达**，一律**不得进入 skillification**，只能进入 `access-recovery` 队列。
> 只有当 T2 可达且知识确实不存在时，该 Gap 才有资格被视为真实知识缺口。

价值在于它把两种长得一样的 gap 分开了：**"我拿不到"和"它不存在"在 trace 里表现完全相同，处置方式却相反。** 前者要修通路，后者才该沉淀能力。不区分的话，E3 越勤奋，真源漂移越快。

---

## 7｜仍然读不到的部分（fail-closed 声明）

公开仓检索解答了结构、同步、调用链的大部分问题。以下仍**拒绝推测填充**：

| 缺口 | 影响 |
|---|---|
| `LLM-Wiki` 仓本体 | 无法验证**真实** `_schema.md`（sample 版可能与生产版不同）、笔记总数当前值、git 历史、`.obsidian` 配置 |
| `knowledge-liming` / `llm-wiki-operator` / `knowledge-orchestrator` 实现 | 仅 `local:~/.claude/skills/` 引用；继任仓 `yuanli-os-starter` 亦 404 |
| `yuanli.memory.search` 等 MCP 六接口 server 实现 | 只到 G0 契约冻结，无实现可验证 |
| `brain-estate-registry.v1.0.yaml` / Context Compiler 合同正文 | 在私有 Soul `governance/information/` |
| 1078 条 concepts 全量清单 | 只有规模数字（第 8 节从引用反推出约 50 条，非全量） |
| 生产 embedding 模型与索引位置 | `embed_sources.py` 公开，生产配置未公开 |
| Notion 8 类 × Wiki G2 6 类的 crosswalk | 两侧公开材料均无此文件——洞察 5 的建议正是要补它 |

**解除方式**：在 Cursor Dashboard（Cloud Agents → Secrets）配置对 `LLM-Wiki` 有读权限的 GitHub token。届时可把洞察 4、5 从「基于契约与引用的推断」升级为「基于仓库事实的裁决」，重点验证两件事：**生产 `_schema.md` 的真实字段**，以及 **1078 条 concepts 的 frontmatter 实际填充率**。

---

## 8｜从公开引用反推的概念条目（约 50 条，非全量）

用于判断 T2 的语义覆盖范围。**字面模式 `wiki 概念 <name>` 在 90 个公开仓里只命中 1 个**：`industrial-ip-equity-architecture`（`ip-company-strategy-cockpit` 第 6 步治理隔离引用）。其余通过 `LLM-Wiki/concepts/` 等路径引用反推。

**ASCII slug（`concepts/`）**

```
24h-rescore-protocol · ai-native-organization · asymmetric-advantage
bowling-pin-strategy · business-moat-framework · crossing-chasm-fundraising
dual-axis-rubric · five-dimension-asymmetric-advantage-test · force-os
four-force-assets · four-venture-cycles · genius-zone · golden-shadow
individuation · industrial-ip-equity-architecture · information-aesthetic-intuition
k-type-wealth-divergence · kong-zi-ren-sheng-jie-duan-xin-jie
longxia-handshake-dispatch · longxia-three-standards · meta-constitution
mvp-closure · n1-light-bootstrap-rebound · osa-loop · portable-company-brain
recursive-evolution · right-time-surface · shadow-integration
three-circles-protocol · twelve-archetype-system · typed-relationships-schema
walking-pizza-management · yuan-li-zi-chan · yuanli-os-company-brain-overview
```

**中文文件名（`concepts/`）**

```
借势合力 · 原力创业 · 原力觉醒 · 品类独创 · 模式升级 · 壁垒锁定
原力战略 · 原力财富 · 心理账户 · moc-yuanli-chuangye
```

> ⚠️ 一处已知的用词漂移：`concepts/模式升级.md` 是 legacy 名，`yuanli-strategy-trilogy` 注明**对外应称「模式升维」**，wiki 旧页待对齐。这正是洞察 4 里 frontmatter 缺失导致的典型后果——没有字段能标记"此页用词已被上位裁决取代"。

**`syntheses/`（L4/L5 级综合，价值最高的一批）**

```
递归进化与AI共生 · 原力OS治理演进史 · 原力龙虾产品架构全景图
天赋资产×品类独创转化引擎 · 从单位经济到复利飞轮 · 原型人格到品牌叙事
康波周期与创业择时 · 甜用户识别与品类独创的闭环
原力创业-借势合力方法论提炼 · 原力创业学员案例-三母题实证地图
原力战略私教辅导模式复盘 · 原力财富-财富三变全景综述
两千年管理史的终结-AI时代组织进化的原力解读
```

**`insights/`（人类专属，AI 永不写）**

```
原力觉醒：AI时代的主体性觉醒与共生进化 · 原力战略-概念体系总纲.md
```

**其他路径**

```
llm-wiki/qin-xiao-ming/ · sources/wechat-mp/<公众号>/ · sources/feishu/
_factory/yuanli-startup-greenbook-v0.2/ · _factory/{lessons,evolutions,skills,patterns}/
domains/01-charity/ … 14-family-office/ · public/{orange-book,green-book}/
```
