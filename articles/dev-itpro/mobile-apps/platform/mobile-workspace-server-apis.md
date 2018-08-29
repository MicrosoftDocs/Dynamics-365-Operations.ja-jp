---
title: "サーバー側の開発 (ワークスペース X++ API)"
description: "Microsoft Dynamics 365 for Finance and Operations には、豊富なオフラインおよびモバイルの相互関係と、扱いやすいデザイナー体験を可能にする携帯電話アプリのサポートが含まれています。"
author: RobinARH
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.search.region: Global
ms.author: shshabazz
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: f3a1f7893aa7835c04b331045911eb3b9c47212e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="server-side-development-workspace-x-apis"></a><span data-ttu-id="74407-103">サーバー側の開発 (ワークスペース X++ API)</span><span class="sxs-lookup"><span data-stu-id="74407-103">Server-side development (workspace X++ APIs)</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="class-sysappactionattribute"></a><span data-ttu-id="74407-104">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-104">Class SysAppActionAttribute</span></span> 
<span data-ttu-id="74407-105">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-105">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-106">Methods</span></span>

| <span data-ttu-id="74407-107">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-107">Method name</span></span> | <span data-ttu-id="74407-108">返品</span><span class="sxs-lookup"><span data-stu-id="74407-108">Returns</span></span> | <span data-ttu-id="74407-109">説明</span><span class="sxs-lookup"><span data-stu-id="74407-109">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-110">新規</span><span class="sxs-lookup"><span data-stu-id="74407-110">new</span></span> | <span data-ttu-id="74407-111">無効</span><span class="sxs-lookup"><span data-stu-id="74407-111">void</span></span> | <span data-ttu-id="74407-112">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-112">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="74407-113">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="74407-113">pageMethodName</span></span> | <span data-ttu-id="74407-114">str</span><span class="sxs-lookup"><span data-stu-id="74407-114">str</span></span> | <span data-ttu-id="74407-115">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-115">Gets the get method name which forms the page under which this task resides</span></span> |
| <span data-ttu-id="74407-116">actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-116">actionTitle</span></span> | <span data-ttu-id="74407-117">str</span><span class="sxs-lookup"><span data-stu-id="74407-117">str</span></span> | <span data-ttu-id="74407-118">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-118">Gets the Action Title</span></span> |
| <span data-ttu-id="74407-119">actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-119">actionDescription</span></span> | <span data-ttu-id="74407-120">str</span><span class="sxs-lookup"><span data-stu-id="74407-120">str</span></span> | <span data-ttu-id="74407-121">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-121">Gets the Action Description</span></span> |
| <span data-ttu-id="74407-122">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="74407-122">crudOperationType</span></span> | <span data-ttu-id="74407-123">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="74407-123">SysAppCRUDOperation</span></span> | <span data-ttu-id="74407-124">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="74407-124">Gets the Crud Operation Type like Create, Update, Delete</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-125">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-125">Method new</span></span> 
<span data-ttu-id="74407-126">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-126">Creates a new instance of SysAppActionAttribute class</span></span>

     public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-127">Parameters</span></span>

| <span data-ttu-id="74407-128">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-128">Parameter name</span></span> |  <span data-ttu-id="74407-129">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-129">Parameter type</span></span> | <span data-ttu-id="74407-130">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-130">Optional</span></span> | <span data-ttu-id="74407-131">説明</span><span class="sxs-lookup"><span data-stu-id="74407-131">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-132">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-132">_actionTitle</span></span> | <span data-ttu-id="74407-133">str</span><span class="sxs-lookup"><span data-stu-id="74407-133">str</span></span> | <span data-ttu-id="74407-134">はい</span><span class="sxs-lookup"><span data-stu-id="74407-134">True</span></span> | <span data-ttu-id="74407-135">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-135">Action title</span></span>
| <span data-ttu-id="74407-136">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-136">_actionDescription</span></span> | <span data-ttu-id="74407-137">str</span><span class="sxs-lookup"><span data-stu-id="74407-137">str</span></span> | <span data-ttu-id="74407-138">はい</span><span class="sxs-lookup"><span data-stu-id="74407-138">True</span></span> | <span data-ttu-id="74407-139">アクション説明</span><span class="sxs-lookup"><span data-stu-id="74407-139">Action description</span></span>
| <span data-ttu-id="74407-140">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="74407-140">_crudOperationType</span></span> | <span data-ttu-id="74407-141">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="74407-141">SysAppCRUDOperation</span></span> | <span data-ttu-id="74407-142">はい</span><span class="sxs-lookup"><span data-stu-id="74407-142">True</span></span> | <span data-ttu-id="74407-143">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="74407-143">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="74407-144">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="74407-144">_pageMethodName</span></span> | <span data-ttu-id="74407-145">str</span><span class="sxs-lookup"><span data-stu-id="74407-145">str</span></span> | <span data-ttu-id="74407-146">はい</span><span class="sxs-lookup"><span data-stu-id="74407-146">True</span></span> | <span data-ttu-id="74407-147">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="74407-147">Name of the method constructing parent page</span></span>


### <a name="method-pagemethodname"></a><span data-ttu-id="74407-148">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="74407-148">Method pageMethodName</span></span> 
<span data-ttu-id="74407-149">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-149">Gets the get method name which forms the page under which this task resides</span></span>

     public str pageMethodName () 


#### <a name="return-value"></a><span data-ttu-id="74407-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-150">Return Value</span></span> 
<span data-ttu-id="74407-151">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-151">The page method name which forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="74407-152">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-152">Method actionTitle</span></span> 
<span data-ttu-id="74407-153">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-153">Gets the Action Title</span></span>

     public str actionTitle () 


#### <a name="return-value"></a><span data-ttu-id="74407-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-154">Return Value</span></span> 
<span data-ttu-id="74407-155">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-155">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="74407-156">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-156">Method actionDescription</span></span> 
<span data-ttu-id="74407-157">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-157">Gets the Action Description</span></span>

     public str actionDescription () 


#### <a name="return-value"></a><span data-ttu-id="74407-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-158">Return Value</span></span> 
<span data-ttu-id="74407-159">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-159">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="74407-160">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="74407-160">Method crudOperationType</span></span> 
<span data-ttu-id="74407-161">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="74407-161">Gets the Crud Operation Type like Create, Update, Delete</span></span>

     public SysAppCRUDOperation crudOperationType () 


#### <a name="return-value"></a><span data-ttu-id="74407-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-162">Return Value</span></span> 
<span data-ttu-id="74407-163">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-163">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="74407-164">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-164">Class SysAppActionMetadata</span></span> 
<span data-ttu-id="74407-165">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="74407-165">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="74407-166">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-166">Methods</span></span>

| <span data-ttu-id="74407-167">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-167">Method name</span></span> | <span data-ttu-id="74407-168">返品</span><span class="sxs-lookup"><span data-stu-id="74407-168">Returns</span></span> | <span data-ttu-id="74407-169">説明</span><span class="sxs-lookup"><span data-stu-id="74407-169">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-170">新規</span><span class="sxs-lookup"><span data-stu-id="74407-170">new</span></span> | <span data-ttu-id="74407-171">無効</span><span class="sxs-lookup"><span data-stu-id="74407-171">void</span></span> |  |
| <span data-ttu-id="74407-172">getActionName</span><span class="sxs-lookup"><span data-stu-id="74407-172">getActionName</span></span> | <span data-ttu-id="74407-173">str</span><span class="sxs-lookup"><span data-stu-id="74407-173">str</span></span> | <span data-ttu-id="74407-174">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-174">Returns the action name</span></span> |
| <span data-ttu-id="74407-175">actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-175">actionTitle</span></span> | <span data-ttu-id="74407-176">str</span><span class="sxs-lookup"><span data-stu-id="74407-176">str</span></span> | <span data-ttu-id="74407-177">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-177">Gets or sets the action title</span></span> |
| <span data-ttu-id="74407-178">actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-178">actionDescription</span></span> | <span data-ttu-id="74407-179">str</span><span class="sxs-lookup"><span data-stu-id="74407-179">str</span></span> | <span data-ttu-id="74407-180">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-180">Gets or sets the action description</span></span> |
| <span data-ttu-id="74407-181">actionHidden</span><span class="sxs-lookup"><span data-stu-id="74407-181">actionHidden</span></span> | <span data-ttu-id="74407-182">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-182">boolean</span></span> | <span data-ttu-id="74407-183">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-183">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="74407-184">actionOrder</span><span class="sxs-lookup"><span data-stu-id="74407-184">actionOrder</span></span> | <span data-ttu-id="74407-185">int</span><span class="sxs-lookup"><span data-stu-id="74407-185">int</span></span> | <span data-ttu-id="74407-186">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-186">Gets or sets the action order</span></span> |
| <span data-ttu-id="74407-187">getControl</span><span class="sxs-lookup"><span data-stu-id="74407-187">getControl</span></span> | <span data-ttu-id="74407-188">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-188">SysAppControlMetadata</span></span> | <span data-ttu-id="74407-189">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-189">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="74407-190">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-190">getControlEnumerator</span></span> | <span data-ttu-id="74407-191">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-191">MapEnumerator</span></span> | <span data-ttu-id="74407-192">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-192">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="74407-193">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-193">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-194">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-194">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata) 


#### <a name="parameters"></a><span data-ttu-id="74407-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-195">Parameters</span></span>

| <span data-ttu-id="74407-196">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-196">Parameter name</span></span> |  <span data-ttu-id="74407-197">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-197">Parameter type</span></span> | <span data-ttu-id="74407-198">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-198">Optional</span></span> | <span data-ttu-id="74407-199">説明</span><span class="sxs-lookup"><span data-stu-id="74407-199">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-200">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="74407-200">_taskmetadata</span></span> | <span data-ttu-id="74407-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="74407-202">False</span><span class="sxs-lookup"><span data-stu-id="74407-202">False</span></span> | 


### <a name="method-getactionname"></a><span data-ttu-id="74407-203">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="74407-203">Method getActionName</span></span> 
<span data-ttu-id="74407-204">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-204">Returns the action name</span></span>

     public str getActionName () 


#### <a name="return-value"></a><span data-ttu-id="74407-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-205">Return Value</span></span> 
<span data-ttu-id="74407-206">アクション名</span><span class="sxs-lookup"><span data-stu-id="74407-206">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="74407-207">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-207">Method actionTitle</span></span> 
<span data-ttu-id="74407-208">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-208">Gets or sets the action title</span></span>

     public str actionTitle ([str _actionTitle]) 


#### <a name="parameters"></a><span data-ttu-id="74407-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-209">Parameters</span></span>

| <span data-ttu-id="74407-210">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-210">Parameter name</span></span> |  <span data-ttu-id="74407-211">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-211">Parameter type</span></span> | <span data-ttu-id="74407-212">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-212">Optional</span></span> | <span data-ttu-id="74407-213">説明</span><span class="sxs-lookup"><span data-stu-id="74407-213">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-214">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-214">_actionTitle</span></span> | <span data-ttu-id="74407-215">str</span><span class="sxs-lookup"><span data-stu-id="74407-215">str</span></span> | <span data-ttu-id="74407-216">はい</span><span class="sxs-lookup"><span data-stu-id="74407-216">True</span></span> | <span data-ttu-id="74407-217">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-217">The action title</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-218">Return Value</span></span> 
<span data-ttu-id="74407-219">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-219">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="74407-220">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-220">Method actionDescription</span></span> 
<span data-ttu-id="74407-221">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-221">Gets or sets the action description</span></span>

     public str actionDescription ([str _actionDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-222">Parameters</span></span>

| <span data-ttu-id="74407-223">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-223">Parameter name</span></span> |  <span data-ttu-id="74407-224">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-224">Parameter type</span></span> | <span data-ttu-id="74407-225">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-225">Optional</span></span> | <span data-ttu-id="74407-226">説明</span><span class="sxs-lookup"><span data-stu-id="74407-226">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-227">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-227">_actionDescription</span></span> | <span data-ttu-id="74407-228">str</span><span class="sxs-lookup"><span data-stu-id="74407-228">str</span></span> | <span data-ttu-id="74407-229">はい</span><span class="sxs-lookup"><span data-stu-id="74407-229">True</span></span> | <span data-ttu-id="74407-230">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="74407-230">The action description</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-231">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-231">Return Value</span></span> 
<span data-ttu-id="74407-232">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="74407-232">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="74407-233">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="74407-233">Method actionHidden</span></span> 
<span data-ttu-id="74407-234">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-234">Gets or sets whether action is hidden</span></span>

     public boolean actionHidden ([boolean _actionHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-235">Parameters</span></span>

| <span data-ttu-id="74407-236">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-236">Parameter name</span></span> |  <span data-ttu-id="74407-237">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-237">Parameter type</span></span> | <span data-ttu-id="74407-238">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-238">Optional</span></span> | <span data-ttu-id="74407-239">説明</span><span class="sxs-lookup"><span data-stu-id="74407-239">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-240">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="74407-240">_actionHidden</span></span> | <span data-ttu-id="74407-241">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-241">boolean</span></span> | <span data-ttu-id="74407-242">はい</span><span class="sxs-lookup"><span data-stu-id="74407-242">True</span></span> | <span data-ttu-id="74407-243">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="74407-243">Action hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-244">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-244">Return Value</span></span> 
<span data-ttu-id="74407-245">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="74407-245">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="74407-246">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="74407-246">Method actionOrder</span></span> 
<span data-ttu-id="74407-247">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-247">Gets or sets the action order</span></span>

     public int actionOrder ([int _actionOrder]) 


#### <a name="parameters"></a><span data-ttu-id="74407-248">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-248">Parameters</span></span>

| <span data-ttu-id="74407-249">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-249">Parameter name</span></span> |  <span data-ttu-id="74407-250">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-250">Parameter type</span></span> | <span data-ttu-id="74407-251">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-251">Optional</span></span> | <span data-ttu-id="74407-252">説明</span><span class="sxs-lookup"><span data-stu-id="74407-252">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-253">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="74407-253">_actionOrder</span></span> | <span data-ttu-id="74407-254">int</span><span class="sxs-lookup"><span data-stu-id="74407-254">int</span></span> | <span data-ttu-id="74407-255">はい</span><span class="sxs-lookup"><span data-stu-id="74407-255">True</span></span> | <span data-ttu-id="74407-256">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="74407-256">The action order</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-257">Return Value</span></span> 
<span data-ttu-id="74407-258">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="74407-258">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="74407-259">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="74407-259">Method getControl</span></span> 
<span data-ttu-id="74407-260">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-260">Returns the control on the current action having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="74407-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-261">Parameters</span></span>

| <span data-ttu-id="74407-262">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-262">Parameter name</span></span> |  <span data-ttu-id="74407-263">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-263">Parameter type</span></span> | <span data-ttu-id="74407-264">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-264">Optional</span></span> | <span data-ttu-id="74407-265">説明</span><span class="sxs-lookup"><span data-stu-id="74407-265">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-266">_controlName</span><span class="sxs-lookup"><span data-stu-id="74407-266">_controlName</span></span> | <span data-ttu-id="74407-267">str</span><span class="sxs-lookup"><span data-stu-id="74407-267">str</span></span> | <span data-ttu-id="74407-268">False</span><span class="sxs-lookup"><span data-stu-id="74407-268">False</span></span> | <span data-ttu-id="74407-269">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="74407-269">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-270">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-270">Return Value</span></span> 
<span data-ttu-id="74407-271">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="74407-271">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action;otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="74407-272">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-272">Method getControlEnumerator</span></span> 
<span data-ttu-id="74407-273">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-273">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="74407-274">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-274">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-275">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-275">Return Value</span></span> 
<span data-ttu-id="74407-276">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-276">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="74407-277">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="74407-277">Class SysAppAttributeHelper</span></span> 
<span data-ttu-id="74407-278">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="74407-278">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="74407-279">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-279">Methods</span></span>

| <span data-ttu-id="74407-280">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-280">Method name</span></span> | <span data-ttu-id="74407-281">返品</span><span class="sxs-lookup"><span data-stu-id="74407-281">Returns</span></span> | <span data-ttu-id="74407-282">説明</span><span class="sxs-lookup"><span data-stu-id="74407-282">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-283">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="74407-283">getAttributeFromClass</span></span> | <span data-ttu-id="74407-284">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-284">SysAttribute</span></span> | <span data-ttu-id="74407-285">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="74407-285">gets attribute from class</span></span> |


### <a name="method-getattributefromclass"></a><span data-ttu-id="74407-286">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="74407-286">Method getAttributeFromClass</span></span> 
<span data-ttu-id="74407-287">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="74407-287">gets attribute from class</span></span>

     public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType) 


#### <a name="parameters"></a><span data-ttu-id="74407-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-288">Parameters</span></span>

| <span data-ttu-id="74407-289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-289">Parameter name</span></span> |  <span data-ttu-id="74407-290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-290">Parameter type</span></span> | <span data-ttu-id="74407-291">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-291">Optional</span></span> | <span data-ttu-id="74407-292">説明</span><span class="sxs-lookup"><span data-stu-id="74407-292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-293">_sysClass</span><span class="sxs-lookup"><span data-stu-id="74407-293">_sysClass</span></span> | <span data-ttu-id="74407-294">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="74407-294">SysDictClass</span></span> | <span data-ttu-id="74407-295">False</span><span class="sxs-lookup"><span data-stu-id="74407-295">False</span></span> | <span data-ttu-id="74407-296">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="74407-296">class for which attributes is required</span></span>
| <span data-ttu-id="74407-297">_attributeType</span><span class="sxs-lookup"><span data-stu-id="74407-297">_attributeType</span></span> | <span data-ttu-id="74407-298">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="74407-298">SysAppAttributeType</span></span> | <span data-ttu-id="74407-299">False</span><span class="sxs-lookup"><span data-stu-id="74407-299">False</span></span> | <span data-ttu-id="74407-300">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="74407-300">Type of attribute like SysAppEntityAttribute</span></span>


## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="74407-301">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-301">Class SysAppCollectionAttribute</span></span> 
<span data-ttu-id="74407-302">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-302">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="74407-303">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-303">Methods</span></span>

| <span data-ttu-id="74407-304">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-304">Method name</span></span> | <span data-ttu-id="74407-305">返品</span><span class="sxs-lookup"><span data-stu-id="74407-305">Returns</span></span> | <span data-ttu-id="74407-306">説明</span><span class="sxs-lookup"><span data-stu-id="74407-306">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-307">新規</span><span class="sxs-lookup"><span data-stu-id="74407-307">new</span></span> | <span data-ttu-id="74407-308">無効</span><span class="sxs-lookup"><span data-stu-id="74407-308">void</span></span> | <span data-ttu-id="74407-309">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-309">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-310">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-310">Method new</span></span> 
<span data-ttu-id="74407-311">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-311">Constructor</span></span>

     public void new (str _itemContractName, [str _label], [str _relationshipName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-312">Parameters</span></span>

| <span data-ttu-id="74407-313">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-313">Parameter name</span></span> |  <span data-ttu-id="74407-314">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-314">Parameter type</span></span> | <span data-ttu-id="74407-315">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-315">Optional</span></span> | <span data-ttu-id="74407-316">説明</span><span class="sxs-lookup"><span data-stu-id="74407-316">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-317">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="74407-317">_itemContractName</span></span> | <span data-ttu-id="74407-318">str</span><span class="sxs-lookup"><span data-stu-id="74407-318">str</span></span> | <span data-ttu-id="74407-319">False</span><span class="sxs-lookup"><span data-stu-id="74407-319">False</span></span> | <span data-ttu-id="74407-320">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="74407-320">Data contract name of list item</span></span>
| <span data-ttu-id="74407-321">_label</span><span class="sxs-lookup"><span data-stu-id="74407-321">_label</span></span> | <span data-ttu-id="74407-322">str</span><span class="sxs-lookup"><span data-stu-id="74407-322">str</span></span> | <span data-ttu-id="74407-323">はい</span><span class="sxs-lookup"><span data-stu-id="74407-323">True</span></span> | <span data-ttu-id="74407-324">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-324">List control label</span></span>
| <span data-ttu-id="74407-325">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="74407-325">_relationshipName</span></span> | <span data-ttu-id="74407-326">str</span><span class="sxs-lookup"><span data-stu-id="74407-326">str</span></span> | <span data-ttu-id="74407-327">はい</span><span class="sxs-lookup"><span data-stu-id="74407-327">True</span></span> | <span data-ttu-id="74407-328">関係名。</span><span class="sxs-lookup"><span data-stu-id="74407-328">Relationship name.</span></span> <span data-ttu-id="74407-329">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="74407-329">By default the entity name of the list item is used as relationship name</span></span>


## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="74407-330">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-330">Class SysAppControlMetadata</span></span> 
<span data-ttu-id="74407-331">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="74407-331">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="74407-332">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="74407-332">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="74407-333">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-333">Methods</span></span>

| <span data-ttu-id="74407-334">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-334">Method name</span></span> | <span data-ttu-id="74407-335">返品</span><span class="sxs-lookup"><span data-stu-id="74407-335">Returns</span></span> | <span data-ttu-id="74407-336">説明</span><span class="sxs-lookup"><span data-stu-id="74407-336">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-337">新規</span><span class="sxs-lookup"><span data-stu-id="74407-337">new</span></span> | <span data-ttu-id="74407-338">無効</span><span class="sxs-lookup"><span data-stu-id="74407-338">void</span></span> | <span data-ttu-id="74407-339">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-339">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="74407-340">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="74407-340">getBaseLanguageId</span></span> | <span data-ttu-id="74407-341">str</span><span class="sxs-lookup"><span data-stu-id="74407-341">str</span></span> | <span data-ttu-id="74407-342">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="74407-342">Returns the base language id for the app</span></span> |
| <span data-ttu-id="74407-343">getControlName</span><span class="sxs-lookup"><span data-stu-id="74407-343">getControlName</span></span> | <span data-ttu-id="74407-344">str</span><span class="sxs-lookup"><span data-stu-id="74407-344">str</span></span> | <span data-ttu-id="74407-345">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-345">Returns the control name</span></span> |
| <span data-ttu-id="74407-346">controlLabel</span><span class="sxs-lookup"><span data-stu-id="74407-346">controlLabel</span></span> | <span data-ttu-id="74407-347">str</span><span class="sxs-lookup"><span data-stu-id="74407-347">str</span></span> | <span data-ttu-id="74407-348">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-348">Gets and sets the control label</span></span> |
| <span data-ttu-id="74407-349">controlHidden</span><span class="sxs-lookup"><span data-stu-id="74407-349">controlHidden</span></span> | <span data-ttu-id="74407-350">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-350">boolean</span></span> | <span data-ttu-id="74407-351">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-351">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="74407-352">controlOrder</span><span class="sxs-lookup"><span data-stu-id="74407-352">controlOrder</span></span> | <span data-ttu-id="74407-353">int</span><span class="sxs-lookup"><span data-stu-id="74407-353">int</span></span> | <span data-ttu-id="74407-354">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-354">Gets or sets the control order</span></span> |
| <span data-ttu-id="74407-355">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="74407-355">controlMandatory</span></span> | <span data-ttu-id="74407-356">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-356">boolean</span></span> | <span data-ttu-id="74407-357">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-357">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="74407-358">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="74407-358">controlAllowNegative</span></span> | <span data-ttu-id="74407-359">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-359">boolean</span></span> | <span data-ttu-id="74407-360">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="74407-360">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="74407-361">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="74407-361">controlMaxLength</span></span> | <span data-ttu-id="74407-362">int</span><span class="sxs-lookup"><span data-stu-id="74407-362">int</span></span> | <span data-ttu-id="74407-363">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-363">Gets or sets the control max length</span></span> |
| <span data-ttu-id="74407-364">getProperty</span><span class="sxs-lookup"><span data-stu-id="74407-364">getProperty</span></span> | <span data-ttu-id="74407-365">anytype</span><span class="sxs-lookup"><span data-stu-id="74407-365">anytype</span></span> | <span data-ttu-id="74407-366">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-366">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="74407-367">setProperty</span><span class="sxs-lookup"><span data-stu-id="74407-367">setProperty</span></span> | <span data-ttu-id="74407-368">無効</span><span class="sxs-lookup"><span data-stu-id="74407-368">void</span></span> | <span data-ttu-id="74407-369">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="74407-369">Sets the control property referenced by the key</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-370">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-370">Method new</span></span> 
<span data-ttu-id="74407-371">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-371">Creates a new instance of the control metadata</span></span>

     public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId]) 


#### <a name="parameters"></a><span data-ttu-id="74407-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-372">Parameters</span></span>

| <span data-ttu-id="74407-373">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-373">Parameter name</span></span> |  <span data-ttu-id="74407-374">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-374">Parameter type</span></span> | <span data-ttu-id="74407-375">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-375">Optional</span></span> | <span data-ttu-id="74407-376">説明</span><span class="sxs-lookup"><span data-stu-id="74407-376">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-377">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-377">_controlMetadata</span></span> | <span data-ttu-id="74407-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="74407-379">False</span><span class="sxs-lookup"><span data-stu-id="74407-379">False</span></span> | <span data-ttu-id="74407-380">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-380">The controlMetadata object</span></span>
| <span data-ttu-id="74407-381">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="74407-381">_baseLanguageId</span></span> | <span data-ttu-id="74407-382">str</span><span class="sxs-lookup"><span data-stu-id="74407-382">str</span></span> | <span data-ttu-id="74407-383">はい</span><span class="sxs-lookup"><span data-stu-id="74407-383">True</span></span> | <span data-ttu-id="74407-384">基本言語</span><span class="sxs-lookup"><span data-stu-id="74407-384">The base language</span></span>


### <a name="method-getbaselanguageid"></a><span data-ttu-id="74407-385">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="74407-385">Method getBaseLanguageId</span></span> 
<span data-ttu-id="74407-386">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="74407-386">Returns the base language id for the app</span></span>

     public str getBaseLanguageId () 


#### <a name="return-value"></a><span data-ttu-id="74407-387">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-387">Return Value</span></span> 
<span data-ttu-id="74407-388">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="74407-388">The base language id</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="74407-389">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="74407-389">Method getControlName</span></span> 
<span data-ttu-id="74407-390">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-390">Returns the control name</span></span>

     public str getControlName () 


#### <a name="return-value"></a><span data-ttu-id="74407-391">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-391">Return Value</span></span> 
<span data-ttu-id="74407-392">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="74407-392">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="74407-393">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="74407-393">Method controlLabel</span></span> 
<span data-ttu-id="74407-394">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-394">Gets and sets the control label</span></span>

     public str controlLabel ([str _controlLabel]) 


#### <a name="parameters"></a><span data-ttu-id="74407-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-395">Parameters</span></span>

| <span data-ttu-id="74407-396">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-396">Parameter name</span></span> |  <span data-ttu-id="74407-397">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-397">Parameter type</span></span> | <span data-ttu-id="74407-398">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-398">Optional</span></span> | <span data-ttu-id="74407-399">説明</span><span class="sxs-lookup"><span data-stu-id="74407-399">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-400">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="74407-400">_controlLabel</span></span> | <span data-ttu-id="74407-401">str</span><span class="sxs-lookup"><span data-stu-id="74407-401">str</span></span> | <span data-ttu-id="74407-402">はい</span><span class="sxs-lookup"><span data-stu-id="74407-402">True</span></span> | <span data-ttu-id="74407-403">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-403">The control label</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-404">Return Value</span></span> 
<span data-ttu-id="74407-405">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-405">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="74407-406">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="74407-406">Method controlHidden</span></span> 
<span data-ttu-id="74407-407">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-407">Gets and sets whether the control is hidden</span></span>

     public boolean controlHidden ([boolean _controlHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-408">Parameters</span></span>

| <span data-ttu-id="74407-409">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-409">Parameter name</span></span> |  <span data-ttu-id="74407-410">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-410">Parameter type</span></span> | <span data-ttu-id="74407-411">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-411">Optional</span></span> | <span data-ttu-id="74407-412">説明</span><span class="sxs-lookup"><span data-stu-id="74407-412">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-413">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="74407-413">_controlHidden</span></span> | <span data-ttu-id="74407-414">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-414">boolean</span></span> | <span data-ttu-id="74407-415">はい</span><span class="sxs-lookup"><span data-stu-id="74407-415">True</span></span> | <span data-ttu-id="74407-416">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="74407-416">Control hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-417">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-417">Return Value</span></span> 
<span data-ttu-id="74407-418">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="74407-418">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="74407-419">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="74407-419">Method controlOrder</span></span> 
<span data-ttu-id="74407-420">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-420">Gets or sets the control order</span></span>

     public int controlOrder ([int _controlOrder]) 


#### <a name="parameters"></a><span data-ttu-id="74407-421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-421">Parameters</span></span>

| <span data-ttu-id="74407-422">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-422">Parameter name</span></span> |  <span data-ttu-id="74407-423">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-423">Parameter type</span></span> | <span data-ttu-id="74407-424">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-424">Optional</span></span> | <span data-ttu-id="74407-425">説明</span><span class="sxs-lookup"><span data-stu-id="74407-425">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-426">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="74407-426">_controlOrder</span></span> | <span data-ttu-id="74407-427">int</span><span class="sxs-lookup"><span data-stu-id="74407-427">int</span></span> | <span data-ttu-id="74407-428">はい</span><span class="sxs-lookup"><span data-stu-id="74407-428">True</span></span> | <span data-ttu-id="74407-429">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="74407-429">The control order</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-430">Return Value</span></span> 
<span data-ttu-id="74407-431">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="74407-431">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="74407-432">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="74407-432">Method controlMandatory</span></span> 
<span data-ttu-id="74407-433">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-433">Gets or sets the control mandatory</span></span>

     public boolean controlMandatory ([boolean _controlMandatory]) 


#### <a name="parameters"></a><span data-ttu-id="74407-434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-434">Parameters</span></span>

| <span data-ttu-id="74407-435">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-435">Parameter name</span></span> |  <span data-ttu-id="74407-436">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-436">Parameter type</span></span> | <span data-ttu-id="74407-437">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-437">Optional</span></span> | <span data-ttu-id="74407-438">説明</span><span class="sxs-lookup"><span data-stu-id="74407-438">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-439">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="74407-439">_controlMandatory</span></span> | <span data-ttu-id="74407-440">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-440">boolean</span></span> | <span data-ttu-id="74407-441">はい</span><span class="sxs-lookup"><span data-stu-id="74407-441">True</span></span> | <span data-ttu-id="74407-442">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="74407-442">The control mandatory</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-443">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-443">Return Value</span></span> 
<span data-ttu-id="74407-444">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="74407-444">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="74407-445">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="74407-445">Method controlAllowNegative</span></span> 
<span data-ttu-id="74407-446">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="74407-446">Gets or sets the control allow negative</span></span>

     public boolean controlAllowNegative ([boolean _controlAllowNegative]) 


#### <a name="parameters"></a><span data-ttu-id="74407-447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-447">Parameters</span></span>

| <span data-ttu-id="74407-448">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-448">Parameter name</span></span> |  <span data-ttu-id="74407-449">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-449">Parameter type</span></span> | <span data-ttu-id="74407-450">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-450">Optional</span></span> | <span data-ttu-id="74407-451">説明</span><span class="sxs-lookup"><span data-stu-id="74407-451">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-452">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="74407-452">_controlAllowNegative</span></span> | <span data-ttu-id="74407-453">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-453">boolean</span></span> | <span data-ttu-id="74407-454">はい</span><span class="sxs-lookup"><span data-stu-id="74407-454">True</span></span> | <span data-ttu-id="74407-455">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="74407-455">The control allow negative</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-456">Return Value</span></span> 
<span data-ttu-id="74407-457">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="74407-457">The control allow negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="74407-458">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="74407-458">Method controlMaxLength</span></span> 
<span data-ttu-id="74407-459">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-459">Gets or sets the control max length</span></span>

     public int controlMaxLength ([int _controlMaxLength]) 


#### <a name="parameters"></a><span data-ttu-id="74407-460">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-460">Parameters</span></span>

| <span data-ttu-id="74407-461">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-461">Parameter name</span></span> |  <span data-ttu-id="74407-462">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-462">Parameter type</span></span> | <span data-ttu-id="74407-463">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-463">Optional</span></span> | <span data-ttu-id="74407-464">説明</span><span class="sxs-lookup"><span data-stu-id="74407-464">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-465">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="74407-465">_controlMaxLength</span></span> | <span data-ttu-id="74407-466">int</span><span class="sxs-lookup"><span data-stu-id="74407-466">int</span></span> | <span data-ttu-id="74407-467">はい</span><span class="sxs-lookup"><span data-stu-id="74407-467">True</span></span> | <span data-ttu-id="74407-468">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="74407-468">The control max length</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-469">Return Value</span></span> 
<span data-ttu-id="74407-470">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="74407-470">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="74407-471">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="74407-471">Method getProperty</span></span> 
<span data-ttu-id="74407-472">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-472">Gets the control property referenced by the key</span></span>

     public anytype getProperty (str _key) 


#### <a name="parameters"></a><span data-ttu-id="74407-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-473">Parameters</span></span>

| <span data-ttu-id="74407-474">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-474">Parameter name</span></span> |  <span data-ttu-id="74407-475">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-475">Parameter type</span></span> | <span data-ttu-id="74407-476">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-476">Optional</span></span> | <span data-ttu-id="74407-477">説明</span><span class="sxs-lookup"><span data-stu-id="74407-477">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-478">_key</span><span class="sxs-lookup"><span data-stu-id="74407-478">_key</span></span> | <span data-ttu-id="74407-479">str</span><span class="sxs-lookup"><span data-stu-id="74407-479">str</span></span> | <span data-ttu-id="74407-480">False</span><span class="sxs-lookup"><span data-stu-id="74407-480">False</span></span> | <span data-ttu-id="74407-481">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="74407-481">The name of the control property</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-482">Return Value</span></span> 
<span data-ttu-id="74407-483">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="74407-483">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="74407-484">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="74407-484">Method setProperty</span></span> 
<span data-ttu-id="74407-485">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="74407-485">Sets the control property referenced by the key</span></span>

     public void setProperty (str _key, anytype _value) 


#### <a name="parameters"></a><span data-ttu-id="74407-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-486">Parameters</span></span>

| <span data-ttu-id="74407-487">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-487">Parameter name</span></span> |  <span data-ttu-id="74407-488">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-488">Parameter type</span></span> | <span data-ttu-id="74407-489">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-489">Optional</span></span> | <span data-ttu-id="74407-490">説明</span><span class="sxs-lookup"><span data-stu-id="74407-490">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-491">_key</span><span class="sxs-lookup"><span data-stu-id="74407-491">_key</span></span> | <span data-ttu-id="74407-492">str</span><span class="sxs-lookup"><span data-stu-id="74407-492">str</span></span> | <span data-ttu-id="74407-493">False</span><span class="sxs-lookup"><span data-stu-id="74407-493">False</span></span> | <span data-ttu-id="74407-494">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="74407-494">The name of the control property</span></span>
| <span data-ttu-id="74407-495">_value</span><span class="sxs-lookup"><span data-stu-id="74407-495">_value</span></span> | <span data-ttu-id="74407-496">anytype</span><span class="sxs-lookup"><span data-stu-id="74407-496">anytype</span></span> | <span data-ttu-id="74407-497">False</span><span class="sxs-lookup"><span data-stu-id="74407-497">False</span></span> | <span data-ttu-id="74407-498">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="74407-498">The value of the control property</span></span>


## <a name="class-sysappentityattribute"></a><span data-ttu-id="74407-499">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-499">Class SysAppEntityAttribute</span></span> 
<span data-ttu-id="74407-500">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-500">SysAppEntityAttribute used for decorating data contract entitities</span></span>

### <a name="methods"></a><span data-ttu-id="74407-501">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-501">Methods</span></span>

| <span data-ttu-id="74407-502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-502">Method name</span></span> | <span data-ttu-id="74407-503">返品</span><span class="sxs-lookup"><span data-stu-id="74407-503">Returns</span></span> | <span data-ttu-id="74407-504">説明</span><span class="sxs-lookup"><span data-stu-id="74407-504">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-505">新規</span><span class="sxs-lookup"><span data-stu-id="74407-505">new</span></span> | <span data-ttu-id="74407-506">無効</span><span class="sxs-lookup"><span data-stu-id="74407-506">void</span></span> | <span data-ttu-id="74407-507">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-507">Constructor</span></span> |
| <span data-ttu-id="74407-508">名前</span><span class="sxs-lookup"><span data-stu-id="74407-508">name</span></span> | <span data-ttu-id="74407-509">str</span><span class="sxs-lookup"><span data-stu-id="74407-509">str</span></span> | <span data-ttu-id="74407-510">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-510">Gets the name of the entity</span></span> |
| <span data-ttu-id="74407-511">entityKey</span><span class="sxs-lookup"><span data-stu-id="74407-511">entityKey</span></span> | <span data-ttu-id="74407-512">str</span><span class="sxs-lookup"><span data-stu-id="74407-512">str</span></span> | <span data-ttu-id="74407-513">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="74407-513">Gets the entity key</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-514">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-514">Method new</span></span> 
<span data-ttu-id="74407-515">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-515">Constructor</span></span>

     public void new (str _name, str _entityKey) 


#### <a name="parameters"></a><span data-ttu-id="74407-516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-516">Parameters</span></span>

| <span data-ttu-id="74407-517">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-517">Parameter name</span></span> |  <span data-ttu-id="74407-518">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-518">Parameter type</span></span> | <span data-ttu-id="74407-519">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-519">Optional</span></span> | <span data-ttu-id="74407-520">説明</span><span class="sxs-lookup"><span data-stu-id="74407-520">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-521">_name</span><span class="sxs-lookup"><span data-stu-id="74407-521">_name</span></span> | <span data-ttu-id="74407-522">str</span><span class="sxs-lookup"><span data-stu-id="74407-522">str</span></span> | <span data-ttu-id="74407-523">False</span><span class="sxs-lookup"><span data-stu-id="74407-523">False</span></span> | <span data-ttu-id="74407-524">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-524">Entity name</span></span>
| <span data-ttu-id="74407-525">_entityKey</span><span class="sxs-lookup"><span data-stu-id="74407-525">_entityKey</span></span> | <span data-ttu-id="74407-526">str</span><span class="sxs-lookup"><span data-stu-id="74407-526">str</span></span> | <span data-ttu-id="74407-527">False</span><span class="sxs-lookup"><span data-stu-id="74407-527">False</span></span> | <span data-ttu-id="74407-528">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="74407-528">Name of the entity's key</span></span>


### <a name="method-name"></a><span data-ttu-id="74407-529">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-529">Method name</span></span> 
<span data-ttu-id="74407-530">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-530">Gets the name of the entity</span></span>

     public str name () 


#### <a name="return-value"></a><span data-ttu-id="74407-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-531">Return Value</span></span> 
<span data-ttu-id="74407-532">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="74407-532">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="74407-533">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="74407-533">Method entityKey</span></span> 
<span data-ttu-id="74407-534">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="74407-534">Gets the entity key</span></span>

     public str entityKey () 


#### <a name="return-value"></a><span data-ttu-id="74407-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-535">Return Value</span></span> 
<span data-ttu-id="74407-536">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="74407-536">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="74407-537">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-537">Class SysAppEntityContext</span></span> 
<span data-ttu-id="74407-538">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-538">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="74407-539">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-539">Methods</span></span>

| <span data-ttu-id="74407-540">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-540">Method name</span></span> | <span data-ttu-id="74407-541">返品</span><span class="sxs-lookup"><span data-stu-id="74407-541">Returns</span></span> | <span data-ttu-id="74407-542">説明</span><span class="sxs-lookup"><span data-stu-id="74407-542">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-543">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="74407-543">constructFromParams</span></span> | <span data-ttu-id="74407-544">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-544">SysAppEntityContext</span></span> | <span data-ttu-id="74407-545">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="74407-545">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="74407-546">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="74407-546">constructFromBuffer</span></span> | <span data-ttu-id="74407-547">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-547">SysAppEntityContext</span></span> | <span data-ttu-id="74407-548">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="74407-548">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="74407-549">entityName</span><span class="sxs-lookup"><span data-stu-id="74407-549">entityName</span></span> | <span data-ttu-id="74407-550">str</span><span class="sxs-lookup"><span data-stu-id="74407-550">str</span></span> | <span data-ttu-id="74407-551">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-551">Entity name on which filter applies</span></span> |
| <span data-ttu-id="74407-552">entityId</span><span class="sxs-lookup"><span data-stu-id="74407-552">entityId</span></span> | <span data-ttu-id="74407-553">str</span><span class="sxs-lookup"><span data-stu-id="74407-553">str</span></span> | <span data-ttu-id="74407-554">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-554">Field value on which filter applies</span></span> |


### <a name="method-constructfromparams"></a><span data-ttu-id="74407-555">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="74407-555">Method constructFromParams</span></span> 
<span data-ttu-id="74407-556">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="74407-556">Constructs SysAppEntityContext from entityName and entityId</span></span>

     public SysAppEntityContext constructFromParams (str _entityName, str _entityId) 


#### <a name="parameters"></a><span data-ttu-id="74407-557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-557">Parameters</span></span>

| <span data-ttu-id="74407-558">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-558">Parameter name</span></span> |  <span data-ttu-id="74407-559">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-559">Parameter type</span></span> | <span data-ttu-id="74407-560">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-560">Optional</span></span> | <span data-ttu-id="74407-561">説明</span><span class="sxs-lookup"><span data-stu-id="74407-561">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-562">_entityName</span><span class="sxs-lookup"><span data-stu-id="74407-562">_entityName</span></span> | <span data-ttu-id="74407-563">str</span><span class="sxs-lookup"><span data-stu-id="74407-563">str</span></span> | <span data-ttu-id="74407-564">False</span><span class="sxs-lookup"><span data-stu-id="74407-564">False</span></span> | <span data-ttu-id="74407-565">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-565">Entity name</span></span>
| <span data-ttu-id="74407-566">_entityId</span><span class="sxs-lookup"><span data-stu-id="74407-566">_entityId</span></span> | <span data-ttu-id="74407-567">str</span><span class="sxs-lookup"><span data-stu-id="74407-567">str</span></span> | <span data-ttu-id="74407-568">False</span><span class="sxs-lookup"><span data-stu-id="74407-568">False</span></span> | <span data-ttu-id="74407-569">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="74407-569">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-570">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-570">Return Value</span></span> 
<span data-ttu-id="74407-571">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="74407-571">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="74407-572">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="74407-572">Method constructFromBuffer</span></span> 
<span data-ttu-id="74407-573">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="74407-573">Constructs SysAppEntityContext from table buffer</span></span>

     public SysAppEntityContext constructFromBuffer (Common _tableBuffer) 


#### <a name="parameters"></a><span data-ttu-id="74407-574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-574">Parameters</span></span>

| <span data-ttu-id="74407-575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-575">Parameter name</span></span> |  <span data-ttu-id="74407-576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-576">Parameter type</span></span> | <span data-ttu-id="74407-577">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-577">Optional</span></span> | <span data-ttu-id="74407-578">説明</span><span class="sxs-lookup"><span data-stu-id="74407-578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-579">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="74407-579">_tableBuffer</span></span> | <span data-ttu-id="74407-580">共通</span><span class="sxs-lookup"><span data-stu-id="74407-580">Common</span></span> | <span data-ttu-id="74407-581">False</span><span class="sxs-lookup"><span data-stu-id="74407-581">False</span></span> | <span data-ttu-id="74407-582">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="74407-582">table buffer forming the entity</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-583">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-583">Return Value</span></span> 
<span data-ttu-id="74407-584">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="74407-584">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="74407-585">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="74407-585">Method entityName</span></span> 
<span data-ttu-id="74407-586">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-586">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-587">Parameters</span></span>

| <span data-ttu-id="74407-588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-588">Parameter name</span></span> |  <span data-ttu-id="74407-589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-589">Parameter type</span></span> | <span data-ttu-id="74407-590">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-590">Optional</span></span> | <span data-ttu-id="74407-591">説明</span><span class="sxs-lookup"><span data-stu-id="74407-591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-592">_entityName</span><span class="sxs-lookup"><span data-stu-id="74407-592">_entityName</span></span> | <span data-ttu-id="74407-593">str</span><span class="sxs-lookup"><span data-stu-id="74407-593">str</span></span> | <span data-ttu-id="74407-594">はい</span><span class="sxs-lookup"><span data-stu-id="74407-594">True</span></span> | <span data-ttu-id="74407-595">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-595">Entity name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-596">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-596">Return Value</span></span> 
<span data-ttu-id="74407-597">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-597">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="74407-598">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="74407-598">Method entityId</span></span> 
<span data-ttu-id="74407-599">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-599">Field value on which filter applies</span></span>

     public str entityId ([str _entityId]) 


#### <a name="parameters"></a><span data-ttu-id="74407-600">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-600">Parameters</span></span>

| <span data-ttu-id="74407-601">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-601">Parameter name</span></span> |  <span data-ttu-id="74407-602">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-602">Parameter type</span></span> | <span data-ttu-id="74407-603">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-603">Optional</span></span> | <span data-ttu-id="74407-604">説明</span><span class="sxs-lookup"><span data-stu-id="74407-604">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-605">_entityId</span><span class="sxs-lookup"><span data-stu-id="74407-605">_entityId</span></span> | <span data-ttu-id="74407-606">str</span><span class="sxs-lookup"><span data-stu-id="74407-606">str</span></span> | <span data-ttu-id="74407-607">はい</span><span class="sxs-lookup"><span data-stu-id="74407-607">True</span></span> | <span data-ttu-id="74407-608">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="74407-608">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-609">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-609">Return Value</span></span> 
<span data-ttu-id="74407-610">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="74407-610">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="74407-611">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-611">Class SysAppFieldAttribute</span></span> 
<span data-ttu-id="74407-612">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-612">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="74407-613">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-613">Methods</span></span>

| <span data-ttu-id="74407-614">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-614">Method name</span></span> | <span data-ttu-id="74407-615">返品</span><span class="sxs-lookup"><span data-stu-id="74407-615">Returns</span></span> | <span data-ttu-id="74407-616">説明</span><span class="sxs-lookup"><span data-stu-id="74407-616">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-617">新規</span><span class="sxs-lookup"><span data-stu-id="74407-617">new</span></span> | <span data-ttu-id="74407-618">無効</span><span class="sxs-lookup"><span data-stu-id="74407-618">void</span></span> | <span data-ttu-id="74407-619">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-619">Creates a new instance of SysAppFieldAttribute class</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-620">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-620">Method new</span></span> 
<span data-ttu-id="74407-621">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-621">Creates a new instance of SysAppFieldAttribute class</span></span>

     public void new (str _fieldName, str _label) 


#### <a name="parameters"></a><span data-ttu-id="74407-622">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-622">Parameters</span></span>

| <span data-ttu-id="74407-623">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-623">Parameter name</span></span> |  <span data-ttu-id="74407-624">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-624">Parameter type</span></span> | <span data-ttu-id="74407-625">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-625">Optional</span></span> | <span data-ttu-id="74407-626">説明</span><span class="sxs-lookup"><span data-stu-id="74407-626">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-627">_fieldName</span><span class="sxs-lookup"><span data-stu-id="74407-627">_fieldName</span></span> | <span data-ttu-id="74407-628">str</span><span class="sxs-lookup"><span data-stu-id="74407-628">str</span></span> | <span data-ttu-id="74407-629">False</span><span class="sxs-lookup"><span data-stu-id="74407-629">False</span></span> | <span data-ttu-id="74407-630">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-630">Entity field name with which control is bound</span></span>
| <span data-ttu-id="74407-631">_label</span><span class="sxs-lookup"><span data-stu-id="74407-631">_label</span></span> | <span data-ttu-id="74407-632">str</span><span class="sxs-lookup"><span data-stu-id="74407-632">str</span></span> | <span data-ttu-id="74407-633">False</span><span class="sxs-lookup"><span data-stu-id="74407-633">False</span></span> | <span data-ttu-id="74407-634">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-634">Control label</span></span>


## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="74407-635">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="74407-635">Class SysAppFieldMultiSelectHelper</span></span> 
<span data-ttu-id="74407-636">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="74407-636">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="74407-637">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-637">Methods</span></span>

| <span data-ttu-id="74407-638">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-638">Method name</span></span> | <span data-ttu-id="74407-639">返品</span><span class="sxs-lookup"><span data-stu-id="74407-639">Returns</span></span> | <span data-ttu-id="74407-640">説明</span><span class="sxs-lookup"><span data-stu-id="74407-640">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-641">新規</span><span class="sxs-lookup"><span data-stu-id="74407-641">new</span></span> | <span data-ttu-id="74407-642">無効</span><span class="sxs-lookup"><span data-stu-id="74407-642">void</span></span> | <span data-ttu-id="74407-643">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-643">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="74407-644">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="74407-644">getSelectedRecIds</span></span> | <span data-ttu-id="74407-645">コンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-645">container</span></span> | <span data-ttu-id="74407-646">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-646">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="74407-647">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="74407-647">getSelectedValues</span></span> | <span data-ttu-id="74407-648">コンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-648">container</span></span> | <span data-ttu-id="74407-649">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-649">Returns a container of selected values</span></span> |
| <span data-ttu-id="74407-650">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="74407-650">getSelectedRecords</span></span> | <span data-ttu-id="74407-651">共通</span><span class="sxs-lookup"><span data-stu-id="74407-651">Common</span></span> | <span data-ttu-id="74407-652">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="74407-652">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="74407-653">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="74407-653">The buffer is marked as temp..</span></span>  <span data-ttu-id="74407-654">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-654">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="74407-655">setControlValue</span><span class="sxs-lookup"><span data-stu-id="74407-655">setControlValue</span></span> | <span data-ttu-id="74407-656">無効</span><span class="sxs-lookup"><span data-stu-id="74407-656">void</span></span> | <span data-ttu-id="74407-657">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="74407-657">A setter to set the multi select control value</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-658">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-658">Method new</span></span> 
<span data-ttu-id="74407-659">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-659">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

     public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl) 


#### <a name="parameters"></a><span data-ttu-id="74407-660">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-660">Parameters</span></span>

| <span data-ttu-id="74407-661">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-661">Parameter name</span></span> |  <span data-ttu-id="74407-662">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-662">Parameter type</span></span> | <span data-ttu-id="74407-663">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-663">Optional</span></span> | <span data-ttu-id="74407-664">説明</span><span class="sxs-lookup"><span data-stu-id="74407-664">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-665">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="74407-665">_multiSelectTableId</span></span> | <span data-ttu-id="74407-666">TableId</span><span class="sxs-lookup"><span data-stu-id="74407-666">TableId</span></span> | <span data-ttu-id="74407-667">False</span><span class="sxs-lookup"><span data-stu-id="74407-667">False</span></span> | <span data-ttu-id="74407-668">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="74407-668">The backing tableId for the field</span></span>
| <span data-ttu-id="74407-669">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="74407-669">_valueFieldId</span></span> | <span data-ttu-id="74407-670">FieldId</span><span class="sxs-lookup"><span data-stu-id="74407-670">FieldId</span></span> | <span data-ttu-id="74407-671">False</span><span class="sxs-lookup"><span data-stu-id="74407-671">False</span></span> | <span data-ttu-id="74407-672">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="74407-672">The fieldId for the field which will be shown in the multi select control</span></span>
| <span data-ttu-id="74407-673">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="74407-673">_multiSelectControl</span></span> | <span data-ttu-id="74407-674">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="74407-674">FormStringControl</span></span> | <span data-ttu-id="74407-675">False</span><span class="sxs-lookup"><span data-stu-id="74407-675">False</span></span> | <span data-ttu-id="74407-676">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="74407-676">The string control that will be the multi select control</span></span>


### <a name="method-getselectedrecids"></a><span data-ttu-id="74407-677">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="74407-677">Method getSelectedRecIds</span></span> 
<span data-ttu-id="74407-678">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-678">Returns a container of recIds of the records that were selected</span></span>

     public container getSelectedRecIds () 


#### <a name="return-value"></a><span data-ttu-id="74407-679">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-679">Return Value</span></span> 
<span data-ttu-id="74407-680">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-680">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="74407-681">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="74407-681">Method getSelectedValues</span></span> 
<span data-ttu-id="74407-682">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-682">Returns a container of selected values</span></span>

     public container getSelectedValues () 


#### <a name="return-value"></a><span data-ttu-id="74407-683">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-683">Return Value</span></span> 
<span data-ttu-id="74407-684">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-684">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="74407-685">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="74407-685">Method getSelectedRecords</span></span> 
<span data-ttu-id="74407-686">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="74407-686">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="74407-687">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="74407-687">The buffer is marked as temp..</span></span>  <span data-ttu-id="74407-688">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-688">Later a while-Select can be used to iterate through all the records</span></span>

     public Common getSelectedRecords () 


#### <a name="return-value"></a><span data-ttu-id="74407-689">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-689">Return Value</span></span> 
<span data-ttu-id="74407-690">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="74407-690">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="74407-691">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="74407-691">Method setControlValue</span></span> 
<span data-ttu-id="74407-692">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="74407-692">A setter to set the multi select control value</span></span>

     public void setControlValue (str _value) 


#### <a name="parameters"></a><span data-ttu-id="74407-693">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-693">Parameters</span></span>

| <span data-ttu-id="74407-694">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-694">Parameter name</span></span> |  <span data-ttu-id="74407-695">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-695">Parameter type</span></span> | <span data-ttu-id="74407-696">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-696">Optional</span></span> | <span data-ttu-id="74407-697">説明</span><span class="sxs-lookup"><span data-stu-id="74407-697">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-698">_value</span><span class="sxs-lookup"><span data-stu-id="74407-698">_value</span></span> | <span data-ttu-id="74407-699">str</span><span class="sxs-lookup"><span data-stu-id="74407-699">str</span></span> | <span data-ttu-id="74407-700">False</span><span class="sxs-lookup"><span data-stu-id="74407-700">False</span></span> | <span data-ttu-id="74407-701">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="74407-701">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>


## <a name="class-sysappfiltercontext"></a><span data-ttu-id="74407-702">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="74407-702">Class SysAppFilterContext</span></span> 
<span data-ttu-id="74407-703">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="74407-703">SysAppFilterContext class which holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="74407-704">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-704">Methods</span></span>

| <span data-ttu-id="74407-705">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-705">Method name</span></span> | <span data-ttu-id="74407-706">返品</span><span class="sxs-lookup"><span data-stu-id="74407-706">Returns</span></span> | <span data-ttu-id="74407-707">説明</span><span class="sxs-lookup"><span data-stu-id="74407-707">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-708">entityName</span><span class="sxs-lookup"><span data-stu-id="74407-708">entityName</span></span> | <span data-ttu-id="74407-709">str</span><span class="sxs-lookup"><span data-stu-id="74407-709">str</span></span> | <span data-ttu-id="74407-710">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-710">Entity name on which filter applies</span></span> |
| <span data-ttu-id="74407-711">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-711">filterFieldName</span></span> | <span data-ttu-id="74407-712">str</span><span class="sxs-lookup"><span data-stu-id="74407-712">str</span></span> | <span data-ttu-id="74407-713">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-713">Field name on which filter applies</span></span> |
| <span data-ttu-id="74407-714">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="74407-714">filterFieldValueList</span></span> | <span data-ttu-id="74407-715">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-715">List</span></span> | <span data-ttu-id="74407-716">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-716">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="74407-717">演算子</span><span class="sxs-lookup"><span data-stu-id="74407-717">operator</span></span> | <span data-ttu-id="74407-718">str</span><span class="sxs-lookup"><span data-stu-id="74407-718">str</span></span> | <span data-ttu-id="74407-719">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-719">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="74407-720">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="74407-720">addFilterFieldValue</span></span> | <span data-ttu-id="74407-721">無効</span><span class="sxs-lookup"><span data-stu-id="74407-721">void</span></span> | <span data-ttu-id="74407-722">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="74407-722">Adds filter field value</span></span> |


### <a name="method-entityname"></a><span data-ttu-id="74407-723">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="74407-723">Method entityName</span></span> 
<span data-ttu-id="74407-724">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-724">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-725">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-725">Parameters</span></span>

| <span data-ttu-id="74407-726">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-726">Parameter name</span></span> |  <span data-ttu-id="74407-727">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-727">Parameter type</span></span> | <span data-ttu-id="74407-728">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-728">Optional</span></span> | <span data-ttu-id="74407-729">説明</span><span class="sxs-lookup"><span data-stu-id="74407-729">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-730">_entityName</span><span class="sxs-lookup"><span data-stu-id="74407-730">_entityName</span></span> | <span data-ttu-id="74407-731">str</span><span class="sxs-lookup"><span data-stu-id="74407-731">str</span></span> | <span data-ttu-id="74407-732">はい</span><span class="sxs-lookup"><span data-stu-id="74407-732">True</span></span> | <span data-ttu-id="74407-733">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-733">Entity name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-734">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-734">Return Value</span></span> 
<span data-ttu-id="74407-735">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-735">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="74407-736">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-736">Method filterFieldName</span></span> 
<span data-ttu-id="74407-737">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-737">Field name on which filter applies</span></span>

     public str filterFieldName ([str _filterFieldName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-738">Parameters</span></span>

| <span data-ttu-id="74407-739">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-739">Parameter name</span></span> |  <span data-ttu-id="74407-740">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-740">Parameter type</span></span> | <span data-ttu-id="74407-741">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-741">Optional</span></span> | <span data-ttu-id="74407-742">説明</span><span class="sxs-lookup"><span data-stu-id="74407-742">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-743">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-743">_filterFieldName</span></span> | <span data-ttu-id="74407-744">str</span><span class="sxs-lookup"><span data-stu-id="74407-744">str</span></span> | <span data-ttu-id="74407-745">はい</span><span class="sxs-lookup"><span data-stu-id="74407-745">True</span></span> | <span data-ttu-id="74407-746">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-746">Field name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-747">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-747">Return Value</span></span> 
<span data-ttu-id="74407-748">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-748">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="74407-749">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="74407-749">Method filterFieldValueList</span></span> 
<span data-ttu-id="74407-750">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-750">Gets the list of filter field values based on which filter happens</span></span>

     public List filterFieldValueList () 


#### <a name="return-value"></a><span data-ttu-id="74407-751">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-751">Return Value</span></span> 
<span data-ttu-id="74407-752">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-752">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="74407-753">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="74407-753">Method operator</span></span> 
<span data-ttu-id="74407-754">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-754">Operator based on which result will be fetched</span></span>

     public str operator ([str _operator]) 


#### <a name="parameters"></a><span data-ttu-id="74407-755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-755">Parameters</span></span>

| <span data-ttu-id="74407-756">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-756">Parameter name</span></span> |  <span data-ttu-id="74407-757">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-757">Parameter type</span></span> | <span data-ttu-id="74407-758">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-758">Optional</span></span> | <span data-ttu-id="74407-759">説明</span><span class="sxs-lookup"><span data-stu-id="74407-759">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-760">_operator</span><span class="sxs-lookup"><span data-stu-id="74407-760">_operator</span></span> | <span data-ttu-id="74407-761">str</span><span class="sxs-lookup"><span data-stu-id="74407-761">str</span></span> | <span data-ttu-id="74407-762">はい</span><span class="sxs-lookup"><span data-stu-id="74407-762">True</span></span> | <span data-ttu-id="74407-763">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-763">Operator based on which result will be fetched</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-764">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-764">Return Value</span></span> 
<span data-ttu-id="74407-765">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-765">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="74407-766">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="74407-766">Method addFilterFieldValue</span></span> 
<span data-ttu-id="74407-767">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="74407-767">Adds filter field value</span></span>

     public void addFilterFieldValue ( _filterFieldValueList) 


#### <a name="parameters"></a><span data-ttu-id="74407-768">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-768">Parameters</span></span>

| <span data-ttu-id="74407-769">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-769">Parameter name</span></span> |  <span data-ttu-id="74407-770">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-770">Parameter type</span></span> | <span data-ttu-id="74407-771">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-771">Optional</span></span> | <span data-ttu-id="74407-772">説明</span><span class="sxs-lookup"><span data-stu-id="74407-772">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-773">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="74407-773">_filterFieldValueList</span></span> |  | <span data-ttu-id="74407-774">False</span><span class="sxs-lookup"><span data-stu-id="74407-774">False</span></span> | <span data-ttu-id="74407-775">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-775">Filter field values based on which filter happens</span></span>


## <a name="class-sysapplookupattribute"></a><span data-ttu-id="74407-776">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-776">Class SysAppLookUpAttribute</span></span> 
<span data-ttu-id="74407-777">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-777">SysAppPageAttribute used for decorating pages that is also lookup page</span></span>

### <a name="methods"></a><span data-ttu-id="74407-778">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-778">Methods</span></span>

| <span data-ttu-id="74407-779">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-779">Method name</span></span> | <span data-ttu-id="74407-780">返品</span><span class="sxs-lookup"><span data-stu-id="74407-780">Returns</span></span> | <span data-ttu-id="74407-781">説明</span><span class="sxs-lookup"><span data-stu-id="74407-781">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-782">新規</span><span class="sxs-lookup"><span data-stu-id="74407-782">new</span></span> | <span data-ttu-id="74407-783">無効</span><span class="sxs-lookup"><span data-stu-id="74407-783">void</span></span> | <span data-ttu-id="74407-784">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-784">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="74407-785">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-785">displayFieldName</span></span> | <span data-ttu-id="74407-786">str</span><span class="sxs-lookup"><span data-stu-id="74407-786">str</span></span> | <span data-ttu-id="74407-787">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-787">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="74407-788">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-788">valueFieldName</span></span> | <span data-ttu-id="74407-789">str</span><span class="sxs-lookup"><span data-stu-id="74407-789">str</span></span> | <span data-ttu-id="74407-790">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-790">Gets the value field name of lookup control</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-791">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-791">Method new</span></span> 
<span data-ttu-id="74407-792">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-792">Creates a new instance of SysAppLookUpAttribute class</span></span>

     public void new (str _displayFieldName, str _valueFieldName) 


#### <a name="parameters"></a><span data-ttu-id="74407-793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-793">Parameters</span></span>

| <span data-ttu-id="74407-794">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-794">Parameter name</span></span> |  <span data-ttu-id="74407-795">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-795">Parameter type</span></span> | <span data-ttu-id="74407-796">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-796">Optional</span></span> | <span data-ttu-id="74407-797">説明</span><span class="sxs-lookup"><span data-stu-id="74407-797">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-798">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-798">_displayFieldName</span></span> | <span data-ttu-id="74407-799">str</span><span class="sxs-lookup"><span data-stu-id="74407-799">str</span></span> | <span data-ttu-id="74407-800">False</span><span class="sxs-lookup"><span data-stu-id="74407-800">False</span></span> | <span data-ttu-id="74407-801">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="74407-801">Lookup display field.</span></span> <span data-ttu-id="74407-802">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="74407-802">Name of any control of lookup page</span></span>
| <span data-ttu-id="74407-803">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-803">_valueFieldName</span></span> | <span data-ttu-id="74407-804">str</span><span class="sxs-lookup"><span data-stu-id="74407-804">str</span></span> | <span data-ttu-id="74407-805">False</span><span class="sxs-lookup"><span data-stu-id="74407-805">False</span></span> | <span data-ttu-id="74407-806">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="74407-806">Lookup value field.</span></span> <span data-ttu-id="74407-807">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="74407-807">Name of control formed by root data contract constructing lookup page</span></span>


### <a name="method-displayfieldname"></a><span data-ttu-id="74407-808">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-808">Method displayFieldName</span></span> 
<span data-ttu-id="74407-809">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-809">Gets the display field name of lookup control</span></span>

     public str displayFieldName () 


#### <a name="return-value"></a><span data-ttu-id="74407-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-810">Return Value</span></span> 
<span data-ttu-id="74407-811">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-811">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="74407-812">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-812">Method valueFieldName</span></span> 
<span data-ttu-id="74407-813">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-813">Gets the value field name of lookup control</span></span>

     public str valueFieldName () 


#### <a name="return-value"></a><span data-ttu-id="74407-814">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-814">Return Value</span></span> 
<span data-ttu-id="74407-815">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="74407-815">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="74407-816">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-816">Class SysAppLookupFieldAttribute</span></span> 
<span data-ttu-id="74407-817">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-817">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="74407-818">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-818">Methods</span></span>

| <span data-ttu-id="74407-819">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-819">Method name</span></span> | <span data-ttu-id="74407-820">返品</span><span class="sxs-lookup"><span data-stu-id="74407-820">Returns</span></span> | <span data-ttu-id="74407-821">説明</span><span class="sxs-lookup"><span data-stu-id="74407-821">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-822">新規</span><span class="sxs-lookup"><span data-stu-id="74407-822">new</span></span> | <span data-ttu-id="74407-823">無効</span><span class="sxs-lookup"><span data-stu-id="74407-823">void</span></span> | <span data-ttu-id="74407-824">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-824">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="74407-825">entityName</span><span class="sxs-lookup"><span data-stu-id="74407-825">entityName</span></span> | <span data-ttu-id="74407-826">str</span><span class="sxs-lookup"><span data-stu-id="74407-826">str</span></span> | <span data-ttu-id="74407-827">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-827">Gets the name of the entity with which lookup page is related</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-828">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-828">Method new</span></span> 
<span data-ttu-id="74407-829">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-829">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

     public void new ( _name) 


#### <a name="parameters"></a><span data-ttu-id="74407-830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-830">Parameters</span></span>

| <span data-ttu-id="74407-831">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-831">Parameter name</span></span> |  <span data-ttu-id="74407-832">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-832">Parameter type</span></span> | <span data-ttu-id="74407-833">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-833">Optional</span></span> | <span data-ttu-id="74407-834">説明</span><span class="sxs-lookup"><span data-stu-id="74407-834">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-835">_name</span><span class="sxs-lookup"><span data-stu-id="74407-835">_name</span></span> |  | <span data-ttu-id="74407-836">False</span><span class="sxs-lookup"><span data-stu-id="74407-836">False</span></span> | <span data-ttu-id="74407-837">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="74407-837">Name of the entity with which lookup page is related</span></span>


### <a name="method-entityname"></a><span data-ttu-id="74407-838">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="74407-838">Method entityName</span></span> 
<span data-ttu-id="74407-839">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-839">Gets the name of the entity with which lookup page is related</span></span>

     public str entityName () 


#### <a name="return-value"></a><span data-ttu-id="74407-840">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-840">Return Value</span></span> 
<span data-ttu-id="74407-841">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="74407-841">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="74407-842">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-842">Class SysAppPageAttribute</span></span> 
<span data-ttu-id="74407-843">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-843">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-844">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-844">Methods</span></span>

| <span data-ttu-id="74407-845">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-845">Method name</span></span> | <span data-ttu-id="74407-846">返品</span><span class="sxs-lookup"><span data-stu-id="74407-846">Returns</span></span> | <span data-ttu-id="74407-847">説明</span><span class="sxs-lookup"><span data-stu-id="74407-847">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-848">新規</span><span class="sxs-lookup"><span data-stu-id="74407-848">new</span></span> | <span data-ttu-id="74407-849">無効</span><span class="sxs-lookup"><span data-stu-id="74407-849">void</span></span> | <span data-ttu-id="74407-850">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-850">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="74407-851">pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-851">pageTitle</span></span> | <span data-ttu-id="74407-852">str</span><span class="sxs-lookup"><span data-stu-id="74407-852">str</span></span> | <span data-ttu-id="74407-853">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-853">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="74407-854">pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-854">pageDescription</span></span> | <span data-ttu-id="74407-855">str</span><span class="sxs-lookup"><span data-stu-id="74407-855">str</span></span> | <span data-ttu-id="74407-856">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-856">Gets the Page Description</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-857">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-857">Method new</span></span> 
<span data-ttu-id="74407-858">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-858">Creates a new instance of SysAppPageAttribute class</span></span>

     public void new ([str _pageTitle], [str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-859">Parameters</span></span>

| <span data-ttu-id="74407-860">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-860">Parameter name</span></span> |  <span data-ttu-id="74407-861">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-861">Parameter type</span></span> | <span data-ttu-id="74407-862">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-862">Optional</span></span> | <span data-ttu-id="74407-863">説明</span><span class="sxs-lookup"><span data-stu-id="74407-863">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-864">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-864">_pageTitle</span></span> | <span data-ttu-id="74407-865">str</span><span class="sxs-lookup"><span data-stu-id="74407-865">str</span></span> | <span data-ttu-id="74407-866">はい</span><span class="sxs-lookup"><span data-stu-id="74407-866">True</span></span> | <span data-ttu-id="74407-867">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-867">The page title</span></span>
| <span data-ttu-id="74407-868">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-868">_pageDescription</span></span> | <span data-ttu-id="74407-869">str</span><span class="sxs-lookup"><span data-stu-id="74407-869">str</span></span> | <span data-ttu-id="74407-870">はい</span><span class="sxs-lookup"><span data-stu-id="74407-870">True</span></span> | <span data-ttu-id="74407-871">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-871">The page description</span></span>


### <a name="method-pagetitle"></a><span data-ttu-id="74407-872">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-872">Method pageTitle</span></span> 
<span data-ttu-id="74407-873">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-873">Gets the Page Title of the page</span></span>

     public str pageTitle () 


#### <a name="return-value"></a><span data-ttu-id="74407-874">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-874">Return Value</span></span> 
<span data-ttu-id="74407-875">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-875">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="74407-876">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-876">Method pageDescription</span></span> 
<span data-ttu-id="74407-877">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-877">Gets the Page Description</span></span>

     public str pageDescription () 


#### <a name="return-value"></a><span data-ttu-id="74407-878">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-878">Return Value</span></span> 
<span data-ttu-id="74407-879">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-879">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="74407-880">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-880">Class SysAppPageMetadata</span></span> 
<span data-ttu-id="74407-881">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="74407-881">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="74407-882">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-882">Methods</span></span>

| <span data-ttu-id="74407-883">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-883">Method name</span></span> | <span data-ttu-id="74407-884">返品</span><span class="sxs-lookup"><span data-stu-id="74407-884">Returns</span></span> | <span data-ttu-id="74407-885">説明</span><span class="sxs-lookup"><span data-stu-id="74407-885">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-886">新規</span><span class="sxs-lookup"><span data-stu-id="74407-886">new</span></span> | <span data-ttu-id="74407-887">無効</span><span class="sxs-lookup"><span data-stu-id="74407-887">void</span></span> |  |
| <span data-ttu-id="74407-888">getPageName</span><span class="sxs-lookup"><span data-stu-id="74407-888">getPageName</span></span> | <span data-ttu-id="74407-889">str</span><span class="sxs-lookup"><span data-stu-id="74407-889">str</span></span> | <span data-ttu-id="74407-890">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-890">Returns the page name</span></span> |
| <span data-ttu-id="74407-891">pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-891">pageTitle</span></span> | <span data-ttu-id="74407-892">str</span><span class="sxs-lookup"><span data-stu-id="74407-892">str</span></span> | <span data-ttu-id="74407-893">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-893">Gets and sets the page title</span></span> |
| <span data-ttu-id="74407-894">pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-894">pageDescription</span></span> | <span data-ttu-id="74407-895">str</span><span class="sxs-lookup"><span data-stu-id="74407-895">str</span></span> | <span data-ttu-id="74407-896">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-896">Gets or sets the page description</span></span> |
| <span data-ttu-id="74407-897">pageHidden</span><span class="sxs-lookup"><span data-stu-id="74407-897">pageHidden</span></span> | <span data-ttu-id="74407-898">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-898">boolean</span></span> | <span data-ttu-id="74407-899">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-899">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="74407-900">pageOrder</span><span class="sxs-lookup"><span data-stu-id="74407-900">pageOrder</span></span> | <span data-ttu-id="74407-901">int</span><span class="sxs-lookup"><span data-stu-id="74407-901">int</span></span> | <span data-ttu-id="74407-902">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-902">Gets or sets the page order</span></span> |
| <span data-ttu-id="74407-903">getControl</span><span class="sxs-lookup"><span data-stu-id="74407-903">getControl</span></span> | <span data-ttu-id="74407-904">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-904">SysAppControlMetadata</span></span> | <span data-ttu-id="74407-905">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-905">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="74407-906">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-906">getControlEnumerator</span></span> | <span data-ttu-id="74407-907">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-907">MapEnumerator</span></span> | <span data-ttu-id="74407-908">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-908">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="74407-909">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-909">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-910">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata) 


#### <a name="parameters"></a><span data-ttu-id="74407-911">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-911">Parameters</span></span>

| <span data-ttu-id="74407-912">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-912">Parameter name</span></span> |  <span data-ttu-id="74407-913">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-913">Parameter type</span></span> | <span data-ttu-id="74407-914">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-914">Optional</span></span> | <span data-ttu-id="74407-915">説明</span><span class="sxs-lookup"><span data-stu-id="74407-915">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-916">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-916">_pageMetadata</span></span> | <span data-ttu-id="74407-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="74407-918">False</span><span class="sxs-lookup"><span data-stu-id="74407-918">False</span></span> | 


### <a name="method-getpagename"></a><span data-ttu-id="74407-919">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="74407-919">Method getPageName</span></span> 
<span data-ttu-id="74407-920">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-920">Returns the page name</span></span>

     public str getPageName () 


#### <a name="return-value"></a><span data-ttu-id="74407-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-921">Return Value</span></span> 
<span data-ttu-id="74407-922">ページ名</span><span class="sxs-lookup"><span data-stu-id="74407-922">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="74407-923">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-923">Method pageTitle</span></span> 
<span data-ttu-id="74407-924">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-924">Gets and sets the page title</span></span>

     public str pageTitle ([str _pageTitle]) 


#### <a name="parameters"></a><span data-ttu-id="74407-925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-925">Parameters</span></span>

| <span data-ttu-id="74407-926">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-926">Parameter name</span></span> |  <span data-ttu-id="74407-927">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-927">Parameter type</span></span> | <span data-ttu-id="74407-928">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-928">Optional</span></span> | <span data-ttu-id="74407-929">説明</span><span class="sxs-lookup"><span data-stu-id="74407-929">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-930">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-930">_pageTitle</span></span> | <span data-ttu-id="74407-931">str</span><span class="sxs-lookup"><span data-stu-id="74407-931">str</span></span> | <span data-ttu-id="74407-932">はい</span><span class="sxs-lookup"><span data-stu-id="74407-932">True</span></span> | <span data-ttu-id="74407-933">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-933">The page title</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-934">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-934">Return Value</span></span> 
<span data-ttu-id="74407-935">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-935">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="74407-936">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-936">Method pageDescription</span></span> 
<span data-ttu-id="74407-937">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-937">Gets or sets the page description</span></span>

     public str pageDescription ([str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-938">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-938">Parameters</span></span>

| <span data-ttu-id="74407-939">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-939">Parameter name</span></span> |  <span data-ttu-id="74407-940">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-940">Parameter type</span></span> | <span data-ttu-id="74407-941">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-941">Optional</span></span> | <span data-ttu-id="74407-942">説明</span><span class="sxs-lookup"><span data-stu-id="74407-942">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-943">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-943">_pageDescription</span></span> | <span data-ttu-id="74407-944">str</span><span class="sxs-lookup"><span data-stu-id="74407-944">str</span></span> | <span data-ttu-id="74407-945">はい</span><span class="sxs-lookup"><span data-stu-id="74407-945">True</span></span> | <span data-ttu-id="74407-946">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-946">The page description</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-947">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-947">Return Value</span></span> 
<span data-ttu-id="74407-948">ページの説明></span><span class="sxs-lookup"><span data-stu-id="74407-948">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="74407-949">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="74407-949">Method pageHidden</span></span> 
<span data-ttu-id="74407-950">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-950">Gets and sets whether the page is hidden in the workspace</span></span>

     public boolean pageHidden ([boolean _pageHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-951">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-951">Parameters</span></span>

| <span data-ttu-id="74407-952">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-952">Parameter name</span></span> |  <span data-ttu-id="74407-953">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-953">Parameter type</span></span> | <span data-ttu-id="74407-954">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-954">Optional</span></span> | <span data-ttu-id="74407-955">説明</span><span class="sxs-lookup"><span data-stu-id="74407-955">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-956">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="74407-956">_pageHidden</span></span> | <span data-ttu-id="74407-957">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-957">boolean</span></span> | <span data-ttu-id="74407-958">はい</span><span class="sxs-lookup"><span data-stu-id="74407-958">True</span></span> | <span data-ttu-id="74407-959">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="74407-959">page hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-960">Return Value</span></span> 
<span data-ttu-id="74407-961">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="74407-961">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="74407-962">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="74407-962">Method pageOrder</span></span> 
<span data-ttu-id="74407-963">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-963">Gets or sets the page order</span></span>

     public int pageOrder ([int _pageOrder]) 


#### <a name="parameters"></a><span data-ttu-id="74407-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-964">Parameters</span></span>

| <span data-ttu-id="74407-965">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-965">Parameter name</span></span> |  <span data-ttu-id="74407-966">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-966">Parameter type</span></span> | <span data-ttu-id="74407-967">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-967">Optional</span></span> | <span data-ttu-id="74407-968">説明</span><span class="sxs-lookup"><span data-stu-id="74407-968">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-969">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="74407-969">_pageOrder</span></span> | <span data-ttu-id="74407-970">int</span><span class="sxs-lookup"><span data-stu-id="74407-970">int</span></span> | <span data-ttu-id="74407-971">はい</span><span class="sxs-lookup"><span data-stu-id="74407-971">True</span></span> | <span data-ttu-id="74407-972">ページの順序</span><span class="sxs-lookup"><span data-stu-id="74407-972">The page order</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-973">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-973">Return Value</span></span> 
<span data-ttu-id="74407-974">ページの順序</span><span class="sxs-lookup"><span data-stu-id="74407-974">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="74407-975">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="74407-975">Method getControl</span></span> 
<span data-ttu-id="74407-976">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-976">Returns the control on the current page having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="74407-977">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-977">Parameters</span></span>

| <span data-ttu-id="74407-978">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-978">Parameter name</span></span> |  <span data-ttu-id="74407-979">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-979">Parameter type</span></span> | <span data-ttu-id="74407-980">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-980">Optional</span></span> | <span data-ttu-id="74407-981">説明</span><span class="sxs-lookup"><span data-stu-id="74407-981">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-982">_controlName</span><span class="sxs-lookup"><span data-stu-id="74407-982">_controlName</span></span> | <span data-ttu-id="74407-983">str</span><span class="sxs-lookup"><span data-stu-id="74407-983">str</span></span> | <span data-ttu-id="74407-984">False</span><span class="sxs-lookup"><span data-stu-id="74407-984">False</span></span> | <span data-ttu-id="74407-985">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="74407-985">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-986">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-986">Return Value</span></span> 
<span data-ttu-id="74407-987">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="74407-987">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="74407-988">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-988">Method getControlEnumerator</span></span> 
<span data-ttu-id="74407-989">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-989">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="74407-990">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-990">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-991">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-991">Return Value</span></span> 
<span data-ttu-id="74407-992">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-992">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="74407-993">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-993">Class SysAppProjectionAttribute</span></span> 
<span data-ttu-id="74407-994">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-994">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="74407-995">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-995">Methods</span></span>

| <span data-ttu-id="74407-996">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-996">Method name</span></span> | <span data-ttu-id="74407-997">返品</span><span class="sxs-lookup"><span data-stu-id="74407-997">Returns</span></span> | <span data-ttu-id="74407-998">説明</span><span class="sxs-lookup"><span data-stu-id="74407-998">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-999">新規</span><span class="sxs-lookup"><span data-stu-id="74407-999">new</span></span> | <span data-ttu-id="74407-1000">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1000">void</span></span> | <span data-ttu-id="74407-1001">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1001">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1002">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1002">Method new</span></span> 
<span data-ttu-id="74407-1003">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1003">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

     public void new (str _label) 


#### <a name="parameters"></a><span data-ttu-id="74407-1004">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1004">Parameters</span></span>

| <span data-ttu-id="74407-1005">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1005">Parameter name</span></span> |  <span data-ttu-id="74407-1006">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1006">Parameter type</span></span> | <span data-ttu-id="74407-1007">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1007">Optional</span></span> | <span data-ttu-id="74407-1008">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1008">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1009">_label</span><span class="sxs-lookup"><span data-stu-id="74407-1009">_label</span></span> | <span data-ttu-id="74407-1010">str</span><span class="sxs-lookup"><span data-stu-id="74407-1010">str</span></span> | <span data-ttu-id="74407-1011">False</span><span class="sxs-lookup"><span data-stu-id="74407-1011">False</span></span> | <span data-ttu-id="74407-1012">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-1012">Control label</span></span>


## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="74407-1013">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1013">Class SysAppRelationalAttribute</span></span> 
<span data-ttu-id="74407-1014">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1014">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1015">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1015">Methods</span></span>

| <span data-ttu-id="74407-1016">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1016">Method name</span></span> | <span data-ttu-id="74407-1017">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1017">Returns</span></span> | <span data-ttu-id="74407-1018">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1018">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1019">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1019">new</span></span> | <span data-ttu-id="74407-1020">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1020">void</span></span> | <span data-ttu-id="74407-1021">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-1021">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1022">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1022">Method new</span></span> 
<span data-ttu-id="74407-1023">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-1023">Constructor</span></span>

     public void new ([str _name]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1024">Parameters</span></span>

| <span data-ttu-id="74407-1025">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1025">Parameter name</span></span> |  <span data-ttu-id="74407-1026">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1026">Parameter type</span></span> | <span data-ttu-id="74407-1027">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1027">Optional</span></span> | <span data-ttu-id="74407-1028">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1028">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1029">_name</span><span class="sxs-lookup"><span data-stu-id="74407-1029">_name</span></span> | <span data-ttu-id="74407-1030">str</span><span class="sxs-lookup"><span data-stu-id="74407-1030">str</span></span> | <span data-ttu-id="74407-1031">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1031">True</span></span> | <span data-ttu-id="74407-1032">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="74407-1032">Property name of the referenced entity</span></span>


## <a name="class-sysapprequestparams"></a><span data-ttu-id="74407-1033">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="74407-1033">Class SysAppRequestParams</span></span> 
<span data-ttu-id="74407-1034">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="74407-1034">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1035">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1035">Methods</span></span>

| <span data-ttu-id="74407-1036">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1036">Method name</span></span> | <span data-ttu-id="74407-1037">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1037">Returns</span></span> | <span data-ttu-id="74407-1038">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1038">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1039">entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-1039">entityContext</span></span> | <span data-ttu-id="74407-1040">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-1040">SysAppEntityContext</span></span> | <span data-ttu-id="74407-1041">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1041">Entity context of the request</span></span> |
| <span data-ttu-id="74407-1042">filterContext</span><span class="sxs-lookup"><span data-stu-id="74407-1042">filterContext</span></span> | <span data-ttu-id="74407-1043">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-1043">List</span></span> | <span data-ttu-id="74407-1044">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-1044">List of SysAppFilterContext for filter contexts</span></span> |


### <a name="method-entitycontext"></a><span data-ttu-id="74407-1045">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-1045">Method entityContext</span></span> 
<span data-ttu-id="74407-1046">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1046">Entity context of the request</span></span>

     public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1047">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1047">Parameters</span></span>

| <span data-ttu-id="74407-1048">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1048">Parameter name</span></span> |  <span data-ttu-id="74407-1049">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1049">Parameter type</span></span> | <span data-ttu-id="74407-1050">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1050">Optional</span></span> | <span data-ttu-id="74407-1051">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1051">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1052">_entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-1052">_entityContext</span></span> | <span data-ttu-id="74407-1053">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-1053">SysAppEntityContext</span></span> | <span data-ttu-id="74407-1054">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1054">True</span></span> | <span data-ttu-id="74407-1055">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1055">Entity context of the request</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1056">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1056">Return Value</span></span> 
<span data-ttu-id="74407-1057">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1057">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="74407-1058">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="74407-1058">Method filterContext</span></span> 
<span data-ttu-id="74407-1059">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-1059">List of SysAppFilterContext for filter contexts</span></span>

     public List filterContext ([List _filterContext]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1060">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1060">Parameters</span></span>

| <span data-ttu-id="74407-1061">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1061">Parameter name</span></span> |  <span data-ttu-id="74407-1062">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1062">Parameter type</span></span> | <span data-ttu-id="74407-1063">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1063">Optional</span></span> | <span data-ttu-id="74407-1064">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1064">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1065">_filterContext</span><span class="sxs-lookup"><span data-stu-id="74407-1065">_filterContext</span></span> | <span data-ttu-id="74407-1066">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-1066">List</span></span> | <span data-ttu-id="74407-1067">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1067">True</span></span> | <span data-ttu-id="74407-1068">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-1068">List of SysAppFilterContext for filter contexts of page</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1069">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1069">Return Value</span></span> 
<span data-ttu-id="74407-1070">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-1070">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="74407-1071">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="74407-1071">Class SysAppResponse</span></span> 
<span data-ttu-id="74407-1072">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="74407-1072">SysAppResponse class.</span></span>  <span data-ttu-id="74407-1073">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="74407-1073">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1074">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1074">Methods</span></span>

| <span data-ttu-id="74407-1075">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1075">Method name</span></span> | <span data-ttu-id="74407-1076">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1076">Returns</span></span> | <span data-ttu-id="74407-1077">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1077">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1078">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1078">new</span></span> | <span data-ttu-id="74407-1079">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1079">void</span></span> |  |
| <span data-ttu-id="74407-1080">jobId</span><span class="sxs-lookup"><span data-stu-id="74407-1080">jobId</span></span> | <span data-ttu-id="74407-1081">str</span><span class="sxs-lookup"><span data-stu-id="74407-1081">str</span></span> | <span data-ttu-id="74407-1082">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-1082">Job Id of the request</span></span> |
| <span data-ttu-id="74407-1083">データ</span><span class="sxs-lookup"><span data-stu-id="74407-1083">data</span></span> | <span data-ttu-id="74407-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="74407-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="74407-1085">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-1085">Data of the page</span></span> |
| <span data-ttu-id="74407-1086">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="74407-1086">failedInAppCall</span></span> | <span data-ttu-id="74407-1087">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1087">boolean</span></span> | <span data-ttu-id="74407-1088">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-1088">Data of the page</span></span> |
| <span data-ttu-id="74407-1089">commits</span><span class="sxs-lookup"><span data-stu-id="74407-1089">commits</span></span> | <span data-ttu-id="74407-1090">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-1090">List</span></span> | <span data-ttu-id="74407-1091">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="74407-1091">Commits after task is completed</span></span> |
| <span data-ttu-id="74407-1092">メッセージ</span><span class="sxs-lookup"><span data-stu-id="74407-1092">messages</span></span> | <span data-ttu-id="74407-1093">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-1093">List</span></span> | <span data-ttu-id="74407-1094">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-1094">Job Id of the request</span></span> |
| <span data-ttu-id="74407-1095">addMessage</span><span class="sxs-lookup"><span data-stu-id="74407-1095">addMessage</span></span> | <span data-ttu-id="74407-1096">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1096">void</span></span> | <span data-ttu-id="74407-1097">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="74407-1097">Adds message</span></span> |
| <span data-ttu-id="74407-1098">addCommit</span><span class="sxs-lookup"><span data-stu-id="74407-1098">addCommit</span></span> | <span data-ttu-id="74407-1099">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1099">void</span></span> | <span data-ttu-id="74407-1100">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="74407-1100">Adds commits</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1101">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1101">Method new</span></span> 


     public void new () 


### <a name="method-jobid"></a><span data-ttu-id="74407-1102">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="74407-1102">Method jobId</span></span> 
<span data-ttu-id="74407-1103">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-1103">Job Id of the request</span></span>

     public str jobId () 


#### <a name="return-value"></a><span data-ttu-id="74407-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1104">Return Value</span></span> 
<span data-ttu-id="74407-1105">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-1105">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="74407-1106">メソッド data</span><span class="sxs-lookup"><span data-stu-id="74407-1106">Method data</span></span> 
<span data-ttu-id="74407-1107">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-1107">Data of the page</span></span>

     public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1108">Parameters</span></span>

| <span data-ttu-id="74407-1109">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1109">Parameter name</span></span> |  <span data-ttu-id="74407-1110">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1110">Parameter type</span></span> | <span data-ttu-id="74407-1111">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1111">Optional</span></span> | <span data-ttu-id="74407-1112">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1112">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1113">_data</span><span class="sxs-lookup"><span data-stu-id="74407-1113">_data</span></span> | <span data-ttu-id="74407-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="74407-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="74407-1115">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1115">True</span></span> | <span data-ttu-id="74407-1116">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-1116">Data of the page</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1117">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1117">Return Value</span></span> 
<span data-ttu-id="74407-1118">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-1118">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="74407-1119">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="74407-1119">Method failedInAppCall</span></span> 
<span data-ttu-id="74407-1120">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-1120">Data of the page</span></span>

     public boolean failedInAppCall ([boolean _failedInAppCall]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1121">Parameters</span></span>

| <span data-ttu-id="74407-1122">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1122">Parameter name</span></span> |  <span data-ttu-id="74407-1123">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1123">Parameter type</span></span> | <span data-ttu-id="74407-1124">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1124">Optional</span></span> | <span data-ttu-id="74407-1125">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1125">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1126">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="74407-1126">_failedInAppCall</span></span> | <span data-ttu-id="74407-1127">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1127">boolean</span></span> | <span data-ttu-id="74407-1128">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1128">True</span></span> | <span data-ttu-id="74407-1129">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="74407-1129">Sets to true if it fails in calling application code</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1130">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1130">Return Value</span></span> 
<span data-ttu-id="74407-1131">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="74407-1131">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="74407-1132">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="74407-1132">Method commits</span></span> 
<span data-ttu-id="74407-1133">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="74407-1133">Commits after task is completed</span></span>

     public List commits () 


#### <a name="return-value"></a><span data-ttu-id="74407-1134">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1134">Return Value</span></span> 
<span data-ttu-id="74407-1135">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="74407-1135">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="74407-1136">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="74407-1136">Method messages</span></span> 
<span data-ttu-id="74407-1137">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-1137">Job Id of the request</span></span>

     public List messages () 


#### <a name="return-value"></a><span data-ttu-id="74407-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1138">Return Value</span></span> 
<span data-ttu-id="74407-1139">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="74407-1139">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="74407-1140">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="74407-1140">Method addMessage</span></span> 
<span data-ttu-id="74407-1141">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="74407-1141">Adds message</span></span>

     public void addMessage (SysAppResponseMessage _message) 


#### <a name="parameters"></a><span data-ttu-id="74407-1142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1142">Parameters</span></span>

| <span data-ttu-id="74407-1143">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1143">Parameter name</span></span> |  <span data-ttu-id="74407-1144">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1144">Parameter type</span></span> | <span data-ttu-id="74407-1145">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1145">Optional</span></span> | <span data-ttu-id="74407-1146">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1146">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1147">_message</span><span class="sxs-lookup"><span data-stu-id="74407-1147">_message</span></span> | <span data-ttu-id="74407-1148">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="74407-1148">SysAppResponseMessage</span></span> | <span data-ttu-id="74407-1149">False</span><span class="sxs-lookup"><span data-stu-id="74407-1149">False</span></span> | <span data-ttu-id="74407-1150">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="74407-1150">message as SysAppResponseMessage object</span></span>


### <a name="method-addcommit"></a><span data-ttu-id="74407-1151">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="74407-1151">Method addCommit</span></span> 
<span data-ttu-id="74407-1152">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="74407-1152">Adds commits</span></span>

     public void addCommit (SysAppEntityContext _entityContext) 


#### <a name="parameters"></a><span data-ttu-id="74407-1153">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1153">Parameters</span></span>

| <span data-ttu-id="74407-1154">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1154">Parameter name</span></span> |  <span data-ttu-id="74407-1155">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1155">Parameter type</span></span> | <span data-ttu-id="74407-1156">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1156">Optional</span></span> | <span data-ttu-id="74407-1157">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1157">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1158">_entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-1158">_entityContext</span></span> | <span data-ttu-id="74407-1159">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-1159">SysAppEntityContext</span></span> | <span data-ttu-id="74407-1160">False</span><span class="sxs-lookup"><span data-stu-id="74407-1160">False</span></span> | <span data-ttu-id="74407-1161">確定済のエンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1161">Entity context containing entity name and entity id of the entity that is committed</span></span>


## <a name="class-sysappresponsemessage"></a><span data-ttu-id="74407-1162">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="74407-1162">Class SysAppResponseMessage</span></span> 
<span data-ttu-id="74407-1163">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="74407-1163">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1164">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1164">Methods</span></span>

| <span data-ttu-id="74407-1165">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1165">Method name</span></span> | <span data-ttu-id="74407-1166">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1166">Returns</span></span> | <span data-ttu-id="74407-1167">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1167">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1168">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1168">new</span></span> | <span data-ttu-id="74407-1169">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1169">void</span></span> | <span data-ttu-id="74407-1170">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1170">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="74407-1171">テキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1171">text</span></span> | <span data-ttu-id="74407-1172">str</span><span class="sxs-lookup"><span data-stu-id="74407-1172">str</span></span> | <span data-ttu-id="74407-1173">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="74407-1173">Gets the message text</span></span> |
| <span data-ttu-id="74407-1174">タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1174">type</span></span> | <span data-ttu-id="74407-1175">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="74407-1175">SysAppMessageType</span></span> | <span data-ttu-id="74407-1176">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-1176">Gets the message type: info, error , warning</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1177">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1177">Method new</span></span> 
<span data-ttu-id="74407-1178">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1178">Creates a new instance of SysAppResponseMessage class</span></span>

     public void new (str _text, [SysAppMessageType _type]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1179">Parameters</span></span>

| <span data-ttu-id="74407-1180">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1180">Parameter name</span></span> |  <span data-ttu-id="74407-1181">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1181">Parameter type</span></span> | <span data-ttu-id="74407-1182">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1182">Optional</span></span> | <span data-ttu-id="74407-1183">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1183">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1184">_text</span><span class="sxs-lookup"><span data-stu-id="74407-1184">_text</span></span> | <span data-ttu-id="74407-1185">str</span><span class="sxs-lookup"><span data-stu-id="74407-1185">str</span></span> | <span data-ttu-id="74407-1186">False</span><span class="sxs-lookup"><span data-stu-id="74407-1186">False</span></span> | <span data-ttu-id="74407-1187">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1187">The message text</span></span>
| <span data-ttu-id="74407-1188">_type</span><span class="sxs-lookup"><span data-stu-id="74407-1188">_type</span></span> | <span data-ttu-id="74407-1189">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="74407-1189">SysAppMessageType</span></span> | <span data-ttu-id="74407-1190">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1190">True</span></span> | <span data-ttu-id="74407-1191">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-1191">Message Type: info, error , warning</span></span>


### <a name="method-text"></a><span data-ttu-id="74407-1192">メソッド text</span><span class="sxs-lookup"><span data-stu-id="74407-1192">Method text</span></span> 
<span data-ttu-id="74407-1193">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="74407-1193">Gets the message text</span></span>

     public str text () 


#### <a name="return-value"></a><span data-ttu-id="74407-1194">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1194">Return Value</span></span> 
<span data-ttu-id="74407-1195">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="74407-1195">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="74407-1196">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1196">Method type</span></span> 
<span data-ttu-id="74407-1197">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-1197">Gets the message type: info, error , warning</span></span>

     public SysAppMessageType type () 


#### <a name="return-value"></a><span data-ttu-id="74407-1198">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1198">Return Value</span></span> 
<span data-ttu-id="74407-1199">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-1199">The message type: info, error , warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="74407-1200">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1200">Class SysAppSecurityAttribute</span></span> 
<span data-ttu-id="74407-1201">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="74407-1201">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="74407-1202">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="74407-1202">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1203">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1203">Methods</span></span>

| <span data-ttu-id="74407-1204">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1204">Method name</span></span> | <span data-ttu-id="74407-1205">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1205">Returns</span></span> | <span data-ttu-id="74407-1206">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1206">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1207">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1207">new</span></span> | <span data-ttu-id="74407-1208">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1208">void</span></span> | <span data-ttu-id="74407-1209">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="74407-1209">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="74407-1210">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="74407-1210">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="74407-1211">menuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1211">menuItemType</span></span> | <span data-ttu-id="74407-1212">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1212">MenuItemType</span></span> | <span data-ttu-id="74407-1213">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="74407-1213">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="74407-1214">menuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1214">menuItemName</span></span> | <span data-ttu-id="74407-1215">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1215">MenuItemName</span></span> | <span data-ttu-id="74407-1216">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="74407-1216">Gets the Menu Item Name of the page</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1217">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1217">Method new</span></span> 
<span data-ttu-id="74407-1218">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="74407-1218">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="74407-1219">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="74407-1219">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

     public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1220">Parameters</span></span>

| <span data-ttu-id="74407-1221">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1221">Parameter name</span></span> |  <span data-ttu-id="74407-1222">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1222">Parameter type</span></span> | <span data-ttu-id="74407-1223">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1223">Optional</span></span> | <span data-ttu-id="74407-1224">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1224">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1225">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1225">_menuItemName</span></span> | <span data-ttu-id="74407-1226">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1226">MenuItemName</span></span> | <span data-ttu-id="74407-1227">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1227">True</span></span> | <span data-ttu-id="74407-1228">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="74407-1228">Menu Item Name of the page</span></span>
| <span data-ttu-id="74407-1229">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1229">_menuItemType</span></span> | <span data-ttu-id="74407-1230">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1230">MenuItemType</span></span> | <span data-ttu-id="74407-1231">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1231">True</span></span> | <span data-ttu-id="74407-1232">アクション、表示または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1232">Menu Item Type of the page like action, display or output</span></span>


### <a name="method-menuitemtype"></a><span data-ttu-id="74407-1233">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1233">Method menuItemType</span></span> 
<span data-ttu-id="74407-1234">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="74407-1234">Gets the Menu Item Type of the page</span></span>

     public MenuItemType menuItemType () 


#### <a name="return-value"></a><span data-ttu-id="74407-1235">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1235">Return Value</span></span> 
<span data-ttu-id="74407-1236">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1236">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="74407-1237">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1237">Method menuItemName</span></span> 
<span data-ttu-id="74407-1238">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="74407-1238">Gets the Menu Item Name of the page</span></span>

     public MenuItemName menuItemName () 


#### <a name="return-value"></a><span data-ttu-id="74407-1239">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1239">Return Value</span></span> 
<span data-ttu-id="74407-1240">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="74407-1240">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="74407-1241">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="74407-1241">Class SysAppWorkspace</span></span> 
<span data-ttu-id="74407-1242">これは、AX モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="74407-1242">This is the base class of AX mobile workspace.</span></span> <span data-ttu-id="74407-1243">AX モバイル ワークスペース クラスは、このクラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74407-1243">AX mobile workspace classes needs to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1244">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1244">Methods</span></span>

| <span data-ttu-id="74407-1245">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1245">Method name</span></span> | <span data-ttu-id="74407-1246">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1246">Returns</span></span> | <span data-ttu-id="74407-1247">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1247">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1248">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="74407-1248">getEnumValues</span></span> | <span data-ttu-id="74407-1249">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-1249">List</span></span> | <span data-ttu-id="74407-1250">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-1250">Called during workspace initialization.</span></span> <span data-ttu-id="74407-1251">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-1251">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="74407-1252">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1252">getWorkspaceMetadata</span></span> | <span data-ttu-id="74407-1253">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1253">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="74407-1254">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-1254">Called during workspace initialization.</span></span> <span data-ttu-id="74407-1255">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-1255">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="74407-1256">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-1256">onBeginAppJob</span></span> | <span data-ttu-id="74407-1257">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1257">void</span></span> | <span data-ttu-id="74407-1258">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-1258">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="74407-1259">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-1259">onEndAppJob</span></span> | <span data-ttu-id="74407-1260">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1260">void</span></span> | <span data-ttu-id="74407-1261">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-1261">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="74407-1262">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1262">workspaceHidden</span></span> | <span data-ttu-id="74407-1263">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1263">boolean</span></span> | <span data-ttu-id="74407-1264">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="74407-1264">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="74407-1265">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74407-1265">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="74407-1266">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1266">If the attribute is not specified on the class than it always returns false</span></span> |


### <a name="method-getenumvalues"></a><span data-ttu-id="74407-1267">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="74407-1267">Method getEnumValues</span></span> 
<span data-ttu-id="74407-1268">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-1268">Called during workspace initialization.</span></span> <span data-ttu-id="74407-1269">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-1269">Can be used to modify the enum values that are returned to AX mobile</span></span>

     public List getEnumValues (EnumName _enumName) 


#### <a name="parameters"></a><span data-ttu-id="74407-1270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1270">Parameters</span></span>

| <span data-ttu-id="74407-1271">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1271">Parameter name</span></span> |  <span data-ttu-id="74407-1272">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1272">Parameter type</span></span> | <span data-ttu-id="74407-1273">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1273">Optional</span></span> | <span data-ttu-id="74407-1274">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1274">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1275">_enumName</span><span class="sxs-lookup"><span data-stu-id="74407-1275">_enumName</span></span> | <span data-ttu-id="74407-1276">EnumName</span><span class="sxs-lookup"><span data-stu-id="74407-1276">EnumName</span></span> | <span data-ttu-id="74407-1277">False</span><span class="sxs-lookup"><span data-stu-id="74407-1277">False</span></span> | <span data-ttu-id="74407-1278">列挙名</span><span class="sxs-lookup"><span data-stu-id="74407-1278">The enum name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1279">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1279">Return Value</span></span> 
<span data-ttu-id="74407-1280">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="74407-1280">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="74407-1281">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1281">Method getWorkspaceMetadata</span></span> 
<span data-ttu-id="74407-1282">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-1282">Called during workspace initialization.</span></span> <span data-ttu-id="74407-1283">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-1283">Can be used to modify the workspace metadata</span></span>

     public SysAppWorkspaceMetadata getWorkspaceMetadata () 


#### <a name="return-value"></a><span data-ttu-id="74407-1284">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1284">Return Value</span></span> 
<span data-ttu-id="74407-1285">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-1285">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="74407-1286">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-1286">Method onBeginAppJob</span></span> 
<span data-ttu-id="74407-1287">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-1287">Called before the start of execution of AX mobile job</span></span>

     public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest) 


#### <a name="parameters"></a><span data-ttu-id="74407-1288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1288">Parameters</span></span>

| <span data-ttu-id="74407-1289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1289">Parameter name</span></span> |  <span data-ttu-id="74407-1290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1290">Parameter type</span></span> | <span data-ttu-id="74407-1291">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1291">Optional</span></span> | <span data-ttu-id="74407-1292">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1293">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="74407-1293">_sysAppJobRequest</span></span> | <span data-ttu-id="74407-1294">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="74407-1294">SysAppJobRequest</span></span> | <span data-ttu-id="74407-1295">False</span><span class="sxs-lookup"><span data-stu-id="74407-1295">False</span></span> | <span data-ttu-id="74407-1296">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="74407-1296">A class containing job request parameters</span></span>


### <a name="method-onendappjob"></a><span data-ttu-id="74407-1297">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-1297">Method onEndAppJob</span></span> 
<span data-ttu-id="74407-1298">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-1298">Called after the end of execution of AX mobile job</span></span>

     public void onEndAppJob (SysAppJobResponse _sysAppJobResponse) 


#### <a name="parameters"></a><span data-ttu-id="74407-1299">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1299">Parameters</span></span>

| <span data-ttu-id="74407-1300">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1300">Parameter name</span></span> |  <span data-ttu-id="74407-1301">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1301">Parameter type</span></span> | <span data-ttu-id="74407-1302">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1302">Optional</span></span> | <span data-ttu-id="74407-1303">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1303">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1304">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="74407-1304">_sysAppJobResponse</span></span> | <span data-ttu-id="74407-1305">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="74407-1305">SysAppJobResponse</span></span> | <span data-ttu-id="74407-1306">False</span><span class="sxs-lookup"><span data-stu-id="74407-1306">False</span></span> | <span data-ttu-id="74407-1307">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="74407-1307">A class containing job response parameters</span></span>


### <a name="method-workspacehidden"></a><span data-ttu-id="74407-1308">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1308">Method workspaceHidden</span></span> 
<span data-ttu-id="74407-1309">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="74407-1309">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="74407-1310">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74407-1310">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="74407-1311">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1311">If the attribute is not specified on the class than it always returns false</span></span>

     public boolean workspaceHidden () 


#### <a name="return-value"></a><span data-ttu-id="74407-1312">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1312">Return Value</span></span> 
<span data-ttu-id="74407-1313">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1313">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="74407-1314">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1314">Class SysAppWorkspaceAttribute</span></span> 
<span data-ttu-id="74407-1315">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="74407-1315">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1316">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1316">Methods</span></span>

| <span data-ttu-id="74407-1317">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1317">Method name</span></span> | <span data-ttu-id="74407-1318">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1318">Returns</span></span> | <span data-ttu-id="74407-1319">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1319">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1320">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1320">new</span></span> | <span data-ttu-id="74407-1321">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1321">void</span></span> | <span data-ttu-id="74407-1322">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1322">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="74407-1323">AppId</span><span class="sxs-lookup"><span data-stu-id="74407-1323">AppId</span></span> | <span data-ttu-id="74407-1324">str</span><span class="sxs-lookup"><span data-stu-id="74407-1324">str</span></span> | <span data-ttu-id="74407-1325">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1325">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="74407-1326">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-1326">AppResourceName</span></span> | <span data-ttu-id="74407-1327">str</span><span class="sxs-lookup"><span data-stu-id="74407-1327">str</span></span> | <span data-ttu-id="74407-1328">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1328">Gets or sets the AOT Resource name which contains the workspace</span></span> |
| <span data-ttu-id="74407-1329">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1329">WorkspaceHidden</span></span> | <span data-ttu-id="74407-1330">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1330">boolean</span></span> | <span data-ttu-id="74407-1331">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1331">Gets or sets if the workspace is hidden from designer</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1332">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1332">Method new</span></span> 
<span data-ttu-id="74407-1333">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1333">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

     public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1334">Parameters</span></span>

| <span data-ttu-id="74407-1335">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1335">Parameter name</span></span> |  <span data-ttu-id="74407-1336">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1336">Parameter type</span></span> | <span data-ttu-id="74407-1337">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1337">Optional</span></span> | <span data-ttu-id="74407-1338">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1338">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1339">_appId</span><span class="sxs-lookup"><span data-stu-id="74407-1339">_appId</span></span> | <span data-ttu-id="74407-1340">str</span><span class="sxs-lookup"><span data-stu-id="74407-1340">str</span></span> | <span data-ttu-id="74407-1341">False</span><span class="sxs-lookup"><span data-stu-id="74407-1341">False</span></span> | <span data-ttu-id="74407-1342">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="74407-1342">The appId of the workspace</span></span>
| <span data-ttu-id="74407-1343">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-1343">_appResourceName</span></span> | <span data-ttu-id="74407-1344">str</span><span class="sxs-lookup"><span data-stu-id="74407-1344">str</span></span> | <span data-ttu-id="74407-1345">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1345">True</span></span> | <span data-ttu-id="74407-1346">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="74407-1346">The AOT resource name which contains the workspace</span></span>
| <span data-ttu-id="74407-1347">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1347">_workspaceHidden</span></span> | <span data-ttu-id="74407-1348">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1348">boolean</span></span> | <span data-ttu-id="74407-1349">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1349">True</span></span> | <span data-ttu-id="74407-1350">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="74407-1350">The workspace is hidden from designer</span></span>


### <a name="method-appid"></a><span data-ttu-id="74407-1351">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="74407-1351">Method AppId</span></span> 
<span data-ttu-id="74407-1352">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1352">Gets or sets the AppId of the workspace</span></span>

     public str AppId ([str _appId]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1353">Parameters</span></span>

| <span data-ttu-id="74407-1354">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1354">Parameter name</span></span> |  <span data-ttu-id="74407-1355">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1355">Parameter type</span></span> | <span data-ttu-id="74407-1356">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1356">Optional</span></span> | <span data-ttu-id="74407-1357">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1357">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1358">_appId</span><span class="sxs-lookup"><span data-stu-id="74407-1358">_appId</span></span> | <span data-ttu-id="74407-1359">str</span><span class="sxs-lookup"><span data-stu-id="74407-1359">str</span></span> | <span data-ttu-id="74407-1360">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1360">True</span></span> | <span data-ttu-id="74407-1361">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="74407-1361">The AppId of the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1362">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1362">Return Value</span></span> 
<span data-ttu-id="74407-1363">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="74407-1363">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="74407-1364">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-1364">Method AppResourceName</span></span> 
<span data-ttu-id="74407-1365">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1365">Gets or sets the AOT Resource name which contains the workspace</span></span>

     public str AppResourceName ([str _appResourceName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1366">Parameters</span></span>

| <span data-ttu-id="74407-1367">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1367">Parameter name</span></span> |  <span data-ttu-id="74407-1368">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1368">Parameter type</span></span> | <span data-ttu-id="74407-1369">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1369">Optional</span></span> | <span data-ttu-id="74407-1370">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1370">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1371">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-1371">_appResourceName</span></span> | <span data-ttu-id="74407-1372">str</span><span class="sxs-lookup"><span data-stu-id="74407-1372">str</span></span> | <span data-ttu-id="74407-1373">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1373">True</span></span> | <span data-ttu-id="74407-1374">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="74407-1374">The AOT Resource name which contains the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1375">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1375">Return Value</span></span> 
<span data-ttu-id="74407-1376">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="74407-1376">The AOT Resource name which contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="74407-1377">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1377">Method WorkspaceHidden</span></span> 
<span data-ttu-id="74407-1378">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1378">Gets or sets if the workspace is hidden from designer</span></span>

     public boolean WorkspaceHidden ([boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1379">Parameters</span></span>

| <span data-ttu-id="74407-1380">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1380">Parameter name</span></span> |  <span data-ttu-id="74407-1381">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1381">Parameter type</span></span> | <span data-ttu-id="74407-1382">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1382">Optional</span></span> | <span data-ttu-id="74407-1383">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1383">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1384">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1384">_workspaceHidden</span></span> | <span data-ttu-id="74407-1385">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1385">boolean</span></span> | <span data-ttu-id="74407-1386">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1386">True</span></span> | <span data-ttu-id="74407-1387">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="74407-1387">The workspace hidden</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1388">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1388">Return Value</span></span> 
<span data-ttu-id="74407-1389">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="74407-1389">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="74407-1390">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1390">Class SysAppWorkspaceMetadata</span></span> 
<span data-ttu-id="74407-1391">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="74407-1391">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1392">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1392">Methods</span></span>

| <span data-ttu-id="74407-1393">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1393">Method name</span></span> | <span data-ttu-id="74407-1394">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1394">Returns</span></span> | <span data-ttu-id="74407-1395">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1395">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1396">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1396">new</span></span> | <span data-ttu-id="74407-1397">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1397">void</span></span> |  |
| <span data-ttu-id="74407-1398">addConfig</span><span class="sxs-lookup"><span data-stu-id="74407-1398">addConfig</span></span> | <span data-ttu-id="74407-1399">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1399">void</span></span> | <span data-ttu-id="74407-1400">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="74407-1400">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="74407-1401">getPage</span><span class="sxs-lookup"><span data-stu-id="74407-1401">getPage</span></span> | <span data-ttu-id="74407-1402">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1402">SysAppPageMetadata</span></span> | <span data-ttu-id="74407-1403">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="74407-1403">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="74407-1404">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1404">getPageEnumerator</span></span> | <span data-ttu-id="74407-1405">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1405">MapEnumerator</span></span> | <span data-ttu-id="74407-1406">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-1406">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="74407-1407">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-1407">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="74407-1408">getAction</span><span class="sxs-lookup"><span data-stu-id="74407-1408">getAction</span></span> | <span data-ttu-id="74407-1409">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1409">SysAppActionMetadata</span></span> | <span data-ttu-id="74407-1410">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="74407-1410">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="74407-1411">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1411">getActionEnumerator</span></span> | <span data-ttu-id="74407-1412">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1412">MapEnumerator</span></span> | <span data-ttu-id="74407-1413">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-1413">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="74407-1414">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-1414">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="74407-1415">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1415">getPageNameForRecordingId</span></span> | <span data-ttu-id="74407-1416">str</span><span class="sxs-lookup"><span data-stu-id="74407-1416">str</span></span> | <span data-ttu-id="74407-1417">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1417">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="74407-1418">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1418">getActionNameForRecordingId</span></span> | <span data-ttu-id="74407-1419">str</span><span class="sxs-lookup"><span data-stu-id="74407-1419">str</span></span> | <span data-ttu-id="74407-1420">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1420">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="74407-1421">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1421">workspaceTitle</span></span> | <span data-ttu-id="74407-1422">str</span><span class="sxs-lookup"><span data-stu-id="74407-1422">str</span></span> | <span data-ttu-id="74407-1423">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1423">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="74407-1424">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1424">workspaceDescription</span></span> | <span data-ttu-id="74407-1425">str</span><span class="sxs-lookup"><span data-stu-id="74407-1425">str</span></span> | <span data-ttu-id="74407-1426">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1426">Gets and sets the workspace description</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1427">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1427">Method new</span></span> 


     public void new (str _appId, [SysAppWorkspaceAttribute _attribute]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1428">Parameters</span></span>

| <span data-ttu-id="74407-1429">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1429">Parameter name</span></span> |  <span data-ttu-id="74407-1430">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1430">Parameter type</span></span> | <span data-ttu-id="74407-1431">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1431">Optional</span></span> | <span data-ttu-id="74407-1432">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1432">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1433">_appId</span><span class="sxs-lookup"><span data-stu-id="74407-1433">_appId</span></span> | <span data-ttu-id="74407-1434">str</span><span class="sxs-lookup"><span data-stu-id="74407-1434">str</span></span> | <span data-ttu-id="74407-1435">False</span><span class="sxs-lookup"><span data-stu-id="74407-1435">False</span></span> | 
| <span data-ttu-id="74407-1436">_attribute</span><span class="sxs-lookup"><span data-stu-id="74407-1436">_attribute</span></span> | <span data-ttu-id="74407-1437">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1437">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="74407-1438">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1438">True</span></span> | 


### <a name="method-addconfig"></a><span data-ttu-id="74407-1439">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="74407-1439">Method addConfig</span></span> 
<span data-ttu-id="74407-1440">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="74407-1440">Adds a custom config to the mobile workspace metadata</span></span>

     public void addConfig (str _configName, object _configValue) 


#### <a name="parameters"></a><span data-ttu-id="74407-1441">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1441">Parameters</span></span>

| <span data-ttu-id="74407-1442">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1442">Parameter name</span></span> |  <span data-ttu-id="74407-1443">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1443">Parameter type</span></span> | <span data-ttu-id="74407-1444">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1444">Optional</span></span> | <span data-ttu-id="74407-1445">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1445">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1446">_configName</span><span class="sxs-lookup"><span data-stu-id="74407-1446">_configName</span></span> | <span data-ttu-id="74407-1447">str</span><span class="sxs-lookup"><span data-stu-id="74407-1447">str</span></span> | <span data-ttu-id="74407-1448">False</span><span class="sxs-lookup"><span data-stu-id="74407-1448">False</span></span> | <span data-ttu-id="74407-1449">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="74407-1449">A config name</span></span>
| <span data-ttu-id="74407-1450">_configValue</span><span class="sxs-lookup"><span data-stu-id="74407-1450">_configValue</span></span> | <span data-ttu-id="74407-1451">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-1451">object</span></span> | <span data-ttu-id="74407-1452">False</span><span class="sxs-lookup"><span data-stu-id="74407-1452">False</span></span> | <span data-ttu-id="74407-1453">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-1453">An object of a X++ data contract class</span></span>


### <a name="method-getpage"></a><span data-ttu-id="74407-1454">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="74407-1454">Method getPage</span></span> 
<span data-ttu-id="74407-1455">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="74407-1455">Returns the page with the pageName provided</span></span>

     public SysAppPageMetadata getPage (str _pageName) 


#### <a name="parameters"></a><span data-ttu-id="74407-1456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1456">Parameters</span></span>

| <span data-ttu-id="74407-1457">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1457">Parameter name</span></span> |  <span data-ttu-id="74407-1458">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1458">Parameter type</span></span> | <span data-ttu-id="74407-1459">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1459">Optional</span></span> | <span data-ttu-id="74407-1460">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1460">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1461">_pageName</span><span class="sxs-lookup"><span data-stu-id="74407-1461">_pageName</span></span> | <span data-ttu-id="74407-1462">str</span><span class="sxs-lookup"><span data-stu-id="74407-1462">str</span></span> | <span data-ttu-id="74407-1463">False</span><span class="sxs-lookup"><span data-stu-id="74407-1463">False</span></span> | <span data-ttu-id="74407-1464">ページ名</span><span class="sxs-lookup"><span data-stu-id="74407-1464">A page name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1465">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1465">Return Value</span></span> 
<span data-ttu-id="74407-1466">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1466">Returns the pageMetadata if a page with the provided name exist;otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="74407-1467">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1467">Method getPageEnumerator</span></span> 
<span data-ttu-id="74407-1468">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-1468">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="74407-1469">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-1469">Where key is page name and value is of type SysAppPageMetadata</span></span>

     public MapEnumerator getPageEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-1470">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1470">Return Value</span></span> 
<span data-ttu-id="74407-1471">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-1471">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="74407-1472">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="74407-1472">Method getAction</span></span> 
<span data-ttu-id="74407-1473">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="74407-1473">Returns the action with the actionName provided</span></span>

     public SysAppActionMetadata getAction (str _actionName) 


#### <a name="parameters"></a><span data-ttu-id="74407-1474">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1474">Parameters</span></span>

| <span data-ttu-id="74407-1475">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1475">Parameter name</span></span> |  <span data-ttu-id="74407-1476">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1476">Parameter type</span></span> | <span data-ttu-id="74407-1477">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1477">Optional</span></span> | <span data-ttu-id="74407-1478">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1478">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1479">_actionName</span><span class="sxs-lookup"><span data-stu-id="74407-1479">_actionName</span></span> | <span data-ttu-id="74407-1480">str</span><span class="sxs-lookup"><span data-stu-id="74407-1480">str</span></span> | <span data-ttu-id="74407-1481">False</span><span class="sxs-lookup"><span data-stu-id="74407-1481">False</span></span> | <span data-ttu-id="74407-1482">アクション名</span><span class="sxs-lookup"><span data-stu-id="74407-1482">An action name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1483">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1483">Return Value</span></span> 
<span data-ttu-id="74407-1484">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1484">Returns the ActionMetadata if an action with the provided name exist;otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="74407-1485">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1485">Method getActionEnumerator</span></span> 
<span data-ttu-id="74407-1486">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-1486">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="74407-1487">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-1487">Where key is action name and value is of type SysAppActionMetadata</span></span>

     public MapEnumerator getActionEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-1488">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1488">Return Value</span></span> 
<span data-ttu-id="74407-1489">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-1489">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="74407-1490">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1490">Method getPageNameForRecordingId</span></span> 
<span data-ttu-id="74407-1491">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1491">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

     public str getPageNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="74407-1492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1492">Parameters</span></span>

| <span data-ttu-id="74407-1493">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1493">Parameter name</span></span> |  <span data-ttu-id="74407-1494">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1494">Parameter type</span></span> | <span data-ttu-id="74407-1495">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1495">Optional</span></span> | <span data-ttu-id="74407-1496">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1496">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1497">_recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1497">_recordingId</span></span> | <span data-ttu-id="74407-1498">str</span><span class="sxs-lookup"><span data-stu-id="74407-1498">str</span></span> | <span data-ttu-id="74407-1499">False</span><span class="sxs-lookup"><span data-stu-id="74407-1499">False</span></span> | <span data-ttu-id="74407-1500">recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1500">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1501">Return Value</span></span> 
<span data-ttu-id="74407-1502">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="74407-1502">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="74407-1503">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1503">Method getActionNameForRecordingId</span></span> 
<span data-ttu-id="74407-1504">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1504">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

     public str getActionNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="74407-1505">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1505">Parameters</span></span>

| <span data-ttu-id="74407-1506">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1506">Parameter name</span></span> |  <span data-ttu-id="74407-1507">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1507">Parameter type</span></span> | <span data-ttu-id="74407-1508">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1508">Optional</span></span> | <span data-ttu-id="74407-1509">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1509">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1510">_recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1510">_recordingId</span></span> | <span data-ttu-id="74407-1511">str</span><span class="sxs-lookup"><span data-stu-id="74407-1511">str</span></span> | <span data-ttu-id="74407-1512">False</span><span class="sxs-lookup"><span data-stu-id="74407-1512">False</span></span> | <span data-ttu-id="74407-1513">recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-1513">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1514">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1514">Return Value</span></span> 
<span data-ttu-id="74407-1515">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="74407-1515">An action name if the supplied recordingId is used by a workspace action;otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="74407-1516">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1516">Method workspaceTitle</span></span> 
<span data-ttu-id="74407-1517">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1517">Gets and sets the workspace title</span></span>

     public str workspaceTitle ([str _workspaceTitle]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1518">Parameters</span></span>

| <span data-ttu-id="74407-1519">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1519">Parameter name</span></span> |  <span data-ttu-id="74407-1520">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1520">Parameter type</span></span> | <span data-ttu-id="74407-1521">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1521">Optional</span></span> | <span data-ttu-id="74407-1522">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1522">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1523">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1523">_workspaceTitle</span></span> | <span data-ttu-id="74407-1524">str</span><span class="sxs-lookup"><span data-stu-id="74407-1524">str</span></span> | <span data-ttu-id="74407-1525">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1525">True</span></span> | <span data-ttu-id="74407-1526">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="74407-1526">The workspace title</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1527">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1527">Return Value</span></span> 
<span data-ttu-id="74407-1528">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="74407-1528">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="74407-1529">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1529">Method workspaceDescription</span></span> 
<span data-ttu-id="74407-1530">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1530">Gets and sets the workspace description</span></span>

     public str workspaceDescription ([str _workspaceDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1531">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1531">Parameters</span></span>

| <span data-ttu-id="74407-1532">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1532">Parameter name</span></span> |  <span data-ttu-id="74407-1533">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1533">Parameter type</span></span> | <span data-ttu-id="74407-1534">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1534">Optional</span></span> | <span data-ttu-id="74407-1535">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1535">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1536">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1536">_workspaceDescription</span></span> | <span data-ttu-id="74407-1537">str</span><span class="sxs-lookup"><span data-stu-id="74407-1537">str</span></span> | <span data-ttu-id="74407-1538">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1538">True</span></span> | <span data-ttu-id="74407-1539">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="74407-1539">The workspace description</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1540">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1540">Return Value</span></span> 
<span data-ttu-id="74407-1541">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="74407-1541">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="74407-1542">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1542">Class SysAppWorkspaceSecurityAttribute</span></span> 
<span data-ttu-id="74407-1543">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="74407-1543">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1544">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1544">Methods</span></span>

| <span data-ttu-id="74407-1545">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1545">Method name</span></span> | <span data-ttu-id="74407-1546">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1546">Returns</span></span> | <span data-ttu-id="74407-1547">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1547">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1548">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1548">new</span></span> | <span data-ttu-id="74407-1549">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1549">void</span></span> | <span data-ttu-id="74407-1550">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="74407-1550">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="74407-1551">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1551">WorkspaceMenuItemName</span></span> | <span data-ttu-id="74407-1552">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1552">MenuItemName</span></span> | <span data-ttu-id="74407-1553">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1553">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="74407-1554">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1554">WorkspaceMenuItemType</span></span> | <span data-ttu-id="74407-1555">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1555">MenuItemType</span></span> | <span data-ttu-id="74407-1556">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1556">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1557">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1557">Method new</span></span> 
<span data-ttu-id="74407-1558">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="74407-1558">Creates a new instance of attribute</span></span>

     public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1559">Parameters</span></span>

| <span data-ttu-id="74407-1560">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1560">Parameter name</span></span> |  <span data-ttu-id="74407-1561">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1561">Parameter type</span></span> | <span data-ttu-id="74407-1562">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1562">Optional</span></span> | <span data-ttu-id="74407-1563">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1563">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1564">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1564">_workspaceMenuItemName</span></span> | <span data-ttu-id="74407-1565">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1565">MenuItemName</span></span> | <span data-ttu-id="74407-1566">False</span><span class="sxs-lookup"><span data-stu-id="74407-1566">False</span></span> | <span data-ttu-id="74407-1567">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="74407-1567">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="74407-1568">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1568">_workspaceMenuItemType</span></span> | <span data-ttu-id="74407-1569">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1569">MenuItemType</span></span> | <span data-ttu-id="74407-1570">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1570">True</span></span> | <span data-ttu-id="74407-1571">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1571">The menu item type</span></span>


### <a name="method-workspacemenuitemname"></a><span data-ttu-id="74407-1572">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1572">Method WorkspaceMenuItemName</span></span> 
<span data-ttu-id="74407-1573">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1573">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

     public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1574">Parameters</span></span>

| <span data-ttu-id="74407-1575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1575">Parameter name</span></span> |  <span data-ttu-id="74407-1576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1576">Parameter type</span></span> | <span data-ttu-id="74407-1577">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1577">Optional</span></span> | <span data-ttu-id="74407-1578">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1579">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1579">_workspaceMenuItemName</span></span> | <span data-ttu-id="74407-1580">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-1580">MenuItemName</span></span> | <span data-ttu-id="74407-1581">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1581">True</span></span> | <span data-ttu-id="74407-1582">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="74407-1582">The workspace menu item for the workspace security attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1583">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1583">Return Value</span></span> 
<span data-ttu-id="74407-1584">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="74407-1584">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="74407-1585">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1585">Method WorkspaceMenuItemType</span></span> 
<span data-ttu-id="74407-1586">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1586">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

     public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1587">Parameters</span></span>

| <span data-ttu-id="74407-1588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1588">Parameter name</span></span> |  <span data-ttu-id="74407-1589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1589">Parameter type</span></span> | <span data-ttu-id="74407-1590">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1590">Optional</span></span> | <span data-ttu-id="74407-1591">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1592">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1592">_workspaceMenuItemType</span></span> | <span data-ttu-id="74407-1593">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-1593">MenuItemType</span></span> | <span data-ttu-id="74407-1594">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1594">True</span></span> | <span data-ttu-id="74407-1595">workspacesecurity 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1595">The workspace menu item type for the workspacesecurity attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1596">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1596">Return Value</span></span> 
<span data-ttu-id="74407-1597">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1597">The workspace menu item type for the workspace security attribute</span></span>

## <a name="class-sysappactionattribute"></a><span data-ttu-id="74407-1598">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1598">Class SysAppActionAttribute</span></span> 
<span data-ttu-id="74407-1599">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1599">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1600">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1600">Methods</span></span>

| <span data-ttu-id="74407-1601">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1601">Method name</span></span> | <span data-ttu-id="74407-1602">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1602">Returns</span></span> | <span data-ttu-id="74407-1603">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1603">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1604">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1604">new</span></span> | <span data-ttu-id="74407-1605">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1605">void</span></span> | <span data-ttu-id="74407-1606">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1606">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="74407-1607">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="74407-1607">pageMethodName</span></span> | <span data-ttu-id="74407-1608">str</span><span class="sxs-lookup"><span data-stu-id="74407-1608">str</span></span> | <span data-ttu-id="74407-1609">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-1609">Gets the get method name which forms the page under which this task resides</span></span> |
| <span data-ttu-id="74407-1610">actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1610">actionTitle</span></span> | <span data-ttu-id="74407-1611">str</span><span class="sxs-lookup"><span data-stu-id="74407-1611">str</span></span> | <span data-ttu-id="74407-1612">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-1612">Gets the Action Title</span></span> |
| <span data-ttu-id="74407-1613">actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1613">actionDescription</span></span> | <span data-ttu-id="74407-1614">str</span><span class="sxs-lookup"><span data-stu-id="74407-1614">str</span></span> | <span data-ttu-id="74407-1615">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-1615">Gets the Action Description</span></span> |
| <span data-ttu-id="74407-1616">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="74407-1616">crudOperationType</span></span> | <span data-ttu-id="74407-1617">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="74407-1617">SysAppCRUDOperation</span></span> | <span data-ttu-id="74407-1618">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="74407-1618">Gets the Crud Operation Type like Create, Update, Delete</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1619">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1619">Method new</span></span> 
<span data-ttu-id="74407-1620">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1620">Creates a new instance of SysAppActionAttribute class</span></span>

     public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1621">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1621">Parameters</span></span>

| <span data-ttu-id="74407-1622">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1622">Parameter name</span></span> |  <span data-ttu-id="74407-1623">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1623">Parameter type</span></span> | <span data-ttu-id="74407-1624">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1624">Optional</span></span> | <span data-ttu-id="74407-1625">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1625">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1626">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1626">_actionTitle</span></span> | <span data-ttu-id="74407-1627">str</span><span class="sxs-lookup"><span data-stu-id="74407-1627">str</span></span> | <span data-ttu-id="74407-1628">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1628">True</span></span> | <span data-ttu-id="74407-1629">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-1629">Action title</span></span>
| <span data-ttu-id="74407-1630">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1630">_actionDescription</span></span> | <span data-ttu-id="74407-1631">str</span><span class="sxs-lookup"><span data-stu-id="74407-1631">str</span></span> | <span data-ttu-id="74407-1632">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1632">True</span></span> | <span data-ttu-id="74407-1633">アクション説明</span><span class="sxs-lookup"><span data-stu-id="74407-1633">Action description</span></span>
| <span data-ttu-id="74407-1634">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="74407-1634">_crudOperationType</span></span> | <span data-ttu-id="74407-1635">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="74407-1635">SysAppCRUDOperation</span></span> | <span data-ttu-id="74407-1636">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1636">True</span></span> | <span data-ttu-id="74407-1637">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="74407-1637">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="74407-1638">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="74407-1638">_pageMethodName</span></span> | <span data-ttu-id="74407-1639">str</span><span class="sxs-lookup"><span data-stu-id="74407-1639">str</span></span> | <span data-ttu-id="74407-1640">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1640">True</span></span> | <span data-ttu-id="74407-1641">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="74407-1641">Name of the method constructing parent page</span></span>


### <a name="method-pagemethodname"></a><span data-ttu-id="74407-1642">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="74407-1642">Method pageMethodName</span></span> 
<span data-ttu-id="74407-1643">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-1643">Gets the get method name which forms the page under which this task resides</span></span>

     public str pageMethodName () 


#### <a name="return-value"></a><span data-ttu-id="74407-1644">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1644">Return Value</span></span> 
<span data-ttu-id="74407-1645">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1645">The page method name which forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="74407-1646">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1646">Method actionTitle</span></span> 
<span data-ttu-id="74407-1647">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-1647">Gets the Action Title</span></span>

     public str actionTitle () 


#### <a name="return-value"></a><span data-ttu-id="74407-1648">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1648">Return Value</span></span> 
<span data-ttu-id="74407-1649">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-1649">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="74407-1650">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1650">Method actionDescription</span></span> 
<span data-ttu-id="74407-1651">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-1651">Gets the Action Description</span></span>

     public str actionDescription () 


#### <a name="return-value"></a><span data-ttu-id="74407-1652">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1652">Return Value</span></span> 
<span data-ttu-id="74407-1653">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-1653">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="74407-1654">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="74407-1654">Method crudOperationType</span></span> 
<span data-ttu-id="74407-1655">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="74407-1655">Gets the Crud Operation Type like Create, Update, Delete</span></span>

     public SysAppCRUDOperation crudOperationType () 


#### <a name="return-value"></a><span data-ttu-id="74407-1656">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1656">Return Value</span></span> 
<span data-ttu-id="74407-1657">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1657">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="74407-1658">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1658">Class SysAppActionMetadata</span></span> 
<span data-ttu-id="74407-1659">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="74407-1659">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1660">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1660">Methods</span></span>

| <span data-ttu-id="74407-1661">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1661">Method name</span></span> | <span data-ttu-id="74407-1662">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1662">Returns</span></span> | <span data-ttu-id="74407-1663">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1663">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1664">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1664">new</span></span> | <span data-ttu-id="74407-1665">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1665">void</span></span> |  |
| <span data-ttu-id="74407-1666">getActionName</span><span class="sxs-lookup"><span data-stu-id="74407-1666">getActionName</span></span> | <span data-ttu-id="74407-1667">str</span><span class="sxs-lookup"><span data-stu-id="74407-1667">str</span></span> | <span data-ttu-id="74407-1668">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1668">Returns the action name</span></span> |
| <span data-ttu-id="74407-1669">actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1669">actionTitle</span></span> | <span data-ttu-id="74407-1670">str</span><span class="sxs-lookup"><span data-stu-id="74407-1670">str</span></span> | <span data-ttu-id="74407-1671">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1671">Gets or sets the action title</span></span> |
| <span data-ttu-id="74407-1672">actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1672">actionDescription</span></span> | <span data-ttu-id="74407-1673">str</span><span class="sxs-lookup"><span data-stu-id="74407-1673">str</span></span> | <span data-ttu-id="74407-1674">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1674">Gets or sets the action description</span></span> |
| <span data-ttu-id="74407-1675">actionHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1675">actionHidden</span></span> | <span data-ttu-id="74407-1676">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1676">boolean</span></span> | <span data-ttu-id="74407-1677">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1677">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="74407-1678">actionOrder</span><span class="sxs-lookup"><span data-stu-id="74407-1678">actionOrder</span></span> | <span data-ttu-id="74407-1679">int</span><span class="sxs-lookup"><span data-stu-id="74407-1679">int</span></span> | <span data-ttu-id="74407-1680">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1680">Gets or sets the action order</span></span> |
| <span data-ttu-id="74407-1681">getControl</span><span class="sxs-lookup"><span data-stu-id="74407-1681">getControl</span></span> | <span data-ttu-id="74407-1682">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1682">SysAppControlMetadata</span></span> | <span data-ttu-id="74407-1683">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-1683">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="74407-1684">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1684">getControlEnumerator</span></span> | <span data-ttu-id="74407-1685">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1685">MapEnumerator</span></span> | <span data-ttu-id="74407-1686">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-1686">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="74407-1687">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-1687">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1688">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1688">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata) 


#### <a name="parameters"></a><span data-ttu-id="74407-1689">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1689">Parameters</span></span>

| <span data-ttu-id="74407-1690">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1690">Parameter name</span></span> |  <span data-ttu-id="74407-1691">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1691">Parameter type</span></span> | <span data-ttu-id="74407-1692">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1692">Optional</span></span> | <span data-ttu-id="74407-1693">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1693">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1694">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1694">_taskmetadata</span></span> | <span data-ttu-id="74407-1695">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1695">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="74407-1696">False</span><span class="sxs-lookup"><span data-stu-id="74407-1696">False</span></span> | 


### <a name="method-getactionname"></a><span data-ttu-id="74407-1697">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="74407-1697">Method getActionName</span></span> 
<span data-ttu-id="74407-1698">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1698">Returns the action name</span></span>

     public str getActionName () 


#### <a name="return-value"></a><span data-ttu-id="74407-1699">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1699">Return Value</span></span> 
<span data-ttu-id="74407-1700">アクション名</span><span class="sxs-lookup"><span data-stu-id="74407-1700">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="74407-1701">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1701">Method actionTitle</span></span> 
<span data-ttu-id="74407-1702">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1702">Gets or sets the action title</span></span>

     public str actionTitle ([str _actionTitle]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1703">Parameters</span></span>

| <span data-ttu-id="74407-1704">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1704">Parameter name</span></span> |  <span data-ttu-id="74407-1705">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1705">Parameter type</span></span> | <span data-ttu-id="74407-1706">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1706">Optional</span></span> | <span data-ttu-id="74407-1707">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1707">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1708">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="74407-1708">_actionTitle</span></span> | <span data-ttu-id="74407-1709">str</span><span class="sxs-lookup"><span data-stu-id="74407-1709">str</span></span> | <span data-ttu-id="74407-1710">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1710">True</span></span> | <span data-ttu-id="74407-1711">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-1711">The action title</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1712">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1712">Return Value</span></span> 
<span data-ttu-id="74407-1713">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-1713">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="74407-1714">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1714">Method actionDescription</span></span> 
<span data-ttu-id="74407-1715">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1715">Gets or sets the action description</span></span>

     public str actionDescription ([str _actionDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1716">Parameters</span></span>

| <span data-ttu-id="74407-1717">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1717">Parameter name</span></span> |  <span data-ttu-id="74407-1718">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1718">Parameter type</span></span> | <span data-ttu-id="74407-1719">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1719">Optional</span></span> | <span data-ttu-id="74407-1720">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1720">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1721">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="74407-1721">_actionDescription</span></span> | <span data-ttu-id="74407-1722">str</span><span class="sxs-lookup"><span data-stu-id="74407-1722">str</span></span> | <span data-ttu-id="74407-1723">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1723">True</span></span> | <span data-ttu-id="74407-1724">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="74407-1724">The action description</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1725">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1725">Return Value</span></span> 
<span data-ttu-id="74407-1726">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="74407-1726">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="74407-1727">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1727">Method actionHidden</span></span> 
<span data-ttu-id="74407-1728">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1728">Gets or sets whether action is hidden</span></span>

     public boolean actionHidden ([boolean _actionHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1729">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1729">Parameters</span></span>

| <span data-ttu-id="74407-1730">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1730">Parameter name</span></span> |  <span data-ttu-id="74407-1731">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1731">Parameter type</span></span> | <span data-ttu-id="74407-1732">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1732">Optional</span></span> | <span data-ttu-id="74407-1733">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1733">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1734">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1734">_actionHidden</span></span> | <span data-ttu-id="74407-1735">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1735">boolean</span></span> | <span data-ttu-id="74407-1736">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1736">True</span></span> | <span data-ttu-id="74407-1737">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="74407-1737">Action hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1738">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1738">Return Value</span></span> 
<span data-ttu-id="74407-1739">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="74407-1739">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="74407-1740">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="74407-1740">Method actionOrder</span></span> 
<span data-ttu-id="74407-1741">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1741">Gets or sets the action order</span></span>

     public int actionOrder ([int _actionOrder]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1742">Parameters</span></span>

| <span data-ttu-id="74407-1743">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1743">Parameter name</span></span> |  <span data-ttu-id="74407-1744">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1744">Parameter type</span></span> | <span data-ttu-id="74407-1745">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1745">Optional</span></span> | <span data-ttu-id="74407-1746">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1746">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1747">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="74407-1747">_actionOrder</span></span> | <span data-ttu-id="74407-1748">int</span><span class="sxs-lookup"><span data-stu-id="74407-1748">int</span></span> | <span data-ttu-id="74407-1749">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1749">True</span></span> | <span data-ttu-id="74407-1750">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="74407-1750">The action order</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1751">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1751">Return Value</span></span> 
<span data-ttu-id="74407-1752">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="74407-1752">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="74407-1753">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="74407-1753">Method getControl</span></span> 
<span data-ttu-id="74407-1754">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-1754">Returns the control on the current action having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="74407-1755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1755">Parameters</span></span>

| <span data-ttu-id="74407-1756">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1756">Parameter name</span></span> |  <span data-ttu-id="74407-1757">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1757">Parameter type</span></span> | <span data-ttu-id="74407-1758">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1758">Optional</span></span> | <span data-ttu-id="74407-1759">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1759">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1760">_controlName</span><span class="sxs-lookup"><span data-stu-id="74407-1760">_controlName</span></span> | <span data-ttu-id="74407-1761">str</span><span class="sxs-lookup"><span data-stu-id="74407-1761">str</span></span> | <span data-ttu-id="74407-1762">False</span><span class="sxs-lookup"><span data-stu-id="74407-1762">False</span></span> | <span data-ttu-id="74407-1763">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="74407-1763">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1764">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1764">Return Value</span></span> 
<span data-ttu-id="74407-1765">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="74407-1765">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action;otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="74407-1766">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-1766">Method getControlEnumerator</span></span> 
<span data-ttu-id="74407-1767">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-1767">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="74407-1768">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-1768">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-1769">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1769">Return Value</span></span> 
<span data-ttu-id="74407-1770">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-1770">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="74407-1771">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="74407-1771">Class SysAppAttributeHelper</span></span> 
<span data-ttu-id="74407-1772">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="74407-1772">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1773">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1773">Methods</span></span>

| <span data-ttu-id="74407-1774">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1774">Method name</span></span> | <span data-ttu-id="74407-1775">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1775">Returns</span></span> | <span data-ttu-id="74407-1776">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1776">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1777">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="74407-1777">getAttributeFromClass</span></span> | <span data-ttu-id="74407-1778">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1778">SysAttribute</span></span> | <span data-ttu-id="74407-1779">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="74407-1779">gets attribute from class</span></span> |


### <a name="method-getattributefromclass"></a><span data-ttu-id="74407-1780">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="74407-1780">Method getAttributeFromClass</span></span> 
<span data-ttu-id="74407-1781">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="74407-1781">gets attribute from class</span></span>

     public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType) 


#### <a name="parameters"></a><span data-ttu-id="74407-1782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1782">Parameters</span></span>

| <span data-ttu-id="74407-1783">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1783">Parameter name</span></span> |  <span data-ttu-id="74407-1784">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1784">Parameter type</span></span> | <span data-ttu-id="74407-1785">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1785">Optional</span></span> | <span data-ttu-id="74407-1786">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1786">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1787">_sysClass</span><span class="sxs-lookup"><span data-stu-id="74407-1787">_sysClass</span></span> | <span data-ttu-id="74407-1788">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="74407-1788">SysDictClass</span></span> | <span data-ttu-id="74407-1789">False</span><span class="sxs-lookup"><span data-stu-id="74407-1789">False</span></span> | <span data-ttu-id="74407-1790">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="74407-1790">class for which attributes is required</span></span>
| <span data-ttu-id="74407-1791">_attributeType</span><span class="sxs-lookup"><span data-stu-id="74407-1791">_attributeType</span></span> | <span data-ttu-id="74407-1792">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="74407-1792">SysAppAttributeType</span></span> | <span data-ttu-id="74407-1793">False</span><span class="sxs-lookup"><span data-stu-id="74407-1793">False</span></span> | <span data-ttu-id="74407-1794">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="74407-1794">Type of attribute like SysAppEntityAttribute</span></span>


## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="74407-1795">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1795">Class SysAppCollectionAttribute</span></span> 
<span data-ttu-id="74407-1796">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1796">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1797">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1797">Methods</span></span>

| <span data-ttu-id="74407-1798">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1798">Method name</span></span> | <span data-ttu-id="74407-1799">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1799">Returns</span></span> | <span data-ttu-id="74407-1800">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1800">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1801">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1801">new</span></span> | <span data-ttu-id="74407-1802">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1802">void</span></span> | <span data-ttu-id="74407-1803">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-1803">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1804">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1804">Method new</span></span> 
<span data-ttu-id="74407-1805">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-1805">Constructor</span></span>

     public void new (str _itemContractName, [str _label], [str _relationshipName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1806">Parameters</span></span>

| <span data-ttu-id="74407-1807">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1807">Parameter name</span></span> |  <span data-ttu-id="74407-1808">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1808">Parameter type</span></span> | <span data-ttu-id="74407-1809">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1809">Optional</span></span> | <span data-ttu-id="74407-1810">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1810">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1811">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="74407-1811">_itemContractName</span></span> | <span data-ttu-id="74407-1812">str</span><span class="sxs-lookup"><span data-stu-id="74407-1812">str</span></span> | <span data-ttu-id="74407-1813">False</span><span class="sxs-lookup"><span data-stu-id="74407-1813">False</span></span> | <span data-ttu-id="74407-1814">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="74407-1814">Data contract name of list item</span></span>
| <span data-ttu-id="74407-1815">_label</span><span class="sxs-lookup"><span data-stu-id="74407-1815">_label</span></span> | <span data-ttu-id="74407-1816">str</span><span class="sxs-lookup"><span data-stu-id="74407-1816">str</span></span> | <span data-ttu-id="74407-1817">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1817">True</span></span> | <span data-ttu-id="74407-1818">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-1818">List control label</span></span>
| <span data-ttu-id="74407-1819">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="74407-1819">_relationshipName</span></span> | <span data-ttu-id="74407-1820">str</span><span class="sxs-lookup"><span data-stu-id="74407-1820">str</span></span> | <span data-ttu-id="74407-1821">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1821">True</span></span> | <span data-ttu-id="74407-1822">関係名。</span><span class="sxs-lookup"><span data-stu-id="74407-1822">Relationship name.</span></span> <span data-ttu-id="74407-1823">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="74407-1823">By default the entity name of the list item is used as relationship name</span></span>


## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="74407-1824">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1824">Class SysAppControlMetadata</span></span> 
<span data-ttu-id="74407-1825">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="74407-1825">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="74407-1826">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="74407-1826">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1827">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1827">Methods</span></span>

| <span data-ttu-id="74407-1828">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1828">Method name</span></span> | <span data-ttu-id="74407-1829">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1829">Returns</span></span> | <span data-ttu-id="74407-1830">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1830">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1831">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1831">new</span></span> | <span data-ttu-id="74407-1832">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1832">void</span></span> | <span data-ttu-id="74407-1833">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1833">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="74407-1834">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="74407-1834">getBaseLanguageId</span></span> | <span data-ttu-id="74407-1835">str</span><span class="sxs-lookup"><span data-stu-id="74407-1835">str</span></span> | <span data-ttu-id="74407-1836">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1836">Returns the base language id for the app</span></span> |
| <span data-ttu-id="74407-1837">getControlName</span><span class="sxs-lookup"><span data-stu-id="74407-1837">getControlName</span></span> | <span data-ttu-id="74407-1838">str</span><span class="sxs-lookup"><span data-stu-id="74407-1838">str</span></span> | <span data-ttu-id="74407-1839">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1839">Returns the control name</span></span> |
| <span data-ttu-id="74407-1840">controlLabel</span><span class="sxs-lookup"><span data-stu-id="74407-1840">controlLabel</span></span> | <span data-ttu-id="74407-1841">str</span><span class="sxs-lookup"><span data-stu-id="74407-1841">str</span></span> | <span data-ttu-id="74407-1842">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1842">Gets and sets the control label</span></span> |
| <span data-ttu-id="74407-1843">controlHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1843">controlHidden</span></span> | <span data-ttu-id="74407-1844">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1844">boolean</span></span> | <span data-ttu-id="74407-1845">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1845">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="74407-1846">controlOrder</span><span class="sxs-lookup"><span data-stu-id="74407-1846">controlOrder</span></span> | <span data-ttu-id="74407-1847">int</span><span class="sxs-lookup"><span data-stu-id="74407-1847">int</span></span> | <span data-ttu-id="74407-1848">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1848">Gets or sets the control order</span></span> |
| <span data-ttu-id="74407-1849">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="74407-1849">controlMandatory</span></span> | <span data-ttu-id="74407-1850">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1850">boolean</span></span> | <span data-ttu-id="74407-1851">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1851">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="74407-1852">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="74407-1852">controlAllowNegative</span></span> | <span data-ttu-id="74407-1853">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1853">boolean</span></span> | <span data-ttu-id="74407-1854">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="74407-1854">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="74407-1855">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="74407-1855">controlMaxLength</span></span> | <span data-ttu-id="74407-1856">int</span><span class="sxs-lookup"><span data-stu-id="74407-1856">int</span></span> | <span data-ttu-id="74407-1857">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1857">Gets or sets the control max length</span></span> |
| <span data-ttu-id="74407-1858">getProperty</span><span class="sxs-lookup"><span data-stu-id="74407-1858">getProperty</span></span> | <span data-ttu-id="74407-1859">anytype</span><span class="sxs-lookup"><span data-stu-id="74407-1859">anytype</span></span> | <span data-ttu-id="74407-1860">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-1860">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="74407-1861">setProperty</span><span class="sxs-lookup"><span data-stu-id="74407-1861">setProperty</span></span> | <span data-ttu-id="74407-1862">無効</span><span class="sxs-lookup"><span data-stu-id="74407-1862">void</span></span> | <span data-ttu-id="74407-1863">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="74407-1863">Sets the control property referenced by the key</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-1864">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-1864">Method new</span></span> 
<span data-ttu-id="74407-1865">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-1865">Creates a new instance of the control metadata</span></span>

     public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1866">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1866">Parameters</span></span>

| <span data-ttu-id="74407-1867">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1867">Parameter name</span></span> |  <span data-ttu-id="74407-1868">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1868">Parameter type</span></span> | <span data-ttu-id="74407-1869">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1869">Optional</span></span> | <span data-ttu-id="74407-1870">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1870">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1871">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1871">_controlMetadata</span></span> | <span data-ttu-id="74407-1872">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-1872">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="74407-1873">False</span><span class="sxs-lookup"><span data-stu-id="74407-1873">False</span></span> | <span data-ttu-id="74407-1874">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-1874">The controlMetadata object</span></span>
| <span data-ttu-id="74407-1875">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="74407-1875">_baseLanguageId</span></span> | <span data-ttu-id="74407-1876">str</span><span class="sxs-lookup"><span data-stu-id="74407-1876">str</span></span> | <span data-ttu-id="74407-1877">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1877">True</span></span> | <span data-ttu-id="74407-1878">基本言語</span><span class="sxs-lookup"><span data-stu-id="74407-1878">The base language</span></span>


### <a name="method-getbaselanguageid"></a><span data-ttu-id="74407-1879">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="74407-1879">Method getBaseLanguageId</span></span> 
<span data-ttu-id="74407-1880">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1880">Returns the base language id for the app</span></span>

     public str getBaseLanguageId () 


#### <a name="return-value"></a><span data-ttu-id="74407-1881">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1881">Return Value</span></span> 
<span data-ttu-id="74407-1882">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="74407-1882">The base language id</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="74407-1883">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="74407-1883">Method getControlName</span></span> 
<span data-ttu-id="74407-1884">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-1884">Returns the control name</span></span>

     public str getControlName () 


#### <a name="return-value"></a><span data-ttu-id="74407-1885">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1885">Return Value</span></span> 
<span data-ttu-id="74407-1886">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="74407-1886">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="74407-1887">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="74407-1887">Method controlLabel</span></span> 
<span data-ttu-id="74407-1888">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1888">Gets and sets the control label</span></span>

     public str controlLabel ([str _controlLabel]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1889">Parameters</span></span>

| <span data-ttu-id="74407-1890">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1890">Parameter name</span></span> |  <span data-ttu-id="74407-1891">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1891">Parameter type</span></span> | <span data-ttu-id="74407-1892">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1892">Optional</span></span> | <span data-ttu-id="74407-1893">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1893">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1894">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="74407-1894">_controlLabel</span></span> | <span data-ttu-id="74407-1895">str</span><span class="sxs-lookup"><span data-stu-id="74407-1895">str</span></span> | <span data-ttu-id="74407-1896">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1896">True</span></span> | <span data-ttu-id="74407-1897">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-1897">The control label</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1898">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1898">Return Value</span></span> 
<span data-ttu-id="74407-1899">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-1899">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="74407-1900">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1900">Method controlHidden</span></span> 
<span data-ttu-id="74407-1901">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-1901">Gets and sets whether the control is hidden</span></span>

     public boolean controlHidden ([boolean _controlHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1902">Parameters</span></span>

| <span data-ttu-id="74407-1903">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1903">Parameter name</span></span> |  <span data-ttu-id="74407-1904">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1904">Parameter type</span></span> | <span data-ttu-id="74407-1905">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1905">Optional</span></span> | <span data-ttu-id="74407-1906">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1906">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1907">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="74407-1907">_controlHidden</span></span> | <span data-ttu-id="74407-1908">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1908">boolean</span></span> | <span data-ttu-id="74407-1909">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1909">True</span></span> | <span data-ttu-id="74407-1910">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="74407-1910">Control hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1911">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1911">Return Value</span></span> 
<span data-ttu-id="74407-1912">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="74407-1912">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="74407-1913">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="74407-1913">Method controlOrder</span></span> 
<span data-ttu-id="74407-1914">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1914">Gets or sets the control order</span></span>

     public int controlOrder ([int _controlOrder]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1915">Parameters</span></span>

| <span data-ttu-id="74407-1916">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1916">Parameter name</span></span> |  <span data-ttu-id="74407-1917">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1917">Parameter type</span></span> | <span data-ttu-id="74407-1918">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1918">Optional</span></span> | <span data-ttu-id="74407-1919">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1919">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1920">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="74407-1920">_controlOrder</span></span> | <span data-ttu-id="74407-1921">int</span><span class="sxs-lookup"><span data-stu-id="74407-1921">int</span></span> | <span data-ttu-id="74407-1922">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1922">True</span></span> | <span data-ttu-id="74407-1923">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="74407-1923">The control order</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1924">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1924">Return Value</span></span> 
<span data-ttu-id="74407-1925">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="74407-1925">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="74407-1926">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="74407-1926">Method controlMandatory</span></span> 
<span data-ttu-id="74407-1927">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1927">Gets or sets the control mandatory</span></span>

     public boolean controlMandatory ([boolean _controlMandatory]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1928">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1928">Parameters</span></span>

| <span data-ttu-id="74407-1929">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1929">Parameter name</span></span> |  <span data-ttu-id="74407-1930">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1930">Parameter type</span></span> | <span data-ttu-id="74407-1931">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1931">Optional</span></span> | <span data-ttu-id="74407-1932">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1932">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1933">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="74407-1933">_controlMandatory</span></span> | <span data-ttu-id="74407-1934">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1934">boolean</span></span> | <span data-ttu-id="74407-1935">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1935">True</span></span> | <span data-ttu-id="74407-1936">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="74407-1936">The control mandatory</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1937">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1937">Return Value</span></span> 
<span data-ttu-id="74407-1938">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="74407-1938">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="74407-1939">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="74407-1939">Method controlAllowNegative</span></span> 
<span data-ttu-id="74407-1940">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="74407-1940">Gets or sets the control allow negative</span></span>

     public boolean controlAllowNegative ([boolean _controlAllowNegative]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1941">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1941">Parameters</span></span>

| <span data-ttu-id="74407-1942">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1942">Parameter name</span></span> |  <span data-ttu-id="74407-1943">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1943">Parameter type</span></span> | <span data-ttu-id="74407-1944">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1944">Optional</span></span> | <span data-ttu-id="74407-1945">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1945">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1946">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="74407-1946">_controlAllowNegative</span></span> | <span data-ttu-id="74407-1947">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-1947">boolean</span></span> | <span data-ttu-id="74407-1948">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1948">True</span></span> | <span data-ttu-id="74407-1949">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="74407-1949">The control allow negative</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1950">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1950">Return Value</span></span> 
<span data-ttu-id="74407-1951">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="74407-1951">The control allow negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="74407-1952">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="74407-1952">Method controlMaxLength</span></span> 
<span data-ttu-id="74407-1953">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-1953">Gets or sets the control max length</span></span>

     public int controlMaxLength ([int _controlMaxLength]) 


#### <a name="parameters"></a><span data-ttu-id="74407-1954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1954">Parameters</span></span>

| <span data-ttu-id="74407-1955">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1955">Parameter name</span></span> |  <span data-ttu-id="74407-1956">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1956">Parameter type</span></span> | <span data-ttu-id="74407-1957">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1957">Optional</span></span> | <span data-ttu-id="74407-1958">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1958">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1959">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="74407-1959">_controlMaxLength</span></span> | <span data-ttu-id="74407-1960">int</span><span class="sxs-lookup"><span data-stu-id="74407-1960">int</span></span> | <span data-ttu-id="74407-1961">はい</span><span class="sxs-lookup"><span data-stu-id="74407-1961">True</span></span> | <span data-ttu-id="74407-1962">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="74407-1962">The control max length</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1963">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1963">Return Value</span></span> 
<span data-ttu-id="74407-1964">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="74407-1964">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="74407-1965">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="74407-1965">Method getProperty</span></span> 
<span data-ttu-id="74407-1966">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-1966">Gets the control property referenced by the key</span></span>

     public anytype getProperty (str _key) 


#### <a name="parameters"></a><span data-ttu-id="74407-1967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1967">Parameters</span></span>

| <span data-ttu-id="74407-1968">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1968">Parameter name</span></span> |  <span data-ttu-id="74407-1969">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1969">Parameter type</span></span> | <span data-ttu-id="74407-1970">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1970">Optional</span></span> | <span data-ttu-id="74407-1971">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1971">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1972">_key</span><span class="sxs-lookup"><span data-stu-id="74407-1972">_key</span></span> | <span data-ttu-id="74407-1973">str</span><span class="sxs-lookup"><span data-stu-id="74407-1973">str</span></span> | <span data-ttu-id="74407-1974">False</span><span class="sxs-lookup"><span data-stu-id="74407-1974">False</span></span> | <span data-ttu-id="74407-1975">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="74407-1975">The name of the control property</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-1976">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-1976">Return Value</span></span> 
<span data-ttu-id="74407-1977">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="74407-1977">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="74407-1978">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="74407-1978">Method setProperty</span></span> 
<span data-ttu-id="74407-1979">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="74407-1979">Sets the control property referenced by the key</span></span>

     public void setProperty (str _key, anytype _value) 


#### <a name="parameters"></a><span data-ttu-id="74407-1980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-1980">Parameters</span></span>

| <span data-ttu-id="74407-1981">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-1981">Parameter name</span></span> |  <span data-ttu-id="74407-1982">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-1982">Parameter type</span></span> | <span data-ttu-id="74407-1983">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-1983">Optional</span></span> | <span data-ttu-id="74407-1984">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1984">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-1985">_key</span><span class="sxs-lookup"><span data-stu-id="74407-1985">_key</span></span> | <span data-ttu-id="74407-1986">str</span><span class="sxs-lookup"><span data-stu-id="74407-1986">str</span></span> | <span data-ttu-id="74407-1987">False</span><span class="sxs-lookup"><span data-stu-id="74407-1987">False</span></span> | <span data-ttu-id="74407-1988">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="74407-1988">The name of the control property</span></span>
| <span data-ttu-id="74407-1989">_value</span><span class="sxs-lookup"><span data-stu-id="74407-1989">_value</span></span> | <span data-ttu-id="74407-1990">anytype</span><span class="sxs-lookup"><span data-stu-id="74407-1990">anytype</span></span> | <span data-ttu-id="74407-1991">False</span><span class="sxs-lookup"><span data-stu-id="74407-1991">False</span></span> | <span data-ttu-id="74407-1992">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="74407-1992">The value of the control property</span></span>


## <a name="class-sysappentityattribute"></a><span data-ttu-id="74407-1993">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1993">Class SysAppEntityAttribute</span></span> 
<span data-ttu-id="74407-1994">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-1994">SysAppEntityAttribute used for decorating data contract entities</span></span>

### <a name="methods"></a><span data-ttu-id="74407-1995">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-1995">Methods</span></span>

| <span data-ttu-id="74407-1996">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-1996">Method name</span></span> | <span data-ttu-id="74407-1997">返品</span><span class="sxs-lookup"><span data-stu-id="74407-1997">Returns</span></span> | <span data-ttu-id="74407-1998">説明</span><span class="sxs-lookup"><span data-stu-id="74407-1998">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-1999">新規</span><span class="sxs-lookup"><span data-stu-id="74407-1999">new</span></span> | <span data-ttu-id="74407-2000">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2000">void</span></span> | <span data-ttu-id="74407-2001">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-2001">Constructor</span></span> |
| <span data-ttu-id="74407-2002">名前</span><span class="sxs-lookup"><span data-stu-id="74407-2002">name</span></span> | <span data-ttu-id="74407-2003">str</span><span class="sxs-lookup"><span data-stu-id="74407-2003">str</span></span> | <span data-ttu-id="74407-2004">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2004">Gets the name of the entity</span></span> |
| <span data-ttu-id="74407-2005">entityKey</span><span class="sxs-lookup"><span data-stu-id="74407-2005">entityKey</span></span> | <span data-ttu-id="74407-2006">str</span><span class="sxs-lookup"><span data-stu-id="74407-2006">str</span></span> | <span data-ttu-id="74407-2007">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2007">Gets the entity key</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2008">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2008">Method new</span></span> 
<span data-ttu-id="74407-2009">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-2009">Constructor</span></span>

     public void new (str _name, str _entityKey) 


#### <a name="parameters"></a><span data-ttu-id="74407-2010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2010">Parameters</span></span>

| <span data-ttu-id="74407-2011">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2011">Parameter name</span></span> |  <span data-ttu-id="74407-2012">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2012">Parameter type</span></span> | <span data-ttu-id="74407-2013">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2013">Optional</span></span> | <span data-ttu-id="74407-2014">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2014">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2015">_name</span><span class="sxs-lookup"><span data-stu-id="74407-2015">_name</span></span> | <span data-ttu-id="74407-2016">str</span><span class="sxs-lookup"><span data-stu-id="74407-2016">str</span></span> | <span data-ttu-id="74407-2017">False</span><span class="sxs-lookup"><span data-stu-id="74407-2017">False</span></span> | <span data-ttu-id="74407-2018">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2018">Entity name</span></span>
| <span data-ttu-id="74407-2019">_entityKey</span><span class="sxs-lookup"><span data-stu-id="74407-2019">_entityKey</span></span> | <span data-ttu-id="74407-2020">str</span><span class="sxs-lookup"><span data-stu-id="74407-2020">str</span></span> | <span data-ttu-id="74407-2021">False</span><span class="sxs-lookup"><span data-stu-id="74407-2021">False</span></span> | <span data-ttu-id="74407-2022">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="74407-2022">Name of the entity's key</span></span>


### <a name="method-name"></a><span data-ttu-id="74407-2023">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2023">Method name</span></span> 
<span data-ttu-id="74407-2024">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2024">Gets the name of the entity</span></span>

     public str name () 


#### <a name="return-value"></a><span data-ttu-id="74407-2025">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2025">Return Value</span></span> 
<span data-ttu-id="74407-2026">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="74407-2026">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="74407-2027">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="74407-2027">Method entityKey</span></span> 
<span data-ttu-id="74407-2028">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2028">Gets the entity key</span></span>

     public str entityKey () 


#### <a name="return-value"></a><span data-ttu-id="74407-2029">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2029">Return Value</span></span> 
<span data-ttu-id="74407-2030">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="74407-2030">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="74407-2031">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2031">Class SysAppEntityContext</span></span> 
<span data-ttu-id="74407-2032">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2032">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2033">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2033">Methods</span></span>

| <span data-ttu-id="74407-2034">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2034">Method name</span></span> | <span data-ttu-id="74407-2035">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2035">Returns</span></span> | <span data-ttu-id="74407-2036">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2036">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2037">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="74407-2037">constructFromParams</span></span> | <span data-ttu-id="74407-2038">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2038">SysAppEntityContext</span></span> | <span data-ttu-id="74407-2039">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="74407-2039">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="74407-2040">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="74407-2040">constructFromBuffer</span></span> | <span data-ttu-id="74407-2041">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2041">SysAppEntityContext</span></span> | <span data-ttu-id="74407-2042">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="74407-2042">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="74407-2043">entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2043">entityName</span></span> | <span data-ttu-id="74407-2044">str</span><span class="sxs-lookup"><span data-stu-id="74407-2044">str</span></span> | <span data-ttu-id="74407-2045">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2045">Entity name on which filter applies</span></span> |
| <span data-ttu-id="74407-2046">entityId</span><span class="sxs-lookup"><span data-stu-id="74407-2046">entityId</span></span> | <span data-ttu-id="74407-2047">str</span><span class="sxs-lookup"><span data-stu-id="74407-2047">str</span></span> | <span data-ttu-id="74407-2048">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-2048">Field value on which filter applies</span></span> |


### <a name="method-constructfromparams"></a><span data-ttu-id="74407-2049">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="74407-2049">Method constructFromParams</span></span> 
<span data-ttu-id="74407-2050">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="74407-2050">Constructs SysAppEntityContext from entityName and entityId</span></span>

     public SysAppEntityContext constructFromParams (str _entityName, str _entityId) 


#### <a name="parameters"></a><span data-ttu-id="74407-2051">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2051">Parameters</span></span>

| <span data-ttu-id="74407-2052">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2052">Parameter name</span></span> |  <span data-ttu-id="74407-2053">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2053">Parameter type</span></span> | <span data-ttu-id="74407-2054">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2054">Optional</span></span> | <span data-ttu-id="74407-2055">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2055">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2056">_entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2056">_entityName</span></span> | <span data-ttu-id="74407-2057">str</span><span class="sxs-lookup"><span data-stu-id="74407-2057">str</span></span> | <span data-ttu-id="74407-2058">False</span><span class="sxs-lookup"><span data-stu-id="74407-2058">False</span></span> | <span data-ttu-id="74407-2059">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2059">Entity name</span></span>
| <span data-ttu-id="74407-2060">_entityId</span><span class="sxs-lookup"><span data-stu-id="74407-2060">_entityId</span></span> | <span data-ttu-id="74407-2061">str</span><span class="sxs-lookup"><span data-stu-id="74407-2061">str</span></span> | <span data-ttu-id="74407-2062">False</span><span class="sxs-lookup"><span data-stu-id="74407-2062">False</span></span> | <span data-ttu-id="74407-2063">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="74407-2063">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2064">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2064">Return Value</span></span> 
<span data-ttu-id="74407-2065">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="74407-2065">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="74407-2066">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="74407-2066">Method constructFromBuffer</span></span> 
<span data-ttu-id="74407-2067">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="74407-2067">Constructs SysAppEntityContext from table buffer</span></span>

     public SysAppEntityContext constructFromBuffer (Common _tableBuffer) 


#### <a name="parameters"></a><span data-ttu-id="74407-2068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2068">Parameters</span></span>

| <span data-ttu-id="74407-2069">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2069">Parameter name</span></span> |  <span data-ttu-id="74407-2070">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2070">Parameter type</span></span> | <span data-ttu-id="74407-2071">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2071">Optional</span></span> | <span data-ttu-id="74407-2072">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2072">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2073">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="74407-2073">_tableBuffer</span></span> | <span data-ttu-id="74407-2074">共通</span><span class="sxs-lookup"><span data-stu-id="74407-2074">Common</span></span> | <span data-ttu-id="74407-2075">False</span><span class="sxs-lookup"><span data-stu-id="74407-2075">False</span></span> | <span data-ttu-id="74407-2076">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="74407-2076">table buffer forming the entity</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2077">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2077">Return Value</span></span> 
<span data-ttu-id="74407-2078">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="74407-2078">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="74407-2079">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2079">Method entityName</span></span> 
<span data-ttu-id="74407-2080">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2080">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2081">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2081">Parameters</span></span>

| <span data-ttu-id="74407-2082">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2082">Parameter name</span></span> |  <span data-ttu-id="74407-2083">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2083">Parameter type</span></span> | <span data-ttu-id="74407-2084">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2084">Optional</span></span> | <span data-ttu-id="74407-2085">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2085">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2086">_entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2086">_entityName</span></span> | <span data-ttu-id="74407-2087">str</span><span class="sxs-lookup"><span data-stu-id="74407-2087">str</span></span> | <span data-ttu-id="74407-2088">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2088">True</span></span> | <span data-ttu-id="74407-2089">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2089">Entity name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2090">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2090">Return Value</span></span> 
<span data-ttu-id="74407-2091">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2091">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="74407-2092">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="74407-2092">Method entityId</span></span> 
<span data-ttu-id="74407-2093">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-2093">Field value on which filter applies</span></span>

     public str entityId ([str _entityId]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2094">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2094">Parameters</span></span>

| <span data-ttu-id="74407-2095">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2095">Parameter name</span></span> |  <span data-ttu-id="74407-2096">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2096">Parameter type</span></span> | <span data-ttu-id="74407-2097">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2097">Optional</span></span> | <span data-ttu-id="74407-2098">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2098">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2099">_entityId</span><span class="sxs-lookup"><span data-stu-id="74407-2099">_entityId</span></span> | <span data-ttu-id="74407-2100">str</span><span class="sxs-lookup"><span data-stu-id="74407-2100">str</span></span> | <span data-ttu-id="74407-2101">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2101">True</span></span> | <span data-ttu-id="74407-2102">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="74407-2102">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2103">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2103">Return Value</span></span> 
<span data-ttu-id="74407-2104">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="74407-2104">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="74407-2105">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2105">Class SysAppFieldAttribute</span></span> 
<span data-ttu-id="74407-2106">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2106">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2107">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2107">Methods</span></span>

| <span data-ttu-id="74407-2108">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2108">Method name</span></span> | <span data-ttu-id="74407-2109">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2109">Returns</span></span> | <span data-ttu-id="74407-2110">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2110">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2111">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2111">new</span></span> | <span data-ttu-id="74407-2112">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2112">void</span></span> | <span data-ttu-id="74407-2113">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2113">Creates a new instance of SysAppFieldAttribute class</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2114">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2114">Method new</span></span> 
<span data-ttu-id="74407-2115">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2115">Creates a new instance of SysAppFieldAttribute class</span></span>

     public void new (str _fieldName, str _label) 


#### <a name="parameters"></a><span data-ttu-id="74407-2116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2116">Parameters</span></span>

| <span data-ttu-id="74407-2117">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2117">Parameter name</span></span> |  <span data-ttu-id="74407-2118">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2118">Parameter type</span></span> | <span data-ttu-id="74407-2119">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2119">Optional</span></span> | <span data-ttu-id="74407-2120">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2120">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2121">_fieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2121">_fieldName</span></span> | <span data-ttu-id="74407-2122">str</span><span class="sxs-lookup"><span data-stu-id="74407-2122">str</span></span> | <span data-ttu-id="74407-2123">False</span><span class="sxs-lookup"><span data-stu-id="74407-2123">False</span></span> | <span data-ttu-id="74407-2124">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-2124">Entity field name with which control is bound</span></span>
| <span data-ttu-id="74407-2125">_label</span><span class="sxs-lookup"><span data-stu-id="74407-2125">_label</span></span> | <span data-ttu-id="74407-2126">str</span><span class="sxs-lookup"><span data-stu-id="74407-2126">str</span></span> | <span data-ttu-id="74407-2127">False</span><span class="sxs-lookup"><span data-stu-id="74407-2127">False</span></span> | <span data-ttu-id="74407-2128">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-2128">Control label</span></span>


## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="74407-2129">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="74407-2129">Class SysAppFieldMultiSelectHelper</span></span> 
<span data-ttu-id="74407-2130">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="74407-2130">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2131">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2131">Methods</span></span>

| <span data-ttu-id="74407-2132">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2132">Method name</span></span> | <span data-ttu-id="74407-2133">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2133">Returns</span></span> | <span data-ttu-id="74407-2134">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2134">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2135">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2135">new</span></span> | <span data-ttu-id="74407-2136">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2136">void</span></span> | <span data-ttu-id="74407-2137">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2137">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="74407-2138">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="74407-2138">getSelectedRecIds</span></span> | <span data-ttu-id="74407-2139">コンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-2139">container</span></span> | <span data-ttu-id="74407-2140">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2140">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="74407-2141">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="74407-2141">getSelectedValues</span></span> | <span data-ttu-id="74407-2142">コンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-2142">container</span></span> | <span data-ttu-id="74407-2143">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2143">Returns a container of selected values</span></span> |
| <span data-ttu-id="74407-2144">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="74407-2144">getSelectedRecords</span></span> | <span data-ttu-id="74407-2145">共通</span><span class="sxs-lookup"><span data-stu-id="74407-2145">Common</span></span> | <span data-ttu-id="74407-2146">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2146">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="74407-2147">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="74407-2147">The buffer is marked as temp..</span></span>  <span data-ttu-id="74407-2148">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-2148">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="74407-2149">setControlValue</span><span class="sxs-lookup"><span data-stu-id="74407-2149">setControlValue</span></span> | <span data-ttu-id="74407-2150">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2150">void</span></span> | <span data-ttu-id="74407-2151">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="74407-2151">A setter to set the multi select control value</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2152">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2152">Method new</span></span> 
<span data-ttu-id="74407-2153">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2153">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

     public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl) 


#### <a name="parameters"></a><span data-ttu-id="74407-2154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2154">Parameters</span></span>

| <span data-ttu-id="74407-2155">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2155">Parameter name</span></span> |  <span data-ttu-id="74407-2156">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2156">Parameter type</span></span> | <span data-ttu-id="74407-2157">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2157">Optional</span></span> | <span data-ttu-id="74407-2158">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2158">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2159">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="74407-2159">_multiSelectTableId</span></span> | <span data-ttu-id="74407-2160">TableId</span><span class="sxs-lookup"><span data-stu-id="74407-2160">TableId</span></span> | <span data-ttu-id="74407-2161">False</span><span class="sxs-lookup"><span data-stu-id="74407-2161">False</span></span> | <span data-ttu-id="74407-2162">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="74407-2162">The backing tableId for the field</span></span>
| <span data-ttu-id="74407-2163">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="74407-2163">_valueFieldId</span></span> | <span data-ttu-id="74407-2164">FieldId</span><span class="sxs-lookup"><span data-stu-id="74407-2164">FieldId</span></span> | <span data-ttu-id="74407-2165">False</span><span class="sxs-lookup"><span data-stu-id="74407-2165">False</span></span> | <span data-ttu-id="74407-2166">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="74407-2166">The fieldId for the field which will be shown in the multi select control</span></span>
| <span data-ttu-id="74407-2167">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="74407-2167">_multiSelectControl</span></span> | <span data-ttu-id="74407-2168">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="74407-2168">FormStringControl</span></span> | <span data-ttu-id="74407-2169">False</span><span class="sxs-lookup"><span data-stu-id="74407-2169">False</span></span> | <span data-ttu-id="74407-2170">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="74407-2170">The string control that will be the multi select control</span></span>


### <a name="method-getselectedrecids"></a><span data-ttu-id="74407-2171">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="74407-2171">Method getSelectedRecIds</span></span> 
<span data-ttu-id="74407-2172">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2172">Returns a container of recIds of the records that were selected</span></span>

     public container getSelectedRecIds () 


#### <a name="return-value"></a><span data-ttu-id="74407-2173">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2173">Return Value</span></span> 
<span data-ttu-id="74407-2174">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-2174">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="74407-2175">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="74407-2175">Method getSelectedValues</span></span> 
<span data-ttu-id="74407-2176">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2176">Returns a container of selected values</span></span>

     public container getSelectedValues () 


#### <a name="return-value"></a><span data-ttu-id="74407-2177">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2177">Return Value</span></span> 
<span data-ttu-id="74407-2178">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="74407-2178">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="74407-2179">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="74407-2179">Method getSelectedRecords</span></span> 
<span data-ttu-id="74407-2180">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2180">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="74407-2181">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="74407-2181">The buffer is marked as temp..</span></span>  <span data-ttu-id="74407-2182">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-2182">Later a while-Select can be used to iterate through all the records</span></span>

     public Common getSelectedRecords () 


#### <a name="return-value"></a><span data-ttu-id="74407-2183">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2183">Return Value</span></span> 
<span data-ttu-id="74407-2184">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="74407-2184">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="74407-2185">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="74407-2185">Method setControlValue</span></span> 
<span data-ttu-id="74407-2186">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="74407-2186">A setter to set the multi select control value</span></span>

     public void setControlValue (str _value) 


#### <a name="parameters"></a><span data-ttu-id="74407-2187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2187">Parameters</span></span>

| <span data-ttu-id="74407-2188">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2188">Parameter name</span></span> |  <span data-ttu-id="74407-2189">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2189">Parameter type</span></span> | <span data-ttu-id="74407-2190">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2190">Optional</span></span> | <span data-ttu-id="74407-2191">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2191">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2192">_value</span><span class="sxs-lookup"><span data-stu-id="74407-2192">_value</span></span> | <span data-ttu-id="74407-2193">str</span><span class="sxs-lookup"><span data-stu-id="74407-2193">str</span></span> | <span data-ttu-id="74407-2194">False</span><span class="sxs-lookup"><span data-stu-id="74407-2194">False</span></span> | <span data-ttu-id="74407-2195">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="74407-2195">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>


## <a name="class-sysappfiltercontext"></a><span data-ttu-id="74407-2196">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="74407-2196">Class SysAppFilterContext</span></span> 
<span data-ttu-id="74407-2197">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="74407-2197">SysAppFilterContext class which holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2198">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2198">Methods</span></span>

| <span data-ttu-id="74407-2199">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2199">Method name</span></span> | <span data-ttu-id="74407-2200">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2200">Returns</span></span> | <span data-ttu-id="74407-2201">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2201">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2202">entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2202">entityName</span></span> | <span data-ttu-id="74407-2203">str</span><span class="sxs-lookup"><span data-stu-id="74407-2203">str</span></span> | <span data-ttu-id="74407-2204">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2204">Entity name on which filter applies</span></span> |
| <span data-ttu-id="74407-2205">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2205">filterFieldName</span></span> | <span data-ttu-id="74407-2206">str</span><span class="sxs-lookup"><span data-stu-id="74407-2206">str</span></span> | <span data-ttu-id="74407-2207">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-2207">Field name on which filter applies</span></span> |
| <span data-ttu-id="74407-2208">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="74407-2208">filterFieldValueList</span></span> | <span data-ttu-id="74407-2209">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-2209">List</span></span> | <span data-ttu-id="74407-2210">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2210">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="74407-2211">演算子</span><span class="sxs-lookup"><span data-stu-id="74407-2211">operator</span></span> | <span data-ttu-id="74407-2212">str</span><span class="sxs-lookup"><span data-stu-id="74407-2212">str</span></span> | <span data-ttu-id="74407-2213">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-2213">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="74407-2214">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="74407-2214">addFilterFieldValue</span></span> | <span data-ttu-id="74407-2215">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2215">void</span></span> | <span data-ttu-id="74407-2216">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="74407-2216">Adds filter field value</span></span> |


### <a name="method-entityname"></a><span data-ttu-id="74407-2217">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2217">Method entityName</span></span> 
<span data-ttu-id="74407-2218">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2218">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2219">Parameters</span></span>

| <span data-ttu-id="74407-2220">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2220">Parameter name</span></span> |  <span data-ttu-id="74407-2221">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2221">Parameter type</span></span> | <span data-ttu-id="74407-2222">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2222">Optional</span></span> | <span data-ttu-id="74407-2223">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2223">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2224">_entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2224">_entityName</span></span> | <span data-ttu-id="74407-2225">str</span><span class="sxs-lookup"><span data-stu-id="74407-2225">str</span></span> | <span data-ttu-id="74407-2226">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2226">True</span></span> | <span data-ttu-id="74407-2227">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2227">Entity name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2228">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2228">Return Value</span></span> 
<span data-ttu-id="74407-2229">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2229">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="74407-2230">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2230">Method filterFieldName</span></span> 
<span data-ttu-id="74407-2231">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-2231">Field name on which filter applies</span></span>

     public str filterFieldName ([str _filterFieldName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2232">Parameters</span></span>

| <span data-ttu-id="74407-2233">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2233">Parameter name</span></span> |  <span data-ttu-id="74407-2234">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2234">Parameter type</span></span> | <span data-ttu-id="74407-2235">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2235">Optional</span></span> | <span data-ttu-id="74407-2236">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2236">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2237">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2237">_filterFieldName</span></span> | <span data-ttu-id="74407-2238">str</span><span class="sxs-lookup"><span data-stu-id="74407-2238">str</span></span> | <span data-ttu-id="74407-2239">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2239">True</span></span> | <span data-ttu-id="74407-2240">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-2240">Field name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2241">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2241">Return Value</span></span> 
<span data-ttu-id="74407-2242">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-2242">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="74407-2243">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="74407-2243">Method filterFieldValueList</span></span> 
<span data-ttu-id="74407-2244">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2244">Gets the list of filter field values based on which filter happens</span></span>

     public List filterFieldValueList () 


#### <a name="return-value"></a><span data-ttu-id="74407-2245">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2245">Return Value</span></span> 
<span data-ttu-id="74407-2246">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-2246">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="74407-2247">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="74407-2247">Method operator</span></span> 
<span data-ttu-id="74407-2248">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-2248">Operator based on which result will be fetched</span></span>

     public str operator ([str _operator]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2249">Parameters</span></span>

| <span data-ttu-id="74407-2250">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2250">Parameter name</span></span> |  <span data-ttu-id="74407-2251">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2251">Parameter type</span></span> | <span data-ttu-id="74407-2252">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2252">Optional</span></span> | <span data-ttu-id="74407-2253">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2253">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2254">_operator</span><span class="sxs-lookup"><span data-stu-id="74407-2254">_operator</span></span> | <span data-ttu-id="74407-2255">str</span><span class="sxs-lookup"><span data-stu-id="74407-2255">str</span></span> | <span data-ttu-id="74407-2256">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2256">True</span></span> | <span data-ttu-id="74407-2257">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-2257">Operator based on which result will be fetched</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2258">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2258">Return Value</span></span> 
<span data-ttu-id="74407-2259">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="74407-2259">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="74407-2260">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="74407-2260">Method addFilterFieldValue</span></span> 
<span data-ttu-id="74407-2261">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="74407-2261">Adds filter field value</span></span>

     public void addFilterFieldValue ( _filterFieldValueList) 


#### <a name="parameters"></a><span data-ttu-id="74407-2262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2262">Parameters</span></span>

| <span data-ttu-id="74407-2263">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2263">Parameter name</span></span> |  <span data-ttu-id="74407-2264">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2264">Parameter type</span></span> | <span data-ttu-id="74407-2265">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2265">Optional</span></span> | <span data-ttu-id="74407-2266">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2266">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2267">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="74407-2267">_filterFieldValueList</span></span> |  | <span data-ttu-id="74407-2268">False</span><span class="sxs-lookup"><span data-stu-id="74407-2268">False</span></span> | <span data-ttu-id="74407-2269">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="74407-2269">Filter field values based on which filter happens</span></span>


## <a name="class-sysapplookupattribute"></a><span data-ttu-id="74407-2270">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2270">Class SysAppLookUpAttribute</span></span> 
<span data-ttu-id="74407-2271">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2271">SysAppPageAttribute used for decorating pages that is also lookup page</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2272">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2272">Methods</span></span>

| <span data-ttu-id="74407-2273">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2273">Method name</span></span> | <span data-ttu-id="74407-2274">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2274">Returns</span></span> | <span data-ttu-id="74407-2275">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2275">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2276">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2276">new</span></span> | <span data-ttu-id="74407-2277">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2277">void</span></span> | <span data-ttu-id="74407-2278">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2278">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="74407-2279">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2279">displayFieldName</span></span> | <span data-ttu-id="74407-2280">str</span><span class="sxs-lookup"><span data-stu-id="74407-2280">str</span></span> | <span data-ttu-id="74407-2281">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-2281">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="74407-2282">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2282">valueFieldName</span></span> | <span data-ttu-id="74407-2283">str</span><span class="sxs-lookup"><span data-stu-id="74407-2283">str</span></span> | <span data-ttu-id="74407-2284">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2284">Gets the value field name of lookup control</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2285">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2285">Method new</span></span> 
<span data-ttu-id="74407-2286">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2286">Creates a new instance of SysAppLookUpAttribute class</span></span>

     public void new (str _displayFieldName, str _valueFieldName) 


#### <a name="parameters"></a><span data-ttu-id="74407-2287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2287">Parameters</span></span>

| <span data-ttu-id="74407-2288">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2288">Parameter name</span></span> |  <span data-ttu-id="74407-2289">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2289">Parameter type</span></span> | <span data-ttu-id="74407-2290">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2290">Optional</span></span> | <span data-ttu-id="74407-2291">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2291">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2292">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2292">_displayFieldName</span></span> | <span data-ttu-id="74407-2293">str</span><span class="sxs-lookup"><span data-stu-id="74407-2293">str</span></span> | <span data-ttu-id="74407-2294">False</span><span class="sxs-lookup"><span data-stu-id="74407-2294">False</span></span> | <span data-ttu-id="74407-2295">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="74407-2295">Lookup display field.</span></span> <span data-ttu-id="74407-2296">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="74407-2296">Name of any control of lookup page</span></span>
| <span data-ttu-id="74407-2297">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2297">_valueFieldName</span></span> | <span data-ttu-id="74407-2298">str</span><span class="sxs-lookup"><span data-stu-id="74407-2298">str</span></span> | <span data-ttu-id="74407-2299">False</span><span class="sxs-lookup"><span data-stu-id="74407-2299">False</span></span> | <span data-ttu-id="74407-2300">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="74407-2300">Lookup value field.</span></span> <span data-ttu-id="74407-2301">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="74407-2301">Name of control formed by root data contract constructing lookup page</span></span>


### <a name="method-displayfieldname"></a><span data-ttu-id="74407-2302">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2302">Method displayFieldName</span></span> 
<span data-ttu-id="74407-2303">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="74407-2303">Gets the display field name of lookup control</span></span>

     public str displayFieldName () 


#### <a name="return-value"></a><span data-ttu-id="74407-2304">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2304">Return Value</span></span> 
<span data-ttu-id="74407-2305">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="74407-2305">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="74407-2306">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="74407-2306">Method valueFieldName</span></span> 
<span data-ttu-id="74407-2307">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2307">Gets the value field name of lookup control</span></span>

     public str valueFieldName () 


#### <a name="return-value"></a><span data-ttu-id="74407-2308">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2308">Return Value</span></span> 
<span data-ttu-id="74407-2309">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="74407-2309">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="74407-2310">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2310">Class SysAppLookupFieldAttribute</span></span> 
<span data-ttu-id="74407-2311">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2311">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2312">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2312">Methods</span></span>

| <span data-ttu-id="74407-2313">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2313">Method name</span></span> | <span data-ttu-id="74407-2314">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2314">Returns</span></span> | <span data-ttu-id="74407-2315">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2315">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2316">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2316">new</span></span> | <span data-ttu-id="74407-2317">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2317">void</span></span> | <span data-ttu-id="74407-2318">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2318">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="74407-2319">entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2319">entityName</span></span> | <span data-ttu-id="74407-2320">str</span><span class="sxs-lookup"><span data-stu-id="74407-2320">str</span></span> | <span data-ttu-id="74407-2321">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2321">Gets the name of the entity with which lookup page is related</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2322">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2322">Method new</span></span> 
<span data-ttu-id="74407-2323">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2323">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

     public void new ( _name) 


#### <a name="parameters"></a><span data-ttu-id="74407-2324">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2324">Parameters</span></span>

| <span data-ttu-id="74407-2325">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2325">Parameter name</span></span> |  <span data-ttu-id="74407-2326">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2326">Parameter type</span></span> | <span data-ttu-id="74407-2327">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2327">Optional</span></span> | <span data-ttu-id="74407-2328">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2328">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2329">_name</span><span class="sxs-lookup"><span data-stu-id="74407-2329">_name</span></span> |  | <span data-ttu-id="74407-2330">False</span><span class="sxs-lookup"><span data-stu-id="74407-2330">False</span></span> | <span data-ttu-id="74407-2331">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="74407-2331">Name of the entity with which lookup page is related</span></span>


### <a name="method-entityname"></a><span data-ttu-id="74407-2332">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="74407-2332">Method entityName</span></span> 
<span data-ttu-id="74407-2333">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2333">Gets the name of the entity with which lookup page is related</span></span>

     public str entityName () 


#### <a name="return-value"></a><span data-ttu-id="74407-2334">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2334">Return Value</span></span> 
<span data-ttu-id="74407-2335">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="74407-2335">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="74407-2336">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2336">Class SysAppPageAttribute</span></span> 
<span data-ttu-id="74407-2337">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2337">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2338">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2338">Methods</span></span>

| <span data-ttu-id="74407-2339">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2339">Method name</span></span> | <span data-ttu-id="74407-2340">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2340">Returns</span></span> | <span data-ttu-id="74407-2341">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2341">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2342">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2342">new</span></span> | <span data-ttu-id="74407-2343">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2343">void</span></span> | <span data-ttu-id="74407-2344">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2344">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="74407-2345">pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-2345">pageTitle</span></span> | <span data-ttu-id="74407-2346">str</span><span class="sxs-lookup"><span data-stu-id="74407-2346">str</span></span> | <span data-ttu-id="74407-2347">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2347">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="74407-2348">pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-2348">pageDescription</span></span> | <span data-ttu-id="74407-2349">str</span><span class="sxs-lookup"><span data-stu-id="74407-2349">str</span></span> | <span data-ttu-id="74407-2350">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2350">Gets the Page Description</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2351">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2351">Method new</span></span> 
<span data-ttu-id="74407-2352">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2352">Creates a new instance of SysAppPageAttribute class</span></span>

     public void new ([str _pageTitle], [str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2353">Parameters</span></span>

| <span data-ttu-id="74407-2354">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2354">Parameter name</span></span> |  <span data-ttu-id="74407-2355">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2355">Parameter type</span></span> | <span data-ttu-id="74407-2356">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2356">Optional</span></span> | <span data-ttu-id="74407-2357">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2357">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2358">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-2358">_pageTitle</span></span> | <span data-ttu-id="74407-2359">str</span><span class="sxs-lookup"><span data-stu-id="74407-2359">str</span></span> | <span data-ttu-id="74407-2360">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2360">True</span></span> | <span data-ttu-id="74407-2361">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-2361">The page title</span></span>
| <span data-ttu-id="74407-2362">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-2362">_pageDescription</span></span> | <span data-ttu-id="74407-2363">str</span><span class="sxs-lookup"><span data-stu-id="74407-2363">str</span></span> | <span data-ttu-id="74407-2364">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2364">True</span></span> | <span data-ttu-id="74407-2365">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-2365">The page description</span></span>


### <a name="method-pagetitle"></a><span data-ttu-id="74407-2366">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-2366">Method pageTitle</span></span> 
<span data-ttu-id="74407-2367">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2367">Gets the Page Title of the page</span></span>

     public str pageTitle () 


#### <a name="return-value"></a><span data-ttu-id="74407-2368">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2368">Return Value</span></span> 
<span data-ttu-id="74407-2369">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-2369">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="74407-2370">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-2370">Method pageDescription</span></span> 
<span data-ttu-id="74407-2371">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2371">Gets the Page Description</span></span>

     public str pageDescription () 


#### <a name="return-value"></a><span data-ttu-id="74407-2372">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2372">Return Value</span></span> 
<span data-ttu-id="74407-2373">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-2373">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="74407-2374">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2374">Class SysAppPageMetadata</span></span> 
<span data-ttu-id="74407-2375">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="74407-2375">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2376">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2376">Methods</span></span>

| <span data-ttu-id="74407-2377">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2377">Method name</span></span> | <span data-ttu-id="74407-2378">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2378">Returns</span></span> | <span data-ttu-id="74407-2379">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2379">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2380">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2380">new</span></span> | <span data-ttu-id="74407-2381">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2381">void</span></span> |  |
| <span data-ttu-id="74407-2382">getPageName</span><span class="sxs-lookup"><span data-stu-id="74407-2382">getPageName</span></span> | <span data-ttu-id="74407-2383">str</span><span class="sxs-lookup"><span data-stu-id="74407-2383">str</span></span> | <span data-ttu-id="74407-2384">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2384">Returns the page name</span></span> |
| <span data-ttu-id="74407-2385">pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-2385">pageTitle</span></span> | <span data-ttu-id="74407-2386">str</span><span class="sxs-lookup"><span data-stu-id="74407-2386">str</span></span> | <span data-ttu-id="74407-2387">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-2387">Gets and sets the page title</span></span> |
| <span data-ttu-id="74407-2388">pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-2388">pageDescription</span></span> | <span data-ttu-id="74407-2389">str</span><span class="sxs-lookup"><span data-stu-id="74407-2389">str</span></span> | <span data-ttu-id="74407-2390">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2390">Gets or sets the page description</span></span> |
| <span data-ttu-id="74407-2391">pageHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2391">pageHidden</span></span> | <span data-ttu-id="74407-2392">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2392">boolean</span></span> | <span data-ttu-id="74407-2393">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-2393">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="74407-2394">pageOrder</span><span class="sxs-lookup"><span data-stu-id="74407-2394">pageOrder</span></span> | <span data-ttu-id="74407-2395">int</span><span class="sxs-lookup"><span data-stu-id="74407-2395">int</span></span> | <span data-ttu-id="74407-2396">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2396">Gets or sets the page order</span></span> |
| <span data-ttu-id="74407-2397">getControl</span><span class="sxs-lookup"><span data-stu-id="74407-2397">getControl</span></span> | <span data-ttu-id="74407-2398">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2398">SysAppControlMetadata</span></span> | <span data-ttu-id="74407-2399">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2399">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="74407-2400">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2400">getControlEnumerator</span></span> | <span data-ttu-id="74407-2401">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2401">MapEnumerator</span></span> | <span data-ttu-id="74407-2402">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2402">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="74407-2403">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-2403">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2404">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2404">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata) 


#### <a name="parameters"></a><span data-ttu-id="74407-2405">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2405">Parameters</span></span>

| <span data-ttu-id="74407-2406">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2406">Parameter name</span></span> |  <span data-ttu-id="74407-2407">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2407">Parameter type</span></span> | <span data-ttu-id="74407-2408">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2408">Optional</span></span> | <span data-ttu-id="74407-2409">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2409">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2410">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2410">_pageMetadata</span></span> | <span data-ttu-id="74407-2411">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2411">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="74407-2412">False</span><span class="sxs-lookup"><span data-stu-id="74407-2412">False</span></span> | 


### <a name="method-getpagename"></a><span data-ttu-id="74407-2413">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="74407-2413">Method getPageName</span></span> 
<span data-ttu-id="74407-2414">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2414">Returns the page name</span></span>

     public str getPageName () 


#### <a name="return-value"></a><span data-ttu-id="74407-2415">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2415">Return Value</span></span> 
<span data-ttu-id="74407-2416">ページ名</span><span class="sxs-lookup"><span data-stu-id="74407-2416">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="74407-2417">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-2417">Method pageTitle</span></span> 
<span data-ttu-id="74407-2418">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-2418">Gets and sets the page title</span></span>

     public str pageTitle ([str _pageTitle]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2419">Parameters</span></span>

| <span data-ttu-id="74407-2420">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2420">Parameter name</span></span> |  <span data-ttu-id="74407-2421">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2421">Parameter type</span></span> | <span data-ttu-id="74407-2422">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2422">Optional</span></span> | <span data-ttu-id="74407-2423">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2423">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2424">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="74407-2424">_pageTitle</span></span> | <span data-ttu-id="74407-2425">str</span><span class="sxs-lookup"><span data-stu-id="74407-2425">str</span></span> | <span data-ttu-id="74407-2426">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2426">True</span></span> | <span data-ttu-id="74407-2427">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-2427">The page title</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2428">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2428">Return Value</span></span> 
<span data-ttu-id="74407-2429">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="74407-2429">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="74407-2430">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-2430">Method pageDescription</span></span> 
<span data-ttu-id="74407-2431">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2431">Gets or sets the page description</span></span>

     public str pageDescription ([str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2432">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2432">Parameters</span></span>

| <span data-ttu-id="74407-2433">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2433">Parameter name</span></span> |  <span data-ttu-id="74407-2434">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2434">Parameter type</span></span> | <span data-ttu-id="74407-2435">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2435">Optional</span></span> | <span data-ttu-id="74407-2436">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2436">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2437">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="74407-2437">_pageDescription</span></span> | <span data-ttu-id="74407-2438">str</span><span class="sxs-lookup"><span data-stu-id="74407-2438">str</span></span> | <span data-ttu-id="74407-2439">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2439">True</span></span> | <span data-ttu-id="74407-2440">ページの説明</span><span class="sxs-lookup"><span data-stu-id="74407-2440">The page description</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2441">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2441">Return Value</span></span> 
<span data-ttu-id="74407-2442">ページの説明></span><span class="sxs-lookup"><span data-stu-id="74407-2442">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="74407-2443">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2443">Method pageHidden</span></span> 
<span data-ttu-id="74407-2444">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-2444">Gets and sets whether the page is hidden in the workspace</span></span>

     public boolean pageHidden ([boolean _pageHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2445">Parameters</span></span>

| <span data-ttu-id="74407-2446">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2446">Parameter name</span></span> |  <span data-ttu-id="74407-2447">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2447">Parameter type</span></span> | <span data-ttu-id="74407-2448">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2448">Optional</span></span> | <span data-ttu-id="74407-2449">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2449">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2450">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2450">_pageHidden</span></span> | <span data-ttu-id="74407-2451">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2451">boolean</span></span> | <span data-ttu-id="74407-2452">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2452">True</span></span> | <span data-ttu-id="74407-2453">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="74407-2453">page hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2454">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2454">Return Value</span></span> 
<span data-ttu-id="74407-2455">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="74407-2455">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="74407-2456">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="74407-2456">Method pageOrder</span></span> 
<span data-ttu-id="74407-2457">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2457">Gets or sets the page order</span></span>

     public int pageOrder ([int _pageOrder]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2458">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2458">Parameters</span></span>

| <span data-ttu-id="74407-2459">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2459">Parameter name</span></span> |  <span data-ttu-id="74407-2460">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2460">Parameter type</span></span> | <span data-ttu-id="74407-2461">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2461">Optional</span></span> | <span data-ttu-id="74407-2462">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2462">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2463">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="74407-2463">_pageOrder</span></span> | <span data-ttu-id="74407-2464">int</span><span class="sxs-lookup"><span data-stu-id="74407-2464">int</span></span> | <span data-ttu-id="74407-2465">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2465">True</span></span> | <span data-ttu-id="74407-2466">ページの順序</span><span class="sxs-lookup"><span data-stu-id="74407-2466">The page order</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2467">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2467">Return Value</span></span> 
<span data-ttu-id="74407-2468">ページの順序</span><span class="sxs-lookup"><span data-stu-id="74407-2468">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="74407-2469">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="74407-2469">Method getControl</span></span> 
<span data-ttu-id="74407-2470">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2470">Returns the control on the current page having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="74407-2471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2471">Parameters</span></span>

| <span data-ttu-id="74407-2472">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2472">Parameter name</span></span> |  <span data-ttu-id="74407-2473">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2473">Parameter type</span></span> | <span data-ttu-id="74407-2474">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2474">Optional</span></span> | <span data-ttu-id="74407-2475">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2475">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2476">_controlName</span><span class="sxs-lookup"><span data-stu-id="74407-2476">_controlName</span></span> | <span data-ttu-id="74407-2477">str</span><span class="sxs-lookup"><span data-stu-id="74407-2477">str</span></span> | <span data-ttu-id="74407-2478">False</span><span class="sxs-lookup"><span data-stu-id="74407-2478">False</span></span> | <span data-ttu-id="74407-2479">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="74407-2479">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2480">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2480">Return Value</span></span> 
<span data-ttu-id="74407-2481">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="74407-2481">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="74407-2482">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2482">Method getControlEnumerator</span></span> 
<span data-ttu-id="74407-2483">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2483">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="74407-2484">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-2484">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-2485">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2485">Return Value</span></span> 
<span data-ttu-id="74407-2486">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-2486">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="74407-2487">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2487">Class SysAppProjectionAttribute</span></span> 
<span data-ttu-id="74407-2488">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2488">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2489">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2489">Methods</span></span>

| <span data-ttu-id="74407-2490">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2490">Method name</span></span> | <span data-ttu-id="74407-2491">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2491">Returns</span></span> | <span data-ttu-id="74407-2492">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2492">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2493">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2493">new</span></span> | <span data-ttu-id="74407-2494">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2494">void</span></span> | <span data-ttu-id="74407-2495">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2495">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2496">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2496">Method new</span></span> 
<span data-ttu-id="74407-2497">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2497">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

     public void new (str _label) 


#### <a name="parameters"></a><span data-ttu-id="74407-2498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2498">Parameters</span></span>

| <span data-ttu-id="74407-2499">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2499">Parameter name</span></span> |  <span data-ttu-id="74407-2500">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2500">Parameter type</span></span> | <span data-ttu-id="74407-2501">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2501">Optional</span></span> | <span data-ttu-id="74407-2502">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2502">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2503">_label</span><span class="sxs-lookup"><span data-stu-id="74407-2503">_label</span></span> | <span data-ttu-id="74407-2504">str</span><span class="sxs-lookup"><span data-stu-id="74407-2504">str</span></span> | <span data-ttu-id="74407-2505">False</span><span class="sxs-lookup"><span data-stu-id="74407-2505">False</span></span> | <span data-ttu-id="74407-2506">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="74407-2506">Control label</span></span>


## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="74407-2507">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2507">Class SysAppRelationalAttribute</span></span> 
<span data-ttu-id="74407-2508">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2508">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2509">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2509">Methods</span></span>

| <span data-ttu-id="74407-2510">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2510">Method name</span></span> | <span data-ttu-id="74407-2511">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2511">Returns</span></span> | <span data-ttu-id="74407-2512">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2512">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2513">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2513">new</span></span> | <span data-ttu-id="74407-2514">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2514">void</span></span> | <span data-ttu-id="74407-2515">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-2515">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2516">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2516">Method new</span></span> 
<span data-ttu-id="74407-2517">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="74407-2517">Constructor</span></span>

     public void new ([str _name]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2518">Parameters</span></span>

| <span data-ttu-id="74407-2519">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2519">Parameter name</span></span> |  <span data-ttu-id="74407-2520">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2520">Parameter type</span></span> | <span data-ttu-id="74407-2521">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2521">Optional</span></span> | <span data-ttu-id="74407-2522">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2522">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2523">_name</span><span class="sxs-lookup"><span data-stu-id="74407-2523">_name</span></span> | <span data-ttu-id="74407-2524">str</span><span class="sxs-lookup"><span data-stu-id="74407-2524">str</span></span> | <span data-ttu-id="74407-2525">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2525">True</span></span> | <span data-ttu-id="74407-2526">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="74407-2526">Property name of the referenced entity</span></span>


## <a name="class-sysapprequestparams"></a><span data-ttu-id="74407-2527">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="74407-2527">Class SysAppRequestParams</span></span> 
<span data-ttu-id="74407-2528">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="74407-2528">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2529">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2529">Methods</span></span>

| <span data-ttu-id="74407-2530">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2530">Method name</span></span> | <span data-ttu-id="74407-2531">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2531">Returns</span></span> | <span data-ttu-id="74407-2532">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2532">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2533">entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2533">entityContext</span></span> | <span data-ttu-id="74407-2534">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2534">SysAppEntityContext</span></span> | <span data-ttu-id="74407-2535">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2535">Entity context of the request</span></span> |
| <span data-ttu-id="74407-2536">filterContext</span><span class="sxs-lookup"><span data-stu-id="74407-2536">filterContext</span></span> | <span data-ttu-id="74407-2537">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-2537">List</span></span> | <span data-ttu-id="74407-2538">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-2538">List of SysAppFilterContext for filter contexts</span></span> |


### <a name="method-entitycontext"></a><span data-ttu-id="74407-2539">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2539">Method entityContext</span></span> 
<span data-ttu-id="74407-2540">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2540">Entity context of the request</span></span>

     public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2541">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2541">Parameters</span></span>

| <span data-ttu-id="74407-2542">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2542">Parameter name</span></span> |  <span data-ttu-id="74407-2543">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2543">Parameter type</span></span> | <span data-ttu-id="74407-2544">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2544">Optional</span></span> | <span data-ttu-id="74407-2545">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2545">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2546">_entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2546">_entityContext</span></span> | <span data-ttu-id="74407-2547">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2547">SysAppEntityContext</span></span> | <span data-ttu-id="74407-2548">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2548">True</span></span> | <span data-ttu-id="74407-2549">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2549">Entity context of the request</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2550">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2550">Return Value</span></span> 
<span data-ttu-id="74407-2551">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2551">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="74407-2552">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="74407-2552">Method filterContext</span></span> 
<span data-ttu-id="74407-2553">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-2553">List of SysAppFilterContext for filter contexts</span></span>

     public List filterContext ([List _filterContext]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2554">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2554">Parameters</span></span>

| <span data-ttu-id="74407-2555">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2555">Parameter name</span></span> |  <span data-ttu-id="74407-2556">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2556">Parameter type</span></span> | <span data-ttu-id="74407-2557">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2557">Optional</span></span> | <span data-ttu-id="74407-2558">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2558">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2559">_filterContext</span><span class="sxs-lookup"><span data-stu-id="74407-2559">_filterContext</span></span> | <span data-ttu-id="74407-2560">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-2560">List</span></span> | <span data-ttu-id="74407-2561">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2561">True</span></span> | <span data-ttu-id="74407-2562">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-2562">List of SysAppFilterContext for filter contexts of page</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2563">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2563">Return Value</span></span> 
<span data-ttu-id="74407-2564">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="74407-2564">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="74407-2565">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="74407-2565">Class SysAppResponse</span></span> 
<span data-ttu-id="74407-2566">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="74407-2566">SysAppResponse class.</span></span>  <span data-ttu-id="74407-2567">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="74407-2567">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2568">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2568">Methods</span></span>

| <span data-ttu-id="74407-2569">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2569">Method name</span></span> | <span data-ttu-id="74407-2570">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2570">Returns</span></span> | <span data-ttu-id="74407-2571">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2571">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2572">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2572">new</span></span> | <span data-ttu-id="74407-2573">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2573">void</span></span> |  |
| <span data-ttu-id="74407-2574">jobId</span><span class="sxs-lookup"><span data-stu-id="74407-2574">jobId</span></span> | <span data-ttu-id="74407-2575">str</span><span class="sxs-lookup"><span data-stu-id="74407-2575">str</span></span> | <span data-ttu-id="74407-2576">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-2576">Job Id of the request</span></span> |
| <span data-ttu-id="74407-2577">データ</span><span class="sxs-lookup"><span data-stu-id="74407-2577">data</span></span> | <span data-ttu-id="74407-2578">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="74407-2578">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="74407-2579">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-2579">Data of the page</span></span> |
| <span data-ttu-id="74407-2580">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="74407-2580">failedInAppCall</span></span> | <span data-ttu-id="74407-2581">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2581">boolean</span></span> | <span data-ttu-id="74407-2582">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-2582">Data of the page</span></span> |
| <span data-ttu-id="74407-2583">commits</span><span class="sxs-lookup"><span data-stu-id="74407-2583">commits</span></span> | <span data-ttu-id="74407-2584">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-2584">List</span></span> | <span data-ttu-id="74407-2585">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="74407-2585">Commits after task is completed</span></span> |
| <span data-ttu-id="74407-2586">メッセージ</span><span class="sxs-lookup"><span data-stu-id="74407-2586">messages</span></span> | <span data-ttu-id="74407-2587">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-2587">List</span></span> | <span data-ttu-id="74407-2588">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-2588">Job Id of the request</span></span> |
| <span data-ttu-id="74407-2589">addMessage</span><span class="sxs-lookup"><span data-stu-id="74407-2589">addMessage</span></span> | <span data-ttu-id="74407-2590">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2590">void</span></span> | <span data-ttu-id="74407-2591">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="74407-2591">Adds message</span></span> |
| <span data-ttu-id="74407-2592">addCommit</span><span class="sxs-lookup"><span data-stu-id="74407-2592">addCommit</span></span> | <span data-ttu-id="74407-2593">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2593">void</span></span> | <span data-ttu-id="74407-2594">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="74407-2594">Adds commits</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2595">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2595">Method new</span></span> 


     public void new () 


### <a name="method-jobid"></a><span data-ttu-id="74407-2596">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="74407-2596">Method jobId</span></span> 
<span data-ttu-id="74407-2597">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-2597">Job Id of the request</span></span>

     public str jobId () 


#### <a name="return-value"></a><span data-ttu-id="74407-2598">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2598">Return Value</span></span> 
<span data-ttu-id="74407-2599">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-2599">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="74407-2600">メソッド data</span><span class="sxs-lookup"><span data-stu-id="74407-2600">Method data</span></span> 
<span data-ttu-id="74407-2601">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-2601">Data of the page</span></span>

     public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2602">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2602">Parameters</span></span>

| <span data-ttu-id="74407-2603">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2603">Parameter name</span></span> |  <span data-ttu-id="74407-2604">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2604">Parameter type</span></span> | <span data-ttu-id="74407-2605">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2605">Optional</span></span> | <span data-ttu-id="74407-2606">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2606">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2607">_data</span><span class="sxs-lookup"><span data-stu-id="74407-2607">_data</span></span> | <span data-ttu-id="74407-2608">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="74407-2608">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="74407-2609">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2609">True</span></span> | <span data-ttu-id="74407-2610">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-2610">Data of the page</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2611">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2611">Return Value</span></span> 
<span data-ttu-id="74407-2612">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-2612">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="74407-2613">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="74407-2613">Method failedInAppCall</span></span> 
<span data-ttu-id="74407-2614">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="74407-2614">Data of the page</span></span>

     public boolean failedInAppCall ([boolean _failedInAppCall]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2615">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2615">Parameters</span></span>

| <span data-ttu-id="74407-2616">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2616">Parameter name</span></span> |  <span data-ttu-id="74407-2617">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2617">Parameter type</span></span> | <span data-ttu-id="74407-2618">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2618">Optional</span></span> | <span data-ttu-id="74407-2619">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2619">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2620">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="74407-2620">_failedInAppCall</span></span> | <span data-ttu-id="74407-2621">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2621">boolean</span></span> | <span data-ttu-id="74407-2622">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2622">True</span></span> | <span data-ttu-id="74407-2623">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="74407-2623">Sets to true if it fails in calling application code</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2624">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2624">Return Value</span></span> 
<span data-ttu-id="74407-2625">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="74407-2625">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="74407-2626">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="74407-2626">Method commits</span></span> 
<span data-ttu-id="74407-2627">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="74407-2627">Commits after task is completed</span></span>

     public List commits () 


#### <a name="return-value"></a><span data-ttu-id="74407-2628">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2628">Return Value</span></span> 
<span data-ttu-id="74407-2629">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="74407-2629">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="74407-2630">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="74407-2630">Method messages</span></span> 
<span data-ttu-id="74407-2631">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="74407-2631">Job Id of the request</span></span>

     public List messages () 


#### <a name="return-value"></a><span data-ttu-id="74407-2632">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2632">Return Value</span></span> 
<span data-ttu-id="74407-2633">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="74407-2633">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="74407-2634">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="74407-2634">Method addMessage</span></span> 
<span data-ttu-id="74407-2635">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="74407-2635">Adds message</span></span>

     public void addMessage (SysAppResponseMessage _message) 


#### <a name="parameters"></a><span data-ttu-id="74407-2636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2636">Parameters</span></span>

| <span data-ttu-id="74407-2637">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2637">Parameter name</span></span> |  <span data-ttu-id="74407-2638">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2638">Parameter type</span></span> | <span data-ttu-id="74407-2639">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2639">Optional</span></span> | <span data-ttu-id="74407-2640">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2640">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2641">_message</span><span class="sxs-lookup"><span data-stu-id="74407-2641">_message</span></span> | <span data-ttu-id="74407-2642">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="74407-2642">SysAppResponseMessage</span></span> | <span data-ttu-id="74407-2643">False</span><span class="sxs-lookup"><span data-stu-id="74407-2643">False</span></span> | <span data-ttu-id="74407-2644">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="74407-2644">message as SysAppResponseMessage object</span></span>


### <a name="method-addcommit"></a><span data-ttu-id="74407-2645">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="74407-2645">Method addCommit</span></span> 
<span data-ttu-id="74407-2646">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="74407-2646">Adds commits</span></span>

     public void addCommit (SysAppEntityContext _entityContext) 


#### <a name="parameters"></a><span data-ttu-id="74407-2647">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2647">Parameters</span></span>

| <span data-ttu-id="74407-2648">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2648">Parameter name</span></span> |  <span data-ttu-id="74407-2649">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2649">Parameter type</span></span> | <span data-ttu-id="74407-2650">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2650">Optional</span></span> | <span data-ttu-id="74407-2651">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2651">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2652">_entityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2652">_entityContext</span></span> | <span data-ttu-id="74407-2653">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="74407-2653">SysAppEntityContext</span></span> | <span data-ttu-id="74407-2654">False</span><span class="sxs-lookup"><span data-stu-id="74407-2654">False</span></span> | <span data-ttu-id="74407-2655">確定済のエンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2655">Entity context containing entity name and entity id of the entity that is committed</span></span>


## <a name="class-sysappresponsemessage"></a><span data-ttu-id="74407-2656">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="74407-2656">Class SysAppResponseMessage</span></span> 
<span data-ttu-id="74407-2657">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="74407-2657">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2658">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2658">Methods</span></span>

| <span data-ttu-id="74407-2659">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2659">Method name</span></span> | <span data-ttu-id="74407-2660">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2660">Returns</span></span> | <span data-ttu-id="74407-2661">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2661">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2662">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2662">new</span></span> | <span data-ttu-id="74407-2663">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2663">void</span></span> | <span data-ttu-id="74407-2664">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2664">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="74407-2665">テキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2665">text</span></span> | <span data-ttu-id="74407-2666">str</span><span class="sxs-lookup"><span data-stu-id="74407-2666">str</span></span> | <span data-ttu-id="74407-2667">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2667">Gets the message text</span></span> |
| <span data-ttu-id="74407-2668">タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2668">type</span></span> | <span data-ttu-id="74407-2669">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="74407-2669">SysAppMessageType</span></span> | <span data-ttu-id="74407-2670">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-2670">Gets the message type: info, error , warning</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2671">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2671">Method new</span></span> 
<span data-ttu-id="74407-2672">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2672">Creates a new instance of SysAppResponseMessage class</span></span>

     public void new (str _text, [SysAppMessageType _type]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2673">Parameters</span></span>

| <span data-ttu-id="74407-2674">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2674">Parameter name</span></span> |  <span data-ttu-id="74407-2675">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2675">Parameter type</span></span> | <span data-ttu-id="74407-2676">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2676">Optional</span></span> | <span data-ttu-id="74407-2677">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2677">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2678">_text</span><span class="sxs-lookup"><span data-stu-id="74407-2678">_text</span></span> | <span data-ttu-id="74407-2679">str</span><span class="sxs-lookup"><span data-stu-id="74407-2679">str</span></span> | <span data-ttu-id="74407-2680">False</span><span class="sxs-lookup"><span data-stu-id="74407-2680">False</span></span> | <span data-ttu-id="74407-2681">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2681">The message text</span></span>
| <span data-ttu-id="74407-2682">_type</span><span class="sxs-lookup"><span data-stu-id="74407-2682">_type</span></span> | <span data-ttu-id="74407-2683">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="74407-2683">SysAppMessageType</span></span> | <span data-ttu-id="74407-2684">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2684">True</span></span> | <span data-ttu-id="74407-2685">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-2685">Message Type: info, error , warning</span></span>


### <a name="method-text"></a><span data-ttu-id="74407-2686">メソッド text</span><span class="sxs-lookup"><span data-stu-id="74407-2686">Method text</span></span> 
<span data-ttu-id="74407-2687">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2687">Gets the message text</span></span>

     public str text () 


#### <a name="return-value"></a><span data-ttu-id="74407-2688">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2688">Return Value</span></span> 
<span data-ttu-id="74407-2689">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="74407-2689">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="74407-2690">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2690">Method type</span></span> 
<span data-ttu-id="74407-2691">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-2691">Gets the message type: info, error , warning</span></span>

     public SysAppMessageType type () 


#### <a name="return-value"></a><span data-ttu-id="74407-2692">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2692">Return Value</span></span> 
<span data-ttu-id="74407-2693">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="74407-2693">The message type: info, error , warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="74407-2694">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2694">Class SysAppSecurityAttribute</span></span> 
<span data-ttu-id="74407-2695">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="74407-2695">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="74407-2696">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="74407-2696">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2697">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2697">Methods</span></span>

| <span data-ttu-id="74407-2698">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2698">Method name</span></span> | <span data-ttu-id="74407-2699">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2699">Returns</span></span> | <span data-ttu-id="74407-2700">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2700">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2701">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2701">new</span></span> | <span data-ttu-id="74407-2702">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2702">void</span></span> | <span data-ttu-id="74407-2703">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="74407-2703">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="74407-2704">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="74407-2704">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="74407-2705">menuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-2705">menuItemType</span></span> | <span data-ttu-id="74407-2706">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-2706">MenuItemType</span></span> | <span data-ttu-id="74407-2707">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2707">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="74407-2708">menuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-2708">menuItemName</span></span> | <span data-ttu-id="74407-2709">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-2709">MenuItemName</span></span> | <span data-ttu-id="74407-2710">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2710">Gets the Menu Item Name of the page</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2711">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2711">Method new</span></span> 
<span data-ttu-id="74407-2712">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="74407-2712">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="74407-2713">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="74407-2713">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

     public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2714">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2714">Parameters</span></span>

| <span data-ttu-id="74407-2715">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2715">Parameter name</span></span> |  <span data-ttu-id="74407-2716">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2716">Parameter type</span></span> | <span data-ttu-id="74407-2717">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2717">Optional</span></span> | <span data-ttu-id="74407-2718">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2718">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2719">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-2719">_menuItemName</span></span> | <span data-ttu-id="74407-2720">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-2720">MenuItemName</span></span> | <span data-ttu-id="74407-2721">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2721">True</span></span> | <span data-ttu-id="74407-2722">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="74407-2722">Menu Item Name of the page</span></span>
| <span data-ttu-id="74407-2723">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-2723">_menuItemType</span></span> | <span data-ttu-id="74407-2724">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-2724">MenuItemType</span></span> | <span data-ttu-id="74407-2725">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2725">True</span></span> | <span data-ttu-id="74407-2726">アクション、表示または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2726">Menu Item Type of the page like action, display or output</span></span>


### <a name="method-menuitemtype"></a><span data-ttu-id="74407-2727">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-2727">Method menuItemType</span></span> 
<span data-ttu-id="74407-2728">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="74407-2728">Gets the Menu Item Type of the page</span></span>

     public MenuItemType menuItemType () 


#### <a name="return-value"></a><span data-ttu-id="74407-2729">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2729">Return Value</span></span> 
<span data-ttu-id="74407-2730">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2730">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="74407-2731">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-2731">Method menuItemName</span></span> 
<span data-ttu-id="74407-2732">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="74407-2732">Gets the Menu Item Name of the page</span></span>

     public MenuItemName menuItemName () 


#### <a name="return-value"></a><span data-ttu-id="74407-2733">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2733">Return Value</span></span> 
<span data-ttu-id="74407-2734">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="74407-2734">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="74407-2735">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="74407-2735">Class SysAppWorkspace</span></span> 
<span data-ttu-id="74407-2736">これは、AX モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="74407-2736">This is the base class of AX mobile workspace.</span></span> <span data-ttu-id="74407-2737">AX モバイル ワークスペース クラスは、このクラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74407-2737">AX mobile workspace classes needs to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2738">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2738">Methods</span></span>

| <span data-ttu-id="74407-2739">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2739">Method name</span></span> | <span data-ttu-id="74407-2740">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2740">Returns</span></span> | <span data-ttu-id="74407-2741">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2741">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2742">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="74407-2742">getEnumValues</span></span> | <span data-ttu-id="74407-2743">リスト</span><span class="sxs-lookup"><span data-stu-id="74407-2743">List</span></span> | <span data-ttu-id="74407-2744">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-2744">Called during workspace initialization.</span></span> <span data-ttu-id="74407-2745">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-2745">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="74407-2746">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2746">getWorkspaceMetadata</span></span> | <span data-ttu-id="74407-2747">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2747">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="74407-2748">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-2748">Called during workspace initialization.</span></span> <span data-ttu-id="74407-2749">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-2749">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="74407-2750">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-2750">onBeginAppJob</span></span> | <span data-ttu-id="74407-2751">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2751">void</span></span> | <span data-ttu-id="74407-2752">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-2752">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="74407-2753">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-2753">onEndAppJob</span></span> | <span data-ttu-id="74407-2754">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2754">void</span></span> | <span data-ttu-id="74407-2755">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-2755">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="74407-2756">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2756">workspaceHidden</span></span> | <span data-ttu-id="74407-2757">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2757">boolean</span></span> | <span data-ttu-id="74407-2758">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="74407-2758">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="74407-2759">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74407-2759">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="74407-2760">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2760">If the attribute is not specified on the class than it always returns false</span></span> |


### <a name="method-getenumvalues"></a><span data-ttu-id="74407-2761">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="74407-2761">Method getEnumValues</span></span> 
<span data-ttu-id="74407-2762">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-2762">Called during workspace initialization.</span></span> <span data-ttu-id="74407-2763">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-2763">Can be used to modify the enum values that are returned to AX mobile</span></span>

     public List getEnumValues (EnumName _enumName) 


#### <a name="parameters"></a><span data-ttu-id="74407-2764">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2764">Parameters</span></span>

| <span data-ttu-id="74407-2765">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2765">Parameter name</span></span> |  <span data-ttu-id="74407-2766">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2766">Parameter type</span></span> | <span data-ttu-id="74407-2767">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2767">Optional</span></span> | <span data-ttu-id="74407-2768">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2768">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2769">_enumName</span><span class="sxs-lookup"><span data-stu-id="74407-2769">_enumName</span></span> | <span data-ttu-id="74407-2770">EnumName</span><span class="sxs-lookup"><span data-stu-id="74407-2770">EnumName</span></span> | <span data-ttu-id="74407-2771">False</span><span class="sxs-lookup"><span data-stu-id="74407-2771">False</span></span> | <span data-ttu-id="74407-2772">列挙名</span><span class="sxs-lookup"><span data-stu-id="74407-2772">The enum name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2773">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2773">Return Value</span></span> 
<span data-ttu-id="74407-2774">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="74407-2774">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="74407-2775">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2775">Method getWorkspaceMetadata</span></span> 
<span data-ttu-id="74407-2776">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74407-2776">Called during workspace initialization.</span></span> <span data-ttu-id="74407-2777">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="74407-2777">Can be used to modify the workspace metadata</span></span>

     public SysAppWorkspaceMetadata getWorkspaceMetadata () 


#### <a name="return-value"></a><span data-ttu-id="74407-2778">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2778">Return Value</span></span> 
<span data-ttu-id="74407-2779">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-2779">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="74407-2780">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-2780">Method onBeginAppJob</span></span> 
<span data-ttu-id="74407-2781">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-2781">Called before the start of execution of AX mobile job</span></span>

     public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest) 


#### <a name="parameters"></a><span data-ttu-id="74407-2782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2782">Parameters</span></span>

| <span data-ttu-id="74407-2783">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2783">Parameter name</span></span> |  <span data-ttu-id="74407-2784">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2784">Parameter type</span></span> | <span data-ttu-id="74407-2785">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2785">Optional</span></span> | <span data-ttu-id="74407-2786">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2786">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2787">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="74407-2787">_sysAppJobRequest</span></span> | <span data-ttu-id="74407-2788">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="74407-2788">SysAppJobRequest</span></span> | <span data-ttu-id="74407-2789">False</span><span class="sxs-lookup"><span data-stu-id="74407-2789">False</span></span> | <span data-ttu-id="74407-2790">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="74407-2790">A class containing job request parameters</span></span>


### <a name="method-onendappjob"></a><span data-ttu-id="74407-2791">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="74407-2791">Method onEndAppJob</span></span> 
<span data-ttu-id="74407-2792">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="74407-2792">Called after the end of execution of AX mobile job</span></span>

     public void onEndAppJob (SysAppJobResponse _sysAppJobResponse) 


#### <a name="parameters"></a><span data-ttu-id="74407-2793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2793">Parameters</span></span>

| <span data-ttu-id="74407-2794">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2794">Parameter name</span></span> |  <span data-ttu-id="74407-2795">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2795">Parameter type</span></span> | <span data-ttu-id="74407-2796">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2796">Optional</span></span> | <span data-ttu-id="74407-2797">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2797">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2798">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="74407-2798">_sysAppJobResponse</span></span> | <span data-ttu-id="74407-2799">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="74407-2799">SysAppJobResponse</span></span> | <span data-ttu-id="74407-2800">False</span><span class="sxs-lookup"><span data-stu-id="74407-2800">False</span></span> | <span data-ttu-id="74407-2801">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="74407-2801">A class containing job response parameters</span></span>


### <a name="method-workspacehidden"></a><span data-ttu-id="74407-2802">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2802">Method workspaceHidden</span></span> 
<span data-ttu-id="74407-2803">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="74407-2803">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="74407-2804">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74407-2804">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="74407-2805">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2805">If the attribute is not specified on the class than it always returns false</span></span>

     public boolean workspaceHidden () 


#### <a name="return-value"></a><span data-ttu-id="74407-2806">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2806">Return Value</span></span> 
<span data-ttu-id="74407-2807">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2807">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="74407-2808">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2808">Class SysAppWorkspaceAttribute</span></span> 
<span data-ttu-id="74407-2809">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="74407-2809">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2810">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2810">Methods</span></span>

| <span data-ttu-id="74407-2811">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2811">Method name</span></span> | <span data-ttu-id="74407-2812">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2812">Returns</span></span> | <span data-ttu-id="74407-2813">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2813">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2814">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2814">new</span></span> | <span data-ttu-id="74407-2815">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2815">void</span></span> | <span data-ttu-id="74407-2816">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2816">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="74407-2817">AppId</span><span class="sxs-lookup"><span data-stu-id="74407-2817">AppId</span></span> | <span data-ttu-id="74407-2818">str</span><span class="sxs-lookup"><span data-stu-id="74407-2818">str</span></span> | <span data-ttu-id="74407-2819">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2819">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="74407-2820">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-2820">AppResourceName</span></span> | <span data-ttu-id="74407-2821">str</span><span class="sxs-lookup"><span data-stu-id="74407-2821">str</span></span> | <span data-ttu-id="74407-2822">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2822">Gets or sets the AOT Resource name which contains the workspace</span></span> |
| <span data-ttu-id="74407-2823">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2823">WorkspaceHidden</span></span> | <span data-ttu-id="74407-2824">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2824">boolean</span></span> | <span data-ttu-id="74407-2825">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2825">Gets or sets if the workspace is hidden from designer</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2826">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2826">Method new</span></span> 
<span data-ttu-id="74407-2827">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="74407-2827">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

     public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2828">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2828">Parameters</span></span>

| <span data-ttu-id="74407-2829">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2829">Parameter name</span></span> |  <span data-ttu-id="74407-2830">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2830">Parameter type</span></span> | <span data-ttu-id="74407-2831">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2831">Optional</span></span> | <span data-ttu-id="74407-2832">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2832">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2833">_appId</span><span class="sxs-lookup"><span data-stu-id="74407-2833">_appId</span></span> | <span data-ttu-id="74407-2834">str</span><span class="sxs-lookup"><span data-stu-id="74407-2834">str</span></span> | <span data-ttu-id="74407-2835">False</span><span class="sxs-lookup"><span data-stu-id="74407-2835">False</span></span> | <span data-ttu-id="74407-2836">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="74407-2836">The appId of the workspace</span></span>
| <span data-ttu-id="74407-2837">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-2837">_appResourceName</span></span> | <span data-ttu-id="74407-2838">str</span><span class="sxs-lookup"><span data-stu-id="74407-2838">str</span></span> | <span data-ttu-id="74407-2839">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2839">True</span></span> | <span data-ttu-id="74407-2840">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="74407-2840">The AOT resource name which contains the workspace</span></span>
| <span data-ttu-id="74407-2841">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2841">_workspaceHidden</span></span> | <span data-ttu-id="74407-2842">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2842">boolean</span></span> | <span data-ttu-id="74407-2843">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2843">True</span></span> | <span data-ttu-id="74407-2844">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="74407-2844">The workspace is hidden from designer</span></span>


### <a name="method-appid"></a><span data-ttu-id="74407-2845">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="74407-2845">Method AppId</span></span> 
<span data-ttu-id="74407-2846">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2846">Gets or sets the AppId of the workspace</span></span>

     public str AppId ([str _appId]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2847">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2847">Parameters</span></span>

| <span data-ttu-id="74407-2848">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2848">Parameter name</span></span> |  <span data-ttu-id="74407-2849">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2849">Parameter type</span></span> | <span data-ttu-id="74407-2850">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2850">Optional</span></span> | <span data-ttu-id="74407-2851">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2851">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2852">_appId</span><span class="sxs-lookup"><span data-stu-id="74407-2852">_appId</span></span> | <span data-ttu-id="74407-2853">str</span><span class="sxs-lookup"><span data-stu-id="74407-2853">str</span></span> | <span data-ttu-id="74407-2854">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2854">True</span></span> | <span data-ttu-id="74407-2855">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="74407-2855">The AppId of the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2856">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2856">Return Value</span></span> 
<span data-ttu-id="74407-2857">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="74407-2857">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="74407-2858">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-2858">Method AppResourceName</span></span> 
<span data-ttu-id="74407-2859">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2859">Gets or sets the AOT Resource name which contains the workspace</span></span>

     public str AppResourceName ([str _appResourceName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2860">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2860">Parameters</span></span>

| <span data-ttu-id="74407-2861">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2861">Parameter name</span></span> |  <span data-ttu-id="74407-2862">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2862">Parameter type</span></span> | <span data-ttu-id="74407-2863">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2863">Optional</span></span> | <span data-ttu-id="74407-2864">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2864">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2865">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="74407-2865">_appResourceName</span></span> | <span data-ttu-id="74407-2866">str</span><span class="sxs-lookup"><span data-stu-id="74407-2866">str</span></span> | <span data-ttu-id="74407-2867">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2867">True</span></span> | <span data-ttu-id="74407-2868">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="74407-2868">The AOT Resource name which contains the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2869">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2869">Return Value</span></span> 
<span data-ttu-id="74407-2870">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="74407-2870">The AOT Resource name which contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="74407-2871">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2871">Method WorkspaceHidden</span></span> 
<span data-ttu-id="74407-2872">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-2872">Gets or sets if the workspace is hidden from designer</span></span>

     public boolean WorkspaceHidden ([boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2873">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2873">Parameters</span></span>

| <span data-ttu-id="74407-2874">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2874">Parameter name</span></span> |  <span data-ttu-id="74407-2875">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2875">Parameter type</span></span> | <span data-ttu-id="74407-2876">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2876">Optional</span></span> | <span data-ttu-id="74407-2877">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2877">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2878">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="74407-2878">_workspaceHidden</span></span> | <span data-ttu-id="74407-2879">ブール値</span><span class="sxs-lookup"><span data-stu-id="74407-2879">boolean</span></span> | <span data-ttu-id="74407-2880">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2880">True</span></span> | <span data-ttu-id="74407-2881">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="74407-2881">The workspace hidden</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2882">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2882">Return Value</span></span> 
<span data-ttu-id="74407-2883">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="74407-2883">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="74407-2884">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2884">Class SysAppWorkspaceMetadata</span></span> 
<span data-ttu-id="74407-2885">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="74407-2885">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="74407-2886">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-2886">Methods</span></span>

| <span data-ttu-id="74407-2887">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-2887">Method name</span></span> | <span data-ttu-id="74407-2888">返品</span><span class="sxs-lookup"><span data-stu-id="74407-2888">Returns</span></span> | <span data-ttu-id="74407-2889">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2889">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-2890">新規</span><span class="sxs-lookup"><span data-stu-id="74407-2890">new</span></span> | <span data-ttu-id="74407-2891">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2891">void</span></span> |  |
| <span data-ttu-id="74407-2892">addConfig</span><span class="sxs-lookup"><span data-stu-id="74407-2892">addConfig</span></span> | <span data-ttu-id="74407-2893">無効</span><span class="sxs-lookup"><span data-stu-id="74407-2893">void</span></span> | <span data-ttu-id="74407-2894">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="74407-2894">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="74407-2895">getPage</span><span class="sxs-lookup"><span data-stu-id="74407-2895">getPage</span></span> | <span data-ttu-id="74407-2896">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2896">SysAppPageMetadata</span></span> | <span data-ttu-id="74407-2897">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2897">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="74407-2898">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2898">getPageEnumerator</span></span> | <span data-ttu-id="74407-2899">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2899">MapEnumerator</span></span> | <span data-ttu-id="74407-2900">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2900">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="74407-2901">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-2901">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="74407-2902">getAction</span><span class="sxs-lookup"><span data-stu-id="74407-2902">getAction</span></span> | <span data-ttu-id="74407-2903">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="74407-2903">SysAppActionMetadata</span></span> | <span data-ttu-id="74407-2904">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2904">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="74407-2905">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2905">getActionEnumerator</span></span> | <span data-ttu-id="74407-2906">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2906">MapEnumerator</span></span> | <span data-ttu-id="74407-2907">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2907">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="74407-2908">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-2908">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="74407-2909">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-2909">getPageNameForRecordingId</span></span> | <span data-ttu-id="74407-2910">str</span><span class="sxs-lookup"><span data-stu-id="74407-2910">str</span></span> | <span data-ttu-id="74407-2911">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2911">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="74407-2912">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-2912">getActionNameForRecordingId</span></span> | <span data-ttu-id="74407-2913">str</span><span class="sxs-lookup"><span data-stu-id="74407-2913">str</span></span> | <span data-ttu-id="74407-2914">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2914">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="74407-2915">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="74407-2915">workspaceTitle</span></span> | <span data-ttu-id="74407-2916">str</span><span class="sxs-lookup"><span data-stu-id="74407-2916">str</span></span> | <span data-ttu-id="74407-2917">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-2917">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="74407-2918">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="74407-2918">workspaceDescription</span></span> | <span data-ttu-id="74407-2919">str</span><span class="sxs-lookup"><span data-stu-id="74407-2919">str</span></span> | <span data-ttu-id="74407-2920">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-2920">Gets and sets the workspace description</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-2921">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-2921">Method new</span></span> 


     public void new (str _appId, [SysAppWorkspaceAttribute _attribute]) 


#### <a name="parameters"></a><span data-ttu-id="74407-2922">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2922">Parameters</span></span>

| <span data-ttu-id="74407-2923">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2923">Parameter name</span></span> |  <span data-ttu-id="74407-2924">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2924">Parameter type</span></span> | <span data-ttu-id="74407-2925">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2925">Optional</span></span> | <span data-ttu-id="74407-2926">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2926">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2927">_appId</span><span class="sxs-lookup"><span data-stu-id="74407-2927">_appId</span></span> | <span data-ttu-id="74407-2928">str</span><span class="sxs-lookup"><span data-stu-id="74407-2928">str</span></span> | <span data-ttu-id="74407-2929">False</span><span class="sxs-lookup"><span data-stu-id="74407-2929">False</span></span> | 
| <span data-ttu-id="74407-2930">_attribute</span><span class="sxs-lookup"><span data-stu-id="74407-2930">_attribute</span></span> | <span data-ttu-id="74407-2931">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-2931">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="74407-2932">はい</span><span class="sxs-lookup"><span data-stu-id="74407-2932">True</span></span> | 


### <a name="method-addconfig"></a><span data-ttu-id="74407-2933">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="74407-2933">Method addConfig</span></span> 
<span data-ttu-id="74407-2934">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="74407-2934">Adds a custom config to the mobile workspace metadata</span></span>

     public void addConfig (str _configName, object _configValue) 


#### <a name="parameters"></a><span data-ttu-id="74407-2935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2935">Parameters</span></span>

| <span data-ttu-id="74407-2936">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2936">Parameter name</span></span> |  <span data-ttu-id="74407-2937">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2937">Parameter type</span></span> | <span data-ttu-id="74407-2938">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2938">Optional</span></span> | <span data-ttu-id="74407-2939">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2939">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2940">_configName</span><span class="sxs-lookup"><span data-stu-id="74407-2940">_configName</span></span> | <span data-ttu-id="74407-2941">str</span><span class="sxs-lookup"><span data-stu-id="74407-2941">str</span></span> | <span data-ttu-id="74407-2942">False</span><span class="sxs-lookup"><span data-stu-id="74407-2942">False</span></span> | <span data-ttu-id="74407-2943">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="74407-2943">A config name</span></span>
| <span data-ttu-id="74407-2944">_configValue</span><span class="sxs-lookup"><span data-stu-id="74407-2944">_configValue</span></span> | <span data-ttu-id="74407-2945">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-2945">object</span></span> | <span data-ttu-id="74407-2946">False</span><span class="sxs-lookup"><span data-stu-id="74407-2946">False</span></span> | <span data-ttu-id="74407-2947">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="74407-2947">An object of a X++ data contract class</span></span>


### <a name="method-getpage"></a><span data-ttu-id="74407-2948">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="74407-2948">Method getPage</span></span> 
<span data-ttu-id="74407-2949">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2949">Returns the page with the pageName provided</span></span>

     public SysAppPageMetadata getPage (str _pageName) 


#### <a name="parameters"></a><span data-ttu-id="74407-2950">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2950">Parameters</span></span>

| <span data-ttu-id="74407-2951">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2951">Parameter name</span></span> |  <span data-ttu-id="74407-2952">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2952">Parameter type</span></span> | <span data-ttu-id="74407-2953">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2953">Optional</span></span> | <span data-ttu-id="74407-2954">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2954">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2955">_pageName</span><span class="sxs-lookup"><span data-stu-id="74407-2955">_pageName</span></span> | <span data-ttu-id="74407-2956">str</span><span class="sxs-lookup"><span data-stu-id="74407-2956">str</span></span> | <span data-ttu-id="74407-2957">False</span><span class="sxs-lookup"><span data-stu-id="74407-2957">False</span></span> | <span data-ttu-id="74407-2958">ページ名</span><span class="sxs-lookup"><span data-stu-id="74407-2958">A page name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2959">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2959">Return Value</span></span> 
<span data-ttu-id="74407-2960">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2960">Returns the pageMetadata if a page with the provided name exist; otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="74407-2961">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2961">Method getPageEnumerator</span></span> 
<span data-ttu-id="74407-2962">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2962">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="74407-2963">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-2963">Where key is page name and value is of type SysAppPageMetadata</span></span>

     public MapEnumerator getPageEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-2964">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2964">Return Value</span></span> 
<span data-ttu-id="74407-2965">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-2965">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="74407-2966">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="74407-2966">Method getAction</span></span> 
<span data-ttu-id="74407-2967">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="74407-2967">Returns the action with the actionName provided</span></span>

     public SysAppActionMetadata getAction (str _actionName) 


#### <a name="parameters"></a><span data-ttu-id="74407-2968">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2968">Parameters</span></span>

| <span data-ttu-id="74407-2969">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2969">Parameter name</span></span> |  <span data-ttu-id="74407-2970">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2970">Parameter type</span></span> | <span data-ttu-id="74407-2971">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2971">Optional</span></span> | <span data-ttu-id="74407-2972">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2972">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2973">_actionName</span><span class="sxs-lookup"><span data-stu-id="74407-2973">_actionName</span></span> | <span data-ttu-id="74407-2974">str</span><span class="sxs-lookup"><span data-stu-id="74407-2974">str</span></span> | <span data-ttu-id="74407-2975">False</span><span class="sxs-lookup"><span data-stu-id="74407-2975">False</span></span> | <span data-ttu-id="74407-2976">アクション名</span><span class="sxs-lookup"><span data-stu-id="74407-2976">An action name</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2977">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2977">Return Value</span></span> 
<span data-ttu-id="74407-2978">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2978">Returns the ActionMetadata if an action with the provided name exist; otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="74407-2979">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="74407-2979">Method getActionEnumerator</span></span> 
<span data-ttu-id="74407-2980">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="74407-2980">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="74407-2981">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="74407-2981">Where key is action name and value is of type SysAppActionMetadata</span></span>

     public MapEnumerator getActionEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="74407-2982">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2982">Return Value</span></span> 
<span data-ttu-id="74407-2983">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="74407-2983">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="74407-2984">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-2984">Method getPageNameForRecordingId</span></span> 
<span data-ttu-id="74407-2985">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2985">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

     public str getPageNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="74407-2986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2986">Parameters</span></span>

| <span data-ttu-id="74407-2987">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-2987">Parameter name</span></span> |  <span data-ttu-id="74407-2988">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-2988">Parameter type</span></span> | <span data-ttu-id="74407-2989">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-2989">Optional</span></span> | <span data-ttu-id="74407-2990">説明</span><span class="sxs-lookup"><span data-stu-id="74407-2990">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-2991">_recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-2991">_recordingId</span></span> | <span data-ttu-id="74407-2992">str</span><span class="sxs-lookup"><span data-stu-id="74407-2992">str</span></span> | <span data-ttu-id="74407-2993">False</span><span class="sxs-lookup"><span data-stu-id="74407-2993">False</span></span> | <span data-ttu-id="74407-2994">recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-2994">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-2995">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-2995">Return Value</span></span> 
<span data-ttu-id="74407-2996">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="74407-2996">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="74407-2997">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="74407-2997">Method getActionNameForRecordingId</span></span> 
<span data-ttu-id="74407-2998">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="74407-2998">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

     public str getActionNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="74407-2999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-2999">Parameters</span></span>

| <span data-ttu-id="74407-3000">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-3000">Parameter name</span></span> |  <span data-ttu-id="74407-3001">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3001">Parameter type</span></span> | <span data-ttu-id="74407-3002">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-3002">Optional</span></span> | <span data-ttu-id="74407-3003">説明</span><span class="sxs-lookup"><span data-stu-id="74407-3003">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-3004">_recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-3004">_recordingId</span></span> | <span data-ttu-id="74407-3005">str</span><span class="sxs-lookup"><span data-stu-id="74407-3005">str</span></span> | <span data-ttu-id="74407-3006">False</span><span class="sxs-lookup"><span data-stu-id="74407-3006">False</span></span> | <span data-ttu-id="74407-3007">recordingId</span><span class="sxs-lookup"><span data-stu-id="74407-3007">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-3008">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-3008">Return Value</span></span> 
<span data-ttu-id="74407-3009">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="74407-3009">An action name if the supplied recordingId is used by a workspace action;otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="74407-3010">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="74407-3010">Method workspaceTitle</span></span> 
<span data-ttu-id="74407-3011">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-3011">Gets and sets the workspace title</span></span>

     public str workspaceTitle ([str _workspaceTitle]) 


#### <a name="parameters"></a><span data-ttu-id="74407-3012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-3012">Parameters</span></span>

| <span data-ttu-id="74407-3013">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-3013">Parameter name</span></span> |  <span data-ttu-id="74407-3014">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3014">Parameter type</span></span> | <span data-ttu-id="74407-3015">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-3015">Optional</span></span> | <span data-ttu-id="74407-3016">説明</span><span class="sxs-lookup"><span data-stu-id="74407-3016">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-3017">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="74407-3017">_workspaceTitle</span></span> | <span data-ttu-id="74407-3018">str</span><span class="sxs-lookup"><span data-stu-id="74407-3018">str</span></span> | <span data-ttu-id="74407-3019">はい</span><span class="sxs-lookup"><span data-stu-id="74407-3019">True</span></span> | <span data-ttu-id="74407-3020">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="74407-3020">The workspace title</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-3021">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-3021">Return Value</span></span> 
<span data-ttu-id="74407-3022">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="74407-3022">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="74407-3023">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="74407-3023">Method workspaceDescription</span></span> 
<span data-ttu-id="74407-3024">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="74407-3024">Gets and sets the workspace description</span></span>

     public str workspaceDescription ([str _workspaceDescription]) 


#### <a name="parameters"></a><span data-ttu-id="74407-3025">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-3025">Parameters</span></span>

| <span data-ttu-id="74407-3026">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-3026">Parameter name</span></span> |  <span data-ttu-id="74407-3027">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3027">Parameter type</span></span> | <span data-ttu-id="74407-3028">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-3028">Optional</span></span> | <span data-ttu-id="74407-3029">説明</span><span class="sxs-lookup"><span data-stu-id="74407-3029">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-3030">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="74407-3030">_workspaceDescription</span></span> | <span data-ttu-id="74407-3031">str</span><span class="sxs-lookup"><span data-stu-id="74407-3031">str</span></span> | <span data-ttu-id="74407-3032">はい</span><span class="sxs-lookup"><span data-stu-id="74407-3032">True</span></span> | <span data-ttu-id="74407-3033">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="74407-3033">The workspace description</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-3034">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-3034">Return Value</span></span> 
<span data-ttu-id="74407-3035">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="74407-3035">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="74407-3036">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="74407-3036">Class SysAppWorkspaceSecurityAttribute</span></span> 
<span data-ttu-id="74407-3037">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="74407-3037">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="74407-3038">メソッド</span><span class="sxs-lookup"><span data-stu-id="74407-3038">Methods</span></span>

| <span data-ttu-id="74407-3039">メソッド名</span><span class="sxs-lookup"><span data-stu-id="74407-3039">Method name</span></span> | <span data-ttu-id="74407-3040">返品</span><span class="sxs-lookup"><span data-stu-id="74407-3040">Returns</span></span> | <span data-ttu-id="74407-3041">説明</span><span class="sxs-lookup"><span data-stu-id="74407-3041">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="74407-3042">新規</span><span class="sxs-lookup"><span data-stu-id="74407-3042">new</span></span> | <span data-ttu-id="74407-3043">無効</span><span class="sxs-lookup"><span data-stu-id="74407-3043">void</span></span> | <span data-ttu-id="74407-3044">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="74407-3044">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="74407-3045">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-3045">WorkspaceMenuItemName</span></span> | <span data-ttu-id="74407-3046">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-3046">MenuItemName</span></span> | <span data-ttu-id="74407-3047">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-3047">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="74407-3048">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-3048">WorkspaceMenuItemType</span></span> | <span data-ttu-id="74407-3049">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-3049">MenuItemType</span></span> | <span data-ttu-id="74407-3050">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-3050">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |


### <a name="method-new"></a><span data-ttu-id="74407-3051">メソッド new</span><span class="sxs-lookup"><span data-stu-id="74407-3051">Method new</span></span> 
<span data-ttu-id="74407-3052">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="74407-3052">Creates a new instance of attribute</span></span>

     public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="74407-3053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-3053">Parameters</span></span>

| <span data-ttu-id="74407-3054">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-3054">Parameter name</span></span> |  <span data-ttu-id="74407-3055">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3055">Parameter type</span></span> | <span data-ttu-id="74407-3056">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-3056">Optional</span></span> | <span data-ttu-id="74407-3057">説明</span><span class="sxs-lookup"><span data-stu-id="74407-3057">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-3058">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-3058">_workspaceMenuItemName</span></span> | <span data-ttu-id="74407-3059">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-3059">MenuItemName</span></span> | <span data-ttu-id="74407-3060">False</span><span class="sxs-lookup"><span data-stu-id="74407-3060">False</span></span> | <span data-ttu-id="74407-3061">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="74407-3061">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="74407-3062">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-3062">_workspaceMenuItemType</span></span> | <span data-ttu-id="74407-3063">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-3063">MenuItemType</span></span> | <span data-ttu-id="74407-3064">はい</span><span class="sxs-lookup"><span data-stu-id="74407-3064">True</span></span> | <span data-ttu-id="74407-3065">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3065">The menu item type</span></span>


### <a name="method-workspacemenuitemname"></a><span data-ttu-id="74407-3066">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-3066">Method WorkspaceMenuItemName</span></span> 
<span data-ttu-id="74407-3067">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-3067">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

     public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName]) 


#### <a name="parameters"></a><span data-ttu-id="74407-3068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-3068">Parameters</span></span>

| <span data-ttu-id="74407-3069">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-3069">Parameter name</span></span> |  <span data-ttu-id="74407-3070">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3070">Parameter type</span></span> | <span data-ttu-id="74407-3071">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-3071">Optional</span></span> | <span data-ttu-id="74407-3072">説明</span><span class="sxs-lookup"><span data-stu-id="74407-3072">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-3073">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-3073">_workspaceMenuItemName</span></span> | <span data-ttu-id="74407-3074">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="74407-3074">MenuItemName</span></span> | <span data-ttu-id="74407-3075">はい</span><span class="sxs-lookup"><span data-stu-id="74407-3075">True</span></span> | <span data-ttu-id="74407-3076">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="74407-3076">The workspace menu item for the workspace security attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-3077">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-3077">Return Value</span></span> 
<span data-ttu-id="74407-3078">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="74407-3078">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="74407-3079">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-3079">Method WorkspaceMenuItemType</span></span> 
<span data-ttu-id="74407-3080">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="74407-3080">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

     public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="74407-3081">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74407-3081">Parameters</span></span>

| <span data-ttu-id="74407-3082">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="74407-3082">Parameter name</span></span> |  <span data-ttu-id="74407-3083">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3083">Parameter type</span></span> | <span data-ttu-id="74407-3084">オプション</span><span class="sxs-lookup"><span data-stu-id="74407-3084">Optional</span></span> | <span data-ttu-id="74407-3085">説明</span><span class="sxs-lookup"><span data-stu-id="74407-3085">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="74407-3086">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-3086">_workspaceMenuItemType</span></span> | <span data-ttu-id="74407-3087">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="74407-3087">MenuItemType</span></span> | <span data-ttu-id="74407-3088">はい</span><span class="sxs-lookup"><span data-stu-id="74407-3088">True</span></span> | <span data-ttu-id="74407-3089">workspacesecurity 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3089">The workspace menu item type for the workspacesecurity attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="74407-3090">戻り値</span><span class="sxs-lookup"><span data-stu-id="74407-3090">Return Value</span></span> 
<span data-ttu-id="74407-3091">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="74407-3091">The workspace menu item type for the workspace security attribute</span></span>

