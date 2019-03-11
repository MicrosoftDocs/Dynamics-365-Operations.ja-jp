---
title: C# の統合言語クエリ (LINQ) プロバイダー
description: このトピックでは、LINQ プロバイダーについて説明します。
author: pvillads
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26751
ms.assetid: 8bd10c93-9d5e-49d7-b20f-7f804e16e76c
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ffd29a18875dd13da35856bb4b55ebc27d41078
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369552"
---
# <a name="language-integrated-query-linq-provider-for-c"></a><span data-ttu-id="e7343-103">C# の統合言語クエリ (LINQ) プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e7343-103">Language Integrated Query (LINQ) provider for C#</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7343-104">このトピックでは、LINQ プロバイダーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e7343-104">This topic discusses the LINQ provider.</span></span>

<span data-ttu-id="e7343-105">LINQ (統合言語クエリ) は、さまざまな場所および形式で保存されているデータにアクセスできるクラスおよびメソッドのセットです。</span><span class="sxs-lookup"><span data-stu-id="e7343-105">LINQ (Language Integrated Query) is a set of classes and methods that enable you to access data that is stored in a variety of places and formats.</span></span> <span data-ttu-id="e7343-106">LINQ フレームワークは、マネージド言語のデータにアクセスするための標準です。</span><span class="sxs-lookup"><span data-stu-id="e7343-106">The LINQ framework is the standard for accessing data in managed languages.</span></span> <span data-ttu-id="e7343-107">LINQ は次のような異なる種類のデータ ソースからのデータへのアクセスに関する統合されて一貫した API をプログラマーに提示します。</span><span class="sxs-lookup"><span data-stu-id="e7343-107">LINQ presents to programmers a unified and consistent API for data access from heterogeneous data sources, such as:</span></span>

-   <span data-ttu-id="e7343-108">メモリ内のオブジェクト グラフ</span><span class="sxs-lookup"><span data-stu-id="e7343-108">In-memory object graphs</span></span>
-   <span data-ttu-id="e7343-109">Active Directory エントリ</span><span class="sxs-lookup"><span data-stu-id="e7343-109">Active Directory entries</span></span>
-   <span data-ttu-id="e7343-110">Flickr 画像および XML</span><span class="sxs-lookup"><span data-stu-id="e7343-110">Flickr pictures and XML</span></span>
-   <span data-ttu-id="e7343-111">SQL Server</span><span class="sxs-lookup"><span data-stu-id="e7343-111">SQL Server</span></span>

<span data-ttu-id="e7343-112">LINQ プロバイダーでは、.NET マネージド言語を使用して業務データにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e7343-112">The LINQ provider allows the user to access business data by using .NET managed languages.</span></span>

## <a name="two-syntactical-mechanisms-for-accessing-linq"></a><span data-ttu-id="e7343-113">LINQ にアクセスするための 2 つの構文メカニズム</span><span class="sxs-lookup"><span data-stu-id="e7343-113">Two syntactical mechanisms for accessing LINQ</span></span>
<span data-ttu-id="e7343-114">次のテーブルに示すように、LINQ を使用する構文的アプローチは 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="e7343-114">There are two syntactical approaches for using LINQ, as described in the following table.</span></span>

|                                                                    | <span data-ttu-id="e7343-115">**X++**</span><span class="sxs-lookup"><span data-stu-id="e7343-115">**X++**</span></span>                                                                                   | <span data-ttu-id="e7343-116">**C\# および Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="e7343-116">**C\# and Visual Basic**</span></span>           |
|-----------------|-----------------------|------------------------------------|
| <span data-ttu-id="e7343-117">**標準メソッドの呼び出し構文による LINQ。**</span><span class="sxs-lookup"><span data-stu-id="e7343-117">**LINQ by standard method call syntax.**</span></span>                           | <span data-ttu-id="e7343-118">実用的ではありません。</span><span class="sxs-lookup"><span data-stu-id="e7343-118">Impractical.</span></span> <span data-ttu-id="e7343-119">ジェネリックの言語サポートは、LINQ にとって重要で、X++ ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e7343-119">Language support for generics is vital for LINQ and is not supported in X++.</span></span> | <span data-ttu-id="e7343-120">必須のラムダ構文が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e7343-120">Available, requires lambda syntax.</span></span> |
| <span data-ttu-id="e7343-121">**コンパイラで認識される特殊な構文による LINQ。**</span><span class="sxs-lookup"><span data-stu-id="e7343-121">**LINQ by specialized syntax that is understood by the compiler.**</span></span> | <span data-ttu-id="e7343-122">使用不可。</span><span class="sxs-lookup"><span data-stu-id="e7343-122">Not available.</span></span>                                                                            | <span data-ttu-id="e7343-123">簡単に使用できます。</span><span class="sxs-lookup"><span data-stu-id="e7343-123">Available, easier to use.</span></span>          |

<span data-ttu-id="e7343-124">C\# (または Visual Basic) の LINQ プロバイダーにアクセスするには、2 つの構文メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="e7343-124">There are two syntactic mechanisms for accessing the LINQ provider in C\# (or in Visual Basic):</span></span>

-   <span data-ttu-id="e7343-125">標準、または流暢なメソッドの呼び出し構文。</span><span class="sxs-lookup"><span data-stu-id="e7343-125">By standard, or fluent, method call syntax.</span></span>
-   <span data-ttu-id="e7343-126">特殊な構文により、C\# コンパイラは LINQ メソッド呼び出しと同等として理解できるように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="e7343-126">By specialized syntax that the C\# compiler has been enhanced to understand as equivalent to the LINQ method calls.</span></span> <span data-ttu-id="e7343-127">(このような構文は「構文砂糖」とも呼ばれます。)</span><span class="sxs-lookup"><span data-stu-id="e7343-127">(Such syntax is sometimes called “syntactic sugar”.)</span></span>

<span data-ttu-id="e7343-128">このトピックでは、簡単な特殊構文から始めて、LINQ の各構文メカニズムを検討します。</span><span class="sxs-lookup"><span data-stu-id="e7343-128">This topic is going to review each syntactic mechanism for LINQ, starting with the easier specialized syntax.</span></span>

## <a name="linq-by-specialized-syntax-in-c"></a><span data-ttu-id="e7343-129">C\# の特殊な構文による LINQ</span><span class="sxs-lookup"><span data-stu-id="e7343-129">LINQ by specialized syntax in C\#</span></span>
<span data-ttu-id="e7343-130">一部の .NET 言語は、書きやすい代替方法として LINQ 向けの特殊な構文を理解します。</span><span class="sxs-lookup"><span data-stu-id="e7343-130">Some .NET languages understand specialized syntax for LINQ as an alternative that is easier for us to write.</span></span> <span data-ttu-id="e7343-131">C\# はそのような言語の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="e7343-131">C\# is one such language.</span></span> <span data-ttu-id="e7343-132">***var に関する注記:*** C\# で LINQ を使用するには、変数を宣言するために使用される\#キーワード **var** を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7343-132">***Note about var:*** To use LINQ in C\#, you must understand the C\# keyword **var**, which is used to declare variables.</span></span> <span data-ttu-id="e7343-133">var キーワードは、変数に割り当てられているものによって変数のデータ型を把握するようにコンパイラに指示します。</span><span class="sxs-lookup"><span data-stu-id="e7343-133">The var keyword tells the compiler to figure out the data type of the variable by what is assigned to the variable.</span></span> <span data-ttu-id="e7343-134">この機能は、X++ でも利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="e7343-134">This feature is now also available in X++.</span></span> <span data-ttu-id="e7343-135">タイプはソース コード内に暗黙的に格納されており、コンパイルが完了した後にタイプは解決され、変更されません。</span><span class="sxs-lookup"><span data-stu-id="e7343-135">The type is implicit in the source code, and the type is settled and unvarying after the compilation completes.</span></span>

### <a name="comparing-x-to-c-linq"></a><span data-ttu-id="e7343-136">X++ to C\# LINQ の比較</span><span class="sxs-lookup"><span data-stu-id="e7343-136">Comparing X++ to C\# LINQ</span></span>

<span data-ttu-id="e7343-137">X++ 言語は、便利で使いやすい `while select` ステートメントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e7343-137">The X++ language supports the useful and easy to use `while select` statement.</span></span> <span data-ttu-id="e7343-138">これは、X++ `while select` 構文と特殊な C\#LINQ の構文を比較しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="e7343-138">This lest you compare the X++ `while select` syntax to the specialized C\# LINQ syntax.</span></span> <span data-ttu-id="e7343-139">最初に、これが X++ のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="e7343-139">First, here is the X++ sample.</span></span>

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

<span data-ttu-id="e7343-140">次は、特殊な LINQ 構文と同等の C\# のクエリです。</span><span class="sxs-lookup"><span data-stu-id="e7343-140">Next is an equivalent query in C\# with the specialized LINQ syntax.</span></span>

    // Get access to the data provider:       // C#, with specialized LINQ syntax.
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

## <a name="linq-query-in-c-by-method-syntax-using-the-lambda-operator-gt"></a><span data-ttu-id="e7343-141">ラムダ演算子 =&gt; を使用しているメソッドの構文による C\# の LINQ クエリ</span><span class="sxs-lookup"><span data-stu-id="e7343-141">LINQ query in C\# by method syntax, using the lambda operator =&gt;</span></span>
<span data-ttu-id="e7343-142">次は、C\# での LINQ の別の用途です。今回以外では、LINQ API を呼び出すためにより多くの標準構文が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e7343-142">Next is another use of LINQ in C\#, except this time the more standard syntax is used to call the LINQ API.</span></span> <span data-ttu-id="e7343-143">このアプローチでは、ラムダ演算子 **=&gt;** も使用されます。</span><span class="sxs-lookup"><span data-stu-id="e7343-143">The approach also involves use of the lambda operator **=&gt;**.</span></span> <span data-ttu-id="e7343-144">次の C\# クエリは、前述の C\# クエリと機能的に同等です。</span><span class="sxs-lookup"><span data-stu-id="e7343-144">The following C\# query is functionally equivalent to the preceding C\# query.</span></span>

    var query = customers
        .Where(c => string.Compare(c.AccountNum, "4000") >= 0)
        .Join(customers, 
              primary => primary.AccountNum,
              foreign => foreign.AccountNum,
              (primary, foreign) => new { P = primary, F = foreign })
        .OrderBy(primaryAndForeign => primaryAndForeign.P.AccountNum)
        .Select(primaryAndForeign => primaryAndForeign.P);

<span data-ttu-id="e7343-145">X++ で使用されている `while select` 構文と C\# の特殊な LINQ 構文 (Visual Basic には特に優れた LINQ 構文があります) の間に良好な一致があります。</span><span class="sxs-lookup"><span data-stu-id="e7343-145">There's a good match between the `while select` syntax used in X++ and the specialized LINQ syntax in C\# (Visual Basic has particularly good LINQ syntax).</span></span> <span data-ttu-id="e7343-146">特殊な LINQ 構文は実際、結合を表現する際に有効ですが、C\# コンパイラに組み込まれた特殊な構文は Finance and Operations が提供する拡張機能を処理しません。</span><span class="sxs-lookup"><span data-stu-id="e7343-146">It's evident that the specialized LINQ syntax is actually very useful in expressing joins, but the specialized syntax built into the C\# compiler doesn't handle the extensions provided by Finance and Operations.</span></span>

### <a name="limitation-of-the-specialized-linq-syntax"></a><span data-ttu-id="e7343-147">特殊な LINQ 構文の制限</span><span class="sxs-lookup"><span data-stu-id="e7343-147">Limitation of the specialized LINQ syntax</span></span>

<span data-ttu-id="e7343-148">LINQ プロバイダーへの拡張機能で拡張できない特殊な LINQ 構文の制限。</span><span class="sxs-lookup"><span data-stu-id="e7343-148">A limitation of the specialized LINQ syntax is that it can't be augmented with extensions to the LINQ provider.</span></span> <span data-ttu-id="e7343-149">対照的に、メソッド呼び出しとラムダ演算子の標準構文は必要に応じて拡張できます。</span><span class="sxs-lookup"><span data-stu-id="e7343-149">In contrast, standard syntax of method calls plus the lambda operator can be extended as needed.</span></span> <span data-ttu-id="e7343-150">たとえば、LINQ フレームワークは、C\# で LINQ の特別な構文で表されない会社間のヒントに対するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="e7343-150">For instance, the LINQ framework provides a method for cross-company hints that can't be expressed in the special syntax for LINQ in C\#.</span></span> <span data-ttu-id="e7343-151">ただし、クエリを作成する能力のため、この制限は大きな問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="e7343-151">Fortunately, due to the ability to compose queries, this limitation need not be a major problem.</span></span> <span data-ttu-id="e7343-152">難解な LINQ メソッドへの呼び出しを特殊な LINQ 構文に追加できます。</span><span class="sxs-lookup"><span data-stu-id="e7343-152">Calls to esoteric LINQ methods can be appended to the specialized LINQ syntax.</span></span> <span data-ttu-id="e7343-153">次の C\# コードは、**crosscompany** メソッドに対してこれが実行されていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="e7343-153">The following C\# code shows this being done for the **crosscompany** method.</span></span>

    var query = (from ct in customers
                from trans in customerTransactions
                where ct.AccountNum >= “4000”
                where trans.AccountNum == ct.AccountNum
                orderby ct.AccountNum descending
                select ct).crosscompany();      // C#, mixing LINQ syntax mechanisms.

## <a name="linq-query-execution"></a><span data-ttu-id="e7343-154">LINQ クエリの実行</span><span class="sxs-lookup"><span data-stu-id="e7343-154">LINQ query execution</span></span>
<span data-ttu-id="e7343-155">LINQ クエリ用に生成されたコードは、実行時にツリーを構築します。</span><span class="sxs-lookup"><span data-stu-id="e7343-155">The code generated for a LINQ query builds a tree at run time.</span></span> <span data-ttu-id="e7343-156">クエリの結果が要求されるときは、このツリーは、ツリーを解釈するバックエンドに渡され、クエリで表された形でデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="e7343-156">When the results of the query are required, this tree is passed to the backend that will interpret it, and will provide the data as expressed in the query.</span></span> <span data-ttu-id="e7343-157">X++ コンパイラは、クエリを表すツリーも作成しますが、X++ コンパイラには、データベース バックエンドの機能についての詳細な知識があります。</span><span class="sxs-lookup"><span data-stu-id="e7343-157">The X++ compiler also builds a tree to express the query, but the X++ compiler has intimate knowledge about the capabilities of the database backend.</span></span> <span data-ttu-id="e7343-158">これには、以下のサブセクションで説明する重要な意味があります。</span><span class="sxs-lookup"><span data-stu-id="e7343-158">This has several important implications as described in the following subsections.</span></span>

### <a name="inability-to-diagnose-problems-at-linq-compile-time"></a><span data-ttu-id="e7343-159">LINQ コンパイル時に問題を診断することができません</span><span class="sxs-lookup"><span data-stu-id="e7343-159">Inability to diagnose problems at LINQ compile-time</span></span>

<span data-ttu-id="e7343-160">C\# コンパイラは多くの場合、互換性のない LINQ クエリをバックエンドで処理できないため、実行時に発生するエラーを予測および診断できません。</span><span class="sxs-lookup"><span data-stu-id="e7343-160">The C\# compiler is largely unable to foresee and diagnose errors that will occur at run time due to the inability of the backend to process an incompatible LINQ query.</span></span> <span data-ttu-id="e7343-161">たとえば、次の C\# コード ブロックで、特殊な LINQ 構文が C\# コンパイラに基づいて有効化されます。</span><span class="sxs-lookup"><span data-stu-id="e7343-161">For instance, in the following C\# code block, the specialized LINQ syntax is valid according to the C\# compiler.</span></span> <span data-ttu-id="e7343-162">まだ実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e7343-162">Yet at run time, an error would occur.</span></span>

    var customerQuery = from c in db.Customers    // C#
                        where (from o in db.Orders
                        where o.ShipCountry == “Germany”
                        select o.CustomerID).Contains(c.CustomerID);

<span data-ttu-id="e7343-163">このクエリは現在のデータ レイヤーでは処理できず、コンパイル時にエラーが診断されない間に、実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e7343-163">This query can't be handled by the current data layer, and while no errors are diagnosed at compile time, an error would occur at run time.</span></span>

### <a name="performance-penalty-with-linq"></a><span data-ttu-id="e7343-164">LINQ によるパフォーマンスが低下</span><span class="sxs-lookup"><span data-stu-id="e7343-164">Performance penalty with LINQ</span></span>

<span data-ttu-id="e7343-165">実行時には、ツリーの解析が行われ、適切なアクセス言語が生成されるときに、間接費のペナルティが支払われます。</span><span class="sxs-lookup"><span data-stu-id="e7343-165">There is an overhead penalty paid at run time, when analysis of the tree occurs, and a suitable access language is generated.</span></span> <span data-ttu-id="e7343-166">予想通り、LINQ 式ツリーを分析する際にパフォーマンス ペナルティが発生します。</span><span class="sxs-lookup"><span data-stu-id="e7343-166">As we might expect, the performance penalty is incurred when analyzing the LINQ expression tree.</span></span> <span data-ttu-id="e7343-167">実際にデータをフェッチするために実行時に必要な時間は、C\# と LINQ間と X++ と `while select` 間の間で大きく異なりません。</span><span class="sxs-lookup"><span data-stu-id="e7343-167">The time required at run time to actually fetch the data doesn't vary much between C\# and LINQ versus X++ with `while select`.</span></span> <span data-ttu-id="e7343-168">主要な数値は、レコードがほとんどフェッチされない場合、X++ `while select` と比較して、C\# LINQ ではクエリの最初から最後までのパフォーマンスが約 3 倍長くなりそうなことを示しています。</span><span class="sxs-lookup"><span data-stu-id="e7343-168">Our preliminary numbers show that the beginning-to-end performance of the query is about three times longer with C\# LINQ, compared to X++ `while select`, when very few records are fetched.</span></span> <span data-ttu-id="e7343-169">ただし、多くのレコードがフェッチされる場合、合計時間は C\# と X++ の間でほぼ同じです。</span><span class="sxs-lookup"><span data-stu-id="e7343-169">But when many records are fetched, the total times are about the same between C\# and X++.</span></span> <span data-ttu-id="e7343-170">結論として、言語ツリーを分析するよりも、多くのレコードを取得するほうが時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="e7343-170">The conclusion is that it takes much longer to fetch a lot of records than it takes to analyze the language tree.</span></span>

### <a name="query-composability-with-linq"></a><span data-ttu-id="e7343-171">LINQ を使った構成可能性の照会</span><span class="sxs-lookup"><span data-stu-id="e7343-171">Query composability with LINQ</span></span>

<span data-ttu-id="e7343-172">LINQ によって提供されるモデルでは、クエリをサブクエリで構成できます。</span><span class="sxs-lookup"><span data-stu-id="e7343-172">The model that's provided by LINQ allows queries to be composed of subqueries.</span></span> <span data-ttu-id="e7343-173">X++ 言語は、この機能を正しく提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="e7343-173">The X++ language can't cleanly provide this feature.</span></span> <span data-ttu-id="e7343-174">これを理解するには、次の C\# LINQ コードを考えてみてください。</span><span class="sxs-lookup"><span data-stu-id="e7343-174">To understand this, consider the following C\# LINQ code.</span></span> <span data-ttu-id="e7343-175">フラグは、データの結果の順序を制御するメソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e7343-175">A flag is passed to a method to control the ordering of data results.</span></span>

    private IEnumerable RichCustomers(bool orderByName)    // C#
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

### <a name="set-based-operations-with-linq"></a><span data-ttu-id="e7343-176">LINQ を使ったセットに基づく操作</span><span class="sxs-lookup"><span data-stu-id="e7343-176">Set based operations with LINQ</span></span>

<span data-ttu-id="e7343-177">LINQ クエリは、CRUD 操作に対して適用できます。</span><span class="sxs-lookup"><span data-stu-id="e7343-177">LINQ queries can be applied for CRUD operations.</span></span> <span data-ttu-id="e7343-178">ただし、レコードの更新、削除、挿入のモデルはセット ベース操作の式には役に立ちません。</span><span class="sxs-lookup"><span data-stu-id="e7343-178">But the model for updating, deleting, and inserting records isn't useful for the expression of set based operations.</span></span> <span data-ttu-id="e7343-179">現在、セットベース操作に変換される LINQ モデルに追加する拡張機能に取り組んできます。</span><span class="sxs-lookup"><span data-stu-id="e7343-179">We're now working on extensions to add to the LINQ model that will translate into set based operations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="e7343-180">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="e7343-180">Additional resources</span></span>
--------

[<span data-ttu-id="e7343-181">プログラミング言語のサポート</span><span class="sxs-lookup"><span data-stu-id="e7343-181">Programming language support</span></span>](programming-language-support.md)

[<span data-ttu-id="e7343-182">技術概念ガイド</span><span class="sxs-lookup"><span data-stu-id="e7343-182">Technical Concepts Guide</span></span>](developer-home-page.md)



