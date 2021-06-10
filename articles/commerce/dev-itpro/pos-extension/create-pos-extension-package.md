---
title: POS 拡張機能パッケージ プロジェクトの作成
description: このトピックでは、販売時点管理 (POS) 拡張機能パッケージ プロジェクトの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: b6e97a2939aeaea0480f49ca680e495fc570d8dc
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984234"
---
# <a name="create-a-pos-extension-package-project"></a><span data-ttu-id="9e391-103">POS 拡張機能パッケージ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="9e391-103">Create a POS extension package project</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e391-104">このトピックでは、販売時点管理 (POS) 拡張機能パッケージ プロジェクトの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e391-104">This topic explains how to create a Point of Sale (POS) extension package project.</span></span> <span data-ttu-id="9e391-105">POS 拡張機能パッケージ プロジェクトは、一連の拡張機能で、組み合わせると、Microsoft Visual Studio を使用するカスタム エンド ツー エンド POS シナリオが有効になります。</span><span class="sxs-lookup"><span data-stu-id="9e391-105">A POS extension package project is a set of extensions that, when they are combined, enable a custom end-to-end POS scenario that uses Microsoft Visual Studio.</span></span> <span data-ttu-id="9e391-106">POS 拡張機能 パッケージ プロジェクトは、Modern POS (MPOS) と Cloud POS (CPOS) の両方の拡張機能シナリオに適用されます。</span><span class="sxs-lookup"><span data-stu-id="9e391-106">POS extension package projects apply to extension scenarios for both Modern POS (MPOS) and Cloud POS (CPOS).</span></span>

1. <span data-ttu-id="9e391-107">Visual Studio で、.NET Standard 2.0 で 新しい .NET Standard クラス ライブラリ プロジェクトを作成し、**POS.Extensions** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="9e391-107">In Visual Studio, create a new .NET Standard class library project that uses .NET Standard 2.0, and name it **POS.Extensions**.</span></span>
2. <span data-ttu-id="9e391-108">プロジェクトと一緒に作成されたクラス ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="9e391-108">Delete the class file that is created together with the project.</span></span>
3. <span data-ttu-id="9e391-109">カスタマイズ パッケージ内のすべてのプロジェクトが使用する共有プロパティ ファイル (XML ファイル) を作成します。</span><span class="sxs-lookup"><span data-stu-id="9e391-109">Create a shared properties file (XML file) that all projects in the customization package will use.</span></span> <span data-ttu-id="9e391-110">共有ファイルは、Commerce Runtime (CRT)、Retail Server、および Hardware Service 拡張機能のような異なる Microsoft Dynamics 365 Commerce 拡張機能に使われます。</span><span class="sxs-lookup"><span data-stu-id="9e391-110">This shared file can be used for different Microsoft Dynamics 365 Commerce extensions, such as Commerce runtime (CRT), Retail Server, and Hardware Service extensions.</span></span> <span data-ttu-id="9e391-111">ファイルに名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="9e391-111">Name the file.</span></span> <span data-ttu-id="9e391-112">この例では、ファイルに **CustomizationPackage.props** と名付けます。</span><span class="sxs-lookup"><span data-stu-id="9e391-112">For this example, the file is named **CustomizationPackage.props**.</span></span>
4. <span data-ttu-id="9e391-113">作成したソリューション ファイルと同じディレクトリにファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-113">Add the file to the same directory as the solution file that you created.</span></span>
5. <span data-ttu-id="9e391-114">次のプロパティ値をファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-114">Add the following property values to the file:</span></span>

    + <span data-ttu-id="9e391-115">**PackagePubpur** – パッケージ発行元の ID (たとえば、`CN=Contoso Ltd.`) です。</span><span class="sxs-lookup"><span data-stu-id="9e391-115">**PackagePublisher** – The identity of the package publisher (for example, `CN=Contoso Ltd.`).</span></span> <span data-ttu-id="9e391-116">パッケージに MPOS 拡張機能が含まれている場合、この値は、アプリ署名証明書の件名と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e391-116">If the package contains MPOS extensions, this value must match the subject of the app signing certificate.</span></span>
    + <span data-ttu-id="9e391-117">**PackagePublisherDisplayName** – パッケージ発行元の表示名 (たとえば `Contoso Ltd.`) です。</span><span class="sxs-lookup"><span data-stu-id="9e391-117">**PackagePublisherDisplayName** – The display name of the package publisher (for example, `Contoso Ltd.`).</span></span>
    + <span data-ttu-id="9e391-118">**PackageVersion** – カスタマイズ パッケージのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="9e391-118">**PackageVersion** – The version of the customization package.</span></span> <span data-ttu-id="9e391-119">この値は、メジャー バージョンが 0 (ゼロ) ではない (例えば `1.0.0.0`) であるクアド表記のバージョン文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e391-119">This value must be a version string in quad notation, where the major version isn't 0 (zero) (for example, `1.0.0.0`).</span></span>
    + <span data-ttu-id="9e391-120">**PackageName** – パッケージ名です。</span><span class="sxs-lookup"><span data-stu-id="9e391-120">**PackageName** – The package name.</span></span> <span data-ttu-id="9e391-121">この値は、3 文字から 50 文字の長さの文字列にする必要があり、また、英数字およびピリオドまたはハイフンでのみ構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e391-121">This value must be a string that is between three and 50 characters long, and it must consist of only alphanumeric characters, and periods or hyphens.</span></span> <span data-ttu-id="9e391-122">文字列をピリオドで終了することはできません。</span><span class="sxs-lookup"><span data-stu-id="9e391-122">The string can't end in a period.</span></span>
    + <span data-ttu-id="9e391-123">**PackageDisplayName** – パッケージの表示名です。</span><span class="sxs-lookup"><span data-stu-id="9e391-123">**PackageDisplayName** – The display name of the package.</span></span>
    + <span data-ttu-id="9e391-124">**PackageDescription** – パッケージの説明です。</span><span class="sxs-lookup"><span data-stu-id="9e391-124">**PackageDescription** – The package description.</span></span>

    <span data-ttu-id="9e391-125">XML ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9e391-125">Here is an example of the XML file.</span></span>

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

6. <span data-ttu-id="9e391-126">プロジェクト ファイルを編集し、**インポート** ステートメントを追加し、カスタマイズ パッケージに作成した共有プロパティ (.props) ファイルを含みます。</span><span class="sxs-lookup"><span data-stu-id="9e391-126">Edit the project file, and add an **Import** statement to include the shared properties (.props) file that you created for the customization package.</span></span>

    ```xml
    <Import Project="..\CustomizationPackage.props" />
    ```

7. <span data-ttu-id="9e391-127">プロジェクトの TypeScript サポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9e391-127">Enable TypeScript support for the project:</span></span>

    1. <span data-ttu-id="9e391-128">ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-128">In Solution Explorer, select and hold (or right-click) the project, and then select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="9e391-129">**NuGet パッケージ マネージャー** ウィンドウの **閲覧** タブで、**Microsoft.TypeScript.MSBuild** を検索します。</span><span class="sxs-lookup"><span data-stu-id="9e391-129">In the **NuGet Package Manager** window, on the **Browse** tab, search for **Microsoft.TypeScript.MSBuild**.</span></span>
    3. <span data-ttu-id="9e391-130">パッケージを選び、**インストール** をから最新の安定したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-130">Select the package, select **Install**, and then select the latest stable version.</span></span>

        > [!TIP]
        > <span data-ttu-id="9e391-131">統合開発環境 (IDE) エクスペリエンスでは、インストールする TypeScript NuGet パッケージのバージョンと一致する Visual Studio の TypeScript ツールのバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="9e391-131">For the best integrated development environment (IDE) experience, make sure that the version of the TypeScript Tools for Visual Studio that you install matches the version of the TypeScript NuGet package.</span></span> <span data-ttu-id="9e391-132">Microsoft.TypeScript.MSBuild のバージョン 4.2.3 を選択した場合は、Visual Studio の Typescript 4.2.3 をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9e391-132">If you selected version 4.2.3 of Microsoft.TypeScript.MSBuild, you can install Typescript 4.2.3 for Visual Studio.</span></span>
        >
        > <span data-ttu-id="9e391-133">Visual Studio Typescript ツールへのリンクは、[TypeScript/GitHub でリリース](https://github.com/microsoft/TypeScript/releases) で有効です。</span><span class="sxs-lookup"><span data-stu-id="9e391-133">Links for the Visual Studio Typescript tool are available in [TypeScript/releases on GitHub](https://github.com/microsoft/TypeScript/releases).</span></span>

8. <span data-ttu-id="9e391-134">Retail SDK NuGet パッケージへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-134">Add a reference to the Retail SDK NuGet package:</span></span>

    1. <span data-ttu-id="9e391-135">ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-135">In Solution Explorer, select and hold (or right-click) the project, and then select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="9e391-136">**NuGet パッケージ マネージャー** ウィンドウの **閲覧** タブで、**Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。</span><span class="sxs-lookup"><span data-stu-id="9e391-136">In the **NuGet Package Manager** window, on the **Browse** tab, search for **Microsoft.Dynamics.Commerce.Sdk.Pos**.</span></span>
    3. <span data-ttu-id="9e391-137">パッケージを選択し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-137">Select the package, and then select **Install**.</span></span>

        > [!TIP]
        > <span data-ttu-id="9e391-138">すべての Commerce NuGet パッケージは、次のパブリック リポジトリで見つかります。</span><span class="sxs-lookup"><span data-stu-id="9e391-138">All the Commerce NuGet packages can be found in the following public repository:</span></span>
        >
        > [https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json](https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json)

    4. <span data-ttu-id="9e391-139">パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-139">Add the package source location to the **nuget.config** file of your extension project file.</span></span> <span data-ttu-id="9e391-140">(まだ存在しない場合は、プロジェクト用に **nuget.config** ファイルを作成します。)</span><span class="sxs-lookup"><span data-stu-id="9e391-140">(Create a **nuget.config** file for your project if it doesn't already exist.)</span></span>

        ```xml
        <packageSources>
            <add key="dynamics365-commerce" value="https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json" />
            <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
        </packageSources>
        ```

9. <span data-ttu-id="9e391-141">プロジェクトに **tsconfig.json** ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-141">Add a **tsconfig.json** file to your project:</span></span>

    1. <span data-ttu-id="9e391-142">ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック)し、**追加** から **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-142">In Solution Explorer, select and hold (or right-click) the project, select **Add**, and then select **New item**.</span></span>
    2. <span data-ttu-id="9e391-143">**json** を検索し、**TypeScript JSON 構成ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-143">Search for **json**, and select **TypeScript JSON Configuration File**.</span></span>
    3. <span data-ttu-id="9e391-144">ファイルを **tsconfig.json** に名前を付けて、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-144">Name the file **tsconfig.json**, and then select **Add**.</span></span>

        ![tsconfig.json ファイルを追加](media/json-file.png)

    4. <span data-ttu-id="9e391-146">すべてのフィールドを JavaScript Object Notation (JSON) から削除し、**拡張** フィールドを追加して **pos-tsconfig-base.json** ファイルからファイルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9e391-146">Remove all the fields from the JavaScript Object Notation (JSON), and make the file extend from the **pos-tsconfig-base.json** file by adding an **extends** field.</span></span> <span data-ttu-id="9e391-147">完了すると、XML ファイルは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="9e391-147">When you've finished, the XML file should resemble the following example.</span></span>

        ```JSON
        {
            "extends": "./devDependencies/pos-tsconfig-base.json"
        }
        ```

10. <span data-ttu-id="9e391-148">プロジェクトを構築し、POS の依存関係をプロジェクト ディレクトリにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9e391-148">Build the project to copy the POS dependencies to the project directory.</span></span>
11. <span data-ttu-id="9e391-149">拡張機能パッケージのマニフェスト ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e391-149">Create the manifest file for your extension package:</span></span>

    1. <span data-ttu-id="9e391-150">ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック)し、**追加** から **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-150">In Solution Explorer, select and hold (or right-click) the project, select **Add**, and then **New item**.</span></span>
    2. <span data-ttu-id="9e391-151">**json** を検索し、**JSON ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-151">Search for **json**, and select **JSON File**.</span></span>
    3. <span data-ttu-id="9e391-152">ファイルを **manifest.json** に名前を付けて、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-152">Name the file **manifest.json**, and then select **Add**.</span></span>
    4. <span data-ttu-id="9e391-153">**manifest.json** ファイルで、最初の行として次の JSON を追加し POS 拡張機能マニフェスト スキーマに参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-153">In the **manifest.json** file, add the reference to the POS extension manifest schema by adding the following JSON as the first line.</span></span>

        ```JSON
        {
            "$schema": "./devDependencies/schemas/manifestSchema.json"
        }
        ```

    5. <span data-ttu-id="9e391-154">次のパッケージ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-154">Add the following package information:</span></span>

        + <span data-ttu-id="9e391-155">**名前** – 拡張機能パッケージの名前です。</span><span class="sxs-lookup"><span data-stu-id="9e391-155">**name** – The name of the extension package.</span></span>
        + <span data-ttu-id="9e391-156">**説明** – 拡張機能パッケージの機能の説明です。</span><span class="sxs-lookup"><span data-stu-id="9e391-156">**description** – A description of the extension package's functionality.</span></span>
        + <span data-ttu-id="9e391-157">**発行元** – 拡張機能パッケージの発行元または組織の名前です。</span><span class="sxs-lookup"><span data-stu-id="9e391-157">**publisher** – The name of the extension package's publisher or organization.</span></span>
        + <span data-ttu-id="9e391-158">**バージョン** – 拡張機能パッケージのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="9e391-158">**version** – The version of the extension package.</span></span> <span data-ttu-id="9e391-159">この値は、セマンティック バージョニング パターンに続く必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e391-159">This value must follow the semantic versioning pattern.</span></span>
        + <span data-ttu-id="9e391-160">**minimumPosVersion** – 拡張機能パッケージを実行するために必要な最小 POS バージョンです。</span><span class="sxs-lookup"><span data-stu-id="9e391-160">**minimumPosVersion** – The minimum POS version that is required to run the extension package.</span></span> <span data-ttu-id="9e391-161">バージョン番号は、消費している POS NuGet パッケージと、インストールされた POS アプリによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9e391-161">The version number depends on the POS NuGet package that you're consuming and the POS app that is installed.</span></span> <span data-ttu-id="9e391-162">たとえば、拡張機能プロジェクトでは、インストールされている POS アプリよりも古いバージョンから、POS API または 拡張機能アーティファクトを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="9e391-162">For example, the extension project should not use POS APIs or extension artifacts from a version that is later than the version of the POS app that is installed.</span></span> <span data-ttu-id="9e391-163">ランタイムに、POS アプリは拡張機能パッケージのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e391-163">At runtime, the POS app checks the version of the extension package.</span></span> <span data-ttu-id="9e391-164">インストールされた POS アプリよりも古いバージョンの場合、拡張機能パッケージは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="9e391-164">If it's later than the version of the installed POS app, the extension package won't be loaded.</span></span>

        <span data-ttu-id="9e391-165">こちらは、マニフェスト ファイルの例です。</span><span class="sxs-lookup"><span data-stu-id="9e391-165">Here is an example of a manifest file.</span></span>

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

12. <span data-ttu-id="9e391-166">ソリューションに CRT 拡張機能プロジェクトが含まれている場合、プロジェクト参照をソリューションの各 CRT 拡張機能プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="9e391-166">If your solution contains CRT extension projects, add project references to each CRT extension project in the solution:</span></span>

    1. <span data-ttu-id="9e391-167">ソリューション エクスプローラーで、MPOS を保留 (または右クリック)し、**追加** から **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-167">In Solution Explorer, select and hold (or right-click) the MPOS project, select **Add**, and then select **New item**.</span></span>
    2. <span data-ttu-id="9e391-168">参照マネージャーの左側の **プロジェクト** タブで、CRT 拡張機能プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e391-168">On the **Projects** tab on the left side of Reference Manager, select the CRT extension projects.</span></span>

13. <span data-ttu-id="9e391-169">拡張機能の基本メタデータをすべて作成したら、拡張機能を追加し、拡張機能を含むよう **manifest.json** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="9e391-169">After you've created all the base metadata for the extension, add your extension, and update the **manifest.json** file so that it includes your extension.</span></span> <span data-ttu-id="9e391-170">ユーザー インターフェイス (UI) および拡張機能のロジックを開発する方法については、[GitHub で Dynamics365Storee.InStore](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension) のサンプルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e391-170">For information about how to develop the user interface (UI) and logic for the extension, see the samples in [Dynamics365Commerce.InStore on GitHub](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension).</span></span>

<span data-ttu-id="9e391-171">拡張機能の作成が完了したら、CPOS または MPOS に配置できるようパッケージ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e391-171">After you've finished creating the extensions, you must package them so that they can be deployed to CPOS or MPOS.</span></span> <span data-ttu-id="9e391-172">詳細については、[Modern POS 拡張機能パッケージの .appx ファイルを作成](create-pos-extension-appx.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e391-172">For more information, see [Create an .appx file for a Modern POS extension package](create-pos-extension-appx.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
