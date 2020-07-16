---
title: HeapCheck クラス
description: このトピックでは、HeapCheck クラスについて説明します。
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
ms.openlocfilehash: a5afbaf81b574959b19e4f48a527fe5b75d0be53
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502611"
---
# <a name="class-heapcheck"></a>クラス HeapCheck

[!include [banner](../../includes/banner.md)]


```xpp
class HeapCheck extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                      | 説明                                     |
|---------------------------------------------------------------------------------------------|-------------------------------------------------|
| public int accessCnt()                                                                      |                                                 |
| public int addRefCnt()                                                                      |                                                 |
| public Int64 blocksAllocated(\[int pool\])                                                  |                                                 |
| public int breakCount(\[int count\])                                                        |                                                 |
| public Int64 bytesAllocated(\[int pool\])                                                   |                                                 |
| public Int64 ceiling(int pool, \[int ceiling\])                                             |                                                 |
| public int context(\[int context\])                                                         |                                                 |
| public int count(\[int count\])                                                             |                                                 |
| public int countObjects(int classId)                                                        |                                                 |
| public container createAContainer()                                                         |                                                 |
| public int csCallCnt()                                                                      |                                                 |
| public int csSweepCnt()                                                                     |                                                 |
| public container dataByContext(\[int poolNo\], \[int context\])                             |                                                 |
| public int dumpCursors()                                                                    |                                                 |
| public int dumpObjects()                                                                    |                                                 |
| public int filename(\[str filename\])                                                       |                                                 |
| public int fixedBlockSize(int pool, \[int blockSize\])                                      |                                                 |
| public int floor(int pool, \[int floor\])                                                   |                                                 |
| public int freeRefCnt()                                                                     |                                                 |
| public int getRuntimeBugcheckFlags()                                                        |                                                 |
| public Common getUnfreedCursor()                                                            |                                                 |
| public Common getUnfreedObject()                                                            |                                                 |
| public boolean include(int objectNo, \[boolean include\])                                   |                                                 |
| public boolean moreUnfreedCursors()                                                         |                                                 |
| public boolean moreUnfreedObjects()                                                         |                                                 |
| public int objectContext(int objNo, \[int context\])                                        |                                                 |
| public int pageSize(int pool, \[int pageSize\])                                             |                                                 |
| public int poolCount()                                                                      |                                                 |
| public str poolName(int poolNo)                                                             |                                                 |
| public int smallBlockSize(int pool, \[int blockSize\])                                      |                                                 |
| public int sweepCnt()                                                                       |                                                 |
| public int testBlocks(\[int arg1\])                                                         |                                                 |
| public str unfreedObjectClass()                                                             |                                                 |
| public boolean unfreedObjectClient()                                                        |                                                 |
| public boolean unfreedObjectFinalized()                                                     |                                                 |
| public int unfreedObjectHandle()                                                            |                                                 |
| public int unfreedObjectIdent()                                                             |                                                 |
| public int unfreedObjectUseCount()                                                          |                                                 |
| public str version()                                                                        |                                                 |
| public void checkHeap(str Description, \[int context\], \[int pool\], \[boolean detailed\]) |                                                 |
| public void shrinkPool(\[int poolNo\])                                                      |                                                 |
| public void postCompactingMessage()                                                         |                                                 |
| public void checkHeapDif(str Description, \[int context\], \[int pool\])                    |                                                 |
| public void clearHeapContext()                                                              |                                                 |
| public void writeString(str text)                                                           |                                                 |
| public void firstUnfreedCursor()                                                            |                                                 |
| public void dumpDGMLGraph()                                                                 |                                                 |
| public void firstUnfreedObject()                                                            |                                                 |
| public void setHeapContext(str description)                                                 |                                                 |
| public void new(\[str Filename\])                                                           | Object クラスの新しいインスタンスを初期化します。 |
| public void nextUnfreedObject()                                                             |                                                 |
| public void checkHeapStop()                                                                 |                                                 |
| public void nextUnfreedCursor()                                                             |                                                 |
| public void setRuntimeBugcheckFlags(int flags)                                              |                                                 |
| public void checkHeapStart()                                                                |                                                 |

## <a name="method-accesscnt"></a>メソッド accessCnt

```xpp
public int accessCnt()
```

### <a name="return-value---accesscnt"></a>戻り値 - accessCnt

## <a name="method-addrefcnt"></a>メソッド addRefCnt

```xpp
public int addRefCnt()
```

### <a name="return-value---addrefcnt"></a>戻り値 - addRefCnt

## <a name="method-blocksallocated"></a>メソッド blocksAllocated

```xpp
public Int64 blocksAllocated([int pool])
```

### <a name="parameters---blocksallocated"></a>パラメーター - blocksAllocated

管理グループ  

### <a name="return-value---blocksallocated"></a>戻り値 - blocksAllocated

## <a name="method-breakcount"></a>メソッド breakCount

```xpp
public int breakCount([int count])
```

### <a name="parameters---breakcount"></a>パラメーター - breakCount

カウント  

### <a name="return-value---breakcount"></a>戻り値 - breakCount

## <a name="method-bytesallocated"></a>メソッド bytesAllocated

```xpp
public Int64 bytesAllocated([int pool])
```

### <a name="parameters---bytesallocated"></a>パラメーター - bytesAllocated

管理グループ  

### <a name="return-value---bytesallocated"></a>戻り値 - bytesAllocated

## <a name="method-ceiling"></a>メソッド ceiling

```xpp
public Int64 ceiling(int pool, [int ceiling])
```

### <a name="parameters---ceiling"></a>パラメーター - ceiling

管理グループ  

<!-- -->

ceiling  

### <a name="return-value---ceiling"></a>戻り値 - ceiling

## <a name="method-context"></a>メソッド context

```xpp
public int context([int context])
```

### <a name="parameters---context"></a>パラメーター - context

context  

### <a name="return-value---context"></a>戻り値 - context

## <a name="method-count"></a>メソッド count

```xpp
public int count([int count])
```

### <a name="parameters---count"></a>パラメーター - count

カウント  

### <a name="return-value---count"></a>戻り値 - count

## <a name="method-countobjects"></a>メソッド countObjects

```xpp
public int countObjects(int classId)
```

### <a name="parameters---countobjects"></a>パラメーター - countObjects

classId  

### <a name="return-value---countobjects"></a>戻り値 - countObjects

## <a name="method-createacontainer"></a>メソッド createAContainer

```xpp
public container createAContainer()
```

### <a name="return-value---createacontainer"></a>戻り値 - createAContainer

## <a name="method-cscallcnt"></a>メソッド csCallCnt

```xpp
public int csCallCnt()
```

### <a name="return-value---cscallcnt"></a>戻り値 - csCallCnt

## <a name="method-cssweepcnt"></a>メソッド csSweepCnt

```xpp
public int csSweepCnt()
```

### <a name="return-value---cssweepcnt"></a>戻り値 - csSweepCnt

## <a name="method-databycontext"></a>メソッド dataByContext

```xpp
public container dataByContext([int poolNo], [int context])
```

### <a name="parameters---databycontext"></a>パラメーター - dataByContext

poolNo  

<!-- -->

context  

### <a name="return-value---databycontext"></a>戻り値 - dataByContext

## <a name="method-dumpcursors"></a>メソッド dumpCursors

```xpp
public int dumpCursors()
```

### <a name="return-value---dumpcursors"></a>戻り値 - dumpCursors

## <a name="method-dumpobjects"></a>メソッド dumpObjects

```xpp
public int dumpObjects()
```

### <a name="return-value---dumpobjects"></a>戻り値 - dumpObjects

## <a name="method-filename"></a>メソッド filename

```xpp
public int filename([str filename])
```

### <a name="parameters---filename"></a>パラメーター - filename

filename  

### <a name="return-value---filename"></a>戻り値 - filename

## <a name="method-fixedblocksize"></a>メソッド fixedBlockSize

```xpp
public int fixedBlockSize(int pool, [int blockSize])
```

### <a name="parameters---fixedblocksize"></a>パラメーター - fixedBlockSize

管理グループ  

<!-- -->

blockSize  

### <a name="return-value---fixedblocksize"></a>戻り値 - fixedBlockSize

## <a name="method-floor"></a>メソッド floor

```xpp
public int floor(int pool, [int floor])
```

### <a name="parameters---floor"></a>パラメーター - floor

管理グループ  

<!-- -->

floor  

### <a name="return-value---floor"></a>戻り値 - floor

## <a name="method-freerefcnt"></a>メソッド freeRefCnt

```xpp
public int freeRefCnt()
```

### <a name="return-value---freerefcnt"></a>戻り値 - freeRefCnt

## <a name="method-getruntimebugcheckflags"></a>メソッド getRuntimeBugcheckFlags

```xpp
public int getRuntimeBugcheckFlags()
```

### <a name="return-value---getruntimebugcheckflags"></a>戻り値 - getRuntimeBugcheckFlags

## <a name="method-getunfreedcursor"></a>メソッド getUnfreedCursor

```xpp
public Common getUnfreedCursor()
```

### <a name="return-value---getunfreedcursor"></a>戻り値 - getUnfreedCursor

## <a name="method-getunfreedobject"></a>メソッド getUnfreedObject

```xpp
public Common getUnfreedObject()
```

### <a name="return-value---getunfreedobject"></a>戻り値 - getUnfreedObject

## <a name="method-include"></a>メソッド include

```xpp
public boolean include(int objectNo, [boolean include])
```

### <a name="parameters---include"></a>パラメーター - include

objectNo  

<!-- -->

include  

### <a name="return-value---include"></a>戻り値 - include

## <a name="method-moreunfreedcursors"></a>メソッド moreUnfreedCursors

```xpp
public boolean moreUnfreedCursors()
```

### <a name="return-value---moreunfreedcursors"></a>戻り値 - moreUnfreedCursors

## <a name="method-moreunfreedobjects"></a>メソッド moreUnfreedObjects

```xpp
public boolean moreUnfreedObjects()
```

### <a name="return-value---moreunfreedobjects"></a>戻り値 - moreUnfreedObjects

## <a name="method-objectcontext"></a>メソッド objectContext

```xpp
public int objectContext(int objNo, [int context])
```

### <a name="parameters---objectcontext"></a>パラメーター - objectContext

objNo  

<!-- -->

context  

### <a name="return-value---objectcontext"></a>戻り値 - objectContext

## <a name="method-pagesize"></a>メソッド pageSize

```xpp
public int pageSize(int pool, [int pageSize])
```

### <a name="parameters---pagesize"></a>パラメーター - pageSize

管理グループ  

<!-- -->

pageSize  

### <a name="return-value---pagesize"></a>戻り値 - pageSize

## <a name="method-poolcount"></a>メソッド poolCount

```xpp
public int poolCount()
```

### <a name="return-value---poolcount"></a>戻り値 - poolCount

## <a name="method-poolname"></a>メソッド poolName

```xpp
public str poolName(int poolNo)
```

### <a name="parameters---poolname"></a>パラメーター - poolName

poolNo  

### <a name="return-value---poolname"></a>戻り値 - poolName

## <a name="method-smallblocksize"></a>メソッド smallBlockSize

```xpp
public int smallBlockSize(int pool, [int blockSize])
```

### <a name="parameters---smallblocksize"></a>パラメーター - smallBlockSize

管理グループ  

<!-- -->

blockSize  

### <a name="return-value---smallblocksize"></a>戻り値 - smallBlockSize

## <a name="method-sweepcnt"></a>メソッド sweepCnt

```xpp
public int sweepCnt()
```

### <a name="return-value---sweepcnt"></a>戻り値 - sweepCnt

## <a name="method-testblocks"></a>メソッド testBlocks

```xpp
public int testBlocks([int arg1])
```

### <a name="parameters---testblocks"></a>パラメーター - testBlocks

arg1  

### <a name="return-value---testblocks"></a>戻り値 - testBlocks

## <a name="method-unfreedobjectclass"></a>メソッド unfreedObjectClass

```xpp
public str unfreedObjectClass()
```

### <a name="return-value---unfreedobjectclass"></a>戻り値 - unfreedObjectClass

## <a name="method-unfreedobjectclient"></a>メソッド unfreedObjectClient

```xpp
public boolean unfreedObjectClient()
```

### <a name="return-value---unfreedobjectclient"></a>戻り値 - unfreedObjectClient

## <a name="method-unfreedobjectfinalized"></a>メソッド unfreedObjectFinalized

```xpp
public boolean unfreedObjectFinalized()
```

### <a name="return-value---unfreedobjectfinalized"></a>戻り値 - unfreedObjectFinalized

## <a name="method-unfreedobjecthandle"></a>メソッド unfreedObjectHandle

```xpp
public int unfreedObjectHandle()
```

### <a name="return-value---unfreedobjecthandle"></a>戻り値 - unfreedObjectHandle

## <a name="method-unfreedobjectident"></a>メソッド unfreedObjectIdent

```xpp
public int unfreedObjectIdent()
```

### <a name="return-value---unfreedobjectident"></a>戻り値 - unfreedObjectIdent

## <a name="method-unfreedobjectusecount"></a>メソッド unfreedObjectUseCount

```xpp
public int unfreedObjectUseCount()
```

### <a name="return-value---unfreedobjectusecount"></a>戻り値 - unfreedObjectUseCount

## <a name="method-version"></a>メソッド version

```xpp
public str version()
```

### <a name="return-value---version"></a>戻り値 - version

## <a name="method-checkheap"></a>メソッド checkHeap

```xpp
public void checkHeap(str Description, [int context], [int pool], [boolean detailed])
```

### <a name="parameters---checkheap"></a>パラメーター - checkHeap

説明  

<!-- -->

context  

<!-- -->

管理グループ  

<!-- -->

detailed  

## <a name="method-shrinkpool"></a>メソッド shrinkPool

```xpp
public void shrinkPool([int poolNo])
```

### <a name="parameters---shrinkpool"></a>パラメーター - shrinkPool

poolNo  

## <a name="method-postcompactingmessage"></a>メソッド postCompactingMessage

```xpp
public void postCompactingMessage()
```

## <a name="method-checkheapdif"></a>メソッド checkHeapDif

```xpp
public void checkHeapDif(str Description, [int context], [int pool])
```

### <a name="parameters---checkheapdif"></a>パラメーター - checkHeapDif

説明  

<!-- -->

context  

<!-- -->

管理グループ  

## <a name="method-clearheapcontext"></a>メソッド clearHeapContext

```xpp
public void clearHeapContext()
```

## <a name="method-writestring"></a>メソッド writeString

```xpp
public void writeString(str text)
```

### <a name="parameters---writestring"></a>パラメーター - writeString

テキスト  

## <a name="method-firstunfreedcursor"></a>メソッド firstUnfreedCursor

```xpp
public void firstUnfreedCursor()
```

## <a name="method-dumpdgmlgraph"></a>メソッド dumpDGMLGraph

```xpp
public void dumpDGMLGraph()
```

## <a name="method-firstunfreedobject"></a>メソッド firstUnfreedObject

```xpp
public void firstUnfreedObject()
```

## <a name="method-setheapcontext"></a>メソッド setHeapContext

```xpp
public void setHeapContext(str description)
```

### <a name="parameters---setheapcontext"></a>パラメーター - setHeapContext

説明  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([str Filename])
```

### <a name="parameters---new"></a>パラメーター - new

ファイル名  

## <a name="method-nextunfreedobject"></a>メソッド nextUnfreedObject

```xpp
public void nextUnfreedObject()
```

## <a name="method-checkheapstop"></a>メソッド checkHeapStop

```xpp
public void checkHeapStop()
```

## <a name="method-nextunfreedcursor"></a>メソッド nextUnfreedCursor

```xpp
public void nextUnfreedCursor()
```

## <a name="method-setruntimebugcheckflags"></a>メソッド setRuntimeBugcheckFlags

```xpp
public void setRuntimeBugcheckFlags(int flags)
```

### <a name="parameters---setruntimebugcheckflags"></a>パラメーター - setRuntimeBugcheckFlags

flags  

## <a name="method-checkheapstart"></a>メソッド checkHeapStart

```xpp
public void checkHeapStart()
```

