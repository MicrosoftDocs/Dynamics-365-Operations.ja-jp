---
title: POS 拡張機能パッケージ プロジェクトの作成
description: このトピックでは、POS 拡張機能パッケージ プロジェクトの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 291a661ae0cb3d6ed5812e8c860d2db3e0f34e0b
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960156"
---
# <a name="create-a-pos-extension-package-project"></a><span data-ttu-id="48c28-103">POS 拡張機能パッケージ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="48c28-103">Create a POS extension package project</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48c28-104">このドキュメントの手順では、POS 拡張機能パッケージ プロジェクトを作成する方法について説明します。これは、組み合わせたときに Visual Studio を使用してカスタムのエンド ツー エンド POS シナリオを有効にする一連の拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="48c28-104">The steps in this document describe how to create a POS extension package project, a set of extensions that when combined enable a custom end to end POS scenario using Visual Studio.</span></span> <span data-ttu-id="48c28-105">POS 拡張機能 パッケージ プロジェクトは、Modern POS と Cloud POS の拡張機能のシナリオの両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="48c28-105">POS extension package projects apply to both Modern POS and Cloud POS extension scenarios.</span></span>

1. <span data-ttu-id="48c28-106">Visual Studio で、.NET Standard 2.0 を含む新しい .NET Standard クラス ライブラリ プロジェクトを作成し、**POS.Extensions** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="48c28-106">In Visual Studio, create a new .NET Standard Class Library Project with .NET Standard 2.0 and name it **POS.Extensions**.</span></span>
2. <span data-ttu-id="48c28-107">プロジェクトで作成されたクラス ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="48c28-107">Delete the class file that is created with the project.</span></span>
3. <span data-ttu-id="48c28-108">カスタマイズ パッケージ内のすべてのプロジェクトで使用される共有プロパティ ファイル (XMLファイル) を作成します。</span><span class="sxs-lookup"><span data-stu-id="48c28-108">Create a shared properties file (XML file) to be used by all projects in the customization package.</span></span> <span data-ttu-id="48c28-109">この共有ファイルは、CRT、Retail Server、ハードウェア サービスを含むさまざまなコマース拡張機能で使用できます。</span><span class="sxs-lookup"><span data-stu-id="48c28-109">This shared file can be used for different Commerce extensions including CRT, Retail Server, and Hardware Service.</span></span> <span data-ttu-id="48c28-110">ファイルに **CustomizationPackage.props** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="48c28-110">Name the file **CustomizationPackage.props**.</span></span> <span data-ttu-id="48c28-111">(このファイルには別の名前を選択できます。)</span><span class="sxs-lookup"><span data-stu-id="48c28-111">(You can choose another name for the file.)</span></span>

    1. <span data-ttu-id="48c28-112">前の手順で作成したソリューション ファイルと同じディレクトリにファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-112">Add the file to the same directory as the solution file created in the previous step.</span></span>
    2. <span data-ttu-id="48c28-113">次のプロパティ値をファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-113">Add the following property values to the file:</span></span>

        + <span data-ttu-id="48c28-114">**PackagePubpur**: パッケージ発行元 ID は、たとえば、`CN=Contoso Ltd.` です。</span><span class="sxs-lookup"><span data-stu-id="48c28-114">**PackagePublisher**: The package publisher identity, for example, `CN=Contoso Ltd.`.</span></span> <span data-ttu-id="48c28-115">パッケージに ModernPos の拡張機能が含まれている場合、この値は、アプリ署名証明書の件名と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48c28-115">If the package contains ModernPos extensions, this value must match the subject of the app signing certificate.</span></span>
        + <span data-ttu-id="48c28-116">**PackagePublisherDisplayName**: パッケージの発行元の表示名は、たとえば `Contoso Ltd.` です。</span><span class="sxs-lookup"><span data-stu-id="48c28-116">**PackagePublisherDisplayName**: The display name of the package publisher, for example, `Contoso Ltd.`.</span></span>
        + <span data-ttu-id="48c28-117">**PackageVersion**: カスタマイズ パッケージのバージョン。</span><span class="sxs-lookup"><span data-stu-id="48c28-117">**PackageVersion**: The customization package version.</span></span> <span data-ttu-id="48c28-118">これは、メジャー バージョンが 0 ではないクアド表記のバージョン文字列は、例えば `1.0.0.0` である必要があります。</span><span class="sxs-lookup"><span data-stu-id="48c28-118">This must be a version string in quad notation where the major version is not 0, for example, `1.0.0.0`.</span></span>
        + <span data-ttu-id="48c28-119">**PackageName**: パッケージ名。</span><span class="sxs-lookup"><span data-stu-id="48c28-119">**PackageName**: The package name.</span></span> <span data-ttu-id="48c28-120">これは、英数字とピリオドまたはダッシュ文字で構成される 3 〜 50 文字の長さの文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="48c28-120">This must be a string between 3 and 50 characters in length that consists of alpha-numeric and period or dash characters.</span></span> <span data-ttu-id="48c28-121">文字列をピリオドで終了することはできません。</span><span class="sxs-lookup"><span data-stu-id="48c28-121">The string cannot end in a period.</span></span>
        + <span data-ttu-id="48c28-122">**PackageDisplayName**: パッケージの表示名。</span><span class="sxs-lookup"><span data-stu-id="48c28-122">**PackageDisplayName**: The package display name.</span></span>
        + <span data-ttu-id="48c28-123">**PackageDescription**: パッケージの説明。</span><span class="sxs-lookup"><span data-stu-id="48c28-123">**PackageDescription**: The package description.</span></span>

    3. <span data-ttu-id="48c28-124">XML ファイルは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="48c28-124">The Xml file looks like the following example:</span></span>

        ```xml
        <Project>
          <PropertyGroup>
            <Version>1.0.0.0</Version>
            <PackagePublisher Condition="'$(PackagePublisher)' == ''">$(Publisher)</PackagePublisher>
            <PackagePublisherDisplayName Condition="'$(PackagePublisherDisplayName)' == ''">$(PublisherDisplayName)</PackagePublisherDisplayName>
            <PackageVersion Condition="'$(PackageVersion)' == ''">$(Version)</PackageVersion>
            <PackageName Condition="'$(PackageName)' == ''">Contoso.Commerce</PackageName>
            <PackageDisplayName Condition="'$(PackageDisplayName)' == ''">Contoso POS Commerce Customization</PackageDisplayName>
            <PackageDescription Condition="'$(PackageDescription)' == ''">Contoso POS Commerce Customization</PackageDescription>
          </PropertyGroup>
        </Project>
        ```

4. <span data-ttu-id="48c28-125">プロジェクト ファイルを編集し、**インポート** ステートメントを追加して、上記の手順で作成したカスタマイズ パッケージ **props** ファイルを含みます。</span><span class="sxs-lookup"><span data-stu-id="48c28-125">Edit the project file and add the **Import** statement to include the customization package **props** file created in the step above.</span></span>

    ```xml
    <Import Project="..\CustomizationPackage.props" />
    ```

5. <span data-ttu-id="48c28-126">プロジェクトの TypeScript のサポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="48c28-126">Enable TypeScript support for the project.</span></span>

    1. <span data-ttu-id="48c28-127">プロジェクト ソリューション エクスプローラーを選択し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-127">Right-click the project Solution Explorer and select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="48c28-128">NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-128">Select the **Browse** tab in the NuGet Package Manager window.</span></span>
    3. <span data-ttu-id="48c28-129">**Microsoft.TypeScript.MSBuild** を検索します。</span><span class="sxs-lookup"><span data-stu-id="48c28-129">Search for **Microsoft.TypeScript.MSBuild**.</span></span>
    4. <span data-ttu-id="48c28-130">パッケージを選択し、**インストール** を選択して、最新の安定したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-130">Select the package and select **Install**, then select the latest stable version.</span></span>

        > [!TIP]
        > <span data-ttu-id="48c28-131">最高の IDE エクスペリエンスには、インストールした Visual Studio バージョンの TypeScript ツールが TypeScript NuGet パッケージ バージョンと一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="48c28-131">For the best IDE experience, make sure that the TypeScript Tools for Visual Studio version you have installed matches the TypeScript NuGet package version.</span></span> <span data-ttu-id="48c28-132">Microsoft.TypeScript.MSBuild バージョン 4.2.3 を選択した場合は、Visual Studio の Typescript 4.2.3 をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="48c28-132">If you selected Microsoft.TypeScript.MSBuild version 4.2.3, then you can install the Typescript 4.2.3 for Visual Studio.</span></span>
        > <span data-ttu-id="48c28-133">Visual Studio TypeScript ツールへのリンクは、ここに表示されます: [リリース · microsoft/TypeScript (github.com)](https://github.com/microsoft/TypeScript/releases)</span><span class="sxs-lookup"><span data-stu-id="48c28-133">Links for the Visual Studio Typescript tool can be found here: [Releases · microsoft/TypeScript (github.com)](https://github.com/microsoft/TypeScript/releases)</span></span>

6. <span data-ttu-id="48c28-134">Retails SDK NuGet パッケージへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-134">Add a reference to the Retails SDK NuGet Package.</span></span>

    1. <span data-ttu-id="48c28-135">プロジェクト ソリューション エクスプローラーを選択し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-135">Right-click the project Solution Explorer and select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="48c28-136">NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-136">Select the **Browse** tab in the NuGet Package Manager window.</span></span>
    3. <span data-ttu-id="48c28-137">**Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。</span><span class="sxs-lookup"><span data-stu-id="48c28-137">Search for **Microsoft.Dynamics.Commerce.Sdk.Pos**.</span></span>
    4. <span data-ttu-id="48c28-138">パッケージを選択し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-138">Select the package and then select **Install**.</span></span>

        > [!TIP]
        > <span data-ttu-id="48c28-139">すべての Commerce NuGet パッケージ は、このパブリック リポジトリから見つかりません: [https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json](https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json)。</span><span class="sxs-lookup"><span data-stu-id="48c28-139">All the Commerce NuGet packages can be found from this public repository: [https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json](https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json).</span></span>

    5. <span data-ttu-id="48c28-140">パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-140">Add the package source location to the **nuget.config** file of your extension project file.</span></span> <span data-ttu-id="48c28-141">(プロジェクトが作成されていない場合は、新しい nuget.config ファイルを作成します)。</span><span class="sxs-lookup"><span data-stu-id="48c28-141">(Create a new nuget.config file for your project if it’s not created already).</span></span>

        ```xml
        <packageSources>
            <add key="dynamics365-commerce" value="https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json" />
            <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
            </packageSources>
        ```

7. <span data-ttu-id="48c28-142">次の手順に従って、**tsconfig.json** ファイルをプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-142">Add a **tsconfig.json** file to your project, by following these steps:</span></span>

    1. <span data-ttu-id="48c28-143">プロジェクト ソリューション エクスプローラーを右クリックし、**追加** を選択してから **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-143">Right-click the project Solution Explorer and select **Add** and then **New item**.</span></span>
    2. <span data-ttu-id="48c28-144">**json** を検索し、**TypeScript JSON 構成ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-144">Search for **json** and select **TypeScript JSON Configuration File**.</span></span> <span data-ttu-id="48c28-145">ファイルを **tsconfig.json** に名前を付けて、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-145">Name the file **tsconfig.json**, and then select **Add**.</span></span>

        ![tsconfig.json](media/json-file.png)

    3. <span data-ttu-id="48c28-147">JSON からすべてのファイルを削除し、**拡張機能** フィールドを追加して、**pos-tsconfig-base** **tsconfig** ファイルから拡張します。</span><span class="sxs-lookup"><span data-stu-id="48c28-147">Remove all the fields from the JSON and make it extend from the **pos-tsconfig-base** **tsconfig** file by adding an **extends** field.</span></span> <span data-ttu-id="48c28-148">XML ファイルは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="48c28-148">The Xml file will look like the following example:</span></span>

        ```JSON
        {
            "extends": "./devDependencies/pos-tsconfig-base.json"
        }
        ```

8. <span data-ttu-id="48c28-149">プロジェクトを構築し、POS の依存関係をプロジェクト ディレクトリにコピーします。</span><span class="sxs-lookup"><span data-stu-id="48c28-149">Build the project to copy the POS dependencies to the project directory.</span></span>

9. <span data-ttu-id="48c28-150">拡張機能パッケージのマニフェスト ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="48c28-150">Create the manifest file for your extension package.</span></span>

    1. <span data-ttu-id="48c28-151">プロジェクト ソリューション エクスプローラーを右クリックし、**追加** を選択してから **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-151">Right-click the project Solution Explorer and select **Add** and then **New item**.</span></span>
    2. <span data-ttu-id="48c28-152">**json** を検索し、**JSON ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-152">Search for **json** and select **JSON File**.</span></span> <span data-ttu-id="48c28-153">ファイルを **manifest.json** に名前を付けて、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-153">Name the file **manifest.json**, and then select **Add**.</span></span>
    3. <span data-ttu-id="48c28-154">**manifest.json** の最初の行として次の JSON を追加して、**POS 拡張機能マニフェスト スキーマ** への参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-154">Add the reference to the **POS Extension Manifest Schema** by adding the following JSON as the first line in **manifest.json**:</span></span>

        ```JSON
        {
            "$schema": "./devDependencies/schemas/manifestSchema.json"
        }
        ```

    4. <span data-ttu-id="48c28-155">**manifest.json** ファイルでパッケージ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-155">Add the package information in your **manifest.json** file.</span></span>

        + <span data-ttu-id="48c28-156">**名前**: 拡張パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="48c28-156">**name**: The name of the extension package.</span></span>
        + <span data-ttu-id="48c28-157">**説明**: 拡張機能パッケージの機能の説明。</span><span class="sxs-lookup"><span data-stu-id="48c28-157">**description**: A description of the extension package's functionality.</span></span>
        + <span data-ttu-id="48c28-158">**発行元**: 拡張機能パッケージ発行元または組織の名前。</span><span class="sxs-lookup"><span data-stu-id="48c28-158">**publisher**: The name of the extension package publisher or organization.</span></span>
        + <span data-ttu-id="48c28-159">**バージョン**: 拡張機能パッケージのバージョン。</span><span class="sxs-lookup"><span data-stu-id="48c28-159">**version**: The extension package version.</span></span> <span data-ttu-id="48c28-160">これは、セマンティック バージョニング パターンに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="48c28-160">This must follow semantic versioning pattern.</span></span>
        + <span data-ttu-id="48c28-161">**minimumPosVersion**: この拡張機能パッケージを実行するために必要な最小 POS バージョン。</span><span class="sxs-lookup"><span data-stu-id="48c28-161">**minimumPosVersion**: The minimum POS version required to run this extension package.</span></span> <span data-ttu-id="48c28-162">このバージョン番号は、消費している POS NuGet パッケージと、インストールされている POS アプリケーションによって異なります。</span><span class="sxs-lookup"><span data-stu-id="48c28-162">This version number depends on POS NuGet package you are consuming, and the POS application installed.</span></span> <span data-ttu-id="48c28-163">たとえば、拡張機能プロジェクトでは、インストールされている POS アプリよりも古いバージョンの拡張機能アーティファクトである POS アプリを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="48c28-163">For example, the extension project should not use POS APIs, extension artifacts from version higher than the POS app that is installed.</span></span> <span data-ttu-id="48c28-164">実行時に、POS アプリは、拡張機能パッケージのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="48c28-164">During runtime, the POS app will check the version of the extension package.</span></span> <span data-ttu-id="48c28-165">インストールされている POS アプリよりも高い場合、拡張機能パッケージは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="48c28-165">If it's higher than the installed POS app, then the extension package will not be loaded.</span></span>

        <span data-ttu-id="48c28-166">これは、マニフェスト ファイルの例です。</span><span class="sxs-lookup"><span data-stu-id="48c28-166">This is an example of the manifest file:</span></span>

        ```JSON
        {
            "$schema": "./devDependencies/schemas/manifestSchema.json",
            "name": "Contoso.Pos.Developer.Samples",
            "publisher": "Contoso",
            "version": "1.0.0",
            "minimumPosVersion": "9.28.0.0",
            "description": "An extension package containing POS developer samples to showcase various types of POS extensions.",
        }
        ```

10. <span data-ttu-id="48c28-167">ソリューションに Commerce Runtime 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Commerce Runtime 拡張機能プロジェクトをプロジェクト参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="48c28-167">If your solution contains Commerce Runtime extension projects, then add project references to each of the Commerce Runtime extension projects in the solution.</span></span>

    1. <span data-ttu-id="48c28-168">Modern POS プロジェクト ソリューション エクスプローラーを右クリックし、**追加** を選択してから **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-168">Right-click the Modern POS project Solution Explorer and select **Add** and then **New item**.</span></span>
    2. <span data-ttu-id="48c28-169">参照マネージャの左側にある **プロジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-169">Select the **Projects** tab on the left side of the Reference Manager.</span></span>
    3. <span data-ttu-id="48c28-170">Commerce Runtime 拡張機能プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="48c28-170">Select the Commerce Runtime extension projects.</span></span>

11. <span data-ttu-id="48c28-171">拡張機能の基本メタデータをすべて作成したら、拡張機能を追加し、**manifest.json** を更新して拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="48c28-171">After you have created all the base metadata for the extension, add your extension and update the **manifest.json** to include your extension.</span></span> <span data-ttu-id="48c28-172">拡張機能 UI とロジックの開発の詳細については、[Dynamics365Commerce.InStore](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension) でサンプルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="48c28-172">For information about developing the extension UI and logic, see the samples in[Dynamics365Commerce.InStore](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension).</span></span>

<span data-ttu-id="48c28-173">拡張機能を作成した後、Cloud POS または MPOS に配置する機能拡張をパッケージ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48c28-173">After creating the extensions, you must package them to be deployed to Cloud POS or MPOS.</span></span> <span data-ttu-id="48c28-174">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48c28-174">For more information, see:</span></span>

+ [<span data-ttu-id="48c28-175">Modern POS 拡張 appx ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="48c28-175">Create a Modern POS extension appx file</span></span>](create-pos-extension-appx.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
