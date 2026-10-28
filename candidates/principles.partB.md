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
