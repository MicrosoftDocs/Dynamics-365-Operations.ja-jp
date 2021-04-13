---
title: 明細書の選択中
description: このトピックでは、X++ 言語での while select ステートメントについて説明します。
author: robinarh
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 1b345b0f24c53302175bddec326d00bad2d62b6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749950"
---
# <a name="while-select-statement"></a><span data-ttu-id="b3b3f-103">明細書の選択中</span><span class="sxs-lookup"><span data-stu-id="b3b3f-103">While select statement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3b3f-104">**while select** ステートメントは、データの処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-104">A **while select** statement is used to handle data.</span></span> <span data-ttu-id="b3b3f-105">**select** ステートメントの最も広く使用されている形式です。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-105">It's the most widely used form of the **select** statement.</span></span> <span data-ttu-id="b3b3f-106">**while select** ステートメントは、特定の基準を満たす多くのレコードをループし、各レコードでステートメントを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-106">The **while select** statement loops over many records that meet specific criteria, and can run a statement on each record.</span></span> <span data-ttu-id="b3b3f-107">**while select** ステートメントの構文は、**select** ステートメントの構文に似ていますが、このステートメントは **select** ではなく **while select** により処理されます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-107">The syntax of a **while select** statement resembles the syntax of a **select** statement, but the statement is preceded by **while select** instead of **select**.</span></span>

+ <span data-ttu-id="b3b3f-108">通常、データ操作のために **while select** ステートメントを使用する場合、トランザクション内でデータ整合性を確保するために使用します。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-108">Typically, when you use the **while select** statement for data manipulation, you use it in a transaction to ensure data integrity.</span></span>
+ <span data-ttu-id="b3b3f-109">**while select** ステートメントの結果はテーブル バッファ変数に返されます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-109">The results of the **while select** statement are returned in a table buffer variable.</span></span>
+ <span data-ttu-id="b3b3f-110">**選択** ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-110">If you use a field list in the **select** statement, only those fields are available in the table variable.</span></span>
+ <span data-ttu-id="b3b3f-111">**sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-111">If you use aggregate functions, such as **sum** or **count**, the results are returned in the fields that you perform the **sum** or **count** over.</span></span> <span data-ttu-id="b3b3f-112">整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-112">You can count, average, or sum only integer and real fields.</span></span>
+ <span data-ttu-id="b3b3f-113">**select** ステートメント自体は、ループのステートメントの最初の繰り返しの直前に 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-113">The **select** statement itself is run only one time, immediately before the first iteration of the statements in the loop.</span></span>
+ <span data-ttu-id="b3b3f-114">**while select** ステートメントに追加されたプール式 (例えば、**iCounter &lt; 1**) は 1 度だけテストされます。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-114">Any Boolean expressions that are added to the **while select** statement (for example, **iCounter &lt; 1**) are tested only one time.</span></span> <span data-ttu-id="b3b3f-115">この動作は、C ++ や C\# などの言語の **while** 文の動作とは異なります。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-115">This behavior differs from the behavior of the **while** statement in languages such as C++ and C\#.</span></span> <span data-ttu-id="b3b3f-116">たとえば、次のループは、複数回繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-116">For example, the following loop can have more than one iteration.</span></span>

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

<span data-ttu-id="b3b3f-117">次の例では、アカウント番号が指定された範囲内にある CustTable テーブルのすべての顧客の **AccountNum** と **SalesGroup** の値を出力します。</span><span class="sxs-lookup"><span data-stu-id="b3b3f-117">The following example prints the **AccountNum** and **SalesGroup** values of every customer in the CustTable table whose account number is within a specified range.</span></span>

```xpp
CustTable custTable;

while select custTable
    order by custTable.AccountNum
    where  custTable.AccountNum >= '4010' && custTable.AccountNum <= '4100'
{
    info(strFmt("%1 , %2", custTable.AccountNum, custTable.SalesGroup));
}
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]