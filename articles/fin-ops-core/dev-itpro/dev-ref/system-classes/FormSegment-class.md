---
title: FormSegment クラス
description: このトピックでは、FormSegment クラスについて説明します。
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
ms.openlocfilehash: 883c8b6f28a0e8e1287e27784d6300ec752d8895
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502613"
---
# <a name="class-formsegment"></a>クラス FormSegment

[!include [banner](../../includes/banner.md)]

```xpp
class FormSegment extends Object
```

FormSegment クラスは、SegmentedEntry コントロールでセグメントを表すために使用されます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                          | 説明                            |
|-----------------------------------------------------------------|----------------------------------------|
| public str text()                                               | セグメントの現在のテキストを取得します。  |
| public boolean allowEdit(\[boolean value\])                     |                                        |
| public str description(\[str description\])                     |                                        |
| public boolean enabled(\[boolean value\])                       |                                        |
| public int getIndex()                                           |                                        |
| public str name()                                               |                                        |
| public SegmentedEntryState state(\[SegmentedEntryState state\]) |                                        |
| public str value(\[str value\])                                 | セグメントの現在の値を取得します。 |

## <a name="method-text"></a>メソッド text

セグメントの現在のテキストを取得します。

```xpp
public str text()
```

### <a name="return-value---text"></a>戻り値 - text

セグメントの現在のテキスト。

### <a name="remarks---text"></a>備考 - text

このメソッドは、変更中であっても、セグメントのテキストの持続値を常に返します。 セグメントの保存された最後の値を取得するには、value メソッドを使用します。

## <a name="method-allowedit"></a>メソッド allowEdit

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

## <a name="method-description"></a>メソッドの説明

```xpp
public str description([str description])
```

### <a name="parameters---description"></a>パラメーター - description

説明  

### <a name="return-value---description"></a>戻り値 - description

## <a name="method-enabled"></a>メソッド enabled

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

## <a name="method-getindex"></a>メソッド getIndex

```xpp
public int getIndex()
```

### <a name="return-value---getindex"></a>戻り値 - getIndex

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-state"></a>メソッド state

```xpp
public SegmentedEntryState state([SegmentedEntryState state])
```

### <a name="parameters---state"></a>パラメーター - state

状態  

### <a name="return-value---state"></a>戻り値 - state

## <a name="method-value"></a>メソッド value

セグメントの現在の値を取得します。

```xpp
public str value([str value])
```

### <a name="parameters---value"></a>パラメーター - value

値  

### <a name="return-value---value"></a>戻り値 - value

セグメントの現在の値。

### <a name="remarks---value"></a>備考 - value

このメソッドは、変更中であっても、セグメントの現在の持続値を常に返します。 コントロールの現在のテキストを取得するには、text メソッドを使用します。

