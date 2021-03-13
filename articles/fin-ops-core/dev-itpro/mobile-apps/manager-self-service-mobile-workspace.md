---
title: 自分のチーム モバイル ワークスペース
description: このトピックでは、管理者が直属の部下と拡張スタッフを表示できる自分のチーム モバイル ワークスペースについて、情報を提供します。
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 79678c42545a07054af00cd408e04e9d1a42caed
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127548"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="dfa2c-103">自分のチーム モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="dfa2c-103">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfa2c-104">このトピックでは、**自分のチーム** モバイル ワークスペースについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-104">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="dfa2c-105">このワークスペースでは、管理者が直属の部下および拡張スタッフを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-105">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="dfa2c-106">また、レポート チェーン内の各個人に称賛を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-106">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="dfa2c-107">このモバイル ワークスペースは、Finance and Operations モバイル アプリで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="dfa2c-108">概要</span><span class="sxs-lookup"><span data-stu-id="dfa2c-108">Overview</span></span> 
<span data-ttu-id="dfa2c-109">**自分のチーム** モバイル ワークスペースでは、管理者がこれらのタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-109">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="dfa2c-110">管理者の直属の部下の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-110">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="dfa2c-111">管理者の拡張レポート チームの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-111">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="dfa2c-112">チームの各メンバーに関する生年月日や勤続年数と日数、および報酬と業績情報などの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-112">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="dfa2c-113">管理者の拡張レポート チーム内のいずれかの個人に、称賛を送信します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-113">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dfa2c-114">前提条件</span><span class="sxs-lookup"><span data-stu-id="dfa2c-114">Prerequisites</span></span>
<span data-ttu-id="dfa2c-115">このモバイル ワークスペースを使用するには、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-115">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfa2c-116">前提条件</span><span class="sxs-lookup"><span data-stu-id="dfa2c-116">Prerequisite</span></span></th>
<th><span data-ttu-id="dfa2c-117">役割</span><span class="sxs-lookup"><span data-stu-id="dfa2c-117">Role</span></span></th>
<th><span data-ttu-id="dfa2c-118">説明</span><span class="sxs-lookup"><span data-stu-id="dfa2c-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa2c-119">次の製品のいずれかを組織内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-119">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="dfa2c-120">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="dfa2c-120">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="dfa2c-121">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="dfa2c-121">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="dfa2c-122">システム管理者</span><span class="sxs-lookup"><span data-stu-id="dfa2c-122">System administrator</span></span></td>
<td><span data-ttu-id="dfa2c-123">組織にまだ Finance and Operations アプリが配置されていない場合は、<a href="../deployment/deploy-demo-environment.md">デモ環境の配置</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-123">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="dfa2c-124">組織にまだ人事管理が配置されていない場合、システム管理者は<a href="https://dynamics.microsoft.com/human-resources/overview/">人事管理ウェブページ</a>から評価版バージョンにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-124">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa2c-125"><strong>自分のチーム</strong> モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-125">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="dfa2c-126">システム管理者</span><span class="sxs-lookup"><span data-stu-id="dfa2c-126">System administrator</span></span></td>
<td><span data-ttu-id="dfa2c-127">「<a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-127">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="dfa2c-128">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="dfa2c-128">Download and install the mobile app</span></span>

<span data-ttu-id="dfa2c-129">Finance and Operations モバイル アプリのダウンロードとインストール。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-129">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="dfa2c-130">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="dfa2c-130">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="dfa2c-131">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="dfa2c-131">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="dfa2c-132">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-132">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="dfa2c-133">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-133">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="dfa2c-134">Microsoft Dynamics 365 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-134">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="dfa2c-135">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-135">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="dfa2c-136">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-136">Enter your credentials.</span></span>
4.  <span data-ttu-id="dfa2c-137">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-137">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="dfa2c-138">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-138">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="dfa2c-139">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="dfa2c-139">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="dfa2c-140">自分のチーム モバイル ワークスペースを使用して、チーム メンバーを表示</span><span class="sxs-lookup"><span data-stu-id="dfa2c-140">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="dfa2c-141">モバイル アプリで、**自分のチーム** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-141">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="dfa2c-142">チーム メンバーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-142">A list of team members is shown.</span></span> <span data-ttu-id="dfa2c-143">一覧では、各チーム メンバーのタイトル、およびそのメンバーの直属の部下にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-143">The list also shows each team member's title, and any direct reports that the member has.</span></span>
2.  <span data-ttu-id="dfa2c-144">チーム メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-144">Select a team member.</span></span> <span data-ttu-id="dfa2c-145">**チーム メンバーの概要** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-145">The **Team member summary** page appears.</span></span> <span data-ttu-id="dfa2c-146">このページには、チーム メンバーの生年月日や勤続日数、勤続期間、および現在の職位の年数と報酬情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-146">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="dfa2c-147">自分のチーム モバイル ワークスペースを使用して、拡張チーム メンバーを表示</span><span class="sxs-lookup"><span data-stu-id="dfa2c-147">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="dfa2c-148">モバイル アプリで、**自分のチーム** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-148">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="dfa2c-149">チーム メンバーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-149">A list of team members is shown.</span></span> <span data-ttu-id="dfa2c-150">一覧では、各チーム メンバーのタイトル、およびそのメンバーの直属の部下にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-150">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="dfa2c-151">**直属の部下** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-151">Select the **Direct reports** link.</span></span> <span data-ttu-id="dfa2c-152">拡張チーム メンバーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-152">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="dfa2c-153">チーム メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-153">Select a team member.</span></span> <span data-ttu-id="dfa2c-154">**チーム メンバーの概要** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-154">The **Team member summary** page appears.</span></span> <span data-ttu-id="dfa2c-155">このページには、チーム メンバーの生年月日や勤続日数、勤続期間、および現在の職位の年数と報酬情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-155">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="dfa2c-156">自分のチーム モバイル ワークスペースを使用して、チーム メンバーについて称賛を送信</span><span class="sxs-lookup"><span data-stu-id="dfa2c-156">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="dfa2c-157">モバイル アプリで、**自分のチーム** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-157">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="dfa2c-158">チーム メンバーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-158">A list of team members is shown.</span></span> <span data-ttu-id="dfa2c-159">一覧では、各チーム メンバーのタイトル、およびそのメンバーの直属の部下にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-159">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="dfa2c-160">チーム メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-160">Select a team member.</span></span> <span data-ttu-id="dfa2c-161">**チーム メンバーの概要** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-161">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="dfa2c-162">**称賛の送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-162">Select **Send praise**.</span></span> 
1. <span data-ttu-id="dfa2c-163">送信する称賛のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-163">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="dfa2c-164">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dfa2c-164">Select **Done**.</span></span>
