# Example Output: Learning Agent Skills

> This is a sample output produced by the `learn-new-domain` workflow. It demonstrates the expected artifact shape: source map, extraction, MECE model, and follow-up prompt.

## Source Map

| Tier | Source | Link | Why it matters | Status |
|---|---|---|---|---|
| S | OpenAI Codex Skills | https://developers.openai.com/codex/skills | Official Codex skill behavior, storage, invocation, and plugin packaging | verified |
| S | Agent Skills Specification | https://agentskills.io/specification | Open standard for `SKILL.md`, naming, and progressive disclosure | verified |
| A | Vercel Labs `find-skills` | https://github.com/vercel-labs/skills/blob/main/skills/find-skills/SKILL.md | Strong example of a meta-skill for discovering other skills | verified |

## Second-Order Extraction

1. Skills are not prompt collections. They are procedural knowledge packages.
2. `description` is the routing layer. Weak descriptions make good skills invisible.
3. Progressive disclosure is the core architecture: metadata first, `SKILL.md` second, references/scripts only when needed.
4. High-quality skills preserve validation: output formats, checks, and explicit failure boundaries.

## MECE Framework

| Layer | Question | Output |
|---|---|---|
| Purpose | What problem does this skill solve? | Clear job-to-be-done |
| Trigger | When should it activate? | Bilingual description and negative boundaries |
| Procedure | How should the agent act? | Step-by-step workflow |
| Evidence | How do we know it worked? | Checks, sources, and validation |
| Reuse | How does it stay useful? | Index entry, ownership, and update path |

## Follow-Up Prompt

Which direction should we deepen next: official source analysis, implementation examples, quality scoring, or packaging this into a new `SKILL.md`?
