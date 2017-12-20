---
title: "財務報告のデータ マートのリセット"
description: "財務報告データ マートをリセットする方法について説明します。"
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: ja-jp
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="909e9-103">財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="909e9-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="909e9-104">このトピックでは、次のバージョンの財務報告データ マートをリセットする方法について説明します:</span><span class="sxs-lookup"><span data-stu-id="909e9-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="909e9-105">Microsoft Dynamics 365 for Finance and Operations 財務諸表 7.2.6.0 以降のリリース</span><span class="sxs-lookup"><span data-stu-id="909e9-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="909e9-106">Microsoft Dynamics 365 for Finance and Operations 財務諸表 7.0.10000.4 以降のリリース</span><span class="sxs-lookup"><span data-stu-id="909e9-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="909e9-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (オンプレミス)</span><span class="sxs-lookup"><span data-stu-id="909e9-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="909e9-108">Finance and Operations 財務諸表 7.2.6.0 のリリースを取得するには、<https://support.microsoft.com/en-us/help/4052514> から KB 4052514 をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="909e9-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="909e9-109">Finance and Operations 財務諸表 7.2.6.0 以降のリリースの財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="909e9-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="909e9-110">レポート デザイナーからの財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="909e9-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="909e9-111">このプロセスのステップは、Finance and Operations 財務諸表 7.2.6.0 以降のリリースでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="909e9-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="909e9-112">以前のリリースを持っている場合は、サポート チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="909e9-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="909e9-113">特定のシナリオでは、場合によっては財務諸表のデータ マートをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="909e9-114">レポート デザイナーのクライアントでこのタスクを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="909e9-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="909e9-115">データ マートをリセットする必要があるかもしれない、いくつかのシナリオを次に示します:</span><span class="sxs-lookup"><span data-stu-id="909e9-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="909e9-116">Finance and Operations データベースが復元されましたが、データ マート データベースは復元されませんでした。</span><span class="sxs-lookup"><span data-stu-id="909e9-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="909e9-117">期間の誤ったデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="909e9-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="909e9-118">トラブルシューティング手順の一部として、サポートはデータ マートをリセットするように指示します。</span><span class="sxs-lookup"><span data-stu-id="909e9-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="909e9-119">データ マートのリセットは、データベースの処理の量が小さい時間帯にのみ実行してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="909e9-120">財務諸表は、リセット プロセス中は使用できません。</span><span class="sxs-lookup"><span data-stu-id="909e9-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="909e9-121">データ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="909e9-121">Reset the data mart</span></span>

<span data-ttu-id="909e9-122">データ マートをリセットするには、レポート デザイナーの、[**ツール**] メニューにある、[**データ マートのリセット**] を選択してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="909e9-123">表示されるダイアログ ボックスには2つのセクションがあります: [**統計**] および [**リセット**]。</span><span class="sxs-lookup"><span data-stu-id="909e9-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="909e9-124">[![データ マートのダイアログ ボックスをリセットします](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="909e9-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="909e9-125">統合試行回数</span><span class="sxs-lookup"><span data-stu-id="909e9-125">Integration attempts</span></span>

<span data-ttu-id="909e9-126">[**統合試行回数**] グリッドは、システムがトランザクションの統合を試みた回数を表示します。</span><span class="sxs-lookup"><span data-stu-id="909e9-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="909e9-127">システムは、最初のいくつかの試行ができなかった場合は、日の期間にわたってデータを統合するまで続行されます。</span><span class="sxs-lookup"><span data-stu-id="909e9-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="909e9-128">試行回数が8回以上の場合、および分析コードの組み合わせやトランザクション レコードが多い場合、データ マートをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="909e9-129">このような状況では、データはレポートされません。</span><span class="sxs-lookup"><span data-stu-id="909e9-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="909e9-130">データのステータス</span><span class="sxs-lookup"><span data-stu-id="909e9-130">Data status</span></span>

<span data-ttu-id="909e9-131">[**データのステータス**] グリッドは、データ マート内のトランザクション、為替レート、および分析コード値のスナップショットを表示します。</span><span class="sxs-lookup"><span data-stu-id="909e9-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="909e9-132">古いレコードが多数ある場合、レコードに対して更新が数多く存在することになります。</span><span class="sxs-lookup"><span data-stu-id="909e9-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="909e9-133">このような場合、レポート生成に時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="909e9-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="909e9-134">正しく整合されていない主勘定カテゴリ</span><span class="sxs-lookup"><span data-stu-id="909e9-134">Misaligned main account categories</span></span>

<span data-ttu-id="909e9-135">Microsoft Dynamics 365 for Finance and Operations 財務諸表 7.2.1 以前のリリースを使用している場合で、勘定の名前を変更して勘定カテゴリの間で勘定を移動する場合、データ マートをリセットする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="909e9-136">これらのアクションにより、主勘定カテゴリが正しく整合されなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="909e9-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="909e9-137">[**正しく整合されていない主勘定カテゴリ**] フィールドには問題が発生しているかどうかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="909e9-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="909e9-138">Finance and Operations 財務諸表 7.2.6.0 のリリースで、データ マートをリセットします。</span><span class="sxs-lookup"><span data-stu-id="909e9-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="909e9-139">Finance and Operations 財務諸表 7.2.6.0 以前のリリースでデータ マートをリセットするには、[**データ マートのリセット**] ダイアログ ボックスで、[**データ マートのリセット**] のチェックボックスを選択し、[**OK**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="909e9-140">データ マートのリセットは、スケジュール済ダウンタイム中にのみ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="909e9-141">[![Rデータ マートのチェックボックスをリセットします](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="909e9-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="909e9-142">Microsoft Dynamics 365 for Finance and Operations Financial reporting 7.3.0 のリリースで、データ マートをリセットし、理由を選択してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="909e9-143">データ マートのリセットが必要であると判断した場合は、[**データ マートのリセット**] チェック ボックスを選択し、[**理由**] フィールドで理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="909e9-144"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="909e9-144">The following options are available:</span></span>

- <span data-ttu-id="909e9-145">**データが不足しているか、正しくありません** – 統計に基づき、決定したデータが存在しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="909e9-146">続行する前に、根本原因を判断するためにサポートを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="909e9-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="909e9-147">**データベースの復元** – Finance and Operations データベースが復元されましたが、財務諸表のデータ マートのデータベースは復元されませんでした。</span><span class="sxs-lookup"><span data-stu-id="909e9-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="909e9-148">**その他** – 別の理由によりデータ マートをリセットしています。</span><span class="sxs-lookup"><span data-stu-id="909e9-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="909e9-149">問題があることを懸念する場合は、識別のためにサポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="909e9-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="909e9-150">ステップを完了する前に、すべての既存のタスクの統合が終了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="909e9-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="909e9-151">**ツール** &gt; **統合の状態**を選択することで統合のステータスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="909e9-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="909e9-152">ユーザーと会社をクリア</span><span class="sxs-lookup"><span data-stu-id="909e9-152">Clear users and companies</span></span>

<span data-ttu-id="909e9-153">データベースを復元しましたが、ユーザーまたは会社に変更を加えた場合は [**ユーザーと会社をクリア**] チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="909e9-154">このチェックボックスをオンにすることはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="909e9-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="909e9-155">リセット プロセスを開始する準備ができたら、[**OK**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="909e9-156">プロセスを開始する準備ができていることを確認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="909e9-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="909e9-157">財務諸表は、リセット中およびその後に発生する最初のデータ統合中には使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="909e9-158">統合の状態を確認する場合は、**ツール** &gt; **統合の状態** を選択し、統合が最後に実行された時刻と状態を表示します。</span><span class="sxs-lookup"><span data-stu-id="909e9-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="909e9-159">[![統合のステータスを表示](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="909e9-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="909e9-160">Finance and Operations 財務諸表 7.0.10000.4 以降のリリースの財務報告のデータ マートのリセット</span><span class="sxs-lookup"><span data-stu-id="909e9-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="909e9-161">Finance and Operations データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このセクションのステップに従って、財務諸表のデータ マートが復元したFinance and Operations データベースを正しく使用していることを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="909e9-162">このプロセスの手順は、Microsoft Dynamics AX application version 7.0.1 (2016 年 5 月) (アプリケーション ビルド 7.0.1265.23014 および財務諸表ビルド 7.0.10000.4) およびそれ以降のリリースでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="909e9-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="909e9-163">Finance and Operations の以前のバージョンを持っている場合は、サポート チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="909e9-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="909e9-164">レポート定義のエクスポート</span><span class="sxs-lookup"><span data-stu-id="909e9-164">Export report definitions</span></span>

<span data-ttu-id="909e9-165">最初に、以下の手順を実行しレポート デザイナーからレポート デザインをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="909e9-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="909e9-166">レポート デザイナーで、[**会社**] &gt; [**レポート パーツ グループ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="909e9-167">エクスポートする構成要素グループを選択し、[**エクスポート**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="909e9-168">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="909e9-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="909e9-169">エクスポートするレポート定義を選択します:</span><span class="sxs-lookup"><span data-stu-id="909e9-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="909e9-170">レポート定義および関連するレポート パーツのすべてをエクスポートするには、[**すべて選択**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="909e9-171">特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブを選択してエクスポートする項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="909e9-172">タブ上の複数の項目を選択するには、Ctrl キーを押しながら選択します。エクスポートするレポートを選択したとき、関連する行、列、ツリー、分析コードセットが選択されます。</span><span class="sxs-lookup"><span data-stu-id="909e9-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="909e9-173">[**エクスポート**] の選択</span><span class="sxs-lookup"><span data-stu-id="909e9-173">Select **Export**.</span></span>
5. <span data-ttu-id="909e9-174">ファイル名を入力し、エクスポートされたレポート定義を保存できる安全な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="909e9-175">[**保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-175">Select **Save**.</span></span>

<span data-ttu-id="909e9-176">ファイルを安全な場所にコピーまたはアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="909e9-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="909e9-177">これにより、ファイルは後に異なった環境にもインポートできます。</span><span class="sxs-lookup"><span data-stu-id="909e9-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="909e9-178">Microsoft Azure ストレージ アカウントの使用方法に関する情報は、[AzCopy Command-Line Utility でデータを転送する](/azure/storage/storage-use-azcopy) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="909e9-179">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="909e9-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="909e9-180">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="909e9-181">Azure 仮想マシン (VM) 上の D ドライブの動作に注意してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="909e9-182">Dドライブに、エクスポートしたレポート パーツ グループを完全には保存しません。一時的なドライブの詳細については、次を参照してください。[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="909e9-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="909e9-183">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="909e9-183">Stop services</span></span>

<span data-ttu-id="909e9-184">次のMicrosoft Windows サービスは、Finance and Operations データベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="909e9-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="909e9-185">したがって、Microsoft Remote Desktop を使用して環境内のすべてのコンピュータに接続し、services.msc を使用してこれらのサービスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="909e9-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="909e9-186">ワールド ワイド ウェブ公開サービス (すべての Application Object Server [AOS] コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="909e9-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="909e9-187">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="909e9-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="909e9-188">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス [BI] コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="909e9-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="909e9-189">リセット</span><span class="sxs-lookup"><span data-stu-id="909e9-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="909e9-190">最新の MinorVersionDataUpgrade.zip パッケージをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="909e9-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="909e9-191">最新の MinorVersionDataUpgrade.zip パッケージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="909e9-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="909e9-192">データ アップグレード パッケージの適切なバージョンを検索しダウンロードする手順については、[最新のデータ アップグレード配置可能パッケージをダウンロードする](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="909e9-193">MinorVersionDataUpgrade.zip パッケージをダウンロードするためにアップグレードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="909e9-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="909e9-194">したがって、そのトピックにある「最新のデータ アップグレード配置可能パッケージをダウンロードする」セクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="909e9-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="909e9-195">トピックのその他のすべての手順をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="909e9-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="909e9-196">Finance and Operations データベースに対してスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="909e9-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="909e9-197">財務諸表 データベースに対してではなく、Finance and Operations データベースに対して、次のスクリプトを実行します:</span><span class="sxs-lookup"><span data-stu-id="909e9-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="909e9-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="909e9-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="909e9-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="909e9-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="909e9-200">これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを保証する助けになります。</span><span class="sxs-lookup"><span data-stu-id="909e9-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="909e9-201">データベースをリセットするのには Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="909e9-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="909e9-202">AOS コンピュータで、管理者として Microsoft Windows PowerShell を開始し、Finance and Operations と財務諸表との統合をリセットするために次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="909e9-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="909e9-203">ここでは **Reset-DatamartIntegration** コマンドのパラメータについて説明します:</span><span class="sxs-lookup"><span data-stu-id="909e9-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="909e9-204">**-Reason** の有効な値は、**SERVICING**、**BADDATA**、および **OTHER** です。</span><span class="sxs-lookup"><span data-stu-id="909e9-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="909e9-205">**-ReasonDetail** パラメーターは自由書式です。</span><span class="sxs-lookup"><span data-stu-id="909e9-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="909e9-206">理由と理由の詳細はテレメトリーまたは環境モニタリングに記録されます。</span><span class="sxs-lookup"><span data-stu-id="909e9-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="909e9-207">コマンドを実行した後、データベースをリセットすることを確認するために [**Y**] を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="909e9-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="909e9-208">サービスをリセット</span><span class="sxs-lookup"><span data-stu-id="909e9-208">Restart services</span></span>

<span data-ttu-id="909e9-209">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="909e9-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="909e9-210">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="909e9-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="909e9-211">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="909e9-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="909e9-212">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="909e9-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="909e9-213">レポート定義のインポート</span><span class="sxs-lookup"><span data-stu-id="909e9-213">Import report definitions</span></span>

<span data-ttu-id="909e9-214">エクスポート中に作成されたファイルを使用して、レポート デザイナーからレポート デザインをインポートします。</span><span class="sxs-lookup"><span data-stu-id="909e9-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="909e9-215">レポート デザイナーで、[**会社**] &gt; [**レポート パーツ グループ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="909e9-216">エクスポートする構成要素グループを選択し、[**エクスポート**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="909e9-217">Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="909e9-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="909e9-218">**既定** の構成要素を選択し、[**インポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="909e9-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="909e9-219">エクスポート済みのレポート定義を含むファイルを選択し、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="909e9-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="909e9-220">[**インポート**] ダイアログ ボックスで、インポートするレポート定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="909e9-221">レポート定義および関連するレポート パーツのすべてをインポートするには、[**すべて選択**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="909e9-222">特定のレポート、行、列、ツリー、または分析コードセットをインポートするには、インポートするレポート、行、列、ツリー、または分析コードセットを選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="909e9-223">[**インポート**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="909e9-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="909e9-224">Finance and Operations (オンプレミス) の財務諸表 データ マートをリセットします</span><span class="sxs-lookup"><span data-stu-id="909e9-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="909e9-225">レポート デザイナーおよび Finance and Operations の財務諸表エリアを終了するようすべてのユーザーに指示します。</span><span class="sxs-lookup"><span data-stu-id="909e9-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="909e9-226">財務諸表データベース (MRDB) に対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="909e9-226">Run the following script against the Financial reporting database (MRDB).</span></span>

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

3. <span data-ttu-id="909e9-227">Finance and Operations データベース (AXDB) にある FINANCIALREPORTS テーブルのすべてのレコードを切り捨て、または削除します。</span><span class="sxs-lookup"><span data-stu-id="909e9-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="909e9-228">FINANCIALREPORTVERSION テーブルが Finance and Operations データベースに存在する場合、このテーブルのすべてのレコードを切り捨て、または削除します。</span><span class="sxs-lookup"><span data-stu-id="909e9-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="909e9-229">テーブルが Finance and Operations データベースに存在しない場合、このステップを省略します。</span><span class="sxs-lookup"><span data-stu-id="909e9-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="909e9-230">財務諸表データベースに対して、**ResetDatamart.sql** を実行します。</span><span class="sxs-lookup"><span data-stu-id="909e9-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="909e9-231">このスクリプトはデータ マートの統合を無効にし、すべてのデータ マートを削除し、その後データ マートの統合を再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="909e9-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

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

6. <span data-ttu-id="909e9-232">リセット後は、手動で財務諸表データベースに対して次のクエリを実行し、データの再読み込みを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="909e9-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="909e9-233">すべての行の **LastRunTime** 値、およびその **StateType** が **5** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="909e9-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="909e9-234">**5** の **StateType** 値はデータが正常に再読み込みされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="909e9-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="909e9-235">**7** の値はエラー状態を示します。</span><span class="sxs-lookup"><span data-stu-id="909e9-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="909e9-236">組織階層マップは、初めて実行される時にこの状態になることがあります。</span><span class="sxs-lookup"><span data-stu-id="909e9-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="909e9-237">ただし、エラー状態は自動的に解決されます。</span><span class="sxs-lookup"><span data-stu-id="909e9-237">However, the faulted state but should be automatically resolved.</span></span>

