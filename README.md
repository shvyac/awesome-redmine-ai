# Awesome Redmine AI

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

A curated list of resources for using **AI with Redmine** — AI plugins, MCP servers that let AI agents work with Redmine issues, local LLM setups, automation, GitHub integration, and the API clients and plugins that make it all work. Prefer durable official / project URLs.

**Discovery list only** — most Redmine AI projects are young and small; check compatibility with your Redmine version and review what data is sent to an LLM before installing. ⭐ badges show live GitHub star counts (via shields.io); release badges show the date of the latest GitHub release (YYYY/MM/DD, as of the last refresh); last-commit badges show live commit activity (via shields.io).

## Contents

- [Official & distributions](#official--distributions)
- [AI plugins (inside Redmine)](#ai-plugins-inside-redmine)
- [MCP servers (AI agents → Redmine)](#mcp-servers-ai-agents--redmine)
- [Local LLM stack](#local-llm-stack)
- [Automation & workflows](#automation--workflows)
- [GitHub & chat integration](#github--chat-integration)
- [API clients](#api-clients)
- [Search & knowledge plugins (AI-friendly)](#search--knowledge-plugins-ai-friendly)
- [Related lists](#related-lists)
- [Contributing](#contributing)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

---

## Official & distributions

- [Redmine](https://www.redmine.org/) ![GitHub stars](https://img.shields.io/github/stars/redmine/redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/redmine/redmine?style=flat) - Flexible open-source project management and issue tracking (Ruby on Rails). ([GitHub mirror](https://github.com/redmine/redmine))
- [Redmine Plugins Directory](https://www.redmine.org/plugins) - Official plugin directory.
- [Redmine REST API](https://www.redmine.org/projects/redmine/wiki/Rest_api) - Official REST API documentation, used by every MCP server and client below.
- [RedMica](https://www.redmica.jp/) ![GitHub stars](https://img.shields.io/github/stars/redmica/redmica?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F04-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/redmica/redmica?style=flat) - Redmine-compatible distribution that ships upcoming Redmine features early (Japan). ([GitHub](https://github.com/redmica/redmica))
- [Docker Official Image for Redmine](https://github.com/docker-library/redmine) ![GitHub stars](https://img.shields.io/github/stars/docker-library/redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/docker-library/redmine?style=flat) - Official container image; handy for a local AI test environment.

---

## AI plugins (inside Redmine)

- [Redmine AI Helper](https://github.com/haru/redmine_ai_helper) ![GitHub stars](https://img.shields.io/github/stars/haru/redmine_ai_helper?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/haru/redmine_ai_helper?style=flat) - The most complete AI plugin: chat sidebar, issue / wiki summaries, subtask generation, inline completion, typo checks, repository code explanation, project health reports (with charts, PDF / Markdown export), Office attachments passed to the AI as Markdown, built-in MCP server, and Qdrant vector search for similar / duplicate issues. Can run fully offline with Ollama via the OpenAI-compatible provider.
- [Redmine AI Summary](https://github.com/tuzumkuru/redmine_ai_summary) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/redmine_ai_summary?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F10%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/tuzumkuru/redmine_ai_summary?style=flat) - Generates AI summaries of issues.
- [Redmine AI Assistant](https://github.com/carolcoral/redmine_ai_assistant) ![GitHub stars](https://img.shields.io/github/stars/carolcoral/redmine_ai_assistant?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/carolcoral/redmine_ai_assistant?style=flat) - Unified AI capability hub that other Redmine plugins can call.
- [Redmine GTT Assistant](https://github.com/gtt-project/redmine_gtt_assistant) ![GitHub stars](https://img.shields.io/github/stars/gtt-project/redmine_gtt_assistant?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/gtt-project/redmine_gtt_assistant?style=flat) - "Smart assistant" for the GTT (geo-task-tracker) Redmine stack.
- [Redmine Agent](https://github.com/adhi-software/redmine_agent) ![GitHub stars](https://img.shields.io/github/stars/adhi-software/redmine_agent?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/adhi-software/redmine_agent?style=flat) - AI agent for natural-language queries against Redmine with any configurable LLM backend; custom and schedulable agents, attachments in chat (Redmine 7.0). Requires the companion [redmine_mcp](https://github.com/adhi-software/redmine_mcp) ![GitHub stars](https://img.shields.io/github/stars/adhi-software/redmine_mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F27-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/adhi-software/redmine_mcp?style=flat) plugin.
- [RedmineUP Agent](https://www.redmineup.com/pages/plugins/agent) - Plugin from RedmineUP (see the vendor page for licensing): drafts replies in the issue editor, summarizes issues / wiki pages / forum topics / versions, built-in MCP server for Claude, ChatGPT, Codex and Gemini CLI, and AI usage statistics (Redmine 7.0 / 6.1).

---

## MCP servers (AI agents → Redmine)

Connect any MCP-capable agent (Claude, Cursor, OpenCode, Cline, Continue, Qwen Code, …) to Redmine issues, projects, wikis, and time entries.

- [mcp-redmine](https://github.com/runekaagaard/mcp-redmine) ![GitHub stars](https://img.shields.io/github/stars/runekaagaard/mcp-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/runekaagaard/mcp-redmine?style=flat) - Covers close to 100% of the Redmine API (Python).
- [redmine-mcp-server (jztan)](https://github.com/jztan/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/jztan/redmine-mcp-server?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jztan/redmine-mcp-server?style=flat) - Issues, projects, wikis, time tracking, agile boards, CRM, and RedmineUP Helpdesk tickets, with OAuth2 multi-user support (Python).
- [mcp-server-redmine](https://github.com/yonaka15/mcp-server-redmine) ![GitHub stars](https://img.shields.io/github/stars/yonaka15/mcp-server-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/yonaka15/mcp-server-redmine?style=flat) - MCP server for Redmine (TypeScript).
- [redmine-cli](https://github.com/aarondpn/redmine-cli) ![GitHub stars](https://img.shields.io/github/stars/aarondpn/redmine-cli?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F15-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/aarondpn/redmine-cli?style=flat) - Redmine command-line client with agent Skills and MCP integration (Go).
- [redmine-mcp-server (onozaty)](https://github.com/onozaty/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/onozaty/redmine-mcp-server?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/onozaty/redmine-mcp-server?style=flat) - Comprehensive access to the Redmine REST API, including wiki page uploads (TypeScript).
- [agama-redmine-mcp](https://github.com/0xkillaflow/agama-redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/0xkillaflow/agama-redmine-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F28-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/0xkillaflow/agama-redmine-mcp?style=flat) - Work with issues using natural-language commands (TypeScript).
- [mcp-for-redmine](https://github.com/chspower1/mcp-for-redmine) ![GitHub stars](https://img.shields.io/github/stars/chspower1/mcp-for-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/chspower1/mcp-for-redmine?style=flat) - MCP server for Redmine (TypeScript).
- [mcp-redmine-oauth](https://github.com/tuzumkuru/mcp-redmine-oauth) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/mcp-redmine-oauth?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F14-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/tuzumkuru/mcp-redmine-oauth?style=flat) - MCP server with OAuth authentication; draft tools return a pre-filled Redmine form link so nothing is saved until the user submits it (Python).
- [redmine_mcp_plugin](https://github.com/joaoperfig/redmine_mcp_plugin) ![GitHub stars](https://img.shields.io/github/stars/joaoperfig/redmine_mcp_plugin?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/joaoperfig/redmine_mcp_plugin?style=flat) - Runs the MCP server inside Redmine as a plugin (Streamable HTTP at `/mcp`), using Redmine's own users, permissions and OAuth2 scopes; read-only by default (Redmine 6.1+, Ruby).
- [redmine-mcp (snowild)](https://github.com/snowild/redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/snowild/redmine-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F06%2F27-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/snowild/redmine-mcp?style=flat) - MCP server for Redmine integration (Python).
- [redmine-mcp (KalvadTech)](https://github.com/KalvadTech/redmine-mcp) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/KalvadTech/redmine-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F04-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/KalvadTech/redmine-mcp?style=flat) - Stateless MCP server: each user passes their own Redmine API key as a Bearer token, no database or shared secret; 59 tools covering issues, time entries, wiki, attachments and search, with a container image (Python).
- [redmine_mcp (hsbt)](https://github.com/hsbt/redmine_mcp) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/hsbt/redmine_mcp?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/hsbt/redmine_mcp?style=flat) - Plugin that adds an MCP endpoint to Redmine so AI coding agents (Claude Code and other MCP clients) can search, read, create and update issues and read wiki pages (Ruby).

---

## Local LLM stack

Run the AI side on your own hardware so issue data never leaves your network.

- [Ollama](https://ollama.com/) ![GitHub stars](https://img.shields.io/github/stars/ollama/ollama?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F10-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/ollama/ollama?style=flat) - Easiest local model runner with an OpenAI-compatible API (works with Redmine AI Helper's OpenAI-compatible provider). ([GitHub](https://github.com/ollama/ollama))
- [llama.cpp](https://github.com/ggml-org/llama.cpp) ![GitHub stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/ggml-org/llama.cpp?style=flat) - C/C++ inference engine with an OpenAI-compatible server (`llama-server`).
- [Qdrant](https://qdrant.tech/) ![GitHub stars](https://img.shields.io/github/stars/qdrant/qdrant?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qdrant/qdrant?style=flat) - Self-hostable vector database used by Redmine AI Helper for similar-issue search. ([GitHub](https://github.com/qdrant/qdrant))
- [OpenCode](https://opencode.ai/) ![GitHub stars](https://img.shields.io/github/stars/anomalyco/opencode?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F17-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/anomalyco/opencode?style=flat) - Open-source terminal coding agent; add a Redmine MCP server to read and update issues with a local model. ([GitHub](https://github.com/anomalyco/opencode))
- [Cline](https://cline.bot/) ![GitHub stars](https://img.shields.io/github/stars/cline/cline?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/cline/cline?style=flat) - Autonomous coding agent (VS Code / CLI) with MCP and Ollama support. ([GitHub](https://github.com/cline/cline))
- [Continue](https://github.com/continuedev/continue) ![GitHub stars](https://img.shields.io/github/stars/continuedev/continue?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/continuedev/continue?style=flat) - Open-source coding agent for IDEs and CLI with MCP support (company joined Cursor; the open-source code remains available).
- [Qwen Code](https://github.com/QwenLM/qwen-code) ![GitHub stars](https://img.shields.io/github/stars/QwenLM/qwen-code?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/QwenLM/qwen-code?style=flat) - Terminal coding agent tuned for Qwen3-Coder models, with MCP support.
- [Langfuse](https://langfuse.com/) ![GitHub stars](https://img.shields.io/github/stars/langfuse/langfuse?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/langfuse/langfuse?style=flat) - Self-hostable LLM observability; Redmine AI Helper can send traces to it. ([GitHub](https://github.com/langfuse/langfuse))

---

## Automation & workflows

- [n8n](https://n8n.io/) ![GitHub stars](https://img.shields.io/github/stars/n8n-io/n8n?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F20-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/n8n-io/n8n?style=flat) - Self-hostable workflow automation with native AI / MCP support; reach Redmine through its HTTP Request node and the REST API (e.g. new issue → local LLM triage → chat notification). ([GitHub](https://github.com/n8n-io/n8n))
- [Redmine Custom Workflows](https://github.com/anteo/redmine_custom_workflows) ![GitHub stars](https://img.shields.io/github/stars/anteo/redmine_custom_workflows?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F24-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/anteo/redmine_custom_workflows?style=flat) - Ruby hooks on issue / project events; a place to call an LLM API.
- [Redmine Periodic Task](https://github.com/jperelli/Redmine-Periodic-Task) ![GitHub stars](https://img.shields.io/github/stars/jperelli/Redmine-Periodic-Task?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F07-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jperelli/Redmine-Periodic-Task?style=flat) - Create recurring issues on a schedule.

---

## GitHub & chat integration

- [redmine_github_hook](https://github.com/koppen/redmine_github_hook) ![GitHub stars](https://img.shields.io/github/stars/koppen/redmine_github_hook?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2015%2F08%2F07-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/koppen/redmine_github_hook?style=flat) - Notifies Redmine when commits are pushed to GitHub, linking commits to issues.
- [redmine_github](https://github.com/agileware-jp/redmine_github) ![GitHub stars](https://img.shields.io/github/stars/agileware-jp/redmine_github?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/agileware-jp/redmine_github?style=flat) - Connects a local Redmine to a remote GitHub repository (Agileware, Japan).
- [Redmine Git Hosting](https://github.com/redmine-git-hosting/redmine_git_hosting) ![GitHub stars](https://img.shields.io/github/stars/redmine-git-hosting/redmine_git_hosting?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2022%2F09%2F29-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/redmine-git-hosting/redmine_git_hosting?style=flat) - Host Git repositories from Redmine.
- [redmine-slack](https://github.com/sciyoshi/redmine-slack) ![GitHub stars](https://img.shields.io/github/stars/sciyoshi/redmine-slack?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/sciyoshi/redmine-slack?style=flat) - Slack notifications for Redmine.

---

## API clients

Build your own LLM scripts or agents on top of the Redmine REST API.

- [python-redmine](https://github.com/maxtepkeev/python-redmine) ![GitHub stars](https://img.shields.io/github/stars/maxtepkeev/python-redmine?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F03%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/maxtepkeev/python-redmine?style=flat) - Python library for the Redmine API.
- [php-redmine-api](https://github.com/kbsali/php-redmine-api) ![GitHub stars](https://img.shields.io/github/stars/kbsali/php-redmine-api?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F26-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/kbsali/php-redmine-api?style=flat) - Object-oriented PHP client; v2.10 adds Redmine 7.0 support.
- [redmine-java-api](https://github.com/taskadapter/redmine-java-api) ![GitHub stars](https://img.shields.io/github/stars/taskadapter/redmine-java-api?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2013%2F11%2F27-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/taskadapter/redmine-java-api?style=flat) - Java client for the Redmine API.
- [arcli](https://github.com/mightymatth/arcli) ![GitHub stars](https://img.shields.io/github/stars/mightymatth/arcli?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2023%2F02%2F23-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/mightymatth/arcli?style=flat) - Redmine CLI (Go).

---

## Search & knowledge plugins (AI-friendly)

Good structure and search make Redmine data easier for AI to use.

- [Redmine Full Text Search](https://github.com/clear-code/redmine_full_text_search) ![GitHub stars](https://img.shields.io/github/stars/clear-code/redmine_full_text_search?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/clear-code/redmine_full_text_search?style=flat) - Fast full-text search with Groonga / PGroonga / Mroonga (strong Japanese support); v2.0.3 supports Redmine 7.0 and adds experimental semantic search on PostgreSQL + PGroonga.
- [Redmine Elasticsearch](https://github.com/Restream/redmine_elasticsearch) ![GitHub stars](https://img.shields.io/github/stars/Restream/redmine_elasticsearch?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Restream/redmine_elasticsearch?style=flat) - Full-text search via Elasticsearch.
- [Redmine Knowledgebase](https://github.com/alexbevi/redmine_knowledgebase) ![GitHub stars](https://img.shields.io/github/stars/alexbevi/redmine_knowledgebase?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F10%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/alexbevi/redmine_knowledgebase?style=flat) - Knowledge-base articles inside Redmine.
- [Additionals](https://github.com/alphanodes/additionals) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additionals?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/alphanodes/additionals?style=flat) - Dashboards, wiki macros, and a shared library for other plugins (AlphaNodes).
- [Additional Tags](https://github.com/alphanodes/additional_tags) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additional_tags?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/alphanodes/additional_tags?style=flat) - Tags for issues and wiki pages.

---

## Related lists

- [alexandermeindl/awesome-redmine](https://github.com/alexandermeindl/awesome-redmine) ![GitHub stars](https://img.shields.io/github/stars/alexandermeindl/awesome-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/alexandermeindl/awesome-redmine?style=flat) - General Redmine tools, plugins, and themes (not updated since 2022).
- [shvyac/awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-local-llm?style=flat) - Local LLM engines, apps, and agents.
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) ![GitHub stars](https://img.shields.io/github/stars/punkpeye/awesome-mcp-servers?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/punkpeye/awesome-mcp-servers?style=flat) - MCP servers of all kinds.
- [awesome-selfhosted/awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) ![GitHub stars](https://img.shields.io/github/stars/awesome-selfhosted/awesome-selfhosted?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2023%2F08%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/awesome-selfhosted/awesome-selfhosted?style=flat) - Self-hosted software in general.
- [sindresorhus/awesome](https://github.com/sindresorhus/awesome) ![GitHub stars](https://img.shields.io/github/stars/sindresorhus/awesome?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/sindresorhus/awesome?style=flat) - The Awesome meta-list.

---

## Contributing

Contributions welcome — open a pull request to add a resource, fix a broken link, or suggest a category.

Prefer **durable official / project URLs**, short blurbs, and actively maintained projects. Add a ⭐ star badge for GitHub projects, note the Redmine versions supported when known, and say whether a tool can run with a local LLM. Update both `README.md` and `README.ja.md` when you can.

---

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-ai-dev-tools](https://github.com/shvyac/awesome-ai-dev-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-dev-tools?style=flat&label=%E2%AD%90)
- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-automotive-cae](https://github.com/shvyac/awesome-automotive-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-automotive-cae?style=flat&label=%E2%AD%90)
- [awesome-automotive-todo-mcp](https://github.com/shvyac/awesome-automotive-todo-mcp) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-automotive-todo-mcp?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-hpc](https://github.com/shvyac/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-mcp-ai](https://github.com/shvyac/awesome-mcp-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-mcp-ai?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-quantum](https://github.com/shvyac/awesome-quantum) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-quantum?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
- [awesome-web-app-design](https://github.com/shvyac/awesome-web-app-design) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-web-app-design?style=flat&label=%E2%AD%90)
