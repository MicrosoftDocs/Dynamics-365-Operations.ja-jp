---
title: 顧客エイジング レポート
description: 顧客エイジング レポートには、日付間隔またはエイジング期間でソートされた顧客からの支払い残高が表示されます。
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecd8a402f5bc72cf503607b8b42b892749859639
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735206"
---
# <a name="customer-aging-report"></a>顧客エイジング レポート 

**顧客エイジング** レポートには、日付間隔またはエイジング期間でソートされた顧客からの支払い残高が表示されます。

このレポートを生成するとき、次の既定のパラメーターが表示されます。 これらのパラメーターを使用して、レポートに表示されるデータをフィルタリングできます。 詳細については、[コレクションの設定](set-up-collections.md) 参照してください。

<table>
<colgroup>
<col>
<col>
</colgroup>
<thead>
<tr class="header">
<th><p>フィールド</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>請求分類</strong></p></td>
<td><p>レポートに含める請求分類を 1 つ以上選択します。</p>
<div class="alert">

**注記:** このコントロールは、<STRONG>公的機関</STRONG>のコンフィギュレーション キーが選択されている場合にのみ使用できます。</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>請求分類のない取引を含める</strong></p></td>
<td><p>このチェック ボックスが選択された場合、請求分類が割り当てられていないすべてのトランザクションがレポートに表示されます。</p>
<div class="alert">

**注記:** このコントロールは、<STRONG>公的機関</STRONG>のコンフィギュレーション キーが選択されている場合にのみ使用できます。</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>エイジングの時点</strong></p></td>
<td><p>現在のエイジング バケットで使用される日付を入力します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>時点の残高</strong></p></td>
<td><p>表示する顧客残高の日付を入力します。 これは、トランザクションの締日とも呼ばれます。</p></td>
</tr>
<tr class="even">
<td><p><strong>開始日</strong></p></td>
<td><p>レポートに含める最初の期間間隔またはエイジング期間内の日付を入力します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>基準</strong></p></td>
<td><p>レポートの基準となる日付タイプを選択します。</p>
<ul>
<li><p><strong>トランザクションの日付</strong> – トランザクションの転記日付。 たとえば、これは、期限の計算の基礎となる請求日である場合もあります。</p></li>
<li><p><strong>期限</strong> – 支払条件に基づくトランザクションの期限。</p></li>
<li><p><strong>文書日付</strong> – 期限の計算基準であるユーザー定義の文書日付。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>エイジング期間の定義</strong></p></td>
<td><p>エイジング期間の定義を選択します。 エイジング期間の定義を選択した場合、<strong>サイクル間隔</strong>フィールドは使用されません。</p>
<p>エイジング期間が 6 を超えるエイジング期間の定義は、レポートの印刷に使用できません。</p>
<div class="alert">

**注記:** エイジング期間は、<STRONG>エイジング期間の定義</STRONG>ページで設定できます。</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>エイジング期間の説明を印刷</strong></p></td>
<td><p>レポートの各エイジング期間列の上部にエイジング期間の説明を含めるには、<strong>はい</strong>を選択します。 列ヘッダーのないレポートを印刷するには、<strong>いいえ</strong>を選択します。</p></td>
</tr>
<tr class="even">
<td><p><strong>間隔</strong></p></td>
<td><p>各期間の日数または月数を入力して、使用する期間を定義します。 たとえば、エイジング情報を週単位で表示させる場合は、このフィールドに 7 を入力し、<strong>日付/月</strong>フィールドで <strong>日付</strong>を選択します。</p>
<div class="alert">

**注記:** このフィールドに入力する情報は、エイジング期間の定義を選択しなかった場合にのみ使用されます。 それ以外の場合、印刷方向はエイジング期間の定義で定義されます。</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>日/月</strong></p></td>
<td><p><strong>サイクル間隔</strong>フィールドで期間を定義する際に使用する単位として、<strong>日付</strong>または<strong>月</strong>を選択します。</p></td>
</tr>
<tr class="even">
<td><p><strong>印刷方向</strong></p></td>
<td><p>残高を計算するかどうかを選択し、過去または将来の期間のエイジング レポートを印刷します。 日付は、フィールド<strong>での残高</strong>にて選択した日付を基準にして評価されます。 過去の期間の情報を表示する場合は、<strong>後方</strong>を選択します。 将来の期間の情報を表示する場合は、<strong>前方</strong>を選択します。</p>
<div class="alert">
  
<STRONG>注記:</STRONG> このフィールドに入力する情報は、エイジング期間の定義を選択しなかった場合にのみ使用されます。</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>細目</strong></p></td>
<td><p>レポートに表示される残高に含まれるトランザクションをリストするために選択します。</p></td>
</tr>
<tr class="even">
<td><p><strong>トランザクション通貨での金額を含める</strong></p></td>
<td><p>会計通貨の金額に加え、トランザクション通貨の金額を含めるために選択します。 このチェック ボックスが選択されていない場合、レポートの金額は会計通貨でのみ表示されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>マイナス残高</strong></p></td>
<td><p>残高がマイナスの顧客 ID を含めるために選択します。</p></td>
</tr>
<tr class="even">
<td><p><strong>残高がゼロの口座を除外します</strong></p></td>
<td><p>残高がゼロの顧客勘定を除外するために選択します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>支払状態</strong></p></td>
<td><p>決済されていない支払を表示するために選択します。 これらは、レポートの最初の列に表示されます。</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
