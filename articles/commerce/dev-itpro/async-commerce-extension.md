---
title: ビジネス ロジックで非同期コマース (CRT) API を作成する
description: このトピックでは、非同期で実行される コマース (CRT) アプリケーション プログラミング インターフェイス (API) (つまり、要求) の作成方法について説明します。
author: mugunthanm
ms.date: 02/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: fc696f835f515b7998c518d8687a284bd292769e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791227"
---
# <a name="create-asynchronous-commerce-crt-apis-in-your-business-logic"></a><span data-ttu-id="62db9-103">ビジネス ロジックで非同期コマース (CRT) API を作成する</span><span class="sxs-lookup"><span data-stu-id="62db9-103">Create asynchronous Commerce (CRT) APIs in your business logic</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="62db9-104">このトピックは、Microsoft Dynamics 365 Commerce バージョン 10.0.10 およびそれ以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="62db9-104">This topic applies to Microsoft Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="62db9-105">このトピックでは、新しい非同期フレームワークを使用して Commerce Runtime (CRT) 用の新しいビジネス ロジック (アプリケーション プログラミング インターフェイス、または API) を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="62db9-105">This topic explains how to create new business logic (application programming interfaces, or APIs) for the Commerce Runtime (CRT) by using the new asynchronous framework.</span></span> <span data-ttu-id="62db9-106">コマース API フレームワークでは、拡張機能および標準のコマース ハンドラーの非同期プログラミング モデルがサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="62db9-106">The Commerce API framework now supports an asynchronous programming model for extensions and out-of-box Commerce handlers.</span></span>   

<span data-ttu-id="62db9-107">このフレームワーク拡張機能が追加される前は、要求が同期的にのみ実行できました。</span><span class="sxs-lookup"><span data-stu-id="62db9-107">Before this framework enhancement was added, requests could be run only synchronously.</span></span> <span data-ttu-id="62db9-108">入力/出力 (I/O) 操作、データベース クエリ、またはネットワーク要求などの長い操作により、実行スレッドがブロックされました。</span><span class="sxs-lookup"><span data-stu-id="62db9-108">Long operations, like input/output (I/O) operations, database queries, or network requests, blocked the execution thread.</span></span> <span data-ttu-id="62db9-109">非同期モデルのサポートが Commerce Runtime (CRT) に追加されたので、これらの操作の非同期バージョンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="62db9-109">Now that support for the asynchronous model has been added to the Commerce runtime (CRT), you can use asynchronous versions of these operations.</span></span> <span data-ttu-id="62db9-110">非同期要求は、実行スレッドをブロック解除します。</span><span class="sxs-lookup"><span data-stu-id="62db9-110">Asynchronous requests unblock the execution thread.</span></span>   

<span data-ttu-id="62db9-111">コマース API フレームワークでは、拡張 CRT 要求ハンドラーの **非同期** および **待機** キーワードでサポートされる、**タスク** および **タスク\<T\>** クラスがサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="62db9-111">The Commerce API framework now supports the **Task** and **Task\<T\>** classes that are supported by the **async** and **await** keywords for the extension CRT request handlers.</span></span> <span data-ttu-id="62db9-112">すべての新しい拡張 API に対して非同期のコマース API フレームワークを使用し、拡張機能には標準の非同期コマース API を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62db9-112">You should use the asynchronous Commerce API framework for all new extension APIs and the out-of-box asynchronous Commerce API in extensions.</span></span>

## <a name="async-classesinterface-added-in-the-commerce-api-framework"></a><span data-ttu-id="62db9-113">コマース API フレームワークに追加された非同期クラス/インターフェイス:</span><span class="sxs-lookup"><span data-stu-id="62db9-113">Async classes/interface added in the Commerce API framework:</span></span>


<span data-ttu-id="62db9-114">次の非同期クラスおよびインターフェイスが、コマース API フレームワークに追加されました。</span><span class="sxs-lookup"><span data-stu-id="62db9-114">The following asynchronous classes and interfaces were added in the Commerce API framework.</span></span>

| <span data-ttu-id="62db9-115">クラス/インターフェイス</span><span class="sxs-lookup"><span data-stu-id="62db9-115">Class/Interface</span></span>                     | <span data-ttu-id="62db9-116">説明</span><span class="sxs-lookup"><span data-stu-id="62db9-116">Description</span></span> |
|---------------------------|-------------|
| <span data-ttu-id="62db9-117">SingleAsyncRequestHandler</span><span class="sxs-lookup"><span data-stu-id="62db9-117">SingleAsyncRequestHandler</span></span> | <span data-ttu-id="62db9-118">1 つの要求のみをサポートする非同期ハンドラーの基本クラス。</span><span class="sxs-lookup"><span data-stu-id="62db9-118">The base class for asynchronous handlers that support only one request.</span></span> |
| <span data-ttu-id="62db9-119">IRequestHandlerAsync</span><span class="sxs-lookup"><span data-stu-id="62db9-119">IRequestHandlerAsync</span></span>      | <span data-ttu-id="62db9-120">非同期要求ハンドラーのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="62db9-120">The interface for the asynchronous request handler.</span></span> |
| <span data-ttu-id="62db9-121">IRequestTriggerAsync</span><span class="sxs-lookup"><span data-stu-id="62db9-121">IRequestTriggerAsync</span></span>      | <span data-ttu-id="62db9-122">要求トリガーのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="62db9-122">The interface for the request trigger.</span></span> |
| <span data-ttu-id="62db9-123">CommerceControllerAsync</span><span class="sxs-lookup"><span data-stu-id="62db9-123">CommerceControllerAsync</span></span>   | <span data-ttu-id="62db9-124">非同期拡張機能 Retail サーバー コントローラー クラスの基本クラス。</span><span class="sxs-lookup"><span data-stu-id="62db9-124">The base class for asynchronous extension Retail server controller class.</span></span> |
| <span data-ttu-id="62db9-125">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-125">DatabaseContext</span></span>           | <span data-ttu-id="62db9-126">非同期データベース実行メソッドの基本クラス。</span><span class="sxs-lookup"><span data-stu-id="62db9-126">The base class for asynchronous database execution methods.</span></span> |



<span data-ttu-id="62db9-127">次の非同期メソッドが、コマース API フレームワークに追加されました。</span><span class="sxs-lookup"><span data-stu-id="62db9-127">The following asynchronous methods were added in the Commerce API framework.</span></span>

| <span data-ttu-id="62db9-128">クラス/インターフェイス</span><span class="sxs-lookup"><span data-stu-id="62db9-128">Class/Interface</span></span>           | <span data-ttu-id="62db9-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="62db9-129">Method</span></span>                                              | <span data-ttu-id="62db9-130">説明</span><span class="sxs-lookup"><span data-stu-id="62db9-130">Description</span></span> |
|---------------------------|-----------------------------------------------------|-------------|
| <span data-ttu-id="62db9-131">SingleAsyncRequestHandler</span><span class="sxs-lookup"><span data-stu-id="62db9-131">SingleAsyncRequestHandler</span></span> | <span data-ttu-id="62db9-132">タスク\<TResponse\> プロセス</span><span class="sxs-lookup"><span data-stu-id="62db9-132">Task\<TResponse\> Process</span></span>                           | <span data-ttu-id="62db9-133">各派生クラスによって上書きされる実行メソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-133">The execute method that will be overridden by each derived class.</span></span> |
|                           | <span data-ttu-id="62db9-134">タスク\<Response\> 実行</span><span class="sxs-lookup"><span data-stu-id="62db9-134">Task\<Response\> Execute</span></span>                            | <span data-ttu-id="62db9-135">要求ハンドラーのエントリ ポイントを表すメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-135">The method that represents the entry point of the request handler.</span></span> |
| <span data-ttu-id="62db9-136">IRequestHandlerAsync</span><span class="sxs-lookup"><span data-stu-id="62db9-136">IRequestHandlerAsync</span></span>      | <span data-ttu-id="62db9-137">タスク\<Response\> 実行 (要求の要求)</span><span class="sxs-lookup"><span data-stu-id="62db9-137">Task\<Response\> Execute (Request request)</span></span>          | <span data-ttu-id="62db9-138">非同期要求ハンドラーのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="62db9-138">The interface for the asynchronous request handler.</span></span> |
| <span data-ttu-id="62db9-139">IRequestTriggerAsync</span><span class="sxs-lookup"><span data-stu-id="62db9-139">IRequestTriggerAsync</span></span>      | <span data-ttu-id="62db9-140">タスク OnExecuting(要求の要求)</span><span class="sxs-lookup"><span data-stu-id="62db9-140">Task OnExecuting(Request request)</span></span>                   | <span data-ttu-id="62db9-141">要求が **IRequestHandler** によって処理される前に呼び出されるメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-141">The method that is invoked before the request has been processed by **IRequestHandler**.</span></span> |
| <span data-ttu-id="62db9-142">IRequestTriggerAsync</span><span class="sxs-lookup"><span data-stu-id="62db9-142">IRequestTriggerAsync</span></span>      | <span data-ttu-id="62db9-143">タスク OnExecuted(要求の要求、応答の応答)</span><span class="sxs-lookup"><span data-stu-id="62db9-143">Task OnExecuted(Request request, Response response)</span></span> | <span data-ttu-id="62db9-144">要求が **IRequestHandler** によって処理された後に呼び出されるメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-144">The method that is invoked after the request has been processed by **IRequestHandler**.</span></span> |
| <span data-ttu-id="62db9-145">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-145">DatabaseContext</span></span>           | <span data-ttu-id="62db9-146">非同期タスク<Tuple<int, PagedResult<T>>> ExecuteStoredProcedureAsync<T>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings)</span><span class="sxs-lookup"><span data-stu-id="62db9-146">async Task<Tuple<int, PagedResult<T>>> ExecuteStoredProcedureAsync<T>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)</span></span> | <span data-ttu-id="62db9-147">指定されたパラメーターを使用して、ストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-147">The method that executes the stored procedure using the specified parameters.</span></span> |
| <span data-ttu-id="62db9-148">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-148">DatabaseContext</span></span>           | <span data-ttu-id="62db9-149">非同期タスク<ReadOnlyCollection<T>> ExecuteNonPagedStoredProcedureAsync<T>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings) where T : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-149">async Task<ReadOnlyCollection<T>> ExecuteNonPagedStoredProcedureAsync<T>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-150">指定されたパラメーターを使用して、ストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-150">The method that executes the stored procedure using the specified parameters.</span></span> <span data-ttu-id="62db9-151">実行はページ設定されていません。</span><span class="sxs-lookup"><span data-stu-id="62db9-151">The execution is non-paginated.</span></span> |
|<span data-ttu-id="62db9-152">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-152">DatabaseContext</span></span>            | <span data-ttu-id="62db9-153">非同期タスク<Tuple<PagedResult<T1>、ReadOnlyCollection<T2>>> ExecuteStoredProcedureAsync<T1, T2>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-153">async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>>> ExecuteStoredProcedureAsync<T1, T2>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-154">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-154">The method that executes the specified stored procedure.</span></span> |
| <span data-ttu-id="62db9-155">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-155">DatabaseContext</span></span>                          | <span data-ttu-id="62db9-156">非同期タスク<Tuple<int, Tuple<PagedResult<T1>、ReadOnlyCollection<T2>>>> ExecuteStoredProcedureAsync<T1, T2>(文字列 procedureName、ParameterSet パラメーター、ParameterSet outputParameters、QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-156">async Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>>>> ExecuteStoredProcedureAsync<T1, T2>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-157">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-157">The method that executes the specified stored procedure.</span></span> |
|<span data-ttu-id="62db9-158">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-158">DatabaseContext</span></span>                        | <span data-ttu-id="62db9-159">非同期タスク<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>>> ExecuteStoredProcedureAsync<T1, T2, T3>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-159">async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>>> ExecuteStoredProcedureAsync<T1, T2, T3>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-160">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-160">The method that executes the specified stored procedure.</span></span> |
| <span data-ttu-id="62db9-161">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-161">DatabaseContext</span></span>                          | <span data-ttu-id="62db9-162">非同期タスク<Tuple<int, Tuple<PagedResult<T1>、ReadOnlyCollection<T2>、ReadOnlyCollection<T3>>>> ExecuteStoredProcedureAsync<T1, T2, T3>(文字列 procedureName、ParameterSet パラメーター、ParameterSet outputParameters、QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-162">async Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>>>> ExecuteStoredProcedureAsync<T1, T2, T3>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()  where T3 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-163">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-163">The method that executes the specified stored procedure.</span></span> |
| <span data-ttu-id="62db9-164">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-164">DatabaseContext</span></span>                           | <span data-ttu-id="62db9-165">非同期タスク<Tuple<PagedResult<T1>、ReadOnlyCollection<T2>、ReadOnlyCollection<T3>、ReadOnlyCollection<T4>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-165">async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-166">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-166">The method that executes the specified stored procedure.</span></span> |
| <span data-ttu-id="62db9-167">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-167">DatabaseContext</span></span>           | <span data-ttu-id="62db9-168">非同期タスク<Tuple<int, Tuple<PagedResult<T1>、ReadOnlyCollection<T2>、ReadOnlyCollection<T3>、ReadOnlyCollection<T4>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4>(文字列 procedureName、ParameterSet パラメーター、ParameterSet outputParameters、 QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-168">async Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-169">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-169">The method that executes the specified stored procedure.</span></span> |
|<span data-ttu-id="62db9-170">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-170">DatabaseContext</span></span>   | <span data-ttu-id="62db9-171">非同期タスク<Tuple<PagedResult<T1>、ReadOnlyCollection<T2>、ReadOnlyCollection<T3>、ReadOnlyCollection<T4>、 ReadOnlyCollection<T5>、ReadOnlyCollection<T6>、ReadOnlyCollection<T7>、Tuple<ReadOnlyCollection<T8>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4, T5, T6, T7, T8>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new() where T5 : CommerceEntity, new() where T6 : CommerceEntity, new() where T7 : CommerceEntity, new() where T8 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-171">async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>, ReadOnlyCollection<T5>, ReadOnlyCollection<T6>, ReadOnlyCollection<T7>, Tuple<ReadOnlyCollection<T8>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4, T5, T6, T7, T8>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new() where T5 : CommerceEntity, new() where T6 : CommerceEntity, new() where T7 : CommerceEntity, new() where T8 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-172">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-172">The method that executes the specified stored procedure.</span></span> |
| <span data-ttu-id="62db9-173">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-173">DatabaseContext</span></span>    | <span data-ttu-id="62db9-174">非同期タスク<Tuple<int, Tuple<PagedResult<T1>、ReadOnlyCollection<T2>、ReadOnlyCollection<T3>、ReadOnlyCollection<T4>、 ReadOnlyCollection<T5>、ReadOnlyCollection<T6>、ReadOnlyCollection<T7>、Tuple<ReadOnlyCollection<T8>>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4, T5, T6, T7, T8>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new() where T5 : CommerceEntity, new() where T6 : CommerceEntity, new() where T7 : CommerceEntity, new() where T8 : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-174">Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>, ReadOnlyCollection<T5>, ReadOnlyCollection<T6>, ReadOnlyCollection<T7>, Tuple<ReadOnlyCollection<T8>>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4, T5, T6, T7, T8>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new() where T5 : CommerceEntity, new() where T6 : CommerceEntity, new() where T7 : CommerceEntity, new() where T8 : CommerceEntity, new()</span></span> | <span data-ttu-id="62db9-175">指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-175">The method that executes the specified stored procedure.</span></span> |
| <span data-ttu-id="62db9-176">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-176">DatabaseContext</span></span>       | <span data-ttu-id="62db9-177">非同期タスク<ReadOnlyCollection<T>> ExecuteStoredProcedureScalarCollectionAsync<T>(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings)</span><span class="sxs-lookup"><span data-stu-id="62db9-177">Task<ReadOnlyCollection<T>> ExecuteStoredProcedureScalarCollectionAsync<T>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)</span></span>                   | <span data-ttu-id="62db9-178">単一の結果のコレクションを返すクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="62db9-178">Executes a query that returns a collection of single results.</span></span> |
| <span data-ttu-id="62db9-179">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-179">DatabaseContext</span></span>       | <span data-ttu-id="62db9-180">タスク<int> ExecuteStoredProcedureNonQueryAsync(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings)</span><span class="sxs-lookup"><span data-stu-id="62db9-180">Task<int> ExecuteStoredProcedureNonQueryAsync(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)</span></span> | <span data-ttu-id="62db9-181">指定されたパラメーターを使用して、指定されたストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-181">The method that executes the specified stored procedure with the specified parameters.</span></span> |
| <span data-ttu-id="62db9-182">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-182">DatabaseContext</span></span>       | <span data-ttu-id="62db9-183">タスク<int> ExecuteStoredProcedureScalarAsync(文字列 procedureName、ParameterSet パラメーター、QueryResultSettings resultSettings)</span><span class="sxs-lookup"><span data-stu-id="62db9-183">Task<int> ExecuteStoredProcedureScalarAsync(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)</span></span> | <span data-ttu-id="62db9-184">指定されたパラメーターを使用して戻り値を返す、ストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-184">The method that executes the stored procedure using the specified parameters and returns the return value.</span></span> |
| <span data-ttu-id="62db9-185">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-185">DatabaseContext</span></span>      | <span data-ttu-id="62db9-186">タスク OnExecuting(要求の要求)</span><span class="sxs-lookup"><span data-stu-id="62db9-186">Task OnExecuting(Request request)</span></span>                   | <span data-ttu-id="62db9-187">指定されたパラメーターを使用して戻り値を返す、ストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="62db9-187">Executes the stored procedure using the specified parameters and returns the return value.</span></span> |
| <span data-ttu-id="62db9-188">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-188">DatabaseContext</span></span>      | <span data-ttu-id="62db9-189">タスク<int> ExecuteStoredProcedureScalarAsync(文字列 procedureName、ParameterSet パラメーター、ParameterSet outputParameters、QueryResultSettings resultSettings)</span><span class="sxs-lookup"><span data-stu-id="62db9-189">Task<int> ExecuteStoredProcedureScalarAsync(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings)</span></span> | <span data-ttu-id="62db9-190">指定されたパラメーターを使用して戻り値を返す、ストアド プロシージャを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-190">The method that executes the stored procedure using the specified parameters and returns the return value.</span></span> |
| <span data-ttu-id="62db9-191">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-191">DatabaseContext</span></span>       | <span data-ttu-id="62db9-192">タスク<PagedResult<T>> ReadEntityAsync<T>(IDatabaseQuery query) where T : CommerceEntity, new()</span><span class="sxs-lookup"><span data-stu-id="62db9-192">Task<PagedResult<T>> ReadEntityAsync<T>(IDatabaseQuery query) where T : CommerceEntity, new()</span></span>  | <span data-ttu-id="62db9-193">データベースからエンティティを読み取るメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-193">The method that reads an entity from the database.</span></span> |
| <span data-ttu-id="62db9-194">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-194">DatabaseContext</span></span>       | <span data-ttu-id="62db9-195">タスク ExecuteNonQueryAsync (IDatabaseQuery クエリ)</span><span class="sxs-lookup"><span data-stu-id="62db9-195">Task ExecuteNonQueryAsync(IDatabaseQuery query)</span></span>                   | <span data-ttu-id="62db9-196">出力のないクエリを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-196">The method that executes a query that has no output.</span></span> |
| <span data-ttu-id="62db9-197">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-197">DatabaseContext</span></span>       | <span data-ttu-id="62db9-198">タスク<T> ExecuteScalarAsync<T>(IDatabaseQuery クエリ)</span><span class="sxs-lookup"><span data-stu-id="62db9-198">Task<T> ExecuteScalarAsync<T>(IDatabaseQuery query)</span></span>                   | <span data-ttu-id="62db9-199">出力のないクエリを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-199">The method that executes a query that has no output.</span></span> |
| <span data-ttu-id="62db9-200">DatabaseContext</span><span class="sxs-lookup"><span data-stu-id="62db9-200">DatabaseContext</span></span>       | <span data-ttu-id="62db9-201">タスク<ReadOnlyCollection<T>> ExecuteScalarCollectionAsync<T>(IDatabaseQuery クエリ)</span><span class="sxs-lookup"><span data-stu-id="62db9-201">Task<ReadOnlyCollection<T>> ExecuteScalarCollectionAsync<T>(IDatabaseQuery query)</span></span>                   | <span data-ttu-id="62db9-202">単一の結果のコレクションを返すクエリを実行するメソッド。</span><span class="sxs-lookup"><span data-stu-id="62db9-202">The method that executes a query that returns a collection of single results.</span></span> |
    

<span data-ttu-id="62db9-203">非同期実行は、次のようなシナリオでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="62db9-203">Asynchronous execution is supported for these scenarios:</span></span>

+ <span data-ttu-id="62db9-204">新しいコマース API</span><span class="sxs-lookup"><span data-stu-id="62db9-204">New Commerce APIs</span></span>

    - <span data-ttu-id="62db9-205">非同期 Commerce Runtime API</span><span class="sxs-lookup"><span data-stu-id="62db9-205">Asynchronous Commerce Runtime API</span></span>
    - <span data-ttu-id="62db9-206">非同期 Retail サーバー コントローラー</span><span class="sxs-lookup"><span data-stu-id="62db9-206">Asynchronous Retail server controller</span></span>

+ <span data-ttu-id="62db9-207">実行中のコマース API ハンドラーの上書き</span><span class="sxs-lookup"><span data-stu-id="62db9-207">Overrides of the Commerce API handler that is running</span></span>
+ <span data-ttu-id="62db9-208">プレトリガーとポストトリガー</span><span class="sxs-lookup"><span data-stu-id="62db9-208">Pre-triggers and post-triggers</span></span>

## <a name="create-a-new-asynchronous-commerce-runtime-api"></a><span data-ttu-id="62db9-209">新しい非同期 Commerce Runtime API の作成</span><span class="sxs-lookup"><span data-stu-id="62db9-209">Create a new asynchronous Commerce Runtime API</span></span>

<span data-ttu-id="62db9-210">新しい非同期コマース API を作成するには、次の 3 つのクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62db9-210">To create a new asynchronous Commerce API, you must create three classes:</span></span>

+ <span data-ttu-id="62db9-211">**要求** クラスを実装することにより、要求クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="62db9-211">Create the request class by implementing the **Request** class.</span></span>
+ <span data-ttu-id="62db9-212">**応答** クラスを実装することにより、非同期応答クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="62db9-212">Create the asynchronous response class by implementing the **Response** class.</span></span>
+ <span data-ttu-id="62db9-213">非同期ハンドラー クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="62db9-213">Create the asynchronous handler class.</span></span>

<span data-ttu-id="62db9-214">クラスを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="62db9-214">To create the classes, follow these steps.</span></span>

1. <span data-ttu-id="62db9-215">要求クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="62db9-215">Create the request class.</span></span>

    ```C#
    namespace Contoso
    {
        namespace Commerce.Runtime.AsyncRequestSample.Messages
        {
            using System.Runtime.Serialization;
            using System;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;
    
            /// <summary>
            /// Sample request for AsyncRequestSampleRequest
            /// </summary>
            [DataContract]
            public sealed class AsyncRequestSampleRequest : Request
            {
                /// <summary>
                /// Initializes a new instance of the <see cref="AsyncRequestSampleRequest"/> class.
                /// </summary>
                public AsyncRequestSampleRequest()
                {
                }
    
            }
        }
    }
    ```

2. <span data-ttu-id="62db9-216">応答クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="62db9-216">Create the response class.</span></span>

    ```C#
    namespace Contoso
    {
        namespace Commerce.Runtime.AsyncSample.Messages
        {
            using System.Runtime.Serialization;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;
            using Microsoft.Dynamics.Commerce.Runtime.DataModel;
    
            /// <summary>
            /// Defines a simple response class .
            /// </summary>
            [DataContract]
            public sealed class AsyncSampleResponse : Response
            {
                /// <summary>
                /// Initializes a new instance of the <see cref="AsyncSampleResponse"/> class.
                /// </summary>
                /// <param name="CustomerRec">Customer.</param>
                public AsyncSampleResponse(Customer customer)
                {
                    this.CustomerRec = customer;
                }
    
                /// <summary>
                /// Gets the customer related to the request.
                /// </summary>
                [DataMember]
                public Customer CustomerRec { get; private set; }
    
            }
        }
    }
    ```

3. <span data-ttu-id="62db9-217">非同期ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="62db9-217">Create the asynchronous handler.</span></span>

    ```C#
    using Contoso.Commerce.Runtime.AsyncSample.Messages;
    using System.Linq;
    using System.Threading.Tasks;
    using Microsoft.Dynamics.Commerce.Runtime;
    using Microsoft.Dynamics.Commerce.Runtime.DataModel;
    using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
    
    namespace Commerce.Runtime.AsyncSample.Messages
    {
        public class AsyncSampleRequestHandler : SingleAsyncRequestHandler<AsyncSampleRequest, AsyncSampleResponse>
        {
            protected override async Task<AsyncSampleResponse> Process(AsyncSampleRequest request)
            {
                var customers = await AsyncSampleMethodGetCustomer(request.RequestContext);
    
                return new AsyncSampleResponse(customers);
            }
    
            private async Task<Customer> AsyncSampleMethodGetCustomer(RequestContext context)
            {
                //do custom logic here. Execute any custom logic or request asynchronously.
                var getCustomerRequest = new GetCustomersServiceRequest(QueryResultSettings.SingleRecord, "2001", SearchLocation.Local);
                var getCustomerResponse = await context.ExecuteAsync<GetCustomersServiceResponse>(getCustomerRequest);
                return getCustomerResponse.Customers.SingleOrDefault();
            }
        }
    }
    ```

## <a name="create-a-new-asynchronous-retail-server-controller"></a><span data-ttu-id="62db9-218">新しい非同期 Retail サーバー コントローラーの作成</span><span class="sxs-lookup"><span data-stu-id="62db9-218">Create a new asynchronous Retail server controller</span></span>

<span data-ttu-id="62db9-219">非同期の Retail サーバー コントローラー拡張機能を作成するには、次の例に示すように、**CommerceControllerAsync** クラスからコントローラー クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="62db9-219">To create an asynchronous Retail server controller extension, extend the controller class from the **CommerceControllerAsync** class, as shown in the following example.</span></span>

```C#
namespace Microsoft.Dynamics.Retail.RetailServerLibrary.ODataControllers
{
    using System.Runtime.InteropServices;
    using System.Threading.Tasks;
    using System.Web.Http.Controllers;
    using System.Web.OData;
    using Commerce.Runtime;
    using Commerce.Runtime.Client;
    using Commerce.Runtime.DataModel;

    /// <summary>
    /// The catalogs controller.
    /// </summary>
    [ComVisible(false)]
    public class CustomController : CommerceControllerAsync<MyEntity, string>
    {

        /// <summary>
        /// Gets the controller name.
        /// </summary>
        public override string ControllerName
        {
            get { return "MyEntity"; }
        }

        /// <summary>
        /// Gets the <c>MyEntity</c> entity by key.
        /// </summary>
        /// <param name="key">
        /// The key.
        /// </param>
        /// <returns>
        /// The <see cref="ScanResult"/>.
        /// </returns>
        [CommerceAuthorization(CommerceRoles.Employee)]
        protected override Task<MyEntity> GetEntityByKey(string key)
        {
            return this.GetMyEntityAsync(key);
        }

        /// <summary>
        /// Retrieves the entity information based on <see cref="key"/> input.
        /// </summary>
        /// <param name="key">key input.</param>
        /// <returns>Instance of <see cref="MyEntity"/> that contains entities found by input text.</returns>
        public async Task<MyEntity> GetMyEntityAsync(string key)
        {
            ThrowIf.Null(key, nameof(key));

            var request = new MyCustomRequest(key);
            var response = await this.runtime.ExecuteAsync<MyCustomResponse>(request).ConfigureAwait(false);
            return response.Result;
        }

    }
}
```

## <a name="override-an-out-of-box-request-handler-asynchronously"></a><span data-ttu-id="62db9-220">標準の要求ハンドラーを非同期に上書きする</span><span class="sxs-lookup"><span data-stu-id="62db9-220">Override an out-of-box request handler asynchronously</span></span>

<span data-ttu-id="62db9-221">サポートされる標準の要求ハンドラーを上書きするには、このパターンに従います。</span><span class="sxs-lookup"><span data-stu-id="62db9-221">To override the supported out-of-box request handler, follow this pattern.</span></span>

<span data-ttu-id="62db9-222">たとえば、標準の **GetScanResultRequestHandler** ハンドラーを上書きするには、ハンドラーを上書きしてから、**タスク** と **待機** を使用して応答を返します。</span><span class="sxs-lookup"><span data-stu-id="62db9-222">For example, to override the out-of-box **GetScanResultRequestHandler** handler, override the handler, and return the response by using **Task** and **await**.</span></span>

```C#
namespace Contoso
{
    namespace Commerce.Runtime.Workflow
    {
        using System.Linq;
        using System.Threading.Tasks;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;

        /// <summary>
        /// Workflow that retrieves information based on scan input.
        /// </summary>
        public class GetScanResultRequestHandler : SingleAsyncRequestHandler<GetScanResultRequest, GetScanResultResponse>
        {
            /// <summary>
            /// Executes the workflow to get scan result.
            /// </summary>
            /// <param name="request">Instance of <see cref="GetScanResultRequest"/>.</param>
            /// <returns>Instance of <see cref="GetScanResultResponse"/>.</returns>
            protected override async Task<GetScanResultResponse> Process(GetScanResultRequest request)
            {
                ThrowIf.Null(request, nameof(request));

                var getBarcodeRequest = new GetBarcodeRequest(request.ScanInfo);
                var getBarcodeResponse = request.RequestContext.Execute<GetBarcodeResponse>(getBarcodeRequest);
                Barcode barcode = getBarcodeResponse.Barcode;
                BarcodeMaskType maskType = barcode == null ? BarcodeMaskType.None : barcode.Mask.MaskType;
                ScanResult result = new ScanResult(request.ScanInfo.ScannedText) { Barcode = barcode, MaskType = maskType };

                //For this sample, we skipped lot of logic inside this method. This should be used only for reference on how to override OOB request. The logic written inside this sample is different from the actual implementation of this handler.

                result.Product = await this.GetSingleProductByItemId(request.RequestContext, barcode.ItemBarcode.ItemId, barcode.ItemBarcode.InventoryDimensionId).ConfigureAwait(false);

                return new GetScanResultResponse(result);

            }

            private async Task<SimpleProduct> GetSingleProductByItemId(RequestContext context, string itemId, string inventDimId)
            {
                //do custom logic here. Execute any custom logic or request asynchronously.

                if (string.IsNullOrWhiteSpace(itemId))
                {
                    return null;
                }

                var lookupClause = new ProductLookupClause { ItemId = itemId, InventDimensionId = inventDimId };

                var getProductRequest = new GetProductsServiceRequest(
                    context.GetPrincipal().ChannelId,
                    new[] { lookupClause },
                    QueryResultSettings.AllRecords);
                getProductRequest.SearchLocation = SearchLocation.Local;  // Scanned products must be found locally.
                var products = (await context.ExecuteAsync<GetProductsServiceResponse>(getProductRequest).ConfigureAwait(false)).Products;

                if (products.Results.IsNullOrEmpty() || products.Results.HasMultiple())
                {
                    // if product is not found or multiple products founds (not exact match) return 'null'
                    return null;
                }

                return products.Results.Single();

            }

        }
    }
}
```

## <a name="create-a-trigger-asynchronously"></a><span data-ttu-id="62db9-223">トリガーを非同期に作成する</span><span class="sxs-lookup"><span data-stu-id="62db9-223">Create a trigger asynchronously</span></span>

<span data-ttu-id="62db9-224">トリガーのロジックを非同期で実行するには、**irequesttriggerasync** インターフェイスを拡張してから、ロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="62db9-224">To run the logic in the trigger asynchronously, extend the **IRequestTriggerAsync** interface, and add the logic.</span></span>

```C#
namespace Contoso
{
    using System;
    using System.Collections.Generic;
    using System.Composition;
    using System.Threading.Tasks;
    using Microsoft.Dynamics.Commerce.Runtime.Messages;
    using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;

    /// <summary>
    /// Test implementation of request trigger for <see cref="TestRequest"/>.
    /// </summary>
    public class SampleRequestTriggerAsync : IRequestTriggerAsync
    {
        private readonly Func<Task> onExecutingCallback;
        private readonly Func<Task> onExecutedCallback;

        public TestRequestTriggerAsync()
        {
        }

        [ImportingConstructor]
        public TestRequestTriggerAsync([Import("OnExecutingCallback")]Func<Task> onExecutingCallback, [Import("OnExecutedCallback")]Func<Task> onExecutedCallback)
        {
            this.onExecutingCallback = onExecutingCallback;
            this.onExecutedCallback = onExecutedCallback;
        }

        /// <summary>
        /// Gets the collection of request types supported by this trigger.
        /// </summary>
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new[]
                {
                    // Add the request for pre or post trigger execution.
                    typeof(GetCustomerDataRequest)
                };
            }
        }

        /// <summary>
        /// Invoked before request has been processed by <see cref="IRequestHandler"/>.
        /// </summary>
        /// <param name="request">The incoming request message.</param>
        /// <returns>The empty Task.</returns>
        public Task OnExecuting(Request request)
        {
            if (this.onExecutingCallback != null)
            {
                return this.onExecutingCallback();
            }

            return Task.CompletedTask;
        }

        /// <summary>
        /// Invoked after request has been processed by <see cref="IRequestHandler"/>.
        /// </summary>
        /// <param name="request">The request message processed by handler.</param>
        /// <param name="response">The response message generated by handler.</param>
        /// <returns>The empty Task.</returns>
        public Task OnExecuted(Request request, Response response)
        {
            if (this.onExecutedCallback != null)
            {
                return this.onExecutedCallback();
            }

            return Task.CompletedTask;
        }
    }
}
```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]