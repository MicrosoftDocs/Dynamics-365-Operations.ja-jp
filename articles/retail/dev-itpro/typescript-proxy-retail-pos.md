---
title: Typescript および小売販売時点管理 (POS) の C# プロキシ
description: このトピックでは、Retail プロキシに関する情報と、その生成方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-20
ms.dyn365.ops.version: AX 7.0.0, Retail October 2017 update
ms.openlocfilehash: f2a2ad56d7492a87069a6204081fba079e53fa1b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537522"
---
# <a name="typescript-and-c-proxies-for-retail-point-of-sale-pos"></a>Typescript および小売販売時点管理 (POS) の C# プロキシ

[!include [banner](../../includes/banner.md)]

Retail サーバー アプリケーション プログラミング インターフェイス (API) の新しいコント ローラーを作成するたびに、または既存のコントローラーを拡張するたびに、Retail ソフトウェアの開発キット (SDK) の一部としてし使用できるツールを使用して、Retail プロキシを生成する必要があります。 たとえば、顧客コントローラーを拡張することにより、顧客エンティティの新しい API を追加する場合、Retail プロキシを生成する必要があります。

## <a name="what-is-the-retail-proxy-used-for-and-when-should-you-use-it"></a>Retail プロキシは何に使用される、またそれをいつ使用する必要があるか ?

すべてのクライアントは Retail サーバーとやりとりするためにプロキシ API を使用します。 Retail プロキシは、Retail Server と Commerce Runtime (CRT) 間のインターフェイスを抽象化します。 たとえば、CRT で要求/応答の操作として新しいエンティティとビジネス ロジックを作成し、そのエンティティおよびそれらの要求/応答の操作を公開するために、新しい Retail サーバー API を追加できます。 販売時点管理 (POS) におけるエンティティと要求/応答動作にアクセスして、あるクライアント ロジックを実行する必要が出てきました。 POS ですべてのエンティティと要求/応答メタデータを手動で作成し、適切なパラメーターを使用して Retail サーバーにアクセスすることができます。 ただし、エンティティ、マネージャ、および 2 つの場所で要求/応答コードを複製する必要があり、および多くのコードの書き込みもする必要があるため、このアプローチには追加の間接費が多く含まれます。

Retail プロキシは、Retail Server に追加されたすべてのユーザー定義エンティティと要求/応答操作のプロキシを自動的に作成することによって、この労力を軽減します。 プロキシ ツールは、必須のインターフェイスとすべての必須メタデータを生成し、実際の実装を抽象化します。 この方法では、拡張プロジェクトにファイルを含めることができ、生成されたメタデータとインターフェイスを使用して Retail サーバー API とエンティティにアクセスできます。

## <a name="proxy-types"></a>プロキシのタイプ

クロス プラットフォーム シナリオをサポートするプロキシのタイプには 2 つあります。

- **Typescript プロキシ** – POS は、Typescript プロキシを使用して Retail サーバー API および CRT エンティティにアクセスします。 POS が Retail サーバーを使用する場合は、Typescript プロキシが必要です。 それ以外の場合、POS はオペレーションまたはワークフローのために Retail サーバーと通信することができません。
- **C# プロキシ** - POS はオフラインのときに C# プロキシを使用します。 (POS がオフラインの場合、Retail サーバーを使用せずに CRT と直接通信します)。POS は、Dynamics 電子商取引プラットフォームにもこのプロキシを使用します。 カスタマイゼーションを POS がオフラインのときに動作させ、電子商取引クライアントを Retail Server API にアクセスするようにするには、C＃ プロキシを生成する必要があります。

Typescript プロキシを生成する手順と C# プロキシを生成する手順は異なります。 このトピックの後半では、各タイプのプロキシを生成する方法について説明します。

## <a name="generate-the-typescript-proxy"></a>Typescript プロキシを生成します

> [!IMPORTANT]
> 次の手順は Microsoft Dynamics 365 for Retail (2017 年 7 月リリース) および Microsoft Dynamics 365 for Finance and Operation にのみ適用されます。

POS の Typescript プロキシを生成するには、Retail SDK\\Reference フォルダーから CommerceProxyGenerator.exe ファイルを使用します。

[!NOTE] 
> 最新版の Retail には CommerceProxyGenerator.x.x.x.x (x.x.x.x はバージョン番号で SDK のバージョンによって異なります) という名前のフォルダがあります。 このフォルダは、CommerceProxyGenerator.exe および手順 1 で示すすべてのライブラリと共に RetailSDK\Code\References\, の下に事前コピーされているため、以下で説明する手順 1 を実行する必要はありません。 プロキシを生成するには、このフォルダーから CommerceProxyGenerator を使用する必要があります。

1. プロキシを生成する前に、次のライブラリを **Retail SDK\\Reference\\..** から **Retail SDK\\Reference** フォルダーにコピーします。

    - Microsoft.OData.Core.dll@ 6.11.0.0
    - Microsoft.OData.Edm.dll@ 6.11.0.0
    - Microsoft.Spatial.dll@ 6.11.0.0
    - System.Web.Http.dll@ 5.2.2.0
    - System.Web.OData.dll@ 5.5.1.0

2. カスタマイズされた Retail サーバーと CRT ライブラリを **Retail SDK\\Reference** フォルダーにコピーします。
3. 管理者モードでコマンド プロンプトを開き、**...\\Retail SDK\\Reference** フォルダーに移動します。 次のコマンドを実行してプロキシを生成します。 プロキシ ファイルは同じフォルダーに生成されます。

    ```
    CommerceProxyGenerator.exe <Path>\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptextensions
    
> [!NOTE]
> Use the Microsoft.Dynamics.Retail.RetailServerLibrary.dll file from RetailSDK\Code\References\Microsoft.Dynamics.Retail.RetailServerLibrary.x.x.x.x (x.x.x.x is the version number, which varies based on your SDK version).

Here is an example.

    ``` 
    CommerceProxyGenerator.exe C:\RetailSDK\Reference\Microsoft.Dynamics.Retail.RetailServerLibrary.dll C:\RetailSDK\Reference\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll /application:typescriptextensions
    ```



    In the command that you run, replace **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** with the name of your custom Retail Server extension library. Include the generated files in your POS project. The command generates two files that are based on your extension libraries: DataServiceEntities.g.ts and DataServiceRequests.g.ts.

    > [!NOTE]
    > You must generate the proxy for all Retail Server extensions.

## Generate the C# proxy (7.1 and 7.2)

> [!IMPORTANT]
> The following procedure doesn't apply to version 7.3 and later.

1. Open the **Customization.settings** file from **...Retail SDK\\BuildTools**.
2. Under the **RetailServerLibraryPathForProxyGeneration** node, include all your custom Retail Server extension libraries, as shown here.

    ```
    <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll"/>;
    ```

    In this example, there is just one custom library, **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll**. However, be sure to include all your custom Retail Server extension libraries.

3. Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**.
4. Include your custom CRT project library as a reference to **Proxies.RetailProxy.csproj**.
5. Open **RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions.txt** in the solution.
6. In **UsingStatements.Extensions.txt**, add the **using** statement for your CRT entity namespace and request/response namespace. For example, if you use the **Contoso.Commerce.Runtime.DataModel** namespace in your CRT extension, add that namespace in **UsingStatements.Extensions.txt** to generate the proxy, as shown here.

    ```
    Contoso.Commerce.Runtime.DataModel を使用します;
    ```

7. Build the project.
8. Add a new class under the **Adapters** folder. Use any other manager class from the adapter folder as a template, so that the whole namespace is included.
9. Extend the class from the interface manager, and implement only the required interface methods.
  
    To learn how generate the interface and manager classes, see the Store Hours sample in the Retail SDK. The instructions are in the **RetailSDK\\Code\\Documents\\SampleExtensionsInstructions\\StoreHours\\readme.txt** file.

## Generate the C# proxy (7.3)

> [!IMPORTANT]
> The following procedure applies to both the POS and e-Commerce.

For each Retail Server extension, you must generate a separate proxy.

1. Navigate to **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample**.
2. In Microsoft Visual Studio, open the **Proxies.RetailProxy.Extensions.StoreHoursSample** project file.
3. Right-click, and select to unload the project.
4. Right-click the project, and select to edit the **Proxies.RetailProxy.Extensions.StoreHoursSample.csproj** file.
5. In the first property group section, update the following nodes:

    - **&lt;RootNamespace&gt;** – Specify your custom namespace.
    - **&lt;AssemblyName&gt;** – Specify your custom output library name for the proxy.

6. Update the **CommerceProxyGeneratorExtendedAssemblyPaths** element by specifying the name of your Retail Server extension library.

    Here is an example.

    ```
    <CommerceProxyGeneratorExtendedAssemblyPaths Include="..\..\RetailServer\Extensions.StoreHoursSample\bin\$(Configuration)\net451\$(AssemblyNamePrefix).RetailServer.StoreHoursSample.dll" />
    ```

    > [!NOTE]
    > **.RetailServer.StoreHoursSample.dll** is the name of the Retail Server extension assembly, and the rest of the value is the prefix (if there is a prefix) and the path of the assembly where the proxy engine can find this assembly. The proxy is generated based on this assembly.

7. Save the file, and load the project again.
8. Rename the project according to your extension pattern.
9. After the project is loaded, delete the **StoreDayHoursManager.cs** file from the **Adapters** folder.
10. Add all the relevant CRT and Retail Server libraries to the proxy project as project or assembly references.
11. Rebuild the project.

    You will see that a new Interfaces.g.cs file is generated inside the Adapters folder.

    > [!NOTE]
    > Before you build the proxy project, rebuild all your CRT and Retail Server extension libraries, and drop them into the **RetailSDK\\References** folder.

12. Include the new **Interfaces.g.cs** file in the proxy project. However, don't modify this file.
13. Under the **Adapters** folder, add a new class file, and name it according to your extension pattern.
14. Extend the class from the interface manager class, and implement only the interface methods that are required.

    > [!NOTE]
    > You can find the name of the interface manager class in the Interfaces.g.cs. file.

    In the following example, **IStoreDayHoursManager** is the name of the interface.

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

    ```
    <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />
    ```

    この例では、プロキシ ライブラリ名は **Contoso.Commerce.RetailProxy.StoreHoursSample** です。 プロキシ ライブラリの名前は、**値** フィールドで指定してください。

20. 手動テストでは、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** にある **RetailProxy.MPOSOffline.ext.config** ファイルを開きます。カスタム プロキシ ライブラリの名前で **合成** セクションを更新します。

    次に例を示します。

    ```
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
