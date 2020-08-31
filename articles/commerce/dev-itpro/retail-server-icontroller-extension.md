---
title: 新しい Retail Server API の作成
description: このトピックでは、Retail SDK バージョン 10.0.11 以降を使用して新しい Retail Server API を作成する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 07/22/2020
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
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 11d04399e9e2eb46c985fd8b8d1020b31931bb2b
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665363"
---
# <a name="create-a-new-retail-server-extension-api-retail-sdk-version-10011-and-later"></a>新しい Retail Server 拡張 API の作成 (Retail SDK バージョン 10.0.11 以降)

[!include [banner](../includes/banner.md)]

このドキュメントでは、新しい Retail Server アプリケーション プログラミング インターフェイス (API) の作成方法、および POS または他のクライアントがそれを使用できるようにするための公開方法について説明します。 既存の Retail Server API の変更はサポートされていません。

このトピックは、Retail SDK バージョン 10.0.11 以降に適用されます。

Retail ソフトウェア開発キット (SDK) には、Commerce Runtime (CRT) を含む、エンドツーエンドの Retail Server 拡張機能のサンプルがいくつか用意されているのみです。 これらのサンプルをテンプレートとして使用して、拡張機能を起動できます。 サンプル拡張機能は、**RetailSDK\\SampleExtensions\\RetailServer** フォルダーで見つけることができます。

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

## <a name="create-the-new-retail-server-api"></a>新しい Retail Server API の作成

1. CRT 拡張機能を作成します。 Retail Server 拡張機能を作成する前に、CRT 拡張機能を作成します。 Retail Server API には、パラメーターで CRT を呼び出すロジック以外のロジックはありません。
2. Microsoft .NET Framework バージョン 4.6.1 を使用する新しい C# クラス ライブラリ プロジェクトを作成するか、または Retail SDK 内の Retail Server のサンプルのいずれかをテンプレートとして使用します。
3. Retail Server 拡張機能プロジェクトで、CRT 拡張機能ライブラリまたはプロジェクトへの参照を追加します。 この参照を使用して、CRT 要求、応答およびエンティティを呼び出すことができます。
4. Retail Server 拡張機能プロジェクトで、NuGet パッケージ マネージャーを使用して、**Microsoft.Dynamics.Commerce.Hosting.Contracts** を追加します。 NuGet パッケージは、**RetailSDK\\pkgs** フォルダにあります。
5. 新しいコントローラー クラスを作成し、**IController** からクラスを拡張します。 このコントローラー クラスには、Retail Server API によって公開される必要のあるメソッドが含まれています。 コントローラー クラス内で、CRT 要求を呼び出すメソッドを追加します。 新しいコントローラー クラスを、**CustomerController** や **ProductController** などの既存のコントローラー クラスから拡張しないでください。 拡張クラスでは、**IController** クラスのみを拡張する必要があります。
6. コントローラー クラスを公開するには、コントローラー クラスに **RoutePrefix** 属性を追加します。

    ```csharp
    [RoutePrefix("SimpleExtension")]  
    ```

7. **BindEntity** 属性は、新しいコントローラーを作成してエンティティを公開する場合に、コントローラー クラスで必要です。

    次のサンプル コードでは、エンティティ、文字列、およびブール値を返す単純な Retail Server API を作成します。 サンプルで使用されている CRT 要求および応答は、このサンプルには含まれていません。 CRT 要求および応答の例については、[Commerce Runtime (CRT) の拡張機能およびトリガー](commerce-runtime-extensibility-trigger.md)を参照してください。

    ```csharp
    /// <summary>
        /// New extended controller.
        /// </summary>
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

    Retail Server API では、さまざまな承認ロールがサポートされています。 コントローラー メソッドへのアクセスは、コントローラー メソッドの**承認**属性で指定された承認ロールに基づいて許可されます。 次のコード例には、サポートされている承認ロールが示されています。

    ```csharp
    // Summary:
    // Represents the type of logon type.
    [DataContract]
    public static class CommerceRoles
    {
        //
        // Summary:
        //     Anonymous Role.
        [DataMember]
        public const string Anonymous = "Anonymous";
        //
        // Summary:
        //     SharePoint Role used by Connector.
        [DataMember]
        public const string Storefront = "Storefront";
        //
        // Summary:
        //     Employee Role.
        [DataMember]
        public const string Employee = "Employee";
        //
        // Summary:
        //     Customer Role.
        [DataMember]
        public const string Customer = "Customer";
        //
        // Summary:
        //     Represents the Device level of authentication.
        [DataMember]
        public const string Device = "Device";
        //
        // Summary:
        //     Represents Application level of authentication.
        [DataMember]
        public const string Application = "Application";
        //
        // Summary:
        //     The list of all possible Microsoft.Dynamics.Commerce.Runtime.DataModel.CommerceRoles
        //     values.
        public static readonly string[] All;
    }
    ```

8. 拡張機能プロジェクトをビルドし、バイナリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーにコピーします。
9. **extensionComposition** セクションで新しい拡張ライブラリ名を追加して、**\\RetailServer\\webroot** フォルダーの Commerce Scale Unit **web.config** ファイルを更新します。

    ```xml
    <extensionComposition>
    <!-- Use fully qualified assembly names for ALL if you need to support loading from the Global Assembly Cache.
    If you host in an application with a bin folder, this is not required. -->
    <add source="assembly" value="SimpleExtensionSample" >
    </extensionComposition>
    ```

10. Microsoft インターネット インフォメーション サービス (IIS) で、Commerce Scale Unit を再起動して、新しい拡張機能を読み込みます。
11. 拡張機能が正常に読み込まれたことを確認するには、Retail Server のメタデータを参照します。 エンティティおよびメソッドが一覧に表示されることを確認します。 メタデータを参照するには、Web ブラウザーの次の形式で URL を開きます。

    **https://RS-URL/Commerce/$metadata**

12. クライアントで Retail Server 拡張機能を呼び出すには、クライアント Typescript プロキシを生成する必要があります。 その後、プロキシを使用して、クライアントから新しい Retail Server API を呼び出すことができます。

    Retail Server 拡張 API を使用して、**EdmModelExtender** ファイルを拡張機能に追加する必要はありません。 これらのファイルは、Retail SDK バージョン 10.0.10 またはそれ以前を使用している場合にのみ必要です。

    この新しい **Microsoft.Dynamics.Commerce.Hosting.Contracts** API を使用してビルトされた Retail Server 拡張機能は、オフライン実装でも使用できます。 個別の C# プロキシライブラリを生成する必要はありません。 **\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーのRetail サーバー拡張ライブラリをコピーして、**RetailProxy.MPOSOffline.ext** config ファイルを更新してこの新しいライブラリーに追加します。 拡張機能では、Typescript プロキシのみを生成する必要があります。 SDK サンプルは、**\\RetailSDK\\SampleExtensions\\TypeScriptProxy)** フォルダーにあります。

    次の例は、**RetailProxy.MPOSOffline.ext** 構成ファイル内の **add** 要素を更新する方法を示しています。

    ```xml
    <?xml version="1.0" encoding="utf-8"?> 
    <retai1ProxyExtensions> 
        <composition> 
            <add source="assembly" value="Contoso.RetailServer.StoreHoursSamp1e" /> 
        </composition> 
    </retai1ProxyExtensions> 
    ```

## <a name="generate-the-typescript-proxy-for-pos"></a>POS Typescript プロキシの生成

1. Visual Studio 2017 の **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** からサンプル プロキシ テンプレート プロジェクトを開きます。 必要に応じて名前を変更します。
2. このプロキシ テンプレート プロジェクトに、Retail Server 拡張プロジェクトをプロジェクト参照プロジェクトとして追加します。 既存の **StoreHoursSample** プロジェクト参照を削除します。
3. **Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** を右クリックし、**Edit Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** を選択します。
4. **\<RetailServerExtensionAssemblies\>** ノードの下に、Retail Server 拡張機能のアセンブリ名を指定します。 次の例は、アセンブリ名を追加する方法を示しています。

    ```xml
      <ItemGroup>
        <RetailServerExtensionAssemblies Include="..\..\RetailServer\Extensions.Sample\bin\$(Configuration)\net461\$(AssemblyNamePrefix).RetailServer.Extension.Sample.dll" />
      </ItemGroup>
    ```

5.  **コピー** ノードの下で、**DestinationFolder** パスを拡張フォルダーに更新して、生成されたプロキシファイルが POS 拡張フォルダーに自動的にコピーされるようにします。 生成されたプロキシ ファイルも **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** にコピーされます。 次の例は、パスを更新する方法を示しています。

    ```xml
    <Copy SourceFiles="@(GeneratedDataServiceContracts)" DestinationFolder="$(SdkRootPath)\POS\Extensions\Sample\DataService" SkipUnchangedFiles="true" />
    ```

6. 変更が完了したら、プロキシ プロジェクトをビルドして typescript プロキシ ファイルを生成します。 ビルドが完了すると、**\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** フォルダーでプロキシ ファイルが使用可能となり、そのフォルダーは**コピー** コマンドによって指定されます。 パスとフォルダー パスは、フォルダ構造によって異なる場合があります。
