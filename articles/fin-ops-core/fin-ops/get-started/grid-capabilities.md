---
title: グリッド機能
description: このトピックでは、グリッド コントロールのいくつかの強力な機能について説明します。 これらの機能にアクセスするには、新しいグリッド機能が有効になっている必要があります。
author: jasongre
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0fd0e15ea88e9f5f34d8dff82606a8d26616a16d
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260463"
---
# <a name="grid-capabilities"></a><span data-ttu-id="12402-104">グリッド機能</span><span class="sxs-lookup"><span data-stu-id="12402-104">Grid capabilities</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="12402-105">新しいグリッド コントロールは、ユーザーの生産性を高め、データのより興味深いビューを構築し、データの有意義な洞察を得るために使用できる多くの便利で強力な機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="12402-105">The new grid control provides a number of useful and powerful capabilities that can be used to enhance user productivity, construct more interesting views of your data, and get meaningful insights into your data.</span></span> <span data-ttu-id="12402-106">この記事では、次の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="12402-106">This article will cover the following capabilities:</span></span> 

-  <span data-ttu-id="12402-107">合計の計算</span><span class="sxs-lookup"><span data-stu-id="12402-107">Calculating totals</span></span>
-  <span data-ttu-id="12402-108">データのグループ化</span><span class="sxs-lookup"><span data-stu-id="12402-108">Grouping data</span></span>
-  <span data-ttu-id="12402-109">システムの前に入力する</span><span class="sxs-lookup"><span data-stu-id="12402-109">Typing ahead of the system</span></span>
-  <span data-ttu-id="12402-110">数式の評価</span><span class="sxs-lookup"><span data-stu-id="12402-110">Evaluating math expressions</span></span> 

## <a name="calculating-totals"></a><span data-ttu-id="12402-111">合計の計算</span><span class="sxs-lookup"><span data-stu-id="12402-111">Calculating totals</span></span>
<span data-ttu-id="12402-112">Finance and Operations アプリでは、ユーザーはグリッドの数値列の下に合計を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="12402-112">In Finance and Operations apps, users have the ability to see totals at the bottom of numeric columns in grids.</span></span> <span data-ttu-id="12402-113">これらの合計は、グリッドの下部にあるフッター セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="12402-113">These totals are shown in a footer section at the bottom of the grid.</span></span> 

### <a name="showing-the-grid-footer"></a><span data-ttu-id="12402-114">グリッド フッターの表示</span><span class="sxs-lookup"><span data-stu-id="12402-114">Showing the grid footer</span></span>
<span data-ttu-id="12402-115">Finance and Operations アプリでは、すべての表形式のグリッドの下部にフッター領域があります。</span><span class="sxs-lookup"><span data-stu-id="12402-115">There is a footer area at the bottom of every tabular grid in Finance and Operations apps.</span></span> <span data-ttu-id="12402-116">フッターには、グリッドに表示されるデータに関連する貴重な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="12402-116">The footer can show valuable information that is related to the data that appears in the grid.</span></span> <span data-ttu-id="12402-117">この情報の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="12402-117">Here are some examples of this information:</span></span>

- <span data-ttu-id="12402-118">テーブルで選択された行の数 (複数のレコードが選択されている場合)</span><span class="sxs-lookup"><span data-stu-id="12402-118">The number of selected rows in the table (when more than one record is selected)</span></span>
- <span data-ttu-id="12402-119">構成済の数値列の下の総計</span><span class="sxs-lookup"><span data-stu-id="12402-119">Grand totals at the bottom of configured, numeric columns</span></span>
- <span data-ttu-id="12402-120">データセットの行数</span><span class="sxs-lookup"><span data-stu-id="12402-120">The number of rows in the dataset</span></span> 

<span data-ttu-id="12402-121">このフッターは、既定では非表示になっていますが、簡単にオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="12402-121">This footer is hidden by default, but can be easily turned on.</span></span> <span data-ttu-id="12402-122">グリッドのフッターを表示するには、グリッドの列ヘッダーを右クリックし、**フッターを表示**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-122">To show the footer for a grid, right-click on a column header in the grid and select the **Show footer** option.</span></span> <span data-ttu-id="12402-123">特定のグリッドに対してフッターをオンにすると、ユーザーがそのフッターを非表示にするまでその設定が保持されますが、これは、列ヘッダーを右クリックして**フッターを非表示**を選択することで実行できます。</span><span class="sxs-lookup"><span data-stu-id="12402-123">Once the footer has been turned on for a particular grid, that setting will be remembered until the user opts to hide the footer, which can be done by right-clicking on a column header and selecting **Hide footer**.</span></span>  <span data-ttu-id="12402-124">**フッターの表示/非表示**アクションの配置は、今後の更新で再配置される予定です。</span><span class="sxs-lookup"><span data-stu-id="12402-124">Note the placement of the **Show footer/Hide footer** action is expected to be re-located in a future update.</span></span> 

### <a name="specifying-columns-with-totals"></a><span data-ttu-id="12402-125">合計を含む列の指定</span><span class="sxs-lookup"><span data-stu-id="12402-125">Specifying columns with totals</span></span>
<span data-ttu-id="12402-126">現時点では、既定で合計を表示するように列を構成することはできません。</span><span class="sxs-lookup"><span data-stu-id="12402-126">Currently, no columns will be configured to show totals by default.</span></span> <span data-ttu-id="12402-127">代わりに、この操作は、グリッドで列の幅を調整する場合と同じように、1 回の設定操作と見なされます。</span><span class="sxs-lookup"><span data-stu-id="12402-127">Instead, this is considered a one-time setup activity, similar to adjusting the widths of columns in grids.</span></span> <span data-ttu-id="12402-128">列の合計を表示するように指定すると、その設定は、次にページにアクセスしたときに記録されます。</span><span class="sxs-lookup"><span data-stu-id="12402-128">Once you specify that you want to see totals for a column, that setting will be remembered the next time you visit the page.</span></span>  

<span data-ttu-id="12402-129">合計を表示する列を構成するには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="12402-129">There are two ways to configure a column to show a total:</span></span> 

- <span data-ttu-id="12402-130">合計を表示する列を右クリックし、**この列の合計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-130">Right-click in the column that you want to see a total for, and then select **Total this column**.</span></span> <span data-ttu-id="12402-131">このアクションにより、次の 3 つのイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="12402-131">This action causes three events to occur:</span></span>

    1. <span data-ttu-id="12402-132">フッターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="12402-132">The footer becomes visible.</span></span> 
    2. <span data-ttu-id="12402-133">この列の合計を表示するための設定が保存されます。</span><span class="sxs-lookup"><span data-stu-id="12402-133">Your preference for seeing a total for this column is saved.</span></span> 
    3. <span data-ttu-id="12402-134">この列と、合計を表示するために以前に構成した他のすべての列の合計計算が開始されます。</span><span class="sxs-lookup"><span data-stu-id="12402-134">A calculation of totals is initiated for this column and any other columns that you previously configured to see totals for.</span></span> <span data-ttu-id="12402-135">合計を表示するために必要な時間は、合計しているデータセットのサイズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="12402-135">The time that is required to show a total depends on the size of the dataset that you're totaling.</span></span>

- <span data-ttu-id="12402-136">フッターが表示されたら、合計を表示する列の下部のフッター領域にある**合計の表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-136">After the footer is visible, select **Show total** in the footer area at the bottom of the column that you want to see a total for.</span></span> <span data-ttu-id="12402-137">構成された列がない場合は、すべての数値列で**合計の表示**ボタンが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="12402-137">If there are no configured columns, the **Show total** button will be available for all numeric columns.</span></span> 

    <span data-ttu-id="12402-138">合計に対して少なくとも 1 つの列が構成された後は、**合計の表示**ボタンは、ポイント時またはフォーカス時にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="12402-138">After at least one column is configured for totals, the **Show total** buttons will be available only on hover or focus.</span></span> <span data-ttu-id="12402-139">**合計を表示する**を選択するアクションによって、この列の合計を表示するための設定が保存されるので、その設定は今後ページにアクセスするときに適用されます。</span><span class="sxs-lookup"><span data-stu-id="12402-139">The action of selecting **Show total** just saves your preference for seeing a total in this column, so that the preference is applied during future visits to the page.</span></span> <span data-ttu-id="12402-140">フッターでは、この状態は列に表示されるダッシュによって示されます。</span><span class="sxs-lookup"><span data-stu-id="12402-140">In the footer, this state is indicated by a dash that appears in the column.</span></span> <span data-ttu-id="12402-141">(または、データセットが十分に小さい場合は、合計がすぐに表示されます。)</span><span class="sxs-lookup"><span data-stu-id="12402-141">(Alternatively, if the dataset is small enough, a total is immediately shown.)</span></span>

<span data-ttu-id="12402-142">特定の列の合計を表示する必要がなくなった場合は、列を右クリックして、**合計を非表示**を選択するか、その列のフッターで**合計を非表示**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-142">If you make a mistake and no longer want to see a total in a particular column, right-click on the column and select **Hide total** or select the **Hide total** button in the footer in that column.</span></span> <span data-ttu-id="12402-143">この設定は、今後のページへのアクセスのために保存されます。</span><span class="sxs-lookup"><span data-stu-id="12402-143">This preference will also be saved for future visits to the page.</span></span> 

### <a name="calculating-totals"></a><span data-ttu-id="12402-144">合計の計算</span><span class="sxs-lookup"><span data-stu-id="12402-144">Calculating totals</span></span>
<span data-ttu-id="12402-145">フッターが表示され、列がすでに合計に対して構成されているページにアクセスすると、フッターに合計が表示される場合と表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="12402-145">When you come to a page with the footer visible and columns already configured for totals, totals may or may not be shown in the footer.</span></span> <span data-ttu-id="12402-146">動作は、ページ上のデータセットのサイズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="12402-146">The behavior is dependent on the size of the dataset on the page.</span></span> <span data-ttu-id="12402-147">データセットが十分小さい場合は、合計が自動的にデータセットの行数と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="12402-147">If the dataset is sufficiently small, totals will be shown automatically, along with the number of rows in the dataset.</span></span> <span data-ttu-id="12402-148">合計に対して構成した列の下のフッターにダッシュがある場合、データセットが大きすぎてシステムが合計をすぐに表示できないため、合計を計算するには明示的なアクションが必要です。</span><span class="sxs-lookup"><span data-stu-id="12402-148">If there are dashes in the footer under the columns you configured for totals, then the dataset is too large for the system to show totals immediately, and an explicit action is needed to calculate the totals.</span></span> <span data-ttu-id="12402-149">このためには、フッターの**計算**ボタンをクリックするか、合計を表示する列を右クリックし、**この列の合計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-149">To do this, click the **Calculate** button in the footer, or right-click on a column you want a total for and select **Total this column**.</span></span>  

<span data-ttu-id="12402-150">計算に時間がかかりすぎる場合は、**キャンセル** ボタンを選択して操作を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="12402-150">If the calculation is taking too long, you can cancel the operation by selecting the **Cancel** button.</span></span> <span data-ttu-id="12402-151">ただし、データセットが大きすぎて合計を計算できない場合があり (組織によって課される制限)、代わりにデータをさらにフィルタ処理するように通知されます。</span><span class="sxs-lookup"><span data-stu-id="12402-151">Sometimes, however, the dataset will be too large to calculate totals (a limit imposed by your organization), and you will instead be notified to filter your data more.</span></span>

<span data-ttu-id="12402-152">データセットの行を更新、削除、または作成すると、合計が自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="12402-152">Totals will update automatically as you update, delete, or create rows in the dataset.</span></span>  

## <a name="grouping-data"></a><span data-ttu-id="12402-153">データのグループ化</span><span class="sxs-lookup"><span data-stu-id="12402-153">Grouping data</span></span>
<span data-ttu-id="12402-154">多くの場合、ビジネス ユーザーは、データのアド ホック分析を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12402-154">Business users often need to perform ad-hoc analysis of data.</span></span> <span data-ttu-id="12402-155">これは、Microsoft Excel にデータをエクスポートしてピボット テーブルを使用することで実行できますが、表形式グリッドの**グループ化**機能を使用すると、ユーザーは Finance and Operations アプリ内でデータを興味深い方法で整理できます。</span><span class="sxs-lookup"><span data-stu-id="12402-155">While this can be done by exporting data to Microsoft Excel and using pivot tables, the **Grouping** capability in tabular grids allows users to organize their data in interesting ways within Finance and Operations apps.</span></span> <span data-ttu-id="12402-156">この機能によって**合計**機能が拡張されるのに対し、**グループ化**では、グループ レベルで小計を提供することにより、データについて有意義な洞察を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="12402-156">As this feature extends the **Totals** feature, **Grouping** also allows you to get meaningful insights into the data by providing subtotals at the group level.</span></span>

<span data-ttu-id="12402-157">この機能を使用するには、グループ化する列を右クリックし、**この列別にグループ化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-157">To use this feature, right-click on the column you wish to group by, and select **Group by this column**.</span></span> <span data-ttu-id="12402-158">このアクションにより、選択した列でデータが並べ替えられ、グリッドの先頭に新しいグループ化列が追加されてから、各グループの先頭に「ヘッダー行」が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="12402-158">This action will sort the data by the selected column, add a new Group by column to the beginning to the grid, and insert "header rows" at the beginning of each group.</span></span> <span data-ttu-id="12402-159">これらのヘッダー行では、各グループについて次の情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="12402-159">These header rows provide the following information about each group:</span></span> 
-  <span data-ttu-id="12402-160">グループのデータ値</span><span class="sxs-lookup"><span data-stu-id="12402-160">Data value for the group</span></span> 
-  <span data-ttu-id="12402-161">列ラベル (この情報は、複数のグループ化レベルがサポートされている場合に特に役立ちます。)</span><span class="sxs-lookup"><span data-stu-id="12402-161">Column label (This information will be especially useful after multiple levels of grouping are supported.)</span></span>
-  <span data-ttu-id="12402-162">このグループのデータ行の数</span><span class="sxs-lookup"><span data-stu-id="12402-162">Number of data rows in this group</span></span>
-  <span data-ttu-id="12402-163">合計を表示するように構成された列の小計</span><span class="sxs-lookup"><span data-stu-id="12402-163">Subtotals for any column configured to show totals</span></span>

<span data-ttu-id="12402-164">[保存されているビュー](saved-views.md) を有効にすると、このグループ化をビューの一部としてパーソナル化によって保存し、次回ページにアクセスするときに素早くアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="12402-164">With [Saved views](saved-views.md) enabled, this grouping can be saved by personalization as part of a view for quick access the next time you visit the page.</span></span>  

<span data-ttu-id="12402-165">別の列で**この列別にグループ化**を選択すると、元のグループ化が置き換えられます。これは、プラットフォーム更新プログラム 33 を使用したバージョン 10.0.9 では 1 つのレベルのグループ化のみがサポートされているためです。</span><span class="sxs-lookup"><span data-stu-id="12402-165">If you select **Group by this column** for a different column, the original grouping is replaced, because only one level of grouping is supported in version 10.0.9 with Platform update 33.</span></span>

<span data-ttu-id="12402-166">グリッドのグループ化を元に戻すには、グループ化列を右クリックして、**グループ化解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-166">To undo grouping in a grid, right-click on the grouping column and select **Ungroup**.</span></span>  


## <a name="evaluating-math-expressions"></a><span data-ttu-id="12402-167">数式の評価</span><span class="sxs-lookup"><span data-stu-id="12402-167">Evaluating math expressions</span></span>
<span data-ttu-id="12402-168">生産性を高めるため、ユーザーはグリッドの数値セルに公式を入力できます。</span><span class="sxs-lookup"><span data-stu-id="12402-168">As a productivity booster, users can enter mathematical formulas in numeric cells in a grid.</span></span> <span data-ttu-id="12402-169">システム外部のアプリで計算を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="12402-169">They don't have to do the calculation in an app outside the system.</span></span> <span data-ttu-id="12402-170">例えば、**=15\*4** と入力して、**タブ** キーを押してフィールドの外に移動すると、システムによって式が評価され、フィールドの値として **60** が保存されます。</span><span class="sxs-lookup"><span data-stu-id="12402-170">For example, if you enter **=15\*4** and then press the **Tab** key to move out of the field, the system will evaluate the expression and save a value of **60** for the field.</span></span>

<span data-ttu-id="12402-171">値が式としてシステムで認識されるようにするには、値を等号 (**=**) で開始します。</span><span class="sxs-lookup"><span data-stu-id="12402-171">To make the system recognize a value as an expression, start the value with an equal sign (**=**).</span></span> <span data-ttu-id="12402-172">サポートされている演算子と構文の詳細については、[サポートされている数式記号](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12402-172">For more information about the supported operators and syntax, see [Supported math symbols](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="12402-173">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="12402-173">Frequently asked questions</span></span>
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a><span data-ttu-id="12402-174">環境で新しいグリッド コントロールを有効有効にするにはどうすればよいですか?</span><span class="sxs-lookup"><span data-stu-id="12402-174">How do I enable the new grid control in my environment?</span></span> 

<span data-ttu-id="12402-175">**10.0.9 / Platform update 33 以降** **新しいグリッド コントロール** 機能は、任意の環境の機能管理で直接使用できます。</span><span class="sxs-lookup"><span data-stu-id="12402-175">**10.0.9 / Platform update 33 and later** The **New grid control** feature is available directly in Feature management in any environment.</span></span> <span data-ttu-id="12402-176">他の公開プレビュー機能と同様に、実稼働でこの機能を有効にするには、[補足利用規約](https://go.microsoft.com/fwlink/?linkid=2105274) が適用されます。</span><span class="sxs-lookup"><span data-stu-id="12402-176">Like other public preview features, enabling this feature in production is subject to the [Supplemental Terms of Use Agreement](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>  

<span data-ttu-id="12402-177">**10.0.8 / Platform update 32 および 10.0.7 / Platform update 31** **新しいグリッド コントロール** 機能は、レベル 1 (開発/テスト) およびレベル 2 (サンドボックス) 環境で有効にして、以下の手順に従って追加のテストとデザイン変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="12402-177">**10.0.8 / Platform update 32 and 10.0.7 / Platform update 31** The **New grid control** feature can be enabled in Tier 1 (Dev/Test) and Tier 2 (Sandbox) environments in order to provide additional testing and design changes by following the steps below.</span></span>

1.  <span data-ttu-id="12402-178">**フライトを有効にする** : 次の SQL 明細書を実行します。</span><span class="sxs-lookup"><span data-stu-id="12402-178">**Enable the flight**: Execute the following SQL statement:</span></span> 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. <span data-ttu-id="12402-179">**IIS をリセット**して、静的なフライティング キャッシュをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="12402-179">**Reset IIS** to flush the static flighting cache.</span></span> 

3.  <span data-ttu-id="12402-180">**機能の検索** : **機能管理** ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="12402-180">**Find the feature**: Go to the **Feature management** workspace.</span></span> <span data-ttu-id="12402-181">すべての機能の一覧に **新しいグリッド コントロール** が表示されない場合は、**更新プログラムの確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-181">If **New grid control** does not appear in the list of all features, select **Check for updates**.</span></span>   

4.  <span data-ttu-id="12402-182">**機能の有効化**: 機能の一覧で **新しいグリッド コントロール** 機能を検索し、詳細ウィンドウの **直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12402-182">**Enable the feature**: Find the **New grid control** feature in the list of features, and select **Enable now** on the details pane.</span></span> <span data-ttu-id="12402-183">ブラウザーの更新が必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="12402-183">Note that a browser refresh is required.</span></span> 

<span data-ttu-id="12402-184">以降のすべてのユーザー セッションは、新しいグリッド コントロールを有効にして開始されます。</span><span class="sxs-lookup"><span data-stu-id="12402-184">All subsequent user sessions will start with the new grid control enabled.</span></span>
