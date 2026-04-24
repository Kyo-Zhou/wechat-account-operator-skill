# Publishing Checklist

Use this reference before creating a WeChat draft.

## Metadata

Check:

- title is within WeChat limits and reads naturally
- author is correct
- digest is specific and not generic
- cover is available and suitable

## `md2wechat` Path

Use `md2wechat` for:

- inspect
- preview
- convert
- create draft

If `API mode` is unavailable because the service key is missing or invalid, switch to `AI mode` and be explicit that HTML quality must be manually reviewed before upload.

## Draft-Box Guardrails

Before upload, verify:

- no preview/debug shell content leaked into the body
- no obvious encoding corruption
- no broken tags or strange symbols
- opening screen looks intentional in WeChat
- body does not feel like raw Markdown export

## Common Failure Modes

- invalid IP whitelist
- invalid or stale WeChat secret
- missing cover media id
- test preview content uploaded as draft
- AI-generated HTML that is technically valid but visually crude

## Final Human Review

Even after successful upload, review in the WeChat editor:

- first-screen text rhythm
- section header weight
- paragraph density
- digest and title pairing
- whether the draft feels publishable without embarrassment
