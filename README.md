# Sloot MCP Server

## ✨ Overview

A TypeScript [Model Context Protocol](https://modelcontextprotocol.io/) server built with Express and the official MCP SDK: HTTP + SSE transport, session handling, built-in demo tools, and health checks.

## 🌐 Website

Product context: [https://sloot.ai](https://sloot.ai)

## ⭐ Features

- 🚀 **Express** — HTTP server with MCP streamable transport
- 🔧 **Sessions** — UUID session IDs across requests
- 🛠️ **Built-in tools** — Echo, time, calculator examples
- 📡 **SSE** — Server-Sent Events for MCP notifications
- 🔒 **TypeScript** — Strict typing end-to-end
- ❤️ **Health** — Liveness endpoint for orchestration

## 📁 Project structure

```
sloot-mcp/
├── src/
│   └── index.ts       # MCP server + Express setup
├── dist/              # Compiled output
├── package.json
├── tsconfig.json
└── README.md
```

## 📡 Endpoints

Default port **3000** (override with `PORT`).

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/mcp` | Main MCP request/response |
| `GET` | `/mcp` | SSE / server notifications |
| `DELETE` | `/mcp` | End session |
| `GET` | `/health` | Health and basic status |

Session header (when required): `mcp-session-id: <uuid>`.

### 🧰 Built-in MCP tools

1. **echo** — Echo a message
2. **get_time** — Current server time
3. **calculate** — Basic arithmetic

## 🔗 Integrations

| Integration | Role |
|-------------|------|
| 🔌 [Pipedream](https://pipedream.com/) | SDK present for extended workflows (see code) |
| 🗄️ [Supabase](https://supabase.com/) | Optional client usage in project |

## 🧱 Tech stack

- 🟢 **Node.js**
- 🚂 **Express**
- 🔷 **TypeScript**
- 📦 **@modelcontextprotocol/sdk** — MCP protocol
- 🔐 **jsonwebtoken**, **cors**, **axios**

## 📜 Scripts

| Command | Purpose |
|--------|---------|
| `npm run dev` | ⚡ Run with `tsx` |
| `npm run watch` | 🔁 `tsx watch` |
| `npm run build` | 📦 Compile TypeScript |
| `npm start` | 🚀 Run `dist/index.js` |
| `npm run lint` | 🔍 ESLint |
| `npm run lint:fix` | ✨ ESLint fixes |
| `npm run format` | 📝 Prettier write |
| `npm run format:check` | ✔️ Prettier check |
| `npm run check` | ✅ Lint + format + build |

---

Built with ❤️ for the AI agent community.
