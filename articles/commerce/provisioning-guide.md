---
title: Dynamics 365 Commerce プレビュー環境のプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境をプロビジョニングする方法について説明します。
author: psimolin
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024639"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="f4ca2-103">Dynamics 365 Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="f4ca2-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f4ca2-104">このトピックでは、Dynamics 365 Commerce のプレビュー環境をプロビジョニングする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="f4ca2-105">開始する前に、このトピックにざっと目を通して、プロセスに必要な内容を把握することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="f4ca2-106">Dynamics 365 Commerce プレビューへのアクセス許可がまだ与えられていない場合、[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite) からプレビューのアクセス許可を要求できます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="f4ca2-107">概要</span><span class="sxs-lookup"><span data-stu-id="f4ca2-107">Overview</span></span>

<span data-ttu-id="f4ca2-108">Commerce プレビュー環境を正常にプロビジョニングするには、特定の製品名とタイプを持つプロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="f4ca2-109">Commerce scale unit (CSU) には、後で E コマースをプロビジョニングするために使用する必要がある特定のパラメーターもあります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-109">The environment and commerce scale unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="f4ca2-110">このトピックの手順では、プロビジョニングを完了する必要があるすべての手順と、使用する必要があるパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="f4ca2-111">Commerce プレビュー環境のプロビジョニングが正常に完了した後、いくつかのプロビジョニング後の手順を完了して準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="f4ca2-112">一部の手順は、システムのどの側面を評価するかに応じて使用するオプションです。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="f4ca2-113">オプションの手順は、後からいつでも完了できます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="f4ca2-114">プロビジョニング後に Commerce プレビュー環境を構成する方法については、[Commerce プレビュー環境のコンフィギュレーション](cpe-post-provisioning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="f4ca2-115">Commerce プレビュー環境のオプション機能を構成する方法については、[Commerce プレビュー環境のオプション機能のコンフィギュレーション](cpe-optional-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="f4ca2-116">プロビジョニングの手順について質問がある場合、または問題が発生した場合は、[Microsoft Dynamics 365 Commerce プレビュー Yammer グループ](https://aka.ms/Dynamics365CommercePreviewYammer)から Microsoft にご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f4ca2-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="f4ca2-117">Prerequisites</span></span>

<span data-ttu-id="f4ca2-118">Commerce プレビュー環境をプロビジョニングする前に、次の前提条件が整っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="f4ca2-119">Microsoft Dynamics Lifecycle Services (LCS) ポータルへのアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="f4ca2-120">既存の Microsoft Dynamics 365 のパートナーまたは顧客は、Dynamics 365 Commerce プロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="f4ca2-121">Dynamics 365 Commerce プレビュー プログラムを承諾しました。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="f4ca2-122">**移行、ソリューションの作成、および学習**のためにプロジェクトを作成するのに必要なアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="f4ca2-123">環境のプロビジョニングを行うプロジェクトで、**環境管理者**または**プロジェクト所有者**ロールのメンバーになっています。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="f4ca2-124">Microsoft Azure サブスクリプションへの管理者アクセス許可があるか、または代理として管理者アクセス許可が必要な 2 つの手順を完了することができるサブスクリプション管理者の連絡先があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="f4ca2-125">Azure Active Directory (Azure AD) テナント ID が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="f4ca2-126">E コマース システムの管理者グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="f4ca2-127">評価とレビューのモデレーター グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="f4ca2-128">(このセキュリティ グループは、E コマースのシステム管理グループと同じにすることができます。)</span><span class="sxs-lookup"><span data-stu-id="f4ca2-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="f4ca2-129">Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="f4ca2-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="f4ca2-130">これらの手順は、Commerce プレビュー環境をプロビジョニングする方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="f4ca2-131">それらを正常に完了すると、Commerce プレビュー環境を構成する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="f4ca2-132">ここで説明するすべての活動は、LCS ポータルで発生します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4ca2-133">プレビューのアクセス許可は、コマース プレビュー アプリケーションで指定した LCS アカウントと組織に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="f4ca2-134">Commerce プレビュー環境をプロビジョニングするには、同じアカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="f4ca2-135">コマース プレビュー環境で別の LCS アカウントまたはテナントを使用する必要がある場合は、それらの詳細を Microsoft に提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="f4ca2-136">連絡先情報については、このトピック後半の [Commerce プレビュー環境のサポート](#commerce-preview-environment-support)セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="f4ca2-137">LCS でプレビュー機能が使用可能で有効になっていることを確認する</span><span class="sxs-lookup"><span data-stu-id="f4ca2-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="f4ca2-138">LCS でプレビュー機能が使用可能で有効になっていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="f4ca2-139">プレビューへのアクセス権を要求するために使用したのと同じ LCS アカウントを使用して、[LCS ポータル](https://lcs.dynamics.com)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="f4ca2-140">LCS ホーム ページで右にスクロールし、**プレビュー機能の管理**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![プレビュー管理タイル](./media/preview1.png)

1. <span data-ttu-id="f4ca2-142">**プライベート プレビュー機能**までスクロールし、次の機能が使用可能で有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="f4ca2-143">E コマースの評価</span><span class="sxs-lookup"><span data-stu-id="f4ca2-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="f4ca2-144">Commerce Preview プログラムの環境</span><span class="sxs-lookup"><span data-stu-id="f4ca2-144">Commerce Preview Program Environments</span></span>

    ![プライベート プレビューの機能](./media/preview2.png)

1. <span data-ttu-id="f4ca2-146">これらの機能がリストに表示されない場合は、Microsoft に連絡して、職場の電子メール アドレス、LCS アカウント、およびテナントの詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="f4ca2-147">連絡先情報については、[Commerce プレビュー環境のサポート](#commerce-preview-environment-support) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="f4ca2-148">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="f4ca2-148">Create a new project</span></span>

<span data-ttu-id="f4ca2-149">LCS に新しいプロジェクトを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="f4ca2-150">LCS のホーム ページで、プラス記号 (**+**) を選択してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="f4ca2-151">右側のウィンドウで、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="f4ca2-152">パートナーである場合、**移行、ソリューションの作成、および学習**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="f4ca2-153">顧客の場合、**見込みプリセールス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="f4ca2-154">名前と説明、および業種を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="f4ca2-155">**製品名**フィールドで、**Dynamics 365 Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="f4ca2-156">**製品バージョン** フィールドで、**Dynamics 365 Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="f4ca2-157">**方法**フィールドで、**Dynamics Retail の実装方法**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="f4ca2-158">オプション: ロールとユーザーを既存のプロジェクトからインポートできます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="f4ca2-159">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-159">Select **Create**.</span></span> <span data-ttu-id="f4ca2-160">プロジェクト ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="f4ca2-161">Azure コネクタの追加</span><span class="sxs-lookup"><span data-stu-id="f4ca2-161">Add the Azure Connector</span></span>

<span data-ttu-id="f4ca2-162">LCS プロジェクトに Azure コネクタを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="f4ca2-163">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="f4ca2-164">パートナーである場合は、右端で**プロジェクト設定**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="f4ca2-165">顧客の場合は、トップ メニューで**プロジェクト設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="f4ca2-166">**Azure コネクタ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="f4ca2-167">Azure コネクタを追加するには、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="f4ca2-168">名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-168">Enter a name.</span></span>
1. <span data-ttu-id="f4ca2-169">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="f4ca2-170">**Azure Resource Manager (ARM) を使用するようにコンフィギュレーションする**のオプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="f4ca2-171">**Azure サブスクリプション AAD テナント ドメイン (または ID)** の値が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="f4ca2-172">必要に応じて、Azure サブスクリプション管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="f4ca2-173">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-173">Select **Next**.</span></span>
1. <span data-ttu-id="f4ca2-174">ページの指示に従って、サブスクリプションに必要なアプリケーションのアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="f4ca2-175">必要に応じて、Azure サブスクリプション管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="f4ca2-176">[Azure ポータル](https://portal.azure.com/)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="f4ca2-177">適切なディレクトリが選択されていることを確認し、左側のメニューで**サブスクリプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="f4ca2-178">リストから正しいサブスクリプションを検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="f4ca2-179">必要に応じて検索機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="f4ca2-180">メニューから、**アクセス制御 (IAM)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="f4ca2-181">右側の**ロール割り当ての追加**で、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="f4ca2-182">**ロール割り当ての追加**ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="f4ca2-183">**ロール** フィールドで、**貢献者**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="f4ca2-184">**アクセス権の割り当て先**について、既定値を **Azure AD ユーザー、グループ、またはサービス プリンシパル**のままにします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="f4ca2-185">**選択**の下で、**b96b7e94-b82e-4e71-99a0-cf7fb188acea** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="f4ca2-186">リストから**Dynamics 配置サービス \[wsfed 有効\]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="f4ca2-187">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-187">Select **Save**.</span></span>

1. <span data-ttu-id="f4ca2-188">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-188">Select **Next**.</span></span>
1. <span data-ttu-id="f4ca2-189">ページの指示に従って、サブスクリプションに必要なアプリケーションのアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="f4ca2-190">必要に応じて、Azure サブスクリプション管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="f4ca2-191">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-191">Select **Next**.</span></span>
1. <span data-ttu-id="f4ca2-192">**Azure リージョン** フィールドで、**米国東部**、**米国東部 2**、**米国西部**、または**米国西部 2** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="f4ca2-193">**接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-193">Select **Connect**.</span></span> <span data-ttu-id="f4ca2-194">Azure コネクタがリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="f4ca2-195">コマース プレビュー デモ ベース拡張機能のインポート</span><span class="sxs-lookup"><span data-stu-id="f4ca2-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="f4ca2-196">コマース プレビュー デモ ベース拡張機能をプロジェクトにインポートするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="f4ca2-197">上部にあるプロジェクト名を選択して、プロジェクトのホーム ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="f4ca2-198">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="f4ca2-199">パートナーである場合は、右端の**資産ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="f4ca2-200">顧客の場合は、トップ メニューで**資産ライブラリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="f4ca2-201">左のリストから、**ソフトウェア配置可能パッケージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="f4ca2-202">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-202">Select **Import**.</span></span>
1. <span data-ttu-id="f4ca2-203">**共有アセット ライブラリ**で、資産のリストから**コマース プレビュー デモ ベース拡張機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="f4ca2-204">**ピック**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-204">Select **Pick**.</span></span> <span data-ttu-id="f4ca2-205">資産ライブラリに戻ると、リストに拡張機能が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="f4ca2-206">次の図は、LCS **資産ライブラリ** ページで実行する必要があるアクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![コマース プレビュー デモ ベース拡張機能のインポート](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="f4ca2-208">環境の配置</span><span class="sxs-lookup"><span data-stu-id="f4ca2-208">Deploy the environment</span></span>

<span data-ttu-id="f4ca2-209">環境を配置するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="f4ca2-210">オプションが 1 つしかないページはスキップされるため、手順 6、7、または 8 を完了する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="f4ca2-211">**環境パラメーター** ビューで、**Dynamics 365 Commerce - デモ (10.0.* x* プラットフォーム更新プログラム *xx*)\*\* が**環境名**フィールドのすぐ上に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="f4ca2-212">詳細については、手順 8 の後に表示されているイラストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="f4ca2-213">トップ メニューで、**クラウド ホスト環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="f4ca2-214">環境を追加するために**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="f4ca2-215">**アプリケーション バージョン** フィールドで、最新のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="f4ca2-216">最新バージョン以外のアプリケーション バージョンを特定する必要がある場合は、**10.0.8** より前のバージョンを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="f4ca2-217">**プラットフォーム バージョン** フィールドで、選択したアプリケーション バージョンに対して自動的に選択されたプラットフォーム バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![アプリケーションとプラットフォーム バージョンを選択する](./media/project1.png)

1. <span data-ttu-id="f4ca2-219">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-219">Select **Next**.</span></span>
1. <span data-ttu-id="f4ca2-220">環境のトポロジとして**デモ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-220">Select **Demo** as the environment topology.</span></span>

    ![環境トポロジ 1 を選択する](./media/project2.png)

1. <span data-ttu-id="f4ca2-222">環境のトポロジとして **Dynamics 365 Commerce - デモ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="f4ca2-223">以前に 1 つの Azure コネクタをコンフィギュレーションしている場合、この環境に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="f4ca2-224">複数の Azure コネクタをコンフィギュレーションした場合は、**米国東部**、**米国東部 2**、**米国西部**、または**米国西部 2** から、使用するコネクタを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="f4ca2-225">(最適なエンド ツー エンドのパフォーマンスのために、**米国西部 2** を選択することをお勧めします)。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![環境トポロジ 2 を選択する](./media/project3.png)

1. <span data-ttu-id="f4ca2-227">**環境の配置**のページで、環境名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="f4ca2-228">詳細設定はそのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-228">Leave the advanced settings as they are.</span></span>

    ![環境の配置のページ](./media/project4.png)

1. <span data-ttu-id="f4ca2-230">VM サイズを必要に応じて調整します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-230">Adjust the VM size as required.</span></span> <span data-ttu-id="f4ca2-231">(VM 最小在庫管理単位をお勧めします \[SKU\] **D13 v2**。)</span><span class="sxs-lookup"><span data-stu-id="f4ca2-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="f4ca2-232">価格決定およびライセンス条件を確認、チェック ボックスをオンにして同意したことを示します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="f4ca2-233">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-233">Select **Next**.</span></span>
1. <span data-ttu-id="f4ca2-234">配置の確認ページで、詳細が正しいことを確認した後、**配置**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="f4ca2-235">**クラウド ホスト環境**ビューに戻り、環境がリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="f4ca2-236">要求した環境はキューに格納され、その後配置されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="f4ca2-237">環境ワークフローは完了までに少し時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="f4ca2-238">そのため、約 6 ~ 9 時間後に再度確認してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="f4ca2-239">続行する前に、環境の状態が**配置済み**になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-csu"></a><span data-ttu-id="f4ca2-240">Commerce Scale Unit (CSU) を初期化する</span><span class="sxs-lookup"><span data-stu-id="f4ca2-240">Initialize the commerce scale unit (CSU)</span></span>

<span data-ttu-id="f4ca2-241">CSU を初期化するためには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="f4ca2-242">**クラウド ホスト環境**ビュー内で、リストから環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="f4ca2-243">右側の環境ビューで、**完全な詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="f4ca2-244">環境の詳細のビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-244">The environment details view appears.</span></span>
1. <span data-ttu-id="f4ca2-245">**環境機能**の下で、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="f4ca2-246">**コマース** タブで、**初期化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="f4ca2-247">CSU 初期化パラメーター ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="f4ca2-248">**地域**フィールドで、**米国東部**、**米国東部 2**、**米国西部**、または**米国西部 2** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="f4ca2-249">**バージョン** フィールドで、リストから**バージョンを指定する**を選択し、表示されるフィールドに **9.18.20014.4** を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="f4ca2-250">ここで示されている正確なバージョンを指定してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="f4ca2-251">それ以外の場合は、RCSU を後で正しいバージョンに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="f4ca2-252">**拡張機能の適用**オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="f4ca2-253">拡張機能のリストから、**コマース プレビュー デモ ベース拡張機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="f4ca2-254">**初期化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="f4ca2-255">配置の確認ページで、詳細が正しいことを確認した後、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="f4ca2-256">**コマース** タブが選択されているところでは、**コマースの管理**ビューが再度表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="f4ca2-257">CSU がプロビジョニング用にキューに格納されました。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="f4ca2-258">続行する前に、CSU の状態が**成功**となっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="f4ca2-259">初期化には約 2 ~ 5 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="f4ca2-260">E コマースの初期化</span><span class="sxs-lookup"><span data-stu-id="f4ca2-260">Initialize e-Commerce</span></span>

<span data-ttu-id="f4ca2-261">E コマースを初期化するためには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f4ca2-262">**E コマース** タブで、プレビューの同意を確認し、**設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="f4ca2-263">**E コマース テナント名**フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="f4ca2-264">ただし、この名前は E コマース インスタンスを指す URL の一部に表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="f4ca2-265">**Commerce scale unit の名前**フィールドで、リストから CSU を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-265">In the **Commerce scale unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="f4ca2-266">(リストには 1 つのオプションのみが必要です。)</span><span class="sxs-lookup"><span data-stu-id="f4ca2-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="f4ca2-267">**E コマースの地域**フィールドは自動的に設定され、値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="f4ca2-268">**次へ** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="f4ca2-269">**サポートされているホスト名**フィールドに、`www.fabrikam.com` などの有効なドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="f4ca2-270">**システム管理者の ADD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="f4ca2-271">検索結果を表示するには、拡大クラス アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="f4ca2-272">リストから正しいセキュリティ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="f4ca2-273">**評価とレビュー モデレーター用 ADD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="f4ca2-274">検索結果を表示するには、拡大クラス アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="f4ca2-275">リストから正しいセキュリティ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="f4ca2-276">**評価とレビュー サービスを有効にする**オプションを、有効のままにします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="f4ca2-277">**初期化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-277">Select **Initialize**.</span></span> <span data-ttu-id="f4ca2-278">**E コマース** タブが選択されているところでは、**コマースの管理**ビューが再度表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="f4ca2-279">E コマースの初期化を開始しました。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="f4ca2-280">続行する前に、E コマースの初期化状態が**初期化成功**になるまでお待ちください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="f4ca2-281">右下の**リンク**で、次のリンクの URL をメモします。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="f4ca2-282">**E コマース サイト** – E コマース サイトのルートへのリンク。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="f4ca2-283">**E コマース サイト管理ツール** – サイト管理ツールへのリンク。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="f4ca2-284">Commerce プレビュー環境のサポート</span><span class="sxs-lookup"><span data-stu-id="f4ca2-284">Commerce preview environment support</span></span>

<span data-ttu-id="f4ca2-285">プロビジョニング手順の完了中に問題が発生した場合は、[Microsoft Dynamics 365 Commerce プレビュー Yammer グループ](https://aka.ms/Dynamics365CommercePreviewYammer)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="f4ca2-286">Yammer グループにアクセスしようとして問題が発生した場合は、<Dynamics365Commerce@microsoft.com> から電子メールで Microsoft にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-286">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="f4ca2-287">この電子メール アドレスはアクティブに監視されていません。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-287">This email address isn't actively monitored.</span></span> <span data-ttu-id="f4ca2-288">したがって、応答に遅延が予想されます。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-288">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f4ca2-289">次のステップ</span><span class="sxs-lookup"><span data-stu-id="f4ca2-289">Next steps</span></span>

<span data-ttu-id="f4ca2-290">Commerce プレビュー環境のプロビジョニングと構成のプロセスを続行するには、[Commerce プレビュー環境のコンフィギュレーション](cpe-post-provisioning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4ca2-290">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4ca2-291">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f4ca2-291">Additional resources</span></span>

[<span data-ttu-id="f4ca2-292">Dynamics 365 Commerce プレビュー環境の概要</span><span class="sxs-lookup"><span data-stu-id="f4ca2-292">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="f4ca2-293">Dynamics 365 Commerce レビュー環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f4ca2-293">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="f4ca2-294">Dynamics 365 Commerce プレビュー環境のオプション機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f4ca2-294">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="f4ca2-295">Dynamics 365 Commerce プレビュー環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f4ca2-295">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="f4ca2-296">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="f4ca2-296">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="f4ca2-297">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="f4ca2-297">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="f4ca2-298">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="f4ca2-298">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="f4ca2-299">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="f4ca2-299">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

