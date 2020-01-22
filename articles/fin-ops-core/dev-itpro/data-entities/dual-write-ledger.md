---
title: 統合された元帳
description: このトピックでは、Common Data Service を使用した Finance and Operations とその他の Dynamics 365 アプリケーション間の元帳データの統合について説明します。
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4a0a8f2f52cf9a73efc3557b63793201a7a3f8b8
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853885"
---
# <a name="integrated-ledger"></a>統合された元帳

[!include [banner](../includes/banner.md)]

ビジネス アプリケーションでは、元帳データによって、会社が業務を行うためのコア設定が定義されます。 たとえば、元帳データには、会社が従う会計年度、トランザクションによって処理される通貨、使用する勘定が記述されます。 このトピックでは、この中心的な財務データの統合について説明します。

## <a name="templates"></a>テンプレート

次の表に示すように、元帳データには、データ操作中に連携して動作する中心的な財務のエンティティ マップのコレクションが含まれています。

Finance and Operations アプリ      | その他の Dynamics 365 アプリ
---------------------------------|---------------------------------
通貨                       | transactioncurrencies
FiscalCalendar                   | msdyn\_fiscalcalendars
FiscalCalendarYear               | msdyn\_fiscalcalendaryears
ExchRateType                     | msdyn\_exchangeratetypes
ExchangeRateCurrencyPair         | msdyn\_currencyexchangeratepairs
FiscalPeriodEntity               | msdyn\_fiscalcalendarperiods
MainAccountCategory              | msdyn\_mainaccountcategory
MainAccount                      | msdyn\_mainaccounts
元帳                           | msdyn\_ledgers
ExchangeRates                    | msdyn\_currencyexchangerates
FinancialCalendarPeriod          | msdyn\_fiscalcalendarperiods
DimensionAttributeEntity         | msdyn\_dimensionattributes.md
DimensionIntegrationFormatEntity | msdyn\_financialdimensionformats.md
LedgerChartOfAccounts            | msdyn\_chartofaccounts.md


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




