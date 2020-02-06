---
title: Commerce プレビュー環境のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境をプロビジョニング後にコンフィギュレーションする方法について説明します。
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906142"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="8c4e4-103">Commerce プレビュー環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8c4e4-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8c4e4-104">このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境をプロビジョニング後にコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="8c4e4-105">概要</span><span class="sxs-lookup"><span data-stu-id="8c4e4-105">Overview</span></span>

<span data-ttu-id="8c4e4-106">このトピックの手順は、Commerce プレビュー環境がプロビジョニングされた後にのみ完了してください。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="8c4e4-107">Commerce プレビュー環境をプロビジョニングする方法については、[Commerce プレビュー環境のプロビジョニング](provisioning-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="8c4e4-108">Commerce プレビュー環境をエンドツーエンドでプロビジョニングした後、環境の評価を開始する前に、追加のプロビジョニング後のコンフィギュレーション手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="8c4e4-109">これらの手順を完了するには、Microsoft Dynamics Lifecycle Services (LCS)、Dynamics 365 Commerce、および Dynamics 365 Retail を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="8c4e4-110">始める前に</span><span class="sxs-lookup"><span data-stu-id="8c4e4-110">Before you start</span></span>

1. <span data-ttu-id="8c4e4-111">[LCS ポータル](https://lcs.dynamics.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="8c4e4-112">プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-112">Go to your project.</span></span>
1. <span data-ttu-id="8c4e4-113">トップ メニューで、**クラウド ホスト環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="8c4e4-114">リストで環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="8c4e4-115">右側の環境情報で、**完全な詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="8c4e4-116">**ログイン**を選択してメニューを開き、**環境にログオン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="8c4e4-117">右上隅にある **USRT** 法人が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="8c4e4-118">LCS での販売時点のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8c4e4-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="8c4e4-119">作業者と ID の関連付け</span><span class="sxs-lookup"><span data-stu-id="8c4e4-119">Associate a worker with your identity</span></span>

<span data-ttu-id="8c4e4-120">LCS で作業者を ID に関連付けるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="8c4e4-121">左側のメニューを使用して、**モジュール \> Retail \> 従業員 \> 作業者**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="8c4e4-122">リストで、次のレコードを検索し、選択します: **000713 - アンドリュー コレット**。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="8c4e4-123">アクション ウィンドウで、**Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="8c4e4-124">**既存の ID の関連付け**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="8c4e4-125">**電子メールを使用した検索**の右にある**電子メール** フィールドに、電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="8c4e4-126">**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-126">Select **Search**.</span></span>
1. <span data-ttu-id="8c4e4-127">名前を含むレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="8c4e4-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-128">Select **OK**.</span></span>
1. <span data-ttu-id="8c4e4-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="8c4e4-130">クラウド POS の有効化</span><span class="sxs-lookup"><span data-stu-id="8c4e4-130">Activate Cloud POS</span></span>

<span data-ttu-id="8c4e4-131">LCS のクラウド POS を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="8c4e4-132">トップ メニューで、**クラウド ホスト環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="8c4e4-133">リストで環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="8c4e4-134">右側の環境情報で、**完全な詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="8c4e4-135">**ログイン**を選択してメニューを開き、**クラウド販売時点管理にログオンする**を選択して販売時点管理 (POS) を開きます。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="8c4e4-136">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-136">Select **Next**.</span></span>
1. <span data-ttu-id="8c4e4-137">Microsoft Azure Active Directory (Azure AD) アカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="8c4e4-138">**店舗名**で、**サンフランシスコ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="8c4e4-139">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-139">Select **Next**.</span></span>
1. <span data-ttu-id="8c4e4-140">**レジスターとデバイス**で、**SANFRAN-1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="8c4e4-141">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-141">Select **Activate**.</span></span> <span data-ttu-id="8c4e4-142">サインアウトして、POS のサインイン ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="8c4e4-143">オペレーター ID **000713** およびパスワード **123** を使用して、クラウド POS エクスペリエンスにサインインできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="8c4e4-144">コマースで、サイトを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-144">Set up your site in Commerce</span></span>

<span data-ttu-id="8c4e4-145">コマースでプレビュー サイトの設定を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8c4e4-146">プロビジョニング中に E コマースを初期化したときに作成した URL を使用して、サイト管理ツールにサインインします ([E コマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="8c4e4-147">**Fabrikam** サイトを選択して、サイトの設定ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="8c4e4-148">E コマースを初期化したときに入力したドメインを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="8c4e4-149">**Fabrikam 拡張オンライン ストア**を既定のチャネルとして選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="8c4e4-150">(**拡張**オンライン ストアが選択されていることを確認してください。)</span><span class="sxs-lookup"><span data-stu-id="8c4e4-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="8c4e4-151">既定の言語として **en-us** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="8c4e4-152">**パス** フィールドの値はそのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="8c4e4-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-153">Select **OK**.</span></span> <span data-ttu-id="8c4e4-154">サイトでページのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="8c4e4-155">Retail のジョブの有効化</span><span class="sxs-lookup"><span data-stu-id="8c4e4-155">Enable jobs in Retail</span></span>

<span data-ttu-id="8c4e4-156">Retail のジョブを有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="8c4e4-157">環境 (HQ) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="8c4e4-158">左側のメニューを使用して、**Retail \> 照会およびレポート \> バッチ ジョブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="8c4e4-159">この手順の残りの部分は、次の各ジョブに対して完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="8c4e4-160">小売用の注文電子メール通知の処理</span><span class="sxs-lookup"><span data-stu-id="8c4e4-160">Process retail order email notification</span></span>
    * <span data-ttu-id="8c4e4-161">製品の使用可能性</span><span class="sxs-lookup"><span data-stu-id="8c4e4-161">Product availability</span></span>
    * <span data-ttu-id="8c4e4-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="8c4e4-162">P-0001</span></span>
    * <span data-ttu-id="8c4e4-163">注文ジョブを同期します</span><span class="sxs-lookup"><span data-stu-id="8c4e4-163">Synchronize orders job</span></span>

1. <span data-ttu-id="8c4e4-164">クイック フィルターを使用して、名前でジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="8c4e4-165">ジョブの状態が**源泉徴収**の場合、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="8c4e4-166">レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-166">Select the record.</span></span>
    1. <span data-ttu-id="8c4e4-167">アクション ウィンドウの、**バッチ ジョブ** タブで、**状態の変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="8c4e4-168">**待機中**を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="8c4e4-169">Retail で完全なデータ同期の実行</span><span class="sxs-lookup"><span data-stu-id="8c4e4-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="8c4e4-170">Retail で完全なデータ同期を実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="8c4e4-171">左側にあるメニューを使用して、**モジュール \> Retail \> 本社の設定 \> 小売用スケジューラ \> チャネル データベース**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="8c4e4-172">左側のリストで、**既定**のチャネルが選択できます。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="8c4e4-173">使用可能な他のチャンネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-173">Select the other available channel.</span></span> <span data-ttu-id="8c4e4-174">このチャンネルは **scXXXXXXXXX** と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="8c4e4-175">アクション ウィンドウで、**完全なデータの同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="8c4e4-176">配送スケジュールとして **9999** を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="8c4e4-177">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-177">Select **OK**.</span></span>
1. <span data-ttu-id="8c4e4-178">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="8c4e4-179">テスト購買を実行するためのクレジット カード情報のテスト</span><span class="sxs-lookup"><span data-stu-id="8c4e4-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="8c4e4-180">サイトでテスト トランザクションを実行するには、次のテスト クレジット カード情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="8c4e4-181">**カード番号:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="8c4e4-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="8c4e4-182">**有効期限:** 10/20</span><span class="sxs-lookup"><span data-stu-id="8c4e4-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="8c4e4-183">**カード検証値 (CVV) コード:** 737</span><span class="sxs-lookup"><span data-stu-id="8c4e4-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c4e4-184">どのような状況でも、テスト サイトで実際のクレジット カード情報は絶対に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8c4e4-185">次のステップ</span><span class="sxs-lookup"><span data-stu-id="8c4e4-185">Next steps</span></span>

<span data-ttu-id="8c4e4-186">プロビジョニングとコンフィギュレーションの手順が完了したら、プレビュー環境を評価する準備ができています。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="8c4e4-187">コマース サイト管理ツールの URL を使用して、作成エクスペリエンスに移動します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="8c4e4-188">コマース サイトの URL を使用して、小売顧客サイト エクスペリエンスに移動します。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="8c4e4-189">Commerce プレビュー環境のオプション機能をコンフィギュレーションするには、[Commerce プレビュー環境のオプション機能のコンフィギュレーション](cpe-optional-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c4e4-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c4e4-190">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8c4e4-190">Additional resources</span></span>

[<span data-ttu-id="8c4e4-191">Commerce プレビュー環境の概要</span><span class="sxs-lookup"><span data-stu-id="8c4e4-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8c4e4-192">Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="8c4e4-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="8c4e4-193">Commerce プレビュー環境のオプション機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8c4e4-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="8c4e4-194">Commerce プレビュー環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="8c4e4-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="8c4e4-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8c4e4-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="8c4e4-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="8c4e4-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="8c4e4-197">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="8c4e4-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="8c4e4-198">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="8c4e4-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="8c4e4-199">Dynamics 365 Retail のヘルプ リソース</span><span class="sxs-lookup"><span data-stu-id="8c4e4-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)