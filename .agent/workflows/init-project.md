---
description: プロジェクトの初期セットアップを行う（GEMINI.md作成など）
---

# プロジェクト初期化フロー (Smart Initialization)

1. **Smart Discovery & Context Inference**
   // turbo
   `GEMINI.md` が存在しない場合、以下の推論を行いドラフトを作成する。
   1. **Tech Stack**: `package.json`, `go.mod`, `pom.xml`, `requirements.txt` 等をスキャン。
   2. **Purpose**: `README.md` の冒頭から抽出。
   3. **Security Profile**:
      - Private repo + Enterprise keywords -> **L3**
      - Public repo / Personal -> **L2** (Default)
   4. **Storage**: Standard (`./GEMINI.md`)

2. **Interactive Confirmation (One-Shot)**
   推論結果を提示し、ユーザーに確認を求める。
   
   > **[Antigravity Setup]**
   > I detected the following context:
   > - **Stack**: [Inferred Stack, e.g. Next.js + Tailwind]
   > - **Purpose**: [Inferred Purpose]
   > - **Security**: [L2/L3]
   >
   > Create `GEMINI.md` with this configuration? (Y/n/Modify)

3. **Generation**
   - **Yes**: 推論内容で `GEMINI.md` を生成。
   - **Modify**: ユーザーの指示に従い修正して生成。
   - **No**: 手動作成モードへ移行（テンプレートのみ出力）。

4. **Directory Setup**
   // turbo
   `mkdir docs` (if not exists)

5. **Linter & Tools Setup**
   技術スタックに合わせて、必要な Linter/Formatter (ESLint, Ultralint etc.) の導入を提案する。

