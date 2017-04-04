---
title: "高度なフィルタとクエリ構文"
description: "この記事では、フィルタ処理とクエリ オプションについて説明します。[フィルタ/並べ替えの編集] ダイアログで、&quot;matches&quot; (一致) 演算子を使うときに利用できます。"
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>高度なフィルタとクエリ構文

この記事では、フィルタ処理とクエリ オプションについて説明します。[フィルタ/並べ替えの編集] ダイアログで、"matches" (一致) 演算子を使うときに利用できます。

<a name="advanced-query-syntax"></a>詳細なクエリの構文
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>構文</th>
<th>意味</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>値</em></td>
<td>入力値と等しい</td>
<td>検索する値を入力します。</td>
<td><strong>入力する</strong> 検索 &quot;する&quot;。</td>
</tr>
<tr class="even">
<td>。<em>値</em> (感嘆符) </td>
<td>入力値と等しくない</td>
<td>感嘆符を入力し、次に除外する値を入力します。</td>
<td><strong>。入力する</strong> Smithを除くすべての値が &quot;&quot;検出されます。</td>
</tr>
<tr class="odd">
<td><em>入力開始値</em>..<em>入力終了値</em> (ピリオド 2 つ)</td>
<td>2 つのピリオドで区切られた 2 つの値の間</td>
<td>開始値、2 つのピリオド、終了値の順に入力します。</td>
<td><strong>1..10</strong> すべての値1 ~ 10.の検出されます。 ただし、文字列] <strong>A.C</strong> フィールドで、AとサイトBから開始 &quot;します (&quot;&quot;&quot;C.にまったく同じ値は、&quot;この&quot;クエリCa.を見つけません値を &quot;すべて検索します。&quot; A*のC*に &quot;よって値を &quot;すべて検索する&quot;には、入力します <strong>A.D</strong>。</td>
</tr>
<tr class="even">
<td>..<em>値</em> (2 つのピリオド)</td>
<td>入力値以下</td>
<td>2 つのピリオド、値の順に入力します。</td>
<td><strong>。.1000</strong> 1000以下、100など、999.95で &quot;あり&quot;&quot;、1,000を&quot;参照 &quot;番号&quot;。</td>
</tr>
<tr class="odd">
<td><em>値</em>.. (2 つのピリオド)</td>
<td>入力値以上</td>
<td>値、2 つのピリオドの順に入力します。</td>
<td><strong>1000..</strong> 1000により大きい値)、1,000など、1,000.01 &quot;、&quot;1,000,000を&quot;参照 &quot;番号&quot;。</td>
</tr>
<tr class="even">
<td>&gt;<em>値</em> (符号を超える) </td>
<td>入力値より大きい</td>
<td>[より大きいの署名 (<strong>&gt;</strong>値) と入力します。</td>
<td><strong>&gt;1000</strong> 1000より大きい、1000.01など、20,000 &quot;、&quot;1,000,000を&quot;参照 &quot;番号&quot;。</td>
</tr>
<tr class="odd">
<td>&lt;<em>値</em> よりより記号 (-) </td>
<td>入力値より小さい</td>
<td>[アット マーク () と値より少ないを入力します。</td>
<td><strong>&lt;1000</strong> 期間1000、999.99など、1で &quot;あり&quot;&quot;、-200を&quot;参照 &quot;番号&quot;。</td>
</tr>
<tr class="even">
<td><em>値</em>アスタリスク (*) </td>
<td>入力値で始まる</td>
<td>[開始値、アスタリスクの順に入力します<strong>*</strong> ()。</td>
<td><strong>S*</strong> Stockholm、Sydney、&quot;サンフランシスコ&quot;など、複数 &quot;から&quot;開始&quot;する文字列が &quot;&quot;検出されます。</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>入力値で終わる</td>
<td>アスタリスク、終了値の順に入力します。</td>
<td><strong>*east</strong> Northeast " Southeast "など、East &quot;で&quot;終了 &quot;&quot; する文字列が &quot;&quot;検出されます。</td>
</tr>
<tr class="even">
<td>*<em>値</em>アスタリスク (*) </td>
<td>入力値を含む</td>
<td>アスタリスク、値、アスタリスクの順に入力します。</td>
<td><strong>*th*</strong> thを含むNortheast " &quot;Southeast&quot;の &quot;ような文字列が&quot;&quot;&quot;検出されます。</td>
</tr>
<tr class="odd">
<td>? (疑問符)</td>
<td>不特定の文字を 1 つ以上含む</td>
<td>値内の不特定文字の位置に疑問符を入力します。</td>
<td><strong>Smか。th</strong> 検索 &quot;する&quot; と &quot;"&quot;。</td>
</tr>
<tr class="even">
<td><em>値</em>,<em>値</em> (コンマ)</td>
<td>コンマで区切られた入力値と一致</td>
<td>すべての条件をコンマで区切って入力します。</td>
<td><strong>A、D、F (G</strong> 場所を検索 &quot;が&quot;A &quot;、&quot;D &quot;、&quot;および&quot;<strong>10、20、30、100</strong> F &quot;G.で検索 &quot;10、20、30、100&quot;。</td>
</tr>
<tr class="odd">
<td>(<span class="code">SQL ステートメント</span>) (SQL ステートメントをかっこで囲む)</td>
<td>定義されたクエリと一致</td>
<td>クエリをかっこに囲まれた SQL ステートメントとして入力します。</td>
<td><strong><span class="code"> (データ ソース。Fieldname。= &quot;A&quot;) </span></strong></td>
</tr>
<tr class="even">
<td>選択した</td>
<td>今日の日付</td>
<td>“<strong>T</strong>” を入力します</td>
<td><strong>T</strong> 今日の日付に一致します。</td>
</tr>
<tr class="odd">
<td>(methodName(パラメーター)) (<strong>SysQueryRangeUtil</strong> かっこに囲まれたメソッド)</td>
<td><strong>SysQueryRangeUtil</strong> メソッドのパラメーターで指定された値または値の範囲との照合</td>
<td>値または値の範囲を指定するパラメーターを持つ <strong>SysQueryRangeUtil</strong> メソッドを入力します。</td>
<td><ol>
<li>[ <strong>売掛金勘定</strong> &gt; <strong>請求</strong> &gt; <strong>顧客請求書を開きます</strong>。</li>
<li>Ctrl+Shift+F3 を押して、<strong>照会</strong>ページを開きます。</li>
<li><strong>範囲</strong> タブで <strong>Add</strong> をクリックします。</li>
<li><strong>テーブル</strong> フィールドで、<strong>未処理の顧客トランザクション</strong>を選択します。</li>
<li><strong>フィールド</strong> フィールドで、<strong>期日</strong>を選択します。</li>
<li><strong>基準</strong>フィールドに、「<strong>(yearRange(-2,0))</strong>」と入力します。</li>
<li>[<strong>OK</strong>] をクリックします リスト ページが更新され、入力した基準に一致する請求書を一覧表示します。 この例では、前の 2 年内が支払期限の請求書が一覧表示されます。</li>
</ol>
<strong>SysQueryRangeUtil</strong> の日付メソッドに関する詳細や例については、次のセクションの表を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>SysQueryRangeUtil メソッドを使用する詳細日付クエリ
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>方式</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>日 (_relativeDays=0)</td>
<td>セッション日付を基準として日付を検索します。 正の値は未来の日付を表し、負の値は過去の日付を表します。</td>
<td><ul>
<li><strong>明日</strong> – 「<strong>(Day(1))</strong>」と入力します。</li>
<li><strong>今日</strong> –「<strong>(Day(0))</strong>」と入力します。</li>
<li><strong>昨日</strong> – 「<strong>(Day(-1))</strong>」と入力します。</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>セッション日付を基準として日付範囲を検索します。 正の値は未来の日付を表し、負の値は過去の日付を表します。</td>
<td><ul>
<li><strong>最近 30 日</strong> – 「<strong>(DayRange(-30,0))</strong>」と入力します。</li>
<li><strong>以前の 30 日および将来の 30 日</strong> – 「<strong>(DayRange(-30,30))</strong>」と入力します。</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0) </td>
<td>相対指定の日付より後のすべての日付を検索します。</td>
<td><ul>
<li><strong>30日後以上</strong> – <strong>(GreaterThanDate(30))</strong>と入力します。</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>現在時間より後のすべての日時のエントリを検索します。</td>
<td><ul>
<li><strong>すべての将来の日時</strong> – 「<strong>(GreaterThanUtcNow())</strong>」と入力します。</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0) </td>
<td>相対指定の日付より前のすべての日付を検索します。</td>
<td><ul>
<li><strong>今日から 7 日まで</strong> –「<strong>(LessThanDate(7))</strong>」と入力します。</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>現在時間より前のすべての日時のエントリを検索します。</td>
<td><ul>
<li><strong>すべての過去の日時</strong> – 「<strong>(LessThanUtcNow())</strong>」と入力します。</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>現在の月を基準として、日付の範囲を検索します。</td>
<td><ul>
<li><strong>前の 2 か月</strong> – 「<strong>(MonthRange(-2,0))</strong>」と入力します。</li>
<li><strong>次の 3 か月</strong> –「<strong>(MonthRange(0,3))</strong>」と入力します。</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>現在の年を基準として、日付の範囲を検索します。</td>
<td><ul>
<li><strong>来年</strong> –「<strong>(YearRange(0, 1))</strong>」と入力します。</li>
<li><strong>昨年</strong> –「<strong>(YearRange(-1,0))</strong>」と入力します。</li>
</ul></td>
</tr>
</tbody>
</table>




