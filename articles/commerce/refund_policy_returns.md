---
title: チャネルの返品と払戻のポリシーを作成および更新する
description: このトピックでは、チャネルに対する返品と払戻のポリシーを設定する方法について説明します。
author: ShalabhjainMSFT
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: e23291130d55fdfb5c2e2077b78c221866d72c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792078"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="237db-103">チャネルの返品と払戻のポリシーを作成および更新する</span><span class="sxs-lookup"><span data-stu-id="237db-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="237db-104">Dynamics 365 Commerce のチャネルの返品ポリシーでは、小売業者は、販売時点管理 (POS) デバイスの返品の処理のために支払業者が許可される適用を設定できます。</span><span class="sxs-lookup"><span data-stu-id="237db-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="237db-105">このトピックでは、チャネルに対する返品と払戻のポリシーを設定する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="237db-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="237db-106">ポリシーの範囲は、チャネルに対して許可される支払業者を設定することに制限されています。</span><span class="sxs-lookup"><span data-stu-id="237db-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="237db-107">"許可済"リストは、購入に使用される支払方法に基づきます。</span><span class="sxs-lookup"><span data-stu-id="237db-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="237db-108">例:</span><span class="sxs-lookup"><span data-stu-id="237db-108">For example:</span></span>

- <span data-ttu-id="237db-109">ギフト カードを使用して購入した場合、店舗ポリシーでは、新しいギフト カードに対してのみ払戻を処理するか、または店舗貸方を付与します。</span><span class="sxs-lookup"><span data-stu-id="237db-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="237db-110">現金を使用して購入した場合、払戻が可能なオプションは、現金、ギフト カード、および顧客アカウントですが、クレジット カードには対応していません。</span><span class="sxs-lookup"><span data-stu-id="237db-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="237db-111">返品ポリシーの有効化</span><span class="sxs-lookup"><span data-stu-id="237db-111">Enable return policy</span></span>

<span data-ttu-id="237db-112">チャネル返品ポリシー機能を有効にするには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="237db-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="237db-113">Dynamics 365 Commerce の **機能管理** ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="237db-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="237db-114">機能名のリストで、**チャネル返品ポリシーの有効化** 機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="237db-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="237db-115">**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="237db-116">返品ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="237db-116">Configure return policy</span></span>

<span data-ttu-id="237db-117">小売店舗またはオンライン小売チャネルの返品ポリシーをコンフィギュレーションするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="237db-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="237db-118">**Retail とコマース** \> **チャネル設定** \> **返品** \> **チャネル返品ポリシー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="237db-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="237db-119">**新規** を選択して、新しい返品ポリシーのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="237db-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="237db-120">既存のテンプレートを使用するには、左ウィンドウでテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="237db-121">新しいテンプレートには、チャネルに適用される際にポリシーを識別するのに役立つ名前と説明を追加します。</span><span class="sxs-lookup"><span data-stu-id="237db-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="237db-122">![新しい返品ポリシーの追加](media/Return-policy-page1.png "新しい返品ポリシーの追加")</span><span class="sxs-lookup"><span data-stu-id="237db-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="237db-123">**許可された払戻支払方法** セクションで、各支払方法に固有の **許可済** 返品支払業者を定義します。</span><span class="sxs-lookup"><span data-stu-id="237db-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="237db-124">![支払方法の追加](media/Return-policy-page2.PNG "支払タイプごとに許可される支払方法の設定")</span><span class="sxs-lookup"><span data-stu-id="237db-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="237db-125">支払方法は、組織に対して設定される支払方法から派生したものです。</span><span class="sxs-lookup"><span data-stu-id="237db-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="237db-126">一覧表示された各支払方法に対して許可される返品業者タイプを追加すると、許可された返品業者タイプに対して確実に返品を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="237db-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="237db-127">返品ポリシー テンプレートを、使用される店舗に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="237db-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="237db-128">**Retail チャネル** タブで **追加** を選択し、利用可能なチャネルを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="237db-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="237db-129">**組織ノードの選択** ダイアログ ボックスで、テンプレートが関連付けられている店舗、地域、および組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="237db-130">各店舗に関連付けることができる店舗の返品ポリシー テンプレートは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="237db-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="237db-131">矢印ボタンを使用して、店舗、地域、または組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="237db-132">ポリシーの有効日は、チャネルにポリシーが適用され、チャネル ジョブが実行される日付になります。</span><span class="sxs-lookup"><span data-stu-id="237db-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="237db-133">![組織ノード ダイアログ ボックスの選択](media/Return-policy-page3.PNG "組織ノード ダイアログ ボックスの選択")</span><span class="sxs-lookup"><span data-stu-id="237db-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="237db-134">**配送スケジュール** ページで、**1070** ジョブを実行して、POS でチャネル返品ポリシーを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="237db-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="237db-135">POS のチャネル返品ポリシーのプレビュー</span><span class="sxs-lookup"><span data-stu-id="237db-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="237db-136">次の例のいずれかの手順に従って、POS で許容される返品業者タイプを表示します。</span><span class="sxs-lookup"><span data-stu-id="237db-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="237db-137">レジ担当者またはマネージャとして POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="237db-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="237db-138">**シフトとドロワー** で、**仕訳帳の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="237db-139">返品の一部であるトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="237db-140">返金する品目を選択し、支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="237db-141">選択した支払業者が、許可された返品業者タイプのリストにある場合、レジ担当者はトランザクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="237db-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="237db-142">選択した支払業者が許可されない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="237db-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="237db-143">**請求額** を選択して、すべての許可された返品業者タイプのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="237db-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="237db-144">または</span><span class="sxs-lookup"><span data-stu-id="237db-144">-or-</span></span>

1. <span data-ttu-id="237db-145">レジ担当者またはマネージャとして POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="237db-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="237db-146">**返品トランザクション** を選択し、バーコード スキャンまたは手動入力によってレシート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="237db-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="237db-147">返品の一部であるトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="237db-148">返金する品目を選択し、支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="237db-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="237db-149">選択した支払業者が、許可された返品業者タイプのリストにある場合、レジ担当者はトランザクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="237db-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="237db-150">選択した支払業者が許可されない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="237db-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="237db-151">**請求額** を選択して、すべての許可された返品業者タイプのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="237db-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="237db-152">![不許可の払戻](media/Return-policy-page6.png "不許可の払戻タイプ")</span><span class="sxs-lookup"><span data-stu-id="237db-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="237db-153">![支払方法のリスト](media/Return-policy-page5.PNG "許可された払戻タイプ")</span><span class="sxs-lookup"><span data-stu-id="237db-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
