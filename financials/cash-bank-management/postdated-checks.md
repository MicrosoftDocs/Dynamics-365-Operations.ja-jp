---
title: "先日付小切手"
description: "この記事は、の日付を繰り下げられるにサポートに関する情報をチェックインするMicrosoft Dynamics 365を提供します。 先日付小切手とは、将来の日付で支払を履行または受け取るために発行される小切手です。 したがって、小切手は、特定の日付まで清算できません。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>先日付小切手

この記事は、の日付を繰り下げられるにサポートに関する情報をチェックインするMicrosoft Dynamics 365を提供します。 先日付小切手とは、将来の日付で支払を履行または受け取るために発行される小切手です。 したがって、小切手は、特定の日付まで清算できません。

、Microsoft Dynamics 365は、次の表に示すように、日付を繰り下げられるの完全な管理サイクルをチェックインする売掛金勘定または買掛金勘定の両方をサポートします。
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>シナリオ</th>
<th>細目</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>先日付小切手の設定</td>
<td>新しい支払方法を設定し、発行された小切手、受領済みの小切手および源泉徴収税の精算勘定の支払業務を指定します。</td>
</tr>
<tr class="even">
<td>仕入先からの先日付小切手を登録および転記</td>
<td>仕入先に発行した先日付小切手の詳細を登録します。 支払が転記されると、仕入先の職責を認識されますが、銀行口座は、クレジットではない。 代わりに、精算勘定がこの目的に使用されます。</td>
</tr>
<tr class="odd">
<td>顧客の先日付小切手の登録と転記</td>
<td>顧客から受け取った先日付小切手の詳細を登録します。 支払が転記されると、承認顧客は貸方ですが、銀行口座は、借方ではない。 代わりに、精算勘定がこの目的に使用されます。</td>
</tr>
<tr class="even">
<td>顧客または仕入先の交換によって日付を繰り下げられるチェックを登録および転記します。</td>
<td>
仕入先への、または顧客からの元の小切手が紛失または破損した場合、代替先日付小切手を発行することもできます。 小切手の詳細を登録するときに、元の小切手への参照を提示し、新しい小切手が元の小切手の代替であることを示します。 代替小切手の転記もできます。</td>
</tr>
<tr class="odd">
<td>顧客の先日付小切手を仕入先に転送</td>
<td>顧客から先日付小切手を受け取ったら、支払として仕入先にその小切手を転送できます。</td>
</tr>
<tr class="even">
<td>顧客または仕入先の先日付小切手を決済</td>
<td>小切手が最終的に満期になったとき、顧客または仕入先のつなぎ勘定に転記された先日付小切手を決済します。 小切手を決済すると、銀行が先に使用した精算勘定に対して最終的に借方または貸方となります。</td>
</tr>
<tr class="odd">
<td>仕入先の先日付小切手をキャンセル</td>
<td>転記された先日付小切手をこの場合、キャンセルできます: []チェックは銀行が返されます。
- チェックが間違っている請求書に適用されます。
- 現金払は、小切手に対して行われます。
</td>
</tr>
<tr class="even">
<td>先日付小切手の支払停止</td>
<td>仕入先に発行した先日付小切手に対する支払は、資金不足、仕入先との契約条件の変更、仕入先による欠陥品目の供給、または仕入先への品目の返品などの理由で停止することができます。 取り除かなかった小切手の支払のみ使用できます。</td>
</tr>
</tbody>
</table>





