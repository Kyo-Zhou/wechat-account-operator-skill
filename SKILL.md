---
name: wechat-account-operator
description: Use this when the user wants an end-to-end WeChat Official Account content workflow for any industry or topic direction: define the account positioning, find topics from custom themes or industries, research public sources and reference accounts, shape the article angle, draft and edit long-form posts, design WeChat-friendly layouts, and prepare drafts for publishing workflows. This skill is for public-content research and editorial operations, not for manual backend clicking.
---

# WeChat Account Operator

Use `wechat-account-operator` for a reusable public-account workflow that can fit different industries, not just insurance.

Typical requests:

- help me define the positioning of this public account
- find good topics for this week in my industry
- follow a custom direction such as AI, healthcare, retail, legal, education, finance, insurance, or consumer brands
- study public WeChat articles or benchmark accounts and summarize their style
- turn a policy, trend, event, or company story into a long-form WeChat article
- polish a draft so it reads like a publishable public-account post
- analyze reference WeChat article layouts and extract reusable design patterns
- prepare a WeChat-ready article and hand it off to a publishing tool such as `md2wechat`

## Core Principle

This skill should be driven by the user's chosen direction, not by a fixed niche.

Always identify these first:

- account name
- account topic direction or industry
- target reader
- article type
- desired tone
- publishing goal

Treat the user's direction as configurable input.

Examples:

- insurance policy interpretation
- AI product commentary
- healthcare industry research
- legal compliance explainers
- education trend analysis
- consumer-brand observations

## Workflow

Follow this order unless the user clearly asks for only one stage.

1. Define the account positioning.
2. Collect topics from the user's chosen direction.
3. Research the topic from public sources.
4. Turn the topic into an article brief.
5. Write or refine the draft.
6. Edit for readability and account voice.
7. Design the WeChat layout.
8. Hand off to a publishing workflow when requested.
9. Review the result and capture reusable patterns.

## 1. Account Positioning

Before drafting, lock these down:

- account name
- direction or industry
- target reader
- main content form
- tone

Useful content-form defaults:

- explanatory long-form posts
- commentary and opinion
- industry observation
- case-study breakdowns
- practical how-to explainers

If the account already has published articles, study them first and preserve continuity.

## 2. Topic Discovery

Topic selection must match the user's chosen direction.

Possible topic sources:

- weekly industry developments
- policy or regulation changes
- company events
- product shifts
- market contradictions
- recurring reader questions
- evergreen explainers

Good topics usually satisfy at least two of these:

- timely
- consequential
- explainable
- relevant to the reader
- gives room for interpretation rather than simple summary

If the user gives a custom direction, generate topics inside that direction rather than defaulting to weekly hot topics.

Read [references/workflow.md](references/workflow.md) for the topic filter and drafting sequence.

## 3. Research

Collect public information before taking a position.

Priority order:

- primary documents
- official disclosures
- reputable reporting
- public WeChat articles
- benchmark account examples

When the user gives public WeChat article links, use `js-eyes` if available to inspect the actual page structure and layout. If `js-eyes` is unavailable, fall back to screenshots, copied text, or manual comparison, and say so clearly.

Do not claim backend access unless backend work was actually done.

## 4. Article Brief

Before writing, compress the topic into:

- one core judgment
- three to five supporting points
- one reader payoff

Reader payoffs vary by direction, but usually include:

- what changed
- why it matters
- who is affected
- what to do next
- how to interpret the signal

If the topic is thin, prefer a shorter piece rather than forcing a bloated long-form article.

## 5. Drafting

Default long-form structure:

- opening hook: event, deadline, contradiction, or reader problem
- core explanation: what happened
- deeper logic: why this matters
- reader-facing impact: what the audience should watch
- closing judgment: the lasting takeaway

Prefer useful interpretation over generic summary.

Avoid:

- pure news rewriting
- empty slogans
- fake urgency
- filler transitions that sound like AI scaffolding

## 6. Editing

After the first draft, tighten it for WeChat reading.

Edit in this order:

- title
- opening 2 paragraphs
- section order
- long paragraphs
- repeated phrasing
- summary line and closing

Good WeChat editing usually means:

- faster opening
- earlier conclusion
- fewer abstract piles of nouns
- more scanning anchors

If a sentence sounds like a slogan, rewrite it into a concrete claim.

## 7. Layout Design

For layout, prioritize readability over decoration.

Use a stable visual system:

- strong first screen
- recognizable section headers
- restrained callout blocks
- clean paragraph rhythm
- enough white space

When studying reference articles, extract:

- first-screen pattern
- section-header pattern
- highlight/callout pattern
- divider pattern
- overall visual tone

Prefer a layout that matches the account's editorial character:

- analytical accounts: restrained editorial layout
- consumer/lifestyle accounts: lighter and friendlier layout
- data-heavy accounts: stronger information hierarchy

Read [references/layout-system.md](references/layout-system.md) before doing substantial WeChat layout work.

## 8. Publishing Handoff

This skill handles the editorial workflow. When the user explicitly asks to create a draft or publish, hand off to a publishing tool such as `md2wechat` or to a separate private publisher skill.

Default publish preparation flow:

1. validate metadata
2. inspect the article
3. choose layout mode
4. preview locally
5. upload or create draft

Before upload, verify:

- title
- author
- digest
- cover
- body HTML quality

Use [references/publishing.md](references/publishing.md) for the concrete publishing checklist.

## 9. Review And Reuse

After pushing a draft or finalizing a piece, review three things:

- content quality
- layout quality
- reuse value

Record reusable lessons as:

- title formulas
- opening formulas
- section patterns
- layout modules
- content directions that fit the account well

## Quality Bar

The article is not ready just because it exists as a draft.

A publishable draft should pass all three:

- `worth reading`: has a clear judgment and real takeaway
- `easy to scan`: the first screen and headers reduce reading effort
- `looks intentional`: layout feels edited, not dumped from Markdown

Use [references/quality-bar.md](references/quality-bar.md) as the final gate.
