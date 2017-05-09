---
title: "給付金の適格性ポリシー"
description: "この記事は、だれに特定の給付金の受給資格があるのかを定義するのに役立つ給付金の適格性ポリシーに関する情報が提供されます。"
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 543e43df2ec70e6f6e884019bb1c65bf3661ff35
ms.openlocfilehash: 3f9ab358ecbe7a992341610184002dbd97a31a4d
ms.lasthandoff: 03/31/2017


---

# <a name="benefit-eligibility-policies"></a>給付金の適格性ポリシー

[!include[banner](includes/banner.md)]


このトピックは、だれに特定の給付金の受給資格があるのかを定義するのに役立つ給付金の適格性ポリシーに関する情報が提供されます。

給付金を作成する場合、どの従業員がどの給付金を利用できるかを決定します。 次の表では、特定の従業員が利用できる給付金の例を示します。

| 給付金          | 給付金を利用できる人 |
|------------------|---------------------------------|
| 健康保険 | 全従業員                   |
| 携帯電話     | 販売スタッフ、経営幹部         |
| 駐車許可証   | 経営幹部                      |

次のコンポーネントは、適格性ポリシーの作成に使用されます。

-   ポリシー ルール タイプ
-   給付金の適格性ポリシー

ポリシー ルール タイプは、特定のポリシー ルールを作成する際に使用するクエリ パラメーターを定義します。 ポリシー ルール タイプを作成した後、給付金の適格性ポリシーを作成できます。 ポリシーでは、1 つ以上の法人に適用される一連のルールを作成することができます。 各ポリシー内では、先に作成した給付金の適格性ポリシー ルール タイプを表示できます。 

ポリシー内のルールの範囲を定義します。 たとえば、「**経営幹部**」という名前の給付金の適格性ポリシー ルール タイプを作成する場合、そのポリシー内にどのようなルールがあるかを指定できます。 この例は、そのルールでは、「経営幹部」という言葉を含んだ肩書きがルールに含まれていることを示しています。 ルールのパラメーターまたはポリシーに含まれるルールを定義した後、給付金に特定のルールを割り当てることができます。

<a name="see-also"></a>参照
--------

[給付金プログラムの定義および管理](manage-benefit-program.md)




