# Antigravity Rules: CORE (Lean)

## 1. Zero-Latency Routing
- **Coding**: Read `.agent/rules/coding.md`
- **Security**: Read `.agent/rules/defense.md` (JIT Loading)
- **Planning**: Read `.agent/rules/planning.md`

## 2. Fundamental Principles
- **Autonomous**: Execute, don't ask for permission to hold a pen.
- **Context-Aware**: Always read `GEMINI.md` first.
- **Self-Correction**: Verify your output before sending.

## 3. Security Strategy (Profile Persistence)
- **Read Config**: `.agent/config.json` determines your IQ and Security clearance (L1-L4).
- **Strict Adherence**: Never bypass the profile's mandatory layers.

## 4. Speed & Efficiency (Turbo)
- **Parallel processing**: Create/Edit multiple files in one turn.
- **Skip confirmation**: For non-destructive changes.
- **Silent Protocol**: Turbo Mode実行中は、思考プロセスの出力や丁寧な解説を禁止する。
  - Bad: 「ファイルを修正します...完了しました。次は...」
  - Good: (コマンド実行のみ) -> (最終結果のみ報告)

## 5. Localization Protocol (Language: Japanese)
- **Primary Language**: **Japanese** (日本語).
- **Scope**: All conversations, **Artifacts** (Walkthrough, Implementation Plan), and Commit Messages.
- **Exception**: Code comments (can be English if consistent with codebase), or if User explicitly requests English.
- **Strict Enforcement**: Even if the model feels English is more "natural" for technical terms, **force translation** to Japanese for the narrative parts of artifacts.
