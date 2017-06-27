---
title: "勘定と分析コードの組み合わせの入力 (セグメント化されたエントリのコントロール)"
description: "この記事は、勘定と分析コードの組み合わせまたは勘定科目を入力する方法について説明します。 入力経験は、多くの場合、セグメント化されたエントリのコントロールと呼ばれます。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1535ef5c5eec1389272ce8fd2c2c183f532785b1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a>勘定と分析コードの組み合わせの入力 (セグメント化されたエントリのコントロール)

[!include[banner](../includes/banner.md)]


この記事は、勘定と分析コードの組み合わせまたは勘定科目を入力する方法について説明します。 入力経験は、多くの場合、セグメント化されたエントリのコントロールと呼ばれます。

ユーザーは、一般仕訳帳、予算作成、および転記の定義などのさまざまなページで、勘定と分析コードの組み合わせを入力します。 有効な勘定と分析コードの組み合わせは、元帳に割り当てられた勘定構造と勘定構造に割り当てられた詳細ルールによって異なります。 組み合わせを入力するときに、手動で値を入力するか、または豊富なルックアップ エクスペリエンスを使用できます。 フィールドを入力するときに、入力し始めると、値と説明を検索できます。 たとえば、「180」と入力すると、その番号の組み合わせで始まるすべての値を検索します。 または、「Cash」と入力すれば、「Cash」で始まるすべての説明を持つ値を検索します。 \*Cash や \*180 などのワイルドカードを使用すると、値や説明に検索基準が含まれているかどうか検索することもできます。 

次の表に、ルックアップが閉じているときに使用できるキーボード ショートカットを示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>キーボード ショートカット</th>
<th>アクション</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alt + 下方向キー</td>
<td>ルックアップを開きます。 2 回目に Alt + 下方向キーを押した場合、フォーカスがポップアップのセグメントに移動します。</td>
</tr>
<tr class="even">
<td><ul>
<li>Enter キーおよび Shift + Enter キー</li>
<li>勘定科目表の区切り記号</li>
<li>右方向キーおよび左方向キー</li>
</ul></td>
<td>前後のセグメントへ移動します。</td>
</tr>
<tr class="odd">
<td>タブ</td>
<td>グリッド内で次のフィールドに移動します。</td>
</tr>
</tbody>
</table>

次の表に、ルックアップが開いているときに使用できるキーボード ショートカットを示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>キーボード ショートカット</th>
<th>アクション</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Esc キー</td>
<td>ルックアップを閉じます。</td>
</tr>
<tr class="even">
<td><ul>
<li>上方向キーおよび下方向キー</li>
<li>Page Up キーおよび Page Down キー</li>
<li>Home キーおよび End キー</li>
</ul></td>
<td>一覧での前後の値、値の前後のグループ、またはルックアップの最初または最後の要素に移動します。</td>
</tr>
<tr class="odd">
<td><ul>
<li>勘定科目表の区切り記号</li>
<li>右方向キーおよび左方向キー</li>
</ul></td>
<td>前後のセグメントへ移動します。</td>
</tr>
<tr class="even">
<td>タブ</td>
<td>グリッド内で次のフィールドに移動します。</td>
</tr>
<tr class="odd">
<td>Alt + W キー</td>
<td>[<strong>すべて表示l</strong>] と [<strong>有効なものを表示</strong>] を切り替えます。</td>
</tr>
</tbody>
</table>

 




