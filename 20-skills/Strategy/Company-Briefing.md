# Company Briefing

Use this skill to produce a concise company understanding brief that helps a reader understand what a company does, how its industry works, what strategy it appears to be pursuing, and what signals matter next.

## Purpose

This skill helps turn public research into a right-sized analyst-explainer brief. The goal is company literacy and independent judgment, not a forced investment, employment, or partnership recommendation.

Related files:
- `../../00-core/01-Operating-Principles.md`
- `../../00-core/02-Communication-Style.md`
- `Strategy-Analysis.md`
- `Decision-Memos.md`

## Context Check

Before using this skill:

- Identify the company, its website, and the reason for the brief
- Identify the intended reader and any known decision context
- Confirm whether the output should be a durable file, chat response, or internal note
- Check whether any assumptions may be stale, especially leadership, locations, funding, hiring, product status, partnerships, and recent news
- If the reader needs a recommendation rather than understanding, consider whether `Decision-Memos.md` is a better fit

## When To Use

Use this skill when the reader needs to understand a company well enough to decide whether it is interesting, worth more attention, or worth a deeper diligence pass.

Good use cases include:

- learning an unfamiliar company or industry
- preparing for a networking conversation or interview
- comparing companies at a high level
- building fluency in a sector
- deciding whether a company deserves deeper research

Do not use this skill for:

- a quick triage checklist
- a full investment memo
- a valuation exercise
- an offer decision
- a marketing profile or company puff piece

## Core Principles

- Explain why facts matter, not just what they are.
- Distinguish verified facts, reasonable inferences, and open questions.
- Keep the brief concise enough for the actual job. Do not use the full standard brief when the user needs triage, meeting prep, or a quick decision pass.
- Prefer current primary sources and credible public sources.
- Treat company claims as claims until supported by customers, revenue, product proof, regulatory progress, hiring, contracts, or independent coverage.
- Avoid overconfident culture, leadership, or traction conclusions from thin public evidence.
- Use frameworks only when they clarify the specific company.
- Do not make the reader learn unnecessary vocabulary just to understand the company. Use plain words unless the specialized term is needed and explained.
- Spell out acronyms, abbreviations, and initialisms on first body-text use. Company briefs often contain industry shorthand, so run an acronym pass before finalizing.

## Output Size Modes

Choose the smallest mode that satisfies the user's actual need.

1. `Triage`: 300-700 words. Use for deciding whether a company deserves more attention, updating a tracker, or producing a quick read. Include only the company read, why it matters, fit or concern signals if relevant, and next action.
2. `Meeting prep`: 1,200-2,000 words. Use for founder calls, informational interviews, hiring conversations, and next-day prep. Emphasize the practical read, conversation questions, and where the user may be useful. Do not produce a full company brief unless asked.
3. `Standard company brief`: 2,500-3,500 words. Use when the user wants a durable company-understanding artifact that teaches the business and industry in enough depth to support independent judgment.
4. `Deep diligence`: more than 3,500 words only with explicit approval. Use for unusually complex public companies, investment-style diligence, or situations where the user asks for a deep research package.

If the user asks for a "brief" without specifying depth, default to `Meeting prep` when there is a near-term conversation and `Standard company brief` when the purpose is durable company literacy.

## Source Standard

Use current public research plus official sources by default.

Start with:

- company website
- product pages
- careers page
- company LinkedIn page
- leadership pages and executive profiles
- recent press releases and news
- credible industry or trade sources
- customer, partner, contract, filing, or case-study evidence when available

For public companies, include a practical business read from public financial sources: revenue model, growth or traction, liquidity if easy to assess, capital intensity, and key financial risks. Do not turn the brief into a full financial review unless the user asks.

For private companies, avoid false precision. Funding, headcount, customer count, and revenue may be incomplete or stale. State uncertainty plainly.

## Workflow

## 1. Establish The Basic Read

Answer:

- What does the company do?
- Who uses or buys the product?
- What problem is it trying to solve?
- Why might this company matter now?
- What is the main uncertainty a reader should keep in mind?

This should become the executive orientation, not a long background section.

## 2. Understand Products And Offerings

Identify:

- main products or services
- target customers and use cases
- product maturity
- evidence of adoption or product proof
- dependencies such as regulation, hardware, data, supply chain, integrations, or customer behavior change

Explain what a reader should notice. For example, a product with impressive technical claims but little customer proof should be read differently from a narrower product with clear paying customers.

## 3. Map The Industry And Competitive Landscape

Explain the industry at the level needed to understand the company.

Cover:

- market category and where the company sits
- competitor types, not just competitor names
- substitutes and incumbent approaches
- customer buying dynamics
- regulatory, technical, capital, or distribution constraints
- what is changing in the market

Keep this section interpretive. The point is to help the reader see the game being played.

## 4. Read The Business Model And Stage

Summarize:

- revenue model or likely monetization path
- size and stage
- locations and operating footprint
- funding, ownership, or public-company status
- headcount or hiring signals when available
- traction indicators
- capital intensity and operating complexity

Use plain language. If the company is pre-revenue, development-stage, grant-funded, service-heavy, hardware-intensive, marketplace-like, or enterprise-sales-led, say why that matters.

## 5. Infer Strategy

Describe the company's apparent strategic bet.

Look for:

- wedge or beachhead market
- differentiation
- go-to-market path
- partnerships or ecosystem dependencies
- sequencing of products, customers, or markets
- likely sources of advantage
- execution risks

Do not overstate intention. Use language like "appears to," "suggests," or "the likely bet is" when inferring strategy from public evidence.

## 6. Assess Leadership And Culture Signals

Summarize:

- leadership background and relevant operating experience
- founder or executive communication
- hiring signals and role mix
- employee review patterns, if credible and current
- values and culture claims
- evidence limits

Separate company quality from leadership-style evidence. A promising company may still have unknown culture. A polished executive presence is not the same as proof of a healthy operating environment.

## 7. Identify What To Watch

End the analysis with:

- the biggest open questions
- signals that would strengthen the company read
- signals that would weaken it
- what deeper research should check next

This section should help the reader continue learning, not just close the file.

## Output Structure

Use this shape for `Standard company brief` by default:

1. Executive orientation
2. Products and offerings
3. Industry and competitive landscape
4. Business model, size, and stage
5. Strategy
6. Leadership and culture
7. What to watch
8. Source list

If useful, include a short "How to read this company" note near the top. This should teach the reader what lens matters most, such as capital intensity, regulatory approval, enterprise sales cycles, marketplace liquidity, customer concentration, or founder-led commercialization risk.

For `Triage`, compress the output to:

1. Company read
2. Why it matters or why it may not
3. Main open question
4. Recommended next action

For `Meeting prep`, compress the output to:

1. Executive orientation
2. What matters for this conversation
3. Company, founder, or role signals
4. Questions to ask
5. Where the user might help, if relevant
6. Source list

Do not include every standard section when the shorter mode is enough.

If the brief is acronym-heavy, include a short `Acronyms Used` list near the top or bottom. Keep it compact and include only acronyms that matter to the reader.

## Style

Write in an analyst-explainer style:

- clear, concise, and factual
- skeptical without being cynical
- explanatory without becoming academic
- grounded in evidence
- direct about uncertainty

Avoid:

- promotional language
- generic business jargon
- avoidable five-dollar words such as `substrate`, `leverage`, `operationalize`, `ecosystem`, `inflection`, and `posture`
- unexplained acronyms, abbreviations, or initialisms in body text
- long timelines unless history explains current strategy
- exhaustive lists of competitors without interpretation
- unsupported claims about culture, traction, or leadership quality
- repeating the same company thesis across `Executive orientation`, `How to read this company`, `Strategy`, `What to watch`, and any personal relevance section

Default plain-language rewrites:

- `substrate` -> `foundation`, `base`, or `underlying system`
- `leverage` -> `use`, unless discussing actual financial or mechanical leverage
- `operationalize` -> `put into practice`
- `inflection point` -> `turning point` or `shift`
- `ecosystem` -> `market`, `field`, `network`, or `partners`
- `posture` -> `position`, `stance`, or `recommended approach`

## Quality Bar

A strong company briefing:

- matches the selected output size mode
- explains what the company does in plain English
- teaches the reader how to think about the industry
- shows how products, customers, business model, and strategy fit together
- makes uncertainty visible
- names the next few signals worth watching
- includes enough sources to audit the main claims
- has passed a compression check: overlapping sections are merged, repeated claims are removed, and each section does distinct work
- has passed a plain-language check: avoidable jargon and five-dollar words are replaced, and necessary specialist terms are defined on first use
- has passed an acronym check: every acronym, abbreviation, and initialism is expanded on first body-text use unless it only appears in a URL, file path, ticker, product name, heading, short label, or compact metadata surface

## Common Failure Modes

- Writing a company profile instead of an analysis
- Repeating the company's own positioning without testing it
- Overweighting funding announcements, awards, or executive bios
- Listing competitors without explaining competitive dynamics
- Treating sparse public evidence as proof of culture
- Turning the brief into a full diligence memo
- Letting a personal decision lens dominate the company explanation
- Making the brief too long to be read in one sitting
- Using the `Standard company brief` structure for triage, tracker hygiene, or meeting prep
- Restating the same thesis in several sections instead of letting each section add new signal
- Making an unfamiliar company harder to understand by using avoidable abstract words
- Assuming the reader already knows industry acronyms such as `FAA`, `IDIQ`, `EBITDA`, `RAG`, `GTM`, or `NLP`
