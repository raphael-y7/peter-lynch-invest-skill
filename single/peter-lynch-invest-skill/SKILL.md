---
name: peter-lynch-invest-skill
description: |
  基于《彼得·林奇的成功投资》的 A 股选股分析工具包：先给公司归类（缓慢增长/稳定增长/快速增长/周期/困境反转/隐蔽资产六类），
  按类型设定期望与卖出判据，用 P/E 与收益口径估值，用 13 项财务指标核查基本面，用双向清单筛选候选，
  识别 12 种危险心理说法。适用 trigger：分析个股基本面、估值贵不贵、该不该卖、持仓复查、组合搭配；
  不适用：预测大盘涨跌、期权期货卖空、短线择时。每张能力卡含独立「A股适配」小节（编译者补充，非原书内容）。
metadata:
  cangjie.generated-by: cangjie-tools v2.5.0
  cangjie.variant: single
  cangjie.bundle-id: bundle.peter-lynch-invest-skill
  cangjie.capability-count: 12
  cangjie.entrypoint-count: 1
---
# 彼得·林奇的成功投资（One Up on Wall Street） — 全书能力入口

## 触发与不触发

**适用**：与本书能力域相关的咨询与任务（见下方路由表的意图列）。
**不适用**：
- 大盘/指数走势预测与择时（书中明确否定）
- 期权、期货、卖空策略（书中结论为明确不做，仅提供否定理由）
- 债券与基金选择的完整方法（书中仅作收益对比论据）
- 具体个股买卖推荐

## 核心原则（常驻速览，概览类问题读到这里即可回答）

1. 投资的是公司，不是股市；不预测市场，唯一的买入信号是找到值得研究的公司
2. 先分类后行动：六类公司分类决定买入期望、核查重点与卖出判据
3. 股价长期跟随收益：P/E 与增长率比较、与历史比较、与整体市场比较，绝不买超高 P/E
4. 发现只是第一步：下单前必须完成研究并能两分钟讲清"故事"（为什么买、成功条件、风险）
5. 卖出按类型判据执行，价格下跌本身不是卖出理由；"拔掉鲜花浇灌野草"是最大错误
6. 避开热门股、故事股、多元恶化与一切期权期货卖空

## 能力路由（先读本表，按意图加载 1 张能力卡）

| 用户意图 | 先读 | 补读/备注 |
|---|---|---|
| 判断一家公司属于六类中的哪一类；判断热门产品对公司的意义（产品净利润占比测算）；评估一家大公司股票的上涨空间上限 | references/capabilities/classify-six-types-skill.md | references/capabilities/analyze-checklist-ch15-skill.md、references/capabilities/sell-rules-by-type-skill.md、references/capabilities/two-minute-story-skill.md |
| 判断一只持仓股票现在该不该卖；区分"基本面恶化必须卖"与"价格波动不用卖"；识别煽动效应与过早卖出陷阱 | references/capabilities/sell-rules-by-type-skill.md | references/capabilities/classify-six-types-skill.md、references/capabilities/recheck-holdings-skill.md、references/capabilities/dangerous-sayings-skill.md |
| 用13条理想特征为候选公司打分；用负面清单排除候选（热门股/下一个/多元恶化/小道消息/大客户依赖/花哨名字）；判断一条股票线索值不值得继续研究 | references/capabilities/stock-screening-checklists-skill.md | references/capabilities/pe-valuation-skill.md、references/capabilities/financial-checklist-13-skill.md |
| 判断一只股票当前价格贵不贵；计算并解读市盈率（vs增长率/历史区间/行业/整体市场）；用收益线与股价线背离判断风险；判断买入时点（整体市场P/E水位+恐慌窗口） | references/capabilities/pe-valuation-skill.md | references/capabilities/financial-checklist-13-skill.md、references/capabilities/stock-screening-checklists-skill.md、references/capabilities/analyze-checklist-ch15-skill.md |
| 从年报/财报中提取并解读13项关键财务指标；快速阅读一份年报（跳过文字直取数字）；用每股净现金与负债结构判断公司真实买价与生存能力 | references/capabilities/financial-checklist-13-skill.md | references/capabilities/research-info-gathering-skill.md、references/capabilities/pe-valuation-skill.md、references/capabilities/analyze-checklist-ch15-skill.md |
| 对一只股票做全面的基本面核查；系统化组织一次完整的个股分析 | references/capabilities/analyze-checklist-ch15-skill.md | references/capabilities/classify-six-types-skill.md、references/capabilities/pe-valuation-skill.md、references/capabilities/financial-checklist-13-skill.md、references/capabilities/two-minute-story-skill.md |
| 识别自己或他人话语中的危险投资说法；用书中论据逐条反驳；对期权期货卖空提议给出否定决策 | references/capabilities/dangerous-sayings-skill.md | references/capabilities/sell-rules-by-type-skill.md、references/capabilities/recheck-holdings-skill.md |
| 下单前组织买入理由（类型化故事线）；检验自己是否真懂一家公司 | references/capabilities/two-minute-story-skill.md | references/capabilities/classify-six-types-skill.md、references/capabilities/analyze-checklist-ch15-skill.md、references/capabilities/recheck-holdings-skill.md |
| 判断持仓是否/何时需要重新核查；系统复查一家已持有公司的基本面变化；定位快速增长型公司所处阶段 | references/capabilities/recheck-holdings-skill.md | references/capabilities/two-minute-story-skill.md、references/capabilities/sell-rules-by-type-skill.md、references/capabilities/dangerous-sayings-skill.md |
| 决定持仓数量与类型搭配；判断一笔新买入对组合的影响；处理"卖什么换什么"的换仓决策 | references/capabilities/portfolio-rules-skill.md | references/capabilities/sell-rules-by-type-skill.md、references/capabilities/self-test-eligibility-skill.md |
| 判断当前是否适合入市/加仓；定位自己的信息优势来源（工作/消费现场） | references/capabilities/self-test-eligibility-skill.md | references/capabilities/portfolio-rules-skill.md |
| 系统获取一家公司的真实经营信息；向上市公司提问（问题清单）；甄别投资者关系话术（只取数据） | references/capabilities/research-info-gathering-skill.md | references/capabilities/financial-checklist-13-skill.md、references/capabilities/analyze-checklist-ch15-skill.md |

**非能力类查询**：
- 书名/作者/章节/整书概览 → references/overview.md
- 术语解释 → references/glossary.md
- 决策规则速查（不需要原文依据时） → references/cheatsheet.md
- 完整意图与关键词索引（本表未覆盖的意图先查这里） → references/capability-index.md

## 加载规则

- 每次任务先读本文件，再按路由表加载 **1** 张能力卡；任务明确跨域时最多加载 2 张。
- 概览/书名类问题不加载能力卡，用「核心原则」与 overview.md 回答。
- 路由表与 capability-index.md 都无法命中的意图，明确告知超出本书范围，不要硬套。

## 边界与判停

- 公司类型无法判定时，先回到分类能力完成归型，不带着模糊类型继续分析
- 关键财务数据（收益、负债、现金、增长率）缺失时先补数据，不猜值
- 用户资金为两三年内必需用途或未通过入市三问时，停止选股分析（U12）
- 候选命中避买清单硬性红旗（热门股/多元恶化/单一客户依赖等）时，直接排除不再进入估值
