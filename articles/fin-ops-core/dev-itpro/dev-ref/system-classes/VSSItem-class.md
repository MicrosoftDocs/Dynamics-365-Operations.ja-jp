---
title: VSSItem クラス
description: このトピックでは、VSSItem クラスについて説明します。
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
ms.openlocfilehash: bc0baed9c50a18e106990fd6467d4caa4346db91
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502777"
---
# <a name="class-vssitem"></a>クラス VSSItem

[!include [banner](../../includes/banner.md)]

```xpp
class VSSItem extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                               | 説明                                      |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| public boolean add(\[boolean keepCheckedout\], \[str comment\])                      |                                                  |
| public boolean checkin(\[str comment\])                                              |                                                  |
| public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\]) |                                                  |
| public boolean delete()                                                              |                                                  |
| public boolean destroy()                                                             |                                                  |
| public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\]) |                                                  |
| public str getActionText()                                                           |                                                  |
| public container getCheckedOutTo()                                                   |                                                  |
| public int getCheckoutVersion()                                                      |                                                  |
| public container getHistory()                                                        |                                                  |
| public ComInterface getIUnknown()                                                    |                                                  |
| public int getVersionNo()                                                            |                                                  |
| public str getVSSPath()                                                              |                                                  |
| public boolean isCheckedOut()                                                        |                                                  |
| public boolean isRenamed()                                                           |                                                  |
| public str name(str newName)                                                         |                                                  |
| public boolean rename(str newName)                                                   |                                                  |
| public boolean undoCheckout()                                                        |                                                  |
| private void new()                                                                   | VSSItem クラスの新しいインスタンスを初期化します。 |

## <a name="method-add"></a>メソッド add

```xpp
public boolean add([boolean keepCheckedout], [str comment])
```

### <a name="parameters---add"></a>パラメーター - add

keepCheckedout  

<!-- -->

comment  

### <a name="return-value---add"></a>戻り値 - add

## <a name="method-checkin"></a>メソッド checkin

```xpp
public boolean checkin([str comment])
```

### <a name="parameters---checkin"></a>パラメーター - checkin

comment  

### <a name="return-value---checkin"></a>戻り値 - checkin

## <a name="method-checkout"></a>メソッド checkout

```xpp
public boolean checkout([boolean allowMultipleCheckout], [boolean replaceLocal])
```

### <a name="parameters---checkout"></a>パラメーター - checkout

allowMultipleCheckout  

<!-- -->

replaceLocal  

### <a name="return-value---checkout"></a>戻り値 - checkout

## <a name="method-delete"></a>メソッド delete

```xpp
public boolean delete()
```

### <a name="return-value---delete"></a>戻り値 - delete

## <a name="method-destroy"></a>メソッド destroy

```xpp
public boolean destroy()
```

### <a name="return-value---destroy"></a>戻り値 - destroy

## <a name="method-get"></a>メソッド get

```xpp
public Map get([boolean force], [int version], [str label], [str localFile])
```

### <a name="parameters---get"></a>パラメーター - get

force  

<!-- -->

のバージョン  

<!-- -->

ラベル  

<!-- -->

localFile  

### <a name="return-value---get"></a>戻り値 - get

## <a name="method-getactiontext"></a>メソッド getActionText

```xpp
public str getActionText()
```

### <a name="return-value---getactiontext"></a>戻り値 - getActionText

## <a name="method-getcheckedoutto"></a>メソッド getCheckedOutTo

```xpp
public container getCheckedOutTo()
```

### <a name="return-value---getcheckedoutto"></a>戻り値 - getCheckedOutTo

## <a name="method-getcheckoutversion"></a>メソッド getCheckoutVersion

```xpp
public int getCheckoutVersion()
```

### <a name="return-value---getcheckoutversion"></a>戻り値 - getCheckoutVersion

## <a name="method-gethistory"></a>メソッド getHistory

```xpp
public container getHistory()
```

### <a name="return-value---gethistory"></a>戻り値 - getHistory

## <a name="method-getiunknown"></a>メソッド getIUnknown

```xpp
public ComInterface getIUnknown()
```

### <a name="return-value---getiunknown"></a>戻り値 - getIUnknown

## <a name="method-getversionno"></a>メソッド getVersionNo

```xpp
public int getVersionNo()
```

### <a name="return-value---getversionno"></a>戻り値 - getVersionNo

## <a name="method-getvsspath"></a>メソッド getVSSPath

```xpp
public str getVSSPath()
```

### <a name="return-value---getvsspath"></a>戻り値 - getVSSPath

## <a name="method-ischeckedout"></a>メソッド isCheckedOut

```xpp
public boolean isCheckedOut()
```

### <a name="return-value---ischeckedout"></a>戻り値 - isCheckedOut

## <a name="method-isrenamed"></a>メソッド isRenamed

```xpp
public boolean isRenamed()
```

### <a name="return-value---isrenamed"></a>戻り値 - isRenamed

## <a name="method-name"></a>メソッド名

```xpp
public str name(str newName)
```

### <a name="parameters---name"></a>パラメーター - name

newName  

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-rename"></a>メソッド rename

```xpp
public boolean rename(str newName)
```

### <a name="parameters---rename"></a>パラメーター - rename

newName  

### <a name="return-value---rename"></a>戻り値 - rename

## <a name="method-undocheckout"></a>メソッド undoCheckout

```xpp
public boolean undoCheckout()
```

### <a name="return-value---undocheckout"></a>戻り値 - undoCheckout

## <a name="method-new"></a>メソッド new

VSSItem クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```


