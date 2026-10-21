# Awesome Redmine AI

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

A curated list of resources for using **AI with Redmine** — AI plugins, MCP servers that let AI agents work with Redmine issues, local LLM setups, automation, GitHub integration, and the API clients and plugins that make it all work. Prefer durable official / project URLs.

**Discovery list only** — most Redmine AI projects are young and small; check compatibility with your Redmine version and review what data is sent to an LLM before installing. ⭐ badges show live GitHub star counts (via shields.io).

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

- [Redmine](https://www.redmine.org/) ![GitHub stars](https://img.shields.io/github/stars/redmine/redmine?style=flat&label=%E2%AD%90) - Flexible open-source project management and issue tracking (Ruby on Rails). ([GitHub mirror](https://github.com/redmine/redmine))
- [Redmine Plugins Directory](https://www.redmine.org/plugins) - Official plugin directory.
- [Redmine REST API](https://www.redmine.org/projects/redmine/wiki/Rest_api) - Official REST API documentation, used by every MCP server and client below.
- [RedMica](https://www.redmica.jp/) ![GitHub stars](https://img.shields.io/github/stars/redmica/redmica?style=flat&label=%E2%AD%90) - Redmine-compatible distribution that ships upcoming Redmine features early (Japan). ([GitHub](https://github.com/redmica/redmica))
- [Docker Official Image for Redmine](https://github.com/docker-library/redmine) ![GitHub stars](https://img.shields.io/github/stars/docker-library/redmine?style=flat&label=%E2%AD%90) - Official container image; handy for a local AI test environment.

---

## AI plugins (inside Redmine)

- [Redmine AI Helper](https://github.com/haru/redmine_ai_helper) ![GitHub stars](https://img.shields.io/github/stars/haru/redmine_ai_helper?style=flat&label=%E2%AD%90) - The most complete AI plugin: chat sidebar, issue / wiki summaries, subtask generation, inline completion, typo checks, repository code explanation, project health reports, built-in MCP server, and Qdrant vector search for similar / duplicate issues. Can run fully offline with Ollama via the OpenAI-compatible provider.
- [Redmine AI Summary](https://github.com/tuzumkuru/redmine_ai_summary) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/redmine_ai_summary?style=flat&label=%E2%AD%90) - Generates AI summaries of issues.
- [Redmine AI Assistant](https://github.com/carolcoral/redmine_ai_assistant) ![GitHub stars](https://img.shields.io/github/stars/carolcoral/redmine_ai_assistant?style=flat&label=%E2%AD%90) - Unified AI capability hub that other Redmine plugins can call.
- [Redmine GTT Assistant](https://github.com/gtt-project/redmine_gtt_assistant) ![GitHub stars](https://img.shields.io/github/stars/gtt-project/redmine_gtt_assistant?style=flat&label=%E2%AD%90) - "Smart assistant" for the GTT (geo-task-tracker) Redmine stack.

---

## MCP servers (AI agents → Redmine)

Connect any MCP-capable agent (Claude, Cursor, OpenCode, Cline, Continue, Qwen Code, …) to Redmine issues, projects, wikis, and time entries.

- [mcp-redmine](https://github.com/runekaagaard/mcp-redmine) ![GitHub stars](https://img.shields.io/github/stars/runekaagaard/mcp-redmine?style=flat&label=%E2%AD%90) - Covers close to 100% of the Redmine API (Python).
- [redmine-mcp-server (jztan)](https://github.com/jztan/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/jztan/redmine-mcp-server?style=flat&label=%E2%AD%90) - Issues, projects, wikis, time tracking, agile boards, and CRM, with OAuth2 multi-user support (Python).
- [mcp-server-redmine](https://github.com/yonaka15/mcp-server-redmine) ![GitHub stars](https://img.shields.io/github/stars/yonaka15/mcp-server-redmine?style=flat&label=%E2%AD%90) - MCP server for Redmine (TypeScript).
- [redmine-cli](https://github.com/aarondpn/redmine-cli) ![GitHub stars](https://img.shields.io/github/stars/aarondpn/redmine-cli?style=flat&label=%E2%AD%90) - Redmine command-line client with agent Skills and MCP integration (Go).
- [redmine-mcp-server (onozaty)](https://github.com/onozaty/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/onozaty/redmine-mcp-server?style=flat&label=%E2%AD%90) - Comprehensive access to the Redmine REST API (JavaScript).
- [agama-redmine-mcp](https://github.com/0xkillaflow/agama-redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/0xkillaflow/agama-redmine-mcp?style=flat&label=%E2%AD%90) - Work with issues using natural-language commands (TypeScript).
- [mcp-for-redmine](https://github.com/chspower1/mcp-for-redmine) ![GitHub stars](https://img.shields.io/github/stars/chspower1/mcp-for-redmine?style=flat&label=%E2%AD%90) - MCP server for Redmine (TypeScript).
- [mcp-redmine-oauth](https://github.com/tuzumkuru/mcp-redmine-oauth) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/mcp-redmine-oauth?style=flat&label=%E2%AD%90) - MCP server with OAuth authentication (Python).
- [redmine-mcp (snowild)](https://github.com/snowild/redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/snowild/redmine-mcp?style=flat&label=%E2%AD%90) - MCP server for Redmine integration (Python).

---

## Local LLM stack

Run the AI side on your own hardware so issue data never leaves your network.

- [Ollama](https://ollama.com/) ![GitHub stars](https://img.shields.io/github/stars/ollama/ollama?style=flat&label=%E2%AD%90) - Easiest local model runner with an OpenAI-compatible API (works with Redmine AI Helper's OpenAI-compatible provider). ([GitHub](https://github.com/ollama/ollama))
- [llama.cpp](https://github.com/ggml-org/llama.cpp) ![GitHub stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=flat&label=%E2%AD%90) - C/C++ inference engine with an OpenAI-compatible server (`llama-server`).
- [Qdrant](https://qdrant.tech/) ![GitHub stars](https://img.shields.io/github/stars/qdrant/qdrant?style=flat&label=%E2%AD%90) - Self-hostable vector database used by Redmine AI Helper for similar-issue search. ([GitHub](https://github.com/qdrant/qdrant))
- [OpenCode](https://opencode.ai/) ![GitHub stars](https://img.shields.io/github/stars/anomalyco/opencode?style=flat&label=%E2%AD%90) - Open-source terminal coding agent; add a Redmine MCP server to read and update issues with a local model. ([GitHub](https://github.com/anomalyco/opencode))
- [Cline](https://cline.bot/) ![GitHub stars](https://img.shields.io/github/stars/cline/cline?style=flat&label=%E2%AD%90) - Autonomous coding agent (VS Code / CLI) with MCP and Ollama support. ([GitHub](https://github.com/cline/cline))
- [Continue](https://github.com/continuedev/continue) ![GitHub stars](https://img.shields.io/github/stars/continuedev/continue?style=flat&label=%E2%AD%90) - Open-source coding agent for IDEs and CLI with MCP support (company joined Cursor; the open-source code remains available).
- [Qwen Code](https://github.com/QwenLM/qwen-code) ![GitHub stars](https://img.shields.io/github/stars/QwenLM/qwen-code?style=flat&label=%E2%AD%90) - Terminal coding agent tuned for Qwen3-Coder models, with MCP support.
- [Langfuse](https://langfuse.com/) ![GitHub stars](https://img.shields.io/github/stars/langfuse/langfuse?style=flat&label=%E2%AD%90) - Self-hostable LLM observability; Redmine AI Helper can send traces to it. ([GitHub](https://github.com/langfuse/langfuse))

---

## Automation & workflows

- [n8n](https://n8n.io/) ![GitHub stars](https://img.shields.io/github/stars/n8n-io/n8n?style=flat&label=%E2%AD%90) - Self-hostable workflow automation with native AI / MCP support; reach Redmine through its HTTP Request node and the REST API (e.g. new issue → local LLM triage → chat notification). ([GitHub](https://github.com/n8n-io/n8n))
- [Redmine Custom Workflows](https://github.com/anteo/redmine_custom_workflows) ![GitHub stars](https://img.shields.io/github/stars/anteo/redmine_custom_workflows?style=flat&label=%E2%AD%90) - Ruby hooks on issue / project events; a place to call an LLM API.
- [Redmine Periodic Task](https://github.com/jperelli/Redmine-Periodic-Task) ![GitHub stars](https://img.shields.io/github/stars/jperelli/Redmine-Periodic-Task?style=flat&label=%E2%AD%90) - Create recurring issues on a schedule.

---

## GitHub & chat integration

- [redmine_github_hook](https://github.com/koppen/redmine_github_hook) ![GitHub stars](https://img.shields.io/github/stars/koppen/redmine_github_hook?style=flat&label=%E2%AD%90) - Notifies Redmine when commits are pushed to GitHub, linking commits to issues.
- [redmine_github](https://github.com/agileware-jp/redmine_github) ![GitHub stars](https://img.shields.io/github/stars/agileware-jp/redmine_github?style=flat&label=%E2%AD%90) - Connects a local Redmine to a remote GitHub repository (Agileware, Japan).
- [Redmine Git Hosting](https://github.com/redmine-git-hosting/redmine_git_hosting) ![GitHub stars](https://img.shields.io/github/stars/redmine-git-hosting/redmine_git_hosting?style=flat&label=%E2%AD%90) - Host Git repositories from Redmine.
- [redmine-slack](https://github.com/sciyoshi/redmine-slack) ![GitHub stars](https://img.shields.io/github/stars/sciyoshi/redmine-slack?style=flat&label=%E2%AD%90) - Slack notifications for Redmine.

---

## API clients

Build your own LLM scripts or agents on top of the Redmine REST API.

- [python-redmine](https://github.com/maxtepkeev/python-redmine) ![GitHub stars](https://img.shields.io/github/stars/maxtepkeev/python-redmine?style=flat&label=%E2%AD%90) - Python library for the Redmine API.
- [php-redmine-api](https://github.com/kbsali/php-redmine-api) ![GitHub stars](https://img.shields.io/github/stars/kbsali/php-redmine-api?style=flat&label=%E2%AD%90) - Object-oriented PHP client (looking for a maintainer).
- [redmine-java-api](https://github.com/taskadapter/redmine-java-api) ![GitHub stars](https://img.shields.io/github/stars/taskadapter/redmine-java-api?style=flat&label=%E2%AD%90) - Java client for the Redmine API.
- [arcli](https://github.com/mightymatth/arcli) ![GitHub stars](https://img.shields.io/github/stars/mightymatth/arcli?style=flat&label=%E2%AD%90) - Redmine CLI (Go).

---

## Search & knowledge plugins (AI-friendly)

Good structure and search make Redmine data easier for AI to use.

- [Redmine Full Text Search](https://github.com/clear-code/redmine_full_text_search) ![GitHub stars](https://img.shields.io/github/stars/clear-code/redmine_full_text_search?style=flat&label=%E2%AD%90) - Fast full-text search with Groonga / PGroonga / Mroonga (strong Japanese support).
- [Redmine Elasticsearch](https://github.com/Restream/redmine_elasticsearch) ![GitHub stars](https://img.shields.io/github/stars/Restream/redmine_elasticsearch?style=flat&label=%E2%AD%90) - Full-text search via Elasticsearch.
- [Redmine Knowledgebase](https://github.com/alexbevi/redmine_knowledgebase) ![GitHub stars](https://img.shields.io/github/stars/alexbevi/redmine_knowledgebase?style=flat&label=%E2%AD%90) - Knowledge-base articles inside Redmine.
- [Additionals](https://github.com/alphanodes/additionals) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additionals?style=flat&label=%E2%AD%90) - Dashboards, wiki macros, and a shared library for other plugins (AlphaNodes).
- [Additional Tags](https://github.com/alphanodes/additional_tags) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additional_tags?style=flat&label=%E2%AD%90) - Tags for issues and wiki pages.

---

## Related lists

- [alexandermeindl/awesome-redmine](https://github.com/alexandermeindl/awesome-redmine) ![GitHub stars](https://img.shields.io/github/stars/alexandermeindl/awesome-redmine?style=flat&label=%E2%AD%90) - General Redmine tools, plugins, and themes (not updated since 2022).
- [shvyac/awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90) - Local LLM engines, apps, and agents.
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) ![GitHub stars](https://img.shields.io/github/stars/punkpeye/awesome-mcp-servers?style=flat&label=%E2%AD%90) - MCP servers of all kinds.
- [awesome-selfhosted/awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) ![GitHub stars](https://img.shields.io/github/stars/awesome-selfhosted/awesome-selfhosted?style=flat&label=%E2%AD%90) - Self-hosted software in general.
- [sindresorhus/awesome](https://github.com/sindresorhus/awesome) ![GitHub stars](https://img.shields.io/github/stars/sindresorhus/awesome?style=flat&label=%E2%AD%90) - The Awesome meta-list.

---

## Contributing

Contributions welcome — open a pull request to add a resource, fix a broken link, or suggest a category.

Prefer **durable official / project URLs**, short blurbs, and actively maintained projects. Add a ⭐ star badge for GitHub projects, note the Redmine versions supported when known, and say whether a tool can run with a local LLM. Update both `README.md` and `README.ja.md` when you can.

---

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
