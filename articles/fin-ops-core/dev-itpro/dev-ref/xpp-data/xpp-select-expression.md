---
title: 選択したステートメントを式として記述
description: select ステートメントを式として使用することができます。
author: robinarh
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: robinr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 806ab8544db69ade82c9ddec2b4990b902786a83
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505943"
---
# <a name="writing-a-select-statement-as-an-expression"></a><span data-ttu-id="58ef0-103">選択したステートメントを式として記述</span><span class="sxs-lookup"><span data-stu-id="58ef0-103">Writing a select statement as an expression</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58ef0-104">**select** ステートメントを式として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="58ef0-104">You can use a **select** statement as an expression.</span></span> <span data-ttu-id="58ef0-105">このタイプの **select** ステートメントは、*式 select ステートメント*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="58ef0-105">This type of **select** statement is known as an *expression select statement*.</span></span>

+ <span data-ttu-id="58ef0-106">テーブル バッファ変数は、式 **select** ステートメントで使用できません。</span><span class="sxs-lookup"><span data-stu-id="58ef0-106">You can't use a table buffer variable in an expression **select** statement.</span></span>
+ <span data-ttu-id="58ef0-107">テーブルの名前は、**from** 句で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ef0-107">The name of the table must be used in the **from** clause.</span></span>
+ <span data-ttu-id="58ef0-108">**結合**キーワードはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="58ef0-108">The **join** keyword isn't supported.</span></span>
+ <span data-ttu-id="58ef0-109">**order by** 句でフィールド名を修飾するために、テーブル名を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="58ef0-109">The table name can't be used to qualify a field name in the **order by** clause.</span></span>
+ <span data-ttu-id="58ef0-110">**where** 句では、テーブル名をフィールドの修飾子として使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ef0-110">In a **where** clause, the table name must be used as a qualifier of the field.</span></span>
+ <span data-ttu-id="58ef0-111">**式 select ステートメント**では 1 つのテーブルしか言及できないため、サブセレクトは、サポートされていない**結合**キーワードへの回避策としてサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="58ef0-111">You can only mention one table in an **expression select statement**, therefore subselects aren't supported as a workaround to the unsupported **join** keyword.</span></span>
+ <span data-ttu-id="58ef0-112">データを取り込むことができる唯一の列は、**select** 句の **from** 句の前に名前が付けられている列です。</span><span class="sxs-lookup"><span data-stu-id="58ef0-112">The only column that can be populated with data is the column that is named before the **from** clause in the **select** clause.</span></span>
+ <span data-ttu-id="58ef0-113">閉じ括弧の後に、列の名前を使用してデータ値を参照します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-113">After the closing parenthesis, the name of a column is used to reference the data value.</span></span>

<span data-ttu-id="58ef0-114">次の式は、**CustTable** テーブルの最初の行 (行が存在する場合) から **AccountNum** 列を返します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-114">The following expression returns the **AccountNum** column from the first row (if a row exists) in the **CustTable** table.</span></span>

```xpp
str accountNum = (select AccountNum from CustTable order by AccountNum desc).AccountNum;
info('Max AccountNum: ' + accountNum);
```

<span data-ttu-id="58ef0-115">前の例と同じ結果を達成する単純な方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-115">Here is a simpler way to achieve the same result as the previous example.</span></span>

```xpp
str accountNum = (select maxof(AccountNum) from CustTable).AccountNum;
info('Max AccountNum: ' + accountNum);
```

<span data-ttu-id="58ef0-116">次の例では、ブロックされていない顧客の最大 **RecId**値を返します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-116">The following example returns the maximum **RecId** value of customers that aren't blocked.</span></span> <span data-ttu-id="58ef0-117">ここで、**maxof** 集計関数が使用され、**RecId** フィールドが機能に記載されます。</span><span class="sxs-lookup"><span data-stu-id="58ef0-117">Here, the **maxof** aggregate function is used, and the **RecId** field is mentioned in the function.</span></span> <span data-ttu-id="58ef0-118">集計関数に記載されているフィールドは、閉じかっこの後のデータ値を参照するために使用されるフィールド名と同じでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="58ef0-118">The field that is mentioned in the aggregate function must be the same as the field name that is used to reference the data value after the closing parenthesis.</span></span> <span data-ttu-id="58ef0-119">それ以外の場合、空のデータが返されます。</span><span class="sxs-lookup"><span data-stu-id="58ef0-119">Otherwise, empty data is returned.</span></span>

```xpp
int64 nRecId = (select maxof(RecId) from CustTable
            where CustTable.Blocked == CustVendorBlocked::No).RecId;
info("Max RecId: " + int642Str(nRecId));
```

<span data-ttu-id="58ef0-120">次の例では、**RecId** フィールドは **RecId** の値ではないデータ値を参照するために使用します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-120">In the following example, the **RecId** field is used to reference a data value that isn't a **RecId** value.</span></span> <span data-ttu-id="58ef0-121">**count** 集計関数は、**RecId**値を返しません。</span><span class="sxs-lookup"><span data-stu-id="58ef0-121">The **count** aggregate function doesn't return a **RecId** value.</span></span> <span data-ttu-id="58ef0-122">**RecId** フィールドは通常 **count** 関数と共に使用するのが一般的なプラクティスです。</span><span class="sxs-lookup"><span data-stu-id="58ef0-122">It is a typical practice to use the **RecId** field with the **count** function.</span></span>

```xpp
int64 nRecId = (select count(RecId) from CustTable
            where CustTable.Blocked == CustVendorBlocked::No).RecId;
info('Count of unblocked customers: ' + int642Str(nRecId));
```

## <a name="select-statements-on-fields"></a><span data-ttu-id="58ef0-123">フィールド上の select ステートメント</span><span class="sxs-lookup"><span data-stu-id="58ef0-123">select statements on fields</span></span>

<span data-ttu-id="58ef0-124">**select** ステートメントをフィールド上のルックアップで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="58ef0-124">You can use a **select** statement in a lookup on a field.</span></span> <span data-ttu-id="58ef0-125">テーブルのレコードをフェッチする**選択**ステートメントの後、**.fieldName** を入力してテーブルのフィールドを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="58ef0-125">After a **select** statement that fetches a record in a table, you can enter **.fieldName** to reference a field in the table.</span></span> <span data-ttu-id="58ef0-126">これらの **select** ステートメントは、式で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ef0-126">These **select** statements must be used in expressions.</span></span> <span data-ttu-id="58ef0-127">*通常の **select** ステートメント* は *フィールド **select** ステートメント* と異なります:</span><span class="sxs-lookup"><span data-stu-id="58ef0-127">A *normal **select** statement* differs from a *field **select** statement*:</span></span>

+ <span data-ttu-id="58ef0-128">フィールド **select** ステートメントはテーブル上で直接動作します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-128">The field **select** statement operates directly on a table.</span></span>
+ <span data-ttu-id="58ef0-129">通常の **select** ステートメントは、テーブル バッファ変数で動作します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-129">The normal **select** statement operates on a table buffer variable.</span></span>

<span data-ttu-id="58ef0-130">次の例は、フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="58ef0-130">The following examples display fields.</span></span>

```xpp
print((select CustTable order by AccountStatement).AccountStatement);

if ((select custTable where CustTable.AccountNum == '3000').CreditMax < 5000)
{
    info('This customer has a credit maximum less than $5000.');
}
```
