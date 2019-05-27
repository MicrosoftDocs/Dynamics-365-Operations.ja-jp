---
title: 外部ギフト カードのサポート
description: このトピックでは、Microsoft Dynamics 365 for Retail で現在利用できる外部ギフト カードのサポートについて説明します。
author: sericks007
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.devlang: ''
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: ivanv
ms.search.validFrom: 2017-10-02
ms.dyn365.ops.version: Application update 4
ms.openlocfilehash: 753b2983176b5cc1e51ffb18bfafefbfb07b2bd4
ms.sourcegitcommit: a25f988c4a159a1aea98641cf9eb0e0b9979d00f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2019
ms.locfileid: "1541012"
---
# <a name="support-for-external-gift-cards"></a><span data-ttu-id="11f07-103">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="11f07-103">Support for external gift cards</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11f07-104">顧客にシームレスなエクスペリエンスを提供するために、小売業者はさまざまな支払方法を受け入れることができることを望んでいます。</span><span class="sxs-lookup"><span data-stu-id="11f07-104">To provide a seamless experience for their customers, retailers want to be able to accept a wide variety of payment methods.</span></span> <span data-ttu-id="11f07-105">ギフト カードは、現金やクレジット カードの次に最も頻繁に使用される支払方法の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="11f07-105">Gift cards are one of the most frequently used payment methods after cash and credit cards.</span></span> <span data-ttu-id="11f07-106">多くの小売業者にとっての重要な要件は、販売時点管理 (POS) でさまざまなタイプのギフト カードを各種プロバイダーから受け入れることです。</span><span class="sxs-lookup"><span data-stu-id="11f07-106">An important requirement for many retailers is the ability to accept various types of gift cards, from various providers, at the point of sale (POS).</span></span>

<span data-ttu-id="11f07-107">Microsoft Dynamics 365 for Retail は現在、外部ギフト カードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="11f07-107">Microsoft Dynamics 365 for Retail now supports external gift cards.</span></span> <span data-ttu-id="11f07-108">したがって、小売業者は、GiveX などのギフト カード プロバイダーからのサードパーティ ギフト カードを POS を使用して受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="11f07-108">Therefore, retailers can accept third-party gift cards from gift card providers such GiveX by using the POS.</span></span> <span data-ttu-id="11f07-109">この機能を活用するには、外部のギフト カード サービス プロバイダのアカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="11f07-109">To take advantage of this functionality, you must have an account with an external gift card service provider.</span></span> <span data-ttu-id="11f07-110">この機能は、ソリューションが提供していた標準のギフト カード サポートとは異なります。</span><span class="sxs-lookup"><span data-stu-id="11f07-110">This functionality differs from the out-of-box gift card support that the solution offered.</span></span>

<span data-ttu-id="11f07-111">最初から用意されている Verifone Payment コネクタもアップデートされ、外部ギフト カードの機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="11f07-111">The out-of-box Verifone Payment connector has also been updated so that it supports the functionality for external gift cards.</span></span> <span data-ttu-id="11f07-112">最初の更新で GiveX との統合が可能になりました。</span><span class="sxs-lookup"><span data-stu-id="11f07-112">The initial update enables integration with GiveX.</span></span>

<span data-ttu-id="11f07-113">外部ギフト カードは、小売用バックオフィスと POS の両方に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11f07-113">The external gift card must be configured for both the Retail headquarters and the POS.</span></span> <span data-ttu-id="11f07-114">ギフト カードをコンフィギュレーションする前に、小売業者は外部のギフト カード サービス プロバイダーのアカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="11f07-114">Before the gift card can be configured, the retailer must have an account with an external gift card service provider.</span></span>

## <a name="retail-headquarters-configuration"></a><span data-ttu-id="11f07-115">小売用バックオフィス コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="11f07-115">Retail headquarters configuration</span></span>

1. <span data-ttu-id="11f07-116">**ハードウェア プロファイル**を検索して **POS ハードウェア プロファイル** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="11f07-116">Search for **hardware profile** to open the **POS hardware profile** page.</span></span>
2. <span data-ttu-id="11f07-117">**POS ハードウェア プロファイル**ページで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11f07-117">On the **POS hardware profile** page, follow these steps:</span></span>

   1. <span data-ttu-id="11f07-118">ページの左側にあるナビゲーション バーで、**仮想**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-118">On the navigation bar on the left side of the page, select **Virtual**.</span></span>
   2. <span data-ttu-id="11f07-119">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-119">Select **Edit**.</span></span>
   3. <span data-ttu-id="11f07-120">**ETF サービス**クイック タブの、**コネクタ**グリッドで、最初の入力 **TestConnector** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-120">On the **ETF service** FastTab, in the **Connectors** grid, select the first entry, **TestConnector**.</span></span>
   4. <span data-ttu-id="11f07-121">**サポートされる支払/入金タイプ** フィールドに、**GiftCard** を追加します。</span><span class="sxs-lookup"><span data-stu-id="11f07-121">In the **Supported Tender Types** field, add **GiftCard**.</span></span>

       ![サポートされている支払/入金タイプのリストへの GiftCard の追加](./media/01.png)

   5. <span data-ttu-id="11f07-123">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-123">Select **Save**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="11f07-124">また、**新規** ボタンを使用して複数の支払コネクタを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="11f07-124">You can also use the **New** button to create multiple payment connectors.</span></span> <span data-ttu-id="11f07-125">この方法で、ソリューションに追加された複数のコネクタのサポートを利用できます。</span><span class="sxs-lookup"><span data-stu-id="11f07-125">In this way, you can take advantage of the support for multiple connectors that has been added to the solution.</span></span> <span data-ttu-id="11f07-126">異なる支払メソッドのために異なる支払コネクタを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="11f07-126">You can then have different payment connectors for different payment methods.</span></span> <span data-ttu-id="11f07-127">たとえば、1 つのコネクタですべてのクレジット カードを処理できますが、別のコネクタでギフト カードを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="11f07-127">For example, all credit cards can be processed through one connector, but the gift card can be processed through a different connector.</span></span>

3. <span data-ttu-id="11f07-128">**支払方法** を検索して **支払方法** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="11f07-128">Search for **payment methods** to open the **Payment methods** page.</span></span>
4. <span data-ttu-id="11f07-129">**新規** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11f07-129">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="11f07-130">**支払方法**フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="11f07-130">In the **Payment method** field, enter **12**.</span></span>
    2. <span data-ttu-id="11f07-131">**支払方法名**フィールドに、**外部ギフト カード**と入力します。</span><span class="sxs-lookup"><span data-stu-id="11f07-131">In the **Payment method name** field, enter **External Gift Card**.</span></span>
    3. <span data-ttu-id="11f07-132">**既定の機能**フィールドで、**カード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-132">In the **Default function** field, select **Card**.</span></span>
    4. <span data-ttu-id="11f07-133">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-133">Select **Save**.</span></span>

5. <span data-ttu-id="11f07-134">**すべての小売店舗**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="11f07-134">Open the **All retail stores** page.</span></span>
6. <span data-ttu-id="11f07-135">一覧で、**ヒューストン**の店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-135">In the list, select the **Houston** store.</span></span>
7. <span data-ttu-id="11f07-136">アクション ウィンドウで、**設定** &gt; **支払方法**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-136">On the Action Pane, select **Set up** &gt; **Payment methods**.</span></span>
8. <span data-ttu-id="11f07-137">**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-137">Select **New**.</span></span>
9. <span data-ttu-id="11f07-138">**支払方法**フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="11f07-138">In the **Payment method** field, enter **12**.</span></span> <span data-ttu-id="11f07-139">次に、**支払方法名** および **関数** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="11f07-139">The **Payment method name** and **Function** fields should then be set automatically.</span></span>
10. <span data-ttu-id="11f07-140">**一般**クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="11f07-140">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="11f07-141">**工程名** フィールドを **支払ギフト カード** に設定します。</span><span class="sxs-lookup"><span data-stu-id="11f07-141">Set the **Operation name** field to **Pay gift card**.</span></span>
    - <span data-ttu-id="11f07-142">**コネクタ名** フィールドを **TestConnector** に設定します。</span><span class="sxs-lookup"><span data-stu-id="11f07-142">Set the **Connector name** field to **TestConnector**.</span></span>

11. <span data-ttu-id="11f07-143">**転記**クイック タブで、**ギフト カード品目番号**フィールドを **0010** に設定します。</span><span class="sxs-lookup"><span data-stu-id="11f07-143">On the **Posting** FastTab, set the **Gift card item number** field to **0010**.</span></span>

    ![ギフト カード品目の番号フィールドの設定](./media/05_02.png)

12. <span data-ttu-id="11f07-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-145">Select **Save**.</span></span>
13. <span data-ttu-id="11f07-146">手順4で作成したギフトカードに新たに作成した外部のギフトカードの支払い方法を割り当てるには、 **Card setup** を選択し、 **New** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11f07-146">Select **Card setup** and click **New** to map the gift card created in step 4 to the newly created external gift card payment method.</span></span>  
14. <span data-ttu-id="11f07-147">**ボタン グリッド**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="11f07-147">Open the **Button grid** page.</span></span>
15. <span data-ttu-id="11f07-148">ページの左側にあるナビゲーション バーで、**F2S1M** を検索してフィルター処理オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-148">In the navigation bar on the left side of the page, search for **F2S1M**, and select the filtered option.</span></span>
16. <span data-ttu-id="11f07-149">アクション ウィンドウで、**デザイナー**を選択しボタン デザイナー アプリケーションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="11f07-149">On the Action Pane, select **Designer** to download the button designer application.</span></span>
17. <span data-ttu-id="11f07-150">グリッド デザイナーが表示されたら、空の (灰色) 領域を右クリックして、**新規作成ボタン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-150">When the grid designer appears, right-click on an empty (gray) area, and then select **New button**.</span></span>

    ![新しいボタン](./media/07.png)

18. <span data-ttu-id="11f07-152">新しいボタンを右クリックし、**ボタン プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-152">Right-click the new button, and then select **Button properties**.</span></span>
19. <span data-ttu-id="11f07-153">次のマトリックスに従って **アクション**、**支払タイプ**、および**ボタンのテキスト** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="11f07-153">Set the **Action**, **Payment type**, and **Text on button** properties according to the following matrix.</span></span>

    | <span data-ttu-id="11f07-154">アクション</span><span class="sxs-lookup"><span data-stu-id="11f07-154">Action</span></span>            | <span data-ttu-id="11f07-155">支払タイプ</span><span class="sxs-lookup"><span data-stu-id="11f07-155">Payment type</span></span>       | <span data-ttu-id="11f07-156">ボタンのテキスト</span><span class="sxs-lookup"><span data-stu-id="11f07-156">Text on button</span></span>        |
    |-------------------|--------------------|-----------------------|
    | <span data-ttu-id="11f07-157">ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="11f07-157">Issue gift card</span></span>   | <span data-ttu-id="11f07-158">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="11f07-158">External Gift Card</span></span> | <span data-ttu-id="11f07-159">Ext Issue ギフト カード</span><span class="sxs-lookup"><span data-stu-id="11f07-159">Ext Issue gift card</span></span>   |
    | <span data-ttu-id="11f07-160">ギフト カードに追加</span><span class="sxs-lookup"><span data-stu-id="11f07-160">Add to gift card</span></span>  | <span data-ttu-id="11f07-161">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="11f07-161">External Gift Card</span></span> | <span data-ttu-id="11f07-162">ギフト カードに Ext 追加</span><span class="sxs-lookup"><span data-stu-id="11f07-162">Ext Add to gift card</span></span>  |
    | <span data-ttu-id="11f07-163">ギフト カード残高</span><span class="sxs-lookup"><span data-stu-id="11f07-163">Gift card balance</span></span> | <span data-ttu-id="11f07-164">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="11f07-164">External Gift Card</span></span> | <span data-ttu-id="11f07-165">Ext Gift カード残高</span><span class="sxs-lookup"><span data-stu-id="11f07-165">Ext Gift card balance</span></span> |
    | <span data-ttu-id="11f07-166">ギフト カードで支払う</span><span class="sxs-lookup"><span data-stu-id="11f07-166">Pay gift card</span></span>     | <span data-ttu-id="11f07-167">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="11f07-167">External Gift Card</span></span> | <span data-ttu-id="11f07-168">Ext Pay ギフト カード</span><span class="sxs-lookup"><span data-stu-id="11f07-168">Ext Pay gift card</span></span>     |

    <span data-ttu-id="11f07-169">完了したら、ボタンのレイアウトは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="11f07-169">When you've finished, your button layout should resemble the following illustration.</span></span>

    ![完了したボタン レイアウト](./media/10.png)

20. <span data-ttu-id="11f07-171">デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="11f07-171">Close the designer.</span></span>
21. <span data-ttu-id="11f07-172">**配送スケジュール**を検索します。</span><span class="sxs-lookup"><span data-stu-id="11f07-172">Search for **Distribution Schedule**.</span></span>
22. <span data-ttu-id="11f07-173">ページの左側にあるナビゲーション バーで、**1090**、**1115**、および **1070** を検索します。</span><span class="sxs-lookup"><span data-stu-id="11f07-173">In the navigation bar on the left side of the page, search for **1090**, **1115**, and **1070**.</span></span>
23. <span data-ttu-id="11f07-174">アクション ウィンドウで、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-174">On the Action Pane, select **Run now**.</span></span>
24. <span data-ttu-id="11f07-175">**ダウンロード セッション**を検索してジョブのステータスを確認してください。</span><span class="sxs-lookup"><span data-stu-id="11f07-175">Check the status of the job by searching for **Download sessions**.</span></span>
25. <span data-ttu-id="11f07-176">すべてのジョブの横に **適用済** が表示されるまで待ってから、ブラウザーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="11f07-176">Wait until **Applied** appears next to all the jobs, and then close the browser.</span></span>

## <a name="reset-iis-if-youre-using-retail-store-scale-unit"></a><span data-ttu-id="11f07-177">Retail Store Scale Unit を使用している場合、IIS をリセットします。</span><span class="sxs-lookup"><span data-stu-id="11f07-177">Reset IIS if you're using Retail Store Scale Unit</span></span>

<span data-ttu-id="11f07-178">ストアにある Retail Store Scale Unit (RSSU) を使用している場合は、管理者としてコマンド プロンプト ウィンドウを開き、**iisreset** と入力します。</span><span class="sxs-lookup"><span data-stu-id="11f07-178">If you're using a Retail Store Scale Unit (RSSU) that is located in the store, open a Command Prompt window as an administrator, and enter **iisreset**.</span></span> <span data-ttu-id="11f07-179">それ以外の場合、Retail サーバーが更新されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="11f07-179">Otherwise, wait for the Retail Server to be updated.</span></span>

## <a name="update-merchant-properties"></a><span data-ttu-id="11f07-180">商人プロパティの更新</span><span class="sxs-lookup"><span data-stu-id="11f07-180">Update merchant properties</span></span>

1. <span data-ttu-id="11f07-181">ファイル エクスプローラーで、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\ConfigurationUtility** に移動します。</span><span class="sxs-lookup"><span data-stu-id="11f07-181">In File Explorer, go to **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\ConfigurationUtility**.</span></span>
2. <span data-ttu-id="11f07-182">**HardwareStationConfigurationUtility** 実行可能プログラムを実行します。</span><span class="sxs-lookup"><span data-stu-id="11f07-182">Run the **HardwareStationConfigurationUtility** executable program.</span></span>
3. <span data-ttu-id="11f07-183">正しい Retail サーバー URL を入力してユーティリティをコンフィギュレーションし、**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-183">Configure the utility by entering the correct Retail Server URL, and then select **Install**.</span></span>
4. <span data-ttu-id="11f07-184">ダウンロードが正常に完了したことを確認するには、**C:\\ProgramData\\Microsoft Dynamics AX\\Retail Hardware Station** に移動し、**MerchantInformation.xml** ファイルのタイムスタンプを確認します。</span><span class="sxs-lookup"><span data-stu-id="11f07-184">To verify that the download was successful, go to **C:\\ProgramData\\Microsoft Dynamics AX\\Retail Hardware Station**, and look at the timestamp of the **MerchantInformation.xml** file.</span></span> <span data-ttu-id="11f07-185">これは最新である必要があります。</span><span class="sxs-lookup"><span data-stu-id="11f07-185">It should be very recent.</span></span>

## <a name="configure-and-test-retail-modern-pos"></a><span data-ttu-id="11f07-186">Retail Modern POS のコンフィギュレーションとテスト</span><span class="sxs-lookup"><span data-stu-id="11f07-186">Configure and test Retail Modern POS</span></span>

1. <span data-ttu-id="11f07-187">Retail Modern POS の申請を開始</span><span class="sxs-lookup"><span data-stu-id="11f07-187">Start the Retail Modern POS (MPOS) application.</span></span>
2. <span data-ttu-id="11f07-188">標準の資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="11f07-188">Sign in by using the standard credentials.</span></span>
3. <span data-ttu-id="11f07-189">メッセージが表示されたら、**ドロワー以外の操作の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-189">When you're prompted, select **Perform a non-drawer operation**.</span></span>
4. <span data-ttu-id="11f07-190">メイン画面で、**ハードウェア ステーションの選択**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-190">On the main screen, select **Select hardware station**.</span></span>
5. <span data-ttu-id="11f07-191">ページの右側にあるバーで、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-191">On the bar on the right side of the page, select **Manage**.</span></span>
6. <span data-ttu-id="11f07-192">**仮想周辺機器** をオンにし、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-192">Turn on **Virtual Peripherals**, and then select **OK**.</span></span>
7. <span data-ttu-id="11f07-193">**使用可能なペアリング済ステーション** フィールドで、**仮想周辺機器**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-193">In the **Available paired stations** field, select **Virtual Peripherals**.</span></span>
8. <span data-ttu-id="11f07-194">新しいシフトを開くか、非ドロワー操作を実行するように求められます。</span><span class="sxs-lookup"><span data-stu-id="11f07-194">You're prompted to either open a new shift or perform non-drawer operations.</span></span> <span data-ttu-id="11f07-195">新しいシフトを開くことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="11f07-195">You can now open a new shift.</span></span>
9. <span data-ttu-id="11f07-196">メイン画面で、**現在のトランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-196">On the main screen, select **Current transaction**.</span></span>
10. <span data-ttu-id="11f07-197">**ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-197">Select **Gift cards**.</span></span>
11. <span data-ttu-id="11f07-198">**Ext Issue ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11f07-198">Select **Ext Issue gift card**.</span></span>
12. <span data-ttu-id="11f07-199">**9** で始まる数を入力し、次に金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="11f07-199">Enter a number that starts with **9**, and then provide an amount.</span></span>
13. <span data-ttu-id="11f07-200">品目がカートに追加された後、現金またはカードを使用して支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="11f07-200">After items are added to the cart, you can pay by using cash or a card.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="11f07-201">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="11f07-201">Troubleshooting</span></span> 

### <a name="issue-an-error-occurs-when-you-start-the-hardwarestationconfigurationutility-program"></a><span data-ttu-id="11f07-202">問題: HardwareStationConfigurationUtility プログラムの起動時にエラーが発生します</span><span class="sxs-lookup"><span data-stu-id="11f07-202">Issue: An error occurs when you start the HardwareStationConfigurationUtility program</span></span>

1. <span data-ttu-id="11f07-203">上位のコマンド プロンプトからは、メモ帳で **HardwareStationConfigurationUtility.exe.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="11f07-203">From an elevated command prompt, open the **HardwareStationConfigurationUtility.exe.config** file in Notepad.</span></span>
2. <span data-ttu-id="11f07-204">ファイルで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11f07-204">In the file, follow these steps:</span></span>

    1. <span data-ttu-id="11f07-205">**DataServiceUrl** 値を適切な Retail サーバー URL に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="11f07-205">Replace the **DataServiceUrl** value with the correct Retail Server URL.</span></span>
    2. <span data-ttu-id="11f07-206">**AADLogonUrl** の値が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="11f07-206">Verify that the **AADLogonUrl** value is correct.</span></span>

3. <span data-ttu-id="11f07-207">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="11f07-207">Save and close the file.</span></span>
4. <span data-ttu-id="11f07-208">ユーティリティを再起動します。</span><span class="sxs-lookup"><span data-stu-id="11f07-208">Restart the utility.</span></span>

### <a name="issue-a-token-error-occurs-when-you-try-to-pair-virtual-peripherals"></a><span data-ttu-id="11f07-209">問題: 仮想周辺機器をペアリングしようとしたときにトークン エラーが発生します</span><span class="sxs-lookup"><span data-stu-id="11f07-209">Issue: A token error occurs when you try to pair virtual peripherals</span></span>

1. <span data-ttu-id="11f07-210">MPOS を終了します。</span><span class="sxs-lookup"><span data-stu-id="11f07-210">Exit MPOS.</span></span>
2. <span data-ttu-id="11f07-211">**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package** に移動します。</span><span class="sxs-lookup"><span data-stu-id="11f07-211">Go to **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package**.</span></span>
3. <span data-ttu-id="11f07-212">上位のコマンド プロンプトからは、メモ帳で **Web.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="11f07-212">From an elevated command prompt, open the **Web.config** file in Notepad.</span></span>
4. <span data-ttu-id="11f07-213">**RetailServer** 値を適切な Retail サーバー値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="11f07-213">Replace the **RetailServer** value with the correct Retail Server value.</span></span>
5. <span data-ttu-id="11f07-214">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="11f07-214">Save and close the file.</span></span>
6. <span data-ttu-id="11f07-215">MPOS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="11f07-215">Restart MPOS.</span></span>
7. <span data-ttu-id="11f07-216">問題が解消しない場合は、MPOS を終了し、タスク マネージャーを使用して、実行中の dllhost.exe インスタンスを終了させ、インターネット インフォメーション サービス (IIS) のリセットを別に行います。</span><span class="sxs-lookup"><span data-stu-id="11f07-216">If the issue persists, exit MPOS, use Task Manager to end any instances of dllhost.exe that are running, and then do another reset of Internet Information Services (IIS).</span></span>
