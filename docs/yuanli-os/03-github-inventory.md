# GitHub 仓库盘点｜`moonstachain` 原力体系全景

> 盘点时间：2026-09-15 · 数据源：GitHub REST API（`users/moonstachain/repos`）+ 各仓 README + Notion 投影交叉验证
> **可见性说明**：本次盘点使用的令牌仅对 `yuanli-os-NGP` 有 installation 权限，能读全部**公开**仓库，
> 但**所有私有仓库不可达（HTTP 404）**。法权层几乎全在私有仓，因此本文件对法权层只能做**外部引用重建**。

---

## 0｜规模与总体判断

| 指标 | 数值 |
|---|---|
| 公开仓库总数 | **88** |
| 其中 GitHub 原生已归档 | **19**（全部集中在 2026-07-27） |
| 自建（非 fork） | 55 |
| fork | 33 |
| 原力体系直接相关 | ~41 |
| 私有仓库 | 不可枚举（至少 5 个被外部引用确认存在） |

**三个最重要的结构性判断：**

1. **法权与投影已经彻底分离。** 公开仓库里**没有一个是 Canon Authority**。所有正典法权集中在私有 `yuanli-strategy-soul`。公开仓的自我定位普遍写成 `PROJECTION / CONTENT ENGINEERING`。
2. **2026-07-27 发生过一次大规模仓库治理归档行动**，一天归档 19 个仓库，归档理由统一为"一次性任务完成／超 14 天未动"，并逐仓指定继任仓。这不是荒废，是**主动的法权收敛**。
3. **重心已从"公开 Agent Skill 生态"转向"私有 Canon + 领域 Runtime"。** 2026-08 之后的活跃提交几乎只落在 `yuanli-strategy-soul`（PR 已到 #788）、`yuanli-invest`、`yuanli-strategy-trilogy` 这几处。

---

## 1｜第 0 层｜Canon Authority（全部私有，不可达）

| 仓库 | 角色 | 证据来源 |
|---|---|---|
| `yuanli-strategy-soul` | **T1 Normative Truth / CANON_AUTHORITY**。`CONSTITUTION v1.2｜2026-08-07`。承载 governance contracts、receipts、Estate Registry、三部曲世界观契约、《地心新说》书稿 | Notion `原力OS` 页 Canon URI；`yuanli-strategy-trilogy` README；YOS-BRAIN Atlas 的 Machine Truth Pointers |
| `yuanli-os-starter` | `os-yuanli-share-max` 的**指定继任仓** | `os-yuanli-share-max` README 归档块 |
| `LLM-Wiki` | T2 Semantic Truth 的 committed history projection（本地 OB 为 live master） | YOS-BRAIN Atlas |
| `quant-workspace` | **当前 A9 operational canon** / Reference Quant Runtime | `yuanli-invest` README |
| `yuanli-invest-rsi` | Capability Challenger Lane，状态 **FROZEN** | `yuanli-invest` README |

**活跃度旁证**：Notion 引用中出现 `yuanli-strategy-soul` 的 PR #683 / #686 / #691 / #692 / #693 / #696 / #786 / #788 与 issue #787，时间集中在 2026-09-09 至 09-14。→ 该仓是整个体系真正的**高频施工现场**。

从外部引用重建出的目录骨架：

```
CONSTITUTION.md
docs/worldview/YUANLI-TRILOGY-GREEN-PAPER-v0.1.md
docs/YUANLI-LIFE-STRATEGY-BOUNDARY-v1.md
docs/governance/YOS-BRAIN-E{0,1,2}-REPORT.md
docs/books/geocentric-intelligence/{gcn1n,gcn2,gcn-d0}/...
governance/information/brain-estate-registry.v1.0.yaml
governance/information/brain-{routing,freshness,estate-health}-*.yaml
governance/information/brain-{e2-task,context-compiler}-contract.v0.1.yaml
governance/receipts/yos-brain-e{0,1,2}-*.yaml
assets/C3-一张地图/life-master...
project/ray-a2c1/cand01/...
```

---

## 2｜第 1 层｜领域 Canon（公开，活跃）

| 仓库 | 最近 push | 定位 |
|---|---|---|
| `yuanli-invest` | **2026-09-15** | 原力投研 Canon。North Star：把投资知识编译成 reality-tested、machine-callable 的研究智能。长期复利资产 = `ResearchCapability` |
| `yuanli-strategy-trilogy` | 2026-09-07 | 三部曲**内容工程与 Projection 工作仓**。明确写 `不是 Canon Authority`。承载 TW0/TW1 三世界世界观契约的前台编译 |
| `yuanli-trilogy-max` | 2026-09-07 | 叙事知识库 max — 四拍九段全量正典（资产/创业/OS） |
| `yuanli-health-skills` | 2026-08-31 | 原力健康 skill 集（对应 Supabase `yuanli-health` T4 Runtime） |
| `yuanli-awakening` | 2026-07-05 | 原力觉醒·人生课题正典：公理/框架/四大资产 × 八大人生课题，30 篇原子化互链文档 |

### `yuanli-invest` 的 OS vNext（值得单独记住）

它是 C1–C4 之外**另一套领域内核**，结构上与 C1–C4 同构但语汇独立：

```
一核：Right-Tail Compounding（抓右尾、让赢家复利、永不出局）
三界：P Reality / N Belief / X Asymmetry，其中 X := (Xs, Xa, Xp) 仅表结构分解
三门：E Evidence / V Price / S Survival
一环：Theory → Hypothesis → Capability → Runtime → Replay → Benchmark
      → Failure → Future Settlement → Capability Revision
```

Canonical Research State = `ResearchStateVector`：`P → Xs → N → V → Xa → Xp → S`，E 横贯所有节点。

法权分工：`yuanli-invest` = Canon；Wind AI = Market Reality Runtime；Codex = Research Engineering Runtime；`quant-workspace` = Reference Quant Runtime；Evidence Vault = Audit / Replay Evidence Layer。

关键纪律：**`Receipt = Ledger; Status = Projection`**，`CANON-STATUS.json` 是确定性投影而非事实源；**GitHub 不是 Data Warehouse**；**Research `canon` 不代表可交易**。

---

## 3｜第 2 层｜三部曲十二模块（正典命名，不得改）

```
源头世界｜《原力资产》Source        现实世界｜《原力创业》Venture     未来世界｜《原力OS》Evolution
A1 发现母体                        B1 原力借势                      C1 一纸文脉
A2 回到母体                        B2 品类独创                      C2 一个大脑
A3 获得原力                        B3 模式升维                      C3 一张地图
A4 显化原力                        B4 壁垒锁定                      C4 一条链路
──────────────                    ──────────────                  ──────────────
第一性问题：                        第一性问题：                      第一性问题：
什么持续生成我的不同？               世界为什么选择、付费             今天发生的价值，怎样被
                                   并放大这种不同？                 未来继承并继续做功？
前台动作：回到源头                   前台动作：进入现实               前台动作：创造未来
```

四层等价表述：

```
Canon        原力资产 × 原力创业 × 原力OS
Architecture Source   × Venture  × Evolution
Worldview    源头世界 × 现实世界 × 未来世界
Mechanism    生成     × 选择     × 继承/进化
```

前台世界观句：**回到源头，进入现实，创造未来。**

递归律：`源头世界_n → 现实世界_n → 未来世界_n → Learning/Reuse → 源头世界_n+1`

三条反混淆边界（写在 `yuanli-strategy-trilogy` README 里）：
- `源头世界 ≠ 原力资产改名`（母体是生成源，资产是资产化后可调用的结果）
- `现实世界 ≠ 赚钱世界`（Revenue 只是 Reality Outcome 的一类）
- `未来世界 ≠ AI 未来 / 未来科技 / 趋势预测`（AI 只作 Amplifier）

**Legacy Explanation Settlement**（TW1 裁决，旧解释保留但降权，不得再定义本体关系）：

| 历史表达 | 当前身份 |
|---|---|
| 向内 / 向外 / 向上 | `HISTORICAL_AXIS_DESCRIPTOR` |
| 人 / 事 / 法 | `HISTORICAL_TEACHING_DESCRIPTOR` |
| 主根 / 左腿 / 右腿 | `HISTORICAL_NARRATIVE_DEVICE` |
| U 型理论 / 跨越鸿沟 / 莫比乌斯 | `EXTERNAL_EXPLANATORY_LENS` |
| 「你」× AI | `LEGACY_AMPLIFICATION_METAPHOR` |
| 秘密 × 一万倍 | `NARRATIVE_DEVICE` |

---

## 4｜第 3 层｜Runtime / Platform

| 仓库 | 类型 | 说明 |
|---|---|---|
| `yuanli-os-NGP` | fork of `archestra-ai/archestra` | **本仓库**。Enterprise AI Platform：guardrails / MCP registry / gateway / orchestrator。是原力OS-MCP 走向生产的候选基础设施 |
| `gbrain-yuanli` | 自建 | gbrain 钉版镜像（v0.42.53 + yuanli 3 本地补丁）— 升级窗重放基线。对应 `GBrain / Retrieval Projection` 层 |
| `yuanli-invest-vnpy` | fork | Python 量化交易框架，投研 Runtime 侧 |
| `yuanli-os-agent-team` | fork (claude-flow) | 多 agent 编排平台 |
| `yuanli-interface-skills` | fork，**已归档** | 人机共创基建 |

> 注意 `yuanli-os-NGP` 与原力OS 的关系：它是 **Runtime 候选**，不是 C1–C4 的实现。
> 按 YOS-MCP1-G0 的边界，生产 MCP 尚未上线；WRITE / ACT 未授权。

---

## 5｜第 4 层｜Agent Skill 生态（方法论沉淀）

### 5.1 原力OS 方法内核

| 仓库 | 状态 | 说明 |
|---|---|---|
| `os-yuanli-share-max` | **ARCHIVED 2026-07-27** | kernel + 6 profile + 9 卫星 skill。继任 `yuanli-os-starter`。详见 `02-agent-kernel-os-yuanli.md` |
| `os-yuanli-info-5l` | **ARCHIVED 2026-07-27** | 信息 5 层 / 炼丹 skill — 让讨论跃迁到洞察层，把洞察固化成框架 |
| `clone-alpha` | 活跃度低（2026-03） | 原力OS 克隆体 Alpha，多机部署实验。含 clone-state 心跳/评分/晋升策略、5 个 workflow、飞书 bridge |
| `yuan-li-os-clone-01` | **ARCHIVED** | 克隆体实验第一版 |
| `yuanli-os-quickstart` | 2026-07-09 | 面向企业家的 docsify 上手站。四句话定位："记住 / 回答（带出处）/ 发现 / 增值" |
| `yuanli-os-company-brain-skill` | **ARCHIVED** | Company Brain v0.1，Sentra 式记忆系统：right-time surface + 三圈边界 + typed edges + 抗幻觉 |
| `yuanli-os-dashboard` | **ARCHIVED** | 原力OS 信息系统全景仪表盘 |
| `yuanli-os-greenbook` | **ARCHIVED** | 八万四千-OS-管培孵化绿皮书 · 4 部 55 章，碳基(x·y) → 硅基(ʸx) 跃迁路径 |

### 5.2 战略 / 洞察 / 看板类

| 仓库 | 核心方法论 |
|---|---|
| `ip-company-strategy-cockpit` | 七步管线「框采分炼断现养」编排 12 个 skill + 七门质量闸 + 八元素分类法 + 四看穿透镜 |
| `hybrid-expert-brain-strategy` | Pyramid + SCQA + MECE + Action Title + 12 维密度 + Cascading Causal → 单页战略蓝图 HTML |
| `osa-strategy-card-distiller` | 逐字稿 → 一张 OSA 卡 · 七道质量门 + 六段管道（收敛 × 拔高 × 校准） |
| `high-density-mckinsey-report-designer` | 金字塔 + SCQA + MECE + Action Title，12 维 rubric（报告适配版） |
| `high-info-density-dashboard-designer` | 12 维 rubric + 6 模块 + 8 反模式，N=3 verified |
| `cascading-causal-cockpit` | 多层级联因果图谱，点击 archetype 反追完整传导路径 |
| `embedded-strategy-brain` | 把静态 HTML 看板升级成带活问答 AI 的看板（BYOK 纯前端） |
| `recursive-capability-architect` | Producer-Verifier-Improver 递归能力增长系统 |
| `liu-chenming-strategy-framework` | 刘晨明/广发策略方法论蒸馏：资产三分法 × 四维跟踪指标 × 决策规则 |
| `yuanli-strategy-playbook` | **ARCHIVED** · 原力战略绿皮书方法论正典（对内操盘手版），七册「道体法术器守」+ 附录 |
| `yuanli-narrative-strategy-map` | **ARCHIVED** · 学员逐字稿 → 高信息密度单文件 H5 战略地图 |
| `yuanli-research-max` | **ARCHIVED** · 研究操作系统，8 个研究方法论内核 → 6 阶段流水线（设计门→前置检索→联网收集→双轴分析→萃取判层→失真证伪→交付） |
| `cbm-osa-ipo-map-kit` | CBM/OSA/IPO 地图工具包 |

**跨仓库共享构件**（这是这批 skill 真正的复用内核）：
质量门 / rubric 评分 / 管线阶段划分 / `N=1`·`N=3` 证据标注惯例 / 失真与防失真护栏 / 洞察层跃迁判据。
这些构件与 `os-yuanli` 的 `audit-rubric`（6 轴 × 5 检查点）和策略层次阶梯（数据→特征→观点→洞察→全局最优）是同源的。

### 5.3 数据 / 逆向 / 交付类

`db-reverse-engineer`（3 步系统性 DB 逆向，N=1 某寺院 163 表）· `yuanli-strategic-data-workbook`（ARCHIVED，25 sheet 顶层聚合）· `yuanli-dual-layer-data-workbook`（ARCHIVED，顶层聚合 + 底层 fact，cid_hash 可 JOIN）· `yuanli-data-middleware`（ARCHIVED，N=0 experimental）

### 5.4 前置 / 意图层

`qiqiao-linglong`（七窍玲珑 — 意图探求与收敛的前置追问层，最少提问榨干意图，镜像主人隐性方法而非通用套路）

### 5.5 内容 / 渠道 / 飞书类

`wechat-writer` · `wechat-mp-reader` · `wechat-radar-dashboard-skill` · `feishu-expert-brain-architect` · `guanpei-recruit-skill` · `xhs-remote-publisher` · `nas-video-autoclip` · `aliyun-h5-autodeploy` · `zhiku-market-skill`（随身智库 AI 组件市场，1800+ 组件查询）· `yuanli-notebooklm-router`（ARCHIVED，28-notebook 生态自动路由）

### 5.6 前台站点

`yuanli-strategy-web` · `yuanli-website`（ARCHIVED）· `yuanli-startup-map-site`（ARCHIVED）· `os-sm-site` · `os-gd-yufo-vip-guide`（ARCHIVED）· `moonstachain.github.io` · `siyuan-ipad-pwa` · `ai-governance-atlas`

---

## 6｜2026-07-27 归档批次全表（19 个）

统一归档语句：

> ⚠️ **ARCHIVED(2026-07-27 · 仓库治理归档行动)**
> 归档原因：一次性任务完成/超14天未动。继任仓：`<successor>`。
> 本仓只读保留作历史证据；如需恢复请联系仓主 unarchive。

```
os-yuanli-share-max              → yuanli-os-starter
os-yuanli-info-5l
yuanli-os-greenbook
yuanli-os-company-brain-skill
yuanli-os-dashboard
yuan-li-os-clone-01
yuanli-website
yuanli-startup-map-site
yuanli-startup-map-book
yuanli-trilogy-narrative         → (yuanli-trilogy-max 承接)
yuanli-narrative-strategy-map
yuanli-strategy-playbook
yuanli-research-max
yuanli-notebooklm-router
yuanli-data-middleware
yuanli-dual-layer-data-workbook
yuanli-strategic-data-workbook
yuanli-interface-skills (fork)
os-gd-yufo-vip-guide
```

**为什么这件事重要**：它本身就是 C4 的一次实例演示——`OUT`（这些仓库跑完了一次性任务）→ `LRN`（哪些值得留）→ 归档并指定继任仓（Reuse 路径明确）。而且它符合 `evolution-flywheel` 的"合流与去重"要求：**合流本身是一个任务，要走完整协议，不是"整理一下"**。

---

## 7｜盘点结论与建议

### 已经很强的地方

1. **法权纪律罕见地严格。** 每个公开仓都主动声明自己不是 Canon，Notion 每页都标 `Projection, not Truth`。这在个人/小团队知识系统里几乎见不到。
2. **反自欺机制成体系。** 七个不等号、Hard Negatives、fail-closed、Receipt = Ledger、24/24 hard negative replay——不是口号，是有 CI 和 receipt 的。
3. **归档是主动治理而非荒废。** 19 个仓库一天归档并逐个指定继任，说明有真实的仓库生命周期管理。

### 当前的结构性风险

1. **单点法权集中在私有单仓。** `yuanli-strategy-soul` 同时承载宪法、governance contracts、receipts、三部曲世界观、《地心新说》书稿、project 工作区。PR 已到 #788。风险不是丢失（git 有历史），而是**语义拥挤**——一个仓里混了 Canon、Contract、Receipt、Book、Project 五类对象，未来的边界审计成本会持续上升。
2. **两套战略语法并存尚未 crosswalk。** 详见 `02-agent-kernel-os-yuanli.md` 第 8 节：`os-yuanli` 的五级策略阶梯 vs C3 的 CBM 六原语。YPORT4-G0 已明令"不得另造平行战略语法"，但公开 skill 生态里大量仓库仍在用五级阶梯 + 12 维 rubric。
3. **T2 语义真源可达性是当前最大运行瓶颈。** YOS-BRAIN E0/E1 已经把它标成 `⛔ ACCESS BLOCKED`（MacBook-Pro-M4.local 离线 → OB / NAS / Remote Gateway / 飞书直读全部 fail-closed）。这意味着**最高频的语义查询目前无法走首选权威路径**。
4. **公开 Agent Skill 生态与私有 Canon 之间没有自动同步。** 41 个原力相关公开仓中约一半已归档，剩下的方法论内容与 Canon v1.2 之间没有 crosswalk 文件。新 agent 读公开仓会得到**已降权的解释**（例如"向内/向外/向上"这类已被裁决为 `HISTORICAL_AXIS_DESCRIPTOR` 的表达）。

### 三条可执行建议（不含时间估计）

1. **在 Soul 仓建一份 `PUBLIC-REPO-CROSSWALK.md`。** 把 41 个公开原力仓逐个标注 `Keep / Reproject / Demote / Historical`，并标出哪些表述已被 TW1 或 YPORT4-G0 降权。这直接解决风险 4，也是 YPORT4-G1 "Surface Crosswalk" 的自然延伸。
2. **做一次 `os-yuanli` × CBM 战略语法 crosswalk。** 把五级阶梯明确定位为 `Heat → Battle` 的晋级成熟度判据，而不是独立战略输出格式。解决风险 2 的法权漂移。
3. **给 Soul 仓做一次对象类边界审计。** 按 YPORT4-G0 的六类一等对象（Identity/Law、Capability、Knowledge/Evidence、Strategy/Portfolio、Runtime/Reality、Learning/Reuse）检查 `docs/` `governance/` `project/` `assets/` 的现有归属，把 Book OS 这类内容工程物与 Canon/Contract 分离。解决风险 1。
