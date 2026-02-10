# Mission: 旅支度 (Environment Setup)

> **🗺️ World Map**: **[Intro]** > [Front] > [Back] > [Cloud] > [Dungeon] > [Real]

## 📍 Learning Roadmap (学習のロードマップ)

### 🎯 Today's Can-Do (到達目標)
- **「なぜGitが必要なのか」** を、ゲームのセーブデータに例えて説明できる。
- AIツール (Cursor) をインストールし、日本語でチャットができる。
- 自分のプロジェクトをクラウド (GitHub) に保存できる。

このミッションのゴールは、**「最強の武器（AI & Git）を手に入れること」** です。
初期設定はトラブルが最も起きやすい「最初のボス」です。慎重に進めてください。

1.  **Cursor**: AI搭載コードエディタの導入。
2.  **Git & GitHub**: バージョン管理システムの導入。
3.  **Communication**: Slackでの報告ルールの確認。
4.  **Mentor Bot**: AIアシスタントの設定。

---

## Step 0: コミュニケーションの準備 (Slack)

この研修では、毎日の進捗報告を **Slack** で行います。
現場のエンジニアと同様に、「チームで動く」感覚を掴んでください。

1.  **準備**: 会社指定のSlackワークスペースにログインしていることを確認してください。
2.  **チャンネル参加**:
    - 研修担当から口頭で伝えられたチャンネルに参加してください。
3.  **挨拶**:
    - チャンネルに参加したら、一言「よろしくお願いします」と投稿してください。これが最初のコミュニケーションです。

---

## Step 1: エディタの導入 (Install Cursor)

AIが統合された開発ツール **Cursor** をインストールします。

1.  [公式サイト (cursor.sh)](https://cursor.sh/) にアクセス。
2.  `Download` ボタンからインストーラーを入手し、実行。
    - ※設定は全てデフォルトのままで問題ありません。
3.  **日本語化**:
    - 起動後、画面右上の歯車アイコン（Settings）-> `Extensions`。
    - `Japanese Language Pack` を検索してインストール。

---

## Step 2: GitHub連携 (Git Setup)

プログラミングの変更履歴を保存するツール **Git** と、それをクラウドに保存する **GitHub** を準備します。

1.  **GitHubアカウント作成**:
    - [GitHub.com](https://github.com/) でアカウントを作成（無料）。
2.  **リポジトリの作成**:
    - GitHub右上の「＋」 -> `New repository`。
    - **Repository name**: `ai-training-quest`
    - **Public/Private**: **Private**（非公開）を選択。
    - **"Add a README file"**: ✅ **必ずチェックを入れる**。
    - `Create repository` をクリック。

### ローカル環境への複製 (Clone)
1.  緑色の `<> Code` ボタン -> `HTTPS` のURLをコピー。
2.  PCの適当なフォルダでターミナル（Git Bash等）を開く。
3.  以下のコマンドを実行（URLは自分のものに置き換え）。
    ```bash
    git clone [コピーしたURL]
    ```
4.  作成された `ai-training-quest` フォルダを、Cursorで開く（File -> Open Folder）。

> [!IMPORTANT]
> エクスプローラーに `README.md` が表示されていれば、連携成功です。

---

## Step 3: AIメンターの設定 (Configure Mentor Bot)

プロジェクト専用のAIアシスタント（システムプロンプト）を導入します。

1.  **ルールファイルの入手**:
    - [Mentor Bot Rule (.cursorrules)](https://raw.githubusercontent.com/Wait-For-Official-Repo/.cursorrules) からダウンロード。
2.  **配置**:
    - `ai-training-quest` 直下に `.cursorrules` という名前でファイルを配置。
    - ※拡張子が `.txt` にならないよう注意してください。

### 動作確認
1.  Cursorのチャット欄 (`Ctrl + L`) を開く。
2.  「こんにちは」と入力して送信。
3.  AIから、研修のガイドラインに沿った応答（Mentor Botとしての振る舞い）が返ってくれば設定完了です。

---

## 📜 Day 0-Ex: プロジェクト発足 (First Commit)

最後に、あなたがこの開発プロジェクトのオーナーであることを宣言します。
これが **「First Commit（最初の記録）」** です。

1.  **READMEの編集**:
    - `README.md` を開く。
    - 最初から書いてある文字を消し、以下のように書き換える。
    ```markdown
    # Project Log
    これは、私がAI駆動エンジニアになるための学習記録である。
    目標: 「10日後には、自分の力でアプリを作れるようになる！」
    ```
    - ※本名は書かないでください！ ペンネームや意気込みだけでOKです。

2.  **変更の保存 (Commit)**:
    - ターミナル（詠唱画面）を開く (`Ctrl + @`)。
    - 以下のコマンドを入力し、Enter。
    ```bash
    git add .
    git commit -m "Project Init: Hello World!"
    git push origin main
    ```

3.  **確認**:
    - GitHubのページを再読み込みする。
    - あなたの書いた「目標」が表示されていれば、手続き完了です。

### 🧙‍♂️ Oral Exam (口頭試問)
Mentor Botに向かって、こう話しかけてください。
「Day 0 クリア！GitとGitHubの違いについて、ゲームに例えて説明するから聞いてて！」

合格が出たら、旅の準備は完了です。
次は **Day 1: 創造の魔法（HTML/CSS）** です。

---
**[Next]** 👉 [Day 1: Frontend Basics (基本)](../Day01_Frontend_HTML/01_concept_structure.md)
