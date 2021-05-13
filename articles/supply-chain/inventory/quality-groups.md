---
title: 品目品質グループ
description: このトピックでは、品目品質グループの使用および作成して、製品を論理的にグループ化し、品質指示の自動生成用に品質関連に割り当てる方法について説明します。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3074a6a8cc054be045bf593b509e76a1043af0b7
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956725"
---
# <a name="item-quality-groups"></a><span data-ttu-id="3653a-103">品目品質グループ</span><span class="sxs-lookup"><span data-stu-id="3653a-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3653a-104">品質グループとは、複数の品目に共通するテスト要件です。</span><span class="sxs-lookup"><span data-stu-id="3653a-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="3653a-105">このトピックでは、品目品質グループの使用および作成して、製品を論理的にグループ化し、品質指示の自動生成用に品質関連に割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3653a-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="3653a-106">品質グループに割り当てられる品目、または品目に割り当てられる品質グループを、設定、編集、および表示するには、**在庫管理 \> 設定 \> 品質グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3653a-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="3653a-107">**テスト グループ** ページのテスト要件を定義した後、品質指示を自動生成するルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="3653a-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="3653a-108">プロセスを簡略化するため、個別の品目のルールは定義しません。</span><span class="sxs-lookup"><span data-stu-id="3653a-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="3653a-109">代わりに、**品質関連** ページの品質グループのルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="3653a-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="3653a-110">品目品質グループの例</span><span class="sxs-lookup"><span data-stu-id="3653a-110">Example of an item quality group</span></span>

<span data-ttu-id="3653a-111">ある製造会社で、受入検査に同じテスト要件があるさまざまな原材料を購入しています。</span><span class="sxs-lookup"><span data-stu-id="3653a-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="3653a-112">そのため、その会社では品質グループを定義し、そのグループに原材料と関連付けた品目番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3653a-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="3653a-113">後で、同じテスト要件がある新しいタイプの原材料を購入します。</span><span class="sxs-lookup"><span data-stu-id="3653a-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="3653a-114">新しい材料の新しいテスト要件を設定せずに、既存の品質グループに新しい材料の品目番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="3653a-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="3653a-115">また、同じ会社では同じ製造テスト要件の品目を製造し、同じ要件で出荷前テストを実行して品目を出荷しています。</span><span class="sxs-lookup"><span data-stu-id="3653a-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="3653a-116">したがって、この会社はさらに 2 つの品質グループを定義し、各グループに関連品目番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3653a-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="3653a-117">品質グループの作成</span><span class="sxs-lookup"><span data-stu-id="3653a-117">Create a quality group</span></span>

<span data-ttu-id="3653a-118">品質グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3653a-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="3653a-119">**在庫管理 \> 設定 \> 品質管理 \> 品質グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3653a-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="3653a-120">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="3653a-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="3653a-121">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="3653a-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="3653a-122">**品質グループ** – 品質グループの固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3653a-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="3653a-123">**説明** – 品質グループの詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="3653a-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="3653a-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3653a-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="3653a-125">品目を品質グループに手動で追加する</span><span class="sxs-lookup"><span data-stu-id="3653a-125">Manually add items to a quality group</span></span>

<span data-ttu-id="3653a-126">品目を品質グループに手動で追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3653a-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="3653a-127">**在庫管理 \> 設定 \> 品質管理 \> 品質グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3653a-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="3653a-128">品目を追加する品質グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="3653a-129">アクション ペインで、**品目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="3653a-130">アクション ウィンドウの、**品質グループの品目** ページで、**新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="3653a-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="3653a-131">次に、新しい行に対して、**品目番号** フィールドを追加する品目番号に設定します。</span><span class="sxs-lookup"><span data-stu-id="3653a-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="3653a-132">追加する新しい品目ごとに前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3653a-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="3653a-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3653a-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="3653a-134">複数品目を品質グループに追加する</span><span class="sxs-lookup"><span data-stu-id="3653a-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="3653a-135">複数品目を品質グループに追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3653a-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="3653a-136">**在庫管理 \> 設定 \> 品質管理 \> 品質グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3653a-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="3653a-137">品目を追加する品質グループを作成および選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="3653a-138">アクション ペインで、**品目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="3653a-139">**照会** ダイアログ ボックスで、追加する品目のフィルター条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="3653a-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="3653a-140">たとえば、特定の品目グループのすべての品目をフィルター処理する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3653a-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="3653a-141">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-141">Select **OK**.</span></span>
1. <span data-ttu-id="3653a-142">**品目の追加** ダイアログ ボックスで、クエリに一致するすべての品目がグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3653a-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="3653a-143">結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="3653a-143">Review the results.</span></span>

    <span data-ttu-id="3653a-144">変更が必要な場合は、**選択** をオンにして **照会** ダイアログ ボックスに戻り、クエリを調整します。</span><span class="sxs-lookup"><span data-stu-id="3653a-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="3653a-145">追加するすべての品目が結果に含まれる場合は、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="3653a-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3653a-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="3653a-147">品目を品質グループに手動で関連付ける</span><span class="sxs-lookup"><span data-stu-id="3653a-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="3653a-148">品目を品質グループに手動で関連付けるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3653a-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="3653a-149">**在庫管理 \> 設定 \> 品質管理 \> 品目品質グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3653a-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="3653a-150">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="3653a-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="3653a-151">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="3653a-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="3653a-152">**品目番号** – 追加する品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="3653a-153">**品質グループ** – 品目に割り当てる品質グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="3653a-154">追加する必要がある品目と品質グループの組み合わせごとに、前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3653a-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="3653a-155">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3653a-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="3653a-156">リリース済製品ページからの品質グループを手動で追加する</span><span class="sxs-lookup"><span data-stu-id="3653a-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="3653a-157">**リリース済製品** ページからの品質グループを手動で追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3653a-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="3653a-158">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3653a-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="3653a-159">品質グループを割り当てる製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="3653a-160">アクション ウィンドウの、**在庫の管理** タブの、**品質** グループで、**品目品質グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3653a-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="3653a-161">アクション ウィンドウの、**品質グループの品目** ページで、**新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="3653a-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="3653a-162">次に、新しい行に対して、**品質グループ** フィールドを製品に割り当てる品質グループに設定します。</span><span class="sxs-lookup"><span data-stu-id="3653a-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="3653a-163">製品に割り当てる追加の品質グループごとに前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3653a-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="3653a-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3653a-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3653a-165">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3653a-165">Additional resources</span></span>

- [<span data-ttu-id="3653a-166">品質管理テスト機器</span><span class="sxs-lookup"><span data-stu-id="3653a-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="3653a-167">品質管理テスト</span><span class="sxs-lookup"><span data-stu-id="3653a-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="3653a-168">品質管理テスト グループ</span><span class="sxs-lookup"><span data-stu-id="3653a-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="3653a-169">品質管理テスト変数</span><span class="sxs-lookup"><span data-stu-id="3653a-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="3653a-170">品質関連</span><span class="sxs-lookup"><span data-stu-id="3653a-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
