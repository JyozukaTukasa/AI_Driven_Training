# Day 4: 記憶の城 (Cloud Database)

> **🗺️ World Map**: [Intro] > [Front] > [Back] > **[Cloud]** > [Dungeon] > [Real]

## 📍 Learning Roadmap

### 🎯 Today's Can-Do
- サーバー（処理）とデータベース（記憶）の違いを説明できる。
- **Firebase (Firestore)** にデータを保存し、読み出すことができる。
- **セキュリティルール** を設定し、他人のデータを消せないように守る。

---

## 📅 Morning Routine (09:00 - 10:00)

### 1. Planning (WBS)
- [ ] [WBS Template](../99_Resources/wbs_template.md) を使用。
- [ ] ここからはテンプレートなし。自分で昨日までの実績を元に見積もる。
- [ ] **AI上司によるレビュー (Mandatory)**: 「このスケジュールで無理がないか？」を必ず聞くこと。

### 2. Concept Research (AI Ban)
- `RDBMS NoSQL 違い`
- `Firestore Collection Document 構造`
- `Firebase Security Rules`

---

## 🏃‍♂️ Drills (数稽古) (10:00 - 12:00)

データを「ブラウザ」ではなく「クラウド（外部の金庫）」に保存します。
これで、リロードしても消えなくなります。

### ✍️ Step 1: Write (書き込み)
- [ ] [Drill 1: Write to Cloud](./drills/01_firestore_write.md) (日記を保存する)

### 📖 Step 2: Read (読み込み)
- [ ] [Drill 2: Read from Cloud](./drills/02_firestore_read.md) (日記を読み出す)

---

## 🏰 Mission (総合演習) (13:00 - 16:00)

世界中の誰もが閲覧・投稿できる、リアルタイムチャットを作ります。

- 👉 **[Mission: 消えないチャット (Global Chat)](./mission_cloud_db.md)**

---

## 📝 Closing (16:00 - 18:00)

- **Hardening**: ブラウザのコンソールからデータを削除しようとし、エラーになることを確認する。
- **Report**: 「なぜDBが必要なのか（変数じゃダメなのか）」を日報に書く。

---
**[Next]** 👉 [Day 5: 統合開発 (The Dungeon)](../Day05_Integrated/05_concept_design.md)
