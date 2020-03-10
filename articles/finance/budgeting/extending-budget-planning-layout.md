---
title: 予算計画レイアウトの拡張
description: このトピックでは、BudgetPlanLineActiveView テーブルの列数を拡張して、予算計画レイアウトの追加データに対応する方法を説明します。
author: ryansandness
manager: AnnBe
ms.date: 07/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region:
- Global for most topics. Set Country/Region name for localizations
ms.author: ryansand
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.4
ms.openlocfilehash: 59fc5f3daa58c6744fbfdb180dc4994867593b97
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080751"
---
# <a name="extend-the-budget-planning-layout"></a>予算計画レイアウトの拡張

## <a name="overview"></a>概要

このトピックでは、BudgetPlanLineActiveView テーブルの列数を拡張して、予算計画レイアウトの追加データに対応するプロセスを説明します。 複数年にわたって情報を比較する場合、多くのシナリオを評価する場合、毎週または毎日の期間を評価する場合、このプロセスが必要になる場合があります。 このトピックは開発者が対象です。

- **BudgetPlanLineActiveView テーブル** – この表はピボットされた予算計画データを含みます。 初期状態では、36 の通貨列と 36 の数量列が含まれます。 この既定の構成でユーザーは予算計画レイアウトを操作し、最大 3 年間の月次計画データを表示および比較できます。
- **BudgetPlanWorksheetEntity エンティティ** – このエンティティは BudgetPlanLineActiveView テーブルに相当し、Microsoft Excel ワークシートのデータソースとして機能します。 このエンティティの列は BudgetPlanLineActiveView テーブルの列にマップされます。 テーブルの変更は、エンティティで複製する必要があります。

## <a name="extend-the-columns-in-the-budgetplanlineactiveview-table"></a>BudgetPlanLineActiveView テーブルで列を拡張する

4 ステップのプロセスを使用して BudgetPlanLineActiveView テーブルの列を拡張できます。 これらの手順を完了したら、プロジェクトをビルドして変更を検証する必要があります。 

### <a name="step-1-add-columns-to-the-budgetplanlineactiveview-table"></a>ステップ 1: BudgetPlanLineActiveView テーブルに列を追加

プロセスを開始するには、新しい拡張機能を作成し、フィールドを追加して、追加するフィールドのデータ型を設定します。

1. Microsoft Visual Studio を開く
2. アプリケーション エクスプローラを開きます。
3. **BudgetPlanLineActiveView** テーブルで新しいプロジェクトの拡張を作成します。
4. デザイナー モードでテーブルを開きます。 
5. **フィールド** を右クリックして **新規 \> 実績** を選択します。
6. 次に使用可能な名前を使用してフィールドに名前を付け、接尾語が増分されます (たとえば **TransactionCurrencyAmount37**)。
7. 拡張データ型を **BudgetPlanCurrencyAmount** に設定します。
8. **フィールド** を右クリックして **新規 \> 実績** を選択します。
9. 次に使用可能な名前を使用してフィールドに名前を付け、接尾語が増分されます (たとえば **Quantity37**)。
10. 拡張データ型を **BudgetPlanQuantity** に設定します。
11. 必要な各拡張データ型のすべての追加列に対してステップ 5 〜 10 を繰り返します。
12. オプション: **金額** フィールド グループの数量列に追加された通貨列を **数量** フィールド グループに追加します。

### <a name="step-2-add-columns-to-the-budgetplanworksheetentity-entity"></a>ステップ 2 : BudgetPlanWorksheetEntity エンティティに列を追加

BudgetPlanWorksheetEntity エンティティに列を追加するには、次の手順に従います。

1. 既存のプロジェクトへの **BudgetPlanWorksheetEntity** エンティティで拡張機能を作成します。
2. エンティティ拡張機能をデザイナー モードで開きます。
3. データ ソース ノードからフィールド ノードに列をドラッグします。

### <a name="step-3-create-an-extension-for-the-budgetplan-form"></a>ステップ 3: BudgetPlan フォームの拡張機能を作成

新しい列を含むように **BudgetPlan** フォームを更新するには、次の手順を実行します。

1. **BudgetPlan** フォームで拡張機能を作成します。
2. **TransactionCurrencyAmount** や **数量** フィールドに存在する新しいイベント ハンドラーで、イベントやカスタマイズを新しいフィールドに複製します。 次の例は **CurrencyAmount** と **数量** の両方に現在存在する標準イベントを示します。 これらのイベントは、元の 36 の **CurrencyAmount** と **Quantity** の値を超えて作成する必要があります。

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

3. **TransactionCurrencyAmount** や **数量** 列の作成した各コピーに対して、変更されたイベント ハンドラーが存在することを確認します。
4. フォーム デザイナーの上の検索フィールドに **LineViewLinesGrid** と入力して、ノードを見つけて展開します。 

    検索フィールドの最後で **X** を選択して、検索をキャンセルします。 行ビュー グリッドは展開されたまま表示されます。

5. 追加したすべての新しい列を **LineViewLinesGrid** (グリッド) にドラッグします。
6. 既存の命名パターンに従うように、新しいフィールドの名前を変更します (たとえば **TransactionCurrencyAmount37** や **Quantity37**)。
7. **Quantity** と **TransactionCurrencyAmounts** の順序にフィールドを並べ替えます。
8. 変更を保存します。

### <a name="step-4-update-the-budgetplanlinefieldactiveviewmapping-class-via-a-delegate"></a>ステップ 4: デリゲートを介して BudgetPlanLineFieldActiveViewMapping クラスを更新

BudgetPlanLineActiveView と BudgetPlanLine テーブル間のマッピングを拡張するには、次の手順に従います。

- 新しいクラスを作成して **gettingBudgetPlanLineFieldName** デリゲートからイベント ハンドラー メソッドに貼り付けます。 拡張した **TransactionCurrencyAmount** と **数量** 各フィールドごとに明細書が必要です。

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

## <a name="sync-the-database-and-build-the-project"></a>データベースを同期し、プロジェクトをビルドします

データベースを同期し、プロジェクトをビルドします。

## <a name="validate-your-changes"></a>変更の検証

変更を検証するには、36 の通貨列や数量列を超える予算計画のレイアウトを作成する必要があります。 すべてのステップを正しく完了した場合、各列に値を入力し値を保存して Excel で編集できます。
