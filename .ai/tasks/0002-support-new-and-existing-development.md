# 新規・既存・混在する開発への対応を整える

- Status: completed
- Depends on: none

## 目的と要求

ユーザー依頼に基づき、単一ハーネスで作業対象の状態を判断し、新規・既存・混在する開発に対応する。task運用、要件参照、導入・更新の不整合を解消する。

## 変更対象

AGENTS.md、README.md、.ai/README.md、.ai/common.md、.ai/project.md、.ai/guides/01-requirements.md、.ai/guides/02-design.md、.ai/guides/03-implementation.md、.ai/guides/04-testing.md、.ai/tasks/README.md、本task。

## 対象外と制約

導入先への一括反映、アプリ実装、コミット・pushは行わない。既存の未追跡.DS_Storeを保持する。承認済みの実装依頼に不要な再承認を要求せず、要求や受け入れ条件を勝手に変更しない。

## 受け入れ条件・検証

作業対象単位の状態判断、初期設計と検証手段の整備、既存部分の互換性、task更新権限、既存の要件正本、上書きしない導入・更新が一貫して記載されること。差分、相対リンク、git diff --checkを確認する。

## 実施結果

- 作業対象単位の判断、初期設計・検証、既存の回帰確認、task更新権限、要件正本と導入・更新手順を整合させた。
- 文書差分、ローカル相対リンク、git diff --checkを確認した。アプリ動作の検証は対象外。
- 他プロジェクトへの反映、コミット・pushは行っていない。
