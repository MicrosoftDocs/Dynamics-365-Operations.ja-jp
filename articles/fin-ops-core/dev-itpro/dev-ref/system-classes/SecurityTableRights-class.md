---
title: SecurityTableRights クラス
description: このトピックでは、SecurityTableRights クラスについて説明します。
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
ms.openlocfilehash: 319dd41615c3609001c38295dd3574815450ac65
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502809"
---
# <a name="class-securitytablerights"></a>クラス SecurityTableRights

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityTableRights extends Object
```

SecurityTableRights クラスには、テーブル セキュリティ権限に関する情報が含まれます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                   | 説明                                               |
|----------------------------------------------------------|-----------------------------------------------------------|
| public AccessRight fieldAccessRight(FieldName fieldName) | テーブルのフィールドのアクセス権を取得します。        |
| public AccessRight tableAccessRight()                    | テーブルのアクセス権を取得します。                     |
| private void new()                                       | SecurityTableRights クラスのインスタンスを初期化します。 |

## <a name="method-fieldaccessright"></a>メソッド fieldAccessRight

テーブルのフィールドのアクセス権を取得します。

```xpp
public AccessRight fieldAccessRight(FieldName fieldName)
```

### <a name="parameters---fieldaccessright"></a>パラメーター - fieldAccessRight

fieldName  

### <a name="return-value---fieldaccessright"></a>戻り値 - fieldAccessRight

フィールドの AccesRight インスタンス。

## <a name="method-tableaccessright"></a>メソッド tableAccessRight

テーブルのアクセス権を取得します。

```xpp
public AccessRight tableAccessRight()
```

### <a name="return-value---tableaccessright"></a>戻り値 - tableAccessRight

テーブルの AccesRight インスタンス。

## <a name="method-new"></a>メソッド new

SecurityTableRights クラスのインスタンスを初期化します。

```xpp
private void new()
```

