---
title: "プロジェクト時間入力モバイル ワークスペース"
description: "このトピックでは、プロジェクト時間入力モバイル ワークスペースに関する情報を提供します。 このワークスペースにより、ユーザーはモバイル デバイスを使用して入力をし、プロジェクトに対して時間を節約できます。"
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: c04ffccdcbf104b1d5db30a41116663fcedd4e1d
ms.contentlocale: ja-jp
ms.lasthandoff: 12/01/2017

---

# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="66794-104">プロジェクト時間入力モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="66794-104">Project time entry mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="66794-105">このトピックでは、[プロジェクト時間入力] モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="66794-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="66794-106">このワークスペースにより、ユーザーはモバイル デバイスを使用して入力をし、プロジェクトに対して時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="66794-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="66794-107">このモバイル ワークスペースは、Microsoft Dynamics 365 for Unified Operations モバイル アプリで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="66794-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="66794-108">概要</span><span class="sxs-lookup"><span data-stu-id="66794-108">Overview</span></span>
<span data-ttu-id="66794-109">毎日の作業の一環として、プロジェクト リソースは多くの場合オンサイトか、または出張します。</span><span class="sxs-lookup"><span data-stu-id="66794-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="66794-110">**プロジェクト時間入力** モバイル ワークスペースでは、選択したモバイル デバイスで、プロジェクトに対する支払請求可能または非請求可能な時間を入力できます。</span><span class="sxs-lookup"><span data-stu-id="66794-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="66794-111">そのためプロジェクト リソースは、いつでも、どこでも時間のエントリを記録できます。</span><span class="sxs-lookup"><span data-stu-id="66794-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="66794-112">既に記録されている時間のエントリを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="66794-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="66794-113">具体的には、[プロジェクト時間の入力] モバイル ワークスペースでは、ユーザーは、これらのタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="66794-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="66794-114">選択された任意の日付について、特定のタスクに費やした時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="66794-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="66794-115">時間を入力するプロジェクトを特定するため、プロジェクト名または顧客で検索します。</span><span class="sxs-lookup"><span data-stu-id="66794-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="66794-116">費やした時間のカテゴリおよび活動を指定します。</span><span class="sxs-lookup"><span data-stu-id="66794-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="66794-117">プロジェクトに支払請求可能または非請求可能として時間を記録します。</span><span class="sxs-lookup"><span data-stu-id="66794-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="66794-118">必要に応じて外部または内部コメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="66794-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="66794-119">前提条件</span><span class="sxs-lookup"><span data-stu-id="66794-119">Prerequisites</span></span>
<span data-ttu-id="66794-120">組織に配置されている Microsoft Dynamics 365 のバージョンに基づいて、前提条件は異なります。</span><span class="sxs-lookup"><span data-stu-id="66794-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="66794-121">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition を使用している場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="66794-121">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span></span>
<span data-ttu-id="66794-122">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition を組織に配置している場合、システム管理者は**プロジェクト時間の入力**モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66794-122">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="66794-123">手順については、「[モバイル ワークスペースの公開](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66794-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="66794-124">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を使用している場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="66794-124">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="66794-125">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム 更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="66794-125">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="66794-126">前提条件</span><span class="sxs-lookup"><span data-stu-id="66794-126">Prerequisite</span></span></th>
<th><span data-ttu-id="66794-127">役割</span><span class="sxs-lookup"><span data-stu-id="66794-127">Role</span></span></th>
<th><span data-ttu-id="66794-128">説明</span><span class="sxs-lookup"><span data-stu-id="66794-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="66794-129">KB 4018050 を実装します。</span><span class="sxs-lookup"><span data-stu-id="66794-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="66794-130">システム管理者</span><span class="sxs-lookup"><span data-stu-id="66794-130">System administrator</span></span></td>
<td><span data-ttu-id="66794-131">KB 4018050 は、<strong>プロジェクト時間入力</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。</span><span class="sxs-lookup"><span data-stu-id="66794-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="66794-132">KB 4018050 を実装するには、システム管理者は次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="66794-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="66794-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Microsoft Dynamics Lifecycle Services (LCS) からメタデータ修正プログラムをダウンロードします</a>。</span><span class="sxs-lookup"><span data-stu-id="66794-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="66794-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">メタデータ修正プログラムをインストールします。</a></span><span class="sxs-lookup"><span data-stu-id="66794-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="66794-135"><strong>ApplicationSuite</strong> と <strong>ProjectMobile</strong> モデルを含む <a href="../../dev-itpro/deployment/create-apply-deployable-package.md">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="66794-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="66794-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">配置可能パッケージを適用します</a>。</span><span class="sxs-lookup"><span data-stu-id="66794-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66794-137">[<strong>プロジェクト時間の入力</strong>] モバイル ワークスペースを公開します。</span><span class="sxs-lookup"><span data-stu-id="66794-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="66794-138">システム管理者</span><span class="sxs-lookup"><span data-stu-id="66794-138">System administrator</span></span></td>
<td><span data-ttu-id="66794-139">「<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66794-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="66794-140">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="66794-140">Download and install the mobile app</span></span>

<span data-ttu-id="66794-141">Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="66794-141">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="66794-142">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="66794-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="66794-143">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="66794-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="66794-144">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="66794-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="66794-145">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="66794-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="66794-146">Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="66794-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="66794-147">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="66794-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="66794-148">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="66794-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="66794-149">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66794-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="66794-150">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66794-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="66794-151">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="66794-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="66794-152">プロジェクト時間入力モバイル ワークスペースを使用して時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="66794-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="66794-153">モバイル デバイスで、**プロジェクト時間入力** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="66794-154">**時間入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-154">Select **Time entry**.</span></span> <span data-ttu-id="66794-155">現在の週のカレンダーの日付が表示されます。</span><span class="sxs-lookup"><span data-stu-id="66794-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="66794-156">選択された日付で、**アクション** &gt; **新しいエントリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="66794-157">記録する時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="66794-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="66794-158">時間入力するプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-158">Select the project for the time entry.</span></span> <span data-ttu-id="66794-159">オフラインで使用する場合のために、アプリに読み込まれたプロジェクトのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66794-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="66794-160">既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="66794-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="66794-161">詳細については、[モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66794-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="66794-162">プロジェクトが一覧にない場合は、[検索] を選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="66794-163">名前で検索するか、プロジェクト名または顧客での検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="66794-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="66794-164">カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-164">Select a category.</span></span> <span data-ttu-id="66794-165">オフラインで使用する場合のために、アプリに読み込まれたカテゴリのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66794-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="66794-166">既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="66794-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="66794-167">詳細については、[モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66794-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="66794-168">カテゴリが一覧にない場合は、[検索] を選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="66794-169">カテゴリで検索するか、カテゴリ名での検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="66794-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="66794-170">活動を選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-170">Select an activity.</span></span> <span data-ttu-id="66794-171">一覧には、オフラインで使用するためにアプリケーションに読み込まれた活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="66794-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="66794-172">既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="66794-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="66794-173">詳細については、[モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66794-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="66794-174">活動が一覧にない場合は、[検索] を選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="66794-175">活動番号で検索するか、目的別の検索に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="66794-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="66794-176">明細行プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-176">Select the line property.</span></span>
12. <span data-ttu-id="66794-177">オプション: 外部または内部コメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="66794-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="66794-178">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66794-178">Select **Done**.</span></span>

