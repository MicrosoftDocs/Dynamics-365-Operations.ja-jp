---
title: "サーバー側 API"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4acc6dea4dec4e81aaea3111ee6c5db6e1c07076
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="server-side-development-workspace-x-apis"></a><span data-ttu-id="b03d2-103">サーバー側の開発 (ワークスペース X++ API)</span><span class="sxs-lookup"><span data-stu-id="b03d2-103">Server-side development (workspace X++ APIs)</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="class-sysappactionattribute"></a><span data-ttu-id="b03d2-104">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-104">Class SysAppActionAttribute</span></span> 
<span data-ttu-id="b03d2-105">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-105">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-106">Methods</span></span>

| <span data-ttu-id="b03d2-107">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-107">Method name</span></span> | <span data-ttu-id="b03d2-108">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-108">Returns</span></span> | <span data-ttu-id="b03d2-109">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-109">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-110">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-110">new</span></span> | <span data-ttu-id="b03d2-111">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-111">void</span></span> | <span data-ttu-id="b03d2-112">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-112">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="b03d2-113">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="b03d2-113">pageMethodName</span></span> | <span data-ttu-id="b03d2-114">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-114">str</span></span> | <span data-ttu-id="b03d2-115">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-115">Gets the get method name which forms the page under which this task resides</span></span> |
| <span data-ttu-id="b03d2-116">actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-116">actionTitle</span></span> | <span data-ttu-id="b03d2-117">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-117">str</span></span> | <span data-ttu-id="b03d2-118">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-118">Gets the Action Title</span></span> |
| <span data-ttu-id="b03d2-119">actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-119">actionDescription</span></span> | <span data-ttu-id="b03d2-120">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-120">str</span></span> | <span data-ttu-id="b03d2-121">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-121">Gets the Action Description</span></span> |
| <span data-ttu-id="b03d2-122">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="b03d2-122">crudOperationType</span></span> | <span data-ttu-id="b03d2-123">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="b03d2-123">SysAppCRUDOperation</span></span> | <span data-ttu-id="b03d2-124">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-124">Gets the Crud Operation Type like Create, Update, Delete</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-125">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-125">Method new</span></span> 
<span data-ttu-id="b03d2-126">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-126">Creates a new instance of SysAppActionAttribute class</span></span>

     public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-127">Parameters</span></span>

| <span data-ttu-id="b03d2-128">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-128">Parameter name</span></span> |  <span data-ttu-id="b03d2-129">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-129">Parameter type</span></span> | <span data-ttu-id="b03d2-130">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-130">Optional</span></span> | <span data-ttu-id="b03d2-131">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-131">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-132">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-132">_actionTitle</span></span> | <span data-ttu-id="b03d2-133">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-133">str</span></span> | <span data-ttu-id="b03d2-134">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-134">True</span></span> | <span data-ttu-id="b03d2-135">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-135">Action title</span></span>
| <span data-ttu-id="b03d2-136">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-136">_actionDescription</span></span> | <span data-ttu-id="b03d2-137">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-137">str</span></span> | <span data-ttu-id="b03d2-138">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-138">True</span></span> | <span data-ttu-id="b03d2-139">アクション説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-139">Action description</span></span>
| <span data-ttu-id="b03d2-140">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="b03d2-140">_crudOperationType</span></span> | <span data-ttu-id="b03d2-141">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="b03d2-141">SysAppCRUDOperation</span></span> | <span data-ttu-id="b03d2-142">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-142">True</span></span> | <span data-ttu-id="b03d2-143">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="b03d2-143">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="b03d2-144">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="b03d2-144">_pageMethodName</span></span> | <span data-ttu-id="b03d2-145">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-145">str</span></span> | <span data-ttu-id="b03d2-146">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-146">True</span></span> | <span data-ttu-id="b03d2-147">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-147">Name of the method constructing parent page</span></span>


### <a name="method-pagemethodname"></a><span data-ttu-id="b03d2-148">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="b03d2-148">Method pageMethodName</span></span> 
<span data-ttu-id="b03d2-149">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-149">Gets the get method name which forms the page under which this task resides</span></span>

     public str pageMethodName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-150">Return Value</span></span> 
<span data-ttu-id="b03d2-151">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-151">The page method name which forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="b03d2-152">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-152">Method actionTitle</span></span> 
<span data-ttu-id="b03d2-153">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-153">Gets the Action Title</span></span>

     public str actionTitle () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-154">Return Value</span></span> 
<span data-ttu-id="b03d2-155">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-155">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="b03d2-156">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-156">Method actionDescription</span></span> 
<span data-ttu-id="b03d2-157">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-157">Gets the Action Description</span></span>

     public str actionDescription () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-158">Return Value</span></span> 
<span data-ttu-id="b03d2-159">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-159">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="b03d2-160">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="b03d2-160">Method crudOperationType</span></span> 
<span data-ttu-id="b03d2-161">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-161">Gets the Crud Operation Type like Create, Update, Delete</span></span>

     public SysAppCRUDOperation crudOperationType () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-162">Return Value</span></span> 
<span data-ttu-id="b03d2-163">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-163">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="b03d2-164">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-164">Class SysAppActionMetadata</span></span> 
<span data-ttu-id="b03d2-165">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-165">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-166">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-166">Methods</span></span>

| <span data-ttu-id="b03d2-167">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-167">Method name</span></span> | <span data-ttu-id="b03d2-168">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-168">Returns</span></span> | <span data-ttu-id="b03d2-169">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-169">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-170">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-170">new</span></span> | <span data-ttu-id="b03d2-171">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-171">void</span></span> |  |
| <span data-ttu-id="b03d2-172">getActionName</span><span class="sxs-lookup"><span data-stu-id="b03d2-172">getActionName</span></span> | <span data-ttu-id="b03d2-173">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-173">str</span></span> | <span data-ttu-id="b03d2-174">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-174">Returns the action name</span></span> |
| <span data-ttu-id="b03d2-175">actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-175">actionTitle</span></span> | <span data-ttu-id="b03d2-176">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-176">str</span></span> | <span data-ttu-id="b03d2-177">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-177">Gets or sets the action title</span></span> |
| <span data-ttu-id="b03d2-178">actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-178">actionDescription</span></span> | <span data-ttu-id="b03d2-179">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-179">str</span></span> | <span data-ttu-id="b03d2-180">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-180">Gets or sets the action description</span></span> |
| <span data-ttu-id="b03d2-181">actionHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-181">actionHidden</span></span> | <span data-ttu-id="b03d2-182">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-182">boolean</span></span> | <span data-ttu-id="b03d2-183">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-183">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="b03d2-184">actionOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-184">actionOrder</span></span> | <span data-ttu-id="b03d2-185">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-185">int</span></span> | <span data-ttu-id="b03d2-186">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-186">Gets or sets the action order</span></span> |
| <span data-ttu-id="b03d2-187">getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-187">getControl</span></span> | <span data-ttu-id="b03d2-188">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-188">SysAppControlMetadata</span></span> | <span data-ttu-id="b03d2-189">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-189">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="b03d2-190">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-190">getControlEnumerator</span></span> | <span data-ttu-id="b03d2-191">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-191">MapEnumerator</span></span> | <span data-ttu-id="b03d2-192">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-192">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="b03d2-193">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-193">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-194">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-194">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-195">Parameters</span></span>

| <span data-ttu-id="b03d2-196">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-196">Parameter name</span></span> |  <span data-ttu-id="b03d2-197">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-197">Parameter type</span></span> | <span data-ttu-id="b03d2-198">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-198">Optional</span></span> | <span data-ttu-id="b03d2-199">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-199">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-200">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-200">_taskmetadata</span></span> | <span data-ttu-id="b03d2-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="b03d2-202">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-202">False</span></span> | 


### <a name="method-getactionname"></a><span data-ttu-id="b03d2-203">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="b03d2-203">Method getActionName</span></span> 
<span data-ttu-id="b03d2-204">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-204">Returns the action name</span></span>

     public str getActionName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-205">Return Value</span></span> 
<span data-ttu-id="b03d2-206">アクション名</span><span class="sxs-lookup"><span data-stu-id="b03d2-206">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="b03d2-207">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-207">Method actionTitle</span></span> 
<span data-ttu-id="b03d2-208">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-208">Gets or sets the action title</span></span>

     public str actionTitle ([str _actionTitle]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-209">Parameters</span></span>

| <span data-ttu-id="b03d2-210">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-210">Parameter name</span></span> |  <span data-ttu-id="b03d2-211">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-211">Parameter type</span></span> | <span data-ttu-id="b03d2-212">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-212">Optional</span></span> | <span data-ttu-id="b03d2-213">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-213">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-214">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-214">_actionTitle</span></span> | <span data-ttu-id="b03d2-215">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-215">str</span></span> | <span data-ttu-id="b03d2-216">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-216">True</span></span> | <span data-ttu-id="b03d2-217">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-217">The action title</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-218">Return Value</span></span> 
<span data-ttu-id="b03d2-219">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-219">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="b03d2-220">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-220">Method actionDescription</span></span> 
<span data-ttu-id="b03d2-221">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-221">Gets or sets the action description</span></span>

     public str actionDescription ([str _actionDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-222">Parameters</span></span>

| <span data-ttu-id="b03d2-223">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-223">Parameter name</span></span> |  <span data-ttu-id="b03d2-224">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-224">Parameter type</span></span> | <span data-ttu-id="b03d2-225">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-225">Optional</span></span> | <span data-ttu-id="b03d2-226">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-226">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-227">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-227">_actionDescription</span></span> | <span data-ttu-id="b03d2-228">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-228">str</span></span> | <span data-ttu-id="b03d2-229">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-229">True</span></span> | <span data-ttu-id="b03d2-230">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-230">The action description</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-231">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-231">Return Value</span></span> 
<span data-ttu-id="b03d2-232">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-232">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="b03d2-233">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-233">Method actionHidden</span></span> 
<span data-ttu-id="b03d2-234">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-234">Gets or sets whether action is hidden</span></span>

     public boolean actionHidden ([boolean _actionHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-235">Parameters</span></span>

| <span data-ttu-id="b03d2-236">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-236">Parameter name</span></span> |  <span data-ttu-id="b03d2-237">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-237">Parameter type</span></span> | <span data-ttu-id="b03d2-238">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-238">Optional</span></span> | <span data-ttu-id="b03d2-239">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-239">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-240">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-240">_actionHidden</span></span> | <span data-ttu-id="b03d2-241">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-241">boolean</span></span> | <span data-ttu-id="b03d2-242">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-242">True</span></span> | <span data-ttu-id="b03d2-243">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="b03d2-243">Action hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-244">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-244">Return Value</span></span> 
<span data-ttu-id="b03d2-245">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b03d2-245">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="b03d2-246">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-246">Method actionOrder</span></span> 
<span data-ttu-id="b03d2-247">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-247">Gets or sets the action order</span></span>

     public int actionOrder ([int _actionOrder]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-248">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-248">Parameters</span></span>

| <span data-ttu-id="b03d2-249">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-249">Parameter name</span></span> |  <span data-ttu-id="b03d2-250">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-250">Parameter type</span></span> | <span data-ttu-id="b03d2-251">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-251">Optional</span></span> | <span data-ttu-id="b03d2-252">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-252">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-253">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-253">_actionOrder</span></span> | <span data-ttu-id="b03d2-254">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-254">int</span></span> | <span data-ttu-id="b03d2-255">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-255">True</span></span> | <span data-ttu-id="b03d2-256">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-256">The action order</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-257">Return Value</span></span> 
<span data-ttu-id="b03d2-258">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-258">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="b03d2-259">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-259">Method getControl</span></span> 
<span data-ttu-id="b03d2-260">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-260">Returns the control on the current action having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-261">Parameters</span></span>

| <span data-ttu-id="b03d2-262">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-262">Parameter name</span></span> |  <span data-ttu-id="b03d2-263">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-263">Parameter type</span></span> | <span data-ttu-id="b03d2-264">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-264">Optional</span></span> | <span data-ttu-id="b03d2-265">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-265">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-266">_controlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-266">_controlName</span></span> | <span data-ttu-id="b03d2-267">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-267">str</span></span> | <span data-ttu-id="b03d2-268">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-268">False</span></span> | <span data-ttu-id="b03d2-269">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="b03d2-269">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-270">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-270">Return Value</span></span> 
<span data-ttu-id="b03d2-271">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="b03d2-271">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action;otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="b03d2-272">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-272">Method getControlEnumerator</span></span> 
<span data-ttu-id="b03d2-273">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-273">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="b03d2-274">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-274">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-275">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-275">Return Value</span></span> 
<span data-ttu-id="b03d2-276">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-276">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="b03d2-277">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="b03d2-277">Class SysAppAttributeHelper</span></span> 
<span data-ttu-id="b03d2-278">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-278">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-279">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-279">Methods</span></span>

| <span data-ttu-id="b03d2-280">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-280">Method name</span></span> | <span data-ttu-id="b03d2-281">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-281">Returns</span></span> | <span data-ttu-id="b03d2-282">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-282">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-283">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-283">getAttributeFromClass</span></span> | <span data-ttu-id="b03d2-284">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-284">SysAttribute</span></span> | <span data-ttu-id="b03d2-285">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="b03d2-285">gets attribute from class</span></span> |


### <a name="method-getattributefromclass"></a><span data-ttu-id="b03d2-286">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-286">Method getAttributeFromClass</span></span> 
<span data-ttu-id="b03d2-287">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="b03d2-287">gets attribute from class</span></span>

     public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-288">Parameters</span></span>

| <span data-ttu-id="b03d2-289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-289">Parameter name</span></span> |  <span data-ttu-id="b03d2-290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-290">Parameter type</span></span> | <span data-ttu-id="b03d2-291">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-291">Optional</span></span> | <span data-ttu-id="b03d2-292">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-293">_sysClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-293">_sysClass</span></span> | <span data-ttu-id="b03d2-294">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-294">SysDictClass</span></span> | <span data-ttu-id="b03d2-295">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-295">False</span></span> | <span data-ttu-id="b03d2-296">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-296">class for which attributes is required</span></span>
| <span data-ttu-id="b03d2-297">_attributeType</span><span class="sxs-lookup"><span data-stu-id="b03d2-297">_attributeType</span></span> | <span data-ttu-id="b03d2-298">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="b03d2-298">SysAppAttributeType</span></span> | <span data-ttu-id="b03d2-299">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-299">False</span></span> | <span data-ttu-id="b03d2-300">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="b03d2-300">Type of attribute like SysAppEntityAttribute</span></span>


## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="b03d2-301">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-301">Class SysAppCollectionAttribute</span></span> 
<span data-ttu-id="b03d2-302">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-302">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-303">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-303">Methods</span></span>

| <span data-ttu-id="b03d2-304">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-304">Method name</span></span> | <span data-ttu-id="b03d2-305">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-305">Returns</span></span> | <span data-ttu-id="b03d2-306">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-306">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-307">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-307">new</span></span> | <span data-ttu-id="b03d2-308">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-308">void</span></span> | <span data-ttu-id="b03d2-309">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-309">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-310">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-310">Method new</span></span> 
<span data-ttu-id="b03d2-311">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-311">Constructor</span></span>

     public void new (str _itemContractName, [str _label], [str _relationshipName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-312">Parameters</span></span>

| <span data-ttu-id="b03d2-313">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-313">Parameter name</span></span> |  <span data-ttu-id="b03d2-314">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-314">Parameter type</span></span> | <span data-ttu-id="b03d2-315">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-315">Optional</span></span> | <span data-ttu-id="b03d2-316">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-316">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-317">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="b03d2-317">_itemContractName</span></span> | <span data-ttu-id="b03d2-318">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-318">str</span></span> | <span data-ttu-id="b03d2-319">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-319">False</span></span> | <span data-ttu-id="b03d2-320">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="b03d2-320">Data contract name of list item</span></span>
| <span data-ttu-id="b03d2-321">_label</span><span class="sxs-lookup"><span data-stu-id="b03d2-321">_label</span></span> | <span data-ttu-id="b03d2-322">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-322">str</span></span> | <span data-ttu-id="b03d2-323">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-323">True</span></span> | <span data-ttu-id="b03d2-324">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-324">List control label</span></span>
| <span data-ttu-id="b03d2-325">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="b03d2-325">_relationshipName</span></span> | <span data-ttu-id="b03d2-326">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-326">str</span></span> | <span data-ttu-id="b03d2-327">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-327">True</span></span> | <span data-ttu-id="b03d2-328">関係名。</span><span class="sxs-lookup"><span data-stu-id="b03d2-328">Relationship name.</span></span> <span data-ttu-id="b03d2-329">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-329">By default the entity name of the list item is used as relationship name</span></span>


## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="b03d2-330">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-330">Class SysAppControlMetadata</span></span> 
<span data-ttu-id="b03d2-331">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-331">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="b03d2-332">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="b03d2-332">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-333">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-333">Methods</span></span>

| <span data-ttu-id="b03d2-334">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-334">Method name</span></span> | <span data-ttu-id="b03d2-335">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-335">Returns</span></span> | <span data-ttu-id="b03d2-336">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-336">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-337">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-337">new</span></span> | <span data-ttu-id="b03d2-338">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-338">void</span></span> | <span data-ttu-id="b03d2-339">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-339">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="b03d2-340">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="b03d2-340">getBaseLanguageId</span></span> | <span data-ttu-id="b03d2-341">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-341">str</span></span> | <span data-ttu-id="b03d2-342">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-342">Returns the base language id for the app</span></span> |
| <span data-ttu-id="b03d2-343">getControlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-343">getControlName</span></span> | <span data-ttu-id="b03d2-344">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-344">str</span></span> | <span data-ttu-id="b03d2-345">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-345">Returns the control name</span></span> |
| <span data-ttu-id="b03d2-346">controlLabel</span><span class="sxs-lookup"><span data-stu-id="b03d2-346">controlLabel</span></span> | <span data-ttu-id="b03d2-347">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-347">str</span></span> | <span data-ttu-id="b03d2-348">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-348">Gets and sets the control label</span></span> |
| <span data-ttu-id="b03d2-349">controlHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-349">controlHidden</span></span> | <span data-ttu-id="b03d2-350">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-350">boolean</span></span> | <span data-ttu-id="b03d2-351">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-351">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="b03d2-352">controlOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-352">controlOrder</span></span> | <span data-ttu-id="b03d2-353">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-353">int</span></span> | <span data-ttu-id="b03d2-354">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-354">Gets or sets the control order</span></span> |
| <span data-ttu-id="b03d2-355">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="b03d2-355">controlMandatory</span></span> | <span data-ttu-id="b03d2-356">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-356">boolean</span></span> | <span data-ttu-id="b03d2-357">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-357">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="b03d2-358">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="b03d2-358">controlAllowNegative</span></span> | <span data-ttu-id="b03d2-359">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-359">boolean</span></span> | <span data-ttu-id="b03d2-360">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="b03d2-360">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="b03d2-361">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="b03d2-361">controlMaxLength</span></span> | <span data-ttu-id="b03d2-362">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-362">int</span></span> | <span data-ttu-id="b03d2-363">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-363">Gets or sets the control max length</span></span> |
| <span data-ttu-id="b03d2-364">getProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-364">getProperty</span></span> | <span data-ttu-id="b03d2-365">anytype</span><span class="sxs-lookup"><span data-stu-id="b03d2-365">anytype</span></span> | <span data-ttu-id="b03d2-366">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-366">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="b03d2-367">setProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-367">setProperty</span></span> | <span data-ttu-id="b03d2-368">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-368">void</span></span> | <span data-ttu-id="b03d2-369">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-369">Sets the control property referenced by the key</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-370">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-370">Method new</span></span> 
<span data-ttu-id="b03d2-371">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-371">Creates a new instance of the control metadata</span></span>

     public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-372">Parameters</span></span>

| <span data-ttu-id="b03d2-373">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-373">Parameter name</span></span> |  <span data-ttu-id="b03d2-374">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-374">Parameter type</span></span> | <span data-ttu-id="b03d2-375">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-375">Optional</span></span> | <span data-ttu-id="b03d2-376">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-376">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-377">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-377">_controlMetadata</span></span> | <span data-ttu-id="b03d2-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="b03d2-379">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-379">False</span></span> | <span data-ttu-id="b03d2-380">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-380">The controlMetadata object</span></span>
| <span data-ttu-id="b03d2-381">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="b03d2-381">_baseLanguageId</span></span> | <span data-ttu-id="b03d2-382">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-382">str</span></span> | <span data-ttu-id="b03d2-383">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-383">True</span></span> | <span data-ttu-id="b03d2-384">基本言語</span><span class="sxs-lookup"><span data-stu-id="b03d2-384">The base language</span></span>


### <a name="method-getbaselanguageid"></a><span data-ttu-id="b03d2-385">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="b03d2-385">Method getBaseLanguageId</span></span> 
<span data-ttu-id="b03d2-386">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-386">Returns the base language id for the app</span></span>

     public str getBaseLanguageId () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-387">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-387">Return Value</span></span> 
<span data-ttu-id="b03d2-388">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-388">The base language id</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="b03d2-389">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-389">Method getControlName</span></span> 
<span data-ttu-id="b03d2-390">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-390">Returns the control name</span></span>

     public str getControlName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-391">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-391">Return Value</span></span> 
<span data-ttu-id="b03d2-392">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="b03d2-392">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="b03d2-393">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="b03d2-393">Method controlLabel</span></span> 
<span data-ttu-id="b03d2-394">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-394">Gets and sets the control label</span></span>

     public str controlLabel ([str _controlLabel]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-395">Parameters</span></span>

| <span data-ttu-id="b03d2-396">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-396">Parameter name</span></span> |  <span data-ttu-id="b03d2-397">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-397">Parameter type</span></span> | <span data-ttu-id="b03d2-398">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-398">Optional</span></span> | <span data-ttu-id="b03d2-399">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-399">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-400">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="b03d2-400">_controlLabel</span></span> | <span data-ttu-id="b03d2-401">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-401">str</span></span> | <span data-ttu-id="b03d2-402">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-402">True</span></span> | <span data-ttu-id="b03d2-403">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-403">The control label</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-404">Return Value</span></span> 
<span data-ttu-id="b03d2-405">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-405">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="b03d2-406">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-406">Method controlHidden</span></span> 
<span data-ttu-id="b03d2-407">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-407">Gets and sets whether the control is hidden</span></span>

     public boolean controlHidden ([boolean _controlHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-408">Parameters</span></span>

| <span data-ttu-id="b03d2-409">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-409">Parameter name</span></span> |  <span data-ttu-id="b03d2-410">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-410">Parameter type</span></span> | <span data-ttu-id="b03d2-411">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-411">Optional</span></span> | <span data-ttu-id="b03d2-412">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-412">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-413">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-413">_controlHidden</span></span> | <span data-ttu-id="b03d2-414">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-414">boolean</span></span> | <span data-ttu-id="b03d2-415">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-415">True</span></span> | <span data-ttu-id="b03d2-416">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="b03d2-416">Control hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-417">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-417">Return Value</span></span> 
<span data-ttu-id="b03d2-418">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b03d2-418">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="b03d2-419">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-419">Method controlOrder</span></span> 
<span data-ttu-id="b03d2-420">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-420">Gets or sets the control order</span></span>

     public int controlOrder ([int _controlOrder]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-421">Parameters</span></span>

| <span data-ttu-id="b03d2-422">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-422">Parameter name</span></span> |  <span data-ttu-id="b03d2-423">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-423">Parameter type</span></span> | <span data-ttu-id="b03d2-424">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-424">Optional</span></span> | <span data-ttu-id="b03d2-425">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-425">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-426">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-426">_controlOrder</span></span> | <span data-ttu-id="b03d2-427">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-427">int</span></span> | <span data-ttu-id="b03d2-428">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-428">True</span></span> | <span data-ttu-id="b03d2-429">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-429">The control order</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-430">Return Value</span></span> 
<span data-ttu-id="b03d2-431">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-431">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="b03d2-432">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="b03d2-432">Method controlMandatory</span></span> 
<span data-ttu-id="b03d2-433">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-433">Gets or sets the control mandatory</span></span>

     public boolean controlMandatory ([boolean _controlMandatory]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-434">Parameters</span></span>

| <span data-ttu-id="b03d2-435">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-435">Parameter name</span></span> |  <span data-ttu-id="b03d2-436">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-436">Parameter type</span></span> | <span data-ttu-id="b03d2-437">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-437">Optional</span></span> | <span data-ttu-id="b03d2-438">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-438">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-439">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="b03d2-439">_controlMandatory</span></span> | <span data-ttu-id="b03d2-440">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-440">boolean</span></span> | <span data-ttu-id="b03d2-441">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-441">True</span></span> | <span data-ttu-id="b03d2-442">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="b03d2-442">The control mandatory</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-443">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-443">Return Value</span></span> 
<span data-ttu-id="b03d2-444">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="b03d2-444">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="b03d2-445">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="b03d2-445">Method controlAllowNegative</span></span> 
<span data-ttu-id="b03d2-446">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="b03d2-446">Gets or sets the control allow negative</span></span>

     public boolean controlAllowNegative ([boolean _controlAllowNegative]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-447">Parameters</span></span>

| <span data-ttu-id="b03d2-448">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-448">Parameter name</span></span> |  <span data-ttu-id="b03d2-449">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-449">Parameter type</span></span> | <span data-ttu-id="b03d2-450">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-450">Optional</span></span> | <span data-ttu-id="b03d2-451">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-451">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-452">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="b03d2-452">_controlAllowNegative</span></span> | <span data-ttu-id="b03d2-453">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-453">boolean</span></span> | <span data-ttu-id="b03d2-454">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-454">True</span></span> | <span data-ttu-id="b03d2-455">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-455">The control allow negative</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-456">Return Value</span></span> 
<span data-ttu-id="b03d2-457">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-457">The control allow negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="b03d2-458">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="b03d2-458">Method controlMaxLength</span></span> 
<span data-ttu-id="b03d2-459">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-459">Gets or sets the control max length</span></span>

     public int controlMaxLength ([int _controlMaxLength]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-460">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-460">Parameters</span></span>

| <span data-ttu-id="b03d2-461">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-461">Parameter name</span></span> |  <span data-ttu-id="b03d2-462">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-462">Parameter type</span></span> | <span data-ttu-id="b03d2-463">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-463">Optional</span></span> | <span data-ttu-id="b03d2-464">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-464">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-465">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="b03d2-465">_controlMaxLength</span></span> | <span data-ttu-id="b03d2-466">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-466">int</span></span> | <span data-ttu-id="b03d2-467">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-467">True</span></span> | <span data-ttu-id="b03d2-468">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="b03d2-468">The control max length</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-469">Return Value</span></span> 
<span data-ttu-id="b03d2-470">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="b03d2-470">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="b03d2-471">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-471">Method getProperty</span></span> 
<span data-ttu-id="b03d2-472">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-472">Gets the control property referenced by the key</span></span>

     public anytype getProperty (str _key) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-473">Parameters</span></span>

| <span data-ttu-id="b03d2-474">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-474">Parameter name</span></span> |  <span data-ttu-id="b03d2-475">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-475">Parameter type</span></span> | <span data-ttu-id="b03d2-476">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-476">Optional</span></span> | <span data-ttu-id="b03d2-477">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-477">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-478">_key</span><span class="sxs-lookup"><span data-stu-id="b03d2-478">_key</span></span> | <span data-ttu-id="b03d2-479">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-479">str</span></span> | <span data-ttu-id="b03d2-480">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-480">False</span></span> | <span data-ttu-id="b03d2-481">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="b03d2-481">The name of the control property</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-482">Return Value</span></span> 
<span data-ttu-id="b03d2-483">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="b03d2-483">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="b03d2-484">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-484">Method setProperty</span></span> 
<span data-ttu-id="b03d2-485">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-485">Sets the control property referenced by the key</span></span>

     public void setProperty (str _key, anytype _value) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-486">Parameters</span></span>

| <span data-ttu-id="b03d2-487">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-487">Parameter name</span></span> |  <span data-ttu-id="b03d2-488">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-488">Parameter type</span></span> | <span data-ttu-id="b03d2-489">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-489">Optional</span></span> | <span data-ttu-id="b03d2-490">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-490">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-491">_key</span><span class="sxs-lookup"><span data-stu-id="b03d2-491">_key</span></span> | <span data-ttu-id="b03d2-492">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-492">str</span></span> | <span data-ttu-id="b03d2-493">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-493">False</span></span> | <span data-ttu-id="b03d2-494">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="b03d2-494">The name of the control property</span></span>
| <span data-ttu-id="b03d2-495">_value</span><span class="sxs-lookup"><span data-stu-id="b03d2-495">_value</span></span> | <span data-ttu-id="b03d2-496">anytype</span><span class="sxs-lookup"><span data-stu-id="b03d2-496">anytype</span></span> | <span data-ttu-id="b03d2-497">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-497">False</span></span> | <span data-ttu-id="b03d2-498">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-498">The value of the control property</span></span>


## <a name="class-sysappentityattribute"></a><span data-ttu-id="b03d2-499">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-499">Class SysAppEntityAttribute</span></span> 
<span data-ttu-id="b03d2-500">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-500">SysAppEntityAttribute used for decorating data contract entitities</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-501">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-501">Methods</span></span>

| <span data-ttu-id="b03d2-502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-502">Method name</span></span> | <span data-ttu-id="b03d2-503">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-503">Returns</span></span> | <span data-ttu-id="b03d2-504">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-504">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-505">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-505">new</span></span> | <span data-ttu-id="b03d2-506">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-506">void</span></span> | <span data-ttu-id="b03d2-507">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-507">Constructor</span></span> |
| <span data-ttu-id="b03d2-508">名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-508">name</span></span> | <span data-ttu-id="b03d2-509">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-509">str</span></span> | <span data-ttu-id="b03d2-510">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-510">Gets the name of the entity</span></span> |
| <span data-ttu-id="b03d2-511">entityKey</span><span class="sxs-lookup"><span data-stu-id="b03d2-511">entityKey</span></span> | <span data-ttu-id="b03d2-512">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-512">str</span></span> | <span data-ttu-id="b03d2-513">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-513">Gets the entity key</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-514">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-514">Method new</span></span> 
<span data-ttu-id="b03d2-515">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-515">Constructor</span></span>

     public void new (str _name, str _entityKey) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-516">Parameters</span></span>

| <span data-ttu-id="b03d2-517">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-517">Parameter name</span></span> |  <span data-ttu-id="b03d2-518">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-518">Parameter type</span></span> | <span data-ttu-id="b03d2-519">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-519">Optional</span></span> | <span data-ttu-id="b03d2-520">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-520">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-521">_name</span><span class="sxs-lookup"><span data-stu-id="b03d2-521">_name</span></span> | <span data-ttu-id="b03d2-522">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-522">str</span></span> | <span data-ttu-id="b03d2-523">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-523">False</span></span> | <span data-ttu-id="b03d2-524">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-524">Entity name</span></span>
| <span data-ttu-id="b03d2-525">_entityKey</span><span class="sxs-lookup"><span data-stu-id="b03d2-525">_entityKey</span></span> | <span data-ttu-id="b03d2-526">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-526">str</span></span> | <span data-ttu-id="b03d2-527">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-527">False</span></span> | <span data-ttu-id="b03d2-528">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-528">Name of the entity's key</span></span>


### <a name="method-name"></a><span data-ttu-id="b03d2-529">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-529">Method name</span></span> 
<span data-ttu-id="b03d2-530">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-530">Gets the name of the entity</span></span>

     public str name () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-531">Return Value</span></span> 
<span data-ttu-id="b03d2-532">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-532">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="b03d2-533">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="b03d2-533">Method entityKey</span></span> 
<span data-ttu-id="b03d2-534">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-534">Gets the entity key</span></span>

     public str entityKey () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-535">Return Value</span></span> 
<span data-ttu-id="b03d2-536">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="b03d2-536">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="b03d2-537">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-537">Class SysAppEntityContext</span></span> 
<span data-ttu-id="b03d2-538">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-538">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-539">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-539">Methods</span></span>

| <span data-ttu-id="b03d2-540">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-540">Method name</span></span> | <span data-ttu-id="b03d2-541">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-541">Returns</span></span> | <span data-ttu-id="b03d2-542">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-542">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-543">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="b03d2-543">constructFromParams</span></span> | <span data-ttu-id="b03d2-544">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-544">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-545">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-545">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="b03d2-546">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="b03d2-546">constructFromBuffer</span></span> | <span data-ttu-id="b03d2-547">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-547">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-548">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="b03d2-548">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="b03d2-549">entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-549">entityName</span></span> | <span data-ttu-id="b03d2-550">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-550">str</span></span> | <span data-ttu-id="b03d2-551">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-551">Entity name on which filter applies</span></span> |
| <span data-ttu-id="b03d2-552">entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-552">entityId</span></span> | <span data-ttu-id="b03d2-553">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-553">str</span></span> | <span data-ttu-id="b03d2-554">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-554">Field value on which filter applies</span></span> |


### <a name="method-constructfromparams"></a><span data-ttu-id="b03d2-555">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="b03d2-555">Method constructFromParams</span></span> 
<span data-ttu-id="b03d2-556">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-556">Constructs SysAppEntityContext from entityName and entityId</span></span>

     public SysAppEntityContext constructFromParams (str _entityName, str _entityId) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-557">Parameters</span></span>

| <span data-ttu-id="b03d2-558">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-558">Parameter name</span></span> |  <span data-ttu-id="b03d2-559">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-559">Parameter type</span></span> | <span data-ttu-id="b03d2-560">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-560">Optional</span></span> | <span data-ttu-id="b03d2-561">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-561">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-562">_entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-562">_entityName</span></span> | <span data-ttu-id="b03d2-563">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-563">str</span></span> | <span data-ttu-id="b03d2-564">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-564">False</span></span> | <span data-ttu-id="b03d2-565">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-565">Entity name</span></span>
| <span data-ttu-id="b03d2-566">_entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-566">_entityId</span></span> | <span data-ttu-id="b03d2-567">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-567">str</span></span> | <span data-ttu-id="b03d2-568">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-568">False</span></span> | <span data-ttu-id="b03d2-569">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-569">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-570">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-570">Return Value</span></span> 
<span data-ttu-id="b03d2-571">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="b03d2-571">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="b03d2-572">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="b03d2-572">Method constructFromBuffer</span></span> 
<span data-ttu-id="b03d2-573">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="b03d2-573">Constructs SysAppEntityContext from table buffer</span></span>

     public SysAppEntityContext constructFromBuffer (Common _tableBuffer) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-574">Parameters</span></span>

| <span data-ttu-id="b03d2-575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-575">Parameter name</span></span> |  <span data-ttu-id="b03d2-576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-576">Parameter type</span></span> | <span data-ttu-id="b03d2-577">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-577">Optional</span></span> | <span data-ttu-id="b03d2-578">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-579">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="b03d2-579">_tableBuffer</span></span> | <span data-ttu-id="b03d2-580">共通</span><span class="sxs-lookup"><span data-stu-id="b03d2-580">Common</span></span> | <span data-ttu-id="b03d2-581">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-581">False</span></span> | <span data-ttu-id="b03d2-582">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="b03d2-582">table buffer forming the entity</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-583">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-583">Return Value</span></span> 
<span data-ttu-id="b03d2-584">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="b03d2-584">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="b03d2-585">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-585">Method entityName</span></span> 
<span data-ttu-id="b03d2-586">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-586">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-587">Parameters</span></span>

| <span data-ttu-id="b03d2-588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-588">Parameter name</span></span> |  <span data-ttu-id="b03d2-589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-589">Parameter type</span></span> | <span data-ttu-id="b03d2-590">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-590">Optional</span></span> | <span data-ttu-id="b03d2-591">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-592">_entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-592">_entityName</span></span> | <span data-ttu-id="b03d2-593">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-593">str</span></span> | <span data-ttu-id="b03d2-594">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-594">True</span></span> | <span data-ttu-id="b03d2-595">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-595">Entity name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-596">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-596">Return Value</span></span> 
<span data-ttu-id="b03d2-597">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-597">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="b03d2-598">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-598">Method entityId</span></span> 
<span data-ttu-id="b03d2-599">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-599">Field value on which filter applies</span></span>

     public str entityId ([str _entityId]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-600">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-600">Parameters</span></span>

| <span data-ttu-id="b03d2-601">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-601">Parameter name</span></span> |  <span data-ttu-id="b03d2-602">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-602">Parameter type</span></span> | <span data-ttu-id="b03d2-603">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-603">Optional</span></span> | <span data-ttu-id="b03d2-604">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-604">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-605">_entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-605">_entityId</span></span> | <span data-ttu-id="b03d2-606">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-606">str</span></span> | <span data-ttu-id="b03d2-607">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-607">True</span></span> | <span data-ttu-id="b03d2-608">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-608">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-609">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-609">Return Value</span></span> 
<span data-ttu-id="b03d2-610">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-610">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="b03d2-611">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-611">Class SysAppFieldAttribute</span></span> 
<span data-ttu-id="b03d2-612">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-612">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-613">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-613">Methods</span></span>

| <span data-ttu-id="b03d2-614">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-614">Method name</span></span> | <span data-ttu-id="b03d2-615">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-615">Returns</span></span> | <span data-ttu-id="b03d2-616">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-616">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-617">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-617">new</span></span> | <span data-ttu-id="b03d2-618">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-618">void</span></span> | <span data-ttu-id="b03d2-619">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-619">Creates a new instance of SysAppFieldAttribute class</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-620">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-620">Method new</span></span> 
<span data-ttu-id="b03d2-621">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-621">Creates a new instance of SysAppFieldAttribute class</span></span>

     public void new (str _fieldName, str _label) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-622">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-622">Parameters</span></span>

| <span data-ttu-id="b03d2-623">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-623">Parameter name</span></span> |  <span data-ttu-id="b03d2-624">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-624">Parameter type</span></span> | <span data-ttu-id="b03d2-625">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-625">Optional</span></span> | <span data-ttu-id="b03d2-626">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-626">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-627">_fieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-627">_fieldName</span></span> | <span data-ttu-id="b03d2-628">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-628">str</span></span> | <span data-ttu-id="b03d2-629">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-629">False</span></span> | <span data-ttu-id="b03d2-630">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-630">Entity field name with which control is bound</span></span>
| <span data-ttu-id="b03d2-631">_label</span><span class="sxs-lookup"><span data-stu-id="b03d2-631">_label</span></span> | <span data-ttu-id="b03d2-632">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-632">str</span></span> | <span data-ttu-id="b03d2-633">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-633">False</span></span> | <span data-ttu-id="b03d2-634">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-634">Control label</span></span>


## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="b03d2-635">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="b03d2-635">Class SysAppFieldMultiSelectHelper</span></span> 
<span data-ttu-id="b03d2-636">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="b03d2-636">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-637">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-637">Methods</span></span>

| <span data-ttu-id="b03d2-638">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-638">Method name</span></span> | <span data-ttu-id="b03d2-639">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-639">Returns</span></span> | <span data-ttu-id="b03d2-640">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-640">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-641">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-641">new</span></span> | <span data-ttu-id="b03d2-642">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-642">void</span></span> | <span data-ttu-id="b03d2-643">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-643">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="b03d2-644">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="b03d2-644">getSelectedRecIds</span></span> | <span data-ttu-id="b03d2-645">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-645">container</span></span> | <span data-ttu-id="b03d2-646">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-646">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="b03d2-647">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-647">getSelectedValues</span></span> | <span data-ttu-id="b03d2-648">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-648">container</span></span> | <span data-ttu-id="b03d2-649">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-649">Returns a container of selected values</span></span> |
| <span data-ttu-id="b03d2-650">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="b03d2-650">getSelectedRecords</span></span> | <span data-ttu-id="b03d2-651">共通</span><span class="sxs-lookup"><span data-stu-id="b03d2-651">Common</span></span> | <span data-ttu-id="b03d2-652">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-652">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="b03d2-653">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-653">The buffer is marked as temp..</span></span>  <span data-ttu-id="b03d2-654">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-654">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="b03d2-655">setControlValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-655">setControlValue</span></span> | <span data-ttu-id="b03d2-656">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-656">void</span></span> | <span data-ttu-id="b03d2-657">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="b03d2-657">A setter to set the multi select control value</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-658">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-658">Method new</span></span> 
<span data-ttu-id="b03d2-659">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-659">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

     public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-660">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-660">Parameters</span></span>

| <span data-ttu-id="b03d2-661">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-661">Parameter name</span></span> |  <span data-ttu-id="b03d2-662">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-662">Parameter type</span></span> | <span data-ttu-id="b03d2-663">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-663">Optional</span></span> | <span data-ttu-id="b03d2-664">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-664">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-665">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="b03d2-665">_multiSelectTableId</span></span> | <span data-ttu-id="b03d2-666">TableId</span><span class="sxs-lookup"><span data-stu-id="b03d2-666">TableId</span></span> | <span data-ttu-id="b03d2-667">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-667">False</span></span> | <span data-ttu-id="b03d2-668">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="b03d2-668">The backing tableId for the field</span></span>
| <span data-ttu-id="b03d2-669">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="b03d2-669">_valueFieldId</span></span> | <span data-ttu-id="b03d2-670">FieldId</span><span class="sxs-lookup"><span data-stu-id="b03d2-670">FieldId</span></span> | <span data-ttu-id="b03d2-671">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-671">False</span></span> | <span data-ttu-id="b03d2-672">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="b03d2-672">The fieldId for the field which will be shown in the multi select control</span></span>
| <span data-ttu-id="b03d2-673">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-673">_multiSelectControl</span></span> | <span data-ttu-id="b03d2-674">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-674">FormStringControl</span></span> | <span data-ttu-id="b03d2-675">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-675">False</span></span> | <span data-ttu-id="b03d2-676">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="b03d2-676">The string control that will be the multi select control</span></span>


### <a name="method-getselectedrecids"></a><span data-ttu-id="b03d2-677">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="b03d2-677">Method getSelectedRecIds</span></span> 
<span data-ttu-id="b03d2-678">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-678">Returns a container of recIds of the records that were selected</span></span>

     public container getSelectedRecIds () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-679">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-679">Return Value</span></span> 
<span data-ttu-id="b03d2-680">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-680">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="b03d2-681">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-681">Method getSelectedValues</span></span> 
<span data-ttu-id="b03d2-682">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-682">Returns a container of selected values</span></span>

     public container getSelectedValues () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-683">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-683">Return Value</span></span> 
<span data-ttu-id="b03d2-684">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-684">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="b03d2-685">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="b03d2-685">Method getSelectedRecords</span></span> 
<span data-ttu-id="b03d2-686">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-686">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="b03d2-687">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-687">The buffer is marked as temp..</span></span>  <span data-ttu-id="b03d2-688">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-688">Later a while-Select can be used to iterate through all the records</span></span>

     public Common getSelectedRecords () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-689">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-689">Return Value</span></span> 
<span data-ttu-id="b03d2-690">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="b03d2-690">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="b03d2-691">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-691">Method setControlValue</span></span> 
<span data-ttu-id="b03d2-692">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="b03d2-692">A setter to set the multi select control value</span></span>

     public void setControlValue (str _value) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-693">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-693">Parameters</span></span>

| <span data-ttu-id="b03d2-694">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-694">Parameter name</span></span> |  <span data-ttu-id="b03d2-695">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-695">Parameter type</span></span> | <span data-ttu-id="b03d2-696">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-696">Optional</span></span> | <span data-ttu-id="b03d2-697">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-697">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-698">_value</span><span class="sxs-lookup"><span data-stu-id="b03d2-698">_value</span></span> | <span data-ttu-id="b03d2-699">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-699">str</span></span> | <span data-ttu-id="b03d2-700">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-700">False</span></span> | <span data-ttu-id="b03d2-701">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-701">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>


## <a name="class-sysappfiltercontext"></a><span data-ttu-id="b03d2-702">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-702">Class SysAppFilterContext</span></span> 
<span data-ttu-id="b03d2-703">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-703">SysAppFilterContext class which holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-704">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-704">Methods</span></span>

| <span data-ttu-id="b03d2-705">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-705">Method name</span></span> | <span data-ttu-id="b03d2-706">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-706">Returns</span></span> | <span data-ttu-id="b03d2-707">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-707">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-708">entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-708">entityName</span></span> | <span data-ttu-id="b03d2-709">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-709">str</span></span> | <span data-ttu-id="b03d2-710">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-710">Entity name on which filter applies</span></span> |
| <span data-ttu-id="b03d2-711">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-711">filterFieldName</span></span> | <span data-ttu-id="b03d2-712">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-712">str</span></span> | <span data-ttu-id="b03d2-713">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-713">Field name on which filter applies</span></span> |
| <span data-ttu-id="b03d2-714">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="b03d2-714">filterFieldValueList</span></span> | <span data-ttu-id="b03d2-715">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-715">List</span></span> | <span data-ttu-id="b03d2-716">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-716">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="b03d2-717">演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-717">operator</span></span> | <span data-ttu-id="b03d2-718">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-718">str</span></span> | <span data-ttu-id="b03d2-719">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-719">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="b03d2-720">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-720">addFilterFieldValue</span></span> | <span data-ttu-id="b03d2-721">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-721">void</span></span> | <span data-ttu-id="b03d2-722">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-722">Adds filter field value</span></span> |


### <a name="method-entityname"></a><span data-ttu-id="b03d2-723">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-723">Method entityName</span></span> 
<span data-ttu-id="b03d2-724">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-724">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-725">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-725">Parameters</span></span>

| <span data-ttu-id="b03d2-726">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-726">Parameter name</span></span> |  <span data-ttu-id="b03d2-727">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-727">Parameter type</span></span> | <span data-ttu-id="b03d2-728">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-728">Optional</span></span> | <span data-ttu-id="b03d2-729">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-729">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-730">_entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-730">_entityName</span></span> | <span data-ttu-id="b03d2-731">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-731">str</span></span> | <span data-ttu-id="b03d2-732">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-732">True</span></span> | <span data-ttu-id="b03d2-733">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-733">Entity name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-734">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-734">Return Value</span></span> 
<span data-ttu-id="b03d2-735">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-735">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="b03d2-736">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-736">Method filterFieldName</span></span> 
<span data-ttu-id="b03d2-737">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-737">Field name on which filter applies</span></span>

     public str filterFieldName ([str _filterFieldName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-738">Parameters</span></span>

| <span data-ttu-id="b03d2-739">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-739">Parameter name</span></span> |  <span data-ttu-id="b03d2-740">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-740">Parameter type</span></span> | <span data-ttu-id="b03d2-741">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-741">Optional</span></span> | <span data-ttu-id="b03d2-742">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-742">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-743">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-743">_filterFieldName</span></span> | <span data-ttu-id="b03d2-744">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-744">str</span></span> | <span data-ttu-id="b03d2-745">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-745">True</span></span> | <span data-ttu-id="b03d2-746">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-746">Field name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-747">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-747">Return Value</span></span> 
<span data-ttu-id="b03d2-748">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-748">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="b03d2-749">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="b03d2-749">Method filterFieldValueList</span></span> 
<span data-ttu-id="b03d2-750">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-750">Gets the list of filter field values based on which filter happens</span></span>

     public List filterFieldValueList () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-751">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-751">Return Value</span></span> 
<span data-ttu-id="b03d2-752">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-752">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="b03d2-753">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="b03d2-753">Method operator</span></span> 
<span data-ttu-id="b03d2-754">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-754">Operator based on which result will be fetched</span></span>

     public str operator ([str _operator]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-755">Parameters</span></span>

| <span data-ttu-id="b03d2-756">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-756">Parameter name</span></span> |  <span data-ttu-id="b03d2-757">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-757">Parameter type</span></span> | <span data-ttu-id="b03d2-758">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-758">Optional</span></span> | <span data-ttu-id="b03d2-759">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-759">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-760">_operator</span><span class="sxs-lookup"><span data-stu-id="b03d2-760">_operator</span></span> | <span data-ttu-id="b03d2-761">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-761">str</span></span> | <span data-ttu-id="b03d2-762">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-762">True</span></span> | <span data-ttu-id="b03d2-763">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-763">Operator based on which result will be fetched</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-764">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-764">Return Value</span></span> 
<span data-ttu-id="b03d2-765">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-765">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="b03d2-766">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-766">Method addFilterFieldValue</span></span> 
<span data-ttu-id="b03d2-767">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-767">Adds filter field value</span></span>

     public void addFilterFieldValue ( _filterFieldValueList) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-768">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-768">Parameters</span></span>

| <span data-ttu-id="b03d2-769">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-769">Parameter name</span></span> |  <span data-ttu-id="b03d2-770">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-770">Parameter type</span></span> | <span data-ttu-id="b03d2-771">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-771">Optional</span></span> | <span data-ttu-id="b03d2-772">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-772">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-773">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="b03d2-773">_filterFieldValueList</span></span> |  | <span data-ttu-id="b03d2-774">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-774">False</span></span> | <span data-ttu-id="b03d2-775">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-775">Filter field values based on which filter happens</span></span>


## <a name="class-sysapplookupattribute"></a><span data-ttu-id="b03d2-776">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-776">Class SysAppLookUpAttribute</span></span> 
<span data-ttu-id="b03d2-777">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-777">SysAppPageAttribute used for decorating pages that is also lookup page</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-778">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-778">Methods</span></span>

| <span data-ttu-id="b03d2-779">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-779">Method name</span></span> | <span data-ttu-id="b03d2-780">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-780">Returns</span></span> | <span data-ttu-id="b03d2-781">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-781">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-782">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-782">new</span></span> | <span data-ttu-id="b03d2-783">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-783">void</span></span> | <span data-ttu-id="b03d2-784">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-784">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="b03d2-785">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-785">displayFieldName</span></span> | <span data-ttu-id="b03d2-786">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-786">str</span></span> | <span data-ttu-id="b03d2-787">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-787">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="b03d2-788">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-788">valueFieldName</span></span> | <span data-ttu-id="b03d2-789">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-789">str</span></span> | <span data-ttu-id="b03d2-790">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-790">Gets the value field name of lookup control</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-791">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-791">Method new</span></span> 
<span data-ttu-id="b03d2-792">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-792">Creates a new instance of SysAppLookUpAttribute class</span></span>

     public void new (str _displayFieldName, str _valueFieldName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-793">Parameters</span></span>

| <span data-ttu-id="b03d2-794">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-794">Parameter name</span></span> |  <span data-ttu-id="b03d2-795">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-795">Parameter type</span></span> | <span data-ttu-id="b03d2-796">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-796">Optional</span></span> | <span data-ttu-id="b03d2-797">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-797">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-798">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-798">_displayFieldName</span></span> | <span data-ttu-id="b03d2-799">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-799">str</span></span> | <span data-ttu-id="b03d2-800">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-800">False</span></span> | <span data-ttu-id="b03d2-801">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="b03d2-801">Lookup display field.</span></span> <span data-ttu-id="b03d2-802">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-802">Name of any control of lookup page</span></span>
| <span data-ttu-id="b03d2-803">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-803">_valueFieldName</span></span> | <span data-ttu-id="b03d2-804">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-804">str</span></span> | <span data-ttu-id="b03d2-805">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-805">False</span></span> | <span data-ttu-id="b03d2-806">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="b03d2-806">Lookup value field.</span></span> <span data-ttu-id="b03d2-807">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-807">Name of control formed by root data contract constructing lookup page</span></span>


### <a name="method-displayfieldname"></a><span data-ttu-id="b03d2-808">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-808">Method displayFieldName</span></span> 
<span data-ttu-id="b03d2-809">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-809">Gets the display field name of lookup control</span></span>

     public str displayFieldName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-810">Return Value</span></span> 
<span data-ttu-id="b03d2-811">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-811">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="b03d2-812">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-812">Method valueFieldName</span></span> 
<span data-ttu-id="b03d2-813">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-813">Gets the value field name of lookup control</span></span>

     public str valueFieldName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-814">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-814">Return Value</span></span> 
<span data-ttu-id="b03d2-815">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="b03d2-815">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="b03d2-816">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-816">Class SysAppLookupFieldAttribute</span></span> 
<span data-ttu-id="b03d2-817">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-817">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-818">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-818">Methods</span></span>

| <span data-ttu-id="b03d2-819">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-819">Method name</span></span> | <span data-ttu-id="b03d2-820">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-820">Returns</span></span> | <span data-ttu-id="b03d2-821">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-821">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-822">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-822">new</span></span> | <span data-ttu-id="b03d2-823">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-823">void</span></span> | <span data-ttu-id="b03d2-824">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-824">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="b03d2-825">entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-825">entityName</span></span> | <span data-ttu-id="b03d2-826">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-826">str</span></span> | <span data-ttu-id="b03d2-827">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-827">Gets the name of the entity with which lookup page is related</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-828">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-828">Method new</span></span> 
<span data-ttu-id="b03d2-829">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-829">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

     public void new ( _name) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-830">Parameters</span></span>

| <span data-ttu-id="b03d2-831">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-831">Parameter name</span></span> |  <span data-ttu-id="b03d2-832">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-832">Parameter type</span></span> | <span data-ttu-id="b03d2-833">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-833">Optional</span></span> | <span data-ttu-id="b03d2-834">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-834">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-835">_name</span><span class="sxs-lookup"><span data-stu-id="b03d2-835">_name</span></span> |  | <span data-ttu-id="b03d2-836">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-836">False</span></span> | <span data-ttu-id="b03d2-837">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-837">Name of the entity with which lookup page is related</span></span>


### <a name="method-entityname"></a><span data-ttu-id="b03d2-838">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-838">Method entityName</span></span> 
<span data-ttu-id="b03d2-839">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-839">Gets the name of the entity with which lookup page is related</span></span>

     public str entityName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-840">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-840">Return Value</span></span> 
<span data-ttu-id="b03d2-841">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-841">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="b03d2-842">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-842">Class SysAppPageAttribute</span></span> 
<span data-ttu-id="b03d2-843">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-843">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-844">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-844">Methods</span></span>

| <span data-ttu-id="b03d2-845">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-845">Method name</span></span> | <span data-ttu-id="b03d2-846">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-846">Returns</span></span> | <span data-ttu-id="b03d2-847">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-847">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-848">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-848">new</span></span> | <span data-ttu-id="b03d2-849">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-849">void</span></span> | <span data-ttu-id="b03d2-850">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-850">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="b03d2-851">pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-851">pageTitle</span></span> | <span data-ttu-id="b03d2-852">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-852">str</span></span> | <span data-ttu-id="b03d2-853">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-853">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="b03d2-854">pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-854">pageDescription</span></span> | <span data-ttu-id="b03d2-855">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-855">str</span></span> | <span data-ttu-id="b03d2-856">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-856">Gets the Page Description</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-857">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-857">Method new</span></span> 
<span data-ttu-id="b03d2-858">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-858">Creates a new instance of SysAppPageAttribute class</span></span>

     public void new ([str _pageTitle], [str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-859">Parameters</span></span>

| <span data-ttu-id="b03d2-860">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-860">Parameter name</span></span> |  <span data-ttu-id="b03d2-861">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-861">Parameter type</span></span> | <span data-ttu-id="b03d2-862">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-862">Optional</span></span> | <span data-ttu-id="b03d2-863">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-863">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-864">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-864">_pageTitle</span></span> | <span data-ttu-id="b03d2-865">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-865">str</span></span> | <span data-ttu-id="b03d2-866">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-866">True</span></span> | <span data-ttu-id="b03d2-867">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-867">The page title</span></span>
| <span data-ttu-id="b03d2-868">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-868">_pageDescription</span></span> | <span data-ttu-id="b03d2-869">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-869">str</span></span> | <span data-ttu-id="b03d2-870">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-870">True</span></span> | <span data-ttu-id="b03d2-871">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-871">The page description</span></span>


### <a name="method-pagetitle"></a><span data-ttu-id="b03d2-872">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-872">Method pageTitle</span></span> 
<span data-ttu-id="b03d2-873">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-873">Gets the Page Title of the page</span></span>

     public str pageTitle () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-874">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-874">Return Value</span></span> 
<span data-ttu-id="b03d2-875">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-875">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="b03d2-876">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-876">Method pageDescription</span></span> 
<span data-ttu-id="b03d2-877">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-877">Gets the Page Description</span></span>

     public str pageDescription () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-878">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-878">Return Value</span></span> 
<span data-ttu-id="b03d2-879">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-879">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="b03d2-880">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-880">Class SysAppPageMetadata</span></span> 
<span data-ttu-id="b03d2-881">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-881">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-882">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-882">Methods</span></span>

| <span data-ttu-id="b03d2-883">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-883">Method name</span></span> | <span data-ttu-id="b03d2-884">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-884">Returns</span></span> | <span data-ttu-id="b03d2-885">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-885">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-886">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-886">new</span></span> | <span data-ttu-id="b03d2-887">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-887">void</span></span> |  |
| <span data-ttu-id="b03d2-888">getPageName</span><span class="sxs-lookup"><span data-stu-id="b03d2-888">getPageName</span></span> | <span data-ttu-id="b03d2-889">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-889">str</span></span> | <span data-ttu-id="b03d2-890">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-890">Returns the page name</span></span> |
| <span data-ttu-id="b03d2-891">pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-891">pageTitle</span></span> | <span data-ttu-id="b03d2-892">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-892">str</span></span> | <span data-ttu-id="b03d2-893">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-893">Gets and sets the page title</span></span> |
| <span data-ttu-id="b03d2-894">pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-894">pageDescription</span></span> | <span data-ttu-id="b03d2-895">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-895">str</span></span> | <span data-ttu-id="b03d2-896">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-896">Gets or sets the page description</span></span> |
| <span data-ttu-id="b03d2-897">pageHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-897">pageHidden</span></span> | <span data-ttu-id="b03d2-898">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-898">boolean</span></span> | <span data-ttu-id="b03d2-899">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-899">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="b03d2-900">pageOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-900">pageOrder</span></span> | <span data-ttu-id="b03d2-901">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-901">int</span></span> | <span data-ttu-id="b03d2-902">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-902">Gets or sets the page order</span></span> |
| <span data-ttu-id="b03d2-903">getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-903">getControl</span></span> | <span data-ttu-id="b03d2-904">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-904">SysAppControlMetadata</span></span> | <span data-ttu-id="b03d2-905">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-905">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="b03d2-906">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-906">getControlEnumerator</span></span> | <span data-ttu-id="b03d2-907">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-907">MapEnumerator</span></span> | <span data-ttu-id="b03d2-908">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-908">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="b03d2-909">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-909">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-910">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-911">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-911">Parameters</span></span>

| <span data-ttu-id="b03d2-912">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-912">Parameter name</span></span> |  <span data-ttu-id="b03d2-913">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-913">Parameter type</span></span> | <span data-ttu-id="b03d2-914">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-914">Optional</span></span> | <span data-ttu-id="b03d2-915">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-915">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-916">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-916">_pageMetadata</span></span> | <span data-ttu-id="b03d2-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="b03d2-918">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-918">False</span></span> | 


### <a name="method-getpagename"></a><span data-ttu-id="b03d2-919">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="b03d2-919">Method getPageName</span></span> 
<span data-ttu-id="b03d2-920">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-920">Returns the page name</span></span>

     public str getPageName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-921">Return Value</span></span> 
<span data-ttu-id="b03d2-922">ページ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-922">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="b03d2-923">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-923">Method pageTitle</span></span> 
<span data-ttu-id="b03d2-924">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-924">Gets and sets the page title</span></span>

     public str pageTitle ([str _pageTitle]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-925">Parameters</span></span>

| <span data-ttu-id="b03d2-926">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-926">Parameter name</span></span> |  <span data-ttu-id="b03d2-927">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-927">Parameter type</span></span> | <span data-ttu-id="b03d2-928">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-928">Optional</span></span> | <span data-ttu-id="b03d2-929">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-929">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-930">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-930">_pageTitle</span></span> | <span data-ttu-id="b03d2-931">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-931">str</span></span> | <span data-ttu-id="b03d2-932">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-932">True</span></span> | <span data-ttu-id="b03d2-933">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-933">The page title</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-934">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-934">Return Value</span></span> 
<span data-ttu-id="b03d2-935">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-935">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="b03d2-936">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-936">Method pageDescription</span></span> 
<span data-ttu-id="b03d2-937">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-937">Gets or sets the page description</span></span>

     public str pageDescription ([str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-938">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-938">Parameters</span></span>

| <span data-ttu-id="b03d2-939">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-939">Parameter name</span></span> |  <span data-ttu-id="b03d2-940">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-940">Parameter type</span></span> | <span data-ttu-id="b03d2-941">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-941">Optional</span></span> | <span data-ttu-id="b03d2-942">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-942">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-943">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-943">_pageDescription</span></span> | <span data-ttu-id="b03d2-944">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-944">str</span></span> | <span data-ttu-id="b03d2-945">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-945">True</span></span> | <span data-ttu-id="b03d2-946">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-946">The page description</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-947">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-947">Return Value</span></span> 
<span data-ttu-id="b03d2-948">ページの説明></span><span class="sxs-lookup"><span data-stu-id="b03d2-948">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="b03d2-949">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-949">Method pageHidden</span></span> 
<span data-ttu-id="b03d2-950">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-950">Gets and sets whether the page is hidden in the workspace</span></span>

     public boolean pageHidden ([boolean _pageHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-951">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-951">Parameters</span></span>

| <span data-ttu-id="b03d2-952">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-952">Parameter name</span></span> |  <span data-ttu-id="b03d2-953">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-953">Parameter type</span></span> | <span data-ttu-id="b03d2-954">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-954">Optional</span></span> | <span data-ttu-id="b03d2-955">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-955">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-956">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-956">_pageHidden</span></span> | <span data-ttu-id="b03d2-957">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-957">boolean</span></span> | <span data-ttu-id="b03d2-958">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-958">True</span></span> | <span data-ttu-id="b03d2-959">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="b03d2-959">page hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-960">Return Value</span></span> 
<span data-ttu-id="b03d2-961">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="b03d2-961">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="b03d2-962">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-962">Method pageOrder</span></span> 
<span data-ttu-id="b03d2-963">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-963">Gets or sets the page order</span></span>

     public int pageOrder ([int _pageOrder]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-964">Parameters</span></span>

| <span data-ttu-id="b03d2-965">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-965">Parameter name</span></span> |  <span data-ttu-id="b03d2-966">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-966">Parameter type</span></span> | <span data-ttu-id="b03d2-967">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-967">Optional</span></span> | <span data-ttu-id="b03d2-968">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-968">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-969">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-969">_pageOrder</span></span> | <span data-ttu-id="b03d2-970">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-970">int</span></span> | <span data-ttu-id="b03d2-971">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-971">True</span></span> | <span data-ttu-id="b03d2-972">ページの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-972">The page order</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-973">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-973">Return Value</span></span> 
<span data-ttu-id="b03d2-974">ページの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-974">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="b03d2-975">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-975">Method getControl</span></span> 
<span data-ttu-id="b03d2-976">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-976">Returns the control on the current page having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-977">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-977">Parameters</span></span>

| <span data-ttu-id="b03d2-978">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-978">Parameter name</span></span> |  <span data-ttu-id="b03d2-979">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-979">Parameter type</span></span> | <span data-ttu-id="b03d2-980">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-980">Optional</span></span> | <span data-ttu-id="b03d2-981">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-981">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-982">_controlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-982">_controlName</span></span> | <span data-ttu-id="b03d2-983">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-983">str</span></span> | <span data-ttu-id="b03d2-984">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-984">False</span></span> | <span data-ttu-id="b03d2-985">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="b03d2-985">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-986">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-986">Return Value</span></span> 
<span data-ttu-id="b03d2-987">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="b03d2-987">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="b03d2-988">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-988">Method getControlEnumerator</span></span> 
<span data-ttu-id="b03d2-989">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-989">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="b03d2-990">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-990">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-991">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-991">Return Value</span></span> 
<span data-ttu-id="b03d2-992">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-992">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="b03d2-993">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-993">Class SysAppProjectionAttribute</span></span> 
<span data-ttu-id="b03d2-994">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-994">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-995">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-995">Methods</span></span>

| <span data-ttu-id="b03d2-996">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-996">Method name</span></span> | <span data-ttu-id="b03d2-997">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-997">Returns</span></span> | <span data-ttu-id="b03d2-998">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-998">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-999">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-999">new</span></span> | <span data-ttu-id="b03d2-1000">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1000">void</span></span> | <span data-ttu-id="b03d2-1001">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1001">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1002">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1002">Method new</span></span> 
<span data-ttu-id="b03d2-1003">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1003">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

     public void new (str _label) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1004">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1004">Parameters</span></span>

| <span data-ttu-id="b03d2-1005">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1005">Parameter name</span></span> |  <span data-ttu-id="b03d2-1006">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1006">Parameter type</span></span> | <span data-ttu-id="b03d2-1007">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1007">Optional</span></span> | <span data-ttu-id="b03d2-1008">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1008">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1009">_label</span><span class="sxs-lookup"><span data-stu-id="b03d2-1009">_label</span></span> | <span data-ttu-id="b03d2-1010">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1010">str</span></span> | <span data-ttu-id="b03d2-1011">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1011">False</span></span> | <span data-ttu-id="b03d2-1012">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1012">Control label</span></span>


## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="b03d2-1013">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1013">Class SysAppRelationalAttribute</span></span> 
<span data-ttu-id="b03d2-1014">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1014">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1015">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1015">Methods</span></span>

| <span data-ttu-id="b03d2-1016">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1016">Method name</span></span> | <span data-ttu-id="b03d2-1017">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1017">Returns</span></span> | <span data-ttu-id="b03d2-1018">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1018">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1019">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1019">new</span></span> | <span data-ttu-id="b03d2-1020">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1020">void</span></span> | <span data-ttu-id="b03d2-1021">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1021">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1022">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1022">Method new</span></span> 
<span data-ttu-id="b03d2-1023">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1023">Constructor</span></span>

     public void new ([str _name]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1024">Parameters</span></span>

| <span data-ttu-id="b03d2-1025">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1025">Parameter name</span></span> |  <span data-ttu-id="b03d2-1026">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1026">Parameter type</span></span> | <span data-ttu-id="b03d2-1027">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1027">Optional</span></span> | <span data-ttu-id="b03d2-1028">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1028">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1029">_name</span><span class="sxs-lookup"><span data-stu-id="b03d2-1029">_name</span></span> | <span data-ttu-id="b03d2-1030">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1030">str</span></span> | <span data-ttu-id="b03d2-1031">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1031">True</span></span> | <span data-ttu-id="b03d2-1032">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1032">Property name of the referenced entity</span></span>


## <a name="class-sysapprequestparams"></a><span data-ttu-id="b03d2-1033">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="b03d2-1033">Class SysAppRequestParams</span></span> 
<span data-ttu-id="b03d2-1034">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1034">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1035">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1035">Methods</span></span>

| <span data-ttu-id="b03d2-1036">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1036">Method name</span></span> | <span data-ttu-id="b03d2-1037">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1037">Returns</span></span> | <span data-ttu-id="b03d2-1038">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1038">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1039">entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1039">entityContext</span></span> | <span data-ttu-id="b03d2-1040">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1040">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-1041">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1041">Entity context of the request</span></span> |
| <span data-ttu-id="b03d2-1042">filterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1042">filterContext</span></span> | <span data-ttu-id="b03d2-1043">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1043">List</span></span> | <span data-ttu-id="b03d2-1044">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1044">List of SysAppFilterContext for filter contexts</span></span> |


### <a name="method-entitycontext"></a><span data-ttu-id="b03d2-1045">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1045">Method entityContext</span></span> 
<span data-ttu-id="b03d2-1046">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1046">Entity context of the request</span></span>

     public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1047">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1047">Parameters</span></span>

| <span data-ttu-id="b03d2-1048">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1048">Parameter name</span></span> |  <span data-ttu-id="b03d2-1049">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1049">Parameter type</span></span> | <span data-ttu-id="b03d2-1050">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1050">Optional</span></span> | <span data-ttu-id="b03d2-1051">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1051">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1052">_entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1052">_entityContext</span></span> | <span data-ttu-id="b03d2-1053">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1053">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-1054">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1054">True</span></span> | <span data-ttu-id="b03d2-1055">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1055">Entity context of the request</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1056">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1056">Return Value</span></span> 
<span data-ttu-id="b03d2-1057">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1057">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="b03d2-1058">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1058">Method filterContext</span></span> 
<span data-ttu-id="b03d2-1059">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1059">List of SysAppFilterContext for filter contexts</span></span>

     public List filterContext ([List _filterContext]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1060">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1060">Parameters</span></span>

| <span data-ttu-id="b03d2-1061">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1061">Parameter name</span></span> |  <span data-ttu-id="b03d2-1062">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1062">Parameter type</span></span> | <span data-ttu-id="b03d2-1063">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1063">Optional</span></span> | <span data-ttu-id="b03d2-1064">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1064">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1065">_filterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1065">_filterContext</span></span> | <span data-ttu-id="b03d2-1066">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1066">List</span></span> | <span data-ttu-id="b03d2-1067">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1067">True</span></span> | <span data-ttu-id="b03d2-1068">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1068">List of SysAppFilterContext for filter contexts of page</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1069">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1069">Return Value</span></span> 
<span data-ttu-id="b03d2-1070">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1070">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="b03d2-1071">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="b03d2-1071">Class SysAppResponse</span></span> 
<span data-ttu-id="b03d2-1072">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1072">SysAppResponse class.</span></span>  <span data-ttu-id="b03d2-1073">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1073">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1074">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1074">Methods</span></span>

| <span data-ttu-id="b03d2-1075">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1075">Method name</span></span> | <span data-ttu-id="b03d2-1076">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1076">Returns</span></span> | <span data-ttu-id="b03d2-1077">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1077">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1078">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1078">new</span></span> | <span data-ttu-id="b03d2-1079">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1079">void</span></span> |  |
| <span data-ttu-id="b03d2-1080">jobId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1080">jobId</span></span> | <span data-ttu-id="b03d2-1081">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1081">str</span></span> | <span data-ttu-id="b03d2-1082">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-1082">Job Id of the request</span></span> |
| <span data-ttu-id="b03d2-1083">データ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1083">data</span></span> | <span data-ttu-id="b03d2-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="b03d2-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="b03d2-1085">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1085">Data of the page</span></span> |
| <span data-ttu-id="b03d2-1086">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="b03d2-1086">failedInAppCall</span></span> | <span data-ttu-id="b03d2-1087">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1087">boolean</span></span> | <span data-ttu-id="b03d2-1088">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1088">Data of the page</span></span> |
| <span data-ttu-id="b03d2-1089">commits</span><span class="sxs-lookup"><span data-stu-id="b03d2-1089">commits</span></span> | <span data-ttu-id="b03d2-1090">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1090">List</span></span> | <span data-ttu-id="b03d2-1091">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1091">Commits after task is completed</span></span> |
| <span data-ttu-id="b03d2-1092">メッセージ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1092">messages</span></span> | <span data-ttu-id="b03d2-1093">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1093">List</span></span> | <span data-ttu-id="b03d2-1094">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-1094">Job Id of the request</span></span> |
| <span data-ttu-id="b03d2-1095">addMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-1095">addMessage</span></span> | <span data-ttu-id="b03d2-1096">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1096">void</span></span> | <span data-ttu-id="b03d2-1097">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-1097">Adds message</span></span> |
| <span data-ttu-id="b03d2-1098">addCommit</span><span class="sxs-lookup"><span data-stu-id="b03d2-1098">addCommit</span></span> | <span data-ttu-id="b03d2-1099">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1099">void</span></span> | <span data-ttu-id="b03d2-1100">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-1100">Adds commits</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1101">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1101">Method new</span></span> 


     public void new () 


### <a name="method-jobid"></a><span data-ttu-id="b03d2-1102">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1102">Method jobId</span></span> 
<span data-ttu-id="b03d2-1103">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-1103">Job Id of the request</span></span>

     public str jobId () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1104">Return Value</span></span> 
<span data-ttu-id="b03d2-1105">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-1105">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="b03d2-1106">メソッド data</span><span class="sxs-lookup"><span data-stu-id="b03d2-1106">Method data</span></span> 
<span data-ttu-id="b03d2-1107">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1107">Data of the page</span></span>

     public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1108">Parameters</span></span>

| <span data-ttu-id="b03d2-1109">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1109">Parameter name</span></span> |  <span data-ttu-id="b03d2-1110">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1110">Parameter type</span></span> | <span data-ttu-id="b03d2-1111">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1111">Optional</span></span> | <span data-ttu-id="b03d2-1112">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1112">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1113">_data</span><span class="sxs-lookup"><span data-stu-id="b03d2-1113">_data</span></span> | <span data-ttu-id="b03d2-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="b03d2-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="b03d2-1115">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1115">True</span></span> | <span data-ttu-id="b03d2-1116">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1116">Data of the page</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1117">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1117">Return Value</span></span> 
<span data-ttu-id="b03d2-1118">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1118">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="b03d2-1119">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="b03d2-1119">Method failedInAppCall</span></span> 
<span data-ttu-id="b03d2-1120">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1120">Data of the page</span></span>

     public boolean failedInAppCall ([boolean _failedInAppCall]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1121">Parameters</span></span>

| <span data-ttu-id="b03d2-1122">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1122">Parameter name</span></span> |  <span data-ttu-id="b03d2-1123">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1123">Parameter type</span></span> | <span data-ttu-id="b03d2-1124">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1124">Optional</span></span> | <span data-ttu-id="b03d2-1125">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1125">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1126">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="b03d2-1126">_failedInAppCall</span></span> | <span data-ttu-id="b03d2-1127">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1127">boolean</span></span> | <span data-ttu-id="b03d2-1128">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1128">True</span></span> | <span data-ttu-id="b03d2-1129">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1129">Sets to true if it fails in calling application code</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1130">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1130">Return Value</span></span> 
<span data-ttu-id="b03d2-1131">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1131">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="b03d2-1132">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="b03d2-1132">Method commits</span></span> 
<span data-ttu-id="b03d2-1133">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1133">Commits after task is completed</span></span>

     public List commits () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1134">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1134">Return Value</span></span> 
<span data-ttu-id="b03d2-1135">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1135">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="b03d2-1136">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="b03d2-1136">Method messages</span></span> 
<span data-ttu-id="b03d2-1137">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-1137">Job Id of the request</span></span>

     public List messages () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1138">Return Value</span></span> 
<span data-ttu-id="b03d2-1139">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1139">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="b03d2-1140">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-1140">Method addMessage</span></span> 
<span data-ttu-id="b03d2-1141">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-1141">Adds message</span></span>

     public void addMessage (SysAppResponseMessage _message) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1142">Parameters</span></span>

| <span data-ttu-id="b03d2-1143">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1143">Parameter name</span></span> |  <span data-ttu-id="b03d2-1144">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1144">Parameter type</span></span> | <span data-ttu-id="b03d2-1145">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1145">Optional</span></span> | <span data-ttu-id="b03d2-1146">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1146">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1147">_message</span><span class="sxs-lookup"><span data-stu-id="b03d2-1147">_message</span></span> | <span data-ttu-id="b03d2-1148">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-1148">SysAppResponseMessage</span></span> | <span data-ttu-id="b03d2-1149">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1149">False</span></span> | <span data-ttu-id="b03d2-1150">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1150">message as SysAppResponseMessage object</span></span>


### <a name="method-addcommit"></a><span data-ttu-id="b03d2-1151">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="b03d2-1151">Method addCommit</span></span> 
<span data-ttu-id="b03d2-1152">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-1152">Adds commits</span></span>

     public void addCommit (SysAppEntityContext _entityContext) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1153">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1153">Parameters</span></span>

| <span data-ttu-id="b03d2-1154">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1154">Parameter name</span></span> |  <span data-ttu-id="b03d2-1155">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1155">Parameter type</span></span> | <span data-ttu-id="b03d2-1156">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1156">Optional</span></span> | <span data-ttu-id="b03d2-1157">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1157">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1158">_entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1158">_entityContext</span></span> | <span data-ttu-id="b03d2-1159">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-1159">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-1160">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1160">False</span></span> | <span data-ttu-id="b03d2-1161">確定済のエンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1161">Entity context containing entity name and entity id of the entity that is committed</span></span>


## <a name="class-sysappresponsemessage"></a><span data-ttu-id="b03d2-1162">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-1162">Class SysAppResponseMessage</span></span> 
<span data-ttu-id="b03d2-1163">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-1163">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1164">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1164">Methods</span></span>

| <span data-ttu-id="b03d2-1165">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1165">Method name</span></span> | <span data-ttu-id="b03d2-1166">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1166">Returns</span></span> | <span data-ttu-id="b03d2-1167">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1167">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1168">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1168">new</span></span> | <span data-ttu-id="b03d2-1169">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1169">void</span></span> | <span data-ttu-id="b03d2-1170">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1170">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="b03d2-1171">テキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1171">text</span></span> | <span data-ttu-id="b03d2-1172">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1172">str</span></span> | <span data-ttu-id="b03d2-1173">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1173">Gets the message text</span></span> |
| <span data-ttu-id="b03d2-1174">タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1174">type</span></span> | <span data-ttu-id="b03d2-1175">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1175">SysAppMessageType</span></span> | <span data-ttu-id="b03d2-1176">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-1176">Gets the message type: info, error , warning</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1177">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1177">Method new</span></span> 
<span data-ttu-id="b03d2-1178">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1178">Creates a new instance of SysAppResponseMessage class</span></span>

     public void new (str _text, [SysAppMessageType _type]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1179">Parameters</span></span>

| <span data-ttu-id="b03d2-1180">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1180">Parameter name</span></span> |  <span data-ttu-id="b03d2-1181">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1181">Parameter type</span></span> | <span data-ttu-id="b03d2-1182">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1182">Optional</span></span> | <span data-ttu-id="b03d2-1183">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1183">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1184">_text</span><span class="sxs-lookup"><span data-stu-id="b03d2-1184">_text</span></span> | <span data-ttu-id="b03d2-1185">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1185">str</span></span> | <span data-ttu-id="b03d2-1186">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1186">False</span></span> | <span data-ttu-id="b03d2-1187">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1187">The message text</span></span>
| <span data-ttu-id="b03d2-1188">_type</span><span class="sxs-lookup"><span data-stu-id="b03d2-1188">_type</span></span> | <span data-ttu-id="b03d2-1189">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1189">SysAppMessageType</span></span> | <span data-ttu-id="b03d2-1190">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1190">True</span></span> | <span data-ttu-id="b03d2-1191">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-1191">Message Type: info, error , warning</span></span>


### <a name="method-text"></a><span data-ttu-id="b03d2-1192">メソッド text</span><span class="sxs-lookup"><span data-stu-id="b03d2-1192">Method text</span></span> 
<span data-ttu-id="b03d2-1193">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1193">Gets the message text</span></span>

     public str text () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1194">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1194">Return Value</span></span> 
<span data-ttu-id="b03d2-1195">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1195">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="b03d2-1196">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1196">Method type</span></span> 
<span data-ttu-id="b03d2-1197">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-1197">Gets the message type: info, error , warning</span></span>

     public SysAppMessageType type () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1198">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1198">Return Value</span></span> 
<span data-ttu-id="b03d2-1199">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-1199">The message type: info, error , warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="b03d2-1200">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1200">Class SysAppSecurityAttribute</span></span> 
<span data-ttu-id="b03d2-1201">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1201">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="b03d2-1202">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1202">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1203">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1203">Methods</span></span>

| <span data-ttu-id="b03d2-1204">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1204">Method name</span></span> | <span data-ttu-id="b03d2-1205">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1205">Returns</span></span> | <span data-ttu-id="b03d2-1206">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1206">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1207">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1207">new</span></span> | <span data-ttu-id="b03d2-1208">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1208">void</span></span> | <span data-ttu-id="b03d2-1209">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1209">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="b03d2-1210">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="b03d2-1210">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="b03d2-1211">menuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1211">menuItemType</span></span> | <span data-ttu-id="b03d2-1212">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1212">MenuItemType</span></span> | <span data-ttu-id="b03d2-1213">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1213">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="b03d2-1214">menuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1214">menuItemName</span></span> | <span data-ttu-id="b03d2-1215">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1215">MenuItemName</span></span> | <span data-ttu-id="b03d2-1216">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1216">Gets the Menu Item Name of the page</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1217">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1217">Method new</span></span> 
<span data-ttu-id="b03d2-1218">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1218">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="b03d2-1219">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="b03d2-1219">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

     public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1220">Parameters</span></span>

| <span data-ttu-id="b03d2-1221">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1221">Parameter name</span></span> |  <span data-ttu-id="b03d2-1222">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1222">Parameter type</span></span> | <span data-ttu-id="b03d2-1223">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1223">Optional</span></span> | <span data-ttu-id="b03d2-1224">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1224">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1225">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1225">_menuItemName</span></span> | <span data-ttu-id="b03d2-1226">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1226">MenuItemName</span></span> | <span data-ttu-id="b03d2-1227">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1227">True</span></span> | <span data-ttu-id="b03d2-1228">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1228">Menu Item Name of the page</span></span>
| <span data-ttu-id="b03d2-1229">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1229">_menuItemType</span></span> | <span data-ttu-id="b03d2-1230">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1230">MenuItemType</span></span> | <span data-ttu-id="b03d2-1231">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1231">True</span></span> | <span data-ttu-id="b03d2-1232">アクション、表示または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1232">Menu Item Type of the page like action, display or output</span></span>


### <a name="method-menuitemtype"></a><span data-ttu-id="b03d2-1233">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1233">Method menuItemType</span></span> 
<span data-ttu-id="b03d2-1234">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1234">Gets the Menu Item Type of the page</span></span>

     public MenuItemType menuItemType () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1235">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1235">Return Value</span></span> 
<span data-ttu-id="b03d2-1236">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1236">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="b03d2-1237">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1237">Method menuItemName</span></span> 
<span data-ttu-id="b03d2-1238">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1238">Gets the Menu Item Name of the page</span></span>

     public MenuItemName menuItemName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1239">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1239">Return Value</span></span> 
<span data-ttu-id="b03d2-1240">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1240">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="b03d2-1241">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="b03d2-1241">Class SysAppWorkspace</span></span> 
<span data-ttu-id="b03d2-1242">これは、AX モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1242">This is the base class of AX mobile workspace.</span></span> <span data-ttu-id="b03d2-1243">AX モバイル ワークスペース クラスは、このクラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1243">AX mobile workspace classes needs to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1244">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1244">Methods</span></span>

| <span data-ttu-id="b03d2-1245">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1245">Method name</span></span> | <span data-ttu-id="b03d2-1246">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1246">Returns</span></span> | <span data-ttu-id="b03d2-1247">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1247">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1248">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-1248">getEnumValues</span></span> | <span data-ttu-id="b03d2-1249">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1249">List</span></span> | <span data-ttu-id="b03d2-1250">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1250">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-1251">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-1251">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="b03d2-1252">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1252">getWorkspaceMetadata</span></span> | <span data-ttu-id="b03d2-1253">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1253">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="b03d2-1254">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1254">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-1255">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-1255">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="b03d2-1256">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-1256">onBeginAppJob</span></span> | <span data-ttu-id="b03d2-1257">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1257">void</span></span> | <span data-ttu-id="b03d2-1258">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-1258">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="b03d2-1259">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-1259">onEndAppJob</span></span> | <span data-ttu-id="b03d2-1260">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1260">void</span></span> | <span data-ttu-id="b03d2-1261">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-1261">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="b03d2-1262">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1262">workspaceHidden</span></span> | <span data-ttu-id="b03d2-1263">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1263">boolean</span></span> | <span data-ttu-id="b03d2-1264">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1264">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="b03d2-1265">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1265">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="b03d2-1266">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1266">If the attribute is not specified on the class than it always returns false</span></span> |


### <a name="method-getenumvalues"></a><span data-ttu-id="b03d2-1267">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-1267">Method getEnumValues</span></span> 
<span data-ttu-id="b03d2-1268">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1268">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-1269">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-1269">Can be used to modify the enum values that are returned to AX mobile</span></span>

     public List getEnumValues (EnumName _enumName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1270">Parameters</span></span>

| <span data-ttu-id="b03d2-1271">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1271">Parameter name</span></span> |  <span data-ttu-id="b03d2-1272">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1272">Parameter type</span></span> | <span data-ttu-id="b03d2-1273">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1273">Optional</span></span> | <span data-ttu-id="b03d2-1274">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1274">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1275">_enumName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1275">_enumName</span></span> | <span data-ttu-id="b03d2-1276">EnumName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1276">EnumName</span></span> | <span data-ttu-id="b03d2-1277">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1277">False</span></span> | <span data-ttu-id="b03d2-1278">列挙名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1278">The enum name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1279">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1279">Return Value</span></span> 
<span data-ttu-id="b03d2-1280">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="b03d2-1280">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="b03d2-1281">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1281">Method getWorkspaceMetadata</span></span> 
<span data-ttu-id="b03d2-1282">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1282">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-1283">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-1283">Can be used to modify the workspace metadata</span></span>

     public SysAppWorkspaceMetadata getWorkspaceMetadata () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1284">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1284">Return Value</span></span> 
<span data-ttu-id="b03d2-1285">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1285">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="b03d2-1286">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-1286">Method onBeginAppJob</span></span> 
<span data-ttu-id="b03d2-1287">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-1287">Called before the start of execution of AX mobile job</span></span>

     public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1288">Parameters</span></span>

| <span data-ttu-id="b03d2-1289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1289">Parameter name</span></span> |  <span data-ttu-id="b03d2-1290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1290">Parameter type</span></span> | <span data-ttu-id="b03d2-1291">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1291">Optional</span></span> | <span data-ttu-id="b03d2-1292">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1293">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="b03d2-1293">_sysAppJobRequest</span></span> | <span data-ttu-id="b03d2-1294">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="b03d2-1294">SysAppJobRequest</span></span> | <span data-ttu-id="b03d2-1295">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1295">False</span></span> | <span data-ttu-id="b03d2-1296">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-1296">A class containing job request parameters</span></span>


### <a name="method-onendappjob"></a><span data-ttu-id="b03d2-1297">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-1297">Method onEndAppJob</span></span> 
<span data-ttu-id="b03d2-1298">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-1298">Called after the end of execution of AX mobile job</span></span>

     public void onEndAppJob (SysAppJobResponse _sysAppJobResponse) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1299">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1299">Parameters</span></span>

| <span data-ttu-id="b03d2-1300">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1300">Parameter name</span></span> |  <span data-ttu-id="b03d2-1301">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1301">Parameter type</span></span> | <span data-ttu-id="b03d2-1302">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1302">Optional</span></span> | <span data-ttu-id="b03d2-1303">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1303">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1304">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="b03d2-1304">_sysAppJobResponse</span></span> | <span data-ttu-id="b03d2-1305">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="b03d2-1305">SysAppJobResponse</span></span> | <span data-ttu-id="b03d2-1306">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1306">False</span></span> | <span data-ttu-id="b03d2-1307">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-1307">A class containing job response parameters</span></span>


### <a name="method-workspacehidden"></a><span data-ttu-id="b03d2-1308">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1308">Method workspaceHidden</span></span> 
<span data-ttu-id="b03d2-1309">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1309">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="b03d2-1310">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1310">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="b03d2-1311">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1311">If the attribute is not specified on the class than it always returns false</span></span>

     public boolean workspaceHidden () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1312">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1312">Return Value</span></span> 
<span data-ttu-id="b03d2-1313">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1313">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="b03d2-1314">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1314">Class SysAppWorkspaceAttribute</span></span> 
<span data-ttu-id="b03d2-1315">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1315">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1316">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1316">Methods</span></span>

| <span data-ttu-id="b03d2-1317">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1317">Method name</span></span> | <span data-ttu-id="b03d2-1318">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1318">Returns</span></span> | <span data-ttu-id="b03d2-1319">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1319">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1320">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1320">new</span></span> | <span data-ttu-id="b03d2-1321">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1321">void</span></span> | <span data-ttu-id="b03d2-1322">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1322">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="b03d2-1323">AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1323">AppId</span></span> | <span data-ttu-id="b03d2-1324">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1324">str</span></span> | <span data-ttu-id="b03d2-1325">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1325">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="b03d2-1326">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1326">AppResourceName</span></span> | <span data-ttu-id="b03d2-1327">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1327">str</span></span> | <span data-ttu-id="b03d2-1328">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1328">Gets or sets the AOT Resource name which contains the workspace</span></span> |
| <span data-ttu-id="b03d2-1329">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1329">WorkspaceHidden</span></span> | <span data-ttu-id="b03d2-1330">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1330">boolean</span></span> | <span data-ttu-id="b03d2-1331">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1331">Gets or sets if the workspace is hidden from designer</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1332">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1332">Method new</span></span> 
<span data-ttu-id="b03d2-1333">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1333">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

     public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1334">Parameters</span></span>

| <span data-ttu-id="b03d2-1335">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1335">Parameter name</span></span> |  <span data-ttu-id="b03d2-1336">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1336">Parameter type</span></span> | <span data-ttu-id="b03d2-1337">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1337">Optional</span></span> | <span data-ttu-id="b03d2-1338">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1338">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1339">_appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1339">_appId</span></span> | <span data-ttu-id="b03d2-1340">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1340">str</span></span> | <span data-ttu-id="b03d2-1341">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1341">False</span></span> | <span data-ttu-id="b03d2-1342">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1342">The appId of the workspace</span></span>
| <span data-ttu-id="b03d2-1343">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1343">_appResourceName</span></span> | <span data-ttu-id="b03d2-1344">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1344">str</span></span> | <span data-ttu-id="b03d2-1345">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1345">True</span></span> | <span data-ttu-id="b03d2-1346">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1346">The AOT resource name which contains the workspace</span></span>
| <span data-ttu-id="b03d2-1347">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1347">_workspaceHidden</span></span> | <span data-ttu-id="b03d2-1348">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1348">boolean</span></span> | <span data-ttu-id="b03d2-1349">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1349">True</span></span> | <span data-ttu-id="b03d2-1350">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="b03d2-1350">The workspace is hidden from designer</span></span>


### <a name="method-appid"></a><span data-ttu-id="b03d2-1351">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1351">Method AppId</span></span> 
<span data-ttu-id="b03d2-1352">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1352">Gets or sets the AppId of the workspace</span></span>

     public str AppId ([str _appId]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1353">Parameters</span></span>

| <span data-ttu-id="b03d2-1354">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1354">Parameter name</span></span> |  <span data-ttu-id="b03d2-1355">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1355">Parameter type</span></span> | <span data-ttu-id="b03d2-1356">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1356">Optional</span></span> | <span data-ttu-id="b03d2-1357">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1357">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1358">_appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1358">_appId</span></span> | <span data-ttu-id="b03d2-1359">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1359">str</span></span> | <span data-ttu-id="b03d2-1360">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1360">True</span></span> | <span data-ttu-id="b03d2-1361">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1361">The AppId of the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1362">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1362">Return Value</span></span> 
<span data-ttu-id="b03d2-1363">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1363">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="b03d2-1364">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1364">Method AppResourceName</span></span> 
<span data-ttu-id="b03d2-1365">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1365">Gets or sets the AOT Resource name which contains the workspace</span></span>

     public str AppResourceName ([str _appResourceName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1366">Parameters</span></span>

| <span data-ttu-id="b03d2-1367">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1367">Parameter name</span></span> |  <span data-ttu-id="b03d2-1368">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1368">Parameter type</span></span> | <span data-ttu-id="b03d2-1369">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1369">Optional</span></span> | <span data-ttu-id="b03d2-1370">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1370">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1371">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1371">_appResourceName</span></span> | <span data-ttu-id="b03d2-1372">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1372">str</span></span> | <span data-ttu-id="b03d2-1373">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1373">True</span></span> | <span data-ttu-id="b03d2-1374">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1374">The AOT Resource name which contains the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1375">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1375">Return Value</span></span> 
<span data-ttu-id="b03d2-1376">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1376">The AOT Resource name which contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="b03d2-1377">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1377">Method WorkspaceHidden</span></span> 
<span data-ttu-id="b03d2-1378">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1378">Gets or sets if the workspace is hidden from designer</span></span>

     public boolean WorkspaceHidden ([boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1379">Parameters</span></span>

| <span data-ttu-id="b03d2-1380">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1380">Parameter name</span></span> |  <span data-ttu-id="b03d2-1381">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1381">Parameter type</span></span> | <span data-ttu-id="b03d2-1382">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1382">Optional</span></span> | <span data-ttu-id="b03d2-1383">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1383">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1384">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1384">_workspaceHidden</span></span> | <span data-ttu-id="b03d2-1385">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1385">boolean</span></span> | <span data-ttu-id="b03d2-1386">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1386">True</span></span> | <span data-ttu-id="b03d2-1387">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="b03d2-1387">The workspace hidden</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1388">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1388">Return Value</span></span> 
<span data-ttu-id="b03d2-1389">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="b03d2-1389">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="b03d2-1390">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1390">Class SysAppWorkspaceMetadata</span></span> 
<span data-ttu-id="b03d2-1391">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1391">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1392">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1392">Methods</span></span>

| <span data-ttu-id="b03d2-1393">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1393">Method name</span></span> | <span data-ttu-id="b03d2-1394">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1394">Returns</span></span> | <span data-ttu-id="b03d2-1395">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1395">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1396">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1396">new</span></span> | <span data-ttu-id="b03d2-1397">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1397">void</span></span> |  |
| <span data-ttu-id="b03d2-1398">addConfig</span><span class="sxs-lookup"><span data-stu-id="b03d2-1398">addConfig</span></span> | <span data-ttu-id="b03d2-1399">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1399">void</span></span> | <span data-ttu-id="b03d2-1400">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1400">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="b03d2-1401">getPage</span><span class="sxs-lookup"><span data-stu-id="b03d2-1401">getPage</span></span> | <span data-ttu-id="b03d2-1402">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1402">SysAppPageMetadata</span></span> | <span data-ttu-id="b03d2-1403">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1403">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="b03d2-1404">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1404">getPageEnumerator</span></span> | <span data-ttu-id="b03d2-1405">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1405">MapEnumerator</span></span> | <span data-ttu-id="b03d2-1406">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1406">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="b03d2-1407">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-1407">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="b03d2-1408">getAction</span><span class="sxs-lookup"><span data-stu-id="b03d2-1408">getAction</span></span> | <span data-ttu-id="b03d2-1409">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1409">SysAppActionMetadata</span></span> | <span data-ttu-id="b03d2-1410">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1410">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="b03d2-1411">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1411">getActionEnumerator</span></span> | <span data-ttu-id="b03d2-1412">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1412">MapEnumerator</span></span> | <span data-ttu-id="b03d2-1413">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1413">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="b03d2-1414">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-1414">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="b03d2-1415">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1415">getPageNameForRecordingId</span></span> | <span data-ttu-id="b03d2-1416">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1416">str</span></span> | <span data-ttu-id="b03d2-1417">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1417">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="b03d2-1418">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1418">getActionNameForRecordingId</span></span> | <span data-ttu-id="b03d2-1419">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1419">str</span></span> | <span data-ttu-id="b03d2-1420">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1420">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="b03d2-1421">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1421">workspaceTitle</span></span> | <span data-ttu-id="b03d2-1422">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1422">str</span></span> | <span data-ttu-id="b03d2-1423">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1423">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="b03d2-1424">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1424">workspaceDescription</span></span> | <span data-ttu-id="b03d2-1425">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1425">str</span></span> | <span data-ttu-id="b03d2-1426">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1426">Gets and sets the workspace description</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1427">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1427">Method new</span></span> 


     public void new (str _appId, [SysAppWorkspaceAttribute _attribute]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1428">Parameters</span></span>

| <span data-ttu-id="b03d2-1429">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1429">Parameter name</span></span> |  <span data-ttu-id="b03d2-1430">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1430">Parameter type</span></span> | <span data-ttu-id="b03d2-1431">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1431">Optional</span></span> | <span data-ttu-id="b03d2-1432">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1432">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1433">_appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1433">_appId</span></span> | <span data-ttu-id="b03d2-1434">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1434">str</span></span> | <span data-ttu-id="b03d2-1435">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1435">False</span></span> | 
| <span data-ttu-id="b03d2-1436">_attribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1436">_attribute</span></span> | <span data-ttu-id="b03d2-1437">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1437">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="b03d2-1438">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1438">True</span></span> | 


### <a name="method-addconfig"></a><span data-ttu-id="b03d2-1439">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="b03d2-1439">Method addConfig</span></span> 
<span data-ttu-id="b03d2-1440">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1440">Adds a custom config to the mobile workspace metadata</span></span>

     public void addConfig (str _configName, object _configValue) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1441">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1441">Parameters</span></span>

| <span data-ttu-id="b03d2-1442">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1442">Parameter name</span></span> |  <span data-ttu-id="b03d2-1443">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1443">Parameter type</span></span> | <span data-ttu-id="b03d2-1444">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1444">Optional</span></span> | <span data-ttu-id="b03d2-1445">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1445">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1446">_configName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1446">_configName</span></span> | <span data-ttu-id="b03d2-1447">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1447">str</span></span> | <span data-ttu-id="b03d2-1448">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1448">False</span></span> | <span data-ttu-id="b03d2-1449">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1449">A config name</span></span>
| <span data-ttu-id="b03d2-1450">_configValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-1450">_configValue</span></span> | <span data-ttu-id="b03d2-1451">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1451">object</span></span> | <span data-ttu-id="b03d2-1452">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1452">False</span></span> | <span data-ttu-id="b03d2-1453">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1453">An object of a X++ data contract class</span></span>


### <a name="method-getpage"></a><span data-ttu-id="b03d2-1454">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="b03d2-1454">Method getPage</span></span> 
<span data-ttu-id="b03d2-1455">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1455">Returns the page with the pageName provided</span></span>

     public SysAppPageMetadata getPage (str _pageName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1456">Parameters</span></span>

| <span data-ttu-id="b03d2-1457">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1457">Parameter name</span></span> |  <span data-ttu-id="b03d2-1458">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1458">Parameter type</span></span> | <span data-ttu-id="b03d2-1459">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1459">Optional</span></span> | <span data-ttu-id="b03d2-1460">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1460">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1461">_pageName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1461">_pageName</span></span> | <span data-ttu-id="b03d2-1462">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1462">str</span></span> | <span data-ttu-id="b03d2-1463">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1463">False</span></span> | <span data-ttu-id="b03d2-1464">ページ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1464">A page name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1465">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1465">Return Value</span></span> 
<span data-ttu-id="b03d2-1466">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1466">Returns the pageMetadata if a page with the provided name exist;otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="b03d2-1467">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1467">Method getPageEnumerator</span></span> 
<span data-ttu-id="b03d2-1468">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1468">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="b03d2-1469">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-1469">Where key is page name and value is of type SysAppPageMetadata</span></span>

     public MapEnumerator getPageEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1470">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1470">Return Value</span></span> 
<span data-ttu-id="b03d2-1471">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-1471">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="b03d2-1472">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="b03d2-1472">Method getAction</span></span> 
<span data-ttu-id="b03d2-1473">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1473">Returns the action with the actionName provided</span></span>

     public SysAppActionMetadata getAction (str _actionName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1474">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1474">Parameters</span></span>

| <span data-ttu-id="b03d2-1475">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1475">Parameter name</span></span> |  <span data-ttu-id="b03d2-1476">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1476">Parameter type</span></span> | <span data-ttu-id="b03d2-1477">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1477">Optional</span></span> | <span data-ttu-id="b03d2-1478">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1478">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1479">_actionName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1479">_actionName</span></span> | <span data-ttu-id="b03d2-1480">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1480">str</span></span> | <span data-ttu-id="b03d2-1481">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1481">False</span></span> | <span data-ttu-id="b03d2-1482">アクション名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1482">An action name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1483">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1483">Return Value</span></span> 
<span data-ttu-id="b03d2-1484">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1484">Returns the ActionMetadata if an action with the provided name exist;otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="b03d2-1485">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1485">Method getActionEnumerator</span></span> 
<span data-ttu-id="b03d2-1486">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1486">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="b03d2-1487">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-1487">Where key is action name and value is of type SysAppActionMetadata</span></span>

     public MapEnumerator getActionEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1488">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1488">Return Value</span></span> 
<span data-ttu-id="b03d2-1489">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-1489">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="b03d2-1490">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1490">Method getPageNameForRecordingId</span></span> 
<span data-ttu-id="b03d2-1491">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1491">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

     public str getPageNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1492">Parameters</span></span>

| <span data-ttu-id="b03d2-1493">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1493">Parameter name</span></span> |  <span data-ttu-id="b03d2-1494">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1494">Parameter type</span></span> | <span data-ttu-id="b03d2-1495">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1495">Optional</span></span> | <span data-ttu-id="b03d2-1496">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1496">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1497">_recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1497">_recordingId</span></span> | <span data-ttu-id="b03d2-1498">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1498">str</span></span> | <span data-ttu-id="b03d2-1499">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1499">False</span></span> | <span data-ttu-id="b03d2-1500">recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1500">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1501">Return Value</span></span> 
<span data-ttu-id="b03d2-1502">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1502">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="b03d2-1503">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1503">Method getActionNameForRecordingId</span></span> 
<span data-ttu-id="b03d2-1504">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1504">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

     public str getActionNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1505">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1505">Parameters</span></span>

| <span data-ttu-id="b03d2-1506">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1506">Parameter name</span></span> |  <span data-ttu-id="b03d2-1507">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1507">Parameter type</span></span> | <span data-ttu-id="b03d2-1508">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1508">Optional</span></span> | <span data-ttu-id="b03d2-1509">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1509">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1510">_recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1510">_recordingId</span></span> | <span data-ttu-id="b03d2-1511">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1511">str</span></span> | <span data-ttu-id="b03d2-1512">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1512">False</span></span> | <span data-ttu-id="b03d2-1513">recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1513">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1514">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1514">Return Value</span></span> 
<span data-ttu-id="b03d2-1515">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1515">An action name if the supplied recordingId is used by a workspace action;otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="b03d2-1516">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1516">Method workspaceTitle</span></span> 
<span data-ttu-id="b03d2-1517">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1517">Gets and sets the workspace title</span></span>

     public str workspaceTitle ([str _workspaceTitle]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1518">Parameters</span></span>

| <span data-ttu-id="b03d2-1519">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1519">Parameter name</span></span> |  <span data-ttu-id="b03d2-1520">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1520">Parameter type</span></span> | <span data-ttu-id="b03d2-1521">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1521">Optional</span></span> | <span data-ttu-id="b03d2-1522">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1522">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1523">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1523">_workspaceTitle</span></span> | <span data-ttu-id="b03d2-1524">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1524">str</span></span> | <span data-ttu-id="b03d2-1525">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1525">True</span></span> | <span data-ttu-id="b03d2-1526">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1526">The workspace title</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1527">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1527">Return Value</span></span> 
<span data-ttu-id="b03d2-1528">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1528">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="b03d2-1529">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1529">Method workspaceDescription</span></span> 
<span data-ttu-id="b03d2-1530">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1530">Gets and sets the workspace description</span></span>

     public str workspaceDescription ([str _workspaceDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1531">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1531">Parameters</span></span>

| <span data-ttu-id="b03d2-1532">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1532">Parameter name</span></span> |  <span data-ttu-id="b03d2-1533">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1533">Parameter type</span></span> | <span data-ttu-id="b03d2-1534">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1534">Optional</span></span> | <span data-ttu-id="b03d2-1535">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1535">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1536">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1536">_workspaceDescription</span></span> | <span data-ttu-id="b03d2-1537">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1537">str</span></span> | <span data-ttu-id="b03d2-1538">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1538">True</span></span> | <span data-ttu-id="b03d2-1539">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1539">The workspace description</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1540">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1540">Return Value</span></span> 
<span data-ttu-id="b03d2-1541">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1541">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="b03d2-1542">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1542">Class SysAppWorkspaceSecurityAttribute</span></span> 
<span data-ttu-id="b03d2-1543">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1543">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1544">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1544">Methods</span></span>

| <span data-ttu-id="b03d2-1545">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1545">Method name</span></span> | <span data-ttu-id="b03d2-1546">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1546">Returns</span></span> | <span data-ttu-id="b03d2-1547">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1547">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1548">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1548">new</span></span> | <span data-ttu-id="b03d2-1549">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1549">void</span></span> | <span data-ttu-id="b03d2-1550">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="b03d2-1550">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="b03d2-1551">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1551">WorkspaceMenuItemName</span></span> | <span data-ttu-id="b03d2-1552">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1552">MenuItemName</span></span> | <span data-ttu-id="b03d2-1553">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1553">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="b03d2-1554">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1554">WorkspaceMenuItemType</span></span> | <span data-ttu-id="b03d2-1555">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1555">MenuItemType</span></span> | <span data-ttu-id="b03d2-1556">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1556">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1557">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1557">Method new</span></span> 
<span data-ttu-id="b03d2-1558">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="b03d2-1558">Creates a new instance of attribute</span></span>

     public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1559">Parameters</span></span>

| <span data-ttu-id="b03d2-1560">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1560">Parameter name</span></span> |  <span data-ttu-id="b03d2-1561">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1561">Parameter type</span></span> | <span data-ttu-id="b03d2-1562">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1562">Optional</span></span> | <span data-ttu-id="b03d2-1563">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1563">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1564">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1564">_workspaceMenuItemName</span></span> | <span data-ttu-id="b03d2-1565">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1565">MenuItemName</span></span> | <span data-ttu-id="b03d2-1566">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1566">False</span></span> | <span data-ttu-id="b03d2-1567">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1567">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="b03d2-1568">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1568">_workspaceMenuItemType</span></span> | <span data-ttu-id="b03d2-1569">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1569">MenuItemType</span></span> | <span data-ttu-id="b03d2-1570">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1570">True</span></span> | <span data-ttu-id="b03d2-1571">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1571">The menu item type</span></span>


### <a name="method-workspacemenuitemname"></a><span data-ttu-id="b03d2-1572">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1572">Method WorkspaceMenuItemName</span></span> 
<span data-ttu-id="b03d2-1573">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1573">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

     public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1574">Parameters</span></span>

| <span data-ttu-id="b03d2-1575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1575">Parameter name</span></span> |  <span data-ttu-id="b03d2-1576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1576">Parameter type</span></span> | <span data-ttu-id="b03d2-1577">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1577">Optional</span></span> | <span data-ttu-id="b03d2-1578">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1579">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1579">_workspaceMenuItemName</span></span> | <span data-ttu-id="b03d2-1580">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1580">MenuItemName</span></span> | <span data-ttu-id="b03d2-1581">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1581">True</span></span> | <span data-ttu-id="b03d2-1582">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="b03d2-1582">The workspace menu item for the workspace security attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1583">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1583">Return Value</span></span> 
<span data-ttu-id="b03d2-1584">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="b03d2-1584">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="b03d2-1585">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1585">Method WorkspaceMenuItemType</span></span> 
<span data-ttu-id="b03d2-1586">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1586">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

     public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1587">Parameters</span></span>

| <span data-ttu-id="b03d2-1588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1588">Parameter name</span></span> |  <span data-ttu-id="b03d2-1589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1589">Parameter type</span></span> | <span data-ttu-id="b03d2-1590">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1590">Optional</span></span> | <span data-ttu-id="b03d2-1591">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1592">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1592">_workspaceMenuItemType</span></span> | <span data-ttu-id="b03d2-1593">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1593">MenuItemType</span></span> | <span data-ttu-id="b03d2-1594">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1594">True</span></span> | <span data-ttu-id="b03d2-1595">workspacesecurity 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1595">The workspace menu item type for the workspacesecurity attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1596">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1596">Return Value</span></span> 
<span data-ttu-id="b03d2-1597">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1597">The workspace menu item type for the workspace security attribute</span></span>

## <a name="class-sysappactionattribute"></a><span data-ttu-id="b03d2-1598">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1598">Class SysAppActionAttribute</span></span> 
<span data-ttu-id="b03d2-1599">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1599">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1600">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1600">Methods</span></span>

| <span data-ttu-id="b03d2-1601">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1601">Method name</span></span> | <span data-ttu-id="b03d2-1602">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1602">Returns</span></span> | <span data-ttu-id="b03d2-1603">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1603">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1604">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1604">new</span></span> | <span data-ttu-id="b03d2-1605">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1605">void</span></span> | <span data-ttu-id="b03d2-1606">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1606">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="b03d2-1607">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1607">pageMethodName</span></span> | <span data-ttu-id="b03d2-1608">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1608">str</span></span> | <span data-ttu-id="b03d2-1609">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1609">Gets the get method name which forms the page under which this task resides</span></span> |
| <span data-ttu-id="b03d2-1610">actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1610">actionTitle</span></span> | <span data-ttu-id="b03d2-1611">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1611">str</span></span> | <span data-ttu-id="b03d2-1612">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1612">Gets the Action Title</span></span> |
| <span data-ttu-id="b03d2-1613">actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1613">actionDescription</span></span> | <span data-ttu-id="b03d2-1614">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1614">str</span></span> | <span data-ttu-id="b03d2-1615">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1615">Gets the Action Description</span></span> |
| <span data-ttu-id="b03d2-1616">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1616">crudOperationType</span></span> | <span data-ttu-id="b03d2-1617">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="b03d2-1617">SysAppCRUDOperation</span></span> | <span data-ttu-id="b03d2-1618">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1618">Gets the Crud Operation Type like Create, Update, Delete</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1619">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1619">Method new</span></span> 
<span data-ttu-id="b03d2-1620">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1620">Creates a new instance of SysAppActionAttribute class</span></span>

     public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1621">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1621">Parameters</span></span>

| <span data-ttu-id="b03d2-1622">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1622">Parameter name</span></span> |  <span data-ttu-id="b03d2-1623">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1623">Parameter type</span></span> | <span data-ttu-id="b03d2-1624">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1624">Optional</span></span> | <span data-ttu-id="b03d2-1625">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1625">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1626">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1626">_actionTitle</span></span> | <span data-ttu-id="b03d2-1627">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1627">str</span></span> | <span data-ttu-id="b03d2-1628">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1628">True</span></span> | <span data-ttu-id="b03d2-1629">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1629">Action title</span></span>
| <span data-ttu-id="b03d2-1630">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1630">_actionDescription</span></span> | <span data-ttu-id="b03d2-1631">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1631">str</span></span> | <span data-ttu-id="b03d2-1632">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1632">True</span></span> | <span data-ttu-id="b03d2-1633">アクション説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1633">Action description</span></span>
| <span data-ttu-id="b03d2-1634">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1634">_crudOperationType</span></span> | <span data-ttu-id="b03d2-1635">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="b03d2-1635">SysAppCRUDOperation</span></span> | <span data-ttu-id="b03d2-1636">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1636">True</span></span> | <span data-ttu-id="b03d2-1637">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="b03d2-1637">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="b03d2-1638">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1638">_pageMethodName</span></span> | <span data-ttu-id="b03d2-1639">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1639">str</span></span> | <span data-ttu-id="b03d2-1640">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1640">True</span></span> | <span data-ttu-id="b03d2-1641">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-1641">Name of the method constructing parent page</span></span>


### <a name="method-pagemethodname"></a><span data-ttu-id="b03d2-1642">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1642">Method pageMethodName</span></span> 
<span data-ttu-id="b03d2-1643">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1643">Gets the get method name which forms the page under which this task resides</span></span>

     public str pageMethodName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1644">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1644">Return Value</span></span> 
<span data-ttu-id="b03d2-1645">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1645">The page method name which forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="b03d2-1646">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1646">Method actionTitle</span></span> 
<span data-ttu-id="b03d2-1647">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1647">Gets the Action Title</span></span>

     public str actionTitle () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1648">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1648">Return Value</span></span> 
<span data-ttu-id="b03d2-1649">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1649">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="b03d2-1650">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1650">Method actionDescription</span></span> 
<span data-ttu-id="b03d2-1651">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1651">Gets the Action Description</span></span>

     public str actionDescription () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1652">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1652">Return Value</span></span> 
<span data-ttu-id="b03d2-1653">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1653">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="b03d2-1654">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1654">Method crudOperationType</span></span> 
<span data-ttu-id="b03d2-1655">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-1655">Gets the Crud Operation Type like Create, Update, Delete</span></span>

     public SysAppCRUDOperation crudOperationType () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1656">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1656">Return Value</span></span> 
<span data-ttu-id="b03d2-1657">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1657">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="b03d2-1658">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1658">Class SysAppActionMetadata</span></span> 
<span data-ttu-id="b03d2-1659">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1659">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1660">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1660">Methods</span></span>

| <span data-ttu-id="b03d2-1661">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1661">Method name</span></span> | <span data-ttu-id="b03d2-1662">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1662">Returns</span></span> | <span data-ttu-id="b03d2-1663">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1663">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1664">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1664">new</span></span> | <span data-ttu-id="b03d2-1665">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1665">void</span></span> |  |
| <span data-ttu-id="b03d2-1666">getActionName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1666">getActionName</span></span> | <span data-ttu-id="b03d2-1667">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1667">str</span></span> | <span data-ttu-id="b03d2-1668">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1668">Returns the action name</span></span> |
| <span data-ttu-id="b03d2-1669">actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1669">actionTitle</span></span> | <span data-ttu-id="b03d2-1670">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1670">str</span></span> | <span data-ttu-id="b03d2-1671">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1671">Gets or sets the action title</span></span> |
| <span data-ttu-id="b03d2-1672">actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1672">actionDescription</span></span> | <span data-ttu-id="b03d2-1673">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1673">str</span></span> | <span data-ttu-id="b03d2-1674">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1674">Gets or sets the action description</span></span> |
| <span data-ttu-id="b03d2-1675">actionHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1675">actionHidden</span></span> | <span data-ttu-id="b03d2-1676">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1676">boolean</span></span> | <span data-ttu-id="b03d2-1677">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1677">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="b03d2-1678">actionOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-1678">actionOrder</span></span> | <span data-ttu-id="b03d2-1679">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-1679">int</span></span> | <span data-ttu-id="b03d2-1680">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1680">Gets or sets the action order</span></span> |
| <span data-ttu-id="b03d2-1681">getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-1681">getControl</span></span> | <span data-ttu-id="b03d2-1682">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1682">SysAppControlMetadata</span></span> | <span data-ttu-id="b03d2-1683">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1683">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="b03d2-1684">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1684">getControlEnumerator</span></span> | <span data-ttu-id="b03d2-1685">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1685">MapEnumerator</span></span> | <span data-ttu-id="b03d2-1686">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1686">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="b03d2-1687">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-1687">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1688">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1688">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1689">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1689">Parameters</span></span>

| <span data-ttu-id="b03d2-1690">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1690">Parameter name</span></span> |  <span data-ttu-id="b03d2-1691">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1691">Parameter type</span></span> | <span data-ttu-id="b03d2-1692">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1692">Optional</span></span> | <span data-ttu-id="b03d2-1693">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1693">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1694">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1694">_taskmetadata</span></span> | <span data-ttu-id="b03d2-1695">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1695">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="b03d2-1696">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1696">False</span></span> | 


### <a name="method-getactionname"></a><span data-ttu-id="b03d2-1697">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1697">Method getActionName</span></span> 
<span data-ttu-id="b03d2-1698">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1698">Returns the action name</span></span>

     public str getActionName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1699">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1699">Return Value</span></span> 
<span data-ttu-id="b03d2-1700">アクション名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1700">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="b03d2-1701">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1701">Method actionTitle</span></span> 
<span data-ttu-id="b03d2-1702">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1702">Gets or sets the action title</span></span>

     public str actionTitle ([str _actionTitle]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1703">Parameters</span></span>

| <span data-ttu-id="b03d2-1704">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1704">Parameter name</span></span> |  <span data-ttu-id="b03d2-1705">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1705">Parameter type</span></span> | <span data-ttu-id="b03d2-1706">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1706">Optional</span></span> | <span data-ttu-id="b03d2-1707">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1707">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1708">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-1708">_actionTitle</span></span> | <span data-ttu-id="b03d2-1709">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1709">str</span></span> | <span data-ttu-id="b03d2-1710">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1710">True</span></span> | <span data-ttu-id="b03d2-1711">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1711">The action title</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1712">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1712">Return Value</span></span> 
<span data-ttu-id="b03d2-1713">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1713">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="b03d2-1714">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1714">Method actionDescription</span></span> 
<span data-ttu-id="b03d2-1715">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1715">Gets or sets the action description</span></span>

     public str actionDescription ([str _actionDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1716">Parameters</span></span>

| <span data-ttu-id="b03d2-1717">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1717">Parameter name</span></span> |  <span data-ttu-id="b03d2-1718">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1718">Parameter type</span></span> | <span data-ttu-id="b03d2-1719">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1719">Optional</span></span> | <span data-ttu-id="b03d2-1720">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1720">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1721">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-1721">_actionDescription</span></span> | <span data-ttu-id="b03d2-1722">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1722">str</span></span> | <span data-ttu-id="b03d2-1723">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1723">True</span></span> | <span data-ttu-id="b03d2-1724">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1724">The action description</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1725">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1725">Return Value</span></span> 
<span data-ttu-id="b03d2-1726">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1726">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="b03d2-1727">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1727">Method actionHidden</span></span> 
<span data-ttu-id="b03d2-1728">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1728">Gets or sets whether action is hidden</span></span>

     public boolean actionHidden ([boolean _actionHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1729">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1729">Parameters</span></span>

| <span data-ttu-id="b03d2-1730">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1730">Parameter name</span></span> |  <span data-ttu-id="b03d2-1731">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1731">Parameter type</span></span> | <span data-ttu-id="b03d2-1732">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1732">Optional</span></span> | <span data-ttu-id="b03d2-1733">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1733">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1734">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1734">_actionHidden</span></span> | <span data-ttu-id="b03d2-1735">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1735">boolean</span></span> | <span data-ttu-id="b03d2-1736">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1736">True</span></span> | <span data-ttu-id="b03d2-1737">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1737">Action hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1738">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1738">Return Value</span></span> 
<span data-ttu-id="b03d2-1739">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1739">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="b03d2-1740">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-1740">Method actionOrder</span></span> 
<span data-ttu-id="b03d2-1741">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1741">Gets or sets the action order</span></span>

     public int actionOrder ([int _actionOrder]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1742">Parameters</span></span>

| <span data-ttu-id="b03d2-1743">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1743">Parameter name</span></span> |  <span data-ttu-id="b03d2-1744">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1744">Parameter type</span></span> | <span data-ttu-id="b03d2-1745">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1745">Optional</span></span> | <span data-ttu-id="b03d2-1746">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1746">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1747">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-1747">_actionOrder</span></span> | <span data-ttu-id="b03d2-1748">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-1748">int</span></span> | <span data-ttu-id="b03d2-1749">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1749">True</span></span> | <span data-ttu-id="b03d2-1750">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-1750">The action order</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1751">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1751">Return Value</span></span> 
<span data-ttu-id="b03d2-1752">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-1752">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="b03d2-1753">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-1753">Method getControl</span></span> 
<span data-ttu-id="b03d2-1754">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1754">Returns the control on the current action having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1755">Parameters</span></span>

| <span data-ttu-id="b03d2-1756">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1756">Parameter name</span></span> |  <span data-ttu-id="b03d2-1757">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1757">Parameter type</span></span> | <span data-ttu-id="b03d2-1758">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1758">Optional</span></span> | <span data-ttu-id="b03d2-1759">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1759">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1760">_controlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1760">_controlName</span></span> | <span data-ttu-id="b03d2-1761">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1761">str</span></span> | <span data-ttu-id="b03d2-1762">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1762">False</span></span> | <span data-ttu-id="b03d2-1763">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1763">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1764">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1764">Return Value</span></span> 
<span data-ttu-id="b03d2-1765">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="b03d2-1765">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action;otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="b03d2-1766">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-1766">Method getControlEnumerator</span></span> 
<span data-ttu-id="b03d2-1767">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1767">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="b03d2-1768">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-1768">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1769">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1769">Return Value</span></span> 
<span data-ttu-id="b03d2-1770">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-1770">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="b03d2-1771">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="b03d2-1771">Class SysAppAttributeHelper</span></span> 
<span data-ttu-id="b03d2-1772">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-1772">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1773">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1773">Methods</span></span>

| <span data-ttu-id="b03d2-1774">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1774">Method name</span></span> | <span data-ttu-id="b03d2-1775">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1775">Returns</span></span> | <span data-ttu-id="b03d2-1776">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1776">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1777">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-1777">getAttributeFromClass</span></span> | <span data-ttu-id="b03d2-1778">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1778">SysAttribute</span></span> | <span data-ttu-id="b03d2-1779">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1779">gets attribute from class</span></span> |


### <a name="method-getattributefromclass"></a><span data-ttu-id="b03d2-1780">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-1780">Method getAttributeFromClass</span></span> 
<span data-ttu-id="b03d2-1781">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1781">gets attribute from class</span></span>

     public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1782">Parameters</span></span>

| <span data-ttu-id="b03d2-1783">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1783">Parameter name</span></span> |  <span data-ttu-id="b03d2-1784">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1784">Parameter type</span></span> | <span data-ttu-id="b03d2-1785">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1785">Optional</span></span> | <span data-ttu-id="b03d2-1786">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1786">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1787">_sysClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-1787">_sysClass</span></span> | <span data-ttu-id="b03d2-1788">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="b03d2-1788">SysDictClass</span></span> | <span data-ttu-id="b03d2-1789">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1789">False</span></span> | <span data-ttu-id="b03d2-1790">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-1790">class for which attributes is required</span></span>
| <span data-ttu-id="b03d2-1791">_attributeType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1791">_attributeType</span></span> | <span data-ttu-id="b03d2-1792">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="b03d2-1792">SysAppAttributeType</span></span> | <span data-ttu-id="b03d2-1793">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1793">False</span></span> | <span data-ttu-id="b03d2-1794">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="b03d2-1794">Type of attribute like SysAppEntityAttribute</span></span>


## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="b03d2-1795">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1795">Class SysAppCollectionAttribute</span></span> 
<span data-ttu-id="b03d2-1796">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1796">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1797">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1797">Methods</span></span>

| <span data-ttu-id="b03d2-1798">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1798">Method name</span></span> | <span data-ttu-id="b03d2-1799">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1799">Returns</span></span> | <span data-ttu-id="b03d2-1800">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1800">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1801">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1801">new</span></span> | <span data-ttu-id="b03d2-1802">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1802">void</span></span> | <span data-ttu-id="b03d2-1803">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1803">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1804">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1804">Method new</span></span> 
<span data-ttu-id="b03d2-1805">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1805">Constructor</span></span>

     public void new (str _itemContractName, [str _label], [str _relationshipName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1806">Parameters</span></span>

| <span data-ttu-id="b03d2-1807">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1807">Parameter name</span></span> |  <span data-ttu-id="b03d2-1808">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1808">Parameter type</span></span> | <span data-ttu-id="b03d2-1809">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1809">Optional</span></span> | <span data-ttu-id="b03d2-1810">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1810">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1811">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1811">_itemContractName</span></span> | <span data-ttu-id="b03d2-1812">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1812">str</span></span> | <span data-ttu-id="b03d2-1813">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1813">False</span></span> | <span data-ttu-id="b03d2-1814">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1814">Data contract name of list item</span></span>
| <span data-ttu-id="b03d2-1815">_label</span><span class="sxs-lookup"><span data-stu-id="b03d2-1815">_label</span></span> | <span data-ttu-id="b03d2-1816">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1816">str</span></span> | <span data-ttu-id="b03d2-1817">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1817">True</span></span> | <span data-ttu-id="b03d2-1818">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1818">List control label</span></span>
| <span data-ttu-id="b03d2-1819">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1819">_relationshipName</span></span> | <span data-ttu-id="b03d2-1820">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1820">str</span></span> | <span data-ttu-id="b03d2-1821">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1821">True</span></span> | <span data-ttu-id="b03d2-1822">関係名。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1822">Relationship name.</span></span> <span data-ttu-id="b03d2-1823">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1823">By default the entity name of the list item is used as relationship name</span></span>


## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="b03d2-1824">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1824">Class SysAppControlMetadata</span></span> 
<span data-ttu-id="b03d2-1825">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1825">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="b03d2-1826">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="b03d2-1826">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1827">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1827">Methods</span></span>

| <span data-ttu-id="b03d2-1828">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1828">Method name</span></span> | <span data-ttu-id="b03d2-1829">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1829">Returns</span></span> | <span data-ttu-id="b03d2-1830">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1830">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1831">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1831">new</span></span> | <span data-ttu-id="b03d2-1832">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1832">void</span></span> | <span data-ttu-id="b03d2-1833">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1833">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="b03d2-1834">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1834">getBaseLanguageId</span></span> | <span data-ttu-id="b03d2-1835">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1835">str</span></span> | <span data-ttu-id="b03d2-1836">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1836">Returns the base language id for the app</span></span> |
| <span data-ttu-id="b03d2-1837">getControlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1837">getControlName</span></span> | <span data-ttu-id="b03d2-1838">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1838">str</span></span> | <span data-ttu-id="b03d2-1839">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1839">Returns the control name</span></span> |
| <span data-ttu-id="b03d2-1840">controlLabel</span><span class="sxs-lookup"><span data-stu-id="b03d2-1840">controlLabel</span></span> | <span data-ttu-id="b03d2-1841">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1841">str</span></span> | <span data-ttu-id="b03d2-1842">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1842">Gets and sets the control label</span></span> |
| <span data-ttu-id="b03d2-1843">controlHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1843">controlHidden</span></span> | <span data-ttu-id="b03d2-1844">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1844">boolean</span></span> | <span data-ttu-id="b03d2-1845">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1845">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="b03d2-1846">controlOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-1846">controlOrder</span></span> | <span data-ttu-id="b03d2-1847">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-1847">int</span></span> | <span data-ttu-id="b03d2-1848">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1848">Gets or sets the control order</span></span> |
| <span data-ttu-id="b03d2-1849">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="b03d2-1849">controlMandatory</span></span> | <span data-ttu-id="b03d2-1850">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1850">boolean</span></span> | <span data-ttu-id="b03d2-1851">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1851">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="b03d2-1852">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="b03d2-1852">controlAllowNegative</span></span> | <span data-ttu-id="b03d2-1853">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1853">boolean</span></span> | <span data-ttu-id="b03d2-1854">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1854">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="b03d2-1855">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="b03d2-1855">controlMaxLength</span></span> | <span data-ttu-id="b03d2-1856">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-1856">int</span></span> | <span data-ttu-id="b03d2-1857">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1857">Gets or sets the control max length</span></span> |
| <span data-ttu-id="b03d2-1858">getProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-1858">getProperty</span></span> | <span data-ttu-id="b03d2-1859">anytype</span><span class="sxs-lookup"><span data-stu-id="b03d2-1859">anytype</span></span> | <span data-ttu-id="b03d2-1860">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1860">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="b03d2-1861">setProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-1861">setProperty</span></span> | <span data-ttu-id="b03d2-1862">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-1862">void</span></span> | <span data-ttu-id="b03d2-1863">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1863">Sets the control property referenced by the key</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-1864">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-1864">Method new</span></span> 
<span data-ttu-id="b03d2-1865">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-1865">Creates a new instance of the control metadata</span></span>

     public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1866">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1866">Parameters</span></span>

| <span data-ttu-id="b03d2-1867">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1867">Parameter name</span></span> |  <span data-ttu-id="b03d2-1868">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1868">Parameter type</span></span> | <span data-ttu-id="b03d2-1869">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1869">Optional</span></span> | <span data-ttu-id="b03d2-1870">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1870">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1871">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1871">_controlMetadata</span></span> | <span data-ttu-id="b03d2-1872">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-1872">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="b03d2-1873">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1873">False</span></span> | <span data-ttu-id="b03d2-1874">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-1874">The controlMetadata object</span></span>
| <span data-ttu-id="b03d2-1875">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1875">_baseLanguageId</span></span> | <span data-ttu-id="b03d2-1876">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1876">str</span></span> | <span data-ttu-id="b03d2-1877">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1877">True</span></span> | <span data-ttu-id="b03d2-1878">基本言語</span><span class="sxs-lookup"><span data-stu-id="b03d2-1878">The base language</span></span>


### <a name="method-getbaselanguageid"></a><span data-ttu-id="b03d2-1879">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="b03d2-1879">Method getBaseLanguageId</span></span> 
<span data-ttu-id="b03d2-1880">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1880">Returns the base language id for the app</span></span>

     public str getBaseLanguageId () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1881">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1881">Return Value</span></span> 
<span data-ttu-id="b03d2-1882">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-1882">The base language id</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="b03d2-1883">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-1883">Method getControlName</span></span> 
<span data-ttu-id="b03d2-1884">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1884">Returns the control name</span></span>

     public str getControlName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-1885">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1885">Return Value</span></span> 
<span data-ttu-id="b03d2-1886">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1886">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="b03d2-1887">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="b03d2-1887">Method controlLabel</span></span> 
<span data-ttu-id="b03d2-1888">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1888">Gets and sets the control label</span></span>

     public str controlLabel ([str _controlLabel]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1889">Parameters</span></span>

| <span data-ttu-id="b03d2-1890">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1890">Parameter name</span></span> |  <span data-ttu-id="b03d2-1891">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1891">Parameter type</span></span> | <span data-ttu-id="b03d2-1892">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1892">Optional</span></span> | <span data-ttu-id="b03d2-1893">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1893">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1894">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="b03d2-1894">_controlLabel</span></span> | <span data-ttu-id="b03d2-1895">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1895">str</span></span> | <span data-ttu-id="b03d2-1896">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1896">True</span></span> | <span data-ttu-id="b03d2-1897">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1897">The control label</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1898">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1898">Return Value</span></span> 
<span data-ttu-id="b03d2-1899">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-1899">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="b03d2-1900">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1900">Method controlHidden</span></span> 
<span data-ttu-id="b03d2-1901">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1901">Gets and sets whether the control is hidden</span></span>

     public boolean controlHidden ([boolean _controlHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1902">Parameters</span></span>

| <span data-ttu-id="b03d2-1903">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1903">Parameter name</span></span> |  <span data-ttu-id="b03d2-1904">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1904">Parameter type</span></span> | <span data-ttu-id="b03d2-1905">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1905">Optional</span></span> | <span data-ttu-id="b03d2-1906">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1906">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1907">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-1907">_controlHidden</span></span> | <span data-ttu-id="b03d2-1908">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1908">boolean</span></span> | <span data-ttu-id="b03d2-1909">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1909">True</span></span> | <span data-ttu-id="b03d2-1910">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="b03d2-1910">Control hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1911">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1911">Return Value</span></span> 
<span data-ttu-id="b03d2-1912">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1912">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="b03d2-1913">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-1913">Method controlOrder</span></span> 
<span data-ttu-id="b03d2-1914">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1914">Gets or sets the control order</span></span>

     public int controlOrder ([int _controlOrder]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1915">Parameters</span></span>

| <span data-ttu-id="b03d2-1916">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1916">Parameter name</span></span> |  <span data-ttu-id="b03d2-1917">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1917">Parameter type</span></span> | <span data-ttu-id="b03d2-1918">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1918">Optional</span></span> | <span data-ttu-id="b03d2-1919">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1919">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1920">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-1920">_controlOrder</span></span> | <span data-ttu-id="b03d2-1921">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-1921">int</span></span> | <span data-ttu-id="b03d2-1922">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1922">True</span></span> | <span data-ttu-id="b03d2-1923">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-1923">The control order</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1924">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1924">Return Value</span></span> 
<span data-ttu-id="b03d2-1925">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-1925">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="b03d2-1926">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="b03d2-1926">Method controlMandatory</span></span> 
<span data-ttu-id="b03d2-1927">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1927">Gets or sets the control mandatory</span></span>

     public boolean controlMandatory ([boolean _controlMandatory]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1928">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1928">Parameters</span></span>

| <span data-ttu-id="b03d2-1929">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1929">Parameter name</span></span> |  <span data-ttu-id="b03d2-1930">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1930">Parameter type</span></span> | <span data-ttu-id="b03d2-1931">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1931">Optional</span></span> | <span data-ttu-id="b03d2-1932">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1932">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1933">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="b03d2-1933">_controlMandatory</span></span> | <span data-ttu-id="b03d2-1934">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1934">boolean</span></span> | <span data-ttu-id="b03d2-1935">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1935">True</span></span> | <span data-ttu-id="b03d2-1936">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="b03d2-1936">The control mandatory</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1937">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1937">Return Value</span></span> 
<span data-ttu-id="b03d2-1938">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="b03d2-1938">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="b03d2-1939">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="b03d2-1939">Method controlAllowNegative</span></span> 
<span data-ttu-id="b03d2-1940">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="b03d2-1940">Gets or sets the control allow negative</span></span>

     public boolean controlAllowNegative ([boolean _controlAllowNegative]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1941">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1941">Parameters</span></span>

| <span data-ttu-id="b03d2-1942">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1942">Parameter name</span></span> |  <span data-ttu-id="b03d2-1943">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1943">Parameter type</span></span> | <span data-ttu-id="b03d2-1944">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1944">Optional</span></span> | <span data-ttu-id="b03d2-1945">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1945">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1946">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="b03d2-1946">_controlAllowNegative</span></span> | <span data-ttu-id="b03d2-1947">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1947">boolean</span></span> | <span data-ttu-id="b03d2-1948">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1948">True</span></span> | <span data-ttu-id="b03d2-1949">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1949">The control allow negative</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1950">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1950">Return Value</span></span> 
<span data-ttu-id="b03d2-1951">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1951">The control allow negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="b03d2-1952">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="b03d2-1952">Method controlMaxLength</span></span> 
<span data-ttu-id="b03d2-1953">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-1953">Gets or sets the control max length</span></span>

     public int controlMaxLength ([int _controlMaxLength]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1954">Parameters</span></span>

| <span data-ttu-id="b03d2-1955">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1955">Parameter name</span></span> |  <span data-ttu-id="b03d2-1956">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1956">Parameter type</span></span> | <span data-ttu-id="b03d2-1957">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1957">Optional</span></span> | <span data-ttu-id="b03d2-1958">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1958">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1959">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="b03d2-1959">_controlMaxLength</span></span> | <span data-ttu-id="b03d2-1960">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-1960">int</span></span> | <span data-ttu-id="b03d2-1961">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-1961">True</span></span> | <span data-ttu-id="b03d2-1962">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="b03d2-1962">The control max length</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1963">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1963">Return Value</span></span> 
<span data-ttu-id="b03d2-1964">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="b03d2-1964">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="b03d2-1965">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-1965">Method getProperty</span></span> 
<span data-ttu-id="b03d2-1966">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1966">Gets the control property referenced by the key</span></span>

     public anytype getProperty (str _key) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1967">Parameters</span></span>

| <span data-ttu-id="b03d2-1968">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1968">Parameter name</span></span> |  <span data-ttu-id="b03d2-1969">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1969">Parameter type</span></span> | <span data-ttu-id="b03d2-1970">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1970">Optional</span></span> | <span data-ttu-id="b03d2-1971">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1971">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1972">_key</span><span class="sxs-lookup"><span data-stu-id="b03d2-1972">_key</span></span> | <span data-ttu-id="b03d2-1973">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1973">str</span></span> | <span data-ttu-id="b03d2-1974">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1974">False</span></span> | <span data-ttu-id="b03d2-1975">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1975">The name of the control property</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-1976">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1976">Return Value</span></span> 
<span data-ttu-id="b03d2-1977">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1977">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="b03d2-1978">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="b03d2-1978">Method setProperty</span></span> 
<span data-ttu-id="b03d2-1979">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1979">Sets the control property referenced by the key</span></span>

     public void setProperty (str _key, anytype _value) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-1980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-1980">Parameters</span></span>

| <span data-ttu-id="b03d2-1981">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1981">Parameter name</span></span> |  <span data-ttu-id="b03d2-1982">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-1982">Parameter type</span></span> | <span data-ttu-id="b03d2-1983">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-1983">Optional</span></span> | <span data-ttu-id="b03d2-1984">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1984">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-1985">_key</span><span class="sxs-lookup"><span data-stu-id="b03d2-1985">_key</span></span> | <span data-ttu-id="b03d2-1986">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-1986">str</span></span> | <span data-ttu-id="b03d2-1987">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1987">False</span></span> | <span data-ttu-id="b03d2-1988">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="b03d2-1988">The name of the control property</span></span>
| <span data-ttu-id="b03d2-1989">_value</span><span class="sxs-lookup"><span data-stu-id="b03d2-1989">_value</span></span> | <span data-ttu-id="b03d2-1990">anytype</span><span class="sxs-lookup"><span data-stu-id="b03d2-1990">anytype</span></span> | <span data-ttu-id="b03d2-1991">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-1991">False</span></span> | <span data-ttu-id="b03d2-1992">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-1992">The value of the control property</span></span>


## <a name="class-sysappentityattribute"></a><span data-ttu-id="b03d2-1993">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1993">Class SysAppEntityAttribute</span></span> 
<span data-ttu-id="b03d2-1994">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-1994">SysAppEntityAttribute used for decorating data contract entities</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-1995">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-1995">Methods</span></span>

| <span data-ttu-id="b03d2-1996">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-1996">Method name</span></span> | <span data-ttu-id="b03d2-1997">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-1997">Returns</span></span> | <span data-ttu-id="b03d2-1998">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-1998">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-1999">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-1999">new</span></span> | <span data-ttu-id="b03d2-2000">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2000">void</span></span> | <span data-ttu-id="b03d2-2001">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2001">Constructor</span></span> |
| <span data-ttu-id="b03d2-2002">名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-2002">name</span></span> | <span data-ttu-id="b03d2-2003">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2003">str</span></span> | <span data-ttu-id="b03d2-2004">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2004">Gets the name of the entity</span></span> |
| <span data-ttu-id="b03d2-2005">entityKey</span><span class="sxs-lookup"><span data-stu-id="b03d2-2005">entityKey</span></span> | <span data-ttu-id="b03d2-2006">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2006">str</span></span> | <span data-ttu-id="b03d2-2007">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2007">Gets the entity key</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2008">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2008">Method new</span></span> 
<span data-ttu-id="b03d2-2009">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2009">Constructor</span></span>

     public void new (str _name, str _entityKey) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2010">Parameters</span></span>

| <span data-ttu-id="b03d2-2011">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2011">Parameter name</span></span> |  <span data-ttu-id="b03d2-2012">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2012">Parameter type</span></span> | <span data-ttu-id="b03d2-2013">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2013">Optional</span></span> | <span data-ttu-id="b03d2-2014">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2014">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2015">_name</span><span class="sxs-lookup"><span data-stu-id="b03d2-2015">_name</span></span> | <span data-ttu-id="b03d2-2016">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2016">str</span></span> | <span data-ttu-id="b03d2-2017">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2017">False</span></span> | <span data-ttu-id="b03d2-2018">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2018">Entity name</span></span>
| <span data-ttu-id="b03d2-2019">_entityKey</span><span class="sxs-lookup"><span data-stu-id="b03d2-2019">_entityKey</span></span> | <span data-ttu-id="b03d2-2020">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2020">str</span></span> | <span data-ttu-id="b03d2-2021">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2021">False</span></span> | <span data-ttu-id="b03d2-2022">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-2022">Name of the entity's key</span></span>


### <a name="method-name"></a><span data-ttu-id="b03d2-2023">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2023">Method name</span></span> 
<span data-ttu-id="b03d2-2024">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2024">Gets the name of the entity</span></span>

     public str name () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2025">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2025">Return Value</span></span> 
<span data-ttu-id="b03d2-2026">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-2026">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="b03d2-2027">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="b03d2-2027">Method entityKey</span></span> 
<span data-ttu-id="b03d2-2028">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2028">Gets the entity key</span></span>

     public str entityKey () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2029">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2029">Return Value</span></span> 
<span data-ttu-id="b03d2-2030">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="b03d2-2030">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="b03d2-2031">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2031">Class SysAppEntityContext</span></span> 
<span data-ttu-id="b03d2-2032">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2032">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2033">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2033">Methods</span></span>

| <span data-ttu-id="b03d2-2034">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2034">Method name</span></span> | <span data-ttu-id="b03d2-2035">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2035">Returns</span></span> | <span data-ttu-id="b03d2-2036">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2036">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2037">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="b03d2-2037">constructFromParams</span></span> | <span data-ttu-id="b03d2-2038">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2038">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-2039">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2039">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="b03d2-2040">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="b03d2-2040">constructFromBuffer</span></span> | <span data-ttu-id="b03d2-2041">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2041">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-2042">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="b03d2-2042">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="b03d2-2043">entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2043">entityName</span></span> | <span data-ttu-id="b03d2-2044">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2044">str</span></span> | <span data-ttu-id="b03d2-2045">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2045">Entity name on which filter applies</span></span> |
| <span data-ttu-id="b03d2-2046">entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2046">entityId</span></span> | <span data-ttu-id="b03d2-2047">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2047">str</span></span> | <span data-ttu-id="b03d2-2048">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2048">Field value on which filter applies</span></span> |


### <a name="method-constructfromparams"></a><span data-ttu-id="b03d2-2049">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="b03d2-2049">Method constructFromParams</span></span> 
<span data-ttu-id="b03d2-2050">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2050">Constructs SysAppEntityContext from entityName and entityId</span></span>

     public SysAppEntityContext constructFromParams (str _entityName, str _entityId) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2051">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2051">Parameters</span></span>

| <span data-ttu-id="b03d2-2052">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2052">Parameter name</span></span> |  <span data-ttu-id="b03d2-2053">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2053">Parameter type</span></span> | <span data-ttu-id="b03d2-2054">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2054">Optional</span></span> | <span data-ttu-id="b03d2-2055">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2055">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2056">_entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2056">_entityName</span></span> | <span data-ttu-id="b03d2-2057">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2057">str</span></span> | <span data-ttu-id="b03d2-2058">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2058">False</span></span> | <span data-ttu-id="b03d2-2059">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2059">Entity name</span></span>
| <span data-ttu-id="b03d2-2060">_entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2060">_entityId</span></span> | <span data-ttu-id="b03d2-2061">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2061">str</span></span> | <span data-ttu-id="b03d2-2062">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2062">False</span></span> | <span data-ttu-id="b03d2-2063">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2063">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2064">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2064">Return Value</span></span> 
<span data-ttu-id="b03d2-2065">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="b03d2-2065">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="b03d2-2066">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="b03d2-2066">Method constructFromBuffer</span></span> 
<span data-ttu-id="b03d2-2067">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="b03d2-2067">Constructs SysAppEntityContext from table buffer</span></span>

     public SysAppEntityContext constructFromBuffer (Common _tableBuffer) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2068">Parameters</span></span>

| <span data-ttu-id="b03d2-2069">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2069">Parameter name</span></span> |  <span data-ttu-id="b03d2-2070">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2070">Parameter type</span></span> | <span data-ttu-id="b03d2-2071">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2071">Optional</span></span> | <span data-ttu-id="b03d2-2072">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2072">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2073">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="b03d2-2073">_tableBuffer</span></span> | <span data-ttu-id="b03d2-2074">共通</span><span class="sxs-lookup"><span data-stu-id="b03d2-2074">Common</span></span> | <span data-ttu-id="b03d2-2075">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2075">False</span></span> | <span data-ttu-id="b03d2-2076">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2076">table buffer forming the entity</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2077">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2077">Return Value</span></span> 
<span data-ttu-id="b03d2-2078">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="b03d2-2078">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="b03d2-2079">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2079">Method entityName</span></span> 
<span data-ttu-id="b03d2-2080">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2080">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2081">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2081">Parameters</span></span>

| <span data-ttu-id="b03d2-2082">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2082">Parameter name</span></span> |  <span data-ttu-id="b03d2-2083">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2083">Parameter type</span></span> | <span data-ttu-id="b03d2-2084">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2084">Optional</span></span> | <span data-ttu-id="b03d2-2085">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2085">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2086">_entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2086">_entityName</span></span> | <span data-ttu-id="b03d2-2087">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2087">str</span></span> | <span data-ttu-id="b03d2-2088">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2088">True</span></span> | <span data-ttu-id="b03d2-2089">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2089">Entity name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2090">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2090">Return Value</span></span> 
<span data-ttu-id="b03d2-2091">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2091">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="b03d2-2092">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2092">Method entityId</span></span> 
<span data-ttu-id="b03d2-2093">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2093">Field value on which filter applies</span></span>

     public str entityId ([str _entityId]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2094">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2094">Parameters</span></span>

| <span data-ttu-id="b03d2-2095">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2095">Parameter name</span></span> |  <span data-ttu-id="b03d2-2096">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2096">Parameter type</span></span> | <span data-ttu-id="b03d2-2097">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2097">Optional</span></span> | <span data-ttu-id="b03d2-2098">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2098">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2099">_entityId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2099">_entityId</span></span> | <span data-ttu-id="b03d2-2100">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2100">str</span></span> | <span data-ttu-id="b03d2-2101">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2101">True</span></span> | <span data-ttu-id="b03d2-2102">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2102">Entity value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2103">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2103">Return Value</span></span> 
<span data-ttu-id="b03d2-2104">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2104">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="b03d2-2105">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2105">Class SysAppFieldAttribute</span></span> 
<span data-ttu-id="b03d2-2106">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2106">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2107">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2107">Methods</span></span>

| <span data-ttu-id="b03d2-2108">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2108">Method name</span></span> | <span data-ttu-id="b03d2-2109">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2109">Returns</span></span> | <span data-ttu-id="b03d2-2110">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2110">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2111">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2111">new</span></span> | <span data-ttu-id="b03d2-2112">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2112">void</span></span> | <span data-ttu-id="b03d2-2113">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2113">Creates a new instance of SysAppFieldAttribute class</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2114">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2114">Method new</span></span> 
<span data-ttu-id="b03d2-2115">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2115">Creates a new instance of SysAppFieldAttribute class</span></span>

     public void new (str _fieldName, str _label) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2116">Parameters</span></span>

| <span data-ttu-id="b03d2-2117">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2117">Parameter name</span></span> |  <span data-ttu-id="b03d2-2118">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2118">Parameter type</span></span> | <span data-ttu-id="b03d2-2119">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2119">Optional</span></span> | <span data-ttu-id="b03d2-2120">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2120">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2121">_fieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2121">_fieldName</span></span> | <span data-ttu-id="b03d2-2122">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2122">str</span></span> | <span data-ttu-id="b03d2-2123">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2123">False</span></span> | <span data-ttu-id="b03d2-2124">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2124">Entity field name with which control is bound</span></span>
| <span data-ttu-id="b03d2-2125">_label</span><span class="sxs-lookup"><span data-stu-id="b03d2-2125">_label</span></span> | <span data-ttu-id="b03d2-2126">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2126">str</span></span> | <span data-ttu-id="b03d2-2127">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2127">False</span></span> | <span data-ttu-id="b03d2-2128">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-2128">Control label</span></span>


## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="b03d2-2129">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="b03d2-2129">Class SysAppFieldMultiSelectHelper</span></span> 
<span data-ttu-id="b03d2-2130">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2130">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2131">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2131">Methods</span></span>

| <span data-ttu-id="b03d2-2132">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2132">Method name</span></span> | <span data-ttu-id="b03d2-2133">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2133">Returns</span></span> | <span data-ttu-id="b03d2-2134">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2134">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2135">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2135">new</span></span> | <span data-ttu-id="b03d2-2136">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2136">void</span></span> | <span data-ttu-id="b03d2-2137">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2137">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="b03d2-2138">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="b03d2-2138">getSelectedRecIds</span></span> | <span data-ttu-id="b03d2-2139">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-2139">container</span></span> | <span data-ttu-id="b03d2-2140">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2140">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="b03d2-2141">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-2141">getSelectedValues</span></span> | <span data-ttu-id="b03d2-2142">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-2142">container</span></span> | <span data-ttu-id="b03d2-2143">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2143">Returns a container of selected values</span></span> |
| <span data-ttu-id="b03d2-2144">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="b03d2-2144">getSelectedRecords</span></span> | <span data-ttu-id="b03d2-2145">共通</span><span class="sxs-lookup"><span data-stu-id="b03d2-2145">Common</span></span> | <span data-ttu-id="b03d2-2146">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2146">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="b03d2-2147">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2147">The buffer is marked as temp..</span></span>  <span data-ttu-id="b03d2-2148">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2148">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="b03d2-2149">setControlValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-2149">setControlValue</span></span> | <span data-ttu-id="b03d2-2150">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2150">void</span></span> | <span data-ttu-id="b03d2-2151">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2151">A setter to set the multi select control value</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2152">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2152">Method new</span></span> 
<span data-ttu-id="b03d2-2153">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2153">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

     public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2154">Parameters</span></span>

| <span data-ttu-id="b03d2-2155">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2155">Parameter name</span></span> |  <span data-ttu-id="b03d2-2156">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2156">Parameter type</span></span> | <span data-ttu-id="b03d2-2157">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2157">Optional</span></span> | <span data-ttu-id="b03d2-2158">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2158">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2159">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2159">_multiSelectTableId</span></span> | <span data-ttu-id="b03d2-2160">TableId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2160">TableId</span></span> | <span data-ttu-id="b03d2-2161">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2161">False</span></span> | <span data-ttu-id="b03d2-2162">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2162">The backing tableId for the field</span></span>
| <span data-ttu-id="b03d2-2163">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2163">_valueFieldId</span></span> | <span data-ttu-id="b03d2-2164">FieldId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2164">FieldId</span></span> | <span data-ttu-id="b03d2-2165">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2165">False</span></span> | <span data-ttu-id="b03d2-2166">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2166">The fieldId for the field which will be shown in the multi select control</span></span>
| <span data-ttu-id="b03d2-2167">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-2167">_multiSelectControl</span></span> | <span data-ttu-id="b03d2-2168">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-2168">FormStringControl</span></span> | <span data-ttu-id="b03d2-2169">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2169">False</span></span> | <span data-ttu-id="b03d2-2170">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="b03d2-2170">The string control that will be the multi select control</span></span>


### <a name="method-getselectedrecids"></a><span data-ttu-id="b03d2-2171">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="b03d2-2171">Method getSelectedRecIds</span></span> 
<span data-ttu-id="b03d2-2172">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2172">Returns a container of recIds of the records that were selected</span></span>

     public container getSelectedRecIds () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2173">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2173">Return Value</span></span> 
<span data-ttu-id="b03d2-2174">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-2174">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="b03d2-2175">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-2175">Method getSelectedValues</span></span> 
<span data-ttu-id="b03d2-2176">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2176">Returns a container of selected values</span></span>

     public container getSelectedValues () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2177">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2177">Return Value</span></span> 
<span data-ttu-id="b03d2-2178">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="b03d2-2178">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="b03d2-2179">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="b03d2-2179">Method getSelectedRecords</span></span> 
<span data-ttu-id="b03d2-2180">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2180">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="b03d2-2181">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2181">The buffer is marked as temp..</span></span>  <span data-ttu-id="b03d2-2182">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2182">Later a while-Select can be used to iterate through all the records</span></span>

     public Common getSelectedRecords () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2183">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2183">Return Value</span></span> 
<span data-ttu-id="b03d2-2184">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="b03d2-2184">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="b03d2-2185">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-2185">Method setControlValue</span></span> 
<span data-ttu-id="b03d2-2186">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2186">A setter to set the multi select control value</span></span>

     public void setControlValue (str _value) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2187">Parameters</span></span>

| <span data-ttu-id="b03d2-2188">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2188">Parameter name</span></span> |  <span data-ttu-id="b03d2-2189">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2189">Parameter type</span></span> | <span data-ttu-id="b03d2-2190">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2190">Optional</span></span> | <span data-ttu-id="b03d2-2191">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2191">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2192">_value</span><span class="sxs-lookup"><span data-stu-id="b03d2-2192">_value</span></span> | <span data-ttu-id="b03d2-2193">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2193">str</span></span> | <span data-ttu-id="b03d2-2194">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2194">False</span></span> | <span data-ttu-id="b03d2-2195">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2195">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>


## <a name="class-sysappfiltercontext"></a><span data-ttu-id="b03d2-2196">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2196">Class SysAppFilterContext</span></span> 
<span data-ttu-id="b03d2-2197">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-2197">SysAppFilterContext class which holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2198">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2198">Methods</span></span>

| <span data-ttu-id="b03d2-2199">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2199">Method name</span></span> | <span data-ttu-id="b03d2-2200">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2200">Returns</span></span> | <span data-ttu-id="b03d2-2201">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2201">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2202">entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2202">entityName</span></span> | <span data-ttu-id="b03d2-2203">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2203">str</span></span> | <span data-ttu-id="b03d2-2204">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2204">Entity name on which filter applies</span></span> |
| <span data-ttu-id="b03d2-2205">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2205">filterFieldName</span></span> | <span data-ttu-id="b03d2-2206">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2206">str</span></span> | <span data-ttu-id="b03d2-2207">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2207">Field name on which filter applies</span></span> |
| <span data-ttu-id="b03d2-2208">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="b03d2-2208">filterFieldValueList</span></span> | <span data-ttu-id="b03d2-2209">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2209">List</span></span> | <span data-ttu-id="b03d2-2210">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2210">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="b03d2-2211">演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2211">operator</span></span> | <span data-ttu-id="b03d2-2212">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2212">str</span></span> | <span data-ttu-id="b03d2-2213">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2213">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="b03d2-2214">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-2214">addFilterFieldValue</span></span> | <span data-ttu-id="b03d2-2215">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2215">void</span></span> | <span data-ttu-id="b03d2-2216">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-2216">Adds filter field value</span></span> |


### <a name="method-entityname"></a><span data-ttu-id="b03d2-2217">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2217">Method entityName</span></span> 
<span data-ttu-id="b03d2-2218">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2218">Entity name on which filter applies</span></span>

     public str entityName ([str _entityName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2219">Parameters</span></span>

| <span data-ttu-id="b03d2-2220">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2220">Parameter name</span></span> |  <span data-ttu-id="b03d2-2221">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2221">Parameter type</span></span> | <span data-ttu-id="b03d2-2222">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2222">Optional</span></span> | <span data-ttu-id="b03d2-2223">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2223">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2224">_entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2224">_entityName</span></span> | <span data-ttu-id="b03d2-2225">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2225">str</span></span> | <span data-ttu-id="b03d2-2226">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2226">True</span></span> | <span data-ttu-id="b03d2-2227">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2227">Entity name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2228">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2228">Return Value</span></span> 
<span data-ttu-id="b03d2-2229">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2229">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="b03d2-2230">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2230">Method filterFieldName</span></span> 
<span data-ttu-id="b03d2-2231">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2231">Field name on which filter applies</span></span>

     public str filterFieldName ([str _filterFieldName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2232">Parameters</span></span>

| <span data-ttu-id="b03d2-2233">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2233">Parameter name</span></span> |  <span data-ttu-id="b03d2-2234">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2234">Parameter type</span></span> | <span data-ttu-id="b03d2-2235">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2235">Optional</span></span> | <span data-ttu-id="b03d2-2236">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2236">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2237">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2237">_filterFieldName</span></span> | <span data-ttu-id="b03d2-2238">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2238">str</span></span> | <span data-ttu-id="b03d2-2239">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2239">True</span></span> | <span data-ttu-id="b03d2-2240">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2240">Field name on which filter applies</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2241">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2241">Return Value</span></span> 
<span data-ttu-id="b03d2-2242">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2242">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="b03d2-2243">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="b03d2-2243">Method filterFieldValueList</span></span> 
<span data-ttu-id="b03d2-2244">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2244">Gets the list of filter field values based on which filter happens</span></span>

     public List filterFieldValueList () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2245">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2245">Return Value</span></span> 
<span data-ttu-id="b03d2-2246">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2246">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="b03d2-2247">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2247">Method operator</span></span> 
<span data-ttu-id="b03d2-2248">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2248">Operator based on which result will be fetched</span></span>

     public str operator ([str _operator]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2249">Parameters</span></span>

| <span data-ttu-id="b03d2-2250">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2250">Parameter name</span></span> |  <span data-ttu-id="b03d2-2251">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2251">Parameter type</span></span> | <span data-ttu-id="b03d2-2252">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2252">Optional</span></span> | <span data-ttu-id="b03d2-2253">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2253">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2254">_operator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2254">_operator</span></span> | <span data-ttu-id="b03d2-2255">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2255">str</span></span> | <span data-ttu-id="b03d2-2256">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2256">True</span></span> | <span data-ttu-id="b03d2-2257">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2257">Operator based on which result will be fetched</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2258">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2258">Return Value</span></span> 
<span data-ttu-id="b03d2-2259">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2259">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="b03d2-2260">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-2260">Method addFilterFieldValue</span></span> 
<span data-ttu-id="b03d2-2261">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-2261">Adds filter field value</span></span>

     public void addFilterFieldValue ( _filterFieldValueList) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2262">Parameters</span></span>

| <span data-ttu-id="b03d2-2263">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2263">Parameter name</span></span> |  <span data-ttu-id="b03d2-2264">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2264">Parameter type</span></span> | <span data-ttu-id="b03d2-2265">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2265">Optional</span></span> | <span data-ttu-id="b03d2-2266">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2266">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2267">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="b03d2-2267">_filterFieldValueList</span></span> |  | <span data-ttu-id="b03d2-2268">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2268">False</span></span> | <span data-ttu-id="b03d2-2269">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2269">Filter field values based on which filter happens</span></span>


## <a name="class-sysapplookupattribute"></a><span data-ttu-id="b03d2-2270">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2270">Class SysAppLookUpAttribute</span></span> 
<span data-ttu-id="b03d2-2271">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2271">SysAppPageAttribute used for decorating pages that is also lookup page</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2272">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2272">Methods</span></span>

| <span data-ttu-id="b03d2-2273">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2273">Method name</span></span> | <span data-ttu-id="b03d2-2274">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2274">Returns</span></span> | <span data-ttu-id="b03d2-2275">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2275">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2276">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2276">new</span></span> | <span data-ttu-id="b03d2-2277">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2277">void</span></span> | <span data-ttu-id="b03d2-2278">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2278">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="b03d2-2279">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2279">displayFieldName</span></span> | <span data-ttu-id="b03d2-2280">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2280">str</span></span> | <span data-ttu-id="b03d2-2281">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2281">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="b03d2-2282">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2282">valueFieldName</span></span> | <span data-ttu-id="b03d2-2283">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2283">str</span></span> | <span data-ttu-id="b03d2-2284">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2284">Gets the value field name of lookup control</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2285">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2285">Method new</span></span> 
<span data-ttu-id="b03d2-2286">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2286">Creates a new instance of SysAppLookUpAttribute class</span></span>

     public void new (str _displayFieldName, str _valueFieldName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2287">Parameters</span></span>

| <span data-ttu-id="b03d2-2288">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2288">Parameter name</span></span> |  <span data-ttu-id="b03d2-2289">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2289">Parameter type</span></span> | <span data-ttu-id="b03d2-2290">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2290">Optional</span></span> | <span data-ttu-id="b03d2-2291">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2291">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2292">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2292">_displayFieldName</span></span> | <span data-ttu-id="b03d2-2293">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2293">str</span></span> | <span data-ttu-id="b03d2-2294">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2294">False</span></span> | <span data-ttu-id="b03d2-2295">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2295">Lookup display field.</span></span> <span data-ttu-id="b03d2-2296">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-2296">Name of any control of lookup page</span></span>
| <span data-ttu-id="b03d2-2297">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2297">_valueFieldName</span></span> | <span data-ttu-id="b03d2-2298">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2298">str</span></span> | <span data-ttu-id="b03d2-2299">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2299">False</span></span> | <span data-ttu-id="b03d2-2300">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2300">Lookup value field.</span></span> <span data-ttu-id="b03d2-2301">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-2301">Name of control formed by root data contract constructing lookup page</span></span>


### <a name="method-displayfieldname"></a><span data-ttu-id="b03d2-2302">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2302">Method displayFieldName</span></span> 
<span data-ttu-id="b03d2-2303">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2303">Gets the display field name of lookup control</span></span>

     public str displayFieldName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2304">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2304">Return Value</span></span> 
<span data-ttu-id="b03d2-2305">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2305">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="b03d2-2306">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2306">Method valueFieldName</span></span> 
<span data-ttu-id="b03d2-2307">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2307">Gets the value field name of lookup control</span></span>

     public str valueFieldName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2308">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2308">Return Value</span></span> 
<span data-ttu-id="b03d2-2309">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2309">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="b03d2-2310">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2310">Class SysAppLookupFieldAttribute</span></span> 
<span data-ttu-id="b03d2-2311">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2311">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2312">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2312">Methods</span></span>

| <span data-ttu-id="b03d2-2313">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2313">Method name</span></span> | <span data-ttu-id="b03d2-2314">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2314">Returns</span></span> | <span data-ttu-id="b03d2-2315">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2315">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2316">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2316">new</span></span> | <span data-ttu-id="b03d2-2317">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2317">void</span></span> | <span data-ttu-id="b03d2-2318">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2318">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="b03d2-2319">entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2319">entityName</span></span> | <span data-ttu-id="b03d2-2320">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2320">str</span></span> | <span data-ttu-id="b03d2-2321">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2321">Gets the name of the entity with which lookup page is related</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2322">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2322">Method new</span></span> 
<span data-ttu-id="b03d2-2323">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2323">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

     public void new ( _name) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2324">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2324">Parameters</span></span>

| <span data-ttu-id="b03d2-2325">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2325">Parameter name</span></span> |  <span data-ttu-id="b03d2-2326">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2326">Parameter type</span></span> | <span data-ttu-id="b03d2-2327">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2327">Optional</span></span> | <span data-ttu-id="b03d2-2328">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2328">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2329">_name</span><span class="sxs-lookup"><span data-stu-id="b03d2-2329">_name</span></span> |  | <span data-ttu-id="b03d2-2330">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2330">False</span></span> | <span data-ttu-id="b03d2-2331">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-2331">Name of the entity with which lookup page is related</span></span>


### <a name="method-entityname"></a><span data-ttu-id="b03d2-2332">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2332">Method entityName</span></span> 
<span data-ttu-id="b03d2-2333">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2333">Gets the name of the entity with which lookup page is related</span></span>

     public str entityName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2334">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2334">Return Value</span></span> 
<span data-ttu-id="b03d2-2335">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="b03d2-2335">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="b03d2-2336">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2336">Class SysAppPageAttribute</span></span> 
<span data-ttu-id="b03d2-2337">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2337">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2338">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2338">Methods</span></span>

| <span data-ttu-id="b03d2-2339">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2339">Method name</span></span> | <span data-ttu-id="b03d2-2340">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2340">Returns</span></span> | <span data-ttu-id="b03d2-2341">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2341">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2342">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2342">new</span></span> | <span data-ttu-id="b03d2-2343">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2343">void</span></span> | <span data-ttu-id="b03d2-2344">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2344">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="b03d2-2345">pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-2345">pageTitle</span></span> | <span data-ttu-id="b03d2-2346">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2346">str</span></span> | <span data-ttu-id="b03d2-2347">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2347">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="b03d2-2348">pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-2348">pageDescription</span></span> | <span data-ttu-id="b03d2-2349">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2349">str</span></span> | <span data-ttu-id="b03d2-2350">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2350">Gets the Page Description</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2351">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2351">Method new</span></span> 
<span data-ttu-id="b03d2-2352">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2352">Creates a new instance of SysAppPageAttribute class</span></span>

     public void new ([str _pageTitle], [str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2353">Parameters</span></span>

| <span data-ttu-id="b03d2-2354">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2354">Parameter name</span></span> |  <span data-ttu-id="b03d2-2355">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2355">Parameter type</span></span> | <span data-ttu-id="b03d2-2356">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2356">Optional</span></span> | <span data-ttu-id="b03d2-2357">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2357">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2358">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-2358">_pageTitle</span></span> | <span data-ttu-id="b03d2-2359">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2359">str</span></span> | <span data-ttu-id="b03d2-2360">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2360">True</span></span> | <span data-ttu-id="b03d2-2361">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-2361">The page title</span></span>
| <span data-ttu-id="b03d2-2362">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-2362">_pageDescription</span></span> | <span data-ttu-id="b03d2-2363">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2363">str</span></span> | <span data-ttu-id="b03d2-2364">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2364">True</span></span> | <span data-ttu-id="b03d2-2365">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2365">The page description</span></span>


### <a name="method-pagetitle"></a><span data-ttu-id="b03d2-2366">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-2366">Method pageTitle</span></span> 
<span data-ttu-id="b03d2-2367">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2367">Gets the Page Title of the page</span></span>

     public str pageTitle () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2368">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2368">Return Value</span></span> 
<span data-ttu-id="b03d2-2369">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-2369">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="b03d2-2370">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-2370">Method pageDescription</span></span> 
<span data-ttu-id="b03d2-2371">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2371">Gets the Page Description</span></span>

     public str pageDescription () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2372">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2372">Return Value</span></span> 
<span data-ttu-id="b03d2-2373">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2373">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="b03d2-2374">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2374">Class SysAppPageMetadata</span></span> 
<span data-ttu-id="b03d2-2375">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2375">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2376">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2376">Methods</span></span>

| <span data-ttu-id="b03d2-2377">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2377">Method name</span></span> | <span data-ttu-id="b03d2-2378">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2378">Returns</span></span> | <span data-ttu-id="b03d2-2379">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2379">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2380">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2380">new</span></span> | <span data-ttu-id="b03d2-2381">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2381">void</span></span> |  |
| <span data-ttu-id="b03d2-2382">getPageName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2382">getPageName</span></span> | <span data-ttu-id="b03d2-2383">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2383">str</span></span> | <span data-ttu-id="b03d2-2384">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2384">Returns the page name</span></span> |
| <span data-ttu-id="b03d2-2385">pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-2385">pageTitle</span></span> | <span data-ttu-id="b03d2-2386">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2386">str</span></span> | <span data-ttu-id="b03d2-2387">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2387">Gets and sets the page title</span></span> |
| <span data-ttu-id="b03d2-2388">pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-2388">pageDescription</span></span> | <span data-ttu-id="b03d2-2389">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2389">str</span></span> | <span data-ttu-id="b03d2-2390">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2390">Gets or sets the page description</span></span> |
| <span data-ttu-id="b03d2-2391">pageHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2391">pageHidden</span></span> | <span data-ttu-id="b03d2-2392">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2392">boolean</span></span> | <span data-ttu-id="b03d2-2393">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2393">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="b03d2-2394">pageOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-2394">pageOrder</span></span> | <span data-ttu-id="b03d2-2395">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-2395">int</span></span> | <span data-ttu-id="b03d2-2396">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2396">Gets or sets the page order</span></span> |
| <span data-ttu-id="b03d2-2397">getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-2397">getControl</span></span> | <span data-ttu-id="b03d2-2398">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2398">SysAppControlMetadata</span></span> | <span data-ttu-id="b03d2-2399">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2399">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="b03d2-2400">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2400">getControlEnumerator</span></span> | <span data-ttu-id="b03d2-2401">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2401">MapEnumerator</span></span> | <span data-ttu-id="b03d2-2402">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2402">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="b03d2-2403">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-2403">Where Key is control name and value is of type SysAppControlMetadata</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2404">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2404">Method new</span></span> 


     public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2405">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2405">Parameters</span></span>

| <span data-ttu-id="b03d2-2406">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2406">Parameter name</span></span> |  <span data-ttu-id="b03d2-2407">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2407">Parameter type</span></span> | <span data-ttu-id="b03d2-2408">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2408">Optional</span></span> | <span data-ttu-id="b03d2-2409">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2409">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2410">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2410">_pageMetadata</span></span> | <span data-ttu-id="b03d2-2411">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2411">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="b03d2-2412">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2412">False</span></span> | 


### <a name="method-getpagename"></a><span data-ttu-id="b03d2-2413">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2413">Method getPageName</span></span> 
<span data-ttu-id="b03d2-2414">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2414">Returns the page name</span></span>

     public str getPageName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2415">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2415">Return Value</span></span> 
<span data-ttu-id="b03d2-2416">ページ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2416">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="b03d2-2417">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-2417">Method pageTitle</span></span> 
<span data-ttu-id="b03d2-2418">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2418">Gets and sets the page title</span></span>

     public str pageTitle ([str _pageTitle]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2419">Parameters</span></span>

| <span data-ttu-id="b03d2-2420">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2420">Parameter name</span></span> |  <span data-ttu-id="b03d2-2421">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2421">Parameter type</span></span> | <span data-ttu-id="b03d2-2422">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2422">Optional</span></span> | <span data-ttu-id="b03d2-2423">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2423">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2424">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-2424">_pageTitle</span></span> | <span data-ttu-id="b03d2-2425">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2425">str</span></span> | <span data-ttu-id="b03d2-2426">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2426">True</span></span> | <span data-ttu-id="b03d2-2427">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-2427">The page title</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2428">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2428">Return Value</span></span> 
<span data-ttu-id="b03d2-2429">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-2429">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="b03d2-2430">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-2430">Method pageDescription</span></span> 
<span data-ttu-id="b03d2-2431">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2431">Gets or sets the page description</span></span>

     public str pageDescription ([str _pageDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2432">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2432">Parameters</span></span>

| <span data-ttu-id="b03d2-2433">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2433">Parameter name</span></span> |  <span data-ttu-id="b03d2-2434">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2434">Parameter type</span></span> | <span data-ttu-id="b03d2-2435">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2435">Optional</span></span> | <span data-ttu-id="b03d2-2436">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2436">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2437">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-2437">_pageDescription</span></span> | <span data-ttu-id="b03d2-2438">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2438">str</span></span> | <span data-ttu-id="b03d2-2439">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2439">True</span></span> | <span data-ttu-id="b03d2-2440">ページの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2440">The page description</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2441">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2441">Return Value</span></span> 
<span data-ttu-id="b03d2-2442">ページの説明></span><span class="sxs-lookup"><span data-stu-id="b03d2-2442">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="b03d2-2443">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2443">Method pageHidden</span></span> 
<span data-ttu-id="b03d2-2444">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2444">Gets and sets whether the page is hidden in the workspace</span></span>

     public boolean pageHidden ([boolean _pageHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2445">Parameters</span></span>

| <span data-ttu-id="b03d2-2446">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2446">Parameter name</span></span> |  <span data-ttu-id="b03d2-2447">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2447">Parameter type</span></span> | <span data-ttu-id="b03d2-2448">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2448">Optional</span></span> | <span data-ttu-id="b03d2-2449">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2449">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2450">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2450">_pageHidden</span></span> | <span data-ttu-id="b03d2-2451">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2451">boolean</span></span> | <span data-ttu-id="b03d2-2452">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2452">True</span></span> | <span data-ttu-id="b03d2-2453">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2453">page hidden value</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2454">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2454">Return Value</span></span> 
<span data-ttu-id="b03d2-2455">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2455">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="b03d2-2456">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-2456">Method pageOrder</span></span> 
<span data-ttu-id="b03d2-2457">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2457">Gets or sets the page order</span></span>

     public int pageOrder ([int _pageOrder]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2458">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2458">Parameters</span></span>

| <span data-ttu-id="b03d2-2459">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2459">Parameter name</span></span> |  <span data-ttu-id="b03d2-2460">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2460">Parameter type</span></span> | <span data-ttu-id="b03d2-2461">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2461">Optional</span></span> | <span data-ttu-id="b03d2-2462">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2462">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2463">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="b03d2-2463">_pageOrder</span></span> | <span data-ttu-id="b03d2-2464">int</span><span class="sxs-lookup"><span data-stu-id="b03d2-2464">int</span></span> | <span data-ttu-id="b03d2-2465">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2465">True</span></span> | <span data-ttu-id="b03d2-2466">ページの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-2466">The page order</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2467">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2467">Return Value</span></span> 
<span data-ttu-id="b03d2-2468">ページの順序</span><span class="sxs-lookup"><span data-stu-id="b03d2-2468">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="b03d2-2469">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="b03d2-2469">Method getControl</span></span> 
<span data-ttu-id="b03d2-2470">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2470">Returns the control on the current page having the provided control name</span></span>

     public SysAppControlMetadata getControl (str _controlName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2471">Parameters</span></span>

| <span data-ttu-id="b03d2-2472">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2472">Parameter name</span></span> |  <span data-ttu-id="b03d2-2473">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2473">Parameter type</span></span> | <span data-ttu-id="b03d2-2474">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2474">Optional</span></span> | <span data-ttu-id="b03d2-2475">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2475">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2476">_controlName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2476">_controlName</span></span> | <span data-ttu-id="b03d2-2477">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2477">str</span></span> | <span data-ttu-id="b03d2-2478">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2478">False</span></span> | <span data-ttu-id="b03d2-2479">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2479">The control name that will be used to search for control</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2480">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2480">Return Value</span></span> 
<span data-ttu-id="b03d2-2481">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="b03d2-2481">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="b03d2-2482">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2482">Method getControlEnumerator</span></span> 
<span data-ttu-id="b03d2-2483">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2483">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="b03d2-2484">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-2484">Where Key is control name and value is of type SysAppControlMetadata</span></span>

     public MapEnumerator getControlEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2485">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2485">Return Value</span></span> 
<span data-ttu-id="b03d2-2486">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2486">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="b03d2-2487">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2487">Class SysAppProjectionAttribute</span></span> 
<span data-ttu-id="b03d2-2488">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2488">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2489">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2489">Methods</span></span>

| <span data-ttu-id="b03d2-2490">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2490">Method name</span></span> | <span data-ttu-id="b03d2-2491">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2491">Returns</span></span> | <span data-ttu-id="b03d2-2492">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2492">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2493">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2493">new</span></span> | <span data-ttu-id="b03d2-2494">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2494">void</span></span> | <span data-ttu-id="b03d2-2495">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2495">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2496">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2496">Method new</span></span> 
<span data-ttu-id="b03d2-2497">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2497">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

     public void new (str _label) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2498">Parameters</span></span>

| <span data-ttu-id="b03d2-2499">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2499">Parameter name</span></span> |  <span data-ttu-id="b03d2-2500">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2500">Parameter type</span></span> | <span data-ttu-id="b03d2-2501">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2501">Optional</span></span> | <span data-ttu-id="b03d2-2502">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2502">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2503">_label</span><span class="sxs-lookup"><span data-stu-id="b03d2-2503">_label</span></span> | <span data-ttu-id="b03d2-2504">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2504">str</span></span> | <span data-ttu-id="b03d2-2505">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2505">False</span></span> | <span data-ttu-id="b03d2-2506">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="b03d2-2506">Control label</span></span>


## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="b03d2-2507">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2507">Class SysAppRelationalAttribute</span></span> 
<span data-ttu-id="b03d2-2508">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2508">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2509">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2509">Methods</span></span>

| <span data-ttu-id="b03d2-2510">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2510">Method name</span></span> | <span data-ttu-id="b03d2-2511">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2511">Returns</span></span> | <span data-ttu-id="b03d2-2512">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2512">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2513">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2513">new</span></span> | <span data-ttu-id="b03d2-2514">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2514">void</span></span> | <span data-ttu-id="b03d2-2515">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2515">Constructor</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2516">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2516">Method new</span></span> 
<span data-ttu-id="b03d2-2517">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2517">Constructor</span></span>

     public void new ([str _name]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2518">Parameters</span></span>

| <span data-ttu-id="b03d2-2519">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2519">Parameter name</span></span> |  <span data-ttu-id="b03d2-2520">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2520">Parameter type</span></span> | <span data-ttu-id="b03d2-2521">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2521">Optional</span></span> | <span data-ttu-id="b03d2-2522">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2522">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2523">_name</span><span class="sxs-lookup"><span data-stu-id="b03d2-2523">_name</span></span> | <span data-ttu-id="b03d2-2524">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2524">str</span></span> | <span data-ttu-id="b03d2-2525">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2525">True</span></span> | <span data-ttu-id="b03d2-2526">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2526">Property name of the referenced entity</span></span>


## <a name="class-sysapprequestparams"></a><span data-ttu-id="b03d2-2527">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="b03d2-2527">Class SysAppRequestParams</span></span> 
<span data-ttu-id="b03d2-2528">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2528">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2529">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2529">Methods</span></span>

| <span data-ttu-id="b03d2-2530">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2530">Method name</span></span> | <span data-ttu-id="b03d2-2531">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2531">Returns</span></span> | <span data-ttu-id="b03d2-2532">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2532">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2533">entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2533">entityContext</span></span> | <span data-ttu-id="b03d2-2534">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2534">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-2535">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2535">Entity context of the request</span></span> |
| <span data-ttu-id="b03d2-2536">filterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2536">filterContext</span></span> | <span data-ttu-id="b03d2-2537">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2537">List</span></span> | <span data-ttu-id="b03d2-2538">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2538">List of SysAppFilterContext for filter contexts</span></span> |


### <a name="method-entitycontext"></a><span data-ttu-id="b03d2-2539">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2539">Method entityContext</span></span> 
<span data-ttu-id="b03d2-2540">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2540">Entity context of the request</span></span>

     public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2541">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2541">Parameters</span></span>

| <span data-ttu-id="b03d2-2542">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2542">Parameter name</span></span> |  <span data-ttu-id="b03d2-2543">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2543">Parameter type</span></span> | <span data-ttu-id="b03d2-2544">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2544">Optional</span></span> | <span data-ttu-id="b03d2-2545">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2545">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2546">_entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2546">_entityContext</span></span> | <span data-ttu-id="b03d2-2547">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2547">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-2548">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2548">True</span></span> | <span data-ttu-id="b03d2-2549">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2549">Entity context of the request</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2550">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2550">Return Value</span></span> 
<span data-ttu-id="b03d2-2551">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2551">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="b03d2-2552">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2552">Method filterContext</span></span> 
<span data-ttu-id="b03d2-2553">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2553">List of SysAppFilterContext for filter contexts</span></span>

     public List filterContext ([List _filterContext]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2554">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2554">Parameters</span></span>

| <span data-ttu-id="b03d2-2555">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2555">Parameter name</span></span> |  <span data-ttu-id="b03d2-2556">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2556">Parameter type</span></span> | <span data-ttu-id="b03d2-2557">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2557">Optional</span></span> | <span data-ttu-id="b03d2-2558">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2558">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2559">_filterContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2559">_filterContext</span></span> | <span data-ttu-id="b03d2-2560">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2560">List</span></span> | <span data-ttu-id="b03d2-2561">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2561">True</span></span> | <span data-ttu-id="b03d2-2562">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2562">List of SysAppFilterContext for filter contexts of page</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2563">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2563">Return Value</span></span> 
<span data-ttu-id="b03d2-2564">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2564">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="b03d2-2565">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="b03d2-2565">Class SysAppResponse</span></span> 
<span data-ttu-id="b03d2-2566">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2566">SysAppResponse class.</span></span>  <span data-ttu-id="b03d2-2567">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2567">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2568">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2568">Methods</span></span>

| <span data-ttu-id="b03d2-2569">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2569">Method name</span></span> | <span data-ttu-id="b03d2-2570">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2570">Returns</span></span> | <span data-ttu-id="b03d2-2571">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2571">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2572">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2572">new</span></span> | <span data-ttu-id="b03d2-2573">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2573">void</span></span> |  |
| <span data-ttu-id="b03d2-2574">jobId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2574">jobId</span></span> | <span data-ttu-id="b03d2-2575">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2575">str</span></span> | <span data-ttu-id="b03d2-2576">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-2576">Job Id of the request</span></span> |
| <span data-ttu-id="b03d2-2577">データ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2577">data</span></span> | <span data-ttu-id="b03d2-2578">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="b03d2-2578">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="b03d2-2579">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2579">Data of the page</span></span> |
| <span data-ttu-id="b03d2-2580">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="b03d2-2580">failedInAppCall</span></span> | <span data-ttu-id="b03d2-2581">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2581">boolean</span></span> | <span data-ttu-id="b03d2-2582">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2582">Data of the page</span></span> |
| <span data-ttu-id="b03d2-2583">commits</span><span class="sxs-lookup"><span data-stu-id="b03d2-2583">commits</span></span> | <span data-ttu-id="b03d2-2584">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2584">List</span></span> | <span data-ttu-id="b03d2-2585">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2585">Commits after task is completed</span></span> |
| <span data-ttu-id="b03d2-2586">メッセージ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2586">messages</span></span> | <span data-ttu-id="b03d2-2587">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2587">List</span></span> | <span data-ttu-id="b03d2-2588">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-2588">Job Id of the request</span></span> |
| <span data-ttu-id="b03d2-2589">addMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-2589">addMessage</span></span> | <span data-ttu-id="b03d2-2590">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2590">void</span></span> | <span data-ttu-id="b03d2-2591">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-2591">Adds message</span></span> |
| <span data-ttu-id="b03d2-2592">addCommit</span><span class="sxs-lookup"><span data-stu-id="b03d2-2592">addCommit</span></span> | <span data-ttu-id="b03d2-2593">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2593">void</span></span> | <span data-ttu-id="b03d2-2594">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-2594">Adds commits</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2595">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2595">Method new</span></span> 


     public void new () 


### <a name="method-jobid"></a><span data-ttu-id="b03d2-2596">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2596">Method jobId</span></span> 
<span data-ttu-id="b03d2-2597">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-2597">Job Id of the request</span></span>

     public str jobId () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2598">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2598">Return Value</span></span> 
<span data-ttu-id="b03d2-2599">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-2599">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="b03d2-2600">メソッド data</span><span class="sxs-lookup"><span data-stu-id="b03d2-2600">Method data</span></span> 
<span data-ttu-id="b03d2-2601">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2601">Data of the page</span></span>

     public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2602">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2602">Parameters</span></span>

| <span data-ttu-id="b03d2-2603">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2603">Parameter name</span></span> |  <span data-ttu-id="b03d2-2604">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2604">Parameter type</span></span> | <span data-ttu-id="b03d2-2605">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2605">Optional</span></span> | <span data-ttu-id="b03d2-2606">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2606">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2607">_data</span><span class="sxs-lookup"><span data-stu-id="b03d2-2607">_data</span></span> | <span data-ttu-id="b03d2-2608">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="b03d2-2608">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="b03d2-2609">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2609">True</span></span> | <span data-ttu-id="b03d2-2610">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2610">Data of the page</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2611">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2611">Return Value</span></span> 
<span data-ttu-id="b03d2-2612">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2612">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="b03d2-2613">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="b03d2-2613">Method failedInAppCall</span></span> 
<span data-ttu-id="b03d2-2614">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2614">Data of the page</span></span>

     public boolean failedInAppCall ([boolean _failedInAppCall]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2615">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2615">Parameters</span></span>

| <span data-ttu-id="b03d2-2616">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2616">Parameter name</span></span> |  <span data-ttu-id="b03d2-2617">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2617">Parameter type</span></span> | <span data-ttu-id="b03d2-2618">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2618">Optional</span></span> | <span data-ttu-id="b03d2-2619">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2619">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2620">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="b03d2-2620">_failedInAppCall</span></span> | <span data-ttu-id="b03d2-2621">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2621">boolean</span></span> | <span data-ttu-id="b03d2-2622">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2622">True</span></span> | <span data-ttu-id="b03d2-2623">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2623">Sets to true if it fails in calling application code</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2624">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2624">Return Value</span></span> 
<span data-ttu-id="b03d2-2625">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2625">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="b03d2-2626">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="b03d2-2626">Method commits</span></span> 
<span data-ttu-id="b03d2-2627">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2627">Commits after task is completed</span></span>

     public List commits () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2628">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2628">Return Value</span></span> 
<span data-ttu-id="b03d2-2629">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2629">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="b03d2-2630">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="b03d2-2630">Method messages</span></span> 
<span data-ttu-id="b03d2-2631">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="b03d2-2631">Job Id of the request</span></span>

     public List messages () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2632">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2632">Return Value</span></span> 
<span data-ttu-id="b03d2-2633">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2633">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="b03d2-2634">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-2634">Method addMessage</span></span> 
<span data-ttu-id="b03d2-2635">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-2635">Adds message</span></span>

     public void addMessage (SysAppResponseMessage _message) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2636">Parameters</span></span>

| <span data-ttu-id="b03d2-2637">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2637">Parameter name</span></span> |  <span data-ttu-id="b03d2-2638">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2638">Parameter type</span></span> | <span data-ttu-id="b03d2-2639">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2639">Optional</span></span> | <span data-ttu-id="b03d2-2640">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2640">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2641">_message</span><span class="sxs-lookup"><span data-stu-id="b03d2-2641">_message</span></span> | <span data-ttu-id="b03d2-2642">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-2642">SysAppResponseMessage</span></span> | <span data-ttu-id="b03d2-2643">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2643">False</span></span> | <span data-ttu-id="b03d2-2644">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2644">message as SysAppResponseMessage object</span></span>


### <a name="method-addcommit"></a><span data-ttu-id="b03d2-2645">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="b03d2-2645">Method addCommit</span></span> 
<span data-ttu-id="b03d2-2646">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="b03d2-2646">Adds commits</span></span>

     public void addCommit (SysAppEntityContext _entityContext) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2647">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2647">Parameters</span></span>

| <span data-ttu-id="b03d2-2648">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2648">Parameter name</span></span> |  <span data-ttu-id="b03d2-2649">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2649">Parameter type</span></span> | <span data-ttu-id="b03d2-2650">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2650">Optional</span></span> | <span data-ttu-id="b03d2-2651">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2651">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2652">_entityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2652">_entityContext</span></span> | <span data-ttu-id="b03d2-2653">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="b03d2-2653">SysAppEntityContext</span></span> | <span data-ttu-id="b03d2-2654">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2654">False</span></span> | <span data-ttu-id="b03d2-2655">確定済のエンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2655">Entity context containing entity name and entity id of the entity that is committed</span></span>


## <a name="class-sysappresponsemessage"></a><span data-ttu-id="b03d2-2656">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b03d2-2656">Class SysAppResponseMessage</span></span> 
<span data-ttu-id="b03d2-2657">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-2657">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2658">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2658">Methods</span></span>

| <span data-ttu-id="b03d2-2659">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2659">Method name</span></span> | <span data-ttu-id="b03d2-2660">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2660">Returns</span></span> | <span data-ttu-id="b03d2-2661">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2661">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2662">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2662">new</span></span> | <span data-ttu-id="b03d2-2663">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2663">void</span></span> | <span data-ttu-id="b03d2-2664">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2664">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="b03d2-2665">テキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2665">text</span></span> | <span data-ttu-id="b03d2-2666">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2666">str</span></span> | <span data-ttu-id="b03d2-2667">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2667">Gets the message text</span></span> |
| <span data-ttu-id="b03d2-2668">タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2668">type</span></span> | <span data-ttu-id="b03d2-2669">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="b03d2-2669">SysAppMessageType</span></span> | <span data-ttu-id="b03d2-2670">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-2670">Gets the message type: info, error , warning</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2671">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2671">Method new</span></span> 
<span data-ttu-id="b03d2-2672">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2672">Creates a new instance of SysAppResponseMessage class</span></span>

     public void new (str _text, [SysAppMessageType _type]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2673">Parameters</span></span>

| <span data-ttu-id="b03d2-2674">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2674">Parameter name</span></span> |  <span data-ttu-id="b03d2-2675">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2675">Parameter type</span></span> | <span data-ttu-id="b03d2-2676">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2676">Optional</span></span> | <span data-ttu-id="b03d2-2677">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2677">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2678">_text</span><span class="sxs-lookup"><span data-stu-id="b03d2-2678">_text</span></span> | <span data-ttu-id="b03d2-2679">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2679">str</span></span> | <span data-ttu-id="b03d2-2680">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2680">False</span></span> | <span data-ttu-id="b03d2-2681">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2681">The message text</span></span>
| <span data-ttu-id="b03d2-2682">_type</span><span class="sxs-lookup"><span data-stu-id="b03d2-2682">_type</span></span> | <span data-ttu-id="b03d2-2683">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="b03d2-2683">SysAppMessageType</span></span> | <span data-ttu-id="b03d2-2684">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2684">True</span></span> | <span data-ttu-id="b03d2-2685">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-2685">Message Type: info, error , warning</span></span>


### <a name="method-text"></a><span data-ttu-id="b03d2-2686">メソッド text</span><span class="sxs-lookup"><span data-stu-id="b03d2-2686">Method text</span></span> 
<span data-ttu-id="b03d2-2687">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2687">Gets the message text</span></span>

     public str text () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2688">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2688">Return Value</span></span> 
<span data-ttu-id="b03d2-2689">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2689">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="b03d2-2690">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2690">Method type</span></span> 
<span data-ttu-id="b03d2-2691">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-2691">Gets the message type: info, error , warning</span></span>

     public SysAppMessageType type () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2692">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2692">Return Value</span></span> 
<span data-ttu-id="b03d2-2693">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="b03d2-2693">The message type: info, error , warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="b03d2-2694">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2694">Class SysAppSecurityAttribute</span></span> 
<span data-ttu-id="b03d2-2695">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2695">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="b03d2-2696">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2696">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2697">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2697">Methods</span></span>

| <span data-ttu-id="b03d2-2698">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2698">Method name</span></span> | <span data-ttu-id="b03d2-2699">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2699">Returns</span></span> | <span data-ttu-id="b03d2-2700">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2700">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2701">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2701">new</span></span> | <span data-ttu-id="b03d2-2702">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2702">void</span></span> | <span data-ttu-id="b03d2-2703">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2703">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="b03d2-2704">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2704">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="b03d2-2705">menuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-2705">menuItemType</span></span> | <span data-ttu-id="b03d2-2706">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-2706">MenuItemType</span></span> | <span data-ttu-id="b03d2-2707">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2707">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="b03d2-2708">menuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2708">menuItemName</span></span> | <span data-ttu-id="b03d2-2709">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2709">MenuItemName</span></span> | <span data-ttu-id="b03d2-2710">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2710">Gets the Menu Item Name of the page</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2711">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2711">Method new</span></span> 
<span data-ttu-id="b03d2-2712">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2712">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="b03d2-2713">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2713">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

     public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2714">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2714">Parameters</span></span>

| <span data-ttu-id="b03d2-2715">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2715">Parameter name</span></span> |  <span data-ttu-id="b03d2-2716">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2716">Parameter type</span></span> | <span data-ttu-id="b03d2-2717">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2717">Optional</span></span> | <span data-ttu-id="b03d2-2718">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2718">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2719">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2719">_menuItemName</span></span> | <span data-ttu-id="b03d2-2720">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2720">MenuItemName</span></span> | <span data-ttu-id="b03d2-2721">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2721">True</span></span> | <span data-ttu-id="b03d2-2722">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2722">Menu Item Name of the page</span></span>
| <span data-ttu-id="b03d2-2723">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-2723">_menuItemType</span></span> | <span data-ttu-id="b03d2-2724">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-2724">MenuItemType</span></span> | <span data-ttu-id="b03d2-2725">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2725">True</span></span> | <span data-ttu-id="b03d2-2726">アクション、表示または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2726">Menu Item Type of the page like action, display or output</span></span>


### <a name="method-menuitemtype"></a><span data-ttu-id="b03d2-2727">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-2727">Method menuItemType</span></span> 
<span data-ttu-id="b03d2-2728">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2728">Gets the Menu Item Type of the page</span></span>

     public MenuItemType menuItemType () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2729">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2729">Return Value</span></span> 
<span data-ttu-id="b03d2-2730">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2730">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="b03d2-2731">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2731">Method menuItemName</span></span> 
<span data-ttu-id="b03d2-2732">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="b03d2-2732">Gets the Menu Item Name of the page</span></span>

     public MenuItemName menuItemName () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2733">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2733">Return Value</span></span> 
<span data-ttu-id="b03d2-2734">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2734">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="b03d2-2735">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="b03d2-2735">Class SysAppWorkspace</span></span> 
<span data-ttu-id="b03d2-2736">これは、AX モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2736">This is the base class of AX mobile workspace.</span></span> <span data-ttu-id="b03d2-2737">AX モバイル ワークスペース クラスは、このクラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2737">AX mobile workspace classes needs to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2738">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2738">Methods</span></span>

| <span data-ttu-id="b03d2-2739">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2739">Method name</span></span> | <span data-ttu-id="b03d2-2740">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2740">Returns</span></span> | <span data-ttu-id="b03d2-2741">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2741">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2742">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-2742">getEnumValues</span></span> | <span data-ttu-id="b03d2-2743">リスト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2743">List</span></span> | <span data-ttu-id="b03d2-2744">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2744">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-2745">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2745">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="b03d2-2746">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2746">getWorkspaceMetadata</span></span> | <span data-ttu-id="b03d2-2747">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2747">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="b03d2-2748">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2748">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-2749">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2749">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="b03d2-2750">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-2750">onBeginAppJob</span></span> | <span data-ttu-id="b03d2-2751">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2751">void</span></span> | <span data-ttu-id="b03d2-2752">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-2752">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="b03d2-2753">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-2753">onEndAppJob</span></span> | <span data-ttu-id="b03d2-2754">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2754">void</span></span> | <span data-ttu-id="b03d2-2755">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-2755">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="b03d2-2756">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2756">workspaceHidden</span></span> | <span data-ttu-id="b03d2-2757">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2757">boolean</span></span> | <span data-ttu-id="b03d2-2758">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2758">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="b03d2-2759">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2759">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="b03d2-2760">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2760">If the attribute is not specified on the class than it always returns false</span></span> |


### <a name="method-getenumvalues"></a><span data-ttu-id="b03d2-2761">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="b03d2-2761">Method getEnumValues</span></span> 
<span data-ttu-id="b03d2-2762">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2762">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-2763">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2763">Can be used to modify the enum values that are returned to AX mobile</span></span>

     public List getEnumValues (EnumName _enumName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2764">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2764">Parameters</span></span>

| <span data-ttu-id="b03d2-2765">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2765">Parameter name</span></span> |  <span data-ttu-id="b03d2-2766">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2766">Parameter type</span></span> | <span data-ttu-id="b03d2-2767">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2767">Optional</span></span> | <span data-ttu-id="b03d2-2768">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2768">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2769">_enumName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2769">_enumName</span></span> | <span data-ttu-id="b03d2-2770">EnumName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2770">EnumName</span></span> | <span data-ttu-id="b03d2-2771">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2771">False</span></span> | <span data-ttu-id="b03d2-2772">列挙名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2772">The enum name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2773">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2773">Return Value</span></span> 
<span data-ttu-id="b03d2-2774">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="b03d2-2774">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="b03d2-2775">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2775">Method getWorkspaceMetadata</span></span> 
<span data-ttu-id="b03d2-2776">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2776">Called during workspace initialization.</span></span> <span data-ttu-id="b03d2-2777">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="b03d2-2777">Can be used to modify the workspace metadata</span></span>

     public SysAppWorkspaceMetadata getWorkspaceMetadata () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2778">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2778">Return Value</span></span> 
<span data-ttu-id="b03d2-2779">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2779">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="b03d2-2780">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-2780">Method onBeginAppJob</span></span> 
<span data-ttu-id="b03d2-2781">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-2781">Called before the start of execution of AX mobile job</span></span>

     public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2782">Parameters</span></span>

| <span data-ttu-id="b03d2-2783">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2783">Parameter name</span></span> |  <span data-ttu-id="b03d2-2784">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2784">Parameter type</span></span> | <span data-ttu-id="b03d2-2785">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2785">Optional</span></span> | <span data-ttu-id="b03d2-2786">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2786">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2787">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="b03d2-2787">_sysAppJobRequest</span></span> | <span data-ttu-id="b03d2-2788">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="b03d2-2788">SysAppJobRequest</span></span> | <span data-ttu-id="b03d2-2789">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2789">False</span></span> | <span data-ttu-id="b03d2-2790">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-2790">A class containing job request parameters</span></span>


### <a name="method-onendappjob"></a><span data-ttu-id="b03d2-2791">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="b03d2-2791">Method onEndAppJob</span></span> 
<span data-ttu-id="b03d2-2792">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="b03d2-2792">Called after the end of execution of AX mobile job</span></span>

     public void onEndAppJob (SysAppJobResponse _sysAppJobResponse) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2793">Parameters</span></span>

| <span data-ttu-id="b03d2-2794">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2794">Parameter name</span></span> |  <span data-ttu-id="b03d2-2795">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2795">Parameter type</span></span> | <span data-ttu-id="b03d2-2796">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2796">Optional</span></span> | <span data-ttu-id="b03d2-2797">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2797">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2798">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="b03d2-2798">_sysAppJobResponse</span></span> | <span data-ttu-id="b03d2-2799">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="b03d2-2799">SysAppJobResponse</span></span> | <span data-ttu-id="b03d2-2800">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2800">False</span></span> | <span data-ttu-id="b03d2-2801">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="b03d2-2801">A class containing job response parameters</span></span>


### <a name="method-workspacehidden"></a><span data-ttu-id="b03d2-2802">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2802">Method workspaceHidden</span></span> 
<span data-ttu-id="b03d2-2803">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2803">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="b03d2-2804">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2804">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="b03d2-2805">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2805">If the attribute is not specified on the class than it always returns false</span></span>

     public boolean workspaceHidden () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2806">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2806">Return Value</span></span> 
<span data-ttu-id="b03d2-2807">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2807">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="b03d2-2808">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2808">Class SysAppWorkspaceAttribute</span></span> 
<span data-ttu-id="b03d2-2809">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2809">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2810">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2810">Methods</span></span>

| <span data-ttu-id="b03d2-2811">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2811">Method name</span></span> | <span data-ttu-id="b03d2-2812">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2812">Returns</span></span> | <span data-ttu-id="b03d2-2813">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2813">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2814">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2814">new</span></span> | <span data-ttu-id="b03d2-2815">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2815">void</span></span> | <span data-ttu-id="b03d2-2816">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2816">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="b03d2-2817">AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2817">AppId</span></span> | <span data-ttu-id="b03d2-2818">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2818">str</span></span> | <span data-ttu-id="b03d2-2819">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2819">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="b03d2-2820">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2820">AppResourceName</span></span> | <span data-ttu-id="b03d2-2821">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2821">str</span></span> | <span data-ttu-id="b03d2-2822">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2822">Gets or sets the AOT Resource name which contains the workspace</span></span> |
| <span data-ttu-id="b03d2-2823">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2823">WorkspaceHidden</span></span> | <span data-ttu-id="b03d2-2824">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2824">boolean</span></span> | <span data-ttu-id="b03d2-2825">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2825">Gets or sets if the workspace is hidden from designer</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2826">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2826">Method new</span></span> 
<span data-ttu-id="b03d2-2827">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="b03d2-2827">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

     public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2828">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2828">Parameters</span></span>

| <span data-ttu-id="b03d2-2829">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2829">Parameter name</span></span> |  <span data-ttu-id="b03d2-2830">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2830">Parameter type</span></span> | <span data-ttu-id="b03d2-2831">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2831">Optional</span></span> | <span data-ttu-id="b03d2-2832">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2832">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2833">_appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2833">_appId</span></span> | <span data-ttu-id="b03d2-2834">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2834">str</span></span> | <span data-ttu-id="b03d2-2835">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2835">False</span></span> | <span data-ttu-id="b03d2-2836">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2836">The appId of the workspace</span></span>
| <span data-ttu-id="b03d2-2837">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2837">_appResourceName</span></span> | <span data-ttu-id="b03d2-2838">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2838">str</span></span> | <span data-ttu-id="b03d2-2839">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2839">True</span></span> | <span data-ttu-id="b03d2-2840">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2840">The AOT resource name which contains the workspace</span></span>
| <span data-ttu-id="b03d2-2841">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2841">_workspaceHidden</span></span> | <span data-ttu-id="b03d2-2842">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2842">boolean</span></span> | <span data-ttu-id="b03d2-2843">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2843">True</span></span> | <span data-ttu-id="b03d2-2844">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="b03d2-2844">The workspace is hidden from designer</span></span>


### <a name="method-appid"></a><span data-ttu-id="b03d2-2845">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2845">Method AppId</span></span> 
<span data-ttu-id="b03d2-2846">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2846">Gets or sets the AppId of the workspace</span></span>

     public str AppId ([str _appId]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2847">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2847">Parameters</span></span>

| <span data-ttu-id="b03d2-2848">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2848">Parameter name</span></span> |  <span data-ttu-id="b03d2-2849">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2849">Parameter type</span></span> | <span data-ttu-id="b03d2-2850">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2850">Optional</span></span> | <span data-ttu-id="b03d2-2851">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2851">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2852">_appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2852">_appId</span></span> | <span data-ttu-id="b03d2-2853">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2853">str</span></span> | <span data-ttu-id="b03d2-2854">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2854">True</span></span> | <span data-ttu-id="b03d2-2855">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2855">The AppId of the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2856">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2856">Return Value</span></span> 
<span data-ttu-id="b03d2-2857">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2857">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="b03d2-2858">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2858">Method AppResourceName</span></span> 
<span data-ttu-id="b03d2-2859">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2859">Gets or sets the AOT Resource name which contains the workspace</span></span>

     public str AppResourceName ([str _appResourceName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2860">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2860">Parameters</span></span>

| <span data-ttu-id="b03d2-2861">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2861">Parameter name</span></span> |  <span data-ttu-id="b03d2-2862">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2862">Parameter type</span></span> | <span data-ttu-id="b03d2-2863">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2863">Optional</span></span> | <span data-ttu-id="b03d2-2864">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2864">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2865">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2865">_appResourceName</span></span> | <span data-ttu-id="b03d2-2866">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2866">str</span></span> | <span data-ttu-id="b03d2-2867">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2867">True</span></span> | <span data-ttu-id="b03d2-2868">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2868">The AOT Resource name which contains the workspace</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2869">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2869">Return Value</span></span> 
<span data-ttu-id="b03d2-2870">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2870">The AOT Resource name which contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="b03d2-2871">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2871">Method WorkspaceHidden</span></span> 
<span data-ttu-id="b03d2-2872">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2872">Gets or sets if the workspace is hidden from designer</span></span>

     public boolean WorkspaceHidden ([boolean _workspaceHidden]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2873">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2873">Parameters</span></span>

| <span data-ttu-id="b03d2-2874">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2874">Parameter name</span></span> |  <span data-ttu-id="b03d2-2875">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2875">Parameter type</span></span> | <span data-ttu-id="b03d2-2876">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2876">Optional</span></span> | <span data-ttu-id="b03d2-2877">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2877">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2878">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="b03d2-2878">_workspaceHidden</span></span> | <span data-ttu-id="b03d2-2879">ブール値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2879">boolean</span></span> | <span data-ttu-id="b03d2-2880">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2880">True</span></span> | <span data-ttu-id="b03d2-2881">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="b03d2-2881">The workspace hidden</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2882">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2882">Return Value</span></span> 
<span data-ttu-id="b03d2-2883">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="b03d2-2883">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="b03d2-2884">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2884">Class SysAppWorkspaceMetadata</span></span> 
<span data-ttu-id="b03d2-2885">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2885">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-2886">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-2886">Methods</span></span>

| <span data-ttu-id="b03d2-2887">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2887">Method name</span></span> | <span data-ttu-id="b03d2-2888">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-2888">Returns</span></span> | <span data-ttu-id="b03d2-2889">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2889">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-2890">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-2890">new</span></span> | <span data-ttu-id="b03d2-2891">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2891">void</span></span> |  |
| <span data-ttu-id="b03d2-2892">addConfig</span><span class="sxs-lookup"><span data-stu-id="b03d2-2892">addConfig</span></span> | <span data-ttu-id="b03d2-2893">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-2893">void</span></span> | <span data-ttu-id="b03d2-2894">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2894">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="b03d2-2895">getPage</span><span class="sxs-lookup"><span data-stu-id="b03d2-2895">getPage</span></span> | <span data-ttu-id="b03d2-2896">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2896">SysAppPageMetadata</span></span> | <span data-ttu-id="b03d2-2897">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2897">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="b03d2-2898">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2898">getPageEnumerator</span></span> | <span data-ttu-id="b03d2-2899">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2899">MapEnumerator</span></span> | <span data-ttu-id="b03d2-2900">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2900">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="b03d2-2901">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-2901">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="b03d2-2902">getAction</span><span class="sxs-lookup"><span data-stu-id="b03d2-2902">getAction</span></span> | <span data-ttu-id="b03d2-2903">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="b03d2-2903">SysAppActionMetadata</span></span> | <span data-ttu-id="b03d2-2904">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2904">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="b03d2-2905">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2905">getActionEnumerator</span></span> | <span data-ttu-id="b03d2-2906">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2906">MapEnumerator</span></span> | <span data-ttu-id="b03d2-2907">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2907">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="b03d2-2908">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-2908">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="b03d2-2909">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2909">getPageNameForRecordingId</span></span> | <span data-ttu-id="b03d2-2910">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2910">str</span></span> | <span data-ttu-id="b03d2-2911">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2911">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="b03d2-2912">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2912">getActionNameForRecordingId</span></span> | <span data-ttu-id="b03d2-2913">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2913">str</span></span> | <span data-ttu-id="b03d2-2914">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2914">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="b03d2-2915">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-2915">workspaceTitle</span></span> | <span data-ttu-id="b03d2-2916">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2916">str</span></span> | <span data-ttu-id="b03d2-2917">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2917">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="b03d2-2918">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-2918">workspaceDescription</span></span> | <span data-ttu-id="b03d2-2919">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2919">str</span></span> | <span data-ttu-id="b03d2-2920">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-2920">Gets and sets the workspace description</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-2921">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-2921">Method new</span></span> 


     public void new (str _appId, [SysAppWorkspaceAttribute _attribute]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2922">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2922">Parameters</span></span>

| <span data-ttu-id="b03d2-2923">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2923">Parameter name</span></span> |  <span data-ttu-id="b03d2-2924">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2924">Parameter type</span></span> | <span data-ttu-id="b03d2-2925">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2925">Optional</span></span> | <span data-ttu-id="b03d2-2926">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2926">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2927">_appId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2927">_appId</span></span> | <span data-ttu-id="b03d2-2928">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2928">str</span></span> | <span data-ttu-id="b03d2-2929">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2929">False</span></span> | 
| <span data-ttu-id="b03d2-2930">_attribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2930">_attribute</span></span> | <span data-ttu-id="b03d2-2931">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-2931">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="b03d2-2932">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-2932">True</span></span> | 


### <a name="method-addconfig"></a><span data-ttu-id="b03d2-2933">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="b03d2-2933">Method addConfig</span></span> 
<span data-ttu-id="b03d2-2934">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2934">Adds a custom config to the mobile workspace metadata</span></span>

     public void addConfig (str _configName, object _configValue) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2935">Parameters</span></span>

| <span data-ttu-id="b03d2-2936">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2936">Parameter name</span></span> |  <span data-ttu-id="b03d2-2937">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2937">Parameter type</span></span> | <span data-ttu-id="b03d2-2938">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2938">Optional</span></span> | <span data-ttu-id="b03d2-2939">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2939">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2940">_configName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2940">_configName</span></span> | <span data-ttu-id="b03d2-2941">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2941">str</span></span> | <span data-ttu-id="b03d2-2942">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2942">False</span></span> | <span data-ttu-id="b03d2-2943">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2943">A config name</span></span>
| <span data-ttu-id="b03d2-2944">_configValue</span><span class="sxs-lookup"><span data-stu-id="b03d2-2944">_configValue</span></span> | <span data-ttu-id="b03d2-2945">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2945">object</span></span> | <span data-ttu-id="b03d2-2946">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2946">False</span></span> | <span data-ttu-id="b03d2-2947">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b03d2-2947">An object of a X++ data contract class</span></span>


### <a name="method-getpage"></a><span data-ttu-id="b03d2-2948">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="b03d2-2948">Method getPage</span></span> 
<span data-ttu-id="b03d2-2949">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2949">Returns the page with the pageName provided</span></span>

     public SysAppPageMetadata getPage (str _pageName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2950">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2950">Parameters</span></span>

| <span data-ttu-id="b03d2-2951">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2951">Parameter name</span></span> |  <span data-ttu-id="b03d2-2952">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2952">Parameter type</span></span> | <span data-ttu-id="b03d2-2953">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2953">Optional</span></span> | <span data-ttu-id="b03d2-2954">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2954">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2955">_pageName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2955">_pageName</span></span> | <span data-ttu-id="b03d2-2956">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2956">str</span></span> | <span data-ttu-id="b03d2-2957">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2957">False</span></span> | <span data-ttu-id="b03d2-2958">ページ名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2958">A page name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2959">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2959">Return Value</span></span> 
<span data-ttu-id="b03d2-2960">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2960">Returns the pageMetadata if a page with the provided name exist; otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="b03d2-2961">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2961">Method getPageEnumerator</span></span> 
<span data-ttu-id="b03d2-2962">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2962">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="b03d2-2963">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-2963">Where key is page name and value is of type SysAppPageMetadata</span></span>

     public MapEnumerator getPageEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2964">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2964">Return Value</span></span> 
<span data-ttu-id="b03d2-2965">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2965">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="b03d2-2966">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="b03d2-2966">Method getAction</span></span> 
<span data-ttu-id="b03d2-2967">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2967">Returns the action with the actionName provided</span></span>

     public SysAppActionMetadata getAction (str _actionName) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2968">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2968">Parameters</span></span>

| <span data-ttu-id="b03d2-2969">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2969">Parameter name</span></span> |  <span data-ttu-id="b03d2-2970">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2970">Parameter type</span></span> | <span data-ttu-id="b03d2-2971">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2971">Optional</span></span> | <span data-ttu-id="b03d2-2972">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2972">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2973">_actionName</span><span class="sxs-lookup"><span data-stu-id="b03d2-2973">_actionName</span></span> | <span data-ttu-id="b03d2-2974">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2974">str</span></span> | <span data-ttu-id="b03d2-2975">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2975">False</span></span> | <span data-ttu-id="b03d2-2976">アクション名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2976">An action name</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2977">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2977">Return Value</span></span> 
<span data-ttu-id="b03d2-2978">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2978">Returns the ActionMetadata if an action with the provided name exist; otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="b03d2-2979">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="b03d2-2979">Method getActionEnumerator</span></span> 
<span data-ttu-id="b03d2-2980">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2980">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="b03d2-2981">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="b03d2-2981">Where key is action name and value is of type SysAppActionMetadata</span></span>

     public MapEnumerator getActionEnumerator () 


#### <a name="return-value"></a><span data-ttu-id="b03d2-2982">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2982">Return Value</span></span> 
<span data-ttu-id="b03d2-2983">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="b03d2-2983">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="b03d2-2984">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2984">Method getPageNameForRecordingId</span></span> 
<span data-ttu-id="b03d2-2985">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2985">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

     public str getPageNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2986">Parameters</span></span>

| <span data-ttu-id="b03d2-2987">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-2987">Parameter name</span></span> |  <span data-ttu-id="b03d2-2988">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-2988">Parameter type</span></span> | <span data-ttu-id="b03d2-2989">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-2989">Optional</span></span> | <span data-ttu-id="b03d2-2990">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-2990">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-2991">_recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2991">_recordingId</span></span> | <span data-ttu-id="b03d2-2992">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-2992">str</span></span> | <span data-ttu-id="b03d2-2993">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-2993">False</span></span> | <span data-ttu-id="b03d2-2994">recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2994">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-2995">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-2995">Return Value</span></span> 
<span data-ttu-id="b03d2-2996">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b03d2-2996">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="b03d2-2997">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-2997">Method getActionNameForRecordingId</span></span> 
<span data-ttu-id="b03d2-2998">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="b03d2-2998">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

     public str getActionNameForRecordingId (str _recordingId) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-2999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-2999">Parameters</span></span>

| <span data-ttu-id="b03d2-3000">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3000">Parameter name</span></span> |  <span data-ttu-id="b03d2-3001">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3001">Parameter type</span></span> | <span data-ttu-id="b03d2-3002">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-3002">Optional</span></span> | <span data-ttu-id="b03d2-3003">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3003">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-3004">_recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-3004">_recordingId</span></span> | <span data-ttu-id="b03d2-3005">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-3005">str</span></span> | <span data-ttu-id="b03d2-3006">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-3006">False</span></span> | <span data-ttu-id="b03d2-3007">recordingId</span><span class="sxs-lookup"><span data-stu-id="b03d2-3007">A recordingId</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-3008">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-3008">Return Value</span></span> 
<span data-ttu-id="b03d2-3009">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b03d2-3009">An action name if the supplied recordingId is used by a workspace action;otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="b03d2-3010">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-3010">Method workspaceTitle</span></span> 
<span data-ttu-id="b03d2-3011">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-3011">Gets and sets the workspace title</span></span>

     public str workspaceTitle ([str _workspaceTitle]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-3012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-3012">Parameters</span></span>

| <span data-ttu-id="b03d2-3013">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3013">Parameter name</span></span> |  <span data-ttu-id="b03d2-3014">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3014">Parameter type</span></span> | <span data-ttu-id="b03d2-3015">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-3015">Optional</span></span> | <span data-ttu-id="b03d2-3016">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3016">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-3017">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="b03d2-3017">_workspaceTitle</span></span> | <span data-ttu-id="b03d2-3018">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-3018">str</span></span> | <span data-ttu-id="b03d2-3019">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-3019">True</span></span> | <span data-ttu-id="b03d2-3020">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-3020">The workspace title</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-3021">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-3021">Return Value</span></span> 
<span data-ttu-id="b03d2-3022">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="b03d2-3022">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="b03d2-3023">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-3023">Method workspaceDescription</span></span> 
<span data-ttu-id="b03d2-3024">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-3024">Gets and sets the workspace description</span></span>

     public str workspaceDescription ([str _workspaceDescription]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-3025">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-3025">Parameters</span></span>

| <span data-ttu-id="b03d2-3026">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3026">Parameter name</span></span> |  <span data-ttu-id="b03d2-3027">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3027">Parameter type</span></span> | <span data-ttu-id="b03d2-3028">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-3028">Optional</span></span> | <span data-ttu-id="b03d2-3029">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3029">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-3030">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="b03d2-3030">_workspaceDescription</span></span> | <span data-ttu-id="b03d2-3031">str</span><span class="sxs-lookup"><span data-stu-id="b03d2-3031">str</span></span> | <span data-ttu-id="b03d2-3032">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-3032">True</span></span> | <span data-ttu-id="b03d2-3033">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3033">The workspace description</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-3034">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-3034">Return Value</span></span> 
<span data-ttu-id="b03d2-3035">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3035">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="b03d2-3036">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="b03d2-3036">Class SysAppWorkspaceSecurityAttribute</span></span> 
<span data-ttu-id="b03d2-3037">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="b03d2-3037">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="b03d2-3038">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03d2-3038">Methods</span></span>

| <span data-ttu-id="b03d2-3039">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3039">Method name</span></span> | <span data-ttu-id="b03d2-3040">返品</span><span class="sxs-lookup"><span data-stu-id="b03d2-3040">Returns</span></span> | <span data-ttu-id="b03d2-3041">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3041">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="b03d2-3042">新規</span><span class="sxs-lookup"><span data-stu-id="b03d2-3042">new</span></span> | <span data-ttu-id="b03d2-3043">無効</span><span class="sxs-lookup"><span data-stu-id="b03d2-3043">void</span></span> | <span data-ttu-id="b03d2-3044">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="b03d2-3044">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="b03d2-3045">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-3045">WorkspaceMenuItemName</span></span> | <span data-ttu-id="b03d2-3046">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-3046">MenuItemName</span></span> | <span data-ttu-id="b03d2-3047">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-3047">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="b03d2-3048">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-3048">WorkspaceMenuItemType</span></span> | <span data-ttu-id="b03d2-3049">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-3049">MenuItemType</span></span> | <span data-ttu-id="b03d2-3050">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-3050">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |


### <a name="method-new"></a><span data-ttu-id="b03d2-3051">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b03d2-3051">Method new</span></span> 
<span data-ttu-id="b03d2-3052">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="b03d2-3052">Creates a new instance of attribute</span></span>

     public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-3053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-3053">Parameters</span></span>

| <span data-ttu-id="b03d2-3054">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3054">Parameter name</span></span> |  <span data-ttu-id="b03d2-3055">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3055">Parameter type</span></span> | <span data-ttu-id="b03d2-3056">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-3056">Optional</span></span> | <span data-ttu-id="b03d2-3057">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3057">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-3058">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-3058">_workspaceMenuItemName</span></span> | <span data-ttu-id="b03d2-3059">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-3059">MenuItemName</span></span> | <span data-ttu-id="b03d2-3060">False</span><span class="sxs-lookup"><span data-stu-id="b03d2-3060">False</span></span> | <span data-ttu-id="b03d2-3061">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3061">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="b03d2-3062">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-3062">_workspaceMenuItemType</span></span> | <span data-ttu-id="b03d2-3063">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-3063">MenuItemType</span></span> | <span data-ttu-id="b03d2-3064">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-3064">True</span></span> | <span data-ttu-id="b03d2-3065">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3065">The menu item type</span></span>


### <a name="method-workspacemenuitemname"></a><span data-ttu-id="b03d2-3066">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-3066">Method WorkspaceMenuItemName</span></span> 
<span data-ttu-id="b03d2-3067">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-3067">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

     public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-3068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-3068">Parameters</span></span>

| <span data-ttu-id="b03d2-3069">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3069">Parameter name</span></span> |  <span data-ttu-id="b03d2-3070">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3070">Parameter type</span></span> | <span data-ttu-id="b03d2-3071">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-3071">Optional</span></span> | <span data-ttu-id="b03d2-3072">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3072">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-3073">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-3073">_workspaceMenuItemName</span></span> | <span data-ttu-id="b03d2-3074">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="b03d2-3074">MenuItemName</span></span> | <span data-ttu-id="b03d2-3075">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-3075">True</span></span> | <span data-ttu-id="b03d2-3076">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="b03d2-3076">The workspace menu item for the workspace security attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-3077">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-3077">Return Value</span></span> 
<span data-ttu-id="b03d2-3078">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="b03d2-3078">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="b03d2-3079">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-3079">Method WorkspaceMenuItemType</span></span> 
<span data-ttu-id="b03d2-3080">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="b03d2-3080">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

     public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType]) 


#### <a name="parameters"></a><span data-ttu-id="b03d2-3081">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b03d2-3081">Parameters</span></span>

| <span data-ttu-id="b03d2-3082">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b03d2-3082">Parameter name</span></span> |  <span data-ttu-id="b03d2-3083">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3083">Parameter type</span></span> | <span data-ttu-id="b03d2-3084">オプション</span><span class="sxs-lookup"><span data-stu-id="b03d2-3084">Optional</span></span> | <span data-ttu-id="b03d2-3085">説明</span><span class="sxs-lookup"><span data-stu-id="b03d2-3085">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="b03d2-3086">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-3086">_workspaceMenuItemType</span></span> | <span data-ttu-id="b03d2-3087">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="b03d2-3087">MenuItemType</span></span> | <span data-ttu-id="b03d2-3088">はい</span><span class="sxs-lookup"><span data-stu-id="b03d2-3088">True</span></span> | <span data-ttu-id="b03d2-3089">workspacesecurity 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3089">The workspace menu item type for the workspacesecurity attribute</span></span>


#### <a name="return-value"></a><span data-ttu-id="b03d2-3090">戻り値</span><span class="sxs-lookup"><span data-stu-id="b03d2-3090">Return Value</span></span> 
<span data-ttu-id="b03d2-3091">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="b03d2-3091">The workspace menu item type for the workspace security attribute</span></span>

