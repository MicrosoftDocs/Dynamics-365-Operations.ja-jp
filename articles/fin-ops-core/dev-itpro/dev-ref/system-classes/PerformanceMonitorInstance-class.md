---
title: PerformanceMonitorInstance クラス
description: このトピックでは、PerformanceMonitorInstance クラスについて説明します。
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
ms.openlocfilehash: 7bbbbc368736fe767d301cc8479c305039e94865
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502535"
---
# <a name="class-performancemonitorinstance"></a>クラス PerformanceMonitorInstance

[!include [banner](../../includes/banner.md)]

```xpp
class PerformanceMonitorInstance extends Object
```

PerformanceMonitorInstance クラスは、プロセス モニターが実行されるコンピューターで実行されているプロセスを表します。

## <a name="remarks"></a>備考

このクラスは、プロセス カウンターのクエリを可能にします。 このクラスのオブジェクトを使用してプロセス カウンターをクエリすることができます。 各カウンターは、プロセス パラメーターを表します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                       | 説明                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| public PerformanceMonitorCounter getCounter(str counterName) |                                                                                                |
| public str name()                                            |                                                                                                |
| public str toString()                                        | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。 |

## <a name="method-getcounter"></a>メソッド getCounter

```xpp
public PerformanceMonitorCounter getCounter(str counterName)
```

### <a name="parameters---getcounter"></a>パラメーター - getCounter

counterName  

### <a name="return-value---getcounter"></a>戻り値 - getCounter

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

クラスのテキストの説明を返します。

### <a name="remarks---tostring"></a>備考 - toString

既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。 ただし、一部のクラスでは、追加情報が文字列で返されます。

