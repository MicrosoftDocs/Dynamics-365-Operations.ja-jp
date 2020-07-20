---
title: xVersionControl クラス
description: このトピックでは、xVersionControl クラスについて説明します。
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
ms.openlocfilehash: f9ea8c0a2e9c1343bbdc32d074319ba694948457
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502757"
---
# <a name="class-xversioncontrol"></a>クラス xVersionControl

[!include [banner](../../includes/banner.md)]

```xpp
class xVersionControl extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                            | 説明                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| public boolean allowCreate(TreeNode node)                                                                                                                         |                                                          |
| public boolean allowDelete(TreeNode node)                                                                                                                         |                                                          |
| public boolean allowEdit(TreeNode node)                                                                                                                           |                                                          |
| public boolean allowRename(TreeNode node)                                                                                                                         |                                                          |
| public boolean checkOut(TreeNode node)                                                                                                                            |                                                          |
| public boolean create(TreeNode node)                                                                                                                              |                                                          |
| public boolean delete(TreeNode node)                                                                                                                              |                                                          |
| public int getAvailableId(UtilElementType objectType, UtilEntryLevel layer, \[int parentId\], \[IdAllocationSchema idAllocationSchema\], \[boolean inheritance\]) |                                                          |
| public int getAvailableLabelId(str labelFile, str language, \[IdAllocationSchema idAllocationSchema\])                                                            |                                                          |
| public boolean ideIntegration()                                                                                                                                   |                                                          |
| public boolean moveToModel(TreeNode node, int modelId)                                                                                                            |                                                          |
| public boolean rename(TreeNode node, str newname)                                                                                                                 |                                                          |
| public boolean undoCheckOut(TreeNode node, \[boolean showDialog\])                                                                                                |                                                          |
| public Set unwantedObjectTypes()                                                                                                                                  |                                                          |
| public void colorAOT()                                                                                                                                            |                                                          |
| public void save(TreeNode node)                                                                                                                                   |                                                          |
| public void showHistory(TreeNode node)                                                                                                                            |                                                          |
| public void updateCheckedOutList(Set checkedOutObjects)                                                                                                           |                                                          |
| public void getLatestVersion(\[TreeNode node\], \[boolean delLocalFiles\])                                                                                        |                                                          |
| public void checkIn(TreeNode node)                                                                                                                                |                                                          |
| public void new()                                                                                                                                                 | xVersionControl クラスの新しいインスタンスを初期化します。 |
| public void reload()                                                                                                                                              |                                                          |
| public void getLabelVersion(\[TreeNode node\], \[str label\])                                                                                                     |                                                          |

## <a name="method-allowcreate"></a>メソッド allowCreate

```xpp
public boolean allowCreate(TreeNode node)
```

### <a name="parameters---allowcreate"></a>パラメーター - allowCreate

node  

### <a name="return-value---allowcreate"></a>戻り値 - allowCreate

## <a name="method-allowdelete"></a>メソッド allowDelete

```xpp
public boolean allowDelete(TreeNode node)
```

### <a name="parameters---allowdelete"></a>パラメーター - allowDelete

node  

### <a name="return-value---allowdelete"></a>戻り値 - allowDelete

## <a name="method-allowedit"></a>メソッド allowEdit

```xpp
public boolean allowEdit(TreeNode node)
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

node  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

## <a name="method-allowrename"></a>メソッド allowRename

```xpp
public boolean allowRename(TreeNode node)
```

### <a name="parameters---allowrename"></a>パラメーター - allowRename

node  

### <a name="return-value---allowrename"></a>戻り値 - allowRename

## <a name="method-checkout"></a>メソッド checkOut

```xpp
public boolean checkOut(TreeNode node)
```

### <a name="parameters---checkout"></a>パラメーター - checkOut

node  

### <a name="return-value---checkout"></a>戻り値 - checkOut

## <a name="method-create"></a>メソッド create

```xpp
public boolean create(TreeNode node)
```

### <a name="parameters---create"></a>パラメーター - create

node  

### <a name="return-value---create"></a>戻り値 - create

## <a name="method-delete"></a>メソッド delete

```xpp
public boolean delete(TreeNode node)
```

### <a name="parameters---delete"></a>パラメーター - delete

node  

### <a name="return-value---delete"></a>戻り値 - delete

## <a name="method-getavailableid"></a>メソッド getAvailableId

```xpp
public int getAvailableId(UtilElementType objectType, UtilEntryLevel layer, [int parentId], [IdAllocationSchema idAllocationSchema], [boolean inheritance])
```

### <a name="parameters---getavailableid"></a>パラメーター - getAvailableId

objectType  

<!-- -->

 レイヤー  

<!-- -->

parentId  

<!-- -->

idAllocationSchema  

<!-- -->

inheritance  

### <a name="return-value---getavailableid"></a>戻り値 - getAvailableId

## <a name="method-getavailablelabelid"></a>メソッド getAvailableLabelId

```xpp
public int getAvailableLabelId(str labelFile, str language, [IdAllocationSchema idAllocationSchema])
```

### <a name="parameters---getavailablelabelid"></a>パラメーター - getAvailableLabelId

labelFile  

<!-- -->

言語  

<!-- -->

idAllocationSchema  

### <a name="return-value---getavailablelabelid"></a>戻り値 - getAvailableLabelId

## <a name="method-ideintegration"></a>メソッド ideIntegration

```xpp
public boolean ideIntegration()
```

### <a name="return-value---ideintegration"></a>戻り値 - ideIntegration

## <a name="method-movetomodel"></a>メソッド moveToModel

```xpp
public boolean moveToModel(TreeNode node, int modelId)
```

### <a name="parameters---movetomodel"></a>パラメーター - moveToModel

node  

<!-- -->

modelId  

### <a name="return-value---movetomodel"></a>戻り値 - moveToModel

## <a name="method-rename"></a>メソッド rename

```xpp
public boolean rename(TreeNode node, str newname)
```

### <a name="parameters---rename"></a>パラメーター - rename

node  

<!-- -->

newname  

### <a name="return-value---rename"></a>戻り値 - rename

## <a name="method-undocheckout"></a>メソッド undoCheckOut

```xpp
public boolean undoCheckOut(TreeNode node, [boolean showDialog])
```

### <a name="parameters---undocheckout"></a>パラメーター - undoCheckOut

node  

<!-- -->

showDialog  

### <a name="return-value---undocheckout"></a>戻り値 - undoCheckOut

## <a name="method-unwantedobjecttypes"></a>メソッド unwantedObjectTypes

```xpp
public Set unwantedObjectTypes()
```

### <a name="return-value---unwantedobjecttypes"></a>戻り値 - unwantedObjectTypes

## <a name="method-coloraot"></a>メソッド colorAOT

```xpp
public void colorAOT()
```

## <a name="method-save"></a>メソッド save

```xpp
public void save(TreeNode node)
```

### <a name="parameters---save"></a>パラメーター - save

node  

## <a name="method-showhistory"></a>メソッド showHistory

```xpp
public void showHistory(TreeNode node)
```

### <a name="parameters---showhistory"></a>パラメーター - showHistory

node  

## <a name="method-updatecheckedoutlist"></a>メソッド updateCheckedOutList

```xpp
public void updateCheckedOutList(Set checkedOutObjects)
```

### <a name="parameters---updatecheckedoutlist"></a>パラメーター - updateCheckedOutList

checkedOutObjects  

## <a name="method-getlatestversion"></a>メソッド getLatestVersion

```xpp
public void getLatestVersion([TreeNode node], [boolean delLocalFiles])
```

### <a name="parameters---getlatestversion"></a>パラメーター - getLatestVersion

node  

<!-- -->

delLocalFiles  

## <a name="method-checkin"></a>メソッド checkIn

```xpp
public void checkIn(TreeNode node)
```

### <a name="parameters---checkin"></a>パラメーター - checkIn

node  

## <a name="method-new"></a>メソッド new

xVersionControl クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-reload"></a>メソッド reload

```xpp
public void reload()
```

## <a name="method-getlabelversion"></a>メソッド getLabelVersion

```xpp
public void getLabelVersion([TreeNode node], [str label])
```

### <a name="parameters---getlabelversion"></a>パラメーター - getLabelVersion

node  

<!-- -->

ラベル  



