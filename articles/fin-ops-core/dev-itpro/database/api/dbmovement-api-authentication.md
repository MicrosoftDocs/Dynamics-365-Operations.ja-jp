---
title: データベース移動 API - 認証
description: このトピックでは、データベース移動のアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。
author: laneswenka
manager: AnnBe
ms.date: 09/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a447b29142b40bf7618fdbce2202f2ee8f732bed
ms.sourcegitcommit: d800613020d5548d100c8f240fb81bb6258a3646
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2019
ms.locfileid: "2573568"
---
# <a name="authentication"></a><span data-ttu-id="66e53-103">認証</span><span class="sxs-lookup"><span data-stu-id="66e53-103">Authentication</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="66e53-104">このトピックでは、データベース移動のアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。</span><span class="sxs-lookup"><span data-stu-id="66e53-104">This topic provides overview information about how to authenticate with the Database Movement application programming interface (API).</span></span>

## <a name="fundamentals"></a><span data-ttu-id="66e53-105">基本</span><span class="sxs-lookup"><span data-stu-id="66e53-105">Fundamentals</span></span>

<span data-ttu-id="66e53-106">データベース移動 API を呼び出すには、アプリケーションが Microsoft ID プラットフォームからアクセス トークンを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66e53-106">To call the Database Movement API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="66e53-107">アクセス トークンには、アプリケーションに関する情報と、Microsoft Dynamics Lifecycle Services (LCS) のリソースを呼び出すために必要なアクセス許可が含まれています。</span><span class="sxs-lookup"><span data-stu-id="66e53-107">The access token contains information about your application and the permission that it has to call resources in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="access-token"></a><span data-ttu-id="66e53-108">アクセス トークン</span><span class="sxs-lookup"><span data-stu-id="66e53-108">Access token</span></span>

<span data-ttu-id="66e53-109">Microsoft ID プラットフォームにより発行されるアクセス トークンは、base64 エンコードされた JavaScript Object Notation (JSON) Web トークン (JWT) です。</span><span class="sxs-lookup"><span data-stu-id="66e53-109">Access tokens that are issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="66e53-110">これにはデータベース移動 API および Microsoft ID プラットフォームによって保護されるその他の Web API が呼び出し元を検証し、呼び出し元が要求している操作を実行するための適切なアクセス許可を持っていることを確認するのに使用する情報 (クレーム) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="66e53-110">They contain information (claims) that the Database Movement API and other web APIs that are secured by the Microsoft identity platform use to validate the caller and make sure that the caller has the correct permissions to perform the operation that they are requesting.</span></span> <span data-ttu-id="66e53-111">呼び出し中に、アクセス トークンを不透明として扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="66e53-111">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="66e53-112">アクセス トークンは、常に Transport Layer Security (TLS) や Hypertext Transfer Protocol Secure (HTTPS) などのセキュリティで保護されたチャネルを介して送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66e53-112">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="66e53-113">Microsoft ID プラットフォームによって発行されるアクセス トークンの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="66e53-113">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="66e53-114">データベース移動 API を呼び出すには、アクセス トークンを HTTP 要求の承認ヘッダーにベアラー トークンとして関連付けます。</span><span class="sxs-lookup"><span data-stu-id="66e53-114">To call the Database Movement API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="66e53-115">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="66e53-115">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: lcsapi.lcs.dynamics.com
GET https://lcsapi.lcs.dynamics.com/databasemovement/v1/databases
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="66e53-116">Azure ポータルを使用して新しいアプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="66e53-116">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="66e53-117">勤務先または学校アカウント、または Microsoft アカウントを使用して、[Microsoft Azure ポータル](https://portal.azure.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="66e53-117">Sign in to the [Microsoft Azure portal](https://portal.azure.com) by using a work or school account, or a personal Microsoft account.</span></span>
2. <span data-ttu-id="66e53-118">アカウントで複数のテナントにアクセスが許可されている場合は、右上隅でアカウントを選択し、ポータル セッションを目的の Azure Active Directory (Azure AD) テナントに設定します。</span><span class="sxs-lookup"><span data-stu-id="66e53-118">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>
3. <span data-ttu-id="66e53-119">左ウィンドウで、**Azure Active Directory** サービスを選択し、**アプリ登録 \> 新規登録**を選択します。</span><span class="sxs-lookup"><span data-stu-id="66e53-119">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>
4. <span data-ttu-id="66e53-120">**アプリケーションの登録**ページが表示されたら、アプリケーションの登録情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="66e53-120">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="66e53-121">**名前** – アプリのユーザーに表示される、意味のあるアプリケーション名を入力します。</span><span class="sxs-lookup"><span data-stu-id="66e53-121">**Name** – Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="66e53-122">**サポートされる勘定タイプ** – アプリがサポートする必要がある勘定タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="66e53-122">**Supported account types** – Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="66e53-123">サポートされる勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="66e53-123">Supported account types</span></span> | <span data-ttu-id="66e53-124">説明</span><span class="sxs-lookup"><span data-stu-id="66e53-124">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="66e53-125">この組織ディレクトリのみでの勘定</span><span class="sxs-lookup"><span data-stu-id="66e53-125">Accounts in this organizational directory only</span></span> | <span data-ttu-id="66e53-126">基幹業務アプリを構築している場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="66e53-126">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="66e53-127">このオプションは、アプリをディレクトリに登録していない限り使用できません。</span><span class="sxs-lookup"><span data-stu-id="66e53-127">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="66e53-128">このオプションは、**Azure AD のみの単一テナント**にマップされます。</span><span class="sxs-lookup"><span data-stu-id="66e53-128">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="66e53-129">このオプションは、アプリをディレクトリの外部に登録していない限り、既定のオプションです。</span><span class="sxs-lookup"><span data-stu-id="66e53-129">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="66e53-130">この場合、既定のオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント**です。</span><span class="sxs-lookup"><span data-stu-id="66e53-130">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="66e53-131">任意の組織ディレクトリでのアカウント</span><span class="sxs-lookup"><span data-stu-id="66e53-131">Accounts in any organizational directory</span></span> | <span data-ttu-id="66e53-132">このオプションを選択して、すべてのビジネスおよび教育機関の顧客を対象にします。</span><span class="sxs-lookup"><span data-stu-id="66e53-132">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="66e53-133">このオプションは、**Azure AD のみのマルチ テナント**にマップされます。</span><span class="sxs-lookup"><span data-stu-id="66e53-133">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="66e53-134">アプリを **Azure AD のみの単一テナント**として登録した場合は、**認証**ブレードを使用して **Azure AD のみのマルチ テナント**に更新してから、**Azure AD のみの単一テナント**に戻ります。</span><span class="sxs-lookup"><span data-stu-id="66e53-134">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="66e53-135">任意の組織ディレクトリおよび個人の Microsoft アカウントでのアカウント</span><span class="sxs-lookup"><span data-stu-id="66e53-135">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="66e53-136">このオプションを選択して、最も幅広い顧客を対象にします。</span><span class="sxs-lookup"><span data-stu-id="66e53-136">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="66e53-137">このオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント**にマップされます。</span><span class="sxs-lookup"><span data-stu-id="66e53-137">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="66e53-138">アプリを **Azure AD マルチ テナントと個人の Microsoft アカウント**として登録した場合、ユーザー インターフェイス (UI) でこの設定を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="66e53-138">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="66e53-139">代わりに、アプリケーション マニフェスト エディターを使用してサポートされているアカウント タイプを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66e53-139">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="66e53-140">**リダイレクト URI (オプション)** – 構築しているアプリのタイプを選択します: **Web** または **パブリック クライアント (モバイル & デスクトップ)**。</span><span class="sxs-lookup"><span data-stu-id="66e53-140">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="66e53-141">次に、アプリのリダイレクト URI (または返信 URL) を入力します。</span><span class="sxs-lookup"><span data-stu-id="66e53-141">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="66e53-142">Web アプリに関しては、アプリのベース URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="66e53-142">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="66e53-143">たとえば、`http://localhost:31544` はローカル コンピューターで実行する Web アプリの URL である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="66e53-143">For example, `http://localhost:31544` might be the URL for a web app that rus on your local machine.</span></span> <span data-ttu-id="66e53-144">ユーザーは、この URL を使用して Web クライアント アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="66e53-144">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="66e53-145">パブリック クライアント アプリに関しては、Azure AD を使用してトークン応答を返すための URI を指定します。</span><span class="sxs-lookup"><span data-stu-id="66e53-145">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="66e53-146">`myapp://auth` などの、アプリに固有の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="66e53-146">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="66e53-147">Web アプリまたはネイティブ アプリの特定の例を表示するには、[Azure AD からのクイック スタート ガイド](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66e53-147">To see specific examples for web apps or native apps, see the [quick start guides from Azure AD](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="66e53-148">**API アクセス許可**で、**アクセス許可の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="66e53-148">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="66e53-149">次に、**自分の組織が使用する API** タブで、**Dynamics Lifecycle services** サービスを検索し、アプリに**ユーザー\_偽装**のアクセス許可を追加します。</span><span class="sxs-lookup"><span data-stu-id="66e53-149">Then, on the **APIs my organization uses** tab, search for **Dynamics Lifecycle services**, and add the **user\_impersonation** permission to your app.</span></span>
6. <span data-ttu-id="66e53-150">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66e53-150">Select **Register**.</span></span>

<span data-ttu-id="66e53-151">[![Azure ポータルで新しいアプリに登録する](../media/new-app-registration-expanded.png)](../media/new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="66e53-151">[![Registering a new app in the Azure portal](../media/new-app-registration-expanded.png)](../media/new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="66e53-152">Azure AD は、アプリに固有のアプリケーション ID (クライアント ID) を割り当て、アプリの**概要**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66e53-152">Azure AD assigns a unique application ID (client ID) to your app, and you're taken to the **Overview** page for your app.</span></span> <span data-ttu-id="66e53-153">アプリに複数の機能を追加するには、他のコンフィギュレーション オプション (ブランド化のオプションや証明書とシークレットのオプションなど) を選択できます。</span><span class="sxs-lookup"><span data-stu-id="66e53-153">To add more capabilities to your app, you can select other configuration options, such as options for branding, and for certificates and secrets.</span></span>
