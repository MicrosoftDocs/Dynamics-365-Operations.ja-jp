---
title: 明細書を選択
description: この記事では、X++ 言語での select ステートメントについて説明します。
author: josaw1
ms.date: 08/27/2021
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 209a83c9ae9ba4681383c3ece2f411b5aad01df4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271351"
---
# <a name="select-statement"></a>明細書を選択

[!include [banner](../../includes/banner.md)]

**select** ステートメントは、データベースからデータをフェッチまたは操作します。

+ すべての **選択** ステートメントではレコードをフェッチするためテーブル変数を使用します。 この変数は、**select** 文を実行する前に宣言する必要があります。
+ **select** ステートメントは、レコードを 1 つだけ、またはフィールドをフェッチします。 複数のレコードをフェッチまたは移動したりするには、**next** ステートメントまたは **[while select](xpp-while-select.md)** ステートメントを使用できます。

    + **next** ステートメントは、テーブルの次のレコードをフェッチします。 **選択** ステートメントの前に、**次** ステートメントがある場合、エラーが発生します。 **次** ステートメントを使用する場合、**firstOnly** 検索オプションを使用しません。
    + **while select** ステートメントを使用して複数のレコードを移動する方がより適切です。

+ **select** ステートメントの結果はテーブル バッファ変数に返されます。
+ **選択** ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。

## <a name="select-example"></a>例の選択

次の例では、CustTable テーブルの最初の行のすべての列をフェッチし、その行の **AccountNum** 列に値を出力します。

```xpp
CustTable custTable;
select * from custTable;
info("AccountNum: " + custTable.AccountNum);
```

データ選択のその他の例については、[データの選択](xpp-select.md)を参照してください。

## <a name="insert-example"></a>例の挿入

次の例では、新しいレコードを CustTable テーブルに挿入します。 新しいレコードの **AccountNum** 列は **2000** に設定され、**CustGroup** 列は **1** に設定されます。 レコードの他のフィールドは空白になります。

```xpp
ttsBegin;
    CustTable custTable;
    select forUpdate custTable;
    custTable.AccountNum = '2000';
    custTable.CustGroup = '1';
    custTable.insert();
ttsCommit;
```

データの挿入に関するその他の例については、[データの挿入](xpp-insert.md) を参照してください。

## <a name="update-example"></a>例の更新

次の例では、更新する CustTable テーブルを選択します。 **AccountNum** フィールドの値が **2000** に等しいレコードのみが更新されます。 **next** への呼び出しはなく、この例では **select while** ステートメントを使用していないため、1 つのレコードのみが更新されます。 **CreditMax** フィールドの値が **5000** に変更されます。

```xpp
ttsBegin;
    CustTable custTable;
    select forUpdate custTable
        where custTable.AccountNum == '2000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

データの更新に関するその他の例については、[データの更新](xpp-update.md) を参照してください。

## <a name="delete-example"></a>例の削除

次の例では、**AccountNum** フィールドが **2000** である CustTable テーブルのすべてのレコードがデータベースから削除されます。 一度に 1 つのレコードが削除されます。

```xpp
ttsBegin;
    CustTable custTable;
    while select forUpdate CustTable
        where custTable.AccountNum == '2000'
    {
        custTable.delete();
    }
ttsCommit;
```

データの削除に関するその他の例については、[データの削除](xpp-select.md) を参照してください。

## <a name="syntax-of-the-select-statement"></a>Select ステートメントの構文

構文では次の記号が使用されています。

+ **\[\]** – かっこはオプションの要素を囲みます。
+ **{}** – 中かっこは、0 回以上含めることができる要素を囲みます。
+ **\+** – プラス記号は、1回以上含めることができる要素を示します。
+ **|** – バーはオプションを示します。

| 記号                | &nbsp;  | 式 |
|-----------------------|---|------------|
| *SelectStatement*     | = | *パラメーター* を **選択する** |
| *パラメーター*          | = | { *FindOption* } \[ *FieldList* **from** \] *TableBufferVariable* \[ *IndexClause* \] \[ *Options* \] \[ *WhereClause* \] \[ *JoinClause* \] |
| *FindOption*          | = | **crossCompany** \[**:** *ContainerVariable*\] \| **reverse** \| **firstFast** \| *FirstOption* \| **forUpdate** \| **noFetch** \| *ForceOption* \| **forceSelectOrder** \| **forceNestedLoop** \| *LockOption* \| **repeatableRead** \| **validTimeState** |
| *FirstOption*         | = | **firstOnly** \| **firstOnly10** \| **firstOnly100** \| **firstOnly1000** |
| *LockOption*          | = | **optimisticLock** \| **pessimisticLock** |
| *ForceOption*         | = | **forcePlaceholders** \| **forceLiterals** |
| *FieldList*           | = | { *フィールド* } \| **\*** |
| *フィールド*               | = | *集計* **(** *FieldIdentifier* **)** \| *FieldIdentifier* |
| *集計*           | = | **合計** \| **平均** \| **minof** \| **maxof** \| **集計** |
| *オプション*             | = | *OrderClause* \| *IndexClause* |
| *OrderClause*         | = | \[*OrderBy* \[*GroupBy*\]\] \| \[*GroupBy* \[*OrderBy*\]\] |
| *OrderBy*             | = | **order** \[**by**\] *FieldOrder* {**、** *FieldOrder* } |
| *GroupBy*             | = | **group** \[**by**\] *FieldOrder* {**、** *FieldOrder* } |
| *FieldOrder*          | = | *FieldIdentifier* \[ **asc** \| **desc** \] |
| *IndexClause*         | = | **インデックス** *IndexName* \| **インデックス ヒント** *IndexName* |
| *WhereClause*         | = | **where** *式* *InClause* |
| *InClause*            | = | **in** *リスト* |
| *JoinClause*          | = | \[**exists** \| **notexists** \| **outer** \] **join** *Parameters* |
| *ContainerVariable*   | = | コンテナー。 |
| *式*          | = | 式。 |
| *TableBufferVariable* | = | 結果の変数名。 |
| *FieldIdentifier*     | = | テーブルでのフィールドの名前。 |
| *IndexName*           | = | テーブルのインデックスの名前。 |
| *リスト*                | = | 値の配列。 |

## <a name="aggregate-functions"></a>集計関数

集計関数は、レコードのグループに対する単一のフィールドで計算を実行します。

+ 集計関数を実行したフィールドに結果が返されます。
+ 結果のフィールドは、**group by** 句の集計値とフィールドです。
+ 整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。
+ **sum** 関数が **null** を返す場合、行は返されません。

### <a name="differences-between-x-and-sql"></a>X++ と SQL 間の違い

業界標準の SQL では、データベース クエリに集計関数を含めることができます。 例では、**count(RecID)** および **sum(columnA)** があります。 集計関数が使用されるが、どの行も **WHERE** 句と一致しないときは、行は、集計の結果を保持するために行を返す必要があります。 返された行では、**count** 関数には **0** (ゼロ)、**sum** 関数には **null** が表示されます。 X++ はデータベースの **null** 値の概念をサポートしません。 したがって、**sum** 関数が **null** を返す場合、行はユーザーに返されません。 また、すべてのデータ型は、状況によっては **null** 値として処理される特定の値を持ちます。

## <a name="grouping-and-ordering-the-query-results"></a>クエリ結果のグループ化および順序付け

クエリは複数の **group by** 句を持つことができますが、フィールドは 1 つの **group by** 句のテーブル名で修飾できます。 テーブル名の修飾子を使用することをお勧めします。 **order by** 句は、**group by** と同じ構文パターンに従います。 両方の句が提供されている場合は、**join** (または **from**) 句の後に表示する必要があり、両方とも同じ **join** 句に存在する **where** 句よりも前にある必要があります。 すべての **group by**、**order by**、および **where** の各句を、最後の **join** 句のすぐ後に表示することをお勧めします。 次の例は、フィールドがテーブル名で修飾されている **group by** 句を示しています。

```xpp
CustTable custTable;
CustGroup custGroup;
struct groupSummary = new struct("int CustomerCount; str CustGroup");

while select count(CreditMax) from custTable
    join custGroup
    order by custGroup.Name
    group by custGroup.CustGroup
    where custTable.CustGroup == custGroup.CustGroup
        && custGroup.Name like "*Days*"
{

    groupSummary.value("CustomerCount", custTable.CreditMax);
    groupSummary.value("CustGroup", custGroup.CustGroup);
    info(groupSummary.toString());
}

// Example output:
// (CustomerCount:1; CustGroup:"1")
// (CustomerCount:3; CustGroup:"2")
```

## <a name="join-tables"></a>テーブルの結合

次の例は、**select** ステートメントの一部として内部結合を実行する方法を示しています。 この例では、**order by** 句も表示されており、各フィールドはテーブル名で修飾されています。 したがって、1 つの **order by** 句のみを使用して、取得したレコードのソート方法を制御することができます。

```xpp
CustTable custTable;
CustGroup custGroup;
struct output = new struct("int AccountNum; str CustGroup");

while select AccountNum from custTable
    join Name from custGroup
    order by custGroup.Name, custTable.AccountNum
    where custTable.CustGroup == custGroup.CustGroup
{
    info(custGroup.Name + ': ' + custTable.AccountNum);
}

// Example output:
// Days1: 6000
// Days1: 6001
// Days2: 5000
```

## <a name="using-where-order-by-and-index-hint-together-in-a-query"></a>クエリで where、order by、および index hint を一緒に使用する

返されるデータを並べ替えるには、**select** ステートメントで **order by** キーワードを使用します。 **index hint** キーワードを使用して、クエリで使用するインデックスを指定し、インデックスで定義された方法で選択したレコードを並び替えます。 インデックスは、レコードの選択を最適化します。 特定の順序でレコードを選択するには、**インデックス ヒント** キーワードを **並べ替え** の式と組み合わせます。 出力を逆順に並べ替えるには、**逆** キーワードを使用します。 テーブルのインデックスが無効になっている場合 (インデックスの **有効** プロパティが **いいえ** に設定されている場合)、索引を参照する **選択** ステートメントは引き続き有効です。 ただし、インデックスがデータベースに存在しないため、データベースはデータを並べ替えるヒントとしてインデックスを使用できません。 次のテーブルは、**select** ステートメントで **index hint** および **order by** キーワードを使用する方法を示しています。

| タスク | 明細書を選択 |
|------|-----|
| 注文が重要でない場合は、レコードを選択します。 | select .. where ... |
| 注文が重要な場合は、レコードを選択します。 | select .. order by ... where ... |
| レコードを選択し、特定のインデックスを強制的に使用します。 | select .. index hint ... where ... |
| 注文が重要な場合は、レコードを選択し、特定のインデックスを強制的に使用します。 | select .. index hint ... order by ... where ... |

次の例は、顧客の範囲と期日に基づいて、SalesTable テーブルからトランザクションを選択する方法を示しています。

```xpp
SalesTable salesTable;
select salesTable
    index hint CustIdx
    order by CustAccount
    where
        salesTable.CustAccount >= '3000'
        && salesTable.CustAccount <= '4000'
        && salesTable.FixedDueDate >= 12\12\2004
        && salesTable.FixedDueDate <= 05\05\2009;
```

## <a name="asc-keyword"></a>asc キーワード

**asc** キーワードは、**order by** または **group by** 句のオプションです。 昇順の並べ替え順序を指定します。 **昇順** または **降順** のどちらも指定されない場合、並べ替えは降順になります。

```xpp
CustTable custTable;
select * from custTable
    order by Value asc;
```

## <a name="avg-keyword"></a>avg キーワード

**avg** キーワードはフィールドの平均を返します。

```xpp
CustTable custTable;
select avg(Value) from custTable;
info(int642Str(custTable.Value));
```

## <a name="count-keyword"></a>count キーワード

**count** キーワードは、レコードの数を返します。

```xpp
CustTable custTable;
int64 iCountRows;
select count(RecID) from custTable;
iCountRows = custTable.RecID;
info('Rows: ' + int642Str(iCountRows));
```

## <a name="crosscompany-keyword"></a>crossCompany キーワード

**crossCompany** キーワードは、ユーザーが読み取りを承認されているすべての会社のデータを返します。 コンテナを追加して関連する会社の数を削減することができます。 次の例では、ユーザーが読み取りを承認されている会社のデータを返します。 結果は **dat** および **dmo** 会社に限定されます。

```xpp
CustTable custTable;
container conCompanies = ['dat','dmo'];
select crossCompany :conCompanies
    * from custTable;
```

### <a name="crosscompany-clause-can-contain-arbitrary-expressions"></a>crossCompany 句には任意の式を含めることができます

**crossCompany** 句は、検索ステートメントを考慮する必要のある会社を示すために **select** ステートメントで使用できます。 構文は、コンテナー型の変数である単一の識別子ではなく、コンテナー型の任意の式を許可するように拡張されています。

このコード例では、会社を含むコンテナーを作成します。

```xpp
private void SampleMethod()
{
    MyTable t;
    container mycompanies = ['dat', 'dmo'];
    select crosscompany: mycompanies t;
}
```

このコードでは、変数の代わりに式を使用します。

```xpp
private void SampleMethod()
{
    MyTable t;
    container mycompanies = ['dat', 'dmo'];
    select crosscompany: (['dat'] + ['dmo']) t;
}
```

## <a name="desc-keyword"></a>降順キーワード

**desc** キーワードは、**order by** または **group by** 句のオプションです。 降順の並べ替え順序を指定します。 **昇順** または **降順** のどちらも指定されない場合、並べ替えは降順になります。

```xpp
CustTable custTable;
select * from custTable
    order by Value desc;
```

## <a name="exists-keyword"></a>exists キーワード

**exists** キーワードは、ブール値と **結合** 句を返すメソッドです。

```xpp
CtrTable ctrTable;
CustTable custTable;
while select AccountNum, Value from custTable
    order by AccountNum
    exists join * from ctrTable
    where (ctrTable.AccountNum == custTable.AccountNum)
{
}
```

## <a name="firstfast-keyword"></a>firstFast キーワード

**Firstfast** キーワードは優先順位のヒントです。 最初の行はより迅速に表示されますが、このオプションの合計戻り時間は遅くなる場合があります。 **firstFast** ヒントは、すべてのページから自動的に発行されます。

次のコード例では、最初の行をすばやく返します。

```xpp
CustTable custTable;
select firstFast custTable
    order by AccountNum;
```

## <a name="firstonly-firstonly10-firstonly100-and-firstonly1000-keywords"></a>firstOnly、firstOnly10、firstOnly100、および firstOnly1000 キーワード

**firstOnly** キーワードは、限られた数の行を返すことによって、フェッチを高速化します。 クエリに **firstOnly** を含めると、ランタイムはテーブル バッファーを返します。 **firstOnly** を省略すると、レコードを反復処理できるオブジェクトがランタイムによって割り当てられます。 パフォーマンスの観点から、最初のレコードをフェッチすることを目的とする場合のみ **firstOnly** を使用する必要があります。

| キーワード       | 説明                |
|---------------|----------------------------|
| firstOnly     | 最初の行のみを返します。 |
| firstOnly10   | 10 行を返します。            |
| firstOnly100  | 100 行を返します。           |
| firstOnly1000 | 1,000 行を返します。         |

次のコード例では、結果の最初の行のみが返されます。

```xpp
CustTable custTable;
select firstOnly custTable
    index hint AccountIdx
    where custTable.AccountNum == '5000';
```

## <a name="forceliterals-keyword"></a>forceLiterals キーワード

**forceLiterals** キーワードは、最適化時に Microsoft SQL Server データベースに対して **where** 句で使用される実際値を明らかにするように、カーネルに指示します。 **forceLiterals** および **forcePlaceholders** キーワードは相互に排他的です。 詳細については、[forcePlaceholders キーワード](#forceplaceholders-keyword) セクションを参照してください。

> [!WARNING]
> **選択** 明細書に **forceLiterals** キーワードは使用しないでください。SQL インジェクションのセキュリティ脅威にさらされるためです。

## <a name="forcenestedloop-keyword"></a>forceNestedLoop キーワード

**forceNestedLoop** キーワードを使用すると、SQL Server データベースはネストループ アルゴリズムを使用して、結合アルゴリズムを含む特定の SQL ステートメントを処理します。 したがって、2 番目のテーブルのレコードがフェッチされる前に、1 番目のテーブルのレコードがフェッチされます。 通常、ハッシュ結合やマージ結合などの他の結合アルゴリズムが考慮されます。 このキーワードは、**forceSelectOrder** キーワードと組み合わされることがよくあります。

```xpp
CustGroup custGroup;
CustTable custTable;

while select forceNestedLoop custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    Info(custTable.CustGroup);
}
```

## <a name="forceplaceholders-keyword"></a>forcePlaceholders キーワード

**forcePlaceholders** キーワードは、最適化時に SQL Server データベースに対して **where** 句で使用される実際値を明らかに **しない** ように、カーネルに指示します。 既定では、この動作は **結合** ステートメントではないすべてのステートメントで使用されます。 このキーワードを使用する利点は、他の検索値がある同様の明細書のアクセス計画をカーネルが再利用できることです。 欠点は、アクセス計画が計算されても、データの配布が不均一になる可能性があるという事実が考慮されないことです。 アクセス計画は、平均的なアクセス計画です。 **forcePlaceholders** および **forceLiterals** キーワードは相互に排他的です。

次の例では、**CustTable** テーブルと結合されている **CustGroup** テーブルを反復処理します。

```xpp
CustGroup custGroup;
CustTable custTable;

while select forcePlaceholders custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    Info(custTable.CustGroup);
}
```

## <a name="forceselectorder-keyword"></a>forceSelectOrder キーワード

**forceSelectOrder** キーワードを指定すると、SQL Server データベースは指定した順序で結合内のテーブルにアクセスします。 2 つのテーブルが結合している場合、明細書の最初のテーブルに最初にアクセスします。 このキーワードは、**forceNestedLoop** キーワードと組み合わされることがよくあります。

次の例では、**CustGroup** フィールドの CustGroup および CustTable テーブルを結合します。

```xpp
CustGroup custGroup;
CustTable custTable;

while select forceSelectOrder custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    Info(custTable.CustGroup);
}
```

## <a name="forupdate-keyword"></a>forUpdate キーワード

**forUpdate** キーワードは、更新用にのみレコードを選択します。 基になるデータベースによっては、レコードが他のユーザーのためにロックされるかもしれません。 次の例では、**AccountNum** の値が **2000** であるレコードの更新のために、CustTable テーブルの **CreditMax** 列を選択します。

```xpp
ttsBegin;
    CustTable custTable;
    select forUpdate custTable
        where custTable.AccountNum == '2000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

## <a name="group-by-keyword"></a>group by キーワード

**group by** キーワードは、選択したレコードをフィールドごとにグループ化するようデータベースに指示します。

```xpp
CustTable custTable;
while select sum(CreditMax) from custTable
    group by CustGroup
{
    info(custTable.CustGroup + ' ' + int642Str(custTable.CreditMax));
}
```

## <a name="in-keyword"></a>in キーワード

**in** キーワードは、値がリストに含まれている行をフィルター処理します。

**in** キーワードを使用しない場合、記述するコードは次の例のようになります。

```X++
// This code doesn't use the in keyword.
private CostAmountStdAdjustment calcCostAmountStdAdjustment()
{
    InventSettlement inventSettlement;

    select sum(CostAmountAdjustment) from inventSettlement
        where inventSettlement.TransRecId == this.RecId
            && inventSettlement.Cancelled == NoYes::No
            && (inventSettlement.OperationsPosting == LedgerpostingType::purchStdProfit
                || inventSettlement.OperationsPosting == LedgerpostingType::purchStdLoss
                || inventSettlement.OperationsPosting == LedgerpostingType::InventStdProfit
                || inventSettlement.OperationsPosting == LedgerpostingType::InventStdLoss);

    return inventSettlement.CostAmountAdjustment;
}
```

**in** キーワードを使用する場合、記述するコードは次の例のようになります。

```X++
// This code uses the in keyword.
private CostAmountStdAdjustment calcCostAmountStdAdjustment()
{
    InventSettlement inventSettlement;
    container ledgerPostingTypes = this.ledgerPostingTypesForCostAmountStdAdjustmentCalculation();

    select sum(CostAmountAdjustment) from inventSettlement
        where inventSettlement.TransRecId == this.RecId
            && inventSettlement.Cancelled == NoYes::No
            && inventSettlement.OperationsPosting in ledgerPostingTypes;

    return inventSettlement.CostAmountAdjustment;
}

protected container ledgerPostingTypesForCostAmountStdAdjustmentCalculation()
{
return [
    LedgerPostingType::purchStdProfit,
    LedgerPostingType::PurchStdLoss,
    LedgerPostingType::InventStdProfit,
    LedgerPostingType::InventStdLoss
];
}
```

## <a name="index-keyword"></a>index キーワード

**index** キーワードは、選択されたレコードをインデックスで指定されたとおりに並べ替えるようデータベースに指示します。

```xpp
CustTable custTable;
while select AccountNum, Value from custTable
    index AccountIdx
{
    Info(custTable.AccountNum +  ": " + int642Str(custTable.Value));
}
```

## <a name="index-hint-keyword"></a>index hint キーワード

**index hint** キーワードは、特定のインデックスを使用して、選択されたレコードをインデックスで指定されたとおりに並べ替えるためのヒントをデータベースに提供します。 データベースはヒントを無視できます。 インデックス ヒントが正しくない場合はパフォーマンスに大きな影響を与えます。 インデックス ヒントは、動的な **where** 句または **order by** 句がない SQL ステートメント、およびヒントの効果を確認できる SQL ステートメントにのみ適用する必要があります。

クエリで **index hint** を使用する前に、テーブルで **allowIndexHint(true)** を呼び出す必要があります。 **index hint** の既定の動作 **false** であり、ヒントは無視されます。

> [!WARNING]
> **index hint** は慎重に注意して使用し、パフォーマンスが向上することが確実な場合にのみ使用してください。 **index hint** キーワードと API を使用すると、必要に応じて正しいヒントを渡すことができます。 疑問がある場合は、**index hint** の使用を避けてください。

次の例では、**AccountIdx** インデックスを使用して、クエリ内のレコードを CustTable テーブルで並べ替えます。

```xpp
str _accountNum = '111';
CustTable custTable;
custTable.allowIndexHint(true);

while select forUpdate custTable
    index hint AccountIdx
    where custTable.AccountNum == _accountNum
{
}
```

## <a name="join-keyword"></a>join キーワード

**join** キーワードは、両方のテーブルで共有される列のテーブルを結合するために使用されます。 SQL に見られるような **on** キーワードがないため、結合基準は **where** 句で指定されます。 このキーワードは、テーブルをループして関連テーブルのトランザクションを更新する場合に必要な SQL ステートメントの数を減らします。 たとえば、テーブル内の 500 のレコードを処理し、別のテーブルで関連するレコードを更新します。 入れ子になった **while select** を使用する場合、データベースへの 501 トリップがあります。 ただし、**結合** を使用する場合、データベースへのトリップは 1 回だけになります。

```xpp
CustTable custTable;
CustGroup custGroup;
int totalCredit;

while select custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    totalCredit += custTable.CreditMax;
}
}
```

## <a name="maxof-keyword"></a>maxof キーワード

**maxof** キーワードはフィールドの最大値を返します。

```xpp
CustTable custTable;
select maxof(CreditMax) from custTable;
info(int642Str(custTable.Value));
```

## <a name="minof-keyword"></a>minof キーワード

**minof** キーワードはフィールドの最小値を返します。

```xpp
CustTable custTable;
select minof(CreditMax) from custTable;
info(int642Str(custTable.Value));
```

## <a name="nofetch-keyword"></a>noFetch キーワード

**noFetch** キーワードは、今すぐレコードを取得する必要がないことを示します。 このキーワードは通常、**select** 文の結果を、実際のフェッチを実行するクエリなどの別のアプリケーション オブジェクトに渡すときに使用します。

次の例では、クエリ変数を作成しますがレコードはフェッチしません。

```xpp
CustTable custTable;
select noFetch custTable
    order by AccountNum;
```

## <a name="notexists-keyword"></a>notExists キーワード

転記がない場合にのみ、**notExists** キーワードが選択されます。

``` xpp
CustTable custTable;
CtrTable ctrTable;

while select AccountNum, Value from custTable
    order by AccountNum
    notExists join * from ctrTable
    where (ctrTable.AccountNum == custTable.AccountNum)
{
}
```

## <a name="optimisticlock-keyword"></a>optimisticLock キーワード

**optimisticLock** キーワードは、テーブルに異なる値が設定されていても、オプティミスティック同時実行制御を使用してステートメントを実行させます。

```xpp
CustTable custTable;
select optimisticLock custTable
    where custTable.AccountNum > '1000';
```

## <a name="order-by-keyword"></a>order by キーワード

**order by** キーワードは、選択されたレコードを **order by** リストのフィールドで並べ替えるようデータベースに指示します。 キーワード **by** はオプションです。

```xpp
CustTable custTable;
select * from custTable
    order by accountNum desc
    where custTable.AccountNum > '100';
info("AccountNum: " + custTable.AccountNum);
```

次の例では、CustTable テーブルの最も高い **AccountNum** 値を出力します。

```xpp
CustTable custTable;
select reverse custTable
    order by accountNum;
info("AccountNum: " + custTable.AccountNum);
```

## <a name="outer-keyword"></a>outer キーワード

**outer** キーワードは、最初に名前が付けられたテーブルからすべての行を返します。2 番目に名前が付けられたテーブルで一致するものがない行も返します。 この結合は左外部結合です。 既定値は、他の結合テーブルの一致する行から取得できなかったデータに置き換えられます。

**left** キーワードはなく、右外部結合もありません。

内部結合については、**on** 句でフィルター処理する場合の動作は **where** 句でフィルター処理する場合の動作と同じです。

```xpp
CustTable custTable;
CustGroup custGroupTable;

while select CustGroup from custGroupTable
    order by CustGroup
    outer join * from custGroupTable
    where custTable.CustGroup == custGroupTable.CustGroup
{
    Info(custTable.CustGroup + ', ' + custGroupTable.Name);
}
```

次の例は、2 つのテーブルに基づいています。 フィールド タイプとサンプル データが含まれています。 SalesOrder 親テーブルと SalesOrderLine 子テーブルの間には、一対多の関係があります。 SalesOrder テーブルの各行に対して、 SalesOrderLine テーブルには 0 (ゼロ) またはそれ以上の行があります。 SalesOrder テーブルには 2 つの行があります。

| SalesOrderID (整数、主キー) | DateAdded (日付) |
|-------------------------------------|------------------|
| 1                                   | 2010-01-01       |
| 2                                   | 2010-02-02       |

SalesOrderLine テーブルには、**SalesOrderID** という名前の外部キー フィールドが含まれています。 このフィールドは、SalesOrder テーブルの主キー列を参照します。 **2** の **SalesOrderID** 値は、SalesOrderLine テーブルのデータには発生しません。

| SalesOrderLineID (文字列、主キー) | 数量 (整数) | SalesOrderID (整数、外部キー) |
|----------------------------------------|--------------------|-------------------------------------|
| AA                                     | 32                 | 1                                   |
| BB                                     | 67                 | 1                                   |
| CC                                     | 66                 | 1                                   |

次のコードでは、**select** ステートメントで 2 つのテーブルを読み込みます。 **select** ステートメントには、左の **outer join** 句が含まれています。 結合基準とデータ フィルターは両方とも **where** 句にあります。 コードからの出力も表示されます。 出力の 2 番目のレコードには、値が **2** の **SalesOrderID** があります。 ただし、その値は SalesOrderLine テーブルに存在しません。 したがって、2 番目のレコードのフィールドの一部には、整数の場合は **0**、文字列の場合は長さゼロの文字列が既定値となります。

```xpp
SalesOrder recSalesOrder;
SalesOrderLine recSalesOrderLine;
struct struct4 = new struct
    ("int SalesOrderID;"
    + "date DateAdded;"
    + "str SalesOrderLineID;"
    + "int Quantity"
    );
while select *
    from
        recSalesOrder
        outer join recSalesOrderLine
    where
        recSalesOrder.SalesOrderID == recSalesOrderLine.SalesOrderID
        && recSalesOrderLine.Quantity == 66
{
    struct4.value("SalesOrderID", recSalesOrder.SalesOrderID);
    struct4.value("DateAdded", recSalesOrder.DateAdded);
    struct4.value("SalesOrderLineID", recSalesOrderLine.SalesOrderLineID);
    struct4.value("Quantity", recSalesOrderLine.Quantity);
    info(struct4.toString());
}

// Example output:
// (SalesOrderID:1; DateAdded:2010/1/1; SalesOrderLineID:"CC"; Quantity:66)
// (SalesOrderID:2; DateAdded:2010/2/2; SalesOrderLineID:""; Quantity:0)
```

## <a name="pessimisticlock-keyword"></a>pessimisticLock キーワード

**pessimisticLock** キーワードは、テーブルに異なる値が設定されていても、ペシミスティック同時実行制御を使用してステートメントを実行させます。

```xpp
CustTable custTable;
select pessimisticLock custTable
    where custTable.AccountNum > '1000';
```

## <a name="repeatableread-keyword"></a>repeatableRead キーワード

この **repeatableRead** キーワードは、他の取引が現在の取引内のロジックによって読み取られたデータを変更する前に、現在の取引を完了する必要があることを指定します。 明示的なトランザクションは **ttsAbort** または最も外側の **ttsCommit** のいずれかで完了します。 スタンドアロンの **select** 明細書では、トランザクション期間は **select** コマンドの期間です。 ただし、このキーワードがコードに表示されない場合でも、データベースは時に、個々の **選択** ステートメントの **repeatableRead** と同等のものを実施します。 (動作は、テーブルをスキャンするかどうかを決定するためにデータベースが使用する方法によって異なります。) 詳細については、基になるリレーショナル データベース製品のドキュメントを参照してください。

## <a name="reverse-keyword"></a>reverse キーワード

**reverse** キーワードは、逆の順序レコードを返します。

```xpp
CustTable custTable;
select reverse custTable
    order by AccountNum;
```

## <a name="sum-keyword"></a>sum キーワード

**sum** キーワードはフィールドの合計を返します。 すべてのアカウント、注文明細行などの合計を計算するために使用できます。

```xpp
CustTable custTable;
select sum(CreditMax) from custTable;
info(int642Str(custTable.Value));
```

## <a name="validtimestate-keyword"></a>validTimeState キーワード

**validTimeState** キーワードは、**ValidTimeStateFieldType** プロパティが **なし** 以外の値に設定されているテーブルの行を選択します。

```xpp
CustPackingSlipTransHistory history;
utcDateTime dateFrom, dateTo = DateTimeUtil::utcNow();
anytype recid = -1;
select
    validTimeState(dateFrom, dateTo)
    *
    from history;
recid = history.RecId;
info('RecId:' + int642Str(recid));
```

## <a name="where-keyword"></a>where キーワード

**where** キーワードは、式が **true** であるテーブルのからの行をフィルタ処理します。

次の例では、**AccountNum** の値が 100 を超える顧客を検索します。

```xpp
CustTable custTable;
select * from custTable
    where custTable.AccountNum > '100';
info("AccountNum: " + custTable.AccountNum);
```

次の例では、100 よりも大きい、最小の **AccountNum** 値を出力します。

```xpp
CustTable custTable;
select * from custTable
    order by accountNum
    where custTable.AccountNum > '100';
info("AccountNum: " + custTable.AccountNum);
```

次の例では、100 よりも大きい、最大の **AccountNum** 値を出力します。

```xpp
CustTable custTable;
select * from custTable
    order by accountNum desc
    where custTable.accountNum > "100";
info("AccountNum: " + custTable.AccountNum);
```

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
