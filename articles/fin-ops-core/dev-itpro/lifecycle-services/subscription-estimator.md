---
title: Lifecycle Services (LCS) のサブスクリプション試算
description: このトピックでは、Lifecycle Services (LCS) で利用可能なサブスクリプション試算ツールを使用する方法について説明します。
author: angelmarshall
ms.date: 03/25/2021
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
ms.openlocfilehash: d66c75039ec6d1f1fc1b55b52396874887c601a5
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921203"
---
# <a name="subscription-estimator-in-lifecycle-services-lcs"></a><span data-ttu-id="47d74-103">Lifecycle Services (LCS) のサブスクリプション試算</span><span class="sxs-lookup"><span data-stu-id="47d74-103">Subscription estimator in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47d74-104">サブスクリプション見積もりツールは、Microsoft Dynamics Lifecycle Services (LCS) で使用できるツールです。</span><span class="sxs-lookup"><span data-stu-id="47d74-104">Subscription estimator is a tool that is available in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="47d74-105">Microsoft は、このツールを使用して、顧客に対して準備する必要がある実稼働環境の初期サイズを見積ります。</span><span class="sxs-lookup"><span data-stu-id="47d74-105">Microsoft uses this tool to estimate the initial size of the production environment that must be provisioned for a customer.</span></span> <span data-ttu-id="47d74-106">顧客が実稼働環境の配置を要求する前に、トランザクション カウントの観点からピーク作業負荷を見積もり、その情報を LCS にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47d74-106">Before customers can request deployment of a production environment, they must estimate their peak workloads in terms of transaction counts and then upload that information to LCS.</span></span> <span data-ttu-id="47d74-107">ユーザー ライセンスの詳細およびトランザクション カウントを使用してサブスクリプション要件を推測することにより、サブスクリプション見積もりツールは、プロビジョニングされた環境が顧客の業務要件を満たしていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="47d74-107">By using the details of user licenses and transaction counts to infer subscription requirements, the Subscription estimator tool helps ensure that the provisioned environment meets the customer's business requirements.</span></span>

<span data-ttu-id="47d74-108">サブスクリプション試算ツールを使用するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="47d74-108">Follow these steps to use the Subscription estimator tool.</span></span>

1. <span data-ttu-id="47d74-109">LCS で、実装プロジェクトに関連付けられているプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="47d74-109">In LCS, open the project that is associated with the implementation project.</span></span>
2. <span data-ttu-id="47d74-110">ページの上部にあるハンバーガー アイコン選択し、**サブスクリプション見積もりツール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47d74-110">At the top of the page, select the hamburger icon, and then select **Subscription estimator**.</span></span>

    <span data-ttu-id="47d74-111">[![サブスクリプション見積もりツール](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)</span><span class="sxs-lookup"><span data-stu-id="47d74-111">[![subscription estimator](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)</span></span>

3. <span data-ttu-id="47d74-112">サンプルの使用状況プロファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="47d74-112">Download the sample usage profile.</span></span>
4. <span data-ttu-id="47d74-113">各タブで必要な質問に回答します。Commerce の顧客の場合は、**Retail と Commerce** タブ上の質問に回答してください。</span><span class="sxs-lookup"><span data-stu-id="47d74-113">Answer the required questions on each tab. If you're a Commerce customer, be sure to answer the questions on the **Retail and Commerce** tab.</span></span>
5. <span data-ttu-id="47d74-114">使用状況プロファイルをローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="47d74-114">Save the usage profile locally.</span></span>
6. <span data-ttu-id="47d74-115">使用プロファイルをアップロードするには、**新しい見積もり** を選択し、見積もりに名前を付け、使用プロファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="47d74-115">To upload the usage profile, select **New estimate**, name the estimate, and then upload the usage profile.</span></span>
7. <span data-ttu-id="47d74-116">アップロードが完了した後、**アクティブとしてマークする** を選択し見積もりを有効にします。</span><span class="sxs-lookup"><span data-stu-id="47d74-116">After the upload is completed, select **Mark as Active** to activate an estimate.</span></span> <span data-ttu-id="47d74-117">生産の配置をコンフィギュレーションするために有効な見積が必要です。</span><span class="sxs-lookup"><span data-stu-id="47d74-117">An active estimate is required in order to configure a production deployment.</span></span>

<span data-ttu-id="47d74-118">有効でアクティブな見積があるときは、**構成** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="47d74-118">When there is a valid active estimate, the **Configure** button becomes available.</span></span> <span data-ttu-id="47d74-119">このボタンを使用すると、製造環境の展開を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="47d74-119">You can use this button to request a production environment deployment.</span></span>

> [!NOTE]
> <span data-ttu-id="47d74-120">複数の見積を使用できますが、1 つの見積に **アクティブ** とマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47d74-120">Although you can have multiple estimates, one estimate must be marked as **Active**.</span></span> <span data-ttu-id="47d74-121">実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。</span><span class="sxs-lookup"><span data-stu-id="47d74-121">After the production environment has been deployed, or deployment of the environment has received sign-off, the active estimate is locked.</span></span> <span data-ttu-id="47d74-122">別の見積もりを有効見積もりとしてマークするには、LCS のサポート ポータルを使用してサポート要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="47d74-122">To mark a different estimate as the active estimate, create a support request by using the Support portal in LCS.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="47d74-123">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="47d74-123">Frequently asked questions</span></span>

### <a name="why-isnt-the-configure-button-for-deploying-a-production-environment-available-even-though-there-is-an-active-estimate-and-why-does-a-warning-message-appear-in-the-action-center-on-the-project-dashboard"></a><span data-ttu-id="47d74-124">アクティブな見積があるにもかかわらず、実稼動環境の **コンフィギュレーション** ボタンが有効なのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="47d74-124">Why isn't the **Configure** button for deploying a production environment available, even though there is an active estimate?</span></span> <span data-ttu-id="47d74-125">また、プロジェクト ダッシュ ボード上のアクション センターに警告メッセージが表示されるのはなぜでしょうか?</span><span class="sxs-lookup"><span data-stu-id="47d74-125">And why does a warning message appear in the Action Center on the project dashboard?</span></span>

<span data-ttu-id="47d74-126">複数の実装プロジェクトがある場合、**コンフィギュレーション** ボタンを有効にされていない可能性があり、アクション センターに不足しているライセンス数に関する警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="47d74-126">If you have multiple implementation projects, the **Configure** button might not be enabled and a warning message will appear in the Action Center regarding an insufficient number of licenses.</span></span> <span data-ttu-id="47d74-127">サポート リクエストを記録すると、サポート チームがこの問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="47d74-127">Log a support request, and the Support team can help resolve this issue.</span></span>

### <a name="why-does-an-error-occur-when-i-mark-an-estimate-as-active"></a><span data-ttu-id="47d74-128">見積に **有効** とマークするとエラーが発生するのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="47d74-128">Why does an error occur when I mark an estimate as **Active**?</span></span>

<span data-ttu-id="47d74-129">見積を **有効** とマークすると、次のエラー メッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="47d74-129">When you mark an estimate as **Active**, you might receive the following error message:</span></span>

<span data-ttu-id="47d74-130">*見積が作成されましたが、要件を満たしていません*</span><span class="sxs-lookup"><span data-stu-id="47d74-130">*Estimate created but does not meet requirements*</span></span>

<span data-ttu-id="47d74-131">このエラーは、入力されたトランザクション明細行がサブスクリプション見積ツールの制限内にない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="47d74-131">This error occurs if transaction lines that are entered aren't within the limits of the Subscription estimation tool.</span></span> <span data-ttu-id="47d74-132">このエラーを解決するには、サポート要求を作成し、使用プロファイルを添付します。</span><span class="sxs-lookup"><span data-stu-id="47d74-132">To resolve this error, create a support request, and attach the usage profile.</span></span> <span data-ttu-id="47d74-133">次に、インスタンスのサイズを手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="47d74-133">Your instance can then be manually sized.</span></span>

### <a name="how-can-i-update-my-subscription-if-my-production-environment-is-deployed"></a><span data-ttu-id="47d74-134">実稼動環境が配置されている場合、どのようにサブスクリプションを更新ことができますか?</span><span class="sxs-lookup"><span data-stu-id="47d74-134">How can I update my subscription if my production environment is deployed?</span></span>

<span data-ttu-id="47d74-135">[サブスクリプション見積](subscription-estimator.md) は、実働の要求をする前に必要なステップです。</span><span class="sxs-lookup"><span data-stu-id="47d74-135">The [Subscription estimator](subscription-estimator.md) is a required step before requesting production.</span></span> <span data-ttu-id="47d74-136">複数の見積を使用できますが、1 つは **アクティブ** とマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47d74-136">Although you can have multiple estimates, one must be marked as  **Active**.</span></span> <span data-ttu-id="47d74-137">有効なサブスクリプション見積を使用して、実稼働環境のサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="47d74-137">The active subscription estimate is used to size the production environment.</span></span> <span data-ttu-id="47d74-138">実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。</span><span class="sxs-lookup"><span data-stu-id="47d74-138">After the production environment has been deployed, or deployment of the environment has received sign-off, the active estimate is locked.</span></span> <span data-ttu-id="47d74-139">別の見積もりを有効見積もりとしてマークするには、LCS のサポート ポータルを使用してサポート要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="47d74-139">To mark a different estimate as the active estimate, create a support request by using the Support portal in LCS.</span></span> <span data-ttu-id="47d74-140">プロジェクトのライセンス量が増加した場合、新しいサブスクリプション見積を作成し、サポート リクエストを記録して、有効としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47d74-140">If you have an  increase in the licensing volume  of your project, you will need to create a new subscription estimator and log a support request to have it marked as Active.</span></span> <span data-ttu-id="47d74-141">サイズ変更をする場合、新しいサブスクリプション見積に基づいて適用されることがあります。</span><span class="sxs-lookup"><span data-stu-id="47d74-141">Resizing may be applicable based on the new subscription estimate.</span></span>

### <a name="what-should-i-do-to-activate-my-subscription-estimate-if-i-have-multiple-projects-in-the-same-tenant"></a><span data-ttu-id="47d74-142">同じテナントに複数のプロジェクトがある場合、サブスクリプション見積を有効にするには何をする必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="47d74-142">What should I do to activate my subscription estimate if I have multiple projects in the same tenant?</span></span>

<span data-ttu-id="47d74-143">同じテナント内に複数のプロジェクトを実装する場合、LCS のアクション センターに「*サブスクリプションの見積が完了していない*」ことを示す警告が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="47d74-143">When you are implementing several projects in the same tenant, a warning indicating "*subscription estimate is not complete*" may appear in the Action Center of LCS.</span></span> <span data-ttu-id="47d74-144">このエラーは、すべての実装プロジェクトの見積ユーザーの数が、購入したライセンスの数を超えないようにする必要があることを示しています。</span><span class="sxs-lookup"><span data-stu-id="47d74-144">This error will indicate that the total number of estimated users for all implementation projects should not exceed the number of purchased licenses.</span></span> <span data-ttu-id="47d74-145">これは、有効なサブスクリプション見積のユーザーの合計が、同じタイプのテナント ライセンス数を上回っている場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="47d74-145">This may happen if the sum of users on the active subscription estimates is superior to the tenant license count of the same type.</span></span> <span data-ttu-id="47d74-146">これを修正するには、できるだけ早く Microsoft にサポート リクエストを送信し、ライセンス配賦に関する情報を含め、サブスクリプション見積を修正するよう求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="47d74-146">To have this corrected, you should submit a support request to Microsoft as soon as possible, asking for the subscription estimations to be corrected, including the information about license allocation.</span></span> <span data-ttu-id="47d74-147">サポート チームにより、見積エディションのプロセスは有効になります。</span><span class="sxs-lookup"><span data-stu-id="47d74-147">With the help of the Support team, the process for the estimation edition will be enabled.</span></span>

<span data-ttu-id="47d74-148">リクエストを送信する前に、必要なすべてのライセンスが有効にされていることを確認し、実稼働環境のサイズ変更が必要な場合には、ダウンタイムが必要になることがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="47d74-148">Make sure that you have all the required licenses active before submitting the request and be aware that in cases were resizing of the production environment is needed, it may require downtime.</span></span>

> [!NOTE] 
> <span data-ttu-id="47d74-149">FastTrack ソリューション アーキテクトは、サブスクリプション見積のアップロードまたは更新に関与していません。</span><span class="sxs-lookup"><span data-stu-id="47d74-149">FastTrack Solutions architects have no involvement in uploading or updating the Subscription Estimator.</span></span> <span data-ttu-id="47d74-150">LCS のサブスクリプション見積に関する警告が特定された場合、上記の指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="47d74-150">If you identify any warnings regarding the Subscription Estimator in LCS, follow the instructions above.</span></span> <span data-ttu-id="47d74-151">問題が継続する場合、Microsoft サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="47d74-151">If you continue to have issues, contact Microsoft Support.</span></span> 

<span data-ttu-id="47d74-152">その他のエラー メッセージが表示されたり、その他の問題が発生した場合は、サポート チームがその問題に対処できるようにサポート リクエストを作成し、アクティブな見積を添付します。</span><span class="sxs-lookup"><span data-stu-id="47d74-152">If you receive any other error message or encounter any other issue, create a support request, and attach your active estimate so that the Support team can address the issue.</span></span>
 
 ## <a name="additional-resources"></a><span data-ttu-id="47d74-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="47d74-153">Additional resources</span></span>
 [<span data-ttu-id="47d74-154">サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="47d74-154">Subscriptions, LCS projects, and Azure Active Directory tenants FAQ</span></span>](../../fin-ops/get-started/subscription-overview.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
