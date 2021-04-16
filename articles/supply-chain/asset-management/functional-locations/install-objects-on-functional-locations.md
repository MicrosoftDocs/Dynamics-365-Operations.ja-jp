---
title: 機能的な場所に資産を導入する
description: このトピックでは、資産管理で機能的な場所に資産を導入する方法について説明します。
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 818c7eb86851047fa333fd4df11c8c7534c2a06b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839706"
---
# <a name="install-assets-on-functional-locations"></a><span data-ttu-id="881ea-103">機能的な場所に資産を導入する</span><span class="sxs-lookup"><span data-stu-id="881ea-103">Install assets on functional locations</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="881ea-104">機能的な場所の構造を作成したら、次の手順で、関連する機能的な場所に資産を導入します。</span><span class="sxs-lookup"><span data-stu-id="881ea-104">After you've created functional location structures, the next step is to install assets on the relevant functional locations.</span></span> <span data-ttu-id="881ea-105">このトピックでは、資産管理でそれらの機能的な場所に資産を導入する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="881ea-105">This topic explains how to install assets on those functional locations in Asset Management.</span></span> <span data-ttu-id="881ea-106">資産の作成方法については、[資産の概要](../objects/introduction-to-objects.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="881ea-106">For information about how to create assets, see [Introduction to assets](../objects/introduction-to-objects.md).</span></span>

<span data-ttu-id="881ea-107">資産構造を作成した場合は、資産構造全体を機能的な場所に導入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="881ea-107">If you've created an asset structure, the whole asset structure must be installed on a functional location.</span></span> <span data-ttu-id="881ea-108">したがって、機能的な場所で選択できるのは、親資産 (親資産を持たない上位レベルの資産) のみです。</span><span class="sxs-lookup"><span data-stu-id="881ea-108">Therefore, only parent assets (top-level assets that have no parent asset) can be selected on a functional location.</span></span> <span data-ttu-id="881ea-109">関連するすべての子資産 (下位資産) も、機能的な場所に導入されます。</span><span class="sxs-lookup"><span data-stu-id="881ea-109">All related child assets (sub-assets) will also be installed on the functional location.</span></span> <span data-ttu-id="881ea-110">機能的な場所に資産を導入すると、機能的な場所に対して選択された機能的な場所タイプの設定に応じて、機能的な場所の財務分析コードが自動的に転送される場合があります。</span><span class="sxs-lookup"><span data-stu-id="881ea-110">When you install assets on a functional location, the financial dimensions of the functional location might be automatically transferred to them, depending on the setup on the functional location type that is selected for the functional location.</span></span> <span data-ttu-id="881ea-111">機能的な場所タイプの設定方法の詳細については、[機能的な場所のタイプ](../setup-for-functional-locations/functional-location-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="881ea-111">For more information about how to set up functional location types, see [Functional location types](../setup-for-functional-locations/functional-location-types.md).</span></span>

> [!NOTE]
> <span data-ttu-id="881ea-112">機能的な場所に使用される機能的な場所タイプに資産タイプを設定できます。</span><span class="sxs-lookup"><span data-stu-id="881ea-112">You can set up asset types on the functional location type that is used for a functional location.</span></span> <span data-ttu-id="881ea-113">この場合、機能的な場所に資産を導入すると、同じ資産タイプを持つ親資産のみが、機能的な場所に導入できる資産のリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="881ea-113">In this case, when you install assets on the functional location, only parent assets that have the same asset type are shown in the list of assets that can be installed on the functional location.</span></span>

<span data-ttu-id="881ea-114">機能的な場所に資産を導入した後、必要に応じて親資産または資産構造を置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="881ea-114">After you've installed assets on a functional location, you can replace a parent asset or an asset structure as you require.</span></span> <span data-ttu-id="881ea-115">資産を導入するときと同様に、置換する親資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-115">As when you install assets, you select a parent asset to replace.</span></span> <span data-ttu-id="881ea-116">関連するすべての子資産も置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="881ea-116">All related child assets will also be replaced.</span></span> 


## <a name="install-an-asset-structure-on-a-functional-location"></a><span data-ttu-id="881ea-117">機能的な場所に資産構造を導入する</span><span class="sxs-lookup"><span data-stu-id="881ea-117">Install an asset structure on a functional location</span></span>

1. <span data-ttu-id="881ea-118">**資産管理**\>**共通**\>**機能的な場所**\>**すべての機能的な場所** または **有効な機能的な場所** を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-118">Select **Asset management** \> **Common** \> **Functional locations** \> **All Functional locations** or **Active functional locations**.</span></span>
2. <span data-ttu-id="881ea-119">資産を導入する機能的な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-119">Select the functional location to install an asset on.</span></span>
3. <span data-ttu-id="881ea-120">**資産導入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-120">Select **Install asset**.</span></span>

    <span data-ttu-id="881ea-121">**属性** セクションには、機能的な場所に対して選択された機能的な場所タイプに設定されている資産属性要件のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="881ea-121">The **Attributes** section shows a list of the asset attribute requirements that are set up on the functional location type that is selected for the functional location.</span></span> <span data-ttu-id="881ea-122">属性は情報提供のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="881ea-122">The attributes are for informational purposes only.</span></span> <span data-ttu-id="881ea-123">システムは、導入する資産に設定されている資産属性に対して属性を検証しません。</span><span class="sxs-lookup"><span data-stu-id="881ea-123">The system doesn't validate the attributes against the asset attributes that are set up on the asset that you're installing.</span></span> <span data-ttu-id="881ea-124">**資産** フィールドで資産を選択した後、その検証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="881ea-124">You must do that validation after you select an asset in the **Asset** field.</span></span>

4. <span data-ttu-id="881ea-125">**資産** フィールドで、導入する親資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-125">In the **Asset** field, select the parent asset to install.</span></span> <span data-ttu-id="881ea-126">関連するすべての子資産が自動的に導入に含まれます。</span><span class="sxs-lookup"><span data-stu-id="881ea-126">All related child assets are automatically included in the installation.</span></span>

    <span data-ttu-id="881ea-127">資産リストの右側にある **資産属性** セクションには、選択した資産に関連する資産属性が表示されます。</span><span class="sxs-lookup"><span data-stu-id="881ea-127">The **Asset attributes** section to the right of the asset list shows the asset attributes that are related to the selected asset.</span></span>

5. <span data-ttu-id="881ea-128">**有効** フィールドで、資産の導入が有効になる日時を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-128">In the **Effective** field, select the date and time that the asset installation is valid from.</span></span> <span data-ttu-id="881ea-129">その日時以降、資産および関連する下位資産の原価は、機能的な場所に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="881ea-129">After that date and time, costs for the asset and related sub-assets will be related to the functional location.</span></span>

    > [!NOTE]
    > <span data-ttu-id="881ea-130">資産に設定された資産属性が、**属性** セクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="881ea-130">The asset attributes that are set up on the asset are added to the **Attributes** section.</span></span> <span data-ttu-id="881ea-131">たとえば、資産と機能的な場所両方の要件として、**重量** 属性要件が追加されました。</span><span class="sxs-lookup"><span data-stu-id="881ea-131">For example, the **Weight** attribute requirement has been added as a requirement on both the asset and the functional location.</span></span> <span data-ttu-id="881ea-132">資産に機能的な場所と同じタイプの属性要件がある場合、資産の属性要件の値が **値** フィールドに入力されます。</span><span class="sxs-lookup"><span data-stu-id="881ea-132">If the asset has attribute requirements of the same type as the functional location, the values of the asset's attribute requirements are entered in the **Value** fields.</span></span> <span data-ttu-id="881ea-133">したがって、機能的な場所に設定されている属性要件に対して資産価値を検証することができます。</span><span class="sxs-lookup"><span data-stu-id="881ea-133">Therefore, you can validate the asset values against the attribute requirements that are set up on the functional location.</span></span> <span data-ttu-id="881ea-134">機能的な場所に設定されている属性要件は、チェック マークでマークされています。</span><span class="sxs-lookup"><span data-stu-id="881ea-134">The attribute requirements that are set up on the functional location are marked with a check mark.</span></span>

6. <span data-ttu-id="881ea-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-135">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="881ea-136">新しい機能的な場所に資産を導入することにより、資産の導入を変更するには、この手順のステップ 1～6 に従います。</span><span class="sxs-lookup"><span data-stu-id="881ea-136">To change the installation of an asset by installing it on a new functional location, follow steps 1 through 6 of this procedure.</span></span> <span data-ttu-id="881ea-137">新しい機能的な場所に資産を導入すると、資産は以前の機能的な場所から自動的にアンインストールされます。</span><span class="sxs-lookup"><span data-stu-id="881ea-137">When you install an asset on a new functional location, the asset is automatically uninstalled from the previous functional location.</span></span> <span data-ttu-id="881ea-138">新しい機能的な場所に導入する前に資産に対して作成された有効なメンテナンス要求またはワーク オーダーは、新しい機能的な場所に自動的に転送 **されません**。</span><span class="sxs-lookup"><span data-stu-id="881ea-138">Any active maintenance requests or work orders that were created on the asset before you installed it on a new functional location are **not** automatically transferred to the new functional location.</span></span> <span data-ttu-id="881ea-139">これらのメンテナンス要求とワーク オーダーが資産に対して引き続き必要な場合は、資産が新しい場所に導入された後に手動で再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="881ea-139">If those maintenance requests and work orders are still required for the asset, you must manually re-create them after the asset is installed on the new location.</span></span>

7. <span data-ttu-id="881ea-140">機能的な場所に導入されている下位資産を含むすべての資産のリストを表示するには、**すべての機能的な場所** ページで機能的な場所を選択し、**資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-140">To view a list of all the assets, including sub-assets, that are installed on the functional location, select the functional location on the **All Functional locations** page, and then select **Assets**.</span></span>
8. <span data-ttu-id="881ea-141">機能的な場所に導入されている資産に関連する有効なメンテナンス要求、ワーク オーダー、またはエラー登録のリストを表示するには、**すべての機能的な場所** ページで機能的な場所を選択し、**要求**、**ワーク オーダー**、または **エラー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-141">To view a list of active maintenance requests, active work orders, or fault registrations that are related to the assets that are installed on a functional location, select the functional location on the **All Functional locations** page, and then select **Requests**, **Work orders**, or **Faults**.</span></span>

> [!NOTE]
> <span data-ttu-id="881ea-142">資産関連のデータが変更されると、資産が導入されている機能的な場所で自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="881ea-142">When asset-related data is changed, it's automatically updated on the functional location that the asset is installed on.</span></span> <span data-ttu-id="881ea-143">この自動更新は、リクエスト要求、ワーク オーダー、資産エラー登録、メンテナンス ダウンタイム登録、および資産測定登録の変更に関連します。</span><span class="sxs-lookup"><span data-stu-id="881ea-143">This automatic update pertains to changes to maintenance requests, work orders, asset fault registrations, maintenance downtime registrations, and asset measure registrations.</span></span>

## <a name="automatically-create-one-asset-on-a-functional-location"></a><span data-ttu-id="881ea-144">機能的な場所に 1 つの資産を自動的に作成する</span><span class="sxs-lookup"><span data-stu-id="881ea-144">Automatically create one asset on a functional location</span></span>

<span data-ttu-id="881ea-145">機能的な場所で、*1 つ* の資産を自動作成するために、機能的な場所のステージとタイプを設定できます。</span><span class="sxs-lookup"><span data-stu-id="881ea-145">You can set up functional location stages and functional location types to handle the automatic creation of *one* asset on a functional location.</span></span> <span data-ttu-id="881ea-146">資産は、機能的な場所と同じ ID と名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="881ea-146">The asset gets the same ID and name as the functional location.</span></span> <span data-ttu-id="881ea-147">この機能は、建物などの大きな静的資産のメンテナンスを処理する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="881ea-147">This functionality might be useful when you're handling maintenance on a large, static asset, such as a building.</span></span>

<span data-ttu-id="881ea-148">機能的な場所に資産を自動的に作成する前に、次の設定データが使用可能になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="881ea-148">Before you can automatically create an asset on a functional location, the following setup data must be available:</span></span>

- <span data-ttu-id="881ea-149">資産の自動作成を処理するために、機能的な場所タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="881ea-149">Create a functional location type to handle the automatic creation of an asset.</span></span> <span data-ttu-id="881ea-150">**資産タイプ** フィールドで、資産タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-150">In the **Asset type** field, select an asset type.</span></span> <span data-ttu-id="881ea-151">詳細については、[機能的な場所タイプ](../setup-for-functional-locations/functional-location-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="881ea-151">For more information, see [Functional location types](../setup-for-functional-locations/functional-location-types.md).</span></span>
- <span data-ttu-id="881ea-152">資産の自動作成を処理するために、機能的な場所のライフスタイルの状態を作成します。</span><span class="sxs-lookup"><span data-stu-id="881ea-152">Create a functional location lifecycle state to handle the automatic creation of an asset.</span></span> <span data-ttu-id="881ea-153">**資産の作成** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="881ea-153">Set the **Create asset** option to **Yes**.</span></span> <span data-ttu-id="881ea-154">詳細については、[機能的な場所のライフスタイルの状態](../setup-for-functional-locations/functional-location-stages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="881ea-154">For more information, see [Functional location lifecycle states](../setup-for-functional-locations/functional-location-stages.md).</span></span>

<span data-ttu-id="881ea-155">設定データが利用可能になると、資産を作成する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="881ea-155">After the setup data is available, you're ready to create an asset.</span></span>

1. <span data-ttu-id="881ea-156">**すべての機能的な場所** ページで、資産を自動的に作成する機能的な場所が、この目的のために作成した機能的な場所タイプを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="881ea-156">On the **All Functional locations** page, make sure that the functional location where you want the asset to be automatically created uses the functional location type that you created for this purpose.</span></span>
2. <span data-ttu-id="881ea-157">リストから機能的な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-157">Select the functional location in the list.</span></span>
3. <span data-ttu-id="881ea-158">**機能的な場所の状態を更新する** を選択し、この目的のために作成したライフサイクル状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="881ea-158">Select **Update functional location state**, and then select the lifecycle state that you created for this purpose.</span></span> <span data-ttu-id="881ea-159">1 つの資産が機能的な場所に自動的に導入されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="881ea-159">One asset is now automatically installed on the functional location.</span></span> <span data-ttu-id="881ea-160">この資産は、機能的な場所と同じ名前です。</span><span class="sxs-lookup"><span data-stu-id="881ea-160">This asset has the same name as the functional location.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]