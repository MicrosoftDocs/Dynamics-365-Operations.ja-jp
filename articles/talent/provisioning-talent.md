---
title: "Microsoft Dynamics 365 for Talent のプロビジョニング"
description: "このトピックでは、Microsoft Dynamics 365 for Talent の新しい環境のプロビジョニングについて説明します。"
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: d8516091ea4427f59e01e02f06b0010628c1a8ed
ms.contentlocale: ja-jp
ms.lasthandoff: 01/19/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="7bde7-103">Microsoft Dynamics 365 for Talent のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="7bde7-103">Provision Microsoft Dynamics 365 for Talent</span></span>
<span data-ttu-id="7bde7-104">このトピックでは、Microsoft Dynamics 365 for Talent の新しい環境のプロビジョニングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-104">This topic walks you through the process of provisioning a new environment for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="7bde7-105">このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="7bde7-105">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="7bde7-106">Talent サービス プランがすでに含まれている Microsoft Dynamics 365 ライセンスがあり、このトピックの手順を完了できない場合は、サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="7bde7-106">If you have an existing Microsoft Dynamics 365 license that already includes the Talent service plan, and you can't complete the steps in this topic, contact Support.</span></span>

<span data-ttu-id="7bde7-107">始めに、グローバル管理者は [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) にサインインし、新しい Talent プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-107">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) and create a new Talent project.</span></span> <span data-ttu-id="7bde7-108">ライセンスの問題で Talent プロビジョニングが妨げられない限り、サポートまたは Dynamics サービス エンジニアリング チーム (DSE) の担当者に問い合わせる必要はありません</span><span class="sxs-lookup"><span data-stu-id="7bde7-108">Unless a licensing issue prevents you from provisioning Talent, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="7bde7-109">LCS プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="7bde7-109">Create an LCS project</span></span>
<span data-ttu-id="7bde7-110">Talent 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bde7-110">To use LCS to manage your Talent environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="7bde7-111">Talent をサブスクライブするために使用したアカウントを使用して [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7bde7-111">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Talent.</span></span>
2. <span data-ttu-id="7bde7-112">プラス記号 (**+**) を選択してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-112">Select the plus sign (**+**) to create a project.</span></span>
3. <span data-ttu-id="7bde7-113">製品名、製品バージョンとして **Microsoft Dynamics 365 for Talent** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-113">Select **Microsoft Dynamics 365 for Talent** as the product name and product version.</span></span>
4. <span data-ttu-id="7bde7-114">**Dynamics 365 for Talent** の方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-114">Select the **Dynamics 365 for Talent** methodology.</span></span>
5. <span data-ttu-id="7bde7-115">[作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-115">Select **Create**.</span></span>

<span data-ttu-id="7bde7-116">Talent を使い始める方法については、新しいプロジェクトで作成した **Talent** の方法を参照してくだい。</span><span class="sxs-lookup"><span data-stu-id="7bde7-116">For information about how to get started with Talent, see the **Talent** methodology that you created in your new project.</span></span> <span data-ttu-id="7bde7-117">プロジェクトの作成が終了したら、Talent 環境を設定するために次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="7bde7-117">After you've finished creating the project, complete the following procedure to provision your Talent environment.</span></span>

## <a name="provision-a-talent-project"></a><span data-ttu-id="7bde7-118">Talent プロジェクトのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="7bde7-118">Provision a Talent project</span></span>
<span data-ttu-id="7bde7-119">LCS プロジェクトを作成した後は、環境に Talent をプロビジョニングすることができます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-119">After you've created an LCS project, you can provision Talent into an environment.</span></span>

1. <span data-ttu-id="7bde7-120">LCS プロジェクトでは、[Talent アプリの管理] タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-120">In your LCS project, select the **Talent App Management** tile.</span></span>
2. <span data-ttu-id="7bde7-121">Talent は PowerApps の統合および拡張機能を有効にするために Microsoft PowerApps の環境に常にプロビジョニングされています。</span><span class="sxs-lookup"><span data-stu-id="7bde7-121">Talent is always provisioned into a Microsoft PowerApps environment, to enable PowerApps integration and extensibility.</span></span> <span data-ttu-id="7bde7-122">すでに PowerApps 環境を持っていない場合、続行する前にこのトピックの「新しい PowerApps 環境の作成 (必要な場合)」セクションにある手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="7bde7-122">If you don't already have a PowerApps environment, follow the steps in the "Create a new PowerApps environment (if required)" section of this topic before you continue.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bde7-123">既存の環境を表示、または新しい環境を作成するために、Talent をプロビジョニングするテナント管理者は PowerApps P2 ライセンスに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bde7-123">To view existing environments or create new environments, the tenant admin who provisions Talent must be assigned to the PowerApps P2 license.</span></span> <span data-ttu-id="7bde7-124">組織に PowerApps P2 ライセンスがない場合、CSP または [PowerApps 価格ページ](https://powerapps.microsoft.com/en-us/pricing/) から入手することができます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-124">If your organization doesn't have a PowerApps P2 license, you can get one from your CSP or from the [PowerApps pricing page](https://powerapps.microsoft.com/en-us/pricing/).</span></span>

3. <span data-ttu-id="7bde7-125">**追加**を選択し、Talent をプロビジョニングする環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-125">Select **Add**, and then select the environment to provision Talent into.</span></span>
4. <span data-ttu-id="7bde7-126">使用条件に同意、および展開を開始するために [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-126">Select **Yes** to agree to the terms and begin deployment.</span></span>

    <span data-ttu-id="7bde7-127">新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-127">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="7bde7-128">ただし、配置状態が**配置済み**に更新されるまでは、環境の使用を開始できません。</span><span class="sxs-lookup"><span data-stu-id="7bde7-128">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="7bde7-129">このプロセスには通常、数分間かかります</span><span class="sxs-lookup"><span data-stu-id="7bde7-129">This process typically takes just a few minutes.</span></span> <span data-ttu-id="7bde7-130">プロビジョニングに失敗する場合、サポートに連絡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bde7-130">If provisioning fails, you must contact Support.</span></span>

6. <span data-ttu-id="7bde7-131">新しい環境を使用するために [Talent にログオンします] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-131">Select **Log on to Talent** to use your new environment.</span></span>

> [!NOTE]
> <span data-ttu-id="7bde7-132">最終要件をまだサインオフしていない場合、プロジェクトに Talent のテスト インスタンスを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-132">If you haven't yet signed off on the final requirements, you can deploy a test instance of Talent in the project.</span></span> <span data-ttu-id="7bde7-133">サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-133">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="7bde7-134">テストのために新しい環境を使用する場合は、実稼動環境を作成するためにこの手順を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bde7-134">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

## <a name="create-a-new-powerapps-environment-if-required"></a><span data-ttu-id="7bde7-135">新しい PowerApps 環境の作成 (必要な場合)</span><span class="sxs-lookup"><span data-stu-id="7bde7-135">Create a new PowerApps environment (if required)</span></span>
1. <span data-ttu-id="7bde7-136">LCS の [環境の管理] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-136">Select **Manage Environments** in LCS.</span></span> <span data-ttu-id="7bde7-137">既存の環境の表示および新しい環境の作成ができる [PowerApps 管理者センター](https://preview.admin.powerapps.com/environments) に移動します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-137">You're taken to the [PowerApps Admin Center](https://preview.admin.powerapps.com/environments), where you can view existing environments and create new environments.</span></span>
2. <span data-ttu-id="7bde7-138">(**+**) [新しい環境] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-138">Select the (**+**) **New environment** button.</span></span>
3. <span data-ttu-id="7bde7-139">環境の一意の名前を入力し、配置する場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-139">Enter a unique name for the environment, and select the location to deploy to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bde7-140">Talent はすべての地域で利用できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="7bde7-140">Talent isn't available in all regions.</span></span> <span data-ttu-id="7bde7-141">したがって、環境の場所を選択する前に使用可能かを必ず確認してください。</span><span class="sxs-lookup"><span data-stu-id="7bde7-141">Therefore, be sure to check for availability before you select the location for your environment.</span></span>

4. <span data-ttu-id="7bde7-142">データベースを作成するかどうかを尋ねられた場合、[データベースの作成] を選択し、Talent データの一部をホストする Common Data Service (CDS) データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-142">When you're asked whether you want to create a database, select **Create database** to create the Common Data Service (CDS) database that must host part of your Talent data.</span></span> <span data-ttu-id="7bde7-143">データベースを作成し、PowerApps アプリケーションと Talent を統合することもできます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-143">By creating a database, you can also integrate PowerApps applications with Talent.</span></span>
5. <span data-ttu-id="7bde7-144">データベースに使用するアクセス レベルについて尋ねられます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-144">You're asked about the access level that you want to use for the database.</span></span> <span data-ttu-id="7bde7-145">Talent ユーザーが PowerApps アプリケーションを使用して機密データに直接アクセスすることを防止するために、[アクセスの制限] を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7bde7-145">We recommend that you select **Restrict access**, because this option prevents Talent users from directly accessing sensitive data by using a PowerApps application.</span></span>
6. <span data-ttu-id="7bde7-146">作成される CDS データベースにはデモ データが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-146">The CDS database that is created contains demo data.</span></span> <span data-ttu-id="7bde7-147">このデモ データは、デモ データの会社を使用してテストを行う、またはタスク記録およびタスク ガイドを作成する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-147">This demo data is useful, because you can use the demo data company for testing, or to create task recordings or task guides.</span></span> <span data-ttu-id="7bde7-148">ただし、デモ データは、他の情報の中でも、無効な従業員や架空の住所を運用環境に追加します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-148">However, the demo data adds inactive employees and fictitious addresses, among other information, to your production environment.</span></span> <span data-ttu-id="7bde7-149">デモ データを削除するには、CDS の作成が終了した後にこれらの手順に従います:</span><span class="sxs-lookup"><span data-stu-id="7bde7-149">To remove the demo data, follow these steps after you've finished creating the CDS database:</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7bde7-150">以前に CDS データベースを作成し、会社の生産データを入力した場合、これらの手順で選択したデータベース内の **すべて** のデータが (会社の実動データであっても) 削除されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7bde7-150">If you previously created a CDS database and entered any of your company's production data into it, be aware that these steps remove **all** the data in the selected database, even your company's production data.</span></span>

    1. <span data-ttu-id="7bde7-151">[PowerApps](https://preview.web.powerapps.com/home) にサインインし、手順 2 で作成した環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-151">Sign in to [PowerApps](https://preview.web.powerapps.com/home), and go to the environment that you created in step 2.</span></span>
    2. <span data-ttu-id="7bde7-152">[エンティティ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-152">Select **Entities**.</span></span> <span data-ttu-id="7bde7-153">ページの右側にある省略記号ボタン (**…**) を選択し、[すべてのデータをクリア] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-153">On the right side of the page, select the ellipse (**…**) button, and then select **Clear all data**.</span></span>
    3. <span data-ttu-id="7bde7-154">[データを削除] を選択し、データを削除することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-154">Select **Delete data** to confirm that you want to remove the data.</span></span> <span data-ttu-id="7bde7-155">このアクションは、既定で CDS に含まれているすべてのデモ データを削除します。</span><span class="sxs-lookup"><span data-stu-id="7bde7-155">This action removes all the demo data that is included in the CDS by default.</span></span> <span data-ttu-id="7bde7-156">選択したデータベースに入力されている他のデータも削除されます。</span><span class="sxs-lookup"><span data-stu-id="7bde7-156">It also removes any other data that has been entered in the selected database.</span></span>

<span data-ttu-id="7bde7-157">新しい環境を使用することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7bde7-157">You can now use your new environment.</span></span>

