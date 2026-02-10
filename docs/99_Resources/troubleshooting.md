# Troubleshooting Guide (トラブルシューティング)
「エラー」は敵ではなく、道しるべです。
よく遭遇するエラーと、その対処法をまとめました。ちと、その退治方法（解決策）を記した書。
Mentor Botに案内されたら、ここを読んで戦え。

| Monster Name (エラー名) | 症状 (Symptom) | 武器 (Solution) |
|:---|:---|:---|
| **The 404 Phantom** | `Not Found` / ページが見つからない | 1. URLのスペルミス。<br>2. サーバー(`uvicorn`)が起動していない。<br>3. ファイルの場所が違う。 |
| **The CORS Hydra** | 赤文字で `CORS error` / データが取れない | フロントとバックエンドのドメインが違う時に出る。<br>FastAPIに `CORSMiddleware` を追加する魔法で倒せる。 |
| **The 500 Behemoth** | `Internal Server Error` | サーバー側で致命的なバグ起きている。<br>**ブラウザではなく、ターミナルのログを見る** と正体がわかる。 |
| **The Git Conflict** | `CONFLICT` / マージできない | 同じ行を別々に書き換えてしまった。<br>VS Codeでファイルを開き、`<<<< HEAD` の箇所を探し、「Accept Current Change」等を選ぶ。 |
| **The Whiteout** | 画面が真っ白で何も出ない | 構文エラーの可能性が高い。<br>**F12キー** を押して「Console」タブを開くと、そこに正体が隠れている。 |
| **The API Key Leak** | GitHubから警告メールが来る | `.env` を使い忘れている。<br>即座にFirebaseコンソールでキーを無効化し、再発行せよ。 |
