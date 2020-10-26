---
title: サーバー側の開発 (ワークスペース X++ API)
description: このトピックでは、モバイル フォン アプリをサポートするプラットフォームに関する詳細情報を提供します。これにより、オフラインおよびモバイルの相互関係が充実し、使いやすいデザイナー エクスペリエンスを実現できます。
author: RobinARH
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 255544
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 3b494f057a9181f0bde8fe7c2cf89c663fbf2f0e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987262"
---
# <a name="server-side-development-workspace-x-apis"></a><span data-ttu-id="8698d-103">サーバー側の開発 (ワークスペース X++ API)</span><span class="sxs-lookup"><span data-stu-id="8698d-103">Server-side development (workspace X++ APIs)</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="class-sysappactionattribute"></a><span data-ttu-id="8698d-104">クラス SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-104">Class SysAppActionAttribute</span></span>

<span data-ttu-id="8698d-105">ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-105">SysAppActionAttribute used for decorating methods defining actions of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-106">Methods</span></span>

| <span data-ttu-id="8698d-107">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-107">Method name</span></span> | <span data-ttu-id="8698d-108">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-108">Returns</span></span> | <span data-ttu-id="8698d-109">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-109">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-110">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-110">new</span></span> | <span data-ttu-id="8698d-111">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-111">void</span></span> | <span data-ttu-id="8698d-112">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-112">Creates a new instance of SysAppActionAttribute class</span></span> |
| <span data-ttu-id="8698d-113">pageMethodName</span><span class="sxs-lookup"><span data-stu-id="8698d-113">pageMethodName</span></span> | <span data-ttu-id="8698d-114">str</span><span class="sxs-lookup"><span data-stu-id="8698d-114">str</span></span> | <span data-ttu-id="8698d-115">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="8698d-115">Gets the get method name which forms the page under which this task resides</span></span> |
| <span data-ttu-id="8698d-116">actionTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-116">actionTitle</span></span> | <span data-ttu-id="8698d-117">str</span><span class="sxs-lookup"><span data-stu-id="8698d-117">str</span></span> | <span data-ttu-id="8698d-118">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-118">Gets the Action Title</span></span> |
| <span data-ttu-id="8698d-119">actionDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-119">actionDescription</span></span> | <span data-ttu-id="8698d-120">str</span><span class="sxs-lookup"><span data-stu-id="8698d-120">str</span></span> | <span data-ttu-id="8698d-121">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-121">Gets the Action Description</span></span> |
| <span data-ttu-id="8698d-122">crudOperationType</span><span class="sxs-lookup"><span data-stu-id="8698d-122">crudOperationType</span></span> | <span data-ttu-id="8698d-123">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="8698d-123">SysAppCRUDOperation</span></span> | <span data-ttu-id="8698d-124">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="8698d-124">Gets the Crud Operation Type like Create, Update, Delete</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-125">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-125">Method new</span></span>

<span data-ttu-id="8698d-126">SysAppActionAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-126">Creates a new instance of SysAppActionAttribute class</span></span>

```xpp
public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-127">Parameters</span></span>

| <span data-ttu-id="8698d-128">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-128">Parameter name</span></span> |  <span data-ttu-id="8698d-129">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-129">Parameter type</span></span> | <span data-ttu-id="8698d-130">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-130">Optional</span></span> | <span data-ttu-id="8698d-131">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-131">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-132">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-132">_actionTitle</span></span> | <span data-ttu-id="8698d-133">str</span><span class="sxs-lookup"><span data-stu-id="8698d-133">str</span></span> | <span data-ttu-id="8698d-134">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-134">True</span></span> | <span data-ttu-id="8698d-135">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-135">Action title</span></span>
| <span data-ttu-id="8698d-136">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-136">_actionDescription</span></span> | <span data-ttu-id="8698d-137">str</span><span class="sxs-lookup"><span data-stu-id="8698d-137">str</span></span> | <span data-ttu-id="8698d-138">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-138">True</span></span> | <span data-ttu-id="8698d-139">アクション説明</span><span class="sxs-lookup"><span data-stu-id="8698d-139">Action description</span></span>
| <span data-ttu-id="8698d-140">_crudOperationType</span><span class="sxs-lookup"><span data-stu-id="8698d-140">_crudOperationType</span></span> | <span data-ttu-id="8698d-141">SysAppCRUDOperation</span><span class="sxs-lookup"><span data-stu-id="8698d-141">SysAppCRUDOperation</span></span> | <span data-ttu-id="8698d-142">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-142">True</span></span> | <span data-ttu-id="8698d-143">作成、更新、削除などの CRUD の操作</span><span class="sxs-lookup"><span data-stu-id="8698d-143">CRUD operation like Create, Update, Delete</span></span>
| <span data-ttu-id="8698d-144">_pageMethodName</span><span class="sxs-lookup"><span data-stu-id="8698d-144">_pageMethodName</span></span> | <span data-ttu-id="8698d-145">str</span><span class="sxs-lookup"><span data-stu-id="8698d-145">str</span></span> | <span data-ttu-id="8698d-146">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-146">True</span></span> | <span data-ttu-id="8698d-147">親ページを構築するメソッドの名前</span><span class="sxs-lookup"><span data-stu-id="8698d-147">Name of the method constructing parent page</span></span>

### <a name="method-pagemethodname"></a><span data-ttu-id="8698d-148">メソッド pageMethodName</span><span class="sxs-lookup"><span data-stu-id="8698d-148">Method pageMethodName</span></span>

<span data-ttu-id="8698d-149">このタスクが存在するページを形成する Page メソッド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="8698d-149">Gets the get method name which forms the page under which this task resides</span></span>

```xpp
public str pageMethodName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-150">Return Value</span></span>

<span data-ttu-id="8698d-151">このタスクが存在するページを形成する Page メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-151">The page method name which forms the page under which this task resides</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="8698d-152">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-152">Method actionTitle</span></span>

<span data-ttu-id="8698d-153">アクション タイトルの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-153">Gets the Action Title</span></span>

```xpp
public str actionTitle ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-154">Return Value</span></span>

<span data-ttu-id="8698d-155">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-155">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="8698d-156">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-156">Method actionDescription</span></span>

<span data-ttu-id="8698d-157">アクション説明の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-157">Gets the Action Description</span></span>

```xpp
public str actionDescription ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-158">Return Value</span></span>

<span data-ttu-id="8698d-159">ページの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-159">The page description</span></span>

### <a name="method-crudoperationtype"></a><span data-ttu-id="8698d-160">メソッド crudOperationType</span><span class="sxs-lookup"><span data-stu-id="8698d-160">Method crudOperationType</span></span>

<span data-ttu-id="8698d-161">作成、更新、削除などの CRUD 操作タイプを取得</span><span class="sxs-lookup"><span data-stu-id="8698d-161">Gets the Crud Operation Type like Create, Update, Delete</span></span>

```xpp
public SysAppCRUDOperation crudOperationType ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-162">Return Value</span></span>

<span data-ttu-id="8698d-163">作成、更新、削除などの CRUD 操作タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-163">The Crud Operation Type like Create, Update, Delete</span></span>

## <a name="class-sysappactionmetadata"></a><span data-ttu-id="8698d-164">クラス SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-164">Class SysAppActionMetadata</span></span>

<span data-ttu-id="8698d-165">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="8698d-165">This class can be used to access and update AX mobile workspace action metadata</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-166">方法</span><span class="sxs-lookup"><span data-stu-id="8698d-166">Methods</span></span>

| <span data-ttu-id="8698d-167">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-167">Method name</span></span> | <span data-ttu-id="8698d-168">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-168">Returns</span></span> | <span data-ttu-id="8698d-169">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-169">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-170">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-170">new</span></span> | <span data-ttu-id="8698d-171">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-171">void</span></span> |  |
| <span data-ttu-id="8698d-172">getActionName</span><span class="sxs-lookup"><span data-stu-id="8698d-172">getActionName</span></span> | <span data-ttu-id="8698d-173">str</span><span class="sxs-lookup"><span data-stu-id="8698d-173">str</span></span> | <span data-ttu-id="8698d-174">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-174">Returns the action name</span></span> |
| <span data-ttu-id="8698d-175">actionTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-175">actionTitle</span></span> | <span data-ttu-id="8698d-176">str</span><span class="sxs-lookup"><span data-stu-id="8698d-176">str</span></span> | <span data-ttu-id="8698d-177">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-177">Gets or sets the action title</span></span> |
| <span data-ttu-id="8698d-178">actionDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-178">actionDescription</span></span> | <span data-ttu-id="8698d-179">str</span><span class="sxs-lookup"><span data-stu-id="8698d-179">str</span></span> | <span data-ttu-id="8698d-180">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-180">Gets or sets the action description</span></span> |
| <span data-ttu-id="8698d-181">actionHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-181">actionHidden</span></span> | <span data-ttu-id="8698d-182">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-182">boolean</span></span> | <span data-ttu-id="8698d-183">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-183">Gets or sets whether action is hidden</span></span> |
| <span data-ttu-id="8698d-184">actionOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-184">actionOrder</span></span> | <span data-ttu-id="8698d-185">int</span><span class="sxs-lookup"><span data-stu-id="8698d-185">int</span></span> | <span data-ttu-id="8698d-186">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-186">Gets or sets the action order</span></span> |
| <span data-ttu-id="8698d-187">getControl</span><span class="sxs-lookup"><span data-stu-id="8698d-187">getControl</span></span> | <span data-ttu-id="8698d-188">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-188">SysAppControlMetadata</span></span> | <span data-ttu-id="8698d-189">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-189">Returns the control on the current action having the provided control name</span></span> |
| <span data-ttu-id="8698d-190">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-190">getControlEnumerator</span></span> | <span data-ttu-id="8698d-191">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-191">MapEnumerator</span></span> | <span data-ttu-id="8698d-192">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-192">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="8698d-193">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-193">Where Key is control name and value is of type SysAppControlMetadata</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-194">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-194">Method new</span></span>

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-195">Parameters</span></span>

| <span data-ttu-id="8698d-196">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-196">Parameter name</span></span> |  <span data-ttu-id="8698d-197">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-197">Parameter type</span></span> | <span data-ttu-id="8698d-198">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-198">Optional</span></span> | <span data-ttu-id="8698d-199">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-199">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-200">_taskmetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-200">_taskmetadata</span></span> | <span data-ttu-id="8698d-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-201">Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata</span></span> | <span data-ttu-id="8698d-202">False</span><span class="sxs-lookup"><span data-stu-id="8698d-202">False</span></span> |

### <a name="method-getactionname"></a><span data-ttu-id="8698d-203">メソッド getActionName</span><span class="sxs-lookup"><span data-stu-id="8698d-203">Method getActionName</span></span>

<span data-ttu-id="8698d-204">アクション名を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-204">Returns the action name</span></span>

```xpp
public str getActionName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-205">Return Value</span></span>

<span data-ttu-id="8698d-206">アクション名</span><span class="sxs-lookup"><span data-stu-id="8698d-206">The action name</span></span>

### <a name="method-actiontitle"></a><span data-ttu-id="8698d-207">メソッド actionTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-207">Method actionTitle</span></span>

<span data-ttu-id="8698d-208">アクション タイトルの取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-208">Gets or sets the action title</span></span>

```xpp
public str actionTitle ([str _actionTitle])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-209">Parameters</span></span>

| <span data-ttu-id="8698d-210">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-210">Parameter name</span></span> |  <span data-ttu-id="8698d-211">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-211">Parameter type</span></span> | <span data-ttu-id="8698d-212">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-212">Optional</span></span> | <span data-ttu-id="8698d-213">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-213">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-214">_actionTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-214">_actionTitle</span></span> | <span data-ttu-id="8698d-215">str</span><span class="sxs-lookup"><span data-stu-id="8698d-215">str</span></span> | <span data-ttu-id="8698d-216">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-216">True</span></span> | <span data-ttu-id="8698d-217">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-217">The action title</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-218">Return Value</span></span>

<span data-ttu-id="8698d-219">アクション タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-219">The action title</span></span>

### <a name="method-actiondescription"></a><span data-ttu-id="8698d-220">メソッド actionDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-220">Method actionDescription</span></span>

<span data-ttu-id="8698d-221">アクションの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-221">Gets or sets the action description</span></span>

```xpp
public str actionDescription ([str _actionDescription])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-222">Parameters</span></span>

| <span data-ttu-id="8698d-223">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-223">Parameter name</span></span> |  <span data-ttu-id="8698d-224">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-224">Parameter type</span></span> | <span data-ttu-id="8698d-225">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-225">Optional</span></span> | <span data-ttu-id="8698d-226">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-226">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-227">_actionDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-227">_actionDescription</span></span> | <span data-ttu-id="8698d-228">str</span><span class="sxs-lookup"><span data-stu-id="8698d-228">str</span></span> | <span data-ttu-id="8698d-229">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-229">True</span></span> | <span data-ttu-id="8698d-230">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-230">The action description</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-231">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-231">Return Value</span></span>

<span data-ttu-id="8698d-232">アクションの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-232">The action description</span></span>

### <a name="method-actionhidden"></a><span data-ttu-id="8698d-233">メソッド actionHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-233">Method actionHidden</span></span>

<span data-ttu-id="8698d-234">アクションが非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-234">Gets or sets whether action is hidden</span></span>

```xpp
public boolean actionHidden ([boolean _actionHidden])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-235">Parameters</span></span>

| <span data-ttu-id="8698d-236">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-236">Parameter name</span></span> |  <span data-ttu-id="8698d-237">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-237">Parameter type</span></span> | <span data-ttu-id="8698d-238">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-238">Optional</span></span> | <span data-ttu-id="8698d-239">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-239">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-240">_actionHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-240">_actionHidden</span></span> | <span data-ttu-id="8698d-241">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-241">boolean</span></span> | <span data-ttu-id="8698d-242">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-242">True</span></span> | <span data-ttu-id="8698d-243">アクションの非表示値</span><span class="sxs-lookup"><span data-stu-id="8698d-243">Action hidden value</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-244">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-244">Return Value</span></span>

<span data-ttu-id="8698d-245">アクションが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8698d-245">True if the action is hidden; otherwise false</span></span>

### <a name="method-actionorder"></a><span data-ttu-id="8698d-246">メソッド actionOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-246">Method actionOrder</span></span>

<span data-ttu-id="8698d-247">アクション順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-247">Gets or sets the action order</span></span>

```xpp
public int actionOrder ([int _actionOrder])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-248">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-248">Parameters</span></span>

| <span data-ttu-id="8698d-249">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-249">Parameter name</span></span> |  <span data-ttu-id="8698d-250">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-250">Parameter type</span></span> | <span data-ttu-id="8698d-251">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-251">Optional</span></span> | <span data-ttu-id="8698d-252">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-252">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-253">_actionOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-253">_actionOrder</span></span> | <span data-ttu-id="8698d-254">int</span><span class="sxs-lookup"><span data-stu-id="8698d-254">int</span></span> | <span data-ttu-id="8698d-255">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-255">True</span></span> | <span data-ttu-id="8698d-256">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="8698d-256">The action order</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-257">Return Value</span></span>

<span data-ttu-id="8698d-258">アクションの順序</span><span class="sxs-lookup"><span data-stu-id="8698d-258">The action order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="8698d-259">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="8698d-259">Method getControl</span></span>

<span data-ttu-id="8698d-260">指定されたコントロールの名前を持つ現在のアクションのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-260">Returns the control on the current action having the provided control name</span></span>

```xpp
public SysAppControlMetadata getControl (str _controlName)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-261">Parameters</span></span>

| <span data-ttu-id="8698d-262">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-262">Parameter name</span></span> |  <span data-ttu-id="8698d-263">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-263">Parameter type</span></span> | <span data-ttu-id="8698d-264">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-264">Optional</span></span> | <span data-ttu-id="8698d-265">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-265">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-266">_controlName</span><span class="sxs-lookup"><span data-stu-id="8698d-266">_controlName</span></span> | <span data-ttu-id="8698d-267">str</span><span class="sxs-lookup"><span data-stu-id="8698d-267">str</span></span> | <span data-ttu-id="8698d-268">False</span><span class="sxs-lookup"><span data-stu-id="8698d-268">False</span></span> | <span data-ttu-id="8698d-269">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="8698d-269">The control name that will be used to search for control</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-270">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-270">Return Value</span></span>

<span data-ttu-id="8698d-271">指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="8698d-271">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the action; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="8698d-272">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-272">Method getControlEnumerator</span></span>

<span data-ttu-id="8698d-273">アクションの制御を列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-273">Returns a map enumerator that can be used to enumerate action controls.</span></span>  <span data-ttu-id="8698d-274">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-274">Where Key is control name and value is of type SysAppControlMetadata</span></span>

```xpp
public MapEnumerator getControlEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-275">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-275">Return Value</span></span>

<span data-ttu-id="8698d-276">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="8698d-276">A map enumerator</span></span>

## <a name="class-sysappattributehelper"></a><span data-ttu-id="8698d-277">クラス SysAppAttributeHelper</span><span class="sxs-lookup"><span data-stu-id="8698d-277">Class SysAppAttributeHelper</span></span>

<span data-ttu-id="8698d-278">拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス</span><span class="sxs-lookup"><span data-stu-id="8698d-278">SysAppAttributeHelper class for fetching attributes from all the extended class</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-279">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-279">Methods</span></span>

| <span data-ttu-id="8698d-280">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-280">Method name</span></span> | <span data-ttu-id="8698d-281">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-281">Returns</span></span> | <span data-ttu-id="8698d-282">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-282">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-283">getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="8698d-283">getAttributeFromClass</span></span> | <span data-ttu-id="8698d-284">SysAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-284">SysAttribute</span></span> | <span data-ttu-id="8698d-285">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="8698d-285">gets attribute from class</span></span> |

### <a name="method-getattributefromclass"></a><span data-ttu-id="8698d-286">メソッド getAttributeFromClass</span><span class="sxs-lookup"><span data-stu-id="8698d-286">Method getAttributeFromClass</span></span>

<span data-ttu-id="8698d-287">クラスから属性を取得します</span><span class="sxs-lookup"><span data-stu-id="8698d-287">gets attribute from class</span></span>

```xpp
public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-288">Parameters</span></span>

| <span data-ttu-id="8698d-289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-289">Parameter name</span></span> |  <span data-ttu-id="8698d-290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-290">Parameter type</span></span> | <span data-ttu-id="8698d-291">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-291">Optional</span></span> | <span data-ttu-id="8698d-292">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-293">_sysClass</span><span class="sxs-lookup"><span data-stu-id="8698d-293">_sysClass</span></span> | <span data-ttu-id="8698d-294">SysDictClass</span><span class="sxs-lookup"><span data-stu-id="8698d-294">SysDictClass</span></span> | <span data-ttu-id="8698d-295">False</span><span class="sxs-lookup"><span data-stu-id="8698d-295">False</span></span> | <span data-ttu-id="8698d-296">属性が必要なクラス</span><span class="sxs-lookup"><span data-stu-id="8698d-296">class for which attributes is required</span></span>
| <span data-ttu-id="8698d-297">_attributeType</span><span class="sxs-lookup"><span data-stu-id="8698d-297">_attributeType</span></span> | <span data-ttu-id="8698d-298">SysAppAttributeType</span><span class="sxs-lookup"><span data-stu-id="8698d-298">SysAppAttributeType</span></span> | <span data-ttu-id="8698d-299">False</span><span class="sxs-lookup"><span data-stu-id="8698d-299">False</span></span> | <span data-ttu-id="8698d-300">SysAppEntityAttribute と同様の属性の型</span><span class="sxs-lookup"><span data-stu-id="8698d-300">Type of attribute like SysAppEntityAttribute</span></span>

## <a name="class-sysappcollectionattribute"></a><span data-ttu-id="8698d-301">クラス SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-301">Class SysAppCollectionAttribute</span></span>

<span data-ttu-id="8698d-302">リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-302">SysAppCollectionAttribute used for decorating methods forming list control</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-303">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-303">Methods</span></span>

| <span data-ttu-id="8698d-304">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-304">Method name</span></span> | <span data-ttu-id="8698d-305">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-305">Returns</span></span> | <span data-ttu-id="8698d-306">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-306">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-307">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-307">new</span></span> | <span data-ttu-id="8698d-308">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-308">void</span></span> | <span data-ttu-id="8698d-309">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8698d-309">Constructor</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-310">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-310">Method new</span></span>

<span data-ttu-id="8698d-311">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8698d-311">Constructor</span></span>

```xpp
public void new (str _itemContractName, [str _label], [str _relationshipName])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-312">Parameters</span></span>

| <span data-ttu-id="8698d-313">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-313">Parameter name</span></span> |  <span data-ttu-id="8698d-314">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-314">Parameter type</span></span> | <span data-ttu-id="8698d-315">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-315">Optional</span></span> | <span data-ttu-id="8698d-316">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-316">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-317">_itemContractName</span><span class="sxs-lookup"><span data-stu-id="8698d-317">_itemContractName</span></span> | <span data-ttu-id="8698d-318">str</span><span class="sxs-lookup"><span data-stu-id="8698d-318">str</span></span> | <span data-ttu-id="8698d-319">False</span><span class="sxs-lookup"><span data-stu-id="8698d-319">False</span></span> | <span data-ttu-id="8698d-320">リスト項目のデータ契約名</span><span class="sxs-lookup"><span data-stu-id="8698d-320">Data contract name of list item</span></span>
| <span data-ttu-id="8698d-321">_label</span><span class="sxs-lookup"><span data-stu-id="8698d-321">_label</span></span> | <span data-ttu-id="8698d-322">str</span><span class="sxs-lookup"><span data-stu-id="8698d-322">str</span></span> | <span data-ttu-id="8698d-323">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-323">True</span></span> | <span data-ttu-id="8698d-324">リスト コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="8698d-324">List control label</span></span>
| <span data-ttu-id="8698d-325">_relationshipName</span><span class="sxs-lookup"><span data-stu-id="8698d-325">_relationshipName</span></span> | <span data-ttu-id="8698d-326">str</span><span class="sxs-lookup"><span data-stu-id="8698d-326">str</span></span> | <span data-ttu-id="8698d-327">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-327">True</span></span> | <span data-ttu-id="8698d-328">関係名。</span><span class="sxs-lookup"><span data-stu-id="8698d-328">Relationship name.</span></span> <span data-ttu-id="8698d-329">既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。</span><span class="sxs-lookup"><span data-stu-id="8698d-329">By default the entity name of the list item is used as relationship name</span></span>

## <a name="class-sysappcontrolmetadata"></a><span data-ttu-id="8698d-330">クラス SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-330">Class SysAppControlMetadata</span></span>

<span data-ttu-id="8698d-331">容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。</span><span class="sxs-lookup"><span data-stu-id="8698d-331">Represents an X++ wrapper over the managed ControlMetadata object to facilitate.</span></span>  <span data-ttu-id="8698d-332">X++ オブジェクトとしてオブジェクトを回覧</span><span class="sxs-lookup"><span data-stu-id="8698d-332">passing around the object as X++ object</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-333">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-333">Methods</span></span>

| <span data-ttu-id="8698d-334">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-334">Method name</span></span> | <span data-ttu-id="8698d-335">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-335">Returns</span></span> | <span data-ttu-id="8698d-336">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-336">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-337">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-337">new</span></span> | <span data-ttu-id="8698d-338">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-338">void</span></span> | <span data-ttu-id="8698d-339">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-339">Creates a new instance of the control metadata</span></span> |
| <span data-ttu-id="8698d-340">getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="8698d-340">getBaseLanguageId</span></span> | <span data-ttu-id="8698d-341">str</span><span class="sxs-lookup"><span data-stu-id="8698d-341">str</span></span> | <span data-ttu-id="8698d-342">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-342">Returns the base language id for the app</span></span> |
| <span data-ttu-id="8698d-343">getControlName</span><span class="sxs-lookup"><span data-stu-id="8698d-343">getControlName</span></span> | <span data-ttu-id="8698d-344">str</span><span class="sxs-lookup"><span data-stu-id="8698d-344">str</span></span> | <span data-ttu-id="8698d-345">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-345">Returns the control name</span></span> |
| <span data-ttu-id="8698d-346">controlLabel</span><span class="sxs-lookup"><span data-stu-id="8698d-346">controlLabel</span></span> | <span data-ttu-id="8698d-347">str</span><span class="sxs-lookup"><span data-stu-id="8698d-347">str</span></span> | <span data-ttu-id="8698d-348">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-348">Gets and sets the control label</span></span> |
| <span data-ttu-id="8698d-349">controlHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-349">controlHidden</span></span> | <span data-ttu-id="8698d-350">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-350">boolean</span></span> | <span data-ttu-id="8698d-351">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-351">Gets and sets whether the control is hidden</span></span> |
| <span data-ttu-id="8698d-352">controlOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-352">controlOrder</span></span> | <span data-ttu-id="8698d-353">int</span><span class="sxs-lookup"><span data-stu-id="8698d-353">int</span></span> | <span data-ttu-id="8698d-354">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-354">Gets or sets the control order</span></span> |
| <span data-ttu-id="8698d-355">controlMandatory</span><span class="sxs-lookup"><span data-stu-id="8698d-355">controlMandatory</span></span> | <span data-ttu-id="8698d-356">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-356">boolean</span></span> | <span data-ttu-id="8698d-357">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-357">Gets or sets the control mandatory</span></span> |
| <span data-ttu-id="8698d-358">controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="8698d-358">controlAllowNegative</span></span> | <span data-ttu-id="8698d-359">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-359">boolean</span></span> | <span data-ttu-id="8698d-360">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="8698d-360">Gets or sets the control allow negative</span></span> |
| <span data-ttu-id="8698d-361">controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="8698d-361">controlMaxLength</span></span> | <span data-ttu-id="8698d-362">int</span><span class="sxs-lookup"><span data-stu-id="8698d-362">int</span></span> | <span data-ttu-id="8698d-363">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-363">Gets or sets the control max length</span></span> |
| <span data-ttu-id="8698d-364">getProperty</span><span class="sxs-lookup"><span data-stu-id="8698d-364">getProperty</span></span> | <span data-ttu-id="8698d-365">anytype</span><span class="sxs-lookup"><span data-stu-id="8698d-365">anytype</span></span> | <span data-ttu-id="8698d-366">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="8698d-366">Gets the control property referenced by the key</span></span> |
| <span data-ttu-id="8698d-367">setProperty</span><span class="sxs-lookup"><span data-stu-id="8698d-367">setProperty</span></span> | <span data-ttu-id="8698d-368">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-368">void</span></span> | <span data-ttu-id="8698d-369">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8698d-369">Sets the control property referenced by the key</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-370">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-370">Method new</span></span>

<span data-ttu-id="8698d-371">コントロールのメタデータの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-371">Creates a new instance of the control metadata</span></span>

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-372">Parameters</span></span>

| <span data-ttu-id="8698d-373">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-373">Parameter name</span></span> |  <span data-ttu-id="8698d-374">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-374">Parameter type</span></span> | <span data-ttu-id="8698d-375">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-375">Optional</span></span> | <span data-ttu-id="8698d-376">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-376">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-377">_controlMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-377">_controlMetadata</span></span> | <span data-ttu-id="8698d-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-378">Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata</span></span> | <span data-ttu-id="8698d-379">False</span><span class="sxs-lookup"><span data-stu-id="8698d-379">False</span></span> | <span data-ttu-id="8698d-380">controlMetadata オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8698d-380">The controlMetadata object</span></span>
| <span data-ttu-id="8698d-381">_baseLanguageId</span><span class="sxs-lookup"><span data-stu-id="8698d-381">_baseLanguageId</span></span> | <span data-ttu-id="8698d-382">str</span><span class="sxs-lookup"><span data-stu-id="8698d-382">str</span></span> | <span data-ttu-id="8698d-383">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-383">True</span></span> | <span data-ttu-id="8698d-384">基本言語</span><span class="sxs-lookup"><span data-stu-id="8698d-384">The base language</span></span>

### <a name="method-getbaselanguageid"></a><span data-ttu-id="8698d-385">メソッド getBaseLanguageId</span><span class="sxs-lookup"><span data-stu-id="8698d-385">Method getBaseLanguageId</span></span>

<span data-ttu-id="8698d-386">アプリケーションの基本言語 id を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-386">Returns the base language id for the app</span></span>

```xpp
public str getBaseLanguageId ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-387">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-387">Return Value</span></span>

<span data-ttu-id="8698d-388">基本言語 ID</span><span class="sxs-lookup"><span data-stu-id="8698d-388">The base language id</span></span>

### <a name="method-getcontrolname"></a><span data-ttu-id="8698d-389">メソッド getControlName</span><span class="sxs-lookup"><span data-stu-id="8698d-389">Method getControlName</span></span>

<span data-ttu-id="8698d-390">コントロール名を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-390">Returns the control name</span></span>

```xpp
public str getControlName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-391">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-391">Return Value</span></span>

<span data-ttu-id="8698d-392">コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="8698d-392">The control name</span></span>

### <a name="method-controllabel"></a><span data-ttu-id="8698d-393">メソッド controlLabel</span><span class="sxs-lookup"><span data-stu-id="8698d-393">Method controlLabel</span></span>

<span data-ttu-id="8698d-394">コントロール ラベルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-394">Gets and sets the control label</span></span>

```xpp
public str controlLabel ([str _controlLabel])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-395">Parameters</span></span>

| <span data-ttu-id="8698d-396">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-396">Parameter name</span></span> |  <span data-ttu-id="8698d-397">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-397">Parameter type</span></span> | <span data-ttu-id="8698d-398">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-398">Optional</span></span> | <span data-ttu-id="8698d-399">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-399">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-400">_controlLabel</span><span class="sxs-lookup"><span data-stu-id="8698d-400">_controlLabel</span></span> | <span data-ttu-id="8698d-401">str</span><span class="sxs-lookup"><span data-stu-id="8698d-401">str</span></span> | <span data-ttu-id="8698d-402">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-402">True</span></span> | <span data-ttu-id="8698d-403">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="8698d-403">The control label</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-404">Return Value</span></span>

<span data-ttu-id="8698d-405">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="8698d-405">The control label</span></span>

### <a name="method-controlhidden"></a><span data-ttu-id="8698d-406">メソッド controlHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-406">Method controlHidden</span></span>

<span data-ttu-id="8698d-407">コントロールを非表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-407">Gets and sets whether the control is hidden</span></span>

```xpp
public boolean controlHidden ([boolean _controlHidden])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-408">Parameters</span></span>

| <span data-ttu-id="8698d-409">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-409">Parameter name</span></span> |  <span data-ttu-id="8698d-410">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-410">Parameter type</span></span> | <span data-ttu-id="8698d-411">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-411">Optional</span></span> | <span data-ttu-id="8698d-412">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-412">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-413">_controlHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-413">_controlHidden</span></span> | <span data-ttu-id="8698d-414">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-414">boolean</span></span> | <span data-ttu-id="8698d-415">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-415">True</span></span> | <span data-ttu-id="8698d-416">非表示値の制御</span><span class="sxs-lookup"><span data-stu-id="8698d-416">Control hidden value</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-417">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-417">Return Value</span></span>

<span data-ttu-id="8698d-418">コントロールが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8698d-418">True if the control is hidden; otherwise false</span></span>

### <a name="method-controlorder"></a><span data-ttu-id="8698d-419">メソッド controlOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-419">Method controlOrder</span></span>

<span data-ttu-id="8698d-420">コントロール順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-420">Gets or sets the control order</span></span>

```xpp
public int controlOrder ([int _controlOrder])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-421">Parameters</span></span>

| <span data-ttu-id="8698d-422">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-422">Parameter name</span></span> |  <span data-ttu-id="8698d-423">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-423">Parameter type</span></span> | <span data-ttu-id="8698d-424">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-424">Optional</span></span> | <span data-ttu-id="8698d-425">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-425">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-426">_controlOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-426">_controlOrder</span></span> | <span data-ttu-id="8698d-427">int</span><span class="sxs-lookup"><span data-stu-id="8698d-427">int</span></span> | <span data-ttu-id="8698d-428">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-428">True</span></span> | <span data-ttu-id="8698d-429">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="8698d-429">The control order</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-430">Return Value</span></span>

<span data-ttu-id="8698d-431">コントロール順序</span><span class="sxs-lookup"><span data-stu-id="8698d-431">The control order</span></span>

### <a name="method-controlmandatory"></a><span data-ttu-id="8698d-432">メソッド controlMandatory</span><span class="sxs-lookup"><span data-stu-id="8698d-432">Method controlMandatory</span></span>

<span data-ttu-id="8698d-433">必須コントロールの取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-433">Gets or sets the control mandatory</span></span>

```xpp
public boolean controlMandatory ([boolean _controlMandatory])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-434">Parameters</span></span>

| <span data-ttu-id="8698d-435">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-435">Parameter name</span></span> |  <span data-ttu-id="8698d-436">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-436">Parameter type</span></span> | <span data-ttu-id="8698d-437">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-437">Optional</span></span> | <span data-ttu-id="8698d-438">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-438">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-439">_controlMandatory</span><span class="sxs-lookup"><span data-stu-id="8698d-439">_controlMandatory</span></span> | <span data-ttu-id="8698d-440">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-440">boolean</span></span> | <span data-ttu-id="8698d-441">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-441">True</span></span> | <span data-ttu-id="8698d-442">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="8698d-442">The control mandatory</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-443">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-443">Return Value</span></span>

<span data-ttu-id="8698d-444">必須のコントロール</span><span class="sxs-lookup"><span data-stu-id="8698d-444">The control mandatory</span></span>

### <a name="method-controlallownegative"></a><span data-ttu-id="8698d-445">メソッド controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="8698d-445">Method controlAllowNegative</span></span>

<span data-ttu-id="8698d-446">負の値を許可するコントロールを取得または設定します</span><span class="sxs-lookup"><span data-stu-id="8698d-446">Gets or sets the control allow negative</span></span>

```xpp
public boolean controlAllowNegative ([boolean _controlAllowNegative])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-447">Parameters</span></span>

| <span data-ttu-id="8698d-448">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-448">Parameter name</span></span> |  <span data-ttu-id="8698d-449">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-449">Parameter type</span></span> | <span data-ttu-id="8698d-450">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-450">Optional</span></span> | <span data-ttu-id="8698d-451">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-451">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-452">_controlAllowNegative</span><span class="sxs-lookup"><span data-stu-id="8698d-452">_controlAllowNegative</span></span> | <span data-ttu-id="8698d-453">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-453">boolean</span></span> | <span data-ttu-id="8698d-454">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-454">True</span></span> | <span data-ttu-id="8698d-455">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="8698d-455">The control allow negative</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-456">Return Value</span></span>

<span data-ttu-id="8698d-457">コントロールは負の値を許可します。</span><span class="sxs-lookup"><span data-stu-id="8698d-457">The control allow negative</span></span>

### <a name="method-controlmaxlength"></a><span data-ttu-id="8698d-458">メソッド controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="8698d-458">Method controlMaxLength</span></span>

<span data-ttu-id="8698d-459">コントロールの最大長の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-459">Gets or sets the control max length</span></span>

```xpp
public int controlMaxLength ([int _controlMaxLength])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-460">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-460">Parameters</span></span>

| <span data-ttu-id="8698d-461">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-461">Parameter name</span></span> |  <span data-ttu-id="8698d-462">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-462">Parameter type</span></span> | <span data-ttu-id="8698d-463">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-463">Optional</span></span> | <span data-ttu-id="8698d-464">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-464">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-465">_controlMaxLength</span><span class="sxs-lookup"><span data-stu-id="8698d-465">_controlMaxLength</span></span> | <span data-ttu-id="8698d-466">int</span><span class="sxs-lookup"><span data-stu-id="8698d-466">int</span></span> | <span data-ttu-id="8698d-467">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-467">True</span></span> | <span data-ttu-id="8698d-468">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="8698d-468">The control max length</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-469">Return Value</span></span>

<span data-ttu-id="8698d-470">コントロールの最大長</span><span class="sxs-lookup"><span data-stu-id="8698d-470">The control max length</span></span>

### <a name="method-getproperty"></a><span data-ttu-id="8698d-471">メソッド getProperty</span><span class="sxs-lookup"><span data-stu-id="8698d-471">Method getProperty</span></span>

<span data-ttu-id="8698d-472">キーによって参照されるコントロール プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="8698d-472">Gets the control property referenced by the key</span></span>

```xpp
public anytype getProperty (str _key)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-473">Parameters</span></span>

| <span data-ttu-id="8698d-474">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-474">Parameter name</span></span> |  <span data-ttu-id="8698d-475">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-475">Parameter type</span></span> | <span data-ttu-id="8698d-476">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-476">Optional</span></span> | <span data-ttu-id="8698d-477">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-477">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-478">_key</span><span class="sxs-lookup"><span data-stu-id="8698d-478">_key</span></span> | <span data-ttu-id="8698d-479">str</span><span class="sxs-lookup"><span data-stu-id="8698d-479">str</span></span> | <span data-ttu-id="8698d-480">False</span><span class="sxs-lookup"><span data-stu-id="8698d-480">False</span></span> | <span data-ttu-id="8698d-481">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="8698d-481">The name of the control property</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-482">Return Value</span></span>

<span data-ttu-id="8698d-483">プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="8698d-483">The property value</span></span>

### <a name="method-setproperty"></a><span data-ttu-id="8698d-484">メソッド setProperty</span><span class="sxs-lookup"><span data-stu-id="8698d-484">Method setProperty</span></span>

<span data-ttu-id="8698d-485">キーによって参照されるコントロール プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8698d-485">Sets the control property referenced by the key</span></span>

```xpp
public void setProperty (str _key, anytype _value)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-486">Parameters</span></span>

| <span data-ttu-id="8698d-487">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-487">Parameter name</span></span> |  <span data-ttu-id="8698d-488">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-488">Parameter type</span></span> | <span data-ttu-id="8698d-489">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-489">Optional</span></span> | <span data-ttu-id="8698d-490">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-490">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-491">_key</span><span class="sxs-lookup"><span data-stu-id="8698d-491">_key</span></span> | <span data-ttu-id="8698d-492">str</span><span class="sxs-lookup"><span data-stu-id="8698d-492">str</span></span> | <span data-ttu-id="8698d-493">False</span><span class="sxs-lookup"><span data-stu-id="8698d-493">False</span></span> | <span data-ttu-id="8698d-494">コントロール プロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="8698d-494">The name of the control property</span></span>
| <span data-ttu-id="8698d-495">_value</span><span class="sxs-lookup"><span data-stu-id="8698d-495">_value</span></span> | <span data-ttu-id="8698d-496">anytype</span><span class="sxs-lookup"><span data-stu-id="8698d-496">anytype</span></span> | <span data-ttu-id="8698d-497">False</span><span class="sxs-lookup"><span data-stu-id="8698d-497">False</span></span> | <span data-ttu-id="8698d-498">コントロール プロパティの値</span><span class="sxs-lookup"><span data-stu-id="8698d-498">The value of the control property</span></span>

## <a name="class-sysappentityattribute"></a><span data-ttu-id="8698d-499">クラス SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-499">Class SysAppEntityAttribute</span></span>

<span data-ttu-id="8698d-500">データ契約エンティティの修飾に使用される SysAppEntityAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-500">SysAppEntityAttribute used for decorating data contract entities</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-501">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-501">Methods</span></span>

| <span data-ttu-id="8698d-502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-502">Method name</span></span> | <span data-ttu-id="8698d-503">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-503">Returns</span></span> | <span data-ttu-id="8698d-504">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-504">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-505">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-505">new</span></span> | <span data-ttu-id="8698d-506">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-506">void</span></span> | <span data-ttu-id="8698d-507">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8698d-507">Constructor</span></span> |
| <span data-ttu-id="8698d-508">名前</span><span class="sxs-lookup"><span data-stu-id="8698d-508">name</span></span> | <span data-ttu-id="8698d-509">str</span><span class="sxs-lookup"><span data-stu-id="8698d-509">str</span></span> | <span data-ttu-id="8698d-510">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-510">Gets the name of the entity</span></span> |
| <span data-ttu-id="8698d-511">entityKey</span><span class="sxs-lookup"><span data-stu-id="8698d-511">entityKey</span></span> | <span data-ttu-id="8698d-512">str</span><span class="sxs-lookup"><span data-stu-id="8698d-512">str</span></span> | <span data-ttu-id="8698d-513">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-513">Gets the entity key</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-514">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-514">Method new</span></span>

<span data-ttu-id="8698d-515">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8698d-515">Constructor</span></span>

```xpp
public void new (str _name, str _entityKey)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-516">Parameters</span></span>

| <span data-ttu-id="8698d-517">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-517">Parameter name</span></span> |  <span data-ttu-id="8698d-518">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-518">Parameter type</span></span> | <span data-ttu-id="8698d-519">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-519">Optional</span></span> | <span data-ttu-id="8698d-520">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-520">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-521">_name</span><span class="sxs-lookup"><span data-stu-id="8698d-521">_name</span></span> | <span data-ttu-id="8698d-522">str</span><span class="sxs-lookup"><span data-stu-id="8698d-522">str</span></span> | <span data-ttu-id="8698d-523">False</span><span class="sxs-lookup"><span data-stu-id="8698d-523">False</span></span> | <span data-ttu-id="8698d-524">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-524">Entity name</span></span>
| <span data-ttu-id="8698d-525">_entityKey</span><span class="sxs-lookup"><span data-stu-id="8698d-525">_entityKey</span></span> | <span data-ttu-id="8698d-526">str</span><span class="sxs-lookup"><span data-stu-id="8698d-526">str</span></span> | <span data-ttu-id="8698d-527">False</span><span class="sxs-lookup"><span data-stu-id="8698d-527">False</span></span> | <span data-ttu-id="8698d-528">エンティティのキーの名前</span><span class="sxs-lookup"><span data-stu-id="8698d-528">Name of the entity's key</span></span>

### <a name="method-name"></a><span data-ttu-id="8698d-529">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-529">Method name</span></span>

<span data-ttu-id="8698d-530">エンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-530">Gets the name of the entity</span></span>

```xpp
public str name ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-531">Return Value</span></span>

<span data-ttu-id="8698d-532">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="8698d-532">Name of the entity</span></span>

### <a name="method-entitykey"></a><span data-ttu-id="8698d-533">メソッド entityKey</span><span class="sxs-lookup"><span data-stu-id="8698d-533">Method entityKey</span></span>

<span data-ttu-id="8698d-534">エンティティ キーの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-534">Gets the entity key</span></span>

```xpp
public str entityKey ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-535">Return Value</span></span>

<span data-ttu-id="8698d-536">エンティティ キー</span><span class="sxs-lookup"><span data-stu-id="8698d-536">Entity key</span></span>

## <a name="class-sysappentitycontext"></a><span data-ttu-id="8698d-537">クラス SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-537">Class SysAppEntityContext</span></span>

<span data-ttu-id="8698d-538">エンティティ コンテキストを定義するために使用される SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-538">SysAppEntityContext used for defining entity context</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-539">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-539">Methods</span></span>

| <span data-ttu-id="8698d-540">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-540">Method name</span></span> | <span data-ttu-id="8698d-541">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-541">Returns</span></span> | <span data-ttu-id="8698d-542">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-542">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-543">constructFromParams</span><span class="sxs-lookup"><span data-stu-id="8698d-543">constructFromParams</span></span> | <span data-ttu-id="8698d-544">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-544">SysAppEntityContext</span></span> | <span data-ttu-id="8698d-545">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="8698d-545">Constructs SysAppEntityContext from entityName and entityId</span></span> |
| <span data-ttu-id="8698d-546">constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="8698d-546">constructFromBuffer</span></span> | <span data-ttu-id="8698d-547">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-547">SysAppEntityContext</span></span> | <span data-ttu-id="8698d-548">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="8698d-548">Constructs SysAppEntityContext from table buffer</span></span> |
| <span data-ttu-id="8698d-549">entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-549">entityName</span></span> | <span data-ttu-id="8698d-550">str</span><span class="sxs-lookup"><span data-stu-id="8698d-550">str</span></span> | <span data-ttu-id="8698d-551">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-551">Entity name on which filter applies</span></span> |
| <span data-ttu-id="8698d-552">entityId</span><span class="sxs-lookup"><span data-stu-id="8698d-552">entityId</span></span> | <span data-ttu-id="8698d-553">str</span><span class="sxs-lookup"><span data-stu-id="8698d-553">str</span></span> | <span data-ttu-id="8698d-554">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="8698d-554">Field value on which filter applies</span></span> |

### <a name="method-constructfromparams"></a><span data-ttu-id="8698d-555">メソッド constructFromParams</span><span class="sxs-lookup"><span data-stu-id="8698d-555">Method constructFromParams</span></span>

<span data-ttu-id="8698d-556">entityName と entityId から SysAppEntityContext を構築します。</span><span class="sxs-lookup"><span data-stu-id="8698d-556">Constructs SysAppEntityContext from entityName and entityId</span></span>

```xpp
public SysAppEntityContext constructFromParams (str _entityName, str _entityId)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-557">Parameters</span></span>

| <span data-ttu-id="8698d-558">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-558">Parameter name</span></span> |  <span data-ttu-id="8698d-559">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-559">Parameter type</span></span> | <span data-ttu-id="8698d-560">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-560">Optional</span></span> | <span data-ttu-id="8698d-561">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-561">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-562">_entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-562">_entityName</span></span> | <span data-ttu-id="8698d-563">str</span><span class="sxs-lookup"><span data-stu-id="8698d-563">str</span></span> | <span data-ttu-id="8698d-564">False</span><span class="sxs-lookup"><span data-stu-id="8698d-564">False</span></span> | <span data-ttu-id="8698d-565">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-565">Entity name</span></span>
| <span data-ttu-id="8698d-566">_entityId</span><span class="sxs-lookup"><span data-stu-id="8698d-566">_entityId</span></span> | <span data-ttu-id="8698d-567">str</span><span class="sxs-lookup"><span data-stu-id="8698d-567">str</span></span> | <span data-ttu-id="8698d-568">False</span><span class="sxs-lookup"><span data-stu-id="8698d-568">False</span></span> | <span data-ttu-id="8698d-569">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="8698d-569">Entity value</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-570">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-570">Return Value</span></span>

<span data-ttu-id="8698d-571">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="8698d-571">Instance of SysAppEntityContext</span></span>

### <a name="method-constructfrombuffer"></a><span data-ttu-id="8698d-572">メソッド constructFromBuffer</span><span class="sxs-lookup"><span data-stu-id="8698d-572">Method constructFromBuffer</span></span>

<span data-ttu-id="8698d-573">テーブル バッファーから SysAppEntityContext を構築</span><span class="sxs-lookup"><span data-stu-id="8698d-573">Constructs SysAppEntityContext from table buffer</span></span>

```xpp
public SysAppEntityContext constructFromBuffer (Common _tableBuffer)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-574">Parameters</span></span>

| <span data-ttu-id="8698d-575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-575">Parameter name</span></span> |  <span data-ttu-id="8698d-576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-576">Parameter type</span></span> | <span data-ttu-id="8698d-577">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-577">Optional</span></span> | <span data-ttu-id="8698d-578">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-579">_tableBuffer</span><span class="sxs-lookup"><span data-stu-id="8698d-579">_tableBuffer</span></span> | <span data-ttu-id="8698d-580">共通</span><span class="sxs-lookup"><span data-stu-id="8698d-580">Common</span></span> | <span data-ttu-id="8698d-581">False</span><span class="sxs-lookup"><span data-stu-id="8698d-581">False</span></span> | <span data-ttu-id="8698d-582">エンティティを形成するテーブル バッファ</span><span class="sxs-lookup"><span data-stu-id="8698d-582">table buffer forming the entity</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-583">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-583">Return Value</span></span>

<span data-ttu-id="8698d-584">SysAppEntityContext のインスタンス</span><span class="sxs-lookup"><span data-stu-id="8698d-584">Instance of SysAppEntityContext</span></span>

### <a name="method-entityname"></a><span data-ttu-id="8698d-585">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-585">Method entityName</span></span>

<span data-ttu-id="8698d-586">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-586">Entity name on which filter applies</span></span>

```xpp
public str entityName ([str _entityName])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-587">Parameters</span></span>

| <span data-ttu-id="8698d-588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-588">Parameter name</span></span> |  <span data-ttu-id="8698d-589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-589">Parameter type</span></span> | <span data-ttu-id="8698d-590">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-590">Optional</span></span> | <span data-ttu-id="8698d-591">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-592">_entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-592">_entityName</span></span> | <span data-ttu-id="8698d-593">str</span><span class="sxs-lookup"><span data-stu-id="8698d-593">str</span></span> | <span data-ttu-id="8698d-594">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-594">True</span></span> | <span data-ttu-id="8698d-595">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-595">Entity name</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-596">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-596">Return Value</span></span>

<span data-ttu-id="8698d-597">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-597">Entity name</span></span>

### <a name="method-entityid"></a><span data-ttu-id="8698d-598">メソッド entityId</span><span class="sxs-lookup"><span data-stu-id="8698d-598">Method entityId</span></span>

<span data-ttu-id="8698d-599">フィルターを適用するフィールド値</span><span class="sxs-lookup"><span data-stu-id="8698d-599">Field value on which filter applies</span></span>

```xpp
public str entityId ([str _entityId])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-600">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-600">Parameters</span></span>

| <span data-ttu-id="8698d-601">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-601">Parameter name</span></span> |  <span data-ttu-id="8698d-602">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-602">Parameter type</span></span> | <span data-ttu-id="8698d-603">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-603">Optional</span></span> | <span data-ttu-id="8698d-604">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-604">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-605">_entityId</span><span class="sxs-lookup"><span data-stu-id="8698d-605">_entityId</span></span> | <span data-ttu-id="8698d-606">str</span><span class="sxs-lookup"><span data-stu-id="8698d-606">str</span></span> | <span data-ttu-id="8698d-607">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-607">True</span></span> | <span data-ttu-id="8698d-608">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="8698d-608">Entity value</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-609">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-609">Return Value</span></span>

<span data-ttu-id="8698d-610">エンティティの値</span><span class="sxs-lookup"><span data-stu-id="8698d-610">Entity value</span></span>

## <a name="class-sysappfieldattribute"></a><span data-ttu-id="8698d-611">クラス SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-611">Class SysAppFieldAttribute</span></span>

<span data-ttu-id="8698d-612">連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-612">SysAppFieldAttribute used for decorating methods forming bound fields</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-613">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-613">Methods</span></span>

| <span data-ttu-id="8698d-614">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-614">Method name</span></span> | <span data-ttu-id="8698d-615">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-615">Returns</span></span> | <span data-ttu-id="8698d-616">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-616">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-617">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-617">new</span></span> | <span data-ttu-id="8698d-618">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-618">void</span></span> | <span data-ttu-id="8698d-619">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-619">Creates a new instance of SysAppFieldAttribute class</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-620">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-620">Method new</span></span>

<span data-ttu-id="8698d-621">SysAppFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-621">Creates a new instance of SysAppFieldAttribute class</span></span>

```xpp
public void new (str _fieldName, str _label)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-622">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-622">Parameters</span></span>

| <span data-ttu-id="8698d-623">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-623">Parameter name</span></span> |  <span data-ttu-id="8698d-624">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-624">Parameter type</span></span> | <span data-ttu-id="8698d-625">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-625">Optional</span></span> | <span data-ttu-id="8698d-626">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-626">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-627">_fieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-627">_fieldName</span></span> | <span data-ttu-id="8698d-628">str</span><span class="sxs-lookup"><span data-stu-id="8698d-628">str</span></span> | <span data-ttu-id="8698d-629">False</span><span class="sxs-lookup"><span data-stu-id="8698d-629">False</span></span> | <span data-ttu-id="8698d-630">コントロールがバインドされるエンティティ フィールド名</span><span class="sxs-lookup"><span data-stu-id="8698d-630">Entity field name with which control is bound</span></span>
| <span data-ttu-id="8698d-631">_label</span><span class="sxs-lookup"><span data-stu-id="8698d-631">_label</span></span> | <span data-ttu-id="8698d-632">str</span><span class="sxs-lookup"><span data-stu-id="8698d-632">str</span></span> | <span data-ttu-id="8698d-633">False</span><span class="sxs-lookup"><span data-stu-id="8698d-633">False</span></span> | <span data-ttu-id="8698d-634">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="8698d-634">Control label</span></span>

## <a name="class-sysappfieldmultiselecthelper"></a><span data-ttu-id="8698d-635">クラス SysAppFieldMultiSelectHelper</span><span class="sxs-lookup"><span data-stu-id="8698d-635">Class SysAppFieldMultiSelectHelper</span></span>

<span data-ttu-id="8698d-636">D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。</span><span class="sxs-lookup"><span data-stu-id="8698d-636">A helper class to provide helper methods for multi select scenarios used with D365 mobile app</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-637">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-637">Methods</span></span>

| <span data-ttu-id="8698d-638">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-638">Method name</span></span> | <span data-ttu-id="8698d-639">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-639">Returns</span></span> | <span data-ttu-id="8698d-640">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-640">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-641">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-641">new</span></span> | <span data-ttu-id="8698d-642">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-642">void</span></span> | <span data-ttu-id="8698d-643">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-643">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span> |
| <span data-ttu-id="8698d-644">getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="8698d-644">getSelectedRecIds</span></span> | <span data-ttu-id="8698d-645">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8698d-645">container</span></span> | <span data-ttu-id="8698d-646">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-646">Returns a container of recIds of the records that were selected</span></span> |
| <span data-ttu-id="8698d-647">getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="8698d-647">getSelectedValues</span></span> | <span data-ttu-id="8698d-648">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8698d-648">container</span></span> | <span data-ttu-id="8698d-649">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-649">Returns a container of selected values</span></span> |
| <span data-ttu-id="8698d-650">getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="8698d-650">getSelectedRecords</span></span> | <span data-ttu-id="8698d-651">共通</span><span class="sxs-lookup"><span data-stu-id="8698d-651">Common</span></span> | <span data-ttu-id="8698d-652">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-652">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="8698d-653">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="8698d-653">The buffer is marked as temp..</span></span>  <span data-ttu-id="8698d-654">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="8698d-654">Later a while-Select can be used to iterate through all the records</span></span> |
| <span data-ttu-id="8698d-655">setControlValue</span><span class="sxs-lookup"><span data-stu-id="8698d-655">setControlValue</span></span> | <span data-ttu-id="8698d-656">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-656">void</span></span> | <span data-ttu-id="8698d-657">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="8698d-657">A setter to set the multi select control value</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-658">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-658">Method new</span></span>

<span data-ttu-id="8698d-659">SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-659">Creates a new instance of SysAppFieldMultiSelectHelper class</span></span>

```xpp
public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-660">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-660">Parameters</span></span>

| <span data-ttu-id="8698d-661">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-661">Parameter name</span></span> |  <span data-ttu-id="8698d-662">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-662">Parameter type</span></span> | <span data-ttu-id="8698d-663">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-663">Optional</span></span> | <span data-ttu-id="8698d-664">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-664">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-665">_multiSelectTableId</span><span class="sxs-lookup"><span data-stu-id="8698d-665">_multiSelectTableId</span></span> | <span data-ttu-id="8698d-666">TableId</span><span class="sxs-lookup"><span data-stu-id="8698d-666">TableId</span></span> | <span data-ttu-id="8698d-667">False</span><span class="sxs-lookup"><span data-stu-id="8698d-667">False</span></span> | <span data-ttu-id="8698d-668">フィールドのバッキング tableId。</span><span class="sxs-lookup"><span data-stu-id="8698d-668">The backing tableId for the field</span></span>
| <span data-ttu-id="8698d-669">_valueFieldId</span><span class="sxs-lookup"><span data-stu-id="8698d-669">_valueFieldId</span></span> | <span data-ttu-id="8698d-670">FieldId</span><span class="sxs-lookup"><span data-stu-id="8698d-670">FieldId</span></span> | <span data-ttu-id="8698d-671">False</span><span class="sxs-lookup"><span data-stu-id="8698d-671">False</span></span> | <span data-ttu-id="8698d-672">複数選択コントロールに表示されるフィールドの fieldId</span><span class="sxs-lookup"><span data-stu-id="8698d-672">The fieldId for the field which will be shown in the multi select control</span></span>
| <span data-ttu-id="8698d-673">_multiSelectControl</span><span class="sxs-lookup"><span data-stu-id="8698d-673">_multiSelectControl</span></span> | <span data-ttu-id="8698d-674">FormStringControl</span><span class="sxs-lookup"><span data-stu-id="8698d-674">FormStringControl</span></span> | <span data-ttu-id="8698d-675">False</span><span class="sxs-lookup"><span data-stu-id="8698d-675">False</span></span> | <span data-ttu-id="8698d-676">複数選択コントロールになる文字列コントロール</span><span class="sxs-lookup"><span data-stu-id="8698d-676">The string control that will be the multi select control</span></span>

### <a name="method-getselectedrecids"></a><span data-ttu-id="8698d-677">メソッド getSelectedRecIds</span><span class="sxs-lookup"><span data-stu-id="8698d-677">Method getSelectedRecIds</span></span>

<span data-ttu-id="8698d-678">選択されたレコードの recIds のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-678">Returns a container of recIds of the records that were selected</span></span>

```xpp
public container getSelectedRecIds ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-679">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-679">Return Value</span></span>

<span data-ttu-id="8698d-680">選択されたレコードの recOds のコンテナー</span><span class="sxs-lookup"><span data-stu-id="8698d-680">A container of recOds for the records that were selected</span></span>

### <a name="method-getselectedvalues"></a><span data-ttu-id="8698d-681">メソッド getSelectedValues</span><span class="sxs-lookup"><span data-stu-id="8698d-681">Method getSelectedValues</span></span>

<span data-ttu-id="8698d-682">選択した値のコンテナーを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-682">Returns a container of selected values</span></span>

```xpp
public container getSelectedValues ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-683">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-683">Return Value</span></span>

<span data-ttu-id="8698d-684">選択した値のコンテナー</span><span class="sxs-lookup"><span data-stu-id="8698d-684">A container of selected values</span></span>

### <a name="method-getselectedrecords"></a><span data-ttu-id="8698d-685">メソッド getSelectedRecords</span><span class="sxs-lookup"><span data-stu-id="8698d-685">Method getSelectedRecords</span></span>

<span data-ttu-id="8698d-686">選択したすべてのレコードを含むバッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-686">Returns a buffer that contain all the selected records..</span></span>  <span data-ttu-id="8698d-687">バッファが temp. としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="8698d-687">The buffer is marked as temp..</span></span>  <span data-ttu-id="8698d-688">後で、while-Select はすべてのレコードを反復処理するために使用できます</span><span class="sxs-lookup"><span data-stu-id="8698d-688">Later a while-Select can be used to iterate through all the records</span></span>

```xpp
public Common getSelectedRecords ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-689">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-689">Return Value</span></span>

<span data-ttu-id="8698d-690">選択したすべてのレコードを含むバッファー</span><span class="sxs-lookup"><span data-stu-id="8698d-690">A buffer containing all the selected records</span></span>

### <a name="method-setcontrolvalue"></a><span data-ttu-id="8698d-691">メソッド setControlValue</span><span class="sxs-lookup"><span data-stu-id="8698d-691">Method setControlValue</span></span>

<span data-ttu-id="8698d-692">複数選択コントロール値を設定するセッター</span><span class="sxs-lookup"><span data-stu-id="8698d-692">A setter to set the multi select control value</span></span>

```xpp
public void setControlValue (str _value)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-693">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-693">Parameters</span></span>

| <span data-ttu-id="8698d-694">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-694">Parameter name</span></span> |  <span data-ttu-id="8698d-695">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-695">Parameter type</span></span> | <span data-ttu-id="8698d-696">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-696">Optional</span></span> | <span data-ttu-id="8698d-697">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-697">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-698">_value</span><span class="sxs-lookup"><span data-stu-id="8698d-698">_value</span></span> | <span data-ttu-id="8698d-699">str</span><span class="sxs-lookup"><span data-stu-id="8698d-699">str</span></span> | <span data-ttu-id="8698d-700">False</span><span class="sxs-lookup"><span data-stu-id="8698d-700">False</span></span> | <span data-ttu-id="8698d-701">SysAppFieldMultiSelectHelper によって使用されるコロン区切り値</span><span class="sxs-lookup"><span data-stu-id="8698d-701">A colon separated value that will be used by SysAppFieldMultiSelectHelper</span></span>

## <a name="class-sysappfiltercontext"></a><span data-ttu-id="8698d-702">クラス SysAppFilterContext</span><span class="sxs-lookup"><span data-stu-id="8698d-702">Class SysAppFilterContext</span></span>

<span data-ttu-id="8698d-703">コンテキスト値を保持している SysAppFilterContext クラス</span><span class="sxs-lookup"><span data-stu-id="8698d-703">SysAppFilterContext class which holds context values</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-704">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-704">Methods</span></span>

| <span data-ttu-id="8698d-705">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-705">Method name</span></span> | <span data-ttu-id="8698d-706">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-706">Returns</span></span> | <span data-ttu-id="8698d-707">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-707">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-708">entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-708">entityName</span></span> | <span data-ttu-id="8698d-709">str</span><span class="sxs-lookup"><span data-stu-id="8698d-709">str</span></span> | <span data-ttu-id="8698d-710">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-710">Entity name on which filter applies</span></span> |
| <span data-ttu-id="8698d-711">filterFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-711">filterFieldName</span></span> | <span data-ttu-id="8698d-712">str</span><span class="sxs-lookup"><span data-stu-id="8698d-712">str</span></span> | <span data-ttu-id="8698d-713">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="8698d-713">Field name on which filter applies</span></span> |
| <span data-ttu-id="8698d-714">filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="8698d-714">filterFieldValueList</span></span> | <span data-ttu-id="8698d-715">リスト</span><span class="sxs-lookup"><span data-stu-id="8698d-715">List</span></span> | <span data-ttu-id="8698d-716">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-716">Gets the list of filter field values based on which filter happens</span></span> |
| <span data-ttu-id="8698d-717">演算子</span><span class="sxs-lookup"><span data-stu-id="8698d-717">operator</span></span> | <span data-ttu-id="8698d-718">str</span><span class="sxs-lookup"><span data-stu-id="8698d-718">str</span></span> | <span data-ttu-id="8698d-719">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="8698d-719">Operator based on which result will be fetched</span></span> |
| <span data-ttu-id="8698d-720">addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="8698d-720">addFilterFieldValue</span></span> | <span data-ttu-id="8698d-721">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-721">void</span></span> | <span data-ttu-id="8698d-722">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="8698d-722">Adds filter field value</span></span> |

### <a name="method-entityname"></a><span data-ttu-id="8698d-723">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-723">Method entityName</span></span>

<span data-ttu-id="8698d-724">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-724">Entity name on which filter applies</span></span>

```xpp
public str entityName ([str _entityName])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-725">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-725">Parameters</span></span>

| <span data-ttu-id="8698d-726">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-726">Parameter name</span></span> |  <span data-ttu-id="8698d-727">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-727">Parameter type</span></span> | <span data-ttu-id="8698d-728">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-728">Optional</span></span> | <span data-ttu-id="8698d-729">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-729">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-730">_entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-730">_entityName</span></span> | <span data-ttu-id="8698d-731">str</span><span class="sxs-lookup"><span data-stu-id="8698d-731">str</span></span> | <span data-ttu-id="8698d-732">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-732">True</span></span> | <span data-ttu-id="8698d-733">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-733">Entity name on which filter applies</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-734">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-734">Return Value</span></span>

<span data-ttu-id="8698d-735">フィルターを適用するエンティティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-735">Entity name on which filter applies</span></span>

### <a name="method-filterfieldname"></a><span data-ttu-id="8698d-736">メソッド filterFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-736">Method filterFieldName</span></span>

<span data-ttu-id="8698d-737">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="8698d-737">Field name on which filter applies</span></span>

```xpp
public str filterFieldName ([str _filterFieldName])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-738">Parameters</span></span>

| <span data-ttu-id="8698d-739">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-739">Parameter name</span></span> |  <span data-ttu-id="8698d-740">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-740">Parameter type</span></span> | <span data-ttu-id="8698d-741">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-741">Optional</span></span> | <span data-ttu-id="8698d-742">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-742">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-743">_filterFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-743">_filterFieldName</span></span> | <span data-ttu-id="8698d-744">str</span><span class="sxs-lookup"><span data-stu-id="8698d-744">str</span></span> | <span data-ttu-id="8698d-745">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-745">True</span></span> | <span data-ttu-id="8698d-746">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="8698d-746">Field name on which filter applies</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-747">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-747">Return Value</span></span>

<span data-ttu-id="8698d-748">フィルターを適用するフィールド名</span><span class="sxs-lookup"><span data-stu-id="8698d-748">Field name on which filter applies</span></span>

### <a name="method-filterfieldvaluelist"></a><span data-ttu-id="8698d-749">メソッド filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="8698d-749">Method filterFieldValueList</span></span>

<span data-ttu-id="8698d-750">フィルター処理動作に基づくフィルターの一覧フィールド値の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-750">Gets the list of filter field values based on which filter happens</span></span>

```xpp
public List filterFieldValueList ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-751">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-751">Return Value</span></span>

<span data-ttu-id="8698d-752">フィルター処理動作に基づくフィルターの一覧フィールド値</span><span class="sxs-lookup"><span data-stu-id="8698d-752">List of filter field values based on which filter happens</span></span>

### <a name="method-operator"></a><span data-ttu-id="8698d-753">メソッド operator</span><span class="sxs-lookup"><span data-stu-id="8698d-753">Method operator</span></span>

<span data-ttu-id="8698d-754">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="8698d-754">Operator based on which result will be fetched</span></span>

```xpp
public str operator ([str _operator])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-755">Parameters</span></span>

| <span data-ttu-id="8698d-756">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-756">Parameter name</span></span> |  <span data-ttu-id="8698d-757">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-757">Parameter type</span></span> | <span data-ttu-id="8698d-758">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-758">Optional</span></span> | <span data-ttu-id="8698d-759">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-759">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-760">_operator</span><span class="sxs-lookup"><span data-stu-id="8698d-760">_operator</span></span> | <span data-ttu-id="8698d-761">str</span><span class="sxs-lookup"><span data-stu-id="8698d-761">str</span></span> | <span data-ttu-id="8698d-762">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-762">True</span></span> | <span data-ttu-id="8698d-763">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="8698d-763">Operator based on which result will be fetched</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-764">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-764">Return Value</span></span>

<span data-ttu-id="8698d-765">結果のフェッチに使用される演算子</span><span class="sxs-lookup"><span data-stu-id="8698d-765">Operator based on which result will be fetched</span></span>

### <a name="method-addfilterfieldvalue"></a><span data-ttu-id="8698d-766">メソッド addFilterFieldValue</span><span class="sxs-lookup"><span data-stu-id="8698d-766">Method addFilterFieldValue</span></span>

<span data-ttu-id="8698d-767">フィルター フィールド値の追加</span><span class="sxs-lookup"><span data-stu-id="8698d-767">Adds filter field value</span></span>

```xpp
public void addFilterFieldValue ( _filterFieldValueList)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-768">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-768">Parameters</span></span>

| <span data-ttu-id="8698d-769">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-769">Parameter name</span></span> |  <span data-ttu-id="8698d-770">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-770">Parameter type</span></span> | <span data-ttu-id="8698d-771">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-771">Optional</span></span> | <span data-ttu-id="8698d-772">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-772">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-773">_filterFieldValueList</span><span class="sxs-lookup"><span data-stu-id="8698d-773">_filterFieldValueList</span></span> |  | <span data-ttu-id="8698d-774">False</span><span class="sxs-lookup"><span data-stu-id="8698d-774">False</span></span> | <span data-ttu-id="8698d-775">フィルター処理動作に基づくフィルター フィールド値</span><span class="sxs-lookup"><span data-stu-id="8698d-775">Filter field values based on which filter happens</span></span>

## <a name="class-sysapplookupattribute"></a><span data-ttu-id="8698d-776">クラス SysAppLookUpAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-776">Class SysAppLookUpAttribute</span></span>

<span data-ttu-id="8698d-777">ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-777">SysAppPageAttribute used for decorating pages that is also lookup page</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-778">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-778">Methods</span></span>

| <span data-ttu-id="8698d-779">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-779">Method name</span></span> | <span data-ttu-id="8698d-780">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-780">Returns</span></span> | <span data-ttu-id="8698d-781">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-781">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-782">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-782">new</span></span> | <span data-ttu-id="8698d-783">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-783">void</span></span> | <span data-ttu-id="8698d-784">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-784">Creates a new instance of SysAppLookUpAttribute class</span></span> |
| <span data-ttu-id="8698d-785">displayFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-785">displayFieldName</span></span> | <span data-ttu-id="8698d-786">str</span><span class="sxs-lookup"><span data-stu-id="8698d-786">str</span></span> | <span data-ttu-id="8698d-787">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="8698d-787">Gets the display field name of lookup control</span></span> |
| <span data-ttu-id="8698d-788">valueFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-788">valueFieldName</span></span> | <span data-ttu-id="8698d-789">str</span><span class="sxs-lookup"><span data-stu-id="8698d-789">str</span></span> | <span data-ttu-id="8698d-790">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-790">Gets the value field name of lookup control</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-791">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-791">Method new</span></span>

<span data-ttu-id="8698d-792">SysAppLookUpAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-792">Creates a new instance of SysAppLookUpAttribute class</span></span>

```xpp
public void new (str _displayFieldName, str _valueFieldName)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-793">Parameters</span></span>

| <span data-ttu-id="8698d-794">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-794">Parameter name</span></span> |  <span data-ttu-id="8698d-795">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-795">Parameter type</span></span> | <span data-ttu-id="8698d-796">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-796">Optional</span></span> | <span data-ttu-id="8698d-797">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-797">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-798">_displayFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-798">_displayFieldName</span></span> | <span data-ttu-id="8698d-799">str</span><span class="sxs-lookup"><span data-stu-id="8698d-799">str</span></span> | <span data-ttu-id="8698d-800">False</span><span class="sxs-lookup"><span data-stu-id="8698d-800">False</span></span> | <span data-ttu-id="8698d-801">ルックアップ表示フィールド。</span><span class="sxs-lookup"><span data-stu-id="8698d-801">Lookup display field.</span></span> <span data-ttu-id="8698d-802">ルックアップ ページの任意のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="8698d-802">Name of any control of lookup page</span></span>
| <span data-ttu-id="8698d-803">_valueFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-803">_valueFieldName</span></span> | <span data-ttu-id="8698d-804">str</span><span class="sxs-lookup"><span data-stu-id="8698d-804">str</span></span> | <span data-ttu-id="8698d-805">False</span><span class="sxs-lookup"><span data-stu-id="8698d-805">False</span></span> | <span data-ttu-id="8698d-806">ルックアップの値フィールド。</span><span class="sxs-lookup"><span data-stu-id="8698d-806">Lookup value field.</span></span> <span data-ttu-id="8698d-807">ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="8698d-807">Name of control formed by root data contract constructing lookup page</span></span>

### <a name="method-displayfieldname"></a><span data-ttu-id="8698d-808">メソッド displayFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-808">Method displayFieldName</span></span>

<span data-ttu-id="8698d-809">ルックアップ コントロールの表示フィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="8698d-809">Gets the display field name of lookup control</span></span>

```xpp
public str displayFieldName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-810">Return Value</span></span>

<span data-ttu-id="8698d-811">ルックアップ コントロールの表示フィールド名</span><span class="sxs-lookup"><span data-stu-id="8698d-811">The display field name of lookup control</span></span>

### <a name="method-valuefieldname"></a><span data-ttu-id="8698d-812">メソッド valueFieldName</span><span class="sxs-lookup"><span data-stu-id="8698d-812">Method valueFieldName</span></span>

<span data-ttu-id="8698d-813">ルックアップ コントロールのフィールド名の値の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-813">Gets the value field name of lookup control</span></span>

```xpp
public str valueFieldName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-814">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-814">Return Value</span></span>

<span data-ttu-id="8698d-815">ルックアップ コントロールのフィールド名値</span><span class="sxs-lookup"><span data-stu-id="8698d-815">The value field name of lookup control</span></span>

## <a name="class-sysapplookupfieldattribute"></a><span data-ttu-id="8698d-816">クラス SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-816">Class SysAppLookupFieldAttribute</span></span>

<span data-ttu-id="8698d-817">アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-817">SysAppLookupFieldAttribute used for decorating look up fields of action</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-818">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-818">Methods</span></span>

| <span data-ttu-id="8698d-819">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-819">Method name</span></span> | <span data-ttu-id="8698d-820">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-820">Returns</span></span> | <span data-ttu-id="8698d-821">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-821">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-822">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-822">new</span></span> | <span data-ttu-id="8698d-823">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-823">void</span></span> | <span data-ttu-id="8698d-824">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-824">Creates a new instance of SysAppLookupFieldAttribute class</span></span> |
| <span data-ttu-id="8698d-825">entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-825">entityName</span></span> | <span data-ttu-id="8698d-826">str</span><span class="sxs-lookup"><span data-stu-id="8698d-826">str</span></span> | <span data-ttu-id="8698d-827">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-827">Gets the name of the entity with which lookup page is related</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-828">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-828">Method new</span></span>

<span data-ttu-id="8698d-829">SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-829">Creates a new instance of SysAppLookupFieldAttribute class</span></span>

```xpp
public void new ( _name)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-830">Parameters</span></span>

| <span data-ttu-id="8698d-831">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-831">Parameter name</span></span> |  <span data-ttu-id="8698d-832">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-832">Parameter type</span></span> | <span data-ttu-id="8698d-833">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-833">Optional</span></span> | <span data-ttu-id="8698d-834">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-834">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-835">_name</span><span class="sxs-lookup"><span data-stu-id="8698d-835">_name</span></span> |  | <span data-ttu-id="8698d-836">False</span><span class="sxs-lookup"><span data-stu-id="8698d-836">False</span></span> | <span data-ttu-id="8698d-837">ルックアップ ページが関連するエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="8698d-837">Name of the entity with which lookup page is related</span></span>

### <a name="method-entityname"></a><span data-ttu-id="8698d-838">メソッド entityName</span><span class="sxs-lookup"><span data-stu-id="8698d-838">Method entityName</span></span>

<span data-ttu-id="8698d-839">ルックアップ ページが関連するエンティティの名前の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-839">Gets the name of the entity with which lookup page is related</span></span>

```xpp
public str entityName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-840">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-840">Return Value</span></span>

<span data-ttu-id="8698d-841">エンティティの名前</span><span class="sxs-lookup"><span data-stu-id="8698d-841">Name of the entity</span></span>

## <a name="class-sysapppageattribute"></a><span data-ttu-id="8698d-842">クラス SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-842">Class SysAppPageAttribute</span></span>

<span data-ttu-id="8698d-843">ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-843">SysAppPageAttribute used for decorating methods defining page of workspace</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-844">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-844">Methods</span></span>

| <span data-ttu-id="8698d-845">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-845">Method name</span></span> | <span data-ttu-id="8698d-846">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-846">Returns</span></span> | <span data-ttu-id="8698d-847">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-847">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-848">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-848">new</span></span> | <span data-ttu-id="8698d-849">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-849">void</span></span> | <span data-ttu-id="8698d-850">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-850">Creates a new instance of SysAppPageAttribute class</span></span> |
| <span data-ttu-id="8698d-851">pageTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-851">pageTitle</span></span> | <span data-ttu-id="8698d-852">str</span><span class="sxs-lookup"><span data-stu-id="8698d-852">str</span></span> | <span data-ttu-id="8698d-853">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-853">Gets the Page Title of the page</span></span> |
| <span data-ttu-id="8698d-854">pageDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-854">pageDescription</span></span> | <span data-ttu-id="8698d-855">str</span><span class="sxs-lookup"><span data-stu-id="8698d-855">str</span></span> | <span data-ttu-id="8698d-856">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-856">Gets the Page Description</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-857">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-857">Method new</span></span>

<span data-ttu-id="8698d-858">SysAppPageAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-858">Creates a new instance of SysAppPageAttribute class</span></span>

```xpp
public void new ([str _pageTitle], [str _pageDescription])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-859">Parameters</span></span>

| <span data-ttu-id="8698d-860">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-860">Parameter name</span></span> |  <span data-ttu-id="8698d-861">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-861">Parameter type</span></span> | <span data-ttu-id="8698d-862">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-862">Optional</span></span> | <span data-ttu-id="8698d-863">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-863">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-864">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-864">_pageTitle</span></span> | <span data-ttu-id="8698d-865">str</span><span class="sxs-lookup"><span data-stu-id="8698d-865">str</span></span> | <span data-ttu-id="8698d-866">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-866">True</span></span> | <span data-ttu-id="8698d-867">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-867">The page title</span></span>
| <span data-ttu-id="8698d-868">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-868">_pageDescription</span></span> | <span data-ttu-id="8698d-869">str</span><span class="sxs-lookup"><span data-stu-id="8698d-869">str</span></span> | <span data-ttu-id="8698d-870">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-870">True</span></span> | <span data-ttu-id="8698d-871">ページの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-871">The page description</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="8698d-872">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-872">Method pageTitle</span></span>

<span data-ttu-id="8698d-873">ページのページのタイトルの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-873">Gets the Page Title of the page</span></span>

```xpp
public str pageTitle ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-874">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-874">Return Value</span></span>

<span data-ttu-id="8698d-875">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-875">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="8698d-876">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-876">Method pageDescription</span></span>

<span data-ttu-id="8698d-877">ページの説明の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-877">Gets the Page Description</span></span>

```xpp
public str pageDescription ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-878">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-878">Return Value</span></span>

<span data-ttu-id="8698d-879">ページの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-879">The page description</span></span>

## <a name="class-sysapppagemetadata"></a><span data-ttu-id="8698d-880">クラス SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-880">Class SysAppPageMetadata</span></span>

<span data-ttu-id="8698d-881">このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="8698d-881">This class can be used to access and update AX mobile workspace page metadata</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-882">方法</span><span class="sxs-lookup"><span data-stu-id="8698d-882">Methods</span></span>

| <span data-ttu-id="8698d-883">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-883">Method name</span></span> | <span data-ttu-id="8698d-884">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-884">Returns</span></span> | <span data-ttu-id="8698d-885">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-885">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-886">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-886">new</span></span> | <span data-ttu-id="8698d-887">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-887">void</span></span> |  |
| <span data-ttu-id="8698d-888">getPageName</span><span class="sxs-lookup"><span data-stu-id="8698d-888">getPageName</span></span> | <span data-ttu-id="8698d-889">str</span><span class="sxs-lookup"><span data-stu-id="8698d-889">str</span></span> | <span data-ttu-id="8698d-890">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-890">Returns the page name</span></span> |
| <span data-ttu-id="8698d-891">pageTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-891">pageTitle</span></span> | <span data-ttu-id="8698d-892">str</span><span class="sxs-lookup"><span data-stu-id="8698d-892">str</span></span> | <span data-ttu-id="8698d-893">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-893">Gets and sets the page title</span></span> |
| <span data-ttu-id="8698d-894">pageDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-894">pageDescription</span></span> | <span data-ttu-id="8698d-895">str</span><span class="sxs-lookup"><span data-stu-id="8698d-895">str</span></span> | <span data-ttu-id="8698d-896">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-896">Gets or sets the page description</span></span> |
| <span data-ttu-id="8698d-897">pageHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-897">pageHidden</span></span> | <span data-ttu-id="8698d-898">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-898">boolean</span></span> | <span data-ttu-id="8698d-899">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-899">Gets and sets whether the page is hidden in the workspace</span></span> |
| <span data-ttu-id="8698d-900">pageOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-900">pageOrder</span></span> | <span data-ttu-id="8698d-901">int</span><span class="sxs-lookup"><span data-stu-id="8698d-901">int</span></span> | <span data-ttu-id="8698d-902">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-902">Gets or sets the page order</span></span> |
| <span data-ttu-id="8698d-903">getControl</span><span class="sxs-lookup"><span data-stu-id="8698d-903">getControl</span></span> | <span data-ttu-id="8698d-904">SysAppControlMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-904">SysAppControlMetadata</span></span> | <span data-ttu-id="8698d-905">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-905">Returns the control on the current page having the provided control name</span></span> |
| <span data-ttu-id="8698d-906">getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-906">getControlEnumerator</span></span> | <span data-ttu-id="8698d-907">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-907">MapEnumerator</span></span> | <span data-ttu-id="8698d-908">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-908">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="8698d-909">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-909">Where Key is control name and value is of type SysAppControlMetadata</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-910">Method new</span></span>

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-911">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-911">Parameters</span></span>

| <span data-ttu-id="8698d-912">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-912">Parameter name</span></span> |  <span data-ttu-id="8698d-913">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-913">Parameter type</span></span> | <span data-ttu-id="8698d-914">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-914">Optional</span></span> | <span data-ttu-id="8698d-915">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-915">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-916">_pageMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-916">_pageMetadata</span></span> | <span data-ttu-id="8698d-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-917">Microsoft.Dynamics.Client.ServerForm.App.PageMetadata</span></span> | <span data-ttu-id="8698d-918">False</span><span class="sxs-lookup"><span data-stu-id="8698d-918">False</span></span> |

### <a name="method-getpagename"></a><span data-ttu-id="8698d-919">メソッド getPageName</span><span class="sxs-lookup"><span data-stu-id="8698d-919">Method getPageName</span></span>

<span data-ttu-id="8698d-920">ページ名を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-920">Returns the page name</span></span>

```xpp
public str getPageName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-921">Return Value</span></span>

<span data-ttu-id="8698d-922">ページ名</span><span class="sxs-lookup"><span data-stu-id="8698d-922">The page name</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="8698d-923">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-923">Method pageTitle</span></span>

<span data-ttu-id="8698d-924">ページ タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-924">Gets and sets the page title</span></span>

```xpp
public str pageTitle ([str _pageTitle])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-925">Parameters</span></span>

| <span data-ttu-id="8698d-926">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-926">Parameter name</span></span> |  <span data-ttu-id="8698d-927">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-927">Parameter type</span></span> | <span data-ttu-id="8698d-928">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-928">Optional</span></span> | <span data-ttu-id="8698d-929">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-929">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-930">_pageTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-930">_pageTitle</span></span> | <span data-ttu-id="8698d-931">str</span><span class="sxs-lookup"><span data-stu-id="8698d-931">str</span></span> | <span data-ttu-id="8698d-932">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-932">True</span></span> | <span data-ttu-id="8698d-933">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-933">The page title</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-934">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-934">Return Value</span></span>

<span data-ttu-id="8698d-935">ページ タイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-935">The page title</span></span>

### <a name="method-pagedescription"></a><span data-ttu-id="8698d-936">メソッド pageDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-936">Method pageDescription</span></span>

<span data-ttu-id="8698d-937">ページの説明の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-937">Gets or sets the page description</span></span>

```xpp
public str pageDescription ([str _pageDescription])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-938">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-938">Parameters</span></span>

| <span data-ttu-id="8698d-939">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-939">Parameter name</span></span> |  <span data-ttu-id="8698d-940">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-940">Parameter type</span></span> | <span data-ttu-id="8698d-941">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-941">Optional</span></span> | <span data-ttu-id="8698d-942">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-942">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-943">_pageDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-943">_pageDescription</span></span> | <span data-ttu-id="8698d-944">str</span><span class="sxs-lookup"><span data-stu-id="8698d-944">str</span></span> | <span data-ttu-id="8698d-945">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-945">True</span></span> | <span data-ttu-id="8698d-946">ページの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-946">The page description</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-947">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-947">Return Value</span></span>

<span data-ttu-id="8698d-948">ページの説明></span><span class="sxs-lookup"><span data-stu-id="8698d-948">The page description></span></span>

### <a name="method-pagehidden"></a><span data-ttu-id="8698d-949">メソッド pageHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-949">Method pageHidden</span></span>

<span data-ttu-id="8698d-950">ワークスペースでページを表示にするかどうかの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-950">Gets and sets whether the page is hidden in the workspace</span></span>

```xpp
public boolean pageHidden ([boolean _pageHidden])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-951">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-951">Parameters</span></span>

| <span data-ttu-id="8698d-952">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-952">Parameter name</span></span> |  <span data-ttu-id="8698d-953">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-953">Parameter type</span></span> | <span data-ttu-id="8698d-954">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-954">Optional</span></span> | <span data-ttu-id="8698d-955">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-955">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-956">_pageHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-956">_pageHidden</span></span> | <span data-ttu-id="8698d-957">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-957">boolean</span></span> | <span data-ttu-id="8698d-958">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-958">True</span></span> | <span data-ttu-id="8698d-959">ページの非表示の値</span><span class="sxs-lookup"><span data-stu-id="8698d-959">page hidden value</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-960">Return Value</span></span>

<span data-ttu-id="8698d-961">ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。</span><span class="sxs-lookup"><span data-stu-id="8698d-961">True if the current page is hidden in workspace; otherwise false</span></span>

### <a name="method-pageorder"></a><span data-ttu-id="8698d-962">メソッド pageOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-962">Method pageOrder</span></span>

<span data-ttu-id="8698d-963">ページ順序の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-963">Gets or sets the page order</span></span>

```xpp
public int pageOrder ([int _pageOrder])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-964">Parameters</span></span>

| <span data-ttu-id="8698d-965">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-965">Parameter name</span></span> |  <span data-ttu-id="8698d-966">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-966">Parameter type</span></span> | <span data-ttu-id="8698d-967">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-967">Optional</span></span> | <span data-ttu-id="8698d-968">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-968">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-969">_pageOrder</span><span class="sxs-lookup"><span data-stu-id="8698d-969">_pageOrder</span></span> | <span data-ttu-id="8698d-970">int</span><span class="sxs-lookup"><span data-stu-id="8698d-970">int</span></span> | <span data-ttu-id="8698d-971">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-971">True</span></span> | <span data-ttu-id="8698d-972">ページの順序</span><span class="sxs-lookup"><span data-stu-id="8698d-972">The page order</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-973">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-973">Return Value</span></span>

<span data-ttu-id="8698d-974">ページの順序</span><span class="sxs-lookup"><span data-stu-id="8698d-974">The page order</span></span>

### <a name="method-getcontrol"></a><span data-ttu-id="8698d-975">メソッド getControl</span><span class="sxs-lookup"><span data-stu-id="8698d-975">Method getControl</span></span>

<span data-ttu-id="8698d-976">指定されたコントロールの名前を持つ現在のページのコントロールを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-976">Returns the control on the current page having the provided control name</span></span>

```xpp
public SysAppControlMetadata getControl (str _controlName)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-977">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-977">Parameters</span></span>

| <span data-ttu-id="8698d-978">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-978">Parameter name</span></span> |  <span data-ttu-id="8698d-979">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-979">Parameter type</span></span> | <span data-ttu-id="8698d-980">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-980">Optional</span></span> | <span data-ttu-id="8698d-981">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-981">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-982">_controlName</span><span class="sxs-lookup"><span data-stu-id="8698d-982">_controlName</span></span> | <span data-ttu-id="8698d-983">str</span><span class="sxs-lookup"><span data-stu-id="8698d-983">str</span></span> | <span data-ttu-id="8698d-984">False</span><span class="sxs-lookup"><span data-stu-id="8698d-984">False</span></span> | <span data-ttu-id="8698d-985">コントロールを検索するために使用されるコントロール名</span><span class="sxs-lookup"><span data-stu-id="8698d-985">The control name that will be used to search for control</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-986">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-986">Return Value</span></span>

<span data-ttu-id="8698d-987">指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null</span><span class="sxs-lookup"><span data-stu-id="8698d-987">An object of SysAppControlMetadata is returned if a control with the provided control name exist on the page; otherwise null</span></span>

### <a name="method-getcontrolenumerator"></a><span data-ttu-id="8698d-988">メソッド getControlEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-988">Method getControlEnumerator</span></span>

<span data-ttu-id="8698d-989">ページ コントロールを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-989">Returns a map enumerator that can be used to enumerate page controls.</span></span>  <span data-ttu-id="8698d-990">ここで、Key はコントロール名で、値は SysAppControlMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-990">Where Key is control name and value is of type SysAppControlMetadata</span></span>

```xpp
public MapEnumerator getControlEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-991">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-991">Return Value</span></span>

<span data-ttu-id="8698d-992">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="8698d-992">A map enumerator</span></span>

## <a name="class-sysappprojectionattribute"></a><span data-ttu-id="8698d-993">クラス SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-993">Class SysAppProjectionAttribute</span></span>

<span data-ttu-id="8698d-994">非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-994">SysAppProjectionAttribute used for decorating methods forming unbound fields</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-995">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-995">Methods</span></span>

| <span data-ttu-id="8698d-996">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-996">Method name</span></span> | <span data-ttu-id="8698d-997">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-997">Returns</span></span> | <span data-ttu-id="8698d-998">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-998">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-999">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-999">new</span></span> | <span data-ttu-id="8698d-1000">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1000">void</span></span> | <span data-ttu-id="8698d-1001">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-1001">Creates a new instance of SysAppControlMetadataAttributes class</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1002">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1002">Method new</span></span>

<span data-ttu-id="8698d-1003">SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-1003">Creates a new instance of SysAppControlMetadataAttributes class</span></span>

```xpp
public void new (str _label)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1004">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1004">Parameters</span></span>

| <span data-ttu-id="8698d-1005">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1005">Parameter name</span></span> |  <span data-ttu-id="8698d-1006">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1006">Parameter type</span></span> | <span data-ttu-id="8698d-1007">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1007">Optional</span></span> | <span data-ttu-id="8698d-1008">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1008">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1009">_label</span><span class="sxs-lookup"><span data-stu-id="8698d-1009">_label</span></span> | <span data-ttu-id="8698d-1010">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1010">str</span></span> | <span data-ttu-id="8698d-1011">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1011">False</span></span> | <span data-ttu-id="8698d-1012">コントロール ラベル</span><span class="sxs-lookup"><span data-stu-id="8698d-1012">Control label</span></span>

## <a name="class-sysapprelationalattribute"></a><span data-ttu-id="8698d-1013">クラス SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-1013">Class SysAppRelationalAttribute</span></span>

<span data-ttu-id="8698d-1014">参照コントロールの修飾に使用される SysAppRelationalAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-1014">SysAppRelationalAttribute used for decorating reference controls</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1015">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-1015">Methods</span></span>

| <span data-ttu-id="8698d-1016">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1016">Method name</span></span> | <span data-ttu-id="8698d-1017">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1017">Returns</span></span> | <span data-ttu-id="8698d-1018">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1018">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1019">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-1019">new</span></span> | <span data-ttu-id="8698d-1020">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1020">void</span></span> | <span data-ttu-id="8698d-1021">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8698d-1021">Constructor</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1022">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1022">Method new</span></span>

<span data-ttu-id="8698d-1023">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8698d-1023">Constructor</span></span>

```xpp
public void new ([str _name])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1024">Parameters</span></span>

| <span data-ttu-id="8698d-1025">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1025">Parameter name</span></span> |  <span data-ttu-id="8698d-1026">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1026">Parameter type</span></span> | <span data-ttu-id="8698d-1027">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1027">Optional</span></span> | <span data-ttu-id="8698d-1028">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1028">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1029">_name</span><span class="sxs-lookup"><span data-stu-id="8698d-1029">_name</span></span> | <span data-ttu-id="8698d-1030">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1030">str</span></span> | <span data-ttu-id="8698d-1031">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1031">True</span></span> | <span data-ttu-id="8698d-1032">参照されるエンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="8698d-1032">Property name of the referenced entity</span></span>

## <a name="class-sysapprequestparams"></a><span data-ttu-id="8698d-1033">クラス SysAppRequestParams</span><span class="sxs-lookup"><span data-stu-id="8698d-1033">Class SysAppRequestParams</span></span>

<span data-ttu-id="8698d-1034">詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1034">Request class for X++ methods generating details and action pages</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1035">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-1035">Methods</span></span>

| <span data-ttu-id="8698d-1036">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1036">Method name</span></span> | <span data-ttu-id="8698d-1037">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1037">Returns</span></span> | <span data-ttu-id="8698d-1038">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1038">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1039">entityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1039">entityContext</span></span> | <span data-ttu-id="8698d-1040">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1040">SysAppEntityContext</span></span> | <span data-ttu-id="8698d-1041">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1041">Entity context of the request</span></span> |
| <span data-ttu-id="8698d-1042">filterContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1042">filterContext</span></span> | <span data-ttu-id="8698d-1043">リスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1043">List</span></span> | <span data-ttu-id="8698d-1044">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1044">List of SysAppFilterContext for filter contexts</span></span> |

### <a name="method-entitycontext"></a><span data-ttu-id="8698d-1045">メソッド entityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1045">Method entityContext</span></span>

<span data-ttu-id="8698d-1046">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1046">Entity context of the request</span></span>

```xpp
public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1047">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1047">Parameters</span></span>

| <span data-ttu-id="8698d-1048">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1048">Parameter name</span></span> |  <span data-ttu-id="8698d-1049">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1049">Parameter type</span></span> | <span data-ttu-id="8698d-1050">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1050">Optional</span></span> | <span data-ttu-id="8698d-1051">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1051">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1052">_entityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1052">_entityContext</span></span> | <span data-ttu-id="8698d-1053">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1053">SysAppEntityContext</span></span> | <span data-ttu-id="8698d-1054">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1054">True</span></span> | <span data-ttu-id="8698d-1055">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1055">Entity context of the request</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1056">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1056">Return Value</span></span>

<span data-ttu-id="8698d-1057">要求のエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1057">Entity context of the request</span></span>

### <a name="method-filtercontext"></a><span data-ttu-id="8698d-1058">メソッド filterContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1058">Method filterContext</span></span>

<span data-ttu-id="8698d-1059">フィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1059">List of SysAppFilterContext for filter contexts</span></span>

```xpp
public List filterContext ([List _filterContext])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1060">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1060">Parameters</span></span>

| <span data-ttu-id="8698d-1061">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1061">Parameter name</span></span> |  <span data-ttu-id="8698d-1062">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1062">Parameter type</span></span> | <span data-ttu-id="8698d-1063">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1063">Optional</span></span> | <span data-ttu-id="8698d-1064">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1064">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1065">_filterContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1065">_filterContext</span></span> | <span data-ttu-id="8698d-1066">リスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1066">List</span></span> | <span data-ttu-id="8698d-1067">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1067">True</span></span> | <span data-ttu-id="8698d-1068">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1068">List of SysAppFilterContext for filter contexts of page</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1069">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1069">Return Value</span></span>

<span data-ttu-id="8698d-1070">ページのフィルター コンテキストの SysAppFilterContext のリスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1070">List of SysAppFilterContext for filter contexts of page</span></span>

## <a name="class-sysappresponse"></a><span data-ttu-id="8698d-1071">クラス SysAppResponse</span><span class="sxs-lookup"><span data-stu-id="8698d-1071">Class SysAppResponse</span></span>

<span data-ttu-id="8698d-1072">SysAppResponse クラス。</span><span class="sxs-lookup"><span data-stu-id="8698d-1072">SysAppResponse class.</span></span>  <span data-ttu-id="8698d-1073">このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1073">This class holds the response object for generated pages and actions</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1074">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-1074">Methods</span></span>

| <span data-ttu-id="8698d-1075">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1075">Method name</span></span> | <span data-ttu-id="8698d-1076">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1076">Returns</span></span> | <span data-ttu-id="8698d-1077">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1077">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1078">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-1078">new</span></span> | <span data-ttu-id="8698d-1079">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1079">void</span></span> |  |
| <span data-ttu-id="8698d-1080">jobId</span><span class="sxs-lookup"><span data-stu-id="8698d-1080">jobId</span></span> | <span data-ttu-id="8698d-1081">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1081">str</span></span> | <span data-ttu-id="8698d-1082">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="8698d-1082">Job Id of the request</span></span> |
| <span data-ttu-id="8698d-1083">データ</span><span class="sxs-lookup"><span data-stu-id="8698d-1083">data</span></span> | <span data-ttu-id="8698d-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="8698d-1084">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="8698d-1085">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="8698d-1085">Data of the page</span></span> |
| <span data-ttu-id="8698d-1086">failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="8698d-1086">failedInAppCall</span></span> | <span data-ttu-id="8698d-1087">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-1087">boolean</span></span> | <span data-ttu-id="8698d-1088">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="8698d-1088">Data of the page</span></span> |
| <span data-ttu-id="8698d-1089">commits</span><span class="sxs-lookup"><span data-stu-id="8698d-1089">commits</span></span> | <span data-ttu-id="8698d-1090">リスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1090">List</span></span> | <span data-ttu-id="8698d-1091">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="8698d-1091">Commits after task is completed</span></span> |
| <span data-ttu-id="8698d-1092">メッセージ</span><span class="sxs-lookup"><span data-stu-id="8698d-1092">messages</span></span> | <span data-ttu-id="8698d-1093">リスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1093">List</span></span> | <span data-ttu-id="8698d-1094">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="8698d-1094">Job Id of the request</span></span> |
| <span data-ttu-id="8698d-1095">addMessage</span><span class="sxs-lookup"><span data-stu-id="8698d-1095">addMessage</span></span> | <span data-ttu-id="8698d-1096">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1096">void</span></span> | <span data-ttu-id="8698d-1097">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="8698d-1097">Adds message</span></span> |
| <span data-ttu-id="8698d-1098">addCommit</span><span class="sxs-lookup"><span data-stu-id="8698d-1098">addCommit</span></span> | <span data-ttu-id="8698d-1099">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1099">void</span></span> | <span data-ttu-id="8698d-1100">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="8698d-1100">Adds commits</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1101">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1101">Method new</span></span>

```xpp
public void new ()
```

### <a name="method-jobid"></a><span data-ttu-id="8698d-1102">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="8698d-1102">Method jobId</span></span>

<span data-ttu-id="8698d-1103">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="8698d-1103">Job Id of the request</span></span>

```xpp
public str jobId ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1104">Return Value</span></span>

<span data-ttu-id="8698d-1105">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="8698d-1105">jobid of the request</span></span>

### <a name="method-data"></a><span data-ttu-id="8698d-1106">メソッド data</span><span class="sxs-lookup"><span data-stu-id="8698d-1106">Method data</span></span>

<span data-ttu-id="8698d-1107">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="8698d-1107">Data of the page</span></span>

```xpp
public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1108">Parameters</span></span>

| <span data-ttu-id="8698d-1109">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1109">Parameter name</span></span> |  <span data-ttu-id="8698d-1110">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1110">Parameter type</span></span> | <span data-ttu-id="8698d-1111">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1111">Optional</span></span> | <span data-ttu-id="8698d-1112">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1112">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1113">_data</span><span class="sxs-lookup"><span data-stu-id="8698d-1113">_data</span></span> | <span data-ttu-id="8698d-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span><span class="sxs-lookup"><span data-stu-id="8698d-1114">Microsoft.Dynamics.Client.ServerForm.App.CompositeData</span></span> | <span data-ttu-id="8698d-1115">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1115">True</span></span> | <span data-ttu-id="8698d-1116">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="8698d-1116">Data of the page</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1117">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1117">Return Value</span></span>

<span data-ttu-id="8698d-1118">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="8698d-1118">Data of the page</span></span>

### <a name="method-failedinappcall"></a><span data-ttu-id="8698d-1119">メソッド failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="8698d-1119">Method failedInAppCall</span></span>

<span data-ttu-id="8698d-1120">ページのデータ</span><span class="sxs-lookup"><span data-stu-id="8698d-1120">Data of the page</span></span>

```xpp
public boolean failedInAppCall ([boolean _failedInAppCall])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1121">Parameters</span></span>

| <span data-ttu-id="8698d-1122">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1122">Parameter name</span></span> |  <span data-ttu-id="8698d-1123">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1123">Parameter type</span></span> | <span data-ttu-id="8698d-1124">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1124">Optional</span></span> | <span data-ttu-id="8698d-1125">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1125">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1126">_failedInAppCall</span><span class="sxs-lookup"><span data-stu-id="8698d-1126">_failedInAppCall</span></span> | <span data-ttu-id="8698d-1127">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-1127">boolean</span></span> | <span data-ttu-id="8698d-1128">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1128">True</span></span> | <span data-ttu-id="8698d-1129">アプリケーション コードの呼び出しに失敗した場合は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1129">Sets to true if it fails in calling application code</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1130">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1130">Return Value</span></span>

<span data-ttu-id="8698d-1131">アプリケーション コードの呼び出しに失敗した場合は true です。</span><span class="sxs-lookup"><span data-stu-id="8698d-1131">True when fails in calling application code</span></span>

### <a name="method-commits"></a><span data-ttu-id="8698d-1132">メソッド commits</span><span class="sxs-lookup"><span data-stu-id="8698d-1132">Method commits</span></span>

<span data-ttu-id="8698d-1133">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="8698d-1133">Commits after task is completed</span></span>

```xpp
public List commits ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1134">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1134">Return Value</span></span>

<span data-ttu-id="8698d-1135">タスクが完了した後にコミットします。</span><span class="sxs-lookup"><span data-stu-id="8698d-1135">Commits after task is completed</span></span>

### <a name="method-messages"></a><span data-ttu-id="8698d-1136">メソッド messages</span><span class="sxs-lookup"><span data-stu-id="8698d-1136">Method messages</span></span>

<span data-ttu-id="8698d-1137">要求のジョブ ID</span><span class="sxs-lookup"><span data-stu-id="8698d-1137">Job Id of the request</span></span>

```xpp
public List messages ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1138">Return Value</span></span>

<span data-ttu-id="8698d-1139">タスクが完了した後のメッセージ</span><span class="sxs-lookup"><span data-stu-id="8698d-1139">Messages after task is completed</span></span>

### <a name="method-addmessage"></a><span data-ttu-id="8698d-1140">メソッド addMessage</span><span class="sxs-lookup"><span data-stu-id="8698d-1140">Method addMessage</span></span>

<span data-ttu-id="8698d-1141">メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="8698d-1141">Adds message</span></span>

```xpp
public void addMessage (SysAppResponseMessage _message)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1142">Parameters</span></span>

| <span data-ttu-id="8698d-1143">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1143">Parameter name</span></span> |  <span data-ttu-id="8698d-1144">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1144">Parameter type</span></span> | <span data-ttu-id="8698d-1145">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1145">Optional</span></span> | <span data-ttu-id="8698d-1146">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1146">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1147">_message</span><span class="sxs-lookup"><span data-stu-id="8698d-1147">_message</span></span> | <span data-ttu-id="8698d-1148">SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8698d-1148">SysAppResponseMessage</span></span> | <span data-ttu-id="8698d-1149">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1149">False</span></span> | <span data-ttu-id="8698d-1150">SysAppResponseMessage オブジェクトとしてのメッセージ</span><span class="sxs-lookup"><span data-stu-id="8698d-1150">message as SysAppResponseMessage object</span></span>

### <a name="method-addcommit"></a><span data-ttu-id="8698d-1151">メソッド addCommit</span><span class="sxs-lookup"><span data-stu-id="8698d-1151">Method addCommit</span></span>

<span data-ttu-id="8698d-1152">コミットの追加</span><span class="sxs-lookup"><span data-stu-id="8698d-1152">Adds commits</span></span>

```xpp
public void addCommit (SysAppEntityContext _entityContext)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1153">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1153">Parameters</span></span>

| <span data-ttu-id="8698d-1154">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1154">Parameter name</span></span> |  <span data-ttu-id="8698d-1155">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1155">Parameter type</span></span> | <span data-ttu-id="8698d-1156">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1156">Optional</span></span> | <span data-ttu-id="8698d-1157">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1157">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1158">_entityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1158">_entityContext</span></span> | <span data-ttu-id="8698d-1159">SysAppEntityContext</span><span class="sxs-lookup"><span data-stu-id="8698d-1159">SysAppEntityContext</span></span> | <span data-ttu-id="8698d-1160">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1160">False</span></span> | <span data-ttu-id="8698d-1161">確定済のエンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1161">Entity context containing entity name and entity id of the entity that is committed</span></span>

## <a name="class-sysappresponsemessage"></a><span data-ttu-id="8698d-1162">クラス SysAppResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8698d-1162">Class SysAppResponseMessage</span></span>

<span data-ttu-id="8698d-1163">応答メッセージの SysAppResponseMessage クラス</span><span class="sxs-lookup"><span data-stu-id="8698d-1163">SysAppResponseMessage class for response messages</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1164">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-1164">Methods</span></span>

| <span data-ttu-id="8698d-1165">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1165">Method name</span></span> | <span data-ttu-id="8698d-1166">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1166">Returns</span></span> | <span data-ttu-id="8698d-1167">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1167">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1168">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-1168">new</span></span> | <span data-ttu-id="8698d-1169">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1169">void</span></span> | <span data-ttu-id="8698d-1170">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-1170">Creates a new instance of SysAppResponseMessage class</span></span> |
| <span data-ttu-id="8698d-1171">テキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1171">text</span></span> | <span data-ttu-id="8698d-1172">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1172">str</span></span> | <span data-ttu-id="8698d-1173">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-1173">Gets the message text</span></span> |
| <span data-ttu-id="8698d-1174">タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1174">type</span></span> | <span data-ttu-id="8698d-1175">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="8698d-1175">SysAppMessageType</span></span> | <span data-ttu-id="8698d-1176">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="8698d-1176">Gets the message type: info, error , warning</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1177">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1177">Method new</span></span>

<span data-ttu-id="8698d-1178">SysAppResponseMessage クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-1178">Creates a new instance of SysAppResponseMessage class</span></span>

```xpp
public void new (str _text, [SysAppMessageType _type])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1179">Parameters</span></span>

| <span data-ttu-id="8698d-1180">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1180">Parameter name</span></span> |  <span data-ttu-id="8698d-1181">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1181">Parameter type</span></span> | <span data-ttu-id="8698d-1182">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1182">Optional</span></span> | <span data-ttu-id="8698d-1183">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1183">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1184">_text</span><span class="sxs-lookup"><span data-stu-id="8698d-1184">_text</span></span> | <span data-ttu-id="8698d-1185">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1185">str</span></span> | <span data-ttu-id="8698d-1186">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1186">False</span></span> | <span data-ttu-id="8698d-1187">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1187">The message text</span></span>
| <span data-ttu-id="8698d-1188">_type</span><span class="sxs-lookup"><span data-stu-id="8698d-1188">_type</span></span> | <span data-ttu-id="8698d-1189">SysAppMessageType</span><span class="sxs-lookup"><span data-stu-id="8698d-1189">SysAppMessageType</span></span> | <span data-ttu-id="8698d-1190">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1190">True</span></span> | <span data-ttu-id="8698d-1191">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="8698d-1191">Message Type: info, error , warning</span></span>

### <a name="method-text"></a><span data-ttu-id="8698d-1192">メソッド text</span><span class="sxs-lookup"><span data-stu-id="8698d-1192">Method text</span></span>

<span data-ttu-id="8698d-1193">メッセージ テキストの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-1193">Gets the message text</span></span>

```xpp
public str text ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1194">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1194">Return Value</span></span>

<span data-ttu-id="8698d-1195">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1195">The message text</span></span>

### <a name="method-type"></a><span data-ttu-id="8698d-1196">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1196">Method type</span></span>

<span data-ttu-id="8698d-1197">メッセージの種類を取得します: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="8698d-1197">Gets the message type: info, error , warning</span></span>

```xpp
public SysAppMessageType type ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1198">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1198">Return Value</span></span>

<span data-ttu-id="8698d-1199">メッセージ タイプ: 情報、エラー、警告</span><span class="sxs-lookup"><span data-stu-id="8698d-1199">The message type: info, error , warning</span></span>

## <a name="class-sysappsecurityattribute"></a><span data-ttu-id="8698d-1200">クラス SysAppSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-1200">Class SysAppSecurityAttribute</span></span>

<span data-ttu-id="8698d-1201">ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。</span><span class="sxs-lookup"><span data-stu-id="8698d-1201">SysAppSecurityAttribute used for decorating methods forming pages and actions.</span></span>  <span data-ttu-id="8698d-1202">ページまたはアクションのセキュリティ属性を指定します</span><span class="sxs-lookup"><span data-stu-id="8698d-1202">specifies security attribute of page or action</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1203">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-1203">Methods</span></span>

| <span data-ttu-id="8698d-1204">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1204">Method name</span></span> | <span data-ttu-id="8698d-1205">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1205">Returns</span></span> | <span data-ttu-id="8698d-1206">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1206">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1207">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-1207">new</span></span> | <span data-ttu-id="8698d-1208">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1208">void</span></span> | <span data-ttu-id="8698d-1209">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1209">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="8698d-1210">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="8698d-1210">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span> |
| <span data-ttu-id="8698d-1211">menuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1211">menuItemType</span></span> | <span data-ttu-id="8698d-1212">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1212">MenuItemType</span></span> | <span data-ttu-id="8698d-1213">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-1213">Gets the Menu Item Type of the page</span></span> |
| <span data-ttu-id="8698d-1214">menuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1214">menuItemName</span></span> | <span data-ttu-id="8698d-1215">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1215">MenuItemName</span></span> | <span data-ttu-id="8698d-1216">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-1216">Gets the Menu Item Name of the page</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1217">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1217">Method new</span></span>

<span data-ttu-id="8698d-1218">SysAppSecurityAttribute クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1218">Creates a new instance of SysAppSecurityAttribute class.</span></span>  <span data-ttu-id="8698d-1219">これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます</span><span class="sxs-lookup"><span data-stu-id="8698d-1219">This will help in checking if the user logged in has access to the specified menu item and menu item type</span></span>

```xpp
public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1220">Parameters</span></span>

| <span data-ttu-id="8698d-1221">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1221">Parameter name</span></span> |  <span data-ttu-id="8698d-1222">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1222">Parameter type</span></span> | <span data-ttu-id="8698d-1223">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1223">Optional</span></span> | <span data-ttu-id="8698d-1224">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1224">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1225">_menuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1225">_menuItemName</span></span> | <span data-ttu-id="8698d-1226">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1226">MenuItemName</span></span> | <span data-ttu-id="8698d-1227">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1227">True</span></span> | <span data-ttu-id="8698d-1228">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="8698d-1228">Menu Item Name of the page</span></span>
| <span data-ttu-id="8698d-1229">_menuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1229">_menuItemType</span></span> | <span data-ttu-id="8698d-1230">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1230">MenuItemType</span></span> | <span data-ttu-id="8698d-1231">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1231">True</span></span> | <span data-ttu-id="8698d-1232">アクション、表示または出力など、ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1232">Menu Item Type of the page like action, display or output</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="8698d-1233">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1233">Method menuItemType</span></span>

<span data-ttu-id="8698d-1234">ページのメニュー項目タイプの取得</span><span class="sxs-lookup"><span data-stu-id="8698d-1234">Gets the Menu Item Type of the page</span></span>

```xpp
public MenuItemType menuItemType ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1235">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1235">Return Value</span></span>

<span data-ttu-id="8698d-1236">ページのメニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1236">Menu Item Type of the page</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="8698d-1237">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1237">Method menuItemName</span></span>

<span data-ttu-id="8698d-1238">ページのメニュー項目名の取得</span><span class="sxs-lookup"><span data-stu-id="8698d-1238">Gets the Menu Item Name of the page</span></span>

```xpp
public MenuItemName menuItemName ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1239">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1239">Return Value</span></span>

<span data-ttu-id="8698d-1240">ページのメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="8698d-1240">Menu Item Name of the page</span></span>

## <a name="class-sysappworkspace"></a><span data-ttu-id="8698d-1241">クラス SysAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="8698d-1241">Class SysAppWorkspace</span></span>

<span data-ttu-id="8698d-1242">これは、AX モバイル ワークスペースの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="8698d-1242">This is the base class of AX mobile workspace.</span></span> <span data-ttu-id="8698d-1243">AX モバイル ワークスペース クラスは、このクラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8698d-1243">AX mobile workspace classes needs to extend from this class</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1244">方法</span><span class="sxs-lookup"><span data-stu-id="8698d-1244">Methods</span></span>

| <span data-ttu-id="8698d-1245">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1245">Method name</span></span> | <span data-ttu-id="8698d-1246">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1246">Returns</span></span> | <span data-ttu-id="8698d-1247">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1247">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1248">getEnumValues</span><span class="sxs-lookup"><span data-stu-id="8698d-1248">getEnumValues</span></span> | <span data-ttu-id="8698d-1249">リスト</span><span class="sxs-lookup"><span data-stu-id="8698d-1249">List</span></span> | <span data-ttu-id="8698d-1250">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1250">Called during workspace initialization.</span></span> <span data-ttu-id="8698d-1251">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="8698d-1251">Can be used to modify the enum values that are returned to AX mobile</span></span> |
| <span data-ttu-id="8698d-1252">getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-1252">getWorkspaceMetadata</span></span> | <span data-ttu-id="8698d-1253">SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-1253">SysAppWorkspaceMetadata</span></span> | <span data-ttu-id="8698d-1254">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1254">Called during workspace initialization.</span></span> <span data-ttu-id="8698d-1255">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="8698d-1255">Can be used to modify the workspace metadata</span></span> |
| <span data-ttu-id="8698d-1256">onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="8698d-1256">onBeginAppJob</span></span> | <span data-ttu-id="8698d-1257">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1257">void</span></span> | <span data-ttu-id="8698d-1258">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="8698d-1258">Called before the start of execution of AX mobile job</span></span> |
| <span data-ttu-id="8698d-1259">onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="8698d-1259">onEndAppJob</span></span> | <span data-ttu-id="8698d-1260">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1260">void</span></span> | <span data-ttu-id="8698d-1261">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="8698d-1261">Called after the end of execution of AX mobile job</span></span> |
| <span data-ttu-id="8698d-1262">workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-1262">workspaceHidden</span></span> | <span data-ttu-id="8698d-1263">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-1263">boolean</span></span> | <span data-ttu-id="8698d-1264">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1264">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="8698d-1265">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1265">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="8698d-1266">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1266">If the attribute is not specified on the class than it always returns false</span></span> |

### <a name="method-getenumvalues"></a><span data-ttu-id="8698d-1267">メソッド getEnumValues</span><span class="sxs-lookup"><span data-stu-id="8698d-1267">Method getEnumValues</span></span>

<span data-ttu-id="8698d-1268">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1268">Called during workspace initialization.</span></span> <span data-ttu-id="8698d-1269">AX モバイルに返される列挙型の値を変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="8698d-1269">Can be used to modify the enum values that are returned to AX mobile</span></span>

```xpp
public List getEnumValues (EnumName _enumName)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1270">Parameters</span></span>

| <span data-ttu-id="8698d-1271">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1271">Parameter name</span></span> |  <span data-ttu-id="8698d-1272">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1272">Parameter type</span></span> | <span data-ttu-id="8698d-1273">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1273">Optional</span></span> | <span data-ttu-id="8698d-1274">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1274">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1275">_enumName</span><span class="sxs-lookup"><span data-stu-id="8698d-1275">_enumName</span></span> | <span data-ttu-id="8698d-1276">EnumName</span><span class="sxs-lookup"><span data-stu-id="8698d-1276">EnumName</span></span> | <span data-ttu-id="8698d-1277">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1277">False</span></span> | <span data-ttu-id="8698d-1278">列挙名</span><span class="sxs-lookup"><span data-stu-id="8698d-1278">The enum name</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1279">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1279">Return Value</span></span>

<span data-ttu-id="8698d-1280">列挙値の一覧</span><span class="sxs-lookup"><span data-stu-id="8698d-1280">A list of enum value</span></span>

### <a name="method-getworkspacemetadata"></a><span data-ttu-id="8698d-1281">メソッド getWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-1281">Method getWorkspaceMetadata</span></span>

<span data-ttu-id="8698d-1282">ワークスペースの初期化中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1282">Called during workspace initialization.</span></span> <span data-ttu-id="8698d-1283">ワークスペースのメタデータを変更するために使用できます</span><span class="sxs-lookup"><span data-stu-id="8698d-1283">Can be used to modify the workspace metadata</span></span>

```xpp
public SysAppWorkspaceMetadata getWorkspaceMetadata ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1284">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1284">Return Value</span></span>

<span data-ttu-id="8698d-1285">ワークスペース メタデータを表すオブジェクト</span><span class="sxs-lookup"><span data-stu-id="8698d-1285">An object representing the workspace metadata</span></span>

### <a name="method-onbeginappjob"></a><span data-ttu-id="8698d-1286">メソッド onBeginAppJob</span><span class="sxs-lookup"><span data-stu-id="8698d-1286">Method onBeginAppJob</span></span>

<span data-ttu-id="8698d-1287">AX モバイル ジョブの実行開始前の呼び出し</span><span class="sxs-lookup"><span data-stu-id="8698d-1287">Called before the start of execution of AX mobile job</span></span>

```xpp
public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1288">Parameters</span></span>

| <span data-ttu-id="8698d-1289">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1289">Parameter name</span></span> |  <span data-ttu-id="8698d-1290">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1290">Parameter type</span></span> | <span data-ttu-id="8698d-1291">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1291">Optional</span></span> | <span data-ttu-id="8698d-1292">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1292">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1293">_sysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="8698d-1293">_sysAppJobRequest</span></span> | <span data-ttu-id="8698d-1294">SysAppJobRequest</span><span class="sxs-lookup"><span data-stu-id="8698d-1294">SysAppJobRequest</span></span> | <span data-ttu-id="8698d-1295">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1295">False</span></span> | <span data-ttu-id="8698d-1296">ジョブ要求パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="8698d-1296">A class containing job request parameters</span></span>

### <a name="method-onendappjob"></a><span data-ttu-id="8698d-1297">メソッド onEndAppJob</span><span class="sxs-lookup"><span data-stu-id="8698d-1297">Method onEndAppJob</span></span>

<span data-ttu-id="8698d-1298">AX モバイル ジョブの実行の終了後の呼び出し</span><span class="sxs-lookup"><span data-stu-id="8698d-1298">Called after the end of execution of AX mobile job</span></span>

```xpp
public void onEndAppJob (SysAppJobResponse _sysAppJobResponse)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1299">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1299">Parameters</span></span>

| <span data-ttu-id="8698d-1300">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1300">Parameter name</span></span> |  <span data-ttu-id="8698d-1301">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1301">Parameter type</span></span> | <span data-ttu-id="8698d-1302">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1302">Optional</span></span> | <span data-ttu-id="8698d-1303">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1303">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1304">_sysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="8698d-1304">_sysAppJobResponse</span></span> | <span data-ttu-id="8698d-1305">SysAppJobResponse</span><span class="sxs-lookup"><span data-stu-id="8698d-1305">SysAppJobResponse</span></span> | <span data-ttu-id="8698d-1306">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1306">False</span></span> | <span data-ttu-id="8698d-1307">ジョブ応答パラメーターを含むクラス</span><span class="sxs-lookup"><span data-stu-id="8698d-1307">A class containing job response parameters</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="8698d-1308">メソッド workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-1308">Method workspaceHidden</span></span>

<span data-ttu-id="8698d-1309">ワークスペースを非表示にするかどうかを制御するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1309">Can be used to control whether the workspace is hidden or not.</span></span>  <span data-ttu-id="8698d-1310">現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1310">Checks that the current user have access menu item specified by SysAppWorkspaceSecurityAttribute on the workspace class .</span></span>  <span data-ttu-id="8698d-1311">クラスに属性が指定されていない場合は常に false を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1311">If the attribute is not specified on the class than it always returns false</span></span>

```xpp
public boolean workspaceHidden ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1312">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1312">Return Value</span></span>

<span data-ttu-id="8698d-1313">ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1313">Returns true if the workspace is hidden otherwise false</span></span>

## <a name="class-sysappworkspaceattribute"></a><span data-ttu-id="8698d-1314">クラス SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-1314">Class SysAppWorkspaceAttribute</span></span>

<span data-ttu-id="8698d-1315">SysAppWorkspace から拡張されたクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1315">Applied on classes that are extended from SysAppWorkspace</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1316">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-1316">Methods</span></span>

| <span data-ttu-id="8698d-1317">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1317">Method name</span></span> | <span data-ttu-id="8698d-1318">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1318">Returns</span></span> | <span data-ttu-id="8698d-1319">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1319">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1320">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-1320">new</span></span> | <span data-ttu-id="8698d-1321">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1321">void</span></span> | <span data-ttu-id="8698d-1322">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-1322">Creates a new instance of SysAppWorkspaceAttribute class</span></span> |
| <span data-ttu-id="8698d-1323">AppId</span><span class="sxs-lookup"><span data-stu-id="8698d-1323">AppId</span></span> | <span data-ttu-id="8698d-1324">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1324">str</span></span> | <span data-ttu-id="8698d-1325">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1325">Gets or sets the AppId of the workspace</span></span> |
| <span data-ttu-id="8698d-1326">AppResourceName</span><span class="sxs-lookup"><span data-stu-id="8698d-1326">AppResourceName</span></span> | <span data-ttu-id="8698d-1327">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1327">str</span></span> | <span data-ttu-id="8698d-1328">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1328">Gets or sets the AOT Resource name which contains the workspace</span></span> |
| <span data-ttu-id="8698d-1329">WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-1329">WorkspaceHidden</span></span> | <span data-ttu-id="8698d-1330">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-1330">boolean</span></span> | <span data-ttu-id="8698d-1331">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1331">Gets or sets if the workspace is hidden from designer</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1332">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1332">Method new</span></span>

<span data-ttu-id="8698d-1333">SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="8698d-1333">Creates a new instance of SysAppWorkspaceAttribute class</span></span>

```xpp
public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1334">Parameters</span></span>

| <span data-ttu-id="8698d-1335">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1335">Parameter name</span></span> |  <span data-ttu-id="8698d-1336">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1336">Parameter type</span></span> | <span data-ttu-id="8698d-1337">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1337">Optional</span></span> | <span data-ttu-id="8698d-1338">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1338">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1339">_appId</span><span class="sxs-lookup"><span data-stu-id="8698d-1339">_appId</span></span> | <span data-ttu-id="8698d-1340">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1340">str</span></span> | <span data-ttu-id="8698d-1341">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1341">False</span></span> | <span data-ttu-id="8698d-1342">ワークスペースの appId</span><span class="sxs-lookup"><span data-stu-id="8698d-1342">The appId of the workspace</span></span>
| <span data-ttu-id="8698d-1343">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="8698d-1343">_appResourceName</span></span> | <span data-ttu-id="8698d-1344">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1344">str</span></span> | <span data-ttu-id="8698d-1345">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1345">True</span></span> | <span data-ttu-id="8698d-1346">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="8698d-1346">The AOT resource name which contains the workspace</span></span>
| <span data-ttu-id="8698d-1347">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-1347">_workspaceHidden</span></span> | <span data-ttu-id="8698d-1348">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-1348">boolean</span></span> | <span data-ttu-id="8698d-1349">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1349">True</span></span> | <span data-ttu-id="8698d-1350">ワークスペースはデザイナーには表示されません</span><span class="sxs-lookup"><span data-stu-id="8698d-1350">The workspace is hidden from designer</span></span>

### <a name="method-appid"></a><span data-ttu-id="8698d-1351">メソッド AppId</span><span class="sxs-lookup"><span data-stu-id="8698d-1351">Method AppId</span></span>

<span data-ttu-id="8698d-1352">ワークスペースの AppId の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1352">Gets or sets the AppId of the workspace</span></span>

```xpp
public str AppId ([str _appId])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1353">Parameters</span></span>

| <span data-ttu-id="8698d-1354">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1354">Parameter name</span></span> |  <span data-ttu-id="8698d-1355">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1355">Parameter type</span></span> | <span data-ttu-id="8698d-1356">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1356">Optional</span></span> | <span data-ttu-id="8698d-1357">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1357">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1358">_appId</span><span class="sxs-lookup"><span data-stu-id="8698d-1358">_appId</span></span> | <span data-ttu-id="8698d-1359">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1359">str</span></span> | <span data-ttu-id="8698d-1360">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1360">True</span></span> | <span data-ttu-id="8698d-1361">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="8698d-1361">The AppId of the workspace</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1362">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1362">Return Value</span></span>

<span data-ttu-id="8698d-1363">ワークスペースの AppId</span><span class="sxs-lookup"><span data-stu-id="8698d-1363">The AppId of the workspace</span></span>

### <a name="method-appresourcename"></a><span data-ttu-id="8698d-1364">メソッド AppResourceName</span><span class="sxs-lookup"><span data-stu-id="8698d-1364">Method AppResourceName</span></span>

<span data-ttu-id="8698d-1365">ワークスペースを含む AOT リソース名の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1365">Gets or sets the AOT Resource name which contains the workspace</span></span>

```xpp
public str AppResourceName ([str _appResourceName])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1366">Parameters</span></span>

| <span data-ttu-id="8698d-1367">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1367">Parameter name</span></span> |  <span data-ttu-id="8698d-1368">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1368">Parameter type</span></span> | <span data-ttu-id="8698d-1369">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1369">Optional</span></span> | <span data-ttu-id="8698d-1370">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1370">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1371">_appResourceName</span><span class="sxs-lookup"><span data-stu-id="8698d-1371">_appResourceName</span></span> | <span data-ttu-id="8698d-1372">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1372">str</span></span> | <span data-ttu-id="8698d-1373">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1373">True</span></span> | <span data-ttu-id="8698d-1374">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="8698d-1374">The AOT Resource name which contains the workspace</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1375">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1375">Return Value</span></span>

<span data-ttu-id="8698d-1376">ワークスペースを含む AOT リソース名</span><span class="sxs-lookup"><span data-stu-id="8698d-1376">The AOT Resource name which contains the workspace</span></span>

### <a name="method-workspacehidden"></a><span data-ttu-id="8698d-1377">メソッド WorkspaceHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-1377">Method WorkspaceHidden</span></span>

<span data-ttu-id="8698d-1378">ワークスペースがデザイナーに非表示かどうかを取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1378">Gets or sets if the workspace is hidden from designer</span></span>

```xpp
public boolean WorkspaceHidden ([boolean _workspaceHidden])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1379">Parameters</span></span>

| <span data-ttu-id="8698d-1380">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1380">Parameter name</span></span> |  <span data-ttu-id="8698d-1381">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1381">Parameter type</span></span> | <span data-ttu-id="8698d-1382">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1382">Optional</span></span> | <span data-ttu-id="8698d-1383">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1383">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1384">_workspaceHidden</span><span class="sxs-lookup"><span data-stu-id="8698d-1384">_workspaceHidden</span></span> | <span data-ttu-id="8698d-1385">ブール値</span><span class="sxs-lookup"><span data-stu-id="8698d-1385">boolean</span></span> | <span data-ttu-id="8698d-1386">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1386">True</span></span> | <span data-ttu-id="8698d-1387">非表示のワークスペース</span><span class="sxs-lookup"><span data-stu-id="8698d-1387">The workspace hidden</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1388">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1388">Return Value</span></span>

<span data-ttu-id="8698d-1389">ワークスペースがデザイナーに非表示かどうか</span><span class="sxs-lookup"><span data-stu-id="8698d-1389">Whether the workspace is hidden from designer or not</span></span>

## <a name="class-sysappworkspacemetadata"></a><span data-ttu-id="8698d-1390">クラス SysAppWorkspaceMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-1390">Class SysAppWorkspaceMetadata</span></span>

<span data-ttu-id="8698d-1391">このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。</span><span class="sxs-lookup"><span data-stu-id="8698d-1391">This class can be used to access and update metadata of an AX mobile workspace</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1392">方法</span><span class="sxs-lookup"><span data-stu-id="8698d-1392">Methods</span></span>

| <span data-ttu-id="8698d-1393">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1393">Method name</span></span> | <span data-ttu-id="8698d-1394">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1394">Returns</span></span> | <span data-ttu-id="8698d-1395">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1395">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1396">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-1396">new</span></span> | <span data-ttu-id="8698d-1397">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1397">void</span></span> |  |
| <span data-ttu-id="8698d-1398">addConfig</span><span class="sxs-lookup"><span data-stu-id="8698d-1398">addConfig</span></span> | <span data-ttu-id="8698d-1399">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1399">void</span></span> | <span data-ttu-id="8698d-1400">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1400">Adds a custom config to the mobile workspace metadata</span></span> |
| <span data-ttu-id="8698d-1401">getPage</span><span class="sxs-lookup"><span data-stu-id="8698d-1401">getPage</span></span> | <span data-ttu-id="8698d-1402">SysAppPageMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-1402">SysAppPageMetadata</span></span> | <span data-ttu-id="8698d-1403">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1403">Returns the page with the pageName provided</span></span> |
| <span data-ttu-id="8698d-1404">getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-1404">getPageEnumerator</span></span> | <span data-ttu-id="8698d-1405">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-1405">MapEnumerator</span></span> | <span data-ttu-id="8698d-1406">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1406">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="8698d-1407">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-1407">Where key is page name and value is of type SysAppPageMetadata</span></span> |
| <span data-ttu-id="8698d-1408">getAction</span><span class="sxs-lookup"><span data-stu-id="8698d-1408">getAction</span></span> | <span data-ttu-id="8698d-1409">SysAppActionMetadata</span><span class="sxs-lookup"><span data-stu-id="8698d-1409">SysAppActionMetadata</span></span> | <span data-ttu-id="8698d-1410">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1410">Returns the action with the actionName provided</span></span> |
| <span data-ttu-id="8698d-1411">getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-1411">getActionEnumerator</span></span> | <span data-ttu-id="8698d-1412">MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-1412">MapEnumerator</span></span> | <span data-ttu-id="8698d-1413">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1413">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="8698d-1414">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-1414">Where key is action name and value is of type SysAppActionMetadata</span></span> |
| <span data-ttu-id="8698d-1415">getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1415">getPageNameForRecordingId</span></span> | <span data-ttu-id="8698d-1416">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1416">str</span></span> | <span data-ttu-id="8698d-1417">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1417">Returns a pageName if the provided recordingId is used by a workspace page</span></span> |
| <span data-ttu-id="8698d-1418">getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1418">getActionNameForRecordingId</span></span> | <span data-ttu-id="8698d-1419">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1419">str</span></span> | <span data-ttu-id="8698d-1420">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1420">Returns a actionName if the provided recordingId is used by a workspace action</span></span> |
| <span data-ttu-id="8698d-1421">workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-1421">workspaceTitle</span></span> | <span data-ttu-id="8698d-1422">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1422">str</span></span> | <span data-ttu-id="8698d-1423">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1423">Gets and sets the workspace title</span></span> |
| <span data-ttu-id="8698d-1424">workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-1424">workspaceDescription</span></span> | <span data-ttu-id="8698d-1425">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1425">str</span></span> | <span data-ttu-id="8698d-1426">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1426">Gets and sets the workspace description</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1427">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1427">Method new</span></span>

```xpp
public void new (str _appId, [SysAppWorkspaceAttribute _attribute])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1428">Parameters</span></span>

| <span data-ttu-id="8698d-1429">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1429">Parameter name</span></span> |  <span data-ttu-id="8698d-1430">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1430">Parameter type</span></span> | <span data-ttu-id="8698d-1431">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1431">Optional</span></span> | <span data-ttu-id="8698d-1432">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1432">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1433">_appId</span><span class="sxs-lookup"><span data-stu-id="8698d-1433">_appId</span></span> | <span data-ttu-id="8698d-1434">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1434">str</span></span> | <span data-ttu-id="8698d-1435">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1435">False</span></span> |
| <span data-ttu-id="8698d-1436">_attribute</span><span class="sxs-lookup"><span data-stu-id="8698d-1436">_attribute</span></span> | <span data-ttu-id="8698d-1437">SysAppWorkspaceAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-1437">SysAppWorkspaceAttribute</span></span> | <span data-ttu-id="8698d-1438">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1438">True</span></span> |

### <a name="method-addconfig"></a><span data-ttu-id="8698d-1439">メソッド addConfig</span><span class="sxs-lookup"><span data-stu-id="8698d-1439">Method addConfig</span></span>

<span data-ttu-id="8698d-1440">モバイル ワークスペース メタデータにカスタム構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1440">Adds a custom config to the mobile workspace metadata</span></span>

```xpp
public void addConfig (str _configName, object _configValue)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1441">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1441">Parameters</span></span>

| <span data-ttu-id="8698d-1442">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1442">Parameter name</span></span> |  <span data-ttu-id="8698d-1443">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1443">Parameter type</span></span> | <span data-ttu-id="8698d-1444">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1444">Optional</span></span> | <span data-ttu-id="8698d-1445">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1445">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1446">_configName</span><span class="sxs-lookup"><span data-stu-id="8698d-1446">_configName</span></span> | <span data-ttu-id="8698d-1447">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1447">str</span></span> | <span data-ttu-id="8698d-1448">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1448">False</span></span> | <span data-ttu-id="8698d-1449">コンフィギュレーション名</span><span class="sxs-lookup"><span data-stu-id="8698d-1449">A config name</span></span>
| <span data-ttu-id="8698d-1450">_configValue</span><span class="sxs-lookup"><span data-stu-id="8698d-1450">_configValue</span></span> | <span data-ttu-id="8698d-1451">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8698d-1451">object</span></span> | <span data-ttu-id="8698d-1452">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1452">False</span></span> | <span data-ttu-id="8698d-1453">X++ データ契約クラスのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="8698d-1453">An object of a X++ data contract class</span></span>

### <a name="method-getpage"></a><span data-ttu-id="8698d-1454">メソッド getPage</span><span class="sxs-lookup"><span data-stu-id="8698d-1454">Method getPage</span></span>

<span data-ttu-id="8698d-1455">提供される pageName を持つページを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1455">Returns the page with the pageName provided</span></span>

```xpp
public SysAppPageMetadata getPage (str _pageName)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1456">Parameters</span></span>

| <span data-ttu-id="8698d-1457">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1457">Parameter name</span></span> |  <span data-ttu-id="8698d-1458">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1458">Parameter type</span></span> | <span data-ttu-id="8698d-1459">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1459">Optional</span></span> | <span data-ttu-id="8698d-1460">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1460">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1461">_pageName</span><span class="sxs-lookup"><span data-stu-id="8698d-1461">_pageName</span></span> | <span data-ttu-id="8698d-1462">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1462">str</span></span> | <span data-ttu-id="8698d-1463">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1463">False</span></span> | <span data-ttu-id="8698d-1464">ページ名</span><span class="sxs-lookup"><span data-stu-id="8698d-1464">A page name</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1465">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1465">Return Value</span></span>

<span data-ttu-id="8698d-1466">指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1466">Returns the pageMetadata if a page with the provided name exist; otherwise null</span></span>

### <a name="method-getpageenumerator"></a><span data-ttu-id="8698d-1467">メソッド getPageEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-1467">Method getPageEnumerator</span></span>

<span data-ttu-id="8698d-1468">ワークスペース ページを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1468">Returns a map enumerator that can be used to enumerate workspace pages.</span></span>  <span data-ttu-id="8698d-1469">ここで、key はページ名で、値は SysAppPageMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-1469">Where key is page name and value is of type SysAppPageMetadata</span></span>

```xpp
public MapEnumerator getPageEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1470">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1470">Return Value</span></span>

<span data-ttu-id="8698d-1471">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="8698d-1471">A map enumerator</span></span>

### <a name="method-getaction"></a><span data-ttu-id="8698d-1472">メソッド getAction</span><span class="sxs-lookup"><span data-stu-id="8698d-1472">Method getAction</span></span>

<span data-ttu-id="8698d-1473">提供される actionName を持つアクションを返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1473">Returns the action with the actionName provided</span></span>

```xpp
public SysAppActionMetadata getAction (str _actionName)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1474">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1474">Parameters</span></span>

| <span data-ttu-id="8698d-1475">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1475">Parameter name</span></span> |  <span data-ttu-id="8698d-1476">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1476">Parameter type</span></span> | <span data-ttu-id="8698d-1477">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1477">Optional</span></span> | <span data-ttu-id="8698d-1478">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1478">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1479">_actionName</span><span class="sxs-lookup"><span data-stu-id="8698d-1479">_actionName</span></span> | <span data-ttu-id="8698d-1480">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1480">str</span></span> | <span data-ttu-id="8698d-1481">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1481">False</span></span> | <span data-ttu-id="8698d-1482">アクション名</span><span class="sxs-lookup"><span data-stu-id="8698d-1482">An action name</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1483">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1483">Return Value</span></span>

<span data-ttu-id="8698d-1484">指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1484">Returns the ActionMetadata if an action with the provided name exist;otherwise null</span></span>

### <a name="method-getactionenumerator"></a><span data-ttu-id="8698d-1485">メソッド getActionEnumerator</span><span class="sxs-lookup"><span data-stu-id="8698d-1485">Method getActionEnumerator</span></span>

<span data-ttu-id="8698d-1486">ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8698d-1486">Returns a map enumerator that can be used to enumerate workspace actions.</span></span>  <span data-ttu-id="8698d-1487">ここで、key はアクション名で、値は SysAppActionMetadata 型です</span><span class="sxs-lookup"><span data-stu-id="8698d-1487">Where key is action name and value is of type SysAppActionMetadata</span></span>

```xpp
public MapEnumerator getActionEnumerator ()
```

#### <a name="return-value"></a><span data-ttu-id="8698d-1488">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1488">Return Value</span></span>

<span data-ttu-id="8698d-1489">マップ列挙子</span><span class="sxs-lookup"><span data-stu-id="8698d-1489">A map enumerator</span></span>

### <a name="method-getpagenameforrecordingid"></a><span data-ttu-id="8698d-1490">メソッド getPageNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1490">Method getPageNameForRecordingId</span></span>

<span data-ttu-id="8698d-1491">指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1491">Returns a pageName if the provided recordingId is used by a workspace page</span></span>

```xpp
public str getPageNameForRecordingId (str _recordingId)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1492">Parameters</span></span>

| <span data-ttu-id="8698d-1493">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1493">Parameter name</span></span> |  <span data-ttu-id="8698d-1494">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1494">Parameter type</span></span> | <span data-ttu-id="8698d-1495">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1495">Optional</span></span> | <span data-ttu-id="8698d-1496">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1496">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1497">_recordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1497">_recordingId</span></span> | <span data-ttu-id="8698d-1498">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1498">str</span></span> | <span data-ttu-id="8698d-1499">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1499">False</span></span> | <span data-ttu-id="8698d-1500">recordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1500">A recordingId</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1501">Return Value</span></span>

<span data-ttu-id="8698d-1502">指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="8698d-1502">A page name if the supplied recordingId is used by a workspace page; otherwise empty string</span></span>

### <a name="method-getactionnameforrecordingid"></a><span data-ttu-id="8698d-1503">メソッド getActionNameForRecordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1503">Method getActionNameForRecordingId</span></span>

<span data-ttu-id="8698d-1504">指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します</span><span class="sxs-lookup"><span data-stu-id="8698d-1504">Returns a actionName if the provided recordingId is used by a workspace action</span></span>

```xpp
public str getActionNameForRecordingId (str _recordingId)
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1505">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1505">Parameters</span></span>

| <span data-ttu-id="8698d-1506">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1506">Parameter name</span></span> |  <span data-ttu-id="8698d-1507">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1507">Parameter type</span></span> | <span data-ttu-id="8698d-1508">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1508">Optional</span></span> | <span data-ttu-id="8698d-1509">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1509">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1510">_recordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1510">_recordingId</span></span> | <span data-ttu-id="8698d-1511">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1511">str</span></span> | <span data-ttu-id="8698d-1512">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1512">False</span></span> | <span data-ttu-id="8698d-1513">recordingId</span><span class="sxs-lookup"><span data-stu-id="8698d-1513">A recordingId</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1514">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1514">Return Value</span></span>

<span data-ttu-id="8698d-1515">指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="8698d-1515">An action name if the supplied recordingId is used by a workspace action;otherwise empty string</span></span>

### <a name="method-workspacetitle"></a><span data-ttu-id="8698d-1516">メソッド workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-1516">Method workspaceTitle</span></span>

<span data-ttu-id="8698d-1517">ワークスペース タイトルの取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1517">Gets and sets the workspace title</span></span>

```xpp
public str workspaceTitle ([str _workspaceTitle])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1518">Parameters</span></span>

| <span data-ttu-id="8698d-1519">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1519">Parameter name</span></span> |  <span data-ttu-id="8698d-1520">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1520">Parameter type</span></span> | <span data-ttu-id="8698d-1521">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1521">Optional</span></span> | <span data-ttu-id="8698d-1522">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1522">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1523">_workspaceTitle</span><span class="sxs-lookup"><span data-stu-id="8698d-1523">_workspaceTitle</span></span> | <span data-ttu-id="8698d-1524">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1524">str</span></span> | <span data-ttu-id="8698d-1525">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1525">True</span></span> | <span data-ttu-id="8698d-1526">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-1526">The workspace title</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1527">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1527">Return Value</span></span>

<span data-ttu-id="8698d-1528">ワークスペースのタイトル</span><span class="sxs-lookup"><span data-stu-id="8698d-1528">The workspace title</span></span>

### <a name="method-workspacedescription"></a><span data-ttu-id="8698d-1529">メソッド workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-1529">Method workspaceDescription</span></span>

<span data-ttu-id="8698d-1530">ワークスペースの説明の取得および設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1530">Gets and sets the workspace description</span></span>

```xpp
public str workspaceDescription ([str _workspaceDescription])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1531">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1531">Parameters</span></span>

| <span data-ttu-id="8698d-1532">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1532">Parameter name</span></span> |  <span data-ttu-id="8698d-1533">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1533">Parameter type</span></span> | <span data-ttu-id="8698d-1534">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1534">Optional</span></span> | <span data-ttu-id="8698d-1535">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1535">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1536">_workspaceDescription</span><span class="sxs-lookup"><span data-stu-id="8698d-1536">_workspaceDescription</span></span> | <span data-ttu-id="8698d-1537">str</span><span class="sxs-lookup"><span data-stu-id="8698d-1537">str</span></span> | <span data-ttu-id="8698d-1538">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1538">True</span></span> | <span data-ttu-id="8698d-1539">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1539">The workspace description</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1540">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1540">Return Value</span></span>

<span data-ttu-id="8698d-1541">ワークスペースの説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1541">The workspace description</span></span>

## <a name="class-sysappworkspacesecurityattribute"></a><span data-ttu-id="8698d-1542">クラス SysAppWorkspaceSecurityAttribute</span><span class="sxs-lookup"><span data-stu-id="8698d-1542">Class SysAppWorkspaceSecurityAttribute</span></span>

<span data-ttu-id="8698d-1543">この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="8698d-1543">Controls the visibility based of workspace based on the menu item tied to this attribute</span></span>

### <a name="methods"></a><span data-ttu-id="8698d-1544">メソッド</span><span class="sxs-lookup"><span data-stu-id="8698d-1544">Methods</span></span>

| <span data-ttu-id="8698d-1545">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8698d-1545">Method name</span></span> | <span data-ttu-id="8698d-1546">返品</span><span class="sxs-lookup"><span data-stu-id="8698d-1546">Returns</span></span> | <span data-ttu-id="8698d-1547">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1547">Description</span></span> |
| -- | -- | -- |
| <span data-ttu-id="8698d-1548">新規</span><span class="sxs-lookup"><span data-stu-id="8698d-1548">new</span></span> | <span data-ttu-id="8698d-1549">無効</span><span class="sxs-lookup"><span data-stu-id="8698d-1549">void</span></span> | <span data-ttu-id="8698d-1550">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="8698d-1550">Creates a new instance of attribute</span></span> |
| <span data-ttu-id="8698d-1551">WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1551">WorkspaceMenuItemName</span></span> | <span data-ttu-id="8698d-1552">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1552">MenuItemName</span></span> | <span data-ttu-id="8698d-1553">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1553">Gets or sets the workspace menuItem for the workspace security attribute</span></span> |
| <span data-ttu-id="8698d-1554">WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1554">WorkspaceMenuItemType</span></span> | <span data-ttu-id="8698d-1555">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1555">MenuItemType</span></span> | <span data-ttu-id="8698d-1556">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1556">Gets or sets the workspace menu item type for the workspace security attribute</span></span> |

### <a name="method-new"></a><span data-ttu-id="8698d-1557">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8698d-1557">Method new</span></span>

<span data-ttu-id="8698d-1558">属性の新しいインスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="8698d-1558">Creates a new instance of attribute</span></span>

```xpp
public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1559">Parameters</span></span>

| <span data-ttu-id="8698d-1560">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1560">Parameter name</span></span> |  <span data-ttu-id="8698d-1561">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1561">Parameter type</span></span> | <span data-ttu-id="8698d-1562">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1562">Optional</span></span> | <span data-ttu-id="8698d-1563">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1563">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1564">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1564">_workspaceMenuItemName</span></span> | <span data-ttu-id="8698d-1565">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1565">MenuItemName</span></span> | <span data-ttu-id="8698d-1566">False</span><span class="sxs-lookup"><span data-stu-id="8698d-1566">False</span></span> | <span data-ttu-id="8698d-1567">ワークスペースを関連付ける必要のあるメニュー項目名</span><span class="sxs-lookup"><span data-stu-id="8698d-1567">The menu item name to which the workspace needs to be tied</span></span>
| <span data-ttu-id="8698d-1568">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1568">_workspaceMenuItemType</span></span> | <span data-ttu-id="8698d-1569">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1569">MenuItemType</span></span> | <span data-ttu-id="8698d-1570">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1570">True</span></span> | <span data-ttu-id="8698d-1571">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1571">The menu item type</span></span>

### <a name="method-workspacemenuitemname"></a><span data-ttu-id="8698d-1572">メソッド WorkspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1572">Method WorkspaceMenuItemName</span></span>

<span data-ttu-id="8698d-1573">ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1573">Gets or sets the workspace menuItem for the workspace security attribute</span></span>

```xpp
public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1574">Parameters</span></span>

| <span data-ttu-id="8698d-1575">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1575">Parameter name</span></span> |  <span data-ttu-id="8698d-1576">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1576">Parameter type</span></span> | <span data-ttu-id="8698d-1577">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1577">Optional</span></span> | <span data-ttu-id="8698d-1578">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1578">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1579">_workspaceMenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1579">_workspaceMenuItemName</span></span> | <span data-ttu-id="8698d-1580">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="8698d-1580">MenuItemName</span></span> | <span data-ttu-id="8698d-1581">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1581">True</span></span> | <span data-ttu-id="8698d-1582">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="8698d-1582">The workspace menu item for the workspace security attribute</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1583">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1583">Return Value</span></span>

<span data-ttu-id="8698d-1584">ワークスペース セキュリティ属性のワークスペース メニュー項目</span><span class="sxs-lookup"><span data-stu-id="8698d-1584">The workspace menu item for the workspace security attribute</span></span>

### <a name="method-workspacemenuitemtype"></a><span data-ttu-id="8698d-1585">メソッド WorkspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1585">Method WorkspaceMenuItemType</span></span>

<span data-ttu-id="8698d-1586">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定</span><span class="sxs-lookup"><span data-stu-id="8698d-1586">Gets or sets the workspace menu item type for the workspace security attribute</span></span>

```xpp
public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType])
```

#### <a name="parameters"></a><span data-ttu-id="8698d-1587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8698d-1587">Parameters</span></span>

| <span data-ttu-id="8698d-1588">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="8698d-1588">Parameter name</span></span> |  <span data-ttu-id="8698d-1589">パラメーター タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1589">Parameter type</span></span> | <span data-ttu-id="8698d-1590">オプション</span><span class="sxs-lookup"><span data-stu-id="8698d-1590">Optional</span></span> | <span data-ttu-id="8698d-1591">説明</span><span class="sxs-lookup"><span data-stu-id="8698d-1591">Description</span></span> |
| -- | -- | -- | -- |
| <span data-ttu-id="8698d-1592">_workspaceMenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1592">_workspaceMenuItemType</span></span> | <span data-ttu-id="8698d-1593">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="8698d-1593">MenuItemType</span></span> | <span data-ttu-id="8698d-1594">はい</span><span class="sxs-lookup"><span data-stu-id="8698d-1594">True</span></span> | <span data-ttu-id="8698d-1595">workspacesecurity 属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1595">The workspace menu item type for the workspacesecurity attribute</span></span>

#### <a name="return-value"></a><span data-ttu-id="8698d-1596">戻り値</span><span class="sxs-lookup"><span data-stu-id="8698d-1596">Return Value</span></span>

<span data-ttu-id="8698d-1597">ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="8698d-1597">The workspace menu item type for the workspace security attribute</span></span>
