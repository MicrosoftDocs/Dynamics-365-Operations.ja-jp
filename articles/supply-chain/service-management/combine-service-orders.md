---
title: サービス注文の組み合わせ
description: サービス注文を組み合わせることができます。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f89c60561746ac9f1c2e9d611089bfac69089081
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676778"
---
# <a name="combine-service-orders"></a>サービス注文の組み合わせ   

[!include [banner](../includes/banner.md)]


**サービス合意** フォームでサービス注文明細行を自動的に作成する場合、次のいずれかのオプションを選択してそれらをグループ化する方法を指定できます。

  - **サービス契約別**

  - **サービス作業別**

  - **従業員別**

  - **サービス対象別**

## <a name="example"></a>例

開始日が 2007 年 3 月 31 日のサービス合意を作成します。 **サービス注文の組み合わせ** フィールドで、**サービス対象別** を指定します。 その後、次のサービス合意項目を作成します。

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
<th><p>契約明細行番号</p></th>
<th><p>トランザクション タイプ</p></th>
<th><p>説明</p></th>
<th><p>間隔</p></th>
<th><p>サービス対象</p></th>
<th><p>入社日</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>時</strong></p></td>
<td><p>SAL1</p></td>
<td><p>毎週</p></td>
<td><p>X-1</p></td>
<td><p>2007 - 04 - 01</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>時</strong></p></td>
<td><p>SAL2</p></td>
<td><p>隔週</p></td>
<td><p>X-2</p></td>
<td><p>2007 - 04 - 01</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>時</strong></p></td>
<td><p>SAL3</p></td>
<td><p>毎週</p></td>
<td><p>X-2</p></td>
<td><p>2007 - 04 - 01</p></td>
</tr>
</tbody>
</table>


どのサービス合意項目でも時間枠は指定しません。 したがって、サービス注文明細行は、該当する算出日から移動しません。

次に、**サービス注文の作成** フォームで 2007 年 4 月 1 日から 2007 年 4 月 30 日までのサービス注文明細行を生成します。

合計で 10 件のサービス注文が作成されます。 選択した組み合わせの設定が **サービス対象別** であるため、作成されるすべてのサービス注文の明細行が、1 つの特定のサービス対象を含むサービス注文明細行のみになります。 サービス合意から生成され、同じサービス日付と対象を含むサービス注文明細行が、同じサービス注文に組み合わせられます。


> [!NOTE]
> <P>この例では、<STRONG>サービス管理パラメーター</STRONG>フォームで指定されたカレンダーに休業日がないものとします。</P>



サービス注文明細行をさらにサービス注文にグループ化する場合は、サービス合意項目に対して指定する時間枠に基づきます。

## <a name="see-also"></a>参照

[サービス注文の自動作成](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]