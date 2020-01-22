---
title: Talent 環境の削除
description: このトピックでは、Microsoft Dynamics 365 Talent のテスト ドライブ環境または実稼動環境の削除について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e752d658388fc6cb6f4b84ac83cb12a71522199b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898113"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="80fea-103">Talent 環境の削除</span><span class="sxs-lookup"><span data-stu-id="80fea-103">Remove Talent environments</span></span>

<span data-ttu-id="80fea-104">このトピックでは、Microsoft Dynamics 365 Talent のテスト ドライブ環境または実稼動環境の削除について説明します。</span><span class="sxs-lookup"><span data-stu-id="80fea-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="80fea-105">テスト ドライブ環境の削除</span><span class="sxs-lookup"><span data-stu-id="80fea-105">Removing a test drive environment</span></span>

<span data-ttu-id="80fea-106">Talent テスト ドライブは、60 日間の有効期限ポリシーでプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="80fea-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="80fea-107">ただし、テスト ドライブ環境の所有者には、次の手順に従って早期にトライアルを終了するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="80fea-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="80fea-108">[Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="80fea-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="80fea-109">**環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="80fea-109">Select **Environments**.</span></span>
3. <span data-ttu-id="80fea-110">テスト ドライブ環境を選択します。これには、次のような命名パターンがあります: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="80fea-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="80fea-111">**削除**を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="80fea-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="80fea-112">既存のテスト ドライブ環境が削除されます。</span><span class="sxs-lookup"><span data-stu-id="80fea-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="80fea-113">削除すると、新しいテスト ドライブ環境にサイン アップが可能です。</span><span class="sxs-lookup"><span data-stu-id="80fea-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="80fea-114">実稼動環境の削除</span><span class="sxs-lookup"><span data-stu-id="80fea-114">Removing a production environment</span></span>

<span data-ttu-id="80fea-115">このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="80fea-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="80fea-116">ひとつの Talent 環境がひとつの Power Apps 環境内に「含まれている」ため、2 つのオプションを考慮できます。</span><span class="sxs-lookup"><span data-stu-id="80fea-116">Since a single Talent environment is “contained” within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="80fea-117">最初のオプションは、Power Apps 環境全体を削除することです。2 番目のオプションは、Talent のみを削除することです。</span><span class="sxs-lookup"><span data-stu-id="80fea-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="80fea-118">最初のオプションは、Talent をプロビジョニングする目的で特別に Power Apps 環境を作成し、実装を開始したばかりの場合、または既存の統合がない場合に優先されます。</span><span class="sxs-lookup"><span data-stu-id="80fea-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="80fea-119">2 つめのオプションは、Power Apps および Power Automate で活用されている豊富なデータが格納された Power Apps 環境が確立されている場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="80fea-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="80fea-120">Power Apps 環境を削除する前に、それが Talent のスコープ外の豊富なデータ統合に使用されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="80fea-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="80fea-121">また、既定の Power Apps 環境を削除することはできないので注意してください。</span><span class="sxs-lookup"><span data-stu-id="80fea-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="80fea-122">Talent や関連付けられたアプリ、およびフローを含む Power Apps 環境全体を削除するには:</span><span class="sxs-lookup"><span data-stu-id="80fea-122">To remove the entire Power Apps environment, including Talent and the associated apps and flows:</span></span>

1. <span data-ttu-id="80fea-123">[Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="80fea-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="80fea-124">**環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="80fea-124">Select **Environments**.</span></span>
3. <span data-ttu-id="80fea-125">削除する環境を選択してください。</span><span class="sxs-lookup"><span data-stu-id="80fea-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="80fea-126">**削除**を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="80fea-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="80fea-127">削除が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="80fea-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="80fea-128">Talent をサブスクライブするために使用したアカウントを使用して [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="80fea-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="80fea-129">環境を含む Talent プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="80fea-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="80fea-130">LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="80fea-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="80fea-131">削除するインスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="80fea-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="80fea-132">**インスタンスの削除**を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="80fea-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="80fea-133">既存の Power Apps 環境から Talent 環境を削除するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="80fea-133">To remove a Talent environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="80fea-134">Talent DevOps チームのサポートおよび連絡を含む必要性が、LCS で直接この機能が有効になるまでの一時的なものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="80fea-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="80fea-135">サポートに連絡し、削除要求を開始してください。</span><span class="sxs-lookup"><span data-stu-id="80fea-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="80fea-136">サポート チームはTalent DevOps チームの削除リクエストを開始します。</span><span class="sxs-lookup"><span data-stu-id="80fea-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="80fea-137">環境が削除されたという知らせを受けた後に続行してください。</span><span class="sxs-lookup"><span data-stu-id="80fea-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="80fea-138">Talent をサブスクライブするために使用したアカウントを使用して LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="80fea-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="80fea-139">環境を含む Talent プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="80fea-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="80fea-140">LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="80fea-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="80fea-141">削除するインスタンスを選択します。そのさい、配置ステータスが **失敗** とマークされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="80fea-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="80fea-142">**インスタンスの削除**を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="80fea-142">Select **Remove instance** and confirm your decision.</span></span> 

