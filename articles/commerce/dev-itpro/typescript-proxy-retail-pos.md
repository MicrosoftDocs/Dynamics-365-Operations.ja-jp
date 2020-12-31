---
title: Typescript および小売販売時点管理 (POS) の C# プロキシ
description: このトピックでは、コマース プロキシに関する情報と、その生成方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-20
ms.dyn365.ops.version: AX 7.0.0, Retail October 2017 update
ms.openlocfilehash: 0870f7cb7cc672338bb07e7b72c60090300422ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680376"
---
# <a name="typescript-and-c-proxies-for-retail-point-of-sale-pos"></a><span data-ttu-id="42329-103">Typescript および小売販売時点管理 (POS) の C# プロキシ</span><span class="sxs-lookup"><span data-stu-id="42329-103">Typescript and C# proxies for Retail point of sale (POS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42329-104">新しい小売サーバー API を作成する場合は、Retail ソフトウェア開発キット (SDK) の一部として使用できるツールを使用して、Commerce プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42329-104">When you create a new Retail Server API, you must generate the Commerce proxy by using the tools that are available as part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="42329-105">たとえば、新しい Retail サーバー API を追加する場合は、Commerce プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42329-105">For example, you must generate the Commerce proxy if you add a new Retail Server API.</span></span>

## <a name="the-commerce-proxy-and-when-to-use-it"></a><span data-ttu-id="42329-106">Commerce プロキシとそれを使用する場合</span><span class="sxs-lookup"><span data-stu-id="42329-106">The Commerce proxy and when to use it</span></span>

<span data-ttu-id="42329-107">すべてのクライアントは Retail Serve とやりとりするためにプロキシ API を使用します。</span><span class="sxs-lookup"><span data-stu-id="42329-107">All clients use the proxy API to interact with Retail Server.</span></span> <span data-ttu-id="42329-108">Commerce プロキシは、Retail Server と Commerce Runtime (CRT) 間のインターフェイスを抽象化します。</span><span class="sxs-lookup"><span data-stu-id="42329-108">The Commerce proxy abstracts the interface between Retail Server and the Commerce runtime (CRT).</span></span> <span data-ttu-id="42329-109">たとえば、CRT で要求/応答の操作として新しいエンティティとビジネス ロジックを作成し、そのエンティティおよびそれらの要求/応答の操作を公開するために、新しい Retail サーバー API を追加できます。</span><span class="sxs-lookup"><span data-stu-id="42329-109">For example, you create a new entity and some business logic as request/response operations in CRT, and you add a new Retail Server API to expose that entity and those request/response operations.</span></span> <span data-ttu-id="42329-110">販売時点管理 (POS) におけるエンティティと要求/応答動作にアクセスして、あるクライアント ロジックを実行する必要が出てきました。</span><span class="sxs-lookup"><span data-stu-id="42329-110">You now want to access the entity and the request/response operations in the point of sale (POS) to do some client logic.</span></span> <span data-ttu-id="42329-111">POS ですべてのエンティティと要求/応答メタデータを手動で作成し、適切なパラメーターを使用して Retail サーバー API にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="42329-111">You can manually create all the entities and request/response metadata in the POS, and access the Retail Server API by using the correct parameters.</span></span> <span data-ttu-id="42329-112">ただし、エンティティ、マネージャ、および 2 つの場所で要求/応答コードを複製する必要があり、および多くのコードの書き込みもする必要があるため、このアプローチには追加の間接費が多く含まれます。</span><span class="sxs-lookup"><span data-stu-id="42329-112">However, this approach involves lots of additional overhead, because you must duplicate the entities, manager, and request/response code in two places, and you must also write lots of code.</span></span>

<span data-ttu-id="42329-113">Commerce プロキシは、Retail Server に追加されたすべてのユーザー定義エンティティと要求/応答操作のプロキシを自動的に作成することによって、この労力を軽減します。</span><span class="sxs-lookup"><span data-stu-id="42329-113">The Commerce proxy reduces this effort by automatically generating the proxy for all the custom entities and request/response operations that are added in Retail Server.</span></span> <span data-ttu-id="42329-114">プロキシ ツールは、必須のインターフェイスとすべての必須メタデータを生成し、実際の実装を抽象化します。</span><span class="sxs-lookup"><span data-stu-id="42329-114">The proxy tool generates the required interface and all the required metadata, and abstracts the actual implementation.</span></span> <span data-ttu-id="42329-115">この方法では、拡張プロジェクトにファイルを含めることができ、生成されたメタデータとインターフェイスを使用して Retail サーバー API とエンティティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="42329-115">In that way, you can include the files in the extension projects, and can access the Retail Server APIs and the entities by using the metadata and interface that are generated.</span></span>

## <a name="proxy-types"></a><span data-ttu-id="42329-116">プロキシのタイプ</span><span class="sxs-lookup"><span data-stu-id="42329-116">Proxy types</span></span>

<span data-ttu-id="42329-117">クロス プラットフォーム シナリオをサポートするプロキシのタイプには 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="42329-117">There two types of proxy to support cross-platform scenarios:</span></span>

- <span data-ttu-id="42329-118">**Typescript プロキシ** – POS は、Typescript プロキシを使用して Retail サーバー API および CRT エンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="42329-118">**Typescript proxy** – The POS uses the Typescript proxy to access the Retail Server APIs and CRT entities.</span></span> <span data-ttu-id="42329-119">POS が Retail サーバーを使用する場合は、Typescript プロキシが必要です。</span><span class="sxs-lookup"><span data-stu-id="42329-119">If the POS uses Retail Server, it requires the Typescript proxy.</span></span> <span data-ttu-id="42329-120">それ以外の場合、POS はオペレーションまたはワークフローのために Retail サーバーと通信することができません。</span><span class="sxs-lookup"><span data-stu-id="42329-120">Otherwise, the POS can't communicate with the Retail Server for any operations or workflows.</span></span>
- <span data-ttu-id="42329-121">**C# プロキシ** - POS はオフラインのときに C# プロキシを使用します。</span><span class="sxs-lookup"><span data-stu-id="42329-121">**C# proxy** – The POS uses the C# proxy when it's offline.</span></span> <span data-ttu-id="42329-122">(POS がオフラインの場合、Retail サーバーを使用せずに CRT と直接通信します)。POS は、Dynamics 電子商取引プラットフォームにもこのプロキシを使用します。</span><span class="sxs-lookup"><span data-stu-id="42329-122">(When the POS is offline, it communicates directly with CRT, without using Retail Server.) The POS also uses this proxy for the Dynamics e-Commerce platform.</span></span> <span data-ttu-id="42329-123">カスタマイゼーションを POS がオフラインのときに動作させ、電子商取引クライアントを Retail Server API にアクセスするようにするには、C＃ プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42329-123">If you want your customization to work when the POS is offline, and you want your e-Commerce client to access the Retail Server APIs, you must generate the C# proxy.</span></span>

<span data-ttu-id="42329-124">Typescript プロキシを生成する手順と C# プロキシを生成する手順は異なります。</span><span class="sxs-lookup"><span data-stu-id="42329-124">The steps to generate the Typescript proxy and the C# proxy differ.</span></span> <span data-ttu-id="42329-125">このトピックの後半では、各タイプのプロキシを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="42329-125">The rest of this topic explains how to generate each type of proxy.</span></span>

## <a name="generate-the-typescript-proxy-10011-or-lower-retail-server"></a><span data-ttu-id="42329-126">Typescript プロキシ (10.0.11 以前) Retail サーバーの生成</span><span class="sxs-lookup"><span data-stu-id="42329-126">Generate the Typescript proxy (10.0.11 or lower) Retail Server</span></span>

<span data-ttu-id="42329-127">Microsoft Dynamics Commerce バージョン 10.0.12 以降を使用している場合は、[新しい Ratail サーバー拡張機能 API を作成する](retail-server-icontroller-extension.md) で説明している手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="42329-127">If you are using Microsoft Dynamics Commerce version 10.0.12 or greater, follow the steps mentioned in [Create a new Retail Server extension API](retail-server-icontroller-extension.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42329-128">Retail SDK ルート フォルダーから MSBuild を実行して、CommerceProxyGenerator.exe パッケージを復元します。</span><span class="sxs-lookup"><span data-stu-id="42329-128">Run MSBuild from the Retail SDK root folder to restore the CommerceProxyGenerator.exe package.</span></span> <span data-ttu-id="42329-129">Visual Studio の開発者コマンド プロンプト、または MSBuild コマンド プロンプトを使用して、参照フォルダー内のすべてのパッケージを復元してから、プロキシを生成します。</span><span class="sxs-lookup"><span data-stu-id="42329-129">Use the Visual Studio developer command prompt or MSBuild command prompt to restore all the packages in the reference folder before generating the proxy.</span></span> <span data-ttu-id="42329-130">この手順を実行しないと、RetailSDK\Reference フォルダーで CommerceProxyGenerator.exe パッケージを利用できません。</span><span class="sxs-lookup"><span data-stu-id="42329-130">If you do not perform this step, the CommerceProxyGenerator.exe package will not be available in the RetailSDK\Reference folder.</span></span>

<span data-ttu-id="42329-131">Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator.<version_number>\tools フォルダーから CommerceProxyGenerator.exe ファイルを使用して、POS の typescript プロキシを生成します。</span><span class="sxs-lookup"><span data-stu-id="42329-131">Use the CommerceProxyGenerator.exe file from the Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator.<version_number>\tools folder to generate the typescript proxy for the POS.</span></span>

1. <span data-ttu-id="42329-132">プロキシを生成する前に、カスタマイズされた Retail サーバー API、CRT、その他の依存ライブラリを、**Retail SDK\\参照** フォルダーにコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="42329-132">Before you generate the proxy, copy the customized Retail Server API, CRT, and other dependent libraries to the **Retail SDK\\Reference** folder.</span></span>
2. <span data-ttu-id="42329-133">管理者としてコマンド プロンプト ウィンドウを開き、**...\\Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator\<version_number>\tools** フォルダーへ移動します。</span><span class="sxs-lookup"><span data-stu-id="42329-133">Open a Command Prompt window as an administrator, and go to the **...\\Retail SDK\\Reference\\Microsoft.Dynamics.Commerce.Tools.CoreProxyGenerator\<version_number>\tools** folder.</span></span> <span data-ttu-id="42329-134">次のコマンドを実行してプロキシを生成します。</span><span class="sxs-lookup"><span data-stu-id="42329-134">Run the following command to generate the proxy.</span></span> <span data-ttu-id="42329-135">プロキシ ファイルは同じフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="42329-135">The proxy files will be generated in the same folder.</span></span>

  
  <span data-ttu-id="42329-136">POS Typescript プロキシ</span><span class="sxs-lookup"><span data-stu-id="42329-136">POS Typescript proxy</span></span>
```Console 
    CommerceProxyGenerator.exe <Path>\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptextensions
```
 <span data-ttu-id="42329-137">電子商取引の Typescript プロキシ</span><span class="sxs-lookup"><span data-stu-id="42329-137">e-Commerce Typescript proxy</span></span>
 ```Console 
    CommerceProxyGenerator.exe <Path>\Microsoft.Dynamics.Retail.RetailServerLibrary.dll <FilePathNameForRetailServerExtensionDLL> /application:typescriptmoduleextensions
```

> [!NOTE]
> <span data-ttu-id="42329-138">Microsoft.Dynamics.Retail.RetailServerLibrary.dll file from \RetailSDK\References\Microsoft.Dynamics.Commerce.Tools.ExtensionsProxyGenerator.<version_number>\build を使用します。</span><span class="sxs-lookup"><span data-stu-id="42329-138">Use the Microsoft.Dynamics.Retail.RetailServerLibrary.dll file from \RetailSDK\References\Microsoft.Dynamics.Commerce.Tools.ExtensionsProxyGenerator.<version_number>\build.</span></span>

```Console
Example
CommerceProxyGenerator.exe C:\\RetailSDK\\References\\Microsoft.Dynamics.Commerce.Tools.ExtensionsProxyGenerator.9.21.20042.5\\build\\Microsoft.Dynamics.Retail.RetailServerLibrary.dll C:\\RetailSDK\\References\\Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll /a:typescriptextensions
```

<span data-ttu-id="42329-139">実行するコマンドで、**Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** をカスタム Retail サーバー拡張ライブラリの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="42329-139">In the above command, replace **Microsoft.Dynamics.RetailServer.CrossLoyaltySample.dll** with the name of your custom Retail Server extension library.</span></span> <span data-ttu-id="42329-140">POS プロジェクトに生成されたファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="42329-140">Include the generated files in your POS project.</span></span> <span data-ttu-id="42329-141">このコマンドは、拡張ライブラリに基づいた 2 つのファイル、DataServiceEntities.g.ts と DataServiceRequests.g.tss を生成します。</span><span class="sxs-lookup"><span data-stu-id="42329-141">The command generates two files that are based on your extension libraries: DataServiceEntities.g.ts and DataServiceRequests.g.ts.</span></span>

## <a name="generate-the-c-proxy-commerce-version-10011-or-lower"></a><span data-ttu-id="42329-142">C# プロキシ (Commerce バージョン 10.0.11 以下) の生成</span><span class="sxs-lookup"><span data-stu-id="42329-142">Generate the C# proxy (Commerce version 10.0.11 or lower)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42329-143">この Microsoft.Dynamics.Commerce.Hosting.Contracts API を使用してビルトされた Retail Server 拡張機能は、オフライン実装でも使用でき、別に C# プロキシ ライブラリを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="42329-143">Retail Server extension built using this the Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts API can be used in and offline implementation, no need to generate separate C# proxy library.</span></span> <span data-ttu-id="42329-144">この手順は、Dynamics.Commerce.Runtime.Hosting.Contracts を使用しない Commerce バージョン 10.0.11 以前、または低またはRetail Server の拡張機能に対してのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="42329-144">This step is required only for Commerce version 10.0.11 or lower or Retail Server extensions not using the Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts.</span></span>

<span data-ttu-id="42329-145">Retail サーバー拡張機能ごとに、別個のプロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42329-145">For each Retail Server extension, you must generate a separate proxy.</span></span>

1. <span data-ttu-id="42329-146">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample** に移動します。</span><span class="sxs-lookup"><span data-stu-id="42329-146">Navigate to **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample**.</span></span>
2. <span data-ttu-id="42329-147">Microsoft Visual Studio で、**Proxies.RetailProxy.Extensions.StoreHoursSample** プロジェクト ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="42329-147">In Microsoft Visual Studio, open the **Proxies.RetailProxy.Extensions.StoreHoursSample** project file.</span></span>
3. <span data-ttu-id="42329-148">右クリックし、プロジェクトのアンロードを選択します。</span><span class="sxs-lookup"><span data-stu-id="42329-148">Right-click, and select to unload the project.</span></span>
4. <span data-ttu-id="42329-149">プロジェクトを右クリックし、**Proxies.RetailProxy.Extensions.StoreHoursSample.csproj** を選択して編集します。</span><span class="sxs-lookup"><span data-stu-id="42329-149">Right-click the project, and select to edit the **Proxies.RetailProxy.Extensions.StoreHoursSample.csproj** file.</span></span>
5. <span data-ttu-id="42329-150">最初のプロパティ グループ セクションで、次のノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="42329-150">In the first property group section, update the following nodes:</span></span>

    - <span data-ttu-id="42329-151">**&lt;RootNamespace&gt;** – ユーザー設定の名前空間を指定します。</span><span class="sxs-lookup"><span data-stu-id="42329-151">**&lt;RootNamespace&gt;** – Specify your custom namespace.</span></span>
    - <span data-ttu-id="42329-152">**&lt;AssemblyName&gt;** – プロキシのカスタム出力ライブラリ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="42329-152">**&lt;AssemblyName&gt;** – Specify your custom output library name for the proxy.</span></span>

6. <span data-ttu-id="42329-153">Retail サーバーの拡張機能ライブラリ名を指定して、**CommerceProxyGeneratorExtendedAssemblyPaths** 要素を更新します。</span><span class="sxs-lookup"><span data-stu-id="42329-153">Update the **CommerceProxyGeneratorExtendedAssemblyPaths** element by specifying the name of your Retail Server extension library.</span></span>

    <span data-ttu-id="42329-154">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="42329-154">Here is an example.</span></span>

    ```xml
    <CommerceProxyGeneratorExtendedAssemblyPaths Include="..\..\RetailServer\Extensions.StoreHoursSample\bin\$(Configuration)\net451\$(AssemblyNamePrefix).RetailServer.StoreHoursSample.dll" />
    ```

    > [!NOTE]
    > <span data-ttu-id="42329-155">**.RetailServer.StoreHoursSample.dll** は、Retail サーバー拡張アセンブリの名前です。残りの値は、接頭語 (接頭語がある場合) と、プロキシ エンジンがこのアセンブリを見つけることができるアセンブリのパスです。</span><span class="sxs-lookup"><span data-stu-id="42329-155">**.RetailServer.StoreHoursSample.dll** is the name of the Retail Server extension assembly, and the rest of the value is the prefix (if there is a prefix) and the path of the assembly where the proxy engine can find this assembly.</span></span> <span data-ttu-id="42329-156">プロキシは、このアセンブリに基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="42329-156">The proxy is generated based on this assembly.</span></span>

7. <span data-ttu-id="42329-157">ファイルを保存し、プロジェクトを再度読み込みます。</span><span class="sxs-lookup"><span data-stu-id="42329-157">Save the file, and load the project again.</span></span>
8. <span data-ttu-id="42329-158">拡張パターンに従って、プロジェクトの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="42329-158">Rename the project according to your extension pattern.</span></span>
9. <span data-ttu-id="42329-159">プロジェクトが読み込まれた後、**アダプタ** フォルダから **StoreDayHoursManager.cs** ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="42329-159">After the project is loaded, delete the **StoreDayHoursManager.cs** file from the **Adapters** folder.</span></span>
10. <span data-ttu-id="42329-160">すべての関連する CRT と Retail サーバー ライブラリをプロジェクトまたはアセンブリ参照としてプロキシ プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="42329-160">Add all the relevant CRT and Retail Server libraries to the proxy project as project or assembly references.</span></span>
11. <span data-ttu-id="42329-161">プロジェクトをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="42329-161">Rebuild the project.</span></span>

    <span data-ttu-id="42329-162">アダプタ フォルダー内で新しい Interfaces.g.cs ファイルが生成されると表示されます。</span><span class="sxs-lookup"><span data-stu-id="42329-162">You will see that a new Interfaces.g.cs file is generated inside the Adapters folder.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42329-163">プロキシ プロジェクトを作成する前に、すべての CRT および Retail サーバー拡張ライブラリを再構築して、**RetailSDK\\References** フォルダーにドロップしてください。</span><span class="sxs-lookup"><span data-stu-id="42329-163">Before you build the proxy project, rebuild all your CRT and Retail Server extension libraries, and drop them into the **RetailSDK\\References** folder.</span></span>

12. <span data-ttu-id="42329-164">プロキシ プロジェクト内に新しい **Interfaces.g.cs** ファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="42329-164">Include the new **Interfaces.g.cs** file in the proxy project.</span></span> <span data-ttu-id="42329-165">ただし、このファイルを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="42329-165">However, don't modify this file.</span></span>
13. <span data-ttu-id="42329-166">**アダプタ** フォルダーで、新しいクラス ファイルを追加し、拡張機能のパターンに従って名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="42329-166">Under the **Adapters** folder, add a new class file, and name it according to your extension pattern.</span></span>
14. <span data-ttu-id="42329-167">インターフェイス マネージャー クラスからクラスを拡張し、必要なインターフェイス メソッドのみを実装します。</span><span class="sxs-lookup"><span data-stu-id="42329-167">Extend the class from the interface manager class, and implement only the interface methods that are required.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42329-168">Interfaces.g.cs ファイルで、インターフェイス マネージャー クラスの名前を見つけることが</span><span class="sxs-lookup"><span data-stu-id="42329-168">You can find the name of the interface manager class in the Interfaces.g.cs.</span></span> <span data-ttu-id="42329-169">できます。</span><span class="sxs-lookup"><span data-stu-id="42329-169">file.</span></span>

    <span data-ttu-id="42329-170">次の例では、**IStoreDayHoursManager** はインターフェイスの名前です。</span><span class="sxs-lookup"><span data-stu-id="42329-170">In the following example, **IStoreDayHoursManager** is the name of the interface.</span></span>

    ```C#
    public interface IStoreDayHoursManager : Microsoft.Dynamics.Commerce.RetailProxy.IEntityManager
    {
    }
    ```

    <span data-ttu-id="42329-171">フル サンプル コードについては、**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample** にある **Proxies.RetailProxy.Extensions.StoreHoursSample** プロジェクトをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="42329-171">For the full sample code, see the **Proxies.RetailProxy.Extensions.StoreHoursSample** project under **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.StoreHoursSample**.</span></span>

15. <span data-ttu-id="42329-172">メソッド内で、実際の CRT 要求/応答を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="42329-172">Inside the methods you will call the actual CRT request/response.</span></span> <span data-ttu-id="42329-173">プロキシ プロジェクトに任意のロジックを含めないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="42329-173">Avoid including any logic in the proxy project.</span></span> <span data-ttu-id="42329-174">プロキシ プロジェクトは、CRT 要求/応答だけを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="42329-174">The proxy project should just call the CRT request/response.</span></span>
16. <span data-ttu-id="42329-175">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="42329-175">Build the project.</span></span>
17. <span data-ttu-id="42329-176">出力アセンブリをコピーして、**RetailSDK\\References** フォルダーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="42329-176">Copy the output assembly, and paste it in the **RetailSDK\\References** folder.</span></span>
18. <span data-ttu-id="42329-177">**RetailSDK\\Assets** フォルダーに移動して **RetailProxy.MPOSOffline.ext.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="42329-177">Navigate to the **RetailSDK\\Assets** folder, and open the **RetailProxy.MPOSOffline.ext.config** file.</span></span>
19. <span data-ttu-id="42329-178">**合成** セクションで、新しいプロキシ ライブラリ (つまり、プロキシ プロジェクトをビルドした後に生成されたアセンブリ) の名前を登録します。</span><span class="sxs-lookup"><span data-stu-id="42329-178">In the **composition** section, register the name of your new proxy library (that is, the assembly that was generated after you built your proxy project).</span></span>

    <span data-ttu-id="42329-179">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="42329-179">Here is an example.</span></span>

    ```xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />
    ```

    <span data-ttu-id="42329-180">この例では、プロキシ ライブラリ名は **Contoso.Commerce.RetailProxy.StoreHoursSample** です。</span><span class="sxs-lookup"><span data-stu-id="42329-180">In this example, the proxy library is named **Contoso.Commerce.RetailProxy.StoreHoursSample**.</span></span> <span data-ttu-id="42329-181">プロキシ ライブラリの名前は、**値** フィールドで指定してください。</span><span class="sxs-lookup"><span data-stu-id="42329-181">You should specify the name of your proxy library in the **value** field.</span></span>

20. <span data-ttu-id="42329-182">手動テストでは、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** にある **RetailProxy.MPOSOffline.ext.config** ファイルを開きます。カスタム プロキシ ライブラリの名前で **合成** セクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="42329-182">For manual testing, open the **RetailProxy.MPOSOffline.ext.config** file under **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext**. Update the **composition** section with the name of the custom proxy library.</span></span>

    <span data-ttu-id="42329-183">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="42329-183">Here is an example.</span></span>

    ```xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.StoreHoursSample" />
    ```

21. <span data-ttu-id="42329-184">電子商取引の場合、電子商取引プロジェクトから呼び出しする前に、拡張のプロキシを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42329-184">For e-Commerce, you must initialize the proxy for the extensions before you call it from your e-Commerce project.</span></span> <span data-ttu-id="42329-185">電子商取引の **Startup.cs** ファイル (または、Web プロジェクトの初期化などの同等のファイル) で、Retail プロキシ拡張の拡張データ モデル (EDM) を使用して **RetailServerContext** を初期化します。</span><span class="sxs-lookup"><span data-stu-id="42329-185">In your e-Commerce **Startup.cs** file (or an equivalent, such as web project initialization), initialize **RetailServerContext** with the Extended data model(EDM) model for your Retail proxy extension.</span></span> <span data-ttu-id="42329-186">それ以外の場合、プロキシのを呼び出そうとすると、ランタイム エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42329-186">Otherwise, you will receive a runtime error when you try to call the proxy.</span></span> <span data-ttu-id="42329-187">このステップは 1 回のみ完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42329-187">You must complete this step only one time.</span></span>

    <span data-ttu-id="42329-188">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="42329-188">Here is an example.</span></span>

    ```C#
    RetailServerContext.Initialize(newIEdmModelExtension[]
    {
        // /* BEGIN SDKSAMPLE_STOREHOURS
        new Contoso.Commerce.RetailProxy.StoreHoursSample.EdmModel(),
        // END SDKSAMPLE_STOREHOURS */
    });
    ```
