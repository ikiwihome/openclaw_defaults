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

```bash
TAVILY_API_KEY=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 \
python3 ~/.openclaw/workspace/skills/openclaw-tavily-search/scripts/tavily_search.py \
  --query "..." --max-results 5 --format md --include-answer
```

---

*在这里添加你的工具配置和备忘。*
