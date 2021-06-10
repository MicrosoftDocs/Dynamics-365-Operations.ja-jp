---
title: POS 拡張機能での Knockout.js の使用
description: このトピックでは、POS 拡張機能で Knockout.js を使用する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: ee46590f5a8b542e3733776429b6c33a6fbc5c9c
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984298"
---
# <a name="use-knockoutjs-in-pos-extensions"></a><span data-ttu-id="40669-103">POS 拡張機能での Knockout.js の使用</span><span class="sxs-lookup"><span data-stu-id="40669-103">Use Knockout.js in POS extensions</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="40669-104">このトピックでは、POS 拡張機能での **Knockout.js** を使用した基本的な作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="40669-104">This topic shows some basic tasks using **Knockout.js** in POS extensions.</span></span> <span data-ttu-id="40669-105">これは、Retail SDK バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="40669-105">It applies to Retail SDK version 10.0.18 and later.</span></span>

1. <span data-ttu-id="40669-106">**Knockout.js** ライブラリの NuGet パッケージ参照を、Pos.Extensions プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="40669-106">Add a NuGet package reference for the **Knockout.js** library to your Pos.Extensions project.</span></span>
2. <span data-ttu-id="40669-107">MSBuild ターゲットを追加して、ビルド中に knockout ライブラリをプロジェクト ディレクトリにコピーし、パッケージに含めます。</span><span class="sxs-lookup"><span data-stu-id="40669-107">Add an MSBuild target to copy the knockout library to your project directory during the build and include it in your package.</span></span> <span data-ttu-id="40669-108">Xml は、次の例に示されています。</span><span class="sxs-lookup"><span data-stu-id="40669-108">The Xml is shown in the following example.</span></span>

    ```XML
    <Target Name="ContentIncludeKnockoutLibrary" BeforeTargets="AssignTargetPaths" DependsOnTargets="RunResolvePackageDependencies">
        <PropertyGroup>
            <KnockoutjsFile>Libraries/knockout.js</KnockoutjsFile>
            <KnockoutLibraryFilePath Condition="'%(PackageDefinitions.Name)' == 'knockoutjs'">%(PackageDefinitions.ResolvedPath)\Content\Scripts\knockout-%(PackageDefinitions.Version).js</KnockoutLibraryFilePath>
        </PropertyGroup>
        <Copy SourceFiles="$(KnockoutLibraryFilePath)" DestinationFiles="$(KnockoutjsFile)" SkipUnchangedFiles="true" /> <!-- Necessary for CPOS -->
        <ItemGroup>
            <Content Include="$(KnockoutjsFile)"></Content>
        </ItemGroup>
    </Target>
    ```

3. <span data-ttu-id="40669-109">knockout ライブラリをパッケージの **manifest.json** ファイルの依存関係として追加します。</span><span class="sxs-lookup"><span data-stu-id="40669-109">Add the knockout library as a dependency in your package’s **manifest.json** file.</span></span> <span data-ttu-id="40669-110">manifest.json を更新して、Knockout ライブラリの **依存関係** 配列に新しいエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="40669-110">Update the manifest.json to add a new entry in the **dependencies** array for the Knockout library.</span></span>

    > [!NOTE]
    > <span data-ttu-id="40669-111">**modulePath** は、上記ターゲットの **KnockoutjsFile** 変数と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40669-111">The **modulePath** must match the **KnockoutjsFile** variable in the target shown above.</span></span>

    ```JSON
    "dependencies": [
        {
          "alias": "knockout",
          "format": "amd",
          "modulePath": "Libraries/knockout"
        }
    ]
    ```

4. <span data-ttu-id="40669-112">Pos.Extensions プロジェクト ファイルを更新して、Knockout.js タイプの宣言を含めます。</span><span class="sxs-lookup"><span data-stu-id="40669-112">Update your Pos.Extensions project file to include the Knockout.js type declarations.</span></span>

    1. <span data-ttu-id="40669-113">knockout の公式リリースに移動します。</span><span class="sxs-lookup"><span data-stu-id="40669-113">Navigate to the knockout official releases.</span></span>
    2. <span data-ttu-id="40669-114">manifest.json に依存関係として含めていたバージョンのソース コード (zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="40669-114">Download the source code (zip) of the version that was included as a dependency in the manifest.json.</span></span>
    3. <span data-ttu-id="40669-115">zip ファイルのコンテンツを抽出します。</span><span class="sxs-lookup"><span data-stu-id="40669-115">Extract the content of the zip file.</span></span> <span data-ttu-id="40669-116">タイプは、**<KNOCKOUT_LIBRARY_FOLDER>\build\types\knockout.d.ts** にあります。</span><span class="sxs-lookup"><span data-stu-id="40669-116">The types are located at **<KNOCKOUT_LIBRARY_FOLDER>\build\types\knockout.d.ts**.</span></span>
    4. <span data-ttu-id="40669-117">**knockout.d.ts** ファイルを拡張機能プロジェクトの任意のフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="40669-117">Copy the **knockout.d.ts** file to any folder in the extension project.</span></span>
    5. <span data-ttu-id="40669-118">**tsconfig.json** ファイルを更新して、**Knockout.js** の **パス** エイリアスを含めます。</span><span class="sxs-lookup"><span data-stu-id="40669-118">Update your **tsconfig.json** file to include a **paths** alias for **Knockout.js**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="40669-119">次のコード例の **Libraries/knockout** を、前の手順で **knockout.d.ts** ファイルをコピーした場所への相対パスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="40669-119">Replace **Libraries/knockout** in the following code example with the relative path to where you copied the **knockout.d.ts** file in the previous step.</span></span>

        ```JSON
        {
          "extends": "./devDependencies/pos-tsconfig-base.json",
          "compilerOptions": {
            "baseUrl": ".",
            "paths": {
              "knockout": [ "Libraries/knockout" ]
            },
            "noImplicitAny": false
          }
        }
        ```

    6. <span data-ttu-id="40669-120">**knockout.d.ts** ファイルが自動的に含まれない場合に備えて、プロジェクトに含め、ソース管理システムにチェック インします。</span><span class="sxs-lookup"><span data-stu-id="40669-120">Include the **knockout.d.ts** file in the project in case it wasn't included automatically and check it in to your source control system.</span></span>

5. <span data-ttu-id="40669-121">**ApplicationStart** トリガーを作成して **__posStopExtensionsBinding** ハンドラーを登録し、**Knockout.js** のパッケージ バージョンと、POS に読み込まれる他のバージョンとの競合を防ぎます。</span><span class="sxs-lookup"><span data-stu-id="40669-121">Create an **ApplicationStart** trigger to register the **__posStopExtensionsBinding** handler to prevent collisions between the package’s version of **Knockout.js** and others that might be loaded in POS.</span></span> <span data-ttu-id="40669-122">[POS 拡張機能の例](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension)で、例を表示します。</span><span class="sxs-lookup"><span data-stu-id="40669-122">An example is available in the [POS extension samples](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension).</span></span>

6. <span data-ttu-id="40669-123">次のコード例に示すように、ライブラリをインポートして、拡張モジュールで **Knockout.js** を使用します。</span><span class="sxs-lookup"><span data-stu-id="40669-123">Use **Knockout.js** in your extension modules by importing the library as shown in the following code example.</span></span>

```TypeScript
import ko from "knockout"; // The name of the import 'knockout' must match the one in the tsconfig and manifest file.
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
