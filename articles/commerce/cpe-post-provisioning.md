---
title: Dynamics 365 Commerce 評価環境のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニング後に構成する方法について説明します。
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b291a6515c6a3ae7382ea2ad8024ca036489de19
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937041"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="6a308-103">Dynamics 365 Commerce 評価環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6a308-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a308-104">このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニング後に構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a308-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="6a308-105">このトピックに記載の手順は、コマースの評価環境がプロビジョニングされた後でのみ着手してください。</span><span class="sxs-lookup"><span data-stu-id="6a308-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="6a308-106">コマースの評価環境をプロビジョニングする方法については、[コマースの評価環境のプロビジョニング](provisioning-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a308-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="6a308-107">コマースの評価環境をエンドツーエンドでプロビジョニングした後は、環境の評価を開始する前に、プロビジョニング後の追加の構成ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a308-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="6a308-108">これらの手順を完了するには、Microsoft Dynamics Lifecycle Services (LCS) と Dynamics 365 Commerce を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a308-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="6a308-109">始める前に</span><span class="sxs-lookup"><span data-stu-id="6a308-109">Before you start</span></span>

1. <span data-ttu-id="6a308-110">[LCS ポータル](https://lcs.dynamics.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="6a308-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="6a308-111">プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="6a308-111">Go to your project.</span></span>
1. <span data-ttu-id="6a308-112">トップ メニューで、**クラウド ホスト環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="6a308-113">リストで環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="6a308-114">右側の環境情報で、**環境にログインする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="6a308-115">コマースの本部に送信されます。</span><span class="sxs-lookup"><span data-stu-id="6a308-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="6a308-116">右上隅にある **USRT** 法人が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a308-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="6a308-117">コマース本部でのプロビジョニング後の活動では、法人として **USRT** が常に選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6a308-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="6a308-118">販売時点管理を構成する</span><span class="sxs-lookup"><span data-stu-id="6a308-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="6a308-119">作業者と ID の関連付け</span><span class="sxs-lookup"><span data-stu-id="6a308-119">Associate a worker with your identity</span></span>

<span data-ttu-id="6a308-120">作業者を ID に関連付けるには、コマース本部で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6a308-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="6a308-121">左側のメニューを使用して、**モジュール \> 小売りとコマース \> 従業員 \> 作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a308-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="6a308-122">リストで、次のレコードを検索し、選択します: **000713 - アンドリュー コレット**。</span><span class="sxs-lookup"><span data-stu-id="6a308-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="6a308-123">アクション ウィンドウで、**コマース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="6a308-124">**既存の ID の関連付け** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="6a308-125">**電子メールを使用した検索** の右にある **電子メール** フィールドに、電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="6a308-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="6a308-126">**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-126">Select **Search**.</span></span>
1. <span data-ttu-id="6a308-127">名前を含むレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="6a308-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-128">Select **OK**.</span></span>
1. <span data-ttu-id="6a308-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="6a308-130">クラウド POS の有効化</span><span class="sxs-lookup"><span data-stu-id="6a308-130">Activate Cloud POS</span></span>

<span data-ttu-id="6a308-131">LCS のクラウド POS を有効にするには、LCS で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6a308-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="6a308-132">トップ メニューで、**クラウド ホスト環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="6a308-133">リストで環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="6a308-134">右側の環境情報で、**クラウド販売時点管理にログインする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="6a308-135">**次へ** を選択し て、**開始する前に** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a308-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="6a308-136">**サーバー URL** フィールドに変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6a308-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="6a308-137">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-137">Select **Next**.</span></span>
1. <span data-ttu-id="6a308-138">Microsoft Azure Active Directory (Azure AD) アカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="6a308-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="6a308-139">**店舗名** 配下で、 **サンフランシスコ** を選択し、**次へ** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="6a308-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="6a308-140">**レジスターとデバイス** で、**SANFRAN-1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="6a308-141">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-141">Select **Activate**.</span></span> <span data-ttu-id="6a308-142">サインアウトして、POS のサインイン ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="6a308-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="6a308-143">オペレーター ID **000713** およびパスワード **123** を使用して、クラウド POS エクスペリエンスにサインインできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6a308-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="6a308-144">コマースで、サイトを設定します。</span><span class="sxs-lookup"><span data-stu-id="6a308-144">Set up your site in Commerce</span></span>

<span data-ttu-id="6a308-145">コマースで評価サイトの設定を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6a308-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6a308-146">プロビジョニングの実行時に eコマースを初期化した際に作成した URL を使用して、コマース サイトの管理ツールにサイン インします ([eコマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="6a308-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="6a308-147">**Fabrikam** サイトを選択して、サイトの設定ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a308-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="6a308-148">E コマースを初期化したときに入力したドメインを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="6a308-149">**Fabrikam 拡張オンライン ストア** を既定のチャネルとして選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="6a308-150">(**拡張** オンライン ストアが選択されていることを確認してください。)</span><span class="sxs-lookup"><span data-stu-id="6a308-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="6a308-151">既定の言語として **en-us** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="6a308-152">**パス** フィールドの値はそのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="6a308-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="6a308-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-153">Select **OK**.</span></span> <span data-ttu-id="6a308-154">サイトでページのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a308-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="6a308-155">ジョブの有効化</span><span class="sxs-lookup"><span data-stu-id="6a308-155">Enable jobs</span></span>

<span data-ttu-id="6a308-156">コマースのジョブを有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6a308-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6a308-157">環境 (HQ) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="6a308-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="6a308-158">左側のメニューを使用して、**小売りとコマース \> 照会およびレポート \> バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a308-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="6a308-159">この手順の残りの部分は、次の各ジョブに対して完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a308-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="6a308-160">小売用の注文電子メール通知の処理</span><span class="sxs-lookup"><span data-stu-id="6a308-160">Process retail order email notification</span></span>
    * <span data-ttu-id="6a308-161">製品の使用可能性</span><span class="sxs-lookup"><span data-stu-id="6a308-161">Product availability</span></span>
    * <span data-ttu-id="6a308-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="6a308-162">P-0001</span></span>
    * <span data-ttu-id="6a308-163">注文ジョブを同期します</span><span class="sxs-lookup"><span data-stu-id="6a308-163">Synchronize orders job</span></span>

1. <span data-ttu-id="6a308-164">クイック フィルターを使用して、名前でジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="6a308-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="6a308-165">ジョブの状態が **実行中** の場合、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6a308-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="6a308-166">レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-166">Select the record.</span></span>
    1. <span data-ttu-id="6a308-167">アクション ウィンドウの、**バッチ ジョブ** タブで、**状態の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="6a308-168">**キャンセル** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="6a308-169">必要に応じて、以下のジョブの繰り返し間隔を1分に設定することも可能です。</span><span class="sxs-lookup"><span data-stu-id="6a308-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="6a308-170">小売用の注文電子メール通知ジョブの処理</span><span class="sxs-lookup"><span data-stu-id="6a308-170">Process retail order email notification job</span></span>
* <span data-ttu-id="6a308-171">P-0001 ジョブ</span><span class="sxs-lookup"><span data-stu-id="6a308-171">P-0001 job</span></span>
* <span data-ttu-id="6a308-172">注文ジョブを同期します</span><span class="sxs-lookup"><span data-stu-id="6a308-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="6a308-173">完全データ同期の実行</span><span class="sxs-lookup"><span data-stu-id="6a308-173">Run full data synchronization</span></span>

<span data-ttu-id="6a308-174">コマースで完全なデータ同期を実行するには、コマース本部で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6a308-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="6a308-175">左側のメニューを使用して、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース スケジューラ \> チャネル データベース** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a308-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="6a308-176">使用可能な他のチャネル **scXXXXXXXXX** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="6a308-177">アクション ウィンドウで、**完全なデータの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="6a308-178">配送スケジュールとして **9999** を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a308-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="6a308-179">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-179">Select **OK**.</span></span>
1. <span data-ttu-id="6a308-180">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a308-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="6a308-181">テスト購買を実行するためのクレジット カード情報のテスト</span><span class="sxs-lookup"><span data-stu-id="6a308-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="6a308-182">サイトでテスト トランザクションを実行するには、次のテスト クレジット カード情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a308-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="6a308-183">**カード番号:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="6a308-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="6a308-184">**有効期限:** 10/20</span><span class="sxs-lookup"><span data-stu-id="6a308-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="6a308-185">**カード検証値 (CVV) コード:** 737</span><span class="sxs-lookup"><span data-stu-id="6a308-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a308-186">どのような状況でも、テスト サイトで実際のクレジット カード情報は絶対に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6a308-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6a308-187">次のステップ</span><span class="sxs-lookup"><span data-stu-id="6a308-187">Next steps</span></span>

<span data-ttu-id="6a308-188">プロビジョニングと構成の手順が完了したら、評価環境を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6a308-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="6a308-189">コマース サイト ビルダーの URL を使用して、作成エクスペリエンスに移動します。</span><span class="sxs-lookup"><span data-stu-id="6a308-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="6a308-190">コマース サイトの URL を使用して、小売顧客サイト エクスペリエンスに移動します。</span><span class="sxs-lookup"><span data-stu-id="6a308-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="6a308-191">コマースの評価環境のオプション機能を構成するには、[コマース評価環境のオプション機能を構成する](cpe-optional-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a308-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a308-192">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6a308-192">Additional resources</span></span>

[<span data-ttu-id="6a308-193">Dynamics 365 Commerce 評価環境の概要</span><span class="sxs-lookup"><span data-stu-id="6a308-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="6a308-194">Dynamics 365 Commerce 評価環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="6a308-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="6a308-195">Dynamics 365 Commerce 評価環境のオプション機能を構成する</span><span class="sxs-lookup"><span data-stu-id="6a308-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="6a308-196">Dynamics 365 Commerce 評価環境で BOPIS を構成する</span><span class="sxs-lookup"><span data-stu-id="6a308-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="6a308-197">Dynamics 365 Commerce 評価環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="6a308-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="6a308-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6a308-198">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="6a308-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="6a308-199">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="6a308-200">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="6a308-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="6a308-201">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="6a308-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]