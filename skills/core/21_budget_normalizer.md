# 21_budget_normalizer — 予算書正規化 (v0.1)

## 役割

自治体ごとにフォーマットが違う予算・決算書を、比較可能な標準形式に変換する。

## 入力

- 予算書・決算書のPDFやExcel
- 事業別明細書

## 出力（固定フォーマット）

### Normalized Budget Data

- Fiscal Year:
- Department:
- Project Name:
- Amount (JPY):
- Source of Funds: (一般財源/国庫支出金/債等)
- KPI (あれば):

## 絶対ルール

- 数字の桁間違いは厳禁。
- 単位（千円、百万円）を必ず「円」または「統一単位」に揃える。

## よくある失敗

- 臨時財政対策債などの特殊な財源を見落とす。

## 次に呼ぶ skill

- 分析へ: `22_budget_insight_finder`
