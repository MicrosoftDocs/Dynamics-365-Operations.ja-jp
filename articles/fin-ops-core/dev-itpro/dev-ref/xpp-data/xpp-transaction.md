---
title: X++ トランザクションの整合性
description: このトピックでは、X++ 言語でのトランザクションの整合性について説明します。
author: RobinARH
ms.date: 06/16/2020
ms.topic: article
audience: Developer
ms.reviewer: robinr
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 051d9c0724a0f0ccdca25cd4bab304d02c239618
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865910"
---
# <a name="x-transactional-integrity"></a><span data-ttu-id="7abe6-103">X++ トランザクションの整合性</span><span class="sxs-lookup"><span data-stu-id="7abe6-103">X++ transactional integrity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7abe6-104">このトピックでは、X++ 言語でのトランザクションの整合性について説明します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-104">This topic describes transactional integrity in the X++ language.</span></span>

<span data-ttu-id="7abe6-105">トランザクションの整合性を確認する手順を踏まなかった場合、データが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7abe6-105">If you don't take steps to ensure the integrity of transactions, data corruption can occur.</span></span> <span data-ttu-id="7abe6-106">少なくとも、システム上の同時ユーザーに関してスケーラビリティが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7abe6-106">At the very least, you might experience poor scalability with respect to concurrent users on the system.</span></span> <span data-ttu-id="7abe6-107">**forUpdate** チェックと **ttsLevel** チェックの 2 つの内部チェック機能がトランザクションの安全性を保証します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-107">Two internal checking features help ensure the integrity of transactions: the **forUpdate** check and the **ttsLevel** check.</span></span>

- <span data-ttu-id="7abe6-108">**forUpdate** チェックは、更新のために最初に選択されたレコードのみを更新または削除されるのを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7abe6-108">A **forUpdate** check helps ensure that a record can be updated or deleted only if it has first been selected for update.</span></span> <span data-ttu-id="7abe6-109">**select** ステートメント内の **forUpdate** キーワードまたはテーブル上の **selectForUpdate** メソッドのいずれかを使用することで、更新プログラムのレコードを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="7abe6-109">You can select a record for update by using either the **forUpdate** keyword in the **select** statement or the **selectForUpdate** method on the table.</span></span>
- <span data-ttu-id="7abe6-110">**ttsLevel** チェックは、レコードが更新のために選択されたのと同じトランザクション範囲内でのみ更新または削除できることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7abe6-110">A **ttsLevel** check helps ensure that a record can be updated or deleted only in the same transaction scope where it was selected for update.</span></span>

<span data-ttu-id="7abe6-111">整合性を確保するために、次のステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-111">The following statements are used to help ensure integrity:</span></span>

- <span data-ttu-id="7abe6-112">**ttsBegin** – このステートメントは、トランザクションの開始位置を示します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-112">**ttsBegin** – This statement marks the beginning of a transaction.</span></span> <span data-ttu-id="7abe6-113">これにより、データの整合性が確保され、トランザクションが終了するまで (**ttsCommit** または **ttsAbort** を通じて) 実行されるすべての更新が一貫していることも保証します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-113">It helps ensure data integrity and also helps ensure that all updates that are done until the transaction ends (through **ttsCommit** or **ttsAbort**) are consistent.</span></span>
- <span data-ttu-id="7abe6-114">**ttsCommit** – このステートメントは、トランザクションの正常終了を示します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-114">**ttsCommit** – This statement marks the successful end of a transaction.</span></span> <span data-ttu-id="7abe6-115">トランザクションを終了してコミットします。</span><span class="sxs-lookup"><span data-stu-id="7abe6-115">It ends and commits a transaction.</span></span> <span data-ttu-id="7abe6-116">Finance and Operations アプリは、確定されたトランザクションが意図に従って実行されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-116">The Finance and Operations app ensures that a transaction that has been committed will be performed according to intentions.</span></span>
- <span data-ttu-id="7abe6-117">**ttsAbort** – このステートメントを使用すると、現在のトランザクションのすべての変更を明示的に破棄できます。</span><span class="sxs-lookup"><span data-stu-id="7abe6-117">**ttsAbort** – This statement lets you explicitly discard all changes in the current transaction.</span></span> <span data-ttu-id="7abe6-118">この場合、データベースは元の状態にロールバックされ、何も変更されていません。</span><span class="sxs-lookup"><span data-stu-id="7abe6-118">In this case, the database is rolled back to the original state, where nothing has been changed.</span></span> <span data-ttu-id="7abe6-119">この文は通常、ユーザーが現在のジョブを中断したいことを検出した場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-119">Typically, you use this statement if you've detected that the user wants to break the current job.</span></span> <span data-ttu-id="7abe6-120">**ttsAbort** ステートメントは、データベースが一貫していることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7abe6-120">The **ttsAbort** statement helps ensure that the database is consistent.</span></span>

<span data-ttu-id="7abe6-121">通常、**ttsAbort** の代わりに、例外処理を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7abe6-121">Usually, it's a better idea to use exception handling instead of **ttsAbort**.</span></span> <span data-ttu-id="7abe6-122">**throw** ステートメントは、自動的に現在のトランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-122">The **throw** statement automatically aborts the current transaction.</span></span> <span data-ttu-id="7abe6-123">次の例が示すように、**ttsBegin** と **ttsCommit** の間の明細書には 1 つ以上のトランザクション ブロックを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7abe6-123">As the following example shows, statements between **ttsBegin** and **ttsCommit** can include one or more transaction blocks.</span></span> <span data-ttu-id="7abe6-124">そのような場合、最後の **ttsCommit** ステートメントが正常に終了するまでコミットされるものはありません。</span><span class="sxs-lookup"><span data-stu-id="7abe6-124">In these cases, nothing is committed until a successful exit from the final **ttsCommit** statement occurs.</span></span>

```xpp
ttsBegin;
    // Some statements.
    ttsBegin;
        // More statements.
    ttsCommit;
ttsCommit;
```

<span data-ttu-id="7abe6-125">次の例では、レコードのセットを選択し、**CustGroup** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-125">The following example selects a set of records and updates the **CustGroup** field.</span></span> <span data-ttu-id="7abe6-126">このコードは、**select** ステートメントがレコードを返さない場合、例外をスローし ます。</span><span class="sxs-lookup"><span data-stu-id="7abe6-126">This code will throw an exception if the **select** statement doesn't return any records.</span></span>

```xpp
Custtable custTable;
ttsBegin;
    select forUpdate custTable where custTable.AccountNum == '5000';
    custTable.CustGroup = '1';
    custTable.update();
ttsCommit;
```

## <a name="example-of-code-that-is-rejected-by-the-forupdate-check"></a><span data-ttu-id="7abe6-127">forUpdate チェックにより拒否されたコードの例</span><span class="sxs-lookup"><span data-stu-id="7abe6-127">Example of code that is rejected by the forUpdate check</span></span>

<span data-ttu-id="7abe6-128">この例では、**forUpdate** キーワードがないため、最初のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-128">In this example, the first failure occurs because the **forUpdate** keyword is missing.</span></span> 

```xpp
ttsBegin;
    select myTable; // Rejected by the forUpdate check.
    mytable.myField = 'xyz';
    myTable.update();
ttsCommit;
```

## <a name="example-of-code-that-is-rejected-by-the-ttslevel-check"></a><span data-ttu-id="7abe6-129">ttsLevel チェックにより拒否されたコードの例</span><span class="sxs-lookup"><span data-stu-id="7abe6-129">Example of code that is rejected by the ttsLevel check</span></span>

<span data-ttu-id="7abe6-130">この例では、更新のトランザクション スコープが、レコードが **ttsCommit** の更新用に選択されたトランザクション スコープとは異なるためにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7abe6-130">In this example, the failure occurs because the transaction scope of the update differs from the transaction scope where the record was selected for update in **ttsCommit**.</span></span>

```xpp
ttsBegin;
    select forUpdate * from myTable;
    myTable.myField = 'xyz';
ttsCommit;

ttsBegin;
    myTable.update(); // Rejected by the ttsLevel check.
ttsCommit;
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]