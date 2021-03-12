---
title: 小売チャネルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しいチャネルを作成する方法について説明します。
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
ms.openlocfilehash: 100822ecea03d03267f98654c66e74f2f5924bd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997728"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="838f9-103">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="838f9-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="838f9-104">このトピックでは、Microsoft Dynamics 365 Commerce に新しいチャネルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="838f9-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="838f9-105">概要</span><span class="sxs-lookup"><span data-stu-id="838f9-105">Overview</span></span>

<span data-ttu-id="838f9-106">Dynamics 365 Commerce は複数の小売チャンネルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="838f9-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="838f9-107">これらの小売チャンネルには、オンライン ストア、コール センター、および小売用店舗 (従来型の店舗とも呼ばれる) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="838f9-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="838f9-108">各小売店舗チャネルは、独自の支払方法、価格グループ、POS レジスタ、収入/経費勘定、およびスタッフを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="838f9-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="838f9-109">小売店舗チャネルを作成する前に、これらのすべての要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="838f9-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="838f9-110">小売チャネルを作成する前に、[チャネルの前提条件](channels-prerequisites.md)に従っていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="838f9-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="838f9-111">新しい小売チャネルの作成および構成</span><span class="sxs-lookup"><span data-stu-id="838f9-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="838f9-112">ナビゲーション ウィンドウで、**モジュール \> チャネル \> 店舗 \> すべての店舗** に移動します。</span><span class="sxs-lookup"><span data-stu-id="838f9-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="838f9-113">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="838f9-114">**名前** フィールドで、新しいチャネルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="838f9-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="838f9-115">**店舗番号** フィールドで、固有の店舗番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="838f9-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="838f9-116">番号は英数字で、最大文字数は 10 です。</span><span class="sxs-lookup"><span data-stu-id="838f9-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="838f9-117">**法人** ドロップダウン リストで、適切な法人を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="838f9-118">**倉庫** ドロップダウン リストで、適切な倉庫を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="838f9-119">**店舗タイム ゾーン** フィールドで、適切なタイム ゾーンを選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="838f9-120">**売上税グループ** ドロップダウン リストで、店舗の適切な売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="838f9-121">**通貨** フィールドで、適切な通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="838f9-122">**顧客アドレス帳** フィールドで、有効なアドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="838f9-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="838f9-123">**既定の顧客** フィールドで、有効な既定の顧客を指定します。</span><span class="sxs-lookup"><span data-stu-id="838f9-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="838f9-124">**機能プロファイル** フィールドで、該当する場合は機能プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="838f9-125">**電子メール通知プロファイル** フィールドに、有効な電子メール通知プロファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="838f9-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="838f9-126">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="838f9-127">次の図は、新しい小売チャネルの作成を示しています。</span><span class="sxs-lookup"><span data-stu-id="838f9-127">The following image shows the creation of a new retail channel.</span></span>

![新しい小売チャネル](media/channel-setup-retail-1.png)

<span data-ttu-id="838f9-129">次の図は、小売チャネルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="838f9-129">The following image shows an example retail channel.</span></span>

![小売チャネルの例](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="838f9-131">その他の設定</span><span class="sxs-lookup"><span data-stu-id="838f9-131">Other settings</span></span>

<span data-ttu-id="838f9-132">**明細書/決算** セクションおよび **その他** のセクションで設定できるオプション設定には、小売店舗のニーズに応じてさまざまなものがあります。</span><span class="sxs-lookup"><span data-stu-id="838f9-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="838f9-133">**画面レイアウト** セクションでの既定のスクリーン レイアウト設定に関する情報については、[販売時点管理 (POS) の画面レイアウト](pos-screen-layouts.md)を、および **ハードウェア ステーション** セクションのセットアップ情報については、[Retail ハードウェア ステーションのコンフィギュレーションおよびインストール](retail-hardware-station-configuration-installation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="838f9-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="838f9-134">次の図は、小売チャネルの設定構成の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="838f9-134">The following image shows an example retail channel setup configuration.</span></span>

![小売チャネル構成の例](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="838f9-136">追加チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="838f9-136">Additional channel set up</span></span>

<span data-ttu-id="838f9-137">**設定** セクションの下にある **アクション ウィンドウ** で、チャネルに対して設定する必要がある追加の品目があります。</span><span class="sxs-lookup"><span data-stu-id="838f9-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="838f9-138">オンライン チャネルの設定に必要な追加タスクには、支払方法、現金申告、荷渡方法、収入/経費勘定、セクション、フルフィルメント グループの割り当て、および安全があります。</span><span class="sxs-lookup"><span data-stu-id="838f9-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="838f9-139">次の図は、**設定** タブのさまざまな追加の小売チャネル設定オプションを示します。</span><span class="sxs-lookup"><span data-stu-id="838f9-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![チャネルの設定](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="838f9-141">支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="838f9-141">Set up payment methods</span></span>

<span data-ttu-id="838f9-142">支払方法を設定するには、このチャネルでサポートされている各支払タイプに対して、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="838f9-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="838f9-143">アクション ウィンドウで、**設定** タブを選択し、**支払方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="838f9-144">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="838f9-145">ナビゲーション ウィンドウで、目的の支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="838f9-146">**全般** セクションで、**操作名** を指定し、その他の必要な設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="838f9-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="838f9-147">支払タイプに必要に応じて追加の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="838f9-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="838f9-148">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="838f9-149">次の図は、現金支払い方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="838f9-149">The following image shows an example of a cash payment method.</span></span>

![支払方法の例](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="838f9-151">現金申告の設定</span><span class="sxs-lookup"><span data-stu-id="838f9-151">Set up cash declaration</span></span>

1. <span data-ttu-id="838f9-152">アクション ウィンドウで、**設定** タブを選択し、**現金申告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="838f9-153">アクション ウィンドウで、**新規** を選択し、該当するすべての **コイン** および **注記** の単位を作成します。</span><span class="sxs-lookup"><span data-stu-id="838f9-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="838f9-154">次の図は、現金申告の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="838f9-154">The following image shows an example of a cash declaration.</span></span>

![現金申告の設定](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="838f9-156">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="838f9-156">Set up modes of delivery</span></span>

<span data-ttu-id="838f9-157">構成されたデリバリー モードは、**アクション ウィンドウ** の **設定** タブで **デリバリー モード** を選択することによって確認できます。</span><span class="sxs-lookup"><span data-stu-id="838f9-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="838f9-158">デリバリー モードを変更または追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="838f9-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="838f9-159">ナビゲーション ウィンドウで、**モジュール \> 在庫管理 \> デリバリー モード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="838f9-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="838f9-160">アクション ウィンドウで、**新規** を選択して新しいデリバリー モードを作成するか、既存のモードを選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="838f9-161">**小売チャネル** セクションで、**行の追加** を選択してチャネルを追加します。</span><span class="sxs-lookup"><span data-stu-id="838f9-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="838f9-162">各チャネルを個別に追加する代わりに、組織ノードを使用してチャネルを追加すると、チャネルの追加を効率化できます。</span><span class="sxs-lookup"><span data-stu-id="838f9-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="838f9-163">次の図は、デリバリー モードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="838f9-163">The following image shows an example of a mode of delivery.</span></span>

![荷渡方法の設定](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="838f9-165">収入/経費勘定の設定</span><span class="sxs-lookup"><span data-stu-id="838f9-165">Set up income/expense account</span></span>

<span data-ttu-id="838f9-166">収入/経費勘定を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="838f9-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="838f9-167">アクション ウィンドウで、**設定** タブを選択し、**収入/経費勘定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="838f9-168">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="838f9-169">**名前** に、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="838f9-170">**検索名** に、検索名を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="838f9-171">**勘定タイプ** に、勘定タイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="838f9-172">必要に応じて、**メッセージ行 1**、**メッセージ行 2**、**伝票テキスト 1**、および **伝票テキスト 2** のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="838f9-173">**転記** に、転記情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="838f9-174">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="838f9-175">以下の図は、収入/経費勘定の例を示します。</span><span class="sxs-lookup"><span data-stu-id="838f9-175">The following image shows an example of an income/expense account.</span></span>

![収入/経費勘定の設定](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="838f9-177">セクションの設定</span><span class="sxs-lookup"><span data-stu-id="838f9-177">Set up sections</span></span>

<span data-ttu-id="838f9-178">セクションをセットアップするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="838f9-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="838f9-179">アクション ウィンドウで、**設定** タブを選択し、**セクション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="838f9-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="838f9-180">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="838f9-181">**セクション番号** で、セクション番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="838f9-182">**説明** で、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="838f9-183">**セクション サイズ** で、セクション サイズを入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="838f9-184">必要に応じて、**一般** および **販売統計** の追加設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="838f9-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="838f9-185">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="838f9-186">フルフィルメント グループの割り当ての設定</span><span class="sxs-lookup"><span data-stu-id="838f9-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="838f9-187">フルフィルメント グループの割り当てを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="838f9-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="838f9-188">アクション ウィンドウで、**設定** タブを選択し、**フルフィルメント グループの割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="838f9-189">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="838f9-190">**フルフィルメント グループ** ドロップダウン リストで、フルフィルメント グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="838f9-191">**説明** ドロップダウン リストに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="838f9-192">アクション ウィンドウで、**保存** を選択します</span><span class="sxs-lookup"><span data-stu-id="838f9-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="838f9-193">次の図は、フルフィルメント グループの割り当ての設定の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="838f9-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![フルフィルメント グループの割り当ての設定](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="838f9-195">安全の設定</span><span class="sxs-lookup"><span data-stu-id="838f9-195">Set up safes</span></span>

<span data-ttu-id="838f9-196">安全をセットアップするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="838f9-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="838f9-197">アクション ウィンドウで、**設定** タブを選択し、**安全** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="838f9-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="838f9-198">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="838f9-199">安全の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="838f9-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="838f9-200">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="838f9-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="838f9-201">追加リソース</span><span class="sxs-lookup"><span data-stu-id="838f9-201">Additional resources</span></span>

[<span data-ttu-id="838f9-202">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="838f9-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="838f9-203">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="838f9-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="838f9-204">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="838f9-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="838f9-205">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="838f9-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

