# Market Brief v6 — Master Style

Status: **ACTIVE MASTER TEMPLATE**

Reference implementation: `market-briefs/2026-09-09-0715.html`
Reference commit: `4b984bb7229b43e418acee7a2204f02bd6a84258`

## Core direction

Use the **Editorial C / Financial Times–inspired** layout as the default for all future market briefs.

### Typography
- Korean body and headlines: `Nanum Myeongjo` web font first, then serif fallback.
- Large editorial headline, generous line-height, restrained letter-spacing.
- Serif typography should remain dominant across the entire report.

### Color
- Paper: `#F4F3EF`
- Panel/light surface: `#FCFBF8`
- Soft neutral: `#ECEDEA`
- Main text: `#273038`
- Muted text/rules: gray family
- Burgundy: `#8C1D2C`
- Burgundy is reserved for judgement, risk, important interpretation, section numbers, and key conclusion.
- Do not color ordinary up/down moves green/red.

### What v6 removes
- No dark dashboard style.
- No shaded card stacks.
- No card-within-card composition.
- No decorative vertical Burgundy bars.
- No AI-looking left-side accent rails.
- No heavy boxes around interpretation blocks.
- No gradients or shadows.

### Editorial structure
- Use whitespace, serif hierarchy, and thin horizontal rules to separate information.
- Top header: kicker + large `증시 브리핑` title + DATE / AS OF / MARKET metadata.
- `종합 판단`: large editorial sentence, no boxed card.
- `상승 요인 / 위험 요인`: two-column text comparison on desktop; stacked with a thin horizontal rule on iPhone.
- Numeric facts: flat metric grid separated by thin rules, not individual cards.
- `해석 / 핵심`: editorial note with title + paragraph and horizontal rules only.
- Semiconductor section: two-column newspaper article layout; no boxed cards.
- Market snapshot: flat row list.
- News/fundamentals: editorial story columns with no card backgrounds.
- Scenario & Action: row-based structure; on iPhone each scenario stacks vertically instead of rendering a cramped table.
- Watch events: time + body rows separated by horizontal rules.
- Final conclusion: charcoal top rule + large Burgundy conclusion sentence.
- Today Checklist: question/answer rows, no cards.
- Sources: small serif text at bottom with DATA CUT / market-status tags.

## Mobile rules
- iPhone portrait first.
- Two-column comparison stacks to one column where readability requires it.
- Metric grid becomes 2 columns.
- Semiconductor columns become 1 column.
- Scenario rows become vertical blocks with `조건 / 해석 / 대응` labels.
- Watch and checklist become 1 column.
- Avoid narrow multi-column tables that wrap headings character-by-character.

## Fixed content order
1. 종합 판단
2. 상승 요인 / 위험 요인
3. 01 Korea Close
4. 02 Semiconductor Check
5. 03 US Open / Pre / After-hours Snapshot
6. 04 핵심 변동 원인
7. 05 AI · Memory Fundamentals
8. 06 Scenario & Action
9. 07 Watch 이벤트
10. 핵심 결론
11. 08 Today Checklist
12. Sources

## Data rules
- Re-check current public data on every execution.
- Verify every number with date and source.
- Clearly distinguish pre-market / regular session / after-hours / confirmed prior close.
- Mark unavailable values as `확인 불가` or `미확정`; never guess.
- On holidays, explicitly state that values are the prior trading day's confirmed close.
- Include KOSPI200 night futures when available and label the close time.
- Micron: verify recent official earnings and next official earnings schedule; mark unconfirmed items as unconfirmed.
- Event dates/times must be exact in KST and ET when officially published; never invent missing official times.
- Keep instrument coverage to the explicitly requested market instruments only. Do not add commentary, exclusion notices, verification notes, or legacy listing-status topics for instruments outside that scope.

## Permanent-link rule
- Save each generated HTML under `market-briefs/YYYY-MM-DD-HHMM.html`.
- If the path exists, fetch the current blob SHA and update it.
- Build the final link from the returned commit SHA using:
  `https://rawcdn.githack.com/hero1356-kor/stock-broadcast-catchup/<COMMIT_SHA>/market-briefs/YYYY-MM-DD-HHMM.html`
- Verify the committed file and commit before sharing.
- If GitHub save/verification fails, do not substitute a sandbox link; state failure and provide only the text briefing.

## Version label
All future reports using this design should identify the template as **v6**.