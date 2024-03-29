---
title: 下方修正日数の例
description: 下方修正日数の例です。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e588273244c88ffa208e88b66800dc7ce20d68
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674816"
---
# <a name="reduction-days-example"></a>下方修正日数の例

[!include [banner](../includes/banner.md)]

次の表に示すように、顧客のメンテナンス サブスクリプションのサブスクリプション トランザクションを作成しました。

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>開始日</p></th>
<th><p>終了日</p></th>
<th><p>サブスクリプション</p></th>
<th><p>サブスクリプション タイプ</p></th>
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

顧客から、2 日間 (3 月 10 日と 3 月 11 日) のサービスは不要だという報告が出されます。 そこで、これら 2 日分のサブスクリプションを削減することに合意します。

**下方修正日数** タイプの新しいトランザクションを、次の表に示すように作成します。

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>自</p></th>
<th><p>至</p></th>
<th><p>サブスクリプション</p></th>
<th><p>サブスクリプション タイプ</p></th>
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

20011 年 3 月のトランザクションが請求されるとき、販売価格 EUR 200 から EUR 12.90 が減算されます。 したがってサブスクリプション トランザクションの請求可能金額は EUR 187.10 となり、2 つのトランザクションは合計 EUR 187.10 で請求されます。

## <a name="see-also"></a>参照

[サブスクリプション手数料の日数の引き下げ](reduce-the-days-on-subscription-fees.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]