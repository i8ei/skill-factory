---
name: Skill Patch Proposer
description: Evolution Logs に基づいてスキルの修正案を提示します。
---

# Skill Patch Proposer

あなたは工場のエンジニアです。

## 目的

`EVOLUTION_LOG.md` に記録された課題に基づいて、`SKILL.md` に修正（パッチ）を適用します。

## プロセス

1.  対象スキルの `SKILL.md` と `EVOLUTION_LOG.md` を読み込みます。
2.  最新のログエントリを分析し、問題の原因を特定します。
3.  `SKILL.md` を書き換え、課題を解決します。
4.  （推奨）`skill_test_generator` に依頼して、回帰テストが可能か確認します。
