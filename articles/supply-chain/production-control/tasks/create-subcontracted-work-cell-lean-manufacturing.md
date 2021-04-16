---
title: リーン生産の外注作業セルの作成
description: リーン生産の外注作業をモデル化するには、作業を提供する仕入先に関連付けられている作業セルを作成する必要があります。
author: cvocph
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0dc1e28202c42502cbec0f0066863d24d4396c88
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828901"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="2e8ee-103">リーン生産の外注作業セルの作成</span><span class="sxs-lookup"><span data-stu-id="2e8ee-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e8ee-104">リーン生産の外注作業をモデル化するには、作業を提供する仕入先に関連付けられている作業セルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="2e8ee-105">外注作業セルは、仕入先タイプのリソースの関連付けを通じて仕入先にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="2e8ee-106">USMF デモ会社でこの記録を行う場合、仕入先 ID 1002 およびサイト 1 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="2e8ee-107">仕入先リソースの作成</span><span class="sxs-lookup"><span data-stu-id="2e8ee-107">Create a vendor resource</span></span>
1. <span data-ttu-id="2e8ee-108">[リソース] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-108">Go to Resources.</span></span>
2. <span data-ttu-id="2e8ee-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-109">Click New.</span></span>
3. <span data-ttu-id="2e8ee-110">[リソース] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="2e8ee-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2e8ee-112">[タイプ] フィールドで [仕入先] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="2e8ee-113">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="2e8ee-114">リソース グループを作成する</span><span class="sxs-lookup"><span data-stu-id="2e8ee-114">Create the resource group</span></span>
1. <span data-ttu-id="2e8ee-115">[リソース グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="2e8ee-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-116">Click New.</span></span>
3. <span data-ttu-id="2e8ee-117">[リソース グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="2e8ee-118">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2e8ee-119">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2e8ee-120">作業セルが割り当てられるべきサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="2e8ee-121">理論上、サイトは仕入先が運用している 1 つのサイトを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="2e8ee-122">ただし、ほとんどの場合、外注されたリソースは外注業務を発注するサイトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="2e8ee-123">外注業務セルの入荷および出荷の倉庫が同じサイトである必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="2e8ee-124">[サイト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="2e8ee-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="2e8ee-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="2e8ee-126">[作業セル] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="2e8ee-127">[入庫倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2e8ee-128">仕入先管理作業セルの材料を示すために使用される倉庫および場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="2e8ee-129">多くの場合、仕入先ごとに 1 つの別の倉庫および作業のセルごとに 1 つの場所を使用して倉庫や場所がモデル化されます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="2e8ee-130">[入庫場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2e8ee-131">[出荷倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2e8ee-132">作業セルの外注活動が転記されるとき、材料が転記される倉庫および場所を定義します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="2e8ee-133">倉庫および場所は、仕入先がかんばん作業を報告する場合、仕入先サイトとなります。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="2e8ee-134">または、倉庫および場所は、生産フローの次の手順に関連付けられている受入場所にもなります。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="2e8ee-135">[出荷場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2e8ee-136">[カレンダー] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="2e8ee-137">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-137">Click Add.</span></span>
15. <span data-ttu-id="2e8ee-138">[カレンダー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2e8ee-139">作業セルの作業時間カレンダーをリソース グループに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="2e8ee-140">重要なリソースについては、正確な作業時間、および作業セルまたは仕入先サイトに関連する能力を表す特定のカレンダーを定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="2e8ee-141">[リソース] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="2e8ee-142">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-142">Click Add.</span></span>
    * <span data-ttu-id="2e8ee-143">外注リソース グループには、仕入先にリソース グループをリンクする仕入先タイプの関連付けられたリソースが必要です。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="2e8ee-144">[リソース] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2e8ee-145">以前のサブタスクで作成した仕入先リソースを選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="2e8ee-146">[作業セルの能力] セクションを展開、または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="2e8ee-147">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-147">Click Add.</span></span>
    * <span data-ttu-id="2e8ee-148">作業セルには、定義済能力が必要です。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="2e8ee-149">この例では、標準的な作業日あたり 100 個の処理能力を作成します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="2e8ee-150">[生産フロー モデル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="2e8ee-151">[能力期間] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="2e8ee-152">[平均スループット数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="2e8ee-153">[単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="2e8ee-154">[単位の変更] を解決します。</span><span class="sxs-lookup"><span data-stu-id="2e8ee-154">ResolveChanges the Unit.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]