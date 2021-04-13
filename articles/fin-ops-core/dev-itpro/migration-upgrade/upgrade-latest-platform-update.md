---
title: 最新のプラットフォーム更新プログラムを環境へ適用
description: このトピックでは、最新のプラットフォーム更新プログラムを Finance and Operations 環境に適用する方法について説明します。
author: tariqbell
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 253274
ms.assetid: a70a4f28-9269-4b35-bc29-1edba0b92d83
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 9d9422e505ffa66cd131957ffa79019b1227f3f7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743897"
---
# <a name="apply-the-latest-platform-update-to-environments"></a>最新のプラットフォーム更新プログラムの環境への適用

[!include [banner](../includes/banner.md)]

このトピックでは、最新のプラットフォーム リリースを Finance and Operations 環境に適用する方法について説明します。

## <a name="overview"></a>概要

Finance and Operations では、プラットフォームは次のコンポーネントで構成されています:

-   Application Object Server (AOS)、データ管理フレームワーク、レポートおよびビジネス インテリジェンス (BI) フレームワーク、開発ツール、および分析サービスなどのバイナリ。
-   次のアプリケーション オブジェクト ツリー (AOT) パッケージ。
    -   アプリケーション プラットフォーム
    -   アプリケーション基準
    -   Test Essentials

> [!IMPORTANT]
> 最新のプラットフォームに移行するためには、Finance and Operations の実装で、プラットフォームに属する AOT パッケージのカスタマイズ (オーバーレイヤー) を行うことは **できません**。 この制限は、プラットフォーム更新 3 で導入されたため、プラットフォームにシームレスに継続的な更新を行うことができます。 

## <a name="overall-flow"></a>全体的な流れ
次の図は、プラットフォームを最新の更新プログラムにアップグレードするための全体的なプロセスを示しています。

[![プラットフォームのカスタマイズがない実装のアップグレード プロセス](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)

既にプラットフォーム更新プログラム 4 以降で実行している場合は、最新のリリースに更新することが単純なサービス工程となります。 プラットフォーム更新プログラム パッケージが LCS アセット ライブラリに含まれた後、フローに従って LCS 環境ページから更新を適用します。 **メンテナンス** で **更新プログラムの適用** を選択してから、プラットフォーム更新プログラム パッケージを選択します。

[![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)

次のセクションでは **最新のプラットフォーム パッケージを取得して、LCS を通じて配置された環境に適用する** 方法について説明します。

## <a name="apply-the-latest-platform-update-package"></a>最新のプラットフォーム更新プログラム パッケージを適用
LCS で、環境ページから最新のプラットフォーム更新パッケージを入手するには、2つの方法があります。
- **プラットフォーム バイナリ更新プログラム** タイルをクリックします。 
- **すべてのバイナリ更新プログラム** タイルをクリックすると、アプリケーションとプラットフォームのバイナリ アップデートのパッケージの一覧が表示されます。 (現在のプラットフォーム更新プログラム 4 では、LCS のバイナリ更新プログラムに、最新のプラットフォームへのアップグレードが含まれています)。

> [!NOTE]
> LCS の環境ページのタイルは、現在のバージョンと環境の状態に基づいて、環境に適用される更新のみを表示します。

上記に示されたように、2 つのタイルのいずれかをクリックして、最新のプラットフォーム更新プログラム パッケージを取得します。 プラットフォームに含まれる修正を確認した後に、**パッケージの保存** をクリックして、プロジェクト アセット ライブラリにパッケージを保存します。

プロセスの観点では、プラットフォーム更新プログラム パッケージの展開は、バイナリ修正プログラムの展開可能なパッケージに似ています。

-   クラウド開発、ビルド、デモ、第 2 層サンド ボックス、または実稼働環境にプラットフォーム更新パッケージを適用するには、LCS から直接更新します。

    [![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)

詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md) で、バイナリ修正プログラムを適用するための指示に従って下さい。

> [!NOTE]
> **ドキュメント管理用のファイルの移行**: プラットフォーム更新プログラム 6 以降にアップグレードした後、管理者は **ドキュメント管理パラメーター** ページの **ファイルの移行** ボタンをクリックして、アップグレード プロセスを完了する必要があります。 これにより、データベースに格納されている添付ファイルが BLOB ストレージに移行されます。 移行はバッチ プロセスとして実行され、データベースから Azure Blob Storage に移動されるファイルの数とサイズに応じて、時間がかかる可能性があります。 移行プロセスの実行中に、ユーザーは引き続き添付ファイルを使用できるため、移行には、ユーザーが気づくほどの影響はありません。 バッチ処理がまだ実行されているかどうかを確認するには、**バッチ ジョブ** ページで **データベースに格納されたファイルをブロブ ストレージに移行する** プロセスを探します。

## <a name="apply-a-platform-update-to-environments-that-are-not-connected-to-lcs"></a>LCS に接続されていない環境にプラットフォーム更新プログラムを適用します
このセクションでは、プラットフォーム更新パッケージを *ローカル開発環境* (LCS に接続されていないもの) に適用する方法について説明します。

### <a name="how-to-get-the-platform-update-package"></a>プラットフォーム更新プログラム パッケージを取得する方法
プラットフォーム更新プログラム パッケージは、Microsoft によってリリースされ、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリからインポートすることができます。 パッケージ名の先頭に **Dynamics 365 Unified Operations プラットフォーム更新** が付きます。 プラットフォーム更新プログラムのパッケージをインポートするには、次の手順を使用します。

1.  LCS プロジェクトの資産ライブラリに移動します。
2.  **ソフトウェア配置可能パッケージ** タブで、**インポート** をクリックし、プラットフォーム更新プログラム パッケージへの参照を作成します。 

    [![ボタンのインポート](./media/importupgradepackage.png)](./media/importupgradepackage.png)

3.  目的のプラットフォーム更新プログラム パッケージを選択します。

> [!NOTE]
> 共有アセット ライブラリのパッケージは、目的のプラットフォーム リリースの最新ビルド (ホットフィックス付き) に対応していない可能性があります。 最新のビルドを保証するには、この記事の前半で説明した LCS 環境ページを使用します。

### <a name="apply-the-platform-update-package-to-your-development-environment"></a>開発環境にプラットフォーム更新プログラム パッケージを適用
> [!NOTE]
> これらの手順は、LCS から直接更新できない環境にのみ適用されます。

### <a name="install-the-deployable-package"></a>配置可能パッケージのインストール

1.  プラットフォーム更新パッケージ (AXPlatformUpdate.zip) を使用中の仮想マシン (VM) にダウンロードします。
2.  コンテンツをローカル ディレクトリに解凍します。
3.  アップグレードする環境のタイプに応じて、\\AOSService\\ スクリプトの下の PlatformUpdatePackages.Config ファイルを開き、**MetaPackage** 値を変更します。
    -   開発をアップグレードする場合、またはソース コードが含まれているデモ環境をアップグレードする場合は、**MetaPackage** 値を **dynamicsax-meta-platform-development** に変更します。
    -   レベル 2 のサンド ボックスやソース コードが含まれていない別の環境を含むランタイム環境をアップグレードする場合は、既定値の **dynamicsax-meta-platform-runtime** は正しい値になります。

    > [!NOTE]
    > プラットフォーム更新プログラム 4 以降にアップグレードするときは、手順 3 は適用されません。

4.  配置可能パッケージをインストールする指示に従ってください。 [コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md)
5.  開発環境で作業している場合、アプリケーションのコードをリビルドします。

#### <a name="example"></a>例

```powershell
AXUpdateInstaller.exe generate -runbookid="OneBoxDev" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="OneBoxDev-runbook.xml"

    AXUpdateInstaller.exe import -runbookfile=OneBoxDev-runbook.xml

    AXUpdateInstaller.exe execute -runbookid=OneBoxDev
```

### <a name="install-the-visual-studio-development-tools-platform-update-3-or-earlier"></a>Visual Studio 開発ツール (プラットフォーム更新プログラム 3 またはそれ以前) をインストールする

> [!NOTE]
> プラットフォーム更新プログラム 4 以降を更新する場合にこのセクションをスキップすると、開発ツールは配置可能パッケージのインストールの一部として自動的にインストールされます。

[Visual Studio 開発ツールの更新](../dev-tools/update-development-tools.md) の説明に従って、Visual Studio 開発ツールを更新します。

### <a name="regenerate-form-adaptor-models"></a>フォーム アダプタ モデルの再生成

フォーム アダプター モデルは、テストの自動化に必要です。 新たに更新されたプラットフォーム モデルに基づいて、プラットフォーム フォーム アダプターのモデルを再生成します。 フォーム アダプター モデルを生成するには、xppfagen.exe ツールを使用します。 このツールは、パッケージの bin フォルダー (通常は、j:\\AosService\\PackagesLocalDirectory\\bin) にあります。 プラットフォームのフォーム アダプター モデルの一覧を次に示します。

-   ApplicationPlatformFormAdaptor
-   ApplicationFoundationFormAdaptor
-   DirectoryFormAdaptor

次の例は、フォーム アダプター モデルを生成する方法を示しています。

```powershell
xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationPlatformFormAdaptor" -xmllog="c:\temp\log1.xml"

xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationFoundationFormAdaptor" -xmllog="c:\temp\log2.xml"

xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="DirectoryFormAdaptor" -xmllog="c:\temp\log3.xml"
```

### <a name="install-the-data-management-service-platform-update-3-or-earlier"></a>データ管理サービス (プラットフォーム更新プログラム 3 またはそれ以前) をインストールします

> [!NOTE]
> プラットフォーム更新プログラム 4 以降を更新する場合にこのセクションをスキップすると、データ管理サービスは配置可能パッケージのインストールの一部として自動的にインストールされます。

配置可能なパッケージのインストール後、以下の手順に従って、新しい Data Management サービスをインストールします。 管理者として **コマンド プロンプト** ウィンドウを開き、.\\DIXFService\\Scripts フォルダーから次のコマンドを実行します。

```Console
msiExec.exe /uninstall {5C74B12A-8583-4B4F-B5F5-8E526507A3E0} /passive /qn /quiet
```

Microsoft SQL Server の統合サービス 2016 (13.0) に接続している場合は、次のコマンドを実行します。

```Console
msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin\2012" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt
```

Microsoft SQL Server の統合サービスの早期リリースに接続している場合は、次のコマンドを実行します。

```Console
msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt
```

## <a name="apply-the-platform-update-package-on-a-build-environment-platform-update-6-or-earlier"></a>ビルド環境 (プラットフォーム アップデート 6 またはそれ以前) にプラットフォーム更新プログラムのパッケージを適用

> [!NOTE]
> プラットフォーム更新プログラム 7 以降を更新する場合はこのセクションをスキップします。 これは、ビルド環境のための前提条件ステップでした。

1 つ以上のビルドに対してビルド マシンが使用されているときは、VM を新しいプラットフォーム更新プログラムにアップグレードする前に、メタデータ バックアップ フォルダーからメタデータ パッケージ フォルダーを復元する必要があります。 その後、メタデータのバックアップを削除してください。 これらの手順は、プラットフォームの更新がクリーンな環境に確実に適用されるようにします。 次のビルド プロセスはメタデータ バックアップが存在しないことを検出し、新しいメタデータ バックアップが自動的に作成されます。 この新しいメタデータ バックアップには、更新されたプラットフォームが含まれます。 完全なメタデータ バックアップが存在するかどうかを確認するには、I:\\DynamicsBackup\\Packages (またはダウンロード可能な仮想ハード ディスク \[VHD\] 上の C:\\DynamicsBackup\\Packages) で、BackupComplete.txt ファイルを探してください。 このファイルが存在する場合、メタデータ バックアップが存在し、ファイルにはその作成日時を示すタイムスタンプが含まれています。 展開のメタデータ パッケージ フォルダーをメタデータ バックアップから復元するには、上位の Windows PowerShell **コマンド プロンプト** ウィンドウを開き、以下のコマンドを実行します。 このコマンドは、ビルド プロセスの最初のステップで使用したのと同じスクリプトを実行します。

```powershell
if (Test-Path -Path "I:\DynamicsBackup\Packages\BackupComplete.txt") { C:\DynamicsSDK\PrepareForBuild.ps1 }
```

完全なメタデータ バックアップが存在しない場合、コマンドは新しいバックアップを作成します。 このコマンドも ファイルをメタデータ バックアップから展開のメタデータ パッケージ フォルダーに復元する前に、Finance and Operations 配置サービスおよびインターネット インフォメーション サービス (IIS) を停止します。 次の例のような出力が表示されます。 

```powershell
6:17:52 PM: Preparing build environment...* <em>6:17:53 PM: Updating Dynamics SDK registry key with specified values...</em> <em>6:17:53 PM: Updating Dynamics SDK registry key with values from AOS web config...</em> <em>6:17:53 PM: Stopping Finance and Operations deployment...</em> <em>6:18:06 PM: **A backup already exists at: I:\\DynamicsBackup\\Packages. No new backup will be created</em><em>.</em> <em>6:18:06 PM: **Restoring metadata packages from backup...</em>** <em>6:22:56 PM: **Metadata packages successfully restored from backup</em><em>.</em> <em>6:22:57 PM: Preparing build environment complete.</em> <em>6:22:57 PM: Script completed with exit code: 0</em> 
```

メタデータ バックアップが復元された後、ビルド プロセスでは検出されないようにメタデータ バックアップ フォルダー (DynamicsBackup\\Packages) を削除します。

### <a name="apply-the-platform-update-package"></a>プラットフォーム更新プログラム パッケージを適用

更新プログラムのビルド環境を準備した後、他の環境で使用する同じメソッドでプラットフォームの更新プログラム パッケージを適用します。

<a name="additional-resources"></a>追加リソース
--------

[Finance and Operationsで最新の更新プログラムに移行するためのプロセス](upgrade-latest-update.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]