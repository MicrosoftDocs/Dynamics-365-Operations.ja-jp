---
title: Cloud Scale Unit 拡張機能パッケージの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce Cloud Scale Unit (CSU) の拡張機能パッケージの作成方法について説明します。
author: mugunthanm
ms.date: 04/21/2022
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 03-30-2022
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 4bd357ace02640721401970a43625c30200b2276
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629721"
---
# <a name="create-a-cloud-scale-unit-extension-package"></a>Cloud Scale Unit 拡張機能パッケージの作成

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce Cloud Scale Unit (CSU) の拡張機能パッケージの作成方法について説明します。 

CSU 拡張機能パッケージには、次のコンポーネントの拡張機能コードが含まれます。

- Commerce Runtime (CRT) およびヘッドレス コマース アプリケーション プログラミング インターフェイス (API)
- チャネル データベース拡張機能スクリプト
- 支払コネクタ
- クラウド POS (CPOS)

## <a name="create-a-csu-package"></a>CSU パッケージを作成する

CSU パッケージを作成するには、次のいずれかのオプションを選択し、手順に従います。

### <a name="option-1-download-the-sample-scale-unit-packaging-project-from-github"></a>オプション 1: GitHub からスケール ユニット パッケージ プロジェクトのサンプルをダウンロードする

1. [Dynamics365 Commerce ScaleUnit サンプル](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)からスケール ユニット パッケージ プロジェクトを複製またはダウンロードします。 ソフトウェア開発キット/アプリケーション リリースのバージョンに適切なリリース ブランチ バージョンを選択します。 プロジェクトを複製する方法の詳細については、[GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](retail-sdk/sdk-github.md)を参照してください。
1. CRT 拡張、Retail Server、チャネル データベース、および CPOS 拡張機能プロジェクトをプロジェクト参照としてスケール ユニット パッケージ プロジェクトに追加します。
1. CRT または Retail Server の拡張機能が、実行にいずれかのアセンブリに依存する場合は、それらのアセンブリをプロジェクト参照として拡張機能プロジェクトに含めます。 パッケージの **ext** フォルダーにこれらのアセンブリは含まれます。 ランタイム エラーが発生する可能性があるため、依存アセンブリを **CommerceRuntime.Ext.config** ファイルには追加しないでください。
1. スケール ユニット プロジェクトを構築します。 プロジェクトは、プロジェクト ビン出力フォルダーに **CloudScaleUnitExtensionPackage.zip** 出力パッケージを生成します。 その後、**CloudScaleUnitExtensionPackage.zip** パッケージを Microsoft Lifecycle Services (LCS) にアップロードし、CSU に配置できます。 Visual Studio NuGet パッケージ マネージャーで、使用している SDK/ アプリケーションのバージョンに適した **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet バージョンを選択します。

### <a name="option-2-create-a-new-scale-unit-packaging-project"></a>オプション 2: 新しいスケール ユニット パッケージ プロジェクトを作成する

1. ターゲット フレームワークが .NET Standard 2.0 の、新しい C\# クラス ライブラリ プロジェクトを作成します。
1. 依存関係として **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet パッケージをプロジェクトに追加します。 使用している SDK/ アプリケーションのバージョンに適した **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet バージョンを選択します。
1. [https://pkgs.dev.azure.com/commerce-partner/Registry/\_packaging/dynamics365-commerce/nuget/v3/index.json](https://pkgs.dev.azure.com/commerce-partner/Registry/\_packaging/dynamics365-commerce/nuget/v3/index.json) から、**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** パッケージを使用します。 次の例にあるとおり、パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加できます。

    ```xml
    <packageSources>
        <add key="dynamics365-commerce" value="https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json" />
        <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
        </packageSources>
    ```

1. CRT 拡張、Retail Server、チャネル データベース、および CPOS 拡張機能プロジェクトをプロジェクト参照としてスケール ユニット パッケージ プロジェクトに追加します。
1. CRT または Retail Server の拡張機能が、実行にいずれかのアセンブリに依存する場合は、それらのアセンブリをプロジェクト参照として拡張機能プロジェクトに含めます。 パッケージの **ext** フォルダーにこれらのアセンブリは含まれます。 ランタイム エラーが発生する可能性があるため、依存アセンブリを **CommerceRuntime.Ext.config** ファイルには追加しないでください。
1. スケール ユニット プロジェクトを構築します。 プロジェクトは、プロジェクト ビン出力フォルダーに **CloudScaleUnitExtensionPackage.zip** 出力パッケージを生成します。 その後、**CloudScaleUnitExtensionPackage.zip** パッケージを LCS にアップロードし、CSU に配置できます。

CRT 拡張コンフィギュレーション ファイル (**Web.Config**) は、スケール ユニット パッケージ プロジェクトによって生成されます。 拡張コンフィギュレーション ファイルを手動で作成する必要はありません。

## <a name="deploy-the-package-to-csu"></a>CSU にパッケージを配置する

パッケージを CSU に配置するには、以下の手順に従います。

1. [LCS](https://lcs.dynamics.com/v2) にサインインして、プロジェクトを開きます。
1. **メニュー** ボタン (ハンバーガー メニューまたはハンバーガー ボタンと呼ばれる場合もあります) を選択してから、**資産ライブラリ** を選択します。
1. 資産タイプとして **Commerce Cloud Scale Unit Extension** を選択し、プラス記号 (**+**) ボタンを選択してパッケージをアップロードします。
1. パッケージの名前と説明を入力し、**ファイルの追加** を選択してパッケージ ファイルを追加します。
1. アップロードが完了したら、**確認** を選択してアップロード プロセスを完了します。

    LCS がパッケージを検証します。 この検証には数分かかります。

1. 検証が完了したら、パッケージを **リリース候補** としてマークします。
1. パッケージがアップロードされたら、環境に配置する必要があります。 詳細については、[Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)の手順に従ってください。
