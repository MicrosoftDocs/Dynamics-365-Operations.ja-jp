---
title: B2C テナントを Commerce に 設定
description: このトピックでは、Dynamics 365 Commerce のユーザーサイト認証のために Azure Active Directory (Azure AD) の企業と顧客間 (B2C) テナントを設定する方法について説明します。
author: BrianShook
manager: annbe
ms.date: 04/17 /2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: f4768eede43003aac892b861b4a86ababe98a189
ms.sourcegitcommit: 063c4d7155be6c2cadcafa1630d16ee235285479
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270213"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="65366-103">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="65366-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65366-104">このトピックでは、Dynamics 365 Commerce のユーザーサイト認証のために Azure Active Directory (Azure AD) の企業と顧客間 (B2C) テナントを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="65366-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="65366-105">概要</span><span class="sxs-lookup"><span data-stu-id="65366-105">Overview</span></span>

<span data-ttu-id="65366-106">Dynamics 365 Commerce は Azure AD B2C を使用して、ユーザーの資格情報と認証フローをサポートします。</span><span class="sxs-lookup"><span data-stu-id="65366-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="65366-107">ユーザーは、これらのフローを使用して、登録、サインイン、およびパスワードのリセットを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="65366-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="65366-108">Azure AD B2C では、ユーザー名やパスワードなどの機密性の高いユーザー認証情報を保存します。</span><span class="sxs-lookup"><span data-stu-id="65366-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="65366-109">B2C テナントのユーザー レコードには、B2C ローカル アカウント レコードまたは B2C ソーシャル ID プロバイダー レコードのいずれかが保存されます。</span><span class="sxs-lookup"><span data-stu-id="65366-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="65366-110">これらの B2C レコードは、Commerce 環境内の顧客レコードにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="65366-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="65366-111">Azure ポータルでの既存の AAD B2C テナントの作成またはリンク</span><span class="sxs-lookup"><span data-stu-id="65366-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="65366-112">[Azure ポータル](https://portal.azure.com/)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="65366-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="65366-113">Azure ポータル メニューから、**リソースの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="65366-114">Commerce 環境に関連付けられているサブスクリプションとディレクトリを使用してください。</span><span class="sxs-lookup"><span data-stu-id="65366-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Azure ポータルでのリソースの作成](./media/B2CImage_1.png)

1. <span data-ttu-id="65366-116">**ID \> Azure Active Directory B2C** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65366-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="65366-117">**新しい B2C テナントの作成または既存のテナントへのリンク**のページで、会社のニーズに適した以下のオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="65366-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="65366-118">**新しい Azure AD B2C テナントの作成**: 新しい AAD B2C テナントを作成するには、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="65366-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="65366-119">**新しい Azure AD B2C テナントの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="65366-120">**組織名**に組織名を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="65366-121">**最初のドメイン名**に最初のドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="65366-122">**国/地域**では、国または地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="65366-123">**作成**を選択して、テナントを作成します。</span><span class="sxs-lookup"><span data-stu-id="65366-123">Select **Create** to create the tenant.</span></span>

     ![新しい Azure AD テナントの作成](./media/B2CImage_2.png)

     - <span data-ttu-id="65366-125">**既存の Azure AD B2C テナントを Azure サブスクリプションにリンクする**: リンクする Azure AD テナントが既にある場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="65366-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="65366-126">**既存の Azure AD の B2C テナントを Azure サブスクリプションにリンクする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="65366-127">**Azure AD B2C テナント**には、適切な B2C テナントを選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="65366-128">選択ボックスに「適格な B2C テナントが見つかりません」というメッセージが表示された場合は、適格な B2C テナントが存在しないので、新しいテナントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="65366-129">**リソース グループ**で、**新規作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="65366-130">テナントを格納するリソース グループの**名前**を入力し、**リソース グループの場所**を選択して、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![既存の Azure AD B2C テナントを Azure サブスクリプションにリンクする](./media/B2CImage_3.png)

1. <span data-ttu-id="65366-132">新しい Azure AD B2C ディレクトリが作成されると (しばらく時間がかかる場合があります)、新しいディレクトリへのリンクがダッシュボードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="65366-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="65366-133">このリンクを使用すると、「Azure Active Directory B2C へようこそ」のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="65366-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![新しい AAD ディレクトリへのリンク](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="65366-135">Azure アカウント内に複数のサブスクリプションがある場合、または有効なサブスクリプションにリンクせずに B2C テナントを設定している場合、**トラブルシューティング** バナーは、テナントをサブスクリプションにリンクするよう指示します。</span><span class="sxs-lookup"><span data-stu-id="65366-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="65366-136">トラブルシューティングのメッセージを選択し、指示に従ってサブスクリプションの問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="65366-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="65366-137">次の図は、Azure AD B2C **トラブルシューティング** バナーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![ディレクトリに有効なサブスクリプションがないことを示す警告](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="65366-139">B2C アプリケーションを作成する</span><span class="sxs-lookup"><span data-stu-id="65366-139">Create the B2C application</span></span>

<span data-ttu-id="65366-140">B2C テナントが作成されたら、そのテナント内に B2C アプリケーションを作成して、コマース アクションを操作します。</span><span class="sxs-lookup"><span data-stu-id="65366-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="65366-141">B2C アプリケーションを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="65366-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="65366-142">Azure ポータルで、**アプリケーション**を選択し、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-142">In the Azure portal, select **Applications** and then select **Add**.</span></span>
1. <span data-ttu-id="65366-143">**名前**に、目的の AAD B2C アプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="65366-144">**Web アプリ/Web API** で、**Web アプリ/Web API を含める**を**はい**と選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="65366-145">**暗黙的なフローを許可する**では、**はい** (既定値) を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="65366-146">**返信 URL** で、専用の返信 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="65366-147">返信 URL およびここでのフォーマットについては、[返信 URL](#reply-urls) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65366-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="65366-148">**ネイティブ クライアントを含める**では、**いいえ**を選択します (既定値)。</span><span class="sxs-lookup"><span data-stu-id="65366-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="65366-149">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="65366-150">返信 URL</span><span class="sxs-lookup"><span data-stu-id="65366-150">Reply URLs</span></span>

<span data-ttu-id="65366-151">返信 URL は、サイトが Azure AD B2C を呼び出してユーザーを認証する場合に、リターン ドメインのホワイトリストを使用できるようにするために重要です。</span><span class="sxs-lookup"><span data-stu-id="65366-151">Reply URLs are important as they allow a whitelist of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="65366-152">これにより、認証されたユーザーは、サインイン元のドメイン (サイト ドメイン) に戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="65366-152">This allows the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="65366-153">**Azure AD B2C - アプリケーション \> 新しいアプリケーション**の画面の**返信 URL** ボックスには、サイト ドメインと (環境がプロビジョニングされたら) コマースが生成した URL の両方に個別の明細行を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="65366-154">これらの URL は、常に有効な URL 形式を使用する必要があり、ベース URL のみにする必要があります (末尾のスラッシュやパスは使用しないでください)。</span><span class="sxs-lookup"><span data-stu-id="65366-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="65366-155">次に、続く例のように文字列 ``/_msdyn365/authresp`` をベース URL に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- ``https://fabrikam.com/_msdyn365/authresp``
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="65366-156">ユーザー フロー ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="65366-156">Create user flow policies</span></span>

<span data-ttu-id="65366-157">ユーザー フローは、Azure AD B2C が保護されたサインイン、登録、プロファイルの編集、およびパスワードを忘れた際のユーザー エクスペリエンスを提供するために使用するポリシーです。</span><span class="sxs-lookup"><span data-stu-id="65366-157">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="65366-158">Dynamics 365 Commerce では、これらのフローを使用して、Azure AD B2C テナントと対話するポリシー アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-158">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="65366-159">ユーザーは、これらのポリシーを操作するときに、Azure AD B2C テナントにリダイレクトされてアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-159">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="65366-160">Azure AD B2Cでは、次の 3 つの基本的なユーザー フロー タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="65366-160">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="65366-161">登録とサインイン</span><span class="sxs-lookup"><span data-stu-id="65366-161">Sign up and sign in</span></span>
- <span data-ttu-id="65366-162">プロファイルの編集</span><span class="sxs-lookup"><span data-stu-id="65366-162">Profile editing</span></span>
- <span data-ttu-id="65366-163">パスワードのリセット</span><span class="sxs-lookup"><span data-stu-id="65366-163">Password reset</span></span>

<span data-ttu-id="65366-164">Azure AD が提供する既定のユーザー フローを使用するように選択できます。これにより、AAD B2Cでホストされるページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="65366-164">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="65366-165">また、HTML ページを作成して、これらのユーザー フローのエクスペリエンスの外観をコントロールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="65366-165">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="65366-166">Dynamics 365 Commerce のユーザー ポリシー ページをカスタマイズするには、[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65366-166">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="65366-167">詳細については[Azure Active Directory B2C のユーザーエクスペリエンスのインターフェイスをカスタマイズする](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65366-167">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="65366-168">登録を作成し、ユーザー フロー ポリシーにサインインする</span><span class="sxs-lookup"><span data-stu-id="65366-168">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="65366-169">登録を作成し、ユーザー フロー ポリシーにサインインするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-169">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="65366-170">Azure ポータルで、左のナビゲーション ウィンドウの**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-170">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="65366-171">**Azure AD B2C – ユーザー フロー (ポリシー)** ページで、**新しいユーザー フロー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-171">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="65366-172">**推奨**タブで、**登録してサインイン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-172">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="65366-173">**名前**に、ポリシー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-173">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="65366-174">この名前は、後でポータルによって割り当てられる接頭語 (「B2C_1_」など) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="65366-174">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="65366-175">**ID プロバイダー**の下で、適切なチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="65366-175">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="65366-176">**マルチファクター認証**で、会社に適した選択肢を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-176">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="65366-177">**ユーザー属性およびクレーム**で、必要に応じて属性を収集したり、クレームを返したりするためのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-177">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="65366-178">コマースでは、次の既定のオプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-178">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="65366-179">**属性の収集**</span><span class="sxs-lookup"><span data-stu-id="65366-179">**Collect  attribute**</span></span> | <span data-ttu-id="65366-180">**返品クレーム**</span><span class="sxs-lookup"><span data-stu-id="65366-180">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    |                        | <span data-ttu-id="65366-181">電子メール アドレス</span><span class="sxs-lookup"><span data-stu-id="65366-181">Email Addresses</span></span>   |
    | <span data-ttu-id="65366-182">指定された名前</span><span class="sxs-lookup"><span data-stu-id="65366-182">Given Name</span></span>             | <span data-ttu-id="65366-183">指定された名前</span><span class="sxs-lookup"><span data-stu-id="65366-183">Given Name</span></span>        |
    |                        | <span data-ttu-id="65366-184">ID プロバイダー</span><span class="sxs-lookup"><span data-stu-id="65366-184">Identity Provider</span></span> |
    | <span data-ttu-id="65366-185">姓</span><span class="sxs-lookup"><span data-stu-id="65366-185">Surname</span></span>                | <span data-ttu-id="65366-186">姓</span><span class="sxs-lookup"><span data-stu-id="65366-186">Surname</span></span>           |
    |                        | <span data-ttu-id="65366-187">ユーザーのオブジェクト ID</span><span class="sxs-lookup"><span data-stu-id="65366-187">User’s Object ID</span></span>  |

1. <span data-ttu-id="65366-188">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-188">Select **Create**.</span></span>

<span data-ttu-id="65366-189">次の図は、ユーザー フローにおける Azure AD B2C の登録とサインインの例です。</span><span class="sxs-lookup"><span data-stu-id="65366-189">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![登録とサインイン ポリシーの設定](./media/B2CImage_11.png)

<span data-ttu-id="65366-191">次の図は、ユーザー フローの Azure AD B2C 登録とサインインにおける**ユーザー フローの実行**オプションを示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-191">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![ポリシー フローでのユーザー フロー オプションの実行](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="65366-193">プロファイル編集ユーザー フロー ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="65366-193">Create a profile editing user flow policy</span></span>

<span data-ttu-id="65366-194">プロファイル編集ユーザー フロー ポリシーを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-194">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="65366-195">Azure ポータルで、左のナビゲーション ウィンドウの**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-195">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="65366-196">**Azure AD B2C – ユーザー フロー (ポリシー)** ページで、**新しいユーザー フロー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-196">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="65366-197">**推奨**タブで、**プロファイルの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-197">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="65366-198">**名前**で、プロファイル編集ユーザー フローを入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-198">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="65366-199">この名前は、後でポータルによって割り当てられる接頭語 (「B2C_1_」など) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="65366-199">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="65366-200">**ID プロバイダー**で、**ローカル アカウント サインイン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-200">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="65366-201">**ユーザー属性**で、次のチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-201">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="65366-202">**電子メール アドレス** (**返品クレーム**のみ)</span><span class="sxs-lookup"><span data-stu-id="65366-202">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="65366-203">**指定された名前** (**収集属性**および**返品クレーム**)</span><span class="sxs-lookup"><span data-stu-id="65366-203">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="65366-204">**ID プロバイダー** (**返品クレーム**のみ)</span><span class="sxs-lookup"><span data-stu-id="65366-204">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="65366-205">**姓** (**収集属性**および**返品クレーム**)</span><span class="sxs-lookup"><span data-stu-id="65366-205">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="65366-206">**ユーザーのオブジェクト ID** (**返品クレーム**のみ)</span><span class="sxs-lookup"><span data-stu-id="65366-206">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="65366-207">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-207">Select **Create**.</span></span>

<span data-ttu-id="65366-208">次の図は、Azure AD B2C プロファイル編集ユーザー フローの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-208">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![プロファイル編集ユーザー フローの作成](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="65366-210">パスワード リセット ユーザー フロー ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="65366-210">Create a password reset user flow policy</span></span>

<span data-ttu-id="65366-211">パスワード リセット ユーザー フロー ポリシーを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-211">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="65366-212">Azure ポータルで、左のナビゲーション ウィンドウの**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-212">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="65366-213">**Azure AD B2C – ユーザー フロー (ポリシー)** ページで、**新しいユーザー フロー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-213">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="65366-214">**推奨**タブで、**パスワードのリセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-214">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="65366-215">**名前**に、パスワード リセット ユーザー フローの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-215">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="65366-216">**ID プロバイダー** で、**電子メール アドレスを使用したパスワードのリセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-216">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="65366-217">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-217">Select **Create**.</span></span>
1. <span data-ttu-id="65366-218">**アプリケーション クレーム**で、次のチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-218">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="65366-219">**電子メール アドレス**</span><span class="sxs-lookup"><span data-stu-id="65366-219">**Email addresses**</span></span>
    - <span data-ttu-id="65366-220">**指定された名前**</span><span class="sxs-lookup"><span data-stu-id="65366-220">**Given Name**</span></span>
    - <span data-ttu-id="65366-221">**姓**</span><span class="sxs-lookup"><span data-stu-id="65366-221">**Surname**</span></span>
    - <span data-ttu-id="65366-222">**ユーザーのオブジェクト ID**</span><span class="sxs-lookup"><span data-stu-id="65366-222">**User's Object ID**</span></span>
1. <span data-ttu-id="65366-223">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-223">Select **Create**.</span></span>

<span data-ttu-id="65366-224">次の図は、Azure AD B2C パスワード リセットのユーザー フローで、**メール アドレスを使用したパスワードのリセット**を設定する場所を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-224">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![パスワード リセット ポリシーで「メール アドレスを使用してパスワードをリセットする」を設定する](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="65366-226">ソーシャル ID プロバイダーの追加 (オプション)</span><span class="sxs-lookup"><span data-stu-id="65366-226">Add social identity providers (Optional)</span></span>

<span data-ttu-id="65366-227">ソーシャル ID プロバイダーを使用すると、ユーザーは自分のソーシャル アカウントを使用して認証を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="65366-227">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="65366-228">ソーシャル ID プロバイダー認証の追加は Dynamics 365 Commerce で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="65366-228">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="65366-229">ソーシャル ID プロバイダー認証が追加されていない場合、既定の Azure AD B2C プロファイルがユーザー ベースの主要プロファイルになります。</span><span class="sxs-lookup"><span data-stu-id="65366-229">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="65366-230">ユーザーは自分のユーザー名 (お好みの電子メール アドレス) を選択し、パスワードを設定します。</span><span class="sxs-lookup"><span data-stu-id="65366-230">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="65366-231">Azure AD B2C はユーザーを直接認証します。</span><span class="sxs-lookup"><span data-stu-id="65366-231">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="65366-232">ソーシャル ID プロバイダー認証が追加され、ユーザーがそのいずれかのソーシャル ID プロバイダーを選択した場合でも、Azure AD B2C テナントにはエンティティが作成されます。</span><span class="sxs-lookup"><span data-stu-id="65366-232">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="65366-233">Azure AD B2C は、ソーシャル ID プロバイダーを使用してユーザーの資格情報を認証します。</span><span class="sxs-lookup"><span data-stu-id="65366-233">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="65366-234">ID プロバイダーの登録は B2C テナントにレコードを作成しますが、認証のために外部のソーシャル ID プロバイダーの参照を呼び出すため、ローカル アカウントとは異なる形式です。</span><span class="sxs-lookup"><span data-stu-id="65366-234">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="65366-235">ユーザーは、ソーシャル ID プロバイダー間で同じ電子メール アドレスを使用できます。つまり、認証に使用される電子メール ユーザー名はテナントに対して固有ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="65366-235">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="65366-236">Azure AD B2C は、ユーザーがローカル B2C アカウントで固有の電子メール アドレスを持つ場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="65366-236">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="65366-237">認証用のソーシャル ID プロバイダーを追加する前に、ID プロバイダーのポータルにアクセスして、Azure AD B2C ドキュメントの指示に従って ID プロバイダーアプリケーションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-237">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="65366-238">ドキュメントへのリンクの一覧は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="65366-238">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="65366-239">Amazon</span><span class="sxs-lookup"><span data-stu-id="65366-239">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="65366-240">Azure AD (単一テナント)</span><span class="sxs-lookup"><span data-stu-id="65366-240">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="65366-241">Microsoft アカウント</span><span class="sxs-lookup"><span data-stu-id="65366-241">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="65366-242">Facebook</span><span class="sxs-lookup"><span data-stu-id="65366-242">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="65366-243">GitHub</span><span class="sxs-lookup"><span data-stu-id="65366-243">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="65366-244">Google</span><span class="sxs-lookup"><span data-stu-id="65366-244">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="65366-245">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="65366-245">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="65366-246">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="65366-246">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="65366-247">Twitter</span><span class="sxs-lookup"><span data-stu-id="65366-247">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="65366-248">ソーシャル ID プロバイダーの追加と設定</span><span class="sxs-lookup"><span data-stu-id="65366-248">Add and set up a social identity provider</span></span>

<span data-ttu-id="65366-249">ソーシャル ID プロバイダーを追加および設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-249">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="65366-250">Azure ポータルで、**ID プロバイダー**に移動します。</span><span class="sxs-lookup"><span data-stu-id="65366-250">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="65366-251">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-251">Select **Add**.</span></span> <span data-ttu-id="65366-252">**ID プロバイダーの追加**画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65366-252">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="65366-253">**名前**に、サインイン画面でユーザーに表示される名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-253">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="65366-254">**ID プロバイダー タイプ**で、リストから ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-254">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="65366-255">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-255">Select **OK**.</span></span>
1. <span data-ttu-id="65366-256">**この ID プロバイダーの設定**を選択して**ソーシャル ID プロバイダー**画面にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="65366-256">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="65366-257">**クライアント ID** で、ID プロバイダー アプリケーションの設定から取得したクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-257">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="65366-258">**クライアント シークレット** で、ID プロバイダー アプリケーションの設定から取得したクライアント シークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-258">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="65366-259">サインイン登録ポリシーのユーザー フローを添付します。</span><span class="sxs-lookup"><span data-stu-id="65366-259">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="65366-260">**Azure AD B2C – ユーザー フロー (ポリシー) \>{サインイン登録ポリシー} \> ID プロバイダー**。</span><span class="sxs-lookup"><span data-stu-id="65366-260">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="65366-261">サインイン/登録のユーザー フロー ポリシーを添付するには、アカウントに対して設定した各 ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-261">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="65366-262">これらをテストするには、各 ID プロバイダーに対して**ユーザー フローを実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-262">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="65366-263">新しいタブには、新しい ID プロバイダーの選択ボックスを表示するログイン ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="65366-263">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="65366-264">次の図は、Azure AD B2C での **ID プロバイダーの追加**および **ソーシャル ID プロバイダーの設定**画面の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-264">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![アプリケーションへのソーシャル ID プロバイダーの追加](./media/B2CImage_14.png)

<span data-ttu-id="65366-266">次の図は、Azure AD B2C **ID プロバイダー** ページで ID プロバイダーを選択する方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-266">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![各ソーシャル ID プロバイダーを選択して、ポリシーを有効にする](./media/B2CImage_16.png)

<span data-ttu-id="65366-268">次の図は、ソーシャル ID プロバイダーのサインイン ボタンが表示された既定のサインイン画面の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-268">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![ソーシャル ID プロバイダーのサインイン ボタンが表示された既定のログイン画面の例](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="65366-270">新しい Azure AD B2C 情報でコマース本社を更新する</span><span class="sxs-lookup"><span data-stu-id="65366-270">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="65366-271">上記の Azure AD B2C プロビジョニングの手順が完了したら、Azure AD B2C アプリケーションをDynamics 365 Commerce 環境に登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-271">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="65366-272">新しい Azure AD B2C 情報を使用して本社を更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-272">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="65366-273">コマースで、**コマース共有パラメーター**を開いて、左側のメニューで **ID プロバイダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-273">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="65366-274">**ID プロバイダー**で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="65366-274">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="65366-275">**発行者**ボックスに、ID プロバイダー発行者 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-275">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="65366-276">発行者 URL については、下記の[発行者 URL を取得する](#obtain-issuer-url)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65366-276">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="65366-277">**名前**ボックスに、発行者レコードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-277">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="65366-278">**タイプ** ボックスに、**Azure AD B2C (id_token)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-278">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="65366-279">**依存する関係者**で、上記の B2C ID プロバイダー品目を選択した状態で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="65366-279">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="65366-280">**ClientID** ボックスに B2C アプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-280">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="65366-281">これは、B2C アプリケーションのプロパティ ページの**アプリケーション ID** ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="65366-281">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="65366-282">**タイプ** ボックスに**公的** と入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-282">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="65366-283">**ユーザー タイプ** ボックスに**顧客**と入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-283">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="65366-284">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-284">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="65366-285">コマースの検索ボックスで、**番号順序** (組織管理 > 番号順序) を検索します。</span><span class="sxs-lookup"><span data-stu-id="65366-285">In the Commerce search box, search for **Number sequences** (Organization administration > Number sequences).</span></span>
1. <span data-ttu-id="65366-286">アクション ウィンドウで、**管理**の下にある**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-286">Under the action pane, select **Edit** under **Maintain**.</span></span>
1. <span data-ttu-id="65366-287">**全般**クイック タブで、**いいえ**を選択して**手動**にします。</span><span class="sxs-lookup"><span data-stu-id="65366-287">On the **General** fast tab, select **No** for **Manual**.</span></span>
1. <span data-ttu-id="65366-288">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-288">On the action pane, select **Save**.</span></span> 
1. <span data-ttu-id="65366-289">コマース検索ボックスで、**配送スケジュール**を検索する</span><span class="sxs-lookup"><span data-stu-id="65366-289">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="65366-290">**配送スケジュール** ページの左のナビゲーション メニューで、ジョブ **1110 グローバル コンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-290">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="65366-291">アクション ウィンドウで、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-291">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="65366-292">発行者 URL の取得</span><span class="sxs-lookup"><span data-stu-id="65366-292">Obtain issuer URL</span></span>

<span data-ttu-id="65366-293">ID プロバイダー発行者 URL を取得するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-293">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="65366-294">B2C テナントとポリシーを使用して、次の形式でメタデータ アドレスの URL を作成します。``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="65366-294">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="65366-295">例: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``。</span><span class="sxs-lookup"><span data-stu-id="65366-295">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="65366-296">メタデータ アドレス URL をブラウザーのアドレス バーに入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-296">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="65366-297">メタデータで、ID プロバイダー発行者 URL (**発行者**の値) をコピーします。</span><span class="sxs-lookup"><span data-stu-id="65366-297">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="65366-298">例: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``。</span><span class="sxs-lookup"><span data-stu-id="65366-298">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="65366-299">コマース サイト ビルダーでの B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65366-299">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="65366-300">Azure AD B2C テナントの設定が完了したら、コマース サイト ビルダーで B2C テナントをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-300">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="65366-301">構成手順には、Azure ポータルから B2C アプリケーション情報を収集し、B2C アプリケーション情報をサイト ビルダーに入力してから、B2C アプリケーションをサイトおよびチャンネルに関連付けることが含まれます。</span><span class="sxs-lookup"><span data-stu-id="65366-301">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="65366-302">必要なアプリケーション情報の収集</span><span class="sxs-lookup"><span data-stu-id="65366-302">Collect the required application information</span></span>

<span data-ttu-id="65366-303">必要なアプリケーション情報を収集するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-303">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="65366-304">Azure ポータルで、**ホーム \> Azure AD B2C - アプリケーション**に移動します。</span><span class="sxs-lookup"><span data-stu-id="65366-304">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="65366-305">アプリケーションを選択し、左側のナビゲーション ウィンドウで**プロパティ**を選択して、アプリケーションの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="65366-305">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="65366-306">**アプリケーション ID** ボックスで、B2C テナントで作成した B2C アプリケーションのアプリケーション ID を収集します。</span><span class="sxs-lookup"><span data-stu-id="65366-306">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="65366-307">これは、後に**クライアント GUID** としてサイト ビルダーに入力されます。</span><span class="sxs-lookup"><span data-stu-id="65366-307">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="65366-308">**返信 URL** で、返信 URL を収集します。</span><span class="sxs-lookup"><span data-stu-id="65366-308">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="65366-309">**ホーム \> Azure AD B2C – ユーザー フロー (ポリシー)** に移動して、各ユーザー フロー ポリシーの名前を収集します。</span><span class="sxs-lookup"><span data-stu-id="65366-309">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="65366-310">次の図は、**Azure AD B2C - アプリケーション** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-310">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![テナント内の B2C アプリケーションに移動する](./media/B2CImage_19.png)

<span data-ttu-id="65366-312">次の図は、Azure AD B2C におけるアプリケーション **プロパティ** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-312">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![B2C アプリケーションのプロパティからアプリケーション ID をコピーする](./media/B2CImage_21.png)

<span data-ttu-id="65366-314">次の図は、**Azure AD B2C – ユーザー フロー (ポリシー)** ページのユーザー フロー ポリシーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="65366-314">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![各 B2C ポリシー フローの名前の収集](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="65366-316">コマースに AAD B2C テナント アプリケーションの情報を入力する</span><span class="sxs-lookup"><span data-stu-id="65366-316">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="65366-317">B2C テナントをサイトに関連付ける前に、Azure AD B2C テナントの詳細をコマース サイト ビルダーに入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-317">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="65366-318">AAD B2C テナント アプリケーションの情報をコマースに追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-318">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="65366-319">環境のコマース サイト ビルダーに管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="65366-319">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="65366-320">左のナビゲーション ウィンドウで、**テナント設定**を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="65366-320">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="65366-321">**テナントの設定**で、**B2C 設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-321">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="65366-322">**B2C アプリケーション**横のメイン ウィンドウで、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-322">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="65366-323">(B2Cアプリケーション リストにテナントが表示されている場合は、管理者によってテナントが既に追加されています。</span><span class="sxs-lookup"><span data-stu-id="65366-323">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="65366-324">次の手順 6 の項目が B2C アプリケーションと一致していることを確認します。)</span><span class="sxs-lookup"><span data-stu-id="65366-324">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="65366-325">**B2C アプリケーションの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-325">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="65366-326">B2C テナントおよびアプリケーションの値を使用して、表示されたフォームに次の必須項目を入力します。</span><span class="sxs-lookup"><span data-stu-id="65366-326">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="65366-327">必須ではない (アスタリスクが付いていない) フィールドは空白のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="65366-327">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="65366-328">**アプリケーション名**: B2C アプリケーションの名前。たとえば「Fabrikam B2C」のようになります。</span><span class="sxs-lookup"><span data-stu-id="65366-328">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="65366-329">**テナント名**: B2C テナントの名前。たとえば「Fabrikam」のようになります。</span><span class="sxs-lookup"><span data-stu-id="65366-329">**Tenant Name**: The name of your B2C Tenant, for example "Fabrikam".</span></span>
    - <span data-ttu-id="65366-330">**パスワードを忘れた場合のポリシー ID**: パスワードを忘れた場合のユーザー フロー ポリシー ID。たとえば「B2C_1_PasswordReset」のようになります。</span><span class="sxs-lookup"><span data-stu-id="65366-330">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="65366-331">**登録サインイン ポリシー ID**: 登録およびサインインのユーザー ポリシー ID。たとえば「B2C_1_signup_signin」のようになります。</span><span class="sxs-lookup"><span data-stu-id="65366-331">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="65366-332">**クライアント GUID**: B2C アプリケーション ID。たとえば「22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6」のようになります。</span><span class="sxs-lookup"><span data-stu-id="65366-332">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="65366-333">**プロファイル ポリシー編集 ID**: プロファイル編集ユーザー フロー ポリシー ID。たとえば「B2C_1A_ProfileEdit」のようになります。</span><span class="sxs-lookup"><span data-stu-id="65366-333">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="65366-334">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-334">Select **OK**.</span></span> <span data-ttu-id="65366-335">B2C アプリケーションの名前が一覧に表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="65366-335">You should now see the name of your B2C application appear in the list.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="65366-336">B2C アプリケーションをサイトとチャンネルに関連付ける</span><span class="sxs-lookup"><span data-stu-id="65366-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="65366-337">B2C アプリケーションが既にサイトに関連付けられている場合は、別の B2C アプリケーションに変更すると、この環境で既に登録したユーザーに対して設定されている現在の参照が削除されます。</span><span class="sxs-lookup"><span data-stu-id="65366-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="65366-338">変更された場合、現在割り当てられている B2C アプリケーションに関連付けられている資格情報は、ユーザーが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="65366-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="65366-339">B2C アプリケーションを更新するのは、チャンネルの B2C アプリケーションを初めて設定する場合か、ユーザーが新しい B2C アプリケーションでこのチャンネルに新しい資格情報を再登録する場合のみです。</span><span class="sxs-lookup"><span data-stu-id="65366-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="65366-340">B2C アプリケーションにチャンネルを関連付ける際には注意が必要です。また、アプリケーションに明確な名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="65366-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="65366-341">次の手順でチャンネルが B2C アプリケーションに関連付けられていない場合は、サイトでそのチャンネルにサインインしているユーザーは、B2C アプリケーションの**テナント設定\> B2C 設定**リストで**既定**として表示される B2C アプリケーションに入力されます。</span><span class="sxs-lookup"><span data-stu-id="65366-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="65366-342">B2C アプリケーションをサイトとチャンネルに関連付けるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65366-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="65366-343">コマース サイト ビルダーでサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="65366-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="65366-344">左のナビゲーション ウィンドウで、**サイト設定**を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="65366-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="65366-345">**サイトの設定**で、**チャンネル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="65366-346">**チャンネル**のメイン ウィンドウで、チャンネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="65366-347">右側のチャンネルのプロパティ ウィンドウで、**B2C アプリケーションの選択**ドロップダウン メニューから B2C アプリケーション名を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="65366-348">**閉じる**をクリックし、**保存と公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65366-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="65366-349">B2C 追加情報</span><span class="sxs-lookup"><span data-stu-id="65366-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="65366-350">顧客の移行</span><span class="sxs-lookup"><span data-stu-id="65366-350">Customer migration</span></span>

<span data-ttu-id="65366-351">以前の ID プロバイダー プラットフォームからの顧客レコードの移行を検討している場合は、Dynamics 365 Commerce チームと協力して、顧客移行のニーズを確認してください。</span><span class="sxs-lookup"><span data-stu-id="65366-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="65366-352">顧客の移行に関する Azure AD B2C 追加ドキュメントについては、[Azure Active Directory B2C へのユーザー移行](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65366-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="65366-353">カスタム ポリシー</span><span class="sxs-lookup"><span data-stu-id="65366-353">Custom policies</span></span>

<span data-ttu-id="65366-354">Azure AD B2C の操作および B2C 標準ポリシーで提供されるものを超えるポリシー フローのカスタマイズに関する追加情報については、[Azure Active Directory B2C のカスタム ポリシー](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65366-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="65366-355">二次管理者</span><span class="sxs-lookup"><span data-stu-id="65366-355">Secondary admin</span></span>

<span data-ttu-id="65366-356">B2C テナントの**ユーザー** セクションには、オプションで二次管理者アカウントを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="65366-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="65366-357">これは、直接アカウントまたは一般アカウントにすることができます。</span><span class="sxs-lookup"><span data-stu-id="65366-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="65366-358">チーム リソース間でアカウントを共有する必要がある場合は、共通のアカウントも作成できます。</span><span class="sxs-lookup"><span data-stu-id="65366-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="65366-359">Azure AD B2C に保管されるデータの機密性のため、共通アカウントは会社のセキュリティ慣行に従って綿密に監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65366-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65366-360">追加リソース</span><span class="sxs-lookup"><span data-stu-id="65366-360">Additional resources</span></span>

[<span data-ttu-id="65366-361">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65366-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="65366-362">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="65366-362">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="65366-363">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="65366-363">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="65366-364">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="65366-364">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="65366-365">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="65366-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="65366-366">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="65366-366">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="65366-367">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="65366-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="65366-368">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65366-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="65366-369">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="65366-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="65366-370">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="65366-370">Enable location-based store detection</span></span>](enable-store-detection.md)