---
title: Commerce プレビュー環境のプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境をプロビジョニングする方法について説明します。
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934751"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="a47d5-103">Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="a47d5-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a47d5-104">このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境をプロビジョニングする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="a47d5-105">開始する前に、少なくともトピック全体をざっと見て、プロセスに伴う事柄およびこのトピックに含まれる内容を把握することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="a47d5-106">Dynamics 365 Commerce プレビューへのアクセス許可がまだ与えられていない場合、[コマース Web サイト](https://aka.ms/Dynamics365CommerceWebsite)からプレビューのアクセス許可を要求できます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="a47d5-107">概要</span><span class="sxs-lookup"><span data-stu-id="a47d5-107">Overview</span></span>

<span data-ttu-id="a47d5-108">Commerce プレビュー環境を正常にプロビジョニングするには、特定の製品名とタイプを持つプロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="a47d5-109">環境および Retail Cloud Scale Unit (RCSU) には、後で E コマースをプロビジョニングをするために使用する必要がある特定のパラメーターもあります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="a47d5-110">このトピックの手順では、完了する必要があるすべての手順と、使用する必要があるパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="a47d5-111">Commerce プレビュー環境のプロビジョニングが正常に完了した後、いくつかのプロビジョニング後の手順を完了して準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="a47d5-112">一部の手順は、システムのどの側面を評価するかに応じて使用するオプションです。</span><span class="sxs-lookup"><span data-stu-id="a47d5-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="a47d5-113">オプションの手順は、後からいつでも完了できます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="a47d5-114">プロビジョニング後に Commerce プレビュー環境を構成する方法については、[Commerce プレビュー環境のコンフィギュレーション](cpe-post-provisioning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="a47d5-115">Commerce プレビュー環境のオプション機能を構成する方法については、[Commerce プレビュー環境のオプション機能のコンフィギュレーション](cpe-optional-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="a47d5-116">プロビジョニングの手順について質問がある場合、または問題が発生した場合は、[Microsoft Dynamics 365 Commerce プレビュー Yammer グループ](https://aka.ms/Dynamics365CommercePreviewYammer)から Microsoft にご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a47d5-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="a47d5-117">Prerequisites</span></span>

<span data-ttu-id="a47d5-118">Commerce プレビュー環境をプロビジョニングする前に、次の前提条件が整っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="a47d5-119">Microsoft Dynamics Lifecycle Services (LCS) ポータルへのアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="a47d5-120">Dynamics 365 Commerce プレビュー プログラムを承諾しました。</span><span class="sxs-lookup"><span data-stu-id="a47d5-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="a47d5-121">**見込みプリセールス**または**移行、ソリューションの作成、および学習**のためにプロジェクトを作成するのに必要なアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="a47d5-122">環境のプロビジョニングを行うプロジェクトで、**環境管理者**または**プロジェクト所有者**ロールのメンバーになっています。</span><span class="sxs-lookup"><span data-stu-id="a47d5-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="a47d5-123">Microsoft Azure サブスクリプションへの管理者アクセス許可があるか、または代理として管理者アクセス許可が必要な 2 つの手順を完了することができるサブスクリプション管理者の連絡先があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="a47d5-124">Azure Active Directory (Azure AD) テナント ID が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a47d5-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="a47d5-125">E コマース システムの管理者グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="a47d5-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="a47d5-126">評価とレビューのモデレーター グループとして使用される  Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="a47d5-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="a47d5-127">(このセキュリティ グループは、E コマースのシステム管理グループと同じにすることができます。)</span><span class="sxs-lookup"><span data-stu-id="a47d5-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="a47d5-128">Azure AD テナント ID を検索する</span><span class="sxs-lookup"><span data-stu-id="a47d5-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="a47d5-129">Azure AD テナント ID は、この例 **72f988bf-86f1-41af-91ab-2d7cd011db47** に似たグローバル固有識別子 (GUID) です。</span><span class="sxs-lookup"><span data-stu-id="a47d5-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="a47d5-130">Azure ポータル を使用した Azure AD テナント ID の検索</span><span class="sxs-lookup"><span data-stu-id="a47d5-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="a47d5-131">[Azure ポータル](https://portal.azure.com/)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="a47d5-132">正しいディレクトリが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="a47d5-133">左側のメニューで、**Azure Active Directory** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="a47d5-134">**管理**の下で、**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="a47d5-135">Azure AD テナント ID は、**ディレクトリ ID** の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="a47d5-136">OpenID Connect メタデータを使用した Azure AD テナント ID の検索</span><span class="sxs-lookup"><span data-stu-id="a47d5-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="a47d5-137">**\{YOUR\_DOMAIN\}** を、ドメイン (`microsoft.com` など) に置き換えて OpenID URL を作成します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="a47d5-138">たとえば、`https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` は、`https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration` になります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="a47d5-139">ドメインを含む OpenID URL に移動します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="a47d5-140">複数のプロパティ値で Azure AD テナント ID を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="a47d5-141">**authorization\_endpoint** を見つけ、`login.microsoftonline.com/` の直後に表示される GUID を抽出します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="a47d5-142">Azure AD セキュリティ グループ IDの検索</span><span class="sxs-lookup"><span data-stu-id="a47d5-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="a47d5-143">Azure AD セキュリティ グループの ID は、次の例 **436ea7f5-ee6c-40c1-9f08-825c5811066a** に類似した GUID です。</span><span class="sxs-lookup"><span data-stu-id="a47d5-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="a47d5-144">この手順では、ID を検索しようとしているグループのメンバーであると想定しています。</span><span class="sxs-lookup"><span data-stu-id="a47d5-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="a47d5-145">[グラフ エクスプローラー](https://developer.microsoft.com/graph/graph-explorer#)を開きます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="a47d5-146">**Microsoft によるサインイン**を選択し、資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="a47d5-147">左側から、**さらにサンプルを表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="a47d5-148">右側のウィンドウで、**グループ**を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="a47d5-149">右側のウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-149">Close the right pane.</span></span>
1. <span data-ttu-id="a47d5-150">**所属するすべてのグループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="a47d5-151">**応答プレビュー** フィールドで、グループを検索します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="a47d5-152">セキュリティ グループ ID が、**ID** プロパティの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="a47d5-153">Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="a47d5-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="a47d5-154">これらの手順は、Commerce プレビュー環境をプロビジョニングする方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="a47d5-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="a47d5-155">それらを正常に完了すると、Commerce プレビュー環境を構成する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="a47d5-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="a47d5-156">ここで説明するすべての活動は、LCS ポータルで発生します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a47d5-157">プレビューのアクセス許可は、プレビュー アプリケーションで指定した LCS アカウントと組織に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a47d5-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="a47d5-158">Commerce プレビュー環境をプロビジョニングするには、同じアカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="a47d5-159">Commerce プレビュー環境で別の LCS アカウントまたはテナントを使用する必要がある場合は、それらの詳細を Microsoft に提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="a47d5-160">連絡先情報については、このトピック後半の [Commerce プレビュー環境のサポート](#commerce-preview-environment-support)セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="a47d5-161">E コマース アプリケーションへのアクセス許可を与える</span><span class="sxs-lookup"><span data-stu-id="a47d5-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a47d5-162">サインインするユーザーは、Azure AD テナント ID を持つ Azure AD テナント管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="a47d5-163">このステップが正常に完了しなかった場合、残りのプロビジョニング ステップは失敗します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="a47d5-164">E コマース アプリケーションに Azure サブスクリプションへのアクセスを承認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="a47d5-165">次の形式で URL を組み立てます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="a47d5-166">URL をブラウザーまたはテキスト エディターにコピーして貼り付け、**\{AAD\_テナント\_ID\}** を、Azure AD テナント ID に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="a47d5-167">URL を開きます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-167">Then open the URL.</span></span>
1. <span data-ttu-id="a47d5-168">Azure AD サインイン ダイアログ ボックスでサインインし、**Dynamics 365 Commerce (プレビュー)** アクセス許可をサブスクリプションに付与することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="a47d5-169">操作が成功したかどうかを示すページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="a47d5-170">LCS でプレビュー機能が使用可能で有効になっていることを確認する</span><span class="sxs-lookup"><span data-stu-id="a47d5-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="a47d5-171">LCS でプレビュー機能が使用可能で有効になっていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="a47d5-172">プレビューへのアクセス権を要求するために使用したのと同じ LCS アカウントを使用して、[LCS ポータル](https://lcs.dynamics.com)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="a47d5-173">LCS ホーム ページで右にスクロールし、**プレビュー機能の管理**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![プレビュー管理タイル](./media/preview1.png)

1. <span data-ttu-id="a47d5-175">**プライベート プレビュー機能**までスクロールし、次の機能が使用可能で有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="a47d5-176">E コマースの評価</span><span class="sxs-lookup"><span data-stu-id="a47d5-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="a47d5-177">Commerce Preview プログラムの環境</span><span class="sxs-lookup"><span data-stu-id="a47d5-177">Commerce Preview Program Environments</span></span>

    ![プライベート プレビューの機能](./media/preview2.png)

1. <span data-ttu-id="a47d5-179">これらの機能がリストに表示されない場合は、Microsoft に連絡して、職場の電子メール アドレス、LCS アカウント、およびテナントの詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="a47d5-180">連絡先情報については、[Commerce プレビュー環境のサポート](#commerce-preview-environment-support) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="a47d5-181">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="a47d5-181">Create a new project</span></span>

<span data-ttu-id="a47d5-182">LCS に新しいプロジェクトを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="a47d5-183">LCS のホーム ページで、プラス記号 (**+**) を選択してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="a47d5-184">右側のウィンドウで、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="a47d5-185">パートナーである場合、**移行、ソリューションの作成、および学習**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="a47d5-186">顧客の場合、**見込みプリセールス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="a47d5-187">名前と説明、および業種を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="a47d5-188">**製品名**フィールドで、**Dynamics 365 Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="a47d5-189">**製品バージョン** フィールドで、**Dynamics 365 Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="a47d5-190">**方法**フィールドで、**Dynamics Retail の実装方法**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="a47d5-191">オプション: ロールとユーザーを既存のプロジェクトからインポートできます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="a47d5-192">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-192">Select **Create**.</span></span> <span data-ttu-id="a47d5-193">プロジェクト ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="a47d5-194">Azure コネクタの追加</span><span class="sxs-lookup"><span data-stu-id="a47d5-194">Add the Azure Connector</span></span>

<span data-ttu-id="a47d5-195">LCS プロジェクトに Azure コネクタを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="a47d5-196">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="a47d5-197">パートナーである場合は、右端で**プロジェクト設定**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="a47d5-198">顧客の場合は、トップ メニューで**プロジェクト設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="a47d5-199">**Azure コネクタ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="a47d5-200">Azure コネクタを追加するには、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="a47d5-201">名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-201">Enter a name.</span></span>
1. <span data-ttu-id="a47d5-202">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="a47d5-203">**Azure Resource Manager (ARM) を使用するようにコンフィギュレーションする**のオプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="a47d5-204">**Azure サブスクリプション AAD テナント ドメイン (または ID)** の値が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="a47d5-205">必要に応じて、Azure サブスクリプション管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="a47d5-206">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-206">Select **Next**.</span></span>
1. <span data-ttu-id="a47d5-207">ページの指示に従って、サブスクリプションに必要なアプリケーションのアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="a47d5-208">必要に応じて、Azure サブスクリプション管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="a47d5-209">[Azure ポータル](https://portal.azure.com/)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="a47d5-210">適切なディレクトリが選択されていることを確認し、左側のメニューで**サブスクリプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="a47d5-211">リストから正しいサブスクリプションを検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="a47d5-212">必要に応じて検索機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="a47d5-213">メニューから、**アクセス制御 (IAM)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="a47d5-214">右側の**ロール割り当ての追加**で、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="a47d5-215">**ロール割り当ての追加**ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="a47d5-216">**ロール** フィールドで、**貢献者**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="a47d5-217">**アクセス権の割り当て先**について、既定値を **Azure AD ユーザー、グループ、またはサービス プリンシパル**のままにします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="a47d5-218">**選択**の下で、**b96b7e94-b82e-4e71-99a0-cf7fb188acea** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="a47d5-219">リストから**Dynamics 配置サービス \[wsfed 有効\]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="a47d5-220">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-220">Select **Save**.</span></span>

1. <span data-ttu-id="a47d5-221">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-221">Select **Next**.</span></span>
1. <span data-ttu-id="a47d5-222">ページの指示に従って、サブスクリプションに必要なアプリケーションのアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="a47d5-223">必要に応じて、Azure サブスクリプション管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="a47d5-224">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-224">Select **Next**.</span></span>
1. <span data-ttu-id="a47d5-225">**Azure リージョン** フィールドで、**米国東部**、**米国東部 2**、**米国西部**、または**米国西部 2** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="a47d5-226">**接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-226">Select **Connect**.</span></span> <span data-ttu-id="a47d5-227">Azure コネクタがリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="a47d5-228">コマース プレビュー デモ ベース拡張機能のインポート</span><span class="sxs-lookup"><span data-stu-id="a47d5-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="a47d5-229">コマース プレビュー デモ ベース拡張機能をプロジェクトにインポートするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="a47d5-230">上部にあるプロジェクト名を選択して、プロジェクトのホーム ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="a47d5-231">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="a47d5-232">パートナーである場合は、右端の**資産ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="a47d5-233">顧客の場合は、トップ メニューで**資産ライブラリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="a47d5-234">左のリストから、**ソフトウェア配置可能パッケージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="a47d5-235">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-235">Select **Import**.</span></span>
1. <span data-ttu-id="a47d5-236">**共有アセット ライブラリ**で、資産のリストから**コマース プレビュー デモ ベース拡張機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="a47d5-237">**ピック**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-237">Select **Pick**.</span></span> <span data-ttu-id="a47d5-238">資産ライブラリに戻ると、リストに拡張機能が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="a47d5-239">次の図は、LCS **資産ライブラリ** ページで実行する必要があるアクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="a47d5-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![コマース プレビュー デモ ベース拡張機能のインポート](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="a47d5-241">環境の配置</span><span class="sxs-lookup"><span data-stu-id="a47d5-241">Deploy the environment</span></span>

<span data-ttu-id="a47d5-242">環境を配置するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a47d5-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="a47d5-243">オプションが 1 つしかないページはスキップされるため、手順 6、7、または 8 を完了する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a47d5-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="a47d5-244">**環境パラメーター** ビューで、**Dynamics 365 Commerce (プレビュー) - デモ (10.0.6 プラットフォーム更新プログラム 30)** が**環境名**フィールドのすぐ上に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="a47d5-245">手順 8 の後に表示されているイラストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="a47d5-246">トップ メニューで、**クラウド ホスト環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="a47d5-247">環境を追加するために**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="a47d5-248">**アプリケーション バージョン** フィールドで、**10.0.6** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="a47d5-249">**プラットフォーム バージョン**フィールドで、**プラットフォーム更新プログラム 30** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![アプリケーションとプラットフォーム バージョンを選択する](./media/project1.png)

1. <span data-ttu-id="a47d5-251">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-251">Select **Next**.</span></span>
1. <span data-ttu-id="a47d5-252">環境のトポロジとして**デモ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-252">Select **Demo** as the environment topology.</span></span>

    ![環境トポロジ 1 を選択する](./media/project2.png)

1. <span data-ttu-id="a47d5-254">環境のトポロジとして**Dynamics 365 Commerce (プレビュー) - デモ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="a47d5-255">以前に 1 つの Azure コネクタをコンフィギュレーションしている場合、この環境に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="a47d5-256">複数の Azure コネクタをコンフィギュレーションした場合は、**米国東部**、**米国東部 2**、**米国西部**、または**米国西部 2** から、使用するコネクタを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="a47d5-257">(最適なエンド ツー エンドのパフォーマンスのために、**米国西部 2** を選択することをお勧めします)。</span><span class="sxs-lookup"><span data-stu-id="a47d5-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![環境トポロジ 2 を選択する](./media/project3.png)

1. <span data-ttu-id="a47d5-259">**環境の配置**のページで、環境名を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="a47d5-260">詳細設定はそのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-260">Leave the advanced settings as they are.</span></span>

    ![環境の配置のページ](./media/project4.png)

1. <span data-ttu-id="a47d5-262">VM サイズを必要に応じて調整します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-262">Adjust the VM size as required.</span></span> <span data-ttu-id="a47d5-263">(VM 最小在庫管理単位をお勧めします \[SKU\] **D13 v2**。)</span><span class="sxs-lookup"><span data-stu-id="a47d5-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="a47d5-264">価格決定およびライセンス条件を確認、チェック ボックスをオンにして同意したことを示します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="a47d5-265">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-265">Select **Next**.</span></span>
1. <span data-ttu-id="a47d5-266">配置の確認ページで、詳細が正しいことを確認した後、**配置**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="a47d5-267">**クラウド ホスト環境**ビューに戻り、環境がリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="a47d5-268">要求した環境はキューに格納され、その後配置されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="a47d5-269">環境ワークフローは完了までに少し時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="a47d5-270">そのため、約 6 ~ 9 時間後に再度確認してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="a47d5-271">続行する前に、環境の状態が**配置済み**になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="a47d5-272">RCSU の初期化</span><span class="sxs-lookup"><span data-stu-id="a47d5-272">Initialize RCSU</span></span>

<span data-ttu-id="a47d5-273">RCSU を初期化するためには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a47d5-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="a47d5-274">**クラウド ホスト環境**ビュー内で、リストから環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="a47d5-275">右側の環境ビューで、**完全な詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="a47d5-276">環境の詳細のビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-276">The environment details view appears.</span></span>
1. <span data-ttu-id="a47d5-277">**環境機能**の下で、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="a47d5-278">**小売**タブで、**初期化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="a47d5-279">RCSU 初期化パラメーター ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="a47d5-280">**地域**フィールドで、**米国東部**、**米国東部 2**、**米国西部**、または**米国西部 2** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="a47d5-281">**バージョン** フィールドで、リストから**バージョンを指定する**を選択し、表示されるフィールドに **9.16.19262.5** を指定します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="a47d5-282">ここで示されている正確なバージョンを指定してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="a47d5-283">それ以外の場合は、RCSU を後で正しいバージョンに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="a47d5-284">**拡張機能の適用**オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="a47d5-285">拡張機能のリストから、**コマース プレビュー デモ ベース拡張機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="a47d5-286">**初期化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="a47d5-287">配置の確認ページで、詳細が正しいことを確認した後、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="a47d5-288">**小売**タブが選択され、**小売管理**ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="a47d5-289">RCSU がプロビジョニング用にキューに格納されました。</span><span class="sxs-lookup"><span data-stu-id="a47d5-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="a47d5-290">続行する前に、RCSU の状態が**成功**になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="a47d5-291">初期化には約 2 ~ 5 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="a47d5-292">E コマースの初期化</span><span class="sxs-lookup"><span data-stu-id="a47d5-292">Initialize e-Commerce</span></span>

<span data-ttu-id="a47d5-293">E コマースを初期化するためには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a47d5-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a47d5-294">**E コマース (プレビュー)** タブで、プレビューの同意を確認し、**設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="a47d5-295">**E コマース テナント名**フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="a47d5-296">ただし、この名前は E コマース インスタンスを指す URL の一部に表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="a47d5-297">**Retail cloud scale unit の名前**フィールドで、リストから RCSU を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="a47d5-298">(リストには 1 つのオプションのみが必要です。)</span><span class="sxs-lookup"><span data-stu-id="a47d5-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="a47d5-299">**E コマースの地域**フィールドは自動的に設定され、値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="a47d5-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="a47d5-300">**次へ** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="a47d5-301">**サポートされているホスト名**フィールドに、`www.fabrikam.com` などの有効なドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="a47d5-302">**システム管理者の ADD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="a47d5-303">検索結果を表示するには、拡大クラス アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="a47d5-304">リストからセキュリティ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="a47d5-305">**評価とレビュー モデレーター用 ADD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="a47d5-306">検索結果を表示するには、拡大クラス アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="a47d5-307">リストからセキュリティ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="a47d5-308">**評価とレビュー サービスを有効にする**オプションを、有効のままにします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="a47d5-309">「E コマース アプリケーションへのアクセスを許可する」セクションの説明に従って、Microsoft Azure Active Directory (Azure AD) の同意の手順を完了している場合は、このチェック ボックスをオンにして同意を確認します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="a47d5-310">この手順をまだ完了していない場合は、初期化を行う前にこの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="a47d5-311">チェック ボックスの横にあるテキスト内のリンクを選択して、同意ダイアログ ボックスを開き、手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="a47d5-312">**初期化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a47d5-312">Select **Initialize**.</span></span> <span data-ttu-id="a47d5-313">**E コマース (プレビュー)** タブが選択され、**小売管理**ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="a47d5-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="a47d5-314">E コマースの初期化を開始しました。</span><span class="sxs-lookup"><span data-stu-id="a47d5-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="a47d5-315">続行する前に、E コマースの初期化状態が**初期化成功**になるまでお待ちください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="a47d5-316">右下の**リンク**で、次のリンクの URL をメモします。</span><span class="sxs-lookup"><span data-stu-id="a47d5-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="a47d5-317">**E コマース サイト** – E コマース サイトのルートへのリンク。</span><span class="sxs-lookup"><span data-stu-id="a47d5-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="a47d5-318">**E コマース サイト管理ツール** – サイト管理ツールへのリンク。</span><span class="sxs-lookup"><span data-stu-id="a47d5-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="a47d5-319">Commerce プレビュー環境のサポート</span><span class="sxs-lookup"><span data-stu-id="a47d5-319">Commerce preview environment support</span></span>

<span data-ttu-id="a47d5-320">プロビジョニング手順の完了中に問題が発生した場合は、[Microsoft Dynamics 365 Commerce プレビュー Yammer グループ](https://aka.ms/Dynamics365CommercePreviewYammer)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="a47d5-321">Yammer グループにアクセスしようとして問題が発生した場合は、<Dynamics365Commerce@microsoft.com> から電子メールで Microsoft にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="a47d5-322">この電子メール アドレスはアクティブに監視されていません。</span><span class="sxs-lookup"><span data-stu-id="a47d5-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="a47d5-323">したがって、応答に遅延が予想されます。</span><span class="sxs-lookup"><span data-stu-id="a47d5-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a47d5-324">次のステップ</span><span class="sxs-lookup"><span data-stu-id="a47d5-324">Next steps</span></span>

<span data-ttu-id="a47d5-325">Commerce プレビュー環境のプロビジョニングと構成のプロセスを続行するには、[Commerce プレビュー環境のコンフィギュレーション](cpe-post-provisioning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a47d5-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a47d5-326">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a47d5-326">Additional resources</span></span>

[<span data-ttu-id="a47d5-327">Commerce プレビュー環境の概要</span><span class="sxs-lookup"><span data-stu-id="a47d5-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="a47d5-328">Commerce プレビュー環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a47d5-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="a47d5-329">Commerce プレビュー環境のオプション機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a47d5-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="a47d5-330">Commerce プレビュー環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="a47d5-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="a47d5-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a47d5-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="a47d5-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="a47d5-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="a47d5-333">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="a47d5-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="a47d5-334">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="a47d5-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="a47d5-335">Dynamics 365 Retail のヘルプ リソース</span><span class="sxs-lookup"><span data-stu-id="a47d5-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
