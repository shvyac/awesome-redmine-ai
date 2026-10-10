# Awesome Redmine AI（日本語）

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[English README](README.md)

**Redmine で AI を活用する**ためのリソースの厳選リストです。AI プラグイン、AI エージェントから Redmine のチケットを操作する MCP サーバー、ローカル LLM 構成、自動化、GitHub 連携、そしてそれらを支える API クライアントやプラグインをまとめています。できるだけ公式／プロジェクトの耐久性のある URL を優先しています。

**発見・学習用のリストです。** Redmine の AI 関連プロジェクトの多くは新しく小規模です。導入前に、お使いの Redmine のバージョンとの互換性と、LLM にどのデータが送られるかを確認してください。⭐ バッジは GitHub のスター数をリアルタイム表示します（shields.io）。

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

---

## 公式・ディストリビューション

- [Redmine（英語）](https://www.redmine.org/) ![GitHub stars](https://img.shields.io/github/stars/redmine/redmine?style=flat&label=%E2%AD%90) - オープンソースのプロジェクト管理・課題管理システム（Ruby on Rails）。（[GitHub ミラー](https://github.com/redmine/redmine)）
- [Redmine プラグインディレクトリ（英語）](https://www.redmine.org/plugins) - 公式のプラグイン一覧。
- [Redmine REST API（英語）](https://www.redmine.org/projects/redmine/wiki/Rest_api) - 公式 REST API ドキュメント。以下の MCP サーバーやクライアントはすべてこれを利用。
- [RedMica](https://www.redmica.jp/) ![GitHub stars](https://img.shields.io/github/stars/redmica/redmica?style=flat&label=%E2%AD%90) - Redmine の次期バージョンの機能を先取りした互換ディストリビューション（ファーエンドテクノロジー）。（[GitHub](https://github.com/redmica/redmica)）
- [Redmine 公式 Docker イメージ（英語）](https://github.com/docker-library/redmine) ![GitHub stars](https://img.shields.io/github/stars/docker-library/redmine?style=flat&label=%E2%AD%90) - 公式コンテナイメージ。AI 連携の検証環境づくりに便利。

---

## AI プラグイン（Redmine 内で動作）

- [Redmine AI Helper（英語）](https://github.com/haru/redmine_ai_helper) ![GitHub stars](https://img.shields.io/github/stars/haru/redmine_ai_helper?style=flat&label=%E2%AD%90) - 最も充実した AI プラグイン。AI チャット、チケット／Wiki の要約、サブタスク生成、入力補完、誤字チェック、リポジトリのコード説明、プロジェクト健全性レポート、MCP サーバー機能、Qdrant による類似・重複チケット検索。OpenAI 互換プロバイダー経由で Ollama を使えば完全オフライン運用も可能。
- [Redmine AI Summary（英語）](https://github.com/tuzumkuru/redmine_ai_summary) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/redmine_ai_summary?style=flat&label=%E2%AD%90) - チケットの AI 要約を生成。
- [Redmine AI Assistant（英語）](https://github.com/carolcoral/redmine_ai_assistant) ![GitHub stars](https://img.shields.io/github/stars/carolcoral/redmine_ai_assistant?style=flat&label=%E2%AD%90) - 他の Redmine プラグインから共通で呼び出せる AI 機能の基盤。
- [Redmine GTT Assistant（英語）](https://github.com/gtt-project/redmine_gtt_assistant) ![GitHub stars](https://img.shields.io/github/stars/gtt-project/redmine_gtt_assistant?style=flat&label=%E2%AD%90) - GTT（地理情報タスク管理）向け Redmine 構成用の「スマートアシスタント」。

---

## MCP サーバー（AI エージェント → Redmine）

MCP 対応のエージェント（Claude、Cursor、OpenCode、Cline、Continue、Qwen Code など）から、Redmine のチケット・プロジェクト・Wiki・作業時間を操作できます。

- [mcp-redmine（英語）](https://github.com/runekaagaard/mcp-redmine) ![GitHub stars](https://img.shields.io/github/stars/runekaagaard/mcp-redmine?style=flat&label=%E2%AD%90) - Redmine API のほぼ 100% をカバー（Python）。
- [redmine-mcp-server（jztan）（英語）](https://github.com/jztan/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/jztan/redmine-mcp-server?style=flat&label=%E2%AD%90) - チケット・プロジェクト・Wiki・工数・アジャイルボード・CRM に対応。OAuth2 による複数ユーザー対応（Python）。
- [mcp-server-redmine（英語）](https://github.com/yonaka15/mcp-server-redmine) ![GitHub stars](https://img.shields.io/github/stars/yonaka15/mcp-server-redmine?style=flat&label=%E2%AD%90) - Redmine 用 MCP サーバー（TypeScript）。
- [redmine-cli（英語）](https://github.com/aarondpn/redmine-cli) ![GitHub stars](https://img.shields.io/github/stars/aarondpn/redmine-cli?style=flat&label=%E2%AD%90) - AI エージェント向け Skills と MCP 連携を備えた Redmine CLI（Go）。
- [redmine-mcp-server（onozaty）（英語）](https://github.com/onozaty/redmine-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/onozaty/redmine-mcp-server?style=flat&label=%E2%AD%90) - Redmine REST API を網羅的に扱える MCP サーバー（JavaScript）。
- [agama-redmine-mcp（英語）](https://github.com/0xkillaflow/agama-redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/0xkillaflow/agama-redmine-mcp?style=flat&label=%E2%AD%90) - 自然言語の指示でチケットを操作（TypeScript）。
- [mcp-for-redmine（英語）](https://github.com/chspower1/mcp-for-redmine) ![GitHub stars](https://img.shields.io/github/stars/chspower1/mcp-for-redmine?style=flat&label=%E2%AD%90) - Redmine 用 MCP サーバー（TypeScript）。
- [mcp-redmine-oauth（英語）](https://github.com/tuzumkuru/mcp-redmine-oauth) ![GitHub stars](https://img.shields.io/github/stars/tuzumkuru/mcp-redmine-oauth?style=flat&label=%E2%AD%90) - OAuth 認証対応の MCP サーバー（Python）。
- [redmine-mcp（snowild）（英語）](https://github.com/snowild/redmine-mcp) ![GitHub stars](https://img.shields.io/github/stars/snowild/redmine-mcp?style=flat&label=%E2%AD%90) - Redmine 連携用 MCP サーバー（Python）。

---

## ローカル LLM 構成

AI 側を手元のハードウェアで動かし、チケットのデータを社外に出さない構成。

- [Ollama（英語）](https://ollama.com/) ![GitHub stars](https://img.shields.io/github/stars/ollama/ollama?style=flat&label=%E2%AD%90) - OpenAI 互換 API を持つ最も手軽なローカルモデル実行環境（Redmine AI Helper の OpenAI 互換プロバイダーで利用可能）。（[GitHub](https://github.com/ollama/ollama)）
- [llama.cpp（英語）](https://github.com/ggml-org/llama.cpp) ![GitHub stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=flat&label=%E2%AD%90) - OpenAI 互換サーバー（`llama-server`）付きの C/C++ 推論エンジン。
- [Qdrant（英語）](https://qdrant.tech/) ![GitHub stars](https://img.shields.io/github/stars/qdrant/qdrant?style=flat&label=%E2%AD%90) - セルフホスト可能なベクトル DB。Redmine AI Helper の類似チケット検索で使用。（[GitHub](https://github.com/qdrant/qdrant)）
- [OpenCode（英語）](https://opencode.ai/) ![GitHub stars](https://img.shields.io/github/stars/anomalyco/opencode?style=flat&label=%E2%AD%90) - オープンソースのターミナル型コーディングエージェント。Redmine 用 MCP サーバーを追加すれば、ローカルモデルでチケットの参照・更新が可能。（[GitHub](https://github.com/anomalyco/opencode)）
- [Cline（英語）](https://cline.bot/) ![GitHub stars](https://img.shields.io/github/stars/cline/cline?style=flat&label=%E2%AD%90) - MCP と Ollama に対応した自律型コーディングエージェント（VS Code／CLI）。（[GitHub](https://github.com/cline/cline)）
- [Continue（英語）](https://github.com/continuedev/continue) ![GitHub stars](https://img.shields.io/github/stars/continuedev/continue?style=flat&label=%E2%AD%90) - MCP 対応の IDE／CLI 向けオープンソースコーディングエージェント（開発元は Cursor に合流。オープンソースのコードは引き続き公開）。
- [Qwen Code（英語）](https://github.com/QwenLM/qwen-code) ![GitHub stars](https://img.shields.io/github/stars/QwenLM/qwen-code?style=flat&label=%E2%AD%90) - Qwen3-Coder 向けに調整されたターミナル型コーディングエージェント。MCP 対応。
- [Langfuse（英語）](https://langfuse.com/) ![GitHub stars](https://img.shields.io/github/stars/langfuse/langfuse?style=flat&label=%E2%AD%90) - セルフホスト可能な LLM 監視・評価基盤。Redmine AI Helper の利用状況を記録可能。（[GitHub](https://github.com/langfuse/langfuse)）

---

## 自動化・ワークフロー

- [n8n（英語）](https://n8n.io/) ![GitHub stars](https://img.shields.io/github/stars/n8n-io/n8n?style=flat&label=%E2%AD%90) - AI／MCP 機能を備えたセルフホスト可能なワークフロー自動化ツール。HTTP Request ノードと REST API で Redmine と連携（例: 新規チケット → ローカル LLM で分類 → チャット通知）。（[GitHub](https://github.com/n8n-io/n8n)）
- [Redmine Custom Workflows（英語）](https://github.com/anteo/redmine_custom_workflows) ![GitHub stars](https://img.shields.io/github/stars/anteo/redmine_custom_workflows?style=flat&label=%E2%AD%90) - チケットやプロジェクトのイベントに Ruby の処理を追加。LLM API を呼び出す場所として使える。
- [Redmine Periodic Task（英語）](https://github.com/jperelli/Redmine-Periodic-Task) ![GitHub stars](https://img.shields.io/github/stars/jperelli/Redmine-Periodic-Task?style=flat&label=%E2%AD%90) - 定期的にチケットを自動作成。

---

## GitHub・チャット連携

- [redmine_github_hook（英語）](https://github.com/koppen/redmine_github_hook) ![GitHub stars](https://img.shields.io/github/stars/koppen/redmine_github_hook?style=flat&label=%E2%AD%90) - GitHub への push を Redmine に通知し、コミットとチケットを紐づけ。
- [redmine_github](https://github.com/agileware-jp/redmine_github) ![GitHub stars](https://img.shields.io/github/stars/agileware-jp/redmine_github?style=flat&label=%E2%AD%90) - 手元の Redmine とリモートの GitHub リポジトリを接続（アジャイルウェア）。
- [Redmine Git Hosting（英語）](https://github.com/redmine-git-hosting/redmine_git_hosting) ![GitHub stars](https://img.shields.io/github/stars/redmine-git-hosting/redmine_git_hosting?style=flat&label=%E2%AD%90) - Redmine から Git リポジトリをホスティング。
- [redmine-slack（英語）](https://github.com/sciyoshi/redmine-slack) ![GitHub stars](https://img.shields.io/github/stars/sciyoshi/redmine-slack?style=flat&label=%E2%AD%90) - Redmine の更新を Slack に通知。

---

## API クライアント

Redmine REST API の上に、自作の LLM スクリプトやエージェントを作る場合に。

- [python-redmine（英語）](https://github.com/maxtepkeev/python-redmine) ![GitHub stars](https://img.shields.io/github/stars/maxtepkeev/python-redmine?style=flat&label=%E2%AD%90) - Redmine API 用 Python ライブラリ。
- [php-redmine-api（英語）](https://github.com/kbsali/php-redmine-api) ![GitHub stars](https://img.shields.io/github/stars/kbsali/php-redmine-api?style=flat&label=%E2%AD%90) - オブジェクト指向の PHP クライアント（メンテナ募集中）。
- [redmine-java-api（英語）](https://github.com/taskadapter/redmine-java-api) ![GitHub stars](https://img.shields.io/github/stars/taskadapter/redmine-java-api?style=flat&label=%E2%AD%90) - Redmine API 用 Java クライアント。
- [arcli（英語）](https://github.com/mightymatth/arcli) ![GitHub stars](https://img.shields.io/github/stars/mightymatth/arcli?style=flat&label=%E2%AD%90) - Redmine CLI（Go）。

---

## 検索・ナレッジ系プラグイン（AI と相性が良いもの）

データが整理され検索しやすいほど、AI も Redmine の情報を活用しやすくなります。

- [Redmine Full Text Search](https://github.com/clear-code/redmine_full_text_search) ![GitHub stars](https://img.shields.io/github/stars/clear-code/redmine_full_text_search?style=flat&label=%E2%AD%90) - Groonga／PGroonga／Mroonga による高速全文検索（日本語に強い。クリアコード）。
- [Redmine Elasticsearch（英語）](https://github.com/Restream/redmine_elasticsearch) ![GitHub stars](https://img.shields.io/github/stars/Restream/redmine_elasticsearch?style=flat&label=%E2%AD%90) - Elasticsearch による全文検索。
- [Redmine Knowledgebase（英語）](https://github.com/alexbevi/redmine_knowledgebase) ![GitHub stars](https://img.shields.io/github/stars/alexbevi/redmine_knowledgebase?style=flat&label=%E2%AD%90) - Redmine 内のナレッジベース記事。
- [Additionals（英語）](https://github.com/alphanodes/additionals) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additionals?style=flat&label=%E2%AD%90) - ダッシュボード、Wiki マクロ、他プラグイン用の共通ライブラリ（AlphaNodes）。
- [Additional Tags（英語）](https://github.com/alphanodes/additional_tags) ![GitHub stars](https://img.shields.io/github/stars/alphanodes/additional_tags?style=flat&label=%E2%AD%90) - チケットと Wiki ページにタグを追加。

---

## 関連リスト

- [alexandermeindl/awesome-redmine（英語）](https://github.com/alexandermeindl/awesome-redmine) ![GitHub stars](https://img.shields.io/github/stars/alexandermeindl/awesome-redmine?style=flat&label=%E2%AD%90) - Redmine 全般のツール・プラグイン・テーマ（2022年以降更新なし）。
- [shvyac/awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90) - ローカル LLM のエンジン・アプリ・エージェント集。
- [punkpeye/awesome-mcp-servers（英語）](https://github.com/punkpeye/awesome-mcp-servers) ![GitHub stars](https://img.shields.io/github/stars/punkpeye/awesome-mcp-servers?style=flat&label=%E2%AD%90) - あらゆる種類の MCP サーバー集。
- [awesome-selfhosted/awesome-selfhosted（英語）](https://github.com/awesome-selfhosted/awesome-selfhosted) ![GitHub stars](https://img.shields.io/github/stars/awesome-selfhosted/awesome-selfhosted?style=flat&label=%E2%AD%90) - セルフホスト用ソフト全般。
- [sindresorhus/awesome（英語）](https://github.com/sindresorhus/awesome) ![GitHub stars](https://img.shields.io/github/stars/sindresorhus/awesome?style=flat&label=%E2%AD%90) - Awesome のメタリスト。

---

## コントリビューション

コントリビューション歓迎です。リソース追加、リンク切れ修正、カテゴリ提案はプルリクエストでどうぞ。

**公式／プロジェクトの耐久性のある URL**、短い説明、継続的にメンテナンスされているプロジェクトを優先してください。GitHub のプロジェクトには ⭐ スター数バッジを付け、分かる範囲で対応する Redmine のバージョンと、ローカル LLM で動かせるかどうかを明記してください。可能なら `README.md` と `README.ja.md` の両方を更新してください。
