---
title: 統合された元帳
description: このトピックでは、Dataverse を使用した Finance and Operations とその他の Dynamics 365 アプリケーション間の元帳データの統合について説明します。
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f8095b0a755e40e5665d951d33ea4ce60e749165
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567699"
---
# <a name="integrated-ledger"></a><span data-ttu-id="b8c4d-103">統合された元帳</span><span class="sxs-lookup"><span data-stu-id="b8c4d-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b8c4d-104">ビジネス アプリケーションでは、元帳データによって、会社が業務を行うためのコア設定が定義されます。</span><span class="sxs-lookup"><span data-stu-id="b8c4d-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="b8c4d-105">たとえば、元帳データには、会社が従う会計年度、トランザクションによって処理される通貨、使用する勘定が記述されます。</span><span class="sxs-lookup"><span data-stu-id="b8c4d-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="b8c4d-106">このトピックでは、この中心的な財務データの統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="b8c4d-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="b8c4d-107">テンプレート</span><span class="sxs-lookup"><span data-stu-id="b8c4d-107">Templates</span></span>

<span data-ttu-id="b8c4d-108">次の表に示すように、元帳データには、データ操作中に連携して動作する中心的な財務テーブル マップのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8c4d-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="b8c4d-109">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="b8c4d-109">Finance and Operations apps</span></span>      | <span data-ttu-id="b8c4d-110">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="b8c4d-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="b8c4d-111">説明</span><span class="sxs-lookup"><span data-stu-id="b8c4d-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="b8c4d-112">通貨</span><span class="sxs-lookup"><span data-stu-id="b8c4d-112">Currencies</span></span>                       | <span data-ttu-id="b8c4d-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="b8c4d-113">transactioncurrencies</span></span>            |
<span data-ttu-id="b8c4d-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="b8c4d-114">FiscalCalendar</span></span>                   | <span data-ttu-id="b8c4d-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="b8c4d-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="b8c4d-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="b8c4d-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="b8c4d-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="b8c4d-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="b8c4d-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="b8c4d-118">ExchRateType</span></span>                     | <span data-ttu-id="b8c4d-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="b8c4d-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="b8c4d-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="b8c4d-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="b8c4d-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="b8c4d-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="b8c4d-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="b8c4d-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="b8c4d-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="b8c4d-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="b8c4d-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="b8c4d-124">MainAccountCategory</span></span>              | <span data-ttu-id="b8c4d-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="b8c4d-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="b8c4d-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="b8c4d-126">MainAccount</span></span>                      | <span data-ttu-id="b8c4d-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="b8c4d-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="b8c4d-128">元帳</span><span class="sxs-lookup"><span data-stu-id="b8c4d-128">Ledger</span></span>                           | <span data-ttu-id="b8c4d-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="b8c4d-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="b8c4d-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="b8c4d-130">ExchangeRates</span></span>                    | <span data-ttu-id="b8c4d-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="b8c4d-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="b8c4d-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="b8c4d-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="b8c4d-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="b8c4d-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="b8c4d-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="b8c4d-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="b8c4d-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="b8c4d-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="b8c4d-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="b8c4d-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="b8c4d-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="b8c4d-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="b8c4d-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="b8c4d-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="b8c4d-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="b8c4d-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]