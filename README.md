# 🧠 solc-mcp


`solc-mcp` is a Solidity Compilation module for [PILSO OS](https://pil.so) — the secure execution layer for onchain agents and LLMs.  
This MCP server allows agents to securely compile Solidity contracts from within the MCP runtime, enabling dynamic smart contract creation, analysis, and deployment workflows.

Part of the PILSO OS Suite — Pilot Interface for LLMs Signature Operations — this server adds Solidity compilation to the modular MCP agent stack.

📄 Full `erc20-mcp` documentation: [docs.pil.so](https://docs.pil.so/mcp-server-models/erc20-mcp-token-operations)

---

## ✨ Key Features

- 🛠 **On-the-Fly Compilation**: Accepts raw Solidity code, compiles it with `solc`, and returns ABI + bytecode in a structured format.
- 🤖 **Agent-Ready**: Fully compatible with LLM agents like Claude or GPT-4 inside the PILSO runtime.
- ⚙️ **Version Flexibility**: Supports version targeting via `solc` and `solc-js`, so agents can specify compiler versions dynamically.
- 🔌 **Composable**: Integrates seamlessly with other MCP tools like `chainlist-mcp`, `erc20-mcp`, or `metamask-mcp`.

---

## 📦 Requirements

- Node.js (v20 or higher)
- `pnpm`

---

## 🚀 Setup

```bash
# 1. Clone the repo
git clone https://github.com/pilso/solc-mcp.git
cd solc-mcp

# 2. Install dependencies
pnpm install

# 3. Build the project
pnpm build
```

## 🧠 Usage with Claude / PILSO Agent
Include in your .mcpilot.config.json:

```bash
{
  "mcpServers": {
    "solc": {
      "command": "node",
      "args": ["./dist/index.js"]
    }
  }
}
```

Then your agent can compile contracts with prompts like:
`Compile this Solidity contract and return the ABI and bytecode for deployment.`

---

## 🧱 Part of PILSO OS

PILSO OS is the trustless AI signing layer for Web3 — powered by modular MCP servers.

`solc-mcp` is part of the PILSO OS suite — enabling secure contract compilation and deployment flows, driven by LLMs. 

This MCP module makes it possible for agents to reason about and interact with smart contracts at the code level, safely and deterministically.

---

## 📚 Documentation

Full documentation available at: [https://docs.pil.so](https://docs.pil.so)

---

## ⚖️ License

MIT License
