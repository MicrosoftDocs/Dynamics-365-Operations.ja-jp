---
title: SQL インジェクション攻撃の緩和
description: このトピックでは、X++ で SQL インジェクション攻撃を緩和する方法について説明します。
author: pvillads
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31301
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68f8482c2488a7429b48f5e93411c7844c37ceea
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750968"
---
# <a name="mitigate-a-sql-injection-attack"></a><span data-ttu-id="cdcce-103">SQL インジェクション攻撃の緩和</span><span class="sxs-lookup"><span data-stu-id="cdcce-103">Mitigate a SQL injection attack</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="cdcce-104">SQL インジェクション攻撃は、悪意のあるデータ値がクエリ文字列で Microsoft SQL Server に渡されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-104">An SQL injection attack occurs when malicious data values are passed to Microsoft SQL Server in a query string.</span></span> <span data-ttu-id="cdcce-105">それらの値により、データベースに多くの損害が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-105">Those values can cause lots of damage in a database.</span></span> <span data-ttu-id="cdcce-106">SQL インジェクションは、ユーザー入力など、制御されていないソースからデータを SQL Server に渡すクエリを使用する方法に慎重でない場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-106">SQL injection can occur if you aren't careful about how you use a query to pass data that comes from an uncontrolled source, such as user input, to SQL Server.</span></span> <span data-ttu-id="cdcce-107">通常、X++ の組み込みデータ アクセス ステートメントにより回避されるため、Finance and Operations アプリで SQL インジェクションは問題になりません。</span><span class="sxs-lookup"><span data-stu-id="cdcce-107">SQL injection isn't usually an issue in Finance and Operations apps, because the built-in data access statements in X++ prevent it.</span></span> <span data-ttu-id="cdcce-108">ただし、ダイレクト SQL を使用する場合、SQL コードがそのままサーバーに渡されるときに SQL インジェクションが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-108">However, if you use Direct-SQL, SQL injection can occur when raw SQL code is passed to the server.</span></span>

<span data-ttu-id="cdcce-109">新しい API は、これらの攻撃を軽減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-109">A new API will help mitigate these attacks.</span></span> <span data-ttu-id="cdcce-110">Finance and Operations アプリのバージョン 10.0.17 用のプラットフォーム更新プログラム (2021 年 4 月) から API が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="cdcce-110">The API is available starting with platform updates for version 10.0.17 of Finance and Operations apps (April 2021).</span></span>

## <a name="the-issue"></a><span data-ttu-id="cdcce-111">問題</span><span class="sxs-lookup"><span data-stu-id="cdcce-111">The issue</span></span>

<span data-ttu-id="cdcce-112">開発者が次のコードを作成して、姓に基づいて顧客の名を検索するというシナリオを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-112">Consider a scenario where a developer writes the following code to look up the first name of customers, based on their last name.</span></span>

```xpp
public str GetFirstName(str name)
{
    str sqlStatementText = "SELECT TOP(1) firstName FROM Customer WHERE customer.Name = '" + name + "'";

    // Create a connection to the SQL Server
    var connection = new Connection();

    // Create a statement and submit the sql statement to the server:
    Statement statement = connection.createStatement();
    var results= statement.executeQuery(sqlStatementText);

    // Get the first record:
    results.next();
    statement.close();

    // Harvest the results.
    return results.getString(1);
}
```

<span data-ttu-id="cdcce-113">また、ユーザーが顧客名を入力する文字列フィールドのあるページ、またはサーバーに名前を入力できるようにするサービス エンドポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-113">Additionally, there is either a page where users can enter customer names in a string field, or a service endpoint that enables names to come into the server.</span></span>

<span data-ttu-id="cdcce-114">このシナリオでは、ユーザーが「Jones」などの有効な名前を入力すると、すべてが適切に機能します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-114">In this scenario, everything works well if users enter valid names such as "Jones."</span></span> <span data-ttu-id="cdcce-115">ただし、悪意のあるユーザーは、次の文字列を名前として入力することがあります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-115">However, a malicious user might enter the following string as a name.</span></span>

```xpp
'; drop table Customer --
```

<span data-ttu-id="cdcce-116">この場合、サーバーが実行する最後のクエリは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-116">In this case, here is the final query that the server runs.</span></span>

```xpp
SELECT TOP(1) firstName FROM Customer WHERE customer.Name = ''; drop table Customer --'
```

<span data-ttu-id="cdcce-117">指定された文字列の最初の引用符は、ユーザーが検索している名前を含んでいる文字列のリテラルで終了します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-117">The first quotation mark in the given string just ends the string literal that should contain the name that the user is looking for.</span></span> <span data-ttu-id="cdcce-118">セミコロン (;) はステートメントのターミネーター トークンとなるため、別の SQL ステートメントが実行されます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-118">Then another SQL statement is run because of the semicolon (;), which is a statement terminator token.</span></span> <span data-ttu-id="cdcce-119">この 2 つ目のステートメントは **顧客** テーブルとそれに含まれるすべてのデータを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-119">This second statement irretrievably deletes the **Customer** table and all the data in it.</span></span> <span data-ttu-id="cdcce-120">最後に、コメント文字 (--) により、最後の単一引用符で構文エラーが発生しないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-120">Finally, the commenting characters (--) ensure that the single quotation mark at the end doesn't cause syntax errors.</span></span> <span data-ttu-id="cdcce-121">したがって、文字列は有効な Transact SQL (T-SQL) になります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-121">Therefore, the string is valid Transact SQL (T-SQL).</span></span>

<span data-ttu-id="cdcce-122">SQL インジェクションは、実行時のテーブル、ビュー、およびストアド プロシージャの作成または削除を行う操作の実行を回避できるように、SQL Server への接続が制限されないために発生します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-122">SQL injection occurs because the connection to SQL Server doesn't impose any restrictions that prevent it from performing operations that create or delete tables, views, and stored procedures at runtime.</span></span> <span data-ttu-id="cdcce-123">したがって、組織は、開発者が実行している事柄を分かっている合理的なユーザーであるという前提に依存しています。</span><span class="sxs-lookup"><span data-stu-id="cdcce-123">Therefore, organizations must rely on the assumption that developers are reasonable people who know what they are doing.</span></span>

## <a name="the-solution"></a><span data-ttu-id="cdcce-124">ソリューション</span><span class="sxs-lookup"><span data-stu-id="cdcce-124">The solution</span></span>

<span data-ttu-id="cdcce-125">SQL Server は、*ステートメント パラメーター* を使用して脅威を緩和します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-125">SQL Server mitigates the threat by using *statement parameters*.</span></span> <span data-ttu-id="cdcce-126">ステートメント パラメーターは、結果の文字列のテキストが変更される可能性があるリテラルを使用することはありません。</span><span class="sxs-lookup"><span data-stu-id="cdcce-126">Statement parameters never use literals that are subject to textual changes to the resulting string.</span></span> <span data-ttu-id="cdcce-127">代わりに、コンテキストに依存する方法で提供される実際のコンテンツである、名前付きパラメーターが提供されます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-127">Instead, they provide named parameters, the actual content of which is provided contextually.</span></span> <span data-ttu-id="cdcce-128">このリリースで、Microsoft は、コードで SQL 文字列を作成する代わりにパラメーターを使用できるように新しい API を追加しました。</span><span class="sxs-lookup"><span data-stu-id="cdcce-128">For this release, Microsoft has added a new API that lets you use parameters instead of building SQL strings in code.</span></span>

<span data-ttu-id="cdcce-129">次の例で、これらの変更が組み込まれた後、前の例のコードがどのように見えるかを示します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-129">The following example shows what the code from the previous example looks like after these changes are incorporated.</span></span>

```xpp
public str GetFirstName(str name)
{
    str sqlStatementText = "SELECT TOP(1) firstName FROM Customer WHERE customer.Name = @Name";

    // Create a connection to the SQL Server
    var connection = new Connection();

    // Submit the sql statement to the server:
    Statement statement = connection.createStatement();

    // Create a mapping from parameter names onto values
    Map paramMap = SqlParams::create();
    paramMap.add('Name', name);

    // Execute the query, providing both the query
    // and the parameters.
    var results= statement.executeQueryWithParameters(sqlStatementText, paramMap);

    // Capture the results:
    results.next();
    statement.close();

    return results.getString(1);
}
```

<span data-ttu-id="cdcce-130">更新された例では、パラメーターを使っていなかった古い API の代わりに、新しい **executeQueryWithParameters** API を使用しています。</span><span class="sxs-lookup"><span data-stu-id="cdcce-130">The updated example uses the new **executeQueryWithParameters** API instead of the old API that didn't take parameters.</span></span> <span data-ttu-id="cdcce-131">このコードは、パラメーター名からパラメーター値へのマッピングを含むマップをビルドします。</span><span class="sxs-lookup"><span data-stu-id="cdcce-131">The code builds the map that contains the mapping from parameter names to parameter values.</span></span> <span data-ttu-id="cdcce-132">この場合、**名前** は SQL の **\@Name** の値になります。</span><span class="sxs-lookup"><span data-stu-id="cdcce-132">In this case, **Name** will be the value of **\@Name** in SQL.</span></span> <span data-ttu-id="cdcce-133">**名前** の値は、任意のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-133">The incoming **name** value can be anything.</span></span>

<span data-ttu-id="cdcce-134">**ステートメント** タイプの関連メソッドは、行ではなく整数値を返すステートメントを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-134">A related method on the **Statement** type is used to run statements that return integer values instead of rows.</span></span> <span data-ttu-id="cdcce-135">通常、整数値は影響を受けた行数を示します。</span><span class="sxs-lookup"><span data-stu-id="cdcce-135">Typically, the integer value indicates the number of rows that are affected.</span></span> <span data-ttu-id="cdcce-136">次の例では、**executeQueryWithParameters** API を使用した X++ データ ステートメントを使用しています。</span><span class="sxs-lookup"><span data-stu-id="cdcce-136">The following example uses the X++ data statements with the **executeQueryWithParameters** API.</span></span>

```xpp
public void InsertWithStrParameter()
{
    var connection = new Connection();
    Statement statement = connection.createStatement();

    connection.ttsbegin();

    str sql = @"
        UPDATE Wages
        SET Wages.Wage = Wages.Wage * @percent
        WHERE Wages.Level = @Level";

    Map paramMap = SqlParams::create();
    paramMap.add('percent', 1.1);        // 10 percent increase
    paramMap.add('Level', 'Manager');    // Management increase

    int cnt = statement.executeUpdateWithParameters(sql, paramMap);
    statement.close();

    connection.ttscommit();
}
```

## <a name="conclusion"></a><span data-ttu-id="cdcce-137">まとめ</span><span class="sxs-lookup"><span data-stu-id="cdcce-137">Conclusion</span></span>

<span data-ttu-id="cdcce-138">Microsoft は新しいメソッドを導入しているので、既存のメソッド (つまり、パラメーターなしのメソッド) を廃止としてマークしています。</span><span class="sxs-lookup"><span data-stu-id="cdcce-138">As Microsoft introduces the new methods, we are also marking the existing methods (that is, the methods without the parameters) as obsolete.</span></span> <span data-ttu-id="cdcce-139">通常の廃止期間が適用されます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-139">The usual deprecation periods apply.</span></span> <span data-ttu-id="cdcce-140">したがって、コードを更新して、パラメーターにより提供される新しい保護を活用することができます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-140">Therefore, you can update your code to take advantage of the new protection that the parameters provide.</span></span>

<span data-ttu-id="cdcce-141">新しい **executeQueryWithParameters** API は顧客を災害から保護するのに役立ちますが、使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cdcce-141">Although the new **executeQueryWithParameters** API helps you protect your customers from disasters, you aren't required to use it.</span></span> <span data-ttu-id="cdcce-142">文字列を連結し、空のパラメーター セットを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="cdcce-142">You can still do string concatenations and provide an empty parameter set.</span></span> <span data-ttu-id="cdcce-143">ただし、この場合、パラメーターを提供することによるメリットはありません。</span><span class="sxs-lookup"><span data-stu-id="cdcce-143">However, in this case, you don't gain the advantages that the parameters provide.</span></span> <span data-ttu-id="cdcce-144">この機会を利用して、コード内で使用されている危険を取り除いてください。</span><span class="sxs-lookup"><span data-stu-id="cdcce-144">We hope that you will take this opportunity to eliminate any dangerous usage that you have in your code.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]