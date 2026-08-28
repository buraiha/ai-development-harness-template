# AI Development Harness Template

CodexなどのAI開発エージェントに、リポジトリ内での仕事の進め方を共有するための汎用テンプレートです。

特定の言語やフレームワークには依存せず、次の流れを共通化します。

```text
要求理解 → 調査 → 変更方針 → 実装 → 検証 → 必要な修正 → 最終確認 → 報告
```

## 推奨構成例

```text
AGENTS.md
.ai/
├── README.md
├── common.md
├── project.md
├── guides/
│   ├── 01-requirements.md
│   ├── 02-design.md
│   ├── 03-implementation.md
│   ├── 04-testing.md
│   └── 05-review.md
└── tasks/
    ├── README.md
    ├── 0001-add-authentication.md
    └── 0002-add-user-pricing-table.md
docs/
├── architecture/
├── specifications/
└── decisions/
```

`0001-add-authentication.md`、`0002-add-user-pricing-table.md`、`docs/` 配下は導入先で必要に応じて追加する例であり、このテンプレートには含まれていません。

- `README.md`: 人間向けの概要と利用方法
- `AGENTS.md`: AIが最初に読む入口、基本原則、指示の優先順位
- `.ai/common.md`: プロジェクトを問わない共通の作業ルール
- `.ai/project.md`: AIの判断へ直接影響する、最小限のプロジェクト固有ルール
- `.ai/guides/`: 要求整理、設計、実装、テスト、レビューの再利用可能な手順
- `.ai/tasks/`: 機能追加や変更ごとの個別実装指示書
- `docs/`: 現在有効な詳しい仕様、設計、重要な意思決定

## 個別タスクの使い方

`.ai/tasks/` には、ひとまとまりの開発内容ごとに指示書を作成します。ファイル名は `4桁の連番-開発内容.md` とし、開発内容には英小文字の kebab-case を使用します。

```text
0001-add-authentication.md
0002-add-user-pricing-table.md
0003-add-pricing-settings-ui.md
```

各タスクには、少なくとも次の内容を記載します。

- 状態と依存するタスク
- 実装する目的と要求
- 変更対象と対象外
- 守るべき既存仕様や制約
- 受け入れ条件
- 想定する検証方法

AIへ作業を依頼するときは対象のタスクファイルを明示します。連番はタスクの識別に使用し、実行順序や依存関係は本文へ明記します。指定されていないタスクは自動的な実装対象になりません。

タスク文書は実装時点の指示です。完了後も有効な仕様や設計は `README.md` または `docs/` に反映し、タスク文書だけを現在の仕様の根拠にしないでください。

## 導入方法

1. `AGENTS.md` と `.ai/` を対象リポジトリのルートへコピーします。
2. `.ai/project.md` のプレースホルダーを、対象プロジェクトで確認できる事実に置き換えます。
3. 詳しい仕様や設計は、対象プロジェクトの `README.md` または `docs/` で管理します。
4. 個別の実装指示は `.ai/tasks/` に追加します。
5. 実際のAI作業で不足したルールだけを、少しずつ追加します。

最小構成で始める場合は、`.ai/common.md` の必要な要点と短い `Project Specific Rules` を `AGENTS.md` に統合します。その場合は、存在しない `.ai/common.md`、`.ai/project.md`、`.ai/guides/`、`.ai/tasks/` を必須とする記述も、実際の構成に合わせて削除または調整してください。現在の `AGENTS.md` だけをそのままコピーする方法ではありません。

## 方針

- 既存実装を調査してから変更する
- 要求を満たすための必要最小限の変更に留める
- ユーザーの既存変更や未追跡ファイルを保護する
- 既存の検証手段を調査して使用する
- 未確認事項を確認済みとして扱わない
- 明示的な依頼なしにコミット、プッシュ、デプロイ、本番操作を行わない

詳しい導入方針は [`.ai/README.md`](.ai/README.md) を参照してください。
