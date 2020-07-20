---
title: PerformanceMonitor クラス
description: このトピックでは、PerformanceMonitor クラスについて説明します。
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
ms.openlocfilehash: e52265cfd029b9b60882b1d2b78fd901fc752668
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502541"
---
# <a name="class-performancemonitor"></a>クラス PerformanceMonitor

[!include [banner](../../includes/banner.md)]

```xpp
class PerformanceMonitor extends Object
```

PerformanceMonitor クラスは、システムで実行されているプロセスのデータをフェッチします。

## <a name="remarks"></a>備考

いつでもシステムのスナップショットを取得して、システムで実行されている任意のプロセスのカウンター上で移動することができます。

## <a name="examples"></a>例

次の例は、現在実行中のすべてのプロセスの processId および workingset 値を出力します。

```xpp
static void pvPerformanceMonitorTest(args a) 
{ 
    int i, j;  
    PerformanceMonitorInstance instance;  
    PerformanceMonitorCounter counter1, counter2;  
    PerformanceMonitor pm = new PerformanceMonitor();  
    // Take a current snapshot of the system. 
    pm.takeSnapshot ();  
    // Traverse all the running processes. 
    for (i= 1; i <= pm.instanceCount(); i++)  
    {  
        instance = pm.instance(i);  
        counter1 = instance.getCounter("ID Process");  
        counter2 = instance.getCounter("Working Set");  
        print instance.name(), " ",  
        counter1.intData(), " ",  
        counter2.intData();  
    } 
    pause;  
}
```

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                    |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| public PerformanceMonitorInstance instance(int instanceNo) |                                                                                                |
| public int instanceCount()                                 | インスタンス数 (現在のスナップショットのプロセスの数) を返します。          |
| public int processId()                                     | このメソッドを実行しているプロセスの processId 値を返します。                        |
| public str systemName()                                    |                                                                                                |
| public boolean takeSnapshot(\[str processName\])           |                                                                                                |
| public str toString()                                      | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。 |
| public void new()                                          | PerformanceMonitor クラスの新しいインスタンスを初期化します。                                    |

## <a name="method-instance"></a>メソッド instance

```xpp
public PerformanceMonitorInstance instance(int instanceNo)
```

### <a name="parameters---instance"></a>パラメーター - instance

instanceNo  

### <a name="return-value---instance"></a>戻り値 - instance

## <a name="method-instancecount"></a>メソッド instanceCount

インスタンス数 (現在のスナップショットのプロセスの数) を返します。

```xpp
public int instanceCount()
```

### <a name="return-value---instancecount"></a>戻り値 - instanceCount

現在のスナップショット内のプロセス数。

### <a name="remarks---instancecount"></a>備考 - instanceCount

現在実行中のプロセスのスナップショットを取得するには、takeSnapshot メソッドを使用します。

### <a name="examples---instancecount"></a>例 - instanceCount

```xpp
static void pvPerformanceMonitorTest(args a) 
{ 
    int i, j; 
    PerformanceMonitorInstance instance; 
    PerformanceMonitorCounter counter1, counter2; 
    PerformanceMonitor pm = new PerformanceMonitor(); 
    // Take a current snapshot of the system. 
    pm.takeSnapshot (); 
    // Traverse all the running processes. 
    for (i= 1; i <= pm.instanceCount(); i++) 
    { 
        instance = pm.instance(i); 
        counter1 = instance.getCounter("ID Process"); 
        counter2 = instance.getCounter("Working Set"); 
        print instance.name(), " ",  
            counter1.intData(), " ",  
            counter2.intData(); 
    } 
    pause; 
}
```

## <a name="method-processid"></a>メソッド processId

このメソッドを実行しているプロセスの processId 値を返します。

```xpp
public int processId()
```

### <a name="return-value---processid"></a>戻り値 - processId

このメソッドを実行しているプロセスの processId 値です。

### <a name="examples---processid"></a>例 - processId

```xpp
static void processIdDemo(args a) 
{ 
    PerformanceMonitor pm = new PerformanceMonitor(); 
    print pm.processId(); 
    pause; 
}
```

## <a name="method-systemname"></a>メソッド systemName

```xpp
public str systemName()
```

### <a name="return-value---systemname"></a>戻り値 - systemName

## <a name="method-takesnapshot"></a>メソッド takeSnapshot

```xpp
public boolean takeSnapshot([str processName])
```

### <a name="parameters---takesnapshot"></a>パラメーター - takeSnapshot

processName  

### <a name="return-value---takesnapshot"></a>戻り値 - takeSnapshot

## <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

クラスのテキストの説明。

### <a name="remarks---tostring"></a>備考 - toString

既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。 ただし、一部のクラスでは、追加情報が文字列で返されます。

## <a name="method-new"></a>メソッド new

PerformanceMonitor クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

