---
title: "財務諸表デザイナーでの行の定義"
description: "行定義は、財務レポートの各行の内容を指定する、レポート コンポーネントまたは構成要素です。 行定義は、複数の会社が使用できる構成要素グループを作成するために、列定義、レポート ツリー定義およびレポートの定義と組み合わせることができます。"
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 06a75889e62cbba6e47a8543cf663868df5ae2e3
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="c766a-104">財務諸表デザイナーでの行の定義</span><span class="sxs-lookup"><span data-stu-id="c766a-104">Row definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c766a-105">行定義は、財務レポートの各行の内容を指定する、レポート コンポーネントまたは構成要素です。</span><span class="sxs-lookup"><span data-stu-id="c766a-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="c766a-106">行定義は、複数の会社が使用できる構成要素グループを作成するために、列定義、レポート ツリー定義およびレポートの定義と組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="c766a-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

<a name="create-a-row-definition"></a><span data-ttu-id="c766a-107">行定義の作成</span><span class="sxs-lookup"><span data-stu-id="c766a-107">Create a row definition</span></span>
-----------------------

1.  <span data-ttu-id="c766a-108">レポート デザイナーのナビゲーション ウィンドウで、[**行の定義**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="c766a-109">[**ファイル**] メニューの [**新規**] をクリックし、[**行定義**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="c766a-110">各セルの内容に関する詳細については、[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c766a-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="c766a-111">行定義を開く</span><span class="sxs-lookup"><span data-stu-id="c766a-111">Open a row definition</span></span>
1.  <span data-ttu-id="c766a-112">レポート デザイナーのナビゲーション ウィンドウで、[**行の定義**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="c766a-113">行定義の名前をダブルクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="c766a-113">Double-click the name of the row definition to open.</span></span>
3.  <span data-ttu-id="c766a-114">行定義に関連付けられている構成要素を表示するには、行定義を右クリックし、[**関連**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c766a-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="c766a-115">行定義の内容</span><span class="sxs-lookup"><span data-stu-id="c766a-115">Contents of a row definition</span></span>
<span data-ttu-id="c766a-116">行定義は、最大 20,000 行の財務分析コードを保有することができ、次の情報を含むことができます:</span><span class="sxs-lookup"><span data-stu-id="c766a-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

-   <span data-ttu-id="c766a-117">[**現金**] または [**総収益**] などのセクションの見出し、明細行、およびスペースを作成することでレポートに意味を追加する説明用テキストです。</span><span class="sxs-lookup"><span data-stu-id="c766a-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
-   <span data-ttu-id="c766a-118">Microsoft Dynamics 365 for Finance and Operations の分析コード値を含めることができる財務データへのリンク **注記:** レポートが生成されるたびに財務分析コード システムからデータを取得するよう行定義を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c766a-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations **Note:** You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>
-   <span data-ttu-id="c766a-119">リンクされている財務データに基づく行の合計と式です</span><span class="sxs-lookup"><span data-stu-id="c766a-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="c766a-120">通常、行定義の各行には以下の情報タイプの 1 つが含まれています:</span><span class="sxs-lookup"><span data-stu-id="c766a-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

-   <span data-ttu-id="c766a-121">財務分析コード システムへの参照です</span><span class="sxs-lookup"><span data-stu-id="c766a-121">References to the financial dimensions system</span></span>
-   <span data-ttu-id="c766a-122">データに基づく合計または計算です</span><span class="sxs-lookup"><span data-stu-id="c766a-122">Totals or calculations that are based on the data</span></span>
-   <span data-ttu-id="c766a-123">フォーマット</span><span class="sxs-lookup"><span data-stu-id="c766a-123">Formatting</span></span>

<span data-ttu-id="c766a-124">行定義に情報を入力するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="c766a-124">There are two methods for entering information in a row definition:</span></span>

-   <span data-ttu-id="c766a-125">手動で新しい行定義に行情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c766a-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="c766a-126">詳細については、[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c766a-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
-   <span data-ttu-id="c766a-127">財務分析コードから行情報を直接プルするには、レポート デザイナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="c766a-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="c766a-128">詳細については、「[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)」の「関連するフォーミュラ / 行 / 単位」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c766a-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="c766a-129">行定義への分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="c766a-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="c766a-130">分析コードは、データおよび値の交差です。</span><span class="sxs-lookup"><span data-stu-id="c766a-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="c766a-131">レポート デザイナーでデータおよび値をグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="c766a-131">You can group data and values in report designer.</span></span> <span data-ttu-id="c766a-132">トランザクションをより詳細に分類および分析できます。</span><span class="sxs-lookup"><span data-stu-id="c766a-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="c766a-133">[**分析コードから行を挿入**] ダイアログ ボックスを使用して、行定義に複数の行を同時に追加できます。</span><span class="sxs-lookup"><span data-stu-id="c766a-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="c766a-134">ダイアログ ボックスは、分析コードごとに 1 つの列を表示します。</span><span class="sxs-lookup"><span data-stu-id="c766a-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="c766a-135">次の表では、各分析コードで指定する情報のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="c766a-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="c766a-136">オプション</span><span class="sxs-lookup"><span data-stu-id="c766a-136">Option</span></span>                | <span data-ttu-id="c766a-137">説明</span><span class="sxs-lookup"><span data-stu-id="c766a-137">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c766a-138">分析コード</span><span class="sxs-lookup"><span data-stu-id="c766a-138">Dimension</span></span>             | <span data-ttu-id="c766a-139">行定義に追加する分析コードを識別するパターンです。</span><span class="sxs-lookup"><span data-stu-id="c766a-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="c766a-140">このパターンには、分析コードの各位置に対応する 1 つのアンパサンド (&) または番号記号 (\#) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c766a-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="c766a-141">通常、[主勘定分析コード] にはすべてアンパサンドを、他の分析コードにはすべて番号記号を使用します。</span><span class="sxs-lookup"><span data-stu-id="c766a-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="c766a-142">分析コード範囲の開始</span><span class="sxs-lookup"><span data-stu-id="c766a-142">Dimension Range Start</span></span> | <span data-ttu-id="c766a-143">行定義に追加するこの分析コードの最初の値です。</span><span class="sxs-lookup"><span data-stu-id="c766a-143">The first value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="c766a-144">分析コード範囲の終了</span><span class="sxs-lookup"><span data-stu-id="c766a-144">Dimension Range End</span></span>   | <span data-ttu-id="c766a-145">行定義に追加するこの分析コードの最後の値です。</span><span class="sxs-lookup"><span data-stu-id="c766a-145">The last value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                  |

<span data-ttu-id="c766a-146">行定義に分析コードを追加するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="c766a-146">To add dimensions to a row definition, follow these steps.</span></span>

1.  <span data-ttu-id="c766a-147">レポート デザイナーで [**列定義**] をクリックして変更する行定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="c766a-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="c766a-148">[**編集**] メニューで [**分析コードから行を挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3.  <span data-ttu-id="c766a-149">[**分析コードから行を挿入**] ダイアログ ボックスの [**分析コード**] 行で、行定義に転送する分析コードのセルを選択し、[**すべて &&&**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4.  <span data-ttu-id="c766a-150">行定義を特定の範囲の分析コード値に限定するには、[**分析コード範囲の開始**] セルに開始分析コード値を、[**分析コード範囲の終了**] セルに終了分析コード値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c766a-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="c766a-151">選択した分析コードのすべての値を対象とする場合は、これらのセルは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="c766a-151">To include all values for the selected dimension, leave these cells empty.</span></span> <span data-ttu-id="c766a-152">[**メモ:**] 分析コードの範囲にワイルドカード (\* または ?) を使用すると、ERP データベースのデータの照合方法によっては意図した結果が返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c766a-152">**Note:** Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>
5.  <span data-ttu-id="c766a-153">[**開始行コード**] フィールドで、行定義に追加する最初の分析コード値の行コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="c766a-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6.  <span data-ttu-id="c766a-154">[**行の増分**] フィールドで、連続する行コード間の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="c766a-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="c766a-155">たとえば、最初の行コードが 100 で増分値が 30 の場合、最初の新しい行コードは 100、130、160、190、および 220 になります。</span><span class="sxs-lookup"><span data-stu-id="c766a-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="c766a-156">新しいフォーマットおよぶ式のフォーミュラを挿入するための十分なスペースを提供する増分値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c766a-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7.  <span data-ttu-id="c766a-157">[**OK**] をクリックします</span><span class="sxs-lookup"><span data-stu-id="c766a-157">Click **OK**.</span></span> <span data-ttu-id="c766a-158">選択した分析コード値ごとに 1 つの行が行定義に追加されます。</span><span class="sxs-lookup"><span data-stu-id="c766a-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="c766a-159">行定義の丸めの調整</span><span class="sxs-lookup"><span data-stu-id="c766a-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="c766a-160">金額が丸められた貸借対照表がある場合は、合計が不均衡になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c766a-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="c766a-161">この問題は、たとえば、貸借対照表レポートに丸めオプションを使用して、レポート定義が丸め処理を指定した場合でも発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="c766a-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="c766a-162">行定義のオプションの [**丸め調整行**] オプションを使用して、貸借対照表の金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="c766a-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="c766a-163">レポート定義の [**設定**] タブで丸めのオフまたは変更ができます。</span><span class="sxs-lookup"><span data-stu-id="c766a-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="c766a-164">次の表に、金額の丸め方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c766a-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="c766a-165">次の表では、丸めがオフになっている場合、行 100 と行 200 の合計が異なります。</span><span class="sxs-lookup"><span data-stu-id="c766a-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="c766a-166">行コード</span><span class="sxs-lookup"><span data-stu-id="c766a-166">Row code</span></span> | <span data-ttu-id="c766a-167">丸めを使用しない金額</span><span class="sxs-lookup"><span data-stu-id="c766a-167">Amounts without rounding</span></span> | <span data-ttu-id="c766a-168">千の単位に丸められた金額</span><span class="sxs-lookup"><span data-stu-id="c766a-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="c766a-169">100</span><span class="sxs-lookup"><span data-stu-id="c766a-169">100</span></span>      | <span data-ttu-id="c766a-170">3,600</span><span class="sxs-lookup"><span data-stu-id="c766a-170">3,600</span></span>                    | <span data-ttu-id="c766a-171">4</span><span class="sxs-lookup"><span data-stu-id="c766a-171">4</span></span>                                       |
| <span data-ttu-id="c766a-172">200</span><span class="sxs-lookup"><span data-stu-id="c766a-172">200</span></span>      | <span data-ttu-id="c766a-173">3,700</span><span class="sxs-lookup"><span data-stu-id="c766a-173">3,700</span></span>                    | <span data-ttu-id="c766a-174">4</span><span class="sxs-lookup"><span data-stu-id="c766a-174">4</span></span>                                       |
| <span data-ttu-id="c766a-175">小計</span><span class="sxs-lookup"><span data-stu-id="c766a-175">Total</span></span>    | <span data-ttu-id="c766a-176">7,300</span><span class="sxs-lookup"><span data-stu-id="c766a-176">7,300</span></span>                    | <span data-ttu-id="c766a-177">8</span><span class="sxs-lookup"><span data-stu-id="c766a-177">8</span></span>                                       |

<span data-ttu-id="c766a-178">貸借対照表の丸めを調整するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="c766a-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1.  <span data-ttu-id="c766a-179">レポート デザイナーで [**列定義**] をクリックして変更する行定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="c766a-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="c766a-180">[**編集**] メニューで、[**丸め調整**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3.  <span data-ttu-id="c766a-181">[**丸め調整**] ダイアログ ボックスに次の値を入力します:</span><span class="sxs-lookup"><span data-stu-id="c766a-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>
    -   <span data-ttu-id="c766a-182">[**丸め調整行**] – 貸借対照表の収支を合わせるために調整される行の行コードです。</span><span class="sxs-lookup"><span data-stu-id="c766a-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    -   <span data-ttu-id="c766a-183">[**総資産の行**] – 総資産を含む貸借対照表の行の行コードです。</span><span class="sxs-lookup"><span data-stu-id="c766a-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    -   <span data-ttu-id="c766a-184">[[**負債合計および資本の行**] – 負債合計および資本を含む貸借対照表の行の行コードです。</span><span class="sxs-lookup"><span data-stu-id="c766a-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    -   <span data-ttu-id="c766a-185">[**調整金額の制限**] – 自動調整での制限に指定する正の整数です。</span><span class="sxs-lookup"><span data-stu-id="c766a-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="c766a-186">この金額は、実際の丸め誤差の絶対値と比較されます。</span><span class="sxs-lookup"><span data-stu-id="c766a-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    <span data-ttu-id="c766a-187">**注記:**これらの行コードは、財務データとリンクしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c766a-187">**Note:** These row codes must be linked to your financial data.</span></span> <span data-ttu-id="c766a-188">つまり、行の [**財務分析コードへのリンク**] セルには分析コード値が必要です。</span><span class="sxs-lookup"><span data-stu-id="c766a-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="c766a-189">説明 (**DESC**)、計算 (**CALC**)、または合計 (**TOT**) の行を参照**しない**でください。</span><span class="sxs-lookup"><span data-stu-id="c766a-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="c766a-190">丸めがオンの場合は、貸借対照表の金額が均等に釣り合います。</span><span class="sxs-lookup"><span data-stu-id="c766a-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span> <span data-ttu-id="c766a-191">**注記:**調整の制限は、レポート定義に対して指定されている [**丸め精度**] オプションに基づいて適用されます。</span><span class="sxs-lookup"><span data-stu-id="c766a-191">**Note:** The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="c766a-192">たとえば、レポートで千の位で丸めるよう選択し [**調整金額の制限**] フィールドに「**2**」を入力すると、[**丸め調整行**] フィールドで識別された値が $2,000 単位で増加または減少した場合に警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c766a-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="c766a-193">行および列のテキストの書式設定</span><span class="sxs-lookup"><span data-stu-id="c766a-193">Format row and column text</span></span>
<span data-ttu-id="c766a-194">フォントを変更しテキストの書式を設定することにより、レポートの外観をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="c766a-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="c766a-195">次のセクションでは、レポートの行および列の外観の書式を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c766a-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="c766a-196">フォント スタイルの管理</span><span class="sxs-lookup"><span data-stu-id="c766a-196">Manage font styles</span></span>

<span data-ttu-id="c766a-197">レポートのフォント スタイルを作成し、変更できます。</span><span class="sxs-lookup"><span data-stu-id="c766a-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="c766a-198">ドキュメント、またはレポートの特定の行または列に、それらのスタイルを適用できます。</span><span class="sxs-lookup"><span data-stu-id="c766a-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c766a-199">フォント スタイルの作成</span><span class="sxs-lookup"><span data-stu-id="c766a-199">Create a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="c766a-200">レポート デザイナーの [<strong>書式設定</strong>] メニューで [<strong>スタイルおよびフォーマット</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="c766a-201">[<strong>スタイルおよびフォーマット</strong>] ダイアログ ボックスの [<strong>新規</strong>] をクリックして、新しいスタイル用の一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c766a-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="c766a-202">フォントを選択して [<strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c766a-203">フォント スタイルの変更</span><span class="sxs-lookup"><span data-stu-id="c766a-203">Modify a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="c766a-204">レポート デザイナーの [<strong>書式設定</strong>] メニューで [<strong>スタイルおよびフォーマット</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="c766a-205">[<strong>スタイルおよびフォーマット</strong>] ダイアログ ボックスで、変更するスタイルを選択し、[<strong>変更</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="c766a-206">フォントを選択して [<strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c766a-207">フォント スタイルの適用</span><span class="sxs-lookup"><span data-stu-id="c766a-207">Apply a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="c766a-208">レポート デザイナーの、定義または列定義、あるいはフッターとヘッダーで、1 つ以上のセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c766a-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="c766a-209">ツール バー上の [<strong>スタイル</strong>] 一覧で、フォント スタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c766a-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="c766a-210">行のテキストの書式設定</span><span class="sxs-lookup"><span data-stu-id="c766a-210">Format row text</span></span>

<span data-ttu-id="c766a-211">列定義で指定された書式は、レポート定義で指定された書式を上書きします。</span><span class="sxs-lookup"><span data-stu-id="c766a-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="c766a-212">テキスト形式を変更するには、書式設定ツールバーのコントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="c766a-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="c766a-213">これらのコントロールは Microsoft Windows の標準コントロールです。</span><span class="sxs-lookup"><span data-stu-id="c766a-213">These controls are standard Microsoft Windows controls.</span></span>

1.  <span data-ttu-id="c766a-214">レポート デザイナーで、変更する列定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="c766a-214">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="c766a-215">書式を設定するセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c766a-215">Select the cells to format.</span></span> <span data-ttu-id="c766a-216">複数のセルを選択する場合は、Ctrl キーを押しながらセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c766a-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3.  <span data-ttu-id="c766a-217">適用するフォーマットのツール バーのボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="c766a-218">たとえば行をインデントにするには、行を選択し、ツール バーの **インデントの増加** ![インデントの増加](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "インデントの増加") をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="c766a-219">レポートのデザイン中に列を調整</span><span class="sxs-lookup"><span data-stu-id="c766a-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="c766a-220">行定義内の作業中の列を見やすくするには、ビュー ウィンドウ内の列の幅を調整し、列を表示または非表示にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c766a-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="c766a-221">加えた変更は、画面に表示される列の外観にだけ影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="c766a-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="c766a-222">レポートの書式設定列には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c766a-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="c766a-223">ビュー ウィンドウ内の列の幅の変更</span><span class="sxs-lookup"><span data-stu-id="c766a-223">Change the width of a column in the view pane</span></span>

1.  <span data-ttu-id="c766a-224">レポート デザイナーで、変更する列定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="c766a-224">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="c766a-225">[**書式設定**] メニューで、[**列の幅**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c766a-225">On the **Format** menu, select **Column Width**.</span></span>
3.  <span data-ttu-id="c766a-226">[**列の幅**]ダイアログ ボックスで、ファイル名を入力し、次に [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="c766a-227">または、列の見出しの右側の境界をドラッグして列の幅を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="c766a-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="c766a-228">ビュー ウィンドウ内の列の非表示</span><span class="sxs-lookup"><span data-stu-id="c766a-228">Hide columns in the view pane</span></span>

1.  <span data-ttu-id="c766a-229">レポート デザイナーで、変更する列定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="c766a-229">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="c766a-230">最小化する列を選択します。</span><span class="sxs-lookup"><span data-stu-id="c766a-230">Select the column or columns to minimize.</span></span>
3.  <span data-ttu-id="c766a-231">右クリックしてから、[**非表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="c766a-232">ビュー ウィンドウ内のすべての非表示の列を表示</span><span class="sxs-lookup"><span data-stu-id="c766a-232">Show all hidden columns in the view pane</span></span>

1.  <span data-ttu-id="c766a-233">レポート デザイナーで、変更する列定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="c766a-233">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="c766a-234">表示する最小化された列を右クリックし、[**非表示解除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c766a-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


<a name="see-also"></a><span data-ttu-id="c766a-235">参照</span><span class="sxs-lookup"><span data-stu-id="c766a-235">See also</span></span>
--------

[<span data-ttu-id="c766a-236">財務報告</span><span class="sxs-lookup"><span data-stu-id="c766a-236">Financial reporting</span></span>](financial-reporting-intro.md)




