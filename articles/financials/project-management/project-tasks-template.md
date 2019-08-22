---
title: プロジェクトタスクを Project Service Automation から Finance and Operations に直接同期します
description: このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト タスクを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7ea5036682ad5b61fe56acd20a591cccc01f2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838322"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>プロジェクトタスクを Project Service Automation から Finance and Operations に直接同期します

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト タスクを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE]
> - プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。
> - Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。 勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。
> - 実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0.1 以降で使用可能です。

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations のデータ フロー

Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト タスクに関するデータ フローを有効にします。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>テンプレートおよびタスク

テンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクは Project Service Automation から Finance and Operations プロジェクト タスクを同期させるために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクト タスク (Project Service Automation から Finance and Operations)
- **データ統合プロジェクトのタスク名:** プロジェクト タスク

プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| プロジェクト タスク              | プロジェクトタスクの統合エンティティ |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト タスクは Project Service Automation で管理され、プロジェクト活動として Finance and Operations に同期されます。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。

## <a name="power-query"></a>Power Query

この条件が満たされた場合、フィルター処理する Microsoft Power Query for Excel を使用する必要があります。

- プロジェクト タスク内のリソース特定のレコードがあります。

Power Query を使用する必要がある場合は、このガイドラインに従います。

- プロジェクト タスク (Project Service Automation から Finance and Operations) テンプレートには、**IsLineTask** から **False** のフィルターを設定することでプロジェクト タスクからのリソース特定レコードを除外する既定のフィルターがあります。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
