---
title: データの選択
description: この記事では、X++ 言語での select ステートメントについて説明します。
author: josaw1
ms.date: 08/27/2021
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac1b9fdf8792ff91229daa84df5f3972b0ef8aa3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271347"
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
select firstonly custTable; //this is a short notation for 'select firstonly * from custTable;'  
info("AccountNum: " + custTable.AccountNum);
```

次の例では、CustTable テーブルで各行の **AccountNum** 列の値を出力します。

```xpp
CustTable custTable;
while select custTable
{
    info("AccountNum: " + custTable.AccountNum);
}
```

次の例では、**select** ステートメントによって返された最初の 2 つの行の **AccountNum** 列の値を出力します。

```xpp
CustTable custTable;
select custTable;
info("AccountNum: " + custTable.AccountNum);

next custTable;
info("AccountNum: " + custTable.AccountNum);
```

詳細については、[select ステートメント](xpp-select-statement.md)を参照してください。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
