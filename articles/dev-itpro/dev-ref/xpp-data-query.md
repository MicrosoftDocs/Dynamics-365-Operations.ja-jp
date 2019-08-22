---
title: X++ データの選択と操作
description: このトピックでは、X++ 言語でのデータの選択と操作のサポートについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150273
ms.assetid: 999a5ecf-559b-4d66-8b05-9a8e477e0518
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 7b7e9648c8e5b4da138db8a8f4c1451dd4f1f953
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833622"
---
# <a name="x-data-selection-and-manipulation"></a>X++ データの選択と操作

[!include [banner](../includes/banner.md)]

このトピックでは、X++ 言語でのデータの選択と操作のサポートについて説明します。

データベースに格納されているデータにアクセスして取得するため、SQL ステートメントを対話的またはソース コード内で使用することができます。 データの操作には、次のステートメントを使用します。

-   **選択** – 変更するデータを選択します。
-   **挿入** – 1 つ以上の新しいレコードをテーブルに追加します。
-   **更新** – 既存のテーブル レコードのデータを変更します。
-   **削除** – 既存のレコードをテーブルから削除します。

データを変更する前に、**選択**ステートメントを使用して更新するデータを選択する必要があります。 **select forUpdate** コマンドは、更新のためにのみレコードを選択します。 **insert**、**update**、**delete** ステートメントは、一度に 1 つのレコードに対して操作を実行します。 **array insert**、**insert\_recordset**、**RecordInsertList**、**update\_recordset** ステートメントは、同時に複数のレコードに対して操作を実行します。

## <a name="select-statements"></a>select ステートメント
**select** ステートメントは、データベースからデータをフェッチまたは操作します。 すべての**選択**ステートメントではレコードをフェッチするためテーブル変数を使用します。 この変数は、**select** 文を実行する前に宣言する必要があります。 **select** ステートメントは、レコードを 1 つだけ、またはフィールドをフェッチします。 追加のレコードを取得するには、**次** のステートメントを使用します。 **next** ステートメントは、テーブルの次のレコードをフェッチします。 **選択**ステートメントの前に、**次**ステートメントがある場合、エラーが発生します。 **次**ステートメントを使用する場合、**firstOnly** 検索オプションを使用しません。 複数のレコードを通過する必要がある場合は、**while** **select** ステートメントを使用する方がより適切です。 **select** ステートメントの結果はテーブル バッファ変数に返されます。 **選択**ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。 **sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。 整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。

## <a name="syntax-of-select-statements"></a>Select 文の構文

|                   |   |    |
|-------------------|---|----|
|*SelectStatement*  | = | <i>パラメーター</i>を**選択する**  |
|[*パラメーター*]       | = | **\[ \[** *FindOptions* **\]** **\[** *FieldList* **から \] \]** *TableBufferVariable* **\[** *IndexClause* **\]** **\[** *オプション* **\]** **\[** *WhereClause* **\]** **\[** *JoinClause* **\]** |
|*FindOptions*      | = | **crossCompany** \| **reverse** \| **firstFast** \| \[ **firstOnly** \| **firstOnly10** \| **firstOnly100** \| **firstOnly1000** \] \| **forUpdate** \| **noFetch** \| \[**forcePlaceholders** \| **forceLiterals**\] \| **forceselectorder** \| **forceNestedLoop** \| **repeatableRead** \| **validTimeState** |                                              |
|*FieldList*        | = | *フィールド* **{ ,** *フィールド* **}** \| * |
|*フィールド*            | = | *集計* **(** *FieldIdentifier***) |
|*集計*        | = | **合計** \| **平均** \| **minof** \| **maxof** \| **集計** |
|*オプション*          | = | \[ **order by**, **group by**, *FieldIdentifier* \[ **昇順** \| **降順** \] {, *FieldIdentifier* \[ **昇順** \| **降順** \] }] \| \[  *IndexClause* \]
|*IndexClause*      | = | **インデックス** *IndexName* \| **インデックス ヒント** *IndexName* |
|*WhereClause*      | = | **WHERE** *式* |
|*JoinClause*       | = | \[**exists** \| **notexists** \| **outer** ] **join**  *Parameters*|

### <a name="keywords-that-are-used-in-select-statements"></a>select ステートメントで使用されるキーワード

| キーワード           | 説明 |
|-------------------|-------------|
| asc               | このキーワードは、**order by** または **group by** のオプションです。 昇順の並べ替えを指定します。 **昇順**または**降順**のどちらも指定されない場合、並べ替えは降順になります。  |
| avg               | このキーワードはフィールドの平均を返します。|
| カウント             | このキーワードは、レコード数を返します。 |
| crossCompany      | このキーワードは、ユーザーが読み取りを承認されているすべての会社のデータを戻します。 コンテナを追加して関連する会社の数を削減することができます。  |
| desc              | このキーワードは、**order by** または **group by** のオプションです。 降順の並べ替えを指定します。 **昇順**または**降順**のどちらも指定されない場合、並べ替えは降順になります。 |
| exists            | このキーワードは、ブール値と**結合**句を返すメソッドです。 |
| firstFast         | このキーワードは優先順位のヒントです。 最初の行はより迅速に表示されますが、このオプションの合計戻り時間は遅くなる場合があります。 **firstFast** ヒントは、すべてのページから自動的に発行されます。 |
| firstOnly         | このキーワードを使用すると、最初の行のみを戻すことでフェッチを高速化できます。 |
| firstOnly10       | このキーワードは **firstOnly** と同じですが、1 つではなく 10 行を返します。 |
| firstOnly100      | このキーワードは **firstOnly** と同じですが、1 つではなく 100 行を返します。 |
| firstOnly1000     | このキーワードは **firstOnly** と同じですが、1 つではなく 1,000 行を返します。 |
| forceLiterals     | このキーワードは、最適化時に Microsoft SQL Server データベースに対して **where** 句で使用される実際値を明らかするように、カーネルに指示します。 **forceLiterals** および **forcePlaceholders** キーワードは相互に排他的です。 **選択** 明細書に **forceLiterals** キーワードは使用しないでください。SQL インジェクションのセキュリティ脅威にさらされるためです。|
| forceNestedLoop   | このキーワードを使用すると、SQL Server データベースはネストループ アルゴリズムを使用して、結合アルゴリズムを含む特定の SQL ステートメントを処理します。 したがって、2 番目のテーブルのレコードがフェッチされる前に、1 番目のテーブルのレコードがフェッチされます。 通常、ハッシュ結合やマージ結合などの他の結合アルゴリズムが考慮されます。 このキーワードは、**forceSelectOrder** キーワードと組み合わされることがよくあります。 |
| forcePlaceholders | このキーワードは、最適化時に SQL Server データベースに対して **where** 句で使用される実際値を明らかに*しない*ように、カーネルに指示します。 既定では、この動作は**結合**ステートメントではないすべてのステートメントで使用されます。 このキーワードを使用する利点は、他の検索値がある同様の明細書のアクセス計画をカーネルが再利用できることです。 欠点は、アクセス計画が計算されることですが、データの配布が不均一である可能性があることは考慮されません。 アクセス計画は、平均的なアクセス計画です。 **forcePlaceholders** および **forceLiterals** キーワードは相互に排他的です。 |
| forceSelectOrder  | このキーワードを指定すると、SQL Server データベースは指定した順序で結合内のテーブルにアクセスします。 2 つのテーブルが結合している場合、明細書の最初のテーブルに最初にアクセスします。 このキーワードは、**forceNestedLoop** キーワードと組み合わされることがよくあります。 |
| forUpdate         | このキーワードは、更新のみのレコードを選択します。 基になるデータベースによっては、レコードが他のユーザーのためにロックされるかもしれません。 |
| group by          | このキーワードは、選択したレコードをフィールドごとにグループ化するようデータベースに指示します。 |
| 指数             | このキーワードは、インデックスで定義された方法で選択されたレコードをソートするようにデータベースに指示します。 |
| index hint        | このキーワードは、インデックスで定義された方法で選択されたレコードをソートするために、データベースではインデックスを役立てます。 データベースはヒントを無視できます。 インデックス ヒントが正しくない場合はパフォーマンスに大きな影響を与えます。 インデックス ヒントは、動的な **where** 句または **order by** 句がない SQL ステートメント、およびヒントの効果を確認できる SQL ステートメントにのみ適用する必要があります。 |
| join              | このキーワードは、両方のテーブルで共有される列のテーブルを結合するために使用されます。 結合基準は、**on** 節に指定されていないため、**where** 節に指定されています。 このキーワードは、テーブルをループして関連テーブルのトランザクションを更新する場合に必要な SQL ステートメントの数を減らします。 たとえば、テーブル内の 500 のレコードを処理し、別のテーブルで関連するレコードを更新します。 入れ子になった **while select** を使用する場合、データベースへの 501 トリップがあります。 ただし、**結合**を使用する場合、データベースへのトリップは 1 回だけになります。 |
| maxof             | このキーワードはフィールドの最大値を返します。  |
| minof             | このキーワードはフィールドの最小値を返します。 |
| noFetch           | このキーワードは、今すぐレコードを取得する必要がないことを示します。 このキーワードは通常、**select** 文の結果を、実際のフェッチを実行するクエリなどの別のアプリケーション オブジェクトに渡すときに使用します。 |
| notExists         | 転記がない場合にのみ、このキーワードが選択されます。 |
| optimisticLock    | このキーワードは、テーブルに異なる値が設定されていても、オプティミスティック同時実行制御を使用してステートメントを実行させます。 |
| order by          | このキーワードは、選択されたレコードを**順**リストのフィールドでソートするようデータベースに指示します。 |
| outer             | このキーワードは、2 番目に名前が付けられたテーブルに行が一致しない場合でも、最初に名前が付けられたテーブルからすべての行を戻します。 **左**がなくても、この結合は左外部結合です。 右外部結合はありません。  |
| pessimisticLock   | このキーワードは、テーブルに異なる値が設定されていても、ペシミスティック同時実行制御を使用してステートメントを実行させます。  |
| repeatableRead    | このキーワードは、他の取引が現在の取引内のロジックによって読み取られたデータを変更する前に、現在の取引を完了する必要があることを指定します。 明示的なトランザクションは **ttsAbort** または最も外側の **ttsCommit** のいずれかで完了します。 スタンドアロンの **select** 明細書では、トランザクション期間は **select** コマンドの期間です。 ただし、このキーワードがコードに表示されない場合でも、データベースは時に、個々の**選択**ステートメントの **repeatableRead** と同等のものを実施します。 (動作は、テーブルをスキャンするかどうかを決定するためにデータベースが使用する方法によって異なります。) 詳細については、基になるリレーショナル データベース製品のドキュメントを参照してください。 |
| リバース           | レコードが逆の順序で返されます。  |
| sum               | このキーワードはフィールドの合計を返します。 すべてのアカウント、注文明細行などの合計を計算するために使用できます。 |
| validTimeState    | このキーワードは、**ValidTimeStateFieldType** プロパティが**なし**以外の値に設定されているテーブルの行をフィルタリングします。 |

#### <a name="keyword-examples"></a>キーワードの例

```X++
// asc keyword example.
select * from custTable
    order by Name asc;

// avg keyword example. 
CustTable custTable;;
select avg(value) from custTable;
print custTable.value;

// count keyword example. 
CustTable xCT;int64 iCountRows; ;
Select COUNT(RecID) from xCT;
iCountRows = xCT.RecID;

// crossCompany keyword example.
CustTable custTable;
container conCompanies = ['dat','dmo'];
select crossCompany :conCompanies
    * from custTable;

// desc keyword example.
select * from custTable
    order by Name desc;

// exists keyword example. 
while select AccountNum, Name from custTable
    order by AccountNum
    exists join * from ctr
    where (ctr.AccountNum ==
        custTable.AccountNum)

// firstFast keyword example.
select firstFast custTable
    order by AccountNum;

// firstOnly keyword example.
static InventTable find(ItemIditemId, boolean update = false)
{
    InventTable inventTable;
    inventTable.selectForUpdate(update);
    if (itemId)
    {
        select firstonly inventTable
            index hint ItemIdx
            where inventTable.itemId == itemId;
    }
    return inventTable;
}

// forceNestedLoop keyword example.
while select forceSelectOrder
    forceNestedLoop inventTransThis
index hint TransIdIdx
where inventTransThis.InventTransId
    == inventTrans.InventTransId
    && inventTransThis.StatusIssue
    <= StatusIssue::ReservOrdered

// forcePlaceholders keyword example.
static void forcePlaceHoldersExample(Args _args){
    SalesTable salesTable;
    SalesLine salesLine;
    while select forcePlaceholders salesLine
        join salesTable
            where salesTable.SalesId ==
                salesLine.SalesId
                && salesTable.SalesId == '10'
    {
        //more code
    }
}

// forceSelectOrder keyword example.
display ForecastHasPurch hasForecastPurch(){
    ForecastPurch forecastPurch;
    InventDim nventDim;
select firstOnly forcePlaceholders
    forceSelectOrder recId
    from forecastPurch
    index hint ItemIdx
    where forecastPurch.itemId == this.itemId
exists join inventDim
    index hint DimIdIdx
    where inventDim.inventDimId == forecastPurch.inventDimId
        && inventDim.configId == this.configId;
    return forecastPurch.recId;
}

// forUpdate keyword example.
ttsBegin; while select forUpdate ledgerJournalTrans
    index hint NumVoucherIdx
    where ledgerJournalTrans.journalNum ==
    _journalNum &&
    ledgerJournalTrans.voucher == _voucher
{
    ledgerJournalTrans.doDelete();
    counter++;
}
if (counter
    && ledgerJournalTable.journalType
    != LedgerJournalType::Periodic)
{
    NumberSeq::release(
        ledgerJournalTable.voucherSeries,
        _voucher);
}
ttsCommit;

// group by keyword example.
CustTable custTable;;
while select sum(CreditMax) from custTable
    group by CustGroup
{
    print custTable.CustGroup, " ",custTable.CreditMax;
}

// index keyword example.
CustTable custTable;;
while select AccountNum, Name from custTable
    index AccountIdx
{
    print custTable.AccountNum, " ", custTable.Name;
}

// index hint keyword example.
while select forUpdate ledgerJournalTrans
    index hint NumVoucherIdx
    where ledgerJournalTrans.journalNum
        == _journalNum

// join keyword example.
while select ledgerTable
    join ledgerTrans
    where ledgerTrans.accountNum == ledgerTable.accountNum
{
    amountMST += ledgerTrans.amountMST;
}

// maxof keyword example.
CustTable custTable;;
select maxof(CreditMax) from custTable;

// minof keyword example.
CustTable custTable;;
select minof(CreditMax) from custTable;

// noFetch keyword example.
select noFetch custTable
    order by AccountNum

// notExists keyword example.
while select AccountNum, Name from custTable
    order by AccountNum
    notExists join * from ctr
    where (ctr.AccountNum ==
        custTable.AccountNum)

// optimisticLock keyword example.
select optimisticLock custTable
    where custTable.AccountNum > '1000'

// order by keyword example.
select * from custTable
    order by accountNum desc
    where custTable.AccountNum > "100";

// outer keyword example.
while select AccountNum
    from custTable
    order by AccountNum
    outer join * from custBankAccount
    where custBankAccount.AccountNum ==
        custTable.AccountNum
{
    print custTable.AccountNum,
    " , ", custBankAccount.DlvMode;
} 

// pessimisticLock keyword example.
select pessimisticLock custTable
    where custTable.AccountNum > '1000';

// reverse keyword example.
select reverse custTable
    order by AccountNum;

// sum keyword example.
CustTable custTable;;
select sum(CreditMax) from custTable;

// validTimeState keyword example.
static void VtsJob1(Args _args)
{
    // A validTimeState table.
    CustPackingSlipTransHistory xrec1;
    utcDateTime myDateFrom , myDateTo;
    anytype myAnytype = -1;
    myDateFrom = DateTimeUtil::utcNow();
    myDateTo = myDateFrom;
    SELECT
        validTimeState(myDateFrom, myDateTo)
            *
            FROM xrec1;
    myAnytype = xrec1.getFieldValue("RecId");
    info(myAnytype);
}
```

## <a name="select-statement-examples"></a>select ステートメントの例
次の例では、**select** ステートメントの使用方法を示しています。

```X++
CustTable custTable;
// A customer is found and returned in custTable
select * from custTable;
info("A: " + custTable.AccountNum);

// A customer with account number > "100" is found
select * from custTable
    where custTable.AccountNum > "100";
info("B: " + custTable.AccountNum);

// Customer with the lowest account number > "100" found:
select *
    from custTable 
    order by accountNum
    where custTable.AccountNum > "100";
info("C1: " + custTable.AccountNum);

// The next customer is read
next custTable;
info("C2: " + custTable.AccountNum);

// Customer with highest account number
// (greater than 100) found: Fourth Coffee
select *
    from custTable 
    order by accountNum desc
    where custTable.accountNum > "100";
info("D1: " + custTable.AccountNum);

// The next record is read (DESC): Fabrikam, Inc.
next custTable;
info("D2: " + custTable.AccountNum);

// Customer with highest account number found: Fourth Coffee
select reverse custTable
    order by accountNum;
info("E: " + custTable.AccountNum);

// Customer with "lowest" name and account number
// in the interval 100 to 1000 is found. This is Coho Winery.
select *
    from custTable
    order by DlvMode
    where custTable.accountNum > "100"
        && custTable.accountNum < "1000";
info("F: " + custTable.AccountNum);

// The count select returns the number of customers.
select count(AccountNum)
    from custTable;

// Prints the result of the count
info(strFmt("G: %1 = Count of AccountNums", custTable.accountNum));

// Returns the average credit max for non-blocked customers.
select avg(CreditMax)
    from custTable
    where custTable.blocked == CustVendorBlocked::No;

// Prints the result of the avg
info(strFmt("H: %1 = Average CreditMax", custTable.CreditMax));

/*** Display from infolog:
Message (02:00:34 pm)
A: 4000
B: 4000
C1: 4000
C2: 4001
D1: 4507
D2: 4506
E: 4507
F: 
G: 29 = Count of AccountNums
H: 103.45 = Average CreditMax
***/
```

### <a name="join-example"></a>join の例

次の例は、SQL **select** ステートメントの一部として内部結合を実行する方法を示しています。 この例では、**order by** 句も表示されており、各フィールドはテーブル名で修飾されています。 したがって、1 つの **order by** 句のみを使用して、取得したレコードのソート方法を制御することができます。

```X++
CustTable xrecCustTable;
CashDisc xrecCashDisc;
struct sut4;
sut4 = new struct("str AccountNum; str CashDisc; str Description");
while select firstOnly10 *
    from xrecCustTable
    order by xrecCashDisc.Description
    join xrecCashDisc
    where xrecCustTable.CashDisc ==
        xrecCashDisc.CashDiscCode
        && xrecCashDisc.Description LIKE "*Days*"
    {
        sut4.value("AccountNum", xrecCustTable.AccountNum );
        sut4.value("CashDisc", xrecCashDisc.CashDiscCode );
        sut4.value("Description", xrecCashDisc.Description );
        info(sut4.toString());
    }
/*********  Actual Infolog output
Message (02:29:37 pm)
(AccountNum:"1101"; CashDisc:"0.5%D10"; Description:"0.5% 10 days")
(AccountNum:"4001"; CashDisc:"0.5%D10"; Description:"0.5% 10 days")
(AccountNum:"1102"; CashDisc:"0.5%D30"; Description:"0.5% 30 days")
(AccountNum:"1201"; CashDisc:"0.5%D30"; Description:"0.5% 30 days")
(AccountNum:"2211"; CashDisc:"0.5%D30"; Description:"0.5% 30 days")
(AccountNum:"1202"; CashDisc:"1%D15"; Description:"1% 15 days")
(AccountNum:"1203"; CashDisc:"1%D07"; Description:"1% 7 days")
(AccountNum:"2212"; CashDisc:"1%D07"; Description:"1% 7 days")
(AccountNum:"2213"; CashDisc:"1%D07"; Description:"1% 7 days")
(AccountNum:"2214"; CashDisc:"1%D07"; Description:"1% 7 days")
*********/
}
```

### <a name="group-by-and-order-by-example"></a>group by および order by の例

次の例は、**group by** 句のフィールドをテーブル名で修飾できることを示しています。 複数の **group by** 句が存在する場合があります。 ただし、フィールドは 1 つの **group by** 句のみのテーブル名により限定されます。 テーブル名の修飾子を使用することをお勧めします。 **order by** 句は、**group by** と同じ構文パターンに従います。 両方の句が提供されている場合は、**join** (または **from**) 句の後に表示する必要があり、両方とも同じ **join** 句に存在する **where** 句よりも前にある必要があります。 すべての **group by**、**order by**、および**where** の各句を、最後の **join** 句のすぐ後に表示することをお勧めします。

```X++
CustTable xrecCustTable;
CashDisc xrecCashDisc;
struct sut4;
sut4 = new struct("str AccountNum_Count; str CashDisc; str Description");
while select count(AccountNum)
    from xrecCustTable
    order by xrecCashDisc.Description
    join xrecCashDisc
        group by xrecCashDisc.CashDiscCode
            where xrecCustTable.CashDisc ==
                xrecCashDisc.CashDiscCode
                && xrecCashDisc.Description LIKE "*Days*"
    {
        sut4.value("AccountNum_Count", xrecCustTable.AccountNum );
        sut4.value("CashDisc", xrecCashDisc.CashDiscCode );
        sut4.value("Description", xrecCashDisc.Description );
        info(sut4.toString());
    }
/*********  Actual Infolog output
Message (02:45:26 pm)
(AccountNum_Count:"2"; CashDisc:"0.5%D10"; Description:"")
(AccountNum_Count:"3"; CashDisc:"0.5%D30"; Description:"")
(AccountNum_Count:"4"; CashDisc:"1%D07"; Description:"")
(AccountNum_Count:"1"; CashDisc:"1%D15"; Description:"")
(AccountNum_Count:"1"; CashDisc:"2%D30"; Description:"")
(AccountNum_Count:"1"; CashDisc:"3%D10"; Description:"")
*********/
}
```

### <a name="select-statement-that-has-an-outer-join"></a>外部結合を持つ select ステートメント

**select** ステートメントは、**where** 句において外部結合のフィルター処理をサポートします。 標準 SQL の **join** 句には、フィルター基準の **on** キーワードがあります。 ただし、このキーワードは X++ でサポートされていません。 内部結合は、その他の連結テーブルの行に一致しないすべてのテーブル行を拒否します。 ただし、他の連結テーブルに一致する行がない場合でも、外部結合には最初のテーブルからの行が含まれます。 既定値は、他の結合テーブルの一致する行から取得できなかったデータに置き換えられます。 **join** 句の一部である **on** 句に相当する、outer join をフィルター処理することができます。 内部結合については、**on** 句でフィルター処理する場合の動作は **where** 句でフィルター処理する場合の動作と同じです。

#### <a name="select-statement-example"></a>select ステートメントの例

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

```X++
static void SelectOuterJoinExample(Args _args)
{
    SalesOrder recSalesOrder;
    SalesOrderLine recSalesOrderLine;
    struct struct4;

    struct4 = new struct
        ("int SalesOrderID;"
        + "date DateAdded;"
        + "str SalesOrderLineID;"
        + "int Quantity"
        );
    while
    select
        *
        from
            recSalesOrder
            OUTER JOIN recSalesOrderLine
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
}
/*********  Actual Infolog output (with break spaces entered in between each output)
(SalesOrderID:1;
DateAdded:2010/1/1;
SalesOrderLineID:"CC";
Quantity:66)
(SalesOrderID:2;
DateAdded:2010/2/2;
SalesOrderLineID:"";
Quantity:0)
*********/
```

## <a name="while-select-statements"></a>while select ステートメント
**while select** ステートメントは、データの処理に使用されます。 **select** ステートメントの最も広く使用されている形式です。 **while select** ステートメントは、特定の基準を満たす多くのレコードをループし、各レコードでステートメントを実行することができます。 通常、データ操作のために **while select** 文を使用する場合、トランザクション内でデータ整合性を確保するために使用します。 **while select** ステートメントの結果はテーブル バッファ変数に返されます。 **選択**ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。 **sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。 整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。 **while select** ステートメントの構文は、**select** ステートメントの構文に似ていますが、このステートメントは**select** ではなく **while select** により処理されます。 **select** ステートメント自体は、ループのステートメントの最初の繰り返しの直前に 1 回だけ実行されます。 **while select** に追加されたブール式 (**iCounter &lt; 1** など) は 1 度だけテストされます。 この動作は、C ++ や C\# などの言語の **while** 文の動作とは異なります。 たとえば、次のループは、複数回繰り返します。

```X++
static void JobWhileSelect(Args _args)
{
    int iCounter = 0;
    BankAccountTable xrecBAT;
    while select * from xrecBAT
        where iCounter < 1
    {
        iCounter++;
        Global::info(strFmt("%1 , %2", iCounter, xrecBAT.AccountID));
    }
}

/*** Display from infolog:
Message (04:59:38 pm)
1 , Cash1
2 , STB-DKK
3 , STB-EUR
***/
```

### <a name="while-select-example"></a>while select の例

次の例では、アカウント番号が指定された範囲内にある CustTable テーブルのすべての顧客のアカウント番号と売上グループを出力します。

```X++
static void JobPrintTel(Args _args)
{
    CustTable xrecCT;
    while select xrecCT
        order by xrecCT.AccountNum
            where  xrecCT.AccountNum >= "4010"
                && xrecCT.AccountNum <= "4100"
    {
        Global::info(strFmt("%1 , %2",
            xrecCT.AccountNum, xrecCT.SalesGroup));
    }
}

/*** Display from Infolog:
Message (06:04:03 pm)
4010 , CSG-EU
4011 , CSG-EU
4012 , CSG-OTH
4013 , CSG-OTH
4014 , CSG-OTH
4015 , CSG-OTH
4016 , CSG-EU
4017 , CSG-EU
4018 , CSG-EU
4020 , 
4024 , 
***/
```

### <a name="while-select-example"></a>while select の例

次の例では、**forUpdate** キーワードを使用しています。

```X++
static void LedgerJob(Args _args)
{
    LedgerJournalTrans ledgerJournalTrans;
    LedgerJournalTable ledgerJournalTable;
    LedgerJournalId    jnJournalNum;
    Voucher            vVoucher;
    Counter            counter = 0;
    jnJournalNum = "999999_999"; //"000012_003";
    vVoucher = "88888_888"; //"00001_IRG";
    ledgerJournalTable =
        ledgerJournalTable::find(jnJournalNum);
    ttsBegin;
    while select forUpdate ledgerJournalTrans
        index hint NumVoucherIdx
            where ledgerJournalTrans.journalNum == jnJournalNum
                && ledgerJournalTrans.voucher == vVoucher
    {
        ledgerJournalTrans.doDelete();
        counter++;
    }
    //NumberSeq updates needed?
    ttsCommit;
    Global::info(strFmt("counter = %1", counter));
}
```

### <a name="deleting-a-set-of-records"></a>レコードのセットを削除します

**while select** ステートメントを使用して一部の基準を満たすレコードのセットを確認し、各レコードでアクションを実行することができます。 次の例では、ステートメントを使用して一連のレコードを削除します。

```X++
TableName myXrec;
while select myXrec where conditions // conditions is a Boolean variable defined elsewhere.
{
    myXrec.delete();
}
```

同じ効果は **delete\_from** キーワードを使用して達成することができます。

```X++
TableName myXrec;
delete_from myXrec where conditions; // conditions is a Boolean variable defined elsewhere.
```

### <a name="select-statements-on-fields"></a>フィールド上の select ステートメント

**select** ステートメントをフィールド上のルックアップで使用することができます。 テーブルのレコードをフェッチする**選択**ステートメントの後、**.fieldName** を入力してテーブルのフィールドを参照することができます。 これらの **select** ステートメントは、式で使用する必要があります。 *通常の **select** ステートメント* は *フィールド **select** ステートメント* と異なります:

-   フィールド **select** ステートメントはテーブル上で直接動作します。
-   通常の **select** ステートメントは、テーブル バッファ変数で動作します。

### <a name="select-field-example"></a>フィールド例を選択

```X++
void selectFieldExamples ()
{
    // Prints the NameRef field from the selected customer
    print (select CustTable order by AccountStatement).AccountStatement;

    // Uses the balance field from the customer with AccountNum 3000
    if ((select custTable where CustTable.AccountNum == '3000').CreditMax < 50000)
        print "This customer has a credit maximum less than $50,000.";
}
```

### <a name="aggregate-functions-differences-between-x-and-sql"></a>集計関数: X++ および SQL の差額

業界標準の SQL では、データベース クエリに*集計関数*を含めることができます。 例では、**count(RecID)** および **sum(columnA)** があります。 集計関数が使用されるが、どの行も **WHERE** 句と一致しないときは、行は、集計の結果を保持するために行を返す必要があります。 返された行では、**count** 関数には **0** (ゼロ)、**sum** 関数には **null** が表示されます。 X++ はデータベースの **null** 値の概念をサポートしません。 したがって、**sum** 関数が **null** を返す場合、行はユーザーに返されません。 また、すべてのデータ型は、状況によっては **null** 値として処理される特定の値を持ちます。

### <a name="index-and-order-by-keywords-in-select-statements"></a>select ステートメント内の index および order by キーワード

返されるデータを並べ替えるには、**select** ステートメントで **order by** キーワードを使用します。 **index hint** キーワードを使用して、クエリで使用するインデックスを指定し、インデックスで定義された方法で選択したレコードをソートします。 インデックスは、レコードの選択を最適化します。 特定の順序でレコードを選択するには、**インデックス ヒント**キーワードを**並べ替え**の式と組み合わせます。 出力を逆順に並べ替えるには、**逆**キーワードを使用します。 テーブルのインデックスが無効になっている場合 (インデックスの**有効**プロパティが**いいえ**に設定されている場合)、索引を参照する**選択**ステートメントは引き続き有効です。 ただし、インデックスがデータベースに存在しないため、データベースはデータを並べ替えるヒントとしてインデックスを使用できません。 次のテーブルは、**select** ステートメントで **index hint** および **order by** キーワードを使用する方法を示しています。

| タスク                                                                                 | 使用                                   |
|--------------------------------------------------------------------------------------|---------------------------------------|
| 注文が重要でない場合は、レコードを選択します。                                     | select .. where ...                   |
| 注文が重要な場合は、レコードを選択します。                                        | select .. order by ... where ...      |
| レコードを選択し、特定のインデックスを強制的に使用します。                               | select .. index hint ... where ...    |
| 注文が重要な場合は、レコードを選択し、特定のインデックスを強制的に使用します。 | select .. index hint ... order by ... where ... |

### <a name="index-and-order-by-example"></a>index および order by の例

次の例は、顧客の範囲と期日に基づいて、SalesTable テーブルからトランザクションを選択する方法を示しています。

```X++
SalesTable salesTable;
    select salesTable
    index hint CustIdx
    order by CustAccount
    where salesTable.CustAccount >= '3000'
        && salesTable.CustAccount <= '4000'
        && salesTable.FixedDueDate >= 12\12\2004
        && salesTable.FixedDueDate <= 05\05\2009;
```

### <a name="index-hint"></a>index hint

クエリの**インデックス ヒント**を使用する前に、サーバー上で使用できるヒントを指定する必要があります。

1.  **スタート**&gt; **管理ツール** &gt; **Microsoft Dynamics AX サーバー コンフィギュレーション**に移動します。
2.  **データベースのチューニング** タブで、**クエリで INDEX のヒントを許可する** を選択し、**OK** をクリックします。
3.  Application Object Server (AOS) サービスの再起動を要求するメッセージ ボックスが表示されたら、**はい** をクリックします。 サービスが再起動されるまで、インデックス ヒントは有効化されません。

**SELECT** ステートメント内の **インデックス ヒント** が非クラスター化インデックスを参照し、**WHERE** 句に同じテーブルのクラスタ化インデックスに存在するフィールドのみが含まれているときは、ヒントで指定されているインデックスではなく、クラスタ化インデックスが使用されます。 たとえば、SQL Server Management Studio で **sp\_helpindex InventTable** を実行し、InventTable テーブルが **DataAreaId** および **ItemId** 列でクラスター インデックスを、さらに **DataAreaId**、**ItemProductId**、および **ItemType** 列で非クラスター化インデックスを持っていることを確認します。

| インデックス名       | 説明                                        | キーの列                         |
|------------------|----------------------------------------------------|-------------------------------------|
| I\_175ITEMIDX    | プライマリにあるクラスタ化された一意の主キー | DATAAREAID、ITEMID                  |
| I\_175PRODUCTIDX | 非集合、プライマリに配置                  | DATAAREAID、ITEMPRODUCTID、ITEMTYPE |

次のコードでは、**インデックス ヒント**で指定される非クラスター化インデックスではなく、クラスター化インデックスが使用されます。

```X++
static void IndexHint(Args _args)
{
    InventTable inv;
    select * from inv index hint GroupItemIdx
        where inv.ItemId == 'B-R14';
}
```

### <a name="writing-a-select-statement-as-an-expression"></a>選択したステートメントを式として記述

**select** ステートメントを式として使用することができます。 このタイプの **select** ステートメントは *式 **select** ステートメント* と呼ばれます。 テーブル バッファ変数は、式 **select** ステートメントで使用できません。 テーブルの名前は、**from** 句で使用する必要があります。 式**選択**明細書の 1 つの制限は、**結合**キーワードが式結合でサポートされていないことです。

### <a name="expression-select-examples"></a>式選択の例

次の例では、かっこ内の **select** ステートメントは 1 つの行を返します。 データを取り込むことができる唯一の列は、**select** 句の **from** 句の前に名前が付けられている列です。 閉じ括弧の後に、その列の名前を使用してデータ値を参照します: **).AccountNum;**。 この例は、**firstonly** キーワードを使用するため、最大で 1 行を返します。 ただし、**firstonly** キーワードが省略されるとしても **sAccountNum** に割り当てられる値は同じです。 この例の **where** 句には、**where** 句が **order by** 句の後に配置されるべきであることを示し以外の目的がありません。 **order by** 句でフィールド名を修飾するために、テーブル名を使用することはできません。

```X++
int64 nRecId, nCount;
str sAccountNum, sName;
sAccountNum = (select firstonly AccountNum from CustTable
    order by AccountNum desc
    where 0 == 0 // 'where' must occur after 'order by'. )
    .AccountNum;
info(strFmt("Test_1.a: %1", sAccountNum));
```

前の例と同じ結果を達成する単純な方法を次に示します。

```X++
/********* Actual Infolog output
 Test_1.a: 4507Test_1.b: 4507
 *********/

int64 nRecId, nCount;
str sAccountNum, sName;
sAccountNum = (select maxof(AccountNum) from CustTable).AccountNum;
info(strFmt("Test_1.b: %1", sAccountNum));
```
次の例には、**where** 句が含まれています。 **where** 句では、テーブル名をフィールドの修飾子として使用する必要があります。 ここで、**maxof** 集計関数が使用され、**RecId** フィールドが機能に記載されます。 集計関数に記載されているフィールドは、閉じかっこの後のデータ値を参照するために使用されるフィールド名と同じでなければなりません。 それ以外の場合、空のデータが返されます。

```X++
int64 nRecId, nCount;
str sAccountNum, sName;
nRecId = (select maxof(RecId) from CustTable
    where CustTable.Blocked == CustVendorBlocked::No)
    .RecId;
info(strFmt("Test_2.c: %1", nRecId));

/********* Actual Infolog output
Test_2.c: 5637144604
*********/
```

次の例では、フィールド名 (この場合は **RecId**) は **RecId** の値ではないデータ値を参照するために使用します。 **count** 集計関数は、**RecId**値を返しません。 **RecId** フィールドは通常 **cound** 関数と共に使用されます。

```X++
int64 nRecId, nCount;
str sAccountNum, sName;
nRecId = (select count(RecId) from CustTable
    where CustTable.Blocked == CustVendorBlocked::No)
    .RecId;
info(strFmt("Test_2.d: %1", nRecId));

/********* Actual Infolog output
Test_2.d: 29
*********/
```

**join** キーワードは、式 **select** ステートメントでサポートされていません。 次の例は、サブセレクトを示しています。 ただし、式選択の**ステートメント**は、標準の内部結合に相当するサブセレクトをサポートしていません。 したがって、次の例では、1 つの式 **select** ステートメント内 (つまり、副選択内) に 2 つのテーブルが記述されているため、コンパイルは行われません。 この例に示すように、サブセレクトはサポートされていますが、制限された方法でのみサポートされます。

```X++
// This job does not compile.
static void BadJob(Args _args)
{
    sName = (select Name from AssetTable
        where AssetTable.AssetId ==
            // Here starts the subselect.
            (select AssetId from AssetTrans
                where AssetTrans.AssetId ==
                    AssetTable.AssetId // Compiler rejects this line.
            ).AssetId).Name;
    info(strFmt("Test_3: %1", sName));
}

/********* Actual Infolog output
Test_3: CNC-Metal shade
*********/
```

## <a name="update-method"></a>update メソッド
**update** テーブル メソッドは、バッファーの内容で現在のレコードを更新します。 また、適切なシステム フィールドも更新されます。 **where** 句はオプションです。 これが使用されるとき、**WHERE** 句は、テーブルの各行を処理するときに **更新** でテストされる条件を指定します。 その条件に対する **true** をテストする行のみ新しい値で更新されます。 **update\_recordset** 演算子は、同時に複数のレコードを更新するレコード セット ベースの演算子です。 **update** の動作をオーバーライドするには、**doUpdate** メソッドを使用します。 次の例では、更新する custTable テーブルを選択します。 **AccountNum** フィールドの値が **4000** に等しいレコードは更新されます。 (この場合、レコードは 1 つだけ更新されます。) **CreditMax** フィールドの値は **5000** に変更されます。

```X++
CustTable custTable;
ttsBegin;
    select forUpdate custTable
    where custTable.AccountNum == '4000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

## <a name="doupdate-method"></a>doUpdate メソッド
**doUpdate** メソッドは、バッファーの内容で現在のレコードを更新します。 このメソッドでは、適切なシステム フィールドも更新されます。 テーブルでの **更新** メソッドをバイパスする必要があるときは、**doUpdate** メソッドを使用する必要があります。 **doUpdate** テーブル メソッドの構文は、**void doUpdate()** です。 次の例では、**CreditMax** フィールドの値は 1,000 ずつ増加します。

```X++
static void Job1(Args _args)
{
    CustTable custTable;
    ttsBegin;
    select forUpdate custTable
    where custTable.CreditMax == 3000;
    if (custTable)
    {
        custTable.CreditMax += 1000;
        custTable.doUpdate();
    }
    ttsCommit;
}
```

## <a name="delete-method"></a>delete メソッド
**削除** テーブル メソッドは、データベースから現在のレコードを削除します。 このメソッドを使用するには、**where** 句を使用して削除する行を指定します。 一度に 1 つのレコードが、指定されたテーブルから削除されます。 **delete\_from** 演算子は、同時に複数のレコードを削除するレコード セット ベースの演算子です。 **delete** メソッドは上書きすることができます。 たとえば、レコードが削除される前に、追加の検証を追加する場合があります。 **削除**方法をオーバーライドする場合、**doDelete** を呼び出すことで、**削除**メソッドの元の (ベース) バージョンを実行できます。 したがって、**doDelete** メソッドへの呼び出しは**delete** メソッドの **super()** への呼び出しに相当します。 次の例では、**where** 句の条件を満たす MyTable テーブル内のすべてのレコード (つまり、**AccountNum** フィールドの値が **1000** に等しいすべてのレコード) がデータベースから削除されます。 一度に 1 つのレコードが削除されます。

```X++
ttsBegin;
while select forUpdate myTable
    where myTable.AccountNum == '1000'
{
    myTable.delete();
}
ttsCommit;
```

## <a name="dodelete-method"></a>doDelete メソッド
**delete** テーブル メソッドと同様に、**doDelete** テーブル メソッドは、データベースから現在のレコードを削除します。 **delete** テーブル メソッドがオーバーライドされていて、オーバーライドされているバージョンではなく **delete** メソッドの元の (基本) バージョンを実行する場合は **doDelete** メソッドを使用します。 したがって、**doDelete** メソッドへの呼び出しは**delete** メソッドの **super()** への呼び出しに相当します。 次の例では、**200** 以上のアカウント番号を持つ myTable テーブルのすべてのレコードを削除します。

```X++
ttsBegin;
while select forUpdate myTable
    where myTable.AccountNum >='200';
{
    myTable.doDelete();
}
ttsCommit;
```

## <a name="insert-method"></a>insert メソッド
**insert** メソッドは、一度に 1 つのレコードを更新します。 一度に複数のレコードを挿入するには、配列挿入、**挿入\_レコードセット**、または **RecordSortedList.insertDatabase** を挿入します。 **insert** メソッドの動作をオーバーライドするには、**doInsert** メソッドを使用します。 **xRecord .insert** メソッドは、**RecId** フィールドおよびシステム フィールドの値を生成した後、データベースにバッファーの内容を挿入します。 **挿入**メソッドが作用する方法を次に示します。

-   クエリによって選択されている行の指定された列のみ、名前付きテーブルに挿入されます。
-   コピー元のテーブルの列とコピー先のテーブルの列は、互換性のある型であることが必要です。
-   両方のテーブルの列がタイプおよび順序において一致する場合、列リストは**挿入**句から省略されます。

### <a name="insert-example-inserting-a-new-record"></a>insert の例: 新規レコードの挿入

次の例では、新しいレコードを CustTable テーブルに挿入します。 新しいレコードの **AccountNum** フィールドは **5000** に設定され、**Name** フィールドは **MyCompany** に設定されます。 (レコードの他のフィールドは空白になります。)

```X++
CustTable custTable;
ttsBegin;
select forUpdate custTable;
custTable.AccountNum = '5000';
custTable.insert();
ttsCommit;
```

### <a name="insert-example-transaction-and-duplicate-key"></a>insert の例: トランザクションと重複キー

次の例は、明示的なトランザクションのコンテキストで **DuplicateKeyException** 例外をキャッチする方法を示しています。 既存の一意の値が重複しているため、**xRecord .insert**の 呼び出しが失敗した場合に例外がスローされます。 **catch** ブロックでは、コードで修正アクションを実行するか、後で分析するためにエラーを記録したりできます。 これにより、トランザクションの保留中のすべての作業が失うことなく、コードの実行を続けることできます。 **挿入\_レコードセット** などのセットに基づく操作によって発生する重複キー例外を把握することはできません。 この例は、TableNumberAとTableNumberB という 2 つのテーブルによって異なります。 両方のテーブルには 1 つの必須の整数フィールドがあります。 これらのフィールドはそれぞれ、**NumberAKey** および **NumberBKey** と命名されます。 固有インデックスは、各キー フィールドで定義されます。 TableNumberA テーブルには、少なくとも 1 つのレコードが必要です。

```X++
static void JobDuplicKeyException44Job(Args _args)
{
    TableNumberA tabNumA; // Has one record, key = 11.
    TableNumberB tabNumB;
    int iCountTries = 0, iNumberAdjust = 0, iNewKey, ii;
    container ctNotes;
    // Empty the B table.
    delete_from tabNumB;
    // Insert a copy of one record.
    insert_recordset tabNumB (NumberBKey)
    select firstOnly NumberAKey from tabNumA order by NumberAKey asc;
    ttsBegin;
    try
    {
        iCountTries++;
        ctNotes += strFmt("---- Inside the try block, try count is %1. ----", iCountTries);
        while select * from tabNumA order by NumberAKey asc
        {
            tabNumB .clear();
            iNewKey = tabNumA .NumberAKey + iNumberAdjust;
            tabNumB .NumberBKey = iNewKey;
            ctNotes += strFmT ("-- %1 is the key to be tried. --" ,iNewKey);
            tabNumB .insert();
            ctNotes += "-- .insert() successful. --";
            break; // Keeps demo simple.
        }
        ttsCommit;
    }
    catch (Exception ::DuplicateKeyException, tabNumB) // Table is optional.
    {
        ctNotes += "---- Inside the catch block. ----";
        ctNotes += infolog .text();
        if (iCountTries <= 1)
        {
            ctNotes += "-- Will issue retry. --";
            iNumberAdjust = 1;
            retry; // Erases Infolog.
        }
        else
        {
            ctNotes += "-- Aborting the transaction. --";
            ttsAbort;
        }
    }
    for (ii=1; ii <= conLen(ctNotes); ii++)
    {
        info(conPeek(ctNotes ,ii));
    }
}

/*********Actual Infolog output
        Message (10:53:13 am)
    ---- Inside the try block, try count is 1. ----
    -- 11 is the key to be tried. --
    ---- Inside the catch block. ----
    Cannot create a record in TableNumberB (TableNumberB).
    The record already exists.
    -- Will issue retry. --
    ---- Inside the try block, try count is 2. ----
    -- 12 is the key to be tried. --
    -- .insert() successful. --
*********/
```

## <a name="doinsert-method"></a>doInsert メソッド
**doInsert** メソッドは、**RecId** フィールドおよびその他のシステム フィールドの値を生成した後、データベースにバッファーの内容を挿入します。 テーブルの **insert** メソッドをバイパスする必要がある場合は、このメソッドを使用します。 次の例では、新しいレコードが挿入されます。 レコードの **name** フィールドは **Warren Langer** に設定され、**value** フィールドは **100** に設定されます。

```X++
ttsBegin;
myTable.name = 'Warren Langer';
myTable.value = 100;
myTable.doInsert();
ttsCommit;
```

## <a name="transactional-integrity"></a>トランザクションの整合性
手順で、トランザクションの整合性を保証しなかった場合、データが破損する可能性があります。 少なくとも、システム上の同時ユーザーに関してスケーラビリティが低下する可能性があります。 **forUpdate** チェックと **tssLevel** チェックの 2 つの内部チェック機能がトランザクションの完全性を保証します。 **forUpdate** チェックは、更新のために最初に選択されたレコードのみを更新または削除されるのを保証するのに役立ちます。 **select** ステートメント内の **forUpdate** キーワードまたはテーブル上の **selectForUpdate** メソッドのいずれかを使用することで、更新プログラムのレコードを選択することができます。 **ttsLevel** チェックは、レコードが更新のために選択されたのと同じトランザクション範囲内でのみ更新または削除できることを保証するのに役立ちます。 整合性を保証するために、次のステートメントを使用します。

-   **ttsBegin** – このステートメントは、トランザクションの開始位置を示します。 これにより、データの整合性が保証され、トランザクションが終了するまで (**ttsCommit** または **ttsAbort** を通じて) 実行されるすべての更新が一貫したもの (すべてまたはなし) であることも保証されます。
-   **ttsCommit** – このステートメントは、トランザクションの正常終了を示します。 トランザクションを終了してコミットします。 Finance and Operations は、確定されたトランザクションが意図に従って実行されるのを保証するのに役立ちます。
-   **ttsAbort** – このステートメントを使用すると、現在のトランザクションのすべての変更を明示的に破棄できます。 この場合、データベースは何も変更されていない元の状態にロールバックされます。 この文は通常、ユーザーが現在のジョブを中断したいことを検出した場合に使用します。 **ttsAbort** ステートメントは、データベースが一貫していることを保証するのに役立ちます。

通常、**ttsAbort** の代わりに、例外処理を使用することをお勧めします。 **throw** ステートメントは、自動的に現在のトランザクションを中断します。 次の例が示すように、**ttsBegin** と **ttsCommit** の間の明細書には 1 つ以上のトランザクション ブロックを含めることができます。 そのような場合、最後の **ttsCommit** ステートメントから正常に終了するまで実際にコミットされるものはありません。

```X++
ttsBegin;
    // Some statements.
ttsBegin;
    // More statements.
ttsCommit;
ttsCommit;
```

次の例では、レコードのセットを選択し、**NameAlias** フィールドを更新します。

```X++
Custtable custTable;
ttsBegin;
select forUpdate custTable where custTable.AccountNum == '4000';
custTable.NameAlias = custTable.Name;
custTable.update();
ttsCommit;
```

### <a name="example-of-code-that-is-rejected-by-the-two-transaction-integrity-checks"></a>2 つのトランザクションの整合性チェックが拒否したコード例

この例では、**forupdate** キーワードがないため、最初のエラーが発生します。 2 番目のエラーは、更新のトランザクション スコープが、レコードが **ttsCommit** の更新用に選択されたトランザクション スコープと異なるために発生します。

```X++
ttsBegin;
select myTable; // Rejected by the forUpdate check.
mytable.myField = 'xyz';
myTable.update();
ttsCommit;
ttsBegin;
select forUpdate * from myTable;
myTable.myField = 'xyz';
ttsCommit;
...
ttsBegin;
myTable.update(); // Rejected by the ttsLevel check.
ttsCommit;
```

## <a name="speeding-up-sql-operations"></a>SQL 操作の高速化
次の構文では、複数のレコードを挿入、更新、または削除できます。 これらのコンストラクトを使用することにより、アプリケーションとデータベース間の通信が減少するためパフォーマンスが向上します。 場合によっては、レコードのセットに基づく操作をレコードごとの操作に戻すことができます。

| 構築         | 説明                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------|
| RecordSortedList  | 1 つのデータベース トリップに複数のレコードを挿入します。 特定のテーブルのデータのサブセットを必要とし、現在インデックスとして存在しない順序でソートする場合は、このコンストラクトを使用します |
| RecordInsertList  | 1 つのデータベース トリップに複数のレコードを挿入します。 データをソートする必要がない場合は、この構文を使用します。 |
| insert\_recordset | 複数のレコードを 1 つまたは複数のテーブルから別のテーブルに直接コピーします。        |
| update\_recordset | 1 回のデータベース トリップでテーブルの複数の行を更新します。                                                  |
| delete\_from      | 1 回のデータベース トリップでデータベースから複数のレコードを削除します。                                        |

## <a name="insert_recordset"></a>insert\_recordset
**insert\_recordset** ステートメントは、1 回のサーバー トリップで、1 つ以上のソース テーブルからデータを直接 1 つのターゲット テーブルにコピーします。 配列挿入より **insert\_recordset** を使用したほうが高速です。 ただし、配列挿入は、データを挿入する前に処理する場合より柔軟になります。 **挿入\_レコード セット**はレコード セットに基づく、一度に複数のレコードに対する操作を実行する演算子です。 ただし、多くの場合レコードごとの操作に戻れます。

### <a name="insert_recordset-syntax"></a>insert\_recordset 構文

*ListOfFields* 出力先テーブルは、ソース テーブル内のフィールドのリストと一致する必要があります。 データは、フィールドの一覧に表示されている順に転送されます。 フィールドの一覧に表示されていない出力先テーブルのフィールドは、他の領域と同じように、**0** (ゼロ) の値に割り当てられています。 **RecId** などのシステム フィールドは、出力先テーブルのカーネルによって透過的に割り当てられます。

**insert\_recordset** *DestinationTable* **(** *ListOfFields* **)**

**select** *ListOfFields1* **from** *SourceTable* **\[ where** *WhereClause* **\]** 

**\[ join** *ListOfFields2* **from** *JoinedSourceTable* **\[ where** *JoinedWhereClause* **\]\]**

### <a name="example-inserting-data-from-another-table"></a>例: 別のテーブルからデータを挿入

この例では、**myNum** および **mySum** レコードは anotherTable テーブルから取得され、myTable テーブルに挿入されます。 レコードは **myNum** に基づいてグループ化されます。**100** 以下の値を持つ **myNum** のみが挿入に含まれます。

```X++
insert_recordset myTable (myNum, mySum)
    select myNum, sum(myValue)
        from anotherTable
        group by myNum
        where myNum <= 100;
```

### <a name="example-inserting-data-from-variables"></a>例: 変数からデータを挿入

次の例は、**insert\_recordset** ステートメントが変数で提供されるデータを挿入できることを示しています。 この例では、1 行だけ挿入するために **firstonly** キーワードが使用されます。 **128** または**このリテラル文字列**などのリテラルは、挿入されるデータのソースとして使用することはできません。

```X++
static void InsertVariable3Job(Args _args)
{
    TableAlphabet    tabA2;
    BankAccountTable tabB3;
    str  1 sLetter = "a";
    str 16 sExampleWord = "apple";
    DELETE_FROM tabA2;
    INSERT_RECORDSET tabA2
        (Letter ,ExampleWord)
    select firstonly
        sLetter ,sExampleWord // Variables.
    from tabB3;
    WHILE SELECT * from tabA2
    {
        info(tabA2 .Letter + " , " + tabA2 .ExampleWord);
    }

/***********  Actual Infolog output
Message (04:03:52 pm)
a , apple
***********/
}
```

### <a name="example-inserting-data-by-using-a-join"></a>例: 結合を使用してデータを挿入

次の例は、サブセレクトを持つ **insert\_recordset** ステートメント上の 3 つのテーブルの結合を示しています。 また、同じ結合がある **while** **select** ステートメントも示します。 変数は、1 つの列に挿入された値を供給するために使用されます。 **str** 変数は、宣言する必要があり、長さを対応するデータベース フィールドの最大長さ以下にする必要があります。 この例では、tabEmplProj5 テーブルに対する **insert\_recordset** ステートメントがあります。 ターゲット フィールドの 1 つに**説明**という名前が付けられ、フィールドのデータはローカル変数 **sDescriptionVariable** から取得されます。 **説明** フィールドの構成キーは無効の場合でも **insert\_recordset** ステートメントは成功します。 システムでは、**Description** フィールドと **sDescriptionVariable** 変数の両方を無視します。 したがって、このコードは*コンフィギュレーション キーの自動化*の例を提供します。 コンフィギュレーション キーの自動化は、コンフィギュレーション キーがオフになっているフィールドにデータを挿入する **insert\_ recordset** ステートメントの動作を、システムが自動的に調整できるときに発生します。

```X++
static void InsertJoin42Job(Args _args)
{
    GmTabDepartment tabDept2;
    GmTabEmployee tabEmpl3;
    GmTabProject tabProj4;
    GmTabEmployeeProject tabEmplProj5;
    str 64 sDescriptionVariable = "From variable.";
    DELETE_FROM tabEmplProj5;
    INSERT_RECORDSET tabEmplProj5
        (
        Description
        , EmployeeRecId
        , ProjectRecId
        )
    Select
        sDescriptionVariable
        , RecId
    from
        tabEmpl3
        join
            tabDept2
            where tabEmpl3 .DepartmentGuid == tabDept2 .DepartmentGuid
        join RecId
            from tabProj4
            where tabDept2 .DepartmentGuid == tabProj4 .DepartmentGuid
    info(int642str(tabEmplProj5 .rowCount())
        + " ==Number of rows inserted.");
    WHILE SELECT *
        from
            tabEmplProj5
            join tabEmpl3
                where tabEmplProj5 .EmployeeRecId == tabEmpl3 .RecId
            join tabProj4
                where tabEmplProj5 .ProjectRecId == tabProj4 .RecId
    {
        info(
            tabEmpl3 .EmployeeName
            + "  --works on--  "
            + tabProj4 .ProjectName
            + " (" + tabEmplProj5 .Description + ")."
            );
    }

/*****************  Actual Infolog output
Message (01:05:41 pm)
4 ==Number of rows inserted.
Alice  --works on--  Project ZZZ (From variable.).
Alice  --works on--  Project YY (From variable.).
Beth  --works on--  Project ZZZ (From variable.).
Beth  --works on--  Project YY (From variable.).
*****************/
}
```

## <a name="update_recordset"></a>update\_recordset
**update\_recordset** ステートメントでは、サーバーへの 1 回のアクセスで複数の行を更新することができます。 したがって、SQL Server の機能は、一部のタスクのパフォーマンスを向上させるのに役立ちます。 ****update\_recordset**** ステートメントは X++ の **delete\_from** と SQL の **update set** に似ています。 フェッチ、変更、更新によって個別に各レコードを取得しません。代わりに、データベース サーバー側で設定された SQL スタイル レコードで動作します。 **更新**メソッドがオーバーライドされた場合、実装は、一度に 1 つのレコードが更新される古典的なループ構造に戻されます。 (この動作は、削除対象の **削除の\_対象** の動作に似ています。) したがって、構築は、一時テーブルとテーブル全体 - キャッシュされたテーブルで、ループ構造を使用して動作します。

### <a name="example-update-that-is-based-on-a-calculated-value"></a>例: 計算値に基づく更新プログラム

次の例では、myTableBuffer テーブルを更新して、テーブルのすべてのレコードで **field1**フィールドの値を 10% 増分します。

```X++
MyTable myTableBuffer;
update_recordset myTableBuffer
setting field1 = field1 * 1.10;
```

### <a name="example-update-that-uses-a-where-clause"></a>例: where 句を使用する更新プログラム

次の例では、**field1** フィールドの値が **0** の myTable テーブルのすべてのレコードを更新します。 **field1** フィールドには、新しい値 **1** が割り当てられます。 **field2** フィールドには、**fieldX** および **fieldY** の合計値が割り当てられます。 この例では、複数のフィールドを同時に更新し、**where** 句を満たす行のみを更新します。

```X++
MyTable myTableBuffer;
update_recordset myTableBuffer
setting
    field1 = 1,
    field2 = fieldX + fieldY
where field1 == 0;
```

### <a name="example-updating-joined-tables"></a>例: 結合されたテーブルの更新プログラム

次の例は、**update\_recordset** ステートメントが複数のテーブルの結合をサポートしていることを示しています。 結合されたテーブルのデータを使用して、更新中のテーブル内のフィールドに値を割り当てることができます。

```X++
static void Join22aJob(Args _args)
{
    TableEmployee tabEmpl;
    TableDepartment tabDept;
    TableProject tabProj;
    update_recordset tabEmpl
    setting
        currentStatusDescription = tabDept .DeptName
            + ", " + tabProj .ProjName
    join tabDept
        where tabDept .DeptId == tabEmpl .DeptId
    join tabProj
        where tabProj .ProjId == tabEmpl .ProjId;
    info(strFmt("Number of records updated is %1."
        ,tabEmpl .rowCount()));
}
```

## <a name="delete_from"></a>delete\_from
**delete\_from** ステートメントを使用することにより、データベース テーブルから複数のレコードを削除することができます。 この方法は、一度に 1 つのレコードを削除するループで **xRecord .delete** メソッドを使用する方法よりも効率的かつ高速になります。 **delete** メソッドをオーバーライドした場合、システムは削除される各行につき 1 回 **delete\_from** ステートメントを **delete** メソッドを呼び出すコードに解釈します。

### <a name="example-efficiently-deleting-records-by-using-delete_from"></a>例: delete\_from を使用して、効率的にレコードを削除

次の例は、複数のレコードを効率的に削除する方法を示しています。

```X++
static void DeleteMultiRow1aJob(Args _args)
{
    MyWidgetTable tabWidget;
    delete_from tabWidget
        where tabWidget .quantity <= 100;
}
```

#### <a name="example-inefficiently-deleting-records-by-using-forupdate"></a>例: forUpdate を使用して、非効率的にレコードを削除

次の例は非効率的です。 個別の SQL **削除**呼び出しを、各レコードのデータベース サーバーに発行します。 **xRecord** **.delete** メソッドが、呼び出しごとに複数のレコードを削除することはありません。

```X++
static void DeleteMultiRow1bJob(Args _args)
{
    MyWidgetTable tabWidget; // extends xRecord.
    ttsBegin;
    while select
        forUpdated
        tabWidget
        where tabWidget .quantity <= 100
    {
        tabWidget .delete();
    }
    ttsCommit;
}
```
### <a name="example-a-delete-operation-that-has-an-inner-join"></a>例: 内部結合を持つ削除操作

内部結合は **delete\_from** ステートメントではサポートされません。 したがって、修正していない **join** キーワードを **delete\_from** ステートメント上で使用することができません。 ただし、他の方法を使用して内部結合を論理的に実行できます。 次の例は、一連のステートメントを通して内部結合ロジックを達成するための新旧の手法を示しています。

```X++
// This is the new and recommended way of using the delete_from method and inner joins.
// The following code example is relatively efficient. It issues a
// separate delete_from statement for each loop iteration. However, each
// delete_from statement can delete multiple records, a subset of all the
// records that the job deletes.
static void DeleteInnerJoin2bJob(Args _args)
{
    MyWidgetTable tabWidget; // extends xRecord.
    ttsBegin;
    while select
        from tabGalaxy
            where tabGalaxy .isTrusted == 0
    {
        delete_from tabWidget
            where tabWidget .GalaxyRecId ==
                tabGalaxy .RecId;
    }
    ttsCommit;
}

// This is the old way of using the delete method and inner joins.
// The following delete method is inefficient. It issues a
// separate SQL delete call to the database server for each record.
static void DeleteInnerJoin2aJob(Args _args)
{
    MyWidgetTable tabWidget; // extends xRecord.
    ttsBegin;
    while select
        forUpdate
        tabWidget
        join tabGalaxy
            where
                tabWidget .GalaxyRecId == tabGalaxy .RecId
                && tabGalaxy .isTrusted == 0
    {
        tabWidget .delete();
    }
    ttsCommit;
}
```
### <a name="example-a-delete-operation-that-uses-the-notexists-join-keyword"></a>例: notexists 結合キーワードを使用する削除操作

**notexists join** キーワード ペアは **delete\_from** ステートメント内で使用することができます。 次の例の **delete\_from** ステートメントが効率的です。 **notexists join** 句を使用すると、**delete\_from** ステートメントが特定の行セットを削除できるようになります。 この例では、**delete\_from** ステートメントが子の注文明細行の行がない親の注文ヘッダー行をすべて削除します。 また、**exists join** 句を **delete\_from** ステートメント上で使用することができます。

```X++
static void DeleteFromNotexists3bJob(Args _args)
{
    GmTabOrderHeader tabOHeader;
    GmTabOrderLine tabOLine;
    AddressState tabAddressState;
    str 127 sOH_Info;
    str 127 sOL_Data;
    int64 i64OHRecId;
    delete_from tabOLine;
    delete_from tabOHeader;
    // Inserts into parent table.
    sOH_Info = "Albert needs tires.";
    insert_recordset tabOHeader
        (OH_Info)
        select firstOnly sOH_Info from tabAddressState;
    sOH_Info = "Benson wants plastic.";
    insert_recordset tabOHeader
        (OH_Info)
        select firstOnly sOH_Info from tabAddressState;
    // Obtain a OrderHeader RecId,
    // use it to insert one child row.
    sOL_Data = "4 re-treads.";
    while select firstOnly tabOHeader
        order by OH_Info
        where tabOHeader .OH_Info like "A*"
    {
        i64OHRecId = tabOHeader .RecId;
        insert_recordset tabOLine
            (OL_Data ,OrderHeaderRecId)
            select firstOnly
                sOL_Data ,i64OHRecId
                from tabAddressState;
        break;
    }
    // Before the delete notexists.
    // Display all parent, and then all child rows.
    while select tabOHeader
        order by OH_Info
    {
        info(strFmt(
            "Before: OHeader:  OH_Info==%1 , RecId==%2"
            ,tabOHeader .OH_Info ,tabOHeader .RecId
            ));
    }
    while select tabOLine
        order by OL_Data
    {
        info(strFmt(
            "Before: OLine:  OL_Data==%1 , OrderHeaderRecId==%2"
            ,tabOLine .OL_Data ,tabOLine .OrderHeaderRecId
            ));
    }
    // Delete_From NotExists Join, to remove from the
    // parent table all order headers without children.
    delete_from tabOHeader
        notexists join tabOLine
            where tabOHeader .RecId ==
                tabOLine .OrderHeaderRecId;
    info(strFmt
        ("%1 is the number of childless OHeader records deleted."
        ,tabOHeader.rowCount()));
    // After the delete notexists.
    // Display all parent, and then all child rows.
    info("- - - - - - - - - - - - - - -");
    while select tabOHeader
        order by OH_Info
    {
        info(strFmt(
            "After: OHeader:  OH_Info==%1 , RecId==%2"
            ,tabOHeader .OH_Info ,tabOHeader .RecId
            ));
    }
    while select tabOLine
        order by OL_Data
    {
        info(strFmt(
            "After: OLine:  OL_Data==%1 , OrderHeaderRecId==%2"
            ,tabOLine .OL_Data ,tabOLine .OrderHeaderRecId
            ));
    }

/**************  Actual Infolog output
Message (12:54:14 pm)
Before: OHeader:  OH_Info==Albert needs tires. , RecId==5637144608
Before: OHeader:  OH_Info==Benson wants plastic. , RecId==5637144609
Before: OLine:  OL_Data==4 re-treads. , OrderHeaderRecId==5637144608
1 is the number of childless OHeader records deleted.
- - - - - - - - - - - - - - -
After: OHeader:  OH_Info==Albert needs tires. , RecId==5637144608
After: OLine:  OL_Data==4 re-treads. , OrderHeaderRecId==5637144608
**************/
}
```

## <a name="maintain-fast-sql-operations"></a>高速な SQL 操作の管理
レコード セット ベースの操作をより低速のレコードごとの操作に変換できる状況があります。 次の情報は、これらの状況を識別します。


### <a name="non-sql-tables"></a>非 SQL テーブル

| 工程 | 変換可能 |
|---|---|
|DELETE_FROM|有|
|UPDATE_RECORDSET|有|
|INSERT_RECORDSET|有|
|ARRAY_INSERT|有|
|オーバーライドにこの設定を使用する|該当なし|

### <a name="delete-actions"></a>アクションの削除

| 工程 | 変換可能 |
|---|---|
|DELETE_FROM|有|
|UPDATE_RECORDSET|無|
|INSERT_RECORDSET|無|
|ARRAY_INSERT|無|
|オーバーライドにこの設定を使用する|**skipDeleteActions**|

### <a name="the-database-log-is-enabled"></a>データベース ログが有効になっています。

| 工程 | 変換可能 |
|---|---|
|DELETE_FROM|有|
|UPDATE_RECORDSET|有|
|INSERT_RECORDSET|有|
|ARRAY_INSERT|無|
|オーバーライドにこの設定を使用する|**skipDatabaseLog**|

### <a name="overridden-method"></a>オーバーライドされたメソッド

| 工程 | 変換可能 |
|---|---|
|DELETE_FROM|有|
|UPDATE_RECORDSET|有|
|INSERT_RECORDSET|有|
|ARRAY_INSERT|有|
|オーバーライドにこの設定を使用する|**skipDataMethods**|

### <a name="alerts-are-set-up-for-the-table"></a>警告はテーブルの設定をします。

| 工程 | 変換可能 |
|---|---|
|DELETE_FROM|有|
|UPDATE_RECORDSET|有|
|INSERT_RECORDSET|有|
|ARRAY_INSERT|無|
|オーバーライドにこの設定を使用する|**skipEvents**|

### <a name="the-validtimestatefieldtype-property-on-a-table-isnt-equal-to-none"></a>テーブル上の ValidTimeStateFieldType プロパティは、[なし] とは等しくなりません。

| 工程 | 変換可能 |
|---|---|
|DELETE_FROM|有|
|UPDATE_RECORDSET|有|
|INSERT_RECORDSET|有|
|ARRAY_INSERT|有|
|オーバーライドにこの設定を使用する|該当なし|


**オーバーライドにこの設定を使用**に対して表示される設定を使用して、パフォーマンスに悪影響を与える 1 つまたは複数の要因を明示的にスキップまたは無視します。 何らかの理由で前述の SQL 操作のひとつがレコードごとの操作にダウングレードされた場合、すべての **skip\*** 設定も無視されます。 たとえば、次のコードでは、コンテナーまたはメモ フィールドが myTable で定義されている場合はこの方法をスキップする必要があると明確に示されていても、myTable テーブルで**挿入**メソッドが実行されます。

```X++
public void tutorialRecordInsertList()
{
    MyTable myTable;
    RecordInsertList insertList = new RecordInsertList(
        myTable.TableId,
        True);
    int i;
    for ( i = 1; i <=  100; i++ )
    {
        myTable.value = i;
        insertList.add(myTable);
    }
    insertList.insertDatabase();
}
```



