# プロジェクト定義書 (GEMINI.md)

## 1. プロジェクト目的 (Purpose)
- **製品名**: AI駆動開発新人研修マニュアル (AI-Driven Dev Training Kit)
- **目的**: 
  - プログラミング未経験者を10日間で「AIを活用して自走できるエンジニア」に育成する。
  - **「引き出し戦略 (The Drawer Strategy)」**: 暗記ではなく、Index（索引）を作り、必要な情報を引き出して判断する能力を養う。
  - **「サバイバル・エンジニア」**: 未知の技術やトラブルに遭遇しても、自力で解決策を見つけ出せる基礎体力をつける。
  - **「Trainee Experience (TX)」**: 挫折させず、孤独にさせず、楽しく完走させる（Safety Net & Gamification）。
- **ターゲット**: 
  - エンジニア未経験者。
  - AIへの指示出し（プロンプト）未経験者。
  - 変化の激しい業界で生き残るための「メタスキル（学習の仕方）」を身につけたい人。

## 2. コア・コンセプト (Core Concepts)
1.  **The Drawer Strategy (引き出し戦略)**
    -   すべてを暗記せず、「引き出し（Index）」を作って検索する。
2.  **Universal Engineering (普遍的エンジニアリング)**
    -   タグや構文ではなく、「UI構造」「データフロー」などの共通概念を学ぶ。
3.  **Gradual WBS (段階的自走)**
    -   Trace (真似る) -> Adjust (調整する) -> Create (作る) の3ステップで、タスク管理能力を身につける。
4.  **The Guardian Manager (守護者)**
    -   AIを「失敗させないための頼れるPM」として定義し、無謀な計画を未然に防ぐ。

## 3. カリキュラム概要 (10 Days Roadmap)
- **Day 0: Mindset & Tools**
  - AI駆動開発の地図、武器（Cursor/Git）、心構え。
- **Day 1-2: Structure (Frontend)**
  - UIの構造化（箱と余白）。"Visual Dictionary" を使った言語化訓練。
- **Day 3-4: Connection (Backend/Cloud)**
  - データの流れ。APIとDBの概念理解。"Guardian Manager" による見積もり訓練。
- **Day 5: Integration (The Dungeon)**
  - 予約システム開発。WBS作成からデプロイまで、フルスタックな自走。
- **Day 6-10: Real World**
  - (Phase 2にて詳細規定)

## 4. 成果物 (Deliverables)
- **研修マニュアル (PDF出力用)**
  - `docs/00_Curriculum/` 配下に集約。
- **Resources**
  - `Visual Dictionary`, `WBS Template`, `Mentor Prompt`。

## 5. 技術スタック & ツール
- **Development**: Cursor (AI Editor), VS Code.
- **Frontend**: HTML/CSS/JS (Foundation) -> React (Optional).
- **Backend**: Python (FastAPI).
- **Infra**: Firebase (Hosting/Auth).
- **AI**: Claude 3.5 Sonnet / GPT-4o (via Cursor).

## 6. プロジェクト運用ルール
- **言語**: 日本語 (Japanese).
- **ドキュメント管理**: `docs/` 配下で管理。
- **図解**: Mermaid記法または画像埋め込みで「可視化」を徹底する。
