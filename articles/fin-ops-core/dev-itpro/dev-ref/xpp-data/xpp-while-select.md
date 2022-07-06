---
title: 明細書の選択中
description: この記事では、X++ 言語での while select ステートメントについて説明します。
author: tonyafehr
ms.date: 06/16/2020
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: c7cd85590aa5c22154279f8666265455c9618098
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867177"
---
# <a name="while-select-statement"></a>明細書の選択中

[!include [banner](../../includes/banner.md)]

**while select** ステートメントは、データの処理に使用されます。 **select** ステートメントの最も広く使用されている形式です。 **while select** ステートメントは、特定の基準を満たす多くのレコードをループし、各レコードでステートメントを実行することができます。 **while select** ステートメントの構文は、**select** ステートメントの構文に似ていますが、このステートメントは **select** ではなく **while select** により処理されます。

+ 通常、データ操作のために **while select** ステートメントを使用する場合、トランザクション内でデータ整合性を確保するために使用します。
+ **while select** ステートメントの結果はテーブル バッファ変数に返されます。
+ **選択** ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。
+ **sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。 整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。
+ **select** ステートメント自体は、ループのステートメントの最初の繰り返しの直前に 1 回だけ実行されます。
+ **while select** ステートメントに追加されたプール式 (例えば、**iCounter &lt; 1**) は 1 度だけテストされます。 この動作は、C ++ や C\# などの言語の **while** 文の動作とは異なります。 たとえば、次のループは、複数回繰り返します。

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

次の例では、アカウント番号が指定された範囲内にある CustTable テーブルのすべての顧客の **AccountNum** と **SalesGroup** の値を出力します。

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