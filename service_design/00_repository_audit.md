# 00 リポジトリ監査(Phase 0)

- 作成日:2026-07-13
- 状態:仮案(Hiromi承認前)
- 作業ブランチ:`claude/fable5-service-design-review-jwu324`(環境割り当てブランチ。指示書記載の `service-design/fable5-initial-review` とは名称が異なるが、Hiromi了承済みでこのブランチを使用)

## 1. 確認したファイル

読み取り専用で以下を確認した。すべて存在し、指示書記載の構成と完全一致。

| ファイル | 位置づけ |
|---|---|
| `README.md` | 実行手順の概要 |
| `MASTER_PROMPT.md` | サービス設計の本体指示(優先順位4位) |
| `context/00_START_HERE.md` | 読み込み順・優先順位ルール |
| `context/01_SERVICE_SOURCE_OF_TRUTH.md` | **正本 v0.2**(優先順位2位) |
| `context/02_FACTS_HYPOTHESES_UNKNOWNS.md` | 事実・仮説H1〜H8・不明点 |
| `context/03_DECISION_LOG.md` | 判断履歴 D-001〜D-010(優先順位3位) |
| `context/04_TARGET_USER_AND_USE_CASES.md` | ターゲット候補・適合/不適合条件・UC-01〜03 |
| `context/05_PROVIDER_PROFILE_AND_BOUNDARIES.md` | Hiromiの経験・境界・制約 |
| `context/06_VALIDATION_PLAN_AND_METRICS.md` | 検証A/B/C・GO/STOP基準 |
| `context/07_INFORMATION_SECURITY_AND_DATA_RULES.md` | 情報管理ルール |
| `context/08_REVIEW_EVIDENCE_SUMMARY.md` | 仮想レビュー(市場事実ではない) |
| `context/09_SAMPLE_CASES_FOR_DESIGN_TEST.md` | 架空サンプル3件(設計テスト用) |
| `context/10_OUTPUT_ACCEPTANCE_CRITERIA.md` | 成果物受入基準 |
| `context/11_FABLE5_RUN_INSTRUCTION.md` | 実行開始指示 |

## 2. Git状態(作業開始時点)

- remote:`origin = hiromimasuda/it-pj1`
- default branch:`main`
- 最新コミット:`cb1cdff` "Add files via upload"
- 未コミット変更:なし(clean)
- 未追跡ファイル:なし(本監査時点。以後 `service_design/` 配下の新規6ファイルのみ追加)

## 3. 不足ファイル

- `.gitignore` が存在しない。現状は機密ファイルがないため実害なし。将来、案件メモ等をローカルへ置く場合は除外設定を推奨(例:`work_notes/`、`*.local.md`)。
- LICENSE等はプライベート運用のため不要と判断。

## 4. 重複

- サービス定義・ターゲット・価格・工数の記述が `MASTER_PROMPT.md` と `context/01` に重複して存在するが、内容はほぼ一致しており実害なし。更新時は正本(01)のみ更新し、MASTER_PROMPT側は参照扱いとすることを推奨。

## 5. 矛盾(検出5件と扱い)

| # | 矛盾・相違 | 採用した扱い |
|---|---|---|
| 1 | `MASTER_PROMPT.md` §2.4 は候補Aを「最優先ターゲット」と断定。正本§4・D-009 は「未確定・未決定」 | 優先順位ルールにより**正本の「未決定」を採用**。Phase 2 で比較 |
| 2 | `MASTER_PROMPT.md` §13 の期限「2026-07-19までに有料予約1件」 | Hiromi指示により**期限は一旦スルー。運用開始は7月末〜8月想定**(2026-07-13セッション決定) |
| 3 | 成果物ファイルリスト:セッション指示書は Phase 0〜3 用6ファイル、MASTER_PROMPT §9 は全Phase用21ファイル | **最新指示(6ファイル構成)を採用**。21ファイルは Phase 4 以降で該当分のみ作成 |
| 4 | 初回回答形式がセッション指示書§13 / `11_FABLE5_RUN_INSTRUCTION.md` / MASTER_PROMPT §14 で相違 | セッション指示書§13 を採用済み |
| 5 | 作業ブランチ名の相違(指示書 vs 環境割り当て) | 環境割り当てブランチを使用(Hiromi了承済み) |

## 6. 機密情報の疑い

**なし。** 全ファイルを確認したが、パスワード・APIキー・認証情報・実在顧客情報・Legaseed固有非公開情報は含まれていない。`09_SAMPLE_CASES` は冒頭に「実在人物・会社・Legaseedの情報ではありません」と明記済み。

## 7. 作業開始上のブロッカー

なし。Phase 1〜3 を進行可能。

## 8. 既存ファイルへの変更

行っていない。本監査を含む `service_design/` 配下6ファイルはすべて新規作成であり、既存ファイルの編集・削除・移動は一切ない。commit・push は Hiromi の明示承認まで行わない。
