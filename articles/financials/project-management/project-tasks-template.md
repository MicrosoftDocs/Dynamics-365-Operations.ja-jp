---
title: "Project Service Automation からプロジェクト タスクを同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト タスクを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Project Service Automation からプロジェクト タスクを直接プロジェクト活動の Finance and Operations に同期します。

このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト タスクを同期させるために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE]
> プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations のデータ フロー

Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト タスクに関するデータ フローを有効にします。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>テンプレートおよびタスク

テンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクは Project Service Automation から Finance and Operations プロジェクト タスクを同期させるために使用されます。

-**データ統合のテンプレートの名前:** プロジェクト タスク (Project Service Automation から Finance and Operations) - **プロジェクトのタスクの名前:** プロジェクト タスク

プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。

## <a name="entity-set"></a>エンティティ セット

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| プロジェクト タスク                           | 統合エンティティのプロジェクト タスク。   |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト タスクは Project Service Automation で管理され、プロジェクト活動として Finance and Operations に同期されます。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。

## <a name="power-query"></a>Power Query

これらの条件が満たされた場合、フィルター処理する Microsoft Power Query を使用する必要があります。

- プロジェクト タスク内のリソース特定のレコードがあります。

Power Query を使用する必要がある場合は、これらのガイドラインに従います。

- プロジェクト タスク (Project Service Automation から Finance and Operations) テンプレートは、既定のフィルターに **IsLineTask** から **False** のフィルターを設定することでプロジェクト タスク内のリソース特定レコードを除外できます。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


