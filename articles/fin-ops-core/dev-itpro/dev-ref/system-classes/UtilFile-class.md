---
title: UtilFile クラス
description: このトピックでは、UtilFile クラスについて説明します。
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
ms.openlocfilehash: 09a89fec9372dc62abbf9a9441624d70293e6951
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502780"
---
# <a name="class-utilfile"></a>クラス UtilFile

[!include [banner](../../includes/banner.md)]

```xpp
class UtilFile extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                      |
|-------------------------------------------------------------|------------------------------------------------------------------|
| public boolean aodFileExist(UtilEntryLevel layer)           |                                                                  |
| public int importAODFile(UtilEntryLevel layer, int modelId) |                                                                  |
| public str layers()                                         |                                                                  |
| public boolean needReindex()                                |                                                                  |
| public void check(str layer, str action)                    |                                                                  |
| public void new(str fileType)                               | Object クラスの新しいインスタンスを初期化します。                  |
| public void reindex()                                       | X++ コードとメタデータの作成、読み取り、更新、および削除ができます。 |
| public void flushCache()                                    |                                                                  |

## <a name="method-aodfileexist"></a>メソッド aodFileExist

```xpp
public boolean aodFileExist(UtilEntryLevel layer)
```

### <a name="parameters---aodfileexist"></a>パラメーター - aodFileExist

 レイヤー  

### <a name="return-value---aodfileexist"></a>戻り値 - aodFileExist

## <a name="method-importaodfile"></a>メソッド importAODFile

```xpp
public int importAODFile(UtilEntryLevel layer, int modelId)
```

### <a name="parameters---importaodfile"></a>パラメーター - importAODFile

 レイヤー  

<!-- -->

modelId  

### <a name="return-value---importaodfile"></a>戻り値 - importAODFile

## <a name="method-layers"></a>メソッド layers

```xpp
public str layers()
```

### <a name="return-value---layers"></a>戻り値 - layers

## <a name="method-needreindex"></a>メソッド needReindex

```xpp
public boolean needReindex()
```

### <a name="return-value---needreindex"></a>戻り値 - needReindex

## <a name="method-check"></a>メソッド check

```xpp
public void check(str layer, str action)
```

### <a name="parameters---check"></a>パラメーター - check

 レイヤー  

<!-- -->

アクション  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(str fileType)
```

### <a name="parameters---new"></a>パラメーター - new

fileType  

## <a name="method-reindex"></a>メソッド reindex

X++ コードとメタデータの作成、読み取り、更新、および削除ができます。

```xpp
public void reindex()
```

### <a name="remarks---reindex"></a>備考 - reindex

この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples---reindex"></a>例 - reindex

次の例では、UtilFile.reindex メソッドを呼び出します。 変更を実行する前に、ユーザーが必要なセキュリティ キーを持っているかどうかを確認します。

```xpp
server static public void Main(Args _args) 
{ 
    UtilFile u; 
    u = new UtilFile("util"); 
    if (u) 
    { 
        u.reindex(); 
    } 
}
```

## <a name="method-flushcache"></a>メソッド flushCache

```xpp
public void flushCache()
```


