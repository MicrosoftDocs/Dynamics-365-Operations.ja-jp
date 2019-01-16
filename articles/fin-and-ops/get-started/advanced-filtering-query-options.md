---
title: "高度なフィルター処理とクエリ構文"
description: "この記事では、フィルター処理とクエリ オプションについて説明します。フィルター ウィンドウあるいはグリッド列ヘッダーのフィルター処理においてフィルター/並べ替えの編集ダイアログあるいは matches (一致) 演算子を使う時に利用できます。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 01a508e97721099f92b9167dfdfa1b9669b9341c
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="advanced-filtering-and-query-syntax"></a>高度なフィルター処理とクエリ構文

[!include [banner](../includes/banner.md)]

この記事では、フィルター処理とクエリ オプションについて説明します。フィルター ウィンドウあるいはグリッド列ヘッダーのフィルター処理においてフィルター/並べ替えの編集ダイアログあるいは **matches (一致)** 演算子を使う時に利用できます。

## <a name="advanced-query-syntax"></a>高度なクエリ構文

<table>
<thead>
<tr>
<th>構文</th>
<th>意味</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>値</em></td>
<td>入力値と等しい</td>
<td>検索する値を入力します。</td>
<td><strong>Smith</strong> と入力すると &quot;Smith&quot; が検出されます。</td>
</tr>
<tr>
<td>!<em>値</em> (感嘆符)</td>
<td>入力値と等しくない</td>
<td>感嘆符を入力し、次に除外する値を入力します。</td>
<td><strong>!Smith</strong> と入力すると &quot;Smith&quot; 以外のすべての値が検出されます。</td>
</tr>
<tr>
<td><em>入力開始値</em>..<em>入力終了値</em> (ピリオド 2 つ)</td>
<td>2 つのピリオドで区切られた 2 つの値の間</td>
<td>開始値、2 つのピリオド、終了値の順に入力します。</td>
<td><strong>1..10</strong> と入力すると、1 ～ 10 までのすべての値が検出されます。 ただし、文字列フィールドに <strong>A..C</strong> と入力すると、&quot;A&quot; および &quot;B&quot; で始まるすべての値と、値  &quot;C&quot; が検出されます。 たとえば、このクエリでは &quot;Ca&quot; が検出されません。 &quot;A<em>&quot; から &quot;C</em>&quot; までのすべての値を検出するには、<strong>A..D</strong>と入力します。</td>
</tr>
<tr>
<td>..<em>値</em> (2 つのピリオド)</td>
<td>入力値以下</td>
<td>2 つのピリオド、値の順に入力します。</td>
<td><strong>..1000</strong> と入力すると、1000 以下のすべての数値が検出されます (&quot;100&quot;、&quot;999.95&quot;、&quot;1,000&quot; など)。</td>
</tr>
<tr>
<td><em>値</em>.. (2 つのピリオド)</td>
<td>入力値以上</td>
<td>値、2 つのピリオドの順に入力します。</td>
<td><strong>1000..</strong> と入力すると、 1000 以上のすべての数値が検出されます (&quot;1,000&quot;、&quot;1,000.01&quot;、&quot;1,000,000&quot; など)。</td>
</tr>
<tr>
<td>&gt;<em>値</em> (大なり記号)</td>
<td>入力値より大きい</td>
<td>大なり記号 (<strong>&gt;</strong>)、値の順に入力します。</td>
<td><strong>&gt;1000</strong> と入力すると、&quot;1000.01&quot;、&quot;20,000&quot;、&quot;1,000,000&quot; など、1000 より大きい数値が検出されます。</td>
</tr>
<tr>
<td>&lt;<em>値</em> (小なり記号)</td>
<td>入力値より小さい</td>
<td>小なり記号 (<strong>&lt;</strong>)、値の順に入力します。</td>
<td><strong>&lt;1000</strong> と入力すると、&quot;999.99&quot;、&quot;1&quot;、&quot;-200&quot; など、1000 より小さい数値が検出されます。</td>
</tr>
<tr>
<td><em>値</em>* (アスタリスク)</td>
<td>入力値で始まる</td>
<td>開始値、アスタリスク (<strong>*</strong>) の順に入力します。</td>
<td><strong>S*</strong>では、&quot;S&quot; で始まるすべての文字列が検出されます (&quot;Stockholm&quot;、&quot;Sydney&quot;、&quot;San Francisco&quot; など)。</td>
</tr>
<tr>
<td>*<em>値</em> (アスタリスク)</td>
<td>入力値で終わる</td>
<td>アスタリスク、終了値の順に入力します。</td>
<td><strong>*east</strong>では、&quot;east&quot; で終了するすべての文字列が検出されます (&quot;Northeast&quot; や &quot;Southeast&quot; など)。</td>
</tr>
<tr>
<td>*<em>値</em>* (アスタリスク)</td>
<td>入力値を含む</td>
<td>アスタリスク、値、アスタリスクの順に入力します。</td>
<td><strong>*th*</strong>では、&quot;th&quot; を含むすべての文字列が検出されます (&quot;Northeast&quot; や &quot;Southeast&quot; など)。</td>
</tr>
<tr>
<td>? (疑問符)</td>
<td>不特定の文字を 1 つ以上含む</td>
<td>値内の不特定文字の位置に疑問符を入力します。</td>
<td><strong>Sm?th</strong> と入力すると、&quot;Smith&quot; や &quot;Smyth&quot; が検出されます。</td>
</tr>
<tr>
<td><em>値</em>,<em>値</em> (コンマ)</td>
<td>コンマで区切られた入力値と一致</td>
<td>すべての条件をコンマで区切って入力します。</td>
<td><strong>A、D、F、G</strong> と入力すると、&quot;A&quot;、&quot;D&quot;、&quot;F&quot; および &quot;G&quot; が検出されます。 <strong>10、20、30、100</strong> と入力すると、&quot;10、20、30、100&quot; が検出されます。</td>
</tr>
<tr>
<td>(<span class="code">SQL ステートメント</span>) (SQL ステートメントをかっこで囲む)</td>
<td>定義されたクエリと一致</td>
<td>クエリをかっこに囲まれた SQL ステートメントとして入力します。</td>
<td><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></td>
</tr>
<tr>
<td>選択した</td>
<td>今日の日付</td>
<td><strong>T</strong> を入力します</td>
<td><strong>T</strong> 今日の日付に一致します。</td>
</tr>
<tr>
<td>(methodName(パラメーター)) (<strong>SysQueryRangeUtil</strong> かっこに囲まれたメソッド)</td>
<td><strong>SysQueryRangeUtil</strong> メソッドのパラメーターで指定された値または値の範囲との照合</td>
<td>値または値の範囲を指定するパラメーターを持つ <strong>SysQueryRangeUtil</strong> メソッドを入力します。</td>
<td>
<ol>
<li><strong>売掛金勘定</strong> &gt; <strong>請求書</strong> &gt; <strong>未処理の顧客請求書</strong> の順にクリックします。</li>
<li>Ctrl+Shift+F3 を押して、<strong>照会</strong>ページを開きます。</li>
<li><strong>範囲</strong> タブで <strong>Add</strong> をクリックします。</li>
<li><strong>テーブル</strong> フィールドで、<strong>未処理の顧客トランザクション</strong>を選択します。</li>
<li><strong>フィールド</strong> フィールドで、<strong>期日</strong>を選択します。</li>
<li><strong>基準</strong>フィールドに、<strong>(yearRange(-2,0))</strong> と入力します。</li>
<li><strong>OK</strong> をクリックします。 リスト ページが更新され、入力した基準に一致する請求書を一覧表示します。 この例では、前の 2 年内が支払期限の請求書が一覧表示されます。</li>
</ol>
<strong>SysQueryRangeUtil</strong> の日付メソッドに関する詳細や例については、次のセクションの表を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>SysQueryRangeUtil メソッドを使用する詳細日付クエリ

<table>
<thead>
<tr>
<th>方式</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr>
<td>日 (_relativeDays=0)</td>
<td>セッション日付を基準として日付を検索します。 正の値は未来の日付を表し、負の値は過去の日付を表します。</td>
<td>
<ul>
<li><strong>明日</strong> – <strong>(Day(1))</strong> と入力します。</li>
<li><strong>今日</strong> – <strong>(Day(0))</strong> と入力します。</li>
<li><strong>昨日</strong> – <strong>(Day(-1))</strong> と入力します。</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>セッション日付を基準として日付範囲を検索します。 正の値は未来の日付を表し、負の値は過去の日付を表します。</td>
<td>
<ul>
<li><strong>最近 30 日</strong> – <strong>(DayRange(-30,0))</strong> と入力します。</li>
<li><strong>以前の 30 日および将来の 30 日</strong> – <strong>(DayRange(-30,30))</strong> と入力します。</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>相対指定の日付より後のすべての日付を検索します。</td>
<td>
<ul>
<li><strong>30日後以上</strong> – <strong>(GreaterThanDate(30))</strong>と入力します。</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>現在時間より後のすべての日時のエントリを検索します。</td>
<td>
<ul>
<li><strong>すべての将来の日時</strong> – <strong>(GreaterThanUtcNow())</strong> と入力します。</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>相対指定の日付より前のすべての日付を検索します。</td>
<td>
<ul>
<li><strong>今日から 7 日まで</strong> – <strong>(LessThanDate(7))</strong> と入力します。</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>現在時間より前のすべての日時のエントリを検索します。</td>
<td>
<ul>
<li><strong>すべての過去の日時</strong> – <strong>(LessThanUtcNow())</strong> と入力します。</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>現在の月を基準として、日付の範囲を検索します。</td>
<td>
<ul>
<li><strong>前の 2 か月</strong> – <strong>(MonthRange(-2,0))</strong> と入力します。</li>
<li><strong>次の 3 か月</strong> – <strong>(MonthRange(0,3))</strong> と入力します。</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>現在の年を基準として、日付の範囲を検索します。</td>
<td>
<ul>
<li><strong>来年</strong> – <strong>(YearRange(0, 1))</strong> と入力します。</li>
<li><strong>昨年</strong> – <strong>(YearRange(-1,0))</strong> と入力します。</li>
</ul>
</td>
</tr>
</tbody>
</table>

