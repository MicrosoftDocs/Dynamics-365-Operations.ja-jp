---
title: AOSSessionInfo クラス
description: このトピックでは、AOSSessionInfo クラスについて説明します。
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
ms.openlocfilehash: 6a834ddbe74577370f0e4eb0dbae700d196c784a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502753"
---
# <a name="class-aossessioninfo"></a>クラス AOSSessionInfo

[!include [banner](../../includes/banner.md)]

```xpp
class AOSSessionInfo extends Object
```

AOSSessionInfo クラスは、Application Object Server (AOS) のセッションに関する情報を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                             | 説明                                                               |
|------------------------------------|---------------------------------------------------------------------------|
| public AOSClientMode clientMode()  | AOS セッションのクライアント モードを返します。                              |
| public int cpuTime()               | CPU が AOS セッションに使用するミリ秒数を返します。 |
| public int idleTicks()             | AOS との最後の通信以降のミリ秒数を返します。 |
| public int sessionId()             | AOS セッションの ID を返します。                                        |
| public void new(\[int sessionId\]) | AOSSessionInfo クラスのインスタンスを作成します。                          |

## <a name="method-clientmode"></a>メソッド clientMode

AOS セッションのクライアント モードを返します。

```xpp
public AOSClientMode clientMode()
```

### <a name="return-value---clientmode"></a>戻り値 - clientMode

AOS セッションのクライアント モード。

## <a name="method-cputime"></a>メソッド cpuTime

CPU が AOS セッションに使用するミリ秒数を返します。

```xpp
public int cpuTime()
```

### <a name="return-value---cputime"></a>戻り値 - cpuTime

CPU が AOS セッションに使用するミリ秒数。

## <a name="method-idleticks"></a>メソッド idleTicks

AOS との最後の通信以降のミリ秒数を返します。

```xpp
public int idleTicks()
```

### <a name="return-value---idleticks"></a>戻り値 - idleTicks

AOS との最後の通信以降のミリ秒数。

## <a name="method-sessionid"></a>メソッド sessionId

AOS セッションの ID を返します。

```xpp
public int sessionId()
```

### <a name="return-value---sessionid"></a>戻り値 - sessionId

AOS セッションの ID。

## <a name="method-new"></a>メソッド new

AOSSessionInfo クラスのインスタンスを作成します。

```xpp
public void new([int sessionId])
```

### <a name="parameters---new"></a>パラメーター - new

sessionId  
AOSSessionInfo クラスのインスタンスを作成するために使用されるセッション ID。 セッション ID が指定されていない場合、現在のセッションが使用されます; 省略。

