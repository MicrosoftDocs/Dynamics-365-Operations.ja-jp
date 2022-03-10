---
title: ノルウェーのキャッシュ レジスタの展開ガイドライン (レガシ)
description: このトピックは、Microsoft Dynamics 365 Commerce のノルウェーでのローカライズを有効にする方法を示す配置ガイドです。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 019bac01abdc0b2e16718c08953b44fbccef83a3
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944791"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>ノルウェーのキャッシュ レジスタの展開ガイドライン (レガシ)

[!include [banner](../includes/banner.md)]

このトピックは、Microsoft Dynamics 365 Commerce のノルウェーでのローカライズを有効にする方法を示す配置ガイドです。 ローカライズは、コマース コンポーネントのいくつかの拡張機能で構成されます。 たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。 ノルウェーのローカライズの詳細については、 [ノルウェーのキャッシュ レジスター機能](./emea-nor-cash-registers.md) を参照してください。

このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。 SDK に関する詳細については、[Retail ソフトウエア開発キット (SDK) アーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

このサンプルは Commerce runtime (CRT)、Retail Server、そして POS の拡張機能で構成されます。 このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。

> [!NOTE]
> Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。 このトピックは、アプリの以前の複数のバージョンに適用されるため、このトピック全体で *Retail サーバー* を使用します。
>
> 使用しているコマースのバージョンによって、このトピックの手順の一部が異なります。 詳細については、 [Dynamics 365 Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。

### <a name="using-certificate-profiles-in-commerce-channels"></a>Commerce チャネルでの証明書プロファイルの使用

Commerce バージョン 10.0.15 では、Key Vault または本社が使用できない場合に、オフラインにするためのフェールオーバーをサポートする[小売店舗のユーザー定義の証明書プロファイル](./certificate-profiles-for-retail-stores.md) を使用できます。 この機能は、[小売チャンネルのシークレットを管理 ](../dev-itpro/manage-secrets.md) を拡張ます。

CRT でこの機能を適用するには、次の手順を実行します。

1. 新しい CRT 拡張機能プロジェクトを作成します (C# クラス ライブラリ プロジェクト タイプ)。 Retail ソフトウェア開発キット (SDK) からサンプル テンプレートを使用します (RetailSDK\SampleExtensions\CommerceRuntime)。

2. CertificateSignatureServiceRequest のカスタム ハンドラーを SequentialSignatureRegister プロジェクトに追加します。

3. シークレット呼び出しを読み取るには、profileId パラメーターのあるコンストラクターを使用し、`GetUserDefinedSecretCertificateServiceRequest` を実行します。 これにより、証明書プロファイルの設定で機能が開始されます。 この設定に基づいて、証明書は Azure Key Vault またはローカルマシン ストレージから取得されます。

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. 証明書が取得されたら、データ署名に進みます。

5. CRT 拡張機能プロジェクトを作成します。

6. 出力クラス ライブラリをコピーし、手動テスト用の ...\RetailServer\webroot\bin\Ext に貼り付けます。

7. CommerceRuntime.Ext.config ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順を実行します。

### <a name="the-crt-extension-components"></a>CRT 拡張コンポーネント

CRT サンプルには、CRT 拡張コンポーネントが含まれます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。

#### <a name="receiptsnorway-component"></a>ReceiptsNorway コンポーネント

1. **Runtime.Extensions.ReceiptsNorway** プロジェクトを探して、構築します。
2. **Extensions.ReceiptsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsNorway.dll** アセンブリファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt コンポーネント

1. **Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。
2. **Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="xzreportsnorway-component"></a>XZReportsNorway コンポーネント

1. **Runtime.Extensions.XZReportsNorway** プロジェクトを探して、構築します。
2. **Extensions.XZReportsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsNorway.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent サンプル コンポーネント

1. **Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature サンプル コンポーネント

1. **Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。
2. 拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。
3. プロジェクトを構築します。
4. **Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル

5. ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

6. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

7. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent サンプル コンポーネント

1. **Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature サンプル コンポーネント

1. **Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。
2. 拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。
3. プロジェクトを構築します。
4. **Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル

5. ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

6. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

7. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messages コンポーネント

1. **Runtime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトを検索します。
2. **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent サンプル コンポーネント

1. **Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature サンプル コンポーネント

1. **Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。
2. 拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。
3. プロジェクトを構築します。
4. **Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル

5. ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

6. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

7. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

# <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent サンプル コンポーネント

1. **Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。
2. 拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。
3. プロジェクトを構築します。
4. **Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル

5. ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

6. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

7. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway コンポーネント

1. **Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。
2. **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway コンポーネント

1. **Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。
2. **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEvent ノルウェイ コンポーネント

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。
2. 拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。
3. プロジェクトを構築します。
4. **Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル

5. ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

6. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

7. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway コンポーネント

1. **Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。
2. **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway コンポーネント

1. **Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。
2. **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEvent ノルウェイ コンポーネント

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。
2. 拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。
3. プロジェクトを構築します。
4. **Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル

5. ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

6. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

7. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway コンポーネント

1. **Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。
2. **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway コンポーネント

1. **Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。
2. **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

---

### <a name="the-retail-server-extension-components"></a>Retail Server 拡張コンポーネント

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignature Retail Server サンプル コンポーネント

1. **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。
2. **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを Retail Server 拡張機能フォルダーにコピーします。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。

    ---

4. Retail Server のコンフィギュレーション ファイルを検索します。 ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。
5. コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Retail Server 拡張機能の依存関係を登録します。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4/)

    1. **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。

        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル
        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル

    2. ファイルを、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーにコピーします。
    3. CRT 用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。 ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later/)

    1. **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。
    2. ファイルをIIS Retail Server サイトがある場所の **\\bin** フォルダーにコピーします。
    3. CRT 用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。 ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > 作業は不要です。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    > [!NOTE]
    > 作業は不要です。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    > [!NOTE]
    > 作業は不要です。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    > [!NOTE]
    > 作業は不要です。

    ---

### <a name="the-modern-pos-extension-components"></a>Modern POS 拡張コンポーネント

#### <a name="implement-the-proxy-code-for-offline-mode"></a>オフライン モード用プロキシ コードを実装します。

この箇所は Retail Server コントローラーと同じですが、クライアントが接続されていない場合に使用されるローカル CRT を拡張します。

1. **Customization.settings** ファイルで、**@(RetailServerLibraryPathForProxyGeneration)** セクションを変更し、プロキシ生成で新しい Retail Server アセンブリを使用するようにします。
2. **StoreOperationsManager** クラスで次のインターフェイス メソッドを実装します。 最初の繰り返しには、次のコードを追加します。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    ---

3. プロキシ コードを再生成するには、コマンドラインから **msbuild/t:Rebuild** コマンドを使用して **プロキシ** フォルダーを構築します。
4. **Proxies.RetailProxy** プロジェクトの依存関係を解決します。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** project to reference **SalesTransactionSignatureSample** に追加します。

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** プロジェクトと、**SalesTransactionSignatureSample.Messages** 参照に追加します。

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    ---

5. **StoreOperationsManager** クラスでインターフェイス メソッドを調節します。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    ---

6. **dllhost.exe.config** ファイルを更新し、クライアント ブローカーが新しい RetailProxy アセンブリを読み込みます。

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>小売プロキシ拡張コンポーネント (Retail 7.3.1 およびそれ以降)

Retail 7.3.1 もしくはそれ以降を使用しているときに限り、次の手順を実行します。

1. **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。
2. **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。
3. アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。
4. 拡張機能コンフィギュレーション ファイルで Retail プロキシの変更を登録します。 ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modern POS 拡張コンポーネント

1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

2. **Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. 除外リストから次のフォルダーを削除して、**tsconfig.json** で拡張機能がコンパイルされるようにします。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. 適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

5. ソリューションをリビルドします。
6. デバッガーでModern POS を実行し、機能をテストします。

### <a name="cloud-pos-extension-components"></a>クラウド POS 拡張コンポーネント

1. **RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
2. **Pos.Extensions** プロジェクトの、既存ソース コード フォルダーを含めます。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. 除外リストから次のフォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. 適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

5. ソリューションをリビルドします。
6. **実行** コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。
7. 機能をテストします。

### <a name="set-up-required-parameters-in-headquarters"></a>バックオフィスで要求されるパラメーターを設定します

詳細については、 [ノルウェイのキャッシュ レジスター機能](./emea-nor-cash-registers.md) を参照してください。

## <a name="production-environment"></a>実稼働環境

以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。

1. [クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。
2. **RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。

    1. **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの **構成** セクションに、次の行を追加します。

        # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. コマース プロキシ カスタマイズを有効にします。

        # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

        **dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

        **dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

        **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

        **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

        **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. **Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。

    1. 小売プロキシ カスタマイズを有効にします。

        # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

        **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

        **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

        **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

        **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

        **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。

        # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。

        # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. 以下のファイルを修正して、配置可能なパッケージ内に ノルウェーのリソース ファイルを含めます。
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - **Sdk.ModernPos.Shared.csproj** ファイルの場合 
    - **ItemGroup** セクションに新しい行を追加
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > <ファイル名> ではなく、リソース ファイルの名前を指定します。 次に示す例にも同じことが当てはまります。
 
    - **Target Name="CopyPackageFiles"** セクションに行を追加します。
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - **Sdk.RetailServerSetup.proj** ファイルの場合 
    - **ItemGroup** セクションに新しい行を追加
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - **Target Name="CopyPackageFiles"** セクションに行を追加します。
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. 拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。 その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。

    # <a name="application-update-4"></a>[アプリケーション 更新 4](#tab/app-update-4)

    ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。

    # <a name="application-update-5-and-later"></a>[アプリケーション更新プログラム 5 以降](#tab/app-update-5-and-later)

    ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。

    ---

6. Retail Server コンフィギュレーション ファイルを更新します。 **RetailSDK\\Packages\\RetailServer\\Code\\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。
8. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Modern POS のオフライン モードでのデジタル署名を有効にします。

Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。

1. POS にサインインします。
2. **データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。 **ダウンロードの保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。
3. POS からのサインアウト
4. オフライン データベースが完全に同期するため少しの間待ちます。
5. POS にサインインします。
6. **データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。 **オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。
7. Modern POS を再起動します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
