---
title: ユーザーのサインインに対するカスタム ページの設定
description: このトピックでは Microsoft Dynamics 365 Commerce で、Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントのユーザー向けにカスタマイズされたサインインを処理するカスタム ページを構築する方法について説明します。
author: brianshook
manager: annbe
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 20bfacbc2374003814e12e7737644d118d404cc0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945562"
---
# <a name="set-up-custom-pages-for-user-logins"></a><span data-ttu-id="e8021-103">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="e8021-103">Set up custom pages for user logins</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e8021-104">このトピックでは Microsoft Dynamics 365 Commerce で、Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントのユーザー向けにカスタマイズされたサインインを処理するカスタム ページを構築する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8021-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="e8021-105">概要</span><span class="sxs-lookup"><span data-stu-id="e8021-105">Overview</span></span>

<span data-ttu-id="e8021-106">Dynamics 365 Commerce で作成されたカスタム ページを利用してユーザー サインイン フローを処理するには、コマース環境で参照される Azure AD ポリシーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8021-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="e8021-107">Azure AD B2C アプリケーションを使用して、「登録してサインイン」、「プロファイル編集」、および「パスワード リセット」 Azure AD B2C ポリシーをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="e8021-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="e8021-108">その後、Microsoft Dynamics Lifecycle Services (LCS) を使用してコマース環境で実行されるプロビジョニング プロセス中に、Azure AD B2C テナントとポリシー名を参照できます。</span><span class="sxs-lookup"><span data-stu-id="e8021-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="e8021-109">カスタム コマース ページは、サインイン、登録、アカウント プロファイル編集、またはパスワード リセット モジュールを使用して構築できます。</span><span class="sxs-lookup"><span data-stu-id="e8021-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="e8021-110">これらのカスタム ページ用に公開されたページ URL は、Azure ポータルの Azure AD B2C ポリシー コンフィギュレーションで参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8021-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="e8021-111">B2C ポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="e8021-111">Set up B2C policies</span></span>

<span data-ttu-id="e8021-112">Azure AD B2C テナントを設定し、コマース環境に関連付けた後、Azure ポータル **Azure AD B2C** ページに移動し、メニューの**ポリシー**で、**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![メニューのユーザー フロー (ポリシー) コマンド](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="e8021-114">「登録してサインイン」、「プロファイル編集」、および「パスワード リセット」 ユーザー サインイン フローをコンフィギュレーションできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e8021-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="e8021-115">「登録とサインイン」 ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e8021-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="e8021-116">「登録とサインイン」 ポリシーをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="e8021-117">**新しいユーザー フロー**を選択し、**推奨**タブで、**登録とサインイン** ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="e8021-118">ポリシーの名前を入力します (たとえば、**B2C\_1\_SignInSignUp**)。</span><span class="sxs-lookup"><span data-stu-id="e8021-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="e8021-119">**ID プロバイダー** セクションで、ポリシーに使用する ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e8021-120">少なくとも、**電子メールの登録**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8021-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="e8021-121">**属性の収集**の列で、**電子メール アドレス**、**指定された名前**、および**姓**のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e8021-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="e8021-122">**返品クレーム**の列で、**電子メール アドレス**、**指定された名前**、**ID プロバイダー**、**姓**、および**ユーザー オブジェクト ID**のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e8021-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![選択された属性とクレーム](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="e8021-124">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8021-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e8021-125">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e8021-126">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする**のオプションを**オン**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![新しいポリシーのプロパティ ページ](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="e8021-128">ポリシー名は、コマース環境で完全に参照されます。</span><span class="sxs-lookup"><span data-stu-id="e8021-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="e8021-129">(**B2C\_1\_** の接頭語は参照に含まれます。) 作成したポリシーの名前を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="e8021-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="e8021-130">既存のコマース環境のポリシーを置き換える場合は、元のポリシーを削除して、同じ名前の新しいポリシーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e8021-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="e8021-131">または、環境が既にプロビジョニングされている場合は、サービス要求を通じて新しいポリシー名を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="e8021-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="e8021-132">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="e8021-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e8021-133">ここでは、ポリシーを閉じて、Azure ポータルの**ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e8021-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="e8021-134">「プロファイル編集」ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e8021-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="e8021-135">「プロファイル編集」をコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="e8021-136">**新しいユーザー フロー**を選択し、**推奨**タブで、**プロファイル編集**ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="e8021-137">ポリシーの名前を入力します (たとえば、**B2C\_1\_EditProfile**)。</span><span class="sxs-lookup"><span data-stu-id="e8021-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="e8021-138">**ID プロバイダー** セクションで、ポリシーに使用する ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e8021-139">少なくとも、**ローカル アカウント サインイン**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8021-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="e8021-140">**属性の収集**の列で、**電子メール アドレス**および**姓**のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e8021-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="e8021-141">**返品クレーム**の列で、**電子メール アドレス**、**指定された名前**、**ID プロバイダー**、**姓**、および**ユーザー オブジェクト ID**のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e8021-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="e8021-142">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8021-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e8021-143">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e8021-144">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする**のオプションを**オン**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e8021-145">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="e8021-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e8021-146">ここでは、ポリシーを閉じて、Azure ポータルの**ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e8021-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="e8021-147">「パスワードのリセット」 ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e8021-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="e8021-148">「パスワードのリセット」 ポリシーをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="e8021-149">**新しいユーザー フロー**を選択し、**プレビュー** タブで、**パスワード リセット v1.1** ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![プレビュー タブで選択されたパスワード リセット v1.1 ポリシー](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="e8021-151">ポリシーの名前を入力します (たとえば、**B2C\_1\_ForgetPassword**)。</span><span class="sxs-lookup"><span data-stu-id="e8021-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="e8021-152">**ID プロバイダー** セクションで、**電子メールアドレスを使用したパスワードのリセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="e8021-153">**返品クレーム**の列で、**電子メール アドレス**、**指定された名前**、**姓**、および**ユーザー オブジェクト ID** のチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e8021-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![選択されたクレーム](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="e8021-155">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8021-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e8021-156">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e8021-157">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする**のオプションを**オン**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e8021-158">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="e8021-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e8021-159">ここでは、ポリシーを閉じて、Azure ポータルの**ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e8021-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="e8021-160">カスタム ページの構築</span><span class="sxs-lookup"><span data-stu-id="e8021-160">Build the custom pages</span></span>

<span data-ttu-id="e8021-161">ユーザーのサインインを処理するカスタム ページを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="e8021-162">コマース作成ツールでサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="e8021-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="e8021-163">次の 5 つのテンプレートと 5 ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8021-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="e8021-164">サインイン モジュールを使用する**サインイン** テンプレートおよびページ。</span><span class="sxs-lookup"><span data-stu-id="e8021-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="e8021-165">登録モジュールを使用する**登録**テンプレートおよびページ。</span><span class="sxs-lookup"><span data-stu-id="e8021-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="e8021-166">パスワード リセット モジュールを使用する**パスワードのリセット** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="e8021-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="e8021-167">パスワード リセット検証モジュールを使用する**パスワードのリセット検証**テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="e8021-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="e8021-168">アカウント プロファイルの編集モジュールを使用する**プロファイル編集**テンプレートとページ</span><span class="sxs-lookup"><span data-stu-id="e8021-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="e8021-169">プロパティを作成するときは、次のガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="e8021-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="e8021-170">各ページまたは各モジュールについて、ビジネス要件に最も適したレイアウトとスタイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e8021-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="e8021-171">Azure AD B2C の設定で使用する必要があるすべてのページと URL を公開します。</span><span class="sxs-lookup"><span data-stu-id="e8021-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="e8021-172">ページと URL を公開した後、Azure AD B2C ポリシーのコンフィギュレーションに使用する必要がある URL を収集します。</span><span class="sxs-lookup"><span data-stu-id="e8021-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="e8021-173">**?preloadscripts=true** 接尾語は、使用時にすべての URL に追加されます。</span><span class="sxs-lookup"><span data-stu-id="e8021-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8021-174">相対リンクが設定されている汎用のヘッダーおよびフッターを再利用しないようにします。</span><span class="sxs-lookup"><span data-stu-id="e8021-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="e8021-175">これらのページは、使用時に Azure AD B2C ドメインでホストされるので、すべてのリンクに対して絶対 URL を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8021-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="e8021-176">カスタム ページ情報を使用して、Azure AD B2C ポリシーをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="e8021-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="e8021-177">Azure ポータルで、**Azure AD B2C** ページに戻り、メニューの**ポリシー**で、**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="e8021-178">カスタム ページ情報で「登録とサインイン」 ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="e8021-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="e8021-179">カスタム ページ情報で「登録とサインイン」 ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e8021-180">以前にコンフィギュレーションした**サインインと登録**ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e8021-181">**統一登録またはサインインのページ**のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="e8021-182">**カスタム ページ コンテンツの使用**オプションを、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e8021-183">**カスタム ページのURI** フィールドに、完全なサインイン URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="e8021-184">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e8021-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e8021-185">たとえば、「``www.<my domain>.com/sign-in?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e8021-186">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e8021-187">**ローカル アカウントの登録ページ**のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="e8021-188">**カスタム ページ コンテンツの使用**オプションを、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e8021-189">**カスタム ページの URI** フィールドに、完全なサインアップ URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="e8021-190">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e8021-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e8021-191">たとえば、「``www.<my domain>.com/sign-up?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e8021-192">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e8021-193">**ユーザー属性** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="e8021-194">**電子メール アドレス**、**指定された名前**、および**姓**の属性に対して、**必要な検証**フィールドで、**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="e8021-195">**指定された名前**、および**姓**の属性に対して、**オプション** フィールドで、**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![ローカル アカウントの登録ページ ポリシーのコンフィギュレーション](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="e8021-197">カスタム ページ情報で「プロファイル編集」ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="e8021-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="e8021-198">カスタム ページ情報で「プロファイル編集」ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e8021-199">以前にコンフィギュレーションした**プロファイル編集**ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e8021-200">**プロファイル編集ページ**のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="e8021-201">**カスタム ページ コンテンツの使用**オプションを、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e8021-202">**カスタム ページの URI** フィールドに、完全なプロファイル編集 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="e8021-203">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e8021-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e8021-204">たとえば、「``www.<my domain>.com/profile-edit?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e8021-205">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e8021-206">**ユーザー属性** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="e8021-207">**電子メールアドレス**、**指定された名前**の属性に対して、**必要な検証**フィールドで**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="e8021-208">**指定された名前**、および**姓**の属性に対して、**オプション** フィールドで、**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="e8021-209">カスタム ページ情報で「パスワードのリセット」 ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="e8021-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="e8021-210">カスタム ページ情報で「パスワードのリセット」 ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8021-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e8021-211">以前にコンフィギュレーションした**パスワードのリセット** ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e8021-212">**新しいパスワード ページ**のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="e8021-213">**カスタム ページ コンテンツの使用**オプションを、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e8021-214">**カスタム ページの URI** フィールドに、完全なパスワード リセット URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="e8021-215">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e8021-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e8021-216">たとえば、「``www.<my domain>.com/passwordreset?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e8021-217">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e8021-218">**アカウントの検証ページ**のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="e8021-219">**カスタム ページ コンテンツの使用**オプションを、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8021-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e8021-220">**カスタム ページの URI** フィールドに、完全なパスワード リセット検証 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="e8021-221">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e8021-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e8021-222">たとえば、「``www.<my domain>.com/passwordreset-verification?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8021-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e8021-223">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8021-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="e8021-224">ラベルと説明の既定のテキスト文字列のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="e8021-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="e8021-225">スターター キットでは、サインイン モジュールにはラベルと説明の既定のテキスト文字列が事前に入力されています。</span><span class="sxs-lookup"><span data-stu-id="e8021-225">In the starter kit, sign in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="e8021-226">サインイン モジュールの global.json ファイルの値を更新することにより、ソフトウェア開発キット (SDK) でこれらの文字列をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="e8021-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="e8021-227">たとえば、パスワード リンクを忘れた場合の既定のテキストは**パスワードをお忘れですか**です。</span><span class="sxs-lookup"><span data-stu-id="e8021-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="e8021-228">以下は、サインイン ページに表示される既定のテキストを示しています。</span><span class="sxs-lookup"><span data-stu-id="e8021-228">The following shows this default text on the sign-in page.</span></span>

![サインイン ページでパスワード リンクを忘れた場合の既定のテキスト](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="e8021-230">ただし、スタート キット サインイン モジュールの global.json ファイルでは、次の図に示すように、**パスワードをお忘れですか**にテキストを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="e8021-230">However, in the global.json file for the starter kit sign in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![サインイン モジュール global.json ファイルの更新されたリンク テキスト](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="e8021-232">global.json ファイルを更新して変更内容を公開すると、コマースとライブ サインイン ページの両方のサインイン モジュールに新しいリンク テキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8021-232">After you update the global.json file and publish your changes, the new link text appears in the sign in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8021-233">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e8021-233">Additional resources</span></span>

[<span data-ttu-id="e8021-234">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e8021-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e8021-235">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="e8021-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e8021-236">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="e8021-236">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e8021-237">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="e8021-237">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e8021-238">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="e8021-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e8021-239">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="e8021-239">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e8021-240">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="e8021-240">Enable location-based store detection</span></span>](enable-store-detection.md)