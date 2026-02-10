# 🎨 Visual Assets Production List (制作指示書)

カリキュラムに必要な画像・動画素材のリストです。
**「誰が作るべきか（Source）」** を明確にし、AIによるハルシネーション（嘘のUI生成）を防ぎます。

## 🤖 Gemini Prompt Strategy (Anti-Hallucination)
AIは「文字」と「正確なUI」を描くのが苦手です。
ハルシネーション（謎の言語や崩れたボタン）を防ぐため、以下の戦略でプロンプトを構築しました。

1.  **Text-Free Policy**: 画像内に文字を入れさせない（後でパワポ等で入れる）。
2.  **Abstract/Schematic**: 「本物のUI」ではなく「概念図」や「ワイヤーフレーム」として描かせる。
3.  **Negative Prompt**: 「文字、コード、リアルな人間」を禁止する。

> **Common Style Prompt (共通スタイル)**:
> `Isometric educational diagram, clean white background, flat vector style. High contrast, distinct shapes. NO text, NO code, NO realistic faces. 80% professional technical illustration, 20% subtle RPG fantasy elements.`

---

## Day 0: Intro & Setup

| ID | File | Source | Content & Refined Prompt | Priority |
|:---|:---|:---|:---|:---|
| 0-1 | `00_concept_map.md` | **🎨 AI (Gemini)** | **World Map (Concept)**<br>文字なしの地図。4つのエリアが道で繋がっている。<br>**Prompt**: *Isometric fantasy map of 4 distinct regions connected by a path. 1. Forest, 2. Plains, 3. Mountains, 4. Floating Castle. Video game level select map style. Clean vector art, white background. No text labels.* | ★★★ |
| 0-2 | `00_concept_map.md` | **🎨 AI (Gemini)** | **Web Three Roles (Metaphor)**<br>文字なしのレストラン断面図。<br>**Prompt**: *Cutaway cross-section illustration of a tavern. Three zones: Dining area (client), Walking waiter (server), Kitchen with chef (database). Simple flat design, architectural sketch style. No text, no speech bubbles.* | ★★★ |
| 0-3 | `mission_setup.md` | **📷 User** | **Cursor Settings**<br>実画面。`Japanese Language Pack` の箇所。 | ★★☆ |
| 0-4 | `mission_setup.md` | **📷 User** | **GitHub Repo Creation**<br>実画面。`Private` チェックボックス。 | ★★★ |
| 0-5 | `mission_setup.md` | **📷 User** | **Git Clone**<br>実画面。`<> Code` ボタン。 | ★★☆ |

---

## Day 1: Frontend Basics

| ID | File | Source | Content & Refined Prompt | Priority |
|:---|:---|:---|:---|:---|
| 1-1 | `01_concept_structure.md` | **🎨 AI (Gemini)** | **The Box Model (Concept)**<br>文字なしの「箱の分解図」。<br>**Prompt**: *Exploded view diagram of a cube. Four layers: Inner glowing core, empty air gap, solid frame, outer space. Technical drawing style. Minimalist. No text labels.* | ★★★ |
| 1-2 | `drills/01_button.md` | **📷 User** | **Drill 1 Goal**<br>実画面。完成した青いボタン。 | ★★☆ |
| 1-3 | `01_concept_structure.md` | **🎨 AI (Gemini)** | **Visual Translation Flow (Metaphor)**<br>「手書きメモ」→「魔法の書」→「PC画面」の遷移。<br>**Prompt**: *Three stage transformation icon set. Left: Paper with scribble. Middle: Glowing book. Right: Computer screen with abstract lines. Connected by arrows. Flat vector icons. No text.* | ★★★ |
| 1-4 | `mission_profile_site.md` | **🎨 AI (Gemini)** | **Profile Site Mockup (Design)**<br>文字が潰れても良い「雰囲気」だけのUI。<br>**Prompt**: *Abstract UI design mockup of a RPG status screen. Dark mode. Bento grid layout with avatar and progress bars. Placeholder rectangles instead of text. Cyberpunk fantasy aesthetic.* | ★★★ |
| 1-5 | `mission_profile_site.md` | **🎨 AI (Gemini)** | **HTML vs CSS (Metaphor)**<br>「骨組み」と「装飾」の対比。<br>**Prompt**: *Side by side comparison. Left: Wireframe mannequin. Right: Fully clothed fashion model. Simple vector illustration. Minimalist style.* | ★★☆ |

---

## Day 2: JS Logic

| ID | File | Source | Content & Refined Prompt | Priority |
|:---|:---|:---|:---|:---|
| 2-1 | `02_concept_logic.md` | **🎨 AI (Gemini)** | **Event Listener (Metaphor)**<br>「スイッチ」と「扉」の連動。<br>**Prompt**: *A finger pressing a stone button, connected by a wire to an opening stone door. Simple mechanical diagram. Dungeon puzzle mechanism style. White background.* | ★★★ |
| 2-2 | `mission_monster_bestiary.md` | **📷 User** | **DevTools Console**<br>実画面。赤いエラーメッセージ。 | ★★★ |
| 2-3 | `mission_monster_bestiary.md` | **📷 User** | **Comment Out**<br>実画面。コードのコメントアウト。 | ★★☆ |
| 2-4 | `mission_monster_bestiary.md` | **📷 User** | **Counter Demo (GIF)**<br>画面収録。カウンターの動作。 | ★★☆ |

---

## Day 3: Backend API

| ID | File | Source | Content & Refined Prompt | Priority |
|:---|:---|:---|:---|:---|
| 3-1 | `03_concept_api.md` | **🎨 AI (Gemini)** | **API Endpoints (Metaphor)**<br>2つの窓口がある建物。<br>**Prompt**: *Isometric illustration of a building with two service windows. Queue of abstract people. Simple architectural style. No text labels.* | ★★★ |
| 3-2 | `03_concept_api.md` | **🎨 AI (Gemini)** | **Request/Response (Metaphor)**<br>行きと帰りの矢印。<br>**Prompt**: *Cycle diagram. An envelope flying right, a parcel flying left. Connected by looped arrows. Concept of exchange. Flat vector art.* | ★★☆ |
| 3-3 | `mission_pub_board.md` | **📷 User** | **JSON in Browser**<br>実画面。JSONデータ。 | ★★☆ |
| 3-4 | `mission_pub_board.md` | **📷 User** | **FastAPI Docs**<br>実画面。Swagger UI。 | ★☆☆ |

---

## Day 4: Cloud DB

| ID | File | Source | Content & Refined Prompt | Priority |
|:---|:---|:---|:---|:---|
| 4-1 | `04_concept_cloud.md` | **📷 User** | **Firestore Console**<br>実画面。コレクション一覧。 | ★★★ |
| 4-2 | `mission_cloud_db.md` | **📷 User** | **Realtime Sync (GIF)**<br>画面収録。同期の様子。 | ★★★ |
| 4-3 | `mission_cloud_db.md` | **📷 User** | **Rules Editor**<br>実画面。ルール編集画面。 | ★★☆ |
| 4-4 | `mission_cloud_db.md` | **📷 User** | **Access Denied**<br>実画面。権限エラー。 | ★★☆ |

---

## Day 5: Integration

| ID | File | Source | Content & Refined Prompt | Priority |
|:---|:---|:---|:---|:---|
| 5-1 | `05_concept_design.md` | **🎨 AI (Gemini)** | **System Architecture (Diagram)**<br>スマホと雲の接続図。<br>**Prompt**: *Simple network diagram. Left: Smartphone icon. Right: Cloud icon. Connected by a line. Clean technical illustration. Blue and white colors. No text.* | ★★★ |
| 5-2 | `mission_booking_system.md` | **🎨 AI (Gemini)** | **System Mockup (Design)**<br>雰囲気だけの予約サイト。<br>**Prompt**: *Abstract website mockup. Hero image of camping tent at night. Below are grid layouts representing booking forms. Wireframe style but with moody colors. No legible text.* | ★★★ |
| 5-3 | `31_implementation.md` | **📷 User** | **React Error Overlay**<br>実画面。赤画面エラー。 | ★★☆ |
| 5-4 | `31_implementation.md` | **📷 User** | **Deployment Success**<br>実画面。デプロイ完了ログ。 | ★★★ |

---

## Resources (Glossary)

| ID | File | Source | Content & Refined Prompt | Priority |
|:---|:---|:---|:---|:---|
| R-1 | `visual_dictionary.md` | **🎨 AI (Gemini)** | **Tag Cards (Visual Dictionary)**<br>文字なしの抽象アイコン。<br>**Prompt**: *Set of 3 simple icons. 1. A cardboard box. 2. A picture frame. 3. A chain link. Consistent cute vector style. White background. No text.* | ★★★ |
| R-2 | `glossary.md` | **🎨 AI (Gemini)** | **Architecture Comparison**<br>上書き vs 完成品。<br>**Prompt**: *Conceptual comparison diagram. Left: A robot arm drawing on a screen. Right: A printer outputting a finished sheet. Simple flowchart style. No text.* | ★☆☆ |

---

## Day 0: Intro & Setup

| ID | File | Source | Content & Gemini Prompt | Priority |
|:---|:---|:---|:---|:---|
| 0-1 | `00_concept_map.md` | **🎨 AI (Gemini)** | **World Map (Concept)**<br>RPG風の地図だが、道のりは明確なロードマップ。<br>**Prompt**: *Isometric map of a learning journey. Four distinct regions connected by a clear path: 1. Forest of Intro, 2. Plains of Frontend, 3. Mountains of Backend, 4. Sky Castle of Cloud. Game level select screen style but clean and educational. White background.* | ★★★ |
| 0-2 | `00_concept_map.md` | **🎨 AI (Gemini)** | **Web Three Roles (Metaphor)**<br>レストランの断面図。<br>**Prompt**: *Isometric cutaway view of a fantasy tavern. Three zones: 1. Client (Adventurer ordering at table), 2. Server (Waiter carrying tray), 3. Database (Chef cooking in kitchen). Educational diagram style, distinct zones, clean lines, white background.* | ★★★ |
| 0-3 | `mission_setup.md` | **📷 User** | **Cursor Settings**<br>Cursorの設定画面で `Japanese Language Pack` をインストールしている瞬間。<br>※「拡張機能」アイコンの位置を示すため。 | ★★☆ |
| 0-4 | `mission_setup.md` | **📷 User** | **GitHub Repo Creation**<br>`Private` と `Add README` にチェックが入った作成画面。<br>※ここを間違えるとPublicになるため、実画面必須。 | ★★★ |
| 0-5 | `mission_setup.md` | **📷 User** | **Git Clone**<br>GitHubの緑色の `<> Code` ボタンを押し、URLをコピーしている様子。<br>※UIが変わる可能性があるため、最新の実画面が良い。 | ★★☆ |

---

## Day 1: Frontend Basics

| ID | File | Source | Content & Gemini Prompt | Priority |
|:---|:---|:---|:---|:---|
| 1-1 | `01_concept_structure.md` | **🎨 AI (Gemini)** | **The Box Model (Concept)**<br>箱の構造図。ファンタジーの宝箱を解剖するイメージ。<br>**Prompt**: *Exploded view diagram of a treasure chest representing CSS Box Model. Layers: 1. Content (Glowing Gem inside), 2. Padding (Air gap), 3. Border (Wooden frame), 4. Margin (Space outside). Technical labeling style, clean vector art, white background.* | ★★★ |
| 1-2 | `drills/01_button.md` | **📷 User** | **Drill 1 Goal**<br>完成した「青いボタン（影付き、角丸）」のスクリーンショット。<br>※「これが作れれば正解」という基準値を示すため。 | ★★☆ |
| 1-3 | `01_concept_structure.md` | **🎨 AI (Gemini)** | **Visual Translation Flow (Metaphor)**<br>「メモ」が「辞書」を通って「コード」になる魔法。<br>**Prompt**: *Transformation process diagram. Left: Hand-drawn paper sketch. Middle: Magic spellbook (Dictionary). Right: Glowing computer code. Connected by arrows. Flat icon style, simple and clear.* | ★★★ |
| 1-4 | `mission_profile_site.md` | **🎨 AI (Gemini)** | **Profile Site Mockup (Design)**<br>RPGステータス画面風のWebデザイン。<br>**Prompt**: *Web UI design mockup. RPG Character Status Screen theme. Dark mode. Bento grid layout showing Avatar face, HP/MP bars, and Strength stats. Modern clean UI with retro game flavor. High resolution.* | ★★★ |
| 1-5 | `mission_profile_site.md` | **🎨 AI (Gemini)** | **HTML vs CSS (Metaphor)**<br>「骨」と「装備」の比較。<br>**Prompt**: *Comparison illustration. Left: Wireframe skeleton of a knight (labeled HTML). Right: Fully armored and colored knight (labeled CSS). Educational comparison, simple clear lines, white background.* | ★★☆ |

---

## Day 2: JS Logic

| ID | File | Source | Content & Gemini Prompt | Priority |
|:---|:---|:---|:---|:---|
| 2-1 | `02_concept_logic.md` | **🎨 AI (Gemini)** | **Event Listener (Metaphor)**<br>「ボタン（原因）」と「ドア（結果）」の関係。<br>**Prompt**: *Cause and effect diagram. Action: Finger pressing a dungeon stone button. Reaction: A stone door opening. Connected by a wire. Simple technical diagram style, subtle fantasy elements.* | ★★★ |
| 2-2 | `mission_monster_bestiary.md` | **📷 User** | **DevTools Console**<br>ChromeのF12コンソール画面。赤いエラーメッセージが出ている状態。<br>※初心者は「赤い文字」を見るとパニックになるため、実物を見せて安心させる。 | ★★★ |
| 2-3 | `mission_monster_bestiary.md` | **📷 User** | **Comment Out**<br>コードに `//` を入れた状態 (エディタ画面) と、ボタンが反応しない画面。<br>※コメントアウトの色（緑など）を見せるため。 | ★★☆ |
| 2-4 | `mission_monster_bestiary.md` | **📷 User** | **Counter Demo (GIF)**<br>画面収録。ボタンをクリック連打し、数字が `0 -> 1 -> 2` と増える様子。<br>※「動き」は静止画では伝わらないため。 | ★★☆ |

---

## Day 3: Backend API

| ID | File | Source | Content & Gemini Prompt | Priority |
|:---|:---|:---|:---|:---|
| 3-1 | `03_concept_api.md` | **🎨 AI (Gemini)** | **API Endpoints (Metaphor)**<br>役所の窓口。<br>**Prompt**: *Isometric illustration of a Guild Hall reception desk. Two windows. Window 1 labeled '/hello' with a greeter. Window 2 labeled '/quest' with a scroll. Clean educational vector art, white background.* | ★★★ |
| 3-2 | `03_concept_api.md` | **🎨 AI (Gemini)** | **Request/Response (Metaphor)**<br>手紙の往復。<br>**Prompt**: *Communication cycle diagram. Left: Adventurer sending a letter (Request). Right: Guild master sending a package back (Response). Connected by loop arrows. Flat design, educational.* | ★★☆ |
| 3-3 | `mission_pub_board.md` | **📷 User** | **JSON in Browser**<br>ブラウザ画面。装飾のないテキストデータ（JSON）が表示されている様子。<br>※「壊れてるわけじゃない」と伝えるため。 | ★★☆ |
| 3-4 | `mission_pub_board.md` | **📷 User** | **FastAPI Docs**<br>`/docs` にアクセスし、Swagger UI (青いヘッダーの画面) が出ている様子。<br>※「自動で説明書ができる」という感動を伝えるため。 | ★☆☆ |

---

## Day 4: Cloud DB

| ID | File | Source | Content & Gemini Prompt | Priority |
|:---|:---|:---|:---|:---|
| 4-1 | `04_concept_cloud.md` | **📷 User** | **Firestore Console**<br>Firebaseコンソール画面。ColletionとDocumentの2カラム表示。<br>※UIが独特で迷いやすいため、実画面必須。 | ★★★ |
| 4-2 | `mission_cloud_db.md` | **📷 User** | **Realtime Sync (GIF)**<br>画面収録。2つのウィンドウを並べ、片方で投稿→もう片方が即座に反映される様子。<br>※Firebase最大の魅力（魔法）なので、必ず動画で見せる。 | ★★★ |
| 4-3 | `mission_cloud_db.md` | **📷 User** | **Rules Editor**<br>Firebaseの「Rules」タブのエディタ画面。<br>※Codeを書く場所がブラウザ上にあることを示す。 | ★★☆ |
| 4-4 | `mission_cloud_db.md` | **📷 User** | **Access Denied**<br>コンソールに出た赤いエラー `Missing or insufficient permissions`。<br>※「正しくガードされた」ことの証明。 | ★★☆ |

---

## Day 5: Integration

| ID | File | Source | Content & Gemini Prompt | Priority |
|:---|:---|:---|:---|:---|
| 5-1 | `05_concept_design.md` | **🎨 AI (Gemini)** | **System Architecture (Diagram)**<br>フロントとDBの接続図。<br>**Prompt**: *Web application architecture diagram. Left: Smartphone and PC (React). Right: Cloud Database icon (Firestore). Connected by data lines. Crystal clear technical style, blue color scheme.* | ★★★ |
| 5-2 | `mission_booking_system.md` | **🎨 AI (Gemini)** | **System Mockup (Design)**<br>完成予想図。<br>**Prompt**: *Web website design mockup. Luxury Glamping Booking Site. Hero image of a tent under starry night. Booking calendar form. Professional modern UI, elegant atmosphere.* | ★★★ |
| 5-3 | `31_implementation.md` | **📷 User** | **React Error Overlay**<br>Reactのエラーで画面が真っ赤になった状態。<br>※「これがRed Screen of Death」と教えるため。 | ★★☆ |
| 5-4 | `31_implementation.md` | **📷 User** | **Deployment Success**<br>ターミナルのログ。`Deploy complete!` の文字と `Hosting URL`。<br>※最後の達成感を共有するため。 | ★★★ |

---

## Resources (Glossary)

| ID | File | Source | Content & Gemini Prompt | Priority |
|:---|:---|:---|:---|:---|
| R-1 | `visual_dictionary.md` | **🎨 AI (Gemini)** | **Tag Cards (Visual Dictionary)**<br>タグの擬人化カード。<br>**Prompt**: *Set of trading card designs for HTML tags. 'div' represented as a cardboard box. 'img' represented as a picture frame. 'a' represented as a chain link. Cute mascot style, clean vector art.* | ★★★ |
| R-2 | `glossary.md` | **🎨 AI (Gemini)** | **Architecture Comparison**<br>SPA vs SSR。<br>**Prompt**: *Comparison diagram. Left (SPA): Digital paper being overwritten by a robot arm. Right (SSR): A printer delivering a fully printed page. Educational metaphor, simple and clear.* | ★☆☆ |

---

## Day 0: Intro & Setup

| ID | File | Source | Content & Instructions | Priority |
|:---|:---|:---|:---|:---|
| 0-1 | `00_concept_map.md` | **🎨 AI** | **World Map**<br>RPG風の地図。「Introの森」「Front平原」「Back山脈」「Cloud城」などが描かれている。<br>Prompt: *Fantasy world map, rpg style, 6 regions, distinct landscape features, adventure map* | ★★★ |
| 0-2 | `00_concept_map.md` | **🎨 AI** | **Web Three Roles**<br>レストランのイラスト。Client(客), Server(ウェイター), DB(厨房)の関係。<br>Prompt: *Restaurant isometric illustration, customer ordering, waiter carrying food, chef cooking in kitchen, simple flat design* | ★★★ |
| 0-3 | `mission_setup.md` | **📷 User** | **Cursor Settings**<br>Cursorの設定画面で `Japanese Language Pack` をインストールしている瞬間。<br>※「拡張機能」アイコンの位置を示すため。 | ★★☆ |
| 0-4 | `mission_setup.md` | **📷 User** | **GitHub Repo Creation**<br>`Private` と `Add README` にチェックが入った作成画面。<br>※ここを間違えるとPublicになるため、実画面必須。 | ★★★ |
| 0-5 | `mission_setup.md` | **📷 User** | **Git Clone**<br>GitHubの緑色の `<> Code` ボタンを押し、URLをコピーしている様子。<br>※UIが変わる可能性があるため、最新の実画面が良い。 | ★★☆ |

---

## Day 1: Frontend Basics

| ID | File | Source | Content & Instructions | Priority |
|:---|:---|:---|:---|:---|
| 1-1 | `01_concept_structure.md` | **🎨 AI** | **The Box Model**<br>箱の解剖図。Margin(外), Border(枠), Padding(内), Content(中身)を色分けした図。<br>Prompt: *CSS Box Model diagram, 3D cube exploded view, margin border padding labels, educational, clean* | ★★★ |
| 1-2 | `drills/01_button.md` | **📷 User** | **Drill 1 Goal**<br>完成した「青いボタン（影付き、角丸）」のスクリーンショット。<br>※「これが作れれば正解」という基準値を示すため。 | ★★☆ |
| 1-3 | `01_concept_structure.md` | **🎨 AI** | **Visual Translation Flow**<br>メモ書き(日本語)が、タグ(Dictionary)を通って、コード(英語)に変換される流れ。<br>Prompt: *Process flow diagram, hand drawn sketch turning into structured code, magic transformation, flat icon style* | ★★★ |
| 1-4 | `mission_profile_site.md` | **🎨 AI** | **Profile Site Mockup**<br>RPGのステータス画面風のWebサイトデザイン。ダークモード。<br>Prompt: *RPG status screen UI design, dark mode, pixel art style, character profile stats, retro game interface* | ★★★ |
| 1-5 | `mission_profile_site.md` | **🎨 AI** | **HTML vs CSS**<br>「骨だけのガイコツ(HTML)」と「服を着たおしゃれな人(CSS)」の対比。<br>Prompt: *Skeleton vs Fashion Model comparison, structure vs style, simple cartoon style, educational* | ★★☆ |

---

## Day 2: JS Logic

| ID | File | Source | Content & Instructions | Priority |
|:---|:---|:---|:---|:---|
| 2-1 | `02_concept_logic.md` | **🎨 AI** | **Event Listener**<br>「玄関のチャイムを押す指」と「ドアを開ける住人」。<br>Prompt: *Person ringing doorbell, another person opening door, cause and effect illustration, simple vector art* | ★★★ |
| 2-2 | `mission_monster_bestiary.md` | **📷 User** | **DevTools Console**<br>ChromeのF12コンソール画面。赤いエラーメッセージが出ている状態。<br>※初心者は「赤い文字」を見るとパニックになるため、実物を見せて安心させる。 | ★★★ |
| 2-3 | `mission_monster_bestiary.md` | **📷 User** | **Comment Out**<br>コードに `//` を入れた状態 (エディタ画面) と、ボタンが反応しない画面。<br>※コメントアウトの色（緑など）を見せるため。 | ★★☆ |
| 2-4 | `mission_monster_bestiary.md` | **📷 User** | **Counter Demo (GIF)**<br>画面収録。ボタンをクリック連打し、数字が `0 -> 1 -> 2` と増える様子。<br>※「動き」は静止画では伝わらないため。 | ★★☆ |

---

## Day 3: Backend API

| ID | File | Source | Content & Instructions | Priority |
|:---|:---|:---|:---|:---|
| 3-1 | `03_concept_api.md` | **🎨 AI** | **API Endpoints**<br>役所の窓口のイラスト。`/hello`係と`/quests`係がいる。<br>Prompt: *City hall service counters, queue of people, signposts reading '/hello' and '/quests', isometric illustration* | ★★★ |
| 3-2 | `03_concept_api.md` | **🎨 AI** | **Request/Response**<br>手紙（Request）を出して、小包（Response）が届く往復図。<br>Prompt: *Mail delivery cycle, sending letter, receiving package, arrow flow diagram, flat design* | ★★☆ |
| 3-3 | `mission_pub_board.md` | **📷 User** | **JSON in Browser**<br>ブラウザ画面。装飾のないテキストデータ（JSON）が表示されている様子。<br>※「壊れてるわけじゃない」と伝えるため。 | ★★☆ |
| 3-4 | `mission_pub_board.md` | **📷 User** | **FastAPI Docs**<br>`/docs` にアクセスし、Swagger UI (青いヘッダーの画面) が出ている様子。<br>※「自動で説明書ができる」という感動を伝えるため。 | ★☆☆ |

---

## Day 4: Cloud DB

| ID | File | Source | Content & Instructions | Priority |
|:---|:---|:---|:---|:---|
| 4-1 | `04_concept_cloud.md` | **📷 User** | **Firestore Console**<br>Firebaseコンソール画面。ColletionとDocumentの2カラム表示。<br>※UIが独特で迷いやすいため、実画面必須。 | ★★★ |
| 4-2 | `mission_cloud_db.md` | **📷 User** | **Realtime Sync (GIF)**<br>画面収録。2つのウィンドウを並べ、片方で投稿→もう片方が即座に反映される様子。<br>※Firebase最大の魅力（魔法）なので、必ず動画で見せる。 | ★★★ |
| 4-3 | `mission_cloud_db.md` | **📷 User** | **Rules Editor**<br>Firebaseの「Rules」タブのエディタ画面。<br>※Codeを書く場所がブラウザ上にあることを示す。 | ★★☆ |
| 4-4 | `mission_cloud_db.md` | **📷 User** | **Access Denied**<br>コンソールに出た赤いエラー `Missing or insufficient permissions`。<br>※「正しくガードされた」ことの証明。 | ★★☆ |

---

## Day 5: Integration

| ID | File | Source | Content & Instructions | Priority |
|:---|:---|:---|:---|:---|
| 5-1 | `05_concept_design.md` | **🎨 AI** | **System Architecture**<br>React (スマホ/PC) から Firestore (雲) に線が繋がっている構成図。<br>Prompt: *Web application architecture diagram, React frontend connecting to Cloud Database, clean tech lines, blue color scheme* | ★★★ |
| 5-2 | `mission_booking_system.md` | **🎨 AI** | **System Mockup (Idea)**<br>こんなアプリを作ろう、という理想図。グランピング予約サイト。<br>Prompt: *Glamping booking website design, luxury camping, starlit night background, booking form, modern UI* | ★★★ |
| 5-3 | `31_implementation.md` | **📷 User** | **React Error Overlay**<br>Reactのエラーで画面が真っ赤になった状態。<br>※「これがRed Screen of Death」と教えるため。 | ★★☆ |
| 5-4 | `31_implementation.md` | **📷 User** | **Deployment Success**<br>ターミナルのログ。`Deploy complete!` の文字と `Hosting URL`。<br>※最後の達成感を共有するため。 | ★★★ |

---

## Resources (Glossary)

| ID | File | Source | Content & Instructions | Priority |
|:---|:---|:---|:---|:---|
| R-1 | `visual_dictionary.md` | **🎨 AI** | **Tag Cards (Visual Dictionary)**<br>タグを擬人化・カード化したもの。<br>Prompt: *Trading card design for HTML tags, 'div' as a box, 'img' as a picture frame, 'a' as a chain link, cute mascot style* | ★★★ |
| R-2 | `glossary.md` | **🎨 AI** | **Architecture Comparison**<br>SPA (紙芝居) vs SSR (完成品配達) の違い。<br>Prompt: *Comparison diagram, SPA overwriting paper, SSR delivering finished painting, explanatory illustration* | ★☆☆ |

