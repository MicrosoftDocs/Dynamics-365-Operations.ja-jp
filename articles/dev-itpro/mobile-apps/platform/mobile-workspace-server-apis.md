---
title: サーバー側の開発 (ワークスペース X++ API)
description: Microsoft Dynamics 365 for Finance and Operations には、豊富なオフラインおよびモバイルの相互関係と、扱いやすいデザイナー体験を可能にする携帯電話アプリのサポートが含まれています。
author: RobinARH
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.search.region: Global
ms.author: shshabazz
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: f3a1f7893aa7835c04b331045911eb3b9c47212e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549736"
---
# <a name="server-side-development-workspace-x-apis"></a><span data-ttu-id="d9e27-103">サーバー側の開発 (ワークスペース X++ API)</span><span class="sxs-lookup"><span data-stu-id="d9e27-103">Server-side development (workspace X++ APIs)</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="class-sysappactionattribute"></a><span data-ttu-id="d9e27-104">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-104">Class SysAppActionAttribute</span></span> 
<span data-ttu-id="d9e27-105">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-105">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-106">Methods</span></span>

| <span data-ttu-id="d9e27-107">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-107">Method name</span></span> | <span data-ttu-id="d9e27-108">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-108">Returns</span></span> | <span data-ttu-id="d9e27-109">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-109">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-110">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-110">new</span></span> | <span data-ttu-id="d9e27-111">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-111">void</span></span> | <span data-ttu-id="d9e27-112">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-112">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="d9e27-113">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="d9e27-113">pageMethodName</span></span> | <span data-ttu-id="d9e27-114">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-114">str</span></span> | <span data-ttu-id="d9e27-115">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-115">Gets the get method name which forms the page under which this task resides</span></span> |
| <span data-ttu-id="d9e27-116">actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-116">actionTitle</span></span> | <span data-ttu-id="d9e27-117">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-117">str</span></span> | <span data-ttu-id="d9e27-118">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-118">Gets the Action Title</span></span> |
| <span data-ttu-id="d9e27-119">actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-119">actionDescription</span></span> | <span data-ttu-id="d9e27-120">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-120">str</span></span> | <span data-ttu-id="d9e27-121">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-121">Gets the Action Description</span></span> |
| <span data-ttu-id="d9e27-122">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="d9e27-122">crudOperationType</span></span> | <span data-ttu-id="d9e27-123">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="d9e27-123">SysAppCRUDOperation</span></span> | <span data-ttu-id="d9e27-124">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-124">Gets the Crud Operation Type like Create, Update, Delete</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-125">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-125">Method new</span></span> 
<span data-ttu-id="d9e27-126">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-126">Creates a new instance of SysAppActionAttribute class</span></span>

     public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-127">Parameters</span></span>

| <span data-ttu-id="d9e27-128">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-128">Parameter name</span></span> |  <span data-ttu-id="d9e27-129">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-129">Parameter type</span></span> | <span data-ttu-id="d9e27-130">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-130">Optional</span></span> | <span data-ttu-id="d9e27-131">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-131">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-132">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-132">_actionTitle</span></span> | <span data-ttu-id="d9e27-133">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-133">str</span></span> | <span data-ttu-id="d9e27-134">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-134">True</span></span> | <span data-ttu-id="d9e27-135">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-135">Action title</span></span>
| <span data-ttu-id="d9e27-136">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-136">_actionDescription</span></span> | <span data-ttu-id="d9e27-137">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-137">str</span></span> | <span data-ttu-id="d9e27-138">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-138">True</span></span> | <span data-ttu-id="d9e27-139">アクション説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-139">Action description</span></span>
| <span data-ttu-id="d9e27-140">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="d9e27-140">_crudOperationType</span></span> | <span data-ttu-id="d9e27-141">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="d9e27-141">SysAppCRUDOperation</span></span> | <span data-ttu-id="d9e27-142">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-142">True</span></span> | <span data-ttu-id="d9e27-143">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="d9e27-143">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="d9e27-144">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="d9e27-144">_pageMethodName</span></span> | <span data-ttu-id="d9e27-145">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-145">str</span></span> | <span data-ttu-id="d9e27-146">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-146">True</span></span> | <span data-ttu-id="d9e27-147">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-147">Name of the method constructing parent page</span></span>


### <a name="method-pagemethodname"></a><span data-ttu-id="d9e27-148">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="d9e27-148">Method pageMethodName</span></span> 
<span data-ttu-id="d9e27-149">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-149">Gets the get method name which forms the page under which this task resides</span></span>

     public str pageMethodName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-150">Return Value</span></span> 
<span data-ttu-id="d9e27-151">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-151">The page method name which forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="d9e27-152">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-152">Method actionTitle</span></span> 
<span data-ttu-id="d9e27-153">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-153">Gets the Action Title</span></span>

     public str actionTitle () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-154">Return Value</span></span> 
<span data-ttu-id="d9e27-155">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-155">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="d9e27-156">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-156">Method actionDescription</span></span> 
<span data-ttu-id="d9e27-157">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-157">Gets the Action Description</span></span>

     public str actionDescription () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-158">Return Value</span></span> 
<span data-ttu-id="d9e27-159">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-159">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="d9e27-160">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="d9e27-160">Method crudOperationType</span></span> 
<span data-ttu-id="d9e27-161">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-161">Gets the Crud Operation Type like Create, Update, Delete</span></span>

     public SysAppCRUDOperation crudOperationType () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-162">Return Value</span></span> 
<span data-ttu-id="d9e27-163">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-163">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="d9e27-164">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-164">Class SysAppActionMetadata</span></span> 
<span data-ttu-id="d9e27-165">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-165">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-166">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-166">Methods</span></span>

| <span data-ttu-id="d9e27-167">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-167">Method name</span></span> | <span data-ttu-id="d9e27-168">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-168">Returns</span></span> | <span data-ttu-id="d9e27-169">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-169">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-170">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-170">new</span></span> | <span data-ttu-id="d9e27-171">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-171">void</span></span> |  |
| <span data-ttu-id="d9e27-172">getActionName</span><span class="sxs-lookup"><span data-stu-id="d9e27-172">getActionName</span></span> | <span data-ttu-id="d9e27-173">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-173">str</span></span> | <span data-ttu-id="d9e27-174">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-174">Returns the action name</span></span> |
| <span data-ttu-id="d9e27-175">actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-175">actionTitle</span></span> | <span data-ttu-id="d9e27-176">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-176">str</span></span> | <span data-ttu-id="d9e27-177">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-177">Gets or sets the action title</span></span> |
| <span data-ttu-id="d9e27-178">actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-178">actionDescription</span></span> | <span data-ttu-id="d9e27-179">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-179">str</span></span> | <span data-ttu-id="d9e27-180">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-180">Gets or sets the action description</span></span> |
| <span data-ttu-id="d9e27-181">actionHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-181">actionHidden</span></span> | <span data-ttu-id="d9e27-182">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-182">boolean</span></span> | <span data-ttu-id="d9e27-183">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-183">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="d9e27-184">actionOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-184">actionOrder</span></span> | <span data-ttu-id="d9e27-185">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-185">int</span></span> | <span data-ttu-id="d9e27-186">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-186">Gets or sets the action order</span></span> |
| <span data-ttu-id="d9e27-187">getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-187">getControl</span></span> | <span data-ttu-id="d9e27-188">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-188">SysAppControlMetadata</span></span> | <span data-ttu-id="d9e27-189">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-189">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="d9e27-190">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-190">getControlEnumerator</span></span> | <span data-ttu-id="d9e27-191">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-191">MapEnumerator</span></span> | <span data-ttu-id="d9e27-192">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-192">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="d9e27-193">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-193">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-194">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-194">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-195">Parameters</span></span>

| <span data-ttu-id="d9e27-196">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-196">Parameter name</span></span> |  <span data-ttu-id="d9e27-197">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-197">Parameter type</span></span> | <span data-ttu-id="d9e27-198">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-198">Optional</span></span> | <span data-ttu-id="d9e27-199">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-199">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-200">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-200">_taskmetadata</span></span> | <span data-ttu-id="d9e27-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="d9e27-202">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-202">False</span></span> | 


### <a name="method-getactionname"></a><span data-ttu-id="d9e27-203">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="d9e27-203">Method getActionName</span></span> 
<span data-ttu-id="d9e27-204">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-204">Returns the action name</span></span>

     public str getActionName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-205">Return Value</span></span> 
<span data-ttu-id="d9e27-206">アクション名</span><span class="sxs-lookup"><span data-stu-id="d9e27-206">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="d9e27-207">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-207">Method actionTitle</span></span> 
<span data-ttu-id="d9e27-208">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-208">Gets or sets the action title</span></span>

     public str actionTitle ([str _actionTitle]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-209">Parameters</span></span>

| <span data-ttu-id="d9e27-210">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-210">Parameter name</span></span> |  <span data-ttu-id="d9e27-211">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-211">Parameter type</span></span> | <span data-ttu-id="d9e27-212">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-212">Optional</span></span> | <span data-ttu-id="d9e27-213">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-213">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-214">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-214">_actionTitle</span></span> | <span data-ttu-id="d9e27-215">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-215">str</span></span> | <span data-ttu-id="d9e27-216">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-216">True</span></span> | <span data-ttu-id="d9e27-217">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-217">The action title</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-218">Return Value</span></span> 
<span data-ttu-id="d9e27-219">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-219">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="d9e27-220">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-220">Method actionDescription</span></span> 
<span data-ttu-id="d9e27-221">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-221">Gets or sets the action description</span></span>

     public str actionDescription ([str _actionDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-222">Parameters</span></span>

| <span data-ttu-id="d9e27-223">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-223">Parameter name</span></span> |  <span data-ttu-id="d9e27-224">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-224">Parameter type</span></span> | <span data-ttu-id="d9e27-225">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-225">Optional</span></span> | <span data-ttu-id="d9e27-226">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-226">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-227">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-227">_actionDescription</span></span> | <span data-ttu-id="d9e27-228">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-228">str</span></span> | <span data-ttu-id="d9e27-229">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-229">True</span></span> | <span data-ttu-id="d9e27-230">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-230">The action description</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-231">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-231">Return Value</span></span> 
<span data-ttu-id="d9e27-232">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-232">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="d9e27-233">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-233">Method actionHidden</span></span> 
<span data-ttu-id="d9e27-234">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-234">Gets or sets whether action is hidden</span></span>

     public boolean actionHidden ([boolean _actionHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-235">Parameters</span></span>

| <span data-ttu-id="d9e27-236">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-236">Parameter name</span></span> |  <span data-ttu-id="d9e27-237">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-237">Parameter type</span></span> | <span data-ttu-id="d9e27-238">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-238">Optional</span></span> | <span data-ttu-id="d9e27-239">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-239">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-240">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-240">_actionHidden</span></span> | <span data-ttu-id="d9e27-241">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-241">boolean</span></span> | <span data-ttu-id="d9e27-242">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-242">True</span></span> | <span data-ttu-id="d9e27-243">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="d9e27-243">Action hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-244">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-244">Return Value</span></span> 
<span data-ttu-id="d9e27-245">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d9e27-245">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="d9e27-246">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-246">Method actionOrder</span></span> 
<span data-ttu-id="d9e27-247">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-247">Gets or sets the action order</span></span>

     public int actionOrder ([int _actionOrder]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-248">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-248">Parameters</span></span>

| <span data-ttu-id="d9e27-249">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-249">Parameter name</span></span> |  <span data-ttu-id="d9e27-250">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-250">Parameter type</span></span> | <span data-ttu-id="d9e27-251">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-251">Optional</span></span> | <span data-ttu-id="d9e27-252">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-252">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-253">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-253">_actionOrder</span></span> | <span data-ttu-id="d9e27-254">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-254">int</span></span> | <span data-ttu-id="d9e27-255">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-255">True</span></span> | <span data-ttu-id="d9e27-256">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-256">The action order</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-257">Return Value</span></span> 
<span data-ttu-id="d9e27-258">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-258">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="d9e27-259">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-259">Method getControl</span></span> 
<span data-ttu-id="d9e27-260">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-260">Returns the control on the current action having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-261">Parameters</span></span>

| <span data-ttu-id="d9e27-262">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-262">Parameter name</span></span> |  <span data-ttu-id="d9e27-263">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-263">Parameter type</span></span> | <span data-ttu-id="d9e27-264">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-264">Optional</span></span> | <span data-ttu-id="d9e27-265">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-265">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-266">_controlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-266">_controlName</span></span> | <span data-ttu-id="d9e27-267">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-267">str</span></span> | <span data-ttu-id="d9e27-268">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-268">False</span></span> | <span data-ttu-id="d9e27-269">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="d9e27-269">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-270">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-270">Return Value</span></span> 
<span data-ttu-id="d9e27-271">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="d9e27-271">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action;otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="d9e27-272">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-272">Method getControlEnumerator</span></span> 
<span data-ttu-id="d9e27-273">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-273">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="d9e27-274">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-274">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-275">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-275">Return Value</span></span> 
<span data-ttu-id="d9e27-276">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-276">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="d9e27-277">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="d9e27-277">Class SysAppAttributeHelper</span></span> 
<span data-ttu-id="d9e27-278">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-278">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-279">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-279">Methods</span></span>

| <span data-ttu-id="d9e27-280">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-280">Method name</span></span> | <span data-ttu-id="d9e27-281">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-281">Returns</span></span> | <span data-ttu-id="d9e27-282">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-282">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-283">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-283">getAttributeFromClass</span></span> | <span data-ttu-id="d9e27-284">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-284">SysAttribute</span></span> | <span data-ttu-id="d9e27-285">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="d9e27-285">gets attribute from class</span></span> |


### <a name="method-getattributefromclass"></a><span data-ttu-id="d9e27-286">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-286">Method getAttributeFromClass</span></span> 
<span data-ttu-id="d9e27-287">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="d9e27-287">gets attribute from class</span></span>

     public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-288">Parameters</span></span>

| <span data-ttu-id="d9e27-289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-289">Parameter name</span></span> |  <span data-ttu-id="d9e27-290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-290">Parameter type</span></span> | <span data-ttu-id="d9e27-291">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-291">Optional</span></span> | <span data-ttu-id="d9e27-292">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-293">_sysClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-293">_sysClass</span></span> | <span data-ttu-id="d9e27-294">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-294">SysDictClass</span></span> | <span data-ttu-id="d9e27-295">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-295">False</span></span> | <span data-ttu-id="d9e27-296">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-296">class for which attributes is required</span></span>
| <span data-ttu-id="d9e27-297">_attributeType</span><span class="sxs-lookup"><span data-stu-id="d9e27-297">_attributeType</span></span> | <span data-ttu-id="d9e27-298">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="d9e27-298">SysAppAttributeType</span></span> | <span data-ttu-id="d9e27-299">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-299">False</span></span> | <span data-ttu-id="d9e27-300">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="d9e27-300">Type of attribute like SysAppEntityAttribute</span></span>


## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="d9e27-301">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-301">Class SysAppCollectionAttribute</span></span> 
<span data-ttu-id="d9e27-302">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-302">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-303">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-303">Methods</span></span>

| <span data-ttu-id="d9e27-304">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-304">Method name</span></span> | <span data-ttu-id="d9e27-305">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-305">Returns</span></span> | <span data-ttu-id="d9e27-306">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-306">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-307">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-307">new</span></span> | <span data-ttu-id="d9e27-308">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-308">void</span></span> | <span data-ttu-id="d9e27-309">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-309">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-310">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-310">Method new</span></span> 
<span data-ttu-id="d9e27-311">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-311">Constructor</span></span>

     public void new (str _itemContractName, [str _label], [str _relationshipName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-312">Parameters</span></span>

| <span data-ttu-id="d9e27-313">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-313">Parameter name</span></span> |  <span data-ttu-id="d9e27-314">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-314">Parameter type</span></span> | <span data-ttu-id="d9e27-315">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-315">Optional</span></span> | <span data-ttu-id="d9e27-316">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-316">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-317">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="d9e27-317">_itemContractName</span></span> | <span data-ttu-id="d9e27-318">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-318">str</span></span> | <span data-ttu-id="d9e27-319">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-319">False</span></span> | <span data-ttu-id="d9e27-320">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="d9e27-320">Data contract name of list item</span></span>
| <span data-ttu-id="d9e27-321">_label</span><span class="sxs-lookup"><span data-stu-id="d9e27-321">_label</span></span> | <span data-ttu-id="d9e27-322">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-322">str</span></span> | <span data-ttu-id="d9e27-323">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-323">True</span></span> | <span data-ttu-id="d9e27-324">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-324">List control label</span></span>
| <span data-ttu-id="d9e27-325">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="d9e27-325">_relationshipName</span></span> | <span data-ttu-id="d9e27-326">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-326">str</span></span> | <span data-ttu-id="d9e27-327">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-327">True</span></span> | <span data-ttu-id="d9e27-328">関係名。</span><span class="sxs-lookup"><span data-stu-id="d9e27-328">Relationship name.</span></span> <span data-ttu-id="d9e27-329">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-329">By default the entity name of the list item is used as relationship name</span></span>


## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="d9e27-330">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-330">Class SysAppControlMetadata</span></span> 
<span data-ttu-id="d9e27-331">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-331">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="d9e27-332">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="d9e27-332">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-333">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-333">Methods</span></span>

| <span data-ttu-id="d9e27-334">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-334">Method name</span></span> | <span data-ttu-id="d9e27-335">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-335">Returns</span></span> | <span data-ttu-id="d9e27-336">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-336">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-337">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-337">new</span></span> | <span data-ttu-id="d9e27-338">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-338">void</span></span> | <span data-ttu-id="d9e27-339">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-339">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="d9e27-340">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="d9e27-340">getBaseLanguageId</span></span> | <span data-ttu-id="d9e27-341">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-341">str</span></span> | <span data-ttu-id="d9e27-342">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-342">Returns the base language id for the app</span></span> |
| <span data-ttu-id="d9e27-343">getControlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-343">getControlName</span></span> | <span data-ttu-id="d9e27-344">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-344">str</span></span> | <span data-ttu-id="d9e27-345">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-345">Returns the control name</span></span> |
| <span data-ttu-id="d9e27-346">controlLabel</span><span class="sxs-lookup"><span data-stu-id="d9e27-346">controlLabel</span></span> | <span data-ttu-id="d9e27-347">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-347">str</span></span> | <span data-ttu-id="d9e27-348">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-348">Gets and sets the control label</span></span> |
| <span data-ttu-id="d9e27-349">controlHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-349">controlHidden</span></span> | <span data-ttu-id="d9e27-350">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-350">boolean</span></span> | <span data-ttu-id="d9e27-351">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-351">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="d9e27-352">controlOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-352">controlOrder</span></span> | <span data-ttu-id="d9e27-353">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-353">int</span></span> | <span data-ttu-id="d9e27-354">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-354">Gets or sets the control order</span></span> |
| <span data-ttu-id="d9e27-355">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="d9e27-355">controlMandatory</span></span> | <span data-ttu-id="d9e27-356">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-356">boolean</span></span> | <span data-ttu-id="d9e27-357">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-357">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="d9e27-358">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="d9e27-358">controlAllowNegative</span></span> | <span data-ttu-id="d9e27-359">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-359">boolean</span></span> | <span data-ttu-id="d9e27-360">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="d9e27-360">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="d9e27-361">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="d9e27-361">controlMaxLength</span></span> | <span data-ttu-id="d9e27-362">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-362">int</span></span> | <span data-ttu-id="d9e27-363">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-363">Gets or sets the control max length</span></span> |
| <span data-ttu-id="d9e27-364">getProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-364">getProperty</span></span> | <span data-ttu-id="d9e27-365">anytype</span><span class="sxs-lookup"><span data-stu-id="d9e27-365">anytype</span></span> | <span data-ttu-id="d9e27-366">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-366">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="d9e27-367">setProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-367">setProperty</span></span> | <span data-ttu-id="d9e27-368">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-368">void</span></span> | <span data-ttu-id="d9e27-369">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-369">Sets the control property referenced by the key</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-370">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-370">Method new</span></span> 
<span data-ttu-id="d9e27-371">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-371">Creates a new instance of the control metadata</span></span>

     public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-372">Parameters</span></span>

| <span data-ttu-id="d9e27-373">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-373">Parameter name</span></span> |  <span data-ttu-id="d9e27-374">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-374">Parameter type</span></span> | <span data-ttu-id="d9e27-375">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-375">Optional</span></span> | <span data-ttu-id="d9e27-376">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-376">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-377">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-377">_controlMetadata</span></span> | <span data-ttu-id="d9e27-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="d9e27-379">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-379">False</span></span> | <span data-ttu-id="d9e27-380">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-380">The controlMetadata object</span></span>
| <span data-ttu-id="d9e27-381">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="d9e27-381">_baseLanguageId</span></span> | <span data-ttu-id="d9e27-382">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-382">str</span></span> | <span data-ttu-id="d9e27-383">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-383">True</span></span> | <span data-ttu-id="d9e27-384">基本言語</span><span class="sxs-lookup"><span data-stu-id="d9e27-384">The base language</span></span>


### <a name="method-getbaselanguageid"></a><span data-ttu-id="d9e27-385">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="d9e27-385">Method getBaseLanguageId</span></span> 
<span data-ttu-id="d9e27-386">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-386">Returns the base language id for the app</span></span>

     public str getBaseLanguageId () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-387">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-387">Return Value</span></span> 
<span data-ttu-id="d9e27-388">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-388">The base language id</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="d9e27-389">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-389">Method getControlName</span></span> 
<span data-ttu-id="d9e27-390">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-390">Returns the control name</span></span>

     public str getControlName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-391">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-391">Return Value</span></span> 
<span data-ttu-id="d9e27-392">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="d9e27-392">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="d9e27-393">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="d9e27-393">Method controlLabel</span></span> 
<span data-ttu-id="d9e27-394">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-394">Gets and sets the control label</span></span>

     public str controlLabel ([str _controlLabel]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-395">Parameters</span></span>

| <span data-ttu-id="d9e27-396">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-396">Parameter name</span></span> |  <span data-ttu-id="d9e27-397">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-397">Parameter type</span></span> | <span data-ttu-id="d9e27-398">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-398">Optional</span></span> | <span data-ttu-id="d9e27-399">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-399">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-400">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="d9e27-400">_controlLabel</span></span> | <span data-ttu-id="d9e27-401">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-401">str</span></span> | <span data-ttu-id="d9e27-402">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-402">True</span></span> | <span data-ttu-id="d9e27-403">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-403">The control label</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-404">Return Value</span></span> 
<span data-ttu-id="d9e27-405">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-405">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="d9e27-406">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-406">Method controlHidden</span></span> 
<span data-ttu-id="d9e27-407">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-407">Gets and sets whether the control is hidden</span></span>

     public boolean controlHidden ([boolean _controlHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-408">Parameters</span></span>

| <span data-ttu-id="d9e27-409">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-409">Parameter name</span></span> |  <span data-ttu-id="d9e27-410">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-410">Parameter type</span></span> | <span data-ttu-id="d9e27-411">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-411">Optional</span></span> | <span data-ttu-id="d9e27-412">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-412">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-413">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-413">_controlHidden</span></span> | <span data-ttu-id="d9e27-414">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-414">boolean</span></span> | <span data-ttu-id="d9e27-415">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-415">True</span></span> | <span data-ttu-id="d9e27-416">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="d9e27-416">Control hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-417">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-417">Return Value</span></span> 
<span data-ttu-id="d9e27-418">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d9e27-418">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="d9e27-419">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-419">Method controlOrder</span></span> 
<span data-ttu-id="d9e27-420">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-420">Gets or sets the control order</span></span>

     public int controlOrder ([int _controlOrder]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-421">Parameters</span></span>

| <span data-ttu-id="d9e27-422">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-422">Parameter name</span></span> |  <span data-ttu-id="d9e27-423">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-423">Parameter type</span></span> | <span data-ttu-id="d9e27-424">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-424">Optional</span></span> | <span data-ttu-id="d9e27-425">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-425">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-426">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-426">_controlOrder</span></span> | <span data-ttu-id="d9e27-427">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-427">int</span></span> | <span data-ttu-id="d9e27-428">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-428">True</span></span> | <span data-ttu-id="d9e27-429">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-429">The control order</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-430">Return Value</span></span> 
<span data-ttu-id="d9e27-431">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-431">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="d9e27-432">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="d9e27-432">Method controlMandatory</span></span> 
<span data-ttu-id="d9e27-433">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-433">Gets or sets the control mandatory</span></span>

     public boolean controlMandatory ([boolean _controlMandatory]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-434">Parameters</span></span>

| <span data-ttu-id="d9e27-435">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-435">Parameter name</span></span> |  <span data-ttu-id="d9e27-436">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-436">Parameter type</span></span> | <span data-ttu-id="d9e27-437">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-437">Optional</span></span> | <span data-ttu-id="d9e27-438">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-438">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-439">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="d9e27-439">_controlMandatory</span></span> | <span data-ttu-id="d9e27-440">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-440">boolean</span></span> | <span data-ttu-id="d9e27-441">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-441">True</span></span> | <span data-ttu-id="d9e27-442">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="d9e27-442">The control mandatory</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-443">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-443">Return Value</span></span> 
<span data-ttu-id="d9e27-444">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="d9e27-444">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="d9e27-445">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="d9e27-445">Method controlAllowNegative</span></span> 
<span data-ttu-id="d9e27-446">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="d9e27-446">Gets or sets the control allow negative</span></span>

     public boolean controlAllowNegative ([boolean _controlAllowNegative]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-447">Parameters</span></span>

| <span data-ttu-id="d9e27-448">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-448">Parameter name</span></span> |  <span data-ttu-id="d9e27-449">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-449">Parameter type</span></span> | <span data-ttu-id="d9e27-450">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-450">Optional</span></span> | <span data-ttu-id="d9e27-451">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-451">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-452">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="d9e27-452">_controlAllowNegative</span></span> | <span data-ttu-id="d9e27-453">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-453">boolean</span></span> | <span data-ttu-id="d9e27-454">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-454">True</span></span> | <span data-ttu-id="d9e27-455">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-455">The control allow negative</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-456">Return Value</span></span> 
<span data-ttu-id="d9e27-457">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-457">The control allow negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="d9e27-458">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="d9e27-458">Method controlMaxLength</span></span> 
<span data-ttu-id="d9e27-459">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-459">Gets or sets the control max length</span></span>

     public int controlMaxLength ([int _controlMaxLength]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-460">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-460">Parameters</span></span>

| <span data-ttu-id="d9e27-461">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-461">Parameter name</span></span> |  <span data-ttu-id="d9e27-462">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-462">Parameter type</span></span> | <span data-ttu-id="d9e27-463">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-463">Optional</span></span> | <span data-ttu-id="d9e27-464">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-464">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-465">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="d9e27-465">_controlMaxLength</span></span> | <span data-ttu-id="d9e27-466">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-466">int</span></span> | <span data-ttu-id="d9e27-467">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-467">True</span></span> | <span data-ttu-id="d9e27-468">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="d9e27-468">The control max length</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-469">Return Value</span></span> 
<span data-ttu-id="d9e27-470">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="d9e27-470">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="d9e27-471">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-471">Method getProperty</span></span> 
<span data-ttu-id="d9e27-472">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-472">Gets the control property referenced by the key</span></span>

     public anytype getProperty (str _key) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-473">Parameters</span></span>

| <span data-ttu-id="d9e27-474">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-474">Parameter name</span></span> |  <span data-ttu-id="d9e27-475">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-475">Parameter type</span></span> | <span data-ttu-id="d9e27-476">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-476">Optional</span></span> | <span data-ttu-id="d9e27-477">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-477">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-478">_key</span><span class="sxs-lookup"><span data-stu-id="d9e27-478">_key</span></span> | <span data-ttu-id="d9e27-479">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-479">str</span></span> | <span data-ttu-id="d9e27-480">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-480">False</span></span> | <span data-ttu-id="d9e27-481">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="d9e27-481">The name of the control property</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-482">Return Value</span></span> 
<span data-ttu-id="d9e27-483">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="d9e27-483">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="d9e27-484">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-484">Method setProperty</span></span> 
<span data-ttu-id="d9e27-485">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-485">Sets the control property referenced by the key</span></span>

     public void setProperty (str _key, anytype _value) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-486">Parameters</span></span>

| <span data-ttu-id="d9e27-487">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-487">Parameter name</span></span> |  <span data-ttu-id="d9e27-488">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-488">Parameter type</span></span> | <span data-ttu-id="d9e27-489">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-489">Optional</span></span> | <span data-ttu-id="d9e27-490">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-490">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-491">_key</span><span class="sxs-lookup"><span data-stu-id="d9e27-491">_key</span></span> | <span data-ttu-id="d9e27-492">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-492">str</span></span> | <span data-ttu-id="d9e27-493">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-493">False</span></span> | <span data-ttu-id="d9e27-494">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="d9e27-494">The name of the control property</span></span>
| <span data-ttu-id="d9e27-495">_value</span><span class="sxs-lookup"><span data-stu-id="d9e27-495">_value</span></span> | <span data-ttu-id="d9e27-496">anytype</span><span class="sxs-lookup"><span data-stu-id="d9e27-496">anytype</span></span> | <span data-ttu-id="d9e27-497">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-497">False</span></span> | <span data-ttu-id="d9e27-498">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-498">The value of the control property</span></span>


## <a name="class-sysappentityattribute"></a><span data-ttu-id="d9e27-499">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-499">Class SysAppEntityAttribute</span></span> 
<span data-ttu-id="d9e27-500">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-500">SysAppEntityAttribute used for decorating data contract entitities</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-501">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-501">Methods</span></span>

| <span data-ttu-id="d9e27-502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-502">Method name</span></span> | <span data-ttu-id="d9e27-503">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-503">Returns</span></span> | <span data-ttu-id="d9e27-504">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-504">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-505">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-505">new</span></span> | <span data-ttu-id="d9e27-506">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-506">void</span></span> | <span data-ttu-id="d9e27-507">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-507">Constructor</span></span> |
| <span data-ttu-id="d9e27-508">名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-508">name</span></span> | <span data-ttu-id="d9e27-509">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-509">str</span></span> | <span data-ttu-id="d9e27-510">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-510">Gets the name of the entity</span></span> |
| <span data-ttu-id="d9e27-511">entityKey</span><span class="sxs-lookup"><span data-stu-id="d9e27-511">entityKey</span></span> | <span data-ttu-id="d9e27-512">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-512">str</span></span> | <span data-ttu-id="d9e27-513">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-513">Gets the entity key</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-514">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-514">Method new</span></span> 
<span data-ttu-id="d9e27-515">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-515">Constructor</span></span>

     public void new (str _name, str _entityKey) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-516">Parameters</span></span>

| <span data-ttu-id="d9e27-517">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-517">Parameter name</span></span> |  <span data-ttu-id="d9e27-518">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-518">Parameter type</span></span> | <span data-ttu-id="d9e27-519">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-519">Optional</span></span> | <span data-ttu-id="d9e27-520">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-520">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-521">_name</span><span class="sxs-lookup"><span data-stu-id="d9e27-521">_name</span></span> | <span data-ttu-id="d9e27-522">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-522">str</span></span> | <span data-ttu-id="d9e27-523">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-523">False</span></span> | <span data-ttu-id="d9e27-524">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-524">Entity name</span></span>
| <span data-ttu-id="d9e27-525">_entityKey</span><span class="sxs-lookup"><span data-stu-id="d9e27-525">_entityKey</span></span> | <span data-ttu-id="d9e27-526">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-526">str</span></span> | <span data-ttu-id="d9e27-527">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-527">False</span></span> | <span data-ttu-id="d9e27-528">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-528">Name of the entity's key</span></span>


### <a name="method-name"></a><span data-ttu-id="d9e27-529">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-529">Method name</span></span> 
<span data-ttu-id="d9e27-530">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-530">Gets the name of the entity</span></span>

     public str name () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-531">Return Value</span></span> 
<span data-ttu-id="d9e27-532">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-532">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="d9e27-533">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="d9e27-533">Method entityKey</span></span> 
<span data-ttu-id="d9e27-534">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-534">Gets the entity key</span></span>

     public str entityKey () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-535">Return Value</span></span> 
<span data-ttu-id="d9e27-536">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="d9e27-536">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="d9e27-537">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-537">Class SysAppEntityContext</span></span> 
<span data-ttu-id="d9e27-538">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-538">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-539">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-539">Methods</span></span>

| <span data-ttu-id="d9e27-540">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-540">Method name</span></span> | <span data-ttu-id="d9e27-541">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-541">Returns</span></span> | <span data-ttu-id="d9e27-542">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-542">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-543">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="d9e27-543">constructFromParams</span></span> | <span data-ttu-id="d9e27-544">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-544">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-545">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-545">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="d9e27-546">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="d9e27-546">constructFromBuffer</span></span> | <span data-ttu-id="d9e27-547">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-547">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-548">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="d9e27-548">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="d9e27-549">entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-549">entityName</span></span> | <span data-ttu-id="d9e27-550">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-550">str</span></span> | <span data-ttu-id="d9e27-551">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-551">Entity name on which filter applies</span></span> |
| <span data-ttu-id="d9e27-552">entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-552">entityId</span></span> | <span data-ttu-id="d9e27-553">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-553">str</span></span> | <span data-ttu-id="d9e27-554">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-554">Field value on which filter applies</span></span> |


### <a name="method-constructfromparams"></a><span data-ttu-id="d9e27-555">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="d9e27-555">Method constructFromParams</span></span> 
<span data-ttu-id="d9e27-556">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-556">Constructs SysAppEntityContext from entityName and entityId</span></span>

     public SysAppEntityContext constructFromParams (str _entityName, str _entityId) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-557">Parameters</span></span>

| <span data-ttu-id="d9e27-558">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-558">Parameter name</span></span> |  <span data-ttu-id="d9e27-559">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-559">Parameter type</span></span> | <span data-ttu-id="d9e27-560">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-560">Optional</span></span> | <span data-ttu-id="d9e27-561">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-561">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-562">_entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-562">_entityName</span></span> | <span data-ttu-id="d9e27-563">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-563">str</span></span> | <span data-ttu-id="d9e27-564">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-564">False</span></span> | <span data-ttu-id="d9e27-565">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-565">Entity name</span></span>
| <span data-ttu-id="d9e27-566">_entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-566">_entityId</span></span> | <span data-ttu-id="d9e27-567">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-567">str</span></span> | <span data-ttu-id="d9e27-568">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-568">False</span></span> | <span data-ttu-id="d9e27-569">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-569">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-570">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-570">Return Value</span></span> 
<span data-ttu-id="d9e27-571">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="d9e27-571">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="d9e27-572">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="d9e27-572">Method constructFromBuffer</span></span> 
<span data-ttu-id="d9e27-573">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="d9e27-573">Constructs SysAppEntityContext from table buffer</span></span>

     public SysAppEntityContext constructFromBuffer (Common _tableBuffer) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-574">Parameters</span></span>

| <span data-ttu-id="d9e27-575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-575">Parameter name</span></span> |  <span data-ttu-id="d9e27-576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-576">Parameter type</span></span> | <span data-ttu-id="d9e27-577">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-577">Optional</span></span> | <span data-ttu-id="d9e27-578">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-579">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="d9e27-579">_tableBuffer</span></span> | <span data-ttu-id="d9e27-580">共通</span><span class="sxs-lookup"><span data-stu-id="d9e27-580">Common</span></span> | <span data-ttu-id="d9e27-581">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-581">False</span></span> | <span data-ttu-id="d9e27-582">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="d9e27-582">table buffer forming the entity</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-583">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-583">Return Value</span></span> 
<span data-ttu-id="d9e27-584">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="d9e27-584">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="d9e27-585">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-585">Method entityName</span></span> 
<span data-ttu-id="d9e27-586">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-586">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-587">Parameters</span></span>

| <span data-ttu-id="d9e27-588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-588">Parameter name</span></span> |  <span data-ttu-id="d9e27-589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-589">Parameter type</span></span> | <span data-ttu-id="d9e27-590">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-590">Optional</span></span> | <span data-ttu-id="d9e27-591">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-592">_entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-592">_entityName</span></span> | <span data-ttu-id="d9e27-593">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-593">str</span></span> | <span data-ttu-id="d9e27-594">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-594">True</span></span> | <span data-ttu-id="d9e27-595">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-595">Entity name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-596">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-596">Return Value</span></span> 
<span data-ttu-id="d9e27-597">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-597">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="d9e27-598">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-598">Method entityId</span></span> 
<span data-ttu-id="d9e27-599">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-599">Field value on which filter applies</span></span>

     public str entityId ([str _entityId]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-600">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-600">Parameters</span></span>

| <span data-ttu-id="d9e27-601">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-601">Parameter name</span></span> |  <span data-ttu-id="d9e27-602">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-602">Parameter type</span></span> | <span data-ttu-id="d9e27-603">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-603">Optional</span></span> | <span data-ttu-id="d9e27-604">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-604">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-605">_entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-605">_entityId</span></span> | <span data-ttu-id="d9e27-606">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-606">str</span></span> | <span data-ttu-id="d9e27-607">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-607">True</span></span> | <span data-ttu-id="d9e27-608">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-608">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-609">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-609">Return Value</span></span> 
<span data-ttu-id="d9e27-610">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-610">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="d9e27-611">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-611">Class SysAppFieldAttribute</span></span> 
<span data-ttu-id="d9e27-612">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-612">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-613">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-613">Methods</span></span>

| <span data-ttu-id="d9e27-614">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-614">Method name</span></span> | <span data-ttu-id="d9e27-615">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-615">Returns</span></span> | <span data-ttu-id="d9e27-616">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-616">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-617">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-617">new</span></span> | <span data-ttu-id="d9e27-618">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-618">void</span></span> | <span data-ttu-id="d9e27-619">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-619">Creates a new instance of SysAppFieldAttribute class</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-620">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-620">Method new</span></span> 
<span data-ttu-id="d9e27-621">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-621">Creates a new instance of SysAppFieldAttribute class</span></span>

     public void new (str _fieldName, str _label) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-622">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-622">Parameters</span></span>

| <span data-ttu-id="d9e27-623">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-623">Parameter name</span></span> |  <span data-ttu-id="d9e27-624">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-624">Parameter type</span></span> | <span data-ttu-id="d9e27-625">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-625">Optional</span></span> | <span data-ttu-id="d9e27-626">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-626">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-627">_fieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-627">_fieldName</span></span> | <span data-ttu-id="d9e27-628">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-628">str</span></span> | <span data-ttu-id="d9e27-629">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-629">False</span></span> | <span data-ttu-id="d9e27-630">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-630">Entity field name with which control is bound</span></span>
| <span data-ttu-id="d9e27-631">_label</span><span class="sxs-lookup"><span data-stu-id="d9e27-631">_label</span></span> | <span data-ttu-id="d9e27-632">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-632">str</span></span> | <span data-ttu-id="d9e27-633">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-633">False</span></span> | <span data-ttu-id="d9e27-634">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-634">Control label</span></span>


## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="d9e27-635">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="d9e27-635">Class SysAppFieldMultiSelectHelper</span></span> 
<span data-ttu-id="d9e27-636">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="d9e27-636">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-637">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-637">Methods</span></span>

| <span data-ttu-id="d9e27-638">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-638">Method name</span></span> | <span data-ttu-id="d9e27-639">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-639">Returns</span></span> | <span data-ttu-id="d9e27-640">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-640">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-641">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-641">new</span></span> | <span data-ttu-id="d9e27-642">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-642">void</span></span> | <span data-ttu-id="d9e27-643">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-643">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="d9e27-644">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="d9e27-644">getSelectedRecIds</span></span> | <span data-ttu-id="d9e27-645">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-645">container</span></span> | <span data-ttu-id="d9e27-646">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-646">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="d9e27-647">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-647">getSelectedValues</span></span> | <span data-ttu-id="d9e27-648">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-648">container</span></span> | <span data-ttu-id="d9e27-649">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-649">Returns a container of selected values</span></span> |
| <span data-ttu-id="d9e27-650">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="d9e27-650">getSelectedRecords</span></span> | <span data-ttu-id="d9e27-651">共通</span><span class="sxs-lookup"><span data-stu-id="d9e27-651">Common</span></span> | <span data-ttu-id="d9e27-652">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-652">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="d9e27-653">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-653">The buffer is marked as temp..</span></span>  <span data-ttu-id="d9e27-654">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-654">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="d9e27-655">setControlValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-655">setControlValue</span></span> | <span data-ttu-id="d9e27-656">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-656">void</span></span> | <span data-ttu-id="d9e27-657">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="d9e27-657">A setter to set the multi select control value</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-658">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-658">Method new</span></span> 
<span data-ttu-id="d9e27-659">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-659">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

     public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-660">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-660">Parameters</span></span>

| <span data-ttu-id="d9e27-661">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-661">Parameter name</span></span> |  <span data-ttu-id="d9e27-662">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-662">Parameter type</span></span> | <span data-ttu-id="d9e27-663">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-663">Optional</span></span> | <span data-ttu-id="d9e27-664">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-664">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-665">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="d9e27-665">_multiSelectTableId</span></span> | <span data-ttu-id="d9e27-666">TableId</span><span class="sxs-lookup"><span data-stu-id="d9e27-666">TableId</span></span> | <span data-ttu-id="d9e27-667">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-667">False</span></span> | <span data-ttu-id="d9e27-668">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="d9e27-668">The backing tableId for the field</span></span>
| <span data-ttu-id="d9e27-669">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="d9e27-669">_valueFieldId</span></span> | <span data-ttu-id="d9e27-670">FieldId</span><span class="sxs-lookup"><span data-stu-id="d9e27-670">FieldId</span></span> | <span data-ttu-id="d9e27-671">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-671">False</span></span> | <span data-ttu-id="d9e27-672">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="d9e27-672">The fieldId for the field which will be shown in the multi select control</span></span>
| <span data-ttu-id="d9e27-673">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-673">_multiSelectControl</span></span> | <span data-ttu-id="d9e27-674">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-674">FormStringControl</span></span> | <span data-ttu-id="d9e27-675">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-675">False</span></span> | <span data-ttu-id="d9e27-676">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="d9e27-676">The string control that will be the multi select control</span></span>


### <a name="method-getselectedrecids"></a><span data-ttu-id="d9e27-677">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="d9e27-677">Method getSelectedRecIds</span></span> 
<span data-ttu-id="d9e27-678">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-678">Returns a container of recIds of the records that were selected</span></span>

     public container getSelectedRecIds () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-679">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-679">Return Value</span></span> 
<span data-ttu-id="d9e27-680">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-680">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="d9e27-681">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-681">Method getSelectedValues</span></span> 
<span data-ttu-id="d9e27-682">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-682">Returns a container of selected values</span></span>

     public container getSelectedValues () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-683">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-683">Return Value</span></span> 
<span data-ttu-id="d9e27-684">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-684">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="d9e27-685">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="d9e27-685">Method getSelectedRecords</span></span> 
<span data-ttu-id="d9e27-686">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-686">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="d9e27-687">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-687">The buffer is marked as temp..</span></span>  <span data-ttu-id="d9e27-688">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-688">Later a while-Select can be used to iterate through all the records</span></span>

     public Common getSelectedRecords () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-689">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-689">Return Value</span></span> 
<span data-ttu-id="d9e27-690">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="d9e27-690">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="d9e27-691">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-691">Method setControlValue</span></span> 
<span data-ttu-id="d9e27-692">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="d9e27-692">A setter to set the multi select control value</span></span>

     public void setControlValue (str _value) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-693">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-693">Parameters</span></span>

| <span data-ttu-id="d9e27-694">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-694">Parameter name</span></span> |  <span data-ttu-id="d9e27-695">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-695">Parameter type</span></span> | <span data-ttu-id="d9e27-696">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-696">Optional</span></span> | <span data-ttu-id="d9e27-697">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-697">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-698">_value</span><span class="sxs-lookup"><span data-stu-id="d9e27-698">_value</span></span> | <span data-ttu-id="d9e27-699">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-699">str</span></span> | <span data-ttu-id="d9e27-700">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-700">False</span></span> | <span data-ttu-id="d9e27-701">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-701">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>


## <a name="class-sysappfiltercontext"></a><span data-ttu-id="d9e27-702">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-702">Class SysAppFilterContext</span></span> 
<span data-ttu-id="d9e27-703">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-703">SysAppFilterContext class which holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-704">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-704">Methods</span></span>

| <span data-ttu-id="d9e27-705">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-705">Method name</span></span> | <span data-ttu-id="d9e27-706">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-706">Returns</span></span> | <span data-ttu-id="d9e27-707">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-707">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-708">entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-708">entityName</span></span> | <span data-ttu-id="d9e27-709">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-709">str</span></span> | <span data-ttu-id="d9e27-710">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-710">Entity name on which filter applies</span></span> |
| <span data-ttu-id="d9e27-711">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-711">filterFieldName</span></span> | <span data-ttu-id="d9e27-712">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-712">str</span></span> | <span data-ttu-id="d9e27-713">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-713">Field name on which filter applies</span></span> |
| <span data-ttu-id="d9e27-714">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="d9e27-714">filterFieldValueList</span></span> | <span data-ttu-id="d9e27-715">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-715">List</span></span> | <span data-ttu-id="d9e27-716">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-716">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="d9e27-717">演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-717">operator</span></span> | <span data-ttu-id="d9e27-718">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-718">str</span></span> | <span data-ttu-id="d9e27-719">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-719">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="d9e27-720">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-720">addFilterFieldValue</span></span> | <span data-ttu-id="d9e27-721">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-721">void</span></span> | <span data-ttu-id="d9e27-722">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-722">Adds filter field value</span></span> |


### <a name="method-entityname"></a><span data-ttu-id="d9e27-723">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-723">Method entityName</span></span> 
<span data-ttu-id="d9e27-724">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-724">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-725">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-725">Parameters</span></span>

| <span data-ttu-id="d9e27-726">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-726">Parameter name</span></span> |  <span data-ttu-id="d9e27-727">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-727">Parameter type</span></span> | <span data-ttu-id="d9e27-728">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-728">Optional</span></span> | <span data-ttu-id="d9e27-729">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-729">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-730">_entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-730">_entityName</span></span> | <span data-ttu-id="d9e27-731">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-731">str</span></span> | <span data-ttu-id="d9e27-732">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-732">True</span></span> | <span data-ttu-id="d9e27-733">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-733">Entity name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-734">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-734">Return Value</span></span> 
<span data-ttu-id="d9e27-735">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-735">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="d9e27-736">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-736">Method filterFieldName</span></span> 
<span data-ttu-id="d9e27-737">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-737">Field name on which filter applies</span></span>

     public str filterFieldName ([str _filterFieldName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-738">Parameters</span></span>

| <span data-ttu-id="d9e27-739">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-739">Parameter name</span></span> |  <span data-ttu-id="d9e27-740">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-740">Parameter type</span></span> | <span data-ttu-id="d9e27-741">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-741">Optional</span></span> | <span data-ttu-id="d9e27-742">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-742">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-743">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-743">_filterFieldName</span></span> | <span data-ttu-id="d9e27-744">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-744">str</span></span> | <span data-ttu-id="d9e27-745">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-745">True</span></span> | <span data-ttu-id="d9e27-746">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-746">Field name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-747">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-747">Return Value</span></span> 
<span data-ttu-id="d9e27-748">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-748">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="d9e27-749">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="d9e27-749">Method filterFieldValueList</span></span> 
<span data-ttu-id="d9e27-750">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-750">Gets the list of filter field values based on which filter happens</span></span>

     public List filterFieldValueList () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-751">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-751">Return Value</span></span> 
<span data-ttu-id="d9e27-752">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-752">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="d9e27-753">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="d9e27-753">Method operator</span></span> 
<span data-ttu-id="d9e27-754">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-754">Operator based on which result will be fetched</span></span>

     public str operator ([str _operator]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-755">Parameters</span></span>

| <span data-ttu-id="d9e27-756">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-756">Parameter name</span></span> |  <span data-ttu-id="d9e27-757">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-757">Parameter type</span></span> | <span data-ttu-id="d9e27-758">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-758">Optional</span></span> | <span data-ttu-id="d9e27-759">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-759">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-760">_operator</span><span class="sxs-lookup"><span data-stu-id="d9e27-760">_operator</span></span> | <span data-ttu-id="d9e27-761">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-761">str</span></span> | <span data-ttu-id="d9e27-762">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-762">True</span></span> | <span data-ttu-id="d9e27-763">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-763">Operator based on which result will be fetched</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-764">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-764">Return Value</span></span> 
<span data-ttu-id="d9e27-765">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-765">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="d9e27-766">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-766">Method addFilterFieldValue</span></span> 
<span data-ttu-id="d9e27-767">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-767">Adds filter field value</span></span>

     public void addFilterFieldValue ( _filterFieldValueList) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-768">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-768">Parameters</span></span>

| <span data-ttu-id="d9e27-769">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-769">Parameter name</span></span> |  <span data-ttu-id="d9e27-770">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-770">Parameter type</span></span> | <span data-ttu-id="d9e27-771">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-771">Optional</span></span> | <span data-ttu-id="d9e27-772">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-772">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-773">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="d9e27-773">_filterFieldValueList</span></span> |  | <span data-ttu-id="d9e27-774">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-774">False</span></span> | <span data-ttu-id="d9e27-775">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-775">Filter field values based on which filter happens</span></span>


## <a name="class-sysapplookupattribute"></a><span data-ttu-id="d9e27-776">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-776">Class SysAppLookUpAttribute</span></span> 
<span data-ttu-id="d9e27-777">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-777">SysAppPageAttribute used for decorating pages that is also lookup page</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-778">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-778">Methods</span></span>

| <span data-ttu-id="d9e27-779">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-779">Method name</span></span> | <span data-ttu-id="d9e27-780">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-780">Returns</span></span> | <span data-ttu-id="d9e27-781">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-781">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-782">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-782">new</span></span> | <span data-ttu-id="d9e27-783">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-783">void</span></span> | <span data-ttu-id="d9e27-784">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-784">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="d9e27-785">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-785">displayFieldName</span></span> | <span data-ttu-id="d9e27-786">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-786">str</span></span> | <span data-ttu-id="d9e27-787">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-787">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="d9e27-788">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-788">valueFieldName</span></span> | <span data-ttu-id="d9e27-789">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-789">str</span></span> | <span data-ttu-id="d9e27-790">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-790">Gets the value field name of lookup control</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-791">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-791">Method new</span></span> 
<span data-ttu-id="d9e27-792">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-792">Creates a new instance of SysAppLookUpAttribute class</span></span>

     public void new (str _displayFieldName, str _valueFieldName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-793">Parameters</span></span>

| <span data-ttu-id="d9e27-794">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-794">Parameter name</span></span> |  <span data-ttu-id="d9e27-795">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-795">Parameter type</span></span> | <span data-ttu-id="d9e27-796">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-796">Optional</span></span> | <span data-ttu-id="d9e27-797">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-797">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-798">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-798">_displayFieldName</span></span> | <span data-ttu-id="d9e27-799">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-799">str</span></span> | <span data-ttu-id="d9e27-800">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-800">False</span></span> | <span data-ttu-id="d9e27-801">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="d9e27-801">Lookup display field.</span></span> <span data-ttu-id="d9e27-802">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-802">Name of any control of lookup page</span></span>
| <span data-ttu-id="d9e27-803">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-803">_valueFieldName</span></span> | <span data-ttu-id="d9e27-804">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-804">str</span></span> | <span data-ttu-id="d9e27-805">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-805">False</span></span> | <span data-ttu-id="d9e27-806">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="d9e27-806">Lookup value field.</span></span> <span data-ttu-id="d9e27-807">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-807">Name of control formed by root data contract constructing lookup page</span></span>


### <a name="method-displayfieldname"></a><span data-ttu-id="d9e27-808">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-808">Method displayFieldName</span></span> 
<span data-ttu-id="d9e27-809">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-809">Gets the display field name of lookup control</span></span>

     public str displayFieldName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-810">Return Value</span></span> 
<span data-ttu-id="d9e27-811">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-811">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="d9e27-812">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-812">Method valueFieldName</span></span> 
<span data-ttu-id="d9e27-813">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-813">Gets the value field name of lookup control</span></span>

     public str valueFieldName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-814">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-814">Return Value</span></span> 
<span data-ttu-id="d9e27-815">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="d9e27-815">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="d9e27-816">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-816">Class SysAppLookupFieldAttribute</span></span> 
<span data-ttu-id="d9e27-817">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-817">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-818">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-818">Methods</span></span>

| <span data-ttu-id="d9e27-819">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-819">Method name</span></span> | <span data-ttu-id="d9e27-820">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-820">Returns</span></span> | <span data-ttu-id="d9e27-821">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-821">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-822">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-822">new</span></span> | <span data-ttu-id="d9e27-823">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-823">void</span></span> | <span data-ttu-id="d9e27-824">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-824">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="d9e27-825">entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-825">entityName</span></span> | <span data-ttu-id="d9e27-826">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-826">str</span></span> | <span data-ttu-id="d9e27-827">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-827">Gets the name of the entity with which lookup page is related</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-828">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-828">Method new</span></span> 
<span data-ttu-id="d9e27-829">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-829">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

     public void new ( _name) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-830">Parameters</span></span>

| <span data-ttu-id="d9e27-831">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-831">Parameter name</span></span> |  <span data-ttu-id="d9e27-832">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-832">Parameter type</span></span> | <span data-ttu-id="d9e27-833">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-833">Optional</span></span> | <span data-ttu-id="d9e27-834">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-834">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-835">_name</span><span class="sxs-lookup"><span data-stu-id="d9e27-835">_name</span></span> |  | <span data-ttu-id="d9e27-836">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-836">False</span></span> | <span data-ttu-id="d9e27-837">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-837">Name of the entity with which lookup page is related</span></span>


### <a name="method-entityname"></a><span data-ttu-id="d9e27-838">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-838">Method entityName</span></span> 
<span data-ttu-id="d9e27-839">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-839">Gets the name of the entity with which lookup page is related</span></span>

     public str entityName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-840">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-840">Return Value</span></span> 
<span data-ttu-id="d9e27-841">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-841">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="d9e27-842">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-842">Class SysAppPageAttribute</span></span> 
<span data-ttu-id="d9e27-843">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-843">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-844">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-844">Methods</span></span>

| <span data-ttu-id="d9e27-845">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-845">Method name</span></span> | <span data-ttu-id="d9e27-846">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-846">Returns</span></span> | <span data-ttu-id="d9e27-847">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-847">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-848">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-848">new</span></span> | <span data-ttu-id="d9e27-849">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-849">void</span></span> | <span data-ttu-id="d9e27-850">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-850">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="d9e27-851">pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-851">pageTitle</span></span> | <span data-ttu-id="d9e27-852">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-852">str</span></span> | <span data-ttu-id="d9e27-853">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-853">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="d9e27-854">pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-854">pageDescription</span></span> | <span data-ttu-id="d9e27-855">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-855">str</span></span> | <span data-ttu-id="d9e27-856">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-856">Gets the Page Description</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-857">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-857">Method new</span></span> 
<span data-ttu-id="d9e27-858">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-858">Creates a new instance of SysAppPageAttribute class</span></span>

     public void new ([str _pageTitle], [str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-859">Parameters</span></span>

| <span data-ttu-id="d9e27-860">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-860">Parameter name</span></span> |  <span data-ttu-id="d9e27-861">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-861">Parameter type</span></span> | <span data-ttu-id="d9e27-862">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-862">Optional</span></span> | <span data-ttu-id="d9e27-863">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-863">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-864">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-864">_pageTitle</span></span> | <span data-ttu-id="d9e27-865">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-865">str</span></span> | <span data-ttu-id="d9e27-866">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-866">True</span></span> | <span data-ttu-id="d9e27-867">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-867">The page title</span></span>
| <span data-ttu-id="d9e27-868">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-868">_pageDescription</span></span> | <span data-ttu-id="d9e27-869">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-869">str</span></span> | <span data-ttu-id="d9e27-870">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-870">True</span></span> | <span data-ttu-id="d9e27-871">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-871">The page description</span></span>


### <a name="method-pagetitle"></a><span data-ttu-id="d9e27-872">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-872">Method pageTitle</span></span> 
<span data-ttu-id="d9e27-873">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-873">Gets the Page Title of the page</span></span>

     public str pageTitle () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-874">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-874">Return Value</span></span> 
<span data-ttu-id="d9e27-875">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-875">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="d9e27-876">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-876">Method pageDescription</span></span> 
<span data-ttu-id="d9e27-877">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-877">Gets the Page Description</span></span>

     public str pageDescription () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-878">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-878">Return Value</span></span> 
<span data-ttu-id="d9e27-879">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-879">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="d9e27-880">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-880">Class SysAppPageMetadata</span></span> 
<span data-ttu-id="d9e27-881">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-881">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-882">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-882">Methods</span></span>

| <span data-ttu-id="d9e27-883">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-883">Method name</span></span> | <span data-ttu-id="d9e27-884">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-884">Returns</span></span> | <span data-ttu-id="d9e27-885">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-885">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-886">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-886">new</span></span> | <span data-ttu-id="d9e27-887">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-887">void</span></span> |  |
| <span data-ttu-id="d9e27-888">getPageName</span><span class="sxs-lookup"><span data-stu-id="d9e27-888">getPageName</span></span> | <span data-ttu-id="d9e27-889">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-889">str</span></span> | <span data-ttu-id="d9e27-890">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-890">Returns the page name</span></span> |
| <span data-ttu-id="d9e27-891">pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-891">pageTitle</span></span> | <span data-ttu-id="d9e27-892">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-892">str</span></span> | <span data-ttu-id="d9e27-893">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-893">Gets and sets the page title</span></span> |
| <span data-ttu-id="d9e27-894">pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-894">pageDescription</span></span> | <span data-ttu-id="d9e27-895">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-895">str</span></span> | <span data-ttu-id="d9e27-896">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-896">Gets or sets the page description</span></span> |
| <span data-ttu-id="d9e27-897">pageHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-897">pageHidden</span></span> | <span data-ttu-id="d9e27-898">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-898">boolean</span></span> | <span data-ttu-id="d9e27-899">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-899">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="d9e27-900">pageOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-900">pageOrder</span></span> | <span data-ttu-id="d9e27-901">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-901">int</span></span> | <span data-ttu-id="d9e27-902">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-902">Gets or sets the page order</span></span> |
| <span data-ttu-id="d9e27-903">getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-903">getControl</span></span> | <span data-ttu-id="d9e27-904">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-904">SysAppControlMetadata</span></span> | <span data-ttu-id="d9e27-905">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-905">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="d9e27-906">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-906">getControlEnumerator</span></span> | <span data-ttu-id="d9e27-907">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-907">MapEnumerator</span></span> | <span data-ttu-id="d9e27-908">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-908">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="d9e27-909">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-909">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-910">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-911">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-911">Parameters</span></span>

| <span data-ttu-id="d9e27-912">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-912">Parameter name</span></span> |  <span data-ttu-id="d9e27-913">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-913">Parameter type</span></span> | <span data-ttu-id="d9e27-914">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-914">Optional</span></span> | <span data-ttu-id="d9e27-915">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-915">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-916">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-916">_pageMetadata</span></span> | <span data-ttu-id="d9e27-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="d9e27-918">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-918">False</span></span> | 


### <a name="method-getpagename"></a><span data-ttu-id="d9e27-919">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="d9e27-919">Method getPageName</span></span> 
<span data-ttu-id="d9e27-920">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-920">Returns the page name</span></span>

     public str getPageName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-921">Return Value</span></span> 
<span data-ttu-id="d9e27-922">ページ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-922">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="d9e27-923">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-923">Method pageTitle</span></span> 
<span data-ttu-id="d9e27-924">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-924">Gets and sets the page title</span></span>

     public str pageTitle ([str _pageTitle]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-925">Parameters</span></span>

| <span data-ttu-id="d9e27-926">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-926">Parameter name</span></span> |  <span data-ttu-id="d9e27-927">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-927">Parameter type</span></span> | <span data-ttu-id="d9e27-928">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-928">Optional</span></span> | <span data-ttu-id="d9e27-929">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-929">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-930">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-930">_pageTitle</span></span> | <span data-ttu-id="d9e27-931">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-931">str</span></span> | <span data-ttu-id="d9e27-932">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-932">True</span></span> | <span data-ttu-id="d9e27-933">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-933">The page title</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-934">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-934">Return Value</span></span> 
<span data-ttu-id="d9e27-935">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-935">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="d9e27-936">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-936">Method pageDescription</span></span> 
<span data-ttu-id="d9e27-937">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-937">Gets or sets the page description</span></span>

     public str pageDescription ([str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-938">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-938">Parameters</span></span>

| <span data-ttu-id="d9e27-939">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-939">Parameter name</span></span> |  <span data-ttu-id="d9e27-940">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-940">Parameter type</span></span> | <span data-ttu-id="d9e27-941">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-941">Optional</span></span> | <span data-ttu-id="d9e27-942">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-942">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-943">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-943">_pageDescription</span></span> | <span data-ttu-id="d9e27-944">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-944">str</span></span> | <span data-ttu-id="d9e27-945">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-945">True</span></span> | <span data-ttu-id="d9e27-946">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-946">The page description</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-947">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-947">Return Value</span></span> 
<span data-ttu-id="d9e27-948">ページの説明></span><span class="sxs-lookup"><span data-stu-id="d9e27-948">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="d9e27-949">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-949">Method pageHidden</span></span> 
<span data-ttu-id="d9e27-950">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-950">Gets and sets whether the page is hidden in the workspace</span></span>

     public boolean pageHidden ([boolean _pageHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-951">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-951">Parameters</span></span>

| <span data-ttu-id="d9e27-952">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-952">Parameter name</span></span> |  <span data-ttu-id="d9e27-953">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-953">Parameter type</span></span> | <span data-ttu-id="d9e27-954">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-954">Optional</span></span> | <span data-ttu-id="d9e27-955">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-955">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-956">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-956">_pageHidden</span></span> | <span data-ttu-id="d9e27-957">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-957">boolean</span></span> | <span data-ttu-id="d9e27-958">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-958">True</span></span> | <span data-ttu-id="d9e27-959">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="d9e27-959">page hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-960">Return Value</span></span> 
<span data-ttu-id="d9e27-961">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="d9e27-961">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="d9e27-962">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-962">Method pageOrder</span></span> 
<span data-ttu-id="d9e27-963">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-963">Gets or sets the page order</span></span>

     public int pageOrder ([int _pageOrder]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-964">Parameters</span></span>

| <span data-ttu-id="d9e27-965">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-965">Parameter name</span></span> |  <span data-ttu-id="d9e27-966">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-966">Parameter type</span></span> | <span data-ttu-id="d9e27-967">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-967">Optional</span></span> | <span data-ttu-id="d9e27-968">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-968">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-969">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-969">_pageOrder</span></span> | <span data-ttu-id="d9e27-970">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-970">int</span></span> | <span data-ttu-id="d9e27-971">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-971">True</span></span> | <span data-ttu-id="d9e27-972">ページの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-972">The page order</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-973">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-973">Return Value</span></span> 
<span data-ttu-id="d9e27-974">ページの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-974">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="d9e27-975">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-975">Method getControl</span></span> 
<span data-ttu-id="d9e27-976">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-976">Returns the control on the current page having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-977">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-977">Parameters</span></span>

| <span data-ttu-id="d9e27-978">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-978">Parameter name</span></span> |  <span data-ttu-id="d9e27-979">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-979">Parameter type</span></span> | <span data-ttu-id="d9e27-980">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-980">Optional</span></span> | <span data-ttu-id="d9e27-981">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-981">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-982">_controlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-982">_controlName</span></span> | <span data-ttu-id="d9e27-983">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-983">str</span></span> | <span data-ttu-id="d9e27-984">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-984">False</span></span> | <span data-ttu-id="d9e27-985">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="d9e27-985">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-986">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-986">Return Value</span></span> 
<span data-ttu-id="d9e27-987">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="d9e27-987">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="d9e27-988">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-988">Method getControlEnumerator</span></span> 
<span data-ttu-id="d9e27-989">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-989">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="d9e27-990">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-990">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-991">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-991">Return Value</span></span> 
<span data-ttu-id="d9e27-992">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-992">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="d9e27-993">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-993">Class SysAppProjectionAttribute</span></span> 
<span data-ttu-id="d9e27-994">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-994">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-995">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-995">Methods</span></span>

| <span data-ttu-id="d9e27-996">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-996">Method name</span></span> | <span data-ttu-id="d9e27-997">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-997">Returns</span></span> | <span data-ttu-id="d9e27-998">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-998">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-999">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-999">new</span></span> | <span data-ttu-id="d9e27-1000">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1000">void</span></span> | <span data-ttu-id="d9e27-1001">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1001">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1002">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1002">Method new</span></span> 
<span data-ttu-id="d9e27-1003">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1003">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

     public void new (str _label) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1004">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1004">Parameters</span></span>

| <span data-ttu-id="d9e27-1005">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1005">Parameter name</span></span> |  <span data-ttu-id="d9e27-1006">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1006">Parameter type</span></span> | <span data-ttu-id="d9e27-1007">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1007">Optional</span></span> | <span data-ttu-id="d9e27-1008">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1008">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1009">_label</span><span class="sxs-lookup"><span data-stu-id="d9e27-1009">_label</span></span> | <span data-ttu-id="d9e27-1010">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1010">str</span></span> | <span data-ttu-id="d9e27-1011">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1011">False</span></span> | <span data-ttu-id="d9e27-1012">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1012">Control label</span></span>


## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="d9e27-1013">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1013">Class SysAppRelationalAttribute</span></span> 
<span data-ttu-id="d9e27-1014">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1014">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1015">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1015">Methods</span></span>

| <span data-ttu-id="d9e27-1016">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1016">Method name</span></span> | <span data-ttu-id="d9e27-1017">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1017">Returns</span></span> | <span data-ttu-id="d9e27-1018">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1018">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1019">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1019">new</span></span> | <span data-ttu-id="d9e27-1020">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1020">void</span></span> | <span data-ttu-id="d9e27-1021">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1021">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1022">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1022">Method new</span></span> 
<span data-ttu-id="d9e27-1023">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1023">Constructor</span></span>

     public void new ([str _name]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1024">Parameters</span></span>

| <span data-ttu-id="d9e27-1025">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1025">Parameter name</span></span> |  <span data-ttu-id="d9e27-1026">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1026">Parameter type</span></span> | <span data-ttu-id="d9e27-1027">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1027">Optional</span></span> | <span data-ttu-id="d9e27-1028">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1028">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1029">_name</span><span class="sxs-lookup"><span data-stu-id="d9e27-1029">_name</span></span> | <span data-ttu-id="d9e27-1030">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1030">str</span></span> | <span data-ttu-id="d9e27-1031">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1031">True</span></span> | <span data-ttu-id="d9e27-1032">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1032">Property name of the referenced entity</span></span>


## <a name="class-sysapprequestparams"></a><span data-ttu-id="d9e27-1033">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="d9e27-1033">Class SysAppRequestParams</span></span> 
<span data-ttu-id="d9e27-1034">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1034">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1035">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1035">Methods</span></span>

| <span data-ttu-id="d9e27-1036">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1036">Method name</span></span> | <span data-ttu-id="d9e27-1037">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1037">Returns</span></span> | <span data-ttu-id="d9e27-1038">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1038">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1039">entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1039">entityContext</span></span> | <span data-ttu-id="d9e27-1040">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1040">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-1041">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1041">Entity context of the request</span></span> |
| <span data-ttu-id="d9e27-1042">filterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1042">filterContext</span></span> | <span data-ttu-id="d9e27-1043">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1043">List</span></span> | <span data-ttu-id="d9e27-1044">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1044">List of SysAppFilterContext for filter contexts</span></span> |


### <a name="method-entitycontext"></a><span data-ttu-id="d9e27-1045">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1045">Method entityContext</span></span> 
<span data-ttu-id="d9e27-1046">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1046">Entity context of the request</span></span>

     public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1047">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1047">Parameters</span></span>

| <span data-ttu-id="d9e27-1048">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1048">Parameter name</span></span> |  <span data-ttu-id="d9e27-1049">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1049">Parameter type</span></span> | <span data-ttu-id="d9e27-1050">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1050">Optional</span></span> | <span data-ttu-id="d9e27-1051">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1051">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1052">_entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1052">_entityContext</span></span> | <span data-ttu-id="d9e27-1053">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1053">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-1054">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1054">True</span></span> | <span data-ttu-id="d9e27-1055">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1055">Entity context of the request</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1056">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1056">Return Value</span></span> 
<span data-ttu-id="d9e27-1057">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1057">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="d9e27-1058">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1058">Method filterContext</span></span> 
<span data-ttu-id="d9e27-1059">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1059">List of SysAppFilterContext for filter contexts</span></span>

     public List filterContext ([List _filterContext]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1060">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1060">Parameters</span></span>

| <span data-ttu-id="d9e27-1061">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1061">Parameter name</span></span> |  <span data-ttu-id="d9e27-1062">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1062">Parameter type</span></span> | <span data-ttu-id="d9e27-1063">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1063">Optional</span></span> | <span data-ttu-id="d9e27-1064">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1064">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1065">_filterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1065">_filterContext</span></span> | <span data-ttu-id="d9e27-1066">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1066">List</span></span> | <span data-ttu-id="d9e27-1067">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1067">True</span></span> | <span data-ttu-id="d9e27-1068">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1068">List of SysAppFilterContext for filter contexts of page</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1069">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1069">Return Value</span></span> 
<span data-ttu-id="d9e27-1070">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1070">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="d9e27-1071">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="d9e27-1071">Class SysAppResponse</span></span> 
<span data-ttu-id="d9e27-1072">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1072">SysAppResponse class.</span></span>  <span data-ttu-id="d9e27-1073">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1073">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1074">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1074">Methods</span></span>

| <span data-ttu-id="d9e27-1075">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1075">Method name</span></span> | <span data-ttu-id="d9e27-1076">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1076">Returns</span></span> | <span data-ttu-id="d9e27-1077">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1077">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1078">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1078">new</span></span> | <span data-ttu-id="d9e27-1079">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1079">void</span></span> |  |
| <span data-ttu-id="d9e27-1080">jobId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1080">jobId</span></span> | <span data-ttu-id="d9e27-1081">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1081">str</span></span> | <span data-ttu-id="d9e27-1082">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-1082">Job Id of the request</span></span> |
| <span data-ttu-id="d9e27-1083">データ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1083">data</span></span> | <span data-ttu-id="d9e27-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="d9e27-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="d9e27-1085">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1085">Data of the page</span></span> |
| <span data-ttu-id="d9e27-1086">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="d9e27-1086">failedInAppCall</span></span> | <span data-ttu-id="d9e27-1087">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1087">boolean</span></span> | <span data-ttu-id="d9e27-1088">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1088">Data of the page</span></span> |
| <span data-ttu-id="d9e27-1089">commits</span><span class="sxs-lookup"><span data-stu-id="d9e27-1089">commits</span></span> | <span data-ttu-id="d9e27-1090">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1090">List</span></span> | <span data-ttu-id="d9e27-1091">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1091">Commits after task is completed</span></span> |
| <span data-ttu-id="d9e27-1092">メッセージ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1092">messages</span></span> | <span data-ttu-id="d9e27-1093">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1093">List</span></span> | <span data-ttu-id="d9e27-1094">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-1094">Job Id of the request</span></span> |
| <span data-ttu-id="d9e27-1095">addMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-1095">addMessage</span></span> | <span data-ttu-id="d9e27-1096">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1096">void</span></span> | <span data-ttu-id="d9e27-1097">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-1097">Adds message</span></span> |
| <span data-ttu-id="d9e27-1098">addCommit</span><span class="sxs-lookup"><span data-stu-id="d9e27-1098">addCommit</span></span> | <span data-ttu-id="d9e27-1099">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1099">void</span></span> | <span data-ttu-id="d9e27-1100">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-1100">Adds commits</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1101">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1101">Method new</span></span> 


     public void new () 


### <a name="method-jobid"></a><span data-ttu-id="d9e27-1102">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1102">Method jobId</span></span> 
<span data-ttu-id="d9e27-1103">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-1103">Job Id of the request</span></span>

     public str jobId () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1104">Return Value</span></span> 
<span data-ttu-id="d9e27-1105">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-1105">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="d9e27-1106">メソッド data</span><span class="sxs-lookup"><span data-stu-id="d9e27-1106">Method data</span></span> 
<span data-ttu-id="d9e27-1107">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1107">Data of the page</span></span>

     public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1108">Parameters</span></span>

| <span data-ttu-id="d9e27-1109">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1109">Parameter name</span></span> |  <span data-ttu-id="d9e27-1110">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1110">Parameter type</span></span> | <span data-ttu-id="d9e27-1111">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1111">Optional</span></span> | <span data-ttu-id="d9e27-1112">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1112">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1113">_data</span><span class="sxs-lookup"><span data-stu-id="d9e27-1113">_data</span></span> | <span data-ttu-id="d9e27-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="d9e27-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="d9e27-1115">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1115">True</span></span> | <span data-ttu-id="d9e27-1116">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1116">Data of the page</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1117">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1117">Return Value</span></span> 
<span data-ttu-id="d9e27-1118">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1118">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="d9e27-1119">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="d9e27-1119">Method failedInAppCall</span></span> 
<span data-ttu-id="d9e27-1120">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1120">Data of the page</span></span>

     public boolean failedInAppCall ([boolean _failedInAppCall]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1121">Parameters</span></span>

| <span data-ttu-id="d9e27-1122">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1122">Parameter name</span></span> |  <span data-ttu-id="d9e27-1123">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1123">Parameter type</span></span> | <span data-ttu-id="d9e27-1124">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1124">Optional</span></span> | <span data-ttu-id="d9e27-1125">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1125">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1126">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="d9e27-1126">_failedInAppCall</span></span> | <span data-ttu-id="d9e27-1127">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1127">boolean</span></span> | <span data-ttu-id="d9e27-1128">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1128">True</span></span> | <span data-ttu-id="d9e27-1129">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1129">Sets to true if it fails in calling application code</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1130">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1130">Return Value</span></span> 
<span data-ttu-id="d9e27-1131">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1131">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="d9e27-1132">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="d9e27-1132">Method commits</span></span> 
<span data-ttu-id="d9e27-1133">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1133">Commits after task is completed</span></span>

     public List commits () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1134">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1134">Return Value</span></span> 
<span data-ttu-id="d9e27-1135">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1135">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="d9e27-1136">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="d9e27-1136">Method messages</span></span> 
<span data-ttu-id="d9e27-1137">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-1137">Job Id of the request</span></span>

     public List messages () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1138">Return Value</span></span> 
<span data-ttu-id="d9e27-1139">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1139">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="d9e27-1140">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-1140">Method addMessage</span></span> 
<span data-ttu-id="d9e27-1141">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-1141">Adds message</span></span>

     public void addMessage (SysAppResponseMessage _message) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1142">Parameters</span></span>

| <span data-ttu-id="d9e27-1143">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1143">Parameter name</span></span> |  <span data-ttu-id="d9e27-1144">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1144">Parameter type</span></span> | <span data-ttu-id="d9e27-1145">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1145">Optional</span></span> | <span data-ttu-id="d9e27-1146">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1146">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1147">_message</span><span class="sxs-lookup"><span data-stu-id="d9e27-1147">_message</span></span> | <span data-ttu-id="d9e27-1148">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-1148">SysAppResponseMessage</span></span> | <span data-ttu-id="d9e27-1149">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1149">False</span></span> | <span data-ttu-id="d9e27-1150">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1150">message as SysAppResponseMessage object</span></span>


### <a name="method-addcommit"></a><span data-ttu-id="d9e27-1151">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="d9e27-1151">Method addCommit</span></span> 
<span data-ttu-id="d9e27-1152">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-1152">Adds commits</span></span>

     public void addCommit (SysAppEntityContext _entityContext) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1153">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1153">Parameters</span></span>

| <span data-ttu-id="d9e27-1154">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1154">Parameter name</span></span> |  <span data-ttu-id="d9e27-1155">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1155">Parameter type</span></span> | <span data-ttu-id="d9e27-1156">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1156">Optional</span></span> | <span data-ttu-id="d9e27-1157">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1157">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1158">_entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1158">_entityContext</span></span> | <span data-ttu-id="d9e27-1159">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-1159">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-1160">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1160">False</span></span> | <span data-ttu-id="d9e27-1161">確定済のエンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1161">Entity context containing entity name and entity id of the entity that is committed</span></span>


## <a name="class-sysappresponsemessage"></a><span data-ttu-id="d9e27-1162">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-1162">Class SysAppResponseMessage</span></span> 
<span data-ttu-id="d9e27-1163">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-1163">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1164">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1164">Methods</span></span>

| <span data-ttu-id="d9e27-1165">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1165">Method name</span></span> | <span data-ttu-id="d9e27-1166">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1166">Returns</span></span> | <span data-ttu-id="d9e27-1167">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1167">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1168">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1168">new</span></span> | <span data-ttu-id="d9e27-1169">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1169">void</span></span> | <span data-ttu-id="d9e27-1170">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1170">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="d9e27-1171">テキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1171">text</span></span> | <span data-ttu-id="d9e27-1172">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1172">str</span></span> | <span data-ttu-id="d9e27-1173">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1173">Gets the message text</span></span> |
| <span data-ttu-id="d9e27-1174">タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1174">type</span></span> | <span data-ttu-id="d9e27-1175">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1175">SysAppMessageType</span></span> | <span data-ttu-id="d9e27-1176">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-1176">Gets the message type: info, error , warning</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1177">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1177">Method new</span></span> 
<span data-ttu-id="d9e27-1178">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1178">Creates a new instance of SysAppResponseMessage class</span></span>

     public void new (str _text, [SysAppMessageType _type]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1179">Parameters</span></span>

| <span data-ttu-id="d9e27-1180">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1180">Parameter name</span></span> |  <span data-ttu-id="d9e27-1181">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1181">Parameter type</span></span> | <span data-ttu-id="d9e27-1182">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1182">Optional</span></span> | <span data-ttu-id="d9e27-1183">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1183">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1184">_text</span><span class="sxs-lookup"><span data-stu-id="d9e27-1184">_text</span></span> | <span data-ttu-id="d9e27-1185">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1185">str</span></span> | <span data-ttu-id="d9e27-1186">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1186">False</span></span> | <span data-ttu-id="d9e27-1187">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1187">The message text</span></span>
| <span data-ttu-id="d9e27-1188">_type</span><span class="sxs-lookup"><span data-stu-id="d9e27-1188">_type</span></span> | <span data-ttu-id="d9e27-1189">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1189">SysAppMessageType</span></span> | <span data-ttu-id="d9e27-1190">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1190">True</span></span> | <span data-ttu-id="d9e27-1191">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-1191">Message Type: info, error , warning</span></span>


### <a name="method-text"></a><span data-ttu-id="d9e27-1192">メソッド text</span><span class="sxs-lookup"><span data-stu-id="d9e27-1192">Method text</span></span> 
<span data-ttu-id="d9e27-1193">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1193">Gets the message text</span></span>

     public str text () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1194">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1194">Return Value</span></span> 
<span data-ttu-id="d9e27-1195">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1195">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="d9e27-1196">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1196">Method type</span></span> 
<span data-ttu-id="d9e27-1197">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-1197">Gets the message type: info, error , warning</span></span>

     public SysAppMessageType type () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1198">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1198">Return Value</span></span> 
<span data-ttu-id="d9e27-1199">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-1199">The message type: info, error , warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="d9e27-1200">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1200">Class SysAppSecurityAttribute</span></span> 
<span data-ttu-id="d9e27-1201">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1201">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="d9e27-1202">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1202">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1203">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1203">Methods</span></span>

| <span data-ttu-id="d9e27-1204">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1204">Method name</span></span> | <span data-ttu-id="d9e27-1205">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1205">Returns</span></span> | <span data-ttu-id="d9e27-1206">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1206">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1207">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1207">new</span></span> | <span data-ttu-id="d9e27-1208">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1208">void</span></span> | <span data-ttu-id="d9e27-1209">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1209">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="d9e27-1210">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="d9e27-1210">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="d9e27-1211">menuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1211">menuItemType</span></span> | <span data-ttu-id="d9e27-1212">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1212">MenuItemType</span></span> | <span data-ttu-id="d9e27-1213">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1213">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="d9e27-1214">menuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1214">menuItemName</span></span> | <span data-ttu-id="d9e27-1215">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1215">MenuItemName</span></span> | <span data-ttu-id="d9e27-1216">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1216">Gets the Menu Item Name of the page</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1217">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1217">Method new</span></span> 
<span data-ttu-id="d9e27-1218">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1218">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="d9e27-1219">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="d9e27-1219">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

     public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1220">Parameters</span></span>

| <span data-ttu-id="d9e27-1221">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1221">Parameter name</span></span> |  <span data-ttu-id="d9e27-1222">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1222">Parameter type</span></span> | <span data-ttu-id="d9e27-1223">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1223">Optional</span></span> | <span data-ttu-id="d9e27-1224">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1224">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1225">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1225">_menuItemName</span></span> | <span data-ttu-id="d9e27-1226">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1226">MenuItemName</span></span> | <span data-ttu-id="d9e27-1227">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1227">True</span></span> | <span data-ttu-id="d9e27-1228">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1228">Menu Item Name of the page</span></span>
| <span data-ttu-id="d9e27-1229">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1229">_menuItemType</span></span> | <span data-ttu-id="d9e27-1230">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1230">MenuItemType</span></span> | <span data-ttu-id="d9e27-1231">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1231">True</span></span> | <span data-ttu-id="d9e27-1232">アクション、表示または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1232">Menu Item Type of the page like action, display or output</span></span>


### <a name="method-menuitemtype"></a><span data-ttu-id="d9e27-1233">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1233">Method menuItemType</span></span> 
<span data-ttu-id="d9e27-1234">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1234">Gets the Menu Item Type of the page</span></span>

     public MenuItemType menuItemType () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1235">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1235">Return Value</span></span> 
<span data-ttu-id="d9e27-1236">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1236">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="d9e27-1237">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1237">Method menuItemName</span></span> 
<span data-ttu-id="d9e27-1238">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1238">Gets the Menu Item Name of the page</span></span>

     public MenuItemName menuItemName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1239">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1239">Return Value</span></span> 
<span data-ttu-id="d9e27-1240">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1240">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="d9e27-1241">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="d9e27-1241">Class SysAppWorkspace</span></span> 
<span data-ttu-id="d9e27-1242">これは、AX モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1242">This is the base class of AX mobile workspace.</span></span> <span data-ttu-id="d9e27-1243">AX モバイル ワークスペース クラスは、このクラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1243">AX mobile workspace classes needs to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1244">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-1244">Methods</span></span>

| <span data-ttu-id="d9e27-1245">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1245">Method name</span></span> | <span data-ttu-id="d9e27-1246">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1246">Returns</span></span> | <span data-ttu-id="d9e27-1247">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1247">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1248">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-1248">getEnumValues</span></span> | <span data-ttu-id="d9e27-1249">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1249">List</span></span> | <span data-ttu-id="d9e27-1250">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1250">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-1251">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-1251">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="d9e27-1252">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1252">getWorkspaceMetadata</span></span> | <span data-ttu-id="d9e27-1253">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1253">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="d9e27-1254">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1254">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-1255">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-1255">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="d9e27-1256">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-1256">onBeginAppJob</span></span> | <span data-ttu-id="d9e27-1257">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1257">void</span></span> | <span data-ttu-id="d9e27-1258">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-1258">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="d9e27-1259">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-1259">onEndAppJob</span></span> | <span data-ttu-id="d9e27-1260">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1260">void</span></span> | <span data-ttu-id="d9e27-1261">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-1261">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="d9e27-1262">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1262">workspaceHidden</span></span> | <span data-ttu-id="d9e27-1263">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1263">boolean</span></span> | <span data-ttu-id="d9e27-1264">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1264">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="d9e27-1265">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1265">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="d9e27-1266">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1266">If the attribute is not specified on the class than it always returns false</span></span> |


### <a name="method-getenumvalues"></a><span data-ttu-id="d9e27-1267">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-1267">Method getEnumValues</span></span> 
<span data-ttu-id="d9e27-1268">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1268">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-1269">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-1269">Can be used to modify the enum values that are returned to AX mobile</span></span>

     public List getEnumValues (EnumName _enumName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1270">Parameters</span></span>

| <span data-ttu-id="d9e27-1271">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1271">Parameter name</span></span> |  <span data-ttu-id="d9e27-1272">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1272">Parameter type</span></span> | <span data-ttu-id="d9e27-1273">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1273">Optional</span></span> | <span data-ttu-id="d9e27-1274">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1274">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1275">_enumName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1275">_enumName</span></span> | <span data-ttu-id="d9e27-1276">EnumName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1276">EnumName</span></span> | <span data-ttu-id="d9e27-1277">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1277">False</span></span> | <span data-ttu-id="d9e27-1278">列挙名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1278">The enum name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1279">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1279">Return Value</span></span> 
<span data-ttu-id="d9e27-1280">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="d9e27-1280">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="d9e27-1281">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1281">Method getWorkspaceMetadata</span></span> 
<span data-ttu-id="d9e27-1282">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1282">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-1283">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-1283">Can be used to modify the workspace metadata</span></span>

     public SysAppWorkspaceMetadata getWorkspaceMetadata () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1284">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1284">Return Value</span></span> 
<span data-ttu-id="d9e27-1285">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1285">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="d9e27-1286">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-1286">Method onBeginAppJob</span></span> 
<span data-ttu-id="d9e27-1287">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-1287">Called before the start of execution of AX mobile job</span></span>

     public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1288">Parameters</span></span>

| <span data-ttu-id="d9e27-1289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1289">Parameter name</span></span> |  <span data-ttu-id="d9e27-1290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1290">Parameter type</span></span> | <span data-ttu-id="d9e27-1291">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1291">Optional</span></span> | <span data-ttu-id="d9e27-1292">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1293">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="d9e27-1293">_sysAppJobRequest</span></span> | <span data-ttu-id="d9e27-1294">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="d9e27-1294">SysAppJobRequest</span></span> | <span data-ttu-id="d9e27-1295">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1295">False</span></span> | <span data-ttu-id="d9e27-1296">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-1296">A class containing job request parameters</span></span>


### <a name="method-onendappjob"></a><span data-ttu-id="d9e27-1297">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-1297">Method onEndAppJob</span></span> 
<span data-ttu-id="d9e27-1298">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-1298">Called after the end of execution of AX mobile job</span></span>

     public void onEndAppJob (SysAppJobResponse _sysAppJobResponse) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1299">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1299">Parameters</span></span>

| <span data-ttu-id="d9e27-1300">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1300">Parameter name</span></span> |  <span data-ttu-id="d9e27-1301">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1301">Parameter type</span></span> | <span data-ttu-id="d9e27-1302">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1302">Optional</span></span> | <span data-ttu-id="d9e27-1303">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1303">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1304">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="d9e27-1304">_sysAppJobResponse</span></span> | <span data-ttu-id="d9e27-1305">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="d9e27-1305">SysAppJobResponse</span></span> | <span data-ttu-id="d9e27-1306">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1306">False</span></span> | <span data-ttu-id="d9e27-1307">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-1307">A class containing job response parameters</span></span>


### <a name="method-workspacehidden"></a><span data-ttu-id="d9e27-1308">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1308">Method workspaceHidden</span></span> 
<span data-ttu-id="d9e27-1309">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1309">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="d9e27-1310">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1310">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="d9e27-1311">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1311">If the attribute is not specified on the class than it always returns false</span></span>

     public boolean workspaceHidden () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1312">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1312">Return Value</span></span> 
<span data-ttu-id="d9e27-1313">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1313">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="d9e27-1314">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1314">Class SysAppWorkspaceAttribute</span></span> 
<span data-ttu-id="d9e27-1315">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1315">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1316">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1316">Methods</span></span>

| <span data-ttu-id="d9e27-1317">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1317">Method name</span></span> | <span data-ttu-id="d9e27-1318">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1318">Returns</span></span> | <span data-ttu-id="d9e27-1319">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1319">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1320">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1320">new</span></span> | <span data-ttu-id="d9e27-1321">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1321">void</span></span> | <span data-ttu-id="d9e27-1322">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1322">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="d9e27-1323">AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1323">AppId</span></span> | <span data-ttu-id="d9e27-1324">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1324">str</span></span> | <span data-ttu-id="d9e27-1325">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1325">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="d9e27-1326">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1326">AppResourceName</span></span> | <span data-ttu-id="d9e27-1327">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1327">str</span></span> | <span data-ttu-id="d9e27-1328">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1328">Gets or sets the AOT Resource name which contains the workspace</span></span> |
| <span data-ttu-id="d9e27-1329">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1329">WorkspaceHidden</span></span> | <span data-ttu-id="d9e27-1330">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1330">boolean</span></span> | <span data-ttu-id="d9e27-1331">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1331">Gets or sets if the workspace is hidden from designer</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1332">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1332">Method new</span></span> 
<span data-ttu-id="d9e27-1333">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1333">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

     public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1334">Parameters</span></span>

| <span data-ttu-id="d9e27-1335">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1335">Parameter name</span></span> |  <span data-ttu-id="d9e27-1336">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1336">Parameter type</span></span> | <span data-ttu-id="d9e27-1337">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1337">Optional</span></span> | <span data-ttu-id="d9e27-1338">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1338">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1339">_appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1339">_appId</span></span> | <span data-ttu-id="d9e27-1340">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1340">str</span></span> | <span data-ttu-id="d9e27-1341">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1341">False</span></span> | <span data-ttu-id="d9e27-1342">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1342">The appId of the workspace</span></span>
| <span data-ttu-id="d9e27-1343">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1343">_appResourceName</span></span> | <span data-ttu-id="d9e27-1344">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1344">str</span></span> | <span data-ttu-id="d9e27-1345">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1345">True</span></span> | <span data-ttu-id="d9e27-1346">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1346">The AOT resource name which contains the workspace</span></span>
| <span data-ttu-id="d9e27-1347">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1347">_workspaceHidden</span></span> | <span data-ttu-id="d9e27-1348">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1348">boolean</span></span> | <span data-ttu-id="d9e27-1349">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1349">True</span></span> | <span data-ttu-id="d9e27-1350">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="d9e27-1350">The workspace is hidden from designer</span></span>


### <a name="method-appid"></a><span data-ttu-id="d9e27-1351">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1351">Method AppId</span></span> 
<span data-ttu-id="d9e27-1352">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1352">Gets or sets the AppId of the workspace</span></span>

     public str AppId ([str _appId]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1353">Parameters</span></span>

| <span data-ttu-id="d9e27-1354">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1354">Parameter name</span></span> |  <span data-ttu-id="d9e27-1355">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1355">Parameter type</span></span> | <span data-ttu-id="d9e27-1356">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1356">Optional</span></span> | <span data-ttu-id="d9e27-1357">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1357">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1358">_appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1358">_appId</span></span> | <span data-ttu-id="d9e27-1359">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1359">str</span></span> | <span data-ttu-id="d9e27-1360">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1360">True</span></span> | <span data-ttu-id="d9e27-1361">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1361">The AppId of the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1362">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1362">Return Value</span></span> 
<span data-ttu-id="d9e27-1363">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1363">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="d9e27-1364">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1364">Method AppResourceName</span></span> 
<span data-ttu-id="d9e27-1365">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1365">Gets or sets the AOT Resource name which contains the workspace</span></span>

     public str AppResourceName ([str _appResourceName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1366">Parameters</span></span>

| <span data-ttu-id="d9e27-1367">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1367">Parameter name</span></span> |  <span data-ttu-id="d9e27-1368">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1368">Parameter type</span></span> | <span data-ttu-id="d9e27-1369">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1369">Optional</span></span> | <span data-ttu-id="d9e27-1370">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1370">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1371">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1371">_appResourceName</span></span> | <span data-ttu-id="d9e27-1372">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1372">str</span></span> | <span data-ttu-id="d9e27-1373">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1373">True</span></span> | <span data-ttu-id="d9e27-1374">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1374">The AOT Resource name which contains the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1375">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1375">Return Value</span></span> 
<span data-ttu-id="d9e27-1376">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1376">The AOT Resource name which contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="d9e27-1377">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1377">Method WorkspaceHidden</span></span> 
<span data-ttu-id="d9e27-1378">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1378">Gets or sets if the workspace is hidden from designer</span></span>

     public boolean WorkspaceHidden ([boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1379">Parameters</span></span>

| <span data-ttu-id="d9e27-1380">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1380">Parameter name</span></span> |  <span data-ttu-id="d9e27-1381">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1381">Parameter type</span></span> | <span data-ttu-id="d9e27-1382">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1382">Optional</span></span> | <span data-ttu-id="d9e27-1383">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1383">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1384">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1384">_workspaceHidden</span></span> | <span data-ttu-id="d9e27-1385">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1385">boolean</span></span> | <span data-ttu-id="d9e27-1386">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1386">True</span></span> | <span data-ttu-id="d9e27-1387">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="d9e27-1387">The workspace hidden</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1388">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1388">Return Value</span></span> 
<span data-ttu-id="d9e27-1389">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="d9e27-1389">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="d9e27-1390">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1390">Class SysAppWorkspaceMetadata</span></span> 
<span data-ttu-id="d9e27-1391">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1391">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1392">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-1392">Methods</span></span>

| <span data-ttu-id="d9e27-1393">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1393">Method name</span></span> | <span data-ttu-id="d9e27-1394">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1394">Returns</span></span> | <span data-ttu-id="d9e27-1395">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1395">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1396">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1396">new</span></span> | <span data-ttu-id="d9e27-1397">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1397">void</span></span> |  |
| <span data-ttu-id="d9e27-1398">addConfig</span><span class="sxs-lookup"><span data-stu-id="d9e27-1398">addConfig</span></span> | <span data-ttu-id="d9e27-1399">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1399">void</span></span> | <span data-ttu-id="d9e27-1400">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1400">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="d9e27-1401">getPage</span><span class="sxs-lookup"><span data-stu-id="d9e27-1401">getPage</span></span> | <span data-ttu-id="d9e27-1402">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1402">SysAppPageMetadata</span></span> | <span data-ttu-id="d9e27-1403">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1403">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="d9e27-1404">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1404">getPageEnumerator</span></span> | <span data-ttu-id="d9e27-1405">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1405">MapEnumerator</span></span> | <span data-ttu-id="d9e27-1406">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1406">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="d9e27-1407">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-1407">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="d9e27-1408">getAction</span><span class="sxs-lookup"><span data-stu-id="d9e27-1408">getAction</span></span> | <span data-ttu-id="d9e27-1409">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1409">SysAppActionMetadata</span></span> | <span data-ttu-id="d9e27-1410">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1410">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="d9e27-1411">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1411">getActionEnumerator</span></span> | <span data-ttu-id="d9e27-1412">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1412">MapEnumerator</span></span> | <span data-ttu-id="d9e27-1413">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1413">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="d9e27-1414">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-1414">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="d9e27-1415">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1415">getPageNameForRecordingId</span></span> | <span data-ttu-id="d9e27-1416">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1416">str</span></span> | <span data-ttu-id="d9e27-1417">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1417">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="d9e27-1418">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1418">getActionNameForRecordingId</span></span> | <span data-ttu-id="d9e27-1419">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1419">str</span></span> | <span data-ttu-id="d9e27-1420">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1420">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="d9e27-1421">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1421">workspaceTitle</span></span> | <span data-ttu-id="d9e27-1422">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1422">str</span></span> | <span data-ttu-id="d9e27-1423">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1423">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="d9e27-1424">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1424">workspaceDescription</span></span> | <span data-ttu-id="d9e27-1425">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1425">str</span></span> | <span data-ttu-id="d9e27-1426">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1426">Gets and sets the workspace description</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1427">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1427">Method new</span></span> 


     public void new (str _appId, [SysAppWorkspaceAttribute _attribute]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1428">Parameters</span></span>

| <span data-ttu-id="d9e27-1429">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1429">Parameter name</span></span> |  <span data-ttu-id="d9e27-1430">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1430">Parameter type</span></span> | <span data-ttu-id="d9e27-1431">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1431">Optional</span></span> | <span data-ttu-id="d9e27-1432">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1432">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1433">_appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1433">_appId</span></span> | <span data-ttu-id="d9e27-1434">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1434">str</span></span> | <span data-ttu-id="d9e27-1435">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1435">False</span></span> | 
| <span data-ttu-id="d9e27-1436">_attribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1436">_attribute</span></span> | <span data-ttu-id="d9e27-1437">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1437">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="d9e27-1438">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1438">True</span></span> | 


### <a name="method-addconfig"></a><span data-ttu-id="d9e27-1439">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="d9e27-1439">Method addConfig</span></span> 
<span data-ttu-id="d9e27-1440">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1440">Adds a custom config to the mobile workspace metadata</span></span>

     public void addConfig (str _configName, object _configValue) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1441">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1441">Parameters</span></span>

| <span data-ttu-id="d9e27-1442">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1442">Parameter name</span></span> |  <span data-ttu-id="d9e27-1443">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1443">Parameter type</span></span> | <span data-ttu-id="d9e27-1444">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1444">Optional</span></span> | <span data-ttu-id="d9e27-1445">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1445">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1446">_configName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1446">_configName</span></span> | <span data-ttu-id="d9e27-1447">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1447">str</span></span> | <span data-ttu-id="d9e27-1448">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1448">False</span></span> | <span data-ttu-id="d9e27-1449">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1449">A config name</span></span>
| <span data-ttu-id="d9e27-1450">_configValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-1450">_configValue</span></span> | <span data-ttu-id="d9e27-1451">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1451">object</span></span> | <span data-ttu-id="d9e27-1452">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1452">False</span></span> | <span data-ttu-id="d9e27-1453">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1453">An object of a X++ data contract class</span></span>


### <a name="method-getpage"></a><span data-ttu-id="d9e27-1454">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="d9e27-1454">Method getPage</span></span> 
<span data-ttu-id="d9e27-1455">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1455">Returns the page with the pageName provided</span></span>

     public SysAppPageMetadata getPage (str _pageName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1456">Parameters</span></span>

| <span data-ttu-id="d9e27-1457">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1457">Parameter name</span></span> |  <span data-ttu-id="d9e27-1458">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1458">Parameter type</span></span> | <span data-ttu-id="d9e27-1459">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1459">Optional</span></span> | <span data-ttu-id="d9e27-1460">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1460">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1461">_pageName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1461">_pageName</span></span> | <span data-ttu-id="d9e27-1462">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1462">str</span></span> | <span data-ttu-id="d9e27-1463">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1463">False</span></span> | <span data-ttu-id="d9e27-1464">ページ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1464">A page name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1465">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1465">Return Value</span></span> 
<span data-ttu-id="d9e27-1466">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1466">Returns the pageMetadata if a page with the provided name exist;otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="d9e27-1467">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1467">Method getPageEnumerator</span></span> 
<span data-ttu-id="d9e27-1468">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1468">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="d9e27-1469">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-1469">Where key is page name and value is of type SysAppPageMetadata</span></span>

     public MapEnumerator getPageEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1470">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1470">Return Value</span></span> 
<span data-ttu-id="d9e27-1471">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-1471">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="d9e27-1472">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="d9e27-1472">Method getAction</span></span> 
<span data-ttu-id="d9e27-1473">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1473">Returns the action with the actionName provided</span></span>

     public SysAppActionMetadata getAction (str _actionName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1474">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1474">Parameters</span></span>

| <span data-ttu-id="d9e27-1475">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1475">Parameter name</span></span> |  <span data-ttu-id="d9e27-1476">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1476">Parameter type</span></span> | <span data-ttu-id="d9e27-1477">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1477">Optional</span></span> | <span data-ttu-id="d9e27-1478">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1478">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1479">_actionName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1479">_actionName</span></span> | <span data-ttu-id="d9e27-1480">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1480">str</span></span> | <span data-ttu-id="d9e27-1481">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1481">False</span></span> | <span data-ttu-id="d9e27-1482">アクション名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1482">An action name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1483">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1483">Return Value</span></span> 
<span data-ttu-id="d9e27-1484">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1484">Returns the ActionMetadata if an action with the provided name exist;otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="d9e27-1485">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1485">Method getActionEnumerator</span></span> 
<span data-ttu-id="d9e27-1486">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1486">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="d9e27-1487">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-1487">Where key is action name and value is of type SysAppActionMetadata</span></span>

     public MapEnumerator getActionEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1488">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1488">Return Value</span></span> 
<span data-ttu-id="d9e27-1489">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-1489">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="d9e27-1490">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1490">Method getPageNameForRecordingId</span></span> 
<span data-ttu-id="d9e27-1491">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1491">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

     public str getPageNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1492">Parameters</span></span>

| <span data-ttu-id="d9e27-1493">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1493">Parameter name</span></span> |  <span data-ttu-id="d9e27-1494">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1494">Parameter type</span></span> | <span data-ttu-id="d9e27-1495">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1495">Optional</span></span> | <span data-ttu-id="d9e27-1496">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1496">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1497">_recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1497">_recordingId</span></span> | <span data-ttu-id="d9e27-1498">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1498">str</span></span> | <span data-ttu-id="d9e27-1499">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1499">False</span></span> | <span data-ttu-id="d9e27-1500">recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1500">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1501">Return Value</span></span> 
<span data-ttu-id="d9e27-1502">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1502">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="d9e27-1503">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1503">Method getActionNameForRecordingId</span></span> 
<span data-ttu-id="d9e27-1504">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1504">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

     public str getActionNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1505">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1505">Parameters</span></span>

| <span data-ttu-id="d9e27-1506">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1506">Parameter name</span></span> |  <span data-ttu-id="d9e27-1507">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1507">Parameter type</span></span> | <span data-ttu-id="d9e27-1508">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1508">Optional</span></span> | <span data-ttu-id="d9e27-1509">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1509">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1510">_recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1510">_recordingId</span></span> | <span data-ttu-id="d9e27-1511">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1511">str</span></span> | <span data-ttu-id="d9e27-1512">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1512">False</span></span> | <span data-ttu-id="d9e27-1513">recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1513">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1514">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1514">Return Value</span></span> 
<span data-ttu-id="d9e27-1515">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1515">An action name if the supplied recordingId is used by a workspace action;otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="d9e27-1516">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1516">Method workspaceTitle</span></span> 
<span data-ttu-id="d9e27-1517">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1517">Gets and sets the workspace title</span></span>

     public str workspaceTitle ([str _workspaceTitle]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1518">Parameters</span></span>

| <span data-ttu-id="d9e27-1519">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1519">Parameter name</span></span> |  <span data-ttu-id="d9e27-1520">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1520">Parameter type</span></span> | <span data-ttu-id="d9e27-1521">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1521">Optional</span></span> | <span data-ttu-id="d9e27-1522">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1522">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1523">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1523">_workspaceTitle</span></span> | <span data-ttu-id="d9e27-1524">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1524">str</span></span> | <span data-ttu-id="d9e27-1525">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1525">True</span></span> | <span data-ttu-id="d9e27-1526">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1526">The workspace title</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1527">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1527">Return Value</span></span> 
<span data-ttu-id="d9e27-1528">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1528">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="d9e27-1529">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1529">Method workspaceDescription</span></span> 
<span data-ttu-id="d9e27-1530">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1530">Gets and sets the workspace description</span></span>

     public str workspaceDescription ([str _workspaceDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1531">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1531">Parameters</span></span>

| <span data-ttu-id="d9e27-1532">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1532">Parameter name</span></span> |  <span data-ttu-id="d9e27-1533">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1533">Parameter type</span></span> | <span data-ttu-id="d9e27-1534">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1534">Optional</span></span> | <span data-ttu-id="d9e27-1535">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1535">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1536">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1536">_workspaceDescription</span></span> | <span data-ttu-id="d9e27-1537">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1537">str</span></span> | <span data-ttu-id="d9e27-1538">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1538">True</span></span> | <span data-ttu-id="d9e27-1539">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1539">The workspace description</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1540">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1540">Return Value</span></span> 
<span data-ttu-id="d9e27-1541">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1541">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="d9e27-1542">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1542">Class SysAppWorkspaceSecurityAttribute</span></span> 
<span data-ttu-id="d9e27-1543">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1543">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1544">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1544">Methods</span></span>

| <span data-ttu-id="d9e27-1545">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1545">Method name</span></span> | <span data-ttu-id="d9e27-1546">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1546">Returns</span></span> | <span data-ttu-id="d9e27-1547">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1547">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1548">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1548">new</span></span> | <span data-ttu-id="d9e27-1549">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1549">void</span></span> | <span data-ttu-id="d9e27-1550">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="d9e27-1550">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="d9e27-1551">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1551">WorkspaceMenuItemName</span></span> | <span data-ttu-id="d9e27-1552">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1552">MenuItemName</span></span> | <span data-ttu-id="d9e27-1553">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1553">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="d9e27-1554">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1554">WorkspaceMenuItemType</span></span> | <span data-ttu-id="d9e27-1555">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1555">MenuItemType</span></span> | <span data-ttu-id="d9e27-1556">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1556">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1557">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1557">Method new</span></span> 
<span data-ttu-id="d9e27-1558">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="d9e27-1558">Creates a new instance of attribute</span></span>

     public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1559">Parameters</span></span>

| <span data-ttu-id="d9e27-1560">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1560">Parameter name</span></span> |  <span data-ttu-id="d9e27-1561">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1561">Parameter type</span></span> | <span data-ttu-id="d9e27-1562">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1562">Optional</span></span> | <span data-ttu-id="d9e27-1563">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1563">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1564">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1564">_workspaceMenuItemName</span></span> | <span data-ttu-id="d9e27-1565">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1565">MenuItemName</span></span> | <span data-ttu-id="d9e27-1566">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1566">False</span></span> | <span data-ttu-id="d9e27-1567">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1567">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="d9e27-1568">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1568">_workspaceMenuItemType</span></span> | <span data-ttu-id="d9e27-1569">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1569">MenuItemType</span></span> | <span data-ttu-id="d9e27-1570">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1570">True</span></span> | <span data-ttu-id="d9e27-1571">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1571">The menu item type</span></span>


### <a name="method-workspacemenuitemname"></a><span data-ttu-id="d9e27-1572">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1572">Method WorkspaceMenuItemName</span></span> 
<span data-ttu-id="d9e27-1573">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1573">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

     public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1574">Parameters</span></span>

| <span data-ttu-id="d9e27-1575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1575">Parameter name</span></span> |  <span data-ttu-id="d9e27-1576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1576">Parameter type</span></span> | <span data-ttu-id="d9e27-1577">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1577">Optional</span></span> | <span data-ttu-id="d9e27-1578">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1579">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1579">_workspaceMenuItemName</span></span> | <span data-ttu-id="d9e27-1580">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1580">MenuItemName</span></span> | <span data-ttu-id="d9e27-1581">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1581">True</span></span> | <span data-ttu-id="d9e27-1582">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="d9e27-1582">The workspace menu item for the workspace security attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1583">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1583">Return Value</span></span> 
<span data-ttu-id="d9e27-1584">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="d9e27-1584">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="d9e27-1585">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1585">Method WorkspaceMenuItemType</span></span> 
<span data-ttu-id="d9e27-1586">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1586">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

     public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1587">Parameters</span></span>

| <span data-ttu-id="d9e27-1588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1588">Parameter name</span></span> |  <span data-ttu-id="d9e27-1589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1589">Parameter type</span></span> | <span data-ttu-id="d9e27-1590">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1590">Optional</span></span> | <span data-ttu-id="d9e27-1591">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1592">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1592">_workspaceMenuItemType</span></span> | <span data-ttu-id="d9e27-1593">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1593">MenuItemType</span></span> | <span data-ttu-id="d9e27-1594">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1594">True</span></span> | <span data-ttu-id="d9e27-1595">workspacesecurity 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1595">The workspace menu item type for the workspacesecurity attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1596">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1596">Return Value</span></span> 
<span data-ttu-id="d9e27-1597">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1597">The workspace menu item type for the workspace security attribute</span></span>

## <a name="class-sysappactionattribute"></a><span data-ttu-id="d9e27-1598">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1598">Class SysAppActionAttribute</span></span> 
<span data-ttu-id="d9e27-1599">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1599">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1600">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1600">Methods</span></span>

| <span data-ttu-id="d9e27-1601">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1601">Method name</span></span> | <span data-ttu-id="d9e27-1602">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1602">Returns</span></span> | <span data-ttu-id="d9e27-1603">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1603">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1604">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1604">new</span></span> | <span data-ttu-id="d9e27-1605">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1605">void</span></span> | <span data-ttu-id="d9e27-1606">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1606">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="d9e27-1607">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1607">pageMethodName</span></span> | <span data-ttu-id="d9e27-1608">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1608">str</span></span> | <span data-ttu-id="d9e27-1609">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1609">Gets the get method name which forms the page under which this task resides</span></span> |
| <span data-ttu-id="d9e27-1610">actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1610">actionTitle</span></span> | <span data-ttu-id="d9e27-1611">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1611">str</span></span> | <span data-ttu-id="d9e27-1612">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1612">Gets the Action Title</span></span> |
| <span data-ttu-id="d9e27-1613">actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1613">actionDescription</span></span> | <span data-ttu-id="d9e27-1614">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1614">str</span></span> | <span data-ttu-id="d9e27-1615">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1615">Gets the Action Description</span></span> |
| <span data-ttu-id="d9e27-1616">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1616">crudOperationType</span></span> | <span data-ttu-id="d9e27-1617">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="d9e27-1617">SysAppCRUDOperation</span></span> | <span data-ttu-id="d9e27-1618">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1618">Gets the Crud Operation Type like Create, Update, Delete</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1619">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1619">Method new</span></span> 
<span data-ttu-id="d9e27-1620">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1620">Creates a new instance of SysAppActionAttribute class</span></span>

     public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1621">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1621">Parameters</span></span>

| <span data-ttu-id="d9e27-1622">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1622">Parameter name</span></span> |  <span data-ttu-id="d9e27-1623">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1623">Parameter type</span></span> | <span data-ttu-id="d9e27-1624">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1624">Optional</span></span> | <span data-ttu-id="d9e27-1625">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1625">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1626">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1626">_actionTitle</span></span> | <span data-ttu-id="d9e27-1627">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1627">str</span></span> | <span data-ttu-id="d9e27-1628">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1628">True</span></span> | <span data-ttu-id="d9e27-1629">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1629">Action title</span></span>
| <span data-ttu-id="d9e27-1630">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1630">_actionDescription</span></span> | <span data-ttu-id="d9e27-1631">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1631">str</span></span> | <span data-ttu-id="d9e27-1632">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1632">True</span></span> | <span data-ttu-id="d9e27-1633">アクション説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1633">Action description</span></span>
| <span data-ttu-id="d9e27-1634">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1634">_crudOperationType</span></span> | <span data-ttu-id="d9e27-1635">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="d9e27-1635">SysAppCRUDOperation</span></span> | <span data-ttu-id="d9e27-1636">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1636">True</span></span> | <span data-ttu-id="d9e27-1637">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="d9e27-1637">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="d9e27-1638">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1638">_pageMethodName</span></span> | <span data-ttu-id="d9e27-1639">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1639">str</span></span> | <span data-ttu-id="d9e27-1640">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1640">True</span></span> | <span data-ttu-id="d9e27-1641">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-1641">Name of the method constructing parent page</span></span>


### <a name="method-pagemethodname"></a><span data-ttu-id="d9e27-1642">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1642">Method pageMethodName</span></span> 
<span data-ttu-id="d9e27-1643">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1643">Gets the get method name which forms the page under which this task resides</span></span>

     public str pageMethodName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1644">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1644">Return Value</span></span> 
<span data-ttu-id="d9e27-1645">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1645">The page method name which forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="d9e27-1646">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1646">Method actionTitle</span></span> 
<span data-ttu-id="d9e27-1647">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1647">Gets the Action Title</span></span>

     public str actionTitle () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1648">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1648">Return Value</span></span> 
<span data-ttu-id="d9e27-1649">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1649">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="d9e27-1650">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1650">Method actionDescription</span></span> 
<span data-ttu-id="d9e27-1651">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1651">Gets the Action Description</span></span>

     public str actionDescription () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1652">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1652">Return Value</span></span> 
<span data-ttu-id="d9e27-1653">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1653">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="d9e27-1654">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1654">Method crudOperationType</span></span> 
<span data-ttu-id="d9e27-1655">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-1655">Gets the Crud Operation Type like Create, Update, Delete</span></span>

     public SysAppCRUDOperation crudOperationType () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1656">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1656">Return Value</span></span> 
<span data-ttu-id="d9e27-1657">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1657">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="d9e27-1658">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1658">Class SysAppActionMetadata</span></span> 
<span data-ttu-id="d9e27-1659">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1659">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1660">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-1660">Methods</span></span>

| <span data-ttu-id="d9e27-1661">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1661">Method name</span></span> | <span data-ttu-id="d9e27-1662">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1662">Returns</span></span> | <span data-ttu-id="d9e27-1663">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1663">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1664">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1664">new</span></span> | <span data-ttu-id="d9e27-1665">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1665">void</span></span> |  |
| <span data-ttu-id="d9e27-1666">getActionName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1666">getActionName</span></span> | <span data-ttu-id="d9e27-1667">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1667">str</span></span> | <span data-ttu-id="d9e27-1668">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1668">Returns the action name</span></span> |
| <span data-ttu-id="d9e27-1669">actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1669">actionTitle</span></span> | <span data-ttu-id="d9e27-1670">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1670">str</span></span> | <span data-ttu-id="d9e27-1671">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1671">Gets or sets the action title</span></span> |
| <span data-ttu-id="d9e27-1672">actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1672">actionDescription</span></span> | <span data-ttu-id="d9e27-1673">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1673">str</span></span> | <span data-ttu-id="d9e27-1674">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1674">Gets or sets the action description</span></span> |
| <span data-ttu-id="d9e27-1675">actionHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1675">actionHidden</span></span> | <span data-ttu-id="d9e27-1676">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1676">boolean</span></span> | <span data-ttu-id="d9e27-1677">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1677">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="d9e27-1678">actionOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-1678">actionOrder</span></span> | <span data-ttu-id="d9e27-1679">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-1679">int</span></span> | <span data-ttu-id="d9e27-1680">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1680">Gets or sets the action order</span></span> |
| <span data-ttu-id="d9e27-1681">getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-1681">getControl</span></span> | <span data-ttu-id="d9e27-1682">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1682">SysAppControlMetadata</span></span> | <span data-ttu-id="d9e27-1683">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1683">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="d9e27-1684">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1684">getControlEnumerator</span></span> | <span data-ttu-id="d9e27-1685">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1685">MapEnumerator</span></span> | <span data-ttu-id="d9e27-1686">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1686">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="d9e27-1687">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-1687">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1688">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1688">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1689">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1689">Parameters</span></span>

| <span data-ttu-id="d9e27-1690">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1690">Parameter name</span></span> |  <span data-ttu-id="d9e27-1691">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1691">Parameter type</span></span> | <span data-ttu-id="d9e27-1692">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1692">Optional</span></span> | <span data-ttu-id="d9e27-1693">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1693">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1694">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1694">_taskmetadata</span></span> | <span data-ttu-id="d9e27-1695">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1695">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="d9e27-1696">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1696">False</span></span> | 


### <a name="method-getactionname"></a><span data-ttu-id="d9e27-1697">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1697">Method getActionName</span></span> 
<span data-ttu-id="d9e27-1698">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1698">Returns the action name</span></span>

     public str getActionName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1699">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1699">Return Value</span></span> 
<span data-ttu-id="d9e27-1700">アクション名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1700">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="d9e27-1701">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1701">Method actionTitle</span></span> 
<span data-ttu-id="d9e27-1702">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1702">Gets or sets the action title</span></span>

     public str actionTitle ([str _actionTitle]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1703">Parameters</span></span>

| <span data-ttu-id="d9e27-1704">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1704">Parameter name</span></span> |  <span data-ttu-id="d9e27-1705">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1705">Parameter type</span></span> | <span data-ttu-id="d9e27-1706">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1706">Optional</span></span> | <span data-ttu-id="d9e27-1707">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1707">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1708">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-1708">_actionTitle</span></span> | <span data-ttu-id="d9e27-1709">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1709">str</span></span> | <span data-ttu-id="d9e27-1710">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1710">True</span></span> | <span data-ttu-id="d9e27-1711">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1711">The action title</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1712">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1712">Return Value</span></span> 
<span data-ttu-id="d9e27-1713">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1713">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="d9e27-1714">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1714">Method actionDescription</span></span> 
<span data-ttu-id="d9e27-1715">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1715">Gets or sets the action description</span></span>

     public str actionDescription ([str _actionDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1716">Parameters</span></span>

| <span data-ttu-id="d9e27-1717">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1717">Parameter name</span></span> |  <span data-ttu-id="d9e27-1718">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1718">Parameter type</span></span> | <span data-ttu-id="d9e27-1719">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1719">Optional</span></span> | <span data-ttu-id="d9e27-1720">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1720">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1721">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-1721">_actionDescription</span></span> | <span data-ttu-id="d9e27-1722">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1722">str</span></span> | <span data-ttu-id="d9e27-1723">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1723">True</span></span> | <span data-ttu-id="d9e27-1724">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1724">The action description</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1725">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1725">Return Value</span></span> 
<span data-ttu-id="d9e27-1726">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1726">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="d9e27-1727">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1727">Method actionHidden</span></span> 
<span data-ttu-id="d9e27-1728">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1728">Gets or sets whether action is hidden</span></span>

     public boolean actionHidden ([boolean _actionHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1729">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1729">Parameters</span></span>

| <span data-ttu-id="d9e27-1730">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1730">Parameter name</span></span> |  <span data-ttu-id="d9e27-1731">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1731">Parameter type</span></span> | <span data-ttu-id="d9e27-1732">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1732">Optional</span></span> | <span data-ttu-id="d9e27-1733">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1733">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1734">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1734">_actionHidden</span></span> | <span data-ttu-id="d9e27-1735">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1735">boolean</span></span> | <span data-ttu-id="d9e27-1736">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1736">True</span></span> | <span data-ttu-id="d9e27-1737">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1737">Action hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1738">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1738">Return Value</span></span> 
<span data-ttu-id="d9e27-1739">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1739">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="d9e27-1740">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-1740">Method actionOrder</span></span> 
<span data-ttu-id="d9e27-1741">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1741">Gets or sets the action order</span></span>

     public int actionOrder ([int _actionOrder]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1742">Parameters</span></span>

| <span data-ttu-id="d9e27-1743">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1743">Parameter name</span></span> |  <span data-ttu-id="d9e27-1744">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1744">Parameter type</span></span> | <span data-ttu-id="d9e27-1745">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1745">Optional</span></span> | <span data-ttu-id="d9e27-1746">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1746">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1747">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-1747">_actionOrder</span></span> | <span data-ttu-id="d9e27-1748">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-1748">int</span></span> | <span data-ttu-id="d9e27-1749">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1749">True</span></span> | <span data-ttu-id="d9e27-1750">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-1750">The action order</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1751">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1751">Return Value</span></span> 
<span data-ttu-id="d9e27-1752">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-1752">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="d9e27-1753">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-1753">Method getControl</span></span> 
<span data-ttu-id="d9e27-1754">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1754">Returns the control on the current action having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1755">Parameters</span></span>

| <span data-ttu-id="d9e27-1756">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1756">Parameter name</span></span> |  <span data-ttu-id="d9e27-1757">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1757">Parameter type</span></span> | <span data-ttu-id="d9e27-1758">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1758">Optional</span></span> | <span data-ttu-id="d9e27-1759">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1759">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1760">_controlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1760">_controlName</span></span> | <span data-ttu-id="d9e27-1761">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1761">str</span></span> | <span data-ttu-id="d9e27-1762">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1762">False</span></span> | <span data-ttu-id="d9e27-1763">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1763">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1764">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1764">Return Value</span></span> 
<span data-ttu-id="d9e27-1765">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="d9e27-1765">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action;otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="d9e27-1766">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-1766">Method getControlEnumerator</span></span> 
<span data-ttu-id="d9e27-1767">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1767">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="d9e27-1768">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-1768">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1769">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1769">Return Value</span></span> 
<span data-ttu-id="d9e27-1770">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-1770">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="d9e27-1771">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="d9e27-1771">Class SysAppAttributeHelper</span></span> 
<span data-ttu-id="d9e27-1772">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-1772">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1773">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1773">Methods</span></span>

| <span data-ttu-id="d9e27-1774">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1774">Method name</span></span> | <span data-ttu-id="d9e27-1775">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1775">Returns</span></span> | <span data-ttu-id="d9e27-1776">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1776">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1777">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-1777">getAttributeFromClass</span></span> | <span data-ttu-id="d9e27-1778">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1778">SysAttribute</span></span> | <span data-ttu-id="d9e27-1779">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1779">gets attribute from class</span></span> |


### <a name="method-getattributefromclass"></a><span data-ttu-id="d9e27-1780">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-1780">Method getAttributeFromClass</span></span> 
<span data-ttu-id="d9e27-1781">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1781">gets attribute from class</span></span>

     public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1782">Parameters</span></span>

| <span data-ttu-id="d9e27-1783">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1783">Parameter name</span></span> |  <span data-ttu-id="d9e27-1784">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1784">Parameter type</span></span> | <span data-ttu-id="d9e27-1785">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1785">Optional</span></span> | <span data-ttu-id="d9e27-1786">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1786">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1787">_sysClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-1787">_sysClass</span></span> | <span data-ttu-id="d9e27-1788">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="d9e27-1788">SysDictClass</span></span> | <span data-ttu-id="d9e27-1789">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1789">False</span></span> | <span data-ttu-id="d9e27-1790">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-1790">class for which attributes is required</span></span>
| <span data-ttu-id="d9e27-1791">_attributeType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1791">_attributeType</span></span> | <span data-ttu-id="d9e27-1792">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="d9e27-1792">SysAppAttributeType</span></span> | <span data-ttu-id="d9e27-1793">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1793">False</span></span> | <span data-ttu-id="d9e27-1794">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="d9e27-1794">Type of attribute like SysAppEntityAttribute</span></span>


## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="d9e27-1795">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1795">Class SysAppCollectionAttribute</span></span> 
<span data-ttu-id="d9e27-1796">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1796">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1797">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1797">Methods</span></span>

| <span data-ttu-id="d9e27-1798">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1798">Method name</span></span> | <span data-ttu-id="d9e27-1799">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1799">Returns</span></span> | <span data-ttu-id="d9e27-1800">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1800">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1801">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1801">new</span></span> | <span data-ttu-id="d9e27-1802">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1802">void</span></span> | <span data-ttu-id="d9e27-1803">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1803">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1804">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1804">Method new</span></span> 
<span data-ttu-id="d9e27-1805">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1805">Constructor</span></span>

     public void new (str _itemContractName, [str _label], [str _relationshipName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1806">Parameters</span></span>

| <span data-ttu-id="d9e27-1807">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1807">Parameter name</span></span> |  <span data-ttu-id="d9e27-1808">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1808">Parameter type</span></span> | <span data-ttu-id="d9e27-1809">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1809">Optional</span></span> | <span data-ttu-id="d9e27-1810">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1810">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1811">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1811">_itemContractName</span></span> | <span data-ttu-id="d9e27-1812">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1812">str</span></span> | <span data-ttu-id="d9e27-1813">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1813">False</span></span> | <span data-ttu-id="d9e27-1814">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1814">Data contract name of list item</span></span>
| <span data-ttu-id="d9e27-1815">_label</span><span class="sxs-lookup"><span data-stu-id="d9e27-1815">_label</span></span> | <span data-ttu-id="d9e27-1816">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1816">str</span></span> | <span data-ttu-id="d9e27-1817">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1817">True</span></span> | <span data-ttu-id="d9e27-1818">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1818">List control label</span></span>
| <span data-ttu-id="d9e27-1819">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1819">_relationshipName</span></span> | <span data-ttu-id="d9e27-1820">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1820">str</span></span> | <span data-ttu-id="d9e27-1821">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1821">True</span></span> | <span data-ttu-id="d9e27-1822">関係名。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1822">Relationship name.</span></span> <span data-ttu-id="d9e27-1823">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1823">By default the entity name of the list item is used as relationship name</span></span>


## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="d9e27-1824">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1824">Class SysAppControlMetadata</span></span> 
<span data-ttu-id="d9e27-1825">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1825">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="d9e27-1826">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="d9e27-1826">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1827">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1827">Methods</span></span>

| <span data-ttu-id="d9e27-1828">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1828">Method name</span></span> | <span data-ttu-id="d9e27-1829">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1829">Returns</span></span> | <span data-ttu-id="d9e27-1830">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1830">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1831">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1831">new</span></span> | <span data-ttu-id="d9e27-1832">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1832">void</span></span> | <span data-ttu-id="d9e27-1833">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1833">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="d9e27-1834">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1834">getBaseLanguageId</span></span> | <span data-ttu-id="d9e27-1835">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1835">str</span></span> | <span data-ttu-id="d9e27-1836">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1836">Returns the base language id for the app</span></span> |
| <span data-ttu-id="d9e27-1837">getControlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1837">getControlName</span></span> | <span data-ttu-id="d9e27-1838">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1838">str</span></span> | <span data-ttu-id="d9e27-1839">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1839">Returns the control name</span></span> |
| <span data-ttu-id="d9e27-1840">controlLabel</span><span class="sxs-lookup"><span data-stu-id="d9e27-1840">controlLabel</span></span> | <span data-ttu-id="d9e27-1841">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1841">str</span></span> | <span data-ttu-id="d9e27-1842">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1842">Gets and sets the control label</span></span> |
| <span data-ttu-id="d9e27-1843">controlHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1843">controlHidden</span></span> | <span data-ttu-id="d9e27-1844">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1844">boolean</span></span> | <span data-ttu-id="d9e27-1845">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1845">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="d9e27-1846">controlOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-1846">controlOrder</span></span> | <span data-ttu-id="d9e27-1847">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-1847">int</span></span> | <span data-ttu-id="d9e27-1848">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1848">Gets or sets the control order</span></span> |
| <span data-ttu-id="d9e27-1849">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="d9e27-1849">controlMandatory</span></span> | <span data-ttu-id="d9e27-1850">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1850">boolean</span></span> | <span data-ttu-id="d9e27-1851">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1851">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="d9e27-1852">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="d9e27-1852">controlAllowNegative</span></span> | <span data-ttu-id="d9e27-1853">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1853">boolean</span></span> | <span data-ttu-id="d9e27-1854">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1854">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="d9e27-1855">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="d9e27-1855">controlMaxLength</span></span> | <span data-ttu-id="d9e27-1856">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-1856">int</span></span> | <span data-ttu-id="d9e27-1857">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1857">Gets or sets the control max length</span></span> |
| <span data-ttu-id="d9e27-1858">getProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-1858">getProperty</span></span> | <span data-ttu-id="d9e27-1859">anytype</span><span class="sxs-lookup"><span data-stu-id="d9e27-1859">anytype</span></span> | <span data-ttu-id="d9e27-1860">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1860">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="d9e27-1861">setProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-1861">setProperty</span></span> | <span data-ttu-id="d9e27-1862">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-1862">void</span></span> | <span data-ttu-id="d9e27-1863">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1863">Sets the control property referenced by the key</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-1864">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-1864">Method new</span></span> 
<span data-ttu-id="d9e27-1865">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-1865">Creates a new instance of the control metadata</span></span>

     public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1866">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1866">Parameters</span></span>

| <span data-ttu-id="d9e27-1867">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1867">Parameter name</span></span> |  <span data-ttu-id="d9e27-1868">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1868">Parameter type</span></span> | <span data-ttu-id="d9e27-1869">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1869">Optional</span></span> | <span data-ttu-id="d9e27-1870">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1870">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1871">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1871">_controlMetadata</span></span> | <span data-ttu-id="d9e27-1872">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-1872">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="d9e27-1873">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1873">False</span></span> | <span data-ttu-id="d9e27-1874">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-1874">The controlMetadata object</span></span>
| <span data-ttu-id="d9e27-1875">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1875">_baseLanguageId</span></span> | <span data-ttu-id="d9e27-1876">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1876">str</span></span> | <span data-ttu-id="d9e27-1877">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1877">True</span></span> | <span data-ttu-id="d9e27-1878">基本言語</span><span class="sxs-lookup"><span data-stu-id="d9e27-1878">The base language</span></span>


### <a name="method-getbaselanguageid"></a><span data-ttu-id="d9e27-1879">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="d9e27-1879">Method getBaseLanguageId</span></span> 
<span data-ttu-id="d9e27-1880">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1880">Returns the base language id for the app</span></span>

     public str getBaseLanguageId () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1881">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1881">Return Value</span></span> 
<span data-ttu-id="d9e27-1882">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-1882">The base language id</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="d9e27-1883">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-1883">Method getControlName</span></span> 
<span data-ttu-id="d9e27-1884">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1884">Returns the control name</span></span>

     public str getControlName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-1885">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1885">Return Value</span></span> 
<span data-ttu-id="d9e27-1886">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1886">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="d9e27-1887">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="d9e27-1887">Method controlLabel</span></span> 
<span data-ttu-id="d9e27-1888">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1888">Gets and sets the control label</span></span>

     public str controlLabel ([str _controlLabel]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1889">Parameters</span></span>

| <span data-ttu-id="d9e27-1890">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1890">Parameter name</span></span> |  <span data-ttu-id="d9e27-1891">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1891">Parameter type</span></span> | <span data-ttu-id="d9e27-1892">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1892">Optional</span></span> | <span data-ttu-id="d9e27-1893">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1893">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1894">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="d9e27-1894">_controlLabel</span></span> | <span data-ttu-id="d9e27-1895">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1895">str</span></span> | <span data-ttu-id="d9e27-1896">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1896">True</span></span> | <span data-ttu-id="d9e27-1897">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1897">The control label</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1898">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1898">Return Value</span></span> 
<span data-ttu-id="d9e27-1899">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-1899">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="d9e27-1900">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1900">Method controlHidden</span></span> 
<span data-ttu-id="d9e27-1901">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1901">Gets and sets whether the control is hidden</span></span>

     public boolean controlHidden ([boolean _controlHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1902">Parameters</span></span>

| <span data-ttu-id="d9e27-1903">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1903">Parameter name</span></span> |  <span data-ttu-id="d9e27-1904">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1904">Parameter type</span></span> | <span data-ttu-id="d9e27-1905">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1905">Optional</span></span> | <span data-ttu-id="d9e27-1906">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1906">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1907">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-1907">_controlHidden</span></span> | <span data-ttu-id="d9e27-1908">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1908">boolean</span></span> | <span data-ttu-id="d9e27-1909">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1909">True</span></span> | <span data-ttu-id="d9e27-1910">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="d9e27-1910">Control hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1911">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1911">Return Value</span></span> 
<span data-ttu-id="d9e27-1912">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1912">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="d9e27-1913">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-1913">Method controlOrder</span></span> 
<span data-ttu-id="d9e27-1914">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1914">Gets or sets the control order</span></span>

     public int controlOrder ([int _controlOrder]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1915">Parameters</span></span>

| <span data-ttu-id="d9e27-1916">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1916">Parameter name</span></span> |  <span data-ttu-id="d9e27-1917">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1917">Parameter type</span></span> | <span data-ttu-id="d9e27-1918">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1918">Optional</span></span> | <span data-ttu-id="d9e27-1919">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1919">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1920">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-1920">_controlOrder</span></span> | <span data-ttu-id="d9e27-1921">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-1921">int</span></span> | <span data-ttu-id="d9e27-1922">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1922">True</span></span> | <span data-ttu-id="d9e27-1923">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-1923">The control order</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1924">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1924">Return Value</span></span> 
<span data-ttu-id="d9e27-1925">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-1925">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="d9e27-1926">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="d9e27-1926">Method controlMandatory</span></span> 
<span data-ttu-id="d9e27-1927">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1927">Gets or sets the control mandatory</span></span>

     public boolean controlMandatory ([boolean _controlMandatory]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1928">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1928">Parameters</span></span>

| <span data-ttu-id="d9e27-1929">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1929">Parameter name</span></span> |  <span data-ttu-id="d9e27-1930">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1930">Parameter type</span></span> | <span data-ttu-id="d9e27-1931">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1931">Optional</span></span> | <span data-ttu-id="d9e27-1932">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1932">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1933">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="d9e27-1933">_controlMandatory</span></span> | <span data-ttu-id="d9e27-1934">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1934">boolean</span></span> | <span data-ttu-id="d9e27-1935">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1935">True</span></span> | <span data-ttu-id="d9e27-1936">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="d9e27-1936">The control mandatory</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1937">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1937">Return Value</span></span> 
<span data-ttu-id="d9e27-1938">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="d9e27-1938">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="d9e27-1939">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="d9e27-1939">Method controlAllowNegative</span></span> 
<span data-ttu-id="d9e27-1940">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="d9e27-1940">Gets or sets the control allow negative</span></span>

     public boolean controlAllowNegative ([boolean _controlAllowNegative]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1941">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1941">Parameters</span></span>

| <span data-ttu-id="d9e27-1942">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1942">Parameter name</span></span> |  <span data-ttu-id="d9e27-1943">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1943">Parameter type</span></span> | <span data-ttu-id="d9e27-1944">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1944">Optional</span></span> | <span data-ttu-id="d9e27-1945">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1945">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1946">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="d9e27-1946">_controlAllowNegative</span></span> | <span data-ttu-id="d9e27-1947">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1947">boolean</span></span> | <span data-ttu-id="d9e27-1948">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1948">True</span></span> | <span data-ttu-id="d9e27-1949">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1949">The control allow negative</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1950">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1950">Return Value</span></span> 
<span data-ttu-id="d9e27-1951">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1951">The control allow negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="d9e27-1952">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="d9e27-1952">Method controlMaxLength</span></span> 
<span data-ttu-id="d9e27-1953">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-1953">Gets or sets the control max length</span></span>

     public int controlMaxLength ([int _controlMaxLength]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1954">Parameters</span></span>

| <span data-ttu-id="d9e27-1955">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1955">Parameter name</span></span> |  <span data-ttu-id="d9e27-1956">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1956">Parameter type</span></span> | <span data-ttu-id="d9e27-1957">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1957">Optional</span></span> | <span data-ttu-id="d9e27-1958">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1958">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1959">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="d9e27-1959">_controlMaxLength</span></span> | <span data-ttu-id="d9e27-1960">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-1960">int</span></span> | <span data-ttu-id="d9e27-1961">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-1961">True</span></span> | <span data-ttu-id="d9e27-1962">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="d9e27-1962">The control max length</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1963">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1963">Return Value</span></span> 
<span data-ttu-id="d9e27-1964">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="d9e27-1964">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="d9e27-1965">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-1965">Method getProperty</span></span> 
<span data-ttu-id="d9e27-1966">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1966">Gets the control property referenced by the key</span></span>

     public anytype getProperty (str _key) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1967">Parameters</span></span>

| <span data-ttu-id="d9e27-1968">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1968">Parameter name</span></span> |  <span data-ttu-id="d9e27-1969">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1969">Parameter type</span></span> | <span data-ttu-id="d9e27-1970">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1970">Optional</span></span> | <span data-ttu-id="d9e27-1971">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1971">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1972">_key</span><span class="sxs-lookup"><span data-stu-id="d9e27-1972">_key</span></span> | <span data-ttu-id="d9e27-1973">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1973">str</span></span> | <span data-ttu-id="d9e27-1974">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1974">False</span></span> | <span data-ttu-id="d9e27-1975">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1975">The name of the control property</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-1976">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1976">Return Value</span></span> 
<span data-ttu-id="d9e27-1977">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1977">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="d9e27-1978">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="d9e27-1978">Method setProperty</span></span> 
<span data-ttu-id="d9e27-1979">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1979">Sets the control property referenced by the key</span></span>

     public void setProperty (str _key, anytype _value) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-1980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-1980">Parameters</span></span>

| <span data-ttu-id="d9e27-1981">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1981">Parameter name</span></span> |  <span data-ttu-id="d9e27-1982">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-1982">Parameter type</span></span> | <span data-ttu-id="d9e27-1983">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-1983">Optional</span></span> | <span data-ttu-id="d9e27-1984">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1984">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-1985">_key</span><span class="sxs-lookup"><span data-stu-id="d9e27-1985">_key</span></span> | <span data-ttu-id="d9e27-1986">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-1986">str</span></span> | <span data-ttu-id="d9e27-1987">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1987">False</span></span> | <span data-ttu-id="d9e27-1988">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="d9e27-1988">The name of the control property</span></span>
| <span data-ttu-id="d9e27-1989">_value</span><span class="sxs-lookup"><span data-stu-id="d9e27-1989">_value</span></span> | <span data-ttu-id="d9e27-1990">anytype</span><span class="sxs-lookup"><span data-stu-id="d9e27-1990">anytype</span></span> | <span data-ttu-id="d9e27-1991">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-1991">False</span></span> | <span data-ttu-id="d9e27-1992">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-1992">The value of the control property</span></span>


## <a name="class-sysappentityattribute"></a><span data-ttu-id="d9e27-1993">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1993">Class SysAppEntityAttribute</span></span> 
<span data-ttu-id="d9e27-1994">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-1994">SysAppEntityAttribute used for decorating data contract entities</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-1995">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-1995">Methods</span></span>

| <span data-ttu-id="d9e27-1996">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-1996">Method name</span></span> | <span data-ttu-id="d9e27-1997">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-1997">Returns</span></span> | <span data-ttu-id="d9e27-1998">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-1998">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-1999">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-1999">new</span></span> | <span data-ttu-id="d9e27-2000">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2000">void</span></span> | <span data-ttu-id="d9e27-2001">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2001">Constructor</span></span> |
| <span data-ttu-id="d9e27-2002">名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-2002">name</span></span> | <span data-ttu-id="d9e27-2003">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2003">str</span></span> | <span data-ttu-id="d9e27-2004">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2004">Gets the name of the entity</span></span> |
| <span data-ttu-id="d9e27-2005">entityKey</span><span class="sxs-lookup"><span data-stu-id="d9e27-2005">entityKey</span></span> | <span data-ttu-id="d9e27-2006">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2006">str</span></span> | <span data-ttu-id="d9e27-2007">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2007">Gets the entity key</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2008">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2008">Method new</span></span> 
<span data-ttu-id="d9e27-2009">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2009">Constructor</span></span>

     public void new (str _name, str _entityKey) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2010">Parameters</span></span>

| <span data-ttu-id="d9e27-2011">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2011">Parameter name</span></span> |  <span data-ttu-id="d9e27-2012">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2012">Parameter type</span></span> | <span data-ttu-id="d9e27-2013">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2013">Optional</span></span> | <span data-ttu-id="d9e27-2014">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2014">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2015">_name</span><span class="sxs-lookup"><span data-stu-id="d9e27-2015">_name</span></span> | <span data-ttu-id="d9e27-2016">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2016">str</span></span> | <span data-ttu-id="d9e27-2017">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2017">False</span></span> | <span data-ttu-id="d9e27-2018">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2018">Entity name</span></span>
| <span data-ttu-id="d9e27-2019">_entityKey</span><span class="sxs-lookup"><span data-stu-id="d9e27-2019">_entityKey</span></span> | <span data-ttu-id="d9e27-2020">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2020">str</span></span> | <span data-ttu-id="d9e27-2021">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2021">False</span></span> | <span data-ttu-id="d9e27-2022">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-2022">Name of the entity's key</span></span>


### <a name="method-name"></a><span data-ttu-id="d9e27-2023">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2023">Method name</span></span> 
<span data-ttu-id="d9e27-2024">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2024">Gets the name of the entity</span></span>

     public str name () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2025">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2025">Return Value</span></span> 
<span data-ttu-id="d9e27-2026">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-2026">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="d9e27-2027">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="d9e27-2027">Method entityKey</span></span> 
<span data-ttu-id="d9e27-2028">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2028">Gets the entity key</span></span>

     public str entityKey () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2029">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2029">Return Value</span></span> 
<span data-ttu-id="d9e27-2030">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="d9e27-2030">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="d9e27-2031">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2031">Class SysAppEntityContext</span></span> 
<span data-ttu-id="d9e27-2032">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2032">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2033">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2033">Methods</span></span>

| <span data-ttu-id="d9e27-2034">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2034">Method name</span></span> | <span data-ttu-id="d9e27-2035">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2035">Returns</span></span> | <span data-ttu-id="d9e27-2036">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2036">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2037">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="d9e27-2037">constructFromParams</span></span> | <span data-ttu-id="d9e27-2038">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2038">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-2039">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2039">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="d9e27-2040">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="d9e27-2040">constructFromBuffer</span></span> | <span data-ttu-id="d9e27-2041">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2041">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-2042">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="d9e27-2042">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="d9e27-2043">entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2043">entityName</span></span> | <span data-ttu-id="d9e27-2044">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2044">str</span></span> | <span data-ttu-id="d9e27-2045">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2045">Entity name on which filter applies</span></span> |
| <span data-ttu-id="d9e27-2046">entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2046">entityId</span></span> | <span data-ttu-id="d9e27-2047">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2047">str</span></span> | <span data-ttu-id="d9e27-2048">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2048">Field value on which filter applies</span></span> |


### <a name="method-constructfromparams"></a><span data-ttu-id="d9e27-2049">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="d9e27-2049">Method constructFromParams</span></span> 
<span data-ttu-id="d9e27-2050">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2050">Constructs SysAppEntityContext from entityName and entityId</span></span>

     public SysAppEntityContext constructFromParams (str _entityName, str _entityId) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2051">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2051">Parameters</span></span>

| <span data-ttu-id="d9e27-2052">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2052">Parameter name</span></span> |  <span data-ttu-id="d9e27-2053">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2053">Parameter type</span></span> | <span data-ttu-id="d9e27-2054">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2054">Optional</span></span> | <span data-ttu-id="d9e27-2055">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2055">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2056">_entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2056">_entityName</span></span> | <span data-ttu-id="d9e27-2057">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2057">str</span></span> | <span data-ttu-id="d9e27-2058">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2058">False</span></span> | <span data-ttu-id="d9e27-2059">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2059">Entity name</span></span>
| <span data-ttu-id="d9e27-2060">_entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2060">_entityId</span></span> | <span data-ttu-id="d9e27-2061">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2061">str</span></span> | <span data-ttu-id="d9e27-2062">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2062">False</span></span> | <span data-ttu-id="d9e27-2063">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2063">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2064">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2064">Return Value</span></span> 
<span data-ttu-id="d9e27-2065">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="d9e27-2065">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="d9e27-2066">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="d9e27-2066">Method constructFromBuffer</span></span> 
<span data-ttu-id="d9e27-2067">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="d9e27-2067">Constructs SysAppEntityContext from table buffer</span></span>

     public SysAppEntityContext constructFromBuffer (Common _tableBuffer) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2068">Parameters</span></span>

| <span data-ttu-id="d9e27-2069">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2069">Parameter name</span></span> |  <span data-ttu-id="d9e27-2070">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2070">Parameter type</span></span> | <span data-ttu-id="d9e27-2071">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2071">Optional</span></span> | <span data-ttu-id="d9e27-2072">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2072">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2073">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="d9e27-2073">_tableBuffer</span></span> | <span data-ttu-id="d9e27-2074">共通</span><span class="sxs-lookup"><span data-stu-id="d9e27-2074">Common</span></span> | <span data-ttu-id="d9e27-2075">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2075">False</span></span> | <span data-ttu-id="d9e27-2076">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2076">table buffer forming the entity</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2077">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2077">Return Value</span></span> 
<span data-ttu-id="d9e27-2078">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="d9e27-2078">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="d9e27-2079">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2079">Method entityName</span></span> 
<span data-ttu-id="d9e27-2080">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2080">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2081">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2081">Parameters</span></span>

| <span data-ttu-id="d9e27-2082">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2082">Parameter name</span></span> |  <span data-ttu-id="d9e27-2083">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2083">Parameter type</span></span> | <span data-ttu-id="d9e27-2084">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2084">Optional</span></span> | <span data-ttu-id="d9e27-2085">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2085">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2086">_entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2086">_entityName</span></span> | <span data-ttu-id="d9e27-2087">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2087">str</span></span> | <span data-ttu-id="d9e27-2088">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2088">True</span></span> | <span data-ttu-id="d9e27-2089">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2089">Entity name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2090">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2090">Return Value</span></span> 
<span data-ttu-id="d9e27-2091">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2091">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="d9e27-2092">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2092">Method entityId</span></span> 
<span data-ttu-id="d9e27-2093">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2093">Field value on which filter applies</span></span>

     public str entityId ([str _entityId]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2094">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2094">Parameters</span></span>

| <span data-ttu-id="d9e27-2095">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2095">Parameter name</span></span> |  <span data-ttu-id="d9e27-2096">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2096">Parameter type</span></span> | <span data-ttu-id="d9e27-2097">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2097">Optional</span></span> | <span data-ttu-id="d9e27-2098">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2098">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2099">_entityId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2099">_entityId</span></span> | <span data-ttu-id="d9e27-2100">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2100">str</span></span> | <span data-ttu-id="d9e27-2101">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2101">True</span></span> | <span data-ttu-id="d9e27-2102">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2102">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2103">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2103">Return Value</span></span> 
<span data-ttu-id="d9e27-2104">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2104">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="d9e27-2105">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2105">Class SysAppFieldAttribute</span></span> 
<span data-ttu-id="d9e27-2106">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2106">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2107">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2107">Methods</span></span>

| <span data-ttu-id="d9e27-2108">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2108">Method name</span></span> | <span data-ttu-id="d9e27-2109">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2109">Returns</span></span> | <span data-ttu-id="d9e27-2110">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2110">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2111">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2111">new</span></span> | <span data-ttu-id="d9e27-2112">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2112">void</span></span> | <span data-ttu-id="d9e27-2113">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2113">Creates a new instance of SysAppFieldAttribute class</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2114">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2114">Method new</span></span> 
<span data-ttu-id="d9e27-2115">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2115">Creates a new instance of SysAppFieldAttribute class</span></span>

     public void new (str _fieldName, str _label) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2116">Parameters</span></span>

| <span data-ttu-id="d9e27-2117">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2117">Parameter name</span></span> |  <span data-ttu-id="d9e27-2118">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2118">Parameter type</span></span> | <span data-ttu-id="d9e27-2119">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2119">Optional</span></span> | <span data-ttu-id="d9e27-2120">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2120">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2121">_fieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2121">_fieldName</span></span> | <span data-ttu-id="d9e27-2122">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2122">str</span></span> | <span data-ttu-id="d9e27-2123">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2123">False</span></span> | <span data-ttu-id="d9e27-2124">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2124">Entity field name with which control is bound</span></span>
| <span data-ttu-id="d9e27-2125">_label</span><span class="sxs-lookup"><span data-stu-id="d9e27-2125">_label</span></span> | <span data-ttu-id="d9e27-2126">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2126">str</span></span> | <span data-ttu-id="d9e27-2127">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2127">False</span></span> | <span data-ttu-id="d9e27-2128">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-2128">Control label</span></span>


## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="d9e27-2129">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="d9e27-2129">Class SysAppFieldMultiSelectHelper</span></span> 
<span data-ttu-id="d9e27-2130">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2130">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2131">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2131">Methods</span></span>

| <span data-ttu-id="d9e27-2132">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2132">Method name</span></span> | <span data-ttu-id="d9e27-2133">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2133">Returns</span></span> | <span data-ttu-id="d9e27-2134">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2134">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2135">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2135">new</span></span> | <span data-ttu-id="d9e27-2136">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2136">void</span></span> | <span data-ttu-id="d9e27-2137">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2137">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="d9e27-2138">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="d9e27-2138">getSelectedRecIds</span></span> | <span data-ttu-id="d9e27-2139">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-2139">container</span></span> | <span data-ttu-id="d9e27-2140">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2140">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="d9e27-2141">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-2141">getSelectedValues</span></span> | <span data-ttu-id="d9e27-2142">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-2142">container</span></span> | <span data-ttu-id="d9e27-2143">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2143">Returns a container of selected values</span></span> |
| <span data-ttu-id="d9e27-2144">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="d9e27-2144">getSelectedRecords</span></span> | <span data-ttu-id="d9e27-2145">共通</span><span class="sxs-lookup"><span data-stu-id="d9e27-2145">Common</span></span> | <span data-ttu-id="d9e27-2146">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2146">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="d9e27-2147">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2147">The buffer is marked as temp..</span></span>  <span data-ttu-id="d9e27-2148">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2148">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="d9e27-2149">setControlValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-2149">setControlValue</span></span> | <span data-ttu-id="d9e27-2150">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2150">void</span></span> | <span data-ttu-id="d9e27-2151">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2151">A setter to set the multi select control value</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2152">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2152">Method new</span></span> 
<span data-ttu-id="d9e27-2153">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2153">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

     public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2154">Parameters</span></span>

| <span data-ttu-id="d9e27-2155">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2155">Parameter name</span></span> |  <span data-ttu-id="d9e27-2156">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2156">Parameter type</span></span> | <span data-ttu-id="d9e27-2157">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2157">Optional</span></span> | <span data-ttu-id="d9e27-2158">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2158">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2159">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2159">_multiSelectTableId</span></span> | <span data-ttu-id="d9e27-2160">TableId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2160">TableId</span></span> | <span data-ttu-id="d9e27-2161">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2161">False</span></span> | <span data-ttu-id="d9e27-2162">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2162">The backing tableId for the field</span></span>
| <span data-ttu-id="d9e27-2163">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2163">_valueFieldId</span></span> | <span data-ttu-id="d9e27-2164">FieldId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2164">FieldId</span></span> | <span data-ttu-id="d9e27-2165">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2165">False</span></span> | <span data-ttu-id="d9e27-2166">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2166">The fieldId for the field which will be shown in the multi select control</span></span>
| <span data-ttu-id="d9e27-2167">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-2167">_multiSelectControl</span></span> | <span data-ttu-id="d9e27-2168">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-2168">FormStringControl</span></span> | <span data-ttu-id="d9e27-2169">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2169">False</span></span> | <span data-ttu-id="d9e27-2170">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="d9e27-2170">The string control that will be the multi select control</span></span>


### <a name="method-getselectedrecids"></a><span data-ttu-id="d9e27-2171">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="d9e27-2171">Method getSelectedRecIds</span></span> 
<span data-ttu-id="d9e27-2172">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2172">Returns a container of recIds of the records that were selected</span></span>

     public container getSelectedRecIds () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2173">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2173">Return Value</span></span> 
<span data-ttu-id="d9e27-2174">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-2174">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="d9e27-2175">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-2175">Method getSelectedValues</span></span> 
<span data-ttu-id="d9e27-2176">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2176">Returns a container of selected values</span></span>

     public container getSelectedValues () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2177">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2177">Return Value</span></span> 
<span data-ttu-id="d9e27-2178">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="d9e27-2178">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="d9e27-2179">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="d9e27-2179">Method getSelectedRecords</span></span> 
<span data-ttu-id="d9e27-2180">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2180">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="d9e27-2181">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2181">The buffer is marked as temp..</span></span>  <span data-ttu-id="d9e27-2182">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2182">Later a while-Select can be used to iterate through all the records</span></span>

     public Common getSelectedRecords () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2183">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2183">Return Value</span></span> 
<span data-ttu-id="d9e27-2184">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="d9e27-2184">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="d9e27-2185">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-2185">Method setControlValue</span></span> 
<span data-ttu-id="d9e27-2186">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2186">A setter to set the multi select control value</span></span>

     public void setControlValue (str _value) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2187">Parameters</span></span>

| <span data-ttu-id="d9e27-2188">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2188">Parameter name</span></span> |  <span data-ttu-id="d9e27-2189">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2189">Parameter type</span></span> | <span data-ttu-id="d9e27-2190">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2190">Optional</span></span> | <span data-ttu-id="d9e27-2191">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2191">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2192">_value</span><span class="sxs-lookup"><span data-stu-id="d9e27-2192">_value</span></span> | <span data-ttu-id="d9e27-2193">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2193">str</span></span> | <span data-ttu-id="d9e27-2194">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2194">False</span></span> | <span data-ttu-id="d9e27-2195">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2195">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>


## <a name="class-sysappfiltercontext"></a><span data-ttu-id="d9e27-2196">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2196">Class SysAppFilterContext</span></span> 
<span data-ttu-id="d9e27-2197">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-2197">SysAppFilterContext class which holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2198">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2198">Methods</span></span>

| <span data-ttu-id="d9e27-2199">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2199">Method name</span></span> | <span data-ttu-id="d9e27-2200">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2200">Returns</span></span> | <span data-ttu-id="d9e27-2201">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2201">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2202">entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2202">entityName</span></span> | <span data-ttu-id="d9e27-2203">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2203">str</span></span> | <span data-ttu-id="d9e27-2204">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2204">Entity name on which filter applies</span></span> |
| <span data-ttu-id="d9e27-2205">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2205">filterFieldName</span></span> | <span data-ttu-id="d9e27-2206">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2206">str</span></span> | <span data-ttu-id="d9e27-2207">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2207">Field name on which filter applies</span></span> |
| <span data-ttu-id="d9e27-2208">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="d9e27-2208">filterFieldValueList</span></span> | <span data-ttu-id="d9e27-2209">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2209">List</span></span> | <span data-ttu-id="d9e27-2210">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2210">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="d9e27-2211">演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2211">operator</span></span> | <span data-ttu-id="d9e27-2212">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2212">str</span></span> | <span data-ttu-id="d9e27-2213">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2213">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="d9e27-2214">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-2214">addFilterFieldValue</span></span> | <span data-ttu-id="d9e27-2215">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2215">void</span></span> | <span data-ttu-id="d9e27-2216">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-2216">Adds filter field value</span></span> |


### <a name="method-entityname"></a><span data-ttu-id="d9e27-2217">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2217">Method entityName</span></span> 
<span data-ttu-id="d9e27-2218">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2218">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2219">Parameters</span></span>

| <span data-ttu-id="d9e27-2220">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2220">Parameter name</span></span> |  <span data-ttu-id="d9e27-2221">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2221">Parameter type</span></span> | <span data-ttu-id="d9e27-2222">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2222">Optional</span></span> | <span data-ttu-id="d9e27-2223">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2223">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2224">_entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2224">_entityName</span></span> | <span data-ttu-id="d9e27-2225">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2225">str</span></span> | <span data-ttu-id="d9e27-2226">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2226">True</span></span> | <span data-ttu-id="d9e27-2227">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2227">Entity name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2228">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2228">Return Value</span></span> 
<span data-ttu-id="d9e27-2229">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2229">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="d9e27-2230">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2230">Method filterFieldName</span></span> 
<span data-ttu-id="d9e27-2231">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2231">Field name on which filter applies</span></span>

     public str filterFieldName ([str _filterFieldName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2232">Parameters</span></span>

| <span data-ttu-id="d9e27-2233">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2233">Parameter name</span></span> |  <span data-ttu-id="d9e27-2234">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2234">Parameter type</span></span> | <span data-ttu-id="d9e27-2235">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2235">Optional</span></span> | <span data-ttu-id="d9e27-2236">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2236">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2237">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2237">_filterFieldName</span></span> | <span data-ttu-id="d9e27-2238">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2238">str</span></span> | <span data-ttu-id="d9e27-2239">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2239">True</span></span> | <span data-ttu-id="d9e27-2240">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2240">Field name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2241">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2241">Return Value</span></span> 
<span data-ttu-id="d9e27-2242">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2242">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="d9e27-2243">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="d9e27-2243">Method filterFieldValueList</span></span> 
<span data-ttu-id="d9e27-2244">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2244">Gets the list of filter field values based on which filter happens</span></span>

     public List filterFieldValueList () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2245">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2245">Return Value</span></span> 
<span data-ttu-id="d9e27-2246">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2246">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="d9e27-2247">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2247">Method operator</span></span> 
<span data-ttu-id="d9e27-2248">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2248">Operator based on which result will be fetched</span></span>

     public str operator ([str _operator]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2249">Parameters</span></span>

| <span data-ttu-id="d9e27-2250">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2250">Parameter name</span></span> |  <span data-ttu-id="d9e27-2251">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2251">Parameter type</span></span> | <span data-ttu-id="d9e27-2252">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2252">Optional</span></span> | <span data-ttu-id="d9e27-2253">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2253">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2254">_operator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2254">_operator</span></span> | <span data-ttu-id="d9e27-2255">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2255">str</span></span> | <span data-ttu-id="d9e27-2256">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2256">True</span></span> | <span data-ttu-id="d9e27-2257">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2257">Operator based on which result will be fetched</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2258">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2258">Return Value</span></span> 
<span data-ttu-id="d9e27-2259">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2259">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="d9e27-2260">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-2260">Method addFilterFieldValue</span></span> 
<span data-ttu-id="d9e27-2261">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-2261">Adds filter field value</span></span>

     public void addFilterFieldValue ( _filterFieldValueList) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2262">Parameters</span></span>

| <span data-ttu-id="d9e27-2263">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2263">Parameter name</span></span> |  <span data-ttu-id="d9e27-2264">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2264">Parameter type</span></span> | <span data-ttu-id="d9e27-2265">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2265">Optional</span></span> | <span data-ttu-id="d9e27-2266">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2266">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2267">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="d9e27-2267">_filterFieldValueList</span></span> |  | <span data-ttu-id="d9e27-2268">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2268">False</span></span> | <span data-ttu-id="d9e27-2269">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2269">Filter field values based on which filter happens</span></span>


## <a name="class-sysapplookupattribute"></a><span data-ttu-id="d9e27-2270">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2270">Class SysAppLookUpAttribute</span></span> 
<span data-ttu-id="d9e27-2271">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2271">SysAppPageAttribute used for decorating pages that is also lookup page</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2272">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2272">Methods</span></span>

| <span data-ttu-id="d9e27-2273">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2273">Method name</span></span> | <span data-ttu-id="d9e27-2274">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2274">Returns</span></span> | <span data-ttu-id="d9e27-2275">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2275">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2276">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2276">new</span></span> | <span data-ttu-id="d9e27-2277">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2277">void</span></span> | <span data-ttu-id="d9e27-2278">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2278">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="d9e27-2279">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2279">displayFieldName</span></span> | <span data-ttu-id="d9e27-2280">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2280">str</span></span> | <span data-ttu-id="d9e27-2281">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2281">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="d9e27-2282">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2282">valueFieldName</span></span> | <span data-ttu-id="d9e27-2283">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2283">str</span></span> | <span data-ttu-id="d9e27-2284">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2284">Gets the value field name of lookup control</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2285">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2285">Method new</span></span> 
<span data-ttu-id="d9e27-2286">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2286">Creates a new instance of SysAppLookUpAttribute class</span></span>

     public void new (str _displayFieldName, str _valueFieldName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2287">Parameters</span></span>

| <span data-ttu-id="d9e27-2288">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2288">Parameter name</span></span> |  <span data-ttu-id="d9e27-2289">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2289">Parameter type</span></span> | <span data-ttu-id="d9e27-2290">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2290">Optional</span></span> | <span data-ttu-id="d9e27-2291">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2291">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2292">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2292">_displayFieldName</span></span> | <span data-ttu-id="d9e27-2293">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2293">str</span></span> | <span data-ttu-id="d9e27-2294">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2294">False</span></span> | <span data-ttu-id="d9e27-2295">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2295">Lookup display field.</span></span> <span data-ttu-id="d9e27-2296">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-2296">Name of any control of lookup page</span></span>
| <span data-ttu-id="d9e27-2297">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2297">_valueFieldName</span></span> | <span data-ttu-id="d9e27-2298">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2298">str</span></span> | <span data-ttu-id="d9e27-2299">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2299">False</span></span> | <span data-ttu-id="d9e27-2300">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2300">Lookup value field.</span></span> <span data-ttu-id="d9e27-2301">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-2301">Name of control formed by root data contract constructing lookup page</span></span>


### <a name="method-displayfieldname"></a><span data-ttu-id="d9e27-2302">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2302">Method displayFieldName</span></span> 
<span data-ttu-id="d9e27-2303">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2303">Gets the display field name of lookup control</span></span>

     public str displayFieldName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2304">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2304">Return Value</span></span> 
<span data-ttu-id="d9e27-2305">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2305">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="d9e27-2306">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2306">Method valueFieldName</span></span> 
<span data-ttu-id="d9e27-2307">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2307">Gets the value field name of lookup control</span></span>

     public str valueFieldName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2308">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2308">Return Value</span></span> 
<span data-ttu-id="d9e27-2309">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2309">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="d9e27-2310">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2310">Class SysAppLookupFieldAttribute</span></span> 
<span data-ttu-id="d9e27-2311">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2311">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2312">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2312">Methods</span></span>

| <span data-ttu-id="d9e27-2313">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2313">Method name</span></span> | <span data-ttu-id="d9e27-2314">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2314">Returns</span></span> | <span data-ttu-id="d9e27-2315">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2315">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2316">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2316">new</span></span> | <span data-ttu-id="d9e27-2317">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2317">void</span></span> | <span data-ttu-id="d9e27-2318">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2318">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="d9e27-2319">entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2319">entityName</span></span> | <span data-ttu-id="d9e27-2320">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2320">str</span></span> | <span data-ttu-id="d9e27-2321">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2321">Gets the name of the entity with which lookup page is related</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2322">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2322">Method new</span></span> 
<span data-ttu-id="d9e27-2323">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2323">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

     public void new ( _name) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2324">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2324">Parameters</span></span>

| <span data-ttu-id="d9e27-2325">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2325">Parameter name</span></span> |  <span data-ttu-id="d9e27-2326">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2326">Parameter type</span></span> | <span data-ttu-id="d9e27-2327">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2327">Optional</span></span> | <span data-ttu-id="d9e27-2328">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2328">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2329">_name</span><span class="sxs-lookup"><span data-stu-id="d9e27-2329">_name</span></span> |  | <span data-ttu-id="d9e27-2330">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2330">False</span></span> | <span data-ttu-id="d9e27-2331">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-2331">Name of the entity with which lookup page is related</span></span>


### <a name="method-entityname"></a><span data-ttu-id="d9e27-2332">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2332">Method entityName</span></span> 
<span data-ttu-id="d9e27-2333">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2333">Gets the name of the entity with which lookup page is related</span></span>

     public str entityName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2334">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2334">Return Value</span></span> 
<span data-ttu-id="d9e27-2335">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="d9e27-2335">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="d9e27-2336">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2336">Class SysAppPageAttribute</span></span> 
<span data-ttu-id="d9e27-2337">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2337">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2338">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2338">Methods</span></span>

| <span data-ttu-id="d9e27-2339">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2339">Method name</span></span> | <span data-ttu-id="d9e27-2340">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2340">Returns</span></span> | <span data-ttu-id="d9e27-2341">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2341">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2342">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2342">new</span></span> | <span data-ttu-id="d9e27-2343">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2343">void</span></span> | <span data-ttu-id="d9e27-2344">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2344">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="d9e27-2345">pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-2345">pageTitle</span></span> | <span data-ttu-id="d9e27-2346">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2346">str</span></span> | <span data-ttu-id="d9e27-2347">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2347">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="d9e27-2348">pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-2348">pageDescription</span></span> | <span data-ttu-id="d9e27-2349">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2349">str</span></span> | <span data-ttu-id="d9e27-2350">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2350">Gets the Page Description</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2351">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2351">Method new</span></span> 
<span data-ttu-id="d9e27-2352">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2352">Creates a new instance of SysAppPageAttribute class</span></span>

     public void new ([str _pageTitle], [str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2353">Parameters</span></span>

| <span data-ttu-id="d9e27-2354">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2354">Parameter name</span></span> |  <span data-ttu-id="d9e27-2355">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2355">Parameter type</span></span> | <span data-ttu-id="d9e27-2356">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2356">Optional</span></span> | <span data-ttu-id="d9e27-2357">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2357">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2358">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-2358">_pageTitle</span></span> | <span data-ttu-id="d9e27-2359">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2359">str</span></span> | <span data-ttu-id="d9e27-2360">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2360">True</span></span> | <span data-ttu-id="d9e27-2361">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-2361">The page title</span></span>
| <span data-ttu-id="d9e27-2362">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-2362">_pageDescription</span></span> | <span data-ttu-id="d9e27-2363">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2363">str</span></span> | <span data-ttu-id="d9e27-2364">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2364">True</span></span> | <span data-ttu-id="d9e27-2365">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2365">The page description</span></span>


### <a name="method-pagetitle"></a><span data-ttu-id="d9e27-2366">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-2366">Method pageTitle</span></span> 
<span data-ttu-id="d9e27-2367">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2367">Gets the Page Title of the page</span></span>

     public str pageTitle () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2368">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2368">Return Value</span></span> 
<span data-ttu-id="d9e27-2369">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-2369">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="d9e27-2370">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-2370">Method pageDescription</span></span> 
<span data-ttu-id="d9e27-2371">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2371">Gets the Page Description</span></span>

     public str pageDescription () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2372">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2372">Return Value</span></span> 
<span data-ttu-id="d9e27-2373">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2373">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="d9e27-2374">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2374">Class SysAppPageMetadata</span></span> 
<span data-ttu-id="d9e27-2375">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2375">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2376">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-2376">Methods</span></span>

| <span data-ttu-id="d9e27-2377">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2377">Method name</span></span> | <span data-ttu-id="d9e27-2378">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2378">Returns</span></span> | <span data-ttu-id="d9e27-2379">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2379">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2380">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2380">new</span></span> | <span data-ttu-id="d9e27-2381">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2381">void</span></span> |  |
| <span data-ttu-id="d9e27-2382">getPageName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2382">getPageName</span></span> | <span data-ttu-id="d9e27-2383">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2383">str</span></span> | <span data-ttu-id="d9e27-2384">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2384">Returns the page name</span></span> |
| <span data-ttu-id="d9e27-2385">pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-2385">pageTitle</span></span> | <span data-ttu-id="d9e27-2386">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2386">str</span></span> | <span data-ttu-id="d9e27-2387">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2387">Gets and sets the page title</span></span> |
| <span data-ttu-id="d9e27-2388">pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-2388">pageDescription</span></span> | <span data-ttu-id="d9e27-2389">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2389">str</span></span> | <span data-ttu-id="d9e27-2390">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2390">Gets or sets the page description</span></span> |
| <span data-ttu-id="d9e27-2391">pageHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2391">pageHidden</span></span> | <span data-ttu-id="d9e27-2392">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2392">boolean</span></span> | <span data-ttu-id="d9e27-2393">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2393">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="d9e27-2394">pageOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-2394">pageOrder</span></span> | <span data-ttu-id="d9e27-2395">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-2395">int</span></span> | <span data-ttu-id="d9e27-2396">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2396">Gets or sets the page order</span></span> |
| <span data-ttu-id="d9e27-2397">getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-2397">getControl</span></span> | <span data-ttu-id="d9e27-2398">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2398">SysAppControlMetadata</span></span> | <span data-ttu-id="d9e27-2399">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2399">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="d9e27-2400">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2400">getControlEnumerator</span></span> | <span data-ttu-id="d9e27-2401">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2401">MapEnumerator</span></span> | <span data-ttu-id="d9e27-2402">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2402">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="d9e27-2403">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-2403">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2404">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2404">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2405">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2405">Parameters</span></span>

| <span data-ttu-id="d9e27-2406">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2406">Parameter name</span></span> |  <span data-ttu-id="d9e27-2407">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2407">Parameter type</span></span> | <span data-ttu-id="d9e27-2408">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2408">Optional</span></span> | <span data-ttu-id="d9e27-2409">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2409">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2410">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2410">_pageMetadata</span></span> | <span data-ttu-id="d9e27-2411">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2411">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="d9e27-2412">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2412">False</span></span> | 


### <a name="method-getpagename"></a><span data-ttu-id="d9e27-2413">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2413">Method getPageName</span></span> 
<span data-ttu-id="d9e27-2414">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2414">Returns the page name</span></span>

     public str getPageName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2415">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2415">Return Value</span></span> 
<span data-ttu-id="d9e27-2416">ページ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2416">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="d9e27-2417">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-2417">Method pageTitle</span></span> 
<span data-ttu-id="d9e27-2418">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2418">Gets and sets the page title</span></span>

     public str pageTitle ([str _pageTitle]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2419">Parameters</span></span>

| <span data-ttu-id="d9e27-2420">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2420">Parameter name</span></span> |  <span data-ttu-id="d9e27-2421">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2421">Parameter type</span></span> | <span data-ttu-id="d9e27-2422">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2422">Optional</span></span> | <span data-ttu-id="d9e27-2423">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2423">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2424">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-2424">_pageTitle</span></span> | <span data-ttu-id="d9e27-2425">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2425">str</span></span> | <span data-ttu-id="d9e27-2426">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2426">True</span></span> | <span data-ttu-id="d9e27-2427">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-2427">The page title</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2428">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2428">Return Value</span></span> 
<span data-ttu-id="d9e27-2429">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-2429">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="d9e27-2430">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-2430">Method pageDescription</span></span> 
<span data-ttu-id="d9e27-2431">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2431">Gets or sets the page description</span></span>

     public str pageDescription ([str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2432">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2432">Parameters</span></span>

| <span data-ttu-id="d9e27-2433">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2433">Parameter name</span></span> |  <span data-ttu-id="d9e27-2434">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2434">Parameter type</span></span> | <span data-ttu-id="d9e27-2435">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2435">Optional</span></span> | <span data-ttu-id="d9e27-2436">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2436">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2437">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-2437">_pageDescription</span></span> | <span data-ttu-id="d9e27-2438">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2438">str</span></span> | <span data-ttu-id="d9e27-2439">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2439">True</span></span> | <span data-ttu-id="d9e27-2440">ページの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2440">The page description</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2441">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2441">Return Value</span></span> 
<span data-ttu-id="d9e27-2442">ページの説明></span><span class="sxs-lookup"><span data-stu-id="d9e27-2442">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="d9e27-2443">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2443">Method pageHidden</span></span> 
<span data-ttu-id="d9e27-2444">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2444">Gets and sets whether the page is hidden in the workspace</span></span>

     public boolean pageHidden ([boolean _pageHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2445">Parameters</span></span>

| <span data-ttu-id="d9e27-2446">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2446">Parameter name</span></span> |  <span data-ttu-id="d9e27-2447">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2447">Parameter type</span></span> | <span data-ttu-id="d9e27-2448">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2448">Optional</span></span> | <span data-ttu-id="d9e27-2449">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2449">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2450">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2450">_pageHidden</span></span> | <span data-ttu-id="d9e27-2451">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2451">boolean</span></span> | <span data-ttu-id="d9e27-2452">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2452">True</span></span> | <span data-ttu-id="d9e27-2453">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2453">page hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2454">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2454">Return Value</span></span> 
<span data-ttu-id="d9e27-2455">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2455">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="d9e27-2456">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-2456">Method pageOrder</span></span> 
<span data-ttu-id="d9e27-2457">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2457">Gets or sets the page order</span></span>

     public int pageOrder ([int _pageOrder]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2458">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2458">Parameters</span></span>

| <span data-ttu-id="d9e27-2459">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2459">Parameter name</span></span> |  <span data-ttu-id="d9e27-2460">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2460">Parameter type</span></span> | <span data-ttu-id="d9e27-2461">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2461">Optional</span></span> | <span data-ttu-id="d9e27-2462">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2462">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2463">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="d9e27-2463">_pageOrder</span></span> | <span data-ttu-id="d9e27-2464">int</span><span class="sxs-lookup"><span data-stu-id="d9e27-2464">int</span></span> | <span data-ttu-id="d9e27-2465">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2465">True</span></span> | <span data-ttu-id="d9e27-2466">ページの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-2466">The page order</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2467">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2467">Return Value</span></span> 
<span data-ttu-id="d9e27-2468">ページの順序</span><span class="sxs-lookup"><span data-stu-id="d9e27-2468">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="d9e27-2469">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="d9e27-2469">Method getControl</span></span> 
<span data-ttu-id="d9e27-2470">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2470">Returns the control on the current page having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2471">Parameters</span></span>

| <span data-ttu-id="d9e27-2472">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2472">Parameter name</span></span> |  <span data-ttu-id="d9e27-2473">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2473">Parameter type</span></span> | <span data-ttu-id="d9e27-2474">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2474">Optional</span></span> | <span data-ttu-id="d9e27-2475">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2475">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2476">_controlName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2476">_controlName</span></span> | <span data-ttu-id="d9e27-2477">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2477">str</span></span> | <span data-ttu-id="d9e27-2478">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2478">False</span></span> | <span data-ttu-id="d9e27-2479">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2479">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2480">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2480">Return Value</span></span> 
<span data-ttu-id="d9e27-2481">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="d9e27-2481">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="d9e27-2482">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2482">Method getControlEnumerator</span></span> 
<span data-ttu-id="d9e27-2483">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2483">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="d9e27-2484">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-2484">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2485">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2485">Return Value</span></span> 
<span data-ttu-id="d9e27-2486">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2486">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="d9e27-2487">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2487">Class SysAppProjectionAttribute</span></span> 
<span data-ttu-id="d9e27-2488">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2488">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2489">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2489">Methods</span></span>

| <span data-ttu-id="d9e27-2490">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2490">Method name</span></span> | <span data-ttu-id="d9e27-2491">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2491">Returns</span></span> | <span data-ttu-id="d9e27-2492">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2492">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2493">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2493">new</span></span> | <span data-ttu-id="d9e27-2494">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2494">void</span></span> | <span data-ttu-id="d9e27-2495">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2495">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2496">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2496">Method new</span></span> 
<span data-ttu-id="d9e27-2497">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2497">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

     public void new (str _label) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2498">Parameters</span></span>

| <span data-ttu-id="d9e27-2499">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2499">Parameter name</span></span> |  <span data-ttu-id="d9e27-2500">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2500">Parameter type</span></span> | <span data-ttu-id="d9e27-2501">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2501">Optional</span></span> | <span data-ttu-id="d9e27-2502">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2502">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2503">_label</span><span class="sxs-lookup"><span data-stu-id="d9e27-2503">_label</span></span> | <span data-ttu-id="d9e27-2504">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2504">str</span></span> | <span data-ttu-id="d9e27-2505">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2505">False</span></span> | <span data-ttu-id="d9e27-2506">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="d9e27-2506">Control label</span></span>


## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="d9e27-2507">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2507">Class SysAppRelationalAttribute</span></span> 
<span data-ttu-id="d9e27-2508">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2508">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2509">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2509">Methods</span></span>

| <span data-ttu-id="d9e27-2510">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2510">Method name</span></span> | <span data-ttu-id="d9e27-2511">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2511">Returns</span></span> | <span data-ttu-id="d9e27-2512">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2512">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2513">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2513">new</span></span> | <span data-ttu-id="d9e27-2514">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2514">void</span></span> | <span data-ttu-id="d9e27-2515">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2515">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2516">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2516">Method new</span></span> 
<span data-ttu-id="d9e27-2517">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2517">Constructor</span></span>

     public void new ([str _name]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2518">Parameters</span></span>

| <span data-ttu-id="d9e27-2519">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2519">Parameter name</span></span> |  <span data-ttu-id="d9e27-2520">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2520">Parameter type</span></span> | <span data-ttu-id="d9e27-2521">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2521">Optional</span></span> | <span data-ttu-id="d9e27-2522">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2522">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2523">_name</span><span class="sxs-lookup"><span data-stu-id="d9e27-2523">_name</span></span> | <span data-ttu-id="d9e27-2524">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2524">str</span></span> | <span data-ttu-id="d9e27-2525">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2525">True</span></span> | <span data-ttu-id="d9e27-2526">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2526">Property name of the referenced entity</span></span>


## <a name="class-sysapprequestparams"></a><span data-ttu-id="d9e27-2527">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="d9e27-2527">Class SysAppRequestParams</span></span> 
<span data-ttu-id="d9e27-2528">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2528">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2529">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2529">Methods</span></span>

| <span data-ttu-id="d9e27-2530">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2530">Method name</span></span> | <span data-ttu-id="d9e27-2531">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2531">Returns</span></span> | <span data-ttu-id="d9e27-2532">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2532">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2533">entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2533">entityContext</span></span> | <span data-ttu-id="d9e27-2534">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2534">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-2535">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2535">Entity context of the request</span></span> |
| <span data-ttu-id="d9e27-2536">filterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2536">filterContext</span></span> | <span data-ttu-id="d9e27-2537">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2537">List</span></span> | <span data-ttu-id="d9e27-2538">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2538">List of SysAppFilterContext for filter contexts</span></span> |


### <a name="method-entitycontext"></a><span data-ttu-id="d9e27-2539">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2539">Method entityContext</span></span> 
<span data-ttu-id="d9e27-2540">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2540">Entity context of the request</span></span>

     public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2541">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2541">Parameters</span></span>

| <span data-ttu-id="d9e27-2542">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2542">Parameter name</span></span> |  <span data-ttu-id="d9e27-2543">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2543">Parameter type</span></span> | <span data-ttu-id="d9e27-2544">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2544">Optional</span></span> | <span data-ttu-id="d9e27-2545">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2545">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2546">_entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2546">_entityContext</span></span> | <span data-ttu-id="d9e27-2547">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2547">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-2548">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2548">True</span></span> | <span data-ttu-id="d9e27-2549">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2549">Entity context of the request</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2550">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2550">Return Value</span></span> 
<span data-ttu-id="d9e27-2551">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2551">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="d9e27-2552">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2552">Method filterContext</span></span> 
<span data-ttu-id="d9e27-2553">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2553">List of SysAppFilterContext for filter contexts</span></span>

     public List filterContext ([List _filterContext]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2554">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2554">Parameters</span></span>

| <span data-ttu-id="d9e27-2555">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2555">Parameter name</span></span> |  <span data-ttu-id="d9e27-2556">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2556">Parameter type</span></span> | <span data-ttu-id="d9e27-2557">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2557">Optional</span></span> | <span data-ttu-id="d9e27-2558">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2558">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2559">_filterContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2559">_filterContext</span></span> | <span data-ttu-id="d9e27-2560">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2560">List</span></span> | <span data-ttu-id="d9e27-2561">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2561">True</span></span> | <span data-ttu-id="d9e27-2562">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2562">List of SysAppFilterContext for filter contexts of page</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2563">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2563">Return Value</span></span> 
<span data-ttu-id="d9e27-2564">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2564">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="d9e27-2565">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="d9e27-2565">Class SysAppResponse</span></span> 
<span data-ttu-id="d9e27-2566">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2566">SysAppResponse class.</span></span>  <span data-ttu-id="d9e27-2567">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2567">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2568">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2568">Methods</span></span>

| <span data-ttu-id="d9e27-2569">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2569">Method name</span></span> | <span data-ttu-id="d9e27-2570">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2570">Returns</span></span> | <span data-ttu-id="d9e27-2571">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2571">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2572">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2572">new</span></span> | <span data-ttu-id="d9e27-2573">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2573">void</span></span> |  |
| <span data-ttu-id="d9e27-2574">jobId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2574">jobId</span></span> | <span data-ttu-id="d9e27-2575">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2575">str</span></span> | <span data-ttu-id="d9e27-2576">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-2576">Job Id of the request</span></span> |
| <span data-ttu-id="d9e27-2577">データ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2577">data</span></span> | <span data-ttu-id="d9e27-2578">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="d9e27-2578">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="d9e27-2579">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2579">Data of the page</span></span> |
| <span data-ttu-id="d9e27-2580">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="d9e27-2580">failedInAppCall</span></span> | <span data-ttu-id="d9e27-2581">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2581">boolean</span></span> | <span data-ttu-id="d9e27-2582">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2582">Data of the page</span></span> |
| <span data-ttu-id="d9e27-2583">commits</span><span class="sxs-lookup"><span data-stu-id="d9e27-2583">commits</span></span> | <span data-ttu-id="d9e27-2584">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2584">List</span></span> | <span data-ttu-id="d9e27-2585">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2585">Commits after task is completed</span></span> |
| <span data-ttu-id="d9e27-2586">メッセージ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2586">messages</span></span> | <span data-ttu-id="d9e27-2587">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2587">List</span></span> | <span data-ttu-id="d9e27-2588">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-2588">Job Id of the request</span></span> |
| <span data-ttu-id="d9e27-2589">addMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-2589">addMessage</span></span> | <span data-ttu-id="d9e27-2590">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2590">void</span></span> | <span data-ttu-id="d9e27-2591">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-2591">Adds message</span></span> |
| <span data-ttu-id="d9e27-2592">addCommit</span><span class="sxs-lookup"><span data-stu-id="d9e27-2592">addCommit</span></span> | <span data-ttu-id="d9e27-2593">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2593">void</span></span> | <span data-ttu-id="d9e27-2594">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-2594">Adds commits</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2595">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2595">Method new</span></span> 


     public void new () 


### <a name="method-jobid"></a><span data-ttu-id="d9e27-2596">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2596">Method jobId</span></span> 
<span data-ttu-id="d9e27-2597">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-2597">Job Id of the request</span></span>

     public str jobId () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2598">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2598">Return Value</span></span> 
<span data-ttu-id="d9e27-2599">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-2599">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="d9e27-2600">メソッド data</span><span class="sxs-lookup"><span data-stu-id="d9e27-2600">Method data</span></span> 
<span data-ttu-id="d9e27-2601">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2601">Data of the page</span></span>

     public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2602">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2602">Parameters</span></span>

| <span data-ttu-id="d9e27-2603">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2603">Parameter name</span></span> |  <span data-ttu-id="d9e27-2604">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2604">Parameter type</span></span> | <span data-ttu-id="d9e27-2605">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2605">Optional</span></span> | <span data-ttu-id="d9e27-2606">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2606">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2607">_data</span><span class="sxs-lookup"><span data-stu-id="d9e27-2607">_data</span></span> | <span data-ttu-id="d9e27-2608">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="d9e27-2608">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="d9e27-2609">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2609">True</span></span> | <span data-ttu-id="d9e27-2610">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2610">Data of the page</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2611">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2611">Return Value</span></span> 
<span data-ttu-id="d9e27-2612">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2612">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="d9e27-2613">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="d9e27-2613">Method failedInAppCall</span></span> 
<span data-ttu-id="d9e27-2614">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2614">Data of the page</span></span>

     public boolean failedInAppCall ([boolean _failedInAppCall]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2615">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2615">Parameters</span></span>

| <span data-ttu-id="d9e27-2616">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2616">Parameter name</span></span> |  <span data-ttu-id="d9e27-2617">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2617">Parameter type</span></span> | <span data-ttu-id="d9e27-2618">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2618">Optional</span></span> | <span data-ttu-id="d9e27-2619">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2619">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2620">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="d9e27-2620">_failedInAppCall</span></span> | <span data-ttu-id="d9e27-2621">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2621">boolean</span></span> | <span data-ttu-id="d9e27-2622">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2622">True</span></span> | <span data-ttu-id="d9e27-2623">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2623">Sets to true if it fails in calling application code</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2624">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2624">Return Value</span></span> 
<span data-ttu-id="d9e27-2625">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2625">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="d9e27-2626">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="d9e27-2626">Method commits</span></span> 
<span data-ttu-id="d9e27-2627">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2627">Commits after task is completed</span></span>

     public List commits () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2628">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2628">Return Value</span></span> 
<span data-ttu-id="d9e27-2629">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2629">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="d9e27-2630">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="d9e27-2630">Method messages</span></span> 
<span data-ttu-id="d9e27-2631">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="d9e27-2631">Job Id of the request</span></span>

     public List messages () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2632">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2632">Return Value</span></span> 
<span data-ttu-id="d9e27-2633">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2633">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="d9e27-2634">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-2634">Method addMessage</span></span> 
<span data-ttu-id="d9e27-2635">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-2635">Adds message</span></span>

     public void addMessage (SysAppResponseMessage _message) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2636">Parameters</span></span>

| <span data-ttu-id="d9e27-2637">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2637">Parameter name</span></span> |  <span data-ttu-id="d9e27-2638">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2638">Parameter type</span></span> | <span data-ttu-id="d9e27-2639">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2639">Optional</span></span> | <span data-ttu-id="d9e27-2640">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2640">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2641">_message</span><span class="sxs-lookup"><span data-stu-id="d9e27-2641">_message</span></span> | <span data-ttu-id="d9e27-2642">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-2642">SysAppResponseMessage</span></span> | <span data-ttu-id="d9e27-2643">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2643">False</span></span> | <span data-ttu-id="d9e27-2644">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2644">message as SysAppResponseMessage object</span></span>


### <a name="method-addcommit"></a><span data-ttu-id="d9e27-2645">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="d9e27-2645">Method addCommit</span></span> 
<span data-ttu-id="d9e27-2646">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="d9e27-2646">Adds commits</span></span>

     public void addCommit (SysAppEntityContext _entityContext) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2647">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2647">Parameters</span></span>

| <span data-ttu-id="d9e27-2648">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2648">Parameter name</span></span> |  <span data-ttu-id="d9e27-2649">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2649">Parameter type</span></span> | <span data-ttu-id="d9e27-2650">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2650">Optional</span></span> | <span data-ttu-id="d9e27-2651">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2651">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2652">_entityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2652">_entityContext</span></span> | <span data-ttu-id="d9e27-2653">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="d9e27-2653">SysAppEntityContext</span></span> | <span data-ttu-id="d9e27-2654">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2654">False</span></span> | <span data-ttu-id="d9e27-2655">確定済のエンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2655">Entity context containing entity name and entity id of the entity that is committed</span></span>


## <a name="class-sysappresponsemessage"></a><span data-ttu-id="d9e27-2656">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9e27-2656">Class SysAppResponseMessage</span></span> 
<span data-ttu-id="d9e27-2657">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-2657">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2658">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2658">Methods</span></span>

| <span data-ttu-id="d9e27-2659">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2659">Method name</span></span> | <span data-ttu-id="d9e27-2660">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2660">Returns</span></span> | <span data-ttu-id="d9e27-2661">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2661">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2662">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2662">new</span></span> | <span data-ttu-id="d9e27-2663">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2663">void</span></span> | <span data-ttu-id="d9e27-2664">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2664">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="d9e27-2665">テキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2665">text</span></span> | <span data-ttu-id="d9e27-2666">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2666">str</span></span> | <span data-ttu-id="d9e27-2667">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2667">Gets the message text</span></span> |
| <span data-ttu-id="d9e27-2668">タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2668">type</span></span> | <span data-ttu-id="d9e27-2669">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="d9e27-2669">SysAppMessageType</span></span> | <span data-ttu-id="d9e27-2670">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-2670">Gets the message type: info, error , warning</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2671">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2671">Method new</span></span> 
<span data-ttu-id="d9e27-2672">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2672">Creates a new instance of SysAppResponseMessage class</span></span>

     public void new (str _text, [SysAppMessageType _type]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2673">Parameters</span></span>

| <span data-ttu-id="d9e27-2674">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2674">Parameter name</span></span> |  <span data-ttu-id="d9e27-2675">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2675">Parameter type</span></span> | <span data-ttu-id="d9e27-2676">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2676">Optional</span></span> | <span data-ttu-id="d9e27-2677">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2677">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2678">_text</span><span class="sxs-lookup"><span data-stu-id="d9e27-2678">_text</span></span> | <span data-ttu-id="d9e27-2679">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2679">str</span></span> | <span data-ttu-id="d9e27-2680">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2680">False</span></span> | <span data-ttu-id="d9e27-2681">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2681">The message text</span></span>
| <span data-ttu-id="d9e27-2682">_type</span><span class="sxs-lookup"><span data-stu-id="d9e27-2682">_type</span></span> | <span data-ttu-id="d9e27-2683">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="d9e27-2683">SysAppMessageType</span></span> | <span data-ttu-id="d9e27-2684">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2684">True</span></span> | <span data-ttu-id="d9e27-2685">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-2685">Message Type: info, error , warning</span></span>


### <a name="method-text"></a><span data-ttu-id="d9e27-2686">メソッド text</span><span class="sxs-lookup"><span data-stu-id="d9e27-2686">Method text</span></span> 
<span data-ttu-id="d9e27-2687">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2687">Gets the message text</span></span>

     public str text () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2688">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2688">Return Value</span></span> 
<span data-ttu-id="d9e27-2689">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2689">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="d9e27-2690">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2690">Method type</span></span> 
<span data-ttu-id="d9e27-2691">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-2691">Gets the message type: info, error , warning</span></span>

     public SysAppMessageType type () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2692">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2692">Return Value</span></span> 
<span data-ttu-id="d9e27-2693">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="d9e27-2693">The message type: info, error , warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="d9e27-2694">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2694">Class SysAppSecurityAttribute</span></span> 
<span data-ttu-id="d9e27-2695">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2695">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="d9e27-2696">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2696">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2697">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2697">Methods</span></span>

| <span data-ttu-id="d9e27-2698">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2698">Method name</span></span> | <span data-ttu-id="d9e27-2699">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2699">Returns</span></span> | <span data-ttu-id="d9e27-2700">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2700">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2701">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2701">new</span></span> | <span data-ttu-id="d9e27-2702">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2702">void</span></span> | <span data-ttu-id="d9e27-2703">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2703">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="d9e27-2704">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2704">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="d9e27-2705">menuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-2705">menuItemType</span></span> | <span data-ttu-id="d9e27-2706">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-2706">MenuItemType</span></span> | <span data-ttu-id="d9e27-2707">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2707">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="d9e27-2708">menuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2708">menuItemName</span></span> | <span data-ttu-id="d9e27-2709">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2709">MenuItemName</span></span> | <span data-ttu-id="d9e27-2710">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2710">Gets the Menu Item Name of the page</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2711">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2711">Method new</span></span> 
<span data-ttu-id="d9e27-2712">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2712">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="d9e27-2713">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2713">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

     public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2714">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2714">Parameters</span></span>

| <span data-ttu-id="d9e27-2715">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2715">Parameter name</span></span> |  <span data-ttu-id="d9e27-2716">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2716">Parameter type</span></span> | <span data-ttu-id="d9e27-2717">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2717">Optional</span></span> | <span data-ttu-id="d9e27-2718">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2718">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2719">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2719">_menuItemName</span></span> | <span data-ttu-id="d9e27-2720">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2720">MenuItemName</span></span> | <span data-ttu-id="d9e27-2721">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2721">True</span></span> | <span data-ttu-id="d9e27-2722">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2722">Menu Item Name of the page</span></span>
| <span data-ttu-id="d9e27-2723">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-2723">_menuItemType</span></span> | <span data-ttu-id="d9e27-2724">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-2724">MenuItemType</span></span> | <span data-ttu-id="d9e27-2725">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2725">True</span></span> | <span data-ttu-id="d9e27-2726">アクション、表示または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2726">Menu Item Type of the page like action, display or output</span></span>


### <a name="method-menuitemtype"></a><span data-ttu-id="d9e27-2727">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-2727">Method menuItemType</span></span> 
<span data-ttu-id="d9e27-2728">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2728">Gets the Menu Item Type of the page</span></span>

     public MenuItemType menuItemType () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2729">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2729">Return Value</span></span> 
<span data-ttu-id="d9e27-2730">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2730">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="d9e27-2731">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2731">Method menuItemName</span></span> 
<span data-ttu-id="d9e27-2732">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="d9e27-2732">Gets the Menu Item Name of the page</span></span>

     public MenuItemName menuItemName () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2733">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2733">Return Value</span></span> 
<span data-ttu-id="d9e27-2734">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2734">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="d9e27-2735">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="d9e27-2735">Class SysAppWorkspace</span></span> 
<span data-ttu-id="d9e27-2736">これは、AX モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2736">This is the base class of AX mobile workspace.</span></span> <span data-ttu-id="d9e27-2737">AX モバイル ワークスペース クラスは、このクラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2737">AX mobile workspace classes needs to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2738">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-2738">Methods</span></span>

| <span data-ttu-id="d9e27-2739">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2739">Method name</span></span> | <span data-ttu-id="d9e27-2740">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2740">Returns</span></span> | <span data-ttu-id="d9e27-2741">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2741">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2742">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-2742">getEnumValues</span></span> | <span data-ttu-id="d9e27-2743">リスト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2743">List</span></span> | <span data-ttu-id="d9e27-2744">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2744">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-2745">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2745">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="d9e27-2746">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2746">getWorkspaceMetadata</span></span> | <span data-ttu-id="d9e27-2747">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2747">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="d9e27-2748">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2748">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-2749">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2749">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="d9e27-2750">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-2750">onBeginAppJob</span></span> | <span data-ttu-id="d9e27-2751">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2751">void</span></span> | <span data-ttu-id="d9e27-2752">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-2752">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="d9e27-2753">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-2753">onEndAppJob</span></span> | <span data-ttu-id="d9e27-2754">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2754">void</span></span> | <span data-ttu-id="d9e27-2755">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-2755">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="d9e27-2756">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2756">workspaceHidden</span></span> | <span data-ttu-id="d9e27-2757">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2757">boolean</span></span> | <span data-ttu-id="d9e27-2758">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2758">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="d9e27-2759">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2759">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="d9e27-2760">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2760">If the attribute is not specified on the class than it always returns false</span></span> |


### <a name="method-getenumvalues"></a><span data-ttu-id="d9e27-2761">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="d9e27-2761">Method getEnumValues</span></span> 
<span data-ttu-id="d9e27-2762">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2762">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-2763">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2763">Can be used to modify the enum values that are returned to AX mobile</span></span>

     public List getEnumValues (EnumName _enumName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2764">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2764">Parameters</span></span>

| <span data-ttu-id="d9e27-2765">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2765">Parameter name</span></span> |  <span data-ttu-id="d9e27-2766">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2766">Parameter type</span></span> | <span data-ttu-id="d9e27-2767">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2767">Optional</span></span> | <span data-ttu-id="d9e27-2768">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2768">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2769">_enumName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2769">_enumName</span></span> | <span data-ttu-id="d9e27-2770">EnumName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2770">EnumName</span></span> | <span data-ttu-id="d9e27-2771">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2771">False</span></span> | <span data-ttu-id="d9e27-2772">列挙名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2772">The enum name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2773">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2773">Return Value</span></span> 
<span data-ttu-id="d9e27-2774">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="d9e27-2774">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="d9e27-2775">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2775">Method getWorkspaceMetadata</span></span> 
<span data-ttu-id="d9e27-2776">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2776">Called during workspace initialization.</span></span> <span data-ttu-id="d9e27-2777">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="d9e27-2777">Can be used to modify the workspace metadata</span></span>

     public SysAppWorkspaceMetadata getWorkspaceMetadata () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2778">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2778">Return Value</span></span> 
<span data-ttu-id="d9e27-2779">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2779">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="d9e27-2780">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-2780">Method onBeginAppJob</span></span> 
<span data-ttu-id="d9e27-2781">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-2781">Called before the start of execution of AX mobile job</span></span>

     public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2782">Parameters</span></span>

| <span data-ttu-id="d9e27-2783">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2783">Parameter name</span></span> |  <span data-ttu-id="d9e27-2784">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2784">Parameter type</span></span> | <span data-ttu-id="d9e27-2785">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2785">Optional</span></span> | <span data-ttu-id="d9e27-2786">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2786">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2787">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="d9e27-2787">_sysAppJobRequest</span></span> | <span data-ttu-id="d9e27-2788">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="d9e27-2788">SysAppJobRequest</span></span> | <span data-ttu-id="d9e27-2789">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2789">False</span></span> | <span data-ttu-id="d9e27-2790">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-2790">A class containing job request parameters</span></span>


### <a name="method-onendappjob"></a><span data-ttu-id="d9e27-2791">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="d9e27-2791">Method onEndAppJob</span></span> 
<span data-ttu-id="d9e27-2792">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="d9e27-2792">Called after the end of execution of AX mobile job</span></span>

     public void onEndAppJob (SysAppJobResponse _sysAppJobResponse) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2793">Parameters</span></span>

| <span data-ttu-id="d9e27-2794">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2794">Parameter name</span></span> |  <span data-ttu-id="d9e27-2795">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2795">Parameter type</span></span> | <span data-ttu-id="d9e27-2796">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2796">Optional</span></span> | <span data-ttu-id="d9e27-2797">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2797">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2798">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="d9e27-2798">_sysAppJobResponse</span></span> | <span data-ttu-id="d9e27-2799">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="d9e27-2799">SysAppJobResponse</span></span> | <span data-ttu-id="d9e27-2800">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2800">False</span></span> | <span data-ttu-id="d9e27-2801">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="d9e27-2801">A class containing job response parameters</span></span>


### <a name="method-workspacehidden"></a><span data-ttu-id="d9e27-2802">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2802">Method workspaceHidden</span></span> 
<span data-ttu-id="d9e27-2803">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2803">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="d9e27-2804">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2804">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="d9e27-2805">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2805">If the attribute is not specified on the class than it always returns false</span></span>

     public boolean workspaceHidden () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2806">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2806">Return Value</span></span> 
<span data-ttu-id="d9e27-2807">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2807">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="d9e27-2808">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2808">Class SysAppWorkspaceAttribute</span></span> 
<span data-ttu-id="d9e27-2809">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2809">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2810">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-2810">Methods</span></span>

| <span data-ttu-id="d9e27-2811">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2811">Method name</span></span> | <span data-ttu-id="d9e27-2812">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2812">Returns</span></span> | <span data-ttu-id="d9e27-2813">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2813">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2814">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2814">new</span></span> | <span data-ttu-id="d9e27-2815">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2815">void</span></span> | <span data-ttu-id="d9e27-2816">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2816">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="d9e27-2817">AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2817">AppId</span></span> | <span data-ttu-id="d9e27-2818">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2818">str</span></span> | <span data-ttu-id="d9e27-2819">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2819">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="d9e27-2820">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2820">AppResourceName</span></span> | <span data-ttu-id="d9e27-2821">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2821">str</span></span> | <span data-ttu-id="d9e27-2822">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2822">Gets or sets the AOT Resource name which contains the workspace</span></span> |
| <span data-ttu-id="d9e27-2823">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2823">WorkspaceHidden</span></span> | <span data-ttu-id="d9e27-2824">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2824">boolean</span></span> | <span data-ttu-id="d9e27-2825">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2825">Gets or sets if the workspace is hidden from designer</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2826">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2826">Method new</span></span> 
<span data-ttu-id="d9e27-2827">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9e27-2827">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

     public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2828">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2828">Parameters</span></span>

| <span data-ttu-id="d9e27-2829">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2829">Parameter name</span></span> |  <span data-ttu-id="d9e27-2830">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2830">Parameter type</span></span> | <span data-ttu-id="d9e27-2831">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2831">Optional</span></span> | <span data-ttu-id="d9e27-2832">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2832">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2833">_appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2833">_appId</span></span> | <span data-ttu-id="d9e27-2834">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2834">str</span></span> | <span data-ttu-id="d9e27-2835">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2835">False</span></span> | <span data-ttu-id="d9e27-2836">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2836">The appId of the workspace</span></span>
| <span data-ttu-id="d9e27-2837">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2837">_appResourceName</span></span> | <span data-ttu-id="d9e27-2838">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2838">str</span></span> | <span data-ttu-id="d9e27-2839">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2839">True</span></span> | <span data-ttu-id="d9e27-2840">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2840">The AOT resource name which contains the workspace</span></span>
| <span data-ttu-id="d9e27-2841">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2841">_workspaceHidden</span></span> | <span data-ttu-id="d9e27-2842">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2842">boolean</span></span> | <span data-ttu-id="d9e27-2843">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2843">True</span></span> | <span data-ttu-id="d9e27-2844">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="d9e27-2844">The workspace is hidden from designer</span></span>


### <a name="method-appid"></a><span data-ttu-id="d9e27-2845">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2845">Method AppId</span></span> 
<span data-ttu-id="d9e27-2846">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2846">Gets or sets the AppId of the workspace</span></span>

     public str AppId ([str _appId]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2847">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2847">Parameters</span></span>

| <span data-ttu-id="d9e27-2848">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2848">Parameter name</span></span> |  <span data-ttu-id="d9e27-2849">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2849">Parameter type</span></span> | <span data-ttu-id="d9e27-2850">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2850">Optional</span></span> | <span data-ttu-id="d9e27-2851">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2851">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2852">_appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2852">_appId</span></span> | <span data-ttu-id="d9e27-2853">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2853">str</span></span> | <span data-ttu-id="d9e27-2854">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2854">True</span></span> | <span data-ttu-id="d9e27-2855">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2855">The AppId of the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2856">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2856">Return Value</span></span> 
<span data-ttu-id="d9e27-2857">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2857">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="d9e27-2858">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2858">Method AppResourceName</span></span> 
<span data-ttu-id="d9e27-2859">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2859">Gets or sets the AOT Resource name which contains the workspace</span></span>

     public str AppResourceName ([str _appResourceName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2860">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2860">Parameters</span></span>

| <span data-ttu-id="d9e27-2861">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2861">Parameter name</span></span> |  <span data-ttu-id="d9e27-2862">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2862">Parameter type</span></span> | <span data-ttu-id="d9e27-2863">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2863">Optional</span></span> | <span data-ttu-id="d9e27-2864">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2864">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2865">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2865">_appResourceName</span></span> | <span data-ttu-id="d9e27-2866">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2866">str</span></span> | <span data-ttu-id="d9e27-2867">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2867">True</span></span> | <span data-ttu-id="d9e27-2868">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2868">The AOT Resource name which contains the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2869">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2869">Return Value</span></span> 
<span data-ttu-id="d9e27-2870">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2870">The AOT Resource name which contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="d9e27-2871">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2871">Method WorkspaceHidden</span></span> 
<span data-ttu-id="d9e27-2872">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2872">Gets or sets if the workspace is hidden from designer</span></span>

     public boolean WorkspaceHidden ([boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2873">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2873">Parameters</span></span>

| <span data-ttu-id="d9e27-2874">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2874">Parameter name</span></span> |  <span data-ttu-id="d9e27-2875">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2875">Parameter type</span></span> | <span data-ttu-id="d9e27-2876">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2876">Optional</span></span> | <span data-ttu-id="d9e27-2877">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2877">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2878">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="d9e27-2878">_workspaceHidden</span></span> | <span data-ttu-id="d9e27-2879">ブール値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2879">boolean</span></span> | <span data-ttu-id="d9e27-2880">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2880">True</span></span> | <span data-ttu-id="d9e27-2881">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="d9e27-2881">The workspace hidden</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2882">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2882">Return Value</span></span> 
<span data-ttu-id="d9e27-2883">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="d9e27-2883">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="d9e27-2884">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2884">Class SysAppWorkspaceMetadata</span></span> 
<span data-ttu-id="d9e27-2885">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2885">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-2886">方法</span><span class="sxs-lookup"><span data-stu-id="d9e27-2886">Methods</span></span>

| <span data-ttu-id="d9e27-2887">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2887">Method name</span></span> | <span data-ttu-id="d9e27-2888">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-2888">Returns</span></span> | <span data-ttu-id="d9e27-2889">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2889">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-2890">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-2890">new</span></span> | <span data-ttu-id="d9e27-2891">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2891">void</span></span> |  |
| <span data-ttu-id="d9e27-2892">addConfig</span><span class="sxs-lookup"><span data-stu-id="d9e27-2892">addConfig</span></span> | <span data-ttu-id="d9e27-2893">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-2893">void</span></span> | <span data-ttu-id="d9e27-2894">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2894">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="d9e27-2895">getPage</span><span class="sxs-lookup"><span data-stu-id="d9e27-2895">getPage</span></span> | <span data-ttu-id="d9e27-2896">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2896">SysAppPageMetadata</span></span> | <span data-ttu-id="d9e27-2897">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2897">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="d9e27-2898">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2898">getPageEnumerator</span></span> | <span data-ttu-id="d9e27-2899">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2899">MapEnumerator</span></span> | <span data-ttu-id="d9e27-2900">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2900">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="d9e27-2901">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-2901">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="d9e27-2902">getAction</span><span class="sxs-lookup"><span data-stu-id="d9e27-2902">getAction</span></span> | <span data-ttu-id="d9e27-2903">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="d9e27-2903">SysAppActionMetadata</span></span> | <span data-ttu-id="d9e27-2904">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2904">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="d9e27-2905">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2905">getActionEnumerator</span></span> | <span data-ttu-id="d9e27-2906">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2906">MapEnumerator</span></span> | <span data-ttu-id="d9e27-2907">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2907">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="d9e27-2908">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-2908">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="d9e27-2909">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2909">getPageNameForRecordingId</span></span> | <span data-ttu-id="d9e27-2910">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2910">str</span></span> | <span data-ttu-id="d9e27-2911">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2911">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="d9e27-2912">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2912">getActionNameForRecordingId</span></span> | <span data-ttu-id="d9e27-2913">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2913">str</span></span> | <span data-ttu-id="d9e27-2914">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2914">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="d9e27-2915">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-2915">workspaceTitle</span></span> | <span data-ttu-id="d9e27-2916">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2916">str</span></span> | <span data-ttu-id="d9e27-2917">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2917">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="d9e27-2918">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-2918">workspaceDescription</span></span> | <span data-ttu-id="d9e27-2919">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2919">str</span></span> | <span data-ttu-id="d9e27-2920">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-2920">Gets and sets the workspace description</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-2921">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-2921">Method new</span></span> 


     public void new (str _appId, [SysAppWorkspaceAttribute _attribute]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2922">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2922">Parameters</span></span>

| <span data-ttu-id="d9e27-2923">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2923">Parameter name</span></span> |  <span data-ttu-id="d9e27-2924">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2924">Parameter type</span></span> | <span data-ttu-id="d9e27-2925">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2925">Optional</span></span> | <span data-ttu-id="d9e27-2926">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2926">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2927">_appId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2927">_appId</span></span> | <span data-ttu-id="d9e27-2928">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2928">str</span></span> | <span data-ttu-id="d9e27-2929">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2929">False</span></span> | 
| <span data-ttu-id="d9e27-2930">_attribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2930">_attribute</span></span> | <span data-ttu-id="d9e27-2931">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-2931">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="d9e27-2932">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-2932">True</span></span> | 


### <a name="method-addconfig"></a><span data-ttu-id="d9e27-2933">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="d9e27-2933">Method addConfig</span></span> 
<span data-ttu-id="d9e27-2934">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2934">Adds a custom config to the mobile workspace metadata</span></span>

     public void addConfig (str _configName, object _configValue) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2935">Parameters</span></span>

| <span data-ttu-id="d9e27-2936">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2936">Parameter name</span></span> |  <span data-ttu-id="d9e27-2937">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2937">Parameter type</span></span> | <span data-ttu-id="d9e27-2938">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2938">Optional</span></span> | <span data-ttu-id="d9e27-2939">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2939">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2940">_configName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2940">_configName</span></span> | <span data-ttu-id="d9e27-2941">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2941">str</span></span> | <span data-ttu-id="d9e27-2942">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2942">False</span></span> | <span data-ttu-id="d9e27-2943">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2943">A config name</span></span>
| <span data-ttu-id="d9e27-2944">_configValue</span><span class="sxs-lookup"><span data-stu-id="d9e27-2944">_configValue</span></span> | <span data-ttu-id="d9e27-2945">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2945">object</span></span> | <span data-ttu-id="d9e27-2946">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2946">False</span></span> | <span data-ttu-id="d9e27-2947">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9e27-2947">An object of a X++ data contract class</span></span>


### <a name="method-getpage"></a><span data-ttu-id="d9e27-2948">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="d9e27-2948">Method getPage</span></span> 
<span data-ttu-id="d9e27-2949">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2949">Returns the page with the pageName provided</span></span>

     public SysAppPageMetadata getPage (str _pageName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2950">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2950">Parameters</span></span>

| <span data-ttu-id="d9e27-2951">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2951">Parameter name</span></span> |  <span data-ttu-id="d9e27-2952">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2952">Parameter type</span></span> | <span data-ttu-id="d9e27-2953">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2953">Optional</span></span> | <span data-ttu-id="d9e27-2954">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2954">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2955">_pageName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2955">_pageName</span></span> | <span data-ttu-id="d9e27-2956">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2956">str</span></span> | <span data-ttu-id="d9e27-2957">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2957">False</span></span> | <span data-ttu-id="d9e27-2958">ページ名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2958">A page name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2959">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2959">Return Value</span></span> 
<span data-ttu-id="d9e27-2960">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2960">Returns the pageMetadata if a page with the provided name exist; otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="d9e27-2961">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2961">Method getPageEnumerator</span></span> 
<span data-ttu-id="d9e27-2962">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2962">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="d9e27-2963">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-2963">Where key is page name and value is of type SysAppPageMetadata</span></span>

     public MapEnumerator getPageEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2964">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2964">Return Value</span></span> 
<span data-ttu-id="d9e27-2965">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2965">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="d9e27-2966">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="d9e27-2966">Method getAction</span></span> 
<span data-ttu-id="d9e27-2967">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2967">Returns the action with the actionName provided</span></span>

     public SysAppActionMetadata getAction (str _actionName) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2968">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2968">Parameters</span></span>

| <span data-ttu-id="d9e27-2969">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2969">Parameter name</span></span> |  <span data-ttu-id="d9e27-2970">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2970">Parameter type</span></span> | <span data-ttu-id="d9e27-2971">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2971">Optional</span></span> | <span data-ttu-id="d9e27-2972">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2972">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2973">_actionName</span><span class="sxs-lookup"><span data-stu-id="d9e27-2973">_actionName</span></span> | <span data-ttu-id="d9e27-2974">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2974">str</span></span> | <span data-ttu-id="d9e27-2975">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2975">False</span></span> | <span data-ttu-id="d9e27-2976">アクション名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2976">An action name</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2977">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2977">Return Value</span></span> 
<span data-ttu-id="d9e27-2978">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2978">Returns the ActionMetadata if an action with the provided name exist; otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="d9e27-2979">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="d9e27-2979">Method getActionEnumerator</span></span> 
<span data-ttu-id="d9e27-2980">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2980">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="d9e27-2981">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="d9e27-2981">Where key is action name and value is of type SysAppActionMetadata</span></span>

     public MapEnumerator getActionEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="d9e27-2982">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2982">Return Value</span></span> 
<span data-ttu-id="d9e27-2983">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="d9e27-2983">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="d9e27-2984">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2984">Method getPageNameForRecordingId</span></span> 
<span data-ttu-id="d9e27-2985">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2985">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

     public str getPageNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2986">Parameters</span></span>

| <span data-ttu-id="d9e27-2987">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-2987">Parameter name</span></span> |  <span data-ttu-id="d9e27-2988">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-2988">Parameter type</span></span> | <span data-ttu-id="d9e27-2989">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-2989">Optional</span></span> | <span data-ttu-id="d9e27-2990">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-2990">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-2991">_recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2991">_recordingId</span></span> | <span data-ttu-id="d9e27-2992">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-2992">str</span></span> | <span data-ttu-id="d9e27-2993">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-2993">False</span></span> | <span data-ttu-id="d9e27-2994">recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2994">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-2995">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-2995">Return Value</span></span> 
<span data-ttu-id="d9e27-2996">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d9e27-2996">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="d9e27-2997">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-2997">Method getActionNameForRecordingId</span></span> 
<span data-ttu-id="d9e27-2998">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="d9e27-2998">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

     public str getActionNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-2999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-2999">Parameters</span></span>

| <span data-ttu-id="d9e27-3000">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3000">Parameter name</span></span> |  <span data-ttu-id="d9e27-3001">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3001">Parameter type</span></span> | <span data-ttu-id="d9e27-3002">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-3002">Optional</span></span> | <span data-ttu-id="d9e27-3003">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3003">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-3004">_recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-3004">_recordingId</span></span> | <span data-ttu-id="d9e27-3005">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-3005">str</span></span> | <span data-ttu-id="d9e27-3006">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-3006">False</span></span> | <span data-ttu-id="d9e27-3007">recordingId</span><span class="sxs-lookup"><span data-stu-id="d9e27-3007">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-3008">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-3008">Return Value</span></span> 
<span data-ttu-id="d9e27-3009">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d9e27-3009">An action name if the supplied recordingId is used by a workspace action;otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="d9e27-3010">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-3010">Method workspaceTitle</span></span> 
<span data-ttu-id="d9e27-3011">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-3011">Gets and sets the workspace title</span></span>

     public str workspaceTitle ([str _workspaceTitle]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-3012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-3012">Parameters</span></span>

| <span data-ttu-id="d9e27-3013">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3013">Parameter name</span></span> |  <span data-ttu-id="d9e27-3014">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3014">Parameter type</span></span> | <span data-ttu-id="d9e27-3015">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-3015">Optional</span></span> | <span data-ttu-id="d9e27-3016">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3016">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-3017">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="d9e27-3017">_workspaceTitle</span></span> | <span data-ttu-id="d9e27-3018">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-3018">str</span></span> | <span data-ttu-id="d9e27-3019">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-3019">True</span></span> | <span data-ttu-id="d9e27-3020">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-3020">The workspace title</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-3021">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-3021">Return Value</span></span> 
<span data-ttu-id="d9e27-3022">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="d9e27-3022">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="d9e27-3023">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-3023">Method workspaceDescription</span></span> 
<span data-ttu-id="d9e27-3024">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-3024">Gets and sets the workspace description</span></span>

     public str workspaceDescription ([str _workspaceDescription]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-3025">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-3025">Parameters</span></span>

| <span data-ttu-id="d9e27-3026">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3026">Parameter name</span></span> |  <span data-ttu-id="d9e27-3027">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3027">Parameter type</span></span> | <span data-ttu-id="d9e27-3028">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-3028">Optional</span></span> | <span data-ttu-id="d9e27-3029">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3029">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-3030">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="d9e27-3030">_workspaceDescription</span></span> | <span data-ttu-id="d9e27-3031">str</span><span class="sxs-lookup"><span data-stu-id="d9e27-3031">str</span></span> | <span data-ttu-id="d9e27-3032">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-3032">True</span></span> | <span data-ttu-id="d9e27-3033">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3033">The workspace description</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-3034">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-3034">Return Value</span></span> 
<span data-ttu-id="d9e27-3035">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3035">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="d9e27-3036">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="d9e27-3036">Class SysAppWorkspaceSecurityAttribute</span></span> 
<span data-ttu-id="d9e27-3037">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d9e27-3037">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="d9e27-3038">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9e27-3038">Methods</span></span>

| <span data-ttu-id="d9e27-3039">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3039">Method name</span></span> | <span data-ttu-id="d9e27-3040">返品</span><span class="sxs-lookup"><span data-stu-id="d9e27-3040">Returns</span></span> | <span data-ttu-id="d9e27-3041">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3041">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="d9e27-3042">新規</span><span class="sxs-lookup"><span data-stu-id="d9e27-3042">new</span></span> | <span data-ttu-id="d9e27-3043">無効</span><span class="sxs-lookup"><span data-stu-id="d9e27-3043">void</span></span> | <span data-ttu-id="d9e27-3044">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="d9e27-3044">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="d9e27-3045">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-3045">WorkspaceMenuItemName</span></span> | <span data-ttu-id="d9e27-3046">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-3046">MenuItemName</span></span> | <span data-ttu-id="d9e27-3047">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-3047">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="d9e27-3048">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-3048">WorkspaceMenuItemType</span></span> | <span data-ttu-id="d9e27-3049">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-3049">MenuItemType</span></span> | <span data-ttu-id="d9e27-3050">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-3050">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |


### <a name="method-new"></a><span data-ttu-id="d9e27-3051">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d9e27-3051">Method new</span></span> 
<span data-ttu-id="d9e27-3052">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="d9e27-3052">Creates a new instance of attribute</span></span>

     public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-3053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-3053">Parameters</span></span>

| <span data-ttu-id="d9e27-3054">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3054">Parameter name</span></span> |  <span data-ttu-id="d9e27-3055">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3055">Parameter type</span></span> | <span data-ttu-id="d9e27-3056">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-3056">Optional</span></span> | <span data-ttu-id="d9e27-3057">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3057">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-3058">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-3058">_workspaceMenuItemName</span></span> | <span data-ttu-id="d9e27-3059">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-3059">MenuItemName</span></span> | <span data-ttu-id="d9e27-3060">False</span><span class="sxs-lookup"><span data-stu-id="d9e27-3060">False</span></span> | <span data-ttu-id="d9e27-3061">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3061">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="d9e27-3062">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-3062">_workspaceMenuItemType</span></span> | <span data-ttu-id="d9e27-3063">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-3063">MenuItemType</span></span> | <span data-ttu-id="d9e27-3064">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-3064">True</span></span> | <span data-ttu-id="d9e27-3065">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3065">The menu item type</span></span>


### <a name="method-workspacemenuitemname"></a><span data-ttu-id="d9e27-3066">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-3066">Method WorkspaceMenuItemName</span></span> 
<span data-ttu-id="d9e27-3067">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-3067">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

     public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-3068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-3068">Parameters</span></span>

| <span data-ttu-id="d9e27-3069">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3069">Parameter name</span></span> |  <span data-ttu-id="d9e27-3070">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3070">Parameter type</span></span> | <span data-ttu-id="d9e27-3071">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-3071">Optional</span></span> | <span data-ttu-id="d9e27-3072">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3072">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-3073">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-3073">_workspaceMenuItemName</span></span> | <span data-ttu-id="d9e27-3074">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="d9e27-3074">MenuItemName</span></span> | <span data-ttu-id="d9e27-3075">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-3075">True</span></span> | <span data-ttu-id="d9e27-3076">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="d9e27-3076">The workspace menu item for the workspace security attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-3077">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-3077">Return Value</span></span> 
<span data-ttu-id="d9e27-3078">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="d9e27-3078">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="d9e27-3079">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-3079">Method WorkspaceMenuItemType</span></span> 
<span data-ttu-id="d9e27-3080">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="d9e27-3080">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

     public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="d9e27-3081">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e27-3081">Parameters</span></span>

| <span data-ttu-id="d9e27-3082">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="d9e27-3082">Parameter name</span></span> |  <span data-ttu-id="d9e27-3083">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3083">Parameter type</span></span> | <span data-ttu-id="d9e27-3084">オプション</span><span class="sxs-lookup"><span data-stu-id="d9e27-3084">Optional</span></span> | <span data-ttu-id="d9e27-3085">説明</span><span class="sxs-lookup"><span data-stu-id="d9e27-3085">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="d9e27-3086">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-3086">_workspaceMenuItemType</span></span> | <span data-ttu-id="d9e27-3087">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="d9e27-3087">MenuItemType</span></span> | <span data-ttu-id="d9e27-3088">はい</span><span class="sxs-lookup"><span data-stu-id="d9e27-3088">True</span></span> | <span data-ttu-id="d9e27-3089">workspacesecurity 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3089">The workspace menu item type for the workspacesecurity attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="d9e27-3090">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9e27-3090">Return Value</span></span> 
<span data-ttu-id="d9e27-3091">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="d9e27-3091">The workspace menu item type for the workspace security attribute</span></span>
