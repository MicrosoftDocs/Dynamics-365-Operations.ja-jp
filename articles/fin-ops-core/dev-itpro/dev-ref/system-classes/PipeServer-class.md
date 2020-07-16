---
title: PipeServer クラス
description: このトピックでは、PipeServer クラスについて説明します。
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
ms.openlocfilehash: 4da417f032acb263613b4a650bd2e76e674a5f08
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502876"
---
# <a name="class-pipeserver"></a><span data-ttu-id="399c0-103">クラス PipeServer</span><span class="sxs-lookup"><span data-stu-id="399c0-103">Class PipeServer</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PipeServer extends Object
```

<span data-ttu-id="399c0-104">PipeServer クラスでは、名前付きパイプのサーバー側がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="399c0-104">The PipeServer class supports the server side of a named pipe connection.</span></span>

## <a name="remarks"></a><span data-ttu-id="399c0-105">備考</span><span class="sxs-lookup"><span data-stu-id="399c0-105">Remarks</span></span>

<span data-ttu-id="399c0-106">PipeServer オブジェクトが PipeServer.new メソッドを使用して作成されたときに、名前付きパイプが作成されます。</span><span class="sxs-lookup"><span data-stu-id="399c0-106">A named pipe is created when a PipeServer object is created by using the PipeServer.new method.</span></span> <span data-ttu-id="399c0-107">作成されるパイプは、読み取りアクセス権を保有し、メッセージ モードの状態にあります。</span><span class="sxs-lookup"><span data-stu-id="399c0-107">The pipe that is created has read access and is in message mode.</span></span> <span data-ttu-id="399c0-108">パイプの名前には自動的に接頭語 \\\\.\\pipe\\Dynamics が付けられます。</span><span class="sxs-lookup"><span data-stu-id="399c0-108">The name of the pipe is automatically prefixed with \\\\.\\pipe\\Dynamics.</span></span> <span data-ttu-id="399c0-109">現在のセッション SID は名前の接尾辞になります。</span><span class="sxs-lookup"><span data-stu-id="399c0-109">The current session SID is postfixed to the name.</span></span> <span data-ttu-id="399c0-110">サーバーのパイプ接続に提供されるサポートは、以下のセキュリティ上の理由により制限されています。</span><span class="sxs-lookup"><span data-stu-id="399c0-110">The support that is provided for pipe connections on the server is restricted for the following security reasons:</span></span>

-   <span data-ttu-id="399c0-111">パイプは、セッションが作成されたコンピュータ上の現在のログオン セッションのみに対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="399c0-111">The pipe is supported only for the current logon session on the computer that the session was created on.</span></span>
-   <span data-ttu-id="399c0-112">パイプを作成するユーザーは、そのパイプと通信できる唯一のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="399c0-112">The user who creates the pipe is the only person who can communicate with that pipe.</span></span>

## <a name="examples"></a><span data-ttu-id="399c0-113">例</span><span class="sxs-lookup"><span data-stu-id="399c0-113">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="399c0-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="399c0-114">Methods</span></span>

| <span data-ttu-id="399c0-115">方法</span><span class="sxs-lookup"><span data-stu-id="399c0-115">Method</span></span>                                              | <span data-ttu-id="399c0-116">説明</span><span class="sxs-lookup"><span data-stu-id="399c0-116">Description</span></span>                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="399c0-117">public boolean blockingMode(\[boolean block\])</span><span class="sxs-lookup"><span data-stu-id="399c0-117">public boolean blockingMode(\[boolean block\])</span></span>      |                                                                              |
| <span data-ttu-id="399c0-118">public boolean connect()</span><span class="sxs-lookup"><span data-stu-id="399c0-118">public boolean connect()</span></span>                            | <span data-ttu-id="399c0-119">クライアントが名前付きパイプに接続するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="399c0-119">Waits for a client to connect to the named pipe.</span></span>                             |
| <span data-ttu-id="399c0-120">public boolean disconnect()</span><span class="sxs-lookup"><span data-stu-id="399c0-120">public boolean disconnect()</span></span>                         | <span data-ttu-id="399c0-121">名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。</span><span class="sxs-lookup"><span data-stu-id="399c0-121">Disconnects the server end of the named pipe instance from a client process.</span></span> |
| <span data-ttu-id="399c0-122">public int errorCode()</span><span class="sxs-lookup"><span data-stu-id="399c0-122">public int errorCode()</span></span>                              |                                                                              |
| <span data-ttu-id="399c0-123">public str read()</span><span class="sxs-lookup"><span data-stu-id="399c0-123">public str read()</span></span>                                   | <span data-ttu-id="399c0-124">パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="399c0-124">Reads data from the named pipe, as written by a pipe client.</span></span>                 |
| <span data-ttu-id="399c0-125">public void new(str pipename, \[boolean blocking\])</span><span class="sxs-lookup"><span data-stu-id="399c0-125">public void new(str pipename, \[boolean blocking\])</span></span> | <span data-ttu-id="399c0-126">PipeServer クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="399c0-126">Creates a new instance of the PipeServer class.</span></span>                              |

## <a name="method-blockingmode"></a><span data-ttu-id="399c0-127">メソッド blockingMode</span><span class="sxs-lookup"><span data-stu-id="399c0-127">Method blockingMode</span></span>

```xpp
public boolean blockingMode([boolean block])
```

### <a name="parameters---blockingmode"></a><span data-ttu-id="399c0-128">パラメーター - blockingMode</span><span class="sxs-lookup"><span data-stu-id="399c0-128">Parameters - blockingMode</span></span>

<span data-ttu-id="399c0-129">block</span><span class="sxs-lookup"><span data-stu-id="399c0-129">block</span></span>  

### <a name="return-value---blockingmode"></a><span data-ttu-id="399c0-130">戻り値 - blockingMode</span><span class="sxs-lookup"><span data-stu-id="399c0-130">Return Value - blockingMode</span></span>

## <a name="method-connect"></a><span data-ttu-id="399c0-131">メソッド connect</span><span class="sxs-lookup"><span data-stu-id="399c0-131">Method connect</span></span>

<span data-ttu-id="399c0-132">クライアントが名前付きパイプに接続するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="399c0-132">Waits for a client to connect to the named pipe.</span></span>

```xpp
public boolean connect()
```

### <a name="return-value---connect"></a><span data-ttu-id="399c0-133">戻り値 - connect</span><span class="sxs-lookup"><span data-stu-id="399c0-133">Return Value - connect</span></span>

<span data-ttu-id="399c0-134">メソッドが成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="399c0-134">true if the method succeeds; otherwise, false.</span></span>

### <a name="remarks---connect"></a><span data-ttu-id="399c0-135">備考 - connect</span><span class="sxs-lookup"><span data-stu-id="399c0-135">Remarks - connect</span></span>

<span data-ttu-id="399c0-136">クライアントが接続するのを待機している場合は、現在のスレッドをブロックしない場合、PipeServer.connect メソッドを使用しないようにし、代わりに PipeServer.read メソッドを使用してポーリングします。</span><span class="sxs-lookup"><span data-stu-id="399c0-136">If you do not want to block the current thread if it is waiting for a client to connect, avoid using the PipeServer.connect method, and poll by using the PipeServer.read method instead.</span></span>

## <a name="method-disconnect"></a><span data-ttu-id="399c0-137">メソッド disconnect</span><span class="sxs-lookup"><span data-stu-id="399c0-137">Method disconnect</span></span>

<span data-ttu-id="399c0-138">名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。</span><span class="sxs-lookup"><span data-stu-id="399c0-138">Disconnects the server end of the named pipe instance from a client process.</span></span>

```xpp
public boolean disconnect()
```

### <a name="return-value---disconnect"></a><span data-ttu-id="399c0-139">戻り値 - disconnect</span><span class="sxs-lookup"><span data-stu-id="399c0-139">Return Value - disconnect</span></span>

<span data-ttu-id="399c0-140">メソッドが成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="399c0-140">true if the method succeeds; otherwise, false.</span></span>

## <a name="method-errorcode"></a><span data-ttu-id="399c0-141">メソッド errorCode</span><span class="sxs-lookup"><span data-stu-id="399c0-141">Method errorCode</span></span>

```xpp
public int errorCode()
```

### <a name="return-value---errorcode"></a><span data-ttu-id="399c0-142">戻り値 - errorCode</span><span class="sxs-lookup"><span data-stu-id="399c0-142">Return Value - errorCode</span></span>

## <a name="method-read"></a><span data-ttu-id="399c0-143">メソッド read</span><span class="sxs-lookup"><span data-stu-id="399c0-143">Method read</span></span>

<span data-ttu-id="399c0-144">パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="399c0-144">Reads data from the named pipe, as written by a pipe client.</span></span>

```xpp
public str read()
```

### <a name="return-value---read"></a><span data-ttu-id="399c0-145">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="399c0-145">Return Value - read</span></span>

<span data-ttu-id="399c0-146">データが読み取られた場合に、パイプから読み取られるデータ。</span><span class="sxs-lookup"><span data-stu-id="399c0-146">The data that is read from the pipe, if any data is read.</span></span>

### <a name="remarks---read"></a><span data-ttu-id="399c0-147">備考 - read</span><span class="sxs-lookup"><span data-stu-id="399c0-147">Remarks - read</span></span>

<span data-ttu-id="399c0-148">クライアントが名前付きパイプに接続されていないために、このメソッドが呼び出されたときにデータを使用できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="399c0-148">Data might not be available when this method is called, perhaps because no client has connected to the named pipe.</span></span> <span data-ttu-id="399c0-149">クライアントへの接続を待機する場合は、接続方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="399c0-149">If you want to wait for a client to connect, use the connect method.</span></span> <span data-ttu-id="399c0-150">ただし、クライアントの接続を待機している現在のスレッドをブロックしない場合、読み取りメソッドを使用してポーリングします。</span><span class="sxs-lookup"><span data-stu-id="399c0-150">However, if you do not want to block the current thread that is waiting for a client to connect, poll by using the read method.</span></span>

## <a name="method-new"></a><span data-ttu-id="399c0-151">メソッド new</span><span class="sxs-lookup"><span data-stu-id="399c0-151">Method new</span></span>

<span data-ttu-id="399c0-152">PipeServer クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="399c0-152">Creates a new instance of the PipeServer class.</span></span>

```xpp
public void new(str pipename, [boolean blocking])
```

### <a name="parameters---new"></a><span data-ttu-id="399c0-153">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="399c0-153">Parameters - new</span></span>

<span data-ttu-id="399c0-154">pipename</span><span class="sxs-lookup"><span data-stu-id="399c0-154">pipename</span></span>  
<span data-ttu-id="399c0-155">ブロック動作を使用するかどうかを示すブール値フラグ。</span><span class="sxs-lookup"><span data-stu-id="399c0-155">A Boolean flag that indicates whether blocking behavior should be used.</span></span> <span data-ttu-id="399c0-156">非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="399c0-156">Non-blocking mode is supported for compatibility with Microsoft LAN Manager version 2.0 and should not be used to achieve asynchronous I/O with named pipes.</span></span> <span data-ttu-id="399c0-157">代わりに、ポーリング技術を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="399c0-157">Instead, a polling technique should be used.</span></span> <span data-ttu-id="399c0-158">読み取りメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="399c0-158">See the read method.</span></span>

<!-- -->

<span data-ttu-id="399c0-159">ブロック</span><span class="sxs-lookup"><span data-stu-id="399c0-159">blocking</span></span>  
<span data-ttu-id="399c0-160">ブロック動作を使用するかどうかを示すブール値フラグ。</span><span class="sxs-lookup"><span data-stu-id="399c0-160">A Boolean flag that indicates whether blocking behavior should be used.</span></span> <span data-ttu-id="399c0-161">非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="399c0-161">Non-blocking mode is supported for compatibility with Microsoft LAN Manager version 2.0 and should not be used to achieve asynchronous I/O with named pipes.</span></span> <span data-ttu-id="399c0-162">代わりに、ポーリング技術を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="399c0-162">Instead, a polling technique should be used.</span></span> <span data-ttu-id="399c0-163">読み取りメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="399c0-163">See the read method.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="399c0-164">備考 - new</span><span class="sxs-lookup"><span data-stu-id="399c0-164">Remarks - new</span></span>

<span data-ttu-id="399c0-165">いくつかの制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="399c0-165">Some restrictions apply.</span></span> <span data-ttu-id="399c0-166">PipeServer クラスの一般的な説明の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="399c0-166">See the example in the general description of the PipeServer class.</span></span>

