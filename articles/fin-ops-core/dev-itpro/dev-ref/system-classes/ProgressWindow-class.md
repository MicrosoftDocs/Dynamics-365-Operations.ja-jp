---
title: ProgressWindow クラス
description: このトピックでは、ProgressWindow クラスについて説明します。
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
ms.openlocfilehash: 163866523c89da79004156066b290eafa523eb13
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502874"
---
# <a name="class-progresswindow"></a>クラス ProgressWindow

[!include [banner](../../includes/banner.md)]

```xpp
class ProgressWindow extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                             |
|-------------------------------------------------------------|---------------------------------------------------------|
| public int addProgressControl(\[int progressControlCount\]) |                                                         |
| public void ProgressBarVisible(int index, int visible)      |                                                         |
| public void ProgressValue(int index, int progressValue)     |                                                         |
| public void ControlMinMax(int index, int min, int max)      |                                                         |
| public void ProgressTextVisible(int index, int visible)     |                                                         |
| public void Animation(str animation)                        |                                                         |
| public void ControlText(int index, str text)                |                                                         |
| public void FormCaption(str text)                           |                                                         |
| public void ControlTime(str text)                           |                                                         |
| public void finalize()                                      |                                                         |
| public void new()                                           | ProgressWindow クラスの新しいインスタンスを初期化します。 |

## <a name="method-addprogresscontrol"></a>メソッド addProgressControl

```xpp
public int addProgressControl([int progressControlCount])
```

### <a name="parameters---addprogresscontrol"></a>パラメーター - addProgressControl

progressControlCount  

### <a name="return-value---addprogresscontrol"></a>戻り値 - addProgressControl

## <a name="method-progressbarvisible"></a>メソッド ProgressBarVisible

```xpp
public void ProgressBarVisible(int index, int visible)
```

### <a name="parameters---progressbarvisible"></a>パラメーター - ProgressBarVisible

指数  

<!-- -->

表示  

## <a name="method-progressvalue"></a>メソッド ProgressValue

```xpp
public void ProgressValue(int index, int progressValue)
```

### <a name="parameters---progressvalue"></a>パラメーター - ProgressValue

指数  

<!-- -->

progressValue  

## <a name="method-controlminmax"></a>メソッド ControlMinMax

```xpp
public void ControlMinMax(int index, int min, int max)
```

### <a name="parameters---controlminmax"></a>パラメーター - ControlMinMax

指数  

<!-- -->

最小  

<!-- -->

最大  

## <a name="method-progresstextvisible"></a>メソッド ProgressTextVisible

```xpp
public void ProgressTextVisible(int index, int visible)
```

### <a name="parameters---progresstextvisible"></a>パラメーター - ProgressTextVisible

指数  

<!-- -->

表示  

## <a name="method-animation"></a>メソッド アニメーション

```xpp
public void Animation(str animation)
```

### <a name="parameters---animation"></a>パラメーター - Animation

animation  

## <a name="method-controltext"></a>メソッド ControlText

```xpp
public void ControlText(int index, str text)
```

### <a name="parameters---controltext"></a>パラメーター - ControlText

指数  

<!-- -->

テキスト  

## <a name="method-formcaption"></a>メソッド FormCaption

```xpp
public void FormCaption(str text)
```

### <a name="parameters---formcaption"></a>パラメーター - FormCaption

テキスト  

## <a name="method-controltime"></a>メソッド ControlTime

```xpp
public void ControlTime(str text)
```

### <a name="parameters---controltime"></a>パラメーター - ControlTime

テキスト  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

ProgressWindow クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

