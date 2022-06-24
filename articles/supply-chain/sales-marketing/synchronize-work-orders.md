---
title: Field Service から Supply Chain Management へのプロジェクトの作業指示書の同期
description: この記事では、Dynamics 365 Field Service から Dynamics 365 Supply Chain Management にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: Henrikan
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: a43a7f7e900205bdb23fb9a35ca1518369683a42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860496"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Field Service から Supply Chain Management へのプロジェクトの作業指示書の同期

[!include[banner](../includes/banner.md)]

この記事では、Dynamics 365 Field Service から Dynamics 365 Supply Chain Management にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Supply Chain Management および Field Service 間の業務プロセスの同期。](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

使用されている **ワーク オーダーとプロジェクト (Field Service から Supply Chain Management)** テンプレートは、**ワーク オーダー (Field Service から Supply Chain Management)** テンプレートに基づきます。 詳細については、[Field Service のワーク オーダーと Supply Chain Management の販売注文との同期](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order) を参照してください。

この記事では、2 つのテンプレートの相違のみについて説明します:
- **ワーク オーダーとプロジェクト (Field Service から Supply Chain Management)**
- **ワーク オーダー (Field Service から Supply Chain Management)**

主な違いは、このテンプレートには Field Service のワーク オーダーに割り当てられたプロジェクト番号のマッピングが含まれており、Supply Chain Management で作成された販売注文にはプロジェクト番号が含まれ、関連付けられているプロジェクトの請求が確実に行われるようにしていることです。 これに加え、テンプレートは高度なクエリおよびフィルター処理を使用します。

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

**データ統合でのテンプレートの名前:**

- ワーク オーダーとプロジェクト (Field Service から Supply Chain Management)

**データ統合プロジェクトのタスク名:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
**外部プロジェクト** フィールドが、ワーク オーダー エンティティに追加されました。 このフィールドはルックアップで、ワーク オーダーがプロジェクトにタグ付けられ、販売注文は Supply Chain Management 内のプロジェクトに関連付けられます。 **システム ステータス** がオープン – 処理中 (690,970,000) から上位のステータスへ変わった場合、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderHeader

[![データ統合のテンプレート マッピング、作業指示書とプロジェクト (Field Service から Supply Chain Management): WorkOrderHeader。](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderHeaderProject

[![データ統合のテンプレート マッピング、作業指示書とプロジェクト (Field Service から Supply Chain Management): WorkOrderHeaderProject。](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderProduct

[![データ統合のテンプレート マッピング、作業指示書とプロジェクト (Field Service から Supply Chain Management): WorkOrderProduct。](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderService

[![データ統合のテンプレート マッピング、作業指示書とプロジェクト (Field Service から Supply Chain Management): WorkOrderService。](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]