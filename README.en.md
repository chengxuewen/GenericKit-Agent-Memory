# GenericKit-Agent-Memory

AI agent memory storage submodule for the [GenericKit](https://gitee.com/chengxuewen/GenericKit) project.

## Purpose

This repository is a Git submodule of GenericKit (located at `.agents/GenericKit-Agent-Memory/`),
storing AI development session memory data via the `opencode-mem0` plugin.

## Configuration

In GenericKit's `.opencode/opencode.json`:

```json
{
  "plugin": ["opencode-mem0"],
  "mem0": {
    "storage_dir": ".agents/GenericKit-Agent-Memory"
  }
}
```

## Directory Structure

```
.agents/GenericKit-Agent-Memory/
├── README.md                   # Chinese version
├── README.en.md                # This file (English)
├── SESSION-YYYY-MM-DD.md       # Per-session development summaries
└── ...                         # mem0 plugin managed files
```

## Submodule Management

```bash
# Clone with submodules
git clone --recurse-submodules https://gitee.com/chengxuewen/GenericKit.git

# Update memory to latest
cd .agents/GenericKit-Agent-Memory && git pull origin master
```
