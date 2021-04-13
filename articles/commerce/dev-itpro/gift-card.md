---
title: 外部ギフト カードのサポート
description: このトピックでは、Microsoft Dynamics 365 Commerce で現在利用できる外部ギフト カードのサポートについて説明します。
author: rubencdelgado
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.devlang: ''
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: ivanv
ms.search.validFrom: 2017-10-02
ms.dyn365.ops.version: Application update 4
ms.openlocfilehash: df50170f3ca00e5055a6f3683c4430aa160f000a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797221"
---
# <a name="support-for-external-gift-cards"></a><span data-ttu-id="07869-103">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="07869-103">Support for external gift cards</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07869-104">このトピックでは、コール センターや店舗での、Retail Modern point of sale (MPOS) における外部ギフトカードの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="07869-104">This topic explains how to set up external gift cards in Retail Modern point of sale (MPOS), the call center, and the storefront.</span></span>

<span data-ttu-id="07869-105">Microsoft Dynamics 365 Commerce では、*内部* および *外部* ギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="07869-105">Microsoft Dynamics 365 Commerce supports both *internal* and *external* gift cards.</span></span> <span data-ttu-id="07869-106">内部ギフト カードは Dynamics 365 Commerce で完全に管理されますが、外部ギフトカードはサード パーティによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="07869-106">Internal gift cards are managed entirely in Dynamics 365 Commerce, whereas external gift cards are administered by a third party.</span></span> <span data-ttu-id="07869-107">小売業者の工程が Microsoft Dynamics で完全に実行されている場合、内部ギフト カードが最適なソリューションである場合があります。</span><span class="sxs-lookup"><span data-stu-id="07869-107">If a retailer's operations are run entirely in Microsoft Dynamics, internal gift cards are sometimes the best solution.</span></span> <span data-ttu-id="07869-108">複数の国や地域にわたる複雑な企業、および複数の販売時点管理 (POS) システムでは、多くの場合サード パーティを使用してギフト カードの残高を管理し、それらのシステムでギフト カードを使用できるようにすることが最善です。</span><span class="sxs-lookup"><span data-stu-id="07869-108">For complex enterprises that span multiple countries or regions, and multiple point of sale (POS) systems, it's often best to use a third party to manage gift card balances and enable gift cards to be used across those systems.</span></span>

<span data-ttu-id="07869-109">他のカード支払タイプのサポートと同様に、使用される支払コネクタには外部ギフト カードのサポートが組み込まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-109">Like support for other card payment types, support for external gift cards must be built into the payment connector that is used.</span></span> <span data-ttu-id="07869-110">Adyen 向け標準支払コネクタでは、POS、コールセンター、および E コマース ストアフロントの SVS と Givex を通じて外部ギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="07869-110">The out-of-box payment connector for Adyen supports external gift cards through SVS and Givex in POS, the call center, and the e-commerce storefront.</span></span>

## <a name="external-gift-card-setup"></a><span data-ttu-id="07869-111">外部ギフト カードの設定</span><span class="sxs-lookup"><span data-stu-id="07869-111">External gift card setup</span></span>

> [!NOTE]
> <span data-ttu-id="07869-112">一部の設定手順では、デモ データが使用されることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="07869-112">Some setup steps assume that demo data is used.</span></span> <span data-ttu-id="07869-113">手順は、使用するデータセットによって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="07869-113">The steps might vary, depending on the dataset that is used.</span></span> <span data-ttu-id="07869-114">テスト コネクタは、サンドボックスのみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="07869-114">The test connector is for sandbox purposes only.</span></span> <span data-ttu-id="07869-115">テスト コネクタは UAT または実稼働環境ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="07869-115">The test connector is not supported for use in UAT or production environments.</span></span> 

### <a name="card-types"></a><span data-ttu-id="07869-116">カード タイプ</span><span class="sxs-lookup"><span data-stu-id="07869-116">Card types</span></span>

1. <span data-ttu-id="07869-117">**カード タイプ** を検索します。</span><span class="sxs-lookup"><span data-stu-id="07869-117">Search for **Card Types**.</span></span> 
2. <span data-ttu-id="07869-118">**新規** を選択し、次の値を追加して、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-118">Select **New**, add the following values, and then select **Save**.</span></span>

    | <span data-ttu-id="07869-119">フィールド名</span><span class="sxs-lookup"><span data-stu-id="07869-119">Field name</span></span>     | <span data-ttu-id="07869-120">Value</span><span class="sxs-lookup"><span data-stu-id="07869-120">Value</span></span>                  |
    |----------------|------------------------|
    | <span data-ttu-id="07869-121">カード ID</span><span class="sxs-lookup"><span data-stu-id="07869-121">Card ID</span></span>        | <span data-ttu-id="07869-122">**EXTGC**</span><span class="sxs-lookup"><span data-stu-id="07869-122">**EXTGC**</span></span>              |
    | <span data-ttu-id="07869-123">カード タイプ名</span><span class="sxs-lookup"><span data-stu-id="07869-123">Card type name</span></span> | <span data-ttu-id="07869-124">**外部ギフト カード**</span><span class="sxs-lookup"><span data-stu-id="07869-124">**External Gift Card**</span></span> |
    | <span data-ttu-id="07869-125">カード タイプ</span><span class="sxs-lookup"><span data-stu-id="07869-125">Card types</span></span>     | <span data-ttu-id="07869-126">**ギフト カード**</span><span class="sxs-lookup"><span data-stu-id="07869-126">**Gift card**</span></span>          |
    | <span data-ttu-id="07869-127">カード発行元</span><span class="sxs-lookup"><span data-stu-id="07869-127">Card issuer</span></span>    | <span data-ttu-id="07869-128">任意の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-128">Enter any description.</span></span> |

### <a name="card-numbers"></a><span data-ttu-id="07869-129">カード番号</span><span class="sxs-lookup"><span data-stu-id="07869-129">Card numbers</span></span>

1. <span data-ttu-id="07869-130">**カード タイプ** ページで、新しく作成されたギフト カードを選択し、**カード番号** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-130">On the **Card types** page, select the newly created gift card, and then select **Card numbers**.</span></span>
2. <span data-ttu-id="07869-131">外部ギフト カードで使用されるカード番号の範囲を指定し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-131">Specify the range of card numbers that should be used for external gift cards, and then select **Save**.</span></span>

<span data-ttu-id="07869-132">次の例では、カード番号の最初の 4 桁が **6036** の場合、このトピックの "カード タイプ" セクションで設定したギフト カードにカードがマップされます。</span><span class="sxs-lookup"><span data-stu-id="07869-132">In the following example, if the first four digits of a card number are **6036**, the card will be mapped to the gift card that you set up in the "Card types" section of this topic.</span></span>

| <span data-ttu-id="07869-133">フィールド名</span><span class="sxs-lookup"><span data-stu-id="07869-133">Field name</span></span>         | <span data-ttu-id="07869-134">Value</span><span class="sxs-lookup"><span data-stu-id="07869-134">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="07869-135">開始カード番号</span><span class="sxs-lookup"><span data-stu-id="07869-135">Card number from</span></span>   | <span data-ttu-id="07869-136">6000</span><span class="sxs-lookup"><span data-stu-id="07869-136">6000</span></span>  |
| <span data-ttu-id="07869-137">終了カード番号</span><span class="sxs-lookup"><span data-stu-id="07869-137">Card number to</span></span>     | <span data-ttu-id="07869-138">6999</span><span class="sxs-lookup"><span data-stu-id="07869-138">6999</span></span>  |
| <span data-ttu-id="07869-139">識別対象の桁</span><span class="sxs-lookup"><span data-stu-id="07869-139">Digits to identify</span></span> | <span data-ttu-id="07869-140">4</span><span class="sxs-lookup"><span data-stu-id="07869-140">4</span></span>     |

### <a name="payment-methods"></a><span data-ttu-id="07869-141">支払方法</span><span class="sxs-lookup"><span data-stu-id="07869-141">Payment methods</span></span>

1. <span data-ttu-id="07869-142">**支払方法** を検索して、**支払方法** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-142">Search for **Payment methods** to open the **Payment methods** page.</span></span>
2. <span data-ttu-id="07869-143">**新規** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="07869-143">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="07869-144">**支払方法** フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-144">In the **Payment method** field, enter **12**.</span></span>
    2. <span data-ttu-id="07869-145">**支払方法名** フィールドに、**外部ギフト カード** と入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-145">In the **Payment method name** field, enter **External Gift Card**.</span></span>
    3. <span data-ttu-id="07869-146">**既定の機能** フィールドで、**カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-146">In the **Default function** field, select **Card**.</span></span>
    4. <span data-ttu-id="07869-147">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-147">Select **Save**.</span></span>

## <a name="store-setup"></a><span data-ttu-id="07869-148">ストアの設定</span><span class="sxs-lookup"><span data-stu-id="07869-148">Store setup</span></span>

1. <span data-ttu-id="07869-149">**すべての店舗** を検索して、**すべての店舗** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-149">Search for **All stores** to open the **All stores** page.</span></span>
2. <span data-ttu-id="07869-150">一覧で、**サンフランシスコ** の店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-150">Select the **San Francisco** store in the list.</span></span>
3. <span data-ttu-id="07869-151">アクション ウィンドウの、**製品** タブの、**設定** グループで、**支払方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-151">On the Action Pane, on the **Set up** tab, in the **Set up** group, select **Payment methods**.</span></span>
4. <span data-ttu-id="07869-152">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-152">Select **New**.</span></span>
5. <span data-ttu-id="07869-153">**支払方法** フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-153">In the **Payment method** field, enter **12**.</span></span> <span data-ttu-id="07869-154">次に、**支払方法名** および **関数** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="07869-154">The **Payment method name** and **Function** fields should then be set automatically.</span></span>
6. <span data-ttu-id="07869-155">**一般** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-155">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="07869-156">**工程名** フィールドを **支払ギフト カード** に設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-156">Set the **Operation name** field to **Pay gift card**.</span></span>
    - <span data-ttu-id="07869-157">**コネクタ名** フィールドを **TestConnector** に設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-157">Set the **Connector name** field to **TestConnector**.</span></span>

9. <span data-ttu-id="07869-158">**転記** クイック タブで、**ギフト カード品目番号** フィールドを **0010** に設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-158">On the **Posting** FastTab, set the **Gift card item number** field to **0010**.</span></span>

    ![ギフト カード品目の番号フィールドの設定](./media/05_02.png)

10. <span data-ttu-id="07869-160">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-160">Select **Save**.</span></span>
11. <span data-ttu-id="07869-161">**カード設定** を選択し、**新規** を選択して、ギフト カードの支払方法をサンフランシスコ店舗の新規作成された外部ギフト カード支払方法にマップします。</span><span class="sxs-lookup"><span data-stu-id="07869-161">Select **Card setup**, and then select **New** to map the gift card payment method to the newly created external gift card payment method for the San Francisco store.</span></span>

## <a name="pos-setup"></a><span data-ttu-id="07869-162">POS の設定</span><span class="sxs-lookup"><span data-stu-id="07869-162">POS setup</span></span>

1. <span data-ttu-id="07869-163">Dynamics 365 Commerce バックオフィスで、**ハードウェア プロファイル** を検索して **POS ハードウェア プロファイル** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-163">In Dynamics 365 Commerce Headquarters, search for **Hardware profiles** to open the **POS hardware profile** page.</span></span>
2. <span data-ttu-id="07869-164">左のウィンドウで、**仮想** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-164">In the left pane, select **Virtual**.</span></span>
3. <span data-ttu-id="07869-165">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-165">Select **Edit**.</span></span>
4. <span data-ttu-id="07869-166">**EFT サービス** クイック タブの、**コネクタ** グリッドで、最初の入力 **TestConnector** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-166">On the **EFT service** FastTab, in the **Connectors** grid, select the first entry, **TestConnector**.</span></span>
5. <span data-ttu-id="07869-167">**サポートされる支払/入金タイプ** フィールドに、**GiftCard** を追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-167">In the **Supported Tender Types** field, add **GiftCard**.</span></span>

    ![サポートされている支払/入金タイプのリストへの GiftCard の追加](./media/01.png)

6. <span data-ttu-id="07869-169">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-169">Select **Save**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="07869-170">また、**新規** ボタンを使用して複数の支払コネクタを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="07869-170">You can also use the **New** button to create multiple payment connectors.</span></span> <span data-ttu-id="07869-171">この方法で、ソリューションに追加された複数のコネクタのサポートを利用できます。</span><span class="sxs-lookup"><span data-stu-id="07869-171">In this way, you can take advantage of the support for multiple connectors that has been added to the solution.</span></span> <span data-ttu-id="07869-172">異なる支払メソッドのために異なる支払コネクタを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="07869-172">You can then have different payment connectors for different payment methods.</span></span> <span data-ttu-id="07869-173">たとえば、1 つのコネクタですべてのクレジット カードを処理できますが、別のコネクタでギフト カードを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="07869-173">For example, all credit cards can be processed through one connector, but gift cards can be processed through a different connector.</span></span>

### <a name="update-the-button-grid"></a><span data-ttu-id="07869-174">ボタン グリッドの更新</span><span class="sxs-lookup"><span data-stu-id="07869-174">Update the button grid</span></span>

1. <span data-ttu-id="07869-175">**ボタン グリッド** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="07869-175">Go to the **Button grid** page.</span></span>
2. <span data-ttu-id="07869-176">ページの左側にあるナビゲーション バーで、**F2S1M** を検索してフィルター処理オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-176">In the navigation bar on the left side of the page, search for **F2S1M**, and select the filtered option.</span></span>
3. <span data-ttu-id="07869-177">アクション ウィンドウで、**デザイナー** を選択しボタン デザイナー アプリケーションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="07869-177">On the Action Pane, select **Designer** to download the button designer application.</span></span>
4. <span data-ttu-id="07869-178">グリッド デザイナーが表示されたら、空の (灰色) 領域を右クリックして、**新規作成ボタン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-178">When the grid designer appears, right-click on an empty (gray) area, and then select **New button**.</span></span>

    ![新しいボタン](./media/07.png)

5. <span data-ttu-id="07869-180">新しいボタンを右クリックし、**ボタン プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-180">Right-click the new button, and then select **Button properties**.</span></span>
6. <span data-ttu-id="07869-181">次のマトリックスに従って **アクション**、**支払タイプ**、および **ボタンのテキスト** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-181">Set the **Action**, **Payment type**, and **Text on button** properties according to the following matrix.</span></span>

    | <span data-ttu-id="07869-182">アクション</span><span class="sxs-lookup"><span data-stu-id="07869-182">Action</span></span>            | <span data-ttu-id="07869-183">支払タイプ</span><span class="sxs-lookup"><span data-stu-id="07869-183">Payment type</span></span>       | <span data-ttu-id="07869-184">ボタンのテキスト</span><span class="sxs-lookup"><span data-stu-id="07869-184">Text on button</span></span>        |
    |-------------------|--------------------|-----------------------|
    | <span data-ttu-id="07869-185">ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="07869-185">Issue gift card</span></span>   | <span data-ttu-id="07869-186">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="07869-186">External Gift Card</span></span> | <span data-ttu-id="07869-187">Ext Issue ギフト カード</span><span class="sxs-lookup"><span data-stu-id="07869-187">Ext Issue gift card</span></span>   |
    | <span data-ttu-id="07869-188">ギフト カードに追加</span><span class="sxs-lookup"><span data-stu-id="07869-188">Add to gift card</span></span>  | <span data-ttu-id="07869-189">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="07869-189">External Gift Card</span></span> | <span data-ttu-id="07869-190">ギフト カードに Ext 追加</span><span class="sxs-lookup"><span data-stu-id="07869-190">Ext Add to gift card</span></span>  |
    | <span data-ttu-id="07869-191">ギフト カード残高</span><span class="sxs-lookup"><span data-stu-id="07869-191">Gift card balance</span></span> | <span data-ttu-id="07869-192">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="07869-192">External Gift Card</span></span> | <span data-ttu-id="07869-193">Ext Gift カード残高</span><span class="sxs-lookup"><span data-stu-id="07869-193">Ext Gift card balance</span></span> |
    | <span data-ttu-id="07869-194">ギフト カードで支払う</span><span class="sxs-lookup"><span data-stu-id="07869-194">Pay gift card</span></span>     | <span data-ttu-id="07869-195">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="07869-195">External Gift Card</span></span> | <span data-ttu-id="07869-196">Ext Pay ギフト カード</span><span class="sxs-lookup"><span data-stu-id="07869-196">Ext Pay gift card</span></span>     |

    <span data-ttu-id="07869-197">完了したら、ボタンのレイアウトは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="07869-197">When you've finished, your button layout should resemble the following illustration.</span></span>

    ![完了したボタン レイアウト](./media/10.png)

7. <span data-ttu-id="07869-199">デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="07869-199">Close the designer.</span></span>
8. <span data-ttu-id="07869-200">**配送スケジュール** を検索します。</span><span class="sxs-lookup"><span data-stu-id="07869-200">Search for **Distribution Schedule**.</span></span>
9. <span data-ttu-id="07869-201">ページの左側にあるナビゲーション バーで、**1090**、**1115**、および **1070** を検索します。</span><span class="sxs-lookup"><span data-stu-id="07869-201">In the navigation bar on the left side of the page, search for **1090**, **1115**, and **1070**.</span></span>
10. <span data-ttu-id="07869-202">アクション ウィンドウで、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-202">On the Action Pane, select **Run now**.</span></span>
11. <span data-ttu-id="07869-203">**ダウンロード セッション** を検索してジョブのステータスを確認してください。</span><span class="sxs-lookup"><span data-stu-id="07869-203">Check the status of the job by searching for **Download sessions**.</span></span>
12. <span data-ttu-id="07869-204">すべてのジョブの横に **適用済** が表示されるまで待ってから、ブラウザーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="07869-204">Wait until **Applied** appears next to all the jobs, and then close the browser.</span></span>

    > [!NOTE]
    > <span data-ttu-id="07869-205">店舗にある Retail Commerce Scale Unit (RCSU) を使用している場合は、IIS リセットを実行してキャッシュをクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-205">If you are using Retail Commerce Scale Unit (RCSU) that is located in the store, you need to perform an IIS reset to clear the cache.</span></span> <span data-ttu-id="07869-206">これは IIS アプリケーションから実行するか、または管理者コマンド プロンプト ウィンドウを開いて `iisreset` を入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-206">You can either do this through the IIS application or open an admin Command Prompt window and enter `iisreset`.</span></span> <span data-ttu-id="07869-207">それ以外の場合、RCSU が更新されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="07869-207">Otherwise, wait for the RCSU to be updated.</span></span>

## <a name="configure-and-test-modern-pos"></a><span data-ttu-id="07869-208">Modern POS のコンフィギュレーションおよびテスト</span><span class="sxs-lookup"><span data-stu-id="07869-208">Configure and test Modern POS</span></span>

1. <span data-ttu-id="07869-209">Modern POS (MPOS) アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="07869-209">Start the Modern POS (MPOS) application.</span></span>
2. <span data-ttu-id="07869-210">標準の資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="07869-210">Sign in by using the standard credentials.</span></span>
3. <span data-ttu-id="07869-211">メッセージが表示されたら、**ドロワー以外の操作の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-211">When you're prompted, select **Perform a non-drawer operation**.</span></span>
4. <span data-ttu-id="07869-212">メイン画面で、**ハードウェア ステーションの選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-212">On the main screen, select **Select hardware station**.</span></span>
5. <span data-ttu-id="07869-213">ページの右側にあるバーで、**管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-213">On the bar on the right side of the page, select **Manage**.</span></span>
6. <span data-ttu-id="07869-214">**仮想周辺機器** をオンにし、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-214">Turn on **Virtual Peripherals**, and then select **OK**.</span></span>
7. <span data-ttu-id="07869-215">**使用可能なペアリング済ステーション** フィールドで、**仮想周辺機器** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-215">In the **Available paired stations** field, select **Virtual Peripherals**.</span></span>
8. <span data-ttu-id="07869-216">新しいシフトを開くか、非ドロワー操作を実行するように求められます。</span><span class="sxs-lookup"><span data-stu-id="07869-216">You're prompted to either open a new shift or perform non-drawer operations.</span></span> <span data-ttu-id="07869-217">新しいシフトを開くことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="07869-217">You can now open a new shift.</span></span>
9. <span data-ttu-id="07869-218">メイン画面で、**現在のトランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-218">On the main screen, select **Current transaction**.</span></span>
10. <span data-ttu-id="07869-219">**ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-219">Select **Gift cards**.</span></span>
11. <span data-ttu-id="07869-220">**Ext Issue ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-220">Select **Ext Issue gift card**.</span></span>
12. <span data-ttu-id="07869-221">**9** で始まる数を入力し、次に金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="07869-221">Enter a number that starts with **9**, and then provide an amount.</span></span>
13. <span data-ttu-id="07869-222">品目がカートに追加された後、現金またはカードを使用して支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="07869-222">After items are added to the cart, you can pay by using cash or a card.</span></span>

<span data-ttu-id="07869-223">外部ギフト カードのサポートを示すためにテスト コネクタを使用する場合は、カード番号 **61234** を使用して支払を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-223">When you use the test connector to demonstrate support for external gift cards, you should use card number **61234** to make payments.</span></span> <span data-ttu-id="07869-224">個人識別番号 (PIN) を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="07869-224">You won't be prompted for a personal identification number (PIN).</span></span> <span data-ttu-id="07869-225">テスト コネクタは、生産では **決して** 使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="07869-225">The test connector should **never** be used in production.</span></span>

## <a name="external-gift-cards-for-the-call-center-and-storefront"></a><span data-ttu-id="07869-226">コール センターおよびストアフロントの外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="07869-226">External gift cards for the call center and storefront</span></span>

> [!NOTE]
> <span data-ttu-id="07869-227">コール センターおよびストアフロントの外部ギフト カード サポートは、**機能管理** ワークスペースで有効になっています。</span><span class="sxs-lookup"><span data-stu-id="07869-227">External gift card support for call center and storefront is enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="07869-228">**オムニ チャネル支払** を有効にし、**詳細な外部ギフト カードの有効** を有効をにします。</span><span class="sxs-lookup"><span data-stu-id="07869-228">Enable **Omni-channel payments**, then enable **Enable advanced external gift card**.</span></span> <span data-ttu-id="07869-229">ストアフロントで外部ギフト カードを設定するのに必要な追加手順については、[eコマース デジタル ギフト カード](../digital-gift-cards.md)専用のドキュメント記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07869-229">For additional steps required to set up external gift cards in the storefront, please visit the docs article dedicated to  [E-commerce digital gift cards](../digital-gift-cards.md).</span></span> 

### <a name="tokenization"></a><span data-ttu-id="07869-230">トークン化</span><span class="sxs-lookup"><span data-stu-id="07869-230">Tokenization</span></span>

<span data-ttu-id="07869-231">コール センターおよびストアフロントの外部ギフト カードに対する標準実装および支払ソフトウェア開発キット (SDK) のサポートには、トークン化が必要です。</span><span class="sxs-lookup"><span data-stu-id="07869-231">The out-of-box implementation and Payments software development kit (SDK) support for external gift cards in the call center and storefront requires tokenization.</span></span> <span data-ttu-id="07869-232">外部ギフト カードが処理される際、トークンが実際のギフト カード番号を参照するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="07869-232">When external gift cards are processed, tokens are used to refer to the actual gift card number.</span></span> <span data-ttu-id="07869-233">トークンなしでは外部ギフト カードの処理が正しく機能しない可能性があるため、これはサード パーティ実装では重要です。</span><span class="sxs-lookup"><span data-stu-id="07869-233">This is important for 3rd party implementations because without tokens, external gift card processing may not function correctly.</span></span> <span data-ttu-id="07869-234">たとえば、ギフト カードの支払いが注文に追加された際にキャプチャされたが、注文の作成中に問題が発生した場合、ギフト カードの支払いは、実際のギフト カード番号ではなく、トランザクション自体への参照 (トークン) を使用して取り消されます。</span><span class="sxs-lookup"><span data-stu-id="07869-234">For example, if a gift card payment is captured when it's added to an order, but an issue occurs during order creation, the gift card payment will be reversed using references (tokens) to the transaction itself, not using the actual gift card number.</span></span> 

### <a name="purchases-and-refunds"></a><span data-ttu-id="07869-235">購入と払戻</span><span class="sxs-lookup"><span data-stu-id="07869-235">Purchases and refunds</span></span>

<span data-ttu-id="07869-236">外部ギフト カードが購入に使用される場合、ギフト カードの支払/入金明細行は前払として保存されます。</span><span class="sxs-lookup"><span data-stu-id="07869-236">When an external gift card is used for a purchase, the tender line for the gift card is saved as a prepayment.</span></span> <span data-ttu-id="07869-237">したがって、注文の作成時に購入の資金が取得されます。</span><span class="sxs-lookup"><span data-stu-id="07869-237">Therefore, the funds for the purchase are captured when the order is created.</span></span>

<span data-ttu-id="07869-238">外部ギフト カードには払戻が適用されません。</span><span class="sxs-lookup"><span data-stu-id="07869-238">External gift cards aren't eligible for refunds.</span></span> <span data-ttu-id="07869-239">一部には、ユーザーが破棄したギフト カードの払戻を防ぐために、この制限が設けられています。</span><span class="sxs-lookup"><span data-stu-id="07869-239">In part, this limitation is in place to prevent a refund from being given for a gift card that the user has discarded.</span></span> <span data-ttu-id="07869-240">未処理の注文に外部ギフト カードが支払として含まれており、顧客が注文のキャンセルする場合、新しいギフト カードまたはその他の形式のクレジットを顧客に発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-240">If an unprocessed order includes an external gift card as payment, and the customer wants to cancel the order, a new gift card or some other form of credit must be issued to the customer.</span></span>

<span data-ttu-id="07869-241">注文の一部として発行されるギフト カードの明細行は、フルフィルメント前にキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="07869-241">Gift cards lines that are issued as part of an order can be canceled before fulfillment.</span></span>

### <a name="issuing-gift-cards-through-fulfillment"></a><span data-ttu-id="07869-242">フルフィルメントによるギフトカードの発行</span><span class="sxs-lookup"><span data-stu-id="07869-242">Issuing gift cards through fulfillment</span></span>

<span data-ttu-id="07869-243">現物のギフト カードおよび仮想ギフト カードには、特徴的なフルフィルメント方法があります。</span><span class="sxs-lookup"><span data-stu-id="07869-243">Physical gift cards and virtual gift cards have distinct fulfillment methods.</span></span>

<span data-ttu-id="07869-244">現物ギフト カードは、**出荷** タイプの荷渡方法にマップされるギフト カードです。</span><span class="sxs-lookup"><span data-stu-id="07869-244">Physical gift cards are gift cards that are mapped to a mode of delivery of the **Shipping** type.</span></span> <span data-ttu-id="07869-245">注文処理の一部としてギフト カード プロバイダーを通じて直接発行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-245">They must be issued directly through the gift card provider as part of order processing.</span></span> <span data-ttu-id="07869-246">その後、ピッキング リスト登録プロセスの一部として、ギフト カード番号を注文明細行にマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-246">The gift card number must then be mapped to the order line as part of the pick list registration process.</span></span> <span data-ttu-id="07869-247">次に、マスクされたギフト カード番号が注文明細行に再保存されます。</span><span class="sxs-lookup"><span data-stu-id="07869-247">Next, the masked gift card number is saved back to the order line.</span></span> <span data-ttu-id="07869-248">発行されるギフト カードはその後、注文請求の一部として有効化されます。</span><span class="sxs-lookup"><span data-stu-id="07869-248">The gift card that is issued is then activated as part of order invoicing.</span></span>

<span data-ttu-id="07869-249">仮想ギフト カードは、注文請求の一部として発行されます。</span><span class="sxs-lookup"><span data-stu-id="07869-249">Virtual gift cards are issued as part of order invoicing.</span></span> <span data-ttu-id="07869-250">ギフト カードの明細行が **梱包済** としてマークされている場合、発行の対象となります。</span><span class="sxs-lookup"><span data-stu-id="07869-250">When a gift card line is marked as **Packed**, it becomes eligible to be issued.</span></span> <span data-ttu-id="07869-251">仮想ギフト カードは、請求の一部として発行されます。</span><span class="sxs-lookup"><span data-stu-id="07869-251">Virtual gift cards are issued as part of invoicing.</span></span> <span data-ttu-id="07869-252">請求が発生すると、ギフト カード番号が支払コネクタを介してプロバイダーから取得されます。</span><span class="sxs-lookup"><span data-stu-id="07869-252">When invoicing occurs, the gift card number is obtained from the provider through the payment connector.</span></span> <span data-ttu-id="07869-253">その後、有効化されたギフト カードの番号が、ギフト カードの受信者に電子メールで送信されます。</span><span class="sxs-lookup"><span data-stu-id="07869-253">The number for the activated gift card is then sent to the gift card recipient via email.</span></span> <span data-ttu-id="07869-254">請求が発生すると、マスクされたギフト カード番号が注文明細行に再保存されます。</span><span class="sxs-lookup"><span data-stu-id="07869-254">When invoicing occurs, the masked gift card number is then saved back to the order line.</span></span>

### <a name="using-modes-of-delivery-for-gift-card-products-in-the-call-center-and-e-commerce"></a><span data-ttu-id="07869-255">コール センターおよび E コマースでのギフト カード製品の荷渡方法の使用</span><span class="sxs-lookup"><span data-stu-id="07869-255">Using modes of delivery for gift card products in the call center and e-commerce</span></span>

<span data-ttu-id="07869-256">コール センターおよびストアフロント チャネルでは、POS とは異なり、ギフト カードの発行には専用の操作は使用されません。</span><span class="sxs-lookup"><span data-stu-id="07869-256">In the call center and storefront channels, unlike in POS, a dedication operation isn't used to issue gift cards.</span></span> <span data-ttu-id="07869-257">代わりに、ギフト カードは、トランザクションに明細行品目を追加することにより発行されます。</span><span class="sxs-lookup"><span data-stu-id="07869-257">Instead, gift cards are issued by adding a line item to a transaction.</span></span> <span data-ttu-id="07869-258">特に、E コマースおよびコール センターのギフト カード製品は、製品バリアントにマップされるか、標準製品としてモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="07869-258">Specifically, gift card products for e-commerce and the call center can be either mapped to product variants or modeled as standard products.</span></span>

<span data-ttu-id="07869-259">製品バリアントが使用される場合、ギフト カード注文の作成者はバリアントを選択するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="07869-259">If product variants are used, the person who creates the gift card order is prompted to select the variant.</span></span> <span data-ttu-id="07869-260">その後、該当する荷渡方法がその製品バリアントに対して使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="07869-260">The relevant mode of delivery will then be available for that product variant.</span></span>

<span data-ttu-id="07869-261">荷渡方法では、ギフト カードのタイプをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-261">Modes of delivery must support the type of gift card.</span></span> <span data-ttu-id="07869-262">たとえば、**現物** スタイルのギフト カード製品バリアントは、出荷に関連する荷渡方法にマップされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-262">For example, a gift card product variant of the **Physical** style must be mapped to a mode of delivery that is related to shipping.</span></span> <span data-ttu-id="07869-263">**電子メール** スタイルのギフト カード製品バリアントは、電子荷渡方法にマップされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-263">A gift card product variant of the **Email** style must be mapped to an electronic mode of delivery.</span></span> <span data-ttu-id="07869-264">電子荷渡方法は、**コマース パラメーター** ページの **顧客注文** タブで定義されます。</span><span class="sxs-lookup"><span data-stu-id="07869-264">The electronic mode of delivery is defined on the **Customer orders** tab of the **Commerce parameters** page.</span></span>

> [!NOTE]
> <span data-ttu-id="07869-265">現在、eコマースでサポートされているのは仮想ギフト カードのみです。</span><span class="sxs-lookup"><span data-stu-id="07869-265">Only virtual gift cards are currently supported in e-commerce.</span></span> <span data-ttu-id="07869-266">eコマースでの仮想ギフト カードの設定の詳細については、[eコマース デジタル ギフト カード ](../digital-gift-cards.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07869-266">For more details about setting up virtual gift cards in e-commerce, see [E-commerce digital gift cards](../digital-gift-cards.md).</span></span> 

## <a name="setup-for-the-call-center-and-storefront"></a><span data-ttu-id="07869-267">コール センターとストアフロントの設定</span><span class="sxs-lookup"><span data-stu-id="07869-267">Setup for the call center and storefront</span></span>

### <a name="payment-services-setup"></a><span data-ttu-id="07869-268">支払サービスの設定</span><span class="sxs-lookup"><span data-stu-id="07869-268">Payment services setup</span></span>

<span data-ttu-id="07869-269">バックオフィスの、**支払サービス** ページで、コール センターの支払サービス アカウントをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="07869-269">In the back office, on the **Payment services** page, configure the payment services account for the call center.</span></span> <span data-ttu-id="07869-270">各支払コネクタには、異なる設定手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="07869-270">Each payment connector requires different setup steps.</span></span> <span data-ttu-id="07869-271">コール センターで使用する支払サービスは、**既定** としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="07869-271">The payment service that the call center uses is marked as **Default**.</span></span>

## <a name="call-center-setup"></a><span data-ttu-id="07869-272">コール センターの設定</span><span class="sxs-lookup"><span data-stu-id="07869-272">Call center setup</span></span>

1. <span data-ttu-id="07869-273">**すべてのコール センター** を検索して、コール センター ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-273">Search for **All call centers** to open the call centers page.</span></span>
2. <span data-ttu-id="07869-274">一覧で、**ファッション コール センター** ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-274">Select the **Fashion call center** store in the list.</span></span>
3. <span data-ttu-id="07869-275">アクション ウィンドウの、**製品** タブの、**設定** グループで、**支払方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-275">On the Action Pane, on the **Set up** tab, in the **Set up** group, select **Payment methods**.</span></span>
4. <span data-ttu-id="07869-276">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-276">Select **New**.</span></span>
5. <span data-ttu-id="07869-277">**支払方法** フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-277">In the **Payment method** field, enter **12**.</span></span> <span data-ttu-id="07869-278">次に、**支払方法名** および **関数** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="07869-278">The **Payment method name** and **Function** fields will then be set automatically.</span></span>
6. <span data-ttu-id="07869-279">**一般** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-279">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="07869-280">**工程名** フィールドで、**支払ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-280">In the **Operation name** field, select **Pay gift card**.</span></span>
    - <span data-ttu-id="07869-281">**コネクタ名** フィールドで、**TestConnector** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-281">In the **Connector name** field, select **TestConnector**.</span></span>

9. <span data-ttu-id="07869-282">**転記** クイック タブで、**ギフト カード品目番号** フィールドを **0010** に設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-282">On the **Posting** FastTab, set the **Gift card item number** field to **0010**.</span></span>
10. <span data-ttu-id="07869-283">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-283">Select **Save**.</span></span>
11. <span data-ttu-id="07869-284">**カード設定** を選択してから、**新規** を選択して、ギフト カードの支払方法を **ファッション コール センター** の新規作成された外部ギフト カード支払方法にマップします。</span><span class="sxs-lookup"><span data-stu-id="07869-284">Select **Card setup**, and then select **New** to map the gift card payment method to the newly created external gift card payment method for the **Fashion call center**.</span></span>

## <a name="online-store-setup"></a><span data-ttu-id="07869-285">オンライン ストアの設定</span><span class="sxs-lookup"><span data-stu-id="07869-285">Online store setup</span></span>

1. <span data-ttu-id="07869-286">**オンライン ストア** を検索して、オンライン ストア ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-286">Search for **Online stores** to open the online stores page.</span></span>
2. <span data-ttu-id="07869-287">リストの **Fabrikam 拡張オンライン** ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-287">Select the **Fabrikam extended online** store in the list.</span></span>
3. <span data-ttu-id="07869-288">アクション ウィンドウの、**製品** タブの、**設定** グループで、**支払方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-288">On the Action Pane, on the **Set up** tab, in the **Set up** group, select **Payment methods**.</span></span>
4. <span data-ttu-id="07869-289">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-289">Select **New**.</span></span>
5. <span data-ttu-id="07869-290">**支払方法** フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-290">In the **Payment method** field, enter **12**.</span></span> <span data-ttu-id="07869-291">次に、**支払方法名** および **関数** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="07869-291">The **Payment method name** and **Function** fields will then be set automatically.</span></span>
6. <span data-ttu-id="07869-292">**一般** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-292">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="07869-293">**工程名** フィールドで、**支払ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-293">In the **Operation name** field, select **Pay gift card**.</span></span>
    - <span data-ttu-id="07869-294">**コネクタ名** フィールドで、**TestConnector** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-294">In the **Connector name** field, select **TestConnector**.</span></span>

9. <span data-ttu-id="07869-295">**転記** クイック タブで、**ギフト カード品目番号** フィールドを **0010** に設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-295">On the **Posting** FastTab, set the **Gift card item number** field to **0010**.</span></span>
10. <span data-ttu-id="07869-296">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-296">Select **Save**.</span></span>
11. <span data-ttu-id="07869-297">**カード設定** を選択してから、**新規** を選択して、ギフト カードの支払方法を **Fabrikam 拡張オンライン ストア** の新規作成された外部ギフト カード支払方法にマップします。</span><span class="sxs-lookup"><span data-stu-id="07869-297">Select **Card setup**, and then select **New** to map the gift card payment method to the newly created external gift card payment method for the **Fabrikam extended online store**.</span></span>

## <a name="online-store-payments-setup"></a><span data-ttu-id="07869-298">オンライン ストア支払いの設定</span><span class="sxs-lookup"><span data-stu-id="07869-298">Online store payments setup</span></span>

<span data-ttu-id="07869-299">外部のギフト カードの処理に Adyen を使用するようオンライン ストアの支払口座をコンフィギュレーションするには、Adyen コネクタ用ドキュメントの [eコマース設定セクション](adyen-connector.md?tabs=8-1-3#e-commerce)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07869-299">To configure the payment accounts for your online store to use Adyen for external gift card processing, please refer to the [e-Commerce setup section](adyen-connector.md?tabs=8-1-3#e-commerce) of the documentation for the Adyen connector.</span></span> 

#### <a name="adyen-external-gift-card-setup"></a><span data-ttu-id="07869-300">Adyen 外部ギフト カードの設定</span><span class="sxs-lookup"><span data-stu-id="07869-300">Adyen external gift card setup</span></span>

<span data-ttu-id="07869-301">支払サービスの設定方法を示す例については、[Adyen 支払コネクタのドキュメント](adyen-connector.md?tabs=8-1-3) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07869-301">For an example that shows how to set up payment services, see the [documentation for the Adyen payment connector](adyen-connector.md?tabs=8-1-3).</span></span>

<span data-ttu-id="07869-302">コール センターとストアフロントに関しては、Adyen コネクタは次のギフト カードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="07869-302">For the call center and storefront, the Adyen connector supports the following gift cards.</span></span>

| <span data-ttu-id="07869-303">ブランド</span><span class="sxs-lookup"><span data-stu-id="07869-303">Brand</span></span>   | <span data-ttu-id="07869-304">ギフト カード タイプ</span><span class="sxs-lookup"><span data-stu-id="07869-304">Gift card type</span></span>   | <span data-ttu-id="07869-305">サポート</span><span class="sxs-lookup"><span data-stu-id="07869-305">Supported</span></span> | <span data-ttu-id="07869-306">アクティブ化</span><span class="sxs-lookup"><span data-stu-id="07869-306">Activation</span></span>       |
|---------|------------------|-----------|------------------|
| <span data-ttu-id="07869-307">SVS</span><span class="sxs-lookup"><span data-stu-id="07869-307">SVS</span></span>     | <span data-ttu-id="07869-308">現物</span><span class="sxs-lookup"><span data-stu-id="07869-308">Physical</span></span>         | <span data-ttu-id="07869-309">はい</span><span class="sxs-lookup"><span data-stu-id="07869-309">Yes</span></span>       | <span data-ttu-id="07869-310">手動</span><span class="sxs-lookup"><span data-stu-id="07869-310">Manually</span></span>         |
| <span data-ttu-id="07869-311">SVS</span><span class="sxs-lookup"><span data-stu-id="07869-311">SVS</span></span>     | <span data-ttu-id="07869-312">電子メール</span><span class="sxs-lookup"><span data-stu-id="07869-312">Email</span></span>            | <span data-ttu-id="07869-313">はい</span><span class="sxs-lookup"><span data-stu-id="07869-313">Yes</span></span>       | <span data-ttu-id="07869-314">プログラム化</span><span class="sxs-lookup"><span data-stu-id="07869-314">Programmatically</span></span> |
| <span data-ttu-id="07869-315">Givex</span><span class="sxs-lookup"><span data-stu-id="07869-315">Givex</span></span>   | <span data-ttu-id="07869-316">現物</span><span class="sxs-lookup"><span data-stu-id="07869-316">Physical</span></span>         | <span data-ttu-id="07869-317">はい</span><span class="sxs-lookup"><span data-stu-id="07869-317">Yes</span></span>       | <span data-ttu-id="07869-318">手動</span><span class="sxs-lookup"><span data-stu-id="07869-318">Manually</span></span>         |

> [!NOTE]
> <span data-ttu-id="07869-319">標準の Adyen コネクタでは、既定でギフト カードがコンフィギュレーションされません。</span><span class="sxs-lookup"><span data-stu-id="07869-319">In the out-of-box Adyen connector, gift cards are not configured by default.</span></span> <span data-ttu-id="07869-320">支払コネクタの商社プロパティでギフト カード プロバイダーを指定するには、[Adyen 支払コネクタのドキュメント](adyen-connector.md?tabs=8-1-3)の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="07869-320">To specify the gift card provider in the merchant properties of the payment connector, follow the instructions in the [documentation for the Adyen payment connector](adyen-connector.md?tabs=8-1-3).</span></span>

#### <a name="test-connector-external-gift-card-setup"></a><span data-ttu-id="07869-321">テスト コネクタの外部ギフト カードの設定</span><span class="sxs-lookup"><span data-stu-id="07869-321">Test connector external gift card setup</span></span>

<span data-ttu-id="07869-322">テスト コネクタの外部ギフト カードを設定するには、**支払サービス** ページで **Dyn オンライン** を選択してから、**サポートされている支払/入金タイプ** フィールドで、**借方** の後に **;GiftCard** を追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-322">To set up external gift cards for the test connector, on the **Payment services** page, select **Dyn Online**, and then, in the **Supported Tender Types** field, add **;GiftCard** after **Debit**.</span></span> <span data-ttu-id="07869-323">次に **クレジット カード タイプ** を選択し、ギフト カード支払方法に支払仕訳帳を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="07869-323">Then select **Credit card types**, and assign a payment journal to the gift card payment method.</span></span>

### <a name="gift-card-product-setup"></a><span data-ttu-id="07869-324">ギフト カード製品の設定</span><span class="sxs-lookup"><span data-stu-id="07869-324">Gift card product setup</span></span>

<span data-ttu-id="07869-325">次の手順では、製品マスターを使用して外部ギフト カードを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="07869-325">The following procedure shows how to set up an external gift card by using product masters.</span></span> <span data-ttu-id="07869-326">外部ギフト カードには、製品マスターは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="07869-326">Product masters aren't required for external gift cards.</span></span> <span data-ttu-id="07869-327">ただし、現物ギフト カードと仮想ギフト カードの両方を使用する場合に、製品マスターは役立ちます。</span><span class="sxs-lookup"><span data-stu-id="07869-327">However, they can be helpful when both physical and virtual gift cards are used.</span></span>

1. <span data-ttu-id="07869-328">**スタイル グループ** を検索して、**スタイル グループ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-328">Search for **Style groups** to open the **Style groups** page.</span></span>
2. <span data-ttu-id="07869-329">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-329">Select **New**.</span></span>
3. <span data-ttu-id="07869-330">名前 (たとえば、**ギフト**) および説明 (たとえば、**ギフト カード スタイル グループ**) を入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-330">Enter a name (for example, **Gift**) and a description (for example, **Gift card style group**).</span></span>
4. <span data-ttu-id="07869-331">使用可能なギフト カードのタイプに合うスタイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-331">Add styles to suit the types of gift cards that are available.</span></span> <span data-ttu-id="07869-332">たとえば、**現物** スタイルおよび **電子メール** スタイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-332">For example, add **Physical** and **Email** styles.</span></span>
5. <span data-ttu-id="07869-333">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="07869-333">Save your changes.</span></span>
6. <span data-ttu-id="07869-334">**製品マスター** を検索して、**製品マスター** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-334">Search for **Product masters** to open the **Product masters** page.</span></span>
7. <span data-ttu-id="07869-335">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-335">Select **New**.</span></span>
8. <span data-ttu-id="07869-336">製品番号 (たとえば、**ギフト**) を入力し、小売カテゴリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="07869-336">Enter a product number (for example, **Gift**), and assign a retail category.</span></span>
9. <span data-ttu-id="07869-337">**製品分析コード グループ** フィールドで、**スタイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-337">In the **Product dimension group** field, select **Style**.</span></span>
10. <span data-ttu-id="07869-338">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-338">Select **OK**.</span></span>
11. <span data-ttu-id="07869-339">製品マスターで、以前に作成したスタイル グループを選択します (**ギフト**)。</span><span class="sxs-lookup"><span data-stu-id="07869-339">In the product master, select the style group that you created earlier (**Gift**).</span></span>
12. <span data-ttu-id="07869-340">アクション ウィンドウの、**製品** タブの、**設定** グループで、**分析コード グループ** を選択してから、保管分析コード グループと追跡用分析コード グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="07869-340">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**, and then assign a storage dimension group and a tracking dimension group.</span></span>
13. <span data-ttu-id="07869-341">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-341">Select **Save**.</span></span>
14. <span data-ttu-id="07869-342">**製品バリアント** を選択し、**バリアント修正候補** を選択してから、必要に応じてギフト カード バリアント番号を編集します。</span><span class="sxs-lookup"><span data-stu-id="07869-342">Select **Product variants**, select **Variant suggestions**, and edit the gift card variant numbers as you require.</span></span>
15. <span data-ttu-id="07869-343">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-343">Select **Create**.</span></span>

    ![外部ギフト カードの製品バリアント](media/VariantSuggestions.png)

16. <span data-ttu-id="07869-345">**リリース製品** を選択し、**次へ** を 2 回選択し、会社 (たとえば、**USRT**) を選択してから、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-345">Select **Release products**, select **Next** two times, select a company (for example, **USRT**), and then select **Next**.</span></span> <span data-ttu-id="07869-346">最後に **次へ** を選択して、製品マスターをリリースします。</span><span class="sxs-lookup"><span data-stu-id="07869-346">Finally select **Next** to release the product master.</span></span>
17. <span data-ttu-id="07869-347">**荷渡方法** を検索して、**荷渡方法** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-347">Search for **Modes of delivery** to open the **Modes of delivery** page.</span></span>
18. <span data-ttu-id="07869-348">**電子** 荷渡方法を選択してから、**電子メール** ギフト カード バリアントを追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-348">Select the **Electronic** mode of delivery, and add the **Email** gift card variant.</span></span> <span data-ttu-id="07869-349">該当するコール センターおよびオンライン チャネルが含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="07869-349">Make sure that applicable call centers and online channels are included.</span></span>

    ![電子的方法による納品](media/EmailMoD.png)

19. <span data-ttu-id="07869-351">出荷の荷渡方法を選択してから、**現物** ギフト カード バリアントを追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-351">Select a shipping mode of delivery, and add the **Physical** gift card variant.</span></span>
20. <span data-ttu-id="07869-352">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-352">Select **Save**.</span></span>
21. <span data-ttu-id="07869-353">**配送モードの処理** を検索して、**配送モードの処理** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-353">Search for **Process delivery modes** to open the **Process delivery modes** dialog box.</span></span>
22. <span data-ttu-id="07869-354">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-354">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="07869-355">現在、ギフト カードは MPOS 顧客注文の作成または店舗内での受取に対してはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="07869-355">Gift cards aren't currently supported for MPOS customer order creation or for in-store pickup.</span></span>

23. <span data-ttu-id="07869-356">**カテゴリ別リリース済製品** を検索して、**リリース済製品の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-356">Search for **Released products by category** to open the **Released product details** page.</span></span>
24. <span data-ttu-id="07869-357">外部ギフト カード品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-357">Select the external gift card item.</span></span>
25. <span data-ttu-id="07869-358">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-358">Set the following values.</span></span>

    | <span data-ttu-id="07869-359">クイックタブ</span><span class="sxs-lookup"><span data-stu-id="07869-359">FastTab</span></span>           | <span data-ttu-id="07869-360">フィールド</span><span class="sxs-lookup"><span data-stu-id="07869-360">Field</span></span>               | <span data-ttu-id="07869-361">Value</span><span class="sxs-lookup"><span data-stu-id="07869-361">Value</span></span>                 |
    |-------------------|-------------------- |-----------------------|
    | <span data-ttu-id="07869-362">一般</span><span class="sxs-lookup"><span data-stu-id="07869-362">General</span></span>           | <span data-ttu-id="07869-363">品目モデル グループ</span><span class="sxs-lookup"><span data-stu-id="07869-363">Item model group</span></span>    | <span data-ttu-id="07869-364">MA\_Retail</span><span class="sxs-lookup"><span data-stu-id="07869-364">MA\_Retail</span></span>            |
    | <span data-ttu-id="07869-365">購買</span><span class="sxs-lookup"><span data-stu-id="07869-365">Purchase</span></span>          | <span data-ttu-id="07869-366">発注書単位</span><span class="sxs-lookup"><span data-stu-id="07869-366">Purchase order unit</span></span> | <span data-ttu-id="07869-367">ea</span><span class="sxs-lookup"><span data-stu-id="07869-367">ea</span></span>                    |
    | <span data-ttu-id="07869-368">販売</span><span class="sxs-lookup"><span data-stu-id="07869-368">Sell</span></span>              | <span data-ttu-id="07869-369">販売注文単位</span><span class="sxs-lookup"><span data-stu-id="07869-369">Sales order unit</span></span>    | <span data-ttu-id="07869-370">ea</span><span class="sxs-lookup"><span data-stu-id="07869-370">ea</span></span>                    |
    | <span data-ttu-id="07869-371">販売</span><span class="sxs-lookup"><span data-stu-id="07869-371">Sell</span></span>              | <span data-ttu-id="07869-372">価格調整を許可する</span><span class="sxs-lookup"><span data-stu-id="07869-372">Allow price adjust</span></span>  | <span data-ttu-id="07869-373">はい</span><span class="sxs-lookup"><span data-stu-id="07869-373">Yes</span></span>                   |
    | <span data-ttu-id="07869-374">在庫の管理</span><span class="sxs-lookup"><span data-stu-id="07869-374">Manage inventory</span></span>  | <span data-ttu-id="07869-375">在庫単位</span><span class="sxs-lookup"><span data-stu-id="07869-375">Inventory unit</span></span>      | <span data-ttu-id="07869-376">ea</span><span class="sxs-lookup"><span data-stu-id="07869-376">ea</span></span>                    |
    | <span data-ttu-id="07869-377">原価の管理</span><span class="sxs-lookup"><span data-stu-id="07869-377">Manage costs</span></span>      | <span data-ttu-id="07869-378">品目グループの天気</span><span class="sxs-lookup"><span data-stu-id="07869-378">Posting item group</span></span>  | <span data-ttu-id="07869-379">任意</span><span class="sxs-lookup"><span data-stu-id="07869-379">Any</span></span>                   |

26. <span data-ttu-id="07869-380">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-380">Select **Save**.</span></span>

<span data-ttu-id="07869-381">ストアフロントでは、店舗の品揃えにもギフト カードを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-381">For the storefront, the gift card must also be included in the storefront's assortment.</span></span> <span data-ttu-id="07869-382">詳細については、[品揃え管理](../assortments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07869-382">For more information, see [Assortment management](../assortments.md).</span></span>

> [!NOTE]
> <span data-ttu-id="07869-383">POS での外部ギフトカード設定に使用するギフトカード製品は、品目の変数を含む製品マスターを使用しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-383">The gift card product used for external gift card setup in POS should not use product masters with item variants.</span></span> <span data-ttu-id="07869-384">品目の変数に基づくギフトカードは、今まで通りPOSでの支払いや残高照会、キャッシュアウトに使用することができますが、発行の POS に関連付けられているギフトカード製品は標準の製品である必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-384">Gift cards based on item variants may still be used for payments, balance inquiries, and cash out in POS, but gift card products associated with the POS for issuance must be standard products.</span></span> 


### <a name="set-up-notification-emails-for-virtual-gift-cards"></a><span data-ttu-id="07869-385">仮想ギフトカードの通知電子メールの設定</span><span class="sxs-lookup"><span data-stu-id="07869-385">Set up notification emails for virtual gift cards</span></span>

<span data-ttu-id="07869-386">電子メール設定の詳細については、[電子メール機能のコンフィギュレーション](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/configure-email-functionality-in-microsoft-dynamics-ax) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07869-386">For information about email setup, see [Configure email functionality](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/configure-email-functionality-in-microsoft-dynamics-ax).</span></span>

<span data-ttu-id="07869-387">コマース用電子メール通知の設定方法の詳細については、[電子メール通知プロファイルの設定](../email-notification-profiles.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07869-387">For information about how to set up email notifications for Commerce, see [Set up an email notification profile](../email-notification-profiles.md).</span></span>

<span data-ttu-id="07869-388">電子メールで発行されるギフト カードの場合、**小売用電子メール通知タイプ** フィールドの値は **ギフト カードの発行** となります。</span><span class="sxs-lookup"><span data-stu-id="07869-388">For gift cards that are issued via email, the value of the **Retail email notification type** field is **Issue gift card**.</span></span>

### <a name="call-center-setup"></a><span data-ttu-id="07869-389">コール センターの設定</span><span class="sxs-lookup"><span data-stu-id="07869-389">Call center setup</span></span>

1. <span data-ttu-id="07869-390">**すべてのコール センター** を検索して、**コール センター** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-390">Search for **All call centers** to open the **Call center** page.</span></span>
2. <span data-ttu-id="07869-391">一覧で、コール センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-391">In the list, select a call center.</span></span>
3. <span data-ttu-id="07869-392">アクション ウィンドウの、**チャネル** タブの、**ユーザー** グループで、**チャネル ユーザー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-392">On the Action Pane, on the **Channel** tab, in the **Users** group, select **Channel users**.</span></span>
4. <span data-ttu-id="07869-393">ユーザーを追加し、**保存** を選択してから、**チャネル ユーザー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="07869-393">Add a user, select **Save**, and then close the **Channel users** page.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="07869-394">**顧客サービス** ページにアクセスして注文を作成する場合、ユーザーはコール センター ユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-394">Users must be call center users when they access the **Customer service** page and create orders.</span></span> <span data-ttu-id="07869-395">それ以外の場合は、コール センター機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="07869-395">Otherwise, call center capabilities won't be available.</span></span>

5. <span data-ttu-id="07869-396">**コール センター** ページに戻って 、アクション ウィンドウの、**設定** タブの、**設定** グループで、**支払方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-396">Back on the **Call center** page, on the Action Pane, on the **Set up** tab, in the **Set up** group, select **Payment methods**.</span></span>
6. <span data-ttu-id="07869-397">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-397">Select **New**.</span></span>
7. <span data-ttu-id="07869-398">**支払方法** フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-398">In the **Payment method** field, enter **12**.</span></span> <span data-ttu-id="07869-399">次に、**支払方法名** および **関数** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="07869-399">The **Payment method name** and **Function** fields should then be set automatically.</span></span>
8. <span data-ttu-id="07869-400">**一般** クイック タブで、外部ギフト カードに使用する必要があるコネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-400">On the **General** FastTab, select the connector that should be used for the external gift card.</span></span>
9. <span data-ttu-id="07869-401">**カード設定** を選択してから、**新規** を選択して、ギフト カードの支払方法を外部ギフト カード支払方法にマップします。</span><span class="sxs-lookup"><span data-stu-id="07869-401">Select **Card setup**, and then select **New** to map the gift card payment method to the external gift card payment method.</span></span>
10. <span data-ttu-id="07869-402">**転記** クイック タブで、外部ギフト カードの一般会計勘定を指定します。</span><span class="sxs-lookup"><span data-stu-id="07869-402">On the **Posting** FastTab, specify general ledger accounts for the external gift cards.</span></span> <span data-ttu-id="07869-403">デモ データでは、**112140** を一般会計勘定番号として使用できます。</span><span class="sxs-lookup"><span data-stu-id="07869-403">In demo data, **112140** can be used as the general ledger account number.</span></span>
11. <span data-ttu-id="07869-404">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-404">Select **Save**.</span></span>
12. <span data-ttu-id="07869-405">**カード設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-405">Select **Card setup**.</span></span>
13. <span data-ttu-id="07869-406">**新規** を選択し、前に作成した外部ギフト カードを選択してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-406">Select **New**, select the external gift card that you created earlier, and then select **Save**.</span></span>
14. <span data-ttu-id="07869-407">**カード設定** ページを閉じ、**支払方法** ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="07869-407">Close the **Card setup** page, and refresh the **Payment methods** page.</span></span>
15. <span data-ttu-id="07869-408">外部ギフト カードの支払方法を選択してから、**一般** クイック タブの、**ギフト カード アカウント** セクションの、**コネクタ名** フィールドに、**TestConnector** コネクタを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="07869-408">Select the external gift card payment method, and then, on the **General** FastTab, in the **Gift card account** section, in the **Connector name** field, assign the **TestConnector** connector.</span></span>
16. <span data-ttu-id="07869-409">**転記** クイック タブで、ギフト カード品目番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="07869-409">On the **Posting** FastTab, assign the gift card item number.</span></span>
17. <span data-ttu-id="07869-410">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-410">Select **Save**.</span></span>
18. <span data-ttu-id="07869-411">**カード設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-411">Select **Card setup**.</span></span>
19. <span data-ttu-id="07869-412">内部ギフト カードの **カード設定** ページには 2 つの追加のコンフィギュレーション フィールドが含まれるようになりました: **有効期限を確認する** および **PIN が必要**。</span><span class="sxs-lookup"><span data-stu-id="07869-412">The **Card setup** page for the internal gift card now includes two additional configuration fields: **Check expiration date** and **PIN required**.</span></span> <span data-ttu-id="07869-413">これらのフィールドは、外部ギフト カード プロバイダーの必要に応じて設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-413">Set these fields as required by the external gift card provider.</span></span>

### <a name="issue-external-gift-cards-in-the-call-center"></a><span data-ttu-id="07869-414">コール センターでの外部ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="07869-414">Issue external gift cards in the call center</span></span>

1. <span data-ttu-id="07869-415">コール センター ユーザーとして、**顧客サービス** を検索して **顧客サービス** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-415">As a call center user, search for **Customer service** to open the **Customer service** page.</span></span>
2. <span data-ttu-id="07869-416">**検索** 機能を使用して顧客を追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-416">Add a customer by using the **Search** function.</span></span>
3. <span data-ttu-id="07869-417">**新しい販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-417">Select **New sales order**.</span></span>
4. <span data-ttu-id="07869-418">**ヘッダー** を選択し、有効な荷渡方法を追加します。</span><span class="sxs-lookup"><span data-stu-id="07869-418">Select **Header**, and add a valid mode of delivery.</span></span>
5. <span data-ttu-id="07869-419">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-419">Select **Lines**.</span></span>
6. <span data-ttu-id="07869-420">**品目番号** フィールドで、ギフト カード品目番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="07869-420">In the **Item number** field, specify the gift card item number.</span></span>
7. <span data-ttu-id="07869-421">**バリアント番号** フィールドで、製品マスターを使用している場合のバリアント番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="07869-421">In the **Variant number** field, specify the variant number if you're using a product master.</span></span>
8. <span data-ttu-id="07869-422">**単位** フィールドで、ギフト カードの単価を指定します。</span><span class="sxs-lookup"><span data-stu-id="07869-422">In the **Unit price** field, specify the unit price for the gift card.</span></span>

    > [!NOTE]
    > <span data-ttu-id="07869-423">荷渡方法がバリアントにマップされており、任意のギフトカードに対して **電子** 荷渡方法が指定されている場合は、ギフト カード タイプは、**梱包** タブで自動的に **電子メール** に設定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="07869-423">If modes of delivery are mapped to variants, and if **Electronic** modes of delivery are specified for any gift cards, the gift card type should automatically be set to **Email** on the **Packing** tab.</span></span>

9. <span data-ttu-id="07869-424">**明細行の詳細** クイック タブの、**梱包** タブで、次のいずれかの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="07869-424">On the **Line details** FastTab, on the **Packing** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="07869-425">仮想ギフト カードに関しては、**購入担当者の名前**、**購入担当電子メール**、**受取人の名前**、**受取人電子メール**、および **ギフト メッセージ** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-425">For virtual gift cards, set the **Buyer name**, **Buyer email**, **Recipient name**, **Recipient email**, and **Gift message** fields.</span></span>
    - <span data-ttu-id="07869-426">現物ギフト カードに関しては、**購入担当者の名前**、**受取人の名前**、および **ギフト メッセージ** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="07869-426">For physical gift cards, set the **Buyer name**, **Recipient name**, and **Gift message** fields.</span></span>

10. <span data-ttu-id="07869-427">**価格と割引** タブの、**理由コード** フィールドで、価格変更の理由を指定します。</span><span class="sxs-lookup"><span data-stu-id="07869-427">On the **Price and discount** tab, in the **Reason code** field, specify the reason for the price override.</span></span>
11. <span data-ttu-id="07869-428">**完了** を選択し、支払を追加して、注文を送信します。</span><span class="sxs-lookup"><span data-stu-id="07869-428">Select **Complete**, add a payment, and submit the order.</span></span>

### <a name="pay-by-using-external-gift-cards-in-the-call-center"></a><span data-ttu-id="07869-429">コール センターでの外部ギフト カードを使用する支払</span><span class="sxs-lookup"><span data-stu-id="07869-429">Pay by using external gift cards in the call center</span></span>

1. <span data-ttu-id="07869-430">コール センター ユーザーとして、注文を作成し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-430">As a call center user, create an order, and select **Complete**.</span></span>
2. <span data-ttu-id="07869-431">**支払** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-431">On the **Payments** FastTab, select **Add**.</span></span>
3. <span data-ttu-id="07869-432">外部ギフト カードの支払方法を選択し、該当する場合は番号と PIN を入力します。</span><span class="sxs-lookup"><span data-stu-id="07869-432">Select the external gift card payment method, and enter the number and PIN, if applicable.</span></span> <span data-ttu-id="07869-433">テスト コネクタの場合、**61234** を番号として使用でき、PIN は検証されません。</span><span class="sxs-lookup"><span data-stu-id="07869-433">For the test connector, **61234** can be used as the number, and the PIN isn't validated.</span></span>
4. <span data-ttu-id="07869-434">割合または支払金額を使用して、支払金額を定義します。</span><span class="sxs-lookup"><span data-stu-id="07869-434">Use a percentage amount or a payment amount to define the payment amount.</span></span>

    ![コール センターでの外部ギフト カードの支払](media/PayinCallCenter.png)

5. <span data-ttu-id="07869-436">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07869-436">Select **OK**.</span></span>
6. <span data-ttu-id="07869-437">**送信** を選択して、注文を完了します。</span><span class="sxs-lookup"><span data-stu-id="07869-437">Select **Submit** to complete the order.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="07869-438">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="07869-438">Troubleshooting</span></span> 

### <a name="issue-an-error-occurs-when-you-start-the-hardwarestationconfigurationutility-program"></a><span data-ttu-id="07869-439">問題: HardwareStationConfigurationUtility プログラムの起動時にエラーが発生します</span><span class="sxs-lookup"><span data-stu-id="07869-439">Issue: An error occurs when you start the HardwareStationConfigurationUtility program</span></span>

1. <span data-ttu-id="07869-440">上位のコマンド プロンプトからは、メモ帳で **HardwareStationConfigurationUtility.exe.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-440">From an elevated command prompt, open the **HardwareStationConfigurationUtility.exe.config** file in Notepad.</span></span>
2. <span data-ttu-id="07869-441">ファイルで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="07869-441">In the file, follow these steps:</span></span>

    1. <span data-ttu-id="07869-442">**DataServiceUrl** 値を適切な Commerce Scale Unit URL に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="07869-442">Replace the **DataServiceUrl** value with the correct Commerce Scale Unit URL.</span></span>
    2. <span data-ttu-id="07869-443">**AADLogonUrl** の値が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="07869-443">Verify that the **AADLogonUrl** value is correct.</span></span>

3. <span data-ttu-id="07869-444">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="07869-444">Save and close the file.</span></span>
4. <span data-ttu-id="07869-445">ユーティリティを再起動します。</span><span class="sxs-lookup"><span data-stu-id="07869-445">Restart the utility.</span></span>

### <a name="issue-a-token-error-occurs-when-you-try-to-pair-virtual-peripherals"></a><span data-ttu-id="07869-446">問題: 仮想周辺機器をペアリングしようとしたときにトークン エラーが発生します</span><span class="sxs-lookup"><span data-stu-id="07869-446">Issue: A token error occurs when you try to pair virtual peripherals</span></span>

1. <span data-ttu-id="07869-447">MPOS を終了します。</span><span class="sxs-lookup"><span data-stu-id="07869-447">Exit MPOS.</span></span>
2. <span data-ttu-id="07869-448">**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package** に移動します。</span><span class="sxs-lookup"><span data-stu-id="07869-448">Go to **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package**.</span></span>
3. <span data-ttu-id="07869-449">上位のコマンド プロンプトからは、メモ帳で **Web.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="07869-449">From an elevated command prompt, open the **Web.config** file in Notepad.</span></span>
4. <span data-ttu-id="07869-450">**RetailServer** 値を適切な Commerce Scale Unit 値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="07869-450">Replace the **RetailServer** value with the correct Commerce Scale Unit value.</span></span>
5. <span data-ttu-id="07869-451">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="07869-451">Save and close the file.</span></span>
6. <span data-ttu-id="07869-452">MPOS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="07869-452">Restart MPOS.</span></span>
7. <span data-ttu-id="07869-453">問題が解消しない場合は、MPOS を終了し、タスク マネージャーを使用して、実行中の dllhost.exe インスタンスを終了させ、インターネット インフォメーション サービス (IIS) のリセットを別に行います。</span><span class="sxs-lookup"><span data-stu-id="07869-453">If the issue persists, exit MPOS, use Task Manager to end any instances of dllhost.exe that are running, and then do another reset of Internet Information Services (IIS).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]