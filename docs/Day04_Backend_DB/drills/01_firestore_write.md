# Drill 1: The Recorder (データを保存)

Day 4 は **データベース (Database)** です。
ページを閉じても消えない「永久の記憶」を扱います。
まずは「書き込む（Save）」練習です。

## 🎯 Goal
-   入力フォームに文字を入れて「保存」ボタンを押す。
-   その文字が、クラウド上のデータベース (Firestore) に保存される。
-   (今回はブラウザのコンソールで「保存成功」が見えればOK)

---

## Step 1: Block Sketch
1.  **入力**: テキストボックス (`<input>`)。
2.  **イベント**: 保存ボタン (`<button>`) をクリック。
3.  **通信**: クラウドにデータを送る (`addDoc`)。

---

## Step 2: Visual Dictionary
-   **「保管庫」** → `collection(db, "roomName")` (特定の部屋)
-   **「追加する」** → `addDoc(保管庫, データ)`

---

## Step 3: Construct

### 🤖 Prompt Example
```text
【作りたいもの】
Firebase Firestore にデータを保存するフォーム。

【構造】
- 入力欄 (`<input type="text" id="msg">`)
- 保存ボタン (`<button id="saveBtn">`)

【動き】
1. Firestoreの設定 (Config) を読み込んでください。
2. ボタンが押されたら、入力された文字を取得して、
   Firestoreの `messages` というコレクションに保存してください。
   - 保存するデータ: `{ text: "入力された文字", date: Timestamp }`
3. 保存できたら、コンソールに "Saved!" と表示してください。
```

---

## Step 4: Code Literacy
1.  **「宛先」はどこ？**
    -   `collection(db, "messages")` という部分を探してください。
    -   この `messages` を `secrets` に変えると、別の「部屋」に保存されます。
2.  **「手紙の中身」は？**
    -   `addDoc` のカッコの中にある `{ text: ... }` を探してください。
    -   ここに `hero: "Tanaka"` を書き足すと、保存される情報が増えます。
