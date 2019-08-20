---
title: 財務報告のデータ マートのリセット
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の財務報告データ マートをリセットする方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 02/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: IT Pro, Developer
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1e8399fe381587fd28936e18c335c81ecbfa836f
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849935"
---
# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="5f7f7-103">財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="5f7f7-103">Reset the Financial reporting data mart</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f7f7-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations の次のバージョンの財務報告データ マートをリセットする方法について説明します:</span><span class="sxs-lookup"><span data-stu-id="5f7f7-104">This topic explains how to reset the Financial reporting data mart for the following versions of Microsoft Dynamics 365 for Finance and Operations:</span></span>

- <span data-ttu-id="5f7f7-105">財務報告 7.2.6.0 以降のリリース</span><span class="sxs-lookup"><span data-stu-id="5f7f7-105">Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="5f7f7-106">財務報告 7.0.10000.4 以降のリリース</span><span class="sxs-lookup"><span data-stu-id="5f7f7-106">Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="5f7f7-107">Microsoft Dynamics 365 for Finance and Operations (設置型)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-107">Microsoft Dynamics 365 for Finance and Operations (on-premises)</span></span>

<span data-ttu-id="5f7f7-108">Finance and Operations の財務報告リリース 7.2.6.0 を取得するには、<https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514> から KB 4052514 をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="5f7f7-109">Finance and Operations 財務諸表 7.2.6.0 以降のリリースの財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="5f7f7-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="5f7f7-110">レポート デザイナーからの財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="5f7f7-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="5f7f7-111">このプロセスのステップは、Finance and Operations 財務諸表 7.2.6.0 以降のリリースでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="5f7f7-112">以前のリリースを持っている場合は、サポート チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="5f7f7-113">レポート デザイナーのバージョンを検索するには、次のビデオをご覧ください。:[レポート デザイナーのバージョンを検索する方法](https://www.youtube.com/watch?v=icfA5Q3kp4w)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-113">To find the version of report designer, watch this video: [How to find the version of Report designer](https://www.youtube.com/watch?v=icfA5Q3kp4w)</span></span>

<span data-ttu-id="5f7f7-114">特定のシナリオでは、場合によっては財務諸表のデータ マートをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-114">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="5f7f7-115">レポート デザイナーのクライアントでこのタスクを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-115">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="5f7f7-116">データ マートをリセットする必要があるかもしれない、いくつかのシナリオを次に示します:</span><span class="sxs-lookup"><span data-stu-id="5f7f7-116">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="5f7f7-117">Finance and Operations データベースが復元されましたが、データ マート データベースは復元されませんでした。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-117">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="5f7f7-118">期間の誤ったデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-118">You see incorrect data for a period.</span></span>
- <span data-ttu-id="5f7f7-119">トラブルシューティング手順の一部として、サポートはデータ マートをリセットするように指示します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-119">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="5f7f7-120">データ マートのリセットは、データベースの処理の量が小さい時間帯にのみ実行してください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-120">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="5f7f7-121">財務諸表は、リセット プロセス中は使用できません。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-121">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="5f7f7-122">データ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="5f7f7-122">Reset the data mart</span></span>

<span data-ttu-id="5f7f7-123">データ マートをリセットするには、レポート デザイナーの、**ツール** メニューにある、**データ マートのリセット** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-123">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="5f7f7-124">表示されるダイアログ ボックスには2つのセクションがあります: **統計** および **リセット**。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-124">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="5f7f7-125">[![データ マートのダイアログ ボックスをリセットします](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-125">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="5f7f7-126">統合試行回数</span><span class="sxs-lookup"><span data-stu-id="5f7f7-126">Integration attempts</span></span>

<span data-ttu-id="5f7f7-127">**統合試行回数** グリッドは、システムがトランザクションの統合を試みた回数を表示します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-127">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="5f7f7-128">システムは、最初のいくつかの試行ができなかった場合は、日の期間にわたってデータを統合するまで続行されます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-128">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="5f7f7-129">試行回数が8回以上の場合、および分析コードの組み合わせやトランザクション レコードが多い場合、データ マートをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-129">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="5f7f7-130">このような状況では、データはレポートされません。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-130">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="5f7f7-131">データのステータス</span><span class="sxs-lookup"><span data-stu-id="5f7f7-131">Data status</span></span>

<span data-ttu-id="5f7f7-132">**データのステータス** グリッドは、データ マート内のトランザクション、為替レート、および分析コード値のスナップショットを表示します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-132">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="5f7f7-133">古いレコードが多数ある場合、レコードに対して更新が数多く存在することになります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-133">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="5f7f7-134">このような場合、レポート生成に時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-134">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="5f7f7-135">正しく整合されていない主勘定カテゴリ</span><span class="sxs-lookup"><span data-stu-id="5f7f7-135">Misaligned main account categories</span></span>

<span data-ttu-id="5f7f7-136">Microsoft Dynamics 365 for Finance and Operations 財務諸表 7.2.1 以前のリリースを使用している場合で、勘定の名前を変更して勘定カテゴリの間で勘定を移動する場合、データ マートをリセットする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-136">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="5f7f7-137">これらのアクションにより、主勘定カテゴリが正しく整合されなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-137">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="5f7f7-138">**正しく整合されていない主勘定カテゴリ** フィールドには問題が発生しているかどうかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-138">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="5f7f7-139">Finance and Operations 財務諸表 7.2.6.0 のリリースで、データ マートをリセットします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-139">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="5f7f7-140">Finance and Operations 財務諸表 7.2.6.0 以前のリリースでデータ マートをリセットするには、**データ マートのリセット** ダイアログ ボックスで、**データ マートのリセット** のチェックボックスを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-140">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="5f7f7-141">データ マートのリセットは、スケジュール済ダウンタイム中にのみ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-141">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="5f7f7-142">[![Rデータ マートのチェックボックスをリセットします](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-142">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="5f7f7-143">Microsoft Dynamics 365 for Finance and Operations Finance and Operations 財務諸表 7.3.0 のリリースで、データ マートをリセットし、理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-143">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="5f7f7-144">データ マートのリセットが必要であると判断した場合は、**データ マートのリセット** チェック ボックスを選択し、**理由** フィールドで理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-144">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="5f7f7-145"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-145">The following options are available:</span></span>

- <span data-ttu-id="5f7f7-146">**データが不足しているか、正しくありません** – 統計に基づき、決定したデータが存在しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-146">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="5f7f7-147">続行する前に、根本原因を判断するためにサポートを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-147">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="5f7f7-148">**データベースの復元** – Finance and Operations データベースが復元されましたが、財務諸表のデータ マートのデータベースは復元されませんでした。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-148">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="5f7f7-149">**その他** – 別の理由によりデータ マートをリセットしています。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-149">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="5f7f7-150">問題があることを懸念する場合は、識別のためにサポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-150">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="5f7f7-151">[![データ マートのリセット](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-151">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5f7f7-152">リセットを開始する前に、すべてのデータ マート リセット タスクが初回の読み込みを完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-152">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="5f7f7-153">**ツール** &gt; **統合の状態** を選択して、前回のランタイム列で値を探すことにより、これを確定できます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-153">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="5f7f7-154">ユーザーと会社をクリア</span><span class="sxs-lookup"><span data-stu-id="5f7f7-154">Clear users and companies</span></span>

<span data-ttu-id="5f7f7-155">データベースを復元しましたが、ユーザーまたは会社に変更を加えた場合は **ユーザーと会社をクリア** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-155">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="5f7f7-156">このチェックボックスをオンにすることはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-156">You should rarely have to select this check box.</span></span>

<span data-ttu-id="5f7f7-157">リセット プロセスを開始する準備ができたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-157">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="5f7f7-158">プロセスを開始する準備ができていることを確認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-158">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="5f7f7-159">財務諸表は、リセット中およびその後に発生する最初のデータ統合中には使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-159">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="5f7f7-160">統合の状態を確認する場合は、**ツール** &gt; **統合の状態** を選択し、統合が最後に実行された時刻と状態を表示します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-160">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="5f7f7-161">[![統合のステータスを表示](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-161">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="5f7f7-162">すべてのマッピングが RanToCompletion の状態を表示し、および統合の状態ウィンドウが左下隅で「統合が完了しました」と表示する場合、リセットが完了します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-162">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says "Integration complete" in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="5f7f7-163">Finance and Operations 財務諸表 7.0.10000.4 以降のリリースの財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="5f7f7-163">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="5f7f7-164">Finance and Operations データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このセクションのステップに従って、財務諸表のデータ マートが復元したFinance and Operations データベースを正しく使用していることを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-164">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="5f7f7-165">このプロセスの手順は、Microsoft Dynamics AX application version 7.0.1 (2016 年 5 月) (アプリケーション ビルド 7.0.1265.23014 および財務諸表ビルド 7.0.10000.4) およびそれ以降のリリースでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-165">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="5f7f7-166">Finance and Operations の以前のバージョンを持っている場合は、サポート チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-166">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="5f7f7-167">レポート定義のエクスポート</span><span class="sxs-lookup"><span data-stu-id="5f7f7-167">Export report definitions</span></span>

<span data-ttu-id="5f7f7-168">最初に、以下の手順を実行しレポート デザイナーからレポート デザインをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-168">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="5f7f7-169">レポート デザイナーで、**会社** &gt; **レポート パーツ グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-169">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="5f7f7-170">エクスポートする構成要素グループを選択し、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-170">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f7f7-171">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-171">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="5f7f7-172">エクスポートするレポート定義を選択します:</span><span class="sxs-lookup"><span data-stu-id="5f7f7-172">Select the report definitions to export:</span></span>

    - <span data-ttu-id="5f7f7-173">レポート定義および関連するレポート パーツのすべてをエクスポートするには、**すべて選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-173">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="5f7f7-174">特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブを選択してエクスポートする項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-174">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="5f7f7-175">タブ上の複数の項目を選択するには、Ctrl キーを押しながら選択します。エクスポートするレポートを選択したとき、関連する行、列、ツリー、分析コードセットが選択されます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-175">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="5f7f7-176">**エクスポート** の選択</span><span class="sxs-lookup"><span data-stu-id="5f7f7-176">Select **Export**.</span></span>
5. <span data-ttu-id="5f7f7-177">ファイル名を入力し、エクスポートされたレポート定義を保存できる安全な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-177">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="5f7f7-178">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-178">Select **Save**.</span></span>

<span data-ttu-id="5f7f7-179">ファイルを安全な場所にコピーまたはアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-179">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="5f7f7-180">これにより、ファイルは後に異なった環境にもインポートできます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-180">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="5f7f7-181">Microsoft Azure ストレージ アカウントの使用方法に関する情報は、「[AzCopy Command-Line Utility でデータを転送する](/azure/storage/storage-use-azcopy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-181">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="5f7f7-182">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-182">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="5f7f7-183">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-183">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="5f7f7-184">Azure 仮想マシン (VM) 上の D ドライブの動作に注意してください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-184">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="5f7f7-185">Dドライブに、エクスポートしたレポート パーツ グループを完全には保存しません。一時的なドライブの詳細については、次を参照してください。[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="5f7f7-185">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="5f7f7-186">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="5f7f7-186">Stop services</span></span>

<span data-ttu-id="5f7f7-187">次の Microsoft Windows サービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-187">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="5f7f7-188">したがって、Microsoft Remote Desktop を使用して環境内のすべてのコンピュータに接続し、services.msc を使用してこれらのサービスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-188">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="5f7f7-189">ワールド ワイド ウェブ公開サービス (すべての Application Object Server [AOS] コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-189">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="5f7f7-190">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-190">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="5f7f7-191">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス [BI] コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-191">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="5f7f7-192">リセット</span><span class="sxs-lookup"><span data-stu-id="5f7f7-192">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="5f7f7-193">最新の MinorVersionDataUpgrade.zip パッケージをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="5f7f7-193">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="5f7f7-194">最新の MinorVersionDataUpgrade.zip パッケージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-194">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="5f7f7-195">データ アップグレード パッケージの正しいバージョンを検索およびダウンロードする方法については、開発、デモ、またはサンド ボックス環境でデータのアップグレード トピックのセクション [適切なデータ アップグレード配置可能パッケージを選択](../migration-upgrade/upgrade-data-to-latest-update.md#select-the-correct-data-upgrade-deployable-package) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-195">For instructions about how to find and download the correct version of the data upgrade package, see the section [Select the correct data upgrade deployable package](../migration-upgrade/upgrade-data-to-latest-update.md#select-the-correct-data-upgrade-deployable-package) in the Upgrade data in development, demo, or sandbox environments topic.</span></span>

<span data-ttu-id="5f7f7-196">MinorVersionDataUpgrade.zip パッケージをダウンロードするためにアップグレードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-196">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="5f7f7-197">したがって、そのトピックにある「最新のデータ アップグレード配置可能パッケージをダウンロードする」セクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-197">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="5f7f7-198">トピックのその他のすべての手順をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-198">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="5f7f7-199">Finance and Operations データベースに対してスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="5f7f7-199">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="5f7f7-200">財務諸表 データベースに対してではなく、Finance and Operations データベースに対して、次のスクリプトを実行します:</span><span class="sxs-lookup"><span data-stu-id="5f7f7-200">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="5f7f7-201">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="5f7f7-201">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="5f7f7-202">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="5f7f7-202">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="5f7f7-203">これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを保証する助けになります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-203">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="5f7f7-204">データベースをリセットするのには Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-204">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="5f7f7-205">AOS コンピュータで、管理者として Microsoft Windows PowerShell を開始し、Finance and Operations と財務諸表との統合をリセットするために次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-205">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>" -SkipMRTableReset
```

> [!NOTE]
> - <span data-ttu-id="5f7f7-206">SkipMRTableReset を使用している場合、ツリー ユニット セキュリティを維持します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-206">SkipMRTableReset preserves tree unit security if you are using it.</span></span>
> - <span data-ttu-id="5f7f7-207">SkipMRTableReset に一致するパラメーターが見つからないエラーが発生する場合は、パラメーターを削除して、もう一度行うことができます (以降のバージョンは、このスイッチを含めるための既定の動作更新が完了)。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-207">If you get an error that a parameter cannot be found that matches SkipMRTableReset, you can remove the parameter and try again (later versions have updated the default behavior to include this switch).</span></span>

<span data-ttu-id="5f7f7-208">ここでは **Reset-DatamartIntegration** コマンドのパラメータについて説明します:</span><span class="sxs-lookup"><span data-stu-id="5f7f7-208">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="5f7f7-209">**-Reason** の有効な値は、**SERVICING**、**BADDATA**、および **OTHER** です。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-209">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="5f7f7-210">**-ReasonDetail** パラメーターは自由書式です。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-210">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="5f7f7-211">理由と理由の詳細はテレメトリーまたは環境モニタリングに記録されます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-211">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="5f7f7-212">コマンドを実行した後、データベースをリセットすることを確認するために **Y** を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-212">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="5f7f7-213">サービスをリセット</span><span class="sxs-lookup"><span data-stu-id="5f7f7-213">Restart services</span></span>

<span data-ttu-id="5f7f7-214">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-214">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="5f7f7-215">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-215">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="5f7f7-216">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-216">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="5f7f7-217">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="5f7f7-217">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="5f7f7-218">レポート定義のインポート</span><span class="sxs-lookup"><span data-stu-id="5f7f7-218">Import report definitions</span></span>

<span data-ttu-id="5f7f7-219">エクスポート中に作成されたファイルを使用して、レポート デザイナーからレポート デザインをインポートします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-219">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="5f7f7-220">レポート デザイナーで、**会社** &gt; **レポート パーツ グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-220">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="5f7f7-221">エクスポートする構成要素グループを選択し、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-221">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f7f7-222">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-222">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="5f7f7-223">**既定** の構成要素を選択し、**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-223">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="5f7f7-224">エクスポート済みのレポート定義を含むファイルを選択し、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-224">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="5f7f7-225">**インポート** ダイアログ ボックスで、インポートするレポート定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-225">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="5f7f7-226">レポート定義および関連するレポート パーツのすべてをインポートするには、**すべて選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-226">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="5f7f7-227">特定のレポート、行、列、ツリー、または分析コードセットをインポートするには、インポートするレポート、行、列、ツリー、または分析コードセットを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-227">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="5f7f7-228">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-228">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="5f7f7-229">Finance and Operations (オンプレミス) の財務諸表 データ マートをリセットします</span><span class="sxs-lookup"><span data-stu-id="5f7f7-229">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="5f7f7-230">レポート デザイナーおよび Finance and Operations の財務諸表エリアを終了するようすべてのユーザーに指示します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-230">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="5f7f7-231">財務諸表データベース (MRDB) に対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-231">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
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
    ```

3. <span data-ttu-id="5f7f7-232">Finance and Operations データベース (AXDB) にある FINANCIALREPORTS テーブルのすべてのレコードを切り捨て、または削除します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-232">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="5f7f7-233">FINANCIALREPORTVERSION テーブルが Finance and Operations データベースに存在する場合、このテーブルのすべてのレコードを切り捨て、または削除します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-233">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="5f7f7-234">テーブルが Finance and Operations データベースに存在しない場合、このステップを省略します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-234">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="5f7f7-235">財務諸表データベースに対して、**ResetDatamart.sql** を実行します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-235">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="5f7f7-236">このスクリプトはデータ マートの統合を無効にし、すべてのデータ マートを削除し、その後データ マートの統合を再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-236">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
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
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
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
        IF @tablename <> 'VersionHistory'
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
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
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
    ```

6. <span data-ttu-id="5f7f7-237">リセット後は、手動で財務諸表データベースに対して次のクエリを実行し、データの再読み込みを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-237">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="5f7f7-238">すべての行の **LastRunTime** 値、およびその **StateType** が **5** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-238">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="5f7f7-239">**5** の **StateType** 値はデータが正常に再読み込みされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-239">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="5f7f7-240">**7** の値はエラー状態を示します。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-240">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="5f7f7-241">組織階層マップは、初めて実行される時にこの状態になることがあります。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-241">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="5f7f7-242">ただし、エラー状態は自動的に解決されます。</span><span class="sxs-lookup"><span data-stu-id="5f7f7-242">However, the faulted state but should be automatically resolved.</span></span>
