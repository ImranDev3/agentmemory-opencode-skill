# agentmemory-opencode-skill

<p align="center">
  <strong>OpenCode Skill for agentmemory - Persistent Memory for AI Coding Agents</strong>
</p>

---

## About

**OpenCode Skill for agentmemory** - A persistent memory system that makes your AI coding agent remember everything across sessions. No more re-explaining your code, tech stack, or preferences. Built on the original agentmemory project.

**What it does:**
- Remembers everything across sessions
- No more re-explaining your code/tech stack
- Automatic capture of tool usage, errors, decisions
- Hybrid search (BM25 + Vector + Knowledge Graph)
- 95.2% retrieval accuracy

**Credit:** Built on the amazing [agentmemory](https://github.com/rohitg00/agentmemory) by [rohitg00](https://github.com/rohitg00/agentmemory) (4400+ stars!)

---

## Features

- `/recall` - Search past memories
- `/remember` - Save important insights
- `/session-history` - View past sessions
- `/forget` - Delete memories
- 51 MCP tools
- 12 auto hooks
- Real-time viewer at http://localhost:3113

---

## Quick Start

```bash
# 1. Clone & Install
git clone https://github.com/ImranDev3/agentmemory-opencode-skill.git
cd agentmemory-opencode-skill
npm install
npm run build

# 2. Start MCP Server
node dist/standalone.mjs

# 3. Configure OpenCode
# Add to opencode.json:
{
  "mcp": {
    "agentmemory": {
      "type": "local",
      "command": ["node", "dist/standalone.mjs"],
      "enabled": true
    }
  }
}
```

---

## Commands

| Command | Description |
|---------|-------------|
| `/recall <query>` | Search memory |
| `/remember <insight>` | Save to memory |
| `/session-history` | View past sessions |
| `/forget <query>` | Delete memory |

---

## Credits

- **Original Project:** [rohitg00/agentmemory](https://github.com/rohitg00/agentmemory)
- **Author:** [rohitg00](https://github.com/rohitg00)
- **License:** Apache 2.0

---

## About Me

Hi! I'm Imran - a passionate developer who loves building tools for AI coding agents.

This skill is my contribution to the OpenCode community, bringing the power of agentmemory to OpenCode users.

**Connect with me:**
- GitHub: [@ImranDev3](https://github.com/ImranDev3)

Feel free to reach out if you have any questions or suggestions!

---

## Star the Original!

If you find this useful, please star the original [agentmemory](https://github.com/rohitg00/agentmemory) repo!

---
<p align="center">
  Made with ❤️ for the OpenCode community
</p>