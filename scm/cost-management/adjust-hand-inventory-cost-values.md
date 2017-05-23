---
title: "手持在庫原価価値の調整"
description: "[手持在庫の調整] ページを使用して、在庫決算プロセスの実行後に、手持在庫数量の原価価格を調整します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a62d8d453be096dda221415437e78c695f3e5cf7
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>手持在庫原価価値の調整

[!include[banner](../includes/banner.md)]


[手持在庫の調整] ページを使用して、在庫決算プロセスの実行後に、手持在庫数量の原価価格を調整します。

**手持在庫の調整**ページを使用すると、在庫決算プロセスの実行後に、手持在庫数量の原価価格を調整することができます。 **注記:** **手持在庫の調整**ページを開くには、**決算と調整**ページで、完了した在庫決算プロセスのレコードを選択し、[**調整**] &gt; [**手持在庫**] の順にクリックします。 **例:** 2 月に次のトランザクションが発生しました。

-   2 月 1 日: コスト USD 10.00、数量 2 の在庫財務入庫
-   2 月 5 日: コスト USD 13.00、数量 1 の在庫財務入庫
-   2 月 19 日: 移動平均コスト USD 11.00、数量 1 の在庫財務出庫

この品目には先入れ先出し (FIFO) 在庫モデルが設定され、2 月 28 日に在庫原価計算が実行されました。 USD 11.00 の財務出庫トランザクションは 2 月 1 日の財務入庫に対して決済され、USD 1.00 の調整が行われます。 この場合、次の在庫入庫に未処理の在庫数量が含まれることになります。

-   2 月 1 日: コスト USD 10.00、数量 1
-   2 月 5 日: コスト USD 13.00、数量 1

この 2 つの品目の原価を USD 15.00 に設定するには、手持在庫調整オプションを使用して、未処理の手持在庫数量を最後の在庫原価計算期間の時点で調整します。 **注記:** 手持在庫調整トランザクションの転記日は、最後の在庫原価計算の実行日になります。 この日付は変更できません。



