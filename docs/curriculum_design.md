# 詳細設計書: カリキュラム構成案 (Content Design) v7

## 基本方針: "Adventure & Incubation"
- **Tone**: 「冒険」のワクワク感を取り戻す。
- **Incubation**: 「動く」だけでなく「書ける（ドキュメント）」エンジニアを育てる。
- **AI Policy**: **「プロンプトを考えること」こそがエンジニアの仕事** と定義する。安易なコピペを禁止し、段階的に補助輪を外す。

---

## 0. 教育戦略: Structural Drills & The 8-Hour Routine

「AIに頼めば一瞬で終わる」ことを、あえて**8時間かけて**深く味わいます。
AIは「手」として使い、研修生は「頭（設計・理解・言語化）」をフル回転させます。

### 📊 Project Management Strategy (WBS)
初心者がいきなり「タスク分解」をするのは不可能です（作業の粒度がわからないため）。
そのため、以下の **「段階的リリース (Gradual Release)」** で進めます。

1.  **Day 1-2 (Copy)**: サンプルWBS (`wbs_examples/`) を写経し、**「実績」** だけを記入する。まずは「時間の流れ」を体感する。
2.  **Day 3-4 (Adjust)**: サンプルをベースに、自分のペースに合わせて「予定」を修正する。
3.  **Day 5 (Create)**: 白紙のテンプレートから、自分でタスクを洗い出し、時間を計算する。

### ⏳ The Daily Schedule (1日の標準タイムテーブル)
「いつドリルをやるのか」を明確化し、**学習サイクル（Input -> Output -> Teach）** を強制します。

| 時間 | フェーズ | 内容 (What to do) | AI使用 |
|:---|:---|:---|:---|
| **09:00 - 09:30** | **0. Morning Plan (WBS)** | `wbs_template.md` を埋め、**「この計画で無理がないか」をAIにレビューしてもらう**。<br>※上司の承認をもらう疑似体験。 | 🆗 Reviewer |
| **09:30 - 10:00** | **1. Concept Research (調査)** | その日のテーマ（HTMLとは？APIとは？）を**ググって**調べる。<br>AIに聞くのは禁止。公式ドキュメントや技術記事を読む訓練。 | 🆖 Forbidden |
| **10:00 - 12:00** | **2. Structural Drills (素振り)** | 用意された3つのドリルを行う。<br>ただし「クリア」だけでは不十分。**「色を変える」「数を増やす」などの応用実験**を自ら行う。 | 🆗 Copilot |
| **13:00 - 15:00** | **3. Mission (演習)** | Boss Battle (アプリ作成)。<br>Drillの知識を総動員して、ゼロから設計・実装する。 | 🆗 Copilot |
| **15:00 - 16:00** | **4. Hardening (堅牢化)** | **「意地悪テスト」の時間**。<br>連打、異常値、削除などを行い、セキュリティと堅牢性を高める。 | 🆗 Copilot |
| **16:00 - 17:00** | **5. Dissection Report (解剖)** | 生成されたコードの「どこ」が「何」をしているか、図やコメントで解説資料を作る。<br>**「AIが書いたコードの責任を持つ」**訓練。 | 🆗 Assistant |
| **17:00 - 18:00** | **6. Teacher Mode (言語化)** | 今日の学びを、**「自分より初心者の人」に教えるつもりで** 日報やQiita記事の下書きとしてまとめる。 | 🆗 Reviewer |

### 📚 Daily Research Themes (AI禁止タイムの課題)
09:00-10:00 は **「AI禁止」** です。自力で以下のキーワードをGoogle検索し、**「自分なりの言葉」** でノートにまとめてください。

| Day | テーマ (Theme) | 検索キーワード (Keywords) | 問い (Questions to Answer) |
|:---|:---|:---|:---|
| **Day 1** | **UIの構造 (Universal UI)** | `UI 階層構造`, `ボックスモデル 概念`, `レスポンシブデザインとは` | ・スマホアプリもWebも、全ては「四角い箱」でできている？<br>・「内側の余白 (Padding)」と「外側の余白 (Margin)」の違いは？<br>・「親」と「子」の関係（入れ子構造）とは？ |
| **Day 2** | **動きの正体** | `DOMとは`, `JavaScript イベント`, `変数と定数` | ・「ボタンが押された」ことをPCはどうやって知る？<br>・なぜ `const` を使うべきなの？<br>・`console.log` は誰のためにある？ |
| **Day 3** | **通信の会話** | `HTTPリクエスト レスポンス`, `JSONとは`, `ステータスコード 意味` | ・ブラウザとサーバーはどうやって会話している？<br>・JSONはなぜ「軽量」と呼ばれる？<br>・`200` と `404` と `500` の違いは？ |
| **Day 4** | **データの家** | `RDB NoSQL 違い`, `クラウドデータベース`, `Firestore 仕組み` | ・Excelとデータベースは何が違う？<br>・なぜ「サーバーレス」が流行っている？<br>・チャットのログはずっと残るべき？ |
| **Day 5** | **設計と合意** | `要件定義書 書き方`, `UI/UX デザイン`, `アジャイル開発` | ・「欲しいもの」と「作れるもの」のギャップはどう埋める？<br>・なぜいきなりコードを書いてはいけない？<br>・「良い設計」とは？ |


### The 3-Step Flow: Block First
全てのドリル（小課題）で、以下の3ステップを徹底させる。

1.  **Block Sketch (ブロック分解)**
    -   Webサイトを「親箱」「画像」「ボタン」などの日本語ブロックとして分解・認識する。
    -   *Output*: 日本語のメモ（構造ツリー）。
2.  **Translation (翻訳)**
    -   **Visual Dictionary (ビジュアル辞書)** を使い、日本語ブロックをタグに変換する。
    -   例：「横並びの箱」→ `display: flex`, 「押せる箱」→ `<button>`
3.  **Construct (構築)**
    -   翻訳した用語を使って、やりたいことをAIに**言葉で説明（言語化）**する。
    -   *Rule*: 無理にコードプロンプトを書こうとせず、「何（名詞）を・どう配置して（動詞）・どうしたいか（形容詞）」を伝える。
    -   例：「`div`という箱の中に、`button`を置いて、`flex`で真ん中に寄せて」

---

## Curriculum Roadmap (Drills & Missions)
各Dayは **Drills (数稽古)** で基礎を固め、**Mission (総合演習)** でアプリを作る構成とする。

---

## Day 0: 冒険の地図と装備 (Map & Inventory)
**目標**: 開発環境を整え、自分が挑む世界の広さを知る。

### 1. 世界の仕組み (The World Map)
- **Concept**: 「クエスト（Webアプリ）はどうやって動いている？」
- **Setup**: Cursor, Git, Mentor Bot。
    - **Mentor Bot**: GitHubから `.cursorrules` をダウンロードして配置する。

---

## Day 1-2: 構造化の基礎 (Frontend Structure)
**目標**: 「見たまま」を「ブロック」に分解し、それを「コード」に翻訳できるようになる。

### Day 1: HTML/CSS Drills (5本ノック + 1 Mission)
- **Concept**: Webサイトは「箱」の積み重ねである。
- **New Tool**: **The Visual Dictionary (タグ絵合わせ図鑑)**
- **Drills (素振り)**:
    1.  **The Button**: ただの箱を「押せるボタン」にする（`border-radius`, `box-shadow`）。
    2.  **The Card**: 画像と文字を縦に積む。
    3.  **The Holy Trinity**: ヘッダー、メイン、フッターを積む。
    4.  **The Flex Layout**: 3つの箱を「横並び」にする。
    5.  **The Grid**: 写真を格子状に並べる。
- **Mission**: "冒険者の名刺（プロフィールサイト）"
    -   Drillで作ったパーツを組み合わせて作る。

### Day 2: JS Logic Drills (5本ノック + 1 Mission)
- **Concept**: 「動き」もブロックで考える（イベント・状態・分岐）。
- **Drills (素振り)**:
    1.  **Toggle**: クリックでON/OFF（背景色）を変える。
    2.  **Counter**: 数字を増やす・減らす（変数の変化）。
    3.  **Input**: 入力した文字を画面に出す（リアルタイム反映）。
    4.  **Timer**: 3秒後にアラートを出す（非同期の入り口）。
    5.  **Omikuji**: ランダムに運勢を出す（配列と乱数）。
- **Mission**: "インタラクティブ・モンスター図鑑"
    -   クリックすると詳細が出る、検索できる等の機能実装。

---

## Day 3-4: 城の裏側と世界樹 (Backend & Cloud)
**目標**: 自分だけの城を、世界樹（クラウド）につなぐ。

### Day 3: 指令所 (API Server)
- **Prompt Lv.2 (Structure)**: 「役割（あなたはPythonのプロです）」を指定する重要性を教える。
- **Topic**: "酒場の掲示板 API"
- **Training: Cartography Lv.1 (Data Flow)**
    - **Visualization**: Cursorのプレビューボタン。
    - **Action**: AIに「Mermaidで描いて」と依頼するが、具体的な指示文は自分で考えさせる。

### Day 4: 世界樹への接続 (Cloud Integration)
- **Topic**: "消えないCloud Database (Auth/Firestore)"
- **Security Check**: APIキー管理とセキュリティルール。

---

## Day 5: 試練の塔 (The Dungeon & Scrolls)
**目標**: コードを書く前に「地図（設計書）」を書く。

### Day 5: グランピング予約システム "Starry Night"
- **Mission 1: 依頼書の解読 (Requirements)**
    - **Action**: テンプレートを埋める。

- **Mission 2: 設計図の作成 (Basic Design)**
    - **Prompt Lv.3 (Free)**: AIへの指示は一切サポートしない。「画面遷移図を描かせろ」という司令のみ。
    - **Concept**: AI駆動開発。

- **Mission 3: 実装 (Build with React + Firebase)**
    - **Scope**: フルスタック実装（妥協なし）。
    - **Strategy: The Copy-Paste Magic (資産の再利用)**
        - Day 4のコードを流用する。
    - **Prompt Lv.3 (Free)**: 「Reactで作って」だけでは動かないことを痛感させる。「どのファイルの、どの部分を、どう変えるか」まで指示しないと動かない経験をさせる。
    - **New**: AI Plan Review.
    - **New**: Hardening with QA.

---

## Day 6-10: 未踏の地へ (Into the Wild)
**目標**: ガイドのない世界で生き抜く。
