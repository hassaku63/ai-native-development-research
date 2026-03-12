# AI-Native Development Research

## このリポジトリについて

このリポジトリは、**2024〜2026年にかけてのAI-Native ソフトウェア開発プラクティスに関する系統的リサーチと分析**をまとめたものです。

### 目的

主要テック企業（Anthropic、Google、OpenAI、GitHub/Microsoft、Meta 等）の公式エンジニアリングブログ・リサーチペーパー・公式ドキュメントを横断的に収集・整理し、以下の問いに答えることを目的としています。

1. **2026年時点の業界標準（ゴールデンパス）は何か？** — 複数企業が独立して収束した「デファクトスタンダード」なプラクティスの特定
2. **企業・ツール間でアプローチが異なる点はどこか？** — 技術的対立軸とトレードオフの整理
3. **AI-Native SWE へのパラダイムシフトをどう評価するか？** — CI/CD・テスト・ドキュメントの本質的変化と AI-Ready Architecture の考察

### ここまでにやってきたこと

| ステップ | 内容 | 成果物 |
|:--|:--|:--|
| **1. 系統的リサーチ** | Anthropic・Google・OpenAI・GitHub 等の一次情報源（公式ブログ・論文・ドキュメント）から AI-Native 開発プラクティスを収集し、カテゴリ別に整理 | [`research.md`](./research.md) |
| **2. 質的メタ統合分析** | 収集済みプラクティス（16エントリ）を対象に、アカデミックな「質的メタ統合（Qualitative Meta-Synthesis）」手法で分析。共通設計パターン・技術的対立軸・パラダイムシフトの評価・実践への提言を構造化レポートとして作成 | [`meta-analysis.md`](./meta-analysis.md) |

---

## ファイル構成

```
.
├── README.md              # このファイル。リポジトリ概要とナビゲーション
├── research.md            # 一次データ：AI-Native開発プラクティス系統的リサーチ（16エントリ）
├── meta-analysis.md       # 二次分析：質的メタ統合レポート
├── CLAUDE.md              # Claude 向けシステムプロンプト
├── CHATGPT.md             # ChatGPT 向けカスタムインストラクション
└── .github/
    └── copilot-instructions.md  # GitHub Copilot 向けシステムプロンプト
```

---

## research.md の概要

2024〜2026年に公開された技術情報源を対象に、以下の5カテゴリで16エントリを収集・整理。

| カテゴリ | エントリ数 |
|:--|:--|
| AIエージェント・ワークフロー | 5 |
| AI-Readyなコードベース設計 | 3 |
| 既存SWE領域への統合 | 3 |
| 評価とガバナンス | 3 |
| 人間とAIの協調（UX） | 3 |

---

## meta-analysis.md の概要

`research.md` の16エントリを入力として、以下のセクションで構成した分析レポート。

1. **Executive Summary** — 業界到達点の3行要約
2. **収束進化（共通設計パターン）マトリクス** — 8つのゴールデンパス（P1〜P8）と相互関係図
3. **アプローチの相違（4つの技術的対立軸）** — トレードオフと判断基準付き
4. **AI-Native SWE へのパラダイムシフト評価** — CI/CD・テスト・ドキュメントの変容と AI-Ready Architecture 4層モデル
5. **論争点と今後の注視領域** — 5つの未解決課題
6. **実践への提言** — Priority 1〜3 に分類した高ROIアクションアイテム

---

## AI アシスタントと一緒に使うには

このリポジトリでは、Claude・GitHub Copilot・ChatGPT がこのリサーチの文脈を理解した状態で対話・補助できるよう、各 AI 向けのシステムプロンプトファイルを用意しています。

| AI | ファイル | 読み込み方 |
|:--|:--|:--|
| **Claude** | [`CLAUDE.md`](./CLAUDE.md) | `claude` CLI が自動読み込み / Project Knowledge に追加 |
| **GitHub Copilot** | [`.github/copilot-instructions.md`](./.github/copilot-instructions.md) | リポジトリに配置するだけで Copilot が自動参照 |
| **ChatGPT** | [`CHATGPT.md`](./CHATGPT.md) | GPT の「カスタムインストラクション」または「プロジェクト」に貼り付け |