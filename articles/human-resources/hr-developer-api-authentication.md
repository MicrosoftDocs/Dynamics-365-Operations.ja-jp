---
title: 認証
description: この記事では、Microsoft Dynamics 365 Human Resources データのアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 94d76a9f6d4a3d7afcb9b85d961899880ca9fc75
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893451"
---
# <a name="authentication"></a><span data-ttu-id="531c3-103">認証</span><span class="sxs-lookup"><span data-stu-id="531c3-103">Authentication</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="531c3-104">この記事では、Microsoft Dynamics 365 Human Resources データのアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。</span><span class="sxs-lookup"><span data-stu-id="531c3-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="531c3-105">概要</span><span class="sxs-lookup"><span data-stu-id="531c3-105">Overview</span></span>

<span data-ttu-id="531c3-106">人事管理のデータ API は OData 実装です。</span><span class="sxs-lookup"><span data-stu-id="531c3-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="531c3-107">詳細については、[データ プロトコル (OData) を開く](../fin-ops-core/dev-itpro/data-entities/odata.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="531c3-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="531c3-108">API がアプリケーションからのサービス要求を処理する前に、アプリケーションは承認された呼び出し元として認証される必要があります。</span><span class="sxs-lookup"><span data-stu-id="531c3-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="531c3-109">基本</span><span class="sxs-lookup"><span data-stu-id="531c3-109">Fundamentals</span></span>

<span data-ttu-id="531c3-110">データ API を呼び出すには、アプリケーションが Microsoft ID プラットフォームからアクセス トークンを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="531c3-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="531c3-111">アクセス トークンには、アプリケーションに関する情報と、人事管理のリソースを呼び出すために必要なアクセス許可が含まれています。</span><span class="sxs-lookup"><span data-stu-id="531c3-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="531c3-112">アクセス トークン</span><span class="sxs-lookup"><span data-stu-id="531c3-112">Access token</span></span>

<span data-ttu-id="531c3-113">Microsoft ID プラットフォームにより発行されるアクセス トークンは、base64 エンコードされた JavaScript Object Notation (JSON) Web トークン (JWT) です。</span><span class="sxs-lookup"><span data-stu-id="531c3-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="531c3-114">これにはデータ API (および Microsoft ID プラットフォームによって保護されるその他の Web API) が呼び出し元を検証し、呼び出し元が要求している操作を実行するための適切なアクセス許可を持っていることを確認するのに使用する情報 (クレーム) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="531c3-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="531c3-115">呼び出し中に、アクセス トークンを不透明として扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="531c3-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="531c3-116">アクセス トークンは、常に Transport Layer Security (TLS) や Hypertext Transfer Protocol Secure (HTTPS) などのセキュリティで保護されたチャネルを介して送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="531c3-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="531c3-117">Microsoft ID プラットフォームによって発行されるアクセス トークンの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="531c3-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="531c3-118">データ API を呼び出すには、アクセス トークンを HTTP 要求の承認ヘッダーにベアラー トークンとして関連付けます。</span><span class="sxs-lookup"><span data-stu-id="531c3-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="531c3-119">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="531c3-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="531c3-120">Azure ポータルを使用して新しいアプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="531c3-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="531c3-121">勤務先または学校のアカウント、または個人の Microsoft アカウントを使用して、[Microsoft Azure ポータル](https://portal.azure.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="531c3-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="531c3-122">アカウントで複数のテナントにアクセスが許可されている場合は、右上隅でアカウントを選択し、ポータル セッションを目的の Azure Active Directory (Azure AD) テナントに設定します。</span><span class="sxs-lookup"><span data-stu-id="531c3-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="531c3-123">左ウィンドウで、**Azure Active Directory** サービスを選択し、**アプリ登録 \> 新規登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="531c3-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="531c3-124">**アプリケーションの登録** ページが表示されたら、アプリケーションの登録情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="531c3-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="531c3-125">**名前**: アプリのユーザーに表示される、意味のあるアプリケーション名を入力します。</span><span class="sxs-lookup"><span data-stu-id="531c3-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="531c3-126">**サポートされる勘定タイプ**: アプリがサポートする必要がある勘定タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="531c3-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="531c3-127">サポートされる勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="531c3-127">Supported account types</span></span> | <span data-ttu-id="531c3-128">説明</span><span class="sxs-lookup"><span data-stu-id="531c3-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="531c3-129">この組織ディレクトリのみでの勘定</span><span class="sxs-lookup"><span data-stu-id="531c3-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="531c3-130">基幹業務アプリを構築している場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="531c3-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="531c3-131">このオプションは、アプリをディレクトリに登録していない限り使用できません。</span><span class="sxs-lookup"><span data-stu-id="531c3-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="531c3-132">このオプションは、**Azure AD のみの単一テナント** にマップされます。</span><span class="sxs-lookup"><span data-stu-id="531c3-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="531c3-133">このオプションは、アプリをディレクトリの外部に登録していない限り、既定のオプションです。</span><span class="sxs-lookup"><span data-stu-id="531c3-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="531c3-134">この場合、既定のオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント** です。</span><span class="sxs-lookup"><span data-stu-id="531c3-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="531c3-135">任意の組織ディレクトリでのアカウント</span><span class="sxs-lookup"><span data-stu-id="531c3-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="531c3-136">このオプションを選択して、すべてのビジネスおよび教育機関の顧客を対象にします。</span><span class="sxs-lookup"><span data-stu-id="531c3-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="531c3-137">このオプションは、**Azure AD のみのマルチ テナント** にマップされます。</span><span class="sxs-lookup"><span data-stu-id="531c3-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="531c3-138">アプリを **Azure AD のみの単一テナント** として登録した場合は、**認証** ブレードを使用して **Azure AD のみのマルチ テナント** に更新してから、**Azure AD のみの単一テナント** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="531c3-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="531c3-139">任意の組織ディレクトリおよび個人の Microsoft アカウントでのアカウント</span><span class="sxs-lookup"><span data-stu-id="531c3-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="531c3-140">このオプションを選択して、最も幅広い顧客を対象にします。</span><span class="sxs-lookup"><span data-stu-id="531c3-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="531c3-141">このオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント** にマップされます。</span><span class="sxs-lookup"><span data-stu-id="531c3-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="531c3-142">アプリを **Azure AD マルチ テナントと個人の Microsoft アカウント** として登録した場合、ユーザー インターフェイス (UI) でこの設定を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="531c3-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="531c3-143">代わりに、アプリケーション マニフェスト エディターを使用してサポートされているアカウント タイプを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="531c3-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="531c3-144">**リダイレクト URI (オプション)** – 構築しているアプリのタイプを選択します: **Web** または **パブリック クライアント (モバイル & デスクトップ)**。</span><span class="sxs-lookup"><span data-stu-id="531c3-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="531c3-145">次に、アプリのリダイレクト URI (または返信 URL) を入力します。</span><span class="sxs-lookup"><span data-stu-id="531c3-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="531c3-146">Web アプリに関しては、アプリのベース URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="531c3-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="531c3-147">たとえば、`http://localhost:31544` はローカル コンピューターで実行する Web アプリの URL である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="531c3-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="531c3-148">ユーザーは、この URL を使用して Web クライアント アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="531c3-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="531c3-149">パブリック クライアント アプリに関しては、Azure AD を使用してトークン応答を返すための URI を指定します。</span><span class="sxs-lookup"><span data-stu-id="531c3-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="531c3-150">`myapp://auth` などの、アプリに固有の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="531c3-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="531c3-151">Web アプリまたはネイティブ アプリの特定の例を表示するには、[Microsoft ID プラットフォーム (旧「開発者向けAzure Active Directory」)](/azure/active-directory/develop/#quickstarts)のクイックスタートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="531c3-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="531c3-152">**API アクセス許可** で、**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="531c3-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="531c3-153">次に、**自分の組織が使用する API** タブで **Dynamics 365 Human Resources** サービスを検索し、アプリに **user\_impersonation** のアクセス許可を追加します。</span><span class="sxs-lookup"><span data-stu-id="531c3-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="531c3-154">人事管理のアプリケーション ID は f9be0c49-aa22-4ec6-911a-c5da515226ff です。</span><span class="sxs-lookup"><span data-stu-id="531c3-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="531c3-155">この ID を使用して、正しいアプリケーションが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="531c3-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="531c3-156">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="531c3-156">Select **Register**.</span></span>

   <span data-ttu-id="531c3-157">[![Azure ポータルで新しいアプリに登録する](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="531c3-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="531c3-158">Azure AD は、アプリに固有のアプリケーション ID (クライアント ID) を割り当て、アプリの **概要** ページへと移動します。</span><span class="sxs-lookup"><span data-stu-id="531c3-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="531c3-159">アプリに複数の機能を追加するには、他のコンフィギュレーション オプション (ブランド化のオプションや証明書とシークレットのオプションなど) を選択できます。</span><span class="sxs-lookup"><span data-stu-id="531c3-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="531c3-160">アクセス トークンの取得</span><span class="sxs-lookup"><span data-stu-id="531c3-160">Retrieving an access token</span></span>

<span data-ttu-id="531c3-161">人事管理データ API を呼び出すためのアクセス トークンを取得する方法の詳細は、クライアント アプリケーションの開発に使用しているテクノロジーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="531c3-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="531c3-162">たとえば、[サード パーティー ユーティリティのテスト](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (Postman など)、C# コンソール アプリケーションや Web サービスの開発、または javascript/TypeScript クライアントのビルドを行っている場合です。</span><span class="sxs-lookup"><span data-stu-id="531c3-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="531c3-163">C# クライアント アプリケーションの例:</span><span class="sxs-lookup"><span data-stu-id="531c3-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="531c3-164">アクセス トークンを取得したら、上記のように、データ API に送信する各要求でベアラー トークンとして認証ヘッダーでトークンを渡します。</span><span class="sxs-lookup"><span data-stu-id="531c3-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]