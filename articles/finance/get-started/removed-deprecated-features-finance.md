---
title: Dynamics 365 Finance の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689497"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance の削除済みまたは推奨されない機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Finance 10.0.16 リリースの削除済みまたは非推奨の機能

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"元帳トランザクションのエクスポート形式 (BE)" 電子レポート形式と、個別の "元帳トランザクション エクスポート (BE)" モデル (ベルギー)

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | "標準監査ファイル (SAF)" モデルの下にある新しい ER 形式で置き換えました。  |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **ステータス**                         | 非推奨: 2021 年 12 月 1 日までに、"元帳トランザクションのエクスポート形式 (BE)" 電子レポート (ER) 形式と、個別の "元帳トランザクション エクスポート (BE)" モデルのサポートを終了する予定です。 "標準監査ファイル (SAF)" モデルの代わりに、新しい "一般会計のデータ エクスポート (BE)" 形式と "一般会計のデータ モデル マッピング" が導入されます。 |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>SSRS 形式の英国用 "VAT 100" レポート

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | "税申告モデル" で、新しい ER 形式である "VAT 申告 Excel (UK)" 形式と置き換えました。  |
| **別の機能で置き換えられているか?**   | あり |
| **影響を受ける製品領域**         | 申請書 |
| **配置オプション**              | All |
| **ステータス**                         | 非推奨: 2021 年 12 月 1 日までに、SSRS 形式の "VAT 100 レポート" のサポートを終了する予定です。 "税申告モデル" の新しい "VAT 申告の Excel (UK)" 形式は、[MTD VAT 機能](../localizations/emea-gbr-mtd-vat-integration.md) に導入されました。 |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Finance 10.0.15 リリースの削除済みまたは非推奨の機能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 における Internet Explorer 11 のサポートの非推奨

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | 2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。<br><br>これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。 2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。 |
| **別の機能で置き換えられているか?**   | Microsoft Edge に移行することをお勧めします。|
| **影響を受ける製品領域**         | すべての Dynamics 365 製品 |
| **配置オプション**              | All|
| **ステータス**                         | 非推奨。 2021 年 8 月以降は、Internet Explorer 11 はサポートされません。|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance 10.0.12 リリースの削除済みまたは非推奨の機能

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>ポーランド SSRS レポート: 仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | 法的に必須ではありません。  |
| **別の機能で置き換えられているか?**   | はい (VAT 申告を含む標準監査ファイル用の Excel 形式 - JPK_VDEK) |
| **影響を受ける製品領域**         | 応募 |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: 2021 年 7 月 1 日には、SSRS レポートのサポートはなくなります: **仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014**。 代わりに、VAT 申告を含む標準監査ファイルの Excel 形式 (JPK_VDEK) の例が導入されます。 |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance 10.0.11 リリースの削除済みまたは非推奨の機能

### <a name="norwegian-standard-main-accounts"></a>ノルウェー標準主勘定

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | 再設計  |
| **別の機能で置き換えられているか?**   | はい (ER 形式のアプリケーション固有パラメータに置き換えられます) |
| **影響を受ける製品領域**         | 応募 |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: 2021 年 4 月 1 日までに、標準主勘定に関連する機能: 参照フィールド、関連テーブル、データ エンティティ はサポートされなくなる予定です。 |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance 10.0.7 リリースの削除済みまたは非推奨の機能

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります
|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | 勘定グループを選択する機能に変更されました。  |
| **別の機能で置き換えられているか?**   | 有 |
| **影響を受ける製品領域**         | ワークフロー |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: 2020 年 12 月 1 日までに、勘定グループを選択せずに中国の伝票タイプ設定をサポートしなくなります。 新しいデザインの詳細については、[10.0.7 の新機能](whats-new-changed-10-0-7.md)を参照してください。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表
以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]