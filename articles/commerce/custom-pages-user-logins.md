---
title: ユーザーのサインインに対するカスタム ページの設定
description: このトピックでは Microsoft Dynamics 365 Commerce で、Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントのユーザー向けにカスタマイズされたサインインを処理するカスタム ページを構築する方法について説明します。
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d4a1c2f45d77c3ff9a7bb4dffaf12d877dc04e69
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936783"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="e80d6-103">ユーザーのサインインに対するカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="e80d6-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e80d6-104">このトピックでは Microsoft Dynamics 365 Commerce で、Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントのユーザー向けにカスタマイズされたサインインを処理するカスタム ページを構築する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="e80d6-105">Dynamics 365 Commerce で作成されたカスタム ページを利用してユーザー サインイン フローを処理するには、コマース環境で参照される Azure AD ポリシーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="e80d6-106">Azure AD B2C アプリケーションを使用して、「登録してサインイン」、「プロファイル編集」、および「パスワード リセット」 Azure AD B2C ポリシーをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="e80d6-107">その後、Microsoft Dynamics Lifecycle Services (LCS) を使用してコマース環境で実行されるプロビジョニング プロセス中に、Azure AD B2C テナントとポリシー名を参照できます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="e80d6-108">カスタム Commerce ページは、サインイン、登録、アカウント プロファイル編集、パスワード リセット、汎用の AAD モジュールを使用して構築できます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, password reset, or generic AAD modules.</span></span> <span data-ttu-id="e80d6-109">これらのカスタム ページ用に公開されたページ URL は、Azure ポータルの Azure AD B2C ポリシー コンフィギュレーションで参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

> [!WARNING] 
> <span data-ttu-id="e80d6-110">Azure AD B2C は、2021 年 8 月 1 日までに古い (レガシ) ユーザー フローを破棄します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-110">Azure AD B2C will retire old (legacy) user flows by August 1, 2021.</span></span> <span data-ttu-id="e80d6-111">したがって、ユーザー フローを新しい推奨バージョンに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-111">Therefore, you should plan to migrate your user flows to the new recommended version.</span></span> <span data-ttu-id="e80d6-112">新しいバージョンでは、機能パリティと新しい機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-112">The new version provides feature parity and new features.</span></span> <span data-ttu-id="e80d6-113">詳細については、[Azure Active Directory B2C のユーザー フロー](/azure/active-directory-b2c/user-flow-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e80d6-113">For more information, see [User flows in Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).</span></span>

><span data-ttu-id="e80d6-114">推奨される B2C ユーザー フローには、Commerce のバージョン 10.0.15 以上のモジュール ライブラリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-114">The module library for Commerce version 10.0.15 or higher should be used with the recommended B2C user flows.</span></span> <span data-ttu-id="e80d6-115">また、Azure AD B2C で提供されている既定のユーザー ポリシー ページを使用して、企業のブランディングに合わせて背景画像やロゴ、背景色を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-115">The default user policy pages offered in Azure AD B2C can also be used, and allow for added background image, logo, and background color changes related to company branding.</span></span> <span data-ttu-id="e80d6-116">デザインの機能については制限がありますが、既定のユーザー ポリシー ページは、専用のカスタム ページを作成・設定しなくても、Azure AD の B2C ポリシーの機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-116">Though more limited in design capabilities, the default user policy pages provide Azure AD B2C policy functionality without creating and configuring dedicated custom pages.</span></span> 

## <a name="set-up-b2c-policies"></a><span data-ttu-id="e80d6-117">B2C ポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="e80d6-117">Set up B2C policies</span></span>

<span data-ttu-id="e80d6-118">Azure AD B2C テナントを設定し、コマース環境に関連付けた後、Azure ポータル **Azure AD B2C** ページに移動し、メニューの **ポリシー** で、**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-118">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![メニューのユーザー フロー (ポリシー) コマンド](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="e80d6-120">「登録してサインイン」、「プロファイル編集」、および「パスワード リセット」 ユーザー サインイン フローをコンフィギュレーションできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e80d6-120">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="e80d6-121">「登録とサインイン」 ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e80d6-121">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="e80d6-122">「登録とサインイン」 ポリシーをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-122">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="e80d6-123">**新しいユーザー フロー** を選択し、**登録とサインイン** を選択し、**推奨** タブの **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-123">Select **New user flow**, select **Sign up and sign in**, select the **Recommended** tab,  and then select **Create**.</span></span>
1. <span data-ttu-id="e80d6-124">ポリシーの名前を入力します (たとえば、**B2C\_1\_SignInSignUp**)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-124">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="e80d6-125">**ID プロバイダー** セクションで、ポリシーに使用する ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-125">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e80d6-126">少なくとも、**電子メールの登録** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-126">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="e80d6-127">**属性の収集** の列で、**電子メール アドレス**、**指定された名前**、および **姓** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e80d6-127">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="e80d6-128">**返品クレーム** の列で、**電子メール アドレス**、**指定された名前**、**ID プロバイダー**、**姓**、および **ユーザー オブジェクト ID** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e80d6-128">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![選択された属性とクレーム](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="e80d6-130">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-130">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e80d6-131">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-131">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e80d6-132">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする** のオプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-132">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![新しいポリシーのプロパティ ページ](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="e80d6-134">ポリシー名は、コマース環境で完全に参照されます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-134">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="e80d6-135">(**B2C\_1\_** の接頭語は参照に含まれます。) 作成したポリシーの名前を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="e80d6-135">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="e80d6-136">既存のコマース環境のポリシーを置き換える場合は、元のポリシーを削除して、同じ名前の新しいポリシーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-136">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="e80d6-137">または、環境が既にプロビジョニングされている場合は、サービス要求を通じて新しいポリシー名を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-137">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="e80d6-138">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-138">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e80d6-139">ここでは、ポリシーを閉じて、Azure ポータルの **ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-139">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="e80d6-140">「プロファイル編集」ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e80d6-140">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="e80d6-141">「プロファイル編集」をコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-141">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="e80d6-142">**新しいユーザー フロー** を選択し、**プロフィールの設定** を選択し、**推奨** タブの **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-142">Select **New user flow**, select **Profile editing**, select the **Recommended** tab, and then select **Create**.</span></span>
1. <span data-ttu-id="e80d6-143">ポリシーの名前を入力します (たとえば、**B2C\_1\_EditProfile**)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-143">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="e80d6-144">**ID プロバイダー** セクションで、ポリシーに使用する ID プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-144">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e80d6-145">少なくとも、**ローカル アカウント サインイン** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-145">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="e80d6-146">**属性の収集** の列で、**名** と **姓** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e80d6-146">In the **Collect attribute** column, select the check boxes for **Given Name** and **Surname**.</span></span>
1. <span data-ttu-id="e80d6-147">**返品クレーム** の列で、**電子メール アドレス**、**指定された名前**、**ID プロバイダー**、**姓**、および **ユーザー オブジェクト ID** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e80d6-147">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="e80d6-148">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-148">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e80d6-149">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-149">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e80d6-150">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする** のオプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-150">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e80d6-151">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-151">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e80d6-152">ここでは、ポリシーを閉じて、Azure ポータルの **ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-152">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="e80d6-153">「パスワードのリセット」 ポリシーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e80d6-153">Configure the "Password reset" policy</span></span>

<span data-ttu-id="e80d6-154">「パスワードのリセット」 ポリシーをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-154">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="e80d6-155">**新しいユーザー フロー** を選択し、**パスワード リセット オプション** を選択して、**推奨** タブを選択して、**作成** をクリック します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-155">Select **New user flow**, and then select the **Password reset** option, and choose the **Recommended** tab, and click **Create**.</span></span>
1. <span data-ttu-id="e80d6-156">ポリシーの名前を入力します (たとえば、**B2C\_1\_ForgetPassword**)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-156">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="e80d6-157">**ID プロバイダー** セクションで、**電子メールアドレスを使用したパスワードのリセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-157">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="e80d6-158">**返品クレーム** の列で、**電子メール アドレス**、**指定された名前**、**姓**、および **ユーザー オブジェクト ID** のチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e80d6-158">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="e80d6-159">**OK** を選択してポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-159">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e80d6-160">新しいポリシー名をダブルクリックし、ナビゲーション ウィンドウで **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-160">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e80d6-161">**JavaScript を使用したページ レイアウト (プレビュー) を有効にする** のオプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-161">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e80d6-162">カスタム ページを作成した後、このポリシーに戻り設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-162">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e80d6-163">ここでは、ポリシーを閉じて、Azure ポータルの **ユーザー フロー (ポリシー)** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-163">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="e80d6-164">カスタム ページの構築</span><span class="sxs-lookup"><span data-stu-id="e80d6-164">Build the custom pages</span></span>

<span data-ttu-id="e80d6-165">専用の Azure AD モジュールは、Azure AD B2C ユーザー ポリシー用のカスタム ページを作成する Commerce に含まれています。</span><span class="sxs-lookup"><span data-stu-id="e80d6-165">Dedicated Azure AD modules are included in Commerce to build custom pages for Azure AD B2C user policies.</span></span> <span data-ttu-id="e80d6-166">以下の主な Azure AD B2C モジュールを使用して、各ユーザー ポリシー ページのレイアウトに特化したページを構築することができます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-166">Pages can be built specifically for each user policy page's layout using the main Azure AD B2C modules detailed below.</span></span> <span data-ttu-id="e80d6-167">また、**汎用 AAD** モジュールは、 Azure AD B2Cのすべてのページ レイアウトとポリシーに使用することができます (以下に記載されていないポリシー内のページレイアウト オプションにも使用できます)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-167">Alternatively, the **AAD Generic** module can be used for all page layouts and policies in Azure AD B2C (even for page layout options within policies not listed below).</span></span> 

- <span data-ttu-id="e80d6-168">ページ固有の Azure AD のモジュールは、Azure AD の B2C でレンダリングされたデータ入力項目に結合されます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-168">Page-specific Azure AD modules are bound to data input items rendered by Azure AD B2C.</span></span> <span data-ttu-id="e80d6-169">これらのモジュールでは、ページ内の要素の位置をより細かく制御することができます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-169">These modules give you more control over the positioning of the elements in your pages.</span></span> <span data-ttu-id="e80d6-170">しかし、以下に説明する既定の設定以外の差異を考慮して、さらに多くのページやモジュール拡張を構築する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-170">However, more pages and module extensions may need to be built to account for variances beyond the default settings described below.</span></span>
- <span data-ttu-id="e80d6-171">**汎用の AAD** モジュールは、Azure AD B2C 用の "div "要素を作成し、ユーザーポリシーのページレイアウト内のすべての要素をレンダリングします。これにより、ページの B2C 機能に柔軟性が与えられますが、ポジショニングとスタイリングのコントロールは少なくなります (また、CSS は、サイトのルック＆フィールに合わせて使用することができます)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-171">The **AAD Generic** module creates the "div" element for Azure AD B2C to render all elements in the user policy page layout, giving more flexibility to the B2C functions of the page, but less control of the positioning and styling (though CSS can be used to match the look and feel of your site).</span></span>

<span data-ttu-id="e80d6-172">**汎用の AAD** モジュールを使ってひとつのページを作成し、それをすべてのユーザーポリシーページに使用することも、サインイン、サインアップ、プロファイル編集、パスワードリセット、パスワードリセット確認用の各 Azure AD モジュールを使って特定のページを構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-172">You can create a single page with the **AAD Generic** module and use it for all of your user policy pages, or you can build out specific pages using the individual Azure AD modules for sign-in, sign-up, profile edit, password reset, and password reset verification.</span></span> <span data-ttu-id="e80d6-173">また、以下に示すページ レイアウトには特定の Azure AD ページを使用し、これらのページまたは他のユーザーポリシー ページ内の残りのページ レイアウトには汎用の AAD モジュール ページを使用するなど、両方を混在させることも可能です。</span><span class="sxs-lookup"><span data-stu-id="e80d6-173">You may also use a mix of both, using the specific Azure AD pages for the page layouts noted below, and the generic AAD module page for remaining page layouts within these or other user policies pages.</span></span>

<span data-ttu-id="e80d6-174">モジュール ライブラリに同梱されている Azure AD モジュールについては、[アイデンティティ管理のページとモジュール](identity-mgmt-modules.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e80d6-174">To learn more about the Azure AD Modules that ship with the module library, read more at [Identity management pages and modules](identity-mgmt-modules.md).</span></span>

<span data-ttu-id="e80d6-175">ユーザーのサイン インを処理する特定の ID モジュールを持つカスタム ページを構築するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e80d6-175">To build the custom pages with specific identity modules to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="e80d6-176">Commerce サイト ビルダーで、ご利用のサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-176">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="e80d6-177">次の5つのテンプレートとページを作成します (サイトにまだ存在していない場合) :</span><span class="sxs-lookup"><span data-stu-id="e80d6-177">Build the following five templates and pages (if not already present in your site):</span></span>
    - <span data-ttu-id="e80d6-178">サインイン モジュールを使用する **サインイン** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="e80d6-178">A **Sign In** template and page that use the sign-in module.</span></span>
    - <span data-ttu-id="e80d6-179">登録モジュールを使用する **登録** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="e80d6-179">A **Sign Up** template and page that use the sign-up module.</span></span>
    - <span data-ttu-id="e80d6-180">パスワード リセット モジュールを使用する **パスワードのリセット** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="e80d6-180">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="e80d6-181">パスワード リセット検証モジュールを使用する **パスワードのリセット検証** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="e80d6-181">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="e80d6-182">アカウント プロファイルの編集モジュールを使用する **プロファイル編集** テンプレートとページ。</span><span class="sxs-lookup"><span data-stu-id="e80d6-182">A **Profile Edit** template and page that use the account profile edit module.</span></span>

<span data-ttu-id="e80d6-183">プロパティを作成するときは、次のガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="e80d6-183">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="e80d6-184">各ページまたは各モジュールについて、ビジネス要件に最も適したレイアウトとスタイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-184">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="e80d6-185">Azure AD B2C の設定で使用する必要があるすべてのページと URL を公開します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-185">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="e80d6-186">ページと URL を公開した後、Azure AD B2C ポリシーのコンフィギュレーションに使用する必要がある URL を収集します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-186">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="e80d6-187">**?preloadscripts=true** 接尾語は、使用時にすべての URL に追加されます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-187">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e80d6-188">Azure AD の B2C で参照されるように構築されたページは、Azure AD の B2C テナントのドメインから直接提供されます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-188">Pages built to be referenced in Azure AD B2C are served directly from the Azure AD B2C tenant's domain.</span></span> <span data-ttu-id="e80d6-189">相対リンクが設定されている汎用のヘッダーおよびフッターは再利用しないでください。</span><span class="sxs-lookup"><span data-stu-id="e80d6-189">Do not reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="e80d6-190">これらのページは、使用時に Azure AD B2C ドメインでホストされるので、すべてのリンクに対して絶対 URL を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-190">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span> <span data-ttu-id="e80d6-191">Azure AD 関連のカスタム ページは、絶対的な URL で特定のヘッダーとフッターを作成し、Retail サーバーへの接続を必要とする Commerce 固有のモジュールは削除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e80d6-191">It is recommended to create a specific header and footer with absolute URLs for your Azure AD-related custom pages, with any Commerce-specific modules that require connection to Retail Server removed.</span></span> <span data-ttu-id="e80d6-192">たとえば、お気に入り、検索バー、サインイン リンク、カート モジュールは、Azure AD B2C ユーザー フローで使用されるページには含めないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="e80d6-192">For example, the favorites, search bar, sign-in link, and cart modules should not be included in any pages which will be used in Azure AD B2C user flows.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="e80d6-193">カスタム ページ情報を使用して、Azure AD B2C ポリシーをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="e80d6-193">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="e80d6-194">Azure ポータルで、**Azure AD B2C** ページに戻り、メニューの **ポリシー** で、**ユーザー フロー (ポリシー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-194">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="e80d6-195">カスタム ページ情報で「登録とサインイン」 ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="e80d6-195">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="e80d6-196">カスタム ページ情報で「登録とサインイン」 ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-196">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e80d6-197">以前にコンフィギュレーションした **サインインと登録** ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-197">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e80d6-198">**統一登録またはサインインのページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-198">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="e80d6-199">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-199">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e80d6-200">**カスタム ページのURI** フィールドに、完全なサインイン URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-200">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="e80d6-201">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-201">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e80d6-202">たとえば、「``www.<my domain>.com/sign-in?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-202">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e80d6-203">**ページ レイアウト バージョン** フィールドで、バージョン **2.1.0** またはそれ以降を選択します (Commerce バージョン 10.0.15 以上のモジュール ライブラリが必要です)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-203">In the **Page Layout Version** field, select version **2.1.0** or later (requires module library for Commerce version 10.0.15 or higher).</span></span>
1. <span data-ttu-id="e80d6-204">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-204">Select **Save**.</span></span>
1. <span data-ttu-id="e80d6-205">**ローカル アカウントの登録ページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-205">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="e80d6-206">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-206">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e80d6-207">**カスタム ページの URI** フィールドに、完全なサインアップ URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-207">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="e80d6-208">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-208">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e80d6-209">たとえば、「``www.<my domain>.com/sign-up?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-209">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e80d6-210">**ページ レイアウト バージョン** フィールドで、バージョン **2.1.0** またはそれ以降を選択します (Commerce バージョン 10.0.15 以上のモジュール ライブラリが必要です)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-210">In the **Page Layout Version** field, select version **2.1.0** or later (requires module library for Commerce version 10.0.15 or higher).</span></span>
1. <span data-ttu-id="e80d6-211">**ユーザー属性** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-211">In the **User attributes** section, follow these steps:</span></span>
    1. <span data-ttu-id="e80d6-212">**名** と **姓** の属性については、**検証を要求する** 列に **いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-212">For the **Given Name** and **Surname** attributes, select **No** in the **Requires Verification** column.</span></span>
    1. <span data-ttu-id="e80d6-213">**電子メール アドレス** 属性に対しては、**検証を要求する** 列を既定値の **はい** のままにしておくことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-213">For **Email Address** attribute, it is recommended to leave the default value **Yes** selected in the **Requires Verification** column.</span></span> <span data-ttu-id="e80d6-214">このオプションにより、入力されたメール アドレスでサインアップしたユーザーが、そのメール アドレスを所有していることを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-214">This option ensures that users signing up with a given email address verify that they own the email address.</span></span>
    1. <span data-ttu-id="e80d6-215">**電子メール アドレス**、**名**、**姓** の属性に対して、**オプション** 列で、**いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-215">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Optional** column.</span></span>
1. <span data-ttu-id="e80d6-216">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-216">Select **Save**.</span></span>

    ![ローカル アカウントの登録ページ ポリシーの構成](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="e80d6-218">カスタム ページ情報で「プロファイル編集」ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="e80d6-218">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="e80d6-219">カスタム ページ情報で「プロファイル編集」ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-219">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e80d6-220">以前にコンフィギュレーションした **プロファイル編集** ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-220">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e80d6-221">**プロファイル編集 ページ** レイアウトを選択します (画面によっては、下にスクロールして他のレイアウト オプションを表示する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-221">Select the **Profile edit page** layout (may require scrolling down past other layout options, depending on your screen).</span></span>
1. <span data-ttu-id="e80d6-222">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-222">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e80d6-223">**カスタム ページの URI** フィールドに、完全なプロファイル編集 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-223">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="e80d6-224">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-224">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e80d6-225">たとえば、「``www.<my domain>.com/profile-edit?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-225">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e80d6-226">**ページ レイアウト バージョン** に対しては、バージョン **2.1.0** またはそれ以上を選択します (Commerce バージョン 10.0.15 以上のモジュール ライブラリが必要です)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-226">For **Page Layout Version**, select version **2.1.0** or higher (requires module library for Commerce version 10.0.15 or higher).</span></span>
1. <span data-ttu-id="e80d6-227">**ユーザー属性** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-227">In the **User attributes** section, follow these steps:</span></span>
    1. <span data-ttu-id="e80d6-228">**名** と **姓** の属性に対しては、**オプション** 列で、**いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-228">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** column.</span></span>
    1. <span data-ttu-id="e80d6-229">**名** と **姓** の属性については、**検証を要求する** 列に **いいえ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-229">For the **Given Name** and **Surname** attributes, select **No** in the **Requires verification** column.</span></span>
1. <span data-ttu-id="e80d6-230">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-230">Select **Save**.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="e80d6-231">カスタム ページ情報で「パスワードのリセット」 ポリシーを更新する</span><span class="sxs-lookup"><span data-stu-id="e80d6-231">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="e80d6-232">カスタム ページ情報で「パスワードのリセット」 ポリシーを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-232">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e80d6-233">以前にコンフィギュレーションした **パスワードのリセット** ポリシーで、ナビゲーション ウィンドウで、**ページ レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-233">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e80d6-234">**パスワードを忘れた場合のページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-234">Select the **Forgot password page** layout.</span></span>
1. <span data-ttu-id="e80d6-235">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-235">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e80d6-236">**カスタム ページの URI** フィールドに、完全なパスワード リセット検証 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-236">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="e80d6-237">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-237">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e80d6-238">たとえば、「``www.<my domain>.com/password-reset-verification?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-238">For example, enter ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e80d6-239">**ページ レイアウト バージョン** フィールドで、バージョン **2.1.0** またはそれ以上を選択します (Commerce バージョン 10.0.15 以上のモジュール ライブラリが必要です)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-239">In the **Page Layout Version** field, select version **2.1.0** or higher (requires module library for Commerce version 10.0.15 or higher).</span></span>
2. <span data-ttu-id="e80d6-240">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-240">Select **Save**.</span></span>
3. <span data-ttu-id="e80d6-241">**パスワードを変更するページ** のレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-241">Select the **Change password page** layout.</span></span>
4. <span data-ttu-id="e80d6-242">**カスタム ページ コンテンツの使用** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-242">Set the **Use custom page content** option to **Yes**.</span></span>
5. <span data-ttu-id="e80d6-243">**カスタム ページの URI** フィールドに、完全なパスワード リセット URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-243">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="e80d6-244">**preloadscripts=true** 接尾語を含めます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-244">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e80d6-245">たとえば、「``www.<my domain>.com/password-reset?preloadscripts=true``」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-245">For example, enter ``www.<my domain>.com/password-reset?preloadscripts=true``.</span></span>
6. <span data-ttu-id="e80d6-246">**ページ レイアウト バージョン** フィールドで、バージョン **2.1.0** またはそれ以上を選択します (Commerce バージョン 10.0.15 以上のモジュール ライブラリが必要です)。</span><span class="sxs-lookup"><span data-stu-id="e80d6-246">In the **Page Layout Version** field, select version **2.1.0** or higher (requires module library for Commerce version 10.0.15 or higher).</span></span>
7. <span data-ttu-id="e80d6-247">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e80d6-247">Select **Save**.</span></span>

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="e80d6-248">ラベルと説明の既定のテキスト文字列のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="e80d6-248">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="e80d6-249">モジュール ライブラリでは、サインイン モジュールにはラベルと説明の既定のテキスト文字列が事前に入力されています。</span><span class="sxs-lookup"><span data-stu-id="e80d6-249">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="e80d6-250">文字列のカスタマイズは、作業中のモジュールのプロパティ ペインで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-250">You can customize the strings in the properties pane of the module you are working on.</span></span> <span data-ttu-id="e80d6-251">ページ上の追加文字列 (**パスワードをお忘れですか？** リンク テキストや **アカウント作成** などの呼びかけテキスト) は、Commerce ソフトウェア開発キット (SDK) を使用して、サインイン モジュールの global.json ファイルの値を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e80d6-251">Additional strings on the page (such as the **Forgotten password?** link text or the **Create an account** call to action text) will require using the Commerce software development kit (SDK) and updating the values in the global.json file for the sign-in module.</span></span>

<span data-ttu-id="e80d6-252">たとえば、パスワード リンクを忘れた場合の既定のテキストは **パスワードをお忘れですか** です。</span><span class="sxs-lookup"><span data-stu-id="e80d6-252">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="e80d6-253">以下は、サインイン ページに表示される既定のテキストを示しています。</span><span class="sxs-lookup"><span data-stu-id="e80d6-253">The following shows this default text on the sign-in page.</span></span>

![サインイン ページでパスワード リンクを忘れた場合の既定のテキスト](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="e80d6-255">ただし、モジュール ライブラリ サインイン モジュールの global.json ファイルでは、次の図に示すように、**パスワードをお忘れですか？** のテキストを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-255">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![サインイン モジュール global.json ファイルの更新されたリンク テキスト](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="e80d6-257">global.json ファイルを更新して変更内容を公開すると、コマースとライブ サインイン ページの両方のサイン イン モジュールに新しいリンク テキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e80d6-257">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e80d6-258">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e80d6-258">Additional resources</span></span>

[<span data-ttu-id="e80d6-259">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e80d6-259">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e80d6-260">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="e80d6-260">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e80d6-261">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="e80d6-261">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e80d6-262">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="e80d6-262">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e80d6-263">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="e80d6-263">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e80d6-264">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="e80d6-264">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e80d6-265">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="e80d6-265">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e80d6-266">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e80d6-266">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e80d6-267">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="e80d6-267">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e80d6-268">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="e80d6-268">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]