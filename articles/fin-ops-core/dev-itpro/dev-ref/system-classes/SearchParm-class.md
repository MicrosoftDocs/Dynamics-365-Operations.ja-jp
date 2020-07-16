---
title: SearchParm クラス
description: このトピックでは、SearchParm クラスについて説明します。
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
ms.openlocfilehash: c06c6cb4c8391d1e5ddefb54a20296985b4c87ed
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502816"
---
# <a name="class-searchparm"></a>クラス SearchParm

[!include [banner](../../includes/banner.md)]

```xpp
class SearchParm extends Object
```

SearchParm クラスは、カーネルと sysTreeSearch クラス間のインターフェイスとして機能し、アプリケーション オブジェクト ツリー (AOT) で検索できるようにします。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                          | 説明 |
|-------------------------------------------------|-------------|
| public str nodeName(\[str name\])               |             |
| public int nodeType(\[int type\])               |             |
| public str nodeTypeArray()                      |             |
| public str propertyName(\[str name\])           |             |
| public str propertyValue(\[str value\])         |             |
| public str replaceString(\[str replaceString\]) |             |
| public int searchFlag(\[int flag\])             |             |
| public str searchString(\[str searchString\])   |             |
| public int searchType(\[int type\])             |             |
| public boolean startSearch()                    |             |
| public TreeNode topNode(\[TreeNode node\])      |             |
| public str topNodeName(\[str name\])            |             |
| public int topNodeType(\[int type\])            |             |
| public void preSearch()                         |             |
| public void killSearch()                        |             |

## <a name="method-nodename"></a>メソッド nodeName

```xpp
public str nodeName([str name])
```

### <a name="parameters---nodename"></a>パラメーター - nodeName

名前  

### <a name="return-value---nodename"></a>戻り値 - nodeName

## <a name="method-nodetype"></a>メソッド nodeType

```xpp
public int nodeType([int type])
```

### <a name="parameters---nodetype"></a>パラメーター - nodeType

タイプ  

### <a name="return-value---nodetype"></a>戻り値 - nodeType

## <a name="method-nodetypearray"></a>メソッド nodeTypeArray

```xpp
public str nodeTypeArray()
```

### <a name="return-value---nodetypearray"></a>戻り値 - nodeTypeArray

## <a name="method-propertyname"></a>メソッド propertyName

```xpp
public str propertyName([str name])
```

### <a name="parameters---propertyname"></a>パラメーター - propertyName

名前  

### <a name="return-value---propertyname"></a>戻り値 - propertyName

## <a name="method-propertyvalue"></a>メソッド propertyValue

```xpp
public str propertyValue([str value])
```

### <a name="parameters---propertyvalue"></a>パラメーター - propertyValue

値  

### <a name="return-value---propertyvalue"></a>戻り値 - propertyValue

## <a name="method-replacestring"></a>メソッド replaceString

```xpp
public str replaceString([str replaceString])
```

### <a name="parameters---replacestring"></a>パラメーター - replaceString

replaceString  

### <a name="return-value---replacestring"></a>戻り値 - replaceString

## <a name="method-searchflag"></a>メソッド searchFlag

```xpp
public int searchFlag([int flag])
```

### <a name="parameters---searchflag"></a>パラメーター - searchFlag

flag  

### <a name="return-value---searchflag"></a>戻り値 - searchFlag

## <a name="method-searchstring"></a>メソッド searchString

```xpp
public str searchString([str searchString])
```

### <a name="parameters---searchstring"></a>パラメーター - searchString

searchString  

### <a name="return-value---searchstring"></a>戻り値 - searchString

## <a name="method-searchtype"></a>メソッド searchType

```xpp
public int searchType([int type])
```

### <a name="parameters---searchtype"></a>パラメーター - searchType

タイプ  

### <a name="return-value---searchtype"></a>戻り値 - searchType

## <a name="method-startsearch"></a>メソッド startSearch

```xpp
public boolean startSearch()
```

### <a name="return-value---startsearch"></a>戻り値 - startSearch

## <a name="method-topnode"></a>メソッド topNode

```xpp
public TreeNode topNode([TreeNode node])
```

### <a name="parameters---topnode"></a>パラメーター - topNode

node  

### <a name="return-value---topnode"></a>戻り値 - topNode

## <a name="method-topnodename"></a>メソッド topNodeName

```xpp
public str topNodeName([str name])
```

### <a name="parameters---topnodename"></a>パラメーター - topNodeName

名前  

### <a name="return-value---topnodename"></a>戻り値 - topNodeName

## <a name="method-topnodetype"></a>メソッド topNodeType

```xpp
public int topNodeType([int type])
```

### <a name="parameters---topnodetype"></a>パラメーター - topNodeType

タイプ  

### <a name="return-value---topnodetype"></a>戻り値 - topNodeType

## <a name="method-presearch"></a>メソッド preSearch

```xpp
public void preSearch()
```

## <a name="method-killsearch"></a>メソッド killSearch

```xpp
public void killSearch()
```

