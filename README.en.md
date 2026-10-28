<h1 align="center">Peter Lynch Invest Skill</h1>

<p align="center"><a href="README.md">中文</a> | English</p>

An AI skill pack for immediate use — it distills the stock-picking and holding methods in Peter Lynch's *One Up on Wall Street* into 12 capability cards that can be triggered individually or combined.

It is not a book summary, nor a reading response — it breaks the reusable methodology in the book into skill modules that can be triggered, executed and tested.

## What these skills solve

- You hold a stock but cannot say which of the six company categories it belongs to — and without the category, how much to buy, when to sell and which metric to watch are all wrong
- The stock is down 30% and thoughts like "it can't fall any more" or "at 3 dollars how much can I lose" show up, with no tool to rebut them line by line
- P/E is 40 with 15% growth and you cannot tell whether that is expensive; P/E of 8 looks cheap (a low P/E is not cheap, and for cyclicals you must read it backwards)
- You put the annual report down after three pages, not knowing which numbers matter first: how to compute net cash per share, what debt level is dangerous, what it means when inventory grows faster than sales
- A stock has doubled, the news is all praise and analysts all rate it top, and you cannot decide whether to take profit or keep holding; when it drops 25% you want to cut
- Whether to hold 5 positions or 20, what to buy with the proceeds, and why "pulling the flowers and watering the weeds" is the biggest mistake

## What was distilled

12 capability cards, organized in the order "classify first, screen second, do the math third, state the thesis fourth, manage discipline last":

- **Classification gate**: `classify-six-types` (six categories — slow growers, stalwarts, fast growers, cyclicals, turnarounds, asset plays — plus the net-profit share of a hot product)
- **Candidate screening**: `stock-screening-checklists` (13 positive criteria scored, 6 avoid-list flags excluded — a two-way gate)
- **Financials and valuation**: `financial-checklist-13` (cash position, debt structure, dividend record, book-value traps, hidden assets, free cash flow, inventories, pensions, growth, margins), `pe-valuation` (three P/E comparisons, (growth + dividend yield)/P/E, price-versus-earnings line divergence, two buying windows)
- **Full review**: `analyze-checklist-ch15` (the chapter-15 general checklist plus per-type items — the skeleton of one complete due-diligence pass)
- **Information and pre-commitment**: `research-info-gathering` (annual-report numbers / IR questions / field checks, taking facts and never adjectives), `two-minute-story` (the two-minute monologue before ordering: why buy, what must go right, what can go wrong — if you cannot say it, you do not buy)
- **Holding and selling**: `recheck-holdings` (new developments trigger a review, price moves do not; the three stages of a fast grower), `sell-rules-by-type` (a sell-criteria table per category — neither "it already doubled" nor "it already fell" is a criterion)
- **Portfolio and psychology**: `portfolio-rules` (3–10 positions, category mix, switch stocks not into cash, no stop-loss orders), `dangerous-sayings` (12 dangerous sayings rebutted one by one, plus the rejection of options, futures and short selling), `self-test-eligibility` (the three pre-entry questions and where an amateur's edge actually is — the first gate of the pipeline)

Seven of them are promoted to standalone skills (`classify-six-types`, `sell-rules-by-type`, `stock-screening-checklists`, `pe-valuation`, `financial-checklist-13`, `analyze-checklist-ch15`, `dangerous-sayings`); the other five (`two-minute-story`, `recheck-holdings`, `portfolio-rules`, `self-test-eligibility`, `research-info-gathering`) are reached through the source router. Every card carries its own "A-share adaptation" section — that section is added by the compiler and is not part of the original book.

`verified.md` records the 13 canonical units from the verification stage: the "13 stock-picking criteria" and "avoid list" units were merged into a single card (`stock-screening-checklists`, since both share the same output contract), which is why the final build ships 12 capability cards.

## Two packaging modes: single and pack

The same 12 capability cards are compiled twice, at two granularities. The content is identical; the only difference is how many entries an agent can discover.

| | single (one entry) | pack (compact pack, multiple entries) |
|---|---|---|
| Discoverable entries | **1**: `peter-lynch-invest-skill` | **8**: one source router + 7 promoted standalone skills |
| Where the 12 cards live | All inside the entry's `references/capabilities/`, loaded 1–2 at a time by the routing table | 7 high-frequency cards become standalone skills; all 12 still live in the router's `references/` |
| Triggering | Only the entry description participates in matching; routing happens after entry | The 7 high-frequency capabilities are matched directly, one hop fewer |
| Upgrades | Replace 1 directory | Replace 8 directories |

The 7 cards promoted to standalone skills in the pack:

- `classify-six-types` — six-category classification
- `sell-rules-by-type` — sell criteria by company type
- `stock-screening-checklists` — two-way screening checklists
- `pe-valuation` — P/E and earnings-based valuation
- `financial-checklist-13` — the 13 financial checks
- `analyze-checklist-ch15` — the stock-analysis master checklist
- `dangerous-sayings` — the 12 dangerous sayings, rebutted

### Which one to install

Pick by the way you work, and **install only one**:

| How you work | Recommended | Why |
|---|---|---|
| You use DSH / Codex / Claude Code with a skills directory and want a clean list | single | Takes 1 slot, loses no capabilities |
| Your daily questions concentrate on "what type is this / should I sell / is it expensive / how do I read the report / vet this for me / is that saying right" | pack | Those are exactly the promoted standalone skills, matched directly |
| You distribute to several agents or teammates who pick what they need | pack | They can install only the standalone skills they want |
| You want to install once and maintain one directory | single | Upgrades replace a single directory |

> Both builds come from the same bundle and carry identical capabilities. **Installing both will double-trigger**, so pick one.

## Examples

### Example 1: after a double, with the news all praise — should I sell?

**User question**

"I bought this at 18 and it is 42 now, more than double. The news is all praise lately and almost every analyst rates it top. Should I take profit?"

**How the skill reasons**

- First `classify-six-types`: classify by 3–5 year net-profit growth; 20%–25% puts it in **fast grower** (corroborated by small size and strong growth)
- Then the fast-grower criteria in `sell-rules-by-type`, checked one by one: (1) P/E of 30 against a most-optimistic two-year growth forecast of only 15%–20% (valuation-growth mismatch); (2) same-store sales down 3% in the latest quarter; (3) expansion stalling — no new stores opened, stores shabby, new stores disappointing
- `recheck-holdings` locates the stage: expansion / saturation / decline — telling a normal slowdown apart from a stage change
- The key step: this card states plainly that "it already doubled" is not a sell reason (the Toys "R" Us lesson of one buy and five sells), and neither is any price move

**Sample answer**

> Do not decide on the gain — doubling is not a sell signal for a fast grower; in the book, Toys "R" Us was sold out five times on exactly that thought and 25× was left on the table. Your stock is a fast grower, and it has only three criteria: valuation-growth mismatch (P/E 30 with only 15%–20% growth expected), same-store sales down 3% last quarter, and stalling expansion. None of the three fires, and none of the secondary signals either ("two senior executives left for a competitor", "12-city roadshow in two weeks painting an extremely rosy picture"), so the verdict is **keep holding**, and the pseudo-reasons excluded are "it went up a lot" and "the news is all praise". The analyst ratings and media praise are worth noting the other way: 40 analysts at top rating + 60% institutional ownership + three national magazines praising the CEO is the overheating combination the book names. If same-store growth slid from 10% to 2% without reaching -3%, that is still not a sell but a **switch to review** — use `recheck-holdings` to fix what to look at next and when.

### Example 2: P/E of 40 with fast growth — can I buy?

**User question**

"This company trades at 40× earnings but is growing fast. Isn't that what growth stocks are supposed to get? Can I buy?"

**How the skill reasons**

- Gate first, `classify-six-types`: confirm the type — for a cyclical you must read P/E **backwards** (the multiple looks lowest at peak earnings, which is the most dangerous moment); skip this and everything after is wrong
- Then `pe-valuation`, measuring the same P/E with three rulers: against the earnings growth rate (P/E ≈ growth is fair, half the growth rate is cheap, twice the growth rate means losing money is very likely); (growth + dividend yield)/P/E ≥ 1.5 to be attractive; then against its own historical range and the overall market level
- Cross-check with `financial-checklist-13`: net cash per share = (cash + securities − long-term debt) / shares outstanding, subtracted from the price to get the effective P/E — a cash-rich company's headline P/E overstates what you actually pay
- One independent red line: **never buy a stock with an extremely high P/E**. It takes part in no comparison; it is a veto

**Sample answer**

> Do the math before the story. P/E 40 against 15% growth scores (15+2)/40 ≈ 0.43, far below the 1.5 bar; and 40× is more than twice the 15% growth rate (2×15=30), which by the book's wording falls in the "losing money is very likely" bucket. The card's worked example is a direct comparison: price 24.00, EPS 1.20, growth 15%, dividend yield 2% gives P/E 20.00 and a score of 0.85 — already "too expensive, do not buy". Your 40× is twice as expensive again. Then the second ruler: what has its own P/E range been over recent years, and where is the overall market? If 40× sits clearly above its own history, you are paying for high growth "from now until forever", and McDonald's (P/E 50 back to 13), Avon (P/E 64) and Polaroid (P/E 50, down 89% in 18 months) are all that road. One thing must come first: confirm it is not a cyclical — cyclicals look cheapest exactly when earnings peak, so read the multiple backwards. So the answer is **do not buy**, unless you can show growth holding above 20% and this 40× sitting below its own historical range.

## How these skills were generated

These skills were produced with the **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** RIA-TV++ pipeline, in six stages:

1. **Whole-book comprehension (Adler analysis)** — apply Mortimer Adler's analytical reading method to the book: structure, interpretation, criticism, application
2. **Parallel extraction** — several specialized extractors (frameworks, principles, cases, counter-examples, terminology) mine candidate methodology units from the source text (609 candidates for this book)
3. **Triple verification** — every candidate must pass three checks: at least two independent in-book supports (cross-domain), the ability to answer questions the book never explicitly addresses (predictive power), and not being common sense (distinctiveness)
4. **RIA++ construction** — structure each unit along R (quotation) / I (restatement in own words) / A1 (in-book case) / A2 (future trigger scenario) / E (executable steps) / B (boundaries and blind spots)
5. **Zettelkasten linking** — map dependencies, contrasts and combinations between cards, producing the capability index and routing table
6. **Trigger and output testing** — write trigger blind tests (including decoy questions: fire when they should, stay silent when they should not) and output evaluation scenarios for every card; failing cards go back for rework and are re-verified afterwards

This book needed one more layer: the original is set in the 1980s US market, so every card carries an "A-share adaptation" section — the GNP≈3% classification baseline becomes China's nominal GDP growth, investor-relations channels become Hudongyi and Cninfo, and balance-sheet items are mapped to A-share reporting conventions. That section is added by the compiler and is not part of the original book.

## Testing and verification

This repository publishes the test material from the generation process alongside the skills: `evals/test-results.md` is the item-by-item scoring report, including failing cases, correction rules and known test biases — not just the passes.

- **Trigger precision**: 98 prompts shuffled and handed to 4 independent blind-test agents that see only the name/description of the 12 cards and the router entry. Every hard metric passed — promoted skills fired when they should 28/28, pure information-query decoys 7/7 with zero false triggers, and zero cross-calling among promoted skills 7/7
- **Raw and corrected figures both published**: raw hit rate 59/98 (60.2%); under the report's three documented correction rules (R1 direct selection of a router-domain card, R2 reasonable handling of edge cases, R3 reachability including direct selection) 98/98. Both figures are disclosed side by side
- **Output evaluation**: 12 cards × normal + boundary scenarios = 24 scenarios, run blind by 48 independent execution agents. The new_skill variant passed 24/24 assertions (100%); the without_skill variant passed 22/24 (91.7%)
- **The two failures show what the cards add**: without_skill could not cite the book's numbering system in `out-sayings-01` / `out-sayings-02`, nor the "80%–95% of long-term option and futures buyers lose money" figure — exactly the in-book numeric anchors the cards carry
- **Stop discipline**: in boundary scenarios the cards reliably refuse or ask instead (no sell criteria applied to an unclassified stock, `can_pass=false` when the input is pure emotion, an explicit "cannot verify" instead of a guessed number when data is missing)
- **Rework**: 0 capabilities needed rework, 0 descriptions needed changes
- **Known test bias**: in `out-ch15-02` the without_skill agent read the book transcript from the workspace on its own, so that case is really a "with the book" baseline; both variants passed and the conclusion is unaffected, but it is recorded

## Repository layout

```text
peter-lynch-invest-skill/
├── README.md                        ← Chinese version
├── README.en.md                     ← you are reading this
├── LICENSE                          ← MIT
├── BOOK_OVERVIEW.md                 ← whole-book comprehension (Adler four-step, stage 0 output)
├── verified.md                      ← triple-verification conclusions for the 13 canonical units
├── INDEX.md                         ← skill map: capability table + dependencies + loading order
├── bundle/                          ← canonical bundle (audit artifact, source of truth)
│   ├── verified.yaml                ← full definitions and promotion verdicts for the 12 cards
│   ├── cards/                       ← the 12 capability cards as authored
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
│   └── book/                        ← book-level material
│       ├── overview.md
│       └── glossary.md
├── single/                          ← single-entry build
│   └── peter-lynch-invest-skill/
│       ├── SKILL.md                 ← entry: triggers + routing table + loading rules
│       ├── BUILD_MANIFEST.json      ← build manifest and file hashes
│       └── references/
│           ├── overview.md          ← whole-book overview
│           ├── capability-index.md  ← full intent and keyword index
│           ├── cheatsheet.md        ← decision-rule quick reference
│           ├── glossary.md          ← glossary
│           └── capabilities/        ← 12 capability cards (same names as bundle/cards)
├── pack/                            ← multi-entry build (compact pack)
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── peter-lynch-invest-skill-router/
│   │   ├── SKILL.md                 ← source router entry
│   │   └── references/              ← 12 cards + 4 indexes, called by the router
│   ├── analyze-checklist-ch15/
│   │   └── SKILL.md
│   ├── classify-six-types/
│   │   └── SKILL.md
│   ├── dangerous-sayings/
│   │   └── SKILL.md
│   ├── financial-checklist-13/
│   │   └── SKILL.md
│   ├── pe-valuation/
│   │   └── SKILL.md
│   ├── sell-rules-by-type/
│   │   └── SKILL.md
│   └── stock-screening-checklists/
│       └── SKILL.md
└── evals/
    └── test-results.md              ← trigger blind tests and output evaluation, item by item
```

## Usage

Clone the repository first:

```bash
git clone https://github.com/raphael-y7/peter-lynch-invest-skill.git
```

### Install single (recommended first try)

```bash
# macOS / Linux
cp -r peter-lynch-invest-skill/single/peter-lynch-invest-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\peter-lynch-invest-skill\single\peter-lynch-invest-skill "$env:USERPROFILE\.agents\skills\"
```

### Install pack

Copy only the directories that contain a `SKILL.md`; do not copy the two JSON files under `pack/` into your skills directory:

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

> `~/.agents/skills` is the DSH skills directory; with another agent, use its own skills directory (for example `~/.claude/skills` for Claude Code).

### How to verify the install

Ask: "This stock has doubled for me — should I sell?" If the agent first classifies the company, then applies the sell criteria for that category and states plainly that "it went up a lot" is not a sell reason, instead of giving generic technical commentary or simply telling you to take profit, the install works. With the single build it reads the entry first and then routes to a card; with the pack build the matching capability is hit directly.

## Sources

- *One Up on Wall Street* by Peter Lynch and John Rothchild

## Notice

This repository publishes distilled skills, indexes and rule quick references only. It contains no PDF, EPUB, OCR files, screenshots or full-book transcripts of the source book. Quotations that appear in the capability cards serve solely to attribute methodology and keep the material auditable.

All numeric criteria in the book (the six-category growth bands, the P/E-to-growth multiples, the 13 financial thresholds, the option and futures loss rates, etc.) are case- and experience-based rules without statistical backtesting; some baselines are 1980s US market conventions, and the reset values in the A-share adaptation sections are compiler conventions. Test them on your own instruments and declare the convention you use. Nothing in this repository is investment advice.


## License

[MIT](./LICENSE)
