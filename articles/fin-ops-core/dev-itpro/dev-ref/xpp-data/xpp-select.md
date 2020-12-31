---
title: データの選択
description: このトピックでは、X++ 言語での select ステートメントについて説明します。
author: robinarh
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 1963736c429f1af69aa7d69b03937f6287874673
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408735"
---
# <a name="select-data"></a><span data-ttu-id="b06f2-103">データの選択</span><span class="sxs-lookup"><span data-stu-id="b06f2-103">Select data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b06f2-104">**select** ステートメントは、データベースからデータをフェッチまたは操作します。</span><span class="sxs-lookup"><span data-stu-id="b06f2-104">The **select** statement fetches or manipulates data from the database.</span></span>

+ <span data-ttu-id="b06f2-105">すべての **選択** ステートメントではレコードをフェッチするためテーブル変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="b06f2-105">All **select** statements use a table variable to fetch records.</span></span> <span data-ttu-id="b06f2-106">この変数は、**select** 文を実行する前に宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b06f2-106">This variable must be declared before a **select** statement can be run.</span></span>
+ <span data-ttu-id="b06f2-107">**select** ステートメントは、レコードを 1 つだけ、またはフィールドをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="b06f2-107">The **select** statement fetches only one record, or field.</span></span> <span data-ttu-id="b06f2-108">複数のレコードをフェッチまたは移動したりするには、**next** ステートメントまたは **[while select](xpp-while-select.md)** ステートメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b06f2-108">To fetch or traverse multiple records, you can use the **next** statement or the **[while select](xpp-while-select.md)** statement.</span></span>

    + <span data-ttu-id="b06f2-109">**next** ステートメントは、テーブルの次のレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="b06f2-109">The **next** statement fetches the next record in the table.</span></span> <span data-ttu-id="b06f2-110">**選択** ステートメントの前に、**次** ステートメントがある場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b06f2-110">If no **select** statement precedes the **next** statement, an error occurs.</span></span> <span data-ttu-id="b06f2-111">**次** ステートメントを使用する場合、**firstOnly** 検索オプションを使用しません。</span><span class="sxs-lookup"><span data-stu-id="b06f2-111">If you use a **next** statement, don't use the **firstOnly** find option.</span></span>
    + <span data-ttu-id="b06f2-112">**while select** ステートメントを使用して複数のレコードを移動する方がより適切です。</span><span class="sxs-lookup"><span data-stu-id="b06f2-112">It's more appropriate to use a **while select** statement to traverse multiple records.</span></span>

+ <span data-ttu-id="b06f2-113">**select** ステートメントの結果はテーブル バッファ変数に返されます。</span><span class="sxs-lookup"><span data-stu-id="b06f2-113">The results of a **select** statement are returned in a table buffer variable.</span></span>
+ <span data-ttu-id="b06f2-114">**選択** ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b06f2-114">If you use a field list in the **select** statement, only those fields are available in the table variable.</span></span>

<span data-ttu-id="b06f2-115">次の例では、CustTable テーブルの最初の行のすべての列をフェッチし、その行の **AccountNum** 列に値を出力します。</span><span class="sxs-lookup"><span data-stu-id="b06f2-115">The following example fetches all the columns in the first row of the CustTable table and prints the value in the **AccountNum** column of that row.</span></span>

```xpp
CustTable custTable;
select * from custTable;
info("AccountNum: " + custTable.AccountNum);
```

<span data-ttu-id="b06f2-116">次の例では、CustTable テーブルで各行の **AccountNum** 列の値を出力します。</span><span class="sxs-lookup"><span data-stu-id="b06f2-116">The following example prints the value in the **AccountNum** column of each row in the CustTable table.</span></span>

```xpp
CustTable custTable;
while select * from custTable
{
    info("AccountNum: " + custTable.AccountNum);
}
```

<span data-ttu-id="b06f2-117">次の例では、**select** ステートメントによって返された最初の 2 つの行の **AccountNum** 列の値を出力します。</span><span class="sxs-lookup"><span data-stu-id="b06f2-117">The following example prints the value in the **AccountNum** column of the first two rows that are returned by the **select** statement.</span></span>

```xpp
CustTable custTable;
select * from custTable;
info("AccountNum: " + custTable.AccountNum);

next custTable;
info("AccountNum: " + custTable.AccountNum);
```

<span data-ttu-id="b06f2-118">詳細については、[select ステートメント](xpp-select-statement.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b06f2-118">For more examples, see [Select statement](xpp-select-statement.md).</span></span>
