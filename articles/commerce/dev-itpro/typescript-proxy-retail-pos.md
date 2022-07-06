---
title: TypeScript および小売販売時点管理 (POS) の C# プロキシ
description: この記事では、コマース プロキシに関する情報と、その生成方法について説明します。
author: mugunthanm
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-20
ms.dyn365.ops.version: AX 7.0.0, Retail October 2017 update
ms.openlocfilehash: 41b0cefbe6528357f005d7a49d09c4f9483b1a71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889383"
---
# <a name="typescript-and-c-proxies-for-retail-point-of-sale-pos"></a>TypeScript および小売販売時点管理 (POS) の C# プロキシ

[!include [banner](../../includes/banner.md)]

新しい小売サーバー API を作成する場合は、Retail ソフトウェア開発キット (SDK) の一部として使用できるツールを使用して、Commerce プロキシを生成する必要があります。 たとえば、新しい Retail サーバー API を追加する場合は、Commerce プロキシを生成する必要があります。

## <a name="the-commerce-proxy-and-when-to-use-it"></a>Commerce プロキシとそれを使用する場合

すべてのクライアントは Retail Serve とやりとりするためにプロキシ API を使用します。 Commerce プロキシは、Retail Server と Commerce Runtime (CRT) 間のインターフェイスを抽象化します。 たとえば、CRT で要求/応答の操作として新しいエンティティとビジネス ロジックを作成し、そのエンティティおよびそれらの要求/応答の操作を公開するために、新しい Retail サーバー API を追加できます。 販売時点管理 (POS) におけるエンティティと要求/応答動作にアクセスして、あるクライアント ロジックを実行する必要が出てきました。 POS ですべてのエンティティと要求/応答メタデータを手動で作成し、適切なパラメーターを使用して Retail サーバー API にアクセスすることができます。 ただし、エンティティ、マネージャ、および 2 つの場所で要求/応答コードを複製する必要があり、および多くのコードの書き込みもする必要があるため、このアプローチには追加の間接費が多く含まれます。

Commerce プロキシは、Retail Server に追加されたすべてのユーザー定義エンティティと要求/応答操作のプロキシを自動的に作成することによって、この労力を軽減します。 プロキシ ツールは、必須のインターフェイスとすべての必須メタデータを生成し、実際の実装を抽象化します。 この方法では、拡張プロジェクトにファイルを含めることができ、生成されたメタデータとインターフェイスを使用して Retail サーバー API とエンティティにアクセスできます。

## <a name="proxy-types"></a>プロキシのタイプ

クロス プラットフォーム シナリオをサポートするプロキシのタイプには 2 つあります。

- **TypeScript プロキシ**- POS は、TypeScript プロキシを使用して Retail Server API および CRT エンティティにアクセスします。 POS が Retail Server を使用する場合は、TypeScript プロキシが必要です。 それ以外の場合、POS はオペレーションまたはワークフローのために Retail サーバーと通信することができません。
- **C# プロキシ** - POS はオフラインのときに C# プロキシを使用します。 (POS がオフラインの場合、Retail サーバーを使用せずに CRT と直接通信します)。POS は、Dynamics 電子商取引プラットフォームにもこのプロキシを使用します。 カスタマイゼーションを POS がオフラインのときに動作させ、電子商取引クライアントを Retail Server API にアクセスするようにするには、C＃ プロキシを生成する必要があります。

TypeScript プロキシを生成する手順と C# プロキシを生成する手順は異なります。 この記事の後半では、各タイプのプロキシを生成する方法について説明します。

## <a name="generate-the-typescript-proxy-10011-or-lower-retail-server"></a>TypeScript プロキシ (10.0.11 以前) Retail Server の生成

Microsoft Dynamics Commerce バージョン 10.0.12 以降を使用している場合は、[新しい Ratail サーバー拡張機能 API を作成する](retail-server-icontroller-extension.md) で説明している手順に従ってください。

> [!IMPORTANT]
> Retail SDK ルート フォルダーから MSBuild を実行して、CommerceProxyGenerator.exe パッケージを復元します。 Visual Studio の開発者コマンド プロンプト、または MSBuild コマンド プロンプトを使用して、参照フォルダー内のすべてのパッケージを復元してから、プロキシを生成します。 この手順を実行しないと、RetailSDK\Reference フォルダーで CommerceProxyGenerator.exe パッケージを利用できません。

Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator.<version_number>\tools フォルダーから CommerceProxyGenerator.exe ファイルを使用して、POS の typescript プロキシを生成します。

1. プロキシを生成する前に、カスタマイズされた Retail サーバー API、CRT、その他の依存ライブラリを、**Retail SDK\\参照** フォルダーにコピーしてください。
2. 管理者としてコマンド プロンプト ウィンドウを開き、**...\\Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator\<version_number>\tools** フォルダーへ移動します。 次のコマンドを実行してプロキシを生成します。 プロキシ ファイルは同じフォルダーに生成されます。

  
  POS TypeScript プロキシ
```Console 
    CommerceProxyGenerator.exe <Path>\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptextensions
```
 E コマース TypeScript プロキシ
 ```Console 
    CommerceProxyGenerator.exe <Path>\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptmoduleextensions
```

> [!NOTE]
> Microsoft.Dynamics.Retail.RetailServerLibrary.dll file from \RetailSDK\References\Microsoft.Dynamics.Commerce.Tools.ExtensionsProxyGenerator.<version_number>\build を使用します。

```Console
Example
CommerceProxyGenerator.exe C:\\RetailSDK\\References\\Microsoft.Dynamics.Commerce.Tools.ExtensionsProxyGenerator.9.21.20042.5\\build\\Microsoft.Dynamics.Retail.RetailServerLibrary.dll C:\\RetailSDK\\References\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll /a:typescriptextensions
```

実行するコマンドで、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** をカスタム Retail サーバー拡張ライブラリの名前に置き換えます。 POS プロジェクトに生成されたファイルを含めます。 このコマンドは、拡張ライブラリに基づいた 2 つのファイル、DataServiceEntities.g.ts と DataServiceRequests.g.tss を生成します。

## <a name="generate-the-c-proxy-commerce-version-10011-or-lower"></a>C# プロキシ (Commerce バージョン 10.0.11 以下) の生成

> [!IMPORTANT]
> この Microsoft.Dynamics.Commerce.Hosting.Contracts API を使用してビルトされた Retail Server 拡張機能は、オフライン実装でも使用でき、別に C# プロキシ ライブラリを作成する必要はありません。 この手順は、Dynamics.Commerce.Runtime.Hosting.Contracts を使用しない Commerce バージョン 10.0.11 以前、または低またはRetail Server の拡張機能に対してのみ必要です。

Retail サーバー拡張機能ごとに、別個のプロキシを生成する必要があります。

1. **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample** に移動します。
2. Microsoft Visual Studio で、**Proxies.RetailProxy.Extensions.StoreHoursSample** プロジェクト ファイルを開きます。
3. 右クリックし、プロジェクトのアンロードを選択します。
4. プロジェクトを右クリックし、**Proxies.RetailProxy.Extensions.StoreHoursSample.csproj** を選択して編集します。
5. 最初のプロパティ グループ セクションで、次のノードを更新します。

    - **&lt;RootNamespace&gt;** – ユーザー設定の名前空間を指定します。
    - **&lt;AssemblyName&gt;** – プロキシのカスタム出力ライブラリ名を指定します。

6. Retail サーバーの拡張機能ライブラリ名を指定して、**CommerceProxyGeneratorExtendedAssemblyPaths** 要素を更新します。

    次に例を示します。

    ```xml
    <CommerceProxyGeneratorExtendedAssemblyPaths Include="..\..\RetailServer\Extensions.StoreHoursSample\bin\$(Configuration)\net451\$(AssemblyNamePrefix).RetailServer.StoreHoursSample.dll" />
    ```

    > [!NOTE]
    > **.RetailServer.StoreHoursSample.dll** は、Retail サーバー拡張アセンブリの名前です。残りの値は、接頭語 (接頭語がある場合) と、プロキシ エンジンがこのアセンブリを見つけることができるアセンブリのパスです。 プロキシは、このアセンブリに基づいて生成されます。

7. ファイルを保存し、プロジェクトを再度読み込みます。
8. 拡張パターンに従って、プロジェクトの名前を変更します。
9. プロジェクトが読み込まれた後、**アダプタ** フォルダから **StoreDayHoursManager.cs** ファイルを削除します。
10. すべての関連する CRT と Retail サーバー ライブラリをプロジェクトまたはアセンブリ参照としてプロキシ プロジェクトに追加します。
11. プロジェクトをリビルドします。

    アダプタ フォルダー内で新しい Interfaces.g.cs ファイルが生成されると表示されます。

    > [!NOTE]
    > プロキシ プロジェクトを作成する前に、すべての CRT および Retail サーバー拡張ライブラリを再構築して、**RetailSDK\\References** フォルダーにドロップしてください。

12. プロキシ プロジェクト内に新しい **Interfaces.g.cs** ファイルを含めます。 ただし、このファイルを変更しないでください。
13. **アダプタ** フォルダーで、新しいクラス ファイルを追加し、拡張機能のパターンに従って名前をつけます。
14. インターフェイス マネージャー クラスからクラスを拡張し、必要なインターフェイス メソッドのみを実装します。

    > [!NOTE]
    > Interfaces.g.cs ファイルで、インターフェイス マネージャー クラスの名前を見つけることが できます。

    次の例では、**IStoreDayHoursManager** はインターフェイスの名前です。

    ```C#
    public interface IStoreDayHoursManager : Microsoft.Dynamics.Commerce.RetailProxy.IEntityManager
    {
    }
    ```

    フル サンプル コードについては、**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample** にある **Proxies.RetailProxy.Extensions.StoreHoursSample** プロジェクトをご覧ください。

15. メソッド内で、実際の CRT 要求/応答を呼び出します。 プロキシ プロジェクトに任意のロジックを含めないようにしてください。 プロキシ プロジェクトは、CRT 要求/応答だけを呼び出す必要があります。
16. プロジェクトを構築します。
17. 出力アセンブリをコピーして、**RetailSDK\\References** フォルダーに貼り付けます。
18. **RetailSDK\\Assets** フォルダーに移動して **RetailProxy.MPOSOffline.ext.config** を開きます。
19. **合成** セクションで、新しいプロキシ ライブラリ (つまり、プロキシ プロジェクトをビルドした後に生成されたアセンブリ) の名前を登録します。

    次に例を示します。

    ```xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />
    ```

    この例では、プロキシ ライブラリ名は **Contoso.Commerce.RetailProxy.StoreHoursSample** です。 プロキシ ライブラリの名前は、**値** フィールドで指定してください。

20. 手動テストでは、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** にある **RetailProxy.MPOSOffline.ext.config** ファイルを開きます。カスタム プロキシ ライブラリの名前で **合成** セクションを更新します。

    次に例を示します。

    ```xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />
    ```

21. 電子商取引の場合、電子商取引プロジェクトから呼び出しする前に、拡張のプロキシを初期化する必要があります。 電子商取引の **Startup.cs** ファイル (または、Web プロジェクトの初期化などの同等のファイル) で、Retail プロキシ拡張の拡張データ モデル (EDM) を使用して **RetailServerContext** を初期化します。 それ以外の場合、プロキシのを呼び出そうとすると、ランタイム エラーが表示されます。 このステップは 1 回のみ完了する必要があります。

    次に例を示します。

    ```C#
    RetailServerContext.Initialize(newIEdmModelExtension[]
    {
        // /* BEGIN SDKSAMPLE_STOREHOURS
        new Contoso.Commerce.RetailProxy.StoreHoursSample.EdmModel(),
        // END SDKSAMPLE_STOREHOURS */
    });
    ```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
