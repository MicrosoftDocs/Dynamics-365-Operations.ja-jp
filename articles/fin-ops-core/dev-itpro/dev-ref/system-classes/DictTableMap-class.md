---
title: DictTableMap クラス
description: このトピックでは、DictTableMap クラスについて説明します。
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
ms.openlocfilehash: cbdfc6a2624d6129f29862f45e5964517162bbe5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502675"
---
# <a name="class-dicttablemap"></a>クラス DictTableMap

[!include [banner](../../includes/banner.md)]

```xpp
class DictTableMap extends Object
```

DictTableMap クラスは、テーブル マッピングに関する情報を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                 | 説明                                                    |
|----------------------------------------|----------------------------------------------------------------|
| public int table()                     | マッピングが参照するテーブルを取得します。               |
| public int fieldCnt()                  | テーブル マッピングのフィールドの数を取得します。            |
| public int fieldCnt2FieldTo(int cnt)   | マップ フィールドにより参照されているテーブル フィールドを取得します。 |
| public int fieldCnt2FieldFrom(int cnt) | テーブル フィールドを参照しているマップ フィールドを取得します。     |

## <a name="method-table"></a>メソッド table

マッピングが参照するテーブルを取得します。

```xpp
public int table()
```

### <a name="return-value---table"></a>戻り値 - toBlob

テーブル ID。

### <a name="remarks---table"></a>備考 - table

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

## <a name="method-fieldcnt"></a>メソッド fieldCnt

テーブル マッピングのフィールドの数を取得します。

```xpp
public int fieldCnt()
```

### <a name="return-value---fieldcnt"></a>戻り値 - fieldCnt

カウント。

### <a name="remarks---fieldcnt"></a>備考 - fieldCnt

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

## <a name="method-fieldcnt2fieldto"></a>メソッド fieldCnt2FieldTo

マップ フィールドにより参照されているテーブル フィールドを取得します。

```xpp
public int fieldCnt2FieldTo(int cnt)
```

### <a name="parameters---fieldcnt2fieldto"></a>パラメーター - fieldCnt2FieldTo

cnt  

### <a name="return-value---fieldcnt2fieldto"></a>戻り値 - fieldCnt2FieldTo

テーブル フィールド ID。

### <a name="remarks---fieldcnt2fieldto"></a>備考 - fieldCnt2FieldTo

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

## <a name="method-fieldcnt2fieldfrom"></a>メソッド fieldCnt2FieldFrom

テーブル フィールドを参照しているマップ フィールドを取得します。

```xpp
public int fieldCnt2FieldFrom(int cnt)
```

### <a name="parameters---fieldcnt2fieldfrom"></a>パラメーター - fieldCnt2FieldFrom

cnt  

### <a name="return-value---fieldcnt2fieldfrom"></a>戻り値 - fieldCnt2FieldFrom

マップ フィールド ID。

### <a name="remarks---fieldcnt2fieldfrom"></a>備考 - fieldCnt2FieldFrom

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

