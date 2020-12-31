---
title: Finance and Operations アプリのテクニカル サポートを設定する
description: このトピックでは、クラウドおよびオンプレミスの展開のサポートについて説明します。 必要な設定およびサポートの問題を作成して対応する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 29531
ms.assetid: 3734bd06-6d4c-42f5-8f2b-30a451189002
ms.search.region: Global
ms.author: anupams
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45fce57f7324ec0be652e63822657c113eae30d9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681054"
---
# <a name="set-up-technical-support-for-finance-and-operations-apps"></a><span data-ttu-id="5a694-104">Finance and Operations アプリのテクニカル サポートを設定する</span><span class="sxs-lookup"><span data-stu-id="5a694-104">Set up technical support for Finance and Operations apps</span></span> 
[!include [banner](../includes/banner.md)]

<a name="prerequisites"></a><span data-ttu-id="5a694-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="5a694-105">Prerequisites</span></span>
--------------

<span data-ttu-id="5a694-106">テクニカル サポートの設定をする前に、Microsoft Azure Active Directory (Azure AD) アカウントを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a694-106">Before you can set up technical support, you must acquire a Microsoft Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="5a694-107">このアカウントは、Microsoft Dynamics 365 Finance and Operations アプリのいずれかの定期売買を設定すると作成されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-107">This account is created when you set up a subscription for one of the Microsoft Dynamics 365 Finance and Operations apps.</span></span>

## <a name="create-an-azure-devops-project"></a><span data-ttu-id="5a694-108">Azure DevOps プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="5a694-108">Create an Azure DevOps project</span></span>
<span data-ttu-id="5a694-109">Lifecycle Services (LCS) プロジェクトの **サポート** タイルは、Azure DevOps を使用し、クライアントを通して送信された問題と、LCS の **サポート** タイルから手動で作成された問題を格納します。</span><span class="sxs-lookup"><span data-stu-id="5a694-109">The **Support** tile in a Lifecycle Services (LCS) project uses Azure DevOps to store issues that are submitted through the client and issues that are manually created from the **Support** tile in LCS.</span></span> <span data-ttu-id="5a694-110">この機能を使用するには、サポートに使用する LCS プロジェクトで Azure DevOps プロジェクトを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a694-110">This functionality requires that a Azure DevOps project be configured in the LCS project that you want to use for support.</span></span> <span data-ttu-id="5a694-111">**サポート** タイルを使用して問題を提出する必要があるすべてのユーザーは、Azure DevOps プロジェクトにアクセスできる必要があり、LCS が Azure DevOps に自身が代わってアクセスを承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a694-111">All users who need to use the **Support** tile to submit an issue must have access to the Azure DevOps project, and must authorize LCS to access Azure DevOps on their own behalf.</span></span> <span data-ttu-id="5a694-112">ほとんどのユーザーは、LCS または Azure DevOps へのアクセス権がありません。</span><span class="sxs-lookup"><span data-stu-id="5a694-112">Most users don't have access to LCS or Azure DevOps.</span></span> <span data-ttu-id="5a694-113">したがって、Azure DevOps プロジェクトでは、問題を提出するために使用できる特別なシステム アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a694-113">Therefore, in the Azure DevOps project, you should create a special system account that can be used to submit issues.</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="5a694-114">新しい Azure DevOps プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="5a694-114">Create a new Azure DevOps project</span></span>

1.  <span data-ttu-id="5a694-115"><https://www.visualstudio.com/> に移動します。</span><span class="sxs-lookup"><span data-stu-id="5a694-115">Go to <https://www.visualstudio.com/>.</span></span>
2.  <span data-ttu-id="5a694-116">右上隅にある **サインイン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-116">Click **Sign in** in the upper-right corner.</span></span>
3.  <span data-ttu-id="5a694-117">サブスクリプションがリンクされているテナントに含まれる AAD アカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="5a694-117">Sign in by using an AAD account that is in the tenant that your subscription is linked to.</span></span> <span data-ttu-id="5a694-118">ブラウザーにすでに資格情報が割り当てられている場合は、サインイン ページは表示されず、右上隅にあるユーザーの名前をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a694-118">If the browser already has your credentials, you won't see the sign-in page and should instead click your name in the upper-right corner.</span></span>
4.  <span data-ttu-id="5a694-119">ページの右側の、**アカウント** で、**今すぐ無料のアカウントを作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-119">On the right side of the page, under **Accounts**, click **Create a free account now**.</span></span>
5.  <span data-ttu-id="5a694-120">アカウント URL を指定し、**アカウントの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-120">Specify an account URL, and then click **Create Account**.</span></span>
6.  <span data-ttu-id="5a694-121">プロジェクトに名前を付け、プロセス テンプレートを指定します。</span><span class="sxs-lookup"><span data-stu-id="5a694-121">Name your project, and specify a process template.</span></span> <span data-ttu-id="5a694-122">これで、プロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-122">Your project should now be created.</span></span>

### <a name="add-users-to-the-azure-devops-project"></a><span data-ttu-id="5a694-123">Azure DevOps プロジェクトへのユーザーの追加</span><span class="sxs-lookup"><span data-stu-id="5a694-123">Add users to the Azure DevOps project</span></span>

1.  <span data-ttu-id="5a694-124">左上にある **Team Services** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-124">In the upper-left corner, click **Team Services**.</span></span>
2.  <span data-ttu-id="5a694-125">**ユーザー** タブで、**追加** をクリックし、サポート エクスペリエンスを使用するユーザーを Azure DevOps アカウントに招待します。</span><span class="sxs-lookup"><span data-stu-id="5a694-125">On the **Users** tab, click **Add**, and invite users who will use the Support experience to the Azure DevOps account.</span></span> <span data-ttu-id="5a694-126">招待する各ユーザーについては、**基本** または **利害関係者** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a694-126">For each user that you invite, select either **Basic** or **Stakeholder**.</span></span>
3.  <span data-ttu-id="5a694-127">左上にある **Team Services** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-127">In the upper-left corner, click **Team Services**.</span></span>
4.  <span data-ttu-id="5a694-128">**参照** をクリックし、以前の手順で作成されたプロジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5a694-128">Click **Browse**, and browse to the project that you created in the previous procedure.</span></span>
5.  <span data-ttu-id="5a694-129">プロジェクト ホーム ページの **メンバー** セクションで、**追加** をクリックして手順 2 で招待したユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="5a694-129">In the **Members** section of the project home page, click **Add**, and add the users that you invited in step 2.</span></span>

### <a name="create-the-support-system-user"></a><span data-ttu-id="5a694-130">サポート システム ユーザーを作成する</span><span class="sxs-lookup"><span data-stu-id="5a694-130">Create the Support system user</span></span>

1.  <span data-ttu-id="5a694-131">Azure AD テナントで新しいユーザーを作成し、**LcsCpsSystemAccount** などの内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a694-131">Create a new user in your Azure AD tenant, and enter a descriptive name, such as **LcsCpsSystemAccount**.</span></span>
2.  <span data-ttu-id="5a694-132">左上にある **Team Services** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-132">In the upper-left corner, click **Team Services**.</span></span>
3.  <span data-ttu-id="5a694-133">**ユーザー** タブで、**追加** をクリックし、手順 1 で作成したシステム ユーザーを招待します。</span><span class="sxs-lookup"><span data-stu-id="5a694-133">On the **Users** tab, click **Add**, and invite the system user that you created in step 1.</span></span> <span data-ttu-id="5a694-134">このユーザーについては、**利害関係者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a694-134">For this user, select **Stakeholder**.</span></span>
4.  <span data-ttu-id="5a694-135">左上にある **Team Services** を再度クリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-135">In the upper-left corner, click **Team Services** again.</span></span>
5.  <span data-ttu-id="5a694-136">**参照** をクリックし、以前に作成したプロジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5a694-136">Click **Browse**, and browse to the project that you created earlier.</span></span>
6.  <span data-ttu-id="5a694-137">プロジェクト ホーム ページの **メンバー** セクションで、**追加** をクリックしてシステム ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="5a694-137">In the **Members** section of the project home page, click **Add**, and add the system user.</span></span>

### <a name="retrieve-the-personal-access-token-for-the-support-system-user"></a><span data-ttu-id="5a694-138">サポート システム ユーザーの個人用アクセス トークンを取得</span><span class="sxs-lookup"><span data-stu-id="5a694-138">Retrieve the personal access token for the Support system user</span></span>

1.  <span data-ttu-id="5a694-139">右上隅にあるユーザー名をクリックして **サインアウト** をクリックすることで、Team Services からサインアウトします。</span><span class="sxs-lookup"><span data-stu-id="5a694-139">Sign out of Team Services by clicking the user name in the upper-right corner and then clicking **Sign out**.</span></span>
2.  <span data-ttu-id="5a694-140">前の手順で作成したサポート システム アカウントを使用して Team Services にサインインします。</span><span class="sxs-lookup"><span data-stu-id="5a694-140">Sign in to Team Services by using the Support system account that you created in the previous procedure.</span></span>
3.  <span data-ttu-id="5a694-141">右上隅でユーザー名をクリックしてから、**自分のプロファイル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-141">In the upper-right corner, click the user name, and then click **My profile**.</span></span>
4.  <span data-ttu-id="5a694-142">**セキュリティ** タブの、**個人用アクセス トークン** タブで、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-142">On the **Security** tab, on the **Personal access tokens** tab, click **Add**.</span></span>
5.  <span data-ttu-id="5a694-143">**LCS サポート システム アカウント** のような説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a694-143">Enter a description, such as **LCS Support system account**.</span></span>
6.  <span data-ttu-id="5a694-144">1 年の有効期限を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a694-144">Select an expiration date of one year.</span></span>
7.  <span data-ttu-id="5a694-145">**選択されているスコープ** をクリックし、**作業項目 (読み取り/書き込み)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a694-145">Click **Selected scopes**, and the select **Work items (read and write)**.</span></span>
8.  <span data-ttu-id="5a694-146">**トークンの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-146">Click **Create token**.</span></span>
9.  <span data-ttu-id="5a694-147">ページから移動した後にアクセスできなくするため、トークンをコピーして、安全な場所に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="5a694-147">Copy the token and paste it in a safe location because it won't be accessible after you move away from the page.</span></span>

## <a name="configure-lcs"></a><span data-ttu-id="5a694-148">LCS の構成</span><span class="sxs-lookup"><span data-stu-id="5a694-148">Configure LCS</span></span>
1.  <span data-ttu-id="5a694-149">アプリケーションが配置された LCS プロジェクトの **所有者** ロールを持っているアカウントを使用して、LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="5a694-149">Sign in to LCS by using an account that has the **Owner** role for the LCS project that the application is deployed in.</span></span>
2.  <span data-ttu-id="5a694-150">LCS でプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="5a694-150">Open the project in LCS.</span></span>
3.  <span data-ttu-id="5a694-151">**プロジェクト設定** をクリックし、**Azure DevOps** リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-151">Click **Project settings**, and then click the **Azure DevOps** link.</span></span>

    <span data-ttu-id="5a694-152">[![LCS-プロジェクト-タイル](./media/lcs-project-tiles-237x300.png)](./media/lcs-project-tiles.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-152">[![LCS-Project-Tiles](./media/lcs-project-tiles-237x300.png)](./media/lcs-project-tiles.png)</span></span>
    
    <span data-ttu-id="5a694-153">[![LCS-プロジェクト-設定-VSO](./media/lcs-project-settings-vso-1024x320.png)](./media/lcs-project-settings-vso.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-153">[![LCS-Project-Settings-VSO](./media/lcs-project-settings-vso-1024x320.png)](./media/lcs-project-settings-vso.png)</span></span>

4.  <span data-ttu-id="5a694-154">**Azure DevOps の設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-154">Click **Setup Azure DevOps**.</span></span>
5.  <span data-ttu-id="5a694-155">**Azure DevOps サイトの URL** フィールドに、前のセクションで作成した Azure DevOps プロジェクトの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a694-155">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps project that you created in the previous section.</span></span>
6.  <span data-ttu-id="5a694-156">**個人用アクセス トークン** フィールドに、前のセクションで作成した個人用アクセス トークンを入力します。</span><span class="sxs-lookup"><span data-stu-id="5a694-156">In the **Personal access token** field, enter the personal access token that you created in the previous section.</span></span> 

    <span data-ttu-id="5a694-157">[![前のセクションで作成した個人用アクセス トークンを入力します。](./media/lcs-project-settings-vso-setup-1.png)](./media/lcs-project-settings-vso-setup-1.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-157">[![Enter the personal access token that you created in the previous section.](./media/lcs-project-settings-vso-setup-1.png)](./media/lcs-project-settings-vso-setup-1.png)</span></span>

7.  <span data-ttu-id="5a694-158">**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-158">Click **Continue**.</span></span>
8.  <span data-ttu-id="5a694-159">使用する VSO プロジェクトを選択し、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-159">Select the VSO project to use, and then click **Continue**.</span></span>
9.  <span data-ttu-id="5a694-160">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-160">Click **Save**.</span></span>
10. <span data-ttu-id="5a694-161">**承認** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-161">Click **Authorize**.</span></span>
11. <span data-ttu-id="5a694-162">確認メッセージ ボックスで、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-162">In the confirmation message box, click **OK**.</span></span>
12. <span data-ttu-id="5a694-163">Visual Studio Online へサインインします。</span><span class="sxs-lookup"><span data-stu-id="5a694-163">Sign in to Visual Studio Online.</span></span>
13. <span data-ttu-id="5a694-164">**承認** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-164">Click **Accept**.</span></span>

## <a name="create-an-issue"></a><span data-ttu-id="5a694-165">問題の作成</span><span class="sxs-lookup"><span data-stu-id="5a694-165">Create an issue</span></span> 
<span data-ttu-id="5a694-166">Microsoft によって公開されている更新プログラムを表示するため、サポート エクスペリエンスが更新されました。</span><span class="sxs-lookup"><span data-stu-id="5a694-166">The Support experience has been updated to show updates that are published by Microsoft.</span></span> <span data-ttu-id="5a694-167">クライアントの上部バーで、**?** をクリックしてから **サポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-167">In the client, on the top bar, click **?**, and then click **Support**.</span></span> 

> [!WARNING]
> <span data-ttu-id="5a694-168">オンプレミスで配置している場合、既存の問題を検索してオンプレミス クライアントから Azure DevOps プロジェクトにサポート インシデントを送信することはできません。</span><span class="sxs-lookup"><span data-stu-id="5a694-168">If you have an on-premises deployment, the option to search for existing issues and submit a support incident from the on-premises client to your Azure DevOps project is not available.</span></span>

<span data-ttu-id="5a694-169">[![wiki1](./media/wiki1-1024x518.png)](./media/wiki1.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-169">[![wiki1](./media/wiki1-1024x518.png)](./media/wiki1.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="5a694-170">Lifecycle Services (LCS) にまだ接続していない場合は、ダイアログ ボックスに接続できる場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-170">If you haven’t already connected to Lifecycle Services (LCS), a dialog box will display where you can connect.</span></span> <span data-ttu-id="5a694-171">続行する前に、接続するリンクをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="5a694-171">Click the link to connect before proceeding.</span></span> 
    <span data-ttu-id="5a694-172">[![クリックして Lifecycle Services に接続する。](./media/wiki2.png)](./media/wiki2.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-172">[![Click to connect to Lifecycle Services.](./media/wiki2.png)](./media/wiki2.png)</span></span>


### <a name="search-for-a-fix"></a><span data-ttu-id="5a694-173">修正プログラムの検索</span><span class="sxs-lookup"><span data-stu-id="5a694-173">Search for a fix</span></span>

<span data-ttu-id="5a694-174">LCS に接続した後は、既存の Microsoft 更新プログラムおよび修正を検索できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-174">After you connect to LCS, you can search for existing Microsoft published updates and fixes.</span></span> <span data-ttu-id="5a694-175">**検索** ボックスに問題を入力し、**入力** を押します。</span><span class="sxs-lookup"><span data-stu-id="5a694-175">Enter your issue in the **Search** box and press **Enter**.</span></span> 

> [!NOTE]
> <span data-ttu-id="5a694-176">すべてのユーザーに対して有効な既存の修正プログラムを検索する機能を使用しない場合は、**SearchExistingFixes** の職務をシステム ユーザー ロールから削除し、この機能を追加するロールにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-176">If you don't want the functionality to search for existing fixes enabled for all users, you can remove the **SearchExistingFixes** duty from the System user role and add it to only those roles which you want to have this functionality.</span></span> <span data-ttu-id="5a694-177">検索結果は、環境に関連する Microsoft 問題検索データに基づきます。</span><span class="sxs-lookup"><span data-stu-id="5a694-177">Search results are based on the Microsoft Issue Search data that is relevant to your environment.</span></span> <span data-ttu-id="5a694-178">既にインストールした修正は、検索結果には含まれません。</span><span class="sxs-lookup"><span data-stu-id="5a694-178">Fixes that you have already installed will not be included in your search results.</span></span> <span data-ttu-id="5a694-179">特定の結果を表示するには、リンクをクリックして詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="5a694-179">To view a specific result, click the link to view the details.</span></span> 

<span data-ttu-id="5a694-180">割り当てられた職務に基づいて、**ダウンロード表示** または **要求表示** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-180">Based on the duties assigned to you, you will see either the **Download view** or the **Request view**.</span></span> 

- <span data-ttu-id="5a694-181">**ダウンロード表示** - 既定では、この表示はシステム管理者のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-181">**Download view** - By default, this view is only available to system administrators.</span></span> <span data-ttu-id="5a694-182">このビューから、直接修正プログラムをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="5a694-182">From this view, you can directly download the hotfix.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="5a694-183">職務 **DownloadHotfix** は、修正プログラムを要求するのではなく、LCS から直接ダウンロードする機能を制御します。</span><span class="sxs-lookup"><span data-stu-id="5a694-183">The duty **DownloadHotfix** controls the ability to directly download fixes from LCS rather than requesting them.</span></span> <span data-ttu-id="5a694-184">既定では、システム管理者のみそのアクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="5a694-184">Only system administrators will have access to it by default.</span></span> <span data-ttu-id="5a694-185">この職務をシステム管理者以外のユーザーに割り当てる場合は、職務を選択したロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="5a694-185">If you want to assign this duty to users other than system administrators, you can do so by adding the duty to the selected roles.</span></span> 
    
- <span data-ttu-id="5a694-186">**要求表示** - 既定では、システム管理者ではないすべてのユーザーがこのビューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-186">**Request view** - By default, this view is available to all users who are not system administrators.</span></span> <span data-ttu-id="5a694-187">このビューから、修正プログラムのダウンロードを要求できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-187">From this view, you can make a request to download the hotfix.</span></span> <span data-ttu-id="5a694-188">修正プログラムをダウンロードする要求を送信した後は、LCS プロジェクトに関連付けられている Azure DevOps プロジェクトに作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-188">After you submit your request to download the hotfix, a work item will be created in the Azure DevOps project that is associated to your LCS project.</span></span> <span data-ttu-id="5a694-189">顧客の IT 管理者は、LCS の **サポート** タイルをクリックし、**修正プログラムの要求** タブをクリックして、要求したすべての修正プログラムを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-189">The customer IT admin can view all requested hotfixes by clicking the **Support** tile in LCS and then clicking the **Hotfix requests** tab.</span></span>

### <a name="search-for-project-work-items-in-azure-devops"></a><span data-ttu-id="5a694-190">Azure DevOps で、プロジェクトの作業項目を検索</span><span class="sxs-lookup"><span data-stu-id="5a694-190">Search for project work items in Azure DevOps</span></span>

<span data-ttu-id="5a694-191">Azure DevOps 管理者は、**#SearchableInFinanceAndOperations** を作業項目にタグ付けすることによって、プロジェクトの作業項目を組織のユーザーに発行することができます。</span><span class="sxs-lookup"><span data-stu-id="5a694-191">The Azure DevOps administrator can publish project work items to your organization users by tagging the work items with **#SearchableInFinanceAndOperations**.</span></span> <span data-ttu-id="5a694-192">タグ付けされた作業項目は、クライアント サポート検索ボックスからユーザーに対して検索可能になります。</span><span class="sxs-lookup"><span data-stu-id="5a694-192">The tagged work items will be searchable for users from the client support search box.</span></span> <span data-ttu-id="5a694-193">検索結果には、Microsoft が公開した更新プログラムや修正プログラムに加えて、タグ付きの Azure DevOps 作業項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a694-193">The search result will include tagged Azure DevOps work items in addition to Microsoft published updates and fixes.</span></span> <span data-ttu-id="5a694-194">次のグラフィックは、公開用のタグ付きの Azure DevOps 作業項目を示しています。</span><span class="sxs-lookup"><span data-stu-id="5a694-194">The following graphic shows a tagged Azure DevOps work item for publishing.</span></span>

<span data-ttu-id="5a694-195">[![vstsTag](./media/VSTS-Tagging.png)](./media/VSTS-Tagging.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-195">[![vstsTag](./media/VSTS-Tagging.png)](./media/VSTS-Tagging.png)</span></span>

<span data-ttu-id="5a694-196">サポート検索ボックスを使用して公開済みの Azure DevOps 作業項目を検索するとき、検索結果は、新しいブラウザー タブに **表示** モードで、作業項目のタイプ、タイトル、状態、および説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-196">When you search for published Azure DevOps work items using the support search box, search results show the work item's type, title, state, and description in a new browser tab with **view** mode.</span></span>  <span data-ttu-id="5a694-197">適切なアクセス許可を持つユーザーが、Azure DevOps の作業項目を編集できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-197">Users with proper permissions can edit the work item in Azure DevOps.</span></span> <span data-ttu-id="5a694-198">次のグラフィックは、公開された Azure DevOps 作業項目の検索結果を示しています。</span><span class="sxs-lookup"><span data-stu-id="5a694-198">The following graphic shows the search result of a published Azure DevOps work item.</span></span>

<span data-ttu-id="5a694-199">[![ViewVSTS](./media/ViewVSTSItem.png)](./media/ViewVSTSItem.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-199">[![ViewVSTS](./media/ViewVSTSItem.png)](./media/ViewVSTSItem.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5a694-200">発行済みの Azure DevOps 作業項目は、組織のユーザーにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-200">The published Azure DevOps work items are only visible to your organization's users.</span></span>  

### <a name="create-and-submit-a-new-issue"></a><span data-ttu-id="5a694-201">新しい問題の作成および送信</span><span class="sxs-lookup"><span data-stu-id="5a694-201">Create and submit a new issue</span></span>
<span data-ttu-id="5a694-202">検索結果から修正プログラムが見つからない場合は、**作成** をクリックし、新しい問題を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-202">If you don’t see a fix in the search results, you can create a new issue by clicking **Create**.</span></span> <span data-ttu-id="5a694-203">これは以前のリリースで使用できる機能と同じで、以前の手順で説明しています。</span><span class="sxs-lookup"><span data-stu-id="5a694-203">This is the same functionality that is available for previous releases and is documented in earlier procedures.</span></span>

## <a name="work-with-issues-in-lcs"></a><span data-ttu-id="5a694-204">LCS での問題についての作業</span><span class="sxs-lookup"><span data-stu-id="5a694-204">Work with issues in LCS</span></span>

### <a name="view-issues"></a><span data-ttu-id="5a694-205">問題の表示</span><span class="sxs-lookup"><span data-stu-id="5a694-205">View issues</span></span>
<span data-ttu-id="5a694-206">LCS **サポート** タイルでは、問題が LCS プロジェクトに関連付けられている Azure DevOps プロジェクトで作業項目として保存されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-206">In the LCS **Support** tile, issues are stored as work items in the Azure DevOps project that is associated with the LCS project.</span></span> <span data-ttu-id="5a694-207">具体的には、問題は、Azure DevOps プロジェクトのタイプに応じて **問題** または **懸案事項** タイプの作業項目として **AxAndLcsGeneratedIssues** 領域に保存されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-207">Specifically, issues are stored as work items of the **Issue** or **Impediment** type, depending on the type of Azure DevOps project, in the **AxAndLcsGeneratedIssues** area.</span></span> <span data-ttu-id="5a694-208">その地域にあるタイプの作業項目のすべてが、**サポート** タイルの問題リストに含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a694-208">Every work item of one of those types in that area will be included in the list of issues in the **Support** tile.</span></span> <span data-ttu-id="5a694-209">Azure DevOps で問題点が変更されると、サポート案件で変更内容が反映されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-209">If an issue is modified in Azure DevOps, the changes will be reflected in Support issues.</span></span> <span data-ttu-id="5a694-210">問題は、Azure DevOps プロジェクト内のユーザーに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5a694-210">Issues can be assigned to any user in the Azure DevOps project.</span></span> <span data-ttu-id="5a694-211">ユーザーは、Azure DevOps で案件を取り扱うために、LCS にアクセスする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5a694-211">Users don't need to have access to LCS to work with issues in Azure DevOps.</span></span>

1.  <span data-ttu-id="5a694-212">[lcs.dynamics.com,](https://lcs.dynamics.com/en/) に移動しサインインします。</span><span class="sxs-lookup"><span data-stu-id="5a694-212">Go to [lcs.dynamics.com,](https://lcs.dynamics.com/en/) and sign in.</span></span>
2.  <span data-ttu-id="5a694-213">払出を表示する環境に関連付けられている LCS プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="5a694-213">Open the LCS project that is associated with the environment that you want to view issues for.</span></span>
3.  <span data-ttu-id="5a694-214">**サポート** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-214">Click the **Support** tile.</span></span> <span data-ttu-id="5a694-215">作成された問題の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="5a694-215">A list of the issues that have been created appears.</span></span>

    <span data-ttu-id="5a694-216">[![LCS-CPS-list](./media/lcs-cps-list-1024x243.png)](./media/lcs-cps-list.png)</span><span class="sxs-lookup"><span data-stu-id="5a694-216">[![LCS-CPS-list](./media/lcs-cps-list-1024x243.png)](./media/lcs-cps-list.png)</span></span>

### <a name="edit-issues"></a><span data-ttu-id="5a694-217">項目を編集</span><span class="sxs-lookup"><span data-stu-id="5a694-217">Edit issues</span></span>
1.  <span data-ttu-id="5a694-218">**問題** グリッドで、問題のタイトルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-218">In the **Issues** grid, click the title of an issue.</span></span>
2.  <span data-ttu-id="5a694-219">このトピックの最初のセクションで設定した Azure DevOps プロジェクトへのアクセス権を持つアカウントを使用して、Azure DevOps へサインインし、**Azure DevOps プロジェクトを作成** します。</span><span class="sxs-lookup"><span data-stu-id="5a694-219">If necessary, sign in to Azure DevOps by using an account that has access to the Azure DevOps project that you set up in the first section of this topic, **Create an Azure DevOps project**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="5a694-220">Azure DevOps には、サインインが必要な場合に作業項目を編集するためのリンクが正しく機能しないという問題があります。</span><span class="sxs-lookup"><span data-stu-id="5a694-220">There is an issue in Azure DevOps, where the link to edit work items doesn't work correctly if sign-in is required.</span></span> <span data-ttu-id="5a694-221">Azure DevOps にサインインした後に **自分自身に割り当て** クエリが表示された場合、LCS に戻って、問題グリッドで問題のタイトルをもう一度クリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-221">If you see the **Assigned to me** query after you sign in to Azure DevOps, go back to LCS, and click the title of the issue in the issue grid again.</span></span>

3.  <span data-ttu-id="5a694-222">Azure DevOps エディターが開きます。</span><span class="sxs-lookup"><span data-stu-id="5a694-222">The Azure DevOps editor opens.</span></span> <span data-ttu-id="5a694-223">問題点を編集し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="5a694-223">Edit the issue, and then save your changes.</span></span> <span data-ttu-id="5a694-224">変更は **サポート** タイルに反映されます。</span><span class="sxs-lookup"><span data-stu-id="5a694-224">The changes will be reflected in the **Support** tile.</span></span>


### <a name="submit-an-issue-to-microsoft"></a><span data-ttu-id="5a694-225">Microsoft に問題を送信</span><span class="sxs-lookup"><span data-stu-id="5a694-225">Submit an issue to Microsoft</span></span>

<span data-ttu-id="5a694-226">Microsoft サポートに問題を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="5a694-226">You can submit issues to Microsoft support.</span></span> <span data-ttu-id="5a694-227">Microsoft に問題点を送信すると、問題に関する情報と添付ファイルを Microsoft サポート インシデントに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5a694-227">When you submit an issue to Microsoft, the information and attachments in the issue can be included in the Microsoft support incident.</span></span> 

<span data-ttu-id="5a694-228">Microsoft に問題を送信するためには、LCS ユーザーに有効な Microsoft サポート プランが必要です。</span><span class="sxs-lookup"><span data-stu-id="5a694-228">LCS users must have a valid Microsoft support plan to submit issues to Microsoft.</span></span> <span data-ttu-id="5a694-229">Microsoft に問題を報告する上で問題が発生している場合は、管理者と連携して、LCS 資格情報が、Microsoft Partner Source Business Center との組織のサポート計画に追加されている、または関連付けられているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5a694-229">If you have trouble submitting issues to Microsoft, work with your administrator to make sure that your LCS credentials are added to or associated with your organization's support plan with Microsoft Partner Source Business Center.</span></span>

1.  <span data-ttu-id="5a694-230">**問題** グリッドで、Microsoft に送信する問題を選択して、**Microsoft に送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-230">In the **Issue** grid, select the issue to submit to Microsoft, and then click **Submit to Microsoft**.</span></span>
2.  <span data-ttu-id="5a694-231">アカウントが複数のサポート組織に関連付けられている場合、使用する組織を選択して Microsoft サポート インシデントを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a694-231">If your account is associated with multiple support organizations, select the organization to use to create the Microsoft support incident.</span></span>
3.  <span data-ttu-id="5a694-232">**問題検索** を使用して、問題がまだ解決されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5a694-232">Use **Issue search** to verify that your issue hasn't already been solved.</span></span>
4.  <span data-ttu-id="5a694-233">**問題検索** により問題が解決されない場合、ページの下部にある **作成インシデント** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-233">If **Issue search** doesn't provide a solution to your issue, click **Create incident** at the bottom of the page.</span></span>
5.  <span data-ttu-id="5a694-234">Microsoft サポート チームに診断データを共有します。</span><span class="sxs-lookup"><span data-stu-id="5a694-234">Share diagnostic data with the Microsoft support team.</span></span> <span data-ttu-id="5a694-235">バージョン情報を提供することによって、問題をより迅速に解決できます。</span><span class="sxs-lookup"><span data-stu-id="5a694-235">By providing version information, your issues can be resolved more quickly.</span></span>
6.  <span data-ttu-id="5a694-236">問題を説明し、連絡先情報を入力してから、**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-236">Describe your issue, provide your contact information, and then click **Submit**.</span></span>

## <a name="support-settings"></a><span data-ttu-id="5a694-237">サポート設定</span><span class="sxs-lookup"><span data-stu-id="5a694-237">Support settings</span></span> 

> [!NOTE]
> <span data-ttu-id="5a694-238">このセクションの情報は、オンプレミスの配置には適用されません。</span><span class="sxs-lookup"><span data-stu-id="5a694-238">The information in this section is not applicable to on-premises deployments.</span></span> 

<span data-ttu-id="5a694-239">アプリケーションを Lifecycle Services から配置するとき、構成は必要ありません。それは、サポート ツールが、配置された Finance and Operations の供給元の同じ LCS プロジェクトに問題を自動的に保存するためです。</span><span class="sxs-lookup"><span data-stu-id="5a694-239">When you deploy your application from Lifecycle Services, no configuration is required, because the Support tool automatically saves any issues to the same LCS project that Finance and Operations was deployed from.</span></span> <span data-ttu-id="5a694-240">サポートされている LCS プロジェクトを確認するには、**システム管理** > **設定** > **システム パラメーター** に移動し、**ヘルプ** > **サポートの連絡先** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a694-240">To verify the LCS project that Support uses, go to **System administration** > **Setup** > **System parameters**, and then click **Help** > **Support Contact**.</span></span> 

## <a name="prevent-users-from-creating-issues-from-the-client"></a><span data-ttu-id="5a694-241">ユーザーが、クライアントからの問題を作成できなようにする</span><span class="sxs-lookup"><span data-stu-id="5a694-241">Prevent users from creating issues from the client</span></span>
<span data-ttu-id="5a694-242">既定では、システム ユーザー ロールに *SysLCSCPSIssueEntry* という権限が割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="5a694-242">By default, the System user role has the privilege, *SysLCSCPSIssueEntry* assigned.</span></span> <span data-ttu-id="5a694-243">この権限は、[ヘルプ] メニューの **サポート チームに連絡** メニュー項目へのアクセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="5a694-243">This privilege controls access to the **Contact your support team** menu item on the Help menu.</span></span> <span data-ttu-id="5a694-244">ユーザーがクライアントからの問題を作成して送信できないようにするには、システム ユーザー ロールからこの権限を削除します。</span><span class="sxs-lookup"><span data-stu-id="5a694-244">If you want to prevent users from being able to create and submit issues from the client, remove this privilege from the System user role.</span></span>
