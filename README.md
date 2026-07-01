# Learn New Domain

Learn any domain from verified top sources. Extract the essence. Build MECE frameworks. Package reusable methods.

`learn-new-domain` is an agent skill for turning an unfamiliar field into a practical tutorial, methodology, checklist, playbook, or agent skill.

It is not a generic summarizer. It is a source-first research and modeling workflow.

```text
Confirm domain
-> confirm output format
-> search web for top sources
-> confirm sources with the user
-> deconstruct top samples separately
-> extract second-order principles
-> build a MECE model
-> ask follow-up questions
-> polish the tutorial or methodology
-> optionally package as an agent skill
```

## Why This Exists

Most AI learning workflows fail in predictable ways:

| Problem | What happens | This skill does instead |
|---|---|---|
| Fake or weak sources | The model invents links or treats random blogs as truth | Requires verified source maps and marks unverified leads |
| Shallow summarization | Produces a readable but weak overview | Extracts principles, gotchas, and reusable patterns |
| Non-MECE structure | Categories overlap or miss key parts | Builds layered, MECE models with boundaries |
| No iteration | Stops after one draft | Prompts the user to ask follow-up questions and refine |
| No reuse | Output becomes a one-off note | Packages results into tutorials, playbooks, checklists, or skills |

## Red Line: No Fake Sources

This skill is web-first and source-first.

It must not fabricate:

- URLs
- authors
- publication dates
- quotes
- GitHub stars
- install counts
- benchmark numbers
- claims of official status

If a source cannot be verified, it must be labeled as an unverified lead and excluded from evidence-based synthesis.

## What It Produces

The user can choose:

1. High-end tutorial
2. Methodology framework
3. Learning path
4. Practical checklist
5. Comparison/evaluation
6. Skill brief
7. `SKILL.md` draft

Default output: high-end tutorial plus methodology framework.

## Source Quality Ladder

| Tier | Source type | Use |
|---|---|---|
| S | Official docs, standards, papers, source code, filings, legal text | Define facts, constraints, and terminology |
| A | Classic books, top courses, expert long-form writing, benchmark case studies | Build judgment and frameworks |
| B | High-quality GitHub projects, real cases, benchmarks, industry reports | Learn practice and edge cases |
| C | Blogs, forum posts, newsletters, marketplace pages | Discover leads only |
| D | Model memory | Background only; never final evidence |

## Example Prompt

```text
Use $learn-new-domain to help me learn AI agent skills.
Find the best sources, confirm them with me, extract the core principles,
build a MECE framework, and turn the result into a practical tutorial.
```

## Install

Copy the skill folder into your local skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/learn-new-domain ~/.codex/skills/
```

Then restart your agent environment if it does not pick up new skills automatically.

The skill itself is in:

```text
skills/learn-new-domain/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── output-patterns.md
    ├── quality-checklist.md
    └── source-quality.md
```

## When To Use

Use this skill when you want to:

- Learn a new field from scratch.
- Build a top-down tutorial from verified sources.
- Turn scattered research into a MECE framework.
- Create a methodology, checklist, playbook, or learning path.
- Package a learning result into an agent skill.

## When Not To Use

Do not use this skill for:

- Quick one-line definitions.
- Pure brainstorming without source requirements.
- Tasks where the user already provided the final source set and only wants editing.
- Claims that require browsing when browsing is unavailable.

## License

MIT
