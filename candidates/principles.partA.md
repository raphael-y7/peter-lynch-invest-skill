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
