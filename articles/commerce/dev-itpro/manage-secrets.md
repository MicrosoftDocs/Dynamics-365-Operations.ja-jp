---
title: 小売チャンネルのシークレットを管理
description: このトピックでは、チャネル データベースを拡張する方法について説明します。
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
ms.openlocfilehash: 133d415a8cc1ac1230c8bbe362b858e42ea2ea82
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004565"
---
# <a name="manage-secrets-for-retail-channels"></a>小売チャンネルのシークレットを管理

[!include [banner](../includes/banner.md)]

このトピックでは、シークレットへのアクセスを必要とするチャンネルで拡張機能を使用している際のシークレット管理方法について説明します。

## <a name="key-vault-setup"></a>Key Vault の設定

1. 拡張機能の開発者は、次の開発手順に従います。

    1. Microsoft Azure Key Vault でテスト シークレットを作成します。
    2. 本社のクライアントを、Key Vault に接続するよう、コンフィギュレーションします。
    3. **Key Vault パラメーター** ページ (**本社 \> Key Vault パラメーター**) で、Key Vault シークレットの拡張子キー名を指定します。 次の手順で、同じ名前を使用する必要があります。
    4. **GetUserDefinedSecretStringValueServiceRequest** Commerce Runtime (CRT) アプリケーション プログラミング インターフェイス (API) を使用して、シークレットを取得します。 シークレットを識別するための一意のシークレット名を渡します。
    5. 拡張機能の選定に関するドキュメントの一部として、拡張機能で参照されている秘密名を指定します。 この方法は他の拡張機能との競合を防ぐのに使用されるため、拡張機能の開発者は、シークレット名用に名前空間を使用することをお勧めします。

2. IT プロフェッショナルまたは実装パートナーは、これらの配置およびコンフィギュレーションの手順に従います。

    1. 拡張機能を顧客環境に適用します。 詳細については、[クラウド環境への更新プログラムの適用](../../dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。
    2. 目的のシークレットを Key Vault にアップロードします (または入力します)。 詳細については、[Azure Key Vault とは何ですか](https://docs.microsoft.com/azure/key-vault/key-vault-overview) を参照してください。
    3. **Key Vault パラメーター**ページで (**本社 \> Key Vault パラメーター**)、本社クライアントを Key Vault に接続するようコンフィギュレーションします。
    4. **Key Vault パラメーター**ページで、本社クライアントの Key Vault シークレットの拡張機能シークレット名を指定します。

## <a name="consume-the-secret-in-the-crt-extension"></a>CRT 拡張機能のシークレットの使用

拡張機能のシークレットを使用するには、次の要求と応答を追加します。

| 要求 / 応答                               | パラメーター                   | 説明 |
|------------------------------------------------|------------------------------|-------------|
| GetUserDefinedSecretStringValueServiceRequest  | 文字列 **secretName**        | 要求クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。 |
| GetUserDefinedSecretStringValueServiceResponse | 文字列 **SecretStringValue** | 応答クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。 この応答は、**SecretStringValue** 値を返すため、拡張機能はこの値を **X509Certificate2** に入力キャストするか、または文字列値として使用することが可能です。 |

CRT 拡張機能のシークレットを読み取るには、次の手順を実行します。

1. 新しい CRT 拡張機能プロジェクトを作成します (C\# クラス ライブラリ プロジェクト タイプ)。 Retail ソフトウェア開発キット (SDK) からサンプル テンプレートを使用します (**RetailSDK\\SampleExtensions\\CommerceRuntime**)。
2. CRT 拡張機能では、新しい要求 / 応答を作成することも、既存 CRT の要求に対してプレトリガーまたはポストトリガーを追加して呼び出すこともできます。 次の例では、トリガーは **SaveCartRequest** に追加されました。 **GetUserDefinedSecretStringValueServiceRequest** を呼び出し、バックオフィスにコンフィギュレーションされたシークレット キーを渡してシークレットを読み取ります。 バックオフィスからシークレットを読み取るために、カスタム コードを書き込む必要はありません。 要求および応答を使用して、値を読み取ることができます。

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

3. CRT 拡張機能プロジェクトを作成します。
4. 出力クラス ライブラリをコピーし、手動テスト用の **…\\RetailServer\\webroot\\bin\\Ext** に貼り付けます。
5. **CommerceRuntime.Ext.config** ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。 次に例を示します。

    ```Xml
    <add source="assembly" value="your custom library name" />
    ```

## <a name="credential-rotation"></a>資格情報のローテーション

この方法を資格情報管理に使用する際、資格情報のローテーションがより効率的になります。 シークレットを更新するには、IT 管理者が Key Vault のシークレットを更新するだけで済みます。 拡張機能を変更する必要はありません。 シークレットを更新した後は、キャッシュの期限が切れると、新しい値が使用され始めます。

## <a name="offline-support"></a>オフライン サポート

資格情報をオフラインでサポートするには、Key Vault の資格情報が使用できないまたはアクセスできない場合に、拡張機能コードでオフラインへのフェールオーバーが必要です。
