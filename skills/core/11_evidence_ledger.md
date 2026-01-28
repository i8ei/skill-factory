# 11_evidence_ledger — 証拠台帳管理 (v0.1)

## 役割

すべての議論・質問・広報の「出典（ソース）」を一元管理する。
捏造や誤認を防ぐためのアンカー。

## 入力

- 参照したい資料（URL、ＰＤＦ、書籍名、議事録）

## 出力（固定フォーマット）

### Evidence Ledger Entry

- ID: E001
- Source Name:
- URL/Location:
- Key Quote:
- Reliability Score (A-C):

## 絶対ルール

- URLやページ数が無いものは「根拠なし」と見なす。
- 伝聞（人から聞いた）は「証言」として区分する。

## よくある失敗

- 「ネットで見た」だけでURLを記録し忘れる。

## 次に呼ぶ skill

- 資料が揃ったら: `31_option_designer`
- 質問を作るなら: `50_protocol_converter`
