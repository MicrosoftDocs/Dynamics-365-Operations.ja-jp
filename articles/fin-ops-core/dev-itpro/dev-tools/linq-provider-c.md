---
title: C# の統合言語クエリ (LINQ) プロバイダー
description: このトピックでは、LINQ プロバイダーについて説明します。
author: pvillads
ms.date: 11/03/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26751
ms.assetid: 8bd10c93-9d5e-49d7-b20f-7f804e16e76c
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 494ec676902c908784b4b033d90c8440e6f92e22
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865892"
---
# <a name="language-integrated-query-linq-provider-for-c"></a><span data-ttu-id="d371f-103">C\# の統合言語クエリ (LINQ) プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d371f-103">Language Integrated Query (LINQ) provider for C\#</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d371f-104">このトピックでは、LINQ プロバイダーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d371f-104">This topic discusses the LINQ provider.</span></span>

<span data-ttu-id="d371f-105">LINQ (統合言語クエリ) は、さまざまな場所および形式で保存されているデータにアクセスできるクラスおよびメソッドのセットです。</span><span class="sxs-lookup"><span data-stu-id="d371f-105">LINQ (Language Integrated Query) is a set of classes and methods that enable you to access data that is stored in a variety of places and formats.</span></span> <span data-ttu-id="d371f-106">LINQ フレームワークは、マネージド言語のデータにアクセスするための標準です。</span><span class="sxs-lookup"><span data-stu-id="d371f-106">The LINQ framework is the standard for accessing data in managed languages.</span></span> <span data-ttu-id="d371f-107">LINQ は次のような異なる種類のデータ ソースからのデータへのアクセスに関する統合されて一貫した API をプログラマーに提示します。</span><span class="sxs-lookup"><span data-stu-id="d371f-107">LINQ presents to programmers a unified and consistent API for data access from heterogeneous data sources, such as:</span></span>

- <span data-ttu-id="d371f-108">メモリ内のオブジェクト グラフ</span><span class="sxs-lookup"><span data-stu-id="d371f-108">In-memory object graphs</span></span>
- <span data-ttu-id="d371f-109">Active Directory エントリ</span><span class="sxs-lookup"><span data-stu-id="d371f-109">Active Directory entries</span></span>
- <span data-ttu-id="d371f-110">Flickr 画像および XML</span><span class="sxs-lookup"><span data-stu-id="d371f-110">Flickr pictures and XML</span></span>
- <span data-ttu-id="d371f-111">SQL Server</span><span class="sxs-lookup"><span data-stu-id="d371f-111">SQL Server</span></span>

<span data-ttu-id="d371f-112">LINQ プロバイダーでは、.NET マネージド言語を使用して業務データにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d371f-112">The LINQ provider allows the user to access business data by using .NET managed languages.</span></span>

## <a name="two-syntactical-mechanisms-for-accessing-linq"></a><span data-ttu-id="d371f-113">LINQ にアクセスするための 2 つの構文メカニズム</span><span class="sxs-lookup"><span data-stu-id="d371f-113">Two syntactical mechanisms for accessing LINQ</span></span>

<span data-ttu-id="d371f-114">次のテーブルに示すように、LINQ を使用する構文的アプローチは 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="d371f-114">There are two syntactical approaches for using LINQ, as described in the following table.</span></span>

| <span data-ttu-id="d371f-115">アプローチ</span><span class="sxs-lookup"><span data-stu-id="d371f-115">Approach</span></span> | <span data-ttu-id="d371f-116">X++</span><span class="sxs-lookup"><span data-stu-id="d371f-116">X++</span></span> | <span data-ttu-id="d371f-117">C\# と Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d371f-117">C\# and Visual Basic</span></span> |
|-------------------------|------------------|---------------------------|
| <span data-ttu-id="d371f-118">標準メソッドの呼び出し構文による LINQ。</span><span class="sxs-lookup"><span data-stu-id="d371f-118">LINQ by standard method call syntax.</span></span> | <span data-ttu-id="d371f-119">実用的ではありません。</span><span class="sxs-lookup"><span data-stu-id="d371f-119">Impractical.</span></span> <span data-ttu-id="d371f-120">ジェネリックの言語サポートは、LINQ にとって重要で、X++ ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d371f-120">Language support for generics is vital for LINQ and is not supported in X++.</span></span> | <span data-ttu-id="d371f-121">必須のラムダ構文が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="d371f-121">Available, requires lambda syntax.</span></span> |
| <span data-ttu-id="d371f-122">コンパイラで認識される特殊な構文による LINQ。</span><span class="sxs-lookup"><span data-stu-id="d371f-122">LINQ by specialized syntax that is understood by the compiler.</span></span> | <span data-ttu-id="d371f-123">使用不可。</span><span class="sxs-lookup"><span data-stu-id="d371f-123">Not available.</span></span>   | <span data-ttu-id="d371f-124">簡単に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d371f-124">Available, easier to use.</span></span> |

<span data-ttu-id="d371f-125">C\# (または Visual Basic) の LINQ プロバイダーにアクセスするには、2 つの構文メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="d371f-125">There are two syntactic mechanisms for accessing the LINQ provider in C\# (or in Visual Basic):</span></span>

- <span data-ttu-id="d371f-126">標準、または流暢なメソッドの呼び出し構文。</span><span class="sxs-lookup"><span data-stu-id="d371f-126">By standard, or fluent, method call syntax.</span></span>
- <span data-ttu-id="d371f-127">特殊な構文により、C\# コンパイラは LINQ メソッド呼び出しと同等として理解できるように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="d371f-127">By specialized syntax that the C\# compiler has been enhanced to understand as equivalent to the LINQ method calls.</span></span> <span data-ttu-id="d371f-128">(このような構文は「構文砂糖」とも呼ばれます。)</span><span class="sxs-lookup"><span data-stu-id="d371f-128">(Such syntax is sometimes called “syntactic sugar”.)</span></span>

<span data-ttu-id="d371f-129">このトピックでは、簡単な特殊構文から始めて、LINQ の各構文メカニズムを検討します。</span><span class="sxs-lookup"><span data-stu-id="d371f-129">This topic is going to review each syntactic mechanism for LINQ, starting with the easier specialized syntax.</span></span>

## <a name="linq-by-specialized-syntax-in-c"></a><span data-ttu-id="d371f-130">C\# の特殊な構文による LINQ</span><span class="sxs-lookup"><span data-stu-id="d371f-130">LINQ by specialized syntax in C\#</span></span>

<span data-ttu-id="d371f-131">一部の .NET 言語は、書きやすい代替方法として LINQ 向けの特殊な構文を理解します。</span><span class="sxs-lookup"><span data-stu-id="d371f-131">Some .NET languages understand specialized syntax for LINQ as an alternative that is easier for us to write.</span></span> <span data-ttu-id="d371f-132">C\# はそのような言語の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="d371f-132">C\# is one such language.</span></span>

<span data-ttu-id="d371f-133">C\# で LINQ を使用するには、変数の宣言に使われる、C\# のキーワード **var** を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d371f-133">To use LINQ in C\#, you must understand the C\# keyword **var**, which is used to declare variables.</span></span> <span data-ttu-id="d371f-134">var キーワードは、変数に割り当てられているものによって変数のデータ型を把握するようにコンパイラに指示します。</span><span class="sxs-lookup"><span data-stu-id="d371f-134">The var keyword tells the compiler to figure out the data type of the variable by what is assigned to the variable.</span></span> <span data-ttu-id="d371f-135">この機能は、X++ でも利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="d371f-135">This feature is now also available in X++.</span></span> <span data-ttu-id="d371f-136">タイプはソース コード内に暗黙的に格納されており、コンパイルが完了した後にタイプは解決され、変更されません。</span><span class="sxs-lookup"><span data-stu-id="d371f-136">The type is implicit in the source code, and the type is settled and unvarying after the compilation completes.</span></span>

### <a name="comparing-x-to-c-linq"></a><span data-ttu-id="d371f-137">X++ to C\# LINQ の比較</span><span class="sxs-lookup"><span data-stu-id="d371f-137">Comparing X++ to C\# LINQ</span></span>

<span data-ttu-id="d371f-138">X++ 言語は、便利で使いやすい `while select` ステートメントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d371f-138">The X++ language supports the useful and easy to use `while select` statement.</span></span> <span data-ttu-id="d371f-139">これは、X++ `while select` 構文と特殊な C\#LINQ の構文を比較しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="d371f-139">This lest you compare the X++ `while select` syntax to the specialized C\# LINQ syntax.</span></span> <span data-ttu-id="d371f-140">最初に、これが X++ のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="d371f-140">First, here is the X++ sample.</span></span>

```xpp
CustTable ct;     // X++, traditional while select.
CustTrans trans;

while select * from ct
    where ct.AccountNum >= ‘4000’
    join RecId from trans
    where trans.RecId == ct.RecId
    order by ct.AccountNum desc
{
    print ct.AccountNum;
}
```

<span data-ttu-id="d371f-141">次は、特殊な LINQ 構文と同等の C\# のクエリです。</span><span class="sxs-lookup"><span data-stu-id="d371f-141">Next is an equivalent query in C\# with the specialized LINQ syntax.</span></span>

```csharp
// C#, with specialized LINQ syntax.
// Get access to the data provider:
var provider = new QueryProvider(null);

var customers = new QueryCollection(provider);
var customerTransactions = new QueryCollection(provider);

var query = from ct in customers
            from trans in customerTransactions
            where ct.AccountNum >= “4000”
            where trans.AccountNum == ct.AccountNum
            orderby ct.AccountNum descending
            select ct;

foreach (var ct in query)
{
    System.Console.WriteLine(ct.AccountNum);
}
```

## <a name="linq-query-in-c-by-method-syntax-using-the-lambda-operator-"></a><span data-ttu-id="d371f-142">メソッド構文による C\# の LINQ クエリでは、ラムダ演算子 > を使用します</span><span class="sxs-lookup"><span data-stu-id="d371f-142">LINQ query in C\# by method syntax, using the lambda operator ></span></span>

<span data-ttu-id="d371f-143">次は、C\# での LINQ の別の用途です。今回以外では、LINQ API を呼び出すためにより多くの標準構文が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d371f-143">Next is another use of LINQ in C\#, except this time the more standard syntax is used to call the LINQ API.</span></span> <span data-ttu-id="d371f-144">この方法では、ラムダ演算子 `>` を使用します。</span><span class="sxs-lookup"><span data-stu-id="d371f-144">The approach also involves use of the lambda operator `>`.</span></span> <span data-ttu-id="d371f-145">次の C\# クエリは、前述の C\# クエリと機能的に同等です。</span><span class="sxs-lookup"><span data-stu-id="d371f-145">The following C\# query is functionally equivalent to the preceding C\# query.</span></span>

```csharp
var query = customers
    .Where(c => string.Compare(c.AccountNum, "4000") >= 0)
    .Join(customers,
        primary => primary.AccountNum,
        foreign => foreign.AccountNum,
        (primary, foreign) => new { P = primary, F = foreign })
    .OrderBy(primaryAndForeign => primaryAndForeign.P.AccountNum)
    .Select(primaryAndForeign => primaryAndForeign.P);
```

<span data-ttu-id="d371f-146">X++ で使用されている `while select` 構文と C\# の特殊な LINQ 構文 (Visual Basic には特に優れた LINQ 構文があります) の間に良好な一致があります。</span><span class="sxs-lookup"><span data-stu-id="d371f-146">There's a good match between the `while select` syntax used in X++ and the specialized LINQ syntax in C\# (Visual Basic has particularly good LINQ syntax).</span></span> <span data-ttu-id="d371f-147">特殊な LINQ 構文は実際、結合を表現する際に有効ですが、C\# コンパイラに組み込まれた特殊な構文は Finance and Operations アプリケーションが提供する拡張機能を処理しません。</span><span class="sxs-lookup"><span data-stu-id="d371f-147">It's evident that the specialized LINQ syntax is actually very useful in expressing joins, but the specialized syntax built into the C\# compiler doesn't handle the extensions provided by the Finance and Operations applications.</span></span>

### <a name="limitation-of-the-specialized-linq-syntax"></a><span data-ttu-id="d371f-148">特殊な LINQ 構文の制限</span><span class="sxs-lookup"><span data-stu-id="d371f-148">Limitation of the specialized LINQ syntax</span></span>

<span data-ttu-id="d371f-149">LINQ プロバイダーへの拡張機能で拡張できない特殊な LINQ 構文の制限。</span><span class="sxs-lookup"><span data-stu-id="d371f-149">A limitation of the specialized LINQ syntax is that it can't be augmented with extensions to the LINQ provider.</span></span> <span data-ttu-id="d371f-150">対照的に、メソッド呼び出しとラムダ演算子の標準構文は必要に応じて拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d371f-150">In contrast, standard syntax of method calls plus the lambda operator can be extended as needed.</span></span> <span data-ttu-id="d371f-151">たとえば、LINQ フレームワークは、C\# で LINQ の特別な構文で表されない会社間のヒントに対するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="d371f-151">For instance, the LINQ framework provides a method for cross-company hints that can't be expressed in the special syntax for LINQ in C\#.</span></span> <span data-ttu-id="d371f-152">ただし、クエリを作成する能力のため、この制限は大きな問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="d371f-152">Fortunately, due to the ability to compose queries, this limitation need not be a major problem.</span></span> <span data-ttu-id="d371f-153">難解な LINQ メソッドへの呼び出しを特殊な LINQ 構文に追加できます。</span><span class="sxs-lookup"><span data-stu-id="d371f-153">Calls to esoteric LINQ methods can be appended to the specialized LINQ syntax.</span></span> <span data-ttu-id="d371f-154">次の C\# コードは、**crosscompany** メソッドに対してこれが実行されていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="d371f-154">The following C\# code shows this being done for the **crosscompany** method.</span></span>

```csharp
// C#, mixing LINQ syntax mechanisms.
var query = (from ct in customers
            from trans in customerTransactions
            where ct.AccountNum >= “4000”
            where trans.AccountNum == ct.AccountNum
            orderby ct.AccountNum descending
            select ct).crosscompany();
```

## <a name="linq-query-execution"></a><span data-ttu-id="d371f-155">LINQ クエリの実行</span><span class="sxs-lookup"><span data-stu-id="d371f-155">LINQ query execution</span></span>

<span data-ttu-id="d371f-156">LINQ クエリ用に生成されたコードは、実行時にツリーを構築します。</span><span class="sxs-lookup"><span data-stu-id="d371f-156">The code generated for a LINQ query builds a tree at run time.</span></span> <span data-ttu-id="d371f-157">クエリの結果が要求されるときは、このツリーは、ツリーを解釈するバックエンドに渡され、クエリで表された形でデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="d371f-157">When the results of the query are required, this tree is passed to the backend that will interpret it, and will provide the data as expressed in the query.</span></span> <span data-ttu-id="d371f-158">X++ コンパイラは、クエリを表すツリーも作成しますが、X++ コンパイラには、データベース バックエンドの機能についての詳細な知識があります。</span><span class="sxs-lookup"><span data-stu-id="d371f-158">The X++ compiler also builds a tree to express the query, but the X++ compiler has intimate knowledge about the capabilities of the database backend.</span></span> <span data-ttu-id="d371f-159">これには、以下のサブセクションで説明する重要な意味があります。</span><span class="sxs-lookup"><span data-stu-id="d371f-159">This has several important implications as described in the following subsections.</span></span>

### <a name="inability-to-diagnose-problems-at-linq-compile-time"></a><span data-ttu-id="d371f-160">LINQ コンパイル時に問題を診断することができません</span><span class="sxs-lookup"><span data-stu-id="d371f-160">Inability to diagnose problems at LINQ compile-time</span></span>

<span data-ttu-id="d371f-161">C\# コンパイラは多くの場合、互換性のない LINQ クエリをバックエンドで処理できないため、実行時に発生するエラーを予測および診断できません。</span><span class="sxs-lookup"><span data-stu-id="d371f-161">The C\# compiler is largely unable to foresee and diagnose errors that will occur at run time due to the inability of the backend to process an incompatible LINQ query.</span></span> <span data-ttu-id="d371f-162">たとえば、次の C\# コード ブロックで、特殊な LINQ 構文が C\# コンパイラに基づいて有効化されます。</span><span class="sxs-lookup"><span data-stu-id="d371f-162">For instance, in the following C\# code block, the specialized LINQ syntax is valid according to the C\# compiler.</span></span> <span data-ttu-id="d371f-163">まだ実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d371f-163">Yet at run time, an error would occur.</span></span>

```csharp
var customerQuery = from c in db.Customers
                    where (from o in db.Orders
                    where o.ShipCountry == “Germany”
                    select o.CustomerID).Contains(c.CustomerID);
```

<span data-ttu-id="d371f-164">このクエリは現在のデータ レイヤーでは処理できず、コンパイル時にエラーが診断されない間に、実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d371f-164">This query can't be handled by the current data layer, and while no errors are diagnosed at compile time, an error would occur at run time.</span></span>

### <a name="performance-penalty-with-linq"></a><span data-ttu-id="d371f-165">LINQ によるパフォーマンスが低下</span><span class="sxs-lookup"><span data-stu-id="d371f-165">Performance penalty with LINQ</span></span>

<span data-ttu-id="d371f-166">実行時には、ツリーの解析が行われ、適切なアクセス言語が生成されるときに、間接費のペナルティが支払われます。</span><span class="sxs-lookup"><span data-stu-id="d371f-166">There is an overhead penalty paid at run time, when analysis of the tree occurs, and a suitable access language is generated.</span></span> <span data-ttu-id="d371f-167">予想通り、LINQ 式ツリーを分析する際にパフォーマンス ペナルティが発生します。</span><span class="sxs-lookup"><span data-stu-id="d371f-167">As we might expect, the performance penalty is incurred when analyzing the LINQ expression tree.</span></span> <span data-ttu-id="d371f-168">実際にデータをフェッチするために実行時に必要な時間は、C\# と LINQ間と X++ と `while select` 間の間で大きく異なりません。</span><span class="sxs-lookup"><span data-stu-id="d371f-168">The time required at run time to actually fetch the data doesn't vary much between C\# and LINQ versus X++ with `while select`.</span></span> <span data-ttu-id="d371f-169">主要な数値は、レコードがほとんどフェッチされない場合、X++ `while select` と比較して、C\# LINQ ではクエリの最初から最後までのパフォーマンスが約 3 倍長くなりそうなことを示しています。</span><span class="sxs-lookup"><span data-stu-id="d371f-169">Our preliminary numbers show that the beginning-to-end performance of the query is about three times longer with C\# LINQ, compared to X++ `while select`, when very few records are fetched.</span></span> <span data-ttu-id="d371f-170">ただし、多くのレコードがフェッチされる場合、合計時間は C\# と X++ の間でほぼ同じです。</span><span class="sxs-lookup"><span data-stu-id="d371f-170">But when many records are fetched, the total times are about the same between C\# and X++.</span></span> <span data-ttu-id="d371f-171">結論として、言語ツリーを分析するよりも、多くのレコードを取得するほうが時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="d371f-171">The conclusion is that it takes much longer to fetch a lot of records than it takes to analyze the language tree.</span></span>

### <a name="composing-queries-with-linq"></a><span data-ttu-id="d371f-172">LINQ を使用したクエリの作成</span><span class="sxs-lookup"><span data-stu-id="d371f-172">Composing queries with LINQ</span></span>

<span data-ttu-id="d371f-173">LINQ によって提供されるモデルでは、クエリをサブクエリで構成できます。</span><span class="sxs-lookup"><span data-stu-id="d371f-173">The model that's provided by LINQ allows queries to be composed of subqueries.</span></span> <span data-ttu-id="d371f-174">X++ 言語は、この機能を正しく提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="d371f-174">The X++ language can't cleanly provide this feature.</span></span> <span data-ttu-id="d371f-175">これを理解するには、次の C\# LINQ コードを考えてみてください。</span><span class="sxs-lookup"><span data-stu-id="d371f-175">To understand this, consider the following C\# LINQ code.</span></span> <span data-ttu-id="d371f-176">フラグは、データの結果の順序を制御するメソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="d371f-176">A flag is passed to a method to control the ordering of data results.</span></span>

```csharp
private IEnumerable RichCustomers(bool orderByName)
{
    // Create a query for the rich customers. Note carefully
    // that no data is fetched when this is executed.
    var q = from c in customers where c.AmountMst > 1000000.0m select c;

    if (orderByName)
    {
        // Add the order by clause to the existing query.
        // Still no data is yet fetched.
        return q.OrderBy(c => c.AccountNum);
    }
    else
    {
        return q;
    }
}
```

### <a name="set-based-operations-with-linq"></a><span data-ttu-id="d371f-177">LINQ を使ったセットに基づく操作</span><span class="sxs-lookup"><span data-stu-id="d371f-177">Set based operations with LINQ</span></span>

<span data-ttu-id="d371f-178">LINQ クエリは、CRUD 操作に対して適用できます。</span><span class="sxs-lookup"><span data-stu-id="d371f-178">LINQ queries can be applied for CRUD operations.</span></span> <span data-ttu-id="d371f-179">ただし、レコードの更新、削除、挿入のモデルはセット ベース操作の式には役に立ちません。</span><span class="sxs-lookup"><span data-stu-id="d371f-179">But the model for updating, deleting, and inserting records isn't useful for the expression of set based operations.</span></span> <span data-ttu-id="d371f-180">現在、セットベース操作に変換される LINQ モデルに追加する拡張機能に取り組んできます。</span><span class="sxs-lookup"><span data-stu-id="d371f-180">We're now working on extensions to add to the LINQ model that will translate into set based operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d371f-181">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d371f-181">Additional resources</span></span>

[<span data-ttu-id="d371f-182">X++ と X++ コンパイラの変更</span><span class="sxs-lookup"><span data-stu-id="d371f-182">Changes in X++ and the X++ compiler</span></span>](programming-language-support.md)

[<span data-ttu-id="d371f-183">開発およびカスタマイズのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="d371f-183">Develop and customize home page</span></span>](developer-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]