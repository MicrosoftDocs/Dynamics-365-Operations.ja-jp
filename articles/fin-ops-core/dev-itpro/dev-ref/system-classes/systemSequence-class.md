---
title: systemSequence クラス
description: このトピックでは、systemSequence クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef5dddfa74bd867868a98addd0804cac7e65178b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503000"
---
# <a name="class-systemsequence"></a>クラス systemSequence

[!include [banner](../../includes/banner.md)]

```xpp
class systemSequence extends Object
```

systemSequence クラスは、システム シーケンス ジェネレータを手動で制御し、すべての SQL テーブルに対して一意の RecIds を提供します。

## <a name="remarks"></a>備考

SQL テーブルにレコードが挿入されると、各レコードが関連付けられている会社に関係なく、各レコードに一意の RecId が割り当てられます。 このクラスを使用するときは十分に注意してください。データの整合性が失われる可能性があります。 このクラスは、通常、データのインポートやエクスポート ルーチン、または非常に大きなジョブに使用されます。 レコード ID は、int64 データ型の値です。 レコード ID が割り当てられる範囲は、5637144576 から 2 ^ 63 (9223372036854775808) までです。 大きい未使用の RecId 範囲が作成された場合、途中で RecId がなくなることがあります。 使用されている Recid 範囲の間にある未使用の RecId 範囲を再利用するのは、非常に複雑なプロセスです。

## <a name="examples"></a>例

次の例では、CustTable テーブルの int64max 値を予約しています。

```xpp
static public void Main(Args _args) 
{ 
    systemSequence seq; 
    seq = new SystemSequence(); 
    if (seq) 
    { 
        // Allocate 20 recordIds for CustTable table. 
        seq.reserveValues(20, tablenum(CustTable)); 
        // Suspend automatic recId allocation. 
        Seq.suspendRecIds(tablenum(CustTable)); 
        // Manually generate recIds in the range allocated. 
        // Remove the recId suspension. 
        Seq.removeRecIdSuspension(); 
      } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                             | 説明                                                                                                                     |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| public Int64 flushValues(TableId tableId)                          | 指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。                                                    |
| public Int64 reserveTransids(Int64 nReserved, \[TableId tableId\]) |                                                                                                                                 |
| public Int64 reserveValues(Int64 nReserved, TableId tableId)       | recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。 |
| public void suspendTransIds(TableId tableId)                       |                                                                                                                                 |
| public void suspendRecIds(TableId tableId)                         |                                                                                                                                 |
| public void removeRecIdSuspension(\[TableId tableId\])             |                                                                                                                                 |
| public void new()                                                  | systemSequence クラスの新しいインスタンスを初期化します。                                                                         |
| public void removeTransIdSuspension(\[TableId tableId\])           |                                                                                                                                 |

## <a name="method-flushvalues"></a>メソッド flushValues

指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。

```xpp
public Int64 flushValues(TableId tableId)
```

### <a name="parameters---flushvalues"></a>パラメーター - flushValues

tableId  

### <a name="return-value---flushvalues"></a>戻り値 - flushValues

キャッシュからフラッシュされた recIds の数。

### <a name="remarks---flushvalues"></a>備考 - flushValues

テーブルへのその後挿入によりテーブルの recId が予約され、システム シーケンス キャッシュにはテーブルの recId の予約済み範囲が入力されます。

## <a name="method-reservetransids"></a>メソッド reserveTransids

```xpp
public Int64 reserveTransids(Int64 nReserved, [TableId tableId])
```

### <a name="parameters---reservetransids"></a>パラメーター - reserveTransids

nReserved  

<!-- -->

tableId  

### <a name="return-value---reservetransids"></a>戻り値 - reserveTransids

## <a name="method-reservevalues"></a>メソッド reserveValues

recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。

```xpp
public Int64 reserveValues(Int64 nReserved, TableId tableId)
```

### <a name="parameters---reservevalues"></a>パラメーター - reserveValues

nReserved  

<!-- -->

tableId  

### <a name="return-value---reservevalues"></a>戻り値 - reserveValues

最初に使用可能な予約済み recId。

### <a name="remarks---reservevalues"></a>備考 - reserveValues

予約した recIds の範囲は、すぐに予約されています。

## <a name="method-suspendtransids"></a>メソッド suspendTransIds

```xpp
public void suspendTransIds(TableId tableId)
```

### <a name="parameters---suspendtransids"></a>パラメーター - suspendTransIds

tableId  

## <a name="method-suspendrecids"></a>メソッド suspendRecIds

```xpp
public void suspendRecIds(TableId tableId)
```

### <a name="parameters---suspendrecids"></a>パラメーター - suspendRecIds

tableId  

## <a name="method-removerecidsuspension"></a>メソッド removeRecIdSuspension

```xpp
public void removeRecIdSuspension([TableId tableId])
```

### <a name="parameters---removerecidsuspension"></a>パラメーター - removeRecIdSuspension

tableId  

## <a name="method-new"></a>メソッド new

systemSequence クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-removetransidsuspension"></a>メソッド removeTransIdSuspension

```xpp
public void removeTransIdSuspension([TableId tableId])
```

### <a name="parameters---removetransidsuspension"></a>パラメーター - removeTransIdSuspension

tableId  



