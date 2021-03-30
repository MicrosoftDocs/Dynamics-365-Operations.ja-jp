---
title: 作業ポリシー
description: このトピックでは、作業ポリシーを設定する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3e7814790bce0aee648421e3a69d702fd0012404
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248550"
---
# <a name="work-policies"></a><span data-ttu-id="40c62-103">作業ポリシー</span><span class="sxs-lookup"><span data-stu-id="40c62-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40c62-104">このトピックでは、作業ポリシーをサポートするようにシステムと倉庫アプリを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="40c62-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="40c62-105">この機能を使用すると、発注書または移動オーダーを受け取ったとき、または製造プロセスを完了したときに、他の必要な機能を作成することなく、すぐに在庫を登録することができます。</span><span class="sxs-lookup"><span data-stu-id="40c62-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="40c62-106">このトピックでは、一般情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="40c62-106">This topic provides general information.</span></span> <span data-ttu-id="40c62-107">ライセンス プレートの受け取りに関する詳細については、[ウェアハウス アプリを介したライセンス プレートの受け取り](warehousing-mobile-device-app-license-plate-receiving.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40c62-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="40c62-108">作業ポリシーは、製造品目が完了として報告されたとき、または倉庫アプリを使用して商品を受け取ったときに、倉庫作業を作成するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="40c62-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="40c62-109">各作業ポリシーを設定するには、作業指示タイプとプロセス、在庫場所、必要に応じて各製品の条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="40c62-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="40c62-110">たとえば、製品 *A0001* の発注書は、倉庫 *24* の場所 *RECV* で受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="40c62-111">その後、製品は、場所 *RECV* の別のプロセスで消費されます。</span><span class="sxs-lookup"><span data-stu-id="40c62-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="40c62-112">この場合は、作業者が場所 *RECV* で受け取った製品 *A0001* を報告したときに、プットアウェイ作業が作成されないようにするための作業ポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="40c62-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="40c62-113">作業ポリシーを有効にするには、**作業ポリシー** ページの **在庫場所** クイックタブで、少なくとも 1 つの場所を定義する必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="40c62-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="40c62-114">複数の作業ポリシーに同じ場所を指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="40c62-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="40c62-115">モバイル デバイス メニュー項目の **印刷ラベル** オプションは、作業を作成しなければライセンス プレートのラベルを印刷しません。</span><span class="sxs-lookup"><span data-stu-id="40c62-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="40c62-116">システムでの機能の有効化</span><span class="sxs-lookup"><span data-stu-id="40c62-116">Activate the features in your system</span></span>

<span data-ttu-id="40c62-117">このトピックで説明されている機能をシステムですべて使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で次の 2 つの機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="40c62-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="40c62-118">ライセンス プレートの入庫拡張機能</span><span class="sxs-lookup"><span data-stu-id="40c62-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="40c62-119">入庫作業の作業ポリシー拡張機能</span><span class="sxs-lookup"><span data-stu-id="40c62-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="40c62-120">作業ポリシー ページ</span><span class="sxs-lookup"><span data-stu-id="40c62-120">The Work policies page</span></span>

<span data-ttu-id="40c62-121">作業ポリシーを設定するには、**倉庫管理 \> 設定 \> 作業 \> 作業ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="40c62-122">その後、各クイックタブで、次のセクションの説明に従ってフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="40c62-123">[作業指示タイプ] クイックタブ</span><span class="sxs-lookup"><span data-stu-id="40c62-123">The Work order types FastTab</span></span>

<span data-ttu-id="40c62-124">**作業指示タイプ** クイックタブで、作業ポリシーが適用されるすべての作業指示タイプおよび関連する作業プロセスを追加します。</span><span class="sxs-lookup"><span data-stu-id="40c62-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="40c62-125">作業ポリシーでは、次の作業指示タイプと関連する作業プロセスがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="40c62-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="40c62-126">ワーク オーダー タイプ</span><span class="sxs-lookup"><span data-stu-id="40c62-126">Work order type</span></span> | <span data-ttu-id="40c62-127">作業プロセス</span><span class="sxs-lookup"><span data-stu-id="40c62-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="40c62-128">原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="40c62-128">Raw material picking</span></span>| <span data-ttu-id="40c62-129">すべての関連プロセス</span><span class="sxs-lookup"><span data-stu-id="40c62-129">All related processes</span></span> |
| <span data-ttu-id="40c62-130">連産物と副産物のプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="40c62-130">Co-product and by-product put away</span></span> | <span data-ttu-id="40c62-131">すべての関連プロセス</span><span class="sxs-lookup"><span data-stu-id="40c62-131">All related processes</span></span> |
| <span data-ttu-id="40c62-132">完成品のプットアウェイ</span><span class="sxs-lookup"><span data-stu-id="40c62-132">Finished goods putaway</span></span> | <span data-ttu-id="40c62-133">すべての関連プロセス</span><span class="sxs-lookup"><span data-stu-id="40c62-133">All related processes</span></span> |
| <span data-ttu-id="40c62-134">移動入庫</span><span class="sxs-lookup"><span data-stu-id="40c62-134">Transfer receipt</span></span> | <span data-ttu-id="40c62-135">ライセンス プレートの受け取り (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="40c62-136">発注書</span><span class="sxs-lookup"><span data-stu-id="40c62-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="40c62-137">ライセンス プレートの受け取り (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="40c62-138">積荷品目入庫 (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="40c62-139">発注書明細行受取 (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="40c62-140">発注書品目受取 (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="40c62-141">作業ポリシーが同じ作業指示タイプの複数の作業プロセスに適用されるように設定するには、作業プロセスごとに 1 行ずつグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="40c62-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="40c62-142">グリッドの各行で、**作業作成方法** フィールドを次のいずれかの値に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="40c62-143">**しない**: 作業ポリシーは、選択したワーク オーダー タイプおよび関連する作業プロセスのために作成された倉庫作業を防ぎます。</span><span class="sxs-lookup"><span data-stu-id="40c62-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="40c62-144">**クロスドッキング**: 作業ポリシーは、**クロスドッキング ポリシー名** フィールドで選択したポリシーを使用して、クロスドッキング作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="40c62-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="40c62-145">[在庫場所] クイックタブ</span><span class="sxs-lookup"><span data-stu-id="40c62-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="40c62-146">**在庫場所** クイックタブで、この作業ポリシーが適用されるすべての場所を追加します。</span><span class="sxs-lookup"><span data-stu-id="40c62-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="40c62-147">場所は作業ポリシーに関連付けられなければ、作業ポリシーはどのプロセスにも適用されません。</span><span class="sxs-lookup"><span data-stu-id="40c62-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="40c62-148">複数の作業ポリシーに同じ場所を指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="40c62-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="40c62-149">**ライセンス プレートの追跡を使用する** オプションがオフになっている場所プロファイルに割り当てられている倉庫の場所を使用できます。</span><span class="sxs-lookup"><span data-stu-id="40c62-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="40c62-150">この場合、作業者は手持在庫を直接登録します。</span><span class="sxs-lookup"><span data-stu-id="40c62-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="40c62-151">製品クイック タブ</span><span class="sxs-lookup"><span data-stu-id="40c62-151">The Products FastTab</span></span>

<span data-ttu-id="40c62-152">**製品** タブで、ポリシーを適用する製品を制御する **製品の選択** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="40c62-153">**すべて**: ポリシーをすべての製品に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="40c62-154">**選択済み**: グリッドに一覧表示されている製品にのみポリシーを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="40c62-155">製品をグリッドに追加したり、グリッドから削除したりするには、**製品** ファストタブのツールバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="40c62-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="40c62-156">既定とカスタムの "移動先" の場所</span><span class="sxs-lookup"><span data-stu-id="40c62-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="40c62-157">このセクションで説明されている機能をシステムで利用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で *ライセンス プレート受取の拡張機能* と *入荷作業の作業ポリシー機能拡張* 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="40c62-158">以前は、システムは各倉庫に対して定義されている既定の場所のみでの入荷しかサポートされていませんでした。</span><span class="sxs-lookup"><span data-stu-id="40c62-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="40c62-159">ただし、次の作業作成プロセスを使用するモバイル デバイス メニュー項目には、**既定のデータを使用する** オプションが用意されました。</span><span class="sxs-lookup"><span data-stu-id="40c62-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="40c62-160">このオプションを使用すると、カスタムの "移動先" の場所を 1 つまたは複数のメニュー項目に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="40c62-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="40c62-161">(このオプションは、その他のタイプのメニュー項目では使用可能です。)</span><span class="sxs-lookup"><span data-stu-id="40c62-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="40c62-162">ライセンス プレートの受け取り (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="40c62-163">積荷品目入庫 (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="40c62-164">発注書明細行受取 (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="40c62-165">発注書品目受取 (およびプットアウェイ)</span><span class="sxs-lookup"><span data-stu-id="40c62-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="40c62-166">メニュー項目の **移動先場所** の設定は、そのメニュー項目を使用して処理されるすべての注文について、倉庫の既定の入荷場所を上書きします。</span><span class="sxs-lookup"><span data-stu-id="40c62-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="40c62-167">カスタムの場所での入荷をサポートするためにモバイル デバイスのメニュー項目を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="40c62-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="40c62-168">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="40c62-169">このセクションで前に示した作業作成プロセスのいずれかを使用するメニュー項目を選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="40c62-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="40c62-170">**一般** クイック タブで、**既定のデータを使用する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="40c62-171">アクション ウィンドウで、**既定のデータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="40c62-172">**既定のデータ** ページで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="40c62-173">**既定のデータ フィールド:** このフィールドを *移動先* 場所に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="40c62-174">**倉庫:** このメニュー品目で使用する出荷先倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="40c62-175">**場所:** このフィールドには、選択した倉庫に対して使用可能なすべての保管場所 ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="40c62-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="40c62-176">ただし、このフィールドの設定は、実際には何も影響しません。</span><span class="sxs-lookup"><span data-stu-id="40c62-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="40c62-177">したがって、空白のままにできます。</span><span class="sxs-lookup"><span data-stu-id="40c62-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="40c62-178">ただし、リストを使用して、**ハードコードされた値** フィールドに入力する必要がある ID を確認できます。</span><span class="sxs-lookup"><span data-stu-id="40c62-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="40c62-179">**ハードコードされた値**: このメニュー項目に適用される入荷場所の場所 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="40c62-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="40c62-180">作業ポリシーは、すべての入荷場所が関連する作業ポリシー設定に記載されている場合にのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="40c62-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="40c62-181">この要件は、既定の倉庫の入庫場所を使用しているか、カスタムの "移動先" 場所を使用しているかに関係なく適用されます。</span><span class="sxs-lookup"><span data-stu-id="40c62-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="40c62-182">シナリオ例: 倉庫入荷</span><span class="sxs-lookup"><span data-stu-id="40c62-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="40c62-183">*発注書品目受取 (およびプットアウェイ)* プロセスで入荷するすべての製品は、場所 *FL-001* に登録されており、倉庫 *24* で利用可能である必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="40c62-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="40c62-184">ただし、作業を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="40c62-184">However, work should not be created.</span></span> <span data-ttu-id="40c62-185">他のプロセス (つまり、他のモバイル デバイスのメニュー項目を使用) によって入荷した製品を既定の倉庫の入荷場所 (*RECV*) に登録し、通常どおりに作業を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="40c62-186">(このシナリオでは、既定の入荷設定は表示されません)。</span><span class="sxs-lookup"><span data-stu-id="40c62-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="40c62-187">このシナリオには、次の要素が必要です。</span><span class="sxs-lookup"><span data-stu-id="40c62-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="40c62-188">すべての製品について、*FL-001* での *発注書品目受取 (およびプットアウェイ)* プロセスの作業ポリシー</span><span class="sxs-lookup"><span data-stu-id="40c62-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="40c62-189">既定のデータを持ち、**移動先場所** フィールドが *FL-001* に設定されているモバイル デバイス メニュー項目</span><span class="sxs-lookup"><span data-stu-id="40c62-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="40c62-190">必要条件</span><span class="sxs-lookup"><span data-stu-id="40c62-190">Prerequisites</span></span>

<span data-ttu-id="40c62-191">このシナリオで説明されている機能をシステムで利用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で *ライセンス プレート受取の拡張機能* と *入荷作業の作業ポリシー機能拡張* 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="40c62-192">このシナリオでは、標準のデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="40c62-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="40c62-193">したがって、ここで提供されているものを使ってシナリオを進める場合は、デモ データがインストールされているシステムで作業する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="40c62-194">また、**USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="40c62-195">作業ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="40c62-195">Set up a work policy</span></span>

1. <span data-ttu-id="40c62-196">**倉庫管理 \> 設定 \> 作業 \> 作業ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="40c62-197">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-197">Select **New**.</span></span>
1. <span data-ttu-id="40c62-198">**作業ポリシー名** フィールドに、*購買品目プットアウェイ作業なし* と入力します。</span><span class="sxs-lookup"><span data-stu-id="40c62-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="40c62-199">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-199">Select **Save**.</span></span>
1. <span data-ttu-id="40c62-200">**作業指示タイプ** クイックタブで、**追加** を選択して行をグリッドに追加し、新しい行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="40c62-201">**作業指示タイプ:** *発注書*</span><span class="sxs-lookup"><span data-stu-id="40c62-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="40c62-202">**作業プロセス:** *購買注文品目の受取 (およびプットアウェイ)*</span><span class="sxs-lookup"><span data-stu-id="40c62-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="40c62-203">**作業作成方法:** *なし*</span><span class="sxs-lookup"><span data-stu-id="40c62-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="40c62-204">**クロスドッキング ポリシー名:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="40c62-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="40c62-205">**在庫場所** クイックタブで、**追加** を選択して行をグリッドに追加し、新しい行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="40c62-206">**倉庫:** *24*</span><span class="sxs-lookup"><span data-stu-id="40c62-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="40c62-207">**場所:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="40c62-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="40c62-208">**製品** クイックタブで、**製品の選択** フィールドを *すべて* に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="40c62-209">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="40c62-210">入荷場所を変更するためのモバイル デバイスのメニュー項目の設定</span><span class="sxs-lookup"><span data-stu-id="40c62-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="40c62-211">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="40c62-212">左ウィンドウで、既存の **購買の入庫** メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="40c62-213">**一般** クイック タブで、**既定のデータを使用する** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="40c62-214">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-214">Select **Save**.</span></span>
1. <span data-ttu-id="40c62-215">アクション ウィンドウで、**既定のデータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="40c62-216">**既定のデータ** ページのアクション ペインで、**新規** を選択して行をグリッドに追加し、新しい行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="40c62-217">**既定のデータフィールド:** *移動先*</span><span class="sxs-lookup"><span data-stu-id="40c62-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="40c62-218">**倉庫:** *24*</span><span class="sxs-lookup"><span data-stu-id="40c62-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="40c62-219">**場所:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="40c62-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="40c62-220">**ハードコードされた値:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="40c62-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="40c62-221">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="40c62-222">作業を作成しないで発注書を受け取る</span><span class="sxs-lookup"><span data-stu-id="40c62-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="40c62-223">このセクションの例では、倉庫に設定されている既定の入庫場所とは異なる場所で、購買注文品目を作成するのではなく、入庫する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="40c62-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="40c62-224">この例では、このシナリオで前に作成した作業ポリシーおよびモバイル デバイス品目を使用します。</span><span class="sxs-lookup"><span data-stu-id="40c62-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="40c62-225">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="40c62-225">Create a purchase order</span></span>

1. <span data-ttu-id="40c62-226">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="40c62-227">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-227">Select **New**.</span></span>
1. <span data-ttu-id="40c62-228">**発注書の作成** ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="40c62-229">**仕入先勘定 :** *US-101*</span><span class="sxs-lookup"><span data-stu-id="40c62-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="40c62-230">**サイト:** *2*</span><span class="sxs-lookup"><span data-stu-id="40c62-230">**Site:** *2*</span></span>
    - <span data-ttu-id="40c62-231">**倉庫:** *24*</span><span class="sxs-lookup"><span data-stu-id="40c62-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="40c62-232">**OK** を選択して新しい発注書を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="40c62-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="40c62-233">**購買注文明細行** クイックタブで、空の行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="40c62-234">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="40c62-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="40c62-235">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="40c62-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="40c62-236">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-236">Select **Save**.</span></span>
1. <span data-ttu-id="40c62-237">発注書番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="40c62-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="40c62-238">発注書の受け取り</span><span class="sxs-lookup"><span data-stu-id="40c62-238">Receive a purchase order</span></span>

1. <span data-ttu-id="40c62-239">モバイル デバイスで、ユーザー ID として *24*、パスワードとして *1* を使用して、倉庫 *24* にログインします。</span><span class="sxs-lookup"><span data-stu-id="40c62-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="40c62-240">**入庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="40c62-241">**購買入庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-241">Select **Purchase receive**.</span></span> <span data-ttu-id="40c62-242">**場所** フィールドは、*FL-001* に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="40c62-243">前の手順で作成した発注書の発注書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="40c62-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="40c62-244">**品目番号** フィールドに、*A0001* と入力します。</span><span class="sxs-lookup"><span data-stu-id="40c62-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="40c62-245">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-245">Select **OK**.</span></span>
1. <span data-ttu-id="40c62-246">**数量** フィールドに *1* と入力します。</span><span class="sxs-lookup"><span data-stu-id="40c62-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="40c62-247">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-247">Select **OK**.</span></span>

<span data-ttu-id="40c62-248">これで、発注書を受け取りましたが、その発注書には作業が関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="40c62-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="40c62-249">手持在庫が更新され、品目 *A0001* の数量が *1* の場合は、場所 *FL-001* で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="40c62-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="40c62-250">シナリオ例: 製造</span><span class="sxs-lookup"><span data-stu-id="40c62-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="40c62-251">次の例では、2 つの製造オーダー、*PRD-001* と *PRD-002* があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="40c62-252">製品オーダー *PRD-001* は、製品 *SC1* が場所 *001* に完了済として報告される *組み立て* として名付けられた工程があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="40c62-253">製造オーダー *PRD-002* には、*塗装* と名付けられた、および場所 *001* から製品 *SC1* の消費の工程があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="40c62-254">製造オーダー *PRD-002* は、場所 *001* からの原材料消費 *RM1* も消費します。</span><span class="sxs-lookup"><span data-stu-id="40c62-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="40c62-255">原材料 *RM1* は、倉庫の場所 *BULK-001* に保存され、原材料のピッキングの倉庫作業によって場所 *001* がピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="40c62-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="40c62-256">ピッキング作業は、生産 *PRD-002* がリリースされるときに生成されます。</span><span class="sxs-lookup"><span data-stu-id="40c62-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="40c62-257">[![倉庫作業ポリシー](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="40c62-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="40c62-258">このシナリオの倉庫作業ポリシーをコンフィギュレーションする計画の場合、次の点を考慮する必要があります:</span><span class="sxs-lookup"><span data-stu-id="40c62-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="40c62-259">完成品のプットアウェイの倉庫作業は、製造オーダー *PRD-001* から場所 *001* に完成済として 製品 *SC1* を報告するときに必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="40c62-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="40c62-260">製造オーダー *PRD-002* の *塗装* 工程が同じ場所で製品 *SC1* を消費するためです。</span><span class="sxs-lookup"><span data-stu-id="40c62-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="40c62-261">原材料ピッキングの倉庫作業は、倉庫の場所 *BULK-001* から場所 *001* へ原材料 *RM1* を移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="40c62-262">次の例では、これらの考慮事項に基づいて、設定できる作業ポリシーについて示しています。</span><span class="sxs-lookup"><span data-stu-id="40c62-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="40c62-263">**作業ポリシー名:** *プットアウェイ機能なし*</span><span class="sxs-lookup"><span data-stu-id="40c62-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="40c62-264">**作業指示のタイプ:** *完成品のプット アウェイ* および *連産物と副産物のプット アウェイ*</span><span class="sxs-lookup"><span data-stu-id="40c62-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="40c62-265">**在庫場所:** 倉庫 *51* および場所 *001*</span><span class="sxs-lookup"><span data-stu-id="40c62-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="40c62-266">**製品:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="40c62-266">**Products:** *SC1*</span></span>

<span data-ttu-id="40c62-267">次のシナリオ例は、このシナリオの倉庫作業ポリシーを設定する方法の手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="40c62-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="40c62-268">シナリオ例: ライセンス プレートにより制御されていない場所に完了済として報告する</span><span class="sxs-lookup"><span data-stu-id="40c62-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="40c62-269">このシナリオには、ライセンス プレート制御ではない場所に完了済として製造オーダーが報告される例についても説明します。</span><span class="sxs-lookup"><span data-stu-id="40c62-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="40c62-270">このシナリオでは、標準のデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="40c62-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="40c62-271">したがって、ここで提供されているものを使ってシナリオを進める場合は、デモ データがインストールされているシステムで作業する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="40c62-272">また、**USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40c62-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="40c62-273">倉庫作業ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="40c62-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="40c62-274">倉庫のプロセスは必ずしも倉庫作業を含みません。</span><span class="sxs-lookup"><span data-stu-id="40c62-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="40c62-275">作業ポリシーを定義して、原材料のピッキングの作業の作成、および特定の場所での一連の製品に対する完成品のプットアウェイを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="40c62-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="40c62-276">**倉庫管理 \> 設定 \> 作業 \> 作業ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="40c62-277">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-277">Select **New**.</span></span>
1. <span data-ttu-id="40c62-278">**作業ポリシー名** フィールドに、*プットアウェイ作業なし* と入力します。</span><span class="sxs-lookup"><span data-stu-id="40c62-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="40c62-279">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="40c62-280">**作業指示タイプ** クイックタブで、**追加** を選択して行をグリッドに追加し、新しい行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="40c62-281">**ワーク オーダー タイプ:** *完成品のプット アウェイ*</span><span class="sxs-lookup"><span data-stu-id="40c62-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="40c62-282">**作業プロセス:** *すべての関連する作業プロセス*</span><span class="sxs-lookup"><span data-stu-id="40c62-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="40c62-283">**作業作成方法:** *なし*</span><span class="sxs-lookup"><span data-stu-id="40c62-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="40c62-284">**クロスドッキング ポリシー名:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="40c62-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="40c62-285">もう一度 **追加** を選択して 2 番目の行をグリッドに追加し、新しい行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="40c62-286">**ワーク オーダー タイプ:** *連産物と副産物のプット アウェイ*</span><span class="sxs-lookup"><span data-stu-id="40c62-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="40c62-287">**作業プロセス:** *すべての関連する作業プロセス*</span><span class="sxs-lookup"><span data-stu-id="40c62-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="40c62-288">**作業作成方法:** *なし*</span><span class="sxs-lookup"><span data-stu-id="40c62-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="40c62-289">**クロスドッキング ポリシー名:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="40c62-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="40c62-290">**在庫場所** クイックタブで、**追加** を選択して行をグリッドに追加し、新しい行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="40c62-291">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="40c62-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="40c62-292">**保管場所:** *001*</span><span class="sxs-lookup"><span data-stu-id="40c62-292">**Location:** *001*</span></span>

1. <span data-ttu-id="40c62-293">**製品** クイックタブで、**製品の選択** フィールドを *選択済み* に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="40c62-294">**製品** クイックタブで、**追加** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="40c62-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="40c62-295">新しい行で、**品目番号** フィールドを *L0101* に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="40c62-296">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="40c62-297">出荷場所の設定</span><span class="sxs-lookup"><span data-stu-id="40c62-297">Set up an output location</span></span>

1. <span data-ttu-id="40c62-298">**組織管理 \> リソース \> リソース グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="40c62-299">左のウィンドウで、リソース グループ **5102** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="40c62-300">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="40c62-301">**出荷倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="40c62-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="40c62-302">**出荷場所:** *001*</span><span class="sxs-lookup"><span data-stu-id="40c62-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="40c62-303">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="40c62-304">場所 *001* はライセンス プレートにより制御される場所ではありません。</span><span class="sxs-lookup"><span data-stu-id="40c62-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="40c62-305">場所に適用できる作業ポリシーが存在する場合にのみ、ライセンス プレート制御でない出荷場所を設定できます。</span><span class="sxs-lookup"><span data-stu-id="40c62-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="40c62-306">製造オーダーを作成して完了として報告</span><span class="sxs-lookup"><span data-stu-id="40c62-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="40c62-307">**生産管理 \> 製造オーダー \> すべての製造オーダー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="40c62-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="40c62-308">アクション ウィンドウで、**新しい製造オーダー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40c62-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="40c62-309">**製造オーダーの作成** ダイアログ ボックスで、**品目番号** フィールドを *L0101* に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="40c62-310">**作成** を選択して注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="40c62-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="40c62-311">新しい製造オーダーが **すべての製造オーダー** ページのグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="40c62-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="40c62-312">新しい製造オーダーを選択したままにします。</span><span class="sxs-lookup"><span data-stu-id="40c62-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="40c62-313">アクション ペインの、**製造オーダー** タブの、**プロセス** グループで、**見積** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="40c62-314">**見積** ダイアログ ボックスで、見積を読み、**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="40c62-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="40c62-315">アクション ペインの、**製造オーダー** タブの、**プロセス** グループで、**開始** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="40c62-316">**開始** ダイアログ ボックスの **全般** タブで、**自動 BOM 消費** フィールドを *なし* に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="40c62-317">**OK** を選択して設定を保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="40c62-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="40c62-318">[アクション ペイン] の、**製造オーダー** タブで、**プロセス** グループから、**完了レポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40c62-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="40c62-319">**完了レポート** ダイアログ ボックスの **全般** タブで、**エラー適用** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="40c62-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="40c62-320">**OK** を選択して設定を保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="40c62-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="40c62-321">アクション ウィンドウの **倉庫** タブの、**一般** グループで、**作業詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="40c62-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="40c62-322">製造オーダーが完了と報告されたときに、作業はプットアウェイに生成されませんでした。</span><span class="sxs-lookup"><span data-stu-id="40c62-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="40c62-323">この現象は、製品 *L0101* が場所 *001* に完了として報告されるときに作業が生成されないように作業ポリシーを定義しているために発生します。</span><span class="sxs-lookup"><span data-stu-id="40c62-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="40c62-324">詳細</span><span class="sxs-lookup"><span data-stu-id="40c62-324">More information</span></span>

<span data-ttu-id="40c62-325">モバイル デバイス メニュー項目の詳細については、[倉庫作業用のモバイル デバイスの設定](configure-mobile-devices-warehouse.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40c62-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="40c62-326">ライセンス プレートの受け取りと作業ポリシーに関する詳細については、[ウェアハウス アプリを介したライセンス プレートの受け取り](warehousing-mobile-device-app-license-plate-receiving.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40c62-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="40c62-327">入庫積荷管理に関する詳細情報については、[発注書に対する入庫積荷の倉庫処理](inbound-load-handling.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40c62-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]