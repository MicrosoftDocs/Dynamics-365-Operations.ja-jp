---
title: "Retail POS の Typescript と C# プロキシ"
description: "このトピックでは、Retail プロキシに関する情報と、その生成方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 10/20/2017
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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 6baf73c7892a23c842fdf0b04dd078be3a265feb
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="retail-typescript-and-c-proxies"></a><span data-ttu-id="f4723-103">Retail の Typescript プロキシと C# プロキシ</span><span class="sxs-lookup"><span data-stu-id="f4723-103">Retail Typescript and C# proxies</span></span>

[!INCLUDE [banner](../../includes/banner.md)]

<span data-ttu-id="f4723-104">Retail サーバー アプリケーション プログラミング インターフェイス (API) の新しいコント ローラーを作成するたびに、または既存のコントローラーを拡張するたびに、Retail ソフトウェアの開発キット (SDK) の一部としてし使用できるツールを使用して、Retail プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4723-104">Whenever you create a new controller for Retail server application programming interfaces (APIs) or extend the existing controller, you must generate the Retail proxy by using the tools that are available as part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="f4723-105">たとえば、顧客コントローラーを拡張することにより、顧客エンティティの新しい API を追加する場合、Retail プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4723-105">For example, you must generate the Retail proxy if you add a new API for the Customer entity by extending the Customer controller.</span></span>

## <a name="what-is-the-retail-proxy-used-for-and-when-should-you-use-it"></a><span data-ttu-id="f4723-106">Retail プロキシは何に使用される、またそれをいつ使用する必要があるか ?</span><span class="sxs-lookup"><span data-stu-id="f4723-106">What is the Retail proxy used for and when should you use it?</span></span>

<span data-ttu-id="f4723-107">すべてのクライアントは Retail サーバーと対話するためにプロキシ API を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4723-107">All the clients use the proxy API to interact with Retail server.</span></span> <span data-ttu-id="f4723-108">Retail プロキシは、Retail Server と Commerce Runtime (CRT) 間のインターフェイスを抽象化します。</span><span class="sxs-lookup"><span data-stu-id="f4723-108">The Retail proxy abstracts the interface between Retail server and the Commerce runtime (CRT).</span></span> <span data-ttu-id="f4723-109">たとえば、CRT で要求/応答の操作として新しいエンティティとビジネス ロジックを作成し、そのエンティティおよびそれらの要求/応答の操作を公開するために、新しい Retail サーバー API を追加できます。</span><span class="sxs-lookup"><span data-stu-id="f4723-109">For example, you create a new entity and some business logic as request/response operations in CRT, and you add a new Retail server API to expose that  entity and those request/response operations.</span></span> <span data-ttu-id="f4723-110">販売時点管理 (POS) におけるエンティティと要求/応答動作にアクセスして、あるクライアント ロジックを実行する必要が出てきました。</span><span class="sxs-lookup"><span data-stu-id="f4723-110">You now want to access the entity and the request/response operations in the point of sale (POS) to do some client logic.</span></span> <span data-ttu-id="f4723-111">POS ですべてのエンティティと要求/応答メタデータを手動で作成し、適切なパラメーターを使用して Retail サーバーにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="f4723-111">You can manually create all the entities and request/response metadata in the POS, and access the Retail server by using the correct parameters.</span></span> <span data-ttu-id="f4723-112">ただし、エンティティ、マネージャ、および 2 つの場所で要求/応答コードを複製する必要があり、および多くのコードの書き込みもする必要があるため、このアプローチには追加の間接費が多く含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4723-112">However, this approach involves lots of additional overhead, because you must duplicate the entities, manager, and request/response code in two places, and you must also write lots of code.</span></span>

<span data-ttu-id="f4723-113">Retail プロキシは、Retail Server に追加されたすべてのユーザー定義エンティティと要求/応答操作のプロキシを自動的に作成することによって、この労力を軽減します。</span><span class="sxs-lookup"><span data-stu-id="f4723-113">The Retail proxy reduces this effort by automatically generating the proxy for all the custom entities and request/response operations that are added in Retail server.</span></span> <span data-ttu-id="f4723-114">プロキシ ツールは、必須のインターフェイスとすべての必須メタデータを生成し、実際の実装を抽象化します。</span><span class="sxs-lookup"><span data-stu-id="f4723-114">The proxy tool generates the required interface and all the required metadata, and abstracts the actual implementation.</span></span> <span data-ttu-id="f4723-115">この方法では、拡張プロジェクトにファイルを含めることができ、生成されたメタデータとインターフェイスを使用して Retail サーバー API とエンティティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f4723-115">In that way, you can include the files in the extension projects, and can access the Retail server APIs and the entities by using the metadata and interface that are generated.</span></span>

## <a name="proxy-types"></a><span data-ttu-id="f4723-116">プロキシのタイプ</span><span class="sxs-lookup"><span data-stu-id="f4723-116">Proxy types</span></span>

<span data-ttu-id="f4723-117">クロス プラットフォーム シナリオをサポートするプロキシのタイプには 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="f4723-117">There two types of proxy to support cross-platform scenarios:</span></span>

- <span data-ttu-id="f4723-118">**Typescript プロキシ** – POS は、Typescript プロキシを使用して Retail サーバー APIs および CRT エンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f4723-118">**Typescript proxy** – The POS uses the Typescript proxy to access the Retail server APIs and CRT entities.</span></span> <span data-ttu-id="f4723-119">POS が Retail サーバーを使用する場合は、Typescript プロキシーが必要です。</span><span class="sxs-lookup"><span data-stu-id="f4723-119">If the POS is using Retail server, it requires the Typescript proxy.</span></span> <span data-ttu-id="f4723-120">それ以外の場合、POS はオペレーションまたはワークフローのために Retail サーバーと通信することができません。</span><span class="sxs-lookup"><span data-stu-id="f4723-120">Otherwise, the POS won't be able to communicate with the Retail server for any operations or workflows.</span></span>
- <span data-ttu-id="f4723-121">**C# プロキシ** - POS はオフラインで、E コマースのために C# プロキシを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4723-121">**C# proxy** – The POS uses the C# proxy when it's offline and for e-commerce.</span></span> <span data-ttu-id="f4723-122">(POS がオフラインの場合、Retail サーバーを使用せずに CRT と直接通信します。) POS がオフラインのときにカスタマイズを動作させ、E コマースクライアントが Retail サーバー API にアクセスするようにするには、C# プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4723-122">(When the POS is offline, it communicates directly with CRT, without using Retail server.) If you want your customization to work when the POS is offline, and you want your e-commerce client to access the Retail server APIs, you must generate the C# proxy.</span></span>

> [!NOTE]
> <span data-ttu-id="f4723-123">Typescript プロキシと C# プロキシは異なっており、この 2 つを作成する手順も異なります。</span><span class="sxs-lookup"><span data-stu-id="f4723-123">The Typescript proxy and C# proxy differ, and the steps to create them also differ.</span></span>

## <a name="generate-the-typescript-proxy"></a><span data-ttu-id="f4723-124">Typescript プロキシを生成します</span><span class="sxs-lookup"><span data-stu-id="f4723-124">Generate the Typescript proxy</span></span>

<span data-ttu-id="f4723-125">以下の手順は、Microsoft Dynamics 365 for Retail (2017 年 7 月リリース) と Microsoft Dynamics 365 for Finance and Operation にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f4723-125">The following steps apply only to Microsoft Dynamics 365 for Retail (July 2017 release) and Microsoft Dynamics 365 for Finance and Operation.</span></span>

<span data-ttu-id="f4723-126">POS の Typescript プロキシを生成するには、Retail SDK\Reference フォルダーから CommerceProxyGenerator.exe ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4723-126">You use the CommerceProxyGenerator.exe file from the Retail SDK\Reference folder to generate the Typescript proxy for the POS.</span></span>

1. <span data-ttu-id="f4723-127">プロキシを生成する前に、次のライブラリを **Retail SDK\Reference\...** から **Retail SDK\Reference** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f4723-127">Before you generate the proxy, copy the following libraries from **Retail SDK\Reference\...** to the **Retail SDK\Reference** folder:</span></span>

    - <span data-ttu-id="f4723-128">Microsoft.OData.Core.dll@ 6.11.0.0</span><span class="sxs-lookup"><span data-stu-id="f4723-128">Microsoft.OData.Core.dll@ 6.11.0.0</span></span>
    - <span data-ttu-id="f4723-129">Microsoft.OData.Edm.dll@ 6.11.0.0</span><span class="sxs-lookup"><span data-stu-id="f4723-129">Microsoft.OData.Edm.dll@ 6.11.0.0</span></span>
    - <span data-ttu-id="f4723-130">Microsoft.Spatial.dll@ 6.11.0.0</span><span class="sxs-lookup"><span data-stu-id="f4723-130">Microsoft.Spatial.dll@ 6.11.0.0</span></span>
    - <span data-ttu-id="f4723-131">System.Web.Http.dll@ 5.2.2.0</span><span class="sxs-lookup"><span data-stu-id="f4723-131">System.Web.Http.dll@ 5.2.2.0</span></span>
    - <span data-ttu-id="f4723-132">System.Web.OData.dll@ 5.5.1.0</span><span class="sxs-lookup"><span data-stu-id="f4723-132">System.Web.OData.dll@ 5.5.1.0</span></span>

2. <span data-ttu-id="f4723-133">カスタマイズされた Retail サーバーと CRT ライブラリを **Retail SDK\Reference** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f4723-133">Copy the customized Retail server and CRT libraries to the **Retail SDK\Reference** folder.</span></span>
3. <span data-ttu-id="f4723-134">管理者モードでコマンド プロンプトを開き、**...\Retail SDK\Reference** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="f4723-134">Open a Command Prompt window as an administrator, and navigate to the **...\Retail SDK\Reference** folder.</span></span> <span data-ttu-id="f4723-135">次のコマンドを実行してプロキシを生成します。</span><span class="sxs-lookup"><span data-stu-id="f4723-135">Run the following command to generate the proxy.</span></span> <span data-ttu-id="f4723-136">プロキシ ファイルは同じフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="f4723-136">The proxy files will be generated in the same folder.</span></span>

    ```
    CommerceProxyGenerator.exe <Path>\\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptextensions
    ```

    <span data-ttu-id="f4723-137">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f4723-137">Here is an example.</span></span>

    ``` 
    CommerceProxyGenerator.exe C:\\RetailSDK\\Reference\\Microsoft.Dynamics.Retail.RetailServerLibrary.dll C:\\RetailSDK\\Reference\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll /application:typescriptextensions
    ```

    <span data-ttu-id="f4723-138">実行するコマンドで、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** をカスタム Retail サーバー拡張子ライブラリの名前に変えます。</span><span class="sxs-lookup"><span data-stu-id="f4723-138">In the command that you run, replace **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** with the name of your custom Retail server extension library.</span></span> <span data-ttu-id="f4723-139">POS プロジェクトに生成されたファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="f4723-139">Include the generated files in your POS project.</span></span> <span data-ttu-id="f4723-140">このコマンドは、拡張ライブラリに基づいた 2 つのファイル、DataServiceEntities.g.ts と DataServiceRequests.g.tss を生成します。</span><span class="sxs-lookup"><span data-stu-id="f4723-140">The command will generate two files that are based on your extension libraries: DataServiceEntities.g.ts and DataServiceRequests.g.ts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4723-141">すべての Retail サーバー拡張機能のプロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4723-141">You must generate the proxy for all Retail server extensions.</span></span>

## <a name="generate-the-c-proxy-71-and-72---these-step-are-not-not-applicable-for-73-and-higher-versions"></a><span data-ttu-id="f4723-142">C# プロキシ (7.1 および 7.2) の生成 - これらの手順は 7.3 およびより大きいバージョンには適用できません。</span><span class="sxs-lookup"><span data-stu-id="f4723-142">Generate the C# proxy (7.1 and 7.2) - These step are not not applicable for 7.3 and higher versions.</span></span>

1. <span data-ttu-id="f4723-143">**Customization.settings** ファイルを **...Retail SDK\BuildTools** から開きます。</span><span class="sxs-lookup"><span data-stu-id="f4723-143">Open the **Customization.settings** files from **...Retail SDK\BuildTools**.</span></span>
2. <span data-ttu-id="f4723-144">**RetailServerLibraryPathForProxyGeneration** ノードの下には、次に示すように、すべてのカスタム Retail サーバー拡張ライブラリを含めます。</span><span class="sxs-lookup"><span data-stu-id="f4723-144">Under the **RetailServerLibraryPathForProxyGeneration** node, include all custom Retail server extension libraries, as shown here.</span></span>

    ```
    <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll"/>;
    ```

    <span data-ttu-id="f4723-145">この例では、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** はカスタム ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="f4723-145">In this example, **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** is the custom library.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4723-146">すべてのカスタム Retail サーバー拡張ライブラリを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4723-146">Add all your custom Retail server extension libraries.</span></span>

3. <span data-ttu-id="f4723-147">**RetailSDK\Proxies\RetailProxy\Proxies.RetailProxy.csproj** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f4723-147">Open **RetailSDK\Proxies\RetailProxy\Proxies.RetailProxy.csproj**.</span></span>
4. <span data-ttu-id="f4723-148">カスタム CRT プロジェクト ライブラリを **Proxies.RetailProxy.csproj** への参照として含めます。</span><span class="sxs-lookup"><span data-stu-id="f4723-148">Include your custom CRT project library as a reference to **Proxies.RetailProxy.csproj**.</span></span>
5. <span data-ttu-id="f4723-149">ソリューションの **RetailSDK\Proxies\RetailProxy\Adapters\UsingStatements.Extensions.txt** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f4723-149">Open **RetailSDK\Proxies\RetailProxy\Adapters\UsingStatements.Extensions.txt** in the solution.</span></span>
6. <span data-ttu-id="f4723-150">**UsingStatements.Extensions.txt** で、CRT エンティティの名前空間および要求/応答の名前空間の **using** ステートメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4723-150">In **UsingStatements.Extensions.txt**, add the **using** statement for your CRT entity namespace and request/response namespace.</span></span> <span data-ttu-id="f4723-151">たとえば、CRT 拡張機能で **Contoso.Commerce.Runtime.DataModel** 名前空間を使用する場合、追加プロキシを生成するため **UsingStatements.Extensions.txt** にその名前空間を追加します。</span><span class="sxs-lookup"><span data-stu-id="f4723-151">For example, if you use the **Contoso.Commerce.Runtime.DataModel** namespace in your CRT extension, add that namespace in **UsingStatements.Extensions.txt** to generate the proxy.</span></span>

    ```
    using Contoso.Commerce.Runtime.DataModel;
    ```

7. <span data-ttu-id="f4723-152">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="f4723-152">Build the project.</span></span>
8. <span data-ttu-id="f4723-153">**アダプタ** フォルダの新しいクラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4723-153">Add a new class under the **Adapters** folder.</span></span> <span data-ttu-id="f4723-154">アダプター フォルダーの他のマネージャー クラスをテンプレートとして使用すると、名前空間全体が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4723-154">Use any other manager class from the adapter folder as a template, so that the whole namespace is included.</span></span>
9. <span data-ttu-id="f4723-155">インターフェイス マネージャーからクラスを拡張し、必要なインターフェイス メソッドのみを実装します。</span><span class="sxs-lookup"><span data-stu-id="f4723-155">Extend the class from the interface manager, and implement only the required interface methods.</span></span>

    <span data-ttu-id="f4723-156">インターフェイス クラスとマネージャ クラスの生成方法については、Retail SDK の Store Hours サンプルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4723-156">To learn how generate the interface and manager classes, see the Store Hours sample in the Retail SDK.</span></span> <span data-ttu-id="f4723-157">指示は、**RetailSDK\Code\Documents\SampleExtensionsInstructions\StoreHours\readme.txt** ファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="f4723-157">The instructions are in the **RetailSDK\Code\Documents\SampleExtensionsInstructions\StoreHours\readme.txt** file.</span></span>
    
<span data-ttu-id="f4723-158">**7.3 で C# プロキシ (これは POS と e コマースの両方に適用されます) を生成する方法**</span><span class="sxs-lookup"><span data-stu-id="f4723-158">**How to generate C# proxy (this applicable for both POS and Ecommerce) for 7.3**</span></span>

1.  <span data-ttu-id="f4723-159">RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions に移動します。</span><span class="sxs-lookup"><span data-stu-id="f4723-159">Navigate to RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.</span></span> <span data-ttu-id="f4723-160">StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="f4723-160">StoreHoursSample</span></span>

2.  <span data-ttu-id="f4723-161">Proxies.RetailProxy.Extensions.StoreHoursSample プロジェクト ファイルを Visual Studio で開きます。</span><span class="sxs-lookup"><span data-stu-id="f4723-161">Open the Proxies.RetailProxy.Extensions.StoreHoursSample project file in visual studio.</span></span>

3.  <span data-ttu-id="f4723-162">Visual Studio で、右クリックし、プロジェクトをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f4723-162">In visual studio, right click and unload the project.</span></span>

4.  <span data-ttu-id="f4723-163">プロジェクトを右クリックし、[Proxies.RetailProxy.Extensions.StoreHoursSample.csproj ファイルの編集] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4723-163">Right click the project and choose Edit Proxies.RetailProxy.Extensions.StoreHoursSample.csproj file.</span></span>

5.  <span data-ttu-id="f4723-164">最初のプロパティ グループ セクションにある次のノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="f4723-164">Update the below nodes under the first property group section:</span></span>

    <span data-ttu-id="f4723-165"><RootNamespace> - ユーザー設定の名前空間で更新します。</span><span class="sxs-lookup"><span data-stu-id="f4723-165"><RootNamespace> - Update it with your custom namespace</span></span>

    <span data-ttu-id="f4723-166"><AssemblyName>- プロキシのカスタム出力ライブラリ名で更新する</span><span class="sxs-lookup"><span data-stu-id="f4723-166"><AssemblyName> - Update it with your custom output library name for the proxy</span></span>

    <span data-ttu-id="f4723-167"><RetailServerExtensionLibraryNoPrefixForRetailProxyCSharpExtensionGeneration>- Retail サーバー拡張子ライブラリ名で更新します。</span><span class="sxs-lookup"><span data-stu-id="f4723-167"><RetailServerExtensionLibraryNoPrefixForRetailProxyCSharpExtensionGeneration> - Update it with your retail server extension library name.</span></span>

    <span data-ttu-id="f4723-168">**注記:** プロキシは、このライブラリ名に基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="f4723-168">**Note:** Proxy is generated based on this library name.</span></span>

6.  <span data-ttu-id="f4723-169">csproj ファイルを保存し、プロジェクトを再度読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f4723-169">Save the csproj file and load the project again.</span></span>

7.  <span data-ttu-id="f4723-170">拡張パターンに従って、プロジェクトの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="f4723-170">Rename the project according to your extension pattern.</span></span>

8.  <span data-ttu-id="f4723-171">プロジェクトが読み込まれたら、アダプタ フォルダから StoreDayHoursManager.cs ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="f4723-171">Once the project is loaded, delete the StoreDayHoursManager.cs file from the Adapters folder.</span></span>

9.  <span data-ttu-id="f4723-172">プロジェクト参照としてすべての関連する CRT ライブラリを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4723-172">Add all the relevant CRT library as project reference.</span></span> <span data-ttu-id="f4723-173">(Retail サーバーの拡張機能で参照または使用される CRT ライブラリ)</span><span class="sxs-lookup"><span data-stu-id="f4723-173">(CRT libraries referred or used by your retail server extension)</span></span>

10. <span data-ttu-id="f4723-174">プロジェクトをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="f4723-174">Rebuild the project.</span></span>

    <span data-ttu-id="f4723-175">注記: プロキシ プロジェクトを作成する前に、すべての CRT および Retail サーバー拡張ライブラリを再構築して、RetailSDK\\References フォルダーにドロップしてください。</span><span class="sxs-lookup"><span data-stu-id="f4723-175">Note: Before building the proxy project, please rebuild all our CRT and Retail server extensions libraries and drop it in RetailSDK\\References folder.</span></span>

11. <span data-ttu-id="f4723-176">アダプタ フォルダーに新しいクラス ファイルを追加し、拡張機能のパターンに従って名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="f4723-176">Add a new class file under Adapters folder and name it according to your extension pattern.</span></span>

12. <span data-ttu-id="f4723-177">前の手順で追加した CRT エンティティと新しいクラスで使用される名前空間が同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4723-177">Please make sure the namespace used in the CRT entity and the new class you added in the previous step is same.</span></span> <span data-ttu-id="f4723-178">(参照用に営業時間のサンプル プロキシと営業時間 CRT サンプル プロジェクトを確認する)</span><span class="sxs-lookup"><span data-stu-id="f4723-178">(Check the store hours sample proxy and store hours CRT sample project for reference)</span></span>

13. <span data-ttu-id="f4723-179">インターフェイス マネージャーからクラスを拡張およびインターフェイス メソッドを実装します。必要なインターフェイス メソッドのみがそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="f4723-179">Extend the class from the interface manager and implement the interface methods, only the required ones leave others as is.</span></span>

    <span data-ttu-id="f4723-180">注記: インターフェイス名は、ワード コントローラーなしのコントローラー名に類似したものです。</span><span class="sxs-lookup"><span data-stu-id="f4723-180">Note: The interface name will be something similar to your controller name without the word controlloer.</span></span>

    <span data-ttu-id="f4723-181">フル コード サンプルの RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample for full code sample にある Proxies.RetailProxy.Extensions.StoreHoursSample プロジェクトを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f4723-181">Check the Proxies.RetailProxy.Extensions.StoreHoursSample proj under RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample for full code sample.</span></span>
  
14. <span data-ttu-id="f4723-182">メソッド内で、実際の CRT 要求/応答を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f4723-182">Inside the methods you will call the actual CRT request/response.</span></span> <span data-ttu-id="f4723-183">プロキシ プロジェクトではロジックを回避してください。CRT の要求/応答のみを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4723-183">Please avoid any logic in the proxy project, it should only call the CRT request/response.</span></span>

15. <span data-ttu-id="f4723-184">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="f4723-184">Build the project.</span></span>

16. <span data-ttu-id="f4723-185">出力アセンブリをコピーして、RetailSDK\\References フォルダーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f4723-185">Copy the output assembly and paste in RetailSDK\\References folder.</span></span>

17. <span data-ttu-id="f4723-186">RetailSDK\\Assets フォルダーに移動して RetailProxy.MPOSOffline.ext.config を開く</span><span class="sxs-lookup"><span data-stu-id="f4723-186">Navigate to RetailSDK\\Assets folder and open RetailProxy.MPOSOffline.ext.config</span></span>

18. <span data-ttu-id="f4723-187">合成セクションで、新しいプロキシ ライブラリ名を登録します。</span><span class="sxs-lookup"><span data-stu-id="f4723-187">Under the composition section, register your new proxy library name.</span></span> <span data-ttu-id="f4723-188">(プロキシ プロジェクトの作成後に生成されるアセンブリです。</span><span class="sxs-lookup"><span data-stu-id="f4723-188">(The assembly generated after building your proxy project.</span></span>

    <span data-ttu-id="f4723-189">前: <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" /></span><span class="sxs-lookup"><span data-stu-id="f4723-189">Ex: <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" /></span></span>

    <span data-ttu-id="f4723-190">**注記:** 値フィールドには、プロキシ ライブラリの名前を追加します (Contoso.Commerce.RetailProxy.StoreHoursSample など)。</span><span class="sxs-lookup"><span data-stu-id="f4723-190">**Note:** In the value field you will add your proxy library name, in the example we used       Contoso.Commerce.RetailProxy.StoreHoursSample</span></span>

19. <span data-ttu-id="f4723-191">手動テストでは、構成セクションでカスタム プロキシ ライブラリ名を持つ、C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext で、RetailProxy.MPOSOffline.ext.config を更新します。</span><span class="sxs-lookup"><span data-stu-id="f4723-191">For manual testing, update the RetailProxy.MPOSOffline.ext.config under the C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext with the custom proxy library name under the composition section.</span></span>

    <span data-ttu-id="f4723-192">前: <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" /></span><span class="sxs-lookup"><span data-stu-id="f4723-192">Ex: <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" /></span></span>

<span data-ttu-id="f4723-193">**注記:** 電子商取引の場合は、電子商取引プロジェクトから呼び出す前に、拡張機能のプロキシを初期化するためのもう 1 つの追加手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4723-193">**Note:** In case of e-commerce, you must perform one more additional step to initialize the proxy for the extensions before calling it from your e-commerce project:</span></span>

1. <span data-ttu-id="f4723-194">E コマース Startup.cs (または Web プロジェクトの初期化などの同等のもの) では、Retail プロキシの拡張機能の edm モデルで RetailServerContext を初期化する必要があり、そうせずにプロキシを呼び出そうとした場合、ランタイム エラーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f4723-194">In your e-commerce Startup.cs (or their equivalent like web project initialization etc.) you must initialize the RetailServerContext with the edm model for your retail proxy extension or else you will get runtime error if you try to call the proxy.</span></span> <span data-ttu-id="f4723-195">RetailServerContext を初期化するために、1 回のみこれを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4723-195">You need to do this only once to initialize the RetailServerContext.</span></span>
             
<span data-ttu-id="f4723-196">前:</span><span class="sxs-lookup"><span data-stu-id="f4723-196">Ex:</span></span>
```C#
  RetailServerContext.Initialize(newIEdmModelExtension[]
                {
                   // /* BEGIN SDKSAMPLE_STOREHOURS
 
                   new Contoso.Commerce.RetailProxy.StoreHoursSample.EdmModel(),
 
                    // END SDKSAMPLE_STOREHOURS */
                });
```

