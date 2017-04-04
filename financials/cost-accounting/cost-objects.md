---
title: "原価オブジェクト分析コード"
description: "原価を分析する際、原価要素分析コードを使用して、原価がどこに流れるかを決定します。 原価オブジェクト分析コードを使用して、原価を割り当てる場所を決定します。 このトピックでは、原価オブジェクト分析コードについて説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 87c13e268ab8825e06095d24e03694cf0f271a63
ms.openlocfilehash: 6029fbc070c3d476bb0918b60f43c8c33e8e0bc6
ms.lasthandoff: 03/31/2017


---

# <a name="cost-object-dimensions"></a>原価オブジェクト分析コード

原価を分析する際、原価要素分析コードを使用して、原価がどこに流れるかを決定します。 原価オブジェクト分析コードを使用して、原価を割り当てる場所を決定します。 このトピックでは、原価オブジェクト分析コードについて説明します。

原価オブジェクトは、見積、原価の割り当て、または直接測定するオブジェクトのタイプがあります。 標準的な原価のオブジェクトには、製品、プロジェクト、リソース、部門、原価部門、および地理的領域が含まれます。 管理は、原価を定量化するのに原価オブジェクトを使用し、収益性分析を推進します。

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>原価オブジェクト分析コードと原価オブジェクト分析コード メンバー
原価オブジェクトは、*原価オブジェクト分析コード*として知られています。 原価オブジェクト分析コードが参照するエンティティを決定した後、個々の分析コード値を指定するか、またはそれらを他のソース システムから原価オブジェクトにインポートする必要があります。 これらの個別の分析コード値は*原価オブジェクト分析コード メンバ*と呼ばれます。 たとえば、原価オブジェクト分析コードとして原価部門として知られる財務分析コードを使用するとします。 個々の原価部門にどのように原価が流れるかを確認するには、原価オブジェクト分析コード メンバをインポートする必要があります。 この場合、原価オブジェクト分析コード メンバは、販売、生産、管理、地理的な場所などの実際の原価部門です。 次のスクリーン ショットは、原価オブジェクト分析コード メンバーとしての実際の原価部門である原価オブジェクト分析コードとしての原価部門の例を示しています。 

[![オブジェクト分析コード] (。/media/costオブジェクトdimensions.png) ] (。/media/costオブジェクトdimensions.png) 

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>データ コネクタを使用して原価オブジェクト分析コード メンバーをインポートする
原価オブジェクト分析コードメンバーのインポートを容易にするために、データ コネクタを使用して、原価オブジェクト分析コードとして使用するエンティティから値を取得します。 ビルド済のデータ コネクタ、または構築するカスタム データ コネクタを使用できます。


