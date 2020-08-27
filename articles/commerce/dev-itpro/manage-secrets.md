---
title: 小売チャンネルのシークレットを管理
description: このトピックでは、シークレットへのアクセスを必要とするチャンネルで拡張機能を使用している際のシークレット管理方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 08/06/2020
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
ms.openlocfilehash: 7fa972dfd730aad297550973ee5d5caf4598f641
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666348"
---
# <a name="manage-secrets-for-retail-channels"></a><span data-ttu-id="b5a21-103">小売チャンネルのシークレットを管理</span><span class="sxs-lookup"><span data-stu-id="b5a21-103">Manage secrets for retail channels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5a21-104">このトピックでは、シークレットへのアクセスを必要とするチャンネルで拡張機能を使用している際のシークレット管理方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-104">This topic explains how to manage secrets when you're using an extension with channels that require access to secrets.</span></span> <span data-ttu-id="b5a21-105">拡張機能では、カスタム証明書を Commerce Scale Unit に配置したり、拇印やシークレットを web.config ファイルに追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="b5a21-105">Extensions will not be able to deploy any custom certificates in Commerce scale unit or add thumbprints or secrets in web.config files.</span></span> <span data-ttu-id="b5a21-106">シークレットを管理するための推奨される方法は、このトピックで説明したように、Azure Key Vault を使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="b5a21-106">The recommended approach for managing secrets is to use the Azure Key Vault, as noted in this topic.</span></span>

## <a name="key-vault-setup"></a><span data-ttu-id="b5a21-107">Key Vault の設定</span><span class="sxs-lookup"><span data-stu-id="b5a21-107">Key Vault setup</span></span>

1. <span data-ttu-id="b5a21-108">拡張機能の開発者は、次の開発手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b5a21-108">The extension developer follows these development steps:</span></span>

    1. <span data-ttu-id="b5a21-109">Microsoft Azure Key Vault でテスト シークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-109">Create a test secret in Microsoft Azure Key Vault.</span></span>
    2. <span data-ttu-id="b5a21-110">本社のクライアントを、Key Vault に接続するよう、コンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b5a21-110">Configure the head-office client to connect to Key Vault.</span></span>
    3. <span data-ttu-id="b5a21-111">**Key Vault パラメーター** ページ (**本社 \> Key Vault パラメーター**) で、Key Vault シークレットの拡張子キー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-111">On the **Key Vault Parameters** page (**Head Office \> Key Vault Parameters**), specify an extension key name for the Key Vault secret.</span></span> <span data-ttu-id="b5a21-112">次の手順で、同じ名前を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a21-112">The same name must be used in the next step.</span></span>
    4. <span data-ttu-id="b5a21-113">**GetUserDefinedSecretStringValueServiceRequest** Commerce Runtime (CRT) アプリケーション プログラミング インターフェイス (API) を使用して、シークレットを取得します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-113">Use the **GetUserDefinedSecretStringValueServiceRequest** Commerce Runtime (CRT) application programming interface (API) to get the secret.</span></span> <span data-ttu-id="b5a21-114">シークレットを識別するための一意のシークレット名を渡します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-114">Pass a unique secret name to identify the secret.</span></span>
    5. <span data-ttu-id="b5a21-115">拡張機能の選定に関するドキュメントの一部として、拡張機能で参照されている秘密名を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-115">As part of the documentation of the extension setup, state the secret name that is referenced in the extension.</span></span> <span data-ttu-id="b5a21-116">この方法は他の拡張機能との競合を防ぐのに使用されるため、拡張機能の開発者は、シークレット名用に名前空間を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5a21-116">We recommend that the extension developer use a namespace for the secret name, because this approach helps prevent conflicts with other extensions.</span></span>

2. <span data-ttu-id="b5a21-117">IT プロフェッショナルまたは実装パートナーは、これらの配置およびコンフィギュレーションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b5a21-117">The IT pro or implementation partner follows these deployment and configuration steps:</span></span>

    1. <span data-ttu-id="b5a21-118">拡張機能を顧客環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-118">Apply the extension to the customer environment.</span></span> <span data-ttu-id="b5a21-119">詳細については、[クラウド環境への更新プログラムの適用](../../dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5a21-119">For details, see [Apply updates to cloud environments](../../dev-itpro/deployment/apply-deployable-package-system.md).</span></span>
    2. <span data-ttu-id="b5a21-120">目的のシークレットを Key Vault にアップロードします (または入力します)。</span><span class="sxs-lookup"><span data-stu-id="b5a21-120">Upload the desired secrets to Key Vault (or enter them).</span></span> <span data-ttu-id="b5a21-121">詳細については、[Azure Key Vault とは何ですか](https://docs.microsoft.com/azure/key-vault/key-vault-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5a21-121">For details, see [What is Azure Key Vault?](https://docs.microsoft.com/azure/key-vault/key-vault-overview)</span></span>
    3. <span data-ttu-id="b5a21-122">**Key Vault パラメーター**ページで (**本社 \> Key Vault パラメーター**)、本社クライアントを Key Vault に接続するようコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b5a21-122">On the **Key Vault Parameters** page (**Head Office \> Key Vault Parameters**), configure the head-office client to connect to Key Vault.</span></span>
    4. <span data-ttu-id="b5a21-123">**Key Vault パラメーター**ページで、本社クライアントの Key Vault シークレットの拡張機能シークレット名を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-123">On the **Key Vault Parameters** page, specify the extension secret name for the Key Vault secret in the head-office client.</span></span>

## <a name="consume-the-secret-in-the-crt-extension"></a><span data-ttu-id="b5a21-124">CRT 拡張機能のシークレットの使用</span><span class="sxs-lookup"><span data-stu-id="b5a21-124">Consume the secret in the CRT extension</span></span>

<span data-ttu-id="b5a21-125">拡張機能のシークレットを使用するには、次の要求と応答を追加します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-125">To consume the secret in the extension, add the following request and response.</span></span>

| <span data-ttu-id="b5a21-126">要求 / 応答</span><span class="sxs-lookup"><span data-stu-id="b5a21-126">Request/response</span></span>                               | <span data-ttu-id="b5a21-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b5a21-127">Parameters</span></span>                   | <span data-ttu-id="b5a21-128">説明</span><span class="sxs-lookup"><span data-stu-id="b5a21-128">Description</span></span> |
|------------------------------------------------|------------------------------|-------------|
| <span data-ttu-id="b5a21-129">GetUserDefinedSecretStringValueServiceRequest</span><span class="sxs-lookup"><span data-stu-id="b5a21-129">GetUserDefinedSecretStringValueServiceRequest</span></span>  | <span data-ttu-id="b5a21-130">文字列 **secretName**</span><span class="sxs-lookup"><span data-stu-id="b5a21-130">string **secretName**</span></span>        | <span data-ttu-id="b5a21-131">要求クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5a21-131">The request class that is used to get user-defined secrets from Headquarters.</span></span> |
| <span data-ttu-id="b5a21-132">GetUserDefinedSecretStringValueServiceResponse</span><span class="sxs-lookup"><span data-stu-id="b5a21-132">GetUserDefinedSecretStringValueServiceResponse</span></span> | <span data-ttu-id="b5a21-133">文字列 **SecretStringValue**</span><span class="sxs-lookup"><span data-stu-id="b5a21-133">string **SecretStringValue**</span></span> | <span data-ttu-id="b5a21-134">応答クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5a21-134">The response class that is used to get user-defined secrets from Headquarters.</span></span> <span data-ttu-id="b5a21-135">この応答は、**SecretStringValue** 値を返すため、拡張機能はこの値を **X509Certificate2** に入力キャストするか、または文字列値として使用することが可能です。</span><span class="sxs-lookup"><span data-stu-id="b5a21-135">The response returns a **SecretStringValue** value, and extensions can type-cast this value to **X509Certificate2** or use it as string value.</span></span> |

<span data-ttu-id="b5a21-136">CRT 拡張機能のシークレットを読み取るには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-136">To read the secret in the CRT extension, follow these steps.</span></span>

1. <span data-ttu-id="b5a21-137">新しい CRT 拡張機能プロジェクトを作成します (C\# クラス ライブラリ プロジェクト タイプ)。</span><span class="sxs-lookup"><span data-stu-id="b5a21-137">Create a new CRT extension project (C\# class library project type).</span></span> <span data-ttu-id="b5a21-138">Retail ソフトウェア開発キット (SDK) からサンプル テンプレートを使用します (**RetailSDK\\SampleExtensions\\CommerceRuntime**)。</span><span class="sxs-lookup"><span data-stu-id="b5a21-138">Use the sample templates from the Retail software development kit (SDK) (**RetailSDK\\SampleExtensions\\CommerceRuntime**).</span></span>
2. <span data-ttu-id="b5a21-139">CRT 拡張機能では、新しい要求 / 応答を作成することも、既存 CRT の要求に対してプレトリガーまたはポストトリガーを追加して呼び出すこともできます。</span><span class="sxs-lookup"><span data-stu-id="b5a21-139">In the CRT extension, you can create a new request/response, or you can add a pre-trigger or post-trigger for the existing CRT request, and then call it.</span></span> <span data-ttu-id="b5a21-140">次の例では、トリガーは **SaveCartRequest** に追加されました。</span><span class="sxs-lookup"><span data-stu-id="b5a21-140">In the following example, a trigger was added for **SaveCartRequest**.</span></span> <span data-ttu-id="b5a21-141">**GetUserDefinedSecretStringValueServiceRequest** を呼び出し、バックオフィスにコンフィギュレーションされたシークレット キーを渡してシークレットを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="b5a21-141">It calls **GetUserDefinedSecretStringValueServiceRequest** to read the secret by passing the secret key that is configured in Headquarters.</span></span> <span data-ttu-id="b5a21-142">バックオフィスからシークレットを読み取るために、カスタム コードを書き込む必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b5a21-142">You don't have to write custom code to read the secret from Headquarters.</span></span> <span data-ttu-id="b5a21-143">要求および応答を使用して、値を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="b5a21-143">You can use the request and response to read the value.</span></span>

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
               
                string result = null;
                   
                GetUserDefinedSecretStringValueServiceRequest keyVaultRequest = new GetUserDefinedSecretStringValueServiceRequest("SecretName");
                GetUserDefinedSecretStringValueServiceResponse keyVaultResponse = request.RequestContext.Execute<GetUserDefinedSecretStringValueServiceResponse>(keyVaultRequest);
                result = keyVaultResponse.SecretStringValue;

                 GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: null, secretName: "SecretName", thumbprint: null, expirationInterval: null);
                 GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

                X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
               
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

3. <span data-ttu-id="b5a21-144">CRT 拡張機能プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-144">Build the CRT extension project.</span></span>
4. <span data-ttu-id="b5a21-145">出力クラス ライブラリをコピーし、手動テスト用の **…\\RetailServer\\webroot\\bin\\Ext** に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b5a21-145">Copy the output class library, and paste it into **…\\RetailServer\\webroot\\bin\\Ext** for manual testing.</span></span>
5. <span data-ttu-id="b5a21-146">**CommerceRuntime.Ext.config** ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-146">In the **CommerceRuntime.Ext.config** file, update the extension composition section with the custom library information.</span></span> <span data-ttu-id="b5a21-147">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5a21-147">Here is an example.</span></span>

    ```Xml
    <add source="assembly" value="your custom library name" />
    ```

## <a name="credential-rotation"></a><span data-ttu-id="b5a21-148">資格情報のローテーション</span><span class="sxs-lookup"><span data-stu-id="b5a21-148">Credential rotation</span></span>

<span data-ttu-id="b5a21-149">この方法を資格情報管理に使用する際、資格情報のローテーションがより効率的になります。</span><span class="sxs-lookup"><span data-stu-id="b5a21-149">When this approach is used for credential management, credential rotation is more streamlined.</span></span> <span data-ttu-id="b5a21-150">シークレットを更新するには、IT 管理者が Key Vault のシークレットを更新するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="b5a21-150">To update a secret, an IT admin just has to update the secret in Key Vault.</span></span> <span data-ttu-id="b5a21-151">拡張機能を変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b5a21-151">No change is required to the extension.</span></span> <span data-ttu-id="b5a21-152">シークレットを更新した後は、キャッシュの期限が切れると、新しい値が使用され始めます。</span><span class="sxs-lookup"><span data-stu-id="b5a21-152">After a secret is updated, the new value starts to be used when the cache expires.</span></span>

## <a name="offline-support"></a><span data-ttu-id="b5a21-153">オフライン サポート</span><span class="sxs-lookup"><span data-stu-id="b5a21-153">Offline support</span></span>

<span data-ttu-id="b5a21-154">資格情報をオフラインでサポートするには、Key Vault の資格情報が使用できないまたはアクセスできない場合に、拡張機能コードでオフラインへのフェールオーバーが必要です。</span><span class="sxs-lookup"><span data-stu-id="b5a21-154">Offline support for credentials requires that the extension code handle failover to offline when Key Vault credentials aren't available or accessible.</span></span>
