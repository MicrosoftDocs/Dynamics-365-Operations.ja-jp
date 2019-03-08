---
title: ライセンス プレートにより制御されていない場所での完了レポート (申請、2016 年 5 月)
description: このタスク ガイドでは、ライセンス プレートにより制御されていない場所への完了報告時の例を示します。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "344550"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="23405-103">ライセンス プレートにより制御されていない場所での完了レポート (申請、2016 年 5 月)</span><span class="sxs-lookup"><span data-stu-id="23405-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23405-104">このタスク ガイドでは、ライセンス プレートにより制御されていない場所への完了報告時の例を示します。</span><span class="sxs-lookup"><span data-stu-id="23405-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="23405-105">適用できる作業ポリシーは、このタスクの前提条件です。</span><span class="sxs-lookup"><span data-stu-id="23405-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="23405-106">前のタスク ガイドでは、作業ポリシーの設定を示しました。</span><span class="sxs-lookup"><span data-stu-id="23405-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="23405-107">このタスク ガイドでは、Dynamics AX アプリケーション 7.0.1 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="23405-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="23405-108">出荷場所の設定</span><span class="sxs-lookup"><span data-stu-id="23405-108">Set up an output location</span></span>
1. <span data-ttu-id="23405-109">[組織管理] > [リソース] > [リソース グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="23405-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="23405-110">一覧で、リソース グループ「5102」を選択します。</span><span class="sxs-lookup"><span data-stu-id="23405-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="23405-111">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-111">Click Edit.</span></span>
4. <span data-ttu-id="23405-112">[出荷倉庫] フィールドに、「51」を入力します。</span><span class="sxs-lookup"><span data-stu-id="23405-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="23405-113">[出荷場所] フィールドに、「001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="23405-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="23405-114">場所 001 はライセンス プレートにより制御される場所ではありません。</span><span class="sxs-lookup"><span data-stu-id="23405-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="23405-115">場所に適用できる作業ポリシーが存在する場合にのみ、ライセンス プレートのない出荷場所を設定できます。</span><span class="sxs-lookup"><span data-stu-id="23405-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="23405-116">製造オーダーを作成して完了として報告</span><span class="sxs-lookup"><span data-stu-id="23405-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="23405-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="23405-117">Close the page.</span></span>
2. <span data-ttu-id="23405-118">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="23405-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="23405-119">[新しい製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-119">Click New production order.</span></span>
4. <span data-ttu-id="23405-120">[品目番号] フィールドに、「L0101」を入力します。</span><span class="sxs-lookup"><span data-stu-id="23405-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="23405-121">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-121">Click Create.</span></span>
6. <span data-ttu-id="23405-122">アクション ペインで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="23405-123">[見積] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-123">Click Estimate.</span></span>
8. <span data-ttu-id="23405-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-124">Click OK.</span></span>
9. <span data-ttu-id="23405-125">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-125">Click Start.</span></span>
10. <span data-ttu-id="23405-126">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-126">Click the General tab.</span></span>
11. <span data-ttu-id="23405-127">[自動 BOM 消費] フィールドで、「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="23405-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="23405-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-128">Click OK.</span></span>
13. <span data-ttu-id="23405-129">［完了レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-129">Click Report as finished.</span></span>
14. <span data-ttu-id="23405-130">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-130">Click the General tab.</span></span>
15. <span data-ttu-id="23405-131">[エラー適用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="23405-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="23405-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-132">Click OK.</span></span>
17. <span data-ttu-id="23405-133">アクション ペインで [倉庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="23405-134">[作業の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23405-134">Click Work details.</span></span>
    * <span data-ttu-id="23405-135">製造オーダーが完了と報告されたときに、作業はプット アウェイに生成されませんでした。</span><span class="sxs-lookup"><span data-stu-id="23405-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="23405-136">これは、製品 L0101 が場所 001 に完了として報告されるときに作業が生成されないように作業ポリシーを定義しているために発生します。</span><span class="sxs-lookup"><span data-stu-id="23405-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

