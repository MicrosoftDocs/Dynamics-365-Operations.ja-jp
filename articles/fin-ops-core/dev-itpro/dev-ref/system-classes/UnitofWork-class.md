---
title: UnitofWork クラス
description: このトピックでは、UnitofWork クラスについて説明します。
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
ms.openlocfilehash: 39d2c1f070dac147a8c96bfa2d4945df9bc2b409
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502785"
---
# <a name="class-unitofwork"></a>クラス UnitofWork

[!include [banner](../../includes/banner.md)]


```xpp
class UnitofWork extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                       | 説明                                         |
|--------------------------------------------------------------|-----------------------------------------------------|
| public boolean getByKey(Common record)                       |                                                     |
| public void updateonSaveChanges(Common record)               |                                                     |
| public void saveChanges(\[UserConnection user\_connection\]) |                                                     |
| public void deleteonSaveChanges(Common record)               |                                                     |
| public void insertonSaveChanges(Common record)               |                                                     |
| public void finalize()                                       |                                                     |
| public void new()                                            | UnitofWork クラスの新しいインスタンスを初期化します。 |
| public void clear()                                          |                                                     |

## <a name="method-getbykey"></a>メソッド getByKey

```xpp
public boolean getByKey(Common record)
```

### <a name="parameters---getbykey"></a>パラメーター - getByKey

記録  

### <a name="return-value---getbykey"></a>戻り値 - getByKey

## <a name="method-updateonsavechanges"></a>メソッド updateonSaveChanges

```xpp
public void updateonSaveChanges(Common record)
```

### <a name="parameters---updateonsavechanges"></a>パラメーター - updateonSaveChanges

記録  

## <a name="method-savechanges"></a>メソッド saveChanges

```xpp
public void saveChanges([UserConnection user_connection])
```

### <a name="parameters---savechanges"></a>パラメータ－ - saveChanges

user\_connection  

## <a name="method-deleteonsavechanges"></a>メソッド deleteonSaveChanges

```xpp
public void deleteonSaveChanges(Common record)
```

### <a name="parameters---deleteonsavechanges"></a>パラメーター - deleteonSaveChanges

記録  

## <a name="method-insertonsavechanges"></a>メソッド insertonSaveChanges

```xpp
public void insertonSaveChanges(Common record)
```

### <a name="parameters---insertonsavechanges"></a>パラメーター - insertonSaveChanges

記録  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

UnitofWork クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-clear"></a>メソッド clear

```xpp
public void clear()
```

