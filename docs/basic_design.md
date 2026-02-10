# 基本設計書: ドキュメントフォーマット & 構造設計 (v2)

## 1. デザインコンセプト: "The Quest Log"
マニュアル全体を「冒険の書（Quest Log）」に見立て、読むストレスを減らし、ワクワク感を維持するデザインを採用する。

## 2.5. メディア・配信戦略 (Delivery & Media Strategy)
**「GitHubそのものを教科書にする」** 方針に変更します。
PDFではなく、GitHub上の Markdown ビューワー（または GitHub Pages）で閲覧することを前提とし、新人がGitHubのUIに慣れる機会を増やします。

### 🌍 Platform (GitHub vs Notion)
- **Primary**: **GitHub Repository** (`docs/` フォルダ)
    -   **理由**: 研修で使うツールそのものであり、マニュアルを読む行為自体が「GitHubに慣れる」訓練になるため。
    -   **管理**: コードとドキュメントを一元管理できる（Version Control）。

### 🖼️ 画像 (Images)
- **配置**: `docs/images/` 配下。
- **表示**: GitHubのMarkdownビューワーは画像・GIFをネイティブに表示可能。
- **貼り付け**: `![説明](../images/day01/sample.png)`

### 🎥 動画 (Videos)
GitHub上での閲覧を前提とするため、表現の幅が広がります。
1.  **GIFアニメ (推奨)**:
    -   「クリックの瞬間」などの短い動作はGIFにする。自動再生されるため、クリックの手間がない。
2.  **埋め込み動画 (mp4)**:
    -   GitHubは `drag & drop` で動画をアップロード可能（README等）。
    -   または YouTube リンクを貼り、サムネイルを表示させる。
    -   `[![Alt](http://img.youtube.com/vi/VIDEO_ID/0.jpg)](http://www.youtube.com/watch?v=VIDEO_ID)`

---

## 2.5. メディア戦略 (Media Strategy)
PDF出力とGitHub閲覧の両方に対応するためのルール。

### 🖼️ 画像 (Images)
- **配置**: `docs/images/` 配下に格納する。
- **パス**: 相対パスで記述する（例: `![] (../images/day01/draw.png)`）。
- **目的**: 画面キャプチャ、図解。

### 🎥 動画 (Videos) -> GIF & Links
PDFには動画が埋め込めないため、以下の2パターンで対応する。
1.  **GIFアニメーション**:
    -   「ボタンを押す」「コマンドを打つ」などの短い動作（5秒以内）。
    -   画像と同じ扱いでPDFにも埋め込まれる（動かないが、静止画として表示される/ツールによる）。
    -   *今回は「静止画（コマ送り）」を推奨（ファイルサイズ削減のため）。*
2.  **QRコード / リンク**:
    -   長時間の解説が必要な場合は、YouTube等のURLを貼り、QRコード画像を添える。
    -   `[![使い方動画](../images/qr_video.png)](https://youtube.com/...)`
```

---

## 3. ページレイアウト (Page Layout Model)
各章（MDファイル）は、以下の定型フォーマット（テンプレート）に従って記述する。

### [Header] 冒険の現在地 (The World Map)
ページの最上部に、「全行程のどこにいるか」と「今日のルート」を可視化する。

```markdown
# Quest 1-1: 最初のWebページを召喚せよ

> **🗺️ World Map**: [Intro] > **[Front]** > [Back] > [Cloud] > [Dungeon] > [Real]

## 📍 Today's Route (今日のルート)
このクエストでは、以下の順序で攻略を進めます。迷子にならないように地図を確認しましょう。
1. **Cursorを開く** (武器を構える)
2. **AIに指示を出す** (呪文を唱える)
3. **ブラウザで確認する** (結果を見る)
4. **HTMLの正体を知る** (解剖する)

## 🎯 Final Objective (最終ゴール)
- **このクエストを完了すると？**: 
  - 世界に一つだけの「自己紹介サイト」が手に入ります。
  - 「コードを書かずにアプリを作る」感覚をマスターできます。
```

### [Body] 攻略チャート (Atomic Steps)
「1手順1画像」を基本とし、迷子を防止する。

```markdown
### Step 1: Cursorを開く
1. デスクトップの `Cursor` アイコンをダブルクリックします。
   ![Cursor Icon](/images/01/icon_click.png)
2. `Ctrl + Shift + N` を押して新しいウィンドウを開きます。

> [!TIP] **Wizard's Note (賢者の助言)**
> `Ctrl + Shift + N` は「新しい窓を開く」呪文（ショートカット）です。一生使うので覚えよう。
```

### [Engagement] ゲーム化要素
区切りごとに以下の要素を配置。

- **👾 Encounter! (エラー発生)**:
  - よくあるエラーをあえて予言する。「ここで赤い文字が出たら、それはモンスター『Syntax Error』です。こうすれば倒せます」
- **💾 Save Point (コミット)**:
  - 「ここまで動いたらセーブ（Git Commit）しましょう。合言葉は『Initial Commit』」

### [Footer] 報酬と振り返り
```markdown
## 💎 Loot (獲得スキル)
- [x] HTMLファイルの作り方
- [x] ブラウザでのファイル閲覧方法

## 🛑 Checkpoint (関所)
隣の人、またはMentor Botに以下の説明ができたら次へ進めます。
- 「HTMLコードがブラウザで絵になるまでの流れ（地図）を描いてみて？」
```

---

## 4. 編集・運用ワークフロー (Maintainability)
頻繁なアップデートに対応するための仕組み。

1.  **Source of Truth**: 全て `docs/` 配下のMarkdown。
2.  **PDF Generation**:
    -   **VS Code (Markdown PDF)**: 最も手軽。開発者がそのままPDF化して確認可能。
    -   **Vivliostyle (Optional)**: CSSで高度な組版が必要な場合（今回はVS Code拡張で十分と判断）。
3.  **Linting**: `markdownlint` を導入し、フォーマット崩れを自動検知。
