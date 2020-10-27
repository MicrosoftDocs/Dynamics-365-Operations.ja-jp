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
# <a name="consume-retail-server-apis-in-external-applications"></a>外部アプリケーションでの Retail Server API の使用

[!include [banner](../includes/banner.md)]

このトピックでは、外部アプリケーションで Retail Server API を使用する方法について説明します。 Retail Server は、外部アプリケーションが API を使用できるように、Open Data Protocol (OData) Web エンドポイントを公開します。 また、Retail Server は Commerce Runtime (CRT) ビジネス ロジックをホストし、それを OData エンドポイントとして公開します。 これらのエンドポイントは、Retail Server API と呼ばれます。

外部アプリケーションでは、HTTPS を使用して OData サービスを使用できます。 Retail Server には、API を利用するための複数のオプションがあります。

- **Retail Server プロキシ** – 厳密に型指定された API を使用する方法。 さまざまなアプリケーションのタイプに対して公開される複数のタイプのプロキシがあります。

    - **C\# プロキシ** – サーバー側とネイティブの両方のアプリケーションが、C\# バイナリ (クラス ライブラリ) を使用して API やその他のエンティティにアクセスできます。
    - **TypeScript プロキシ** – クライアント アプリケーションは、.ts プロキシ ファイルを使用して API およびその他のエンティティにアクセスできます。

- **OData クライアント** – OData クライアントや Postman から API を使用することができます。または Retail Server URL に対する HTTPS 要求を生成することにより、API を使用することもできます。

メタデータを参照するには、Web ブラウザーの次のフォーマットで Retail Server の URL を開きます。 すると、すべての Retail Server API、および入出力パラメータの一覧が表示されます。

```rest
https://RS-URL/Commerce/$metadata
```

## <a name="security-and-authentication-that-are-required-to-consume-apis"></a>API の使用に必要なセキュリティと認証

各 API へのアクセスは、ネイティブで次のロールに従って制限されます。

- **従業員** – このロールに関連付けられている API にアクセスするには、販売時点管理 (POS) デバイスの有効化 (デバイス トークン) が必要で、認証済み従業員がアクセスできます。
- **顧客** – このロールに関連付けられている API へのアクセスには、認証済み顧客が必要です。 通常、E コマース サイトでは、これらの API を使用して、注文履歴の取得や顧客の詳細の変更などの操作を実行します。
- **アプリケーション** – このロールに関連付けられている API にアクセスするには、Azure Active Directory (Azure AD) のサービス間認証など、アプリケーション レベルの認証が必要です。
- **匿名** – このロールに関連付けられている API は、主にユーザー認証を行わない E コマース サイトによって使用されます。
- **カスタマイズされた API** – このロールに関連付けられている API へのアクセスを制限するには、POS デバイスの有効化、顧客認証、匿名認証などの方法を使用します。

外部アプリケーションの統合では、API にアクセスするために**アプリケーション**認証フローのみを必要とします。 E コマース アプリケーションの統合には、**顧客**認証が必要です。

このトピックでは、**アプリケーション認証**フローの設定と、**アプリケーション**認証コンテキストを使用した API へのアクセスに重点を置いて説明します。

外部アプリケーションから API にアクセスする前に、外部アプリケーションを Azure アプリ登録に登録する必要があります。また、登録されたアプリケーションの詳細を Commerce Headquarters に追加する必要があります。

認証フローの詳細については、[Dynamics 365 Commerce 認証フロー](../arch-auth-flow.md) を参照してください。

## <a name="register-the-application-in-azure-app-registration"></a>Azure アプリ登録で、アプリケーションを登録する

アプリケーションの登録は、アプリと Microsoft ID プラットフォームとの間に信頼関係を確立します。 信頼は単一方向で、アプリケーションは Microsoft ID プラットフォームを信頼しますが、逆向きでは信頼されません。 アプリの登録を作成するには、次の手順に従います。

1. [Azure ポータル](https://portal.azure.com/)にサインインします。
2. 複数のテナントへのアクセス許可がある場合は、トップメニューの**ディレクトリ + 購読**フィルターを使用して、アプリケーションを登録するテナントを選択します。
3. **Azure Active Directory** を検索して選択します。
4. **管理**で、**アプリの登録**を選択し、**新規登録**を選択します。
5. アプリケーションの名前を入力します。 アプリのユーザーにはこの名前が表示されます。後で変更することもできます。
6. **この組織ディレクトリのアカウントのみ (Microsoft のみ、単一テナント)** としてこのアプリケーションを使用できるユーザーを指定します。
7. **URI のリダイレクト**フィールドは既定値のままにします。 何も変更しないでください。
8. **登録**を選択して、最初のアプリ登録を行います。

登録が完了すると、Azure ポータルに、アプリ登録の**概要**ウィンドウが表示されます。 このウィンドウには、**アプリケーション (クライアント) ID** フィールドが表示されます。 このフィールドの値は、*アプリケーション ID* または*クライアント ID* と呼ばれます。 Microsoft ID プラットフォームでアプリケーションを一意に識別します。

### <a name="add-a-client-secret"></a>クライアント シークレットの追加

クライアント シークレットは、*アプリケーション パスワード*と呼ばれることもあります。 これは、アプリが、自身の ID に対する証明書の代わりとして使用できる文字列値です。

1. Azure ポータルの**アプリの登録**で、アプリケーションを選択します。
2. **証明書とシークレット** &gt; **新しいクライアント シークレット**を選択します。
3. クライアント シークレットの説明を入力します。
4. 期間を選択します。
5. **追加**を選択します。
6. シークレットの値は、クライアント アプリケーション コードで使用できるように必ず書き留めてください。 **このページから移動すると、シークレットの値が再度表示されることはありません。**

## <a name="register-the-app-in-the-finance-and-operations-app-so-that-retail-server-trusts-it"></a>Retail Server から信頼されるようにするため、Finance and Operations アプリで、対象アプリを登録する

1. Commerce Headquarters で、**Retail と Commerce** &gt; **本社の設定** &gt; **パラメーター** &gt; **Commerce 共有パラメーター**の順に移動します。
2. **ID プロバイダー** クイック タブで、`HTTPS://sts.windows.net/` で始まるプロバイダーを選択します。 選択に基づいて、**依存する関係者**クイック タブの値が設定されます。
3. **依存する関係者**クイック タブで、**追加**を選択します。 Azure でアプリの登録時に生成されたクライアント ID を入力します。 **Type** フィールドを**機密情報**に、**UserType**フィールドを**アプリケーション**に設定します。
4. アクション ウィンドウで、**保存**を選択します。
5. 新しい依存する関係者を選択し、**サーバー リソース ID** クイック タブで **追加** を選択します。 **サーバー リソース ID** 列に、Retail Server の URL を入力します。
6. アクション ウィンドウで、**保存**を選択します。
7. **Retail と Commerce** &gt; **Retail および Commerce IT** &gt; **配送スケジュール**の順に移動し、Commerce Data Exchange (CDX) ジョブ **1110** を実行します。

## <a name="access-the-apis-by-using-postman"></a>Postman を使用した API へのアクセス

いくつかのサードパーティ製ツールを使用すると、Azure サービスでの認証、Web API 要求の作成と送信、および応答の表示を行うことができます。 Postman は、最も普及しているツールの 1 つです。 [Postman クライアント ツールのダウンロードとインストール](https://www.postman.com/)。

この例では、**GetOrderHistory** API にアクセスします。 この API は、特定の顧客の注文履歴を取得します。 **従業員**、**顧客**、または**アプリケーション**の認証コンテキストを使用してのみアクセスできます。 対象アプリケーションには**アプリケーション**認証コンテキストがあるため、**GetOrderHistory** API にアクセスして顧客注文履歴を取得できます。

API にアクセスするには、最初に認証トークンを生成します。 その後、その認証トークンを使用して API にアクセスします。

すべての API の一覧については、[Commerce Scale Unit 顧客およびコンシューマー API](retail-server-customer-consumer-api.md) を参照してください。

### <a name="generate-an-authorization-token-by-using-postman"></a>Postman を使用した認証トークンの生成

1. Postman で、以下の要求 URL と本文パラメータを持つ GET 要求を作成します。

    **要求 URL**

    ```rest
    https://login.microsoftonline.com/{tenant-id}/oauth2/token
    ```

    > [!NOTE]
    > テナント ID は、Azure アプリの登録の**概要**ウィンドウから取得できます。 クライアント ID の横に表示されます。

    **本文パラメータ**

    | キー            | 先頭値                                                              |
    |----------------|--------------------------------------------------------------------|
    | grant\_type    | **client\_credentials**                                            |
    | client\_id     | Azure アプリの登録時に生成されたクライアント ID     |
    | client\_secret | Azure アプリの登録時に生成されたクライアント シークレット |
    | リソース       | Retail Server の URL                                              |

2. 要求が実行を完了すると、応答本文に **access\_token** の値が生成されます。 このトークンの値をコピーします。 Retail Server に接続するためにこれを使用します。

### <a name="get-order-history-by-using-postman"></a>Postman を使用した注文履歴の取得

- Postman で、以下の要求 URL、パラメーター、およびヘッダー パラメーターを持つ POST 要求を作成します。

    **要求 URL**

    ```rest
    <https://Retail>serverurl/Commerce/Customers('2001')/GetOrderHistory
    ```

    > [!NOTE]
    > **2001** をご自身の顧客 ID に置換します。

    **パラメーター**

    | キー         | 先頭値 |
    |-------------|-------|
    | $top        | 10    |
    | API のバージョン | 7.3   |

    **ヘッダー パラメーター**

    | キー           | 先頭値                                            |
    |---------------|--------------------------------------------------|
    | OUN           | この小売チャネルの作業単位番号 |
    | 認証 | **id\_token { access\_token }**                  |

    > [!NOTE]
    > **Access_token** については、認証要求で生成された **access_token** の値をコピーして貼り付けます。 次に **id_token** を接頭語として付けます。

要求の実行が完了した後、応答の本文には顧客注文履歴が含まれます。

## <a name="access-the-retail-server-apis-by-using-a-console-application"></a>コンソール アプリケーションを使用した Retail Server API へのアクセス

1. Visual Studio 2017 を使用して、コンソール アプリケーションを作成します。
2. **App.config** ファイルには、次のコンフィギュレーションを含めます。

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

### <a name="update-the-configuration-settings-with-actual-values"></a>実際の値によるコンフィギュレーション設定の更新

1. プロジェクトの NuGet パッケージ マネージャを使用して、以下の NuGet パッケージを追加します。

    + Microsoft.IdentityModel.Clients.ActiveDirectory
    + Microsoft.Dynamics.Commerce.RetailProxy

    **Microsoft.Dynamics.Commerce.RetailProxy** NuGet パッケージは、**RetailSDK\\Pkgs** フォルダから追加することができます。 NuGet マネージャで、**RetailSDK\\pkgs** フォルダのローカル リポジトリを追加します。

2. **Program.cs** ファイルに、以下の変数を追加します。

    ```C#
    private static string clientId;
    private static string clientSecret;
    private static Uri retailServerUrl;
    private static string resource;
    private static string operatingUnitNumber;
    private static Uri authority;
    ```

3. **Program.cs** ファイルに、アプリ設定を読み取るための **GetConfiguration** メソッドを追加します。

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

4. **Program.cs** ファイルに、アクセス トークンを取得するための **CreateManagerFactory** メソッドを追加します。

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

5. **GetOrderHistory** メソッドを追加して、注文を読み取ります。

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

6. **Main** メソッドでは、**GetOrderHistory** メソッドを呼び出してレコードを読み取ります。

    ```C#
    static void Main(string[] args)
    {
        GetConfiguration();
        Microsoft.Dynamics.Commerce.RetailProxy.PagedResult<SalesOrder> orderHistory = Task.Run(async () => await GetOrderHistory("2001")).Result;
        Console.WriteLine(orderHistory.FirstOrDefault<SalesOrder>().Id);
    }
    ```
