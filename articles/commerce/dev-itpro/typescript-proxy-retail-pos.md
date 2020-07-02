---
title: Typescript および小売販売時点管理 (POS) の C# プロキシ
description: このトピックでは、コマース プロキシに関する情報と、その生成方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 06/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-20
ms.dyn365.ops.version: AX 7.0.0, Retail October 2017 update
ms.openlocfilehash: 862fbd14fb7c57156c8c04b325f340d8384e5171
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443477"
---
# <a name="typescript-and-c-proxies-for-retail-point-of-sale-pos"></a>Typescript および小売販売時点管理 (POS) の C# プロキシ

[!include [banner](../../includes/banner.md)]

Commerce Scale Unit アプリケーション プログラミング インターフェイス (API) の新しいコントローラーを作成するたびに、または既存のコントローラーを拡張するたびに、Retail ソフトウェアの開発キット (SDK) の一部として提供されているツールを使用して、Commerce プロキシを生成する必要があります。 たとえば、顧客コントローラーを拡張することにより、顧客エンティティの新しい API を追加する場合、コマース プロキシを生成する必要があります。

## <a name="what-is-the-commerce-proxy-used-for-and-when-should-you-use-it"></a>コマース プロキシは何に使用され、いつ使用するか?

すべてのクライアントは Commerce Scale Unit とやりとりするためにプロキシ API を使用します。 コマース プロキシは、Commerce Scale Unit と Commerce Runtime (CRT) 間のインターフェイスを抽象化します。 たとえば、CRT で要求/応答の操作として新しいエンティティとビジネス ロジックを作成し、そのエンティティおよびそれらの要求/応答の操作を公開するために、新しい Commerce Scale Unit API を追加できます。 販売時点管理 (POS) におけるエンティティと要求/応答動作にアクセスして、あるクライアント ロジックを実行する必要が出てきました。 POS ですべてのエンティティと要求/応答メタデータを手動で作成し、適切なパラメーターを使用して Commerce Scale Unit にアクセスすることができます。 ただし、エンティティ、マネージャ、および 2 つの場所で要求/応答コードを複製する必要があり、および多くのコードの書き込みもする必要があるため、このアプローチには追加の間接費が多く含まれます。

コマース プロキシは、Commerce Scale Unit に追加されたすべてのカスタム エンティティと要求/応答操作のプロキシを自動的に作成することによって、この労力を軽減します。 プロキシ ツールは、必須のインターフェイスとすべての必須メタデータを生成し、実際の実装を抽象化します。 この方法では、拡張プロジェクトにファイルを含めることができ、生成されたメタデータとインターフェイスを使用して Commerce Scale Unit API とエンティティにアクセスできます。

## <a name="proxy-types"></a>プロキシのタイプ

クロス プラットフォーム シナリオをサポートするプロキシのタイプには 2 つあります。

- **Typescript プロキシ** – POS は、Typescript プロキシを使用して Commerce Scale Unit API および CRT エンティティにアクセスします。 POS が Commerce Scale Unit を使用する場合は、Typescript プロキシが必要です。 でなければ、POS はオペレーションまたはワークフローのために Commerce Scale Unit と通信することができません。
- **C# プロキシ** - POS はオフラインのときに C# プロキシを使用します。 (POS がオフラインの場合、Commerce Scale Unit を使用せずに CRT と直接通信します)。POS は、Dynamics 電子商取引プラットフォームにもこのプロキシを使用します。 POS がオフラインのときにカスタマイズを動作させ、電子商取引クライアントが Commerce Scale Unit API にアクセスできるようにするには、C# プロキシを生成する必要があります。

Typescript プロキシを生成する手順と C# プロキシを生成する手順は異なります。 このトピックの後半では、各タイプのプロキシを生成する方法について説明します。

## <a name="generate-the-typescript-proxy"></a>Typescript プロキシを生成します

> [!IMPORTANT]
> 次の手順は Microsoft Dynamics 365 Retail (2017 年 7 月リリース) および Microsoft Dynamics 365 Finance にのみ適用されます。 Retail SDK のルート フォルダから MSBuild を使用する必要があります。 Visual studio の開発者コマンド プロンプト、または MSBuild コマンドプロンプトを使用して、参照フォルダー内のすべてのパッケージを復元してから、プロキシを生成します。 この手順を実行しない場合、RetailSDK\Reference フォルダーに CoreProxyGenerator.exe パッケージを利用できません。

Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator.<version_number>\tools フォルダーから CommerceProxyGenerator.exe ファイルを使用して、POS の typescript プロキシを生成します。

1. プロキシを生成する前に、カスタマイズした Commerce Scale Unit、CRT、およびその他の依存ライブラリを、**Retail SDK\\Reference** フォルダにコピーします。
2. 管理者としてコマンド プロンプト ウィンドウを開き、**...\\Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator.<version_number>\tools** フォルダへ移動します。 次のコマンドを実行してプロキシを生成します。 プロキシ ファイルは同じフォルダーに生成されます。

    ```Console
    CommerceProxyGenerator.exe <Path>\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptextensions
    ```

> [!NOTE]
> \RetailSDK\References\Microsoft.Dynamics.Commerce.Tools.ExtensionsProxyGenerator.<version_number>\build から Microsoft.Dynamics.Retail.RetailServerLibrary.dll ファイルを使用します。

```Console
Ex:
CommerceProxyGenerator.exe C:\\RetailSDK\\References\\Microsoft.Dynamics.Commerce.Tools.ExtensionsProxyGenerator.9.21.20042.5\\build\\Microsoft.Dynamics.Retail.RetailServerLibrary.dll C:\\RetailSDK\\References\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll /a:typescriptextensions
```

実行するコマンドで、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** をカスタム Commerce Scale Unit 拡張ライブラリの名前に置き換えます。 POS プロジェクトに生成されたファイルを含めます。 このコマンドは、拡張ライブラリに基づいた 2 つのファイル、DataServiceEntities.g.ts と DataServiceRequests.g.tss を生成します。

> [!NOTE]
> すべての Commerce Scale Unit 拡張機能のプロキシを生成する必要があります。

## <a name="generate-the-c-proxy-71-and-72"></a>C# プロキシ (7.1 および 7.2) の生成

> [!IMPORTANT]
> 7.3 以降のバージョンには、次の手順は適用されません。

1. **Customization.settings** ファイルを **...Retail SDK\\BuildTools** から開きます。
2. **RetailServerLibraryPathForProxyGeneration** ノードの下には、次に示すように、すべてのカスタム Retail サーバー拡張ライブラリを含めます。

    ```xml
    <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll"/>;
    ```

    この例では、カスタム ライブラリは **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** の 1 つだけあります。 ただし、カスタム Retail サーバー拡張ライブラリが含まれるようにします。

3. **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開きます。
4. カスタム CRT プロジェクト ライブラリを **Proxies.RetailProxy.csproj** への参照として含めます。
5. ソリューションの **RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions.txt** を開きます。
6. **UsingStatements.Extensions.txt** で、CRT エンティティの名前空間および要求/応答の名前空間の **using** ステートメントを追加します。 たとえば、CRT 拡張機能で **Contoso.Commerce.Runtime.DataModel** 名前空間を使用する場合、ここに示すように、追加プロキシを生成するため **UsingStatements.Extensions.txt** にその名前空間を追加します。

    ```csharp
    using Contoso.Commerce.Runtime.DataModel;
    ```

7. プロジェクトを構築します。
8. **アダプタ** フォルダの新しいクラスを追加します。 アダプター フォルダーの他のマネージャー クラスをテンプレートとして使用すると、名前空間全体が含まれます。
9. インターフェイス マネージャーからクラスを拡張し、必要なインターフェイス メソッドのみを実装します。
  
    インターフェイス クラスとマネージャ クラスの生成方法については、Retail SDK の Store Hours サンプルを参照してください。 指示は、**RetailSDK\\Code\\Documents\\SampleExtensionsInstructions\\StoreHours\\readme.txt** ファイルにあります。

## <a name="generate-the-c-proxy-73"></a>C# プロキシ (7.3) の生成

> [!IMPORTANT]
> 次の手順は、POS と電子商取引の両方に適用されます。

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
