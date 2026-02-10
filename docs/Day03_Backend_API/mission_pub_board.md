# Mission: 酒場の掲示板 API (Pub Board)

Day 3 の Boss Battle です。
Drillで学んだ「Fetch」「JSON」「パラメータ」を使って、**「あなた自身のAPIサーバー」** を作ります。
ここからは、ブラウザ（Frontend）だけでなく、サーバー（Backend）のコードも書きます。

## 🎯 Goal (完成イメージ)
Python (FastAPI) を使って、以下の機能を持つAPIを作ります。

1.  `/hello?name=xxx` にアクセスすると、`{"message": "Hello, xxx"}` を返す (Drill 3の応用)。
2.  `/quests` にアクセスすると、クエスト一覧を **JSON** で返す (Drill 2の応用)。

---

## Step 1: Block Sketch
-   **サーバー (係の人)**
    -   「挨拶の窓口 (`/hello`)」を作る。
    -   「クエスト一覧の窓口 (`/quests`)」を作る。
-   **データ**
    -   クエストのリスト `[{"title": "スライム討伐"}, ...]`

---

## Step 2: Translation
-   **「窓口を作る」** → `@app.get("/path")` (Python/FastAPIの書き方)
-   **「返す」** → `return { ... }`

---

## Step 3: Construct

### 🤖 Prompt Example
```text
【作りたいもの】
PythonのFastAPIを使った、シンプルなAPIサーバー。

【機能】
1. ルート (`/`)
   - `{"message": "Welcome to the Pub Board API"}` を返す。

2. 挨拶窓口 (`/hello`)
   - クエリパラメータ `name` を受け取る。
   - `{"message": "Hello, {name}!"}` を返す。

3. クエスト窓口 (`/quests`)
   - 以下の配列データをJSONで返す。
   - `[{"id": 1, "title": "ハーブ集め", "reward": 100}, {"id": 2, "title": "ドラゴン討伐", "reward": 9999}]`
```

---

## Step 4: Code Literacy (解剖)
1.  **「窓口」はどこ？**
    -   `@app.get(...)` という行がいくつありますか？
    -   新しい窓口 `/shop` を作って、`{"item": "Potion"}` を返すように改造できますか？
2.  **「サーバーを起動する」命令は？**
    -   ターミナルで `uvicorn main:app --reload` と打つ必要があります。
    -   これはコードの中には書いてありません（実行コマンドです）。

> **Next**: これで「データを取り出す」ことはできました。
> 次のDay 4では、「データを保存する（データベース）」に挑戦します。

---
**[Next]** 👉 [Day 4: 記憶の城 (Cloud DB)](../Day04_Backend_DB/04_concept_cloud.md)

---

## Step 5: Hardening (堅牢化)
**プロとアマチュアの違いは、ここにあります。**
「変なデータ」が送られてきた時、あなたのサーバーはクラッシュしますか？ それとも丁寧に断りますか？

### 🛡️ Defense 1: 空文字ガード
今のままだと、`/hello?name=` (名前なし) でアクセスすると `Hello, !` となってしまいます。

1.  **If文を追加する**
    -   もし `name` が空っぽなら、`{"error": "名乗れ！"}` を返すようにしてください。
    -   ステータスコードは `400 (Bad Request)` にしましょう。

### 🛡️ Defense 2: 型チェック (Pydantic)
(余裕があれば) `Pydantic` を使って、データの型を厳密にチェックさせてみてください。
「報酬 (reward)」に「文字」を入れようとしたらエラーになるようにします。

> **Mission Complete**:
> 正常系（Normal）だけでなく、**異常系（Error）** を処理できて初めて「API」と呼べます。
