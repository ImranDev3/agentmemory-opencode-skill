---
name: agentmemory
description: Persistent memory for AI coding agents - remembers everything across sessions so you don't have to re-explain
argument-hint: "[search query or memory to save]"
user-invocable: true
---

# AgentMemory - Persistent Memory for AI Coding Agents

agentmemory silently captures what your agent does, compresses it into searchable memory, and injects the right context when the next session starts.

## Quick Start

```bash
# Terminal 1: Start the memory server
npx @agentmemory/agentmemory

# Terminal 2: Add to OpenCode
# Edit opencode.json and add the MCP config
```

## Configuration for OpenCode

Add this to your `opencode.json`:

```json
{
  "mcp": {
    "agentmemory": {
      "type": "local",
      "command": ["npx", "-y", "@agentmemory/mcp"],
      "enabled": true,
      "env": {
        "AGENTMEMORY_URL": "http://localhost:3111"
      }
    }
  }
}
```

## Commands

### Search Memory
Use `/recall <query>` or `memory_smart_search` MCP tool to search past observations.

Example: `/recall JWT auth middleware`

### Remember Something
Use `/remember <what to remember>` or `memory_save` MCP tool to save insights.

Example: `/remember Use jose package instead of jsonwebtoken for Edge compatibility`

### Session History
Use `/session-history` to see recent session summaries.

### Forget
Use `/forget` to delete observations or sessions.

## What Gets Captured

The system automatically captures:
- User prompts
- Tool usage (file edits, tests, commands)
- Error contexts
- Session summaries
- Sub-agent lifecycle

## Key MCP Tools

- `memory_smart_search` - Hybrid semantic + keyword search
- `memory_save` - Save an insight, decision, or pattern
- `memory_recall` - Search past observations
- `memory_sessions` - List recent sessions
- `memory_profile` - Project profile (concepts, files, patterns)
- `memory_file_history` - Past observations about specific files

## Viewer

Open `http://localhost:3113` to watch memory build live with session replay, knowledge graph, and health dashboard.

## Troubleshooting

If MCP tools aren't available:
1. Confirm agentmemory server is running (`npx @agentmemory/agentmemory`)
2. Check OpenCode config has correct MCP entry
3. Restart OpenCode after config changes

For more info: https://github.com/rohitg00/agentmemory