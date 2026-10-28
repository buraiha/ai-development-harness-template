# macOSメタデータの除外

- Status: completed
- Depends on: none

## 目的・範囲

ユーザー依頼に従い.gitignoreへ.DS_Storeを追加し、本taskとともにコミットする。メタデータ自体は削除せず、既存の文書やアプリには変更を加えない。

## 検証

差分・git diff --check・check-ignoreとコミット後のGit状態を確認する。pushは行わない。

## 実施結果

.DS_Storeの除外規則を追加した。差分と除外確認を行い、コミット後に作業ツリーがクリーンか確認する。
