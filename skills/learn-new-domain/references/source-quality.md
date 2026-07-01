# Source Quality Ladder

Use this before source selection and source confirmation.

## Reliability Tiers

| Tier | Source Type | Examples | Use |
|---|---|---|---|
| S | Official / primary sources | Official docs, standards, papers, source code, financial filings, legal text | Define facts, constraints, and terminology |
| A | Canonical expert sources | Classic books, top courses, expert long-form writing, benchmark case studies | Build judgment and frameworks |
| B | Strong implementation examples | High-quality GitHub projects, real cases, benchmarks, industry reports | Learn practice and edge cases |
| C | Community summaries | Blogs, forum posts, newsletters, marketplace pages | Discover leads; do not treat as final truth |
| D | Model prior knowledge | Model memory | Background only; never final evidence |

## Source Map Format

```markdown
## Source Map

| Tier | Source | Link | Why it matters | Status |
|---|---|---|---|---|
```

Status values:

- `verified`: opened or otherwise checked in this run.
- `user-provided`: supplied by the user.
- `unverified lead`: found but not opened/confirmed.
- `rejected`: not suitable or low quality.

## Source Confirmation Rule

Before deep synthesis, show the source map and ask the user:

```text
这些信息源是否符合你的预期？要不要指定/排除某些来源？
```

Proceed if the user confirms, or if the user explicitly asks you to continue with your best judgment.

## False Source Guard

Never invent:

- URLs
- authors
- publication dates
- direct quotes
- GitHub stars
- install counts
- benchmark numbers
- claims of "official" status

If unsure, say "未确认" or "I could not verify this source."
