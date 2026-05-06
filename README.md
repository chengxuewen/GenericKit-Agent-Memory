# GenericKit-Agent-Memory

GenericKit 项目的 AI 代理记忆存储子仓库。

## 用途

此仓库作为 [GenericKit](https://gitee.com/chengxuewen/GenericKit) 项目的 Git 子模块，
通过 **mem0 MCP** 存储 AI 开发会话的记忆数据，支持 Claude Code、OpenCode、Codex 等多个代理平台。

## 配置

### MCP Server（跨平台通用）

`.mcp.json`：
```json
{
  "mcpServers": {
    "mem0": {
      "command": "npx",
      "args": ["-y", "@mem0/mcp"],
      "env": { "MEM0_DIR": ".agents/GenericKit-Agent-Memory" }
    }
  }
}
```

### OpenCode 专用

`.opencode/opencode.json`：
```json
{
  "mcp": {
    "mem0": {
      "command": "npx",
      "args": ["-y", "@mem0/mcp"],
      "env": { "MEM0_DIR": ".agents/GenericKit-Agent-Memory" }
    }
  }
}
```

### Claude Code

直接引用 `.mcp.json`，无需额外配置。

## 目录结构

```
.agents/GenericKit-Agent-Memory/
├── README.md                   # 本文件
├── README.en.md                # English version
├── SESSION-YYYY-MM-DD.md       # 各次开发会话摘要
└── ...                         # mem0 自动管理的记忆文件
```

## 子模块管理

```bash
git clone --recurse-submodules https://gitee.com/chengxuewen/GenericKit.git
```
