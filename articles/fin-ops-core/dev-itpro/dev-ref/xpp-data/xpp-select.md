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
# <a name="select-data"></a>データの選択

[!include [banner](../../includes/banner.md)]

**select** ステートメントは、データベースからデータをフェッチまたは操作します。

+ すべての **選択** ステートメントではレコードをフェッチするためテーブル変数を使用します。 この変数は、**select** 文を実行する前に宣言する必要があります。
+ **select** ステートメントは、レコードを 1 つだけ、またはフィールドをフェッチします。 複数のレコードをフェッチまたは移動したりするには、**next** ステートメントまたは **[while select](xpp-while-select.md)** ステートメントを使用できます。

    + **next** ステートメントは、テーブルの次のレコードをフェッチします。 **選択** ステートメントの前に、**次** ステートメントがある場合、エラーが発生します。 **次** ステートメントを使用する場合、**firstOnly** 検索オプションを使用しません。
    + **while select** ステートメントを使用して複数のレコードを移動する方がより適切です。

+ **select** ステートメントの結果はテーブル バッファ変数に返されます。
+ **選択** ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。

次の例では、CustTable テーブルの最初の行のすべての列をフェッチし、その行の **AccountNum** 列に値を出力します。

```xpp
CustTable custTable;
select * from custTable;
info("AccountNum: " + custTable.AccountNum);
```

次の例では、CustTable テーブルで各行の **AccountNum** 列の値を出力します。

```xpp
CustTable custTable;
while select * from custTable
{
    info("AccountNum: " + custTable.AccountNum);
}
```

次の例では、**select** ステートメントによって返された最初の 2 つの行の **AccountNum** 列の値を出力します。

```xpp
CustTable custTable;
select * from custTable;
info("AccountNum: " + custTable.AccountNum);

next custTable;
info("AccountNum: " + custTable.AccountNum);
```

詳細については、[select ステートメント](xpp-select-statement.md)を参照してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]