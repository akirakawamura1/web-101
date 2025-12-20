# Git 初期設定とコミット手順

## 実施日
2025年12月15日

## 概要
web-101 プロジェクトの Git リポジトリ初期化と GitHub への接続を完了。

---

## 実施内容

### 1. Git リポジトリの初期化
```bash
git init
```
- /Users/akirakawamura/Desktop/web-101/ に .git フォルダが作成される

### 2. ファイルをステージングに追加
```bash
git add .
```
- フォルダ構成、.gitignore、index.html などを追加

### 3. 初回コミット作成
```bash
git commit -m "初期設定: フォルダ構成とindex.htmlを作成"
```
- **コミットハッシュ:** fc98e47
- **ブランチ:** main
- **追加ファイル:** 44 ファイル
- **挿入行数:** 90 行

### 4. GitHub リポジトリの作成
- GitHub.com でリポジトリを新規作成
- リポジトリ名: web-101
- URL: https://github.com/akirakawamura1/web-101.git

### 5. ローカルリポジトリを GitHub に接続
```bash
git remote add origin https://github.com/akirakawamura1/web-101.git
```

### 6. リモート接続の確認
```bash
git remote -v
```
**出力:**
```
origin  https://github.com/akirakawamura1/web-101.git (fetch)
origin  https://github.com/akirakawamura1/web-101.git (push)
```

### 7. VS Code で「Branch の発行」ボタンをクリック
- ローカルの main ブランチを GitHub に発行

---

## 完了確認

```bash
git log --oneline
```
**出力:**
```
fc98e47 (HEAD -> main, origin/main) 初期設定: フォルダ構成とindex.htmlを作成
```

**ポイント:** `origin/main` が表示されているため、GitHub との同期が完了

---

## 今後の使用方法

### コードを変更してコミットする場合
```bash
git add .
git commit -m "変更内容"
git push origin main
```

### GitHub で確認
https://github.com/akirakawamura1/web-101

---

## 参考情報

- **ローカルリポジトリ:** /Users/akirakawamura/Desktop/web-101/
- **リモートリポジトリ:** GitHub (akirakawamura1/web-101)
- **デフォルトブランチ:** main
- **現在の状態:** ローカルと GitHub が完全に同期済み ✓

---

# 2025年12月21日: フォルダ整理

## 概要
ファイル管理を効率化するため、プロジェクトのフォルダ構成を整理しました。

## 実施内容

### 1. フォルダの作成とファイルの移動
- `css/`: スタイルシート (`.css`) を移動
- `js/`: スクリプトファイル (`.js`) を移動
- `images/`: 画像ファイル (`.png`, `.jpg` 等) を移動

### 2. パスの更新
- `index.html` 内のリンクパスを新しい構成に合わせて修正

### 3. 変更の記録
```bash
git add .
git commit -m "リファクタリング: フォルダ構成を整理"
git push origin main
```
