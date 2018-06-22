---
title: "Dynamics 365 Finance and Operations 環境に最新のプラットフォーム更新プログラムを適用"
description: "ここでは、Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 環境に最新のプラットフォーム リリースを適用する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 03/06/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 253274
ms.assetid: a70a4f28-9269-4b35-bc29-1edba0b92d83
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 9ae6c70d043297af26cd27ec2337e006999b6095
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="apply-the-latest-platform-update-to-your-microsoft-dynamics-365-finance-and-operations-environment"></a>Microsoft Dynamics 365 Finance and Operations 環境への最新のプラットフォーム更新プログラムの適用

[!include [banner](../includes/banner.md)]

ここでは、Microsoft Dynamics 365 for Finance and Operations 環境に最新のプラットフォーム リリースを適用する方法について説明します。

## <a name="overview"></a>概要

Microsoft Dynamics 365 for Finance and Operations プラットフォームは、次のコンポーネントで構成されます。

-   Application Object Server (AOS)、データ管理フレームワーク、レポートおよびビジネス インテリジェンス (BI) フレームワーク、開発ツール、および分析サービスなどの Finance and Operations プラットフォーム バイナリ。
-   次のアプリケーション オブジェクト ツリー (AOT) パッケージ。
    -   アプリケーション プラットフォーム
    -   アプリケーション基準
    -   Test Essentials

> [!IMPORTANT]
> 最新の Finance and Operations プラットフォームに移行するためには、Finance and Operations の実装で、プラットフォームに属する AOT パッケージのカスタマイズ (オーバーレイヤー) を行うことは**できません**。 この制限は、プラットフォーム更新 3 で導入されたため、プラットフォームにシームレスに継続的な更新を行うことができます。 プラットフォーム 更新プログラム 3 よりも古いプラットフォームで実行している場合、「[以前のビルドからプラットフォーム更新プログラム 3 にアップグレードする](#Upgrading-to-platform-update-3-from-an-earlier-build)」というセクションを参照します。

## <a name="overall-flow"></a>全体的な流れ
次の図は、Finance and Operations プラットフォームを最新の更新プログラムにアップグレードするための全体的なプロセスを示しています。

[![プラットフォームのカスタマイズがない実装のアップグレード プロセス](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)

既にプラットフォーム更新プログラム 4 以降で実行している場合は、Finance and Operations プラットフォームを最新のリリースに更新することが単純なサービス工程となります。 プラットフォーム更新プログラムのパッケージが LCS アセット ライブラリに入ったら、LCS 環境ページから更新を適用するためにフローに従います。メンテナンスで更新プログラムの適用を選択し、プラットフォーム更新プログラム パッケージを選択します。

[![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)

次のセクションでは**最新のプラットフォーム パッケージを取得して、LCS を通じて配置された環境に適用する**方法について説明します。

## <a name="apply-the-latest-platform-update-package"></a>最新のプラットフォーム更新プログラム パッケージを適用
LCS で、環境ページから最新のプラットフォーム更新パッケージを入手するには、2つの方法があります。
- **プラットフォーム バイナリ更新プログラム** タイルをクリックします。 
- **すべてのバイナリ更新プログラム** タイルをクリックすると、アプリケーションとプラットフォームのバイナリ アップデートのパッケージの一覧が表示されます。 (現在のプラットフォーム更新プログラム 4 では、LCS のバイナリ更新プログラムに、最新のプラットフォームへのアップグレードが含まれています)。

> [!NOTE]
> LCS の環境ページのタイルは、現在のバージョンと環境の状態に基づいて、環境に適用される更新のみを表示します。

上記に示されたように、2 つのタイルのいずれかをクリックして、最新のプラットフォーム更新プログラム パッケージを取得します。 プラットフォームに含まれる修正を確認した後に、**パッケージの保存**をクリックして、プロジェクト アセット ライブラリにパッケージを保存します。

プロセスの観点では、プラットフォーム更新プログラム パッケージの展開は、バイナリ修正プログラムの展開可能なパッケージに似ています。

-   クラウド開発、ビルド、デモ、第 2 層サンド ボックス、または実稼働環境にプラットフォーム更新パッケージを適用するには、LCS から直接更新します。
[![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)

詳細については、[配置可能パッケージの適用](../deployment/apply-deployable-package-system.md) で、バイナリ修正プログラムを適用するための指示に従って下さい。

> [!NOTE]
> **ドキュメント管理用のファイルの移行**: プラットフォーム更新プログラム 6 以降にアップグレードした後、管理者は**ドキュメント管理パラメーター**ページの**ファイルの移行**ボタンをクリックして、アップグレード プロセスを完了する必要があります。 これにより、データベースに格納されている添付ファイルが BLOB ストレージに移行されます。 移行はバッチ プロセスとして実行され、データベースから Azure Blob Storage に移動されるファイルの数とサイズに応じて、時間がかかる可能性があります。 移行プロセスの実行中に、ユーザーは引き続き添付ファイルを使用できるため、移行には、ユーザーが気づくほどの影響はありません。 バッチ処理がまだ実行されているかどうかを確認するには、**バッチ ジョブ** ページで **データベースに格納されたファイルをブロブ ストレージに移行する** プロセスを探します。

## <a name="apply-a-platform-update-to-environments-that-are-not-connected-to-lcs"></a>LCS に接続されていない環境にプラットフォーム更新プログラムを適用します
このセクションでは、プラットフォーム更新パッケージを*ローカル開発環境* (LCS に接続されていないもの) に適用する方法について説明します。

### <a name="how-to-get-the-platform-update-package"></a>プラットフォーム更新プログラム パッケージを取得する方法
プラットフォーム更新プログラム パッケージは、Microsoft によってリリースされ、Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリからインポートすることができます。 パッケージ名の先頭に **Dynamics 365 Unified Operations Platform Update** が付きます。 プラットフォーム更新プログラムのパッケージをインポートするには、次の手順を使用します。

1.  LCS プロジェクトの資産ライブラリに移動します。
2.  **ソフトウェア配置可能パッケージ**タブで、**インポート**をクリックし、プラットフォーム更新プログラム パッケージへの参照を作成します。 [![ボタンのインポート](./media/importupgradepackage.png)](./media/importupgradepackage.png)
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
> Platform Update 4 以降にアップグレードするときは、手順 3 は適用されません。

4.  配置可能パッケージをインストールする指示に従ってください。 [配置可能パッケージのインストール](../deployment/install-deployable-package.md)をご覧ください。
5.  開発環境で作業している場合、アプリケーションのコードをリビルドします。

#### <a name="example"></a>例

```AXUpdateInstaller.exe generate -runbookid="OneBoxDev" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="OneBoxDev-runbook.xml"

    AXUpdateInstaller.exe import -runbookfile=OneBoxDev-runbook.xml

    AXUpdateInstaller.exe execute -runbookid=OneBoxDev
```

### Install the Visual Studio development tools (Platform update 3 or earlier)

> [!NOTE]
> Skip this section if you are updating to platform update 4 or later, development tools are automatically installed as part of installing the deployable package.

Update the Visual Studio development tools as described in [Updating the Visual Studio development tools](../dev-tools/update-development-tools.md).

### Regenerate form adaptor models

Form adaptor models are required for test automation. Regenerate the platform form adaptor models, based on the newly updated platform models. Use the xppfagen.exe tool to generate the form adaptor models. This tool is located in the package's bin folder (typically, j:\\AosService\\PackagesLocalDirectory\\bin). Here is a list of the platform form adaptor models:

-   ApplicationPlatformFormAdaptor
-   ApplicationFoundationFormAdaptor
-   DirectoryFormAdaptor

The following examples show how to generate the form adaptor models.
```
xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationPlatformFormAdaptor" -xmllog="c:\temp\log1.xml"

xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationFoundationFormAdaptor" -xmllog="c:\temp\log2.xml"

xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="DirectoryFormAdaptor" -xmllog="c:\temp\log3.xml"
```

### Install the Data Management service (Platform update 3 or earlier)

> [!NOTE]
> Skip this section if you are updating to platform update 4 or newer, the data management service is automatically installed as part of installing the deployable package.

After the deployable package is installed, follow these instructions to install the new Data Management service. Open a **Command Prompt** window as an administrator, and run the following commands from the .\\DIXFService\\Scripts folder.

    msiExec.exe /uninstall {5C74B12A-8583-4B4F-B5F5-8E526507A3E0} /passive /qn /quiet

If you're connected to Microsoft SQL Server Integration Services 2016 (13.0), run the following command.

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin\2012" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt

If you're connected to an earlier release of Microsoft SQL Server Integration Services, run the following command.

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt

## Apply the platform update package on a build environment (Platform update 6 or earlier)

> [!NOTE]
> Skip this section if you are updating to platform update 7 or newer. This was a pre-requesite step for build environments.

If the build machine has been used for one or more builds, you should restore the metadata packages folder from the metadata backup folder before you upgrade the VM to a newer Dynamics 365 for Finance and Operations platform. You should then delete the metadata backup. These steps help ensure that the platform update will be applied on a clean environment. The next build process will then detect that no metadata backup exists and will automatically create a new one. This new metadata backup will include the updated platform. To determine whether a complete metadata backup exists, look for a BackupComplete.txt file in I:\\DynamicsBackup\\Packages (or C:\\DynamicsBackup\\Packages on a downloadable virtual hard disk \[VHD\]). If this file is present, a metadata backup exists, and the file will contain a timestamp that indicates when it was created. To restore the deployment's metadata packages folder from the metadata backup, open an elevated Windows PowerShell **Command Prompt** window, and run the following command. This command will run the same script that is used in the first step of the build process.

    if (Test-Path -Path "I:\DynamicsBackup\Packages\BackupComplete.txt") { C:\DynamicsSDK\PrepareForBuild.ps1 }

If a complete metadata backup doesn't exist, the command will create a new backup. This command will also stop the Finance and Operations deployment services and Internet Information Services (IIS) before it restores the files from the metadata backup to the deployment's metadata packages folder. 
You should see output that resembles the following example. 
```
午後 6 時 17 分 52 秒: ビルド定義環境を準備しています...* <em>午後 6 時 17 分 53 秒: 指定された値で Dynamics SDK のレジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53 秒: AOS の web config からの値で Dynamics SDK レジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53 秒: Finance and Operations の配置を停止しています...</em> <em>午後 6 時 18 分 06 秒: **バックアップが次の場所に既に存在します: I:\\DynamicsBackup\\Packages。新しいバックアップは作成されません</em><em>。</em> <em>午後 6 時 18 分 6 秒: **メタデータ パッケージをバックアップから復元する</em>** <em>午後 6 時 22 分 56 秒: **メタデータ パッケージを正常にバックアップから復元しました</em><em>。</em> <em>午後 6 時 22 分 57: ビルド環境の準備が完了しました。</em> <em>午後 6 時 22 分 57 秒: 終了コード 0 でスクリプトが完了</em> 
```

After the metadata backup has been restored, delete (or rename) the metadata backup folder (DynamicsBackup\\Packages), so that it will no longer be found by the build process.

### Apply the platform update package

After you've prepared your build environment for this update, apply the platform update package by using the same method that you use on other environments.

## Upgrading to platform update 3 from an earlier build
When upgrading to platform update 3 from an earlier build, there are some very important considerations because of two key changes in update 3:

- It is no longer possible to overlayer platform models (Application Platform, Application Foundation, Test Essentials).
- You need to delete all X++ hotfixes to the platform that are in you version control (see the section below)
- The Directory model is no longer in platform, it has moved to the application in Finance and Operations release 1611.

This means two things:

1.  If taking only platform update 3 and not taking the application update (Finance and Operations version 1611), then you cannot have overlayering on any of the following models. All overlayering on these models must be removed before attempting to install update 3:
    -   Application Platform
    -   Application Foundation
    -   Test Essentials
    -   Directory

2.  If you cannot remove over-layering from the Directory model, and you still want to upgrade, you will have to do a complete upgrade of the platform and the application (Finance and Operations version 1611) as described in [Overview of moving to the latest update of Finance and Operations](upgrade-latest-update.md).

### Delete platform metadata hotfixes from your VSTS project (Platform update 2 or earlier)

> [!NOTE]
> This section is not relevant if you are already on Platform update 3 and updating to a newer platform.

Before you install the new platform update, you must clean up your Microsoft Visual Studio Team Services (VSTS) source control project.
Remove any X++ or metadata hotfixes that you've installed on your existing platform. If you have any X++ or metadata hotfixes that are checked in to your VSTS project for any of the following Microsoft models, delete them from your project by using the Microsoft Visual Studio Source Control Explorer.

-   Application Platform
-   Application Foundation
-   TestEssentials
-   Directory

You can find these hotfixes by browsing the check-in history of these Microsoft models. For example, use Source Control Explorer to browse the check-in history of the Trunk\\Main\\Metadata\\ApplicationFoundation\\ApplicationFoundation folder, and delete all XML files that have been checked in to it.
![View History](./media/checkinhistory.png)

Additional resources
--------

[Overview of moving to the latest update of Microsoft Dynamics 365 for Finance and Operations](upgrade-latest-update.md)




