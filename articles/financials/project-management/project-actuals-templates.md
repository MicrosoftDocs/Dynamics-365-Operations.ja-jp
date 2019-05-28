---
title: プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。
description: このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト実績を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571103"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト実績を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。

テンプレートは、Project Service Automation から Finance and Operations のステージング テーブルへ、トランザクションを同期します。 同期が完了した後、ステージング テーブルから統合仕訳帳にデータをインポートするよう**指定する**必要があります。

> [!NOTE]
> - プロジェクト実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0.1 以降で使用可能です。
> - Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。 勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。
> - Finance and Operations 7.3.0 を使用し、Project Service Automation から手数料トランザクションを挿入する場合は、プロジェクト請求書にそれらの手数料を含めるために KB 4345320 をインストールする必要があります。
> - Project Service Automation で時間や経費のトランザクションに対する消費税金額を入力する場合は、Project Service Automation 更新プログラム 7 をインストールする必要があります。 それ以外の場合は、税の実績は関連付けられている時間または経費の実績にリンクされず、Finance and Operations に同期されません。 詳細については、サポートにお問い合わせください。

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations のデータ フロー

Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト実績に関するデータ フローを有効にします。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Project Service Automation からのプロジェクト実績

### <a name="template-and-tasks"></a>テンプレートおよびタスク

使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクは、Project Service Automation から Finance and Operations プロジェクト実績を同期させるために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクト実績 (Project Service Automation から Finance and Operations)
- **プロジェクトのタスク名:**

    - 実績
    - トランザクション接続

### <a name="entity-set"></a>エンティティ セット

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| 実績                    | プロジェクト実績の統合エンティティ                   |
| トランザクション接続    | プロジェクト トランザクション リレーションシップに対する統合エンティティ |

### <a name="entity-flow"></a>エンティティのフロー

プロジェクト実績は Project Service Automation で管理され、Finance and Operations のプロジェクトの統合仕訳帳に同期されます。 既定の財務分析コードと転記設定に基づいて、会計が適用されます。

### <a name="prerequisites"></a>前提条件

実績の同期を行う前に、Project Service Automation 統合パラメーターを設定し、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクションのカテゴリを同期する必要があります。

### <a name="power-query"></a>Power Query

プロジェクト実績テンプレートで、Microsoft Power Query for Excel を使用してこれらのタスクを完了する必要があります。

- Project Service Automation のトランザクション タイプを、Finance and Operations の正しいトランザクション タイプに変換します。 プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートでは、既にこの変換を定義しています。
- Project Service Automation の請求タイプを、Finance and Operations の正しい請求タイプに変換します。 プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートでは、既にこの変換を定義しています。 すると、請求タイプは **Project Service Automation の統合パラメーター**ページのコンフィギュレーションに基づいて、明細行プロパティにマップされます。
- このテンプレートと同期する必要のある、特定の組織単位のリソースにフィルター処理します。
- 会社間時間または会社間経費の実績を Finance and Operations に同期させると、Finance and Operations で契約組織単位を、正しい法人に変換する必要があります。 プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートでは、条件付き列がデモ データに基づいて定義されます。 正しい法人に最後に挿入された条件付き列を更新する必要があります。 それ以外の場合は、統合エラーが発生し、あるいは無効な実績トランザクションが Finance and Operations にインポートされることがあります。
- 会社間時間または会社間経費の実績が Finance and operations と同期されない場合、最後に挿入した条件付き列をテンプレートから削除する必要があります。 それ以外の場合は、統合エラーが発生し、あるいは無効な実績トランザクションが Finance and Operations にインポートされることがあります。

#### <a name="contract-organizational-unit"></a>契約組織単位
テンプレートの挿入された条件付き列を更新するには、**マップ**矢印をクリックしてマッピングを開きます。 **高度なクエリおよびフィルタリング**リンクを選択して Power Query を開きます。

- 既定のプロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートを使用している場合、Power Query で、**適用されたステップ**セクションから最後の**挿入された条件**を選択します。 **機能**入力で、**USSI** を統合で使用する必要がある法人の名前に置き換えます。 必要に応じて**関数**入力に追加条件を追加し、**USMF** から正しい法人へ**他の**条件を更新します。
- 新しいテンプレートを作成する場合、会社間時間および会社間経費をサポートするために列を追加する必要があります。 **条件付き列の追加**を選択し、列に **LegalEntity** などの名前を付けます。 **msdyn\_contractorganizationalunitid.msdyn\_name** が \<組織単位\>である場合は列の条件を入力してから、 \<法人を入力\>します。その他 null を表します。

### <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![テンプレートのマッピング](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Project Service Automation から統合後のステージング テーブルからのインポート

ステージング テーブルの定期処理からのインポートは、Project Service Automation から Finance and Operations への実績の同期後に実行される必要があります。 この処理では、プロジェクト トランザクションがステージング テーブルから Project Service Automation 統合仕訳帳にインポートされ、会計が適用され、インポートされたトランザクションが転記されます。 この処理はバッチ モードで実行し、必要に応じて繰り返し実行されるバッチとして設定することをお勧めします。

## <a name="update-actuals-from-finance-and-operations"></a>Finance and Operations からの実績の更新

### <a name="template-and-tasks"></a>テンプレートおよびタスク

次のテンプレートおよび基本的なタスクは Finance and Operations から Project Service Automation へ伝票番号とプロジェクト実績に転記した消費税を同期させるために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクト実績の更新 (Finance and Operations から Project Service Automation)
- **プロジェクトのタスク名:**

    - 実績 
    - TransactionConnections

### <a name="entity-set"></a>エンティティ セット

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| プロジェクト実績の統合エンティティ                   | 実績                    |
| プロジェクト トランザクション リレーションシップに対する統合エンティティ | Transaction Connections    |

### <a name="entity-flow"></a>エンティティのフロー

プロジェクト実績は Project Service Automation で管理され、Finance and Operations のプロジェクトの統合仕訳帳に同期されます。 Finance and Operations に実績が転記された後、Finance and Operations からの伝票番号によって、Project Service Automation で更新されます。 Finance and Operations で消費税が追加された場合、Project Service Automation で新しい税実績が作成されます。

### <a name="power-query"></a>Power Query

プロジェクト実績更新テンプレートで、Power Query を使用してこれらのタスクを完了する必要があります。

- Finance and Operations のトランザクション タイプを、Project Service Automation の正しいトランザクション タイプに変換します。 プロジェクト実績の更新 (Finance and Operations から Project Service Automation) テンプレートでは、既にこの変換を定義しています。
- Finance and Operations の請求タイプを、Project Service Automation の正しい請求タイプに変換します。 プロジェクト実績の更新 (Finance and Operations から Project Service Automation) テンプレートでは、既にこの変換を定義しています。

### <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![テンプレートのマッピング](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
