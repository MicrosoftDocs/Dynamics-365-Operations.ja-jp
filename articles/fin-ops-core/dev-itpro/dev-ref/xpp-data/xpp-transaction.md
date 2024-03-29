---
title: X++ トランザクションの整合性
description: この記事では、X++ 言語でのトランザクションの整合性について説明します。
author: josaw1
ms.date: 06/16/2020
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 780c3f3ab7d4e0240e41c2e44922546ceb03c1a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271339"
---
# <a name="x-transactional-integrity"></a>X++ トランザクションの整合性

[!include [banner](../../includes/banner.md)]

この記事では、X++ 言語でのトランザクションの整合性について説明します。

トランザクションの整合性を確認する手順を踏まなかった場合、データが破損する可能性があります。 少なくとも、システム上の同時ユーザーに関してスケーラビリティが低下する可能性があります。 **forUpdate** チェックと **ttsLevel** チェックの 2 つの内部チェック機能がトランザクションの安全性を保証します。

- **forUpdate** チェックは、更新のために最初に選択されたレコードのみを更新または削除されるのを確認するのに役立ちます。 **select** ステートメント内の **forUpdate** キーワードまたはテーブル上の **selectForUpdate** メソッドのいずれかを使用することで、更新プログラムのレコードを選択することができます。
- **ttsLevel** チェックは、レコードが更新のために選択されたのと同じトランザクション範囲内でのみ更新または削除できることを保証するのに役立ちます。

整合性を確保するために、次のステートメントを使用します。

- **ttsBegin** – このステートメントは、トランザクションの開始位置を示します。 これにより、データの整合性が確保され、トランザクションが終了するまで (**ttsCommit** または **ttsAbort** を通じて) 実行されるすべての更新が一貫していることも保証します。
- **ttsCommit** – このステートメントは、トランザクションの正常終了を示します。 トランザクションを終了してコミットします。 財務と運用アプリにより、確定されたトランザクションが意図に従って実行されます。
- **ttsAbort** – このステートメントを使用すると、現在のトランザクションのすべての変更を明示的に破棄できます。 この場合、データベースは元の状態にロールバックされ、何も変更されていません。 この文は通常、ユーザーが現在のジョブを中断したいことを検出した場合に使用します。 **ttsAbort** ステートメントは、データベースが一貫していることを保証するのに役立ちます。

通常、**ttsAbort** の代わりに、例外処理を使用することをお勧めします。 **throw** ステートメントは、自動的に現在のトランザクションを中断します。 次の例が示すように、**ttsBegin** と **ttsCommit** の間の明細書には 1 つ以上のトランザクション ブロックを含めることができます。 そのような場合、最後の **ttsCommit** ステートメントが正常に終了するまでコミットされるものはありません。

```xpp
ttsBegin;
    // Some statements.
    ttsBegin;
        // More statements.
    ttsCommit;
ttsCommit;
```

次の例では、レコードのセットを選択し、**CustGroup** フィールドを更新します。 このコードは、**select** ステートメントがレコードを返さない場合、例外をスローし ます。

```xpp
Custtable custTable;
ttsBegin;
    select forUpdate custTable where custTable.AccountNum == '5000';
    custTable.CustGroup = '1';
    custTable.update();
ttsCommit;
```

## <a name="example-of-code-that-is-rejected-by-the-forupdate-check"></a>forUpdate チェックにより拒否されたコードの例

この例では、**forUpdate** キーワードがないため、最初のエラーが発生します。 

```xpp
ttsBegin;
    select myTable; // Rejected by the forUpdate check.
    mytable.myField = 'xyz';
    myTable.update();
ttsCommit;
```

## <a name="example-of-code-that-is-rejected-by-the-ttslevel-check"></a>ttsLevel チェックにより拒否されたコードの例

この例では、更新のトランザクション スコープが、レコードが **ttsCommit** の更新用に選択されたトランザクション スコープとは異なるためにエラーが発生します。

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
