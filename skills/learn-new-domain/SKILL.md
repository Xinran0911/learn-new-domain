---
name: learn-new-domain
description: Source-first learning workflow for a new field. Use when the user wants to learn a domain, start this skill, research a new topic, find top sources, extract essence, build a MECE framework, produce a tutorial/methodology/checklist/playbook, or optionally turn the learning result into a Skill. 默认联网寻找并确认高质量信息源；信息源造假是红线。
---

# Learn New Domain

## Purpose

Use this skill to learn a new field from verified top sources, extract the essence, build a MECE model, and package the result into a tutorial, methodology, checklist, playbook, or optional Skill.

使用本技能学习一个新领域：默认联网寻找精华信息源，逐份解读，二次萃取，MECE 建模，多轮追问打磨，最后产出教程、方法论、清单、playbook，或让用户选择是否继续封装成 Skill。

## Hard Red Lines

- Never fabricate sources, links, citations, authors, dates, quotes, repository stats, install counts, or claims.
- Never treat model memory as a final evidence source.
- If a source cannot be opened or verified, label it as an unverified lead and do not use it as evidence.
- For factual or current claims, provide source links or state that the claim is unverified.
- Separate source discovery from synthesis. Do not synthesize from a fake or unconfirmed source list.

中文红线：

- 信息源造假是红线。
- 不能编链接、编作者、编日期、编引用、编 GitHub stars、编安装量。
- 打不开或没核验的资料只能叫“未验证线索”，不能当证据。
- 不能用模型记忆冒充资料来源。

## Trigger Workflow

If the user says they want to learn a field, start with field and output confirmation.

If the user only says "start this skill" or "use this skill", ask:

```text
你想学习什么领域？最终希望产出什么形式：高阶教程、方法论框架、学习路径、实操清单、对比评测、Skill brief，还是 SKILL.md 草案？
```

Do not begin source search until the domain is clear enough.

## Output Options

Offer these options when output format is unclear:

1. 高阶教程：适合系统学习
2. 方法论框架：适合复用和迁移
3. 学习路径：适合长期学习计划
4. 实操清单：适合马上执行
5. 对比评测：适合选型和决策
6. Skill brief：适合后续创建 Skill
7. SKILL.md 草案：适合直接封装成 Skill

Default to "高阶教程 + 方法论框架" when the user wants depth but does not choose.

## Core SOP

Follow this chain for substantial learning tasks:

```text
确认领域
→ 确认输出形式
→ 联网寻找 Top 信息源
→ 让用户确认信息源
→ 分别解读 Top 样本
→ 二次萃取
→ MECE 建模
→ 多轮追问补洞
→ 让用户确认成果
→ 继续打磨教程/方法论
→ 询问是否封装成 Skill
→ 最后总结
```

English version:

```text
Confirm domain
→ confirm output format
→ search web for top sources
→ confirm sources with user
→ deconstruct top samples separately
→ extract second-order principles
→ build a MECE model
→ ask follow-up questions to fill gaps
→ get user confirmation
→ polish tutorial/methodology
→ ask whether to package as a Skill
→ final summary
```

## Source Discovery

Default to web search for source discovery. If web access is unavailable, say so explicitly and ask whether to continue from user-provided files or local notes.

Read `references/source-quality.md` before ranking sources.

Source discovery rules:

1. Prefer official, primary, canonical, and implementation sources.
2. Rank sources before synthesis.
3. Show a source map and ask the user to confirm or adjust the source set before deep synthesis.
4. Use community summaries only as leads unless cross-validated.
5. Keep source links in the final artifact.

## Deconstruction And Synthesis

For each top source, deconstruct separately:

- What problem does it solve?
- What is the author's/source's authority?
- What are the key concepts and structure?
- What principles are reusable?
- What gotchas or edge cases appear?
- What should not be copied?

Then synthesize across sources:

- Extract shared principles.
- Resolve conflicts.
- Identify missing categories.
- Build a MECE model with sequence and boundaries.
- Convert the model into practice: examples, checklist, templates, exercises, or Skill design.

## Follow-Up Loop

This skill should actively prompt the user to refine the output.

After each meaningful draft, ask one concise follow-up:

- "这个方向对吗，要不要更偏实操/理论/案例？"
- "你还想追问哪个模块？"
- "是否要我继续压测这个框架的 MECE 和反例？"
- "是否要把这份教程进一步封装成 Skill？"

Do not declare the artifact finished until the user confirms it is good enough or asks to stop.

## Packaging

Read `references/output-patterns.md` when choosing final structure.

Read `references/quality-checklist.md` before finalizing a large tutorial or methodology.

When the user wants a Skill output:

- Produce a Skill brief first.
- Ask for confirmation before writing `SKILL.md`.
- If proceeding, use `skill-design-partner` or `skill-creator` conventions.
- If the user wants to publish or share the resulting Skill on GitHub, use `publish-skill-to-github` before any generic GitHub publish flow.

中文：如果用户要把产出的 Skill 发布到 GitHub、公开分享或做成仓库，先走 `publish-skill-to-github` 的 README、真实截图、许可证和验证检查，再提交推送。

## Final Summary

At the end, summarize:

- The domain learned.
- The strongest sources used.
- The final artifact produced.
- The core model/methodology.
- Remaining weak assumptions or open questions.
- Suggested next practice or packaging step.
