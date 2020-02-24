---
title: インスタンスの削除
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009627"
---
# <a name="remove-an-instance"></a><span data-ttu-id="cbc9e-102">インスタンスの削除</span><span class="sxs-lookup"><span data-stu-id="cbc9e-102">Remove an instance</span></span>

<span data-ttu-id="cbc9e-103">この記事では、Microsoft Dynamics 365 Human Resources のテスト ドライブ環境または実稼動環境の削除について説明します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="cbc9e-104">テスト ドライブ環境の削除</span><span class="sxs-lookup"><span data-stu-id="cbc9e-104">Remove a test drive environment</span></span>

<span data-ttu-id="cbc9e-105">人事管理のテスト ドライブは、60 日間の有効期限ポリシーでプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="cbc9e-106">ただし、テスト ドライブ環境の所有者には、次の手順に従って早期にトライアルを終了するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="cbc9e-107">[Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="cbc9e-108">**環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-108">Select **Environments**.</span></span>
3. <span data-ttu-id="cbc9e-109">テスト ドライブ環境を選択します。これには、次のような命名パターンがあります: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="cbc9e-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="cbc9e-110">**削除**を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="cbc9e-111">既存のテスト ドライブ環境が削除されます。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="cbc9e-112">削除すると、新しいテスト ドライブ環境にサイン アップが可能です。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="cbc9e-113">実稼動環境の削除</span><span class="sxs-lookup"><span data-stu-id="cbc9e-113">Remove a production environment</span></span>

<span data-ttu-id="cbc9e-114">この記事では、人事管理をクラウド ソリューション プロバイダー (CSP) またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="cbc9e-115">ひとつの人事管理環境がひとつの Power Apps 環境内に含まれているため、2 つのオプションを考慮できます。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="cbc9e-116">最初のオプションは、Power Apps 環境全体を削除することです。2 番目のオプションは、人事管理のみを削除することです。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="cbc9e-117">最初のオプションは、人事管理をプロビジョニングする目的で特別に Power Apps 環境を作成し、実装を開始したばかりの場合、または既存の統合がない場合に優先されます。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="cbc9e-118">2 つめのオプションは、Power Apps および Power Automate で活用されている豊富なデータが格納された Power Apps 環境が確立されている場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="cbc9e-119">Power Apps 環境を削除する前に、それが人事管理のスコープ外の豊富なデータ統合に使用されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="cbc9e-120">また、既定の Power Apps 環境を削除することはできないので注意してください。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="cbc9e-121">人事管理や関連付けられたアプリ、およびフローを含む Power Apps 環境全体を削除するには:</span><span class="sxs-lookup"><span data-stu-id="cbc9e-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="cbc9e-122">[Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="cbc9e-123">**環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-123">Select **Environments**.</span></span>
3. <span data-ttu-id="cbc9e-124">削除する環境を選択してください。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="cbc9e-125">**削除**を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="cbc9e-126">削除が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="cbc9e-127">人事管理をサブスクライブするために使用したアカウントを使用して [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="cbc9e-128">環境を含む人事管理プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="cbc9e-129">LCS プロジェクトでは、**人事管理アプリの管理**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="cbc9e-130">削除するインスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="cbc9e-131">**インスタンスの削除**を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="cbc9e-132">既存の Power Apps 環境から人事管理環境を削除するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="cbc9e-133">人事管理 DevOps チームのサポートおよび連絡を含む必要性が、LCS で直接この機能が有効になるまでの一時的なものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="cbc9e-134">サポートに連絡し、削除要求を開始してください。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="cbc9e-135">サポート チームは、人事管理チームの削除リクエストを開始します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="cbc9e-136">環境が削除されたという知らせを受けた後に続行してください。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="cbc9e-137">人事管理をサブスクライブするために使用したアカウントを使用して LCS にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="cbc9e-138">環境を含む人事管理プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="cbc9e-139">LCS プロジェクトでは、**人事管理アプリの管理**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="cbc9e-140">削除するインスタンスを選択します。そのさい、配置ステータスが **失敗** とマークされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="cbc9e-141">**インスタンスの削除**を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="cbc9e-141">Select **Remove instance** and confirm your decision.</span></span> 
