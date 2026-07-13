# Fable 5 サービス設計コンテキストパック

このフォルダは、`MASTER_PROMPT.md`と併用する補助資料です。

## 目的

Fable 5が次を混同しないようにします。

- 正式に採用している前提
- 未検証の仮説
- 過去の検討案
- 仮想ユーザー・仮想専門家のレビュー
- Hiromiの提供能力と制約
- 情報管理上の境界
- GO・PIVOT・STOPの判定基準

## 読み込み順

1. `01_SERVICE_SOURCE_OF_TRUTH.md`
2. `02_FACTS_HYPOTHESES_UNKNOWNS.md`
3. `03_DECISION_LOG.md`
4. `04_TARGET_USER_AND_USE_CASES.md`
5. `05_PROVIDER_PROFILE_AND_BOUNDARIES.md`
6. `06_VALIDATION_PLAN_AND_METRICS.md`
7. `07_INFORMATION_SECURITY_AND_DATA_RULES.md`
8. `08_REVIEW_EVIDENCE_SUMMARY.md`
9. `09_SAMPLE_CASES_FOR_DESIGN_TEST.md`
10. `10_OUTPUT_ACCEPTANCE_CRITERIA.md`

その後、`MASTER_PROMPT.md`を実行してください。

## 情報が矛盾した場合の優先順位

1. Hiromiによる最新の明示的な承認
2. `01_SERVICE_SOURCE_OF_TRUTH.md`
3. `03_DECISION_LOG.md`
4. `MASTER_PROMPT.md`
5. その他の補助資料
6. 過去の草案・仮想レビュー

仮想ユーザー・仮想専門家の意見は、市場調査結果ではありません。

## 更新ルール

- 正式決定：`01_SERVICE_SOURCE_OF_TRUTH.md`
- 判断経緯：`03_DECISION_LOG.md`
- 仮説状態：`02_FACTS_HYPOTHESES_UNKNOWNS.md`
- 検証結果：`06_VALIDATION_PLAN_AND_METRICS.md`

Hiromiの承認なしに正本を上書きしないでください。
