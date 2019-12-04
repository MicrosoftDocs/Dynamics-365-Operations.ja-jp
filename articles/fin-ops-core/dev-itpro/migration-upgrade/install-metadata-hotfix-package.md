---
title: 開発環境でのメタデータの修正プログラムのインストール
description: このトピックでは、開発環境にアプリケーション メタデータの修正プログラムをインストールする方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 09/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 79822
ms.assetid: 9b132253-1748-4b71-b128-c4b9d3a311ae
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143886e342e1c901a7cf2b87ef6deec7dc1515fe
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812047"
---
# <a name="install-metadata-hotfixes-in-development-environments"></a>開発環境でのメタデータの修正プログラムのインストール

[!include [banner](../includes/banner.md)]

このトピックでは、開発環境にアプリケーション メタデータの修正プログラムをインストールする方法について説明します。

メタデータ修正プログラムのパッケージには、開発環境でのモデル要素 (XML ファイル) への変更 (メタデータまたは X++ ソース コード) が含まれています。 修正プログラムは、新しいモデルの要素を含めることもできます。 メタデータ修正プログラムのパッケージは、SCDP ファイルの形式です。 この記事では、メタデータ修正プログラム パッケージのインストール プロセスについて説明し、同じプロジェクトで作業している他の開発者とパッケージを共有する方法について説明します。

## <a name="overall-flow"></a>全体的な流れ
次の図は、全体的なフローを示しています。 

[![メタデータ修正プログラムのパッケージをインストールするためのプロセス](./media/configureinstallhotfix-1.png)](./media/configureinstallhotfix-1.png)

## <a name="download-the-hotfix-from-lcs"></a>修正プログラムを LCS からダウンロード
修正プログラムをダウンロードする方法の詳細については、 [Lifecycle Services (LCS) から更新プログラムのダウンロード](download-hotfix-lcs.md) を参照してください。 ZIP ファイルをダウンロードした後は、そこから SCDP メタデータの修正プログラム パッケージを抽出し、ローカル フォルダーに保存できます。

## <a name="install-the-hotfix"></a>修正プログラムのインストール
### <a name="before-you-begin"></a>準備

-   このトピックでは、あなたのパッケージ フォルダが c:\\AOSService\\PackagesLocalDirectory\\Bin にあることを前提としています。 いくつかの仮想マシン (Vm) では、c:\\Packages, i:\\AOSService\\PackagesLocalDirectory\\Bin または k:\\AOSService\\PackagesLocalDirectory\\Bin に表示されている場合があります。
-   Microsoft Azure DevOps または別のソース管理システムを使用していない場合は、(メタデータ ストアとも呼ばれる) パッケージ フォルダーのバックアップを作成します。 Azure DevOps を使用していないときに、開発を実行することはお勧めしません。
-   Azure DevOps または Microsoft Team Foundation Server (TFS) バージョン コントロールがない場合、現在のワークスペースの**保留中の変更**一覧にファイルがないことを確認します。 保留中の変更がある場合は、メタデータの修正プログラムをインストールする前に、それらを送信するかまたは棚に置くことをお勧めします。

### <a name="install-the-metadata-hotfix-package"></a>メタデータ修正プログラム パッケージのインストール

メタデータ修正プログラムのインストールを起動するには、コマンド プロンプトから SCDPBundleInstall.exe ユーティリティを呼び出します。 SCDPBundleInstall.exe は、パッケージの bin フォルダーに配置されます。

#### <a name="without-version-control-not-recommended"></a>バージョン コントロールなし (非推奨)

ソース管理の Azure DevOps または TFS を使用していない場合は、次のコマンドを使用します。

    SCDPBundleInstall.exe -install -packagepath=<scdp file containing the hotfix> -metadatastorepath=<metadata packages root folder>

#### <a name="with-version-control-recommended"></a>バージョン管理の使用 (推奨)

ソース管理に Azure DevOps または TFS を使用している場合は、次の手順を実行します。以下のコマンドを使用して、修正プログラム パッケージのインストールを**準備**します。 この手順は、プラットフォーム更新プログラム 2 (2016 年 8 月) よりも古いプラットフォームを使用している場合は利用できません)

    SCDPBundleInstall.exe -prepare -packagepath=<scdp file containing the hotfixes> -metadatastorepath=<metadata packages root folder> -tfsworkspacepath=<path of local workspace folder> -tfsprojecturi=<URI of the Azure DevOps or TFS project collection>

これにより、環境内のすべての既存ファイルの変更セットが作成され、修正プログラム パッケージによって変更されます。この場合、prepare コマンドによって修正プログラムはインストールされません。 次に例を示します。

    SCDPBundleInstall.exe -prepare -packagepath=c:\temp\hotfixbundle1234.axscdppkg -metadatastorepath= c:\AOSService\PackagesLocalDirectory -tfsworkspacepath= c:\AOSService\PackagesLocalDirectory -tfsprojecturi=https://myaccount.visualstudio.com/defaultcollection

保留中の変更を**チェックイン**して、バージョン管理システムでこれらのファイルのバックアップを作成します。 これにより、必要に応じて修正プログラムをロールバックすることができます。 次のコマンドを使用して修正プログラムを**インストール**します。

    SCDPBundleInstall.exe -install -packagepath=<scdp file containing the hotfixes> -metadatastorepath=<metadata packages root folder> -tfsworkspacepath=<path of local workspace folder> -tfsprojecturi=<URI of the Azure DevOps or TFS project collection>

プラットフォーム更新プログラム 2 (2016 年 8 月) よりも古いプラットフォームを使用している場合は、**-install** オプションを指定する必要はありません。 次に例を示します。

    SCDPBundleInstall.exe -install -packagepath=c:\temp\hotfixbundle1234.axscdppkg -metadatastorepath= c:\AOSService\PackagesLocalDirectory -tfsworkspacepath= c:\AOSService\PackagesLocalDirectory -tfsprojecturi=https://myaccount.visualstudio.com/defaultcollection

Azure DevOps/TFS パラメーターを使用して、パッケージによって修正されたファイルを、チーム エクスプ ローラー内の保留中の変更の一覧に追加できます。

### <a name="required-parameters"></a>必須パラメーター

    /packagepath=[Path of the local scdp file containing the hotfixes downloaded from Lifecycle Service (LCS)]

    /metadatastorepath=[Path of the local metadata store folder, such as c:\AOSService\PackagesLocalDirectory]

### <a name="tfs-parameters"></a>TFS パラメーター

ソース管理に Azure DevOps または TFS を使用している場合は、次の 2 つのパラメーターを指定する必要があります。

    /tfsprojecturi=[URI of the TFS Project to connect to]

    /tfsworkspacepath=[Path of the local workspace, usually equal to the metadatastorepath]

インストール コマンドが呼び出されると、パッケージのインストール プロセスが開始されます。 インストール プロセスの一環として、メタデータ ストア フォルダ内の一部の XML ファイルはそれ自体の修正で加えられた変更を反映するように更新されます。 Azure DevOps または TFS を使用している場合、これらのファイルがチーム エクスプローラーの**保留中の変更**ウィンドウに含まれた変更のリストに追加されます。 

[![保留中の変更ウィンドウに含まれている変更の一覧](./media/configureinstallhotfix-2.png)](./media/configureinstallhotfix-2.png)

## <a name="resolve-conflicts-that-are-generated-by-the-installation-of-the-hotfix"></a>修正プログラムのインストールによって生成された競合を解決
場合によっては、メタデータ修正プログラム パッケージに、上位モデルでカスタマイズされていたオブジェクトへの変更が含まれています。 この場合、インストール プロセスは修正プログラムのインストール後に解決する必要がある競合を自動的に生成します。 開発ツールを使用すると、競合しているすべての品目をグループ化するプロジェクトを作成することができます。 たとえば、VendTable フォームをカスタマイズするアプリケーション スイート パッケージに VAR レイヤー モデルがあり、SYS レイヤ モデルで VendTable フォームを変更する修正プログラムをインストールする場合、VAR レイヤ モデルで競合が発生する可能性があります。

1.  **Dynamics 365** &gt; **アドイン** &gt; **競合からプロジェクトを作成する**とクリックします。
2.  ダイアログ ボックスで、モデルを選択して競合を確認します。
3.  **プロジェクトの作成** をクリックします。 修正プログラムが適用された後に競合していることが見つかった選択しているモデルの要素のみを含むプロジェクトが生成されます。
4.  競合する要素のデザイナーを開いて、表示されたツールを使って競合を表示し、解決します。

<!--The Office Mix at <https://mix.office.com/watch/1rl75ei2cs6d7> provides an introduction to the conflict resolution tools in the development environment.-->

## <a name="build-and-test-on-a-local-vm"></a>ローカル VM のビルドおよびテスト
修正プログラムの影響を受けるすべてのモデルをビルドし、アプリケーションをテストします。

## <a name="check-pending-changes-in-to-version-control"></a>バージョン管理の保留中の変更のチェック
この更新プログラムに関連するすべての変更で問題がなければ、Microsoft Visual Studio のチーム エクスプローラーを使用して、保留中の変更を Azure DevOps にチェックインします。 **コメント**フィールドにコメントを入力し、**チェック イン**をクリックします。 ソース コード リポジトリには、変更の履歴が維持されます。 

> [!NOTE]
> ビルドとテストの自動化にビルド環境を使用する場合、ビルドの自動化プロセスは、Azure DevOps プロジェクトにあるメタデータの修正プログラム ファイルを作成できます。 それが属しているモデルの記述子ファイルがバージョン管理にチェックインする場合にのみ、修正プログラムを構築できます。 たとえば、修正プログラムのインストール プロセスがディレクトリ モデル (このファイルは保留中の変更の一覧に表示されます) が属しているファイルを変更した場合、ディレクトリ モデル (c:\\AOSService\\PackagesLocalDirectory\\ディレクトリ\\記述子\\Directory.xml) の記述子ファイルが既に Azure DevOps プロジェクトにチェックインされていることを確認します。 チェックインされていない場合は、ソース管理エクスプローラーを使用してチェックインする前に、追加保留中の変更の一覧に追加します。 

[![保留中の変更のリストに記述子ファイルを手動で追加します](./media/configureinstallhotfix-8.png)](./media/configureinstallhotfix-8.png)

## <a name="synchronize-other-development-vms"></a>その他の開発 VM を同期
この記事で記載されているように、修正プログラムが開発 VM でインストールされた後、再インストール、競合の解決、同じ Azure DevOps プロジェクトに接続されている他の開発 VMでの検証をする必要はありません。 同じ Azure DevOps プロジェクトに接続されている開発者とテスターは、ローカル VM に変更を同期させてビルドするだけで済みます。

## <a name="deploy"></a>配置
開発環境にメタデータの修正プログラムを適用した後、競合を解決し、変更を検証したら、配置可能パッケージを作成しテスト環境またはサンドボックス環境に変更する必要があります。 ビルドとテストの自動化にビルド インスタンスを使用すると、ビルド プロセスによって配置可能なパッケージが自動的に作成されます。 詳細については、[配置可能パッケージの作成](../deployment/create-apply-deployable-package.md)を参照してください。

