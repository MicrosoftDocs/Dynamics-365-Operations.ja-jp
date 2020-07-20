---
title: CryptoAPI クラス
description: このトピックでは、CryptoAPI クラスについて説明します。
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
ms.openlocfilehash: c8e96c4690752da8c32d077f87f7b181813000e3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502702"
---
# <a name="class-cryptoapi"></a>クラス CryptoAPI

[!include [banner](../../includes/banner.md)]

```xpp
class CryptoAPI extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                   | 説明                                     |
|------------------------------------------|-------------------------------------------------|
| public container decrypt(container blob) |                                                 |
| public container encrypt(container blob) |                                                 |
| public container getKey()                |                                                 |
| public Int64 salt()                      |                                                 |
| public void new(Int64 salt)              | Object クラスの新しいインスタンスを初期化します。 |
| ::public static void resetKey()          |                                                 |

## <a name="method-decrypt"></a>メソッド decrypt

```xpp
public container decrypt(container blob)
```

### <a name="parameters---decrypt"></a>パラメーター - decrypt

blob  

### <a name="return-value---decrypt"></a>戻り値 - decrypt

## <a name="method-encrypt"></a>メソッド encrypt

```xpp
public container encrypt(container blob)
```

### <a name="parameters---encrypt"></a>パラメーター - encrypt

blob  

### <a name="return-value---encrypt"></a>戻り値 - encrypt

## <a name="method-getkey"></a>メソッド getKey

```xpp
public container getKey()
```

### <a name="return-value---getkey"></a>戻り値 - getKey

## <a name="method-salt"></a>メソッド salt

```xpp
public Int64 salt()
```

### <a name="return-value---salt"></a>戻り値 - salt

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(Int64 salt)
```

### <a name="parameters---new"></a>パラメーター - new

salt  

## <a name="method-resetkey"></a>メソッド resetKey

```xpp
public static void resetKey()
```

