---
title: 在庫オブジェクトの値
description: この記事は、在庫オブジェクトの値の計算方法についての情報を提供します。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daa36dad4009cc25b89363dcff6b4496205522e3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981490"
---
# <a name="inventory-object-values"></a>在庫オブジェクトの値

[!include [banner](../includes/banner.md)]

この記事は、在庫オブジェクトの値の計算方法についての情報を提供します。 

**現物数量** という名前の新しい機能は、特定の在庫オブジェクトの値を表示できます。 

原価オブジェクトは、在庫会計が実行されるエンティティ レベルを表します。 原価オブジェクトの詳細については、「[原価オブジェクト](cost-object.md)」を参照してください。 

特定の在庫オブジェクトの値を表示するには、**原価のオブジェクト** ページで **現物数量** をクリックします。 在庫オブジェクトの値がどのように計算されるかは次のとおりです。 

在庫オブジェクト . 値 = コスト オブジェクト . 平均単位コスト × 在庫オブジェクト . 数量 

次の例では、在庫オブジェクトとコスト オブジェクトの値の計算方法を示します。 2 つの製品受領書イベントは、品目 A に登録されます。

-   製品受領書 1 : 数量 = 100 個、金額 = $1,000.00、サイト = 1、倉庫 =11、バッチ番号。 = B1
-   製品受領書 2 : 数量 = 50 個、金額 = $800.00、サイト = 1、倉庫 =11、バッチ番号。 = B2

次の表に、原価オブジェクトの計算結果を示します。 **原価オブジェクト** ページの結果を表示できます。

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

次の表に、在庫オブジェクトの計算結果を示します。 **原価オブジェクト** ページの **現物数量** をクリックすることにより、結果を表示できます。

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



<a name="additional-resources"></a>その他のリソース
--------

[原価オブジェクト](cost-object.md)

[原価エントリ](cost-entries.md)

[新機能および変更された機能](../../fin-and-ops/get-started/whats-new-changed.md)



