# verified.md — 阶段1.5三重验证通过的能力单元（13个）

> 验证标准：methodology/03-stage1.5-triple-verify.md（V1来源充分性 / V2可执行性walkthrough / V3任务增益）
> 每单元完整验证记录（含逐候选 decision、V1抽查、V2演练输入输出、B段素材、缺口）见 `verified-parts/U*.md`。
> 候选池总量 609 条（frameworks 75 / principles 288 / cases 132 / counter-examples 89 / glossary 25）。
> 编译去向：13 个规范单元编译为 **12 条能力**（`bundle/verified.yaml` 的 `capabilities` 实测 12 条）——U03「13条选股准则」与 U04「避而不买清单」输出契约相同，合并为 `stock-screening-checklists` 一张能力卡，故能力数与单元数相差 1。

## 单元总表

| unit | slug | 标题 | tasks | 成员规模 | decision | 记录文件 |
|---|---|---|---|---|---|---|
| U01 | classify-six-types | 六类公司分类判定（含产品净利润占比测算） | task-01, task-13 | 32候选→17成员 | verified | verified-parts/U01-classify-six-types.md |
| U02 | sell-rules-by-type | 分类型卖出判据（17.4六类清单） | task-02 | 13候选→8成员 | verified | verified-parts/U02-sell-rules-by-type.md |
| U03 | pick-13-criteria | 13条选股准则核查 | task-03 | 21成员 | verified | verified-parts/U03-pick-13-criteria.md |
| U04 | avoid-list | 避而不买清单（6类排除） | task-04 | 11成员 | verified | verified-parts/U04-avoid-list.md |
| U05 | pe-valuation | 市盈率与收益估值口径（P/E三重比较、vs增长率、收益线背离、买入时机） | task-05, task-14 | 24候选ID→12内容簇 | verified | verified-parts/U05-pe-valuation.md |
| U06 | financial-checklist-13 | 13项财务指标核查（+年报阅读法+福特数据链） | task-06 | 33成员 | verified | verified-parts/U06-financial-checklist-13.md |
| U07 | two-minute-story | 两分钟沉思独白（类型化故事模板） | task-07 | 核心6条 | verified | verified-parts/U07-two-minute-story.md |
| U08 | analyze-checklist-ch15 | 股票分析要点一览表（通用层+六类型专项，15.1） | task-08 | 核心8条 | verified | verified-parts/U08-analyze-checklist-ch15.md |
| U09 | recheck-holdings | 定期重新核查（触发器+三阶段定位） | task-09 | 核心3条 | verified | verified-parts/U09-recheck-holdings.md |
| U10 | dangerous-sayings | 12种危险说法识别与反驳+期权期货卖空否定 | task-10, task-15 | 35项（规则+机制双层） | verified | verified-parts/U10-dangerous-sayings.md |
| U11 | portfolio-rules | 组合构建与持有纪律 | task-11 | 17候选→16成员 | verified | verified-parts/U11-portfolio-rules.md |
| U12 | self-test-eligibility | 入市自我测试与业余优势定位 | task-12 | 47成员+4 reference | verified | verified-parts/U12-self-test-eligibility.md |
| U13 | research-info-gathering | 信息获取与调研程序 | task-06/08辅助 | 15核心+5相邻 | verified | verified-parts/U13-research-info-gathering.md |

## 支撑素材（阶段2 的 A1/B 段来源）

- **案例 132 条**：123 条映射到 13 单元（映射表与各单元代表案例★见 `support-mapping.md`）；9 条纯叙事/论据转 `references.md`。
- **反例 89 条**：86 条映射（各单元代表反例★见 `support-mapping.md`）；3 条转 `references.md`。
- **术语 25 条**：全部保留，阶段 3 进 GLOSSARY；与单元强关联已在映射表标注。

## 去重与降级汇总

- rejected-duplicate（去重保留canonical）：U01内9条、U02内3条（归U11）、U08内15.2重述32条指向各专题单元、各单元内部同义合并若干——全部明细见各 verified-parts 文件的 candidate_decisions 字段，汇总登记于 `rejected/duplicates.md`。
- reference 降级（有来源价值不可独立执行）：长期收益数据论据、鸡尾酒会理论（作者自嘲）、买入时机叙事等 → `references.md`（阶段3并入 book/overview.md 参考区）。
- needs_review（不进active池）：39项缺口与双口径冲突 → `needs-review.md`（含：六类边界4-10%/12-20%无仲裁规则、福特净现金16 vs 16.30两口径、La Quinta 15倍/11倍双口径、L3474转写重复句、止损厌恶与A股实践冲突等）。

## 验证质量说明

- V1 抽查覆盖每单元全部核心规则的原文引用（数字阈值逐字核对：六类增长率口径、17.4全部卖出阈值、HSN 3→47→3.5、下一个跌59%-96%、1:2.3、福特16.30数据链、表13-1/13-2复利与弹性、期权80%-95%亏损等）。
- V2 walkthrough 均用新输入完成并核对输出（各单元记录含 input/expected/observed）；纸面演练，阶段4再做真实执行测试。
- 已知系统性缺口（不阻塞、进A股适配节与B段）：1988年美国制度背景（无涨跌停/T+0/年底避税抛售/价值线与Form 4渠道）、"问经纪人"与"拜访总部"A股不可行、"撒谎持2万股"不可移植（合规）、LIFO已禁用、P/E≈增长率对周期股不适用（书中自行承认）。
