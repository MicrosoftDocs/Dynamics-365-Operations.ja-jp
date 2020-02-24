---
title: 会社のディレクトリ モバイル ワークスペース
description: このトピックでは、ユーザーが閲覧し、組織内の他の従業員と連絡が取れるようにする、会社のディレクトリ モバイル ワークスペースに関する情報を提供します。
author: jcart1106
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 445a2872dcd0e4d3aca9a50c7539fdabb0ed7818
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005589"
---
# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="c4943-103">会社のディレクトリ モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="c4943-103">Company directory mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4943-104">このトピックでは、**会社のディレクトリ** モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4943-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="c4943-105">このワークスペースで、ユーザーは閲覧して組織内の他の従業員と連絡を取ることができます。</span><span class="sxs-lookup"><span data-stu-id="c4943-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="c4943-106">このモバイル ワークスペースは、Finance and Operations モバイル アプリと一緒に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4943-106">This mobile workspace can be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="c4943-107">概要</span><span class="sxs-lookup"><span data-stu-id="c4943-107">Overview</span></span>
<span data-ttu-id="c4943-108">**会社のディレクトリ** モバイル ワークスペースにより、ユーザーは次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="c4943-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="c4943-109">組織内の従業員の一覧を表示する。</span><span class="sxs-lookup"><span data-stu-id="c4943-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="c4943-110">組織内の従業員を検索する。</span><span class="sxs-lookup"><span data-stu-id="c4943-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="c4943-111">従業員の連絡先情報を表示する。</span><span class="sxs-lookup"><span data-stu-id="c4943-111">View contact information for employees.</span></span>
- <span data-ttu-id="c4943-112">プロファイル情報から従業員に連絡する。</span><span class="sxs-lookup"><span data-stu-id="c4943-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c4943-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="c4943-113">Prerequisites</span></span>
<span data-ttu-id="c4943-114">このモバイル ワークスペースを使用するには、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4943-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4943-115">前提条件</span><span class="sxs-lookup"><span data-stu-id="c4943-115">Prerequisite</span></span></th>
<th><span data-ttu-id="c4943-116">役割</span><span class="sxs-lookup"><span data-stu-id="c4943-116">Role</span></span></th>
<th><span data-ttu-id="c4943-117">説明</span><span class="sxs-lookup"><span data-stu-id="c4943-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4943-118">次の製品のいずれかを組織内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4943-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="c4943-119">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="c4943-119">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="c4943-120">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="c4943-120">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="c4943-121">システム管理者</span><span class="sxs-lookup"><span data-stu-id="c4943-121">System administrator</span></span></td>
<td><span data-ttu-id="c4943-122">組織にまだ Finance and Operations アプリが配置されていない場合は、<a href="../deployment/deploy-demo-environment.md">デモ環境の配置</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4943-122">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="c4943-123">組織にまだ人事管理が配置されていない場合、システム管理者は<a href="https://dynamics.microsoft.com/human-resources/overview/">人事管理ウェブページ</a>から評価版バージョンにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c4943-123">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4943-124"><strong>会社のディレクトリ</strong> モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4943-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="c4943-125">システム管理者</span><span class="sxs-lookup"><span data-stu-id="c4943-125">System administrator</span></span></td>
<td><span data-ttu-id="c4943-126">「<a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4943-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="c4943-127">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="c4943-127">Download and install the mobile app</span></span>
<span data-ttu-id="c4943-128">Finance and Operations モバイル アプリのダウンロードとインストール。</span><span class="sxs-lookup"><span data-stu-id="c4943-128">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="c4943-129">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="c4943-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="c4943-130">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="c4943-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="c4943-131">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="c4943-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="c4943-132">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="c4943-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="c4943-133">Microsoft Dynamics 365 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4943-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="c4943-134">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="c4943-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="c4943-135">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4943-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="c4943-136">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4943-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="c4943-137">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4943-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="c4943-138">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="c4943-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="c4943-139">モバイル ワークスペースを使用して、会社のディレクトリを表示します。</span><span class="sxs-lookup"><span data-stu-id="c4943-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="c4943-140">モバイル アプリで、**会社のディレクトリ** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4943-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="c4943-141">従業員の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4943-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="c4943-142">従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4943-142">Select an employee.</span></span> <span data-ttu-id="c4943-143">**従業員のプロファイル**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4943-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="c4943-144">このページの情報には、従業員の名、姓、肩書き、および部署が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4943-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="c4943-145">モバイル ワークスペースを使用して、会社のディレクトリを検索します。</span><span class="sxs-lookup"><span data-stu-id="c4943-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="c4943-146">モバイル アプリで、**会社のディレクトリ** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4943-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="c4943-147">**検索**フィールドに、従業員の名、姓、肩書き、または部署を入力して検索を開始します。</span><span class="sxs-lookup"><span data-stu-id="c4943-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="c4943-148">従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4943-148">Select an employee.</span></span> <span data-ttu-id="c4943-149">**従業員のプロファイル**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4943-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="c4943-150">このページの情報には、従業員の名、姓、肩書き、および部署が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4943-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
