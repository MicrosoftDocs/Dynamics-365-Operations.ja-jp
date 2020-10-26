---
title: 分析コード ベースの製品マスターの部品表の作成
description: この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7961cfb4ad0e20c49d327d83f56c08811598ac1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986290"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="5d606-103">分析コード ベースの製品マスターの部品表の作成</span><span class="sxs-lookup"><span data-stu-id="5d606-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d606-104">この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d606-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="5d606-105">最初の 4 つの記録がこの手順を完了するのに必要なデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="5d606-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="5d606-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="5d606-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5d606-107">このタスクは通常、製品デザイナーによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="5d606-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="5d606-108">製品を選択します</span><span class="sxs-lookup"><span data-stu-id="5d606-108">Select the product</span></span>
1. <span data-ttu-id="5d606-109">[リリース済製品の保守] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="5d606-110">[リリース済製品] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-110">Click Released products.</span></span>
3. <span data-ttu-id="5d606-111">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5d606-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5d606-112">この順序による最初のタスク ガイドで作成した、分析コード ベースのコンフィギュレーション テクノロジ付きのリリース製品マスターを検索します。</span><span class="sxs-lookup"><span data-stu-id="5d606-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="5d606-113">アクション ペインで、[エンジニア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="5d606-114">[BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="5d606-115">新しい BOM と BOM バージョンを作成します</span><span class="sxs-lookup"><span data-stu-id="5d606-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="5d606-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-116">Click New.</span></span>
2. <span data-ttu-id="5d606-117">[BOM と BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="5d606-118">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d606-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="5d606-119">サイトの設定</span><span class="sxs-lookup"><span data-stu-id="5d606-119">Setting a site</span></span>  
    * <span data-ttu-id="5d606-120">この手順では、BOM の特定のサイトは設定しません。</span><span class="sxs-lookup"><span data-stu-id="5d606-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="5d606-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-121">Click OK.</span></span>
5. <span data-ttu-id="5d606-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-122">Click New.</span></span>
    * <span data-ttu-id="5d606-123">この手順では、BOM に 4 つの明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="5d606-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="5d606-124">2 つの明細行はケーブル オプションを表し、もう 2 つの明細行はキャビネット オプションを表します。</span><span class="sxs-lookup"><span data-stu-id="5d606-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="5d606-125">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5d606-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="5d606-126">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="5d606-127">品目番号 A0001、HDMI 6' Cables を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="5d606-128">[コンフィギュレーション グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="5d606-129">この順序のガイド 4 で作成されたケーブル コンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="5d606-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-130">Click New.</span></span>
    * <span data-ttu-id="5d606-131">品目番号 A0002、HDMI 12' Cables を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="5d606-132">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5d606-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="5d606-133">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="5d606-134">[コンフィギュレーション グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="5d606-135">もう一度ケーブル コンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="5d606-136">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-136">Click New.</span></span>
14. <span data-ttu-id="5d606-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5d606-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="5d606-138">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="5d606-139">品目番号 D0002 Cabinet を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="5d606-140">[コンフィギュレーション グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="5d606-141">この BOM 明細行のキャビネット コンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="5d606-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-142">Click New.</span></span>
18. <span data-ttu-id="5d606-143">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5d606-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="5d606-144">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="5d606-145">最後の BOM 明細行として、品目番号 M0007 StandardCabinet を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="5d606-146">[コンフィギュレーション グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="5d606-147">最後の BOM 明細行に [キャビネット コンフィギュレーション グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="5d606-148">承認と有効化</span><span class="sxs-lookup"><span data-stu-id="5d606-148">Approve and activate</span></span>
1. <span data-ttu-id="5d606-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5d606-149">Close the page.</span></span>
2. <span data-ttu-id="5d606-150">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-150">Click Approve.</span></span>
3. <span data-ttu-id="5d606-151">[承認者] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5d606-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="5d606-152">[部品表も承認しますか?] で [はい] を選択します。アクションを使用すると、このチェック ボックスは自動的にオンになります。</span><span class="sxs-lookup"><span data-stu-id="5d606-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="5d606-153">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-153">Click OK.</span></span>
6. <span data-ttu-id="5d606-154">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d606-154">Click Activate.</span></span>

