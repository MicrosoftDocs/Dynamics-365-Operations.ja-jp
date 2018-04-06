---
title: "プロジェクトの発注書"
description: "この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。 発注書を作成する方法は、発注書の目的、購入する品目の消費時期、プロジェクトに請求される時期で決まります。"
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: dae65394a2180ccbf3317a41b635ba97034e541b
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="purchase-orders-for-a-project"></a>プロジェクトの発注書

[!include[banner](../includes/banner.md)]


この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。 発注書を作成する方法は、発注書の目的、購入する品目の消費時期、プロジェクトに請求される時期で決まります。

Microsoft Dynamics 365 for Finance and Operations では、プロジェクトの発注書を作成する場合、複数の方法を使用できます。 発注書を作成する方法は、発注書の目的、購入する品目の消費時期、プロジェクトに請求される時期で決まります。

### <a name="methods-for-creating-a-purchase-order"></a>発注書を作成する方法

プロジェクト管理と会計で発注書を作成するには、次の方法のうち 1 つを使用できます。 発注書の目的は、発注書が消費される時点、つまり品目がプロジェクトで請求される時点を決定することです。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>方式</th>
<th>目的</th>
<th>品目の消費</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>プロジェクトからの発注書を直接作成します。</td>
<td>プロジェクトでの消費用に外部仕入先から品目を購買するには、この方法を使用します。 発注書を次の 2 つの方法で作成できます。
<ul>
<li>プロジェクト自体から作成します。 この場合、プロジェクトはすでに発注書のために定義されています。</li>
<li>プロジェクト発注書に移動することで作成します。 発注書の作成対象となる仕入先とプロジェクトを両方とも選択する必要があります。</li>
</ul></td>
<td>品目は、仕入先請求書が更新された時点で消費されます。</td>
</tr>
<tr class="even">
<td>販売注文から発注書を作成する。</td>
<td>プロジェクトから販売注文を作成する際に品目を購買する場合は、この方法を使用します。</td>
<td>品目は、販売注文が顧客に請求された時点で消費されます。</td>
</tr>
<tr class="odd">
<td>在庫品目要求から発注書を作成する。</td>
<td>プロジェクトから在庫品目要求を作成する際に品目を購買する場合は、この方法を使用します。</td>
<td>品目は、在庫品目要求梱包明細が更新された時点で消費されます。</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> 仕入先請求書または梱包明細を更新するときに、在庫品目要求の梱包明細を更新するように求めるメッセージが表示されます。

詳細については、「[在庫品目要求から発注書の品目を受け取る](tasks/receive-items-purchase-order-item-requirement.md)」を参照してください。


