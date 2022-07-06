---
title: Microsoft ホステッド エージェントと Azure Pipelines を使用するビルドの自動化
description: この記事では、Microsoft Azure DevOps でエージェントにおける X++ のビルド プロセスを自動化する方法について説明します。
author: jorisdg
ms.date: 03/05/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f42e17d5930b5c863c5c0bd4325b9b5b50b3ead5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867060"
---
# <a name="build-automation-that-uses-microsoft-hosted-agents-and-azure-pipelines"></a>Microsoft ホステッド エージェントと Azure Pipelines を使用するビルドの自動化

[!include [banner](../includes/banner.md)]

Microsoft Windows で実行される任意のビルド エージェントで、X++ コードのビルドと配置可能なパッケージの作成プロセスを自動化できます。 これらのエージェントには、[Microsoft-ホステッド エージェント](/azure/devops/pipelines/agents/hosted)が含まれています。 この方法は、ビルド バーチャル マシン (VM) の配置の設定、保守、およびコストを回避するのに役立ちます。 また、ビルド エージェントの既存の設定を再利用して、他の .NET ビルド自動化を実行することもできます。

> [!NOTE]
> この機能は、コンパイルとパッケージングに限定されています。 このランタイムを必要とする X++ 単体テスト (SysTest)、データベースの同期、またはその他の機能 (Application Object Server \[AOS \]) やそのコンポーネントはサポートされていません。

## <a name="prerequisites-for-building-x-code"></a>X++ コードをビルドするための前提条件

### <a name="build-projects"></a>プロジェクトのビルド

Azure DevOps での X++ のビルドに .NET ツールを使用するには、Microsoft Build Engine (MSBuild) とカスタム X++ のターゲットが使用されます。 X++ ソース コード レポジトリには、ビルドする各パッケージの X++ プロジェクトが含まれている必要があります。 オプションで、ソリューション ファイルを使用して、C# プロジェクトの依存関係を含むプロジェクトをグループ化したり、明示的なビルド順序を指定したりできます。 リポジトリにプロジェクトがまだ含まれていない場合は、Visual Studio にプロジェクトを作成できます。

> [!NOTE]
> 既存の X++ プロジェクト (rnrproj) を使用する場合は、プラットフォーム更新プログラム 27 以降の Visual Studio ツールを使用して、それを作成するか、または開いて保存しておく必要があります。
>
> 1 つのパッケージには複数のモデルを含めることができますが、常に完全にビルドする必要があります。 したがって、パッケージ全体をビルドするために必要なプロジェクトは 1 つだけです。 また、プロジェクトにはオブジェクトを含める必要はありませんが、プロジェクトに含めることができます。

### <a name="nuget-packages"></a>NuGet パッケージ

X++ コードをビルドするには、X++ コンパイラ (xppc.exe) などの基本的な開発者ツールを実行する必要があります。 また、アプリケーション プラットフォームやアプリケーション スイートなどの参照先パッケージは、コンパイルされた形式で使用できる必要があります。 このプロセスを有効にするために、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリには、X++ ビルドを実行するために必要な NuGet パッケージが用意されています。

次のパッケージは、共有アセット ライブラリからダウンロードできます。

- **Microsoft.Dynamics.AX.Platform.CompilerPackage** – このパッケージには、ビルドを実行するために必要な X++コンパイラおよび関連ツールが含まれています。
- **Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp** – このパッケージには、アプリケーション プラットフォームおよび関連モジュールのコンパイル済み X++ コードが含まれています。 このコードは、ビルドに対して最適化されています。
- **Microsoft.Dynamics.AX.Application.DevALM.BuildXpp** – このパッケージには、アプリケーションおよび関連モジュールのコンパイル済み X++ コードが含まれています。 このコードは、ビルドに対して最適化されています。

バージョン 10.0.18 から、アプリケーション スイート パッケージは 2 つのパッケージに分割され、共有アセット ライブラリからダウンロードする追加のパッケージがあります。

- **Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp** – このパッケージには、アプリケーション スイート モジュールのコンパイル済み X++ コードが含まれています。 このコードは、ビルドに対して最適化されています。

これらのパッケージを LCS からダウンロードし、ビルドを実行する Azure DevOps 組織内の Azure コンポーネント フィードに追加し ます。 Azure コンポーネントを作成し、NuGet パッケージを追加する方法の詳細については、次のトピックを参照してください。

- [Azure DevOps サービスおよび TFS の NuGet パッケージの使用を開始する](/azure/devops/artifacts/get-started-nuget)
- [フィードの作成](/azure/devops/artifacts/get-started-nuget#create-a-feed)
- [独自の NuGet パッケージの作成と公開](/azure/devops/artifacts/get-started-nuget#create-and-publish-your-own-nuget-package)

> [!NOTE]
> 無料の Azure DevOps 組織には、Azure コンポーネントの限られたストレージしかありません。 ストレージ容量を解放するために、古いバージョンと使用していないバージョンを削除することを検討してください。 詳細については、[Azure コンポーネントのサインアップ](/azure/devops/artifacts/start-using-azure-artifacts#billing-and-free-monthly-usage) を参照してください。

ビルド中に使用する必要があるパッケージを特定するには、ビルド時に nuget.exe ファイルと packages.config ファイルを用意する必要があります。 これらのファイルを作成し、ソース管理リポジトリに追加することをお勧めします。 これらのファイルのパスは NuGet コマンドの明示的な入力であるため、ソース管理内の任意の場所にファイルを格納でき ます。

nuget.exe ファイルには、パッケージが格納されているソース フィードを持つ NuGet が含まれています。 packages.config ファイルでは、パッケージとそのバージョンが指定されています。 新しいバージョンに対してビルドする場合は、packages.config ファイルのバージョンを更新するだけで済みます。 サンプルの nuget.config ファイルを含む詳細については、[Azure Pipelines でのパッケージ管理 NuGet パッケージの復元](/azure/devops/pipelines/packages/nuget-restore)を参照してください。

次の例は、一般的な X++ ビルドに必要な 3 つの主要なパッケージのための、**packages.config** ファイルを示しています。 一覧のバージョンを実際のバージョンの NuGet パッケージに置き換える必要があります。

+ バージョン 10.0.17 以前の場合は、次の packages.config レイアウトを使用します。

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <packages>
        <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5644.16778" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.464.13" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5644.16778" targetFramework="net40" />
    </packages>
    ```

+ バージョン 10.0.18 以降の場合は、次の packages.config レイアウトを使用します。

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <packages>
        <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5968.16973" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5968.16973" targetFramework="net40" />
    </packages>
    ```

## <a name="creating-the-pipeline"></a>パイプラインの作成

Azure DevOps は、ビルドを自動化するために使用できるパイプラインを提供します。 パイプラインには、YML と Classic の 2 つのタイプがあります。 YML パイプラインは、Git ソース管理リポジトリを使用している場合にのみ使用できます。 Classic パイプラインを使用して、Team Foundation バージョン管理 (TFVC) リポジトリをビルドする必要があります。 詳細については、 [Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) を参照してください。

このセクションでは、パイプラインで X++ コードを作成するために必要な手順について説明します。 [Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリでは、既存の Azure DevOps プロジェクトにインポートできるサンプル パイプラインを見つけることができます。

### <a name="creating-a-basic-build-pipeline"></a>基本的なビルド パイプラインの作成

X++ をコンパイルするための基本パイプラインには、2 つの手順が必要です。

1. NuGet パッケージをインストールします。
2. ソリューションまたはプロジェクトをビルドします。

抽出された NuGet パッケージの使用を容易にするために、**NuGet インストール** オプションを使用して、**-ExcludeVersion** [NuGet コマンドライン オプション](/nuget/reference/cli-reference/cli-ref-install#options)を指定することを検討してください。 このようにして、パッケージのバージョンに関係なく、抽出されたパッケージ パスをビルドで使用できます。 **NuGet インストーラー** タスクを使用し、**インストールの種類** フィールドを **インストール** に設定します。 最後に、前の手順で作成した packages.config ファイルと nuget.config ファイルのパスを指定します。

次の NuGet 引数の例では、パッケージ バージョンに対してサブフォルダーが作成されないようにし、NuGet パッケージを **$(Pipeline.Workspace)\\NuGets** に展開します。

`-ExcludeVersion -OutputDirectory "$(Pipeline.Workspace)\NuGets"`

MSBuild を使用して X++ をビルドするには、いくつかの引数を指定する必要があります。 ソリューションをビルドするパイプライン ステップでは、これらの引数を **MSBuild 引数** フィールドで指定できます。

| 引数 | 説明 |
| --- | --- |
| /p:BuildTasksDirectory | 抽出されたコンパイラ ツール NuGet パッケージのパス (DevAlm フォルダー内のサブフォルダを含む)。 |
| /p:MetadataDirectory | X++ ソース コードのパス。 |
| /p:FrameworkDirectory | 抽出されたコンパイラ ツール NuGet パッケージのパス。 |
| /p:ReferenceFolder | コンパイルで参照され、必須である X++ パッケージのバイナリを含むパスのセミコロン区切りのリスト (アプリケーション プラットフォームやアプリケーション スイートなど)。 コンパイルするコードに互いを参照する複数のパッケージがある場合は、出力ディレクトリもここに含める必要があります。 |
| /p:ReferencePath | コンパイル時に参照され、必須である X++ 以外のすべてのバイナリを含むパスのセミコロン区切りのリスト。 必要な参照が含まれている場合があるため、抽出したコンパイラ ツール NuGet パッケージの場所を含める必要があります。 |
| /p:OutputDirectory | コンパイラがフォルダーとバイナリを作成するパス。 |

次の MSBuild 引数の例では、NuGet パッケージが **$(Pipeline.Workspace)\\NuGets** にインストールされており、X++ のソース コードが **$(Build.SourcesDirectory)\\Metadata** 内にあり、コンパイラの出力を **$(Build.BinariesDirectory)** にする必要があることを前提としています。

+ バージョン 10.0.17 以前の場合は、次の引数を使用します。

    ```dos
    /p:BuildTasksDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage\DevAlm"
    /p:MetadataDirectory="$(Build.SourcesDirectory)\Metadata"
    /p:FrameworkDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage"
    /p:ReferenceFolder="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp\ref\net40;$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Application.DevALM.BuildXpp\ref\net40;$(Build.SourcesDirectory)\Metadata;$(Build.BinariesDirectory)"
    /p:ReferencePath="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage" /p:OutputDirectory="$(Build.BinariesDirectory)"
    ```
    
+ バージョン 10.0.18 以降の場合は、次の引数を使用します。

    ```dos
    /p:BuildTasksDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage\DevAlm"
    /p:MetadataDirectory="$(Build.SourcesDirectory)\Metadata"
    /p:FrameworkDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage"
    /p:ReferenceFolder="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp\ref\net40;$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Application.DevALM.BuildXpp\ref\net40;$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp\ref\net40;$(Build.SourcesDirectory)\Metadata;$(Build.BinariesDirectory)"
    /p:ReferencePath="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage" /p:OutputDirectory="$(Build.BinariesDirectory)"
    ```

パイプライン サンプルでは、NuGet パッケージ名とパスの変数を使用して、これらのコマンドを簡略化しています。

### <a name="creating-a-full-pipeline-that-includes-packaging"></a>パッケージを含む完全なパイプラインの作成

利便性のため、パイプラインにはバージョン管理手順とパッケージ手順が含まれている必要があります。 これらのステップをパイプラインに追加する前に、Azure DevOps の [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps 組織にインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[Azure DevOps のドキュメント](/azure/devops/marketplace/install-extension)を参照してください。

パイプライン全体は、少なくとも次の手順で構成されている必要があります。

1. NuGet パッケージをインストールします。
2. [モデルバージョンを更新](pipeline-model-version.md)します。
3. ソリューションまたはプロジェクトをビルドします。
4. エージェントに NuGet 3.3.0 またはそれ以前のバージョンをインストールします。 (配置可能なパッケージを作成するステップでは、この手順が必要です)。
5. [配置可能パッケージを作成します](pipeline-create-deployable-package.md)。
6. 配置可能パッケージ コンポーネントをビルド出力として発行します。

配置可能パッケージを作成するには、ビルド エージェントですぐに NuGet を使用できるようにする必要があります。 したがって、パッケージを作成するステップの前に、Azure DevOps の **NuGetツール インストーラー** タスクを実行する必要があります。

> [!NOTE]
> ソース コード リポジトリに ISVs のようなサード パーティのバイナリ パッケージが含まれる場合は、パッケージ ステップに明示的に追加する必要があります。 詳細については、[Azure Pipelines での配置可能パッケージの作成](pipeline-create-deployable-package.md) を参照してください。

> [!NOTE]
> NuGet バージョン 3.4 以降のセマンティック バージョニング機能のために、タスクによってバージョン 3.3.0 またはそれ以前のバージョンがインストールされることを確認してください。 現在、配置可能パッケージの生成はセマンティック バージョニングをサポートしていません。

### <a name="sample-pipeline-for-x-developers"></a>X++ 開発者のためのサンプル パイプライン

[Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリでは、既存の Azure DevOps プロジェクトにインポートできるサンプル パイプラインを見つけることができます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

