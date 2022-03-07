---
title: サブスクリプション販売価格
description: 定サブスクリプションを作成すると、販売価格 (サブスクリプション) フォームで作成した販売価格設定から販売価格が派生します。
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd63fc290263babafabd6e29441f008d0cf10e13
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569988"
---
# <a name="subscription-sales-prices"></a>サブスクリプション販売価格

[!include [banner](../includes/banner.md)]

サブスクリプションを作成すると、**販売価格 (サブスクリプション)** フォームで作成した販売価格設定から販売価格が派生します。

**販売価格 (サブスクリプション)** フォームでは、特定のサブスクリプション用の販売価格、または、より広範囲に適用される販売価格を作成できます。 サブスクリプションに適用される販売価格については、サブスクリプションと販売価格の期間コードと通貨が一致している必要があります。

サブスクリプションと販売価格で期間コードと通貨が一致する場合は、サブスクリプション販売価格が次の表の優先順位に従って選択されます。 表の空白セルは空白のフィールドを示し、X はトランザクションの生成元であるサブスクリプションの値と等しい値であることを示します。

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>優先順位</p></th>
<th><p><strong>カテゴリ</strong></p></th>
<th><p><strong>プロジェクト ID</strong></p></th>
<th><p><strong>サブスクリプション</strong></p></th>
<th><p><strong>販売通貨</strong></p></th>
<th><p><strong>期間コード</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>x</p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>x</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>x</p></td>
<td><p>x</p></td>
</tr>
</tbody>
</table>

サブスクリプション手数料を作成すると、詳細レベルが最も高い販売価格 (上の表を参照) がサブスクリプション販売価格として選択されます。

## <a name="update-and-index-subscription-sales-prices"></a>サブスクリプション販売価格の更新および指数化

サブスクリプション販売価格を更新するには、基準価格または指数を更新します。 割合で更新するか、または新しい値に更新できます。

## <a name="subscription-fee-sales-prices"></a>サブスクリプション手数料の販売価格

サブスクリプション手数料を作成するときは、サブスクリプションの販売価格設定に基づいて販売価格が決定されます。 その場合、サブスクリプション価格設定の基準価格を使用するか、または指標化された販売価格を作成できます。

## <a name="example"></a>例

新しいプロジェクト 9030 に対し、EUR 500 のサブスクリプション販売価格を設定するとします。 **販売価格 (サブスクリプション)** フォームで、次の表に示すように、サブスクリプション販売価格の明細行を作成します。

<table>
<colgroup>
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
<th><p>発効日</p></th>
<th><p>カテゴリ</p></th>
<th><p>プロジェクト</p></th>
<th><p>サブスクリプション</p></th>
<th><p>期間コード</p></th>
<th><p>販売通貨</p></th>
<th><p>販売価格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2006 - 08 - 28</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>月</p></td>
<td><p>EUR / EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


**カテゴリ** および **サブスクリプション** フィールドが空白であることに注意してください。

次に、以下のサブスクリプションを作成します。

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>サービス サブスクリプション</p></th>
<th><p>プロジェクト</p></th>
<th><p>サブスクリプション グループ</p></th>
<th><p>カテゴリ</p></th>
<th><p>通貨</p></th>
<th><p>期間コード</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p>EUR / EUR</p></td>
<td><p>毎月</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR / EUR</p></td>
<td><p>毎月</p></td>
</tr>
</tbody>
</table>


次に、サブスクリプション グループ Sub1 内の両方のサブスクリプションにサブスクリプション手数料を作成します。

1.  **サービス管理** \> **設定** \> **サービス サブスクリプション** \> **サブスクリプション グループ** の順にクリックします。

2.  **サブスクリプション グループ** フォームで、**関数** \> **サブスクリプション手数料の作成** をクリックします。

3.  **サブスクリプション手数料の作成** フォームに、適切な情報を入力します。 詳細については、[サブスクリプション手数料トランザクションの作成](create-subscription-fee-transactions.md)を参照してください。

販売価格 EUR 500 を持つサブスクリプション手数料は、次の表に示すように、両方のサブスクリプションで作成されます。

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
<th><p>プロジェクト日付</p></th>
<th><p>サービス サブスクリプション</p></th>
<th><p>プロジェクト</p></th>
<th><p>カテゴリ</p></th>
<th><p>開始日</p></th>
<th><p>終了日</p></th>
<th><p>販売通貨</p></th>
<th><p>販売価格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2006 - 08 - 28</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>2007 - 01 - 01</p></td>
<td><p>2007 - 03 - 31</p></td>
<td><p>EUR / EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>2006 - 08 - 28</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>2007 - 01 - 01</p></td>
<td><p>2007 - 03 - 31</p></td>
<td><p>EUR / EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


その後、プロジェクト 9030 に対するカテゴリ SubCat1 の販売価格を指定するよう決定します。 したがって、プロジェクト 9030 および手数料カテゴリ SubCat1 の組み合わせに対して EUR 550 の販売価格を持つ、新しい販売価格明細行を作成します。 これで、次の図に示すように、プロジェクト 9030 のサブスクリプション販売価格明細行が 2 行になります。

<table>
<colgroup>
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
<th><p>発効日</p></th>
<th><p>カテゴリ</p></th>
<th><p>プロジェクト</p></th>
<th><p>サブスクリプション</p></th>
<th><p>期間コード</p></th>
<th><p>通貨</p></th>
<th><p>販売価格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2007 - 08 - 28</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>月</p></td>
<td><p>EUR / EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>2007 - 08 - 28</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>月</p></td>
<td><p>EUR / EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>

上記の手順を繰り返して、サブスクリプション グループ Sub1 の両方のサブスクリプションにサブスクリプション手数料を作成します。 次の表に、サブスクリプション グループに関連付けられる各サブスクリプションに対して作成されたトランザクションを示します。

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
<th><p>プロジェクト日付</p></th>
<th><p>サブスクリプション</p></th>
<th><p>プロジェクト</p></th>
<th><p>カテゴリ</p></th>
<th><p>開始日</p></th>
<th><p>終了日</p></th>
<th><p>販売通貨</p></th>
<th><p>販売価格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2007 - 07 - 28</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>2008 - 01 - 01</p></td>
<td><p>2008 - 03 - 31</p></td>
<td><p>EUR / EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>2008 - 07 - 28</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>2008 - 01 - 01</p></td>
<td><p>2008 - 03 - 31</p></td>
<td><p>EUR / EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>

サブスクリプション 00020\_135 に対する最初のトランザクションでは、特定のプロジェクトとカテゴリの組み合わせに対して設定されたサブスクリプション販売価格から、販売価格 EUR 550 が派生します。 サブスクリプション 00021\_135 に対する 2 番目のトランザクションでは、プロジェクト 9030 とカテゴリ SubCat2 の組み合わせに対して価格が設定されていないため、販売価格 EUR 500 がプロジェクトのサブスクリプション販売価格として使用されます。

## <a name="see-also"></a>参照

[サブスクリプション販売価格の更新および指数化](update-and-index-subscription-sales-prices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
