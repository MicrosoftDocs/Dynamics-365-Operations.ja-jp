---
title: Dynamics 365 Commerce の評価環境で BOPIS を構成する
description: このトピックでは、プロビジョニング後の Microsoft Dynamics 365 Commerce の評価環境における オンライン購入、店舗での受け取り (BOPIS) の構成方法について説明します。
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62dabaa2610341cc8ad8e85812a317ac3123fcb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413650"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="9f368-103">Dynamics 365 Commerce の評価環境で BOPIS を構成する</span><span class="sxs-lookup"><span data-stu-id="9f368-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f368-104">このトピックでは、プロビジョニング後の、 Microsoft Dynamics 365 Commerce の評価環境におけるオンライン購入、店頭受取 (BOPIS) を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9f368-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="9f368-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="9f368-105">Prerequisite</span></span>

<span data-ttu-id="9f368-106">このトピックに記載の手順は、Commerce の評価環境のプロビジョニングと構成が完了した後にのみ実行してください。</span><span class="sxs-lookup"><span data-stu-id="9f368-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="9f368-107">環境のプロビジョニングと構成方法については、 [Dynamics 365 Commerce の評価環境をプロビジョニングする](provisioning-guide.md) と [ Dynamics 365 Commerce の評価環境を構成する](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f368-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="9f368-108">Commerce 環境のプロビジョニングとエンドツーエンドの構成完了後に、このトピックを使用して BOPIS のシナリオを有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="9f368-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="9f368-109">POS の構成</span><span class="sxs-lookup"><span data-stu-id="9f368-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="9f368-110">Modern POS の構成</span><span class="sxs-lookup"><span data-stu-id="9f368-110">Configure Modern POS</span></span>

<span data-ttu-id="9f368-111">クレジット カードの支払を含む BOPIS シナリオには、ハードウェア ステーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="9f368-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="9f368-112">ハードウェア ステーションは、Windows 用および、 Android 用 Modern POS プログラムに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="9f368-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="9f368-113">iOS 用の Cloud POS または Modern POS を使用している場合、販売時点管理（POS）クライアントは、共有ハードウェア ステーションとペアリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f368-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="9f368-114">このトピックでは、Windows 用 BOPIS と Android クライアントの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9f368-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="9f368-115">共有ハードウェア ステーションを設定する方法の詳細については、[小売りハードウェア ステーションの設定とインストール](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f368-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="9f368-116">**小売りとコマース\> チャンネル設定 \> POS 設定 \> レジスター の順に移動します**。</span><span class="sxs-lookup"><span data-stu-id="9f368-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="9f368-117">**SANFRAN-5** の登録を選択し、 **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="9f368-118">**ハードウェア プロファイル** フィールドの値を **HW002** から **HW001** に変更し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f368-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="9f368-119">変更を同期するには、、**小売りと Commerce \> 小売りとCommerce IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f368-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="9f368-120">配送スケジュールに **1090** を選択し、アクション ウィンドウで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="9f368-121">**はい** を選択し、続いて **OK** をクリックしてデータの同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="9f368-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="9f368-122">Modern POS のインストール</span><span class="sxs-lookup"><span data-stu-id="9f368-122">Install Modern POS</span></span>

1. <span data-ttu-id="9f368-123">**小売りとコマース\> チャンネル設定 \> POS 設定 \> デバイス の順に移動します**。</span><span class="sxs-lookup"><span data-stu-id="9f368-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="9f368-124">デバイスに **SANFRANCIS-5** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="9f368-125">アクション ウィンドウで **ダウンロード** を選択し、続いて **構成ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="9f368-126">**ダウンロード** を選択し、**Retail Modern POS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="9f368-127">**ModernPOSSetup** ファイルのダウンロードが完了したら、**ファイルを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![ファイルを開きます](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="9f368-129">インストール プロセスを開始するには、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="9f368-130">インストールが完了したら、**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="9f368-131">Modern POS の有効化</span><span class="sxs-lookup"><span data-stu-id="9f368-131">Activate Modern POS</span></span>

1. <span data-ttu-id="9f368-132">Windows デスクトップで、 **スタート** ボタンを選択し、**Retail Modern POS** と入力します。</span><span class="sxs-lookup"><span data-stu-id="9f368-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="9f368-133">**Retail Modern POS** アプリケーションを選択して、有効化を開始します。</span><span class="sxs-lookup"><span data-stu-id="9f368-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="9f368-134">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-134">Select **Next**.</span></span> <span data-ttu-id="9f368-135">**サーバー URL**、 **デバイスID**、 **登録番号** の各フィールドには、前述の手順でダウンロードした構成ファイルの情報を使用して事前設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f368-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="9f368-136">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-136">Select **Activate**.</span></span>
5. <span data-ttu-id="9f368-137">認証ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f368-137">An authentication dialog box appears.</span></span> <span data-ttu-id="9f368-138">既に作業者 **000713-Andrew Collette** に関連付けられている電子メール アドレスを使用するアカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f368-139">作業者に ID が関連付けられていない場合、有効化は失敗します。</span><span class="sxs-lookup"><span data-stu-id="9f368-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="9f368-140">この場合は、トピック [Dynamics 365 Commerce 評価環境の構成](cpe-post-provisioning.md#associate-a-worker-with-your-identity) 配下の「作業者とあなたの ID を関連付ける」 に記載の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="9f368-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="9f368-141">組織によるデバイス管理を許可するかどうかを確認するメッセージが表示された場合は、**このアプリのみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="9f368-142">有効化が完了したら、**開始する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="9f368-143">Modern POS の BOPIS を有効化する</span><span class="sxs-lookup"><span data-stu-id="9f368-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="9f368-144">オペレーター ID に **000713**、パスワードに **123** を使用して Modern POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9f368-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="9f368-145">入門者向けチュートリアルビデオの再生中に、ダイアログボックスの左下隅にある 2 つのチェック ボックスをオンにして、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9f368-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="9f368-146">シフトの終了を確認するメッセージが表示されない場合は、**ようこそ** ページを右方向に にスクロールし、 **シフトを閉じる** を選択してから、POS に再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="9f368-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="9f368-147">サイン イン後、メッセージが表示されたら **ドロワー以外の操作の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="9f368-148">**ようこそ**  ページで右にスクロールし、**ハードウェア ステーションの選択** 操作を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="9f368-149">**管理** を選択し、**ハードウェア ステーションを使用する** オプションを **オン** に設定して **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="9f368-150">POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="9f368-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="9f368-151">ログイン後、**新規シフトを開く** を選択し、 **ドロワー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="9f368-152">BOPIS シナリオを完了する</span><span class="sxs-lookup"><span data-stu-id="9f368-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="9f368-153">店舗内集配用のウェブストア注文を作成する</span><span class="sxs-lookup"><span data-stu-id="9f368-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="9f368-154">環境の構成をする過程の [e コマースの初期化](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) ステップで指定したURLに移動します。</span><span class="sxs-lookup"><span data-stu-id="9f368-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="9f368-155">品目を選択し、**カートに追加する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="9f368-156">[ショッピングバッグ] ページで、追加した注文明細行に対して **これを選択する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="9f368-157">**店舗の選択** ダイアログ ボックスで、**サンフランシスコ** と入力し、**検索** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="9f368-158">結果の一覧で、サンフランシスコの店舗を見つけ、**ここで集荷する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="9f368-159">[ショッピングバッグ] ページで、**ゲストとしてチェックアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="9f368-160">チェックアウトを続行するには、Cookie の通知に同意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f368-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="9f368-161">この通知は、チェック アウトページの上部にバナーとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f368-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="9f368-162">クレジット カードの支払方法については、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f368-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="9f368-163">**カード名義人名:** 名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f368-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="9f368-164">**カード番号:** **4111-1111-1111-1111** を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f368-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="9f368-165">**有効期限:** **10/20** を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f368-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="9f368-166">**カードのセキュリティー コード (CVV) :** **737** を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f368-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9f368-167">どのような状況でも、テスト サイトで実際のクレジット カード情報は絶対に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="9f368-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="9f368-168">請求先住所の詳細を入力し、**保存して続行** を選択し、チェック アウトを続行します。</span><span class="sxs-lookup"><span data-stu-id="9f368-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="9f368-169">注文の準備ができたら、**チェックアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="9f368-170">オンライン注文をバック オフィスに同期します</span><span class="sxs-lookup"><span data-stu-id="9f368-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="9f368-171">オンライン注文を同期する方法の詳細については、[オンライン販売と支払の転記](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f368-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="9f368-172">店頭で注文を集荷する</span><span class="sxs-lookup"><span data-stu-id="9f368-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="9f368-173">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="9f368-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="9f368-174">**ようこそ** 画面で、**注文の履行** を選択します</span><span class="sxs-lookup"><span data-stu-id="9f368-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="9f368-175">集荷対象商品の一覧では、オンラインで注文した商品の中から明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="9f368-176">注文明細行が選択されている間、**集荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="9f368-177">[トランザクション] 画面に明細行品目が追加され、**$0.00** が期日の残高として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f368-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="9f368-178">**$0.00** の未払の残高を選択するか、取引を完了する支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f368-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9f368-179">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9f368-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="9f368-180">POS で取得したオンライン注文の残高がゼロではない場合</span><span class="sxs-lookup"><span data-stu-id="9f368-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="9f368-181">店舗内集配の注文が取得されたときに、[未払残高] が0ではない場合は、Modern POSが使用されていること、およびハードウェア ステーションが有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9f368-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="9f368-182">IOS 用 クラウド POS または Modern POS を使用している場合は、共有ハードウェア ステーションが有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9f368-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="9f368-183">オンラインで行われた支払を取得するには、何らかの形式の有効なハードウェア ステーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="9f368-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="9f368-184">決済のキャプチャに関する一般的な問題</span><span class="sxs-lookup"><span data-stu-id="9f368-184">General issues with payment capture</span></span>

<span data-ttu-id="9f368-185">すべての一般的な問題については、Modern POS またはインターネット インフォメーション サービス（IIS）ハードウェア ステーション イベント ログを常に参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f368-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="9f368-186">これらのログは、Windows イベント ログの以下のノードにあります：</span><span class="sxs-lookup"><span data-stu-id="9f368-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="9f368-187">アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="9f368-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="9f368-188">アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="9f368-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f368-189">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9f368-189">Additional resources</span></span>

[<span data-ttu-id="9f368-190">Dynamics 365 Commerce 評価環境の概要</span><span class="sxs-lookup"><span data-stu-id="9f368-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="9f368-191">Dynamics 365 Commerce 評価環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="9f368-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="9f368-192">Dynamics 365 Commerce 評価環境のオプション機能を構成する</span><span class="sxs-lookup"><span data-stu-id="9f368-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9f368-193">Dynamics 365 Commerce 評価環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="9f368-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="9f368-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="9f368-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="9f368-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="9f368-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="9f368-196">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="9f368-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="9f368-197">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="9f368-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="9f368-198">Adyen 支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="9f368-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="9f368-199">オンライン支払手段を Adyen コネクタで保存</span><span class="sxs-lookup"><span data-stu-id="9f368-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="9f368-200">オムニ チャネル支払の概要</span><span class="sxs-lookup"><span data-stu-id="9f368-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
