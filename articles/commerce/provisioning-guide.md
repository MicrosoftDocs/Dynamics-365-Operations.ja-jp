---
title: Dynamics 365 Commerce 評価環境のプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニングする方法について説明します。
author: psimolin
manager: annbe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/05/2020
ms.locfileid: "4413908"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="8de9e-103">Dynamics 365 Commerce 評価環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="8de9e-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8de9e-104">このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニングする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="8de9e-105">開始する前に、このトピックにざっと目を通して、プロセスに必要な内容を把握することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8de9e-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="8de9e-106">コマースの評価環境は一般的には提供されておらず、パートナーや顧客からのリクエストに応じて付与されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="8de9e-107">ライセンスの詳細については、Microsoft パートナーにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="8de9e-108">概要</span><span class="sxs-lookup"><span data-stu-id="8de9e-108">Overview</span></span>

<span data-ttu-id="8de9e-109">Commerce 評価環境を正常にプロビジョニングするには、特定の製品名とタイプを持つプロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8de9e-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="8de9e-110">この環境と Commerce Scale Unit (CSU) には、後から E コマースをプロビジョニングする場合に使用する必要がある特定のパラメーターもいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="8de9e-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="8de9e-111">このトピックの手順では、プロビジョニングを完了するために必要なすべての手順と、使用する必要があるパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="8de9e-112">Commerce 評価環境のプロビジョニングが正常に完了した後、いくつかのプロビジョニング後の手順を完了して、使用のために準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8de9e-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="8de9e-113">一部の手順は、システムのどの側面を評価するかに応じて使用するオプションです。</span><span class="sxs-lookup"><span data-stu-id="8de9e-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="8de9e-114">オプションの手順は、後からいつでも完了できます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="8de9e-115">プロビジョニング後に Commerce 評価環境を構成する方法については、[Commerce 評価環境のコンフィギュレーション](cpe-post-provisioning.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="8de9e-116">Commerce 評価環境のオプション機能を構成する方法については、[Commerce 評価環境のオプション機能のコンフィギュレーション](cpe-optional-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8de9e-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="8de9e-117">Prerequisites</span></span>

<span data-ttu-id="8de9e-118">Commerce 評価環境をプロビジョニングする前に、次の前提条件が整っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8de9e-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="8de9e-119">あなたは評価プログラムに参加し、評価環境の能力を付与されました。</span><span class="sxs-lookup"><span data-stu-id="8de9e-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="8de9e-120">Microsoft Dynamics Lifecycle Services (LCS) ポータルへのアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="8de9e-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="8de9e-121">既存の Microsoft Dynamics 365 のパートナーまたは顧客は、Dynamics 365 Commerce プロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="8de9e-122">Microsoft Azure サブスクリプションへの管理者アクセスがあるか、必要に応じてサポートできるサブスクリプション管理者に連絡しています。</span><span class="sxs-lookup"><span data-stu-id="8de9e-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="8de9e-123">Azure Active Directory (Azure AD) テナント ID が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="8de9e-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="8de9e-124">E コマース システムの管理者グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="8de9e-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="8de9e-125">評価とレビューのモデレーター グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="8de9e-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="8de9e-126">(このセキュリティ グループは、E コマースのシステム管理グループと同じにすることができます。)</span><span class="sxs-lookup"><span data-stu-id="8de9e-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="8de9e-127">このリストは包括的なものではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="8de9e-128">問題が発生した場合は、Microsoft パートナーの連絡先に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="8de9e-129">Commerce 評価環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="8de9e-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="8de9e-130">これらの手順は、Commerce 評価環境をプロビジョニングする方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="8de9e-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="8de9e-131">それらを正常に完了すると、Commerce 評価環境を構成する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="8de9e-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="8de9e-132">ここで説明するすべての活動は、LCS ポータルで発生します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="8de9e-133">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="8de9e-133">Create a new project</span></span>

<span data-ttu-id="8de9e-134">LCS に新しいプロジェクトを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="8de9e-135">LCS のホーム ページで、プラス記号 (**+**) を選択してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="8de9e-136">右側のウィンドウで、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="8de9e-137">パートナーである場合、**移行、ソリューションの作成、および学習** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="8de9e-138">顧客の場合、**見込みプリセールス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="8de9e-139">名前と説明、および業種を入力します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="8de9e-140">**製品名** フィールドで、**Dynamics 365 Commerce** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="8de9e-141">**製品バージョン** フィールドで、**Dynamics 365 Commerce** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="8de9e-142">**方法** フィールドで、**Dynamics Retail の実装方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="8de9e-143">オプション: ロールとユーザーを既存のプロジェクトからインポートできます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="8de9e-144">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-144">Select **Create**.</span></span> <span data-ttu-id="8de9e-145">プロジェクト ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="8de9e-146">Azure コネクタの追加</span><span class="sxs-lookup"><span data-stu-id="8de9e-146">Add the Azure Connector</span></span>

<span data-ttu-id="8de9e-147">Azure コネクタ を LCS プロジェクトに追加するには、[Azure Resource Manager (ARM) 研修プロセス](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="8de9e-148">環境の配置</span><span class="sxs-lookup"><span data-stu-id="8de9e-148">Deploy the environment</span></span>

<span data-ttu-id="8de9e-149">環境を配置するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9e-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="8de9e-150">オプションが 1 つしかないページはスキップされるため、手順 6、7、または 8 を完了する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8de9e-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="8de9e-151">**環境パラメーター** ビューで、**Dynamics 365 Commerce - デモ (10.0.* x* プラットフォーム更新プログラム *xx*)\*\* が **環境名** フィールドのすぐ上に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="8de9e-152">詳細については、手順 8 の後に表示されているイラストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="8de9e-153">トップ メニューで、**クラウド ホスト環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="8de9e-154">環境を追加するために **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="8de9e-155">**アプリケーション バージョン** フィールドで、最新のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="8de9e-156">最新バージョン以外のアプリケーション バージョンを特定する必要がある場合は、**10.0.14** より前のバージョンを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="8de9e-157">**プラットフォーム バージョン** フィールドで、選択したアプリケーション バージョンに対して自動的に選択されたプラットフォーム バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![アプリケーションとプラットフォーム バージョンを選択する](./media/project1.png)

1. <span data-ttu-id="8de9e-159">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-159">Select **Next**.</span></span>
1. <span data-ttu-id="8de9e-160">環境のトポロジとして **デモ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-160">Select **Demo** as the environment topology.</span></span>

    ![環境トポロジ 1 を選択する](./media/project2.png)

1. <span data-ttu-id="8de9e-162">**環境の配置** のページで、環境名を入力します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="8de9e-163">詳細設定はそのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-163">Leave the advanced settings as they are.</span></span>

    ![環境の配置のページ](./media/project4.png)

1. <span data-ttu-id="8de9e-165">VM サイズを必要に応じて調整します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-165">Adjust the VM size as required.</span></span> <span data-ttu-id="8de9e-166">(VM 最小在庫管理単位をお勧めします \[SKU\] **D13 v2**。)</span><span class="sxs-lookup"><span data-stu-id="8de9e-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="8de9e-167">価格決定およびライセンス条件を確認、チェック ボックスをオンにして同意したことを示します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="8de9e-168">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-168">Select **Next**.</span></span>
1. <span data-ttu-id="8de9e-169">配置の確認ページで、詳細が正しいことを確認した後、**配置** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="8de9e-170">**クラウド ホスト環境** ビューに戻り、環境がリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="8de9e-171">要求した環境はキューに格納され、その後配置されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="8de9e-172">環境ワークフローは完了までに少し時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="8de9e-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="8de9e-173">そのため、約 6 ~ 9 時間後に再度確認してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="8de9e-174">続行する前に、環境の状態が **配置済み** になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="8de9e-175">Commerce Scale Unit (CSU) を初期化する (クラウド)</span><span class="sxs-lookup"><span data-stu-id="8de9e-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="8de9e-176">CSU を初期化するためには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9e-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="8de9e-177">**クラウド ホスト環境** ビュー内で、リストから環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="8de9e-178">右側の環境ビューで、**完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="8de9e-179">環境の詳細のビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-179">The environment details view appears.</span></span>
1. <span data-ttu-id="8de9e-180">**環境機能** の下で、**管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="8de9e-181">**コマース** タブで、**初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="8de9e-182">CSU 初期化パラメーター ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="8de9e-183">**地域** フィールドで、環境を配置したのと同じか、またはそれに近い地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="8de9e-184">**バージョン** フィールドはそのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="8de9e-185">**初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="8de9e-186">配置の確認ページで、詳細が正しいことを確認した後、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="8de9e-187">**コマース** タブが選択されているところでは、**コマースの管理** ビューが再度表示されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="8de9e-188">CSU がプロビジョニング用にキューに格納されました。</span><span class="sxs-lookup"><span data-stu-id="8de9e-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="8de9e-189">続行する前に、CSU の状態が **成功** となっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="8de9e-190">初期化には約 2 ~ 5 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="8de9e-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="8de9e-191">環境の詳細ビューに **管理** リンクが見つからない場合は 、Microsoft の連絡先に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="8de9e-192">E コマースの初期化</span><span class="sxs-lookup"><span data-stu-id="8de9e-192">Initialize e-Commerce</span></span>

<span data-ttu-id="8de9e-193">E コマースを初期化するためには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9e-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8de9e-194">**E コマース** タブで、評価の同意を確認し、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="8de9e-195">**E コマース環境名** フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="8de9e-196">この名前は E コマース インスタンスを指す URL の一部に表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="8de9e-197">**Commerce Scale Unit の名前** フィールドで、リストから CSU を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="8de9e-198">(リストには 1 つのオプションのみが必要です。)</span><span class="sxs-lookup"><span data-stu-id="8de9e-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="8de9e-199">**E コマースの地域** フィールドは自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="8de9e-200">**次へ** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="8de9e-201">**サポートされているホスト名** フィールドに、`www.fabrikam.com` などの有効なドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="8de9e-202">**システム管理者の AAD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力し、虫眼鏡記号を選択して検索結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="8de9e-203">リストで正しいセキュリティ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="8de9e-204">**評価とレビュー モデレーター用 AAD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力し、虫眼鏡記号を選択して検索結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="8de9e-205">リストで正しいセキュリティ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="8de9e-206">**評価とレビュー サービスを有効にする** オプションを、**はい** のままにします。</span><span class="sxs-lookup"><span data-stu-id="8de9e-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="8de9e-207">**初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9e-207">Select **Initialize**.</span></span> <span data-ttu-id="8de9e-208">**E コマース** タブが選択されているところでは、**コマースの管理** ビューが再度表示されます。</span><span class="sxs-lookup"><span data-stu-id="8de9e-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="8de9e-209">E コマースの初期化を開始しました。</span><span class="sxs-lookup"><span data-stu-id="8de9e-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="8de9e-210">続行する前に、E コマースの初期化状態が **初期化成功** になるまでお待ちください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="8de9e-211">右下の **リンク** で、次のリンクの URL をメモします。</span><span class="sxs-lookup"><span data-stu-id="8de9e-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="8de9e-212">**E コマース サイト** – E コマース サイトのルートへのリンク。</span><span class="sxs-lookup"><span data-stu-id="8de9e-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="8de9e-213">**Commerce サイト ビルダー** – サイト管理ツールへのリンク。</span><span class="sxs-lookup"><span data-stu-id="8de9e-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8de9e-214">次のステップ</span><span class="sxs-lookup"><span data-stu-id="8de9e-214">Next steps</span></span>

<span data-ttu-id="8de9e-215">Commerce 評価環境のプロビジョニングと構成のプロセスを続行するには、[Commerce 評価環境のコンフィギュレーション](cpe-post-provisioning.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8de9e-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8de9e-216">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8de9e-216">Additional resources</span></span>

[<span data-ttu-id="8de9e-217">Dynamics 365 Commerce 評価環境の概要</span><span class="sxs-lookup"><span data-stu-id="8de9e-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8de9e-218">Dynamics 365 Commerce の評価環境を構成する</span><span class="sxs-lookup"><span data-stu-id="8de9e-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="8de9e-219">Dynamics 365 Commerce 評価環境で BOPIS を構成する</span><span class="sxs-lookup"><span data-stu-id="8de9e-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="8de9e-220">Dynamics 365 Commerce 評価環境のオプション機能を構成する</span><span class="sxs-lookup"><span data-stu-id="8de9e-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="8de9e-221">Dynamics 365 Commerce 評価環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="8de9e-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="8de9e-222">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8de9e-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="8de9e-223">Commerce Scale Unit (クラウド)</span><span class="sxs-lookup"><span data-stu-id="8de9e-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="8de9e-224">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="8de9e-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="8de9e-225">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="8de9e-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
