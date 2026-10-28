<h1 align="center">彼得·林奇的成功投资 Skill</h1>

<p align="center">中文 | <a href="README.en.md">English</a></p>

一套可直接使用的 AI skill 工具包——把彼得·林奇《彼得·林奇的成功投资（One Up on Wall Street）》里的选股与持有方法，蒸馏成 12 张可单独触发、也可组合调用的能力卡。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skills 能解决什么问题

- 手里一只股票，说不清它到底属于六类公司里的哪一类——而类型不定，买多少、什么时候卖、盯哪个指标就全都是错的
- 股价跌了 30%，脑子里冒出"已经跌这么多了不可能再跌""只有 3 块钱能亏多少"，却没有一套能逐条反驳的工具
- 看到 P/E 40 倍、业绩增速 15%，判断不了贵不贵；看到 P/E 只有 8 倍又以为是便宜（低 P/E 不等于便宜，周期股甚至要反着读）
- 年报翻了三页就放下，不知道先抓哪几个数字：每股净现金怎么算、负债多少算危险线、存货增速超过销售意味着什么
- 一只票涨了一倍、新闻全是夸、分析师全给最高评级，不知道该落袋还是继续拿；跌了 25% 又想割
- 持仓该 5 只还是 20 只、卖了的钱立刻买什么、为什么"拔掉鲜花浇灌野草"是最大的错误

## 蒸馏了什么

12 张能力卡，按"先归型、再过筛、再算账、再讲清故事、最后管纪律"的顺序组织：

- **分类闸门**：`classify-six-types`（六类公司分类判定：缓慢增长 / 稳定增长 / 快速增长 / 周期 / 困境反转 / 隐蔽资产，含热门产品净利润占比测算）
- **候选筛选**：`stock-screening-checklists`（13 条选股准则正向打分 + 6 类避而不买负向排除，双向把关）
- **财报与估值**：`financial-checklist-13`（13 项财务指标核查：现金头寸、负债结构、股息记录、账面价值陷阱、隐蔽资产、自由现金流、存货、养老金、增长率、利润率）、`pe-valuation`（P/E 三重比较、(增长率+股息率)/P/E、收益线与股价线背离、两个买入窗口）
- **全面核查**：`analyze-checklist-ch15`（第 15 章通用要点 + 六类型专项核查，一次完整尽调的骨架）
- **信息与收口**：`research-info-gathering`（年报数字 / IR 提问 / 实地验证三层调研，只取事实不取形容词）、`two-minute-story`（下单前两分钟独白：为什么买、成功条件、主要风险，讲不清就不买）
- **持有与卖出**：`recheck-holdings`（新情况触发核查、价格波动本身不触发；快速增长公司三阶段定位）、`sell-rules-by-type`（六类卖出判据表，"已涨 N 倍"和"跌了多少"都不是判据）
- **组合与心理**：`portfolio-rules`（3–10 只、类型搭配、换股不换现金、不用止损指令）、`dangerous-sayings`（12 种危险说法逐条反驳 + 期权期货卖空否定）、`self-test-eligibility`（入市三问与业余优势定位，流水线第一道门槛）

其中 7 张晋级为独立 skill（`classify-six-types`、`sell-rules-by-type`、`stock-screening-checklists`、`pe-valuation`、`financial-checklist-13`、`analyze-checklist-ch15`、`dangerous-sayings`），另 5 张（`two-minute-story`、`recheck-holdings`、`portfolio-rules`、`self-test-eligibility`、`research-info-gathering`）经来源路由入口到达。每张卡都含独立的「A股适配」小节——该小节是编译者补充，非原书内容。

`verified.md` 记录的是验证阶段的 13 个规范单元：其中「13 条选股准则」与「避而不买清单」两个单元在编译时合并为一张卡（`stock-screening-checklists`，两者输出契约相同），所以最终产出 12 张能力卡。

## 两种打包模式：single 与 pack

同一套 12 张能力卡，按两种粒度各编译了一次。两者内容完全相同，区别只在"agent 能看到几个入口"。

| | single（单一入口） | pack（compact pack，多入口） |
|---|---|---|
| 可发现入口 | **1 个**：`peter-lynch-invest-skill` | **8 个**：1 个来源路由入口 + 7 个已晋级独立 skill |
| 12 张能力卡放在哪 | 全部在入口的 `references/capabilities/` 里，由入口按路由表按需加载 1–2 张 | 7 张高频卡各自独立成 skill；全部 12 张仍在 router 的 `references/` 里 |
| 触发方式 | 只有入口的 description 参与匹配，进入后靠路由表分流 | 7 个高频能力可被 description 直接命中，少一跳 |
| 升级维护 | 替换 1 个目录 | 替换 8 个目录 |

pack 里被晋级为独立 skill 的 7 张卡：

- `classify-six-types` — 六类公司分类判定
- `sell-rules-by-type` — 分类型卖出判据
- `stock-screening-checklists` — 双向筛选清单
- `pe-valuation` — 市盈率与收益估值口径
- `financial-checklist-13` — 13 项财务指标核查
- `analyze-checklist-ch15` — 股票分析要点一览表
- `dangerous-sayings` — 12 种危险说法识别与反驳

### 该装哪一种

按你的工作方式选，**只装一种**：

| 你的工作方式 | 推荐 | 原因 |
|---|---|---|
| 用 DSH / Codex / Claude Code 等有 skills 目录，希望列表干净 | single | 只占 1 个入口，能力一张不少 |
| 日常问题高度集中在"这是哪类公司 / 该不该卖 / 贵不贵 / 财报怎么看 / 帮我把关 / 这话说得对不对" | pack | 这 7 类正是被晋级的独立 skill，能直接命中 |
| 要分发给多个 agent 或团队，各自按需取用 | pack | 可以只装其中几个独立 skill，不必整包 |
| 只想装一次、不想维护多个目录 | single | 升级时只替换 1 个目录 |

> 两版由同一个 Bundle 编译，能力内容一致。**同时安装会重复触发**，请只装一种。

## 效果示例

### 示例 1：翻倍之后，新闻全在夸——该不该卖

**用户问题**

"这只票我 18 块买的，现在 42 块，翻了一倍多。最近新闻全是夸它的，分析师也基本都给最高评级。要不要先落袋？"

**skill 如何判断**

- 先 `classify-six-types`：用近 3–5 年净利增速归型，20%–25% 区间落在**快速增长型**（佐证：规模小、成长性强）
- 进 `sell-rules-by-type` 的快速增长判据，三条硬判据逐条核：①P/E 30 倍而未来两年最乐观盈利增长预期只有 15%–20%（估值-增长错配）；②最近一季同店销售额降低 3%；③扩张失速——停止开新店、门店破旧、新店销售令人失望
- 用 `recheck-holdings` 定位所处阶段：扩张期 / 饱和期 / 衰退期，判断"增速放缓"是正常降速还是阶段切换
- 关键一步：这张卡明确写着「已涨 N 倍」本身不是卖出理由（玩具反斗城 1 买 5 卖的教训），价格涨跌都不构成判据

**最终回答示例**

> 先别用涨幅做决定——翻一倍在快速增长型里不是卖出信号，书里玩具反斗城就是被"涨太多了"这个念头反复卖飞了 25 倍。你的票归在快速增长型，判据只有三条：估值与增长错配（P/E 30 倍却只预期 15%–20% 增长）、最近一季同店销售额降 3%、扩张失速。三条都没命中，也没有"两位高管离职加盟对手""两周 12 城路演描绘极乐观前景"这类辅助信号，结论是**继续持有**，被排除的伪理由是"涨得多"和"新闻都在夸"。分析师最高评级和媒体吹捧反而要记一笔：40 个分析师最高评级 + 机构持股 60% + 3 家国家级杂志吹捧 CEO，是书里点名的过热组合。如果同店增速从 10% 掉到 2% 但还没到 -3%，那也不是卖，是**转复查**——按 `recheck-holdings` 定好下次看什么、什么时候看。

### 示例 2：P/E 40 倍、增长很快，能不能买

**用户问题**

"这家公司 P/E 40 倍，但业绩增长很快，是不是成长股就该享受高估值？能买吗？"

**skill 如何判断**

- 前置门 `classify-six-types`：先确认类型——周期股要**反着读 P/E**（盈利峰值时 P/E 显得最低，恰是最危险的时刻），这一步不做，后面全错
- 进 `pe-valuation`，用三把尺子量同一个 P/E：与收益增长率比（P/E ≈ 增长率算合理、只有一半算便宜、是增长率两倍则亏钱可能非常大）；(增长率+股息率)/P/E ≥ 1.5 才算吸引人；再与自身历史区间、整体市场 P/E 水位比
- 用 `financial-checklist-13` 交叉验证：每股净现金 =（现金 + 证券 − 长期负债）/ 股本，从股价里扣掉再算真实 P/E——账上现金多的公司，名义 P/E 会高估你实际付的价
- 最后一条独立红线：**绝不买市盈率特别高的股票**，它不参与任何比较，是否决项

**最终回答示例**

> 先算数，再谈故事。P/E 40 倍配 15% 的增长率，得分是 (15+2)/40 ≈ 0.43，远低于 1.5 的门槛；而 40 倍已经是 15% 增长率的两倍以上（2×15=30），按书里的口径属于"亏钱的可能非常大"那一档。卡片里的演算样例可以直接对照：股价 24.00、EPS 1.20、增长率 15%、股息率 2%，P/E = 20.00 倍、得分 0.85，结论已经是"偏贵，不买"——你的 40 倍比它还贵一倍。再看第二把尺子：它自己过去几年的 P/E 区间是多少？整体市场现在是什么水位？如果这 40 倍明显高于它自己的历史区间，那你要为"从此直到永远的高增长"付钱，而书里的麦当劳（P/E 50 倍跌回 13 倍）、雅芳（P/E 64 倍）、宝丽来（P/E 50 倍，18 个月跌 89%）都是这条路。还有一件事必须先做：先确认它不是周期股——周期股盈利见顶时 P/E 最低、最像便宜货，反着读才安全。所以答案是：**不买**，除非你能把增长率稳定抬到 20% 以上且这个 40 倍低于它自己的历史区间。

## 这些 skill 是怎么生成出来的

这套 skill 使用 **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** 的 RIA-TV++ 流水线生成，整个流程分六个阶段：

1. **整书理解（Adler 分析）**——用 Mortimer Adler 的分析阅读法，对全书做结构、解释、批判、应用四步拆解
2. **并行提取**——同时派多个专项提取器（框架、原则、案例、反例、术语），从原文中提取候选方法论单元（本书候选池 609 条）
3. **三重验证筛选**——每个候选必须通过三项检验：书内至少有 2 处独立佐证（跨域）、能回答书中未明说的新问题（预测力）、不是常识（独特性）
4. **RIA++ 构造**——按 R（原文引用）/ I（用自己的话重写）/ A1（书中案例）/ A2（未来触发场景）/ E（可执行步骤）/ B（边界与盲点）六个维度结构化
5. **Zettelkasten 链接**——找出能力卡之间的依赖、对比、组合关系，生成能力索引与路由表
6. **触发与输出测试**——为每张卡设计触发盲测题（含诱饵题：该触发时要触发，不该触发时要沉默）与输出评测场景，未通过的卡回炉重做，回炉后再做回归验证

本书的蒸馏还多一层处理：原书是 1980 年代的美国市场语境，因此每张卡都附了一节「A股适配」——把 GNP≈3% 的分类基准换成中国名义 GDP 增速、把投资者关系渠道换成互动易与巨潮资讯、把负债科目映射成 A 股报表口径。这一节是编译者补充，不属于原书内容。

## 测试与验证

本仓库连生成过程的测试材料一起发布：`evals/test-results.md` 是逐项评分报告，包含失败用例、修正规则与测试偏差的完整记录，不是只留通过记录。

- **触发精度**：98 条 prompt 打乱后交 4 个独立盲测代理，只看 12 张卡与路由入口的 name/description 逐条选择。硬指标全过——晋级技能该触发时 28/28、纯信息查询诱饵 7/7 零误触、晋级技能之间零抢调用 7/7
- **原始口径与修正口径同时披露**：原始命中 59/98（60.2%）；按报告里三条文档化修正规则（R1 路由域直选、R2 边界题合理处理、R3 可达性含直选）为 98/98，两条口径并列公开
- **输出评测**：12 张能力卡 × 正常 + 边界两个场景，共 24 个场景，48 个独立执行代理盲跑。new_skill 变体 24/24 断言通过（100%），without_skill 变体 22/24（91.7%）
- **两个失败用例说明卡片的价值**：without_skill 在 `out-sayings-01` / `out-sayings-02` 上说不出书中编号体系与"期权期货长期买家 80%–95% 亏损"这个关键论据——正是能力卡承载的书内数字锚点
- **判停纪律**：边界场景下卡片稳定拒答或转澄清（类型未知不套卖出判据、信息全是情绪则判 `can_pass=false`、数据缺失显式标注"无法核查"不猜值）
- **回炉情况**：无需回炉的能力 0 个，无需修改 description 的能力 0 个
- **已知测试偏差**：`out-ch15-02` 的 without 代理自行读取了工作区原书转写稿，该 case 实为"有原书"基线，两变体均通过，结论不受影响但记录在案

## 仓库结构

```text
peter-lynch-invest-skill/
├── README.md                        ← 你正在看的
├── README.en.md                     ← English version
├── LICENSE                          ← MIT
├── BOOK_OVERVIEW.md                 ← 整书理解（Adler 四步拆解，阶段 0 产出）
├── TEST_SUMMARY.md                  ← 阶段 4 压力测试摘要（范围 / 结构检查 / 结果）
├── CANGJIE_ADAPTATION.md            ← 仓颉适配说明（文本状态 / 蒸馏目标 / 证据规则 / 使用边界）
├── verified.md                      ← 13 个规范单元的三重验证结论
├── INDEX.md                         ← skill 地图：能力总表 + 依赖关系 + 加载顺序
├── bundle/                          ← 规范 Bundle（审计产物，源真相）
│   ├── verified.yaml                ← 12 张能力卡的完整定义与晋级结论
│   ├── cards/                       ← 12 张能力卡原稿
│   │   ├── analyze-checklist-ch15.md
│   │   ├── classify-six-types.md
│   │   ├── dangerous-sayings.md
│   │   ├── financial-checklist-13.md
│   │   ├── pe-valuation.md
│   │   ├── portfolio-rules.md
│   │   ├── recheck-holdings.md
│   │   ├── research-info-gathering.md
│   │   ├── self-test-eligibility.md
│   │   ├── sell-rules-by-type.md
│   │   ├── stock-screening-checklists.md
│   │   └── two-minute-story.md
│   └── book/                        ← 整书层素材
│       ├── overview.md
│       └── glossary.md
├── candidates/                      ← 阶段 1 五提取器候选池（609 条，审计留档）
│   ├── frameworks.md                ← 框架 75 条（合并稿）
│   ├── frameworks.partA.md          ← 框架分卷 A（32 条）
│   ├── frameworks.partB.md          ← 框架分卷 B（43 条）
│   ├── principles.md                ← 原则 288 条（合并稿）
│   ├── principles.partA.md          ← 原则分卷 A（122 条）
│   ├── principles.partB.md          ← 原则分卷 B（166 条）
│   ├── cases.md                     ← 案例 132 条
│   ├── counter-examples.md          ← 反例 89 条
│   └── glossary.md                  ← 术语 25 条
├── single/                          ← 单一入口模式
│   └── peter-lynch-invest-skill/
│       ├── SKILL.md                 ← 入口：触发条件 + 路由表 + 加载规则
│       ├── BUILD_MANIFEST.json      ← 编译清单与文件哈希
│       ├── test-prompts.json        ← 入口 skill 的回归用例（10 条）
│       └── references/
│           ├── overview.md          ← 整书概览
│           ├── capability-index.md  ← 完整意图与关键词索引
│           ├── cheatsheet.md        ← 决策规则速查
│           ├── glossary.md          ← 术语表
│           └── capabilities/        ← 12 张能力卡（与 bundle/cards 同名）
├── pack/                            ← 多入口模式（compact pack）
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── peter-lynch-invest-skill-router/
│   │   ├── SKILL.md                 ← 来源路由入口
│   │   ├── test-prompts.json        ← router 的回归用例（35 条）
│   │   └── references/              ← 12 张卡 + 4 个索引，供 router 内部调用
│   ├── analyze-checklist-ch15/
│   │   ├── SKILL.md
│   │   └── test-prompts.json        ← 回归用例（9 条）
│   ├── classify-six-types/
│   │   ├── SKILL.md
│   │   └── test-prompts.json        ← 回归用例（9 条）
│   ├── dangerous-sayings/
│   │   ├── SKILL.md
│   │   └── test-prompts.json        ← 回归用例（9 条）
│   ├── financial-checklist-13/
│   │   ├── SKILL.md
│   │   └── test-prompts.json        ← 回归用例（9 条）
│   ├── pe-valuation/
│   │   ├── SKILL.md
│   │   └── test-prompts.json        ← 回归用例（9 条）
│   ├── sell-rules-by-type/
│   │   ├── SKILL.md
│   │   └── test-prompts.json        ← 回归用例（9 条）
│   └── stock-screening-checklists/
│       ├── SKILL.md
│       └── test-prompts.json        ← 回归用例（9 条）
└── evals/
    └── test-results.md              ← 触发盲测与输出评测的逐项评分
```

## 如何使用

先把仓库克隆下来：

```bash
git clone https://github.com/raphael-y7/peter-lynch-invest-skill.git
```

### 装 single（推荐先试这个）

```bash
# macOS / Linux
cp -r peter-lynch-invest-skill/single/peter-lynch-invest-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\peter-lynch-invest-skill\single\peter-lynch-invest-skill "$env:USERPROFILE\.agents\skills\"
```

### 装 pack

只复制含 `SKILL.md` 的目录，不要把 `pack/` 下的两个 json 一起拷进 skills 目录：

```bash
# macOS / Linux
cd peter-lynch-invest-skill/pack
cp -r peter-lynch-invest-skill-router \
      classify-six-types \
      sell-rules-by-type \
      stock-screening-checklists \
      pe-valuation \
      financial-checklist-13 \
      analyze-checklist-ch15 \
      dangerous-sayings ~/.agents/skills/
```

```powershell
# Windows
$pack = ".\peter-lynch-invest-skill\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('peter-lynch-invest-skill-router','classify-six-types','sell-rules-by-type','stock-screening-checklists','pe-valuation','financial-checklist-13','analyze-checklist-ch15','dangerous-sayings') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` 是 DSH 的 skill 目录；用别的 agent 时换成它自己的 skills 目录即可（例如 Claude Code 是 `~/.claude/skills`）。

### 怎么确认装好了

装完问一句"这只票我翻倍了该不该卖"，看 agent 是否先去判定公司类型、再按类型套卖出判据，并明确说出"涨得多不是卖出理由"，而不是给你一段泛泛的技术分析或直接建议落袋。装的是 single 时，它会先读入口再按路由表进能力卡；装的是 pack 时，对应能力会被直接命中。

## 来源

- 《彼得·林奇的成功投资》（One Up on Wall Street）彼得·林奇、约翰·罗瑟查尔德 著

## 声明

本仓库只发布蒸馏后的 skill、索引与规则速查材料，不包含原书 PDF、EPUB、OCR 文件、截图或全书转写稿。能力卡中出现的原文引用仅用于标注方法论出处和保持可审计性。

书中所有数字判据（六类增长率分档、P/E 与增长率的倍数关系、13 项财务指标阈值、期权期货亏损率等）都是案例与经验归纳，原书未提供统计回测背书；部分标尺是 1980 年代美国市场口径，A股适配小节的重设值属编译者约定，使用时需按标的自行测试并声明所用口径。本仓库内容不构成投资建议。


## License

[MIT](./LICENSE)
