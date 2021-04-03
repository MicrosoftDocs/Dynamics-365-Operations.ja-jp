---
title: ユーザーのサインインに対するカスタム ページの設定
description: このトピックでは Microsoft Dynamics 365 Commerce で、Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントのユーザー向けにカスタマイズされたサインインを処理するカスタム ページを構築する方法について説明します。
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477951"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="84683-103">ユーザーのサインインに対するカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="84683-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84683-104">このトピックでは Microsoft Dynamics 365 Commerce で、Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントのユーザー向けにカスタマイズされたサインインを処理するカスタム ページを構築する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84683-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="84683-105">Dynamics 365 Commerce で作成されたカスタム ページを利用してユーザー サインイン フローを処理するには、コマース環境で参照される Azure AD ポリシーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84683-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="84683-106">Azure AD B2C アプリケーションを使用して、「登録してサインイン」、「プロファイル編集」、および「パスワード リセット」 Azure AD B2C ポリシーをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="84683-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="84683-107">その後、Microsoft Dynamics Lifecycle Services (LCS) を使用してコマース環境で実行されるプロビジョニング プロセス中に、Azure AD B2C テナントとポリシー名を参照できます。</span><span class="sxs-lookup"><span data-stu-id="84683-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="84683-108">カスタム コマース ページは、サインイン、登録、アカウント プロファイル編集、またはパスワード リセット モジュールを使用して構築できます。</span><span class="sxs-lookup"><span data-stu-id="84683-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="84683-109">これらのカスタム ページ用に公開されたページ URL は、Azure ポータルの Azure AD B2C ポリシー コンフィギュレーションで参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84683-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="84683-110">B2C ポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="84683-110">Set up B2C policies</span></span>

<span data-ttu-id="84683-111">Azure AD B2C テナントを設定し、コマース環境に関連付けた後、Azure ポータル **Azure AD B2C** ページに移動し、メニューの **ポリシー** で、**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![メニューのユーザー フロー (ポリシー) コマンド](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="84683-113">「登録してサインイン」、「プロファイル編集」、および「パスワード リセット」 ユーザー サインイン フローをコンフィギュレーションできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="84683-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="84683-114">「登録とサインイン」 ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="84683-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="84683-115">「登録とサインイン」 ポリシーをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="84683-116">**新しいユーザー フロー** を選択し、**推奨** タブで、**登録とサインイン** ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="84683-117">ポリシーの名前を入力します (たとえば、**B2C\_1\_SignInSignUp**)。</span><span class="sxs-lookup"><span data-stu-id="84683-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="84683-118">**ID プロバイダー** セクションで、ポリシーに使用する ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="84683-119">少なくとも、**電子メールの登録** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84683-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="84683-120">**属性の収集** の列で、**電子メール アドレス**、**指定された名前**、および **姓** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="84683-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="84683-121">**返品クレーム** の列で、**電子メール アドレス**、**指定された名前**、**ID プロバイダー**、**姓**、および **ユーザー オブジェクト ID** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="84683-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![選択された属性とクレーム](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="84683-123">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="84683-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="84683-124">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="84683-125">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする** のオプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![新しいポリシーのプロパティ ページ](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="84683-127">ポリシー名は、コマース環境で完全に参照されます。</span><span class="sxs-lookup"><span data-stu-id="84683-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="84683-128">(**B2C\_1\_** の接頭語は参照に含まれます。) 作成したポリシーの名前を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="84683-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="84683-129">既存のコマース環境のポリシーを置き換える場合は、元のポリシーを削除して、同じ名前の新しいポリシーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="84683-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="84683-130">または、環境が既にプロビジョニングされている場合は、サービス要求を通じて新しいポリシー名を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="84683-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="84683-131">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="84683-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="84683-132">ここでは、ポリシーを閉じて、Azure ポータルの **ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="84683-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="84683-133">「プロファイル編集」ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="84683-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="84683-134">「プロファイル編集」をコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="84683-135">**新しいユーザー フロー** を選択し、**推奨** タブで、**プロファイル編集** ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="84683-136">ポリシーの名前を入力します (たとえば、**B2C\_1\_EditProfile**)。</span><span class="sxs-lookup"><span data-stu-id="84683-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="84683-137">**ID プロバイダー** セクションで、ポリシーに使用する ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="84683-138">少なくとも、**ローカル アカウント サインイン** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84683-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="84683-139">**属性の収集** の列で、**電子メール アドレス** および **姓** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="84683-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="84683-140">**返品クレーム** の列で、**電子メール アドレス**、**指定された名前**、**ID プロバイダー**、**姓**、および **ユーザー オブジェクト ID** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="84683-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="84683-141">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="84683-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="84683-142">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="84683-143">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする** のオプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="84683-144">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="84683-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="84683-145">ここでは、ポリシーを閉じて、Azure ポータルの **ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="84683-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="84683-146">「パスワードのリセット」 ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="84683-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="84683-147">「パスワードのリセット」 ポリシーをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="84683-148">**新しいユーザー フロー** を選択し、**プレビュー** タブで、**パスワード リセット v1.1** ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![プレビュー タブで選択されたパスワード リセット v1.1 ポリシー](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="84683-150">ポリシーの名前を入力します (たとえば、**B2C\_1\_ForgetPassword**)。</span><span class="sxs-lookup"><span data-stu-id="84683-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="84683-151">**ID プロバイダー** セクションで、**電子メールアドレスを使用したパスワードのリセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="84683-152">**返品クレーム** の列で、**電子メール アドレス**、**指定された名前**、**姓**、および **ユーザー オブジェクト ID** のチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="84683-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![選択されたクレーム](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="84683-154">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="84683-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="84683-155">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="84683-156">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする** のオプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="84683-157">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="84683-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="84683-158">ここでは、ポリシーを閉じて、Azure ポータルの **ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="84683-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="84683-159">カスタム ページの構築</span><span class="sxs-lookup"><span data-stu-id="84683-159">Build the custom pages</span></span>

<span data-ttu-id="84683-160">ユーザーのサインインを処理するカスタム ページを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="84683-161">コマース作成ツールでサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="84683-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="84683-162">次の 5 つのテンプレートと 5 ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="84683-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="84683-163">サインイン モジュールを使用する **サインイン** テンプレートおよびページ。</span><span class="sxs-lookup"><span data-stu-id="84683-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="84683-164">登録モジュールを使用する **登録** テンプレートおよびページ。</span><span class="sxs-lookup"><span data-stu-id="84683-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="84683-165">パスワード リセット モジュールを使用する **パスワードのリセット** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="84683-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="84683-166">パスワード リセット検証モジュールを使用する **パスワードのリセット検証** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="84683-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="84683-167">アカウント プロファイルの編集モジュールを使用する **プロファイル編集** テンプレートとページ</span><span class="sxs-lookup"><span data-stu-id="84683-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="84683-168">プロパティを作成するときは、次のガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="84683-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="84683-169">各ページまたは各モジュールについて、ビジネス要件に最も適したレイアウトとスタイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="84683-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="84683-170">Azure AD B2C の設定で使用する必要があるすべてのページと URL を公開します。</span><span class="sxs-lookup"><span data-stu-id="84683-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="84683-171">ページと URL を公開した後、Azure AD B2C ポリシーのコンフィギュレーションに使用する必要がある URL を収集します。</span><span class="sxs-lookup"><span data-stu-id="84683-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="84683-172">**?preloadscripts=true** 接尾語は、使用時にすべての URL に追加されます。</span><span class="sxs-lookup"><span data-stu-id="84683-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84683-173">相対リンクが設定されている汎用のヘッダーおよびフッターを再利用しないようにします。</span><span class="sxs-lookup"><span data-stu-id="84683-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="84683-174">これらのページは、使用時に Azure AD B2C ドメインでホストされるので、すべてのリンクに対して絶対 URL を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84683-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="84683-175">カスタム ページ情報を使用して、Azure AD B2C ポリシーをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="84683-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="84683-176">Azure ポータルで、**Azure AD B2C** ページに戻り、メニューの **ポリシー** で、**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="84683-177">カスタム ページ情報で「登録とサインイン」 ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="84683-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="84683-178">カスタム ページ情報で「登録とサインイン」 ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="84683-179">以前にコンフィギュレーションした **サインインと登録** ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="84683-180">**統一登録またはサインインのページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="84683-181">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="84683-182">**カスタム ページのURI** フィールドに、完全なサインイン URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="84683-183">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="84683-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="84683-184">たとえば、「``www.<my domain>.com/sign-in?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="84683-185">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="84683-186">**ローカル アカウントの登録ページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="84683-187">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="84683-188">**カスタム ページの URI** フィールドに、完全なサインアップ URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="84683-189">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="84683-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="84683-190">たとえば、「``www.<my domain>.com/sign-up?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="84683-191">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="84683-192">**ユーザー属性** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="84683-193">**電子メール アドレス**、**指定された名前**、および **姓** の属性に対して、**必要な検証** フィールドで、**いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="84683-194">**指定された名前**、および **姓** の属性に対して、**オプション** フィールドで、**いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![ローカル アカウントの登録ページ ポリシーのコンフィギュレーション](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="84683-196">カスタム ページ情報で「プロファイル編集」ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="84683-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="84683-197">カスタム ページ情報で「プロファイル編集」ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="84683-198">以前にコンフィギュレーションした **プロファイル編集** ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="84683-199">**プロファイル編集ページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="84683-200">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="84683-201">**カスタム ページの URI** フィールドに、完全なプロファイル編集 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="84683-202">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="84683-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="84683-203">たとえば、「``www.<my domain>.com/profile-edit?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="84683-204">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="84683-205">**ユーザー属性** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="84683-206">**電子メールアドレス**、**指定された名前** の属性に対して、**必要な検証** フィールドで **いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="84683-207">**指定された名前**、および **姓** の属性に対して、**オプション** フィールドで、**いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="84683-208">カスタム ページ情報で「パスワードのリセット」 ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="84683-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="84683-209">カスタム ページ情報で「パスワードのリセット」 ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="84683-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="84683-210">以前にコンフィギュレーションした **パスワードのリセット** ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="84683-211">**新しいパスワード ページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="84683-212">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="84683-213">**カスタム ページの URI** フィールドに、完全なパスワード リセット URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="84683-214">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="84683-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="84683-215">たとえば、「``www.<my domain>.com/passwordreset?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="84683-216">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="84683-217">**アカウントの検証ページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="84683-218">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="84683-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="84683-219">**カスタム ページの URI** フィールドに、完全なパスワード リセット検証 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="84683-220">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="84683-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="84683-221">たとえば、「``www.<my domain>.com/passwordreset-verification?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="84683-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="84683-222">**ページ レイアウト バージョン (プレビュー)** フィールドで、**1.2.0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84683-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="84683-223">ラベルと説明の既定のテキスト文字列のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="84683-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="84683-224">モジュール ライブラリでは、サインイン モジュールにはラベルと説明の既定のテキスト文字列が事前に入力されています。</span><span class="sxs-lookup"><span data-stu-id="84683-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="84683-225">サインイン モジュールの global.json ファイルの値を更新することにより、ソフトウェア開発キット (SDK) でこれらの文字列をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="84683-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="84683-226">たとえば、パスワード リンクを忘れた場合の既定のテキストは **パスワードをお忘れですか** です。</span><span class="sxs-lookup"><span data-stu-id="84683-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="84683-227">以下は、サインイン ページに表示される既定のテキストを示しています。</span><span class="sxs-lookup"><span data-stu-id="84683-227">The following shows this default text on the sign-in page.</span></span>

![サインイン ページでパスワード リンクを忘れた場合の既定のテキスト](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="84683-229">ただし、モジュール ライブラリ サインイン モジュールの global.json ファイルでは、次の図に示すように、**パスワードをお忘れですか？** のテキストを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="84683-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![サインイン モジュール global.json ファイルの更新されたリンク テキスト](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="84683-231">global.json ファイルを更新して変更内容を公開すると、コマースとライブ サインイン ページの両方のサイン イン モジュールに新しいリンク テキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="84683-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84683-232">追加リソース</span><span class="sxs-lookup"><span data-stu-id="84683-232">Additional resources</span></span>

[<span data-ttu-id="84683-233">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="84683-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="84683-234">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="84683-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="84683-235">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="84683-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="84683-236">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="84683-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="84683-237">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="84683-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="84683-238">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="84683-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="84683-239">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="84683-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="84683-240">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="84683-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="84683-241">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="84683-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="84683-242">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="84683-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
