---
title: Object クラス
description: このトピックでは、Object クラスについて説明します。
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
ms.openlocfilehash: 12a3c9e9fccfe809ea5011e63c956ac37b256a34
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502566"
---
# <a name="class-object"></a>クラス オブジェクト

[!include [banner](../../includes/banner.md)]


```xpp
class Object
```

Object クラスは、その他のすべてのクラスの派生元となる基本クラスです。

## <a name="remarks"></a>備考

オブジェクト クラスのメソッドは、任意のオブジェクトに対して呼び出すことができます。 Object クラスは、開発者がオブジェクトの実際のタイプを知らなくても、割り当ておよび等価チェックを実行できるようにするために使用されます。 メソッドは 3 つのグループにグループ化できます。

-   タイム アウト メソッド - 指定した時間が経過した後にメソッドをアクティブにするために使用できます。
-   プロセス フローを制御したり、別のオブジェクトがそのタスクを終了するを待機するために使用される、Wait、Notify、NotifyAll メソッドなどのメソッドを処理します。
-   クラス メソッド - オブジェクトに関する基本情報を返します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                      | 説明                                                                                                 |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public boolean equal(Object object)                                         | 指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。                                        |
| public int getTimeOutTimerHandle()                                          | オブジェクトのタイマー ハンドルを返します。                                                                    |
| public ClassId handle()                                                     | オブジェクトのクラスのハンドルを取得します。                                                            |
| public boolean SysObsoleteAttribute()                                       |                                                                                                             |
| public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\]) |                                                                                                             |
| public str toString()                                                       | 現在のオブジェクトを表す文字列を返します。                                                        |
| public int usageCount()                                                     | オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。 |
| public str xml(\[int indent\])                                              | 現在のオブジェクトを表す XML 文字列を返します。                                                   |
| public boolean Equals(System.Object obj)                                    |                                                                                                             |
| public int GetHashCode()                                                    |                                                                                                             |
| public void finalize()                                                      |                                                                                                             |
| public void wait()                                                          | プロセスを一時停止します。                                                                                           |
| public void cancelTimeOut(int timerHandle)                                  | setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。                                                    |
| public void new()                                                           | Object クラスの新しいインスタンスを初期化します。                                                             |
| public void notify()                                                        | このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。                              |
| public void notifyAll()                                                     | このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。                            |

## <a name="method-equal"></a>メソッド equal

指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。

```xpp
public boolean equal(Object object)
```

### <a name="parameters---equal"></a>パラメーター - equal

オブジェクト  
現在のオブジェクトと比較するオブジェクト。

### <a name="return-value---equal"></a>戻り値 - equal

指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。 ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。

### <a name="examples---equal"></a>例 - equal

次の例では、現在のインスタンスと別のオブジェクトを比較します。

```xpp
static void Object_Equal(Args _args) 
{ 
    Object objA = new Object(); 
    Object objB = new Object(); 
    print objA.equal(objA);  // true. 
    print objA.equal(objB);  // false. 
    objA = objB; 
    print objA.equal(objB);  // true. 
 }
```

## <a name="method-gettimeouttimerhandle"></a>メソッド getTimeOutTimerHandle

オブジェクトのタイマー ハンドルを返します。

```xpp
public int getTimeOutTimerHandle()
```

### <a name="return-value---gettimeouttimerhandle"></a>戻り値 - getTimeOutTimerHandle

オブジェクトのタイマー ハンドル。

### <a name="remarks---gettimeouttimerhandle"></a>備考 - getTimeOutTimerHandle

オブジェクトのタイマー ハンドルは、setTimeOut メソッドを呼び出すことによって設定されます。

### <a name="examples---gettimeouttimerhandle"></a>例 - getTimeOutTimerHandle

次の例では、タイムアウトを設定してから、タイムアウトをキャンセルします。

```xpp
public void myJob() 
{ 
    int timerHandle = 0; 
    this.setTimeOut(identifierstr(workerFunction), 0); 
    //Perform some operations. 
    timerHandle = this.getTimeOutTimerHandle(); 
    this.cancelTimeOut( timerHandle ); 
}
```

## <a name="method-handle"></a>メソッド handle

オブジェクトのクラスのハンドルを取得します。

```xpp
public ClassId handle()
```

### <a name="return-value---handle"></a>戻り値 - handle

現在のオブジェクトのクラスのハンドル、つまり classId プロパティです。

### <a name="remarks---handle"></a>備考 - handle

クラスの処理が後のリリースで変更されない、またはユーザー定義クラスのエクスポートまたはインポートの後に変更されないという保証はありません。 このメソッドによって返される値を、クラスを参照する永続的な定数として使用しないことを強くお勧めします。

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public boolean SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public int SysObsoleteAttribute(str Method, int WaitTime, [boolean idle])
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

方法  

<!-- -->

WaitTime  

<!-- -->

idle  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="examples---tostring"></a>例 - toString

次の例では、o のクラス名を出力します。

```xpp
static void Object_ToString_Job(Args _args) 
{ 
    Object o = new Object(); 
    print o.toString();  // Prints out: "Class Object" 
    pause; 
}
```

## <a name="method-usagecount"></a>メソッド usageCount

オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。

```xpp
public int usageCount()
```

### <a name="return-value---usagecount"></a>戻り値 - usageCount

オブジェクトが持つ参照の現在の数。

### <a name="remarks---usagecount"></a>備考 - usageCount

オブジェクトが作成されると、その参照カウンターが 1 になります。 新しい参照が作成されると、その値が増加します。 スコープ外の参照は、値が減少します。

### <a name="examples---usagecount"></a>例 - usageCount

次の例では、objA の参照の数を出力ウィンドウに出力します。

```xpp
static void Object_UsageCount(Args _args) 
{ 
    Object objA = new Object(); 
    Object objB; 
    print objA.usageCount();    // Prints 1. 
    objB = objA;                // objB is a reference to objA. 
    print objA.usageCount();    // prints 2 
    pause; 
}
```

## <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a>パラメーター - xml

インデント  
返された XML 文字列のインデントの量 (省略可能)。

### <a name="return-value---xml"></a>戻り値 - xml

現在のオブジェクトを表す XML 文字列です。

### <a name="remarks---xml"></a>備考 - xml

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

## <a name="method-equals"></a>メソッド Equals

```xpp
public boolean Equals(System.Object obj)
```

### <a name="parameters---equals"></a>パラメーター - Equals

obj  

### <a name="return-value---equals"></a>戻り値 - Equals 

## <a name="method-gethashcode"></a>メソッド GetHashCode

```xpp
public int GetHashCode()
```

### <a name="return-value---gethashcode"></a>戻り値 - GetHashCode

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-wait"></a>メソッド wait

プロセスを一時停止します。

```xpp
public void wait()
```

### <a name="remarks---wait"></a>備考 - wait

このメソッドの最も一般的な使い方は、ユーザーに何らかの入力を求めるオブジェクトを開始し、そのオブジェクト (フォームなど) の wait メソッドを呼び出すことです。 次のコード行は、オブジェクトが notify メソッド または notifyAll メソッドを呼び出すまで実行されません。 フォームから wait メソッドが呼び出されるとき、ユーザーは通知メソッドを手動で呼び出す必要はありません。それは、ユーザーがフォームを閉じるか、または [適用] ボタンを押すと、フォームが Object.notifyAll メソッドを呼び出すためです。 このメソッドはスレッドの同期のためのものではありません。 代わりに waitUntilSignaled メソッドを使用します。

### <a name="examples---wait"></a>例 - wait

次の例では、GetUserInput ダイアログを開き、ブロックし、ユーザーがフォームを閉じるまで待機します。

```xpp
{ 
    Args a = new Args("GetUserInput"); 
    formRun fr = new formRun(a); 
    fr.init(); 
    fr.run(); 
    fr.wait(); 
    // Execution will resume at this point, only after 
    // the user has closed the form. 
}
```

## <a name="method-canceltimeout"></a>メソッド cancelTimeOut

setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。

```xpp
public void cancelTimeOut(int timerHandle)
```

### <a name="parameters---canceltimeout"></a>パラメーター - cancelTimeOut

timerHandle  
削除する予定イベントのハンドル。 ハンドルは、Object.setTimeOut メソッドによって返される値です。

### <a name="remarks---canceltimeout"></a>備考 - cancelTimeOut

まだ処理されていないスケジュールされたタイムアウト呼び出しは、オブジェクト自体が削除されると自動的に削除されます。

### <a name="examples---canceltimeout"></a>例 - cancelTimeOut

次の例では、Object.setTimeOut メソッドを呼び出した後、タイムアウトをキャンセルします。

```xpp
void Object_cancelTimeOut(Args _args) 
{ 
    int th; // timerHandle. 
    // timedMethod is a worker method. 
    th = this.setTimeOut( "timedMethod", 2000 ); 
    //.... 
    // Remove timeOut later. 
    CancelTimeOut(th); 
}
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-notify"></a>メソッド notify

このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。

```xpp
public void notify()
```

### <a name="examples---notify"></a>例 - notify

次の例では、オブジェクトをロックしてから解放します。

```xpp
public void doWork() 
{ 
    // Perform some actions. 
    this.setTimeOut(identifierstr(workerFunction), 0); 
    this.wait(); // Lock and wait for notify to be called. 
} 
public void workerFunction() 
{ 
    // Perform some actions. 
    // Work is done; unlock the doWork method. 
    this.notify(); 
}
```

## <a name="method-notifyall"></a>メソッド notifyAll

このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。

```xpp
public void notifyAll()
```

### <a name="remarks---notifyall"></a>備考 - notifyAll 

このメソッドの現在の実装では、notify メソッドと notifyAll メソッドの呼び出しに違いはありません。 フォームは、ユーザーがフォームを閉じるまたは「適用」ボタンを押す際に、notifyAll メソッドを自動で呼び出します。

### <a name="examples---notifyall"></a>例 - notifyAll

次の例では、notifyAll メソッドの使用方法を示しています。

```xpp
public void doWork() 
{ 
      //Do some work. 
      this.setTimeOut(identifierstr(workerFunction), 0); 
      this.wait(); // block and wait for notify. 
} 
public void workerFunction() 
{ 
// Do some work. 
//... 
// Work is done. Notify an unblock. 
this.notify(); 
} 
```

