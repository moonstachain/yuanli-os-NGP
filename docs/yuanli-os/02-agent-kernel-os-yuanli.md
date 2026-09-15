# GitHub 侧的 Agent 方法内核｜`os-yuanli`（治理OS × 工作OS）

> **法权声明**：Agent Context Projection，不是 Canon。
> 本文件描述的是**公开分享版** kernel（`moonstachain/os-yuanli-share-max`，已于 2026-07-27 归档）。
> 归档继任仓：`yuanli-os-starter`（私有，当前令牌不可达）。

---

## 0｜它和 C1–C4 是什么关系（先说清最容易搞混的一点）

这是两套**不同层级**的东西，不是同一个"四模块"：

| | `os-yuanli` kernel | 原力 OS C1–C4 |
|---|---|---|
| 载体 | Claude Code / Codex Agent Skill | 主体的完整时间轴 OS |
| 治理对象 | **一次 Agent 任务**的接管方式 | **一个主体**跨时间的法权、认知、战略、现实 |
| 分层 | Tier 0–3（Kernel/Capability/Adapter/Reference）+ L0–L4 | C1 / C2 / C3 / C4 |
| 法权位置 | 属于 Runtime 侧的方法协议 | Canon 侧，法权在 Soul 仓库 |
| 当前状态 | 公开版已归档 | ACTIVE，Canon v1.2 |

**准确表述**：`os-yuanli` 是 C4 链路上"Agent 如何执行一个 WPK"的方法协议实现，
外加一部分 C1（边界/授权）和 C3（策略判断）的**局部投影**。它不是 C1–C4 的替代品。

---

## 1｜总公式与六判断

```
原力OS = 治理OS × 工作OS
治理OS 负责方向正确 · 工作OS 负责事情做成
```

**六判断**（每次任务显式输出）：

| 判断 | 防的失败模式 |
|---|---|
| 自治判断 | 越权 / 浪费不该由你做的事 |
| 全局最优判断 | 局部勤奋掩盖整体偏航 |
| 能力复用判断 | 重复造轮子 |
| 验真判断 | 假完成（自己说做完了就算完了） |
| 进化判断 | 用完就扔，系统不变强 |
| 当前最大失真 | 在错误假设上推进 |

---

## 2｜3 × 3 治理矩阵

治理OS 三条线 × 工作OS 三层，每层都要过三条线。

| 工作层 | 递归进化 | 全局最优 | 人类友好 |
|---|---|---|---|
| **主题层** | 会不会沉淀长期能力？ | 是不是当前最大战场？ | 让人更聚焦还是更散？ |
| **策略层** | 能不能变成复用框架？ | 解核心矛盾还是修局部？ | 减少返工还是增加审校？ |
| **执行层** | 这条链路越跑越稳吗？ | 推动结果还是制造进度幻觉？ | 真实减轻体力/算力吗？ |

三层 gate 不可跳：

```
主题层 —— 值不值得进入这场仗？（跳过 → 做了不该做的事，时间回不来）
  ↓
策略层 —— 怎么赢这场仗？（跳过 → 执行很忙，但方向错了）
  ↓
执行层 —— 跑一条可验真的链路（不验真 → 自己骗自己"做完了"）
```

**冲突顺序**：`真实/授权边界 > 主题是否值得进入 > 全局最优 > 递归进化 > 人类友好 > 局部速度与漂亮`

---

## 3｜策略层次阶梯

```
数据 → 特征 → 观点 → 洞察 → 全局最优
```

- **数据**：原始事实
- **特征**：抽出了可命名的模式
- **观点**：有倾向，但还没解释为什么
- **洞察**：揭示了别人没看见的结构性机制
- **全局最优**：在系统层面给出取舍与方向

策略 gate 的关键问题："你现在在哪一层？该不该跃迁到上一层？"
**大多数被拒绝的策略停在"观点"** —— 能说一段，但不足以赢。

---

## 4｜八份协议（Tier 1 Capability）

| 协议 | 核心内容 |
|---|---|
| `task-protocol` | 一个任务 = 一个 `.md`；5 段必填（Done Condition / Why / How / Evidence / Evolution）；状态机 `planning → pending → in_progress → completed → closed`（+ `blocked` / `escalated`）。**没 Evidence 不能 completed，没 Evolution 不能 closed** |
| `layer-dependencies` | 五层 `L0 Evolution Engine → L1 Strategy Methodology → L2 Atomic Capabilities → L3 Composable Flows → L4 Scenario Deliverables`；只能向下依赖；每层独立可替换 |
| `brain-tiers` | 三 tier：`A Strategy Brain`（Opus 级，判断/创造）/ `B Execute Brain`（Sonnet 级，默认主力）/ `C Knowledge Brain`（Haiku/脚本，查分整）。**能用脚本的不引入 LLM** |
| `router-five-axes` | 五轴排序：`任务适配度 > 验真能力 > 成本 > 能力复用 > 附加复杂度`。前两维是硬门槛 |
| `truth-hierarchy` | 五层真源：`本地 artifacts/仓库文件 > 用户当场指令 > 项目级配置 > skill 内置知识 > LLM 权重`。memory 可建立假设，不能替代事实确认 |
| `guides-and-sensors` | 双控回路：Guides 前馈 + Sensors 反馈 + Evolution 沉淀回规则。最小合规三件套：1 份全局 guide + 1 个 Evidence sensor + 1 条 Evolution 规则 |
| `backflow-channels` | 三通道：`Local Sync`（秒级）/ `Async Remote`（commit 可追溯）/ `External System`（必须声明哪边是真源）。防三种失败：静默成功、双源漂移、孤儿 artifacts |
| `evolution-flywheel` | 三条升级通道：新 Skill（≥3 次成功复用）/ 新 Guide（反复发生的失败）/ 新 Template。**硬门槛：能不能立刻被下次任务消费** |

---

## 5｜审计评分模型（6 轴 × 10 分）

`主题层 / 策略层 / 执行层 / 递归进化 / 全局最优 / 人类友好`，每轴 5 个检查点，每点 `2 分已形成 / 1 分部分 / 0 分缺口`，六轴取平均保留一位小数。

等级带：`9.0+ A` · `8.0–8.9 B+` · `7.0–7.9 B` · `6.0–6.9 C+` · `5.0–5.9 C` · `<5.0 D`

报告规则：每轴必须说明**怎么得来的 / 扣在哪儿 / 证据是什么 / 下一步怎么改**。禁止裸分。

---

## 6｜四层基建（2026-04-24 Harness Patterns 对标落地）

| 优先级 | 升级 | 内容 |
|---|---|---|
| P0 | 确定性治理钩子 | 3 个 lifecycle hooks（`SessionStart` / `PostToolUse:Agent` / `Stop`），把治理检查从 prompt 层下沉到系统层 |
| P1 | 上下文压缩协议 | 4 层信息衰减：锚点层（永不压缩）→ 决策层（保留结论+关键证据）→ 过程层（压一句话）→ 噪声层（删除） |
| P2 | 权限分级 | 4 级子 agent 权限：`read-only` / `plan-only` / `full` / `guarded` |
| P3 | 模式语言规范 | 每个 skill 用 `pattern_card`（problem / forces / solution / tradeoffs）描述 |

上下文压缩的**锚点层**（永不压缩）= 六判断结果、任务族+mode 判断、主题层结论、策略层核心矛盾与路线、当前最大失真、验真目标。触发条件：对话 ≥15 轮 / 上下文占用 >60% / 任务阶段切换 / 发现自己在重复提问。

---

## 7｜六档 profile 与能力还原率

作者本机基线（截至 2026-04-24）：169 个 skill / ~15 个 MCP / Wiki 593 concepts + 5700 sources + 14 domains（193MB）/ 3 个 hook。

| profile | 还原率 | 覆盖面 | 关键依赖 |
|---|---|---|---|
| `lite` | ~10% | kernel + 9 卫星 skill | 无 |
| `engineer` | ~55% | gstack 全链 + TDD + 架构图 | `gh` CLI |
| `content` | ~45% | 切角五件套 + 内容引擎 + 文风门 | 无 |
| `yuanli-full` | ~80% | 原力五域 + Wiki + 炼丹 + AI 管家 | `$WIKI_ROOT` |
| `governance` | ~35% | skill-creator/audit/bandit/trainer | 无 |
| `lark-ops` | ~60%（飞书维度） | 飞书 20 skill + 5 bridge | 飞书 app 凭证 |

9 个卫星 skill：`skill-router` / `evidence-gate` / `intent-grounding` / `closure-evolution` / `jiyao-youyao-haiyao-zaiyao` / `content-quality-gate` / `evolution-log` / `routing-playbook` / `strategy-governor`

显式不迁移：个人 memory、Wiki 全量内容、私有 bridge token、MCP OAuth token、settings 里的 env 私密变量、作者个人 `CLAUDE.md`。

---

## 8｜两套内核的 Crosswalk（重要）

| `os-yuanli` 构件 | 对应 C1–C4 | 说明 |
|---|---|---|
| 六判断 · 自治判断 | **C1** | 授权边界 |
| 六判断 · 当前最大失真 | **C1 + C2** | 失真是治理校准器 |
| 主题层 gate | **C1** | 值不值得进入 = Boundary + Intent |
| 策略层 gate | **C3** | 怎么赢 = Policy State |
| 执行层 route + 验真 | **C4** | WPK → ACT → OUT |
| `truth-hierarchy` 五层 | **C2**（Runtime 侧） | 与 T1–T5 Estate 真源正交 |
| `evolution-flywheel` | **C4 的 LRN → Reuse** | 但门槛更松，见下 |
| `audit-rubric` 6 轴 | 跨 C1–C4 的成熟度尺 | 与 L1–L4 成熟度阶梯不是同一把尺 |

### 三处需要注意的张力

**① 两套战略语法并存。**
`os-yuanli` 用「数据→特征→观点→洞察→全局最优」五级阶梯；C3 用 CBM 六原语（Component / State / Heat / Battle / Tradeoff / Reality-Reuse）。
YPORT4-G0 第 1.2 条明确要求"所有战略页面必须能映射到六原语之一，**不能另造平行战略语法**"。
→ 结论：五级阶梯可以作为 `Heat → Battle` 晋级时的**成熟度判据**使用（判断一个 Candidate 够不够格晋级），但不应作为独立的战略输出格式。二者需要一次显式 crosswalk 才能避免法权漂移。

**② 进化门槛宽严不一。**
`evolution-flywheel` 的硬门槛是"能不能**立刻被下次任务消费**"，并且允许"本轮无新增进化"作为合法状态。
C4 的门槛是 `Task2 preload → DEC/WPK/ACT 真实改变 → Reuse Receipt`。
→ 结论：`os-yuanli` 的 Evolution Note 只能产出 **Learning Candidate**，不能声称 Reuse 或 Compounding。这与 `yuanli.learning.propose` 的定位一致（AI 只能提候选）。

**③ 真源层级需要 crosswalk。**
`truth-hierarchy` 的第 1 层是"本地 artifacts / 当前仓库文件"最高。
但在 Estate 体系里，T1 是 GitHub Soul（Normative），本地仓库文件属于 T5 或工作副本。
→ 结论：`truth-hierarchy` 治理的是"**这次 session 内**该信谁"，Estate 治理的是"**这个领域**谁说了算"。两者不冲突，但 Agent 必须知道自己在用哪一把尺，不能用本地文件覆盖 Canon。

---

## 9｜归档状态与法权迁移信号

`os-yuanli-share-max` README 开头：

> ⚠️ **ARCHIVED(2026-07-27 · 仓库治理归档行动)**
> 归档原因：一次性任务完成/超14天未动。继任仓：`yuanli-os-starter`。
> 本仓只读保留作历史证据。

同批归档的还有 `os-yuanli-info-5l` / `os-yuanli-share-max` / `yuanli-website`（均 2026-07-27 前后最后 push）。

**这个信号的含义**：2026-07 之后，原力 OS 的法权与活跃开发已从"公开可分享的 Agent Skill 仓库群"收敛到私有的 `yuanli-strategy-soul`（Canon Authority）+ `yuanli-os-starter`（继任 starter）。
公开仓库群现在的角色是 **历史证据 / 方法论投影**，不再是 active canon。

因此：**读公开 skill 仓库可以理解方法论，但不能据此判断当前系统状态。** 当前状态必须回到 Soul 仓库与对应 Runtime Estate 验证。
