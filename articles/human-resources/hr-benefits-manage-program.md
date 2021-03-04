---
title: 給付金プログラムの定義および管理
description: 人事管理は、給付金、控除、および組織が作業者に対して提供または処理する作業者の報酬プランを設定および管理するのに使用できる一連のツールを提供します。 この記事は、管理された給付金を設定する方法に関する情報を提供します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a7fe99d4982b8f35871b15e8049c39eb806e315c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419335"
---
# <a name="define-and-manage-a-benefits-program"></a>福利厚生プログラムの定義および管理

Human Resources は、組織が従業員に対して提供または処理する給付金、控除、および従業員の報酬プランを設定および管理するために使用できる一連のツールを提供します。 この記事は、設定と給付金を管理する方法の情報を提供します。

## <a name="benefit-setup"></a>Benefit の設定

作業者を給付金に登録する前に、各給付金の要素を作成する必要があります。 これらの要素は同様の給付金計画を組み合わせて、控除割合と計算の詳細などの既定の設定を定義します。 これらの設定の多くは、作業者が給付金に後で登録されたときに調整できます。 各給付金計画に対して、組織が複数の登録オプションを提供するか、作業者が計画への登録を免除できます。 

[![給付金プロセス フロー](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>給付金の要素

給付金の作成を開始し、作業者を登録する前に、給付金を構成する要素、つまり、タイプ、計画およびオプションを定義する必要があります。

-   **タイプ** – 医療または駐車料金など、固有の給付金計画の集合。
-   **計画** – 業者との契約による固有の給付金。
-   **オプション** – 従業員のみまたは従業員と配偶者/パートナーなどの補償範囲レベル。

視力または歯科などの各給付金のタイプごとに、組織は作業者に複数の計画を提供できます。 各計画ごとに、組織はさまざまなオプションを提供できます。 たとえば、作業者は年間の給与から、1 回 2 回または 3 回追加の定期生命保険の補充を購入できます。 計画とオプションの各組み合わせが、作業者が登録する給付金になります。 

[![給付金の図](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>適格性
さまざまな要因により、雇用主が提供する給付金のさまざまなタイプに対する作業者の適格性が決定します。 Dynamics 365 Human Resources を使用して給付金を作成すると、その給付金が適用される適格性のタイプを設定できます。 

すべての作業者が給付金を使用できるようにすることができます。 たとえば、一部の会社では、駐車許可証を付加給付としてすべての従業員に提供します。 この給付金を作成する場合、**すべての作業者が適格** である適格性として設定します。 

債権差し押さえ、および税徴収の処理などの他の給付金については、適格性は適用されません。 これらのタイプの給付金を作成する場合、**適格性処理のバイパス** として適格性を設定します。 

最後に、福利厚生の適格性はルールに基づいています。 たとえばある会社が、従業員に生命保険の給付金の 2 つのタイプを提供するとします。 経営幹部の従業員は、1 つの生命保険プランの適格性がありますが、他のすべてのフルタイム従業員は他の生命保険プランの適格性があります。 人事管理では、すべての経営幹部の従業員を検索する適格性ルール、また他のすべてのフルタイム従業員を検索する適格性ルールを作成でき、次に適切な給付金にそれらのルールを適用します。

## <a name="enrollment"></a>登録
組織が提供する給付金を作成し、適格性を決定した後に、作業者を給付金に登録します。 給付金に 1 人の作業者を登録する、または単一のプロセス中に 1 つまたは複数の給付金に多数の作業者を登録できます。 

場合によっては、組織は特定の給付金の提供を停止します。 この場合、給付金および登録されている作業者を更新する必要があります。 給付金有効期限一括設定により、給付金の有効期限とその給付金に登録している作業者の登録の有効期限両方を一括で変更することができます。 給付金に登録されている複数の作業者を選択し、それらの補償の終了日を変更することもできます。 

同様に、給付金の一括延長により、当初計画していた期間より長く給付金を提供すると決定した場合に、給付金およびその給付金に登録されている作業者両方の有効期限を同時に延長できます。




[!INCLUDE[footer-include](../includes/footer-banner.md)]