---
title: 定期売買販売価格
description: 定期売買を作成すると、販売価格 (定期売買) フォームで作成した販売価格設定から販売価格が派生します。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560692"
---
# <a name="subscription-sales-prices"></a>定期売買販売価格   

[!include [banner](../includes/banner.md)]


定期売買を作成すると、**販売価格 (定期売買)** フォームで作成した販売価格設定から販売価格が派生します。

**販売価格 (定期売買)** フォームでは、特定の定期売買用の販売価格、または、より広範囲に適用される販売価格を作成できます。 定期売買に適用される販売価格については、定期売買と販売価格の期間コードと通貨が一致している必要があります。

定期売買と販売価格で期間コードと通貨が一致する場合は、定期売買販売価格が次の表の優先順位に従って選択されます。 表の空白セルは空白のフィールドを示し、X はトランザクションの生成元である定期売買の値と等しい値であることを示します。

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>優先順位</p></th>
<th><p><strong>カテゴリ</strong></p></th>
<th><p><strong>プロジェクト ID</strong></p></th>
<th><p><strong>定期売買</strong></p></th>
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


定期売買手数料を作成すると、詳細レベルが最も高い販売価格 (上の表を参照) が定期売買販売価格として選択されます。

## <a name="update-and-index-subscription-sales-prices"></a>定期売買販売価格の更新および指数化

定期売買販売価格を更新するには、基準価格または指数を更新します。 割合で更新するか、または新しい値に更新できます。

## <a name="subscription-fee-sales-prices"></a>定期売買手数料の販売価格

定期売買手数料を作成するときは、定期売買の販売価格設定に基づいて販売価格が決定されます。 その場合、定期売買価格設定の基準価格を使用するか、または指標化された販売価格を作成できます。

## <a name="example"></a>例

新しいプロジェクト 9030 に対し、EUR 500 の定期売買販売価格を設定するとします。 **販売価格 (定期売買)** フォームで、次の表に示すように、定期売買販売価格の明細行を作成します。

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>発効日</p></th>
<th><p>カテゴリ</p></th>
<th><p>プロジェクト</p></th>
<th><p>定期売買</p></th>
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


**カテゴリ**および**定期売買**フィールドが空白であることに注意してください。

次に、以下の定期売買を作成します。

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>サービスの定期売買</p></th>
<th><p>プロジェクト</p></th>
<th><p>定期売買グループ</p></th>
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


次に、定期売買グループ Sub1 内の両方の定期売買に定期売買手数料を作成します。

1.  **サービス管理** \> **設定** \> **サービスの定期売買** \> **定期売買グループ**の順にクリックします。

2.  **定期売買グループ**フォームで、**関数** \> **定期売買手数料の作成**をクリックします。

3.  **定期売買手数料の作成**フォームに、適切な情報を入力します。 詳細については、[定期売買手数料トランザクションの作成](create-subscription-fee-transactions.md)を参照してください。

販売価格 EUR 500 を持つ定期売買手数料は、次の表に示すように、両方の定期売買で作成されます。

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
<th><p>プロジェクト日付</p></th>
<th><p>サービスの定期売買</p></th>
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


その後、プロジェクト 9030 に対するカテゴリ SubCat1 の販売価格を指定するよう決定します。 したがって、プロジェクト 9030 および手数料カテゴリ SubCat1 の組み合わせに対して EUR 550 の販売価格を持つ、新しい販売価格明細行を作成します。 これで、次の図に示すように、プロジェクト 9030 の定期売買販売価格明細行が 2 行になります。

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>発効日</p></th>
<th><p>カテゴリ</p></th>
<th><p>プロジェクト</p></th>
<th><p>定期売買</p></th>
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


上記の手順を繰り返して、定期売買グループ Sub1 の両方の定期売買に定期売買手数料を作成します。 次の表に、定期売買グループに関連付けられる各定期売買に対して作成されたトランザクションを示します。

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
<th><p>プロジェクト日付</p></th>
<th><p>定期売買</p></th>
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


定期売買 00020\_135 に対する最初のトランザクションでは、特定のプロジェクトとカテゴリの組み合わせに対して設定された定期売買販売価格から、販売価格 EUR 550 が派生します。 定期売買 00021\_135 に対する 2 番目のトランザクションでは、プロジェクト 9030 とカテゴリ SubCat2 の組み合わせに対して価格が設定されていないため、販売価格 EUR 500 がプロジェクトの定期売買販売価格として使用されます。

## <a name="see-also"></a>参照

[定期売買販売価格の更新および指数化](update-and-index-subscription-sales-prices.md)

  


