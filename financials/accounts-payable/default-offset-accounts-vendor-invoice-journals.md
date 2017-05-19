---
title: "仕入先請求仕訳帳および請求書承認仕訳帳の既定の相手勘定"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 68df43b9cd3940552daa2ba3473fdd015708e0c8
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>仕入先請求仕訳帳および請求書承認仕訳帳の既定の相手勘定

[!include[banner](../includes/banner.md)]




既定の相手勘定は、次の仕入先請求仕訳帳のページで使用されます:

-   請求仕訳帳
-   請求書承認仕訳帳

次の表を使用して、請求仕訳の既定の勘定を割り当てる場所を決定します。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>既定の勘定を設定する</th>
<th>既定の勘定が提供される場所</th>
<th>このオプションが処理に与える影響</th>
<th>このオプションを使用する状況</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>仕入先グループ</strong> – <strong>仕入先グループ</strong>ページから開くことができる<strong>既定の勘定の設定</strong>ページで、仕入先グループの既定の相手勘定を設定します 。</td>
<td><ul>
<li>仕入先</li>
<li>既定の勘定が仕入先勘定に対して指定されていない場合の仕入先グループ内の仕入先勘定の仕訳エントリ</li>
</ul></td>
<td>仕入先グループの既定の相手勘定は、<strong>既定の勘定の設定</strong>ページに仕入先の既定の相手勘定として表示されます。 <strong>すべての仕入先</strong>リスト ページから、このページを開くことができます。</td>
<td>同じ仕入先グループから繰り返し同種の物品に対して支払を行っている場合は、このオプションを使用します。</td>
</tr>
<tr class="even">
<td><strong>仕入先</strong> – <strong>仕入先</strong>ページから開くことができる<strong>既定の勘定の設定</strong>ページで、仕入先の既定の勘定を設定します 。</td>
<td>仕入先勘定の仕訳入力</td>
<td>仕入先勘定の既定の相手勘定は、仕入先勘定の仕訳入力の既定の相手勘定として表示されます。</td>
<td>同じ仕入先から繰り返し同種の物品に対して支払を行っている場合は、このオプションを使用します。</td>
</tr>
<tr class="odd">
<td><strong>仕訳帳名</strong> – は、<strong>仕訳帳名</strong>ページの仕訳帳の既定の相手勘定を設定します。 <strong>固定相手勘定</strong>オプションを選択します。 仕訳帳名の仕訳帳タイプが<strong>仕入帳</strong>または<strong>承認</strong>の場合は、仕訳帳名で既定の相手勘定を指定することができないことに注意してください。</td>
<td><ul>
<li>仕訳帳名を使用する仕訳帳のヘッダー</li>
<li>仕訳帳名を使用する仕訳帳の仕訳入力</li>
</ul></td>
<td><strong>仕訳帳名</strong>ページの<strong>固定相手勘定</strong>オプションがオンの場合、仕訳帳名の相手勘定は、仕入先または仕入先グループの既定の相手勘定を上書きします。</td>
<td>このオプションを使用すると、特定の勘定に請求する特定の原価および経費の仕訳帳を、仕入先や仕入先グループの所属先に関わらず、設定することができます。</td>
</tr>
<tr class="even">
<td><strong>仕訳帳名</strong> – は、<strong>仕訳帳名</strong>ページの仕訳帳の既定の相手勘定を設定します。 <strong>固定相手勘定</strong>オプションをオフにします。 仕訳帳名の仕訳帳タイプが<strong>仕入帳</strong>または<strong>承認</strong>の場合は、仕訳帳名で既定の相手勘定を指定することができないことに注意してください。</td>
<td><ul>
<li>仕訳帳ヘッダー</li>
<li>仕訳帳名を使用する仕訳帳の仕訳入力</li>
</ul></td>
<td>これらの既定のエントリは、仕訳帳ヘッダーのページで使用され、仕訳帳ヘッダー ページの相手勘定は仕訳帳伝票ページで既定のエントリとして使用されます。 <strong>仕訳帳名</strong>ページの既定の勘定は、既定の勘定が仕入先勘定に設定されていない場合にのみ使用されます。</td>
<td>このオプションを使用して、既定の仕入先相手勘定が割り当てられていないときに使用する既定の勘定を設定します。</td>
</tr>
<tr class="odd">
<td><strong>仕訳帳ヘッダー</strong> – 仕訳帳の既定の相手勘定を設定して、仕訳伝票ページの既定のエントリとして使用します。 仕訳帳名の仕訳帳タイプが<strong>仕入帳</strong>または<strong>承認</strong>の場合は、仕訳帳ヘッダーで既定の相手勘定を指定することができないことに注意してください。</td>
<td>仕訳帳の仕訳入力</td>
<td>仕訳帳の既定の相手勘定は、仕訳伝票ページの既定のエントリとして使用されます。</td>
<td>仕訳帳のほとんどのエントリに同じ相手勘定が存在する場合は、このオプションを使用するとデータ入力が速くなります。</td>
</tr>
</tbody>
</table>






