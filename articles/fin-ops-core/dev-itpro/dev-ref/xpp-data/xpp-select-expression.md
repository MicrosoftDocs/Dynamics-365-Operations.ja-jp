---
title: select ステートメントを式として記述
description: この記事では、select ステートメントを式として使用する方法について説明します。
author: josaw1
ms.date: 06/16/2020
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3d2f5be90f797903989f0a2209bc80e5967aec2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271343"
---
# <a name="write-select-statements-as-expressions"></a>select ステートメントを式として記述

[!include [banner](../../includes/banner.md)]

**select** ステートメントを式として使用することができます。 このタイプの **select** ステートメントは *式 **select** ステートメント* と呼ばれます。

+ テーブル バッファ変数は、式 **select** ステートメントで使用できません。
+ テーブルの名前は、**from** 句で使用する必要があります。
+ **結合** キーワードはサポートされていません。
+ **order by** 句でフィールド名を修飾するために、テーブル名を使用することはできません。
+ **where** 句では、テーブル名をフィールドの修飾子として使用する必要があります。
+ 式の **select** ステートメントで言及できるのは 1 つのテーブルのみです。 したがって、サブセレクトは、サポートされていない **join** キーワードの回避策としてサポートされていません。
+ データを入力できる唯一の列は、**select** 句の **from** 句の前に名前が付けられた列です。
+ 閉じ括弧の後に、列の名前を使用してデータ値を参照します。

次の式は、CustTable テーブルの最初の行 (行が存在する場合) の **AccountNum** 列の値を返します。

```xpp
str accountNum = (select AccountNum from CustTable order by AccountNum desc).AccountNum;
info('Max AccountNum: ' + accountNum);
```

前の例と同じ結果を達成する単純な方法を次に示します。

```xpp
str accountNum = (select maxof(AccountNum) from CustTable).AccountNum;
info('Max AccountNum: ' + accountNum);
```

次の例では、ブロックされていない顧客の最大 **RecId** 値を返します。 ここで、**maxof** 集計関数が使用され、**RecId** フィールドが機能に記載されます。 集計関数に記載されているフィールドは、閉じかっこの後のデータ値を参照するために使用されるフィールド名と一致していなければなりません。 それ以外の場合、空のデータが返されます。

```xpp
int64 nRecId = (select maxof(RecId) from CustTable
            where CustTable.Blocked == CustVendorBlocked::No).RecId;
info("Max RecId: " + int642Str(nRecId));
```

次の例では、**RecId** フィールドは **RecId** の値ではないデータ値を参照するために使用します。 **count** 集計関数は、**RecId** 値を返しません。 **RecId** フィールドは通常 **count** 関数と共に使用するのが一般的なプラクティスです。

```xpp
int64 nRecId = (select count(RecId) from CustTable
            where CustTable.Blocked == CustVendorBlocked::No).RecId;
info('Count of unblocked customers: ' + int642Str(nRecId));
```

## <a name="select-statements-on-fields"></a>フィールド上の select ステートメント

**select** ステートメントをフィールド上のルックアップで使用することができます。 テーブルのレコードをフェッチする **選択** ステートメントの後、**.fieldName** を入力してテーブルのフィールドを参照することができます。 これらの **select** ステートメントは、式で使用する必要があります。 *通常の **select** ステートメント* は、*フィールド **select** ステートメント* と次の点で異なります。

+ フィールド **select** ステートメントはテーブル上で直接動作します。
+ 通常の **select** ステートメントは、テーブル バッファ変数で動作します。

次の例では、select ステートメントからフィールドにアクセスする方法を示します。

```xpp
print((select CustTable order by AccountStatement).AccountStatement);

if ((select custTable where CustTable.AccountNum == '3000').CreditMax < 5000)
{
    info('This customer has a credit maximum less than $5000.');
}
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
