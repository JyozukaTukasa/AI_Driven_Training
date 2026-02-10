---
description: 作業内容を保存し、セッションを安全に終了する
---

# Wrap Up (Session Reset)

現在の作業状態を記録し、安心してチャットをリセットできる状態を作ります。

## 1. 状態の保存 (Context Checkpointing)
次回起動時(`onboard`)のトークン節約のため、**「未来の自分への引き継ぎ書」** を作成します。

1. **Checkpoint作成**
   以下の内容を `memory/checkpoint.md` に上書き保存してください。
   - **Current Phase**: (例: Implementation)
   - **Active Task**: (例: ユーザー認証機能の実装)
   - **Next Step**: (例: 統合テストの作成)
   - **Security Level**: (例: L2 Standard)

   Run: `echo "# Checkpoint\nPhase: ...\nTask: ...\nNext: ...\nSec: ..." > memory/checkpoint.md`

2. **Task保存**
   現在のタスクリストも確認します。
   Run: `cat task.md`

## 2. 完了メッセージ (Completion)
ユーザーに対して以下のメッセージを表示して終了してください。

> **✅ Session Wrapped Up**
> 
> 現在の作業状況を保存しました。
> コンテキストをクリアにするため、このチャットをアーカイブし、新しいチャットを開始してください。
> 
> 次のチャットでは、再開用コマンド `@[/onboard]` を実行してください。
