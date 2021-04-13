---
title: 財務報告のデータ マートのリセット
description: このトピックでは、Microsoft Dynamics 365 Finance の財務報告データ マートをリセットする方法について説明します。
author: aprilolson
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: IT Pro, Developer
ms.reviewer: kfend
ms.custom: 261824
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6e0b209907a1168616cbbddfa310ca2c3d75f94
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754334"
---
# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="6f889-103">財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="6f889-103">Reset the Financial reporting data mart</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f889-104">このトピックでは、 Microsoft Dynamics 365 Finance での Financial Reporting のリセット方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6f889-104">This topic explains how to reset the Financial reporting data mart for Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="6f889-105">データマートは、ユーザーの役割 と クライアント や インフラストラクチャー へのアクセス権に応じて、複数の方法でリセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f889-105">The data mart can be reset in multiple ways, depending on the user's role and access to the client or infrastructure.</span></span>

<span data-ttu-id="6f889-106">データマートのリセットは、データベース で あまり処理が行われていないときだけに留めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="6f889-106">You should reset the data mart only when a small amount of processing is occurring on the database.</span></span> <span data-ttu-id="6f889-107">財務諸表は、リセット プロセス中は使用できません。</span><span class="sxs-lookup"><span data-stu-id="6f889-107">Financial reporting will be unavailable during the reset process.</span></span>

> [!NOTE]
> <span data-ttu-id="6f889-108">データ マートのリセットが必要なことを確認するには、[データ マートをリセットする場合](when-to-reset-data-mart.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f889-108">To confirm that it's necessary to reset your data mart, see [When to reset a data mart](when-to-reset-data-mart.md).</span></span>

> <span data-ttu-id="6f889-109">データマートのリセットは、レポートの構造を定義しているレポートの定義には影響しません。</span><span class="sxs-lookup"><span data-stu-id="6f889-109">A reset of the data mart doesn't affect any report definitions that define the structure of reports.</span></span> <span data-ttu-id="6f889-110">しかし、レポートのエクスポートを実行してバックアップを取っておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f889-110">Nevertheless, it's always a good idea to have a backup of your reports, which you accomplish by exporting them.</span></span> <span data-ttu-id="6f889-111">レポート定義をエクスポートする手順は、このトピックの後半にあるレポート定義のエクスポートとインポートという名前のセクションの最後に記載されています。</span><span class="sxs-lookup"><span data-stu-id="6f889-111">The steps for exporting report definitions are included at the end of this topic in the section titled, Export and import report definitions, later in this topic.</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="6f889-112">レポート デザイナーからの財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="6f889-112">Reset the Financial reporting data mart from Report designer</span></span>

<span data-ttu-id="6f889-113">レポート デザイナーのバージョンを検索するには、次のビデオをご覧ください: [レポート デザイナーのバージョンを検索する方法](https://www.youtube.com/watch?v=icfA5Q3kp4w)</span><span class="sxs-lookup"><span data-stu-id="6f889-113">To find the version of report designer, watch this video: [How to find the version of Report designer](https://www.youtube.com/watch?v=icfA5Q3kp4w)</span></span>

<span data-ttu-id="6f889-114">レポート デザイナーでデータマートをリセットするには、 以下の図に示されているように、 **ツール** メニューで **データマートのリセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-114">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart** as shown in the following illustration.</span></span> <span data-ttu-id="6f889-115">表示されるダイアログ ボックスには2つのセクションがあります: **統計** および **リセット**。</span><span class="sxs-lookup"><span data-stu-id="6f889-115">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="6f889-116">[![データ マートのダイアログ ボックスをリセットします](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="6f889-116">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="6f889-117">統合試行回数</span><span class="sxs-lookup"><span data-stu-id="6f889-117">Integration attempts</span></span>

<span data-ttu-id="6f889-118">**統合試行回数** グリッドは、システムがトランザクションの統合を試みた回数を表示します。</span><span class="sxs-lookup"><span data-stu-id="6f889-118">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="6f889-119">システムは、最初のいくつかの試行ができなかった場合は、日の期間にわたってデータを統合するまで続行されます。</span><span class="sxs-lookup"><span data-stu-id="6f889-119">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="6f889-120">試行回数が8回以上の場合、および分析コードの組み合わせやトランザクション レコードが多い場合、データ マートをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f889-120">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="6f889-121">このような状況では、データはレポートされません。</span><span class="sxs-lookup"><span data-stu-id="6f889-121">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="6f889-122">データのステータス</span><span class="sxs-lookup"><span data-stu-id="6f889-122">Data status</span></span>

<span data-ttu-id="6f889-123">**データのステータス** グリッドは、データ マート内のトランザクション、為替レート、および分析コード値のスナップショットを表示します。</span><span class="sxs-lookup"><span data-stu-id="6f889-123">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="6f889-124">古いレコードが多数ある場合、レコードに対して更新が数多く存在することになります。</span><span class="sxs-lookup"><span data-stu-id="6f889-124">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="6f889-125">この場合は、レポートの生成に要する時間が長くなることがあります。</span><span class="sxs-lookup"><span data-stu-id="6f889-125">This situation might increase the time that is required to generate reports.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="6f889-126">正しく整合されていない主勘定カテゴリ</span><span class="sxs-lookup"><span data-stu-id="6f889-126">Misaligned main account categories</span></span>

<span data-ttu-id="6f889-127">財務報告 7.2.1 以前のリリースを使用している場合で、勘定の名前を変更して勘定カテゴリの間で勘定を移動する場合、データ マートをリセットする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="6f889-127">If you're using a release that is earlier than Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="6f889-128">これらのアクションにより、主勘定カテゴリが正しく整合されなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="6f889-128">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="6f889-129">**正しく整合されていない主勘定カテゴリ** フィールドには問題が発生しているかどうかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f889-129">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-and-select-a-reason"></a><span data-ttu-id="6f889-130">データマートをリセットし、理由をひとつ選択してください</span><span class="sxs-lookup"><span data-stu-id="6f889-130">Reset the data mart and select a reason</span></span>

<span data-ttu-id="6f889-131">データ マートのリセットが必要であると判断した場合は、**データ マートのリセット** チェック ボックスを選択し、**理由** フィールドで理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-131">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="6f889-132"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6f889-132">The following options are available:</span></span>

- <span data-ttu-id="6f889-133">**データが不足しているか、正しくありません** – 統計に基づき、決定したデータが存在しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6f889-133">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="6f889-134">続行する前に、根本原因を判断するためにサポートを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f889-134">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="6f889-135">**データベースの復元** – データベースが復元されましたが、財務報告のデータ マートのデータベースは復元されませんでした。</span><span class="sxs-lookup"><span data-stu-id="6f889-135">**Restore database** – The database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="6f889-136">**その他** – 別の理由によりデータ マートをリセットしています。</span><span class="sxs-lookup"><span data-stu-id="6f889-136">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="6f889-137">問題があることを懸念する場合は、識別のためにサポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="6f889-137">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="6f889-138">[![データ マートのリセット](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="6f889-138">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="6f889-139">リセットを開始する前に、すべてのデータ マート リセット タスクが初回の読み込みを完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f889-139">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="6f889-140">**ツール** &gt; **統合の状態** を選択して、前回のランタイム列で値を探すことにより、これを確定できます。</span><span class="sxs-lookup"><span data-stu-id="6f889-140">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="6f889-141">ユーザーと会社をクリア</span><span class="sxs-lookup"><span data-stu-id="6f889-141">Clear users and companies</span></span>

<span data-ttu-id="6f889-142">データベースの復元後にユーザーまたは会社を変更した場合は、 **ユーザーと企業の削除** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-142">Select the **Clear users and companies** check box if you restored your database, but then changed users or companies.</span></span> <span data-ttu-id="6f889-143">このチェックボックスをオンにすることはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="6f889-143">You should rarely have to select this check box.</span></span>

<span data-ttu-id="6f889-144">リセット プロセスを開始する準備ができたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-144">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="6f889-145">プロセスを開始する準備ができていることを確認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="6f889-145">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="6f889-146">財務諸表は、リセット中およびその後に発生する最初のデータ統合中には使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6f889-146">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="6f889-147">統合の状態を確認する場合は、**ツール** &gt; **統合の状態** を選択し、統合が最後に実行された時刻と状態を表示します。</span><span class="sxs-lookup"><span data-stu-id="6f889-147">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="6f889-148">[![統合のステータスを表示](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="6f889-148">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="6f889-149">すべてのマッピングの状態が **RanToCompletion** と表示され、 **統合の状態** ダイアログボックスの左下隅に「統合が完了しました」というメッセージが表示されたら、リセットは完了です。</span><span class="sxs-lookup"><span data-stu-id="6f889-149">The reset is finished when all mappings show a status of **RanToCompletion**, and an "Integration complete" message appears in the lower-left corner of the **Integration Status** dialog box.</span></span>

## <a name="reset-the-financial-reporting-data-mart-through-windows-powershell"></a><span data-ttu-id="6f889-150">Windows PowerShell を介して Financial Reporting の データマートをリセットする</span><span class="sxs-lookup"><span data-stu-id="6f889-150">Reset the Financial reporting data mart through Windows PowerShell</span></span>

<span data-ttu-id="6f889-151">データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このセクションのステップに従って、財務報告のデータ マートが復元したデータベースを正しく使用していることを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f889-151">If you ever restore your database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored database.</span></span>

### <a name="stop-services"></a><span data-ttu-id="6f889-152">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="6f889-152">Stop services</span></span>

<span data-ttu-id="6f889-153">次の Microsoft Windows サービスでは、Finance and Operations データベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="6f889-153">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="6f889-154">したがって、Microsoft Remote Desktop を使用して環境内のすべてのコンピュータに接続し、services.msc を使用してこれらのサービスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f889-154">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="6f889-155">ワールド ワイド Web パブリッシング サービス (すべての アプリケーション オブジェクト サーバー (AOS) \[AOS\] の コンピューター)</span><span class="sxs-lookup"><span data-stu-id="6f889-155">World wide web publishing service (on all Application Object Servers \[AOS\] computers)</span></span>
- <span data-ttu-id="6f889-156">バッチ管理サービス (非プライベート AOS コンピューター上のみ)</span><span class="sxs-lookup"><span data-stu-id="6f889-156">Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="6f889-157">Management Reporter 2012 プロセス サービス (ビジネス インテリジェンス \[BI\] の コンピューター のみ)</span><span class="sxs-lookup"><span data-stu-id="6f889-157">Management Reporter 2012 Process Service (on Business intelligence \[BI\] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="6f889-158">リセット</span><span class="sxs-lookup"><span data-stu-id="6f889-158">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="6f889-159">最新の MinorVersionDataUpgrade.zip パッケージをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="6f889-159">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="6f889-160">最新の MinorVersionDataUpgrade.zip パッケージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6f889-160">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="6f889-161">データ更新パッケージの正しいバージョンを検索およびダウンロードする方法については、開発、デモ、またはサンド ボックス環境でデータを更新するトピックの [開発環境またはデモ環境でデータを更新する](../migration-upgrade/upgrade-data-to-latest-update.md#select-the-correct-data-upgrade-deployable-package) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f889-161">For instructions about how to find and download the correct version of the data upgrade package, see the section [Upgrade data in development or demo environments](../migration-upgrade/upgrade-data-to-latest-update.md#select-the-correct-data-upgrade-deployable-package) in the Upgrade data in development, demo, or sandbox environments topic.</span></span>

<span data-ttu-id="6f889-162">MinorVersionDataUpgrade.zip パッケージをダウンロードするためにアップグレードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6f889-162">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="6f889-163">そのため、当該トピックの 「最新のデータ アップグレード 展開可が能なパッケージをダウンロードする」 セクションの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f889-163">Therefore, you just have to follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="6f889-164">トピックのその他のすべての手順をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="6f889-164">You can skip all the other steps in the topic.</span></span>

#### <a name="run-prerequisite-sql-scripts-against-the-database"></a><span data-ttu-id="6f889-165">データベースに対して 前提となる SQL スクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="6f889-165">Run prerequisite SQL scripts against the database</span></span>

<span data-ttu-id="6f889-166">財務報告データベースに対してではなく、データベースに対して、次のスクリプトを実行します:</span><span class="sxs-lookup"><span data-stu-id="6f889-166">Run the following scripts against the database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="6f889-167">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="6f889-167">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="6f889-168">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="6f889-168">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="6f889-169">これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを保証する助けになります。</span><span class="sxs-lookup"><span data-stu-id="6f889-169">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-script-to-reset-the-database"></a><span data-ttu-id="6f889-170">Windows PowerShell スクリプトを実行してデータベースのリセットをする</span><span class="sxs-lookup"><span data-stu-id="6f889-170">Run a Windows PowerShell script to reset the database</span></span>

<span data-ttu-id="6f889-171">AOS コンピュータで、管理者として Microsoft Windows PowerShell を開始し、アプリケーションと財務報告との統合をリセットするために次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6f889-171">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between application and Financial reporting.</span></span>

```powershell
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>" -SkipMRTableReset
```

> [!NOTE]
> - <span data-ttu-id="6f889-172">SkipMRTableReset を使用している場合は、ツリーユニットのセキュリティが維持されます。</span><span class="sxs-lookup"><span data-stu-id="6f889-172">SkipMRTableReset preserves tree unit security if you're using it.</span></span>
> - <span data-ttu-id="6f889-173">SkipMRTableReset に一致するパラメーターが見つからないエラーが発生する場合は、パラメーターを削除して、もう一度行うことができます (以降のバージョンは、このスイッチを含めるための既定の動作更新が完了)。</span><span class="sxs-lookup"><span data-stu-id="6f889-173">If you get an error that a parameter cannot be found that matches SkipMRTableReset, you can remove the parameter and try again (later versions have updated the default behavior to include this switch).</span></span>

<span data-ttu-id="6f889-174">ここでは **Reset-DatamartIntegration** コマンドのパラメータについて説明します:</span><span class="sxs-lookup"><span data-stu-id="6f889-174">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="6f889-175">**-Reason** の有効な値は、**SERVICING**、**BADDATA**、および **OTHER** です。</span><span class="sxs-lookup"><span data-stu-id="6f889-175">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="6f889-176">**-ReasonDetail** パラメーターは自由書式です。</span><span class="sxs-lookup"><span data-stu-id="6f889-176">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="6f889-177">理由と理由の詳細はテレメトリーまたは環境モニタリングに記録されます。</span><span class="sxs-lookup"><span data-stu-id="6f889-177">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="6f889-178">コマンドを実行した後、データベースをリセットすることを確認するために **Y** を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="6f889-178">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="6f889-179">サービスをリセット</span><span class="sxs-lookup"><span data-stu-id="6f889-179">Restart services</span></span>

<span data-ttu-id="6f889-180">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="6f889-180">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="6f889-181">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="6f889-181">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="6f889-182">バッチ管理サービス (非プライベート AOS コンピューター上のみ)</span><span class="sxs-lookup"><span data-stu-id="6f889-182">Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="6f889-183">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="6f889-183">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-dynamics-365-finance--operations-on-premises-through-sql-server-management-studio"></a><span data-ttu-id="6f889-184">SQL Server Management Studio を介して、 Dynamics 365 Finance と Operations (on-premises) の Financial Reporting データマート をリセットする</span><span class="sxs-lookup"><span data-stu-id="6f889-184">Reset the Financial reporting data mart for Dynamics 365 Finance + Operations (on-premises) through SQL Server Management Studio</span></span>

<span data-ttu-id="6f889-185">作業を開始する前に、すべてのユーザーがレポート デザイナーを閉じて、財務報告エリアを終了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6f889-185">Before getting started, be sure that all users close Report designer and exit the Financial reporting area.</span></span>

1. <span data-ttu-id="6f889-186">MRDB とも呼ばれる SQL Server 内の ManagementReporter という名前の財務報告に使用されるデータベースで、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="6f889-186">On the database used for Financial reporting, which is named ManagementReporter within SQL Server, which is also referred to as MRDB, execute the following script.</span></span> <span data-ttu-id="6f889-187">2020 年 4 月 9 日更新: Reset Datamart Begin.txt</span><span class="sxs-lookup"><span data-stu-id="6f889-187">which was last updated April 9, 2020: Reset Datamart Begin.txt</span></span>

    ```sql
    ------------------------------------------------------------------------------------------
    ------------------------------------------------------------------------------------------
    --setup for servicing mode

    BEGIN TRANSACTION
    IF NOT EXISTS(SELECT SCHEMA_NAME FROM INFORMATION_SCHEMA.SCHEMATA WHERE SCHEMA_NAME = 'Servicing')
    BEGIN 
        EXEC ('CREATE SCHEMA Servicing') 
    END

    IF (DATABASE_PRINCIPAL_ID('GeneralUser') IS NULL)
    BEGIN
        CREATE ROLE [GeneralUser] AUTHORIZATION [dbo];
    END
    ALTER AUTHORIZATION ON SCHEMA::Servicing TO [GeneralUser]

    IF NOT EXISTS(SELECT NAME FROM SYS.TABLES WHERE Name = 'ServicingLock')
    BEGIN 
        CREATE TABLE [Servicing].[ServicingLock] ([Name] nvarchar(255) not null, [Value] int not null, [LastServiceTimestamp] datetime null)
    END

    IF NOT EXISTS(SELECT 1 FROM [Servicing].[ServicingLock])
    BEGIN 
        INSERT INTO [Servicing].[ServicingLock] (Name, Value) VALUES ('ServicingLockMode', 0)
    END
    COMMIT TRANSACTION


    PRINT 'Entering servicing mode'
    DECLARE @result int;
    EXEC @result = sp_getapplock @DbPrincipal='public', @Resource='ServicingLock', @LockMode='Exclusive', @LockOwner='Session', @LockTimeout=300000;
    IF @result < 0 RAISERROR ('Unable to acquire SQL applock. Result: %d', 16, 1, @result);

    BEGIN TRY
    IF EXISTS(SELECT TOP 1 1 FROM INFORMATION_SCHEMA.COLUMNS WHERE TABLE_SCHEMA = 'Scheduling' COLLATE DATABASE_DEFAULT AND TABLE_NAME = 'SchedulerRegister' COLLATE DATABASE_DEFAULT AND COLUMN_NAME = 'ServicingMode' COLLATE DATABASE_DEFAULT)
    BEGIN       
           UPDATE Scheduling.SchedulerRegister SET ServicingMode = 1 WHERE ServicingMode = 0        
           UPDATE [Servicing].[ServicingLock] SET Name = 'SchedulerServicingMode', Value = 1, LastServiceTimestamp = GETUTCDATE() WHERE Value = 0
    END
    PRINT 'Acquired servicing locks'

    --Disable maps
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)

    ------------------------------------------------------------------------------------------
    ------------------------------------------------------------------------------------------
    ------------------------------------------------------------------------------------------


    ------------------------------
    PRINT 'Save and Drop Indexes Of FactAttributeValue and DimensionValueAttributeValue'
    ------------------------------

    IF EXISTS(SELECT 1 FROM sys.procedures WHERE object_id = OBJECT_ID('[Datamart].[SaveAndDropAttributeValueIndexes]'))
    BEGIN
        IF (NOT EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND  TABLE_NAME = 'AttributeValueIndexesBackUp'))
        BEGIN
            --create table to store indexses
            -- Indexes of different table can have same index_id,but we need unique index id
            Create table [Datamart].[AttributeValueIndexesBackUp]
            (
                IndexID INT not null IDENTITY(1,1) PRIMARY KEY,
                IndexName NVARCHAR(255),
                IsUnique BIT,
                IndexType NVARCHAR(60),
                FilterDefinition NVARCHAR(max),
                KeyColumns NVARCHAR(max),
                IncludedColumns NVARCHAR(max),
                IndexRetry INT,
                IndexStatus NVARCHAR(60),
                AttributeType INT,
            )
        END

        IF (EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND  TABLE_NAME = 'FactAttributeValue')) 
        BEGIN
            --truncate table to increase index drop performance
            PRINT('TRUNCATE TABLE [Datamart].[FactAttributeValue]')
            EXEC('TRUNCATE TABLE [Datamart].[FactAttributeValue]')
            EXEC [Datamart].[SaveAndDropAttributeValueIndexes] 'FACTID','[Datamart].[FactAttributeValue]'
        END

        IF (EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND  TABLE_NAME = 'DimensionValueAttributeValue')) 
        BEGIN
            --truncate table to increase index drop performance
            PRINT('TRUNCATE TABLE [Datamart].[DimensionValueAttributeValue]')
            EXEC('TRUNCATE TABLE [Datamart].[DimensionValueAttributeValue]')
            EXEC [Datamart].[SaveAndDropAttributeValueIndexes] 'DIMENSIONVALUEID','[Datamart].[DimensionValueAttributeValue]'
        END
    End

    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @stagingTableName nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT t.TABLE_NAME as TableName
    FROM INFORMATION_SCHEMA.TABLES t WITH (NOLOCK)
    WHERE t.TABLE_SCHEMA = 'Datamart' and (t.TABLE_NAME like 'FactStaging[0-9]%' or t.TABLE_NAME like 'DimensionCombinationStaging[0-9]%')
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @stagingTableName
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP TABLE IF EXISTS [Datamart].' + @stagingTableName)
        FETCH NEXT FROM dropCursor INTO @stagingTableName
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor

    ------------------------------
    PRINT 'Dropping tables with dynamic columns'
    ------------------------------
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationProcessing
    DROP TABLE IF EXISTS [Datamart].DimensionCombination
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationResolving
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationStaging
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationUnreferenced
    DROP TABLE IF EXISTS [Datamart].DimensionValueAttributeValue
    DROP TABLE IF EXISTS [Datamart].FactAttributeValue
    DROP TABLE IF EXISTS [Datamart].TranslatedPeriodBalance
    DROP TABLE IF EXISTS [Datamart].TranslatedPeriodBalanceChanges

    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
    FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables

    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory' and @tablename <> 'AttributeValueIndexesBackUp'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
                EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
                INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
                WHERE o.[type] = 'V'
                AND referenced_schema_name = @schemaname
                AND referenced_entity_name = @tablename))
            BEGIN
                PRINT 'deleting from ' + @tablename
                EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
                PRINT 'truncating from ' + @tablename
                EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables

    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------

    -- Rebuild the tables with dynamic columns
    IF EXISTS(SELECT 1 FROM sys.procedures WHERE object_id = OBJECT_ID('[Datamart].[AddDynamicTables]'))
        BEGIN
            EXEC [Datamart].AddDynamicTables
        END
    ELSE
        BEGIN
            ---- Basically a copy of sproc AddDynamicTables
            IF NOT EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME = 'DimensionCombinationStaging' AND TABLE_SCHEMA = 'Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombinationStaging](
                    [Id] [bigint] NOT NULL,
                    [OrganizationId] [int] NULL,
                    [Description] [nvarchar](51) NULL,
                    [SourceKey] [nvarchar](100) NOT NULL,
                    [OrganizationKey] [nvarchar](100) NULL,
                    [FreshnessDate][datetime2] NULL default sysutcdatetime())

                CREATE STATISTICS [stat_dcs_org] ON [Datamart].DimensionCombinationStaging (OrganizationKey)
            END

            IF NOT EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME = 'DimensionCombinationResolving' AND TABLE_SCHEMA = 'Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombinationResolving]
                (
                    [Id] [BIGINT] NOT NULL,
                    [Description] [NVARCHAR](51) NULL,
                    [SourceKey] [NVARCHAR](100) NULL,
                    [OrganizationId] [INT] NULL
                )
            END

            IF NOT EXISTS(SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='DimensionCombination' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombination](
                    [Id] [bigint] NOT NULL,
                    [Description] [nvarchar](51) NULL,
                    [SourceKey] [nvarchar](100) NULL,
                    [OrganizationId] [int] NULL
                )
            END

            IF NOT EXISTS(SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='FactAttributeValue' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[FactAttributeValue](
                    [FactId] [bigint] NOT NULL
                )
            END

            IF NOT EXISTS(SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='DimensionValueAttributeValue' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionValueAttributeValue](
                    [DimensionValueId] [bigint] NOT NULL
                )
            END

            IF NOT EXISTS(SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='PeriodExchangeRate' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[PeriodExchangeRate]
                (
                    [PeriodId] INT NOT NULL,
                    [FromUnitOfMeasureId] INT NOT NULL,
                    [CurrencyMethod] TINYINT NOT NULL,
                    [ExchangeRateTypeId] INT NOT NULL,
                    CONSTRAINT [PK_PeriodExchangeRates] PRIMARY KEY ([FromUnitOfMeasureId], [PeriodId], [CurrencyMethod], [ExchangeRateTypeId])
                )
            END

            IF NOT EXISTS(SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='TranslatedPeriodBalance' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[TranslatedPeriodBalance](
                    [PeriodId] [INT] NOT NULL,
                    [DimensionsId] [BIGINT] NOT NULL,
                    [ScenarioId] [INT] NOT NULL,
                    [FactType] [SMALLINT] NOT NULL,
                    [PostingLayerId] [INT] NULL
                )
            END

            IF NOT EXISTS(SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='TranslatedPeriodBalanceChanges' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].TranslatedPeriodBalanceChanges(PeriodId bigint, DimensionsId bigint, ScenarioId int, PostingLayerId int null, FactType smallint,
                        constraint [IDX_BC1] unique Clustered (PeriodId, DimensionsId, ScenarioId, PostingLayerId, FactType DESC))
            END

            IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_NAME = 'DimensionCombinationArchive' AND TABLE_SCHEMA='Datamart')
            BEGIN
                IF EXISTS (SELECT TOP 1 * FROM [Datamart].[DimensionCombinationArchive])
                BEGIN
                    -- move archived combinations from the obsolete DimensionCombinationArchive table to a new table in the archive
                    -- and set its generation to 5, so it will run in 4 hours (which is how long the archived combinations were attempted originally before moving to the archive table).
                    DECLARE @archiveId INT = 0
                    INSERT INTO [Datamart].[Archive] (Generation, NextAttempt) VALUES (5, DATEADD(MINUTE, POWER(3, 5), SYSUTCDATETIME()))
                    SET @archiveId = SCOPE_IDENTITY()

                    DECLARE @comboArchiveTableName nvarchar(100) = 'DimensionCombinationStaging' + CAST(@archiveId as nvarchar(10))
                    EXEC sp_rename 'Datamart.DimensionCombinationArchive', @comboArchiveTableName

                    DECLARE @factArchiveTableName nvarchar(100) = 'FactStaging' + CAST(@archiveId as nvarchar(10))
                    EXEC ('select top 0 * into Datamart.' + @factArchiveTableName + ' from Datamart.FactStaging')
                END
                ELSE
                BEGIN
                    DROP TABLE [Datamart].[DimensionCombinationArchive]
                END
            END

            IF NOT EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE='BASE TABLE' AND TABLE_NAME = 'DimensionCombinationUnreferenced' and TABLE_SCHEMA ='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombinationUnreferenced]
                (
                    [Id] [bigint] NOT NULL,
                    [Description] [nvarchar](51) NULL,
                    [SourceKey] [nvarchar](100) NULL,
                    [OrganizationId] [int] NULL
                )

                DECLARE @columnIndex int
                DECLARE @idColumn nvarchar(128)
                DECLARE columnCursor CURSOR LOCAL FAST_FORWARD FOR SELECT DISTINCT ColumnIndex FROM [Datamart].DimensionDefinition ORDER BY ColumnIndex
                OPEN columnCursor
                FETCH NEXT FROM columnCursor INTO @columnIndex
                WHILE (@@FETCH_STATUS <> -1)
                BEGIN
                    SET @idColumn = 'Dimension' + CAST(@columnIndex as nvarchar(3)) + 'Id'
                    EXEC [Datamart].AddColumn @schemaName = 'Datamart', @tableName = 'DimensionCombinationUnreferenced', @columnName = @idColumn, @columnType = 'bigint NULL'
                    FETCH NEXT FROM columnCursor INTO @columnIndex
                END
                CLOSE columnCursor
                DEALLOCATE columnCursor


                DECLARE @dcColumnList nvarchar(max) = ''
                DECLARE @rowsCopied bigint
                DECLARE @columnName nvarchar(100)
                DECLARE columnNameCursor cursor local fast_forward for select distinct Name from sys.columns c where c.object_id = OBJECT_ID('DimensionCombination')
                OPEN columnNameCursor
                FETCH NEXT FROM columnNameCursor INTO @columnName
                WHILE (@@FETCH_STATUS <> -1)
                BEGIN
                    IF @dcColumnList <> ''
                        SET @dcColumnList = @dcColumnList + ', '

                    SET @dcColumnList = @dcColumnList + @columnName
                    FETCH NEXT FROM columnNameCursor INTO @columnName
                END
                CLOSE columnNameCursor
                DEALLOCATE columnNameCursor

                if @dcColumnList <> ''
                BEGIN
                    exec ('
                        insert into [Datamart].DimensionCombinationUnreferenced (' + @dcColumnList + ')
                        select ' + @dcColumnList + ' from [Datamart].DimensionCombination dc
                        where dc.Id not in (Select distinct DimensionsId from [Datamart].Fact)')

                    SET @rowsCopied = @@ROWCOUNT
                    IF @rowsCopied > 0
                    BEGIN
                        DECLARE @comboCount bigint
                        EXEC [Datamart].GetRowCount 'DimensionCombination', @comboCount

                        IF (@rowsCopied * 2) > @comboCount
                        BEGIN
                            -- most of the combinations in the combination table were unreferenced, so it would be faster to move the referenced out, truncate the table, then move back
                            SELECT * INTO #referencedCombos from [Datamart].DimensionCombination dc
                            WHERE dc.Id NOT IN (SELECT Id from [Datamart].DimensionCombinationUnreferenced)

                            TRUNCATE TABLE [Datamart].[DimensionCombination]

                            INSERT INTO [Datamart].[DimensionCombination]
                            SELECT * FROM #referencedCombos

                            DROP TABLE #referencedCombos
                        END
                        ELSE
                        BEGIN
                            -- we didn't find many unreferenced combinations, so delete them
                            DELETE FROM [Datamart].[DimensionCombination] WHERE Id in (SELECT Id FROM [Datamart].[DimensionCombinationUnreferenced])
                        END
                    END
                END
            END
        END



    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    
    EXEC sys.sp_releaseapplock @Resource='ServicingLock', @LockOwner='Session'
    END TRY
    BEGIN CATCH
    EXEC sys.sp_releaseapplock @Resource='ServicingLock', @LockOwner='Session'
    ;THROW;
    END CATCH
    

2. (Optional) On the MRDB, execute the following script, which was last updated February 25, 2020: ResetUsersAndCompanies.txt
> [!NOTE]
> Do not run this script unless you need to delete all users and companies. This script will remove user references from previously generated reports, and remove users from their assigned security groups. This step is not required in most cases.

```sql
-- Attempt to delete integrated users
    DECLARE @userId nvarchar(max)
    DECLARE removeUserCursor CURSOR LOCAL FAST_FORWARD FOR
    select UserID from Reporting.SecurityUser su join Reporting.SecurityUserIntegration sui on su.UserID = sui.ID
    OPEN removeUserCursor
    FETCH NEXT FROM removeUserCursor INTO @userId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        BEGIN TRY
           exec Reporting.SecurityUserDeleteRelatedEntities @userId
           delete from Reporting.SecurityGroupUser where UserID = @userId
           delete from Reporting.SecurityUser where UserID = @userId
        END TRY
        BEGIN CATCH
        -- Just skip if we cannot delete a user, integration should take care of it
        END CATCH
        FETCH NEXT FROM removeUserCursor INTO @userId
    END
    CLOSE removeUserCursor
    DEALLOCATE removeUserCursor

-- Attempt to delete integrated companies
    DECLARE @companyId nvarchar(max)
    DECLARE removeCompanyCursor CURSOR LOCAL FAST_FORWARD FOR
    select cc.ID from Reporting.ControlCompany cc join Reporting.ControlCompanyIntegration cci on cc.ID = cci.ID
    OPEN removeCompanyCursor
    FETCH NEXT FROM removeCompanyCursor INTO @companyId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        BEGIN TRY
           delete from Reporting.ControlCompany where ID = @companyId
        END TRY
        BEGIN CATCH
        -- Just skip if we cannot delete a company
        END CATCH
        FETCH NEXT FROM removeCompanyCursor INTO @companyId
    END
    CLOSE removeCompanyCursor
    DEALLOCATE removeCompanyCursor
```

3. <span data-ttu-id="6f889-188">AXDB と呼ばれる Dynamics 365 Finance のためのデータベースでは、2019 年 2 月 25 日に更新された次のスクリプトを使用して財務報告の関連テーブルをクリアします: Reset Datamart AXDB.txt</span><span class="sxs-lookup"><span data-stu-id="6f889-188">On the database for Dynamics 365 Finance, which is referred to as AXDB, clear the financial reporting related tables with the following script, which was last updated February 25, 2019: Reset Datamart AXDB.txt</span></span>

```sql
IF EXISTS (SELECT 1 FROM [INFORMATION_SCHEMA].[TABLES] WHERE [TABLE_SCHEMA] = 'dbo' and [TABLE_NAME] = 'FINANCIALREPORTS') 
BEGIN 
    TRUNCATE TABLE [dbo].[FINANCIALREPORTS] 
END 
IF EXISTS (SELECT 1 FROM [INFORMATION_SCHEMA].[TABLES] WHERE [TABLE_SCHEMA] = 'dbo' and [TABLE_NAME] = 'FINANCIALREPORTVERSION') 
BEGIN 
    TRUNCATE TABLE [dbo].[FINANCIALREPORTVERSION] 
END  
```


4. <span data-ttu-id="6f889-189">MRDB では、次の最後に更新されたスクリプトを使用して統合とエンド サービス モードを再び有効にし、2019 年 2 月 25 日に更新された次のスクリプトを使用して財務報告の関連テーブルをクリアします: Reset Datamart END.txt</span><span class="sxs-lookup"><span data-stu-id="6f889-189">On the MRDB, re-enable the integration and end servicing mode with the script below, which was last updated clear the financial reporting related tables with the script below, which was last updated February 25, 2019: Reset Datamart END.txt</span></span>



```sql
DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
FROM [Scheduling].[Task] t with(nolock)
JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
------------------------------------------
------------------------------------------
PRINT 'Reset the map tokens'
UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
FROM [Scheduling].[Task] t with(nolock)
JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
PRINT 'Reset the tasks'
UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
FROM [Scheduling].[Task] t with(nolock)
JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
PRINT 'Enable integration tasks, RunImmediately'
UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
PRINT 'Enable the Maintenance Task'
UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
(SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
------------------------------------------
------------------------------------------

UPDATE [Servicing].[ServicingLock] SET [Value] = 0 WHERE [Value] = 1
IF EXISTS(SELECT TOP 1 1 FROM INFORMATION_SCHEMA.COLUMNS WHERE TABLE_SCHEMA = 'Scheduling' COLLATE DATABASE_DEFAULT AND TABLE_NAME = 'SchedulerRegister' COLLATE DATABASE_DEFAULT AND COLUMN_NAME = 'ServicingMode' COLLATE DATABASE_DEFAULT)
BEGIN
       UPDATE Scheduling.SchedulerRegister SET ServicingMode = 0
END
```


5. <span data-ttu-id="6f889-190">リセット後は、手動で財務諸表データベースに対して次のクエリを実行し、データの再読み込みを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="6f889-190">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```sql
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

<span data-ttu-id="6f889-191">すべての行の **LastRunTime** 値、およびその **StateType** が **5** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6f889-191">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="6f889-192">**5** の **StateType** 値はデータが正常に再読み込みされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="6f889-192">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="6f889-193">**7** の値はエラー状態を示します。</span><span class="sxs-lookup"><span data-stu-id="6f889-193">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="6f889-194">組織階層マップは、初めて実行される時にこの状態になることがあります。</span><span class="sxs-lookup"><span data-stu-id="6f889-194">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="6f889-195">ただし、エラー状態は自動的に解決されます。</span><span class="sxs-lookup"><span data-stu-id="6f889-195">However, the default state but should be automatically resolved.</span></span>

## <a name="export-and-import-report-definitions"></a><span data-ttu-id="6f889-196">レポートの定義を エクスポート/インポートする</span><span class="sxs-lookup"><span data-stu-id="6f889-196">Export and import report definitions</span></span>

<span data-ttu-id="6f889-197">データ マートのリセットは、どのレポート定義にも影響しませんが、データ移動のアクティビティによってはレポート定義が失われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6f889-197">Although a reset of the data mart doesn't affect any report definitions, some data movement activities can cause report definitions to be lost.</span></span> <span data-ttu-id="6f889-198">ユーザー受け入れテスト(UAT)テスト環境で新しいレポートを作成する場合は、UAT環境を本番環境のコピーで上書きするなどして、データ移動アクティビティを実行の際には十分に注意してください。</span><span class="sxs-lookup"><span data-stu-id="6f889-198">Be very careful when you perform a data movement activity such as overwriting a user acceptance testing (UAT) test environment with a copy of the production environment if new reports were being created in the UAT environment.</span></span> <span data-ttu-id="6f889-199">レポート定義をエクスポートすると、定義を復元する必要が生じた場合に、バックアップを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6f889-199">Exporting report definitions can provide a backup in the event that it becomes necessary to restore your definitions.</span></span> 

### <a name="export-report-definitions"></a><span data-ttu-id="6f889-200">レポート定義のエクスポート</span><span class="sxs-lookup"><span data-stu-id="6f889-200">Export report definitions</span></span>

<span data-ttu-id="6f889-201">最初に、以下の手順を実行しレポート デザイナーからレポート デザインをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="6f889-201">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="6f889-202">レポート デザイナーで、**会社** &gt; **レポート パーツ グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-202">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="6f889-203">エクスポートする構成要素グループを選択し、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-203">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f889-204">Finance and Operations に関しては、1 つの構成要素グループのみがサポートされています: **既定**。</span><span class="sxs-lookup"><span data-stu-id="6f889-204">For Finance and Operations, only one building block group is supported: **Default**.</span></span>

3. <span data-ttu-id="6f889-205">エクスポートするレポート定義を選択します:</span><span class="sxs-lookup"><span data-stu-id="6f889-205">Select the report definitions to export:</span></span>

    - <span data-ttu-id="6f889-206">レポート定義および関連するレポート パーツのすべてをエクスポートするには、**すべて選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-206">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="6f889-207">特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブを選択してエクスポートする項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-207">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="6f889-208">タブにて複数のレコードを選択するには、キーボードの **Ctrl キー** を押しながら選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-208">To select multiple items on a tab, press and hold the **Ctrl** key while you make your selections.</span></span> <span data-ttu-id="6f889-209">エクスポートをするレポートを選択すると、関連する行、列、ツリー、各要素のセットが選択されます。</span><span class="sxs-lookup"><span data-stu-id="6f889-209">When you select reports to export, the associated rows, columns, trees, and dimension sets are also selected.</span></span>

4. <span data-ttu-id="6f889-210">**エクスポート** の選択</span><span class="sxs-lookup"><span data-stu-id="6f889-210">Select **Export**.</span></span>
5. <span data-ttu-id="6f889-211">ファイル名を入力し、エクスポートしたレポート定義を保存する保護された安全な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-211">Enter a file name, and select a secure location to save the exported report definitions in.</span></span>
6. <span data-ttu-id="6f889-212">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-212">Select **Save**.</span></span>

<span data-ttu-id="6f889-213">ファイルを安全な場所にコピーまたはアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="6f889-213">You can copy or upload the file to a secure location.</span></span>

> [!WARNING]
> <span data-ttu-id="6f889-214">Microsoft Azure Virtual Machines (VMs) の Dドライブ の挙動には気をつけてください。</span><span class="sxs-lookup"><span data-stu-id="6f889-214">Be aware of the behavior of drive D on Microsoft Azure virtual machines (VMs).</span></span> <span data-ttu-id="6f889-215">Dドライブに、エクスポートしたレポート パーツ グループを完全には保存しません。一時的なドライブの詳細については、次を参照してください。[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="6f889-215">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="import-report-definitions"></a><span data-ttu-id="6f889-216">レポート定義のインポート</span><span class="sxs-lookup"><span data-stu-id="6f889-216">Import report definitions</span></span>

<span data-ttu-id="6f889-217">次に、エクスポートの課程で作成されたファイルを使用して、レポート デザイナー から レポートのデザイン を インポートします。</span><span class="sxs-lookup"><span data-stu-id="6f889-217">Next, import your report designs from Report designer by using the file that was created during export.</span></span>

1. <span data-ttu-id="6f889-218">レポート デザイナーで、**会社** &gt; **レポート パーツ グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-218">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="6f889-219">**既定** の構成要素を選択し、**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f889-219">Select the **Default** building block, and then select **Import**.</span></span>
3. <span data-ttu-id="6f889-220">エクスポート済みのレポート定義を含むファイルを選択し、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f889-220">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
4. <span data-ttu-id="6f889-221">**インポート** ダイアログ ボックスで、インポートするレポート定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-221">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="6f889-222">レポート定義および関連するレポート パーツのすべてをインポートするには、**すべて選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-222">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="6f889-223">特定のレポートをインポートするには、行、列、ツリー、あるいは必要な要素を選択してください。</span><span class="sxs-lookup"><span data-stu-id="6f889-223">To import specific reports, rows, columns, trees, or dimension sets, select them.</span></span>

5. <span data-ttu-id="6f889-224">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f889-224">Select **Import**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]