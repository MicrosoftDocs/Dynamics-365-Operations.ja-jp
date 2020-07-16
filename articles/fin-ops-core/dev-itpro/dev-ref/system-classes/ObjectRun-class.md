---
title: ObjectRun クラス
description: このトピックでは、ObjectRun クラスについて説明します。
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
ms.openlocfilehash: 7064d776ce636c4412c55f5e7a3aa0a98a928c93
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502565"
---
# <a name="class-objectrun"></a>クラス ObjectRun

[!include [banner](../../includes/banner.md)]

```xpp
class ObjectRun extends Object
```

FormRun クラスおよび ReportRun クラスの基本クラスとして使用されます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                      | 説明                                                                                                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public xArgs args()         | オブジェクトが作成された引数を返します。                                                                                                             |
| public boolean isDetached() | このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。                                                                                      |
| public void attach()        | メソッドの呼び出しが取り消されます。 これは、ObjectRun.detach メソッドの呼び出しの逆です。 呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。 |
| public void detach()        | フォーカスをウィンドウ間で切り替えられるように許可します。                                                                                                                            |

## <a name="method-args"></a>メソッド args

オブジェクトが作成された引数を返します。

```xpp
public xArgs args()
```

### <a name="return-value---args"></a>戻り値 - args

オブジェクトの引数を含む Args クラス オブジェクトです。

## <a name="method-isdetached"></a>メソッド isDetached

このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。

```xpp
public boolean isDetached()
```

### <a name="return-value---isdetached"></a>戻り値 - isDetached

デタッチが呼び出された場合は true。それ以外の場合は、false。

## <a name="method-attach"></a>メソッド attach

メソッドの呼び出しが取り消されます。 これは、ObjectRun.detach メソッドの呼び出しの逆です。 呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。

```xpp
public void attach()
```

## <a name="method-detach"></a>メソッド detach

フォーカスをウィンドウ間で切り替えられるように許可します。

```xpp
public void detach()
```

### <a name="remarks---detach"></a>備考 - detach

たとえば、新しいフォームの実行方法を呼び出すことにより、新しいフォームが既存のフォームから作成されます。 実行メソッドを呼び出すと、フォーカスが新しいフォームに変更されます。 解除メソッドを呼び出すと、ユーザーは 2 番目のフォームを閉じることなく最初のフォームに戻ることができます。 ObjectRun.attach Method メソッドの呼び出しは、解除メソッドの影響を取り消します。

