# 《彼得·林奇的成功投资》— 反例提取（counter-example-extractor 产出）

> 阶段 1 并行产出。来源：source_合并转写稿.md（行号 L* 均指该文件），经 FTS 索引召回 + 原文逐段核验。
> 覆盖：12种危险说法（第18章逐条）、6类避而不买（第9章逐类）、林奇自认错误（缅因州制糖/Bildner's/错过清单/过早卖出/得州航空/Radice/锐步等）、机构失败模式（滞后性/四项检验/掩埋罪证/规模限制）、估值与财务指标陷阱、心理陷阱、期权期货卖空否定。
> 共 88 条，供下游能力卡 Boundary(B) 段使用。task_ids 对应 BOOK_OVERVIEW.md 的 task-01~task-15。

---

## A. 认知与信息陷阱（导论 + 第1-5章）

```yaml
- id: ce01
  title: 产品畅销不等于股票好（帮宝适谬误 / 科尔克椰菜娃娃）
  type: counter-example
  source_chapter: 导论 0.6 · L163-169
  source_quote: |
    "科尔克公司仅仅凭着生产20世纪最畅销的玩具'椰菜娃娃'仍然无法挽救这家资产负债表
    非常糟糕的公司最终陷入破产的命运……1983年最高上涨到65美元，但股价最终还是下跌
    到了只有1.75美元。找到有发展潜力的公司只是股票投资的第一步，接下来第二步还要
    仔细进行研究分析。"
  failure_mode: |
    因为身边看到某产品热销就直接买其公司股票，跳过第二步基本面研究；畅销产品
    可能只占净利润极小比例（帮宝适之于宝洁），或公司资产负债表本已糟糕（科尔克）。
  mechanism: |
    消费者感知到的是产品成功，而股价取决于净利润占比、财务结构与估值。产品畅销
    信息高度公开，反而常常已被市场定价甚至过度定价；没有"净利润影响比例+资产负债表"
    两步核验，感知优势无法转化为投资优势。
  warning_signs:
    - 购买理由只有"这个产品到处都在卖"
    - 说不出该产品占公司总销售额/净利润的比例
    - 未看过公司资产负债表就下单
  bound_to:
    - "业余优势利用（身边信息只能作为线索，不能作为结论）"
    - "公司分类前的产品影响测算（7.1）"
  tags: [counter-example, product-fallacy, consumer-signal]
  task_ids: [task-12, task-13]

- id: ce02
  title: 投资自己完全搞不懂业务的公司
  type: counter-example
  source_chapter: 导论 0.5 · L155-161
  source_quote: |
    "如果你连这些词汇是用来描述赛马奔跑的速度还是电脑存储芯片的速度都搞不清的话，
    那么你最好还是离这些一般人根本搞不懂其业务的公司的股票远点。"
  failure_mode: |
    买进业务术语都读不懂的公司（1兆静态随机存取存储器、双极简化指令系统……），
    无法判断收益来源、竞争格局与风险，等于闭眼下注。
  mechanism: |
    越不懂的业务越容易被故事和术语包装出专业感与稀缺感，触发"别人懂我也要抢"的
    心理；不懂则后续既不能核查基本面变化，也拿不住或不知道何时该卖。
  warning_signs:
    - 招股说明/研报里的技术名词一个也解释不了
    - 依赖"分析师推荐"替代自己判断
    - 只能复述公司宣传语，说不出公司怎么赚钱
  bound_to:
    - "能力圈原则（身边信息优势方法论）"
    - "两分钟独白（讲不清故事就不能买）"
  tags: [counter-example, competence-circle, tech-jargon]
  task_ids: [task-07, task-12]

- id: ce03
  title: 按图索骥的投资者——舍近求远追温彻斯特磁盘
  type: counter-example
  source_chapter: 导论 0.3 · L107-127
  source_quote: |
    "汉德图斯对磁盘驱动器一窍不通……还是拨通了经纪人电话……温彻斯特磁盘驱动器公司
    在这一季度的销量非常差，结果导致其股价从10美元跌到了5美元。"
  failure_mode: |
    放弃妻子天天光顾、生意火爆的 The Limited 服装店不买，转而买报纸吹捧、自己
    一无所知的温彻斯特磁盘驱动器公司，10美元跌到5美元割肉出局。
  mechanism: |
    "远处的消息显得更专业"错觉：印刷成铅字、被大券商列上推荐名单的信息自带权威感；
    身边可验证的信息反而被当作生活琐事忽略。热门行业（磁盘驱动器）同时涌入30-35家
    竞争者，行业高增长与个股盈利脱节。
  warning_signs:
    - 买远处的热门、忽略身边的熟悉
    - 决策依据是"美林把它列上推荐名单"
    - 行业增速数字漂亮但说不清这家公司的护城河
  bound_to:
    - "业余优势利用"
    - "利基/竞争壁垒检验（8.1.9）"
  tags: [counter-example, designed-investor, wall-street-hype]
  task_ids: [task-12, task-13]

- id: ce04
  title: 高位追热门股——汉德图斯50美元买The Limited
  type: counter-example
  source_chapter: 导论 0.3 · L129-141
  source_quote: |
    "汉德图斯以每股50美元的价格买入了The Limited公司的股票，这个价位几乎是1987年
    的最高价位，不久股票的价格下跌到了16美元一股。在下跌50%到差不多每股25美元时，
    他赶紧把股票给卖掉了。"
  failure_mode: |
    等股票上了推荐名单、杂志封面、30位分析师跟踪之后才"发现"它，买在几乎最高点，
    跌一半后割肉——同一只好股票上完成了"错过→追高→割肉"全套错误。
  mechanism: |
    机构与媒体集中覆盖时恰恰是信息红利耗尽、股价透支之时（滞后性的另一面）；
    此时买入者既无成本优势也无认知优势，只能靠下一个更傻的接盘者。
  warning_signs:
    - 自己是因为杂志封面/电视节目/推荐名单才知道这只股票
    - 身边人（妻子）早已对该店失去兴趣（衣服变贵、款式变差）却听不进去
    - 分析师数量、机构持股比例骤增
  bound_to:
    - "业余优势利用"
    - "快速增长型卖出信号核查（17.4.4：40个分析师+60%机构持股=卖出）"
  tags: [counter-example, chase-high, media-hype]
  task_ids: [task-12, task-09]

- id: ce05
  title: 林奇自己也错过The Limited（高位才买、赔钱持有）
  type: counter-example
  source_chapter: 导论 0.4 · L145-147
  source_quote: |
    "我也和汉德图斯一样在The Limited公司受到广泛关注并且经营状况已经开始恶化的时候
    才买入了它的股票，甚至直到现在我还持有着这只让我赔了很多钱的股票。"
  failure_mode: |
    专业基金经理同样会错过眼皮底下的十倍股，并且在关注度顶峰（基本面已开始恶化时）
    才买入，然后因不甘心而长期持有赔钱股。
  mechanism: |
    作者以此自证：错过不是业余者的专利；补救办法不是追高，而是"身边永远有足够的
    十倍股"，小组合抓住一只即可。同时警示：被广泛认可与基本面恶化常同时出现。
  warning_signs:
    - 因"大家都在买"而补偿性买入错过的牛股
    - 买入时公司已从第二阶段进入饱和期
  bound_to:
    - "错过心理管理（18.10/18.11）"
    - "定期重新核查（买入理由失效要重估）"
  tags: [counter-example, self-admitted, missed-tenbagger]
  task_ids: [task-09, task-12]

- id: ce06
  title: 盲目听信专业投资者的建议
  type: counter-example
  source_chapter: 导论 · L10-16
  source_quote: |
    "第一条投资准则是：千万不要听信任何专业投资者的投资建议！……只有当业余投资者
    一味盲目听信于专业投资人时，他们在投资上才会变得十分愚蠢。"
  failure_mode: |
    跟风买入"林奇正在买"的股票：①他可能错（其自认约40%时间表现愚蠢）；②你不知道
    他何时变卦卖出；③你本有更好的身边信息源。
  mechanism: |
    把他人结论当自己的判断，既丢失信息优势又丢失卖出纪律；抄作业者总是在基金
    季报公布后追高，在基金经理调仓后踩空。
  warning_signs:
    - 买入理由是"某某大佬买了"
    - 无法独立回答"这家公司属于六类中哪一类"
  bound_to:
    - "业余优势利用"
    - "两分钟独白"
  tags: [counter-example, authority-bias, copy-trade]
  task_ids: [task-12, task-07]

- id: ce07
  title: 缅因州制糖——增长依赖无法控制的第三方
  type: counter-example
  source_chapter: 第1章 · L257-263
  source_quote: |
    "缅因州的农民非常谨小慎微。第一年他们只试种了1/4英亩……当终于把种植面积扩大到
    1英亩时，炼糖厂不得不因业务量不足而关门停业……股价跌到了每股6美分。经过这次
    投资惨败之后，我发誓再不购买像缅因州制糖公司这类公司的股票。"
  failure_mode: |
    林奇服役期间自认"稳赚不赔"的股票损失惨重：公司利润完全取决于千万个谨小慎微的
    农民是否快速改种甜菜，而农民行为公司根本无法控制。
  mechanism: |
    商业计划的外部关键环节若由慢决策、零违约成本的分散第三方掌握，收入兑现速度
    会远低于测算；林奇买股票时人在韩国，仅凭朋友推荐+故事就重仓。
  warning_signs:
    - 收入模型依赖大量第三方的行为改变（渠道、农户、加盟商）
    - 自己身在远处、无法实地验证就下单
    - 产生"稳赚不赔"的确定感
  bound_to:
    - "两分钟独白（必须说清成功的前提条件）"
    - "快速增长型公司核查（扩张计划可执行性）"
  tags: [counter-example, self-admitted, third-party-dependency]
  task_ids: [task-07, task-12]

- id: ce08
  title: 华尔街滞后性——好公司无人覆盖，追随时已晚
  type: counter-example
  source_chapter: 第2章 2.1 · L307-333
  source_quote: |
    "The Limited公司1981年已开400家专卖店，此时仅有6位分析师跟踪……1985年股价15美元
    时大多数分析师才开始加入唱赞歌队伍，使股价狂涨到52.875美元——已远脱离基本面。
    SCI上市后整整10年竟没有一位分析师关注……对IBM跟踪的分析师有56人之多。"
  failure_mode: |
    机构系统性晚发现：等分析师齐推荐、机构齐买入时往往已是顶部（The Limited 52.875
    美元）；而业余者若同样等"权威确认"再买，就同时放弃了信息优势和制度优势。
  mechanism: |
    机构等别人先买才敢买的胆怯文化（滞后性）+覆盖名单趋同，导致覆盖数与股价位置
    正相关：分析师最多时恰是风险最高时。
  warning_signs:
    - 某股票分析师数量短期内翻倍
    - 自己的买入理由是"机构开始进场了"
  bound_to:
    - "业余优势利用（要早于华尔街发现，而不是跟随）"
    - "13条选股准则之8.1.5（机构没有持股是买入优点而非风险）"
  tags: [counter-example, institutional-lag, analyst-coverage]
  task_ids: [task-12, task-03]

- id: ce09
  title: 批准名单与"四项检验全部合格"
  type: counter-example
  source_chapter: 第2章 2.2 · L335-355
  source_quote: |
    "列入选股名单中的每一只股票往往必须得到30位投资管理人员的一致同意，但是既然
    根本不存在一部由全体委员会成员共同写成的名著……也不存在由委员会选出的股票组合
    会取得非凡的投资业绩。"
  failure_mode: |
    机构用层层审批的统一名单选股：先找"拒绝买入的理由"保饭碗，再由委员会一致同意
    产生平庸组合；养老金账户只能得到普普通通的回报。
  mechanism: |
    惩罚差异、奖励从众的考核结构（琼斯因业绩低于邻居而威胁抽资），使"业绩差异化"
    成为机构最怕的风险；对业余者的含义：机构冷落名单是寻宝地，机构抱团名单是危险区。
  warning_signs:
    - 自己持仓与热门机构持仓高度重合
    - 用"大家都通过了检验"代替自己的研究
  bound_to:
    - "业余优势利用（反向机会）"
    - "避而不买清单（机构扎堆=热门）"
  tags: [counter-example, institutional-failure, approved-list]
  task_ids: [task-04, task-12]

- id: ce10
  title: 掩埋罪证——机构卖掉赔钱股、留住账面盈利股
  type: counter-example
  source_chapter: 第2章 2.2 · L357-393
  source_quote: |
    "不分青红皂白就把目前暂时赔钱的股票全部卖掉的做法被称为'掩埋罪证'……即使后来
    （七棵橡树）股价上涨了10倍，也还是会从养老金账户中被剔除，因为弗林特本人不喜欢
    这只股票。"
  failure_mode: |
    布恩·道格被客户每季拷问，被迫卖掉不知名但优质的七棵橡树、留住人人皆知但收益
    平平的施乐——按持有者情绪而非基本面调仓，最终从独立思考退化为集体思考。
  mechanism: |
    基金经理1/4工作时间用于向客户解释；赔钱股=需要辩护的证据，卖掉即销毁证据。
    短期账面好看的激励压倒长期收益。
  warning_signs:
    - 自己因为"这只股票让我在朋友面前丢脸"而想卖
    - 持仓按成本与浮盈浮亏分类而非按公司类型与基本面分类
  bound_to:
    - "分类型卖出判据（17.4，按基本面而非账面盈亏卖）"
    - "拔掉鲜花浇灌野草之戒（16.3）"
  tags: [counter-example, institutional-failure, burying-evidence]
  task_ids: [task-02, task-11]

- id: ce11
  title: 机构规模限制错失十倍股（10%/5%/市值门槛）
  type: counter-example
  source_chapter: 第2章 2.3 · L399-413
  source_quote: |
    "在这些限制下，你根本不可能购买七棵橡树或Dunkin's Donuts……Scudder等一流基金
    恰恰在克莱斯勒跌到最低点（3.5美元）之前停止追踪，直到它再次上涨到30美元才重新
    列入名单。"
  failure_mode: |
    基金持股≤公司股本10%、单股≤基金资产5%、市值门槛三重限制，使大基金只能在大
    公司里打转，并在小公司"从很便宜涨到价格很高"后才被允许买入（克莱斯勒3.5→30）。
  mechanism: |
    合规规则为防风险而设，副作用是把最大的超额收益区（无机构覆盖的小市值公司）
    划为禁区；业余者无此限制，这是制度性套利空间。
  warning_signs:
    - 因"市值太小、机构进不去"而放弃研究（逻辑颠倒）
  bound_to:
    - "业余优势利用"
    - "13条选股准则之8.1.5"
  tags: [counter-example, institutional-failure, size-constraint]
  task_ids: [task-12, task-03]

- id: ce12
  title: 饭碗逻辑——"买IBM亏钱不丢饭碗"
  type: counter-example
  source_chapter: 第2章 2.2 · L339-341
  source_quote: |
    "'如果你购买的是IBM的股票而使客户资金遭受损失，那么你永远不会因此而丢掉饭碗。'
    ……当沃尔玛股价只有4美元时专业投资者并不会购买，等到40美元、50位分析师跟踪时
    他们才买。"
  failure_mode: |
    专业者在"不知名公司赚大钱"与"知名公司亏小钱"之间永远选后者，导致4美元的沃尔玛
    没人买、40美元的沃尔玛抢着买。
  mechanism: |
    声誉风险不对称：买IBM亏钱是IBM的错，买La Quinta亏钱是经理的错。业余者若模仿
    这种"安全"偏好，等于放弃自己的全部优势去承担机构的缺点。
  warning_signs:
    - 自己选股时优先"说出去有面子"的知名公司
    - 对不知名公司的第一反应是风险而不是机会
  bound_to:
    - "业余优势利用"
    - "避而不买清单（热门不等于安全）"
  tags: [counter-example, institutional-failure, career-risk]
  task_ids: [task-12]

- id: ce13
  title: 赌徒式炒股——不管赢面都下注
  type: counter-example
  source_chapter: 第3章 3.4 · L546-560
  source_quote: |
    "那些持续输钱的人则会不管赢面大小都下注，盼望着奇迹出现……奇迹出现的次数刚好
    让输钱的人不会死心总想翻本，一赌再赌而一输再输。"
  failure_mode: |
    打听热门消息频繁进出，如同只按马鬃漂亮下注；不愿在局面不利时认输离场，
    靠希望而非概率交易。
  mechanism: |
    梭哈类比：赢家随新牌（新信息）不断重算赔率并敢加注/敢弃牌；输家把自我价值
    绑在单局胜负上，损失厌恶反而导致不肯止损离场（对错误判断的止损≠对股价的止损）。
  warning_signs:
    - 新信息恶化仍"等奇迹"
    - 从不算"这家公司成功的前提还剩几个"
    - 以翻本为目的加仓
  bound_to:
    - "定期重新核查（每张新牌都要重估）"
    - "两分钟独白（先写下成功前提）"
  tags: [counter-example, gambling-mindset, loss-aversion]
  task_ids: [task-09, task-12]

- id: ce14
  title: 好公司、错误价格——蓝筹也会亏一半
  type: counter-example
  source_chapter: 第3章 3.4 · L562
  source_quote: |
    "一些投资者认为，只要买入蓝筹股就不用再关注基本面，结果因为这种盲目草率的做法
    一下子就亏损了近一半的投资资金，而且可能后来用8年也没有涨回原来的价位。"
  failure_mode: |
    把"公司好"当成"股票任何时候都能买"：70年代初数百万美元追高百时美、麦当劳等
    蓝筹，亏损过半且8年不回本。
  mechanism: |
    风险不来自公司类型而来自投资者的方法（买价过高）；好公司在过高估值下，
    需要多年收益增长才能消化股价，期间持有者大概率中途放弃。
  warning_signs:
    - 买入理由只有"这是最好的公司"
    - 不看当前市盈率相对历史/增长率的位置
  bound_to:
    - "P/E估值纪律（绝不买超高P/E）"
    - "股价与收益关系（价格终将回归收益）"
  tags: [counter-example, overpaying, blue-chip]
  task_ids: [task-05]

- id: ce15
  title: 拿两三年内要用的钱入市（寡妇学费案例）
  type: counter-example
  source_chapter: 第4章 4.2 · L612-616
  source_quote: |
    "如果碰上市场像踩了一块香蕉皮一样突然大跌时，这位寡妇的宝贝儿子德克斯特就没钱
    上哈佛而只能去上夜校了……蓝筹股可能也会在三年甚至五年的时间里一直下跌或者一动不动。"
  failure_mode: |
    为两三年内的刚性支出（学费、生活费）买"安全蓝筹"，被迫在低点卖出，
    把临时性下跌变成永久性亏损。
  mechanism: |
    股票10-20年走势可测、两三年内涨跌与掷硬币无异；用钱期限与股票收敛期限错配，
    使投资者成为强制卖家。
  warning_signs:
    - 资金有明确的到期用途
    - 靠固定收入生活或需要本金维持现金流
  bound_to:
    - "入市资格自我测试（先买房、闲钱入市）"
  tags: [counter-example, time-horizon, forced-seller]
  task_ids: [task-12]

- id: ce16
  title: 情绪三态循环与反向情绪数据
  type: counter-example
  source_chapter: 第4章 4.3 · L624-636
  source_quote: |
    "在1987年10月19日大跌之前，80%的投资顾问却预测大牛市行情即将再次来临……投资者
    不断地在担心害怕、洋洋自得、灰心丧气三种情绪之间变化：低点不敢买，上涨追高，
    跌破成本后慌张割肉。"
  failure_mode: |
    下跌后过度担心不敢买、上涨后追高自得不研究、套牢后灰心割肉——在50美元买、
    60美元加仓、40美元全卖的经典亏损剧本。
  mechanism: |
    Investor's Intelligence数据：大众情绪极端乐观时市场见顶（1972/1987）、极端悲观
    时见底（1974/1982）；情绪是惯性指标，做情绪的追随者等于做基本面的背叛者。
  warning_signs:
    - 买入是因为"再不买就晚了"
    - 加仓理由是"看，我说对了吧"
    - 卖出理由是"我想我错了"（只有价格、没有基本面变化）
  bound_to:
    - "买入时机判断（崩盘期机会）"
    - "12种危险说法反驳（18.12涨跌不证明对错）"
  tags: [counter-example, sentiment-cycle, behavioral]
  task_ids: [task-10, task-14]

- id: ce17
  title: 假逆向投资者
  type: counter-example
  source_chapter: 第4章 4.3 · L638
  source_quote: |
    "他们总是等逆向投资已经非常流行以至于成了一个被大家普遍接受的观点时，才会变成
    逆向投资者……真正的逆向投资者会耐心等待市场热情冷却，买入不再被关注的公司。"
  failure_mode: |
    为反而反：热门股涨就卖空所有人都在买的股票；或等"逆向"成为流行词之后才逆向。
  mechanism: |
    把逆向当姿态而非方法：逆向的对象应是市场关注度与估值，而非价格方向本身；
    无基本面支撑的逆向=另一种从众。
  warning_signs:
    - 操作的依据是"大多数人在做相反的事"
    - 说不出这家冷门公司的基本面理由
  bound_to:
    - "13条选股准则（冷门/被抛弃是特征之一，但需基本面配合）"
  tags: [counter-example, contrarian-trap]
  task_ids: [task-03, task-12]

- id: ce18
  title: 为历史重演做准备（玛雅人综合症）
  type: counter-example
  source_chapter: 第5章 5.1 · L670-684
  source_quote: |
    "玛雅人为防洪水搬到树上，第二次灾难却是火灾……我们总是在为最近已经发生的事情
    再次做准备，而不是在为将要发生的事情做准备。"
  failure_mode: |
    1987年崩盘后退出股市的人，为"再次崩盘"做准备，结果被随后的上涨第二次愚弄；
    担心油价涨到100美元的人两年后又在担心跌到5美元。
  mechanism: |
    可得性偏差：最近的灾难权重被放大；而下一次危机的形态永远与上一次不同，
    针对上次的防御对下次基本无效，反而错过机会。
  warning_signs:
    - 调仓理由是"上次就是这么跌的"
    - 宏观叙事一年内180度反转（通胀→衰退、油价高→油价低）
  bound_to:
    - "不预测市场原则"
    - "买入时机判断"
  tags: [counter-example, availability-bias, market-timing]
  task_ids: [task-14, task-12]

- id: ce19
  title: 鸡尾酒会第四阶段——邻居向你荐股
  type: counter-example
  source_chapter: 第5章 5.2 · L686-700
  source_quote: |
    "第四阶段，他们再一次簇拥到我周围，但是这一次是他们告诉我应该买哪些股票，甚至
    是牙医也会向我推荐三五只股票……这是一个股市已经上涨到最高点而将要下跌的准确信号。"
  failure_mode: |
    以宴会情绪四阶段为准择时：在最热闹的第四阶段进场（作者自嘲该理论"可参考不可
    当真、不拿它打赌"，防的是第四阶段入场的冲动）。
  mechanism: |
    情绪传导链（专业人士→懂一点的人→大众→反过来教专业人士）完成时，增量买家
    枯竭；这是情绪指标而非交易系统。
  warning_signs:
    - 完全不懂股票的熟人开始荐股并晒盈利
    - 自己因为"人人都在赚钱"而入场
  bound_to:
    - "不预测市场原则"
    - "整体市盈率风向标（10.3）"
  tags: [counter-example, sentiment-indicator, cocktail-party]
  task_ids: [task-14, task-05]
```

## B. 选股侧反例（第6-9章）

```yaml
- id: ce20
  title: 林奇自认错过——Dreyfus与表6-1清单
  type: counter-example
  source_chapter: 第6章 6.3 · L886-941；表6-1 · L943-986
  source_quote: |
    "1977年Dreyfus为40美分，1986年接近40美元……那么我从这几家基金公司大牛股上赚了
    多少钱呢？一分钱也没有。表6-1所列只是我错过或过早卖出的10倍股中的一小部分
    （公司名从a到m）。"
  failure_mode: |
    坐在信息金矿上（富达内部人最懂基金业繁荣）却一股未买Dreyfus/Franklin/Federated；
    错过的十倍股按字母排满两页。作者以此证明：错过是常态，不能成为追高的借口。
  mechanism: |
    熟悉≠已行动：信息优势不经过"分类+研究+下单"三步就归零；而"错过损失"是幻觉
    （见ce58），为追回错过而买的"下一个"才是真亏损。
  warning_signs:
    - 对身边行业繁荣只有感叹没有研究动作
    - 因懊悔错失而急于买同类替代品
  bound_to:
    - "业余优势利用（优势必须兑换成研究）"
    - "错过心理管理（18.10/18.11）"
  tags: [counter-example, self-admitted, missed-tenbagger]
  task_ids: [task-12, task-10]

- id: ce21
  title: 快速增长型公司过热的破产风险
  type: counter-example
  source_chapter: 第7章 7.3.3 · L1276-1284
  source_quote: |
    "一旦资金短缺的公司遇到十分头痛的大麻烦，通常的结果是按照《破产法》第11章申请
    破产保护……当增长速度放慢时，规模较小的快速增长型公司将会面临倒闭的风险。"
  failure_mode: |
    把"快速增长"标签当成安全标签：头脑过热而财务实力不足的新公司一旦资金链断裂
    直接进破产程序；规模过大者则股票迅速贬值（华尔街不念旧情）。
  mechanism: |
    高增长靠资本开支与复制维持，收入暂缓而债务刚性；第二阶段最安全、第一与第三
    阶段风险最大——不看阶段只看增速的买入会被阶段切换双杀。
  warning_signs:
    - 资产负债表脆弱（高短期负债、薄现金）却讲扩张故事
    - 增长率开始下滑但估值仍按高增长定价
  bound_to:
    - "六类公司分类（快速增长型必须配合生命周期阶段）"
    - "负债结构核查（13.4）"
  tags: [counter-example, growth-stock, bankruptcy-risk]
  task_ids: [task-01, task-06]

- id: ce22
  title: 把周期股当稳定股拿——"压箱底"陷阱
  type: counter-example
  source_chapter: 第7章 7.5 · L1434-1445
  source_quote: |
    "百时美你可以压在箱底20年不管不问，但是对于得克萨斯航空的股票你可不能这样长期
    持有不管不问。对于不够稳定可靠的周期型公司股票在经济衰退期你可千万不能像对
    稳定增长型公司那样放心得不管不问。"
  failure_mode: |
    用错持有策略：周期股按稳定股"买入持有"，衰退期死扛；或把翻倍/持满两年/跌10%
    止损等陈词滥调当普适法则套在所有类型上。
  mechanism: |
    类型决定规则：周期股的收益线是大起大落，"长期持有"会让上一轮的利润在下一轮
    衰退中全数回吐；卖出时机在周期顶（往往市盈率最低、市场最乐观时）。
  warning_signs:
    - 对周期股使用"好公司拿十年"逻辑
    - 以固定涨幅/固定期限决定卖出
  bound_to:
    - "六类公司分类（先分类再定持有策略）"
    - "分类型卖出判据（17.4.3）"
  tags: [counter-example, cyclical-misclassification, hold-discipline]
  task_ids: [task-01, task-02]

- id: ce23
  title: 热门行业的热门股——家庭购物网络（HSN）
  type: counter-example
  source_chapter: 第9章 9.1 · L1874-1923
  source_quote: |
    "在16个月内它的股价从3美元涨到47美元，然后又跌回到3.5美元……这种追涨而高价买入
    热门股的投资风险之大跟轮盘赌简直没什么区别。公司通过借债购买电视台广告，
    资产负债情况在迅速恶化。"
  failure_mode: |
    因社交压力（车上、火车上人人谈论）追买最热门行业最热门股，涨过头后跌得同样快，
    且绝不给你在成本价体面离场的机会。
  mechanism: |
    支撑热门股股价的只有一厢情愿的期望而非基本面；收入/利润/前景撑不起估值时，
    下跌不设缓冲；买入热门行为本身已证明该投资者不会及早卖出。
  warning_signs:
    - 身边所有人都在谈论这只股票
    - 估值方法算不出当前价格（任何估值都"远远超过"）
    - 公司靠举债购买增长（借债买广告/门店）
  bound_to:
    - "避而不买清单（第9章）"
    - "13条选股准则（反着用：热门即是排除项）"
  tags: [counter-example, hot-stock, hsn, social-pressure]
  task_ids: [task-04]

- id: ce24
  title: 高增长行业引来蜂拥竞争（地毯/硬盘驱动器）
  type: counter-example
  source_chapter: 第9章 9.1 · L1925-1933
  source_quote: |
    "地毯分析师说繁荣将永远持续，客户大量买入……与此同时一下子有200家新竞争者加入，
    价格战使每个厂商都很难赚到一分钱利润。专家们说硬盘驱动器行业将以每年52%增长，
    他们说得不错，但随后30-35家公司蜂拥而入，行业再也无利可图。"
  failure_mode: |
    买"行业永远两位数增长"故事：行业增速兑现了，但无专利/利基保护的暴利必然引来
    供给，利润在竞争中被消灭——行业成功与股东回报可以完全脱钩。
  mechanism: |
    模仿是商界最要命的攻击方式；无法用专利或利基保护的商业创意，成功之日就是
    利润被摊薄之时。分析师在增速顶点发布"永远增长"预测。
  warning_signs:
    - 分析师用"行业增速"论证个股
    - 行业新进入者名单快速变长
    - 公司无专利、无运费壁垒、无品牌利基
  bound_to:
    - "13条选股准则之8.1.9（利基）与8.1.8（零增长行业）"
    - "避而不买清单"
  tags: [counter-example, hot-industry, competition-erosion]
  task_ids: [task-03, task-04]

- id: ce25
  title: 石油服务热门——汤姆·布朗公司50美元→1美元
  type: counter-example
  source_chapter: 第9章 9.1 · L1933-1935
  source_quote: |
    "布朗先生说：'你会把汽车和房子都输个精光，只能光着屁股去参加圣诞舞会。'4年后，
    布朗公司的股票真的从50美元跌到了1美元……布朗公司几乎是一个空壳：一堆无用的
    钻井架、可疑的油气田、惊人的债务和惨不忍睹的资产负债表。"
  failure_mode: |
    只因招股书里有"石油"二字就疯狂抢购石油服务股（尽管对石油服务的了解仅限于
    加油站加油）；看多者在50美元重仓，4年后跌到1美元。
  mechanism: |
    概念传染：行业标签替代公司分析；CEO公开羞辱空头形成的舆论压力=情绪高点信号；
    资产负债表（债务+可疑资产）早已给出答案，无人去看。
  warning_signs:
    - 买入依据是行业名词而非公司报表
    - 管理层用嘲讽空头代替回应财务质疑
  bound_to:
    - "避而不买清单"
    - "负债结构核查（13.4）"
  tags: [counter-example, oil-service, concept-stock]
  task_ids: [task-04, task-06]

- id: ce26
  title: 施乐——热门+多元恶化的双重绞杀
  type: counter-example
  source_chapter: 第9章 9.1 · L1937-1941
  source_quote: |
    "1972年施乐股价高达170美元时，分析师断言它将无限期持续增长，随后佳能、IBM、
    柯达进入复印行业……施乐收购不相关企业进行多元化，结果股价下跌了84%。"
  failure_mode: |
    "施乐=复印"的垄断叙事在170美元被当作永恒；竞争摧毁利润后，公司又用不相关的
    多元化自救，雪上加霜。20年行业需求从未下降，厂商却没赚到钱。
  mechanism: |
    技术领先无壁垒续命（无利基保护），竞争者批量复制产品；管理层面对主业压力的
    标准错误动作是买不懂的业务——热门股+多元恶化是常见的连锁反应。
  warning_signs:
    - 把"XX成了代名词"当买入理由（估值已透支）
    - 强劲竞争者进入原核心市场
    - 公司开始收购与主业无关的业务
  bound_to:
    - "避而不买清单（热门+多元恶化两节）"
    - "利基检验"
  tags: [counter-example, xerox, moat-erosion, diworseification]
  task_ids: [task-04]

- id: ce27
  title: 被吹捧成"下一个"的公司
  type: counter-example
  source_chapter: 第9章 9.2 · L1943-1951
  source_quote: |
    "被吹捧成下一个的公司几乎从来都不会真正成为它的楷模……所有被称为'下一个
    Circuit City'的公司（First Family、Good Guys、Highland、Crazy Eddie、Fretters）
    股票市值都比最初下跌了59%～96%。"
  failure_mode: |
    因错过楷模公司而买入"下一个XX"：模仿者气数已尽，且楷模被大量模仿时也快成为
    明日黄花（"下一个IBM"满天飞时IBM真陷入困境）。
  mechanism: |
    "下一个"称号是营销话术而非经营事实；同一成功模式被第N次复制时，先发优势、
    选址、供应链均已不在；追逐者的买入需求恰为原股东提供退出流动性。
  warning_signs:
    - 公司名片/研报核心卖点是"下一个XX"
    - 自己的买入动机是"上次错过了XX"
  bound_to:
    - "避而不买清单（9.2）"
    - "错过心理管理（18.11）"
  tags: [counter-example, next-big-thing, fomo]
  task_ids: [task-04, task-10]

- id: ce28
  title: 多元恶化——Mobil/吉列/通用磨坊的愚蠢收购
  type: counter-example
  source_chapter: 第9章 9.3 · L1953-1979
  source_quote: |
    "收购对象的特点：①价格过于高估；②业务完全超出理解范围。美孚收购Marcor困扰
    好几年、Container Corporation低价卖掉赔钱；吉列把业务扩到数字手表再一笔注销；
    美国工业公司一年进行300次收购。"
  failure_mode: |
    盈利公司不回购不分红，把钱浪费在高价、不懂的收购上；每隔十年在"疯狂收购"
    与"低价剥离"之间轮回，财富从大公司股东转移给被收购的小公司股东。
  mechanism: |
    管理层激励偏向"刺激的收购"而非"无想象力的回购"；协同效应多数是幻觉
    （吉列收Foamy刮胡泡有协同、收化妆品没有）；判断标准=是否懂、是否相关。
  warning_signs:
    - 公司宣布收购与主业无关、且出价高昂的业务
    - 现金充裕却长期不回购不提分红
    - 管理层谈"技术前沿"收购（17.4.1卖出信号）
  bound_to:
    - "避而不买清单（9.3）"
    - "13条选股准则之8.1.13（回购是正面特征）"
    - "缓慢增长型卖出信号（17.4.1）"
  tags: [counter-example, diworseification, m&a]
  task_ids: [task-04, task-02]

- id: ce29
  title: Genesco——150次收购走向破产（对照Melville）
  type: counter-example
  source_chapter: 第9章 9.3 · L1983-2010
  source_quote: |
    "1956～1973年的17年间Genesco进行了150次收购，账面看起来非常强大，基本面却已
    恶化得非常严重……1974年以后Genesco的股票再也没能涨回来；Melville则上涨了
    30倍。"
  failure_mode: |
    同为制鞋商，Genesco疯狂收购不相关业务（Bonwit Teller、Tiffany、证券咨询……）
    破收；Melville先经营好上一次收购再买下一次，多元优化。销售额做大、股票归零。
  mechanism: |
    收购成功与否不在次数而在协同与管理能力；账面销售额增长掩盖利润率恶化，
    熊市（1973-74）成为照妖镜：收益稳的反弹创新高，恶化的永不再涨回。
  warning_signs:
    - 收购频率高且跨行业
    - 收益不随销售额增长（协同失效）
  bound_to:
    - "避而不买清单（9.3）"
    - "收益核查（股价长期跟随收益）"
  tags: [counter-example, diworseification, genesco]
  task_ids: [task-04]

- id: ce30
  title: 小声耳语的股票——KMS工业与失败清单
  type: counter-example
  source_chapter: 第9章 9.4 · L2020-2034
  source_quote: |
    "KMS公司1980年做'非晶体硅光电材料'，1984年'视频多路复用器'，1985年'化学驱动
    球体内爆法'，1986年'惯性约束聚变'……股价从40美元跌到2.5美元，靠8股缩1股才没
    跌到几分钱。以下是我惨遭失败的案例：国家卫生保健中心从14美元跌到50美分……"
  failure_mode: |
    讲爆炸性故事、解决全国大难题（石油短缺/吸毒/艾滋病）的无收益公司，故事催眠
    听者；林奇买的每一只小声耳语股票都让他赔钱。共同点：吹牛吹破天、没有实质内容。
  mechanism: |
    无收益→无市盈率可查，传统估值工具全部失效，只剩期望定价；故事的情绪感染力
    （"咝咝声"）替代了牛排；等公司有收益记录再买仍可获10倍回报，早买无奖。
  warning_signs:
    - 推荐人压低声音说"大黑马"
    - 公司业务描述恰好解决"全国性大难题"
    - 没有收益、无法计算市盈率
    - 年报关键词逐年更换（追逐概念）
    - 出现缩股（8股缩1股）、跌成仙股、进粉单名单
  bound_to:
    - "避而不买清单（9.4）"
    - "13条选股准则（反用：有收益、有记录）"
  tags: [counter-example, whisper-stock, story-stock, kms]
  task_ids: [task-04]

- id: ce31
  title: Bioresponse——林奇自认的小声耳语损失
  type: counter-example
  source_chapter: 第9章 9.4 · L2028
  source_quote: |
    "1983年2月我以每股9.25美元的价格购买了Bioresponse（从牛身上提取淋巴液）的股票，
    最高曾上涨到16美元，但现在这家公司已经坠入深渊、无可救药，幸运的是我及早卖出
    只赔了一点儿钱。"
  failure_mode: |
    林奇亲自拜访总部、多家券商跟踪推荐、办公室简朴（好信号）齐备，仍逃不过
    亏损——故事公司的"好信号"无法替代收益记录。
  mechanism: |
    即使尽调到位，无收益公司的不确定性也无法定价；唯一救他的是及时认错卖出的
    纪律（及早卖出只赔一点），而非判断力。
  warning_signs:
    - 用"参观过总部""管理层朴素"替代收益证据
    - 多家券商联合推荐一家无收益公司
  bound_to:
    - "避而不买清单（9.4）"
    - "卖出纪律（错了就早卖）"
  tags: [counter-example, self-admitted, whisper-stock, bioresponse]
  task_ids: [task-04, task-02]

- id: ce32
  title: IPO冲动——"现在不买就来不及了"
  type: counter-example
  source_chapter: 第9章 9.4 · L2038-2042
  source_quote: |
    "投资者的心理压力在于，觉得必须在IPO时买入否则后悔也来不及了，但这种观点很少
    情况下是正确的……这种首次发行的新股4只中有3只长期表现令人失望。"
  failure_mode: |
    被首日暴涨诱惑（基因技术35→89美元；苹果新股上市第一天林奇全部卖掉赚20%）
    冲进新股；新公司上涨空间有限，4只新股3只长期失望。
  mechanism: |
    IPO定价与情绪由承销节奏制造稀缺感；无经营历史=无法核查的极端形态。
    例外方向：从母公司分拆出来的"老公司新上市"（玩具反斗城、Safety-Kleen）
    有历史记录可查，性质完全不同。
  warning_signs:
    - 买入理由是"上市第一天肯定涨"
    - 公司无完整经营周期记录
    - 分不清"全新公司IPO"与"母公司分拆上市"
  bound_to:
    - "避而不买清单（9.4延伸）"
    - "13条选股准则之8.1.4（分拆才是机会）"
  tags: [counter-example, ipo, fomo]
  task_ids: [task-04]

- id: ce33
  title: 过度依赖大客户的供应商（SCI Systems/Tandon）
  type: counter-example
  source_chapter: 第9章 9.5 · L2046-2050
  source_quote: |
    "如果一家公司把25%～50%的商品都卖给了同一个客户，这表明该公司的经营处于十分
    不稳定的状态之中……失去重要客户会带来毁灭性灾难，大客户还能逼迫供应商降价，
    购买这种股票几乎不可能获得很大的投资成功。"
  failure_mode: |
    供应商公司命运系于单一客户的续约意愿（IBM随时可自制零部件或更换供应商）；
    合同取消=瞬间灾难，谈判地位悬殊持续压缩利润率。
  mechanism: |
    收入集中度是隐性杠杆：客户集中度越高，估值应给的折扣越大；
    "主要客户经营放缓"也是各类型卖出清单的通用信号（17.4.5）。
  warning_signs:
    - 年报/招股书中单一客户销售占比≥25%
    - 最大客户自身行业进入下行
  bound_to:
    - "避而不买清单（9.5）"
    - "13项财务指标之产品销售占比（13.1）"
  tags: [counter-example, customer-concentration]
  task_ids: [task-04, task-06]

- id: ce34
  title: 名字花里胡哨的公司（UAL→Allegis）
  type: counter-example
  source_chapter: 第9章 9.6 · L2052-2054
  source_quote: |
    "资质平平的公司如果名字起得花里胡哨却可以吸引投资者买入，并给他们一种错误的
    安全感。只要名字里有'高级''主要''微型'，或有字母x，或是神秘缩写词，就会让
    投资者一见钟情。UAL把名字改成Allegis是为了吸引追赶时髦的投资者。"
  failure_mode: |
    把"名字听起来有技术感/高级感"当质量信号买入；好公司名字乏味让人远离（错失），
    平庸公司名字花哨让人追买（亏损），两个方向的错误同源。
  mechanism: |
    名字是营销变量而非资产；花哨名称与机构关注同时上升，恰是业余者低价买入窗口
    关闭之时（瓶盖瓶塞封口公司若改名CroCorSea，业余者就没机会了）。
  warning_signs:
    - 公司刚改了一个更时髦的名字
    - 名词堆砌技术词汇（micro/x/首字母缩写）
  bound_to:
    - "避而不买清单（9.6）"
    - "13条选股准则之8.1.1（名字枯燥是优点）"
  tags: [counter-example, fancy-name, branding-trap]
  task_ids: [task-04, task-03]

- id: ce35
  title: 缩股、仙股与粉单——归零前的最后形态
  type: counter-example
  source_chapter: 第9章 9.4 · L2026、L2032（注释[3] · L2062）
  source_quote: |
    "KMS只是因为进行了一次8股缩为1股的缩股之后才没让它的股价下跌到只有几分钱的
    悲惨命运。MGF石油的股票成了只有几美分的仙股；美国太阳能之王出现在粉单市场
    公司名单上。"
  failure_mode: |
    故事股的终局链路：高位→缩股化妆→仙股→粉单消失。持有者以"反正只剩几美分"
    心理死守到流动性归零。
  mechanism: |
    缩股不改变公司价值只重置价格坐标，为下一轮稀释续命；进入粉单（无监管报价
    体系）后连价格发现都失去，卖出通道关闭。
  warning_signs:
    - 公司公告缩股/合股
    - 股价长期低于1美元
    - 退至场外/粉单报价
  bound_to:
    - "避而不买清单（9.4）"
    - "3美元低价股谬误（18.4）"
  tags: [counter-example, reverse-split, penny-stock, pink-sheets]
  task_ids: [task-04, task-10]
```

## C. 估值与调研反例（第10-13章）

```yaml
- id: ce36
  title: 绝不买超高市盈率——麦当劳50倍之跌
  type: counter-example
  source_chapter: 第10章 10.2 · L2339-2341
  source_quote: |
    "千万不要买入市盈率特别高的股票……1972年麦当劳运营仍然优秀，但股价被哄抬到
    75美元、市盈率50倍，收益增长无法达到预期，股价从75美元大跌回25美元。股价大跌
    并非公司运营出错，只是75美元实在太过于高估。"
  failure_mode: |
    为伟大公司支付50倍市盈率：公司没变坏，仅"增长不及过分预期"就足以让股价
    跌去2/3——好公司与好股票的分离。
  mechanism: |
    高P/E隐含多年超高增长假设；收益回归常态增长时，估值与盈利双杀；
    "特别重的马鞍是赛马奔跑的障碍"。
  warning_signs:
    - 市盈率远超其历史正常区间
    - 为证明当前P/E合理所需的增长率超过公司能力（见ce38雅芳测算）
  bound_to:
    - "P/E实操纪律（绝不买超高P/E红线）"
    - "P/E vs 增长率口径"
  tags: [counter-example, valuation, mcdonalds, high-pe]
  task_ids: [task-05]

- id: ce37
  title: EDS——500倍市盈率的世纪高估
  type: counter-example
  source_chapter: 第10章 10.2 · L2343-2349；16.2 · L3464
  source_quote: |
    "EDS市盈率竟高达500倍！……随后几年EDS业绩表现都非常优秀，收益以惊人速度增长，
    但1974年股价仍从40美元暴跌到3美元——不是因为经营失误，而是股价被过度高估。"
  failure_mode: |
    即便随后15年盈利增长约20倍、1984年被通用汽车以44美元收购，44美元也只相当于
    其10年前价格——超高价买入者即使"看对公司"也赚不到钱。
  mechanism: |
    超高P/E等于把公司"从此之后直到永远"的业绩都提前支付；当增长兑现时，
    卖方不是公司而是预期本身；价格回归收益的方式可以是通过十年横盘。
  warning_signs:
    - 研报用"市盈率应该更高"来论证买入
    - 无法用任何增长率假设在10年内收回投资
  bound_to:
    - "P/E实操纪律"
    - "收益预测五途径核查（增长计划可证伪）"
  tags: [counter-example, valuation, eds, extreme-pe]
  task_ids: [task-05]

- id: ce38
  title: 雅芳——64倍市盈率与"十亿瓶香水"
  type: counter-example
  source_chapter: 第10章 10.2 · L2351；17.4.4 · L3682
  source_quote: |
    "雅芳要维持64倍市盈率，收入必须超过美国整个钢铁工业、石油工业及加州收入总和，
    而且这只能让高价买入者收回成本而已。事实上雅芳收益不但没有增长反而下降，
    1974年股价跌到18.625美元。"
  failure_mode: |
    大市值公司戴64倍市盈率：市场份额天花板使所需增长在算术上不可能；
    "美国每两个家庭主妇中就有一个得当雅芳销售代表"。
  mechanism: |
    市值越大，翻倍所需的增量收入越接近宏观总量；用"市占率×人口"做上限测算
    是戳破大公司高估值的试金石。
  warning_signs:
    - 大市值公司讲持续高增长故事
    - 渗透率已高却按低渗透率定价
    - 增长靠提价而非新市场（17.4.2信号）
  bound_to:
    - "P/E实操纪律"
    - "快速增长型卖出判据（17.4.4）"
  tags: [counter-example, valuation, avon, saturation]
  task_ids: [task-05, task-02]

- id: ce39
  title: 宝丽来——SX-70预期泡沫与50倍市盈率
  type: counter-example
  source_chapter: 第10章 10.2 · L2353-2355
  source_quote: |
    "投资者预期SX-70相机会创造惊人收益增长，但相机和胶卷定价太高且操作有问题，
    消费者很快失去兴趣。即使SX-70大获成功，宝丽来也必须至少向每个美国家庭出售
    4台相机，才能支撑50倍的市盈率。"
  failure_mode: |
    单一爆款产品预期支撑50倍P/E：产品本身不及预期+所需销量在算术上不可能，
    18个月内股价大跌89%（143→14.125美元），32年辉煌历史不构成保护。
  mechanism: |
    "每家几台"式测算（同雅芳）暴露增长假设荒谬；成名蓝筹+新产品故事=
    预期最大化组合，预期落空时没有估值缓冲。
  warning_signs:
    - 估值锚定在尚未上市/刚上市的新产品上
    - 所需渗透率测算超过常识上限
  bound_to:
    - "P/E实操纪律"
    - "产品畅销信号评估（0.6/7.1）"
  tags: [counter-example, valuation, polaroid, product-expectation]
  task_ids: [task-05, task-13]

- id: ce40
  title: 百时美30倍P/E配15%增长——为稳定付双倍价
  type: counter-example
  source_chapter: 第16章 16.2 · L3462
  source_quote: |
    "投资者过于追捧百时美，市盈率高达30倍，但收益增长率实际只有15%……以收益增长率
    两倍的市盈率买入，就是在冒不必要的巨大风险追逐不太可能实现的盈利。后来连续
    10年收益增长才使股价达到比较合理的市盈率水平。"
  failure_mode: |
    买入"最安全"的稳定增长型蓝筹却支付增长率两倍的P/E，结果是十年消化估值、
    持有无回报——安全公司在错误价格上并不安全。
  mechanism: |
    P/E≈增长率是定价合理线，两倍即透支一倍增长；稳定增长型本就是"低风险中回报"，
    透支后变成"无风险补偿的等待"。
  warning_signs:
    - P/E与增长率之比接近或超过2
    - 稳定蓝筹成为市场宠儿（人人称赞时）
  bound_to:
    - "P/E vs 增长率口径"
    - "稳定增长型卖出判据（17.4.2：P/E超历史正常水平即卖）"
  tags: [counter-example, valuation, Bristol-Myers, peg]
  task_ids: [task-05, task-02]

- id: ce41
  title: 整体市场市盈率风向标失察（8倍→16倍）
  type: counter-example
  source_chapter: 第10章 10.3 · L2357-2365
  source_quote: |
    "1982-1987年整体市盈率从8倍升到16倍，投资者为同等的收益支付了1982年两倍的价格，
    这是大多数股票已经过于高估的警告信号……1971年整体市场平均市盈率达到20倍最高点，
    随后1973-74年股市经历自30年代以来最剧烈的暴跌。"
  failure_mode: |
    只看个股不看整体水位：个股估值合理但整体P/E翻倍时，系统性修正会把
    合理估值的股票一起打下去。
  mechanism: |
    整体P/E由利率与情绪共同驱动；水位翻倍后任何边际利空都能触发全市场
    估值回归——个股防御不了系统性P/E收缩。
  warning_signs:
    - 指数整体P/E处于历史区间上沿
    - 缓慢增长型公司享有快速增长型的P/E（错配普遍化）
  bound_to:
    - "整体市场P/E风向标"
    - "买入时机判断（高水位期控制新增仓位）"
  tags: [counter-example, market-valuation, systemic-risk]
  task_ids: [task-05, task-14]

- id: ce42
  title: 低市盈率不等于便宜
  type: counter-example
  source_chapter: 第10章 10.1 · L2327
  source_quote: |
    "有些专门寻找便宜货的投资者认为不管什么股票只要市盈率低就应该买下来，但这种
    策略对我来说没有什么意义……对于陶氏化学明显偏低的市盈率，对于沃尔玛而言
    并非如此。"
  failure_mode: |
    跨类型、跨行业直接比较P/E绝对值，见"个位数P/E"就捡：周期股在利润顶部
    P/E最低恰是卖出区（见ce63），低P/E可能内含利润均值回归的陷阱。
  mechanism: |
    P/E的分母（收益）性质不同：周期股收益在峰值、困境股收益在谷底，同一倍数
    含义相反；必须先分类再解释P/E。
  warning_signs:
    - 筛选条件只有"P/E低于X"
    - 未确认公司类型就解释P/E高低
  bound_to:
    - "P/E实操纪律（先分类后估值）"
    - "六类公司分类"
  tags: [counter-example, valuation, pe-screen-trap]
  task_ids: [task-05, task-01]

- id: ce43
  title: Bildner's——忘记问"经营模式能否复制"
  type: counter-example
  source_chapter: 第11章 11.2 · L2453-2475
  source_quote: |
    "你几乎询问了所有问题，却忘了询问最重要的问题——它的经营策略在其他地方进行
    复制也能同样获得成功吗？……Bildner's股价最后跌到0.125美元，我分批卖出，亏损
    50%～95%。在公司经营能力得到证明之前，千万不要提前贸然买入。"
  failure_mode: |
    林奇自认的典型错误：对波士顿老店的完美调研（位置、客源、赚钱能力、招股书
    低负债、租赁开店）全部通过，唯独没验证模式跨城市复制能力；波士顿百货新店、
    曼哈顿分店、亚特兰大扩张接连惨败，资本开支超募资，公司滑向破产。
  mechanism: |
    单店成功要素（本地客群、选址、熟客文化）未必可迁移；"下一个Taco Bell"的
    类比本身就是投资者讲给自己听的故事；募集资金烧完前若模式未验证，公司没有
    第二次机会。教训双面：等复制验证再买；确认失败后应"在牌变差之前及早摊牌"。
  warning_signs:
    - 只调研了发源地门店
    - 新店扩张计划激进而管理人才储备不明
    - 新城市首店业绩不佳仍继续扩张
    - 资本开支增速超过募资
  bound_to:
    - "两分钟独白（必须包含复制性提问）"
    - "快速增长型核查（第二阶段才最安全）"
  tags: [counter-example, self-admitted, bildners, replicability]
  task_ids: [task-07, task-01]

- id: ce44
  title: 把内部人士卖出当卖出信号
  type: counter-example
  source_chapter: 第11章 11.1 · L2449-2451；17.2 · L3586
  source_quote: |
    "因为内部人士卖掉一只股票就否定这只股票是一个非常愚蠢的理由"——La Quinta一位
    创始人以市价一半卖出，令林奇几乎放弃这只后来10年涨11倍的股票；皮特里停止买入
    玩具反斗城后林奇在5美元卖出，错过25倍（见ce52）。
  failure_mode: |
    把内部人士卖出/大买家停止买入解读为基本面恶化信号而卖出好股票。
  mechanism: |
    内部人士卖出的常见原因是分散资产（创始人多元化自己的组合），与公司前景
    无关；反向指标真正有信息量的场景是内部人士在买入（8.1.12），卖出的噪音远
    大于信号。
  warning_signs:
    - 卖出理由是"高管在卖/大户不买了"
    - 同期公司经营数据并无恶化
  bound_to:
    - "13条选股准则之8.1.12（内部人士买入是正面信号，反向不成立）"
    - "两分钟独白（重读最初买入理由）"
  tags: [counter-example, insider-selling, signal-misread]
  task_ids: [task-03, task-07]

- id: ce45
  title: 相信投资者关系部门的形容词
  type: counter-example
  source_chapter: 第12章 12.3 · L2565-2583
  source_quote: |
    "软件公司IR：公司日子越难过，工作人员的口气越乐观。你永远听不到服装公司说
    '一般'……投资者没有必要浪费时间揣摩形容词的含意，更简单的对策就是：不要理会
    任何形容词，只管事实和数据。"
  failure_mode: |
    把IR的乐观措辞（"基本可以""难以置信""好得不能再好"）当作经营信息；
    高技术/服装公司的语言通胀使形容词彻底失真。
  mechanism: |
    行业竞争文化决定IR语言风格：越是挣扎的行业越必须乐观（否则对手抢走合同）；
    成熟产业（纺织）则系统性地过度悲观。形容词是营销变量，数据才是信息。
  warning_signs:
    - 通话记录里只有形容词没有数字
    - 只说"好极了"但给不出同店销售/订单/毛利率数据
  bound_to:
    - "信息获取程序（12.2打电话要事实数据）"
  tags: [counter-example, ir-language, information-quality]
  task_ids: [task-08]

- id: ce46
  title: 豪华总部=收益之忧（Uniroyal式办公楼）
  type: counter-example
  source_chapter: 第12章 12.4 · L2589-2597
  source_quote: |
    "Uniroyal总部看起来像一所富丽堂皇的大学预科学校，我想这可不是一个好的迹象，
    我可以肯定公司将要走下坡路……公司高级管理人员把办公室装饰得非常豪华之日，
    就是投资者应该为这家公司的收益开始忧心之时。"
  failure_mode: |
    把气派的总部、精美的古典家具、抛光胡桃木墙当作公司实力信号——方向完全反了。
  mechanism: |
    资本配置偏好暴露管理层优先级：排场开支与股东回报此消彼长；
    对照组：瓶盖瓶塞封口（总裁办公室看得到生产线、油地毡褪色）30年涨280倍。
  warning_signs:
    - 总部/管理层办公室翻新装修
    - 管理层薪酬与期权增速远超利润
  bound_to:
    - "拜访总部程序（简朴=好信号）"
    - "资本配置核查（回购vs排场）"
  tags: [counter-example, corporate-luxury, capital-allocation]
  task_ids: [task-08]

- id: ce47
  title: Tandon/Televideo——"普通人已靠股票暴富"的财富幻觉
  type: counter-example
  source_chapter: 第12章 12.5 · L2603-2609
  source_quote: |
    "Tandon一位普通IR人员持股+期权已值2000万美元……我稍加思考：如果我能从这只股票
    上赚钱，他的财富又要翻倍，这太不可想象了。后来Tandon从35.25美元跌到1.375美元；
    Televideo从40.5美元跌到1美元。"
  failure_mode: |
    高价股+高市盈率+员工普遍持股暴富的组合：一旦"连普通员工都因股票致富"，
    说明股价已透支到荒谬，接盘者是在为内部人的纸面财富买单。
  mechanism: |
    员工期权财富=股价的凸性函数，股价再翻倍则内部财富翻倍而买入者收益有限；
    这种不对称正是估值见顶的体感信号。林奇承认无法科学论证，但两次都灵验。
  warning_signs:
    - 普通员工因持股成为千万富翁
    - 股价已涨数倍+行业竞争激烈（软盘/计算机外设）
  bound_to:
    - "信息获取程序（个人接触中的体感信号）"
    - "P/E纪律"
  tags: [counter-example, wealth-illusion, employee-riches]
  task_ids: [task-08, task-05]

- id: ce48
  title: 只读年报文字、不看报表数字
  type: counter-example
  source_chapter: 第12章 12.7 · L2639-2643
  source_quote: |
    "印在光洁纸面上的文字部分容易理解却往往根本无用，附在后面的数字部分很难理解
    却相当重要……我略过所有文字部分，直接翻到第27页的合并资产负债表（纸张越便宜，
    上面的信息越宝贵）。"
  failure_mode: |
    被年报的封面照片、企业文化长文、赞助展览的故事吸引，跳过资产负债表，
    失去唯一关键的数字信息。
  mechanism: |
    年报文字是公关文本（写给股东看的好话），数字经审计且有法律约束；
    信息价值与印刷成本成反比的自嘲式规律。
  warning_signs:
    - 读年报只读了董事长致辞
    - 说不出公司负债/现金/存货数字
  bound_to:
    - "年报阅读程序（直翻资产负债表）"
    - "13项财务指标提取"
  tags: [counter-example, annual-report, information-priority]
  task_ids: [task-06, task-08]

- id: ce49
  title: GCA vs 应用材料——短期银行负债决定生死
  type: counter-example
  source_chapter: 第13章 13.4 · L2862-2888
  source_quote: |
    "两家公司同样陷入困境：GCA负债1.14亿美元且几乎全部是银行贷款，账上现金只有
    300万美元；应用材料负债1700万、现金3600万。行业复苏后应用材料从8美元涨到
    36美元，GCA宣告破产、以每股10美分被收购——债务负担的不同决定了两家公司
    命运的不同。"
  failure_mode: |
    困境投研只看业务前景不看负债结构：同样迎接行业复苏，短期银行负债的GCA
    撑不到黎明（银行一抽贷即进入破产11章），股东清零。
  mechanism: |
    危机时刻是负债而非其他因素决定存亡：银行贷款可被要求立即偿还（最差），
    长期债券不能（最好）；Micron靠可转换债置换短期贷款才活下来（4→24美元）。
  warning_signs:
    - 负债权益比超80/20（正常为25/75）
    - 负债以短期银行贷款/商业票据为主
    - 现金头寸低于短期负债
  bound_to:
    - "13项财务指标之负债因素（13.4）"
    - "困境反转型投资前提（负债结构核查）"
  tags: [counter-example, debt-structure, gca, distressed]
  task_ids: [task-06, task-01]

- id: ce50
  title: Southmark——高债务公司停发股息
  type: counter-example
  source_chapter: 第13章 13.6 · L2963-2967
  source_quote: |
    "像Southmark这种债务负担严重的公司，永远不可能像几乎没有债务的百时美那样保证
    定期派息——最近它在房地产方面遭受重挫后，股价从11美元直线下跌到3美元，公司
    就暂停派发股息。"
  failure_mode: |
    为股息买高负债公司的股票：地产重挫+停息双杀，股息"安全垫"变成下跌加速器。
  mechanism: |
    股息的可持续性取决于资产负债表而非当前派息率；周期股股息同样不可依赖
    （福特1982年停息、股价跌至4美元以下，25年最低）。买股息要选二三十年
    连续提高股息记录的公司（Kellogg、Ralston Purina）。
  warning_signs:
    - 公司负债沉重却维持高股息
    - 主要业务部门进入下行周期
  bound_to:
    - "13项财务指标之股息（13.5/13.6）"
    - "缓慢增长型选股（股息是核心逻辑，必须验证可持续性）"
  tags: [counter-example, dividend-trap, southmark]
  task_ids: [task-06]

- id: ce51
  title: 联合爱迪生——"绝对安全"公用事业停息崩跌
  type: counter-example
  source_chapter: 第13章 13.5（图13-1）· L2927、L2948-2950；18.8 · L3890-3894
  source_quote: |
    "1974年4月23日联合爱迪生停发股息，股价崩至约2美元（从20多美元），损失80%市值
    ……投资印第安纳公共服务、海湾公用事业这些'稳健'公用事业股票，和投资毫无名气
    的生物遗传公司同样危险，甚至更危险，因为投资者根本没意识到风险的存在。"
  failure_mode: |
    "买入不用操心的公用事业股锁进保险箱等股息"的两代信条在核电事故+监管基数
    问题下崩溃；不设防的持仓跌80%。
  mechanism: |
    公司发展是动态的：核电成本与Rate Base争议使"稳定板块"波动性剧变；
    意识不到的风险比看得见的风险伤害更大（后因现金积累+持续提息而收复——
    恰证明动态核查的必要）。
  warning_signs:
    - 用"这类股票历来稳"替代对当下基本面的核查
    - 行业监管/技术环境发生结构性变化
  bound_to:
    - "定期重新核查（任何股票都不能压箱底）"
    - "12种危险说法之18.8反驳"
  tags: [counter-example, utility-myth, con-edison]
  task_ids: [task-09, task-10]

- id: ce52
  title: 账面价值陷阱——佩恩中央/艾伦伍德/巴菲特织布机
  type: counter-example
  source_chapter: 第13章 13.7 · L2969-2983
  source_quote: |
    "佩恩中央申请破产保护时账面价值还高达每股60多美元；艾伦伍德钢铁账面每股40
    美元，6个月后破产，炼钢设施账面3000万美元实际根本无法使用……巴菲特的织布机
    账面86.6万美元，拍卖只卖了16.3万美元（每台26美元，比拖走的运费还低）。"
  failure_mode: |
    按"股价低于账面价值"捡便宜：账面价值经常与实际价值毫无关系——穿越大山的
    隧道、报废轨道车都按资产入账；产品越接近最终制成品，再次出售的价格越难预测。
  mechanism: |
    账面价值按历史成本入账，清算价值取决于二手市场有无买家；"负债是真实的、
    资产是估计的"——账面4亿资产只卖2亿时，正账面瞬间变负。
  warning_signs:
    - 买入理由主要是"破净"
    - 资产是专用设备、积压布料、在建工程等难以变现项目
    - 负债真实而资产估值可疑
  bound_to:
    - "13项财务指标之账面价值（13.7：必须估算资产真实价值）"
    - "隐蔽资产型判定（资产要'市场尚未定价'才算隐蔽资产）"
  tags: [counter-example, book-value-trap, penn-central, alan-wood]
  task_ids: [task-06]

- id: ce53
  title: Radice——房地产会计制造的账面幻觉（林奇重仓踩雷）
  type: counter-example
  source_chapter: 第13章 13.7 · L2985-2987
  source_quote: |
    "Radice每股账面资产50美元、股价只有10美元，看起来很有吸引力。但账面大部分
    资产是虚幻的——房地产准则允许未售出项目的欠息计入资产。项目没有买主、银行
    收回贷款后，股价跌到75美分……我本来应该知道这种情况的，我管理的麦哲伦基金
    是这家公司的大股东。"
  failure_mode: |
    林奇自认错误：明知账面价值会失真仍重仓佛罗里达土地开发公司，真实价值为
    每股负7美元且被众多投资者估算出来后，股价永远不可能反弹。
  mechanism: |
    房地产会计把资本化利息计入资产，资产随项目滞销而蒸发、负债刚性留存；
    当"真实价值为负"成为共识，没有隐蔽资产并购者来 rescue，估值下限失效。
  warning_signs:
    - 资产大头是"开发中物业"及资本化利息
    - 项目滞销、银行开始收贷
    - 多数机构已算出负真实价值
  bound_to:
    - "13项财务指标之账面价值（13.7）"
    - "隐蔽资产型判定"
  tags: [counter-example, self-admitted, radice, real-estate-accounting]
  task_ids: [task-06]

- id: ce54
  title: 轻率否定身边信号——错过锐步与OshKosh
  type: counter-example
  source_chapter: 第12章 12.6 · L2635
  source_quote: |
    "为什么孩子们一直穿OshKosh的漂亮童装，我却没有买它的股票呢？怎么能够想象
    我竟然会仅仅因为邻居抱怨一双运动鞋弄伤了脚，就说服自己不投资锐步，
    错过一只上涨5倍的大牛股？"
  failure_mode: |
    身边信息用反了：孩子常年穿OshKosh（强信号）视而不见；邻居一句"锐步磨脚"
    （弱信号）就否定整家公司——样本量为一的 anecdotes 覆盖了长期消费事实。
  mechanism: |
    负面轶事的可得性压倒统计性事实；正确做法是把轶事当作启动研究的线索
    （查销量、查投诉率、查同店增长），而不是当作结论。
  warning_signs:
    - 用单次体验/单个熟人评价否决一家公司
    - 对反复出现的消费行为（年年买）毫无反应
  bound_to:
    - "业余优势利用（信号要过研究关，双向都成立）"
    - "实地调查程序"
  tags: [counter-example, self-admitted, anecdote-bias, reebok]
  task_ids: [task-12, task-13]
```

## D. 持有、复查与卖出反例（第14-17章）

```yaml
- id: ce55
  title: Sensormatic——市场饱和后42.5→5.625美元
  type: counter-example
  source_chapter: 第14章 · L3198-3204
  source_quote: |
    "Sensormatic的防窃系统从一个商店扩张到另一个商店时，股票从2美元涨到40美元，
    但市场最终饱和，再也找不到新客户……股价从1983年的42.5美元跌至1984年的5.625
    美元。"
  failure_mode: |
    把第二阶段的复制增长外推到永远：存量客户装完即增长终结，找不到新方法时
    股价与市盈率双杀。
  mechanism: |
    快速增长三阶段模型：第一阶段风险最大、第二阶段最安全最赚钱、第三阶段
    （饱和期）最易出问题；复查必须持续回答"还能往哪里扩张"（温蒂汉堡只能抢
    麦当劳顾客；Anheuser-Busch已占40%啤酒市场）。
  warning_signs:
    - 可渗透门店/客户数接近上限（The Limited 700家最好购物中心已开670家）
    - 开始靠收购而非内生开店维持增长
    - 增长计划从"开新店"变成"提价/增效"
  bound_to:
    - "定期重新核查（阶段切换识别）"
    - "快速增长型卖出判据（17.4.4）"
  tags: [counter-example, saturation, sensormatic, growth-stage]
  task_ids: [task-09, task-02]

- id: ce56
  title: 得州航空双重错误——自满不核查+没换到Delta
  type: counter-example
  source_chapter: 第14章 · L3218-3232
  source_quote: |
    "我从十分担心变成了非常得意的自我满足……在得州航空基本面已经完全土崩瓦解的
    时候，我还沉醉于公司最近业务好转的消息，对报纸每天刊登的行李丢失、航班混乱、
    员工不满等警告视而不见。我的错误是1987年夏天没有及时抛出；另一个错误是没有
    大量增持竞争对手Delta。"
  failure_mode: |
    林奇自认的双重错误：①盈利后（1983年12美元→1987年51.5美元）由警惕变自满，
    1987年2月还在48.25美元追加买入，无视负面新闻与劳资分歧，最终17-18美元割肉；
    ②本可用同一基本面分析抓住东方航空的最大受益者Delta（35→55美元）却只建了
    轻仓。
  mechanism: |
    成功经验制造松懈：沉醉于"每股收益15美元的预期"概念（收购失败航空+削减成本
    =利润自然来的剧本），忘了核查裁员计划根本未执行、劳动合同未到期；
    航空餐饮业的信誉脆弱性（几个晚上就能毁掉50年美誉）。竞争对手分析是同一
    信息的免费期权。
  warning_signs:
    - 对持仓公司的负面报道产生"免疫"
    - 买入理由变成"故事概念"而非已兑现的数据
    - 看好一家困境公司却没检查谁抢走它的客户
  bound_to:
    - "定期重新核查（每隔几个月+新情况触发）"
    - "分类型卖出判据（困境反转恶化即卖）"
    - "竞争对手询问技巧（11.1）"
  tags: [counter-example, self-admitted, texas-air, complacency]
  task_ids: [task-09, task-02]

- id: ce57
  title: 过高的收益预期（25%-30%）
  type: counter-example
  source_chapter: 第16章 · L3406-3410
  source_quote: |
    "过高的预期收益率错在哪里呢？……当股票表现达不到预期时，你会因希望落空而
    严重受挫，焦躁不安的心情会使你恰恰在最不应该放弃的时刻错误地放弃本来正确的
    投资策略，或者更糟：为追逐镜中花水中月的高收益冒不必要的风险。"
  failure_mode: |
    把个别年份的30%当成应得基准，逼自己在错误时点放弃正确策略或加杠杆冒险。
  mechanism: |
    现实基准：股市长期9-10%，业余者自己选股的合理目标12-15%（扣成本后）；
    预期每高一分，行动变形的风险大一分。
  warning_signs:
    - 以"去年赚了30%"要求今年
    - 因落后于不切实际的基准而频繁换股/上杠杆
  bound_to:
    - "组合构建（期望收益设定）"
  tags: [counter-example, return-expectation]
  task_ids: [task-11]

- id: ce58
  title: 频繁换手的成本绞杀
  type: counter-example
  source_chapter: 第16章 · L3422-3424
  source_quote: |
    "业余投资者每次买入或卖出仍需花费1%～2%的交易成本。如果每年把组合全部换手
    一次，就得支付约4%的佣金——从一开始就发生了4%的亏损。要扣成本后获得12%～15%，
    必须从所选股票中获得16%～19%的回报。交易越频繁，越难跑赢指数基金。"
  failure_mode: |
    用行动感替代研究：全年换手一次的业余者在起跑线上就落后4%。
  mechanism: |
    佣金+价差是确定性负和扣减；长期持有者的收益率系统性高于短期交易者。
  warning_signs:
    - 年换手率接近或超过100%
    - 交易动机多为价格波动而非基本面变化
  bound_to:
    - "组合纪律（换股不换现金、低频调仓）"
  tags: [counter-example, turnover-cost, friction]
  task_ids: [task-11]

- id: ce59
  title: 为多元化而多元化
  type: counter-example
  source_chapter: 第16章 16.1 · L3436
  source_quote: |
    "只是为了投资组合多元化而分散投资于一些你并不了解的公司股票是毫无益处的，
    对小投资者来说愚蠢的多元化投资所导致的后果非常恐怖、非常可怕。"
  failure_mode: |
    凑数量求心安：买入一篮子不了解的股票，组合波动或许小了，认知优势归零、
    核查能力为零（另：单押一只股票同样不安全——3-10只为宜）。
  mechanism: |
    分散的保护来自"低相关+各自经过研究"，而不是数量本身；包含雅芳、
    Johns-Manville之类烂股票的5个篮子不如Dunkin' Donuts一只结实篮子。
  warning_signs:
    - 持仓数量增加但说不出新买入公司的买入理由
    - 为了"摊薄风险"买入同行竞品
  bound_to:
    - "组合构建（3-10只、类型搭配、质量优先）"
  tags: [counter-example, diworsification-portfolio]
  task_ids: [task-11]

- id: ce60
  title: 拔掉鲜花浇灌野草
  type: counter-example
  source_chapter: 第16章 16.3 · L3472-3474
  source_quote: |
    "一些投资者习惯性地卖出'赢家'——股价上涨的股票，却死抱住'输家'——股价下跌的
    股票，这种投资策略如同拔掉鲜花却浇灌野草一样愚蠢透顶……二者都把当前股票价格
    变化看做公司基本价值变化的指示器。"
  failure_mode: |
    按浮盈浮亏调仓：赚一点就"见好就收"卖掉好公司，亏的反而"等回本"拿住不放；
    或反向死扛赢家——两个方向错误同源：用价格代替基本面判断。
  mechanism: |
    价格是每天报价的情绪总和，与公司前景的信息含量极低（Taco Bell 1972年股价
    表现糟糕但经营非常成功）；正确操作=卖出基本面恶化且股价上涨的，
    增持基本面好转且股价下跌的。
  warning_signs:
    - 卖出理由是"已经赚了30%了"
    - 持有理由是"已经亏了不忍心卖"
    - 调仓决策里没有出现任何基本面变量
  bound_to:
    - "组合纪律（价格vs基本面双向校验）"
    - "分类型卖出判据"
  tags: [counter-example, behavioral, flowers-weeds]
  task_ids: [task-11, task-02]

- id: ce61
  title: 10%止损指令——把账面亏损变成现实亏损
  type: counter-example
  source_chapter: 第16章 16.3 · L3486-3490
  source_quote: |
    "止损指令根本无法保护投资者避免发生亏损，只不过是使投资者把当前的账面亏损
    变成一个已经发生了的现实亏损。如果你在Taco Bell设置了止损指令，确实能把亏损
    限制在10%以内，却会因此错过上涨10倍的投资机会。设置10%止损，事实上是承认
    自己未来将以低于内在价值的价格卖出股票。"
  failure_mode: |
    用机械止损替代基本面跟踪：股价正常波动率就达50%，10%止损几乎必然被扫掉，
    反复"止损-反弹-追回"循环失血。
  mechanism: |
    止损把决策外包给价格噪声；正确替代= "下跌25%追加买入"的信念+基本面恶化
    才卖出的判据（前提是当初买对了）。
  warning_signs:
    - 每笔单都挂止损单求安心
    - 卖出后同一只股票反复买回
  bound_to:
    - "组合纪律（不设价格止损，改设基本面止损）"
    - "分类型卖出判据"
  tags: [counter-example, stop-loss, price-noise]
  task_ids: [task-11, task-02]

- id: ce62
  title: 过早卖出华纳——一句"过度上涨"的咒语
  type: counter-example
  source_chapter: 第17章 17.2 · L3570-3578
  source_quote: |
    "技术分析师不假思索地回答：'过度上涨。'……华纳从26美元涨到32、38美元，我
    莫名其妙开始大量卖出。后来华纳一路涨到50、60、70美元，最后超过180美元。
    投资建议的最大麻烦是：无论好坏，它都会深深印入你的脑海。"
  failure_mode: |
    林奇自认错误：基本面重查无恙，却被一句随口的"过度上涨"操纵，在38美元清仓
    一只后来涨到180美元以上的股票；连Atari巨亏使其暴跌60%后（76美元）仍是他
    卖价的两倍。
  mechanism: |
    煽动效应的个人信息版：无法证伪的模糊判断（"涨多了"）在焦虑时被大脑反复
    回放；防御=重新审视最初买入理由是否变化，而非价格位置。
  warning_signs:
    - 卖出时引用的是别人的口头判断
    - 基本面复核没有变化但"就是不安心"
  bound_to:
    - "持有纪律（重读买入理由）"
    - "快速增长型卖出判据（按17.4.4信号，不按涨幅）"
  tags: [counter-example, self-admitted, warner, premature-selling, drumbeat]
  task_ids: [task-02, task-09]

- id: ce63
  title: 过早卖出玩具反斗城——1美元买5美元卖，错过25倍
  type: counter-example
  source_chapter: 第17章 17.2 · L3580-3582
  source_quote: |
    "皮特里在5美元时停止买入，我就在这个价位抛出……我在1美元买入、5美元卖出，
    获得5倍回报，怎么还能抱怨呢？但你发现合适的股票并以合理价格买入、所有证据
    表明它将越涨越高时抛出，简直是耻辱。个人投资者一生只有1～2次机会抓住25倍的
    大牛股。"
  failure_mode: |
    把"大买家停止买入"当基本面信号卖出；用"见好就收""一鸟在手"的格言合理化
    错误，5倍收益的心理账户掩盖了25倍的机会成本。
  mechanism: |
    好公司+合理价格+证据持续向好时，利润兑现的确定性低于继续持有的期望值；
    快速增长型公司的正确卖点是其成长逻辑破坏时（同店下滑、扩张停滞），
    而非某个整数倍数。
  warning_signs:
    - 卖出理由是"已经N倍了"
    - 把别人的买卖行为当作公司的基本面信息
  bound_to:
    - "快速增长型卖出判据"
    - "13条准则之8.1.10（重复购买型生意的长持价值）"
  tags: [counter-example, self-admitted, toys-r-us, premature-selling]
  task_ids: [task-02]

- id: ce64
  title: Flowers/Lance——为等并购消息而买卖
  type: counter-example
  source_chapter: 第17章 17.2 · L3584；16.1 · L3444
  source_quote: |
    "有人告诉我这两家公司是被收购兼并的对象，我一直等着它们被并购，最终等得
    不耐烦就卖出了……我基于并购预期买入的股票没有一只后来真的被并购；因为
    基本面良好而持有的公司却往往被并购。"
  failure_mode: |
    把持有逻辑寄托在并购传言上：消息不兑现就失去耐心卖出，卖在起涨前；
    并购恰恰降临在按基本面持有的人头上。
  mechanism: |
    并购时机不可预测，事件驱动策略使持有理由脱离公司价值；
    传言本身（小道消息）就是9.4避买清单的排除项。
  warning_signs:
    - 买入/持有理由包含"据说要被收购"
    - 复查时只盯并购新闻不看经营数据
  bound_to:
    - "两分钟独白（理由必须基于公司自身）"
    - "避而不买清单（小道消息）"
  tags: [counter-example, self-admitted, merger-play, rumor]
  task_ids: [task-07, task-04]

- id: ce65
  title: 煽动效应——宏观噪音与经纪人换股话术
  type: counter-example
  source_chapter: 第17章 17.3 · L3590-3608
  source_quote: |
    "'恭喜你赚钱了，别太贪心……'经纪人劝你卖出Toggle Switch买入Kinder-Mind，
    结果前者继续上涨、后者破产……基于'M1正在提高'就卖出股票，甚至你根本不清楚
    M1是什么，还有比这更愚蠢的理由吗？"
  failure_mode: |
    被重复播放的宏观叙事（M1、准备金率、油价、美元、赤字）和"落袋为安"话术
    操纵，卖出研究过的好股票、买入没研究的替代品——经纪人拿双份佣金。
  mechanism: |
    不祥预兆重复N遍即成"事实"（可得性重复效应）；宏观变量与个股收益的传导
    既弱又不可验证；情绪植入后会在下一次下跌时自动触发卖出。
  warning_signs:
    - 卖出理由是最近反复听到的宏观词
    - 自己无法解释该宏观变量的含义
    - 经纪人建议"卖A买B"式换股
  bound_to:
    - "持有纪律（卖出只对接公司基本面与少数明确传导的事件）"
  tags: [counter-example, drumbeat-effect, macro-noise, broker-conflict]
  task_ids: [task-02, task-09]

- id: ce66
  title: 周期股顶部的低市盈率陷阱（通用动力）
  type: counter-example
  source_chapter: 第17章 17.4.3 · L3650-3658
  source_quote: |
    "通用动力曾一度实现盈利增长而股价却大跌50%，这是远见者提前卖出以避免盈利
    下跌时的抛售浪潮……卖出周期型股票的最佳时机是扩张周期结束时，另一个时机是
    当事情开始变得糟糕时：成本增长、工厂满负荷、公司投资增加产能。"
  failure_mode: |
    用成长股逻辑看周期股的P/E：周期顶利润最高→P/E最低→看起来"便宜"，
    实为卖点；盈利还在增长时股价已开始下跌，投资者误以为是黄金坑。
  mechanism: |
    周期股P/E与安全边际负相关（与成长股相反）；先行指标：存货增加且无法消化、
    大宗商品价格先于收益数月下跌、期货价格低于现货、新竞争者降价、
    双倍预算建豪华新厂。
  warning_signs:
    - 周期股P/E处于历史低位而盈利处于历史高位
    - 停车场堆满存货
    - 商品价格跌而股价还没跌
  bound_to:
    - "P/E实操纪律（先分类再解释P/E）"
    - "周期型卖出判据（17.4.3）"
  tags: [counter-example, cyclical-pe-trap, general-dynamics]
  task_ids: [task-05, task-02]

- id: ce67
  title: 快速增长股崩溃的双重打击
  type: counter-example
  source_chapter: 第17章 17.4.4 · L3674-3696
  source_quote: |
    "如果快速增长型公司经营陷入崩溃、收益锐减，原来被争相买入哄抬到很高水平的
    市盈率也会大大下降——忠诚死守的股东面临损失巨大的双重打击。"
  failure_mode: |
    高P/E快速增长股崩塌时，收益降+估值降双杀（如宝丽来、雅芳）；
    死守者的损失远大于低估值股票的同等经营挫折。
  mechanism: |
    高估值是对高增长的预付；增长逻辑破坏时预付被追回。卖出信号：同店销售降3%、
    新店业绩令人失望、高管与核心员工出走加盟对手、两周12城路演画大饼、
    30倍P/E配15-20%增长预期。
  warning_signs:
    - 同店/单店销售由升转降
    - 核心团队批量离职
    - 管理层密集路演讲乐观前景
    - P/E与可信增长率之比逼近2
  bound_to:
    - "快速增长型卖出判据"
    - "P/E纪律"
  tags: [counter-example, double-hit, growth-collapse]
  task_ids: [task-02, task-05]

- id: ce68
  title: 困境反转股的持有过期（克莱斯勒48美元）
  type: counter-example
  source_chapter: 第17章 17.4.5 · L3700-3704
  source_quote: |
    "克莱斯勒在2美元、5美元、10美元时都是困境反转型股票，但1987年中期达到48美元
    时就不再是了……通用公共电力（GPU）在4-12美元时是困境反转，核设施重启、其他
    公司分担三哩岛清污成本后，38美元的它是优质公用事业股——将来可能涨到45美元，
    但肯定不会涨到400美元。"
  failure_mode: |
    困境反转成功后仍按"反转逻辑"持有：公司已重新归类（克莱斯勒→周期股、
    GPU→公用事业），期望收益随类型切换而坍缩，继续持有等于用旧地图走新路。
  mechanism: |
    反转行情来自"从破产边缘到正常"的一次性重估，完成后上涨动能切换为
    新类型的常规回报；类型迁移必须触发重新分类与卖出评估。
  warning_signs:
    - 债务已清偿、转机人人皆知、媒体开始庆祝
    - 股价上涨主要靠"故事完成"而非新增长
  bound_to:
    - "六类公司分类（类型动态迁移）"
    - "分类型卖出判据（反转完成后换股）"
  tags: [counter-example, turnaround-expiry, chrysler, gpu]
  task_ids: [task-01, task-02]

- id: ce69
  title: 年底避税抛售与低价股保证金踩踏
  type: counter-example
  source_chapter: 第17章 · L3500
  source_quote: |
    "一旦股价跌破每股6美元，用保证金账户购买的投资者就不能用这些股票作担保，
    不得不卖出低价股；机构也往往不得不卖出以免违反限制。这些卖出导致更多跟风
    卖出，把非常好的股票打压到低得惊人的价位。"
  failure_mode: |
    不明时机结构性抛压：10-12月避税抛售+保证金强制平仓+机构合规抛售三重共振，
    好股票被砸出深坑——对卖出者是灾难，对持币者是机会。
  mechanism: |
    抛售由规则与税制触发、与基本面无关；识别结构性卖压（而非基本面恶化）
    是逆向买入的前提。
  warning_signs:
    - 年底低价股无量阴跌
    - 保证金账户持仓集中在低价股
  bound_to:
    - "买入时机判断（年底避税期机会）"
    - "入市资格（不借钱炒股）"
  tags: [counter-example, tax-selling, margin-call]
  task_ids: [task-14]
```

## E. 12种危险说法（第18章，task-10 核心素材）

```yaml
- id: ce70
  title: 说法1"已经跌这么多了，不可能再跌了"（宝丽来）
  type: counter-example
  source_chapter: 第18章 18.1 · L3748-3754
  source_quote: |
    "宝丽来跌破75美元时，坚信'不可能再跌了'的投资者人数增长到一帮人；跌到50美元
    时每个持有者都在重复这句话……不到一年从143.5美元跌到14.125美元，此时才是真正
    '不可能再跌了'的价位。"
  failure_mode: |
    用跌幅本身论证底部：143→100→90→80→75→50美元每一档都有人接"最后一跌"的飞刀；
    基本面（销售盈利大幅下滑+高估）早已说明问题，自欺说法替代了分析。
  mechanism: |
    锚定效应：买入价/前高价成为"合理价"的心理锚；缺乏"跌到多少才算够"的估值
    标尺（净现金、清算价值），只能靠口号自我安慰。
  warning_signs:
    - 加仓理由是"已经跌了X%"
    - 公司销售与盈利同步下滑而只谈股价
  bound_to:
    - "股价与收益关系（收益下滑则价格中枢下移）"
    - "困境反转买入理由（业务好转+净现金，而非跌得多）"
  tags: [counter-example, dangerous-saying, anchoring, polaroid]
  task_ids: [task-10]

- id: ce71
  title: 林奇自认错误——凯撒工业11美元"绝不破10美元"
  type: counter-example
  source_chapter: 第18章 18.1 · L3756-3764
  source_quote: |
    "凯撒从25美元跌到13美元，跌到11美元时我推荐富达买入500万股……我非常自信地
    认为绝对不会跌破10美元。跌到8美元时我劝母亲买入，认为绝不可能跌破7.5美元，
    幸亏她没听。1973年它从7美元跌到6美元又跌到4美元，在这一价位才真正证明
    不可能再跌了。"
  failure_mode: |
    林奇1971年的亲身教训：凭自信给下跌股划底（10美元/7.5美元），一路错一路加；
    母亲不听劝反而避坑。
  mechanism: |
    后来证明4美元才是质优价廉（清算价值每股40美元、市值仅1亿美元=4架波音747），
    最终反弹到30美元——错在"预测底部"，不是"识别便宜"；正确做法是等
    振荡整理2-3年、基本面信号出现再买。
  warning_signs:
    - 对别人（尤其家人）信誓旦旦"绝不可能跌破X"
    - 以自己的成本/推荐价为支撑位
  bound_to:
    - "危险说法反驳（18.1/18.2）"
    - "困境反转买入纪律"
  tags: [counter-example, self-admitted, kaiser, bottom-calling]
  task_ids: [task-10]

- id: ce72
  title: 说法2"你总能知道什么时候跌到底了"（抓住下落的刀子）
  type: counter-example
  source_chapter: 第18章 18.2 · L3766-3772
  source_quote: |
    "抄底一只下跌股票，就像想抓住一把下跌的刀子……不但抄不到底，可能连老本儿都
    输个精光。更稳妥的办法：等刀落地扎进地里，晃动一阵停止后再捡。即使研究得
    非常清楚也难在最低价买入，通常股价重新上涨前会振荡整理2～3年甚至更长。"
  failure_mode: |
    把"跌得深"当买入理由抢反弹；买在半山腰，资金被套多年错过其他机会。
  mechanism: |
    底部是区域不是点位；替代判据=业务开始好转+资产负债表安全边际
    （每股净现金11美元 vs 股价14美元式的事实）。
  warning_signs:
    - 买入理由只有"跌了很多"没有基本面变化
    - 无法忍受"等右侧2-3年"的时间成本
  bound_to:
    - "困境反转买入判据"
    - "13项财务指标之现金头寸"
  tags: [counter-example, dangerous-saying, catching-knife]
  task_ids: [task-10, task-06]

- id: ce73
  title: 说法3"已经这么高了，怎么可能再涨"（菲利普·莫里斯/斯巴鲁）
  type: counter-example
  source_chapter: 第18章 18.3 · L3774-3786、L3840-3850
  source_quote: |
    "菲利普·莫里斯从0.75美元涨到124.5美元，1000美元变成166000美元外加23000美元
    股息……建议客户'翻番就卖出'的专家应该感到耻辱——按他们的建议永远抓不到
    10倍股。斯巴鲁已涨20倍时我查看基本面仍便宜，买入后又赚7倍。"
  failure_mode: |
    用涨幅本身判断见顶：在2.5美元（已3.3倍）卖出后错过23倍；"涨这么多了不可能
    再涨"让人过早收割十倍股。
  mechanism: |
    股票上涨没有人为武断的上限；只要前景良好、盈利继续增长、基本面未变，
    涨幅不是卖出信号——涨幅与估值（P/E vs 增长率）必须区分。
  warning_signs:
    - 卖出/拒绝买入的唯一理由是"已经涨了N倍"
    - 公司盈利与股息曲线仍在创新高
  bound_to:
    - "分类型卖出判据（17.4，按信号不按涨幅）"
    - "P/E vs 增长率（用估值而非涨幅判断贵）"
  tags: [counter-example, dangerous-saying, philip-morris, subaru]
  task_ids: [task-10, task-02]

- id: ce74
  title: 说法4"只有3美元，我能亏多少呢"
  type: counter-example
  source_chapter: 第18章 18.4 · L3852-3864
  source_quote: |
    "无论股价是50美元还是1美元，跌到零都是亏光100%……以50美元买入亏99%的人，
    和以3美元买入亏83%的人，不过是五十步笑百步。猜猜空头在8美元或6美元建仓后
    把股票卖给了谁？正是那些念叨'我能亏多少呢'捡便宜货的不幸投资者。"
  failure_mode: |
    认为低价=低风险、按"每股亏损额"而非"亏损百分比"思考；恰好在崩塌中段
    接下空头的筹码（与ce35缩股/仙股链路衔接）。
  mechanism: |
    最大亏损率对高低价股同为100%；低价股常是基本面更差+缩股化装的结果；
    正确标尺是公司价值与股价之差，不是每股名义价格。
  warning_signs:
    - 用"最多也就亏3美元"安慰自己
    - 因"整股便宜"满仓一只低价股
  bound_to:
    - "危险说法反驳（18.4）"
    - "避而不买清单（小声耳语/低价故事股）"
  tags: [counter-example, dangerous-saying, penny-psychology]
  task_ids: [task-10]

- id: ce75
  title: 说法5"最终股价会涨回来的"（RCA/Johns-Manville）
  type: counter-example
  source_chapter: 第18章 18.5 · L3866-3872
  source_quote: |
    "果真如此的话，西哥特人、成吉思汗的大军最终都应该杀回来了。RCA过去65年股价
    仍然没有涨回来；Johns-Manville面临石棉诉讼，东山再起遥遥无期；保健组织、
    软盘、电子表、移动房屋这些行业的股票至今没有涨回来。"
  failure_mode: |
    把"均值回归"当物理定律套在行业衰落+股本稀释（增发数亿新股摊薄每股收益）
    的股票上，用"拿回来"的执念替代重新估值。
  mechanism: |
    有些下跌是永久性资本毁损（行业淘汰、诉讼、破产、稀释），不存在回归的
    引力；上百家破产公司从未回来。
  warning_signs:
    - 持有理由是"总会回来的"
    - 公司在增发新股/行业被替代技术淘汰
  bound_to:
    - "危险说法反驳（18.5）"
    - "定期重新核查（买入理由已死者重估）"
  tags: [counter-example, dangerous-saying, rca, mean-reversion-myth]
  task_ids: [task-10, task-09]

- id: ce76
  title: 说法6"黎明前总是最黑暗的"（石油服务/货车运输）
  type: counter-example
  source_chapter: 第18章 18.6 · L3874-3880
  source_quote: |
    "1981年美国作业钻井4520口，1984年只剩2200口，许多人此时买入石油服务股相信
    最糟糕已过去；两年后只剩686口。货车总数从1979年95650辆跌到1981年44800辆的
    17年低点，1983年更只剩5700辆——下跌90%的重创。有时在最后变得一片漆黑之前
    也总是最黑暗的。"
  failure_mode: |
    行业下滑中途按"坏到头了"抄底：数据腰斩后仍能再腰斩两次；
    把周期底部误判为周期终点（与ce25同源）。
  mechanism: |
    "已经这么糟"是心理判断不是数据判断；供给出清需要时间与产能退出信号，
    行业数据（钻井数、车队数）连续下滑本身不是反转证据。
  warning_signs:
    - 行业核心运营数据连续多年下滑
    - 买入逻辑依赖"不能再糟了"而非产能出清/需求回升证据
  bound_to:
    - "危险说法反驳（18.6）"
    - "周期型投资判据"
  tags: [counter-example, dangerous-saying, oil-service, false-bottom]
  task_ids: [task-10]

- id: ce77
  title: 说法7"等反弹到10美元我再卖"
  type: counter-example
  source_chapter: 第18章 18.7 · L3882-3886
  source_quote: |
    "从来没有一只严重套牢的股票会如你所愿反弹到你设定的心理价位……这只股票在
    9.75美元以下振荡几年后跌到4美元，最终跌到1美元面值，整个过程可能持续十年。
    每当我陷入这种心理误区，都会提醒自己：除非我对公司有足够信心、愿意在下跌中
    追加买入，否则就应该立刻卖出。"
  failure_mode: |
    把卖出决策挂在一个任意整数上：为等反弹错过所有体面离场窗口，
    忍受十年心理折磨后以更低价格了结。
  mechanism: |
    整数锚（回本价/成本价）无信息含量；唯一有效判据是"敢不敢越跌越买"——
    不敢=对基本面没信心=现在就该卖。
  warning_signs:
    - 持有计划里出现"等回到X美元"
    - 不愿回答"如果今天没有持仓，会不会按现价买入"
  bound_to:
    - "危险说法反驳（18.7）"
    - "分类型卖出判据"
  tags: [counter-example, dangerous-saying, breakeven-anchor]
  task_ids: [task-10, task-02]

- id: ce78
  title: 说法8"保守型股票不会波动太大"
  type: counter-example
  source_chapter: 第18章 18.8 · L3888-3896
  source_quote: |
    "买入根本不用操心的公用事业股票锁进保险箱等股息——由于核事故和收益率基数
    问题，联合爱迪生这样的稳健公用事业股也损失了80%市值……投资这类'稳健'公用
    事业和投资毫无名气的生物遗传公司同样危险，甚至更危险，因为投资者根本没
    意识到风险的存在。"
  failure_mode: |
    "公用事业=绝对安全"的代际信条导致零监控持仓；波动性结构变化（核电、
    储贷、电脑行业化）把"稳定板块"变成高波动板块。
  mechanism: |
    风险来自"没意识到的风险"：不设防的仓位在行业规则改变时无预案；
    事后联合爱迪生不仅收复且创新高——双向证明"锁箱底"策略错误。
  warning_signs:
    - 持仓多年未做过任何复查
    - 行业出现监管/技术结构性变化信号
  bound_to:
    - "危险说法反驳（18.8）"
    - "定期重新核查（所有类型）"
  tags: [counter-example, dangerous-saying, utility-myth, set-and-forget]
  task_ids: [task-10, task-09]

- id: ce79
  title: 说法9"等了这么久，不可能上涨了"（默克）
  type: counter-example
  source_chapter: 第18章 18.9 · L3898-3959
  source_quote: |
    "默克1972-1981年股价一动不动，盈利却年均增长14%，随后5年上涨4倍……American
    Greeting 8年死气沉沉、Lukens 14年不动、Harcourt Brace 12年不动——大多数情况
    我赚钱都是在持有一动不动的股票三四年之后。'一块石头的心电图'是下一波大涨
    的强烈暗示。"
  failure_mode: |
    因"等太久"失去耐心卖出：横盘期恰是收益积累期，卖出后第二天上涨
    （"不卖不涨，一卖就涨"）；把价格停滞误读为公司停滞。
  mechanism: |
    价格与收益的背离终将收敛（图18-2）：横盘中收益线上行=弹簧压缩；
    时间成本焦虑使投资者在最不该放弃时放弃。
  warning_signs:
    - 卖出理由是"拿了三年都没动静"
    - 公司盈利、股息仍在稳步增长
  bound_to:
    - "危险说法反驳（18.9）"
    - "股价与收益背离信号"
  tags: [counter-example, dangerous-saying, merck, patience, flat-stock]
  task_ids: [task-10, task-05]

- id: ce80
  title: 说法10"看看我损失了多少，我竟然没买这只大牛股"
  type: counter-example
  source_chapter: 第18章 18.10 · L3961-3969
  source_quote: |
    "打开钱包看一下银行对账单：你的钱一分没少，只是你回头一看才发现'错失'了
    财富……认为别人赚的钱就是自己赔的钱并非有益态度，只会让人完全疯狂。最糟糕
    的是导致人们为了追最高回报而盲目购买本不该买的股票，把心理上的'亏损'变成
    真金白银的亏损。"
  failure_mode: |
    把未实现的机会成本记作真实损失，在懊悔驱动下追买热门（正是第四阶段入场、
    "下一个XX"的心理燃料——与ce04、ce27连锁）。
  mechanism: |
    反事实账户错觉：知道的股票越多"损失"越大（数十亿甚至万亿）；
    情绪账户无法平仓，唯一出口是冲动交易。
  warning_signs:
    - 反复计算"如果当年买了现在值多少"
    - 因错过A而立即买入同类的B
  bound_to:
    - "危险说法反驳（18.10）"
    - "错过心理管理"
  tags: [counter-example, dangerous-saying, counterfactual-loss, fomo]
  task_ids: [task-10]

- id: ce81
  title: 说法11"错过了这只，我得抓住下一只"（错上加错）
  type: counter-example
  source_chapter: 第18章 18.11 · L3971-3977
  source_quote: |
    "错过玩具反斗城后买入'下一个玩具反斗城'Greenman Brothers，其股价持续下跌——
    第一个错误（错过）不亏一分钱，为弥补它犯下的下一个错误却让你付出真金白银……
    家得宝涨25倍而'下一个家得宝'Scotty只涨25%-30%；错过皮埃蒙特而买人民航空，
    都是错上加错。"
  failure_mode: |
    用"下一个XX"补偿错失感：第一个错误零成本，第二个错误真实扣钱；
    多数情况下，高价买原版好于低价买模仿者。
  mechanism: |
    楷模的成功由时机、位置、执行力构成，称号复制不了其中任何一项；
    追逐者的需求推高模仿者估值，进一步压低回报。
  warning_signs:
    - 买入动机里出现"上次错过了……"
    - 标的的自我定位是"下一个XX"
  bound_to:
    - "危险说法反驳（18.11）"
    - "避而不买清单（9.2）"
  tags: [counter-example, dangerous-saying, next-big-thing, double-mistake]
  task_ids: [task-10, task-04]

- id: ce82
  title: 说法12"涨了=选对了，跌了=选错了"（Zapata vs Ethyl）
  type: counter-example
  source_chapter: 第18章 18.12 · L3979-3987
  source_quote: |
    "1981年Zapata因能源繁荣涨到高点被一致看好，Ethyl因环保署禁令被称为'被碾伤的
    狗'。结果'更好'的Zapata从35美元跌到2美元，Ethyl从2美元涨到32美元……短期涨跌
    既不能证明选股正确，也不能证明错误——它只说明有人愿意支付更多或更少的钱
    买同一只股票。"
  failure_mode: |
    用短期价格验证/推翻自己的判断：涨了拿得住（更危险），跌了自我怀疑割肉；
    "留住赢家扔掉输家"式操作被当成纪律。
  mechanism: |
    短期价格是他人报价而非事实裁决；把价格当成绩单会系统性地在低点卖出
    高认知正确率的持仓、在情绪顶点加仓。
  warning_signs:
    - 以"两个月涨了20%"论证自己英明
    - 基本面没变、只因下跌就推翻原有分析
  bound_to:
    - "危险说法反驳（18.12）"
    - "持有纪律（价格≠证据）"
  tags: [counter-example, dangerous-saying, price-validation, zapata-ethyl]
  task_ids: [task-10]

- id: ce82b
  title: 人民航空——研究不足就买入（林奇自认）
  type: counter-example
  source_chapter: 导论 0.6 · L169
  source_quote: |
    "是投资皮埃蒙特航空那样的卓越公司还是人民航空那样最终破产的公司？现在当我
    提到人民航空时，我多么希望当时能对这家航空公司的情况研究得再详细一些啊，
    果真如此的话，这家公司的股票我恐怕连一股也不会买了。"
  failure_mode: |
    对人民航空研究不足就买入，公司最终破产；（第14章）其残骸被得州航空收购，
    成为ce56连锁错误的一环；在18.11中又与"错过皮埃蒙特而买人民航空"的错上加错
    模式互证。
  mechanism: |
    低价航空的成本故事掩盖了服务与劳资的脆弱性；航空业的信誉与周期属性使
    "便宜+故事"组合风险极高。
  warning_signs:
    - 对公司的研究停留在"模式很好"层面
    - 行业属强周期+服务口碑敏感型
  bound_to:
    - "两分钟独白"
    - "定期重新核查"
  tags: [counter-example, self-admitted, people-express]
  task_ids: [task-07, task-09]
```

## F. 期权、期货与卖空（第19章，task-15 素材）

```yaml
- id: ce83
  title: 期权——判断正确仍输光本金（"万无一失"公司案例）
  type: counter-example
  source_chapter: 第19章 19.1 · L3999-4027
  source_quote: |
    "你确定'万无一失'公司将出重大利好，但3000美元只够买150股，于是你买了1美元/
    份的看涨期权……到期时股价没涨，3000美元全部打水漂。几个星期后股价真的开始
    大涨——你在分析判断完全正确的情况下输光了全部投资。"
  failure_mode: |
    用期权替代股票：对方向的判断正确，但时间杠杆（有效期1-2个月）使判断
    正确仍血本无归；一连串到期作废即倾家荡产。80%-95%的业余期权期货交易者亏损。
  mechanism: |
    期权是零和合同而非公司股份：公司繁荣股东全体受益，期权一方赚的每1美元
    都是另一方的亏损；买4-5份才能凑一年期限，溢价+佣金使成本高得惊人
    （"经纪人的摇钱树"）；资金不进入任何生产性用途。
  warning_signs:
    - 用"确定有利好"论证买短期期权
    - 为"小资金博大收益"选择衍生品
    - 从期权开始接触"技术形态"分析
  bound_to:
    - "否定期权期货（第19章红线结论）"
    - "股票=公司所有权的根本区别"
  tags: [counter-example, options, time-decay, zero-sum]
  task_ids: [task-15]

- id: ce84
  title: 投资组合保险加剧1987年崩盘
  type: counter-example
  source_chapter: 第19章 19.1 · L4029-4033
  source_quote: |
    "机构购买数十亿美元期货期权作'组合保险'……方案要求他们买入更多期货的同时
    必须自动卖出股票，巨量卖出导致股价下跌，又导致再买期货再卖股票的恶性循环。
    在导致1987年10月股市崩盘的合理解释中，组合保险是主要元凶，但许多机构仍在
    继续。"
  failure_mode: |
    机构把衍生品当保险，机制本身成为崩盘放大器；个人投资者模仿"专业做法"
    买看跌期权保护——每年浪费5%-10%资金防10%的下跌，"白忙一场"。
  mechanism: |
    机械规则+杠杆头寸同向共振：保险卖出制造下跌、下跌触发更多保险卖出；
    衍生品保险的保费损耗长期必然侵蚀本金（酒鬼尝一口啤酒 analogy：为保险
    入场者很快滑向投机）。
  warning_signs:
    - 用衍生品"对冲"长期股票持仓
    - 策略包含"下跌自动卖出"条款
  bound_to:
    - "否定期权期货"
    - "组合风险管理（用基本面分散，不用衍生品对冲）"
  tags: [counter-example, portfolio-insurance, 1987-crash, derivatives]
  task_ids: [task-15, task-11]

- id: ce85
  title: 卖空——判断正确仍亏2000-3000万美元（Resorts International）
  type: counter-example
  source_chapter: 第19章 19.2 · L4037-4055
  source_quote: |
    "精明的罗伯特·威尔森卖空国际度假胜地公司，事实证明他的判断是对的——大多数
    卖空者的判断都是对的，但最终是多久？卖空期间股价从70美分涨到70美元，上涨
    100倍，威尔森亏损2000万～3000万美元。卖空的亏损是无限的。"
  failure_mode: |
    亏算机制三重不利：①上涨无限（无止损天花板）；②持仓期无股息且账面盈利
    不能动用、股价上涨还要追加保证金；③市场保持非理性的时间可以超过你的
    资金撑得住的时间——被迫在最高点平仓。
  mechanism: |
    做多最大亏损100%（有限），卖空最大亏损无上限；卡通人物走出悬崖只要不往下看
    就能一直悬空——只要买家没意识到贵，股价就能一直贵。林奇结论：业余者不做卖空。
  warning_signs:
    - 抱有"这公司明显是垃圾"的确信感
    - 卖空理由是估值而非可验证的崩溃催化剂
    - 保证金账户无充足后备资金
  bound_to:
    - "否定卖空（第19章红线结论）"
    - "困境反转/隐蔽资产的正面方法（同一'公司要完'判断应做多对手或等右侧）"
  tags: [counter-example, short-selling, unlimited-loss, resorts]
  task_ids: [task-15]

- id: ce86
  title: 林奇式自我提醒——等一等再买故事股
  type: counter-example
  source_chapter: 第9章 9.4 · L2038
  source_quote: |
    "我总是尽量提醒自己（显然往往并不成功）：如果公司的前景非常美好，那么等到
    明年或者后年再投资仍然会得到很高的回报。当公司用业绩证明自己的实力以后，
    仍然可以从这只股票上赚到10倍的回报。"
  failure_mode: |
    "必须现在买否则来不及"的紧迫感本身是识别陷阱的信号；林奇承认自己
    反复犯此错（往往并不成功），故将其列为对小声耳语股票的最后一道闸。
  mechanism: |
    真实的前景经得起一年等待，等业绩记录出现后再买只损失一小段涨幅；
    经不起等待的"前景"多半是故事。这是延迟满足在选股中的机械化应用。
  warning_signs:
    - 决策时间压力感来自外部（配售、抢筹、首日）
    - 出现"现在不买就永远没机会"的内心独白
  bound_to:
    - "避而不买清单（9.4）"
    - "两分钟独白（含'为什么要现在买'）"
  tags: [counter-example, urgency-trap, self-admitted]
  task_ids: [task-04, task-07]

- id: ce87
  title: 卖出时机陈词滥调（翻番就卖/持满两年/跌10%止损）
  type: counter-example
  source_chapter: 第7章 7.5 · L1436-1441
  source_quote: |
    "把投资策略建立在'翻番就卖出''持有期满两年卖出''下跌10%马上止损'等陈词滥调
    上绝对是非常愚蠢的……把有潜力成为另一个沃尔玛的年轻公司当稳定增长型、只兑现
    50%就卖掉十分愚蠢；Ralston Purina已翻番且基本面不再激动时还指望再翻番，
    你肯定是疯了。"
  failure_mode: |
    用与公司类型无关的固定规则决定卖出：该拿十年的十倍股被50%止盈收割，
    该兑现的成熟股被"长期投资"名义死扛。
  mechanism: |
    卖出判据必须来自类型化的基本面信号（17.4），任何价格/时间参数化规则
    都会在某类股票上系统性亏损。
  warning_signs:
    - 卖出规则里只有价格与时间变量
    - 同一规则套用于所有持仓
  bound_to:
    - "分类型卖出判据（17.4）"
    - "六类公司分类"
  tags: [counter-example, selling-cliches, type-blindness]
  task_ids: [task-02, task-01]

- id: ce88
  title: 基于并购传言与小道消息的持仓（小声耳语的信息源）
  type: counter-example
  source_chapter: 导论 · L14；第9章 9.4 · L2022-2024；17.2 · L3584
  source_quote: |
    "不要理会什么热门消息，不要听证券公司的股票推荐，也不要看'千万不要错过的
    大黑马'之类的最新投资建议……小声耳语推荐'市值太小不适合基金，但你的私人
    账户绝对值得考虑'——这种电话同样打给了你的邻居们。"
  failure_mode: |
    把"别人特意告诉你的消息"当作信息优势：消息的传播广度恰使其无效，
    且推荐方往往有出货动机；Flowers/Lance（ce64）即为并购消息持仓的实例。
  mechanism: |
    真正的优势来自可重复验证的信息源（自己的消费/职业现场+公开财务数据）；
    消息的价值与其传播半径成反比。
  warning_signs:
    - 买入依据是"有人内部告诉我"
    - 无法从公开渠道复核消息的任何部分
    - 消息附带"快买，来不及了"
  bound_to:
    - "业余优势利用"
    - "信息获取程序（12.1-12.7）"
  tags: [counter-example, hot-tips, rumor]
  task_ids: [task-12, task-08]
```

---

## 覆盖核对（对照任务要求）

- 12种危险说法：ce70-ce82 逐条覆盖（18.1-18.12）✅
- 6类避而不买：ce23(热门)、ce27(下一个)、ce28/29(多元恶化)、ce30/31(小声耳语)、ce33(依赖大客户)、ce34(花哨名字) ✅
- 林奇自认错误：ce05(The Limited)、ce07(缅因州制糖)、ce20(Dreyfus/表6-1)、ce31(Bioresponse)、ce43(Bildner's)、ce53(Radice)、ce54(锐步/OshKosh)、ce56(得州航空)、ce62(华纳)、ce63(玩具反斗城)、ce64(Flowers/Lance)、ce71(凯撒)、ce82b(人民航空)、ce86(自我提醒) ✅
- 心理陷阱：ce04/13/16/17(追涨情绪)、ce32(IPO冲动)、ce77(等反弹再卖)、ce74(3美元亏多少)、ce44(内部人士卖出当信号)、ce80(错过损失幻觉) ✅
- 机构失败模式：ce08(滞后性)、ce09(批准名单)、ce10(掩埋罪证)、ce11(规模限制)、ce12(饭碗逻辑) ✅
- 期权期货卖空：ce83/84/85 ✅
- 产品畅销≠股票好：ce01(科尔克/帮宝适谬误) ✅
- 专题词核验：科尔克✅ Bildner✅ 人民航空✅ GCA✅ 艾伦伍德✅ 拉德✅ 佩恩中央✅ 宝丽来✅ 雅芳✅ EDS✅ 凯撒✅ 德罗特(正面人物，非反例，仅在ce09/ce63场景提及)✅ 缅因州制糖✅ 哈瓦莱特✅(ce03/04场景) 温彻斯特✅ 三哩岛✅(ce51/68) 梭哈✅ 掩埋罪证✅ 四项检验✅ 滞后性✅ 缩股/仙股/粉单✅(ce35)

> 注：哈瓦莱特光伏电池（7美元→3.5美元，导论0.3 L117）作为ce03/ce04（汉德图斯夫妇）场景内证据一并引用，未单列条目；博帕尔仅出现于困境反转正面案例语境（7.3.5），无独立失败模式，未列条目。
