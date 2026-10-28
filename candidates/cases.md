# 《彼得·林奇的成功投资》案例提取（case-extractor 产出）

> 提取时间：2026-10-26。取材路径：FTS 检索（`.cangjie/index/lexical.sqlite`，80+ 查询词）+ 全书原文通读核验（source_合并转写稿.md，4221 行）。
> example_kind 口径：firsthand＝林奇本人/麦哲伦的操作或亲历；reported_case＝林奇转述的他人/历史事件（含化名人物故事，已注明）；worked_example＝书中演算、表格、假设情境或"梦中公司"式例题。
> 所有数字均已与原文逐条核对；同一公司多处出现的，各条按其方法论绑定分别收录并注明行号。

---

## 导论

- id: c01
  title: 表0-1 A/B投资策略对比——一只Stop & Shop改变全局
  type: case
  example_kind: worked_example
  source_chapter: 导论0.1 L30-63
  source_quote: |
    "假设1980年12月22日你投资了10000美元买入表0-1中的10只股票，并且一直持有到1983年10月4日……B投资策略……你又多买入了一只股票Stop＆Shop，后来这只股票上涨了10倍。"
  summary: |
    1980-12-22 至 1983-10-04 的演算：10 只股票组合（伯利滋钢铁-8%、可口可乐+60.3%、通用汽车+58.7% 等）合计 +162.7%，$10000 变 $13040（+30.4%），跑输同期标普500的+40.6%；多买一只 Stop & Shop（$6→$60，+900%）后组合变 $21060（+110.6%）。论证"小组合里一只10倍股足以翻盘"。
  bound_to: ["业余投资者的身边信息优势", "组合构建与持有纪律"]
  outcome: 书中给出完整结果：一只10倍股使总收益率从30.4%提高到110.6%；若再加仓回报还能翻两番。
  tags: [worked-example, tenbagger, portfolio]
  task_ids: [task-11, task-12]

- id: c02
  title: "身边公司等额投资"演算组：斯巴鲁/甜甜圈/Gap/La Quinta/SCI/苹果
  type: case
  example_kind: worked_example
  source_chapter: 导论0.2 L67-79
  source_quote: |
    "如果你在购买斯巴鲁汽车时也购买了斯巴鲁汽车公司的股票，那么你现在就成了一位百万富翁？"
  summary: |
    一组"花多少钱买东西就投多少钱买股票"的演算：斯巴鲁 1977 年 $2 买入、1986 年复权价 $312，涨 156 倍，$6410 变 $100 万；Dunkin' Donuts 1982 年一年 $270 → 4 年后 $1539（6倍股），$10000→$47000；Gap 1976 年 $180（10股×$18发行价）→1987 年 $4672.50，$10000→$250000；La Quinta 1973 年 31 晚房费 $371.38 →10 年后 $4363.08；SCI 1969 年葬礼费 $980 →1987 年 $14352.19；苹果电脑 1982 年 $2000 →5 年后 $11950。
  bound_to: ["业余投资者的身边信息优势"]
  outcome: 每一例书中均给出最终市值；这些公司均为真实公司，演算口径为"等额投资"。
  tags: [worked-example, consumer-advantage]
  task_ids: [task-12]

- id: c03
  title: 新英格兰消防员投资Tambrands
  type: case
  example_kind: reported_case
  source_chapter: 导论0.3 L85-87
  source_quote: |
    "这位消防队员注意到当地一家叫做Tambrands的生产女性卫生用品的工厂……他和家人一起投资了2000美元购买了一些Tambrands的股票……到了1972年，这个消防员已经变成了一位百万富翁。"
  summary: |
    20 世纪 50 年代，消防员从工厂快速扩张推断业务兴旺，投入 $2000，随后 5 年每年再投 $2000，到 1972 年成为百万富翁。作者以此说明业余者用普通常识即可战胜专家，并说他本人用"跟这位消防员完全相同的方法"找到许多大牛股。
  bound_to: ["业余投资者的身边信息优势"]
  outcome: 到 1972 年成为百万富翁（原文明确）。
  tags: [reported-case, common-sense, amateur-edge]
  task_ids: [task-12]

- id: c04
  title: 卡罗琳在超级市场发现L'eggs（Hanes公司）
  type: case
  example_kind: firsthand
  source_chapter: 导论0.3 L93-105
  source_quote: |
    "卡罗琳去超级市场买东西时却发现了这家优秀公司……Hanes公司在被联合食品公司收购之前它的股价上涨了6倍……我确信如果Hanes公司没有被收购的话它的股价将会上涨50倍。"
  summary: |
    70 年代初林奇任纺织业分析师却漏掉 L'eggs；妻子卡罗琳购物试穿发现产品（重磅生丝、超市渠道；超市购买机会是百货店的 12 倍）。林奇随后研究并把 Hanes 推荐给富达组合管理人。Hanes 被联合食品（萨拉·李）收购前涨 6 倍；畅销全国后第一、二、三年买入仍至少获 3 倍回报。
  bound_to: ["业余投资者的身边信息优势", "13条选股准则（重复购买的产品）"]
  outcome: 涨 6 倍后被收购；未被收购则估 50 倍；L'eggs 此后 10 年销量持续增长。
  tags: [firsthand, legs, wife-discovery]
  task_ids: [task-12, task-03]

- id: c05
  title: 汉德图斯夫妇：温彻斯特磁盘 vs The Limited（化名故事）
  type: case
  example_kind: reported_case
  source_chapter: 导论0.3 L107-141
  source_quote: |
    "拿出3000美元辛苦赚到的钱来购买温彻斯特公司的股票……结果导致其股价从10美元跌到了5美元……The Limited服装公司的股价已经持续上涨了很多，从1979年12月份的不到50美分……上涨到了1983年的9美元。"
  summary: |
    化名讽刺案例：丈夫听《华尔街日报》+股评买温彻斯特磁盘 $3000（$10→$5，赔 $1500）；妻子逛到的 The Limited 从 1979 年 12 月 <50 美分涨到 1983 年 $9（20 倍，自 1979 年起最终超 100 倍，高点 $52.875）。丈夫直到 1987 年底（3 种刊物吹捧、30 位分析师追踪后）才以近高点 $50 买入，跌到 $16、反弹 $25 时割肉。原文明言这是"化名"保护的朋友。
  bound_to: ["业余投资者的身边信息优势", "避而不买清单（热门股/听消息）", "12种危险说法"]
  outcome: 温彻斯特赔 $1500；The Limited 100 倍；汉德图斯 $50 买入后 $25 卖出。
  tags: [reported-case, pseudonym, houndstooth]
  task_ids: [task-04, task-10, task-12]

- id: c06
  title: 林奇自己也错过The Limited并在高位买入
  type: case
  example_kind: firsthand
  source_chapter: 导论0.4 L145
  source_quote: |
    "我也和汉德图斯一样在The Limited公司受到广泛关注并且经营状况已经开始恶化的时候才买入了它的股票，甚至直到现在我还持有着这只让我赔了很多钱的股票。"
  summary: |
    作者自曝：妻子同样在购物中心见过 The Limited 生意兴隆，但他与汉德图斯一样没有在蒸蒸日上时买入，反而在受关注、基本面恶化后买入并赔钱持有。用来自证"错过身边大牛股人人平等"，佐证身边优势论而非神化作者。
  bound_to: ["业余投资者的身边信息优势"]
  outcome: 该笔持仓赔钱，写书时仍持有（原文明确）。
  tags: [firsthand, mistake, limited]
  task_ids: [task-12]

- id: c07
  title: Coleco椰菜娃娃——畅销产品救不了烂资产负债表
  type: case
  example_kind: reported_case
  source_chapter: 导论0.6 L167
  source_quote: |
    "仅仅凭着生产20世纪最畅销的玩具'椰菜娃娃'仍然无法挽救这家资产负债表非常糟糕的公司最终陷入破产的命运……1983年最高上涨到65美元，但是股价最终还是下跌到了只有1.75美元，1988年这家公司宣告破产。"
  summary: |
    凭家庭视频游戏与椰菜娃娃两次热潮，Coleco 一年左右大涨，1983 年最高 $65；因资产负债表糟糕最终跌至 $1.75，1988 年破产。与玩具反斗城/苹果/皮埃蒙特对照，说明"找到潜力公司只是第一步，还须研究分析"。
  bound_to: ["避而不买清单（热门产品≠好股票）", "13项财务指标（资产负债表）"]
  outcome: 1988 年破产（原文明确）。
  tags: [reported-case, cabbage-patch, balance-sheet]
  task_ids: [task-04, task-06]

## 第1章

- id: c08
  title: 外祖父与城市服务公司（Cities Service）
  type: case
  example_kind: reported_case
  source_chapter: 第1章 L199
  source_quote: |
    "他以为这是一家供应自来水的公用事业公司，后来他去纽约旅行时却发现这家公司原来竟是一家石油公司，于是马上就把股票卖掉了，可是从他卖出股票以后，城市服务公司的股价上涨了50倍。"
  summary: |
    林奇外祖父以为买的是自来水公用事业，发现是石油公司后立刻卖出，错失 50 倍上涨。用来说明"不懂就卖"的家族教训与逆向持有纪律。
  bound_to: ["入市前三问（了解自己在买什么）", "业余投资者的身边信息优势"]
  outcome: 卖出后上涨 50 倍（原文明确）。
  tags: [reported-case, family, missed]
  task_ids: [task-12]

- id: c09
  title: 飞虎航空——林奇的第一只5倍股（1963年$7买入）
  type: case
  example_kind: firsthand
  source_chapter: 第1章 L225-231
  source_quote: |
    "1963年上大学二年级时，我以每股7美元的价格买入了自己的第一只股票'飞虎航空'……不到两年时间，飞虎航空的股价就涨到了32.75美元，这是我寻找到的第一只5倍股。"
  summary: |
    大二时基于一篇空运前景文章以 $7 买入（研究前提其实错了——真正催化是越战空运），不到两年涨到 $32.75（5 倍），获利用于支付沃顿商学院研究生学费。奠定其"大牛股真实存在"的信念。
  bound_to: ["入市前三问与个人素质", "业余投资者的身边信息优势"]
  outcome: 不到两年 5 倍；利润支付了研究生学费（原文明确）。
  tags: [firsthand, first-stock, flying-tiger]
  task_ids: [task-12]

- id: c10
  title: 缅因州制糖公司——士兵休假买入的惨败
  type: case
  example_kind: firsthand
  source_chapter: 第1章 L257-263
  source_quote: |
    "缅因州制糖公司的股票——我坚信会稳赚不赔的一只股票，却让我损失惨重……炼糖厂不得不因业务量不足而关门停业……它的股价跌到了每股6美分。"
  summary: |
    服兵役休假期间听朋友推荐买入缅因州制糖；公司游说农民种甜菜，但谨小慎慢的农民第一年只试种 1/4 英亩、次年半英亩、第三年才 1 英亩，炼糖厂业务量不足倒闭、公司破产，股价跌至 $0.06。教训：让"性子比老牛慢"的参与者实现增长是痴人说梦。
  bound_to: ["避而不买清单（不懂的公司/故事股票）"]
  outcome: 公司破产、股价 $0.06，作者损失惨重（原文明确）。
  tags: [firsthand, mistake, maine-sugar]
  task_ids: [task-04]

## 第2章

- id: c11
  title: The Limited与华尔街滞后性（1969上市→1985年才被追捧）
  type: case
  example_kind: reported_case
  source_chapter: 第2章2.1 L313-333
  source_quote: |
    "直到1985年The Limited公司的股票上涨到每股15美元时，大多数分析师才注意到这只大牛股……使股价一路狂涨到52.875美元——如此之高的股价已经远远脱离了公司的基本面。"
  summary: |
    1969 年由哥伦布小券商承销上市，多年仅 1-2 位分析师追踪（苏茜·霍姆斯、玛吉·吉莉姆因暴风雪被困机场逛店才发现）；1979 年仅 2 家机构持股 0.6%；1979 年 50 美分买入者到 1983 年 $9 已赚 18 倍；1985 年 $15 后分析师蜂拥（37 位）、股价冲至 $52.875 脱离基本面。同节数据群：斯巴鲁最大涨幅期仅三四位分析师；Dunkin' Donuts 1977-86 涨 25 倍仅 2 家大券商追踪；Pep Boys 1981 年 <$1 →1985 年 $9.5 仅 3 位分析师；Stop & Shop $5→$50 分析师 1→4 人；IBM 56 位、埃克森 44 位。
  bound_to: ["专业投资者的制度性劣势（滞后性）"]
  outcome: 早期买入者 18 倍；追高者承受其后的下跌（1984 年即曾从 $9 跌至 $5）。
  tags: [reported-case, street-lag, limited]
  task_ids: [task-12]

- id: c12
  title: 布恩·道格、弗林特与七棵橡树——"掩埋罪证"
  type: case
  example_kind: reported_case
  source_chapter: 第2章2.2-2.3 L357-393, L401-411
  source_quote: |
    "道格为基金买入的成本价格是每股10美元，而现在的股价是每股6美元。'这是怎么回事？'……后来股价上涨了10倍……即使克莱斯勒，可能也要等到……股价也相应回到较高价位以后，才符合养老基金购买股票的标准。"
  summary: |
    化名故事：受托管理人道格因客户弗林特每季审查，被迫为暂时亏损的七棵橡树（$10→$6，处理超市优惠券的枯燥生意，后来涨 10 倍）辩护，最终"掩埋罪证"卖掉、抱住 1967 年起就持有的施乐（$32→$52）与西尔斯（$25→$34.875）。同章：SEC 规则（持单一公司≤10%股本、单股≤基金5%资产）逼退小公司；Scudder 等在克莱斯勒 $3.5 最低点前停止追踪、$30 才重新列入。
  bound_to: ["专业投资者的制度性劣势（滞后性）", "13条选股准则（业务枯燥）"]
  outcome: 七棵橡树后来涨 10 倍；施乐多年持有收益跑不赢货币基金（原文明确）。
  tags: [reported-case, pseudonym, burying-evidence, seven-oaks]
  task_ids: [task-12, task-03]

## 第3章

- id: c13
  title: 曼哈顿岛24美元的复利 + 表3-1六十年四类资产对比
  type: case
  example_kind: worked_example
  source_chapter: 第3章3.2 L455-510
  source_quote: |
    "如果以年利率8%对24美元计算复利……经过362年，这些印第安人可能已经凭此积累起一笔价值接近30万亿美元的财富……1927年，如果你分别在表3-1中所列的4种金融工具上各投资了1000美元……60年后……普通股票272 000美元。"
  summary: |
    复利演算：1626 年 $24 按 8% 复利 362 年 ≈ 30 万亿美元（曼哈顿土地估值仅 281 亿美元）；6% 则为 347 亿美元。表3-1：1927 年各投 $1000、60 年后国库券 $7400、政府债券 $13200、公司债券 $17600、普通股票 $272000（股票是债券的 15 倍）。同期股票平均年收益 9.8% vs 公司债券 5%。
  bound_to: ["股票长期收益远超债券"]
  outcome: 演算结果如上；书中以此确立"长期持有股票"的收益基础。
  tags: [worked-example, compounding, table-3-1]
  task_ids: [task-12]

- id: c14
  title: RCA与伯利恒钢铁——蓝筹长期持有可能一无所获
  type: case
  example_kind: reported_case
  source_chapter: 第3章3.3 L520-532
  source_quote: |
    "RCA公司……1986年通用电气公司收购RCA公司时所支付的价格为每股66.50美元，竟然与1967年的股票市价一模一样……伯利恒钢铁公司现在的股价也远远低于30年前它在1958年的最高价位60美元。"
  summary: |
    "最稳妥"的 RCA 1986 年 $66.50 与 1967 年持平、仅比 1929 年高点 $38.25 涨 74%（57 年年回报不足 1%）；伯利恒钢铁远低于 1958 年 $60 高点。1972-74 大跌中百时美 $9→$4、Teledyne $11→$3、麦当劳 $15→$4。另：华盛顿公共电力（Whoops）债券违约说明债券也有风险。
  bound_to: ["股票长期收益远超债券（前提：方法与价格正确）", "入市前三问（风险取决于方法）"]
  outcome: 各例结局如原文数字；结论"不存在不容错过的蓝筹股"。
  tags: [reported-case, blue-chip-risk, rca]
  task_ids: [task-12]

- id: c15
  title: 岳母的休斯敦工业 vs 母亲的联合爱迪生——"安全股"不赚钱
  type: case
  example_kind: firsthand
  source_chapter: 第3章3.4 L566；第7章7.3.5 L1374；图13-1 L2910-2957
  source_quote: |
    "我建议她买休斯敦工业……在10多年间股价几乎一动不动。我认为我总可以用我母亲的钱'赌上一把'吧，于是我给我母亲买了一只'比较危险'的联合爱迪生公司的股票，结果这只股票上涨了6倍。"
  summary: |
    林奇给岳母买"绝对安全"的休斯敦工业，10 多年不动（图7-1 平坦如特拉华州）；给母亲买"危险"的联合爱迪生，涨 6 倍。联合爱迪生 1974 年曾 $10→$3（"谁会想到"型困境反转），后反弹至 1987 年 $52，并从加拿大买电省下资本开支、积累几十亿美元现金回购提息。论证"风险取决于投资者而非公司类型"。
  bound_to: ["六类公司分类法（缓慢增长 vs 困境反转）", "入市前三问（风险取决于方法）"]
  outcome: 休斯敦工业 10 余年不动；联合爱迪生 6 倍、1987 年达 $52（原文明确）。
  tags: [firsthand, houston-industries, con-edison]
  task_ids: [task-01, task-12]

## 第4章

- id: c16
  title: 寡妇德克斯特的哈佛学费钱——三年内要用的钱不入市
  type: case
  example_kind: worked_example
  source_chapter: 第4章4.2 L612-616
  source_quote: |
    "如果你在两三年之内不得不为孩子支付大学学费，那么就不应该把这笔钱用来投资股票……蓝筹股可能也会在三年甚至五年的时间里一直下跌或者一动也不动。"
  summary: |
    假设情境：寡妇之子德克斯特上高二、可能进哈佛但无奖学金，想靠买蓝筹股凑学费。书中判定：即使是蓝筹股，两三年维度涨跌与掷硬币无异，届时市场若突然大跌，孩子只能上夜校。配套规则：入市资金仅限于"损失了也不影响生活"的部分。
  bound_to: ["入市前三问（未来需要用钱吗）"]
  outcome: 书中结论：这种情况连蓝筹股也不该买（假设情境，无真实结果）。
  tags: [worked-example, self-test, money-needed]
  task_ids: [task-12]

## 第5章

- id: c17
  title: 巴菲特与伯克希尔·哈撒韦——"股市不在我关心范围之内"
  type: case
  example_kind: reported_case
  source_chapter: 第5章5.3 L706-708
  source_quote: |
    "20世纪60年代初期，这家卓越的公司的股票每股股价为7美元，现在则上涨到了每股4900美元。当时向伯克希尔哈撒韦公司股票投资2000美元持有到现在能够获得700倍即140万美元的投资回报。"
  summary: |
    引巴菲特"股票市场根本不在我所关心的范围之内"与高估时退还全部资金的举动，佐证"投资的是公司不是股市"。伯克希尔 60 年代初 $7 → 写书时 $4900；$2000 持有至今 = 140 万美元（700 倍）。
  bound_to: ["不预测市场，投资的是公司"]
  outcome: 700 倍回报（书中口径，原文明确）。
  tags: [reported-case, buffett, berkshire]
  task_ids: [task-14]

- id: c18
  title: 1981年的Dreyfus——股市最差年份的20倍股
  type: case
  example_kind: firsthand
  source_chapter: 第5章5.3 L710
  source_quote: |
    "20世纪80年代中股票市场下跌的唯一年份是1981年，然而这一年却是购买Dreyfus的最佳时刻，从这一年起它开始了从每股2美元到40美元的令人难以置信的上涨，但是我却生生错过了这只上涨20倍的大牛股。"
  summary: |
    1981 年是 80 年代股市唯一下跌的年份，却正是买 Dreyfus 的最佳时机（$2→$40，20 倍），林奇亲自错过。用于论证"我最喜欢的10倍股中有几只恰恰在行情糟糕时期涨幅最大"（另举 Taco Bell 在两次衰退中直线上涨）。
  bound_to: ["不预测市场，投资的是公司", "买入时机（崩盘/低迷期）"]
  outcome: $2→$40（20 倍），林奇当时错过（原文明确）。
  tags: [firsthand, missed, dreyfus]
  task_ids: [task-14]

- id: c19
  title: 预测对了行业仍会亏钱：Radice/Fortune/人民航空/泛美/LTV vs Nucor
  type: case
  example_kind: reported_case
  source_chapter: 第5章5.3 L714-716
  source_quote: |
    "LTV公司的股票在1981～1986年间，从每股的26.5美元跌到了1.125美元。大致上也是在同一时期，同样是钢铁行业的Nucor公司的股票却从每股10美元上涨到了50美元。（两只股票我都买了……）"
  summary: |
    即便预测准了行业繁荣，选错公司照样巨亏：预测到佛罗里达地产繁荣而买 Radice 亏 95%；计算机行业繁荣而买 Fortune System（1983 年 $22→1984 年 $1.875）；航空前景好而买人民航空（倒闭）或泛美（1983 年 $9→1984 年 $4）。同为钢铁复苏：LTV $26.5→$1.125，Nucor $10→$50。林奇坦承两只都买了、却卖了 Nucor 留下 LTV（亲历自嘲）。
  bound_to: ["不预测市场，投资的是公司", "12种危险说法"]
  outcome: 各例结局如数字；林奇留下的是跌 96% 的那只（原文明确）。
  tags: [reported-case, firsthand-element, stock-picking-over-forecast]
  task_ids: [task-14, task-10]

## 第6章

- id: c20
  title: 泰胃美与史克必成——病人和医生早于华尔街的10倍股
  type: case
  example_kind: reported_case
  source_chapter: 第6章6.1 L802-808；图6-1 L810-848；L850
  source_quote: |
    "受益于十分畅销的泰胃美，这家公司的股票从1977年的每股7.5美元上涨到了1987年的每股72美元……1974～1976年，该药进行临床试验期间……股价从每股4美元缓缓上涨到了每股7美元，1977年当政府批准泰胃美可以正式上市销售时，股价为每股11美元。"
  summary: |
    泰胃美 1976 年上市；临床试验期 $4→$7，1977 年获批时 $11，此后一路涨至 $72（1987）。图6-1 中文点评："你可以在FDA批准泰胃美上市以后的两年内买入该股票，你至少还可以获利3倍。"同类第二机会：葛兰素善胃得 1983 年中期 $7.5→1987 年 $30。药剂师/病人/医生早于华尔街知道畅销。
  bound_to: ["业余投资者的身边信息优势", "13条选股准则（重复购买的产品）"]
  outcome: 史克必成 4→72 美元；善胃得 7.5→30 美元（原文明确）。
  tags: [reported-case, tagamet, smithkline, zantac]
  task_ids: [task-12, task-03]

- id: c21
  title: Storer Communications——行业内人人可算的隐蔽资产
  type: case
  example_kind: reported_case
  source_chapter: 第6章6.2 L882
  source_quote: |
    "Storer Communications及其分公司的许多雇员……都可以计算出Storer的电视台和有线网络的真实资产价值相当于每股100美元，而它的股票价格却只有每股30美元……1985年下半年Storer的股票以每股93.50美元被收购进行私有化。"
  summary: |
    电视台/有线网络员工、摄影师、装光缆的工人都能算出资产价值 $100/股，而股价仅 $30。1985 年下半年以 $93.50 被私有化收购；1988 年回看该价仍非常便宜。论证行业内工作者的专业信息优势。
  bound_to: ["业余投资者的身边信息优势", "六类公司分类法（隐蔽资产型）"]
  outcome: 以 $93.50 被收购私有化（原文明确）。
  tags: [reported-case, storer, hidden-asset]
  task_ids: [task-01, task-12]

- id: c22
  title: 基金业大繁荣中一股未买——Dreyfus/Franklin/Federated
  type: case
  example_kind: firsthand
  source_chapter: 第6章6.3 L888-941
  source_quote: |
    "1977年Dreyfus基金公司的股票为40美分，到了1986年上涨到接近40美元，9年时间上涨了100倍……那么到底我从这几家基金公司大牛股上赚了多少钱呢？一分钱也没有。"
  summary: |
    林奇身在富达近 20 年、对基金业最熟悉（"坐在金山银山上"），却一股未买：Dreyfus 1977 年 $0.40→1986 年近 $40（100 倍，图6-2）；Franklin 涨 138 倍；Federated 被 Aetna 收购前涨 50 倍。1987 年大跌后他第二次抓住 Dreyfus（详见 c_ 第17章条目）。全书最重的亲历失误案例，论证"购买你所了解的公司股票"。
  bound_to: ["业余投资者的身边信息优势", "专业投资者的制度性劣势"]
  outcome: 三只均零持仓、零收益；1987 年后才补上 Dreyfus（原文明确）。
  tags: [firsthand, missed, dreyfus, franklin]
  task_ids: [task-12]

- id: c23
  title: 表6-1 我错过的大牛股（a–m 字母名单）
  type: case
  example_kind: firsthand
  source_chapter: 第6章6.3 L943-985
  source_quote: |
    "表6-1所列的只是我掌管麦哲伦基金期间错过或者过早卖出的10倍股中的一小部分股票……仅仅包括从英文名称开头字母为'a'到开头字母为'm'的公司……把它们全部写下来会让我累得够呛。"
  summary: |
    两页名单列 70+ 只错过或过早卖出的 10 倍股（AAR、Ball、Capital Cities、Cray Research、Geico、The Gap、Lockheed、Marriott、Melville、Mylan 等，止于字母 m）。部分因没耐心持有过早卖出只赚一点，部分因时机混乱亏损。
  bound_to: ["组合构建与持有纪律", "业余投资者的身边信息优势"]
  outcome: 名单本身即结果记录；作者自注"错过的都补得回来"依赖组合能力。
  tags: [firsthand, missed-list, table-6-1]
  task_ids: [task-11]

- id: c24
  title: 自动数据处理公司（ADP）——600倍的业务枯燥公司
  type: case
  example_kind: reported_case
  source_chapter: 第6章 L790-796；第8章8.1.1 L1470-1472；第8章8.1.11 L1659
  source_quote: |
    "这家业务十分平凡的公司的股票最初以每股6美分（根据股票分割进行股价调整）的价格公开上市，现在的股价已经上涨到每股40美元，这是一只长期持有上涨600倍的超级大牛股。"
  summary: |
    ADP 一周为 18 万家公司处理 900 万份薪水支票；1961 年上市后盈利年年增长从未下降，最差的 1982-83 衰退期仍增 11%；股价 6 美分→$40（600 倍），1987 年大跌前曾达 $54；账上现金是负债 2 倍。作为"高科技用户受益者"（电脑降价→其成本降）与"名字/业务枯燥"准则的头号例证。
  bound_to: ["13条选股准则（名字枯燥/业务枯燥/高科技用户）"]
  outcome: 600 倍、盈利零年度下降（原文明确）。
  tags: [reported-case, adp, boring-business]
  task_ids: [task-03]

## 第7章

- id: c25
  title: 帮宝适 vs L'eggs——产品对净利润占比的测算（含Retin-A/Bufferin/Sterling对照）
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.1 L1011-1023；第13章13.1 L2802-2806
  source_quote: |
    "帮宝适牌纸尿裤的销售收入仅占整个公司销售收入的一小部分……远远不及L'eggs连裤袜对Hanes这样的小型公司的影响程度那么巨大……强生公司的股票两天内……上涨了8美元，使得整个公司股票市值增加了14亿美元。"
  summary: |
    同一周内两个对照：强生 Retin-A 抗皱新闻使股价两天（1988-1-21/22）涨 $8、市值增 14 亿美元，但该产品上年销售仅 3000 万美元且新适应症未经 FDA 批准；百时美 Bufferin 阿司匹林研究报告只令股价微涨 $0.50 至 $42.875，因 Bufferin 国内销售 7500 万美元 < 总销售 53 亿美元的 1.5%。Sterling 拜耳阿司匹林占收入 6.5%、利润近 15%。核心公式：先问"这种产品对净利润影响多大"。
  bound_to: ["产品销售占比测算（帮宝适谬误）"]
  outcome: 强生追高者被套（书中暗示）；百时美与 Sterling 反应与占比相称（原文数字明确）。
  tags: [reported-case, pampers, retin-a, bufferin]
  task_ids: [task-13]

- id: c26
  title: 通用电气——规模推算：市值接近GNP的1%
  type: case
  example_kind: worked_example
  source_chapter: 第7章7.2 L1033-1039
  source_quote: |
    "通用电气股票市值接近美国国民生产总值的1%……通用电气的股票有9亿股在市场上流通，总市值为390亿美元……除非它把整个世界都收购下来，否则真的没有什么其他办法能够让它快速增长了。"
  summary: |
    用简单数据推演"公司越大涨幅越小"：GE 每年盈利超 30 亿美元、市值 390 亿美元≈GNP 1%，消费者每花 1 美元约有 1 美分给它；如此体量不可能短期再涨数倍。同节对照：Pic 'N' Save vs 西尔斯、Nucor vs USX（钢铁复苏中小厂回报更好）、史克必成 vs 美国家居产品；伯林顿北方 $12→$6→$70 属例外（困境反转）。
  bound_to: ["公司越大涨幅越小", "六类公司分类法"]
  outcome: 推算性结论，无后续跟踪（未说明）。
  tags: [worked-example, ge, size]
  task_ids: [task-01, task-13]

- id: c27
  title: 宝洁与百时美的走势图——稳定增长型两问（图7-3/7-4）
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.3.2 L1150-1204；第15章15.1.3 L3270
  source_quote: |
    "如果你是在1963年买的这只股票，那么你的投资仅能上涨4倍。用25年时间持有一只股票只能获得4倍的投资收益率……简直跟购买债券或者持有货币基金差不多。"
  summary: |
    宝洁（图7-3）1980 年代表现出色，但 1963 年买入 25 年仅 4 倍；百时美（图7-4）收入 20 年只有一个季度下降、1981-82 经济崩溃期逆势上涨、1973-74 却因高估重挫。卖出规则：稳定增长股上涨 30-50% 即考虑换入未涨的同类；衰退期保留此类股票作防御。Kellogg 30 年无一季度收入下降、三次战争八次衰退未降股息。
  bound_to: ["六类公司分类法（稳定增长型）", "分类型卖出判据"]
  outcome: 宝洁 25 年 4 倍；百时美数次大跌中的表现如述（原文明确）。
  tags: [reported-case, pg, bristol-myers, stable-grower]
  task_ids: [task-01, task-02]

- id: c28
  title: 慢行业中的快速增长公司：Anheuser-Busch/万豪/Taco Bell/沃尔玛/Gap
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.3.3 L1272-1278
  source_quote: |
    "酒店行业的年增长率仅为2%，但万豪国际酒店集团公司在过去10年间通过不断抢占该行业的大部分市场份额，其年平均增长率达到了20%。"
  summary: |
    快速增长型公司不必属于热门行业：啤酒（增长缓慢）中的 Anheuser-Busch、酒店（年增 2%）中的万豪（10 年年均 20%）、快餐中的 Taco Bell、百货中的沃尔玛、服装零售中的 Gap——共同点是"在一个地方成功后一次次复制"。反例：60 年代塑料行业火热，陶氏化学由备受追捧沦为随周期起伏的普通化学公司。
  bound_to: ["六类公司分类法（快速增长型）", "13条选股准则（避开热门行业）"]
  outcome: 万豪 10 年年增 20%；陶氏增长放缓后股价随周期起伏（原文明确）。
  tags: [reported-case, marriott, slow-industry-fast-company]
  task_ids: [task-01, task-03]

- id: c29
  title: 克莱斯勒——麦哲伦赚得最多的一笔（1982年$6买入，5年15倍）
  type: case
  example_kind: firsthand
  source_chapter: 第7章7.3.5 L1356-1368；第13章13.4 L2878-2882；第16章16.2 L3460；第17章17.4.5 L3702
  source_quote: |
    "1982年初我开始购买它时股价是6美元（没有根据后来股票分割进行股价调整），然后我就一直看着这只股票在不到两年的时间里上涨了5倍，在5年的时间里上涨了15倍。我曾一度把我管理的基金资产的5%都投资在了克莱斯勒股票上。"
  summary: |
    林奇对克莱斯勒的完整操作与核查：1982 年初 $6 开始建仓，不足 2 年 5 倍、5 年 15 倍，仓位一度达基金资产 5%；若在最低 $1.50 抄底可获 32 倍。事前核查（13.4）：政府 14 亿美元贷款担保+股票期权、账上 10 亿美元现金、卖坦克分部给通用动力再获 3.36 亿美元——一两年内银行逼不死它；公司已成低成本厂商。风险回报（16.2）：顺利 +400%、不顺利 -100%，实际获 15 倍。卖出判据（17.4.5）：$2/$5/$10 是困境反转，1987 年中 $48 时已清债、重分类回周期型。
  bound_to: ["六类公司分类法（困境反转：政府救助型）", "13项财务指标（负债结构与现金头寸）", "分类型卖出判据"]
  outcome: 5 年 15 倍、对基金业绩影响最大（原文明确）。
  tags: [firsthand, chrysler, turnaround, flagship]
  task_ids: [task-01, task-02, task-06]

- id: c30
  title: 洛克希德——政府救助型困境反转（$1→$60）
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.3.5 L1366；第15章15.1.6 L3308
  source_quote: |
    "1973年它的股价只有1美元……你仍然可以在1977年以每股4美元的价格买入，然后在1986年以每股60美元的价格卖出，而我却错过了这只股票。"
  summary: |
    两段式案例：①1973 年 $1，政府出资救助后 1977 年 $4 仍可买，1986 年 $60（林奇错过）。②剥离亏损业务视角（15.1.6）：1980 年国防业务每股收益 $8.04，商用 L-1011 亏损 $6.54/股；1981 年 11 月宣布停产 L-1011、一次性冲销 $26/股；1982 年国防每股收益 $10.78——两年内每股收益 $1.50→$10.78；宣布停产时 $15 买入、4 年最高 $60（4 倍）。
  bound_to: ["六类公司分类法（困境反转）", "公司增加收益的5途径（剥离亏损业务）"]
  outcome: $4→$60；剥离后每股收益 1.50→10.78 美元（原文明确）。
  tags: [reported-case, lockheed, l-1011, divest]
  task_ids: [task-01, task-08]

- id: c31
  title: 佩恩中央铁路——破产蓝筹的大逆转与"最佳隐蔽资产型公司"
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.3.5 L1360-1368；第7章7.3.6 L1402-1404；第13章13.7 L2973；第13章13.8 L3039
  source_quote: |
    "佩恩中央铁路公司走出破产保护之后，公司的巨额亏损可以税前抵扣……那些年份公司所得税率高达50%，因此佩恩中央铁路公司浴火重生后就享有着50%的免税优势……这只股票后来上涨了8倍。"
  summary: |
    华尔街史上创伤最重的破产蓝筹上演大逆转（林奇称从克莱斯勒与佩恩中央的复苏中用绝对金额赚钱最多）。资产清单：税前亏损抵扣（50% 税率下的免税优势）、现金、佛罗里达大量土地、西弗吉尼亚煤矿、曼哈顿航空权；申请破产时账面价值仍高达每股 60 多美元（账面失灵的反例）；税损隐蔽资产使其 1979 年 $5→1985 年 $29（含被收购路径），整段涨 8 倍。
  bound_to: ["六类公司分类法（困境反转：重整型 + 隐蔽资产型）", "13项财务指标（账面价值陷阱/税收亏损抵扣）"]
  outcome: 涨 8 倍；1979 年 $5→1985 年 $29（原文明确）。
  tags: [reported-case, penn-central, hidden-asset, tax-loss]
  task_ids: [task-01, task-06]

- id: c32
  title: 三哩岛与通用公共事业（GPU）——"问题没想的那么严重"型
  type: case
  example_kind: firsthand
  source_chapter: 第7章7.3.5 L1376-1378；第17章17.4.5 L3704
  source_quote: |
    "1980年这只股票跌到3.375美元的低价位，但是你在1985年下半年仍可以每股15美元的价格买入，然后一直看着它在1988年10月上涨到38美元……我从三哩岛核电厂的控股公司通用公共事业公司的股票上赚了很多钱。"
  summary: |
    1979 年三哩岛堆心熔毁；两个买入信号：①1985 年宣布重启未受损的第二个核反应堆；②其他电力公司同意分担三哩岛清污成本。从形势平稳到信号出现提供了长达 7 年的低位买入窗口：1980 年低点 $3.375，1985 年下半年仍可 $15 买入，1988 年 10 月 $38。卖出判据（17.4.5）：$4/$8/$12 是困境反转，第二反应堆重启后已是优质公用事业股，现价 $38 可能到 $45 但不会到 $400。
  bound_to: ["六类公司分类法（困境反转：问题没那么严重型）", "定期重新核查（跟踪事件信号）", "分类型卖出判据"]
  outcome: 3.375→38 美元；林奇"赚了很多钱"（原文明确）。
  tags: [firsthand, three-mile-island, gpu]
  task_ids: [task-01, task-02, task-09]

- id: c33
  title: 博帕尔与Johns-Manville——赔偿不可估量的公司要避开
  type: case
  example_kind: firsthand
  source_chapter: 第7章7.3.5 L1380
  source_quote: |
    "我购买了Johns-Manville的股票，但我发现根本无法估计这家公司承担的赔偿义务总金额到底有多少，于是我就忍痛赔了些小钱把这只股票给卖掉了。"
  summary: |
    与 GPU 相对的边界案例：Union Carbide 博帕尔灾难（数千人死亡、索赔悬而未决）属"悲剧后果难以估量"，林奇直接避开；自己买入的 Johns-Manville（石棉诉讼）因无法估算赔偿总额而忍痛小亏卖出。为困境反转法划定能力边界。
  bound_to: ["六类公司分类法（困境反转的边界）"]
  outcome: Johns-Manville 小亏卖出；后文 18.5 提到该股最终没有涨回来（原文明确）。
  tags: [firsthand, johns-manville, bhopal, boundary]
  task_ids: [task-01, task-04]

- id: c34
  title: 玩具反斗城——从破产母公司分拆出的57倍
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.3.5 L1382；第8章8.1.4 L1506；第9章 L2044；第17章 L3580-3582
  source_quote: |
    "美国玩具反斗城公司从其母公司州际百货公司分拆出来之后独立经营，结果它的股价上涨了57倍。"
  summary: |
    "破产母公司中的好子公司"型困境反转：1978 年从破产的州际百货分拆独立（债权人获股补偿），通过向一家家购物中心复制扩张证明盈利能力。此案例在第8章作为"分拆上市"准则例证、第9章作为分拆类 IPO 优于新公司 IPO 的例证、第17章作为林奇过早卖出的教训（$1 买入、皮特里停止买入后 $5 卖出，1985 年 $25）。
  bound_to: ["六类公司分类法（困境反转：破产母公司好子公司）", "13条选股准则（分拆上市）", "组合构建与持有纪律（过早卖出）"]
  outcome: 57 倍（整段口径）；林奇本人 $1→$5 卖出，德罗斯持有获 25 倍（原文明确）。
  tags: [reported-case, toys-r-us, spinoff]
  task_ids: [task-01, task-03]

- id: c35
  title: Pebble Beach——石料场一项资产就超过整个公司市值
  type: case
  example_kind: reported_case
  source_chapter: 导论0.4 L147；第7章7.3.6 L1392
  source_quote: |
    "1976年底这家公司的股价为每股14.5美元，流通股份共有170万股……整个公司股票市值仅为2500万美元……仅仅这一个石料场就卖了3000万美元……当我站在卵石海滩高尔夫球场的草皮上时……却从来没有想起来问问这是不是一家上市公司。"
  summary: |
    1976 年底 $14.5/股、170 万股流通，总市值仅 2500 万美元；1979 年 5 月 20 世纪福克斯以 7200 万美元（$42.5/股）收购，次日转手单卖石料场即得 3000 万美元——一项资产超过三年前整家公司市值。买者等于免费获得土地、林场、2700 英亩、古木、酒店与两个高尔夫球场。林奇亲历失误：人站在球场上却没想到问"这是上市公司吗"。
  bound_to: ["六类公司分类法（隐蔽资产型）", "业余投资者的身边信息优势"]
  outcome: 被 $7200 万收购、石料场单独卖 $3000 万（原文明确）。
  tags: [reported-case, firsthand-miss, pebble-beach]
  task_ids: [task-01, task-12]

- id: c36
  title: Newhall土地农场——当地人才看得见的20倍
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.3.6 L1394-1396
  source_quote: |
    "有多少住在Newhall大牧场周围的人比华尔街的分析师早好几年就看到了这片土地的巨大升值？他们之中又有多少人仔细研究过这只从20世纪70年代早期开始上涨了20倍并且从1980年以来又上涨了4倍的股票？"
  summary: |
    纽交所上市、显而易见的隐蔽资产股：拥有旧金山湾区克威尔大牧场与洛杉矶以北 30 英里的 Newhall 大牧场（规划社区+购物中心）。每天经过的加州通勤者、参与开发的估价师/银行家/地产代理早于华尔街数年看到土地升值；股价自 70 年代早期涨 20 倍、1980 年以来又涨 4 倍。
  bound_to: ["六类公司分类法（隐蔽资产型）", "业余投资者的身边信息优势"]
  outcome: 20 倍 + 4 倍（原文明确）。
  tags: [reported-case, newhall, hidden-asset]
  task_ids: [task-01, task-12]

- id: c37
  title: Alico——佛罗里达养牛公司的土地价值（$20买入，10年后土地值$200）
  type: case
  example_kind: firsthand
  source_chapter: 第7章7.3.6 L1398
  source_quote: |
    "我所看到的不过是一些矮矮的从生松和小棕榈灌木林、一群在牧场上吃草的牛和二十来个假装卖力工作的员工……直到你计算出能以每股低于20美元的价格购买Alico的股票，并且10年后仅仅这块土地本身的价值就高达每股200多美元。"
  summary: |
    林奇亲自参观过的佛罗里达小型养牛公司：表象平平无奇，算账后每股 <$20 买入、10 年后仅土地价值即达每股 $200+。本地精明人本·希尔·格里芬持续买入等待华尔街发现，"现在他一定赚了大钱"。
  bound_to: ["六类公司分类法（隐蔽资产型）", "业余投资者的身边信息优势（当地优势）"]
  outcome: 土地价值 10 美元/股→200+美元/股（书中口径）；格里芬获利（推测性表述，原文用"一定"）。
  tags: [firsthand, alico, land-value]
  task_ids: [task-01, task-12]

- id: c38
  title: Liberty公司——电视台资产等于全部股价，保险公司白送
  type: case
  example_kind: firsthand
  source_chapter: 第7章7.3.6 L1406
  source_quote: |
    "现在我持有Liberty公司（Liberty Corp.）的股票，这是一家保险公司，仅它拥有的电视台资产一项的价值就超出了我购买该公司股票的价格……这个结果就是你投资这家很有价值的保险公司的成本——零。"
  summary: |
    林奇写书时正在持有的隐蔽资产头寸：电视台资产每股 $30＝股价 $30，相减后保险业务成本为零。展示"算出隐蔽资产→耐心等待"的操作骨架。
  bound_to: ["六类公司分类法（隐蔽资产型）", "13项财务指标（隐蔽资产）"]
  outcome: 未说明（写书时仍持有）。
  tags: [firsthand, liberty, tv-station]
  task_ids: [task-01, task-06]

- id: c39
  title: Telecommunication有线电视台——250倍的错失与"亲身体验"的价值
  type: case
  example_kind: firsthand
  source_chapter: 第7章7.3.6 L1408-1416
  source_quote: |
    "这是一家有线电视公司，1977年它的股价为12美分，10年后上涨到了31美元，上涨了250倍……我一直只持有有线电视行业股票微不足道的仓位……因为我直到1986年我居住的镇上才安装了有线电视。"
  summary: |
    美国最大有线电视公司 1977 年 $0.12→10 年后 $31（250 倍）。行业每用户价值一路上涨：15 年前 $200 → 10 年前 $400 → 5 年前 $1000 → 现在 $2200，行业内人人皆知。林奇只持了微不足道的仓位，坦承原因：家里 1987 年才装有有线电视，缺乏第一手体验，又没听同事莫里斯·史密斯拍桌子劝他加仓。结论："个人亲身体验的价值无法估量。"
  bound_to: ["六类公司分类法（隐蔽资产型）", "业余投资者的身边信息优势（亲身体验）"]
  outcome: 250 倍；林奇仅微量持仓（原文明确）。
  tags: [firsthand, missed, cable, telecommunication]
  task_ids: [task-01, task-12]

- id: c40
  title: 公司类型迁移群：陶氏/AMD/Stop & Shop/LTV/假日酒店/联邦百货/迪士尼
  type: case
  example_kind: reported_case
  source_chapter: 第7章7.4 L1422-1428
  source_quote: |
    "克莱斯勒公司原来是周期型公司，一度濒临破产，变成了一家困境反转型公司，经过成功重组后又变成了周期型公司……迪士尼公司在发展的过程中曾经属于过各种主要的公司类型。"
  summary: |
    类型会随生命周期迁移：陶氏化学与坦帕电气前 10 年快速增长、后 10 年缓慢增长；AMD 与德州仪器由快速增长变周期；Stop & Shop 由缓慢变快速（罕见反例）；LTV 由周期变困境反转；假日酒店增长放缓后因房地产被重新发现为隐蔽资产；联邦百货与联合百货因一流地段资产被整体收购；麦当劳未来可能成为房地产隐蔽资产型；迪士尼先后历经快速增长→稳定增长→隐蔽资产→80 年代中期困境反转。类型判断是动态的，需定期重估。
  bound_to: ["六类公司分类法（类型迁移）", "定期重新核查"]
  outcome: 各公司去向如述（原文明确）。
  tags: [reported-case, type-migration]
  task_ids: [task-01, task-09]

- id: c41
  title: Inco——年轻分析师的第一次成功卖出与17年后的回购
  type: case
  example_kind: firsthand
  source_chapter: 第7章 L1430-1432
  source_quote: |
    "1970年12月，我写了一份建议以每股47.875美元的价格卖出Inco股票的分析报告……1971年这只股票股价跌到了每股25美元，1978年又跌到了每股14美元，到了1982年跌到了每股8美元……这时我为富达麦哲伦基金再次大量买入了Inco公司的股票。"
  summary: |
    Inco 由增长型→周期型→困境反转型的完整亲历：1970 年 12 月林奇据镍消费下降、产能增加、劳力成本高三因素说服富达在 $47.875 清仓（为找买主还接受略低价）；股价 1971 年 $25、1978 年 $14、1982 年 $8；17 年后他以基金经理身份为麦哲伦再次大量买入——此时它已是困境反转型。
  bound_to: ["六类公司分类法（类型迁移）", "信息获取程序（基本面研究驱动卖出）"]
  outcome: 卖出后最深跌至 $8；二次买入的结果未说明。
  tags: [firsthand, inco, sell-then-rebuy]
  task_ids: [task-01]

## 第8章

- id: c42
  title: 名字枯燥群：Pep Boys——Manny, Moe, Jack 与联合石头
  type: case
  example_kind: reported_case
  source_chapter: 第8章8.1.1 L1468-1478
  source_quote: |
    "谁愿意把钱投在一家名字听起来像滑稽电视剧《三个活宝》的公司股票上呢？……而等到华尔街注意到这家公司的股票时，它的股价已经上涨10倍了。"
  summary: |
    名字越枯燥甚至可笑越好：自动数据处理、鲍勃·埃文斯农场、Shoney's、瓶盖瓶塞封口，冠军是 Pep Boys——Manny, Moe, Jack（像《三个活宝》）；华尔街注意到时它已涨 10 倍。反例：联合石头公司（Consolidated Rock）成功后改名 Conrock 又改 Calmat，"时髦"反而驱散了无人关注的红利。
  bound_to: ["13条选股准则（名字枯燥乏味）"]
  outcome: Pep Boys 被华尔街注意前已涨 10 倍（原文明确）。
  tags: [reported-case, pep-boys, boring-name]
  task_ids: [task-03]

- id: c43
  title: 业务枯燥群：瓶盖瓶塞、七棵橡树（$4→$33）与租车代理（$4→$16）
  type: case
  example_kind: reported_case
  source_chapter: 第8章8.1.2 L1482-1486
  source_quote: |
    "它的股票神不知鬼不觉地从每股4美元涨到了每股33美元……租车代理公司的股票以4美元的价格上市……当我上一次查阅这家公司的招股说明书时，它的股票已经上涨到了每股16美元。"
  summary: |
    瓶盖瓶塞封口造罐头盒和瓶盖、《时代》只采访艾科卡不采访它的 CEO；七棵橡树在墨西哥处理超市优惠券（像联储清算支票），$4→$33；租车代理（Agency Rent-A-Car）为修车客户提供代步车，$4 上市→$16。三家让 IBM 的表现"无地自容"。逻辑：业务枯燥→华尔街迟来→低价窗口长。
  bound_to: ["13条选股准则（业务枯燥乏味）"]
  outcome: 七棵橡树 4→33；租车代理 4→16（原文明确）。
  tags: [reported-case, crown-cork, seven-oaks, agency-rent-a-car]
  task_ids: [task-03]

- id: c44
  title: Safety-Kleen——清洗油污的令人厌恶的公司
  type: case
  example_kind: reported_case
  source_chapter: 第8章8.1.3 L1490-1494
  source_quote: |
    "Safety-Kleen派人跑遍所有的加油站，向它们提供一种能够清洗汽车零件上沾的油污的机器……这种脏兮兮、油乎乎的工作日复一日地在重复进行……盈利一直保持持续增长，每个季度公司利润都在增长。"
  summary: |
    从芝加哥生牛皮分拆独立（叠加 8.1.4 准则）；业务是给加油站洗零件、回收油泥并扩展到清除饭店厨具油污。没有分析师愿写它的报告、没有组合经理愿把它列入买入名单——这正是其可爱之处；与 ADP 一样盈利每季增长、股价持续上涨。名字中该用"c"却用"k"也是信号。
  bound_to: ["13条选股准则（业务令人厌恶/分拆）"]
  outcome: 盈利逐季增长（原文明确；未给具体倍数）。
  tags: [reported-case, safety-kleen, disgusting-business]
  task_ids: [task-03]

- id: c45
  title: Envirodyne——塑料叉子与热狗肠衣（$3→$36.875）
  type: case
  example_kind: firsthand
  source_chapter: 第8章8.1.3 L1496-1502
  source_quote: |
    "1985年9月我以每股3美元的价格买入这家公司的股票，1988年这只股票的最高价格达到了36.875美元……Envirodyne公司每股收益才从1985年的34美分增长到了1987年的2美元，1988年创下2.50美元的新高。"
  summary: |
    富达林产品分析师托马斯·斯威尼推荐；名字荒唐（"像能穿透臭氧层的东西"），实为塑料叉/吸管生产商（餐具业第二、吸管业第三、成本最低）。1985 年收购 Viskase（肠衣）、1986 年收购 Filmco（保鲜膜）；每股收益 1985 年 $0.34 → 1987 年 $2.00 → 1988 年 $2.50，现金流清偿收购债务。林奇 1985 年 9 月 $3 买入，1988 年最高 $36.875（约 12 倍）。
  bound_to: ["13条选股准则（业务令人厌恶/内部人士持股）"]
  outcome: $3→$36.875；EPS 0.34→2.50（原文明确）。
  tags: [firsthand, envirodyne, viskase]
  task_ids: [task-03]

- id: c46
  title: 表8-1 分拆上市公司表现 + 小贝尔七家公司（5年+170%）
  type: case
  example_kind: worked_example
  source_chapter: 第8章8.1.4 L1506-1571
  source_quote: |
    "从1983年11月到1988年10月，七家新成立的小贝尔公司的股票平均收益率是114%，再加上股息其总收益率超过了170%。这一收益率以近两倍的优势远远战胜了市场，并且战胜了大多数著名的共同基金，当然也包括我本人所掌管的麦哲伦基金。"
  summary: |
    表8-1 列 15 家表现良好与 4 家表现不佳的分拆公司（如 York International 首日 $14 最高 $59.75；可口可乐企业公司 $15.5→$14.5 属差生）。明星案例是 AT&T 1983 年解体分拆的七家小贝尔：1983.11-1988.10 平均涨 114%、含股息超 170%，近两倍战胜市场、也战胜麦哲伦。林奇本人抓住机会但"购买的股票数量有限"。方法论：分拆后 1-2 个月查内部人士是否在买。
  bound_to: ["13条选股准则（从母公司分拆出来）"]
  outcome: 小贝尔 5 年 +170%（含股息）；表8-1 各家价格数据完整（原文明确）。
  tags: [worked-example, spinoff, baby-bells, table-8-1]
  task_ids: [task-03]

- id: c47
  title: 废物管理公司（Waste Management）与赌场股——谣言即折扣
  type: case
  example_kind: firsthand
  source_chapter: 第8章8.1.6 L1583-1589
  source_quote: |
    "当时我看到他们穿的是印有'固体垃圾'（Solide Waste）的马球套头运动衫……如果你很幸运已经买入了这家垃圾处理公司的股票，那么到现在你的投资就会上涨100倍。"
  summary: |
    林奇亲历：垃圾处理公司高管穿着"固体垃圾"运动衫来富达开会推介。该行业兼有"处理有毒垃圾"与"被黑手党控制"两大传闻，吓退有身份的投资者、压低股价，早期买入者获 100 倍。对照：赌场股因黑手党传闻多年无人敢买，待假日酒店与希尔顿进入赌场业后成人人争抢的香饽饽。
  bound_to: ["13条选股准则（被谣言包围）"]
  outcome: 废物管理 100 倍（原文明确）。
  tags: [firsthand, waste-management, rumor]
  task_ids: [task-03]

- id: c48
  title: SCI丧葬服务——零增长行业的连锁整合（涨20倍后成为明星股反而跑输）
  type: case
  example_kind: reported_case
  source_chapter: 第2章2.1 L323-327；第8章8.1.7-8.1.8 L1593-1619
  source_quote: |
    "直到1986年才开始有一大批的机构投资者追捧SCI的股票……等到SCI公司股票受到华尔街充分关注时它已经上涨了20倍，但是自从成为人人热捧的明星股之后，它的市场表现却开始远远落后于大盘。"
  summary: |
    富达电子业分析师梵德海顿推荐（去得州旅行时发现）。SCI 连锁收购夫妻店殡仪馆成"殡葬业的麦当劳"：461 家殡仪馆、121 处公墓、76 家花店、21 家丧葬用品供应中心、3 家棺材配送中心；因承办霍华德·休斯葬礼而闻名。开创生前预付合同（现金复利增值，5 年年增 40%）；与 American General 换股交易免费回购 20% 股份。1969 年上市 10 年无分析师关注，1982 年希尔森关注时已涨 5 倍；1978 年买入持有到 1987 = 40 倍，而 1983 年 $12 买入 1987 年 $30.375 仅 1 倍多。1986 年机构持股超 50% 后，因两次棺材业收购失败、殡仪馆收购价大涨而跑输大盘——印证"华尔街充分关注=20倍已涨完"。
  bound_to: ["13条选股准则（业务压抑/零增长行业）", "专业投资者的制度性劣势（滞后性）"]
  outcome: 涨 20 倍后受捧，随后跑输大盘（原文明确）。
  tags: [reported-case, sci, funeral, zero-growth]
  task_ids: [task-03, task-12]

- id: c49
  title: 石料场利基三例：运费壁垒、专利与报纸
  type: case
  example_kind: worked_example
  source_chapter: 第8章8.1.9 L1623-1649
  source_quote: |
    "如果你已经拥有了布鲁克林地区的唯一一家石料加工场，那么事实上你已经获得了这个地区石料市场的垄断权……将这些不值钱的东西混合在一起形成的混凝料却能卖到3美元一吨。"
  summary: |
    利基的三种形态：①石料场——石头重、运费吃掉利润，天然形成地区排他特许权（混凝料 $3/吨；芝加哥的石料场抢不走布鲁克林的市场）；福克斯收购 Pebble Beach 正因它有石料场。②专利药——史克的泰胃美专利挡住竞争者 3 年临床试验。③地方垄断媒体——林奇大量买入联合出版公司（《波士顿环球报》占波士顿 90% 以上印刷广告收入）；甘尼特 90 家日报多为当地第一。附：查尔斯河繁殖实验室（养老鼠）让林奇"赚了一大笔钱"。
  bound_to: ["13条选股准则（利基）"]
  outcome: 联合出版与查尔斯河均获利（原文明确，未给倍数）。
  tags: [worked-example, niche, quarry, boston-globe]
  task_ids: [task-03]

- id: c50
  title: 内部人士买入信号——1:2.3 与崩盘后的4:1
  type: case
  example_kind: reported_case
  source_chapter: 第8章8.1.12 L1661-1675
  source_quote: |
    "一般来说，公司内部人士是自家公司股票的净卖方，通常他们的买入卖出比例是1:2.3。1987年8～10月股票指数下跌了1000点之后……公司内部人士买入卖出股票的比例是4:1……如果你看到一个年薪45000美元的员工买入了10000美元的自家公司股票时……意味深长的员工对公司未来充满信心地投下一票。"
  summary: |
    数据型案例：正常时期内部人士买卖比 1:2.3；1987 年 8-10 月指数跌 1000 点后转为 4:1。判别规则：多名副总裁各买 1000 股好过总裁一人买 5000 股；内部人士买入只有一个原因（认为股价低估）；卖出通常无意义。可通过 SEC 表格4与《价值线》等追踪。
  bound_to: ["13条选股准则（内部人士买入）"]
  outcome: 统计口径如上（原文明确）。
  tags: [reported-case, insider-buying]
  task_ids: [task-03]

- id: c51
  title: 回购的正反例：埃克森石油算术、Teledyne 高价回购与瓶盖瓶塞
  type: case
  example_kind: worked_example
  source_chapter: 第8章8.1.13 L1679-1687
  source_quote: |
    "埃克森公司每发现一桶新的石油大约要花费6美元，如果每股股票相当于价值3美元的一桶石油，那么在纽约股票交易所里每回购一股股票的经济效果就相当于发现了一桶价值3美元的石油。"
  summary: |
    回购的三个正面例证：①埃克森——钻孔找油 $6/桶 vs 每股股票含 $3 石油，回购等于半价"找油"；②国际乳品皇后为 60 年代回购先行者；③瓶盖瓶塞 20 年年年回购、从不派息、从不做无利并购，若持续"总有一天股价将会上涨到每股1万美元"；④Teledyne 董事长辛格尔顿始终以高于交易所报价回购（交易所 $5 时付 $7）。
  bound_to: ["13条选股准则（公司在回购股票）"]
  outcome: 各公司表现如述（原文明确）。
  tags: [worked-example, buyback, exxon, teledyne]
  task_ids: [task-03]

- id: c52
  title: 吉列与Navistar——不回购的代价与增发稀释
  type: case
  example_kind: reported_case
  source_chapter: 第8章8.1.13 L1689-1691；图8-1 L1693起
  source_quote: |
    "如果公司不是把资本分散投入到生产美容产品、化妆用具、圆珠笔、打火机……而是定期回购股票并提高股息，那么吉列公司的股价可能已经超过了每股100美元，而不是现在的每股35美元。"
  summary: |
    反面对照：吉列把现金撒向美容品、圆珠笔、打火机、数字手表等偏离主业的产品，若改为定期回购+提息，股价本可超 $100 而非现在的 $35（近 5 年才回归剃刀主业）。国际收割机（Navistar）为度过农用设备崩溃的财务危机增发数百万新股——公司虽重新盈利，但股份稀释使每股收益与股价对复苏几乎无反应。
  bound_to: ["13条选股准则（回购 vs 增发稀释）", "避而不买清单（多元恶化）"]
  outcome: 吉列 $35（对照假设 $100）；Navistar 复苏但股东未获显著回报（原文明确）。
  tags: [reported-case, gillette, navistar, dilution]
  task_ids: [task-03, task-04]

- id: c53
  title: Cajun清洁剂——"梦中的完美公司"（集13条优点于一身）
  type: case
  example_kind: worked_example
  source_chapter: 第8章8.2 L1856-1862
  source_quote: |
    "我以每股7.50美元的价格买了该公司的股票，我比Cajun公司董事的买价还便宜2.50美元！……别掐我。我还在做梦呢。"
  summary: |
    作者明示的虚构合成例题（"我还在做梦呢"）：上市 $8→$10 时董事们纷纷买入；远房亲戚推荐（皮夹克除霉唯一有效）；收益 4 年年增 20% 无一季下降、零负债、衰退期表现良好；参观发现"受训甲壳动物也能监督生产"；因经济学家考夫曼预言加息+美联储主席滑倒受伤引发大盘跌 15%，林奇以 $7.50 买入（比董事便宜 $2.50）。用于演示 13 条准则如何叠加。
  bound_to: ["13条选股准则（综合运用）", "买入时机（无关宏观的个股低价）"]
  outcome: 虚构例题，无真实结果（原文明确为梦境）。
  tags: [worked-example, fictional, dream-company]
  task_ids: [task-03, task-14]

## 第9章

- id: c54
  title: 家庭购物网络（HSN）——16个月$3→$47→$3.5
  type: case
  example_kind: reported_case
  source_chapter: 第9章9.1 L1874-1919；图9-1
  source_quote: |
    "在16个月内它的股价从3美元涨到47美元，然后又跌回到3.5美元（根据股票分割进行股价调整）……这种追涨而高价买入热门股的投资风险之大跟轮盘赌简直没什么区别。"
  summary: |
    电视购物热门股 HSN：16 个月 $3→$47→$3.5（图9-1 显示 1987 年冲高后 1988 年回落至个位数）。基本面崩坏路径：借债购买电视台广告、电话销售出问题、竞争者出现（"人们最多能戴多少条锆石项链"）。同节合并地毯行业案例：簇绒工艺把地毯从 $28/码 降到 $4/码、分析师宣称繁荣永续、200 家新竞争者涌入全行业亏损——热门行业必死于竞争。
  bound_to: ["避而不买清单（热门行业的热门股）"]
  outcome: $47 买入者承受 $3.5 的结局（原文明确）。
  tags: [reported-case, hsn, hot-stock, carpet]
  task_ids: [task-04]

- id: c55
  title: 汤姆·布朗石油服务——50美元宴会上被嘲笑的卖空者对了
  type: case
  example_kind: firsthand
  source_chapter: 第9章9.1 L1935
  source_quote: |
    "1981年，我出席了在科罗拉多州举行的能源业大会的一次宴会……当时股价高达每股50美元……但是4年后，布朗公司的股票真的从50美元跌到了1美元。"
  summary: |
    1981 年能源业宴会上，汤姆·布朗公司 CEO 当众嘲笑卖空其股票的熟人（"你会输得光着屁股去参加圣诞舞会"）。4 年后股价 $50→$1；公司几乎是个空壳：无用钻井架、可疑油气田、惊人债务。林奇在场亲历，用于说明热门行业最热门股的灾难。
  bound_to: ["避而不买清单（热门行业的热门股）"]
  outcome: $50→$1（原文明确）。
  tags: [firsthand, tom-brown, oil-service]
  task_ids: [task-04]

- id: c56
  title: 施乐 vs 菲利普·莫里斯——热门垄断者与负增长行业的15年赛跑
  type: case
  example_kind: reported_case
  source_chapter: 第9章9.1 L1937-1941
  source_quote: |
    "在过去15年，施乐的股票从160美元下跌到了60美元，同期菲利普·莫里斯公司的股票却从14美元上涨到了90美元……负增长行业不会吸引大批竞争对手的进入。"
  summary: |
    1972 年施乐 $170（"施乐"成了复印代名词）时分析师断言永续增长；佳能、IBM、柯达等 20 家涌入后其多元化失败、股价跌 84%。同期负增长行业（美国香烟消费年降约 2%）的菲利普·莫里斯靠海外扩张+提价+降成本，15 年 $14→$90，靠万宝路等品牌利基挡住竞争。
  bound_to: ["避而不买清单（热门股）", "13条选股准则（利基/零增长行业）", "公司增加收益的5途径"]
  outcome: 施乐 160→60；菲利普·莫里斯 14→90（原文明确）。
  tags: [reported-case, xerox, philip-morris]
  task_ids: [task-04, task-03]

- id: c57
  title: "下一个XX"群——Circuit City 的模仿者跌59%-96%
  type: case
  example_kind: reported_case
  source_chapter: 第9章9.2 L1943-1951
  source_quote: |
    "Circuit City的股票从1984年在纽约股票交易所上市交易至今上涨了4倍……而所有被称为'下一个Circuit City'的公司的股票市值都比最初下跌了59%～96%。"
  summary: |
    被吹捧成"下一个"的公司几乎从不兑现：First Family、Good Guys、Highland Superstores、Crazy Eddie、Fretters（"下一个 Circuit City"）市值跌 59%-96%；儿童世界（"下一个玩具反斗城"）步履维艰；仓库俱乐部（"下一个 Price Club"）日子难过。当一家公司被称作"下一个IBM"时，连 IBM 本身也快成为明日黄花。
  bound_to: ["避而不买清单（'下一个'公司）", "12种危险说法（抓住下一只大牛股）"]
  outcome: 模仿者普跌 59%-96%（原文明确）。
  tags: [reported-case, next-circuit-city]
  task_ids: [task-04, task-10]

- id: c58
  title: 美孚 vs 埃克森——多元恶化与专注+回购的对照
  type: case
  example_kind: reported_case
  source_chapter: 第9章9.3 L1965-1967
  source_quote: |
    "从1980年石油价格上涨至最高点至今，美孚石油公司的股价只上涨了10%，而同一期间埃克森公司的股价却翻了一番。"
  summary: |
    美孚收购 Marcor（零售外行+纸箱业务低价甩卖赔钱）、高价收购高级石油损失数百万；1980 年油价顶点至今股价仅 +10%。埃克森除几次小规模失误外拒绝多元化、坚持主业并用多余现金回购，同期翻番；1988 年美孚新管理层卖掉蒙哥马利沃德。
  bound_to: ["避而不买清单（多元恶化）", "13条选股准则（回购）"]
  outcome: 美孚 +10% vs 埃克森 ×2（原文明确）。
  tags: [reported-case, mobil, exxon, diworseification]
  task_ids: [task-04, task-03]

- id: c59
  title: Melville vs Genesco——多元优化与多元恶化的16年对照（图9-2）
  type: case
  example_kind: reported_case
  source_chapter: 第9章9.3 L1983-2018；图9-2 L1985-2006
  source_quote: |
    "到了1987年，Melville股票上涨了30倍。至于Genesco公司，1974年以后财务状况继续恶化，它的股票再也没能涨回来。"
  summary: |
    两家制鞋商的分岔：Melville 从 Thom McAn 鞋店起家，随凯玛特 1962 年扩张爆发，再依次收购 CVS（1969）、Marshall's（1976）、Kay-Bee 玩具（1981），制鞋厂 22 家减至 1 家，每次收购前先把上一次经营成功——1987 年涨 30 倍。Genesco 1956-1973 年 17 年 150 次收购（Bonwit Teller、Tiffany 等），账面变大基本面恶化，最终破产，图9-2 中 16 年后 Melville 约为起点 3.5-4 倍、Genesco 跌约 85%。附：Tisches 家族 Loew's→Lorillard→CNA→CBS 股份是"收购成功"的对照。
  bound_to: ["避而不买清单（多元恶化）", "协同效应辨析"]
  outcome: Melville 30 倍；Genesco 破产未翻身（原文明确）。
  tags: [reported-case, melville, genesco, synergy]
  task_ids: [task-04]

- id: c60
  title: 小声耳语的股票：Bioresponse亲历与失败清单
  type: case
  example_kind: firsthand
  source_chapter: 第9章9.4 L2020-2034
  source_quote: |
    "1983年2月在这家公司增发新股时我以每股9.25美元的价格购买了它的股票，它最高曾上涨到16美元，但现在这家公司已经坠入深渊、无可救药，幸运的是我及早卖出只赔了一点儿钱。"
  summary: |
    林奇亲历 Bioresponse（从牛提取单克隆抗体）：参观旧金山破旧街区顶楼总部（省钱好信号），1983 年 2 月以 $9.25 买入增发新股，最高 $16，最终"坠入深渊"，及早卖出只赔一点。KMS 工业 1980-86 年年年更换神奇业务，$40→$2.5（8 缩 1 才免于仙股）；Smith Labs $25→$1。林奇自列耳语失败清单：神奇世界、Pizza Time Theater、国家卫生保健 $14→$0.50、太阳世界航空 $8→$0.50、美国外科中心、遥控电视、Priam 等——"我所购买的每一只这种小声耳语的股票都让我赔了不少钱"。
  bound_to: ["避而不买清单（小声耳语的股票）"]
  outcome: Bioresponse 小亏离场；清单公司多数归零级下跌（原文明确）。
  tags: [firsthand, whisper-stocks, bioresponse, kms]
  task_ids: [task-04]

- id: c61
  title: IPO两面：基因技术与苹果上市首日 vs 联邦快递的25倍
  type: case
  example_kind: firsthand
  source_chapter: 第9章9.4 L2040-2044
  source_quote: |
    "在苹果电脑公司的股票上我赚得更多，因为那次我想买多少就买多少，在它上市第一天我就把全部股票卖掉得到了20%的高回报……我买的第一只首次发行新股联邦快递后来上涨了25倍。"
  summary: |
    1980-10-04 基因技术 $35 发行、当天最高 $89、收 $71.25，麦哲伦只分到一小部分；苹果 IPO 因马萨诸塞州认定投机性太强（限机构购买），林奇想买多少买多少，首日卖出赚 20%——后来苹果业务崩溃成困境反转他又买回（见 c_ 苹果条目）。统计口径：IPO 新股 4 只中 3 只长期令人失望；分拆类新股（玩具反斗城、租车代理、Safety-Kleen）才让他赚钱。他个人的第一只 IPO 联邦快递后来涨 25 倍。
  bound_to: ["避而不买清单（IPO 投机心理）", "分拆上市的投资机会"]
  outcome: 苹果首日 +20%；联邦快递 25 倍（原文明确）。
  tags: [firsthand, ipo, genentech, apple, fedex]
  task_ids: [task-04, task-03]

- id: c62
  title: 过于依赖大客户的供应商：SCI Systems与Tandon
  type: case
  example_kind: reported_case
  source_chapter: 第9章9.5 L2046-2050
  source_quote: |
    "如果一家公司把25%～50%的商品都卖给了同一个客户，这表明该公司的经营处于十分不稳定的状态之中……像Tandon公司等磁盘驱动器公司就是因为过度依赖少数几家大客户总是处在合同取消大灾难的边缘。"
  summary: |
    SCI Systems（勿与殡葬 SCI 混淆）管理良好但是 IBM 主要零部件供应商——IBM 随时可能自制或不再需要；Tandon 等磁盘驱动器公司长期处在合同取消灾难边缘。大客户还能逼迫降价压缩利润。规则：25%-50% 销售额依赖单一客户即高危。
  bound_to: ["避而不买清单（依赖大客户）"]
  outcome: 未说明（规则性案例）。
  tags: [reported-case, sci-systems, tandon, customer-concentration]
  task_ids: [task-04]

## 第10章

- id: c63
  title: Sensormatic——防窃标签的2→42→5.625（扩张与饱和）
  type: case
  example_kind: reported_case
  source_chapter: 第10章 L2066；第14章 L3200-3206；第15章15.1.5 L3296
  source_quote: |
    "当Sensormatic公司的商店防窃系统从一个商店到另一个商店逐步扩张时……它的股票从每股2美元上涨到了每股40美元，但是它的市场最终还是达到了饱和……它的股价从1983年的每股42.5美元跌至1984年的每股5.625美元。"
  summary: |
    增长三阶段的标尺案例：第二阶段（商店逐店扩张）$2→$40；产品"一次购买"属性决定老客户无法复购，1983 年销售增速放缓时收益"像高台跳水一样直线下跌"，股价 12 个月内 $42→$6（15.1.5 口径）。同节对照：西尔斯遍布都市后无地可扩；The Limited 在 700 家最受欢迎购物中心已开 670 家、又收购 Lerner/Lane Bryant，暗示快增长结束。
  bound_to: ["六类公司分类法（快速增长型三阶段）", "定期重新核查"]
  outcome: $42.5→$5.625（原文明确）。
  tags: [reported-case, sensormatic, saturation]
  task_ids: [task-01, task-09]

- id: c64
  title: 价格线与收益线（图10-1至10-3）：陶氏/雅芳/Limited/万豪/Shoney's
  type: case
  example_kind: reported_case
  source_chapter: 第10章 L2096-2287；图10-1/10-2/10-3
  source_quote: |
    "随着公司收益持续增长，这家公司的股价从1958年的3美元上涨到了1972年的140美元……到了1973年人们对这家公司未来的幻想终于破灭。"
  summary: |
    全书核心图证（16 张图统一规律）：陶氏化学 1971-75 与 1985-88 收益涨股价涨、中间十年收益起伏股价起伏（"破唱片"）；雅芳 1958 年 $3→1972 年 $140 后幻想破灭（《福布斯》提前 10 个月封面警告）；万豪/Shoney's/The Limited 收益线连升、股价随行，Limited 在 1983 与 1987 价格偏离收益时短期大跌。操作提示：价格线低于收益线时买、远高于时卖（"对于雅芳这种操作绝对非常成功"）。
  bound_to: ["收益决定股价（价格线跟随收益线）", "P/E实操口径"]
  outcome: 各图走势如述（原文明确）。
  tags: [reported-case, charts, avon, dow, price-earnings-line]
  task_ids: [task-05]

- id: c65
  title: 凯玛特市盈率演算——P/E是收回投资的年数
  type: case
  example_kind: worked_example
  source_chapter: 第10章10.1 L2291-2325；表10-1
  source_quote: |
    "用35除以3.50就能得出这家公司市盈率为10倍……你购买的100股股票1年后应该获得的收益为350美元，而你最初的投资（3500美元）需要10年的收益才能完全收回。"
  summary: |
    以《华尔街日报》1988-9-13 凯玛特行情为例（股价 $35、每股收益 $3.50）：P/E=10 倍，即 10 年收回投资；2 倍 P/E 两年收回、40 倍要等 40 年。类型基准：公用事业 7-9 倍 < 稳定增长 10-14 倍 < 快速增长 14-20 倍；不能拿陶氏的"低"P/E 与沃尔玛相比。
  bound_to: ["P/E实操口径（计算与分类型基准）"]
  outcome: 演算结果如上（原文明确）。
  tags: [worked-example, pe, kmart]
  task_ids: [task-05]

- id: c66
  title: 麦当劳1972年——50倍P/E的伟大公司仍会腰斩
  type: case
  example_kind: reported_case
  source_chapter: 第10章10.2 L2341
  source_quote: |
    "1972年尽管麦当劳本身的运营还像过去那样优秀……但是它的股价却被投资者哄抬到每股75美元，市盈率高达50倍……导致它的股价从75美元大跌回到了25美元，它的市盈率也相应又回到……13倍。"
  summary: |
    "绝不买超高P/E"红线的头号例证：1972 年麦当劳运营依旧优秀，但 $75 对应 50 倍 P/E，收益增长无法支撑预期，跌至 $25（P/E 回落 13 倍）——大跌非公司之错，而是买价之错。
  bound_to: ["P/E实操口径（绝不买超高P/E）"]
  outcome: $75→$25（原文明确）。
  tags: [reported-case, mcdonald, high-pe]
  task_ids: [task-05]

- id: c67
  title: EDS——500倍市盈率与"盈利增20倍仍不赚钱"
  type: case
  example_kind: reported_case
  source_chapter: 第10章10.2 L2343-2349；第16章16.2 L3464
  source_quote: |
    "这家公司的市盈率竟然高达500倍！……写这篇报告的分析师竟然认为这个市盈率还是比较保守的，因为EDS公司股票市盈率应该能够达到1000倍……1974年，EDS的股价从40美元暴跌到了3美元。"
  summary: |
    60 年代后期 Ross Perot 的 EDS：券商报告 P/E 500 倍、分析师称保守（应可达 1000 倍）。其后公司业绩连年优秀、15 年间盈利增长约 20 倍，但 1974 年股价仍从 $40 暴跌至 $3；1984 年被通用汽车以 $44 整体收购——不过相当于 10 年前的价格。"买价过高时，公司巨大成功也与你无关"的极端例证。
  bound_to: ["P/E实操口径（绝不买超高P/E）", "组合构建与持有纪律（买价决定回报）"]
  outcome: 1974 年 $40→$3；1984 年 GM $44 收购（原文明确）。
  tags: [reported-case, eds, extreme-pe]
  task_ids: [task-05, task-11]

- id: c68
  title: 宝丽来——50倍P/E与SX-70幻觉（18个月跌89%）
  type: case
  example_kind: reported_case
  source_chapter: 第10章10.2 L2353-2355；第18章18.1 L3750-3754
  source_quote: |
    "宝丽来公司也是一家业绩表现非常稳定的公司，拥有32年的辉煌历史，但后来股价却在短短18个月里就大跌了89%。1973年这家公司的股价为每股143美元，但是到了1974年却下跌到只有每股14.125美元……1973年宝丽来公司在最高价位时市盈率高达50倍。"
  summary: |
    估值角度（10.2）：1973 年高点 $143（18.1 节作 $143.5）P/E 50 倍，投资者预期 SX-70 畅销；即便成功也须向每个美国家庭卖 4 台才能支撑。实际定价过高、使用有问题，18 个月跌 89%：$143.5→$14.125（1974），1978 年反弹 $60、1981 年又只剩 $19。18.1 节用它逐级反驳"跌这么多了不可能再跌"：$100→$90→$80→$75→$50 一路有人喊底。
  bound_to: ["P/E实操口径（绝不买超高P/E）", "12种危险说法（不可能再跌了）"]
  outcome: 143.5→14.125 美元，18 个月 -89%（原文明确）。
  tags: [reported-case, polaroid, sx-70, high-pe]
  task_ids: [task-05, task-10]

- id: c69
  title: 股市整体P/E——1982-87年从8倍升到16倍的警告
  type: case
  example_kind: worked_example
  source_chapter: 第10章10.3 L2357-2365
  source_quote: |
    "在最近这次持续5年的大牛市中（1982～1987年）……股票市场整体的市盈率逐渐从8倍左右上升到了16倍……这是一个投资者本来应该注意到的大多数股票已经过于高估的警告信号。"
  summary: |
    整体市场风向标：1982-87 牛市整体 P/E 从约 8 倍升至 16 倍（同等收益支付价格翻倍）；1971 年市场平均 P/E 曾达 20 倍高点，随后 1973-74 出现 30 年代以来最剧烈暴跌使 P/E 回归。个人不预测市场，但可用整体 P/E 识别"大多数股票同时高估"的环境。
  bound_to: ["P/E实操口径（整体市场P/E风向标）"]
  outcome: 1987 年 10 月暴跌验证警告（原文明确）。
  tags: [worked-example, market-pe, 1987]
  task_ids: [task-05, task-14]

## 第11章

- id: c70
  title: 两分钟独白六类模板（含通用磨坊与可口可乐的具体口径）
  type: case
  example_kind: worked_example
  source_chapter: 第11章 L2389-2409
  source_quote: |
    "通用磨坊食品公司……已经把主营业务数量从原来的11个缩减到只有2个……该公司下属的海鲜产品子公司高顿公司在海鲜产品市场的占有率已从7%增长到了25%。"
  summary: |
    下单前的类型化独白示范，各配一段可直接照抄的"故事脚本"：缓慢增长看股息记录；周期看存货/产能（通用汽车 18 个月关 5 家厂、劳动成本降 20%）；隐蔽资产算净值（股价 $8＝录像带 $4+房地产 $7，倒赚 $3）；困境反转看重整成效（通用磨坊 11→2 个主业、卖掉 Eddie Bauer/Talbot/肯纳等，Gorton 市占率 7%→25%，回购数百万股）；稳定增长看 P/E 与催化（可口可乐 P/E 处历史区间低位、出售哥伦比亚影业 50% 股份、健怡可乐畅销、日本销量 +36%/西班牙 +26%）；快速增长看复制扩张（La Quinta 新开店 +20%/季）。
  bound_to: ["两分钟独白与类型化故事"]
  outcome: 模板本身；两个完整正反案例另见 c71/c72。
  tags: [worked-example, two-minute-monologue]
  task_ids: [task-07]

- id: c71
  title: La Quinta成功研究——竞争对手的称赞开始（15倍）
  type: case
  example_kind: firsthand
  source_chapter: 第11章11.1 L2413-2451；导论0.2 L75
  source_quote: |
    "'La Quinta汽车旅馆！'联合旅馆的副总裁十分激动地回答道，'这家旅馆经营得棒极了。在休斯敦和达拉斯地区它彻底把我们打垮了。'……后来我为麦哲伦基金尽可能多地大量买入了La Quinta公司的股票，10年间我在这家公司股票上的投资上涨了11倍。"
  summary: |
    完整调研链：①问联合旅馆（假日酒店最大特许商）副总裁"最成功的竞争对手是谁"——95% 的高管只会诋毁，能赢得称赞者必是牛股；②总部毕哥勒来访讲解商业模式：同等品质房价低 30%（去掉餐厅会议室、120 间小体量、退休夫妇驻店管理、保险公司融资而非银行贷款、选址商务区）；③细节知识（房费≈每间客房造价的 1‰）；④验证：1978 年仅 3 家券商追踪、机构持股 <20%、年增 50% 而 P/E 仅 10 倍；⑤实地：住 3 家不同分店跳床、趟水、拧毛巾；⑥差点因一位创始人半价卖出而放弃——提醒自己"因内部人士卖出而否定股票是愚蠢理由"。结果：书中两处口径——"上涨15倍的大牛股"（L2423）、"10年间上涨11倍"（L2451）；导论演算 1973 年 $371.38→10 年 $4363.08。后因产油州不景气低迷，成为隐蔽资产+困境反转候选。
  bound_to: ["两分钟独白与类型化故事", "信息获取程序（电话/拜访/实地）", "13条选股准则（利基/无机构关注）"]
  outcome: 10 年 11 倍（另一处口径 15 倍）；后陷入低迷（原文明确）。
  tags: [firsthand, la-quinta, competitor-praise]
  task_ids: [task-07, task-08]

- id: c72
  title: Bildner's失败教训——忘了问"经营模式能复制吗"（$13→$0.125）
  type: case
  example_kind: firsthand
  source_chapter: 导论0.6 L165；第11章11.2 L2453-2475
  source_quote: |
    "在没有对这家公司进一步深入研究的情况下，1986年9月我以每股13美元的首次公开发行股票价格购买了Bildner's的股票……它的股价最后下跌到了仅仅只有0.125美元……我分批逐步卖掉了这家公司的股票，亏损程度在50%～95%之间。"
  summary: |
    林奇有身边优势（办公室马路对面的分店、多年午餐亲测"波士顿最好的三明治"）、看了招股书（无银行债、租赁开店两个优点），却没问最关键的问题：本地成功模式能否异地复制？波士顿百货店内两店失败、曼哈顿三家店被熟食店挤垮、再扩张亚特兰大，资本支出超募资、财务入不敷出。股价 $13（1986-9 IPO）→$0.125；林奇分批卖出亏 50%-95%。教训：等复制被证明再买；"下一个Taco Bell"式自我陶醉是失败宣言。
  bound_to: ["两分钟独白与类型化故事（遗漏关键问题）", "快速增长型公司的复制验证", "避而不买清单（未证明的扩张）"]
  outcome: $13→$0.125，作者亏损 50%-95%（原文明确）。
  tags: [firsthand, mistake, bildners]
  task_ids: [task-07, task-04]

## 第12章

- id: c73
  title: 经纪人问询对话模板——从"推荐Zayre"到系统提问La Quinta
  type: case
  example_kind: worked_example
  source_chapter: 第12章12.1 L2497-2535
  source_quote: |
    "经纪人：'我们推荐Zayre公司的股票……' 你：'太好了，那我就买入这只股票。'……如果你用几个前面我已经列出的问题来提示和引导经纪人进行系统分析的话，那么上面的这番对话可能会变成以下这种情形……"
  summary: |
    一组对照对话：被动接受推荐（Zayre）vs 用类型/增长率/当前与历史 P/E/机构持股/内部人士买入/分析师追踪时长等一连串问题把经纪人变成研究助理（La Quinta 版）。用于演示"全方位服务券商"的信息索取方法。
  bound_to: ["信息获取程序（经纪人）"]
  outcome: 方法演示，无投资结果。
  tags: [worked-example, broker-dialogue]
  task_ids: [task-08]

- id: c74
  title: 给公司打电话——宝洁、雷诺兹与Sterling的口径差异
  type: case
  example_kind: worked_example
  source_chapter: 第12章12.2-12.3 L2537-2583
  source_quote: |
    "直接向公司询问'你们公司未来收益是多少'就像一个陌生人问你的年薪是多少一样很不礼貌，就得问得委婉巧妙：'华尔街对贵公司明年的收益预测是多少呢？'……1987年，Sterling药品公司的投资者关系部门可能会告诉你最近有关阿司匹林的大量报道是否刺激了公司的销售增长。"
  summary: |
    打电话的实操规范：先亮研究（"年报显示去年减债 5 亿，后续计划？"）；要事实数据不要形容词——纺织业 IR 一律悲观（"一般"实为优秀）、软件业 IR 一律乐观，"只管事实和数据"；宝洁（82 种产品、107 国销售）能预测收益、雷诺兹金属只能反问铝价。林奇统计：约每 10 个电话有 1 个获得非同一般的信息；打 1000 个电话约有 100 个吃惊信息。技巧：自称持有 2 万股（券商名义持股无法拆穿）改善态度。
  bound_to: ["信息获取程序（给公司打电话）"]
  outcome: 方法与统计口径（原文明确）。
  tags: [worked-example, ir-call, sterling]
  task_ids: [task-08]

- id: c75
  title: 拜访总部信号群——Taco Bell的保龄球场与瓶盖瓶塞的油地毡（30年280倍）
  type: case
  example_kind: firsthand
  source_chapter: 第12章12.4 L2587-2597
  source_quote: |
    "当我看到Taco Bell公司的总部办公室竟然挤在一个保龄球场的后面时，我马上对这家公司就有了一种很好的印象……过去30年里股价上涨了280倍，丰厚的收益和简朴的公司总部真是一个产生大牛股的绝佳组合。"
  summary: |
    拜访总部的信号学：Taco Bell 总部挤在保龄球场后面、高管在地堡式小办公室——好信号；Meridian 银行 22 年收益连增且"记不清上次来的分析师"——好信号（首问："上次分析师来访是什么时候？"）；瓶盖瓶塞总裁办公室能看罐头生产线、褪色油地毡、比军队还破的家具——30 年涨 280 倍；Uniroyal 总部像富丽堂皇的预科学校——坏信号。"办公室越豪华，越该为收益忧心。"
  bound_to: ["信息获取程序（拜访总部）"]
  outcome: 瓶盖瓶塞 30 年 280 倍（原文明确）。
  tags: [firsthand, hq-visit, taco-bell, crown-cork]
  task_ids: [task-08]

- id: c76
  title: Tandon与Televideo——IR职员的财富就是估值警报
  type: case
  example_kind: firsthand
  source_chapter: 第12章12.5 L2603-2609
  source_quote: |
    "根据他所持有的公司股票期权……他的个人财富竟然已经达到了2000万美元……后来Tandon的股票从每股35.25美元跌到了每股1.375美元……后来这只股票从1983年的40.5美元跌到了1987年的1美元。"
  summary: |
    两次亲历的"内部人财富信号"：Tandon 的 IR 普通职员期权财富已达 2000 万美元（股价已涨 8 倍、P/E 高得头晕；若再翻倍他将 4000 万）——林奇拒绝投资，后来 $35.25→$1.375；Televideo 创始人持 1 亿美元市值股票（高 P/E+竞争激烈的计算机辅助设备业）——林奇没买，$40.5（1983）→$1（1987）。规则："无法想象普通员工因持股那么富有时，不买很可能正确。"
  bound_to: ["信息获取程序（与IR个人接触）", "P/E实操口径"]
  outcome: 两股分别跌 96% 与 97.5%（原文明确）。
  tags: [firsthand, tandon, televideo, insider-wealth]
  task_ids: [task-08, task-05]

- id: c77
  title: 实地调查群——玩具反斗城、Pic 'N' Save与Pep Boys的店里观察
  type: case
  example_kind: firsthand
  source_chapter: 第12章12.6 L2611-2633
  source_quote: |
    "自从我的妻子卡罗琳在超级市场购买丝袜发现L'eggs公司以及我吃玉米馅饼快餐发现Taco Bell公司以后，我就一直相信逛街和吃东西是一个进行基本面分析的投资成功之道……当我购买Pic 'N' Save公司的股票之前，我顺便到这家公司在加利福尼亚的一家分店看了看……古龙香水每瓶只卖79美分……"
  summary: |
    实地调查案例集：听德罗斯说玩具反斗城后亲自到分店问顾客（"几乎所有人都说一定再来"）；Pic 'N' Save 分店里 79 美分古龙香水与抢购 Lassie 狗粮（康宝退出后低价接盘转卖）的人群；加州 Pep Boys 新店推销员热情到差点让林奇带走 4 只轮胎。反面：孩子们一直穿 OshKosh B'Gosh 却没买其股票；因妻子朋友抱怨锐步磨脚就放弃，错过 5 倍——"邻居对一双鞋评价差"不构成基本面。停车场访谈：克莱斯勒 Minivan 与福特 Taurus 车主 100% 肯定推荐。
  bound_to: ["信息获取程序（实地调查）", "业余投资者的身边信息优势"]
  outcome: 各持仓结果未逐项说明；锐步 5 倍被错过（原文明确）。
  tags: [firsthand, field-research, pic-n-save]
  task_ids: [task-08, task-12]

- id: c78
  title: 苹果电脑的困境反转——从IPO首日卖出到买入100万股
  type: case
  example_kind: firsthand
  source_chapter: 第9章 L2040；第12章12.6 L2623；第15章15.1.6 L3302, L3318
  source_quote: |
    "随着苹果电脑公司陷入崩溃，股价从60美元跌到15美元……当妻子告诉我说她和孩子们在家里需要再买一台新的苹果电脑，并且富达公司的电脑系统管理人员告诉我说正要给办公室买60台新的……我购买了100万股苹果公司的股票，我从来没有因此而后悔过。"
  summary: |
    林奇对苹果的两段操作：①1980 年 IPO 因马萨诸塞州限制"想买多少买多少"，首日全卖赚 20%；②股价 $60→$15、Lisa 商用机惨败后，两个身边信号（家里要添第二台苹果、富达系统管理员为公司购 60 台 Macintosh）确认家用畅销+进军商用，买入 100 万股且"从未后悔"。核查要点（15.1.6）：账上 2 亿美元现金、零债务，肯定不会破产。
  bound_to: ["六类公司分类法（困境反转）", "业余投资者的身边信息优势", "13项财务指标（现金头寸）"]
  outcome: 买入 100 万股且不后悔；后续涨幅未给具体数字（原文明确"从未后悔"）。
  tags: [firsthand, apple, turnaround, 1m-shares]
  task_ids: [task-01, task-12, task-06]

- id: c79
  title: 克莱斯勒实地拜访——艾柯卡、空车位与Minivan（占全美销量3%）
  type: case
  example_kind: firsthand
  source_chapter: 第12章12.6 L2625-2631
  source_quote: |
    "和克莱斯勒公司总裁李·艾柯卡交谈后，我对克莱斯勒公司能够成功地东山再起的信心大增……在公司总部办公楼外面，我注意到高级管理人员的停车位有一半是空的……直到在我参观展示中心钻进钻出新开发的Lasers和New Yorkers轿车以及LeBaron敞篷车时，才真正让我的投资热情像火山一样爆发。"
  summary: |
    实地信号集：与艾柯卡面谈确认削减成本、改善产品线；高管停车位一半空置（成本纪律信号）；试坐新车型点燃热情。Minivan 与 L'eggs 并列 80 年代两大畅销产品，已占美国轿车和货车总销量 3%，加长车身+更强引擎正是用户想要的改进。停车场访谈 Minivan/Taurus 车主 100% 推荐。
  bound_to: ["信息获取程序（实地调查）", "六类公司分类法（困境反转的确认）"]
  outcome: 支撑 c29 的克莱斯勒 15 倍持仓（原文明确）。
  tags: [firsthand, chrysler, iacocca, minivan]
  task_ids: [task-08, task-01]

- id: c80
  title: 福特年报三分钟——表12-1/12-2的数据链演算
  type: case
  example_kind: worked_example
  source_chapter: 第12章12.7 L2639-2776；表12-1 L2645-2704；表12-2 L2717-2766
  source_quote: |
    "第一行是流动资产，我注意到其中包括56.72亿美元的现金及现金等价物以及44.24亿美元的有价证券……从101亿美元的现金头寸中减去17.5亿美元的长期债务，等于83.5亿美元，这就是福特公司的净现金头寸。"
  summary: |
    读年报方法的标准演示（1987 年福特年报）：跳过光纸文字部分直翻第 27 页合并资产负债表——现金 56.729 亿+有价证券 44.241 亿≈101 亿现金头寸，减长期债务 17.519 亿=净现金 83.5 亿美元；现金逐年增、债务逐年减=业务兴旺双信号。第 38 页十年数据概要（表12-2）：流通股 5.11 亿且两年连降=回购信号；83.5 亿÷5.11 亿股=每股净现金 16.30 美元（"纸张越便宜，信息越宝贵"）。
  bound_to: ["信息获取程序（阅读年报）", "13项财务指标（现金头寸）"]
  outcome: 演算结果即交付物；该数字在 13.3 节支撑继续持有决策（见 c82）。
  tags: [worked-example, ford, annual-report, table-12-1]
  task_ids: [task-08, task-06]

- id: c81
  title: 波音——$40股价含$27现金，"实际买价$15"
  type: case
  example_kind: firsthand
  source_chapter: 第13章13.3 L2842
  source_quote: |
    "1987年初它的股价最低只有40美元略多一些，但是公司每股现金为27美元，因此实际上你的买入价格只有每股15美元左右。1988年初我少量买入了这家公司的股票，后来我又大量买入，直到这只股票成为我的重仓股。"
  summary: |
    现金头寸准则应用：1987 年初波音股价 40 美元出头、每股现金 27 美元→实际买入约 15 美元；叠加大量未完成商用飞机订单，1988 年初少量买入后加至重仓。对照百时美：16 亿现金-2 亿长期债=14 亿净现金，但除以 2.8 亿股仅每股 5 美元，对 40+ 美元股价影响甚微（股价若跌到 15 美元则影响巨大）——每股净现金必须相对股价才有意义。
  bound_to: ["13项财务指标（现金头寸）"]
  outcome: 波音成为重仓股；具体涨幅未说明。
  tags: [firsthand, boeing, net-cash]
  task_ids: [task-06]

- id: c82
  title: 福特500万股与16.30美元净现金——"38美元其实是21.70美元"
  type: case
  example_kind: firsthand
  source_chapter: 第13章13.3 L2826-2840；第15章15.1.1 L3254
  source_quote: |
    "这16.30美元的折扣改变了一切，它意味着我买入股票的真正价格并不是当前的市价每股38美元，而是每股21.70美元……用21.70美元的实际股价计算出来的市盈率是3.1倍……结果后来福特公司股票又上涨了40%还要多。"
  summary: |
    完整亲历演算：福特 1982 年 $4→1988 年初 $38（林奇买了 500 万股，华尔街齐喊周期见顶）。年报显示每股净现金 16.30 美元→实际买价 38-16.3=21.70 美元；汽车业务预期每股收益 7 美元→38 美元口径 P/E 5.4 倍、21.70 美元口径仅 3.1 倍。再拆：金融服务集团每股收益 1.66 美元×10 倍 P/E=16.60 美元，故汽车业务成本仅 38-16.30-16.60=5.10 美元对应 7 美元收益。决定不卖，后又涨 40% 多；15.1.1 总结"每股净现金是股价的下限"。
  bound_to: ["13项财务指标（现金头寸/隐蔽资产）", "六类公司分类法（周期型）"]
  outcome: 1982 年 4 美元→38 美元后再涨 40%+（原文明确）。
  tags: [firsthand, ford, net-cash, 16.30]
  task_ids: [task-06, task-01]

- id: c83
  title: GCA vs 应用材料——负债结构决定同行业生死
  type: case
  example_kind: reported_case
  source_chapter: 第13章13.4 L2864-2876
  source_quote: |
    "1985年下半年，GCA的股票从每股20美元下跌到了每股12美元，而应用材料公司的股票表现更差，它从每股16美元下跌到了每股8美元……GCA宣告破产被其他公司以每股10美分的价格收购，而应用材料公司的股票却上涨了4倍以上，债务负担的不同决定了两家公司命运的不同。"
  summary: |
    同为芯片设备商、同在 1985 下半年腰斩：GCA 负债 1.14 亿美元且几乎全是"对方通知即还"的银行短期贷款、现金仅 300 万、存货 7300 万（明年可能只值 2000 万）；应用材料负债仅 1700 万、现金 3600 万。行业复苏后应用材料 $8→$36（4 倍以上），GCA 破产、以每股 10 美分被收购。准则：困境公司先看负债数量与结构——银行短期债最致命，长期债券给公司喘息时间。
  bound_to: ["13项财务指标（负债因素）", "六类公司分类法（困境反转的存活判据）"]
  outcome: 应用材料 4 倍以上；GCA 破产 $0.10（原文明确）。
  tags: [reported-case, gca, applied-materials, debt]
  task_ids: [task-06, task-01]

- id: c84
  title: Micron Technology——可转债置换短债的救援（富达参与，$4→$24）
  type: case
  example_kind: firsthand
  source_chapter: 第13章13.4 L2884-2888
  source_quote: |
    "Micron公司最后的希望就是发行大量可转换债券……富达基金公司购买了Micron公司发行的大部分可转换债券。当电脑存储器芯片行业再次繁荣起来……这只股票的股价从每股4美元上涨到了每股24美元，富达基金公司也因此赚到了一大笔钱。"
  summary: |
    日本厂商倾销 DRAM 令 Micron 濒临破产（$40→$4），但公司赢了反倾销诉讼、且几乎全美存储器厂商退出后仅存；大量短期银行贷款是致命威胁，解法是发多年后才到期的可转债置换短债。富达买了大部分可转债，行业复苏后 $4→$24（6 倍），"赚了一大笔"。长期负债给困境公司时间解决问题。
  bound_to: ["13项财务指标（负债种类）", "六类公司分类法（困境反转）"]
  outcome: $4→$24；富达获厚利（原文明确）。
  tags: [firsthand, micron, convertible, debt-structure]
  task_ids: [task-06, task-01]

- id: c85
  title: 股息记录群——Fleet-Norstar、Kellogg、Southmark与福特1982
  type: case
  example_kind: reported_case
  source_chapter: 第13章13.5-13.6 L2896-2967
  source_quote: |
    "1987年股票市场崩溃时，派发高股息的股票的表现要比不派发股息的股票好得多，其跌幅还不到整个股市跌幅的一半……Kellogg公司和Ralston Purina公司在过去的三次战争和八次经济衰退中都没有降低过股息。"
  summary: |
    股息三案例：①Fleet-Norstar（前身为工业国民银行）自 1791 年从未中断派息——长期记录是缓慢增长股首选；②Kellogg/Ralston Purina 三次战争八次衰退未降股息；③反例 Southmark 债务沉重，地产受挫后 $11→$3 并暂停派息。周期股口径：福特 1982 年停息、股价跌破 $4（25 年最低），但只要现金未尽，股息可补回。1987 年崩盘高息股跌幅不到大盘一半。
  bound_to: ["13项财务指标（股息）", "六类公司分类法（缓慢增长型）"]
  outcome: 各例结局如数字（原文明确）。
  tags: [reported-case, dividend, kellogg, southmark]
  task_ids: [task-06, task-01]

- id: c86
  title: 账面价值陷阱——艾伦伍德钢铁与巴菲特的织布机拍卖
  type: case
  example_kind: reported_case
  source_chapter: 第13章13.7 L2973-2983
  source_quote: |
    "那种几年前他们以每台5000美元的价格购买的织布机，现在拍卖价格只有每台26美元了……结果账面价值为86.6万美元的织布机最后在拍卖中只卖了16.3万美元。"
  summary: |
    两个账面失灵例：①艾伦伍德钢铁 1976 年底账面 3200 万美元（每股 $40），6 个月后仍依《破产法》11 章申请保护——设计不当的新炼钢设施（账面 3000 万）实际无法使用，钢板厂仅以约 500 万卖给 Lukens；②巴菲特关闭新贝德福德纺织厂，账面 86.6 万美元的织布机（每台原购 $5000）拍卖每台 $26、共得 16.3 万美元。规则：产品越接近最终制成品，清算价越难预测。
  bound_to: ["13项财务指标（账面价值陷阱）"]
  outcome: 两公司/资产清算价远低于账面（原文明确）。
  tags: [reported-case, book-value, alan-wood, looms]
  task_ids: [task-06]

- id: c87
  title: Radice——麦哲伦踩中的账面价值陷阱（$10→$0.75）
  type: case
  example_kind: firsthand
  source_chapter: 第13章13.7 L2985-2987；第5章 L714
  source_quote: |
    "每股账面资产价值为50美元，而股价只有每股10美元……Radice公司股价跌到了75美分……我本来应该知道这种情况的，我管理的麦哲伦基金是这家公司的大股东。"
  summary: |
    佛州土地开发公司，账面每股 $50 vs 股价 $10 看似极便宜；但房地产会计允许把未售项目的借款利息计入资产——项目卖不掉时银行收贷、左边资产蒸发右边负债仍在，真实价值为每股负 7 美元，股价跌至 $0.75 且永无反弹。麦哲伦是其大股东（第 5 章亦引用：预测对佛州地产繁荣而买 Radice 亏 95%）。
  bound_to: ["13项财务指标（账面价值陷阱）", "避而不买清单"]
  outcome: $10→$0.75，麦哲伦亏损（原文明确）。
  tags: [firsthand, radice, book-value-trap]
  task_ids: [task-06, task-04]

- id: c88
  title: Handy & Harman——贵金属存货的隐蔽资产与巴菲特的罕见失手
  type: case
  example_kind: reported_case
  source_chapter: 第13章13.8 L2995-2999；第13章13.10 L3067
  source_quote: |
    "1987年生产贵金属制品的Handy＆Harman公司的账面价值为每股7.83美元……以目前的价格计算（每盎司白银是6.40美元，每盎司黄金是415美元），这些贵金属的价值大约相当于每股19美元。Handy＆Harman公司的股票价格大约是17美元……巴菲特大量持有……已经几年了，但是这只股票却根本没怎么上涨。"
  summary: |
    存货以 30 年前成本入账：账面每股 $7.83，按现价金银价值每股约 $19，而股价仅 $17——低于单项资产。巴菲特持有数年未涨（其罕见业绩不佳的持股），正在减持；若金银大涨该股会大涨。同节附 LIFO/FIFO 演算：30 年前 $40/盎司买入、昨日 $400 买入、今日 $450 卖出——后进先出利润 $50、先进先出利润 $410，计价方法直接决定报告收益。
  bound_to: ["13项财务指标（隐蔽资产/存货计价）"]
  outcome: 巴菲特持有数年未涨、正减持（原文明确）。
  tags: [reported-case, handy-harman, lifo-fifo]
  task_ids: [task-06]

- id: c89
  title: CSX铁路通行权与波士顿第五频道——账面近零的资产卖出天价
  type: case
  example_kind: reported_case
  source_chapter: 第13章13.8 L3003-3011
  source_quote: |
    "1988年，CSX向佛罗里达州出售了80英里的铁路通行权，这块土地的账面价值几乎为零，但是这条铁路却价值1100万美元……并且这笔交易还给它带来了2.64亿美元的税后收入……这家电视台的全部家当最初的账面价值只有250万美元……售价约为4.5亿美元……被低估了300多倍。"
  summary: |
    两例低估型隐蔽资产：①CSX 以近乎零账面的铁路通行权交易获利（保留非高峰使用权，收入不受影响，税后进账 2.64 亿美元）；②波士顿第五频道电视台最初全部投入约 250 万美元（申请文件 2.5 万+发射塔约 100 万+演播室 100-200 万），出售价 4.5 亿美元——账面仅为市价的 1/300。铁路公司（伯林顿北方、联合太平洋、圣达菲南太平洋——加州最大私地所有者 130 万英亩）土地账面近零。
  bound_to: ["13项财务指标（隐蔽资产）"]
  outcome: CSX 税后 2.64 亿；第五频道 4.5 亿成交（原文明确）。
  tags: [reported-case, csx, channel-5, hidden-asset]
  task_ids: [task-06]

- id: c90
  title: 商誉摊销的黑箱——可口可乐灌装商与孟山都NutraSweet
  type: case
  example_kind: worked_example
  source_chapter: 第13章13.8 L3013-3021
  source_quote: |
    "1987年这家公司报告的每股收益为63美分，而实际上它另外还有50美分的每股收益，只不过被用来摊销商誉了……收购后经过4年的摊销，纽特牌阿斯巴甜在孟山都公司的资产负债表上记录的账面价值将会是零。"
  summary: |
    商誉摊销制造"隐性好公司"：可口可乐灌装商控股账面商誉 27 亿美元、40 年强制摊销，1987 年报告每股收益 63 美分+被摊销吞掉的 50 美分；孟山都收购 Seral 取得纽特阿斯巴甜专利，4 年摊销后账面归零，若真实每股收益 10 美元报告只有 8 美元、摊销结束即 +2 美元。研发费用冲销同理——"了解这种情况就拥有独特优势"。
  bound_to: ["13项财务指标（隐蔽资产/摊销）"]
  outcome: 演算性结论，未给后续价格（未说明）。
  tags: [worked-example, goodwill, nutrasweet, coke-enterprises]
  task_ids: [task-06]

- id: c91
  title: UAL——子公司价值之和超过总市值（富达赚一倍）
  type: case
  example_kind: firsthand
  source_chapter: 第13章13.8 L3023
  source_quote: |
    "希尔顿国际公司价值10亿美元，赫兹租车公司……价值13亿美元，威斯汀大酒店价值14亿美元，旅行预订系统也价值10亿美元以上……富达基金公司大量买入了UAL公司的股票，这只股票让我们赚了一倍。"
  summary: |
    富达航空业分析师布拉德·刘易斯发掘的隐蔽资产型：UAL 名下希尔顿国际（10 亿）、赫兹（13 亿）、威斯汀（14 亿）、旅行预订系统（10 亿+）——扣除负债税收后净资产超过总市值，等于免费获得世界最大航空公司之一。富达大量买入赚一倍。
  bound_to: ["13项财务指标（隐蔽资产：控股子公司）"]
  outcome: 富达赚一倍（原文明确）。
  tags: [firsthand, ual, sum-of-parts]
  task_ids: [task-06]

- id: c92
  title: 埃索特与Del Haize——买外国母公司便宜获得美国上市资产
  type: case
  example_kind: firsthand
  source_chapter: 第13章13.8 L3029-3037
  source_quote: |
    "两年后，当在美国上市的埃索特商业系统公司的股价只稍微上涨了一点点时，它的瑞典母公司的股价却上涨了两倍……当食品狮王公司的股票上涨了50%时，我为麦哲伦基金购买的Del Haize公司的股票已经从30美元上涨到了120美元。"
  summary: |
    两条"经由母公司打折买资产"的亲历路径：①富达海外基金乔治·诺贝尔提示后，林奇赴瑞典调研发现埃索特美国子公司便宜、瑞典母公司更便宜（附送其他业务与房地产，沃尔沃等巨头仅 1 位分析师追踪、且没有电脑）——两年后母公司涨两倍而美国子公司仅微涨；②比利时 Del Haize 持食品狮王 25% 股份，该权益价值已超 Del Haize 自身市值——食品狮王涨 50% 期间，麦哲伦持有的 Del Haize $30→$120。附算例：太平洋电信 $29 含 $9 移动牌照、Contel $35 含 $15。
  bound_to: ["13项财务指标（隐蔽资产：持股/牌照）", "信息获取程序（实地调查）"]
  outcome: 瑞典母公司两年两倍；Del Haize 30→120（原文明确）。
  tags: [firsthand, esselte, del-haize, foreign-parent]
  task_ids: [task-06, task-08]

- id: c93
  title: 海岸公司——自由现金流估值（股价$20，每股自由现金流$7）
  type: case
  example_kind: worked_example
  source_chapter: 第13章13.9 L3045-3061
  source_quote: |
    "海岸公司借款24.50亿美元收购了……美国自然资源公司……每股现金流量仍然达到了10美元～11美元，扣除资本支出后每股剩下的现金流量为每股7美元……他们以每股20美元的价格购买该公司的股票，未来10年内就会得到70美元的回报。"
  summary: |
    自由现金流示范：海岸公司每股收益 $2.50、P/E 8 倍、股价 $20 看似平庸，但管道业务无需维护、折旧后每股现金流 $10-11、扣资本支出后自由现金流 $7——20 美元买 10 年 70 美元现金回报。对照"皮格钢铁公司"假设例（1 亿收入须再投 8000 万更新高炉）说明菲利普·莫里斯式轻资本业务的优势。规则：市价现金流量 10:1 为正常；自由现金流/股价≥10% 为佳。
  bound_to: ["13项财务指标（现金流量）"]
  outcome: 演算结论；后续股价未说明。
  tags: [worked-example, coastal, free-cash-flow]
  task_ids: [task-06]

- id: c94
  title: 铝业公司的停车场——存货堆到员工车位
  type: case
  example_kind: firsthand
  source_chapter: 第13章13.10 L3073-3079
  source_quote: |
    "它积压了那么多没有卖出去的存货，以致不但整个仓库从地面直到天花板都堆得满满的，连仓库外员工的停车位大部分空间也堆得满满的……你就可以提醒自己：'等一下，这家公司也许应该首先控制存货的过快增长。'"
  summary: |
    林奇参观铝业公司的直观存货信号：仓库堆满、连员工停车位都被存货占据。规则：存货增速超销售增速即危险（销售+10%而存货+30%→来年问题更大、最终降价减利）；好转的第一个信号是滞销公司存货逐步减少。耐用品差异：$35000 美洲虎不会降到 $3500，$300 过时紫迷你裙 $3 都卖不掉。
  bound_to: ["13项财务指标（存货）", "六类公司分类法（周期型卖出信号）"]
  outcome: 参观判断，未给后续（未说明）。
  tags: [firsthand, inventory, aluminum]
  task_ids: [task-06, task-02]

- id: c95
  title: 养老金对照——USX盈余12亿 vs 伯利恒赤字15亿
  type: case
  example_kind: worked_example
  source_chapter: 第13章13.11 L3085-3089
  source_quote: |
    "USX公司的养老金计划资产为85亿美元，应付给员工的既定的养老金福利义务为73亿美元……伯利恒钢铁公司的养老金资产为23亿美元，既定的养老金义务为38亿美元……这15亿美元的赤字会让它雪上加霜。"
  summary: |
    困境反转买入前的必查项：公司破产也甩不掉养老金义务（像必须偿付的债券）。USX 资产 85 亿/义务 73 亿（盈余 12 亿，不必担心）；伯利恒钢铁 23 亿/38 亿（赤字 15 亿，财务再恶化则雪上加霜，应调低估值）。数据均披露于年报。
  bound_to: ["13项财务指标（养老金计划）"]
  outcome: 数据对照即结论；伯利恒后续走势未说明。
  tags: [worked-example, pension, usx, bethlehem]
  task_ids: [task-06]

- id: c96
  title: 菲利普·莫里斯——提价的算术与130亿收购卡夫
  type: case
  example_kind: reported_case
  source_chapter: 第13章13.12 L3093-3105
  source_quote: |
    "如果一家烟草公司的成本增加4%，同时销售价格提高6%，那么公司的利润率就会增加2%……利润率是10%……那么利润率增加2%则意味着公司收益将会增长20%……1988年10月30日……以130亿美元的价格收购卡夫公司……但菲利普·莫里斯公司的股价也只下跌了5%。"
  summary: |
    增长率=收益增长率的样板：美国香烟消费年降 2%，PM 靠降成本+提价（成本+4%、售价+6%→利润率+2%→收益+20%）实现 40 年收益连增，每 4 个德国人 1 个抽万宝路、每周 747 整机运日本；禁电视广告反而降成本。乱多元化（米勒、通用食品、七喜）也未大损股东。1988-10-30 宣布 130 亿美元（卡夫收益的 20 倍）收购卡夫，股价仅跌 5%（现金流足以 5 年还清负债）。仍可以 10 倍 P/E（增长率一半）买入。
  bound_to: ["13项财务指标（增长率）", "公司增加收益的5途径（提价）"]
  outcome: 收益连增 40 年；收购公告日仅跌 5%（原文明确）。
  tags: [reported-case, philip-morris, pricing-power, kraft]
  task_ids: [task-06]

- id: c97
  title: 表13-1——20%与10%增长率十年复利差2.4倍
  type: case
  example_kind: worked_example
  source_chapter: 第13章13.12 L3107-3137；表13-1 L3109-3129
  source_quote: |
    "开始时，A公司股价每股20美元（相当于每股收益1美元乘以20倍市盈率），到了第10年末时股价为每股123.80美元……B公司……期末的价格为每股26美元……高收益增长率正是创造公司股票上涨很多倍的大牛股的关键所在。"
  summary: |
    书内例题（A/B 公司演算）：每股收益同起 $1.00，A 年增 20%→第 10 年 $6.19、股价 20 倍 P/E 即 $123.80；B 年增 10%→$2.59、10 倍 P/E 即 $26。即使 A 的 P/E 因怀疑降到 15 倍仍值 $92.85；若增长 25% 则第 10 年收益 $9.31、15 倍 P/E=139 美元。沃尔玛与 The Limited 十年大涨皆建于收益复利。
  bound_to: ["13项财务指标（增长率复利）"]
  outcome: 演算结果如上（原文明确）。
  tags: [worked-example, table-13-1, compounding]
  task_ids: [task-06]

- id: c98
  title: 表13-2——行业复苏期低利润率公司弹性（B +255% vs A +47%）
  type: case
  example_kind: worked_example
  source_chapter: 第13章13.13 L3143-3182；表13-2 L3155-3178
  source_quote: |
    "在业务恢复好转的过程中，A公司的税前利润增长了将近50%，而B公司的税前利润则增长了3倍还要多，这可以解释为什么原来处于灾难边缘的不景气公司在业务反弹时能够摇身一变为一只大黑马股票。"
  summary: |
    书内例题：销售收入同为 100 美元的 A（税前利润率 12%）与 B（2%），业务好转后售价+10%、成本+5%：A 税前利润 12→17.60（约+47%），B 从 2→7.10（+255%）。推论：长期持有选高利润率公司；赌行业复苏选低利润率公司。配套数据：公众误以为公司平均利润率 20-40%，实为 5% 左右；福特 1987 年税前利润率 10.3%、Albertson's 3.6%、默克 25%+。
  bound_to: ["13项财务指标（税后/税前利润率）", "六类公司分类法（周期复苏弹性）"]
  outcome: 演算结果如上（原文明确）。
  tags: [worked-example, table-13-2, margin-elasticity]
  task_ids: [task-06, task-01]

## 第14章

- id: c99
  title: 麦当劳成熟期三招——得来速、早餐与炸鸡
  type: case
  example_kind: reported_case
  source_chapter: 第14章 L3210-3214；第15章15.1.3 L3270
  source_quote: |
    "投资者对麦当劳股票投了不信任票（1972～1982年间它的股票一直在横向盘整），但公司收益仍然继续强劲增长……增加早餐的成本非常低，却使销售增长了20%。"
  summary: |
    增长接近上限后靠新方法续命：1972-82 股价横盘、P/E 从 30 倍降到 12 倍，但收益续增——①开车取餐窗口（已超销售收入 1/3）；②早餐（开拓空白时段、低成本带来销售 +20%）；③沙拉与炸鸡（增收益且解除对牛肉成本的依赖）；④海外扩张（英国德国每条街开店还需几十年）。印证"成熟期要看新发展计划及其可行性"。
  bound_to: ["六类公司分类法（快增长的第三阶段）", "定期重新核查（新增长计划）"]
  outcome: P/E 从 30 回落到 12 后随收益续增重拾升势（原文明确）。
  tags: [reported-case, mcdonald, maturity, drive-thru]
  task_ids: [task-01, task-09]

- id: c100
  title: 得克萨斯航空——没有定期核查的双重错误（12→4.75→51.5→9美元）
  type: case
  example_kind: firsthand
  source_chapter: 第14章 L3218-3230
  source_quote: |
    "1987年2月又以每股48.25美元的价格追加购买了更多的得克萨斯航空股票……最后我终于清醒了，开始以每股17～18美元的价格抛出股票。1987年底，得克萨斯航空股价下跌到了每股9美元。"
  summary: |
    第14章核心反面案例：1983 年因大陆航空资产小仓位买入（$12→$4.75、大陆 $3 破产）；确认困境反转后大买，1986 年两只都涨 3 倍；1986 年 2 月收购东方航空后一年内 $51.5 新高（自 1983 年起 10 倍）。错误一：沉醉于"1988 年每股收益 15 美元"的预期，无视行李丢失、航班混乱、东方员工不满等日报可见的恶化信号，1987 年 2 月 $48.25 追加买入；错误二：本应据此反手重仓受益的 Delta 却只建了小仓。1987 年初收益恶化，$17-18 抛出，年底 $9。
  bound_to: ["定期重新核查（忽视恶化的代价）", "业余投资者的身边信息优势（乘客可见）"]
  outcome: 追加买入后从 $48.25 跌至 $9；林奇 $17-18 割肉（原文明确）。
  tags: [firsthand, mistake, texas-air, double-error]
  task_ids: [task-09, task-12]

- id: c101
  title: Delta——东方航空混乱中的受益者（本应重仓）
  type: case
  example_kind: firsthand
  source_chapter: 第14章 L3232
  source_quote: |
    "我本来应该利用这些消息进行基本面分析来抓住另一只大牛股：Delta航空公司的股票……到了1988年中，它的股价却迅速上涨到了每股55美元。成千上万乘坐东方航空公司和Delta航空公司飞机的乘客可能已经看到了以上我所看到的这些情况。"
  summary: |
    东方航空严重经营问题+永久性收缩，最大受益者是主要竞争对手 Delta。林奇已建仓但未加至十大重仓：1987 年夏 $48→$60，10 月 $35，年底 $37，1988 年中 $55。点题：常乘客用身边观察即可复制的投资机会。
  bound_to: ["业余投资者的身边信息优势", "定期重新核查（由恶化为他人转好）"]
  outcome: 1988 年中 $55（自 10 月低点 $35 涨约 57%；原文明确）。
  tags: [firsthand, delta, beneficiary]
  task_ids: [task-09, task-12]

## 第15章

- id: c102
  title: 德州仪器——放弃家用电脑，股价四个月+74%
  type: case
  example_kind: reported_case
  source_chapter: 第15章15.1.6 L3310
  source_quote: |
    "1983年10月这家公司宣布它将放弃家用电脑业务（这也是一个竞争对手如林的热门行业），当年公司仅家用电脑业务就亏损了5亿多美元……宣布放弃家用电脑业务的第二天，股价就从每股101美元上涨到了每股124美元，4个月后上涨到了每股176美元。"
  summary: |
    剥离亏损业务的第二个样板（与洛克希德 L-1011 并列，见 c30）：1983 年 10 月宣布退出年亏 5 亿+美元的家用电脑业务，聚焦半导体与军用电子；虽有一次性大冲销，次日 $101→$124，4 个月后 $176。配套要点：苹果账上 2 亿美元现金零债务（不会破产）；Navistar 增发稀释的反例（复苏但股价不涨）。
  bound_to: ["公司增加收益的5途径（剥离亏损业务）", "分类型核查清单（困境反转）"]
  outcome: 101→124→176 美元（原文明确）。
  tags: [reported-case, texas-instruments, exit-hardware]
  task_ids: [task-08, task-01]

- id: c103
  title: 时代公司——有线电视资产每股60美元，股价100美元
  type: case
  example_kind: firsthand
  source_chapter: 第15章15.1.6 L3312
  source_quote: |
    "仅仅有线电视部分业务的潜在价值就高达每股60美元，因此如果它的股价为每股100美元，你就等于是用每股40美元的价格购买了公司所有的其他业务。"
  summary: |
    林奇"近来最喜欢的困境反转型公司之一"，同时也是隐蔽资产型：已卖掉分公司、大幅削减成本；有线电视业务潜在价值每股 $60，$100 股价意味着其余业务（出版主业）仅按 $40 计价。演示"分部估值"在卖出决策中的应用。
  bound_to: ["分类型核查清单（困境反转/隐蔽资产）", "13项财务指标（隐蔽资产）"]
  outcome: 未说明（写书时为其偏好持仓）。
  tags: [firsthand, time-inc, cable-value]
  task_ids: [task-08, task-06]

## 第16章

- id: c104
  title: 15%对10%——十年复利演算（$40455 vs $25937）
  type: case
  example_kind: worked_example
  source_chapter: 第16章 L3420-3426
  source_quote: |
    "如果他的初始投资为1万美元，按15%的投资收益率计算，经过10年他最终积累的财富将高达40455美元，按10%的市场平均收益率计算，市场最终积累的财富只有25937美元。"
  summary: |
    收益率目标设定演算：业余者自选股应追求扣费后 12-15% 复利（战胜指数 9-10%）；年换手一次约付 4% 成本，需毛收益 16-19%。15% 十年 $10000→$40455 vs 10% →$25937。25-30% 的年收益预期不切实际（只有贝思兄弟级财富增长才做得到）。
  bound_to: ["组合构建与持有纪律（收益率目标）"]
  outcome: 演算结果如上（原文明确）。
  tags: [worked-example, return-target, compounding]
  task_ids: [task-11]

- id: c105
  title: Stop & Shop 4→44美元——"以为是股息股，其实是10倍股"（附万豪之憾）
  type: case
  example_kind: firsthand
  source_chapter: 第16章16.1 L3440-3446
  source_quote: |
    "我原来以为Stop＆Shop公司的股票最多能让我赚到大约30%～40%的投资收益率……最初我以每股4美元买入这只股票，1988年当这家公司被收购私有化时股价达到了每股44美元。"
  summary: |
    持有弹性的论据：1979 年为股息收益率买入 Stop & Shop（当时股价持续下跌），基本面越来越好（超市+Bradlee 折扣店），$4→1988 年 $44 被私有化（10 倍以上）。同段：万豪住过几千晚却只满足于香皂与热水澡、没买几千股。结论：多持几只好股，"意外的 10 倍股"概率才大；林奇从未基于并购预期买入的股票被并购过。仓位结构：增长股不超基金 30-40%、稳定与周期各 10-20%、其余困境反转；1400 只中一半资产集中于 100 只。
  bound_to: ["组合构建与持有纪律", "业余投资者的身边信息优势"]
  outcome: Stop & Shop $4→$44（原文明确）。
  tags: [firsthand, stop-shop, marriott, surprise-tenbagger]
  task_ids: [task-11]

- id: c106
  title: 6次30%的换股复利——"约等于一只4倍股"
  type: case
  example_kind: worked_example
  source_chapter: 第16章16.3 L3470-3490
  source_quote: |
    "6次有30%收益率的投资，其累计复利收益相当于投资一只上涨4倍的大牛股……如果你不能说服自己坚持'当我的股票下跌25%时我就追加买入'的正确信念……那么你永远不可能从股票投资上获得什么像样的回报。"
  summary: |
    换股纪律演算：稳定增长股涨 30-50% 即换成未涨的同类，6 次 30% 复利≈4 倍。配套纪律：只换股不换现金；股价跌 25% 追加而非止损（林奇厌恶止损指令——Taco Bell 设 10% 止损会错过 10 倍）；卖出依据是基本面变化而非价格涨跌。
  bound_to: ["组合构建与持有纪律（换股/不止损）"]
  outcome: 演算结论（原文明确）。
  tags: [worked-example, rotation, no-stop-loss]
  task_ids: [task-11]

## 第17章

- id: c107
  title: 表17-1——几次市场崩溃中的低价买入机会（1972-74 Teledyne 11→3→390）
  type: case
  example_kind: worked_example
  source_chapter: 第17章 L3496-3540；表17-1 L3506-3536
  source_quote: |
    "看看表17-1中所列出那些实力雄厚且盈利增长良好的优秀公司，在最近几次市场崩溃时你可以用很低的价格买入，获得很高的投资回报。"
  summary: |
    四轮崩溃的名单与价格（最高价→最低价→1987 年最高价）：1972-74：Teledyne 11→3→390、Cap Cities 34→9→450、麦当劳 15→4→61.125、菲利普·莫里斯 17.5→8.5→124.5、百时美 8→4→55、默克 17→7→74.25、亨氏 5.75→3→51.75；1976-78：GE 15→11→66.375、万豪 3.75→1.75→44.75；1981-82：Gannett 15→10→56；1983-84：The Limited 10→5→53、Waste Management 16→7→48。另：年底 10-12 月避税抛售期与股价跌破 $6 后的保证金/机构强制卖出制造低价。
  bound_to: ["买入时机（崩盘期/避税抛售期）"]
  outcome: 表内 1987 年最高价即验证结果（原文明确）。
  tags: [worked-example, table-17-1, crash-buying]
  task_ids: [task-14]

- id: c108
  title: 1987年崩盘中的Dreyfus——$16股价含$15净现金
  type: case
  example_kind: firsthand
  source_chapter: 第17章17.1 L3542-3563；表17-2
  source_quote: |
    "Dreyfus基金公司的股价被大量地抛售打压到每股16美元，而每股扣除债务后的净现金为15美元，这样的股票有什么投资风险呢？……我曾错过第一次低价买入Dreyfus基金公司股票的时机，但这一次我决不会错过了。"
  summary: |
    补上第 6 章/第 5 章两次错过的机会（"受骗一次，骗子太坏，受骗两次，自己太傻"）：1987 年崩盘把 Dreyfus 打到 $16，而每股净现金 $15；且公司反而受益（资金流入其货币市场基金）。表17-2 列同期十家公司：沃尔玛 41→20→31.375、家得宝 28→12.5→28.375、可口可乐 53→28→43.125、Pier 1 14→5→11.25、Inco 24→14→28.625、Envirodyne 29.25→10.875→26 等——多数一年内大幅收复。
  bound_to: ["买入时机（崩盘期）", "13项财务指标（现金头寸）"]
  outcome: 表17-2 的 1988-10 股价显示多数收复失地（原文明确）。
  tags: [firsthand, dreyfus, 1987-crash, table-17-2]
  task_ids: [task-14, task-06]

- id: c109
  title: 华纳通信——"过度上涨"一句话让林奇在$38卖出（后来$180）
  type: case
  example_kind: firsthand
  source_chapter: 第17章17.2 L3570-3588
  source_quote: |
    "1977年5月……我以每股26美元的价格买入了这只股票，投入资金相当于整个基金资产规模的3%……后来华纳股价上涨到了38美元，这时我莫名其妙毫无理由地开始大量卖出……当我抛出股票后，华纳股价继续一路攀升到50美元、60美元、70美元，最后竟然超过了180美元。"
  summary: |
    过早卖出的头号亲历：1977 年 5 月 $26 买入（占基金 3%）；一位技术分析师随口说"过度上涨"，此话挥之不去——$32 焦虑、$38 无理由大量卖出；股价随后涨过 $180。即便 1983-84 年 Atari 的 ET 游戏巨亏 5.38 亿美元致股价大跌 60% 至 $76，仍是其卖出价的两倍。教训：投资建议无论好坏都会印入脑海；上涨后持有比下跌后持有更难。
  bound_to: ["12种危险说法（煽动效应）", "组合构建与持有纪律（过早卖出）"]
  outcome: $26 买入、$38 卖出、后超 $180（原文明确）。
  tags: [firsthand, warner, sold-too-soon]
  task_ids: [task-10, task-11]

- id: c110
  title: 玩具反斗城$1买$5卖——25倍留给德罗斯（附Flowers/Lance）
  type: case
  example_kind: firsthand
  source_chapter: 第17章17.2 L3580-3586
  source_quote: |
    "以经过股票分割调整后相当于每股1美元的价格大量买入股票。1985年美国玩具反斗城公司股价上涨到了每股25美元……我买入不久之后很快就卖出了……皮特里在股价为5美元时停止买入股票，于是我就在这个价位抛出了股票。"
  summary: |
    第二个过早卖出案例：$1 大量买入，因发现皮特里（零售泰斗）停止买入便在 $5 卖出（5 倍）；1985 年 $25（25 倍）。推荐人德罗斯替客户坚决持有拿到 25 倍。同段再犯：Flowers 面包与 Lance 饼干因等并购等得不耐烦而卖出，随后被并购。反面确认：La Quinta 内部人士卖出差点吓退林奇——"因内部人士卖出而否定股票是愚蠢理由"。
  bound_to: ["组合构建与持有纪律（过早卖出）", "12种危险说法"]
  outcome: 林奇 $1→$5（5 倍）；坚持者获 25 倍（原文明确）。
  tags: [firsthand, toys-r-us, sold-too-soon, petrie]
  task_ids: [task-11, task-10]

- id: c111
  title: 卖出外国汽车股——1986-87美元贬值驱动的换仓
  type: case
  example_kind: firsthand
  source_chapter: 第17章17.4 L3612-3616
  source_quote: |
    "1986～1987年间，我认为美元汇率下跌会降低那些大部分汽车在美国销售的外国汽车制造商的利润，于是我卖出了捷豹（Jagur）、本田、Subaru和沃尔沃汽车公司的股票。"
  summary: |
    卖出决策的少数宏观例外：林奇一般不管宏观，但"美元贬值→在美销售的外国车企利润受损"属可确定影响的重大事件，故清仓捷豹/本田/斯巴鲁/沃尔沃。同时强调：90% 的卖出是因为"找到了前景更好的公司"。
  bound_to: ["分类型卖出判据（宏观例外）"]
  outcome: 未说明（换仓结果未跟踪）。
  tags: [firsthand, sell-rule, foreign-autos]
  task_ids: [task-02]

- id: c112
  title: 亚历山大鲍德温——夏威夷96000英亩与温伯格的收购
  type: case
  example_kind: reported_case
  source_chapter: 第17章17.4.6 L3720
  source_quote: |
    "亚历山大鲍德温公司拥有夏威夷岛96000英亩的土地和进入夏威夷的独家航运权……后来终于出现了一位人称哈里·温伯格先生的收购方，他买入了公司5%，然后是9%，最后是15%的股票……这只股票曾一度达到每股32美元的最高价位，在1987年10月股市崩盘时下跌到每股16美元，但过了几个月后又重新反弹到了每股30美元。"
  summary: |
    隐蔽资产股的"等袭击者"策略：真实价值远高于 $5 股价，几年无人理会；温伯格持续增持（5%→9%→15%）带动跟风，最高 $32；1987-10 崩盘 $16，数月后回 $30。规则：只要公司没大量借新债，隐蔽资产股就应等收购方出现再卖。
  bound_to: ["六类公司分类法（隐蔽资产型）", "分类型卖出判据（等收购）"]
  outcome: $5→$32，崩盘 $16 后回 $30（原文明确）。
  tags: [reported-case, alexander-baldwin, hidden-asset]
  task_ids: [task-02, task-01]

- id: c113
  title: 迪士尼与斯坦伯格——袭击并购倒逼的价值重估
  type: case
  example_kind: reported_case
  source_chapter: 第17章17.4.6 L3722-3740（注释）
  source_quote: |
    "迪士尼是一家暮气沉沉毫无生气的公司，根本不知道自身的内在价值和发展潜力，直到斯坦伯格先生出现对公司进行袭击并购才刺激公司管理层努力提升股东价值……迪士尼股票集三种股票类型于一身。"
  summary: |
    隐蔽资产+困境反转+增长三合一：1984 年斯坦伯格几天内购入 49% 股份并计划拆卖各业务；贝思兄弟作"白马骑士"回购全部股份，斯坦伯格什么都没做净赚 2300 多万美元；董事会随后聘艾斯纳，公司靠大片、迪士尼频道、海外乐园与电影资料馆/佛州加州地产重振。配套：Storer Broadcasting 同路径。
  bound_to: ["六类公司分类法（隐蔽资产型）", "分类型卖出判据（等收购）"]
  outcome: 艾斯纳十年彻底扭转业绩（注释明确）。
  tags: [reported-case, disney, steinberg, white-knight]
  task_ids: [task-02, task-01]

- id: c114
  title: 皮肯斯来富达推销"并购海湾石油"——林奇不信，雪佛龙信了
  type: case
  example_kind: firsthand
  source_chapter: 第17章17.4.6 L3724
  source_quote: |
    "布恩·皮肯斯来到富达基金公司的办公室，向我们讲述如何并购一个像海湾石油公司这样规模庞大的公司的设想……我根本不相信……直到有一天雪佛龙将收购海湾石油公司我才不得不相信。现在我情愿相信任何规模巨大的东西都有可能被收购。"
  summary: |
    林奇亲历的认知修正案例：当面听完皮肯斯有理有据的并购设想仍断定"不可能"，直到雪佛龙真的收购海湾石油。用于说明 80 年代收购集团（KKR、贝思兄弟、斯坦伯格、伊坎等可融资 200 亿美元）使任何隐蔽资产公司都可能被收购——业余者"等袭击者"的卖出策略因此更可行。
  bound_to: ["六类公司分类法（隐蔽资产型）", "分类型卖出判据（等收购）"]
  outcome: 海湾石油被雪佛龙收购（原文明确）。
  tags: [firsthand, pickens, gulf-oil]
  task_ids: [task-02, task-01]

## 第18章

- id: c115
  title: 凯撒工业——1971年美交所史上最大宗交易与"不可能再跌了"
  type: case
  example_kind: firsthand
  source_chapter: 第18章18.1 L3756-3764
  source_quote: |
    "当时凯撒工业公司已从每股25美元下跌到每股13美元。当股价跌到每股11美元的时候，在我的推荐下，富达基金公司买入了500万股……1973年我非常震惊地看着凯撒公司股价从7美元跌到6美元又跌到4美元。"
  summary: |
    林奇年轻分析师时期的亲历教训：自信 $11"绝不可能跌破 $10"而促成富达买入 500 万股（美交所史上最大宗交易之一），还劝母亲买入（幸未听）；1973 年 $7→$6→$4 才见底。事后核算：流通股仅 2500 万股、$4 即总市值 1 亿美元（当时约 4 架波音 747）；公司拥有地产、铝、钢、水泥、造船、广播电视、吉普车等业务、负债极少，清算价值每股至少 $40；不久反弹至 $30。教训：没有任何法则能告诉你底部在哪。
  bound_to: ["12种危险说法（不可能再跌了）"]
  outcome: $11 买入后最深跌至 $4，后反弹 $30（原文明确）。
  tags: [firsthand, kaiser, falling-knife]
  task_ids: [task-10]

- id: c116
  title: 菲利普·莫里斯75美分买入者的账本（$1000→$166000）
  type: case
  example_kind: worked_example
  source_chapter: 第18章18.3 L3776-3848；图18-1
  source_quote: |
    "任何一个投资者如果能够一直持有菲利普·莫里斯公司的股票，都会非常高兴地看到这只股票从每股0.75美元的价格上涨到了每股124.5美元，也就是说原来1000美元的投资最后上涨到了166000美元，并且这还不包括在上涨过程中所获得的23000美元的股息。"
  summary: |
    "股价这么高不可能再涨"的反例演算：50 年代 $0.75 买入者若 1961 年以 $2.5 卖出（3.3 倍），将错过其后 23 倍；全程持有 $0.75→$124.5，$1000 变 $166000+股息 $23000。图18-1 两处手绘椭圆圈注 1955-56 与 1971-73 高点，点评"不可能再涨了！谁说的？"。
  bound_to: ["12种危险说法（已经这么高了不可能再涨）", "组合构建与持有纪律"]
  outcome: 0.75→124.5 美元；含股息 $1000→$189000（原文明确）。
  tags: [worked-example, philip-morris, hold-forever]
  task_ids: [task-10, task-11]

- id: c117
  title: 斯巴鲁涨20倍后林奇仍买入——又赚7倍
  type: case
  example_kind: firsthand
  source_chapter: 第18章18.3 L3844
  source_quote: |
    "在斯巴鲁公司已经上涨了20倍以后……我查看了公司的基本面，发现斯巴鲁的股价相对于其实际价值仍然十分便宜，于是就买入了这只股票，后来这只股票让我获得了7倍的投资回报。"
  summary: |
    "涨高了不敢买"的正面反例：已涨 20 倍的斯巴鲁，经基本面核查相对实际价值仍便宜，林奇买入后再获 7 倍。要点：股票能涨多高没有人为上限；"涨 1 倍就卖"的 advisers 应感到羞愧。
  bound_to: ["12种危险说法（不可能再涨）"]
  outcome: 再获 7 倍（原文明确）。
  tags: [firsthand, subaru, twenty-bagger]
  task_ids: [task-10]

- id: c118
  title: "$3的股票能亏多少"——50美元亏99%对3美元亏83%
  type: case
  example_kind: worked_example
  source_chapter: 第18章18.4 L3854-3864
  source_quote: |
    "无论一只股票股价是50美元还是1美元，当这只股票股价下跌到零时，对于你来说都是老本亏了个精光，亏损都是100%……猜一猜空头投机者在股价为8美元或6美元时把股票卖给了谁？"
  summary: |
    算术拆穿低价安全感：$50 买入跌到零亏 99%、$3 买入跌到零亏 83%，五十步笑百步；$1000 无论买 $43 还是 $3 的股票，跌到零都亏 $1000。空头恰恰在 $8/$6 的底部区建仓，接盘的正是念叨"能亏多少"的捡便宜者。
  bound_to: ["12种危险说法（3美元能亏多少）"]
  outcome: 演算结论（原文明确）。
  tags: [worked-example, low-price-fallacy]
  task_ids: [task-10]

- id: c119
  title: "黎明前最黑暗"——石油钻井4520→686口与货车95650→5700辆
  type: case
  example_kind: reported_case
  source_chapter: 第18章18.6 L3876-3880
  source_quote: |
    "在1981年，美国作业的石油钻井有4520口，到1984年就只有2200口了……两年过去后还在作业的钻井减少到只有686口……运输货车总数从1979年95650辆的高峰下滑到1981年的44800辆的低谷……1982年货车总数下滑到了17582辆，到1983年更是下滑到5700辆。"
  summary: |
    行业数据反例：1984 年钻井已从 4520 口腰斩至 2200 口，"最坏已过"的买家两年后再看只剩 686 口（至今不足 1000）；货车运输 1979 年 95650 辆→1983 年 5700 辆，行业重挫 90%。"有时在最后变得一片漆黑之前也总是最黑暗的。"
  bound_to: ["12种危险说法（黎明前最黑暗）"]
  outcome: 两个行业继续恶化如数字（原文明确）。
  tags: [reported-case, oil-rigs, trucking]
  task_ids: [task-10]

- id: c120
  title: 默克——9年不动的股价与连增14%的盈利（后5年4倍）
  type: case
  example_kind: firsthand
  source_chapter: 第18章18.9 L3900-3957；图18-2
  source_quote: |
    "从1972～1981年，这只股票的股价一动不动，尽管公司盈利平均每年稳步增长14%。后来发生了什么呢？在随后的5年中这只股票股价上涨了4倍……我这样做了，而且我这样做取得了丰厚的回报。"
  summary: |
    林奇亲历持有：默克 1972-81 股价横盘而盈利年增 14%（图18-2 中文点评："我这样做了，而且我这样做取得了丰厚的回报"），随后 5 年涨 4 倍。配套"一块石头的心电图"论：股价长期一条直线是好兆头。多数人赚钱都在持有不动股票三四年之后，默克只是让他等得更久。
  bound_to: ["12种危险说法（等太久了不可能涨）", "收益决定股价（背离终将收敛）"]
  outcome: 后 5 年 4 倍；林奇持有获丰厚回报（原文明确）。
  tags: [firsthand, merck, flat-line]
  task_ids: [task-10, task-05]

- id: c121
  title: 一动不动股票群——Lukens 15年6倍等五个结局
  type: case
  example_kind: reported_case
  source_chapter: 第18章18.9 L3953-3959
  source_quote: |
    "Lukens公司的股票在15年内上涨了6倍，American Greeting公司的股票在6年内上涨了6倍，Angelica公司的股票4年内上涨了7倍，Brunswick公司的股票6年内上涨了6倍，史克公司的股票2年内上涨了3倍。"
  summary: |
    盘整期样本与结局：Angelica 1974-79 股价波动不超 5 美分、American Greeting 8 年不动、GAF 11 年、Brunswick 整个 70 年代、史克推泰胃美前后 10 年、Harcourt Brace 12 年、Lukens 14 年——随后分别 4-15 年内上涨 3-7 倍。耐心持有"所有人都不理睬"的好公司终有回报。
  bound_to: ["12种危险说法（等太久了不可能涨）"]
  outcome: 五家公司 3-7 倍不等（原文明确）。
  tags: [reported-case, flat-stocks, patience]
  task_ids: [task-10]

- id: c122
  title: 错过家得宝去买Scotty——"下一只"的代价（家得宝25倍 vs Scotty+25%）
  type: case
  example_kind: reported_case
  source_chapter: 第18章18.11 L3971-3977
  source_quote: |
    "家得宝自从上市以后上涨了25倍，而Scotty只上涨了25%～30%，远远落后于同期的股市整体上涨水平……错过大牛股并不会让你发生任何亏损……为了弥补第一个错误而犯下的下一个错误却会让你付出损失真金白银的代价。"
  summary: |
    错上加错的算术：错过玩具反斗城而买 Greenman Brothers（持续下跌）；错过家得宝而买"下一个家得宝"Scotty（仅 +25-30%，跑输大盘）；错过皮埃蒙特而买人民航空、错过 Price Club 而买 Warehouse。多数情况下，以更高价买被吹捧的典范公司，好过便宜买"下一个"。
  bound_to: ["12种危险说法（抓住下一只大牛股）", "避而不买清单（'下一个'公司）"]
  outcome: 家得宝 25 倍 vs Scotty +25-30%（原文明确）。
  tags: [reported-case, home-depot, scotty]
  task_ids: [task-10, task-04]

- id: c123
  title: Zapata vs Ethyl——1981年被看好的跌96%，被叫"死狗"的涨16倍
  type: case
  example_kind: reported_case
  source_chapter: 第18章18.12 L3979-3987
  source_quote: |
    "看起来似乎更好的Zapata公司股价却从35美元下跌到了2美元……与此同时……Ethyl的股价从2美元上涨到了32美元。"
  summary: |
    "股价涨=选对了"的对照反例：1981 年能源繁荣中 Zapata（$35）人人看好，Ethyl 因 EPA 禁含铅汽油添加剂被称"被碾伤的狗"（$2）；其后 Zapata $35→$2，Ethyl 靠精细化工+海外+保险 $2→$32。短期涨跌既不证明选对也不证明选错，只说明有人出价更高/更低。
  bound_to: ["12种危险说法（涨了就是对、跌了就是错）"]
  outcome: Zapata -94%、Ethyl +1500%（原文明确）。
  tags: [reported-case, zapata, ethyl]
  task_ids: [task-10]

## 第19章

- id: c124
  title: "万无一失公司"的期权——判断全对仍亏光$3000
  type: case
  example_kind: worked_example
  source_chapter: 第19章19.1 L4013-4031
  source_quote: |
    "你购买的3000美元的期权价值已经损失掉一半……结果一个月后，股价还是没上涨，期权到期后变得一文不值，你的3000美元投资全部打了水漂……这家万无一失公司的股票真的开始大涨，可是你却一股也没有买。"
  summary: |
    期权否定的核心例题：$3000 本可买 150 股 $20 的"万无一失公司"（已发现泰胃美级利好），却买 4 月到期、行权价 $20、$1/份 的看涨期权（涨到 $35 期权变 $15、账面 $45000）；两个月股价不动，期权先腰斩再归零；数周后股价真的大涨而本金已尽。附加事实：交易所统计 80-95% 的业余期权/期货参与者亏损；期权 1-2 个月到期、需连续购买、佣金高企；"组合保险"（越跌越卖股票买期货）是 1987 年 10 月崩盘主因。
  bound_to: ["否定期权期货（时间损耗归零）"]
  outcome: $3000 归零；判断正确与盈利无关（例题结论明确）。
  tags: [worked-example, options, expire-worthless]
  task_ids: [task-15]

- id: c125
  title: 宝丽来卖空演算——$140卖空到$14的理论盈利与无限风险
  type: case
  example_kind: worked_example
  source_chapter: 第19章19.2 L4043-4051
  source_quote: |
    "你就可以等待宝丽来股价跌到14美元时，用14000美元买回1000股股票……二者冲抵后你会赚到126000美元的盈利……如果股价再上涨一倍达到更加不可思议的每股300美元……你只能被迫平仓，因此承受巨额的亏损。"
  summary: |
    卖空机制的算术演示：$140 融券卖出 1000 股宝丽来（账户记 $140000 负债），$14 回补赚 $126000。但三大缺陷：借股期间股息归出借人；账面盈利在回补前不可动用；股价涨到 $300 时须追加数十万保证金否则被迫平仓——股价上涨无上限，卖空亏损无限。
  bound_to: ["否定卖空（亏损无限）"]
  outcome: 演算两分支如上（原文明确）。
  tags: [worked-example, short-selling, polaroid]
  task_ids: [task-15]

- id: c126
  title: 罗伯特·威尔森卖空Resorts International——判断对了仍亏2000-3000万
  type: case
  example_kind: reported_case
  source_chapter: 第19章19.2 L4053-4055
  source_quote: |
    "就在罗伯特·威尔森卖空股票的期间，国际度假胜地公司的股价从最初的70美分上涨到了70美元，上涨了整整100倍，使得卖空股票的威尔森先生亏损了2000万～3 000万美元。"
  summary: |
    卖空否定的真人案例：精明的威尔森判断正确（公司终将崩溃），但股价先从 $0.70 涨到 $70（100 倍），他亏 2000-3000 万美元离场——"最终是多久？从长期看我们都死了。"卖空不仅需要判断对，还需要耐心、勇气与足够资本扛过上涨。
  bound_to: ["否定卖空（判断对也未必活着见到）"]
  outcome: 威尔森亏 2000-3000 万美元（原文明确）。
  tags: [reported-case, robert-wilson, resorts]
  task_ids: [task-15]

## 第20章

- id: c127
  title: 重大新闻与股市反应错位——从肯尼迪当选到欧佩克禁运（含1985七国会议）
  type: case
  example_kind: firsthand
  source_chapter: 第20章 L4061-4081
  source_quote: |
    "可能爆发核战争的大灾难给华尔街带来的恐惧竟然还不如总统对企业的干预……1973年10月19日……欧佩克宣布石油禁运，导致股市在3个月内下跌了16%，在12个月内下跌了39%……当天股市还上升了4点。"
  summary: |
    林奇亲历的历史事件账本：1960 肯尼迪当选股市上涨；古巴导弹危机跌幅不到 3%；肯尼迪遇刺当天不到 3%、3 天补回；肯尼迪谴责钢铁业反跌 7%（史上最大单日跌幅之一）；尼克松物价管制 +3%、辞职仅 -1%；欧佩克禁运当天 +4 点、随后 12 个月 -39%。真正影响持久的是 1985-9-22 七国会议（美元贬值），股市 6 个月 +38%、受益出口公司两年涨 2-3 倍——而 1987-10-19 的 508 点大跌长期看远不如它重要。另：70 年代"最佳50股"从 1973 年道指 1050 跌到 1974-12 的 578，蓝筹跌 50-90%；1982-83 小高科技随后跌 60-98%；日本 1966-88 涨 17 倍（美国 2 倍）。
  bound_to: ["不预测市场，投资的是公司", "12种危险说法（把新闻当信号）"]
  outcome: 各事件当日与其后走势如述（原文明确）。
  tags: [firsthand, news-vs-market, nifty-fifty, japan]
  task_ids: [task-14, task-10]

- id: c128
  title: 凯玛特与Masco——从濒临倒闭商店到水龙头1000倍
  type: case
  example_kind: reported_case
  source_chapter: 第20章 L4103-4105
  source_quote: |
    "SS Kresge，一个濒临倒闭的专售廉价物品的商店，成功发展出凯玛特购物中心的经营模式，结果这家公司股票十年里上涨了40倍。Masco成功开发出了单柄水龙头，公司股票上涨了1000倍，成为40年来股价表现最伟大的一只股票。"
  summary: |
    长线对照集：SS Kresge 靠凯玛特模式十年 40 倍；生产单柄水龙头的 Masco 涨 1000 倍（40 年最伟大股票）；AT&T 解体的小贝尔 4 年涨 1 倍（AT&T 解体是全书认定的第一里程碑事件，影响 296 万股东）。对照：小道消息乱飞的耳语公司走向破产。
  bound_to: ["业余投资者的身边信息优势（平淡业务出大牛股）", "组合构建与持有纪律"]
  outcome: 40 倍、1000 倍、小贝尔 4 年 1 倍（原文明确）。
  tags: [reported-case, kmart, masco, baby-bells]
  task_ids: [task-12, task-11]

- id: c129
  title: 1987年机构宠儿名单——10个月后遭抛售的十家好公司
  type: case
  example_kind: firsthand
  source_chapter: 第20章 L4111-4117
  source_quote: |
    "这些股票在1987年中期时是大型机构投资者的宠儿，但过了10个月后，尽管它们具有较高的收益、令人兴奋的发展前景以及良好的现金流，却被这些机构投资者无情地以很低的价格抛出……这些公司包括：自动数据处理公司、可口可乐、Dunkin's Donuts、通用电气……"
  summary: |
    机构行为案例：ADP、可口可乐、Dunkin' Donuts、GE、Genuine Parts、菲利普·莫里斯、Primerica、Rite Aid、施贵宝、废物管理——公司本身毫无变化，仅因机构失去兴趣而在 10 个月内遭低价抛售。结论：5 万专业投资者主宰市场，但只在波动最后 20% 的时间里"正确"；业余者可反向利用（乌合之众挤出口时走向入口）。
  bound_to: ["专业投资者的制度性劣势（滞后性与羊群）", "买入时机（机构抛售期）"]
  outcome: 名单与行为如述（原文明确）。
  tags: [firsthand, institutional-favorites, 1987]
  task_ids: [task-12, task-14]

- id: c130
  title: 星期一效应——1987年全年+42点，周一合计-483点
  type: case
  example_kind: worked_example
  source_chapter: 第20章 L4131-4137
  source_quote: |
    "1953～1984年，股市总共上涨了919.6点，在此期间所有星期一的交易日总共下跌了1565点……1987年股市总共上涨了只有42点，在此期间所有星期一的交易日总共下跌了483点。"
  summary: |
    数据演算+林奇的心理解释：1953-84 全年累计 +919.6 点而周一累计 -1565 点；1987 年全年 +42 点、周一 -483 点。解释：周末 60 小时无法与公司交流，投资者积攒恐惧（日元、尼罗河洪水、杀人蜂），周一上午恐慌卖出；周一后几天打电话给公司发现一切正常，故反弹。
  bound_to: ["不预测市场（对宏观噪音的解构）"]
  outcome: 统计口径与解释如述（原文明确）。
  tags: [worked-example, monday-effect]
  task_ids: [task-14]

- id: c131
  title: Taco Bell与百事的收购要约——$40卖出者放弃的$150
  type: case
  example_kind: reported_case
  source_chapter: 第20章 L4155-4159
  source_quote: |
    "当百事可乐以每股40美元的价格要约收购Taco Bell公司的股票时……马上就把股票高价卖给收购方了……根据这家公司强劲的盈利能力计算，现在一个独立的Taco Bell公司的实际价值应该相当于每股150美元。"
  summary: |
    并购热潮的阴暗面：百事 $40 要约收购 Taco Bell 时持有人欢天喜地卖出，但该公司此后继续快速增长，按盈利能力计算独立价值应达每股 $150——收购方拿走了长期复利。通用化演算：$10 底部股被 $20 要约（一夜翻倍）看似大喜，但 $10→$100 的全程中，$20 卖出者每股只赚 $10、让渡 $80。
  bound_to: ["分类型卖出判据（并购要约≠必然卖出）", "组合构建与持有纪律"]
  outcome: Taco Bell 独立估值 $150（书中口径）；要约价 $40（原文明确）。
  tags: [reported-case, taco-bell, buyout]
  task_ids: [task-02, task-11]

- id: c132
  title: 林奇的林奇定律与麦哲伦履历（背景性亲历，供能力卡引用）
  type: case
  example_kind: firsthand
  source_chapter: 第1章 L195-275；导论 L171
  source_quote: |
    "我接管时富达麦哲伦基金资产规模为2000万美元，但整个投资组合却只有40只股票……走出他的办公室后，我把持股总数增加到了60只，六个月后又增加到了100只……如今富达麦哲伦基金的资产规模已经增长到了90亿美元。"
  summary: |
    作者履历的骨架数据（作为下游 skill 的经验背书而非独立方法案例）：1977-5 接管麦哲伦（2000 万美元、40 只）→加至 60/100/150 只→写书时 1400 只、90 亿美元、12 年净值涨 20 多倍、1985-6 起为全美最大基金、战胜 98% 的普通股票基金；其间一度持有 150 只储贷协会股票。"林奇定律：林奇高升，股市下跌。"1987 年 8 月基金净值 +40%、11 月 -11%、全年 +1%。
  bound_to: ["专业投资者的制度性劣势（规模之弊）", "组合构建与持有纪律"]
  outcome: 12 年 20 多倍；1987 年勉强保住不亏记录（原文明确）。
  tags: [firsthand, magellan, background]
  task_ids: [task-11, task-12]

---

## 提取器自检

- [x] 全部 132 条均有 `bound_to`（方法论主题至少 1 个），无纯故事条目；背景性履历条目（c132）已显式标注用途。
- [x] 亲历与转述严格区分：firsthand 均为林奇/麦哲伦/富达的操作、拜访、持仓或亲历在场；化名故事（汉德图斯、布恩·道格）标注 reported_case 并注明"化名"；虚构例题（Cajun清洁剂、寡妇德克斯特、万无一失公司、皮格钢铁、Zapata 对照情境）标注 worked_example。
- [x] 表13-1（c97）、表13-2（c98）、表0-1（c01）、表3-1（c13）、表8-1（c46）、表17-1/17-2（c107/c108）、表6-1（c23）、表12-1/12-2（c80）均为 worked_example/数据表案例。
- [x] 关键数字与原文一致抽检：克莱斯勒 1982 年 $6 起、两年 5 倍、五年 15 倍、仓位 5%、$1.50 抄底=32 倍（L1364-1366）；La Quinta 15 倍/10 年 11 倍两个口径均照录（L2423/L2451）；福特每股净现金 $16.30、实际买价 $21.70、P/E 3.1（L2828-2830）；宝丽来 $143.5→$14.125、18 个月 -89%（L2353/L3754）；得州航空 1983 买→1986 年 $51.5（10 倍）→1987-2 追加 $48.25→年底 $9（L3218-3230）。
- [x] 覆盖检查：原书各章均有条目；第 1 章球童经历、玛雅寓言、鸡尾酒会理论（作者自嘲不可当真）、冯内古特小说等纯叙事/寓言未收录（BOOK_OVERVIEW 已列其为 GLOSSARY/DIGEST 素材）。
- [ ] 阶段 1.5 来源核查待进行（source_quote 均为原文照录，行号已给）。

