---
title: "Retail SDK パッケージ"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の配置可能小売パッケージを作成する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: 0fa3c8e7-49e4-417d-afe9-fa2055f6546f
ms.search.region: Global
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6c6c7c3f63b7a49820811a7ec80248b09b6e3acf
ms.openlocfilehash: 37dfe38c7e7912503133a41ce600f0d3543d6e39
ms.contentlocale: ja-jp
ms.lasthandoff: 06/19/2018

---

# <a name="retail-sdk-packaging"></a>Retail SDK パッケージ

[!include [banner](../../includes/banner.md)]

このトピックでは、次のような Retail コンポーネントの拡張機能のカスタマイズをパッケージ化し、Microsoft Dynamics Lifecycle Services (LCS) を使用して、パッケージを環境に配置する方法について説明します。

- Commerce Runtime (CRT)
- Retail プロキシ
- Retail サーバー
- Modern POS
- クラウド POS
- ハードウェア ステーション
- チャネル データベース スクリプト
- 支払コネクタ
- Retail Store スケール ユニット
- ハイブリッド アプリ (IOS および Android POS アプリ)

## <a name="retail-deployable-package"></a>配置可能小売パッケージ
小売可能なパッケージは、配置に必要なすべてのメタデータと共に、すべてのカスタマイズを含む 1 つの結合されたパッケージです。 この小売展開可能パッケージを使用して、カスタマイズをさまざまな環境に展開できます。 LCS で自動フローを使用して、配置を行うことができます。またはパッケージ内に用意されているスクリプトを使用して手動で行うことができます。 このトピックでは、配置可能小売パッケージを生成するプロセスを説明します。

> [!IMPORTANT]
> Retail コンポーネントのすべてのカスタマイズは、1 つの配置可能なパッケージとして提供されます。 Finance and Operations は、Modern POS、Cloud POS、Retail Store Scale Unit、CRT、Retail Server といった、個々の Retail コンポーネントの個別のパッケージをサポートしていません。 独立したソフトウェア ベンダー (ISV) またはさまざまなパートナーの拡張機能をマージまたは結合する必要がある場合でも、すべての拡張機能を単一の小売展開可能パッケージとしてパッケージする必要があります。
>
> アプリケーション バージョン 7.1.1541.3036 よりも古い Retail ソフトウェア開発キット (SDK) のバージョンを使用して、カスタマイズが個々の Retail コンポーネント パッケージとして構築されパッケージ化された場合、パッケージは LCS の展開に対してサポートされなくなりました。 [KB 4015062](https://fix.lcs.dynamics.com/Home/Index/0/kb/4015062?permission=Download) で修正プログラムを取得する必要があります。その際、カスタマイズはリビルドおよび再梱包されます。

Retail SDK の詳細情報は、[Retail SDK 概要](retail-sdk-overview.md) を参照してください。

### <a name="steps-to-create-a-retail-deployable-package"></a>小売展開可能パッケージを作成する手順
小売展開可能パッケージを生成するには、2 つの方法があります。 Retail ビルドの自動化を使用することができます。または Retail SDK のビルド ツールを使用し、手動でパッケージを生成することもできます。 このトピックでは、手動メソッドを対象としています。

1. 小売スタックに機能をカスタマイズまたは追加します。
2. ビルド ツールを使用して、カスタマイズされたインストール パッケージを識別して、コードサインし、カスタマイズされた CRT、Retail サーバー、ハードウェア ステーション アセンブリ、カスタマイズされたデータベース スクリプトを指定します。
3. すべての設定が **...\\Retail SDK\\BuildTools** フォルダーの **Customization.settings** ファイルで指定された後、Retail SDK フォルダーのルートで **msbuild /t:rebuild** を起動します。 配置可能小売パッケージを生成するために、MSBuild ビルド ツールまたは Microsoft Visual Studio 開発者コマンド ライン ツールのいずれかを使用することができます。 パッケージを作成する前に、すべてのカスタマイズされたアセンブリを、**...\\Retail SDK\\References** フォルダに保存します。 さらに、**...\\Retail SDK\\Assets** フォルダーの **CommerceRuntime.Ext.config**、**CommerceRuntime.MPOSOffline.Ext.config**、 **HardwareStation.Extension.config**、および **RetailProxy.MPOSOffline.ext.config** のような変更済の構成ファイルを入力します。

## <a name="retail-sdk-build-tools--customization-settings"></a>Retail SDK ビルド ツール: カスタマイズ設定
カスタマイズを構築しパッケージ化するために Retail SDK が使用するコンフィギュレーション値のほとんどが BuildTools\\Customization.setting files で設定されます。 これらの値は、バイナリ、コンポーネント、パッケージの名前付け、バージョン管理、コード署名の方法を制御するメタデータを定義します。 このメタデータを定義した後、Retail SDK ビルド システムはカスタマイズ資産を識別し、すべての Retail コンポーネントのためにカスタマイズ資産をパッケージ化します。

次のコンフィギュレーション設定は、 Customization.settings ファイルで使用できます。

- **AssemblyNamePrefix** - アセンブリの接頭語名を指定します。 Retail SDK を作成するときは、すべてのアセンブリに接頭辞としてこの名前が付きます。
- **CustomAssemblyVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム アセンブリ バージョンを指定します。
- **CustomVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム ファイル バージョンを指定します。
- **CustomName** - アセンブリのカスタム名を指定します。
- **CustomDescription** - アセンブリの説明を指定します。
- **CustomPublisher** – アセンブリの発行元を指定します。
- **CustomPublisherDisplayName** - アセンブリの著作権を指定します。
- **SignAssembly** – ビルド時にアセンブリに署名するには**はい**を指定してください。
- **DelaySign** – ビルド中にアセットの署名を延期するには **True** を指定します。
- **AssemblyOriginatorKeyFile** - アセンブリに署名するために使用する厳密な名前キーを指定します。
- **ModernPOSPackageCertificateKeyFile** – Modern POS とハードウェア ステーションの署名に使用する個人情報交換 (PFX) ファイルを指定します。
- **RetailServerLibraryPathForProxyGeneration** – プロキシの生成に使用するカスタマイズされたRetail サーバー アセンブリを指定します (TypeScript と C\# プロキシの両方)。

    7.1 以前のバージョンでは、ここで Retail サーバー アセンブリの名前を指定する必要があります。

    7.2 以降のバージョンでは、プロキシ生成の commerce ジェネレーター ツールを使用します。 ただし、E コマース クライアント側でプロキシを使用している場合は、ここでアセンブリ名を指定してください。

- **ItemGroup** セクションには、次の設定が含まれます。

    - **ISV\_CommerceRuntime\_CustomizableFile** – すべてのカスタマイズされた CRT アセンブリの詳細を指定します。 各 CRT アセンブリに対して 1 つずつ、複数のエントリを持つことができます。

        **例**

        ```
        ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\MyCrtExtension.dll"
        ```

    - **ISV\_RetailServer\_CustomizableFile** – カスタマイズされたすべての Retail サーバー アセンブリの詳細を指定します。 各 Retail サーバー アセンブリに対して 1 つの、複数のエントリを持つことができます。

        **例**

        ```
        ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\MyRetailServerExtension.dll"
        ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\MyRetailServerExtension2.dll"
        ```

    - **ISV\_RetailProxy\_CustomizableFile** – カスタマイズされたすべての Retail プロキシ アセンブリの詳細を指定します。 各 Retail プロキシ アセンブリに対して 1 つの、複数のエントリを持つことができます。 

        **例**

        ```
        ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\MyRetailProxyExtension.dll"
        ```

    - **ISV\_HardwareStation\_CustomizableFile** – カスタマイズされたすべてのハードウェア ステーション アセンブリの詳細を指定します。 カスタマイズされた各ハードウェア ステーション アセンブリに対して 1 つずつ、複数のエントリを持つことができます。

        **例**

        ```
        ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\MyHardwareStationExtension.dll"
        ```

    - **ISV\_CustomDatabaseFile\_アップグレード\_カスタム** – カスタマイズされたすべてのデータベース スクリプトの詳細を指定します。

        **例**

        ```
        ISV_CustomDatabaseFile_Upgrade_Custom Include="$(SdkRootPath)\Database\Upgrade\Custom\SqlUpdatev1.sql"
        ```

> [!IMPORTANT]
> ビルド プロセスを開始する前に、拡張アセンブリを \\Retail SDK\\References に、カスタム データベース スクリプトを \\RetailSDK\\Database\Upgrade\\Custom に配置する必要があります。

### <a name="database-scripts"></a>データベース スクリプト
データベース スクリプトは、Retail サーバーおよび Modern POS オフライン パッケージとともにパッケージ化され、Retail Server および Modern POS がインストールされたときに実行されます。 複数のカスタム データベース スクリプトがある場合は、アルファベット順に実行されます。 したがって、スクリプトを特定の順序で実行したい場合は、それに応じて名前を付ける必要があります。 CRT.RETAILUPGRADEHISTORY テーブルは、データベースに既に適用されているスクリプトを追跡します。 したがって、次のパッケージ アップグレードは、CRT.RETAILUPGRADEHISTORY テーブルに項目がないアップグレード スクリプトのみを実行します。

## <a name="update-the-extension-configuration-files"></a>拡張機能の構成ファイルを更新します
CRT、Retail Server、ハードウェア ステーション、またはプロキシに新しい拡張機能がある場合は、関連する拡張構成ファイルの\<構成\>セクションに拡張アセンブリの詳細を登録する必要があります。 すべての拡張設定ファイルは次で見つけることができます。\\RetailSDK\\資産フォルダ。 すべての拡張機能は拡張ファイルの情報に基づいて読み込まれるため、アセンブリを登録する必要があります。

パッケージを行う前に、次の構成ファイルを更新する必要があります (この領域でカスタマイズがある場合)。

- **CommerceRuntime.Ext.config** – すべての CRT 拡張アセンブリを登録します。

    **例**

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <!-- Register your own assemblies here. -->
            <add source="assembly" value="my custom library" />
        </composition>
    </commerceRuntimeExtensions>
    ```

- **CommerceRuntime.MPOSOffline.Ext.config** – オフラインで、すべての CRT 拡張機能を登録します。

    **例**

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <!-- Register your own assemblies or types here. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </commerceRuntimeExtensions>
    ```

- **HardwareStation.Extension.config** – すべてのハードウェア ステーション拡張機能を登録します。

    **例**

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <hardwareStationExtension>
        <composition>
            <! -- Register your own assemblies or types here. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </hardwareStationExtension>
    ```

- **RetailProxy.MPOSOffline.ext.config** – すべての小売プロキシ拡張機能を登録します。

    **例**

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <retailProxyExtensions>
        <composition>
            <!-- Register your own proxy extension assemblies. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </retailProxyExtensions>
    ```

### <a name="retail-server-extension-assemblies"></a>Retail サーバーの拡張機能アセンブリ
パッケージを開始する前に、Retail Server web.config file の \<extensionComposition\> に、Retail Server 拡張アセンブリのエントリを追加する必要があります。これにより、アセンブリがロードされ、使用できるようになります。 web.config ファイルは、Retail SDK\\パッケージ\\RetailServer\\ コード フォルダーで検索できます。

次の図は、Retail サーバーの Web.config ファイルの例を示します。

[![Retail サーバーの Web.config ファイル](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)

## <a name="generate-a-retail-deployable-package"></a>配置可能小売パッケージを生成
配置可能小売パッケージを生成するには、MSBuild ビルド コマンド プロンプト ウィンドウを開きます。 (開発者仮想マシンの、**開始**メニューで **msbuild** を検索します。) そして、次のコマンドを実行します。

```
msbuild /p:Configuration=Release
```

Microsoft Visual Studio 2015 開発者コマンド ライン ツールで同じコマンドを実行することもできます。

### <a name="packages"></a>パッケージ
ビルドが完了した後、Retail SDK\\Packages\\RetailDeployablePackage フォルダーに、配置可能小売パッケージ が zip ファイルとして (RetailDeployablePackage.zip) が生成されます。

> [!NOTE]
> さまざまな Retail コンポーネントを別々のパッケージにすることはありません。 すべてのパッケージは、RetailDeployablePackage という名の 1 つのバンドル パッケージに結合されます。

## <a name="deploy-the-retail-deployable-packages"></a>小売展開可能パッケージを配置する
手動または LCS 自動化フローを使用してパッケージを配置する方法については、[配置可能なパッケージを適用する](../../../dev-itpro/deployment/apply-deployable-package-system.md)および[配置可能なパッケージをインストールする](../../../dev-itpro/deployment/install-deployable-package.md)を参照してください。

