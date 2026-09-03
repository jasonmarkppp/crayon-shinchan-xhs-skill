---
name: crayon-shinchan-xiaohongshu
summary: Turn source material into a high-retention Xiaohongshu carousel with a playful Crayon-Shin-chan-inspired visual language.
version: 1.0.0
---

# Crayon Shin-chan Xiaohongshu Skill — Codex Edition

## Purpose

Transform user-provided source material into a production-ready Xiaohongshu multi-image post with a playful, hand-drawn, Japanese family-comedy / crayon-manga visual language.

The goal is NOT to summarize the source. The goal is to extract the strongest传播角度, restructure the information for Xiaohongshu reading behavior, and produce page-by-page copy plus visual direction that can be immediately handed to an image-generation or design workflow.

## Default behavior

When this skill is invoked, do not ask unnecessary clarification questions. Use the supplied material as the source of truth, infer the strongest presentation angle, and produce a complete first pass.

Default to 8 pages unless the information density clearly requires 7–10 pages.

## Accepted inputs

You may receive:

- local Markdown / TXT / README files
- pasted text
- extracted content from Feishu / Notion / Docs
- product documentation
- tutorials
- video scripts
- project descriptions
- fragmented notes
- research material

If a linked document is inaccessible, ask the caller or host Agent to fetch/extract the content first. Do not invent unseen source content.

## Core transformation

For every task:

1. Read all available source material.
2. Identify the real user value, not merely the document title.
3. Determine the strongest Xiaohongshu framing.
4. Reorder the information for reading retention rather than preserving source order.
5. Remove low-value repetition.
6. Translate jargon into plain Chinese.
7. Keep each page focused on ONE core point.
8. Design a visual scene for each page.
9. Produce image-generation directions with deliberate text-safe areas.
10. Finish with post copy and a pinned comment.

## Preferred Xiaohongshu framings

Choose one primary angle unless the user specifies otherwise:

- 保姆级教程
- 新手第一次就能跑通
- 原来这个功能已经能做到这一步
- 一文看懂
- 新手避坑
- 实测体验
- 工具推荐
- 从 0 到 1
- 我替你整理好了
- 以前要手动做，现在可以交给 Agent
- 真正值得关注的不是 X，而是 Y

## Copy style

Write in Chinese unless the user requests another language.

Tone:

- conversational
- compact
- internet-native
- lightly humorous
- information-dense
- easy for beginners

Useful sentence patterns may include:

- “其实就是……”
- “你可以理解成……”
- “说白了……”
- “最离谱的是……”
- “重点不是……而是……”
- “看到这里你就懂了。”
- “这一页建议直接收藏。”

Do not overuse the same pattern.

Avoid:

- corporate brochure language
- textbook tone
- long academic paragraphs
- pure feature dumping
- empty hype
- AI-sounding generic conclusions
- three unrelated ideas on one page

## Visual language

The visual identity should feel like a lighthearted 1990s Japanese family comedy manga drawn with crayons and markers:

- naive hand-drawn outlines
- crayon / marker texture
- bright but not neon-heavy color blocks
- simple home / school / office / street scenes
- exaggerated facial expressions
- playful comic dialogue bubbles
- hand-written annotations
- stickers, arrows, memo notes
- imperfect handcrafted layout
- warm everyday humor

When policy, model, or platform constraints make direct reproduction of copyrighted characters inappropriate, replace direct character naming with this descriptive visual language instead of forcing an exact character likeness.

## Character usage strategy

The character should SUPPORT the information, not overpower it.

Typical roles:

- confused beginner
- excited discoverer
- lazy-but-clever office worker
- exaggerated reaction character
- narrator pointing at a UI card
- side character asking a naive question

Do not make every page the same pose.

## Layout rules

Every page should contain:

- 1 dominant message
- 1 visual focal point
- 1–2 supporting annotations
- enough whitespace for mobile reading
- a clearly reserved title / copy zone

Prefer 3:4 vertical composition for Xiaohongshu unless the user specifies another ratio.

Do not cram long paragraphs into the image.

## Default page architecture

### P1 — Cover

Goal: click-through.

Use:
- short main headline
- one strong contrast / result
- expressive character scene
- 2–3 supporting keywords max

### P2 — Why this matters

Explain what changed, why the reader should care, or what problem this solves.

### P3–P6 — Core content

One key concept, step, use case, or contrast per page.

Favor:
- before vs after
- 1 / 2 / 3 steps
- “普通模式 vs Agent 模式”
- real use cases
- visible workflow

### P7 — Pitfalls / checklist

Make the post save-worthy.

### P8 — Conclusion / action

Summarize the real takeaway and invite the reader to save, comment, try, or read the next post.

## Output contract

Return exactly these sections unless the user asks for a different format.

# 1. 内容定位

Include:
- 主题一句话
- 核心受众
- 最强传播角度
- 为什么这个角度比原文标题更适合小红书

# 2. 标题候选

Provide 4–6 titles.

Titles should be specific, clickable, and non-spammy.

# 3. 封面方案

Provide 2–3 options.

Each option must include:
- 大标题
- 小标题
- 辅助卖点
- 画面构图

# 4. 图文页纲

For each page provide:

## Pn｜页面标题

**页面目的：**

**上图主文案：**

**辅助文案：**

**视觉设计：**

**角色表演：**

**排版建议：**

**配图提示词：**

Image prompt must describe:
- page purpose
- scene
- character action / emotion
- composition
- text-safe area
- playful hand-drawn crayon manga look
- simple readable background
- Xiaohongshu carousel design

Do NOT ask the image model to render large blocks of precise Chinese text. The prompt should reserve space for later typography unless the generation model is known to handle text reliably.

# 5. 小红书正文

Write a publish-ready caption that does NOT mechanically repeat every image page.

Structure:
- hook
- 2–4 short paragraphs of value
- practical note / caveat
- soft interaction CTA
- 5–10 relevant hashtags

# 6. 置顶评论

Create one concise pinned comment for:
- resource links
- extra note
- download instructions
- next-post teaser
- or an interaction prompt

If links are not supplied, never invent them. Use placeholders such as `[资料链接]`.

# 7. 可选优化建议

Only include high-value suggestions such as:
- which page should be emphasized
- which page can be removed
- which title is strongest
- whether to split into two posts

## Information integrity

Never fabricate steps, product capabilities, prices, links, or settings not present in the source.

If an important fact is uncertain, mark it as needing verification instead of presenting it as confirmed.

## Execution mode for local files

When running inside Codex or another coding Agent:

1. Locate and read the source files first.
2. Prefer source files over assumptions.
3. If several files are relevant, synthesize them before writing the carousel.
4. If the user asks to save outputs, write Markdown files to a sensible output folder.
5. If image-generation prompts are requested as separate files, create one prompt file per page or a single structured `image-prompts.md`.
6. Do not modify unrelated project files.

## Suggested output files

If the user requests files, use:

```text
output/
├─ xiaohongshu-plan.md
├─ image-prompts.md
└─ caption-and-comment.md
```

## Trigger examples

- “用这个 Skill 把 README 做成 8 页小红书图文。”
- “读取 docs/tutorial.md，生成蜡笔漫画主题的小红书套图方案。”
- “把这份飞书提取内容改造成保姆级教程图文，封面要有点击感。”
- “按 Skill 输出 3:4 套图文案和每页生图提示词。”

## Success criteria

A successful output should feel:

- immediately usable
- clearly restructured rather than summarized
- readable on a phone
- visually coherent as one set
- playful without becoming childish
- useful enough to save
- specific enough to design without another planning round
