# WeChat Account Operator Skill

An open-source skill for end-to-end WeChat Official Account content operations.

一个面向公众号内容运营的开源 skill，涵盖“选题 -> 研究 -> 立意 -> 写稿 -> 编辑 -> 排版交接”流程。

[Workflow Overview](https://github.com/Kyo-Zhou/wechat-official-account-workflow) | [Publishing Pair Repo](https://github.com/Kyo-Zhou/wechat-draft-publisher-skill)

This skill focuses on the editorial side of the workflow:

- define account positioning
- discover topics for a chosen direction or industry
- research public sources and benchmark accounts
- shape the article angle
- draft and edit long-form posts
- analyze reference layouts
- decide whether a draft is publishable

It does not contain real publishing credentials or account-specific secrets.

## Best For

- industry analysis accounts
- commentary and explainer accounts
- founder or brand accounts that publish structured long-form content
- operators who want a repeatable topic-to-draft workflow

适合：

- 行业研究型公众号
- 评论/解读型公众号
- 创始人或品牌表达型公众号
- 想把选题到成稿流程标准化的运营者

## What This Skill Does

This skill helps answer:

- what should this account write about
- which topics are worth covering
- what angle should the article take
- how should the article be structured
- what type of WeChat layout fits the account

## What This Skill Does Not Do

This skill does not:

- store AppID / AppSecret
- click through the WeChat backend manually
- own a production publishing profile

Use a separate publishing layer such as `wechat-draft-publisher` for conversion, preview, and draft-box upload.

## Quick Start

Use this skill when you want to say things like:

- `帮我定义这个公众号的定位`
- `结合 AI 行业，这周有哪些值得写的选题`
- `把这篇政策新闻改成适合公众号发的长文`
- `参考这几篇文章的布局，给我一个更成熟的排版方向`

Recommended working sequence:

1. define the account
2. choose the topic
3. research the topic
4. produce the brief
5. write the draft
6. edit into publishable form
7. hand off to `wechat-draft-publisher`

## Repository Structure

- `SKILL.md`: trigger description and working instructions
- `agents/openai.yaml`: UI-facing metadata
- `references/workflow.md`: topic and drafting workflow
- `references/layout-system.md`: WeChat layout principles
- `references/publishing.md`: publishing handoff checklist
- `references/quality-bar.md`: final editorial gate

## Suggested Workflow

1. Define the account direction.
2. Pick a topic inside that direction.
3. Research the topic from public sources.
4. Build an article brief.
5. Draft and edit the article.
6. Hand off the article package to a publishing layer.

## Recommended Handoff Output

When this skill finishes, it should ideally hand off:

- `article.md`
- `meta.yaml`
- title suggestion
- digest suggestion
- author suggestion
- layout recommendation
- cover recommendation

That output is designed to feed directly into `wechat-draft-publisher-skill`.

See [examples/handoff/meta.yaml](./examples/handoff/meta.yaml) for a minimal handoff example.

## Pairing

Recommended pair:

- `wechat-account-operator-skill`
- `wechat-draft-publisher-skill`

The first handles editorial quality. The second handles publishing execution.

## Example End-To-End Flow

1. Use this repo to define:
   - account direction
   - audience
   - content style
2. Ask it to produce:
   - topic shortlist
   - article brief
   - article draft
   - publishing handoff package
3. Pass the result into `wechat-draft-publisher-skill`.

## Roadmap

- add more article brief examples for different industries
- add reusable benchmark-analysis prompts
- add more explicit account-positioning worksheets
- add a stronger article-handoff schema for downstream tools

## Open-Source Boundary

Safe to open-source:

- workflow definitions
- research logic
- layout principles
- quality gates

Keep private:

- account-specific defaults
- private templates
- production credentials
- proprietary editorial playbooks
