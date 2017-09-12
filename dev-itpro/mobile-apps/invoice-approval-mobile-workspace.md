---
title: "モバイル ワークスペースの請求書承認"
description: "このトピックでは、請求書承認モバイル ワークスペースに関する情報を提供します。 このワークスペースは、仕入先請求書ヘッダーのワークフロー プロセスを通して割り当てられている請求書の一覧を提供します。"
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 24818afbbdf328c8fd3eea691634db24e443b07b
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="41281-104">モバイル ワークスペースの請求書承認</span><span class="sxs-lookup"><span data-stu-id="41281-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="41281-105">このトピックでは、[**請求書承認**] モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="41281-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="41281-106">このワークスペースは、仕入先請求書ヘッダーのワークフロー プロセスを通して割り当てられている請求書の一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="41281-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="41281-107">このモバイル ワークスペースは、Microsoft Dynamics 365 for Unified Operations モバイル アプリで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="41281-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="41281-108">概要</span><span class="sxs-lookup"><span data-stu-id="41281-108">Overview</span></span>

<span data-ttu-id="41281-109">[**請求書承認**] モバイル ワークスペースは、買掛金勘定の担当者およびマネージャーが、仕入先請求書ヘッダーのワークフロー プロセスの一部として割り当てられている請求書を表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="41281-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="41281-110">請求書情報 (明細行と配送の詳細も含む) を表示して、通知された承認決定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="41281-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="41281-111">ワークスペースから、ワークフロー プロセスを通して請求書を移動するアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="41281-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="41281-112">前提条件</span><span class="sxs-lookup"><span data-stu-id="41281-112">Prerequisites</span></span>

<span data-ttu-id="41281-113">このモバイル ワークスペースを使用するには、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="41281-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41281-114">前提条件</span><span class="sxs-lookup"><span data-stu-id="41281-114">Prerequisite</span></span></th>
<th><span data-ttu-id="41281-115">役割</span><span class="sxs-lookup"><span data-stu-id="41281-115">Role</span></span></th>
<th><span data-ttu-id="41281-116">説明</span><span class="sxs-lookup"><span data-stu-id="41281-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41281-117">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 2017 年 7 月の更新プログラムを組織内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41281-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="41281-118">システム管理者</span><span class="sxs-lookup"><span data-stu-id="41281-118">System administrator</span></span></td>
<td><span data-ttu-id="41281-119"><a href="../deployment/deploy-demo-environment.md">デモ環境の配置</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41281-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="41281-120">[<strong>請求書承認</strong>] モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41281-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="41281-121">システム管理者</span><span class="sxs-lookup"><span data-stu-id="41281-121">System administrator</span></span></td>
<td><span data-ttu-id="41281-122">「<a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41281-122">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="41281-123">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="41281-123">Download and install the mobile app</span></span>

<span data-ttu-id="41281-124">Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="41281-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="41281-125">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="41281-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="41281-126">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="41281-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="41281-127">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="41281-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="41281-128">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="41281-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="41281-129">Microsoft Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="41281-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="41281-130">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="41281-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="41281-131">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="41281-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="41281-132">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="41281-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="41281-133">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41281-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="41281-134">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="41281-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="41281-135">請求書承認モバイル ワークスペースを使用して請求書を承認します。</span><span class="sxs-lookup"><span data-stu-id="41281-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="41281-136">モバイル デバイスで、[**請求書承認**] ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="41281-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="41281-137">仕入先請求書ヘッダーのワークフロー プロセスによって割り当てられた請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="41281-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="41281-138">[**請求書の詳細**] ページで、仕入先や日付情報などの請求書ヘッダー情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="41281-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="41281-139">[**請求明細行の詳細**] ビューで、関係する詳細な情報を表示する請求書の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="41281-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="41281-140">[**請求明細行の詳細**] ビューで、[**配分**] を選択して明細行の配分を表示します。</span><span class="sxs-lookup"><span data-stu-id="41281-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="41281-141">ここで、請求明細行の勘定を表示できます。</span><span class="sxs-lookup"><span data-stu-id="41281-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="41281-142">表示される情報には、財務分析コードおよび主勘定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="41281-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="41281-143">[**請求明細行の詳細**] ページで、[**配分**] を選択してすべての配分を表示します。</span><span class="sxs-lookup"><span data-stu-id="41281-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="41281-144">ここで、請求書全体の勘定を表示できます。</span><span class="sxs-lookup"><span data-stu-id="41281-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="41281-145">表示される情報には、財務分析コードおよび主勘定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="41281-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="41281-146">[**添付ファイル**] を選択して、請求書に添付されているメモまたはファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="41281-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="41281-147">[**請求書の詳細**] ページで、確認プロセスを完了する適切なワークフロー アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="41281-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="41281-148">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41281-148">Select **Done**.</span></span>

