---
title: 発注書の承認モバイル ワークスペース
description: このトピックでは、発注書を表示したり、アクションを通じて対応したりできる発注書の承認モバイル ワークスペースに関する情報を提供します。 たとえば、発注書を承認または拒否できます。
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26f0dc3b128daf8c7d8a05d6f3cacc5b7de0c756
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909111"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="bd168-104">発注書の承認モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="bd168-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd168-105">このトピックでは、**発注書の承認** モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd168-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="bd168-106">このワークスペースでは、発注書を表示したり、アクションを通じて対応したりできます。</span><span class="sxs-lookup"><span data-stu-id="bd168-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="bd168-107">たとえば、発注書を承認または拒否できます。</span><span class="sxs-lookup"><span data-stu-id="bd168-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="bd168-108">概要</span><span class="sxs-lookup"><span data-stu-id="bd168-108">Overview</span></span> 
<span data-ttu-id="bd168-109">承認が必要な発注書は、承認ワークフローを経由します。</span><span class="sxs-lookup"><span data-stu-id="bd168-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="bd168-110">ワークフローには、1 人以上の人員のアクションが必要なさまざま手順を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="bd168-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="bd168-111">たとえば、ある人物がタスクの完了または発注書の承認を行う必要があるとします。</span><span class="sxs-lookup"><span data-stu-id="bd168-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="bd168-112">**発注書の承認** モバイル ワークスペースで、モバイル デバイスから簡単に発注書の確認および対応ができます。</span><span class="sxs-lookup"><span data-stu-id="bd168-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="bd168-113">また、このワークスペースを使用して、Web クライアントからできるものと同じワークフロー アクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="bd168-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bd168-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="bd168-114">Prerequisites</span></span>
<span data-ttu-id="bd168-115">組織に配置されている Supply Chain Management のバージョンによって、前提条件は異なります。</span><span class="sxs-lookup"><span data-stu-id="bd168-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="bd168-116">Supply Chain Management を使用する場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="bd168-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="bd168-117">Supply Chain Management を組織に配置している場合、システム管理者は **発注書承認** モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd168-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="bd168-118">手順については、「[モバイル ワークスペースの公開](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd168-118">For instructions, see [Publish a mobile workspace](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="bd168-119">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム 更新プログラム 3 以降を使用する場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="bd168-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="bd168-120">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd168-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bd168-121">前提条件</span><span class="sxs-lookup"><span data-stu-id="bd168-121">Prerequisite</span></span></th>
<th><span data-ttu-id="bd168-122">役割</span><span class="sxs-lookup"><span data-stu-id="bd168-122">Role</span></span></th>
<th><span data-ttu-id="bd168-123">説明</span><span class="sxs-lookup"><span data-stu-id="bd168-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd168-124">KB 4017918 を実装します。</span><span class="sxs-lookup"><span data-stu-id="bd168-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="bd168-125">システム管理者</span><span class="sxs-lookup"><span data-stu-id="bd168-125">System administrator</span></span></td>
<td><span data-ttu-id="bd168-126">KB 4017918 は、<strong>発注書の承認</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。</span><span class="sxs-lookup"><span data-stu-id="bd168-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="bd168-127">KB 4017918 を実装するには、システム管理者は次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd168-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="bd168-128"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services (LCS)</a> からメタデータ修正プログラムをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="bd168-128"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="bd168-129"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします。</a></span><span class="sxs-lookup"><span data-stu-id="bd168-129"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="bd168-130"><strong>SCMMobile</strong> モデルを含む<a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="bd168-130"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="bd168-131"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">配置可能パッケージを適用します</a>。</span><span class="sxs-lookup"><span data-stu-id="bd168-131"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd168-132"><strong>発注書の承認</strong>モバイル ワークスペースを公開します。</span><span class="sxs-lookup"><span data-stu-id="bd168-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="bd168-133">システム管理者</span><span class="sxs-lookup"><span data-stu-id="bd168-133">System administrator</span></span></td>
<td><span data-ttu-id="bd168-134">「<a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd168-134">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="bd168-135">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="bd168-135">Download and install the mobile app</span></span>
<span data-ttu-id="bd168-136">Finance and Operations モバイル アプリのダウンロードとインストール。</span><span class="sxs-lookup"><span data-stu-id="bd168-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="bd168-137">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="bd168-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="bd168-138">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="bd168-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="bd168-139">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="bd168-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="bd168-140">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="bd168-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="bd168-141">Microsoft Dynamics 365 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="bd168-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="bd168-142">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="bd168-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="bd168-143">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="bd168-143">Enter your credentials.</span></span>
4. <span data-ttu-id="bd168-144">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd168-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="bd168-145">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd168-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![使用可能なワークスペースの一覧の発注書の承認ワークスペース](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="bd168-147">自分に割り当てられている注文の表示</span><span class="sxs-lookup"><span data-stu-id="bd168-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="bd168-148">モバイル デバイスで、**発注書の承認** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="bd168-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="bd168-149">**自分に割り当てられた注文** を選択して、発注書の承認ワークフローでアクションを求められたすべての発注書を表示します。</span><span class="sxs-lookup"><span data-stu-id="bd168-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="bd168-150">注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd168-150">Select an order.</span></span> <span data-ttu-id="bd168-151">**注文の詳細** ページで、注文のヘッダー情報と明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd168-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="bd168-152">ワークフロー タスクからガイドラインについて検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="bd168-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="bd168-153">**勘定配布** を選択して、**ヘッダーの勘定配布** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="bd168-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="bd168-154">**注文の詳細** ページに戻り、明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd168-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="bd168-155">注文明細行の詳細から、明細行固有の勘定配布を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="bd168-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="bd168-156">発注書の操作を完了します。</span><span class="sxs-lookup"><span data-stu-id="bd168-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="bd168-157">自分に割り当てられている発注書を表示し、ワークフローの指示を読んでから、アクションを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bd168-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="bd168-158">モバイル デバイスで、**発注書の承認** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="bd168-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="bd168-159">**自分に割り当てられた注文** を選択して、発注書の承認ワークフローでアクションを求められたすべての発注書を表示します。</span><span class="sxs-lookup"><span data-stu-id="bd168-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="bd168-160">注文を選択し、詳細ページを表示します。</span><span class="sxs-lookup"><span data-stu-id="bd168-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="bd168-161">**アクション** を選択して、使用可能なアクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="bd168-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="bd168-162">使用可能なアクションは、自分に割り当てられたタスクに依存します。</span><span class="sxs-lookup"><span data-stu-id="bd168-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="bd168-163">タスクのアクション</span><span class="sxs-lookup"><span data-stu-id="bd168-163">Task action</span></span>    | <span data-ttu-id="bd168-164">承認アクション</span><span class="sxs-lookup"><span data-stu-id="bd168-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="bd168-165">完了</span><span class="sxs-lookup"><span data-stu-id="bd168-165">Complete</span></span>       | <span data-ttu-id="bd168-166">承認</span><span class="sxs-lookup"><span data-stu-id="bd168-166">Approve</span></span>          |
    | <span data-ttu-id="bd168-167">却下</span><span class="sxs-lookup"><span data-stu-id="bd168-167">Return</span></span>         | <span data-ttu-id="bd168-168">否認</span><span class="sxs-lookup"><span data-stu-id="bd168-168">Reject</span></span>           |
    | <span data-ttu-id="bd168-169">変更依頼</span><span class="sxs-lookup"><span data-stu-id="bd168-169">Request change</span></span> | <span data-ttu-id="bd168-170">変更依頼</span><span class="sxs-lookup"><span data-stu-id="bd168-170">Request change</span></span>   |
    | <span data-ttu-id="bd168-171">委任</span><span class="sxs-lookup"><span data-stu-id="bd168-171">Delegate</span></span>       | <span data-ttu-id="bd168-172">委任</span><span class="sxs-lookup"><span data-stu-id="bd168-172">Delegate</span></span>         |

5. <span data-ttu-id="bd168-173">該当するアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bd168-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="bd168-174">**タスクの完了** ページで、コメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="bd168-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="bd168-175">**委任** アクションを選択した場合、タスクを委任するユーザーを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd168-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="bd168-176">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd168-176">Select **Done**.</span></span> <span data-ttu-id="bd168-177">ワークスペースを更新すると、発注書がリストに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="bd168-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]