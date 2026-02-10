# Drill 2: The JSON (データの形)

Webの世界では、データはすべて **JSON (ジェイソン)** という形式でやり取りされます。
「見えないデータ」を「見える形」にする練習です。

## 🎯 Goal
-   自分のプロフィール情報（名前、年齢、趣味）を **JSON形式** で書く。
-   それを画面に「きれいに」表示する。

---

## Step 1: Block Sketch
プログラムではありません。ただの「情報の整理」です。

-   私 (Object)
    -   名前: "Tanaka"
    -   年齢: 25
    -   趣味 (List): ["Game", "Coding"]
    -   スキル (Object): { html: "ok", css: "good" }

---

## Step 2: Visual Dictionary
-   **「情報のカタマリ」** → `{ ... }` (オブジェクト)
-   **「〜の〜」** → `.` (ドット)
    -   私の.名前 = `me.name`

---

## Step 3: Construct

### 🤖 Prompt Example
```text
【作りたいもの】
JSONデータの表示実験。

【データ構造 (JavaScript)】
以下の情報をオブジェクト（JSON）として定義してください。
変数名: `myProfile`
- name: (あなたの名前)
- age: (年齢)
- hobbies: (趣味のリスト)
- isMentoredByAI: true

【表示】
このデータを、`<pre>` タグの中に、`JSON.stringify` を使って見やすく表示してください。
```

---

## Step 4: Code Literacy
1.  **JSONのルール**
    -   データ全体が `{ }` で囲まれていますか？
    -   `key: value` の形になっていますか？
2.  **実験**
    -   `isMentoredByAI` を `false` に書き換えてみてください。

> **Why?**: 今後、APIを使うと必ずこの `{ : }` の形（JSON）でデータが返ってきます。これを見慣れておくことが重要です。
