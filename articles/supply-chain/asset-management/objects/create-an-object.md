---
title: 資産の作成
description: このトピックでは、資産管理で資産を作成する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a01c1fd72b96bd6ff5e6c76e659394e17060c681
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253401"
---
# <a name="create-an-asset"></a><span data-ttu-id="fe0c3-103">資産の作成</span><span class="sxs-lookup"><span data-stu-id="fe0c3-103">Create an asset</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fe0c3-104">このトピックでは、資産管理で資産を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-104">This topic describes how to create an asset in Asset Management.</span></span>

1. <span data-ttu-id="fe0c3-105">**資産管理** > **共通** > **資産** > **全資産** または **有効な資産** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-105">Click **Asset management** > **Common** > **assets** > **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="fe0c3-106">**新規** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-106">Click the **New** button.</span></span>
3. <span data-ttu-id="fe0c3-107">**資産の作成** ダイアログ ボックスで、**資産** (資産 ID) と資産名に関するデータを挿入します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-107">In the **Create assets** dialog, insert data regarding **Asset** (the asset ID) and the asset name.</span></span> <span data-ttu-id="fe0c3-108">**有効** フィールドで、資産の日時を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-108">Select date and time for the asset in the **Effective** field.</span></span> <span data-ttu-id="fe0c3-109">その日付から、資産を機能の場所にインストールしたり、資産構造内の資産を移動および置換することが可能になります。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-109">From that date, you are able to install the asset on a functional location as well as move and replace the asset in an asset structure.</span></span>
4. <span data-ttu-id="fe0c3-110">**資産タイプ** フィールドで、資産の資産タイプ (必須項目) を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-110">In the **Asset type** field, select the asset type for the asset (mandatory field).</span></span> <span data-ttu-id="fe0c3-111">必要に応じて、資産の **資産メーカー** および **資産モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-111">If required, select **Asset manufacturer** and **Asset model** for the asset.</span></span> <span data-ttu-id="fe0c3-112">1 つの製品のみが設定されている場合、その製品は **資産メーカー** フィールドで自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-112">If only one product has been set up, that product is automatically selected in the **Asset manufacturer** field.</span></span> <span data-ttu-id="fe0c3-113">**資産メーカー** および **資産モデル** フィールドで使用できる選択は、[資産メーカーおよびモデル](../setup-for-objects/product-and-model.md)の設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-113">The selections available in the **Asset manufacturer** and **Asset model** fields depend on the setup in [Asset manufacturers and models](../setup-for-objects/product-and-model.md).</span></span>
5. <span data-ttu-id="fe0c3-114">**親資産** グループでは、**資産** フィールドが既定として空白になります。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-114">In the **Parent asset** group, the **Asset** field is blank as default.</span></span> <span data-ttu-id="fe0c3-115">必要に応じて、親資産を選択すると、**親資産** グループ内のすべてのフィールドが自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-115">If required, you can select a parent asset, and then all fields in the **Parent asset** group will automatically be filled out.</span></span>
    >[!NOTE]  
    ><span data-ttu-id="fe0c3-116">親資産を選択すると、2 つまたは 3 つのタブが使用可能になります。**個人用資産** タブには、ユーザー (システムにログオンしているメンテナンス作業者) が割り当てられる機能の場所に関連する資産が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-116">When you select a parent asset, two or three tabs are available: The **My assets** tab contains assets related to the functional locations to which you (the maintenance worker who is logged on the system) may be allocated.</span></span> <span data-ttu-id="fe0c3-117">[メンテナンス作業者および作業者グループ](../setup-for-objects/workers-and-worker-groups.md) フォームのメンテナンス作業者に機能の場所が設定されていない場合は、**個人用資産** タブは表示されません。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-117">If no functional locations are set up on a maintenance worker in the [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) form, the **My assets** tab will not be visible.</span></span> <span data-ttu-id="fe0c3-118">**有効な資産** タブには、資産ライフサイクル状態が「有効」であるすべての資産の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-118">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="fe0c3-119">**資産表示** タブには、それらの場所にインストールされている機能の場所と資産のツリー ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-119">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="fe0c3-120">設定した既定の機能の場所は、**資産** グループ > **機能の場所** フィールドの資産に対して提案されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-120">The default functional location you have set up is suggested for the asset in the **Asset** group > **Functional location** field.</span></span> <span data-ttu-id="fe0c3-121">必要に応じて、別の機能の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-121">Select another functional location, if required.</span></span>

    >[!NOTE]
    ><span data-ttu-id="fe0c3-122">資産を作成したら、必要に応じて別の機能の場所に資産をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-122">After you have created an asset, you can install it on another functional location, if required.</span></span> <span data-ttu-id="fe0c3-123">機能の場所にインストールできるのは、最上位レベルの資産 (現在の親資産のない資産) のみです。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-123">Only top-level assets (assets without a current parent asset) can be installed on a functional location.</span></span> <span data-ttu-id="fe0c3-124">つまり、選択した機能の場所に最上位レベルの資産と子資産をインストールします。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-124">This means that you install the top level as well as any child assets on the selected functional location.</span></span> <span data-ttu-id="fe0c3-125">機能の場所への資産のインストールの詳細については、[機能の場所の概要](../functional-locations/introduction-to-functional-locations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-125">Read more about installing assets on functional locations in [Introduction to functional locations](../functional-locations/introduction-to-functional-locations.md).</span></span>

7. <span data-ttu-id="fe0c3-126">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-126">Click **OK**.</span></span>
8. <span data-ttu-id="fe0c3-127">**全資産** リストで資産を選択し、**編集** ボタンをクリックして資産に詳細情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-127">Select the asset in the **All Assets** list and click the **Edit** button to add further information to the asset.</span></span>

## <a name="general-information"></a><span data-ttu-id="fe0c3-128">一般情報</span><span class="sxs-lookup"><span data-stu-id="fe0c3-128">General information</span></span>

<span data-ttu-id="fe0c3-129">資産に関連する機能の場所は、**機能の場所** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-129">The functional location to which the asset is related is shown in the **Functional location** field.</span></span> <span data-ttu-id="fe0c3-130">資産が親資産の場合、資産に関連する子の数が **子** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-130">If the asset is a parent asset, the number of children related to the asset is shown in the **Children** field.</span></span> <span data-ttu-id="fe0c3-131">資産が既存の資産に対して下位レベルの資産である場合、親資産の ID が **親** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-131">If the asset is a sub asset to an existing asset, the ID of the parent asset is shown in the **Parent** field.</span></span>

<span data-ttu-id="fe0c3-132">資産の **資産メーカー** および **資産モデル** 情報を編集できます。この情報は、予備部品、代替予備部品、およびジョブ タイプの既定の管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-132">You can edit **Asset manufacturer** and **Asset model** information on the asset, which is used to manage spare parts, alternative spare parts, and job type defaults.</span></span> <span data-ttu-id="fe0c3-133">詳細については、[資産メーカーおよびモデル](../setup-for-objects/product-and-model.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-133">Refer to [Asset manufacturers and models](../setup-for-objects/product-and-model.md) for more information.</span></span> <span data-ttu-id="fe0c3-134">必要に応じて、**年式** と **シリアル番号** に関する情報を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-134">You can also add information about **Model year** and **Serial number**, if required.</span></span>

<span data-ttu-id="fe0c3-135">**現在のライフサイクル状態** は、資産が有効か無効かを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-135">**Current lifecycle state** is used to define if the asset is active or inactive.</span></span> <span data-ttu-id="fe0c3-136">資産を作成する場合、ステージは常に資産ステージ グループの最初のステージに設定されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-136">When creating an asset, the stage is always set to the first stage in the asset stage group.</span></span> <span data-ttu-id="fe0c3-137">資産を有効化する準備ができたら、**資産の状態を更新** をクリックし、「有効な資産」として定義したライフサイクル状態を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-137">When you are ready to activate an asset, click **Update asset state**, and select the lifecycle state that you have defined as "asset active", and click **OK**.</span></span>

<span data-ttu-id="fe0c3-138">**注記:** 資産が「無効」に設定されている場合、その資産の作業指示書を作成することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-138">**Note:** When an asset is set to "inactive", it is no longer possible to create work orders for the asset.</span></span> <span data-ttu-id="fe0c3-139">また、無効な資産の予防的メンテナンス ジョブをスケジュールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-139">Also, you cannot schedule preventive maintenance jobs for an inactive asset.</span></span>

<span data-ttu-id="fe0c3-140">**サービス レベル** および **重大度** フィールドは、資産に対して作成された作業指示書に関連します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-140">The **Service level** and **Criticality** fields relate to work orders created for the asset.</span></span> <span data-ttu-id="fe0c3-141">フィールドには、資産の現在の設定に対して計算された、**サービス レベル** および **重大度** の数値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-141">The fields show the **Service level** and **Criticality** numbers calculated for the current setup for the asset.</span></span> <span data-ttu-id="fe0c3-142">これらの値の設定については、[資産サービス レベル](../setup-for-objects/object-priorities.md) および[資産の重要度タイプ](../setup-for-objects/object-criticalities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-142">Refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md) regarding setup of those values.</span></span>

## <a name="asset"></a><span data-ttu-id="fe0c3-143">資産</span><span class="sxs-lookup"><span data-stu-id="fe0c3-143">Asset</span></span>

<span data-ttu-id="fe0c3-144">資産の **リソース** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-144">You can select a **Resource** for the asset.</span></span> <span data-ttu-id="fe0c3-145">リソースの選択によって、作業指示書のスケジューリングに使用されるカレンダーが決まります。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-145">The resource selection determines which calendar is used for work order scheduling.</span></span> <span data-ttu-id="fe0c3-146">リソースの選択は、固定資産によく使用されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-146">Resource selection is often used for fixed assets.</span></span> <span data-ttu-id="fe0c3-147">リソースおよびリソース グループは、**組織管理** > **リソース** > **リソース グループ** または **リソース** で設定されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-147">Resources and resource groups are set up in **Organization administration** > **Resources** > **Resource groups** or **Resources**.</span></span>

<span data-ttu-id="fe0c3-148">**固定資産番号** フィールドでは、資産に関連する固定資産を選択できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-148">In the **Fixed assets number** field, you can select a fixed asset to be related to the asset.</span></span> <span data-ttu-id="fe0c3-149">これは、資産が投資プロジェクトに関連している場合に関連します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-149">This is relevant if your asset is related to an investment project.</span></span>

- <span data-ttu-id="fe0c3-150">資産が固定資産に関連する場合は、投資プロジェクトに関連する作業指示書に使用する作業指示書タイプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-150">If the asset is related to a fixed asset, you can create a work order type to be used for work orders related to an investment project.</span></span> 
- <span data-ttu-id="fe0c3-151">資産の固定資産に関する情報は、Dynamics 365 Supply Chain Management の **固定資産** モジュールに関連します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-151">Information about fixed assets for an asset is related to the **Fixed assets** module in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fe0c3-152">つまり、**固定資産** > **固定資産** > **固定資産** では、一覧で資産を選択し、その内容を **関連情報** ウィンドウ > **関連付けられたプロジェクト** セクションで表示することで、固定資産に関連付けられている可能性のある資産管理プロジェクトの概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-152">This means that in **Fixed assets** > **Fixed assets** > **Fixed assets**, you can get an overview of the Asset Management projects that may be related to a fixed asset by selecting the asset in the list and viewing the contents in the **Related information** pane > **Associated projects** section.</span></span>


## <a name="details"></a><span data-ttu-id="fe0c3-153">詳細情報</span><span class="sxs-lookup"><span data-stu-id="fe0c3-153">Details</span></span>

<span data-ttu-id="fe0c3-154">**有効開始日** フィールドに、資産ライフサイクル状態を有効な状態に更新した日付 (資産ライフサイクル状態の設定については、[資産ライフサイクル状態](../setup-for-objects/object-stages.md) を参照) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-154">In the **Active from** field, the date on which you updated the asset lifecycle state to an active state (refer to [Asset lifecycle states](../setup-for-objects/object-stages.md) regarding setup of asset lifecycle states), is shown.</span></span> <span data-ttu-id="fe0c3-155">資産が有効でなくなり、資産ライフサイクル状態を無効なライフサイクル状態に更新した場合、資産が無効になる日付が **有効終了日** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-155">If the asset is no longer active, and you have updated the asset lifecycle state to an inactive lifecycle state, the date from which the asset is inactive is shown in the **Active to** field.</span></span> <span data-ttu-id="fe0c3-156">必要に応じて、それらの日付を手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-156">If required, you can manually change those dates.</span></span>

<span data-ttu-id="fe0c3-157">必要に応じて、**交換日** フィールドに資産の交換予定日を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-157">If required, you can insert an expected date for replacement of the asset in the **Replacement date** field.</span></span> <span data-ttu-id="fe0c3-158">資産を交換する推定値は、**交換値** フィールドに挿入できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-158">An estimated value for replacing the asset can be inserted in the **Replacement value** field.</span></span> <span data-ttu-id="fe0c3-159">例: 交換に関する情報を使用して資産の保守コストと比較し、既存の資産の保守コストが急激に増加した場合に新しい資産を購入することを決定できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-159">Example: You can use replacement information to compare it with the costs of maintaining an asset, and subsequently make a decision for purchasing a new asset if maintenance costs on the existing asset increase rapidly.</span></span>

## <a name="notes"></a><span data-ttu-id="fe0c3-160">摘要</span><span class="sxs-lookup"><span data-stu-id="fe0c3-160">Notes</span></span>

<span data-ttu-id="fe0c3-161">**メモ** クイック タブで資産に関連するメモを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-161">You can add notes related to the asset on the **Notes** FastTab.</span></span> <span data-ttu-id="fe0c3-162">ユーザー情報と日付/タイムスタンプをメモに追加する場合は、メモを書き込む前に **タイムスタンプの追加** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-162">Click the **Add timestamp** button before you write the note, if you want to add user information and a date/timestamp to the note.</span></span>

## <a name="attributes"></a><span data-ttu-id="fe0c3-163">属性</span><span class="sxs-lookup"><span data-stu-id="fe0c3-163">Attributes</span></span>

<span data-ttu-id="fe0c3-164">このクイック タブでは、資産属性の値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-164">On this FastTab, you can set values for asset attributes.</span></span> <span data-ttu-id="fe0c3-165">これらの属性を使用して、資産に関連するプロパティまたは特性、たとえばサイズ、重量、マシンの構成などを記述できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-165">These attributes can be used to describe properties or characteristics pertinent to the asset, for example, size, weight, or machine configuration.</span></span>

<span data-ttu-id="fe0c3-166">**明細行の追加** をクリックして、属性の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-166">Click **Add line** and select the attribute type.</span></span> <span data-ttu-id="fe0c3-167">次に、属性タイプに関連付けられている **値** を挿入し、レコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-167">Next, insert the **Value** related to the attribute type and save the record.</span></span>

>[!NOTE] 
><span data-ttu-id="fe0c3-168">**資産属性** と **資産属性の概要** で、資産属性タイプと資産との関係の概要を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-168">You can get an overview of asset attribute types and their relation to the assets in **Asset attribute** and **Asset attribute overview**.</span></span> <span data-ttu-id="fe0c3-169">詳細については、[資産属性の概要](../objects/object-specification-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-169">Refer to [Asset attribute overview](../objects/object-specification-overview.md) for more information.</span></span>

## <a name="vendor"></a><span data-ttu-id="fe0c3-170">仕入先</span><span class="sxs-lookup"><span data-stu-id="fe0c3-170">Vendor</span></span>

<span data-ttu-id="fe0c3-171">**仕入先** クイック タブで、資産の仕入先勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-171">On the **Vendor** FastTab, select a vendor account for the asset.</span></span> <span data-ttu-id="fe0c3-172">また、仕入先保証が付与されている場合は、ここに保証情報を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-172">Also, if a vendor warranty has been granted, you can insert warranty information here.</span></span>

## <a name="address"></a><span data-ttu-id="fe0c3-173">住所</span><span class="sxs-lookup"><span data-stu-id="fe0c3-173">Address</span></span>

<span data-ttu-id="fe0c3-174">**アドレス** クイック タブで、機器のアドレスを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-174">On the **Address** FastTab, you can insert the address of the equipment.</span></span> <span data-ttu-id="fe0c3-175">資産にアドレスが挿入されていない場合、親資産にアドレスがある場合には、資産は親資産のアドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-175">If no address is inserted on the asset, the asset uses the address of a parent asset, if the parent asset has an address.</span></span> <span data-ttu-id="fe0c3-176">資産階層内の資産または親に関連付けられているアドレスがない場合は、資産がインストールされている機能の場所のアドレスが使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-176">If no address is related to the asset or any parents in the asset hierarchy, the address of the functional location on which the asset is installed may be used.</span></span> <span data-ttu-id="fe0c3-177">その機能の場所に関連付けられているアドレスがない場合は、親機能の場所のアドレスが資産で使用されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-177">If that functional location does not have an address related to it, the address of the parent functional location is used on the asset.</span></span>

## <a name="asset-management-plans"></a><span data-ttu-id="fe0c3-178">資産管理計画</span><span class="sxs-lookup"><span data-stu-id="fe0c3-178">Asset management plans</span></span>

<span data-ttu-id="fe0c3-179">メンテナンス計画は、資産の予防的メンテナンス ジョブを定期的にスケジュールするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-179">Maintenance plans are used for scheduling preventive maintenance jobs at regular intervals on the asset.</span></span> <span data-ttu-id="fe0c3-180">このクイック タブでは、選択した資産のメンテナンス計画明細行を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-180">On this FastTab, you can set up maintenance plan lines for the selected asset.</span></span> <span data-ttu-id="fe0c3-181">メンテナンス ラウンドは、定期的に同様のタスクを実行する必要があるさまざまな資産に対して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-181">Maintenance rounds can be set up for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="fe0c3-182">**機能の場所のメンテナンス計画** タブには、資産がインストールされている機能の場所に関連付けられているメンテナンス計画が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-182">On the **Functional location maintenance plans** tab, you see the maintenance plans related to the functional location on which the asset is installed.</span></span>

>[!NOTE]
><span data-ttu-id="fe0c3-183">**全資産** の資産に関連付けられているメンテナンス計画明細行またはメンテナンス ラウンドを削除すると、そのメンテナンス計画またはメンテナンス ラウンドに基づいて作成された、「作成済」状態を持つすべてのメンテナンス スケジュールも自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-183">If you delete a maintenance plan line or a maintenance round related to an asset in **All Asset**, you also automatically delete all maintenance schedules with status "Created" that have been created based on that maintenance plan or maintenance round.</span></span>

## <a name="functional-location-maintenance-plans"></a><span data-ttu-id="fe0c3-184">機能的な場所のメンテナンス計画</span><span class="sxs-lookup"><span data-stu-id="fe0c3-184">Functional location maintenance plans</span></span>

<span data-ttu-id="fe0c3-185">このクイック タブでは、資産がインストールされている機能の場所に関連付けられているメンテナンス計画の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-185">On this FastTab, you get an overview of the maintenance plans related to the functional location on which the asset is installed.</span></span>

## <a name="maintenance-rounds"></a><span data-ttu-id="fe0c3-186">メンテナンス ラウンド</span><span class="sxs-lookup"><span data-stu-id="fe0c3-186">Maintenance rounds</span></span>

<span data-ttu-id="fe0c3-187">このクイック タブでは、資産に関連付けられているメンテナンス ラウンドを追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-187">On this FastTab, you can add or remove maintenance rounds, which are related to the asset.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="fe0c3-188">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="fe0c3-188">Financial dimensions</span></span>

<span data-ttu-id="fe0c3-189">資産の財務分析コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-189">You can select financial dimensions for the asset.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]