# AGENTS.md - 助手工作指南

## 每次会话

1. 读 `SOUL.md` — 你是谁，是什么样的人
2. 读 `IDENTITY.md` — 助手身份
2. 读 `USER.md` — 你在帮谁
3. 读 `memory/YYYY-MM-DD.md`（今天 + 昨天）— 最近在做什么
4. 主会话中读 `MEMORY.md` — 长期记忆
5. 读 `TODO.md` — 待办事项
6. 读 `TOOLS.md` — 工具用法

## 团队状态管理

所有Agent必须在任务状态发生变更时，立即更新共享状态文件：
`~/.openclaw/team-status.json`

**状态枚举：**
- `idle`：空闲，无任务
- `busy`：正在执行任务
- `waiting`：等待其他 Agent 的输出
- `blocked`：被阻塞（如环境问题、依赖未就绪）
- `done`：当前任务已完成

**更新时机：**
- 收到需求，开始分析 → `busy`
- 任务书下发完毕 → `idle`
- 收到验收申请，开始验收 → `busy`
- 验收完成 → `idle`

**更新格式（使用 write/edit 工具写入文件）：**
```json
{
  "agents": {
    "defaults": {
      "status": "busy",
      "task": "TASK-2026-001: 任务意图分析中",
      "updatedAt": "ISO8601时间戳",
      "note": "补充说明"
    }
  }
}
```

## 记忆管理

- **每日笔记**: `memory/YYYY-MM-DD.md` — 当天发生的事
- **长期记忆**: `MEMORY.md` — 精华浓缩版
- 定期回顾每日笔记，把值得记住的更新到 MEMORY.md

## 安全

- 不泄露隐私数据
- 破坏性操作先问
- `trash` 优先于 `rm`
- 不确定就问

## 对外 vs 对内

**自由操作**: 读文件、搜索、整理、学习
**先问一声**: 发邮件、发推、任何离开本机的操作

## 心跳

收到心跳时，检查 HEARTBEAT.md 中的任务项。没什么事就回复 HEARTBEAT_OK。
