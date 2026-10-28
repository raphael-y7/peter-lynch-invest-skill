<h1 align="center">彼得·林奇的成功投资 Skill</h1>

<p align="center">中文 | <a href="README.en.md">English</a></p>

一套可直接使用的 AI skill 工具包——把彼得·林奇《彼得·林奇的成功投资》（One Up on Wall Street）里的选股与持有方法，蒸馏成 12 张可单独触发、也可组合调用的能力卡。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skills 能解决什么问题

- "这公司的产品最近卖爆了，能买它股票吗"——产品热和业绩涨是两回事：先算产品收入占比与产品利润占比，占比不到 1.5% 的利好推不动一家大公司的业绩
- "涨了 40%，该不该落袋"——同一个涨幅在六类公司里含义完全相反：缓慢增长型涨 30%–50% 就该兑现，快速增长型涨 2 倍可能才刚开始
- "这票 P/E 40 倍，贵不贵"——P/E 要和收益增长率比、和它自己的历史区间比、和整体市场水位比，另有一条"绝不买超高 P/E"的否决红线
- 年报几十页不知道看哪几行——13 项指标逐项过：先算每股净现金调低实际买价，再分辨负债是短期银行借款（最危险）还是长期债券（最安全）
- 选股线索一堆分不清该追哪条——13 条准则逐条加分，6 类避买清单命中即排除（热门行业热门股 / "下一个 XX" / 多元恶化 / 小声耳语 / 单一客户依赖 / 花哨名字）
- 跌了想割、涨了想跑、经纪人一劝就换股——12 种危险说法逐条识别反驳，卖出只认公司类型和买入理由是否仍然成立

## 蒸馏了什么

12 张能力卡，按"先备资格、再筛选、再估值核查、最后执行与持有"的顺序组织：

- **入市准备**：`self-test-eligibility`（入市自我测试与业余优势定位）
- **筛选**：`classify-six-types-skill`（六类公司分类判定）、`stock-screening-checklists-skill`（双向筛选清单（13条选股准则+避而不买清单））
- **估值**：`pe-valuation-skill`（市盈率与收益估值口径）、`financial-checklist-13-skill`（13项财务指标核查）
- **核查**：`research-info-gathering`（信息获取与调研程序）、`analyze-checklist-ch15-skill`（股票分析要点一览表（第15章通用+六类型专项核查））
- **执行**：`two-minute-story`（两分钟沉思独白）
- **持有与卖出**：`recheck-holdings`（定期重新核查）、`sell-rules-by-type-skill`（分类型卖出判据）、`portfolio-rules`（组合构建与持有纪律）、`dangerous-sayings-skill`（12种危险说法识别与反驳+衍生品否定）

## 两种打包模式：single 与 pack

同一套 12 张能力卡，按两种粒度各编译了一次。两者内容完全相同，区别只在"agent 能看到几个入口"。

| | single（单一入口） | pack（compact pack，多入口） |
|---|---|---|
| 可发现入口 | **1 个**：`peter-lynch-invest-skill` | **8 个**：1 个来源路由入口 + 7 个已晋级独立 skill |
| 12 张能力卡放在哪 | 全部在入口的 `references/capabilities/` 里，由入口按路由表按需加载 1–2 张 | 7 张高频卡各自独立成 skill；其余 5 张仍在 router 的 `references/` 里 |
| 触发方式 | 只有入口的 description 参与匹配，进入后靠路由表分流 | 7 个高频能力可被 description 直接命中，少一跳 |
| 升级维护 | 替换 1 个目录 | 替换 8 个目录 |

pack 里被晋级为独立 skill 的 7 张卡：

- `classify-six-types-skill` — 六类公司分类判定
- `stock-screening-checklists-skill` — 双向筛选清单（13条选股准则+避而不买清单）
- `pe-valuation-skill` — 市盈率与收益估值口径
- `financial-checklist-13-skill` — 13项财务指标核查
- `analyze-checklist-ch15-skill` — 股票分析要点一览表
- `sell-rules-by-type-skill` — 分类型卖出判据
- `dangerous-sayings-skill` — 12种危险说法识别与反驳+衍生品否定

### 该装哪一种

按你的工作方式选，**只装一种**：

| 你的工作方式 | 推荐 | 原因 |
|---|---|---|
| 用 DSH / Codex / Claude Code 等有 skills 目录，希望列表干净 | single | 只占 1 个入口，能力一张不少 |
| 日常问题高度集中在"这算什么类型的公司 / 贵不贵 / 该不该卖 / 这公司有没有雷" | pack | 这四类正是被晋级的独立 skill，能直接命中 |
| 要分发给多个 agent 或团队，各自按需取用 | pack | 可以只装其中几个独立 skill，不必整包 |
| 只想装一次、不想维护多个目录 | single | 升级时只替换 1 个目录 |

> 两版由同一个 Bundle 编译，能力内容一致。**同时安装会重复触发**，请只装一种。

## 效果示例

### 示例 1：产品卖爆了，能不能买它家股票

**用户问题**

"这家公司的产品最近卖爆了，全网都在讨论，能买它股票吗？"

**skill 如何判断**

- 先过 `classify-six-types-skill`：因热门产品注意到公司时，第一步不是看销量，是算两笔账——产品收入占比 = 产品销售收入 ÷ 公司总收入；产品利润占比 = 产品利润 ÷ 公司总利润
- 用书里的两个锚点裁决：收入占比 < 1.5%（Bufferin 之于百时美，第 7 章 L1021）→ 产品再热也推不动业绩；利润占比 ≥ 15%（Sterling 的阿司匹林，L1023）→ 才可认定是业绩主驱动
- 再判规模（与同业比大 / 中 / 小，规模越大涨幅上限越低），然后按公司自身的净利增速归型：≈3% 缓慢增长、10%–12% 稳定增长、20%–25% 快速增长，收益形态兜住周期型、困境反转型、隐蔽资产型三类
- 类型确定后输出期望区间与下一步入口（估值口径、卖出判据、第 15 章核查清单）

**最终回答示例**

> 先别因为产品火就下单，算两笔账：产品收入占公司总收入多少、产品利润占总利润多少？书里给了两个锚点——收入占比不到 1.5%（Bufferin 之于百时美），这类利好对业绩几乎没有推动，新闻出来股价涨 50 美分就结束了；利润占比到 15% 以上（Sterling 的阿司匹林），才算真正的业绩主驱动。
> 然后归型。如果公司近 3–5 年净利年增速落在 20%–25%、规模还小，它是快速增长型，可以按快速增长型的清单继续核查；如果增速只有 4% 左右，它是缓慢增长型——涨 30%–50% 就是它的兑现区间，产品再火也不改变这一点。
> 两个诚实的提醒：一是 4%–10% 与 12%–20% 这两段边界区间，原书没有给仲裁规则，本卡的处理是按最近似归型并用股息、走势、规模二次佐证，输出时标注"边界区间、不确定"，不要自己编一个阈值；二是产品利润占比若落在 2%–15% 的中间带（两个锚点之间原书没有连续阈值），结论只能是"占比证据不足以支撑产品驱动逻辑"，要求补数据后重判。

### 示例 2：涨了 40%，该不该卖

**用户问题**

"这只票我 20 块买的，现在 28 块，涨了 40%，要不要落袋为安？"

**skill 如何判断**

- `sell-rules-by-type-skill` 的第一步不是看涨幅，是先确认类型——六类公司各有独立判据，同一个信号在不同类型下含义相反
- 缓慢增长型：自买入上涨 30%–50% 即兑现（17.4.1）
- 稳定增长型：股价线超过收益线，或 P/E 远超它自己的正常水平（17.4.2）；涨幅口径是"一两年涨 50% 开始考虑、30%–50% 可换一只还没涨的同类"
- 快速增长型：核心纪律恰恰是**不要过早卖出**——"已涨 N 倍"不在判据表上；真正的判据是 P/E 30 倍而未来两年最乐观盈利增长预期只有 15%–20%、最近一季同店销售降低 3%、扩张失速（17.4.4）
- 最后把两件事分开：故事破坏（买入理由失效，必须卖）与价格下跌（什么也不说明，不用卖）

**最终回答示例**

> 40% 这个数字本身不是判据。先回答一个问题：它属于六类里的哪一类？
> - 缓慢增长型：30%–50% 就是书里的兑现区间，你现在已经进区间了，可以卖。
> - 稳定增长型：书里给的是"一两年涨 50% 开始考虑"，40% 还没到——除非股价线已经明显超过收益线，或 P/E 远超它自己的正常水平。
> - 快速增长型：结论反过来，书里说这类股的卖出技巧是不要过早卖出而错失 10 倍股，涨 40% 完全不在判据表上。它该盯的是 P/E 30 倍却只配 15%–20% 的增长、同店销售单季降低 3%、扩张失速。
> 还有一句必须说明：书里明说"根本没有一个完全适用的统一公式可以确定卖出时机"，也明确斥责"翻番就卖 / 跌 10% 止损"这类不分类型的固定百分比。所以如果你现在说不出它属于哪一类，正确的动作是先归型（`classify-six-types-skill`），而不是先决定卖不卖。

## 这些 skill 是怎么生成出来的

这套 skill 使用 **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** 的 RIA-TV++ 流水线生成，整个流程分六个阶段：

1. **整书理解（Adler 分析）**——用 Mortimer Adler 的分析阅读法，对全书做结构、解释、批判、应用四步拆解
2. **并行提取**——同时派多个专项提取器（框架、原则、案例、反例、术语），从原文中提取候选方法论单元
3. **三重验证筛选**——每个候选必须通过三项检验：书内至少有 2 处独立佐证（跨域）、能回答书中未明说的新问题（预测力）、不是常识（独特性）
4. **RIA++ 构造**——按 R（原文引用）/ I（用自己的话重写）/ A1（书中案例）/ A2（未来触发场景）/ E（可执行步骤）/ B（边界与盲点）六个维度结构化
5. **Zettelkasten 链接**——找出能力卡之间的依赖、对比、组合关系，生成能力索引与路由表
6. **触发与输出测试**——为每张卡设计触发盲测题（含诱饵题：该触发时要触发，不该触发时要沉默）与输出评测场景，未通过的卡回炉重做，回炉后再做回归验证

本书的流水线留痕：阶段 0 整书理解 → 609 条候选提取 → 三重验证筛出 13 个单元 → 编译为 12 张 RIA++ 能力卡。每张卡的「A股适配」小节是编译者补充，与原书事实严格分节，不混在原文引用里。

## 仓库结构

```text
peter-lynch-invest-skill/
├── README.md                      ← 你正在看的
├── README.en.md                   ← English version
├── LICENSE                        ← MIT
├── single/                        ← 单一入口模式
│   └── peter-lynch-invest-skill/
│       ├── SKILL.md               ← 入口：触发条件 + 路由表 + 加载规则
│       ├── BUILD_MANIFEST.json    ← 编译清单与文件哈希
│       └── references/
│           ├── overview.md        ← 整书概览
│           ├── capability-index.md  ← 完整意图与关键词索引
│           ├── cheatsheet.md      ← 决策规则速查
│           ├── glossary.md        ← 术语表
│           └── capabilities/      ← 12 张能力卡
└── pack/                          ← 多入口模式（compact pack）
    ├── BUILD_MANIFEST.json
    ├── capability-destinations.json
    ├── peter-lynch-invest-skill-router/
    │   ├── SKILL.md               ← 来源路由入口
    │   └── references/            ← 12 张卡 + 索引，供 router 内部调用
    ├── classify-six-types-skill/
    │   └── SKILL.md
    ├── stock-screening-checklists-skill/
    │   └── SKILL.md
    ├── pe-valuation-skill/
    │   └── SKILL.md
    ├── financial-checklist-13-skill/
    │   └── SKILL.md
    ├── analyze-checklist-ch15-skill/
    │   └── SKILL.md
    ├── sell-rules-by-type-skill/
    │   └── SKILL.md
    └── dangerous-sayings-skill/
        └── SKILL.md
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
      classify-six-types-skill \
      stock-screening-checklists-skill \
      pe-valuation-skill \
      financial-checklist-13-skill \
      analyze-checklist-ch15-skill \
      sell-rules-by-type-skill \
      dangerous-sayings-skill ~/.agents/skills/
```

```powershell
# Windows
$pack = ".\peter-lynch-invest-skill\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('peter-lynch-invest-skill-router','classify-six-types-skill','stock-screening-checklists-skill','pe-valuation-skill','financial-checklist-13-skill','analyze-checklist-ch15-skill','sell-rules-by-type-skill','dangerous-sayings-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` 是 DSH 的 skill 目录；用别的 agent 时换成它自己的 skills 目录即可（例如 Claude Code 是 `~/.claude/skills`）。

### 怎么确认装好了

装完问一句"这只票涨了 40%，该不该卖"，看 agent 是否先追问公司属于六类里的哪一类、再套该类判据，而不是直接给你一个"涨 40% 就该走"的通用答案。装的是 single 时，它会先读入口再按路由表进能力卡；装的是 pack 时，`sell-rules-by-type-skill` 会被直接命中。

## 来源

- 《彼得·林奇的成功投资》（One Up on Wall Street），彼得·林奇（Peter Lynch）、约翰·罗瑟查尔德（John Rothchild）著，刘建位、徐晓杰 译，机械工业出版社 2010（原著 1989）
- 全书蒸馏产出 12 张能力卡
- 原书成文于 1988–89 年的美国：案例全部来自 1970–80 年代美国公司，没有一个 A 股案例；纸质年报与电话调研是当时的主要信息渠道，整体市盈率 8 倍的判断产生于高利率时代。本套 skill 以 A 股场景为先，每张能力卡的「A股适配」小节（编译者补充，非原书内容）逐一替换了数据源、科目口径与制度前提
- 一切量化阈值（P/E 基准、增长率区间、持股数量、涨跌百分比）在原书里都是经验归纳，仅作起点参照，须以 A 股数据重校

## 声明

本仓库只发布蒸馏后的 skill、索引与规则速查材料，不包含原书 PDF、EPUB、OCR 文件、截图或全书转写稿。能力卡中出现的原文引用仅用于标注方法论出处和保持可审计性。

书中所有数字判据（增长率区间、P/E 分档、同店销售降幅、持股数量、涨跌兑现区间等）都是案例与经验归纳，原书未提供统计回测背书，使用时需按标的自行测试并声明所用口径。本仓库内容不构成投资建议。

## License

[MIT](https://opensource.org/licenses/MIT)
