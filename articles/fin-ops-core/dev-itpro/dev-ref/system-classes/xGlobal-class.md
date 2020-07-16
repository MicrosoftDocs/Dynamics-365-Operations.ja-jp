---
title: xGlobal クラス
description: このトピックでは、xGlobal クラスについて説明します。
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
ms.openlocfilehash: a0e50f9d643d7b64ef9939ed94562340d4790228
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502680"
---
# <a name="class-xglobal"></a>クラス xGlobal

[!include [banner](../../includes/banner.md)]

```xpp
class xGlobal extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                                                                                                                                                                                                             | 説明                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| ::public static ClientType clientKind()                                                                                                                                                                                                                                                                                                                                                            |                                                    |
| ::public static SelectableDataArea company(TableId tableid, \[SelectableDataArea company\])                                                                                                                                                                                                                                                                                                        |                                                    |
| ::public static str computerName()                                                                                                                                                                                                                                                                                                                                                                 |                                                    |
| ::public static boolean hasClient()                                                                                                                                                                                                                                                                                                                                                                |                                                    |
| ::public static int infologLine()                                                                                                                                                                                                                                                                                                                                                                  | 情報ログ バッファの明細行の数を返します。 |
| ::public static boolean isAOS()                                                                                                                                                                                                                                                                                                                                                                    |                                                    |
| ::public static boolean isGuest()                                                                                                                                                                                                                                                                                                                                                                  |                                                    |
| ::public static boolean isUserLanguageRTL()                                                                                                                                                                                                                                                                                                                                                        |                                                    |
| ::public static container languageList()                                                                                                                                                                                                                                                                                                                                                           |                                                    |
| ::public static str machineTzDisplayName()                                                                                                                                                                                                                                                                                                                                                         |                                                    |
| ::public static boolean isObjectOnServer(AnyType object)                                                                                                                                                                                                                                                                                                                                           |                                                    |
| ::public static int randomPositiveInt32()                                                                                                                                                                                                                                                                                                                                                          |                                                    |
| ::public static boolean terminalServer()                                                                                                                                                                                                                                                                                                                                                           |                                                    |
| ::public static WorkerSessionType workerSessionType()                                                                                                                                                                                                                                                                                                                                              |                                                    |
| ::public static System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[int callbackClassId\], \[str callbackStaticMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\]) |                                                    |
| ::public static System.Threading.Tasks.Task runAsyncWithObjectCallback(int runAsClassId, str runAsStaticMethodName, container parms, Object callbackObject, str callbackStaticMethodName)                                                                                                                                                                                                          |                                                    |
| ::public static void forceFormPreload()                                                                                                                                                                                                                                                                                                                                                            | フォームのプリロードが直ちに発生するよう強制します。       |
| private void new()                                                                                                                                                                                                                                                                                                                                                                                 | xGlobal クラスの新しいインスタンスを初期化します。   |

## <a name="method-clientkind"></a>メソッド clientKind

```xpp
public static ClientType clientKind()
```

### <a name="return-value---clientkind"></a>戻り値 - clientKind

## <a name="method-company"></a>メソッド company

```xpp
public static SelectableDataArea company(TableId tableid, [SelectableDataArea company])
```

### <a name="parameters---company"></a>パラメーター - company

tableid  

<!-- -->

会社  

### <a name="return-value---company"></a>戻り値 - company

## <a name="method-computername"></a>メソッド computerName

```xpp
public static str computerName()
```

### <a name="return-value---computername"></a>戻り値 - computerName

## <a name="method-hasclient"></a>メソッド hasClient

```xpp
public static boolean hasClient()
```

### <a name="return-value---hasclient"></a>戻り値 - hasClient

## <a name="method-infologline"></a>メソッド infologLine

情報ログ バッファの明細行の数を返します。

```xpp
public static int infologLine()
```

### <a name="return-value---infologline"></a>戻り値 - infologLine

### <a name="remarks---infologline"></a>備考 - infologLine

このメソッドは、xInfo.line メソッドと同様の機能を持ちますが、サーバーサイド コードを実行しているときにパフォーマンスが向上し、ネットワークの負荷が軽減されます。 XInfo.line は、サーバーで実行されると、クライアントを呼び出して、情報ログ バッファ内の行数を取得します。 xGlobal::infologLine メソッドは、サーバー側の Infolog バッファの行数を取得するので、クライアントに呼び出す必要はありません。 xGlobal::infologLine メソッドは、クライアント上で呼び出されると、クライアント上の情報ログ バッファから行数を直接返します。 このメソッドは、例外を処理するサーバー側のコードを記述するときに特に便利です。 情報ログの行数は、通常、try/catch ブロックが入力される前に保存されます。 例外が発生すると、以前に保存した明細行の数は、try ブロック内のコード中にログ記録されたメッセージを決定するために使用されます。 例外が発生しない場合、保存されている情報ログ バッファ ライン数が多くの場合に使用されます。 xInfo.line メソッドの代わりに xGlobal::infologLine メソッドを使用して情報ログ行を取得することで、クライアントへのラウンド トリップを回避できます。

## <a name="method-isaos"></a>メソッド isAOS

```xpp
public static boolean isAOS()
```

### <a name="return-value---isaos"></a>戻り値 - isAOS

## <a name="method-isguest"></a>メソッド isGuest

```xpp
public static boolean isGuest()
```

### <a name="return-value---isguest"></a>戻り値 - isGuest

## <a name="method-isuserlanguagertl"></a>メソッド isUserLanguageRTL

```xpp
public static boolean isUserLanguageRTL()
```

### <a name="return-value---isuserlanguagertl"></a>戻り値 - isUserLanguageRTL

## <a name="method-languagelist"></a>メソッド languageList

```xpp
public static container languageList()
```

### <a name="return-value---languagelist"></a>戻り値 - languageList

## <a name="method-machinetzdisplayname"></a>メソッド machineTzDisplayName

```xpp
public static str machineTzDisplayName()
```

### <a name="return-value---machinetzdisplayname"></a>戻り値 - machineTzDisplayName

## <a name="method-isobjectonserver"></a>メソッド isObjectOnServer

```xpp
public static boolean isObjectOnServer(AnyType object)
```

### <a name="parameters---isobjectonserver"></a>パラメーター - isObjectOnServer

オブジェクト  

### <a name="return-value---isobjectonserver"></a>戻り値 - isObjectOnServer

## <a name="method-randompositiveint32"></a>メソッド randomPositiveInt32

```xpp
public static int randomPositiveInt32()
```

### <a name="return-value---randompositiveint32"></a>戻り値 - randomPositiveInt32

## <a name="method-terminalserver"></a>メソッド terminalServer

```xpp
public static boolean terminalServer()
```

### <a name="return-value---terminalserver"></a>戻り値 - terminalServer

## <a name="method-workersessiontype"></a>メソッド workerSessionType

```xpp
public static WorkerSessionType workerSessionType()
```

### <a name="return-value---workersessiontype"></a>戻り値 - workerSessionType

## <a name="method-runasync"></a>メソッド runAsync

```xpp
public static System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, [System.Threading.CancellationToken cancellationToken], [int callbackClassId], [str callbackStaticMethodName], [container asyncState], [str userId], [str company], [str language], [str partitionKey], [System.Threading.Tasks.TaskCreationOptions options])
```

### <a name="parameters---runasync"></a>パラメーター - runAsync

runAsClassId  

<!-- -->

runAsStaticMethodName  

<!-- -->

parms  

<!-- -->

cancellationToken  

<!-- -->

callbackClassId  

<!-- -->

callbackStaticMethodName  

<!-- -->

asyncState  

<!-- -->

userId  

<!-- -->

会社  

<!-- -->

言語  

<!-- -->

partitionKey  

<!-- -->

オプション  

### <a name="return-value---runasync"></a>戻り値 - runAsync

## <a name="method-runasyncwithobjectcallback"></a>メソッド runAsyncWithObjectCallback

```xpp
public static System.Threading.Tasks.Task runAsyncWithObjectCallback(int runAsClassId, str runAsStaticMethodName, container parms, Object callbackObject, str callbackStaticMethodName)
```

### <a name="parameters---runasyncwithobjectcallback"></a>パラメーター - runAsyncWithObjectCallback

runAsClassId  

<!-- -->

runAsStaticMethodName  

<!-- -->

parms  

<!-- -->

callbackObject  

<!-- -->

callbackStaticMethodName  

### <a name="return-value---runasyncwithobjectcallback"></a>戻り値 - runAsyncWithObjectCallback

## <a name="method-forceformpreload"></a>メソッド forceFormPreload

フォームのプリロードが直ちに発生するよう強制します。

```xpp
public static void forceFormPreload()
```

### <a name="remarks---forceformpreload"></a>備考 - forceFormPreload

通常、クライアントがアイドルになったときのみ、プリロードが発生します。 実行時間の長い X++ の実行が発生しているシナリオでは、このメソッドを強制的にフォームのプリロードを行うために使用できます。

## <a name="method-new"></a>メソッド new

xGlobal クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

