# リポジトリ初期設定ガイド

テンプレートから作成したリポジトリで最初に行う設定です。

---

## 1. ブランチ保護ルールを設定する

GitHub のリポジトリページ → **Settings** → **Branches** → **Add branch protection rule**

| 項目 | 設定値 |
|---|---|
| Branch name pattern | `main` |
| Require a pull request before merging | **ON** |
| Require approvals | **1** |
| Require status checks to pass before merging | 任意 |
| Include administrators | **ON**（推奨） |

これにより `main` への直接 push が禁止され、PR + レビュー承認が必須になります。

---

## 2. マージ方式を Squash merge のみにする

GitHub のリポジトリページ → **Settings** → **General** → 「Pull Requests」セクション

| 項目 | 設定値 |
|---|---|
| Allow merge commits | **OFF** |
| Allow squash merging | **ON** |
| Allow rebase merging | **OFF** |

---

## 3. リポジトリの Description を設定する

GitHub のリポジトリページ右上の歯車アイコンから、リポジトリの説明を入力:

- 例: `鈴木のプロダクト紹介 LP`
- 例: `佐藤のセミナー管理ツール`

---

## 4. README.md を埋める

リポジトリのルートにある `README.md` の各セクションを記入してください。
空欄のまま PR を出さないようにしましょう。

---

## 5. ローカルにクローンして作業開始

```bash
cd ~/dev
git clone https://github.com/techbloomers/{your-repo-name}.git
cd {your-repo-name}

# 作業ブランチを作成
git switch -c feature/{topic}
```

開発フローの詳細は [CONTRIBUTING ガイド](https://github.com/techbloomers/.github/blob/main/CONTRIBUTING.md) を参照してください。
