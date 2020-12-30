---
title: 下方修正日数の例
description: 下方修正日数の例です。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431707"
---
# <a name="reduction-days-example"></a>下方修正日数の例 

[!include [banner](../includes/banner.md)]


次の表に示すように、顧客のメンテナンス定期売買の定期売買トランザクションを作成しました。

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>開始日</p></th>
<th><p>終了日</p></th>
<th><p>定期売買</p></th>
<th><p>定期売買タイプ</p></th>
<th><p>プロジェクト</p></th>
<th><p>カテゴリ</p></th>
<th><p>販売通貨</p></th>
<th><p>販売価格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011 年 3 月 1 日</p></td>
<td><p>2011 年 3 月 31 日</p></td>
<td><p>NR-2</p></td>
<td><p><strong>通常</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR / EUR</p></td>
<td><p>200.00</p></td>
</tr>
</tbody>
</table>


顧客から、2 日間 (3 月 10 日と 3 月 11 日) のサービスは不要だという報告が出されます。 そこで、これら 2 日分の定期売買を削減することに合意します。

**下方修正日数** タイプの新しいトランザクションを、次の表に示すように作成します。

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>自</p></th>
<th><p>至</p></th>
<th><p>定期売買</p></th>
<th><p>定期売買タイプ</p></th>
<th><p>プロジェクト</p></th>
<th><p>カテゴリ</p></th>
<th><p>販売通貨</p></th>
<th><p>販売価格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011 年 3 月 10 日</p></td>
<td><p>2011 年 3 月 11 日</p></td>
<td><p>NR-2</p></td>
<td><p><strong>下方修正日数</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR / EUR</p></td>
<td><p>-12.90</p></td>
</tr>
</tbody>
</table>


20011 年 3 月のトランザクションが請求されるとき、販売価格 EUR 200 から EUR 12.90 が減算されます。 したがって定期売買トランザクションの請求可能金額は EUR 187.10 となり、2 つのトランザクションは合計 EUR 187.10 で請求されます。

## <a name="see-also"></a>参照

[定期売買手数料の日数の引き下げ](reduce-the-days-on-subscription-fees.md)

  


