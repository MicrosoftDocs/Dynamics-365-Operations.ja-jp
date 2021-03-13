---
title: モバイル ワークスペースの請求書承認
description: このトピックでは、請求書承認モバイル ワークスペースに関する情報を提供します。
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 1a7aa1a03791b8ccb7050389097d1272f5930a49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127572"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="e85d6-103">モバイル ワークスペースの請求書承認</span><span class="sxs-lookup"><span data-stu-id="e85d6-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e85d6-104">このトピックでは、**請求書承認** モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="e85d6-105">このワークスペースは、仕入先請求書ヘッダーのワークフロー プロセスを通して割り当てられている請求書の一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="e85d6-106">このモバイル ワークスペースは、Finance and Operations モバイル アプリで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="e85d6-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="e85d6-107">概要</span><span class="sxs-lookup"><span data-stu-id="e85d6-107">Overview</span></span>

<span data-ttu-id="e85d6-108">**請求書承認** モバイル ワークスペースは、買掛金勘定の担当者およびマネージャーが、仕入先請求書ヘッダーのワークフロー プロセスの一部として割り当てられている請求書を表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e85d6-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="e85d6-109">請求書情報 (明細行と配送の詳細も含む) を表示して、通知された承認決定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="e85d6-110">ワークスペースから、ワークフロー プロセスを通して請求書を移動するアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="e85d6-111">前提条件</span><span class="sxs-lookup"><span data-stu-id="e85d6-111">Prerequisites</span></span>

<span data-ttu-id="e85d6-112">このモバイル ワークスペースを使用するには、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="e85d6-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e85d6-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="e85d6-113">Prerequisite</span></span></th>
<th><span data-ttu-id="e85d6-114">役割</span><span class="sxs-lookup"><span data-stu-id="e85d6-114">Role</span></span></th>
<th><span data-ttu-id="e85d6-115">説明</span><span class="sxs-lookup"><span data-stu-id="e85d6-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e85d6-116">Microsoft Dynamics 365 Finance は組織内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e85d6-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="e85d6-117">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e85d6-117">System administrator</span></span></td>
<td><span data-ttu-id="e85d6-118"><a href="../deployment/deploy-demo-environment.md">デモ環境の配置</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e85d6-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e85d6-119"><strong>請求書承認</strong> モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e85d6-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="e85d6-120">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e85d6-120">System administrator</span></span></td>
<td><span data-ttu-id="e85d6-121">「<a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e85d6-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="e85d6-122">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="e85d6-122">Download and install the mobile app</span></span>

<span data-ttu-id="e85d6-123">Finance and Operations モバイル アプリのダウンロードとインストール。</span><span class="sxs-lookup"><span data-stu-id="e85d6-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="e85d6-124">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="e85d6-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="e85d6-125">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="e85d6-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="e85d6-126">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="e85d6-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="e85d6-127">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="e85d6-128">Microsoft Dynamics 365 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="e85d6-129">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="e85d6-130">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="e85d6-131">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="e85d6-132">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e85d6-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="e85d6-133">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="e85d6-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="e85d6-134">請求書承認モバイル ワークスペースを使用して請求書を承認します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="e85d6-135">モバイル デバイスで、**請求書承認** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="e85d6-136">仕入先請求書ヘッダーのワークフロー プロセスによって割り当てられた請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="e85d6-137">**請求書の詳細** ページで、仕入先や日付情報などの請求書ヘッダー情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="e85d6-138">**請求明細行の詳細** ビューで、関係する詳細な情報を表示する請求書の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="e85d6-139">**請求明細行の詳細** ビューで、**配分** を選択して明細行の配分を表示します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="e85d6-140">ここで、請求明細行の勘定を表示できます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="e85d6-141">表示される情報には、財務分析コードおよび主勘定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="e85d6-142">**請求明細行の詳細** ページで、**配分** を選択してすべての配分を表示します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="e85d6-143">ここで、請求書全体の勘定を表示できます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="e85d6-144">表示される情報には、財務分析コードおよび主勘定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e85d6-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="e85d6-145">**添付ファイル** を選択して、請求書に添付されているメモまたはファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="e85d6-146">**請求書の詳細** ページで、確認プロセスを完了する適切なワークフロー アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="e85d6-147">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e85d6-147">Select **Done**.</span></span>
