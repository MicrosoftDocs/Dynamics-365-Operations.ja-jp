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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="ef130-103">データベースを復元した後の財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="ef130-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef130-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを復元した後に、財務報告データ マートをリセットする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ef130-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="ef130-105">Finance and Operations データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このトピックのステップに従って、財務報告のデータ マートが復元したFinance and Operations データベースを正しく使用していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef130-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="ef130-106">このプロセスのステップは、Dynamics 365 for Operation 2016 年 5 月のリリース (アプリ ビルド 7.0.1265.23014 および財務報告ビルド 7.0.10000.4) およびそれ以降のリリースでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ef130-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="ef130-107">Finance and Operations の以前のリリースを持っている場合は、サポート チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="ef130-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="ef130-108">レポート定義のエクスポート</span><span class="sxs-lookup"><span data-stu-id="ef130-108">Export report definitions</span></span>
<span data-ttu-id="ef130-109">最初に、次の手順を使用してレポート デザイナーにあるレポート デザインをエクスポートします:</span><span class="sxs-lookup"><span data-stu-id="ef130-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="ef130-110">レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef130-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="ef130-111">エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="ef130-112">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ef130-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="ef130-113">エクスポートするレポート定義を選択します:</span><span class="sxs-lookup"><span data-stu-id="ef130-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="ef130-114">すべてのレポート定義および関連する構成要素をエクスポートするには、[**すべて選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="ef130-115">特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブをクリックしてエクスポートする項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef130-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="ef130-116">タブ内の複数の項目を選択するには、Ctrl キーを押しながら選択します。エクスポートするレポートを選択したとき、関連する行、列、ツリー、分析コードセットが選択されます。</span><span class="sxs-lookup"><span data-stu-id="ef130-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="ef130-117">[**エクスポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-117">Click **Export**.</span></span>
5.  <span data-ttu-id="ef130-118">ファイル名を入力し、エクスポートされたレポート定義を保存できる安全な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef130-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="ef130-119">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-119">Click **Save**.</span></span>

<span data-ttu-id="ef130-120">ファイルは、安全な場所にコピーまたはアップロードすることができ、別のときに異なる環境にインポートできるようになります。</span><span class="sxs-lookup"><span data-stu-id="ef130-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="ef130-121">Microsoft Azure ストレージ アカウントの使用に関する情報は、[AzCopy Command-Line Utility でデータを転送する](/azure/storage/storage-use-azcopy) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef130-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="ef130-122">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="ef130-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="ef130-123">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef130-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="ef130-124">Azure 仮想マシン上の D ドライブの動作に注意してください。</span><span class="sxs-lookup"><span data-stu-id="ef130-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="ef130-125">エクスポートされた構成要素グループをここに永久に保管しないでください。</span><span class="sxs-lookup"><span data-stu-id="ef130-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="ef130-126">テンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef130-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="ef130-127">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="ef130-127">Stop services</span></span>
<span data-ttu-id="ef130-128">リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="ef130-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="ef130-129">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="ef130-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="ef130-130">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="ef130-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="ef130-131">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="ef130-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="ef130-132">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="ef130-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="ef130-133">リセット</span><span class="sxs-lookup"><span data-stu-id="ef130-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="ef130-134">最新の MinorVersionDataUpgrade.zip パッケージを検索してダウンロードする</span><span class="sxs-lookup"><span data-stu-id="ef130-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="ef130-135">「[最新のデータ アップグレード配置可能パッケージをダウンロードする](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages)」に記載されている指示に従って、最新の MinorVersionDataUpgrade.zip パッケージを検索します。</span><span class="sxs-lookup"><span data-stu-id="ef130-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="ef130-136">指示では、正しいバージョンのデータ アップグレード パッケージを検索してダウンロードする方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="ef130-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="ef130-137">MinorVersionDataUpgrade.zip パッケージをダウンロードするのにアップグレードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ef130-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="ef130-138">MinorVersionDataUpgrade.zip パッケージのコピーを取得するには、記事の他のステップは実行せずに、ただ「最新のデータ アップグレード配置可能パッケージをダウンロードする」セクションにあるステップのみ完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef130-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="ef130-139">Finance and Operations データベースに対してスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="ef130-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="ef130-140">財務レポート データベースに対してではなく、Finance and Operations データベースに対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="ef130-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="ef130-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="ef130-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="ef130-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="ef130-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="ef130-143">これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef130-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="ef130-144">PowerShell コマンドを実行してデータベースをリセットする</span><span class="sxs-lookup"><span data-stu-id="ef130-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="ef130-145">AOS コンピュータで、Finance and Operations と財務レポートとの統合をリセットするには、PowerShell で管理者として次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ef130-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="ef130-146">コマンドを実行した後、確認のために「Y」を入力するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="ef130-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="ef130-147">パラメーターの説明:</span><span class="sxs-lookup"><span data-stu-id="ef130-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="ef130-148">-Reason の有効な値は、SERVICING, BADDATA, OTHER です。</span><span class="sxs-lookup"><span data-stu-id="ef130-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="ef130-149">-ReasonDetail パラメーターは自由書式です。</span><span class="sxs-lookup"><span data-stu-id="ef130-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="ef130-150">理由と reasonDetail はテレメトリーまたは環境モニタリングに記録されます。</span><span class="sxs-lookup"><span data-stu-id="ef130-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="ef130-151">サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="ef130-151">Start services</span></span>
<span data-ttu-id="ef130-152">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="ef130-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="ef130-153">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="ef130-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="ef130-154">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="ef130-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="ef130-155">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="ef130-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="ef130-156">レポート定義のインポート</span><span class="sxs-lookup"><span data-stu-id="ef130-156">Import report definitions</span></span>
<span data-ttu-id="ef130-157">エクスポート中に作成されたファイルを使用して、レポート デザイナーからレポート デザインをインポートします:</span><span class="sxs-lookup"><span data-stu-id="ef130-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="ef130-158">レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef130-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="ef130-159">エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ef130-160">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ef130-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="ef130-161">**既定** の構成要素を選択し、[**インポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="ef130-162">エクスポート済みのレポート定義を選択し、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="ef130-163">[インポート] ダイアログ ボックスで、インポートするレポート定義を選択します:</span><span class="sxs-lookup"><span data-stu-id="ef130-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="ef130-164">すべてのレポート定義およびサポートする構成要素をインポートするには、[**すべて選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="ef130-165">特定のレポート、行、列、ツリー、または分析コード セットをインポートするには、インポートするレポート、行、列、ツリー、または分析コード セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef130-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="ef130-166">[**インポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef130-166">Click **Import**.</span></span>





