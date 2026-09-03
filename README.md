# Crayon Shin-chan Xiaohongshu Skill

把任意资料整理成「蜡笔小新主题感」的小红书多页图文方案。

本仓库提供两套版本：

- `codex/`：面向 Codex / Claude Code / Cursor Agent 等偏工程型智能体
- `domestic-agents/`：面向 WorkBuddy、豆包、Kimi、通义、国内通用 Agent 等自然语言智能体

> 说明：这里的“蜡笔小新主题感”强调童趣蜡笔、日常漫画、夸张表情、轻松吐槽与高可读图文编排。实际发布或商用时，请自行确认角色形象、商标与版权使用边界；如平台或模型限制直接复现特定角色，可改用“90 年代日式家庭喜剧漫画、童趣蜡笔手绘、圆润五官、夸张表情、生活化场景”等近似视觉语言。

## 适合的输入

- 飞书文档 / Markdown / README
- 教程文章 / 产品介绍
- 视频口播稿 / 录音整理稿
- 零散笔记 / 项目资料
- 使用体验 / 测评 / 方法论

## 默认输出

1. 内容定位
2. 小红书标题候选
3. 封面方案
4. 7–10 页图文页纲
5. 每页可直接上图的文案
6. 每页视觉说明与配图提示词
7. 小红书正文
8. 置顶评论

## 使用方式

本 Skill 默认输出图文方案、逐页文案和生图提示词；生成最终图片需要搭配可用的生图工具。无需把本地测试资料或生成结果上传到仓库。

### Codex

把 `codex/SKILL.md` 放入你的项目 Skill 目录，或直接让 Agent 读取它，然后提供资料并说：

> 使用 Crayon Shin-chan Xiaohongshu Skill，把这份资料做成小红书 8 页套图。

### 国内 Agent

上传或粘贴 `domestic-agents/SKILL.md`，再把资料一起发送，并说：

> 按这个 Skill，把我给你的资料做成蜡笔小新主题的小红书图文。

## 仓库结构

```text
crayon-shinchan-xhs-skill/
├─ README.md
├─ codex/
│  ├─ SKILL.md
│  └─ EXAMPLE_PROMPT.md
└─ domestic-agents/
   ├─ SKILL.md
   └─ EXAMPLE_PROMPT.md
```
