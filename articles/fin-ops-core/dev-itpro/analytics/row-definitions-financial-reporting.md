---
title: 財務諸表デザイナーでの行の定義
description: 行定義は、財務レポートの各行の内容を指定する、レポート コンポーネントまたは構成要素です。 行定義は、複数の会社が使用できる構成要素グループを作成するために、列定義、レポート ツリー定義およびレポートの定義と組み合わせることができます。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 214a36a1284756e47aa1d28af99234657f1861c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688286"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="5e034-104">財務諸表デザイナーでの行の定義</span><span class="sxs-lookup"><span data-stu-id="5e034-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e034-105">行定義は、財務レポートの各行の内容を指定する、レポート コンポーネントまたは構成要素です。</span><span class="sxs-lookup"><span data-stu-id="5e034-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="5e034-106">行定義は、複数の会社が使用できる構成要素グループを作成するために、列定義、レポート ツリー定義およびレポートの定義と組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="5e034-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="5e034-107">行定義の作成</span><span class="sxs-lookup"><span data-stu-id="5e034-107">Create a row definition</span></span>

1. <span data-ttu-id="5e034-108">レポート デザイナーのナビゲーション ウィンドウで、**行の定義** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="5e034-109">**ファイル** メニューの **新規** をクリックし、**行定義** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="5e034-110">各セルの内容に関する詳細については、[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e034-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="5e034-111">行定義を開く</span><span class="sxs-lookup"><span data-stu-id="5e034-111">Open a row definition</span></span>
1. <span data-ttu-id="5e034-112">レポート デザイナーのナビゲーション ウィンドウで、**行の定義** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="5e034-113">行定義の名前をダブルクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="5e034-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="5e034-114">行定義に関連付けられている構成要素を表示するには、行定義を右クリックし、**関連** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e034-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="5e034-115">行定義の内容</span><span class="sxs-lookup"><span data-stu-id="5e034-115">Contents of a row definition</span></span>
<span data-ttu-id="5e034-116">行定義は、最大 20,000 行の財務分析コードを保有することができ、次の情報を含むことができます:</span><span class="sxs-lookup"><span data-stu-id="5e034-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="5e034-117">**現金** または **総収益** などのセクションの見出し、明細行、およびスペースを作成することでレポートに意味を追加する説明用テキストです。</span><span class="sxs-lookup"><span data-stu-id="5e034-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="5e034-118">Microsoft Dynamics 365 Finance の分析コード値を含めることができる財務データへのリンク</span><span class="sxs-lookup"><span data-stu-id="5e034-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e034-119">行定義を設定して、レポートが生成されるたびに財務分析コード システムからデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5e034-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="5e034-120">リンクされている財務データに基づく行の合計と式です</span><span class="sxs-lookup"><span data-stu-id="5e034-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="5e034-121">通常、行定義の各行には以下の情報タイプの 1 つが含まれています:</span><span class="sxs-lookup"><span data-stu-id="5e034-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="5e034-122">財務分析コード システムへの参照です</span><span class="sxs-lookup"><span data-stu-id="5e034-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="5e034-123">データに基づく合計または計算です</span><span class="sxs-lookup"><span data-stu-id="5e034-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="5e034-124">フォーマット</span><span class="sxs-lookup"><span data-stu-id="5e034-124">Formatting</span></span>

<span data-ttu-id="5e034-125">行定義に情報を入力するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="5e034-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="5e034-126">手動で新しい行定義に行情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e034-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="5e034-127">詳細については、[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e034-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="5e034-128">財務分析コードから行情報を直接プルするには、レポート デザイナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e034-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="5e034-129">詳細については、「[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)」の「関連するフォーミュラ / 行 / 単位」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e034-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="5e034-130">行定義への分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="5e034-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="5e034-131">分析コードは、データおよび値の交差です。</span><span class="sxs-lookup"><span data-stu-id="5e034-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="5e034-132">レポート デザイナーでデータおよび値をグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="5e034-132">You can group data and values in report designer.</span></span> <span data-ttu-id="5e034-133">トランザクションをより詳細に分類および分析できます。</span><span class="sxs-lookup"><span data-stu-id="5e034-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="5e034-134">**分析コードから行を挿入** ダイアログ ボックスを使用して、行定義に複数の行を同時に追加できます。</span><span class="sxs-lookup"><span data-stu-id="5e034-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="5e034-135">ダイアログ ボックスは、分析コードごとに 1 つの列を表示します。</span><span class="sxs-lookup"><span data-stu-id="5e034-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="5e034-136">次の表では、各分析コードで指定する情報のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="5e034-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="5e034-137">オプション</span><span class="sxs-lookup"><span data-stu-id="5e034-137">Option</span></span>                | <span data-ttu-id="5e034-138">説明</span><span class="sxs-lookup"><span data-stu-id="5e034-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="5e034-139">分析コード</span><span class="sxs-lookup"><span data-stu-id="5e034-139">Dimension</span></span>             | <span data-ttu-id="5e034-140">行定義に追加する分析コードを識別するパターンです。</span><span class="sxs-lookup"><span data-stu-id="5e034-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="5e034-141">このパターンには、分析コードの各位置に対応する 1 つのアンパサンド (&) または番号記号 (\#) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5e034-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="5e034-142">通常、[主勘定分析コード] にはすべてアンパサンドを、他の分析コードにはすべて番号記号を使用します。</span><span class="sxs-lookup"><span data-stu-id="5e034-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="5e034-143">分析コード範囲の開始</span><span class="sxs-lookup"><span data-stu-id="5e034-143">Dimension Range Start</span></span> | <span data-ttu-id="5e034-144">この分析コードで行定義に追加する最初の値。</span><span class="sxs-lookup"><span data-stu-id="5e034-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="5e034-145">分析コード範囲の終了</span><span class="sxs-lookup"><span data-stu-id="5e034-145">Dimension Range End</span></span>   | <span data-ttu-id="5e034-146">行定義に追加するこの分析コードの最後の値です。</span><span class="sxs-lookup"><span data-stu-id="5e034-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="5e034-147">行定義に分析コードを追加するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e034-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="5e034-148">レポート デザイナーで **列定義** をクリックして変更する行定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="5e034-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="5e034-149">**編集** メニューで **分析コードから行を挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="5e034-150">**分析コードから行を挿入** ダイアログ ボックスの **分析コード** 行で、行定義に転送する分析コードのセルを選択し、**すべて &&&** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="5e034-151">行定義を特定の範囲の分析コード値に限定するには、**分析コード範囲の開始** セルに開始分析コード値を、**分析コード範囲の終了** セルに終了分析コード値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e034-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="5e034-152">選択した分析コードにすべての値を含めるには、これらのセルを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="5e034-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e034-153">分析コードの範囲のワイルドカード文字 (\* または ?) は、ERP データベースのデータの並べ方によっては、目的の結果のすべてを返さない場合があります。</span><span class="sxs-lookup"><span data-stu-id="5e034-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="5e034-154">**開始行コード** フィールドで、行定義に追加する最初の分析コード値の行コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="5e034-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="5e034-155">**行の増分** フィールドで、連続する行コード間の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e034-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="5e034-156">たとえば、最初の行コードが 100 で増分値が 30 の場合、最初の新しい行コードは 100、130、160、190、および 220 になります。</span><span class="sxs-lookup"><span data-stu-id="5e034-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="5e034-157">新しいフォーマットおよぶ式のフォーミュラを挿入するための十分なスペースを提供する増分値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5e034-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="5e034-158">**OK** をクリックします</span><span class="sxs-lookup"><span data-stu-id="5e034-158">Click **OK**.</span></span> <span data-ttu-id="5e034-159">選択した分析コード値ごとに 1 つの行が行定義に追加されます。</span><span class="sxs-lookup"><span data-stu-id="5e034-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="5e034-160">行定義の丸めの調整</span><span class="sxs-lookup"><span data-stu-id="5e034-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="5e034-161">金額が丸められた貸借対照表がある場合は、合計が不均衡になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5e034-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="5e034-162">この問題は、たとえば、貸借対照表レポートに丸めオプションを使用して、レポート定義が丸め処理を指定した場合でも発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="5e034-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="5e034-163">行定義のオプションの **丸め調整行** オプションを使用して、貸借対照表の金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="5e034-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="5e034-164">レポート定義の **設定** タブで丸めのオフまたは変更ができます。</span><span class="sxs-lookup"><span data-stu-id="5e034-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="5e034-165">次の表に、金額の丸め方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5e034-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="5e034-166">次の表では、丸めがオフになっている場合、行 100 と行 200 の合計が異なります。</span><span class="sxs-lookup"><span data-stu-id="5e034-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="5e034-167">行コード</span><span class="sxs-lookup"><span data-stu-id="5e034-167">Row code</span></span> | <span data-ttu-id="5e034-168">丸めを使用しない金額</span><span class="sxs-lookup"><span data-stu-id="5e034-168">Amounts without rounding</span></span> | <span data-ttu-id="5e034-169">千の単位に丸められた金額</span><span class="sxs-lookup"><span data-stu-id="5e034-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="5e034-170">100</span><span class="sxs-lookup"><span data-stu-id="5e034-170">100</span></span>      | <span data-ttu-id="5e034-171">3,600</span><span class="sxs-lookup"><span data-stu-id="5e034-171">3,600</span></span>                    | <span data-ttu-id="5e034-172">4</span><span class="sxs-lookup"><span data-stu-id="5e034-172">4</span></span>                                       |
| <span data-ttu-id="5e034-173">200</span><span class="sxs-lookup"><span data-stu-id="5e034-173">200</span></span>      | <span data-ttu-id="5e034-174">3,700</span><span class="sxs-lookup"><span data-stu-id="5e034-174">3,700</span></span>                    | <span data-ttu-id="5e034-175">4</span><span class="sxs-lookup"><span data-stu-id="5e034-175">4</span></span>                                       |
| <span data-ttu-id="5e034-176">小計</span><span class="sxs-lookup"><span data-stu-id="5e034-176">Total</span></span>    | <span data-ttu-id="5e034-177">7,300</span><span class="sxs-lookup"><span data-stu-id="5e034-177">7,300</span></span>                    | <span data-ttu-id="5e034-178">8</span><span class="sxs-lookup"><span data-stu-id="5e034-178">8</span></span>                                       |

<span data-ttu-id="5e034-179">貸借対照表の丸めを調整するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e034-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="5e034-180">レポート デザイナーで **列定義** をクリックして変更する行定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="5e034-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="5e034-181">**編集** メニューで、**丸め調整** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="5e034-182">**丸め調整** ダイアログ ボックスに次の値を入力します:</span><span class="sxs-lookup"><span data-stu-id="5e034-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="5e034-183">**丸め調整行** – 貸借対照表の収支を合わせるために調整される行の行コードです。</span><span class="sxs-lookup"><span data-stu-id="5e034-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="5e034-184">**総資産の行** – 総資産を含む貸借対照表の行の行コードです。</span><span class="sxs-lookup"><span data-stu-id="5e034-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="5e034-185">**負債合計および資本の行** – 負債合計および資本を含む貸借対照表の行の行コードです。</span><span class="sxs-lookup"><span data-stu-id="5e034-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="5e034-186">**調整金額の制限** – 自動調整での制限に指定する正の整数です。</span><span class="sxs-lookup"><span data-stu-id="5e034-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="5e034-187">この金額は、実際の丸め誤差の絶対値と比較されます。</span><span class="sxs-lookup"><span data-stu-id="5e034-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e034-188">これらの行コードは、財務データに直接リンクされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e034-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="5e034-189">つまり、行には **財務分析コードへのリンク** セルの分析コード値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e034-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="5e034-190">説明 (**DESC**)、計算 (**CALC**)、または合計 (**TOT**) の行を参照 **しない** でください。</span><span class="sxs-lookup"><span data-stu-id="5e034-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="5e034-191">丸めがオンの場合は、貸借対照表の金額が均等に釣り合います。</span><span class="sxs-lookup"><span data-stu-id="5e034-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="5e034-192">調整の制限は、レポート定義に対して指定されている **丸め桁数** オプションに基づいて適用されます。</span><span class="sxs-lookup"><span data-stu-id="5e034-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="5e034-193">たとえば、レポートで千の位で丸めるよう選択し **調整金額の制限** フィールドに **2** を入力すると、**丸め調整行** フィールドで識別された値が $2,000 単位で増加または減少した場合に警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e034-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="5e034-194">行および列のテキストの書式設定</span><span class="sxs-lookup"><span data-stu-id="5e034-194">Format row and column text</span></span>
<span data-ttu-id="5e034-195">フォントを変更しテキストの書式を設定することにより、レポートの外観をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="5e034-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="5e034-196">次のセクションでは、レポートの行および列の外観の書式を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5e034-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="5e034-197">フォント スタイルの管理</span><span class="sxs-lookup"><span data-stu-id="5e034-197">Manage font styles</span></span>

<span data-ttu-id="5e034-198">レポートのフォント スタイルを作成し、変更できます。</span><span class="sxs-lookup"><span data-stu-id="5e034-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="5e034-199">ドキュメント、またはレポートの特定の行または列に、それらのスタイルを適用できます。</span><span class="sxs-lookup"><span data-stu-id="5e034-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="5e034-200"><strong>フォント スタイルの作成</strong></span><span class="sxs-lookup"><span data-stu-id="5e034-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="5e034-201">レポート デザイナーの <strong>書式設定</strong> メニューで <strong>スタイルおよびフォーマット</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="5e034-202"><strong>スタイルと書式</strong>ダイアログ ボックスの<strong>新規</strong>をクリックしてから、新しいスタイルの固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e034-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="5e034-203">フォントを選択してから、<strong>OK</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5e034-204"><strong>フォント スタイルの変更</strong></span><span class="sxs-lookup"><span data-stu-id="5e034-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="5e034-205">レポート デザイナーの <strong>書式設定</strong> メニューで <strong>スタイルおよびフォーマット</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="5e034-206"><strong>スタイルと書式</strong> ダイアログ ボックスで、変更するスタイルを選択して <strong>変更</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="5e034-207">フォントを選択してから、<strong>OK</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5e034-208"><strong>フォント スタイルの適用</strong></span><span class="sxs-lookup"><span data-stu-id="5e034-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="5e034-209">レポート デザイナーの、定義または列定義、あるいはフッターとヘッダーで、1 つ以上のセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e034-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="5e034-210">ツール バーの<strong>スタイル</strong>リストで、フォント スタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e034-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="5e034-211">行のテキストの書式設定</span><span class="sxs-lookup"><span data-stu-id="5e034-211">Format row text</span></span>

<span data-ttu-id="5e034-212">列定義で指定された書式は、レポート定義で指定された書式を上書きします。</span><span class="sxs-lookup"><span data-stu-id="5e034-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="5e034-213">テキスト形式を変更するには、書式設定ツールバーのコントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e034-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="5e034-214">これらのコントロールは Microsoft Windows 標準のコントロールです。</span><span class="sxs-lookup"><span data-stu-id="5e034-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="5e034-215">レポート デザイナーで、変更する行定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="5e034-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="5e034-216">書式を設定するセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e034-216">Select the cells to format.</span></span> <span data-ttu-id="5e034-217">複数のセルを選択する場合は、Ctrl キーを押しながらセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e034-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="5e034-218">適用するフォーマットのツール バーのボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="5e034-219">たとえば行をインデントにするには、行を選択し、ツール バーの **インデントの増加** ![インデントの増加](media/indent.gif "インデントの増加") をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="5e034-220">レポートのデザイン中に列を調整</span><span class="sxs-lookup"><span data-stu-id="5e034-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="5e034-221">行定義内の作業中の列を見やすくするには、ビュー ウィンドウ内の列の幅を調整し、列を表示または非表示にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5e034-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="5e034-222">加えた変更は、画面に表示される列の外観にだけ影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="5e034-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="5e034-223">レポートの書式設定列には影響しません。</span><span class="sxs-lookup"><span data-stu-id="5e034-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="5e034-224">ビュー ウィンドウ内の列の幅の変更</span><span class="sxs-lookup"><span data-stu-id="5e034-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="5e034-225">レポート デザイナーで、変更する列定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="5e034-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="5e034-226">**書式設定** メニューで、**列の幅** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e034-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="5e034-227">**列の幅** ダイアログ ボックスで、ファイル名を入力し、次に **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="5e034-228">または、列の見出しの右側の境界をドラッグして列の幅を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="5e034-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="5e034-229">ビュー ウィンドウ内の列の非表示</span><span class="sxs-lookup"><span data-stu-id="5e034-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="5e034-230">レポート デザイナーで、変更する列定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="5e034-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="5e034-231">最小化する列を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e034-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="5e034-232">右クリックしてから、**非表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="5e034-233">ビュー ウィンドウ内のすべての非表示の列を表示</span><span class="sxs-lookup"><span data-stu-id="5e034-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="5e034-234">レポート デザイナーで、変更する列定義を開きます。</span><span class="sxs-lookup"><span data-stu-id="5e034-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="5e034-235">表示する最小化された列を右クリックし、**非表示解除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e034-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5e034-236">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5e034-236">Additional resources</span></span>

[<span data-ttu-id="5e034-237">財務諸表</span><span class="sxs-lookup"><span data-stu-id="5e034-237">Financial reporting</span></span>](financial-reporting-intro.md)
