---
title: 給付金の適格性ポリシー
description: この記事は、だれに特定の給付金の受給資格があるのかを定義するのに役立つ給付金の適格性ポリシーに関する情報が提供されます。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 87a080c47e34a3265afea6494ff1733dac5bc384
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053108"
---
# <a name="benefit-eligibility-policies"></a>給付金の適格性ポリシー

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事は、だれに特定の給付金の受給資格があるのかを定義するのに役立つ給付金の適格性ポリシーに関する情報が提供されます。

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

ポリシー内のルールの範囲を定義します。 たとえば、**経営幹部** という名前の給付金の適格性ポリシー ルール タイプを作成する場合、そのポリシー内にどのようなルールがあるかを指定できます。 この例は、そのルールでは、「経営幹部」という言葉を含んだ肩書きがルールに含まれていることを示しています。 ルールのパラメーターまたはポリシーに含まれるルールを定義した後、給付金に特定のルールを割り当てることができます。






[!INCLUDE[footer-include](../includes/footer-banner.md)]