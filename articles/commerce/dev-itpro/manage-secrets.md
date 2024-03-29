---
title: 小売チャネルのシークレットの管理
description: この記事では、シークレットへのアクセスを必要とするチャネルで拡張機能を使用している際のシークレット管理方法について説明します。
author: ShalabhjainMSFT
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.custom: 83892
ms.openlocfilehash: 20c0c211859ffedd9676c0f65139135a5ba5268e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278518"
---
# <a name="manage-secrets-for-retail-channels"></a>小売チャネルのシークレットの管理

[!include [banner](../includes/banner.md)]

この記事では、シークレットへのアクセスを必要とするチャネルで拡張機能を使用している際のシークレット管理方法について説明します。 拡張機能では、カスタム証明書を Commerce Scale Unit に配置したり、拇印やシークレットを web.config ファイルに追加することはできません。 シークレットを管理するために推奨される方法は、この記事で説明したように、Azure Key Vault を使用する方法です。

## <a name="key-vault-setup"></a>Key Vault の設定

1. 拡張機能の開発者は、次の開発手順に従います。

    1. Microsoft Azure Key Vault でテスト シークレットを作成します。
    2. 本社のクライアントを、Key Vault に接続するよう、コンフィギュレーションします。
    3. **Key Vault パラメーター** ページ (**本社 \> Key Vault パラメーター**) で、Key Vault シークレットの拡張子キー名を指定します。 次の手順で、同じ名前を使用する必要があります。
    4. **GetUserDefinedSecretStringValueServiceRequest** Commerce Runtime (CRT) アプリケーション プログラミング インターフェイス (API) を使用して、シークレットを取得します。 シークレットを識別するための一意のシークレット名を渡します。
    5. 拡張機能の選定に関するドキュメントの一部として、拡張機能で参照されている秘密名を指定します。 この方法は他の拡張機能との競合を防ぐのに使用されるため、拡張機能の開発者は、シークレット名用に名前空間を使用することをお勧めします。

2. IT プロフェッショナルまたは実装パートナーは、これらの配置およびコンフィギュレーションの手順に従います。

    1. 拡張機能を顧客環境に適用します。 詳細については、[クラウド環境への更新プログラムの適用](../../fin-ops-core/dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。
    2. 目的のシークレットを Key Vault にアップロードします (または入力します)。 詳細については、[Azure Key Vault とは何ですか](/azure/key-vault/key-vault-overview) を参照してください。
    3. **Key Vault パラメーター** ページで (**本社 \> Key Vault パラメーター**)、本社クライアントを Key Vault に接続するようコンフィギュレーションします。
    4. **Key Vault パラメーター** ページで、本社クライアントの Key Vault シークレットの拡張機能シークレット名を指定します。

## <a name="consume-the-secret-in-the-crt-extension"></a>CRT 拡張機能のシークレットの使用

拡張機能のシークレットを使用するには、次の要求と応答を追加します。

| 要求 / 応答                               | パラメーター                   | 説明 |
|------------------------------------------------|------------------------------|-------------|
| GetUserDefinedSecretStringValueServiceRequest  | 文字列 **secretName**        | 要求クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。 |
| GetUserDefinedSecretStringValueServiceResponse | 文字列 **SecretStringValue** | 応答クラスは、バックオフィスからユーザー定義のシークレットを取得するために使用されます。 この応答は、**SecretStringValue** 値を返すため、拡張機能はこの値を **X509Certificate2** に入力キャストするか、または文字列値として使用することが可能です。 |

CRT 拡張機能のシークレットを読み取るには、次の手順を実行します。

### <a name="cache-the-key-vault-in-memory-in-crtretail-server"></a>CRT/Retail Server のメモリに Key Vault をキャッシュする

CRT のKey Vault シークレット値を読み取るために呼び出しが行われるたびに、CRT はリアルタイムで本社に呼び出して値を取得します。 その後本社は Key Vault を呼び出して値を取得します。 値の読み取りには複数のホップが関係するため、呼び出しの待ち時間が長くなります。 したがって、パフォーマンスを向上させるために、CRT/Retail Server 側のメモリに Key Vault の値をキャッシュすることをお勧めします。 Key Vault で値が頻繁に変更される場合は、シナリオに基づいて、キャッシュの有効期限の正しい戦略を決定する必要があります。

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

3. CRT 拡張機能プロジェクトを作成します。
4. 出力クラス ライブラリをコピーし、手動テスト用の **…\\RetailServer\\webroot\\bin\\Ext** に貼り付けます。
5. **CommerceRuntime.Ext.config** ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。 次に例を示します。

    ```Xml
    <add source="assembly" value="your custom library name" />
    ```

## <a name="credential-rotation"></a>資格情報のローテーション

この方法を資格情報管理に使用する際、資格情報のローテーションがより効率的になります。 シークレットを更新するには、IT 管理者が Key Vault でシークレットを更新するだけです。 拡張機能を変更する必要はありません。 

## <a name="offline-support"></a>オフライン サポート

資格情報をオフラインでサポートするには、Key Vault の資格情報が使用できないまたはアクセスできない場合に、拡張機能コードでオフラインへのフェールオーバーが必要です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
