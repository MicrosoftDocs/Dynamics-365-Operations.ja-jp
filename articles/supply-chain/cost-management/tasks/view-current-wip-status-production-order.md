---
title: 製造オーダーの現在の仕掛品ステータスの表示
description: この手順では、製造オーダーの仕掛報告書の表示方法を説明します。
author: AndersGirke
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, ProdTable, CostStatement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8e55ccfe158146a48fd372d6f0f687d169b7632
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432094"
---
# <a name="view-current-wip-status-on-a-production-order"></a><span data-ttu-id="c1e50-103">製造オーダーの現在の仕掛品ステータスの表示</span><span class="sxs-lookup"><span data-stu-id="c1e50-103">View current WIP status on a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1e50-104">この手順では、製造オーダーの仕掛報告書の表示方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c1e50-104">This procedure shows how to view WIP statement on a production order.</span></span> <span data-ttu-id="c1e50-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c1e50-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c1e50-106">この手順は、原価の管理者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="c1e50-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="c1e50-107">[原価管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1e50-107">Click Cost administration.</span></span>
2. <span data-ttu-id="c1e50-108">[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1e50-108">Click Production orders.</span></span>
3. <span data-ttu-id="c1e50-109">[クイック フィルター] を使用して、[生産] フィールドで「p000153」という値を指定してフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="c1e50-109">Use the Quick Filter to filter on the Production field with a value of 'p000153'.</span></span>
4. <span data-ttu-id="c1e50-110">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1e50-110">On the Action Pane, click Manage costs.</span></span>
5. <span data-ttu-id="c1e50-111">[生産仕掛報告書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1e50-111">Click Production WIP statement.</span></span>
6. <span data-ttu-id="c1e50-112">[開始日] フィールドで、日付を「2012 年 12 月 1 日」に設定します。</span><span class="sxs-lookup"><span data-stu-id="c1e50-112">In the From date field, set the date to '2012-12-01'.</span></span>
7. <span data-ttu-id="c1e50-113">[終了日] フィールドで、日付を「2012 年 12 月 31 日」に設定します。</span><span class="sxs-lookup"><span data-stu-id="c1e50-113">In the To date field, set the date to '2012-12-31'.</span></span>

