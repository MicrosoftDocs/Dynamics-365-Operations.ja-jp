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
# <a name="use-knockoutjs-in-pos-extensions"></a>POS 拡張機能での Knockout.js の使用

[!include [banner](../../../includes/banner.md)]

このトピックでは、POS 拡張機能での **Knockout.js** を使用した基本的な作業について説明します。 これは、Retail SDK バージョン 10.0.18 以降に適用されます。

1. **Knockout.js** ライブラリの NuGet パッケージ参照を、Pos.Extensions プロジェクトに追加します。
2. MSBuild ターゲットを追加して、ビルド中に knockout ライブラリをプロジェクト ディレクトリにコピーし、パッケージに含めます。 Xml は、次の例に示されています。

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

3. knockout ライブラリをパッケージの **manifest.json** ファイルの依存関係として追加します。 manifest.json を更新して、Knockout ライブラリの **依存関係** 配列に新しいエントリを追加します。

    > [!NOTE]
    > **modulePath** は、上記ターゲットの **KnockoutjsFile** 変数と一致する必要があります。

    ```JSON
    "dependencies": [
        {
          "alias": "knockout",
          "format": "amd",
          "modulePath": "Libraries/knockout"
        }
    ]
    ```

4. Pos.Extensions プロジェクト ファイルを更新して、Knockout.js タイプの宣言を含めます。

    1. knockout の公式リリースに移動します。
    2. manifest.json に依存関係として含めていたバージョンのソース コード (zip) をダウンロードします。
    3. zip ファイルのコンテンツを抽出します。 タイプは、**<KNOCKOUT_LIBRARY_FOLDER>\build\types\knockout.d.ts** にあります。
    4. **knockout.d.ts** ファイルを拡張機能プロジェクトの任意のフォルダーにコピーします。
    5. **tsconfig.json** ファイルを更新して、**Knockout.js** の **パス** エイリアスを含めます。

        > [!NOTE]
        > 次のコード例の **Libraries/knockout** を、前の手順で **knockout.d.ts** ファイルをコピーした場所への相対パスに置き換えます。

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

    6. **knockout.d.ts** ファイルが自動的に含まれない場合に備えて、プロジェクトに含め、ソース管理システムにチェック インします。

5. **ApplicationStart** トリガーを作成して **__posStopExtensionsBinding** ハンドラーを登録し、**Knockout.js** のパッケージ バージョンと、POS に読み込まれる他のバージョンとの競合を防ぎます。 [POS 拡張機能の例](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension)で、例を表示します。

6. 次のコード例に示すように、ライブラリをインポートして、拡張モジュールで **Knockout.js** を使用します。

```TypeScript
import ko from "knockout"; // The name of the import 'knockout' must match the one in the tsconfig and manifest file.
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
