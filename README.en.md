<h1 align="center">One Up on Wall Street Skill</h1>

<p align="center"><a href="README.md">中文</a> | English</p>

An AI skill pack for immediate use — it distills the stock-picking and holding methods in Peter Lynch's *One Up on Wall Street* into 12 capability cards that can be triggered individually or combined.

It is not a book summary, nor a reading response — it breaks the reusable methodology in the book into skill modules that can be triggered, executed and tested.

## What these skills solve

- "This company's product just went viral — should I buy the stock?" Product hype and earnings growth are two different things: compute the product's revenue share and profit share first, and a contribution below 1.5% cannot move a large company's earnings
- "It is up 40% — should I take profit?" The same gain means opposite things across the six company types: a slow grower's 30%–50% band is its exit line, while a fast grower may only be getting started after doubling
- "A P/E of 40 — is that expensive?" P/E has to be compared with the earnings growth rate, with the stock's own historical range and with the overall market level, plus one veto rule: never buy an extremely high P/E
- An annual report is dozens of pages and you do not know which lines matter — walk the 13 metrics: compute net cash per share to lower the effective purchase price, then separate short-term bank debt (the most dangerous) from long-term bonds (the safest)
- A pile of stock ideas and no way to rank them — 13 criteria add points, and six avoid categories disqualify a candidate outright (hot industry hot stock / "the next X" / diworsification / whispered story / single-customer dependence / fancy name)
- You want to cut losses on the way down, grab gains on the way up, and switch stocks whenever a broker calls — 12 dangerous sayings are identified and rebutted one by one, and a sell decision only rests on company type and whether the original reason for buying still holds

## What was distilled

12 capability cards, organized in the order "qualify yourself first, then screen, then value and verify, then execute and hold":

- **Getting ready**: `self-test-eligibility` (entry self-test and locating your amateur edge)
- **Screening**: `classify-six-types-skill` (six company types), `stock-screening-checklists-skill` (two-way screen: 13 selection criteria + the avoid list)
- **Valuation**: `pe-valuation-skill` (P/E and earnings-based valuation), `financial-checklist-13-skill` (13 financial metrics)
- **Verification**: `research-info-gathering` (information gathering and research routine), `analyze-checklist-ch15-skill` (stock analysis checklist: chapter 15 general layer + six-type specific layers)
- **Execution**: `two-minute-story` (the two-minute monologue)
- **Holding and selling**: `recheck-holdings` (periodic recheck), `sell-rules-by-type-skill` (sell criteria by company type), `portfolio-rules` (portfolio construction and holding discipline), `dangerous-sayings-skill` (12 dangerous sayings plus the rejection of options, futures and short selling)

## Two packaging modes: single and pack

The same 12 capability cards are compiled twice, at two granularities. The content is identical; the only difference is how many entries an agent can discover.

| | single (one entry) | pack (compact pack, multiple entries) |
|---|---|---|
| Discoverable entries | **1**: `peter-lynch-invest-skill` | **8**: one source router + 7 promoted standalone skills |
| Where the 12 cards live | All inside the entry's `references/capabilities/`, loaded 1–2 at a time by the routing table | 7 high-frequency cards become standalone skills; the other 5 stay in the router's `references/` |
| Triggering | Only the entry description participates in matching; routing happens after entry | The 7 high-frequency capabilities are matched directly, one hop fewer |
| Upgrades | Replace 1 directory | Replace 8 directories |

The 7 cards promoted to standalone skills in the pack:

- `classify-six-types-skill` — six company types
- `stock-screening-checklists-skill` — two-way screen: 13 selection criteria + the avoid list
- `pe-valuation-skill` — P/E and earnings-based valuation
- `financial-checklist-13-skill` — 13 financial metrics
- `analyze-checklist-ch15-skill` — stock analysis checklist
- `sell-rules-by-type-skill` — sell criteria by company type
- `dangerous-sayings-skill` — 12 dangerous sayings plus the rejection of derivatives

### Which one to install

Pick by the way you work, and **install only one**:

| How you work | Recommended | Why |
|---|---|---|
| You use DSH / Codex / Claude Code with a skills directory and want a clean list | single | Takes 1 slot, loses no capabilities |
| Your daily questions concentrate on "what type of company is this / is it expensive / should I sell / is this company a trap" | pack | Those four are exactly the promoted standalone skills, matched directly |
| You distribute to several agents or teammates who pick what they need | pack | They can install only the standalone skills they want |
| You want to install once and maintain one directory | single | Upgrades replace a single directory |

> Both builds come from the same bundle and carry identical capabilities. **Installing both will double-trigger**, so pick one.

## Examples

### Example 1: the product went viral — can I buy the stock?

**User question**

"This company's product just went viral and everyone is talking about it. Can I buy the stock?"

**How the skill reasons**

- First `classify-six-types-skill`: when a hot product is what drew you to the company, the first step is not checking sales but doing two calculations — product revenue share = product revenue ÷ total revenue; product profit share = product profit ÷ total profit
- Adjudicate with the two anchors the book provides: a revenue share below 1.5% (Bufferin at Bristol-Myers, chapter 7, L1021) means the hype cannot move earnings; a profit share of 15% or more (Sterling's aspirin, L1023) qualifies as the real driver
- Then size it up (large / mid / small versus peers — the bigger the company, the lower the ceiling) and assign a type from the company's own net-profit growth: ≈3% slow grower, 10%–12% stalwart, 20%–25% fast grower, with earnings shape covering cyclical, turnaround and asset-play
- Once the type is set, output the expectation band and the next entry points (valuation, sell criteria, the chapter 15 checklist)

**Sample answer**

> Do not buy just because the product is hot. Do two calculations first: what share of total revenue does the product contribute, and what share of total profit? The book gives two anchors — with a revenue share below 1.5% (Bufferin at Bristol-Myers), that kind of good news barely moves earnings, and the stock rose 50 cents on the news and stopped; with a profit share of 15% or more (Sterling's aspirin), it is the real driver.
> Then assign a type. If net profit has grown 20%–25% a year for the last 3–5 years and the company is still small, it is a fast grower and you can continue with the fast-grower checklist; if growth is only around 4%, it is a slow grower — 30%–50% is its exit band, and a hot product does not change that.
> Two honest caveats: the 4%–10% and 12%–20% boundary bands have no arbitration rule in the book, so this card assigns the nearest type, cross-checks with dividends, price pattern and size, and labels the output "boundary band, uncertain" rather than inventing a threshold; and if the product's profit share lands in the 2%–15% middle zone (no continuous threshold exists between the two anchors), the only valid conclusion is "the evidence does not support a product-driven thesis" and you must ask for more data before re-judging.

### Example 2: it is up 40% — should I sell?

**User question**

"I bought at 20 and it is 28 now, up 40%. Should I lock in the gain?"

**How the skill reasons**

- `sell-rules-by-type-skill` does not start from the gain — it starts by confirming the type, because the six types have separate criteria and the same signal means the opposite thing under different types
- Slow grower: a 30%–50% gain since purchase is the exit line (17.4.1)
- Stalwart: sell when the price line rises above the earnings line, or when P/E is far above its own normal level (17.4.2); the gain convention is "start thinking at 50% in one or two years, 30%–50% lets you rotate into a peer that has not moved yet"
- Fast grower: the core discipline is precisely **not selling too early** — "already up N times" is not on the criteria table; the real signals are a P/E of 30 against a best-case two-year growth forecast of only 15%–20%, same-store sales down 3% in the latest quarter, and expansion stalling (17.4.4)
- Finally separate two things: the story breaking (the reason for buying no longer holds — must sell) versus price falling (it means nothing — no reason to sell)

**Sample answer**

> The 40% number is not a criterion by itself. Answer one question first: which of the six types is it?
> - Slow grower: 30%–50% is the exit band in the book, you are already inside it, so you can sell.
> - Stalwart: the book says "start thinking at 50% in one or two years" — 40% is not there yet, unless the price line is clearly above the earnings line or P/E is far above its own normal level.
> - Fast grower: the conclusion flips. The book says the selling skill for this type is not selling too early and missing a 10-bagger; being up 40% is not on the criteria table at all. What it should watch is a P/E of 30 against only 15%–20% growth, same-store sales down 3% in a quarter, and expansion stalling.
> One more thing must be said: the book states plainly that "there is no completely applicable universal formula for timing a sale", and it explicitly rejects type-blind fixed percentages such as "sell when it doubles" or "stop out at minus 10%". So if you cannot say which type it is right now, the correct move is to classify it first (`classify-six-types-skill`), not to decide sell-or-hold first.

## How these skills were generated

These skills were produced with the **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** RIA-TV++ pipeline, in six stages:

1. **Whole-book comprehension (Adler analysis)** — apply Mortimer Adler's analytical reading method to the book: structure, interpretation, criticism, application
2. **Parallel extraction** — several specialized extractors (frameworks, principles, cases, counter-examples, terminology) mine candidate methodology units from the source text
3. **Triple verification** — every candidate must pass three checks: at least two independent in-book supports (cross-domain), the ability to answer questions the book never explicitly addresses (predictive power), and not being common sense (distinctiveness)
4. **RIA++ construction** — structure each unit along R (quotation) / I (restatement in own words) / A1 (in-book case) / A2 (future trigger scenario) / E (executable steps) / B (boundaries and blind spots)
5. **Zettelkasten linking** — map dependencies, contrasts and combinations between cards, producing the capability index and routing table
6. **Trigger and output testing** — write trigger blind tests (including decoy questions: fire when they should, stay silent when they should not) and output evaluation scenarios for every card; failing cards go back for rework and are re-verified afterwards

The trail for this book: stage 0 whole-book comprehension → 609 candidate extractions → triple verification narrowing to 13 units → 12 RIA++ capability cards. The "A-share adaptation" section in every card is compiler-supplied material, kept in a separate section from the book's own facts and never mixed into quotations.

## Repository layout

```text
peter-lynch-invest-skill/
├── README.md                      ← Chinese version
├── README.en.md                   ← you are reading this
├── LICENSE                        ← MIT
├── single/                        ← single-entry build
│   └── peter-lynch-invest-skill/
│       ├── SKILL.md               ← entry: triggers + routing table + loading rules
│       ├── BUILD_MANIFEST.json    ← build manifest and file hashes
│       └── references/
│           ├── overview.md        ← whole-book overview
│           ├── capability-index.md  ← full intent and keyword index
│           ├── cheatsheet.md      ← decision-rule quick reference
│           ├── glossary.md        ← glossary
│           └── capabilities/      ← 12 capability cards
└── pack/                          ← multi-entry build (compact pack)
    ├── BUILD_MANIFEST.json
    ├── capability-destinations.json
    ├── peter-lynch-invest-skill-router/
    │   ├── SKILL.md               ← source router entry
    │   └── references/            ← 12 cards + indexes, called by the router
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

> `~/.agents/skills` is the DSH skills directory; with another agent, use its own skills directory (for example `~/.claude/skills` for Claude Code).

### How to verify the install

Ask: "This stock is up 40% — should I sell?" If the agent first asks which of the six types the company belongs to and then applies that type's criteria, instead of answering "up 40%, so take the money", the install works. With the single build it reads the entry first and then routes to a card; with the pack build, `sell-rules-by-type-skill` is hit directly.

## Sources

- *One Up on Wall Street* by Peter Lynch and John Rothchild
- Distilled from the whole book into 12 capability cards

## Notice

This repository publishes distilled skills, indexes and rule quick references only. It contains no PDF, EPUB, OCR files, screenshots or full-book transcripts of the source book. Quotations that appear in the capability cards serve solely to attribute methodology and keep the material auditable.

All numeric criteria in the book (growth bands, P/E tiers, same-store sales declines, position counts, gain bands, etc.) are case- and experience-based rules without statistical backtesting; test them on your own instruments and declare the convention you use. Nothing in this repository is investment advice.

## License

[MIT](https://opensource.org/licenses/MIT)
