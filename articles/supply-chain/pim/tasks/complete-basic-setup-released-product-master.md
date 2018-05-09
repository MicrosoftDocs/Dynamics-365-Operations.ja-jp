--- 
title: "リリース済み製品マスターの基本設定の完了"
description: "この手順は、製品マスターを BOM バージョンで使用する前に必要な最小限の設定の完了方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 35ca13f157537087346a5bcf9c6ccdd659a0d772
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="57ca6-103">リリース済み製品マスターの基本設定の完了</span><span class="sxs-lookup"><span data-stu-id="57ca6-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57ca6-104">この手順は、製品マスターを BOM バージョンで使用する前に必要な最小限の設定の完了方法を示します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="57ca6-105">これは、分析コードベースのコンフィギュレーションでの組み合わせの作成方法を説明する 8 つの手順の 3 番目です。</span><span class="sxs-lookup"><span data-stu-id="57ca6-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="57ca6-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="57ca6-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="57ca6-107">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="57ca6-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57ca6-109">2 番目の手順でリリースする製品マスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="57ca6-110">この製品マスターは、分析コード ベースのコンフィギュレーション テクノロジで作成されます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="57ca6-111">アクション ウィンドウで、[製品] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="57ca6-112">[分析コード グループ] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="57ca6-113">[保管分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="57ca6-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57ca6-115">保管分析コード グループにより、製品トランザクションに使用される保管分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="57ca6-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="57ca6-116">この手順で [サイト] を選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="57ca6-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="57ca6-118">[追跡用分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="57ca6-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57ca6-120">追跡用分析コード グループにより、製品トランザクションに使用される追跡用分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="57ca6-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="57ca6-121">この手順で [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="57ca6-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="57ca6-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-123">Click OK.</span></span>
12. <span data-ttu-id="57ca6-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="57ca6-125">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-125">Click Edit.</span></span>
    * <span data-ttu-id="57ca6-126">[リリース済製品の詳細] フォームを開き、設定作業を続行します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="57ca6-127">[品目モデル グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="57ca6-128">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57ca6-129">品目モデル グループには、品目の入庫および出庫時における品目の管理方法および処理方法を決定する設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="57ca6-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="57ca6-130">在庫モデル グループは、品目消費の計算方法も決定します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="57ca6-131">この手順では [FIFO] を選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="57ca6-132">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="57ca6-133">[原価の管理] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="57ca6-134">[品目グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="57ca6-135">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57ca6-136">品目グループは、在庫品目の分類による在庫管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="57ca6-137">この手順では [CarAudio] を選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="57ca6-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="57ca6-139">アクション ウィンドウで、[計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="57ca6-140">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ca6-140">Click Default order settings.</span></span>
23. <span data-ttu-id="57ca6-141">[既定の注文タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="57ca6-142">[生産] を選択して、この製品マスターの既定の供給オプションが製品の生産であることを指定します。</span><span class="sxs-lookup"><span data-stu-id="57ca6-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="57ca6-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-143">Close the page.</span></span>
25. <span data-ttu-id="57ca6-144">[リリース製品の詳細] フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="57ca6-144">Close the Released product details form.</span></span>


