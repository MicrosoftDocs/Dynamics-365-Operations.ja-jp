---
title: "Retail POS の Typescript と C# プロキシ"
description: "このトピックでは、Retail プロキシに関する情報と、その生成方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-20
ms.dyn365.ops.version: AX 7.0.0, Retail October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 490b7654b86e7bf32393362fd864f1a96f4b7b25
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="retail-typescript-and-c-proxies"></a>Retail の Typescript プロキシと C# プロキシ

[!include [banner](../../includes/banner.md)]

Retail サーバー アプリケーション プログラミング インターフェイス (API) の新しいコント ローラーを作成するたびに、または既存のコントローラーを拡張するたびに、Retail ソフトウェアの開発キット (SDK) の一部としてし使用できるツールを使用して、Retail プロキシを生成する必要があります。 たとえば、顧客コントローラーを拡張することにより、顧客エンティティの新しい API を追加する場合、Retail プロキシを生成する必要があります。

## <a name="what-is-the-retail-proxy-used-for-and-when-should-you-use-it"></a>Retail プロキシは何に使用される、またそれをいつ使用する必要があるか ?

すべてのクライアントは Retail サーバーと対話するためにプロキシ API を使用します。 Retail プロキシは、Retail Server と Commerce Runtime (CRT) 間のインターフェイスを抽象化します。 たとえば、CRT で要求/応答の操作として新しいエンティティとビジネス ロジックを作成し、そのエンティティおよびそれらの要求/応答の操作を公開するために、新しい Retail サーバー API を追加できます。 販売時点管理 (POS) におけるエンティティと要求/応答動作にアクセスして、あるクライアント ロジックを実行する必要が出てきました。 POS ですべてのエンティティと要求/応答メタデータを手動で作成し、適切なパラメーターを使用して Retail サーバーにアクセスすることができます。 ただし、エンティティ、マネージャ、および 2 つの場所で要求/応答コードを複製する必要があり、および多くのコードの書き込みもする必要があるため、このアプローチには追加の間接費が多く含まれます。

Retail プロキシは、Retail Server に追加されたすべてのユーザー定義エンティティと要求/応答操作のプロキシを自動的に作成することによって、この労力を軽減します。 プロキシ ツールは、必須のインターフェイスとすべての必須メタデータを生成し、実際の実装を抽象化します。 この方法では、拡張プロジェクトにファイルを含めることができ、生成されたメタデータとインターフェイスを使用して Retail サーバー API とエンティティにアクセスできます。

## <a name="proxy-types"></a>プロキシのタイプ

クロス プラットフォーム シナリオをサポートするプロキシのタイプには 2 つあります。

- **Typescript プロキシ** – POS は、Typescript プロキシを使用して Retail サーバー APIs および CRT エンティティにアクセスします。 POS が Retail サーバーを使用する場合は、Typescript プロキシーが必要です。 それ以外の場合、POS はオペレーションまたはワークフローのために Retail サーバーと通信することができません。
- **C# プロキシ** - POS はオフラインで、E コマースのために C# プロキシを使用します。 (POS がオフラインの場合、Retail サーバーを使用せずに CRT と直接通信します。) POS がオフラインのときにカスタマイズを動作させ、E コマースクライアントが Retail サーバー API にアクセスするようにするには、C# プロキシを生成する必要があります。

> [!NOTE]
> Typescript プロキシと C# プロキシは異なっており、この 2 つを作成する手順も異なります。

## <a name="generate-the-typescript-proxy"></a>Typescript プロキシを生成します

以下の手順は、Microsoft Dynamics 365 for Retail (2017 年 7 月リリース) と Microsoft Dynamics 365 for Finance and Operation にのみ適用されます。

POS の Typescript プロキシを生成するには、Retail SDK\Reference フォルダーから CommerceProxyGenerator.exe ファイルを使用します。

1. プロキシを生成する前に、次のライブラリを **Retail SDK\Reference\...** から **Retail SDK\Reference** フォルダーにコピーします。

    - Microsoft.OData.Core.dll@ 6.11.0.0
    - Microsoft.OData.Edm.dll@ 6.11.0.0
    - Microsoft.Spatial.dll@ 6.11.0.0
    - System.Web.Http.dll@ 5.2.2.0
    - System.Web.OData.dll@ 5.5.1.0

2. カスタマイズされた Retail サーバーと CRT ライブラリを **Retail SDK\Reference** フォルダーにコピーします。
3. 管理者モードでコマンド プロンプトを開き、**...\Retail SDK\Reference** フォルダーに移動します。 次のコマンドを実行してプロキシを生成します。 プロキシ ファイルは同じフォルダーに生成されます。

    ```
    CommerceProxyGenerator.exe <Path>\\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptextensions
    ```

    次に例を示します。

    ``` 
    CommerceProxyGenerator.exe C:\\RetailSDK\\Reference\\Microsoft.Dynamics.Retail.RetailServerLibrary.dll C:\\RetailSDK\\Reference\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll /application:typescriptextensions
    ```

    実行するコマンドで、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** をカスタム Retail サーバー拡張子ライブラリの名前に変えます。 POS プロジェクトに生成されたファイルを含めます。 このコマンドは、拡張ライブラリに基づいた 2 つのファイル、DataServiceEntities.g.ts と DataServiceRequests.g.tss を生成します。

    > [!NOTE]
    > すべての Retail サーバー拡張機能のプロキシを生成する必要があります。

## <a name="generate-the-c-proxy-71-and-72---these-steps-are-not-applicable-for-version-73-and-higher"></a>C# プロキシ (7.1 および 7.2) の生成 - これらの手順は 7.3 およびより大きいバージョンには適用できません

1. **Customization.settings** ファイルを **...Retail SDK\BuildTools** から開きます。
2. **RetailServerLibraryPathForProxyGeneration** ノードの下には、次に示すように、すべてのカスタム Retail サーバー拡張ライブラリを含めます。

    ```
    <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll"/>;
    ```

    この例では、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** はカスタム ライブラリです。

    > [!NOTE]
    > すべてのカスタム Retail サーバー拡張ライブラリを追加します。

3. **RetailSDK\Proxies\RetailProxy\Proxies.RetailProxy.csproj** を開きます。
4. カスタム CRT プロジェクト ライブラリを **Proxies.RetailProxy.csproj** への参照として含めます。
5. ソリューションの **RetailSDK\Proxies\RetailProxy\Adapters\UsingStatements.Extensions.txt** を開きます。
6. **UsingStatements.Extensions.txt** で、CRT エンティティの名前空間および要求/応答の名前空間の **using** ステートメントを追加します。 たとえば、CRT 拡張機能で **Contoso.Commerce.Runtime.DataModel** 名前空間を使用する場合、追加プロキシを生成するため **UsingStatements.Extensions.txt** にその名前空間を追加します。

    ```
    using Contoso.Commerce.Runtime.DataModel;
    ```

7. プロジェクトを構築します。
8. **アダプタ** フォルダの新しいクラスを追加します。 アダプター フォルダーの他のマネージャー クラスをテンプレートとして使用すると、名前空間全体が含まれます。
9. インターフェイス マネージャーからクラスを拡張し、必要なインターフェイス メソッドのみを実装します。

    インターフェイス クラスとマネージャ クラスの生成方法については、Retail SDK の Store Hours サンプルを参照してください。 指示は、**RetailSDK\Code\Documents\SampleExtensionsInstructions\StoreHours\readme.txt** ファイルにあります。
    
**7.3 で C# プロキシ (これは POS と e コマースの両方に適用されます) を生成する方法**

1.  RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions に移動します。 StoreHoursSample

2.  Proxies.RetailProxy.Extensions.StoreHoursSample プロジェクト ファイルを Visual Studio で開きます。

3.  Visual Studio で、右クリックし、プロジェクトをアップロードします。

4.  プロジェクトを右クリックし、[Proxies.RetailProxy.Extensions.StoreHoursSample.csproj ファイルの編集] を選択します。

5.  最初のプロパティ グループ セクションにある次のノードを更新します。

    <RootNamespace> - ユーザー設定の名前空間で更新します。

    <AssemblyName>- プロキシのカスタム出力ライブラリ名で更新する

    <RetailServerExtensionLibraryNoPrefixForRetailProxyCSharpExtensionGeneration>- Retail サーバー拡張子ライブラリ名で更新します。

    **注記:** プロキシは、このライブラリ名に基づいて生成されます。

6.  csproj ファイルを保存し、プロジェクトを再度読み込みます。

7.  拡張パターンに従って、プロジェクトの名前を変更します。

8.  プロジェクトが読み込まれたら、アダプタ フォルダから StoreDayHoursManager.cs ファイルを削除します。

9.  プロジェクト参照としてすべての関連する CRT ライブラリを追加します。 (Retail サーバーの拡張機能で参照または使用される CRT ライブラリ)

10. プロジェクトをリビルドします。

    注記: プロキシ プロジェクトを作成する前に、すべての CRT および Retail サーバー拡張ライブラリを再構築して、RetailSDK\\References フォルダーにドロップしてください。

11. アダプタ フォルダーに新しいクラス ファイルを追加し、拡張機能のパターンに従って名前をつけます。

12. 前の手順で追加した CRT エンティティと新しいクラスで使用される名前空間が同じであることを確認します。 (参照用に営業時間のサンプル プロキシと営業時間 CRT サンプル プロジェクトを確認する)

13. インターフェイス マネージャーからクラスを拡張およびインターフェイス メソッドを実装します。必要なインターフェイス メソッドのみがそのまま残ります。

    注記: インターフェイス名は、ワード コントローラーなしのコントローラー名に類似したものです。

    フル コード サンプルの RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample for full code sample にある Proxies.RetailProxy.Extensions.StoreHoursSample プロジェクトを確認してください。
  
14. メソッド内で、実際の CRT 要求/応答を呼び出します。 プロキシ プロジェクトではロジックを回避してください。CRT の要求/応答のみを呼び出す必要があります。

15. プロジェクトを構築します。

16. 出力アセンブリをコピーして、RetailSDK\\References フォルダーに貼り付けます。

17. RetailSDK\\Assets フォルダーに移動して RetailProxy.MPOSOffline.ext.config を開く

18. 合成セクションで、新しいプロキシ ライブラリ名を登録します。 (プロキシ プロジェクトの作成後に生成されるアセンブリです。

    前: <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />

    **注記:** 値フィールドには、プロキシ ライブラリの名前を追加します (Contoso.Commerce.RetailProxy.StoreHoursSample など)。

19. 手動テストでは、構成セクションでカスタム プロキシ ライブラリ名を持つ、C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext で、RetailProxy.MPOSOffline.ext.config を更新します。

    前: <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />

**注記:** 電子商取引の場合は、電子商取引プロジェクトから呼び出す前に、拡張機能のプロキシを初期化するためのもう 1 つの追加手順を実行する必要があります。

1. E コマース Startup.cs (または Web プロジェクトの初期化などの同等のもの) では、Retail プロキシの拡張機能の edm モデルで RetailServerContext を初期化する必要があり、そうせずにプロキシを呼び出そうとした場合、ランタイム エラーを受け取ります。 RetailServerContext を初期化するために、1 回のみこれを行う必要があります。
             
前:
```C#
  RetailServerContext.Initialize(newIEdmModelExtension[]
                {
                   // /* BEGIN SDKSAMPLE_STOREHOURS
 
                   new Contoso.Commerce.RetailProxy.StoreHoursSample.EdmModel(),
 
                    // END SDKSAMPLE_STOREHOURS */
                });
```

