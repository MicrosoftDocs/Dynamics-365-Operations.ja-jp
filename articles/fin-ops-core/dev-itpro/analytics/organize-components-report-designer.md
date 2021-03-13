---
title: レポート デザイナーのレポートのコンポーネントを整理
description: このトピックでは、レポート デザイナーで既存のレポート、構成要素、オブジェクトを整理する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b55dcee00f571228ec1e933306d77d9edc12866
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092426"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="af20a-103">レポート デザイナーのレポートのコンポーネントを整理</span><span class="sxs-lookup"><span data-stu-id="af20a-103">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af20a-104">構成要素を設計してレポートを生成後、ユーザーがより容易に検索できるようにこれらのオブジェクトを整理するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="af20a-104">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="af20a-105">この記事では、レポート デザイナーで既存のレポート、構成要素、およびオブジェクトを整理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="af20a-105">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="af20a-106">ファイルの整理を容易にするため、レポート デザイナーのフォルダ、レポート、構成要素、他のオブジェクトの名前を変更できます。</span><span class="sxs-lookup"><span data-stu-id="af20a-106">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="af20a-107">名前を変更するオブジェクトのタイプに応じて、そのオブジェクトとの関連付けを更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="af20a-107">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="af20a-108">[レポート デザイナー] で、フォルダまたは構成要素の名前を変更</span><span class="sxs-lookup"><span data-stu-id="af20a-108">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="af20a-109">レポート デザイナーで、フォルダー、レポート定義、行定義、列定義、およびレポート ツリー定義の名前を変更できます。</span><span class="sxs-lookup"><span data-stu-id="af20a-109">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="af20a-110">レポート デザイナーでのフォルダーまたはレポート パーツの名前変更</span><span class="sxs-lookup"><span data-stu-id="af20a-110">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="af20a-111">レポート デザイナーで、ナビゲーション ウィンドウを使用して、名前を変更するフォルダーまたはオブジェクトを探します。</span><span class="sxs-lookup"><span data-stu-id="af20a-111">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="af20a-112">フォルダーまたはオブジェクトを右クリックし、**名前の変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-112">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="af20a-113">ナビゲーション ウィンドウの **名前** フィールドが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="af20a-113">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="af20a-114">新しい名前を入力してから、[入力] を押します。</span><span class="sxs-lookup"><span data-stu-id="af20a-114">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="af20a-115">構成要素が行定義、列定義、またはレポート ツリー定義の場合は、関連付けられる他の構成要素を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af20a-115">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="af20a-116">手順 3 で名前を変更した構成要素を右クリックし、**関連付け** を選択し、一覧から品目を選択して更新します。</span><span class="sxs-lookup"><span data-stu-id="af20a-116">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="af20a-117">すべての関連付けられた品目が更新されるまで手順 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="af20a-117">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="af20a-118">レポート グループの作成および管理</span><span class="sxs-lookup"><span data-stu-id="af20a-118">Create and manage report groups</span></span>
<span data-ttu-id="af20a-119">同時に複数のレポートを生成するレポート定義をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="af20a-119">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="af20a-120">レポート グループを作成、変更、削除、生成するためには、デザイナーまたは管理者ロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="af20a-120">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="af20a-121">ジェネレータのロールを持つユーザーは、レポート グループを生成でき、また、レポート グループに対してユーザー レポート定義の設定を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="af20a-121">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="af20a-122">レポート グループの作成</span><span class="sxs-lookup"><span data-stu-id="af20a-122">Create a report group</span></span>

1. <span data-ttu-id="af20a-123">レポート デザイナーで、ナビゲーション ウィンドウの **レポート グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-123">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="af20a-124">**ファイル** メニューで、**新規** &gt; **レポート グループの定義** をクリックしてビューア ウィンドウで新しいレポート グループを開きます。</span><span class="sxs-lookup"><span data-stu-id="af20a-124">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="af20a-125">または、ツール バーの **レポート グループ** ボタン ![レポート グループ](media/report-group.gif "レポート グループ") をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-125">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="af20a-126">**レポート グループ** タブをクリックします。 このレポートの生成の個々のレポート定義の情報を上書きするには、**個々のレポート定義の会社、詳細、日付の設定の上書き** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="af20a-126">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="af20a-127">会社名、詳細レベル、仮の設定および日付の情報が自動的に入力されますが、更新することができます。</span><span class="sxs-lookup"><span data-stu-id="af20a-127">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="af20a-128">レポート通貨を表示する複数のレポートを生成するには、**すべてのレポート通貨を含む** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="af20a-128">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="af20a-129">レポートを表示するときに、Web ビューアで **通貨** ボタンをクリックすると、複数のビューにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="af20a-129">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="af20a-130">**グループのレポート** フィールドで、**追加** をクリックして、レポート グループに含めるレポートを選択します。</span><span class="sxs-lookup"><span data-stu-id="af20a-130">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="af20a-131">**追加** ダイアログ ボックスの複数のレポートを選択するには、Ctrl キーを押しながら、レポートを選択します。</span><span class="sxs-lookup"><span data-stu-id="af20a-131">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="af20a-132">レポートを選択したら、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-132">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="af20a-133">**ファイル** &gt; **保存** をクリックして、新しいレポート グループを保存します。</span><span class="sxs-lookup"><span data-stu-id="af20a-133">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="af20a-134">レポート グループを変更</span><span class="sxs-lookup"><span data-stu-id="af20a-134">Modify a report group</span></span>

1. <span data-ttu-id="af20a-135">レポート デザイナーで、ナビゲーション ウィンドウの **レポート グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-135">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="af20a-136">変更するレポート グループをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-136">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="af20a-137">**レポート グループ** タブで、必要な変更をします。</span><span class="sxs-lookup"><span data-stu-id="af20a-137">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="af20a-138">**ファイル** メニューで、**保存** をクリックして変更したレポート グループを保存するか、ツール バーで **保存** ボタン ![保存](media/save.gif "保存") をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-138">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="af20a-139">レポートを一定の間隔で生成されるようにスケジュールした場合、これらの設定を上書きし、レポートをすばやく生成できます。</span><span class="sxs-lookup"><span data-stu-id="af20a-139">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="af20a-140">レポート グループのレポートを生成</span><span class="sxs-lookup"><span data-stu-id="af20a-140">Generate a report group report</span></span>

1. <span data-ttu-id="af20a-141">レポート デザイナーで、ナビゲーション ウィンドウの **レポート グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-141">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="af20a-142">生成するレポート グループを開きます。</span><span class="sxs-lookup"><span data-stu-id="af20a-142">Open the report group to generate.</span></span>
3. <span data-ttu-id="af20a-143">**レポートの生成** ボタン ![レポートの生成](media/generate-report.gif "レポートの生成") をクリックして、レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="af20a-143">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="af20a-144">レポート グループの削除</span><span class="sxs-lookup"><span data-stu-id="af20a-144">Delete a report group</span></span>

1. <span data-ttu-id="af20a-145">レポート デザイナーで、ナビゲーション ウィンドウの **レポート グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="af20a-146">削除するレポート グループを右クリックし、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="af20a-146">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="af20a-147">確認メッセージが表示されたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-147">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="af20a-148">[レポート グループ] タブのコントロール</span><span class="sxs-lookup"><span data-stu-id="af20a-148">Report Group tab controls</span></span>
<span data-ttu-id="af20a-149">次の表で、**レポート グループ** タブのコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="af20a-149">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="af20a-150">状態</span><span class="sxs-lookup"><span data-stu-id="af20a-150">Control</span></span></th>
<th><span data-ttu-id="af20a-151">説明</span><span class="sxs-lookup"><span data-stu-id="af20a-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="af20a-152">個々のレポート定義の会社、詳細、日付の設定を上書き</span><span class="sxs-lookup"><span data-stu-id="af20a-152">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="af20a-153">これらのレポートのみの生成に対して、このレポート グループのレポートの個々のレポート定義を上書きする場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="af20a-153">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af20a-154">法人名等</span><span class="sxs-lookup"><span data-stu-id="af20a-154">Company name</span></span></td>
<td><span data-ttu-id="af20a-155">レポートに使用する会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="af20a-155">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af20a-156">詳細レベル</span><span class="sxs-lookup"><span data-stu-id="af20a-156">Detail level</span></span></td>
<td><span data-ttu-id="af20a-157">レポートが含む詳細レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="af20a-157">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="af20a-158"><strong>財務</strong>− 高レベルの集計レポート。</span><span class="sxs-lookup"><span data-stu-id="af20a-158"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="af20a-159">レポート ツリーに追加された勘定および分析コード以外、勘定および分析コードにドリルダウンできません。</span><span class="sxs-lookup"><span data-stu-id="af20a-159">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="af20a-160"><strong>財務&amp; 勘定</strong> ー 上位レベルの集計および勘定の詳細を含むレポート。</span><span class="sxs-lookup"><span data-stu-id="af20a-160"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="af20a-161"><strong>財務、勘定、&amp; トランザクション</strong> ー 上位レベルの集計およびトランザクションの詳細を含むレポート。</span><span class="sxs-lookup"><span data-stu-id="af20a-161"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="af20a-162">[仮]</span><span class="sxs-lookup"><span data-stu-id="af20a-162">Provisional</span></span></td>
<td><span data-ttu-id="af20a-163">レポートが含む活動タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="af20a-163">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="af20a-164"><strong>転記済み活動のみ</strong> ー 財務データに転記されたトランザクションおよび残高のみを含みます。</span><span class="sxs-lookup"><span data-stu-id="af20a-164"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="af20a-165"><strong>転記済みおよび未転記の活動</strong> ー 財務データに入力および転記されたトランザクションおよび残高のすべてを含みます。</span><span class="sxs-lookup"><span data-stu-id="af20a-165"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="af20a-166"><strong>未転記の活動のみ</strong> ー 財務データに入力済で、未転記のトランザクションのみを含みます。</span><span class="sxs-lookup"><span data-stu-id="af20a-166"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="af20a-167">[すべてのレポート通貨を含める]</span><span class="sxs-lookup"><span data-stu-id="af20a-167">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="af20a-168">Microsoft Dynamics ERP システムでコンフィギュレーションされている追加のレポート通貨は、ここに記載されます。</span><span class="sxs-lookup"><span data-stu-id="af20a-168">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="af20a-169">このチェック ボックスを選択して、指定された通貨で追加のレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="af20a-169">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="af20a-170">これらのレポートをWeb ビューアーで表示する場合は、<strong>通貨</strong> ボタンをクリックして通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="af20a-170">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af20a-171">[レポート定義への日付情報の未保存]</span><span class="sxs-lookup"><span data-stu-id="af20a-171">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="af20a-172">基準期間</span><span class="sxs-lookup"><span data-stu-id="af20a-172">Base period</span></span></li>
<li><span data-ttu-id="af20a-173">基準年</span><span class="sxs-lookup"><span data-stu-id="af20a-173">Base year</span></span></li>
<li><span data-ttu-id="af20a-174">[対象となる期間]</span><span class="sxs-lookup"><span data-stu-id="af20a-174">Period covered</span></span></li>
</ul>
<span data-ttu-id="af20a-175">既定の基準期間の設定だけが、レポート定義に保存されます。</span><span class="sxs-lookup"><span data-stu-id="af20a-175">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af20a-176">[レポート定義への日付情報の保存]</span><span class="sxs-lookup"><span data-stu-id="af20a-176">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="af20a-177">報告日</span><span class="sxs-lookup"><span data-stu-id="af20a-177">Report date</span></span></li>
<li><span data-ttu-id="af20a-178">[既定の基準期間]</span><span class="sxs-lookup"><span data-stu-id="af20a-178">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="af20a-179">[グループのレポート]</span><span class="sxs-lookup"><span data-stu-id="af20a-179">Reports in group</span></span></td>
<td><span data-ttu-id="af20a-180">レポート グループのレポートを追加、削除、再発注します。</span><span class="sxs-lookup"><span data-stu-id="af20a-180">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="af20a-181">レポート グループにレポート定義を追加するには、レポート グループをダブルクリックして開き、<strong>追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-181">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="af20a-182">レポート グループに含めるレポートを選択し、<strong>OK</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-182">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="af20a-183">レポート グループからレポートを削除するには、そのレポートを選択し、<strong>削除</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-183">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="af20a-184">レポートを生成する順序を変更するには、リストからレポートを選択して、<strong>上へ移動</strong> または <strong>下へ移動</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af20a-184">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="af20a-185">追加リソース</span><span class="sxs-lookup"><span data-stu-id="af20a-185">Additional resources</span></span>

[<span data-ttu-id="af20a-186">財務諸表</span><span class="sxs-lookup"><span data-stu-id="af20a-186">Financial reporting</span></span>](financial-reporting-intro.md)
