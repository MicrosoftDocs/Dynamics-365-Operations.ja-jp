---
title: サーバー側の開発 (ワークスペース X++ API)
description: このトピックでは、携帯電話アプリをサポートするプラットフォームについて説明します。このプラットフォームは、充実したオフラインおよびモバイルの相互関係、および使いやすいデザイナー エクスペリエンスを提供します。
author: robinarh
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 255544
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 8ff7f2aeb2e3923e7f553166360b8e618e818422
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127631"
---
# <a name="server-side-development-workspace-x-apis"></a><span data-ttu-id="a77ca-103">サーバー側の開発 (ワークスペース X++ API)</span><span class="sxs-lookup"><span data-stu-id="a77ca-103">Server-side development (workspace X++ APIs)</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="class-sysappactionattribute"></a><span data-ttu-id="a77ca-104">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-104">Class SysAppActionAttribute</span></span>

<span data-ttu-id="a77ca-105">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-105">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-106">Methods</span></span>

| <span data-ttu-id="a77ca-107">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-107">Method name</span></span> | <span data-ttu-id="a77ca-108">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-108">Returns</span></span> | <span data-ttu-id="a77ca-109">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-109">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-110">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-110">new</span></span> | <span data-ttu-id="a77ca-111">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-111">void</span></span> | <span data-ttu-id="a77ca-112">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-112">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="a77ca-113">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="a77ca-113">pageMethodName</span></span> | <span data-ttu-id="a77ca-114">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-114">str</span></span> | <span data-ttu-id="a77ca-115">このタスクが存在するページを形成する Page メソッド名を取得します</span><span class="sxs-lookup"><span data-stu-id="a77ca-115">Gets the get method name that forms the page under which this task resides</span></span> |
| <span data-ttu-id="a77ca-116">actionTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-116">actionTitle</span></span> | <span data-ttu-id="a77ca-117">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-117">str</span></span> | <span data-ttu-id="a77ca-118">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-118">Gets the Action Title</span></span> |
| <span data-ttu-id="a77ca-119">actionDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-119">actionDescription</span></span> | <span data-ttu-id="a77ca-120">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-120">str</span></span> | <span data-ttu-id="a77ca-121">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-121">Gets the Action Description</span></span> |
| <span data-ttu-id="a77ca-122">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="a77ca-122">crudOperationType</span></span> | <span data-ttu-id="a77ca-123">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="a77ca-123">SysAppCRUDOperation</span></span> | <span data-ttu-id="a77ca-124">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-124">Gets the Crud Operation Type like Create, Update, Delete</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-125">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-125">Method new</span></span>

<span data-ttu-id="a77ca-126">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-126">Creates a new instance of SysAppActionAttribute class</span></span>

```xpp
public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-127">Parameters</span></span>

| <span data-ttu-id="a77ca-128">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-128">Parameter name</span></span> |  <span data-ttu-id="a77ca-129">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-129">Parameter type</span></span> | <span data-ttu-id="a77ca-130">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-130">Optional</span></span> | <span data-ttu-id="a77ca-131">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-131">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-132">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-132">_actionTitle</span></span> | <span data-ttu-id="a77ca-133">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-133">str</span></span> | <span data-ttu-id="a77ca-134">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-134">True</span></span> | <span data-ttu-id="a77ca-135">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-135">Action title</span></span>
| <span data-ttu-id="a77ca-136">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-136">_actionDescription</span></span> | <span data-ttu-id="a77ca-137">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-137">str</span></span> | <span data-ttu-id="a77ca-138">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-138">True</span></span> | <span data-ttu-id="a77ca-139">アクション説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-139">Action description</span></span>
| <span data-ttu-id="a77ca-140">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="a77ca-140">_crudOperationType</span></span> | <span data-ttu-id="a77ca-141">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="a77ca-141">SysAppCRUDOperation</span></span> | <span data-ttu-id="a77ca-142">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-142">True</span></span> | <span data-ttu-id="a77ca-143">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="a77ca-143">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="a77ca-144">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="a77ca-144">_pageMethodName</span></span> | <span data-ttu-id="a77ca-145">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-145">str</span></span> | <span data-ttu-id="a77ca-146">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-146">True</span></span> | <span data-ttu-id="a77ca-147">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-147">Name of the method constructing parent page</span></span>

### <a name="method-pagemethodname"></a><span data-ttu-id="a77ca-148">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="a77ca-148">Method pageMethodName</span></span>

<span data-ttu-id="a77ca-149">このタスクが存在するページを形成する Page メソッド名を取得します</span><span class="sxs-lookup"><span data-stu-id="a77ca-149">Gets the get method name that forms the page under which this task resides</span></span>

```xpp
public str pageMethodName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-150">Return Value</span></span>

<span data-ttu-id="a77ca-151">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-151">The page method name that forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="a77ca-152">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-152">Method actionTitle</span></span>

<span data-ttu-id="a77ca-153">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-153">Gets the Action Title</span></span>

```xpp
public str actionTitle ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-154">Return Value</span></span>

<span data-ttu-id="a77ca-155">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-155">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="a77ca-156">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-156">Method actionDescription</span></span>

<span data-ttu-id="a77ca-157">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-157">Gets the Action Description</span></span>

```xpp
public str actionDescription ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-158">Return Value</span></span>

<span data-ttu-id="a77ca-159">ページの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-159">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="a77ca-160">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="a77ca-160">Method crudOperationType</span></span>

<span data-ttu-id="a77ca-161">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-161">Gets the Crud Operation Type like Create, Update, Delete</span></span>

```xpp
public SysAppCRUDOperation crudOperationType ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-162">Return Value</span></span>

<span data-ttu-id="a77ca-163">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-163">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="a77ca-164">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-164">Class SysAppActionMetadata</span></span>

<span data-ttu-id="a77ca-165">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-165">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-166">方法</span><span class="sxs-lookup"><span data-stu-id="a77ca-166">Methods</span></span>

| <span data-ttu-id="a77ca-167">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-167">Method name</span></span> | <span data-ttu-id="a77ca-168">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-168">Returns</span></span> | <span data-ttu-id="a77ca-169">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-169">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-170">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-170">new</span></span> | <span data-ttu-id="a77ca-171">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-171">void</span></span> |  |
| <span data-ttu-id="a77ca-172">getActionName</span><span class="sxs-lookup"><span data-stu-id="a77ca-172">getActionName</span></span> | <span data-ttu-id="a77ca-173">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-173">str</span></span> | <span data-ttu-id="a77ca-174">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-174">Returns the action name</span></span> |
| <span data-ttu-id="a77ca-175">actionTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-175">actionTitle</span></span> | <span data-ttu-id="a77ca-176">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-176">str</span></span> | <span data-ttu-id="a77ca-177">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-177">Gets or sets the action title</span></span> |
| <span data-ttu-id="a77ca-178">actionDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-178">actionDescription</span></span> | <span data-ttu-id="a77ca-179">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-179">str</span></span> | <span data-ttu-id="a77ca-180">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-180">Gets or sets the action description</span></span> |
| <span data-ttu-id="a77ca-181">actionHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-181">actionHidden</span></span> | <span data-ttu-id="a77ca-182">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-182">boolean</span></span> | <span data-ttu-id="a77ca-183">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-183">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="a77ca-184">actionOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-184">actionOrder</span></span> | <span data-ttu-id="a77ca-185">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-185">int</span></span> | <span data-ttu-id="a77ca-186">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-186">Gets or sets the action order</span></span> |
| <span data-ttu-id="a77ca-187">getControl</span><span class="sxs-lookup"><span data-stu-id="a77ca-187">getControl</span></span> | <span data-ttu-id="a77ca-188">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-188">SysAppControlMetadata</span></span> | <span data-ttu-id="a77ca-189">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-189">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="a77ca-190">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-190">getControlEnumerator</span></span> | <span data-ttu-id="a77ca-191">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-191">MapEnumerator</span></span> | <span data-ttu-id="a77ca-192">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-192">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="a77ca-193">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-193">Where Key is control name and value is of type SysAppControlMetadata</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-194">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-194">Method new</span></span>

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-195">Parameters</span></span>

| <span data-ttu-id="a77ca-196">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-196">Parameter name</span></span> |  <span data-ttu-id="a77ca-197">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-197">Parameter type</span></span> | <span data-ttu-id="a77ca-198">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-198">Optional</span></span> | <span data-ttu-id="a77ca-199">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-199">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-200">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-200">_taskmetadata</span></span> | <span data-ttu-id="a77ca-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="a77ca-202">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-202">False</span></span> |

### <a name="method-getactionname"></a><span data-ttu-id="a77ca-203">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="a77ca-203">Method getActionName</span></span>

<span data-ttu-id="a77ca-204">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-204">Returns the action name</span></span>

```xpp
public str getActionName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-205">Return Value</span></span>

<span data-ttu-id="a77ca-206">アクション名</span><span class="sxs-lookup"><span data-stu-id="a77ca-206">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="a77ca-207">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-207">Method actionTitle</span></span>

<span data-ttu-id="a77ca-208">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-208">Gets or sets the action title</span></span>

```xpp
public str actionTitle ([str _actionTitle])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-209">Parameters</span></span>

| <span data-ttu-id="a77ca-210">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-210">Parameter name</span></span> |  <span data-ttu-id="a77ca-211">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-211">Parameter type</span></span> | <span data-ttu-id="a77ca-212">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-212">Optional</span></span> | <span data-ttu-id="a77ca-213">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-213">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-214">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-214">_actionTitle</span></span> | <span data-ttu-id="a77ca-215">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-215">str</span></span> | <span data-ttu-id="a77ca-216">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-216">True</span></span> | <span data-ttu-id="a77ca-217">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-217">The action title</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-218">Return Value</span></span>

<span data-ttu-id="a77ca-219">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-219">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="a77ca-220">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-220">Method actionDescription</span></span>

<span data-ttu-id="a77ca-221">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-221">Gets or sets the action description</span></span>

```xpp
public str actionDescription ([str _actionDescription])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-222">Parameters</span></span>

| <span data-ttu-id="a77ca-223">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-223">Parameter name</span></span> |  <span data-ttu-id="a77ca-224">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-224">Parameter type</span></span> | <span data-ttu-id="a77ca-225">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-225">Optional</span></span> | <span data-ttu-id="a77ca-226">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-226">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-227">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-227">_actionDescription</span></span> | <span data-ttu-id="a77ca-228">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-228">str</span></span> | <span data-ttu-id="a77ca-229">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-229">True</span></span> | <span data-ttu-id="a77ca-230">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-230">The action description</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-231">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-231">Return Value</span></span>

<span data-ttu-id="a77ca-232">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-232">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="a77ca-233">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-233">Method actionHidden</span></span>

<span data-ttu-id="a77ca-234">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-234">Gets or sets whether action is hidden</span></span>

```xpp
public boolean actionHidden ([boolean _actionHidden])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-235">Parameters</span></span>

| <span data-ttu-id="a77ca-236">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-236">Parameter name</span></span> |  <span data-ttu-id="a77ca-237">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-237">Parameter type</span></span> | <span data-ttu-id="a77ca-238">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-238">Optional</span></span> | <span data-ttu-id="a77ca-239">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-239">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-240">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-240">_actionHidden</span></span> | <span data-ttu-id="a77ca-241">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-241">boolean</span></span> | <span data-ttu-id="a77ca-242">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-242">True</span></span> | <span data-ttu-id="a77ca-243">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="a77ca-243">Action hidden value</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-244">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-244">Return Value</span></span>

<span data-ttu-id="a77ca-245">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a77ca-245">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="a77ca-246">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-246">Method actionOrder</span></span>

<span data-ttu-id="a77ca-247">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-247">Gets or sets the action order</span></span>

```xpp
public int actionOrder ([int _actionOrder])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-248">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-248">Parameters</span></span>

| <span data-ttu-id="a77ca-249">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-249">Parameter name</span></span> |  <span data-ttu-id="a77ca-250">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-250">Parameter type</span></span> | <span data-ttu-id="a77ca-251">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-251">Optional</span></span> | <span data-ttu-id="a77ca-252">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-252">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-253">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-253">_actionOrder</span></span> | <span data-ttu-id="a77ca-254">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-254">int</span></span> | <span data-ttu-id="a77ca-255">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-255">True</span></span> | <span data-ttu-id="a77ca-256">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="a77ca-256">The action order</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-257">Return Value</span></span>

<span data-ttu-id="a77ca-258">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="a77ca-258">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="a77ca-259">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="a77ca-259">Method getControl</span></span>

<span data-ttu-id="a77ca-260">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-260">Returns the control on the current action having the provided control name</span></span>

```xpp
public SysAppControlMetadata getControl (str _controlName)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-261">Parameters</span></span>

| <span data-ttu-id="a77ca-262">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-262">Parameter name</span></span> |  <span data-ttu-id="a77ca-263">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-263">Parameter type</span></span> | <span data-ttu-id="a77ca-264">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-264">Optional</span></span> | <span data-ttu-id="a77ca-265">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-265">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-266">_controlName</span><span class="sxs-lookup"><span data-stu-id="a77ca-266">_controlName</span></span> | <span data-ttu-id="a77ca-267">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-267">str</span></span> | <span data-ttu-id="a77ca-268">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-268">False</span></span> | <span data-ttu-id="a77ca-269">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="a77ca-269">The control name that will be used to search for control</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-270">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-270">Return Value</span></span>

<span data-ttu-id="a77ca-271">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="a77ca-271">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="a77ca-272">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-272">Method getControlEnumerator</span></span>

<span data-ttu-id="a77ca-273">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-273">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="a77ca-274">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-274">Where Key is control name and value is of type SysAppControlMetadata</span></span>

```xpp
public MapEnumerator getControlEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-275">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-275">Return Value</span></span>

<span data-ttu-id="a77ca-276">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="a77ca-276">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="a77ca-277">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="a77ca-277">Class SysAppAttributeHelper</span></span>

<span data-ttu-id="a77ca-278">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="a77ca-278">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-279">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-279">Methods</span></span>

| <span data-ttu-id="a77ca-280">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-280">Method name</span></span> | <span data-ttu-id="a77ca-281">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-281">Returns</span></span> | <span data-ttu-id="a77ca-282">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-282">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-283">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="a77ca-283">getAttributeFromClass</span></span> | <span data-ttu-id="a77ca-284">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-284">SysAttribute</span></span> | <span data-ttu-id="a77ca-285">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="a77ca-285">gets attribute from class</span></span> |

### <a name="method-getattributefromclass"></a><span data-ttu-id="a77ca-286">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="a77ca-286">Method getAttributeFromClass</span></span>

<span data-ttu-id="a77ca-287">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="a77ca-287">gets attribute from class</span></span>

```xpp
public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-288">Parameters</span></span>

| <span data-ttu-id="a77ca-289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-289">Parameter name</span></span> |  <span data-ttu-id="a77ca-290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-290">Parameter type</span></span> | <span data-ttu-id="a77ca-291">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-291">Optional</span></span> | <span data-ttu-id="a77ca-292">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-292">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-293">_sysClass</span><span class="sxs-lookup"><span data-stu-id="a77ca-293">_sysClass</span></span> | <span data-ttu-id="a77ca-294">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="a77ca-294">SysDictClass</span></span> | <span data-ttu-id="a77ca-295">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-295">False</span></span> | <span data-ttu-id="a77ca-296">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="a77ca-296">class for which attributes is required</span></span>
| <span data-ttu-id="a77ca-297">_attributeType</span><span class="sxs-lookup"><span data-stu-id="a77ca-297">_attributeType</span></span> | <span data-ttu-id="a77ca-298">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="a77ca-298">SysAppAttributeType</span></span> | <span data-ttu-id="a77ca-299">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-299">False</span></span> | <span data-ttu-id="a77ca-300">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="a77ca-300">Type of attribute like SysAppEntityAttribute</span></span>

## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="a77ca-301">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-301">Class SysAppCollectionAttribute</span></span>

<span data-ttu-id="a77ca-302">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-302">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-303">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-303">Methods</span></span>

| <span data-ttu-id="a77ca-304">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-304">Method name</span></span> | <span data-ttu-id="a77ca-305">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-305">Returns</span></span> | <span data-ttu-id="a77ca-306">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-306">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-307">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-307">new</span></span> | <span data-ttu-id="a77ca-308">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-308">void</span></span> | <span data-ttu-id="a77ca-309">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a77ca-309">Constructor</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-310">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-310">Method new</span></span>

<span data-ttu-id="a77ca-311">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a77ca-311">Constructor</span></span>

```xpp
public void new (str _itemContractName, [str _label], [str _relationshipName])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-312">Parameters</span></span>

| <span data-ttu-id="a77ca-313">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-313">Parameter name</span></span> |  <span data-ttu-id="a77ca-314">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-314">Parameter type</span></span> | <span data-ttu-id="a77ca-315">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-315">Optional</span></span> | <span data-ttu-id="a77ca-316">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-316">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-317">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="a77ca-317">_itemContractName</span></span> | <span data-ttu-id="a77ca-318">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-318">str</span></span> | <span data-ttu-id="a77ca-319">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-319">False</span></span> | <span data-ttu-id="a77ca-320">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="a77ca-320">Data contract name of list item</span></span>
| <span data-ttu-id="a77ca-321">_label</span><span class="sxs-lookup"><span data-stu-id="a77ca-321">_label</span></span> | <span data-ttu-id="a77ca-322">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-322">str</span></span> | <span data-ttu-id="a77ca-323">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-323">True</span></span> | <span data-ttu-id="a77ca-324">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="a77ca-324">List control label</span></span>
| <span data-ttu-id="a77ca-325">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="a77ca-325">_relationshipName</span></span> | <span data-ttu-id="a77ca-326">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-326">str</span></span> | <span data-ttu-id="a77ca-327">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-327">True</span></span> | <span data-ttu-id="a77ca-328">関係名。</span><span class="sxs-lookup"><span data-stu-id="a77ca-328">Relationship name.</span></span> <span data-ttu-id="a77ca-329">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-329">By default the entity name of the list item is used as relationship name</span></span>

## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="a77ca-330">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-330">Class SysAppControlMetadata</span></span>

<span data-ttu-id="a77ca-331">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-331">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="a77ca-332">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="a77ca-332">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-333">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-333">Methods</span></span>

| <span data-ttu-id="a77ca-334">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-334">Method name</span></span> | <span data-ttu-id="a77ca-335">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-335">Returns</span></span> | <span data-ttu-id="a77ca-336">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-336">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-337">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-337">new</span></span> | <span data-ttu-id="a77ca-338">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-338">void</span></span> | <span data-ttu-id="a77ca-339">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-339">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="a77ca-340">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="a77ca-340">getBaseLanguageId</span></span> | <span data-ttu-id="a77ca-341">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-341">str</span></span> | <span data-ttu-id="a77ca-342">アプリケーションの基本言語 ID を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-342">Returns the base language ID for the app</span></span> |
| <span data-ttu-id="a77ca-343">getControlName</span><span class="sxs-lookup"><span data-stu-id="a77ca-343">getControlName</span></span> | <span data-ttu-id="a77ca-344">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-344">str</span></span> | <span data-ttu-id="a77ca-345">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-345">Returns the control name</span></span> |
| <span data-ttu-id="a77ca-346">controlLabel</span><span class="sxs-lookup"><span data-stu-id="a77ca-346">controlLabel</span></span> | <span data-ttu-id="a77ca-347">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-347">str</span></span> | <span data-ttu-id="a77ca-348">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-348">Gets and sets the control label</span></span> |
| <span data-ttu-id="a77ca-349">controlHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-349">controlHidden</span></span> | <span data-ttu-id="a77ca-350">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-350">boolean</span></span> | <span data-ttu-id="a77ca-351">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-351">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="a77ca-352">controlOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-352">controlOrder</span></span> | <span data-ttu-id="a77ca-353">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-353">int</span></span> | <span data-ttu-id="a77ca-354">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-354">Gets or sets the control order</span></span> |
| <span data-ttu-id="a77ca-355">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="a77ca-355">controlMandatory</span></span> | <span data-ttu-id="a77ca-356">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-356">boolean</span></span> | <span data-ttu-id="a77ca-357">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-357">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="a77ca-358">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="a77ca-358">controlAllowNegative</span></span> | <span data-ttu-id="a77ca-359">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-359">boolean</span></span> | <span data-ttu-id="a77ca-360">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="a77ca-360">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="a77ca-361">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="a77ca-361">controlMaxLength</span></span> | <span data-ttu-id="a77ca-362">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-362">int</span></span> | <span data-ttu-id="a77ca-363">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-363">Gets or sets the control max length</span></span> |
| <span data-ttu-id="a77ca-364">getProperty</span><span class="sxs-lookup"><span data-stu-id="a77ca-364">getProperty</span></span> | `anytype` | <span data-ttu-id="a77ca-365">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-365">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="a77ca-366">setProperty</span><span class="sxs-lookup"><span data-stu-id="a77ca-366">setProperty</span></span> | <span data-ttu-id="a77ca-367">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-367">void</span></span> | <span data-ttu-id="a77ca-368">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-368">Sets the control property referenced by the key</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-369">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-369">Method new</span></span>

<span data-ttu-id="a77ca-370">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-370">Creates a new instance of the control metadata</span></span>

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-371">Parameters</span></span>

| <span data-ttu-id="a77ca-372">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-372">Parameter name</span></span> |  <span data-ttu-id="a77ca-373">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-373">Parameter type</span></span> | <span data-ttu-id="a77ca-374">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-374">Optional</span></span> | <span data-ttu-id="a77ca-375">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-375">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-376">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-376">_controlMetadata</span></span> | <span data-ttu-id="a77ca-377">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-377">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="a77ca-378">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-378">False</span></span> | <span data-ttu-id="a77ca-379">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a77ca-379">The controlMetadata object</span></span>
| <span data-ttu-id="a77ca-380">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="a77ca-380">_baseLanguageId</span></span> | <span data-ttu-id="a77ca-381">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-381">str</span></span> | <span data-ttu-id="a77ca-382">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-382">True</span></span> | <span data-ttu-id="a77ca-383">基本言語</span><span class="sxs-lookup"><span data-stu-id="a77ca-383">The base language</span></span>

### <a name="method-getbaselanguageid"></a><span data-ttu-id="a77ca-384">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="a77ca-384">Method getBaseLanguageId</span></span>

<span data-ttu-id="a77ca-385">アプリケーションの基本言語 ID を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-385">Returns the base language ID for the app</span></span>

```xpp
public str getBaseLanguageId ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-386">Return Value</span></span>

<span data-ttu-id="a77ca-387">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="a77ca-387">The base language ID</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="a77ca-388">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="a77ca-388">Method getControlName</span></span>

<span data-ttu-id="a77ca-389">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-389">Returns the control name</span></span>

```xpp
public str getControlName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-390">Return Value</span></span>

<span data-ttu-id="a77ca-391">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="a77ca-391">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="a77ca-392">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="a77ca-392">Method controlLabel</span></span>

<span data-ttu-id="a77ca-393">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-393">Gets and sets the control label</span></span>

```xpp
public str controlLabel ([str _controlLabel])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-394">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-394">Parameters</span></span>

| <span data-ttu-id="a77ca-395">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-395">Parameter name</span></span> |  <span data-ttu-id="a77ca-396">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-396">Parameter type</span></span> | <span data-ttu-id="a77ca-397">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-397">Optional</span></span> | <span data-ttu-id="a77ca-398">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-398">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-399">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="a77ca-399">_controlLabel</span></span> | <span data-ttu-id="a77ca-400">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-400">str</span></span> | <span data-ttu-id="a77ca-401">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-401">True</span></span> | <span data-ttu-id="a77ca-402">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="a77ca-402">The control label</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-403">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-403">Return Value</span></span>

<span data-ttu-id="a77ca-404">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="a77ca-404">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="a77ca-405">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-405">Method controlHidden</span></span>

<span data-ttu-id="a77ca-406">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-406">Gets and sets whether the control is hidden</span></span>

```xpp
public boolean controlHidden ([boolean _controlHidden])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-407">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-407">Parameters</span></span>

| <span data-ttu-id="a77ca-408">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-408">Parameter name</span></span> |  <span data-ttu-id="a77ca-409">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-409">Parameter type</span></span> | <span data-ttu-id="a77ca-410">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-410">Optional</span></span> | <span data-ttu-id="a77ca-411">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-411">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-412">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-412">_controlHidden</span></span> | <span data-ttu-id="a77ca-413">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-413">boolean</span></span> | <span data-ttu-id="a77ca-414">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-414">True</span></span> | <span data-ttu-id="a77ca-415">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="a77ca-415">Control hidden value</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-416">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-416">Return Value</span></span>

<span data-ttu-id="a77ca-417">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a77ca-417">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="a77ca-418">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-418">Method controlOrder</span></span>

<span data-ttu-id="a77ca-419">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-419">Gets or sets the control order</span></span>

```xpp
public int controlOrder ([int _controlOrder])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-420">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-420">Parameters</span></span>

| <span data-ttu-id="a77ca-421">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-421">Parameter name</span></span> |  <span data-ttu-id="a77ca-422">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-422">Parameter type</span></span> | <span data-ttu-id="a77ca-423">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-423">Optional</span></span> | <span data-ttu-id="a77ca-424">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-424">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-425">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-425">_controlOrder</span></span> | <span data-ttu-id="a77ca-426">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-426">int</span></span> | <span data-ttu-id="a77ca-427">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-427">True</span></span> | <span data-ttu-id="a77ca-428">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="a77ca-428">The control order</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-429">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-429">Return Value</span></span>

<span data-ttu-id="a77ca-430">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="a77ca-430">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="a77ca-431">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="a77ca-431">Method controlMandatory</span></span>

<span data-ttu-id="a77ca-432">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-432">Gets or sets the control mandatory</span></span>

```xpp
public boolean controlMandatory ([boolean _controlMandatory])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-433">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-433">Parameters</span></span>

| <span data-ttu-id="a77ca-434">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-434">Parameter name</span></span> |  <span data-ttu-id="a77ca-435">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-435">Parameter type</span></span> | <span data-ttu-id="a77ca-436">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-436">Optional</span></span> | <span data-ttu-id="a77ca-437">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-437">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-438">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="a77ca-438">_controlMandatory</span></span> | <span data-ttu-id="a77ca-439">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-439">boolean</span></span> | <span data-ttu-id="a77ca-440">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-440">True</span></span> | <span data-ttu-id="a77ca-441">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="a77ca-441">The control mandatory</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-442">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-442">Return Value</span></span>

<span data-ttu-id="a77ca-443">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="a77ca-443">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="a77ca-444">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="a77ca-444">Method controlAllowNegative</span></span>

<span data-ttu-id="a77ca-445">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="a77ca-445">Gets or sets the control allow negative</span></span>

```xpp
public boolean controlAllowNegative ([boolean _controlAllowNegative])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-446">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-446">Parameters</span></span>

| <span data-ttu-id="a77ca-447">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-447">Parameter name</span></span> |  <span data-ttu-id="a77ca-448">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-448">Parameter type</span></span> | <span data-ttu-id="a77ca-449">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-449">Optional</span></span> | <span data-ttu-id="a77ca-450">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-450">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-451">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="a77ca-451">_controlAllowNegative</span></span> | <span data-ttu-id="a77ca-452">ブール型</span><span class="sxs-lookup"><span data-stu-id="a77ca-452">boolean</span></span> | <span data-ttu-id="a77ca-453">True</span><span class="sxs-lookup"><span data-stu-id="a77ca-453">True</span></span> | <span data-ttu-id="a77ca-454">コントロールは負の値を許可します</span><span class="sxs-lookup"><span data-stu-id="a77ca-454">The control allows negative</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-455">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-455">Return Value</span></span>

<span data-ttu-id="a77ca-456">コントロールは負の値を許可します</span><span class="sxs-lookup"><span data-stu-id="a77ca-456">The control allows negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="a77ca-457">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="a77ca-457">Method controlMaxLength</span></span>

<span data-ttu-id="a77ca-458">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-458">Gets or sets the control max length</span></span>

```xpp
public int controlMaxLength ([int _controlMaxLength])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-459">Parameters</span></span>

| <span data-ttu-id="a77ca-460">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-460">Parameter name</span></span> |  <span data-ttu-id="a77ca-461">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-461">Parameter type</span></span> | <span data-ttu-id="a77ca-462">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-462">Optional</span></span> | <span data-ttu-id="a77ca-463">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-463">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-464">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="a77ca-464">_controlMaxLength</span></span> | <span data-ttu-id="a77ca-465">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-465">int</span></span> | <span data-ttu-id="a77ca-466">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-466">True</span></span> | <span data-ttu-id="a77ca-467">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="a77ca-467">The control max length</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-468">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-468">Return Value</span></span>

<span data-ttu-id="a77ca-469">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="a77ca-469">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="a77ca-470">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="a77ca-470">Method getProperty</span></span>

<span data-ttu-id="a77ca-471">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-471">Gets the control property referenced by the key</span></span>

```xpp
public anytype getProperty (str _key)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-472">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-472">Parameters</span></span>

| <span data-ttu-id="a77ca-473">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-473">Parameter name</span></span> |  <span data-ttu-id="a77ca-474">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-474">Parameter type</span></span> | <span data-ttu-id="a77ca-475">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-475">Optional</span></span> | <span data-ttu-id="a77ca-476">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-476">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-477">_key</span><span class="sxs-lookup"><span data-stu-id="a77ca-477">_key</span></span> | <span data-ttu-id="a77ca-478">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-478">str</span></span> | <span data-ttu-id="a77ca-479">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-479">False</span></span> | <span data-ttu-id="a77ca-480">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="a77ca-480">The name of the control property</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-481">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-481">Return Value</span></span>

<span data-ttu-id="a77ca-482">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="a77ca-482">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="a77ca-483">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="a77ca-483">Method setProperty</span></span>

<span data-ttu-id="a77ca-484">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-484">Sets the control property referenced by the key</span></span>

```xpp
public void setProperty (str _key, anytype _value)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-485">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-485">Parameters</span></span>

| <span data-ttu-id="a77ca-486">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-486">Parameter name</span></span> |  <span data-ttu-id="a77ca-487">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-487">Parameter type</span></span> | <span data-ttu-id="a77ca-488">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-488">Optional</span></span> | <span data-ttu-id="a77ca-489">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-489">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-490">_key</span><span class="sxs-lookup"><span data-stu-id="a77ca-490">_key</span></span> | <span data-ttu-id="a77ca-491">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-491">str</span></span> | <span data-ttu-id="a77ca-492">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-492">False</span></span> | <span data-ttu-id="a77ca-493">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="a77ca-493">The name of the control property</span></span>
| <span data-ttu-id="a77ca-494">_value</span><span class="sxs-lookup"><span data-stu-id="a77ca-494">_value</span></span> | <span data-ttu-id="a77ca-495">anytype</span><span class="sxs-lookup"><span data-stu-id="a77ca-495">anytype</span></span> | <span data-ttu-id="a77ca-496">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-496">False</span></span> | <span data-ttu-id="a77ca-497">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="a77ca-497">The value of the control property</span></span>

## <a name="class-sysappentityattribute"></a><span data-ttu-id="a77ca-498">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-498">Class SysAppEntityAttribute</span></span>

<span data-ttu-id="a77ca-499">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-499">SysAppEntityAttribute used for decorating data contract entities</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-500">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-500">Methods</span></span>

| <span data-ttu-id="a77ca-501">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-501">Method name</span></span> | <span data-ttu-id="a77ca-502">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-502">Returns</span></span> | <span data-ttu-id="a77ca-503">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-503">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-504">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-504">new</span></span> | <span data-ttu-id="a77ca-505">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-505">void</span></span> | <span data-ttu-id="a77ca-506">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a77ca-506">Constructor</span></span> |
| <span data-ttu-id="a77ca-507">名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-507">name</span></span> | <span data-ttu-id="a77ca-508">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-508">str</span></span> | <span data-ttu-id="a77ca-509">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-509">Gets the name of the entity</span></span> |
| <span data-ttu-id="a77ca-510">entityKey</span><span class="sxs-lookup"><span data-stu-id="a77ca-510">entityKey</span></span> | <span data-ttu-id="a77ca-511">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-511">str</span></span> | <span data-ttu-id="a77ca-512">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-512">Gets the entity key</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-513">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-513">Method new</span></span>

<span data-ttu-id="a77ca-514">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a77ca-514">Constructor</span></span>

```xpp
public void new (str _name, str _entityKey)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-515">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-515">Parameters</span></span>

| <span data-ttu-id="a77ca-516">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-516">Parameter name</span></span> |  <span data-ttu-id="a77ca-517">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-517">Parameter type</span></span> | <span data-ttu-id="a77ca-518">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-518">Optional</span></span> | <span data-ttu-id="a77ca-519">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-519">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-520">_name</span><span class="sxs-lookup"><span data-stu-id="a77ca-520">_name</span></span> | <span data-ttu-id="a77ca-521">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-521">str</span></span> | <span data-ttu-id="a77ca-522">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-522">False</span></span> | <span data-ttu-id="a77ca-523">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-523">Entity name</span></span>
| <span data-ttu-id="a77ca-524">_entityKey</span><span class="sxs-lookup"><span data-stu-id="a77ca-524">_entityKey</span></span> | <span data-ttu-id="a77ca-525">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-525">str</span></span> | <span data-ttu-id="a77ca-526">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-526">False</span></span> | <span data-ttu-id="a77ca-527">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-527">Name of the entity's key</span></span>

### <a name="method-name"></a><span data-ttu-id="a77ca-528">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-528">Method name</span></span>

<span data-ttu-id="a77ca-529">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-529">Gets the name of the entity</span></span>

```xpp
public str name ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-530">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-530">Return Value</span></span>

<span data-ttu-id="a77ca-531">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-531">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="a77ca-532">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="a77ca-532">Method entityKey</span></span>

<span data-ttu-id="a77ca-533">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-533">Gets the entity key</span></span>

```xpp
public str entityKey ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-534">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-534">Return Value</span></span>

<span data-ttu-id="a77ca-535">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="a77ca-535">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="a77ca-536">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-536">Class SysAppEntityContext</span></span>

<span data-ttu-id="a77ca-537">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-537">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-538">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-538">Methods</span></span>

| <span data-ttu-id="a77ca-539">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-539">Method name</span></span> | <span data-ttu-id="a77ca-540">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-540">Returns</span></span> | <span data-ttu-id="a77ca-541">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-541">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-542">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="a77ca-542">constructFromParams</span></span> | <span data-ttu-id="a77ca-543">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-543">SysAppEntityContext</span></span> | <span data-ttu-id="a77ca-544">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-544">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="a77ca-545">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="a77ca-545">constructFromBuffer</span></span> | <span data-ttu-id="a77ca-546">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-546">SysAppEntityContext</span></span> | <span data-ttu-id="a77ca-547">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="a77ca-547">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="a77ca-548">entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-548">entityName</span></span> | <span data-ttu-id="a77ca-549">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-549">str</span></span> | <span data-ttu-id="a77ca-550">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-550">Entity name on which filter applies</span></span> |
| <span data-ttu-id="a77ca-551">entityId</span><span class="sxs-lookup"><span data-stu-id="a77ca-551">entityId</span></span> | <span data-ttu-id="a77ca-552">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-552">str</span></span> | <span data-ttu-id="a77ca-553">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="a77ca-553">Field value on which filter applies</span></span> |

### <a name="method-constructfromparams"></a><span data-ttu-id="a77ca-554">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="a77ca-554">Method constructFromParams</span></span>

<span data-ttu-id="a77ca-555">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-555">Constructs SysAppEntityContext from entityName and entityId</span></span>

```xpp
public SysAppEntityContext constructFromParams (str _entityName, str _entityId)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-556">Parameters</span></span>

| <span data-ttu-id="a77ca-557">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-557">Parameter name</span></span> |  <span data-ttu-id="a77ca-558">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-558">Parameter type</span></span> | <span data-ttu-id="a77ca-559">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-559">Optional</span></span> | <span data-ttu-id="a77ca-560">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-560">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-561">_entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-561">_entityName</span></span> | <span data-ttu-id="a77ca-562">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-562">str</span></span> | <span data-ttu-id="a77ca-563">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-563">False</span></span> | <span data-ttu-id="a77ca-564">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-564">Entity name</span></span>
| <span data-ttu-id="a77ca-565">_entityId</span><span class="sxs-lookup"><span data-stu-id="a77ca-565">_entityId</span></span> | <span data-ttu-id="a77ca-566">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-566">str</span></span> | <span data-ttu-id="a77ca-567">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-567">False</span></span> | <span data-ttu-id="a77ca-568">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="a77ca-568">Entity value</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-569">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-569">Return Value</span></span>

<span data-ttu-id="a77ca-570">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="a77ca-570">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="a77ca-571">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="a77ca-571">Method constructFromBuffer</span></span>

<span data-ttu-id="a77ca-572">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="a77ca-572">Constructs SysAppEntityContext from table buffer</span></span>

```xpp
public SysAppEntityContext constructFromBuffer (Common _tableBuffer)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-573">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-573">Parameters</span></span>

| <span data-ttu-id="a77ca-574">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-574">Parameter name</span></span> |  <span data-ttu-id="a77ca-575">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-575">Parameter type</span></span> | <span data-ttu-id="a77ca-576">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-576">Optional</span></span> | <span data-ttu-id="a77ca-577">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-577">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-578">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="a77ca-578">_tableBuffer</span></span> | <span data-ttu-id="a77ca-579">共通</span><span class="sxs-lookup"><span data-stu-id="a77ca-579">Common</span></span> | <span data-ttu-id="a77ca-580">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-580">False</span></span> | <span data-ttu-id="a77ca-581">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="a77ca-581">table buffer forming the entity</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-582">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-582">Return Value</span></span>

<span data-ttu-id="a77ca-583">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="a77ca-583">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="a77ca-584">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-584">Method entityName</span></span>

<span data-ttu-id="a77ca-585">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-585">Entity name on which filter applies</span></span>

```xpp
public str entityName ([str _entityName])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-586">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-586">Parameters</span></span>

| <span data-ttu-id="a77ca-587">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-587">Parameter name</span></span> |  <span data-ttu-id="a77ca-588">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-588">Parameter type</span></span> | <span data-ttu-id="a77ca-589">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-589">Optional</span></span> | <span data-ttu-id="a77ca-590">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-590">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-591">_entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-591">_entityName</span></span> | <span data-ttu-id="a77ca-592">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-592">str</span></span> | <span data-ttu-id="a77ca-593">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-593">True</span></span> | <span data-ttu-id="a77ca-594">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-594">Entity name</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-595">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-595">Return Value</span></span>

<span data-ttu-id="a77ca-596">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-596">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="a77ca-597">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="a77ca-597">Method entityId</span></span>

<span data-ttu-id="a77ca-598">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="a77ca-598">Field value on which filter applies</span></span>

```xpp
public str entityId ([str _entityId])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-599">Parameters</span></span>

| <span data-ttu-id="a77ca-600">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-600">Parameter name</span></span> |  <span data-ttu-id="a77ca-601">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-601">Parameter type</span></span> | <span data-ttu-id="a77ca-602">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-602">Optional</span></span> | <span data-ttu-id="a77ca-603">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-603">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-604">_entityId</span><span class="sxs-lookup"><span data-stu-id="a77ca-604">_entityId</span></span> | <span data-ttu-id="a77ca-605">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-605">str</span></span> | <span data-ttu-id="a77ca-606">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-606">True</span></span> | <span data-ttu-id="a77ca-607">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="a77ca-607">Entity value</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-608">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-608">Return Value</span></span>

<span data-ttu-id="a77ca-609">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="a77ca-609">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="a77ca-610">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-610">Class SysAppFieldAttribute</span></span>

<span data-ttu-id="a77ca-611">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-611">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-612">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-612">Methods</span></span>

| <span data-ttu-id="a77ca-613">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-613">Method name</span></span> | <span data-ttu-id="a77ca-614">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-614">Returns</span></span> | <span data-ttu-id="a77ca-615">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-615">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-616">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-616">new</span></span> | <span data-ttu-id="a77ca-617">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-617">void</span></span> | <span data-ttu-id="a77ca-618">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-618">Creates a new instance of SysAppFieldAttribute class</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-619">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-619">Method new</span></span>

<span data-ttu-id="a77ca-620">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-620">Creates a new instance of SysAppFieldAttribute class</span></span>

```xpp
public void new (str _fieldName, str _label)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-621">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-621">Parameters</span></span>

| <span data-ttu-id="a77ca-622">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-622">Parameter name</span></span> |  <span data-ttu-id="a77ca-623">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-623">Parameter type</span></span> | <span data-ttu-id="a77ca-624">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-624">Optional</span></span> | <span data-ttu-id="a77ca-625">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-625">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-626">_fieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-626">_fieldName</span></span> | <span data-ttu-id="a77ca-627">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-627">str</span></span> | <span data-ttu-id="a77ca-628">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-628">False</span></span> | <span data-ttu-id="a77ca-629">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-629">Entity field name with which control is bound</span></span>
| <span data-ttu-id="a77ca-630">_label</span><span class="sxs-lookup"><span data-stu-id="a77ca-630">_label</span></span> | <span data-ttu-id="a77ca-631">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-631">str</span></span> | <span data-ttu-id="a77ca-632">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-632">False</span></span> | <span data-ttu-id="a77ca-633">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="a77ca-633">Control label</span></span>

## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="a77ca-634">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="a77ca-634">Class SysAppFieldMultiSelectHelper</span></span>

<span data-ttu-id="a77ca-635">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="a77ca-635">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-636">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-636">Methods</span></span>

| <span data-ttu-id="a77ca-637">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-637">Method name</span></span> | <span data-ttu-id="a77ca-638">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-638">Returns</span></span> | <span data-ttu-id="a77ca-639">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-639">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-640">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-640">new</span></span> | <span data-ttu-id="a77ca-641">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-641">void</span></span> | <span data-ttu-id="a77ca-642">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-642">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="a77ca-643">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="a77ca-643">getSelectedRecIds</span></span> | <span data-ttu-id="a77ca-644">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a77ca-644">container</span></span> | <span data-ttu-id="a77ca-645">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-645">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="a77ca-646">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="a77ca-646">getSelectedValues</span></span> | <span data-ttu-id="a77ca-647">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a77ca-647">container</span></span> | <span data-ttu-id="a77ca-648">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-648">Returns a container of selected values</span></span> |
| <span data-ttu-id="a77ca-649">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="a77ca-649">getSelectedRecords</span></span> | <span data-ttu-id="a77ca-650">共通</span><span class="sxs-lookup"><span data-stu-id="a77ca-650">Common</span></span> | <span data-ttu-id="a77ca-651">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-651">Returns a buffer that contains all the selected records..</span></span>  <span data-ttu-id="a77ca-652">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-652">The buffer is marked as temp..</span></span>  <span data-ttu-id="a77ca-653">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="a77ca-653">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="a77ca-654">setControlValue</span><span class="sxs-lookup"><span data-stu-id="a77ca-654">setControlValue</span></span> | <span data-ttu-id="a77ca-655">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-655">void</span></span> | <span data-ttu-id="a77ca-656">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="a77ca-656">A setter to set the multiselect control value</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-657">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-657">Method new</span></span>

<span data-ttu-id="a77ca-658">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-658">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

```xpp
public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-659">Parameters</span></span>

| <span data-ttu-id="a77ca-660">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-660">Parameter name</span></span> |  <span data-ttu-id="a77ca-661">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-661">Parameter type</span></span> | <span data-ttu-id="a77ca-662">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-662">Optional</span></span> | <span data-ttu-id="a77ca-663">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-663">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-664">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="a77ca-664">_multiSelectTableId</span></span> | <span data-ttu-id="a77ca-665">TableId</span><span class="sxs-lookup"><span data-stu-id="a77ca-665">TableId</span></span> | <span data-ttu-id="a77ca-666">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-666">False</span></span> | <span data-ttu-id="a77ca-667">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="a77ca-667">The backing tableId for the field</span></span>
| <span data-ttu-id="a77ca-668">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="a77ca-668">_valueFieldId</span></span> | <span data-ttu-id="a77ca-669">FieldId</span><span class="sxs-lookup"><span data-stu-id="a77ca-669">FieldId</span></span> | <span data-ttu-id="a77ca-670">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-670">False</span></span> | <span data-ttu-id="a77ca-671">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="a77ca-671">The fieldId for the field that will be shown in the multi select control</span></span>
| <span data-ttu-id="a77ca-672">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="a77ca-672">_multiSelectControl</span></span> | <span data-ttu-id="a77ca-673">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="a77ca-673">FormStringControl</span></span> | <span data-ttu-id="a77ca-674">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-674">False</span></span> | <span data-ttu-id="a77ca-675">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="a77ca-675">The string control that will be the multi select control</span></span>

### <a name="method-getselectedrecids"></a><span data-ttu-id="a77ca-676">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="a77ca-676">Method getSelectedRecIds</span></span>

<span data-ttu-id="a77ca-677">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-677">Returns a container of recIds of the records that were selected</span></span>

```xpp
public container getSelectedRecIds ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-678">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-678">Return Value</span></span>

<span data-ttu-id="a77ca-679">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="a77ca-679">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="a77ca-680">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="a77ca-680">Method getSelectedValues</span></span>

<span data-ttu-id="a77ca-681">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-681">Returns a container of selected values</span></span>

```xpp
public container getSelectedValues ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-682">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-682">Return Value</span></span>

<span data-ttu-id="a77ca-683">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="a77ca-683">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="a77ca-684">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="a77ca-684">Method getSelectedRecords</span></span>

<span data-ttu-id="a77ca-685">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-685">Returns a buffer that contains all the selected records..</span></span>  <span data-ttu-id="a77ca-686">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-686">The buffer is marked as temp..</span></span>  <span data-ttu-id="a77ca-687">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="a77ca-687">Later a while-Select can be used to iterate through all the records</span></span>

```xpp
public Common getSelectedRecords ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-688">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-688">Return Value</span></span>

<span data-ttu-id="a77ca-689">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="a77ca-689">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="a77ca-690">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="a77ca-690">Method setControlValue</span></span>

<span data-ttu-id="a77ca-691">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="a77ca-691">A setter to set the multi select control value</span></span>

```xpp
public void setControlValue (str _value)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-692">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-692">Parameters</span></span>

| <span data-ttu-id="a77ca-693">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-693">Parameter name</span></span> |  <span data-ttu-id="a77ca-694">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-694">Parameter type</span></span> | <span data-ttu-id="a77ca-695">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-695">Optional</span></span> | <span data-ttu-id="a77ca-696">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-696">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-697">_value</span><span class="sxs-lookup"><span data-stu-id="a77ca-697">_value</span></span> | <span data-ttu-id="a77ca-698">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-698">str</span></span> | <span data-ttu-id="a77ca-699">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-699">False</span></span> | <span data-ttu-id="a77ca-700">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-700">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>

## <a name="class-sysappfiltercontext"></a><span data-ttu-id="a77ca-701">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-701">Class SysAppFilterContext</span></span>

<span data-ttu-id="a77ca-702">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="a77ca-702">SysAppFilterContext class that holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-703">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-703">Methods</span></span>

| <span data-ttu-id="a77ca-704">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-704">Method name</span></span> | <span data-ttu-id="a77ca-705">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-705">Returns</span></span> | <span data-ttu-id="a77ca-706">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-706">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-707">entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-707">entityName</span></span> | <span data-ttu-id="a77ca-708">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-708">str</span></span> | <span data-ttu-id="a77ca-709">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-709">Entity name on which filter applies</span></span> |
| <span data-ttu-id="a77ca-710">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-710">filterFieldName</span></span> | <span data-ttu-id="a77ca-711">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-711">str</span></span> | <span data-ttu-id="a77ca-712">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-712">Field name on which filter applies</span></span> |
| <span data-ttu-id="a77ca-713">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="a77ca-713">filterFieldValueList</span></span> | <span data-ttu-id="a77ca-714">リスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-714">List</span></span> | <span data-ttu-id="a77ca-715">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-715">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="a77ca-716">演算子</span><span class="sxs-lookup"><span data-stu-id="a77ca-716">operator</span></span> | <span data-ttu-id="a77ca-717">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-717">str</span></span> | <span data-ttu-id="a77ca-718">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="a77ca-718">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="a77ca-719">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="a77ca-719">addFilterFieldValue</span></span> | <span data-ttu-id="a77ca-720">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-720">void</span></span> | <span data-ttu-id="a77ca-721">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="a77ca-721">Adds filter field value</span></span> |

### <a name="method-entityname"></a><span data-ttu-id="a77ca-722">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-722">Method entityName</span></span>

<span data-ttu-id="a77ca-723">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-723">Entity name on which filter applies</span></span>

```xpp
public str entityName ([str _entityName])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-724">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-724">Parameters</span></span>

| <span data-ttu-id="a77ca-725">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-725">Parameter name</span></span> |  <span data-ttu-id="a77ca-726">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-726">Parameter type</span></span> | <span data-ttu-id="a77ca-727">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-727">Optional</span></span> | <span data-ttu-id="a77ca-728">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-728">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-729">_entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-729">_entityName</span></span> | <span data-ttu-id="a77ca-730">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-730">str</span></span> | <span data-ttu-id="a77ca-731">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-731">True</span></span> | <span data-ttu-id="a77ca-732">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-732">Entity name on which filter applies</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-733">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-733">Return Value</span></span>

<span data-ttu-id="a77ca-734">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-734">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="a77ca-735">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-735">Method filterFieldName</span></span>

<span data-ttu-id="a77ca-736">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-736">Field name on which filter applies</span></span>

```xpp
public str filterFieldName ([str _filterFieldName])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-737">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-737">Parameters</span></span>

| <span data-ttu-id="a77ca-738">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-738">Parameter name</span></span> |  <span data-ttu-id="a77ca-739">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-739">Parameter type</span></span> | <span data-ttu-id="a77ca-740">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-740">Optional</span></span> | <span data-ttu-id="a77ca-741">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-741">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-742">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-742">_filterFieldName</span></span> | <span data-ttu-id="a77ca-743">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-743">str</span></span> | <span data-ttu-id="a77ca-744">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-744">True</span></span> | <span data-ttu-id="a77ca-745">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-745">Field name on which filter applies</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-746">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-746">Return Value</span></span>

<span data-ttu-id="a77ca-747">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-747">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="a77ca-748">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="a77ca-748">Method filterFieldValueList</span></span>

<span data-ttu-id="a77ca-749">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-749">Gets the list of filter field values based on which filter happens</span></span>

```xpp
public List filterFieldValueList ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-750">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-750">Return Value</span></span>

<span data-ttu-id="a77ca-751">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="a77ca-751">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="a77ca-752">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="a77ca-752">Method operator</span></span>

<span data-ttu-id="a77ca-753">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="a77ca-753">Operator based on which result will be fetched</span></span>

```xpp
public str operator ([str _operator])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-754">Parameters</span></span>

| <span data-ttu-id="a77ca-755">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-755">Parameter name</span></span> |  <span data-ttu-id="a77ca-756">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-756">Parameter type</span></span> | <span data-ttu-id="a77ca-757">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-757">Optional</span></span> | <span data-ttu-id="a77ca-758">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-758">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-759">_operator</span><span class="sxs-lookup"><span data-stu-id="a77ca-759">_operator</span></span> | <span data-ttu-id="a77ca-760">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-760">str</span></span> | <span data-ttu-id="a77ca-761">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-761">True</span></span> | <span data-ttu-id="a77ca-762">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="a77ca-762">Operator based on which result will be fetched</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-763">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-763">Return Value</span></span>

<span data-ttu-id="a77ca-764">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="a77ca-764">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="a77ca-765">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="a77ca-765">Method addFilterFieldValue</span></span>

<span data-ttu-id="a77ca-766">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="a77ca-766">Adds filter field value</span></span>

```xpp
public void addFilterFieldValue ( _filterFieldValueList)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-767">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-767">Parameters</span></span>

| <span data-ttu-id="a77ca-768">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-768">Parameter name</span></span> |  <span data-ttu-id="a77ca-769">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-769">Parameter type</span></span> | <span data-ttu-id="a77ca-770">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-770">Optional</span></span> | <span data-ttu-id="a77ca-771">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-771">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-772">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="a77ca-772">_filterFieldValueList</span></span> |  | <span data-ttu-id="a77ca-773">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-773">False</span></span> | <span data-ttu-id="a77ca-774">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="a77ca-774">Filter field values based on which filter happens</span></span>

## <a name="class-sysapplookupattribute"></a><span data-ttu-id="a77ca-775">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-775">Class SysAppLookUpAttribute</span></span>

<span data-ttu-id="a77ca-776">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-776">SysAppPageAttribute used for decorating pages that are also lookup pages</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-777">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-777">Methods</span></span>

| <span data-ttu-id="a77ca-778">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-778">Method name</span></span> | <span data-ttu-id="a77ca-779">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-779">Returns</span></span> | <span data-ttu-id="a77ca-780">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-780">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-781">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-781">new</span></span> | <span data-ttu-id="a77ca-782">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-782">void</span></span> | <span data-ttu-id="a77ca-783">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-783">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="a77ca-784">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-784">displayFieldName</span></span> | <span data-ttu-id="a77ca-785">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-785">str</span></span> | <span data-ttu-id="a77ca-786">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-786">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="a77ca-787">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-787">valueFieldName</span></span> | <span data-ttu-id="a77ca-788">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-788">str</span></span> | <span data-ttu-id="a77ca-789">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-789">Gets the value field name of lookup control</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-790">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-790">Method new</span></span>

<span data-ttu-id="a77ca-791">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-791">Creates a new instance of SysAppLookUpAttribute class</span></span>

```xpp
public void new (str _displayFieldName, str _valueFieldName)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-792">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-792">Parameters</span></span>

| <span data-ttu-id="a77ca-793">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-793">Parameter name</span></span> |  <span data-ttu-id="a77ca-794">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-794">Parameter type</span></span> | <span data-ttu-id="a77ca-795">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-795">Optional</span></span> | <span data-ttu-id="a77ca-796">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-796">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-797">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-797">_displayFieldName</span></span> | <span data-ttu-id="a77ca-798">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-798">str</span></span> | <span data-ttu-id="a77ca-799">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-799">False</span></span> | <span data-ttu-id="a77ca-800">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="a77ca-800">Lookup display field.</span></span> <span data-ttu-id="a77ca-801">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-801">Name of any control of lookup page</span></span>
| <span data-ttu-id="a77ca-802">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-802">_valueFieldName</span></span> | <span data-ttu-id="a77ca-803">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-803">str</span></span> | <span data-ttu-id="a77ca-804">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-804">False</span></span> | <span data-ttu-id="a77ca-805">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="a77ca-805">Lookup value field.</span></span> <span data-ttu-id="a77ca-806">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-806">Name of control formed by root data contract constructing lookup page</span></span>

### <a name="method-displayfieldname"></a><span data-ttu-id="a77ca-807">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-807">Method displayFieldName</span></span>

<span data-ttu-id="a77ca-808">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-808">Gets the display field name of lookup control</span></span>

```xpp
public str displayFieldName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-809">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-809">Return Value</span></span>

<span data-ttu-id="a77ca-810">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-810">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="a77ca-811">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="a77ca-811">Method valueFieldName</span></span>

<span data-ttu-id="a77ca-812">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-812">Gets the value field name of lookup control</span></span>

```xpp
public str valueFieldName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-813">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-813">Return Value</span></span>

<span data-ttu-id="a77ca-814">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="a77ca-814">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="a77ca-815">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-815">Class SysAppLookupFieldAttribute</span></span>

<span data-ttu-id="a77ca-816">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-816">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-817">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-817">Methods</span></span>

| <span data-ttu-id="a77ca-818">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-818">Method name</span></span> | <span data-ttu-id="a77ca-819">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-819">Returns</span></span> | <span data-ttu-id="a77ca-820">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-820">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-821">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-821">new</span></span> | <span data-ttu-id="a77ca-822">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-822">void</span></span> | <span data-ttu-id="a77ca-823">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-823">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="a77ca-824">entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-824">entityName</span></span> | <span data-ttu-id="a77ca-825">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-825">str</span></span> | <span data-ttu-id="a77ca-826">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-826">Gets the name of the entity with which lookup page is related</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-827">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-827">Method new</span></span>

<span data-ttu-id="a77ca-828">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-828">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

```xpp
public void new ( _name)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-829">Parameters</span></span>

| <span data-ttu-id="a77ca-830">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-830">Parameter name</span></span> |  <span data-ttu-id="a77ca-831">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-831">Parameter type</span></span> | <span data-ttu-id="a77ca-832">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-832">Optional</span></span> | <span data-ttu-id="a77ca-833">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-833">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-834">_name</span><span class="sxs-lookup"><span data-stu-id="a77ca-834">_name</span></span> |  | <span data-ttu-id="a77ca-835">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-835">False</span></span> | <span data-ttu-id="a77ca-836">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-836">Name of the entity with which lookup page is related</span></span>

### <a name="method-entityname"></a><span data-ttu-id="a77ca-837">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="a77ca-837">Method entityName</span></span>

<span data-ttu-id="a77ca-838">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-838">Gets the name of the entity with which lookup page is related</span></span>

```xpp
public str entityName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-839">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-839">Return Value</span></span>

<span data-ttu-id="a77ca-840">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="a77ca-840">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="a77ca-841">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-841">Class SysAppPageAttribute</span></span>

<span data-ttu-id="a77ca-842">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-842">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-843">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-843">Methods</span></span>

| <span data-ttu-id="a77ca-844">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-844">Method name</span></span> | <span data-ttu-id="a77ca-845">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-845">Returns</span></span> | <span data-ttu-id="a77ca-846">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-846">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-847">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-847">new</span></span> | <span data-ttu-id="a77ca-848">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-848">void</span></span> | <span data-ttu-id="a77ca-849">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-849">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="a77ca-850">pageTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-850">pageTitle</span></span> | <span data-ttu-id="a77ca-851">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-851">str</span></span> | <span data-ttu-id="a77ca-852">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-852">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="a77ca-853">pageDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-853">pageDescription</span></span> | <span data-ttu-id="a77ca-854">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-854">str</span></span> | <span data-ttu-id="a77ca-855">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-855">Gets the Page Description</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-856">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-856">Method new</span></span>

<span data-ttu-id="a77ca-857">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-857">Creates a new instance of SysAppPageAttribute class</span></span>

```xpp
public void new ([str _pageTitle], [str _pageDescription])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-858">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-858">Parameters</span></span>

| <span data-ttu-id="a77ca-859">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-859">Parameter name</span></span> |  <span data-ttu-id="a77ca-860">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-860">Parameter type</span></span> | <span data-ttu-id="a77ca-861">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-861">Optional</span></span> | <span data-ttu-id="a77ca-862">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-862">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-863">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-863">_pageTitle</span></span> | <span data-ttu-id="a77ca-864">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-864">str</span></span> | <span data-ttu-id="a77ca-865">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-865">True</span></span> | <span data-ttu-id="a77ca-866">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-866">The page title</span></span>
| <span data-ttu-id="a77ca-867">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-867">_pageDescription</span></span> | <span data-ttu-id="a77ca-868">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-868">str</span></span> | <span data-ttu-id="a77ca-869">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-869">True</span></span> | <span data-ttu-id="a77ca-870">ページの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-870">The page description</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="a77ca-871">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-871">Method pageTitle</span></span>

<span data-ttu-id="a77ca-872">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-872">Gets the Page Title of the page</span></span>

```xpp
public str pageTitle ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-873">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-873">Return Value</span></span>

<span data-ttu-id="a77ca-874">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-874">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="a77ca-875">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-875">Method pageDescription</span></span>

<span data-ttu-id="a77ca-876">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-876">Gets the Page Description</span></span>

```xpp
public str pageDescription ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-877">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-877">Return Value</span></span>

<span data-ttu-id="a77ca-878">ページの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-878">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="a77ca-879">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-879">Class SysAppPageMetadata</span></span>

<span data-ttu-id="a77ca-880">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-880">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-881">方法</span><span class="sxs-lookup"><span data-stu-id="a77ca-881">Methods</span></span>

| <span data-ttu-id="a77ca-882">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-882">Method name</span></span> | <span data-ttu-id="a77ca-883">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-883">Returns</span></span> | <span data-ttu-id="a77ca-884">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-884">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-885">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-885">new</span></span> | <span data-ttu-id="a77ca-886">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-886">void</span></span> |  |
| <span data-ttu-id="a77ca-887">getPageName</span><span class="sxs-lookup"><span data-stu-id="a77ca-887">getPageName</span></span> | <span data-ttu-id="a77ca-888">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-888">str</span></span> | <span data-ttu-id="a77ca-889">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-889">Returns the page name</span></span> |
| <span data-ttu-id="a77ca-890">pageTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-890">pageTitle</span></span> | <span data-ttu-id="a77ca-891">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-891">str</span></span> | <span data-ttu-id="a77ca-892">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-892">Gets and sets the page title</span></span> |
| <span data-ttu-id="a77ca-893">pageDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-893">pageDescription</span></span> | <span data-ttu-id="a77ca-894">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-894">str</span></span> | <span data-ttu-id="a77ca-895">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-895">Gets or sets the page description</span></span> |
| <span data-ttu-id="a77ca-896">pageHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-896">pageHidden</span></span> | <span data-ttu-id="a77ca-897">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-897">boolean</span></span> | <span data-ttu-id="a77ca-898">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-898">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="a77ca-899">pageOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-899">pageOrder</span></span> | <span data-ttu-id="a77ca-900">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-900">int</span></span> | <span data-ttu-id="a77ca-901">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-901">Gets or sets the page order</span></span> |
| <span data-ttu-id="a77ca-902">getControl</span><span class="sxs-lookup"><span data-stu-id="a77ca-902">getControl</span></span> | <span data-ttu-id="a77ca-903">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-903">SysAppControlMetadata</span></span> | <span data-ttu-id="a77ca-904">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-904">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="a77ca-905">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-905">getControlEnumerator</span></span> | <span data-ttu-id="a77ca-906">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-906">MapEnumerator</span></span> | <span data-ttu-id="a77ca-907">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-907">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="a77ca-908">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-908">Where Key is control name and value is of type SysAppControlMetadata</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-909">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-909">Method new</span></span>

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-910">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-910">Parameters</span></span>

| <span data-ttu-id="a77ca-911">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-911">Parameter name</span></span> |  <span data-ttu-id="a77ca-912">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-912">Parameter type</span></span> | <span data-ttu-id="a77ca-913">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-913">Optional</span></span> | <span data-ttu-id="a77ca-914">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-914">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-915">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-915">_pageMetadata</span></span> | <span data-ttu-id="a77ca-916">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-916">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="a77ca-917">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-917">False</span></span> |

### <a name="method-getpagename"></a><span data-ttu-id="a77ca-918">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="a77ca-918">Method getPageName</span></span>

<span data-ttu-id="a77ca-919">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-919">Returns the page name</span></span>

```xpp
public str getPageName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-920">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-920">Return Value</span></span>

<span data-ttu-id="a77ca-921">ページ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-921">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="a77ca-922">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-922">Method pageTitle</span></span>

<span data-ttu-id="a77ca-923">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-923">Gets and sets the page title</span></span>

```xpp
public str pageTitle ([str _pageTitle])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-924">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-924">Parameters</span></span>

| <span data-ttu-id="a77ca-925">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-925">Parameter name</span></span> |  <span data-ttu-id="a77ca-926">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-926">Parameter type</span></span> | <span data-ttu-id="a77ca-927">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-927">Optional</span></span> | <span data-ttu-id="a77ca-928">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-928">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-929">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-929">_pageTitle</span></span> | <span data-ttu-id="a77ca-930">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-930">str</span></span> | <span data-ttu-id="a77ca-931">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-931">True</span></span> | <span data-ttu-id="a77ca-932">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-932">The page title</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-933">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-933">Return Value</span></span>

<span data-ttu-id="a77ca-934">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-934">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="a77ca-935">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-935">Method pageDescription</span></span>

<span data-ttu-id="a77ca-936">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-936">Gets or sets the page description</span></span>

```xpp
public str pageDescription ([str _pageDescription])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-937">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-937">Parameters</span></span>

| <span data-ttu-id="a77ca-938">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-938">Parameter name</span></span> |  <span data-ttu-id="a77ca-939">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-939">Parameter type</span></span> | <span data-ttu-id="a77ca-940">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-940">Optional</span></span> | <span data-ttu-id="a77ca-941">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-941">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-942">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-942">_pageDescription</span></span> | <span data-ttu-id="a77ca-943">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-943">str</span></span> | <span data-ttu-id="a77ca-944">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-944">True</span></span> | <span data-ttu-id="a77ca-945">ページの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-945">The page description</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-946">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-946">Return Value</span></span>

<span data-ttu-id="a77ca-947">ページの説明></span><span class="sxs-lookup"><span data-stu-id="a77ca-947">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="a77ca-948">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-948">Method pageHidden</span></span>

<span data-ttu-id="a77ca-949">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-949">Gets and sets whether the page is hidden in the workspace</span></span>

```xpp
public boolean pageHidden ([boolean _pageHidden])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-950">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-950">Parameters</span></span>

| <span data-ttu-id="a77ca-951">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-951">Parameter name</span></span> |  <span data-ttu-id="a77ca-952">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-952">Parameter type</span></span> | <span data-ttu-id="a77ca-953">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-953">Optional</span></span> | <span data-ttu-id="a77ca-954">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-954">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-955">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-955">_pageHidden</span></span> | <span data-ttu-id="a77ca-956">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-956">boolean</span></span> | <span data-ttu-id="a77ca-957">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-957">True</span></span> | <span data-ttu-id="a77ca-958">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="a77ca-958">page hidden value</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-959">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-959">Return Value</span></span>

<span data-ttu-id="a77ca-960">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="a77ca-960">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="a77ca-961">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-961">Method pageOrder</span></span>

<span data-ttu-id="a77ca-962">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-962">Gets or sets the page order</span></span>

```xpp
public int pageOrder ([int _pageOrder])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-963">Parameters</span></span>

| <span data-ttu-id="a77ca-964">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-964">Parameter name</span></span> |  <span data-ttu-id="a77ca-965">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-965">Parameter type</span></span> | <span data-ttu-id="a77ca-966">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-966">Optional</span></span> | <span data-ttu-id="a77ca-967">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-967">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-968">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="a77ca-968">_pageOrder</span></span> | <span data-ttu-id="a77ca-969">int</span><span class="sxs-lookup"><span data-stu-id="a77ca-969">int</span></span> | <span data-ttu-id="a77ca-970">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-970">True</span></span> | <span data-ttu-id="a77ca-971">ページの順序</span><span class="sxs-lookup"><span data-stu-id="a77ca-971">The page order</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-972">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-972">Return Value</span></span>

<span data-ttu-id="a77ca-973">ページの順序</span><span class="sxs-lookup"><span data-stu-id="a77ca-973">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="a77ca-974">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="a77ca-974">Method getControl</span></span>

<span data-ttu-id="a77ca-975">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-975">Returns the control on the current page having the provided control name</span></span>

```xpp
public SysAppControlMetadata getControl (str _controlName)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-976">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-976">Parameters</span></span>

| <span data-ttu-id="a77ca-977">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-977">Parameter name</span></span> |  <span data-ttu-id="a77ca-978">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-978">Parameter type</span></span> | <span data-ttu-id="a77ca-979">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-979">Optional</span></span> | <span data-ttu-id="a77ca-980">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-980">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-981">_controlName</span><span class="sxs-lookup"><span data-stu-id="a77ca-981">_controlName</span></span> | <span data-ttu-id="a77ca-982">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-982">str</span></span> | <span data-ttu-id="a77ca-983">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-983">False</span></span> | <span data-ttu-id="a77ca-984">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="a77ca-984">The control name that will be used to search for control</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-985">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-985">Return Value</span></span>

<span data-ttu-id="a77ca-986">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="a77ca-986">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="a77ca-987">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-987">Method getControlEnumerator</span></span>

<span data-ttu-id="a77ca-988">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-988">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="a77ca-989">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-989">Where Key is control name and value is of type SysAppControlMetadata</span></span>

```xpp
public MapEnumerator getControlEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-990">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-990">Return Value</span></span>

<span data-ttu-id="a77ca-991">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="a77ca-991">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="a77ca-992">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-992">Class SysAppProjectionAttribute</span></span>

<span data-ttu-id="a77ca-993">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-993">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-994">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-994">Methods</span></span>

| <span data-ttu-id="a77ca-995">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-995">Method name</span></span> | <span data-ttu-id="a77ca-996">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-996">Returns</span></span> | <span data-ttu-id="a77ca-997">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-997">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-998">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-998">new</span></span> | <span data-ttu-id="a77ca-999">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-999">void</span></span> | <span data-ttu-id="a77ca-1000">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-1000">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1001">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1001">Method new</span></span>

<span data-ttu-id="a77ca-1002">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-1002">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

```xpp
public void new (str _label)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1003">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1003">Parameters</span></span>

| <span data-ttu-id="a77ca-1004">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1004">Parameter name</span></span> |  <span data-ttu-id="a77ca-1005">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1005">Parameter type</span></span> | <span data-ttu-id="a77ca-1006">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1006">Optional</span></span> | <span data-ttu-id="a77ca-1007">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1007">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1008">_label</span><span class="sxs-lookup"><span data-stu-id="a77ca-1008">_label</span></span> | <span data-ttu-id="a77ca-1009">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1009">str</span></span> | <span data-ttu-id="a77ca-1010">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1010">False</span></span> | <span data-ttu-id="a77ca-1011">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="a77ca-1011">Control label</span></span>

## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="a77ca-1012">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-1012">Class SysAppRelationalAttribute</span></span>

<span data-ttu-id="a77ca-1013">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-1013">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1014">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1014">Methods</span></span>

| <span data-ttu-id="a77ca-1015">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1015">Method name</span></span> | <span data-ttu-id="a77ca-1016">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1016">Returns</span></span> | <span data-ttu-id="a77ca-1017">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1017">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1018">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-1018">new</span></span> | <span data-ttu-id="a77ca-1019">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1019">void</span></span> | <span data-ttu-id="a77ca-1020">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1020">Constructor</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1021">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1021">Method new</span></span>

<span data-ttu-id="a77ca-1022">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1022">Constructor</span></span>

```xpp
public void new ([str _name])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1023">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1023">Parameters</span></span>

| <span data-ttu-id="a77ca-1024">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1024">Parameter name</span></span> |  <span data-ttu-id="a77ca-1025">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1025">Parameter type</span></span> | <span data-ttu-id="a77ca-1026">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1026">Optional</span></span> | <span data-ttu-id="a77ca-1027">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1027">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1028">_name</span><span class="sxs-lookup"><span data-stu-id="a77ca-1028">_name</span></span> | <span data-ttu-id="a77ca-1029">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1029">str</span></span> | <span data-ttu-id="a77ca-1030">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1030">True</span></span> | <span data-ttu-id="a77ca-1031">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1031">Property name of the referenced entity</span></span>

## <a name="class-sysapprequestparams"></a><span data-ttu-id="a77ca-1032">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="a77ca-1032">Class SysAppRequestParams</span></span>

<span data-ttu-id="a77ca-1033">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1033">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1034">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1034">Methods</span></span>

| <span data-ttu-id="a77ca-1035">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1035">Method name</span></span> | <span data-ttu-id="a77ca-1036">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1036">Returns</span></span> | <span data-ttu-id="a77ca-1037">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1037">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1038">entityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1038">entityContext</span></span> | <span data-ttu-id="a77ca-1039">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1039">SysAppEntityContext</span></span> | <span data-ttu-id="a77ca-1040">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1040">Entity context of the request</span></span> |
| <span data-ttu-id="a77ca-1041">filterContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1041">filterContext</span></span> | <span data-ttu-id="a77ca-1042">リスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1042">List</span></span> | <span data-ttu-id="a77ca-1043">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1043">List of SysAppFilterContext for filter contexts</span></span> |

### <a name="method-entitycontext"></a><span data-ttu-id="a77ca-1044">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1044">Method entityContext</span></span>

<span data-ttu-id="a77ca-1045">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1045">Entity context of the request</span></span>

```xpp
public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1046">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1046">Parameters</span></span>

| <span data-ttu-id="a77ca-1047">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1047">Parameter name</span></span> |  <span data-ttu-id="a77ca-1048">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1048">Parameter type</span></span> | <span data-ttu-id="a77ca-1049">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1049">Optional</span></span> | <span data-ttu-id="a77ca-1050">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1050">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1051">_entityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1051">_entityContext</span></span> | <span data-ttu-id="a77ca-1052">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1052">SysAppEntityContext</span></span> | <span data-ttu-id="a77ca-1053">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1053">True</span></span> | <span data-ttu-id="a77ca-1054">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1054">Entity context of the request</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1055">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1055">Return Value</span></span>

<span data-ttu-id="a77ca-1056">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1056">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="a77ca-1057">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1057">Method filterContext</span></span>

<span data-ttu-id="a77ca-1058">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1058">List of SysAppFilterContext for filter contexts</span></span>

```xpp
public List filterContext ([List _filterContext])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1059">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1059">Parameters</span></span>

| <span data-ttu-id="a77ca-1060">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1060">Parameter name</span></span> |  <span data-ttu-id="a77ca-1061">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1061">Parameter type</span></span> | <span data-ttu-id="a77ca-1062">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1062">Optional</span></span> | <span data-ttu-id="a77ca-1063">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1063">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1064">_filterContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1064">_filterContext</span></span> | <span data-ttu-id="a77ca-1065">リスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1065">List</span></span> | <span data-ttu-id="a77ca-1066">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1066">True</span></span> | <span data-ttu-id="a77ca-1067">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1067">List of SysAppFilterContext for filter contexts of page</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1068">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1068">Return Value</span></span>

<span data-ttu-id="a77ca-1069">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1069">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="a77ca-1070">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="a77ca-1070">Class SysAppResponse</span></span>

<span data-ttu-id="a77ca-1071">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1071">SysAppResponse class.</span></span>  <span data-ttu-id="a77ca-1072">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1072">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1073">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1073">Methods</span></span>

| <span data-ttu-id="a77ca-1074">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1074">Method name</span></span> | <span data-ttu-id="a77ca-1075">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1075">Returns</span></span> | <span data-ttu-id="a77ca-1076">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1076">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1077">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-1077">new</span></span> | <span data-ttu-id="a77ca-1078">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1078">void</span></span> |  |
| <span data-ttu-id="a77ca-1079">jobId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1079">jobId</span></span> | <span data-ttu-id="a77ca-1080">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1080">str</span></span> | <span data-ttu-id="a77ca-1081">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="a77ca-1081">Job ID of the request</span></span> |
| <span data-ttu-id="a77ca-1082">データ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1082">data</span></span> | <span data-ttu-id="a77ca-1083">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="a77ca-1083">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="a77ca-1084">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1084">Data of the page</span></span> |
| <span data-ttu-id="a77ca-1085">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="a77ca-1085">failedInAppCall</span></span> | <span data-ttu-id="a77ca-1086">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1086">boolean</span></span> | <span data-ttu-id="a77ca-1087">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1087">Data of the page</span></span> |
| <span data-ttu-id="a77ca-1088">commits</span><span class="sxs-lookup"><span data-stu-id="a77ca-1088">commits</span></span> | <span data-ttu-id="a77ca-1089">一覧</span><span class="sxs-lookup"><span data-stu-id="a77ca-1089">List</span></span> | <span data-ttu-id="a77ca-1090">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1090">Commits after task is completed</span></span> |
| <span data-ttu-id="a77ca-1091">メッセージ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1091">messages</span></span> | <span data-ttu-id="a77ca-1092">一覧</span><span class="sxs-lookup"><span data-stu-id="a77ca-1092">List</span></span> | <span data-ttu-id="a77ca-1093">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="a77ca-1093">Job ID of the request</span></span> |
| <span data-ttu-id="a77ca-1094">addMessage</span><span class="sxs-lookup"><span data-stu-id="a77ca-1094">addMessage</span></span> | <span data-ttu-id="a77ca-1095">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1095">void</span></span> | <span data-ttu-id="a77ca-1096">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="a77ca-1096">Adds message</span></span> |
| <span data-ttu-id="a77ca-1097">addCommit</span><span class="sxs-lookup"><span data-stu-id="a77ca-1097">addCommit</span></span> | <span data-ttu-id="a77ca-1098">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1098">void</span></span> | <span data-ttu-id="a77ca-1099">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="a77ca-1099">Adds commits</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1100">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1100">Method new</span></span>

```xpp
public void new ()
```

### <a name="method-jobid"></a><span data-ttu-id="a77ca-1101">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1101">Method jobId</span></span>

<span data-ttu-id="a77ca-1102">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="a77ca-1102">Job ID of the request</span></span>

```xpp
public str jobId ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1103">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1103">Return Value</span></span>

<span data-ttu-id="a77ca-1104">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="a77ca-1104">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="a77ca-1105">メソッド data</span><span class="sxs-lookup"><span data-stu-id="a77ca-1105">Method data</span></span>

<span data-ttu-id="a77ca-1106">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1106">Data of the page</span></span>

```xpp
public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1107">Parameters</span></span>

| <span data-ttu-id="a77ca-1108">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1108">Parameter name</span></span> |  <span data-ttu-id="a77ca-1109">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1109">Parameter type</span></span> | <span data-ttu-id="a77ca-1110">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1110">Optional</span></span> | <span data-ttu-id="a77ca-1111">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1111">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1112">_data</span><span class="sxs-lookup"><span data-stu-id="a77ca-1112">_data</span></span> | <span data-ttu-id="a77ca-1113">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="a77ca-1113">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="a77ca-1114">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1114">True</span></span> | <span data-ttu-id="a77ca-1115">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1115">Data of the page</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1116">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1116">Return Value</span></span>

<span data-ttu-id="a77ca-1117">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1117">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="a77ca-1118">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="a77ca-1118">Method failedInAppCall</span></span>

<span data-ttu-id="a77ca-1119">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1119">Data of the page</span></span>

```xpp
public boolean failedInAppCall ([boolean _failedInAppCall])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1120">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1120">Parameters</span></span>

| <span data-ttu-id="a77ca-1121">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1121">Parameter name</span></span> |  <span data-ttu-id="a77ca-1122">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1122">Parameter type</span></span> | <span data-ttu-id="a77ca-1123">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1123">Optional</span></span> | <span data-ttu-id="a77ca-1124">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1124">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1125">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="a77ca-1125">_failedInAppCall</span></span> | <span data-ttu-id="a77ca-1126">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1126">boolean</span></span> | <span data-ttu-id="a77ca-1127">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1127">True</span></span> | <span data-ttu-id="a77ca-1128">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1128">Sets to true if it fails in calling application code</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1129">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1129">Return Value</span></span>

<span data-ttu-id="a77ca-1130">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1130">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="a77ca-1131">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="a77ca-1131">Method commits</span></span>

<span data-ttu-id="a77ca-1132">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1132">Commits after task is completed</span></span>

```xpp
public List commits ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1133">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1133">Return Value</span></span>

<span data-ttu-id="a77ca-1134">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1134">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="a77ca-1135">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="a77ca-1135">Method messages</span></span>

<span data-ttu-id="a77ca-1136">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="a77ca-1136">Job ID of the request</span></span>

```xpp
public List messages ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1137">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1137">Return Value</span></span>

<span data-ttu-id="a77ca-1138">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1138">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="a77ca-1139">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="a77ca-1139">Method addMessage</span></span>

<span data-ttu-id="a77ca-1140">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="a77ca-1140">Adds message</span></span>

```xpp
public void addMessage (SysAppResponseMessage _message)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1141">Parameters</span></span>

| <span data-ttu-id="a77ca-1142">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1142">Parameter name</span></span> |  <span data-ttu-id="a77ca-1143">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1143">Parameter type</span></span> | <span data-ttu-id="a77ca-1144">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1144">Optional</span></span> | <span data-ttu-id="a77ca-1145">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1145">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1146">_message</span><span class="sxs-lookup"><span data-stu-id="a77ca-1146">_message</span></span> | <span data-ttu-id="a77ca-1147">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a77ca-1147">SysAppResponseMessage</span></span> | <span data-ttu-id="a77ca-1148">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1148">False</span></span> | <span data-ttu-id="a77ca-1149">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1149">message as SysAppResponseMessage object</span></span>

### <a name="method-addcommit"></a><span data-ttu-id="a77ca-1150">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="a77ca-1150">Method addCommit</span></span>

<span data-ttu-id="a77ca-1151">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="a77ca-1151">Adds commits</span></span>

```xpp
public void addCommit (SysAppEntityContext _entityContext)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1152">Parameters</span></span>

| <span data-ttu-id="a77ca-1153">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1153">Parameter name</span></span> |  <span data-ttu-id="a77ca-1154">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1154">Parameter type</span></span> | <span data-ttu-id="a77ca-1155">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1155">Optional</span></span> | <span data-ttu-id="a77ca-1156">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1156">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1157">_entityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1157">_entityContext</span></span> | <span data-ttu-id="a77ca-1158">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="a77ca-1158">SysAppEntityContext</span></span> | <span data-ttu-id="a77ca-1159">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1159">False</span></span> | <span data-ttu-id="a77ca-1160">確定済エンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1160">Entity context containing entity name and entity ID of the entity that is committed</span></span>

## <a name="class-sysappresponsemessage"></a><span data-ttu-id="a77ca-1161">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a77ca-1161">Class SysAppResponseMessage</span></span>

<span data-ttu-id="a77ca-1162">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="a77ca-1162">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1163">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1163">Methods</span></span>

| <span data-ttu-id="a77ca-1164">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1164">Method name</span></span> | <span data-ttu-id="a77ca-1165">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1165">Returns</span></span> | <span data-ttu-id="a77ca-1166">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1166">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1167">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-1167">new</span></span> | <span data-ttu-id="a77ca-1168">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1168">void</span></span> | <span data-ttu-id="a77ca-1169">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-1169">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="a77ca-1170">テキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1170">text</span></span> | <span data-ttu-id="a77ca-1171">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1171">str</span></span> | <span data-ttu-id="a77ca-1172">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-1172">Gets the message text</span></span> |
| <span data-ttu-id="a77ca-1173">タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1173">type</span></span> | <span data-ttu-id="a77ca-1174">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1174">SysAppMessageType</span></span> | <span data-ttu-id="a77ca-1175">メッセージ タイプを取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="a77ca-1175">Gets the message type: info, error, warning</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1176">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1176">Method new</span></span>

<span data-ttu-id="a77ca-1177">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-1177">Creates a new instance of SysAppResponseMessage class</span></span>

```xpp
public void new (str _text, [SysAppMessageType _type])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1178">Parameters</span></span>

| <span data-ttu-id="a77ca-1179">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1179">Parameter name</span></span> |  <span data-ttu-id="a77ca-1180">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1180">Parameter type</span></span> | <span data-ttu-id="a77ca-1181">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1181">Optional</span></span> | <span data-ttu-id="a77ca-1182">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1182">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1183">_text</span><span class="sxs-lookup"><span data-stu-id="a77ca-1183">_text</span></span> | <span data-ttu-id="a77ca-1184">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1184">str</span></span> | <span data-ttu-id="a77ca-1185">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1185">False</span></span> | <span data-ttu-id="a77ca-1186">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1186">The message text</span></span>
| <span data-ttu-id="a77ca-1187">_type</span><span class="sxs-lookup"><span data-stu-id="a77ca-1187">_type</span></span> | <span data-ttu-id="a77ca-1188">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1188">SysAppMessageType</span></span> | <span data-ttu-id="a77ca-1189">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1189">True</span></span> | <span data-ttu-id="a77ca-1190">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="a77ca-1190">Message Type: info, error, warning</span></span>

### <a name="method-text"></a><span data-ttu-id="a77ca-1191">メソッド text</span><span class="sxs-lookup"><span data-stu-id="a77ca-1191">Method text</span></span>

<span data-ttu-id="a77ca-1192">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-1192">Gets the message text</span></span>

```xpp
public str text ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1193">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1193">Return Value</span></span>

<span data-ttu-id="a77ca-1194">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1194">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="a77ca-1195">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1195">Method type</span></span>

<span data-ttu-id="a77ca-1196">メッセージ タイプを取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="a77ca-1196">Gets the message type: info, error, warning</span></span>

```xpp
public SysAppMessageType type ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1197">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1197">Return Value</span></span>

<span data-ttu-id="a77ca-1198">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="a77ca-1198">The message type: info, error, warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="a77ca-1199">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-1199">Class SysAppSecurityAttribute</span></span>

<span data-ttu-id="a77ca-1200">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1200">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="a77ca-1201">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1201">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1202">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1202">Methods</span></span>

| <span data-ttu-id="a77ca-1203">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1203">Method name</span></span> | <span data-ttu-id="a77ca-1204">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1204">Returns</span></span> | <span data-ttu-id="a77ca-1205">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1205">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1206">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-1206">new</span></span> | <span data-ttu-id="a77ca-1207">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1207">void</span></span> | <span data-ttu-id="a77ca-1208">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1208">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="a77ca-1209">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="a77ca-1209">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="a77ca-1210">menuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1210">menuItemType</span></span> | <span data-ttu-id="a77ca-1211">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1211">MenuItemType</span></span> | <span data-ttu-id="a77ca-1212">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-1212">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="a77ca-1213">menuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1213">menuItemName</span></span> | <span data-ttu-id="a77ca-1214">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1214">MenuItemName</span></span> | <span data-ttu-id="a77ca-1215">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-1215">Gets the Menu Item Name of the page</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1216">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1216">Method new</span></span>

<span data-ttu-id="a77ca-1217">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1217">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="a77ca-1218">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="a77ca-1218">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

```xpp
public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1219">Parameters</span></span>

| <span data-ttu-id="a77ca-1220">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1220">Parameter name</span></span> |  <span data-ttu-id="a77ca-1221">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1221">Parameter type</span></span> | <span data-ttu-id="a77ca-1222">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1222">Optional</span></span> | <span data-ttu-id="a77ca-1223">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1223">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1224">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1224">_menuItemName</span></span> | <span data-ttu-id="a77ca-1225">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1225">MenuItemName</span></span> | <span data-ttu-id="a77ca-1226">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1226">True</span></span> | <span data-ttu-id="a77ca-1227">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1227">Menu Item Name of the page</span></span>
| <span data-ttu-id="a77ca-1228">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1228">_menuItemType</span></span> | <span data-ttu-id="a77ca-1229">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1229">MenuItemType</span></span> | <span data-ttu-id="a77ca-1230">True</span><span class="sxs-lookup"><span data-stu-id="a77ca-1230">True</span></span> | <span data-ttu-id="a77ca-1231">アクション、表示、または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1231">Menu Item Type of the page like action, display, or output</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="a77ca-1232">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1232">Method menuItemType</span></span>

<span data-ttu-id="a77ca-1233">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-1233">Gets the Menu Item Type of the page</span></span>

```xpp
public MenuItemType menuItemType ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1234">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1234">Return Value</span></span>

<span data-ttu-id="a77ca-1235">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1235">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="a77ca-1236">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1236">Method menuItemName</span></span>

<span data-ttu-id="a77ca-1237">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="a77ca-1237">Gets the Menu Item Name of the page</span></span>

```xpp
public MenuItemName menuItemName ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1238">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1238">Return Value</span></span>

<span data-ttu-id="a77ca-1239">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1239">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="a77ca-1240">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="a77ca-1240">Class SysAppWorkspace</span></span>

<span data-ttu-id="a77ca-1241">これは、 モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1241">This is the base class of mobile workspace.</span></span> <span data-ttu-id="a77ca-1242">モバイル ワークスペース クラスは、このクラスから拡張する必要があります</span><span class="sxs-lookup"><span data-stu-id="a77ca-1242">Mobile workspace classes need to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1243">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1243">Methods</span></span>

| <span data-ttu-id="a77ca-1244">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1244">Method name</span></span> | <span data-ttu-id="a77ca-1245">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1245">Returns</span></span> | <span data-ttu-id="a77ca-1246">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1246">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1247">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="a77ca-1247">getEnumValues</span></span> | <span data-ttu-id="a77ca-1248">リスト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1248">List</span></span> | <span data-ttu-id="a77ca-1249">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1249">Called during workspace initialization.</span></span> <span data-ttu-id="a77ca-1250">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="a77ca-1250">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="a77ca-1251">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-1251">getWorkspaceMetadata</span></span> | <span data-ttu-id="a77ca-1252">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-1252">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="a77ca-1253">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1253">Called during workspace initialization.</span></span> <span data-ttu-id="a77ca-1254">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="a77ca-1254">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="a77ca-1255">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="a77ca-1255">onBeginAppJob</span></span> | <span data-ttu-id="a77ca-1256">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1256">void</span></span> | <span data-ttu-id="a77ca-1257">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="a77ca-1257">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="a77ca-1258">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="a77ca-1258">onEndAppJob</span></span> | <span data-ttu-id="a77ca-1259">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1259">void</span></span> | <span data-ttu-id="a77ca-1260">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="a77ca-1260">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="a77ca-1261">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-1261">workspaceHidden</span></span> | <span data-ttu-id="a77ca-1262">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1262">boolean</span></span> | <span data-ttu-id="a77ca-1263">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1263">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="a77ca-1264">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1264">Checks that the current user has access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class.</span></span>  <span data-ttu-id="a77ca-1265">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1265">If the attribute is not specified on the class then it always returns false</span></span> |

### <a name="method-getenumvalues"></a><span data-ttu-id="a77ca-1266">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="a77ca-1266">Method getEnumValues</span></span>

<span data-ttu-id="a77ca-1267">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1267">Called during workspace initialization.</span></span> <span data-ttu-id="a77ca-1268">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="a77ca-1268">Can be used to modify the enum values that are returned to AX mobile</span></span>

```xpp
public List getEnumValues (EnumName _enumName)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1269">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1269">Parameters</span></span>

| <span data-ttu-id="a77ca-1270">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1270">Parameter name</span></span> |  <span data-ttu-id="a77ca-1271">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1271">Parameter type</span></span> | <span data-ttu-id="a77ca-1272">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1272">Optional</span></span> | <span data-ttu-id="a77ca-1273">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1273">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1274">_enumName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1274">_enumName</span></span> | <span data-ttu-id="a77ca-1275">EnumName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1275">EnumName</span></span> | <span data-ttu-id="a77ca-1276">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1276">False</span></span> | <span data-ttu-id="a77ca-1277">列挙名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1277">The enum name</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1278">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1278">Return Value</span></span>

<span data-ttu-id="a77ca-1279">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="a77ca-1279">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="a77ca-1280">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-1280">Method getWorkspaceMetadata</span></span>

<span data-ttu-id="a77ca-1281">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1281">Called during workspace initialization.</span></span> <span data-ttu-id="a77ca-1282">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="a77ca-1282">Can be used to modify the workspace metadata</span></span>

```xpp
public SysAppWorkspaceMetadata getWorkspaceMetadata ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1283">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1283">Return Value</span></span>

<span data-ttu-id="a77ca-1284">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1284">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="a77ca-1285">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="a77ca-1285">Method onBeginAppJob</span></span>

<span data-ttu-id="a77ca-1286">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="a77ca-1286">Called before the start of execution of AX mobile job</span></span>

```xpp
public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1287">Parameters</span></span>

| <span data-ttu-id="a77ca-1288">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1288">Parameter name</span></span> |  <span data-ttu-id="a77ca-1289">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1289">Parameter type</span></span> | <span data-ttu-id="a77ca-1290">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1290">Optional</span></span> | <span data-ttu-id="a77ca-1291">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1291">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1292">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="a77ca-1292">_sysAppJobRequest</span></span> | <span data-ttu-id="a77ca-1293">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="a77ca-1293">SysAppJobRequest</span></span> | <span data-ttu-id="a77ca-1294">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1294">False</span></span> | <span data-ttu-id="a77ca-1295">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="a77ca-1295">A class containing job request parameters</span></span>

### <a name="method-onendappjob"></a><span data-ttu-id="a77ca-1296">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="a77ca-1296">Method onEndAppJob</span></span>

<span data-ttu-id="a77ca-1297">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="a77ca-1297">Called after the end of execution of AX mobile job</span></span>

```xpp
public void onEndAppJob (SysAppJobResponse _sysAppJobResponse)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1298">Parameters</span></span>

| <span data-ttu-id="a77ca-1299">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1299">Parameter name</span></span> |  <span data-ttu-id="a77ca-1300">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1300">Parameter type</span></span> | <span data-ttu-id="a77ca-1301">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1301">Optional</span></span> | <span data-ttu-id="a77ca-1302">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1302">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1303">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="a77ca-1303">_sysAppJobResponse</span></span> | <span data-ttu-id="a77ca-1304">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="a77ca-1304">SysAppJobResponse</span></span> | <span data-ttu-id="a77ca-1305">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1305">False</span></span> | <span data-ttu-id="a77ca-1306">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="a77ca-1306">A class containing job response parameters</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="a77ca-1307">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-1307">Method workspaceHidden</span></span>

<span data-ttu-id="a77ca-1308">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1308">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="a77ca-1309">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1309">Checks that the current user has access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class.</span></span>  <span data-ttu-id="a77ca-1310">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1310">If the attribute is not specified on the class then it always returns false</span></span>

```xpp
public boolean workspaceHidden ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1311">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1311">Return Value</span></span>

<span data-ttu-id="a77ca-1312">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1312">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="a77ca-1313">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-1313">Class SysAppWorkspaceAttribute</span></span>

<span data-ttu-id="a77ca-1314">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1314">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1315">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1315">Methods</span></span>

| <span data-ttu-id="a77ca-1316">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1316">Method name</span></span> | <span data-ttu-id="a77ca-1317">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1317">Returns</span></span> | <span data-ttu-id="a77ca-1318">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1318">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1319">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-1319">new</span></span> | <span data-ttu-id="a77ca-1320">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1320">void</span></span> | <span data-ttu-id="a77ca-1321">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-1321">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="a77ca-1322">AppId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1322">AppId</span></span> | <span data-ttu-id="a77ca-1323">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1323">str</span></span> | <span data-ttu-id="a77ca-1324">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1324">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="a77ca-1325">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1325">AppResourceName</span></span> | <span data-ttu-id="a77ca-1326">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1326">str</span></span> | <span data-ttu-id="a77ca-1327">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1327">Gets or sets the AOT Resource name that contains the workspace</span></span> |
| <span data-ttu-id="a77ca-1328">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-1328">WorkspaceHidden</span></span> | <span data-ttu-id="a77ca-1329">ブール型</span><span class="sxs-lookup"><span data-stu-id="a77ca-1329">boolean</span></span> | <span data-ttu-id="a77ca-1330">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1330">Gets or sets if the workspace is hidden from designer</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1331">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1331">Method new</span></span>

<span data-ttu-id="a77ca-1332">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="a77ca-1332">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

```xpp
public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1333">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1333">Parameters</span></span>

| <span data-ttu-id="a77ca-1334">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1334">Parameter name</span></span> |  <span data-ttu-id="a77ca-1335">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1335">Parameter type</span></span> | <span data-ttu-id="a77ca-1336">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1336">Optional</span></span> | <span data-ttu-id="a77ca-1337">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1337">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1338">_appId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1338">_appId</span></span> | <span data-ttu-id="a77ca-1339">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1339">str</span></span> | <span data-ttu-id="a77ca-1340">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1340">False</span></span> | <span data-ttu-id="a77ca-1341">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1341">The appId of the workspace</span></span>
| <span data-ttu-id="a77ca-1342">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1342">_appResourceName</span></span> | <span data-ttu-id="a77ca-1343">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1343">str</span></span> | <span data-ttu-id="a77ca-1344">True</span><span class="sxs-lookup"><span data-stu-id="a77ca-1344">True</span></span> | <span data-ttu-id="a77ca-1345">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1345">The AOT resource name that contains the workspace</span></span>
| <span data-ttu-id="a77ca-1346">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-1346">_workspaceHidden</span></span> | <span data-ttu-id="a77ca-1347">ブール型</span><span class="sxs-lookup"><span data-stu-id="a77ca-1347">boolean</span></span> | <span data-ttu-id="a77ca-1348">True</span><span class="sxs-lookup"><span data-stu-id="a77ca-1348">True</span></span> | <span data-ttu-id="a77ca-1349">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="a77ca-1349">The workspace is hidden from designer</span></span>

### <a name="method-appid"></a><span data-ttu-id="a77ca-1350">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1350">Method AppId</span></span>

<span data-ttu-id="a77ca-1351">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1351">Gets or sets the AppId of the workspace</span></span>

```xpp
public str AppId ([str _appId])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1352">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1352">Parameters</span></span>

| <span data-ttu-id="a77ca-1353">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1353">Parameter name</span></span> |  <span data-ttu-id="a77ca-1354">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1354">Parameter type</span></span> | <span data-ttu-id="a77ca-1355">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1355">Optional</span></span> | <span data-ttu-id="a77ca-1356">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1356">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1357">_appId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1357">_appId</span></span> | <span data-ttu-id="a77ca-1358">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1358">str</span></span> | <span data-ttu-id="a77ca-1359">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1359">True</span></span> | <span data-ttu-id="a77ca-1360">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1360">The AppId of the workspace</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1361">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1361">Return Value</span></span>

<span data-ttu-id="a77ca-1362">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1362">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="a77ca-1363">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1363">Method AppResourceName</span></span>

<span data-ttu-id="a77ca-1364">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1364">Gets or sets the AOT Resource name that contains the workspace</span></span>

```xpp
public str AppResourceName ([str _appResourceName])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1365">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1365">Parameters</span></span>

| <span data-ttu-id="a77ca-1366">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1366">Parameter name</span></span> |  <span data-ttu-id="a77ca-1367">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1367">Parameter type</span></span> | <span data-ttu-id="a77ca-1368">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1368">Optional</span></span> | <span data-ttu-id="a77ca-1369">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1369">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1370">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1370">_appResourceName</span></span> | <span data-ttu-id="a77ca-1371">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1371">str</span></span> | <span data-ttu-id="a77ca-1372">True</span><span class="sxs-lookup"><span data-stu-id="a77ca-1372">True</span></span> | <span data-ttu-id="a77ca-1373">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1373">The AOT Resource name that contains the workspace</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1374">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1374">Return Value</span></span>

<span data-ttu-id="a77ca-1375">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1375">The AOT Resource name that contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="a77ca-1376">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-1376">Method WorkspaceHidden</span></span>

<span data-ttu-id="a77ca-1377">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1377">Gets or sets if the workspace is hidden from designer</span></span>

```xpp
public boolean WorkspaceHidden ([boolean _workspaceHidden])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1378">Parameters</span></span>

| <span data-ttu-id="a77ca-1379">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1379">Parameter name</span></span> |  <span data-ttu-id="a77ca-1380">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1380">Parameter type</span></span> | <span data-ttu-id="a77ca-1381">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1381">Optional</span></span> | <span data-ttu-id="a77ca-1382">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1382">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1383">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="a77ca-1383">_workspaceHidden</span></span> | <span data-ttu-id="a77ca-1384">ブール値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1384">boolean</span></span> | <span data-ttu-id="a77ca-1385">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1385">True</span></span> | <span data-ttu-id="a77ca-1386">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="a77ca-1386">The workspace hidden</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1387">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1387">Return Value</span></span>

<span data-ttu-id="a77ca-1388">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="a77ca-1388">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="a77ca-1389">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-1389">Class SysAppWorkspaceMetadata</span></span>

<span data-ttu-id="a77ca-1390">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1390">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1391">方法</span><span class="sxs-lookup"><span data-stu-id="a77ca-1391">Methods</span></span>

| <span data-ttu-id="a77ca-1392">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1392">Method name</span></span> | <span data-ttu-id="a77ca-1393">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1393">Returns</span></span> | <span data-ttu-id="a77ca-1394">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1394">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1395">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-1395">new</span></span> | <span data-ttu-id="a77ca-1396">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1396">void</span></span> |  |
| <span data-ttu-id="a77ca-1397">addConfig</span><span class="sxs-lookup"><span data-stu-id="a77ca-1397">addConfig</span></span> | <span data-ttu-id="a77ca-1398">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1398">void</span></span> | <span data-ttu-id="a77ca-1399">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1399">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="a77ca-1400">getPage</span><span class="sxs-lookup"><span data-stu-id="a77ca-1400">getPage</span></span> | <span data-ttu-id="a77ca-1401">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-1401">SysAppPageMetadata</span></span> | <span data-ttu-id="a77ca-1402">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1402">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="a77ca-1403">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-1403">getPageEnumerator</span></span> | <span data-ttu-id="a77ca-1404">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-1404">MapEnumerator</span></span> | <span data-ttu-id="a77ca-1405">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1405">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="a77ca-1406">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-1406">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="a77ca-1407">getAction</span><span class="sxs-lookup"><span data-stu-id="a77ca-1407">getAction</span></span> | <span data-ttu-id="a77ca-1408">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="a77ca-1408">SysAppActionMetadata</span></span> | <span data-ttu-id="a77ca-1409">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1409">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="a77ca-1410">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-1410">getActionEnumerator</span></span> | <span data-ttu-id="a77ca-1411">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-1411">MapEnumerator</span></span> | <span data-ttu-id="a77ca-1412">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1412">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="a77ca-1413">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-1413">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="a77ca-1414">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1414">getPageNameForRecordingId</span></span> | <span data-ttu-id="a77ca-1415">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1415">str</span></span> | <span data-ttu-id="a77ca-1416">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1416">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="a77ca-1417">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1417">getActionNameForRecordingId</span></span> | <span data-ttu-id="a77ca-1418">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1418">str</span></span> | <span data-ttu-id="a77ca-1419">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1419">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="a77ca-1420">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-1420">workspaceTitle</span></span> | <span data-ttu-id="a77ca-1421">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1421">str</span></span> | <span data-ttu-id="a77ca-1422">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1422">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="a77ca-1423">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-1423">workspaceDescription</span></span> | <span data-ttu-id="a77ca-1424">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1424">str</span></span> | <span data-ttu-id="a77ca-1425">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1425">Gets and sets the workspace description</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1426">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1426">Method new</span></span>

```xpp
public void new (str _appId, [SysAppWorkspaceAttribute _attribute])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1427">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1427">Parameters</span></span>

| <span data-ttu-id="a77ca-1428">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1428">Parameter name</span></span> |  <span data-ttu-id="a77ca-1429">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1429">Parameter type</span></span> | <span data-ttu-id="a77ca-1430">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1430">Optional</span></span> | <span data-ttu-id="a77ca-1431">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1431">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1432">_appId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1432">_appId</span></span> | <span data-ttu-id="a77ca-1433">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1433">str</span></span> | <span data-ttu-id="a77ca-1434">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1434">False</span></span> |
| <span data-ttu-id="a77ca-1435">_attribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-1435">_attribute</span></span> | <span data-ttu-id="a77ca-1436">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-1436">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="a77ca-1437">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1437">True</span></span> |

### <a name="method-addconfig"></a><span data-ttu-id="a77ca-1438">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="a77ca-1438">Method addConfig</span></span>

<span data-ttu-id="a77ca-1439">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1439">Adds a custom config to the mobile workspace metadata</span></span>

```xpp
public void addConfig (str _configName, object _configValue)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1440">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1440">Parameters</span></span>

| <span data-ttu-id="a77ca-1441">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1441">Parameter name</span></span> |  <span data-ttu-id="a77ca-1442">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1442">Parameter type</span></span> | <span data-ttu-id="a77ca-1443">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1443">Optional</span></span> | <span data-ttu-id="a77ca-1444">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1444">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1445">_configName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1445">_configName</span></span> | <span data-ttu-id="a77ca-1446">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1446">str</span></span> | <span data-ttu-id="a77ca-1447">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1447">False</span></span> | <span data-ttu-id="a77ca-1448">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1448">A config name</span></span>
| <span data-ttu-id="a77ca-1449">_configValue</span><span class="sxs-lookup"><span data-stu-id="a77ca-1449">_configValue</span></span> | <span data-ttu-id="a77ca-1450">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1450">object</span></span> | <span data-ttu-id="a77ca-1451">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1451">False</span></span> | <span data-ttu-id="a77ca-1452">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="a77ca-1452">An object of an X++ data contract class</span></span>

### <a name="method-getpage"></a><span data-ttu-id="a77ca-1453">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="a77ca-1453">Method getPage</span></span>

<span data-ttu-id="a77ca-1454">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1454">Returns the page with the pageName provided</span></span>

```xpp
public SysAppPageMetadata getPage (str _pageName)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1455">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1455">Parameters</span></span>

| <span data-ttu-id="a77ca-1456">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1456">Parameter name</span></span> |  <span data-ttu-id="a77ca-1457">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1457">Parameter type</span></span> | <span data-ttu-id="a77ca-1458">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1458">Optional</span></span> | <span data-ttu-id="a77ca-1459">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1459">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1460">_pageName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1460">_pageName</span></span> | <span data-ttu-id="a77ca-1461">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1461">str</span></span> | <span data-ttu-id="a77ca-1462">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1462">False</span></span> | <span data-ttu-id="a77ca-1463">ページ名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1463">A page name</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1464">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1464">Return Value</span></span>

<span data-ttu-id="a77ca-1465">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1465">Returns the pageMetadata if a page with the provided name exists; otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="a77ca-1466">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-1466">Method getPageEnumerator</span></span>

<span data-ttu-id="a77ca-1467">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1467">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="a77ca-1468">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-1468">Where key is page name and value is of type SysAppPageMetadata</span></span>

```xpp
public MapEnumerator getPageEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1469">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1469">Return Value</span></span>

<span data-ttu-id="a77ca-1470">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="a77ca-1470">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="a77ca-1471">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="a77ca-1471">Method getAction</span></span>

<span data-ttu-id="a77ca-1472">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1472">Returns the action with the actionName provided</span></span>

```xpp
public SysAppActionMetadata getAction (str _actionName)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1473">Parameters</span></span>

| <span data-ttu-id="a77ca-1474">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1474">Parameter name</span></span> |  <span data-ttu-id="a77ca-1475">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1475">Parameter type</span></span> | <span data-ttu-id="a77ca-1476">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1476">Optional</span></span> | <span data-ttu-id="a77ca-1477">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1477">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1478">_actionName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1478">_actionName</span></span> | <span data-ttu-id="a77ca-1479">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1479">str</span></span> | <span data-ttu-id="a77ca-1480">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1480">False</span></span> | <span data-ttu-id="a77ca-1481">アクション名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1481">An action name</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1482">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1482">Return Value</span></span>

<span data-ttu-id="a77ca-1483">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1483">Returns the ActionMetadata if an action with the provided name exists; otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="a77ca-1484">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="a77ca-1484">Method getActionEnumerator</span></span>

<span data-ttu-id="a77ca-1485">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1485">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="a77ca-1486">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="a77ca-1486">Where key is action name and value is of type SysAppActionMetadata</span></span>

```xpp
public MapEnumerator getActionEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="a77ca-1487">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1487">Return Value</span></span>

<span data-ttu-id="a77ca-1488">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="a77ca-1488">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="a77ca-1489">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1489">Method getPageNameForRecordingId</span></span>

<span data-ttu-id="a77ca-1490">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1490">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

```xpp
public str getPageNameForRecordingId (str _recordingId)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1491">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1491">Parameters</span></span>

| <span data-ttu-id="a77ca-1492">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1492">Parameter name</span></span> |  <span data-ttu-id="a77ca-1493">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1493">Parameter type</span></span> | <span data-ttu-id="a77ca-1494">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1494">Optional</span></span> | <span data-ttu-id="a77ca-1495">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1495">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1496">_recordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1496">_recordingId</span></span> | <span data-ttu-id="a77ca-1497">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1497">str</span></span> | <span data-ttu-id="a77ca-1498">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1498">False</span></span> | <span data-ttu-id="a77ca-1499">recordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1499">A recordingId</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1500">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1500">Return Value</span></span>

<span data-ttu-id="a77ca-1501">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1501">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="a77ca-1502">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1502">Method getActionNameForRecordingId</span></span>

<span data-ttu-id="a77ca-1503">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="a77ca-1503">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

```xpp
public str getActionNameForRecordingId (str _recordingId)
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1504">Parameters</span></span>

| <span data-ttu-id="a77ca-1505">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1505">Parameter name</span></span> |  <span data-ttu-id="a77ca-1506">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1506">Parameter type</span></span> | <span data-ttu-id="a77ca-1507">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1507">Optional</span></span> | <span data-ttu-id="a77ca-1508">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1508">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1509">_recordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1509">_recordingId</span></span> | <span data-ttu-id="a77ca-1510">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1510">str</span></span> | <span data-ttu-id="a77ca-1511">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1511">False</span></span> | <span data-ttu-id="a77ca-1512">recordingId</span><span class="sxs-lookup"><span data-stu-id="a77ca-1512">A recordingId</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1513">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1513">Return Value</span></span>

<span data-ttu-id="a77ca-1514">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です</span><span class="sxs-lookup"><span data-stu-id="a77ca-1514">An action name if the supplied recordingId is used by a workspace action; otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="a77ca-1515">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-1515">Method workspaceTitle</span></span>

<span data-ttu-id="a77ca-1516">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1516">Gets and sets the workspace title</span></span>

```xpp
public str workspaceTitle ([str _workspaceTitle])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1517">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1517">Parameters</span></span>

| <span data-ttu-id="a77ca-1518">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1518">Parameter name</span></span> |  <span data-ttu-id="a77ca-1519">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1519">Parameter type</span></span> | <span data-ttu-id="a77ca-1520">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1520">Optional</span></span> | <span data-ttu-id="a77ca-1521">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1521">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1522">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="a77ca-1522">_workspaceTitle</span></span> | <span data-ttu-id="a77ca-1523">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1523">str</span></span> | <span data-ttu-id="a77ca-1524">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1524">True</span></span> | <span data-ttu-id="a77ca-1525">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-1525">The workspace title</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1526">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1526">Return Value</span></span>

<span data-ttu-id="a77ca-1527">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="a77ca-1527">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="a77ca-1528">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-1528">Method workspaceDescription</span></span>

<span data-ttu-id="a77ca-1529">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1529">Gets and sets the workspace description</span></span>

```xpp
public str workspaceDescription ([str _workspaceDescription])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1530">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1530">Parameters</span></span>

| <span data-ttu-id="a77ca-1531">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1531">Parameter name</span></span> |  <span data-ttu-id="a77ca-1532">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1532">Parameter type</span></span> | <span data-ttu-id="a77ca-1533">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1533">Optional</span></span> | <span data-ttu-id="a77ca-1534">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1534">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1535">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="a77ca-1535">_workspaceDescription</span></span> | <span data-ttu-id="a77ca-1536">str</span><span class="sxs-lookup"><span data-stu-id="a77ca-1536">str</span></span> | <span data-ttu-id="a77ca-1537">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1537">True</span></span> | <span data-ttu-id="a77ca-1538">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1538">The workspace description</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1539">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1539">Return Value</span></span>

<span data-ttu-id="a77ca-1540">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1540">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="a77ca-1541">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="a77ca-1541">Class SysAppWorkspaceSecurityAttribute</span></span>

<span data-ttu-id="a77ca-1542">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="a77ca-1542">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="a77ca-1543">メソッド</span><span class="sxs-lookup"><span data-stu-id="a77ca-1543">Methods</span></span>

| <span data-ttu-id="a77ca-1544">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1544">Method name</span></span> | <span data-ttu-id="a77ca-1545">返品</span><span class="sxs-lookup"><span data-stu-id="a77ca-1545">Returns</span></span> | <span data-ttu-id="a77ca-1546">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1546">Description</span></span> |
|---|---|---|
| <span data-ttu-id="a77ca-1547">新規</span><span class="sxs-lookup"><span data-stu-id="a77ca-1547">new</span></span> | <span data-ttu-id="a77ca-1548">無効</span><span class="sxs-lookup"><span data-stu-id="a77ca-1548">void</span></span> | <span data-ttu-id="a77ca-1549">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="a77ca-1549">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="a77ca-1550">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1550">WorkspaceMenuItemName</span></span> | <span data-ttu-id="a77ca-1551">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1551">MenuItemName</span></span> | <span data-ttu-id="a77ca-1552">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1552">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="a77ca-1553">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1553">WorkspaceMenuItemType</span></span> | <span data-ttu-id="a77ca-1554">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1554">MenuItemType</span></span> | <span data-ttu-id="a77ca-1555">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1555">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |

### <a name="method-new"></a><span data-ttu-id="a77ca-1556">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a77ca-1556">Method new</span></span>

<span data-ttu-id="a77ca-1557">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="a77ca-1557">Creates a new instance of attribute</span></span>

```xpp
public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1558">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1558">Parameters</span></span>

| <span data-ttu-id="a77ca-1559">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1559">Parameter name</span></span> |  <span data-ttu-id="a77ca-1560">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1560">Parameter type</span></span> | <span data-ttu-id="a77ca-1561">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1561">Optional</span></span> | <span data-ttu-id="a77ca-1562">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1562">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1563">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1563">_workspaceMenuItemName</span></span> | <span data-ttu-id="a77ca-1564">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1564">MenuItemName</span></span> | <span data-ttu-id="a77ca-1565">False</span><span class="sxs-lookup"><span data-stu-id="a77ca-1565">False</span></span> | <span data-ttu-id="a77ca-1566">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1566">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="a77ca-1567">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1567">_workspaceMenuItemType</span></span> | <span data-ttu-id="a77ca-1568">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1568">MenuItemType</span></span> | <span data-ttu-id="a77ca-1569">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1569">True</span></span> | <span data-ttu-id="a77ca-1570">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1570">The menu item type</span></span>

### <a name="method-workspacemenuitemname"></a><span data-ttu-id="a77ca-1571">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1571">Method WorkspaceMenuItemName</span></span>

<span data-ttu-id="a77ca-1572">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1572">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

```xpp
public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1573">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1573">Parameters</span></span>

| <span data-ttu-id="a77ca-1574">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1574">Parameter name</span></span> |  <span data-ttu-id="a77ca-1575">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1575">Parameter type</span></span> | <span data-ttu-id="a77ca-1576">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1576">Optional</span></span> | <span data-ttu-id="a77ca-1577">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1577">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1578">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1578">_workspaceMenuItemName</span></span> | <span data-ttu-id="a77ca-1579">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="a77ca-1579">MenuItemName</span></span> | <span data-ttu-id="a77ca-1580">はい</span><span class="sxs-lookup"><span data-stu-id="a77ca-1580">True</span></span> | <span data-ttu-id="a77ca-1581">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="a77ca-1581">The workspace menu item for the workspace security attribute</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1582">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1582">Return Value</span></span>

<span data-ttu-id="a77ca-1583">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="a77ca-1583">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="a77ca-1584">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1584">Method WorkspaceMenuItemType</span></span>

<span data-ttu-id="a77ca-1585">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="a77ca-1585">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

```xpp
public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType])
```

#### <a name="parameters"></a><span data-ttu-id="a77ca-1586">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a77ca-1586">Parameters</span></span>

| <span data-ttu-id="a77ca-1587">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="a77ca-1587">Parameter name</span></span> |  <span data-ttu-id="a77ca-1588">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1588">Parameter type</span></span> | <span data-ttu-id="a77ca-1589">オプション</span><span class="sxs-lookup"><span data-stu-id="a77ca-1589">Optional</span></span> | <span data-ttu-id="a77ca-1590">説明</span><span class="sxs-lookup"><span data-stu-id="a77ca-1590">Description</span></span> |
|---|---|---|---|
| <span data-ttu-id="a77ca-1591">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1591">_workspaceMenuItemType</span></span> | <span data-ttu-id="a77ca-1592">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="a77ca-1592">MenuItemType</span></span> | <span data-ttu-id="a77ca-1593">True</span><span class="sxs-lookup"><span data-stu-id="a77ca-1593">True</span></span> | <span data-ttu-id="a77ca-1594">`workspacesecurity` 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1594">The workspace menu item type for the `workspacesecurity` attribute</span></span>

#### <a name="return-value"></a><span data-ttu-id="a77ca-1595">戻り値</span><span class="sxs-lookup"><span data-stu-id="a77ca-1595">Return Value</span></span>

<span data-ttu-id="a77ca-1596">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ca-1596">The workspace menu item type for the workspace security attribute</span></span>
