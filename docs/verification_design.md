# 検証設計書: "The Proof of Wisdom" (v2)

「読んだつもり」を排除し、アウトプットで理解度を測定する仕組み（Quality Assurance）。
全ての成果物は **Git** で管理し、コミットログを「成長の記録」とする。

## 戦略1: AIへの解説 (The Lenient Feynman Test)
教わるのではなく、**「新人がAIに教える」**スタイルをとる。

- **仕組み**: 
    - 各章の終わりに、Mentor Botが「今の機能、どういう仕組みで動いたの？Webを知らないおばあちゃんでもわかるように教えて？」と質問する。
    - 新人は自分の言葉で説明を入力する。
- **合格基準 (Good Enough)**:
    - 専門用語が間違っていてもOK（例：「リクエスト」を「注文」と言ってもOK）。
    - **「処理の流れ（AしたらBになる）」** が合っていれば合格とする。
    - AIは「完璧です！」または「惜しい！ここの順番だけ逆かも？」と優しく返す設定にする。

## 戦略2: 成果物定義 (Git Deliverables)
「何をもって完了とするか」をファイルレベルで定義する。

| Day | Project | 提出物 (Git Commit) | 条件 | Skill Level |
|:---:|:---|:---|:---|:---|
| **0** | Setup | `README.md` | "Hello World" と自分の意気込みを追記してCommitされていること。 |
| **1** | Profile | `projects/day01/index.html`<br>`projects/day01/style.css` | ブラウザで表示崩れがないこと。<br>画像フォルダが整理されていること。 |
| **2** | Counter | `projects/day02/app.js` | クリックして数字が増えること。 |
| **3** | API | `projects/day03/main.py` | `/omikuji` にアクセスしてJSONが返ること。 |
| **4** | Cloud | `projects/day04/firebase_config.py` | Firestoreへの書き込み成功ログがスクショに残っていること。 |
| **5** | Glamping | `projects/day05/` | 予約画面が表示され、ボタンが反応すること（UI実装）。 |
| **6** | Chart | `projects/day06/` | グラフが表示されていること。 |
| **10** | Final | `projects/final-app/` | READMEに「アプリの概要・動かし方」が書かれていること。 |

## 戦略3: 破壊工作テスト (The Sabotage Test)
「あえて壊す」ことで理解を深める。

- **仕組み**:
    - **Day 2**: 「`addEventListener` の行をコメントアウトして実行してみて。何が起きなくなった？」
    - **Day 3**: 「APIの `return` を消してみて。ブラウザはどういう反応をする？」
- **レポート**:
    - 壊した結果（予想通り動かなくなったこと）を、コミットメッセージや日報に1行書かせる。

## 戦略4: 図解提出 (Visual Proof)
- **Day 5**: 予約システムの「画面遷移図（手書きOK）」を写真に撮り、`projects/day05/design/` に入れる。

---

この設計により、
1.  **AIへの説明** で「腹落ち」を確認し、
2.  **Gitへのコミット** で「物理的な証拠」を残させます。
