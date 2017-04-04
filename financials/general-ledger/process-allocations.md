---
title: "配賦の処理"
description: "この記事では、Microsoft Dynamics 365に処理する予算の計画に使用できる配賦に関する情報を、オプション、示します。 配賦は、複数の勘定科目の組み合わせ全体で金額を配分するのに使用されます。 経費、または収益が正しい会計のオブジェクトに付けられることを保証します。"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 37f4df5d0b79208a8c565bc9101ddde193a6ef5b
ms.lasthandoff: 03/31/2017


---

# <a name="process-allocations"></a>配賦の処理

この記事では、Microsoft Dynamics 365に処理する予算の計画に使用できる配賦に関する情報を、オプション、示します。 配賦は、複数の勘定科目の組み合わせ全体で金額を配分するのに使用されます。 経費、または収益が正しい会計のオブジェクトに付けられることを保証します。

、Microsoft Dynamics 365がこのプロセスをサポートするために次の機能があります:

-   手動で会計配分に分割工程を使用するか、またはドキュメントに財務分析コードの既定のテンプレートを適用して、トランザクション金額を割り当てます。 詳細については、"会計配分[] (\accounts-payable\accounting-distributions.md) 
-   個別の主勘定で定義された配賦条件に基づいてトランザクション金額を自動的に割り当てます。 配賦勘定項目は、勘定項目がソースの勘定科目に定義した条件を満たす場合に、割合と相手方の勘定科目に基づいて仕訳帳ごとに生成されます。
-   元帳配賦ルールに基づいて元帳残高または固定金額を自動的に割り当てます。 元帳配賦ルールは、配賦仕訳帳を使用して定期的に処理されます。 

###  <a name="allocations-in-budget-planning"></a>予算計画での配賦

元帳配賦ルールは、予算計画に使用できます。 予算計画で元帳配賦ルールを使用するとき、配賦ルールは元帳と同じ動作をしますが、データ ソースと相手方のデータは予算計画から取得されます。 手動で予算計画に使用する元帳配賦ルールを選択できます。 また、ワークフロー プロセスの一部として実行される配賦スケジュールを使用できます。

> [!NOTE]
> 会社間元帳配賦ルールは予算計画には使用できません。




