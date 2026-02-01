# GitHub Pages でHTMLを公開する手順

このフォルダ（`site/`）の中身をそのままGitHubにpushすると、**無料でWeb公開**できます。

---

## 1. GitHubでリポジトリを作る

1. [github.com](https://github.com) にログイン
2. 右上 **「+」→「New repository」**
3. **Repository name**: 好きな名前（例: `shoken-affiliate`）
4. **Public** を選択
5. **「Create repository」** をクリック  
   （README や .gitignore は追加しなくてOK）

---

## 2. このフォルダをGitでpushする

ターミナルで **証券開設** フォルダに移動して実行：

```bash
cd /Users/satoukanta/証券開設/site
git init
git add .
git commit -m "初回：HTMLサイト追加"
git branch -M main
git remote add origin https://github.com/あなたのユーザー名/リポジトリ名.git
git push -u origin main
```

- **あなたのユーザー名** … GitHubのユーザー名  
- **リポジトリ名** … さっき作ったリポジトリ名（例: `shoken-affiliate`）

---

## 3. GitHub Pages を有効にする

1. GitHub のリポジトリを開く
2. **「Settings」** をクリック
3. 左メニュー **「Pages」** をクリック
4. **Source** で **「Deploy from a branch」** を選択
5. **Branch** で **「main」** を選び、フォルダは **「/ (root)」**
6. **「Save」** をクリック

数分待つと、次のURLで表示されます：

**https://あなたのユーザー名.github.io/リポジトリ名/**

例: `https://tanaka.github.io/shoken-affiliate/`

---

## 4. 記事を増やすとき

- `site/` 内に **普通にHTMLファイルを追加**（例: `posts/記事2.html`）
- `index.html` の記事一覧にリンクを追加
- 以下を実行してpush：

```bash
cd /Users/satoukanta/証券開設/site
git add .
git commit -m "記事を追加"
git push
```

更新は数分で反映されます。

---

## フォルダ構成（参考）

```
site/
├── index.html          ← トップページ
├── style.css           ← 共通CSS
├── privacy.html        ← 必要なら作成
├── contact.html        ← 必要なら作成
└── posts/
    └── sample.html     ← 記事
```

**普通にHTMLを書いて、このフォルダに保存 → push** だけでOKです。
