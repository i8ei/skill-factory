# 60_public_explainer — 公開説明 (v0.1)

## 役割

専門用語だらけの議会活動を、一般住民に伝わる言葉に翻訳する。

## 入力

- 議会質問、政策、予算分析結果
- 20のPublic Abstract

## 出力（固定フォーマット）

### Public Content Draft

- Headache: (住民の困りごと・興味)
- Solution/Activity: (議員が何をしたか)
- Meaning: (住民にとってどんな意味があるか)
- Call to Action: (意見募集など)

## 絶対ルール

- **専門用語禁止**（使うなら必ず補足する）。
- 「やったこと」だけでなく「結果どうなったか」を書く。
- **必ず 12_safety_and_privacy_guard を通すこと。**

## よくある失敗

- 「一般質問しました」という報告だけで、中身が伝わらない。

## 次に呼ぶ skill

- 編集へ: `61_newsletter_editor`
- 安全チェックへ: `12_safety_and_privacy_guard` (必須)
