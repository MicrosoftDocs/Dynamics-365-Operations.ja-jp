---
title: 二重書き込みでの在庫状況
description: このトピックでは、二重書き込みでの在庫状況の確認方法について説明します。
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 175e1cc568ed027feee39eabfd9f08de6fe7f4b4
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542640"
---
# <a name="inventory-availability-in-dual-write"></a>二重書き込みでの在庫状況

[!include [banner](../../includes/banner.md)]

在庫状況を使用すると、Microsoft Dynamics 365 Sales の **見積**、**注文**、または **請求書** ページに製品を追加する前に、在庫を確認できます。 たとえば、[見込顧客から現金](dual-write-prospect-to-cash.md) の一つの重要なタスクとして在庫の確認と履行日の決定をおこないます。

十分な在庫がない場合は、予想在庫の入庫および払出に基づいて出荷日を見積もることができます。 また、製品の納期回答可能在庫 (ATP) 情報を確認して、事前に定義されたタイム フェンスで ATP 数量を検索することもできます。

## <a name="on-hand-inventory"></a>手持在庫

Dynamics 365 Sales で、**見積**、**注文**、**請求書** の各ページのヘッダーに、新規の **手持在庫** ボタンが追加されました。 このボタンをクリックすると、ダイアログ ボックスが表示され、手持在庫を確認する会社と製品を指定できます。 このダイアログボックスには、[手持在庫](../../../../supply-chain/inventory/tasks/check-availability-stock.md) と同じ情報が表示されます。

このダイアログ ボックスでは、Dynamics 365 Supply Chain Management からの在庫情報が返されます。 この情報には、次の数量が含まれています。

- 手持在庫数量
- 予約済み手持数量
- 使用可能な手持数量
- 注文済数量
- 注文中数量
- 引当済の注文済数量
- 利用可能な合計数量

## <a name="atp-information"></a>ATP 情報

Sales では、**ATP情報** ボタンが **見積**、**注文**、**請求書** の各ページの品目に追加されました。 このボタンを選択すると、ダイアログ ボックスが表示され、会社、製品、在庫サイト、在庫倉庫、注文数量を指定できます。 このダイアログボックスの設定は、[注文-受注](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) に記述されている設定と同じです。

このダイアログ ボックスでは、Supply Chain Management からの ATP 情報が返されます。 この情報には、次の数量が含まれています。

- ATP 数量
- 受入数量
- 払出数量
- 手持在庫数量

## <a name="how-it-works"></a>この機能の動作

**見積書**、**注文**、または **請求書** ページの **手持在庫** ボタンを選択すると、デュアル書き込み呼び出しが **手持在庫** API につくられます。 API によって、特定の製品の在庫が計算されます。 この結果は、**InventCDSInventoryOnHandRequestEntity** と **InventCDSInventoryOnHandEntryEntity** テーブルに格納された後、デュアル書き込みによって Dataverse に書き込まれます。 この機能を使用するには、次のデュアル 書き込みマップを実行する必要があります。 マップの実行時に初期同期をスキップします。

- CDS 在庫の手持在庫エントリー (msdyn_inventoryonhandentries)
- CDS 在庫の手持在庫要求 (msdyn_inventoryonhandrequests)

## <a name="templates"></a>テンプレート

次のテンプレートを使用して、手持在庫の在庫データを公開します。

Finance and Operations アプリ | Customer Engagement アプリ     | 説明
---|---|---
[CDS 手持在庫エントリ](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[CDS 手持在庫要求](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
