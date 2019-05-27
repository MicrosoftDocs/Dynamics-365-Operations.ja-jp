---
title: 原価オブジェクトの原価エントリの表示
description: この手順では、原価対象の原価のエントリを表示する方法を示します。
author: AndersGirke
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, EcoResProductDetailsExtended, InventCostOnhandItem, InventValueTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c67ac7dd06219b9521e4832b18204bcf8662a81
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563161"
---
# <a name="view-cost-entries-for-a-cost-object"></a><span data-ttu-id="48e1b-103">原価オブジェクトの原価エントリの表示</span><span class="sxs-lookup"><span data-stu-id="48e1b-103">View cost entries for a cost object</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48e1b-104">この手順では、原価対象の原価のエントリを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="48e1b-104">This procedure shows how to view cost entries for a cost object.</span></span> <span data-ttu-id="48e1b-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="48e1b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="48e1b-106">この手順は、原価の管理者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="48e1b-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="48e1b-107">[原価管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48e1b-107">Click Cost administration.</span></span>
2. <span data-ttu-id="48e1b-108">[リリース済製品] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48e1b-108">Click Released products.</span></span>
3. <span data-ttu-id="48e1b-109">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="48e1b-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="48e1b-110">たとえば、「m0004」という値を含む [品目番号] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="48e1b-110">For example, filter on the Item number field with a value of 'm0004'.</span></span>
4. <span data-ttu-id="48e1b-111">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48e1b-111">On the Action Pane, click Manage costs.</span></span>
5. <span data-ttu-id="48e1b-112">[原価オブジェクト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48e1b-112">Click Cost objects.</span></span>
6. <span data-ttu-id="48e1b-113">[原価エントリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48e1b-113">Click Cost entries.</span></span>
7. <span data-ttu-id="48e1b-114">[クイック フィルター] を使用して、「p000031」の値を含む [番号] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="48e1b-114">Use the Quick Filter to filter on the Number field with a value of 'p000031'.</span></span>
    * <span data-ttu-id="48e1b-115">原価のエントリが空白の場合、[開始日] を 2012 年 1 月 31 日に、[終了日] を 2012 年 12 月 31 日に設定します。</span><span class="sxs-lookup"><span data-stu-id="48e1b-115">If cost entries are blank, set From date to January 31, 2012 and To date to December 31, 2012.</span></span>  

