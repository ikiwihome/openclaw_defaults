# TOOLS.md - 工具笔记

*记录你的本地配置、API 信息、快捷命令等。助手的随身速查卡。*

## 示例

```
## Gmail
- 账号: your@gmail.com

## 常用命令
- 查天气: weather Beijing
- 查日历: gog cal today
```

## 搜索工具

**联网搜索始终使用 Tavily Search**（不使用 Brave web_search）

## PDF 生成注意事项

- 生成**中文原生 PDF**时，必须显式嵌入支持中文的字体；不要直接用 Helvetica/Times 这类基础西文字体，否则容易出现乱码。
- 当前环境可优先使用 Windows 字体路径中的 `Deng.ttf` / `Dengb.ttf` 作为中文字体来源。

## Word 排版规范

- 以后所有 Word 文档默认采用统一视觉规范，追求工业级美观度。
- 中文字体统一优先使用 **微软雅黑**，英文字体统一使用 **Arial**。
- 默认要求：层级清晰、留白稳定、标题/正文/标签样式统一、颜色克制、页边距和段前段后间距一致。

## 文件目录规范

- 所有 Agents 制作或生成的文件，统一放到各自工作区的 `files/` 目录下。
- 如需交付到 Discord，先放入 `files/`，再发送。

```bash
TAVILY_API_KEY=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 \
python3 ~/.openclaw/workspace/skills/openclaw-tavily-search/scripts/tavily_search.py \
  --query "..." --max-results 5 --format md --include-answer
```

---

*在这里添加你的工具配置和备忘。*
