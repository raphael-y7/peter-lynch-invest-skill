# Skill 地图 — 彼得·林奇的成功投资

一张表看清 12 张能力卡的编号、slug、去向与彼此依赖——先读入口 `SKILL.md`，再按路由表加载 1–2 张卡。

## 能力总表

| capability_id | slug | 中文标题 | 重要度 | 去向 |
|---|---|---|---|---|
| `cap.one-up-on-wall-street.classify-six-types` | `classify-six-types` | 六类公司分类判定 | critical | promoted → 独立 skill |
| `cap.one-up-on-wall-street.sell-rules-by-type` | `sell-rules-by-type` | 分类型卖出判据 | critical | promoted → 独立 skill |
| `cap.one-up-on-wall-street.stock-screening-checklists` | `stock-screening-checklists` | 双向筛选清单（13条选股准则+避而不买清单） | critical | promoted → 独立 skill |
| `cap.one-up-on-wall-street.pe-valuation` | `pe-valuation` | 市盈率与收益估值口径 | critical | promoted → 独立 skill |
| `cap.one-up-on-wall-street.financial-checklist-13` | `financial-checklist-13` | 13项财务指标核查 | critical | promoted → 独立 skill |
| `cap.one-up-on-wall-street.analyze-checklist-ch15` | `analyze-checklist-ch15` | 股票分析要点一览表（第15章通用+六类型专项核查） | high | promoted → 独立 skill |
| `cap.one-up-on-wall-street.dangerous-sayings` | `dangerous-sayings` | 12种危险说法识别与反驳+衍生品否定 | high | promoted → 独立 skill |
| `cap.one-up-on-wall-street.two-minute-story` | `two-minute-story` | 两分钟沉思独白 | high | router → 路由入口 |
| `cap.one-up-on-wall-street.recheck-holdings` | `recheck-holdings` | 定期重新核查 | high | router → 路由入口 |
| `cap.one-up-on-wall-street.portfolio-rules` | `portfolio-rules` | 组合构建与持有纪律 | high | router → 路由入口 |
| `cap.one-up-on-wall-street.self-test-eligibility` | `self-test-eligibility` | 入市自我测试与业余优势定位 | medium | router → 路由入口 |
| `cap.one-up-on-wall-street.research-info-gathering` | `research-info-gathering` | 信息获取与调研程序 | medium | router → 路由入口 |

合计 12 张：7 张 promoted（各自独立成 skill）、5 张 router（经来源路由入口到达）。

## 依赖关系

下表列出 `verified.yaml` 里各卡 `also_read` 字段声明的关系（左列是主卡，右列是主卡执行时可能需要补读的卡）。

| 主卡 | also_read |
|---|---|
| `classify-six-types` | `analyze-checklist-ch15`、`sell-rules-by-type`、`two-minute-story` |
| `sell-rules-by-type` | `classify-six-types`、`recheck-holdings`、`dangerous-sayings` |
| `stock-screening-checklists` | `pe-valuation`、`financial-checklist-13` |
| `pe-valuation` | `financial-checklist-13`、`stock-screening-checklists`、`analyze-checklist-ch15` |
| `financial-checklist-13` | `research-info-gathering`、`pe-valuation`、`analyze-checklist-ch15` |
| `analyze-checklist-ch15` | `classify-six-types`、`pe-valuation`、`financial-checklist-13`、`two-minute-story` |
| `dangerous-sayings` | `sell-rules-by-type`、`recheck-holdings` |
| `two-minute-story` | `classify-six-types`、`analyze-checklist-ch15`、`recheck-holdings` |
| `recheck-holdings` | `two-minute-story`、`sell-rules-by-type`、`dangerous-sayings` |
| `portfolio-rules` | `sell-rules-by-type`、`self-test-eligibility` |
| `self-test-eligibility` | `portfolio-rules` |
| `research-info-gathering` | `financial-checklist-13`、`analyze-checklist-ch15` |

读法提示：

- **枢纽卡**：`classify-six-types` 被 3 张卡引用，是分类前置门——类型不定，卖出判据、核查清单、独白模板都会错位。
- **互相引用**：`sell-rules-by-type` ↔ `recheck-holdings`、`sell-rules-by-type` ↔ `classify-six-types`、`analyze-checklist-ch15` ↔ `classify-six-types`、`portfolio-rules` ↔ `self-test-eligibility` 成对出现，说明它们是同一任务的两面，一次任务里通常成对加载。
- **只被引用一次的卡**：`self-test-eligibility` 与 `research-info-gathering` 各只被一张卡引用，分别位于流水线的入口门槛与信息供给层。

## 加载顺序

1. **先读入口** `SKILL.md`（single 模式）或 `peter-lynch-invest-skill-router/SKILL.md`（pack 模式的 router）：里面是触发条件、核心原则与路由表。
2. **按路由表定位**：用用户意图在路由表里找到对应的那张卡，再加载它。
3. **按需补读 1 张**：只有当任务确实跨域（例如判定类型后立刻要谈卖出），才按 `also_read` 补读第二张；单次任务最多 2 张。
4. **概览类问题不加载卡**：书名、作者、章节、整书结构走 `references/overview.md`；术语走 `references/glossary.md`；只要规则速查走 `references/cheatsheet.md`。
5. **路由表与 `references/capability-index.md` 都命不中**：明确告知超出本书范围，不硬套卡片。

> 每张卡内部按 R（原文）/ I（方法论骨架）/ A1（书中案例）/ A2（触发场景）/ E（可执行步骤）/ B（边界）六段组织，另附编译者补充的「A股适配」小节——该小节非原书内容，使用时请与原文判据区分。
