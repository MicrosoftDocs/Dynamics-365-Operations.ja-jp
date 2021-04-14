---
title: データベース レベルでの集約計算に対するモデル マッピング コンフィギュレーションの使用
description: このトピックでは、新しい電子申告モデル マッピング構成を設計して、効率的な集計計算の組み込み ER 機能を使用する方法について説明します。
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f48596c30127976d915811ffa8412dcc9b2593
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745378"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="b1ff4-103">データベース レベルでの集約計算に対するモデル マッピング コンフィギュレーションの使用</span><span class="sxs-lookup"><span data-stu-id="b1ff4-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1ff4-104">この手順は、新しい電子申告 (ER) モデル マッピング コンフィギュレーションをデザインして、効率的な集計計算の組み込み ER 機能を使用する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="b1ff4-105">この手順では、サンプル会社 Litware、Inc. のコンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="b1ff4-106">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="b1ff4-107">これらのステップは、任意のデータ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="b1ff4-108">これらの手順を完了するには、手順にあるステップ を最初に実行する必要があり、"ER はデータベース レベルでそれらを実行することで、集約計算の効率が向上を図ります (パート 1 : コンフィギュレーションの準備)。"</span><span class="sxs-lookup"><span data-stu-id="b1ff4-108">To complete these steps, you must first complete the steps in the procedure, "ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations)."</span></span>

1. <span data-ttu-id="b1ff4-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b1ff4-110">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="b1ff4-111">ツリーで、「イントラスタット モデル\イントラスタットのサンプル マッピング」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="b1ff4-112">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-112">Click Designer.</span></span>
5. <span data-ttu-id="b1ff4-113">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-113">Click Designer.</span></span>
6. <span data-ttu-id="b1ff4-114">ツリーで、'Dynamics 365 for Operations\Table records'を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="b1ff4-115">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-115">Click Add root.</span></span>
    * <span data-ttu-id="b1ff4-116">グループ化するレコードを表す新しいデータ ソースを追加</span><span class="sxs-lookup"><span data-stu-id="b1ff4-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="b1ff4-117">[名前] フィールドで、「Transactions」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="b1ff4-118">トランザクション</span><span class="sxs-lookup"><span data-stu-id="b1ff4-118">Transactions</span></span>  
9. <span data-ttu-id="b1ff4-119">[テーブル] フィールドで、「Intrastat」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="b1ff4-120">イントラスタット</span><span class="sxs-lookup"><span data-stu-id="b1ff4-120">Intrastat</span></span>  
10. <span data-ttu-id="b1ff4-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-121">Click OK.</span></span>
11. <span data-ttu-id="b1ff4-122">ツリーで、「Functions\Group by」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="b1ff4-123">このデータ ソースのタイプは、レコードをグループ化して必要な集約を計算する実行時、新しいデータ ソースの案内に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="b1ff4-124">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-124">Click Add root.</span></span>
13. <span data-ttu-id="b1ff4-125">名前 フィールドで、「TransactionsGroups」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="b1ff4-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="b1ff4-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="b1ff4-127">[次の基準でグループを編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-127">Click Edit group by.</span></span>
15. <span data-ttu-id="b1ff4-128">ツリーで、[Transactions] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="b1ff4-129">グループ化したいレコードを表す 'レコード リスト' タイプの追加されたデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-129">Select the added data source of the 'Record list' type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="b1ff4-130">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-130">Click Add field to.</span></span>
17. <span data-ttu-id="b1ff4-131">[グループ化の対象] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-131">Click What to group.</span></span>
18. <span data-ttu-id="b1ff4-132">ツリーで、[Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="b1ff4-133">ツリーで、「Transactions\Direction」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="b1ff4-134">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-134">Click Add field to.</span></span>
21. <span data-ttu-id="b1ff4-135">[グループ化されたフィールド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="b1ff4-136">グループ化レベルを指定するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="b1ff4-137">この選択に基づいて、データ ソースは実行時に、イントラスタットのテーブルで満たされる方向コードがあるように、トランザクションの多くのグループとして返されます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="b1ff4-138">ツリーで、「Transactions\Invoice amount(AmountMST)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="b1ff4-139">集約計算のソースを指定するには、そのフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="b1ff4-140">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-140">Click Add field to.</span></span>
24. <span data-ttu-id="b1ff4-141">[集計] フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="b1ff4-142">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="b1ff4-143">[方法] フィールドで、「Sum」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="b1ff4-144">集約タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="b1ff4-145">[名前] フィールドで、「SumOfAmountMST」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="b1ff4-146">コンフィギュレーション済のデータ ソース内にあるこの集約の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="b1ff4-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-147">Click Save.</span></span>
    * <span data-ttu-id="b1ff4-148">この '実行場所' フィールドには、SQL データ ベースで実行時にこのグループ化が実行されることを示すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-148">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="b1ff4-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-149">Close the page.</span></span>
30. <span data-ttu-id="b1ff4-150">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-150">Click OK.</span></span>
31. <span data-ttu-id="b1ff4-151">ツリーで、「Totals」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="b1ff4-152">ツリーで、「TransactionsGroups」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="b1ff4-153">ツリーで、「TransactionsGroups\aggregated」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="b1ff4-154">ツリーで、「TransactionsGroups\aggregated\SumOfAmountMST」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="b1ff4-155">ツリーで、「Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="b1ff4-156">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-156">Click Bind.</span></span>
    * <span data-ttu-id="b1ff4-157">この設定に基づいて、このデータ ソースはトランザクションの各グループに対して 'AmountMST" フィールドの値の合計を計算します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-157">Based on this setting, this data source will calculate the sum of values of the 'AmountMST' field for each groups of transactions.</span></span> <span data-ttu-id="b1ff4-158">この集約計算は、TransactionsGroups.aggregated.TotalAmount 品目として使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="b1ff4-159">ツリーで、「TransactionsGroups」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="b1ff4-160">ツリーで、「TransactionsGroups」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="b1ff4-161">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-161">Click Edit.</span></span>
40. <span data-ttu-id="b1ff4-162">[次の基準でグループを編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-162">Click Edit group by.</span></span>
41. <span data-ttu-id="b1ff4-163">ツリーで、[Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="b1ff4-164">ツリーで、「Transactions\Invoice amount(AmountMST)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="b1ff4-165">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-165">Click Add field to.</span></span>
44. <span data-ttu-id="b1ff4-166">[集計] フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="b1ff4-167">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="b1ff4-168">[方法] フィールドで、「Max」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="b1ff4-169">[名前] フィールドで、「MaxOfAmountMST」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="b1ff4-170">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-170">Click Save.</span></span>
    * <span data-ttu-id="b1ff4-171">現時点では、SQL のデータベース レベルがいくつかの制限で GROUPBY データ ソースの実行を変換することができます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="b1ff4-172">翻訳は、'レコードの一覧' タイプのデータ ソースまたは FILTER 関数を式として実行するデータ ソースのどちらでも行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-172">Translation can be done for either data sources of the 'Record list' type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="b1ff4-173">また、一つの集約のみがグループ化レコードの単一フィールドのためにコンフィギュレーションされている場合も実行できます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="b1ff4-174">たとえ一つ以上の集約が AmountMST フィールドに対してコンフィギュレーションされたとしても、これはまだ '実行場所' フィールドが SQLデータベースの実行時にこのグループ化が実行されることを示しています。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-174">Note that even though more than one aggregation was configured for the AmountMST field, the 'Execution at' field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="b1ff4-175">これは、一つだけの集計がデータ モデルの品目にバインドされて、このデータ ソースから実行時にデータの取得に使用されるためです。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="b1ff4-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-176">Close the page.</span></span>
50. <span data-ttu-id="b1ff4-177">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-177">Click OK.</span></span>
51. <span data-ttu-id="b1ff4-178">ツリーで、「TransactionsGroups」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="b1ff4-179">ツリーで、「TransactionsGroups\aggregated」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="b1ff4-180">ツリーで、「TransactionsGroups\aggregated\MaxOfAmountMST」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="b1ff4-181">ツリーで、「Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="b1ff4-182">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-182">Click Bind.</span></span>
56. <span data-ttu-id="b1ff4-183">ツリーで、「TransactionsGroups」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="b1ff4-184">ツリーで、「TransactionsGroups」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="b1ff4-185">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-185">Click Edit.</span></span>
59. <span data-ttu-id="b1ff4-186">[次の基準でグループを編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-186">Click Edit group by.</span></span>
    * <span data-ttu-id="b1ff4-187">'実行場所' フィールドは、同じフィールドの両方の集約がデータ モデルの品目にバインドされているため、このグループ化がメモリーで実行時に実行されることを示します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-187">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="b1ff4-188">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="b1ff4-189">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-189">Click Delete.</span></span>
62. <span data-ttu-id="b1ff4-190">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-190">Click Yes.</span></span>
63. <span data-ttu-id="b1ff4-191">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-191">Click Delete.</span></span>
64. <span data-ttu-id="b1ff4-192">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-192">Click Yes.</span></span>
65. <span data-ttu-id="b1ff4-193">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-193">Click Add field to.</span></span>
66. <span data-ttu-id="b1ff4-194">[グループ化の対象] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-194">Click What to group.</span></span>
67. <span data-ttu-id="b1ff4-195">ツリーで、「Commodity record(Intrastat)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="b1ff4-196">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-196">Click Save.</span></span>
    * <span data-ttu-id="b1ff4-197">'実行場所' フィールドは、たとえ集約定義が無く、'テーブル レコード' タイプの選択されたデータ ソースが同じ 'イントラスタット' テーブルを参照しても、このグループ化はメモリーの実行時に実行されることを示します。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-197">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of 'Table records' type refers to the same 'Intrastat' table.</span></span> <span data-ttu-id="b1ff4-198">これは、そのデータ ソースがまだ SQL データベース レベルに翻訳できないいくつかの計算済フィールドを含むからです。</span><span class="sxs-lookup"><span data-stu-id="b1ff4-198">This is because the data source contains some calculated fields which can't yet be translated to the SQL database level.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]