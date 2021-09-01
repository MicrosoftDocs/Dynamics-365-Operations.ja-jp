---
title: フランスのキャッシュ レジスターの配置ガイドライン (レガシー)
description: このトピックは、フランスのローカライズ用配置ガイドです。
author: EvgenyPopovMBS
manager: annbe
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: France
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-4-13
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 105202207fd3b151f5819566f559f1f8bfc9ef4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343742"
---
# <a name="deployment-guidelines-for-cash-registers-for-france-legacy"></a>フランスのキャッシュ レジスターの配置ガイドライン (レガシー)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> このサンプル会計統合機能は、[会計統合フレームワーク](./fiscal-integration-for-retail-channel.md)を利用しておらず、今後の更新で非推奨になります。 代わりに、[会計統合フレームワークに基づく機能](./emea-fra-fi-deployment.md)を使用する必要があります。

このトピックは、Dynamics 365 Commerce のフランスでのローカライズを有効にする方法を示す配置ガイドです。 ローカライズは、コンポーネントのいくつかの拡張機能で構成されます。 たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。 フランスのローカライズの詳細については、 [フランスのキャッシュ レジスター機能](./emea-fra-cash-registers.md) を参照してください。

このローカライズは、小売ソフトウェア開発キット (SDK) の一部です。 SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

このローカライズは、Commerce runtime (CRT)、Retail Servers、および POS の拡張機能で構成されます。 このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。

> [!NOTE]
> Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。 このトピックは、アプリの以前の複数のバージョンに適用されるため、このトピック全体で *Retail サーバー* を使用します。

## <a name="storing-a-certificate-for-digital-signing-in-azure-key-vault"></a>Azure Key Vault にデジタル署名用証明書を保存します。

デジタル署名拡張機能は、Retail Serverが配置されているマシンのローカルの証明書のストレージにインストールされている証明書を使用します。 コンフィギュレーション ファイルの証明書の拇印を指定する必要があります (このトピックで後述する [SequentialSignatureRegisterコンポーネント](#sequentialsignatureregister-component) を参照してください)。 実装のトポロジーに応じて、証明書は [Microsoft Azure Key Vault ストレージ](/azure/key-vault/key-vault-get-started) に保存される必要があります。 フランス用ローカライズには、Azure Key Vault ストレージに保存されている証明書を使用して、署名フローを上書きし、販売取引に署名する方法を示すサンプル コードが含まれています。

### <a name="prerequisites"></a>必要条件

Azure Key Vault ストレージに格納されている証明書を使用する前に、次の手順を完了する必要があります。

- Azure Key Vault ストレージを作成する必要があります。 Retail Server と同じ地理的領域にストレージを配置することをお勧めします。
- 証明書は、そのストレージにアップロードされる必要があります。
- ストレージから機密情報を読み取るには、Retail Server アプリケーションが承認される必要があります。

Azure Key Vault を操作する方法の詳細については、次を参照してください。[Azure Key Vault の使用を開始します](/azure/key-vault/key-vault-get-started)。

### <a name="using-the-sample"></a>サンプルを使用してください。

**DigitalSignatureKeyVaultSample** プロジェクトは、Azure Key Vault ストレージに格納されている証明書を使用するためのサンプル コードを含んでいます。 サンプルを実稼働環境で使用するには、ロジックを実装し、**CertificateSignatureServiceRequestHandler** クラスにある **HashAndSignData** メソッドで、次のパラメータを指定できるようにする必要があります。

- **Azure Key Vault URL** - Azure Key Vault ストレージの URL。

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultUrl, "Set your Azure Key Vault URL here");
    ```

- **クライアント ID** - 認証のために Azure Key Vault ストレージに関連付けられている Azure Active Directory (Azure AD) アプリケーションのインタラクティブ クライアント ID。 このクライアントは、 Azure Key Vault ストレージから機密情報を読み取るためのアクセス許可が必要です。

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultInteractiveClientId, "Set the client ID here");
    ```

- **クライアント シークレット** - Azure Key Vault ストレージで認証のために使用される Azure AD アプリケーションと関連している秘密キー。

    ``` csharp
    // Secret key value should be encrypted and stored in a safe place.
    settings.Add(WellKnownKeyVaultSettings.KeyVaultClientSecretKey, "Set the secret key here");
    ```

- **秘密参照**- 証明書への秘密の参照。

    ``` csharp
    SecretCertificate secretCertificate = settingsHelper.SecretProvider.GetSecret("vault:///{Specify the secret reference}") as SecretCertificate;
    ```

署名のフローを上書きする場合は以下の手順を実行します。

1. **DigitalSignatureKeyVaultSample** プロジェクトを構築し、**Contoso.Commerce.Runtime.DigitalSignatureKeyVaultSample.dll** アセンブリを **bin\\ext** Retail Server フォルダーにコピーします。
2. **コンポジション** セクションに次の行を追加して、**commerceRuntime.ext.config** ファイルを更新します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
    ```

> [!NOTE]
> デジタル署名に使用される証明書の拇印は、証明書が Azure Key Vault ストレージに保存されている場合でも、SequentialSignatureRegister アセンブリのコンフィギュレーション ファイルで指定されている必要があります。 詳細については、このトピックの後半の [SequentialSignatureRegister コンポーネント](#sequentialsignatureregister-component) セクションを参照してください。

### <a name="using-certificate-profiles-in-commerce-channels"></a>Commerce チャネルでの証明書プロファイルの使用

Commerce バージョン 10.0.15では、Key Vaultまたは本社が使用できない場合に、オフラインにするためのフェールオーバーをサポートする[小売店舗のユーザー定義の証明書プロファイル](./certificate-profiles-for-retail-stores.md) を使用できます。 この機能は、[小売チャンネルのシークレットを管理 ](../dev-itpro/manage-secrets.md) を拡張ます。

CRT の新しい機能を適用するには、次の手順を実行します。

1. 新しい CRT 拡張機能プロジェクトを作成します (C# クラス ライブラリ プロジェクト タイプ)。 Retail ソフトウェア開発キット (SDK) からサンプル テンプレートを使用します (RetailSDK\SampleExtensions\CommerceRuntime)。
2. CertificateSignatureServiceRequest のカスタム ハンドラーを SequentialSignatureRegister プロジェクトに追加します。
3. シークレット呼び出しを読み取るには、プロファイスされたパラメータのあるコンストラクターを使用し、GetUserDefinedSecretCertificateServiceRequest を実行します。 これにより、証明書プロファイルの設定で機能が開始されます。 この設定に基づいて、証明書は Azure Key Vault またはローカルマシン ストレージから取得されます。

    ``` csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);
    
    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. 証明書が取得されたら、データ署名に進みます。
5. CRT 拡張機能プロジェクトを作成します。
6. 出力クラス ライブラリをコピーし、手動テスト用の ...\RetailServer\webroot\bin\Ext に貼り付けます。
7. CommerceRuntime.Ext.config ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。

## <a name="specifying-application-attributes-that-will-be-printed-on-receipts"></a>レシートに印刷されるアプリケーション属性を指定します。

カスタム フィールドを使用することで、次のようなアプリケーション属性をレシートに印刷できます。<!-- (for more information, see [Cash registers for France](./emea-fra-cash-registers.md))-->:

- **ビルド番号**- POS アプリケーションのソフトウェアのバージョン。 既定では、この値は、Microsoft が POS アプリケーションに割り当てた POS ビルド番号と等しくなります。
- **証明書のカテゴリ** および **証明書の番号** - アプリケーションの認定証明を発行するカテゴリとコンプライアンスの証明書の数。 既定では、値はカテゴリとMicrosoft に与えられた証明書の数に等しい。

    - Microsoft Dynamics 365 for Commerce:

        - **証明書のカテゴリ:** C
        - **証明書番号:** 18/0202

    - Microsoft Dynamics 365 for Commerce:

        - **証明書のカテゴリ:** B
        - **証明書番号:** 18/0203

    > [!NOTE]
    > 既定では、証明書のカテゴリおよび割り当てられている番号が印刷されます。 コマースを実装している場合は、証明書のカテゴリと番号を上書きする必要があります。

POS アプリケーションをカスタマイズしていて、そのカスタマイズがアプリケーションのコンプライアンスに影響を与える場合は、認定機関にコンプライアンスの新しい証明書を要求する必要があります。 この場合、ビルド番号、および証明書のカテゴリ、および番号を上書きする必要があります。 それ以外の場合、証明書のカテゴリおよび番号の既定値が印刷されますが、Microsoft が POS アプリケーションに割り当てた POS ビルド番号も指定する必要があります。

### <a name="overriding-the-build-number"></a>ビルド番号の変更

ソフトウェアのバージョン/ビルド番号と発行元は、**RetailSDK\\BuildTools\\Customization.settings** で指定されます。

```xml
<CustomVersion Condition="'$(CustomVersion)' == ''">1.0.0.1</CustomVersion>
<CustomName Condition="'$(CustomName)' == ''">Contoso Retail Customization</CustomName> 
<CustomDescription Condition="'$(CustomDescription)' == ''">Contoso Retail Customization</CustomDescription>
<CustomPublisher Condition="'$(CustomPublisher)' == ''">CN=Contoso Ltd.</CustomPublisher>
<CustomPublisherDisplayName Condition="'$(CustomPublisherDisplayName)' == ''">Contoso Ltd.</CustomPublisherDisplayName>
<CustomCopyright Condition="'$(CustomCopyright)' == ''">Copyright © 2016</CustomCopyright>
```

### <a name="overriding-the-certificate-category-and-number"></a>証明書のカテゴリや番号の変更

証明書のカテゴリと番号は、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsFrance\\GetSalesTransactionCustomReceiptFieldService** で指定されます。

``` csharp
/// <summary>
/// Certification category.
/// </summary>
private const string CertificationCategory = "C";

/// <summary>
/// Certificate number.
/// </summary>
private const string CertificateNumber = "18/0202";
```

> [!NOTE]
> コマースを実装している場合は、証明書のカテゴリと番号も上書きする必要があります。 この場合、このトピックで先に見たセクション、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) にある証明書のカテゴリおよびに記載されている証明書のカテゴリと番号を使用します。

## <a name="development-environment"></a>開発環境

次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。

### <a name="crt-extension-components"></a>CRT 拡張コンポーネント

CRT サンプルには、CRT 拡張コンポーネントが含まれます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。

#### <a name="commonfrance-component"></a>CommonFrance コンポーネント

1. **Runtime.Extensions.CommonFrance** プロジェクトを見つけ、構築します。
2. **Extensions.CommonFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.CommonFrance.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
    ```

#### <a name="receiptsfrance-component"></a>ReceiptsFrance コンポーネント

1. **Runtime.Extensions.ReceiptsFrance** プロジェクトを探して、構築します。
2. **Extensions.ReceiptsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsFrance.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
    ```

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

#### <a name="salespaymenttransextfrance-component"></a>SalesPaymentTransExtFrance コンポーネント

1. **Runtime.Extensions.SalesPaymentTransExtFrance** プロジェクトを探して、構築します。
2. **Extensions.SalesPaymentTransExtFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
    ```

#### <a name="sequentialsignaturefrance-component"></a>SequentialSignatureFrance コンポーネント

1. **Runtime.Extensions.SequentialSignatureFrance** プロジェクトを探して、構築します。
2. **Extensions.SequentialSignatureFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureFrance.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
    ```

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。
2. 拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。 **CertificateThumbprint** プロパティは、唯一の必須のプロパティです。 この値は必ず文字列で、40 字の長さがあり、大文字で、区切り記号を含みません。 詳細については、[証明書の拇印を取得する方法](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate) を参照してください。

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <configuration>
        <configSections>
            <section name="SequentialSignatureRegister" type="Contoso.Commerce.Runtime.SequentialSignatureRegister.Configuration.SequentialSignatureRegisterConfigSection, Contoso.Commerce.Runtime.SequentialSignatureRegister"/>
        </configSections>
        <SequentialSignatureRegister certificateThumbprint="insert key certificateThumbprint here" certificateStoreLocation="LocalMachine" certificateStoreName="My"/>
        <startup>
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5.1"/>
        </startup>
    </configuration>
    ```

3. プロジェクトを構築します。
4. **Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル

5. ファイルを CRT 拡張フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

6. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

7. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts コンポーネント

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを探して、構築します。
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

#### <a name="xzreportsfrance-component"></a>XZReportsFrance コンポーネント

1. **Runtime.Extensions.XZReportsFrance** プロジェクトを探して、構築します。
2. **Extensions.XZReportsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsFrance.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
    ```

#### <a name="restrictingshiftduration-component"></a>RestrictingShiftDuration コンポーネント

# <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

1. **Runtime.Extensions.RestrictingShiftDuration** プロジェクトを探して、構築します。
2. **Extensions.RestrictingShiftDuration\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RestrictingShiftDuration.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RestrictingShiftDuration" />
    ```

# <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    ```

# <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    ```

---

### <a name="retail-server-extension-components"></a>Retail Server 拡張機能コンポーネント

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignature Retail Server サンプル コンポーネント

1. **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。
2. **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。
3. IIS Retail Server サイトの場所の **\\bin\\ext** フォルダーにアセンブリ ファイルをコピーします。
4. Retail Server のコンフィギュレーション ファイルを検索します。 ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。
5. コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

### <a name="proxy-extension-component"></a>プロキシ拡張機能コンポーネント

Modern POS に対してオフライン モードで拡張機能を有効にする次の手順を実行する必要があります。

#### <a name="salestransactionsignature-retail-proxy-sample-component"></a>SalesTransactionSignature Retail プロキシ サンプル コンポーネント

1. **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。
2. **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。
3. アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。
4. 拡張機能コンフィギュレーション ファイルで、プロキシの変更を登録します。 ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

### <a name="modern-pos-extension-components"></a>Modern POS 拡張コンポーネント

1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

2. **Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - RestrictingShiftDuration
    - SalesTransBuildNumberSample

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    ---

    > [!NOTE]
    > プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで **すべてのファイルを表示する** ボタンを選択します。 このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。 現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。 プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加** を選択します。

3. **tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - RestrictingShiftDuration
    - SalesTransBuildNumberSample

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    ---

4. **extensions.json** で、次の明細行を追加することによって拡張機能が読み込まれるようにします。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "RestrictingShiftDuration"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    ---

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

5. ソリューションをリビルドします。
6. デバッガーでModern POS を実行し、機能をテストします。

### <a name="cloud-pos-extension-components"></a>クラウド POS 拡張コンポーネント

1. **RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
2. **Pos.Extensions** プロジェクトで、既存のソース コードのフォルダーを含めます。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - RestrictingShiftDuration
    - SalesTransBuildNumberSample

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    ---

    > [!NOTE]
    > プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで **すべてのファイルを表示する** ボタンを選択します。 このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。 現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。 プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加** を選択します。

3. **tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - RestrictingShiftDuration
    - SalesTransBuildNumberSample

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SequentialSignature
    - AuditEventSignatureSample
    - SalesTransBuildNumberSample

    ---

4. **extensions.json** で、次の明細行を追加することによって拡張機能が読み込まれるようにします。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "RestrictingShiftDuration"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    ---

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

5. ソリューションをリビルドします。
6. **実行** コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。
7. 機能をテストします。

### <a name="set-up-required-parameters-in-headquarters"></a>バックオフィスで要求されるパラメーターを設定します

詳細については、 [フランスのキャッシュ レジスター機能](./emea-fra-cash-registers.md) を参照してください。

## <a name="production-environment"></a>実稼働環境

以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。

1. [クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。
2. **RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。

    1. **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの **構成** セクションに、次の行を追加します。

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RestrictingShiftDuration" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
        <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
        <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
        ```

        ---

        デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。

        > [!NOTE]
        > この明細行を追加する前に、このトピックの前の方にある[Azure Key Vault にデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) の手順を実行してください。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
        ```

    2. **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに以下の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

3. **Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。

    1. **ItemGroup** セクションに次の行を追加し、配置可能なパッケージにコマース プロキシ拡張機能を含めます。

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

    2. **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.CommonFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RestrictingShiftDuration.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsFrance.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 およびそれ以降](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.CommonFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsFrance.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 およびそれ以降](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.CommonFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsFrance.dll" />
        ```

        ---

        デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。

        > [!NOTE]
        > この明細行を追加する前に、このトピックの前の方にある、[Azure Key Vaultにデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) セクションにある手順を実行してください。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DataSignatureKeyVaultSample.dll" />
        ```

    3. **ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

4. Retail Server コンフィギュレーション ファイルを更新します。 **RetailSDK\\Packages\\RetailServer\\Code\\ web.config** で、**extensionComposition** セクションに次の行を追加します。

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

5. 拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。 その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。 ファイル名は、**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。
6. ビルド番号、カテゴリ、および必要に応じて、コンプライアンスの証明書の番号を上書きします。 詳細については、このトピックの前の方にある、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) セクションにある指示を参照してください。
7. Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
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
