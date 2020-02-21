---
title: Typescript および小売販売時点管理 (POS) の C# プロキシ
description: このトピックでは、コマース プロキシに関する情報と、その生成方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 957dfb330e25c1a0a119c4bf42e1e5fa25095b05
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004623"
---
# <a name="typescript-and-c-proxies-for-retail-point-of-sale-pos"></a><span data-ttu-id="e8043-103">Typescript および小売販売時点管理 (POS) の C# プロキシ</span><span class="sxs-lookup"><span data-stu-id="e8043-103">Typescript and C# proxies for Retail point of sale (POS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8043-104">Commerce Scale Unit アプリケーション プログラミング インターフェイス (API) の新しいコントローラーを作成するたびに、または既存のコントローラーを拡張するたびに、Retail ソフトウェアの開発キット (SDK) の一部として提供されているツールを使用して、Commerce プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-104">When you create a new controller for Commerce Scale Unit application programming interfaces (APIs) or extend the existing controller, you must generate the Commerce proxy by using the tools that are available as part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="e8043-105">たとえば、顧客コントローラーを拡張することにより、顧客エンティティの新しい API を追加する場合、コマース プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-105">For example, you must generate the Commerce proxy if you add a new API for the Customer entity by extending the Customer controller.</span></span>

## <a name="what-is-the-commerce-proxy-used-for-and-when-should-you-use-it"></a><span data-ttu-id="e8043-106">コマース プロキシは何に使用され、いつ使用するか?</span><span class="sxs-lookup"><span data-stu-id="e8043-106">What is the Commerce proxy used for and when should you use it?</span></span>

<span data-ttu-id="e8043-107">すべてのクライアントは Commerce Scale Unit とやりとりするためにプロキシ API を使用します。</span><span class="sxs-lookup"><span data-stu-id="e8043-107">All the clients use the proxy API to interact with Commerce Scale Unit.</span></span> <span data-ttu-id="e8043-108">コマース プロキシは、Commerce Scale Unit と Commerce Runtime (CRT) 間のインターフェイスを抽象化します。</span><span class="sxs-lookup"><span data-stu-id="e8043-108">The Commerce proxy abstracts the interface between Commerce Scale Unit and the Commerce runtime (CRT).</span></span> <span data-ttu-id="e8043-109">たとえば、CRT で要求/応答の操作として新しいエンティティとビジネス ロジックを作成し、そのエンティティおよびそれらの要求/応答の操作を公開するために、新しい Commerce Scale Unit API を追加できます。</span><span class="sxs-lookup"><span data-stu-id="e8043-109">For example, you create a new entity and some business logic as request/response operations in CRT, and you add a new Commerce Scale Unit API to expose that entity and those request/response operations.</span></span> <span data-ttu-id="e8043-110">販売時点管理 (POS) におけるエンティティと要求/応答動作にアクセスして、あるクライアント ロジックを実行する必要が出てきました。</span><span class="sxs-lookup"><span data-stu-id="e8043-110">You now want to access the entity and the request/response operations in the point of sale (POS) to do some client logic.</span></span> <span data-ttu-id="e8043-111">POS ですべてのエンティティと要求/応答メタデータを手動で作成し、適切なパラメーターを使用して Commerce Scale Unit にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="e8043-111">You can manually create all the entities and request/response metadata in the POS, and access the Commerce Scale Unit by using the correct parameters.</span></span> <span data-ttu-id="e8043-112">ただし、エンティティ、マネージャ、および 2 つの場所で要求/応答コードを複製する必要があり、および多くのコードの書き込みもする必要があるため、このアプローチには追加の間接費が多く含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8043-112">However, this approach involves lots of additional overhead, because you must duplicate the entities, manager, and request/response code in two places, and you must also write lots of code.</span></span>

<span data-ttu-id="e8043-113">コマース プロキシは、Commerce Scale Unit に追加されたすべてのカスタム エンティティと要求/応答操作のプロキシを自動的に作成することによって、この労力を軽減します。</span><span class="sxs-lookup"><span data-stu-id="e8043-113">The Commerce proxy reduces this effort by automatically generating the proxy for all the custom entities and request/response operations that are added in Commerce Scale Unit.</span></span> <span data-ttu-id="e8043-114">プロキシ ツールは、必須のインターフェイスとすべての必須メタデータを生成し、実際の実装を抽象化します。</span><span class="sxs-lookup"><span data-stu-id="e8043-114">The proxy tool generates the required interface and all the required metadata, and abstracts the actual implementation.</span></span> <span data-ttu-id="e8043-115">この方法では、拡張プロジェクトにファイルを含めることができ、生成されたメタデータとインターフェイスを使用して Commerce Scale Unit API とエンティティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e8043-115">In that way, you can include the files in the extension projects, and can access the Commerce Scale Unit APIs and the entities by using the metadata and interface that are generated.</span></span>

## <a name="proxy-types"></a><span data-ttu-id="e8043-116">プロキシのタイプ</span><span class="sxs-lookup"><span data-stu-id="e8043-116">Proxy types</span></span>

<span data-ttu-id="e8043-117">クロス プラットフォーム シナリオをサポートするプロキシのタイプには 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="e8043-117">There two types of proxy to support cross-platform scenarios:</span></span>

- <span data-ttu-id="e8043-118">**Typescript プロキシ** – POS は、Typescript プロキシを使用して Commerce Scale Unit API および CRT エンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e8043-118">**Typescript proxy** – The POS uses the Typescript proxy to access the Commerce Scale Unit APIs and CRT entities.</span></span> <span data-ttu-id="e8043-119">POS が Commerce Scale Unit を使用する場合は、Typescript プロキシが必要です。</span><span class="sxs-lookup"><span data-stu-id="e8043-119">If the POS uses Commerce Scale Unit, it requires the Typescript proxy.</span></span> <span data-ttu-id="e8043-120">でなければ、POS はオペレーションまたはワークフローのために Commerce Scale Unit と通信することができません。</span><span class="sxs-lookup"><span data-stu-id="e8043-120">Otherwise, the POS can't communicate with the Commerce Scale Unit for any operations or workflows.</span></span>
- <span data-ttu-id="e8043-121">**C# プロキシ** - POS はオフラインのときに C# プロキシを使用します。</span><span class="sxs-lookup"><span data-stu-id="e8043-121">**C# proxy** – The POS uses the C# proxy when it's offline.</span></span> <span data-ttu-id="e8043-122">(POS がオフラインの場合、Commerce Scale Unit を使用せずに CRT と直接通信します)。POS は、Dynamics 電子商取引プラットフォームにもこのプロキシを使用します。</span><span class="sxs-lookup"><span data-stu-id="e8043-122">(When the POS is offline, it communicates directly with CRT, without using Commerce Scale Unit.) The POS also uses this proxy for the Dynamics e-Commerce platform.</span></span> <span data-ttu-id="e8043-123">POS がオフラインのときにカスタマイズを動作させ、電子商取引クライアントが Commerce Scale Unit API にアクセスできるようにするには、C# プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-123">If you want your customization to work when the POS is offline, and you want your e-Commerce client to access the Commerce Scale Unit APIs, you must generate the C# proxy.</span></span>

<span data-ttu-id="e8043-124">Typescript プロキシを生成する手順と C# プロキシを生成する手順は異なります。</span><span class="sxs-lookup"><span data-stu-id="e8043-124">The steps to generate the Typescript proxy and the C# proxy differ.</span></span> <span data-ttu-id="e8043-125">このトピックの後半では、各タイプのプロキシを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8043-125">The rest of this topic explains how to generate each type of proxy.</span></span>

## <a name="generate-the-typescript-proxy"></a><span data-ttu-id="e8043-126">Typescript プロキシを生成します</span><span class="sxs-lookup"><span data-stu-id="e8043-126">Generate the Typescript proxy</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8043-127">次の手順は Microsoft Microsoft Dynamics 365 Retail (2017 年 7 月リリース) および Microsoft Dynamics 365 Finance にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e8043-127">The following procedure applies only to Microsoft Dynamics 365 Retail (July 2017 release) and Microsoft Dynamics 365 Finance.</span></span>

<span data-ttu-id="e8043-128">Retail SDK\\Reference\\CommerceProxyGenerator.<version_number> フォルダーの CommerceProxyGenerator.exe ファイルを使用して、タイプスクリプト プロキシを生成します。</span><span class="sxs-lookup"><span data-stu-id="e8043-128">Use the CommerceProxyGenerator.exe file from the Retail SDK\\Reference\\CommerceProxyGenerator.<version_number> folder to generate the typescript proxy for the POS.</span></span>

1. <span data-ttu-id="e8043-129">プロキシを生成する前に、カスタマイズした Commerce Scale Unit、CRT、およびその他の依存ライブラリを、**Retail SDK\\Reference** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e8043-129">Before you generate the proxy, copy the customized Commerce Scale Unit, CRT, and other dependent libraries to the **Retail SDK\\Reference** folder.</span></span>
2. <span data-ttu-id="e8043-130">管理者モードでコマンド プロンプトを開き、**...\\Retail SDK\\参照** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="e8043-130">Open a Command Prompt window as an administrator, and go to the **...\\Retail SDK\\Reference** folder.</span></span> <span data-ttu-id="e8043-131">次のコマンドを実行してプロキシを生成します。</span><span class="sxs-lookup"><span data-stu-id="e8043-131">Run the following command to generate the proxy.</span></span> <span data-ttu-id="e8043-132">プロキシ ファイルは同じフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="e8043-132">The proxy files will be generated in the same folder.</span></span>


```
CommerceProxyGenerator.exe <Path>\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptextensions

```

> [!NOTE]
> <span data-ttu-id="e8043-133">次の場所から Microsoft.Dynamics.Retail.RetailServerLibrary.dll ファイルを使用します: \RetailSDK\References\Microsoft.Dynamics.Retail.Proxies.ExtensionsGenerator.<version_number>\build</span><span class="sxs-lookup"><span data-stu-id="e8043-133">Use the Microsoft.Dynamics.Retail.RetailServerLibrary.dll file from \RetailSDK\References\Microsoft.Dynamics.Retail.Proxies.ExtensionsGenerator.<version_number>\build</span></span>\

``` 
Ex:
CommerceProxyGenerator.exe C:\\RetailSDK\\References\\Microsoft.Dynamics.Retail.Proxies.ExtensionsGenerator.9.18.19299.3\\build\Microsoft.Dynamics.Retail.RetailServerLibrary.dll C:\\RetailSDK\\References\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll /a:typescriptextensions
```
<span data-ttu-id="e8043-134">実行するコマンドで、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** をカスタム Commerce Scale Unit 拡張ライブラリの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e8043-134">In the above command, replace **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** with the name of your custom Commerce Scale Unit extension library.</span></span> <span data-ttu-id="e8043-135">POS プロジェクトに生成されたファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="e8043-135">Include the generated files in your POS project.</span></span> <span data-ttu-id="e8043-136">このコマンドは、拡張ライブラリに基づいた 2 つのファイル、DataServiceEntities.g.ts と DataServiceRequests.g.tss を生成します。</span><span class="sxs-lookup"><span data-stu-id="e8043-136">The command generates two files that are based on your extension libraries: DataServiceEntities.g.ts and DataServiceRequests.g.ts.</span></span>

> [!NOTE]
> <span data-ttu-id="e8043-137">すべての Commerce Scale Unit 拡張機能のプロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-137">You must generate the proxy for all Commerce Scale Unit extensions.</span></span>

## <a name="generate-the-c-proxy-71-and-72"></a><span data-ttu-id="e8043-138">C# プロキシ (7.1 および 7.2) の生成</span><span class="sxs-lookup"><span data-stu-id="e8043-138">Generate the C# proxy (7.1 and 7.2)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8043-139">7.3 以降のバージョンには、次の手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="e8043-139">The following procedure doesn't apply to version 7.3 and later.</span></span>

1. <span data-ttu-id="e8043-140">**Customization.settings** ファイルを **...Retail SDK\\BuildTools** から開きます。</span><span class="sxs-lookup"><span data-stu-id="e8043-140">Open the **Customization.settings** file from **...Retail SDK\\BuildTools**.</span></span>
2. <span data-ttu-id="e8043-141">**RetailServerLibraryPathForProxyGeneration** ノードの下には、次に示すように、すべてのカスタム Retail サーバー拡張ライブラリを含めます。</span><span class="sxs-lookup"><span data-stu-id="e8043-141">Under the **RetailServerLibraryPathForProxyGeneration** node, include all your custom Retail Server extension libraries, as shown here.</span></span>

    ```
    <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll"/>;
    ```

    <span data-ttu-id="e8043-142">この例では、カスタム ライブラリは **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** の 1 つだけあります。</span><span class="sxs-lookup"><span data-stu-id="e8043-142">In this example, there is just one custom library, **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll**.</span></span> <span data-ttu-id="e8043-143">ただし、カスタム Retail サーバー拡張ライブラリが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="e8043-143">However, be sure to include all your custom Retail Server extension libraries.</span></span>

3. <span data-ttu-id="e8043-144">**RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開きます。</span><span class="sxs-lookup"><span data-stu-id="e8043-144">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**.</span></span>
4. <span data-ttu-id="e8043-145">カスタム CRT プロジェクト ライブラリを **Proxies.RetailProxy.csproj** への参照として含めます。</span><span class="sxs-lookup"><span data-stu-id="e8043-145">Include your custom CRT project library as a reference to **Proxies.RetailProxy.csproj**.</span></span>
5. <span data-ttu-id="e8043-146">ソリューションの **RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions.txt** を開きます。</span><span class="sxs-lookup"><span data-stu-id="e8043-146">Open **RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions.txt** in the solution.</span></span>
6. <span data-ttu-id="e8043-147">**UsingStatements.Extensions.txt** で、CRT エンティティの名前空間および要求/応答の名前空間の **using** ステートメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="e8043-147">In **UsingStatements.Extensions.txt**, add the **using** statement for your CRT entity namespace and request/response namespace.</span></span> <span data-ttu-id="e8043-148">たとえば、CRT 拡張機能で **Contoso.Commerce.Runtime.DataModel** 名前空間を使用する場合、ここに示すように、追加プロキシを生成するため **UsingStatements.Extensions.txt** にその名前空間を追加します。</span><span class="sxs-lookup"><span data-stu-id="e8043-148">For example, if you use the **Contoso.Commerce.Runtime.DataModel** namespace in your CRT extension, add that namespace in **UsingStatements.Extensions.txt** to generate the proxy, as shown here.</span></span>

    ```
    using Contoso.Commerce.Runtime.DataModel;
    ```

7. <span data-ttu-id="e8043-149">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="e8043-149">Build the project.</span></span>
8. <span data-ttu-id="e8043-150">**アダプタ** フォルダの新しいクラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="e8043-150">Add a new class under the **Adapters** folder.</span></span> <span data-ttu-id="e8043-151">アダプター フォルダーの他のマネージャー クラスをテンプレートとして使用すると、名前空間全体が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8043-151">Use any other manager class from the adapter folder as a template, so that the whole namespace is included.</span></span>
9. <span data-ttu-id="e8043-152">インターフェイス マネージャーからクラスを拡張し、必要なインターフェイス メソッドのみを実装します。</span><span class="sxs-lookup"><span data-stu-id="e8043-152">Extend the class from the interface manager, and implement only the required interface methods.</span></span>
  
    <span data-ttu-id="e8043-153">インターフェイス クラスとマネージャ クラスの生成方法については、Retail SDK の Store Hours サンプルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8043-153">To learn how generate the interface and manager classes, see the Store Hours sample in the Retail SDK.</span></span> <span data-ttu-id="e8043-154">指示は、**RetailSDK\\Code\\Documents\\SampleExtensionsInstructions\\StoreHours\\readme.txt** ファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="e8043-154">The instructions are in the **RetailSDK\\Code\\Documents\\SampleExtensionsInstructions\\StoreHours\\readme.txt** file.</span></span>

## <a name="generate-the-c-proxy-73"></a><span data-ttu-id="e8043-155">C# プロキシ (7.3) の生成</span><span class="sxs-lookup"><span data-stu-id="e8043-155">Generate the C# proxy (7.3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8043-156">次の手順は、POS と電子商取引の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e8043-156">The following procedure applies to both the POS and e-Commerce.</span></span>

<span data-ttu-id="e8043-157">Retail サーバー拡張機能ごとに、別個のプロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-157">For each Retail Server extension, you must generate a separate proxy.</span></span>

1. <span data-ttu-id="e8043-158">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8043-158">Navigate to **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample**.</span></span>
2. <span data-ttu-id="e8043-159">Microsoft Visual Studio で、**Proxies.RetailProxy.Extensions.StoreHoursSample** プロジェクト ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="e8043-159">In Microsoft Visual Studio, open the **Proxies.RetailProxy.Extensions.StoreHoursSample** project file.</span></span>
3. <span data-ttu-id="e8043-160">右クリックし、プロジェクトのアンロードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8043-160">Right-click, and select to unload the project.</span></span>
4. <span data-ttu-id="e8043-161">プロジェクトを右クリックし、**Proxies.RetailProxy.Extensions.StoreHoursSample.csproj** を選択して編集します。</span><span class="sxs-lookup"><span data-stu-id="e8043-161">Right-click the project, and select to edit the **Proxies.RetailProxy.Extensions.StoreHoursSample.csproj** file.</span></span>
5. <span data-ttu-id="e8043-162">最初のプロパティ グループ セクションで、次のノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="e8043-162">In the first property group section, update the following nodes:</span></span>

    - <span data-ttu-id="e8043-163">**&lt;RootNamespace&gt;** – ユーザー設定の名前空間を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8043-163">**&lt;RootNamespace&gt;** – Specify your custom namespace.</span></span>
    - <span data-ttu-id="e8043-164">**&lt;AssemblyName&gt;** – プロキシのカスタム出力ライブラリ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8043-164">**&lt;AssemblyName&gt;** – Specify your custom output library name for the proxy.</span></span>

6. <span data-ttu-id="e8043-165">Retail サーバーの拡張機能ライブラリ名を指定して、**CommerceProxyGeneratorExtendedAssemblyPaths** 要素を更新します。</span><span class="sxs-lookup"><span data-stu-id="e8043-165">Update the **CommerceProxyGeneratorExtendedAssemblyPaths** element by specifying the name of your Retail Server extension library.</span></span>

    <span data-ttu-id="e8043-166">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e8043-166">Here is an example.</span></span>

    ```
    <CommerceProxyGeneratorExtendedAssemblyPaths Include="..\..\RetailServer\Extensions.StoreHoursSample\bin\$(Configuration)\net451\$(AssemblyNamePrefix).RetailServer.StoreHoursSample.dll" />
    ```

    > [!NOTE]
    > <span data-ttu-id="e8043-167">**.RetailServer.StoreHoursSample.dll** は、Retail サーバー拡張アセンブリの名前です。残りの値は、接頭語 (接頭語がある場合) と、プロキシ エンジンがこのアセンブリを見つけることができるアセンブリのパスです。</span><span class="sxs-lookup"><span data-stu-id="e8043-167">**.RetailServer.StoreHoursSample.dll** is the name of the Retail Server extension assembly, and the rest of the value is the prefix (if there is a prefix) and the path of the assembly where the proxy engine can find this assembly.</span></span> <span data-ttu-id="e8043-168">プロキシは、このアセンブリに基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="e8043-168">The proxy is generated based on this assembly.</span></span>

7. <span data-ttu-id="e8043-169">ファイルを保存し、プロジェクトを再度読み込みます。</span><span class="sxs-lookup"><span data-stu-id="e8043-169">Save the file, and load the project again.</span></span>
8. <span data-ttu-id="e8043-170">拡張パターンに従って、プロジェクトの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="e8043-170">Rename the project according to your extension pattern.</span></span>
9. <span data-ttu-id="e8043-171">プロジェクトが読み込まれた後、**アダプタ** フォルダから **StoreDayHoursManager.cs** ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="e8043-171">After the project is loaded, delete the **StoreDayHoursManager.cs** file from the **Adapters** folder.</span></span>
10. <span data-ttu-id="e8043-172">すべての関連する CRT と Retail サーバー ライブラリをプロジェクトまたはアセンブリ参照としてプロキシ プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="e8043-172">Add all the relevant CRT and Retail Server libraries to the proxy project as project or assembly references.</span></span>
11. <span data-ttu-id="e8043-173">プロジェクトをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="e8043-173">Rebuild the project.</span></span>

    <span data-ttu-id="e8043-174">アダプタ フォルダー内で新しい Interfaces.g.cs ファイルが生成されると表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8043-174">You will see that a new Interfaces.g.cs file is generated inside the Adapters folder.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8043-175">プロキシ プロジェクトを作成する前に、すべての CRT および Retail サーバー拡張ライブラリを再構築して、**RetailSDK\\References** フォルダーにドロップしてください。</span><span class="sxs-lookup"><span data-stu-id="e8043-175">Before you build the proxy project, rebuild all your CRT and Retail Server extension libraries, and drop them into the **RetailSDK\\References** folder.</span></span>

12. <span data-ttu-id="e8043-176">プロキシ プロジェクト内に新しい **Interfaces.g.cs** ファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="e8043-176">Include the new **Interfaces.g.cs** file in the proxy project.</span></span> <span data-ttu-id="e8043-177">ただし、このファイルを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="e8043-177">However, don't modify this file.</span></span>
13. <span data-ttu-id="e8043-178">**アダプタ** フォルダーで、新しいクラス ファイルを追加し、拡張機能のパターンに従って名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="e8043-178">Under the **Adapters** folder, add a new class file, and name it according to your extension pattern.</span></span>
14. <span data-ttu-id="e8043-179">インターフェイス マネージャー クラスからクラスを拡張し、必要なインターフェイス メソッドのみを実装します。</span><span class="sxs-lookup"><span data-stu-id="e8043-179">Extend the class from the interface manager class, and implement only the interface methods that are required.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8043-180">Interfaces.g.cs ファイルで、インターフェイス マネージャー クラスの名前を見つけることが</span><span class="sxs-lookup"><span data-stu-id="e8043-180">You can find the name of the interface manager class in the Interfaces.g.cs.</span></span> <span data-ttu-id="e8043-181">できます。</span><span class="sxs-lookup"><span data-stu-id="e8043-181">file.</span></span>

    <span data-ttu-id="e8043-182">次の例では、**IStoreDayHoursManager** はインターフェイスの名前です。</span><span class="sxs-lookup"><span data-stu-id="e8043-182">In the following example, **IStoreDayHoursManager** is the name of the interface.</span></span>

    ```C#
    public interface IStoreDayHoursManager : Microsoft.Dynamics.Commerce.RetailProxy.IEntityManager
    {
    }
    ```

    <span data-ttu-id="e8043-183">フル サンプル コードについては、**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample** にある **Proxies.RetailProxy.Extensions.StoreHoursSample** プロジェクトをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e8043-183">For the full sample code, see the **Proxies.RetailProxy.Extensions.StoreHoursSample** project under **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample**.</span></span>

15. <span data-ttu-id="e8043-184">メソッド内で、実際の CRT 要求/応答を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e8043-184">Inside the methods you will call the actual CRT request/response.</span></span> <span data-ttu-id="e8043-185">プロキシ プロジェクトに任意のロジックを含めないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="e8043-185">Avoid including any logic in the proxy project.</span></span> <span data-ttu-id="e8043-186">プロキシ プロジェクトは、CRT 要求/応答だけを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-186">The proxy project should just call the CRT request/response.</span></span>
16. <span data-ttu-id="e8043-187">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="e8043-187">Build the project.</span></span>
17. <span data-ttu-id="e8043-188">出力アセンブリをコピーして、**RetailSDK\\References** フォルダーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="e8043-188">Copy the output assembly, and paste it in the **RetailSDK\\References** folder.</span></span>
18. <span data-ttu-id="e8043-189">**RetailSDK\\Assets** フォルダーに移動して **RetailProxy.MPOSOffline.ext.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="e8043-189">Navigate to the **RetailSDK\\Assets** folder, and open the **RetailProxy.MPOSOffline.ext.config** file.</span></span>
19. <span data-ttu-id="e8043-190">**合成** セクションで、新しいプロキシ ライブラリ (つまり、プロキシ プロジェクトをビルドした後に生成されたアセンブリ) の名前を登録します。</span><span class="sxs-lookup"><span data-stu-id="e8043-190">In the **composition** section, register the name of your new proxy library (that is, the assembly that was generated after you built your proxy project).</span></span>

    <span data-ttu-id="e8043-191">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e8043-191">Here is an example.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />
    ```

    <span data-ttu-id="e8043-192">この例では、プロキシ ライブラリ名は **Contoso.Commerce.RetailProxy.StoreHoursSample** です。</span><span class="sxs-lookup"><span data-stu-id="e8043-192">In this example, the proxy library is named **Contoso.Commerce.RetailProxy.StoreHoursSample**.</span></span> <span data-ttu-id="e8043-193">プロキシ ライブラリの名前は、**値** フィールドで指定してください。</span><span class="sxs-lookup"><span data-stu-id="e8043-193">You should specify the name of your proxy library in the **value** field.</span></span>

20. <span data-ttu-id="e8043-194">手動テストでは、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** にある **RetailProxy.MPOSOffline.ext.config** ファイルを開きます。カスタム プロキシ ライブラリの名前で **合成** セクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="e8043-194">For manual testing, open the **RetailProxy.MPOSOffline.ext.config** file under **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext**. Update the **composition** section with the name of the custom proxy library.</span></span>

    <span data-ttu-id="e8043-195">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e8043-195">Here is an example.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />
    ```

21. <span data-ttu-id="e8043-196">電子商取引の場合、電子商取引プロジェクトから呼び出しする前に、拡張のプロキシを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-196">For e-Commerce, you must initialize the proxy for the extensions before you call it from your e-Commerce project.</span></span> <span data-ttu-id="e8043-197">電子商取引の **Startup.cs** ファイル (または、Web プロジェクトの初期化などの同等のファイル) で、Retail プロキシ拡張の拡張データ モデル (EDM) を使用して **RetailServerContext** を初期化します。</span><span class="sxs-lookup"><span data-stu-id="e8043-197">In your e-Commerce **Startup.cs** file (or an equivalent, such as web project initialization), initialize **RetailServerContext** with the Extended data model(EDM) model for your Retail proxy extension.</span></span> <span data-ttu-id="e8043-198">それ以外の場合、プロキシのを呼び出そうとすると、ランタイム エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8043-198">Otherwise, you will receive a runtime error when you try to call the proxy.</span></span> <span data-ttu-id="e8043-199">このステップは 1 回のみ完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8043-199">You must complete this step only one time.</span></span>

    <span data-ttu-id="e8043-200">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e8043-200">Here is an example.</span></span>

    ```C#
    RetailServerContext.Initialize(newIEdmModelExtension[]
    {
        // /* BEGIN SDKSAMPLE_STOREHOURS
        new Contoso.Commerce.RetailProxy.StoreHoursSample.EdmModel(),
        // END SDKSAMPLE_STOREHOURS */
    });
    ```
