# sento.group ケイパビリティ一覧（社外提示用）

最終更新: 2025-08-31 13:12 (JST)
作成目的: クライアントから「何ができるか？」を問われた際に、即答・即提示できる統合カタログを提供する
根拠情報: `materials/clients/` 以下の提案書/議事録/進行メモ、社内方針文書（例: `company-resources/sento-group/business-overview/202508方針書.md`）

---

## 1. プロジェクトマネジメント（PM）

できること:
- 開発PM: 要件定義→実装→受入→リリース計画、変更管理、インシデント対応
- DXPM: 現場業務の可視化→標準化→データ化→自動化のロードマップ設計と推進
- 事業継承PM: 既存運用/ナレッジの棚卸し、権限/監査、引継ぎ計画、リスク最小化
- SaaS開発PM（PdM兼務）: 顧客要件→プロダクト仮説→MVP→検証→価格/契約設計

提供内容:
- 週次定例運営、ステークホルダー調整、決裁用資料/提案書の作成、SLA/運用手順書整備
- 要件トレーサビリティ（課題→要件→設計→実装→テスト→運用）の可視化
- 官公庁/入札案件の提案・進行（例: 三重県観光統計関連、入札仕様準拠の帳票/ログ設計）

成果指標の例:
- 同日意思決定率≥80%（定例での即決・次アクション確定）
- 変更要求の平均処理リードタイム≤5営業日
- 障害一次対応≤1営業日、重大インシデント再発率の継続低下

代表実績/根拠:
- 三重県 観光客実態調査（官庁系PM、要件定義〜進行）: Vercelフォーム/GAS/Spreadsheet/Tableau
- 医療機関の人材/資格管理システム運用PM（大規模組織）

---

## 2. 広告運用

できること:
- Google広告の運用/計測/最適化（検索、P-MAX、ディスプレイ、YouTube）
- 事業KPIと連動したROAS/POAS運用、クリエイティブ/LPのABテスト運用

提供内容:
- BigQueryやスプレッドシートと広告プラットフォームの連携、n8n等での自動レポート
- BI（Metabase/Looker Studio）で媒体→流入→CV→売上/粗利のパス可視化

成果指標の例:
- 媒体別粗利貢献の可視化率100%/月、低効果配分の縮減（目安: 広告費3%削減）
- レポーティング工数削減（週次/日次の自動化）

代表実績/根拠:
- ビズリンク: BigQuery×Metabaseで媒体貢献可視化、定期レポート自動化

---

## 3. システム開発（フロント/業務UI/軽量アプリ）

できること:
- Vercel環境での独自フォーム/業務アプリ/モック構築（Next.js、v0、Supabase連携）
- 認証付きアンケート/申請ワークフロー、業務ダッシュボード、軽量CMS/管理UI

提供内容:
- デザイン試作→要件確定のためのインタラクティブモック、API/DBとの疎通実装
- Retool等のローコードでの管理/運用画面の提供

成果指標の例:
- モック経由の要件確定サイクル短縮（例: 2週間→数日）
- 本番デプロイの平均リードタイム≤1営業日（Vercel）

代表実績/根拠:
- 医療/教育/人材領域のNext.js×Vercel実装、各種v0モック/本番URL（社内資料参照）
- HCFA Amape: Supabase×Next×VercelでのSaaS実装ステージング/本番運用

---

## 4. データ基盤構築（ノーコード〜本格DWH）

4.1 ノーコードDBの構築および可視化
- ツール: Airtable / NocoDB、Apps Script、Looker Studio/軽量BI
- 提供内容: スキーマ設計、ビュー/権限設計、運用ルール、更新自動化、テンプレKPI
- 成果指標: 立上げ≤2週間、手作業集計ゼロ化、担当者の自走運用化

4.2 本格データ基盤の構築および可視化
- DWH: Google BigQuery / Amazon Redshift
- ETL/オーケストレーション: n8n、Apps Script、Cloud Functions、（必要に応じて）Airflow相当
- BI: Tableau / Metabase / Looker Studio（権限/共有/テンプレKPI設計）
- データ設計: 最小スキーマ、キー整備（メール/会社ID/外部ID）、履歴（SCD）/イベントログ
- 成果指標: ID連結率≥95%、定期自動更新/監視（欠損・重複アラート）、合意KPIの同一解

代表実績/根拠:
- 三重県 観光データ: Spreadsheet+GAS→Tableau可視化
- ビズリンク: kintone/広告→BigQuery→Metabase、定期アラート/可視化

---

 

## 6. ドメイン特化（医療・公共/観光）

医療:
- 大規模医療機関の人材/資格情報の統合管理、運用/保守、SLA対応

公共/観光:
- 観光インバウンド実態調査の設計/実装（Vercelフォーム、多言語、GAS/Spreadsheet、Tableau）
- 官公庁案件の調達/入札仕様への準拠、PM/進行体制の整備

成果指標の例:
- 月次/週次のレポート定着、関係機関との同日意思決定
- 監査対応の作業時間短縮、データ開示の可逆性確保

---

## 7. アーキテクチャ / セキュリティ / 運用

インフラ/ホスティング:
- Vercel / Render / Fly.io / AWS（要件に応じ選定）

監視/可観測性:
- Sentry / Datadog / Healthchecks

IaC/設定管理（必要に応じて）:
- Terraform、環境変数/秘密情報管理、権限設計

運用/PMO:
- 変更管理、ナレッジベース化、トレーニング、体制/引継ぎ設計

---

## 8. 代表的スタック一覧（抜粋）

- 収集/連携: Shopify, formrun, HubSpot, kintone, GA4, 各SNS API
- ETL/更新: n8n, Apps Script, Cloud Functions
- DWH: BigQuery, Amazon Redshift, PostgreSQL
- BI/可視化: Tableau, Metabase, Looker Studio
- アプリ: Next.js, Vercel, Supabase, Retool, v0
- 監視/運用: Sentry, Datadog, Healthchecks, GitHub Actions

---

## 9. 即答用スニペット（クライアント問合せへの短文回答）

- PMは何ができますか？
  - 開発PM/DXPM/事業継承PM/SaaS開発PM（PdM兼務）まで一気通貫に対応します。週次定例と変更管理/インシデント対応、意思決定を加速する可視化をセットで提供します。

- Google広告の運用は対応可能ですか？
  - はい。BigQuery/MetabaseやLooker Studioで媒体別の粗利貢献を可視化し、定期レポートはn8nで自動化します。広告費の無駄配分削減と意思決定スピード向上を両立します。

- Vercel環境で独自フォームや業務アプリは作れますか？
  - はい。Next.js×Vercelで認証付フォーム/業務UIを短期間で構築し、Spreadsheet/Supabase/DWHと連携します。モック→本番移行も迅速です。

- データ基盤はノーコードと本格DWHのどちらも可能ですか？
  - はい。Airtable/NocoDBによるスピード立上げと、BigQuery/Redshiftによる拡張性ある基盤の両輪に対応します。要件に応じて段階導入します。

- CRM/SFAの移管やクレンジングは？
  - Salesforce/HubSpot/Next SFAに対応します。スキーマ/項目マッピング、重複排除、監査ログ/権限設計まで含めて安全に切替します。

---

## 10. 参考リンク（社内）

- 三重交通/観光プロジェクト関連: `materials/clients/三重交通/`
- ビズリンク/Metabase×BigQuery: `materials/clients/bizlink/`
- GAAAT/Shopify×formrun×HubSpot統合: `materials/clients/株式会社GAAAT/`
- 医療機関/人材管理: `materials/clients/聖マリアンナ医科大学病院/`

備考:
- 本ドキュメントは社外共有前提のため、個人情報・秘密情報は記載しません。

