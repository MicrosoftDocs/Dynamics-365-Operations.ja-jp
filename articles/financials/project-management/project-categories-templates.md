---
title: "Project Service Automation からプロジェクトの経費カテゴリを同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Dynamics 365 for Project Service Automation のプロジェクト経費カテゴリを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる

このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Dynamics 365 for Project Service Automation のプロジェクト経費カテゴリを同期させるために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE]
> プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automation および Finance and Operations のデータ フロー

Project Service Automation および Finance and Operations 統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Finance and Operations および Project Service Automation 間のプロジェクト経費トランザクションのカテゴリに関するデータ フローが有効になります。

プロジェクト経費カテゴリが Finance and Operations で習得されている場合、統合フローは最初に Finance and Operations から Project Service Automation へ、次に Project Service Automation から Finance and Operations へ同期することにより、プロジェクト経費カテゴリ統合 ID を更新します。

プロジェクト経費カテゴリが Project Service Automation で習得されている場合、統合フローは最初に Project Service Automation から Finance and Operations になります。 プロジェクト カテゴリは Project Service Automation から同期する前に、Finance and Operations で構成する必要があります。 Finance and Operations から Project Service Automation へ同期すると、Project Service Automation から Finance and Operations へ再度戻ります。 これにより、カテゴリはリンクされ重複は作成されません。

> [!NOTE]
> 通常、プロジェクトの経費カテゴリは Finance and Operations で習得されます。 ユーザーの状況と同じでない場合、または既に Project Service Automation で作成された経費カテゴリがある場合は、まずプロジェクト経費トランザクション カテゴリ (PSA から Finance and Operations) を使用して同期し、次にプロジェクト経費トランザクション カテゴリ (Finance and Operations から PSA) を使用して同期する必要があります。 再び Project Service Automation から Finance and Operations に同期を実行する必要があります。

> Project Service Automation から最初に同期している場合、プロジェクト カテゴリは Finance and Operations および Project Service Automation トランザクション カテゴリと同期させる必要があるプロジェクト カテゴリを**仕訳帳で有効**に設定する必要があります。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>テンプレートおよびタスク

使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Finance and Operations から Project Service Automation へ同期するために使用されます。

-  **データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation)
-  **プロジェクトのタスクの名前:** Project Service Automation にカテゴリを同期

## <a name="entity-set"></a>エンティティ セット

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| カテゴリに対する統合エンティティ    | トランザクション カテゴリ        |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。

## <a name="power-query"></a>Power Query

Microsoft Power Query を使用して、Project Service Automation から同期する時に、トランザクション カテゴリの請求タイプを設定する必要があります。 プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートは、既定の列と既に提示しているマッピングを持っています。 独自のテンプレートを作成する場合は、Power Query に条件付き列を追加する必要があります。
- プロジェクト経費カテゴリのタスクのマッピング内から高度なクエリおよびフィルタリング フォームを開きます。
- **条件付き列の追加**を選択します。
- 新しい列に、BillingType などの名前を付けます。
- 次の条件を入力します。**CATEGORYID が NULL に等しくない場合は 19235001、それ以外の場合は NULL** です。
- 列の **OK** をクリックします。
- マッピング ページにこの新しい列をマップしてください。

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Project Service Automation から Finance and Operations へ同期させるために使用されます。

-**データ統合のテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations) - **プロジェクトのタスクの名前:** Finance and Operations へカテゴリの同期

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| トランザクション カテゴリ          | カテゴリに対する統合エンティティ  | 

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。 Finance and Operations に同期すると、Project Service Automation から Finance and Operations プロジェクト カテゴリの統合 ID に更新されます。

次の図は、データ インテグレーターのタスク マッピングの例を示します。

> [!NOTE]
> マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

