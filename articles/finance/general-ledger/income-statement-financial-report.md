---
title: 損益計算書財務諸表
description: この記事では、損益計算書の既定のレポートについて説明します。 また、このレポートに関連付けられる構成要素を説明します。
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 429283865c66ca5f03608e4a02c3aba5bb5ea7e3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645580"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="96d09-104">損益計算書財務諸表</span><span class="sxs-lookup"><span data-stu-id="96d09-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96d09-105">この記事では、損益計算書の既定のレポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="96d09-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="96d09-106">また、このレポートに関連付けられる構成要素を説明します。</span><span class="sxs-lookup"><span data-stu-id="96d09-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="96d09-107">既定の損益計算書表</span><span class="sxs-lookup"><span data-stu-id="96d09-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="96d09-108">既定のレポート</span><span class="sxs-lookup"><span data-stu-id="96d09-108">Default report</span></span>             | <span data-ttu-id="96d09-109">目的</span><span class="sxs-lookup"><span data-stu-id="96d09-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d09-110">損益計算書 – 既定</span><span class="sxs-lookup"><span data-stu-id="96d09-110">Income Statement – Default</span></span> | <span data-ttu-id="96d09-111">現在の期間また年間累計の組織の収益性のビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="96d09-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="96d09-112">構成要素</span><span class="sxs-lookup"><span data-stu-id="96d09-112">Building blocks</span></span>
<span data-ttu-id="96d09-113">損益計算書財務諸表は、次の構成要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="96d09-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="96d09-114">既定のレポート</span><span class="sxs-lookup"><span data-stu-id="96d09-114">Default report</span></span>             | <span data-ttu-id="96d09-115">行の定義</span><span class="sxs-lookup"><span data-stu-id="96d09-115">Row definition</span></span>                     | <span data-ttu-id="96d09-116">列の定義</span><span class="sxs-lookup"><span data-stu-id="96d09-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="96d09-117">損益計算書 - 既定</span><span class="sxs-lookup"><span data-stu-id="96d09-117">Income Statement - Default</span></span> | <span data-ttu-id="96d09-118">集計損益計算書 - 既定</span><span class="sxs-lookup"><span data-stu-id="96d09-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="96d09-119">定期処理および現時点の年間累計 - 既定</span><span class="sxs-lookup"><span data-stu-id="96d09-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="96d09-120">行の定義</span><span class="sxs-lookup"><span data-stu-id="96d09-120">Row definition</span></span>

<span data-ttu-id="96d09-121">行定義、集計損益計算書 - 既定には、従来の損益計算書の各部分のセクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96d09-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="96d09-122">主勘定カテゴリの分析コードは、この行定義の構築に使用されます。</span><span class="sxs-lookup"><span data-stu-id="96d09-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="96d09-123">したがって、ユーザーは変更しないでレポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="96d09-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="96d09-124">列の定義</span><span class="sxs-lookup"><span data-stu-id="96d09-124">Column Definition</span></span>

<span data-ttu-id="96d09-125">列の定義には、さまざまな詳細なレベルと財務データを提供する列のさまざまなタイプが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96d09-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="96d09-126">**定期処理と現時点の年間累計 – 既定の列のタイプ:**</span><span class="sxs-lookup"><span data-stu-id="96d09-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="96d09-127">**DESC** – 行定義の説明</span><span class="sxs-lookup"><span data-stu-id="96d09-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="96d09-128">**FD** – 現在の期間の財務データ</span><span class="sxs-lookup"><span data-stu-id="96d09-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="96d09-129">**FD** – 年間累計の財務データ</span><span class="sxs-lookup"><span data-stu-id="96d09-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="96d09-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="96d09-130">Additional resources</span></span>
--------

[<span data-ttu-id="96d09-131">財務諸表の概要</span><span class="sxs-lookup"><span data-stu-id="96d09-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="96d09-132">財務諸表の表示</span><span class="sxs-lookup"><span data-stu-id="96d09-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="96d09-133">Dynamics Financial Reporting ブログ</span><span class="sxs-lookup"><span data-stu-id="96d09-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)



