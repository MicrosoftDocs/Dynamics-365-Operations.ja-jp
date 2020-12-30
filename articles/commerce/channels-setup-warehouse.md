---
title: 倉庫の設定
description: このトピックでは、Microsoft Dynamics 365 Commerce で新しいチャネルと共に使用する倉庫の設定方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413745"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="7af6a-103">倉庫の設定</span><span class="sxs-lookup"><span data-stu-id="7af6a-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7af6a-104">このトピックでは、Microsoft Dynamics 365 Commerce で新しいチャネルと共に使用する倉庫の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7af6a-105">概要</span><span class="sxs-lookup"><span data-stu-id="7af6a-105">Overview</span></span>

<span data-ttu-id="7af6a-106">各 Commerce チャネルには、関連付けられるコンフィギュレーション済みの倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="7af6a-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="7af6a-107">次の手順では、Commerce チャネルの倉庫を設定するために最低限必要なコンフィギュレーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="7af6a-108">倉庫の設定に関する詳細については、[倉庫管理の概要](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7af6a-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="7af6a-109">倉庫サイトのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7af6a-109">Configure a warehouse site</span></span>

<span data-ttu-id="7af6a-110">倉庫を設定する前に、倉庫サイトをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7af6a-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="7af6a-111">倉庫のサイトをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7af6a-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="7af6a-112">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> サイト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="7af6a-113">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7af6a-114">**サイト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="7af6a-115">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7af6a-116">**一般** セクションで、適切な **タイム ゾーン** を設定します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="7af6a-117">**住所** セクションに、住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="7af6a-118">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7af6a-119">次の図は、倉庫サイトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7af6a-119">The following image shows an example warehouse site.</span></span>

![倉庫サイトの例](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="7af6a-121">倉庫の設定</span><span class="sxs-lookup"><span data-stu-id="7af6a-121">Set up a warehouse</span></span>

<span data-ttu-id="7af6a-122">倉庫を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7af6a-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="7af6a-123">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="7af6a-124">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7af6a-125">**倉庫** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="7af6a-126">これが店舗への 1:1 マッピングである場合は、店舗名または地域の配送センターの名前を使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="7af6a-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="7af6a-127">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7af6a-128">**サイト** ドロップダウン リストで、以前に作成した倉庫サイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="7af6a-129">**タイプ** フィールドで、**既定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="7af6a-130">**検査倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **検査** に設定されている追加の倉庫を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7af6a-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="7af6a-131">**トランジット倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **トランジット** に設定されている追加の倉庫を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7af6a-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="7af6a-132">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="7af6a-133">通路を設定します</span><span class="sxs-lookup"><span data-stu-id="7af6a-133">Set up inventory aisles</span></span>

<span data-ttu-id="7af6a-134">在庫通路を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7af6a-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="7af6a-135">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 場所の設定 \> 在庫通路** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="7af6a-136">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7af6a-137">**倉庫** ドロップダウン リストで、以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="7af6a-138">**通路** フィールドに、名前を入力します (例: "Def")。</span><span class="sxs-lookup"><span data-stu-id="7af6a-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="7af6a-139">**名前** フィールドに、名前を入力します (例: "既定の通路")。</span><span class="sxs-lookup"><span data-stu-id="7af6a-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="7af6a-140">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="7af6a-141">倉庫の在庫場所の設定</span><span class="sxs-lookup"><span data-stu-id="7af6a-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="7af6a-142">標準、破損、および返品された在庫の倉庫の在庫場所を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7af6a-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="7af6a-143">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="7af6a-144">以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="7af6a-145">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="7af6a-146">アクション ウィンドウで、**倉庫** を選択し、**在庫場所** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="7af6a-147">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-147">On the action pane, select **New**.</span></span> <span data-ttu-id="7af6a-148">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7af6a-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="7af6a-149">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="7af6a-150">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="7af6a-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="7af6a-151">**場所** ボックスに、倉庫の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="7af6a-152">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="7af6a-153">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="7af6a-154">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7af6a-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="7af6a-155">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="7af6a-156">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="7af6a-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="7af6a-157">**場所** ボックスに、「破損」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="7af6a-158">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="7af6a-159">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="7af6a-160">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7af6a-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="7af6a-161">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="7af6a-162">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="7af6a-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="7af6a-163">**場所** ボックスに、「返品」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="7af6a-164">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="7af6a-165">次の図は、サンフランシスコの倉庫在庫場所の設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="7af6a-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![在庫場所の設定例](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="7af6a-167">倉庫の設定の完了</span><span class="sxs-lookup"><span data-stu-id="7af6a-167">Complete warehouse setup</span></span>

<span data-ttu-id="7af6a-168">倉庫の設定を完了するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7af6a-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="7af6a-169">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="7af6a-170">以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="7af6a-171">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="7af6a-172">**在庫および倉庫管理** で:</span><span class="sxs-lookup"><span data-stu-id="7af6a-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="7af6a-173">**既定の受入場所** を上記で作成した既定の場所に設定します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="7af6a-174">**既定の払出場所** を上記で作成した既定の場所に設定します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="7af6a-175">**住所** セクションで、倉庫の住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="7af6a-176">**小売** セクションで:</span><span class="sxs-lookup"><span data-stu-id="7af6a-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="7af6a-177">**既定の返品場所** ボックスに、以前に作成した返品場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="7af6a-178">**格納** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="7af6a-179">**重量** を **1.00** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="7af6a-180">**保管分析コード** ボックスに、以前に作成した既定の場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="7af6a-181">**倉庫** セクションで、**現物マイナス在庫** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="7af6a-182">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af6a-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7af6a-183">次の図は、コンフィギュレーション済倉庫の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="7af6a-183">The following image shows details for a configured warehouse.</span></span>

![コンフィギュレーション済倉庫の例](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="7af6a-185">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7af6a-185">Additional resources</span></span>

[<span data-ttu-id="7af6a-186">倉庫管理の概要</span><span class="sxs-lookup"><span data-stu-id="7af6a-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7af6a-187">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="7af6a-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7af6a-188">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="7af6a-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7af6a-189">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="7af6a-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="7af6a-190">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="7af6a-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7af6a-191">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="7af6a-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





