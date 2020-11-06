---
title: コール センターのチャネルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しいコール センター チャネルを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: 3f8c47c00b920dae01213d1d241ac8ee6a18d4e3
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107187"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="19251-103">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="19251-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="19251-104">このトピックでは、Microsoft Dynamics 365 Commerce に新しいコール センター チャネルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="19251-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="19251-105">概要</span><span class="sxs-lookup"><span data-stu-id="19251-105">Overview</span></span>


<span data-ttu-id="19251-106">Dynamics 365 Commerce では、コール センターはアプリケーションで定義できる Commerce チャネルのタイプです。</span><span class="sxs-lookup"><span data-stu-id="19251-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="19251-107">コール センター エンティティのチャネルを定義すると、システムによって特定のデータと注文処理の既定値を販売注文に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="19251-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="19251-108">会社は Commerce で複数のコールセンター チャネルを定義できますが、個々のユーザーは 1 つのコール センター チャネルにしかリンクできないことに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19251-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="19251-109">新しいコール センター チャネルを作成する前に、[チャネル設定の前提条件](channels-prerequisites.md) を完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="19251-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="19251-110">新しいコール センター チャネルを作成およびコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="19251-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="19251-111">新しいコール センター チャネルを作成してコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="19251-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="19251-112">ナビゲーション ウィンドウで、 **Retail と Commerce \> チャネル \> コール センター \> すべてのコール センター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="19251-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="19251-113">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="19251-114">**名前** フィールドで、新しいチャネルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="19251-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="19251-115">ドロップダウンから適切な **法人** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="19251-116">ドロップダウンから適切な **倉庫** の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="19251-117">この場所は、顧客または品目のいずれかのレベルで他の既定値が定義されていない限り、このコール センター チャネルに対して作成される販売注文の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="19251-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="19251-118">**既定の顧客** フィールドで、有効な既定の顧客を指定します。</span><span class="sxs-lookup"><span data-stu-id="19251-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="19251-119">このデータは、新しい顧客レコードが作成されるときに、既定値を自動入力するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="19251-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="19251-120">コール センター注文を作成する場合、既定の顧客に対して注文を作成することはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="19251-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="19251-121">**電子メール通知プロファイル** フィールドに、有効な電子メール通知プロファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="19251-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="19251-122">コール センター注文が作成されて処理されると、電子メール通知プロファイルを使用して、注文状況に関する情報を含む自動電子メール警告が顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="19251-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="19251-123">**価格上書き** の情報コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="19251-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="19251-124">このために、最初に情報コードを作成する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="19251-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="19251-125">この情報コードは、コール センター注文で価格変更機能を使用する場合に、ユーザーに対して選択を求める一連の理由コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="19251-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="19251-126">**保留コード** の情報コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="19251-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="19251-127">このために、最初に情報コードを作成する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="19251-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="19251-128">この情報コードは、注文を保留中にする場合に、ユーザーに対して選択を求める一連のオプションの理由コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="19251-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="19251-129">**クレジット** の情報コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="19251-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="19251-130">このために、最初に情報コードを作成する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="19251-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="19251-131">この情報コードでは、コール センターの注文貸方機能を使用して顧客サービスの理由で顧客にその他の払い戻しを行うときにユーザーが選択できる一連の理由コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="19251-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="19251-132">オプション: **財務分析コード** クイック タブで、財務分析コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="19251-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="19251-133">ここに入力した分析コードは、このコール センター チャネルで作成された販売注文に対して既定で設定されます。</span><span class="sxs-lookup"><span data-stu-id="19251-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="19251-134">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19251-134">Click **Save**.</span></span>

<span data-ttu-id="19251-135">次の図は、新しいコール センター チャネルの作成を示しています。</span><span class="sxs-lookup"><span data-stu-id="19251-135">The following image shows the creation of a new call center channel.</span></span>

![新しいコール センター チャネル](media/channel-setup-callcenter-1.png)

<span data-ttu-id="19251-137">次の図は、コール センター チャネルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="19251-137">The following image shows an example call center channel.</span></span>

![コール センター チャネルの例](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="19251-139">追加のチャネル設定</span><span class="sxs-lookup"><span data-stu-id="19251-139">Additional channel setup</span></span>

<span data-ttu-id="19251-140">コール センター チャネルの設定に必要な追加タスクには、支払方法および荷渡方法の設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="19251-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="19251-141">次の図は、 **設定** タブの **荷渡方法** および **支払方法** の設定オプションを示しています。</span><span class="sxs-lookup"><span data-stu-id="19251-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![追加のコール センター チャネル設定アクション](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="19251-143">支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="19251-143">Set up payment methods</span></span>

<span data-ttu-id="19251-144">支払方法を設定するには、このチャネルでサポートされている各支払タイプに対して、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="19251-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="19251-145">ユーザーは事前定義済の支払方法を選択して、コール センター チャネルにリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="19251-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="19251-146">コール センターの支払方法を設定する前に、まず **Retail と Commerce \> チャネル設定 \> 支払方法 \> 支払方法** で主な支払方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="19251-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="19251-147">アクション ウィンドウで、 **設定** タブを選択して、 **支払方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="19251-148">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="19251-149">ナビゲーション ウィンドウで、使用可能な事前定義済の支払から支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="19251-150">支払タイプに必要に応じて追加の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="19251-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="19251-151">クレジット カード、ギフト カード、またはロイヤルティ カードの場合は、 **カード設定** 機能を選択することにより、追加の設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="19251-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="19251-152">**転記** セクションで、支払タイプに対して適切な転記勘定を構成します。</span><span class="sxs-lookup"><span data-stu-id="19251-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="19251-153">アクション ウィンドウで、 **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19251-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="19251-154">次の図は、現金支払い方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="19251-154">The following image shows an example of a cash payment method.</span></span>

![支払方法の例](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="19251-156">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="19251-156">Set up modes of delivery</span></span>

<span data-ttu-id="19251-157">構成されたデリバリー モードは、 **アクション ウィンドウ** の **設定** タブで **デリバリー モード** を選択することによって確認できます。</span><span class="sxs-lookup"><span data-stu-id="19251-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="19251-158">コール センター チャネルに関連付ける荷渡方法を変更または追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="19251-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="19251-159">コール センター 荷渡方法フォームから、 **荷渡方法の管理** を選択する</span><span class="sxs-lookup"><span data-stu-id="19251-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="19251-160">アクション ウィンドウで、 **新規** を選択して新しいデリバリー モードを作成するか、既存のモードを選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="19251-161">**小売チャネル** セクションで、 **行の追加** をクリックしてコール センター チャネルを追加します。</span><span class="sxs-lookup"><span data-stu-id="19251-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="19251-162">各チャネルを個別に追加する代わりに、組織ノードを使用してチャネルを追加すると、チャネルの追加を効率化できます。</span><span class="sxs-lookup"><span data-stu-id="19251-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="19251-163">荷渡方法が **製品** クイック タブおよび **住所** クイック タブのデータで構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="19251-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="19251-164">荷渡方法に有効な製品または配送先住所がない場合は、注文入力時にそれを選択するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="19251-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="19251-165">コール センター荷渡方法の構成に変更を加えた後、変更マトリックスを展開するには、 **配送モードの処理** を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19251-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="19251-166">このジョブは、 **Retail と Commerce \> Retail と Commerce IT \> 配送モードの処理** に移動することによって見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="19251-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="19251-167">次の図は、デリバリー モードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="19251-167">The following image shows an example of a mode of delivery.</span></span>

![荷渡方法の設定](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="19251-169">チャネルのユーザーの設定</span><span class="sxs-lookup"><span data-stu-id="19251-169">Set up channel users</span></span>

<span data-ttu-id="19251-170">Commerce 本社からコール センター チャネルにリンクされた販売注文を作成するには、販売注文を作成するユーザーがコール センター チャネルにリンクされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="19251-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="19251-171">ユーザーは、Commerce 本社で作成された販売注文をコール センター チャネルに手動でリンクすることはできません。</span><span class="sxs-lookup"><span data-stu-id="19251-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="19251-172">リンクは体系的なもので、ユーザー、およびユーザーとコール センター チャネルとの関係に基づいています。</span><span class="sxs-lookup"><span data-stu-id="19251-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="19251-173">ユーザーは、1 つのコール センター チャンネルにしかリンクできません。</span><span class="sxs-lookup"><span data-stu-id="19251-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="19251-174">アクション ウィンドウで、 **チャネル** タブを選択してから、 **チャネル ユーザー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="19251-175">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="19251-176">ドロップダウン選択リストから既存の **ユーザー ID** を選択して、このユーザーをコール センター チャネルにリンクする</span><span class="sxs-lookup"><span data-stu-id="19251-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="19251-177">チャネル ユーザーの設定が完了し、ユーザーが Commerce 本社で新しい販売注文を作成すると、販売注文は関連するコール センター チャネルにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="19251-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="19251-178">このチャネルの構成は、販売注文に体系的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="19251-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="19251-179">販売注文ヘッダーのチャネル名参照を表示することにより、ユーザーは、販売注文がリンクされているコール センター チャネルを確認できます。</span><span class="sxs-lookup"><span data-stu-id="19251-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="19251-180">価格グループの設定</span><span class="sxs-lookup"><span data-stu-id="19251-180">Set up price groups</span></span>

<span data-ttu-id="19251-181">価格グループはオプションですが、使用する場合は、コール センター チャネルで注文する顧客に提供する販売価格を制御できます。</span><span class="sxs-lookup"><span data-stu-id="19251-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="19251-182">価格グループが顧客に対して構成されていない場合、またはカタログ価格グループが販売注文に適用されていない場合 (コール センター注文ヘッダーの **ソースコード ID** フィールドを使用)、チャネル価格グループを使用して品目の価格を検索します。</span><span class="sxs-lookup"><span data-stu-id="19251-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="19251-183">コール センター チャネルに価格グループが見つからない場合は、既定の品目マスター価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="19251-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="19251-184">価格グループを設定するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="19251-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="19251-185">アクション ウィンドウで、 **チャネル** タブをクリックしてから、 **価格グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="19251-186">アクション ウィンドウで、 **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19251-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="19251-187">ドロップダウン選択リストから **小売価格グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19251-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19251-188">追加リソース</span><span class="sxs-lookup"><span data-stu-id="19251-188">Additional resources</span></span>

[<span data-ttu-id="19251-189">チャネルの設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="19251-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="19251-190">コール センターの販売機能</span><span class="sxs-lookup"><span data-stu-id="19251-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="19251-191">コール センターの注文処理オプションの設定</span><span class="sxs-lookup"><span data-stu-id="19251-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="19251-192">コール センターのカタログ</span><span class="sxs-lookup"><span data-stu-id="19251-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="19251-193">詐欺警告の設定および使用</span><span class="sxs-lookup"><span data-stu-id="19251-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="19251-194">コール センターの連続プログラムの設定</span><span class="sxs-lookup"><span data-stu-id="19251-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
