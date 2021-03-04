---
title: 予算計画レイアウトの拡張
description: このトピックでは、BudgetPlanLineActiveView テーブルの列数を拡張して、予算計画レイアウトの追加データに対応する方法を説明します。
author: panolte
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: roschlom
ms.search.region:
- Global for most topics. Set Country/Region name for localizations
ms.author: panolte
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.4
ms.openlocfilehash: 3e1d4431912518ca4262c78861f0568ab4443e0f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017983"
---
# <a name="extend-the-budget-planning-layout"></a><span data-ttu-id="d7bf2-103">予算計画レイアウトの拡張</span><span class="sxs-lookup"><span data-stu-id="d7bf2-103">Extend the budget planning layout</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7bf2-104">このトピックでは、BudgetPlanLineActiveView テーブルの列数を拡張して、予算計画レイアウトの追加データに対応するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-104">This topic describes the process for extending the number of columns in the BudgetPlanLineActiveView table to accommodate additional data in the budget plan layout.</span></span> <span data-ttu-id="d7bf2-105">複数年にわたって情報を比較する場合、多くのシナリオを評価する場合、毎週または毎日の期間を評価する場合、このプロセスが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-105">This process might be required if you're comparing information over multiple years, if many scenarios are being evaluated, or if weekly or daily periods are being evaluated.</span></span> <span data-ttu-id="d7bf2-106">このトピックは開発者が対象です。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-106">This topic was written for a developer audience.</span></span>

- <span data-ttu-id="d7bf2-107">**BudgetPlanLineActiveView テーブル** – この表はピボットされた予算計画データを含みます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-107">**BudgetPlanLineActiveView table** – This table contains the pivoted budget planning data.</span></span> <span data-ttu-id="d7bf2-108">初期状態では、36 の通貨列と 36 の数量列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-108">Out of the box, it contains 36 monetary columns and 36 quantity columns.</span></span> <span data-ttu-id="d7bf2-109">この既定の構成でユーザーは予算計画レイアウトを操作し、最大 3 年間の月次計画データを表示および比較できます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-109">This default configuration lets users manipulate the budget plan layout so that they can show and compare up to three years of monthly planning data.</span></span>
- <span data-ttu-id="d7bf2-110">**BudgetPlanWorksheetEntity エンティティ** – このエンティティは BudgetPlanLineActiveView テーブルに相当し、Microsoft Excel ワークシートのデータソースとして機能します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-110">**BudgetPlanWorksheetEntity entity** – This entity is a counterpart of the BudgetPlanLineActiveView table and serves as a data source for the Microsoft Excel worksheet.</span></span> <span data-ttu-id="d7bf2-111">このエンティティの列は BudgetPlanLineActiveView テーブルの列にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-111">The columns in this entity map to the columns in the BudgetPlanLineActiveView table.</span></span> <span data-ttu-id="d7bf2-112">テーブルの変更は、エンティティで複製する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-112">Any changes in the table must be replicated in the entity.</span></span>

## <a name="extend-the-columns-in-the-budgetplanlineactiveview-table"></a><span data-ttu-id="d7bf2-113">BudgetPlanLineActiveView テーブルで列を拡張する</span><span class="sxs-lookup"><span data-stu-id="d7bf2-113">Extend the columns in the BudgetPlanLineActiveView table</span></span>

<span data-ttu-id="d7bf2-114">4 ステップのプロセスを使用して BudgetPlanLineActiveView テーブルの列を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-114">You can extend the columns in the BudgetPlanLineActiveView table by using a four-step process.</span></span> <span data-ttu-id="d7bf2-115">これらの手順を完了したら、プロジェクトをビルドして変更を検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-115">After you complete these steps, you must build the project and validate your changes.</span></span> 

### <a name="step-1-add-columns-to-the-budgetplanlineactiveview-table"></a><span data-ttu-id="d7bf2-116">ステップ 1: BudgetPlanLineActiveView テーブルに列を追加</span><span class="sxs-lookup"><span data-stu-id="d7bf2-116">Step 1: Add columns to the BudgetPlanLineActiveView table</span></span>

<span data-ttu-id="d7bf2-117">プロセスを開始するには、新しい拡張機能を作成し、フィールドを追加して、追加するフィールドのデータ型を設定します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-117">You begin the process by creating a new extension, adding fields, and setting the data type for the fields that you add.</span></span>

1. <span data-ttu-id="d7bf2-118">Microsoft Visual Studio を開く</span><span class="sxs-lookup"><span data-stu-id="d7bf2-118">Open Microsoft Visual Studio</span></span>
2. <span data-ttu-id="d7bf2-119">アプリケーション エクスプローラを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-119">Open Application explorer.</span></span>
3. <span data-ttu-id="d7bf2-120">**BudgetPlanLineActiveView** テーブルで新しいプロジェクトの拡張を作成します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-120">Create an extension on the **BudgetPlanLineActiveView** table to a new project.</span></span>
4. <span data-ttu-id="d7bf2-121">デザイナー モードでテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-121">Open the table in designer mode.</span></span> 
5. <span data-ttu-id="d7bf2-122">**フィールド** を右クリックして **新規 \> 実績** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-122">Right-click **Fields**, and then select **New \> Real**.</span></span>
6. <span data-ttu-id="d7bf2-123">次に使用可能な名前を使用してフィールドに名前を付け、接尾語が増分されます (たとえば **TransactionCurrencyAmount37**)。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-123">Name the field by using the next available name, where the suffix is incremented (for example, **TransactionCurrencyAmount37**).</span></span>
7. <span data-ttu-id="d7bf2-124">拡張データ型を **BudgetPlanCurrencyAmount** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-124">Set the extended data type to **BudgetPlanCurrencyAmount**.</span></span>
8. <span data-ttu-id="d7bf2-125">**フィールド** を右クリックして **新規 \> 実績** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-125">Right-click **Fields**, and then select **New \> Real**.</span></span>
9. <span data-ttu-id="d7bf2-126">次に使用可能な名前を使用してフィールドに名前を付け、接尾語が増分されます (たとえば **Quantity37**)。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-126">Name the field by using the next available name, where the suffix is incremented (for example, **Quantity37**).</span></span>
10. <span data-ttu-id="d7bf2-127">拡張データ型を **BudgetPlanQuantity** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-127">Set the extended data type to **BudgetPlanQuantity**.</span></span>
11. <span data-ttu-id="d7bf2-128">必要な各拡張データ型のすべての追加列に対してステップ 5 〜 10 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-128">Repeat steps 5 through 10 for all the additional columns of each extended data type that you require.</span></span>
12. <span data-ttu-id="d7bf2-129">オプション: **金額** フィールド グループの数量列に追加された通貨列を **数量** フィールド グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-129">Optional: Add the monetary columns added to the **Monetary** field group quantity columns to the **Quantity** field group.</span></span>

### <a name="step-2-add-columns-to-the-budgetplanworksheetentity-entity"></a><span data-ttu-id="d7bf2-130">ステップ 2 : BudgetPlanWorksheetEntity エンティティに列を追加</span><span class="sxs-lookup"><span data-stu-id="d7bf2-130">Step 2: Add columns to the BudgetPlanWorksheetEntity entity</span></span>

<span data-ttu-id="d7bf2-131">BudgetPlanWorksheetEntity エンティティに列を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-131">To add columns to the BudgetPlanWorksheetEntity entity, follow these follow steps.</span></span>

1. <span data-ttu-id="d7bf2-132">既存のプロジェクトへの **BudgetPlanWorksheetEntity** エンティティで拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-132">Create an extension on the **BudgetPlanWorksheetEntity** entity to the existing project.</span></span>
2. <span data-ttu-id="d7bf2-133">エンティティ拡張機能をデザイナー モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-133">Open the entity extension in designer mode.</span></span>
3. <span data-ttu-id="d7bf2-134">データ ソース ノードからフィールド ノードに列をドラッグします。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-134">Drag the columns from the data sources node into the fields node.</span></span>

### <a name="step-3-create-an-extension-for-the-budgetplan-form"></a><span data-ttu-id="d7bf2-135">ステップ 3: BudgetPlan フォームの拡張機能を作成</span><span class="sxs-lookup"><span data-stu-id="d7bf2-135">Step 3: Create an extension for the BudgetPlan form</span></span>

<span data-ttu-id="d7bf2-136">新しい列を含むように **BudgetPlan** フォームを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-136">To update the **BudgetPlan** form so that it includes the new columns, follow these steps.</span></span>

1. <span data-ttu-id="d7bf2-137">**BudgetPlan** フォームで拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-137">Create an extension on the **BudgetPlan** form.</span></span>
2. <span data-ttu-id="d7bf2-138">**TransactionCurrencyAmount** や **数量** フィールドに存在する新しいイベント ハンドラーで、イベントやカスタマイズを新しいフィールドに複製します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-138">Replicate any events or customizations in a new event handler that exists on the **TransactionCurrencyAmount**, or **Quantity** fields, onto the new fields.</span></span> <span data-ttu-id="d7bf2-139">次の例は **CurrencyAmount** と **数量** の両方に現在存在する標準イベントを示します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-139">The following example shows the standard events that currently exist for both **CurrencyAmount** and **Quantity**.</span></span> <span data-ttu-id="d7bf2-140">これらのイベントは、元の 36 の **CurrencyAmount** と **Quantity** の値を超えて作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-140">These events must be created for anything beyond the original 36 **CurrencyAmount** and **Quantity** values.</span></span>

    ```xpp
    [FormDataFieldEventHandler(formDataFieldStr(BudgetPlan, BudgetPlanLineActiveView, TransactionCurrencyAmount37), FormDataFieldEventType::Modified)]
    publicstaticvoid transactionCurrencyAmount37\_OnModified(FormDataObject \_sender, FormDataFieldEventArgs \_e)
    {
        Object budgetPlanLineActiveView\_ds = \_sender.datasource() asFormDataSource;
        budgetPlanLineActiveView\_ds.updateTransactionCurrencyAmount(fieldNum(BudgetPlanLineActiveView, TransactionCurrencyAmount37));
    }
    [FormDataFieldEventHandler(formDataFieldStr(BudgetPlan, BudgetPlanLineActiveView, Quantity37), FormDataFieldEventType::Modified)]
    publicstaticvoid quantity37\_OnModified(FormDataObject \_sender, FormDataFieldEventArgs \_e)
    {
        Object budgetPlanLineActiveView\_ds = \_sender.datasource() asFormDataSource;
        budgetPlanLineActiveView\_ds.updateQuantity(fieldNum(BudgetPlanLineActiveView, Quantity37));
    }
    ```

3. <span data-ttu-id="d7bf2-141">**TransactionCurrencyAmount** や **数量** 列の作成した各コピーに対して、変更されたイベント ハンドラーが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-141">Verify that a modified event handler exists for every copy that you've created of a **TransactionCurrencyAmount** or **Quantity** column.</span></span>
4. <span data-ttu-id="d7bf2-142">フォーム デザイナーの上の検索フィールドに **LineViewLinesGrid** と入力して、ノードを見つけて展開します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-142">In the search fields above the form designer, enter **LineViewLinesGrid**, find the node, and expand it.</span></span> 

    <span data-ttu-id="d7bf2-143">検索フィールドの最後で **X** を選択して、検索をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-143">Cancel the search by selecting the **X** at the end of the search field.</span></span> <span data-ttu-id="d7bf2-144">行ビュー グリッドは展開されたまま表示されます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-144">The lines view grid will remain expanded and in view.</span></span>

5. <span data-ttu-id="d7bf2-145">追加したすべての新しい列を **LineViewLinesGrid** (グリッド) にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-145">Drag all the new columns that you added onto **LineViewLinesGrid** (the grid).</span></span>
6. <span data-ttu-id="d7bf2-146">既存の命名パターンに従うように、新しいフィールドの名前を変更します (たとえば **TransactionCurrencyAmount37** や **Quantity37**)。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-146">Rename the new fields so that they follow the existing naming pattern (for example, **TransactionCurrencyAmount37** and **Quantity37**).</span></span>
7. <span data-ttu-id="d7bf2-147">**Quantity** と **TransactionCurrencyAmounts** の順序にフィールドを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-147">Reorder the fields so that they are in order for **Quantity** and **TransactionCurrencyAmounts**.</span></span>
8. <span data-ttu-id="d7bf2-148">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-148">Save your changes.</span></span>

### <a name="step-4-update-the-budgetplanlinefieldactiveviewmapping-class-via-a-delegate"></a><span data-ttu-id="d7bf2-149">ステップ 4: デリゲートを介して BudgetPlanLineFieldActiveViewMapping クラスを更新</span><span class="sxs-lookup"><span data-stu-id="d7bf2-149">Step 4: Update the BudgetPlanLineFieldActiveViewMapping class via a delegate</span></span>

<span data-ttu-id="d7bf2-150">BudgetPlanLineActiveView と BudgetPlanLine テーブル間のマッピングを拡張するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-150">To extend the mapping between the BudgetPlanLineActiveView and BudgetPlanLine tables, follow this step.</span></span>

- <span data-ttu-id="d7bf2-151">新しいクラスを作成して **gettingBudgetPlanLineFieldName** デリゲートからイベント ハンドラー メソッドに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-151">Create a new class, and paste in the event handler method from the **gettingBudgetPlanLineFieldName** delegate.</span></span> <span data-ttu-id="d7bf2-152">拡張した **TransactionCurrencyAmount** と **数量** 各フィールドごとに明細書が必要です。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-152">There should be a statement for each **TransactionCurrencyAmount** and **Quantity** field that you extended.</span></span>

    ```xpp
    [SubscribesTo(classStr(BudgetPlanLineFieldActiveViewMapping), staticDelegateStr(BudgetPlanLineFieldActiveViewMapping, gettingBudgetPlanLineFieldName))]
    publicstaticvoid BudgetPlanLineFieldActiveViewMapping\_gettingBudgetPlanLineFieldName(FieldName \_budgetPlanLineActiveViewFieldName, EventHandlerResult \_result)
    {
        FieldName budgetPlanLineFieldName;
        switch (\_budgetPlanLineActiveViewFieldName)
        {
            case
                fieldStr(BudgetPlanLineActiveView, TransactionCurrencyAmount37), fieldStr(BudgetPlanLineActiveView, TransactionCurrencyAmount38):
                budgetPlanLineFieldName = fieldStr(BudgetPlanLine, TransactionCurrencyAmount);
                break;
            case
                fieldStr(BudgetPlanLineActiveView, Quantity37), fieldStr(BudgetPlanLineActiveView, Quantity38):
                budgetPlanLineFieldName = fieldStr(BudgetPlanLine, Quantity);
                break;
        }
        \_result.result(budgetPlanLineFieldName);
    }
    ```

## <a name="build-the-project"></a><span data-ttu-id="d7bf2-153">プロジェクトの構築</span><span class="sxs-lookup"><span data-stu-id="d7bf2-153">Build the project</span></span>

<span data-ttu-id="d7bf2-154">プロジェクトをビルドし、データベースを同期します。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-154">Build your project, and synchronize the database.</span></span>

## <a name="validate-your-changes"></a><span data-ttu-id="d7bf2-155">変更の検証</span><span class="sxs-lookup"><span data-stu-id="d7bf2-155">Validate your changes</span></span>

<span data-ttu-id="d7bf2-156">変更を検証するには、36 の通貨列や数量列を超える予算計画のレイアウトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-156">To validate your changes, you must create a layout in budget planning beyond 36 monetary and/or quantity columns.</span></span> <span data-ttu-id="d7bf2-157">すべてのステップを正しく完了した場合、各列に値を入力し値を保存して Excel で編集できます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-157">If you completed all the steps correctly, you should be able to enter a value in every column, save the value, and edit it in Excel.</span></span>

<span data-ttu-id="d7bf2-158">変更を検証した後は、拡張機能をローカルの開発環境を越えて発行および宣伝できます。</span><span class="sxs-lookup"><span data-stu-id="d7bf2-158">After the changes are verified, the extension can be published and promoted beyond the local development environment.</span></span> 
