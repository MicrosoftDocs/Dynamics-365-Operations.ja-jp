---
title: "オブジェクトの値を在庫にします。"
description: "この記事は、在庫オブジェクトの値の計算方法についての情報を提供します。"
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>オブジェクトの値を在庫にします。

この記事は、在庫オブジェクトの値の計算方法についての情報を提供します。 

いう名前の新しい機能は**現物数量**特定の在庫オブジェクトの値を表示できるようになります。 原価オブジェクトは、在庫会計が実行されるエンティティ レベルを表します。 原価オブジェクトの詳細については、「[原価オブジェクト](cost-object.md)」を参照してください。 特定の在庫金額を表示するには** **原価のオブジェクト**ページでは**現物数量。して、[]をクリックします。 ここで、オブジェクトの値を計算する方法です: 在庫オブジェクト。値は要されたオブジェクト。平均単位原価の×の在庫オブジェクト。在庫オブジェクトと原価のオブジェクトの値を計算する方法数量以下の例を表示します。 2 つの製品受領書イベントは、品目 A に登録されます。

-   製品の入荷1: 数量= 100、コンピュータ、金額は$1,000,00のサイト= 1、倉庫=11のバッチNO。 = B1
-   製品の入荷2: 数量= 50、コンピュータ、金額= $800.00のサイト= 1、倉庫=11のバッチNO。 = B2

次の表に、原価オブジェクトの計算結果を示します。 [**原価オブジェクト**] ページの結果を表示できます。

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>オブジェクト タイプ</th>
<th>品目番号</th>
<th>サービス拠点</th>
<th>件数</th>
<th>在庫単位</th>
<th>値</th>
<th>平均単位原価</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>原価オブジェクト</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>個数</td>
<td><p>$1800.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>

次の表に、在庫オブジェクトの計算結果を示します。 [**原価オブジェクト**] ページの [**現物数量**] をクリックすることにより、結果を表示できます。

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>オブジェクト タイプ</th>
<th>品目番号</th>
<th>サービス拠点</th>
<th>倉庫</th>
<th>バッチ番号</th>
<th>件数</th>
<th>在庫単位</th>
<th>値</th>
<th>平均単位原価</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>在庫オブジェクト</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>個数</td>
<td><p>$1200.00</p></td>
<td><p>$12.00</p></td>
</tr>
<tr class="even">
<td>在庫オブジェクト</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>個数</td>
<td><p>$600.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>参照
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[品目をMicrosoft Dynamics AXで、新しい機能と変更された] (/dynamics365/operations/dev-itpro/get-started/whatです-新しい変更) 


