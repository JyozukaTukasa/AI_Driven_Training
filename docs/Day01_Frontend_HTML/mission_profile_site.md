# Day 1: フロントエンド基礎 (HTML & CSS)

> **🗺️ World Map**: [Intro] > **[Front]** > [Back] > [Cloud] > [Dungeon] > [Real]

## 📍 Learning Roadmap (学習のロードマップ)

### 🎯 Today's Can-Do (到達目標)
- 非エンジニアの友人に **「なぜHTMLだけではデザインが崩れるのか」** を、身近な例え（骨組みと服など）を使って説明できる。
- AIに「四角い箱を作って」と依頼するプロンプトを、自分で考えられる。

![Profile Site Mockup](assets/1-4.png)

何もない状態から、最初のWebページを作成します。
**HTML** は「ページの骨組み（形の魔法）」を、**CSS** は「見た目の装飾（色の魔法）」を担当します。

1.  **Workspace**: フォルダ構成の作成。
2.  **Prompting**: AIへの指示出し（コード生成）。
3.  **Preview**: ブラウザでの表示確認。

---

## Step 1: 開発環境の確認 (Workspace Setup)
開発において「整理整頓」は品質そのものです。
ファイルが散らからないよう、ルールに従ってフォルダを作成します。

1.  Cursorで `ai-training-quest` を開いていることを確認。
2.  **プロジェクト用フォルダ**:
    - `EXPLORER` で右クリック -> `New Folder` -> 名前: `projects`
3.  **Day 1 用フォルダ**:
    - `projects` の中に `day01` を作成。
4.  **素材の配置**:
    - アイコン画像（`icon.png`等）があれば `projects/day01/` に配置。
    - ※画像がない場合は、AIにダミー画像のURLを指定させます。

---

## Step 2: HTMLによる構造化 (Structure)

HTML/CSSを全て手書きする必要はありません。
AIに対して「要件」を明確に伝え、コードを生成させます。

1.  **AI Chatを開く**: `Ctrl + L`
2.  **プロンプト入力 (Prompt Design)**:
    以下の要件をコピーし（または自分の言葉で）、AIに指示を出してください。

```text
実習開始です。
projects/day01/ フォルダの中に、私の自己紹介サイト用ファイル一式を作ってください。

# 要件
1. ファイル名は index.html と style.css にすること。
2. htmlファイルから cssファイルを読み込むこと。
3. 私の名前 "Adventurer" と、自己紹介文、そして画像を配置すること。
4. デザインは「RPGのステータス画面」風の、ダークモード基調にすること。
```

3.  **確認と適用 (Apply)**:
    - AIが提案したコードを確認し、`Apply` (または `Save All`) でファイルを作成します。

---

## Step 3: ブラウザで確認 (Preview)

生成されたコードが、実際にどのようなWebページとして表示されるか確認します。
ソースコード（文字）が、Webページ（UI）に変換されるプロセスです。

1.  左側の `EXPLORER` で `projects/day01/index.html` を見つける。
2.  ファイルを **右クリック** -> `Copy Path` (パスのコピー)。
3.  Chromeなどのブラウザを開く。
4.  アドレスバーに貼り付けて Enter。

🎉 **Congratulations!**
あなたの手元のファイルが、かっこいいWebページになりましたか？
もし画像が表示されていなかったら、画像のファイル名が合っているか確認してみてください。

---

## 🔍 The Analytic Eye (解剖の時間)
AIが書いたコードを、3つの視点（ビジネス・魔法・実例）で解剖してみましょう。

![HTML vs CSS](assets/1-5.png)

### HTML (Structure)
- **定義**: ハイパーテキスト・マークアップ・ランゲージ。Webページの骨組み。
- **魔法**: **形の魔法**。何もない空間に「箱」や「文字」の実体を生み出す。
- **実例**: YouTubeの「動画プレイヤー」や「コメント欄」の四角い枠そのもの。
    - `<div>`: ただの箱。
    - `<h1>`: 見出し（大声）。
    - `<img>`: 画像（幻影）。

### CSS (Style)
- **定義**: カスケーディング・スタイル・シート。見た目の装飾。
- **魔法**: **色の魔法**。骨組みに服を着せたり、化粧をする。
- **実例**: YouTubeの「赤と白のテーマカラー」や「角丸のボタン」。
    - `color: red;`: 文字を赤くする。
    - `background-color: black;`: 背景を黒くする。

> **🤔 Thinking Time: なぜファイルを分けるのか？**
> HTMLの中に直接色を書くことも技術的には可能です。
> しかし、なぜプロはわざわざ `style.css` という別ファイルを作るのでしょうか？
> ヒント：**「YouTubeの全ページの色を一括で変えたい時」** を想像してみましょう。（答えはAIに聞いてみてください）

---

## 🛑 Checkpoint (関所)
自分好みに改造して、リポジトリ（セーブポイント）に保存しましょう。

1.  **Modify**:
    - AIにチャットで「もっとサイバーパンク風にして」「フォントを光らせて」と追加注文し、変化を楽しむ。
2.  **First Commit (Day 1)**:
    - ターミナルで以下を実行。
    ```bash
    git checkput -b feature/day01  # 作業用ブランチ作成
    git add .
    git commit -m "Day 1 Complete: 自己紹介サイト"
    git push origin feature/day01
    ```

3.  **Merge to Main (合体)**:
    -   作業が終わったら、本体（main）に戻って作業を統合します。
    ```bash
    git checkout main        # 本線に戻る
    git merge feature/day01  # 作業を取り込む
    git push origin main     # クラウドの本線も更新
    ```

### 🧙‍♂️ Oral Exam (口頭試問)
Mentor Botに向かって、こう話しかけてください。
「Day 1 クリア！HTMLって何のためにあるのか、おばあちゃんでもわかるように説明するから聞いてて！」

合格が出たら、次は **Day 2: フロントエンドロジック (JavaScript)** へ進みます。

---
**[Next]** 👉 [Day 2: フロントエンドロジック (JavaScript)](../Day02_Frontend_JS/02_concept_logic.md)
