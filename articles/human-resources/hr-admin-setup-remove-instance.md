---
title: インスタンスの削除
description: この記事では、Microsoft Dynamics 365 Human Resources のテスト ドライブ環境または実稼動環境の削除について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a8eac74f0d840251ab56445dd5af4d19d3c0490
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419407"
---
# <a name="remove-an-instance"></a><span data-ttu-id="f8791-103">インスタンスの削除</span><span class="sxs-lookup"><span data-stu-id="f8791-103">Remove an instance</span></span>

<span data-ttu-id="f8791-104">この記事では、Microsoft Dynamics 365 Human Resources のテスト ドライブ環境または実稼動環境の削除について説明します。</span><span class="sxs-lookup"><span data-stu-id="f8791-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="f8791-105">テスト ドライブ環境の削除</span><span class="sxs-lookup"><span data-stu-id="f8791-105">Remove a test drive environment</span></span>

<span data-ttu-id="f8791-106">人事管理のテスト ドライブは、60 日間の有効期限ポリシーでプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="f8791-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="f8791-107">ただし、テスト ドライブ環境の所有者には、次の手順に従って早期にトライアルを終了するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f8791-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="f8791-108">[Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8791-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="f8791-109">**環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8791-109">Select **Environments**.</span></span>
3. <span data-ttu-id="f8791-110">テスト ドライブ環境を選択します。これには、次のような命名パターンがあります: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="f8791-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="f8791-111">**削除** を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="f8791-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="f8791-112">既存のテスト ドライブ環境が削除されます。</span><span class="sxs-lookup"><span data-stu-id="f8791-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="f8791-113">削除すると、新しいテスト ドライブ環境にサイン アップが可能です。</span><span class="sxs-lookup"><span data-stu-id="f8791-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="f8791-114">実稼動環境の削除</span><span class="sxs-lookup"><span data-stu-id="f8791-114">Remove a production environment</span></span>

<span data-ttu-id="f8791-115">この記事では、人事管理をクラウド ソリューション プロバイダー (CSP) またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="f8791-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="f8791-116">ひとつの人事管理環境がひとつの Power Apps 環境内に含まれているため、2 つのオプションを考慮できます。</span><span class="sxs-lookup"><span data-stu-id="f8791-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="f8791-117">最初のオプションは、Power Apps 環境全体を削除することです。2 番目のオプションは、人事管理のみを削除することです。</span><span class="sxs-lookup"><span data-stu-id="f8791-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="f8791-118">最初のオプションは、人事管理をプロビジョニングする目的で特別に Power Apps 環境を作成し、実装を開始したばかりの場合、または既存の統合がない場合に優先されます。</span><span class="sxs-lookup"><span data-stu-id="f8791-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="f8791-119">2 つめのオプションは、Power Apps および Power Automate で活用されている豊富なデータが格納された Power Apps 環境が確立されている場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="f8791-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="f8791-120">Power Apps 環境を削除する前に、それが人事管理のスコープ外の豊富なデータ統合に使用されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="f8791-121">また、既定の Power Apps 環境を削除することはできないので注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="f8791-122">人事管理や関連付けられたアプリ、およびフローを含む Power Apps 環境全体を削除するには:</span><span class="sxs-lookup"><span data-stu-id="f8791-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="f8791-123">[Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8791-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="f8791-124">**環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8791-124">Select **Environments**.</span></span>
3. <span data-ttu-id="f8791-125">削除する環境を選択してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="f8791-126">**削除** を選択し、決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="f8791-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="f8791-127">削除が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="f8791-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="f8791-128">人事管理をサブスクライブするために使用したアカウントを使用して [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="f8791-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="f8791-129">環境を含む人事管理プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8791-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="f8791-130">LCS プロジェクトでは、**人事管理アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8791-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="f8791-131">削除するインスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8791-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="f8791-132">**インスタンスの削除** を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="f8791-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="f8791-133">既存の Power Apps 環境から人事管理環境を削除するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f8791-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="f8791-134">人事管理 DevOps チームのサポートおよび連絡を含む必要性が、LCS で直接この機能が有効になるまでの一時的なものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="f8791-135">サポートに連絡し、削除要求を開始してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="f8791-136">サポート チームは、人事管理チームの削除リクエストを開始します。</span><span class="sxs-lookup"><span data-stu-id="f8791-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="f8791-137">環境が削除されたという知らせを受けた後に続行してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="f8791-138">人事管理をサブスクライブするために使用したアカウントを使用して LCS にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="f8791-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="f8791-139">環境を含む人事管理プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8791-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="f8791-140">LCS プロジェクトでは、**人事管理アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8791-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="f8791-141">削除するインスタンスを選択します。その際、**削除済** の配置ステータスでマークされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8791-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="f8791-142">**インスタンスの削除** を選択して決定内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="f8791-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="f8791-143">論理削除された環境を復旧する</span><span class="sxs-lookup"><span data-stu-id="f8791-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="f8791-144">人事環境に接続されている Power Apps 環境を削除すると、Lifecycle Services の人事管理環境の状態が **論理削除** になります。</span><span class="sxs-lookup"><span data-stu-id="f8791-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="f8791-145">この場合、ユーザーは人事に接続することはできません。</span><span class="sxs-lookup"><span data-stu-id="f8791-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="f8791-146">環境を復元するには、次の操作を行います :</span><span class="sxs-lookup"><span data-stu-id="f8791-146">To restore the environment:</span></span>

1. <span data-ttu-id="f8791-147">[Power Apps 環境の復旧](/power-platform/admin/recover-environment.md)の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="f8791-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="f8791-148">管理者に連絡して、人事環境を復元してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="f8791-149">詳細については、[サポート](hr-admin-troubleshooting-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8791-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="f8791-150">Power Apps 環境は、削除後の 7 日間のみ保存されています。</span><span class="sxs-lookup"><span data-stu-id="f8791-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="f8791-151">この 7 日の期間内に環境を復旧する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8791-151">You must recover the environment within the seven day period.</span></span>
