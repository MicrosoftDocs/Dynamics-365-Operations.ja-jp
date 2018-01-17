---
title: "Excel 用予算計画テンプレート"
description: "このトピックでは、予算計画で使用できる Microsoft Excel テンプレートを作成する方法について説明します。"
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 5f75f359d40e385859cdd3cbe3c64dfb3fc4e3a9
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="abe28-103">Excel 用予算計画テンプレート</span><span class="sxs-lookup"><span data-stu-id="abe28-103">Budget planning templates for Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="abe28-104">このトピックでは、予算計画で使用できる Microsoft Excel テンプレートを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="abe28-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="abe28-105">このトピックでは、標準デモ データ セットと管理者ユーザー ログインを使用して予算計画に使用する Excel テンプレートを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="abe28-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="abe28-106">予算計画に関する詳細については、「[予算計画の概要](budget-planning-overview-configuration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abe28-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="abe28-107">「[予算計画 101](budget-plan.md)」チュートリアルに従って、基本モジュールのコンフィギュレーションと使用の原則について参照することもできます。</span><span class="sxs-lookup"><span data-stu-id="abe28-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="abe28-108">予算計画ドキュメント レイアウトを使用したワークシートの生成</span><span class="sxs-lookup"><span data-stu-id="abe28-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="abe28-109">予算計画ドキュメントは、1 つ以上のレイアウトを使用して表示、編集できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="abe28-110">各レイアウトでは、Excel ワークシートで予算計画データを表示および編集する関連の予算計画ドキュメント テンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="abe28-111">このトピックでは、予算計画ドキュメント テンプレートは既存のレイアウト コンフィギュレーションを使用して生成されます。</span><span class="sxs-lookup"><span data-stu-id="abe28-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="abe28-112">[予算計画の一覧] ([予算作成] &gt; [予算計画]) を開きます。</span><span class="sxs-lookup"><span data-stu-id="abe28-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="abe28-113">[新規] をクリックして、新しい予算計画ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="abe28-113">Click **New** to create a new budget plan document.</span></span> 

  <span data-ttu-id="abe28-114">[![予算計画の一覧](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="abe28-115">[追加] の行オプションを使用して、行を追加します。</span><span class="sxs-lookup"><span data-stu-id="abe28-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="abe28-116">[レイアウト] をクリックして、予算計画ドキュメントのレイアウト コンフィギュレーションを表示します。</span><span class="sxs-lookup"><span data-stu-id="abe28-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

  <span data-ttu-id="abe28-117">[![予算計画の追加](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="abe28-118">レイアウト コンフィギュレーションを確認し、必要に応じて調整できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="abe28-119">[テンプレート] &gt; [生成] の順に移動して、このレイアウトの Excel ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="abe28-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="abe28-120">テンプレートが生成された後、[テンプレート] &gt; [表示] の順に移動して予算計画ドキュメント テンプレートを開いて確認します。</span><span class="sxs-lookup"><span data-stu-id="abe28-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="abe28-121">ローカル ドライブに Excel ファイルを保存できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="abe28-122">[![名前を付けて保存](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="abe28-123">予算計画ドキュメント レイアウトは、Excel テンプレートが関連付けられると編集できません。</span><span class="sxs-lookup"><span data-stu-id="abe28-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="abe28-124">レイアウトを変更するには、関連する Excel テンプレート ファイルを削除して再生成します。</span><span class="sxs-lookup"><span data-stu-id="abe28-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="abe28-125">これはレイアウトやワークシートのフィールドの同期を維持するために必要です。</span><span class="sxs-lookup"><span data-stu-id="abe28-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="abe28-126">[ワークシートで利用可能] 列が True になっている場合、Excel テンプレートには予算計画ドキュメント レイアウトのすべての要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="abe28-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="abe28-127">重複する要素は、Excel テンプレートで許可されません。</span><span class="sxs-lookup"><span data-stu-id="abe28-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="abe28-128">たとえば、レイアウトに要求 Q1、要求 Q2、要求 Q3、要求 Q4 の列、4 つすべての四半期の列の合計を表す合計要求列が含まれている場合、その四半期列または合計列は Excel テンプレートで使用できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="abe28-129">Excel ファイルは、テーブルのデータが期限切れおよび不正確になることがあるため、更新時に重複する列を更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="abe28-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="abe28-130">[![例](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="abe28-131">Excel を使用した予算計画データの表示および編集で起こる可能性のある問題を回避するには、同じユーザーが、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition および Microsoft Dynamics Office Add-in Data Connector の両方にログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="abe28-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="abe28-132">予算計画ドキュメント テンプレートへのヘッダーの追加</span><span class="sxs-lookup"><span data-stu-id="abe28-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="abe28-133">ヘッダー情報を追加するには、Excel ファイルの一番上の行を選択し、空の行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="abe28-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="abe28-134">[データ コネクタ] の [デザイン] をクリックして Excel ファイルにヘッダー フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="abe28-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="abe28-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="abe28-136">[デザイン] タブで、[追加] フィールドをクリックしてから、[BudgetPlanHeader] をエンティティ データ ソースとして選択します。</span><span class="sxs-lookup"><span data-stu-id="abe28-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="abe28-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="abe28-138">Excel ファイルの挿入位置にカーソルを合わせます。</span><span class="sxs-lookup"><span data-stu-id="abe28-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="abe28-139">[ラベルの追加] をクリックして、フィールド ラベルを選択した場所に追加します。</span><span class="sxs-lookup"><span data-stu-id="abe28-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="abe28-140">[値の追加] を選択して、選択した場所に値フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="abe28-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="abe28-141">[完了] をクリックしてデザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="abe28-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="abe28-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="abe28-143">予算計画ドキュメント テンプレート テーブルへの計算された列の追加</span><span class="sxs-lookup"><span data-stu-id="abe28-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="abe28-144">次に、計算された列が生成された予算計画ドキュメント テンプレートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="abe28-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="abe28-145">[合計要求] 列は、要求 Q1: 要求 Q4 の列を集計し、[調整] 列は、事前定義された係数によって [合計要求] 列を再計算します。</span><span class="sxs-lookup"><span data-stu-id="abe28-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="abe28-146">[データ コネクタ] の [デザイン] をクリックしてテーブルに列を追加します。</span><span class="sxs-lookup"><span data-stu-id="abe28-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="abe28-147">[BudgetPlanWorkshee] データ ソースの横にある [編集] をクリックして、列の追加を開始します。</span><span class="sxs-lookup"><span data-stu-id="abe28-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="abe28-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="abe28-149">選択したフィールド グループに、テンプレートで使用できる列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="abe28-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="abe28-150">[式] をクリックして新しい列を追加します。</span><span class="sxs-lookup"><span data-stu-id="abe28-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="abe28-151">新しい列に名前を付けてから、式を [式] フィールドに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="abe28-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="abe28-152">[更新] をクリックして列を挿入します。</span><span class="sxs-lookup"><span data-stu-id="abe28-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="abe28-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="abe28-154">式を定義するには、式をスプレッドシートで作成し、[デザイン] ウィンドウにコピーします。</span><span class="sxs-lookup"><span data-stu-id="abe28-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="abe28-155">Finance and Operations のバインドされたテーブルは、通常「AXTable1」と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="abe28-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="abe28-156">たとえば、スプレッドシートの要求 Q1 : 要求 Q4 の列を集計するには、式 = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\] となります。</span><span class="sxs-lookup"><span data-stu-id="abe28-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="abe28-157">以上の手順を繰り返して、[調整] 列を挿入します。</span><span class="sxs-lookup"><span data-stu-id="abe28-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="abe28-158">この列では式 = AxTable1\[Total request\]\\*$I$1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="abe28-158">Use formula = AxTable1\[Total request\]\\*$I$1 for this column.</span></span> <span data-ttu-id="abe28-159">これは、セル I1 の値を取得し、[合計要求] 列の値をかけて、調整金額を計算します。</span><span class="sxs-lookup"><span data-stu-id="abe28-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="abe28-160">Excel ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="abe28-160">Save and close the Excel file.</span></span> <span data-ttu-id="abe28-161">Finance and Operations に戻り、[レイアウト] で、[テンプレート] &gt; [アップロード] をクリックし、予算計画に使用する保存した Excel テンプレートをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="abe28-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="abe28-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="abe28-163">[レイアウト] スライダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="abe28-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="abe28-164">**予算計画**ドキュメントで、[ワークシート] をクリックして Excel でドキュメントを表示して編集します。</span><span class="sxs-lookup"><span data-stu-id="abe28-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="abe28-165">調整された Excel テンプレートがこの予算計画ワークシートの作成に使用され、計算された列が前の手順で定義された式を使用して更新されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="abe28-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="abe28-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="abe28-167">予算計画テンプレートを作成するためのヒントとトリック</span><span class="sxs-lookup"><span data-stu-id="abe28-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="abe28-168">予算計画テンプレートに追加のデータ ソースを追加して使用することはできますか。</span><span class="sxs-lookup"><span data-stu-id="abe28-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="abe28-169">はい、[デザイン] メニューを使用して Excel テンプレートの同じシートまたは他のシートに追加のエンティティを追加できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="abe28-170">たとえば、Excel で予算計画データを使用している場合、[BudgetPlanProposedProject] のデータ ソースを追加して、同時に提示されるプロジェクトの一覧を作成して管理できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="abe28-171">大量のデータ ソースが含まれている場合、Excel ブックのパフォーマンスに影響が出る場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="abe28-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="abe28-172">[データ コネクタ] の [フィルター] オプションを使用して、追加のデータ ソースに希望するフィルターを追加できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="abe28-173">他のユーザーに対してデータ コネクタの [デザイン] オプションを非表示にできますか。</span><span class="sxs-lookup"><span data-stu-id="abe28-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="abe28-174">はい、[データ コネクタ] オプションを開いて、他のユーザーから [デザイン] オプションを非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="abe28-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="abe28-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="abe28-176">[データ コネクタ オプション] を展開して、[デザインの有効化] チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="abe28-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="abe28-177">これで、[デザイン] オプションを [データ コネクタ] から非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="abe28-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="abe28-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="abe28-179">ユーザーがデータを使用する際に、誤ってデータ コネクタを閉じないようにできますか。</span><span class="sxs-lookup"><span data-stu-id="abe28-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="abe28-180">テンプレートをロックしてユーザーが閉じないようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="abe28-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="abe28-181">ロックをオンにするには、[データ コネクタ] をクリックすると、右上に矢印が表示されます。</span><span class="sxs-lookup"><span data-stu-id="abe28-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="abe28-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="abe28-183">追加メニューの矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abe28-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="abe28-184">[ロック] を選択します。</span><span class="sxs-lookup"><span data-stu-id="abe28-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="abe28-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="abe28-186">予算計画テンプレートでセルの書式、色、条件付き書式、グラフなど Excel の他の機能を使用できますか。</span><span class="sxs-lookup"><span data-stu-id="abe28-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="abe28-187">はい、Excel の標準機能のほとんどが、予算計画テンプレートで機能します。</span><span class="sxs-lookup"><span data-stu-id="abe28-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="abe28-188">ユーザーに色コードを使用して読み取り専用と編集可能列を区別することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="abe28-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="abe28-189">条件付き書式は、予算の問題のある領域を強調表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="abe28-190">列合計は、テーブルの Excel の標準式を使用して簡単に表示できます。</span><span class="sxs-lookup"><span data-stu-id="abe28-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="abe28-191">また、予算データの追加のグループ化やビジュアル化のためにピボット テーブルおよびグラフを作成して使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="abe28-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="abe28-192">[データ] タブの [接続] グループで、[すべて更新] をクリックしてから、[接続のプロパティ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abe28-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="abe28-193">[使用] タブをクリックします。[更新] で、[ファイルを開いたときにデータを更新] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="abe28-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="abe28-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="abe28-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




