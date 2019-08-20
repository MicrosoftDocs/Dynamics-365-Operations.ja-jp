---
title: 機能的な場所を作成する
description: このトピックでは、資産管理で機能的な場所を作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d1f9714f57d19a13444fea9864d72c3341b15ea
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783408"
---
# <a name="create-functional-locations"></a><span data-ttu-id="77be9-103">機能的な場所を作成する</span><span class="sxs-lookup"><span data-stu-id="77be9-103">Create functional locations</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="77be9-104">このトピックでは、資産管理で機能的な場所を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="77be9-104">This topic explains how to create a functional location in Asset Management.</span></span>

<span data-ttu-id="77be9-105">機能的な場所の構造を作成する場合、一度機能的な場所を作成すると、元の場所から移動できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="77be9-105">When you create a functional location structure, be aware once you have created a functional location, you cannot move it from the original location.</span></span> <span data-ttu-id="77be9-106">つまり、資産管理で機能的な場所の作成を開始する前に、機能的な場所の構造を慎重に検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77be9-106">This means that you should carefully consider the structure of your functional locations before you start creating them in Asset Management.</span></span> <span data-ttu-id="77be9-107">機能的な場所を後悔している場合、まだ使用されていない場合は削除できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-107">If you regret a functional location, you can delete it, provided that it has not yet been taken into use.</span></span>

<span data-ttu-id="77be9-108">機能的な場所を操作できるようにするには、まず機能的な場所の 2 つの "カテゴリ" を作成します。</span><span class="sxs-lookup"><span data-stu-id="77be9-108">To be able to work with functional locations, you start by creating two "categories" of functional locations:</span></span>

- <span data-ttu-id="77be9-109">サブ場所ではない *1 つ*の既定の機能的な場所を作成します。</span><span class="sxs-lookup"><span data-stu-id="77be9-109">Create *one* default functional location with not sub locations.</span></span> <span data-ttu-id="77be9-110">この機能的な場所は、新しい資産を作成するときに資産に対する標準の場所としてのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-110">This functional location is used only as the standard location for assets when you create new assets.</span></span>  
- <span data-ttu-id="77be9-111">会社のメンテナンス ジョブの管理に必要な機能的な場所の構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="77be9-111">Create the functional location structures required for managing maintenance jobs in your company.</span></span>

## <a name="create-a-default-functional-location"></a><span data-ttu-id="77be9-112">既定の機能的な場所を作成する</span><span class="sxs-lookup"><span data-stu-id="77be9-112">Create a default functional location</span></span>

<span data-ttu-id="77be9-113">機能する的な場所を使用する場合は、まず新しい資産の作成時に使用する既定の場所を 1 つ作成します。</span><span class="sxs-lookup"><span data-stu-id="77be9-113">When you use functional locations, start by creating one default location to be used when you create new assets.</span></span> <span data-ttu-id="77be9-114">この機能的な場所は、**資産管理** > **設定** > **資産管理パラメーター** > **資産** リンク > **既定の機能的な場所**フィールドで選択したものです。</span><span class="sxs-lookup"><span data-stu-id="77be9-114">This functional location is the one you select in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Default functional location** field.</span></span> <span data-ttu-id="77be9-115">既定の機能的な場所は、新しい資産を作成するときに使用できますが、それらの資産に対する機能的な場所の構造がまだ設定されていません。</span><span class="sxs-lookup"><span data-stu-id="77be9-115">The default functional location can be used when you create new assets, and you have not yet set up a functional location structure for those assets.</span></span>

1. <span data-ttu-id="77be9-116">**資産管理** > **共通** > **機能的な場所** > **すべての機能的な場所**を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-116">Select **Asset management** > **Common** > **Functional locations** > **All Functional locations**.</span></span>  
2. <span data-ttu-id="77be9-117">**すべての機能的な場所**で、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-117">In **All functional locations**, select **New**.</span></span>
3. <span data-ttu-id="77be9-118">**機能的な場所**フィールドに "0000" や "既定" などの ID を挿入し、これが特別な機能的な場所であることを示します。</span><span class="sxs-lookup"><span data-stu-id="77be9-118">Insert an ID in the **Functional location** field, for example, "0000" or "Default", to indicate that this is a special functional location.</span></span>
4. <span data-ttu-id="77be9-119">**名前**フィールドに、既定の機能的な場所の名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="77be9-119">Insert name for the default functional location in the **Name** field.</span></span>
5. <span data-ttu-id="77be9-120">**親**フィールドで親を選択*しない*でください – フィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="77be9-120">Do *not* select a parent in the **Parent** field – leave this field blank.</span></span>
6. <span data-ttu-id="77be9-121">**機能的な場所タイプ** フィールドで、既定の機能的な場所に使用する機能的な場所タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-121">In the **Functional location type** field, select the functional location type to be used for the default functional location.</span></span> <span data-ttu-id="77be9-122">機能的な場所タイプの設定方法の詳細については、[機能的な場所タイプ](../setup-for-functional-locations/functional-location-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77be9-122">See [Functional location types](../setup-for-functional-locations/functional-location-types.md) for more information on how to set up functional location types.</span></span>
7. <span data-ttu-id="77be9-123">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-123">Select **OK**.</span></span> <span data-ttu-id="77be9-124">この機能的な場所は、会社が使用する機能的な場所に資産をインストールするまで新しい資産の一時的な場所としてのみ使用されるため、ここにデータを追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="77be9-124">You should not add further data to this functional location as it is only used as a temporary location for new assets until you install the assets on the functional locations used by your company.</span></span>

## <a name="create-functional-locations"></a><span data-ttu-id="77be9-125">機能的な場所を作成する</span><span class="sxs-lookup"><span data-stu-id="77be9-125">Create functional locations</span></span>

<span data-ttu-id="77be9-126">次の手順では、会社のメンテナンス管理に必要な機能的な場所を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="77be9-126">The following procedure describes how you create the functional locations required for maintenance management in your company.</span></span>

1. <span data-ttu-id="77be9-127">**資産管理** > **共通** > **機能的な場所** > **すべての機能的な場所**を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-127">Select **Asset management** > **Common** > **Functional locations** > **All Functional locations**.</span></span> <span data-ttu-id="77be9-128">グリッド ビューまたは詳細ビューから機能的な場所を作成できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-128">You can create a functional location from grid view or details view.</span></span>
2. <span data-ttu-id="77be9-129">**新規**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-129">Select the **New** button.</span></span>
3. <span data-ttu-id="77be9-130">**機能的な場所**フィールドに ID を挿入します。</span><span class="sxs-lookup"><span data-stu-id="77be9-130">Insert an ID in the **Functional location** field.</span></span>
4. <span data-ttu-id="77be9-131">**名前**フィールドに、機能的な場所の名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="77be9-131">Insert a name for the functional location in the **Name** field.</span></span>
5. <span data-ttu-id="77be9-132">機能的な場所が構造内のサブ場所である場合は、**親**フィールドの親場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-132">If the functional location is a sub location in a structure, select the parent location in the **Parent** field.</span></span>
6. <span data-ttu-id="77be9-133">**機能的な場所タイプ** フィールドでタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-133">Select a type in the **Functional location type** field.</span></span>
7. <span data-ttu-id="77be9-134">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-134">Select **OK**.</span></span>
8. <span data-ttu-id="77be9-135">機能的な場所を選択し、**編集**ボタンをクリックして詳細情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="77be9-135">Select the functional location and click the **Edit** button to add further information.</span></span>

>[!NOTE]
><span data-ttu-id="77be9-136">機能的な場所のライフサイクル状態の設定によっては、機能的な場所に対するすべてのサブ場所を作成し、資産のインストールを開始する前に機能的な場所のライフサイクル状態を変更することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="77be9-136">Depending on your setup of functional location lifecycle states, you may have to create all sub locations for a functional location, and then change the functional location lifecycle state before you can start installing assets.</span></span> <span data-ttu-id="77be9-137">資産インストールの詳細については、[機能の場所への資産のインストール](../functional-locations/install-objects-on-functional-locations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77be9-137">See [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md) for more information on asset installation.</span></span> <span data-ttu-id="77be9-138">機能的な場所のライフサイクル状態の設定の詳細については、[機能的な場所のライフサイクル状態](../setup-for-functional-locations/functional-location-stages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77be9-138">See [Functional location lifecycle states](../setup-for-functional-locations/functional-location-stages.md) to learn more about setup of functional location lifecycle states.</span></span>

<span data-ttu-id="77be9-139">詳細ビューには、機能的な場所に関する情報を追加および編集できるクイック タブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-139">In Details view, you will see FastTabs on which you can add and edit information about the functional location.</span></span>

## <a name="general-information"></a><span data-ttu-id="77be9-140">一般情報</span><span class="sxs-lookup"><span data-stu-id="77be9-140">General Information</span></span>

<span data-ttu-id="77be9-141">このセクションでは、機能的な場所の構造での親情報および子情報の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="77be9-141">This section provides an overview of parent and child information in the functional location structure.</span></span> <span data-ttu-id="77be9-142">**詳細**セクションでは、機能的な場所に関連する資産属性、メンテナンス計画、および資産の数を確認できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-142">In the **Details** section, you can see the number of asset attributes, maintenance plans, and assets related to the functional location.</span></span> <span data-ttu-id="77be9-143">**在庫**セクションでは、機能的な場所に関連するサイトおよび倉庫を選択できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-143">In the **Inventory** section, you can select the site and warehouse to which the functional location is related.</span></span> <span data-ttu-id="77be9-144">サイトおよび倉庫は、ワーク オーダー品目予測に関連して使用されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-144">Site and warehouse is used in connection with work order item forecasts.</span></span> <span data-ttu-id="77be9-145">品目予測を作成すると、資産の機能的な場所からサイトおよび倉庫情報が自動的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-145">When creating an item forecast, site and warehouse information from the functional location of the asset is automatically used.</span></span> <span data-ttu-id="77be9-146">**ライフサイクル状態**セクションでは、機能的な場所のライフサイクル状態に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-146">In the **Lifecycle state** section, information about the functional location lifecycle state is displayed.</span></span>

## <a name="installed-assets"></a><span data-ttu-id="77be9-147">インストール済資産</span><span class="sxs-lookup"><span data-stu-id="77be9-147">Installed assets</span></span>

<span data-ttu-id="77be9-148">資産インストールの詳細については、[機能の場所への資産のインストール](../functional-locations/install-objects-on-functional-locations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77be9-148">Refer to [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md) for more information on asset installation.</span></span> <span data-ttu-id="77be9-149">このクイック タブの**表示**ボタンを使用して、クイック タブにより多くのフィールドを表示できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-149">You can use the **View** button on this FastTab to show more fields on the FastTab.</span></span> <span data-ttu-id="77be9-150">**発効日**および**サブ資産**フィールドをグリッドに表示できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-150">The **Valid from** and **Sub asset** fields can be shown in the grid.</span></span>

## <a name="asset-attribute-requirements"></a><span data-ttu-id="77be9-151">資産属性の要件</span><span class="sxs-lookup"><span data-stu-id="77be9-151">Asset attribute requirements</span></span>

<span data-ttu-id="77be9-152">このクイック タブでは、機能的な場所にインストールする資産の特定の属性要件を追加できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-152">On this FastTab you can add specific attribute requirements for the assets that you install on the functional location.</span></span> <span data-ttu-id="77be9-153">これらの要件は、情報提供のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="77be9-153">These requirements are for information purposes only.</span></span> <span data-ttu-id="77be9-154">他の属性要件を持つ資産をインストールするのを妨げるものではありません。</span><span class="sxs-lookup"><span data-stu-id="77be9-154">They do not prevent you from installing assets with other attribute requirements.</span></span> <span data-ttu-id="77be9-155">**明細行の追加**を選択して、属性タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-155">Select **Add line** and select the attribute type.</span></span> <span data-ttu-id="77be9-156">次に、該当する**値**を挿入し、**しきい値基準**フィールドでしきい値を選択し、レコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="77be9-156">Then you insert the relevant **Value**, select a threshold in the **Threshold criteria** field and save the record.</span></span>

## <a name="maintenance-plans-and-maintenance-rounds"></a><span data-ttu-id="77be9-157">メンテナンス計画およびメンテナンス ラウンド</span><span class="sxs-lookup"><span data-stu-id="77be9-157">Maintenance plans and Maintenance rounds</span></span>

<span data-ttu-id="77be9-158">ここでは、開始日を含むメンテナンス計画とメンテナンス ラウンドを機能的な場所に追加できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-158">Here you can add maintenance plans and maintenance rounds to the functional location, including a start date.</span></span> <span data-ttu-id="77be9-159">機能的な場所にインストールされている資産には、他のメンテナンス計画が設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="77be9-159">The assets installed on a functional location may have other maintenance plans set up.</span></span> <span data-ttu-id="77be9-160">すべてのメンテナンス計画およびメンテナンス ラウンドは、機能的な場所および現在インストールされている資産の資産カレンダー エントリのスケジューリングに使用できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-160">All maintenance plans and maintenance rounds can be used for scheduling asset calendar entries for a functional location and its currently installed assets.</span></span>

>[!NOTE]
><span data-ttu-id="77be9-161">**すべての機能的な場所**詳細ビュー > **メンテナンス計画**クイック タブで、メンテナンス計画の資産タイプ、資産ブランド、資産モデルの設定の更新をする場合、メンテナンス計画をスケジューリングした後、機能的な場所に関連する既存のメンテナンス スケジュール エントリは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-161">If you update the setup of asset types, asset brands, and asset models on maintenance plans in **All functional locations** detail view > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="77be9-162">機能的な場所の更新されたメンテナンス計画設定に対応する新しいスケジュール エントリを作成するには、その機能的な場所に対する新しいメンテナンス計画スケジュールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77be9-162">In order to create new schedule entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> 

## <a name="address"></a><span data-ttu-id="77be9-163">住所</span><span class="sxs-lookup"><span data-stu-id="77be9-163">Address</span></span>

<span data-ttu-id="77be9-164">**アドレス** クイック タブに、機能的な場所アドレスを挿入します。</span><span class="sxs-lookup"><span data-stu-id="77be9-164">Insert the functional location address on the **Address** FastTab.</span></span> <span data-ttu-id="77be9-165">機能的な場所のアドレスは継承されます。つまりサブ場所にアドレスが定義されていない場合は、親場所のアドレスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-165">Addresses on functional locations are inherited, meaning if a sub location has no address defined, the address of the parent location is used.</span></span>

## <a name="workers"></a><span data-ttu-id="77be9-166">作業者</span><span class="sxs-lookup"><span data-stu-id="77be9-166">Workers</span></span>

<span data-ttu-id="77be9-167">このクイック タブでは、機能的な場所に所属する作業者を追加し、作業者の基本として機能的な場所を選択できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-167">On this FastTab, you can add workers affiliated with the functional location, and you can select a functional location as primary for the worker.</span></span> 

## <a name="attributes"></a><span data-ttu-id="77be9-168">属性</span><span class="sxs-lookup"><span data-stu-id="77be9-168">Attributes</span></span>

<span data-ttu-id="77be9-169">このクイック タブでは、機能的な場所属性の値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-169">On this FastTab, you can set values for functional location attributes.</span></span> <span data-ttu-id="77be9-170">これらの属性を使用して、構造プロパティ、建物タイプ、エリアの説明、地上または地下の場所など、機能的な場所に関連するプロパティまたは特性を記述できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-170">These attributes can be used to describe properties or characteristics pertinent to the functional location, for example, structural properties, building type, area descriptions, or location above or under ground.</span></span>

<span data-ttu-id="77be9-171">**明細行の追加**を選択して、属性タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-171">Select **Add line** and select the attribute type.</span></span> <span data-ttu-id="77be9-172">次に、属性タイプに関連付けられている**値**を挿入し、レコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="77be9-172">Next, insert the **Value** related to the attribute type and save the record.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="77be9-173">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="77be9-173">Financial dimensions</span></span>

<span data-ttu-id="77be9-174">機能的な場所の財務分析コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-174">You can select financial dimensions for the functional location.</span></span> <span data-ttu-id="77be9-175">[機能的な場所タイプ](../setup-for-functional-locations/functional-location-types.md) は、機能的な場所からの財務分析コードを自動的に更新できるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-175">[Functional location types](../setup-for-functional-locations/functional-location-types.md) can be set up to allow for automatic update of financial dimensions from a functional location.</span></span> <span data-ttu-id="77be9-176">つまり、財務分析コードにインストールされた資産は、機能的な場所の財務分析コードを自動的に取得します。</span><span class="sxs-lookup"><span data-stu-id="77be9-176">This means that assets installed on a financial dimension automatically get the financial dimensions for the functional location.</span></span> <span data-ttu-id="77be9-177">これは、場所に応じて異なるコスト センターが必要な場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="77be9-177">This is useful if you want different cost centers, depending on locations.</span></span>

<span data-ttu-id="77be9-178">**サイト**、**倉庫**、**アドレス**、および**財務分析コード**に関するデータが親機能的な場所で更新されると、更新中に行われるその選択に応じて、サブ機能的な場所が更新されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-178">When data regarding **Site**, **Warehouse**, **Address**, and **Financial dimensions** are updated on a parent functional location, the related sub functional locations can be updated accordingly if you make that selection during the update.</span></span> <span data-ttu-id="77be9-179">ダイアログが開き、更新オプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-179">A dialog opens, providing you with the update options.</span></span>

## <a name="copy-a-functional-location-structure"></a><span data-ttu-id="77be9-180">機能的な場所の構造をコピーする</span><span class="sxs-lookup"><span data-stu-id="77be9-180">Copy a functional location structure</span></span>

<span data-ttu-id="77be9-181">会社に類似した場所構造を持つ複数の機能的な場所がある場合、資産管理のコピー機能を使用して、類似した複数の場所階層をすばやく作成できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-181">If your company has several functional locations with similar location structures, you can use the copy function in Asset Management to quickly create a number of similar location hierarchies.</span></span> <span data-ttu-id="77be9-182">特定の機能的な場所または構造全体をコピーすると、新しい場所または構造はコピーした名前と同じ名前になります。</span><span class="sxs-lookup"><span data-stu-id="77be9-182">When you copy a specific functional location or an entire structure, the new location or structure has the same name as the one you copied.</span></span> <span data-ttu-id="77be9-183">コピー手順の完了後、新しい機能的な場所に対して選択した機能的な場所のライフサイクル状態で許可されている場合、新しい機能的な場所の名前または他の設定を簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-183">After the copy procedure is done, you can easily change the name or other settings on the new functional location, provided that the functional location lifecycle state selected for the new functional location allows it.</span></span>

1. <span data-ttu-id="77be9-184">**すべての機能的な場所**で、コピーする機能的な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-184">In **All functional locations**, select the functional location you want to copy.</span></span> <span data-ttu-id="77be9-185">たとえば、サブ場所を含む機能的な場所の構造全体をコピーする場合は、一番上の場所 (親) を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-185">For example, you select a top location (parent) if you want to copy the entire functional location structure including sub locations.</span></span>
2. <span data-ttu-id="77be9-186">**機能的な場所の構造をコピーする**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-186">Select the **Copy functional location structure** button.</span></span> <span data-ttu-id="77be9-187">リスト ページで選択した場所が、**コピー元**フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-187">The location you selected in the list page is shown in the **Copy from** field.</span></span>
3. <span data-ttu-id="77be9-188">**新しい機能的な場所**フィールドに新しい場所の名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="77be9-188">Insert the name of the new location in the **New functional location** field.</span></span>
4. <span data-ttu-id="77be9-189">**親で貼り付け**フィールドでは、作成する場所が既存の機能的な場所構造の一部である必要がある場合にのみ、親 ID を挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77be9-189">In the **Parent to paste under** field, you should only insert a parent ID if the location you are creating should be part of an existing functional location structure.</span></span>
5. <span data-ttu-id="77be9-190">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77be9-190">Click **OK**.</span></span> <span data-ttu-id="77be9-191">新しい機能的な場所構造は、**すべての機能的な場所**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-191">The new functional location structure is shown in **All functional locations**.</span></span>

>[!NOTE]
><span data-ttu-id="77be9-192">機能的な場所構造をコピーすると、新しい構造での機能的な場所のライフサイクル状態は、機能的な場所用に作成した "最初の状態" に設定されます。</span><span class="sxs-lookup"><span data-stu-id="77be9-192">When you copy a functional location structure, functional location lifecycle states in the new structure are set to the "first state" that you have created for functional locations.</span></span> <span data-ttu-id="77be9-193">**すべての機能的な場所**で**名前変更**および**削除**ボタンを使用して、機能的な場所の名前変更または削除ができるかどうかは、機能的な場所の現在のライフサイクル状態によって異なります。</span><span class="sxs-lookup"><span data-stu-id="77be9-193">Whether you can rename or delete a functional location using the **Rename** and **Delete** buttons in **All functional locations**, depends on the current lifecycle state of the functional location.</span></span>

## <a name="delete-a-functional-location"></a><span data-ttu-id="77be9-194">機能的な場所の削除</span><span class="sxs-lookup"><span data-stu-id="77be9-194">Delete a Functional Location</span></span>

<span data-ttu-id="77be9-195">削除しようとしている機能的な場所のいずれかに資産がインストールされていない場合、および現在の機能的な場所のライフサイクル状態が許可している場合は、関連するサブ場所を持つ機能的な場所を削除できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-195">A functional location with related sub locations can be deleted if no assets have been installed on any of the functional locations you are trying to delete, and if the current functional location lifecycle state allows it.</span></span>

1. <span data-ttu-id="77be9-196">**すべての機能的な場所**で、削除する機能的な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-196">In **All functional locations**, select the functional location you want to delete.</span></span>
2. <span data-ttu-id="77be9-197">必要に応じて、機能的な場所を、機能的な場所の削除を許可する機能的な場所のライフサイクル状態に更新します。</span><span class="sxs-lookup"><span data-stu-id="77be9-197">If required, update the functional location to a functional location lifecycle state that allows deletion of a functional location.</span></span>
3. <span data-ttu-id="77be9-198">**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="77be9-198">Select **Delete**.</span></span>

>[!NOTE]
><span data-ttu-id="77be9-199">機能的な場所を削除できない場合は、代わりに、この目的用に機能的な場所のライフサイクル状態を設定して削除を処理できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-199">If you cannot delete a functional location, instead you can handle deletion by setting up a functional location lifecycle state for this purpose.</span></span> <span data-ttu-id="77be9-200">たとえば、**機能的な場所のライフサイクル状態**フォームで、有効な状態であってはならない "仕損済" または "削除済" 状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="77be9-200">For example, you can set up a "Scrapped" or "Deleted" stage, which should not be an active stage, in the **Functional location lifecycle states** form.</span></span>
