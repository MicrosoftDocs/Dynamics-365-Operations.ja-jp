---
title: "プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト実績を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。

このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト実績を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

テンプレートは、Project Service Automation から Finance and Operations のステージング テーブルへ、トランザクションを同期します。 同期が完了した後、統合仕訳帳にステージング テーブルからインポートする必要があります。

> [!NOTE]
> プロジェクト実績の統合は、Dynamics 365 for Finance and Operations バージョン 8.01 で使用可能です。

> [!NOTE]
> Project Service Automation で時間や経費のトランザクションに対する消費税金額を入力する場合は、Project Service Automation の更新プログラム 7 をインストールする必要があります。 この更新プログラムがインストールされていない場合、税の実績は関連付けられている時間または経費の実績にリンクされず、Finance and Operations に同期されません。 詳細については、サポートにお問い合わせください。


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations のデータ フロー

Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト実績に関するデータ フローを有効にします。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>テンプレートおよびタスク

使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクは、Project Service Automation から Finance and Operations プロジェクト実績を同期させるために使用されます。

-  **データ統合でのテンプレートの名前:** プロジェクト実績 (Project Service Automation から Finance and Operations)

-  **プロジェクトのタスク名:** 
    - 実績 
    - トランザクション接続

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| 実績                         | プロジェクト実績の統合エンティティ                      |
| トランザクション接続         | プロジェクト トランザクション リレーションシップに対する統合エンティティ    |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト実績は Project Service Automation で管理され、プロジェクトの統合仕訳帳に対する Finance and Operations に同期されます。 既定の財務分析コードと転記設定に基づいて、会計が適用されます。

## <a name="preconditions"></a>事前条件

実績の同期を行う前に、Project Service Automation 統合パラメーターを設定し、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクションのカテゴリを同期する必要があります。

## <a name="power-query"></a>Power Query

プロジェクト実績テンプレートで Microsoft Power Query を使用して、以下を行う必要があります。
- Project Service Automation **トランザクション タイプ**を、Finance and Operations の正しい**トランザクション タイプ**に変換します。 プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートは、既にこの変換を定義しています。
- Project Service Automation **請求タイプ**を、Finance and Operations の正しい**請求タイプ**に変換します。 プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートは、既にこの変換を定義しています。 すると、請求タイプは Dynamics 365 for Project Service Automation 統合パラメーター フォームのコンフィギュレーションに基づいて、**明細行プロパティ**にマップされます。
- このテンプレートと同期する必要のある、特定の**組織単位のリソース**にフィルター処理します。
- **会社間時間または会社間経費の実績**を Finance and Operations に同期させると、Finance and Operations で**契約組織単位**を、正しい**法人**に変換する必要があります。 プロジェクト実績 (Project Service Automation から Finance and Operations) には、デモ データに基づいて定義された条件付き列があります。 正しい法人に最後に挿入された条件付き列を更新する必要があります。 これに失敗すると、統合エラーあるいは Finance and Operations にインポートされた無効な実績トランザクションが発生することがあります。
- **会社間時間または会社間経費の実績**が Finance and operations と同期されない場合、最後に挿入した条件付き列をテンプレートから削除する必要があります。 これに失敗すると、統合エラーあるいは Finance and Operations にインポートされた無効な実績トランザクションが発生することがあります。

### <a name="contract-organizational-unit"></a>契約組織単位
テンプレートの挿入された条件付き列を更新するには、**マップ**矢印をクリックしてマッピングを開きます。 高度なクエリおよびフィルタリングを選択して開きます。
- 既定の Microsoft Project 実績 (Project Service Automation から Finance and Operations) テンプレートを使用している場合、**適用されたステップ**セクションで**挿入された条件**を選択します。 **機能**入力で、**USSI** を統合して使用する**法人**の名前に置き換える必要があります。 **関数**入力に必要な追加条件を追加し、**USMF** から正しい**法人**へ、**他の**条件を更新します。
- 新しいテンプレートを作成する場合、会社間時間および会社間経費をサポートするためにこの列を追加する必要があります。 **条件付き列の追加**を選択し、列に LegalEntity などの名前を付けます。 msdyn_contractorganizationalunitid.msdyn_name が <organizational unit> である場合は列の条件を入力し、次に <enter the Legal entity> を行います。その他は null を表します。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![テンプレートのマッピング](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>ステージング テーブルからインポートする

ステージング テーブルの定期処理からのインポートは、Project Service Automation から Finance and Operations への実績の同期後に実行される必要があります。 この処理では、プロジェクト トランザクションがステージング テーブルから Project Service Automation 統合仕訳帳にインポートされ、会計が適用され、インポートされたトランザクションが転記されます。 この処理はバッチ モードで実行し、必要に応じて繰り返し実行されるバッチとして設定することをお勧めします。

## <a name="update-actuals"></a>実績の更新

次のテンプレートおよび基本的なタスクは Finance and Operations から Project Service Automation へ伝票番号とプロジェクト実績に転記した消費税を同期させるために使用されます。

-  **データ統合でのテンプレートの名前:** プロジェクト実績の更新 (Finance and Operations から Project Service Automation)
-  **プロジェクトのタスク名:** 
     - 実績 
     - TransactionConnections

## <a name="entity-set"></a>エンティティ セット

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| プロジェクト実績の統合エンティティ                         | 実績                           |
| プロジェクト トランザクション リレーションシップに対する統合エンティティ       | Transaction Connections           |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト実績は Project Service Automation で管理され、プロジェクトの統合仕訳帳に対する Finance and Operations に同期されます。 Finance and Operations に転記されると、Finance and Operations からの伝票番号によって、実績は Project Service Automation で更新されます。 Finance and Operations で消費税が追加された場合、PRoject Service Automation で新しい税実績が作成されます。

## <a name="power-query"></a>Power Query

プロジェクト実績更新テンプレートで Microsoft Power Query を使用して、以下を行う必要があります。
- Finance and Operations **トランザクション タイプ**を、Project Service Automation の正しい**トランザクション タイプ**に変換します。 プロジェクト実績更新 (Finance and Operations から Project Service Automation) テンプレートは、既にこの変換を定義しています。
- Finance and Operations **請求タイプ**を、Project Service Automation の正しい**請求タイプ**に変換します。 プロジェクト実績更新 (Finance and Operations から Project Service Automation) テンプレートは、既にこの変換を定義しています。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![テンプレートのマッピング](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




