---
title: 高度なフィルター処理とクエリ構文
description: このトピックでは、フィルター処理とクエリ オプションについて説明します。フィルター ウィンドウあるいはグリッド列ヘッダーのフィルター処理においてフィルター/並べ替えの編集ダイアログあるいは matches (一致) 演算子を使う時に利用できます。
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 650f1c209b1797973634c788645a4659bff28f13
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798674"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="7e5f3-103">高度なフィルター処理とクエリ構文</span><span class="sxs-lookup"><span data-stu-id="7e5f3-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e5f3-104">このトピックでは、フィルター処理とクエリ オプションについて説明します。フィルター ウィンドウあるいはグリッド列ヘッダーのフィルター処理においてフィルター/並べ替えの編集ダイアログあるいは **一致** 演算子を使う時に利用できます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="7e5f3-105">高度なクエリ構文</span><span class="sxs-lookup"><span data-stu-id="7e5f3-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7e5f3-106">構文</span><span class="sxs-lookup"><span data-stu-id="7e5f3-106">Syntax</span></span></th>
<th><span data-ttu-id="7e5f3-107">意味</span><span class="sxs-lookup"><span data-stu-id="7e5f3-107">Character description</span></span></th>
<th><span data-ttu-id="7e5f3-108">説明</span><span class="sxs-lookup"><span data-stu-id="7e5f3-108">Description</span></span></th>
<th><span data-ttu-id="7e5f3-109">例</span><span class="sxs-lookup"><span data-stu-id="7e5f3-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7e5f3-110"><em>値</em></span><span class="sxs-lookup"><span data-stu-id="7e5f3-110"><em>value</em></span></span></td>
<td><span data-ttu-id="7e5f3-111">入力値と等しい</span><span class="sxs-lookup"><span data-stu-id="7e5f3-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-112">検索する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="7e5f3-113"><strong>Smith</strong> と入力すると &quot;Smith&quot; が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-114">!<em>値</em> (感嘆符)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="7e5f3-115">入力値と等しくない</span><span class="sxs-lookup"><span data-stu-id="7e5f3-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-116">感嘆符を入力し、次に除外する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="7e5f3-117"><strong>!Smith</strong> と入力すると &quot;Smith&quot; 以外のすべての値が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-118"><em>入力開始値</em>..<em>入力終了値</em> (ピリオド 2 つ)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="7e5f3-119">2 つのピリオドで区切られた 2 つの値の間</span><span class="sxs-lookup"><span data-stu-id="7e5f3-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="7e5f3-120">開始値、2 つのピリオド、終了値の順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="7e5f3-121"><strong>1..10</strong> と入力すると、1 ～ 10 までのすべての値が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="7e5f3-122">ただし、文字列フィールドに <strong>A..C</strong> と入力すると、&quot;A&quot; および &quot;B&quot; で始まるすべての値と、値  &quot;C&quot; が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="7e5f3-123">たとえば、このクエリでは &quot;Ca&quot; が検出されません。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="7e5f3-124">&quot;A<em>&quot; から &quot;C</em>&quot; までのすべての値を検出するには、<strong>A..D</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-125">..<em>値</em> (2 つのピリオド)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="7e5f3-126">入力値以下</span><span class="sxs-lookup"><span data-stu-id="7e5f3-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-127">2 つのピリオド、値の順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="7e5f3-128"><strong>..1000</strong> と入力すると、1000 以下のすべての数値が検出されます (&quot;100&quot;、&quot;999.95&quot;、&quot;1,000&quot; など)。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-129"><em>値</em>..</span><span class="sxs-lookup"><span data-stu-id="7e5f3-129"><em>value</em>..</span></span> <span data-ttu-id="7e5f3-130">(2 つのピリオド)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-130">(double period)</span></span></td>
<td><span data-ttu-id="7e5f3-131">入力値以上</span><span class="sxs-lookup"><span data-stu-id="7e5f3-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-132">値、2 つのピリオドの順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="7e5f3-133"><strong>1000..</strong> と入力すると、</span><span class="sxs-lookup"><span data-stu-id="7e5f3-133"><strong>1000..</strong></span></span> <span data-ttu-id="7e5f3-134">1000 以上のすべての数値が検出されます (&quot;1,000&quot;、&quot;1,000.01&quot;、&quot;1,000,000&quot; など)。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-135">&gt;<em>値</em> (大なり記号)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="7e5f3-136">入力値より大きい</span><span class="sxs-lookup"><span data-stu-id="7e5f3-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-137">大なり記号 (<strong>&gt;</strong>)、値の順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="7e5f3-138"><strong>&gt;1000</strong> と入力すると、&quot;1000.01&quot;、&quot;20,000&quot;、&quot;1,000,000&quot; など、1000 より大きい数値が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-139">&lt;<em>値</em> (小なり記号)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="7e5f3-140">入力値より小さい</span><span class="sxs-lookup"><span data-stu-id="7e5f3-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-141">小なり記号 (<strong>&lt;</strong>)、値の順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="7e5f3-142"><strong>&lt;1000</strong> と入力すると、&quot;999.99&quot;、&quot;1&quot;、&quot;-200&quot; など、1000 より小さい数値が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-143"><em>値</em>\* (アスタリスク)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="7e5f3-144">入力値で始まる</span><span class="sxs-lookup"><span data-stu-id="7e5f3-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-145">開始値、アスタリスク (<strong>\*</strong>) の順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="7e5f3-146"><strong>S\*</strong>では、&quot;S&quot; で始まるすべての文字列が検出されます (&quot;Stockholm&quot;、&quot;Sydney&quot;、&quot;San Francisco&quot; など)。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-147">\*<em>値</em> (アスタリスク)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="7e5f3-148">入力値で終わる</span><span class="sxs-lookup"><span data-stu-id="7e5f3-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-149">アスタリスク、終了値の順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="7e5f3-150"><strong>\*east</strong>では、&quot;east&quot; で終了するすべての文字列が検出されます (&quot;Northeast&quot; や &quot;Southeast&quot; など)。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-151">*<em>値</em>* (アスタリスク)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="7e5f3-152">入力値を含む</span><span class="sxs-lookup"><span data-stu-id="7e5f3-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="7e5f3-153">アスタリスク、値、アスタリスクの順に入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="7e5f3-154"><strong>*th*</strong>では、&quot;th&quot; を含むすべての文字列が検出されます (&quot;Northeast&quot; や &quot;Southeast&quot; など)。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-155">?</span><span class="sxs-lookup"><span data-stu-id="7e5f3-155">?</span></span> <span data-ttu-id="7e5f3-156">(疑問符)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-156">(question mark)</span></span></td>
<td><span data-ttu-id="7e5f3-157">不特定の文字を 1 つ以上含む</span><span class="sxs-lookup"><span data-stu-id="7e5f3-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="7e5f3-158">値内の不特定文字の位置に疑問符を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="7e5f3-159"><strong>Sm?th</strong> と入力すると、&quot;Smith&quot; や &quot;Smyth&quot; が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-160"><em>値</em>,<em>値</em> (コンマ)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="7e5f3-161">コンマで区切られた入力値と一致</span><span class="sxs-lookup"><span data-stu-id="7e5f3-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="7e5f3-162">すべての条件をコンマで区切って入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="7e5f3-163"><strong>A、D、F、G</strong> と入力すると、&quot;A&quot;、&quot;D&quot;、&quot;F&quot; および &quot;G&quot; が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="7e5f3-164"><strong>10、20、30、100</strong> と入力すると、&quot;10、20、30、100&quot; が検出されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-165">"" (2 つの二重引用符)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="7e5f3-166">空白の値との照合</span><span class="sxs-lookup"><span data-stu-id="7e5f3-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="7e5f3-167">このフィールドの空白値をフィルター処理する 2 つの連続する二重引用符を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="7e5f3-168">2 つの連続した二重引用符 (<strong>""</strong>) は、現在の列に対する値のない行を検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-169">(<span class="code">Finance and Operationsクエリ</span>) (Finance and Operations かっこ間のクエリ)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="7e5f3-170">定義されたクエリと一致</span><span class="sxs-lookup"><span data-stu-id="7e5f3-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="7e5f3-171">Finance and Operations クエリ言語を使用して、かっこの間にクエリを SQL ステートメントとして入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="7e5f3-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="7e5f3-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="7e5f3-173">ルート データソースのフィールドと別のデータソースのフィールドのフィルター条件の構文の例として (すべての顧客ページ用)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-174">T</span><span class="sxs-lookup"><span data-stu-id="7e5f3-174">T</span></span></td>
<td><span data-ttu-id="7e5f3-175">今日の日付</span><span class="sxs-lookup"><span data-stu-id="7e5f3-175">Today's date</span></span></td>
<td><span data-ttu-id="7e5f3-176"><strong>T</strong> を入力します</span><span class="sxs-lookup"><span data-stu-id="7e5f3-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="7e5f3-177"><strong>T</strong> 今日の日付に一致します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-178">(methodName(パラメーター)) (<strong>SysQueryRangeUtil</strong> かっこに囲まれたメソッド)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="7e5f3-179"><strong>SysQueryRangeUtil</strong> メソッドのパラメーターで指定された値または値の範囲との照合</span><span class="sxs-lookup"><span data-stu-id="7e5f3-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="7e5f3-180">値または値の範囲を指定するパラメーターを持つ <strong>SysQueryRangeUtil</strong> メソッドを入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7e5f3-181"><strong>売掛金勘定</strong> &gt; <strong>請求書</strong> &gt; <strong>未処理の顧客請求書</strong> の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-182">Ctrl+Shift+F3 を押して、<strong>照会</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="7e5f3-183"><strong>範囲</strong> タブで <strong>Add</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-184"><strong>テーブル</strong> フィールドで、<strong>未処理の顧客トランザクション</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-185"><strong>フィールド</strong> フィールドで、<strong>期日</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-186"><strong>基準</strong>フィールドに、<strong>(yearRange(-2,0))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-187"><strong>OK</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="7e5f3-188">リスト ページが更新され、入力した基準に一致する請求書を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="7e5f3-189">この例では、前の 2 年内が支払期限の請求書が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="7e5f3-190"><strong>SysQueryRangeUtil</strong> の日付メソッドに関する詳細や例については、次のセクションの表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="7e5f3-191">SysQueryRangeUtil メソッドを使用する詳細日付クエリ</span><span class="sxs-lookup"><span data-stu-id="7e5f3-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7e5f3-192">方式</span><span class="sxs-lookup"><span data-stu-id="7e5f3-192">Method</span></span></th>
<th><span data-ttu-id="7e5f3-193">説明</span><span class="sxs-lookup"><span data-stu-id="7e5f3-193">Description</span></span></th>
<th><span data-ttu-id="7e5f3-194">例</span><span class="sxs-lookup"><span data-stu-id="7e5f3-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7e5f3-195">日 (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="7e5f3-196">セッション日付を基準として日付を検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-196">Find a date relative to the session date.</span></span> <span data-ttu-id="7e5f3-197">正の値は未来の日付を表し、負の値は過去の日付を表します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-198"><strong>明日</strong> – <strong>(Day(1))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-199"><strong>今日</strong> – <strong>(Day(0))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-200"><strong>昨日</strong> – <strong>(Day(-1))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="7e5f3-202">セッション日付を基準として日付範囲を検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="7e5f3-203">正の値は未来の日付を表し、負の値は過去の日付を表します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-204"><strong>最近 30 日</strong> – <strong>(DayRange(-30,0))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-205"><strong>以前の 30 日および将来の 30 日</strong> – <strong>(DayRange(-30,30))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="7e5f3-207">相対指定の日付より後のすべての日付を検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-208"><strong>30日後以上</strong> – <strong>(GreaterThanDate(30))</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="7e5f3-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="7e5f3-210">現在時間より後のすべての日時のエントリを検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-211"><strong>すべての将来の日時</strong> – <strong>(GreaterThanUtcNow())</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="7e5f3-213">相対指定の日付より前のすべての日付を検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-214"><strong>今日から 7 日まで</strong> – <strong>(LessThanDate(7))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="7e5f3-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="7e5f3-216">現在時間より前のすべての日時のエントリを検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-217"><strong>すべての過去の日時</strong> – <strong>(LessThanUtcNow())</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="7e5f3-219">現在の月を基準として、日付の範囲を検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-220"><strong>前の 2 か月</strong> – <strong>(MonthRange(-2,0))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-221"><strong>次の 3 か月</strong> – <strong>(MonthRange(0,3))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7e5f3-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="7e5f3-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="7e5f3-223">現在の年を基準として、日付の範囲を検索します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7e5f3-224"><strong>来年</strong> – <strong>(YearRange(0, 1))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="7e5f3-225"><strong>昨年</strong> – <strong>(YearRange(-1,0))</strong> と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e5f3-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
