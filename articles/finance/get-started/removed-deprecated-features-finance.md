---
title: Dynamics 365 Finance の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
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
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175111"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance の削除済みまたは推奨されない機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

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
