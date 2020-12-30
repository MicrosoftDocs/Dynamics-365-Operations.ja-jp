---
title: Dynamics 365 Commerce の評価環境を構成する
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニング後に構成する方法について説明します。
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413646"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="06425-103">Dynamics 365 Commerce の評価環境を構成する</span><span class="sxs-lookup"><span data-stu-id="06425-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06425-104">このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニング後に構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="06425-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="06425-105">概要</span><span class="sxs-lookup"><span data-stu-id="06425-105">Overview</span></span>

<span data-ttu-id="06425-106">このトピックに記載の手順は、コマースの評価環境がプロビジョニングされた後でのみ着手してください。</span><span class="sxs-lookup"><span data-stu-id="06425-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="06425-107">コマースの評価環境をプロビジョニングする方法については、[コマースの評価環境のプロビジョニング](provisioning-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06425-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="06425-108">コマースの評価環境をエンドツーエンドでプロビジョニングした後は、環境の評価を開始する前に、プロビジョニング後の追加の構成ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06425-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="06425-109">これらの手順を完了するには、Microsoft Dynamics Lifecycle Services (LCS) と Dynamics 365 Commerce を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06425-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="06425-110">始める前に</span><span class="sxs-lookup"><span data-stu-id="06425-110">Before you start</span></span>

1. <span data-ttu-id="06425-111">[LCS ポータル](https://lcs.dynamics.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="06425-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="06425-112">プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="06425-112">Go to your project.</span></span>
1. <span data-ttu-id="06425-113">トップ メニューで、**クラウド ホスト環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="06425-114">リストで環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="06425-115">右側の環境情報で、**環境にログインする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="06425-116">コマースの本部に送信されます。</span><span class="sxs-lookup"><span data-stu-id="06425-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="06425-117">右上隅にある **USRT** 法人が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="06425-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="06425-118">コマース本部でのプロビジョニング後の活動では、法人として **USRT** が常に選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="06425-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="06425-119">販売時点管理を構成する</span><span class="sxs-lookup"><span data-stu-id="06425-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="06425-120">作業者と ID の関連付け</span><span class="sxs-lookup"><span data-stu-id="06425-120">Associate a worker with your identity</span></span>

<span data-ttu-id="06425-121">作業者を ID に関連付けるには、コマース本部で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06425-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="06425-122">左側のメニューを使用して、**モジュール \> 小売りとコマース \> 従業員 \> 作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="06425-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="06425-123">リストで、次のレコードを検索し、選択します: **000713 - アンドリュー コレット**。</span><span class="sxs-lookup"><span data-stu-id="06425-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="06425-124">アクション ウィンドウで、**コマース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="06425-125">**既存の ID の関連付け** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="06425-126">**電子メールを使用した検索** の右にある **電子メール** フィールドに、電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="06425-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="06425-127">**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-127">Select **Search**.</span></span>
1. <span data-ttu-id="06425-128">名前を含むレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="06425-129">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-129">Select **OK**.</span></span>
1. <span data-ttu-id="06425-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="06425-131">クラウド POS の有効化</span><span class="sxs-lookup"><span data-stu-id="06425-131">Activate Cloud POS</span></span>

<span data-ttu-id="06425-132">LCS のクラウド POS を有効にするには、LCS で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06425-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="06425-133">トップ メニューで、**クラウド ホスト環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="06425-134">リストで環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="06425-135">右側の環境情報で、**クラウド販売時点管理にログインする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="06425-136">**次へ** を選択し て、**開始する前に** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="06425-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="06425-137">**サーバー URL** フィールドに変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="06425-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="06425-138">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-138">Select **Next**.</span></span>
1. <span data-ttu-id="06425-139">Microsoft Azure Active Directory (Azure AD) アカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="06425-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="06425-140">**店舗名** 配下で、 **サンフランシスコ** を選択し、**次へ** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="06425-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="06425-141">**レジスターとデバイス** で、**SANFRAN-1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="06425-142">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-142">Select **Activate**.</span></span> <span data-ttu-id="06425-143">サインアウトして、POS のサインイン ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="06425-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="06425-144">オペレーター ID **000713** およびパスワード **123** を使用して、クラウド POS エクスペリエンスにサインインできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="06425-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="06425-145">コマースで、サイトを設定します。</span><span class="sxs-lookup"><span data-stu-id="06425-145">Set up your site in Commerce</span></span>

<span data-ttu-id="06425-146">コマースで評価サイトの設定を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06425-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="06425-147">プロビジョニングの実行時に eコマースを初期化した際に作成した URL を使用して、コマース サイトの管理ツールにサイン インします ([eコマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="06425-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="06425-148">**Fabrikam** サイトを選択して、サイトの設定ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="06425-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="06425-149">E コマースを初期化したときに入力したドメインを選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="06425-150">**Fabrikam 拡張オンライン ストア** を既定のチャネルとして選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="06425-151">(**拡張** オンライン ストアが選択されていることを確認してください。)</span><span class="sxs-lookup"><span data-stu-id="06425-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="06425-152">既定の言語として **en-us** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="06425-153">**パス** フィールドの値はそのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="06425-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="06425-154">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-154">Select **OK**.</span></span> <span data-ttu-id="06425-155">サイトでページのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="06425-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="06425-156">ジョブの有効化</span><span class="sxs-lookup"><span data-stu-id="06425-156">Enable jobs</span></span>

<span data-ttu-id="06425-157">コマースのジョブを有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06425-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="06425-158">環境 (HQ) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="06425-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="06425-159">左側のメニューを使用して、**小売りとコマース \> 照会およびレポート \> バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="06425-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="06425-160">この手順の残りの部分は、次の各ジョブに対して完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06425-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="06425-161">小売用の注文電子メール通知の処理</span><span class="sxs-lookup"><span data-stu-id="06425-161">Process retail order email notification</span></span>
    * <span data-ttu-id="06425-162">製品の使用可能性</span><span class="sxs-lookup"><span data-stu-id="06425-162">Product availability</span></span>
    * <span data-ttu-id="06425-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="06425-163">P-0001</span></span>
    * <span data-ttu-id="06425-164">注文ジョブを同期します</span><span class="sxs-lookup"><span data-stu-id="06425-164">Synchronize orders job</span></span>

1. <span data-ttu-id="06425-165">クイック フィルターを使用して、名前でジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="06425-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="06425-166">ジョブの状態が **実行中** の場合、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06425-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="06425-167">レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-167">Select the record.</span></span>
    1. <span data-ttu-id="06425-168">アクション ウィンドウの、**バッチ ジョブ** タブで、**状態の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="06425-169">**キャンセル** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="06425-170">必要に応じて、以下のジョブの繰り返し間隔を1分に設定することも可能です。</span><span class="sxs-lookup"><span data-stu-id="06425-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="06425-171">小売用の注文電子メール通知ジョブの処理</span><span class="sxs-lookup"><span data-stu-id="06425-171">Process retail order email notification job</span></span>
* <span data-ttu-id="06425-172">P-0001 ジョブ</span><span class="sxs-lookup"><span data-stu-id="06425-172">P-0001 job</span></span>
* <span data-ttu-id="06425-173">注文ジョブを同期します</span><span class="sxs-lookup"><span data-stu-id="06425-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="06425-174">完全データ同期の実行</span><span class="sxs-lookup"><span data-stu-id="06425-174">Run full data synchronization</span></span>

<span data-ttu-id="06425-175">コマースで完全なデータ同期を実行するには、コマース本部で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06425-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="06425-176">左側のメニューを使用して、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース スケジューラ \> チャネル データベース** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="06425-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="06425-177">使用可能な他のチャネル **scXXXXXXXXX** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="06425-178">アクション ウィンドウで、**完全なデータの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="06425-179">配送スケジュールとして **9999** を入力します。</span><span class="sxs-lookup"><span data-stu-id="06425-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="06425-180">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-180">Select **OK**.</span></span>
1. <span data-ttu-id="06425-181">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06425-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="06425-182">テスト購買を実行するためのクレジット カード情報のテスト</span><span class="sxs-lookup"><span data-stu-id="06425-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="06425-183">サイトでテスト トランザクションを実行するには、次のテスト クレジット カード情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="06425-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="06425-184">**カード番号:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="06425-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="06425-185">**有効期限:** 10/20</span><span class="sxs-lookup"><span data-stu-id="06425-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="06425-186">**カード検証値 (CVV) コード:** 737</span><span class="sxs-lookup"><span data-stu-id="06425-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06425-187">どのような状況でも、テスト サイトで実際のクレジット カード情報は絶対に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="06425-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="06425-188">次のステップ</span><span class="sxs-lookup"><span data-stu-id="06425-188">Next steps</span></span>

<span data-ttu-id="06425-189">プロビジョニングと構成の手順が完了したら、評価環境を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="06425-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="06425-190">コマース サイト ビルダーの URL を使用して、作成エクスペリエンスに移動します。</span><span class="sxs-lookup"><span data-stu-id="06425-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="06425-191">コマース サイトの URL を使用して、小売顧客サイト エクスペリエンスに移動します。</span><span class="sxs-lookup"><span data-stu-id="06425-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="06425-192">コマースの評価環境のオプション機能を構成するには、[コマース評価環境のオプション機能を構成する](cpe-optional-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06425-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06425-193">追加リソース</span><span class="sxs-lookup"><span data-stu-id="06425-193">Additional resources</span></span>

[<span data-ttu-id="06425-194">Dynamics 365 Commerce 評価環境の概要</span><span class="sxs-lookup"><span data-stu-id="06425-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="06425-195">Dynamics 365 Commerce 評価環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="06425-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="06425-196">Dynamics 365 Commerce 評価環境のオプション機能を構成する</span><span class="sxs-lookup"><span data-stu-id="06425-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="06425-197">Dynamics 365 Commerce 評価環境で BOPIS を構成する</span><span class="sxs-lookup"><span data-stu-id="06425-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="06425-198">Dynamics 365 Commerce 評価環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="06425-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="06425-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="06425-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="06425-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="06425-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="06425-201">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="06425-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="06425-202">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="06425-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
