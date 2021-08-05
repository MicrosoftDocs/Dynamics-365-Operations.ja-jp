---
title: データの更新
description: このトピックでは、X++ 言語での update および doUpdate メソッドについて説明します。
author: RobinARH
ms.date: 06/16/2020
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 5b711920487704a211a20a9352edd9289309ca48
ms.sourcegitcommit: ff5e892a91a1585472af2191ae45d6291cceb7f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2021
ms.locfileid: "6661412"
---
# <a name="update-data"></a>データの更新

[!include [banner](../../includes/banner.md)]

データベースに格納されているテーブルの 1 つまたは複数の行を更新するため、SQL ステートメントを対話的またはソース コード内で使用できます。

+ **[update メソッド](#update-method)** – バッファーの内容で現在のレコードを更新します。 また、適切なシステム フィールドも更新します。
+ **[doUpdate メソッド](#do-update-method)** – 一度に 1 行を更新します。
+ **[update\_recordset ステートメント](#update-recordset-statement)** – 複数のレコードを 1 回のデータベース トリップで更新します。 **update\_recordset** ステートメントを使用することにより、アプリケーションとデータベース間の通信が減少します。 したがって、パフォーマンスの向上に役立ちます。 場合によっては、レコードのセットに基づく操作をレコードごとの操作に戻すことができます。 詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。

## <a name="update-method"></a><a id="update-method"></a>update メソッド

**update** メソッドは、バッファーの内容で現在のレコードを更新します。 また、適切なシステム フィールドも更新されます。 オプションの **where** 句は、テーブルの各行を処理するときに **update** メソッドでテストされる条件を指定します。 その条件に対する **true** をテストする行のみ新しい値で更新されます。

次の例では、更新する CustTable テーブルを選択します。 **AccountNum** フィールドの値が **4000** に等しいレコードのみが更新されます。 **next** への呼び出しはなく、この例では **select while** ステートメントを使用していないため、1 つのレコードのみが更新されます。 **CreditMax** フィールドの値が **5000** に変更されます。

```xpp
CustTable custTable;
ttsBegin;
    select forUpdate custTable
        where custTable.AccountNum == '4000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

## <a name="doupdate-method"></a><a id="do-update-method"></a>doUpdate メソッド

**update** メソッドの動作をオーバーライドするには、**doUpdate** メソッドを使用します。 **doUpdate** メソッドは、バッファーの内容で現在のレコードを更新します。 また、適切なシステム フィールドも更新されます。 テーブルでの **更新** メソッドをバイパスする必要があるときは、**doUpdate** メソッドを使用する必要があります。 **doUpdate** テーブル メソッドの構文は、**void doUpdate()** です。

> [!WARNING]
> **doUpdate** の呼び出しは、データベース イベント ハンドラー (たとえば **onUpdating** および **onUpdated**)、コマンド チェーン **onUpdate()**、および **update()** の呼び出し自体を含むすべてのロジックをスキップします。 一般に、**doUpdate** を使用することは不適切なプラクティスと見なされており、使用することはお勧めしません。

```xpp
CustTable custTable;
ttsBegin;
select forUpdate custTable
    where custTable.CreditMax == 3000;
if (custTable)
{
    custTable.CreditMax += 1000;
    custTable.doUpdate();
}
ttsCommit;
```

## <a name="update_recordset-statement"></a><a id="update-recordset-statement"></a>update\_recordset ステートメント

**update\_recordset** 演算子は、サーバーへの 1 回のアクセスで複数のレコードを更新するレコード セット ベースの演算子です。 したがって、Microsoft SQL Server の機能は、一部のタスクのパフォーマンスを向上させるのに役立ちます。 **update\_recordset** ステートメントは X++ の **delete\_from** と SQL の **update set** に似ています。 フェッチ、変更、および更新によって各レコードを個別に取得することはありません。 代わりに、データベース サーバー側の SQL スタイル レコード セットで機能します。 **更新** メソッドがオーバーライドされた場合、実装は、一度に 1 つのレコードが更新される古典的なループ構造に戻されます。 (この動作は、削除対象の **削除の\_対象** の動作に似ています。) したがって、構築は、一時テーブルとテーブル全体 - キャッシュされたテーブルで、ループ構造を使用して動作します。

次の例では、CustTable テーブルを更新し、**CreditMax** の値が **0** (ゼロ) よりも大きいレコードに対して **CreditMax** 列の値を **1000** 増分します。

```xpp
CustTable custTable;
ttsBegin;
update_recordset custTable
    setting CreditMax = custTable.CreditMax + 1000
    where custTable.CreditMax > 0;
ttsCommit;
```

次の例では、複数の列を更新します。

```xpp
CustTable custTable;
ttsBegin;
update_recordset custTable
    setting
        CreditMax = custTable.CreditMax + 1000,
        AccountStatement = CustAccountStatement::Always
    where custTable.CreditMax > 0;
ttsCommit;
```

次の例は、**update\_recordset** ステートメントが複数のテーブルの結合をサポートしていることを示しています。 結合されたテーブルのデータを使用して、更新中のテーブル内のフィールドに値を割り当てることができます。

```xpp
TableEmployee tabEmpl;
TableDepartment tabDept;
TableProject tabProj;
update_recordset tabEmpl
    setting
        currentStatusDescription = tabDept.DeptName + ", " + tabProj .ProjName
join tabDept
    where tabDept.DeptId == tabEmpl.DeptId
join tabProj
    where tabProj.ProjId == tabEmpl .ProjId;
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]