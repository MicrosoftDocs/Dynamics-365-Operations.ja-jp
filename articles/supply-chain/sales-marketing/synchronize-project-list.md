---
title: "Finance and Operations から Field Service へのプロジェクト リストの同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Finance and Operations から Field Service へのプロジェクト リストの同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートおよび基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトの同期を実行するために使用されます。

**データ統合でのテンプレートの名前:**
- プロジェクト (Finance and Operations から Field Service)

**データ統合プロジェクトのタスク名:**
- プロジェクト

プロジェクト リストの同期が処理される前に、次の同期タスクが必要です。
- 勘定 (Sales から Finance and Operations) 

## <a name="entity-set"></a>エンティティ セット
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | プロジェクト                |

## <a name="entity-flow"></a>エンティティのフロー
Finance and Operations にプロジェクトが作成されます。 処理中のプロジェクトと**プロジェクト タイプ**時間、原材料および**プロジェクト ステージ**は、プロジェクト番号、プロジェクト名、プロジェクト ステージおよび顧客口座情報を含め、Field Service の**外部プロジェクト** エンティティに同期されます。 **外部プロジェクト**のリストは、Field Service のワーク オーダーと Finance and Operations のプロジェクトをペアリングするために使用されます。
Field Service CRM ソリューション 外部プロジェクトは、Operations からすべてのプロジェクトを取得する新しいエンティティです。
外部プロジェクト フィールドが、ワーク オーダー エンティティに追加されました。 このフィールドはルックアップで、ワーク オーダーとプロジェクトのタグ付けを購入し、それから販売注文は Operations によりプロジェクトに関連付けられます。 システム ステータスがオープンに変わった場合 - 上位のステータスへの Progress(690,970,000) で、外部プロジェクト フィールドはロックされ、値の追加、削除、また変更はできなくなります。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定
### <a name="in-finance-and-operations"></a>Finance and Operations
データ エンティティ プロジェクトの変更追跡を有効化

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング


### <a name="projects-finance-and-operations-to-field-service-projects"></a>プロジェクト (Finance and Operations から Field Service): プロジェクト

[![データ統合のテンプレートのマッピング](./media/FSProject1.png)](./media/FSProject1.png)

