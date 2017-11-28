---
title: "データベースを復元した後の財務報告のデータ マートのリセット"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを復元した後に、財務報告データ マートをリセットする方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>データベースを復元した後の財務報告のデータ マートのリセット

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを復元した後に、財務報告データ マートをリセットする方法について説明します。

Finance and Operations データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このトピックのステップに従って、財務報告のデータ マートが復元したFinance and Operations データベースを正しく使用していることを確認する必要があります。 
> [!Note] 
> このプロセスのステップは、Dynamics 365 for Operation 2016 年 5 月のリリース (アプリ ビルド 7.0.1265.23014 および財務報告ビルド 7.0.10000.4) およびそれ以降のリリースでサポートされています。 Finance and Operations の以前のリリースを持っている場合は、サポート チームに問い合わせてください。

## <a name="export-report-definitions"></a>レポート定義のエクスポート
最初に、次の手順を使用してレポート デザイナーにあるレポート デザインをエクスポートします:

1.  レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。
2.  エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。 

    > [!Note] 
    > Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。
    
3.  エクスポートするレポート定義を選択します:
    -   すべてのレポート定義および関連する構成要素をエクスポートするには、[**すべて選択**] をクリックします。
    -   特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブをクリックしてエクスポートする項目を選択します。 タブ内の複数の項目を選択するには、Ctrl キーを押しながら選択します。エクスポートするレポートを選択したとき、関連する行、列、ツリー、分析コードセットが選択されます。

4.  [**エクスポート**] をクリックします。
5.  ファイル名を入力し、エクスポートされたレポート定義を保存できる安全な場所を選択します。
6.  [**保存**] をクリックします。

ファイルは、安全な場所にコピーまたはアップロードすることができ、別のときに異なる環境にインポートできるようになります。 Microsoft Azure ストレージ アカウントの使用に関する情報は、[AzCopy Command-Line Utility でデータを転送する](/azure/storage/storage-use-azcopy) を参照してください。 
> [!NOTE]
> Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。 ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。 
> [!WARNING]
> Azure 仮想マシン上の D ドライブの動作に注意してください。 エクスポートされた構成要素グループをここに永久に保管しないでください。 テンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) を参照してください。

## <a name="stop-services"></a>サービスの停止
リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。

-   ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
-   Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)
-   Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。

## <a name="reset"></a>リセット
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>最新の MinorVersionDataUpgrade.zip パッケージを検索してダウンロードする

「[最新のデータ アップグレード配置可能パッケージをダウンロードする](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages)」に記載されている指示に従って、最新の MinorVersionDataUpgrade.zip パッケージを検索します。 指示では、正しいバージョンのデータ アップグレード パッケージを検索してダウンロードする方法を説明しています。 MinorVersionDataUpgrade.zip パッケージをダウンロードするのにアップグレードは必要ありません。 MinorVersionDataUpgrade.zip パッケージのコピーを取得するには、記事の他のステップは実行せずに、ただ「最新のデータ アップグレード配置可能パッケージをダウンロードする」セクションにあるステップのみ完了する必要があります。

### <a name="execute-scripts-against-finance-and-operations-database"></a>Finance and Operations データベースに対してスクリプトを実行する

財務レポート データベースに対してではなく、Finance and Operations データベースに対して、次のスクリプトを実行します。

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを確認します。

### <a name="execute-powershell-command-to-reset-database"></a>PowerShell コマンドを実行してデータベースをリセットする

AOS コンピュータで、Finance and Operations と財務レポートとの統合をリセットするには、PowerShell で管理者として次のコマンドを実行します。

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> コマンドを実行した後、確認のために「Y」を入力するよう求められます。

パラメーターの説明:

-   -Reason の有効な値は、SERVICING, BADDATA, OTHER です。
-   -ReasonDetail パラメーターは自由書式です。
-   理由と reasonDetail はテレメトリーまたは環境モニタリングに記録されます。

## <a name="start-services"></a>サービスを開始します。
services.msc を使用して、以前に停止したサービスを再起動します。

-   ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
-   Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)
-   Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

## <a name="import-report-definitions"></a>レポート定義のインポート
エクスポート中に作成されたファイルを使用して、レポート デザイナーからレポート デザインをインポートします:

1.  レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。
2.  エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。 

    > [!NOTE]
    > Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。
    
3.  **既定** の構成要素を選択し、[**インポート**] をクリックします。
4.  エクスポート済みのレポート定義を選択し、[**開く**] をクリックします。
5.  [インポート] ダイアログ ボックスで、インポートするレポート定義を選択します:
    -   すべてのレポート定義およびサポートする構成要素をインポートするには、[**すべて選択**] をクリックします。
    -   特定のレポート、行、列、ツリー、または分析コード セットをインポートするには、インポートするレポート、行、列、ツリー、または分析コード セットを選択します。

6.  [**インポート**] をクリックします。





