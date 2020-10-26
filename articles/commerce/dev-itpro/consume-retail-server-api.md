---
title: 外部アプリケーションでの Retail Server API の使用
description: このトピックでは、外部アプリケーションで Retail Server API を使用する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 1362b07307dcbcd2e647bdedb2f9be9e8078c26a
ms.sourcegitcommit: 47166b3e10097cc2754e0c8459f62dcdeef27053
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2020
ms.locfileid: "3991491"
---
# <a name="consume-retail-server-apis-in-external-applications"></a><span data-ttu-id="2148b-103">外部アプリケーションでの Retail Server API の使用</span><span class="sxs-lookup"><span data-stu-id="2148b-103">Consume Retail Server APIs in external applications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2148b-104">このトピックでは、外部アプリケーションで Retail Server API を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2148b-104">This topic describes how to consume the Retail Server APIs in external applications.</span></span> <span data-ttu-id="2148b-105">Retail Server は、外部アプリケーションが API を使用できるように、Open Data Protocol (OData) Web エンドポイントを公開します。</span><span class="sxs-lookup"><span data-stu-id="2148b-105">Retail Server exposes the Open Data Protocol (OData) web endpoint so that external applications can consume the APIs.</span></span> <span data-ttu-id="2148b-106">また、Retail Server は Commerce Runtime (CRT) ビジネス ロジックをホストし、それを OData エンドポイントとして公開します。</span><span class="sxs-lookup"><span data-stu-id="2148b-106">Retail Server also hosts the Commerce runtime (CRT) business logic and exposes it as OData endpoints.</span></span> <span data-ttu-id="2148b-107">これらのエンドポイントは、Retail Server API と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2148b-107">These endpoints are known as the Retail Server APIs.</span></span>

<span data-ttu-id="2148b-108">外部アプリケーションでは、HTTPS を使用して OData サービスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2148b-108">External applications can consume the OData service through HTTPS.</span></span> <span data-ttu-id="2148b-109">Retail Server には、API を利用するための複数のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="2148b-109">Retail Server provides multiple options for consuming the APIs:</span></span>

- <span data-ttu-id="2148b-110">**Retail Server プロキシ** – 厳密に型指定された API を使用する方法。</span><span class="sxs-lookup"><span data-stu-id="2148b-110">**Retail server proxy** – A strongly typed way to consume the APIs.</span></span> <span data-ttu-id="2148b-111">さまざまなアプリケーションのタイプに対して公開される複数のタイプのプロキシがあります。</span><span class="sxs-lookup"><span data-stu-id="2148b-111">There are multiple types of proxies that are exposed for different application types:</span></span>

    - <span data-ttu-id="2148b-112">**C\# プロキシ** – サーバー側とネイティブの両方のアプリケーションが、C\# バイナリ (クラス ライブラリ) を使用して API やその他のエンティティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2148b-112">**C\# proxy** – Server-side and native applications can consume the C\# binary (class library) to access the APIs and other entities.</span></span>
    - <span data-ttu-id="2148b-113">**TypeScript プロキシ** – クライアント アプリケーションは、.ts プロキシ ファイルを使用して API およびその他のエンティティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2148b-113">**TypeScript proxy** – Client applications can consume the .ts proxy file to access the APIs and other entities.</span></span>

- <span data-ttu-id="2148b-114">**OData クライアント** – OData クライアントや Postman から API を使用することができます。または Retail Server URL に対する HTTPS 要求を生成することにより、API を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2148b-114">**OData client** – The APIs can also be consumed from OData clients, from Postman, or by generating an HTTPS request to the Retail Server URL.</span></span>

<span data-ttu-id="2148b-115">メタデータを参照するには、Web ブラウザーの次のフォーマットで Retail Server の URL を開きます。</span><span class="sxs-lookup"><span data-stu-id="2148b-115">To browse the metadata, open the Retail Server URL in the following format in a web browser.</span></span> <span data-ttu-id="2148b-116">すると、すべての Retail Server API、および入出力パラメータの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-116">The result is a list of all the Retail Server APIs, and input and output parameters.</span></span>

```rest
https://RS-URL/Commerce/$metadata
```

## <a name="security-and-authentication-that-are-required-to-consume-apis"></a><span data-ttu-id="2148b-117">API の使用に必要なセキュリティと認証</span><span class="sxs-lookup"><span data-stu-id="2148b-117">Security and authentication that are required to consume APIs</span></span>

<span data-ttu-id="2148b-118">各 API へのアクセスは、ネイティブで次のロールに従って制限されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-118">Access to each API is natively restricted according to the following roles:</span></span>

- <span data-ttu-id="2148b-119">**従業員** – このロールに関連付けられている API にアクセスするには、販売時点管理 (POS) デバイスの有効化 (デバイス トークン) が必要で、認証済み従業員がアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2148b-119">**Employee** – Access to APIs that are associated with this role requires point of sale (POS) device activation (a device token) and an authenticated employee.</span></span>
- <span data-ttu-id="2148b-120">**顧客** – このロールに関連付けられている API へのアクセスには、認証済み顧客が必要です。</span><span class="sxs-lookup"><span data-stu-id="2148b-120">**Customer** – Access to APIs that are associated with this role requires an authenticated customer.</span></span> <span data-ttu-id="2148b-121">通常、E コマース サイトでは、これらの API を使用して、注文履歴の取得や顧客の詳細の変更などの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="2148b-121">E-Commerce sites generally use these APIs for operations such as retrieving order history and changing customer details.</span></span>
- <span data-ttu-id="2148b-122">**アプリケーション** – このロールに関連付けられている API にアクセスするには、Azure Active Directory (Azure AD) のサービス間認証など、アプリケーション レベルの認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="2148b-122">**Application** – Access to APIs that are associated with this role requires application-level authentication, such as Azure Active Directory (Azure AD) service-to-service authentication.</span></span>
- <span data-ttu-id="2148b-123">**匿名** – このロールに関連付けられている API は、主にユーザー認証を行わない E コマース サイトによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-123">**Anonymous** – APIs that are associated with this role are primarily used by e-Commerce sites without user authentication.</span></span>
- <span data-ttu-id="2148b-124">**カスタマイズされた API** – このロールに関連付けられている API へのアクセスを制限するには、POS デバイスの有効化、顧客認証、匿名認証などの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="2148b-124">**Customized APIs** – Access to APIs that are associated with this role can be restricted by using methods such as POS device activation, customer authentication, and anonymous authentication.</span></span>

<span data-ttu-id="2148b-125">外部アプリケーションの統合では、API にアクセスするために**アプリケーション**認証フローのみを必要とします。</span><span class="sxs-lookup"><span data-stu-id="2148b-125">External application integration requires only the **Application** authentication flow to access the APIs.</span></span> <span data-ttu-id="2148b-126">E コマース アプリケーションの統合には、**顧客**認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="2148b-126">E-commerce application integration requires **Customer** authentication.</span></span>

<span data-ttu-id="2148b-127">このトピックでは、**アプリケーション認証**フローの設定と、**アプリケーション**認証コンテキストを使用した API へのアクセスに重点を置いて説明します。</span><span class="sxs-lookup"><span data-stu-id="2148b-127">This topic is focused on setting up **Application** authentication flows and accessing the APIs by using the **Application** authentication context.</span></span>

<span data-ttu-id="2148b-128">外部アプリケーションから API にアクセスする前に、外部アプリケーションを Azure アプリ登録に登録する必要があります。また、登録されたアプリケーションの詳細を Commerce Headquarters に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2148b-128">Before the APIs are accessed from an external application, the external application must be registered in Azure App registration, and details of the registered application must be added in the Commerce Headquarters.</span></span>

<span data-ttu-id="2148b-129">認証フローの詳細については、[Dynamics 365 Commerce 認証フロー](../arch-auth-flow.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2148b-129">For more information about authentication flows, see [Dynamics 365 Commerce authentication flows](../arch-auth-flow.md).</span></span>

## <a name="register-the-application-in-azure-app-registration"></a><span data-ttu-id="2148b-130">Azure アプリ登録で、アプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="2148b-130">Register the application in Azure App registration</span></span>

<span data-ttu-id="2148b-131">アプリケーションの登録は、アプリと Microsoft ID プラットフォームとの間に信頼関係を確立します。</span><span class="sxs-lookup"><span data-stu-id="2148b-131">Application registration establishes a trust relationship between your app and the Microsoft identity platform.</span></span> <span data-ttu-id="2148b-132">信頼は単一方向で、アプリケーションは Microsoft ID プラットフォームを信頼しますが、逆向きでは信頼されません。</span><span class="sxs-lookup"><span data-stu-id="2148b-132">The trust is unidirectional: your app trusts the Microsoft identity platform, not the other way around.</span></span> <span data-ttu-id="2148b-133">アプリの登録を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2148b-133">Follow these steps to create the app registration.</span></span>

1. <span data-ttu-id="2148b-134">[Azure ポータル](https://portal.azure.com/)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="2148b-134">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
2. <span data-ttu-id="2148b-135">複数のテナントへのアクセス許可がある場合は、トップメニューの**ディレクトリ + 購読**フィルターを使用して、アプリケーションを登録するテナントを選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-135">If you have access to multiple tenants, use the **Directory + subscription** filter on the top menu to select the tenant that you want to register an application in.</span></span>
3. <span data-ttu-id="2148b-136">**Azure Active Directory** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-136">Search for and select **Azure Active Directory**.</span></span>
4. <span data-ttu-id="2148b-137">**管理**で、**アプリの登録**を選択し、**新規登録**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-137">Under **Manage**, select **App registrations**, and then select **New registration**.</span></span>
5. <span data-ttu-id="2148b-138">アプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2148b-138">Enter a name for your application.</span></span> <span data-ttu-id="2148b-139">アプリのユーザーにはこの名前が表示されます。後で変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="2148b-139">Users of your app might see this name, and you can change it later.</span></span>
6. <span data-ttu-id="2148b-140">**この組織ディレクトリのアカウントのみ (Microsoft のみ、単一テナント)** としてこのアプリケーションを使用できるユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2148b-140">Specify who can use this application as **Accounts in this organizational directory only (Microsoft only - Single tenant)**.</span></span>
7. <span data-ttu-id="2148b-141">**URI のリダイレクト**フィールドは既定値のままにします。</span><span class="sxs-lookup"><span data-stu-id="2148b-141">In the **Redirect URI** field, leave the default value.</span></span> <span data-ttu-id="2148b-142">何も変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="2148b-142">Don't change anything.</span></span>
8. <span data-ttu-id="2148b-143">**登録**を選択して、最初のアプリ登録を行います。</span><span class="sxs-lookup"><span data-stu-id="2148b-143">Select **Register** to complete the initial app registration.</span></span>

<span data-ttu-id="2148b-144">登録が完了すると、Azure ポータルに、アプリ登録の**概要**ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-144">When registration is completed, the Azure portal shows the **Overview** pane for the app registration.</span></span> <span data-ttu-id="2148b-145">このウィンドウには、**アプリケーション (クライアント) ID** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-145">This pane includes the **Application (client) ID** field.</span></span> <span data-ttu-id="2148b-146">このフィールドの値は、*アプリケーション ID* または*クライアント ID* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2148b-146">The value of this field is known as the *application ID* or the *client ID*.</span></span> <span data-ttu-id="2148b-147">Microsoft ID プラットフォームでアプリケーションを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="2148b-147">It uniquely identifies your application in the Microsoft identity platform.</span></span>

### <a name="add-a-client-secret"></a><span data-ttu-id="2148b-148">クライアント シークレットの追加</span><span class="sxs-lookup"><span data-stu-id="2148b-148">Add a client secret</span></span>

<span data-ttu-id="2148b-149">クライアント シークレットは、*アプリケーション パスワード*と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="2148b-149">The client secret is also known as an *application password*.</span></span> <span data-ttu-id="2148b-150">これは、アプリが、自身の ID に対する証明書の代わりとして使用できる文字列値です。</span><span class="sxs-lookup"><span data-stu-id="2148b-150">It's a string value that your app can use instead of a certificate to identity itself.</span></span>

1. <span data-ttu-id="2148b-151">Azure ポータルの**アプリの登録**で、アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-151">In the Azure portal, in **App registrations**, select your application.</span></span>
2. <span data-ttu-id="2148b-152">**証明書とシークレット** &gt; **新しいクライアント シークレット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-152">Select **Certificates & secrets** &gt; **New client secret**.</span></span>
3. <span data-ttu-id="2148b-153">クライアント シークレットの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2148b-153">Add a description for your client secret.</span></span>
4. <span data-ttu-id="2148b-154">期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-154">Select a duration.</span></span>
5. <span data-ttu-id="2148b-155">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-155">Select **Add**.</span></span>
6. <span data-ttu-id="2148b-156">シークレットの値は、クライアント アプリケーション コードで使用できるように必ず書き留めてください。</span><span class="sxs-lookup"><span data-stu-id="2148b-156">Be sure to record the secret's value so that you can use it in your client application code.</span></span> <span data-ttu-id="2148b-157">**このページから移動すると、シークレットの値が再度表示されることはありません。**</span><span class="sxs-lookup"><span data-stu-id="2148b-157">**The secret's value is never displayed again after you leave this page.**</span></span>

## <a name="register-the-app-in-the-finance-and-operations-app-so-that-retail-server-trusts-it"></a><span data-ttu-id="2148b-158">Retail Server から信頼されるようにするため、Finance and Operations アプリで、対象アプリを登録する</span><span class="sxs-lookup"><span data-stu-id="2148b-158">Register the app in the Finance and Operations app so that Retail Server trusts it</span></span>

1. <span data-ttu-id="2148b-159">Commerce Headquarters で、**Retail と Commerce** &gt; **本社の設定** &gt; **パラメーター** &gt; **Commerce 共有パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2148b-159">In Commerce Headquarters, go to **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce shared parameters**.</span></span>
2. <span data-ttu-id="2148b-160">**ID プロバイダー** クイック タブで、`HTTPS://sts.windows.net/` で始まるプロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-160">On the **Identity providers** FastTab, select the provider that begins with `HTTPS://sts.windows.net/`.</span></span> <span data-ttu-id="2148b-161">選択に基づいて、**依存する関係者**クイック タブの値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-161">The values on the **Relying parties** FastTab are set based on your selection.</span></span>
3. <span data-ttu-id="2148b-162">**依存する関係者**クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-162">On the **Relying parties** FastTab, select **Add**.</span></span> <span data-ttu-id="2148b-163">Azure でアプリの登録時に生成されたクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="2148b-163">Enter the client ID that was generated during the app registration in Azure.</span></span> <span data-ttu-id="2148b-164">**Type** フィールドを**機密情報**に、**UserType**フィールドを**アプリケーション**に設定します。</span><span class="sxs-lookup"><span data-stu-id="2148b-164">Set the **Type** field to **Confidential** and the **UserType** field to **Application**.</span></span>
4. <span data-ttu-id="2148b-165">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-165">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="2148b-166">新しい依存する関係者を選択し、**サーバー リソース ID** クイック タブで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-166">Select the new relying party, and then, on the **Server resource IDs** FastTab, select **Add**.</span></span> <span data-ttu-id="2148b-167">**サーバー リソース ID** 列に、Retail Server の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="2148b-167">In the **Server Resource ID** column, enter the Retail Server URL.</span></span>
6. <span data-ttu-id="2148b-168">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2148b-168">On the Action Pane, select **Save**.</span></span>
7. <span data-ttu-id="2148b-169">**Retail と Commerce** &gt; **Retail および Commerce IT** &gt; **配送スケジュール**の順に移動し、Commerce Data Exchange (CDX) ジョブ **1110** を実行します。</span><span class="sxs-lookup"><span data-stu-id="2148b-169">Go to **Retail and commerce** &gt; **Retail and commerce IT** &gt; **Distribution Schedule**, and run Commerce Data Exchange (CDX) job **1110**.</span></span>

## <a name="access-the-apis-by-using-postman"></a><span data-ttu-id="2148b-170">Postman を使用した API へのアクセス</span><span class="sxs-lookup"><span data-stu-id="2148b-170">Access the APIs by using Postman</span></span>

<span data-ttu-id="2148b-171">いくつかのサードパーティ製ツールを使用すると、Azure サービスでの認証、Web API 要求の作成と送信、および応答の表示を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2148b-171">Several third-party tools let you authenticate with Azure services, compose and send Web API requests, and view responses.</span></span> <span data-ttu-id="2148b-172">Postman は、最も普及しているツールの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="2148b-172">Postman is one of the most popular tools.</span></span> <span data-ttu-id="2148b-173">[Postman クライアント ツールのダウンロードとインストール](https://www.postman.com/)。</span><span class="sxs-lookup"><span data-stu-id="2148b-173">[Download and install the Postman client tool](https://www.postman.com/).</span></span>

<span data-ttu-id="2148b-174">この例では、**GetOrderHistory** API にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2148b-174">For this example, you will access the **GetOrderHistory** API.</span></span> <span data-ttu-id="2148b-175">この API は、特定の顧客の注文履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="2148b-175">This API retrieves the order history for a specific customer.</span></span> <span data-ttu-id="2148b-176">**従業員**、**顧客**、または**アプリケーション**の認証コンテキストを使用してのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2148b-176">It can be accessed only by using the **Employee**, **Customer** or **Application** authorization context.</span></span> <span data-ttu-id="2148b-177">対象アプリケーションには**アプリケーション**認証コンテキストがあるため、**GetOrderHistory** API にアクセスして顧客注文履歴を取得できます。</span><span class="sxs-lookup"><span data-stu-id="2148b-177">Because your application has the **Application** authorization context, it can access the **GetOrderHistory** API and get the customer order history.</span></span>

<span data-ttu-id="2148b-178">API にアクセスするには、最初に認証トークンを生成します。</span><span class="sxs-lookup"><span data-stu-id="2148b-178">To access the API, you first generate the authorization token.</span></span> <span data-ttu-id="2148b-179">その後、その認証トークンを使用して API にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2148b-179">You then use that authorization token to access the API.</span></span>

<span data-ttu-id="2148b-180">すべての API の一覧については、[Commerce Scale Unit 顧客およびコンシューマー API](retail-server-customer-consumer-api.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2148b-180">For the full list of APIs, see [Commerce Scale Unit customer and consumer APIs](retail-server-customer-consumer-api.md).</span></span>

### <a name="generate-an-authorization-token-by-using-postman"></a><span data-ttu-id="2148b-181">Postman を使用した認証トークンの生成</span><span class="sxs-lookup"><span data-stu-id="2148b-181">Generate an authorization token by using Postman</span></span>

1. <span data-ttu-id="2148b-182">Postman で、以下の要求 URL と本文パラメータを持つ GET 要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="2148b-182">In Postman, create a GET request that has the following request URL and body parameters.</span></span>

    <span data-ttu-id="2148b-183">**要求 URL**</span><span class="sxs-lookup"><span data-stu-id="2148b-183">**Request URL**</span></span>

    ```rest
    https://login.microsoftonline.com/{tenant-id}/oauth2/token
    ```

    > [!NOTE]
    > <span data-ttu-id="2148b-184">テナント ID は、Azure アプリの登録の**概要**ウィンドウから取得できます。</span><span class="sxs-lookup"><span data-stu-id="2148b-184">You can get the tenant ID from the **Overview** pane for your Azure app registration.</span></span> <span data-ttu-id="2148b-185">クライアント ID の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-185">It's shown next to the client ID.</span></span>

    <span data-ttu-id="2148b-186">**本文パラメータ**</span><span class="sxs-lookup"><span data-stu-id="2148b-186">**Body parameters**</span></span>

    | <span data-ttu-id="2148b-187">キー</span><span class="sxs-lookup"><span data-stu-id="2148b-187">Key</span></span>            | <span data-ttu-id="2148b-188">先頭値</span><span class="sxs-lookup"><span data-stu-id="2148b-188">Value</span></span>                                                              |
    |----------------|--------------------------------------------------------------------|
    | <span data-ttu-id="2148b-189">grant\_type</span><span class="sxs-lookup"><span data-stu-id="2148b-189">grant\_type</span></span>    | <span data-ttu-id="2148b-190">**client\_credentials**</span><span class="sxs-lookup"><span data-stu-id="2148b-190">**client\_credentials**</span></span>                                            |
    | <span data-ttu-id="2148b-191">client\_id</span><span class="sxs-lookup"><span data-stu-id="2148b-191">client\_id</span></span>     | <span data-ttu-id="2148b-192">Azure アプリの登録時に生成されたクライアント ID</span><span class="sxs-lookup"><span data-stu-id="2148b-192">The client ID that was generated during Azure app registration</span></span>     |
    | <span data-ttu-id="2148b-193">client\_secret</span><span class="sxs-lookup"><span data-stu-id="2148b-193">client\_secret</span></span> | <span data-ttu-id="2148b-194">Azure アプリの登録時に生成されたクライアント シークレット</span><span class="sxs-lookup"><span data-stu-id="2148b-194">The client secret that was generated during Azure app registration</span></span> |
    | <span data-ttu-id="2148b-195">リソース</span><span class="sxs-lookup"><span data-stu-id="2148b-195">resource</span></span>       | <span data-ttu-id="2148b-196">Retail Server の URL</span><span class="sxs-lookup"><span data-stu-id="2148b-196">The Retail Server URL</span></span>                                              |

2. <span data-ttu-id="2148b-197">要求が実行を完了すると、応答本文に **access\_token** の値が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2148b-197">After the request has finished running, the **access\_token** value will be generated in the response body.</span></span> <span data-ttu-id="2148b-198">このトークンの値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="2148b-198">Copy this token value.</span></span> <span data-ttu-id="2148b-199">Retail Server に接続するためにこれを使用します。</span><span class="sxs-lookup"><span data-stu-id="2148b-199">You will use it to connect to the Retail Server.</span></span>

### <a name="get-order-history-by-using-postman"></a><span data-ttu-id="2148b-200">Postman を使用した注文履歴の取得</span><span class="sxs-lookup"><span data-stu-id="2148b-200">Get order history by using Postman</span></span>

- <span data-ttu-id="2148b-201">Postman で、以下の要求 URL、パラメーター、およびヘッダー パラメーターを持つ POST 要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="2148b-201">In Postman, create a POST request that has the following request URL, parameters, and header parameters.</span></span>

    <span data-ttu-id="2148b-202">**要求 URL**</span><span class="sxs-lookup"><span data-stu-id="2148b-202">**Request URL**</span></span>

    ```rest
    <https://Retail>serverurl/Commerce/Customers('2001')/GetOrderHistory
    ```

    > [!NOTE]
    > <span data-ttu-id="2148b-203">**2001** をご自身の顧客 ID に置換します。</span><span class="sxs-lookup"><span data-stu-id="2148b-203">Replace **2001** with your own customer ID.</span></span>

    <span data-ttu-id="2148b-204">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="2148b-204">**Parameters**</span></span>

    | <span data-ttu-id="2148b-205">キー</span><span class="sxs-lookup"><span data-stu-id="2148b-205">Key</span></span>         | <span data-ttu-id="2148b-206">先頭値</span><span class="sxs-lookup"><span data-stu-id="2148b-206">Value</span></span> |
    |-------------|-------|
    | <span data-ttu-id="2148b-207">$top</span><span class="sxs-lookup"><span data-stu-id="2148b-207">$top</span></span>        | <span data-ttu-id="2148b-208">10</span><span class="sxs-lookup"><span data-stu-id="2148b-208">10</span></span>    |
    | <span data-ttu-id="2148b-209">API のバージョン</span><span class="sxs-lookup"><span data-stu-id="2148b-209">api-version</span></span> | <span data-ttu-id="2148b-210">7.3</span><span class="sxs-lookup"><span data-stu-id="2148b-210">7.3</span></span>   |

    <span data-ttu-id="2148b-211">**ヘッダー パラメーター**</span><span class="sxs-lookup"><span data-stu-id="2148b-211">**Header parameters**</span></span>

    | <span data-ttu-id="2148b-212">キー</span><span class="sxs-lookup"><span data-stu-id="2148b-212">Key</span></span>           | <span data-ttu-id="2148b-213">先頭値</span><span class="sxs-lookup"><span data-stu-id="2148b-213">Value</span></span>                                            |
    |---------------|--------------------------------------------------|
    | <span data-ttu-id="2148b-214">OUN</span><span class="sxs-lookup"><span data-stu-id="2148b-214">OUN</span></span>           | <span data-ttu-id="2148b-215">この小売チャネルの作業単位番号</span><span class="sxs-lookup"><span data-stu-id="2148b-215">The operating unit number of this retail channel</span></span> |
    | <span data-ttu-id="2148b-216">認証</span><span class="sxs-lookup"><span data-stu-id="2148b-216">authorization</span></span> | <span data-ttu-id="2148b-217">**id\_token { access\_token }**</span><span class="sxs-lookup"><span data-stu-id="2148b-217">**id\_token { access\_token }**</span></span>                  |

    > [!NOTE]
    > <span data-ttu-id="2148b-218">**Access_token** については、認証要求で生成された **access_token** の値をコピーして貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2148b-218">For **access_token**, copy and paste the **access_token** value that was generated in the authorization request.</span></span> <span data-ttu-id="2148b-219">次に **id_token** を接頭語として付けます。</span><span class="sxs-lookup"><span data-stu-id="2148b-219">Then prefix it with **id_token**.</span></span>

<span data-ttu-id="2148b-220">要求の実行が完了した後、応答の本文には顧客注文履歴が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2148b-220">After the request has finished running, the response body will contain the customer order history.</span></span>

## <a name="access-the-retail-server-apis-by-using-a-console-application"></a><span data-ttu-id="2148b-221">コンソール アプリケーションを使用した Retail Server API へのアクセス</span><span class="sxs-lookup"><span data-stu-id="2148b-221">Access the Retail Server APIs by using a console application</span></span>

1. <span data-ttu-id="2148b-222">Visual Studio 2017 を使用して、コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="2148b-222">Use Visual Studio 2017 to create a console application.</span></span>
2. <span data-ttu-id="2148b-223">**App.config** ファイルには、次のコンフィギュレーションを含めます。</span><span class="sxs-lookup"><span data-stu-id="2148b-223">In the **app.config** file, include the following configuration.</span></span>

    ```xml
    <appSettings>
        <add key="aadClientId" value="client id generated during app registration in Azure" />
        <add key="aadClientSecret" value="client secret generated during app registration in Azure" />
        <add key="aadAuthority" value="https://sts.windows.net/tenant id/" />
        <add key="retailServerUrl" value="https://RetailserverURL/Commerce" />
        <add key="resource" value="https://REtailServerURL" />
        <add key="operatingUnitNumber" value="OUN value" />
    </appSettings>
    ```

### <a name="update-the-configuration-settings-with-actual-values"></a><span data-ttu-id="2148b-224">実際の値によるコンフィギュレーション設定の更新</span><span class="sxs-lookup"><span data-stu-id="2148b-224">Update the configuration settings with actual values</span></span>

1. <span data-ttu-id="2148b-225">プロジェクトの NuGet パッケージ マネージャを使用して、以下の NuGet パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="2148b-225">Use the NuGet package manager for the project to add the following NuGet packages.</span></span>

    + <span data-ttu-id="2148b-226">Microsoft.IdentityModel.Clients.ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2148b-226">Microsoft.IdentityModel.Clients.ActiveDirectory</span></span>
    + <span data-ttu-id="2148b-227">Microsoft.Dynamics.Commerce.RetailProxy</span><span class="sxs-lookup"><span data-stu-id="2148b-227">Microsoft.Dynamics.Commerce.RetailProxy</span></span>

    <span data-ttu-id="2148b-228">**Microsoft.Dynamics.Commerce.RetailProxy** NuGet パッケージは、**RetailSDK\\Pkgs** フォルダから追加することができます。</span><span class="sxs-lookup"><span data-stu-id="2148b-228">The **Microsoft.Dynamics.Commerce.RetailProxy** NuGet package can be added from the **RetailSDK\\pkgs** folder.</span></span> <span data-ttu-id="2148b-229">NuGet マネージャで、**RetailSDK\\pkgs** フォルダのローカル リポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="2148b-229">In the NuGet manager, add a local repository for the **RetailSDK\\pkgs** folder.</span></span>

2. <span data-ttu-id="2148b-230">**Program.cs** ファイルに、以下の変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="2148b-230">In the **Program.cs** file, add the following variables.</span></span>

    ```C#
    private static string clientId;
    private static string clientSecret;
    private static Uri retailServerUrl;
    private static string resource;
    private static string operatingUnitNumber;
    private static Uri authority;
    ```

3. <span data-ttu-id="2148b-231">**Program.cs** ファイルに、アプリ設定を読み取るための **GetConfiguration** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2148b-231">In the **Program.cs** file, add the **GetConfiguration** method to read the app settings.</span></span>

    ```C#
    private static void GetConfiguration()
    {
        clientId = ConfigurationManager.AppSettings["aadClientId"];
        clientSecret = ConfigurationManager.AppSettings["aadClientSecret"];
        authority = new Uri(ConfigurationManager.AppSettings["aadAuthority"]);
        retailServerUrl = new Uri(ConfigurationManager.AppSettings["retailServerUrl"]);
        operatingUnitNumber = ConfigurationManager.AppSettings["operatingUnitNumber"];
        resource = ConfigurationManager.AppSettings["resource"];
    }
    ```

4. <span data-ttu-id="2148b-232">**Program.cs** ファイルに、アクセス トークンを取得するための **CreateManagerFactory** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2148b-232">In the **Program.cs** file, add the **CreateManagerFactory** method to get the access token.</span></span>

    ```C#
    private static async Task<ManagerFactory> CreateManagerFactory()
    {
        Microsoft.IdentityModel.Clients.ActiveDirectory.AuthenticationContext authenticationContext = new   Microsoft.IdentityModel.Clients.ActiveDirectory.AuthenticationContext(authority.ToString(), false);
        AuthenticationResult authResult = null;
        authResult = await authenticationContext.AcquireTokenAsync(resource, new ClientCredential(clientId, clientSecret));

        ClientCredentialsToken clientCredentialsToken = new ClientCredentialsToken(authResult.AccessToken);
        RetailServerContext retailServerContext = RetailServerContext.Create(retailServerUrl, operatingUnitNumber, clientCredentialsToken);
        ManagerFactory factory = ManagerFactory.Create(retailServerContext);
        return factory;
    }
    ```

5. <span data-ttu-id="2148b-233">**GetOrderHistory** メソッドを追加して、注文を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2148b-233">Add the **GetOrderHistory** method to read the orders.</span></span>

    ```C#
    private static async Task<Microsoft.Dynamics.Commerce.RetailProxy.PagedResult<SalesOrder>> GetOrderHistory(string customerId)
    {
        QueryResultSettings querySettings = new QueryResultSettings
        {
            Paging = new PagingInfo() { Top = 10, Skip = 10 }
        };

        ManagerFactory managerFactory = await CreateManagerFactory();
        ICustomerManager customerManage = managerFactory.GetManager<ICustomerManager>();
        return await customerManage.GetOrderHistory(customerId, querySettings);
    }
    ```

6. <span data-ttu-id="2148b-234">**Main** メソッドでは、**GetOrderHistory** メソッドを呼び出してレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2148b-234">In the **main** method, call the **GetOrderHistory** method to read the records.</span></span>

    ```C#
    static void Main(string[] args)
    {
        GetConfiguration();
        Microsoft.Dynamics.Commerce.RetailProxy.PagedResult<SalesOrder> orderHistory = Task.Run(async () => await GetOrderHistory("2001")).Result;
        Console.WriteLine(orderHistory.FirstOrDefault<SalesOrder>().Id);
    }
    ```
