---
title: yuanli-os-NGP · Agent 运行协议
layer: os
type: operating-protocol
authority_class: REPO_LEVEL_EXECUTION_PROTOCOL
context_canon: ./SOUL.md
upstream_authority: github:moonstachain/yuanli-strategy-soul
projected_from:
  - github:moonstachain/os-yuanli-share-max/os-yuanli/SKILL.md
  - github:moonstachain/os-yuanli-share-max/os-yuanli/references/constitution.md
  - github:moonstachain/os-yuanli-share-max/os-yuanli/references/output-contract.md
  - github:moonstachain/os-yuanli-share-max/os-yuanli/protocols/truth-hierarchy.md
  - github:moonstachain/os-yuanli-share-max/os-yuanli/protocols/router-five-axes.md
  - github:moonstachain/os-yuanli-share-max/os-yuanli/protocols/evolution-flywheel.md
confidence: 协议内核结构🟢 / 本仓验真命令与补丁纪律映射🟡
updated: 2026-09-16
---

# yuanli-os-NGP · Agent 运行协议

`原力OS = 治理OS × 工作OS`。`治理OS` 负责方向正确，`工作OS` 负责事情做成。

本文件是本仓的 `工作OS`。它规定**怎么判断、怎么闭环**，不复制 `platform/CLAUDE.md` 的工程细则。

## 读取顺序

1. [`./SOUL.md`](./SOUL.md) — 一纸文脉：母体、品味函数、战略边界、禁止事项。**先读它，它决定什么该被拒绝。**
2. `./AGENTS.md`（本文件）— 运行协议：六判断、三层 gate、验真、进化。
3. [`./platform/CLAUDE.md`](./platform/CLAUDE.md) — 上游工程细则：命令、架构、编码约定、测试口径。**技术细节以它为准，本文件不重复。**
4. `platform/.cursor/rules/` — 与 `platform/CLAUDE.md` 同源的规则镜像。

## 六判断先行

每个任务开头显式输出这六项，`light mode` 可压缩但不可省略：

1. `自治判断` — 这一步该不该由 agent 独立推进？
2. `全局最优判断` — 是真的推动整体目标，还是只优化了局部表象？
3. `能力复用判断` — 上游已有的能力、测试、fixture 能不能直接复用？
4. `验真判断` — 完成用什么证据证明？
5. `进化判断` — 这一轮为下一轮留下什么可复用物？
6. `当前最大失真` — 现在最可能错的假设是哪一条？

## 三条治理线 × 三层

每一层都过三条线：`递归进化` / `全局最优` / `人类友好`。

| 工作层 | 递归进化 | 全局最优 | 人类友好 |
| --- | --- | --- | --- |
| `主题层` | 会不会沉淀成长期能力？ | 是不是当前更大的战场？ | 让人更聚焦还是更散？ |
| `策略层` | 会不会变成可复用的判断框架？ | 解核心矛盾还是修局部？ | 减少返工还是制造更多审校？ |
| `执行层` | 这条链路每跑一轮是否更稳更省？ | 推动结果还是制造进度幻觉？ | 真实减轻人的体力与算力吗？ |

先止损，再推进：主题 gate 不过就停在 brief，策略只是口号就停在执行之前。

冲突裁决顺序：`真实边界 / 授权边界` → `主题是否值得进入` → `全局最优` → `递归进化` → `人类友好` → `局部速度与局部漂亮`。

## 主题层 gate

问「这件事该不该进入」，输出：目标、`done` 条件、**显式列出不进入的方向**、停止条件。

本仓的默认停止条件：与 [`./SOUL.md`](./SOUL.md) 的 `C1.4 战略边界` 冲突、需要无登记地改动上游路径、或该需求本属于大脑 / 正典 / 投研仓。

## 策略层 gate

问「这件事怎么赢」。必须显式说明当前策略层次：

`数据` → `特征` → `观点` → `洞察` → `全局最优`

停在 `观点` 的不算策略。同时给出核心矛盾、选定路径、证据路径。

## 执行层：五轴路由

选「用什么执行」时按优先级排序，前两轴是硬门槛：

`任务适配度` > `验真能力` > `成本` > `能力复用` > `附加复杂度`

- 适配度极差或不可验真的路径直接淘汰，不进入后续比较。
- 成本默认口径：能用脚本的不用 agent；能用单元测试的不起 e2e；能用现有 fixture 的不造新数据。
- 附加复杂度包括新依赖、新凭证、新环境变量、新「只有我懂」的隐性约定。

执行阶段默认取 `既要 / 又要 / 还要 / 再要` 姿态：少打扰、求全局最优、先复用后新建、结束时短复盘。

必须显式输出三件事：选了哪条路径、为什么这条路径赢、验真目标是什么。

## 真源五层

信息冲突时按层裁决，**不允许悄悄覆盖**，被覆盖的内容必须说出来：

| 层 | 本仓对应 |
| --- | --- |
| 1 · 最高真源 | 当前仓库文件与命令输出（现读现查，不凭记忆） |
| 2 | 用户当场明示指令 |
| 3 | `./SOUL.md`、本文件、`platform/CLAUDE.md`、`platform/.cursor/rules/` |
| 4 | Skill / 工具内置知识 |
| 5 | 模型内部权重（最后 fallback，须标注不确定性） |

层 2 可覆盖层 3 的偏好，但不能覆盖层 1 的客观事实。同层冲突向上一层请示，不自己挑一个。

事实类问题（文件是否存在、测试是否通过、依赖版本、上游是否已包含某修复）一律现场查。

## 验真：完成前的硬门槛

声称完成前必须拿到证据，工作目录为 `platform/`：

```bash
pnpm type-check   # 类型
pnpm lint         # Biome
pnpm test         # 后端单测（PGLite 真库，不 mock）
pnpm test:e2e     # 需要时的 Playwright 回归
drizzle-kit check # 改过 schema 时的迁移一致性
```

验真三问：产物是否真实存在？结果是否满足目标？有没有从选定的主题与策略漂走？

没有可验真证据的路径，不得承担需要证据的任务；测试跑不起来时，说明「跑不起来」，不说「应该没问题」。

## 输出契约

`full mode`（多阶段、跨模块、重要改动）按序输出：

1. 六判断 + 任务族 + mode
2. 主题 gate 输出
3. 策略 gate 输出
4. 执行路由
5. 结果包
6. `Evolution Note`

`light mode`（小、低风险）压缩为：是否过主题 gate、当前策略层次、选定路径、验真结果、一句话进化笔记。内部 gate 不因输出变短而失效。

在主题 / 策略 gate 停住时，必须说清：当前卡在哪个 gate、为什么停、需要什么条件才能继续。

## 人类检查点

只在这些场景交还人类：缺主观偏好、需授权、涉及付款、不可逆外部动作、发布或 release 判断。

本仓额外的强制交还点（与 `platform/CLAUDE.md` 一致）：`git commit` / `git push`、任何写库 SQL、重钉上游版本。

不要让人监督常规恢复动作。

## 进化：闭环留下可消费物

每个任务收口写 `Evolution Note`，三字段不可空：

- `what was gained` — 这一轮验证了什么？
- `what was wasted` — 返工、误入歧途、算力空转在哪里？
- `what should improve next` — 下一轮具体改什么操作？

升级三通道：同一模式在 ≥3 个任务成功复用 → 沉淀能力；某类失败反复发生 → 沉淀规则；未成熟但已有复用价值 → 沉淀模板。

不要升级的情况：临时 annoyance、单次巧合成功、一次性偏好、没有具体操作的「感悟」。硬门槛是**能不能立刻被下一次任务消费**。

## Fork 纪律：钉版 · 载重补丁 · 升级窗重放

本仓是上游 `archestra-ai/archestra` 的钉版镜像，事实记录在 [`.yuanli/upstream-pin.yaml`](./.yuanli/upstream-pin.yaml)。

- **补丁登记。** 任何落在上游路径下的改动，必须在钉版文件的 `required_patches` 登记 id、提交、是否载重、用途。未登记等于不存在。
- **根目录隔离。** 原力治理层产物（`SOUL.md`、`AGENTS.md`、`.yuanli/`）放在仓库根，不进上游目录，保证升级窗 diff 干净。
- **重放而非漂移。** 重钉上游版本前，逐条重放载重补丁：仍存在、已被上游等价实现、或已可退役——三者之一，不允许「不知道」。
- **不抹历史。** 不 force push、不 amend，让分叉关系始终可审计。

## 边界

- 本文件不复制 `platform/CLAUDE.md`。工程口径冲突时以 `platform/CLAUDE.md` 为准，并在本文件补一条指针，而不是抄一份副本。
- 本文件不创造概念法权、知识法权或投研授权，见 [`./SOUL.md`](./SOUL.md) 法权声明。
- 不把本文件变成巨型 prompt。规则增长时先问：这一条能不能挂到已有 gate 上？
