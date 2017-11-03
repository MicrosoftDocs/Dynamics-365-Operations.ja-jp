---
title: "会社のディレクトリ モバイル ワークスペース"
description: "このトピックでは、ユーザーが閲覧して組織内の他の従業員と連絡が取れるようにする、会社のディレクトリ モバイル ワークスペースに関する情報を提供します。"
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Talent, Operations
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73062587a2cfed3af212f618df48a26df574ee87
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="88206-103">会社のディレクトリ モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="88206-103">Company directory mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="88206-104">このトピックでは、**会社のディレクトリ** モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="88206-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="88206-105">このワークスペースで、ユーザーは閲覧して組織内の他の従業員と連絡を取ることができます。</span><span class="sxs-lookup"><span data-stu-id="88206-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="88206-106">このモバイル ワークスペースは、Microsoft Dynamics 365 for Unified Operations モバイル アプリでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="88206-106">This mobile workspace can be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="88206-107">概要</span><span class="sxs-lookup"><span data-stu-id="88206-107">Overview</span></span>
<span data-ttu-id="88206-108">**会社のディレクトリ** モバイル ワークスペースにより、ユーザーは次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="88206-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="88206-109">組織内の従業員の一覧を表示する。</span><span class="sxs-lookup"><span data-stu-id="88206-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="88206-110">組織内の従業員を検索する。</span><span class="sxs-lookup"><span data-stu-id="88206-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="88206-111">従業員の連絡先情報を表示する。</span><span class="sxs-lookup"><span data-stu-id="88206-111">View contact information for employees.</span></span>
- <span data-ttu-id="88206-112">プロファイル情報から従業員に連絡する。</span><span class="sxs-lookup"><span data-stu-id="88206-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="88206-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="88206-113">Prerequisites</span></span>
<span data-ttu-id="88206-114">このモバイル ワークスペースを使用するには、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="88206-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88206-115">前提条件</span><span class="sxs-lookup"><span data-stu-id="88206-115">Prerequisite</span></span></th>
<th><span data-ttu-id="88206-116">役割</span><span class="sxs-lookup"><span data-stu-id="88206-116">Role</span></span></th>
<th><span data-ttu-id="88206-117">説明</span><span class="sxs-lookup"><span data-stu-id="88206-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88206-118">次の製品のいずれかを組織内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88206-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="88206-119">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="88206-119">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span></li>
<li><span data-ttu-id="88206-120">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="88206-120">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="88206-121">システム管理者</span><span class="sxs-lookup"><span data-stu-id="88206-121">System administrator</span></span></td>
<td><span data-ttu-id="88206-122">Finance and Operations をまだ組織に配置していない場合は、「<a href="../deployment/deploy-demo-environment.md">デモ環境の配置</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88206-122">If you don't already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="88206-123">Talent をまだ組織に配置していない場合は、システム管理者は <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent の Web ページ</a> からトライアル バージョンにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="88206-123">If you don't already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="88206-124"><strong>会社のディレクトリ</strong> モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88206-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="88206-125">システム管理者</span><span class="sxs-lookup"><span data-stu-id="88206-125">System administrator</span></span></td>
<td><span data-ttu-id="88206-126">「<a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88206-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="88206-127">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="88206-127">Download and install the mobile app</span></span>
<span data-ttu-id="88206-128">Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="88206-128">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="88206-129">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="88206-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="88206-130">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="88206-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="88206-131">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="88206-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="88206-132">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="88206-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="88206-133">Microsoft Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="88206-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="88206-134">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="88206-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="88206-135">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="88206-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="88206-136">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88206-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="88206-137">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88206-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="88206-138">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="88206-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="88206-139">モバイル ワークスペースを使用して、会社のディレクトリを表示します。</span><span class="sxs-lookup"><span data-stu-id="88206-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="88206-140">モバイル アプリで、**会社のディレクトリ** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="88206-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="88206-141">従業員の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88206-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="88206-142">従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="88206-142">Select an employee.</span></span> <span data-ttu-id="88206-143">[**従業員のプロファイル**] ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88206-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="88206-144">このページの情報には、従業員の名、姓、肩書き、および部署が含まれます。</span><span class="sxs-lookup"><span data-stu-id="88206-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="88206-145">モバイル ワークスペースを使用して、会社のディレクトリを検索します。</span><span class="sxs-lookup"><span data-stu-id="88206-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="88206-146">モバイル アプリで、**会社のディレクトリ** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="88206-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="88206-147">[**検索**] フィールドに、従業員の名、姓、肩書き、または部署を入力して検索を開始します。</span><span class="sxs-lookup"><span data-stu-id="88206-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="88206-148">従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="88206-148">Select an employee.</span></span> <span data-ttu-id="88206-149">[**従業員のプロファイル**] ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88206-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="88206-150">このページの情報には、従業員の名、姓、肩書き、および部署が含まれます。</span><span class="sxs-lookup"><span data-stu-id="88206-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>

