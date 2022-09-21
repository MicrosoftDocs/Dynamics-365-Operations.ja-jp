---
title: Dynamics 365 Finance の削除済みまたは非推奨の機能
description: この記事では、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。
author: kfend
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 070c61df14db4d2538b129b01defd4b82db0b8a7
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462304"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance の削除済みまたは非推奨の機能

[!include [banner](../includes/banner.md)]

この記事では、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> 財務と運用アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](/dynamics/s-e/global/axtechrefrep_61) を参照してください。 これら異なるバージョンのレポートを比較し、財務と運用アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Finance 10.0.30 リリースの削除済みまたは非推奨の機能

### <a name="revenue-recognition"></a>収益認識

[収益認識](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **廃止 / 削除の理由** |改良された機能である [サブスクリプション請求管理](../../finance/accounts-receivable/subscription-billing-summary.md) に置き換えられる
| **別の機能で置き換えられているか?**   | 有効 |
| **影響を受ける製品領域** | アプリケーション |
| **配置オプション** | すべて |
| **状態** | 非推奨: 2023 年 4 月以降、Dynamics 365 Finance の収益認識機能は、修正プログラムでサポートされなくなりました。 お客様には、改良された機能である [サブスクリプション請求管理](../../finance/accounts-receivable/subscription-billing-summary.md) 利用していただくことになります。 2023 年 10 月、収益認識機能は使用できなくなりました。 お客様には、改良された機能であるサブスクリプション請求管理に移動していただくことになります。 収益認識の一部としてバンドル機能については、現時点で交換機能は計画されません。|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Finance 10.0.29 リリースの削除済みまたは非推奨の機能

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>移転価格が課税される在庫移動オーダー

[移転価格が課税される在庫移動オーダー](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **廃止 / 削除の理由** | [インドの在庫移動オーダー](../../finance/localizations/apac-ind-stock-transfer.md)が改良機能に更新されました|
| **別の機能で置き換えられているか?**   | 有効 |
| **影響を受ける製品領域** | アプリケーション |
| **配置オプション** | すべて |
| **状態** | 非推奨です: 2023 年 4 月以降、**移動価格に課税される在庫移動注文** の機能はバグ修正やセキュリティ修正のサポートを受けられなくなります。 お客様には、改良された機能である[インド向け在庫移動注文](../../finance/localizations/apac-ind-stock-transfer.md)をご利用いただくことになります。 2023 年 10 月以降、**移動価格に課税される在庫移動注文** 機能は使えなくなり、お客様には改良された機能への移行をお願いする予定です。 |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>口座取引明細書のインポートとエクスポート (正支払ファイル)

| &nbsp;  | &nbsp;  |
|---|---|
| **廃止 / 削除の理由** |改善された機能に置き換えられた、口座取引明細書をインポートし、正の支払ファイルをエクスポートします。| 
| **別の機能で置き換えられているか?**   | 有効 |
| **影響を受ける製品領域**         | アプリケーション |
| **配置オプション**              | すべて |
| **状態**                         | 推奨されない : ファイルのインポートとエクスポートのための XSLT 機能では、修正とセキュリティを修正したファイルではサポートされません。 顧客は、改善された機能を使用する必要があります: [電子レポートを使用して正の支払ファイルを設定](../../finance/accounts-payable/set-up-positive-pay-er.md) および [電子レポートを使用して高度な口座調整インポートを設定](../../finance/accounts-payable/import-bai2-er.md)。 2022 年 9 月以降は、XSLT 機能は使用できなくなりました。顧客は、改善された機能に移行する必要があります。|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Finance 10.0.26 リリースの削除済みまたは非推奨の機能

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>フィンランドの消費税レポート (レポート コードに基づくデザイン)

[フィンランドの消費税レポート](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい VAT 申告書のデザインに差し替えられた、[フィンランドの VAT 申告書](../localizations/emea-fin-vat-declaration.md) |
| **別の機能で置き換えられているか?**   | 有効 |
| **影響を受ける製品領域**         | アプリケーション |
| **配置オプション**              | すべて |
| **状態**                         | 非推奨: 2023 年 3 月 1 日までに、フィンランドの消費税レポート (フィンランドのレポート レイアウト) がサポートされなくなります。 新しい **VAT 申告 TXT (FI**)、**VAT 申告 Excel (FI)** 電子報告書 (ER) 形式は、**税申告** モデル配下に導入されています。 |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Finance 10.0.24 リリースの削除済みまたは非推奨の機能

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>スウェーデンの消費税レポート (レポート コードに基づくデザイン)

[スウェーデンの消費税支払レポート](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい VAT 申告書のデザインに差し替えられた、[スウェーデンの VAT 申告書](../localizations/emea-swe-vat-declaration-sweden.md) |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | すべて |
| **状態**                         | 非推奨: 2022年12月1日までに、スウェーデンの消費税レポート (スウェーデンのレポート レイアウト) がサポートされなくなります。 新しい **VAT申告 XML (SE**)、**VAT 申告 Excel (SE)** 電子報告書 (ER) 形式は **税申告** モデル配下に導入されています。 |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>オーストリアの VAT 明細書 (レポート コードに基づくデザイン)

[オーストリア向け VAT 明細の内訳](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい VAT 申告書のデザインに差し替えられた、[オーストラリアの VAT 申告書](../localizations/emea-aut-vat-declaration-austria.md) |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | すべて |
| **状態**                         | 非推奨: 2022年12月1日までに、**VAT 申告モデル** では **VAT申告 (AT)** 電子申告  (ER) 形式はサポートされなくなります。 新しい **VAT申告 XML (AT**)、**VAT 申告 Excel (AT)** 形式は **税申告** モデル配下に導入されています。 |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ドイツ向け ELSTER 申告 (レポート コードに基づくデザイン)

[VAT 明細書](../localizations/emea-de-vat-declaration.md)</br>
[ドイツ向けの電子税申告の設定](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[VAT 申告電子送信 (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい VAT 申告書のデザインに差し替えられた、[ドイツの VAT 申告書](../localizations/emea-deu-vat-declaration-germany.md) |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | すべて |
| **状態**                         | 非推奨: 2022年12月1日までに、**Elster (DE)** と **Elster モデル** 電子申告 (ER) 形式はサポートされなくなります。 新しい **VAT申告 XML (DE**)、**VAT 申告 Excel (DE)** 形式は **税申告** モデル配下に導入されています。 |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>オランダ向け OB 申告 (レポート コードに基づくデザイン)

[OB 申告](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい VAT 申告書のデザインに差し替えられた、[オランダの VAT 申告書](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | すべて |
| **状態**                         | 非推奨: 2022年12月1日までに、**OB 申告 (NL)** と **OB 申告モデル** の電子申告 (ER) 形式はサポートされなくなります。 新しい **VAT申告 XML (NL**)、**VAT 申告 Excel (NL)** 形式は **税申告** モデル配下に導入されています。 |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Finance 10.0.20 リリースの削除済みまたは非推奨の機能

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>"RTIR クエリ請求書データ要求 (HU)" 電子レポート (ER) 形式のコンフィギュレーション

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | ハンガリーのオンライン請求システムとの相互運用の電子メッセージング処理から除外 |
| **別の機能で置き換えられているか?**   | なし |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **状態**                         | 非推奨: 2022 年 4 月 15 日までに、「RTIR クエリ請求書データ要求 (HU)」形式の構成をサポートしなくなります。 |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>"ドイツ監査ファイル出力" 形式によるフランスの "フランス監査ファイル" 電子レポート (ER) 形式

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい "FEC 監査ファイル (FR)" 形式に置き換えられた |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **状態**                         | 非推奨: 2022年5月1日より、"ドイツ監査ファイル出力" 形式による、フランスの "フランス監査ファイル" 電子レポート (ER) 形式はサポートされなくなりました。 新しい FEC 監査ファイル (FR) 形式が "データ エクスポート モデル" の下に導入されます。 |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Finance 10.0.17 リリースの削除済みまたは非推奨の機能

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>電子申告コンフィギュレーションのストレージ オプションとしての LCS リポジトリ

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい Regulatory Configuration Service (RCS) のグローバル リポジトリに置き換えられます |
| **別の機能で置き換えられているか?**   | 有効 |
| **影響を受ける製品領域**         | Dynamics 365 Finance、Supply Chain Management、Project Operations 製品|
| **配置オプション**              | All |
| **状態**                         | 非推奨: 2022 年 4 月 1 日より、電子申告 (ER) コンフィギュレーションのストレージ オプションとして Microsoft Dynamics Lifecycle Services (LCS) リポジトリのサポートを終了する予定です。 新しい Microsoft ER コンフィギュレーションは、グローバル リポジトリからのみダウンロードできるように公開されます。 グローバル リポジトリは、Dynamics 365 製品と RCS からアクセスできます。 詳細については、[RCS から ER コンフィグレーションをインポートする](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)および [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止](../localizations/rcs-lcs-repo-dep-faq.md)を参照してください。 |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Finance 10.0.16 リリースの削除済みまたは非推奨の機能

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>チェコ共和国向け「VAT申告 (CZ)」、および 「管理ステートメントのエクスポート ( CZ)」 電子レポート形式

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 新しい形式に置き換えられます |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **状態**                         | 非推奨 : 2022年1月22日より、「VAT申告 (CZ)」、「管理ステートメントのエクスポート (CZ)」の電子申告の形式はサポートされなくなります。 代わりに、新しい VAT申告 XML (CZ)、VAT申告 Excel (CZ)、VAT 管理ステートメント XML (CZ) 形式が「税申告」モデル配下で導入されます。 |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"元帳トランザクションのエクスポート形式 (BE)" 電子レポート形式と、個別の "元帳トランザクション エクスポート (BE)" モデル (ベルギー)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | "標準監査ファイル (SAF)" モデルの下にある新しい ER 形式で置き換えました。  |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **ステータス**                         | 非推奨: 2021 年 12 月 1 日までに、"元帳トランザクションのエクスポート形式 (BE)" 電子レポート (ER) 形式と、個別の "元帳トランザクション エクスポート (BE)" モデルのサポートを終了する予定です。 "標準監査ファイル (SAF)" モデルの代わりに、新しい "一般会計のデータ エクスポート (BE)" 形式と "一般会計のデータ モデル マッピング" が導入されます。 |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>SSRS 形式の英国用 "VAT 100" レポート

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | "税申告モデル" で、新しい ER 形式である "VAT 申告 Excel (UK)" 形式と置き換えました。  |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **ステータス**                         | 非推奨: 2021 年 12 月 1 日までに、SSRS 形式の "VAT 100 レポート" のサポートを終了する予定です。 "税申告モデル" の新しい "VAT 申告の Excel (UK)" 形式は、[MTD VAT 機能](../localizations/emea-gbr-mtd-vat-integration.md) に導入されました。 |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Finance 10.0.15 リリースの削除済みまたは非推奨の機能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 における Internet Explorer 11 のサポートの非推奨

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。<br><br>これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。 2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。 |
| **別の機能で置き換えられているか?**   | Microsoft Edge に移行することをお勧めします。|
| **影響を受ける製品領域**         | すべての Dynamics 365 製品 |
| **配置オプション**              | All|
| **ステータス**                         | 非推奨。 2021 年 8 月以降は、Internet Explorer 11 はサポートされません。|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance 10.0.12 リリースの削除済みまたは非推奨の機能

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>廃止されていない: ポーランド SSRS レポート: 仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 法的に必須ではありません。  |
| **別の機能で置き換えられているか?**   | はい (VAT 申告を含む標準監査ファイル用の Excel 形式 - JPK_VDEK) |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **状態**                         | 非推奨ではない: 2021 年 4 月 27 日現在、SSRS レポートのサポートを継続する予定です: **仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014**。 VAT 申告を含む標準監査ファイルの Excel 形式 (JPK_VDEK) の例も導入されました。 |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance 10.0.11 リリースの削除済みまたは非推奨の機能

### <a name="norwegian-standard-main-accounts"></a>ノルウェー標準主勘定

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 再設計  |
| **別の機能で置き換えられているか?**   | はい (ER 形式のアプリケーション固有パラメータに置き換えられます) |
| **影響を受ける製品領域**         | 応募 |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: 2021 年 4 月 1 日までに、標準主勘定に関連する機能: 参照フィールド、関連テーブル、データ エンティティ はサポートされなくなる予定です。 |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance 10.0.7 リリースの削除済みまたは非推奨の機能

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります

| &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 勘定グループを選択する機能に変更されました。  |
| **別の機能で置き換えられているか?**   | 有 |
| **影響を受ける製品領域**         | ワークフロー |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: 2020 年 12 月 1 日までに、勘定グループを選択せずに中国の伝票タイプ設定をサポートしなくなります。 新しいデザインの詳細については、[10.0.7 の新機能](whats-new-changed-10-0-7.md)を参照してください。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表
以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

