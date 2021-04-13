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
# <a name="mitigate-a-sql-injection-attack"></a>SQL インジェクション攻撃の緩和

[!include [banner](../includes/banner.md)]

[!include [preview-banner](../includes/preview-banner.md)]

SQL インジェクション攻撃は、悪意のあるデータ値がクエリ文字列で Microsoft SQL Server に渡されるときに発生します。 それらの値により、データベースに多くの損害が発生することがあります。 SQL インジェクションは、ユーザー入力など、制御されていないソースからデータを SQL Server に渡すクエリを使用する方法に慎重でない場合に発生することがあります。 通常、X++ の組み込みデータ アクセス ステートメントにより回避されるため、Finance and Operations アプリで SQL インジェクションは問題になりません。 ただし、ダイレクト SQL を使用する場合、SQL コードがそのままサーバーに渡されるときに SQL インジェクションが発生する可能性があります。

新しい API は、これらの攻撃を軽減するのに役立ちます。 Finance and Operations アプリのバージョン 10.0.17 用のプラットフォーム更新プログラム (2021 年 4 月) から API が使用可能です。

## <a name="the-issue"></a>問題

開発者が次のコードを作成して、姓に基づいて顧客の名を検索するというシナリオを考えてみます。

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

また、ユーザーが顧客名を入力する文字列フィールドのあるページ、またはサーバーに名前を入力できるようにするサービス エンドポイントがあります。

このシナリオでは、ユーザーが「Jones」などの有効な名前を入力すると、すべてが適切に機能します。 ただし、悪意のあるユーザーは、次の文字列を名前として入力することがあります。

```xpp
'; drop table Customer --
```

この場合、サーバーが実行する最後のクエリは次のようになります。

```xpp
SELECT TOP(1) firstName FROM Customer WHERE customer.Name = ''; drop table Customer --'
```

指定された文字列の最初の引用符は、ユーザーが検索している名前を含んでいる文字列のリテラルで終了します。 セミコロン (;) はステートメントのターミネーター トークンとなるため、別の SQL ステートメントが実行されます。 この 2 つ目のステートメントは **顧客** テーブルとそれに含まれるすべてのデータを完全に削除します。 最後に、コメント文字 (--) により、最後の単一引用符で構文エラーが発生しないことを確認します。 したがって、文字列は有効な Transact SQL (T-SQL) になります。

SQL インジェクションは、実行時のテーブル、ビュー、およびストアド プロシージャの作成または削除を行う操作の実行を回避できるように、SQL Server への接続が制限されないために発生します。 したがって、組織は、開発者が実行している事柄を分かっている合理的なユーザーであるという前提に依存しています。

## <a name="the-solution"></a>ソリューション

SQL Server は、*ステートメント パラメーター* を使用して脅威を緩和します。 ステートメント パラメーターは、結果の文字列のテキストが変更される可能性があるリテラルを使用することはありません。 代わりに、コンテキストに依存する方法で提供される実際のコンテンツである、名前付きパラメーターが提供されます。 このリリースで、Microsoft は、コードで SQL 文字列を作成する代わりにパラメーターを使用できるように新しい API を追加しました。

次の例で、これらの変更が組み込まれた後、前の例のコードがどのように見えるかを示します。

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

更新された例では、パラメーターを使っていなかった古い API の代わりに、新しい **executeQueryWithParameters** API を使用しています。 このコードは、パラメーター名からパラメーター値へのマッピングを含むマップをビルドします。 この場合、**名前** は SQL の **\@Name** の値になります。 **名前** の値は、任意のものにすることができます。

**ステートメント** タイプの関連メソッドは、行ではなく整数値を返すステートメントを実行するために使用されます。 通常、整数値は影響を受けた行数を示します。 次の例では、**executeQueryWithParameters** API を使用した X++ データ ステートメントを使用しています。

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

## <a name="conclusion"></a>まとめ

Microsoft は新しいメソッドを導入しているので、既存のメソッド (つまり、パラメーターなしのメソッド) を廃止としてマークしています。 通常の廃止期間が適用されます。 したがって、コードを更新して、パラメーターにより提供される新しい保護を活用することができます。

新しい **executeQueryWithParameters** API は顧客を災害から保護するのに役立ちますが、使用する必要はありません。 文字列を連結し、空のパラメーター セットを提供することもできます。 ただし、この場合、パラメーターを提供することによるメリットはありません。 この機会を利用して、コード内で使用されている危険を取り除いてください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]