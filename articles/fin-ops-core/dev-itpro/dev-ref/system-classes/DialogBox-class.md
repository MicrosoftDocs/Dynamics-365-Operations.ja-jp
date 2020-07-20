---
title: DialogBox クラス
description: このトピックでは、DialogBox クラスについて説明します。
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
ms.openlocfilehash: 44349783f326770f2a3b7e086b753c8246bf7cb5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502728"
---
# <a name="class-dialogbox"></a>クラス ダイアログ ボックス

[!include [banner](../../includes/banner.md)]

```xpp
class DialogBox extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                               | 説明                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public DialogButton retval()                                                                         |                                                 |
| public void new(DialogBoxType type, str text, str title, str bottomtext, DialogButton defaultButton) | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                                               |                                                 |

## <a name="method-retval"></a>メソッド retval

```xpp
public DialogButton retval()
```

### <a name="return-value---retval"></a>戻り値 - retval

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(DialogBoxType type, str text, str title, str bottomtext, DialogButton defaultButton)
```

### <a name="parameters---new"></a>パラメーター - new

タイプ  

<!-- -->

テキスト  

<!-- -->

タイトル  

<!-- -->

bottomtext  

<!-- -->

defaultButton  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

