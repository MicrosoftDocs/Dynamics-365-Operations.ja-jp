---
title: 倉庫トランザクション用製品フィルターの構成
description: このトピックでは、製品フィルターやフィルター コードを構成し、倉庫の在庫品目を分類する方法について説明します。 また、特定の品目を注文できる顧客や特定の仕入先から購入できる品目を指定するために、フィルターを使用することもできます。
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: dbf92c5e199ecadb3e4f7c6130427d449ef5b6c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251772"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a><span data-ttu-id="6d65f-104">倉庫トランザクション用製品フィルターの構成</span><span class="sxs-lookup"><span data-stu-id="6d65f-104">Configure product filters for warehouse transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d65f-105">このトピックでは、製品フィルターやフィルター コードを構成し、倉庫の在庫品目を分類する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-105">This topic describes how to configure product filters and filter codes to categorize inventory items in a warehouse.</span></span> <span data-ttu-id="6d65f-106">また、特定の品目を注文できる顧客や特定の仕入先から購入できる品目を指定するために、フィルターを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-106">You can also use filters to specify which customers can order a particular item and which items can be purchased from a particular vendor.</span></span>

<span data-ttu-id="6d65f-107">また、製品フィルターを設定および使用して、自動的に倉庫の在庫品目を整理し、フィルター処理された品目をフィルター グループに結合することができます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-107">Additionally, you can set up and use product filters to automatically organize inventory items in a warehouse and combine filtered items into filter groups.</span></span> <span data-ttu-id="6d65f-108">フィルターは、品目を処理プロセス、購買プロセス、および販売プロセスのカテゴリに分類するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-108">Filters can be used to put items into categories for handling, purchasing, and selling processes.</span></span> <span data-ttu-id="6d65f-109">品目の処理方法が重量や処理制限に基づく場合は、品目をグループ化したり、個別に分けたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-109">You might want to group items together or separate them from each other when the way that they are handled is based on weight or handling restrictions.</span></span> <span data-ttu-id="6d65f-110">また、品目を購入または販売できる顧客または仕入先を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-110">You can also specify which customers or vendors an item can be purchased from or sold to.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6d65f-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="6d65f-111">Prerequisites</span></span>

<span data-ttu-id="6d65f-112">次の表に、開始する前に準備が整っている必要のある前提条件を示します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-112">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="6d65f-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="6d65f-113">Prerequisite</span></span> | <span data-ttu-id="6d65f-114">指示</span><span class="sxs-lookup"><span data-stu-id="6d65f-114">Instructions</span></span> |
|---|---|
| <span data-ttu-id="6d65f-115">**リリース済製品の詳細** ページで製品の構成を開始する前に、製品の保管分析コード グループに対する倉庫処理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-115">Before you start to configure products on the **Released product details** page, you must turn on warehouse processing for the product's storage dimension group.</span></span> | <span data-ttu-id="6d65f-116">**製品情報管理 \> 設定 \> 分析コードとバリアント グループ \> 保管分析コード グループ** に移動し、**倉庫管理プロセスの使用** オプションが *はい* に設定されている保管分析コード グループを選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-116">Go to **Product information management \> Setup \> Dimension and variant groups \> Storage dimension groups**, and select or create a storage dimension group where the **Use warehouse management processes** option is set to *Yes*.</span></span> |
| <span data-ttu-id="6d65f-117">顧客フィルターまたは仕入先フィルター、あるいはその両方を使用する場合は、倉庫管理パラメーターでその使用を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-117">If you will use customer filters and/or vendor filters, you must enable their use in Warehouse management parameters.</span></span> | <span data-ttu-id="6d65f-118">**倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="6d65f-119">**製品フィルター** タブで、**顧客フィルターの有効化** オプション、および/または **仕入先フィルターの有効化** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-119">On the **Product filters** tab, set the **Enable customer filters** and/or **Enable vendor filters** option  to *Yes*.</span></span> |

## <a name="set-up-product-filters"></a><span data-ttu-id="6d65f-120">製品フィルターの設定</span><span class="sxs-lookup"><span data-stu-id="6d65f-120">Set up product filters</span></span>

<span data-ttu-id="6d65f-121">製品フィルターには、列挙 (列挙型) 値である、最大 10 個の **フィルター タイトル** 特性があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-121">Product filters provide up to 10 **Filter title** characteristics, which are enumeration (enum) values.</span></span> <span data-ttu-id="6d65f-122">これらの列挙値は、製品フィルターを作成するときに選択できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-122">These enum values are available for selection when you create a product filter.</span></span> <span data-ttu-id="6d65f-123">*コード 1* から *コード 10* の列挙値はシステム定義であり、品目の特定の特性または属性を表します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-123">The enum values *Code 1* through *Code 10* are system-defined and represent a specific characteristic or attribute of an item.</span></span> <span data-ttu-id="6d65f-124">たとえば、*コード 1* は危険物分類を持つ品目を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-124">For example, *Code 1* might represent items that have a hazardous material classification.</span></span> <span data-ttu-id="6d65f-125">*コード 2* は、仕入先だけが購入できる品目を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-125">*Code 2* might represent items that only vendors can purchase.</span></span> <span data-ttu-id="6d65f-126">次に、製品フィルターは、**フィルタータイトル** 値に関連付けられた特定の **フィルター コード** 値を定義します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-126">Product filters then define the specific **Filter code** value that is associated with a **Filter title** value.</span></span>

1. <span data-ttu-id="6d65f-127">**倉庫管理 \> 設定 \> 製品フィルター \> 製品フィルター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-127">Go to **Warehouse management \> Setup \> Product filters \> Product filters**.</span></span>
1. <span data-ttu-id="6d65f-128">アクション ペインで **新規** を選択して、製品フィルターをグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-128">On the Action Pane, select **New** to add a product filter to the grid.</span></span>
1. <span data-ttu-id="6d65f-129">**フィルター タイトル** フィールドで、値を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-129">In the **Filter title** field, select a value.</span></span>
1. <span data-ttu-id="6d65f-130">**フィルター コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-130">In the **Filter code** field, enter a value.</span></span>

    <span data-ttu-id="6d65f-131">![製品フィルターを設定する](media/Product_Filters10.png "製品フィルターを設定する")</span><span class="sxs-lookup"><span data-stu-id="6d65f-131">![Setting up a product filter](media/Product_Filters10.png "Setting up a product filter")</span></span>

1. <span data-ttu-id="6d65f-132">**説明** フィールドに、コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-132">In the **Description** field, enter a name for the code.</span></span> <span data-ttu-id="6d65f-133">たとえば、*コード 2* は仕入先を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-133">For example, *Code 2* might represent vendors.</span></span> <span data-ttu-id="6d65f-134">その後、特定の仕入先または仕入先グループに対して製品フィルターを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-134">You can then create a product filter for a specific vendor or group of vendors.</span></span> <span data-ttu-id="6d65f-135">詳細については、このトピックの後半の [仕入先フィルター コードの設定](#vendor-product-filters) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d65f-135">For more information, see the [Setup vendor filter codes](#vendor-product-filters) section later in this topic.</span></span>

    <span data-ttu-id="6d65f-136">![製品フィルターのセット](media/Product_Filters.png "製品フィルターのセット")</span><span class="sxs-lookup"><span data-stu-id="6d65f-136">![Set of product filters](media/Product_Filters.png "Set of product filters")</span></span>

## <a name="set-up-product-filter-groups"></a><span data-ttu-id="6d65f-137">製品フィルター グループの設定</span><span class="sxs-lookup"><span data-stu-id="6d65f-137">Set up product filter groups</span></span>

<span data-ttu-id="6d65f-138">フィルター グループを使用して、フィルター コードをグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-138">You can use filter groups to group filter codes.</span></span> <span data-ttu-id="6d65f-139">この機能は、グループが場所のディレクティブのクエリで使用され、一連のコードではなくグループを検索する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-139">This capability is helpful when a group is used in a query in a location directive, and you want to search for the group instead of a series of codes.</span></span> <span data-ttu-id="6d65f-140">各フィルター グループは、品目グループに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-140">Each filter group is associated with an item group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d65f-141">すべての製品フィルター グループが *コード 4* より大きいフィルター コード (つまり、*コード 5* から *コード 10*) を使用できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="6d65f-141">Not all product filter groups are available for filter codes that are higher than *Code 4* (that is, *Code 5* through *Code 10*).</span></span> <span data-ttu-id="6d65f-142">たとえば、リリースされた製品に対して、すべての製品フィルター コードが追加されますが、フィルター コードのグループは更新されません。</span><span class="sxs-lookup"><span data-stu-id="6d65f-142">For example, for released products, although all the product filter codes will be added, the grouping of filter codes won't be updated.</span></span> <span data-ttu-id="6d65f-143">この動作は、今後のリリースで更新される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-143">This behavior might be updated in later releases.</span></span>

<span data-ttu-id="6d65f-144">フィルター グループを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d65f-144">To set up filter groups, follow these steps.</span></span>

1. <span data-ttu-id="6d65f-145">**倉庫管理 \> 設定 \> 製品フィルター \> 製品フィルター グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-145">Go to **Warehouse management \> Setup \> Product filters \> Product filter groups**.</span></span>
1. <span data-ttu-id="6d65f-146">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-146">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6d65f-147">**グループ 1** と **グループ 2** フィールドで、品目を分類するために使用する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-147">In the **Group 1** and **Group 2** fields, enter the names that will be used to categorize items.</span></span>
1. <span data-ttu-id="6d65f-148">**詳細** クイックタブで **新規** を選択して、明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-148">On the **Details** FastTab, select **New** to add a line.</span></span>
1. <span data-ttu-id="6d65f-149">**開始日時** フィールドおよび **終了日時** フィールドに、フィルター グループの開始日と終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-149">In the **Start date/time** and **End date/time** fields, enter start and end dates for the filter group.</span></span>
1. <span data-ttu-id="6d65f-150">**品目グループ** フィールドで、製品フィルターを適用する品目グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-150">In the **Item group** field, select the item group that the product filter should apply to.</span></span>
1. <span data-ttu-id="6d65f-151">**コード 1** から **コード 10** のフィールドで、必要に応じて、グループに含めるフィルター コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-151">In the **Code 1** through **Code 10** fields, select the filter codes to include in the group, as required.</span></span>

    <span data-ttu-id="6d65f-152">![品目グループ](media/ProdFilterGroup.png "品目グループ")</span><span class="sxs-lookup"><span data-stu-id="6d65f-152">![Item group](media/ProdFilterGroup.png "Item group")</span></span>

> [!NOTE]
> <span data-ttu-id="6d65f-153">ページを閉じる際にエラー メッセージが表示された場合は、コード設定が存在しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-153">If you receive an error message when you close the page, a code setup might be missing.</span></span> <span data-ttu-id="6d65f-154">**品目グループ** ページで、**品目グループにフィルタ コード1を割り当てる**、**品目グループにフィルタ コード 2を割り当てる** などのチェック ボックスを選択して、品目グループに対してコードを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-154">On the **Item groups** page, you can make the codes mandatory for an item group by selecting the **Assign filter code 1 for item group**, **Assign filter code 2 for item group**, and so on, check boxes.</span></span>

## <a name="set-up-filter-codes-on-item-groups"></a><span data-ttu-id="6d65f-155">品目グループでフィルター コードの設定</span><span class="sxs-lookup"><span data-stu-id="6d65f-155">Set up filter codes on item groups</span></span>

<span data-ttu-id="6d65f-156">品目グループにフィルター コードを設定して、その品目グループに関連付けられた製品に必要なコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-156">By setting up filter codes on an item group, you can make the codes that are required for products that are attached to that item group.</span></span>

<span data-ttu-id="6d65f-157">品目グループでフィルター コードを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d65f-157">To set up filter codes on item groups, follow these steps.</span></span>

1. <span data-ttu-id="6d65f-158">**在庫管理 \> 設定 \> 在庫 \> 品目グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-158">Go to **Inventory management \> Setup \> Inventory \> Item groups**.</span></span>
1. <span data-ttu-id="6d65f-159">アクション ペインで **新規** を選択し、品目グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-159">On the Action Pane, select **New** to create an item group.</span></span>
1. <span data-ttu-id="6d65f-160">**品目グループ** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-160">In the **Item group** field, enter a name.</span></span>
1. <span data-ttu-id="6d65f-161">**名前** フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-161">In the **Name** field, enter a description.</span></span>
1. <span data-ttu-id="6d65f-162">**倉庫** クイックタブの **必須フィルター** セクションで、品目グループに関連付けられている製品に指定する必要がある フィルター コードのチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-162">On the **Warehouse** FastTab, in the **Filter required** section, select the check boxes for the filter codes that must be specified for products that are associated with the item group.</span></span>

    <span data-ttu-id="6d65f-163">リリースされた製品を更新するには、**リリース済製品の詳細** ページを開き、アクション ペインで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-163">To update a released product, open its **Released product details** page, and then, on the Action Pane, select **Edit**.</span></span> <span data-ttu-id="6d65f-164">その後、コードに関連付けられたフィルターは、**倉庫** クイックタブで使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-164">The filters that are associated with codes then become available on the **Warehouse** FastTab.</span></span>

    <span data-ttu-id="6d65f-165">![品目グループ](media/ItemGroup10.png "品目グループ")</span><span class="sxs-lookup"><span data-stu-id="6d65f-165">![Item groups](media/ItemGroup10.png "Item groups")</span></span>

1. <span data-ttu-id="6d65f-166">**品目グループ フィルター** セクションで、品目の既定フィルター グループであるフィルター グループと一致する必要があるフィルターのチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-166">In the **Item group filter** section, select the check boxes for the filters that must match for the filter group to be the default filter group for an item.</span></span>

    <span data-ttu-id="6d65f-167">たとえば、**フィルター コード 1 を使用** と **フィルター コード 2 を使用** が選択された場合、フィルター グループを選択する前に、品目のフィルター コード 1 とフィルター コード 2 は両方とも品目グループ用のフィルター グループ設定に一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-167">For example, if the **Use filter code 1** and **Use filter code 2** check boxes are selected, both filter code 1 and filter code 2 of the item must match the setup of the filter group for the item group before the filter group can be selected.</span></span> <span data-ttu-id="6d65f-168">新しい品目を作成すると、選択したフィルター グループが、**リリース済製品の詳細** ページの **倉庫** クイックタブにある **グループ 1** フィールドと **グループ 2** フィールドの既定のフィルター グループになります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-168">When you create a new item, the selected filter group will be the default filter group in the **Group 1** and **Group 2** fields on the **Warehouse** FastTab of the **Released product details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d65f-169">製品フィルター コードは、高度な倉庫管理を使用する品目に対してのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-169">Product filter codes are enabled only for items that use advanced warehouse management.</span></span>

## <a name="specify-filter-codes-for-released-products"></a><span data-ttu-id="6d65f-170">リリースされた製品のフィルター コードを指定</span><span class="sxs-lookup"><span data-stu-id="6d65f-170">Specify filter codes for released products</span></span>

<span data-ttu-id="6d65f-171">リリースされた製品に対してフィルター コードを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d65f-171">Follow these steps to specify filter codes for released products.</span></span> <span data-ttu-id="6d65f-172">たとえば、フィルタ コードを使用して、特定の仕入先が購入する危険な製品をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-172">For example, you can use filter codes to group hazardous products that specific vendors purchase.</span></span>

1. <span data-ttu-id="6d65f-173">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-173">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6d65f-174">アクション ペインで **新規** を選択して、製品を作成します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-174">On the Action Pane, select **New** to create a product.</span></span>
1. <span data-ttu-id="6d65f-175">**新たにリリースされた製品** ダイアログ ボックスで、新しい製品の基準を作成するために必要なデータを入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-175">In the **New released product** dialog box, enter the data that is required to create the base of a new product, and then select **OK**.</span></span>

    <span data-ttu-id="6d65f-176">製品に関連付けられた品目グループがフィルター コードに対して構成されていないと、製品フィルター コードは使用できません。</span><span class="sxs-lookup"><span data-stu-id="6d65f-176">Product filter codes aren't enabled unless the item group that is attached to the product has been configured for filter codes.</span></span>

    <span data-ttu-id="6d65f-177">詳細については、[新しい製品の作成](../pim/tasks/create-new-product.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d65f-177">For more information, see [Create a new product](../pim/tasks/create-new-product.md).</span></span>

1. <span data-ttu-id="6d65f-178">**倉庫** クイックタブの **製品フィルター コード** セクションで、必要に応じて **コード 1** から **コード 10** までのフィールドでフィルター コードを選択して、製品のフィルター コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-178">On the **Warehouse** FastTab, in the **Product filter codes** section, select filter codes for the **Code 1** through **Code 10** fields, as required, to specify filter codes for the product.</span></span>

## <a name="set-up-generally-available-items"></a><span data-ttu-id="6d65f-179">一般に入手可能な品目の設定</span><span class="sxs-lookup"><span data-stu-id="6d65f-179">Set up generally available items</span></span>

<span data-ttu-id="6d65f-180">顧客のみ、仕入先のみ、または顧客と仕入先の両方に、特定の在庫品目を入手可能にできます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-180">You can make specific inventory items available only for customers, only for vendors, or for both customers and vendors.</span></span>

> [!NOTE]
> <span data-ttu-id="6d65f-181">顧客フィルターおよび仕入先フィルターは、一般に入手可能に設定されている品目には適用されません。</span><span class="sxs-lookup"><span data-stu-id="6d65f-181">Customer and vendor filters don't apply to any item that is set up as generally available.</span></span>

<span data-ttu-id="6d65f-182">一般に入手可能な品目を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d65f-182">To set up generally available items, follow these steps.</span></span>

1. <span data-ttu-id="6d65f-183">**倉庫管理 \> 設定 \> 製品フィルター \> 一般に入手可能な製品** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-183">Go to **Warehouse management \> Setup \> Product filters \> Generally available products**.</span></span>
1. <span data-ttu-id="6d65f-184">アクション ペインで **新規** を選択して、レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-184">On the Action Pane, select **New** to create a record.</span></span>
1. <span data-ttu-id="6d65f-185">**顧客または仕入先** フィールドで、*顧客*、*仕入先*、または *すべて* を選択して、品目を顧客、仕入先、またはその両方が利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6d65f-185">In the **Customer or vendor** field, select *Customer*, *Vendor*, or *All* to make the items available for customers, vendors, or both.</span></span>
1. <span data-ttu-id="6d65f-186">**開始日時** フィールドに、品目が使用可能になる日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-186">In the **Start date/time** field, enter the date and time when the item will become available.</span></span>
1. <span data-ttu-id="6d65f-187">**品目グループ** フィールドで、品目グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-187">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="6d65f-188">**コード 1** から **コード 10** フィールドで、フィルター コードを選択して、一般的に使用できる品目を制限します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-188">In the **Code 1** through **Code 10** fields, select the filter codes to limit the items that are generally available.</span></span>

    <span data-ttu-id="6d65f-189">品目グループを選択して、一般に入手可能にその品目グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-189">When you select an item group, you set that group of items as generally available.</span></span> <span data-ttu-id="6d65f-190">これらのフィールドでフィルター コードを選択することで、使用できる品目を制限します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-190">By selecting filter codes in these fields, you limit the items that are available.</span></span>

## <a name="set-up-customer-product-filters"></a><span data-ttu-id="6d65f-191">顧客製品フィルターの設定</span><span class="sxs-lookup"><span data-stu-id="6d65f-191">Set up customer product filters</span></span>

<span data-ttu-id="6d65f-192">このオプションの手順を使用して、**一般に入手可能な品目** ページのフィルター設定で使用可能になる品目に加えて、顧客が使用できる品目を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-192">You can use this optional procedure to specify items that should be available for a customer in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="6d65f-193">1 人の顧客に複数のフィルターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-193">You can set up multiple filters for a single customer.</span></span>

<span data-ttu-id="6d65f-194">顧客フィルター コードを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d65f-194">To set up customer filter codes, follow these steps.</span></span>

1. <span data-ttu-id="6d65f-195">**販売とマーケティング \> 顧客 \> すべての顧客** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-195">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="6d65f-196">顧客を選択する。</span><span class="sxs-lookup"><span data-stu-id="6d65f-196">Select a customer.</span></span>
1. <span data-ttu-id="6d65f-197">アクション ペインにある **顧客** タブの **設定** グループで、**製品フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-197">On the Action Pane, on the **Customer** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="6d65f-198">**製品フィルター コード** ページのアクション ペインで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-198">On the **Product filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6d65f-199">**開始日時** フィールドおよび **終了日時** フィールドに、選択した品目グループの開始日と終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-199">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="6d65f-200">**品目グループ** フィールドで、品目グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-200">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="6d65f-201">**コード 1** から **コード 10** のフィールドで、基準として使用するフィルター コードを選択し、選択した品目グループの顧客が使用できる品目を制限します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-201">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for customers in the selected item group.</span></span> <span data-ttu-id="6d65f-202">品目グループに設定されているすべてのフィルター コードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-202">You must make a selection for every filter code that is set up for the item group.</span></span>

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a><span data-ttu-id="6d65f-203">仕入先製品フィルターの設定</span><span class="sxs-lookup"><span data-stu-id="6d65f-203">Set up vendor product filters</span></span>

<span data-ttu-id="6d65f-204">このオプションの手順を使用して、**一般に入手可能な品目** ページのフィルター設定で使用可能になる品目に加えて、仕入先が使用できる品目を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-204">You can use this optional procedure to specify items that should be available for a vendor in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="6d65f-205">1 つの仕入先に複数のフィルターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-205">You can set up multiple filters for a single vendor.</span></span>

<span data-ttu-id="6d65f-206">仕入先フィルター コードを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d65f-206">To set up vendor filter codes, follow these steps.</span></span>

1. <span data-ttu-id="6d65f-207">**調達 \> 仕入先 \> すべての仕入先** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-207">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="6d65f-208">仕入先を選択してください。</span><span class="sxs-lookup"><span data-stu-id="6d65f-208">Select a vendor.</span></span>
1. <span data-ttu-id="6d65f-209">アクション ペインにある **仕入先** タブの **設定** グループで、**製品フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-209">On the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="6d65f-210">**フィルター コード** ページのアクション ペインで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-210">On the **Filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6d65f-211">**開始日時** フィールドおよび **終了日時** フィールドに、選択した品目グループの開始日と終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-211">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="6d65f-212">**品目グループ** フィールドで、品目グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-212">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="6d65f-213">**コード 1** から **コード 10** のフィールドで、基準として使用するフィルター コードを選択し、選択した品目グループの仕入先が使用できる品目を制限します。</span><span class="sxs-lookup"><span data-stu-id="6d65f-213">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for vendors in the selected item group.</span></span> <span data-ttu-id="6d65f-214">品目グループに設定されているすべてのフィルター コードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-214">You must make a selection for every filter code that is set up for the item group.</span></span>

> [!NOTE]
> <span data-ttu-id="6d65f-215">仕入先製品フィルターの設定は、関連付けられた保管分析コード グループに対して倉庫管理プロセスが有効になっているリリースされた製品に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-215">The setup of vendor product filters applies to released products where warehouse management processes are enabled for the associated storage dimension group.</span></span> <span data-ttu-id="6d65f-216">フィルター コードは、ユーザーが購買注文明細行を作成する際に、特定の仕入先から特定の品目を購入できるかどうかをシステムで決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-216">The filter codes are used to determine whether the system will allow users to purchase a given item from a given vendor when they create purchase order lines.</span></span> <span data-ttu-id="6d65f-217">Microsoft Dynamics 365 Supply Chain Management では、仕入先承認を処理する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-217">Microsoft Dynamics 365 Supply Chain Management has two methods for handling vendor approval.</span></span> <span data-ttu-id="6d65f-218">**承認済仕入先チェック メソッド** フィールドが *警告のみ* または *不許可* に設定されているリリースされた製品が 1 つ以上存在する場合、これらの品目に対して両方の仕入先承認方法を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="6d65f-218">If one or more released products exist where the **Approved vendor check method** field is set to *Warning only* or *Not allowed*, both vendor approval methods could be enabled for those items.</span></span> <span data-ttu-id="6d65f-219">この状況では、ユーザーが購買注文明細行を作成するときに問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6d65f-219">This situation might cause issues when users create purchase order lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d65f-220">参照</span><span class="sxs-lookup"><span data-stu-id="6d65f-220">See also</span></span>

[<span data-ttu-id="6d65f-221">詳細については、ブログ記事 WMS-倉庫フィルター コードを参照してください</span><span class="sxs-lookup"><span data-stu-id="6d65f-221">For more information see the blog post WMS-Warehouse Filter Codes</span></span>](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]