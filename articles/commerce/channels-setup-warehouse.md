---
title: 倉庫の設定
description: このトピックでは、Microsoft Dynamics 365 Commerce で新しいチャネルと共に使用する倉庫の設定方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800498"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="a0150-103">倉庫の設定</span><span class="sxs-lookup"><span data-stu-id="a0150-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a0150-104">このトピックでは、Microsoft Dynamics 365 Commerce で新しいチャネルと共に使用する倉庫の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a0150-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a0150-105">各 Commerce チャネルには、関連付けられるコンフィギュレーション済みの倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="a0150-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="a0150-106">次の手順では、Commerce チャネルの倉庫を設定するために最低限必要なコンフィギュレーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="a0150-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="a0150-107">倉庫の設定に関する詳細については、[倉庫管理の概要](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0150-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="a0150-108">倉庫サイトのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a0150-108">Configure a warehouse site</span></span>

<span data-ttu-id="a0150-109">倉庫を設定する前に、倉庫サイトをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0150-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="a0150-110">倉庫のサイトをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0150-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="a0150-111">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> サイト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0150-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="a0150-112">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a0150-113">**サイト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="a0150-114">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="a0150-115">**一般** セクションで、適切な **タイム ゾーン** を設定します。</span><span class="sxs-lookup"><span data-stu-id="a0150-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="a0150-116">**住所** セクションに、住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="a0150-117">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a0150-118">次の図は、倉庫サイトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="a0150-118">The following image shows an example warehouse site.</span></span>

![倉庫サイトの例](media/warehouse-site.png)

## <a name="set-up-a-warehouse&quot;></a><span data-ttu-id=&quot;a0150-120&quot;>倉庫の設定</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-120&quot;>Set up a warehouse</span></span>

<span data-ttu-id=&quot;a0150-121&quot;>倉庫を設定するには、次の手順に従います。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-121&quot;>To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id=&quot;a0150-122&quot;>ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-122&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id=&quot;a0150-123&quot;>アクション ウィンドウで、**新規** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-123&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;a0150-124&quot;>**倉庫** フィールドで値を入力します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-124&quot;>In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id=&quot;a0150-125&quot;>これが店舗への 1:1 マッピングである場合は、店舗名または地域の配送センターの名前を使用することを検討してください。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-125&quot;>If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id=&quot;a0150-126&quot;>**名前** フィールドに値を入力します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-126&quot;>In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id=&quot;a0150-127&quot;>**サイト** ドロップダウン リストで、以前に作成した倉庫サイトを選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-127&quot;>In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id=&quot;a0150-128&quot;>**タイプ** フィールドで、**既定** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-128&quot;>In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id=&quot;a0150-129&quot;>**検査倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **検査** に設定されている追加の倉庫を作成する必要があります。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-129&quot;>If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id=&quot;a0150-130&quot;>**トランジット倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **トランジット** に設定されている追加の倉庫を作成する必要があります。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-130&quot;>If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id=&quot;a0150-131&quot;>アクション ウィンドウで、**保存** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-131&quot;>On the action pane, select **Save**.</span></span>

## <a name=&quot;set-up-inventory-aisles&quot;></a><span data-ttu-id=&quot;a0150-132&quot;>通路を設定します</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-132&quot;>Set up inventory aisles</span></span>

<span data-ttu-id=&quot;a0150-133&quot;>在庫通路を設定するには、次の手順に従います。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-133&quot;>To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id=&quot;a0150-134&quot;>ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 場所の設定 \> 在庫通路** の順に移動します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-134&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id=&quot;a0150-135&quot;>アクション ウィンドウで、**新規** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-135&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;a0150-136&quot;>**倉庫** ドロップダウン リストで、以前に作成した倉庫を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a0150-136&quot;>In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id=&quot;a0150-137&quot;>**通路** フィールドに、名前を入力します (例: &quot;Def")。</span><span class="sxs-lookup"><span data-stu-id="a0150-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="a0150-138">**名前** フィールドに、名前を入力します (例: "既定の通路")。</span><span class="sxs-lookup"><span data-stu-id="a0150-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="a0150-139">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="a0150-140">倉庫の在庫場所の設定</span><span class="sxs-lookup"><span data-stu-id="a0150-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="a0150-141">標準、破損、および返品された在庫の倉庫の在庫場所を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0150-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="a0150-142">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0150-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="a0150-143">以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="a0150-144">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="a0150-145">アクション ウィンドウで、**倉庫** を選択し、**在庫場所** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="a0150-146">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-146">On the action pane, select **New**.</span></span> <span data-ttu-id="a0150-147">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0150-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="a0150-148">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="a0150-149">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="a0150-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="a0150-150">**場所** ボックスに、倉庫の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="a0150-151">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="a0150-152">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="a0150-153">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0150-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="a0150-154">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="a0150-155">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="a0150-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="a0150-156">**場所** ボックスに、「破損」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="a0150-157">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="a0150-158">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="a0150-159">**倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0150-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="a0150-160">**通路** ボックスに、前に指定した通路の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="a0150-161">**手動更新** を **はい** に設定する</span><span class="sxs-lookup"><span data-stu-id="a0150-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="a0150-162">**場所** ボックスに、「返品」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="a0150-163">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="a0150-164">次の図は、サンフランシスコの倉庫在庫場所の設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="a0150-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![在庫場所の設定例](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="a0150-166">倉庫の設定の完了</span><span class="sxs-lookup"><span data-stu-id="a0150-166">Complete warehouse setup</span></span>

<span data-ttu-id="a0150-167">倉庫の設定を完了するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0150-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="a0150-168">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0150-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="a0150-169">以前に作成した倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="a0150-170">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="a0150-171">**在庫および倉庫管理** で:</span><span class="sxs-lookup"><span data-stu-id="a0150-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="a0150-172">**既定の受入場所** を上記で作成した既定の場所に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0150-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="a0150-173">**既定の払出場所** を上記で作成した既定の場所に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0150-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="a0150-174">**住所** セクションで、倉庫の住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="a0150-175">**小売** セクションで:</span><span class="sxs-lookup"><span data-stu-id="a0150-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="a0150-176">**既定の返品場所** ボックスに、以前に作成した返品場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="a0150-177">**格納** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0150-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="a0150-178">**重量** を **1.00** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0150-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="a0150-179">**保管分析コード** ボックスに、以前に作成した既定の場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0150-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="a0150-180">**倉庫** セクションで、**現物マイナス在庫** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0150-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="a0150-181">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0150-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a0150-182">次の図は、コンフィギュレーション済倉庫の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="a0150-182">The following image shows details for a configured warehouse.</span></span>

![コンフィギュレーション済倉庫の例](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="a0150-184">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a0150-184">Additional resources</span></span>

[<span data-ttu-id="a0150-185">倉庫管理の概要</span><span class="sxs-lookup"><span data-stu-id="a0150-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="a0150-186">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="a0150-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a0150-187">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="a0150-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a0150-188">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="a0150-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="a0150-189">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="a0150-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="a0150-190">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="a0150-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
