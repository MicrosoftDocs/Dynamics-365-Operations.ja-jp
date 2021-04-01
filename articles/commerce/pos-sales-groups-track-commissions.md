---
title: 売上グループを使用した販売時点管理 (POS) でのコミッションの追跡
description: 顧客からの支援、アップセリング、クロスセリング、トランザクションの処理を担当したアソシエイトの売上を追跡するのは、一般的な小売業務です。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e4820fa02ce66198e1f363ae46f944e3f24146c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243868"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a><span data-ttu-id="45196-103">売上グループを使用した販売時点管理 (POS) でのコミッションの追跡</span><span class="sxs-lookup"><span data-stu-id="45196-103">Track commissions in the point of sale (POS) by using sales groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="45196-104">支援、アップセリング、クロスセリング、トランザクションを提供することによって顧客と作業した協力者の売上を追跡するのは、一般的な小売業務です。</span><span class="sxs-lookup"><span data-stu-id="45196-104">It's a common retail practice to track sales by the associate who worked with the customer by—providing assistance, up-selling, cross-selling, and processing the transaction.</span></span>

<span data-ttu-id="45196-105">販売担当者による売上の追跡は、アソシエイトの販売能力の測定であり、レジ担当者による売上はスピードと効率の測定です。</span><span class="sxs-lookup"><span data-stu-id="45196-105">Tracking sales by sales representative is a measure of the associates selling abilities, while sales by cashier is a measure of speed and efficiency.</span></span> <span data-ttu-id="45196-106">販売担当者が追跡した売上も、手数料やその他のインセンティブの計算によく使用されます。</span><span class="sxs-lookup"><span data-stu-id="45196-106">Sales tracked by sales representative are also often used to calculate commissions or other incentives.</span></span>

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a><span data-ttu-id="45196-107">従業員を POS の販売担当者に設定する</span><span class="sxs-lookup"><span data-stu-id="45196-107">Configuring a worker to be a sales representative in POS</span></span>

<span data-ttu-id="45196-108">従業員が販売グループに追加されると、その従業員は手数料の対象となり、システム内の販売担当者として識別することができます。</span><span class="sxs-lookup"><span data-stu-id="45196-108">When a worker is added to a sales group, they become eligible for commission and can be identified as a sales representative in the system.</span></span> <span data-ttu-id="45196-109">売上グループに所属していない作業員は、委託の対象とならず、POS (営業拠点) アプリケーションに営業担当者として表示されません。</span><span class="sxs-lookup"><span data-stu-id="45196-109">A worker who isn't in a sales group isn't eligible for commission and won't be listed as a sales representative in the point of sale (POS) application.</span></span> <span data-ttu-id="45196-110">POS では、営業担当者のリストは、店舗に割り当てられた少なくとも 1 人の従業員を含むすべての営業グループから派生しています。</span><span class="sxs-lookup"><span data-stu-id="45196-110">In POS, the list of sales representatives is derived from all sales groups that contain at least one worker assigned to the store.</span></span> <span data-ttu-id="45196-111">一覧は、販売グループ ID と名前 (ID : 名前) の組み合わせとして POS に表示されます。</span><span class="sxs-lookup"><span data-stu-id="45196-111">The list is shown in POS as a combination of Sales group ID and Name (ID : Name).</span></span> <span data-ttu-id="45196-112">小売業者が POS ライン上で販売担当者を自動的に設定するシナリオをサポートするために、既定の売上グループを従業員に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="45196-112">A default sales group can be assigned to workers to support scenarios where the retailer chooses to set the sales representative on POS lines automatically.</span></span> <span data-ttu-id="45196-113">ユーザーは、任意の売上グループから、その作業者がメンバーであることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="45196-113">Users can select from any sales group that the worker is a member of.</span></span>

## <a name="functionality-profile-settings"></a><span data-ttu-id="45196-114">機能プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="45196-114">Functionality profile settings</span></span>

<span data-ttu-id="45196-115">販売担当者が関わる POS のフローとプロセスを決定するストアの機能プロファイル設定がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="45196-115">There are a number of functionality profile settings for a store that will determine the flow and process in POS that involve sales representatives.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45196-116">プロファイル</span><span class="sxs-lookup"><span data-stu-id="45196-116">Profile</span></span></th>
<th><span data-ttu-id="45196-117">説明</span><span class="sxs-lookup"><span data-stu-id="45196-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45196-118">既定ではレジ担当者 (利用可能な場合)</span><span class="sxs-lookup"><span data-stu-id="45196-118">Default to cashier when available</span></span></td>
<td><span data-ttu-id="45196-119">このオプションを有効にすると、POS は自動的にトランザクション明細行に現在のレジ担当者の既定の販売グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="45196-119">If this option is enabled, POS will automatically populate transaction lines with the current cashier's default sales group.</span></span> <span data-ttu-id="45196-120">レジ担当者に既定の売上グループが指定されていない場合、値は設定されません。</span><span class="sxs-lookup"><span data-stu-id="45196-120">If a cashier doesn't have a default sales group specified, the value won't be set.</span></span> <span data-ttu-id="45196-121">ユーザーは、POS ボタン グリッド ボタンを使用して売上グループを手動で設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="45196-121">A user could still manually set the sales group by using a POS button grid button.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45196-122">販売担当者の確認</span><span class="sxs-lookup"><span data-stu-id="45196-122">Prompt for sales representative</span></span></td>
<td><span data-ttu-id="45196-123">このオプションには、3つの値があります。</span><span class="sxs-lookup"><span data-stu-id="45196-123">This option has three possible values:</span></span>
<ul>
<li><span data-ttu-id="45196-124"><strong>いいえ</strong> – このオプションを選択すると、売上グループを選択するよう求められません。</span><span class="sxs-lookup"><span data-stu-id="45196-124"><strong>No</strong> – If this option is selected, the user won't be prompted to select a sales group.</span></span> <span data-ttu-id="45196-125">レジ担当者の既定の売上グループを使用するか、または POS ボタン グリッド ボタンを使用して、この値を手動で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="45196-125">The value could still be set by using a cashier's default Sales group or manually by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="45196-126"><strong>トランザクションの開始</strong> – このオプションが選択されていて、<strong>レジ担当者に対する既定</strong>オプションが有効になっていないか、現在のレジ担当者に既定の売上グループがない場合、ユーザーは各取引の開始時に売上グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="45196-126"><strong>Start of transaction</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group at the beginning of each transaction.</span></span> <span data-ttu-id="45196-127">このプロンプトから販売グループを選択すると、後続のすべての明細行が選択された売上グループにデフォルト設定されます。</span><span class="sxs-lookup"><span data-stu-id="45196-127">Selecting a sales group from this prompt will default all subsequent lines to the selected sales group.</span></span> <span data-ttu-id="45196-128">ユーザーは、POS ボタン グリッド ボタンを使用して売上グループを手動で設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="45196-128">A user could still manually set the sales group by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="45196-129"><strong>各行用</strong> – このオプションが選択されていて、<strong>レジ担当者に対する既定</strong>オプションが有効になっていないか、現在のレジ担当者に既定の売上グループがない場合、ユーザーは各行を追加した後に売上グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="45196-129"><strong>For each line</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group after adding each line.</span></span> <span data-ttu-id="45196-130">ユーザーは、POS ボタン グリッド ボタンを使用して売上グループを手動で設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="45196-130">A user could still manually set the Sales group by using a POS button grid button.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="45196-131">必須</span><span class="sxs-lookup"><span data-stu-id="45196-131">Require</span></span></td>
<td><span data-ttu-id="45196-132">このオプションは、POS が販売担当者のプロンプトを表示するように設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="45196-132">This option is only applicable when POS is configured to prompt for a sales representative.</span></span> <span data-ttu-id="45196-133">有効にすると、続行する前に売上グループを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45196-133">If enabled, the user will be required to choose a sales group before continuing.</span></span> <span data-ttu-id="45196-134">それ以外の場合は、ユーザーはプロンプトが表示されますが、選択せずにキャンセルして続行できます。</span><span class="sxs-lookup"><span data-stu-id="45196-134">Otherwise, the user will be prompted, but can cancel and continue without making a selection.</span></span> <span data-ttu-id="45196-135">明細行が追加された後も、十分な権限を持つユーザーは、その明細行から売上グループを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="45196-135">After the line is added, a user with sufficient permissions could still remove the sales group from the line.</span></span> <span data-ttu-id="45196-136">この状況では、「販売担当者が必要」は適用されません。</span><span class="sxs-lookup"><span data-stu-id="45196-136">"Require sales representative" is not enforced in this situation.</span></span></td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a><span data-ttu-id="45196-137">POS トランザクション画面の営業担当者情報の照会</span><span class="sxs-lookup"><span data-stu-id="45196-137">Displaying the Sales representative information on the POS transactions screen</span></span>

<span data-ttu-id="45196-138">POS トランザクション画面のレイアウトと内容は、画面レイアウト設計者および店舗、登録者、または作業者に割り当てられた画面レイアウトを使用して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="45196-138">The POS transaction screen layout and contents are configurable using the screen layout designer and assigned screen layouts to stores, registers, or workers.</span></span> <span data-ttu-id="45196-139">**販売担当者** フィールドは、入荷ウィンドウの明細行タブに追加可能です。</span><span class="sxs-lookup"><span data-stu-id="45196-139">The **Sales representative** field can be added to the Lines tab of the Receipt pane.</span></span>  <span data-ttu-id="45196-140">これにより、取引画面に各明細行の指定された販売グループの ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="45196-140">This will display the ID of the specified Sales group for each line on the transaction screen.</span></span>

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a><span data-ttu-id="45196-141">販売担当者操作を POS ボタン グリッドに追加する</span><span class="sxs-lookup"><span data-stu-id="45196-141">Adding Sales representative operations to POS button grids</span></span>

<span data-ttu-id="45196-142">POS では、画面レイアウトに含まれるボタン グリッドを設定して POS 操作にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="45196-142">POS allows users to configure button grids, which are included in screen layouts to provide access to POS operations.</span></span> <span data-ttu-id="45196-143">次の POS 操作は、販売担当者に関連するボタン グリッド ボタンに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="45196-143">The following POS operations can be assigned to button grid buttons that pertain to Sales representatives.</span></span>

| <span data-ttu-id="45196-144">操作</span><span class="sxs-lookup"><span data-stu-id="45196-144">Operation</span></span>                                 | <span data-ttu-id="45196-145">説明</span><span class="sxs-lookup"><span data-stu-id="45196-145">Description</span></span> |
|-------------------------------------------|-------------|
| <span data-ttu-id="45196-146">明細行の販売担当者の設定</span><span class="sxs-lookup"><span data-stu-id="45196-146">Set sales representative on line</span></span>          | <span data-ttu-id="45196-147">この POS 操作によって、店舗の適格な販売グループ (ID : 名前) のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45196-147">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span> <span data-ttu-id="45196-148">このリストから売上グループを選択すると、現在のトランザクション明細行の値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="45196-148">Selecting a Sales group from this list will set the value on the current transaction line.</span></span> |
| <span data-ttu-id="45196-149">明細行の販売担当者のクリア</span><span class="sxs-lookup"><span data-stu-id="45196-149">Clear sales representative on line</span></span>        | <span data-ttu-id="45196-150">この POS 操作は、現在のトランザクション明細行から現在の売上グループの値を削除します。</span><span class="sxs-lookup"><span data-stu-id="45196-150">This POS operation removes the current Sales group value from the current transaction line.</span></span> |
| <span data-ttu-id="45196-151">トランザクションの販売担当者を設定</span><span class="sxs-lookup"><span data-stu-id="45196-151">Set sales representative on transaction</span></span>   | <span data-ttu-id="45196-152">この POS 操作によって、店舗の適格な販売グループ (ID : 名前) のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45196-152">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span> <span data-ttu-id="45196-153">このリストから売上グループを選択すると、現在のトランザクションの既定値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="45196-153">Selecting a Sales group from this list will set the default value on the current transaction.</span></span> <span data-ttu-id="45196-154">売上グループが割り当てられていない既存の明細行が設定され、その後に追加される明細行も設定されます。</span><span class="sxs-lookup"><span data-stu-id="45196-154">Any existing lines without a sales group assigned will be set, as well as any subsequently added lines.</span></span> |
| <span data-ttu-id="45196-155">トランザクション販売担当者をクリア</span><span class="sxs-lookup"><span data-stu-id="45196-155">Clear sales representative on transaction</span></span> | <span data-ttu-id="45196-156">この POS 操作は、現在のトランザクション明細行から現在の既定の売上グループ値を削除します。</span><span class="sxs-lookup"><span data-stu-id="45196-156">This POS operation removes the current default Sales group value from the current transaction.</span></span> <span data-ttu-id="45196-157">トランザクションにすでに存在する明細行には影響しません。</span><span class="sxs-lookup"><span data-stu-id="45196-157">It does not impact any lines already existing in the transaction.</span></span> |

## <a name="calculating-commissions"></a><span data-ttu-id="45196-158">コミッションの計算</span><span class="sxs-lookup"><span data-stu-id="45196-158">Calculating commissions</span></span>

<span data-ttu-id="45196-159">コミッションは、明細の転記または受注時の転記時に、指定された売上グループの従業員に対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="45196-159">Commission is calculated for the workers in the specified sales groups at the time of statement posting or sales order posting.</span></span> <span data-ttu-id="45196-160">手数料金額は、営業グループで定義された就業者の手数料シェアと、取引上の顧客または製品 (あるいはその両方) の関連手数料計算設定に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="45196-160">The commission amount is determined based on the worker's commission share, as defined in the sales group and the associated commission calculation settings for the customer and/or products on the transaction.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]