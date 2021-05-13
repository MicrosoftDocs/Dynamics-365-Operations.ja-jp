---
title: 分析コード ベースの製品マスターの部品表の作成
description: この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920708"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="b2269-103">分析コード ベースの製品マスターの部品表の作成</span><span class="sxs-lookup"><span data-stu-id="b2269-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2269-104">この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2269-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="b2269-105">最初の 4 つの記録がこの手順を完了するのに必要なデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2269-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="b2269-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b2269-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b2269-107">このタスクは通常、製品デザイナーによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="b2269-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="b2269-108">製品を選択します</span><span class="sxs-lookup"><span data-stu-id="b2269-108">Select the product</span></span>

1. <span data-ttu-id="b2269-109">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2269-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b2269-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2269-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b2269-111">この順序による最初のタスク ガイドで作成した、分析コード ベースのコンフィギュレーション テクノロジ付きのリリース製品マスターを検索します。</span><span class="sxs-lookup"><span data-stu-id="b2269-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="b2269-112">アクション ペインで、**エンジニア** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="b2269-113">**BOM バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="b2269-114">新しい BOM と BOM バージョンを作成します</span><span class="sxs-lookup"><span data-stu-id="b2269-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="b2269-115">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-115">Select **New**.</span></span>
1. <span data-ttu-id="b2269-116">**BOM と BOM バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="b2269-117">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2269-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="b2269-118">サイトの設定</span><span class="sxs-lookup"><span data-stu-id="b2269-118">Setting a site</span></span>  
    * <span data-ttu-id="b2269-119">この手順では、BOM の特定のサイトは設定しません。</span><span class="sxs-lookup"><span data-stu-id="b2269-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="b2269-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-120">Select **OK**.</span></span>
1. <span data-ttu-id="b2269-121">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-121">Select **New**.</span></span>
    * <span data-ttu-id="b2269-122">この手順では、BOM に 4 つの明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2269-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="b2269-123">2 つの明細行はケーブル オプションを表し、もう 2 つの明細行はキャビネット オプションを表します。</span><span class="sxs-lookup"><span data-stu-id="b2269-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="b2269-124">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2269-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b2269-125">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2269-126">品目番号 A0001、HDMI 6' Cables を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="b2269-127">**コンフィギュレーション グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2269-128">この順序のガイド 4 で作成されたケーブル コンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="b2269-129">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-129">Select **New**.</span></span>
    * <span data-ttu-id="b2269-130">品目番号 A0002、HDMI 12' Cables を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="b2269-131">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2269-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b2269-132">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="b2269-133">**コンフィギュレーション グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2269-134">もう一度ケーブル コンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="b2269-135">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-135">Select **New**.</span></span>
1. <span data-ttu-id="b2269-136">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2269-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b2269-137">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2269-138">品目番号 D0002 Cabinet を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="b2269-139">**コンフィギュレーション グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2269-140">この BOM 明細行のキャビネット コンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="b2269-141">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-141">Select **New**.</span></span>
1. <span data-ttu-id="b2269-142">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2269-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b2269-143">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2269-144">最後の BOM 明細行として、品目番号 M0007 StandardCabinet を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="b2269-145">**コンフィギュレーション グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2269-146">最後の BOM 明細行にキャビネット コンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="b2269-147">承認と有効化</span><span class="sxs-lookup"><span data-stu-id="b2269-147">Approve and activate</span></span>

1. <span data-ttu-id="b2269-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2269-148">Close the page.</span></span>
1. <span data-ttu-id="b2269-149">**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-149">Select **Approve**.</span></span>
1. <span data-ttu-id="b2269-150">**承認者** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="b2269-151">**部品表も承認しますか?** フィールドで、*はい* を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="b2269-152">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-152">Select **OK**.</span></span>
1. <span data-ttu-id="b2269-153">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2269-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]