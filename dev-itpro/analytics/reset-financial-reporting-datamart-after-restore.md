---
title: "データベースを復元した後の財務報告のデータ マートのリセット"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを復元した後に、財務報告データ マートをリセットする方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="ab184-103">データベースを復元した後の財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="ab184-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ab184-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを復元した後に、財務報告データ マートをリセットする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab184-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="ab184-105">Finance and Operations データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このトピックのステップに従って、財務報告のデータ マートが復元したFinance and Operations データベースを正しく使用していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab184-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="ab184-106">このプロセスのステップは、Dynamics 365 for Operation 2016 年 5 月のリリース (アプリ ビルド 7.0.1265.23014 および財務報告ビルド 7.0.10000.4) およびそれ以降のリリースでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ab184-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="ab184-107">Finance and Operations の以前のリリースを持っている場合は、サポート チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="ab184-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="ab184-108">レポート定義のエクスポート</span><span class="sxs-lookup"><span data-stu-id="ab184-108">Export report definitions</span></span>
<span data-ttu-id="ab184-109">最初に、次の手順を使用してレポート デザイナーにあるレポート デザインをエクスポートします:</span><span class="sxs-lookup"><span data-stu-id="ab184-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="ab184-110">レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ab184-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="ab184-111">エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="ab184-112">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ab184-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="ab184-113">エクスポートするレポート定義を選択します:</span><span class="sxs-lookup"><span data-stu-id="ab184-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="ab184-114">すべてのレポート定義および関連する構成要素をエクスポートするには、[**すべて選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="ab184-115">特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブをクリックしてエクスポートする項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab184-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="ab184-116">タブ内の複数の項目を選択するには、Ctrl キーを押しながら選択します。</span><span class="sxs-lookup"><span data-stu-id="ab184-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="ab184-117">エクスポートするレポートを選択すると、関連する行、列、ツリー、および分析コード セットが選択されます。</span><span class="sxs-lookup"><span data-stu-id="ab184-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="ab184-118">[**エクスポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-118">Click **Export**.</span></span>
5.  <span data-ttu-id="ab184-119">ファイル名を入力し、エクスポートされたレポート定義を保存できる安全な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab184-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="ab184-120">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-120">Click **Save**.</span></span>

<span data-ttu-id="ab184-121">ファイルは、安全な場所にコピーまたはアップロードすることができ、別のときに異なる環境にインポートできるようになります。</span><span class="sxs-lookup"><span data-stu-id="ab184-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="ab184-122">Microsoft Azure ストレージ アカウントの使用に関する情報は、[AzCopy Command-Line Utility でデータを転送する](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab184-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="ab184-123">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="ab184-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="ab184-124">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab184-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="ab184-125">Azure 仮想マシン上の D ドライブの動作に注意してください。</span><span class="sxs-lookup"><span data-stu-id="ab184-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="ab184-126">エクスポートされた構成要素グループをここに永久に保管しないでください。</span><span class="sxs-lookup"><span data-stu-id="ab184-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="ab184-127">テンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab184-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="ab184-128">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="ab184-128">Stop services</span></span>
<span data-ttu-id="ab184-129">リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="ab184-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="ab184-130">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="ab184-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="ab184-131">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="ab184-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="ab184-132">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="ab184-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="ab184-133">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="ab184-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="ab184-134">リセット</span><span class="sxs-lookup"><span data-stu-id="ab184-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="ab184-135">最新の MinorVersionDataUpgrade.zip パッケージを検索してダウンロードする</span><span class="sxs-lookup"><span data-stu-id="ab184-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="ab184-136">「[最新のデータ アップグレード配置可能パッケージをダウンロードする](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package)」に記載されている指示に従って、最新の MinorVersionDataUpgrade.zip パッケージを検索します。</span><span class="sxs-lookup"><span data-stu-id="ab184-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="ab184-137">指示では、正しいバージョンのデータ アップグレード パッケージを検索してダウンロードする方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="ab184-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="ab184-138">MinorVersionDataUpgrade.zip パッケージをダウンロードするのにアップグレードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ab184-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="ab184-139">MinorVersionDataUpgrade.zip パッケージのコピーを取得するには、記事の他のステップは実行せずに、ただ「最新のデータ アップグレード配置可能パッケージをダウンロードする」セクションにあるステップのみ完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab184-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="ab184-140">Finance and Operations データベースに対してスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="ab184-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="ab184-141">財務レポート データベースに対してではなく、Finance and Operations データベースに対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="ab184-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="ab184-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="ab184-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="ab184-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="ab184-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="ab184-144">これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ab184-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="ab184-145">PowerShell コマンドを実行してデータベースをリセットする</span><span class="sxs-lookup"><span data-stu-id="ab184-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="ab184-146">Finance and Operations と財務レポートとの統合をリセットするには、AOS コンピュータで直接次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ab184-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="ab184-147">Windows PowerShell を管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="ab184-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="ab184-148">実行: F:</span><span class="sxs-lookup"><span data-stu-id="ab184-148">Execute: F:</span></span>
3.  <span data-ttu-id="ab184-149">実行: cd F:\\MRApplicationService\\MRInstallDirectorytory</span><span class="sxs-lookup"><span data-stu-id="ab184-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="ab184-150">実行: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="ab184-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="ab184-151">実行: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;リセットの理由&gt;”</span><span class="sxs-lookup"><span data-stu-id="ab184-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="ab184-152">確認のために「Y」を入力するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="ab184-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="ab184-153">パラメーターの説明:</span><span class="sxs-lookup"><span data-stu-id="ab184-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="ab184-154">-Reason の有効な値は、SERVICING, BADDATA, OTHER です。</span><span class="sxs-lookup"><span data-stu-id="ab184-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="ab184-155">-ReasonDetail パラメーターは自由書式です。</span><span class="sxs-lookup"><span data-stu-id="ab184-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="ab184-156">理由と reasonDetail はテレメトリーまたは環境モニタリングに記録されます。</span><span class="sxs-lookup"><span data-stu-id="ab184-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="ab184-157">サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="ab184-157">Start services</span></span>
<span data-ttu-id="ab184-158">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="ab184-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="ab184-159">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="ab184-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="ab184-160">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="ab184-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="ab184-161">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="ab184-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="ab184-162">レポート定義のインポート</span><span class="sxs-lookup"><span data-stu-id="ab184-162">Import report definitions</span></span>
<span data-ttu-id="ab184-163">エクスポート中に作成されたファイルを使用して、レポート デザイナーからレポート デザインをインポートします:</span><span class="sxs-lookup"><span data-stu-id="ab184-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="ab184-164">レポート デザイナーで、[**会社**] &gt; [**構成要素グループ**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ab184-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="ab184-165">エクスポートする構成要素グループを選択し、[**エクスポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ab184-166">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ab184-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="ab184-167">**既定** の構成要素を選択し、[**インポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="ab184-168">エクスポート済みのレポート定義を選択し、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="ab184-169">[インポート] ダイアログ ボックスで、インポートするレポート定義を選択します:</span><span class="sxs-lookup"><span data-stu-id="ab184-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="ab184-170">すべてのレポート定義およびサポートする構成要素をインポートするには、[**すべて選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="ab184-171">特定のレポート、行、列、ツリー、または分析コード セットをインポートするには、インポートするレポート、行、列、ツリー、または分析コード セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab184-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="ab184-172">[**インポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab184-172">Click **Import**.</span></span>





