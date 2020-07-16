---
title: FormObjectSetPagingParamsChangedEvtArgs クラス
description: このトピックでは、FormObjectSetPagingParamsChangedEvtArgs クラスについて説明します。
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
ms.openlocfilehash: 0a71f0871580cdbb2ed5dff255e3163638a5fb6c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502918"
---
# <a name="class-formobjectsetpagingparamschangedevtargs"></a>クラス FormObjectSetPagingParamsChangedEvtArgs

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSetPagingParamsChangedEvtArgs extends ManagedEventArgs
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                  | 説明                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| public int pageSize()                                                   |                                                           |
| public boolean pagingEnabled()                                          |                                                           |
| public int startRowIndex()                                              |                                                           |
| public void finalize()                                                  |                                                           |
| public void new(boolean pagingEnabled, int startRowIndex, int pageSize) | ManagedEventArgs クラスの新しいインスタンスを初期化します。 |

## <a name="method-pagesize"></a>メソッド pageSize

```xpp
public int pageSize()
```

### <a name="return-value---pagesize"></a>戻り値 - pageSize

## <a name="method-pagingenabled"></a>メソッド pagingEnabled

```xpp
public boolean pagingEnabled()
```

### <a name="return-value---pagingenabled"></a>戻り値 - pagingEnabled

## <a name="method-startrowindex"></a>メソッド startRowIndex

```xpp
public int startRowIndex()
```

### <a name="return-value---startrowindex"></a>戻り値 - startRowIndex

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

ManagedEventArgs クラスの新しいインスタンスを初期化します。

```xpp
public void new(boolean pagingEnabled, int startRowIndex, int pageSize)
```

### <a name="parameters---new"></a>パラメーター - new

pagingEnabled  

<!-- -->

startRowIndex  

<!-- -->

pageSize  

