---
title: "Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 for Project Service Automation のプロジェクト経費カテゴリを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 for Project Service Automation のプロジェクト経費カテゴリを同期させるために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE]
> - プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。
> - 実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.01 以降で使用可能です。
> - Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。 勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automation および Finance and Operations のデータ フロー

Project Service Automation および Finance and Operations 統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Finance and Operations および Project Service Automation 間のプロジェクト経費トランザクションのカテゴリに関するデータ フローが有効になります。

プロジェクト経費カテゴリが Finance and Operations で習得されている場合、統合フローは最初に Finance and Operations から Project Service Automation になります。 Project Service Automation から Finance and Operations への同期を通してプロジェクトの経費カテゴリの統合 ID が更新されます。

プロジェクト経費カテゴリが Project Service Automation で習得されている場合、統合フローは最初に Project Service Automation から Finance and Operations になります。 プロジェクト カテゴリは Project Service Automation から同期する前に、Finance and Operations で構成する必要があります。 Finance and Operations から Project Service Automation へ同期すると、Project Service Automation から Finance and Operations へ再度戻ります。 これにより、カテゴリがリンクされていると重複が作成されないことを保証します。

> [!NOTE]
> 通常、プロジェクトの経費カテゴリは Finance and Operations で習得されます。 ただし、Finance and Operations でマスターされていない場合、または Project Service Automation で経費カテゴリが既に作成されている場合は、プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations) を使用して最初に同期する必要があります。 次にプロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートを使用して同期します。 それから Project Service Automation から Finance and Operations にもう一度同期を実行する必要があります。
>
> Project Service Automation から最初に同期する場合は、同期を実行する前に Finance and Operations で次の要件を満たす必要があります。
>
> - Project Service Automation で設定されるプロジェクト カテゴリに一致する共有カテゴリが存在し、それは**プロジェクト**および**経費**の両方に対して有効である必要があります。
> - 統合する必要がある Finance and Operations の各法人に対して、次のプロジェクト カテゴリが存在する必要があります。
>
>     - **プロジェクト カテゴリ**が存在します。 
>     - **経費での使用**が有効になっています。
>     - **仕訳帳で有効**が有効になっています。
>     - **トランザクション タイプ**を**経費**に設定します。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Finance and Operations から Project Service Automation へのプロジェクト経費カテゴリの同期

### <a name="template-and-task"></a>テンプレートおよびタスク

テンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Finance and Operations から Project Service Automation へ同期するために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation)
- **プロジェクトのタスクの名前:** Project Service Automation にカテゴリを同期

### <a name="entity-set"></a>エンティティ セット

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| カテゴリに対する統合エンティティ | トランザクション カテゴリ     |

### <a name="entity-flow"></a>エンティティのフロー

プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。

### <a name="power-query"></a>Power Query

Project Service Automation から同期する時に、Microsoft Power Query for Excel を使用してトランザクション カテゴリの請求タイプを設定する必要があります。 プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートは、既定の列とマッピングを提供します。 独自のテンプレートを作成する場合は、Power Query に条件付き列を追加する必要があります。 以下の手順を実行します。

1. プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートで、プロジェクト経費カテゴリ タスクのマッピングを開くには、矢印をクリックします。
2. **高度なクエリおよびフィルタリング**リンクをクリックして、Power Query を開きます。
2. **条件付き列の追加**を選択します。
3. 新しい列に、**BillingType** などの名前を付けます。
4. 次の条件を入力します。**CATEGORYID が NULL に等しくない場合は 19235001、それ以外の場合は NULL** です。
5. 列の **OK** をクリックします。
6. マッピング ページでこの新しい列をマップしてください。

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations へのプロジェクト経費カテゴリの同期

### <a name="template-and-task"></a>テンプレートおよびタスク

次のテンプレートおよび基本的なタスクは、プロジェクト経費カテゴリを Project Service Automation から Finance and Operations へ同期するために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations)
- **プロジェクトのタスクの名前:** Finance and Operations にカテゴリを同期

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| トランザクション カテゴリ     | カテゴリに対する統合エンティティ |

### <a name="entity-flow"></a>エンティティのフロー

プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。 Finance and Operations に同期すると、Project Service Automation からの統合 ID により Finance and Operations のプロジェクト カテゴリが更新されます。

### <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。

> [!NOTE]
> マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

