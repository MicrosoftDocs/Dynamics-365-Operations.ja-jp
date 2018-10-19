--- 
title: "完成品の作成 (2016 年 2 月)"
description: "このタスクでは、完成品の作成に重点を置きます。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 44b3bf17c69f37e7a96c75345a3e4f27ba9eab50
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="2bfac-103">完成品の作成 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="2bfac-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bfac-104">このタスクでは、完成品の作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="2bfac-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="2bfac-105">これは、BOM 計算シリーズの最初のタスクです。</span><span class="sxs-lookup"><span data-stu-id="2bfac-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="2bfac-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="2bfac-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="2bfac-107">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2bfac-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2bfac-108">Click New.</span></span>
3. <span data-ttu-id="2bfac-109">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="2bfac-110">デモの場合、「BOM_1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="2bfac-111">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bfac-112">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-112">Select STD.</span></span> <span data-ttu-id="2bfac-113">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="2bfac-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="2bfac-114">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bfac-115">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-115">For example, select Audio.</span></span> <span data-ttu-id="2bfac-116">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="2bfac-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="2bfac-117">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bfac-118">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-118">Select SiteWH.</span></span> <span data-ttu-id="2bfac-119">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2bfac-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="2bfac-120">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bfac-121">追跡用分析コードはこの例には使用されません。「なし」を選択してください。</span><span class="sxs-lookup"><span data-stu-id="2bfac-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="2bfac-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2bfac-122">Click OK.</span></span>
9. <span data-ttu-id="2bfac-123">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2bfac-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="2bfac-124">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2bfac-124">Click Default order settings.</span></span>
11. <span data-ttu-id="2bfac-125">[既定の注文タイプ] フィールドで、「生産」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="2bfac-126">これは生成される完成品であるので、「生産」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="2bfac-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bfac-128">デモの場合は、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="2bfac-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bfac-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="2bfac-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bfac-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2bfac-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="2bfac-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2bfac-133">Close the page.</span></span>


