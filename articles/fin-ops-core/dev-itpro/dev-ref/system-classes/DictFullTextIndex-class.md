---
title: DictFullTextIndex クラス
description: このトピックでは、DictFullTextIndex クラスについて説明します。
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
ms.openlocfilehash: eeea7ee61da8d6cc49f440dff77364f526f1aae9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502987"
---
# <a name="class-dictfulltextindex"></a>クラス DictFullTextIndex

[!include [banner](../../includes/banner.md)]

```xpp
class DictFullTextIndex extends Object
```

DictFullTextIndex クラスは、フル テキスト インデックスに関するメタデータを返します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                  | 説明                                            |
|---------------------------------------------------------|--------------------------------------------------------|
| public FullTextIndexChangeTracking changeTrackingMode() | フル テキスト インデックスの変更追跡モードを取得します。  |
| public ConfigurationKeyId configurationKeyId()          | インデックスのコンフィギュレーション キーの ID を返します。 |
| public IndexId id()                                     | フル テキスト インデックスの ID を取得します。                    |
| public str name()                                       | フル テキスト インデックスの名前を取得します。                  |
| public TableId tableid()                                | インデックスを含むテーブルの ID を返します。   |
| public void new(TableId tableId, IndexId indexId)       | Object クラスの新しいインスタンスを初期化します。        |

## <a name="method-changetrackingmode"></a>メソッド changeTrackingMode

フル テキスト インデックスの変更追跡モードを取得します。

```xpp
public FullTextIndexChangeTracking changeTrackingMode()
```

### <a name="return-value---changetrackingmode"></a>戻り値 - changeTrackingMode

## <a name="method-configurationkeyid"></a>メソッド configurationKeyId

インデックスのコンフィギュレーション キーの ID を返します。

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a>戻り値 - configurationKeyId

インデックスのコンフィギュレーション キーの ID。インデックスにコンフィギュレーション キーがない場合は 0 (ゼロ)。

## <a name="method-id"></a>メソッド id

フル テキスト インデックスの ID を取得します。

```xpp
public IndexId id()
```

### <a name="return-value---id"></a>戻り値 - id

インデックスの ID です。

## <a name="method-name"></a>メソッド名

フル テキスト インデックスの名前を取得します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

インデックスの名前。

## <a name="method-tableid"></a>メソッド tableid

インデックスを含むテーブルの ID を返します。

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a>戻り値 - tableid

インデックスを含むテーブルの ID。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(TableId tableId, IndexId indexId)
```

### <a name="parameters---new"></a>パラメーター - new

tableId  

<!-- -->

indexId  

