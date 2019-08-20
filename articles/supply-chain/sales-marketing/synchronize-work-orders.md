---
title: Field Service から Finance and Operations へのワーク オーダーとプロジェクトの同期
description: このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843412"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Field Service から Finance and Operations へのワーク オーダーとプロジェクトの同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

使用されている**ワーク オーダーとプロジェクト (Field Service から Finance and Operations)** テンプレートは、**ワーク オーダー (Field Service から Finance and Operations)** テンプレートに基づきます。 詳細については、[Field Service のワーク オーダーと Finance and Operations の販売注文との同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order) を参照してください。

このトピックでは、2 つのテンプレートの相違のみについて説明します:
- **ワーク オーダーとプロジェクト (Field Service から Finance and Operations)**
- **ワーク オーダー (Field Service から Finance and Operations)**

主な違いは、このテンプレートには Field Service のワーク オーダーに割り当てられたプロジェクト番号のマッピングが含まれており、Finance and Operations で作成された販売注文にプロジェクト番号が含まれ、関連付けられているプロジェクトの請求が確実に行われるようにしていることです。 これに加え、テンプレートは高度なクエリおよびフィルター処理を使用します。

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

**データ統合でのテンプレートの名前:**

- ワーク オーダーとプロジェクト (Field Service から Finance and Operations)

**データ統合プロジェクトのタスク名:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
**外部プロジェクト** フィールドが、ワーク オーダー エンティティに追加されました。 このフィールドはルックアップで、ワーク オーダーとプロジェクトのタグ付けを購入し、それから販売注文は Finance and Operations によりプロジェクトに関連付けられます。 **システム ステータス**がオープンから変わった場合 - 上位のステータスへの Progress(690,970,000) で、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeader

[![データ統合のテンプレートのマッピング](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeaderProject

[![データ統合のテンプレートのマッピング](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderProduct

[![データ統合のテンプレートのマッピング](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderService

[![データ統合のテンプレートのマッピング](./media/FSWOP4.png)](./media/FSWOP4.png)
