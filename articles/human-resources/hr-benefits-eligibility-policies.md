---
title: 給付金の適格性ポリシー
description: この記事では、だれに特定の給付金の受給資格があるのかを定義する給付金の適格性ポリシーに関する情報を提供します。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f0b373679690715ddbc518e4df79b81dbb000059
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877777"
---
# <a name="benefit-eligibility-policies"></a>給付金の適格性ポリシー


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、だれに特定の給付金の受給資格があるのかを定義する給付金の適格性ポリシーに関する情報を提供します。

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
