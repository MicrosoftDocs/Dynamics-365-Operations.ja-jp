---
title: 2016 年 8 月リリースへの AX プラットフォームのアップグレード
description: このトピックでは、Microsoft Dynamics AX プラットフォームを Dynamics AX の 2016 年 8 月リリースにアップグレードする方法について説明します。
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 125753
ms.assetid: 99af5334-d30e-4160-9504-881777e9d4ea
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 5b313b07ee4751ccb0e710edf82792a9ec59071f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554509"
---
# <a name="upgrade-the-dynamics-ax-platform-to-the-august-2016-release"></a>2016 年 8 月リリースへの AX プラットフォームのアップグレード

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX プラットフォームを Dynamics AX の 2016 年 8 月リリースにアップグレードする方法について説明します。

<a name="overview"></a>概要
--------

**重要:** このトピックは、2016 年 8 月よりも前の、Microsoft Dynamics AX のリリースにのみ適用されます。 Microsoft Dynamics 365 for Finance and Operations 更新プログラムで、このトピック [Finance and Operations を最新のプラットフォーム更新プログラムに更新](../migration-upgrade/upgrade-latest-platform-update.md) を参照してください。 Microsoft Dynamics AX プラットフォーム は、次のコンポーネントで構成されています。

-   Application Object Server (AOS)、データ管理フレームワーク、レポートおよびビジネス インテリジェンス (BI) フレームワーク、開発ツール、および分析サービスなどの Dynamics AX プラットフォーム バイナリ
-   次のアプリケーション オブジェクト ツリー (AOT) パッケージ。
    -   アプリケーション プラットフォーム
    -   アプリケーション基準
    -   ディレクトリ
    -   TestEssentials

**重要:** Dynamics AX のプラットフォームを新しいリリースに更新する場合は、Dynamics AX の実装はプラットフォームに属するどの AOT パッケージにもカスタマイズ (オーバーレイ) を行なうべきではありません。 プラットフォーム パッケージをカスタマイズ**する**場合 (ソリューションに 1 つ以上のプラットフォーム パッケージに属しているモデルが含まれている場合) は、このトピックの最後に記載されている回避策を完了し、カスタマイズされたプラットフォーム パッケージがある Dynamics AX の実装のために図示され、説明されている総合プロセスを完了します。

## <a name="overall-flow"></a>全体的な流れ
次の図は、Dynamics AX プラットフォームを最新の更新プログラムにアップグレードする 2 つのシナリオの異なるプロセス全体を示しています。

### <a name="dynamics-ax-implementations-that-have-no-customization-of-the-platform"></a>プラットフォームのカスタマイズがない実装の Dynamics AX

[![プラットフォームのカスタマイズがない実装のアップグレード プロセス](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)

### <a name="dynamics-ax-implementations-that-have-customized-platform-packages"></a>プラットフォーム パッケージをカスタマイズした実装の Dynamics AX

[![プラットフォーム パッケージをカスタマイズした実装のアップグレード プロセス](./media/flowwithcustomisations.jpg)](./media/flowwithcustomisations.jpg)

## <a name="import-the-platform-update-package"></a>プラットフォーム更新プログラム パッケージのインポート
プラットフォーム更新プログラム パッケージは、Microsoft によってリリースされ、Microsoft Lifecycle Services (LCS) の共有資産ライブラリからインポートすることができます。 このパッケージの名前は、**Dynamics AX platform  2016 年 8 月リリース (更新プログラム 2)** です。 まだ済んでいない場合、次の手順に従って、**Dynamics AX プラットフォーム 2016 年 8 月リリース (更新プログラム 2)** パッケージをプロジェクトの資産ライブラリにインポートします。

1. LCS プロジェクトの資産ライブラリに移動します。
2. ソフトウェア配置可能パッケージ タブを選択します。
3. <strong>インポートをクリックし、Dynamics AX プラットフォーム 2016 年 8 月リリース (更新プログラム 2) 共有パッケージ**を選択します**</strong>。[![importupgradepackage](./media/importupgradepackage.png)](./media/importupgradepackage.png)

## <a name="how-to-apply-the-platform-upgrade-package"></a>プラットフォーム更新プログラムパッケージを適用する方法
プロセスの観点では、プラットフォーム更新プログラム パッケージは、バイナリ修正プログラムの展開可能なパッケージに似ています。

-   パッケージを開発環境またはビルド環境に適用するには、次のセクションの指示に従います。
-   パッケージをデモ、第 2 層サンド ボックス、または実稼働環境に適用するには、[[展開可能パッケージの適用](../deployment/apply-deployable-package-system.md)] のトピックのバイナリ修正プログラムの指示に従います。

## <a name="apply-the-platform-update-package-on-your-development-environment"></a>開発環境にプラットフォーム更新プログラム パッケージを適用する
### <a name="delete-any-platform-metadata-hotfixes-from-your-azure-devops-project"></a>Azure DevOps プロジェクトからプラットフォーム メタデータの修正プログラムを削除する

新しいプラットフォーム更新プログラムをインストールする前に、Azure DevOps ソース コントロール プロジェクトをクリーンアップする必要があります。 既存のプラットフォームにインストールされているすべての X++ またはメタデータの修正プログラムを削除します。 次の Microsoft モデルのいずれかの Azure DevOps プロジェクトでチェックされている X++ またはメタデータの修正プログラムがある場合は、Visual Studio のソース管理エクスプローラーを使用してプロジェクトから削除します。

-   アプリケーション プラットフォーム
-   アプリケーション基準
-   ディレクトリ
-   TestEssentials

これらの修正プログラムは、Microsoft モデルでこれらのモデルのチェックイン履歴を参照することにより見つけることができます。 たとえば、ソース管理エクスプローラーを使用して、フォルダー *TrunkMainMetadataApplicationFoundationApplicationFoundation* のチェックイン履歴を参照し、この Microsoft モデルでチェックされたすべての XML ファイルを削除します。 [![CheckInHistory](./media/checkinhistory.png)](./media/checkinhistory.png)

### <a name="install-the-deployable-package"></a>配置可能パッケージのインストール

1.  プラットフォーム更新パッケージ (AXPlatformUpdate.zip) を使用中の仮想マシンにコピーします。
2.  コンテンツをローカル ディレクトリに解凍します。
3.  アップグレードする環境のタイプに応じて、AOSService スクリプトの下の PlatformUpdatePackages.Config ファイルを開き、MetaPackage 値を変更します。
    -   開発をアップグレードする場合、またはソース コードが含まれているデモ環境をアップグレードする場合は、**MetaPackage** 値を **dynamicsax-meta-platform-development** に変更します。
    -   レベル 2 のサンド ボックスやソース コードが含まれていない他の環境を含むランタイム環境をアップグレードする場合は、既定値の **dynamicsax-meta-platform-runtime** は正しい値になります。

4.  配置可能パッケージをインストールする標準指示に従ってください。 [配置可能パッケージの適用](../deployment/apply-deployable-package-system.md)をご覧ください。
5.  開発環境で作業している場合、アプリケーションのコードをリビルドします。

**重要:** 開発環境で最初に検証することなく、実行環境でこの更新を適用しないでください。

#### <a name="example-for-a-one-box-development-or-demo-environment"></a>1 つのボックス (開発またはデモ) 環境の例

    AXUpdateInstaller.exe generate -runbookid="OneBoxDev" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="OneBoxDev-runbook.xml"

    AXUpdateInstaller.exe import -runbookfile=OneBoxDev-runbook.xml

    AXUpdateInstaller.exe execute -runbookid=OneBoxDev

### <a name="install-the-visual-studio-development-tools"></a>Visual Studio 開発ツールのインストール

[Dynamics AX Visual Studio 開発ツールの更新](../dev-tools/update-development-tools.md) の説明に従って、Microsoft Visual Studio 開発ツールを更新します。

### <a name="regenerate-form-adaptor-models"></a>フォーム アダプタ モデルの再生成

フォーム アダプター モデルは、テストの自動化に必要です。 新たに更新されたプラットフォーム モデルに基づいて、プラットフォーム フォーム アダプターのモデルを再生成します。 フォーム アダプター モデルを生成するには、xppfagen.exe ツールを使用します。 このツールは、パッケージの bin フォルダー (通常は、j:AosServicePackagesLocalDirectorybin) に配置されています。 プラットフォームのフォーム アダプター モデルの一覧を次に示します。

-   ApplicationPlatformFormAdaptor
-   ApplicationFoundationFormAdaptor
-   DirectoryFormAdaptor

次の例は、フォーム アダプター モデルを生成する方法を示しています。

    xppfagen.exe -metadata=j:AosServicePackagesLocalDirectory -model="ApplicationPlatformFormAdaptor" -xmllog="c:\temp\log1.xml"

    xppfagen.exe -metadata=j:AosServicePackagesLocalDirectory -model="ApplicationFoundationFormAdaptor" -xmllog="c:\temp\log2.xml"

    xppfagen.exe -metadata=j:AosServicePackagesLocalDirectory -model="DirectoryFormAdaptor" -xmllog="c:\temp\log3.xml"

### <a name="install-the-new-data-management-service"></a>新しいデータ管理サービスのインストール

配置可能なパッケージのインストール後、以下の手順に従って、新しい Data Management サービスをインストールします。 管理者としてコマンド プロンプト ウィンドウを開き、.DIXFServiceScripts フォルダーから次のコマンドを実行します。

    msiExec.exe /uninstall {5C74B12A-8583-4B4F-B5F5-8E526507A3E0} /passive /qn /quiet

Microsoft SQL Server の統合サービス 2016 (13.0) に接続している場合は、次のコマンドを実行します。

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin2012" SERVICEACCOUNT="NT AUTHORITYNetworkService" /qb /lv DIXF_log.txt

Microsoft SQL Server の統合サービスの早期リリースに接続している場合は、次のコマンドを実行します。

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin" SERVICEACCOUNT="NT AUTHORITYNetworkService" /qb /lv DIXF_log.txt

## <a name="apply-the-platform-update-package-on-a-build-environment"></a>ビルド環境にプラットフォーム更新プログラム パッケージを適用
ビルド環境のプラットフォーム アップグレード パッケージを適用するには、開発環境に適用する同じ手順が必要です。 ただし、次のように最新のプラットフォームにアップグレードする前に、まず、ビルド環境を準備する必要があります。

### <a name="prepare-your-build-environment"></a>ビルド環境を準備

1 つ以上のビルドに対してビルド マシンが使用されているときは、VM を新しい Dynamics AX プラットフォームにアップグレードする前に、メタデータ バックアップ フォルダーからメタデータ パッケージ フォルダーを復元する必要があります。 その後、メタデータのバックアップを削除してください。 これにより、プラットフォームの更新がクリーンな環境で確実に適用され、次のビルド プロセスでメタデータのバックアップが存在しないことが検出され、新しいプラットフォームが自動的に作成されます。 完全なメタデータ バックアップが存在するかどうかを確認するには、I:\Dynamics\BackupPackages (または、ダウンロード可能な VHD の C:\Dynamics\BackupPackages) で BackupComplete.txt ファイルを探してください。 このファイルの存在は、メタデータ バックアップが存在することを示し、そのファイルにはそれが作成された日時のタイムスタンプが含まれています。 展開のメタデータ パッケージ フォルダーをメタデータ バックアップから復元するには、昇格した PowerShell コマンド プロンプトを開き、以下のコマンドを実行します。 これにより、ビルド プロセスの最初のステップで使用したのと同じスクリプトが実行されます。

    if (Test-Path -Path "I:\Dynamics\BackupPackages\BackupComplete.txt") { C:\Dynamics\SDK\PrepareForBuild.ps1 }

注記: バックアップが存在しない場合は新しいバックアップを作成するため、完全なメタデータ バックアップが存在する場合にのみ、上記のコマンドを実行します。 このコマンドは、ファイルをメタデータ バックアップから展開のメタデータ パッケージ フォルダーに復元する前に、Dynamics AX 展開サービスと IIS を停止します。 このように出力が表示されます: <em>午後 6 時 17 分 52 秒: ビルド定義環境を準備しています...</em> <em>午後 6 時 17 分 53 秒: 指定された値で Dynamics SDK のレジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53 秒: AOS の web config からの値で Dynamics SDK レジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53秒: Dynamics AX の配置を停止しています...</em> <em>午後 6 時 18 分 06 秒: ** バックアップが次の場所に既に存在します: I: DynamicsBackupPackages。新しいバックアップは作成されません</em><em>。</em> <em>午後 6 時 18 分 6 秒: **メタデータ パッケージをバックアップから復元する</em>** <em>午後 6 時 22 分 56 秒: **メタデータ パッケージを正常にバックアップから復元しました</em><em>。</em> <em>午後 6 時 22 分 57: ビルド環境の準備が完了しました。</em> <em>午後 6 時 22 分 57 秒: 終了コード 0 でスクリプトが完了</em>メタデータ バックアップが復元されると、<strong>メタデータ バックアップ フォルダーを削除 (または名前を変更) し (<em>DynamicsBackupPackages</em>)</strong>、ビルド プロセスでは検出されなくなります。

### <a name="apply-the-platform-update-package"></a>プラットフォーム更新プログラム パッケージを適用

この更新のビルド環境を準備したら、[上記の](#apply-the-platform-update-package-on-your-development-environment)説明のように、開発環境に適用するのと同じ方法でプラットフォーム更新プログラム パッケージを適用します。

## <a name="features-that-arent-supported"></a>サポートされていない機能
**Dynamics AX プラットフォーム 2016 年 8 月リリース (更新プログラム 2)** には、次の機能が含まれます。

-   新しいエンティティ格納機能
-   DirectQuery 付き Microsoft Power BI
-   Microsoft Cortana Analytics for Retail

ただし、このトピックに記載されているプロセスを使用して更新する場合、2016 年 2 月のリリースを使用して当初展開された Dynamics AX のインスタンスにはこれらの機能がありません。 これらの機能を有効にするには、元の展開は更新プログラム 1 (2016年5月) の展開でなければなりません。

## <a name="optional-if-your-application-overlays-platform-models"></a>オプション: アプリケーション オーバーレイ プラットフォーム モデルの場合
開発インスタンスにプラットフォーム更新プログラム パッケージを適用する前に、ソリューションに次のいずれかのパッケージに属するモデルが含まれている場合は次の手順に従います。

-   アプリケーション プラットフォーム
-   アプリケーション基準
-   ディレクトリ
-   TestEssentials

1.  Visual Studio で、Microsoft Azure DevOps のバージョン管理プロジェクトに対するすべての保留中の変更をチェックインします。
2.  Visual Studio を終了します。
3.  このトピックの前半で説明した、プラットフォーム更新プログラム配置可能パッケージを適用します。
4.  Visual Studio を起動します。
5.  プラットフォーム モデルをオーバーレイするモデルの潜在的な競合を解決します。 **ヒント:** 競合アドインの作成プロジェクトを使用して、モデル内のすべての競合からプロジェクトを作成できます。[![競合からプロジェクトを作成](./media/projectforconflicts.jpg)](./media/projectforconflicts.jpg)
6.  アプリケーションをリビルドして検証します。
7.  カスタマイズしたプラットフォーム パッケージからカスタム配置可能パッケージを作成します。 このパッケージは、検証のためにサンドボックス/実稼働前の環境に適用する必要があります。


<a name="additional-resources"></a>追加リソース
--------

[最新の Dynamics AX 更新プログラムにアップグレードするためのプロセス](../migration-upgrade/upgrade-latest-update.md)



