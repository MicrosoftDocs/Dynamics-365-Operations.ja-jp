---
title: C# の統合言語クエリ (LINQ) プロバイダー
description: この記事では、LINQ プロバイダーについて説明します。
author: pvillads
ms.date: 11/03/2017
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 26751
ms.assetid: 8bd10c93-9d5e-49d7-b20f-7f804e16e76c
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d2d5b5242fee3a2fb78600f47ccda3a36f0c84f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867042"
---
# <a name="language-integrated-query-linq-provider-for-c"></a>C\# の統合言語クエリ (LINQ) プロバイダー

[!include [banner](../includes/banner.md)]

この記事では、LINQ プロバイダーについて説明します。

LINQ (統合言語クエリ) は、さまざまな場所および形式で保存されているデータにアクセスできるクラスおよびメソッドのセットです。 LINQ フレームワークは、マネージド言語のデータにアクセスするための標準です。 LINQ は次のような異なる種類のデータ ソースからのデータへのアクセスに関する統合されて一貫した API をプログラマーに提示します。

- メモリ内のオブジェクト グラフ
- Active Directory エントリ
- Flickr 画像および XML
- SQL Server

LINQ プロバイダーでは、.NET マネージド言語を使用して業務データにアクセスできます。

## <a name="two-syntactical-mechanisms-for-accessing-linq"></a>LINQ にアクセスするための 2 つの構文メカニズム

次のテーブルに示すように、LINQ を使用する構文的アプローチは 2 つあります。

| アプローチ | X++ | C\# と Visual Basic |
|-------------------------|------------------|---------------------------|
| 標準メソッドの呼び出し構文による LINQ。 | 実用的ではありません。 ジェネリックの言語サポートは、LINQ にとって重要で、X++ ではサポートされていません。 | 必須のラムダ構文が使用可能です。 |
| コンパイラで認識される特殊な構文による LINQ。 | 使用不可。   | 簡単に使用できます。 |

C\# (または Visual Basic) の LINQ プロバイダーにアクセスするには、2 つの構文メカニズムがあります。

- 標準、または流暢なメソッドの呼び出し構文。
- 特殊な構文により、C\# コンパイラは LINQ メソッド呼び出しと同等として理解できるように拡張されています。 (このような構文は「構文砂糖」とも呼ばれます。)

この記事では、簡単な特殊構文から始めて、LINQ の各構文メカニズムを検討します。

## <a name="linq-by-specialized-syntax-in-c"></a>C\# の特殊な構文による LINQ

一部の .NET 言語は、書きやすい代替方法として LINQ 向けの特殊な構文を理解します。 C\# はそのような言語の 1 つです。

C\# で LINQ を使用するには、変数の宣言に使われる、C\# のキーワード **var** を理解する必要があります。 var キーワードは、変数に割り当てられているものによって変数のデータ型を把握するようにコンパイラに指示します。 この機能は、X++ でも利用可能になりました。 タイプはソース コード内に暗黙的に格納されており、コンパイルが完了した後にタイプは解決され、変更されません。

### <a name="comparing-x-to-c-linq"></a>X++ to C\# LINQ の比較

X++ 言語は、便利で使いやすい `while select` ステートメントをサポートしています。 これは、X++ `while select` 構文と特殊な C\#LINQ の構文を比較しないようにするためです。 最初に、これが X++ のサンプルです。

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

次は、特殊な LINQ 構文と同等の C\# のクエリです。

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

## <a name="linq-query-in-c-by-method-syntax-using-the-lambda-operator-"></a>メソッド構文による C\# の LINQ クエリでは、ラムダ演算子 > を使用します

次は、C\# での LINQ の別の用途です。今回以外では、LINQ API を呼び出すためにより多くの標準構文が使用されます。 この方法では、ラムダ演算子 `>` を使用します。 次の C\# クエリは、前述の C\# クエリと機能的に同等です。

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

X++ で使用されている `while select` 構文と C\# の特殊な LINQ 構文 (Visual Basic には特に優れた LINQ 構文があります) の間に良好な一致があります。 特殊な LINQ 構文は実際、結合を表現する際に有効ですが、C\# コンパイラに組み込まれた特殊な構文は Finance and Operations アプリケーションが提供する拡張機能を処理しません。

### <a name="limitation-of-the-specialized-linq-syntax"></a>特殊な LINQ 構文の制限

LINQ プロバイダーへの拡張機能で拡張できない特殊な LINQ 構文の制限。 対照的に、メソッド呼び出しとラムダ演算子の標準構文は必要に応じて拡張できます。 たとえば、LINQ フレームワークは、C\# で LINQ の特別な構文で表されない会社間のヒントに対するメソッドを提供します。 ただし、クエリを作成する能力のため、この制限は大きな問題ではありません。 難解な LINQ メソッドへの呼び出しを特殊な LINQ 構文に追加できます。 次の C\# コードは、**crosscompany** メソッドに対してこれが実行されていることを示しています。

```csharp
// C#, mixing LINQ syntax mechanisms.
var query = (from ct in customers
            from trans in customerTransactions
            where ct.AccountNum >= “4000”
            where trans.AccountNum == ct.AccountNum
            orderby ct.AccountNum descending
            select ct).crosscompany();
```

## <a name="linq-query-execution"></a>LINQ クエリの実行

LINQ クエリ用に生成されたコードは、実行時にツリーを構築します。 クエリの結果が要求されるときは、このツリーは、ツリーを解釈するバックエンドに渡され、クエリで表された形でデータを提供します。 X++ コンパイラは、クエリを表すツリーも作成しますが、X++ コンパイラには、データベース バックエンドの機能についての詳細な知識があります。 これには、以下のサブセクションで説明する重要な意味があります。

### <a name="inability-to-diagnose-problems-at-linq-compile-time"></a>LINQ コンパイル時に問題を診断することができません

C\# コンパイラは多くの場合、互換性のない LINQ クエリをバックエンドで処理できないため、実行時に発生するエラーを予測および診断できません。 たとえば、次の C\# コード ブロックで、特殊な LINQ 構文が C\# コンパイラに基づいて有効化されます。 まだ実行時にエラーが発生します。

```csharp
var customerQuery = from c in db.Customers
                    where (from o in db.Orders
                    where o.ShipCountry == “Germany”
                    select o.CustomerID).Contains(c.CustomerID);
```

このクエリは現在のデータ レイヤーでは処理できず、コンパイル時にエラーが診断されない間に、実行時にエラーが発生します。

### <a name="performance-penalty-with-linq"></a>LINQ によるパフォーマンスが低下

実行時には、ツリーの解析が行われ、適切なアクセス言語が生成されるときに、間接費のペナルティが支払われます。 予想通り、LINQ 式ツリーを分析する際にパフォーマンス ペナルティが発生します。 実際にデータをフェッチするために実行時に必要な時間は、C\# と LINQ間と X++ と `while select` 間の間で大きく異なりません。 主要な数値は、レコードがほとんどフェッチされない場合、X++ `while select` と比較して、C\# LINQ ではクエリの最初から最後までのパフォーマンスが約 3 倍長くなりそうなことを示しています。 ただし、多くのレコードがフェッチされる場合、合計時間は C\# と X++ の間でほぼ同じです。 結論として、言語ツリーを分析するよりも、多くのレコードを取得するほうが時間がかかります。

### <a name="composing-queries-with-linq"></a>LINQ を使用したクエリの作成

LINQ によって提供されるモデルでは、クエリをサブクエリで構成できます。 X++ 言語は、この機能を正しく提供することはできません。 これを理解するには、次の C\# LINQ コードを考えてみてください。 フラグは、データの結果の順序を制御するメソッドに渡されます。

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

### <a name="set-based-operations-with-linq"></a>LINQ を使ったセットに基づく操作

LINQ クエリは、CRUD 操作に対して適用できます。 ただし、レコードの更新、削除、挿入のモデルはセット ベース操作の式には役に立ちません。 現在、セットベース操作に変換される LINQ モデルに追加する拡張機能に取り組んできます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
