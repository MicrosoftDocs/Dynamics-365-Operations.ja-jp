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
ms.openlocfilehash: c46888c0236513bd451665676b992e9dd495cef4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355432"
---
# <a name="create-a-pos-extension-package-project"></a>POS 拡張機能パッケージ プロジェクトの作成

[!include [banner](../../includes/banner.md)]

このトピックでは、販売時点管理 (POS) 拡張機能パッケージ プロジェクトの作成方法について説明します。 POS 拡張機能パッケージ プロジェクトは、一連の拡張機能で、組み合わせると、Microsoft Visual Studio を使用するカスタム エンド ツー エンド POS シナリオが有効になります。 POS 拡張機能 パッケージ プロジェクトは、Modern POS (MPOS) と Cloud POS (CPOS) の両方の拡張機能シナリオに適用されます。

1. Visual Studio で、.NET Standard 2.0 で 新しい .NET Standard クラス ライブラリ プロジェクトを作成し、**POS.Extensions** と名前を付けます。
2. プロジェクトと一緒に作成されたクラス ファイルを削除します。
3. カスタマイズ パッケージ内のすべてのプロジェクトが使用する共有プロパティ ファイル (XML ファイル) を作成します。 共有ファイルは、Commerce Runtime (CRT)、Retail Server、および Hardware Service 拡張機能のような異なる Microsoft Dynamics 365 Commerce 拡張機能に使われます。 ファイルに名前をつけます。 この例では、ファイルに **CustomizationPackage.props** と名付けます。
4. 作成したソリューション ファイルと同じディレクトリにファイルを追加します。
5. 次のプロパティ値をファイルに追加します。

    + **PackagePubpur** – パッケージ発行元の ID (たとえば、`CN=Contoso Ltd.`) です。 パッケージに MPOS 拡張機能が含まれている場合、この値は、アプリ署名証明書の件名と一致する必要があります。
    + **PackagePublisherDisplayName** – パッケージ発行元の表示名 (たとえば `Contoso Ltd.`) です。
    + **PackageVersion** – カスタマイズ パッケージのバージョンです。 この値は、メジャー バージョンが 0 (ゼロ) ではない (例えば `1.0.0.0`) であるクアド表記のバージョン文字列である必要があります。
    + **PackageName** – パッケージ名です。 この値は、3 文字から 50 文字の長さの文字列にする必要があり、また、英数字およびピリオドまたはハイフンでのみ構成されている必要があります。 文字列をピリオドで終了することはできません。
    + **PackageDisplayName** – パッケージの表示名です。
    + **PackageDescription** – パッケージの説明です。

    XML ファイルの例を次に示します。

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

6. プロジェクト ファイルを編集し、**インポート** ステートメントを追加し、カスタマイズ パッケージに作成した共有プロパティ (.props) ファイルを含みます。

    ```xml
    <Import Project="..\CustomizationPackage.props" />
    ```

7. プロジェクトの TypeScript サポートを有効にします。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。
    2. **NuGet パッケージ マネージャー** ウィンドウの **閲覧** タブで、**Microsoft.TypeScript.MSBuild** を検索します。
    3. パッケージを選び、**インストール** をから最新の安定したバージョンを選択します。

        > [!TIP]
        > 統合開発環境 (IDE) エクスペリエンスでは、インストールする TypeScript NuGet パッケージのバージョンと一致する Visual Studio の TypeScript ツールのバージョンが必要です。 Microsoft.TypeScript.MSBuild のバージョン 4.2.3 を選択した場合は、Visual Studio の Typescript 4.2.3 をインストールできます。
        >
        > Visual Studio Typescript ツールへのリンクは、[TypeScript/GitHub でリリース](https://github.com/microsoft/TypeScript/releases) で有効です。

8. Retail SDK NuGet パッケージへの参照を追加します。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。
    2. **NuGet パッケージ マネージャー** ウィンドウの **閲覧** タブで、**Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。
    3. パッケージを選択し、**インストール** を選択します。

        > [!TIP]
        > すべての Commerce NuGet パッケージは、次のパブリック リポジトリで見つかります。
        >
        > [https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json](https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json)

    4. パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加します。 (まだ存在しない場合は、プロジェクト用に **nuget.config** ファイルを作成します。)

        ```xml
        <packageSources>
            <add key="dynamics365-commerce" value="https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json" />
            <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
        </packageSources>
        ```

9. プロジェクトに **tsconfig.json** ファイルを追加します。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック)し、**追加** から **新しい項目** を選択します。
    2. **json** を検索し、**TypeScript JSON 構成ファイル** を選択します。
    3. ファイルを **tsconfig.json** に名前を付けて、**追加** を選択します。

        ![tsconfig.json ファイルを追加します。](media/json-file.png)

    4. すべてのフィールドを JavaScript Object Notation (JSON) から削除し、**拡張** フィールドを追加して **pos-tsconfig-base.json** ファイルからファイルを拡張します。 完了すると、XML ファイルは次の例のようになります。

        ```JSON
        {
            "extends": "./devDependencies/pos-tsconfig-base.json"
        }
        ```

10. プロジェクトを構築し、POS の依存関係をプロジェクト ディレクトリにコピーします。
11. 拡張機能パッケージのマニフェスト ファイルを作成します。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック)し、**追加** から **新しい項目** を選択します。
    2. **json** を検索し、**JSON ファイル** を選択します。
    3. ファイルを **manifest.json** に名前を付けて、**追加** を選択します。
    4. **manifest.json** ファイルで、最初の行として次の JSON を追加し POS 拡張機能マニフェスト スキーマに参照を追加します。

        ```JSON
        {
            "$schema": "./devDependencies/schemas/manifestSchema.json"
        }
        ```

    5. 次のパッケージ情報を追加します。

        + **名前** – 拡張機能パッケージの名前です。
        + **説明** – 拡張機能パッケージの機能の説明です。
        + **発行元** – 拡張機能パッケージの発行元または組織の名前です。
        + **バージョン** – 拡張機能パッケージのバージョンです。 この値は、セマンティック バージョニング パターンに続く必要があります。
        + **minimumPosVersion** – 拡張機能パッケージを実行するために必要な最小 POS バージョンです。 バージョン番号は、消費している POS NuGet パッケージと、インストールされた POS アプリによって異なります。 たとえば、拡張機能プロジェクトでは、インストールされている POS アプリよりも古いバージョンから、POS API または 拡張機能アーティファクトを使用しないでください。 ランタイムに、POS アプリは拡張機能パッケージのバージョンを確認します。 インストールされた POS アプリよりも古いバージョンの場合、拡張機能パッケージは読み込まれません。

        こちらは、マニフェスト ファイルの例です。

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

12. ソリューションに CRT 拡張機能プロジェクトが含まれている場合、プロジェクト参照をソリューションの各 CRT 拡張機能プロジェクトに追加します。

    1. ソリューション エクスプローラーで、MPOS を保留 (または右クリック)し、**追加** から **新しい項目** を選択します。
    2. 参照マネージャーの左側の **プロジェクト** タブで、CRT 拡張機能プロジェクトを選択します。

13. 拡張機能の基本メタデータをすべて作成したら、拡張機能を追加し、拡張機能を含むよう **manifest.json** ファイルを更新します。 ユーザー インターフェイス (UI) および拡張機能のロジックを開発する方法については、[GitHub で Dynamics365Storee.InStore](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension) のサンプルを参照してください。

拡張機能の作成が完了したら、CPOS または MPOS に配置できるようパッケージ化する必要があります。 詳細については、[Modern POS 拡張機能パッケージの .appx ファイルを作成](create-pos-extension-appx.md) を参照してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
