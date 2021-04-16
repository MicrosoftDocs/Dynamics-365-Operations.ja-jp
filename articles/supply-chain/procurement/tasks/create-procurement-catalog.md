---
title: 調達カタログの作成
description: このトピックでは、調達カタログの作成方法を説明します。
author: kamaybac
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59117df519b7aa525713d3acd70195cc42614b9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812401"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="27f53-103">調達カタログの作成</span><span class="sxs-lookup"><span data-stu-id="27f53-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27f53-104">このトピックでは、調達カタログの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="27f53-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="27f53-105">通常、このタスクを実行するのは、調達担当者です。</span><span class="sxs-lookup"><span data-stu-id="27f53-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="27f53-106">さらに従業員が要求を作成する際にカタログを使用する方法も参照できます。</span><span class="sxs-lookup"><span data-stu-id="27f53-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="27f53-107">カタログを作成する前に、システム内に調達カテゴリ階層が必要です。</span><span class="sxs-lookup"><span data-stu-id="27f53-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="27f53-108">階層は、階層にあるすべての製品とともに、新しいカタログによって継承されます。</span><span class="sxs-lookup"><span data-stu-id="27f53-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="27f53-109">調達カテゴリ階層を使用する場合、さらに手順ステップで使用される例にも、このガイドをデモ データ会社 USMF で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="27f53-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="27f53-110">調達カテゴリ階層が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="27f53-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="27f53-111">**ナビゲーション ウィンドウ > モジュール > 調達 > 調達カテゴリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27f53-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="27f53-112">調達カテゴリ階層は USMF のデモ データ会社内で使用でき、製品は **オフィス機器/コンピュータ** カテゴリに追加されました。</span><span class="sxs-lookup"><span data-stu-id="27f53-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="27f53-113">この手順をタスク ガイドとして実行している場合は、カテゴリを参照するときガイドのロックを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f53-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="27f53-114">階層を使用できない場合は、**新規** をクリックして階層を作成します。</span><span class="sxs-lookup"><span data-stu-id="27f53-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="27f53-115">これが実行可能な回数は一度だけです。</span><span class="sxs-lookup"><span data-stu-id="27f53-115">This can only be done once.</span></span>  
2. <span data-ttu-id="27f53-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27f53-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="27f53-117">カタログの作成</span><span class="sxs-lookup"><span data-stu-id="27f53-117">Create a catalog</span></span>
1. <span data-ttu-id="27f53-118">**ナビゲーション ウィンドウ > モジュール > 調達 > カタログ > 調達カタログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27f53-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="27f53-119">**新しい調達カタログ** を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="27f53-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="27f53-120">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27f53-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="27f53-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-121">Select **OK**.</span></span>
5. <span data-ttu-id="27f53-122">ツリーで、**CORP PROCUREMENT CATEGORIES** を展開します。</span><span class="sxs-lookup"><span data-stu-id="27f53-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="27f53-123">ツリーで、**OFFICE MACHINES** を展開します。</span><span class="sxs-lookup"><span data-stu-id="27f53-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="27f53-124">ツリーで、**コンピューター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="27f53-125">調達カテゴリからの製品が一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="27f53-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="27f53-126">製品をカテゴリに追加する場合は、**調達カテゴリ階層** ページまたは **品目の詳細** ページで追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f53-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="27f53-127">**既定** の更新タイプは、調達カテゴリ階層に追加された新しい製品をすぐにカタログに表示するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="27f53-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="27f53-128">更新タイプが **動的** に設定されている場合、変更はすぐに表示されます。</span><span class="sxs-lookup"><span data-stu-id="27f53-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="27f53-129">更新タイプが **静的** の場合、新しい製品は、カタログが再公開された後にカタログを使用している従業員にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="27f53-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="27f53-130">**公開** アクションはページ上部のアクション ウィンドウで使用できます。</span><span class="sxs-lookup"><span data-stu-id="27f53-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="27f53-131">製品が調達カテゴリ階層から削除されると、**既定** の更新タイプ フィールドの値に関係なく、変更はすぐに表示されます。</span><span class="sxs-lookup"><span data-stu-id="27f53-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="27f53-132">アクション ウィンドウで、**カテゴリ ナビゲーション** を選択し、**有効化** が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="27f53-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="27f53-133">**カタログの有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="27f53-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27f53-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="27f53-135">カタログを表示します</span><span class="sxs-lookup"><span data-stu-id="27f53-135">Make the catalog visible</span></span>
1. <span data-ttu-id="27f53-136">**ナビゲーション ウィンドウ > モジュール > 調達 > 設定 > ポリシー > 購買ポリシー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27f53-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="27f53-137">**調達ポリシー USMF** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="27f53-138">作業者がユーザー プロファイルに接続して製品を注文することができるよう、法人の購入ポリシーを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27f53-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="27f53-139">USMF のデモ データでは、管理者ユーザーは **ジュリア ファンダーバーク** と呼ばれる作業者に接続され、既定の USMF で製品を注文します。</span><span class="sxs-lookup"><span data-stu-id="27f53-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="27f53-140">作成したばかりのカタログを選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="27f53-141">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="27f53-142">カタログを使用します</span><span class="sxs-lookup"><span data-stu-id="27f53-142">Use the catalog</span></span>
1. <span data-ttu-id="27f53-143">**ナビゲーション ウィンドウ > モジュール > 調達 > 購買要求 > すべての購買要求** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27f53-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="27f53-144">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-144">Select **New**.</span></span>
3. <span data-ttu-id="27f53-145">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27f53-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="27f53-146">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-146">Select **OK**.</span></span>
5. <span data-ttu-id="27f53-147">**製品の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-147">Select **Add products**.</span></span>
6. <span data-ttu-id="27f53-148">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="27f53-149">左のカテゴリ階層またはリストの先頭にあるフィルターを使用して、製品をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="27f53-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="27f53-150">**明細行に追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="27f53-151">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27f53-151">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]