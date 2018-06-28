---
title: "H クラス"
description: "文字 H で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52591
ms.assetid: c27e2044-28c2-432a-b15f-a41d26a83a52
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8c3de0e154d205eb556867b077e38882692b1a0d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="h-classes"></a>H クラス

[!include [banner](../includes/banner.md)]

文字 H で始まるシステム API クラス。

<a name="class-heapcheck"></a>クラス HeapCheck
---------------

    class HeapCheck extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-accesscnt"></a>メソッド accessCnt

    public int accessCnt()

#### <a name="return-value"></a>戻り値

### <a name="method-addrefcnt"></a>メソッド addRefCnt

    public int addRefCnt()

#### <a name="return-value"></a>戻り値

### <a name="method-blocksallocated"></a>メソッド blocksAllocated

    public Int64 blocksAllocated([int pool])

#### <a name="parameters"></a>パラメーター

管理グループ  

#### <a name="return-value"></a>戻り値

### <a name="method-breakcount"></a>メソッド breakCount

    public int breakCount([int count])

#### <a name="parameters"></a>パラメーター

カウント  

#### <a name="return-value"></a>戻り値

### <a name="method-bytesallocated"></a>メソッド bytesAllocated

    public Int64 bytesAllocated([int pool])

#### <a name="parameters"></a>パラメーター

管理グループ  

#### <a name="return-value"></a>戻り値

### <a name="method-ceiling"></a>メソッド ceiling

    public Int64 ceiling(int pool, [int ceiling])

#### <a name="parameters"></a>パラメーター

管理グループ  

<!-- -->

ceiling  

#### <a name="return-value"></a>戻り値

### <a name="method-context"></a>メソッド context

    public int context([int context])

#### <a name="parameters"></a>パラメーター

context  

#### <a name="return-value"></a>戻り値

### <a name="method-count"></a>メソッド count

    public int count([int count])

#### <a name="parameters"></a>パラメーター

カウント  

#### <a name="return-value"></a>戻り値

### <a name="method-countobjects"></a>メソッド countObjects

    public int countObjects(int classId)

#### <a name="parameters"></a>パラメーター

classId  

#### <a name="return-value"></a>戻り値

### <a name="method-createacontainer"></a>メソッド createAContainer

    public container createAContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-cscallcnt"></a>メソッド csCallCnt

    public int csCallCnt()

#### <a name="return-value"></a>戻り値

### <a name="method-cssweepcnt"></a>メソッド csSweepCnt

    public int csSweepCnt()

#### <a name="return-value"></a>戻り値

### <a name="method-databycontext"></a>メソッド dataByContext

    public container dataByContext([int poolNo], [int context])

#### <a name="parameters"></a>パラメーター

poolNo  

<!-- -->

context  

#### <a name="return-value"></a>戻り値

### <a name="method-dumpcursors"></a>メソッド dumpCursors

    public int dumpCursors()

#### <a name="return-value"></a>戻り値

### <a name="method-dumpobjects"></a>メソッド dumpObjects

    public int dumpObjects()

#### <a name="return-value"></a>戻り値

### <a name="method-filename"></a>メソッド filename

    public int filename([str filename])

#### <a name="parameters"></a>パラメーター

filename  

#### <a name="return-value"></a>戻り値

### <a name="method-fixedblocksize"></a>メソッド fixedBlockSize

    public int fixedBlockSize(int pool, [int blockSize])

#### <a name="parameters"></a>パラメーター

管理グループ  

<!-- -->

blockSize  

#### <a name="return-value"></a>戻り値

### <a name="method-floor"></a>メソッド floor

    public int floor(int pool, [int floor])

#### <a name="parameters"></a>パラメーター

管理グループ  

<!-- -->

floor  

#### <a name="return-value"></a>戻り値

### <a name="method-freerefcnt"></a>メソッド freeRefCnt

    public int freeRefCnt()

#### <a name="return-value"></a>戻り値

### <a name="method-getruntimebugcheckflags"></a>メソッド getRuntimeBugcheckFlags

    public int getRuntimeBugcheckFlags()

#### <a name="return-value"></a>戻り値

### <a name="method-getunfreedcursor"></a>メソッド getUnfreedCursor

    public Common getUnfreedCursor()

#### <a name="return-value"></a>戻り値

### <a name="method-getunfreedobject"></a>メソッド getUnfreedObject

    public Common getUnfreedObject()

#### <a name="return-value"></a>戻り値

### <a name="method-include"></a>メソッド include

    public boolean include(int objectNo, [boolean include])

#### <a name="parameters"></a>パラメーター

objectNo  

<!-- -->

include  

#### <a name="return-value"></a>戻り値

### <a name="method-moreunfreedcursors"></a>メソッド moreUnfreedCursors

    public boolean moreUnfreedCursors()

#### <a name="return-value"></a>戻り値

### <a name="method-moreunfreedobjects"></a>メソッド moreUnfreedObjects

    public boolean moreUnfreedObjects()

#### <a name="return-value"></a>戻り値

### <a name="method-objectcontext"></a>メソッド objectContext

    public int objectContext(int objNo, [int context])

#### <a name="parameters"></a>パラメーター

objNo  

<!-- -->

context  

#### <a name="return-value"></a>戻り値

### <a name="method-pagesize"></a>メソッド pageSize

    public int pageSize(int pool, [int pageSize])

#### <a name="parameters"></a>パラメーター

管理グループ  

<!-- -->

pageSize  

#### <a name="return-value"></a>戻り値

### <a name="method-poolcount"></a>メソッド poolCount

    public int poolCount()

#### <a name="return-value"></a>戻り値

### <a name="method-poolname"></a>メソッド poolName

    public str poolName(int poolNo)

#### <a name="parameters"></a>パラメーター

poolNo  

#### <a name="return-value"></a>戻り値

### <a name="method-smallblocksize"></a>メソッド smallBlockSize

    public int smallBlockSize(int pool, [int blockSize])

#### <a name="parameters"></a>パラメーター

管理グループ  

<!-- -->

blockSize  

#### <a name="return-value"></a>戻り値

### <a name="method-sweepcnt"></a>メソッド sweepCnt

    public int sweepCnt()

#### <a name="return-value"></a>戻り値

### <a name="method-testblocks"></a>メソッド testBlocks

    public int testBlocks([int arg1])

#### <a name="parameters"></a>パラメーター

arg1  

#### <a name="return-value"></a>戻り値

### <a name="method-unfreedobjectclass"></a>メソッド unfreedObjectClass

    public str unfreedObjectClass()

#### <a name="return-value"></a>戻り値

### <a name="method-unfreedobjectclient"></a>メソッド unfreedObjectClient

    public boolean unfreedObjectClient()

#### <a name="return-value"></a>戻り値

### <a name="method-unfreedobjectfinalized"></a>メソッド unfreedObjectFinalized

    public boolean unfreedObjectFinalized()

#### <a name="return-value"></a>戻り値

### <a name="method-unfreedobjecthandle"></a>メソッド unfreedObjectHandle

    public int unfreedObjectHandle()

#### <a name="return-value"></a>戻り値

### <a name="method-unfreedobjectident"></a>メソッド unfreedObjectIdent

    public int unfreedObjectIdent()

#### <a name="return-value"></a>戻り値

### <a name="method-unfreedobjectusecount"></a>メソッド unfreedObjectUseCount

    public int unfreedObjectUseCount()

#### <a name="return-value"></a>戻り値

### <a name="method-version"></a>メソッド version

    public str version()

#### <a name="return-value"></a>戻り値

### <a name="method-checkheap"></a>メソッド checkHeap

    public void checkHeap(str Description, [int context], [int pool], [boolean detailed])

#### <a name="parameters"></a>パラメーター

説明  

<!-- -->

context  

<!-- -->

管理グループ  

<!-- -->

detailed  

### <a name="method-shrinkpool"></a>メソッド shrinkPool

    public void shrinkPool([int poolNo])

#### <a name="parameters"></a>パラメーター

poolNo  

### <a name="method-postcompactingmessage"></a>メソッド postCompactingMessage

    public void postCompactingMessage()

### <a name="method-checkheapdif"></a>メソッド checkHeapDif

    public void checkHeapDif(str Description, [int context], [int pool])

#### <a name="parameters"></a>パラメーター

説明  

<!-- -->

context  

<!-- -->

管理グループ  

### <a name="method-clearheapcontext"></a>メソッド clearHeapContext

    public void clearHeapContext()

### <a name="method-writestring"></a>メソッド writeString

    public void writeString(str text)

#### <a name="parameters"></a>パラメーター

テキスト  

### <a name="method-firstunfreedcursor"></a>メソッド firstUnfreedCursor

    public void firstUnfreedCursor()

### <a name="method-dumpdgmlgraph"></a>メソッド dumpDGMLGraph

    public void dumpDGMLGraph()

### <a name="method-firstunfreedobject"></a>メソッド firstUnfreedObject

    public void firstUnfreedObject()

### <a name="method-setheapcontext"></a>メソッド setHeapContext

    public void setHeapContext(str description)

#### <a name="parameters"></a>パラメーター

description  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([str Filename])

#### <a name="parameters"></a>パラメーター

ファイル名  

### <a name="method-nextunfreedobject"></a>メソッド nextUnfreedObject

    public void nextUnfreedObject()

### <a name="method-checkheapstop"></a>メソッド checkHeapStop

    public void checkHeapStop()

### <a name="method-nextunfreedcursor"></a>メソッド nextUnfreedCursor

    public void nextUnfreedCursor()

### <a name="method-setruntimebugcheckflags"></a>メソッド setRuntimeBugcheckFlags

    public void setRuntimeBugcheckFlags(int flags)

#### <a name="parameters"></a>パラメーター

flags  

### <a name="method-checkheapstart"></a>メソッド checkHeapStart

    public void checkHeapStart()

## <a name="class-helpdocsetnode"></a>クラス HelpDocSetNode
    class HelpDocSetNode extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                |
|------------------------------------------------------------|----------------------------------------------------------------------------|
| public boolean addToApplicationHelpMenu(\[boolean value\]) |                                                                            |
| public boolean addToDeveloperHelpMenu(\[boolean value\])   |                                                                            |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。 |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。              |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。              |
| public int contentLocation(\[int value\])                  |                                                                            |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。      |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                   |
| public str creationTime(\[str value\])                     |                                                                            |
| public boolean developerDocumentSet(\[boolean value\])     |                                                                            |
| public str documentSetDescription(\[str value\])           |                                                                            |
| public str documentSetName(\[str value\])                  |                                                                            |
| public str helpProviderClass(\[str value\])                |                                                                            |
| public Guid origin(\[Guid value\])                         |                                                                            |
| public boolean userDocumentSet(\[boolean value\])          |                                                                            |
| public void new(str DocSetName)                            | TreeNode クラスの新しいインスタンスを初期化します。                          |

### <a name="method-addtoapplicationhelpmenu"></a>メソッド addToApplicationHelpMenu

    public boolean addToApplicationHelpMenu([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-addtodeveloperhelpmenu"></a>メソッド addToDeveloperHelpMenu

    public boolean addToDeveloperHelpMenu([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-contentlocation"></a>メソッド contentLocation

    public int contentLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-developerdocumentset"></a>メソッド developerDocumentSet

    public boolean developerDocumentSet([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-documentsetdescription"></a>メソッド documentSetDescription

    public str documentSetDescription([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-documentsetname"></a>メソッド documentSetName

    public str documentSetName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helpproviderclass"></a>メソッド helpProviderClass

    public str helpProviderClass([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdocumentset"></a>メソッド userDocumentSet

    public boolean userDocumentSet([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str DocSetName)

#### <a name="parameters"></a>パラメーター

DocSetName  

## <a name="class-helpdocumentmanager"></a>クラス HelpDocumentManager
    class HelpDocumentManager extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                              | 説明                                                  |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| public void new()                                                                                                   | HelpDocumentManager クラスの新しいインスタンスを初期化します。 |
| ::public static void showHelpTopic(\[str topic\], \[str documentSet\], \[str contentLanguage\], \[str uiLanguage\]) |                                                              |
| public void finalize()                                                                                              |                                                              |

### <a name="method-new"></a>メソッド new

HelpDocumentManager クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-showhelptopic"></a>メソッド showHelpTopic

    public static void showHelpTopic([str topic], [str documentSet], [str contentLanguage], [str uiLanguage])

#### <a name="parameters"></a>パラメーター

トピック  

<!-- -->

documentSet  

<!-- -->

contentLanguage  

<!-- -->

uiLanguage  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-htmlfont"></a>クラス HtmlFont
    class HtmlFont extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                    | 説明                                     |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public int backColor(\[int value\])                                                                       |                                                 |
| public str fontName(\[str value\])                                                                        |                                                 |
| public int pointSize(\[int value\])                                                                       |                                                 |
| public int style(\[int value\])                                                                           |                                                 |
| public int textColor(\[int value\])                                                                       |                                                 |
| public void new(\[str TypeFace\], \[int PointSize\], \[int Style\], \[int TextColor\], \[int BackColor\]) | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                                                    |                                                 |

### <a name="method-backcolor"></a>メソッド backColor

    public int backColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fontname"></a>メソッド fontName

    public str fontName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-pointsize"></a>メソッド pointSize

    public int pointSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-textcolor"></a>メソッド textColor

    public int textColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([str TypeFace], [int PointSize], [int Style], [int TextColor], [int BackColor])

#### <a name="parameters"></a>パラメーター

TypeFace  

<!-- -->

PointSize  

<!-- -->

スタイル  

<!-- -->

TextColor  

<!-- -->

BackColor  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()




