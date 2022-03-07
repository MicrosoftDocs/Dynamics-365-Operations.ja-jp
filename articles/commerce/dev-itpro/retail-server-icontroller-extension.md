---
title: Retail Server 拡張 API の作成 (Retail SDK バージョン 10.0.11 以降)
description: このトピックでは、Retail SDK バージョン 10.0.11 以降を使用して新しい Retail Server API を作成する方法について説明します。
author: mugunthanm
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 22fa9e482acfb0a843e7c80c2ad3e3b961308c4b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792975"
---
# <a name="create-a-retail-server-extension-api-retail-sdk-version-10011-and-later"></a>Retail Server 拡張 API の作成 (Retail SDK バージョン 10.0.11 以降)

[!include [banner](../includes/banner.md)]

このトピックでは、新しい Retail Server アプリケーション プログラミング インターフェイス (API) の作成方法、および 販売時点管理 (POS) または他のクライアントがそれを使用できるようにするための公開方法について説明します。 既存の Retail Server API の変更はサポートされていません。

このトピックは、Retail ソフトウェア開発キット (SDK) バージョン 10.0.11 以降に適用されます。

Retail SDK には、Commerce Runtime (CRT) を含む、エンドツーエンドの Retail Server 拡張機能のサンプルがいくつか用意されているのみです。 これらのサンプルをテンプレートとして使用して、拡張機能を起動できます。 サンプル拡張機能は、**RetailSDK\\SampleExtensions\\RetailServer** フォルダーで見つけることができます。

## <a name="end-to-end-sample-repository-in-the-retail-sdk"></a>Retail SDK のエンドツーエンド サンプル リポジトリ

| サンプル拡張機能<br>(RetailSDK\\SampleExtensions\\RetailServer) | CRT サンプル<br>(RetailSDK\\SampleExtensions\\CommerceRuntime) | POS サンプル<br>(RetailSDK\\POS\\Extensions) |
|---------------------------------------------|--------------------------------------------|----------------------------------------|
| Extensions.StoreHoursSample                 | Extensions.StoreHoursSample                | StoreHoursSample                       |
| Extensions.SalesTransactionSignatureSample  | Extensions.SalesTransactionSignatureSample | SalesTransactionSignatureSample        |
| Extensions.PrintPackingSlipSample           | Extensions.PrintPackingSlipSample          |                                        |
| Extensions.CrossLoyaltySample               | Extensions.CrossLoyaltySample              |                                        |

## <a name="extension-class-diagram"></a>拡張機能クラス ダイアグラム

次の図は、拡張機能のクラス ダイアグラムを示しています。

![Commerce Scale Unit の拡張機能クラス ダイアグラム](media/RSExtensionClass.png)

> [!NOTE]
> Retail サーバーでは、IController と CommerceController の両方の拡張機能の読み込みはサポートされていません。 両方のタイプの拡張機能を含めると、Retail サーバーの負荷は失敗します。 拡張機能は IController または CommerceController のいずれかである必要があります。 IController 拡張機能に移行する場合は、すべての Retail サーバー拡張機能を IController に移行します。

## <a name="create-a-new-retail-server-api"></a>新しい Retail Server API の作成

1. CRT 拡張機能を作成します。 Retail Server 拡張機能を作成する前に、CRT 拡張機能を作成します。 Retail Server API には、パラメーターで CRT を呼び出すロジック以外のロジックはありません。
2. Microsoft .NET フレームワーク バージョン netstandard 2.0 をターゲット フレームワークとして使用する、新しい C# クラス ライブラリ プロジェクトを作成します。 または、Retail SDK に含まれている Retail Server のサンプルのいずれかをテンプレートとして使用します。
3. Retail Server 拡張機能プロジェクトで、CRT 拡張機能ライブラリまたはプロジェクトへの参照を追加します。 この参照を使用して、CRT 要求、応答およびエンティティを呼び出すことができます。
4. Retail Server 拡張機能プロジェクトで、NuGet パッケージ マネージャーを使用して、**Microsoft.Dynamics.Commerce.Hosting.Contracts** パッケージを追加します。 NuGet パッケージは、**RetailSDK\\pkgs** フォルダにあります。
5. 新しい公開コントローラー クラスを作成し、**IController** からクラスを拡張します。 このコントローラー クラスには、Retail Server API が公開する必要のあるメソッドが含まれているので、コントローラー クラスは公開である必要があります。
6. コントローラー クラス内で、CRT 要求を呼び出すメソッドを追加します。 新しいコントローラー クラスを、**CustomerController**、**SalesOrdersController**、または **ProductController** などの既存のコントローラー クラスから拡張しないでください。 拡張クラスでは、**IController** クラスのみを拡張する必要があります。
7. コントローラー クラス (コントローラー クラス名) 上で **RoutePrefix** 属性を追加します。

    ```csharp
    [RoutePrefix("SimpleExtension")]
    ```

8. コントローラー クラスで **BindEntity** 属性を追加します。 この属性は、新しいコントローラーを作成してエンティティを公開する場合に必要です。

```csharp
[BindEntity(typeof(SimpleEntity))]
```

> [!NOTE]
> 拡張クラスがエンティティにバインドされている場合は、手順 7 と 8 が必要です。 これらの手順は、エンティティではなく、単純型を返す非制限コントローラ クラスには必要ありません。

次のサンプル コードでは、エンティティ、文字列、およびブール値を返す単純な Retail Server API を作成します。 サンプルで使用されている CRT 要求および応答は、このサンプルには含まれていません。 CRT 要求および応答の例については、[Commerce Runtime (CRT) の拡張機能およびトリガー](commerce-runtime-extensibility-trigger.md)を参照してください。

### <a name="sample-code-for-a-controller-class-bounded-to-a-custom-entity"></a>カスタム エンティティにバインドされるコントローラ クラスのサンプルコード

> [!NOTE]
> 拡張コードは、顧客や製品などの既存の OOB エンティティにバインドしてはいけません。

```csharp
// New extended controller.
[RoutePrefix("SimpleExtension")]  
[BindEntity(typeof(SimpleEntity))]
public class SimpleExtensionController : IController
{
    /// <summary>
    /// The action to get the string value.
    /// </summary>
    /// <param name="context">The context parameters.</param>
    /// <param name="stringValue">The string value parameters.</param>
    /// <returns>The string value.</returns>
    [HttpPost]
    [Authorization(CommerceRoles.Customer, CommerceRoles.Employee)]
    public async Task<string> GetStringValue(IEndpointContext context, string stringValue)
    {
        GetStringValueResponse resp = await context.ExecuteAsync<GetStringValueResponse>
                                    (new GetStringValueRequest(stringValue)).ConfigureAwait(false);
        return resp.StringValue;
    }

    /// <summary>
    /// The action to get the bool value.
    /// </summary>
    /// <param name="context">The context parameters.</param>
    /// <param name="boolValue">The string value parameters.</param>
    /// <returns>The bool value.</returns>
    [HttpPost]
    [Authorization(CommerceRoles.Customer, CommerceRoles.Employee)]
    public async Task<bool> GetBoolValue(IEndpointContext context, string boolValue)
    {
        GetBoolValueResponse resp = await context.ExecuteAsync<GetBoolValueResponse>
                                    (new GetBoolValueRequest(boolValue)).ConfigureAwait(false);
        return resp.BoolValue;
    }

    /// <summary>
    /// The action to get the simple entity.
    /// </summary>
    /// <param name="context">The context parameters.</param>
    /// <param name="name">The name parameters.</param>
    /// <returns>The simple entity.</returns>
    [HttpPost]
    [Authorization(CommerceRoles.Customer, CommerceRoles.Employee)]
    public async Task<SimpleEntity> GetSimpleEntity(IEndpointContext context, string name)
    {
        GetSimpleEntityResponse resp = await context.ExecuteAsync<GetSimpleEntityResponse>
                                        (new GetSimpleEntityRequest(name)).ConfigureAwait(false);
        return resp.SimpleEntityObj;
    }
}
```

### <a name="sample-code-for-a-controller-class-not-bounded-to-a-custom-entity"></a>カスタム エンティティにバインドされていないコントローラ クラスのサンプルコード

```csharp
namespace Contoso.UnboundController.Sample
{
    using System.Threading.Tasks;
    using Microsoft.Dynamics.Commerce.Runtime.DataModel;
    using Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts;

    /// <summary>
    /// An extension unbounded controller sample.
    /// </summary>
    public class UnboundController : IController
    {
        /// <summary>
        /// A simple GET endpoint to demonstrate GET endpoints on an unbound controller.
        /// </summary>
        /// <returns>A simple true value to indicate the endpoint was reached.</returns>
        [HttpGet]
        [Authorization(CommerceRoles.Anonymous, CommerceRoles.Application, CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee, CommerceRoles.Storefront)]
        public Task<bool> SampleGet()
        {
            return Task.FromResult(true);
        }

        /// <summary>
        /// A simple POST endpoint to demonstrate POST endpoints on an unbound controller.
        /// </summary>
        /// <returns>A simple true value to indicate the endpoint was reached.</returns>
        [HttpPost]
        [Authorization(CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee)]
        public Task<bool> SamplePost()
        {
            return Task.FromResult(true);
        }
    }
}

```

Retail Server API では、さまざまな承認ロールがサポートされています。 コントローラー メソッドへのアクセスは、コントローラー メソッドの **承認** 属性で指定された承認ロールに基づいて許可されます。 次の例は、サポートされている承認ロールを示しています。 拡張コードは、**承認** 属性の代わりに **CommerceAuthorization** 属性を使用することはできません。 **CommerceAuthorization** 属性は、10.0.11 より前の SDK バージョンでのみサポートされています。


```csharp
// Represents the type of logon type.
[DataContract]
public static class CommerceRoles
{
    // Anonymous Role.
    [DataMember]
    public const string Anonymous = "Anonymous";

    // SharePoint Role used by Connector.
    [DataMember]
    public const string Storefront = "Storefront";

    // Employee Role.
    [DataMember]
    public const string Employee = "Employee";

    // Customer Role.
    [DataMember]
    public const string Customer = "Customer";

    // Represents the Device level of authentication.
    [DataMember]
    public const string Device = "Device";

    // Represents Application level of authentication.
    [DataMember]
    public const string Application = "Application";

    // The list of all possible Microsoft.Dynamics.Commerce.Runtime.DataModel.CommerceRoles values.
    public static readonly string[] All;
}
 ```

### <a name="support-paging-in-retail-server-apis"></a>Retail Server API のページングのサポート

リリース 10.0.18 から、API にページングが必要な場合、API に **QueryResultSettings** を追加し、クライアントから値を渡すことができます。 **QueryResultSettings** には、**PagingInfo** およびレコードがフェッチまたはスキップするための他のパラメーターが含まれます。  

拡張機能は、**QueryResultSettings** を CRT 要求に渡すことができ、データベース クエリがあるときに CRT 要求で使用することができます。

Retail SDK では、完全なサンプル コードを使用することができます: RetailSDK\SampleExtensions\CommerceRuntime\Extensions.StoreHoursSample\StoreHoursDataService.cs RetailSDK\SampleExtensions\RetailServer\Extensions.StoreHoursSample\StoreHoursController.cs"

```csharp

    [HttpPost]
        [Authorization(CommerceRoles.Anonymous, CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee)]
        public async Task<PagedResult<SampleDataModel.StoreDayHours>> GetStoreDaysByStore(IEndpointContext context, string StoreNumber, QueryResultSettings queryResultSettings)
        {
            var request = new GetStoreHoursDataRequest(StoreNumber) { QueryResultSettings = queryResultSettings };
            var hoursResponse = await context.ExecuteAsync<GetStoreHoursDataResponse>(request).ConfigureAwait(false);
            return hoursResponse.DayHours;
        }

```

```csharp

private async Task<Response> GetStoreDayHoursAsync(GetStoreHoursDataRequest request)
            {
                ThrowIf.Null(request, "request");

                using (DatabaseContext databaseContext = new DatabaseContext(request.RequestContext))
                {
                    var query = new SqlPagedQuery(request.QueryResultSettings)
                    {
                        DatabaseSchema = "ext",
                        Select = new ColumnSet("DAY", "OPENTIME", "CLOSINGTIME", "RECID"),
                        From = "CONTOSORETAILSTOREHOURSVIEW",
                        Where = "STORENUMBER = @storeNumber",
                    };

                    query.Parameters["@storeNumber"] = request.StoreNumber;
                    return new GetStoreHoursDataResponse(await databaseContext.ReadEntityAsync<DataModel.StoreDayHours>(query).ConfigureAwait(false));
                }
            }
            
  ```

### <a name="register-the-extension"></a>拡張機能の登録

1. 拡張機能プロジェクトをビルドし、バイナリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーにコピーします。
2. **extensionComposition** セクションで新しい拡張ライブラリ名を追加して、**\\RetailServer\\webroot** フォルダーの Commerce Scale Unit **web.config** ファイルを更新します。

    ```xml
    <extensionComposition>
        <!-- Use fully qualified assembly names for ALL if you need to support loading from the Global Assembly Cache.
        If you host in an application with a bin folder, this is not required. -->
        <add source="assembly" value="SimpleExtensionSample" >
    </extensionComposition>
    ```

3. インターネット インフォメーション サービス (IIS) で Commerce Scale Unit を再起動して、新しい拡張機能を読み込みます。

### <a name="validate-the-extension"></a>拡張機能の検証

1. 拡張機能が正常に読み込まれたことを確認するには、Retail Server のメタデータを参照します。 エンティティおよびメソッドが一覧に表示されることを確認します。 メタデータを参照するには、Web ブラウザーの次の形式で URL を開きます。

    `https://RS-URL/Commerce/$metadata`

2. クライアントで Retail Server 拡張機能を呼び出すには、クライアント Typescript プロキシを生成する必要があります。 その後、プロキシを使用して、クライアントから新しい Retail Server API を呼び出すことができます。

Retail Server 拡張 API を使用して、**EdmModelExtender** ファイルを拡張機能に追加する必要はありません。 これらのファイルは、Retail SDK バージョン 10.0.10 またはそれ以前を使用している場合にのみ必要です。

### <a name="debugging-rs-extension"></a>RS 拡張機能のデバッグ

Visual Studio で RS 拡張機能プロジェクトをデバッグする方法。 **デバッグ > プロセスに添付する** に移動します。 w3wp.exe (Retail Server の IIS プロセス) を選択します。 複数の w3wp.exe プロセスがある場合は、プロセス ID に基づいて適切なプロセスを使用します。 Retail サーバー プロセス IDは、**IIS > ワーカー プロセス** を使用するか、コマンド プロンプトと tasklist コマンドを使用して見つけることができます。

## <a name="generate-the-typescript-proxy-for-pos"></a>POS Typescript プロキシの生成

POS は Typescript プロキシ を使って、Retail サーバー API や CRT エンティティにアクセスします。 プロキシ クラスは、サービスを実行するためのクラスまたは Wrapper として機能し、プロキシ拡張機能を使用せずに Retail Server API やエンティティ メタデータを検索することによって、Retail Server API にアクセスします。

### <a name="steps-to-generate-the-proxy-files"></a>プロキシ ファイルを生成する手順

1. Visual Studio 2017 では、サンプル プロキシ テンプレート プロジェクトを Visual Studio 2017 の **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** から開きます。 新しい名前が必要な場合は、プロジェクトの名前を変更します。
2. このプロキシ テンプレート プロジェクトに、Retail Server 拡張プロジェクトをプロジェクト参照プロジェクトとして追加します。 既存の **StoreHoursSample** プロジェクト参照を削除します。
3. **Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** プロジェクトを右クリックし、**Edit Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** を選択します。
4. **\<RetailServerExtensionAssemblies\>** ノードの下に、Retail Server 拡張機能のアセンブリ名を指定します。 次の例は、アセンブリ名を追加する方法を示しています。

    ```xml
    <ItemGroup>
        <RetailServerExtensionAssemblies Include="..\..\RetailServer\Extensions.Sample\bin\$(Configuration)\net461\$(AssemblyNamePrefix).RetailServer.Extension.Sample.dll" />
    </ItemGroup>
    ```

5. **\<Copy\>** ノードの下で、POS 拡張フォルダーの **DestinationFolder** パスを更新して、生成されたプロキシファイルが POS 拡張フォルダーに自動的にコピーされるようにします。 生成されたプロキシ ファイルも **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** にコピーされます。 次の例は、パスを更新する方法を示しています。

    ```xml
    <Copy SourceFiles="@(GeneratedDataServiceContracts)" DestinationFolder="$(SdkRootPath)\POS\Extensions\Sample\DataService" SkipUnchangedFiles="true" />
    ```

6. 変更が完了したら、プロキシ プロジェクトをビルドして TypeScript プロキシ ファイルを生成します。 ビルドが完了すると、**\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** フォルダーでプロキシ ファイルが使用可能となり、そのフォルダーは **コピー** コマンドによって指定されます。 パスとフォルダー パスは、フォルダ構造によって異なる場合があります。

## <a name="retail-server-extension-in-offline"></a>オフラインの Retail Server 拡張機能

**Microsoft.Dynamics.Commerce.Hosting.Contracts** API を使用してビルトされた Retail Server 拡張機能は、オフライン実装でも使用できます。 個別の C# プロキシ ライブラリを生成する必要はありません。 **\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにある Retail Server 拡張機能ライブラリをコピーして、 **RetailProxy.MPOSOffline.ext** 構成ファイルにこのライブラリを含めるように構成します。 この拡張機能では、Typescript プロキシのみを生成する必要があります。 SDK サンプルは、**\\RetailSDK\\SampleExtensions\\TypeScriptProxy)** フォルダーにあります。

次の例は、**RetailProxy.MPOSOffline.ext** 構成ファイル内の要素の **追加** を更新する方法を示しています。

```xml
<?xml version="1.0" encoding="utf-8"?> 
<retailProxyExtensions> 
    <composition> 
        <add source="assembly" value="Contoso.RetailServer.StoreHoursSample" /> 
    </composition> 
</retailProxyExtensions> 
```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
