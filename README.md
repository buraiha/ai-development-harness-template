# AI Development Harness Template

CodexなどのAI開発エージェントに、リポジトリ内での仕事の進め方を共有するための汎用テンプレートです。

特定の言語やフレームワークには依存せず、次の流れを共通化します。

```text
要求理解 → 調査 → 変更方針 → 実装 → 検証 → 必要な修正 → 最終確認 → 報告
```

## 構成

```text
AGENTS.md
.ai/
├── README.md
├── common.md
├── project.md
└── workflows/
    ├── 01-requirements.md
    ├── 02-design.md
    ├── 03-implementation.md
    ├── 04-testing.md
    └── 05-review.md
```

- `AGENTS.md`: AIが最初に読む入口と基本原則
- `.ai/common.md`: プロジェクト共通の作業ルール
- `.ai/project.md`: AI向けの最小限のプロジェクト固有ルール
- `.ai/workflows/`: 開発フェーズごとの補助手順

## 使い方

1. `AGENTS.md` と `.ai/` を対象リポジトリのルートへコピーします。
2. `.ai/project.md` のプレースホルダーを、対象プロジェクトで確認できる事実に置き換えます。
3. 詳しい仕様や設計は、対象プロジェクトの `README.md` または `docs/` で管理します。
4. 実際のAI作業で不足したルールだけを、少しずつ追加します。

最小構成で始める場合は、`AGENTS.md` だけを配置し、末尾に短い `Project Specific Rules` を追加する運用も可能です。

## 方針

- 既存実装を調査してから変更する
- 要求を満たすための必要最小限の変更に留める
- ユーザーの既存変更や未追跡ファイルを保護する
- 既存の検証手段を調査して使用する
- 未確認事項を確認済みとして扱わない
- 明示的な依頼なしにコミット、プッシュ、デプロイ、本番操作を行わない

詳しい導入方針は [`.ai/README.md`](.ai/README.md) を参照してください。
