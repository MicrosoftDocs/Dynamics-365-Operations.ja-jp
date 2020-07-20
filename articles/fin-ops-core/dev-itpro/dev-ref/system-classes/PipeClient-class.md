---
title: PipeClient クラス
description: このトピックでは、PipeClient クラスについて説明します。
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
ms.openlocfilehash: bb028120e2eb0272185841fda4b819edfb3bce5f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502533"
---
# <a name="class-pipeclient"></a>クラス PipeClient

[!include [banner](../../includes/banner.md)]

```xpp
class PipeClient extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                              | 説明                                         |
|---------------------------------------------------------------------|-----------------------------------------------------|
| public boolean blockingMode(\[boolean block\])                      |                                                     |
| public int errorCode()                                              |                                                     |
| public str read()                                                   |                                                     |
| public boolean write(str buffer)                                    |                                                     |
| public void new(str servername, str pipename, \[boolean blocking\]) | PipeClient クラスの新しいインスタンスを初期化します。 |

## <a name="method-blockingmode"></a>メソッド blockingMode

```xpp
public boolean blockingMode([boolean block])
```

### <a name="parameters---blockingmode"></a>パラメーター - blockingMode

block  

### <a name="return-value---blockingmode"></a>戻り値 - blockingMode

## <a name="method-errorcode"></a>メソッド errorCode

```xpp
public int errorCode()
```

### <a name="return-value---errorcode"></a>戻り値 - errorCode

## <a name="method-read"></a>メソッド read

```xpp
public str read()
```

### <a name="return-value---read"></a>戻り値 - read

## <a name="method-write"></a>メソッド write

```xpp
public boolean write(str buffer)
```

### <a name="parameters---write"></a>パラメーター - write

バッファ  

### <a name="return-value---write"></a>戻り値 - write

## <a name="method-new"></a>メソッド new

PipeClient クラスの新しいインスタンスを初期化します。

```xpp
public void new(str servername, str pipename, [boolean blocking])
```

### <a name="parameters---new"></a>パラメーター - new

servername  

<!-- -->

pipename  

<!-- -->

ブロック  

