---
title: "プロジェクト見積を Project Service Automation から Finance and Operations に直接同期します"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations へプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>プロジェクト見積を Project Service Automation から Finance and Operations に直接同期します

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE]
> - プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。
> - 実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.01 以降で使用可能です。
> - Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。 勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations のデータ フロー

Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト時間見積およびプロジェクト経費見積に関するデータ フローを有効にすることができます。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>プロジェクト時間見積

### <a name="template-and-tasks"></a>テンプレートおよびタスク

使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクはプロジェクト時間見積を Project Service Automation から Finance and Operations へ同期するために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクト時間見積 (Project Service Automation から Finance and Operations)
- **プロジェクトのタスク名:**

    - トランザクション リレーションシップ
    - 経費見積

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| プロジェクト タスク              | プロジェクト時間見積の統合エンティティ |

### <a name="entity-flow"></a>エンティティのフロー

プロジェクト時間見積は Project Service Automation で管理され、プロジェクト時間見積として Finance and Operations に同期されます。

### <a name="prerequisites"></a>前提条件

プロジェクト時間見積の同期を行う前に、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクション カテゴリを同期する必要があります。

### <a name="power-query"></a>Power Query

プロジェクト時間見積テンプレートで、Microsoft Power Query for Excel を使用してこれらのタスクを完了する必要があります。

- 統合が新しい時間予測を作成するときに使用される、既定の予測モデル ID を設定します。
- 時間予測への統合に失敗するタスク内のリソース特定のレコードを除外します。
- 空のトランザクション カテゴリ行を除外します。 このタスクを完了しないと、時間予測が正しくない場合があります。

#### <a name="set-the-default-forecast-model-id"></a>既定の予測モデル ID の設定

テンプレートの既定の予測モデル ID を更新するには、**マップ**矢印をクリックしてマッピングを開きます。 次に**高度なクエリおよびフィルタリング**リンクを選択します。

- 既定のプロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合は、**適用されたステップ**のリストで**挿入された条件**を選択します。 **機能**入力で、**O\_forecast**を統合で使用される予測モデル ID の名前に置き換えます。 既定のテンプレートは、デモ データから予測モデル ID を持ちます。
- 新しいテンプレートを作成する場合は、この列を追加する必要があります。 Power Query で、**条件付き列の追加**を選択し、新しい列に **ModelID** などの名前を入力します。 プロジェクト タスクが null でない場合は、列の条件を入力し \<予測モデル ID を入力\>します。その他は null を表します。

#### <a name="filter-out-resource-specific-records"></a>リソースの特定のレコードを除外します

プロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートは、リソースの特定のレコードを削除する既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。 **高度なクエリおよびフィルタリング**リンクを選択して、**msdyn\_islinetask** 列をフィルタリングし **False** レコードのみを含めます。

#### <a name="filter-out-empty-transaction-category-rows"></a>空のトランザクション カテゴリ行を除外します

空のトランザクション カテゴリがある行を削除するためのフィルターを追加する必要があります。 このタスクは、既定のテンプレートを使用している、または独自のテンプレートを作成しているかどうかに関係なく必要です。 このフィルタは、Project Service Automation からの要約行を削除し、Finance and Operations の時間予測が正しくない可能性があります。 **高度なクエリおよびフィルタリング**リンクを選択し、**msdyn\_transactioncategory\_value** 列の null レコードを除外します。

### <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>プロジェクト経費見積

### <a name="template-and-tasks"></a>テンプレートおよびタスク

次のテンプレートおよび基本的なタスクはプロジェクト経費見積を Project Service Automation から Finance and Operations へ同期させるために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクト経費見積 (Project Service Automation から Finance and Operations)
- **プロジェクトのタスク名:**

    - トランザクション リレーションシップ 
    - 経費見積

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| トランザクション接続    | プロジェクト トランザクション リレーションシップに対する統合エンティティ |
| 見積行             | プロジェクト経費見積に対する統合エンティティ         |

### <a name="entity-flow"></a>エンティティのフロー

プロジェクト経費見積は Project Service Automation で管理され、プロジェクト経費見積として Finance and Operations に同期されます。

### <a name="prerequisites"></a>前提条件

プロジェクト経費見積の同期を行う前に、プロジェクト、プロジェクト タスクおよびプロジェクト経費トランザクション カテゴリを同期する必要があります。

### <a name="power-query"></a>Power Query

プロジェクト経費見積テンプレートで、Power Query を使用して以下のタスクを完了する必要があります。

- 経費見積行レコードのみを含めるようにフィルタリングします。
- 統合が新しい時間予測を作成するときに使用される、既定の予測モデル ID を設定します。
- 請求タイプを変換する。
- トランザクション タイプを変換する。

#### <a name="filter-to-include-only-expense-estimate-lines"></a>経費見積行のみを含めるようにフィルターをする

プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートには、統合に経費明細行のみを含む既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。 **トランザクション リレーションシップ**タスクを選択し、次に**マップ**矢印をクリックしてマッピングを開きます。 **高度なクエリおよびフィルタリング**リンクを選択します。 **msdyn\_transactiontype1** 列をフィルタリングして、**msdyn\_estimateline** のみを含むようにします。

#### <a name="set-the-default-forecast-model-id"></a>既定の予測モデル ID の設定

テンプレートの既定の予測モデル ID を更新するには、**経費見積**タスクを選択し、**マップ**矢印をクリックしてマッピングを開きます。 **高度なクエリおよびフィルタリング**リンクを選択します。

- 既定のプロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合、Power Query で、**適用されたステップ**セクションから最初の**挿入された条件**を選択します。 **機能**入力で、**O\_forecast**を統合で使用される予測モデル ID の名前に置き換えます。 既定のテンプレートは、デモ データから予測モデル ID を持ちます。
- 新しいテンプレートを作成する場合は、この列を追加する必要があります。 Power Query で、**条件付き列の追加**を選択し、新しい列に **ModelID** などの名前を入力します。 見積明細行 ID が null でない場合は、列の条件を入力し、\<予測モデル ID を入力\>します。その他は null を表します。

#### <a name="transform-the-billing-types"></a>請求タイプを変換する

プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取った請求タイプを変換するのに使用する条件付き列を含みます。 独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。 **高度なクエリおよびフィルタリング**リンクを選択し、**条件付き列の追加**を選択します。 新しい列に、**BillingType** などの名前を付けます。 次の条件を入力します。

**msdyn\_billingtype** = 192350000 の場合、**NonChargeable**  
**msdyn\_billingtype** = 192350001 の場合は、**Chargeable**  
**msdyn\_billingtype** = 192350002 の場合は、**Complimentary**  
それ以外の場合は **NotAvailable**

#### <a name="transform-the-transaction-types"></a>トランザクション タイプを変換する

プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取ったトランザクション タイプを変換するのに使用する条件付き列を含みます。 独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。 **高度なクエリおよびフィルタリング**リンクを選択し、**条件付き列の追加**を選択します。 新しい列に、**TransactionType** などの名前を付けます。 次の条件を入力します。

**msdyn\_transactiontypecode** = 192350000 の場合、**原価**  
**msdyn\_transactiontypecode** = 192350005 の場合は、**販売**  
それ以外の場合は **null**

### <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![テンプレートのマッピング](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)

