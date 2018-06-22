---
title: "Retail SDK 小売パッケージ"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の小売展開可能なパッケージを作成する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 2df0a58ece10b9d9baaa0513e4193bb2dec9f428
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="retail-sdk-packaging"></a>Retail SDK 小売パッケージ

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations の小売展開可能なパッケージを手動で作成する方法について説明します。

Retail の展開可能なパッケージは、次の小売コンポーネントがすべて含まれるバンドル パッケージです。

-   Commerce Runtime (CRT)
-   Retail サーバー
-   Modern POS
-   クラウド POS
-   ハードウェア ステーション
-   チャネル データベース スクリプト

Retail ソフトウェアの開発キット (SDK) に関する詳細については、[Retail SDK の概要](retail-sdk-overview.md) を参照してください。 

## <a name="retail-deployable-package"></a>配置可能小売パッケージ
小売展開可能なパッケージは、LCS 展開サービスで使用できる資産です。またはサービスまたはカスタマイズのインストールに手動で配置することができます。 Retail SDK は、既存のソリューションに更新プログラムおよびカスタマイズをインストールまたは展開する 1 つの方法が確保されるように、Microsoft 修正プログラムまたは更新プログラム用に開発されたのと同じパッケージを生成します。

### <a name="steps-to-create-a-retail-deployable-package"></a>Retail の展開可能パッケージを作成する手順

Retail 展開可能パッケージを生成するには、2 つの方法があります。 1 つは小売ビルドの自動化を使用するか、または手動で小売 SDK のビルド ツールを使用します。 このトピックでは、手動での方法について焦点を当てます。
1. 小売スタックに機能をカスタマイズまたは追加します。
2. ビルド ツールを使用して、カスタマイズされたインストール パッケージに ID を与え、コードサインし、カスタマイズされた CRT、リテール サーバー、カスタマイズされたハードウェア ステーション アセンブリ、カスタマイズされたデータベース スクリプトを指定します。
3. すべての設定が Retail SDK\BuildTools フォルダーの Customization.settings ファイルで指定された後、VS dev コマンド プロンプト ツールを使用して Retail SDK フォルダーのルートで **msbuild/t:rebuild** を実行して、配置可能小売パッケージを生成します。 パッケージを作成する前に、カスタマイズしたすべてのアセンブリを Retail SDK\References フォルダーに配置し、commerceruntime.config、CommerceRuntime.MPOSOffline.config、dllhost.exe.config などの変更された構成ファイルを Retail SDK\Assets フォルダーに配置します。

## <a name="retail-sdk-build-tools--customization-settings"></a>Retail SDK ビルド ツール: カスタマイズ設定
BuildTools\Customization.setting ファイルは、Retail SDK のコンフィギュレーション値のほとんどがビルドとパッケージのために設定されています。 これらの値は、バイナリ、コンポーネント、パッケージの名前付け、バージョン管理、コード署名の方法を制御します。 このメタデータを定義した後、Retail SDK ビルド システムは資産に ID を付与するためにそれらを使用し、すべての Retail コンポーネントのカスタマイズ資産をパッケージ化します。

次のコンフィギュレーションの一覧は、Customization.Settings ファイルで使用できます。
-   **AssemblyNamePrefix** - アセンブリの接頭語名を指定します。 Retail SDK を作成するときは、すべてのアセンブリに接頭辞としてこの名前が付きます。
-   **CustomAssemblyVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム アセンブリ バージョンを指定します。
-   **CustomVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム ファイル バージョンを指定します。
-   **CustomName** - アセンブリのカスタム名を指定します。
-   **CustomDescription** - アセンブリの説明を指定します。
-   **CustomPublisher** – アセンブリの発行元を指定します。
-   **CustomPublisherDisplayName** - アセンブリの著作権を指定します。
-   **SignAssembly** – ビルド時にアセンブリに署名する場合 **はい** を指定してください。
-   **DelaySign** - ビルド中にアセットの署名を延期する場合は、**True** を指定します。
-   **AssemblyOriginatorKeyFile** - アセンブリに署名するために使用する厳密な名前キーを指定します。
-   **ModernPOSPackageCertificateKeyFile** – Modern POS とハードウェア ステーションの署名に使用する PFX ファイルを指定します。
-   **RetailServerLibraryPathForProxyGeneration** – プロキシの生成に使用するカスタマイズされた Retail サーバー アセンブリを指定します (TypeScript と C\# プロキシの両方)。
-   **ItemGroup** セクション:
    -   **ISV\_CommerceRuntime\_CustomizableFile** – すべてのカスタマイズされた CRT アセンブリを指定します。 カスタマイズされた各 CRT アセンブリに対して 1 つずつ、複数のエントリを持つことができます。
    -   **ISV\_RetailServer\_CustomizableFile** – カスタマイズされたすべての Retail サーバー アセンブリを指定します。 カスタマイズされた各 Retail サーバー アセンブリに対して 1 つの、複数のエントリを持つことができます。
    -   **ISV\_HardwareStation\_CustomizableFile** – カスタマイズされたすべてのハードウェア ステーション アセンブリを指定します。 カスタマイズされた各ハードウェア ステーション アセンブリに対して 1 つずつ、複数のエントリを持つことができます。
    -   **ISV\_CustomDatabaseFile\_Upgrade\_Custom** – カスタマイズされたすべてのデータベース スクリプトを指定します。


#### <a name="retail-reployable-package"></a>配置可能小売パッケージ

### <a name="crt-extension-assemblies"></a>CRT 拡張アセンブリ
既定では、CRT が個別に配置されないため、個々の小売コンポーネントの個別パッケージはありません。代わりに、CRT 資産は Modern POS、Retail サーバー、および Microsoft Dynamics 365 for Operations HQ などの他のアプリケーション コンポーネントと共にパッケージ化されます。 Retail SDK のビルド ツールが使用されているすべてのコンポーネントで CRT をパッケージ化するためには、次の構成エントリを行う必要があります。

1.  **CRT 拡張アセンブリ** - これらは、CRT 拡張を記述した新しいアセンブリになります。 Retail SDK\\BuildTools\\Customization.settings で CRT 拡張アセンブリのエントリを指定します。 

    [![crt-customization 設定](./media/crt-customization-settings.png)](./media/crt-customization-settings.png)
    
2.  **CRT commerceruntime.config ファイル** - 新しい CRT アセンブリがある場合は、CRT コンフィギュレーション ファイルに追加して、ランタイムが読み込めるようにする必要があります。 Retail SDK\\References\\commerceruntime.config で CRT 拡張アセンブリのエントリを指定します。 

    [![crt-config](./media/crt-config.png)](./media/crt-config.png)

#### <a name="retail-server-extension-assemblies"></a>Retail サーバーの拡張機能アセンブリ
1.  **Retail サーバー拡張アセンブリ** – これらは Retail サーバーのカスタマイズを記述した新しいアセンブリです。 Retail SDK\\BuildTools\\Customization.settings で CRT 拡張アセンブリのエントリを指定します。 

    [![小売サーバー カスタマイズの設定](./media/retail-server-customization-setting.png)](./media/retail-server-customization-setting.png)
    
2.  **Retail サーバー web.config ファイル** – Retail サーバー拡張アセンブリのエントリを Retail サーバーの web.config ファイルに追加し、読み込んで使用する必要があります。 Retail SDK\\Packages\\RetailServer\\Code\\web.config で Retail Server 拡張アセンブリのエントリを指定します。 

    [![小売サーバーの web config](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)

##### <a name="database-scripts"></a>データベース スクリプト
カスタマイズの一環として、 Modern POS のオフライン データベースに加えてチャネル データベースをアップグレードする必要があります。 現在、アップグレード SQL スクリプトを使用して、チャネルおよび Modern POS オフライン データベースをアップグレードしています。 アップグレード SQL スクリプトを記述し、それを Retail SDK\Database\Upgrade\Custom に配置できるので、パッケージ化ツールではそれをピッキングし、適切なコンポーネント (Retail サーバーと Modern POS オフライン) の配置可能なパッケージに含めることができます。 

[![カスタム db スクリプト](./media/custom-db-script.png)](./media/custom-db-script.png) また、Retail SDK\\BuildTools\\Customization.settings を更新して、データベース用にパッケージ化するファイルをビルドツールに入力します。 

[![データベース アップグレードのカスタマイズ設定](./media/database-upgrade-customization-setting-1024x311.png)](./media/database-upgrade-customization-setting.png) データベース スクリプトは、Retail サーバーおよび Modern POS オフライン パッケージとともにパッケージ化され、Retail Server および Modern POS がインストールされたときに実行されます。 複数のカスタム データベース スクリプトがある場合は、アルファベット順に実行されます。 したがって、スクリプトを特定の順序で実行する場合は、それに応じて名前を付ける必要があります。 CRT.RETAILUPGRADEHISTORY テーブルは、データベースに既に適用されているスクリプトを追跡します。 したがって、次のデータベース アップグレードは、CRT.RETAILUPGRADEHISTORY テーブルに項目がないアップグレード スクリプトのみを実行します。

## <a name="generate-a-retail-deployable-package"></a>配置可能小売パッケージを生成

Retail SDK は、msbuild を完全にサポートしています。 Retail SDK をビルドするには、管理者として **Visual studio 2015 開発者コマンド プロンプト ツール** ウィンドウを開き、**msbuild**を実行します (または、非デバッグ バージョンの場合は **msbuild /p:Configuration=Release** を実行します)。 

### <a name="packages"></a>パッケージ

ビルドが完了した後、Retail SDK\Packages\RetailDeployablePackage フォルダーに、配置可能小売パッケージ (RetailDeployablePackage.zip) が生成されます。 注記: Retail 用の個別パッケージはなく、すべては RetailDeployablePackage と呼ばれる 1 つのバンドル パッケージとして結合され作成されます。
      
 ## <a name="deploy-the-retail-deployable-packages"></a>小売展開可能パッケージを配置する
 
手動または LCS 自動化フローを使用してパッケージを展開するには、[[展開可能なパッケージを適用する](../../../dev-itpro/deployment/apply-deployable-package-system.md)] および [[展開可能なパッケージをインストールする](../../../dev-itpro/deployment/install-deployable-package.md)] のトピックを参照してください。

