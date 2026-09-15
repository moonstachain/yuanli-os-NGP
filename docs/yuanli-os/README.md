# 原力 OS｜Agent 理解基线

这套文档的作用：让任何在本仓工作的 AI agent 在开始干活之前，**准确**理解原力 OS 的四模块体系、法权边界和用词纪律，不用每次重新解释。

> **法权声明**：本目录全部文件是 **Agent Context Projection**，不是 Canon。
> 正典法权在 `github.com/moonstachain/yuanli-strategy-soul`（私有），当前 `CONSTITUTION v1.2｜2026-08-07`。
> 冲突时一律以 Soul 为准。本目录不取得 C1–C4 任何法权，也不能作为"当前系统状态"的依据。

---

## 文档

| 文件 | 内容 | 什么时候读 |
|---|---|---|
| [`01-four-module-kernel.md`](01-four-module-kernel.md) | **C1–C4 四模块内核**、八段主链、复利两级证明门、七个不等号、五类 Truth Estate、三 Surface 法权矩阵、12 不可变量、MCP 六接口 | 涉及原力OS 概念、判断真源、写战略/决策内容时 |
| [`02-agent-kernel-os-yuanli.md`](02-agent-kernel-os-yuanli.md) | **`os-yuanli` 方法内核**（治理OS × 工作OS）：六判断、3×3 矩阵、三层 gate、八份协议、6 轴审计 rubric，以及与 C1–C4 的 **crosswalk 与三处张力** | 要按原力方法接管一个任务时 |
| [`03-github-inventory.md`](03-github-inventory.md) | **88 个仓库的法权分层盘点**、三部曲十二模块、2026-07-27 归档批次、结构性风险与建议 | 要找某个能力在哪个仓、或判断某仓是否还有效时 |

精简版（供 agent 自动加载）：[`.cursor/rules/yuanli-os-context.mdc`](../../.cursor/rules/yuanli-os-context.mdc)

---

## 30 秒版

```
原力OS = 完整时间轴 Operating System
上位问题：如何让已经验证的价值不流失，并让下一轮更强？
Hero：让每一次输出都成为下一次输入。

四模块（四器官，一条闭环，不是四个页面）
C1 一纸文脉  Who / Why / Boundary / Authorization   → 输出 CTX（最小必要 Context）
C2 一个大脑  Evidence / Knowledge / Memory / Evaluation
C3 一张地图  Policy State，权威本体 = CBM 事业能力操作模型
C4 一条链路  Work / Action / Outcome / Learning / Reuse

八段主链
CTX → EVD → DEC → WPK → ACT → OUT → LRN → Reuse

复利两级门
Atomic Proof  = SECOND_TASK_REUSE_PROVEN
System Proof  = COMPOUNDING_AT_MEANINGFUL_SCALE

三个 Surface
GitHub = Canon Authority · Notion = Human Projection · Website = Public Projection
One OS × Three Surfaces × One Reality Loop × One Human Sovereign
```

三句最该记住的话：

> **主权归人，运维归系统。**
> **One Brain ≠ One Database。真源不搬家，法权按领域归位。**
> **没有 receipt / evidence / human gate，不允许宣称 PASS、Reality、Learning、Reuse 或 Compounding。**

---

## 本次盘点的可见性边界（重要）

盘点使用的 GitHub 令牌只对 `yuanli-os-NGP` 有 installation 权限。因此：

| 层 | 可见性 |
|---|---|
| 公开仓库（88 个，含 19 个已归档） | ✅ 全部可读 |
| `yuanli-strategy-soul`（Canon Authority） | ⛔ 404 |
| `yuanli-os-starter` / `LLM-Wiki` / `quant-workspace` / `yuanli-invest-rsi` | ⛔ 404 |
| Notion `Yuanli Portal` | ✅ 可读（MCP） |
| 本地 OB LLM-Wiki / NAS / 飞书 | ⛔ 不可达 |

按体系自己的纪律：**这里必须显式 fail-closed 说明缺口，不能用公开仓 + Notion 投影冒充 Canon。**
文档中所有 Soul 仓内容都是通过 Notion 投影和其他公开仓 README 的**外部引用重建**，标注为重建而非直读。

如需让后续 agent 直读 Canon，需要在 Cursor Dashboard（Cloud Agents → Secrets）配置一个对 `yuanli-strategy-soul` 有读权限的 GitHub token，或把该仓加入本 agent 的 installation 范围。
