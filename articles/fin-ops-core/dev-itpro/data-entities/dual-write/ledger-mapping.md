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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 20c038d0d4fe8ec3e07219862f98aef970882f26
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985248"
---
# <a name="integrated-ledger"></a><span data-ttu-id="7561c-103">統合された元帳</span><span class="sxs-lookup"><span data-stu-id="7561c-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="7561c-104">ビジネス アプリケーションでは、元帳データによって、会社が業務を行うためのコア設定が定義されます。</span><span class="sxs-lookup"><span data-stu-id="7561c-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="7561c-105">たとえば、元帳データには、会社が従う会計年度、トランザクションによって処理される通貨、使用する勘定が記述されます。</span><span class="sxs-lookup"><span data-stu-id="7561c-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="7561c-106">このトピックでは、この中心的な財務データの統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="7561c-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="7561c-107">テンプレート</span><span class="sxs-lookup"><span data-stu-id="7561c-107">Templates</span></span>

<span data-ttu-id="7561c-108">次の表に示すように、元帳データには、データ操作中に連携して動作する中心的な財務のエンティティ マップのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7561c-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="7561c-109">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="7561c-109">Finance and Operations apps</span></span>      | <span data-ttu-id="7561c-110">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="7561c-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="7561c-111">説明</span><span class="sxs-lookup"><span data-stu-id="7561c-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="7561c-112">通貨</span><span class="sxs-lookup"><span data-stu-id="7561c-112">Currencies</span></span>                       | <span data-ttu-id="7561c-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="7561c-113">transactioncurrencies</span></span>            |
<span data-ttu-id="7561c-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="7561c-114">FiscalCalendar</span></span>                   | <span data-ttu-id="7561c-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="7561c-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="7561c-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="7561c-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="7561c-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="7561c-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="7561c-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="7561c-118">ExchRateType</span></span>                     | <span data-ttu-id="7561c-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="7561c-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="7561c-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="7561c-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="7561c-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="7561c-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="7561c-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="7561c-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="7561c-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="7561c-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="7561c-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="7561c-124">MainAccountCategory</span></span>              | <span data-ttu-id="7561c-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="7561c-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="7561c-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="7561c-126">MainAccount</span></span>                      | <span data-ttu-id="7561c-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="7561c-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="7561c-128">元帳</span><span class="sxs-lookup"><span data-stu-id="7561c-128">Ledger</span></span>                           | <span data-ttu-id="7561c-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="7561c-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="7561c-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="7561c-130">ExchangeRates</span></span>                    | <span data-ttu-id="7561c-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="7561c-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="7561c-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="7561c-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="7561c-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="7561c-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="7561c-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="7561c-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="7561c-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="7561c-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="7561c-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="7561c-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="7561c-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="7561c-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="7561c-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="7561c-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="7561c-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="7561c-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




