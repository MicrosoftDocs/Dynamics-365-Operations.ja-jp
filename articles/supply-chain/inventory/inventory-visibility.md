---
title: 在庫の視覚化アドイン
description: このトピックでは、Dynamics 365 Supply Chain Management の在庫の視覚化アドインのインストールおよび構成方法を説明します。
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114673"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="9cfab-103">在庫の視覚化アドイン</span><span class="sxs-lookup"><span data-stu-id="9cfab-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="9cfab-104">Inventory Visibility Add-in は、リアルタイムで手持在庫を追跡可能できる独立したスケーラブルなマイクロサービスで、グローバルなビューの在庫表示が実現します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="9cfab-105">手持在庫に関連するすべての情報は、低レベルの SQL 統合を通じて準リアルタイムでサービスにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="9cfab-106">外部システムは RESTful APIs を通じてサービスにアクセスし、指定された分析コードの組み合わせに関する手持在庫情報にクエリを実行します。こうすることで使用可能な手持在庫の一覧を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="9cfab-107">Inventory Visibility は、Microsoft Dataverse に構築されたマイクロサービスなので、Power Apps を構築および Power BI を適用することで拡張し、カスタマイズした機能を提供して、業務要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="9cfab-108">インデックスをアップグレードして在庫クエリを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="9cfab-109">Inventory Visibility には、複数のサードパーティ システムと統合できる構成オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9cfab-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="9cfab-110">このオプションでは、標準化された在庫分析コード、カスタマイズされた拡張性、標準化され構成可能な計算済の数量がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="9cfab-111">このトピックでは、Inventory Visibility Add-in for Dynamics 365 Supply Chain Management のインストールおよび構成方法、およびアプリケーション プログラミング インターフェイス (API) の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="9cfab-112">Inventory Visibility Add-in をインストールする</span><span class="sxs-lookup"><span data-stu-id="9cfab-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="9cfab-113">Microsoft Dynamics Lifecycle Services (LCS) を使用して、 Inventory Visibility Add-in をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9cfab-114">LCS が提供する環境や定期的に更新されるサービスにより、Dynamics 365 Finance and Operations アプリのアプリケーション ライフサイクルを管理するのが楽になります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="9cfab-115">詳細については、 [Lifecycle Services のリソース](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9cfab-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9cfab-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="9cfab-116">Prerequisites</span></span>

<span data-ttu-id="9cfab-117">Inventory Visibility Add-in をインストールする前に、以下を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="9cfab-118">少なくとも 1 つの環境が配置されている LCS 実装プロジェクトを取得する。</span><span class="sxs-lookup"><span data-stu-id="9cfab-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="9cfab-119">LCS でのオファリングで使用するベータ キーを生成する。</span><span class="sxs-lookup"><span data-stu-id="9cfab-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="9cfab-120">LCS でのユーザーに対するオファリングのベータ キーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9cfab-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="9cfab-121">Microsoft Inventory Visibility 製品チームに連絡して、Inventory Visibility Add-in を配置する環境 ID を知らせてください。</span><span class="sxs-lookup"><span data-stu-id="9cfab-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="9cfab-122">これらの前提条件について質問がある場合は、Inventory Visibility 製品チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="9cfab-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="9cfab-123">アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="9cfab-123">Install the add-in</span></span>

<span data-ttu-id="9cfab-124">Inventory Visibility Add-in をインストールするには、以下を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="9cfab-125">[Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) ポータルにサインインします。</span><span class="sxs-lookup"><span data-stu-id="9cfab-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="9cfab-126">ホーム ページで、環境が展開されているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="9cfab-127">プロジェクト ページで、アドインをインストールする環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="9cfab-128">環境 ページで、**環境アドイン** セクションが表示されるまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="9cfab-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="9cfab-129">セクションが表示されない場合は、必須のベータ キーが完全に処理されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9cfab-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="9cfab-130">**環境アドイン** セクションで、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="9cfab-131">![LCS の環境ページ](media/inventory-visibility-environment.png "LCS の環境ページ")</span><span class="sxs-lookup"><span data-stu-id="9cfab-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="9cfab-132">**新しいアドインのインストール** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="9cfab-133">使用可能なアドインの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="9cfab-134">一覧から **在庫サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="9cfab-135">(**Inventory Visibility Add-in for Dynamics 365 Supply Chain Management** として一覧表示される場合があります。)</span><span class="sxs-lookup"><span data-stu-id="9cfab-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="9cfab-136">環境に対して次のフィールドの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="9cfab-137">**AAD アプリケーション ID**</span><span class="sxs-lookup"><span data-stu-id="9cfab-137">**AAD application ID**</span></span>
    - <span data-ttu-id="9cfab-138">**AAD テナント ID**</span><span class="sxs-lookup"><span data-stu-id="9cfab-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="9cfab-139">![セットアップ ページに追加](media/inventory-visibility-setup.png "アドイン セットアップ ページ")</span><span class="sxs-lookup"><span data-stu-id="9cfab-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="9cfab-140">**使用条件** チェック ボックスを選択して、使用条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="9cfab-141">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-141">Select **Install**.</span></span> <span data-ttu-id="9cfab-142">アドインの状態は、**インストール中** として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="9cfab-143">完了したらページを更新して、状態が **インストール済み** に変わっているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="9cfab-144">セキュリティ サービス トークンの取得</span><span class="sxs-lookup"><span data-stu-id="9cfab-144">Get a security service token</span></span>

<span data-ttu-id="9cfab-145">セキュリティ サービス トークンを取得するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9cfab-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="9cfab-146">Azure Portalにログインし、このログインを使用して Supply Chain Management アプリケーションの `clientId` と `clientSecret` を探します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="9cfab-147">次のプロパティを持つ HTTP 要求を送信することにより、 Azure Active Directory トークン (`aadToken`) をフェッチします。</span><span class="sxs-lookup"><span data-stu-id="9cfab-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="9cfab-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="9cfab-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="9cfab-149">**メソッド** - `GET`</span><span class="sxs-lookup"><span data-stu-id="9cfab-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="9cfab-150">**本文の内容 (フォーム データ)**:</span><span class="sxs-lookup"><span data-stu-id="9cfab-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="9cfab-151">キー</span><span class="sxs-lookup"><span data-stu-id="9cfab-151">key</span></span> | <span data-ttu-id="9cfab-152">値</span><span class="sxs-lookup"><span data-stu-id="9cfab-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="9cfab-153">クライアント ID</span><span class="sxs-lookup"><span data-stu-id="9cfab-153">client_id</span></span> | <span data-ttu-id="9cfab-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="9cfab-154">${aadAppId}</span></span> |
        | <span data-ttu-id="9cfab-155">クライアント シークレット</span><span class="sxs-lookup"><span data-stu-id="9cfab-155">client_secret</span></span> | <span data-ttu-id="9cfab-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="9cfab-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="9cfab-157">付与タイプ</span><span class="sxs-lookup"><span data-stu-id="9cfab-157">grant_type</span></span> | <span data-ttu-id="9cfab-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="9cfab-158">client_credentials</span></span> |
        | <span data-ttu-id="9cfab-159">リソース</span><span class="sxs-lookup"><span data-stu-id="9cfab-159">resource</span></span> | <span data-ttu-id="9cfab-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="9cfab-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="9cfab-161">応答で `aadToken` を受け取っている必要があります。これは次の例と似ています。</span><span class="sxs-lookup"><span data-stu-id="9cfab-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="9cfab-162">次に似た JSON 要求を形成します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="9cfab-163">場所:</span><span class="sxs-lookup"><span data-stu-id="9cfab-163">Where:</span></span>
    - <span data-ttu-id="9cfab-164">`client_assertion` 値は、前の手順で受け取った `aadToken` である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="9cfab-165">この `context` 値は、アドインを配置する環境 ID である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="9cfab-166">例に示すように、他のすべての値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="9cfab-167">次のプロパティを使用して HTTP 要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="9cfab-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="9cfab-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="9cfab-169">**メソッド** - `POST`</span><span class="sxs-lookup"><span data-stu-id="9cfab-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="9cfab-170">**HTTP ヘッダー** - API バージョンを含めます (キーは `Api-Version` で値は `1.0` です)</span><span class="sxs-lookup"><span data-stu-id="9cfab-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="9cfab-171">**本文の内容** - 前の手順で作成した JSON 要求を含めます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="9cfab-172">`access_token` を取得します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="9cfab-173">これは、Inventory Visibility API を呼び出すためのベアラー トークンとして必要なものです。</span><span class="sxs-lookup"><span data-stu-id="9cfab-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="9cfab-174">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="9cfab-175">アドインのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9cfab-175">Uninstall the add-in</span></span>

<span data-ttu-id="9cfab-176">アドインをアンインストールするには、**アンインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="9cfab-177">LCS を更新すると、Inventory Visibility Add-in が削除されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="9cfab-178">アンインストールのプロセスでは、アドイン登録が削除され、サービスに格納されているすべてのビジネス データをクリーンアップするジョブが開始されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="9cfab-179">Inventory Visibility Add-in パブリック API</span><span class="sxs-lookup"><span data-stu-id="9cfab-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="9cfab-180">Inventory Visibility Add-in のパブリック REST API は、特定の統合エンドポイントを複数提供します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="9cfab-181">次の 3 つの主要な相互作用タイプをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9cfab-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="9cfab-182">外部システムから、手持在庫の変更をアドインに転記する。</span><span class="sxs-lookup"><span data-stu-id="9cfab-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="9cfab-183">外部システムから現在の手持在庫数量を問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="9cfab-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="9cfab-184">手持ちの Supply Chain Management との自動同期。</span><span class="sxs-lookup"><span data-stu-id="9cfab-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="9cfab-185">自動同期はパブリック API には含まれませんが、Inventory Visibility Add-in が有効な環境ではバックグラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="9cfab-186">認証</span><span class="sxs-lookup"><span data-stu-id="9cfab-186">Authentication</span></span>

<span data-ttu-id="9cfab-187">プラットフォーム セキュリティ トークンは、Inventory Visibility Add-in を呼び出すために使用されるので、Azure Active Directory アプリケーションを使用して Azure Active Directory トークンを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="9cfab-188">セキュリティ トークンを取得する方法の詳細については、[Inventory Visibility Add-in のインストール](#install-add-in) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9cfab-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="9cfab-189">Inventory Visibility API の構成</span><span class="sxs-lookup"><span data-stu-id="9cfab-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="9cfab-190">このサービスを使用する前に、次のサブセクションで説明する構成を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="9cfab-191">環境の詳細によって、構成が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="9cfab-192">主に 4 つの部分から構成されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="9cfab-193">パーティション分割</span><span class="sxs-lookup"><span data-stu-id="9cfab-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="9cfab-194">分析コードの構成</span><span class="sxs-lookup"><span data-stu-id="9cfab-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="9cfab-195">インデックスの作成中</span><span class="sxs-lookup"><span data-stu-id="9cfab-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="9cfab-196">カスタム測定</span><span class="sxs-lookup"><span data-stu-id="9cfab-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="9cfab-197">パーティション分割</span><span class="sxs-lookup"><span data-stu-id="9cfab-197">Partitioning</span></span>

<span data-ttu-id="9cfab-198">パーティション分割は、Inventory Visibility API のパフォーマンスに大きな影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="9cfab-199">有意義なデータ クエリの使用を妥協せずに、データを小規模にグループ化できるスキームを定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9cfab-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="9cfab-200">`organizationId` (Supply Chain Management の `dataAreaId`) は、常にパーティション分割に含まれており、Inventory Visibility は既定で、*サイト + 場所* として分析コードごとのパーティション分割が設定されているので、</span><span class="sxs-lookup"><span data-stu-id="9cfab-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="9cfab-201">フィルターで定義された分析コードで、サービスを常にクエリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="9cfab-202">*サイト* および *場所* は、Inventory Visibility で使用する 2 つの既定の標準分析コードです。</span><span class="sxs-lookup"><span data-stu-id="9cfab-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="9cfab-203">Supply Chain Management では、これらの分析コードは *サイト* ( `InventSiteId`) および *倉庫* (`InventLocationId`) と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="9cfab-204">分析コードの構成</span><span class="sxs-lookup"><span data-stu-id="9cfab-204">Dimension configurations</span></span>

<span data-ttu-id="9cfab-205">Inventory Visibility に既定の標準分析コードの一覧が用意されており、複数のソース システムの統合を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="9cfab-206">次のテーブルでは、Inventory Visibility で既定の分析コード名となる在庫分析コードを一覧表示しています。</span><span class="sxs-lookup"><span data-stu-id="9cfab-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="9cfab-207">分析コード タイプ</span><span class="sxs-lookup"><span data-stu-id="9cfab-207">Dimension type</span></span> | <span data-ttu-id="9cfab-208">分析コード名</span><span class="sxs-lookup"><span data-stu-id="9cfab-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="9cfab-209">品目</span><span class="sxs-lookup"><span data-stu-id="9cfab-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="9cfab-210">品目</span><span class="sxs-lookup"><span data-stu-id="9cfab-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="9cfab-211">品目</span><span class="sxs-lookup"><span data-stu-id="9cfab-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="9cfab-212">品目</span><span class="sxs-lookup"><span data-stu-id="9cfab-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="9cfab-213">追跡</span><span class="sxs-lookup"><span data-stu-id="9cfab-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="9cfab-214">追跡</span><span class="sxs-lookup"><span data-stu-id="9cfab-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="9cfab-215">保管場所</span><span class="sxs-lookup"><span data-stu-id="9cfab-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="9cfab-216">保管場所</span><span class="sxs-lookup"><span data-stu-id="9cfab-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="9cfab-217">在庫状態</span><span class="sxs-lookup"><span data-stu-id="9cfab-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="9cfab-218">倉庫固有</span><span class="sxs-lookup"><span data-stu-id="9cfab-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="9cfab-219">倉庫固有</span><span class="sxs-lookup"><span data-stu-id="9cfab-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="9cfab-220">倉庫固有</span><span class="sxs-lookup"><span data-stu-id="9cfab-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="9cfab-221">前のテーブルで表示されていた分析コード タイプは、参照のみに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="9cfab-222">Inventory Visibility で分析コード タイプを定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9cfab-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="9cfab-223">カスタム分析コードが存在し、Inventory Visibility で使用したときに既定値に送る必要がある場合は、Inventory Visibility で **カスタム分析コード** 名を構成できます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="9cfab-224">RESTful APIs を使用して外部システムが Inventory Visibility へアクセスし、クエリを実行する特定の分析コードに関する手持在庫情報を入手できます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="9cfab-225">統合に関しては、Inventory Visibility を使用すると、Inventory Visibility で *ターゲット分析コード* への *外部チャネル データソース* とソース分析コードを構成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="9cfab-226">ターゲット分析コードは、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="9cfab-227">Inventory Visibility の既定分析コード</span><span class="sxs-lookup"><span data-stu-id="9cfab-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="9cfab-228">カスタム分析コード</span><span class="sxs-lookup"><span data-stu-id="9cfab-228">Custom dimensions</span></span>

<span data-ttu-id="9cfab-229">分析コードを構成する目的は、分析コードおよび分析コードを含む転記イベントに関するクエリで使用する複数のシステム統合を標準化することです。</span><span class="sxs-lookup"><span data-stu-id="9cfab-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="9cfab-230">インデックスの作成中</span><span class="sxs-lookup"><span data-stu-id="9cfab-230">Indexing</span></span>

<span data-ttu-id="9cfab-231">ほとんどの場合、手持在庫クエリは、最高 "合計" レベルのみだけではなく、在庫分析コードに基づいて集計された結果も表示することができます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="9cfab-232">Inventory Visibility を使用すると、分析コードまたは分析コードの組み合わせに基づいてインデックスを設定できるので、柔軟性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="9cfab-233">現在構成できるインデックスは、最大でわずか 5 つです。</span><span class="sxs-lookup"><span data-stu-id="9cfab-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="9cfab-234">業務上のニーズを満たすには、実装する前に、どの分析コードまたは分析コードの組み合わせを使用するかを慎重に検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="9cfab-235">たとえば、次のように製品にクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="9cfab-236">*色* と *サイズ* の分析コード別に、集計された製品の手持在庫にクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="9cfab-237">場合によっては、製品全体にクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="9cfab-238">次のように定義されているインデックスが 2 つあるとします。</span><span class="sxs-lookup"><span data-stu-id="9cfab-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="9cfab-239">空の括弧は、パーティションの製品 ID に基づいて集計されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="9cfab-240">インデックスは、`groupBy` クエリ設定に基づいた結果をどのようにグループ化できるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="9cfab-241">どの `groupBy` 値も定義しない場合、`productid` 別に合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="9cfab-242">それ以外の場合は、`groupBy` を `groupBy=ColorId&groupBy=SizeId` として定義すると、システム内の異なる色とサイズの組み合わせに基づいて複数の明細行が返されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="9cfab-243">要求本文にクエリの基準を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="9cfab-244">色とサイズを組み合わせた製品のサンプル クエリです。</span><span class="sxs-lookup"><span data-stu-id="9cfab-244">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="9cfab-245">カスタム測定</span><span class="sxs-lookup"><span data-stu-id="9cfab-245">Custom measurement</span></span>

<span data-ttu-id="9cfab-246">既定の測定数量は Supply Chain Management にリンクされていますが、既定の測定値の組み合わせで構成された数量が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="9cfab-247">そのためには、カスタム数量を構成し、手持在庫クエリの出力に追加します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="9cfab-248">この機能により、追加または削除される一連の測定を定義して、カスタム測定を作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="9cfab-249">たとえば、次のクエリ条件では、消費システムが使用できるように `MyCustomAvailableforReservation` としてカスタム測定数量を構成します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="9cfab-250">消費システム</span><span class="sxs-lookup"><span data-stu-id="9cfab-250">Consumption system</span></span> | <span data-ttu-id="9cfab-251">計算済測定</span><span class="sxs-lookup"><span data-stu-id="9cfab-251">Calculated measurers</span></span> | <span data-ttu-id="9cfab-252">データ ソース</span><span class="sxs-lookup"><span data-stu-id="9cfab-252">Data source</span></span> | <span data-ttu-id="9cfab-253">モディファイアー</span><span class="sxs-lookup"><span data-stu-id="9cfab-253">Modifier</span></span> | <span data-ttu-id="9cfab-254">モディファイアーの計算タイプ</span><span class="sxs-lookup"><span data-stu-id="9cfab-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="9cfab-255">追加</span><span class="sxs-lookup"><span data-stu-id="9cfab-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="9cfab-256">追加</span><span class="sxs-lookup"><span data-stu-id="9cfab-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="9cfab-257">減算</span><span class="sxs-lookup"><span data-stu-id="9cfab-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="9cfab-258">追加</span><span class="sxs-lookup"><span data-stu-id="9cfab-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="9cfab-259">減算</span><span class="sxs-lookup"><span data-stu-id="9cfab-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="9cfab-260">追加</span><span class="sxs-lookup"><span data-stu-id="9cfab-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="9cfab-261">追加</span><span class="sxs-lookup"><span data-stu-id="9cfab-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="9cfab-262">減算</span><span class="sxs-lookup"><span data-stu-id="9cfab-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="9cfab-263">減算</span><span class="sxs-lookup"><span data-stu-id="9cfab-263">Subtraction</span></span> |

<span data-ttu-id="9cfab-264">これを使用すると、カスタム測定数量に対するクエリが次の出力を返します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="9cfab-265">`MyCustomAvailableforReservation` 出力は、次のようにカスタム測定の計算設定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="9cfab-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="9cfab-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="9cfab-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="9cfab-267">手持在庫変更の転記</span><span class="sxs-lookup"><span data-stu-id="9cfab-267">Posting on-hand changes</span></span>

<span data-ttu-id="9cfab-268">イベントが転記される正確な URL は、地理的領域によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="9cfab-269">フォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="9cfab-270">認証されると、この URL を HTTP `POST` メソッドと一緒に使用し、手持在庫変更のイベントをサービスに送信することができます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="9cfab-271">特別なヘッダーは、HTTP 要求を通じた Dynamics 365 サービスとの通信に使用され、データがリンクされている Supply Chain Management インスタンスの環境 ID を表しています。</span><span class="sxs-lookup"><span data-stu-id="9cfab-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="9cfab-272">例:</span><span class="sxs-lookup"><span data-stu-id="9cfab-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="9cfab-273">手持在庫変更クエリの転記に関する例 1</span><span class="sxs-lookup"><span data-stu-id="9cfab-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="9cfab-274">この例では、Power Apps で分析コードの構成を設定するシナリオを紹介します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="9cfab-275">次のクエリを使用して、Power Apps で分析コードのマッピングを構成します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="9cfab-276">これで、クエリにある `dimensionDataSource` を指定してカスタム分析コード使用できます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="9cfab-277">システムが、カスタム分析コードをベース分析コードに自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="9cfab-278">手持在庫変更クエリの転記に関する例 2</span><span class="sxs-lookup"><span data-stu-id="9cfab-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="9cfab-279">この例では、Power Apps で分析コードの構成に必要なマッピングが設定されていないシナリオを示します。この場合、転記する場合もベース分析コードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="9cfab-280">`dimensionDataSource` フィールドが null 値、空白、または空白の場合は、すべての分析コードがベース分析コードである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="9cfab-281">JSON ドキュメント フィールド プロパティ</span><span class="sxs-lookup"><span data-stu-id="9cfab-281">JSON document field properties</span></span>

<span data-ttu-id="9cfab-282">以前に例として説明した JSON クエリのフィールドには、次のテーブルに表示されているプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="9cfab-283">フィールド ID</span><span class="sxs-lookup"><span data-stu-id="9cfab-283">Field ID</span></span> | <span data-ttu-id="9cfab-284">説明</span><span class="sxs-lookup"><span data-stu-id="9cfab-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="9cfab-285">特定の変更イベントの固有 ID。</span><span class="sxs-lookup"><span data-stu-id="9cfab-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="9cfab-286">この ID を使用してサービスとの通信が転記時に失敗した場合にイベントを再送信しても、同じイベントがシステムで 2 回カウントされることはありません。</span><span class="sxs-lookup"><span data-stu-id="9cfab-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="9cfab-287">イベントにリンクされている組織の ID。</span><span class="sxs-lookup"><span data-stu-id="9cfab-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="9cfab-288">これは、Supply Chain Management 組織またはデータ領域 ID にマップされます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="9cfab-289">問題の製品 ID。</span><span class="sxs-lookup"><span data-stu-id="9cfab-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="9cfab-290">手持在庫を変更する必要のある数量。</span><span class="sxs-lookup"><span data-stu-id="9cfab-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="9cfab-291">たとえば、新たにベーグルを棚に 10 個載せると、この値は 10 になります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="9cfab-292">その後、ベーグルを 3 つ棚から取るか売れた場合、この値は 3 になります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="9cfab-293">イベントやクエリ変更の転記で使用する分析コードのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="9cfab-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="9cfab-294">データ ソースを指定する場合は、指定されたデータ ソースのカスタム分析コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="9cfab-295">分析コードの構成を使用して、Inventory Visibility はカスタム分析コードを既定の標準分析コードにマップできます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="9cfab-296">`dimensionDataSource` が指定されていない場合は、クエリで既定の標準分析コードのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="9cfab-297">キーと値のペアの動的なバッグ。</span><span class="sxs-lookup"><span data-stu-id="9cfab-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="9cfab-298">これらは、Supply Chain Management の一部の分析コードにマップされますが、イベントを Supply Chain Management または外部システムから取得した場合に表示されることがあるカスタム分析コード (*ソース* など) を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="9cfab-299">現在の手持在庫に対するクエリの実行</span><span class="sxs-lookup"><span data-stu-id="9cfab-299">Querying current on-hand</span></span>

<span data-ttu-id="9cfab-300">現在の手持在庫に対してクエリを実行するためのエンドポイントは、次のような URL です。</span><span class="sxs-lookup"><span data-stu-id="9cfab-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="9cfab-301">HTTP `POST` メソッドでクエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="9cfab-302">現在の手持在庫に対するクエリ例 1</span><span class="sxs-lookup"><span data-stu-id="9cfab-302">Current on-hand query example 1</span></span>

<span data-ttu-id="9cfab-303">この例では、Power Apps で分析コードの構成がすでに完了しているシナリオを紹介します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="9cfab-304">次のクエリを使用して、Power Apps で分析コードのマッピングを構成します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="9cfab-305">これで、クエリにある `dimensionDataSource` を指定してカスタム分析コード使用できます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="9cfab-306">システムが、カスタム分析コードをベース分析コードに自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="9cfab-307">`filters` で `DimensionDataSource` を指定し、`filters` および `groupByValues` の両方でカスタム分析コードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9cfab-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="9cfab-308">システムが、カスタム分析コードをベース分析コードに自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="9cfab-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="9cfab-309">現在の手持在庫に対するクエリ例 2</span><span class="sxs-lookup"><span data-stu-id="9cfab-309">Current on-hand query example 2</span></span>

<span data-ttu-id="9cfab-310">この例では、Power Apps で分析コードの構成に必要なマッピングが設定されていないシナリオを示します。この場合、転記する場合もベース分析コードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="9cfab-311">`filters` にある `dimensionDataSource` フィールドが null 値、空白、または空白の場合は、すべての分析コードがベース分析コードである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="9cfab-312">例: 返された結果</span><span class="sxs-lookup"><span data-stu-id="9cfab-312">Example return result</span></span>

<span data-ttu-id="9cfab-313">前の例のクエリを実行すると、次のような結果が返される場合があります。</span><span class="sxs-lookup"><span data-stu-id="9cfab-313">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="9cfab-314">"数量" フィールドは、測定とそれに関連付けられた値のディクショナリとして構成されています。</span><span class="sxs-lookup"><span data-stu-id="9cfab-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
