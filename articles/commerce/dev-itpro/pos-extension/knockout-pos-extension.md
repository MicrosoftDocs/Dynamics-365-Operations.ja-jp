---
title: POS 拡張機能での Knockout.js の使用
description: このトピックでは、販売時点管理 (POS) 拡張機能での Knockout.js の使用方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 1bc7d8559d935fa836076de2a2f3131b340807aa8ce38f024323d1468ea1156f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724542"
---
# <a name="use-knockoutjs-in-pos-extensions"></a>POS 拡張機能での Knockout.js の使用

[!include [banner](../../../includes/banner.md)]

このトピックでは、販売時点管理 (POS) 拡張機能での **Knockout.js** を使用した基本的な作業について説明します。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

1. **Knockout.js** ライブラリの NuGet パッケージ参照を、**Pos.Extensions** プロジェクトに追加します。
2. MSBuild ターゲットを追加して、ビルド中に knockout ライブラリをプロジェクト ディレクトリにコピーし、パッケージに含めます。 次の例は、XML を示しています。

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

3. パッケージの **manifest.json** ファイルを更新して、依存関係として knockout ライブラリが含まれるようにします。 **依存関係** 配列に knockout ライブラリの新しいエントリを追加します。

    > [!NOTE]
    > **modulePath** の値は、前の手順で追加した MSBuild ターゲットの **KnockoutjsFile** 変数と一致する必要があります。

    ```JSON
    "dependencies": [
        {
          "alias": "knockout",
          "format": "amd",
          "modulePath": "Libraries/knockout"
        }
    ]
    ```

4. **Pos.Extensions** プロジェクトファイルを更新して、**Knockout.js** タイプの宣言を含めます。

    1. knockout の公式リリースに移動します。
    2. **manifest.json** ファイルに依存関係として含めていたバージョンのソース コード (zip) をダウンロードします。
    3. zip ファイルのコンテンツを抽出します。 タイプは、**\<KNOCKOUT\_LIBRARY\_FOLDER\>\\build\\types\\knockout.d.ts** にあります。
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

    6. **knockout.d.ts** ファイルが自動的に含まれない場合に備えて、プロジェクトに含め、ソース管理システムにチェックインします。

5. **ApplicationStart**  トリガーを作成して、**\_\_posStopExtensionsBinding** ハンドラーを登録します。 この方法により、**Knockout.js** パッケージのバージョンと POS に読み込まれる他のバージョンとの競合を防ぎます。 [POS 拡張機能の例](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension)で、例を表示します。
6. 次の例に示すように、ライブラリをインポートして、拡張モジュールで **Knockout.js** を使用します。

    ```TypeScript
    import ko from "knockout"; // The name of the import 'knockout' must match the one in the tsconfig and manifest file.
    ```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
