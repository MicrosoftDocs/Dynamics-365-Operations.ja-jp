---
title: 監査ポリシー ルール
description: 経費精算書、仕入先請求書、および発注書が、作成したポリシー ルールに準拠しているかどうか評価するには、監査ポリシーを使用できます。 監査ポリシーに関連付けられているすべてのルールが、指定したスケジュールに従ってバッチ モードで実行されます。  各ポリシー ルールは、ポリシー ルール タイプのインスタンスです。 各ポリシー ルール タイプに対して、一度に 1 つのポリシー ルールだけ有効にできます。
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de6406029aa88424863dd9a47505f5b3ad27f237
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445146"
---
# <a name="audit-policy-rules"></a>監査ポリシー ルール

[!include [banner](../includes/banner.md)]

経費精算書、仕入先請求書、および発注書が、作成したポリシー ルールに準拠しているかどうか評価するには、監査ポリシーを使用できます。 監査ポリシーに関連付けられているすべてのルールが、指定したスケジュールに従ってバッチ モードで実行されます。  各ポリシー ルールは、ポリシー ルール タイプのインスタンスです。 各ポリシー ルール タイプに対して、一度に 1 つのポリシー ルールだけ有効にできます。 

<a name="queries-and-query-types"></a>クエリおよびクエリ タイプ
-----------------------

監査ポリシー ルールを作成する場合は、最初にポリシー ルール タイプを選択します。 ポリシー ルール タイプは、ポリシー ルールを作成するための開始点として使用するアプリケーション オブジェクト ツリー (AOT) のクエリを指定します。 また、ポリシー ルールに使用するクエリ タイプを指定します。 クエリは、ポリシー ルールが評価する元伝票を決定します。 また、法人および日付の両方を識別する元伝票のフィールド指定して、監査するドキュメントを選択する際に使用します。 クエリ タイプは、クエリ ページと監査ポリシー ルール ページの既定のフィールドを制御します。 次の表に、監査ポリシー ルールに使用できるクエリ タイプを示します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>クエリ タイプ</th>
<th>目的</th>
<th>詳細</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>条件付</td>
<td>指定した値に対して元伝票属性を評価します。</td>
<td></td>
</tr>
<tr class="even">
<td>集計</td>
<td>数値の集計によるポリシー ルールに対して複数の元伝票または元伝票明細行を評価します。</td>
<td></td>
</tr>
<tr class="odd">
<td>サンプリング</td>
<td>元伝票から指定した割合をランダムに選択して、ポリシー違反について評価します。</td>
<td>このオプションを選択する際、監査ポリシー ルール ページを使用して、監査のためにランダムに選択するドキュメントの割合を指定します。</td>
</tr>
<tr class="even">
<td>複製</td>
<td>指定したフィールドに重複するエントリが含まれているかどうかを決定するために、元伝票を評価します。</td>
<td>このオプションを選択する際、監査ポリシー ルール ページを使用して、ドキュメントが重複するエントリを評価するときに、ドキュメント選択の日付範囲の開始に追加する日数を指定します。</td>
</tr>
<tr class="odd">
<td>リスト検索</td>
<td>特定のエンティティの元伝票を評価します。</td>
<td>クエリのルート ドキュメントは、監査するドキュメントを定義します。 クエリは dirpartytable テーブルへの参照が含まれるリストのクエリである必要があります。 このオプションは、次の AOT のクエリでのみ使用できます。
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (経費精算書が監視対象の従業員)</li>
<li><span class="ui">AuditPolicyPurchList</span> (発注書が監視対象の仕入先)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (仕入先請求書によって監視する仕入先)</li>
</ul>
このオプションを選択する際、監査ポリシー ルール ページで監視対象のエンティティを指定します。</td>
</tr>
<tr class="even">
<td>キーワード検索</td>
<td>元伝票を評価して、特定の語を含んでいるかどうかを確認します。</td>
<td>このオプションを選択する際、監査ポリシー ルール ページで検索する語を入力します。 監査ポリシー ルール ページでは、入力した語について評価するテーブルおよびフィールドを指定できるオプションも含まれています。</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>共通パラメーター
特定の監査ポリシーのすべてのポリシー ルールは、同じバッチ パラメーターおよび同じドキュメント選択日付範囲を共有します。 ポリシーのこれらのパラメーターは、追加のオプション ページで指定されます。



<a name="additional-resources"></a>その他のリソース
--------

[監査ポリシー違反およびケース](audit-policy-violations-cases.md)
[元伝票の監査ポリシーの定義](tasks/define-audit-policies-source-documents.md)


