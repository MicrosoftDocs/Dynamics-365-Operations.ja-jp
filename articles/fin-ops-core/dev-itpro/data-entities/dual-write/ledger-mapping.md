---
title: 統合された元帳
description: この記事では、Dataverse を使用した財務と運用アプリやその他の Dynamics 365 アプリケーション間の元帳データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 728c131c260586e7f1f787f22ccf02ed81c94c01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289151"
---
# <a name="integrated-ledger"></a>統合された元帳

[!include [banner](../../includes/banner.md)]



ビジネス アプリケーションでは、元帳データによって、会社が業務を行うためのコア設定が定義されます。 たとえば、元帳データには、会社が従う会計年度、トランザクションによって処理される通貨、使用する勘定が記述されます。 この記事では、この中心的な財務データの統合について説明します。

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

