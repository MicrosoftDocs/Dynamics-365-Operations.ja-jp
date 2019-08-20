---
title: リーン生産作業セルの定義
description: 作業セルは、リーン生産のプロセス活動で使用できるリソース グループの特定のフォームです。
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfce85b43a4678bf94a5570f4df047249cf29d1e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836291"
---
# <a name="define-lean-manufacturing-work-cells"></a><span data-ttu-id="9e13d-103">リーン生産作業セルの定義</span><span class="sxs-lookup"><span data-stu-id="9e13d-103">Define lean manufacturing work cells</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e13d-104">作業セルは、リーン生産のプロセス活動で使用できるリソース グループの特定のフォームです。</span><span class="sxs-lookup"><span data-stu-id="9e13d-104">A work cell is a specific form of resource groups that can be used in lean manufacturing process activities.</span></span> <span data-ttu-id="9e13d-105">作業セルには、入荷および出荷場所と生産フロー モデルに基づいた能力定義があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-105">Work cells have input and output locations and a capacity definition based on a production flow model.</span></span> <span data-ttu-id="9e13d-106">リーン生産の作業セルと能力計算の基本概念に関する詳細については、リーン生産についてのホワイト ペーパーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e13d-106">To learn more about the basic concepts of lean manufacturing work cells and capacity calculations, see the white papers on Lean manufacturing.</span></span> <span data-ttu-id="9e13d-107">この手順の作成に使用するデモ データの会社は USMF</span><span class="sxs-lookup"><span data-stu-id="9e13d-107">The demo data company used to create this procedure is USMF</span></span>


## <a name="create-a-work-cell"></a><span data-ttu-id="9e13d-108">作業セルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-108">Create a work cell.</span></span> 
1. <span data-ttu-id="9e13d-109">[組織管理] > [リソース] > [リソース グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="9e13d-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-110">Click New.</span></span>
3. <span data-ttu-id="9e13d-111">[リソース グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-111">In the Resource group field, type a value.</span></span>
    * <span data-ttu-id="9e13d-112">作業セルの ID は、通常、組織コードで、法人に対して固有である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-112">The work cell ID is typically a systematic code and has to be unique for the legal entity.</span></span>  
4. <span data-ttu-id="9e13d-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-113">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9e13d-114">説明には、作業セルの名前またはタイトルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-114">The description contains the name or title of the work cell.</span></span>  
5. <span data-ttu-id="9e13d-115">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9e13d-116">作業セルは 1 つの特定のサイト上にあります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-116">A work cell is located at one specific site.</span></span> <span data-ttu-id="9e13d-117">入荷および出荷の倉庫と場所の両方がこのサイト上に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-117">Both input and output warehouse and location have to be located on this site.</span></span>  
6. <span data-ttu-id="9e13d-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-118">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9e13d-119">[生産単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-119">In the Production unit field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9e13d-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9e13d-121">この作業セルが属する生産単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-121">Select a production unit that this work cell belongs to.</span></span>  
9. <span data-ttu-id="9e13d-122">[作業セル] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-122">Select the Work cell check box.</span></span>
    * <span data-ttu-id="9e13d-123">リーン作業セルとしてリソース グループを使用するには、作業セルのチェック ボックス選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-123">To use a resource group as a lean work cell, the Work cell check box has to be selected.</span></span>  <span data-ttu-id="9e13d-124">リソース グループを作成したら、このプロパティを変更できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9e13d-124">Note that this property cannot be changed after resource group is created.</span></span>  
10. <span data-ttu-id="9e13d-125">[入庫倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-125">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="9e13d-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9e13d-127">会計および部品管理のために、作業現場で指定される材料は、通常特定の仮想倉庫に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-127">For accounting and material control, the material staged on the shop floor is typically allocated to a specific virtual warehouse.</span></span> <span data-ttu-id="9e13d-128">ただし、倉庫の作業を使用して場所を補充する場合は、受入原材料倉庫の一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-128">However, if you want to replenish the locations using warehouse work, they must be part of the receptive raw material warehouse.</span></span>  
12. <span data-ttu-id="9e13d-129">[入庫場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="9e13d-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9e13d-131">プロセス活動のため、入庫場所は一般的に、またはプロセス活動にフィードするピッキング活動を定義することにより、特定の製品または製品バリアントのために上書きできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9e13d-131">Note that for a process activity, the input location can by overwritten in general or for a specific product or product variant by defining picking activities that feed to the process activity.</span></span> <span data-ttu-id="9e13d-132">作業セルの入庫場所はライセンス番号により制御することはできません。</span><span class="sxs-lookup"><span data-stu-id="9e13d-132">The input locations of a work cell cannot be license plate controlled.</span></span>  
14. <span data-ttu-id="9e13d-133">[出荷倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-133">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="9e13d-134">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-134">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e13d-135">複数の生産フローの活動または生産ラインでは、多くは次の作業セルの入庫倉庫、または、製品が生産プロセスの後で通常移動する販売または流通倉庫です。</span><span class="sxs-lookup"><span data-stu-id="9e13d-135">In multiple activity production flows or production lines, this is often the input warehouse of the next work cell or the sales or transit warehouse where a product is typically transferred to after the production process.</span></span> <span data-ttu-id="9e13d-136">リーン生産のプロセスをモデリングする場合、転送を報告されるので、転送は通常不要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9e13d-136">Remember when modeling lean manufacturing processes, transport is usually waste, as is reporting transport.</span></span>  
16. <span data-ttu-id="9e13d-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9e13d-138">[出荷場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-138">In the Output location field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9e13d-139">複数のプロセス活動の生産フローは、通常、次の作業セルの入庫場所です。</span><span class="sxs-lookup"><span data-stu-id="9e13d-139">In a production flow with multiple process activites this if often the input location of the next work cell.</span></span>  
18. <span data-ttu-id="9e13d-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="9e13d-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="9e13d-142">[操作] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-142">Expand or collapse the Operation section.</span></span>
    * <span data-ttu-id="9e13d-143">[実行時間カテゴリ] は、リーンかんばん作業の原価計算と処理を有効にするために提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-143">A Run time category must be provided to enable cost calculation and processing of lean kanban jobs.</span></span>  
21. <span data-ttu-id="9e13d-144">[実行時間カテゴリ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-144">In the Run time category field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="9e13d-145">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e13d-146">実行時間の原価カテゴリは、標準原価計算と一括引き落とし原価計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-146">The run time cost category is used in standard cost calculation and on backflush costing.</span></span>  
23. <span data-ttu-id="9e13d-147">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-147">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="9e13d-148">[カレンダー] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-148">Expand or collapse the Calendars section.</span></span>
25. <span data-ttu-id="9e13d-149">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-149">Click Add.</span></span>
26. <span data-ttu-id="9e13d-150">[カレンダー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-150">In the Calendar field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="9e13d-151">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-151">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e13d-152">通常、特定のサイトの作業セルは、同じ作業時間カレンダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-152">Typically work cells of a given site use the same working time calendar.</span></span> <span data-ttu-id="9e13d-153">作業セルが個別の作業時間を持つことができる場合、作業セルの特定の作業時間カレンダーを作成しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-153">If work cells can have individual working times, you might need to create a specific working time calendar for the work cell.</span></span> <span data-ttu-id="9e13d-154">能力定義は通常、作業日の標準勤務時間に関連付けられるため、リーン作業セルに使用される場合、カレンダーが標準勤務時間を定義する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9e13d-154">Note that the calendar should have a standard working time defined when used for a lean work cell, because the capacity definition is usually related to the standard working time of a work day.</span></span>  
28. <span data-ttu-id="9e13d-155">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-155">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="9e13d-156">[作業セルの能力] セクションを展開、または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-156">Expand or collapse the Work cell capacity section.</span></span>
30. <span data-ttu-id="9e13d-157">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-157">Click Add.</span></span>
31. <span data-ttu-id="9e13d-158">[生産フロー モデル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-158">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="9e13d-159">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-159">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e13d-160">この手順には、スループット能力の定義を示すため、生産フロー モデル タイプの [スループット] が必要です。</span><span class="sxs-lookup"><span data-stu-id="9e13d-160">This procedures requires production flow model type Throughput, to show the definition of throughput capacity.</span></span>  
33. <span data-ttu-id="9e13d-161">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-161">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="9e13d-162">[能力期間] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-162">In the Capacity period field, select an option.</span></span>
    * <span data-ttu-id="9e13d-163">オプションには次のものが含まれます:   能力は、作業セルの作業時間カレンダーの標準的な作業日の長さで示されます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-163">The options include:   Standard workday - The capacity is expressed by the length of the standard workday of the working time calendar for the work cell.</span></span> <span data-ttu-id="9e13d-164">それぞれの日に対して、カレンダーから実際の作業時間が決定され、それに基づいて使用可能な有効能力が計算されます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-164">For each day, the actual working time is determined from the calendar and the effective available capacity is calculated based on that.</span></span>   <span data-ttu-id="9e13d-165">[週] - 週ごとの能力を許可します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-165">Week - Allows a weekly capacity.</span></span> <span data-ttu-id="9e13d-166">実際の作業時間による調整はされません。</span><span class="sxs-lookup"><span data-stu-id="9e13d-166">There is no adjustment done by the actual working time.</span></span>   <span data-ttu-id="9e13d-167">[月] - 月ごとの能力を許可します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-167">Month - Allows a monthly capacity.</span></span> <span data-ttu-id="9e13d-168">実際の能力による調整はされません。</span><span class="sxs-lookup"><span data-stu-id="9e13d-168">There is no adjustment done by the actual capacity.</span></span>   <span data-ttu-id="9e13d-169">通常、標準的な作業日は日ごとの期間に使用され、週ごとの能力は週ごとの能力期間に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-169">Typically, the standard workday is used for daily periods and the weekly capacity is used for weekly capacity periods.</span></span>  
35. <span data-ttu-id="9e13d-170">[平均スループット数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-170">In the Average throughput quantity field, enter a number.</span></span>
    * <span data-ttu-id="9e13d-171">リーン操作は、理想的な環境では最大可能能力には設定されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9e13d-171">Note that a lean operation is never set up for the maximum possible capacity in an ideal environment.</span></span> <span data-ttu-id="9e13d-172">代わりに、能力は常に一般的な状況で実行される工程用に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-172">Instead the capacity should always be defined for operations running under typical circumstances.</span></span>  
36. <span data-ttu-id="9e13d-173">[単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-173">In the Unit field, click the drop-down button to open the lookup.</span></span>
37. <span data-ttu-id="9e13d-174">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-174">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="9e13d-175">[単位の変更] を解決します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-175">ResolveChanges the Unit.</span></span>

## <a name="add-a-financial-dimension"></a><span data-ttu-id="9e13d-176">財務分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="9e13d-176">Add a financial dimension</span></span>
1. <span data-ttu-id="9e13d-177">[財務分析コード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-177">Expand or collapse the Financial dimensions section.</span></span>
    * <span data-ttu-id="9e13d-178">生産フローで定義されている財務分析コードが、所定の作業セルの財務分析コードを上書きすることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9e13d-178">Note that financial dimensions defined on the production flow override the financial dimension of a given work cell.</span></span>    <span data-ttu-id="9e13d-179">選択できる財務分析コードは、システムの財務分析コードのコンフィギュレーションによって決まります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-179">The financial dimensions that can be selected depend on the configuration of the financial dimensions of your system.</span></span> <span data-ttu-id="9e13d-180">次の手順は、USMF 会社のデモ データ セットに対応します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-180">The following steps correspond to the Demo data set in company USMF.</span></span> <span data-ttu-id="9e13d-181">異なるデータを使用すると、この手順は当てはまらない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-181">When using different data, the steps might not be applicable.</span></span>  
2. <span data-ttu-id="9e13d-182">CostCenter フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-182">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9e13d-183">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-183">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e13d-184">リーン作業セルで選択する必要がある分析コードは、特定の法人の会計モデルの財務分析コードの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9e13d-184">The dimensions that need to be selected on lean work cells depend on the implementation of financial dimensions in the accounting model for a specific legal entity.</span></span>  
4. <span data-ttu-id="9e13d-185">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9e13d-186">CostCenter フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e13d-186">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9e13d-187">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e13d-187">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9e13d-188">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-188">In the list, click the link in the selected row.</span></span>

## <a name="save"></a><span data-ttu-id="9e13d-189">保存</span><span class="sxs-lookup"><span data-stu-id="9e13d-189">Save</span></span>
1. <span data-ttu-id="9e13d-190">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e13d-190">Click Save.</span></span>

