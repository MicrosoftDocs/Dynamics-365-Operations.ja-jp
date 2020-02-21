---
title: サービス エンドポイント 概要
description: このトピックでは、使用できるサービス エンドポイントについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a208599e85646e8a6756bf6d3d0d6d4ec603bc
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030883"
---
# <a name="service-endpoints-overview"></a><span data-ttu-id="b58cf-103">サービス エンドポイント 概要</span><span class="sxs-lookup"><span data-stu-id="b58cf-103">Service endpoints overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b58cf-104">このトピックでは、Microsoft Dynamics 365 Finance で使用できるサービス エンドポイントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-104">This topic describes the service endpoints that are available in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="b58cf-105">また、Microsoft Dynamics AX 2012 で使用できるエンドポイントと比較します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-105">It also provides a comparison to the endpoints that are available in Microsoft Dynamics AX 2012.</span></span>

## <a name="list-of-services"></a><span data-ttu-id="b58cf-106">サービスのリスト</span><span class="sxs-lookup"><span data-stu-id="b58cf-106">List of services</span></span>
<span data-ttu-id="b58cf-107">次のテーブルでは、すべてのサービス エンドポイントを一覧表示し、アプリケーション、および AX 2012 で使用可能なエンドポイントを比較しています。</span><span class="sxs-lookup"><span data-stu-id="b58cf-107">The following table lists all the service endpoints, and compares the endpoints available for the application, and AX 2012.</span></span>

| <span data-ttu-id="b58cf-108">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="b58cf-108">Service endpoint</span></span>            | <span data-ttu-id="b58cf-109">AX 2012</span><span class="sxs-lookup"><span data-stu-id="b58cf-109">AX 2012</span></span> | <span data-ttu-id="b58cf-110">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b58cf-110">Finance and Operations</span></span>         |
|-----------------------------|---------|--------------------------------|
| <span data-ttu-id="b58cf-111">ドキュメント サービス (AXDs)</span><span class="sxs-lookup"><span data-stu-id="b58cf-111">Document services (AXDs)</span></span>    | <span data-ttu-id="b58cf-112">はい</span><span class="sxs-lookup"><span data-stu-id="b58cf-112">Yes</span></span>     | <span data-ttu-id="b58cf-113">いいえ – データ エンティティに置き換えられます</span><span class="sxs-lookup"><span data-stu-id="b58cf-113">No – Replaced by data entities</span></span> |
| <span data-ttu-id="b58cf-114">SOAP ベースのメタデータ サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-114">SOAP-based metadata service</span></span> | <span data-ttu-id="b58cf-115">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-115">Yes</span></span>     | <span data-ttu-id="b58cf-116">いいえ – REST メタデータに置き換えられます</span><span class="sxs-lookup"><span data-stu-id="b58cf-116">No – Replaced by REST metadata</span></span> |
| <span data-ttu-id="b58cf-117">SOAP ベースのクエリ サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-117">SOAP-based query service</span></span>    | <span data-ttu-id="b58cf-118">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-118">Yes</span></span>     | <span data-ttu-id="b58cf-119">いいえ – OData に置き換えられます</span><span class="sxs-lookup"><span data-stu-id="b58cf-119">No – Replaced by OData</span></span>         |
| <span data-ttu-id="b58cf-120">OData クエリ サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-120">OData query service</span></span>         | <span data-ttu-id="b58cf-121">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-121">Yes</span></span>     | <span data-ttu-id="b58cf-122">いいえ – OData に置き換えられます</span><span class="sxs-lookup"><span data-stu-id="b58cf-122">No – Replaced by OData</span></span>         |
| <span data-ttu-id="b58cf-123">SOAP ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-123">SOAP-based custom service</span></span>   | <span data-ttu-id="b58cf-124">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-124">Yes</span></span>     | <span data-ttu-id="b58cf-125">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-125">Yes</span></span>                            |
| <span data-ttu-id="b58cf-126">JSON ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-126">JSON-based custom service</span></span>   | <span data-ttu-id="b58cf-127">無</span><span class="sxs-lookup"><span data-stu-id="b58cf-127">No</span></span>      | <span data-ttu-id="b58cf-128">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-128">Yes</span></span>                            |
| <span data-ttu-id="b58cf-129">OData サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-129">OData Service</span></span>               | <span data-ttu-id="b58cf-130">無</span><span class="sxs-lookup"><span data-stu-id="b58cf-130">No</span></span>      | <span data-ttu-id="b58cf-131">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-131">Yes</span></span>                            |
| <span data-ttu-id="b58cf-132">REST メタデータ サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-132">REST Metadata Service</span></span>       | <span data-ttu-id="b58cf-133">無</span><span class="sxs-lookup"><span data-stu-id="b58cf-133">No</span></span>      | <span data-ttu-id="b58cf-134">有</span><span class="sxs-lookup"><span data-stu-id="b58cf-134">Yes</span></span>                            |

<span data-ttu-id="b58cf-135">このトピックは、サービスと、REST メタデータ サービスの認証について説明します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-135">This topic describes authentication for services, and the REST Metadata service.</span></span> <span data-ttu-id="b58cf-136">次のリンクでは、以下のための詳細なドキュメントを提供します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-136">The following links provide detailed documentation for:</span></span>

- [<span data-ttu-id="b58cf-137">顧客サービスの開発</span><span class="sxs-lookup"><span data-stu-id="b58cf-137">Custom service development</span></span>](custom-services.md)
- [<span data-ttu-id="b58cf-138">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="b58cf-138">Open Data Protocol (OData)</span></span>](odata.md)

## <a name="authentication"></a><span data-ttu-id="b58cf-139">認証</span><span class="sxs-lookup"><span data-stu-id="b58cf-139">Authentication</span></span>
<span data-ttu-id="b58cf-140">OData サービス、JSON ベース顧客サービス、および REST メタデータ サービスは、標準の OAuth 2.0 認証をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b58cf-140">OData services, JSON-based custom services, and the REST metadata service support standard OAuth 2.0 authentication.</span></span>

<span data-ttu-id="b58cf-141">現在のところ、[承認コード付与フロー](https://msdn.microsoft.com/library/azure/dn645542.aspx)と[クライアントの資格情報 (共有シークレットまたは証明書) を使用したサービス間の呼び出し](https://docs.microsoft.com/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service)の両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b58cf-141">We currently support both [Authorization Code Grant flow](https://msdn.microsoft.com/library/azure/dn645542.aspx) and [Service to service calls using client credentials (shared secret or certificate)](https://docs.microsoft.com/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service).</span></span>

<span data-ttu-id="b58cf-142">Microsoft Azure Active Directory (AAD) では、次の 2 種類のアプリケーションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b58cf-142">Two kinds of application are supported in Microsoft Azure Active Directory (AAD):</span></span>

- <span data-ttu-id="b58cf-143">**ネイティブ クライアント アプリケーション** – このフローでは、認証と承認にユーザー名とパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-143">**Native client application** – This flow uses a user name and password for authentication and authorization.</span></span>
- <span data-ttu-id="b58cf-144">**Web アプリケーション (機密クライアント)** – 機密クライアントとは、クライアントのパスワードを世界に対して秘密にするアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="b58cf-144">**Web application (Confidential client)** – A confidential client is an application that can keep a client password confidential to the world.</span></span> <span data-ttu-id="b58cf-145">承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。</span><span class="sxs-lookup"><span data-stu-id="b58cf-145">The authorization server assigned this client password to the client application.</span></span>

<span data-ttu-id="b58cf-146">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b58cf-146">For more information, see:</span></span>

- [<span data-ttu-id="b58cf-147">OAuth 2.0 および Azure Active Directory を使用して web アプリケーションへのアクセスを許可する</span><span class="sxs-lookup"><span data-stu-id="b58cf-147">Authorize access to web applications using OAuth 2.0 and Azure Active Directory</span></span>](https://msdn.microsoft.com/library/azure/dn645545.aspx)
- [<span data-ttu-id="b58cf-148">サービス認証問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="b58cf-148">Troubleshoot service authentication issues</span></span>](troubleshoot-service-authentication.md)

<span data-ttu-id="b58cf-149">次の図は、認証コードの付与フローに対して認証を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-149">The following illustration describes how authorization must be configured for Authorization code grant flow.</span></span>

![認証コードの付与フロー](./media/services-authentication.png)

<span data-ttu-id="b58cf-151">以下の図では、クライアントの資格情報 (共有秘密または証明書) を使用したサービス間の呼び出し承認の仕組みを説明します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-151">And below is the illustration describes how authorization works for Service to service calls using client credentials (shared secret or certificate).</span></span>

![クライアント資格情報を使用したサービス間呼び出し](./media/S2SAuth.jpg)

### <a name="register-a-web-application-with-aad"></a><span data-ttu-id="b58cf-153">AAD に Web アプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="b58cf-153">Register a web application with AAD</span></span>

> [!NOTE]
> <span data-ttu-id="b58cf-154">これらの手順は、組織内のすべての人が完了する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b58cf-154">These steps don't have to be completed by all the people in your organization.</span></span> <span data-ttu-id="b58cf-155">Azure サービスの管理者ユーザーのみがアプリケーションを追加し、その開発者とクライアント ID を共有することができます。</span><span class="sxs-lookup"><span data-stu-id="b58cf-155">Only one Azure Service Administrator user can add the application and share the client ID with the developers.</span></span>

<span data-ttu-id="b58cf-156">**前提条件:** Azure サブスクリプションと Azure Active Directory (Azure AD) への管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="b58cf-156">**Prerequisite:** You must have an Azure subscription and admin access to Azure Active Directory (Azure AD).</span></span>

<span data-ttu-id="b58cf-157">クライアントがサービスと通信する前に、(Azure AD) に登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b58cf-157">Before any clients can communicate with the services, they must be registered in (Azure AD).</span></span> <span data-ttu-id="b58cf-158">これらの手順を使用すると、(Azure AD) でアプリケーションに登録できます。</span><span class="sxs-lookup"><span data-stu-id="b58cf-158">These steps will help you register an application with (Azure AD).</span></span> <span data-ttu-id="b58cf-159">この手順については、[Azure アプリ登録のトレーニングガイド](https://docs.microsoft.com/azure/active-directory/develop/app-registrations-training-guide-for-app-registrations-legacy-users)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b58cf-159">The steps are explained in the [Azure app registration training guide](https://docs.microsoft.com/azure/active-directory/develop/app-registrations-training-guide-for-app-registrations-legacy-users).</span></span> <span data-ttu-id="b58cf-160">このプロセスでの固有の構成には、コンテキストで次の追加情報を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b58cf-160">For specific configuration in this process, the following additional information must be used in context.</span></span>

<span data-ttu-id="b58cf-161">**Microsoft DynamicsERP (Microsoft.ERP)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-161">Select **Microsoft Dynamics ERP (Microsoft.ERP)**.</span></span> <span data-ttu-id="b58cf-162">**API を選択** 内の検索フィールドで **Microsoft Dynamics ERP** を検索する場合、使用できないように見えることがあります。</span><span class="sxs-lookup"><span data-stu-id="b58cf-162">If you search for **Microsoft Dynamics ERP** in the search field within **Select an API** it might appear to be unavailable.</span></span> <span data-ttu-id="b58cf-163">その場合は、上に示したようにフルネームを検索してください。</span><span class="sxs-lookup"><span data-stu-id="b58cf-163">In that case, make sure that you search for the full name, as shown above.</span></span>
<span data-ttu-id="b58cf-164">**委任アクセス権** で、少なくとも次のオプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b58cf-164">Under **Delegated permissions**, you must select, at a minimum, the following options:</span></span>

- <span data-ttu-id="b58cf-165">Dynamics AX カスタム サービスへのアクセス</span><span class="sxs-lookup"><span data-stu-id="b58cf-165">Access Dynamics AX Custom Service</span></span>
- <span data-ttu-id="b58cf-166">Dynamics AX データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="b58cf-166">Access Dynamics AX data</span></span>
- <span data-ttu-id="b58cf-167">組織ユーザーとしての Dynamics AX オンラインへのアクセス</span><span class="sxs-lookup"><span data-stu-id="b58cf-167">Access Dynamics AX online as organization users</span></span>

 > [!IMPORTANT]
 > <span data-ttu-id="b58cf-168">このキーは再度表示されないため、コピーしてください。</span><span class="sxs-lookup"><span data-stu-id="b58cf-168">Make sure that you copy the key, because you won't see it again.</span></span> <span data-ttu-id="b58cf-169">OAuth 認証を完了して Azure AD トークンを受け取るには、この秘密のキーを知っておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="b58cf-169">You will be required to know this secret key to complete your OAuth authentication and receive an Azure AD token.</span></span>

### <a name="register-your-external-application"></a><span data-ttu-id="b58cf-170">外部アプリケーションの登録</span><span class="sxs-lookup"><span data-stu-id="b58cf-170">Register your external application</span></span> 

1. <span data-ttu-id="b58cf-171">アプリケーションで、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-171">In the application, go to **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span>
2. <span data-ttu-id="b58cf-172">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-172">Select **New**.</span></span>
3. <span data-ttu-id="b58cf-173">新しいレコード用のフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-173">Fill in the fields for the new record:</span></span>

    - <span data-ttu-id="b58cf-174">**クライアント ID** フィールドで、Azure AD に登録したアプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-174">In the **Client Id** field, enter the application ID that you registered in Azure AD.</span></span>
    - <span data-ttu-id="b58cf-175">**名前**フィールドに、アプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-175">In the **Name** field, enter a name for the application.</span></span>
    - <span data-ttu-id="b58cf-176">**ユーザー ID** フィールドで、適切なサービス アカウントのユーザー ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-176">In the **User ID** field, select an appropriate service account user ID.</span></span> <span data-ttu-id="b58cf-177">この例では、**管理者**ユーザーを選択しました。</span><span class="sxs-lookup"><span data-stu-id="b58cf-177">For this example, we have selected the **Admin** user.</span></span> <span data-ttu-id="b58cf-178">ただし、実行する必要がある操作に対して適切なアクセス許可を持つ、専用のサービス アカウントをプロビジョニングすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b58cf-178">However, as a better practice, you should provision a dedicated service account that has the correct permissions for the operations that must be performed.</span></span>

    <span data-ttu-id="b58cf-179">完了したら、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-179">When you've finished, select **Save**.</span></span>

<span data-ttu-id="b58cf-180">これで、前提条件の設定を完了しました。</span><span class="sxs-lookup"><span data-stu-id="b58cf-180">You've now finished setting up the prerequisites.</span></span> <span data-ttu-id="b58cf-181">外部のアプリケーションが Azure AD Authentication トークンを取得した後、認証 HTTP ヘッダーのトークンを使用して、OData や SOAP などの後続のサービスの呼び出しを行うことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b58cf-181">After the external application retrieves an Azure AD authentication token, it should now be able to use the token in an authorization HTTP header to make subsequent service calls via OData or SOAP, for example.</span></span>

### <a name="client-sample-code"></a><span data-ttu-id="b58cf-182">クライアント サンプル コード</span><span class="sxs-lookup"><span data-stu-id="b58cf-182">Client sample code</span></span>

<span data-ttu-id="b58cf-183">次は、AAD からトークンを取得するための C\# サンプル コードです。</span><span class="sxs-lookup"><span data-stu-id="b58cf-183">The following is C\# sample code for getting a token from AAD.</span></span> <span data-ttu-id="b58cf-184">このフローで、同意フォーム (テナント間アプリケーション用) およびサインイン フォームがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b58cf-184">In this flow, the user will be presented with a consent form (for cross-tenant application) and a sign-in form.</span></span>

```csharp
UriBuilder uri = new UriBuilder ("https://login.windows.net/contoso2ax.onmicrosoft.com");

AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

//request token for the resource - which is the URI for your organization. NOTE: Important do not add a trailing slash at the end of the URI
AuthenticationResult authenticationResult = authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, redirectURI);

//this gets the authorization token, which needs to be passed in the Header of the HTTP Requests
string authenticationHeader = authenticationResult.CreateAuthorizationHeader();
```

<span data-ttu-id="b58cf-185">ポップアップを表示せずにユーザー名とパスワードを渡すには、**AcquireToken** の次のオーバーロードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-185">To pass the user name and password without showing a pop-up, you can use the following overload of **AcquireToken**.</span></span>

```csharp
UserCredential userCred = new UserCredential (username, password);
authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, userCred);
```

## <a name="rest-metadata-service"></a><span data-ttu-id="b58cf-186">REST メタデータ サービス</span><span class="sxs-lookup"><span data-stu-id="b58cf-186">REST metadata service</span></span>
<span data-ttu-id="b58cf-187">REST メタデータ サービスは、読み取り専用サービスです。</span><span class="sxs-lookup"><span data-stu-id="b58cf-187">The REST metadata service is a read-only service.</span></span> <span data-ttu-id="b58cf-188">つまり、ユーザーは GET 要求のみ生成できます。</span><span class="sxs-lookup"><span data-stu-id="b58cf-188">In other words, users can make only GET requests.</span></span> <span data-ttu-id="b58cf-189">このエンドポイントの主な目的は、要素のメタデータ情報を提供することです。</span><span class="sxs-lookup"><span data-stu-id="b58cf-189">The main purpose of this endpoint is to provide metadata information for elements.</span></span> <span data-ttu-id="b58cf-190">OData 実装です。</span><span class="sxs-lookup"><span data-stu-id="b58cf-190">It is an OData implementation.</span></span>

<span data-ttu-id="b58cf-191">このエンドポイントは、`http://\[baseURI\]/Metadata` でホストされています。</span><span class="sxs-lookup"><span data-stu-id="b58cf-191">This endpoint is hosted at `http://\[baseURI\]/Metadata`.</span></span>

<span data-ttu-id="b58cf-192">現在、このエンドポイントは、次の要素のメタデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-192">Currently, this endpoint provides metadata for the following elements:</span></span>

- <span data-ttu-id="b58cf-193">**ラベル** – システムからラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-193">**Labels** – Returns labels from the system.</span></span> <span data-ttu-id="b58cf-194">ラベルには言語と ID のデュアル ペア キーがあり、ラベルの値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="b58cf-194">Labels have a dual pair key of language and ID, so that you can retrieve the value of the label.</span></span>

    <span data-ttu-id="b58cf-195">**例:** `https://[baseURI\]/metadata/Labels(Id='@SVC\_ODataLabelFile:Label1',Language='en-us')`</span><span class="sxs-lookup"><span data-stu-id="b58cf-195">**Example:** `https://[baseURI\]/metadata/Labels(Id='@SVC\_ODataLabelFile:Label1',Language='en-us')`</span></span>

- <span data-ttu-id="b58cf-196">**データ エンティティ** - システム内のすべてのデータ エンティティの JSON 形式の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="b58cf-196">**Data entities** – Returns a JSON-formatted list of all the data entities in the system.</span></span>

    <span data-ttu-id="b58cf-197">**例:** `https://[baseURI\]/Metadata/DataEntities`</span><span class="sxs-lookup"><span data-stu-id="b58cf-197">**Example:** `https://[baseURI\]/Metadata/DataEntities`</span></span>
