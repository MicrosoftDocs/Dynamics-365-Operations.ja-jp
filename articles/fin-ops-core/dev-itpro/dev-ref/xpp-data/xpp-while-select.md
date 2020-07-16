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
# <a name="while-select-statement"></a>while select ステートメント

[!include [banner](../../includes/banner.md)]

**while select** ステートメントは、データの処理に使用されます。 **select** ステートメントの最も広く使用されている形式です。 **while select** ステートメントは、特定の基準を満たす多くのレコードをループし、各レコードでステートメントを実行することができます。 **while select** ステートメントの構文は、**select** ステートメントの構文に似ていますが、このステートメントは**select** ではなく **while select** により処理されます。

+ 通常、データ操作のために **while select** 文を使用する場合、トランザクション内でデータ整合性を確保するために使用します。
+ **while select** ステートメントの結果はテーブル バッファ変数に返されます。
+ **選択**ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。
+ **sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。 整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。
+ **select** ステートメント自体は、ループのステートメントの最初の繰り返しの直前に 1 回だけ実行されます。
+ **while select** に追加されたブール式 (**iCounter &lt; 1** など) は 1 度だけテストされます。 この動作は、C ++ や C\# などの言語の **while** 文の動作とは異なります。 たとえば、次のループは、複数回繰り返します。

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

次の例では、アカウント番号が指定された範囲内にある **CustTable** テーブルのすべての顧客の **AccountNum** と **SalesGroup** を出力します。

```xpp
CustTable custTable;

while select custTable
    order by custTable.AccountNum
    where  custTable.AccountNum >= '4010' && custTable.AccountNum <= '4100'
{
    info(strFmt("%1 , %2", custTable.AccountNum, custTable.SalesGroup));
}
```
