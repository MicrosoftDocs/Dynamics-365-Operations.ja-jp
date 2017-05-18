---
title: "データベースを復元した後の財務報告のデータ マートのリセット"
description: "このトピックでは、Microsoft Dynamics 365 for Operations のデータベースを復元した後に、財務報告データ マートをリセットする方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d4ce390c62cbfb1f693410b004aa296c0ed75eb2
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>データベースを復元した後の財務報告のデータ マートのリセット

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Operations のデータベースを復元した後に、財務報告データ マートをリセットする方法について説明します。 

Dynamics 365 for Operations のデータベースをバックアップから復元するか、または別の環境のデータベースをコピーする必要がある場合があります。 これが発生した場合は、適切な手順に従って、財務報告データマートが、復元された Dynamics 365 for Operations のデータベースを正しく使用している必要があります。 Dynamics 365 for Operations のデータベースを復元する以外の理由で財務報告データマートをリセットするにおいて質問がある場合は、[財務報告のデータ マートの再設定](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) を参照してください。 このプロセスの手順は、Dynamics 365 for Operation 2016 年 5 月のリリース (アプリ ビルド 7.0.1265.23014 および財務報告ビルド 7.0.10000.4) およびそれ以降のリリースでサポートされています。 Dynamics 365 for Operations の以前のリリースを持っている場合、サポート チームに問い合わせてください。

## <a name="export-report-definitions"></a>レポート定義のエクスポート
最初に、次の手順を使用してレポート デザイナーにあるレポート デザインをエクスポートします:

1.  レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。
2.  エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。 **注記:** Dynamics 365 for Operation では、**既定** として 1 つの構成要素グループのみがサポートされます。
3.  エクスポートするレポート定義を選択します:
    -   すべてのレポート定義および関連する構成要素をエクスポートするには、[**すべて選択**] をクリックします。
    -   特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブをクリックしてエクスポートする項目を選択します。 タブ内の複数の項目を選択するには、Ctrl キーを押しながら選択します。 エクスポートするレポートを選択すると、関連する行、列、ツリー、および分析コード セットが選択されます。

4.  [**エクスポート**] をクリックします。
5.  ファイル名を入力し、エクスポートされたレポート定義を保存できる安全な場所を選択します。
6.  [**保存**] をクリックします。

ファイルは、安全な場所にコピーまたはアップロードすることができ、別のときに異なる環境にインポートできるようになります。 Microsoft Azure ストレージ アカウントの使用に関する情報は、[AzCopy Command-Line Utility でデータを転送する](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy) を参照してください。 
> [!NOTE]
> Microsoft は、Dynamics 365 for Operations の契約の一部としてストレージ アカウントを提供しません。 ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。 
> [!WARNING]
> Azure 仮想マシン上の D ドライブの動作に注意してください。 エクスポートされた構成要素グループをここに永久に保管しないでください。 テンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) を参照してください。

## <a name="stop-services"></a>サービスの停止
リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。

-   ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
-   Microsoft Dynamics 365 for Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)
-   Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

これらのサービスでは、Dynamics 365 for Operations のデータベースへの接続が提供されます。

## <a name="reset"></a>リセット
#### <a name="locate-the-latest-dataupgradezip-package"></a>最新の DataUpgrade.zip パッケージを検索します。

[DataUpgrade.zip スクリプトのダウンロード](..\migration-upgrade\upgrade-data-to-latest-update.md) に記載されている指示に従って最新の DataUpgrade.zip パッケージを検索します。 指示では、使用している環境に適したバージョンのデータ アップグレード パッケージを検索する方法を説明しています。

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Dynamics 365 for Operations データベースに対してスクリプトを実行する

財務レポート データベースに対してではなく、Dynamics 365 for Operations データベースに対して、次のスクリプトを実行します。

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを確認します。

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell コマンドを実行してデータベースをリセットする

Dynamics 365 for Operations と財務レポートとの統合をリセットするには、AOS コンピュータで直接次のコマンドを実行します。

1.  Windows PowerShell を管理者として開きます。
2.  実行: F:
3.  実行: cd F:\\MRApplicationService\\MRInstallDirectorytory
4.  実行: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  実行: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;リセットの理由&gt;”
    -   確認のために「Y」を入力するよう求められます。

パラメーターの説明:

-   -Reason の有効な値は、SERVICING, BADDATA, OTHER です。
-   -ReasonDetail パラメーターは自由書式です。
-   理由と reasonDetail はテレメトリーまたは環境モニタリングに記録されます。

## <a name="start-services"></a>サービスを開始します。
services.msc を使用して、以前に停止したサービスを再起動します。

-   ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
-   Microsoft Dynamics 365 for Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)
-   Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

## <a name="import-report-definitions"></a>レポート定義のインポート
エクスポート中に作成されたファイルを使用して、レポート デザイナーからレポート デザインをインポートします:

1.  レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。
2.  エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。 
    > [!NOTE]
    > Dynamics 365 for Operation では、**既定** として 1 つの構成要素グループのみがサポートされます。
3.  **既定** の構成要素を選択し、[**インポート**] をクリックします。
4.  エクスポート済みのレポート定義を選択し、[**開く**] をクリックします。
5.  [インポート] ダイアログ ボックスで、インポートするレポート定義を選択します:
    -   すべてのレポート定義およびサポートする構成要素をインポートするには、[**すべて選択**] をクリックします。
    -   特定のレポート、行、列、ツリー、または分析コード セットをインポートするには、インポートするレポート、行、列、ツリー、または分析コード セットを選択します。

6.  [**インポート**] をクリックします。





