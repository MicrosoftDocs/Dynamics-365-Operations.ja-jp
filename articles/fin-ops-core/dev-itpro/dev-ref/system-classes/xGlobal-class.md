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
# <a name="class-xglobal"></a><span data-ttu-id="c5d2c-103">クラス xGlobal</span><span class="sxs-lookup"><span data-stu-id="c5d2c-103">Class xGlobal</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xGlobal extends Object
```

## <a name="remarks"></a><span data-ttu-id="c5d2c-104">備考</span><span class="sxs-lookup"><span data-stu-id="c5d2c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c5d2c-105">例</span><span class="sxs-lookup"><span data-stu-id="c5d2c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c5d2c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c5d2c-106">Methods</span></span>

| <span data-ttu-id="c5d2c-107">方法</span><span class="sxs-lookup"><span data-stu-id="c5d2c-107">Method</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="c5d2c-108">説明</span><span class="sxs-lookup"><span data-stu-id="c5d2c-108">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="c5d2c-109">::public static ClientType clientKind()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-109">::public static ClientType clientKind()</span></span>                                                                                                                                                                                                                                                                                                                                                            |                                                    |
| <span data-ttu-id="c5d2c-110">::public static SelectableDataArea company(TableId tableid, \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="c5d2c-110">::public static SelectableDataArea company(TableId tableid, \[SelectableDataArea company\])</span></span>                                                                                                                                                                                                                                                                                                        |                                                    |
| <span data-ttu-id="c5d2c-111">::public static str computerName()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-111">::public static str computerName()</span></span>                                                                                                                                                                                                                                                                                                                                                                 |                                                    |
| <span data-ttu-id="c5d2c-112">::public static boolean hasClient()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-112">::public static boolean hasClient()</span></span>                                                                                                                                                                                                                                                                                                                                                                |                                                    |
| <span data-ttu-id="c5d2c-113">::public static int infologLine()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-113">::public static int infologLine()</span></span>                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="c5d2c-114">情報ログ バッファの明細行の数を返します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-114">Returns the number of lines in the Infolog buffer.</span></span> |
| <span data-ttu-id="c5d2c-115">::public static boolean isAOS()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-115">::public static boolean isAOS()</span></span>                                                                                                                                                                                                                                                                                                                                                                    |                                                    |
| <span data-ttu-id="c5d2c-116">::public static boolean isGuest()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-116">::public static boolean isGuest()</span></span>                                                                                                                                                                                                                                                                                                                                                                  |                                                    |
| <span data-ttu-id="c5d2c-117">::public static boolean isUserLanguageRTL()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-117">::public static boolean isUserLanguageRTL()</span></span>                                                                                                                                                                                                                                                                                                                                                        |                                                    |
| <span data-ttu-id="c5d2c-118">::public static container languageList()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-118">::public static container languageList()</span></span>                                                                                                                                                                                                                                                                                                                                                           |                                                    |
| <span data-ttu-id="c5d2c-119">::public static str machineTzDisplayName()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-119">::public static str machineTzDisplayName()</span></span>                                                                                                                                                                                                                                                                                                                                                         |                                                    |
| <span data-ttu-id="c5d2c-120">::public static boolean isObjectOnServer(AnyType object)</span><span class="sxs-lookup"><span data-stu-id="c5d2c-120">::public static boolean isObjectOnServer(AnyType object)</span></span>                                                                                                                                                                                                                                                                                                                                           |                                                    |
| <span data-ttu-id="c5d2c-121">::public static int randomPositiveInt32()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-121">::public static int randomPositiveInt32()</span></span>                                                                                                                                                                                                                                                                                                                                                          |                                                    |
| <span data-ttu-id="c5d2c-122">::public static boolean terminalServer()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-122">::public static boolean terminalServer()</span></span>                                                                                                                                                                                                                                                                                                                                                           |                                                    |
| <span data-ttu-id="c5d2c-123">::public static WorkerSessionType workerSessionType()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-123">::public static WorkerSessionType workerSessionType()</span></span>                                                                                                                                                                                                                                                                                                                                              |                                                    |
| <span data-ttu-id="c5d2c-124">::public static System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[int callbackClassId\], \[str callbackStaticMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\])</span><span class="sxs-lookup"><span data-stu-id="c5d2c-124">::public static System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[int callbackClassId\], \[str callbackStaticMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\])</span></span> |                                                    |
| <span data-ttu-id="c5d2c-125">::public static System.Threading.Tasks.Task runAsyncWithObjectCallback(int runAsClassId, str runAsStaticMethodName, container parms, Object callbackObject, str callbackStaticMethodName)</span><span class="sxs-lookup"><span data-stu-id="c5d2c-125">::public static System.Threading.Tasks.Task runAsyncWithObjectCallback(int runAsClassId, str runAsStaticMethodName, container parms, Object callbackObject, str callbackStaticMethodName)</span></span>                                                                                                                                                                                                          |                                                    |
| <span data-ttu-id="c5d2c-126">::public static void forceFormPreload()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-126">::public static void forceFormPreload()</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="c5d2c-127">フォームのプリロードが直ちに発生するよう強制します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-127">Forces form preloading to occur immediately.</span></span>       |
| <span data-ttu-id="c5d2c-128">private void new()</span><span class="sxs-lookup"><span data-stu-id="c5d2c-128">private void new()</span></span>                                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="c5d2c-129">xGlobal クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-129">Initializes a new instance of the xGlobal class.</span></span>   |

## <a name="method-clientkind"></a><span data-ttu-id="c5d2c-130">メソッド clientKind</span><span class="sxs-lookup"><span data-stu-id="c5d2c-130">Method clientKind</span></span>

```xpp
public static ClientType clientKind()
```

### <a name="return-value---clientkind"></a><span data-ttu-id="c5d2c-131">戻り値 - clientKind</span><span class="sxs-lookup"><span data-stu-id="c5d2c-131">Return Value - clientKind</span></span>

## <a name="method-company"></a><span data-ttu-id="c5d2c-132">メソッド company</span><span class="sxs-lookup"><span data-stu-id="c5d2c-132">Method company</span></span>

```xpp
public static SelectableDataArea company(TableId tableid, [SelectableDataArea company])
```

### <a name="parameters---company"></a><span data-ttu-id="c5d2c-133">パラメーター - company</span><span class="sxs-lookup"><span data-stu-id="c5d2c-133">Parameters - company</span></span>

<span data-ttu-id="c5d2c-134">tableid</span><span class="sxs-lookup"><span data-stu-id="c5d2c-134">tableid</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-135">会社</span><span class="sxs-lookup"><span data-stu-id="c5d2c-135">company</span></span>  

### <a name="return-value---company"></a><span data-ttu-id="c5d2c-136">戻り値 - company</span><span class="sxs-lookup"><span data-stu-id="c5d2c-136">Return Value - company</span></span>

## <a name="method-computername"></a><span data-ttu-id="c5d2c-137">メソッド computerName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-137">Method computerName</span></span>

```xpp
public static str computerName()
```

### <a name="return-value---computername"></a><span data-ttu-id="c5d2c-138">戻り値 - computerName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-138">Return Value - computerName</span></span>

## <a name="method-hasclient"></a><span data-ttu-id="c5d2c-139">メソッド hasClient</span><span class="sxs-lookup"><span data-stu-id="c5d2c-139">Method hasClient</span></span>

```xpp
public static boolean hasClient()
```

### <a name="return-value---hasclient"></a><span data-ttu-id="c5d2c-140">戻り値 - hasClient</span><span class="sxs-lookup"><span data-stu-id="c5d2c-140">Return Value - hasClient</span></span>

## <a name="method-infologline"></a><span data-ttu-id="c5d2c-141">メソッド infologLine</span><span class="sxs-lookup"><span data-stu-id="c5d2c-141">Method infologLine</span></span>

<span data-ttu-id="c5d2c-142">情報ログ バッファの明細行の数を返します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-142">Returns the number of lines in the Infolog buffer.</span></span>

```xpp
public static int infologLine()
```

### <a name="return-value---infologline"></a><span data-ttu-id="c5d2c-143">戻り値 - infologLine</span><span class="sxs-lookup"><span data-stu-id="c5d2c-143">Return Value - infologLine</span></span>

### <a name="remarks---infologline"></a><span data-ttu-id="c5d2c-144">備考 - infologLine</span><span class="sxs-lookup"><span data-stu-id="c5d2c-144">Remarks - infologLine</span></span>

<span data-ttu-id="c5d2c-145">このメソッドは、xInfo.line メソッドと同様の機能を持ちますが、サーバーサイド コードを実行しているときにパフォーマンスが向上し、ネットワークの負荷が軽減されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-145">This method has similar functionality to the xInfo.line method, but it improves performance and lowers network load when you are executing server-side code.</span></span> <span data-ttu-id="c5d2c-146">XInfo.line は、サーバーで実行されると、クライアントを呼び出して、情報ログ バッファ内の行数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-146">When xInfo.line is run on the server, it makes a call to the client to retrieve the number of lines in the Infolog buffer.</span></span> <span data-ttu-id="c5d2c-147">xGlobal::infologLine メソッドは、サーバー側の Infolog バッファの行数を取得するので、クライアントに呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-147">The xGlobal::infologLine method retrieves the line count of the server-side Infolog buffer, so that you do not have to call to the client.</span></span> <span data-ttu-id="c5d2c-148">xGlobal::infologLine メソッドは、クライアント上で呼び出されると、クライアント上の情報ログ バッファから行数を直接返します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-148">When the xGlobal::infologLine method is called on the client, it returns the count directly from the Infolog buffer on the client.</span></span> <span data-ttu-id="c5d2c-149">このメソッドは、例外を処理するサーバー側のコードを記述するときに特に便利です。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-149">This method is especially useful when you are writing server-side code that processes exceptions.</span></span> <span data-ttu-id="c5d2c-150">情報ログの行数は、通常、try/catch ブロックが入力される前に保存されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-150">The number of lines in the Infolog is typically stored before a try/catch block is entered.</span></span> <span data-ttu-id="c5d2c-151">例外が発生すると、以前に保存した明細行の数は、try ブロック内のコード中にログ記録されたメッセージを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-151">If an exception occurs, the number of lines that were previously stored is used to determine which messages were logged during the code in the try block.</span></span> <span data-ttu-id="c5d2c-152">例外が発生しない場合、保存されている情報ログ バッファ ライン数が多くの場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-152">If no exceptions occur, the stored Infolog buffer line count is often unused.</span></span> <span data-ttu-id="c5d2c-153">xInfo.line メソッドの代わりに xGlobal::infologLine メソッドを使用して情報ログ行を取得することで、クライアントへのラウンド トリップを回避できます。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-153">By using the xGlobal::infologLine method instead of the xInfo.line method to retrieve the Infolog lines, you avoid a round trip to the client.</span></span>

## <a name="method-isaos"></a><span data-ttu-id="c5d2c-154">メソッド isAOS</span><span class="sxs-lookup"><span data-stu-id="c5d2c-154">Method isAOS</span></span>

```xpp
public static boolean isAOS()
```

### <a name="return-value---isaos"></a><span data-ttu-id="c5d2c-155">戻り値 - isAOS</span><span class="sxs-lookup"><span data-stu-id="c5d2c-155">Return Value - isAOS</span></span>

## <a name="method-isguest"></a><span data-ttu-id="c5d2c-156">メソッド isGuest</span><span class="sxs-lookup"><span data-stu-id="c5d2c-156">Method isGuest</span></span>

```xpp
public static boolean isGuest()
```

### <a name="return-value---isguest"></a><span data-ttu-id="c5d2c-157">戻り値 - isGuest</span><span class="sxs-lookup"><span data-stu-id="c5d2c-157">Return Value - isGuest</span></span>

## <a name="method-isuserlanguagertl"></a><span data-ttu-id="c5d2c-158">メソッド isUserLanguageRTL</span><span class="sxs-lookup"><span data-stu-id="c5d2c-158">Method isUserLanguageRTL</span></span>

```xpp
public static boolean isUserLanguageRTL()
```

### <a name="return-value---isuserlanguagertl"></a><span data-ttu-id="c5d2c-159">戻り値 - isUserLanguageRTL</span><span class="sxs-lookup"><span data-stu-id="c5d2c-159">Return Value - isUserLanguageRTL</span></span>

## <a name="method-languagelist"></a><span data-ttu-id="c5d2c-160">メソッド languageList</span><span class="sxs-lookup"><span data-stu-id="c5d2c-160">Method languageList</span></span>

```xpp
public static container languageList()
```

### <a name="return-value---languagelist"></a><span data-ttu-id="c5d2c-161">戻り値 - languageList</span><span class="sxs-lookup"><span data-stu-id="c5d2c-161">Return Value - languageList</span></span>

## <a name="method-machinetzdisplayname"></a><span data-ttu-id="c5d2c-162">メソッド machineTzDisplayName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-162">Method machineTzDisplayName</span></span>

```xpp
public static str machineTzDisplayName()
```

### <a name="return-value---machinetzdisplayname"></a><span data-ttu-id="c5d2c-163">戻り値 - machineTzDisplayName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-163">Return Value - machineTzDisplayName</span></span>

## <a name="method-isobjectonserver"></a><span data-ttu-id="c5d2c-164">メソッド isObjectOnServer</span><span class="sxs-lookup"><span data-stu-id="c5d2c-164">Method isObjectOnServer</span></span>

```xpp
public static boolean isObjectOnServer(AnyType object)
```

### <a name="parameters---isobjectonserver"></a><span data-ttu-id="c5d2c-165">パラメーター - isObjectOnServer</span><span class="sxs-lookup"><span data-stu-id="c5d2c-165">Parameters - isObjectOnServer</span></span>

<span data-ttu-id="c5d2c-166">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c5d2c-166">object</span></span>  

### <a name="return-value---isobjectonserver"></a><span data-ttu-id="c5d2c-167">戻り値 - isObjectOnServer</span><span class="sxs-lookup"><span data-stu-id="c5d2c-167">Return Value - isObjectOnServer</span></span>

## <a name="method-randompositiveint32"></a><span data-ttu-id="c5d2c-168">メソッド randomPositiveInt32</span><span class="sxs-lookup"><span data-stu-id="c5d2c-168">Method randomPositiveInt32</span></span>

```xpp
public static int randomPositiveInt32()
```

### <a name="return-value---randompositiveint32"></a><span data-ttu-id="c5d2c-169">戻り値 - randomPositiveInt32</span><span class="sxs-lookup"><span data-stu-id="c5d2c-169">Return Value - randomPositiveInt32</span></span>

## <a name="method-terminalserver"></a><span data-ttu-id="c5d2c-170">メソッド terminalServer</span><span class="sxs-lookup"><span data-stu-id="c5d2c-170">Method terminalServer</span></span>

```xpp
public static boolean terminalServer()
```

### <a name="return-value---terminalserver"></a><span data-ttu-id="c5d2c-171">戻り値 - terminalServer</span><span class="sxs-lookup"><span data-stu-id="c5d2c-171">Return Value - terminalServer</span></span>

## <a name="method-workersessiontype"></a><span data-ttu-id="c5d2c-172">メソッド workerSessionType</span><span class="sxs-lookup"><span data-stu-id="c5d2c-172">Method workerSessionType</span></span>

```xpp
public static WorkerSessionType workerSessionType()
```

### <a name="return-value---workersessiontype"></a><span data-ttu-id="c5d2c-173">戻り値 - workerSessionType</span><span class="sxs-lookup"><span data-stu-id="c5d2c-173">Return Value - workerSessionType</span></span>

## <a name="method-runasync"></a><span data-ttu-id="c5d2c-174">メソッド runAsync</span><span class="sxs-lookup"><span data-stu-id="c5d2c-174">Method runAsync</span></span>

```xpp
public static System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, [System.Threading.CancellationToken cancellationToken], [int callbackClassId], [str callbackStaticMethodName], [container asyncState], [str userId], [str company], [str language], [str partitionKey], [System.Threading.Tasks.TaskCreationOptions options])
```

### <a name="parameters---runasync"></a><span data-ttu-id="c5d2c-175">パラメーター - runAsync</span><span class="sxs-lookup"><span data-stu-id="c5d2c-175">Parameters - runAsync</span></span>

<span data-ttu-id="c5d2c-176">runAsClassId</span><span class="sxs-lookup"><span data-stu-id="c5d2c-176">runAsClassId</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-177">runAsStaticMethodName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-177">runAsStaticMethodName</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-178">parms</span><span class="sxs-lookup"><span data-stu-id="c5d2c-178">parms</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-179">cancellationToken</span><span class="sxs-lookup"><span data-stu-id="c5d2c-179">cancellationToken</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-180">callbackClassId</span><span class="sxs-lookup"><span data-stu-id="c5d2c-180">callbackClassId</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-181">callbackStaticMethodName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-181">callbackStaticMethodName</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-182">asyncState</span><span class="sxs-lookup"><span data-stu-id="c5d2c-182">asyncState</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-183">userId</span><span class="sxs-lookup"><span data-stu-id="c5d2c-183">userId</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-184">会社</span><span class="sxs-lookup"><span data-stu-id="c5d2c-184">company</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-185">言語</span><span class="sxs-lookup"><span data-stu-id="c5d2c-185">language</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-186">partitionKey</span><span class="sxs-lookup"><span data-stu-id="c5d2c-186">partitionKey</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-187">オプション</span><span class="sxs-lookup"><span data-stu-id="c5d2c-187">options</span></span>  

### <a name="return-value---runasync"></a><span data-ttu-id="c5d2c-188">戻り値 - runAsync</span><span class="sxs-lookup"><span data-stu-id="c5d2c-188">Return Value - runAsync</span></span>

## <a name="method-runasyncwithobjectcallback"></a><span data-ttu-id="c5d2c-189">メソッド runAsyncWithObjectCallback</span><span class="sxs-lookup"><span data-stu-id="c5d2c-189">Method runAsyncWithObjectCallback</span></span>

```xpp
public static System.Threading.Tasks.Task runAsyncWithObjectCallback(int runAsClassId, str runAsStaticMethodName, container parms, Object callbackObject, str callbackStaticMethodName)
```

### <a name="parameters---runasyncwithobjectcallback"></a><span data-ttu-id="c5d2c-190">パラメーター - runAsyncWithObjectCallback</span><span class="sxs-lookup"><span data-stu-id="c5d2c-190">Parameters - runAsyncWithObjectCallback</span></span>

<span data-ttu-id="c5d2c-191">runAsClassId</span><span class="sxs-lookup"><span data-stu-id="c5d2c-191">runAsClassId</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-192">runAsStaticMethodName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-192">runAsStaticMethodName</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-193">parms</span><span class="sxs-lookup"><span data-stu-id="c5d2c-193">parms</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-194">callbackObject</span><span class="sxs-lookup"><span data-stu-id="c5d2c-194">callbackObject</span></span>  

<!-- -->

<span data-ttu-id="c5d2c-195">callbackStaticMethodName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-195">callbackStaticMethodName</span></span>  

### <a name="return-value---runasyncwithobjectcallback"></a><span data-ttu-id="c5d2c-196">戻り値 - runAsyncWithObjectCallback</span><span class="sxs-lookup"><span data-stu-id="c5d2c-196">Return Value - runAsyncWithObjectCallback</span></span>

## <a name="method-forceformpreload"></a><span data-ttu-id="c5d2c-197">メソッド forceFormPreload</span><span class="sxs-lookup"><span data-stu-id="c5d2c-197">Method forceFormPreload</span></span>

<span data-ttu-id="c5d2c-198">フォームのプリロードが直ちに発生するよう強制します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-198">Forces form preloading to occur immediately.</span></span>

```xpp
public static void forceFormPreload()
```

### <a name="remarks---forceformpreload"></a><span data-ttu-id="c5d2c-199">備考 - forceFormPreload</span><span class="sxs-lookup"><span data-stu-id="c5d2c-199">Remarks - forceFormPreload</span></span>

<span data-ttu-id="c5d2c-200">通常、クライアントがアイドルになったときのみ、プリロードが発生します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-200">Normally, preloading occurs only when the client has gone idle.</span></span> <span data-ttu-id="c5d2c-201">実行時間の長い X++ の実行が発生しているシナリオでは、このメソッドを強制的にフォームのプリロードを行うために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-201">In scenarios where long-running X++ execution is occurring, this method can be used to force form preloading.</span></span>

## <a name="method-new"></a><span data-ttu-id="c5d2c-202">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c5d2c-202">Method new</span></span>

<span data-ttu-id="c5d2c-203">xGlobal クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c5d2c-203">Initializes a new instance of the xGlobal class.</span></span>

```xpp
private void new()
```

