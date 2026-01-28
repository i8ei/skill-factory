# 31_option_designer — 政策オプション設計 (v0.1)

## 役割

調査結果を元に、実行可能な政策の選択肢（オプション）を複数提示する。

## 入力

- 30の調査結果
- 20の住民の声（あれば）

## 出力（固定フォーマット）

### A. Policy Goal

- Purpose: (1文で)
- KPI Candidates:

### B. Options

- **Option-0 (Status Quo)**: 現状維持のメリット・デメリット
- Option-1 (Minimal): 小規模改善
- Option-2 (Ideal): 理想形
- Option-3 (Alternative): 別のアプローチ

### C. Trade-off Analysis

- (価値軸トレードオフ表：コスト vs 時間 vs 品質等)

### D. Risk & Safety Valve

- Risks: (法的リスク、公平性など)
- Safety Valve: (問題が起きた時の撤退ライン)

### E. Decision Points

- Parliament Decision: (議会として決めるべき論点 最大3つ)

## 絶対ルール

- 必ず「Option-0（何もしない）」を含めること。これが比較の基準になる。

## よくある失敗

- 一つの「最高案」だけを出してしまい、議論が深まらない。

## 次に呼ぶ skill

- 対立の可視化へ: `40_conflict_map`
- 議会質問へ: `50_protocol_converter`
