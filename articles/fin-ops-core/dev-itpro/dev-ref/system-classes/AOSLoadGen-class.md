---
title: AOSLoadGen クラス
description: このトピックでは、AOSLoadGen クラスについて説明します。
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
ms.openlocfilehash: b3043abc007e647c58c8cb1d5e92e236c54caf67
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502751"
---
# <a name="class-aosloadgen"></a>クラス AOSLoadGen

[!include [banner](../../includes/banner.md)]

```xpp
class AOSLoadGen extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                  |
|------------------------------------------------------------|----------------------------------------------|
| public boolean spawnClass(ClassId classId, str parm)       |                                              |
| public boolean spawnJob(UtilElementName jobName, str parm) |                                              |
| public void new(\[UserId user\], \[ClassId infoClass\])    | AOSLoadGen クラスのインスタンスを作成します。 |

## <a name="method-spawnclass"></a>メソッド spawnClass

```xpp
public boolean spawnClass(ClassId classId, str parm)
```

### <a name="parameters---spawnclass"></a>パラメーター - spawnClass

classId  

<!-- -->

parm  

### <a name="return-value---spawnclass"></a>戻り値 - spawnClass

## <a name="method-spawnjob"></a>メソッド spawnJob

```xpp
public boolean spawnJob(UtilElementName jobName, str parm)
```

### <a name="parameters---spawnjob"></a>パラメーター - spawnJob

jobName  

<!-- -->

parm  

### <a name="return-value---spawnjob"></a>戻り値 - spawnJob

## <a name="method-new"></a>メソッド new

AOSLoadGen クラスのインスタンスを作成します。

```xpp
public void new([UserId user], [ClassId infoClass])
```

### <a name="parameters---new"></a>パラメーター - new

ユーザー  
AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。 既定値は情報です。

<!-- -->

infoClass  
AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。 既定値は情報です。

### <a name="remarks---new"></a>備考 - new

新しいメソッドへの入力を制御することは、セキュリティ上のリスクとなる可能性があります。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。
