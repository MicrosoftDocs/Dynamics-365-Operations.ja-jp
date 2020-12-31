---
title: 原価管理ワークスペース パラメーターのコンフィギュレーション
description: '[原価管理ワークスペース] を構成するためにこの手順を使えば、コスト センターや製品グループのような組織内のさまざまなレベルのマネージャーが、原価オブジェクトを見抜くことができます。'
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca05f6174541a6e97ec94db209a99424a87550eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445335"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="3074b-103">原価管理ワークスペース パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3074b-103">Configure cost control workspace parameters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3074b-104">[原価管理ワークスペース] を構成するためにこの手順を使えば、コスト センターや製品グループのような組織内のさまざまなレベルのマネージャーが、原価オブジェクトを見抜くことができます。</span><span class="sxs-lookup"><span data-stu-id="3074b-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="3074b-105">USP2 デモ会社 が、この記録の作成に使用されました。</span><span class="sxs-lookup"><span data-stu-id="3074b-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="3074b-106">[原価会計] > [設定] > [原価管理ワークスペース コンフィギュレーション] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="3074b-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="3074b-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3074b-107">Click New.</span></span>
3. <span data-ttu-id="3074b-108">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3074b-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3074b-109">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3074b-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3074b-110">[公開済] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="3074b-111">このオプションで [はい] を設定すると、これらのロールのいずれかに割り当てられているユーザーは、原価管理ワークスペースでレポートを確認できます: 原価会計マネージャー、原価経理担当、原価経理担当係または原価オブジェクト コントローラー。</span><span class="sxs-lookup"><span data-stu-id="3074b-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="3074b-112">このオプションで [いいえ] を設定すると、これらのロールのいずれかに割り当てられているユーザーのみが、原価管理ワークスペースでレポートを確認できます: 原価会計マネージャー、原価経理担当、または原価経理担当係。</span><span class="sxs-lookup"><span data-stu-id="3074b-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="3074b-113">[データのフィルター処理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3074b-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="3074b-114">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="3074b-115">[予算の元のバージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="3074b-116">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="3074b-117">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="3074b-118">[計算レコードの割り当て] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3074b-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="3074b-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3074b-119">Click New.</span></span>
13. <span data-ttu-id="3074b-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="3074b-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="3074b-121">[会計カレンダー 期間] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="3074b-122">[実際のバージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="3074b-123">列のセクションごとの [会計年度期間] を展開します。</span><span class="sxs-lookup"><span data-stu-id="3074b-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="3074b-124">[現在の期間] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="3074b-125">[原価に表示する列] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3074b-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="3074b-126">[固定費] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="3074b-127">[変動費] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="3074b-128">[原価合計] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="3074b-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3074b-129">Click Save.</span></span>
23. <span data-ttu-id="3074b-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3074b-130">Close the page.</span></span>
24. <span data-ttu-id="3074b-131">[原価会計] > [ワークスペース] > [原価管理] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="3074b-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="3074b-132">選択した会計年度期間の固定、変動、合計、および不明の原価を表示する明細書を選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="3074b-133">[会計カレンダー 期間] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="3074b-134">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3074b-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3074b-135">[原価オブジェクト分析コード階層] を選択後、[原価要素分析コード階層] を展開し、要求された原価の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="3074b-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="3074b-136">たとえば、値を表示するには、階層から [製造間接費] へ展開できます。</span><span class="sxs-lookup"><span data-stu-id="3074b-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

