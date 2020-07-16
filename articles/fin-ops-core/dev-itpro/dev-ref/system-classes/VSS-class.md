---
title: VSS クラス
description: このトピックでは、VSS クラスについて説明します。
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
ms.openlocfilehash: a174fc7f84401839952f697e9fb30218cf5086f4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502778"
---
# <a name="class-vss"></a>クラス VSS

[!include [banner](../../includes/banner.md)]

```xpp
class VSS extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                        | 説明                               |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| public boolean connect()                                                                                      |                                           |
| public boolean connected()                                                                                    |                                           |
| public boolean disconnect()                                                                                   |                                           |
| public container getCheckedoutFiles()                                                                         |                                           |
| public container getConnectionInfo()                                                                          |                                           |
| public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])      |                                           |
| public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)                |                                           |
| public VSSItem newSubProject(str name, str localPath)                                                         |                                           |
| public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\]) |                                           |
| public void new()                                                                                             | VSS クラスのインスタンスを初期化します。 |

## <a name="method-connect"></a>メソッド connect

```xpp
public boolean connect()
```

### <a name="return-value---connect"></a>戻り値 - connect

## <a name="method-connected"></a>メソッド connected

```xpp
public boolean connected()
```

### <a name="return-value---connected"></a>戻り値 - connected

## <a name="method-disconnect"></a>メソッド disconnect

```xpp
public boolean disconnect()
```

### <a name="return-value---disconnect"></a>戻り値 - disconnect

## <a name="method-getcheckedoutfiles"></a>メソッド getCheckedoutFiles

```xpp
public container getCheckedoutFiles()
```

### <a name="return-value---getcheckedoutfiles"></a>戻り値 - getCheckedoutFiles

## <a name="method-getconnectioninfo"></a>メソッド getConnectionInfo

```xpp
public container getConnectionInfo()
```

### <a name="return-value---getconnectioninfo"></a>戻り値 - getConnectionInfo

## <a name="method-getvssitem"></a>メソッド getVSSItem

```xpp
public VSSItem getVSSItem(str vssItemPath, str localFilePath, [boolean completePath], [int version])
```

### <a name="parameters---getvssitem"></a>パラメーター - getVSSItem

vssItemPath  

<!-- -->

localFilePath  

<!-- -->

completePath  

<!-- -->

のバージョン  

### <a name="return-value---getvssitem"></a>戻り値 - getVSSItem

## <a name="method-init"></a>メソッド init

```xpp
public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)
```

### <a name="parameters---init"></a>パラメーター - init

vssIni  

<!-- -->

vssPrjRoot  

<!-- -->

vssWorkingFolder  

<!-- -->

vssUser  

<!-- -->

vssPwd  

### <a name="return-value---init"></a>戻り値 - init

## <a name="method-newsubproject"></a>メソッド newSubProject

```xpp
public VSSItem newSubProject(str name, str localPath)
```

### <a name="parameters---newsubproject"></a>パラメーター - newSubProject

名前  

<!-- -->

localPath  

### <a name="return-value---newsubproject"></a>戻り値 - newSubProject

## <a name="method-synchronizeprojects"></a>メソッド synchronizeProjects

```xpp
public Map synchronizeProjects([Set projects], [boolean force], [boolean delLocalFiles], [str label])
```

### <a name="parameters---synchronizeprojects"></a>パラメーター - synchronizeProjects

プロジェクト  

<!-- -->

force  

<!-- -->

delLocalFiles  

<!-- -->

ラベル  

### <a name="return-value---synchronizeprojects"></a>戻り値 - synchronizeProjects

## <a name="method-new"></a>メソッド new

VSS クラスのインスタンスを初期化します。

```xpp
public void new()
```

