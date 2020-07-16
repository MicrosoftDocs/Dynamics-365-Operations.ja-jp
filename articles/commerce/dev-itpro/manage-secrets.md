---
title: 小売チャンネルのシークレットを管理
description: このトピックでは、シークレットへのアクセスを必要とするチャンネルで拡張機能を使用している際のシークレット管理方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: fe82d98f2b7ba01d676728fb2375762f10f32f91
ms.sourcegitcommit: f7294160d18f15cb762c24f2459b4f0887c37541
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3505648"
---
# <a name="manage-secrets-for-retail-channels"></a><span data-ttu-id="07352-103">小売チャンネルのシークレットを管理</span><span class="sxs-lookup"><span data-stu-id="07352-103">Manage secrets for retail channels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07352-104">このトピックでは、シークレットへのアクセスを必要とするチャンネルで拡張機能を使用している際のシークレット管理方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="07352-104">This topic explains how to manage secrets when you're using an extension with channels that require access to secrets.</span></span>

## <a name="key-vault-setup"></a><span data-ttu-id="07352-105">Key Vault の設定</span><span class="sxs-lookup"><span data-stu-id="07352-105">Key Vault setup</span></span>

1. <span data-ttu-id="07352-106">拡張機能の開発者は、次の開発手順に従います。</span><span class="sxs-lookup"><span data-stu-id="07352-106">The extension developer follows these development steps:</span></span>

    1. <span data-ttu-id="07352-107">Microsoft Azure Key Vault でテスト シークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="07352-107">Create a test secret in Microsoft Azure Key Vault.</span></span>
    2. <span data-ttu-id="07352-108">本社のクライアントを、Key Vault に接続するよう、コンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="07352-108">Configure the head-office client to connect to Key Vault.</span></span>
    3. <span data-ttu-id="07352-109">**Key Vault パラメーター** ページ (**本社 \> Key Vault パラメーター**) で、Key Vault シークレットの拡張子キー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="07352-109">On the **Key Vault Parameters** page (**Head Office \> Key Vault Parameters**), specify an extension key name for the Key Vault secret.</span></span> <span data-ttu-id="07352-110">次の手順で、同じ名前を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07352-110">The same name must be used in the next step.</span></span>
    4. <span data-ttu-id="07352-111">**GetUserDefinedSecretStringValueServiceRequest** Commerce Runtime (CRT) アプリケーション プログラミング インターフェイス (API) を使用して、シークレットを取得します。</span><span class="sxs-lookup"><span data-stu-id="07352-111">Use the **GetUserDefinedSecretStringValueServiceRequest** Commerce Runtime (CRT) application programming interface (API) to get the secret.</span></span> <span data-ttu-id="07352-112">シークレットを識別するための一意のシークレット名を渡します。</span><span class="sxs-lookup"><span data-stu-id="07352-112">Pass a unique secret name to identify the secret.</span></span>
    5. <span data-ttu-id="07352-113">拡張機能の選定に関するドキュメントの一部として、拡張機能で参照されている秘密名を指定します。</span><span class="sxs-lookup"><span data-stu-id="07352-113">As part of the documentation of the extension setup, state the secret name that is referenced in the extension.</span></span> <span data-ttu-id="07352-114">この方法は他の拡張機能との競合を防ぐのに使用されるため、拡張機能の開発者は、シークレット名用に名前空間を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07352-114">We recommend that the extension developer use a namespace for the secret name, because this approach helps prevent conflicts with other extensions.</span></span>

2. <span data-ttu-id="07352-115">IT プロフェッショナルまたは実装パートナーは、これらの配置およびコンフィギュレーションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="07352-115">The IT pro or implementation partner follows these deployment and configuration steps:</span></span>

    1. <span data-ttu-id="07352-116">拡張機能を顧客環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="07352-116">Apply the extension to the customer environment.</span></span> <span data-ttu-id="07352-117">詳細については、[クラウド環境への更新プログラムの適用](../../dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07352-117">For details, see [Apply updates to cloud environments](../../dev-itpro/deployment/apply-deployable-package-system.md).</span></span>
    2. <span data-ttu-id="07352-118">目的のシークレットを Key Vault にアップロードします (または入力します)。</span><span class="sxs-lookup"><span data-stu-id="07352-118">Upload the desired secrets to Key Vault (or enter them).</span></span> <span data-ttu-id="07352-119">詳細については、[Azure Key Vault とは何ですか](https://docs.microsoft.com/azure/key-vault/key-vault-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07352-119">For details, see [What is Azure Key Vault?](https://docs.microsoft.com/azure/key-vault/key-vault-overview)</span></span>
    3. <span data-ttu-id="07352-120">**Key Vault パラメーター**ページで (**本社 \> Key Vault パラメーター**)、本社クライアントを Key Vault に接続するようコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="07352-120">On the **Key Vault Parameters** page (**Head Office \> Key Vault Parameters**), configure the head-office client to connect to Key Vault.</span></span>
    4. <span data-ttu-id="07352-121">**Key Vault パラメーター**ページで、本社クライアントの Key Vault シークレットの拡張機能シークレット名を指定します。</span><span class="sxs-lookup"><span data-stu-id="07352-121">On the **Key Vault Parameters** page, specify the extension secret name for the Key Vault secret in the head-office client.</span></span>

## <a name="consume-the-secret-in-the-crt-extension"></a><span data-ttu-id="07352-122">CRT 拡張機能のシークレットの使用</span><span class="sxs-lookup"><span data-stu-id="07352-122">Consume the secret in the CRT extension</span></span>

<span data-ttu-id="07352-123">拡張機能のシークレットを使用するには、次の要求と応答を追加します。</span><span class="sxs-lookup"><span data-stu-id="07352-123">To consume the secret in the extension, add the following request and response.</span></span>

| <span data-ttu-id="07352-124">要求 / 応答</span><span class="sxs-lookup"><span data-stu-id="07352-124">Request/response</span></span>                               | <span data-ttu-id="07352-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07352-125">Parameters</span></span>                   | <span data-ttu-id="07352-126">説明</span><span class="sxs-lookup"><span data-stu-id="07352-126">Description</span></span> |
|------------------------------------------------|------------------------------|-------------|
| <span data-ttu-id="07352-127">GetUserDefinedSecretStringValueServiceRequest</span><span class="sxs-lookup"><span data-stu-id="07352-127">GetUserDefinedSecretStringValueServiceRequest</span></span>  | <span data-ttu-id="07352-128">文字列 **secretName**</span><span class="sxs-lookup"><span data-stu-id="07352-128">string **secretName**</span></span>        | <span data-ttu-id="07352-129">要求クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="07352-129">The request class that is used to get user-defined secrets from Headquarters.</span></span> |
| <span data-ttu-id="07352-130">GetUserDefinedSecretStringValueServiceResponse</span><span class="sxs-lookup"><span data-stu-id="07352-130">GetUserDefinedSecretStringValueServiceResponse</span></span> | <span data-ttu-id="07352-131">文字列 **SecretStringValue**</span><span class="sxs-lookup"><span data-stu-id="07352-131">string **SecretStringValue**</span></span> | <span data-ttu-id="07352-132">応答クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="07352-132">The response class that is used to get user-defined secrets from Headquarters.</span></span> <span data-ttu-id="07352-133">この応答は、**SecretStringValue** 値を返すため、拡張機能はこの値を **X509Certificate2** に入力キャストするか、または文字列値として使用することが可能です。</span><span class="sxs-lookup"><span data-stu-id="07352-133">The response returns a **SecretStringValue** value, and extensions can type-cast this value to **X509Certificate2** or use it as string value.</span></span> |

<span data-ttu-id="07352-134">CRT 拡張機能のシークレットを読み取るには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="07352-134">To read the secret in the CRT extension, follow these steps.</span></span>

1. <span data-ttu-id="07352-135">新しい CRT 拡張機能プロジェクトを作成します (C\# クラス ライブラリ プロジェクト タイプ)。</span><span class="sxs-lookup"><span data-stu-id="07352-135">Create a new CRT extension project (C\# class library project type).</span></span> <span data-ttu-id="07352-136">Retail ソフトウェア開発キット (SDK) からサンプル テンプレートを使用します (**RetailSDK\\SampleExtensions\\CommerceRuntime**)。</span><span class="sxs-lookup"><span data-stu-id="07352-136">Use the sample templates from the Retail software development kit (SDK) (**RetailSDK\\SampleExtensions\\CommerceRuntime**).</span></span>
2. <span data-ttu-id="07352-137">CRT 拡張機能では、新しい要求 / 応答を作成することも、既存 CRT の要求に対してプレトリガーまたはポストトリガーを追加して呼び出すこともできます。</span><span class="sxs-lookup"><span data-stu-id="07352-137">In the CRT extension, you can create a new request/response, or you can add a pre-trigger or post-trigger for the existing CRT request, and then call it.</span></span> <span data-ttu-id="07352-138">次の例では、トリガーは **SaveCartRequest** に追加されました。</span><span class="sxs-lookup"><span data-stu-id="07352-138">In the following example, a trigger was added for **SaveCartRequest**.</span></span> <span data-ttu-id="07352-139">**GetUserDefinedSecretStringValueServiceRequest** を呼び出し、バックオフィスにコンフィギュレーションされたシークレット キーを渡してシークレットを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="07352-139">It calls **GetUserDefinedSecretStringValueServiceRequest** to read the secret by passing the secret key that is configured in Headquarters.</span></span> <span data-ttu-id="07352-140">バックオフィスからシークレットを読み取るために、カスタム コードを書き込む必要はありません。</span><span class="sxs-lookup"><span data-stu-id="07352-140">You don't have to write custom code to read the secret from Headquarters.</span></span> <span data-ttu-id="07352-141">要求および応答を使用して、値を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="07352-141">You can use the request and response to read the value.</span></span>

    ```csharp
    public class CustomSaveCartTrigger : IRequestTrigger
    {
        /// <summary>
        /// Gets the list of supported request types.
        /// </summary>
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new[]{ typeof(SaveCartRequest) };
            }
        }

        /// <summary>
        /// Pre trigger code.
        /// </summary>
        /// <param name="request">The request.</param>
        public void OnExecuting(Request request)
        {
            ThrowIf.Null(request, "request");
            Type requestedType = request.GetType();
            if (requestedType == typeof(SaveCartRequest))
            {
                // Sample code to get the secret in string format.
                var request = new GetUserDefinedSecretStringValueServiceRequest("SecretName");
                string response = request.RequestContext.Execute<GetUserDefinedSecretStringValueServiceResponse>(request).SecretStringValue;
                // Sample code to get the secret in X509Certificate2 format.
                var request = new GetUserDefinedSecretStringValueServiceRequest ();
                X509Certificate2 response = request.RequestContext.Execute<GetUserDefinedSecretStringValueServiceRequest>(request).Certificate;
                // custom code to additional processing with secrets.
            }
        }

        /// <summary>
        /// Post trigger code.
        /// </summary>
        /// <param name="request">The request.</param>
        /// <param name="response">The response.</param>

        public void OnExecuted(Request request, Response response)
        {
        }
    }
    ```

3. <span data-ttu-id="07352-142">CRT 拡張機能プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="07352-142">Build the CRT extension project.</span></span>
4. <span data-ttu-id="07352-143">出力クラス ライブラリをコピーし、手動テスト用の **…\\RetailServer\\webroot\\bin\\Ext** に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07352-143">Copy the output class library, and paste it into **…\\RetailServer\\webroot\\bin\\Ext** for manual testing.</span></span>
5. <span data-ttu-id="07352-144">**CommerceRuntime.Ext.config** ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="07352-144">In the **CommerceRuntime.Ext.config** file, update the extension composition section with the custom library information.</span></span> <span data-ttu-id="07352-145">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="07352-145">Here is an example.</span></span>

    ```Xml
    <add source="assembly" value="your custom library name" />
    ```

## <a name="credential-rotation"></a><span data-ttu-id="07352-146">資格情報のローテーション</span><span class="sxs-lookup"><span data-stu-id="07352-146">Credential rotation</span></span>

<span data-ttu-id="07352-147">この方法を資格情報管理に使用する際、資格情報のローテーションがより効率的になります。</span><span class="sxs-lookup"><span data-stu-id="07352-147">When this approach is used for credential management, credential rotation is more streamlined.</span></span> <span data-ttu-id="07352-148">シークレットを更新するには、IT 管理者が Key Vault のシークレットを更新するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="07352-148">To update a secret, an IT admin just has to update the secret in Key Vault.</span></span> <span data-ttu-id="07352-149">拡張機能を変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="07352-149">No change is required to the extension.</span></span> <span data-ttu-id="07352-150">シークレットを更新した後は、キャッシュの期限が切れると、新しい値が使用され始めます。</span><span class="sxs-lookup"><span data-stu-id="07352-150">After a secret is updated, the new value starts to be used when the cache expires.</span></span>

## <a name="offline-support"></a><span data-ttu-id="07352-151">オフライン サポート</span><span class="sxs-lookup"><span data-stu-id="07352-151">Offline support</span></span>

<span data-ttu-id="07352-152">資格情報をオフラインでサポートするには、Key Vault の資格情報が使用できないまたはアクセスできない場合に、拡張機能コードでオフラインへのフェールオーバーが必要です。</span><span class="sxs-lookup"><span data-stu-id="07352-152">Offline support for credentials requires that the extension code handle failover to offline when Key Vault credentials aren't available or accessible.</span></span>
