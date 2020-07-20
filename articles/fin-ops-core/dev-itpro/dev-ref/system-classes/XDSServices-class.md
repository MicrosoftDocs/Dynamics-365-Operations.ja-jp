---
title: XDSServices クラス
description: このトピックでは、XDSServices クラスについて説明します。
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
ms.openlocfilehash: 75e51246809898b3c85be2a8c19f40fb4fe87352
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502684"
---
# <a name="class-xdsservices"></a>クラス XDSServices

[!include [banner](../../includes/banner.md)]

```xpp
class XDSServices extends Object
```

XDSServices クラスは、拡張可能なデータ セキュリティ (XDS) 動作を管理するための API を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                 | 説明                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public int flushXDSMyConstructs(int reserved, str tablename)           | XDS で使用される MyConstruct テーブルをフラッシュします。                                                                              |
| public str getQuerySQL(str queryname)                                  |                                                                                                                                   |
| public str getTableSQL(str tablename, \[str policyname\])              |                                                                                                                                   |
| public str getXDSBinding(str name)                                     |                                                                                                                                   |
| public str getXDSContext(int reserved)                                 |                                                                                                                                   |
| public int getXDSToFlushPerServiceSession(int reserved)                | サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかをチェックします。                           |
| public void finalize()                                                 |                                                                                                                                   |
| public void new()                                                      | XDSServices クラスの新しいインスタンスを初期化します。                                                                              |
| public void setXDSContext(int reserved, str contextstring)             |                                                                                                                                   |
| public void setXDSBinding(str name, str value)                         |                                                                                                                                   |
| public void setXDSState(int finalState)                                |                                                                                                                                   |
| public void setXDSToFlushPerServiceSession(int reserved, int newstate) | サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかを決定する設定を設定します。 |
| public void setXDSTrace(int flag, str value)                           |                                                                                                                                   |

## <a name="method-flushxdsmyconstructs"></a>メソッド flushXDSMyConstructs

XDS で使用される MyConstruct テーブルをフラッシュします。

```xpp
public int flushXDSMyConstructs(int reserved, str tablename)
```

### <a name="parameters---flushxdsmyconstructs"></a>パラメーター - flushXDSMyConstructs

reserved  
フラッシュする MyConstruct テーブルの名前。 値が渡されない場合、または空の文字列が渡される場合、すべての MyConstruct テーブルがフラッシュされます。

<!-- -->

tablename  
フラッシュする MyConstruct テーブルの名前。 値が渡されない場合、または空の文字列が渡される場合、すべての MyConstruct テーブルがフラッシュされます。

### <a name="return-value---flushxdsmyconstructs"></a>戻り値 - flushXDSMyConstructs

## <a name="method-getquerysql"></a>メソッド getQuerySQL

```xpp
public str getQuerySQL(str queryname)
```

### <a name="parameters---getquerysql"></a>パラメーター - getQuerySQL

queryname  

### <a name="return-value---getquerysql"></a>戻り値 - getQuerySQL

## <a name="method-gettablesql"></a>メソッド getTableSQL

```xpp
public str getTableSQL(str tablename, [str policyname])
```

### <a name="parameters---gettablesql"></a>パラメーター - getTableSQL

tablename  

<!-- -->

policyname  

### <a name="return-value---gettablesql"></a>戻り値 - getTableSQL

## <a name="method-getxdsbinding"></a>メソッド getXDSBinding

```xpp
public str getXDSBinding(str name)
```

### <a name="parameters---getxdsbinding"></a>パラメーター - getXDSBinding

名前  

### <a name="return-value---getxdsbinding"></a>戻り値 - getXDSBinding

## <a name="method-getxdscontext"></a>メソッド getXDSContext

```xpp
public str getXDSContext(int reserved)
```

### <a name="parameters---getxdscontext"></a>パラメーター - getXDSContext

reserved  

### <a name="return-value---getxdscontext"></a>戻り値 - getXDSContext

## <a name="method-getxdstoflushperservicesession"></a>メソッド getXDSToFlushPerServiceSession

サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかをチェックします。

```xpp
public int getXDSToFlushPerServiceSession(int reserved)
```

### <a name="parameters---getxdstoflushperservicesession"></a>パラメーター - getXDSToFlushPerServiceSession

reserved  
予約済フラグ、現在使用されていません。

### <a name="return-value---getxdstoflushperservicesession"></a>戻り値 - getXDSToFlushPerServiceSession

サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされる場合は 1、それ以外の場合は 0 です。

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

XDSServices クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-setxdscontext"></a>メソッド setXDSContext

```xpp
public void setXDSContext(int reserved, str contextstring)
```

### <a name="parameters---setxdscontext"></a>パラメーター - setXDSContext

reserved  

<!-- -->

contextstring  

## <a name="method-setxdsbinding"></a>メソッド setXDSBinding

```xpp
public void setXDSBinding(str name, str value)
```

### <a name="parameters---setxdsbinding"></a>パラメーター - setXDSBinding

名前  

<!-- -->

値  

## <a name="method-setxdsstate"></a>メソッド setXDSState

```xpp
public void setXDSState(int finalState)
```

### <a name="parameters---setxdsstate"></a>パラメーター - setXDSState

finalState  

## <a name="method-setxdstoflushperservicesession"></a>メソッド setXDSToFlushPerServiceSession

サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかを決定する設定を設定します。

```xpp
public void setXDSToFlushPerServiceSession(int reserved, int newstate)
```

### <a name="parameters---setxdstoflushperservicesession"></a>パラメーター - setXDSToFlushPerServiceSession

reserved  
サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュするかどうかを示す値。 テーブルにフラッシュする場合は 1 を、フラッシュしない場合は 0 を渡します。

<!-- -->

newstate  
サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュするかどうかを示す値。 テーブルにフラッシュする場合は 1 を、フラッシュしない場合は 0 を渡します。

## <a name="method-setxdstrace"></a>メソッド setXDSTrace

```xpp
public void setXDSTrace(int flag, str value)
```

### <a name="parameters---setxdstrace"></a>パラメーター - setXDSTrace

flag  

<!-- -->

値  

