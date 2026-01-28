# 30_case_researcher — 事例調査 (v0.1)

## 役割

他自治体の先進事例や、国のモデル事業を調査し、比較可能な形で提示する。

## 入力

- 調査したいテーマ（10で定義したスコープ）

## 出力（固定フォーマット）

### A. Research Design

- Query: (再現可能な検索クエリ)
- Axis: (比較軸：人口規模、財政力、導入時期など)

### B. Case Cards (3-7 items)

- City:
- Title:
- Summary:
- Pros/Cons:
- Source: (URL必須 -> 11へ登録)

### C. Comparison Table

- (横並び比較表を入れる)

### D. Actionable Items

- Applicability: (自自治体に適用できるか？)
- Questions for Dept: (担当課に聞くべき質問 3-7個)
- Missing Info: (不明点)

## 絶対ルール

- 「成功事例」だけでなく「失敗・撤退事例」も探す努力をする。
- 11_evidence_ledger にすべての出典を登録する。

## よくある失敗

- 人口規模や前提条件が違いすぎる事例（東京23区など）を持ってきてしまい、参考にならない。

## 次に呼ぶ skill

- 政策立案へ: `31_option_designer`
