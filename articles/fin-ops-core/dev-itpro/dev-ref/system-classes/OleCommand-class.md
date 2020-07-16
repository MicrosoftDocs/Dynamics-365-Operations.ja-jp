---
title: OleCommand クラス
description: このトピックでは、OleCommand クラスについて説明します。
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
ms.openlocfilehash: 3b840512bd497132a1022658f45a72c0d61356ca
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502561"
---
# <a name="class-olecommand"></a>クラス OleCommand

[!include [banner](../../includes/banner.md)]

```xpp
class OleCommand extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                              | 説明                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm) |                                                 |
| public void finalize()                                                              |                                                 |
| public void new(ComInterface comObject)                                             | Object クラスの新しいインスタンスを初期化します。 |

## <a name="method-exec"></a>メソッド exec

```xpp
public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)
```

### <a name="parameters---exec"></a>パラメーター - exec

cmdGroup  

<!-- -->

cmdId  

<!-- -->

cmdExecOption  

<!-- -->

parm  

### <a name="return-value---exec"></a>戻り値 - exec

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(ComInterface comObject)
```

### <a name="parameters---new"></a>パラメーター - new

comObject  

