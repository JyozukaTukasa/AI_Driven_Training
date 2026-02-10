# Drill 3: Query Parameters (検索の仕組み)

URLの後ろについている `?q=cat` みたいな文字。これを **クエリパラメータ** と言います。
「情報を受け取って、表示を変える」練習です。

## 🎯 Goal
-   URLに `?name=Tanaka` と入れてアクセスすると、画面に "Hello, Tanaka!" と出る。
-   `?name=Sato` に変えると、"Hello, Sato!" に変わる。

---

## Step 1: Block Sketch
1.  **入力**: URLを見る。
2.  **解析**: `?` の後ろにある `name` を探す。
3.  **表示**: 画面の挨拶を書き換える。

---

## Step 3: Construct

### 🤖 Prompt Example
```text
【作りたいもの】
URLの名前によって挨拶が変わるページ。

【動き】
1. ページが開かれたら、現在のURLの「クエリパラメータ (`name`)」を取得してください。
   - ヒント: `URLSearchParams` を使う
2. もし `name` があれば、画面に `Hello, {name}!` と表示してください。
3. なければ、`Hello, Guest!` と表示してください。
```

---

## Step 4: Code Literacy
1.  **URLを読み取る呪文**
    -   `window.location.search` や `URLSearchParams` を探してください。
    -   これが「ブラウザのアドレスバーを見る」という命令です。

> **Try**: ブラウザのアドレスバーの末尾に `?name=YourName` を手入力してエンター、ページをリロードしてみてください。挨拶が変わりましたか？
