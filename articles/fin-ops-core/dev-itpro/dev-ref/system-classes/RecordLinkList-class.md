---
title: RecordLinkList クラス
description: このトピックでは、RecordLinkList クラスについて説明します。
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
ms.openlocfilehash: af06ffe02fe54b794074bd6d6bc997f0a0e86cfb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502855"
---
# <a name="class-recordlinklist"></a>クラス RecordLinkList

[!include [banner](../../includes/banner.md)]

```xpp
class RecordLinkList extends Object
```

RecordLinkList クラスは、さまざまな種類のレコードを保持することができ、キー入力も並べ替えもされていないレコード バッファーのキャッシュを動的に作成します。

## <a name="remarks"></a>備考

RecordLinkList オブジェクトは、同時にさまざまなタイプのレコードを保持できる二重にリンクされたリストです。 キー入力や並べ替えはされません。 recordLinkList オブジェクトは、同じレコードを再度取得するのではなく、異なるテーブルのレコードをパラメーターとして渡す場合に特に便利です。 recordSortedList オブジェクトのサイズに制限はありません。 そのサイズおよびメモリ消費を制御するのはプログラマーの責任です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                           | 説明                                                                                                                                |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| public int del()                                 | リスト内の現在の位置のレコードを削除します。                                                                                    |
| public TableId fileId()                          | リスト内の現在の位置のレコードのテーブル ID を取得します。                                                                  |
| public boolean first(\[Common record\])          | 一覧の最初のレコードにポインターを設定し、存在する場合は、提供されるバッファーにレコードをコピーします。                |
| public boolean get(Common record, \[int index\]) | 現在の位置、または指定された位置のレコードを、指定されたレコード バッファーにコピーします。ただし、ポインタの位置には影響しません。 |
| public int ins(Common record)                    | リストの最後にレコードを挿入します。                                                                                                     |
| public boolean last(\[Common record\])           | 最後のレコードにリストを配置し、レコードを指定されたレコード バッファにコピーします。                                                     |
| public int len()                                 | リスト内の現在のレコード数を返します。                                                                                         |
| public boolean next(\[Common record\])           | 次のレコードにカーソルを置き、指定されたバッファーにコピーします。                                                                  |
| public Common peek()                             | リスト内の現在の位置のレコードを取得します。                                                                                  |
| public boolean prev(\[Common record\])           | リスト内の前のレコードにポインターを配置し、レコードを指定されたバッファーにコピーします。                                         |
| public void new()                                | RecordLinkList クラスの新しいインスタンスを初期化します。                                                                                    |

## <a name="method-del"></a>メソッド del

リスト内の現在の位置のレコードを削除します。

```xpp
public int del()
```

### <a name="return-value---del"></a>戻り値 - del

リストに残っているレコードの数。

## <a name="method-fileid"></a>メソッド fileId

リスト内の現在の位置のレコードのテーブル ID を取得します。

```xpp
public TableId fileId()
```

### <a name="return-value---fileid"></a>戻り値 - fileId

テーブル ID。

## <a name="method-first"></a>メソッド first

一覧の最初のレコードにポインターを設定し、存在する場合は、提供されるバッファーにレコードをコピーします。

```xpp
public boolean first([Common record])
```

### <a name="parameters---first"></a>パラメーター - first

記録  
結果を含むレコード バッファ (オプション)。

### <a name="return-value---first"></a>戻り値 - first

メソッドが成功する場合は true。レコードが存在しない場合は false。

## <a name="method-get"></a>メソッド get

現在の位置、または指定された位置のレコードを、指定されたレコード バッファーにコピーします。ただし、ポインタの位置には影響しません。

```xpp
public boolean get(Common record, [int index])
```

### <a name="parameters---get"></a>パラメーター - get

記録  
現在のレコードが取得されていない場合に取得するリスト内のレコードの番号 (オプション)。

<!-- -->

指数  
現在のレコードが取得されていない場合に取得するリスト内のレコードの番号 (オプション)。

### <a name="return-value---get"></a>戻り値 - get

レコードを取得できる場合は true。それ以外の場合は、false。

## <a name="method-ins"></a>メソッド ins

リストの最後にレコードを挿入します。

```xpp
public int ins(Common record)
```

### <a name="parameters---ins"></a>パラメーター - ins

記録  
挿入するレコードを保持するために使用するレコード バッファ。

### <a name="return-value---ins"></a>戻り値 - ins

リスト内の要素の数。

## <a name="method-last"></a>メソッド last

最後のレコードにリストを配置し、レコードを指定されたレコード バッファにコピーします。

```xpp
public boolean last([Common record])
```

### <a name="parameters---last"></a>パラメーター - last

記録  
取得されたレコードを保持するために使用するレコード バッファ、オプション。

### <a name="return-value---last"></a>戻り値 - last

メソッドが成功する場合は true。リスト内にレコードが存在しない場合は false。

## <a name="method-len"></a>メソッド len

リスト内の現在のレコード数を返します。

```xpp
public int len()
```

### <a name="return-value---len"></a>戻り値 - len

リスト内のレコードの数。

## <a name="method-next"></a>メソッド next

次のレコードにカーソルを置き、指定されたバッファーにコピーします。

```xpp
public boolean next([Common record])
```

### <a name="parameters---next"></a>パラメーター - next

記録  
ポジションにあるレコードと同じ型のレコード バッファ (オプション)。

### <a name="return-value---next"></a>戻り値 - next

メソッドが成功する場合は true。さらにレコードが存在しない場合は false。

## <a name="method-peek"></a>メソッド peek

リスト内の現在の位置のレコードを取得します。

```xpp
public Common peek()
```

### <a name="return-value---peek"></a>戻り値 - peek

レコードが見つかった場合のレコード バッファ。

## <a name="method-prev"></a>メソッド prev

リスト内の前のレコードにポインターを配置し、レコードを指定されたバッファーにコピーします。

```xpp
public boolean prev([Common record])
```

### <a name="parameters---prev"></a>パラメーター - prev

記録  
コピーするレコードと同じ型のレコード バッファ (オプション)。

### <a name="return-value---prev"></a>戻り値 - prev

ポインターが最初のレコード上にない場合は true。それ以外の場合は、false。

## <a name="method-new"></a>メソッド new

RecordLinkList クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

