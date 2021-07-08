---
title: Lifecycle Services (LCS) のサブスクリプション試算
description: このトピックでは、Lifecycle Services (LCS) で利用可能なサブスクリプション試算ツールを使用する方法について説明します。
author: angelmarshall
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 730c4fa2d5d4e349f8e0e0287f4f37b7589078f4
ms.sourcegitcommit: c9f55e64416d0bbedfdadafb00e4181921ad0f37
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261924"
---
# <a name="subscription-estimator-in-lifecycle-services-lcs"></a><span data-ttu-id="cdb21-103">Lifecycle Services (LCS) のサブスクリプション試算</span><span class="sxs-lookup"><span data-stu-id="cdb21-103">Subscription estimator in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdb21-104">サブスクリプション見積もりツールは、Microsoft Dynamics Lifecycle Services (LCS) で使用できるツールです。</span><span class="sxs-lookup"><span data-stu-id="cdb21-104">Subscription estimator is a tool that is available in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cdb21-105">Microsoft は、このツールを使用して、顧客に対して準備する必要がある実稼働環境の初期サイズを見積ります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-105">Microsoft uses this tool to estimate the initial size of the production environment that must be provisioned for a customer.</span></span> <span data-ttu-id="cdb21-106">顧客が実稼働環境の配置を要求する前に、トランザクション カウントの観点からピーク作業負荷を見積もり、その情報を LCS にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-106">Before customers can request deployment of a production environment, they must estimate their peak workloads in terms of transaction counts and then upload that information to LCS.</span></span> <span data-ttu-id="cdb21-107">ユーザー ライセンスの詳細およびトランザクション カウントを使用してサブスクリプション要件を推測することにより、サブスクリプション見積もりツールは、プロビジョニングされた環境が顧客の業務要件を満たしていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-107">By using the details of user licenses and transaction counts to infer subscription requirements, the Subscription estimator tool helps ensure that the provisioned environment meets the customer's business requirements.</span></span>

<span data-ttu-id="cdb21-108">サブスクリプション試算ツールを使用するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cdb21-108">Follow these steps to use the Subscription estimator tool.</span></span>

1. <span data-ttu-id="cdb21-109">LCS で、実装プロジェクトに関連付けられているプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-109">In LCS, open the project that is associated with the implementation project.</span></span>
2. <span data-ttu-id="cdb21-110">ページの上部にあるハンバーガー アイコン選択し、**サブスクリプション見積もりツール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-110">At the top of the page, select the hamburger icon, and then select **Subscription estimator**.</span></span>

    <span data-ttu-id="cdb21-111">[![サブスクリプション見積もりツール](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)</span><span class="sxs-lookup"><span data-stu-id="cdb21-111">[![subscription estimator](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)</span></span>

3. <span data-ttu-id="cdb21-112">サンプルの使用状況プロファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="cdb21-112">Download the sample usage profile.</span></span>
4. <span data-ttu-id="cdb21-113">各タブで必要な質問に回答します。Commerce の顧客の場合は、**Retail と Commerce** タブ上の質問に回答してください。</span><span class="sxs-lookup"><span data-stu-id="cdb21-113">Answer the required questions on each tab. If you're a Commerce customer, be sure to answer the questions on the **Retail and Commerce** tab.</span></span>
5. <span data-ttu-id="cdb21-114">使用状況プロファイルをローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-114">Save the usage profile locally.</span></span>
6. <span data-ttu-id="cdb21-115">使用プロファイルをアップロードするには、**新しい見積もり** を選択し、見積もりに名前を付け、使用プロファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="cdb21-115">To upload the usage profile, select **New estimate**, name the estimate, and then upload the usage profile.</span></span>
7. <span data-ttu-id="cdb21-116">アップロードが完了した後、**アクティブとしてマークする** を選択し見積もりを有効にします。</span><span class="sxs-lookup"><span data-stu-id="cdb21-116">After the upload is completed, select **Mark as Active** to activate an estimate.</span></span> <span data-ttu-id="cdb21-117">生産の配置をコンフィギュレーションするために有効な見積が必要です。</span><span class="sxs-lookup"><span data-stu-id="cdb21-117">An active estimate is required in order to configure a production deployment.</span></span>

<span data-ttu-id="cdb21-118">有効でアクティブな見積があるときは、**構成** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-118">When there is a valid active estimate, the **Configure** button becomes available.</span></span> <span data-ttu-id="cdb21-119">このボタンを使用すると、製造環境の展開を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-119">You can use this button to request a production environment deployment.</span></span>

## <a name="edit-the-estimate-for-multiple-implementation-projects"></a><span data-ttu-id="cdb21-120">複数の実装プロジェクトの見積を編集する</span><span class="sxs-lookup"><span data-stu-id="cdb21-120">Edit the estimate for multiple implementation projects</span></span>
<span data-ttu-id="cdb21-121">複数の実装プロジェクトの見積を編集するためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-121">To edit the estimate for multiple implementation projects, follow these steps:</span></span>

1.  <span data-ttu-id="cdb21-122">各実装プロジェクトのサブスクリプション試算ツールを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdb21-122">Visit the Subscription Estimator tool for each implementation project.</span></span> <span data-ttu-id="cdb21-123">有効なサブスクリプション見積を編集して、各プロジェクトにライセンス配賦を適用します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-123">Edit the active subscription estimate to apply the license allocation for each project.</span></span>
2.  <span data-ttu-id="cdb21-124">サブスクリプション見積をサブスクリプション試算ツールで編集するには、見積を選択してから **見積編集** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-124">A subscription estimate can be edited in the Subscription estimator tool by selecting an estimate and then selecting the **Edit estimate** button.</span></span> 
    <span data-ttu-id="cdb21-125">[![サブスクリプション見積編集ボタン](./media/SubscriptionEstimatorWithEdit.jpg)](./media/SubscriptionEstimatorWithEdit.jpg)</span><span class="sxs-lookup"><span data-stu-id="cdb21-125">[![Subscription estimator edit button](./media/SubscriptionEstimatorWithEdit.jpg)](./media/SubscriptionEstimatorWithEdit.jpg)</span></span>
3.  <span data-ttu-id="cdb21-126">ダイアログ ボックスで、Finance and Operations ライセンスの各タイプのライセンス数を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-126">Enter the license count for each type of Finance and Operations license in the dialog box.</span></span> <span data-ttu-id="cdb21-127">既定では、各サブスクリプション見積は割り当てられたすべての購入されたライセンスの全数で作成されます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-127">By default, every subscription estimate will be created with the full count of all purchased licenses assigned to it.</span></span> <span data-ttu-id="cdb21-128">顧客は、ライセンスの総数以上を単一の見積に割り当てること、および割り当てられた金額を Dynamics 365 ライセンス ポリシーによって要求されている最低金額以下に減らすことはできません。</span><span class="sxs-lookup"><span data-stu-id="cdb21-128">Customers cannot allocate more than the total number of licenses to a single estimate and cannot reduce the allocated amount to less than the minimum required by the Dynamics 365 Licensing policy.</span></span>
    <span data-ttu-id="cdb21-129">[![サブスクリプション見積編集ダイアログ](./media/SubscriptionEstimatorEditDialog.jpg)](./media/SubscriptionEstimatorEditDialog.jpg)</span><span class="sxs-lookup"><span data-stu-id="cdb21-129">[![Subscription estimator edit dialog](./media/SubscriptionEstimatorEditDialog.jpg)](./media/SubscriptionEstimatorEditDialog.jpg)</span></span>
4.  <span data-ttu-id="cdb21-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-130">Select **Save**.</span></span> <span data-ttu-id="cdb21-131">警告情報を読んで、それに同意します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-131">Read and agree to the warning information.</span></span>  
    <span data-ttu-id="cdb21-132">[![サブスクリプション見積の有効な編集警告](./media/SubscriptionEstimatorEditDialogWarning.jpg)](./media/SubscriptionEstimatorEditDialogWarning.jpg)</span><span class="sxs-lookup"><span data-stu-id="cdb21-132">[![Subscription estimator active edit warning](./media/SubscriptionEstimatorEditDialogWarning.jpg)](./media/SubscriptionEstimatorEditDialogWarning.jpg)</span></span>

[!NOTE] <span data-ttu-id="cdb21-133">複数の見積を使用できますが、1 つの見積にアクティブとマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-133">Although you can have multiple estimates, one estimate must be marked as Active.</span></span> <span data-ttu-id="cdb21-134">実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-134">After the production environment has been deployed, or deployment of the environment has received sign-off, the active estimate is locked.</span></span> <span data-ttu-id="cdb21-135">有効な見積を変更したり、新しい見積を有効としてマークしたりすると、実稼働環境のサイズが変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-135">Any further changes to the active estimate or marking a new estimate as active may cause the production environment to be resized.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="cdb21-136">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="cdb21-136">Frequently asked questions</span></span>

### <a name="why-isnt-the-configure-button-for-deploying-a-production-environment-available-even-though-there-is-an-active-estimate-and-why-does-a-warning-message-appear-in-the-action-center-on-the-project-dashboard"></a><span data-ttu-id="cdb21-137">アクティブな見積があるにもかかわらず、実稼動環境の **コンフィギュレーション** ボタンが有効なのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="cdb21-137">Why isn't the **Configure** button for deploying a production environment available, even though there is an active estimate?</span></span> <span data-ttu-id="cdb21-138">また、プロジェクト ダッシュ ボード上のアクション センターに警告メッセージが表示されるのはなぜでしょうか?</span><span class="sxs-lookup"><span data-stu-id="cdb21-138">And why does a warning message appear in the Action Center on the project dashboard?</span></span>

<span data-ttu-id="cdb21-139">複数の実装プロジェクトがある場合、**コンフィギュレーション** ボタンを有効にされていない可能性があり、アクション センターに不足しているライセンス数に関する警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-139">If you have multiple implementation projects, the **Configure** button might not be enabled and a warning message will appear in the Action Center regarding an insufficient number of licenses.</span></span> <span data-ttu-id="cdb21-140">見積編集機能を使用すると、サブスクリプション試算ツール内の有効なサブスクリプション見積を編集して、そのプロジェクトに必要なライセンス配賦を適用できます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-140">With the Edit estimate function, you can  edit an active subscription estimate within the Subscription Estimator tool to apply the desired license allocation for that project.</span></span>

### <a name="why-does-an-error-occur-when-i-mark-an-estimate-as-active"></a><span data-ttu-id="cdb21-141">見積に **有効** とマークするとエラーが発生するのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="cdb21-141">Why does an error occur when I mark an estimate as **Active**?</span></span>

<span data-ttu-id="cdb21-142">見積を **有効** とマークすると、次のエラー メッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-142">When you mark an estimate as **Active**, you might receive the following error message:</span></span>

<span data-ttu-id="cdb21-143">*見積が作成されましたが、要件を満たしていません*</span><span class="sxs-lookup"><span data-stu-id="cdb21-143">*Estimate created but does not meet requirements*</span></span>

<span data-ttu-id="cdb21-144">このエラーは、入力されたトランザクション明細行がサブスクリプション見積ツールの制限内にない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-144">This error occurs if transaction lines that are entered aren't within the limits of the Subscription estimation tool.</span></span> <span data-ttu-id="cdb21-145">このエラーを解決するには、サポート要求を作成し、使用プロファイルを添付します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-145">To resolve this error, create a support request, and attach the usage profile.</span></span> <span data-ttu-id="cdb21-146">次に、インスタンスのサイズを手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-146">Your instance can then be manually sized.</span></span>

### <a name="how-can-i-update-my-subscription-if-my-production-environment-is-deployed"></a><span data-ttu-id="cdb21-147">実稼動環境が配置されている場合、どのようにサブスクリプションを更新ことができますか?</span><span class="sxs-lookup"><span data-stu-id="cdb21-147">How can I update my subscription if my production environment is deployed?</span></span>

<span data-ttu-id="cdb21-148">[サブスクリプション見積](subscription-estimator.md) は、実働の要求をする前に必要なステップです。</span><span class="sxs-lookup"><span data-stu-id="cdb21-148">The [Subscription estimator](subscription-estimator.md) is a required step before requesting production.</span></span> <span data-ttu-id="cdb21-149">複数の見積を使用できますが、1 つの見積に **有効** とマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-149">Although you can have multiple estimates, one estimate must be marked as  **Active**.</span></span> <span data-ttu-id="cdb21-150">有効なサブスクリプション見積を使用して、実稼働環境のサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-150">The active subscription estimate is used to size the production environment.</span></span> <span data-ttu-id="cdb21-151">実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。</span><span class="sxs-lookup"><span data-stu-id="cdb21-151">After the production environment has been deployed, or deployment of the environment has received sign-off, the active estimate is locked.</span></span> <span data-ttu-id="cdb21-152">有効なサブスクリプション見積を編集するには、サブスクリプション試算ツール内の見積編集機能を選択して、ライセンス配賦を更新します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-152">To edit an active subscription estimate, select the Edit estimate function within the Subscription Estimator tool to update your license allocation.</span></span>

### <a name="what-should-i-do-to-activate-my-subscription-estimate-if-i-have-multiple-projects-in-the-same-tenant"></a><span data-ttu-id="cdb21-153">同じテナントに複数のプロジェクトがある場合、サブスクリプション見積を有効にするには何をする必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="cdb21-153">What should I do to activate my subscription estimate if I have multiple projects in the same tenant?</span></span>

<span data-ttu-id="cdb21-154">同じテナント内に複数のプロジェクトを実装する場合、LCS のアクション センターに「*サブスクリプションの見積が完了していない*」ことを示す警告が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-154">When you are implementing several projects in the same tenant, a warning indicating "*subscription estimate is not complete*" may appear in the Action Center of LCS.</span></span> <span data-ttu-id="cdb21-155">このエラーは、すべての実装プロジェクトの見積ユーザーの数が、購入したライセンスの数を超えないようにする必要があることを示しています。</span><span class="sxs-lookup"><span data-stu-id="cdb21-155">This error will indicate that the total number of estimated users for all implementation projects should not exceed the number of purchased licenses.</span></span> <span data-ttu-id="cdb21-156">これは、有効なサブスクリプション見積のユーザーの合計が、同じタイプのテナント ライセンス数を上回っている場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="cdb21-156">This may happen if the sum of users on the active subscription estimates is superior to the tenant license count of the same type.</span></span> <span data-ttu-id="cdb21-157">有効なサブスクリプション見積を編集するには、サブスクリプション試算ツール内の見積編集機能を選択して、ライセンス配賦を更新します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-157">To edit active subscription estimate, select the Edit estimate function within the Subscription Estimator tool to update your license allocation.</span></span>

> [!NOTE]
> <span data-ttu-id="cdb21-158">FastTrack ソリューション アーキテクトは、サブスクリプション見積のアップロードまたは更新には関与していません。</span><span class="sxs-lookup"><span data-stu-id="cdb21-158">FastTrack Solutions architects are not involved in uploading or updating the Subscription Estimator.</span></span> <span data-ttu-id="cdb21-159">LCS のサブスクリプション見積に関する警告が特定された場合、このトピックの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="cdb21-159">If you identify any warnings regarding the Subscription Estimator in LCS, follow the instructions in this topic.</span></span> <span data-ttu-id="cdb21-160">問題が継続する場合、Microsoft サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="cdb21-160">If you continue to have issues, contact Microsoft Support.</span></span>

<span data-ttu-id="cdb21-161">その他のエラー メッセージが表示されたり、他の問題が発生した場合は、サポート チームがその問題に対処できるように、サポート リクエストを作成し、有効な見積を添付します。</span><span class="sxs-lookup"><span data-stu-id="cdb21-161">If you receive any other error message or encounter other issues, create a support request, and attach your active estimate so that the Support team can address the issue.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdb21-162">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cdb21-162">Additional resources</span></span>

[<span data-ttu-id="cdb21-163">サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="cdb21-163">Subscriptions, LCS projects, and Azure Active Directory tenants FAQ</span></span>](../../fin-ops/get-started/subscription-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
