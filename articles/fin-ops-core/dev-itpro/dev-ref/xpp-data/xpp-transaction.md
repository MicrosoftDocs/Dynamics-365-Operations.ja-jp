---
title: X++ トランザクションの整合性
description: このトピックでは、X++ 言語でのトランザクションの整合性について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150273
ms.assetid: 999a5ecf-559b-4d66-8b05-9a8e477e0518
ms.search.region: Global
ms.author: robinr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: fc2a669d3d46eaacf97720fa7236df3e06372292
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505945"
---
# <a name="transactional-integrity"></a><span data-ttu-id="84217-103">トランザクションの整合性</span><span class="sxs-lookup"><span data-stu-id="84217-103">Transactional integrity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84217-104">このトピックでは、X++ 言語でのトランザクションの整合性について説明します。</span><span class="sxs-lookup"><span data-stu-id="84217-104">This topic describes transactional integrity in the X++ language.</span></span>

<span data-ttu-id="84217-105">トランザクションの整合性を保証する手順を踏まなかった場合、データが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84217-105">If you don't take steps to help guarantee the integrity of transactions, data corruption can occur.</span></span> <span data-ttu-id="84217-106">少なくとも、システム上の同時ユーザーに関してスケーラビリティが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84217-106">At the very least, you might experience poor scalability with respect to concurrent users on the system.</span></span> <span data-ttu-id="84217-107">**forUpdate** チェックと **tssLevel** チェックの 2 つの内部チェック機能がトランザクションの完全性を保証します。</span><span class="sxs-lookup"><span data-stu-id="84217-107">Two internal checking features help guarantee the integrity of transactions: the **forUpdate** check and the **tssLevel** check.</span></span> <span data-ttu-id="84217-108">**forUpdate** チェックは、更新のために最初に選択されたレコードのみを更新または削除されるのを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="84217-108">A **forUpdate** check helps guarantee that a record can be updated or deleted only if it has first been selected for update.</span></span> <span data-ttu-id="84217-109">**select** ステートメント内の **forUpdate** キーワードまたはテーブル上の **selectForUpdate** メソッドのいずれかを使用することで、更新プログラムのレコードを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="84217-109">You can select a record for update by using either the **forUpdate** keyword in the **select** statement or the **selectForUpdate** method on the table.</span></span> <span data-ttu-id="84217-110">**ttsLevel** チェックは、レコードが更新のために選択されたのと同じトランザクション範囲内でのみ更新または削除できることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="84217-110">A **ttsLevel** check helps guarantee that a record can be updated or deleted only within the same transaction scope where it was selected for update.</span></span> <span data-ttu-id="84217-111">整合性を保証するために、次のステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="84217-111">The following statements are used to help guarantee integrity:</span></span>

- <span data-ttu-id="84217-112">**ttsBegin** – このステートメントは、トランザクションの開始位置を示します。</span><span class="sxs-lookup"><span data-stu-id="84217-112">**ttsBegin** – This statement marks the beginning of a transaction.</span></span> <span data-ttu-id="84217-113">これにより、データの整合性が保証され、トランザクションが終了するまで (**ttsCommit** または **ttsAbort** を通じて) 実行されるすべての更新が一貫したもの (すべてまたはなし) であることも保証されます。</span><span class="sxs-lookup"><span data-stu-id="84217-113">It helps guarantee data integrity, and also helps guarantees that all updates that are done until the transaction ends (through **ttsCommit** or **ttsAbort**) are consistent (all or none).</span></span>
- <span data-ttu-id="84217-114">**ttsCommit** – このステートメントは、トランザクションの正常終了を示します。</span><span class="sxs-lookup"><span data-stu-id="84217-114">**ttsCommit** – This statement marks the successful end of a transaction.</span></span> <span data-ttu-id="84217-115">トランザクションを終了してコミットします。</span><span class="sxs-lookup"><span data-stu-id="84217-115">It ends and commits a transaction.</span></span> <span data-ttu-id="84217-116">Finance and Operations アプリは、確定されたトランザクションが意図に従って実行されるのを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="84217-116">The Finance and Operations app helps guarantee that a transaction that has been committed will be performed according to intentions.</span></span>
- <span data-ttu-id="84217-117">**ttsAbort** – このステートメントを使用すると、現在のトランザクションのすべての変更を明示的に破棄できます。</span><span class="sxs-lookup"><span data-stu-id="84217-117">**ttsAbort** – This statement lets you explicitly discard all changes in the current transaction.</span></span> <span data-ttu-id="84217-118">この場合、データベースは何も変更されていない元の状態にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="84217-118">In this case, the database is rolled back to the original state where nothing has been changed.</span></span> <span data-ttu-id="84217-119">この文は通常、ユーザーが現在のジョブを中断したいことを検出した場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="84217-119">Typically, you use this statement if you've detected that the user wants to break the current job.</span></span> <span data-ttu-id="84217-120">**ttsAbort** ステートメントは、データベースが一貫していることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="84217-120">The **ttsAbort** statement helps guarantee that the database is consistent.</span></span>

<span data-ttu-id="84217-121">通常、**ttsAbort** の代わりに、例外処理を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="84217-121">Usually, it's a better idea to use exception handling instead of **ttsAbort**.</span></span> <span data-ttu-id="84217-122">**throw** ステートメントは、自動的に現在のトランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="84217-122">The **throw** statement automatically aborts the current transaction.</span></span> <span data-ttu-id="84217-123">次の例が示すように、**ttsBegin** と **ttsCommit** の間の明細書には 1 つ以上のトランザクション ブロックを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="84217-123">As the following example shows, statements between **ttsBegin** and **ttsCommit** can include one or more transaction blocks.</span></span> <span data-ttu-id="84217-124">そのような場合、最後の **ttsCommit** ステートメントから正常に終了するまでコミットされるものはありません。</span><span class="sxs-lookup"><span data-stu-id="84217-124">In these cases, nothing is committed until the successful exit from the final **ttsCommit** statement.</span></span>

```xpp
ttsBegin;
    // Some statements.
    ttsBegin;
        // More statements.
    ttsCommit;
ttsCommit;
```

<span data-ttu-id="84217-125">次の例では、レコードのセットを選択し、**CustGroup** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="84217-125">The following example selects a set of records and updates the **CustGroup** field.</span></span> <span data-ttu-id="84217-126">このコードは、**select** ステートメントがレコードを返さない場合、例外をスローし ます。</span><span class="sxs-lookup"><span data-stu-id="84217-126">This code will throw an exception if the **select** statement doesn't return any records.</span></span>

```xpp
Custtable custTable;
ttsBegin;
    select forUpdate custTable where custTable.AccountNum == '5000';
    custTable.CustGroup = '1';
    custTable.update();
ttsCommit;
```

## <a name="example-of-code-rejected-by-the-forupdate-check"></a><span data-ttu-id="84217-127">forupdate チェックにより拒否されたコードの例</span><span class="sxs-lookup"><span data-stu-id="84217-127">Example of code rejected by the forupdate check</span></span>

<span data-ttu-id="84217-128">この例では、**forupdate** キーワードがないため、最初のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="84217-128">In this example, the first failure occurs because the **forupdate** keyword is missing.</span></span> 

```xpp
ttsBegin;
    select myTable; // Rejected by the forUpdate check.
    mytable.myField = 'xyz';
    myTable.update();
ttsCommit;
```

## <a name="example-of-code-rejected-by-the-tsslevel-check"></a><span data-ttu-id="84217-129">tsslevel チェックにより拒否されたコードの例</span><span class="sxs-lookup"><span data-stu-id="84217-129">Example of code rejected by the tsslevel check</span></span>

<span data-ttu-id="84217-130">この例では、更新のトランザクション スコープが、レコードが **ttsCommit** の更新用に選択されたトランザクション スコープとは異なるためにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="84217-130">In this example, the failure occurs because the transaction scope of the update differs from the transaction scope where the record was selected for update in **ttsCommit**.</span></span>

```xpp
ttsBegin;
    select forUpdate * from myTable;
    myTable.myField = 'xyz';
ttsCommit;

ttsBegin;
    myTable.update(); // Rejected by the ttsLevel check.
ttsCommit;
```
