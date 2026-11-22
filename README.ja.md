# Awesome Redmine AI（日本語）

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[English README](README.md)

**Redmine で AI を活用する**ためのリソースの厳選リストです。AI プラグイン、AI エージェントから Redmine のチケットを操作する MCP サーバー、ローカル LLM 構成、自動化、GitHub 連携、そしてそれらを支える API クライアントやプラグインをまとめています。できるだけ公式／プロジェクトの耐久性のある URL を優先しています。

**発見・学習用のリストです。** Redmine の AI 関連プロジェクトの多くは新しく小規模です。導入前に、お使いの Redmine のバージョンとの互換性と、LLM にどのデータが送られるかを確認してください。⭐ バッジは GitHub のスター数をリアルタイム表示します(shields.io)。release バッジは GitHub の最新リリース日(YYYY/MM/DD、最終更新時点)を示します。last commit バッジは最新コミット日をリアルタイム表示します(shields.io)。

## 目次

- [公式・ディストリビューション](#公式ディストリビューション)
- [AI プラグイン（Redmine 内で動作）](#ai-プラグインredmine-内で動作)
- [MCP サーバー（AI エージェント → Redmine）](#mcp-サーバーai-エージェント--redmine)
- [ローカル LLM 構成](#ローカル-llm-構成)
- [自動化・ワークフロー](#自動化ワークフロー)
- [GitHub・チャット連携](#githubチャット連携)
- [API クライアント](#api-クライアント)
- [検索・ナレッジ系プラグイン（AI と相性が良いもの）](#検索ナレッジ系プラグインai-と相性が良いもの)
- [関連リスト](#関連リスト)
- [コントリビューション](#コントリビューション)
- [shvyac の awesome リスト](#shvyac-の-awesome-リスト)

---

## 公式・ディストリビューション

- [Redmine（英語）](https://www.redmine.org/) ![GitHub stars](https://img.shields.io/github/stars/redmine/redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/redmine/redmine?style=flat) - オープンソースのプロジェクト管理・課題管理システム（Ruby on Rails）。（[GitHub ミラー](https://github.com/redmine/redmine)）
- [Redmine プラグインディレクトリ（英語）](https://www.redmine.org/plugins) - 公式のプラグイン一覧。
- [Redmine REST API（英語）](https://www.redmine.org/projects/redmine/wiki/Rest_api) - 公式 REST API ドキュメント。以下の MCP サーバーやクライアントはすべてこれを利用。
- [RedMica](https://www.redmica.jp/) ![GitHub stars](https://img.shields.io/github/stars/redmica/redmica?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F04-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/redmica/redmica?style=flat) - Redmine の次期バージョンの機能を先取りした互換ディストリビューション（ファーエンドテクノロジー）。（[GitHub](https://github.com/redmica/redmica)）
- [Redmine 公式 Docker イメージ（英語）](https://github.com/docker-library/redmine) ![GitHub stars](https://img.shields.io/github/stars/docker-library/redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/docker-library/redmine?style=flat) - 公式コンテナイメージ。AI 連携の検証環境づくりに便利。

---

## AI プラグイン（Redmine 内で動作）

- [Redmine AI Helper（英語）](https://github.com/haru/redmine_ai_helper) ![GitHub stars](https://img.shields.io/github/stars/haru/redmine_ai_helper?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/haru/redmine_ai_helper?style=flat) - 最も充実した AI プラグイン。AI チャット、チケット／Wiki の要約、サブタスク生成、入力補完、誤字チェック、リポジトリのコード説明、プロジェクト健全性レポート（グラフ付き、PDF／Markdown 出力）、Office 添付ファイルを Markdown として AI に渡す機能、MCP サーバー機能、Qdrant による類似・重複チケット検索。OpenAI 互換プロバイダー経由で Ollama を使えば完全オフライン運用も可能。
- [Redmine AI Summary（英語）](https://github.com/tuzumkuru/redmine_ai_summary) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/redmine_ai_summary?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F10%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/tuzumkuru/redmine_ai_summary?style=flat) - チケットの AI 要約を生成。
- [Redmine AI Assistant（英語）](https://github.com/carolcoral/redmine_ai_assistant) ![GitHub stars](https://img.shields.io/github/stars/carolcoral/redmine_ai_assistant?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/carolcoral/redmine_ai_assistant?style=flat) - 他の Redmine プラグインから共通で呼び出せる AI 機能の基盤。
- [Redmine GTT Assistant（英語）](https://github.com/gtt-project/redmine_gtt_assistant) ![GitHub stars](https://img.shields.io/github/stars/gtt-project/redmine_gtt_assistant?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/gtt-project/redmine_gtt_assistant?style=flat) - GTT（地理情報タスク管理）向け Redmine 構成用の「スマートアシスタント」。
- [Redmine Agent（英語）](https://github.com/adhi-software/redmine_agent) ![GitHub stars](https://img.shields.io/github/stars/adhi-software/redmine_agent?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/adhi-software/redmine_agent?style=flat) - 任意の LLM をバックエンドに設定し、自然言語で Redmine を問い合わせる AI エージェント。カスタムエージェント、定期実行エージェント、チャットへの添付ファイルに対応（Redmine 7.0）。併用プラグイン [redmine_mcp](https://github.com/adhi-software/redmine_mcp) ![GitHub stars](https://img.shields.io/github/stars/adhi-software/redmine_mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F27-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/adhi-software/redmine_mcp?style=flat) が必要。
- [RedmineUP Agent（英語）](https://www.redmineup.com/pages/plugins/agent) - RedmineUP 製のプラグイン（ライセンスはベンダーページを参照）。チケット編集画面での返信下書き、チケット／Wiki／フォーラム／バージョンの AI 要約、Claude・ChatGPT・Codex・Gemini CLI 向けの MCP サーバー内蔵、AI 利用統計（Redmine 7.0／6.1）。

---

## MCP サーバー（AI エージェント → Redmine）

MCP 対応のエージェント（Claude、Cursor、OpenCode、Cline、Continue、Qwen Code など）から、Redmine のチケット・プロジェクト・Wiki・作業時間を操作できます。

- [mcp-redmine（英語）](https://github.com/runekaagaard/mcp-redmine) ![GitHub stars](https://img.shields.io/github/stars/runekaagaard/mcp-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/runekaagaard/mcp-redmine?style=flat) - Redmine API のほぼ 100% をカバー（Python）。
- [redmine-mcp-server（jztan）（英語）](https://github.com/jztan/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/jztan/redmine-mcp-server?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jztan/redmine-mcp-server?style=flat) - チケット・プロジェクト・Wiki・工数・アジャイルボード・CRM・RedmineUP Helpdesk チケットに対応。OAuth2 による複数ユーザー対応（Python）。
- [mcp-server-redmine（英語）](https://github.com/yonaka15/mcp-server-redmine) ![GitHub stars](https://img.shields.io/github/stars/yonaka15/mcp-server-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/yonaka15/mcp-server-redmine?style=flat) - Redmine 用 MCP サーバー（TypeScript）。
- [redmine-cli（英語）](https://github.com/aarondpn/redmine-cli) ![GitHub stars](https://img.shields.io/github/stars/aarondpn/redmine-cli?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F15-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/aarondpn/redmine-cli?style=flat) - AI エージェント向け Skills と MCP 連携を備えた Redmine CLI（Go）。
- [redmine-mcp-server（onozaty）（英語）](https://github.com/onozaty/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/onozaty/redmine-mcp-server?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/onozaty/redmine-mcp-server?style=flat) - Redmine REST API を網羅的に扱える MCP サーバー。Wiki ページへのファイル添付にも対応（TypeScript）。
- [agama-redmine-mcp（英語）](https://github.com/0xkillaflow/agama-redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/0xkillaflow/agama-redmine-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F28-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/0xkillaflow/agama-redmine-mcp?style=flat) - 自然言語の指示でチケットを操作（TypeScript）。
- [mcp-for-redmine（英語）](https://github.com/chspower1/mcp-for-redmine) ![GitHub stars](https://img.shields.io/github/stars/chspower1/mcp-for-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/chspower1/mcp-for-redmine?style=flat) - Redmine 用 MCP サーバー（TypeScript）。
- [mcp-redmine-oauth（英語）](https://github.com/tuzumkuru/mcp-redmine-oauth) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/mcp-redmine-oauth?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F14-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/tuzumkuru/mcp-redmine-oauth?style=flat) - OAuth 認証対応の MCP サーバー。下書きツールは入力済みの Redmine フォームへのリンクを返し、ユーザーが送信するまで保存されない（Python）。
- [redmine_mcp_plugin（英語）](https://github.com/joaoperfig/redmine_mcp_plugin) ![GitHub stars](https://img.shields.io/github/stars/joaoperfig/redmine_mcp_plugin?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/joaoperfig/redmine_mcp_plugin?style=flat) - MCP サーバーを Redmine のプラグインとして動かす（`/mcp` で Streamable HTTP）。Redmine のユーザー・権限・OAuth2 スコープをそのまま使い、初期状態は読み取り専用（Redmine 6.1 以降、Ruby）。
- [redmine-mcp（snowild）（英語）](https://github.com/snowild/redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/snowild/redmine-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F06%2F27-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/snowild/redmine-mcp?style=flat) - Redmine 連携用 MCP サーバー（Python）。
- [redmine-mcp（KalvadTech）（英語）](https://github.com/KalvadTech/redmine-mcp) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/KalvadTech/redmine-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F04-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/KalvadTech/redmine-mcp?style=flat) - ステートレスな MCP サーバー。各ユーザーが自分の Redmine API キーを Bearer トークンで渡し、DB・共有シークレットなし。チケット・工数・Wiki・添付・検索など 59 ツール、Docker イメージあり（Python）。
- [redmine_mcp（hsbt）（英語）](https://github.com/hsbt/redmine_mcp) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/hsbt/redmine_mcp?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/hsbt/redmine_mcp?style=flat) - Redmine に MCP エンドポイントを追加するプラグイン。Claude Code などの AI エージェントからチケットの検索・閲覧・作成・更新と Wiki ページの閲覧ができる（Ruby）。

---

## ローカル LLM 構成

AI 側を手元のハードウェアで動かし、チケットのデータを社外に出さない構成。

- [Ollama（英語）](https://ollama.com/) ![GitHub stars](https://img.shields.io/github/stars/ollama/ollama?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F10-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/ollama/ollama?style=flat) - OpenAI 互換 API を持つ最も手軽なローカルモデル実行環境（Redmine AI Helper の OpenAI 互換プロバイダーで利用可能）。（[GitHub](https://github.com/ollama/ollama)）
- [llama.cpp（英語）](https://github.com/ggml-org/llama.cpp) ![GitHub stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/ggml-org/llama.cpp?style=flat) - OpenAI 互換サーバー（`llama-server`）付きの C/C++ 推論エンジン。
- [Qdrant（英語）](https://qdrant.tech/) ![GitHub stars](https://img.shields.io/github/stars/qdrant/qdrant?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qdrant/qdrant?style=flat) - セルフホスト可能なベクトル DB。Redmine AI Helper の類似チケット検索で使用。（[GitHub](https://github.com/qdrant/qdrant)）
- [OpenCode（英語）](https://opencode.ai/) ![GitHub stars](https://img.shields.io/github/stars/anomalyco/opencode?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F17-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/anomalyco/opencode?style=flat) - オープンソースのターミナル型コーディングエージェント。Redmine 用 MCP サーバーを追加すれば、ローカルモデルでチケットの参照・更新が可能。（[GitHub](https://github.com/anomalyco/opencode)）
- [Cline（英語）](https://cline.bot/) ![GitHub stars](https://img.shields.io/github/stars/cline/cline?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/cline/cline?style=flat) - MCP と Ollama に対応した自律型コーディングエージェント（VS Code／CLI）。（[GitHub](https://github.com/cline/cline)）
- [Continue（英語）](https://github.com/continuedev/continue) ![GitHub stars](https://img.shields.io/github/stars/continuedev/continue?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/continuedev/continue?style=flat) - MCP 対応の IDE／CLI 向けオープンソースコーディングエージェント（開発元は Cursor に合流。オープンソースのコードは引き続き公開）。
- [Qwen Code（英語）](https://github.com/QwenLM/qwen-code) ![GitHub stars](https://img.shields.io/github/stars/QwenLM/qwen-code?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/QwenLM/qwen-code?style=flat) - Qwen3-Coder 向けに調整されたターミナル型コーディングエージェント。MCP 対応。
- [Langfuse（英語）](https://langfuse.com/) ![GitHub stars](https://img.shields.io/github/stars/langfuse/langfuse?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/langfuse/langfuse?style=flat) - セルフホスト可能な LLM 監視・評価基盤。Redmine AI Helper の利用状況を記録可能。（[GitHub](https://github.com/langfuse/langfuse)）

---

## 自動化・ワークフロー

- [n8n（英語）](https://n8n.io/) ![GitHub stars](https://img.shields.io/github/stars/n8n-io/n8n?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F20-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/n8n-io/n8n?style=flat) - AI／MCP 機能を備えたセルフホスト可能なワークフロー自動化ツール。HTTP Request ノードと REST API で Redmine と連携（例: 新規チケット → ローカル LLM で分類 → チャット通知）。（[GitHub](https://github.com/n8n-io/n8n)）
- [Redmine Custom Workflows（英語）](https://github.com/anteo/redmine_custom_workflows) ![GitHub stars](https://img.shields.io/github/stars/anteo/redmine_custom_workflows?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F24-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/anteo/redmine_custom_workflows?style=flat) - チケットやプロジェクトのイベントに Ruby の処理を追加。LLM API を呼び出す場所として使える。
- [Redmine Periodic Task（英語）](https://github.com/jperelli/Redmine-Periodic-Task) ![GitHub stars](https://img.shields.io/github/stars/jperelli/Redmine-Periodic-Task?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F07-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jperelli/Redmine-Periodic-Task?style=flat) - 定期的にチケットを自動作成。

---

## GitHub・チャット連携

- [redmine_github_hook（英語）](https://github.com/koppen/redmine_github_hook) ![GitHub stars](https://img.shields.io/github/stars/koppen/redmine_github_hook?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2015%2F08%2F07-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/koppen/redmine_github_hook?style=flat) - GitHub への push を Redmine に通知し、コミットとチケットを紐づけ。
- [redmine_github](https://github.com/agileware-jp/redmine_github) ![GitHub stars](https://img.shields.io/github/stars/agileware-jp/redmine_github?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/agileware-jp/redmine_github?style=flat) - 手元の Redmine とリモートの GitHub リポジトリを接続（アジャイルウェア）。
- [Redmine Git Hosting（英語）](https://github.com/redmine-git-hosting/redmine_git_hosting) ![GitHub stars](https://img.shields.io/github/stars/redmine-git-hosting/redmine_git_hosting?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2022%2F09%2F29-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/redmine-git-hosting/redmine_git_hosting?style=flat) - Redmine から Git リポジトリをホスティング。
- [redmine-slack（英語）](https://github.com/sciyoshi/redmine-slack) ![GitHub stars](https://img.shields.io/github/stars/sciyoshi/redmine-slack?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/sciyoshi/redmine-slack?style=flat) - Redmine の更新を Slack に通知。

---

## API クライアント

Redmine REST API の上に、自作の LLM スクリプトやエージェントを作る場合に。

- [python-redmine（英語）](https://github.com/maxtepkeev/python-redmine) ![GitHub stars](https://img.shields.io/github/stars/maxtepkeev/python-redmine?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F03%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/maxtepkeev/python-redmine?style=flat) - Redmine API 用 Python ライブラリ。
- [php-redmine-api（英語）](https://github.com/kbsali/php-redmine-api) ![GitHub stars](https://img.shields.io/github/stars/kbsali/php-redmine-api?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F26-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/kbsali/php-redmine-api?style=flat) - オブジェクト指向の PHP クライアント。v2.10 で Redmine 7.0 に対応。
- [redmine-java-api（英語）](https://github.com/taskadapter/redmine-java-api) ![GitHub stars](https://img.shields.io/github/stars/taskadapter/redmine-java-api?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2013%2F11%2F27-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/taskadapter/redmine-java-api?style=flat) - Redmine API 用 Java クライアント。
- [arcli（英語）](https://github.com/mightymatth/arcli) ![GitHub stars](https://img.shields.io/github/stars/mightymatth/arcli?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2023%2F02%2F23-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/mightymatth/arcli?style=flat) - Redmine CLI（Go）。

---

## 検索・ナレッジ系プラグイン（AI と相性が良いもの）

データが整理され検索しやすいほど、AI も Redmine の情報を活用しやすくなります。

- [Redmine Full Text Search](https://github.com/clear-code/redmine_full_text_search) ![GitHub stars](https://img.shields.io/github/stars/clear-code/redmine_full_text_search?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/clear-code/redmine_full_text_search?style=flat) - Groonga／PGroonga／Mroonga による高速全文検索（日本語に強い。クリアコード）。v2.0.3 で Redmine 7.0 に対応し、PostgreSQL + PGroonga での実験的なセマンティック検索を追加。
- [Redmine Elasticsearch（英語）](https://github.com/Restream/redmine_elasticsearch) ![GitHub stars](https://img.shields.io/github/stars/Restream/redmine_elasticsearch?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Restream/redmine_elasticsearch?style=flat) - Elasticsearch による全文検索。
- [Redmine Knowledgebase（英語）](https://github.com/alexbevi/redmine_knowledgebase) ![GitHub stars](https://img.shields.io/github/stars/alexbevi/redmine_knowledgebase?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F10%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/alexbevi/redmine_knowledgebase?style=flat) - Redmine 内のナレッジベース記事。
- [Additionals（英語）](https://github.com/alphanodes/additionals) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additionals?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/alphanodes/additionals?style=flat) - ダッシュボード、Wiki マクロ、他プラグイン用の共通ライブラリ（AlphaNodes）。
- [Additional Tags（英語）](https://github.com/alphanodes/additional_tags) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additional_tags?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/alphanodes/additional_tags?style=flat) - チケットと Wiki ページにタグを追加。

---

## 関連リスト

- [alexandermeindl/awesome-redmine（英語）](https://github.com/alexandermeindl/awesome-redmine) ![GitHub stars](https://img.shields.io/github/stars/alexandermeindl/awesome-redmine?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/alexandermeindl/awesome-redmine?style=flat) - Redmine 全般のツール・プラグイン・テーマ（2022年以降更新なし）。
- [shvyac/awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-local-llm?style=flat) - ローカル LLM のエンジン・アプリ・エージェント集。
- [punkpeye/awesome-mcp-servers（英語）](https://github.com/punkpeye/awesome-mcp-servers) ![GitHub stars](https://img.shields.io/github/stars/punkpeye/awesome-mcp-servers?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/punkpeye/awesome-mcp-servers?style=flat) - あらゆる種類の MCP サーバー集。
- [awesome-selfhosted/awesome-selfhosted（英語）](https://github.com/awesome-selfhosted/awesome-selfhosted) ![GitHub stars](https://img.shields.io/github/stars/awesome-selfhosted/awesome-selfhosted?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2023%2F08%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/awesome-selfhosted/awesome-selfhosted?style=flat) - セルフホスト用ソフト全般。
- [sindresorhus/awesome（英語）](https://github.com/sindresorhus/awesome) ![GitHub stars](https://img.shields.io/github/stars/sindresorhus/awesome?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/sindresorhus/awesome?style=flat) - Awesome のメタリスト。

---

## コントリビューション

コントリビューション歓迎です。リソース追加、リンク切れ修正、カテゴリ提案はプルリクエストでどうぞ。

**公式／プロジェクトの耐久性のある URL**、短い説明、継続的にメンテナンスされているプロジェクトを優先してください。GitHub のプロジェクトには ⭐ スター数バッジを付け、分かる範囲で対応する Redmine のバージョンと、ローカル LLM で動かせるかどうかを明記してください。可能なら `README.md` と `README.ja.md` の両方を更新してください。

---

## shvyac の awesome リスト

[shvyac](https://github.com/shvyac) が管理しているキュレーションリストの一覧:

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
