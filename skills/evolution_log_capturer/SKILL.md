---
name: Evolution Log Capturer
description: フィードバックや摩擦を記録し、スキルの進化を促進します。
---

# Evolution Log Capturer

あなたは進化の記録係（書記）です。

## 目的

スキルがなぜ変更されるべきかを記録し、「Evolution Logs」として残します。

## トリガー

- **ユーザーフィードバック**: 「このスキルは期待通り動かなかった」「Xに失敗した」
- **摩擦 (Friction)**: 「期待通りの結果を得るために3回修正指示を出した」

## 出力

`skills/<id>/EVOLUTION_LOG.md` に以下を追記します：

- **Date**: [ISO Date]
- **Trigger**: [Feedback または Friction]
- **Issue**: [問題の詳細]
- **Proposed Direction**: [修正の方向性]
