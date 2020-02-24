---
title: チャネルの返品と払戻のポリシーを作成および更新する
description: このトピックでは、チャネルに対する返品と払戻のポリシーを設定する方法について説明します。
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 66bb9bbd338561315f2f69ae4aff86a67513b190
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3023229"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="a8422-103">チャネルの返品と払戻のポリシーを作成および更新する</span><span class="sxs-lookup"><span data-stu-id="a8422-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]


## <a name="overview"></a><span data-ttu-id="a8422-104">概要</span><span class="sxs-lookup"><span data-stu-id="a8422-104">Overview</span></span>

<span data-ttu-id="a8422-105">Dynamics 365 Commerce のチャネルの返品ポリシーでは、小売業者は、販売時点管理 (POS) デバイスの返品の処理のために支払業者が許可される適用を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a8422-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="a8422-106">このトピックでは、チャネルに対する返品と払戻のポリシーを設定する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8422-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="a8422-107">ポリシーの範囲は、チャネルに対して許可される支払業者を設定することに制限されています。</span><span class="sxs-lookup"><span data-stu-id="a8422-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="a8422-108">"許可済"リストは、購入に使用される支払方法に基づきます。</span><span class="sxs-lookup"><span data-stu-id="a8422-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="a8422-109">例:</span><span class="sxs-lookup"><span data-stu-id="a8422-109">For example:</span></span>

- <span data-ttu-id="a8422-110">ギフト カードを使用して購入した場合、店舗ポリシーでは、新しいギフト カードに対してのみ払戻を処理するか、または店舗貸方を付与します。</span><span class="sxs-lookup"><span data-stu-id="a8422-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="a8422-111">現金を使用して購入した場合、払戻が可能なオプションは、現金、ギフト カード、および顧客アカウントですが、クレジット カードには対応していません。</span><span class="sxs-lookup"><span data-stu-id="a8422-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="a8422-112">返品ポリシーの有効化</span><span class="sxs-lookup"><span data-stu-id="a8422-112">Enable return policy</span></span>

<span data-ttu-id="a8422-113">チャネル返品ポリシー機能を有効にするには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="a8422-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="a8422-114">Dynamics 365 Commerce の**機能管理**ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="a8422-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="a8422-115">機能名のリストで、**チャネル返品ポリシーの有効化**機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="a8422-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="a8422-116">**直ちに有効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="a8422-117">返品ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a8422-117">Configure return policy</span></span>

<span data-ttu-id="a8422-118">小売店舗またはオンライン小売チャネルの返品ポリシーをコンフィギュレーションするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a8422-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="a8422-119">**Retail とコマース** \> **チャネル設定** \> **返品** \> **チャネル返品ポリシー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a8422-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="a8422-120">**新規**を選択して、新しい返品ポリシーのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8422-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="a8422-121">既存のテンプレートを使用するには、左ウィンドウでテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="a8422-122">新しいテンプレートには、チャネルに適用される際にポリシーを識別するのに役立つ名前と説明を追加します。</span><span class="sxs-lookup"><span data-stu-id="a8422-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="a8422-123">![新しい返品ポリシーの追加](media/Return-policy-page1.png "新しい返品ポリシーの追加")</span><span class="sxs-lookup"><span data-stu-id="a8422-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="a8422-124">**許可された払戻支払方法**セクションで、各支払方法に固有の**許可済**返品支払業者を定義します。</span><span class="sxs-lookup"><span data-stu-id="a8422-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="a8422-125">![支払方法の追加](media/Return-policy-page2.PNG "支払タイプごとに許可される支払方法の設定")</span><span class="sxs-lookup"><span data-stu-id="a8422-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="a8422-126">支払方法は、組織に対して設定される支払方法から派生したものです。</span><span class="sxs-lookup"><span data-stu-id="a8422-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="a8422-127">一覧表示された各支払方法に対して許可される返品業者タイプを追加すると、許可された返品業者タイプに対して確実に返品を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a8422-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="a8422-128">返品ポリシー テンプレートを、使用される店舗に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="a8422-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="a8422-129">**Retail チャネル** タブで**追加**を選択し、利用可能なチャネルを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="a8422-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="a8422-130">**組織ノードの選択**ダイアログ ボックスで、テンプレートが関連付けられている店舗、地域、および組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="a8422-131">各店舗に関連付けることができる店舗の返品ポリシー テンプレートは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="a8422-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="a8422-132">矢印ボタンを使用して、店舗、地域、または組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="a8422-133">ポリシーの有効日は、チャネルにポリシーが適用され、チャネル ジョブが実行される日付になります。</span><span class="sxs-lookup"><span data-stu-id="a8422-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="a8422-134">![組織ノード ダイアログ ボックスの選択](media/Return-policy-page3.PNG "組織ノード ダイアログ ボックスの選択")</span><span class="sxs-lookup"><span data-stu-id="a8422-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="a8422-135">**配送スケジュール** ページで、**1070** ジョブを実行して、POS でチャネル返品ポリシーを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a8422-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="a8422-136">POS のチャネル返品ポリシーのプレビュー</span><span class="sxs-lookup"><span data-stu-id="a8422-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="a8422-137">次の例のいずれかの手順に従って、POS で許容される返品業者タイプを表示します。</span><span class="sxs-lookup"><span data-stu-id="a8422-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="a8422-138">レジ担当者またはマネージャとして POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a8422-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="a8422-139">**シフトとドロワー**で、**仕訳帳の表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="a8422-140">返品の一部であるトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="a8422-141">返金する品目を選択し、支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="a8422-142">選択した支払業者が、許可された返品業者タイプのリストにある場合、レジ担当者はトランザクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="a8422-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="a8422-143">選択した支払業者が許可されない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8422-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="a8422-144">**請求額**を選択して、すべての許可された返品業者タイプのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="a8422-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="a8422-145">または</span><span class="sxs-lookup"><span data-stu-id="a8422-145">-or-</span></span>

1. <span data-ttu-id="a8422-146">レジ担当者またはマネージャとして POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a8422-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="a8422-147">**返品トランザクション**を選択し、バーコード スキャンまたは手動入力によってレシート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="a8422-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="a8422-148">返品の一部であるトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="a8422-149">返金する品目を選択し、支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8422-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="a8422-150">選択した支払業者が、許可された返品業者タイプのリストにある場合、レジ担当者はトランザクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="a8422-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="a8422-151">選択した支払業者が許可されない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8422-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="a8422-152">**請求額**を選択して、すべての許可された返品業者タイプのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="a8422-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="a8422-153">![不許可の払戻](media/Return-policy-page6.png "不許可の払戻タイプ")</span><span class="sxs-lookup"><span data-stu-id="a8422-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="a8422-154">![支払方法のリスト](media/Return-policy-page5.PNG "許可された払戻タイプ")</span><span class="sxs-lookup"><span data-stu-id="a8422-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
