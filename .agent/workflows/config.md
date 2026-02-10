---
description: 設定確認・変更を行う（Security Profile, etc.）
---

# Configuration Management

1. **現在の設定確認**
   Run: `cat .agent/config.json`
   現在の Security Profile と説明を表示する。

2. **設定変更 (Set Profile)**
   ユーザーが新しいプロファイルを指定した場合（例: `@[/config set L3]`）、`config.json` を更新する。
   Run: `echo '{"securityProfile": "L3", "description": "L3: Enterprise (Fintech/Healthcare)"}' > .agent/config.json`

3. **反映確認**
   「設定を **L3** に変更しました。以降のタスクはこの基準で実行されます。」と報告する。
