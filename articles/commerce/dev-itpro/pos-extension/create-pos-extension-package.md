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
# <a name="create-a-pos-extension-package-project"></a>POS 拡張機能パッケージ プロジェクトの作成

[!include [banner](../../includes/banner.md)]

このドキュメントの手順では、POS 拡張機能パッケージ プロジェクトを作成する方法について説明します。これは、組み合わせたときに Visual Studio を使用してカスタムのエンド ツー エンド POS シナリオを有効にする一連の拡張機能です。 POS 拡張機能 パッケージ プロジェクトは、Modern POS と Cloud POS の拡張機能のシナリオの両方に適用されます。

1. Visual Studio で、.NET Standard 2.0 を含む新しい .NET Standard クラス ライブラリ プロジェクトを作成し、**POS.Extensions** と名前を付けます。
2. プロジェクトで作成されたクラス ファイルを削除します。
3. カスタマイズ パッケージ内のすべてのプロジェクトで使用される共有プロパティ ファイル (XMLファイル) を作成します。 この共有ファイルは、CRT、Retail Server、ハードウェア サービスを含むさまざまなコマース拡張機能で使用できます。 ファイルに **CustomizationPackage.props** と名前を付けます。 (このファイルには別の名前を選択できます。)

    1. 前の手順で作成したソリューション ファイルと同じディレクトリにファイルを追加します。
    2. 次のプロパティ値をファイルに追加します。

        + **PackagePubpur**: パッケージ発行元 ID は、たとえば、`CN=Contoso Ltd.` です。 パッケージに ModernPos の拡張機能が含まれている場合、この値は、アプリ署名証明書の件名と一致する必要があります。
        + **PackagePublisherDisplayName**: パッケージの発行元の表示名は、たとえば `Contoso Ltd.` です。
        + **PackageVersion**: カスタマイズ パッケージのバージョン。 これは、メジャー バージョンが 0 ではないクアド表記のバージョン文字列は、例えば `1.0.0.0` である必要があります。
        + **PackageName**: パッケージ名。 これは、英数字とピリオドまたはダッシュ文字で構成される 3 〜 50 文字の長さの文字列である必要があります。 文字列をピリオドで終了することはできません。
        + **PackageDisplayName**: パッケージの表示名。
        + **PackageDescription**: パッケージの説明。

    3. XML ファイルは次の例のようになります。

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

4. プロジェクト ファイルを編集し、**インポート** ステートメントを追加して、上記の手順で作成したカスタマイズ パッケージ **props** ファイルを含みます。

    ```xml
    <Import Project="..\CustomizationPackage.props" />
    ```

5. プロジェクトの TypeScript のサポートを有効にします。

    1. プロジェクト ソリューション エクスプローラーを選択し、**NuGet パッケージの管理** を選択します。
    2. NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。
    3. **Microsoft.TypeScript.MSBuild** を検索します。
    4. パッケージを選択し、**インストール** を選択して、最新の安定したバージョンを選択します。

        > [!TIP]
        > 最高の IDE エクスペリエンスには、インストールした Visual Studio バージョンの TypeScript ツールが TypeScript NuGet パッケージ バージョンと一致していることを確認してください。 Microsoft.TypeScript.MSBuild バージョン 4.2.3 を選択した場合は、Visual Studio の Typescript 4.2.3 をインストールできます。
        > Visual Studio TypeScript ツールへのリンクは、ここに表示されます: [リリース · microsoft/TypeScript (github.com)](https://github.com/microsoft/TypeScript/releases)

6. Retails SDK NuGet パッケージへの参照を追加します。

    1. プロジェクト ソリューション エクスプローラーを選択し、**NuGet パッケージの管理** を選択します。
    2. NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。
    3. **Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。
    4. パッケージを選択し、**インストール** を選択します。

        > [!TIP]
        > すべての Commerce NuGet パッケージ は、このパブリック リポジトリから見つかりません: [https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json](https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json)。

    5. パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加します。 (プロジェクトが作成されていない場合は、新しい nuget.config ファイルを作成します)。

        ```xml
        <packageSources>
            <add key="dynamics365-commerce" value="https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json" />
            <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
            </packageSources>
        ```

7. 次の手順に従って、**tsconfig.json** ファイルをプロジェクトに追加します。

    1. プロジェクト ソリューション エクスプローラーを右クリックし、**追加** を選択してから **新しい項目** を選択します。
    2. **json** を検索し、**TypeScript JSON 構成ファイル** を選択します。 ファイルを **tsconfig.json** に名前を付けて、**追加** を選択します。

        ![tsconfig.json](media/json-file.png)

    3. JSON からすべてのファイルを削除し、**拡張機能** フィールドを追加して、**pos-tsconfig-base** **tsconfig** ファイルから拡張します。 XML ファイルは次の例のようになります。

        ```JSON
        {
            "extends": "./devDependencies/pos-tsconfig-base.json"
        }
        ```

8. プロジェクトを構築し、POS の依存関係をプロジェクト ディレクトリにコピーします。

9. 拡張機能パッケージのマニフェスト ファイルを作成します。

    1. プロジェクト ソリューション エクスプローラーを右クリックし、**追加** を選択してから **新しい項目** を選択します。
    2. **json** を検索し、**JSON ファイル** を選択します。 ファイルを **manifest.json** に名前を付けて、**追加** を選択します。
    3. **manifest.json** の最初の行として次の JSON を追加して、**POS 拡張機能マニフェスト スキーマ** への参照を追加します。

        ```JSON
        {
            "$schema": "./devDependencies/schemas/manifestSchema.json"
        }
        ```

    4. **manifest.json** ファイルでパッケージ情報を追加します。

        + **名前**: 拡張パッケージの名前。
        + **説明**: 拡張機能パッケージの機能の説明。
        + **発行元**: 拡張機能パッケージ発行元または組織の名前。
        + **バージョン**: 拡張機能パッケージのバージョン。 これは、セマンティック バージョニング パターンに従う必要があります。
        + **minimumPosVersion**: この拡張機能パッケージを実行するために必要な最小 POS バージョン。 このバージョン番号は、消費している POS NuGet パッケージと、インストールされている POS アプリケーションによって異なります。 たとえば、拡張機能プロジェクトでは、インストールされている POS アプリよりも古いバージョンの拡張機能アーティファクトである POS アプリを使用しないでください。 実行時に、POS アプリは、拡張機能パッケージのバージョンを確認します。 インストールされている POS アプリよりも高い場合、拡張機能パッケージは読み込まれません。

        これは、マニフェスト ファイルの例です。

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

10. ソリューションに Commerce Runtime 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Commerce Runtime 拡張機能プロジェクトをプロジェクト参照に追加します。

    1. Modern POS プロジェクト ソリューション エクスプローラーを右クリックし、**追加** を選択してから **新しい項目** を選択します。
    2. 参照マネージャの左側にある **プロジェクト** タブを選択します。
    3. Commerce Runtime 拡張機能プロジェクトを選択します。

11. 拡張機能の基本メタデータをすべて作成したら、拡張機能を追加し、**manifest.json** を更新して拡張機能を含めます。 拡張機能 UI とロジックの開発の詳細については、[Dynamics365Commerce.InStore](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension) でサンプルを参照してください。

拡張機能を作成した後、Cloud POS または MPOS に配置する機能拡張をパッケージ化する必要があります。 詳細については、以下を参照してください。

+ [Modern POS 拡張 appx ファイルの作成](create-pos-extension-appx.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
