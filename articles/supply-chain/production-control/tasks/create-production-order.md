---
title: 製造オーダーの作成
description: この手順では、製造オーダーを作成する方法を示します。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e9358811f35e0417099ae65b0206e32a1455f84
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828973"
---
# <a name="create-a-production-order"></a><span data-ttu-id="6848e-103">製造オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="6848e-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6848e-104">この手順では、製造オーダーを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6848e-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="6848e-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6848e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6848e-106">これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 1 番目です。</span><span class="sxs-lookup"><span data-stu-id="6848e-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="6848e-107">製造オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="6848e-107">Create a production order</span></span>
1. <span data-ttu-id="6848e-108">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6848e-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="6848e-109">[新しい製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-109">Click New production order.</span></span>
3. <span data-ttu-id="6848e-110">[品目番号] フィールドに、'D0001' を入力します。</span><span class="sxs-lookup"><span data-stu-id="6848e-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="6848e-111">[出荷] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6848e-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="6848e-112">出荷日は、期日通りに配送できるように製造オーダーを終了させる必要のある日を示します。</span><span class="sxs-lookup"><span data-stu-id="6848e-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="6848e-113">この日付は、スケジューリング プロセスで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6848e-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="6848e-114">たとえば、出荷日から逆算して注文のスケジュールを決めることができます。</span><span class="sxs-lookup"><span data-stu-id="6848e-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="6848e-115">数量を '20' に設定します。</span><span class="sxs-lookup"><span data-stu-id="6848e-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="6848e-116">注記: BOM 番号フィールドには自動的に現在の品目について有効な BOM 番号が表示されますが、承認済 BOM バージョンの一覧から有効な BOM を選択することによって、製造オーダーの BOM を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6848e-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="6848e-117">注記: 工順番号フィールドには自動的に現在の品目について有効な工順番号が表示されますが、承認済の工順バージョンの一覧から有効な工順を選択することによって、製造オーダーの工順を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6848e-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="6848e-118">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="6848e-119">製造オーダーの検証</span><span class="sxs-lookup"><span data-stu-id="6848e-119">Validate the production order</span></span>
1. <span data-ttu-id="6848e-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6848e-121">作成した製造オーダー番号のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="6848e-122">これにより、注文の詳細ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="6848e-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="6848e-123">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-123">Click Edit.</span></span>
3. <span data-ttu-id="6848e-124">[出荷] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6848e-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="6848e-125">たとえば、製品オーダーの出荷日を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="6848e-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="6848e-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-126">Click Save.</span></span>
5. <span data-ttu-id="6848e-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6848e-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="6848e-128">BOM の更新</span><span class="sxs-lookup"><span data-stu-id="6848e-128">Update the BOM</span></span>
1. <span data-ttu-id="6848e-129">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="6848e-130">BOM をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-130">Click BOM.</span></span>
    * <span data-ttu-id="6848e-131">BOM のページを開き、製造オーダーの作成時に既定のデータからコピーされたBOMのデータを検証します。</span><span class="sxs-lookup"><span data-stu-id="6848e-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="6848e-132">この手順では、BOM の数量を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6848e-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="6848e-133">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-133">Click Edit.</span></span>
4. <span data-ttu-id="6848e-134">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6848e-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6848e-135">BOM 明細行の数量を変更すると、製造オーダーの材料消費の原価見積に影響します。</span><span class="sxs-lookup"><span data-stu-id="6848e-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="6848e-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-136">Click Save.</span></span>
6. <span data-ttu-id="6848e-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6848e-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="6848e-138">生産工順の更新</span><span class="sxs-lookup"><span data-stu-id="6848e-138">Update the production route</span></span>
1. <span data-ttu-id="6848e-139">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="6848e-140">[工順] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-140">Click Route.</span></span>
    * <span data-ttu-id="6848e-141">[工順] のページを開き、注文の作成時に既定のデータからコピーされた製造工順のデータを検証します。</span><span class="sxs-lookup"><span data-stu-id="6848e-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="6848e-142">この手順では、生産工順内の作業の数量を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6848e-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="6848e-143">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6848e-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6848e-144">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-144">Click Edit.</span></span>
5. <span data-ttu-id="6848e-145">処理数量 フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6848e-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="6848e-146">処理時間を変更すると、製造オーダーの見積工順消費と原価に影響します。</span><span class="sxs-lookup"><span data-stu-id="6848e-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="6848e-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6848e-147">Click Save.</span></span>
7. <span data-ttu-id="6848e-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6848e-148">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]