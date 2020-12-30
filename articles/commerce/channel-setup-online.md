---
title: オンライン チャネルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しいオンライン チャネルを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 07225d97af76ea665fa28362cc205c6e8dc4fdf4
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2020
ms.locfileid: "4413904"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="c2e89-103">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c2e89-104">このトピックでは、Microsoft Dynamics 365 Commerce に新しいオンライン チャネルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c2e89-105">概要</span><span class="sxs-lookup"><span data-stu-id="c2e89-105">Overview</span></span>

<span data-ttu-id="c2e89-106">Dynamics 365 Commerce は複数の小売チャンネルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="c2e89-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="c2e89-107">これらの小売チャンネルには、オンライン ストア、コール センター、および小売用店舗 (従来型の店舗とも呼ばれる) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c2e89-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="c2e89-108">オンライン ストアは、小売店舗に加えて小売業者のオンライン ストアから製品を購入するオプションを顧客に提供します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="c2e89-109">Commerce でオンライン ストアを作成するには、最初にオンライン チャネルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2e89-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="c2e89-110">新しいオンライン チャネルを作成する前に、[チャネル設定の前提条件](channels-prerequisites.md) を完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c2e89-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="c2e89-111">新しいサイトを作成する前に、少なくとも 1 つのオンライン ストアをコマースで作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2e89-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="c2e89-112">詳細については、[E コマース サイトの作成](create-ecommerce-site.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2e89-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="c2e89-113">新しいオンライン チャネルを作成およびコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="c2e89-113">Create and configure a new online channel</span></span>

<span data-ttu-id="c2e89-114">新しいオンライン チャネルを作成してコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2e89-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="c2e89-115">ナビゲーション ウィンドウで、**モジュール \> チャネル \> オンライン ストア** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="c2e89-116">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c2e89-117">**名前** フィールドで、新しいチャネルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="c2e89-118">**法人** ドロップダウンで、適切な法人を入力します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="c2e89-119">**倉庫** ドロップダウンで、適切な倉庫を入力します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="c2e89-120">**店舗タイム ゾーン** フィールドで、適切なタイム ゾーンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="c2e89-121">**通貨** フィールドで、適切な通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="c2e89-122">**既定の顧客** フィールドで、有効な既定の顧客を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="c2e89-123">**顧客アドレス帳** フィールドで、有効なアドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="c2e89-124">**機能プロファイル** フィールドで、該当する場合は機能プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="c2e89-125">**電子メール通知プロファイル** フィールドに、有効な電子メール通知プロファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="c2e89-126">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c2e89-127">次の図は、新しいオンライン チャネルの作成を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2e89-127">The following image shows the creation of a new online channel.</span></span>

![新しいオンライン チャネル](media/channel-setup-online-1.png)

<span data-ttu-id="c2e89-129">次の図は、オンライン チャネルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2e89-129">The following image shows an example online channel.</span></span>

![オンライン チャネルの例](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="c2e89-131">言語の設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-131">Set up languages</span></span>

<span data-ttu-id="c2e89-132">E コマース サイトで複数の言語をサポートする場合は、**言語** セクションを展開し、必要に応じて追加の言語を追加します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="c2e89-133">支払勘定の設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-133">Set up payment account</span></span>

<span data-ttu-id="c2e89-134">**支払勘定** セクション内から、サードパーティの支払プロバイダーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c2e89-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="c2e89-135">Adyen 支払コネクタ設定の詳細については、[Adyen 向け Dynamics 365 Payment Connector](../retail/dev-itpro/adyen-connector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2e89-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="c2e89-136">追加のチャネル設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-136">Additional channel setup</span></span>

<span data-ttu-id="c2e89-137">オンライン チャネルの設定に必要な追加タスクには、支払方法、荷渡方法、およびフルフィルメント グループの割り当ての設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c2e89-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="c2e89-138">次の図は、**設定** タブの **荷渡方法**、**支払方法**、および **フルフィルメント グループの割り当て** の設定オプションを示しています。</span><span class="sxs-lookup"><span data-stu-id="c2e89-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![追加のオンライン チャネル設定アクション](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="c2e89-140">支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-140">Set up payment methods</span></span>

<span data-ttu-id="c2e89-141">支払方法を設定するには、このチャネルでサポートされている各支払タイプに対して、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2e89-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="c2e89-142">アクション ウィンドウで、**設定** タブを選択し、**支払方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="c2e89-143">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c2e89-144">ナビゲーション ウィンドウで、目的の支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="c2e89-145">**全般** セクションで、**操作名** を指定し、その他の必要な設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="c2e89-146">支払タイプに必要に応じて追加の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="c2e89-147">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c2e89-148">次の図は、現金支払い方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2e89-148">The following image shows an example of a cash payment method.</span></span>

![支払方法の例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="c2e89-150">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-150">Set up modes of delivery</span></span>

<span data-ttu-id="c2e89-151">構成されたデリバリー モードは、**アクション ウィンドウ** の **設定** タブで **デリバリー モード** を選択することによって確認できます。</span><span class="sxs-lookup"><span data-stu-id="c2e89-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="c2e89-152">デリバリー モードを変更または追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2e89-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="c2e89-153">ナビゲーション ウィンドウで、**モジュール \> 在庫管理 \> デリバリー モード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="c2e89-154">アクション ウィンドウで、**新規** を選択して新しいデリバリー モードを作成するか、既存のモードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="c2e89-155">**小売チャネル** セクションで、**行の追加** を選択してチャネルを追加します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="c2e89-156">各チャネルを個別に追加する代わりに、組織ノードを使用してチャネルを追加すると、チャネルの追加を効率化できます。</span><span class="sxs-lookup"><span data-stu-id="c2e89-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="c2e89-157">次の図は、デリバリー モードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2e89-157">The following image shows an example of a mode of delivery.</span></span>

![荷渡方法の設定](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="c2e89-159">フルフィルメント グループの割り当ての設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="c2e89-160">フルフィルメント グループの割り当てを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2e89-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="c2e89-161">アクション ウィンドウで、**設定** タブを選択し、**フルフィルメント グループの割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="c2e89-162">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c2e89-163">**フルフィルメント グループ** ドロップダウン リストで、フルフィルメント グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="c2e89-164">**説明** ドロップダウン リストに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="c2e89-165">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e89-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c2e89-166">次の図は、フルフィルメント グループの割り当ての設定の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2e89-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![フルフィルメント グループの割り当ての設定](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="c2e89-168">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c2e89-168">Additional resources</span></span>

[<span data-ttu-id="c2e89-169">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="c2e89-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c2e89-170">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="c2e89-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="c2e89-171">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="c2e89-172">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="c2e89-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="c2e89-173">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="c2e89-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
