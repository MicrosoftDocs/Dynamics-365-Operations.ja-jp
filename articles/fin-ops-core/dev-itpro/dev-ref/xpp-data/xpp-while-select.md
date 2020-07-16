---
title: while select ステートメント
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
ms.openlocfilehash: 090c548f22a09870b39242a44be6d0655ab77966
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505944"
---
# <a name="while-select-statement"></a><span data-ttu-id="84482-103">while select ステートメント</span><span class="sxs-lookup"><span data-stu-id="84482-103">While select statement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84482-104">**while select** ステートメントは、データの処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84482-104">A **while select** statement is used to handle data.</span></span> <span data-ttu-id="84482-105">**select** ステートメントの最も広く使用されている形式です。</span><span class="sxs-lookup"><span data-stu-id="84482-105">It's the most widely used form of the **select** statement.</span></span> <span data-ttu-id="84482-106">**while select** ステートメントは、特定の基準を満たす多くのレコードをループし、各レコードでステートメントを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="84482-106">The **while select** statement loops over many records that meet specific criteria, and can run a statement on each record.</span></span> <span data-ttu-id="84482-107">**while select** ステートメントの構文は、**select** ステートメントの構文に似ていますが、このステートメントは**select** ではなく **while select** により処理されます。</span><span class="sxs-lookup"><span data-stu-id="84482-107">The syntax of a **while select** statement resembles the syntax of a **select** statement, but the statement is preceded by **while select** instead of **select**.</span></span>

+ <span data-ttu-id="84482-108">通常、データ操作のために **while select** 文を使用する場合、トランザクション内でデータ整合性を確保するために使用します。</span><span class="sxs-lookup"><span data-stu-id="84482-108">Typically, when you use the **while select** statement for data manipulation, you do it in a transaction to ensure data integrity.</span></span>
+ <span data-ttu-id="84482-109">**while select** ステートメントの結果はテーブル バッファ変数に返されます。</span><span class="sxs-lookup"><span data-stu-id="84482-109">The results of a **while select** statement are returned in a table buffer variable.</span></span>
+ <span data-ttu-id="84482-110">**選択**ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="84482-110">If you use a field list in the **select** statement, only those fields are available in the table variable.</span></span>
+ <span data-ttu-id="84482-111">**sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。</span><span class="sxs-lookup"><span data-stu-id="84482-111">If you use aggregate functions, such as **sum** or **count**, the results are returned in the fields that you perform the **sum** or **count** over.</span></span> <span data-ttu-id="84482-112">整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。</span><span class="sxs-lookup"><span data-stu-id="84482-112">You can count, average, or sum only integer and real fields.</span></span>
+ <span data-ttu-id="84482-113">**select** ステートメント自体は、ループのステートメントの最初の繰り返しの直前に 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="84482-113">The **select** statement itself is run only one time, immediately before the first iteration of the statements in the loop.</span></span>
+ <span data-ttu-id="84482-114">**while select** に追加されたブール式 (**iCounter &lt; 1** など) は 1 度だけテストされます。</span><span class="sxs-lookup"><span data-stu-id="84482-114">Any Boolean expressions (such as **iCounter &lt; 1**) that are added to the **while select** are tested only one time.</span></span> <span data-ttu-id="84482-115">この動作は、C ++ や C\# などの言語の **while** 文の動作とは異なります。</span><span class="sxs-lookup"><span data-stu-id="84482-115">This behavior differs from the behavior of the **while** statement in languages such as C++ and C\#.</span></span> <span data-ttu-id="84482-116">たとえば、次のループは、複数回繰り返します。</span><span class="sxs-lookup"><span data-stu-id="84482-116">For example, the following loop can have more than one iteration.</span></span>

    ```xpp
    int iCounter = 0;
    BankAccountTable xrecBAT;

    while select * from xrecBAT
        where iCounter < 1
    {
        iCounter++;
        info(strFmt("%1 , %2", iCounter, xrecBAT.AccountID));
    }
    ```

<span data-ttu-id="84482-117">次の例では、アカウント番号が指定された範囲内にある **CustTable** テーブルのすべての顧客の **AccountNum** と **SalesGroup** を出力します。</span><span class="sxs-lookup"><span data-stu-id="84482-117">The following example prints the **AccountNum** and **SalesGroup** of every customer in the **CustTable** table whose account number is within a specified range.</span></span>

```xpp
CustTable custTable;

while select custTable
    order by custTable.AccountNum
    where  custTable.AccountNum >= '4010' && custTable.AccountNum <= '4100'
{
    info(strFmt("%1 , %2", custTable.AccountNum, custTable.SalesGroup));
}
```