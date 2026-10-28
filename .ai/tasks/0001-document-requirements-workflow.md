# 要件定義から始める開発手順を共通ハーネスへ反映

- Status: completed
- Depends on: none

## 目的・範囲

導入先で整備した要件定義手順を汎用化して同期する。
対象: AGENTS.md、README.md、.ai/README.md、.ai/guides/01-requirements.md、.ai/guides/02-design.md、.ai/tasks/README.md、本task。
要件の正本、要件定義だけの場合のtask不要の例外、要件IDと受け入れ条件の引き継ぎ、合意・承認・検証の区別を記載する。

## 対象外

導入先のアプリ固有要件・project.md・作業履歴のコピー。他プロジェクトへの一括反映。

## 受け入れ条件・検証

入口・README・ガイドの整合、相対リンク、固有情報の混入がないこと、git diff --checkを確認する。
既存の未追跡.DS_Storeを保持しコミットには含めない。コミット・push後にリモート一致を確認する。

## 実施結果

- 要件定義ガイド・設計引き継ぎ・taskとの役割分担を汎用化し、入口とREADMEも整合させた。
- 既存の要件正本の配置は維持するルールを追加した。project.mdの雛形は維持した。
- 相対リンク、アプリ固有情報の混入、差分、git diff --checkを確認した。
- ユーザーの同期依頼に従いmainへコミット・pushし、完了報告前にリモート一致を確認する。
