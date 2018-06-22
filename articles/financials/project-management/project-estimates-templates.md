---
title: "Project Service Automation からプロジェクト見積を直接 Finance and Operations のプロジェクト予測に同期します"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Project Service Automation からプロジェクト見積を直接 Finance and Operations のプロジェクト予測に同期します

このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE]
> プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations のデータ フロー

Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト時間見積およびプロジェクト経費見積に関するデータ フローを有効にすることができます。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>テンプレートおよびタスク

使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクはプロジェクト時間見積を Project Service Automation から Finance and Operations へ同期するために使用されます。

-  **データ統合でのテンプレートの名前:** プロジェクト時間見積 (Project Service Automation から Finance and Operations)

-  **プロジェクトのタスク名:** 
    - トランザクション リレーションシップ 
    - 経費見積

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| プロジェクト タスク                   | プロジェクト時間見積の統合エンティティ   |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト時間見積は Project Service Automation で管理され、プロジェクト時間見積として Finance and Operations に同期されます。

## <a name="preconditions"></a>事前条件

プロジェクト時間見積の同期を行う前に、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクション カテゴリを同期する必要があります。

## <a name="power-query"></a>Power Query

プロジェクト時間見積もりテンプレートで Microsoft Power Query を使用して、以下を行う必要があります。
- 統合が、新しい時間予測を作成するときに使用される**予測モデル ID** を設定します。
- 時間予測への統合に失敗するタスク内のリソース特定のレコードを除外します
- 空のトランザクション カテゴリ行を除外します。 これを行わないと、時間予測が正しくない場合があります。

### <a name="forecast-model-id"></a>予測モデル ID
テンプレートの既定の予測モデル ID を更新するには、**マップ**矢印をクリックしてマッピングを開きます。 高度なクエリおよびフィルタリングを選択して開きます。
- 既定の Microsoft Project 時間見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合は、**適用されたステップ**セクションで**挿入された条件**を選択します。 **機能**入力で、**O_forecast** を統合して使用する**予測モデル ID** の名前に置き換える必要があります。 既定のテンプレートは、デモ データから予測モデル ID を持ちます。
- 新しいテンプレートを作成する場合は、この列を追加する必要があります。 **条件付き列の追加**を選択し、列に ModelID などの名前を付けます。 プロジェクト タスクが null でない場合は列の条件を入力し、次に<enter the forecast model ID>を行います。その他 null を表します。

### <a name="filter-out-resource-specific-records"></a>リソースの特定のレコードを除外します
プロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートは、リソースの特定のレコードを削除する既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。 高度なクエリおよびフィルタリング フォームでは、**msdyn_islinetask** 列にフィルターを選択し **False** レコードのみを含めます。

### <a name="filter-out-empty-transaction-category-rows"></a>空のトランザクション カテゴリ行を除外します
空のトランザクション カテゴリの行を削除するフィルターを追加する必要があります。 これは、既定のテンプレートを使用している場合でも、独自のテンプレートを作成している場合でも必要です。 このフィルタは、Project Service Automation からの要約行を削除し、Finance and Operations の時間予測が正しくない可能性があります。 高度なクエリおよびフィルタリング フォームで、**msdyn_transactioncategory_value** 列の null レコードを除外するように選択します。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

次のテンプレートおよび基本的なタスクはプロジェクト経費見積を Project Service Automation から Finance and Operations へ同期させるために使用されます。

-  **データ統合でのテンプレートの名前:** プロジェクト経費見積 (Project Service Automation から Finance and Operations)
-  **プロジェクトのタスク名:** 
     - トランザクション リレーションシップ 
     - 経費見積

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| トランザクション接続         | プロジェクト トランザクション リレーションシップの統合エンティティ。   |
| 見積行                  | プロジェクト経費見積の統合エンティティ。           |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト経費見積は Project Service Automation で管理され、プロジェクト経費見積として Finance and Operations に同期されます。

## <a name="prerequisites"></a>前提条件

プロジェクト経費見積の同期を行う前に、プロジェクト、プロジェクト タスクおよびプロジェクト経費トランザクション カテゴリを同期する必要があります。

## <a name="power-query"></a>Power Query

プロジェクト経費見積テンプレートの Microsoft Power Query を使用する必要があります。
- 経費見積行レコードのみを含めるようにフィルターをする
- 統合が、新しい時間予測を作成するときに使用される**予測モデル ID** を設定します。
- 請求タイプを変換する。
- トランザクション タイプを変換する。

### <a name="filter-to-include-only-expense-estimate-lines"></a>経費見積行のみを含めるようにフィルターをする
プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートには、統合に経費明細行のみを含めるための既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。 トランザクション リレーションシップのタスクを選択し**マップ**矢印をクリックします。 **高度なクエリとフィルター処理**を選択。 **msdyn_estimateline** のみを含む **msdyn_transactiontype1** 列のフィルター。

### <a name="forecast-model-id"></a>予測モデル ID
テンプレートの既定の予測モデル ID を更新するには、経費見積タスクで、**マップ**矢印をクリックしてマッピングを開きます。 高度なクエリおよびフィルタリングを選択して開きます。
- 既定の Microsoft Project 経費見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合は、**適用されたステップ** セクションで最初の**挿入された条件**を選択します。 **機能**入力で、**O_forecast** を統合して使用する**予測モデル ID** の名前に置き換える必要があります。 既定のテンプレートは、デモ データから予測モデル ID を持ちます。
- 新しいテンプレートを作成する場合は、この列を追加する必要があります。 **条件付き列の追加**を選択し、列に ModelID などの名前を付けます。 見積明細行 ID が null でない場合は、<予測モデル ID を入力> の列の条件を入力します。その他は null を表します。

### <a name="transform-the-billing-types"></a>請求タイプを変換する
プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取った請求タイプを変換するための条件付き列が追加されます。
- 独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。 高度なクエリおよびフィルタリング フォームで、**条件付き列の追加**を選択します。 列に、「BillingType」などの名前を付けます。 入力する条件は次のとおりです。

    **msdyn_billingtype** = 192350000 の場合は、**NonChargeable** それ以外の場合は **msdyn_billingtype** = 192350001、**Chargeable** ならば **msdyn_billingtype** = 192350002、**Complimentary** 以外は **NotAvailable**

### <a name="transform-the-transaction-types"></a>トランザクション タイプを変換する
プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取ったトランザクション タイプを変換するための条件付き列が追加されます。
- 独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。 高度なクエリおよびフィルタリング フォームで、**条件付き列の追加**を選択します。 列に、「TransactionType」などの名前を付けます。 入力する条件は次のとおりです。**msdyn_transactiontypecode** = 192350000 の場合、次に**原価**他に **msdyn_transactiontypecode** = 192350005、それから**販売**他 **null**

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![テンプレートのマッピング](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




