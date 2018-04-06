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
ms.sourcegitcommit: ba1a3a78d59f3aec91473ba9bb20bda4804ec92e
ms.openlocfilehash: 0a43f5ff0987ede9f0cb80e5b4854f78e19e329b
ms.contentlocale: ja-jp
ms.lasthandoff: 03/23/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="c667e-103">Microsoft Dynamics 365 for Talent のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="c667e-103">Provision Microsoft Dynamics 365 for Talent</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="c667e-104">このトピックでは、Microsoft Dynamics 365 for Talent の新しい実稼働環境のプロビジョニングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c667e-104">This topic walks you through the process of provisioning a new production environment for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="c667e-105">このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="c667e-105">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="c667e-106">Talent サービス プランがすでに含まれている Microsoft Dynamics 365 ライセンスがあり、このトピックの手順を完了できない場合は、サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="c667e-106">If you have an existing Microsoft Dynamics 365 license that already includes the Talent service plan, and you can't complete the steps in this topic, contact Support.</span></span>

<span data-ttu-id="c667e-107">始めに、グローバル管理者は [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) にサインインし、新しい Talent プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c667e-107">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) and create a new Talent project.</span></span> <span data-ttu-id="c667e-108">ライセンスの問題で Talent プロビジョニングが妨げられない限り、サポートまたは Dynamics サービス エンジニアリング チーム (DSE) の担当者に問い合わせる必要はありません</span><span class="sxs-lookup"><span data-stu-id="c667e-108">Unless a licensing issue prevents you from provisioning Talent, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="c667e-109">LCS プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="c667e-109">Create an LCS project</span></span>
<span data-ttu-id="c667e-110">Talent 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c667e-110">To use LCS to manage your Talent environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="c667e-111">Talent をサブスクライブするために使用したアカウントを使用して [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="c667e-111">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Talent.</span></span>
2. <span data-ttu-id="c667e-112">プラス記号 (**+**) を選択してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c667e-112">Select the plus sign (**+**) to create a project.</span></span>
3. <span data-ttu-id="c667e-113">製品名、製品バージョンとして **Microsoft Dynamics 365 for Talent** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c667e-113">Select **Microsoft Dynamics 365 for Talent** as the product name and product version.</span></span>
4. <span data-ttu-id="c667e-114">**Dynamics 365 for Talent** の方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="c667e-114">Select the **Dynamics 365 for Talent** methodology.</span></span>
5. <span data-ttu-id="c667e-115">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c667e-115">Select **Create**.</span></span>

<span data-ttu-id="c667e-116">Talent を使い始める方法については、新しいプロジェクトで作成した **Talent** の方法を参照してくだい。</span><span class="sxs-lookup"><span data-stu-id="c667e-116">For information about how to get started with Talent, see the **Talent** methodology that you created in your new project.</span></span> <span data-ttu-id="c667e-117">プロジェクトの作成が終了したら、Talent 環境を設定するために次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="c667e-117">After you've finished creating the project, complete the following procedure to provision your Talent environment.</span></span>

## <a name="provision-a-talent-project"></a><span data-ttu-id="c667e-118">Talent プロジェクトのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="c667e-118">Provision a Talent project</span></span>
<span data-ttu-id="c667e-119">LCS プロジェクトを作成した後は、環境に Talent をプロビジョニングすることができます。</span><span class="sxs-lookup"><span data-stu-id="c667e-119">After you've created an LCS project, you can provision Talent into an environment.</span></span>

1. <span data-ttu-id="c667e-120">LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c667e-120">In your LCS project, select the **Talent App Management** tile.</span></span>
2. <span data-ttu-id="c667e-121">Talent は PowerApps の統合および拡張機能を有効にするために Microsoft PowerApps の環境に常にプロビジョニングされています。</span><span class="sxs-lookup"><span data-stu-id="c667e-121">Talent is always provisioned into a Microsoft PowerApps environment, to enable PowerApps integration and extensibility.</span></span> <span data-ttu-id="c667e-122">続行する前に、このトピックの「PowerApps 環境の選択」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c667e-122">Read the “Selecting a PowerApps environment” section of this topic before you continue.</span></span> 
3. <span data-ttu-id="c667e-123">すでに PowerApps 環境を持っていない場合、続行する前にこのトピックの「新しい PowerApps 環境の作成 (必要な場合)」セクションにある手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="c667e-123">If you don't already have a PowerApps environment, follow the steps in the "Create a new PowerApps environment (if required)" section of this topic before you continue.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c667e-124">既存の環境を表示、または新しい環境を作成するために、Talent をプロビジョニングするテナント管理者は PowerApps P2 ライセンスに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c667e-124">To view existing environments or create new environments, the tenant admin who provisions Talent must be assigned to the PowerApps P2 license.</span></span> <span data-ttu-id="c667e-125">組織に PowerApps P2 ライセンスがない場合、CSP または [PowerApps 価格ページ](https://powerapps.microsoft.com/en-us/pricing/) から入手することができます。</span><span class="sxs-lookup"><span data-stu-id="c667e-125">If your organization doesn't have a PowerApps P2 license, you can get one from your CSP or from the [PowerApps pricing page](https://powerapps.microsoft.com/en-us/pricing/).</span></span>

4. <span data-ttu-id="c667e-126">**追加**を選択し、Talent をプロビジョニングする環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="c667e-126">Select **Add**, and then select the environment to provision Talent into.</span></span>
5. <span data-ttu-id="c667e-127">使用条件に同意、および展開を開始するために **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c667e-127">Select **Yes** to agree to the terms and begin deployment.</span></span>

    <span data-ttu-id="c667e-128">新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c667e-128">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="c667e-129">ただし、配置状態が**配置済み**に更新されるまでは、環境の使用を開始できません。</span><span class="sxs-lookup"><span data-stu-id="c667e-129">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="c667e-130">このプロセスには通常、数分間かかります</span><span class="sxs-lookup"><span data-stu-id="c667e-130">This process typically takes just a few minutes.</span></span> <span data-ttu-id="c667e-131">プロビジョニング プロセスに失敗する場合は、サポートに連絡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c667e-131">If the provisioning process is unsuccessful, you must contact Support.</span></span>

6. <span data-ttu-id="c667e-132">新しい環境を使用するために **Talent にログオンします** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c667e-132">Select **Log on to Talent** to use your new environment.</span></span>

> [!NOTE]
> <span data-ttu-id="c667e-133">最終要件をまだサインオフしていない場合、プロジェクトに Talent のテスト インスタンスを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="c667e-133">If you haven't yet signed off on the final requirements, you can deploy a test instance of Talent in the project.</span></span> <span data-ttu-id="c667e-134">サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c667e-134">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="c667e-135">テストのために新しい環境を使用する場合は、実稼動環境を作成するためにこの手順を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c667e-135">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="c667e-136">Talent 環境は、人事管理 (HR) タスクにコンフィギュレーションされる、または Talent に指定されるデモ データを含まない LCS によってプロビジョニングされています。</span><span class="sxs-lookup"><span data-stu-id="c667e-136">Talent environments that are provisioned through LCS don't contain demo data that is configured for Human resources (HR) tasks, or that is specific to Talent.</span></span> <span data-ttu-id="c667e-137">デモ データを含む環境が必要な場合、60 日間無料 [Talent 試用環境](https://dynamics.microsoft.com/en-us/talent/overview/)に登録することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c667e-137">If you require an environment that contains demo data, we recommend that you sign up for a free 60-day [Talent trial environment](https://dynamics.microsoft.com/en-us/talent/overview/).</span></span> <span data-ttu-id="c667e-138">試用環境は要求したユーザーにより所有されていますが、Core HR のシステム管理経験を通じて他のユーザーも招待できます。</span><span class="sxs-lookup"><span data-stu-id="c667e-138">Although a trial environment is owned by the user who requested it, other users can be invited through the system administration experience for Core HR.</span></span> <span data-ttu-id="c667e-139">試用環境には、安全にプログラムを活用するために使用する架空のデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c667e-139">Trial environments contain fictitious data that can be used to explore the program in a safe manner.</span></span> <span data-ttu-id="c667e-140">これらは実稼動環境として使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="c667e-140">They aren't intended to be used as production environments.</span></span> <span data-ttu-id="c667e-141">試用環境が 60 日後に期限が切れると、その中にあるすべてのデータが削除され復元できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c667e-141">Note that when the trial environment expires after 60 days, all the data in it is deleted and can't be recovered.</span></span> <span data-ttu-id="c667e-142">既存の環境の期限が切れた後、新しい試用環境に登録することができます。</span><span class="sxs-lookup"><span data-stu-id="c667e-142">You can sign up for a new trial environment after the existing environment expires.</span></span>

## <a name="select-a-powerapps-environment"></a><span data-ttu-id="c667e-143">PowerApps 環境の選択</span><span class="sxs-lookup"><span data-stu-id="c667e-143">Select a PowerApps environment</span></span>

<span data-ttu-id="c667e-144">Talent と PowerApps 環境との統合では、PowerApps ツールを使用して Talent データの使用を統合および拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="c667e-144">The integration between Talent and the PowerApps environments lets you integrate and extend the use of Talent data using PowerApps tools.</span></span> <span data-ttu-id="c667e-145">PowerApps 環境の目的を理解することで、Talent を拡張するためのアプリを構築するために役立つだけでなく、Talent プロビジョニングするときに正しい環境を選択するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c667e-145">Understanding the purpose of PowerApps environments will not only help you build apps to extend Talent, but also can also help you select the correct environment when provisioning Talent.</span></span> <span data-ttu-id="c667e-146">環境スコープ、環境アクセス、および環境の作成および選択を含む、PowerApps 環境の詳細については、[ PowerApps 環境の発表](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="c667e-146">For information about PowerApps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing PowerApps environments](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).</span></span> 

<span data-ttu-id="c667e-147">Talent を配置する PowerApps 環境を決定する際には、次のガイダンスを参考にしてください。</span><span class="sxs-lookup"><span data-stu-id="c667e-147">Use the following guidance when determining which PowerApps environment to deploy Talent into:</span></span> 
1. <span data-ttu-id="c667e-148">LCS で管理の環境を選択するか、または PowerApps 管理者センターに直接移動して、既存の環境を表示および新しい環境を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c667e-148">In LCS, select Manage environments, or navigate directly to the PowerApps Admin center , where you can view existing environments and create new environments.</span></span>
2. <span data-ttu-id="c667e-149">1 つの Talent 環境は、1 つの PowerApps 環境にマップされます。</span><span class="sxs-lookup"><span data-stu-id="c667e-149">A single Talent environment is mapped to a single PowerApps environment.</span></span>
3. <span data-ttu-id="c667e-150">PowerApps 環境には、対応する PowerApps、フロー、および CDS アプリケーションと共に、Talent アプリケーションが「含まれて」います。</span><span class="sxs-lookup"><span data-stu-id="c667e-150">A PowerApps environment “contains” the Talent application, along with the corresponding PowerApps, Flow, and CDS applications.</span></span> <span data-ttu-id="c667e-151">PowerApps 環境を削除すると、その中のアプリも削除されます。</span><span class="sxs-lookup"><span data-stu-id="c667e-151">If the PowerApps environment is deleted, so are the apps within it.</span></span>
4. <span data-ttu-id="c667e-152">データの統合およびテスト戦略を考慮する必要があります。たとえばサンドボックス、UAT、生産などです。</span><span class="sxs-lookup"><span data-stu-id="c667e-152">Data integration and testing strategies should be considered, for example: Sandbox, UAT, Production.</span></span> <span data-ttu-id="c667e-153">したがって、後に PowerApps 環境にマッピングされる Talent 環境を変更することは容易ではないため、配置へのさまざまな影響について考慮することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c667e-153">Therefore, we recommend that you consider the various implications for your deployment, because it isn't easy to change which Talent environment is mapped to a PowerApps environment later.</span></span>
5. <span data-ttu-id="c667e-154">次の PowerApps 環境は Talent に対しては使用できず、LCS 内の選択リストからもフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="c667e-154">The following PowerApps environments cannot be used for Talent and will be filtered from the selection list within LCS:</span></span>
 
    <span data-ttu-id="c667e-155">**CDS 2.0 環境** CDS 2.0 は、2018 年 3 月 21 日に公開されますが、Talent は、まだ CDS 2.0 をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c667e-155">**CDS 2.0 Environments** CDS 2.0 will be made publicly available on March 21, 2018; however, Talent does not yet support CDS 2.0.</span></span> <span data-ttu-id="c667e-156">PowerApps 管理センターで CDS 2.0 データベースを表示および作成することはできますが、Talent では使用可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="c667e-156">Though you can view and create CDS 2.0 databases in the PowerApps Admin center, they will not be usable in Talent.</span></span> <span data-ttu-id="c667e-157">Talent 配置で CDS 2.0 環境を使用するオプションは後日利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="c667e-157">The option to use CDS 2.0 Environments in Talent deployments will be available at a later date.</span></span>
   
 > [!Note]
 > <span data-ttu-id="c667e-158">管理ポータルで CDS 1.0 と 2.0 の環境を区別するためには、環境を選択し、[詳細] を確認してください。</span><span class="sxs-lookup"><span data-stu-id="c667e-158">To differentiate between CDS 1.0 and 2.0 environments in the administration portal, select an environment and look at the **Details**.</span></span> <span data-ttu-id="c667e-159">CDS 2.0 環境はすべて、「Dynamics 365 管理センターでこれらの設定を管理することができます」という情報を参照します。インスタンス バージョンを参照し、[データベース] タブはありません。</span><span class="sxs-lookup"><span data-stu-id="c667e-159">CDS 2.0 environments all reference the fact that "You can manage these settings in the Dynamics 365 Administration Center," point to an instance version, and have no Database tab.</span></span> 
 
   <span data-ttu-id="c667e-160">**既定の PowerApps 環境** 各テナントは、既定の PowerApps 環境で自動的にプロビジョニングされますが、すべてのテナント ユーザーは PowerApps 環境にアクセスすることができ、PowerApps または Flow 統合を使用してテストや調査を行う際に意図せずに生産データが壊れる可能性があるため、Talent でそれらを使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="c667e-160">**Default Power Apps environments** Although each tenant is automatically provisioned with a default PowerApps environment, we don't recommend using them with Talent since all tenant users have access to the PowerApps environment and may unintentionally corrupt production data when testing and exploring with PowerApps or Flow integrations.</span></span>
   
   <span data-ttu-id="c667e-161">**テスト ドライブ環境** 「TestDrive – alias@domain」のような名前の環境は、60 日間の有効期限で作成され、その期間が経過すると有効期限切れになり、環境が自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="c667e-161">**Test Drive environments** Environments with a name like ‘TestDrive – alias@domain’ are created with a 60-day expiration period and will expire after that time, causing your environment to be removed automatically.</span></span>
   
   <span data-ttu-id="c667e-162">**サポートされていない地域** 現在の Talent は、次の地域でのみサポートされます: 米国、ヨーロッパ、またはオーストラリア。</span><span class="sxs-lookup"><span data-stu-id="c667e-162">**Unsupported regions** Currently Talent is only supported in the following regions: United States, Europe, or Australia.</span></span>
  
6. <span data-ttu-id="c667e-163">使用する正しい環境を決定した後、実行する特定のアクションはありません</span><span class="sxs-lookup"><span data-stu-id="c667e-163">There is no specific action to take once you have determined the correct environment to use.</span></span> <span data-ttu-id="c667e-164">プロビジョニング プロセスを続行します。</span><span class="sxs-lookup"><span data-stu-id="c667e-164">Continue with the provisioning process.</span></span> 
 
## <a name="create-a-new-powerapps-environment-if-required"></a><span data-ttu-id="c667e-165">新しい PowerApps 環境の作成 (必要な場合)</span><span class="sxs-lookup"><span data-stu-id="c667e-165">Create a new PowerApps environment (if required)</span></span>

<span data-ttu-id="c667e-166">PowerApps プラン 2 のライセンスを持つテナント管理者のコンテキストで、PowerShell スクリプトを実行し、Talent 用に新しい PowerApps 環境の作成を行います。</span><span class="sxs-lookup"><span data-stu-id="c667e-166">Run a PowerShell script to create a new PowerApps environment for Talent in the context of the tenant admin that has the PowerApps Plan 2 license.</span></span> <span data-ttu-id="c667e-167">スクリプトは、次の手順を自動化します。</span><span class="sxs-lookup"><span data-stu-id="c667e-167">The script automates the following steps:</span></span>


 + <span data-ttu-id="c667e-168">PowerApps 環境の作成</span><span class="sxs-lookup"><span data-stu-id="c667e-168">Creation of a PowerApps environment</span></span>
 + <span data-ttu-id="c667e-169">CD 1.0 データベースの作成</span><span class="sxs-lookup"><span data-stu-id="c667e-169">Creation of a CDS 1.0 database</span></span>
 + <span data-ttu-id="c667e-170">CD 1.0 データベース内のすべてのサンプル データをクリア</span><span class="sxs-lookup"><span data-stu-id="c667e-170">Clear all sample data in the CDS 1.0 database</span></span>


<span data-ttu-id="c667e-171">次の手順を完了させて、スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="c667e-171">Complete the following instructions to run the script:</span></span>

1. <span data-ttu-id="c667e-172">次の場所から ProvisionCDSEnvironment.zip ファイルをダウンロードします。[ProvisionCDSEnvironment スクリプト](https://go.microsoft.com/fwlink/?linkid=870436)</span><span class="sxs-lookup"><span data-stu-id="c667e-172">Download the ProvisionCDSEnvironment.zip file from the following location: [ProvisionCDSEnvironment scripts](https://go.microsoft.com/fwlink/?linkid=870436)</span></span>  

2. <span data-ttu-id="c667e-173">ProvisionCDSEnviroinment.zip ファイルの内容全体をフォルダに解凍します。</span><span class="sxs-lookup"><span data-stu-id="c667e-173">Unzip the entire contents of the ProvisionCDSEnviroinment.zip file into a folder.</span></span>

3. <span data-ttu-id="c667e-174">Windows PowerShell または Windows PowerShell ISE プログラムを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="c667e-174">Run the Windows PowerShell or Windows PowerShell ISE program as the administrator.</span></span>

   <span data-ttu-id="c667e-175">スクリプトを実行するための実行ポリシーの設定の詳細については、トピック [実行ポリシーの設定](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="c667e-175">Visit the [Set Execution Policy](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) topic to learn more about setting the execution policy so that scripts can be run.</span></span>
  
4. <span data-ttu-id="c667e-176">PowerShell 内で、ファイルを解凍したフォルダに移動し、以下のコマンドを実行して、次の値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c667e-176">Within PowerShell, navigate to the folder where you unzipped the file and run the following command, replacing values as directed below:</span></span>
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   <span data-ttu-id="c667e-177">**EnvironmentName** は、環境名に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="c667e-177">**EnvironmentName** should be replaced with your environment name.</span></span> <span data-ttu-id="c667e-178">この名前は LCS に表示され、ユーザーが使用する Talent 環境を選択すると表示されます。</span><span class="sxs-lookup"><span data-stu-id="c667e-178">This name will appear in LCS and will be visible when users select which Talent environment to use.</span></span> 

   <span data-ttu-id="c667e-179">**YourLocation** は、Talent がサポートされている地域の 1 つに置き換えてください: 米国、ヨーロッパ、オーストラリア。</span><span class="sxs-lookup"><span data-stu-id="c667e-179">**YourLocation** should be replaced with one of the supported regions for Talent: unitedsates, europe, australia.</span></span> 

   <span data-ttu-id="c667e-180">[-詳細] はオプションであり、問題が発生した場合にサポートに送信する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c667e-180">**-Verbose** is optional and will provide detailed information to send to support if problems are encountered.</span></span>

5. <span data-ttu-id="c667e-181">プロビジョニング プロセスを続行します。</span><span class="sxs-lookup"><span data-stu-id="c667e-181">Continue with the provisioning process.</span></span>
 


## <a name="grant-access-to-the-environment"></a><span data-ttu-id="c667e-182">環境へのアクセスを付与</span><span class="sxs-lookup"><span data-stu-id="c667e-182">Grant access to the environment</span></span>
<span data-ttu-id="c667e-183">既定では、環境を作成したグローバル管理者がそこにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c667e-183">By default, the global administrator who created the environment has access to it.</span></span> <span data-ttu-id="c667e-184">ただし、追加のアプリケーション ユーザーは、明示的にアクセスを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c667e-184">However, additional application users must be explicitly granted access.</span></span> <span data-ttu-id="c667e-185">アクセスを許可するには、Core HR 環境で [ユーザーの追加](../dev-itpro/sysadmin/tasks/create-new-users.md) および [適切なロールを割り当て](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md)ます。</span><span class="sxs-lookup"><span data-stu-id="c667e-185">To grant access, you [add users](../dev-itpro/sysadmin/tasks/create-new-users.md) and [assign the appropriate roles to them](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) in the Core HR environment.</span></span> <span data-ttu-id="c667e-186">Attract および Onboard アプリケーションへアクセスできるよう、それらのユーザーを PowerApps 環境に追加する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="c667e-186">You must also add those users to the PowerApps environment, so that they can access the Attract and Onboard applications.</span></span> <span data-ttu-id="c667e-187">手順をここで説明します。</span><span class="sxs-lookup"><span data-stu-id="c667e-187">The procedure is outlined here.</span></span> <span data-ttu-id="c667e-188">手順を完了するのに助けが必要な場合は、[PowerApps 管理センターの導入](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) ブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c667e-188">If you require help to complete the steps, see the [Introducing the PowerApps admin center](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) blog post.</span></span>

<span data-ttu-id="c667e-189">Talent 環境を展開したグローバル管理者によって、この手順が完了します。</span><span class="sxs-lookup"><span data-stu-id="c667e-189">This procedure is completed by the global administrator who deployed the Talent environment.</span></span>

1. <span data-ttu-id="c667e-190">[PowerApps 管理センター](https://preview.admin.powerapps.com/environments)を開きます。</span><span class="sxs-lookup"><span data-stu-id="c667e-190">Open the [PowerApps Admin center](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="c667e-191">該当する環境をオンにします。</span><span class="sxs-lookup"><span data-stu-id="c667e-191">Select the appropriate environments.</span></span>
3. <span data-ttu-id="c667e-192">[セキュリティ] タブで、必要なユーザーを [環境メーカー] ロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="c667e-192">On the **Security** tab, add the required users to the **Environment Maker** role.</span></span>

    <span data-ttu-id="c667e-193">PowerApps 環境にユーザーを手動で追加するこの最後のステップは、一時的であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c667e-193">Note that this final step, where you manually add users to the PowerApps environment, is temporary.</span></span> <span data-ttu-id="c667e-194">最終的には、ユーザーが Core HR に追加される際に、自動的に完了します。</span><span class="sxs-lookup"><span data-stu-id="c667e-194">Eventually, it will be completed automatically when users are added in Core HR.</span></span>

