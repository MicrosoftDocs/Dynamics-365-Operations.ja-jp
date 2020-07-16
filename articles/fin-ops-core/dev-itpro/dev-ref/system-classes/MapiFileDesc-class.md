---
title: MapiFileDesc クラス
description: このトピックでは、MapiFileDesc クラスについて説明します。
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
ms.openlocfilehash: d38168ee5890f50d0068dea0e879725f3de1b107
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502580"
---
# <a name="class-mapifiledesc"></a>クラス MapiFileDesc

[!include [banner](../../includes/banner.md)]

```xpp
class MapiFileDesc extends Object
```

MapiFileDesc クラスは、メッセージに関連付けられているファイルを取得および設定します。

## <a name="remarks"></a>備考

ファイルの説明は、ファイルの 2 つのタイプの情報で構成されています。

-   ディスク上のファイルをポイントするパス メソッド
-   fileName メソッドには、ユーザーに表示されるファイル名が含まれます。

## <a name="examples"></a>例

```xpp
static void example() 
{ 
    MapiMessage msg = New MapiMessage(); 
    MapiFileDesc attach = new MapiFileDesc(); 
    attach.Path("C:\\files\\myfile.txt"); 
}
```

## <a name="methods"></a>メソッド

| 方法                                | 説明                                           |
|---------------------------------------|-------------------------------------------------------|
| public str fileName(\[str filename\]) |                                                       |
| public str path(\[str thePath\])      |                                                       |
| public void new()                     | MapiFileDesc クラスの新しいインスタンスを初期化します。 |
| public void finalize()                |                                                       |

## <a name="method-filename"></a>メソッド fileName

```xpp
public str fileName([str filename])
```

### <a name="parameters---filename"></a>パラメーター - fileName

filename  

### <a name="return-value---filename"></a>戻り値 - fileName

## <a name="method-path"></a>メソッド path

```xpp
public str path([str thePath])
```

### <a name="parameters---path"></a>パラメーター - path

thePath  

### <a name="return-value---path"></a>戻り値 - path

## <a name="method-new"></a>メソッド new

MapiFileDesc クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

