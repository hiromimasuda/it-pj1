# 00 サービス設計サマリー(全体地図)

- 最終更新:2026-07-13
- 状態:**Phase 0〜10の設計完了+運用キット完備(運用可能状態)**。不明点は仮案として決定済みで、運用前・運用中に改善する方針(Hiromi指示 2026-07-13)。承認事項の一覧は `20_executive_recommendation.md` §15 と `22_launch_checklist.md` A。
- 優先順位:このフォルダ内で記述が食い違う場合、`20_executive_recommendation.md` → 各詳細ファイルの順。正本(`context/01`)との差分は承認後に正本へ反映する。

## サービス(一文)

> 毎週または毎月繰り返している一つのPC業務を実際に観察し、不要な工程を減らし、必要に応じてAIを組み込み、顧客が次回から自分で再利用できる仕事の型へ変える、14日間の短期改善サービス。

- 第一ターゲット(仮):中小企業・ベンチャー(10〜150名)の実務を持つ責任者・マネージャー。個人事業主は比較検証。
- 第一対象業務(仮):週次報告。第二:承認依頼文。
- モニター:9,800円×3件限定 → 正式価格仮説:39,800円。
- 提供上限:1件5時間(1件目は8時間未満なら許容)。

## ファイル構成

| 区分 | ファイル | 内容 |
|---|---|---|
| Phase 0〜3(Gate 1) | `00_repository_audit.md` | リポジトリ監査・矛盾5件 |
| | `01_service_understanding.md` | JTBD・AIの範囲・関係者分析 |
| | `02_target_segment_comparison.md` | 候補A/B 11軸比較 |
| | `03_target_work_comparison.md` | 業務9候補 11軸評価 |
| | `04_hypothesis_register.md` | 仮説H1〜H10(検証行動・判断ルール付き) |
| | `05_gate1_review.md` | Gate 1承認依頼 |
| 設計(Phase 4〜6) | `01_customer_and_problem_definition.md` | 設計用の顧客・課題定義(確定版サマリー) |
| | `03_target_work_selection.md` | 対象業務の選定記録・運用ルール |
| | `04_service_package_design.md` | 商品名3案・提供内容・保証範囲・追加対応 |
| | `05_customer_journey.md` | 14場面の体験設計・最初の価値体験 |
| | `06_pricing_and_unit_economics.md` | 5価格比較・5時間の実現可能性・3段階商品 |
| 販売・提供(Phase 7〜9) | `07_sales_and_acquisition_plan.md` | 候補者選定・行動測定 |
| | `08_delivery_operation.md` | 17工程の運用定義・超過監視点 |
| | `09_information_security_policy.md` | 顧客向け一枚+運用+専門家確認論点 |
| 検証・判断(Phase 10) | `10_validation_plan_7days.md` | 検証A/B/C・結果別判断ルール |
| | `11_risks_and_stop_conditions.md` | 批判的9問・STOP/PIVOT/GO基準 |
| | `12_decision_log.md` | D-011〜D-018追記案(承認待ち) |
| 実務ツール | `13_one_page_service_offer.md` | 一枚の商品説明(送付用) |
| | `14_pre_interview_questions.md` | 事前質問5問+適合確認 |
| | `15_interview_guide.md` | 60分ヒアリング進行台本 |
| | `16_work_improvement_sheet_template.md` | 成果物1テンプレート |
| | `17_before_after_template.md` | 成果物3テンプレート |
| | `18_customer_message_templates.md` | 提案文3種+運用文面4種 |
| | `19_provider_time_tracking_template.md` | 検証C記録表 |
| 最終提言 | `20_executive_recommendation.md` | 判定・今週の一手・承認依頼一覧 |
| 運用キット | `21_operations_runbook.md` | 1案件のDay-by-day実行手順・例外処理 |
| | `22_launch_checklist.md` | 運用開始前チェックリスト・週次セルフレビュー |
| | `23_sample_kit_weekly_report.md` | 実行キット雛形:週次報告(プロンプト・テンプレ・チェックリスト) |
| | `24_sample_kit_approval_request.md` | 実行キット雛形:承認依頼文(承認者プロファイル含む) |
| | `25_design_test_results.md` | 架空サンプル3件への設計テスト結果と設計修正 |
| | `26_candidate_tracker_template.md` | 候補者リスト・検証A/B/Cトラッカー(実名はローカル管理) |
| | `27_application_terms_draft.md` | 申込み確認事項・支払い運用(仮案) |
| | `28_sot_update_proposal.md` | 正本v0.3更新案・受入基準との照合 |

## 検証開始までに残っている作業(Hiromiのみ可能・`22`Aに集約)

1. 就業規則(副業規定)の確認
2. 検証開始日(Day 1)の決定と候補者20名のリストアップ
3. 提案文の口調調整と振込先口座の決定

※正本v0.3への反映(`context/01`・`02`・`03`)は 2026-07-19 に完了済み(`28`参照)。
