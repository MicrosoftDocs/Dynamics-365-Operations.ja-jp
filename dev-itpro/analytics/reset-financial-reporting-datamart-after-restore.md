---
title: "データベースを復元すると財務報告のデータ マートをリセットします。"
description: "このトピックでは、データベースのMicrosoft Dynamics 365を復元すると財務報告のデータ マートをリセットする方法について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>データベースを復元すると財務報告のデータ マートをリセットします。

このトピックでは、データベースのMicrosoft Dynamics 365を復元すると財務報告のデータ マートをリセットする方法について説明します。 

バックアップの工程のデータベース365 for Operationsを復元するか、または別の環境のデータベースをコピーする必要がある場合は、複数のシナリオがあります。 このような場合は、財務報告のデータ マート データベースが工程に対して正しく復元された365 for Operationsを使用することを保証するための適切な手順に従う必要があります。 工程のデータベース365 for Operationsの復元の外の場合に、財務報告のデータ マートの再設定の質問がある場合は、参照して、[Management Reporterデータ マート リセットします] (詳細についてはhttps://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/)を。 このプロセスのステップが工程の月5日の2016リリース (アプリケーションの自動作成7.0.1265.23014および財務報告に基づきます7.0.10000.4)、新しいリリース365 for Operationsでサポートされていることに注意してください。 Dynamics 365 for Operationsの以前のリリースがある場合は、サポートの特定のチーム サポートに問い合わせてください。

## <a name="export-report-definitions"></a>レポート定義をエクスポートします。
最初に、次の手順を使用してレポート デザイナーで、レポートのデザインをエクスポートします:

1.  レポート デザイナーで、会社レポート パーツ グループは** ** &gt; ** **実行されます。
2.  レポート パーツ グループをエクスポートするように選択クリックして**エクスポート**。 **注記:、一つのレポート パーツ グループのみ**、Dynamics 365 for Operationsし、サポートされますが、**既定**。
3.  エクスポートするレポート定義を選択します:
    -   すべてのレポート定義および関連する構成要素をエクスポートするには、[**すべて選択**] をクリックします。
    -   特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブをクリックしてエクスポートする項目を選択します。 タブ内の複数の項目を選択するには、Ctrl キーを押しながら選択します。 エクスポートするレポートを選択すると、関連する行、列、ツリー、分析コードセットが選択されます。

4.  [**エクスポート**。
5.  ファイル名を入力し、エクスポートするレポート定義を保存する安全な場所を選択します。
6.  Click **Save**.

ファイルは、安全な場所にコピーするか、またはアップロードすることができます。別のときに三つ環境にインポートするように、そのします。 MicrosoftのAzureの保管勘定の使用に関する情報が検索できますAzCopyコマンドラインUtilityの[] (https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy)からデータを転送する。 **注記: ** Microsoftは、工程の契約に365 for Operationsの一部として保管勘定は表示されません。 記憶域勘定を購入するか、または別のAzureの定期売買の記憶域アカウントを使用する必要があります。 **重要: ** Azureの仮想機械のDのドライブの動作を確認してください。 エクスポートされたレポート パーツ グループを完全に、ここで保たないでします。 一時ドライブに関する詳細については、表示、[Windows Azureの仮想機械理解します (https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)]の数量をドライブ。

## <a name="stop-services"></a>サービスを停止します。
環境のすべてのコンピュータに接続し、services.mscを使用して、次のWindowsサービスを停止するでリモート デスクトップを使用します:

-   World Wide Webで配送サービス (すべてのAOSコンピュータ) 
-   工程のバッチ管理サービスのMicrosoft Dynamics 365 (、プライベートAOSコンピューターのみ) 
-   Management Reporter 2012のプロセス サービス (BIコンピューターのみ) 

これらのサービス、工程のデータベースのDynamics 365に対する未処理接続があります。

## <a name="reset"></a>リセット
#### <a name="locate-the-latest-dataupgradezip-package"></a>最新のDataUpgrade.zipパッケージを指定します。

ある方向を使用して、最新のDataUpgrade.zipパッケージで指定します。[DataUpgrade.zipのスクリプトをダウンロードします。] (。\migration-upgrade\upgrade-data-to-latest-update.md)。 方向は、環境のデータ アップグレード梱包の正しいバージョンの検索方法を説明します。

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>工程のデータベースのDynamics 365に対してスクリプトを実行します。

工程のデータベースのDynamics 365に対して次のスクリプトが実行していない (財務報告のデータベースに対して)。

-   DataUpgrade.zip\\AosService\\\\ConfigureAxReportingIntegration.sqlのスクリプトが書き込まれます
-   DataUpgrade.zip\\AosService\\\\GrantAzViewChangeTracking.sqlのスクリプトが書き込まれます

これらのユーザー スクリプトは、ロールと変更の追跡の設定が正しいことを確認します。

#### <a name="execute-powershell-command-to-reset-database"></a>データベースをリセットするPowerShellコマンドを実行します。

工程と財務報告365 for Operationsの間の統合をリセットするAOSコンピューターで次のコマンドを一つずつ、実行します:

1.  管理者として開いているウィンドウPowerShell。
2.  実行します: F:
3.  実行します: CD F:\\MRApplicationService\\MRInstallDirectory
4.  実行します: インポート モジュール。\\サーバー\\MRDeploy\\MRDeploy.psd1
5.  実行します: リセットDatamartIntegrationリストの担当者は組織ReasonDetailリセットします (「&lt;の場合の理由」
    -   確認「Y」を入力するように求められます。

パラメータの説明:

-   有効な値の-理由は次のとおりです: [BADDATA、そのサービス。
-   [ReasonDetailパラメータは自由書式のです。
-   理由とreasonDetailはテレメトリー/環境では監視に記録されます。

## <a name="start-services"></a>サービスを開始します。
[先に停止したサービスを再起動するのにservices.mscを使用します:

-   World Wide Webで配送サービス (すべてのAOSコンピュータ) 
-   工程のバッチ管理サービスのMicrosoft Dynamics 365 (、プライベートAOSコンピューターのみ) 
-   Management Reporter 2012のプロセス サービス (BIコンピューターのみ) 

## <a name="import-report-definitions"></a>レポート定義をインポートします。
エクスポート中に作成されたファイルを使用してレポート デザイナーでレポートのデザインをインポートします:

1.  レポート デザイナーで、会社レポート パーツ グループは** ** &gt; ** **実行されます。
2.  レポート パーツ グループをエクスポートするように選択クリックして**エクスポート**。 **注記:、一つのレポート パーツ グループのみ**、Dynamics 365 for Operationsし、サポートされますが、**既定**。
3.  **既定**レポート パーツを選択し、をクリックしてインポート** **。
4.  含むファイルをエクスポートするレポート定義し、をクリックして** **開きます。
5.  [インポート] ダイアログ ボックスで、インポートするレポート定義を選択します:
    -   すべてのレポート定義およびサポートする構成要素をインポートするには、[**すべて選択**] をクリックします。
    -   特定のレポート、行、列、ツリー、または分析コード セットをインポートするには、インポートするレポート、行、列、ツリー、または分析コード セットを選択します。

6.  Click **Import**.



