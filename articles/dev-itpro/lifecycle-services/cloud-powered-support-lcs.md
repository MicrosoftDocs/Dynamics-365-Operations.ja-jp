---
title: "Finance and Operations サポート エクスペリエンスの管理"
description: "このトピックでは、Microsoft Dynamics Lifecycle Services サービス のサポート ツールを使用して、サポート インシデントを管理する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: 0fa10573-8146-446e-8124-8a7af9546add
ms.search.region: Global
ms.author: anupams
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3487d1745c2fac09e8c2f42d4ae7720b8741cfdd
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="manage-finance-and-operations-support-experiences"></a><span data-ttu-id="11e74-103">Finance and Operations サポート エクスペリエンスの管理</span><span class="sxs-lookup"><span data-stu-id="11e74-103">Manage Finance and Operations Support experiences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11e74-104">サポート ツールを使用するには、あらかじめ Lifecycle Services (LCS) でプロジェクトを作成して、環境にシステム診断プログラムをインストールして実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11e74-104">To use the Support tool, you must have previously created a project in Lifecycle Services (LCS) and installed and ran the System diagnostics in your environment.</span></span> <span data-ttu-id="11e74-105">詳細については、[システム診断 (Lifecycle Services, LCS)](ax-2012/system-diagnostics-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11e74-105">For more information, see [System diagnostics (Lifecycle Services, LCS)](ax-2012/system-diagnostics-lcs.md).</span></span>


## <a name="open-a-new-incident"></a><span data-ttu-id="11e74-106">新しいインシデントを開く</span><span class="sxs-lookup"><span data-stu-id="11e74-106">Open a new incident</span></span>
1. <span data-ttu-id="11e74-107">LCS で、サポート インシデントを提出するプロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="11e74-107">In LCS, navigate to the project for which you want to file a support incident.</span></span> 

2. <span data-ttu-id="11e74-108">**サポート** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-108">Click the **Support** tile.</span></span>
   <span data-ttu-id="11e74-109">![サポート メニュー](media/CPS1.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-109">![Support menu](media/CPS1.png)</span></span>

3. <span data-ttu-id="11e74-110">**Microsoft に送信**タブで、**インシデントの送信**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-110">On the **Submitted to Microsoft** tab, click the **Submit an incident** button.</span></span>
   <span data-ttu-id="11e74-111">![サポート ボタン](media/CPS2.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-111">![Support button](media/CPS2.png)</span></span>

4. <span data-ttu-id="11e74-112">問題のカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="11e74-112">Select an issue category.</span></span>
   <span data-ttu-id="11e74-113">![カテゴリ](media/CPS5.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-113">![Category](media/CPS5.png)</span></span>

5. <span data-ttu-id="11e74-114">問題の領域を選択します。</span><span class="sxs-lookup"><span data-stu-id="11e74-114">Select an issue area.</span></span>
   <span data-ttu-id="11e74-115">![面](media/CPS6.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-115">![Area](media/CPS6.png)</span></span>

6. <span data-ttu-id="11e74-116">**問題の説明**ウィンドウで、次を入力します。</span><span class="sxs-lookup"><span data-stu-id="11e74-116">In the **Describe your issue** window, enter the following:</span></span>

   - <span data-ttu-id="11e74-117">環境で問題が発生した場合は、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11e74-117">Select **Yes** if the issue occured in an environment.</span></span> <span data-ttu-id="11e74-118">環境名を選択します。</span><span class="sxs-lookup"><span data-stu-id="11e74-118">Select the environment name.</span></span>  
   - <span data-ttu-id="11e74-119">**タイトル**フィールドの問題について短い説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="11e74-119">Enter a short description of your issue in the **Title** field.</span></span>
   - <span data-ttu-id="11e74-120">問題の詳細と、エラーを再生成するために必要なステップに関する詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="11e74-120">Provide details about the issue detail and the steps needed to reproduce the error.</span></span>
   - <span data-ttu-id="11e74-121">該当する場合は、エラー メッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="11e74-121">If applicable, enter an error message.</span></span> 
   - <span data-ttu-id="11e74-122">可能であれば、問題を示すスクリーン ショットを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="11e74-122">If possible, attach screenshots that illustrate the problem.</span></span> <span data-ttu-id="11e74-123">これを行うには、**コンピュータからの添付ファイル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-123">To do this, click **Attach file from computer**.</span></span>
 
   > [!NOTE]
   > <span data-ttu-id="11e74-124">インシデントを作成するときは、問題検索によって、ユーザーの選択と入力にもとづいて、上位 10 の「実行可能な問題のソリューション」という検索結果が設定され、サポート ケースの作成時に詳細情報が提供されると、これらの結果が動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="11e74-124">When you create an incident, Issue search will populate the top 10 "Possible issue solutions" search results based on the your selection and input, and dynamically refresh these results as more details are provided during support case creation.</span></span> 
   > 
   > <span data-ttu-id="11e74-125">その他のソリューションを検索する必要がある場合も、スタンドアロン問題検索にドロップダウン メニューからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="11e74-125">Standalone Issue search is still accessible via the dropdown menu if you need to search for more solutions.</span></span> 
 
   ![詳細](media/CPS7.png)
 
7. <span data-ttu-id="11e74-127">基本連絡先情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="11e74-127">Enter the primary contact information.</span></span> <span data-ttu-id="11e74-128">これらの連絡先の詳細は、カスタマー サポート チームがケースについて連絡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="11e74-128">These contact details will be used by the customer support team to contact you about the case.</span></span>
   <span data-ttu-id="11e74-129">![連絡先情報](media/CPS8.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-129">![Contact info](media/CPS8.png)</span></span>


8. <span data-ttu-id="11e74-130">サポート契約と重要度レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="11e74-130">Select the support contract and the severity level.</span></span> 
    
   - <span data-ttu-id="11e74-131">オンプレミス環境のサポート契約では、インシデント数に制限があります。</span><span class="sxs-lookup"><span data-stu-id="11e74-131">Support contracts for on-premises environments have a limited incident count.</span></span> 
   - <span data-ttu-id="11e74-132">クラウド環境のサポート契約では、インシデント数が無制限です。</span><span class="sxs-lookup"><span data-stu-id="11e74-132">Support contracts for cloud environments have an unlimited incident count.</span></span> 
   - <span data-ttu-id="11e74-133">オンプレミス製品またはクラウド環境では、使用可能なサポート契約の一覧から、複数層のサポート契約がある場合に使用するサポート オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="11e74-133">For on-premises products or cloud environments, from the list of available support contracts, select the support option to use if you have multiple tier support contracts.</span></span> 
   <span data-ttu-id="11e74-134">![契約と重要度](media/CPS9.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-134">![Contract and severity](media/CPS9.png)</span></span>

9. <span data-ttu-id="11e74-135">**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-135">Click **Submit**.</span></span> 

   ![完成](media/CPS10.png)


<span data-ttu-id="11e74-137">**送信**をクリックした後、インシデントが作成され**インシデント** リストに追加されます。</span><span class="sxs-lookup"><span data-stu-id="11e74-137">After you click **Submit**, an incident is created and added to the **Incidents** list.</span></span> <span data-ttu-id="11e74-138">このケースに割り当てられている Microsoft サポート エンジニアから、電子メール メッセージを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="11e74-138">You will receive an email message from the Microsoft Support Engineer assigned to your case.</span></span> 


## <a name="manage-support-plans"></a><span data-ttu-id="11e74-139">サポート計画の管理</span><span class="sxs-lookup"><span data-stu-id="11e74-139">Manage support plans</span></span>
<span data-ttu-id="11e74-140">次のように、**プレミア サポート**または**パートナーの前貸しをサポート**などのサポート計画を購入した場合は、新しいチケットを作成する前に LCS サポートにそれを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11e74-140">If you purchased a support plan, such as **Premier Support** or **Advance Support for Partners**, you will need to add it to LCS Support before you create a new ticket.</span></span>    

1. <span data-ttu-id="11e74-141">**Microsoft に送信**タブで、**サポート計画の管理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-141">On the **Submitted to Microsoft** tab, click **Manage support plans**.</span></span> 
   <span data-ttu-id="11e74-142">![サポート計画の管理](media/SupportManagePlans.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-142">![Manage support plans](media/SupportManagePlans.png)</span></span>
   
2. <span data-ttu-id="11e74-143">**サポート計画の管理**ページで、**契約の追加**をクリックし、**アクセス ID** および**パスワード/契約 ID** を入力します。</span><span class="sxs-lookup"><span data-stu-id="11e74-143">On the **Manage support plans** page, click **Add contract** to enter the **Access ID** and **Password/Contract ID**.</span></span>
   <span data-ttu-id="11e74-144">![契約の追加](media/SupportAddPlans.png)</span><span class="sxs-lookup"><span data-stu-id="11e74-144">![Add contracts](media/SupportAddPlans.png)</span></span> 
   
   
## <a name="report-production-outage"></a><span data-ttu-id="11e74-145">稼働停止のレポート</span><span class="sxs-lookup"><span data-stu-id="11e74-145">Report production outage</span></span>
<span data-ttu-id="11e74-146">レポート生成停止は、実稼動環境のサービスが低下または使用不可能になった場合、Microsoft サポートに問題をエスカレートを迅速かつ有効なチャンネルを提供します。</span><span class="sxs-lookup"><span data-stu-id="11e74-146">Report production outage provides a quick and effective channel to escalate  issues to Microsoft Support in the event that the services in a production environment are degraded or become unavailable.</span></span>  

<span data-ttu-id="11e74-147">この機能は、Dynamics 365 Finance and Operations を購入し、LCS に配置された**実稼働**環境の**実装**プロジェクトを持つすべての顧客が利用できます。</span><span class="sxs-lookup"><span data-stu-id="11e74-147">This feature is available to all customers that have purchased Dynamics 365 Finance and Operations and have **implementation** projects with a **production** environment deployed in LCS.</span></span>  

<span data-ttu-id="11e74-148">稼働停止は、**複数のユーザーに影響を与え、ビジネスの日常業務遂行を妨げる実稼働環境における 1 つ以上のシステム全体の問題**として定義されます。</span><span class="sxs-lookup"><span data-stu-id="11e74-148">A production outage is defined as **one or more system-wide issues on a live production environment that impact multiple users and prevent your business from performing daily operations**.</span></span> 

<span data-ttu-id="11e74-149">**レポート フロー**</span><span class="sxs-lookup"><span data-stu-id="11e74-149">**Reporting flow**</span></span>
1. <span data-ttu-id="11e74-150">実稼働環境で、顧客は稼働停止やその他の業務を続行できない状況が発生します。</span><span class="sxs-lookup"><span data-stu-id="11e74-150">In a live production environment, a customer experiences an outage or other situation that prevents business from continuing.</span></span>
2. <span data-ttu-id="11e74-151">顧客は、LCS サポート ポータルを使用して稼働停止の問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="11e74-151">The customer reports a production outage issue by using the LCS Support portal.</span></span>
3. <span data-ttu-id="11e74-152">顧客は稼働停止の問題を選択し、追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="11e74-152">The customer selects a production outage issue and provides additional information.</span></span>
4. <span data-ttu-id="11e74-153">Microsoft のサポート エンジニアは、送信の 30 分以内に生産停止チケットを確認し、問題を調査し解決するために利害関係者とすぐに連携を取ります。</span><span class="sxs-lookup"><span data-stu-id="11e74-153">A Microsoft support engineer acknowledges the production outage ticket within 30 minutes of submission and begins to immediately collaborate with stakeholders to investigate and resolve the issue.</span></span>
5. <span data-ttu-id="11e74-154">サポート エンジニアが顧客に連絡してステータス更新を提供する</span><span class="sxs-lookup"><span data-stu-id="11e74-154">A support engineer contacts the customer to provide a status update</span></span>

<span data-ttu-id="11e74-155">**アクセスおよび可用性**</span><span class="sxs-lookup"><span data-stu-id="11e74-155">**Access and availibility**</span></span>

<span data-ttu-id="11e74-156">顧客の実装プロジェクトに追加されたすべてのユーザーはこの機能にアクセスを許可できます。</span><span class="sxs-lookup"><span data-stu-id="11e74-156">All users that have been added to a customer's implementation project have access to this feature.</span></span> <span data-ttu-id="11e74-157">これには、プロジェクト オーナー、組織管理者、チームメンバー、および環境マネージャーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="11e74-157">This includes project owners, organization admins, team members, and environment managers.</span></span> 

<span data-ttu-id="11e74-158">この機能は次で利用できます。</span><span class="sxs-lookup"><span data-stu-id="11e74-158">This feature is available to:</span></span>
- <span data-ttu-id="11e74-159">Dynamics 365 for Finance and Operation</span><span class="sxs-lookup"><span data-stu-id="11e74-159">Dynamics 365 for Finance and Operation</span></span> 
- <span data-ttu-id="11e74-160">Microsoft が管理する環境</span><span class="sxs-lookup"><span data-stu-id="11e74-160">Environments managed by Microsoft</span></span> 
- <span data-ttu-id="11e74-161">LCS プロジェクトの実稼動環境</span><span class="sxs-lookup"><span data-stu-id="11e74-161">A production environment in the LCS Project</span></span> 
- <span data-ttu-id="11e74-162">すべてのサポート計画</span><span class="sxs-lookup"><span data-stu-id="11e74-162">All support plans</span></span>

### <a name="report-a-production-outage"></a><span data-ttu-id="11e74-163">稼働停止のレポート</span><span class="sxs-lookup"><span data-stu-id="11e74-163">Report a production outage</span></span>
1. <span data-ttu-id="11e74-164">LCS プロジェクトにログインします。</span><span class="sxs-lookup"><span data-stu-id="11e74-164">Log into your LCS project.</span></span>
2. <span data-ttu-id="11e74-165">ハンバーガー メニューから**サポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-165">From the hamburger menu, click **Support**.</span></span>
<span data-ttu-id="11e74-166">![サポート](media/outage1.jpg)</span><span class="sxs-lookup"><span data-stu-id="11e74-166">![Support](media/outage1.jpg)</span></span>

3. <span data-ttu-id="11e74-167">**Microsoft に送信**タブで、**稼働停止のレポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-167">On the **Submitted To Microsoft** tab, click **Report production outage**.</span></span>
<span data-ttu-id="11e74-168">![サポート](media/outage2.jpg)</span><span class="sxs-lookup"><span data-stu-id="11e74-168">![Support](media/outage2.jpg)</span></span>

4. <span data-ttu-id="11e74-169">プロダクションの停止を確認し、ドロップダウン リストから停止シナリオを選択してから、**続行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-169">Confirm the production outage, select the outage scenario from the drop-down list, and then click **Continue**.</span></span>
<span data-ttu-id="11e74-170">![シナリオ](media/outage3.jpg)</span><span class="sxs-lookup"><span data-stu-id="11e74-170">![scenario](media/outage3.jpg)</span></span>

5. <span data-ttu-id="11e74-171">停止に関するタイトルと詳細を追加して、**次**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-171">Add a title and details about the outage, and then click **Next**.</span></span>
<span data-ttu-id="11e74-172">![詳細](media/outage4.jpg)</span><span class="sxs-lookup"><span data-stu-id="11e74-172">![detail](media/outage4.jpg)</span></span>

6. <span data-ttu-id="11e74-173">連絡先の情報を入力し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-173">Provide contact information, and then click **Next**.</span></span> 
<span data-ttu-id="11e74-174">![連絡](media/outage5.jpg)</span><span class="sxs-lookup"><span data-stu-id="11e74-174">![contact](media/outage5.jpg)</span></span>

7. <span data-ttu-id="11e74-175">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11e74-175">Click **Done**.</span></span>
<span data-ttu-id="11e74-176">![完了](media/outage6.jpg)</span><span class="sxs-lookup"><span data-stu-id="11e74-176">![done](media/outage6.jpg)</span></span>

> [!NOTE] 
> <span data-ttu-id="11e74-177">停止シナリオに状況が一覧表示されていない場合は、LCS を通じてサポート インシデントを入力します。</span><span class="sxs-lookup"><span data-stu-id="11e74-177">If you don't see your situation listed in the outage scenarios, enter a support incident through LCS.</span></span> <span data-ttu-id="11e74-178">Microsoft のサポート エンジニアによる最初の調査中に、状況が現在の稼働停止シナリオのリストに合っていないことがわかった場合、サポート インシデントが現在のサポート計画に基づいて正しいサポート チームおよび SLA に転送されます。</span><span class="sxs-lookup"><span data-stu-id="11e74-178">If, during the initial investigation by a Microsoft support engineer, it is found the situation does not meet the current list of production outage scenarios, the support incident will be transferred to the correct support team and SLA based on your current support plan.</span></span>



