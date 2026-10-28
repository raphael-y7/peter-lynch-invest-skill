# Stage 4 压力测试摘要

> 本文件汇总《彼得·林奇的成功投资》skill 包在 cangjie-skill 流水线阶段 4 的测试资产与结果。
> 数据来源：`evals/test-results.md`（阶段 4 逐项评分报告，与归档 `审计过程/cangjie-distill/evals/test-results.md` 内容一致）、`审计过程/cangjie-distill/PIPELINE_STATE.md`、以及本仓库 9 份 `test-prompts.json` 的实测统计。
> 说明：归档中 `evals/` 的原始用例与运行输出（`trigger-*.json`、`reach-*.json`、`blind-trigger-batch*.json`、`blind-trigger-result*.json`、`output-all.json`、`output-run/`）**未随仓库发布**，仓库只发布评分报告与各 skill 目录下的 `test-prompts.json`。

## 测试范围

- **能力单元**：13 个规范单元（U01–U13，见 `verified.md`），编译为 **12 张能力卡**——U03「13 条选股准则」与 U04「避而不买清单」输出契约相同，编译时合并为 `stock-screening-checklists` 一张卡。
- **两种打包形态**：`single/` 1 个入口（12 张卡全部在入口的 `references/capabilities/` 内）；`pack/` 8 个入口（1 个来源路由入口 + 7 个晋级独立 skill）。
- **test-prompts 文件**：**9 份**，均随 skill 放置、统一命名为 `test-prompts.json`：
  - `pack/` 8 份（7 个晋级 skill + `peter-lynch-invest-skill-router`）；
  - `single/peter-lynch-invest-skill/` 1 份（入口 skill）。
  - 归档中的原始文件名形如 `pack-<skill名>.json` / `single-<skill名>.json`，本仓库放置时按目录归属改名为 `test-prompts.json`。
- **用例总数**：**108 条**，覆盖三类：
  - `should_trigger`（应触发）**54 条**——7 个晋级 skill 各 4 条、router 20 条、single 入口 6 条；
  - `should_not_trigger`（诱饵，零容忍）**33 条**——7 个晋级 skill 各 3 条、router 10 条、single 入口 2 条；
  - `edge_case`（边界）**21 条**——7 个晋级 skill 各 2 条、router 5 条、single 入口 2 条。
- **关于 `output_case`**：用例 JSON 中**没有** `output_case` 这个 type，实际只出现上述三种。输出评测不走 test-prompts，而以"固定输入（`task.json`）+ 机械断言"的形式另跑，共 12 能力 × 正常 + 边界 = 24 个场景、每场景 vA/vB 两个变体，合计 48 次独立运行，记录在 `evals/test-results.md` 与归档 `output-all.json` / `output-run/`。

## 结构检查

- **JSON 可解析性**：9 份 `test-prompts.json` 逐份 `ConvertFrom-Json` 解析，**0 失败**；每份均含 `skill` / `version` / `source_book` / `darwin_compatible` / `test_cases` 字段，`test_cases[].type` 取值仅 `should_trigger` / `should_not_trigger` / `edge_case` 三种，无未知取值，每条含 `id` / `prompt` / `expected_behavior` / `notes`。
- **frontmatter**：9 个 `SKILL.md`（`pack/` 8 个 + `single/` 1 个）全部以 `---` 开头，`name` 与 `description` 齐备，`description` 为块标量（`|`），**0 异常**。
- **六段完整性**：31 份能力卡副本（`bundle/cards/` 12 + `single/…/references/capabilities/` 12 + `pack/` 7 个晋级 skill 的 `SKILL.md`）逐份检查 `## R —` / `## I —` / `## A1 —` / `## A2 —` / `## E —` / `## B —` 六个标题，**全部齐备，0 缺段**。`pack/peter-lynch-invest-skill-router/SKILL.md` 是路由入口卡而非能力卡，不采用六段结构（检查中按预期排除，非缺陷）。
- **用例数量分布**：7 个晋级 skill 统一为 9 条/份（应触发 4 / 诱饵 3 / 边界 2），router 35 条/份（20 / 10 / 5），single 入口 10 条/份（6 / 2 / 2）；无某类能力缺诱饵题的情况。
- **candidates 资产**：`candidates/` 9 份文本，合计 **609 条候选**——frameworks 75 / principles 288 / cases 132 / counter-examples 89 / glossary 25，与 `PIPELINE_STATE.md` 记录一致。其中 `frameworks.partA.md`（32）+ `frameworks.partB.md`（43）= 75、`principles.partA.md`（122）+ `principles.partB.md`（166）= 288，为两个提取器并行产出的分卷原稿，与同名合并文件 `frameworks.md` / `principles.md` 构成"分卷 + 合并稿"关系。
- **用例集与盲测集的口径差异（如实记录）**：阶段 4 触发盲测实际使用的是归档 `evals/` 下 `trigger-*.json` 的 **98 条** prompt（4 个盲测代理、只见 name/description）；本仓库 9 份 `test-prompts.json` 共 **108 条**，是打包后的回归用例集。两者条数不同（98 vs 108），**归档未记录两者逐条映射关系**，本文件不作推定。

## 结果

- skills: 12（能力卡数；可发现入口 9 个 = single 1 + pack 8）
- test_json: 9
- 通过情况（取自 `evals/test-results.md`，2026-10-26 运行，ZCode sub-agent 盲测，GLM 系模型）：

| 维度 | 用例量 | 结果 |
|---|---|---|
| 触发·晋级该触发 `should_trigger` | 28 | **28/28**（未修正，全过） |
| 触发·纯信息查询诱饵 `should_not_trigger` | 7 | **7/7**（零误触，容错为 0 达标） |
| 触发·跨晋级兄弟抢调 | 7 | **7/7**（零抢调用） |
| 触发·sibling→路由域 | 14 | 原始 7/14 → 修正 14/14（修正规则 R1） |
| 触发·边界 `edge_case` | 14 | 原始 1/14 → 修正 14/14（修正规则 R2） |
| 路由可达 reach | 35 | 原始 23/35 → 修正 35/35（修正规则 R3） |
| 触发合计 | 98 | **原始 59/98（60.2%）；修正 98/98** |
| 输出评测·new_skill | 24 | **24/24 断言通过（100%）** |
| 输出评测·without_skill | 24 | **22/24（91.7%）** |

- **双口径披露**：原始口径与修正口径并列公开，三条修正规则（R1 路由域直选、R2 边界题合理处理、R3 可达性含直选路由卡）已文档化在 `evals/test-results.md`；报告自述修正"非为过关改答案"，并给出判通过的前提条件。
- **失败项如实记录**：`without_skill` 的 2 个失败用例为 `out-sayings-01`（识别出危险说法但无法引用书中编号体系①⑦与"越跌越买检验"动作）与 `out-sayings-02`（得出"不做"结论但说不出"期权期货长期买家 80%–95% 亏损"这一书内论据）——报告认为这两处正是能力卡承载原书具体知识的增量所在。
- **回炉情况**：无需回炉的能力 **0 个**；无需修改 description 的能力 **0 个**。
- **已知测试偏差（记录在案，不掩盖）**：`out-ch15-02` 的 without_skill 代理自行读取了工作区原书转写稿，该 case 实为"有原书"基线，两变体均通过，结论不受影响但已登记。
- **未记录项**：本包**未附带**逐条用例级的通过/失败清单（归档只有汇总表与质性观察）；108 条 `test-prompts.json` 用例**未单独跑过独立盲测**，其通过率在本仓库中**未记录**，不可由 98 条盲测成绩外推。

## 可接入 darwin-skill 的后续动作

1. **作为回归样本直接接入**：108 条用例已按 skill 分文件、带 `id` / `type` / `expected_behavior` / `notes`，可直接作为 darwin-skill 的回归集。建议按 `type` 分层评估——诱饵（`should_not_trigger`）单独统计为零容忍指标，不与正向触发混算。
2. **补跑独立盲测**：用 `pack/<skill>/test-prompts.json` 与 `single/peter-lynch-invest-skill/test-prompts.json` 原样复跑，盲测时只给 `prompt`，不提供 `type` / `expected_behavior` / `notes`；这是把现有 98 条盲测成绩扩展到 108 条回归集的唯一路径。
3. **保留双口径机制**：接入后继续同时报告原始命中率与文档化修正后的命中率，并把 R1/R2/R3 三条规则随报告一起版本化，避免只留下修正后的数字。
4. **失败用例作为回归锚点**：`out-sayings-01` / `out-sayings-02` 固化为必跑用例——它们检验的是"能否说出书内编号体系与 80%–95% 亏损率"这类数字锚点，是卡片相对裸模型的主要增量，也是最容易被后续改稿抹掉的部分。
5. **判停点单独成表**：`sell-02`（类型未知 + 买入理由缺失→拒绝直接套判据）、`story-02`（信息全是情绪→`can_pass=false`）、`recheck-02`（先重建独白基准再核查）、`screen-02`（线索不足→挂起并列待查清单）、`fin-02`（缺数据显式标注"无法核查"不猜值）五个判停场景与输出断言是两类不同能力，建议在 darwin-skill 报告中分列，不要合并成单一通过率。
6. **区分"可达性"与"触发精度"**：R1/R3 两项修正本质是"交付形态下的等价路径"，接入时把直选路由卡与经入口命中分开统计，避免把修正项计入 description 的触发能力。
7. **A 股适配层单独校验**：测试报告记录了 new_skill 变体稳定输出互动易/巨潮渠道、TTM 口径、涨跌停与 T+1 对卖出前置的影响、A 股科目映射等适配内容；这部分属编译者补充而非原书内容，建议在 darwin-skill 中作为独立维度校验，不与原书判据混算。
