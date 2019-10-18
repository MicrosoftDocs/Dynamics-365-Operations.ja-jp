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
ms.openlocfilehash: d608ee3ad90d23279557e5e9be4d398ffac3a266
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010618"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="aa653-103">Talent 環境の削除</span><span class="sxs-lookup"><span data-stu-id="aa653-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aa653-104">このトピックでは、Microsoft Dynamics 365 Talent のテスト ドライブ環境または実稼動環境の削除について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa653-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="aa653-105">テスト ドライブ環境の削除</span><span class="sxs-lookup"><span data-stu-id="aa653-105">Removing a test drive environment</span></span>

<span data-ttu-id="aa653-106">Talent テスト ドライブは、60 日間の有効期限ポリシーでプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="aa653-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="aa653-107">ただし、テスト ドライブ環境の所有者には、次の手順に従って早期にトライアルを終了するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="aa653-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="aa653-108">[PowerApps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="aa653-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="aa653-109">**環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa653-109">Select **Environments**.</span></span>
3. <span data-ttu-id="aa653-110">テスト ドライブ環境を選択します。これには、次のような命名パターンがあります: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="aa653-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="aa653-111">**削除**を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="aa653-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="aa653-112">既存のテスト ドライブ環境が削除されます。</span><span class="sxs-lookup"><span data-stu-id="aa653-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="aa653-113">削除すると、新しいテスト ドライブ環境にサイン アップが可能です。</span><span class="sxs-lookup"><span data-stu-id="aa653-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="aa653-114">実稼動環境の削除</span><span class="sxs-lookup"><span data-stu-id="aa653-114">Removing a production environment</span></span>

<span data-ttu-id="aa653-115">このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="aa653-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="aa653-116">ひとつの Talent 環境がひとつの PowerApps 環境内に「含まれている」ため、2 つのオプションを考慮できます。</span><span class="sxs-lookup"><span data-stu-id="aa653-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="aa653-117">最初のオプションは、PowerApps 環境全体を削除することです。2 番目のオプションは、Talent のみを削除することです。</span><span class="sxs-lookup"><span data-stu-id="aa653-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="aa653-118">最初のオプションは、Talent をプロビジョニングする目的で特別に PowerApps 環境を作成し、実装を開始したばかりの場合、または既存の統合がない場合に優先されます。</span><span class="sxs-lookup"><span data-stu-id="aa653-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="aa653-119">2 つめのオプションは、PowerApps およびフローで活用されている豊富なデータが格納された PowerApps 環境が確立されている場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="aa653-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="aa653-120">PowerApps 環境を削除する前に、それが Talent のスコープ外の豊富なデータ統合に使用されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="aa653-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="aa653-121">また、既定の PowerApps 環境を削除することはできないので注意してください。</span><span class="sxs-lookup"><span data-stu-id="aa653-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="aa653-122">Talent や関連付けられたアプリ、およびフローを含む PowerApps 環境全体を削除するには:</span><span class="sxs-lookup"><span data-stu-id="aa653-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="aa653-123">[PowerApps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="aa653-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="aa653-124">**環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa653-124">Select **Environments**.</span></span>
3. <span data-ttu-id="aa653-125">削除する環境を選択してください。</span><span class="sxs-lookup"><span data-stu-id="aa653-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="aa653-126">**削除**を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="aa653-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="aa653-127">削除が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="aa653-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="aa653-128">Talent をサブスクライブするために使用したアカウントを使用して [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="aa653-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="aa653-129">環境を含む Talent プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa653-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="aa653-130">LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa653-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="aa653-131">削除するインスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa653-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="aa653-132">**インスタンスの削除**を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="aa653-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="aa653-133">既存の PowerApps 環境から Talent 環境を削除するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="aa653-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="aa653-134">Talent DevOps チームのサポートおよび連絡を含む必要性が、LCS で直接この機能が有効になるまでの一時的なものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="aa653-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="aa653-135">サポートに連絡し、削除要求を開始してください。</span><span class="sxs-lookup"><span data-stu-id="aa653-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="aa653-136">サポート チームはTalent DevOps チームの削除リクエストを開始します。</span><span class="sxs-lookup"><span data-stu-id="aa653-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="aa653-137">環境が削除されたという知らせを受けた後に続行してください。</span><span class="sxs-lookup"><span data-stu-id="aa653-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="aa653-138">Talent をサブスクライブするために使用したアカウントを使用して LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="aa653-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="aa653-139">環境を含む Talent プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa653-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="aa653-140">LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa653-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="aa653-141">削除するインスタンスを選択します。そのさい、配置ステータスが **失敗** とマークされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa653-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="aa653-142">**インスタンスの削除**を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="aa653-142">Select **Remove instance** and confirm your decision.</span></span> 

