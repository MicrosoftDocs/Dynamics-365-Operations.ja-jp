---
title: 外部ギフト カードのサポート
description: このトピックでは、Microsoft Dynamics 365 Commerce で現在利用できる外部ギフト カードのサポートについて説明します。
author: sericks007
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.devlang: ''
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: ivanv
ms.search.validFrom: 2017-10-02
ms.dyn365.ops.version: Application update 4
ms.openlocfilehash: 2cf41330e6016af144caa3bdcfa2e7b523b3c3ff
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017742"
---
# <a name="support-for-external-gift-cards"></a><span data-ttu-id="5b368-103">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="5b368-103">Support for external gift cards</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b368-104">顧客にシームレスなエクスペリエンスを提供するために、小売業者はさまざまな支払方法を受け入れることができることを望んでいます。</span><span class="sxs-lookup"><span data-stu-id="5b368-104">To provide a seamless experience for their customers, retailers want to be able to accept a wide variety of payment methods.</span></span> <span data-ttu-id="5b368-105">ギフト カードは、現金やクレジット カードの次に最も頻繁に使用される支払方法の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="5b368-105">Gift cards are one of the most frequently used payment methods after cash and credit cards.</span></span> <span data-ttu-id="5b368-106">多くの小売業者にとっての重要な要件は、販売時点管理 (POS) でさまざまなタイプのギフト カードを各種プロバイダーから受け入れることです。</span><span class="sxs-lookup"><span data-stu-id="5b368-106">An important requirement for many retailers is the ability to accept various types of gift cards, from various providers, at the point of sale (POS).</span></span>

<span data-ttu-id="5b368-107">Microsoft Dynamics 365 Commerce は現在、外部ギフト カードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5b368-107">Microsoft Dynamics 365 Commerce now supports external gift cards.</span></span> <span data-ttu-id="5b368-108">したがって、小売業者は、GiveX などのギフト カード プロバイダーからのサードパーティ ギフト カードを POS を使用して受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="5b368-108">Therefore, retailers can accept third-party gift cards from gift card providers such GiveX by using the POS.</span></span> <span data-ttu-id="5b368-109">この機能を活用するには、外部のギフト カード サービス プロバイダのアカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="5b368-109">To take advantage of this functionality, you must have an account with an external gift card service provider.</span></span> <span data-ttu-id="5b368-110">この機能は、ソリューションが提供していた標準のギフト カード サポートとは異なります。</span><span class="sxs-lookup"><span data-stu-id="5b368-110">This functionality differs from the out-of-box gift card support that the solution offered.</span></span>

<span data-ttu-id="5b368-111">最初から用意されている Verifone Payment コネクタもアップデートされ、外部ギフト カードの機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5b368-111">The out-of-box Verifone Payment connector has also been updated so that it supports the functionality for external gift cards.</span></span> <span data-ttu-id="5b368-112">最初の更新で GiveX との統合が可能になりました。</span><span class="sxs-lookup"><span data-stu-id="5b368-112">The initial update enables integration with GiveX.</span></span>

<span data-ttu-id="5b368-113">外部ギフト カードは、バックオフィスと POS の両方に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b368-113">The external gift card must be configured for both the Headquarters and the POS.</span></span> <span data-ttu-id="5b368-114">ギフト カードをコンフィギュレーションする前に、小売業者は外部のギフト カード サービス プロバイダーのアカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="5b368-114">Before the gift card can be configured, the retailer must have an account with an external gift card service provider.</span></span>

## <a name="headquarters-configuration"></a><span data-ttu-id="5b368-115">バックオフィス コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5b368-115">Headquarters configuration</span></span>

1. <span data-ttu-id="5b368-116">Dynamics 365 Commerce バックオフィスで、**ハードウェア プロファイル**を検索して **POS ハードウェア プロファイル** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b368-116">In Dynamics 365 Commerce Headquarters, search for **Hardware profiles** to open the **POS hardware profile** page.</span></span>
2. <span data-ttu-id="5b368-117">**POS ハードウェア プロファイル**ページで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5b368-117">On the **POS hardware profile** page, follow these steps:</span></span>

   1. <span data-ttu-id="5b368-118">ページの左側にあるナビゲーション バーで、**仮想**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-118">On the navigation bar on the left side of the page, select **Virtual**.</span></span>
   2. <span data-ttu-id="5b368-119">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-119">Select **Edit**.</span></span>
   3. <span data-ttu-id="5b368-120">**ETF サービス**クイック タブの、**コネクタ**グリッドで、最初の入力 **TestConnector** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-120">On the **ETF service** FastTab, in the **Connectors** grid, select the first entry, **TestConnector**.</span></span>
   4. <span data-ttu-id="5b368-121">**サポートされる支払/入金タイプ** フィールドに、**GiftCard** を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b368-121">In the **Supported Tender Types** field, add **GiftCard**.</span></span>

       ![サポートされている支払/入金タイプのリストへの GiftCard の追加](./media/01.png)

   5. <span data-ttu-id="5b368-123">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-123">Select **Save**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="5b368-124">また、**新規** ボタンを使用して複数の支払コネクタを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5b368-124">You can also use the **New** button to create multiple payment connectors.</span></span> <span data-ttu-id="5b368-125">この方法で、ソリューションに追加された複数のコネクタのサポートを利用できます。</span><span class="sxs-lookup"><span data-stu-id="5b368-125">In this way, you can take advantage of the support for multiple connectors that has been added to the solution.</span></span> <span data-ttu-id="5b368-126">異なる支払メソッドのために異なる支払コネクタを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5b368-126">You can then have different payment connectors for different payment methods.</span></span> <span data-ttu-id="5b368-127">たとえば、1 つのコネクタですべてのクレジット カードを処理できますが、別のコネクタでギフト カードを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="5b368-127">For example, all credit cards can be processed through one connector, but the gift card can be processed through a different connector.</span></span>

### <a name="card-types"></a><span data-ttu-id="5b368-128">カード タイプ</span><span class="sxs-lookup"><span data-stu-id="5b368-128">Card Types</span></span>

1. <span data-ttu-id="5b368-129">**カード タイプ**の検索</span><span class="sxs-lookup"><span data-stu-id="5b368-129">Search for **Card Types**</span></span> 
2. <span data-ttu-id="5b368-130">**新規**をクリックし、次の値を追加して、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b368-130">Click **New**, add the following values, and then click **Save**:</span></span>

| <span data-ttu-id="5b368-131">フィールド名</span><span class="sxs-lookup"><span data-stu-id="5b368-131">Field Name</span></span>     | <span data-ttu-id="5b368-132">Value</span><span class="sxs-lookup"><span data-stu-id="5b368-132">Value</span></span>              |
|----------------|--------------------|
| <span data-ttu-id="5b368-133">カード ID</span><span class="sxs-lookup"><span data-stu-id="5b368-133">Card ID</span></span>        | <span data-ttu-id="5b368-134">EXTGC</span><span class="sxs-lookup"><span data-stu-id="5b368-134">EXTGC</span></span>              |
| <span data-ttu-id="5b368-135">カード タイプ名</span><span class="sxs-lookup"><span data-stu-id="5b368-135">Card type name</span></span> | <span data-ttu-id="5b368-136">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-136">External Gift Card</span></span> |
| <span data-ttu-id="5b368-137">カード タイプ</span><span class="sxs-lookup"><span data-stu-id="5b368-137">Card types</span></span>     | <span data-ttu-id="5b368-138">ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-138">Gift card</span></span>          |
| <span data-ttu-id="5b368-139">カード発行元</span><span class="sxs-lookup"><span data-stu-id="5b368-139">Card issuer</span></span>    | <span data-ttu-id="5b368-140">*すべての説明*</span><span class="sxs-lookup"><span data-stu-id="5b368-140">*Any description*</span></span>  |

### <a name="payment-methods"></a><span data-ttu-id="5b368-141">支払方法</span><span class="sxs-lookup"><span data-stu-id="5b368-141">Payment Methods</span></span>

1. <span data-ttu-id="5b368-142">**支払方法**を検索して、**支払方法**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b368-142">Search for **Payment methods** to open the **Payment methods** page.</span></span>
2. <span data-ttu-id="5b368-143">**新規**をクリックし、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5b368-143">Click **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="5b368-144">**支払方法**フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="5b368-144">In the **Payment method** field, enter **12**.</span></span>
    2. <span data-ttu-id="5b368-145">**支払方法名**フィールドに、**外部ギフト カード**と入力します。</span><span class="sxs-lookup"><span data-stu-id="5b368-145">In the **Payment method name** field, enter **External Gift Card**.</span></span>
    3. <span data-ttu-id="5b368-146">**既定の機能**フィールドで、**カード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-146">In the **Default function** field, select **Card**.</span></span>
    4. <span data-ttu-id="5b368-147">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-147">Select **Save**.</span></span>

3. <span data-ttu-id="5b368-148">**すべての店舗**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b368-148">Open the **All stores** page.</span></span>
4. <span data-ttu-id="5b368-149">一覧で、**ヒューストン**の店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-149">In the list, select the **Houston** store.</span></span>
5. <span data-ttu-id="5b368-150">アクション ウィンドウで、**設定** &gt; **支払方法**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b368-150">On the Action Pane, click **Set up** &gt; **Payment methods**.</span></span>
6. <span data-ttu-id="5b368-151">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b368-151">Click **New**.</span></span>
7. <span data-ttu-id="5b368-152">**支払方法**フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="5b368-152">In the **Payment method** field, enter **12**.</span></span> <span data-ttu-id="5b368-153">次に、**支払方法名** および **関数** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5b368-153">The **Payment method name** and **Function** fields should then be set automatically.</span></span>
8. <span data-ttu-id="5b368-154">**一般**クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5b368-154">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="5b368-155">**工程名** フィールドを **支払ギフト カード** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b368-155">Set the **Operation name** field to **Pay gift card**.</span></span>
    - <span data-ttu-id="5b368-156">**コネクタ名** フィールドを **TestConnector** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b368-156">Set the **Connector name** field to **TestConnector**.</span></span>

9. <span data-ttu-id="5b368-157">**転記**クイック タブで、**ギフト カード品目番号**フィールドを **0010** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b368-157">On the **Posting** FastTab, set the **Gift card item number** field to **0010**.</span></span>

    ![ギフト カード品目の番号フィールドの設定](./media/05_02.png)

10. <span data-ttu-id="5b368-159">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b368-159">Click **Save**.</span></span>
11. <span data-ttu-id="5b368-160">手順 4 で作成したギフト カードに新たに作成した外部のギフト カードの支払い方法を割り当てるには、**カードの設定**をクリックし、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b368-160">Click **Card setup** and click **New** to map the gift card created in step 4 to the newly created external gift card payment method.</span></span>

### <a name="update-button-grid"></a><span data-ttu-id="5b368-161">ボタン グリッドの更新</span><span class="sxs-lookup"><span data-stu-id="5b368-161">Update button grid</span></span>

1. <span data-ttu-id="5b368-162">**ボタン グリッド** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="5b368-162">Go to the **Button grid** page.</span></span>
2. <span data-ttu-id="5b368-163">ページの左側にあるナビゲーション バーで、**F2S1M** を検索してフィルター処理オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-163">In the navigation bar on the left side of the page, search for **F2S1M**, and select the filtered option.</span></span>
3. <span data-ttu-id="5b368-164">アクション ウィンドウで、**デザイナー**をクリックしてボタン デザイナー アプリケーションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5b368-164">On the Action Pane, click **Designer** to download the button designer application.</span></span>
4. <span data-ttu-id="5b368-165">グリッド デザイナーが表示されたら、空の (灰色) 領域を右クリックして、**新規作成ボタン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b368-165">When the grid designer appears, right-click on an empty (gray) area, and then click **New button**.</span></span>

    ![新しいボタン](./media/07.png)

5. <span data-ttu-id="5b368-167">新しいボタンを右クリックし、**ボタン プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-167">Right-click the new button, and then select **Button properties**.</span></span>
6. <span data-ttu-id="5b368-168">次のマトリックスに従って **アクション**、**支払タイプ**、および**ボタンのテキスト** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5b368-168">Set the **Action**, **Payment type**, and **Text on button** properties according to the following matrix.</span></span>

    | <span data-ttu-id="5b368-169">アクション</span><span class="sxs-lookup"><span data-stu-id="5b368-169">Action</span></span>            | <span data-ttu-id="5b368-170">支払タイプ</span><span class="sxs-lookup"><span data-stu-id="5b368-170">Payment type</span></span>       | <span data-ttu-id="5b368-171">ボタンのテキスト</span><span class="sxs-lookup"><span data-stu-id="5b368-171">Text on button</span></span>        |
    |-------------------|--------------------|-----------------------|
    | <span data-ttu-id="5b368-172">ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="5b368-172">Issue gift card</span></span>   | <span data-ttu-id="5b368-173">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-173">External Gift Card</span></span> | <span data-ttu-id="5b368-174">Ext Issue ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-174">Ext Issue gift card</span></span>   |
    | <span data-ttu-id="5b368-175">ギフト カードに追加</span><span class="sxs-lookup"><span data-stu-id="5b368-175">Add to gift card</span></span>  | <span data-ttu-id="5b368-176">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-176">External Gift Card</span></span> | <span data-ttu-id="5b368-177">ギフト カードに Ext 追加</span><span class="sxs-lookup"><span data-stu-id="5b368-177">Ext Add to gift card</span></span>  |
    | <span data-ttu-id="5b368-178">ギフト カード残高</span><span class="sxs-lookup"><span data-stu-id="5b368-178">Gift card balance</span></span> | <span data-ttu-id="5b368-179">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-179">External Gift Card</span></span> | <span data-ttu-id="5b368-180">Ext Gift カード残高</span><span class="sxs-lookup"><span data-stu-id="5b368-180">Ext Gift card balance</span></span> |
    | <span data-ttu-id="5b368-181">ギフト カードで支払う</span><span class="sxs-lookup"><span data-stu-id="5b368-181">Pay gift card</span></span>     | <span data-ttu-id="5b368-182">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-182">External Gift Card</span></span> | <span data-ttu-id="5b368-183">Ext Pay ギフト カード</span><span class="sxs-lookup"><span data-stu-id="5b368-183">Ext Pay gift card</span></span>     |

    <span data-ttu-id="5b368-184">完了したら、ボタンのレイアウトは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="5b368-184">When you've finished, your button layout should resemble the following illustration.</span></span>

    ![完了したボタン レイアウト](./media/10.png)

7. <span data-ttu-id="5b368-186">デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b368-186">Close the designer.</span></span>
8. <span data-ttu-id="5b368-187">**配送スケジュール**を検索します。</span><span class="sxs-lookup"><span data-stu-id="5b368-187">Search for **Distribution Schedule**.</span></span>
9. <span data-ttu-id="5b368-188">ページの左側にあるナビゲーション バーで、**1090**、**1115**、および **1070** を検索します。</span><span class="sxs-lookup"><span data-stu-id="5b368-188">In the navigation bar on the left side of the page, search for **1090**, **1115**, and **1070**.</span></span>
10. <span data-ttu-id="5b368-189">アクション ウィンドウで、**今すぐ実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b368-189">On the Action Pane, click **Run now**.</span></span>
11. <span data-ttu-id="5b368-190">**ダウンロード セッション**を検索してジョブのステータスを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5b368-190">Check the status of the job by searching for **Download sessions**.</span></span>
12. <span data-ttu-id="5b368-191">すべてのジョブの横に **適用済** が表示されるまで待ってから、ブラウザーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b368-191">Wait until **Applied** appears next to all the jobs, and then close the browser.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b368-192">店舗にある Retail Commerce Scale Unit (RCSU) を使用している場合は、IIS の残りを実行してキャッシュをクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b368-192">If you are using Retail Commerce Scale Unit (RCSU) that is located in the store, you need to perform an IIS rest to clear the cache.</span></span> <span data-ttu-id="5b368-193">これは IIS アプリケーションから実行するか、または管理者コマンド プロンプト ウィンドウを開いて `iisreset` を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b368-193">You can either do this through the IIS application or open an admin Command Prompt window and enter `iisreset`.</span></span> <span data-ttu-id="5b368-194">それ以外の場合、RCSU が更新されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="5b368-194">Otherwise, wait for the RCSU to be updated.</span></span>

## <a name="update-merchant-properties"></a><span data-ttu-id="5b368-195">商人プロパティの更新</span><span class="sxs-lookup"><span data-stu-id="5b368-195">Update merchant properties</span></span>

1. <span data-ttu-id="5b368-196">ファイル エクスプローラーで、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\ConfigurationUtility** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b368-196">In File Explorer, go to **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\ConfigurationUtility**.</span></span>
2. <span data-ttu-id="5b368-197">**HardwareStationConfigurationUtility** 実行可能プログラムを実行します。</span><span class="sxs-lookup"><span data-stu-id="5b368-197">Run the **HardwareStationConfigurationUtility** executable program.</span></span>
3. <span data-ttu-id="5b368-198">正しい Commerce Scale Unit URL を入力してユーティリティをコンフィギュレーションし、**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-198">Configure the utility by entering the correct Commerce Scale Unit URL, and then select **Install**.</span></span>
4. <span data-ttu-id="5b368-199">ダウンロードが正常に完了したことを確認するには、**C:\\ProgramData\\Microsoft Dynamics AX\\Retail Hardware Station** に移動し、**MerchantInformation.xml** ファイルのタイムスタンプを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b368-199">To verify that the download was successful, go to **C:\\ProgramData\\Microsoft Dynamics AX\\Retail Hardware Station**, and look at the timestamp of the **MerchantInformation.xml** file.</span></span> <span data-ttu-id="5b368-200">これは最新である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b368-200">It should be very recent.</span></span>

## <a name="configure-and-test-modern-pos"></a><span data-ttu-id="5b368-201">Modern POS のコンフィギュレーションおよびテスト</span><span class="sxs-lookup"><span data-stu-id="5b368-201">Configure and test Modern POS</span></span>

1. <span data-ttu-id="5b368-202">Modern POS (MPOS) アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="5b368-202">Start the Modern POS (MPOS) application.</span></span>
2. <span data-ttu-id="5b368-203">標準の資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="5b368-203">Sign in by using the standard credentials.</span></span>
3. <span data-ttu-id="5b368-204">メッセージが表示されたら、**ドロワー以外の操作の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-204">When you're prompted, select **Perform a non-drawer operation**.</span></span>
4. <span data-ttu-id="5b368-205">メイン画面で、**ハードウェア ステーションの選択**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-205">On the main screen, select **Select hardware station**.</span></span>
5. <span data-ttu-id="5b368-206">ページの右側にあるバーで、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-206">On the bar on the right side of the page, select **Manage**.</span></span>
6. <span data-ttu-id="5b368-207">**仮想周辺機器** をオンにし、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-207">Turn on **Virtual Peripherals**, and then select **OK**.</span></span>
7. <span data-ttu-id="5b368-208">**使用可能なペアリング済ステーション** フィールドで、**仮想周辺機器**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-208">In the **Available paired stations** field, select **Virtual Peripherals**.</span></span>
8. <span data-ttu-id="5b368-209">新しいシフトを開くか、非ドロワー操作を実行するように求められます。</span><span class="sxs-lookup"><span data-stu-id="5b368-209">You're prompted to either open a new shift or perform non-drawer operations.</span></span> <span data-ttu-id="5b368-210">新しいシフトを開くことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5b368-210">You can now open a new shift.</span></span>
9. <span data-ttu-id="5b368-211">メイン画面で、**現在のトランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-211">On the main screen, select **Current transaction**.</span></span>
10. <span data-ttu-id="5b368-212">**ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-212">Select **Gift cards**.</span></span>
11. <span data-ttu-id="5b368-213">**Ext Issue ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b368-213">Select **Ext Issue gift card**.</span></span>
12. <span data-ttu-id="5b368-214">**9** で始まる数を入力し、次に金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b368-214">Enter a number that starts with **9**, and then provide an amount.</span></span>
13. <span data-ttu-id="5b368-215">品目がカートに追加された後、現金またはカードを使用して支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="5b368-215">After items are added to the cart, you can pay by using cash or a card.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5b368-216">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="5b368-216">Troubleshooting</span></span> 

### <a name="issue-an-error-occurs-when-you-start-the-hardwarestationconfigurationutility-program"></a><span data-ttu-id="5b368-217">問題: HardwareStationConfigurationUtility プログラムの起動時にエラーが発生します</span><span class="sxs-lookup"><span data-stu-id="5b368-217">Issue: An error occurs when you start the HardwareStationConfigurationUtility program</span></span>

1. <span data-ttu-id="5b368-218">上位のコマンド プロンプトからは、メモ帳で **HardwareStationConfigurationUtility.exe.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b368-218">From an elevated command prompt, open the **HardwareStationConfigurationUtility.exe.config** file in Notepad.</span></span>
2. <span data-ttu-id="5b368-219">ファイルで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5b368-219">In the file, follow these steps:</span></span>

    1. <span data-ttu-id="5b368-220">**DataServiceUrl** 値を適切な Commerce Scale Unit URL に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5b368-220">Replace the **DataServiceUrl** value with the correct Commerce Scale Unit URL.</span></span>
    2. <span data-ttu-id="5b368-221">**AADLogonUrl** の値が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b368-221">Verify that the **AADLogonUrl** value is correct.</span></span>

3. <span data-ttu-id="5b368-222">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b368-222">Save and close the file.</span></span>
4. <span data-ttu-id="5b368-223">ユーティリティを再起動します。</span><span class="sxs-lookup"><span data-stu-id="5b368-223">Restart the utility.</span></span>

### <a name="issue-a-token-error-occurs-when-you-try-to-pair-virtual-peripherals"></a><span data-ttu-id="5b368-224">問題: 仮想周辺機器をペアリングしようとしたときにトークン エラーが発生します</span><span class="sxs-lookup"><span data-stu-id="5b368-224">Issue: A token error occurs when you try to pair virtual peripherals</span></span>

1. <span data-ttu-id="5b368-225">MPOS を終了します。</span><span class="sxs-lookup"><span data-stu-id="5b368-225">Exit MPOS.</span></span>
2. <span data-ttu-id="5b368-226">**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b368-226">Go to **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package**.</span></span>
3. <span data-ttu-id="5b368-227">上位のコマンド プロンプトからは、メモ帳で **Web.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b368-227">From an elevated command prompt, open the **Web.config** file in Notepad.</span></span>
4. <span data-ttu-id="5b368-228">**RetailServer** 値を適切な Commerce Scale Unit 値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5b368-228">Replace the **RetailServer** value with the correct Commerce Scale Unit value.</span></span>
5. <span data-ttu-id="5b368-229">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b368-229">Save and close the file.</span></span>
6. <span data-ttu-id="5b368-230">MPOS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="5b368-230">Restart MPOS.</span></span>
7. <span data-ttu-id="5b368-231">問題が解消しない場合は、MPOS を終了し、タスク マネージャーを使用して、実行中の dllhost.exe インスタンスを終了させ、インターネット インフォメーション サービス (IIS) のリセットを別に行います。</span><span class="sxs-lookup"><span data-stu-id="5b368-231">If the issue persists, exit MPOS, use Task Manager to end any instances of dllhost.exe that are running, and then do another reset of Internet Information Services (IIS).</span></span>
