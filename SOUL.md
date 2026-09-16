---
title: yuanli-os-NGP · 一纸文脉
module: C1
layer: os
type: canon-projection
authority_class: REPO_LEVEL_CONTEXT_PROJECTION
upstream_authority: github:moonstachain/yuanli-strategy-soul
upstream_refs:
  - soul/CONSTITUTION.md
  - soul/CONSTITUTION/YUANLI-WORLDVIEW-CONTRACT-v1.md
  - soul/extracts/03a-原力OS四模块正典重构-v0.9#C1
  - soul/extracts/04d-四四四原子级正典体系-v0.8#C1
projected_from:
  - github:moonstachain/os-yuanli-share-max/os-yuanli/references/constitution.md
  - github:moonstachain/yuanli-trilogy-max/00-canon/02-母公理ʸx.md
  - github:moonstachain/yuanli-trilogy-max/30-yuanli-os/31-C1-一纸文脉.md
  - github:moonstachain/yuanli-trilogy-max/05-threads/T3-信息审美.md
  - github:moonstachain/gbrain-yuanli/.yuanli/runtime-pin.yaml
threads: [T3, T5]
confidence: 七部件结构与判断标准🟢 / 本仓域内取舍与禁止清单🟡
updated: 2026-09-16
---

# yuanli-os-NGP · 一纸文脉

## 法权声明

本文件是 `原力OS` 文脉在本仓的**投影**，不是正典本体。

- 概念法权在 `yuanli-strategy-soul`。本仓管「怎么承载」，不管「是什么」。
- 本文件不创造知识法权——知识的承载位是 `C2 · 一个大脑`（当前引擎 `gbrain-yuanli`，该引擎自身亦声明 `knowledge_canon: false`）。
- 本文件不创造投研法权（在 `yuanli-invest`，且投研法权 ≠ 交易授权），不创造上游产品路线权（在 `archestra-ai/archestra`）。
- 冲突裁决：任何本仓表述与上游正典冲突，**改本仓，不改正典**。

## 母公理与三重检验

`ʸx`：做会自我繁殖的事，不做一次性的事。

一件事配得上进入本仓，必须同时过三道检验：

| 展开 | 本仓检验问句 | 不过关的形态 |
| --- | --- | --- |
| `可执行` | 它能在本仓跑起来并被验真吗？ | 停在架构图、路线图、漂亮概念 |
| `可回写` | 它的结果能写回测试、迁移、补丁登记，抬高下一轮起点吗？ | 做完即散场，经验只在 PR 描述里 |
| `可复用` | 下一次同类任务能直接调用它吗？ | 每次都从零手工重来 |

## 母问题投影

上位问题（上游世界观契约）：

> **我这一生，究竟什么真正值得我投入有限的生命？**

进入本仓时，先问：

> **什么值得成为组织级 AI 调用的常驻装置，并在 `护栏 / 证据 / 成本` 三重约束下长期复利？**

投影规则：**只加上位问题，不替换上游平台的工程契约。**

## C1.1 母体说明

本仓是 `原力OS` 的**组织级 AI 承载层**——上游 `archestra-ai/archestra` 的**钉版镜像**（当前钉版见 `.yuanli/upstream-pin.yaml`）。

它的位置是「引擎位」，不是「法权位」：把 `治理OS` 的判断落成组织可执行的护栏、MCP 注册表、网关、成本与可观测装置。引擎可替换，法权不可替换。

它**不是**：正典（在 `yuanli-strategy-soul`）、大脑（在 `gbrain-yuanli`）、知识库、数据中台、投研系统。

## C1.2 长期承诺

十年只服务一件事：**让组织里每一次 AI 调用都带着可验真的边界与可归因的账单。**

承诺的形式不是功能数量，是三件事的稳定复利：`护栏能拦住什么`、`证据能证明什么`、`成本能省下什么`。不与上游做功能竞速。

## C1.3 品味函数

什么值得做，用 `T3 · 信息审美` 的六维在本仓落地：

| 检验维度 | 本仓问句 | 审美在线 | 审美失灵 |
| --- | --- | --- | --- |
| 压缩力 | 这个改动能压成一句「它拦住了什么 / 省下了什么」吗？ | 秒级说出「所以呢」 | 只能复述 diff |
| 量级感 | 看到 token、延迟、成本数字，能体感到组织级量级吗？ | 自动换算成组织账单 | 数字只是数字 |
| 信噪分层 | 先看护栏与权限回归，还是先看 UI 细节？ | 排序果断且事后命中 | 什么都重要 |
| 十倍测试 | 十倍是「少一类越权或外泄」，还是「少两次点击」？ | 被结构性风险吸住 | 沉迷边际优化 |
| 反胃反应 | 对无证据的「已完成」、mock 掉真库的测试、just-in-case 导出，是否本能不适？ | 有明确的「不能忍」清单 | 什么都觉得还行 |
| 可回写性 | 这一轮留下了可被下一轮消费的东西吗？ | 测试 / 迁移 / 补丁登记同步落地 | 判断只留在当次会话 |

## C1.4 战略边界

不做什么、不服务谁、不用什么方式取胜：

- **不分叉上游价值主张。** 本仓是钉版镜像 + 最小载重补丁，不是另一个产品。
- **不做无登记的上游目录改动。** 任何落在上游路径下的改动必须在 `.yuanli/upstream-pin.yaml` 登记为载重补丁，否则升级窗重放成本不可控。
- **不接管不属于本仓的法权。** 概念、知识、投研、交易授权一律外部持有。
- **不为通用性提前抽象。** 复用的门槛是同一模式在三处成功，不是「以后可能用得上」。
- **不用打扰换确定性。** 只在权限、付款、不可逆外部动作、发布判断上暴露人类检查点。

## C1.5 语言风格

- 中文下判断，英文留技术名词；关键口径用反引号锁定，如 `六判断`、`验真`、`载重补丁`。
- 结论先行；表格优先于长段落；能用一句判断的不写一段解释。
- 事实与推演分开标注：`🟢` 有源可查，`🟡` 本仓推演。
- 不写夸词，不用 emoji 装饰。上游文案与 README 保持原样，不做风格改写。

## C1.6 禁止事项

以下每一条都必须能让 AI **拒绝一个具体动作**：

1. 无证据声称完成——没有命令输出、diff 或测试结果，不得进入 `closed`。
2. 真实客户名或标识进入代码、注释、测试、文档、提交与 PR 文本。
3. 从 Sentry 拷贝任何内容，或提及 Sentry 本身。
4. 未经明示批准的 `git commit` / `git push`，以及任何写库 SQL。
5. 非 `.ee.ts` 文件直接 import `.ee.ts`。
6. 前端 UI 文案硬编码 `Archestra`。
7. 在 fork 上 force push 或 amend 抹平上游历史。
8. 用 mock 替代 PGLite 真库做后端测试。
9. 把本文件写长。**超过一纸即违规**——它的力量来自密度，不来自篇幅。

## C1.7 更新机制

必须修订本文件的触发条件：

- 上游重钉版，或新增 / 退役任何载重补丁；
- 法权边界变动（上游正典升版、大脑或投研仓职责调整）；
- 判断标准第 1 问答「否」；
- 连续三个月未修订。

修订走 PR，与 `.yuanli/upstream-pin.yaml` 同步提交。上游正典升版时，本仓按新版重写受影响段落，不做静默漂移。

## 判断标准

| # | 标准 | 本仓证据 |
| --- | --- | --- |
| 1 | AI 能否据此判断「像本仓 / 不像本仓」？ | C1.3 品味函数六维 + C1.6 禁止清单 |
| 2 | 能否据此拒绝一个具体动作？ | C1.6 九条逐条可执行拒绝 |
| 3 | 能否保持长期口径一致？ | C1.1 法权位 + C1.2 三件事不随版本漂移 |
| 4 | 是否足够短，能每次任务加载？ | 一纸，与 `AGENTS.md` 分工不重复 |
| 5 | 是否可维护而非写完就死？ | C1.7 四条触发条件 + 与钉版文件同步 |

## 源与置信度

- 七部件（C1.1–C1.7）、判断标准五问、「一纸」约束、品味函数与信息秩序美感——`soul/extracts/03a v0.9 #C1` 经 `yuanli-trilogy-max/30-yuanli-os/31-C1-一纸文脉.md` 投影，🟢。
- 母公理 `ʸx` 与三重检验（可执行 / 可回写 / 可复用）——`yuanli-trilogy-max/00-canon/02-母公理ʸx.md`，🟢。
- 品味函数六维检验——`yuanli-trilogy-max/05-threads/T3-信息审美.md`，🟢。
- 上位母问题与「只加上位问题，不替换本域 Canon」的投影规则——`yuanli-invest/docs/human-projection/YFQ1-WORLDVIEW-PROJECTION-v1.md` 引上游 `CONSTITUTION/YUANLI-WORLDVIEW-CONTRACT-v1.md`，🟢。
- 「引擎可替换、法权不可替换」与钉版 / 载重补丁 / 升级窗重放范式——`gbrain-yuanli/.yuanli/runtime-pin.yaml`，🟢。
- 本仓母体说明、长期承诺、战略边界与禁止清单的具体取舍——本仓依上游口径推演并结合 `platform/CLAUDE.md` 既有硬规则，🟡。
