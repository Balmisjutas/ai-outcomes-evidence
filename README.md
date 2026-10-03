# AI in government: evidence of outcomes

**Proposal, not results.** Draft, October 2026. Felipe Alvarez, M2 student in AI (CNAM Paris).
Not affiliated with, or endorsed by, the OECD.

## The idea in two lines

The OECD AI Incidents and Hazards Monitor (AIM) records what goes wrong with AI. I would like
to measure the other side for government AI: of the AI uses that governments list, how many
show a measured result, and not only an expected one.

## The gap, in the OECD's own words

- *Generative AI experimentation in government: Learning from emerging guidelines*, OECD Working
  Papers on Public Governance No. 93 (2026), https://doi.org/10.1787/42815683-en
  - p. 3: "monitoring and evaluation are identified as critical weaknesses, with few governments
    systematically measuring performance, impact, or compliance."
  - p. 7: "Where evaluation occurs, it often relies on basic indicators such as usage or user
    satisfaction, rather than structured assessments of performance, impact, cost and compliance."
  - p. 8: it proposes five areas to assess pilots: performance, projected impact and public
    value, cost and feasibility, usability, risk management.
- *The agentic AI landscape and its conceptual foundations*, OECD AI Papers No. 56 (2026), p. 28:
  "Future work could also prioritise the development of robust, cross-country indicators to
  track the development and adoption of AI agents."
- *Agentic AI in organisations*, OECD AI Papers No. 65 (2026), p. 23: "evaluation and assurance
  mechanisms remain immature". Footnote 1, p. 33: the OECD "is developing a dedicated workstream
  on agentic AI in government".
- The AI in government page of OECD.AI (https://oecd.ai/en/gov) presents the Digital Government
  Outlook 2026 as analysis of "what is needed to move from adoption to impact".

So the OECD already says the weak point is measurement. It is basically a counting question: of
what is listed, how much has evidence?

## What already exists (and what this proposal adds)

The closest work is an audit of the 2025 US federal AI use case inventory by Ishaan Shah
(September 2026, https://github.com/ishaanshah101/fed-ai-inventory-audit). It found that "of
1,480 live use cases, 37 state a numeric performance figure, 9 say what it was measured over,
and none states an uncertainty." This is the same kind of measurement I propose, done once,
for the US. I would build on it and use it as the check for my own rules.

What is not done yet, as far as I could find:
- the same rules applied to several countries' lists, so the numbers can be compared.
- expected benefits kept apart from achieved ones (the lists mostly ask for expected benefits,
  so counting them as results would count intentions).
- the same measurement repeated each time the lists are updated, so it becomes a series and not
  a one-off.

## The design in 5 steps

1. **Take the official lists.** EU Public Sector Tech Watch (open data, CC BY), the US federal
   inventory (yearly), UK Algorithmic Transparency Recording Standard records. The OECD
   *Governing with AI* use cases if they become open data.
2. **Freeze one rule set before reading results.** Written down and dated, and the same for all
   lists. No hand labelling: rules plus a language-model pass where the text needs reading.
3. **Grade each entry** on the levels below, from the entry text and its linked source.
4. **Calibrate.** Run the rules on the US list and compare with Shah's published counts. If my
   count is far from his (more than about 20%), the rules are not good enough and I say so.
5. **Publish a small table and repeat.** Share of live uses at each level, by country and by
   government function. Run again on each new version of the lists. AI agents are a tag inside
   the table, not a separate study, because the lists hold few of them for now.

## Evidence levels

| Level | What the entry shows |
|---|---|
| 0 | No benefit stated |
| 1 | Expected benefit only ("will reduce", "aims to") |
| 2 | Achieved benefit stated, no number |
| 3 | Achieved benefit with a number and a named metric |
| 4 | Level 3 plus what it was measured on (baseline, sample, period) or a check by others (audit office, evaluation, academic study) |

The source type (vendor, press, government, audit, academic) is kept as a separate tag. A
government page can report a number from a small staff survey, so the source alone is not the
grade.

## A small first step (about one week)

- Download the EU and US lists.
- Write and date the rule set.
- Reproduce Shah's US count as the calibration.
- Run the same rules on the EU list.
- Output: one table and one chart, "share of listed live government AI uses with a measured
  outcome, EU and US, by function".

## Limits

- This measures what the lists *say*. A use with no number in its entry may still work well.
  The result is about evidence in public records, not about whether AI works.
- The lists are self-reported and their fields differ, so some levels can only be read from
  free text.
- The lists change a lot between years, so a series needs care with renamed or dropped entries.
- Language-model passes make mistakes. They need a check, first against Shah's counts, later on a
  small sample if a team can provide one.
- Linking each listed system to AIM incidents would be nice but may not work: news rarely names
  an internal government system. I would test the match rate before promising it.
- If the OECD's own use case collection plans an outcome or evidence field, this work should feed
  it, not run next to it.

## Related work

- Shah (2026), audit of the 2025 US federal AI use case inventory:
  https://github.com/ishaanshah101/fed-ai-inventory-audit
- US federal AI use case inventory 2025 (data and data dictionary):
  https://github.com/ombegov/2025-Federal-Agency-AI-Use-Case-Inventory
- EU Public Sector Tech Watch dataset (European Commission):
  https://data.europa.eu/89h/e8e7bddd-8510-4936-9fa6-7e1b399cbd92
- UK Algorithmic Transparency Recording Standard hub:
  https://www.gov.uk/government/collections/algorithmic-transparency-recording-standard-hub
- Ada Lovelace Institute (2026), *Measuring up*:
  https://www.adalovelaceinstitute.org/policy-briefing/measuring-up/
- OECD.AI, AI in government: https://oecd.ai/en/gov
- My earlier notes on counting AI agent incidents with AIM's public data:
  https://github.com/Balmisjutas/ai-agent-incidents
