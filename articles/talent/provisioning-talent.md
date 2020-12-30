---
title: Talent のプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 Talent の新しい環境のプロビジョニングについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
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
ms.openlocfilehash: 5bcdb50475fb341a538211cb122eb7c13067d86a
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527221"
---
# <a name="provision-talent"></a><span data-ttu-id="70cb4-103">Talent のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="70cb4-103">Provision Talent</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="70cb4-104">このトピックでは、Microsoft Dynamics 365 Talent の新しい実稼動環境のプロビジョニングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-104">This topic walks you through the process of provisioning a new production environment for Microsoft Dynamics 365 Talent.</span></span> <span data-ttu-id="70cb4-105">このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="70cb4-105">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="70cb4-106">Talent サービス プランがすでに含まれている Microsoft Dynamics 365 ライセンスがあり、このトピックの手順を完了できない場合は、サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-106">If you have an existing Microsoft Dynamics 365 license that already includes the Talent service plan, and you can't complete the steps in this topic, contact Support.</span></span>

<span data-ttu-id="70cb4-107">始めに、グローバル管理者は [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) にサインインし、新しい Talent プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-107">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) and create a new Talent project.</span></span> <span data-ttu-id="70cb4-108">ライセンスの問題で Talent プロビジョニングが妨げられない限り、サポートまたは Dynamics サービス エンジニアリング チーム (DSE) の担当者に問い合わせる必要はありません</span><span class="sxs-lookup"><span data-stu-id="70cb4-108">Unless a licensing issue prevents you from provisioning Talent, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="70cb4-109">LCS プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="70cb4-109">Create an LCS project</span></span>
<span data-ttu-id="70cb4-110">Talent 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-110">To use LCS to manage your Talent environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="70cb4-111">Talent をサブスクライブするために使用したアカウントを使用して [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="70cb4-111">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Talent.</span></span>

2. <span data-ttu-id="70cb4-112">プラス記号 (**+**) を選択してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-112">Select the plus sign (**+**) to create a project.</span></span>

3. <span data-ttu-id="70cb4-113">製品名、製品バージョンとして **Microsoft Dynamics 365 Talent** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-113">Select **Microsoft Dynamics 365 Talent** as the product name and product version.</span></span>

4. <span data-ttu-id="70cb4-114">**Dynamics 365 Talent** 方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-114">Select the **Dynamics 365 Talent** methodology.</span></span>

5. <span data-ttu-id="70cb4-115">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-115">Select **Create**.</span></span> 

<span data-ttu-id="70cb4-116">Talent を使い始める方法については、新しいプロジェクトで作成した **Talent** の方法を参照してくだい。</span><span class="sxs-lookup"><span data-stu-id="70cb4-116">For information about how to get started with Talent, see the **Talent** methodology that you created in your new project.</span></span> <span data-ttu-id="70cb4-117">プロジェクトの作成が終了したら、Talent 環境を設定するために次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-117">After you've finished creating the project, complete the following procedure to provision your Talent environment.</span></span>

## <a name="provision-a-talent-project"></a><span data-ttu-id="70cb4-118">Talent プロジェクトのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="70cb4-118">Provision a Talent project</span></span>

<span data-ttu-id="70cb4-119">LCS プロジェクトを作成した後は、環境に Talent をプロビジョニングすることができます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-119">After you've created an LCS project, you can provision Talent into an environment.</span></span>

1. <span data-ttu-id="70cb4-120">LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-120">In your LCS project, select the **Talent App Management** tile.</span></span>

2. <span data-ttu-id="70cb4-121">これが人材のサンドボックスまたは実稼働インスタンスであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-121">Indicate whether this is a Sandbox or Production instance of Talent.</span></span> <span data-ttu-id="70cb4-122">初期のプレビュー機能をサンドボックス インスタンスで使用することにより、早期のフィードバックおよびテストを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-122">Early preview features may be available in Sandbox instances to allow for early feedback and testing.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="70cb4-123">Talent インスタンス タイプは、一度設定した後に変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="70cb4-123">The Talent instance type cannot be changed once set.</span></span> <span data-ttu-id="70cb4-124">続行する前に、正しいインスタンス タイプが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-124">Verify the correct instance type is selected before continuing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="70cb4-125">Talent のインスタンス タイプは、Power Apps 管理センターで設定された Microsoft Power Apps 環境のインスタンス タイプとは異なります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-125">The Talent instance type is separate from the instance type of the Microsoft Power Apps environment, which you set in the Power Apps Admin center.</span></span>

3. <span data-ttu-id="70cb4-126">Talent テスト ドライブ エクスペリエンスで使用される同じデモ データのセットを環境に含める場合は、**デモ データを含む** オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="70cb4-126">Select the **Include Demo Data** option if you want your environment to include the same demo data set used in the Talent Test Drive experience.</span></span> <span data-ttu-id="70cb4-127">これは長期的なデモまたはトレーニング環境に便利であり、稼動環境で使用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="70cb4-127">This is beneficial for long-term demo or training environments, and should never be used for production environments.</span></span>  <span data-ttu-id="70cb4-128">初期展開時にこのオプションを選択する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-128">Note that you must choose this option upon initial deployment.</span></span> <span data-ttu-id="70cb4-129">後で、既存の配置を更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="70cb4-129">You cannot update an existing deployment later.</span></span>

4. <span data-ttu-id="70cb4-130">Talent は、Microsoft Power Apps の環境に常にプロビジョニングされていて、これにより Power Apps の統合および拡張機能が有効になります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-130">Talent is always provisioned into a Microsoft Power Apps environment to enable Power Apps integration and extensibility.</span></span> <span data-ttu-id="70cb4-131">続行する前に、このトピックの「Power Apps 環境の選択」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-131">Read the “Selecting a Power Apps environment” section of this topic before you continue.</span></span> <span data-ttu-id="70cb4-132">まだ Power Apps 環境を持っていない場合は、LCS で環境の管理を選択するか、または Power Apps 管理センターに移動します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-132">If you don't already have a Power Apps environment, select Manage environments in LCS or navigate to the Power Apps Admin center.</span></span> <span data-ttu-id="70cb4-133">次に、以下の手順に従って、[Power Apps 環境を作成します](https://docs.microsoft.com/powerapps/administrator/create-environment)。</span><span class="sxs-lookup"><span data-stu-id="70cb4-133">Then follow the steps to [Create a Power Apps environment](https://docs.microsoft.com/powerapps/administrator/create-environment).</span></span>

5. <span data-ttu-id="70cb4-134">人材を供給する環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-134">Select the environment to provision Talent into.</span></span>

6. <span data-ttu-id="70cb4-135">使用条件に同意、および展開を開始するために **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-135">Select **Yes** to agree to the terms and begin deployment.</span></span>

    <span data-ttu-id="70cb4-136">新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-136">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="70cb4-137">ただし、配置状態が **配置済み** に更新されるまでは、環境の使用を開始できません。</span><span class="sxs-lookup"><span data-stu-id="70cb4-137">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="70cb4-138">このプロセスには通常、数分間かかります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-138">This process typically takes a few minutes.</span></span> <span data-ttu-id="70cb4-139">プロビジョニング プロセスに失敗する場合は、サポートに連絡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-139">If the provisioning process is unsuccessful, you must contact Support.</span></span>

7. <span data-ttu-id="70cb4-140">新しい環境を使用するために **Talent にログオンします** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-140">Select **Log on to Talent** to use your new environment.</span></span>

    > [!NOTE]
    > <span data-ttu-id="70cb4-141">最終要件をまだサインオフしていない場合、プロジェクトに Talent のテスト インスタンスを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-141">If you haven't yet signed off on the final requirements, you can deploy a test instance of Talent in the project.</span></span> <span data-ttu-id="70cb4-142">サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-142">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="70cb4-143">テストのために新しい環境を使用する場合は、実稼動環境を作成するためにこの手順を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-143">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

    > <span data-ttu-id="70cb4-144">Talent 定期売買の一部として 2 つの LCS 環境のみが許可されるため、60 日間無料 [Talent 試用環境](https://dynamics.microsoft.com/talent/overview/) の活用を考慮するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="70cb4-144">Because only two LCS environments are allowed as part of the Talent subscription, you might consider leveraging a free 60-day [Talent trial environment](https://dynamics.microsoft.com/talent/overview/).</span></span> <span data-ttu-id="70cb4-145">試用環境は要求したユーザーにより所有されていますが、人事管理のシステム管理経験を通じて他のユーザーも招待できます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-145">Although a trial environment is owned by the user who requested it, other users can be invited through the system administration experience for Human Resources.</span></span> <span data-ttu-id="70cb4-146">試用環境には、安全にプログラムを活用するために使用する架空のデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-146">Trial environments contain fictitious data that can be used to explore the program in a safe manner.</span></span> <span data-ttu-id="70cb4-147">これらは実稼動環境として使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="70cb4-147">They aren't intended to be used as production environments.</span></span> <span data-ttu-id="70cb4-148">試用環境が 60 日後に期限が切れると、その中にあるすべてのデータが削除され復元できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-148">Note that when a trial environment expires after 60 days, all the data that's in it is deleted and can't be recovered.</span></span> <span data-ttu-id="70cb4-149">既存の環境の期限が切れた後、新しい試用環境に登録することができます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-149">You can sign up for a new trial environment after the existing environment expires.</span></span>

## <a name="select-a-power-apps-environment"></a><span data-ttu-id="70cb4-150">Power Apps 環境の選択</span><span class="sxs-lookup"><span data-stu-id="70cb4-150">Select a Power Apps environment</span></span>

<span data-ttu-id="70cb4-151">Talent と Power Apps 環境との統合では、Power Apps ツールを使用して Talent データの使用を統合および拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-151">The integration between Talent and the Power Apps environments lets you integrate and extend the use of Talent data using Power Apps tools.</span></span> <span data-ttu-id="70cb4-152">Power Apps 環境の目的を理解することで、Talent を拡張するためのアプリを構築するために役立つだけでなく、Talent プロビジョニングするときに正しい環境を選択するのにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-152">Understanding the purpose of Power Apps environments will not only help you build apps to extend Talent, but will also help you select the correct environment when provisioning Talent.</span></span> <span data-ttu-id="70cb4-153">環境スコープ、環境アクセス、および環境の作成および選択を含む、Power Apps 環境の詳細については、[Power Apps 環境の発表](https://powerapps.microsoft.com/blog/powerapps-environments/) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-153">For information about Power Apps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing Power Apps environments](https://powerapps.microsoft.com/blog/powerapps-environments/).</span></span> 

<span data-ttu-id="70cb4-154">Talent を配置する Power Apps 環境を決定する際には、次のガイダンスを参考にしてください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-154">Use the following guidance when determining which Power Apps environment to deploy Talent into:</span></span> 

1. <span data-ttu-id="70cb4-155">LCS で **環境の管理** を選択するか、または Power Apps 管理者センターに直接移動して、既存の環境を表示および新しい環境を作成できます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-155">In LCS, select **Manage environments**, or go directly to the Power Apps Admin center where you can view existing environments and create new environments.</span></span>

2. <span data-ttu-id="70cb4-156">1 つの Talent 環境は、1 つの Power Apps 環境にマップされます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-156">A single Talent environment is mapped to a single Power Apps environment.</span></span>

3. <span data-ttu-id="70cb4-157">Power Apps 環境には、対応する Power Apps、Power Automate、および Common Data Service アプリケーションと共に、Talent アプリケーションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="70cb4-157">A Power Apps environment contains Talent, along with the corresponding Power Apps, Power Automate, and Common Data Service applications.</span></span> <span data-ttu-id="70cb4-158">Power Apps 環境を削除すると、その中のアプリも削除されます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-158">If the Power Apps environment is deleted, so are the apps within it.</span></span> <span data-ttu-id="70cb4-159">Talent 環境をプロビジョニングする場合、**試用版** または **製品版** 環境のいずれかをプロビジョニングできます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-159">When provisioning a Talent environment, you can provision either a **Trial** or **Production** environment.</span></span> <span data-ttu-id="70cb4-160">環境の使用方法に基づいて環境のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-160">Choose the type of environment based on how the environment will be used.</span></span> 

4. <span data-ttu-id="70cb4-161">サンドボックス、UAT、または生産などのデータの統合およびテスト戦略を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-161">Data integration and testing strategies should be considered, such as Sandbox, UAT, or Production.</span></span> <span data-ttu-id="70cb4-162">Power Apps 環境にマッピングされている Talent 環境を後になって変更することは容易ではないため、配置へのさまざまな影響について考慮することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="70cb4-162">We recommend that you consider the various implications for your deployment, because it isn't easy to later change which Talent environment is mapped to a Power Apps environment.</span></span>

5. <span data-ttu-id="70cb4-163">次の Power Apps 環境は Talent に対しては使用できず、LCS 内の選択リストからもフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-163">The following Power Apps environments cannot be used for Talent and will be filtered from the selection list within LCS:</span></span>
 
    - <span data-ttu-id="70cb4-164">**既定の Power Apps 環境** - 各テナントは、既定の Power Apps 環境で自動的にプロビジョニングされますが、すべてのテナント ユーザーは Power Apps 環境にアクセスすることができ、Power Apps または Power Automate 統合を使用してテストや調査を行う際に意図せずに生産データが壊れる可能性があるため、Talent でそれらを使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="70cb4-164">**Default Power Apps environments** - Although each tenant is automatically provisioned with a default Power Apps environment, we don't recommend using them with Talent because all tenant users have access to the Power Apps environment and could unintentionally corrupt production data when testing and exploring with Power Apps or Power Automate integrations.</span></span>
   
    - <span data-ttu-id="70cb4-165">**試用環境** - これらの環境は有効期限付きで作成され、その期間が経過すると有効期限切れになり、環境およびその中に含まれるすべての Talent インスタンスは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-165">**Trial environments** - These environments are created with an expiration date and will expire after that time, causing your environment and any Talent instances contained within to be removed automatically.</span></span>
   
    - <span data-ttu-id="70cb4-166">**サポートされていない地域** - 現在の Talent は、次の地域でのみサポートされます: 米国、ヨーロッパ、英国、オーストラリア、カナダおよびアジア。</span><span class="sxs-lookup"><span data-stu-id="70cb4-166">**Unsupported regions** - Currently Talent is only supported in the following regions: United States, Europe, United Kingdom, Australia, Canada and Asia.</span></span>
  
6. <span data-ttu-id="70cb4-167">使用する正しい環境を決定した後、プロビジョニング プロセスを続行できます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-167">After you have determined the correct environment to use, you can continue with the provisioning process.</span></span> 
 
## <a name="grant-access-to-the-environment"></a><span data-ttu-id="70cb4-168">環境へのアクセスを付与</span><span class="sxs-lookup"><span data-stu-id="70cb4-168">Grant access to the environment</span></span>

<span data-ttu-id="70cb4-169">既定では、環境を作成したグローバル管理者がそこにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="70cb4-169">By default, the global administrator who created the environment has access to it.</span></span> <span data-ttu-id="70cb4-170">ただし、追加のアプリケーション ユーザーは、明示的にアクセスを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-170">However, additional application users must be explicitly granted access.</span></span> <span data-ttu-id="70cb4-171">アクセスを許可するには、人事管理環境でユーザーを追加し適切なロールを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-171">To grant access, you need to add users and assign the appropriate roles to them in the Human Resources environment.</span></span> <span data-ttu-id="70cb4-172">Talent を展開するグローバル管理者は、初期化を完了して、他のテナント ユーザーのアクセスを有効にするため、Attract および Onboard の両方も起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70cb4-172">The global administrator that deployed Talent must also launch both Attract and Onboard to complete the initialization and enable access for other tenant users.</span></span>  <span data-ttu-id="70cb4-173">これが発生するまで、他のユーザーは Attract および Onboard にアクセスすることはできませんし、アクセス違反エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="70cb4-173">Until this happens, other users will not be able to access Attract and Onboard and will get access violation errors.</span></span> <span data-ttu-id="70cb4-174">詳細については、[新規ユーザーの作成](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) および [ユーザーのセキュリティ ロールへの割り当て](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70cb4-174">For more information, see [Create new users](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) and [Assign users to security roles](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).</span></span> 
