# 原则候选 · Part A（导论 + 第一部分 + 第6-10章，L1-2388）

> principle-extractor 产出。覆盖范围：导论（L8-183）、第1-5章（L187-766）、第6章（L772-991）、第7章（L993-1456）、第8章（L1458-1870）、第9章（L1872-2062）、第10章（L2064-2385，含10.1-10.4市盈率规则）。
> id 从 pA01 起；type ∈ principle / checklist / rule / calculation / template；计算类补 inputs / formula / units / output / missing_conditions。不做筛选，原子化拆分。

## 导论（L8-183）

- id: pA01
  title: 第一条投资准则——千万不要听信专业投资者的投资建议
  type: rule
  source_chapter: 导论 · 业余投资者的优势（L10）
  source_quote: |
    "在这本书中我要告诉读者的第一条投资准则是：千万不要听信任何专业投资者的投资建议！"
  summary: |
    作者以专业投资者身份开宗明义：业余投资者只要动用3%的智力自主选股，回报即可超过华尔街专家平均水平。专业投资人并不如想象聪明，业余投资者只在盲目听信专业投资人时才变蠢。
  tags: [rule, amateur-advantage, independence]
  task_ids: [task-12]

- id: pA02
  title: 依靠自己投资时只依赖自己的研究，不理会消息与权威动向
  type: rule
  source_chapter: 导论（L18-20）
  source_quote: |
    "你只依赖于自己的研究分析进行投资决策，而不要理会什么热门消息，不要听证券公司的股票推荐……即使你听说彼得·林奇或者其他权威人士正在购买什么股票也根本不要理会。"
  summary: |
    独立投资的纪律：不听消息、不看荐股、不跟权威。三个理由：①权威可能错（聪明投资者约40%时间表现愚蠢）；②不知其何时改变看法卖出；③你自己身边有更好的信息来源。
  tags: [rule, independence, information-source]
  task_ids: [task-12]

- id: pA03
  title: 10倍股产生于日常生活与工作场所，业余者拥有信息与制度双重优势
  type: principle
  source_chapter: 导论（L22-23、L149-153）
  source_quote: |
    "你日常生活的环境正是你寻找'10倍股'（tenbaggers）的最佳地方……你对这些公司的产品赞不绝口而且钟爱有加。"
  summary: |
    工作场所与购物中心的信息领先华尔街数月至数年；小组合只需找到一只10倍股即可大幅提升整体业绩（错过了大多数也仍有足够多机会）。这是全书选股方法论的地基。
  tags: [principle, amateur-advantage, tenbagger]
  task_ids: [task-12, task-13]

- id: pA04
  title: 一只10倍股足以使整个组合扭亏为盈（表0-1 A/B策略证据）
  type: calculation
  source_chapter: 导论 0.1（L30-63，表0-1 L32-59）
  source_quote: |
    "A投资策略使你投资的10000美元升值到了13040美元……如果你还买了Stop＆Shop股票……总投资收益率会高达110.6%。"
  summary: |
    表0-1证据规则：1980-12-22至1983-10-04，10只股票组合（A策略）总收益+162.7%（同期标普+40.6%），仅3年表现平平30.4%；多买一只涨10倍的Stop&Shop（6→60美元，+900%）后总收益110.6%。结论：对一只股票判断越正确，越可能错判其余股票，但一只大牛股仍足以在总体上战胜市场。
  tags: [calculation, portfolio, evidence-table]
  task_ids: [task-11, task-12]
  inputs: [组合各股买入价, 卖出价, 组合总投入]
  formula: 总收益率 = (期末市值 − 期初投入) / 期初投入 ×100%；单股涨跌幅 = (卖出价 − 买入价) / 买入价
  units: 美元/股；百分比
  output: A策略+30.4% vs 标普+40.6%；B策略（多一只10倍股）+110.6%
  missing_conditions: 表0-1未印"合计"字样的+162.7%行指10股涨跌幅简单加总（非复利组合收益），与30.4%总收益口径不同；原文未注明是否含股息

- id: pA05
  title: 不要投资于你根本不了解的公司股票
  type: rule
  source_chapter: 导论 0.5（L155-161）
  source_quote: |
    "投资者总是远离那些就在自己日常生活中能够近距离观察到的公司的股票，反而费尽心机寻找那些生产的产品让人根本无法了解的公司的股票。"
  summary: |
    华尔街不成文规则恰是反面教材：连描述产品的技术词汇都看不懂（存储器/协议/总线结构等），就应离远点，即使经纪人称是"10年一遇的天赐良机"也不搭理。与8.1.1-8.1.3"枯燥乏味"准则互为正反面。
  tags: [rule, circle-of-competence, negative-screen]
  task_ids: [task-12, task-04]

- id: pA06
  title: 热门产品只是线索——第一步找公司，第二步研究分析
  type: rule
  source_chapter: 导论 0.6（L169）
  source_quote: |
    "找到有发展潜力的公司只是股票投资的第一步，接下来第二步还要仔细进行研究分析。"
  summary: |
    产品畅销本身不构成买入理由（椰菜娃娃未能挽救Coleco破产、Bildner's亏损案例在侧）。必须经研究分辨是玩具反斗城式大牛股还是科尔克式垃圾股，才谈得上投资。
  tags: [rule, research-discipline, product-signal]
  task_ids: [task-13, task-07]

- id: pA07
  title: L'eggs规则——畅销产品不必从第一天发现，全国畅销后1-3年买入仍获至少3倍
  type: principle
  source_chapter: 导论 0.3（L105）
  source_quote: |
    "你并不需要从一开始就知道这个畅销全国的商品，你可以在L'eggs畅销全国之后的第一年、第二年、第三年再买入Hanes公司的股票，无论哪一年购买都会让你获得至少3倍的回报。"
  summary: |
    身边信号的时间窗口比直觉宽得多：发现滞后1-3年仍不迟。对应第2章华尔街滞后性——机构确认往往要等涨幅已大之后，业余者有充足的从容入场时间。
  tags: [principle, timing, product-signal]
  task_ids: [task-13, task-14]

- id: pA08
  title: 试用产品、观察商店=做基本面分析
  type: principle
  source_chapter: 导论 0.4（L151-153）
  source_quote: |
    "购买你所熟悉的公司股票……最大的好处在于，当你试穿丝袜或者品尝咖啡时，你就等于是在做基本面分析。"
  summary: |
    消费行为即调研：参观商店并试用产品本就是证券分析师工作的组成部分。看到周围新开8家连锁店时不必等美林专家推荐（Dunkin's Donuts涨5倍后美林才注意到）。
  tags: [principle, research-method, product-signal]
  task_ids: [task-13, task-08]

## 第1章（L191-285）

- id: pA09
  title: 股票投资是艺术不是科学——小学四年级数学足够
  type: principle
  source_chapter: 第1章（L219）
  source_quote: |
    "股票投资是一门艺术，而不是一门科学……每个投资者在上小学四年级时学会的数学知识对于股票投资来说就已经足够了。"
  summary: |
    拒绝过度量化：习惯严格数量分析的人在投资中反而有劣势（若选股可量化，租台克雷计算机就能赚钱）。逻辑学比统计学更有用——华尔街坐而争论股价而不去调研公司，如同古希腊人争论马有多少牙齿而不去数。
  tags: [principle, anti-quantification, epistemology]
  task_ids: [task-12]

- id: pA10
  title: 看到好生意先问"这是一家上市公司吗"
  type: checklist
  source_chapter: 第1章（L147）、第6章（L788）
  source_quote: |
    "卵石海滩……也是20世纪最牛的隐蔽资产型大牛股。当我站在卵石海滩高尔夫球场的草皮上时……却从来没有想起来问问这是不是一家上市公司。"
  source_note: 第6章同型问题："这种玩意儿是哪家上市公司制造的？"
  summary: |
    把身边观察转化为投资线索的第一步是确认主体可投资。作者自省错过Pebble Beach的教训：信息就在眼前，缺的是提问习惯。
  tags: [checklist, idea-generation, hidden-asset]
  task_ids: [task-13]

- id: pA11
  title: 缅因州制糖教训——不买依赖迟缓外部方实现增长的公司
  type: rule
  source_chapter: 第1章（L261-263）
  source_quote: |
    "我发誓再不购买像缅因州制糖公司这类公司的股票，想要让性子比老牛慢的缅因州农民快速行动起来实现业务增长简直是痴人说梦。"
  summary: |
    商业计划依赖第三方（此处为谨小慎微的农民）快速配合才能兑现增长的公司不可投——执行链条不在公司自己手里的增长故事天然不可靠。
  tags: [rule, negative-screen, execution-risk]
  task_ids: [task-04]

## 第2章（L287-445）

- id: pA12
  title: 用适当怀疑的眼光审视专业投资者
  type: principle
  source_chapter: 第2章（L289）
  source_quote: |
    "对于业余投资者来说，非常重要的一点是要用一种适当怀疑的眼光来审视专业投资人……主要上市公司70%的股票都掌握在机构投资者手中。"
  summary: |
    "专业投资"近乎矛盾修饰语。大多数基金经理人心智平平、从众随大流；极少数特立独行者（坦普尔顿、巴菲特等）是例外。理解对手是业余者的必修课。
  tags: [principle, professional-investor, skepticism]
  task_ids: [task-12]

- id: pA13
  title: 华尔街滞后性（Street lag）——机构等别人先买才买，业余者可提前入场
  type: principle
  source_chapter: 第2章 2.1（L311）
  source_quote: |
    "只有在许多大型机构投资者都认为一只股票适合于购买，并且许多著名的华尔街分析师们将其列入推荐购买的股票名单之后，一只股票才有可能真正地吸引投资者们的目光。"
  summary: |
    体制性时滞案例：The Limited上市(1969)后6年仅1位分析师追踪，1979年仅2家机构持股0.6%，1985年股价15美元时分析师才蜂拥，推到52.875美元后崩跌。SCI上市10年无分析师关注。业余者越早买入，越享受机构涌入前的低价。
  tags: [principle, street-lag, information-advantage]
  task_ids: [task-12, task-03]

- id: pA14
  title: 机构"IBM饭碗逻辑"——宁选确定的平庸，不冒不知名的险
  type: principle
  source_chapter: 第2章 2.1-2.2（L339-341）
  source_quote: |
    "华尔街上有一条不成文的潜规则：'如果你购买是IBM的股票而使客户资金遭受损失，那么你永远不会因此而丢掉你的饭碗。'"
  summary: |
    买IBM跌了客户问"该死的IBM怎么了"；买La Quinta跌了就问"该死的你怎么搞的"。基金经理人因此优先找拒绝买入的理由而非买入理由，被迫晚买大票——这是业余者的结构性机会。
  tags: [principle, institutional-behavior, career-risk]
  task_ids: [task-12]

- id: pA15
  title: 机构双重限额规则——单一公司持股≤总股本10%，单只股票≤基金资产5%
  type: calculation
  source_chapter: 第2章 2.3（L401-411）
  source_quote: |
    "美国证券交易委员会规定，一家共同基金在任何一家上市公司的持股比例不能超过其总股本的10%，而且对于任何一只股票的投资总额也不能超过基金总资产的5%。"
  summary: |
    由此推出：10亿美元养老基金按5%上限至少持20只、按40只名单则每只2500万美元；再叠加市值门槛（如1亿美元）与"4项检验全部合格"式选股名单，机构被迫只买大市值著名公司，系统性放弃小公司10倍股（小票涨3倍过市值门槛后机构才能买）。
  tags: [calculation, institutional-constraint, sec-rule]
  task_ids: [task-12]
  inputs: [基金总资产, 选股名单股票数, 公司总股本与市价]
  formula: 单股投资上限=基金资产×5%；持股上限=总股本×10%；市值=股价×流通股数
  units: 美元；百分比
  output: 机构可投股票池被压缩为大约市值前90-100名公司
  missing_conditions: 市值门槛（如1亿美元）为部分基金的自律规则而非SEC统一规定；A股无同名规则，需另行映射

- id: pA16
  title: 业余投资者的制度优势清单——无名单、无监工、可空仓、数量自定
  type: checklist
  source_chapter: 第2章 2.4（L423-437）
  source_quote: |
    "如果找不到基本面良好、十分具有投资吸引力的股票，业余投资者可以什么股票都不买，然后等着更好的投资机会出现再行动，而证券投资基金管理人员就没有这么奢侈的选择了。"
  summary: |
    四项自由：①不受批准名单与行业禁忌约束；②无人逐季盘问（无弗林特式审查与"掩埋罪证"压力）；③持股数量1只到10只自定（机构被迫持1400只）；④可空仓等待。业余者应顺其自然投资，勿模仿机构。
  tags: [checklist, amateur-advantage, institutional-comparison]
  task_ids: [task-12]

- id: pA17
  title: 业余者在工作与生活半径内发现大牛股，早于分析师数月至数年
  type: principle
  source_chapter: 第2章 2.4（L435）
  source_quote: |
    "业余投资者可能会在你家附近或者自己工作的地方附近寻找到绝佳的投资机会，而且业余投资者发现大牛股往往要早在证券分析师得到信息并把相关公司股票推荐给基金经理人的好几个月甚至好几年之前。"
  summary: |
    与pA03呼应但强调时间提前量（数月至数年）。基金从业人员、供应商、顾客、清洁工都属"已获消息者"——信息分布远早于华尔街反应。
  tags: [principle, information-advantage, timing]
  task_ids: [task-12, task-13]

## 第3章（L447-578）

- id: pA18
  title: 股票长期收益率基准口径——股票9.8%/公司债5%/政府债4.4%/国库券3.4%
  type: calculation
  source_chapter: 第3章 3.2（L485）
  source_quote: |
    "从1927年以来，普通股票的平均年投资收益率为9.8%，而公司债券为5%，政府债券为4.4%，短期国库券为3.4%。"
  summary: |
    股票长期收益一枝独秀的核心数据口径（1927-1987约60年）。股票收益与债券收益差4.8个百分点，经复利放大后差距悬殊（见pA20）。逻辑解释：股东分享公司增长，债主只是资金来源，投资债券永远不可能获得10倍回报。
  tags: [calculation, long-term-return, asset-allocation]
  task_ids: [task-12]
  inputs: [1927年以来各资产类别年投资收益率序列]
  formula: 各资产平均年投资收益率（60年口径）
  units: %/年
  output: 普通股票9.8%；公司债券5%；政府债券4.4%；短期国库券3.4%
  missing_conditions: 原文未说明是否含股息再投资、加权方式（算术/几何平均）及债券利息再投资假设；数据止于1988-89年成书时

- id: pA19
  title: 通胀调整口径——CPI长期3%，股票实际6.8%，国库券实际≈0
  type: calculation
  source_chapter: 第3章 3.2（L487）
  source_quote: |
    "根据消费价格指数（CPI）计算，长期通货膨胀率每年为3%。扣除通货膨胀率后普通股票的实际年投资收益率为6.8%，而……短期国库券……的实际年收益率却几乎是零。"
  summary: |
    名义收益必须扣CPI再比较：股票9.8%−3%=6.8%；国库券3.4%−3%≈0。"最保守明智"的工具实际不保值。
  tags: [calculation, inflation-adjustment, real-return]
  task_ids: [task-12]
  inputs: [名义年收益率, CPI长期通胀率3%]
  formula: 实际收益率 ≈ 名义收益率 − 通胀率
  units: %/年
  output: 股票6.8%；国库券≈0
  missing_conditions: 简化为差值近似而非精确费雪公式；3%为美国长期CPI经验值

- id: pA20
  title: 复利证据表3-1——1000美元60年：股票27.2万 vs 公司债1.76万
  type: calculation
  source_chapter: 第3章 3.2（L491-510，表3-1 L493-508）
  source_quote: |
    "1927年，如果你分别在表3-1中所列的4种金融工具上各投资了1000美元，计算复利并且免税，那么60年后……股票投资收益仍然是公司债券投资收益的15倍，甚至是国库券投资收益的30倍还要多！"
  summary: |
    表3-1口径：国库券7400、政府债券13200、公司债券17600、普通股票272000（美元）。60年间历经崩盘、萧条、战争、衰退，股票仍是债券15倍、国库券30倍以上。前提是像沉睡60年的温克尔一样不因恐慌卖出。
  tags: [calculation, compound-interest, evidence-table]
  task_ids: [task-12]
  inputs: [期初1000美元, 年收益率(9.8%/5%/4.4%/3.4%), 60年]
  formula: 终值 = 1000 × (1+r)^60
  units: 美元
  output: 普通股票272000；公司债券17600；政府债券13200；国库券7400
  missing_conditions: 原文声明"计算复利并且免税"；股票9.8%复利60年理论值高于27.2万，原表为出版数据，未说明是否按指数编制规则折算；A股适用需重算本土口径

- id: pA21
  title: 极高利率环境下长期国库券可战胜股市
  type: principle
  source_chapter: 第3章（L463）
  source_quote: |
    "1980年购买20年期美国国库券的投资者会看到……面值已经上涨了将近1倍……每年得到16%的利息……以相当大的优势战胜股市。"
  summary: |
    时代性规则：长期利率从16%高点回落的历史窗口内，锁定高息国库券跑赢股市且零研究成本。边界：依赖1980年代美国利率环境，不可平移。
  tags: [principle, bond-investing, interest-rate]
  task_ids: [task-12]

- id: pA22
  title: 债券赎回条款规则——想赚利率下降的钱只买不可赎回的长期国库券
  type: rule
  source_chapter: 第3章（L465-467）
  source_quote: |
    "由于很少有公司债券是不可赎回的，因此如果你希望能从利率下降中获利的话，我建议你最好还是购买国库券。"
  summary: |
    可提前赎回的公司债/市政债在利率下降时会被发行人赎回（投资者错失资本利得），利率上升时却不赎回（投资者被套牢）——收益不对称。长期国库券到期前5年内才可赎回，是债权投资首选渠道。
  tags: [rule, bond-investing, call-protection]
  task_ids: [task-12]

- id: pA23
  title: 不存在不容错过的蓝筹股——财富不是永恒不变的
  type: principle
  source_chapter: 第3章 3.3（L520-526）
  source_quote: |
    "没有人能保证大公司不会变成小公司，也根本不存在所谓的不容错过的蓝筹股。"
  summary: |
    证据：RCA被收购价66.50美元与1967年持平、仅比1929年高74%（57年<1%/年）；伯利恒钢铁低于30年前高位；道指原始成分股（棉籽油、皮革等）早已消失。破除"长期持有大公司=安全"迷思。
  tags: [principle, blue-chip-myth, long-term-risk]
  task_ids: [task-10, task-12]

- id: pA24
  title: 即使买对股票，错误的时间与价格也会损失惨重
  type: rule
  source_chapter: 第3章 3.3（L528）
  source_quote: |
    "即使是买对了正确的股票，但如果在错误的时间以错误的价格买入，也会损失惨重……百时美从9美元跌到4美元，Teledyne从11美元跌到3美元，而麦当劳则从15美元跌到4美元。"
  summary: |
    好公司≠好股票：1972-74年大跌中优质公司跌50%-75%。风险主要来自投资方法（买价过高）而非公司本身——为第10章P/E红线与pA25张本。
  tags: [rule, entry-price, risk]
  task_ids: [task-05, task-10]

- id: pA25
  title: 风险取决于投资者的方法，而非公司类型
  type: principle
  source_chapter: 第3章 3.4（L562-566）
  source_quote: |
    "能赚大钱的股票往往来自所谓的高风险类型的公司股票，但是与风险更加相关的是投资者，而不是公司的类型。"
  summary: |
    对照案例：研究充分后买"危险"的联合爱迪生赚6倍，"绝对安全"的休斯敦工业10年不动。风险大小由研究深度与买入方法决定，与公司标签（公用事业=安全）无关。
  tags: [principle, risk-definition, method-risk]
  task_ids: [task-12]

- id: pA26
  title: 60%的股票表现与预期一样，就足以创造骄人业绩
  type: principle
  source_chapter: 第3章 3.4（L560）
  source_quote: |
    "如果我选择的股票中有70%的表现与我预期的一样，我就非常高兴了，如果有60%的表现与我预期的一样，我也会十分感激。只要有60%……就足以在华尔街创造一个骄人的投资业绩纪录了。"
  summary: |
    胜率期望管理：选股不需要全对，容忍错误是常态；配合"一只10倍股定乾坤"（pA04）构成正期望组合观。
  tags: [principle, hit-rate, expectation]
  task_ids: [task-11]

- id: pA27
  title: 梭哈规则——新情况确认胜算则继续持有，局势不利则认输离场
  type: principle
  source_chapter: 第3章 3.4（L556-560）
  source_quote: |
    "只要这些新的情况就像新翻开的牌一样表明你的胜算较大时，你就应该继续持有这些公司的股票，就像你继续持有一把好牌一样。"
  summary: |
    投资是提高胜算的赌博：赢家随新信息（收益提升/出售亏损子公司/开拓新市场）加注或弃牌；输家不管赢面大小都下注祈祷奇迹。持有决策由持续出现的新情况驱动，为第14章"定期重新核查"提供原理。
  tags: [principle, holding-discipline, incremental-information]
  task_ids: [task-09, task-02]

## 第4章（L580-643）

- id: pA28
  title: 入市前自我测试三问——房、钱、素质
  type: checklist
  source_chapter: 第4章（L582）
  source_quote: |
    "开始投资任何股票之前，投资者都应该首先问自己以下三个个人问题：①我有一套房子吗？②我未来需要用钱吗？③我具备股票投资成功所必需的个人素质吗？"
  summary: |
    研究公司财务指标之前先照镜子认识自己；这三问比《华尔街日报》任何信息都重要。三问分别对应pA29/pA30-31/pA32。不能事先确定投资目标与信念者，将在市场最低迷时刻恐慌抛售、成为牺牲品。
  tags: [checklist, self-test, pre-investment]
  task_ids: [task-12]

- id: pA29
  title: 先买房，后买股
  type: rule
  source_chapter: 第4章 4.1（L586）
  source_quote: |
    "在你确实打算要进行任何股票投资之前，应该首先考虑购买一套房子……在99%的情况下购买一套房子是能够赚钱的。"
  summary: |
    买房几乎人人做得不错的投资：杠杆+免税+抗通胀+无逐日报价噪音（无保证金追缴、报纸不登你家房价）；平均持有7年 vs 纽交所87%股票年换手。人们花几个月选房子、几分钟选股票——先修房子这门课再入市。
  tags: [rule, house-first, asset-priority]
  task_ids: [task-12]

- id: pA30
  title: 两三年内要用的钱不入市——短期走势预测≈掷硬币
  type: rule
  source_chapter: 第4章 4.2（L612-614）
  source_quote: |
    "如果你在两三年之内不得不为孩子支付大学学费，那么就不应该把这笔钱用来投资股票……未来两三年内股票的价格是涨还是跌……准确概率可能会与你掷硬币猜正反面的准确概率差不多。"
  summary: |
    时间期限匹配规则：股票未来10-20年走势相对可预测，2-3年随机。有刚性用途（学费/固定生活费）的资金即使是买蓝筹股也太危险。
  tags: [rule, time-horizon, money-in-use]
  task_ids: [task-12]

- id: pA31
  title: 只能投入承受得起的损失——损失发生不影响日常生活
  type: rule
  source_chapter: 第4章 4.2（L616）
  source_quote: |
    "在股票市场的投资资金只能限于你能承受得起的损失数量，即使这笔损失真的发生了，在可以预见的将来也不会对你的日常生活产生任何影响。"
  summary: |
    仓位上限的简单公式（作者称对股票和赌马同样适用）。比任何复杂的资产配置公式都实用：以"全损也不改变生活"为资金准入线。
  tags: [rule, position-sizing, risk-capacity]
  task_ids: [task-12]

- id: pA32
  title: 股票投资成功的个人素质清单（12项）
  type: checklist
  source_chapter: 第4章 4.3（L620）
  source_quote: |
    "耐心、自立、常识、对于痛苦的忍耐力、心胸开阔、超然、坚持不懈、谦逊、灵活、愿意独立研究、能够主动承认错误以及能够在市场普遍性恐慌之中不受影响保持冷静的能力。"
  summary: |
    最优秀投资者智商介于最高3%与最差10%之间——天才沉醉理论反而被现实背叛。配套要求：能在信息不完全、不准确的条件下决策（华尔街的事一旦明朗化为时已晚）。
  tags: [checklist, temperament, self-test]
  task_ids: [task-12]

- id: pA33
  title: 在信息不完全、不充分、不准确的条件下做出决策
  type: principle
  source_chapter: 第4章 4.3（L622）
  source_quote: |
    "要有能力在得到的信息不完全、不充分以及得到的信息不完全准确的情况下做出投资决策……那种需要知道所有数据的科学思维方式在华尔街只会一再受挫。"
  summary: |
    决策时点规则：等待完全信息=放弃机会。与pA09（艺术非科学）互证。
  tags: [principle, decision-under-uncertainty]
  task_ids: [task-12]

- id: pA34
  title: 只要公司基本面没有根本变化，就一直持有；约束自己不理会内心感觉
  type: rule
  source_chapter: 第4章 4.3（L640）
  source_quote: |
    "投资的窍门不是要学会相信自己内心的感觉，而是要约束自己不去理会内心的感觉。只要公司的基本面没有什么根本的变化，就一直持有你手中的股票。"
  summary: |
    持有纪律总纲：投资者在担心害怕-洋洋自得-灰心丧气间循环，恰在高点乐观低点恐慌（时事通讯情绪调查反向印证：1972年底仅15%看熊、1982年大牛前55%看熊、1987年崩盘前80%看牛）。听到有人预测市场时"最重要的技巧是打起呼噜睡大觉"。
  tags: [rule, holding-discipline, emotion-control]
  task_ids: [task-09, task-02, task-10]

- id: pA35
  title: 真正的逆向投资——等热情冷却后买被厌倦的公司，而非与热门股对着干
  type: principle
  source_chapter: 第4章 4.3（L638）
  source_quote: |
    "真正的逆向投资者并不是那种与人人追捧的热门股对着干的投资者……会耐心等待市场热情冷却下来，然后再去买入那些不再被人关注的公司股票，特别是那些让华尔街感到厌倦无聊的公司股票。"
  summary: |
    伪逆向=逆向已成流行观点时才逆向。真逆向=时间上等冷却+标的上选冷门。与第8章"枯燥乏味"准则同源。
  tags: [principle, contrarian, definition]
  task_ids: [task-04, task-03, task-10]

## 第5章（L645-766）

- id: pA36
  title: 不要预测股市——预测经济与短期走势都没有用
  type: principle
  source_chapter: 第5章（L648-666）
  source_quote: |
    "投资者并不需要具备预测市场的能力照样可以在股市上赚钱，如果不是这样的话，那么我就应该一分钱也赚不到。"
  summary: |
    证据链：6万名经济学家无人连续预测成功；1973-74、1987两次崩盘事前无人警告；"衰退结束的铃声从来不会响起"。正确预测行业仍可能选错股票（钢铁复苏中LTV跌96%而Nucor涨5倍）——即使能预测宏观，选股功夫一样不能省。
  tags: [principle, no-forecasting, market-timing]
  task_ids: [task-12, task-14]

- id: pA37
  title: 为历史重演做准备无济于事——玛雅寓言
  type: principle
  source_chapter: 第5章 5.1（L670-684）
  source_quote: |
    "下一次的情况永远不会和上一次的一模一样，因此我们根本不可能为下一次的情况事先做好任何准备。"
  summary: |
    玛雅人防洪水后遇火灾、防火灾后遇地震。投资者总在为"上次灾难"做准备（石油5美元/100美元恐惧交替），而下次冲击必然以新形态出现。用于解毒"这次学会了"的过度自信。
  tags: [principle, no-forecasting, black-swan]
  task_ids: [task-10, task-14]

- id: pA38
  title: 鸡尾酒会理论——市场情绪四阶段自测
  type: template
  source_chapter: 第5章 5.2（L688-698）
  source_quote: |
    "当邻居们告诉我该买哪只股票，而且后来股价上涨后我非常后悔没有听从他们的建议时，这是一个股市已经上涨到了最高点而将要下跌的准确信号。"
  summary: |
    四阶段：①无人理基金人（只跟牙医聊牙斑）→市场将止跌反弹；②停留稍长仍聊牙斑→已涨15%；③整晚被围着问买什么→已涨30%；④牙医反过来荐股→见顶信号。边界：作者自嘲"可随意参考，不要指望我拿它打赌"——是情绪温度计而非交易系统。
  tags: [template, sentiment-indicator, cocktail-party]
  task_ids: [task-14]

- id: pA39
  title: 唯一的买入信号——找到一家自己喜欢的上市公司
  type: rule
  source_chapter: 第5章 5.3（L724）
  source_quote: |
    "我所需要的唯一买入信号就是找到一家我喜欢的上市公司，在这种情况下买入股票永远不会太早也不会太迟。"
  summary: |
    时机观收口：不问大盘点位，问"是否找到合理定价的好公司"。找不到符合标准的股票这件事本身就是市场被高估的信号（巴菲特1969退款给合伙人的理由）。
  tags: [rule, buy-signal, company-first]
  task_ids: [task-14, task-03]

- id: pA40
  title: 投资的是公司，而不是股市（巴菲特口径）
  type: principle
  source_chapter: 第5章 5.3（L706）
  source_quote: |
    "巴菲特曾这样写道：'股票市场根本不在我所关心的范围之内。股票市场的存在只不过是提供一个参考，看看是不是有人报出错误的买卖价格做傻事。'"
  summary: |
    "市场应该与投资无关"；担心西点-佩珀瑞尔的床单生意、Taco Bell的新品销量，而不是指数涨跌——"股市自己会照顾自己"。全书心态基石。
  tags: [principle, company-first, buffett-quote]
  task_ids: [task-12]

### 第5章5.4节"本部分要点"16条（L726-758，逐条收录）

- id: pA41
  title: 要点1——不要过高估计专业投资者的技巧和智慧
  type: principle
  source_chapter: 第5章 5.4（L728）
  source_quote: "·不要过高估计专业投资者的技巧和智慧。"
  summary: 第一部分要点清单第1条；与pA01/pA12/pA14互证。
  tags: [principle, part1-summary, professional-investor]
  task_ids: [task-12]

- id: pA42
  title: 要点2——充分利用你已经知道的信息和知识
  type: principle
  source_chapter: 第5章 5.4（L730）
  source_quote: "·充分利用你已经知道的信息和知识。"
  summary: 要点清单第2条；身边信息优势的行动化表述，与pA03/pA08互证。
  tags: [principle, part1-summary, information-advantage]
  task_ids: [task-12, task-13]

- id: pA43
  title: 要点3——寻找尚未被华尔街发现和证实的投资机会（雷达监测范围之外）
  type: principle
  source_chapter: 第5章 5.4（L732）
  source_quote: "·寻找那些尚未被华尔街发现和证实的投资机会——在华尔街'雷达监测范围之外'的公司。"
  summary: 要点清单第3条；滞后性（pA13）的正向操作版，是第8章13条准则的共同本质。
  tags: [principle, part1-summary, street-lag]
  task_ids: [task-03, task-12]

- id: pA44
  title: 要点4——在投资股票之前先买一套房子
  type: rule
  source_chapter: 第5章 5.4（L734）
  source_quote: "·在投资股票之前先买一套房子。"
  summary: 要点清单第4条；pA29的清单化复述。
  tags: [rule, part1-summary, house-first]
  task_ids: [task-12]

- id: pA45
  title: 要点5——投资的是公司，而不是股市
  type: principle
  source_chapter: 第5章 5.4（L736）
  source_quote: "·投资的是公司，而不是股市。"
  summary: 要点清单第5条；pA40的清单化复述。
  tags: [principle, part1-summary, company-first]
  task_ids: [task-12]

- id: pA46
  title: 要点6——忽略股市的短期波动
  type: rule
  source_chapter: 第5章 5.4（L738）
  source_quote: "·忽略股市的短期波动。"
  summary: 要点清单第6条；与pA34持有纪律、pA36不预测互证。
  tags: [rule, part1-summary, volatility]
  task_ids: [task-12, task-10]

- id: pA47
  title: 要点7——投资股票能够赚大钱
  type: principle
  source_chapter: 第5章 5.4（L740）
  source_quote: "·投资股票能够赚大钱。"
  summary: 要点清单第7条；数据支撑见pA18-20（9.8%长期收益、27.2万复利终值）。
  tags: [principle, part1-summary, long-term-return]
  task_ids: [task-12]

- id: pA48
  title: 要点8——投资股票也能够亏大钱
  type: principle
  source_chapter: 第5章 5.4（L742）
  source_quote: "·投资股票也能够亏大钱。"
  summary: 要点清单第8条；与pA24（好公司错价买入也巨亏）、pA23（蓝筹消亡）互证，构成对称风险观。
  tags: [principle, part1-summary, risk]
  task_ids: [task-12, task-10]

- id: pA49
  title: 要点9——预测经济是没有用的
  type: principle
  source_chapter: 第5章 5.4（L744）
  source_quote: "·预测经济是没有用的。"
  summary: 要点清单第9条；pA36的清单化复述（6万经济学家无人连续预测成功）。
  tags: [principle, part1-summary, no-forecasting]
  task_ids: [task-12, task-14]

- id: pA50
  title: 要点10——预测股市的短期走势是没有用的
  type: principle
  source_chapter: 第5章 5.4（L746）
  source_quote: "·预测股市的短期走势是没有用的。"
  summary: 要点清单第10条；与pA30（2-3年预测≈掷硬币）互证。
  tags: [principle, part1-summary, no-forecasting]
  task_ids: [task-12, task-14]

- id: pA51
  title: 要点11——股票的长期回报相对可预测，且远高于长期债券
  type: principle
  source_chapter: 第5章 5.4（L748）
  source_quote: "·股票的长期回报相对而言是可以预测的，而且远远高于长期债券的投资回报。"
  summary: 要点清单第11条；期限结构规则：长期可预测（pA30）+收益占优（pA18-20），二者合并。
  tags: [principle, part1-summary, long-term-return]
  task_ids: [task-12]

- id: pA52
  title: 要点12——持续关注所持股票的公司情况，像玩一局永不结束的梭哈
  type: principle
  source_chapter: 第5章 5.4（L750）
  source_quote: "·持续关注你所持有股票的公司情况，就像是在玩一局永远不会结束的梭哈扑克牌游戏。"
  summary: 要点清单第12条；pA27梭哈规则的清单化复述，指向第14章定期重新核查。
  tags: [principle, part1-summary, monitoring]
  task_ids: [task-09]

- id: pA53
  title: 要点13——并非每个人都适合股票投资，也并非每个阶段都适合
  type: principle
  source_chapter: 第5章 5.4（L752）
  source_quote: "·并不是每个人都适合于股票投资，也并不是每个人一生中的每个阶段都适合于股票投资。"
  summary: 要点清单第13条；入市资格的否定性结论，指向第4章三问（pA28）与"也许你根本不应该与股票市场沾边儿"（L437）。
  tags: [principle, part1-summary, suitability]
  task_ids: [task-12]

- id: pA54
  title: 要点14——业余投资者早在专业投资者数年之前已了解当地优秀公司
  type: principle
  source_chapter: 第5章 5.4（L754）
  source_quote: "·一般业余投资者早在专业投资者数年之前，就已经十分了解当地优秀的上市公司及其产品了。"
  summary: 要点清单第14条；pA17的清单化复述。
  tags: [principle, part1-summary, information-advantage]
  task_ids: [task-12, task-13]

- id: pA55
  title: 要点15——拥有一种与众不同的优势将会帮助你在股票上赚钱
  type: principle
  source_chapter: 第5章 5.4（L756）
  source_quote: "·拥有一种与众不同的优势将会帮助你在股票上赚钱。"
  summary: 要点清单第15条；优势可以是行业专业优势或消费者体验优势（第6章展开），无优势者胜算小。
  tags: [principle, part1-summary, edge]
  task_ids: [task-12, task-13]

- id: pA56
  title: 要点16——一鸟在手胜过十鸟在林
  type: principle
  source_chapter: 第5章 5.4（L758）
  source_quote: "·在股票市场上，一鸟在手胜过十鸟在林。"
  summary: 要点清单第16条（收尾格言）：确定性收益优于远期许诺，呼应稳定增长型的配置价值与对"故事股"（第9章小声耳语）的排斥。
  tags: [principle, part1-summary, maxim]
  task_ids: [task-12]

## 第6章（L772-991）

- id: pA57
  title: 寻找10倍股的最佳顺序——家附近→购物中心→工作的地方
  type: principle
  source_chapter: 第6章（L774）
  source_quote: |
    "寻找10倍股的最佳地方就是从你家附近开始：在那里找不到，就到大型购物中心去找，特别是到工作的地方去找。"
  summary: |
    线索搜索的优先级地图。商业链上每个角色（制造、销售、清洁、分析，乃至拖地清洁工）都会先于华尔街碰到信号：员工看到保险涨价→保险业好转；承包商看到水泥价格走稳→水泥供应商利好。
  tags: [principle, idea-generation, proximity]
  task_ids: [task-13]

- id: pA58
  title: 一年有两三次碰上很有希望的投资机会
  type: principle
  source_chapter: 第6章（L776）
  source_quote: |
    "一般来说，投资者一年中会有两三次碰上很有希望获得成功的投资机会，有时机会可能更多。"
  summary: |
    机会频率的预期校准：好机会常遇而非稀缺，无须因怕错过而降低标准（配合pA39"唯一买入信号"使用）。
  tags: [principle, opportunity-frequency, patience]
  task_ids: [task-13]

- id: pA59
  title: 两种投资优势——行业专家优势与消费者优势，作用场景不同
  type: principle
  source_chapter: 第6章 6.2（L866-884）
  source_quote: |
    "专业优势特别有助于确定是否买入那些业务已经恢复过来一段时间的公司，尤其是那些处于所谓的周期性行业中的公司的股票……作为消费者在选股上的优势是其消费经验十分有助于选择成立不久的新公司，规模较小的、发展很快的公司股票。"
  summary: |
    行业专家优势（化工人见PVC需求涨价库存下降）→判断周期复苏；消费者优势（店员、顾客见排队长龙）→发现新小快公司，尤其零售。两优势可各自发展独立于华尔街渠道的自选股系统。
  tags: [principle, edge, classification-of-advantage]
  task_ids: [task-13, task-01]

- id: pA60
  title: 草根观察者领先专职分析师6-12个月发现行业好转
  type: calculation
  source_chapter: 第6章 6.2（L876）
  source_quote: |
    "在大多数其他行业，在基层工作的草根观察人士能够比专职的金融分析师提前6～12个月的时间发现这些行业经营突然好转的信息。"
  summary: |
    优势的时间量化：基层从业者提前6-12个月发现供给短缺/价格涨跌/需求增减（汽车等被华尔街紧盯的行业除外，其销售数据十天公布一次无优势）。盈利上涨相应推动股价。
  tags: [calculation, edge, time-lead]
  task_ids: [task-13]
  inputs: [行业基层供需信号(价格/库存/订单/新竞争者), 华尔街分析师覆盖密度]
  formula: 草根信息领先时间 ≈ 6-12个月（非汽车等高频公布行业）
  units: 月
  output: 业余者可先于机构在盈利好转兑现前布局
  missing_conditions: 1980年代美国信息环境下的经验值；现代信息传播下窗口已收窄（见BOOK_OVERVIEW批判节）

- id: pA61
  title: 在自己有优势的行业投资胜算更大——外行是最后知道变化的人
  type: rule
  source_chapter: 第6章 6.1（L858-864）
  source_quote: |
    "一个在某一行业拥有优势的人总是比没有优势的人在这一行业进行股票投资的胜算更大——毕竟在行业上没有优势的人是最后一个知道这一行业发生重大变化的人。"
  summary: |
    医生买医药股、石油专家买Schlumberger各得其所；买自己一无所知的行业=给自己加不必要的障碍（马拉松选手去比雪橇）。反例：石油员工靠经纪人买史克必成，泰胃美被竞品替代致股价跌40%时他"最后一个明白"。
  tags: [rule, circle-of-competence, edge]
  task_ids: [task-12, task-13]

- id: pA62
  title: 隐蔽资产筛选规则——每股资产价值超过每股市场价格才值得买
  type: calculation
  source_chapter: 第6章 6.2（L880-882）
  source_quote: |
    "你所寻找的是具有以下特征的公司股票：每股股票的资产价值超过了每股股票的市场价格。在这种让人高兴的情况下，你真的可以不花一分钱就能买到一大笔价值不菲的资产。"
  summary: |
    Storer实例：业内人士可算出电视台+有线网络真实资产价值≈每股100美元，股价仅30美元（1985年以93.50美元被私有化收购）。计算口径：隐蔽资产每股价值 − 股价 = 免费获得的剩余价值（Liberty公司例：电视台30美元−股价30美元=保险公司白送）。
  tags: [calculation, hidden-asset, screening]
  task_ids: [task-06, task-01, task-13]
  inputs: [公司隐蔽资产重估值(电视台/土地/金属/专利等), 流通股数, 当前股价]
  formula: 每股隐蔽资产价值 = 隐蔽资产重估值 ÷ 流通股数；筛选条件：每股资产价值 > 股价
  units: 美元/股
  output: 资产折扣（股价相对资产价值的折价），折价越深安全边际越大
  missing_conditions: 资产"华尔街未注意到"是前提（若已定价则不成立）；重估方法（可比交易/重置成本）原文未给统一口径

- id: pA63
  title: 对投资者最好的药品是需不断重复购买的常用药
  type: principle
  source_chapter: 第6章 6.1（L806）
  source_quote: |
    "对病人来说最好的药品是那种能够一次治愈药到病除的良药，而对投资者来说最好的药品则是那种病人需要不断地购买服用的常用药。"
  summary: |
    泰胃美（需持续服用的胃溃疡药）推动史克必成10年7.5→72美元。重复购买属性使收入可累积、可预测——与8.1.10"人们要不断购买公司的产品"同一条原则的医药版。
  tags: [principle, repeat-purchase, moat]
  task_ids: [task-03, task-13]

## 第7章（L993-1456）

- id: pA64
  title: 最初的信息只是故事的开头——绝不当买入信号
  type: rule
  source_chapter: 第7章（L995-997）
  source_quote: |
    "你都不应该将这种发现看做是一个股票买入信号……到此时为止你所了解的信息只不过是一个需要进一步展开的故事的开头而已。"
  summary: |
    无论线索来自办公室、购物中心还是岳母/名人，都视作"匿名却让人感兴趣的消息"，先研究后行动。研究一家公司"最多不过花几个小时"——不做研究就投资如同不看牌玩梭哈（L1001）。反例：夫妇找伦敦机票花一周末，买500股KLM研究不到5分钟（L1003）。
  tags: [rule, research-discipline, product-signal]
  task_ids: [task-13, task-07]

- id: pA65
  title: 全面研究一家公司最多花几个小时
  type: rule
  source_chapter: 第7章（L999-1001）
  source_quote: |
    "就像一步步弄清一个故事的情节一样，全面深入研究一家公司真的一点也不难，最多不过是花上几个小时而已。"
  summary: |
    研究成本预期管理：以"几个小时"为单位即可完成买入前功课，破除"股票分析神秘高深"的心理障碍；治"愿花几小时比卫生纸却不读年报"的投资综合症（L1009）。
  tags: [rule, research-discipline, effort-budget]
  task_ids: [task-07, task-08]

- id: pA66
  title: 产品热门信号必测——该产品成功对公司净利润影响多大（帮宝适谬误）
  type: calculation
  source_chapter: 第7章 7.1（L1013-1023）
  source_quote: |
    "如果你由于一家公司生产的某一种产品很受欢迎而考虑购买它的股票，那么你首先要弄清楚的第一个问题是：这种产品的成功对于这家公司的净利润影响程度有多大？"
  summary: |
    帮宝适仅占宝洁收入一小部分 vs L'eggs对Hanes举足轻重——同为畅销品，母公司受益天差地别。对照案例：Retin-A上年销售3000万美元（两天涨8美元、市值增14亿美元，追涨者忘乎所以）vs Bufferin国内销售7500万美元不足百时美总收入53亿的1.5%（股价只涨50美分）；Sterling的阿司匹林占收入6.5%却占总利润近15%——必须同时算收入占比与利润占比。
  tags: [calculation, product-signal, net-profit-attribution]
  task_ids: [task-13]
  inputs: [该产品年销售收入, 公司总收入, 该产品利润或利润率, 公司总利润]
  formula: 收入占比 = 产品收入 ÷ 总收入；利润占比 = 产品利润 ÷ 总利润
  units: 百分比
  output: 判断"产品热"能否传导为"利润增"：占比<2%可忽略（Bufferin 1.5%例），占比高（Sterling 15%）才是主驱动
  missing_conditions: 分产品利润数据常不直接披露，需以收入占比+利润率差异估算；原文以"5分钟研究"为可行性标准

- id: pA67
  title: 公司越大，涨幅越小
  type: rule
  source_chapter: 第7章 7.2（L1025-1039）
  source_quote: |
    "只有投资于规模较小的公司股票才有可能获得涨幅最大的投资收益……在其他条件都一样的情况下，购买小公司的股票可以获得更好的回报。"
  summary: |
    可口可乐别指望两年涨4倍；通用电气市值≈GNP的1%、9亿股流通，除非"收购全世界"否则无法快速增长。例外：大公司陷入绝望困境后恢复（克莱斯勒、伯林顿北方6→70美元）属困境反转型。同业对照：Pic 'N' Save胜西尔斯、Nucor胜USX、史克必成胜美国家居产品。
  tags: [rule, size-effect, return-expectation]
  task_ids: [task-01, task-13]

- id: pA68
  title: 六类公司分类框架——判定口径与增长率数值
  type: template
  source_chapter: 第7章 7.3（L1043-1051）
  source_quote: |
    "接下来我就要确定这家公司属于6种公司基本类型中的哪一种类型：缓慢增长型、稳定增长型、快速增长型、周期型、隐蔽资产型以及困境反转型……这6个基本类型完全可以涵盖投资者进行的所有有效分类。"
  summary: |
    全书中枢模板。判定顺序：先定规模大小（相对同行），再归六类。增长类三分支以增长率划分（与GNP对照）：缓慢增长≈GNP增速（美国约3%）、稳定增长10-12%、快速增长20-25%甚至更高；周期看收益形态而非增速；困境反转与隐蔽资产按状态判定。类型决定期望收益、核查重点与卖出判据（第17章）。
  tags: [template, six-categories, classification]
  task_ids: [task-01, task-02, task-08]

- id: pA69
  title: 缓慢增长型——≈GNP增速3%、定期慷慨股息、增长2-4%者不值得持有
  type: rule
  source_chapter: 第7章 7.3.1（L1053-1063、L1144-1148）
  source_quote: |
    "缓慢增长型公司的增长速度非常缓慢，大致与一个国家国民生产总值（GNP）的增长速度相符，接近于最近美国国民生产总值年平均增长速度约3%……在我的投资组合中很难找到增长率为2%～4%的公司。"
  summary: |
    特征：规模巨大历史悠久（典型=电力公用事业）、走势图如"特拉华州平地"、定期慷慨支付股息（想不出扩张方法时才付高息）。既然盈利增长才能推动股价，浪费时间在2-4%增长公司上没有意义。风行行业早晚变缓慢增长（铝业/铁路/钢铁/化工/计算机）。
  tags: [rule, slow-grow, dividend, gnp-benchmark]
  task_ids: [task-01, task-08]

- id: pA70
  title: 稳定增长型——年增10-12%、涨30-50%即卖出换入、组合防衰退保护仓
  type: rule
  source_chapter: 第7章 7.3.2（L1152、L1196-1204）
  source_quote: |
    "这种类型公司盈利的年均增长率为10%～12%……在我购买了稳定增长型股票后，如果它的股价上涨到30%～50%，我就会把它们卖掉，然后再选择那些相似的价格还没有上涨的稳定增长型股票反复进行同样的投资操作。"
  summary: |
    可口可乐/百时美/宝洁类数十亿美元市值巨无霸。收益规则：①10-12%年增长；②涨30-50%就卖、轮动到未涨的同型股；③组合中永远保留一批作衰退期保护（1981-82年百时美逆市上涨；Kellogg 30年无季度下滑）。从这类股票获10倍回报十分罕见。
  tags: [rule, stable-grow, sell-rule, defensive]
  task_ids: [task-01, task-02, task-11]

- id: pA71
  title: 听到"涨了2-3倍"先问"持有了多长时间"
  type: rule
  source_chapter: 第7章 7.3.2（L1198）
  source_quote: |
    "当一个人鼓吹说他因为购买稳定增长型公司的股票……上涨了2倍或者3倍时，你接下来应该问的问题是：'你这只股票持有了多长时间？'"
  summary: |
    收益必须年化审视：25年4倍（宝洁1963年起）≈债券收益，承担股票风险却未获股票回报。时间维度是评估一切"赚了N倍"故事的必问变量。
  tags: [rule, annualized-return, interrogation]
  task_ids: [task-02, task-10]

- id: pA72
  title: 稳定增长股一两年内涨50%就要怀疑涨够了，开始考虑卖出
  type: rule
  source_chapter: 第7章 7.3.2（L1200）
  source_quote: |
    "如果你拥有像百时美公司这样的稳定增长型股票，并且一两年内该股票上涨了50%，你就要怀疑这只股票是否已经上涨得足够高了，并且你得开始考虑要不要把它卖掉了。"
  summary: |
    类型化止盈规则：正常情况下两年50%已属满意回报（高露洁例），除非已知有"令人震惊的新发展"，否则不应对稳定增长股抱百万富翁幻想。
  tags: [rule, stable-grow, sell-rule]
  task_ids: [task-02]

- id: pA73
  title: 快速增长型——规模小、新成立、年增20-25%，10-40倍甚至200倍大牛股之源
  type: principle
  source_chapter: 第7章 7.3.3（L1270-1284）
  source_quote: |
    "快速增长型公司是我最喜欢的股票类型之一：规模小、新成立不久、成长性强、年平均增长率为20%～25%。如果你能够明智地选择，你就会从中发现能够上涨10～40倍甚至200倍的大牛股。"
  summary: |
    小组合找一两只需即大幅提升业绩。风险：头脑过热而财务实力不足的新公司易按破产法11章破产；增长放缓后华尔街绝不心慈手软；规模过大后进退两难（格列佛困境）。选择标准：资产负债表良好+实实在在的丰厚利润（pA76）。
  tags: [principle, fast-grow, twentybagger]
  task_ids: [task-01, task-03]

- id: pA74
  title: 更爱缓慢增长行业中的快速增长公司——抢占份额而非行业红利
  type: principle
  source_chapter: 第7章 7.3.3（L1272-1274）
  source_quote: |
    "快速增长型公司并不一定属于快速增长型行业。事实上我更钟爱不属于快速增长型行业的快速增长型公司……在缓慢增长型行业中，快速增长型公司只需一个能够让其不断增长的市场空间照样能够快速增长。"
  summary: |
    啤酒业慢增而Anheuser-Busch靠抢份额快增；酒店业年增2%而万豪10年平均20%；同理Taco Bell（快餐）、沃尔玛（百货）、The Gap（服装）。模式=一地成功后不断复制扩张。与第9章热门行业陷阱（pA105-106）构成镜像。
  tags: [principle, fast-grow, market-share, slow-industry]
  task_ids: [task-01, task-03]

- id: pA75
  title: 快速增长股投资诀窍——弄清增长期何时结束+该付多少买价
  type: rule
  source_chapter: 第7章 7.3.3（L1284）
  source_quote: |
    "投资快速增长型公司股票的诀窍是弄清楚它们的增长期什么时候会结束以及为了分享快速增长型公司的增长所付出的买入价格应该是多少。"
  summary: |
    两大核心问题前置：增长终点的判断（扩张空间、同店/复制速度）与买入价格（联动第10章P/E口径）。只要增速保持，这类股票一直是股市大赢家。
  tags: [rule, fast-grow, exit-anticipation, valuation]
  task_ids: [task-02, task-05]

- id: pA76
  title: 快速增长型筛选标准——资产负债表良好+实实在在的丰厚利润
  type: checklist
  source_chapter: 第7章 7.3.3（L1284）
  source_quote: |
    "我所寻找的是那种资产负债表良好又有着实实在在的丰厚利润的快速增长型公司。"
  summary: |
    双条件防"头脑过热而财务实力不足"的新公司（此类最易破产）。与13项财务指标核查（第13章）衔接。
  tags: [checklist, fast-grow, balance-sheet, quality]
  task_ids: [task-03, task-06]

- id: pA77
  title: 周期型——扩张收缩循环、时机选择是关键、须识别早期迹象
  type: rule
  source_chapter: 第7章 7.3.4（L1288-1354）
  source_quote: |
    "时机选择是投资周期型公司股票的关键，你必须能够发现公司业务衰退或者繁荣的早期迹象。"
  summary: |
    定义：销售收入和盈利以并非完全可预测却相当有规律的方式涨跌（汽车/航空/轮胎/钢铁/化工/国防）。繁荣时上涨比稳定增长快，衰退时痛苦深重；错误周期阶段买入会亏一半以上且等数年。对周期股"选择时机是最重要的"（图7-5点评）。
  tags: [rule, cyclical, timing]
  task_ids: [task-01, task-02]

- id: pA78
  title: 周期股最易被误解为安全蓝筹——衰退中市值可跌80%
  type: rule
  source_chapter: 第7章 7.3.4（L1352）
  source_quote: |
    "在股市不景气或者国民经济衰退时，如果像百时美这样的稳定增长型公司市值损失50%的话，那么像福特这样的周期型公司市值损失则会高达80%。"
  summary: |
    大型著名周期公司（福特是蓝筹）易被误当稳定增长型持有。判定差异看收益形态：福特交替性大盈大亏（1980-83年最深12个月每股亏损3.21美元），百时美20年仅一个季度下滑。混同二者=类型错误的第一大来源。
  tags: [rule, cyclical, misclassification-risk]
  task_ids: [task-01, task-10]

- id: pA79
  title: 相关行业在职者是周期股投资的特殊优势人群
  type: principle
  source_chapter: 第7章 7.3.4（L1354）、6.2（L870-874）
  source_quote: |
    "如果你在与钢铁、铝业、航空、汽车等有关的行业中工作，那么你已经具备了投资周期型公司股票的特殊优势，与其他任何类型的股票投资相比，这种特殊优势在周期型股票投资中尤其重要。"
  summary: |
    化工人先见PVC需求增/价格涨/库存减、新厂兴建（建成要两三年）；轮胎店主见订单回暖即固特异业绩信号。周期股的时机判断最依赖基层一手信息，故行业优势在此类投资中价值最大。
  tags: [principle, cyclical, edge, industry-insight]
  task_ids: [task-01, task-13]

- id: pA80
  title: 困境反转定义——已受致命打击、几乎要按破产法11章申请保护
  type: principle
  source_chapter: 第7章 7.3.5（L1358-1362）
  source_quote: |
    "困境反转型公司是那种已经受到严重打击而一蹶不振并且几乎要按照《破产法》第11章条款的规定申请破产保护的公司……它们不是业务将会复苏的周期型公司，它们有着可能导致公司灭亡的致命伤。"
  summary: |
    与周期复苏严格区分：克莱斯勒由周期公司跌成困境反转、重组后又变回周期公司。优点：股价收复失地非常迅速；在所有类型中与股市大盘涨跌关联程度最小（1982年克莱斯勒6美元买入5年15倍；洛克希德1977年4美元→1986年60美元）。
  tags: [principle, turnaround, definition, low-correlation]
  task_ids: [task-01, task-11]

- id: pA81
  title: 困境反转五子型清单
  type: checklist
  source_chapter: 第7章 7.3.5（L1374-1384）
  source_quote: |
    "一种是'出资挽救我们否则后果自负'类型……还有一种是'谁会想到'类型……还有一种'问题没有我们预料的那么严重'类型……还有一种'破产母公司中含有经营良好的子公司'类型……还有一种叫做'进行重整使股东价值最大化'类型。"
  summary: |
    ①政府救助型（bail-us-out-or-else：克莱斯勒、洛克希德，依赖政府贷款担保）；②谁会想到型（who-would-have-thunk-it：Con Edison 3→52美元）；③问题没想的那么严重型（三哩岛GPU：1985年重启反应堆+他方分摊治污成本为利好买入信号，7年低价窗口）；④破产母公司中的好子公司（玩具反斗城从州际百货分拆后涨57倍）；⑤重整使股东价值最大化型（佩恩中央：剥离多元恶化子公司）。
  tags: [checklist, turnaround, five-subtypes]
  task_ids: [task-01, task-08]

- id: pA82
  title: 避开悲剧后果难以估量的公司
  type: rule
  source_chapter: 第7章 7.3.5（L1380）
  source_quote: |
    "我尽量避开那些悲剧后果难以估量的公司股票……我购买了Johns-Manville的股票，但我发现根本无法估计这家公司承担的赔偿义务总金额到底有多少，于是我就忍痛赔了些小钱把这只股票给卖掉了。"
  summary: |
    责任敞口无法计算的悲剧（博帕尔毒气泄漏的Union Carbide、石棉赔偿的Johns-Manville）不可投——赔了小钱也要卖。困境反转的前提是损失可测算。
  tags: [rule, turnaround, unquantifiable-liability, negative-screen]
  task_ids: [task-04, task-01]

- id: pA83
  title: 隐蔽资产型定义与资产类型清单
  type: checklist
  source_chapter: 第7章 7.3.6（L1390-1404）
  source_quote: |
    "隐蔽资产型公司（the asset play）是指任何一家拥有你注意到了而华尔街投资大众却没有注意到的价值非同一般的资产的公司……这种隐蔽资产可能十分简单，只是一大堆现金，有时隐蔽资产则是房地产。"
  summary: |
    资产类型清单：现金、房地产（Pebble Beach石料场一项3000万美元>整个公司市值2500万；Newhall牧场；Alico土地每股<20美元买入而10年后土地价值200+美元）、铁路土地及采矿伐木权、金属、石油、报纸、专利药品、电视台（Liberty）、税收亏损抵扣（佩恩中央50%免税优势）、债务中隐藏的价值。投资机会随处可见，需对资产有实际了解+耐心等待（L1418）。
  tags: [checklist, hidden-asset, asset-types]
  task_ids: [task-01, task-06, task-08]

- id: pA84
  title: 公司类型随生命周期迁移——分析时必须重新判定当前类型
  type: principle
  source_chapter: 第7章 7.4（L1420-1432）
  source_quote: |
    "一家公司不可能永远属于某一种固定的类型……快速增长型公司不可能永远保持两位数的增长率，早晚它们的增长动力会被耗尽，然后变成增长率只有个位数的缓慢增长型或稳定增长型公司。"
  summary: |
    迁移路径：快速增长→缓慢/稳定（陶氏、坦帕电气）；快速增长→周期（AMD、德州仪器）；周期↔困境反转（克莱斯勒、LTV）；快速增长→困境反转→隐蔽资产（假日酒店；麦当劳未来可能因房地产成隐蔽资产型）；迪士尼曾历经四类。Inco案例：1970年高增长卖出→1982年8美元困境反转买回。持有期须随类型重判预期与卖点。
  tags: [principle, category-migration, lifecycle, re-classification]
  task_ids: [task-01, task-09]

- id: pA85
  title: 不同类型股票必须区别对待——绝无普遍适用的法则
  type: rule
  source_chapter: 第7章 7.5（L1434-1442）
  source_quote: |
    "把你的投资策略建立在一些普遍流传的陈词滥调上绝对是非常愚蠢的，这些陈词滥调包括：'当你的投资翻番时就卖出股票''持有期满两年后就卖出股票'，或者'当股价下跌10%时马上卖掉股票止损'……绝对不可能找到一个普遍适用于各种类型股票的投资法则。"
  summary: |
    不确定类型就去问经纪人（若其推荐则更必须问）。分类型持有纪律：合理价买的百时美可压箱底20年不管；得州航空不能不管不问；有潜力成第二个沃尔玛的年轻快速增长公司为兑现50%就卖是愚蠢的；Ralston Purina翻番且基本面转平淡后还指望再翻番是疯了。
  tags: [rule, type-specific-rules, no-universal-rule]
  task_ids: [task-01, task-02]

- id: pA86
  title: 将股票分类是分析的第一步——之后了解细节猜测故事结局
  type: principle
  source_chapter: 第7章 7.5（L1444）
  source_quote: |
    "分析一个公司的股票就像分析一个故事一样，将股票分类只是分析公司股票的第一步。现在至少你已经知道了这个故事大致属于什么类型，下一步就是了解各种细节。"
  summary: |
    分类→细节的两步分析结构：分类决定框架（期望、指标、卖点），细节（第8-15章的准则、财务、调研）决定结论。防止"公用事业股票指望菲利普·莫里斯式表现"的错配。
  tags: [principle, classification, analysis-sequence]
  task_ids: [task-01, task-07]

## 第8章 13条选股准则（L1458-1870）

- id: pA87
  title: 总纲——公司业务越简单易懂越好，"傻瓜都能经营"是好特点
  type: principle
  source_chapter: 第8章（L1460-1464）
  source_quote: |
    "我宁愿购买连裤袜公司的股票也不愿购买通信卫星公司的股票……当有人说：'这样的公司连傻瓜都能经营管理'时，这反而让我更加喜欢这家公司，因为或早或晚都有可能将会是一个傻瓜来经营管理这家公司。"
  summary: |
    两条选一原则：无竞争简单行业中的平庸管理公司 > 竞争激烈复杂行业中的杰出管理公司——前者易于追踪研究。13条准则是"完美公司"特征的展开。
  tags: [principle, simplicity, stock-selection]
  task_ids: [task-03]

- id: pA88
  title: 准则1——公司名字听起来枯燥乏味，甚至可笑则更好
  type: principle
  source_chapter: 第8章 8.1.1（L1468-1478）
  source_quote: |
    "这种很简单的业务应该有一个听起来枯燥乏味的名字，名字起得越枯燥乏味，公司就越完美。"
  summary: |
    例：自动数据处理、鲍勃·埃文斯农场、Pep Boys—Manny, Moe & Jack（最可笑=最有赚钱希望）。名字枯燥可让买入价便宜好几美元；警示：公司成功后改名赶时髦（联合石头→Conrock→Calmat）则失去该红利。
  tags: [principle, boring-name, stock-selection]
  task_ids: [task-03]

- id: pA89
  title: 准则2——公司业务枯燥乏味
  type: principle
  source_chapter: 第8章 8.1.2（L1480-1486）
  source_quote: |
    "业务和名称都枯燥乏味的公司保证能够避开华尔街那些所谓专业投资者们的关注……那么你就会有充足的时间以较低的价格买进该公司股票。"
  summary: |
    例：瓶盖瓶塞封口（罐头盒瓶盖）、七棵橡树（处理超市优惠券，4→33美元）、租车代理（修车期代步租车4→16美元）。业务+名称双枯燥=最好；有充足时间低价买入，等华尔街发现推高后转手卖给追风者。
  tags: [principle, boring-business, stock-selection]
  task_ids: [task-03]

- id: pA90
  title: 准则3——公司业务令人厌恶
  type: principle
  source_chapter: 第8章 8.1.3（L1488-1502）
  source_quote: |
    "比只是业务枯燥乏味的公司股票更好的是业务既枯燥乏味又令人厌恶的公司股票。"
  summary: |
    例：Safety-Kleen（清洗汽车零件油污、清饭店厨具油污，名字该用c处用k更值得研究）、Envirodyne（塑料叉子/吸管/热狗肠衣/垃圾袋，3美元→36.875美元）。没人愿写研究报告、没机构愿入名单=股价长期低估。
  tags: [principle, disgusting-business, stock-selection]
  task_ids: [task-03]

- id: pA91
  title: 准则4——公司从母公司分拆出来
  type: principle
  source_chapter: 第8章 8.1.4（L1504-1571）
  source_quote: |
    "公司的分公司或部分业务分拆上市变成独立自由的经济实体……经常会给投资者带来回报惊人的投资机会。"
  summary: |
    机制：母公司不愿子公司失败损害形象→分拆子公司通常资产负债表十分良好；管理层获自由后削成本改革；披露材料写得枯燥低调保守（质量好于年报）；机构把分配到的新股当零钱抛弃。操作：听说分拆或分到新股应马上研究加仓；分拆完成一两个月后查内部人士是否大量买入（见pA94）。
  tags: [principle, spin-off, stock-selection]
  task_ids: [task-03]

- id: pA92
  title: 表8-1证据规则——分拆公司名单（15好/4坏）与AT&T小贝尔案例
  type: template
  source_chapter: 第8章 8.1.4（表8-1 L1512-1559；小贝尔 L1565-1571）
  source_quote: |
    "从1983年11月到1988年10月，七家新成立的小贝尔公司的股票平均收益率是114%，再加上股息其总收益率超过了170%……远远战胜了市场，并且战胜了大多数著名的共同基金。"
  summary: |
    表8-1列15家表现良好（如Argonaut 18→52.125、York Int. 14→59.75）与4家表现不好（如Intelogic Trace 8→3.75）的分拆公司，作为"分拆=机会"的经验证据（非保证）。最佳案例：AT&T分拆的七家小贝尔总回报170%+（经营自由+分成+不需大投资）；296万股东与电话用户皆有优势，少数人利用。正确定策=卖掉母公司AT&T、全部买入小贝尔。
  tags: [template, spin-off, evidence-table]
  task_ids: [task-03]

- id: pA93
  title: 准则5——机构没有持股，分析师不追踪
  type: principle
  source_chapter: 第8章 8.1.5（L1573-1579）
  source_quote: |
    "如果你找到了一只机构投资者持股很少甚至根本没有持股的股票，你就找到了一只有可能赚大钱的潜力股……当一家上市公司告诉我上一次股票分析师来公司的时间是三年前时，我几乎不能掩饰自己内心的狂喜。"
  summary: |
    双重冷门加倍机会（无机构持股+无分析师了解）。高频场景：数千家银行/储贷/保险公司中华尔街只追50-100家。变体：曾风光后被打入冷宫的股票（低谷时的克莱斯勒、埃克森）。查渠道：Vicker's、Nelson's、Spectrum Surveys、价值线、标普股票手册。
  tags: [principle, institutional-neglect, stock-selection]
  task_ids: [task-03]

- id: pA94
  title: 准则6——公司被谣言包围（有毒垃圾或黑手党传闻）
  type: principle
  source_chapter: 第8章 8.1.6（L1581-1589）
  source_quote: |
    "这种荒诞的推断对于最早购买垃圾处理公司股票的投资者来说非常有利，因为这导致其股价相对于真正的投资价值被过于低估了。"
  summary: |
    例：垃圾处理公司（有毒垃圾+黑手党两大传闻，投资上涨100倍）。逻辑：无根据的声誉恐惧造成系统性低估；同类先例：赌场股因黑手党传闻无人敢买，假日/希尔顿入局后成香饽饽。
  tags: [principle, rumor-discount, stock-selection]
  task_ids: [task-03]

- id: pA95
  title: 准则7——公司业务让人感到压抑（如丧葬服务）
  type: principle
  source_chapter: 第8章 8.1.7（L1591-1609）
  source_quote: |
    "如果说除了有毒废料之外，还有什么因素会导致华尔街根本不愿关注一家公司的话，那就是死亡，SCI公司经营的恰恰是丧葬服务业务。"
  summary: |
    SCI模式：连锁整合（只收购一周10多次殡葬服务的生意兴隆殡仪馆）+上下游整合（461殡仪馆/121公墓/花店/棺材配送）+生前预付合同（现金先收复利增值，5年该业务年收入增40%）。机构长期不理睬→低价买入；1986年机构持股超50%成明星股后表现开始落后（并警示棺材收购拖累）。
  tags: [principle, depressing-business, stock-selection]
  task_ids: [task-03]

- id: pA96
  title: 准则8——公司处于零增长行业
  type: principle
  source_chapter: 第8章 8.1.8（L1611-1619）
  source_quote: |
    "我更喜欢的是比低增长行业增长率更低的零增长行业，比如殡葬服务业，往往在这种零增长行业中可以寻找到最赚钱的大牛股。"
  summary: |
    逻辑：高增长行业引来1000个MIT研究生琢磨更便宜地复制（硬盘驱动器业52%年增但35家涌入后无利可图）；零增长行业（丧葬业年增1%）没人竞争→可安心扩大份额（SCI从5%可到10-15%）。对照案例：负增长的烟草业中菲利普·莫里斯15年14→90美元（海外扩张+提价+削成本+品牌利基），同期施乐160→60美元。
  tags: [principle, zero-growth-industry, no-competition]
  task_ids: [task-03, task-04]

- id: pA97
  title: 准则9——公司有一个利基（排他性独家经营权）
  type: principle
  source_chapter: 第8章 8.1.9（L1621-1649）
  source_quote: |
    "无论如何夸大排他性的独家经营权对于一家公司或者公司股东们的价值也不过分。"
  summary: |
    利基形态：①石料场（运费吃掉利润→地区独家经营，混凝料3美元/吨；石头采完还有折旧税收抵扣+资源耗竭补贴）；②独家矿坑（宾厄姆矿坑无法被"发明"）；③专利（药品/杀虫剂/除草剂，审批即摇钱树）；④区域垄断媒体（《波士顿环球报》90%+印刷广告收入）；⑤著名品牌（Robitussin/Tylenol/可口可乐/万宝路）。拥有利基即可提价（提到恰好不引来竞争的水平之下）。
  tags: [principle, niche, moat, pricing-power]
  task_ids: [task-03]

- id: pA98
  title: 准则10——人们要不断购买公司的产品
  type: principle
  source_chapter: 第8章 8.1.10（L1651-1655）
  source_quote: |
    "我宁愿购买生产药品、软饮料、剃须刀片或者香烟的公司的股票，也不愿购买生产玩具的公司的股票。"
  summary: |
    重复购买>一次性购买：玩具每个孩子只买一个且8个月后被替代（换厂家）。有众多稳定行业可选时，何必冒险买易变行业。与pA63（常用药）同源。
  tags: [principle, repeat-purchase, stock-selection]
  task_ids: [task-03]

- id: pA99
  title: 准则11——公司是高技术产品的用户（买受益者而非生产者）
  type: principle
  source_chapter: 第8章 8.1.11（L1657-1659）
  source_quote: |
    "与其购买那些要在无休无止的价格战中苦苦挣扎求生的电脑公司的股票，为什么不购买那些由于电脑价格大战能够用更低的成本购买电脑而提高盈利的公司的股票呢？"
  summary: |
    电脑价格越降，自动数据处理公司成本越低利润越高（上涨600倍）；扫描仪助超市降3%成本即可让利润翻番。规则：技术变革中买用户侧（成本下降受益者），不买生产侧（价格战受害者）。
  tags: [principle, tech-user, stock-selection]
  task_ids: [task-03]

- id: pA100
  title: 准则12——公司内部人士在买入自家公司的股票（1:2.3常态口径）
  type: calculation
  source_chapter: 第8章 8.1.12（L1661-1675）
  source_quote: |
    "一般来说，公司内部人士是自家公司股票的净卖方，通常他们的买入卖出比例是1:2.3……当公司内部人士疯狂地购买自家公司的股票时，你完全可以肯定，这家公司至少在未来6个月内不会倒闭。"
  summary: |
    内部人士买入是最强的秘密信号：买入只有一个原因（认为股价低估、终将上涨）；卖出通常无意义（除非涨幅巨大后多人卖出大部分持仓）。信号强度排序：低薪员工买1万美元>7位副总裁各买1000股>总裁一人买5000股。买入后股价再跌=你可买得比内部人士更便宜。追踪渠道：SEC表格4（Form 4）、Vicker's/内部人士刊物/巴伦/华尔街日报/价值线。1987年崩盘后整体买入卖出比4:1（对比常态1:2.3）提振信心。
  tags: [calculation, insider-buying, signal]
  task_ids: [task-03, task-06]
  inputs: [内部人士买入金额/人数/身份(员工vs高管), 内部人士卖出数据, 常态基准1:2.3]
  formula: 信号强度 ≈ 买入人数×相对薪酬的购买规模；异常判定：买卖比显著偏离1:2.3（如崩盘后4:1）
  units: 比例；美元
  output: "至少6个月内不会倒闭"的确认；低估佐证
  missing_conditions: 内部人士买入≠股价立即上涨；原文未给出"多少人才算多"的量化门槛；A股需映射为公告/董监高持股变动数据

- id: pA101
  title: 准则13——公司在回购股票（vs 增发稀释）
  type: calculation
  source_chapter: 第8章 8.1.13（L1677-1691）
  source_quote: |
    "回购股票是一家公司回报股东的最简单也是最好的方法……如果一家公司回购了自己一半的股份，而且总收益保持不变，那么每股收益就会增长一倍。"
  summary: |
    回购使流通股减少→EPS提高→股价上涨；比削成本/新品更易使EPS翻倍。案例：埃克森回购（3美元/股石油储量 vs 6美元勘探成本，回购=更便宜的"勘探"）；瓶盖瓶塞封口20年每年回购；Teledyne以高于市价定期回购；克莱斯勒业务改善后回购股票+认股权证（图8-2）。反面：Navistar增发1亿新股渡危机，盈利恢复但股东回报被稀释殆尽。多余资金5种用途排序中回购优于：提高股息/开发新品/开拓新业务/收购兼并（吉列把资本浪费于四者导致35美元而非100美元）。
  tags: [calculation, buyback, dilution, capital-allocation]
  task_ids: [task-03, task-06]
  inputs: [回购股数/金额, 总股本变化, 净利润总额, 回购价 vs 内在价值]
  formula: 回购后EPS = 净利润 ÷ (总股本 − 回购股数)；回购一半且总收益不变 → EPS翻倍
  units: 美元/股
  output: 每股收益增厚幅度；判断公司资本配置是否善待股东（回购/分红 vs 高价多元恶化收购/增发）
  missing_conditions: 需区分回购注销与回购用于股权激励；高价位回购（Teledyne式高于市价要约）与低价回购信号含义不同

- id: pA102
  title: 完美公司画像模板——Cajun清洁剂（13条准则的集成演练）
  type: template
  source_chapter: 第8章 8.2（L1844-1862）
  source_quote: |
    "如果我能想到一家非常辉煌的企业，集中了……所有这些公司最糟糕的因素于一身的话，那么这家公司就非Cajun清洁剂公司莫属。"
  summary: |
    虚构的理想标的集成模板（作者自嘲"我还在做梦"）：业务令人厌恶（除霉）+分拆独立+地处沼泽无人拜访+名字可笑+无机构持股+专利凝胶=利基+终生除污保险（预付现金）+董事大量买入+收益4年年增20%无季度下滑+零负债+衰退表现良好。用于演示13条准则如何叠加；买入契机=大盘下跌15%拖累个股，买价可比内部人士更低（7.50 vs 董事10美元）。
  tags: [template, perfect-company, synthesis, fictional-case]
  task_ids: [task-03]

## 第9章 避而不买清单（L1872-2062）

- id: pA103
  title: 避而不买①——热门行业的热门股
  type: rule
  source_chapter: 第9章 9.1（L1874-1941）
  source_quote: |
    "如果说有一种股票我避而不买的话，那它一定是最热门行业中最热门的股票……热门股跌下去和涨上来的速度一样快。"
  summary: |
    特征：人人谈论、社会压力驱使追买；股价涨到远超任何估值方法，支撑只有一厢情愿的期望。案例：家庭购物网络16个月3→47→3.5美元；地毯业（28→4美元/码后200家新对手涌入，全行业无利）；硬盘驱动器（52%行业增速照样毁灭）；石油服务业（Tom Brown 50→1美元）；施乐170美元时断言无限增长，多元化失败跌84%。"靠一个接一个热门股谋生很快得接受福利救济。"
  tags: [rule, hot-stock, negative-screen]
  task_ids: [task-04]

- id: pA104
  title: 无护城河的高增长规则——成功若无法用专利或利基保护，必被群起效仿
  type: rule
  source_chapter: 第9章 9.1（L1929）
  source_quote: |
    "假如你有一个稳赚不赔的商业创意，但却无法用专利或者利基来加以保护，那么一旦你获得成功，你就得防备其他人群起效仿，在商业界，效仿是一种最不纯粹要命的攻击方式。"
  summary: |
    判断高增长能否持续的测试：有无专利/利基保护。热门行业吸引企业家与风投彻夜盘算进入——200家对手+价格战=利润归零。为准则8（零增长行业）与准则9（利基）提供反面逻辑。
  tags: [rule, moat-test, competition, negative-screen]
  task_ids: [task-03, task-04]

- id: pA105
  title: 避而不买②——被吹捧成"下一个XX"的公司
  type: rule
  source_chapter: 第9章 9.2（L1943-1951）
  source_quote: |
    "被吹捧成下一个的公司几乎从来都不会真正成为它的楷模那样卓越非凡的明星……所有被称为'下一个Circuit City'的公司的股票市值都比最初下跌了59%～96%。"
  summary: |
    双重信号：被称"下一个IBM"既表明模仿者气数已尽，也预示楷模本身将成明日黄花（IBM随后果然陷入困境）。案例："下一个玩具反斗城"的儿童世界步履维艰、"下一个Price Club"的仓库俱乐部不好过。
  tags: [rule, next-big-thing, negative-screen]
  task_ids: [task-04]

- id: pA106
  title: 避而不买③——"多元恶化"的公司（高价收购+业务超出理解范围）
  type: rule
  source_chapter: 第9章 9.3（L1953-1963）
  source_quote: |
    "这种一心一意想要'多元化'的公司寻找的是具备以下特点的收购对象：①收购价格过于高估；②经营业务完全超出人们的理解范围。这两点毫无疑问会使公司在收购后发生的损失最大化。"
  summary: |
    十年轮回：10年疯狂多元恶化收购、10年低价剥离重组，实为财富从大公司股东转移给被收购小公司股东。案例：美孚(Marcor/Container贱卖)、吉列（药箱/数字手表）、通用磨坊、美国工业（一年300次收购"一天一家"）、Genesco（17年150次收购后破产）。"多元恶化"仅有的两个好处：持有被收购方股票；从中找困境反转候选（pA81⑤）。
  tags: [rule, diworseification, negative-screen]
  task_ids: [task-04]

- id: pA107
  title: 收购规则——真要收购须相关主业；强回购优于任何收购
  type: rule
  source_chapter: 第9章 9.3（L1981-2018）
  source_quote: |
    "如果一家公司真的必须进行收购的话，我认为它最好是收购与自己的主业相关的公司……我更愿意看到一次强有力的股票回购举动，因为这样的回购对股价来说会产生最纯粹的协同作用。"
  summary: |
    正例Melville（先经营成功上一次收购再进行下一次：CVS/Marshall's/Kay-Bee，制鞋厂22→1家，17年涨30倍）vs 反例Genesco（协同作用失效再未涨回）。协同作用=相关业务组合使整体大于部分；例外认可：主业糟糕时收购另寻出路（巴菲特离开纺织、Tisches家族影院→烟草→保险→CBS）。
  tags: [rule, acquisition-discipline, synergy, buyback]
  task_ids: [task-03, task-04]

- id: pA108
  title: 避而不买④——小声耳语的股票（故事诱人、没有收益）
  type: rule
  source_chapter: 第9章 9.4（L2020-2036）
  source_quote: |
    "这些一旦冒险成功将获得巨大回报但成功机会非常小的高风险股票……往往给投资人讲述一个具有爆炸性效应的故事……除了这一事实以外，另一个共同特点就是吹牛吹破天，却根本没有什么实质内容。"
  summary: |
    特征：私房话式推荐+即将解决国家大难题（石油短缺/艾滋病）的神奇方案。无法计算每股收益（没有收益）、不存在P/E。作者亲身失败清单：KMS工业（40→2.5美元）、Smith Labs（25→1美元）、Bioresponse及近20只。识别测试：只有咝咝声没有牛排在烤。
  tags: [rule, whisper-stock, story-stock, negative-screen]
  task_ids: [task-04]

- id: pA109
  title: 耳语股应对规则——等有收益记录再买不迟，仍可赚10倍
  type: rule
  source_chapter: 第9章 9.4（L2038）
  source_quote: |
    "如果公司的前景非常美好，那么等到明年或者后年再投资仍然会得到很高的回报……当公司用业绩证明自己的实力以后，仍然可以从这只股票上赚到10倍的回报。"
  summary: |
    对治"必须IPO时买入否则来不及"的心理压力（该观点很少正确；基因技术上市日35→89美元属罕见例外）。看一段时间再决定不迟——收益记录会消灭大部分假故事。
  tags: [rule, patience, story-stock]
  task_ids: [task-04, task-14]

- id: pA110
  title: IPO规则——新公司IPO四中三失望；分拆上市IPO是例外
  type: rule
  source_chapter: 第9章 9.4（L2042-2044）
  source_quote: |
    "这种首次发行的新股4只股票中有3只的长期表现都十分令人失望……但是那些从其他公司中分拆出来独立上市的公司的首次公开发行的股票让我赚了很多钱。"
  summary: |
    区分两类IPO：白手起家新公司（无历史可研究，风险大）vs 从成熟母公司分拆的IPO（有长经营历史，"可以像研究福特或可口可乐那样研究它们"：玩具反斗城、租车代理、Safety-Kleen）。例外承认：联邦快递IPO后涨25倍。
  tags: [rule, ipo, spin-off-exception]
  task_ids: [task-04, task-03]

- id: pA111
  title: 避而不买⑤——25%-50%销售额依赖单一客户的供应商
  type: rule
  source_chapter: 第9章 9.5（L2046-2050）
  source_quote: |
    "如果一家公司把25%～50%的商品都卖给了同一个客户，这表明该公司的经营处于十分不稳定的状态之中……购买这种过于依赖大客户的供应商公司的股票几乎不可能获得很大的投资成功。"
  summary: |
    双重风险：①合同随时可能被取消（IBM可自制零部件或不再需要，SCI Systems/Tandon例）；②大客户握有谈判优势可逼迫降价让利，压缩利润空间。判定阈值：单一客户占销售额25%起警惕，50%危险。
  tags: [rule, customer-concentration, negative-screen, threshold]
  task_ids: [task-04]

- id: pA112
  title: 避而不买⑥——名字花里胡哨的公司
  type: rule
  source_chapter: 第9章 9.6（L2052-2054）
  source_quote: |
    "一家资质平平的公司如果名字起得花里胡哨却可以吸引投资者买入，并给他们一种错误的安全感。"
  summary: |
    名字中带"高级""主要""微型"、含字母x、神秘缩写词（UAL改Allegis）会诱发一见钟情式买入。与准则1（枯燥名字）互为镜像：施乐若叫"大卫干式复印机"，投资者本会以怀疑态度认真分析。
  tags: [rule, fancy-name, negative-screen]
  task_ids: [task-04]

## 第10章 收益，收益，还是收益（L2064-2385）

- id: pA113
  title: 股票价值归结为收益和资产，尤其是收益
  type: principle
  source_chapter: 第10章（L2068）
  source_quote: |
    "是什么因素使一家公司具有投资价值？……我个人认为，最终还是归结为两点：收益和资产，尤其是收益。"
  summary: |
    估值第一性原理。有时需数年股价才调整到与真实价值相符，坚信价值决定价格值得。一股股票代表对一家公司的部分所有权，绝非一注彩票（L2070）——分析股票如同评估要买下的洗衣店/药店。
  tags: [principle, earnings-first, valuation-foundation]
  task_ids: [task-05]

- id: pA114
  title: 价格线与收益线并驾齐驱——偏离终会回归
  type: principle
  source_chapter: 第10章（L2096-2100）
  source_quote: |
    "股票的价格线与收益线的波动是并驾齐驱的，如果股票价格线的波动偏离了收益线，它迟早还会回到与收益线相一致的趋势上。"
  summary: |
    全书16张走势图统一论证的规律（陶氏、雅芳、Masco 30年收益涨800倍股价涨1300倍、Shoney's连续116季度增长）。用途：翻阅股票走势图手册自学；长期看公司收益波动最终决定股价波动。
  tags: [principle, price-follows-earnings, chart-reading]
  task_ids: [task-05]

- id: pA115
  title: 价格线远高于收益线=危险信号
  type: rule
  source_chapter: 第10章（L2142、L2287）
  source_quote: |
    "判断股票价格是不是被高估的快捷方法就是比较股票价格走势线与收益线是否相符……在股票价格线低于收益线时购买……在股票价格线远高于收益线时卖掉……我实在想不出比这更好的投资策略了。"
  summary: |
    图上快捷规则：股价线高于收益线是危险信号（雅芳1972年140美元、64倍P/E，随后一年内大跌86%；The Limited 1983/1987两次偏离收益线均短期大跌）。价格线低于收益线时买入胜算大。
  tags: [rule, price-earnings-line, overvaluation-signal]
  task_ids: [task-05]

- id: pA116
  title: 市盈率计算口径——股价÷前12个月每股收益；P/E=收回投资年数
  type: calculation
  source_chapter: 第10章 10.1（L2291-2323）
  source_quote: |
    "用35除以3.50就能得出这家公司市盈率为10倍……市盈率可以看做是一家上市公司获得的收益可以使投资者收回最初投资成本所需的年数。"
  summary: |
    标准口径：P/E = 当前股价 ÷ 前12个月（或上一财政年度）EPS（凯玛特例：35÷3.50=10倍）。解释义：假设收益不变，10倍P/E=10年收回投资；40倍=40年（"到那时你已成老爷爷"）。高P/E=赌未来收益大幅改善，低P/E=市场怀疑前景。
  tags: [calculation, pe-ratio, definition]
  task_ids: [task-05]
  inputs: [当前股价, 前12个月或上一财年每股收益EPS]
  formula: P/E = 股价 ÷ EPS
  units: 倍（年）
  output: 估值倍数及其"收益回收年数"解释（表10-1《华尔街日报》行情表即含P/E列）
  missing_conditions: 亏损公司无P/E；收益异常时（见pA117）须先核查；A股动态/静态/TTM口径需指定

- id: pA117
  title: 异常高P/E须先核查一次性冲销
  type: rule
  source_chapter: 第10章 10.1（L2317）
  source_quote: |
    "有时，报纸上所列的市盈率可能会高得离谱，这通常是因为公司在账面上当期的短期收益中冲销了一笔长期损失……如果市盈率看起来异乎寻常，你可以请经纪人为你解释一下原因。"
  summary: |
    数据质量规则：异常P/E常因收益基数被一次性冲销扭曲而非真实估值，先用经纪人/财报核实原因再下结论。
  tags: [rule, pe-ratio, data-quality, one-time-charge]
  task_ids: [task-05, task-06]

- id: pA118
  title: 类型化P/E基准区间——公用事业7-9倍＜稳定增长10-14倍＜快速增长14-20倍
  type: calculation
  source_chapter: 第10章 10.1（L2327）
  source_quote: |
    "公用事业公司股票的平均市盈率（最近这段时间是7～9倍）低于稳定增长型公司的平均市盈率（这段时间是10～14倍）；相应稳定增长型公司股票的平均市盈率又低于快速增长型公司的平均市盈率（14～20倍）。"
  summary: |
    P/E必须同型比较："不管什么股票只要市盈率低就买"的策略没有意义，不拿苹果与桔子相比——陶氏化学明显偏低的P/E对沃尔玛并非如此。周期型P/E介于缓增与快增之间。基准数字为1980年代美股经验值。
  tags: [calculation, pe-ratio, type-benchmark]
  task_ids: [task-05, task-01]
  inputs: [公司当前P/E, 公司六类分型, 同类型平均P/E]
  formula: 比较基准=同类型公司平均P/E（缓增<周期<稳增<快增）
  units: 倍
  output: 该股P/E相对同型的偏高/偏低/合理判断
  missing_conditions: 区间为1980年代末美国数据，绝对数值不可平移，需以当前市场重估；周期股利润谷底P/E天然虚高须另行处理

- id: pA119
  title: 历史P/E区间比较法——现在支付的价格vs别人过去支付的价格
  type: rule
  source_chapter: 第10章 10.2（L2331-2337）
  source_quote: |
    "在购买一只股票之前，你可能希望追踪了解一下这家公司最近几年的市盈率，以便大致判断正常的市盈率水平应该是多少……比较你和别人支付的股价是否相当。"
  summary: |
    可口可乐例：看现在相对收益支付的价格，再看别人过去支付的价格。数据渠道：经纪人、标普上市公司报告、《价值线投资调查》（"业余投资者必须知道的所有投资相关数据都可以在价值线上找到"）。边界：新公司历史太短无记录。
  tags: [rule, pe-ratio, historical-range, valuation]
  task_ids: [task-05]

- id: pA120
  title: 绝不买入市盈率特别高的股票
  type: rule
  source_chapter: 第10章 10.2（L2339-2355）
  source_quote: |
    "即使关于市盈率你什么都记不住的话，你也一定要牢记一点：千万不要买入市盈率特别高的股票。只要坚决不购买市盈率特别高的股票，就会让你避免巨大的痛苦与巨大的投资亏损。"
  summary: |
    全书最硬的估值红线。案例：麦当劳1972年50倍P/E（运营依旧优秀）75→25美元；EDS 500倍（分析师称应1000倍）40→3美元；雅芳64倍需收入超美国钢铁+石油+加州总和才能收回成本，收益反降、1974年跌到18.625美元；宝丽来50倍（SX-70须每家4台才能支撑）18个月跌89%。机理：高P/E需要持续难以置信的高增长来维持，特别重的马鞍是赛马的障碍。
  tags: [rule, pe-ratio, hard-rule, overvaluation]
  task_ids: [task-05]

- id: pA121
  title: 股市整体P/E风向标——8倍升到16倍即高估警告
  type: rule
  source_chapter: 第10章 10.3（L2359-2365）
  source_quote: |
    "你可以看到股票市场整体的市盈率逐渐从8倍左右上升到了16倍……这是一个投资者本来应该注意到的大多数股票已经过于高估的警告信号。"
  summary: |
    个股P/E相互依存，市场整体也有P/E，是判断整体高估/低估的风向标（虽不必理会大盘走势，但个股普遍高估时整体P/E必然显示）。案例：1982-87牛市整体P/E翻倍至16倍（随后1987年10月暴跌）；1971年整体20倍后1973-74年暴跌。利率影响P/E（低利率→债券吸引力降→愿意为股票付更高价），但牛市乐观情绪可把P/E哄抬到匪夷所思（EDS 500倍等）。
  tags: [rule, market-pe, overvaluation-signal, macro-check]
  task_ids: [task-05, task-14]

- id: pA122
  title: 未来收益无法预测，但可以核查公司提高收益的五途径计划
  type: checklist
  source_chapter: 第10章 10.4（L2367-2379）
  source_quote: |
    "一家公司可以用5种基本方法增加收益：削减成本，提高售价，开拓新的市场，在原有市场上销售出更多的产品，重振、关闭或者剥离亏损的业务。"
  summary: |
    预测收益不可能（分析师预测一错再错，"出乎意料"是财经文章最常搭配词），替代方案：了解公司提高收益的发展计划，定期查看计划是否真的有效提高收益。五途径是调研的关键检查点；职业/生活优势在此最有帮助。短期反常（收益增股价跌/收益降股价涨）源于预期差，不改长期规律。
  tags: [checklist, earnings-driver, five-ways, plan-verification]
  task_ids: [task-05, task-09, task-08]

---

## 附注（覆盖核对）

- 13条选股准则：pA88-pA101（8.1.1-8.1.13 逐条）✔
- 避而不买6类：pA103/pA105/pA106/pA108/pA111/pA112（9.1-9.6 逐条）✔
- 六类公司定义与特征：pA68（总框架）+ pA69/pA70/pA73/pA77/pA80/pA83（六类分条）+ pA81（困境反转5子型）✔
- 内部人士1:2.3、回购vs增发：pA100/pA101 ✔
- P/E规则：pA116-pA121（口径/冲销核查/类型基准/历史区间/绝不买超高/整体风向标）✔
- 第一部分要点16条：pA41-pA56 逐条 ✔；三问与承受损失：pA28-pA32 ✔
- 长期收益口径9.8%/5%/4.4%/3.4%与通胀调整：pA18/pA19/pA20 ✔
- 表0-1、表3-1、表8-1（必读表）：pA04/pA20/pA92 ✔
- 边界说明：计算类中标注了1980年代美国数据、SEC规则、A股映射缺失等 missing_conditions。
# 原则候选 · Part B（第10章10.1起 ～ 第20章，行2289-4221）

> principle-extractor 输出。覆盖全书后半部；前半由 Part A 负责。逐条原子化，未做筛选。
> task_ids 对照见 BOOK_OVERVIEW.md 任务清单（task-01~15）。

```yaml
# ── 第10章 市盈率与收益（L2289-2385）──────────────────────────

- id: pB01
  title: 市盈率基本计算口径（股价/每股收益=收回投资年数）
  type: calculation
  source_chapter: 第10章 10.1（L2289-2325）
  source_quote: |
    "用35除以3.50就能得出这家公司市盈率为10倍……市盈率可以看做是一家上市公司获得的收益可以使投资者收回最初投资成本所需的年数。"
  summary: |
    P/E=当前股价÷前12个月（或上一财年）每股收益；其含义是在收益不变假定下收回投资成本所需年数。报纸行情表即有。若P/E异常高，先问经纪人是否因短期收益冲销长期损失所致。
  inputs: [当前股价, 前12个月或上一财年每股收益]
  formula: "P/E = 股价 ÷ 每股收益；收回成本年数 ≈ P/E"
  units: 倍（年）
  output: 市盈率倍数
  missing_conditions: 亏损股无P/E；收益被一次性项目扭曲时需先问明原因
  tags: [pe-ratio, valuation, calculation]
  task_ids: [task-05]

- id: pB02
  title: 不同类型公司P/E区间不同；不能跨行业比低P/E
  type: rule
  source_chapter: 第10章 10.1（L2327）
  source_quote: |
    "公用事业公司股票的平均市盈率（最近这段时间是7～9倍）低于稳定增长型公司的平均市盈率（10～14倍）……对于陶氏化学公司股票而言明显偏低的市盈率，对于沃尔玛公司股票而言却并非如此。"
  summary: |
    缓慢增长型P/E最低、快速增长型最高、周期型居中（写作期：公用事业7-9倍、稳定增长10-14倍、快速增长14-20倍）。判断P/E高低必须与同行业同类型比较，不能拿苹果比桔子。
  tags: [pe-ratio, company-type, rule]
  task_ids: [task-05, task-01]

- id: pB03
  title: 买入前追踪公司历史市盈率区间
  type: rule
  source_chapter: 第10章 10.2（L2331-2337）
  source_quote: |
    "在购买一只股票之前，你可能希望追踪了解一下这家公司最近几年的市盈率，以便大致判断正常的市盈率水平应该是多少。"
  summary: |
    买前比较"你现在为收益支付的价格"与"别人过去支付的价格"：查公司P/E历史记录（标准普尔报告、证券公司、《价值线》），判断当前P/E相对自身历史是高是低。新上市历史短的公司此法不适用。
  tags: [pe-ratio, valuation, historical-comparison]
  task_ids: [task-05]

- id: pB04
  title: 千万不要买入市盈率特别高的股票
  type: rule
  source_chapter: 第10章 10.2（L2339-2355）
  source_quote: |
    "即使关于市盈率你什么都记不住的话，你也一定要牢记一点：千万不要买入市盈率特别高的股票。"
  summary: |
    超高P/E要求未来收益长期保持难以置信的高增长才能维持股价。麦当劳50倍P/E从75美元跌到25美元、EDS 500倍从40美元跌到3美元、雅芳64倍跌到18.625美元、宝丽来50倍18个月跌89%——公司运营没出错，只是买价过高。
  tags: [pe-ratio, rule, red-line, valuation]
  task_ids: [task-05, task-10]

- id: pB05
  title: 整体市场P/E是高估/低估的风向标
  type: rule
  source_chapter: 第10章 10.3（L2357-2365）
  source_quote: |
    "股票市场整体的市盈率水平对于判断市场整体上是被高估或是低估是一个很好的风向标……从8倍左右上升到了16倍……这是大多数股票已经过于高估的警告信号。"
  summary: |
    个股P/E相互依存，市场整体也有P/E。1982-1987牛市中整体P/E从约8倍升到16倍（同等收益支付价格翻倍）=高估警告；1971年整体平均P/E达20倍后迎来1973-74暴跌。利率低会推高合理P/E，但乐观情绪可把P/E抬到离谱水平。
  tags: [pe-ratio, market-level, rule, bubble-signal]
  task_ids: [task-05, task-14]

- id: pB06
  title: 公司增加收益的5种基本途径
  type: checklist
  source_chapter: 第10章 10.4（L2377-2379）
  source_quote: |
    "一家公司可以用5种基本方法增加收益：削减成本，提高售价，开拓新的市场，在原有市场上销售出更多的产品，重振、关闭或者剥离亏损的业务。"
  summary: |
    削减成本／提高售价／开拓新市场／老市场卖更多／重振关闭剥离亏损业务。预测未来收益不可能，但应弄清公司提高收益的发展计划，并定期核查计划是否真的提高了收益。
  tags: [earnings-growth, checklist, five-ways]
  task_ids: [task-05, task-09]

- id: pB07
  title: 无法预测收益；只核查公司提高收益计划的执行
  type: principle
  source_chapter: 第10章 10.4（L2369-2377）
  source_quote: |
    "虽然你不能准确预测公司的未来收益，但至少你可以了解一下公司为提高收益所制定的发展计划，然后你就可以定期查看公司对这些计划实施后是否真的有效地提高了收益水平。"
  summary: |
    专业与业余投资者预测收益都一错再错（"出乎意料"是财经杂志最常见的词）。可行替代：弄清公司的增利计划（见pB06五途径），按季/年核查执行效果。收益升股价跌或收益降股价升只是短期反常。
  tags: [earnings-forecast, principle, check-execution]
  task_ids: [task-05, task-09]

# ── 第11章 两分钟独白（L2387-2477）──────────────────────────

- id: pB08
  title: 下单前三步：分类→估值→故事
  type: principle
  source_chapter: 第11章（L2389-2391）
  source_quote: |
    "第一步……属于六种类型中的哪一种。第二步，根据股票的市盈率倍数……低估还是高估了。接着第三步是要尽可能详细地了解……公司未来发展的'故事'。"
  summary: |
    每笔买入前依次完成：①六类型归类；②用P/E判断当前价位相对前景低估/高估；③弄清推动公司收益持续增长的动力因素（隐蔽资产型例外：只需耐心抱牢等资产被重新发现）。越能确定动力因素，越能确定前景。
  tags: [buy-process, three-steps, principle]
  task_ids: [task-01, task-05, task-07]

- id: pB09
  title: 两分钟独白模板（原因+成功条件+障碍）
  type: template
  source_chapter: 第11章（L2395-2397）
  source_quote: |
    "在下单购买一只股票之前，我喜欢进行一个两分钟的独白，内容包括：我之所以对这只股票感兴趣的原因是什么；需要具备哪些条件，这家公司才能取得成功；这家公司未来发展面临哪些障碍。"
  summary: |
    下单前用两分钟向家人/朋友/自己讲清三件事：为什么感兴趣、公司成功需要什么条件、面临哪些障碍。若连小孩子都能听懂你的分析，表明你已抓住公司发展的关键。
  tags: [two-minute-monologue, template, buy-decision]
  task_ids: [task-07]

- id: pB10
  title: 六类型公司的两分钟独白主题要点
  type: template
  source_chapter: 第11章（L2399-2409）
  source_quote: |
    "如果你考虑买入的是一家缓慢增长型公司的股票……重点关注的因素包括：'这家公司在过去10年间每年收益都在增加，股息收益率十分吸引人……'"
  summary: |
    分类型独白模板——缓慢增长：10年收益递增+股息记录+从不削减股息（衰退期也提高）；周期：业务状况、存货增减、销售价格；隐蔽资产：隐蔽资产是什么、值多少（录像带业务每股4美元+房地产每股7美元 vs 股价8美元）；困境反转：公司是否已开始自救、重整计划是否见效；稳定增长：P/E、近期涨幅、增长加速因素；快速增长：向哪些市场扩张、如何管理以保持增长。
  tags: [two-minute-monologue, company-type, template]
  task_ids: [task-07, task-01]

- id: pB11
  title: 询问竞争对手是寻找大牛股的技巧
  type: rule
  source_chapter: 第11章 11.1（L2417）
  source_quote: |
    "当某家公司的一位高级管理人员承认另一家竞争对手给他留下了深刻印象时，你就可以断定那家竞争对手公司肯定有些地方做得相当出色。"
  summary: |
    问上市公司高管"你最成功的竞争对手是谁"。95%情况下高管只会诋毁对手（无意义）；一旦高管承认对手出色（如联合旅馆副总裁称赞La Quinta），该对手极可能是大牛股候选。
  tags: [research, competitors, rule, information-edge]
  task_ids: [task-07, task-09]

- id: pB12
  title: 旅馆业千分之一规则（每晚房费≈客房造价的1‰）
  type: calculation
  source_chapter: 第11章 11.1（L2429）
  source_quote: |
    "旅馆和汽车旅馆向客人每晚收取的住宿费通常相当于一间客房实际造价的1‰。"
  summary: |
    行业定价口径：每晚住宿费≈单间客房实际造价×1‰（40万美元客房收400美元/晚，2万美元客房收20美元/晚）。用于快速判断酒店类公司定价与成本结构是否合理。
  inputs: [客房实际造价]
  formula: "每晚房费 ≈ 客房造价 × 1‰"
  units: 美元
  output: 合理每晚房费基准
  missing_conditions: 仅旅馆/汽车旅馆行业经验规律；未含税费与季节因素
  tags: [industry-rule, hotel, calculation]
  task_ids: [task-06]

- id: pB13
  title: 只买已经非常成功的公司，不买"将会成功"的公司
  type: rule
  source_chapter: 第11章 11.1（L2441-2443）
  source_quote: |
    "La Quinta公司已经是一家取得了巨大成功的优秀企业，并非那种将会、可能、也许、很快就会成功的企业。如果公司只有成功的可能而事实上还没有做到非常成功，那么就根本不要购买它们的股票。"
  summary: |
    买入标准是"已经用事实证明了的成功"（La Quinta已成功经营四五年、多处复制成功、年增50%而P/E仅10倍），而非"将来可能成功"。区分已验证成功与愿景。
  tags: [buy-criteria, proven-success, rule]
  task_ids: [task-03, task-07]

- id: pB14
  title: 经营模式复制证明成功之前不要买入
  type: rule
  source_chapter: 第11章 11.2（L2471-2475）
  source_quote: |
    "投资者应该一直捂紧自己的钱袋，等到这家公司证明自己在伊利诺伊州或者缅因州复制这一经营模式同样也能够成功赚钱时，再购买它的股票。"
  summary: |
    Bildner's教训：忘记问"经营策略在其他地方复制也能成功吗？"。必须等公司在起源地以外的第二个市场成功复制模式再买；同时应担心缺乏熟练店长、财力有限、无力克服最初失败的公司。波士顿/纽约新店惨败时就应及早认输卖出。
  tags: [buy-criteria, replication, rule, growth-stock]
  task_ids: [task-03, task-07]

- id: pB15
  title: 内部人士卖出不构成拒绝买入一只股票的理由
  type: rule
  source_chapter: 第11章 11.1（L2449）
  source_quote: |
    "因为内部人士卖掉一只股票就否定这只股票是一个非常愚蠢的理由。"
  summary: |
    La Quinta一位创始人以市价一半卖出，林奇险些因此放弃这只11倍股（该创始人只为分散自己的组合）。内部人士卖出（多为个人财务原因）≠公司基本面恶化。
  tags: [insider-selling, rule, psychological-trap]
  task_ids: [task-10, task-03]

- id: pB16
  title: 在牌变得更差之前及早摊牌认输
  type: rule
  source_chapter: 第11章 11.2（L2475）
  source_quote: |
    "在手上的牌变得更差之前，就应该及早摊牌认输出局，还不至于输得太惨。"
  summary: |
    当失败证据已经明确（如新分店连续惨败），应在局面进一步恶化前卖出止损；不要趴在桌上睡着。与"耐心持有好股"互为边界：前提是区分基本面恶化与单纯股价波动。
  tags: [sell-discipline, cut-loss, rule]
  task_ids: [task-02, task-09]

# ── 第12章 获取真实信息（L2479-2796）──────────────────────────

- id: pB17
  title: 年报之外的四条信息获取途径
  type: checklist
  source_chapter: 第12章（L2487）
  source_quote: |
    "从上市公司年报中无法得到的信息可以通过以下途径获得：向经纪人咨询、给上市公司打电话、去上市公司拜访、做一些实地调查研究。"
  summary: |
    信息获取程序：经纪人（索要研究报告/价值线/内部人数据）→给公司投资者关系部门打电话→拜访总部→实地调查。所有应披露信息都在招股书/季报/年报中；小道消息因"来源越神秘越有说服力"的心理而流行，但公开信息更可靠。
  tags: [information-channels, checklist, research]
  task_ids: [task-09, task-07]

- id: pB18
  title: 向经纪人索要资料与引导系统分析的提问模板
  type: template
  source_chapter: 第12章 12.1（L2495-2531）
  source_quote: |
    "他们可以提供标准普尔公司报告、投资时事通讯、年报、季报、招股说明书、股东大会委托权说明书、价值线投资调查……你可以让他们帮你收集市盈率和公司增长率、公司内部人士持股、机构投资者持股等数据。"
  summary: |
    让经纪人做的事：提供标普报告、价值线、年报季报、委托书、分析师报告；收集P/E与增长率、内部人士/机构持股数据。引导提问清单：什么类型？增长率多少？当前与历史P/E？为何现在是买点？市场在哪？是否盈利？如何为扩张融资不稀释？内部人士在买吗？机构持股？分析师跟踪多久？要5年股价-收益并列图与股息记录。
  tags: [broker, template, question-list]
  task_ids: [task-09, task-07]

- id: pB19
  title: 给公司投资者关系部门打电话的问题清单
  type: template
  source_chapter: 第12章 12.2（L2543-2559）
  source_quote: |
    "直接向公司询问'你们公司未来收益是多少'就像一个陌生人问你的年薪是多少一样很不礼貌，要想让对方容易接受，就得问得委婉巧妙：'华尔街对贵公司明年的收益预测是多少呢？'"
  summary: |
    打电话规则：①提前准备问题，别一上来问"为什么股价在跌"（显得外行，公司自己也不知道）；②问收益用委婉口径"华尔街对贵公司明年的收益预测是多少"；③先展示自己做过功课（"年报看到减债5亿美元，未来削减计划是什么？"）；④两个通用问题："今年公司发展有哪些有利因素/不利因素？"；⑤结束总结几个有利/不利因素。
  tags: [ir-call, template, question-list]
  task_ids: [task-09, task-07]

- id: pB20
  title: 打电话的期望：约10个电话出1个意外信息
  type: principle
  source_chapter: 第12章 12.2（L2561）
  source_quote: |
    "大约每10个电话中会有一个电话让我得知一些非同一般的信息……如果我同一家很不景气的公司的人员通电话，那么10次中有9次……进一步证实公司仍然很不景气，但是到了第10次，会得知一些新的迹象表明公司前景开始乐观。"
  summary: |
    打电话的信息期望值：10%的通话带来出乎意料的信息；不景气公司第10个电话可能带来尚未普遍流传的乐观迹象，好公司则相反（意外常是坏消息）。意外信息对正在买卖该股的决策非常有价值。
  tags: [ir-call, expectation, principle]
  task_ids: [task-09]

- id: pB21
  title: 只管事实和数据，不要理会形容词
  type: rule
  source_chapter: 第12章 12.3（L2583）
  source_quote: |
    "投资者根本没有必要去浪费时间揣摩公司工作人员言语之中形容词的含意，更简单的对策就是：不要理会任何形容词，只管事实和数据。"
  summary: |
    投资者关系部门基本诚实（真相迟早见季报），但形容词因行业而异：成熟产业（纺织）极度保守——"一般"实际是"很好"；服装/软件公司过度乐观——最差也只是"情况基本可以"。对策：剥离所有形容词，只要销售数据等事实。
  tags: [ir-call, facts-vs-adjectives, rule]
  task_ids: [task-09, task-10]

- id: pB22
  title: 总部简朴是好信号，豪华是危险信号
  type: rule
  source_chapter: 第12章 12.4（L2589-2597）
  source_quote: |
    "公司高级管理人员把办公室装饰得非常豪华之日，就是投资者应该为这家公司的收益开始忧心之时。"
  summary: |
    拜访总部找"感觉"：Taco Bell总部挤在保龄球场后面、瓶盖瓶塞封口总裁办公室看得见生产线+褪色油地毡（30年涨280倍）=好公司；富丽堂皇如预科学校的Uniroyal总部、精美古典家具、抛光胡桃木墙=走下坡路迹象。第一个问题问"上次分析师来是什么时候？"——"两年多前"是惊喜（Meridian银行22年收益增长）。
  tags: [headquarter-visit, signal, rule]
  task_ids: [task-09]

- id: pB23
  title: 逛街和吃东西是基本面分析的成功之道（实地调查）
  type: rule
  source_chapter: 第12章 12.6（L2613-2635）
  source_quote: |
    "我就一直相信逛街和吃东西是一个进行基本面分析的投资成功之道……如果能够实地考察一下这家公司经营的实际情况，会让你的分析更加可靠。"
  summary: |
    亲身考察公司经营实况：住店（La Quinta三晚跳床/趟水/拉窗帘）、逛店（玩具反斗城问顾客是否再来、Pic 'N' Save看79美分古龙水被哄抢）、试车（克莱斯勒钻进钻出车型）、停车场访谈车主。但实地不能替代关键问题的询问（Bildner's教训）。国家相似性越强，一地受欢迎的产品越可能全国成功。
  tags: [field-research, information-edge, rule]
  task_ids: [task-09, task-13]

- id: pB24
  title: 读年报法：跳过文字直接翻资产负债表
  type: rule
  source_chapter: 第12章 12.7（L2639-2643）
  source_quote: |
    "印在光洁的纸面上的文字部分容易理解却往往根本无用，附在后面的数字部分很难理解却相当重要……纸张越便宜，上面的信息越宝贵。"
  summary: |
    年报阅读顺序：直接翻到合并资产负债表（如福特年报第27页），再看10年财务数据概要（第38页）。文字部分（颂词、企业文化、赞助展览）几分钟略过。同一方法适用所有年报。
  tags: [annual-report, reading-method, rule]
  task_ids: [task-06]

- id: pB25
  title: 从资产负债表计算净现金头寸（福特83.5亿美元算例）
  type: calculation
  source_chapter: 第12章 12.7（L2705-2715，表12-1/12-2 L2645-2774）
  source_quote: |
    "从101亿美元的现金头寸中减去17.5亿美元的长期债务，等于83.5亿美元，这就是福特公司的净现金头寸……我只是假定公司的其他资产（存货等）足以抵消短期债务。"
  summary: |
    口径：现金头寸=现金及现金等价物+有价证券（福特1987：56.729亿+44.241亿≈101亿）；净现金头寸=现金头寸-长期债务（101-17.5=83.5亿）；简化处理忽略短期债务（假定存货等其他资产足以抵偿）。现金总额高于债务总额→不论发生什么都不会破产。83.5亿÷5.11亿股=每股净现金16.30美元。核查表12-2十年数据：现金逐年增+长期债务减+流通股逐年减（回购）均为业务兴旺信号。
  inputs: [现金及现金等价物, 有价证券, 长期债务, 流通股数]
  formula: "净现金头寸 = (现金及等价物 + 有价证券) - 长期债务；每股净现金 = 净现金头寸 ÷ 流通股数"
  units: 百万美元 / 美元每股
  output: 净现金头寸与每股净现金（福特=83.5亿美元 / 16.30美元）
  missing_conditions: 简化口径忽略短期债务，前提是公司有足够现金偿还短期负债；未扣除表外义务
  tags: [balance-sheet, cash-position, calculation, ford-case]
  task_ids: [task-06]

- id: pB26
  title: 现金增长超过负债增长=资产负债表改善；回购=利好
  type: rule
  source_chapter: 第12章 12.7（L2707-2715）
  source_quote: |
    "当现金相对于债务出现增长时，即现金增长超过负债增长时，这表明公司资产负债表得到了改善。如果情况相反，则表明公司资产负债表进一步恶化。"
  summary: |
    两个年报信号：①现金增+债务减=财务实力改善（反之恶化）；②流通股逐年减少=公司在回购股票（利好）。多数公司长期债务大于现金、现金减债务增=财务实力变弱。可用《价值线》替代自查（含财务实力1-5级评级；其买股时机评级作者不看）。
  tags: [balance-sheet, buyback, signal, rule]
  task_ids: [task-06, task-03]

# ── 第13章 13项财务分析指标（L2798-3182）──────────────────────────

- id: pB27
  title: 指标1｜产品销售额占总销售额的比例
  type: calculation
  source_chapter: 第13章 13.1（L2802-2806）
  source_quote: |
    "这种产品的销售额占公司总销售额的百分比是多少？L'eggs连裤袜使得Hanes公司的股票上涨了很多……帮宝适牌纸尿裤的利润比L'eggs更大，但是这对于规模庞大的宝洁公司的影响却远远没有……那么大。"
  summary: |
    因某热门产品对公司产生兴趣时，先算该产品销售额（利润）占公司总销售额的比重：材料事业部仅占GE总销售收入6.8%→Lexan树脂再畅销对GE股东意义也不大。占比太小则另找该产品的纯生产者或干脆忘掉。
  inputs: [该产品销售额, 公司总销售额]
  formula: "产品占比 = 产品销售额 ÷ 公司总销售额 × 100%"
  units: %
  output: 产品重要性判断（买该公司还是找替代标的）
  missing_conditions: 无统一阈值，需与公司体量相对判断
  tags: [financial-metric, product-mix, calculation, pampers-fallacy]
  task_ids: [task-06, task-13]

- id: pB28
  title: 指标2｜定价合理则P/E=收益增长率；一半偏便宜、两倍危险
  type: calculation
  source_chapter: 第13章 13.2（L2810-2816）
  source_quote: |
    "任何一家公司股票如果定价合理的话，市盈率就会与收益增长率相等……如果一家公司的股票市盈率只有收益增长率的一半，那么这只股票赚钱的可能性就相当大；如果股票市盈率是收益增长率的两倍，那么这只股票亏钱的可能就非常大。"
  summary: |
    P/E与增长率比较法：定价合理→P/E≈年收益增长率（可口可乐15倍P/E应预期15%增长）；P/E<增长率=被低估（12%成长股配6倍P/E很吸引人）；P/E只有增长率一半→赚钱可能相当大；P/E是两倍→亏钱可能非常大。麦哲伦选股一直使用该指标。增长率数据来源：经纪人/《价值线》/标普报告。
  inputs: [股票市盈率, 公司年收益增长率]
  formula: "比较 P/E 与 g：P/E ≈ g 合理；P/E ≈ g/2 便宜；P/E ≈ 2g 危险"
  units: 倍 vs %
  output: 低估/合理/高估判定
  missing_conditions: 增长率须为可持续的正常年份收益增长率；周期股利润波动使该法失真（作者自认）；50-100%的超高增长率不可持续
  tags: [pe-ratio, growth-rate, calculation, core-rule]
  task_ids: [task-05, task-06]

- id: pB29
  title: 指标2b｜(增长率+股息率)÷市盈率 评分公式（≥1.5不错，≥2最佳）
  type: calculation
  source_chapter: 第13章 13.2（L2818-2820）
  source_quote: |
    "我们首先要找到公司收益的长期增长率（假定……12%），然后加上股息收益率（……3%），最后除以市盈率（……10），12加上3再除以10等于1.5……你真正要找的是公司收益增长率相当于市盈率的2倍或者更高的股票。"
  summary: |
    考虑股息的精炼公式：(长期收益增长率%+股息收益率%)÷P/E。结果<1=较差；=1.5=不错；≥2=真正要找的；例：15%+3%÷6倍=3倍="真是太棒了"。
  inputs: [收益长期增长率%, 股息收益率%, 市盈率]
  formula: "得分 = (g + 股息率) ÷ P/E"
  units: 无量纲比值
  output: 股票吸引力得分（<1差，1.5不错，≥2最佳）
  missing_conditions: 需有稳定派息记录的公司；不派息公司退化为 pB28 的 P/E vs g 比较
  tags: [pe-ratio, dividend-yield, calculation, scoring]
  task_ids: [task-05, task-06]

- id: pB30
  title: 指标3｜每股净现金暗含买入折扣（福特16.30美元→实际买价21.70）
  type: calculation
  source_chapter: 第13章 13.3（L2824-2834）
  source_quote: |
    "我买入股票的真正价格并不是当前的市价每股38美元，而是每股21.70美元（38美元减去16.30美元等于21.70美元）……用21.70美元的实际股价计算出来的市盈率是3.1倍。"
  summary: |
    每股净现金=买入价的暗含折扣：福特市价38美元-每股净现金16.30=实际买价21.70美元；按汽车业务每股收益7美元，P/E从5.4倍降至3.1倍→决不卖出，后来又涨40%+。延伸：金融子公司每股收益1.66美元×10倍行业P/E=16.60美元；38-16.30-16.60=仅5.10美元买入汽车业务（对应7美元收益）。现金因素可作为继续持有/买入的决定性证据。
  inputs: [股价, 每股净现金, 分部每股收益, 分部行业平均P/E]
  formula: "实际买价 = 股价 - 每股净现金（- 被低估分部估值）；调整后P/E = 实际买价 ÷ 业务每股收益"
  units: 美元每股 / 倍
  output: 调整后真实买入成本与P/E（福特：21.70美元/3.1倍；含金融分部：5.10美元）
  missing_conditions: 现金要按流通股本摊到每股才有意义；公司可能把现金浪费在愚蠢并购上（需核查管理层资金运用）
  tags: [cash-position, calculation, ford-case, valuation]
  task_ids: [task-06]

- id: pB31
  title: 指标3b｜每股现金的影响力取决于股价高低
  type: rule
  source_chapter: 第13章 13.3（L2844-2846）
  source_quote: |
    "百时美账上拥有16亿美元的现金……平均每股净现金只有5美元。每股5美元的净现金对于每股超过40美元的股价而言并没有太大的影响力。如果它的股价跌到15美元……就非常便宜了。"
  summary: |
    现金多寡本身不代表投资价值：必须除以总股本看每股净现金，再相对股价衡量（百时美每股5美元 vs 40美元股价无影响，vs 15美元股价影响巨大；Schlumberger大量现金摊薄后不值一提）。但作为研究例行步骤，现金头寸检查永远必要——不知何时会碰上福特式的便宜货。
  tags: [cash-position, rule, per-share]
  task_ids: [task-06]

- id: pB32
  title: 指标4｜负债权益比：股东权益75%/负债25%为正常线
  type: calculation
  source_chapter: 第13章 13.4（L2854-2860）
  source_quote: |
    "一份正常的公司资产负债表中，股东权益应占到75%，而负债要少于25%。福特公司的股东权益与负债的比率是180亿美元比17亿美元……负债仅占1%而股东权益占99%，那么……财务实力更加强大；相反……负债高达80%而股东权益仅占20%……十分虚弱。"
  summary: |
    快捷判断财务实力=比较资产负债表右边负债与股东权益谁多：75/25为正常；福特184.92亿权益:17.5亿长期债≈91%/10%（忽略短期债务的简化）=非常强大；99/1更强大；80/20=十分虚弱。算法：负债权益比率（debt-to-equity）。
  inputs: [股东权益总额, 长期负债（短期负债在现金充足时可忽略）]
  formula: "负债占比 = 长期负债 ÷ (长期负债 + 股东权益)；正常线：权益75%/负债25%"
  units: %
  output: 财务实力量级（正常/强大/虚弱）
  missing_conditions: 大致估算口径，忽略短期债务的前提是现金足以偿短债
  tags: [financial-metric, debt-equity, calculation, ford-case]
  task_ids: [task-06]

- id: pB33
  title: 指标4b｜银行短期负债最危险，长期负债最安全
  type: rule
  source_chapter: 第13章 13.4（L2872-2876）
  source_quote: |
    "短期负债（最差的一类负债……）是债权人提出要求时必须马上偿还的负债……长期负债（从股东的观点来看，这是最好的一类负债）的债权人就不能马上收回借款……长期负债给公司提供了充裕的时间来解决问题走出困境。"
  summary: |
    负债种类与数额同等重要：短期负债/bank debt（银行贷款、商业票据）对方一要求就得偿还，还不上即进破产法11章，清算后股东一分不剩；长期负债/funded debt（长期债券）15-30年固定到期、只要付息就不能逼债，给困境公司喘息时间。GCA（负债1.14亿几乎全是银行贷款+现金仅300万）破产 vs 应用材料（负债1700万+现金3600万）反弹4倍+；Micron靠可转债换掉短期贷款而幸存。
  tags: [debt-structure, rule, distress, bank-debt]
  task_ids: [task-06]

- id: pB34
  title: 指标4c｜困境反转型公司先查负债数量与结构
  type: rule
  source_chapter: 第13章 13.4（L2862, L2878-2882）
  source_quote: |
    "在危机之时，是负债而不是其他任何因素最终决定公司是否能够幸免于难还是破产倒闭……我不但特别注意公司的负债数量，并且特别注意公司的负债结构。"
  summary: |
    评估困境反转型（如克莱斯勒）必查：负债多少、是短债还是长债、账上现金多少（克莱斯勒10亿现金+卖坦克分部3.36亿+政府14亿贷款担保=一两年内银行逼不死）。危机中决定存亡的是负债，不是其他任何因素。
  tags: [debt-structure, turn-around, rule, chrysler-case]
  task_ids: [task-06, task-01]

- id: pB35
  title: 指标5｜派息股票更抗跌
  type: principle
  source_chapter: 第13章 13.5（L2904）
  source_quote: |
    "1987年股票市场崩溃时，派发高股息的股票的表现要比不派发股息的股票好得多，其跌幅还不到整个股市跌幅的一半。"
  summary: |
    派息股票的抗跌机制：20美元股价2美元股息=10%股息率，跌到10美元则股息率20%，确定能维持的 高股息率会在底部形成股价支撑；危机中投资者蜂拥买长期派息的蓝筹股。这是组合里保留稳定/缓慢增长型股票的理由之一。
  tags: [dividend, defensive, principle]
  task_ids: [task-06, task-11]

- id: pB36
  title: 指标5b｜换股规则：慢派息老公司→快不派息新公司
  type: rule
  source_chapter: 第13章 13.5（L2906）
  source_quote: |
    "不论何时只要有机会我都会把我的投资组合中那些派发股息却发展缓慢的老公司的股票换成不派发股息却发展迅速的新公司的股票。"
  summary: |
    小公司不派息反而增长更快（留存资金扩张）。有换股机会时，用"派息但缓慢的老公司"换"不派息但快速的新公司"。（与pB102换股不换现金配合使用。）
  tags: [dividend, rotation, rule]
  task_ids: [task-11, task-06]

- id: pB37
  title: 指标6｜股息核查：二三十年定期提高股息的记录是最佳选择
  type: rule
  source_chapter: 第13章 13.6（L2963-2967）
  source_quote: |
    "一家有着二三十年定期提高股息历史记录的公司是你的最佳投资选择。Kellogg公司和Ralston Purina公司在过去的三次战争和八次经济衰退中都没有降低过股息。"
  summary: |
    为股息买股的核查标准：①衰退期与经营糟糕期是否仍能支付股息（Fleet-Norstar自1791年从未中断）；②二三十年定期提高股息的记录；③缓慢增长型公司停止派息=大麻烦（几乎无多余资金）；④重债公司（Southmark 11→3美元后停息）无法像轻债的百时美那样保证派息；⑤周期型股息不可依赖（福特1982停息、股价<4美元，但现金未尽则股息终会补回）。
  tags: [dividend, checklist, rule, slow-grower]
  task_ids: [task-06, task-08]

- id: pB38
  title: 指标7｜账面价值经常严重失真，勿按账面价值买股
  type: rule
  source_chapter: 第13章 13.7（L2969-2989）
  source_quote: |
    "只根据公司财务报表中的每股账面价值来购入股票是非常危险的……账面价值为86.6万美元的织布机最后在拍卖中只卖了16.3万美元。"
  summary: |
    账面价值与实际价值常无关系：佩恩中央破产时账面仍60+美元/股；艾伦伍德钢铁账面40美元/股6个月后破产（新炼钢设施账面3000万实不可用，500万贱卖）；巴菲特织布机账面86.6万拍卖仅16.3万（5000美元/台买、26美元/台卖，低于运费）；Radice每股账面50美元股价10美元，但房地产会计把利息资本化入资产，真实价值每股-7美元→跌到75美分不回头。负债真实+资产高估=负账面价值比一文不值更糟。
  tags: [book-value, trap, rule, counter-case]
  task_ids: [task-06, task-10]

- id: pB39
  title: 指标7b｜产品越接近最终制成品，再售价越难预测
  type: principle
  source_chapter: 第13章 13.7（L2977）
  source_quote: |
    "产品越接近于最终制成品，制造出成品以后再次出售的价格越难以预测。大家都知道棉花的价格是多少，但是谁也无法确定一件橙色纯棉衬衫的价格会是多少。"
  summary: |
    资产清算价值的可预测规律：原材料（棉花、金属块）价格可知，越加工越接近成品的资产（衬衫、落地灯）变现价越不可测。评估账面资产真实价值时按此规律打折。
  tags: [book-value, asset-liquidity, principle]
  task_ids: [task-06]

- id: pB40
  title: 指标8｜隐蔽资产类型清单（九类）
  type: checklist
  source_chapter: 第13章 13.8（L2993-3041）
  source_quote: |
    "公司拥有的自然资源，例如土地、木材、石油或者贵金属的入账价值往往只有其真实价值的一小部分……获得专利权的药品、有线电视的特许经营权、电视和广播电台也同样如此。"
  summary: |
    隐蔽资产九类：①自然资源（土地/木材/石油/贵金属，按30年前成本入账；Handy&Harman存货账面7.83 vs 现价19美元/股）；②品牌（可口可乐、Robitussin）；③专利药（17年独占，账面可能为零）；④有线电视特许权/电视台（第五频道账面250万售4.5亿=低估300倍）；⑤商誉摊销掩盖的真实收益（可口可乐灌装1987报告63美分+被摊销50美分；孟山都纽特阿斯巴甜）；⑥研发费用冲销（研发停止后收益爆炸）；⑦母公司旗下的低估子公司（UAL：希尔顿10亿+赫兹13亿+威斯汀14亿+订票系统10亿>总市值）；⑧持有其他公司股份（雷蒙德12美元含18美元Teleco；Seagram含杜邦25%；Beard 8美元含12美元USPCI）；⑨税收亏损抵扣（佩恩50%税率下收购标的税后利润一夜翻倍；伯利恒钢铁10亿经营亏损抵扣）。
  tags: [hidden-asset, checklist, asset-type]
  task_ids: [task-06, task-01]

- id: pB41
  title: 指标9｜现金流量：10:1为正常比、10%现金收益率是底线、必须用自由现金流
  type: calculation
  source_chapter: 第13章 13.9（L3045-3053）
  source_quote: |
    "如果一只股票为每股20美元，每股现金流量是2美元，那么它的市价现金流量比率就是10:1，这是一个正常水平的标准比率。10%的现金收益率相当于长期持有股票的最低收益率。"
  summary: |
    现金流量估值口径：股价20美元/每股现金流2美元=10:1正常；现金收益率10%是长期持有的最低标准；20%很棒（20美元股价4美元现金流）；10美元现金流则"抵押房屋全押"。关键限定：一定要用自由现金流量（扣除正常资本支出后的现金）——生铁公司流入1亿必须投8000万更新高炉 vs 菲利普·莫里斯不必。喜欢不依赖资本支出的公司。
  inputs: [股价, 每股现金流量, 每股资本支出]
  formula: "市价现金流量比 = 股价 ÷ 每股(自由)现金流量；现金收益率 = 每股(自由)现金流量 ÷ 股价"
  units: 比值 / %
  output: 现金收益率（≥10%及格，20%很棒，50%全押级）
  missing_conditions: 必须为自由现金流量口径（扣资本支出）；不同行业资本密集度差异大，需同行业比较
  tags: [cash-flow, free-cash-flow, calculation]
  task_ids: [task-06]

- id: pB42
  title: 指标9b｜高自由现金流+无意扩张=隐蔽资产型机会（海岸公司算例）
  type: rule
  source_chapter: 第13章 13.9（L3055-3061）
  source_quote: |
    "专注的隐蔽资产型公司投资者都在寻找这样的投资良机：一家普普通通的公司，看起来根本没有什么发展前途，但是每年都拥有很高的自由现金流量，而公司股东却并不打算进一步扩大业务规模。"
  summary: |
    模式：收益一般但自由现金流极高的公司。海岸公司P/E 8倍、每股收益2.50美元看似平庸，但每股现金流10-11美元、扣除资本支出后自由现金流7美元/股；20美元买入未来10年回收70美元。收缩榨取型（租赁公司12年集装箱逐步停业）同样适用；电脑业除外（存货贬值太快）。
  inputs: [每股现金流量, 每股资本支出, 股价, 预期持有年数]
  formula: "年自由现金流 = 现金流量 - 资本支出；n年回收额 = 年自由现金流 × n"
  units: 美元每股
  output: 长期现金回收总额 vs 股价（海岸：7×10=70美元 vs 20美元）
  missing_conditions: 前提是公司确无大额再投资需求且不把现金挥霍于并购
  tags: [free-cash-flow, hidden-asset, calculation, coastal-case]
  task_ids: [task-06]

- id: pB43
  title: 指标10｜存货增速超过销售增速=危险信号
  type: rule
  source_chapter: 第13章 13.10（L3065-3077）
  source_quote: |
    "当存货增长速度比销售增长速度更快时，这就是一个十分危险的信号了……一家公司可能会吹嘘说它的销售额增长了10%，但是如果它的存货同时增长了30%，那么你就必须提醒自己……"
  summary: |
    年报"管理层关于收益的讨论与分析"中存货附注必读。销售额增10%而存货增30%→积压→明年更糟→新老产品自相杀价→降价→利润下降。存货计价LIFO/FIFO不同方法会改变利润（Handy&Harman 450美元卖金：LIFO利润50 vs FIFO利润410），但同一方法下今年末vs去年末同比有效。季报均公布资产负债表，可按季跟踪。耐用品积压后果较轻（美洲虎35000美元不会降到3500，紫色迷你裙300→3仍卖不掉）。
  tags: [inventory, warning-signal, rule, calculation]
  task_ids: [task-06, task-08]

- id: pB44
  title: 指标10b｜不景气公司存货开始减少是经营好转的第一个信号
  type: rule
  source_chapter: 第13章 13.10（L3079）
  source_quote: |
    "如果一家经营状况不景气的公司存货开始逐步减少，那么这应该是公司经营情况好转的第一个信号。"
  summary: |
    反向信号：困境公司存货逐步下降=好转的第一信号。与pB43构成存货双向观察。行业熟悉者可自行判断存货对收益的影响，新手可按季报资产负债表跟踪。
  tags: [inventory, turn-around-signal, rule]
  task_ids: [task-06, task-09]

- id: pB45
  title: 指标11｜养老金核查：基金资产必须超过既定福利义务
  type: rule
  source_chapter: 第13章 13.11（L3085-3089）
  source_quote: |
    "我特别要查看公司的养老基金资产是否超过了应付给员工的既定养老金福利义务……伯利恒钢铁公司的养老金资产为23亿美元，既定的养老金义务为38亿美元……应该调低对这家公司股票的估值。"
  summary: |
    养老金计划义务如必须偿付的债券，公司破产停业仍须支付。买困境反转型股票前必查：养老基金资产vs既定福利义务。USX 85亿资产:73亿义务=不必担心；伯利恒钢铁23亿:38亿=15亿赤字，财务再恶化会雪上加霜→估值调低。养老金情况现在年报公开披露。
  inputs: [养老基金资产, 既定养老金福利义务]
  formula: "养老金盈余 = 基金资产 - 既定义务（正=安全，负=调低估值）"
  units: 亿美元
  output: 养老金缺口判断
  missing_conditions: 需区分既定义务(vested)与非既定义务；利润分享计划无此义务
  tags: [pension, distress, rule, calculation]
  task_ids: [task-06]

- id: pB46
  title: 指标12｜唯一能够影响股价的增长率是收益增长率；20% vs 10%十年差2.4倍
  type: calculation
  source_chapter: 第13章 13.12（L3093-3137，表13-1）
  source_quote: |
    "唯一能够影响股价的增长率是：收益增长率……假设开始时两家公司的每股收益都是1美元……（表13-1：A公司20%第10年6.19美元，B公司10%第10年2.59美元）"
  summary: |
    行业增长≠公司增长（菲利普·莫里斯靠降本+提价在萎缩的香烟行业年增收益；美国消费量每年-2%）。复利算例（表13-1）：同为1美元起点，20%增长10年→6.19美元，10%→2.59美元；20倍P/E下股价20→123.80美元（B仅10→26美元）；即使A的P/E从20降到15仍值92.85美元。不采用30%+估算（高增长率难持续3年更难10年）。20%（P/E 20倍）优于10%（P/E 10倍）。
  inputs: [基年每股收益, 年收益增长率, 市盈率, 年数]
  formula: "第n年EPS = EPS₀ × (1+g)^n；股价 = EPS × P/E（表13-1：1.00×1.2^10=6.19；1.00×1.1^10=2.59）"
  units: 美元
  output: 长期收益与股价差（A 123.80 vs B 26美元；P/E降到15时A仍92.85）
  missing_conditions: 20-25%是可持续上限经验值；50-100%增长率不可外推
  tags: [growth-rate, compounding, calculation, core-rule]
  task_ids: [task-06, task-05]

- id: pB47
  title: 指标12b｜能年年提价而不失客户的公司=非常好的投资机会
  type: rule
  source_chapter: 第13章 13.12（L3099）
  source_quote: |
    "如果你发现了一家每年都能找到合理的办法提高产品价格同时又不会损失客户的公司（像香烟这种让人上瘾的产品就非常符合这种要求），你就找到了一个非常好的投资机会。"
  summary: |
    提价能力是最优增长动力（服装/快餐业绝不可能）。配套口径：成本增4%+售价提6%→利润率+2%；利润率10%的公司收益因此增长20%（2%÷10%=20%）。宝洁卫生纸"挤压技术"减张数500→350是变相提价。
  tags: [pricing-power, rule, earnings-growth]
  task_ids: [task-06, task-03]

- id: pB48
  title: 指标12c｜利润率增幅换算收益增幅
  type: calculation
  source_chapter: 第13章 13.12（L3095）
  source_quote: |
    "如果一家烟草公司的成本增加4%，同时销售价格提高6%，那么公司的利润率就会增加2%……如果公司的利润率是10%……那么利润率增加2%则意味着公司收益将会增长20%（2%÷10%=20%）。"
  summary: |
    换算：售价涨幅-成本涨幅=利润率增幅；收益增长率=利润率增幅÷原利润率。适用于评估"降本提价"型公司的收益弹性。
  inputs: [售价涨幅%, 成本涨幅%, 原利润率%]
  formula: "收益增长率 = (售价涨幅 - 成本涨幅) ÷ 原利润率"
  units: %
  output: 收益增长率（例：(6%-4%)÷10%=20%）
  missing_conditions: 假定销量不变；利润率基数极低时结果放大失真
  tags: [margin-math, calculation, pricing-power]
  task_ids: [task-06]

- id: pB49
  title: 指标13｜税前利润率：同行业比较；长期持有选高、复苏期选低
  type: rule
  source_chapter: 第13章 13.13（L3141-3151, L3182）
  source_quote: |
    "如果你决定不管行业是否景气都打算长期持有一只股票，那么你就应该选择一家税前利润率相对较高的公司；如果你打算在行业成功复苏阶段持有一只股票，你应该选择一家税前利润率相对较低的公司。"
  summary: |
    税前利润率=（销售收入-全部成本含折旧利息）÷销售收入（福特1987：73.8亿/716亿=10.3%；零售商Albertson's仅3.6%；默克25%+）。行业间比较无意义，同行业内比较：利润率最高=成本最低=行业不景气时存活机会最大（A 12% vs B 2%同样降价10%：A剩2%仍赚、B变-8%）。选股规则见quote。
  tags: [pretax-margin, rule, industry-comparison]
  task_ids: [task-06]

- id: pB50
  title: 指标13b｜复苏期低利润率公司弹性最大（表13-2：+47% vs +255%）
  type: calculation
  source_chapter: 第13章 13.13（L3153-3180，表13-2）
  source_quote: |
    "在业务恢复好转的过程中，A公司的税前利润增长了将近50%，而B公司的税前利润则增长了3倍还要多，这可以解释为什么原来处于灾难边缘的不景气公司在业务反弹时能够摇身一变为一只大黑马股票。"
  summary: |
    表13-2算例：销售收入100→110（+10%）、成本+5%时，A公司（成本88→92.40，利润12→17.60，+47%）vs B公司（成本98→102.90，利润2→7.10，+255%）。低利润率公司在行业复苏（汽车、化工、造纸、航空、钢铁、电子、非铁材料反复上演；当下疗养院/天然气/零售）中是最大黑马。公众普遍高估公司利润率（猜20-40%，实际平均仅5%左右）。
  inputs: [销售收入, 成本, 复苏后售价涨幅, 复苏后成本涨幅]
  formula: "利润 = 收入 - 成本；弹性 = Δ利润 ÷ 原利润（B：5.10÷2=255%）"
  units: 美元 / %
  output: 复苏期利润弹性对比
  missing_conditions: 需行业整体好转前提；利润率过低的公司在好转前可能先倒闭（存活是前提）
  tags: [pretax-margin, recovery, calculation, table-13-2]
  task_ids: [task-06]

# ── 第14章 定期重新核查（L3194-3232）──────────────────────────

- id: pB51
  title: 每隔几个月重新核查公司基本面
  type: checklist
  source_chapter: 第14章（L3196）
  source_quote: |
    "每隔几个月就应该重新核查一下你的公司基本面分析。重新核查包括翻阅最新的《价值线》杂志或者公司的季度报表看看公司的收益情况以及收益变化情况是否和你原来的预期相符。"
  summary: |
    复查内容：①最新《价值线》/季报的收益与预期是否相符；②去商店实地看产品是否仍具吸引力；③有无新情况（玩梭哈翻开新牌）；④快速增长型公司必问"如何才能保持收益继续快速增长"。
  tags: [periodic-review, checklist, discipline]
  task_ids: [task-09]

- id: pB52
  title: 增长型公司生命周期三阶段模型
  type: principle
  source_chapter: 第14章（L3198-3202）
  source_quote: |
    "第一阶段是创业期……第二阶段是快速扩张期……第三阶段是成熟期，也叫饱和期……第一阶段风险最大……第二阶段则最安全，并且也是赚钱最多的时期……第三阶段最容易出现问题。"
  summary: |
    三阶段：创业期（解决基本业务缺陷，风险最大）→快速扩张期（复制成功开拓新市场，最安全+赚钱最多）→成熟饱和期（增长接近上限，最易出问题，需找新增长方法）。每阶段持续数年。复查时必须确定公司正处在哪个阶段、是否正在换阶段：Sensormatic进入成熟期后42.5→5.625美元；The Limited开遍670/700家购物中心=增长尽头；麦当劳靠得来速窗口（占收入1/3+）、早餐（+20%销售）、沙拉炸鸡、海外扩张在成熟期再造增长，P/E从30倍落回12倍后收益仍增。
  tags: [growth-stage, lifecycle, principle, core-model]
  task_ids: [task-09, task-01]

- id: pB53
  title: 勿沉醉于业务好转的消息而忽视实际经营恶化（得州航空教训）
  type: rule
  source_chapter: 第14章（L3218-3232）
  source_quote: |
    "我沉醉于……拥有如此巨大的盈利潜力，以至于忘了去查看它们近期的实际经营状况……我只把目光停留在1988年得克萨斯航空公司每股收益高达15美元的预期上，却忽视了报纸每天所刊登的对该公司的负面报道发出的警告信号。"
  summary: |
    教训：未来每股收益预期不能代替对当前实际经营状况的检查；负面报道信号（行李丢失、航班混乱、晚点、乘客发怒、劳资纠纷）累积时必须行动。配套行动：卖出恶化的公司，用基本面分析抓住受益的竞争对手（东方航空出问题→应重仓Delta）。航空/餐饮业的不稳定性：几个晚上的失误可毁50年美誉。
  tags: [review-discipline, counter-case, rule, texas-air]
  task_ids: [task-09, task-02, task-10]

# ── 第15章 分类型核查清单（L3234-3330）──────────────────────────

- id: pB54
  title: 核查清单｜所有类型公司通用六项
  type: checklist
  source_chapter: 第15章 15.1.1（L3242-3254）
  source_quote: |
    "·市盈率……·机构投资者持股占该公司总股本的比例。机构投资者持股比例越低越好。·公司内部人士是否在买入本公司股票？公司是否回购自己的股票？……·现金头寸。福特汽车公司每股净现金为16美元……每股净现金是公司股票价格的底部下限。"
  summary: |
    通用六项：①P/E高低（vs 同行业类似公司）；②机构持股占总股本比例（越低越好）；③内部人士买入+公司回购（均为有利信号）；④收益增长历史（时断时续还是持续稳定；仅隐蔽资产型可不太在意收益）；⑤资产负债情况（负债/权益比）与财务实力评级；⑥现金头寸——每股净现金=股价底部下限（福特16美元→股价不可能跌破16美元）。
  tags: [checklist, universal, core-tool]
  task_ids: [task-08, task-06]

- id: pB55
  title: 核查清单｜缓慢增长型公司（股息专项）
  type: checklist
  source_chapter: 第15章 15.1.2（L3256-3260）
  source_quote: |
    "由于你购买这类公司股票的目的是为了获得股息……所以你应该核查一下这类公司是否长期持续派发股息以及是否能够定期提高股息水平……如果股息占收益的比率比较低，那么这家公司在经营困难时期仍有缓冲资金……"
  summary: |
    两项：①是否长期持续派息+定期提高股息；②股息占收益的比率——比率低=困难期有缓冲资金能保证派息；比率高=股息能否顺利派发相当危险。
  tags: [checklist, slow-grower, dividend]
  task_ids: [task-08, task-01]

- id: pB56
  title: 核查清单｜稳定增长型公司（买入价格专项）
  type: checklist
  source_chapter: 第15章 15.1.3（L3262-3270）
  source_quote: |
    "这类公司都是几乎不可能破产倒闭的大公司，因此关键因素在于买入价格的高低，股票的市盈率会告诉你股价是否过高。"
  summary: |
    四项：①关键在买入价格，P/E判断是否过高；②检查多元化经营情况（可能导致未来收益下降）；③收益长期增长率+近几年是否保持同样势头；④打算永久持有则看衰退期与股市大跌期表现（麦当劳1977好/1984横盘/1987遭打击但整体是不错的防御型股票；百时美1973-74重创系高估所致，1982/84/87都好；Kellogg除1973-74外所有大跌中表现良好）。
  tags: [checklist, stable-grower, entry-price]
  task_ids: [task-08, task-05]

- id: pB57
  title: 核查清单｜周期型公司（存货与周期专项）
  type: checklist
  source_chapter: 第15章 15.1.4（L3272-3282）
  source_quote: |
    "当公司业绩复苏时应该预测到市盈率将会降低，当公司收益会达到最高峰时投资者应该预期到公司增长周期可能即将结束。"
  summary: |
    要点：①密切关注存货变化与供需平衡；②新竞争对手进入=危险信号；③业绩复苏时P/E会降低（周期股低P/E反而危险）；收益最高峰=周期将近结束；④了解行业周期者有预测优势（汽车业三四年扩张后三四年衰退，人必换车）；⑤下滑越厉害，反弹越强（销售低迷比预期多延长一年→反弹时间更长幅度更大）；⑥周期行业中预测上涨远比预测下降容易。
  tags: [checklist, cyclical, inventory, pe-inversion]
  task_ids: [task-08, task-01, task-05]

- id: pB58
  title: 核查清单｜快速增长型公司（增长质量专项）
  type: checklist
  source_chapter: 第15章 15.1.5（L3284-3298）
  source_quote: |
    "我最喜欢那些增长率处于20%～25%之间公司的股票，我反而对那些看起来能够保持高于25%的收益增长率的公司十分担心……公司股票市盈率是否等于或接近于公司收益增长率。"
  summary: |
    七项：①看好的产品销售额占公司总收入的比重（L'eggs之于Hanes大 vs Lexan之于GE小）；②收益增长率20-25%最理想、>25%担心、热门行业50%+必须怀疑；③已在一个以上城市/乡镇成功复制经营模式；④剩余增长空间（Pic 'N' Save还有49个州 vs 西尔斯已遍布全美）；⑤P/E=或≈收益增长率；⑥扩张速度在加快（去年3家今年5家）还是放慢（去年5家今年3家）；一次性销售型公司（Sensormatic）销售放缓是毁灭性的 vs 剃须刀重复购买型；⑦机构投资者与分析师极少关注=低价买入的有利因素。
  tags: [checklist, fast-grower, growth-quality]
  task_ids: [task-08, task-01, task-03]

- id: pB59
  title: 核查清单｜困境反转型公司（生存能力专项）
  type: checklist
  source_chapter: 第15章 15.1.6（L3300-3318）
  source_quote: |
    "最重要的是，一家困境反转型公司在经营困难时期能否经受住债权人要求还款的打击而存活下来？公司拥有多少现金？多少债务？（苹果电脑公司在面临经营危机时拥有2亿美元的现金，没有一分钱的债务，因此你知道它肯定不会破产。）"
  summary: |
    要点：①能否扛住债权人还款打击：现金多少/债务多少/债务结构；赔本状态下还能经营多久（苹果2亿美元现金零债务=不会破产）；②已宣布破产的：清算偿债后还给股东留多少资产；③重整计划：剥离赔钱子公司使收益大变（洛克希德停产L-1011一次性冲销后EPS从1.50→10.78美元，4年15→60美元；德州仪器弃家用电脑次日101→124美元，4个月176美元）；④业务正在好转吗（柯达胶卷重新火爆）；⑤削减成本及效果（克莱斯勒关厂+外包变最低成本厂商）。增发数百万新股筹资可使公司复苏但不能使股价反弹（国际收割机/Navistar）。
  tags: [checklist, turn-around, survival]
  task_ids: [task-08, task-01]

- id: pB60
  title: 核查清单｜隐蔽资产型公司（资产价值专项）
  type: checklist
  source_chapter: 第15章 15.1.7（L3320-3328）
  source_quote: |
    "·公司的资产价值是多少？公司有隐蔽资产吗？·公司有多少债务需要从这些资产中扣除掉？……·是否有袭击并购者对公司感兴趣准备收购公司？"
  summary: |
    四项：①资产价值多少、有无隐蔽资产；②需从资产中扣除的债务有多少（首先关注向债权人的借款）；③是否正在借入新债务使资产价值进一步减少；④有无袭击并购者感兴趣准备收购（帮股东实现隐蔽资产重估升值）。
  tags: [checklist, hidden-asset, asset-value]
  task_ids: [task-08, task-01]

# ── 第15章 15.2 本部分要点（L3330-3394，逐条32条）─────────────

- id: pB61
  title: 要点｜真正了解所持公司的业务与持股理由
  type: principle
  source_chapter: 第15章 15.2（L3332）
  source_quote: "真正了解你所持股公司的业务情况，真正清楚你持有这家公司股票的具体理由（'它肯定会上涨！'根本算不上什么理由）。"
  summary: 持股必须有可陈述的具体理由，"肯定会涨"不是理由。
  tags: [principle, know-what-you-own]
  task_ids: [task-07, task-09]

- id: pB62
  title: 要点｜弄清股票类型才知道合理预期
  type: principle
  source_chapter: 第15章 15.2（L3334）
  source_quote: "弄清楚你所持有的股票属于什么类型，这样你将会更清楚地了解你对投资回报的合理预期应该是多少。"
  summary: 六类型归类是设定收益预期的前提。
  tags: [principle, company-type]
  task_ids: [task-01]

- id: pB63
  title: 要点｜大公司涨幅小、小公司涨幅大
  type: principle
  source_chapter: 第15章 15.2（L3336）
  source_quote: "大公司的股票往往涨幅不会太大，而小公司的股票往往涨幅很大。"
  summary: 公司体量与股价涨幅成反比的经验规律。
  tags: [principle, size-effect]
  task_ids: [task-01, task-03]

- id: pB64
  title: 要点｜热门产品必须算销售收入占比
  type: rule
  source_chapter: 第15章 15.2（L3338）
  source_quote: "如果你预测某家公司能够从某一种特定产品获利的话，那么你应该考虑一下公司总销售收入的规模，计算一下这种产品销售收入在公司总收入中所占的比重。"
  summary: 与pB27同源：产品热度→股票涨幅的换算必经总销售收入占比。
  tags: [rule, product-mix, pampers-fallacy]
  task_ids: [task-13, task-06]

- id: pB65
  title: 要点｜寻找已盈利且证明能异地复制经营理念的小公司
  type: rule
  source_chapter: 第15章 15.2（L3340）
  source_quote: "寻找那些已经盈利并且事实证明它们能够在其他地方复制其经营理念取得成功的小公司。"
  summary: 与pB14同源：已盈利+异地复制已证明=快速增长型的买入前提。
  tags: [rule, fast-grower, replication]
  task_ids: [task-03, task-07]

- id: pB66
  title: 要点｜小心年收益增长率50%-100%的公司
  type: rule
  source_chapter: 第15章 15.2（L3342）
  source_quote: "特别要小心那些年收益增长率高达50%～100%的公司，一定要用怀疑的眼光进行分析。"
  summary: 超高增长率不可持续，须怀疑审视（与pB58增长率20-25%理想区间呼应）。
  tags: [rule, growth-quality, red-flag]
  task_ids: [task-03, task-08]

- id: pB67
  title: 要点｜远离热门行业中的热门股
  type: rule
  source_chapter: 第15章 15.2（L3344）
  source_quote: "远离那些热门行业中的热门股。"
  summary: 避而不买清单首条（第9章呼应）。
  tags: [rule, avoid-list, hot-stock]
  task_ids: [task-04]

- id: pB68
  title: 要点｜不要相信多元化经营
  type: rule
  source_chapter: 第15章 15.2（L3346）
  source_quote: "不要相信多元化经营，事实证明多元化经营往往反而会导致公司经营状况恶化。"
  summary: 多元恶化（diworseification）警告；买入与持有中都要检查多元化动向。
  tags: [rule, avoid-list, diworseification]
  task_ids: [task-04, task-08]

- id: pB69
  title: 要点｜高回报微概率的投资冒险几乎从不成功
  type: principle
  source_chapter: 第15章 15.2（L3348）
  source_quote: "那些一旦成功将获得巨大回报但只有微小成功机会的投资冒险几乎从来都不会成功。"
  summary: 小声耳语类股票的否定原则。
  tags: [principle, avoid-list, whisper-stock]
  task_ids: [task-04]

- id: pB70
  title: 要点｜第一轮业绩上涨时不要盲目买入
  type: rule
  source_chapter: 第15章 15.2（L3350）
  source_quote: "在公司第一轮业绩上涨时最好不要盲目买入，等等看公司的扩张计划是否确实有效再做决定更为稳妥。"
  summary: 与pB14同源：等扩张计划验证后再买。
  tags: [rule, wait-for-proof, fast-grower]
  task_ids: [task-03, task-07]

- id: pB71
  title: 要点｜工作中的投资信息领先专业者数月至数年
  type: principle
  source_chapter: 第15章 15.2（L3352）
  source_quote: "业余投资者从其工作中能够获得有着巨大价值的投资信息，而且往往要比专业投资者提前好几个月甚至好几年得到。"
  summary: 业余优势论的核心断言（第2、6章呼应）。
  tags: [principle, amateur-edge, information-edge]
  task_ids: [task-12]

- id: pB72
  title: 要点｜把股票消息与提供消息的人分开
  type: rule
  source_chapter: 第15章 15.2（L3354）
  source_quote: "把股票消息与提供股票消息的人分开，不要盲目听信任何人的股票消息，不管提供股票消息的人多么聪明、多么有钱、上一次他的消息多么灵验。"
  summary: 任何来源的股票消息都不可直接采信，与消息提供者的身份地位无关。
  tags: [rule, tips, psychological-trap]
  task_ids: [task-10, task-04]

- id: pB73
  title: 要点｜行业专家的信息只在本行业内值钱
  type: rule
  source_chapter: 第15章 15.2（L3356）
  source_quote: "一个行业专家提供的他并不熟悉的其他行业的股票信息往往最终证明并没有什么价值。在造纸行业工作的人往往提供的是制药行业股票的小道信息……"
  summary: 专家信息边界：本行业专家的交叉行业小道消息无价值；只采信其本行业信息。
  tags: [rule, information-edge, expertise-boundary]
  task_ids: [task-12, task-10]

- id: pB74
  title: 要点｜投资业务枯燥、平凡、无人青睐的公司
  type: rule
  source_chapter: 第15章 15.2（L3358）
  source_quote: "投资那些业务简单易懂、枯燥乏味、普通平凡、不受人青睐，并且还没有引起华尔街专业投资者兴趣的公司股票。"
  summary: 13条选股准则的浓缩（第8章呼应）。
  tags: [rule, boring-business, avoid-wall-street-radar]
  task_ids: [task-03]

- id: pB75
  title: 要点｜不增长行业中增长20%-25%的公司最理想
  type: rule
  source_chapter: 第15章 15.2（L3360）
  source_quote: "在不增长行业中增长速度适中的公司（收益增长率为20%～25%）是十分理想的股票投资对象。"
  summary: 零增长行业+20-25%收益增长=理想标的（无人竞争、无 overheating）。
  tags: [rule, fast-grower, no-growth-industry]
  task_ids: [task-03, task-08]

- id: pB76
  title: 要点｜寻找拥有利基的公司
  type: rule
  source_chapter: 第15章 15.2（L3362）
  source_quote: "寻找那种拥有利基的公司。"
  summary: 利基=竞争对手进不来的排他性经营（第8章呼应）。
  tags: [rule, niche, moat]
  task_ids: [task-03]

- id: pB77
  title: 要点｜买困境股票要财务好、避银行债重的公司
  type: rule
  source_chapter: 第15章 15.2（L3364）
  source_quote: "当购买那些公司处于困境之中并且股价表现令人沮丧的股票时，要寻找财务状况非常好的公司，要避开银行债务负担沉重的公司。"
  summary: 与pB33/pB34同源：困境反转选股的负债过滤条件。
  tags: [rule, turn-around, bank-debt]
  task_ids: [task-06, task-08]

- id: pB78
  title: 要点｜没有债务的公司根本不可能破产
  type: principle
  source_chapter: 第15章 15.2（L3366）
  source_quote: "没有债务的公司根本不可能破产。"
  summary: 零负债=不可破产的极端安全线（苹果危机期2亿美元现金零债务案例）。
  tags: [principle, debt, survival]
  task_ids: [task-06]

- id: pB79
  title: 要点｜买股依据是发展前景而非总裁履历
  type: rule
  source_chapter: 第15章 15.2（L3368）
  source_quote: "管理能力也许非常重要，但是管理能力很难进行评估。购买某一家公司股票的依据应该建立在公司发展前景之上，而不是建立在公司总裁的履历或者演讲能力之上。"
  summary: 管理能力难评估，选股锚定公司前景而非明星经理人。
  tags: [rule, management, focus]
  task_ids: [task-03, task-10]

- id: pB80
  title: 要点｜困境公司成功东山再起让投资者赚一大笔
  type: principle
  source_chapter: 第15章 15.2（L3370）
  source_quote: "一家处于困境中的公司成功东山再起会让投资者赚到一大笔钱。"
  summary: 困境反转型的高回报命题（克莱斯勒15倍等）。
  tags: [principle, turn-around, payoff]
  task_ids: [task-01]

- id: pB81
  title: 要点｜股价严重高估时其他再好也赚不到钱
  type: rule
  source_chapter: 第15章 15.2（L3372）
  source_quote: "仔细考虑市盈率的高低。如果股票价格被严重高估，即使公司其他情况都很好，你也不可能从这种股票上赚到一分钱。"
  summary: 与pB04同源：估值是收益兑现的前提条件。
  tags: [rule, pe-ratio, valuation, red-line]
  task_ids: [task-05]

- id: pB82
  title: 要点｜找到公司发展主线并持续监视
  type: principle
  source_chapter: 第15章 15.2（L3374）
  source_quote: "找到公司发展的主线，根据这一主线密切关注监视公司的发展。"
  summary: 每家公司有其"故事主线"（两分钟独白），按主线跟踪核查。
  tags: [principle, story-line, monitoring]
  task_ids: [task-07, task-09]

- id: pB83
  title: 要点｜寻找持续回购自己股票的公司
  type: rule
  source_chapter: 第15章 15.2（L3376）
  source_quote: "寻找那种一直在持续回购自己股票的公司。"
  summary: 回购=利好信号（13条准则之一；福特案例）。
  tags: [rule, buyback, signal]
  task_ids: [task-03, task-06]

- id: pB84
  title: 要点｜研究派息记录与衰退期收益
  type: rule
  source_chapter: 第15章 15.2（L3378）
  source_quote: "研究公司过去几年的派息记录以及在经济衰退期的收益情况如何。"
  summary: 历史核查两维度：派息记录+衰退期收益韧性。
  tags: [rule, dividend, recession-test]
  task_ids: [task-06, task-08]

- id: pB85
  title: 要点｜寻找机构持股比例很小或为零的公司
  type: rule
  source_chapter: 第15章 15.2（L3380）
  source_quote: "寻找那种机构投资者持股比例很小或者机构投资者根本就没有持股的公司。"
  summary: 机构无持股=未被华尔街发现+未来机构买入的推升空间。
  tags: [rule, institutional-holding, avoid-wall-street-radar]
  task_ids: [task-03]

- id: pB86
  title: 要点｜管理者大量持股的公司更值得投资
  type: rule
  source_chapter: 第15章 15.2（L3382）
  source_quote: "如果其他情况都相同的话，那些管理者个人大量持有自家公司股票的公司，要比那种管理者没有持股只拿薪水的公司更值得投资。"
  summary: 管理层利益绑定原则（其他条件相同时）。
  tags: [rule, insider-holding, alignment]
  task_ids: [task-03]

- id: pB87
  title: 要点｜内部人士买入是有利信号，多人同时买入尤甚
  type: rule
  source_chapter: 第15章 15.2（L3384）
  source_quote: "公司内部人士购买自家公司的股票是一个有利的信号，特别是当公司内好几个内部人士同时购买时。"
  summary: 内部人士集体买入的信号强度高于单人买入（与pB15内部人士卖出的不对称性对照）。
  tags: [rule, insider-buying, signal]
  task_ids: [task-03]

- id: pB88
  title: 要点｜每周至少一小时投资研究；算盈亏不算研究
  type: rule
  source_chapter: 第15章 15.2（L3386）
  source_quote: "每个星期至少抽出一个小时的时间进行投资研究。计算累计收到的股息以及计算自己投资盈亏情况并不算是投资研究。"
  summary: 最低研究投入门槛=每周1小时；记账行为不构成研究。
  tags: [rule, time-commitment, research]
  task_ids: [task-12, task-09]

- id: pB89
  title: 要点｜一定要耐心
  type: principle
  source_chapter: 第15章 15.2（L3388）
  source_quote: "一定要耐心。水越等越不开，股票越急越不涨。"
  summary: 耐心格言（默克9年横盘后5年4倍的耐心回报，见pB128）。
  tags: [principle, patience]
  task_ids: [task-09, task-11]

- id: pB90
  title: 要点｜只按账面价值购股非常危险
  type: rule
  source_chapter: 第15章 15.2（L3390）
  source_quote: "只根据公司财务报表中的每股账面价值来购入股票是非常危险的，也是根本不可靠的，应该根据公司资产的真实价值而不是账面价值来买入股票。"
  summary: 与pB38同源：账面价值→真实价值的核查要求。
  tags: [rule, book-value, trap]
  task_ids: [task-06]

- id: pB91
  title: 要点｜怀疑时，等等看
  type: principle
  source_chapter: 第15章 15.2（L3392）
  source_quote: "怀疑时，等等看。"
  summary: 不确定时的默认动作=等待，不行动。
  tags: [principle, wait-and-see, decision-default]
  task_ids: [task-10, task-12]

- id: pB92
  title: 要点｜选股至少像选冰箱一样认真
  type: rule
  source_chapter: 第15章 15.2（L3394）
  source_quote: "在选择一只新股票时要认真研究分析，至少应该与你选择一台新冰箱所花的时间和精力一样多。"
  summary: 日常消费决策的认真程度是选股投入的下限比喻。
  tags: [rule, research-effort]
  task_ids: [task-12, task-07]

# ── 第16章 构建投资组合（L3404-3494）──────────────────────────

- id: pB93
  title: 期望收益率：12%-15%复利是现实目标，25%-30%不切实际
  type: rule
  source_chapter: 第16章（L3406-3426）
  source_quote: |
    "要证明你付出时间和精力自己来选择股票是值得的，从长期来看你应该从股票投资中获得12%～15%的复利投资收益率，进行业绩计算时必须扣除所有成本和佣金，并加上所有股息和其他红利。"
  summary: |
    收益率锚：长期股市平均9-10%（=指数基金基准）；自选股者应以净12-15%复利为目标。25-30%的期望会使你在最不该放弃的时刻放弃正确策略、或冒不必要风险。若长期跑不赢储蓄利率=方法有严重缺陷。计算业绩须扣除订阅费、佣金、研讨会、长途话费等全部成本。10年15%复利：1万→40455美元 vs 10%的25937美元。
  tags: [return-expectation, rule, benchmark]
  task_ids: [task-11, task-12]

- id: pB94
  title: 频繁交易成本算术：年换手一次≈4%佣金拖累
  type: calculation
  source_chapter: 第16章（L3422-3424）
  source_quote: |
    "如果业余投资者每年把投资组合中的股票全部换手一次，他就得支付约4%的佣金……要想在扣除成本后获得12%～15%的实际收益率，就必须从他所选择的股票中获得16%～19%的投资回报。"
  summary: |
    每次买卖成本1-2%；全部换手一次（买+卖）≈4%；目标净12-15%→毛收益需16-19%。交易越频繁越难跑赢指数基金。长期持有者的收益率远超频繁买卖的短期投资人。
  inputs: [单次交易成本率, 年换手次数, 目标净收益率]
  formula: "年佣金 ≈ 2×单次成本×换手次数；所需毛收益 = 目标净收益 + 佣金"
  units: %
  output: 所需毛收益率（净12-15% → 毛16-19%）
  missing_conditions: 基于写作期（1980s末）美股佣金水平；当代低佣金环境数值会降低但方向不变
  tags: [transaction-cost, calculation, turnover]
  task_ids: [task-11]

- id: pB95
  title: 持股3-10只；质量优先，拒绝愚蠢多元化
  type: rule
  source_chapter: 第16章 16.1（L3436-3446）
  source_quote: |
    "我觉得对于一个小的投资组合来说持有3～10只股票比较合适……只是为了投资组合多元化而分散投资于一些你并不了解的公司股票是毫无益处的，对小投资者来说愚蠢的多元化投资所导致的后果非常恐怖、非常可怕。"
  summary: |
    小组合3-10只适当分散。理由：①股票越多出现10倍股概率越大（最好的增长常出乎意料：Stop&Shop预期30-40%实为10倍+）；②持股越多资金配置弹性越大。投资的关键不是确定数量，而是逐一调查研究确定每一只的质量；把所有资金押一只股票不安全（可能遭预料不到的打击）。基于并购预期买入的股票从未真被并购；因基本面良好持有的公司却常被并购。
  tags: [portfolio-size, diversification, rule, core-rule]
  task_ids: [task-11]

- id: pB96
  title: 尽可能多持有满足两条件的股票（特别了解+前景兴奋）
  type: principle
  source_chapter: 第16章 16.1（L3436）
  source_quote: |
    "投资者应该尽可能多地持有符合以下条件的股票：①你个人工作或生活的经验使你对这家公司有着特别深入的了解；②通过一系列的标准进行检查你发现这家公司具有令人兴奋的远大发展前景。"
  summary: 持股集合的定义式标准：个人深度了解+检验后前景兴奋。符合的可能只有1只也可能10来只，数量无关紧要，质量是关键；可专注某一类型（困境反转/隐蔽资产）甚至单只重仓。
  tags: [portfolio-construction, principle, information-edge]
  task_ids: [task-11, task-12]

- id: pB97
  title: 六类型股票的风险-回报对照表
  type: template
  source_chapter: 第16章 16.2（L3456-3460）
  source_quote: |
    "缓慢增长型公司的股票是低风险、低回报的股票……稳定增长型公司股票是低风险、中回报的股票……隐蔽资产型公司股票是低风险、高收益的股票，但前提是你能够确定隐蔽资产的真正价值……周期型公司股票既可能是低风险、高回报……也可能是高风险、低回报……"
  summary: |
    类型风险表：缓慢增长=低风险低回报；稳定增长=低风险中回报（顺年+50%、背年-20%）；隐蔽资产=低风险高回报（判断错损失不大、判断对2-5倍；前提是能确定资产真实价值）；周期=取决于周期预测准确度（对可10倍、错可亏80-90%）；快速增长与困境反转=高风险高回报（克莱斯勒顺+400%/背-100%，实得15倍）。
  tags: [risk-return, company-type, template, core-model]
  task_ids: [task-11, task-01]

- id: pB98
  title: 组合类型搭配示例：2稳定增长+4快速增长+4困境反转
  type: template
  source_chapter: 第16章 16.2（L3462）
  source_quote: |
    "你在设计自己的投资组合时，应该加入2只稳定增长型公司的股票，从而在一定程度上平衡持有4只快速增长型公司股票和4只困境反转型公司股票的巨大投资风险。"
  summary: 10只组合的作者示例搭配：2只稳定增长（降风险）+4只快速增长+4只困境反转。买入稳定增长股目的是降险，但买价过高反增风险（百时美30倍P/E配15%增长）。年龄调整：年轻人可多追10倍股，年长者更需要稳定收入。
  tags: [portfolio-construction, template, mix]
  task_ids: [task-11]

- id: pB99
  title: 林奇麦哲伦基金的类型配置参考（增长股≤30-40%）
  type: template
  source_chapter: 第16章 16.1（L3450）
  source_quote: |
    "我对增长型股票的投资从来没有超过基金资产的30%～40%……我一般将10%～20%左右的基金资产投资于稳定增长型公司的股票，10%～20%左右……投资于周期型公司的股票，剩下的基金资产投资于困境反转型公司的股票。"
  summary: 基金经理参考配置：增长型≤30-40%、稳定增长10-20%、周期10-20%、其余困境反转；哪类机会多就加大哪类比重；二流机会股票出现新利多时提升为主要持股。业余者不必复制1400只（一半资产在100只、2/3在200只），但类型分散思路可借鉴。
  tags: [portfolio-construction, allocation, template, reference]
  task_ids: [task-11]

- id: pB100
  title: 换股不换现金：资金永远留在股市
  type: rule
  source_chapter: 第16章 16.3（L3470）
  source_quote: |
    "我只会把一种股票换成另一种股票，而不会换成现金……要把资金永远留在股票市场里，根据基本面的变化把资金在不同股票之间进行转换。"
  summary: 卖出后立即换成其他股票而非持币；这可避免时机选择失误及其心理痛苦（例外：为应付基金赎回备现金）。卖出赢家换输家或卖出输家抱赢家都错——二者都把股价当成了基本面指示器。
  tags: [portfolio-rule, rotation, always-invested]
  task_ids: [task-11]

- id: pB101
  title: 稳定增长股涨40%卖出规则；6次30%≈4倍复利
  type: calculation
  source_chapter: 第16章 16.3（L3474-3476）
  source_quote: |
    "如果一只稳定增长型公司的股票上涨了40%——这是我期望从这只股票上得到的最高投资收益率，但并没有出现任何利好消息……那么我就会卖出这只股票……6次有30%收益率的投资，其累计复利收益相当于投资一只上涨4倍的大牛股。"
  summary: |
    稳定增长股操作纪律：涨幅达40%（该类型期望上限）且无新利好→卖出，换入尚未上涨的同类。收益算术：6次30%复利≈1.3^6≈4.83倍≈一只4倍大牛股，故中等收益的连续换股可匹敌大牛股。
  inputs: [单次目标收益率, 次数]
  formula: "累计 = (1+单次收益)^次数（1.3^6≈4.83倍）"
  units: 倍
  output: 连续换股的累计收益
  missing_conditions: 依赖每次都能找到下一只达标股票；不含交易成本
  tags: [stable-grower, sell-rule, calculation, rotation]
  task_ids: [task-11, task-02]

- id: pB102
  title: 持有快速增长股的条件与互换规则
  type: rule
  source_chapter: 第16章 16.3（L3478）
  source_quote: |
    "只要快速增长型公司的收益继续增长、规模继续扩张，并且没有出现影响公司增长的障碍，我就会继续持有……其中一只股票已经上涨了50%并且公司发展前景让我感到怀疑，而另一只股票已经下跌或者基本没动但公司发展前景更好，那么我会卖出前一只……增持后一只。"
  summary: 快速增长股持有三条件：收益继续增长+规模继续扩张+无增长障碍（每隔几个月像对陌生公司一样重查）。两选一规则：涨50%+前景怀疑 vs 未涨+前景更好→卖前者买后者。周期与困境反转股同理（卖恶化上涨的、买好转下跌的）。
  tags: [fast-grower, holding-condition, rotation, rule]
  task_ids: [task-11, task-02, task-09]

- id: pB103
  title: 卖基本面恶化股价上涨的，买基本面好转股价下跌的
  type: rule
  source_chapter: 第16章 16.3（L3480）
  source_quote: "卖出那些基本面恶化并且股价上涨的股票，把资金用来增加买入那些基本面好转并且股价下跌的股票。"
  summary: 调仓的核心对偶规则：决策变量=价格相对基本面的变化，而非价格涨跌本身。
  tags: [rotation, rule, fundamentals-vs-price]
  task_ids: [task-11, task-02]

- id: pB104
  title: 股价下跌是追加买入良机；坚持"跌25%就追加"的信念
  type: rule
  source_chapter: 第16章 16.3（L3482-3484）
  source_quote: |
    "如果你不能说服自己坚持'当我的股票下跌25%时我就追加买入'的正确信念，永远戒除'当我的股票下跌25%我就卖出'的毁灭性错误信念，那么你永远不可能从股票投资上获得什么像样的回报。"
  summary: 好股票下跌不是悲剧（低价卖出才是）；应从未来上涨可能性大但股价表现最差/落后的股票中选择追加。25%是心理与操作的追加阈值。
  tags: [buy-the-dip, rule, psychology, core-rule]
  task_ids: [task-11, task-10]

- id: pB105
  title: 厌恶止损指令（10%止损=注定10%亏损）
  type: rule
  source_chapter: 第16章 16.3（L3486-3490）
  source_quote: |
    "止损指令根本无法保护投资者避免发生亏损，只不过是使投资者把当前的账面亏损变成一个已经发生了的现实亏损……你能够举出一个设置了10%止损指令的投资组合，我就同样能够举出一个注定亏损正好是10%的投资组合。"
  summary: 止损指令把账面亏损锁定为现实亏损；股市波动常达10%，Taco Bell设10%止损会错过10倍收益。设置止损=承认将以低于内在价值的价格卖出。"股价翻一番就卖出"同样是错——会错过所有大牛股；只要公司前景不变或更好就坚决持有。
  tags: [stop-order, rule, no-stop-loss, psychology]
  task_ids: [task-11, task-10]

- id: pB106
  title: 以过高价格买入，公司成功也赚不到一分钱
  type: principle
  source_chapter: 第16章 16.2（L3462-3464）
  source_quote: |
    "如果你以过高的价格买入一只股票，那么即使这家公司后来获得了巨大的经营成功，你仍然无法从这家公司的股票上赚到一分钱，这真是一个莫大的悲剧。"
  summary: EDS 1969年500倍P/E，随后15年盈利增约20倍，股价仍从40跌到3美元，1984年被以44美元收购（仅相当于10年前价格）。以两倍增长率的P/E买入稳定增长股（70年代百时美30倍P/E配15%增长）=冒不必要风险追逐不可能的盈利。
  tags: [valuation, principle, overpay-trap]
  task_ids: [task-05, task-10]

# ── 第17章 买入卖出时机（L3496-3740）──────────────────────────

- id: pB107
  title: 买入最佳时机=确信发现价值可靠价格低廉的股票之时
  type: principle
  source_chapter: 第17章（L3498）
  source_quote: "买入股票的最佳时机往往就是你确信发现了价值可靠却价格低廉的股票之时——正如你在商场中发现了一件价廉物美的商品一样。"
  summary: 时机的第一原则：个股发现优先于市场择时；另有两个统计上常见的低价窗口（见pB108/pB109）。
  tags: [buy-timing, principle, stock-picking-first]
  task_ids: [task-14]

- id: pB108
  title: 买入窗口一：年底避税抛售期（10-12月）
  type: rule
  source_chapter: 第17章（L3500-3502）
  source_quote: |
    "一年之中股价下跌最为严重的时期是在10～12月间……如果你已经列出了一系列你想买入的公司股票名单，只要其股价下跌到合理价位你就准备买入，那么年底你最有可能找到等待已久的低价买入良机。"
  summary: 年底为减税卖出亏损股票（个人+机构清理组合+保证金与机构对<6美元低价股的强制卖出），把好股票打压到惊人低价。操作前提：事先列好观察名单，跌到合理价位就买。
  tags: [buy-timing, tax-selling, rule, seasonal]
  task_ids: [task-14]

- id: pB109
  title: 买入窗口二：股市崩盘、大跌、自由落体时
  type: rule
  source_chapter: 第17章（L3504-3564，表17-1/17-2）
  source_quote: |
    "第二个可能发现特别便宜的股票的特殊时期，是在股市崩盘、大跌、激烈振荡、像自由落体一样直线下跌的时候……表17-1中所列出那些实力雄厚且盈利增长良好的优秀公司，在最近几次市场崩溃时你可以用很低的价格买入。"
  summary: |
    崩盘期每隔几年出现；专业投资者因忙碌或束缚无法迅速行动，业余者保持理智即得良机。表17-1证据（最高→最低→1987年最高）：Teledyne 11→3→390、Cap Cities 34→9→450、麦当劳15→4→61.125、百时美8→4→55、默克17→7→74.25、The Limited 10→5→53。表17-2（1987年跌后1988年10月）：Dreyfus 45→16（每股净现金15美元）→25.625、沃尔玛41→20→31.375、可口可乐53→28→43.125、家得宝28→12.5→28.375。
  tags: [buy-timing, crash, rule, table-17-1-2]
  task_ids: [task-14]

- id: pB110
  title: 不要过早卖出：抓住大牛股就持有到最大回报
  type: rule
  source_chapter: 第17章 17.2（L3570-3582）
  source_quote: |
    "当你发现了合适的股票并且以合理的价格买入，所有的证据都表明这只股票将会越涨越高……如果此时你却将它抛出真是太愚蠢了……如果你抓住一只大牛股，你就应该一直持有直到获得最大的回报。"
  summary: 过早卖出案例：华纳26→38美元卖出后涨过180美元（"过度上涨"的技术分析意见植入脑海之害）；玩具反斗城1美元买5美元卖（5倍），错过后来的25倍；等并购消息不耐烦卖出Flowers/Lance后反被并购。个人投资者一生只有1-2次机会抓住25倍股。"见好就收""一鸟在手"不适用于基本面持续向好的大牛股。
  tags: [sell-discipline, not-too-early, rule, tenbagger]
  task_ids: [task-02, task-10]

- id: pB111
  title: 因大买家停止买入或内部人士卖出而卖股是大错
  type: rule
  source_chapter: 第17章 17.2（L3580-3586）
  source_quote: |
    "由于内部人士开始卖出而不再买入一家公司的股票，就像由于外部投资者（像美国玩具反斗城公司的皮特里）停止买入而卖出股票一样，两种行为都是大错特错。"
  summary: 卖出决策的干扰项排除：大买家（皮特里买玩具反斗城至20%后停止）停止买入≠股价必跌；内部人士卖出≠公司变坏。与pB15构成对称规则（买入侧/卖出侧）。
  tags: [sell-discipline, insider-selling, rule, psychological-trap]
  task_ids: [task-10, task-02]

- id: pB112
  title: 感觉被假象愚弄时重审最初买入理由
  type: rule
  source_chapter: 第17章 17.2（L3588）
  source_quote: "这些日子如果我感觉自己有被假象愚弄而出局的危险，那么我就会重新审视一下自己最初购买这只股票的理由，看看现在和过去相比情况有否不同。"
  summary: 在股价上涨后继续持有比下跌后持有更难；动摇时回到"当初为什么买"的原始理由做对比检验，理由未变则持有。
  tags: [holding-discipline, rule, original-thesis]
  task_ids: [task-09, task-10]

- id: pB113
  title: 小心煽动效应：别因不懂的宏观说法卖出股票
  type: principle
  source_chapter: 第17章 17.3（L3590-3608）
  source_quote: |
    "基于'M1正在提高'这种原因就卖出股票，甚至你根本不清楚M1到底是什么，还有比这更愚蠢的理由吗？"
  summary: 亲戚/朋友/经纪人/媒体的愚蠢观点会像"华纳过度上涨"一样植入脑海并驱动操作（经纪人"恭喜赚钱别贪心"的一卖一买=双份佣金）。油价涨跌、美元强弱、货币供给增减都被轮流说成可怕的事。对反复重复的不祥说法保持免疫。
  tags: [psychology, media-noise, principle, drumbeat]
  task_ids: [task-10]

- id: pB114
  title: 卖出思考法：像思考买入一样思考卖出
  type: principle
  source_chapter: 第17章 17.4（L3610-3616）
  source_quote: |
    "多年以来我学会的一个经验就是：像思考何时购买股票一样思考何时卖出股票……在90%的情况下，我卖出股票是因为找到了那些发展前景更好的公司的股票。"
  summary: 没有万能卖出公式；"利率上升就卖出""衰退前卖出"等格言因无法预知宏观而无用。原则：①不关注外部宏观（例外：极明显重大事件影响具体行业，如油价下跌影响石油服务公司）；②知道当初买入理由→自然知道何时卖出；③主要卖出原因=找到前景更好的股票。
  tags: [sell-discipline, principle, core-rule]
  task_ids: [task-02]

- id: pB115
  title: 卖出清单｜缓慢增长型（涨30%-50%即卖）
  type: checklist
  source_chapter: 第17章 17.4.1（L3618-3630）
  source_quote: |
    "当上涨了30%～50%时，或者基本面情况恶化时，即使股价已经下跌我也会坚决赔钱卖出。"
  summary: |
    主规则：涨30-50%卖出；或基本面恶化时即使亏损也坚决卖出。附加信号：①连续两年市场份额流失且正聘请新广告代理商；②无新产品开发、研发经费削减、明显吃老本；③新收购两个与主业无关的业务（多元恶化趋向）并声称寻找"技术前沿"收购；④为收购支付太高代价致资产负债表恶化（从无债有现金变成无现金有负债），股价大跌也无钱回购；⑤股价虽低股息收益率仍很低。
  tags: [sell-checklist, slow-grower, core-tool]
  task_ids: [task-02]

- id: pB116
  title: 卖出清单｜稳定增长型（P/E超常或股价线超收益线即卖）
  type: checklist
  source_chapter: 第17章 17.4.2（L3632-3646）
  source_quote: |
    "如果一只稳定增长型股票的股价线超过收益线，或者市盈率远远超过正常市盈率水平，你应该考虑卖出这只股票，等股价回落后再买回来……期望从稳定增长型股票中找到一只10倍股是毫无意义的。"
  summary: |
    主规则：股价线超收益线或P/E远超正常水平→卖出（回落再买回或换其他未涨的稳定增长股，常用其他类型替换）。附加信号：①过去两年新产品业绩有好有坏、其他产品仍在试验需一年才上市；②P/E 15倍而同行只有11-12倍；③过去一年无管理人员和董事购买自家股票；④占利润25%的主要业务部门将受经济萧条严重打击（房地产、石油勘探等）；⑤增长率放缓，成本削减空间已相当有限。
  tags: [sell-checklist, stable-grower, core-tool]
  task_ids: [task-02]

- id: pB117
  title: 卖出清单｜周期型（周期顶峰/P/E最低点前卖出）
  type: checklist
  source_chapter: 第17章 17.4.3（L3648-3670）
  source_quote: |
    "卖出周期型股票的最佳时机是在公司增长达到顶峰周期即将结束时……另一个明显的卖出信号是，公司的存货不断增加，而且公司无法处理掉新增加的存货……大宗商品价格下跌是另一个应该卖出周期型股票的信号，通常早在公司收益出现问题的几个月之前。"
  summary: |
    主规则：增长顶峰/周期结束前卖出（有远见者提前一年以上卖出；周期股常无缘无故开始下跌；通用动力盈利增长股价反跌50%）。核心时机：①业绩复苏时P/E将降低——P/E最低时最危险；②成本开始增长、工厂满负荷、投资扩产=繁荣期结束；③存货不断增加且无法处理（停车场堆满=该卖甚至已晚）；④大宗商品（汽油、钢材）价格下跌（领先收益数月）、期货价格低于现货；⑤新竞争者进入大幅降价（Inco之鉴）。附加：未来12个月内两个关键工会合同到期且要求恢复工资福利；最终需求下降；用双倍于改造老厂的资本预算建豪华新厂；降本仍无法与国外厂商竞争。
  tags: [sell-checklist, cyclical, core-tool]
  task_ids: [task-02]

- id: pB118
  title: 卖出清单｜快速增长型（勿过早卖；30倍P/E配15-20%增长即卖）
  type: checklist
  source_chapter: 第17章 17.4.4（L3672-3696）
  source_quote: |
    "如果目前有40个华尔街的证券分析师都对一只快速增长型股票给予最高的推荐评级，机构投资者持有这家公司60%的股票，并且有三种国家级主流杂志都在极力吹捧公司的CEO，那么这时绝对应该考虑卖出这只股票了。"
  summary: |
    主规则：重点是不要过早卖出（错过10倍股）；重点观察第二阶段末期（见pB52三阶段）；应回避股票的特征（第9章避而不买清单）也正是应卖出的特征；40分析师最高评级+机构持股60%+3家杂志吹捧CEO=绝对卖出；P/E高到不合逻辑（宝丽来/雅芳50倍）任何小学生都看得出该卖；假日酒店40倍P/E=涨到尽头（扩张到直布罗陀=无处可扩）。附加信号：①最近一季同店销售额降低3%；②新开分店销售业绩令人失望；③两位高管+核心员工辞职加盟竞争对手；④刚结束两周12城路演向机构描述极乐观前景；⑤P/E高达30倍而未来两年最乐观盈利增长预期只有15-20%。
  tags: [sell-checklist, fast-grower, core-tool]
  task_ids: [task-02]

- id: pB119
  title: 卖出清单｜困境反转型（转危为安后卖出并重新分类）
  type: checklist
  source_chapter: 第17章 17.4.5（L3698-3714）
  source_quote: |
    "卖出一只困境反转型股票的最佳时机是在公司成功转危为安之后，所有的困难都已经得到解决，并且每个投资者都知道这家公司已经东山再起了……你应该重新对这家公司股票进行分类。"
  summary: |
    主规则：成功转危为安、人尽皆知时卖出；此后公司已换类型须重新归类再用该类规则判断（克莱斯勒2/5/10美元时是困境反转，48美元时已是实力雄厚的周期型——不可能再涨10倍；GPU三哩岛解决后38美元已是优质公用事业，不会再涨到400美元）。附加信号：①过去连续5个季度债务持续下降后最近季度债务反增2500万美元；②存货增长速度是销售增长速度的两倍；③P/E相对预期收益增长率高得离谱；④最强分公司50%产品售给正遭受销售放缓之苦的最大客户。
  tags: [sell-checklist, turn-around, reclassify, core-tool]
  task_ids: [task-02, task-01]

- id: pB120
  title: 卖出清单｜隐蔽资产型（等袭击并购者出现再卖）
  type: checklist
  source_chapter: 第17章 17.4.6（L3716-3736）
  source_quote: |
    "坚决不要卖出一只隐蔽资产型公司，除非贝思兄弟家族出现来收购这家公司……只要一家隐蔽资产型公司没有大量借债而导致资产价值下降，投资者就应该坚持持有这家公司的股票。"
  summary: |
    主规则：等待袭击并购者（Steinberg/Icahn/Pickens/Trump等）出现才卖——并购、要约收购或杠杆收购使股价猛涨2-4倍（Alexander&Baldwin 5→32美元）；无并购者出现且未大量举债→坚持持有。附加信号：①股价远低于资产真实价值，管理层却宣布增发超过总股本10%的股票筹资搞多元化；②下属分公司预期卖2000万美元实际只卖1200万；③税率降低相当程度减少了税收亏损抵扣（time value of tax-loss carryforward）的价值；④机构持股比例从5年前的25%增加到60%（波士顿几家基金集团为主）。
  tags: [sell-checklist, hidden-asset, raider, core-tool]
  task_ids: [task-02]

# ── 第18章 12种最愚蠢且最危险的说法（L3742-3987，逐条）─────────

- id: pB121
  title: 危险说法1｜"股价已经下跌这么多了，不可能再跌了"
  type: rule
  source_chapter: 第18章 18.1（L3748-3764）
  source_quote: |
    "根本没有什么法则能够告诉我们股价大概会下跌到什么程度……宝丽来……在不到一年的时间里从每股143.5美元下跌到了每股14.125美元，此时才是真正'不可能再跌了'的价位。"
  summary: 反驳证据：宝丽来143.5→14.125美元（跌90%）；凯撒工业25→13→11（林奇推荐富达买500万股）→8→7.5→6→4美元（公司清算价值每股至少40美元、债务极少，最终反弹到30美元）。没有任何法则能预测下跌终点，不要以"跌很多了"作为买入理由。
  tags: [dangerous-saying, rule, falling-knife, polaroid-case]
  task_ids: [task-10]

- id: pB122
  title: 危险说法2｜"你总能知道什么时候一只股票跌到底了"
  type: rule
  source_chapter: 第18章 18.2（L3766-3772）
  source_quote: |
    "想要抄底买入一只下跌的股票，就如同想要抓住一把下跌的刀子……更稳妥的办法是，等刀落到地上后，扎进地里，晃来晃去了一阵后停止不动了，这时再抓起这把刀子也不迟。"
  summary: 抄底如抓下坠的刀。正确做法：等刀落地晃动停止再捡——买入困境反转要有更充分的理由（业务已开始好转+资产负债表每股净现金11美元vs股价14美元），而非"跌多了可能反弹"。且即使研究充分也难买在最低价：股价重新上涨前通常振荡整理2-3年甚至更长。
  tags: [dangerous-saying, rule, bottom-fishing]
  task_ids: [task-10, task-14]

- id: pB123
  title: 危险说法3｜"股价已经这么高了，怎么可能再涨呢"
  type: rule
  source_chapter: 第18章 18.3（L3774-3850）
  source_quote: |
    "关键是一只股票能够上涨多高并没有什么人为武断的上限。如果一家公司的发展前景良好，投资收益会继续增长，基本面也没有什么改变，仅仅因为'股价不可能再涨'就放弃持有这家公司的股票实在是太糟糕了。"
  summary: 反驳证据：菲利普·莫里斯0.75→124.5美元（1000美元→16.6万美元+2.3万美元股息；2.5美元"高位"卖出者错过其后23倍）；斯巴鲁已涨20倍后林奇再买又赚7倍。股票上涨没有人为上限；"涨一倍就自动卖出"的建议者应感到羞愧。
  tags: [dangerous-saying, rule, no-price-ceiling, philip-morris-case]
  task_ids: [task-10, task-02]

- id: pB124
  title: 危险说法4｜"股价只有3美元，我能亏多少呢"
  type: rule
  source_chapter: 第18章 18.4（L3852-3864）
  source_quote: |
    "无论一只股票股价是50美元还是1美元，当这只股票股价下跌到零时，对于你来说都是老本亏了个精光，亏损都是100%。"
  summary: 亏损以百分比而非绝对股价衡量：50美元买入亏99%与3美元买入亏83%是五十步笑百步；1000美元投43美元股或3美元股，跌到零都亏同样的1000美元。低价股的卖家常是等公司明显要破产才建仓的空头（8美元/6美元建仓与60美元无差别，收益率同样100%）。
  tags: [dangerous-saying, rule, low-price-trap, loss-math]
  task_ids: [task-10]

- id: pB125
  title: 危险说法5｜"最终股价会涨回来的"
  type: rule
  source_chapter: 第18章 18.5（L3866-3872）
  source_quote: |
    "果真如此的话，西哥特人、皮克特人、成吉思汗的大军最终都应该会杀回来的。过去人们都说RCA公司股价最终会涨回来的，但65年过去了，它的股价仍然没有涨回来。"
  summary: 反驳证据：RCA 65年未涨回；Johns-Manville（石棉诉讼+增发数亿新股稀释）未涨回；HMO、软盘、双面针织物、电子表、移动房屋等行业股票至今未涨回；上千家已破产公司+有偿债能力却永难重现繁荣的公司+被低价整体收购的公司。"会涨回来"不可靠。
  tags: [dangerous-saying, rule, mean-reversion-fallacy]
  task_ids: [task-10]

- id: pB126
  title: 危险说法6｜"黎明前总是最黑暗的"
  type: rule
  source_chapter: 第18章 18.6（L3874-3880）
  source_quote: |
    "在黎明之前总是最黑暗的，但是有时在最后变得一片漆黑之前也总是最黑暗的。"
  summary: 反驳证据：石油钻井1981年4520口→1984年2200口（众人以为最糟已过而买入）→两年后686口→今天不足1000口；货车运输95650辆(1979)→44800(1981，17年低点，众人买入)→17582(1982)→5700(1983)，行业遭下跌90%重创。事情已经糟糕不代表不会更糟。
  tags: [dangerous-saying, rule, it-gets-worse]
  task_ids: [task-10]

- id: pB127
  title: 危险说法7｜"等到股价反弹到10美元时我才会卖出"
  type: rule
  source_chapter: 第18章 18.7（L3882-3886）
  source_quote: |
    "从来没有一只严重套牢的股票会如你所愿地反弹到你设定的卖出心理价位……除非我对这家公司有着足够的信心，在股价下跌时愿意追加买入更多的股票，否则我就应该立刻卖出这家公司的股票。"
  summary: 心理价位从不被满足：设定10美元卖出的股票往往在9.75美元下方振荡数年后跌向4美元、1美元面值，折磨可达十年。决策检验：愿不愿意在下跌中追加买入？不愿意→立刻卖出。
  tags: [dangerous-saying, rule, anchor-price, exit-test]
  task_ids: [task-10, task-02]

- id: pB128
  title: 危险说法8｜"保守型股票不会波动太大"
  type: rule
  source_chapter: 第18章 18.8（L3888-3896）
  source_quote: |
    "公司发展是动态的，公司发展前景是变化的，根本没有任何一只你可以不管不问只需一直持有的股票。"
  summary: 反驳证据：联合爱迪生因核事故与收益率基数问题损失80%市值（后又反弹更高）；印第安纳公共服务、海湾公用事业、新罕布什尔公共服务与投资无名生物遗传公司同样危险甚至更危险（因为投资者没意识到风险）。公用事业股现在能涨10倍也能跌到1/10；不随波动性改变策略者遭财务+心理双重打击。
  tags: [dangerous-saying, rule, no-buy-and-forget]
  task_ids: [task-10, task-09]

- id: pB129
  title: 危险说法9｜"等的时间太长了，不可能上涨了"
  type: rule
  source_chapter: 第18章 18.9（L3898-3959）
  source_quote: |
    "从1972～1981年，这只股票的股价一动不动，尽管公司盈利平均每年稳步增长14%。后来发生了什么呢？在随后的5年中这只股票股价上涨了4倍。"
  summary: 反驳证据：默克1972-1981横盘9年（盈利年增14%）后5年涨4倍；Angelica 5年不动后4年7倍、American Greeting 8年不动后6年6倍、GAF 11年、Brunswick整个70年代、Lukens 14年不动后15年6倍、史克10年不动后2年3倍。横盘一条线="一块石头的心电图"=下一波大涨的强烈暗示。只要基本面未变，耐心早晚得到回报。
  tags: [dangerous-saying, rule, patience, flat-line-signal]
  task_ids: [task-10, task-09]

- id: pB130
  title: 危险说法10｜"看看我损失了多少钱，我竟然没买这只大牛股"
  type: rule
  source_chapter: 第18章 18.10（L3961-3969）
  source_quote: |
    "没有买入瓶盖瓶塞封口公司股票……你会注意到你的钱仍然一分不少地待在那里……认为别人在股市赚的钱就是我们自己赔的钱并非一种有益的态度。"
  summary: 错过≠亏损：没买的钱一分未少。这种想法最糟的后果是驱使人盲目追逐回报、买本不该买的股票，把心理亏损变成真实亏损。
  tags: [dangerous-saying, rule, fomo]
  task_ids: [task-10]

- id: pB131
  title: 危险说法11｜"我错过了这只大牛股，我得抓住下一只这样的大牛股"
  type: rule
  source_chapter: 第18章 18.11（L3971-3977）
  source_quote: |
    "在大多数情况下，以更高的价格购买的那家被作为典范的优秀公司股票，要好于你用便宜的价格购买所谓能成为下一个这家优秀公司的公司。"
  summary: "下一个"极少成功：错过玩具反斗城买Greenman Brothers（一般公司，持续下跌）；错过家得宝（25倍）买"下一个家得宝"Scotty（仅25-30%）；错过皮埃蒙特买人民航空、错过Price Club买Warehouse=重大亏损。第一错误（错过）不亏钱，为弥补而犯的第二错误损失真金白银。
  tags: [dangerous-saying, rule, next-big-thing, avoid-list]
  task_ids: [task-10, task-04]

- id: pB132
  title: 危险说法12｜"股价上涨=我选对了；股价下跌=我选错了"
  type: rule
  source_chapter: 第18章 18.12（L3979-3987）
  source_quote: |
    "当你购买了一只股票后，短期内股价上涨或者下跌只能说明有人愿意支付更多或更少的价钱去购买同一只股票而已。"
  summary: 作者心中最愚蠢的谬论。反驳证据：1981年Zapata（能源繁荣被一致看好）35→2美元，"被碾伤的狗"Ethyl（EPA禁含铅添加剂）2→32美元。短期涨跌既不证明选股正确也不证明错误（除非20%短线交易者）；"留住赢家扔掉输家"式操作混淆了股价与公司前景。
  tags: [dangerous-saying, rule, price-vs-fundamentals]
  task_ids: [task-10]

# ── 第19章 期权、期货与卖空（L3997-4055）──────────────────────────

- id: pB133
  title: 不做期权期货：80%-95%的参与者亏损
  type: rule
  source_chapter: 第19章 19.1（L4001-4007, L4035）
  source_quote: |
    "根据芝加哥和纽约这两家期货和期权交易的主要交易所的报告，80%～95%的业余投资者在期权和期货交易上是亏损的。在期货和期权交易上亏损的概率比在卡西诺赌场或赛马场上赌博输钱的概率更大。"
  summary: 作者生涯从未买过一次期权期货；交易所自报业余投资者80-95%亏损；亏损概率高于赌场。期货在农产品套保上有正当作用，但股票不存在生产者-消费者价格保险关系。巴菲特认为股票期货期权应定为违法，作者完全赞成。股票投资起码为经济增长提供资本，期权期货市场上没有一分钱投入建设性用途。
  tags: [options-futures, prohibition, rule, core-rule]
  task_ids: [task-15]

- id: pB134
  title: 期权的三重结构性缺陷（到期作废/佣金昂贵/零和游戏）
  type: principle
  source_chapter: 第19章 19.1（L4011-4025）
  source_quote: |
    "期权投资最糟糕的地方是持有期权与持有公司的股份毫不相关……期权交易中一方获得任何1美元的赢利，相应交易的另一方都会发生1美元的亏损。"
  summary: 三缺陷：①有效期仅一两个月，到期一文不值须再买再亏100%（判断正确也可能颗粒无收：3000美元买4月看涨期权到期作废，几周后股价才大涨）；②代价昂贵：需连买4-5份才等于一年期限的选择权，期限越长溢价越高，佣金比例极高（经纪人的摇钱树）；③零和游戏，与公司经营成败完全脱钩（公司兴旺股东受益，期权买卖方互为盈亏）。
  tags: [options, structural-flaw, principle]
  task_ids: [task-15]

- id: pB135
  title: "投资组合保险"无效且加剧崩盘
  type: rule
  source_chapter: 第19章 19.1（L4029-4033）
  source_quote: |
    "事实证明投资组合保险的实际作用却与他们的设想恰恰相反……在导致1987年10月股市崩盘的许多看起来比较合理的解释原因之中，投资组合保险是一个最主要的元凶。"
  summary: 机构组合保险要求跌时买期货同时自动卖股票→股价再跌→再买期货再卖股票的恶性循环，是1987年10月崩盘主要元凶。个人买看跌期权"保险"：到期作废需年年重买，每年浪费5%-10%资金防10%的下跌；且为保险入场者往往很快沦为投机（期权→套保→组合期权→跨式期权，最终亏光并忘了研究基本面）。
  tags: [portfolio-insurance, options, rule, 1987-crash]
  task_ids: [task-15]

- id: pB136
  title: 卖空的三大缺陷与无限亏损
  type: rule
  source_chapter: 第19章 19.2（L4039-4055）
  source_quote: |
    "股票的涨幅是没有任何限制的，因此卖空的亏损也是无限的。"
  summary: 三缺陷：①借股期间股息与其他利益归合法所有者，卖空者得不到；②平仓买回前账面盈利不能动用（股价上涨还须追加保证金否则被迫平仓）；③亏损无限——做多最多亏100%，做空的理论亏损无上限。且判断正确也可能破产：Robert Wilson卖空Resorts International判断最终正确，但股价先从70美分涨到70美元（100倍），他亏损2000万-3000万美元。卖空前需具备耐心+巨大勇气+充足资本三者。
  tags: [short-selling, unlimited-loss, rule, core-rule]
  task_ids: [task-15]

# ── 第20章 5万个专业投资者也许都是错的（L4057-4165）─────────────

- id: pB137
  title: 星期一效应（数据观察+周末恐惧解释）
  type: calculation
  source_chapter: 第20章 20.1（L4131-4137）
  source_quote: |
    "1953～1984年，股市总共上涨了919.6点，在此期间所有星期一的交易日总共下跌了1565点……1987年股市总共上涨了只有42点，在此期间所有星期一的交易日总共下跌了483点。"
  summary: |
    历年总涨跌vs星期一累计：1953-84年+919.6点内周一累计-1565点；1973年+169内周一-149；1974年-235中周一占-149；1984年+149内周一-47；1987年+42内周一-483。解释：周末60小时无法联系公司+周日媒体灾难报道积累恐惧→周一抛售；过周一后打电话发现公司正常→周中反弹。
  inputs: [历年指数涨跌点数, 周一交易日累计涨跌点数]
  formula: "对比全年净涨跌与周一累计涨跌（多组年份反复验证）"
  units: 点
  output: 周一效应存在性判断（样本期成立）
  missing_conditions: 作者自述无法科学论证；数据止于1987年，不可外推至当代市场
  tags: [market-pattern, monday-effect, calculation, observation]
  task_ids: [task-14]

- id: pB138
  title: 反向利用机构乌合之众的抛售
  type: rule
  source_chapter: 第20章 20.1（L4113-4129）
  source_quote: |
    "当这群乌合之众拥挤向出口纷纷卖出股票时，小投资者可以平静地走向入口轻松地低价买入；当这群乌合之众拥挤向入口纷纷买入时，小投资者可以平静地走向出口轻松地高价卖出。"
  summary: 专业投资者仅在典型波动的最后20%时间正确（研究→称赞→抢购→盯紧后门撤出）；1987年中期机构宠儿（自动数据处理、可口可乐、Dunkin' Donuts、GE、菲利普·莫里斯、施贵宝、废物管理等）10个月后因机构失去兴趣被贱卖——公司本身没有任何改变。业余者可等失宠股跌到疯狂低价后买入；业余群体已是稳定股市的关键力量。股市最大的亏损发生在崩盘时卖出者身上，而非长期持有好股票者。
  tags: [contrarian, institutional-behavior, rule]
  task_ids: [task-14, task-11]

- id: pB139
  title: 被溢价收购=股东被抢劫（失去未来10倍增值）
  type: principle
  source_chapter: 第20章 20.1（L4155-4159）
  source_quote: |
    "当并购袭击者来收购经营稳健可靠并且发展前景良好的公司时，其实是这家公司的股东们遭到了抢劫……他们却从此被剥夺了公司股票未来巨大增值所形成的巨额财富。"
  summary: 要约溢价看似好买卖，实则剥夺未来增值：百事40美元要约收购Taco Bell，其独立价值现应相当于每股150美元；10美元反弹途中被20美元收购的股票若终值100美元，卖出者每股只赚10美元、丢掉80美元。最近的收购兼并已从投资者手中夺走许多潜在的10倍股。
  tags: [merger, shareholder-interest, principle]
  task_ids: [task-11, task-02]

- id: pB140
  title: 股票投资需要对国家与经济未来的基本信心
  type: principle
  source_chapter: 第20章 20.1（L4163）
  source_quote: |
    "当你进行股票投资时，你必须对人性、对资本主义、对整个国家、对未来经济的普遍繁荣有一个基本的信心。"
  summary: 在无尽的担忧之墙（艾滋病/干旱/通胀/赤字/贸易赤字/美元……）面前保持基本信心的理由：英国70年贸易赤字仍繁荣；数以千计小公司创造数百万新岗位；公司已学会缩减成本高效运营。担忧清单每月更换，不应驱动卖出决策。
  tags: [confidence, macro-noise, principle]
  task_ids: [task-10, task-12]

# ── 第20章 20.2 本部分要点（L4167-4221，逐条26条）─────────────

- id: pB141
  title: 要点｜未来1个月、1年或3年的某一天股市将突然大跌
  type: principle
  source_chapter: 第20章 20.2（L4171）
  source_quote: "未来1个月、1年或者3年的某一天，股市将会突然大跌。"
  summary: 崩盘不是例外而是必然事件，应作为前提预期而非恐慌理由。
  tags: [principle, crash-expectation]
  task_ids: [task-14, task-10]

- id: pB142
  title: 要点｜股市下跌是买入你喜爱股票的极好机会
  type: rule
  source_chapter: 第20章 20.2（L4173）
  source_quote: "股市下跌是个极好的机会，买入你喜爱的股票。股价修正……使十分优秀的公司股票变得十分廉价。"
  summary: 与pB109同源：把大跌转化为买入窗口的前提是已有"喜爱的股票"清单。
  tags: [rule, buy-the-dip, crash]
  task_ids: [task-14]

- id: pB143
  title: 要点｜不要妄想预测1-2年后的市场走势
  type: rule
  source_chapter: 第20章 20.2（L4175）
  source_quote: "不要妄想预测1年或2年后的市场走势，那是根本不可能的。"
  summary: 市场不可预测原则（第5章呼应）。
  tags: [rule, no-market-timing]
  task_ids: [task-14, task-12]

- id: pB144
  title: 要点｜不需要一直正确也能业绩领先
  type: principle
  source_chapter: 第20章 20.2（L4177）
  source_quote: "你并不需要一直正确，甚至不需要经常正确，照样能够取得高人一筹的投资业绩。"
  summary: 少数大赢足以覆盖多次小错的收益结构。
  tags: [principle, hit-rate, asymmetry]
  task_ids: [task-11, task-12]

- id: pB145
  title: 要点｜大牛股常出乎意料；高回报需持有好几年
  type: principle
  source_chapter: 第20章 20.2（L4179）
  source_quote: "那些让我赚到大钱的大牛股往往出乎我的意料之外……要获得很高的投资回报需要耐心持有股票好几年而不是只持有几个月。"
  summary: 意外性+长期性是10倍股收益的两个属性（作者获利最多的股票往往已持有3-4年）。
  tags: [principle, tenbagger, holding-period]
  task_ids: [task-11, task-02]

- id: pB146
  title: 要点｜不同类型的股票有不同的风险和回报
  type: principle
  source_chapter: 第20章 20.2（L4181）
  source_quote: "不同类型的股票有着不同的风险和回报。"
  summary: 与pB97同源：类型决定风险收益特征。
  tags: [principle, company-type, risk-return]
  task_ids: [task-01]

- id: pB147
  title: 要点｜连续投资稳定增长股的复利累积
  type: principle
  source_chapter: 第20章 20.2（L4183）
  source_quote: "连续投资一系列的稳定增长型股票，尽管每次只有20%～30%的投资收益率，但由于复利的作用累积下来会让你赚到一大笔钱。"
  summary: 与pB101同源：20-30%×连续N次的复利路径。
  tags: [principle, stable-grower, compounding]
  task_ids: [task-11]

- id: pB148
  title: 要点｜短期股价与基本面相反，长期取决于盈利成长
  type: principle
  source_chapter: 第20章 20.2（L4185）
  source_quote: "短期股价走势经常与基本面相反，但长期股价走势最终取决于公司盈利成长性及其可持续性。"
  summary: 全书价格-收益关系命题的最终表述（16张图的共同规律）。
  tags: [principle, price-vs-earnings, core-rule]
  task_ids: [task-05, task-09]

- id: pB149
  title: 要点｜公司现在糟糕不代表将来不会更糟
  type: principle
  source_chapter: 第20章 20.2（L4187）
  source_quote: "一个公司目前经营得十分糟糕，并不代表这家公司将来经营得不会更加糟糕。"
  summary: 与危险说法6（pB126）同源的逆向提醒。
  tags: [principle, it-gets-worse]
  task_ids: [task-10]

- id: pB150
  title: 要点｜股价上涨并不能说明你是对的
  type: principle
  source_chapter: 第20章 20.2（L4189）
  source_quote: "只是根据股价上涨，并不能说明你是对的。"
  summary: 危险说法12（pB132）的正向半句。
  tags: [principle, price-vs-fundamentals]
  task_ids: [task-10]

- id: pB151
  title: 要点｜股价下跌并不能说明你是错的
  type: principle
  source_chapter: 第20章 20.2（L4191）
  source_quote: "只是根据股价下跌，并不能说明你是错的。"
  summary: 危险说法12（pB132）的反向半句；与pB104跌25%追加呼应。
  tags: [principle, price-vs-fundamentals]
  task_ids: [task-10]

- id: pB152
  title: 要点｜机构重仓+华尔街热捧的稳定增长股高估后必然停滞或下跌
  type: rule
  source_chapter: 第20章 20.2（L4193）
  source_quote: "机构投资者重仓持有且华尔街十分关注的稳定增长型股票在跑赢市场且股价高估之后必然面临停滞或下跌。"
  summary: 稳定增长股的拥挤/高估判据（与pB116卖出规则配套）。
  tags: [rule, stable-grower, crowding]
  task_ids: [task-02, task-04]

- id: pB153
  title: 要点｜仅因便宜买入前景普通的公司是肯定失败之道
  type: rule
  source_chapter: 第20章 20.2（L4195）
  source_quote: "仅仅因为股价便宜就买入一只发展前景普通的公司股票是一种肯定失败的投资之道。"
  summary: 便宜不是买入理由，前景才是（低价股陷阱，pB124呼应）。
  tags: [rule, cheap-trap]
  task_ids: [task-04, task-10]

- id: pB154
  title: 要点｜因略微高估就卖出杰出快速增长股是肯定失败之道
  type: rule
  source_chapter: 第20章 20.2（L4197）
  source_quote: "因为股价似乎略为高估就卖出一只杰出的快速增长型公司股票是一种肯定失败的投资之道。"
  summary: 与pB110不过早卖出同源：杰出快速增长股容忍估值波动。
  tags: [rule, fast-grower, sell-discipline]
  task_ids: [task-02]

- id: pB155
  title: 要点｜盈利不会无缘无故增长；快速增长不可永续
  type: principle
  source_chapter: 第20章 20.2（L4199）
  source_quote: "公司盈利不会无缘无故地增长，快速增长型公司也不可能永远保持快速增长。"
  summary: 增长需要动力（pB06五途径）也有尽头（pB52三阶段）。
  tags: [principle, growth-limit]
  task_ids: [task-09, task-01]

- id: pB156
  title: 要点｜没买好股票不会让你损失一分钱
  type: principle
  source_chapter: 第20章 20.2（L4201）
  source_quote: "没有买入一只好股票并不会让你损失一分钱，即使是一只10倍股。"
  summary: 与危险说法10（pB130）同源：错过≠亏损。
  tags: [principle, fomo]
  task_ids: [task-10]

- id: pB157
  title: 要点｜一只股票本身并不知道你持有它
  type: principle
  source_chapter: 第20章 20.2（L4203）
  source_quote: "一只股票本身并不知道你持有它。"
  summary: 克服成本锚定与个人情感投射的心理格言（你的买入价与股票未来无关）。
  tags: [principle, psychology, anchoring]
  task_ids: [task-10]

- id: pB158
  title: 要点｜不要因股价大涨洋洋自得而不再关注基本面
  type: rule
  source_chapter: 第20章 20.2（L4205）
  source_quote: "不要过度迷恋你手中的大牛股，因为股价大涨而洋洋自得，不再关注公司的基本面变化。"
  summary: 持有大牛股期间仍须执行定期复查（pB51），防止得州航空式自我满足（pB53）。
  tags: [rule, holding-discipline, review]
  task_ids: [task-09, task-10]

- id: pB159
  title: 要点｜股价跌到零时无论买价多少亏损都是100%
  type: principle
  source_chapter: 第20章 20.2（L4207）
  source_quote: "如果一只股票价格跌到零，你的亏损是100%，让你输个精光、血本无归，不管你的买入价格是50美元、25美元、5美元还是2美元。"
  summary: 与危险说法4（pB124）同源：绝对亏损上限按投入金额计。
  tags: [principle, loss-math]
  task_ids: [task-10]

- id: pB160
  title: 要点｜高估+更好选择出现时，换股改善组合业绩
  type: rule
  source_chapter: 第20章 20.2（L4209）
  source_quote: |
    "根据公司基本面认真分析后，清除部分股票把资金配置到其他更好的股票上，能够进一步改善你的投资组合业绩。当股价高估以致与公司的真实表现相脱节，而且更好的投资选择出现时，卖掉高估的股票转向其他更好的股票。"
  summary: 换股的两个触发条件：估值与真实表现脱节+更好的选择出现（与pB100/pB103/pB114配套）。
  tags: [rule, rotation, sell-discipline]
  task_ids: [task-11, task-02]

- id: pB161
  title: 要点｜利好如翻出好牌应加大赌注，反之减少
  type: rule
  source_chapter: 第20章 20.2（L4211）
  source_quote: "公司出现利好，如同玩梭哈时翻出好牌，此时应该加大赌注，反之应该减少赌注。"
  summary: 加减仓的驱动是基本面新信息（梭哈比喻贯穿第14章复查），而非股价涨跌。
  tags: [rule, position-sizing, fundamentals-driven]
  task_ids: [task-09, task-11]

- id: pB162
  title: 要点｜卖盈利股抱亏损股=拔掉鲜花浇灌野草
  type: rule
  source_chapter: 第20章 20.2（L4213）
  source_quote: "卖出盈利股票却死抱着亏损股票不放，如同拔掉鲜花却浇灌野草，根本不可能因此改善投资业绩。"
  summary: 全书最著名的心理警告；正确的卖出依据是基本面变化（pB103），不是盈亏状态。
  tags: [rule, psychology, flowers-weeds, core-rule]
  task_ids: [task-10, task-02]

- id: pB163
  title: 要点｜认为自己不能战胜市场就买基金
  type: rule
  source_chapter: 第20章 20.2（L4215）
  source_quote: "如果你认为自己不能战胜市场，那么买入一只共同基金，这样会省去你自己投资需要花费的大量精力和金钱。"
  summary: 自我资格判断的分流出口（连续3-5年基金业绩≈指数则应改投指数基金或换基金）。
  tags: [rule, self-assessment, fund-alternative]
  task_ids: [task-12]

- id: pB164
  title: 要点｜总会有让人担心的事情发生，不要庸人自扰
  type: principle
  source_chapter: 第20章 20.2（L4217）
  source_quote: "总会有让人担心的事情发生，不要庸人自扰。"
  summary: 与pB113煽动效应、pB140担忧之墙同源的心理纪律。
  tags: [principle, worry, psychology]
  task_ids: [task-10]

- id: pB165
  title: 要点｜打开心灵之门，接纳所有创新的想法
  type: principle
  source_chapter: 第20章 20.2（L4219）
  source_quote: "打开你的心灵之门，接纳所有创新的想法。"
  summary: 保持对新事物（新品类、新业态）的开放性——与回避热门不矛盾：开放研究≠追逐热点。
  tags: [principle, open-mindedness]
  task_ids: [task-03, task-12]

- id: pB166
  title: 要点｜你并不需要"亲吻所有的女孩"（错过10倍股无碍战胜市场）
  type: principle
  source_chapter: 第20章 20.2（L4221）
  source_quote: "你并不需要'亲吻所有的女孩'。我也曾错过许多10倍股，但这并不妨碍我仍然能够战胜市场。"
  summary: 与pB130/pB156同源：错过的机会不构成业绩损失；抓住属于自己能力圈内的少数机会即可。
  tags: [principle, fomo, circle-of-competence]
  task_ids: [task-10, task-12]
```

## 提取统计

- 总计 166 条（pB01-pB166）
- 类型分布：principle 约 40 条 / rule 约 70 条 / checklist 约 12 条 / template 约 7 条 / calculation 约 25 条（部分兼具 rule 性质）
- 重点覆盖：
  - 13项财务指标逐项口径：pB27-pB50（含福特16.30美元全算例 pB25/pB30、75/25负债线 pB32、银行短债最危险 pB33、现金流量10%标准 pB41、存货增速 pB43、20%vs10%复利 pB46、税前利润率弹性 pB50）
  - P/E=增长率规则 pB28、(g+股息率)/P/E≥1.5 公式 pB29、一半/两倍规则并入 pB28
  - 整体市场P/E风向标 pB05
  - 收益5途径 pB06
  - 第15章六类核查清单逐类：pB54-pB60；15.2要点32条逐条：pB61-pB92
  - 分类型卖出清单逐类（含全部阈值）：pB115-pB120
  - 组合规则：pB93-pB106（3-10只、12-15%期望、换股不换现金、跌25%追加等）
  - 12种危险说法逐条：pB121-pB132
  - 期权期货95%亏损 pB133-pB135、卖空三缺陷 pB136
  - 买入时机：pB107-pB109（避税期/崩盘期+表17-1/17-2数据）
  - 20.2要点26条逐条：pB141-pB166
