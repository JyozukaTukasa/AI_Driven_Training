# セーフティネット設計書: "The Safety Nets"

研修生の「詰み（挫折）」を防止するための、最後の防衛ラインを定義します。

## 1. 正解の書 (The Solution Grimoire)
「どうしても動かない」時のためのカンニングペーパー（正解コード集）の提供方法。
GitHubリポジトリは配布しないため、マニュアルの一部として提供します。

### 構成 (Directory)
`docs/99_solutions/` 配下に、Dayごとの完成形コードを格納します。

```text
docs/99_solutions/
├── day01/
│   ├── index.html  # 構造の正解
│   └── style.css   # 装飾の正解
├── day03/
│   └── main.py     # APIサーバーの正解
├── day05/
│   └── ...         # 予約システムの正解（Auth/DB接続含む）
└── README.md       # 「使い方の注意（コピペは最終手段）」
```

### 提供ルール
- **原則**: マニュアル本文からはリンクしない。「どうしても無理な場合のみ、巻末の『正解の書』を参照せよ」と案内する。
- **解説**: コードだけでなく、「なぜこの書き方なのか」の短い解説コメントを入れる。

---

## 2. エラー魔物図鑑 (The Monster Encyclopedia)
よくあるエラー（Monster）と、その倒し方をまとめた `docs/99_resources/troubleshooting.md` の構成。

| Error Type | 症状 (Symptom) | 対処法 (Solution) |
|:---|:---|:---|
| **404 Not Found** | ページが見つからない | URLミス、ファイル配置ミス |
| **The CORS Hydra** | 赤文字で `CORS error` と出る | FastAPIに `CORSMiddleware` を追加 |
| **The Git Conflict** | `CONFLICT` と出て進めない | 落ち着いてVS Codeで「Accept Current Change」を選ぶ |
| **The Whiteout** | 画面が真っ白で何も出ない | F12 (DevTools) を開いてConsoleを見る |

### 運用
- Mentor Botのプロンプトに「エラー名を伝えたら、ヒント（調べ方）を案内せよ」と仕込むことで、自己解決を促す。

---

## 3. 用語集 (The Glossary)
専門用語を「冒険用語」として再定義する `docs/99_resources/glossary.md`。

- **API**: 注文を聞いて料理を出す「ウェイター」。
- **Database**: 荷物を預かってくれる「クローク/倉庫」。
- **Deploy**: 自分の城を世界地図に「公開」すること。
- **Commit**: リポジトリへの記録は「セーブポイント」であると教える。

---
これらを準備することで、「答えがない」「言葉がわからない」という不安を払拭します。
