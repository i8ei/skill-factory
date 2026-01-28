# 12_safety_and_privacy_guard — 公開安全ガード (v0.1)

## 役割

成果物を公開する直前に、個人情報・偏見・不正確な断定がないかチェックする。

## 入力

- 公開予定の文章（広報誌、SNS投稿、議会発言案）

## 出力（固定フォーマット）

### Safety Check Report

- Personal Info: <Pass | Fail>
- Substantiation: <Pass | Fail> (断定の根拠はあるか)
- Fairness: <Pass | Fail> (特定の誰かを攻撃していないか)
- Source Consistency: <Pass | Fail> (11の台帳と合致するか)
- Scope Check: <Internal | Limited | Public>

## 絶対ルール

- Failが1つでもあれば公開禁止。
- 修正案を必ず具体的に出す。

## よくある失敗

- 「誰も見てないだろう」と甘く見て、個人名を出してしまう。

## 次に呼ぶ skill

- 修正が必要なら: `60_public_explainer` (再編集)
- OKなら: (完了)
