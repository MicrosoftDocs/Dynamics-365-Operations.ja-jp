---
title: ID 管理ページとモジュール
description: このトピックでは、Microsoft Dynamics 365 Commerce の ID 管理ページおよびモジュールについて説明します。
author: BrianShook
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a09ba4a4d34f5168aa35271a734764df181108a1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022745"
---
# <a name="identity-management-pages-and-modules"></a><span data-ttu-id="3f85f-103">ID 管理ページとモジュール</span><span class="sxs-lookup"><span data-stu-id="3f85f-103">Identity management pages and modules</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3f85f-104">このトピックでは、Microsoft Dynamics 365 Commerce の ID 管理ページおよびモジュールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3f85f-104">This topic covers identity management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3f85f-105">ID 管理モジュールは、eコマース サイトのユーザーが Dynamics 365 Commerce 環境に関連付けられている ID 管理システムと対話するために使用する ID 管理ページの要素を表示します。</span><span class="sxs-lookup"><span data-stu-id="3f85f-105">Identity management modules show elements on identity management pages that e-commerce site users use to interact with the identity management system that is associated with your Dynamics 365 Commerce environment.</span></span> <span data-ttu-id="3f85f-106">特に、ID 管理モジュールは、サインイン、サインアップ、パスワードのリセット、およびアカウント プロフィール編集ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-106">Specifically, identity management modules are used on sign-in, sign-up, password reset, and account profile edit pages.</span></span> <span data-ttu-id="3f85f-107">既定では、Commerce モジュールは、ID プロバイダーとして Azure Active Directory B2C (Azure AD B2C) を使用するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="3f85f-107">By default, Commerce modules are configured to use Azure Active Directory B2C (Azure AD B2C) as the identity provider.</span></span>

> [!WARNING]
> <span data-ttu-id="3f85f-108">Azure AD B2C は、2021 年 8 月 1 日までに古い (レガシ) ユーザー フローを破棄します。</span><span class="sxs-lookup"><span data-stu-id="3f85f-108">Azure AD B2C will retire old (legacy) user flows by August 1, 2021.</span></span> <span data-ttu-id="3f85f-109">したがって、ユーザー フローを新しい推奨バージョンに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f85f-109">Therefore, you should plan to migrate your user flows to the new recommended version.</span></span> <span data-ttu-id="3f85f-110">新しいバージョンでは、機能パリティと新しい機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-110">The new version provides feature parity and new features.</span></span> <span data-ttu-id="3f85f-111">詳細については、[Azure Active Directory B2C のユーザー フロー](/azure/active-directory-b2c/user-flow-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f85f-111">For more information, see [User flows in Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).</span></span>

## <a name="identity-management-pages"></a><span data-ttu-id="3f85f-112">ID 管理ページ</span><span class="sxs-lookup"><span data-stu-id="3f85f-112">Identity management pages</span></span>

<span data-ttu-id="3f85f-113">ID 管理ページは、Commerce サイト ビルダーを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-113">Identity management pages are built in Commerce site builder.</span></span> <span data-ttu-id="3f85f-114">ただし、セキュリティ上の理由から、Commerce サイトからではなく Azure AD B2C サーバーでホストされ、提供されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-114">However, for security reasons, they are hosted and served from Azure AD B2C servers, not from your Commerce site.</span></span> <span data-ttu-id="3f85f-115">ベスト プラクティスとして、ID 管理ページ用に個別の Azure AD ヘッダー フラグメントとフッター フラグメントを作成し、それらに最小限のページ要素を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f85f-115">As a best practice, you should build separate Azure AD header and footer fragments for identity management pages, and include minimal page elements in them.</span></span> <span data-ttu-id="3f85f-116">相対リンクを持つフラグメントや、Commerce 固有の呼び出し (お気に入りボタンやショッピング カート モジュールからの呼び出しなど) を行うフラグメントは、Azure AD B2C サーバーからは機能しません。</span><span class="sxs-lookup"><span data-stu-id="3f85f-116">Fragments that have relative links, or that make Commerce-specific calls (such as calls from the favorites button or shopping cart module), won't work from the Azure AD B2C servers.</span></span> <span data-ttu-id="3f85f-117">Commerce のインスタンスと共にリリースされるスターター サイトには、参照のために Azure AD のヘッダーとフッターのサンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f85f-117">The starter site that is released with your instance of Commerce includes sample Azure AD header and footer fragments for reference.</span></span>

<span data-ttu-id="3f85f-118">Azure AD B2C で ID 管理ページを設定する方法については、「[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f85f-118">For information about how to set up identity management pages in Azure AD B2C, see [Set up custom pages for user sign-ins](custom-pages-user-logins.md).</span></span>

### <a name="associate-published-identity-management-pages-with-the-azure-ad-b2c-user-flow"></a><span data-ttu-id="3f85f-119">発行された ID 管理ページと Azure AD B2C ユーザー フローの関連付け</span><span class="sxs-lookup"><span data-stu-id="3f85f-119">Associate published identity management pages with the Azure AD B2C user flow</span></span>

<span data-ttu-id="3f85f-120">ID 管理ページでは、Azure AD B2C サーバーから初期化された JavaScriptが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-120">Identity management pages use JavaScript that is initialized from the Azure AD B2C server.</span></span> <span data-ttu-id="3f85f-121">多くの場合、サイト ビルダーや eコマース サイトからページをプレビューすると、ページの中央に白い読み込みバーが表示されますが、初期化されることはありません。</span><span class="sxs-lookup"><span data-stu-id="3f85f-121">Often, when a page is previewed from site builder or an e-commerce site, a white loading bar appears in the middle of the page but is never initialized.</span></span> <span data-ttu-id="3f85f-122">ページが発行されたら、[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md) の説明に従って、そのページを Azure AD B2C ユーザー フローに関連付ける必要があります。その後、Azure AD B2C から提供されるページを表示すると、ページ要素がレンダリングされるときに JavaScript が初期化されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-122">After a page is published, you must associate the page with the Azure AD B2C user flow as described in [Set up custom pages for user sign-ins](custom-pages-user-logins.md). Then, when you view the page that is served from Azure AD B2C, the JavaScript will be initialized when page elements are rendered.</span></span>

## <a name="identity-management-modules"></a><span data-ttu-id="3f85f-123">ID 管理モジュール</span><span class="sxs-lookup"><span data-stu-id="3f85f-123">Identity management modules</span></span>

<span data-ttu-id="3f85f-124">Commerce の ID 管理ページで使用されるモジュールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3f85f-124">The following modules are used on identity management pages in Commerce.</span></span>

### <a name="sign-up-module"></a><span data-ttu-id="3f85f-125">サインアップ モジュール</span><span class="sxs-lookup"><span data-stu-id="3f85f-125">Sign-up module</span></span>

<span data-ttu-id="3f85f-126">サインアップ モジュールは、サインアップ ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-126">The sign-up module is used on the sign-up page.</span></span> <span data-ttu-id="3f85f-127">これには、サイト ユーザーがサインアップ フローを完了するために使用するフォーム要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-127">It includes the form elements that site users use to complete the sign-up flow.</span></span> <span data-ttu-id="3f85f-128">ユーザーは、ユーザー名として使用するメール アドレスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3f85f-128">A user provides an email address to use as their user name.</span></span> <span data-ttu-id="3f85f-129">その後、このモジュールによって Azure AD B2C メール検証フローが実行されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-129">The module then enables the Azure AD B2C email verification flow to occur.</span></span> <span data-ttu-id="3f85f-130">このフローでは「コードを送信」がトリガされ、ユーザーが入力したセキュリティ個人識別番号 (PIN) が検証されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-130">In this flow, the "send code" is triggered, and the security personal identification number (PIN) that the user enters is verified.</span></span> <span data-ttu-id="3f85f-131">サインアップ ページで収集された情報は、Azure AD B2C でレコードを作成し、Commerce で顧客レコードを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-131">Information that is collected on the sign-up page is used to create a record in Azure AD B2C and a customer record in Commerce.</span></span>

### <a name="sign-in-module"></a><span data-ttu-id="3f85f-132">サインイン モジュール</span><span class="sxs-lookup"><span data-stu-id="3f85f-132">Sign-in module</span></span>

<span data-ttu-id="3f85f-133">サインイン モジュールは、サインイン ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-133">The sign-in module is used on the sign-in page.</span></span> <span data-ttu-id="3f85f-134">これには、ユーザーが自分のアカウントにサインインするために使用するフォーム要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-134">It includes the form elements that users use to sign in to their accounts.</span></span> <span data-ttu-id="3f85f-135">サインイン ページには、ユーザーがサインアップ ページを開く時に使用できるボタンも表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-135">The sign-in page also includes a button that users can use to open the sign-up page.</span></span> <span data-ttu-id="3f85f-136">この方法で、このページは Azure AD B2Cの「サインアップしてサインインする」ユーザーフローと直接ペアリングされます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-136">In this way, the page is paired directly with the "sign up and sign in" user flow in Azure AD B2C.</span></span>

### <a name="password-reset-modules"></a><span data-ttu-id="3f85f-137">パスワードのリセット モジュール</span><span class="sxs-lookup"><span data-stu-id="3f85f-137">Password reset modules</span></span>

<span data-ttu-id="3f85f-138">パスワードのリセット フローに関連付けられているモジュールは次の 2 種類です。</span><span class="sxs-lookup"><span data-stu-id="3f85f-138">The following two modules are associated with the password reset flow:</span></span>

- <span data-ttu-id="3f85f-139">**パスワードのリセット検証** – このモジュールは、パスワードのリセット検証ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-139">**Password reset verification** – This module is used on the password reset verification page.</span></span> <span data-ttu-id="3f85f-140">これにより、ユーザーはユーザー アカウントに関連付けられているメール アドレスにセキュリティ PIN のメールを送信します。</span><span class="sxs-lookup"><span data-stu-id="3f85f-140">It lets users trigger the sending of a security PIN email to the email address that is associated with the user account.</span></span> <span data-ttu-id="3f85f-141">パスワードのリセットの検証ページでは、ユーザーが受け取ったセキュリティ PIN を入力してアカウントの所有権を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-141">The password reset verification page also lets users enter the security PIN that they receive to verify ownership of the account.</span></span>
- <span data-ttu-id="3f85f-142">**パスワードのリセット** – このモジュールは、パスワードのリセット ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-142">**Password reset** – This module is used on the password reset page.</span></span> <span data-ttu-id="3f85f-143">パスワード リセットの確認ページでアカウントのメール アドレスが確認された後、ユーザーは新しいパスワードを設定して確認できます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-143">It lets users set and confirm a new password after the account email address has been verified on the password reset verification page.</span></span>

### <a name="account-profile-edit-module"></a><span data-ttu-id="3f85f-144">アカウント プロフィール編集モジュール</span><span class="sxs-lookup"><span data-stu-id="3f85f-144">Account profile edit module</span></span>

<span data-ttu-id="3f85f-145">アカウント プロフィールの編集モジュールは、プロフィール編集ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-145">The account profile edit module is used on the account profile edit page.</span></span> <span data-ttu-id="3f85f-146">これにより、ユーザーが名および姓を更新できます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-146">It lets users update their first name (given name) and last name (surname).</span></span> <span data-ttu-id="3f85f-147">これら 2 つの値は Azure AD B2C と Commerce 間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-147">These two values are shared between Azure AD B2C and Commerce.</span></span> <span data-ttu-id="3f85f-148">ユーザーがアカウント プロフィール編集ページを通じて更新を行う場合、値は Azure AD B2C システムと Commerce システムの両方で更新されます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-148">If a user makes any updates via the account profile edit page, the values will be updated in both the Azure AD B2C system and the Commerce system.</span></span>

<span data-ttu-id="3f85f-149">Commerce eコマース サイトでは、ユーザーは **マイ アカウント \> マイ プロフィール \> 詳細の表示 \> 名前** に移動することで自分のアカウント プロフィール編集ページにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-149">On a Commerce e-commerce site, users access their account profile edit page by going to **My account \> My profile \> View details \> Name**.</span></span> <span data-ttu-id="3f85f-150">ユーザーは、**編集** を選択して情報を更新できます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-150">They can then select **Edit** to update their information.</span></span>

### <a name="azure-ad-generic-module"></a><span data-ttu-id="3f85f-151">Azure AD 汎用モジュール</span><span class="sxs-lookup"><span data-stu-id="3f85f-151">Azure AD generic module</span></span>

<span data-ttu-id="3f85f-152">Azure AD 汎用モジュールは Azure AD B2C の推奨パターンに従い、専用の **\<div\>** 要素が設定され、Azure AD B2C がサイトページ上で要素をレンダリングするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-152">The Azure AD generic module follows the recommended pattern for Azure AD B2C, where a dedicated **\<div\>** element is set that Azure AD B2C can use to render elements on a site page.</span></span> <span data-ttu-id="3f85f-153">汎用モジュールは柔軟であり、そのモジュールを含むページをすべての Azure AD B2C ユーザー フローのページ レイアウトに使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-153">The generic module is flexible, and a page that includes it can be used for page layouts for all Azure AD B2C user flows.</span></span>

<span data-ttu-id="3f85f-154">Azure AD B2C は、ページ上のモジュールに異なるユーザー フロー要素をレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="3f85f-154">Azure AD B2C will render the different user flow elements in the module on the page.</span></span> <span data-ttu-id="3f85f-155">したがって、ページのレンダリング時に視覚的要素に対する制御がわずかに少なくなります。</span><span class="sxs-lookup"><span data-stu-id="3f85f-155">Therefore, there is slightly less control over the visual elements when the page is rendered.</span></span> <span data-ttu-id="3f85f-156">カスケード スタイル シート (CSS) スタイルが適用されますが、他の ID 管理モジュールのようにページ要素の複雑な配置を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="3f85f-156">Although Cascading Style Sheets (CSS) styling will apply, complex positioning of page elements can't be done as it can for other identity management modules.</span></span>

<span data-ttu-id="3f85f-157">汎用モジュールを含むページは、Azure AD B2C 設定 (たとえば、サインインおよびサインアップ用の ソーシャル ID プロバイダを追加する場合) を変更したり、将来の Azure AD B2C 機能を使用する場合にモジュールの拡張性調整が必要ないため、より効率的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f85f-157">A page that includes the generic module is more efficient to use, because extensibility adjustments to the module aren't required if you change Azure AD B2C settings (for example, if you add more social identity providers for sign-in and sign-up) or if you use future Azure AD B2C features.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f85f-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3f85f-158">Additional resources</span></span>

[<span data-ttu-id="3f85f-159">ユーザーのサインインに対するカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="3f85f-159">Set up custom pages for user sign-ins</span></span>](custom-pages-user-logins.md)