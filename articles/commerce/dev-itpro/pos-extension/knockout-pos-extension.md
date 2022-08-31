---
title: POS 拡張機能で Knockout.js のような外部またはサード パーティー ライブラリを使用する方法
description: この記事では、販売時点管理 (POS) 拡張機能で Knockout.js のような外部またはサード パーティー ライブラリを使用する方法について説明します。
author: josaw1
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a5f287273c4dcfe7acba3a58c91fbbd717a0a5c0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286602"
---
# <a name="consume-external-or-third-party-libraries-like-knockoutjs-in-pos-extensions"></a>POS 拡張機能で Knockout.js のような外部またはサード パーティー ライブラリを使用する

[!include [banner](../../../includes/banner.md)]

この記事では、販売時点管理 (POS) 拡張機能で **Knockout.js** を使用する方法に関するいくつかの基本的な手順を示します。同じパターンを、他の外部ライブラリまたはサード パーティー ライブラリに適用できます。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

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
> [!NOTE]
> 外部ライブラリが他のライブラリに依存している場合は、依存関係をコピーするために、パッケージ マニフェストと msbuild ターゲットにすべての依存ライブラリを含めます。

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
