---
title: Dynamics 365 Commerce の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。
author: josaw
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443921"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce の削除済みまたは推奨されない機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commerce 10.0.11 リリースの削除済みまたは非推奨の機能
### <a name="data-action-hooks"></a>データ アクションのフック
|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | パフォーマンスの問題のために、データ アクション フック機能は廃止されました。 |
| **別の機能で置き換えられているか?**   | データアクション層のビジネスロジックを変更するために、[データ アクションの上書き](../e-commerce-extensibility/data-action-overrides.md) を使用することが推奨されます。|
| **影響を受ける製品領域**         | eコマースの拡張データ アクション |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: リリース 10.0.11 現在 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce 10.0.10 リリースの削除済みまたは非推奨の機能
### <a name="pos-operation-803---picking-and-receiving"></a>POS operation 803 - ピッキングと入荷
|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | ピッキングと入庫処理は、運用面の見直しに伴い、現在は使用されていません。 |
| **別の機能で置き換えられているか?**   | はい。 この機能は、インバウンド処理 (804) とアウトバウンド処理 (805) の 2 つの新しい POS 工程に置き換えられます。|
| **影響を受ける製品領域**         | 販売時点管理（POS）アプリケーション |
| **配置オプション**              | すべて |
| **ステータス**                         | 使用されていません：リリース 10.0.10 の時点で、ピッキングと入荷の処理は、新たな更新プログラムが適用されません。 今後のリリースでは、この処理に対する重大なバグの修正のみが行われます。 すべてのお客様には、新しい[インバウンド処理](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)と[アウトバウンド処理](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)への移行を奨励して おり、引き続き長期的な製品ロードマップに含まれています。 |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce 10.0.7 リリースの削除済みまたは非推奨の機能
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities と GetAvailableInventoryNearby API
|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | GetProductAvailabilities と GetAvailableInventoryNearby API は、新たに最適化された API に置き換えられます。 |
| **別の機能で置き換えられているか?**   | 今後は、GetEstimatedAvailabilty と GetEstimatedProductWarehouseAvailability API がご利用頂けます。 |
| **影響を受ける製品領域**         | eコマース アプリケーション SDK |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: リリース バージョン 10.0.7 の時点では、GetProductAvailabilities と GetAvailableInventoryNearby に対する新規開発は今後行われません。 これら API をeコマース環境で使用している組織では、新しい GetEstimatedAvailabilty と GetEstimatedProductWarehouseAvailability API に置き換えを行い、[最適化された商品在庫計算機能 ](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) を有効化する必要があります。  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表
以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)を参照してください。
