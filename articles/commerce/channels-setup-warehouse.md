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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 772c7584549b30a34e371a7911131edc01214ed8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477637"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="4c680-103">倉庫の設定</span><span class="sxs-lookup"><span data-stu-id="4c680-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c680-104">このトピックでは、Microsoft Dynamics 365 Commerce で新しいチャネルと共に使用する倉庫の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4c680-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4c680-105">各 Commerce チャネルには、関連付けられるコンフィギュレーション済みの倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="4c680-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="4c680-106">次の手順では、Commerce チャネルの倉庫を設定するために最低限必要なコンフィギュレーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="4c680-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="4c680-107">倉庫の設定に関する詳細については、[倉庫管理の概要](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c680-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="4c680-108">倉庫サイトのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4c680-108">Configure a warehouse site</span></span>

<span data-ttu-id="4c680-109">倉庫を設定する前に、倉庫サイトをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c680-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="4c680-110">倉庫のサイトをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4c680-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="4c680-111">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> サイト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c680-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="4c680-112">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4c680-113">**サイト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="4c680-114">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="4c680-115">**一般** セクションで、適切な **タイム ゾーン** を設定します。</span><span class="sxs-lookup"><span data-stu-id="4c680-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="4c680-116">**住所** セクションに、住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="4c680-117">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4c680-118">次の図は、倉庫サイトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c680-118">The following image shows an example warehouse site.</span></span>

![倉庫サイトの例](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="4c680-120">倉庫の設定</span><span class="sxs-lookup"><span data-stu-id="4c680-120">Set up a warehouse</span></span>

<span data-ttu-id="4c680-121">倉庫を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4c680-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="4c680-122">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c680-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="4c680-123">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4c680-124">**倉庫** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="4c680-125">これが店舗への 1:1 マッピングである場合は、店舗名または地域の配送センターの名前を使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="4c680-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="4c680-126">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="4c680-127">**サイト** ドロップダウン リストで、以前に作成した倉庫サイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="4c680-128">**タイプ** フィールドで、**既定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="4c680-129">**検査倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **検査** に設定されている追加の倉庫を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c680-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="4c680-130">**トランジット倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **トランジット** に設定されている追加の倉庫を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c680-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="4c680-131">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="4c680-132">通路を設定します</span><span class="sxs-lookup"><span data-stu-id="4c680-132">Set up inventory aisles</span></span>

<span data-ttu-id="4c680-133">在庫通路を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4c680-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="4c680-134">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 場所の設定 \> 在庫通路** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c680-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="4c680-135">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4c680-136">**倉庫** ドロップダウン リストで、以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="4c680-137">**通路** フィールドに、名前を入力します (例: "Def")。</span><span class="sxs-lookup"><span data-stu-id="4c680-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="4c680-138">**名前** フィールドに、名前を入力します (例: "既定の通路")。</span><span class="sxs-lookup"><span data-stu-id="4c680-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="4c680-139">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="4c680-140">倉庫の在庫場所の設定</span><span class="sxs-lookup"><span data-stu-id="4c680-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="4c680-141">標準、破損、および返品された在庫の倉庫の在庫場所を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4c680-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="4c680-142">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c680-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="4c680-143">以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="4c680-144">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="4c680-145">アクション ウィンドウで、**倉庫** を選択し、**在庫場所** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="4c680-146">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-146">On the action pane, select **New**.</span></span> <span data-ttu-id="4c680-147">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c680-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="4c680-148">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="4c680-149">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="4c680-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="4c680-150">**場所** ボックスに、倉庫の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="4c680-151">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="4c680-152">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="4c680-153">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c680-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="4c680-154">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="4c680-155">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="4c680-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="4c680-156">**場所** ボックスに、「破損」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="4c680-157">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="4c680-158">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="4c680-159">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c680-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="4c680-160">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="4c680-161">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="4c680-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="4c680-162">**場所** ボックスに、「返品」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="4c680-163">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="4c680-164">次の図は、サンフランシスコの倉庫在庫場所の設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c680-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![在庫場所の設定例](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="4c680-166">倉庫の設定の完了</span><span class="sxs-lookup"><span data-stu-id="4c680-166">Complete warehouse setup</span></span>

<span data-ttu-id="4c680-167">倉庫の設定を完了するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4c680-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="4c680-168">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c680-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="4c680-169">以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="4c680-170">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="4c680-171">**在庫および倉庫管理** で:</span><span class="sxs-lookup"><span data-stu-id="4c680-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="4c680-172">**既定の受入場所** を上記で作成した既定の場所に設定します。</span><span class="sxs-lookup"><span data-stu-id="4c680-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="4c680-173">**既定の払出場所** を上記で作成した既定の場所に設定します。</span><span class="sxs-lookup"><span data-stu-id="4c680-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="4c680-174">**住所** セクションで、倉庫の住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="4c680-175">**小売** セクションで:</span><span class="sxs-lookup"><span data-stu-id="4c680-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="4c680-176">**既定の返品場所** ボックスに、以前に作成した返品場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="4c680-177">**格納** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4c680-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="4c680-178">**重量** を **1.00** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4c680-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="4c680-179">**保管分析コード** ボックスに、以前に作成した既定の場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c680-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="4c680-180">**倉庫** セクションで、**現物マイナス在庫** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4c680-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="4c680-181">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c680-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4c680-182">次の図は、コンフィギュレーション済倉庫の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c680-182">The following image shows details for a configured warehouse.</span></span>

![コンフィギュレーション済倉庫の例](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="4c680-184">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4c680-184">Additional resources</span></span>

[<span data-ttu-id="4c680-185">倉庫管理の概要</span><span class="sxs-lookup"><span data-stu-id="4c680-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="4c680-186">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="4c680-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="4c680-187">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="4c680-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="4c680-188">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="4c680-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="4c680-189">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="4c680-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="4c680-190">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="4c680-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
