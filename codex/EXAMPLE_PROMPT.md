# Codex 调用示例

```text
请读取当前工作区里的资料文件，并使用 `crayon-shinchan-xiaohongshu` Skill。

目标：把资料做成一套 8 页小红书图文。
要求：
- 3:4 竖版
- 蜡笔小新主题感 / 90 年代日式家庭喜剧漫画 + 童趣蜡笔手绘
- 不是简单摘要，要重新找传播角度
- 每页只讲一个重点
- 输出每页上图文案、画面设计和生图提示词
- 最后输出小红书正文和置顶评论

如果资料里有不确定的信息，不要自行补全，标记需要核实。
```

## 保存为文件

```text
读取 `docs/source.md`，按 Skill 生成完整图文方案，并保存到：
- output/xiaohongshu-plan.md
- output/image-prompts.md
- output/caption-and-comment.md
```
