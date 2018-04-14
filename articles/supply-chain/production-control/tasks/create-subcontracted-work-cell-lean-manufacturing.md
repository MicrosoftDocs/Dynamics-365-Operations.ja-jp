--- 
title: "リーン生産の外注作業セルの作成"
description: "リーン生産の外注作業をモデル化するには、作業を提供する仕入先に関連付けられている作業セルを作成する必要があります。"
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d5b7149551df33d439980ec4e04fa343749daa16
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="79866-103">リーン生産の外注作業セルの作成</span><span class="sxs-lookup"><span data-stu-id="79866-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79866-104">リーン生産の外注作業をモデル化するには、作業を提供する仕入先に関連付けられている作業セルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79866-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="79866-105">外注作業セルは、仕入先タイプのリソースの関連付けを通じて仕入先にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="79866-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="79866-106">USMF デモ会社でこの記録を行う場合、仕入先 ID 1002 およびサイト 1 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="79866-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="79866-107">仕入先リソースの作成</span><span class="sxs-lookup"><span data-stu-id="79866-107">Create a vendor resource</span></span>
1. <span data-ttu-id="79866-108">[リソース] に移動します。</span><span class="sxs-lookup"><span data-stu-id="79866-108">Go to Resources.</span></span>
2. <span data-ttu-id="79866-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="79866-109">Click New.</span></span>
3. <span data-ttu-id="79866-110">[リソース] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="79866-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="79866-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="79866-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="79866-112">[タイプ] フィールドで [仕入先] を選択します。</span><span class="sxs-lookup"><span data-stu-id="79866-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="79866-113">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="79866-114">リソース グループを作成する</span><span class="sxs-lookup"><span data-stu-id="79866-114">Create the resource group</span></span>
1. <span data-ttu-id="79866-115">[リソース グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="79866-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="79866-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="79866-116">Click New.</span></span>
3. <span data-ttu-id="79866-117">[リソース グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="79866-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="79866-118">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="79866-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="79866-119">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79866-120">作業セルが割り当てられるべきサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="79866-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="79866-121">理論上、サイトは仕入先が運用している 1 つのサイトを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="79866-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="79866-122">ただし、ほとんどの場合、外注されたリソースは外注業務を発注するサイトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="79866-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="79866-123">外注業務セルの入荷および出荷の倉庫が同じサイトである必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="79866-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="79866-124">[サイト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="79866-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="79866-125">[作業セル] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="79866-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="79866-126">[入庫倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79866-127">仕入先管理作業セルの材料を示すために使用される倉庫および場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="79866-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="79866-128">多くの場合、仕入先ごとに 1 つの別の倉庫および作業のセルごとに 1 つの場所を使用して倉庫や場所がモデル化されます。</span><span class="sxs-lookup"><span data-stu-id="79866-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="79866-129">[入庫場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="79866-130">[出荷倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79866-131">作業セルの外注活動が転記されるとき、材料が転記される倉庫および場所を定義します。</span><span class="sxs-lookup"><span data-stu-id="79866-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="79866-132">倉庫および場所は、仕入先がかんばん作業を報告する場合、仕入先サイトとなります。</span><span class="sxs-lookup"><span data-stu-id="79866-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="79866-133">または、倉庫および場所は、生産フローの次の手順に関連付けられている受入場所にもなります。</span><span class="sxs-lookup"><span data-stu-id="79866-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="79866-134">[出荷場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="79866-135">[カレンダー] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="79866-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="79866-136">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="79866-136">Click Add.</span></span>
15. <span data-ttu-id="79866-137">[カレンダー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79866-138">作業セルの作業時間カレンダーをリソース グループに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="79866-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="79866-139">重要なリソースについては、正確な作業時間、および作業セルまたは仕入先サイトに関連する能力を表す特定のカレンダーを定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="79866-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="79866-140">[リソース] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="79866-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="79866-141">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="79866-141">Click Add.</span></span>
    * <span data-ttu-id="79866-142">外注リソース グループには、仕入先にリソース グループをリンクする仕入先タイプの関連付けられたリソースが必要です。</span><span class="sxs-lookup"><span data-stu-id="79866-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="79866-143">[リソース] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79866-144">以前のサブタスクで作成した仕入先リソースを選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="79866-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="79866-145">[作業セルの能力] セクションを展開、または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="79866-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="79866-146">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="79866-146">Click Add.</span></span>
    * <span data-ttu-id="79866-147">作業セルには、定義済能力が必要です。</span><span class="sxs-lookup"><span data-stu-id="79866-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="79866-148">この例では、標準的な作業日あたり 100 個の処理能力を作成します。</span><span class="sxs-lookup"><span data-stu-id="79866-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="79866-149">[生産フロー モデル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="79866-150">[能力期間] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="79866-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="79866-151">[平均スループット数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="79866-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="79866-152">[単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="79866-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="79866-153">[単位の変更] を解決します。</span><span class="sxs-lookup"><span data-stu-id="79866-153">ResolveChanges the Unit.</span></span>


