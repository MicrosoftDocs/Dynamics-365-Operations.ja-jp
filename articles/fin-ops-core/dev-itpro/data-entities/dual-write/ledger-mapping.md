---
title: 統合された元帳
description: このトピックでは、Dataverse を使用した Finance and Operations とその他の Dynamics 365 アプリケーション間の元帳データの統合について説明します。
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 0deb4198acb59b90bf06e4050889d028df2223e3
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063650"
---
# <a name="integrated-ledger"></a>統合された元帳

[!include [banner](../../includes/banner.md)]



ビジネス アプリケーションでは、元帳データによって、会社が業務を行うためのコア設定が定義されます。 たとえば、元帳データには、会社が従う会計年度、トランザクションによって処理される通貨、使用する勘定が記述されます。 このトピックでは、この中心的な財務データの統合について説明します。

## <a name="templates"></a>テンプレート

次の表に示すように、元帳データには、データ操作中に連携して動作する中心的な財務テーブル マップのコレクションが含まれています。

財務と運用アプリ | Customer Engagement アプリ     | 説明
---------------------------------|----------------------------------|------------
[CDS 為替レート](mapping-reference.md#123) | msdyn_currencyexchangerates |
[勘定科目表](mapping-reference.md#121) | msdyn_chartofaccountses |
[通貨](mapping-reference.md#218) | transactioncurrencies |
[為替レートの通貨ペア](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[為替レート タイプ](mapping-reference.md#129) | msdyn_exchangeratetypes |
[財務分析コード形式](mapping-reference.md#130) | msdyn_financialdimensionformats |
[財務分析コード](mapping-reference.md#128) | msdyn_dimensionattributes |
[会計カレンダー統合エンティティ](mapping-reference.md#132) | msdyn_fiscalcalendars |
[会計カレンダー期間](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[会計暦年統合エンティティ](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[会計](mapping-reference.md#148) | msdyn_ledgers |
[主勘定](mapping-reference.md#152) | msdyn_mainaccounts |
[主勘定カテゴリ](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
