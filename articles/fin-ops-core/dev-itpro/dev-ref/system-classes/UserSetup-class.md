---
title: UserSetup クラス
description: このトピックでは、UserSetup クラスについて説明します。
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
ms.openlocfilehash: ebbd3ff0570dc6af83a805b7a5b81e5ba33b34d2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502781"
---
# <a name="class-usersetup"></a>クラス UserSetup

[!include [banner](../../includes/banner.md)]

```xpp
class UserSetup extends TreeNode
```

UserSetup クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。

## <a name="remarks"></a>備考

このクラスは、主に SysUserSetup フォームで使用されます。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                  | 説明 |
|-----------------------------------------|-------------|
| public boolean xRef(\[boolean enable\]) |             |
| public void setUserSetup(Common cursor) |             |
| public void setDefaults(Common cursor)  |             |

## <a name="method-xref"></a>メソッド xRef

```xpp
public boolean xRef([boolean enable])
```

### <a name="parameters---xref"></a>パラメーター - xRef

enable  

### <a name="return-value---xref"></a>戻り値 - xRef

## <a name="method-setusersetup"></a>メソッド setUserSetup

```xpp
public void setUserSetup(Common cursor)
```

### <a name="parameters---setusersetup"></a>パラメーター - setUserSetup

cursor  

## <a name="method-setdefaults"></a>メソッド setDefaults

```xpp
public void setDefaults(Common cursor)
```

### <a name="parameters---setdefaults"></a>パラメーター - setDefaults

cursor  

