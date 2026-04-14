# TV MAGNET

静的 HTML ベースの TV MAGNET ルーレットデモです。`index.html` を起点に各案へ遷移し、`home.html` と `roulette.html` が設定連携付きの実装ページです。

## ローカル確認

単純な静的サイトなので、ブラウザで [index.html](/Users/anrakukentarou/Desktop/TV magnet/index.html) を直接開けば確認できます。

## GitHub へ公開

1. GitHub で空のリポジトリを作成する
2. このディレクトリで初回コミットを作る
3. 作成した GitHub リポジトリを `origin` として追加する
4. `main` ブランチを push する

```bash
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:<YOUR_ACCOUNT>/<YOUR_REPO>.git
git push -u origin main
```

HTTPS を使う場合は `git remote add origin https://github.com/<YOUR_ACCOUNT>/<YOUR_REPO>.git` に置き換えてください。

## Cloudflare Pages で公開

このリポジトリはビルド不要の静的サイトとしてそのまま公開できます。

1. Cloudflare Dashboard で `Workers & Pages` → `Create application` → `Pages` を開く
2. `Connect to Git` を選び、GitHub リポジトリを接続する
3. 対象リポジトリを選ぶ
4. ビルド設定は次のようにする

```txt
Production branch: main
Framework preset: None
Build command: exit 0
Build output directory: .
Root directory: /
```

5. デプロイを実行する

公開後のトップページは `index.html` です。`home.html` を入口にしたい場合は、`index.html` を差し替えるか、Cloudflare Pages のリダイレクト設定を追加してください。

## 更新フロー

```bash
git add .
git commit -m "Update TV MAGNET"
git push
```

`main` に push すると Cloudflare Pages が自動で再デプロイします。
