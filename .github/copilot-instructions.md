# GitHub Copilot カスタムインストラクション

## このリポジトリの目的

AI-Native ソフトウェア開発プラクティスに関する**系統的リサーチと質的メタ統合分析**を行うリサーチリポジトリです。コードを書くリポジトリではなく、Markdown ドキュメントを主な成果物とする研究プロジェクトです。

## 主要ファイルの役割

| ファイル | 役割 |
|:--|:--|
| `research.md` | 一次データ。Anthropic・Google・OpenAI・GitHub 等の公式情報源から収集した AI-Native 開発プラクティス 16エントリ（5カテゴリ）。 |
| `meta-analysis.md` | 二次分析。`research.md` を入力とした質的メタ統合レポート。8つの共通設計パターン・4つの技術的対立軸・パラダイムシフト評価・実践への提言を含む。 |

## リサーチの知見サマリー

### 業界標準（ゴールデンパス）として収束しているプラクティス

- **Context Engineering（P1）:** プロンプト単体ではなく、AIが動作する情報環境全体を設計する手法。最大54%の性能向上を実証（Anthropic）。
- **Human-in-the-Loop Gate（P3）:** AI生成コードの変更はすべて人間の承認ゲートを経由する設計（GitHub全製品で必須化）。
- **Sandbox Execution + Audit Log（P4）:** エージェントの隔離実行と全操作の監査ログ（MCPゲートウェイで一元管理）。
- **MCP によるツール統合標準化（P5）:** ChatGPT・Gemini・GitHub Copilot が採用。Linux Foundation に移管済み。
- **AI-Readable Codebase（P6）:** AGENTS.md・Skillパック・明示的な境界定義でコードベースを AI-Ready に設計。
- **Eval-Driven Development（P7）:** AI機能の品質管理に定量評価体制を中核として組み込む（SWE-bench Verified 等）。
- **AI as Systemic Change（P8）:** AI 効果は組織のアーキテクチャ・文化・プロセス全体の成熟度に依存（DORA 2025 定量実証）。

### まだ議論が続いている技術的対立軸

- エージェントの自律性境界（高自律 vs Human-in-the-Loop の粒度）
- コンテキスト管理（JIT圧縮取得 vs リッチコンテキスト事前ロード）
- エージェント設計粒度（モノリシック vs マルチエージェント専門分担）
- 評価アプローチ（SWE-bench 等の外部標準 vs DORA 等のプロダクション指標）

## Copilot への依頼時の注意

- **ドキュメント編集依頼:** 既存ファイル（`research.md`、`meta-analysis.md`）のフォーマット・スタイル・日本語表記スタイルを踏襲すること。
- **新規エントリ追加:** `research.md` の表形式（カテゴリ・タイトル・概要・URL・技術的ポイントの5列）を維持すること。
- **分析追加:** `meta-analysis.md` のパターン番号体系（P1〜P8）や対立軸フォーマットに整合させること。
- **英語技術用語:** カタカナまたは英語のまま表記し、一貫性を保つこと。
