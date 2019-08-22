---
title: Finance and Operations から Field Service へのプロジェクト リストの同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843556"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Finance and Operations から Field Service へのプロジェクト リストの同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトの同期を実行するために使用されます。

**データ統合でのテンプレート**
- プロジェクト (Finance and Operations から Field Service)

**データ統合プロジェクトのタスク**
- プロジェクト

プロジェクト リストの同期が処理される前に、次の同期タスクが必要です。
- 勘定 (Sales から Finance and Operations) 

## <a name="entity-set"></a>エンティティ セット
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | プロジェクト                |

## <a name="entity-flow"></a>エンティティのフロー
Finance and Operations にプロジェクトが作成されます。 **プロジェクト タイプ**を**時間、原材料**に、および**プロジェクト ステージ**を**処理中**に設定されたプロジェクトは、プロジェクト番号、プロジェクト名、プロジェクト ステージおよび顧客口座情報を含め、Field Service の**外部プロジェクト** エンティティに同期されます。 **外部プロジェクト**のリストは、Field Service のワーク オーダーと Finance and Operations のプロジェクトをペアリングするために使用されます。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
**外部プロジェクト** エンティティは、Finance and Operations からすべてのプロジェクトを取得します。 **外部プロジェクト** フィールドが、**ワーク オーダー** エンティティに追加されました。 これはルックアップ フィールドであるため、ワーク オーダーがプロジェクトにタグ付けられ、販売注文は Finance and Operations によりプロジェクトに関連付けられます。 **システム ステータス**が**オープン – 処理中 (690,970,000)** から上位のステータスへ変更した後、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定
### <a name="finance-and-operations"></a>Finance and Operations
データ エンティティ プロジェクトの変更追跡を有効にします。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング


### <a name="projects-fin-and-ops-to-field-service-projects"></a>プロジェクト (Finance and Operations から Field Service): プロジェクト

[![データ統合のテンプレートのマッピング](./media/FSProject1.png)](./media/FSProject1.png)
