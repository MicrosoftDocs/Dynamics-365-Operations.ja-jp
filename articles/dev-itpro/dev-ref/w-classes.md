---
title: "W クラス"
description: "文字 W で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 55901
ms.assetid: ca08dc94-1481-4ac0-80f4-d092da5c1c90
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 62d632a0bc881c3f310de2e0899e66e6d91f0fc8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="w-classes"></a><span data-ttu-id="7b846-103">W クラス</span><span class="sxs-lookup"><span data-stu-id="7b846-103">W classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b846-104">文字 W で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="7b846-104">System API classes that start with the letter W.</span></span>

<a name="class-webactionmenufunction"></a><span data-ttu-id="7b846-105">クラス WebActionMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b846-105">Class WebActionMenuFunction</span></span>
---------------------------

    class WebActionMenuFunction extends WebMenuFunction

<span data-ttu-id="7b846-106">WebActionMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-106">The WebActionMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-107">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-107">Remarks</span></span>

<span data-ttu-id="7b846-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-109">例</span><span class="sxs-lookup"><span data-stu-id="7b846-109">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-110">Methods</span></span>

| <span data-ttu-id="7b846-111">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-111">Method</span></span>                                                   | <span data-ttu-id="7b846-112">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-112">Description</span></span>                                                                                                 |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-113">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-113">public boolean big(\[boolean value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="7b846-114">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-114">public int correctPermissions(\[int value\])</span></span>             |                                                                                                             |
| <span data-ttu-id="7b846-115">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-115">public int createPermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="7b846-116">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-116">public int deletePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="7b846-117">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-117">public int enumParameter(\[int value\])</span></span>                  | <span data-ttu-id="7b846-118">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-118">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span> |
| <span data-ttu-id="7b846-119">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-119">public EnumId enumTypeParameter(\[EnumId value\])</span></span>        | <span data-ttu-id="7b846-120">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-120">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                     |
| <span data-ttu-id="7b846-121">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-121">public int imageLocation(\[int value\])</span></span>                  |                                                                                                             |
| <span data-ttu-id="7b846-122">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-122">public str linkedPermissionObject(\[str value\])</span></span>         |                                                                                                             |
| <span data-ttu-id="7b846-123">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-123">public str linkedPermissionObjectChild(\[str value\])</span></span>    |                                                                                                             |
| <span data-ttu-id="7b846-124">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-124">public int linkedPermissionType(\[int value\])</span></span>           |                                                                                                             |
| <span data-ttu-id="7b846-125">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-125">public int maintainUserLicense(\[int value\])</span></span>            | <span data-ttu-id="7b846-126">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-126">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="7b846-127">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-127">public boolean multiSelect(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="7b846-128">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-128">public boolean needsRecord(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="7b846-129">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-129">public str normalImage(\[str value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="7b846-130">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-130">public int normalResource(\[int value\])</span></span>                 |                                                                                                             |
| <span data-ttu-id="7b846-131">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-131">public str object(\[str value\])</span></span>                         | <span data-ttu-id="7b846-132">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-132">Gets or sets the object that the MenuFunction class runs.</span></span>                                                   |
| <span data-ttu-id="7b846-133">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-133">public int objectType(\[int value\])</span></span>                     |                                                                                                             |
| <span data-ttu-id="7b846-134">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-134">public Guid origin(\[Guid value\])</span></span>                       |                                                                                                             |
| <span data-ttu-id="7b846-135">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-135">public str parameters(\[str value\])</span></span>                     | <span data-ttu-id="7b846-136">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-136">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>      |
| <span data-ttu-id="7b846-137">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-137">public int readPermissions(\[int value\])</span></span>                |                                                                                                             |
| <span data-ttu-id="7b846-138">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-138">public str reportDesign(\[str value\])</span></span>                   |                                                                                                             |
| <span data-ttu-id="7b846-139">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-139">public int runOn(\[int value\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="7b846-140">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-140">public int updatePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="7b846-141">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-141">public int viewUserLicense(\[int value\])</span></span>                | <span data-ttu-id="7b846-142">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-142">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="7b846-143">::public static void runCalled(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="7b846-143">::public static void runCalled(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="7b846-144">public void AOTrun(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="7b846-144">public void AOTrun(\[xArgs args\])</span></span>                       | <span data-ttu-id="7b846-145">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="7b846-145">Compiles this node and its sub-tree in the Finance and Operations Application Object Tree (AOT).</span></span>             |
| <span data-ttu-id="7b846-146">::public static void runClient(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="7b846-146">::public static void runClient(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="7b846-147">public void run(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="7b846-147">public void run(\[xArgs args\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="7b846-148">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-148">public void new(str name)</span></span>                                | <span data-ttu-id="7b846-149">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-149">Initializes a new instance of the TreeNode class.</span></span>                                                           |
| <span data-ttu-id="7b846-150">::public static void runServer(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="7b846-150">::public static void runServer(str name, \[xArgs args\])</span></span> |                                                                                                             |

### <a name="method-big"></a><span data-ttu-id="7b846-151">メソッド big</span><span class="sxs-lookup"><span data-stu-id="7b846-151">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-152">Parameters</span></span>

<span data-ttu-id="7b846-153">値</span><span class="sxs-lookup"><span data-stu-id="7b846-153">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-154">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="7b846-155">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-155">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-156">Parameters</span></span>

<span data-ttu-id="7b846-157">値</span><span class="sxs-lookup"><span data-stu-id="7b846-157">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-158">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="7b846-159">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-159">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-160">Parameters</span></span>

<span data-ttu-id="7b846-161">値</span><span class="sxs-lookup"><span data-stu-id="7b846-161">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-162">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="7b846-163">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-163">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-164">Parameters</span></span>

<span data-ttu-id="7b846-165">値</span><span class="sxs-lookup"><span data-stu-id="7b846-165">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-166">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="7b846-167">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="7b846-167">Method enumParameter</span></span>

<span data-ttu-id="7b846-168">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-168">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-169">Parameters</span></span>

<span data-ttu-id="7b846-170">値</span><span class="sxs-lookup"><span data-stu-id="7b846-170">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-171">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-171">Return Value</span></span>

<span data-ttu-id="7b846-172">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7b846-172">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="7b846-173">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="7b846-173">Method enumTypeParameter</span></span>

<span data-ttu-id="7b846-174">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-174">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="7b846-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-175">Parameters</span></span>

<span data-ttu-id="7b846-176">値</span><span class="sxs-lookup"><span data-stu-id="7b846-176">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-177">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-177">Return Value</span></span>

<span data-ttu-id="7b846-178">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7b846-178">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="7b846-179">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="7b846-179">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-180">Parameters</span></span>

<span data-ttu-id="7b846-181">値</span><span class="sxs-lookup"><span data-stu-id="7b846-181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-182">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="7b846-183">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="7b846-183">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-184">Parameters</span></span>

<span data-ttu-id="7b846-185">値</span><span class="sxs-lookup"><span data-stu-id="7b846-185">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-186">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-186">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="7b846-187">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="7b846-187">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-188">Parameters</span></span>

<span data-ttu-id="7b846-189">値</span><span class="sxs-lookup"><span data-stu-id="7b846-189">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-190">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-190">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="7b846-191">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="7b846-191">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-192">Parameters</span></span>

<span data-ttu-id="7b846-193">値</span><span class="sxs-lookup"><span data-stu-id="7b846-193">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-194">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="7b846-195">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="7b846-195">Method maintainUserLicense</span></span>

<span data-ttu-id="7b846-196">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-196">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-197">Parameters</span></span>

<span data-ttu-id="7b846-198">値</span><span class="sxs-lookup"><span data-stu-id="7b846-198">value</span></span>  
<span data-ttu-id="7b846-199">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-199">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b846-200">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-200">Return Value</span></span>

<span data-ttu-id="7b846-201">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-201">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="7b846-202">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="7b846-202">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-203">Parameters</span></span>

<span data-ttu-id="7b846-204">値</span><span class="sxs-lookup"><span data-stu-id="7b846-204">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-205">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="7b846-206">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="7b846-206">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-207">Parameters</span></span>

<span data-ttu-id="7b846-208">値</span><span class="sxs-lookup"><span data-stu-id="7b846-208">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-209">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-209">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="7b846-210">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="7b846-210">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-211">Parameters</span></span>

<span data-ttu-id="7b846-212">値</span><span class="sxs-lookup"><span data-stu-id="7b846-212">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-213">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-213">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="7b846-214">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="7b846-214">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-215">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-215">Parameters</span></span>

<span data-ttu-id="7b846-216">値</span><span class="sxs-lookup"><span data-stu-id="7b846-216">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-217">Return Value</span></span>

### <a name="method-object"></a><span data-ttu-id="7b846-218">メソッド object</span><span class="sxs-lookup"><span data-stu-id="7b846-218">Method object</span></span>

<span data-ttu-id="7b846-219">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-219">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-220">Parameters</span></span>

<span data-ttu-id="7b846-221">値</span><span class="sxs-lookup"><span data-stu-id="7b846-221">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-222">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-222">Return Value</span></span>

<span data-ttu-id="7b846-223">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7b846-223">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-224">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-224">Remarks</span></span>

<span data-ttu-id="7b846-225">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-225">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="7b846-226">フォーム</span><span class="sxs-lookup"><span data-stu-id="7b846-226">Form</span></span>
-   <span data-ttu-id="7b846-227">レポート </span><span class="sxs-lookup"><span data-stu-id="7b846-227">Report</span></span>
-   <span data-ttu-id="7b846-228">ジョブ</span><span class="sxs-lookup"><span data-stu-id="7b846-228">Job</span></span>
-   <span data-ttu-id="7b846-229">クラス</span><span class="sxs-lookup"><span data-stu-id="7b846-229">Class</span></span>
-   <span data-ttu-id="7b846-230">クエリ</span><span class="sxs-lookup"><span data-stu-id="7b846-230">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="7b846-231">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="7b846-231">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-232">Parameters</span></span>

<span data-ttu-id="7b846-233">値</span><span class="sxs-lookup"><span data-stu-id="7b846-233">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-234">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-235">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-235">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-236">Parameters</span></span>

<span data-ttu-id="7b846-237">値</span><span class="sxs-lookup"><span data-stu-id="7b846-237">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-238">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-238">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="7b846-239">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="7b846-239">Method parameters</span></span>

<span data-ttu-id="7b846-240">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-240">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-241">Parameters</span></span>

<span data-ttu-id="7b846-242">値</span><span class="sxs-lookup"><span data-stu-id="7b846-242">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-243">Return Value</span></span>

<span data-ttu-id="7b846-244">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="7b846-244">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-245">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-245">Remarks</span></span>

<span data-ttu-id="7b846-246">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="7b846-246">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="7b846-247">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="7b846-247">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="7b846-248">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-248">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-249">Parameters</span></span>

<span data-ttu-id="7b846-250">値</span><span class="sxs-lookup"><span data-stu-id="7b846-250">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-251">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-251">Return Value</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="7b846-252">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="7b846-252">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-253">Parameters</span></span>

<span data-ttu-id="7b846-254">値</span><span class="sxs-lookup"><span data-stu-id="7b846-254">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-255">Return Value</span></span>

### <a name="method-runon"></a><span data-ttu-id="7b846-256">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="7b846-256">Method runOn</span></span>

    public int runOn([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-257">Parameters</span></span>

<span data-ttu-id="7b846-258">値</span><span class="sxs-lookup"><span data-stu-id="7b846-258">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-259">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-259">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="7b846-260">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-260">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-261">Parameters</span></span>

<span data-ttu-id="7b846-262">値</span><span class="sxs-lookup"><span data-stu-id="7b846-262">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-263">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="7b846-264">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="7b846-264">Method viewUserLicense</span></span>

<span data-ttu-id="7b846-265">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-265">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-266">Parameters</span></span>

<span data-ttu-id="7b846-267">値</span><span class="sxs-lookup"><span data-stu-id="7b846-267">value</span></span>  
<span data-ttu-id="7b846-268">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-268">The user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b846-269">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-269">Return Value</span></span>

<span data-ttu-id="7b846-270">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-270">The user license.</span></span>

### <a name="method-runcalled"></a><span data-ttu-id="7b846-271">メソッド runCalled</span><span class="sxs-lookup"><span data-stu-id="7b846-271">Method runCalled</span></span>

    public static void runCalled(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="7b846-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-272">Parameters</span></span>

<span data-ttu-id="7b846-273">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-273">name</span></span>  

<!-- -->

<span data-ttu-id="7b846-274">args</span><span class="sxs-lookup"><span data-stu-id="7b846-274">args</span></span>  

### <a name="method-aotrun"></a><span data-ttu-id="7b846-275">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="7b846-275">Method AOTrun</span></span>

<span data-ttu-id="7b846-276">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="7b846-276">Compiles this node and its sub-tree in the Finance and Operations Application Object Tree (AOT).</span></span>

    public void AOTrun([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="7b846-277">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-277">Parameters</span></span>

<span data-ttu-id="7b846-278">args</span><span class="sxs-lookup"><span data-stu-id="7b846-278">args</span></span>  

### <a name="method-runclient"></a><span data-ttu-id="7b846-279">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="7b846-279">Method runClient</span></span>

    public static void runClient(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="7b846-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-280">Parameters</span></span>

<span data-ttu-id="7b846-281">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-281">name</span></span>  

<!-- -->

<span data-ttu-id="7b846-282">args</span><span class="sxs-lookup"><span data-stu-id="7b846-282">args</span></span>  

### <a name="method-run"></a><span data-ttu-id="7b846-283">メソッド run</span><span class="sxs-lookup"><span data-stu-id="7b846-283">Method run</span></span>

    public void run([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="7b846-284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-284">Parameters</span></span>

<span data-ttu-id="7b846-285">args</span><span class="sxs-lookup"><span data-stu-id="7b846-285">args</span></span>  

### <a name="method-new"></a><span data-ttu-id="7b846-286">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-286">Method new</span></span>

<span data-ttu-id="7b846-287">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-287">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-288">Parameters</span></span>

<span data-ttu-id="7b846-289">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-289">name</span></span>  

### <a name="method-runserver"></a><span data-ttu-id="7b846-290">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="7b846-290">Method runServer</span></span>

    public static void runServer(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="7b846-291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-291">Parameters</span></span>

<span data-ttu-id="7b846-292">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-292">name</span></span>  

<!-- -->

<span data-ttu-id="7b846-293">args</span><span class="sxs-lookup"><span data-stu-id="7b846-293">args</span></span>  

## <a name="class-webcontentitem"></a><span data-ttu-id="7b846-294">クラス WebContentItem</span><span class="sxs-lookup"><span data-stu-id="7b846-294">Class WebContentItem</span></span>
    class WebContentItem extends SecureNode

<span data-ttu-id="7b846-295">WebContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-295">The WebContentItem class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-296">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-296">Remarks</span></span>

<span data-ttu-id="7b846-297">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-297">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-298">例</span><span class="sxs-lookup"><span data-stu-id="7b846-298">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-299">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-299">Methods</span></span>

| <span data-ttu-id="7b846-300">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-300">Method</span></span>                                            | <span data-ttu-id="7b846-301">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-301">Description</span></span>                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-302">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-302">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="7b846-303">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-303">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="7b846-304">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-304">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="7b846-305">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-305">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-306">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-306">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="7b846-307">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-307">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-308">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-308">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="7b846-309">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-309">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="7b846-310">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-310">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="7b846-311">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-311">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="7b846-312">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-312">public str creationTime(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="7b846-313">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-313">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="7b846-314">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-314">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                               |
| <span data-ttu-id="7b846-315">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-315">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="7b846-316">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-316">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                   |
| <span data-ttu-id="7b846-317">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-317">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="7b846-318">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-318">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="7b846-319">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-319">public str label(\[str value\])</span></span>                   | <span data-ttu-id="7b846-320">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-320">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="7b846-321">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-321">public str name(\[str value\])</span></span>                    | <span data-ttu-id="7b846-322">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-322">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-323">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-323">public str object(\[str value\])</span></span>                  | <span data-ttu-id="7b846-324">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-324">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                 |
| <span data-ttu-id="7b846-325">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-325">public int objectType(\[int value\])</span></span>              |                                                                                                                                           |
| <span data-ttu-id="7b846-326">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-326">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="7b846-327">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-327">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="7b846-328">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-328">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="7b846-329">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-329">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                           |

### <a name="method-changedby"></a><span data-ttu-id="7b846-330">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-330">Method changedBy</span></span>

<span data-ttu-id="7b846-331">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-331">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-332">Parameters</span></span>

<span data-ttu-id="7b846-333">値</span><span class="sxs-lookup"><span data-stu-id="7b846-333">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-334">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-334">Return Value</span></span>

<span data-ttu-id="7b846-335">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-335">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-336">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-336">Method changedDate</span></span>

<span data-ttu-id="7b846-337">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-337">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-338">Parameters</span></span>

<span data-ttu-id="7b846-339">値</span><span class="sxs-lookup"><span data-stu-id="7b846-339">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-340">Return Value</span></span>

<span data-ttu-id="7b846-341">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-341">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-342">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-342">Method changedTime</span></span>

<span data-ttu-id="7b846-343">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-343">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-344">Parameters</span></span>

<span data-ttu-id="7b846-345">値</span><span class="sxs-lookup"><span data-stu-id="7b846-345">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-346">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-346">Return Value</span></span>

<span data-ttu-id="7b846-347">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-347">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-348">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-348">Method createdBy</span></span>

<span data-ttu-id="7b846-349">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-349">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-350">Parameters</span></span>

<span data-ttu-id="7b846-351">値</span><span class="sxs-lookup"><span data-stu-id="7b846-351">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-352">Return Value</span></span>

<span data-ttu-id="7b846-353">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-353">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-354">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-354">Method creationDate</span></span>

<span data-ttu-id="7b846-355">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-355">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-356">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-356">Parameters</span></span>

<span data-ttu-id="7b846-357">値</span><span class="sxs-lookup"><span data-stu-id="7b846-357">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-358">Return Value</span></span>

<span data-ttu-id="7b846-359">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-359">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-360">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-360">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-361">Parameters</span></span>

<span data-ttu-id="7b846-362">値</span><span class="sxs-lookup"><span data-stu-id="7b846-362">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-363">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="7b846-364">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="7b846-364">Method enumParameter</span></span>

<span data-ttu-id="7b846-365">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-365">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-366">Parameters</span></span>

<span data-ttu-id="7b846-367">値</span><span class="sxs-lookup"><span data-stu-id="7b846-367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-368">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-368">Return Value</span></span>

<span data-ttu-id="7b846-369">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7b846-369">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="7b846-370">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="7b846-370">Method enumTypeParameter</span></span>

<span data-ttu-id="7b846-371">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-371">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="7b846-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-372">Parameters</span></span>

<span data-ttu-id="7b846-373">値</span><span class="sxs-lookup"><span data-stu-id="7b846-373">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-374">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-374">Return Value</span></span>

<span data-ttu-id="7b846-375">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7b846-375">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="7b846-376">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b846-376">Method helpText</span></span>

<span data-ttu-id="7b846-377">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-377">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-378">Parameters</span></span>

<span data-ttu-id="7b846-379">値</span><span class="sxs-lookup"><span data-stu-id="7b846-379">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-380">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-380">Return Value</span></span>

<span data-ttu-id="7b846-381">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b846-381">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-382">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-382">Remarks</span></span>

<span data-ttu-id="7b846-383">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-383">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7b846-384">ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b846-384">dialog box.</span></span> <span data-ttu-id="7b846-385">ヘルプ テキストは、250文字以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-385">The The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="7b846-386">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b846-386">Method label</span></span>

<span data-ttu-id="7b846-387">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-387">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-388">Parameters</span></span>

<span data-ttu-id="7b846-389">値</span><span class="sxs-lookup"><span data-stu-id="7b846-389">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-390">Return Value</span></span>

<span data-ttu-id="7b846-391">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b846-391">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-392">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-392">Remarks</span></span>

<span data-ttu-id="7b846-393">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-393">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7b846-394">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-394">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-395">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-395">Method name</span></span>

<span data-ttu-id="7b846-396">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-396">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-397">Parameters</span></span>

<span data-ttu-id="7b846-398">値</span><span class="sxs-lookup"><span data-stu-id="7b846-398">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-399">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-399">Return Value</span></span>

<span data-ttu-id="7b846-400">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-400">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-401">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-401">Remarks</span></span>

<span data-ttu-id="7b846-402">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-402">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-403">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-403">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-404">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-404">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-405">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-405">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-406">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-406">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-407">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-407">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-object"></a><span data-ttu-id="7b846-408">メソッド object</span><span class="sxs-lookup"><span data-stu-id="7b846-408">Method object</span></span>

<span data-ttu-id="7b846-409">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-409">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-410">Parameters</span></span>

<span data-ttu-id="7b846-411">値</span><span class="sxs-lookup"><span data-stu-id="7b846-411">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-412">Return Value</span></span>

<span data-ttu-id="7b846-413">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7b846-413">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-414">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-414">Remarks</span></span>

<span data-ttu-id="7b846-415">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-415">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="7b846-416">フォーム</span><span class="sxs-lookup"><span data-stu-id="7b846-416">Form</span></span>
-   <span data-ttu-id="7b846-417">レポート </span><span class="sxs-lookup"><span data-stu-id="7b846-417">Report</span></span>
-   <span data-ttu-id="7b846-418">ジョブ</span><span class="sxs-lookup"><span data-stu-id="7b846-418">Job</span></span>
-   <span data-ttu-id="7b846-419">クラス</span><span class="sxs-lookup"><span data-stu-id="7b846-419">Class</span></span>
-   <span data-ttu-id="7b846-420">クエリ</span><span class="sxs-lookup"><span data-stu-id="7b846-420">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="7b846-421">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="7b846-421">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-422">Parameters</span></span>

<span data-ttu-id="7b846-423">値</span><span class="sxs-lookup"><span data-stu-id="7b846-423">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-424">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-425">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-425">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-426">Parameters</span></span>

<span data-ttu-id="7b846-427">値</span><span class="sxs-lookup"><span data-stu-id="7b846-427">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-428">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-428">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="7b846-429">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="7b846-429">Method parameters</span></span>

<span data-ttu-id="7b846-430">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-430">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-431">Parameters</span></span>

<span data-ttu-id="7b846-432">値</span><span class="sxs-lookup"><span data-stu-id="7b846-432">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-433">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-433">Return Value</span></span>

<span data-ttu-id="7b846-434">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="7b846-434">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-435">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-435">Remarks</span></span>

<span data-ttu-id="7b846-436">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="7b846-436">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="7b846-437">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="7b846-437">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="7b846-438">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="7b846-438">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-439">Parameters</span></span>

<span data-ttu-id="7b846-440">値</span><span class="sxs-lookup"><span data-stu-id="7b846-440">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-441">Return Value</span></span>

## <a name="class-webcontrolnode"></a><span data-ttu-id="7b846-442">クラス webControlNode</span><span class="sxs-lookup"><span data-stu-id="7b846-442">Class webControlNode</span></span>
    class webControlNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="7b846-443">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-443">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-444">例</span><span class="sxs-lookup"><span data-stu-id="7b846-444">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-445">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-445">Methods</span></span>

| <span data-ttu-id="7b846-446">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-446">Method</span></span>                                                        | <span data-ttu-id="7b846-447">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-447">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-448">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="7b846-448">public str AOTgetSource()</span></span>                                     | <span data-ttu-id="7b846-449">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="7b846-449">Returns the source code of this node.</span></span>                                                                                                         |
| <span data-ttu-id="7b846-450">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-450">public str changedBy(\[str value\])</span></span>                           | <span data-ttu-id="7b846-451">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-451">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="7b846-452">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-452">public Date changedDate(\[Date value\])</span></span>                       | <span data-ttu-id="7b846-453">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-453">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-454">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-454">public str changedTime(\[str value\])</span></span>                         | <span data-ttu-id="7b846-455">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-455">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-456">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-456">public str createdBy(\[str value\])</span></span>                           | <span data-ttu-id="7b846-457">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-457">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="7b846-458">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-458">public Date creationDate(\[Date value\])</span></span>                      | <span data-ttu-id="7b846-459">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-459">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="7b846-460">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-460">public str creationTime(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="7b846-461">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-461">public str filename(\[str value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b846-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span><span class="sxs-lookup"><span data-stu-id="7b846-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span></span> | <span data-ttu-id="7b846-463">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7b846-463">Get a list of web controls that are related to this web control.</span></span>                                                                              |
| <span data-ttu-id="7b846-464">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-464">public str helpText(\[str value\])</span></span>                            | <span data-ttu-id="7b846-465">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-465">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="7b846-466">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-466">public str name(\[str value\])</span></span>                                | <span data-ttu-id="7b846-467">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-467">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-468">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-468">public Guid origin(\[Guid value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b846-469">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-469">public str relativePath(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="7b846-470">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-470">public str version(\[str value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="7b846-471">::public static webControlNode createFromFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="7b846-471">::public static webControlNode createFromFile(str fileName)</span></span>   |                                                                                                                                               |
| <span data-ttu-id="7b846-472">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="7b846-472">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>    | <span data-ttu-id="7b846-473">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-473">Sets the source code of this node.</span></span>                                                                                                            |

### <a name="method-aotgetsource"></a><span data-ttu-id="7b846-474">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-474">Method AOTgetSource</span></span>

<span data-ttu-id="7b846-475">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="7b846-475">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="7b846-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-476">Return Value</span></span>

<span data-ttu-id="7b846-477">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="7b846-477">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-478">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-478">Remarks</span></span>

<span data-ttu-id="7b846-479">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-479">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="7b846-480">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-480">Method changedBy</span></span>

<span data-ttu-id="7b846-481">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-481">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-482">Parameters</span></span>

<span data-ttu-id="7b846-483">値</span><span class="sxs-lookup"><span data-stu-id="7b846-483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-484">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-484">Return Value</span></span>

<span data-ttu-id="7b846-485">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-485">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-486">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-486">Method changedDate</span></span>

<span data-ttu-id="7b846-487">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-487">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-488">Parameters</span></span>

<span data-ttu-id="7b846-489">値</span><span class="sxs-lookup"><span data-stu-id="7b846-489">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-490">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-490">Return Value</span></span>

<span data-ttu-id="7b846-491">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-491">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-492">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-492">Method changedTime</span></span>

<span data-ttu-id="7b846-493">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-493">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-494">Parameters</span></span>

<span data-ttu-id="7b846-495">値</span><span class="sxs-lookup"><span data-stu-id="7b846-495">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-496">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-496">Return Value</span></span>

<span data-ttu-id="7b846-497">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-497">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-498">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-498">Method createdBy</span></span>

<span data-ttu-id="7b846-499">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-499">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-500">Parameters</span></span>

<span data-ttu-id="7b846-501">値</span><span class="sxs-lookup"><span data-stu-id="7b846-501">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-502">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-502">Return Value</span></span>

<span data-ttu-id="7b846-503">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-503">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-504">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-504">Method creationDate</span></span>

<span data-ttu-id="7b846-505">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-505">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-506">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-506">Parameters</span></span>

<span data-ttu-id="7b846-507">値</span><span class="sxs-lookup"><span data-stu-id="7b846-507">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-508">Return Value</span></span>

<span data-ttu-id="7b846-509">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-509">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-510">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-510">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-511">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-511">Parameters</span></span>

<span data-ttu-id="7b846-512">値</span><span class="sxs-lookup"><span data-stu-id="7b846-512">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-513">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="7b846-514">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="7b846-514">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-515">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-515">Parameters</span></span>

<span data-ttu-id="7b846-516">値</span><span class="sxs-lookup"><span data-stu-id="7b846-516">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-517">Return Value</span></span>

### <a name="method-getrelatedwebcontrols"></a><span data-ttu-id="7b846-518">メソッド getRelatedWebControls</span><span class="sxs-lookup"><span data-stu-id="7b846-518">Method getRelatedWebControls</span></span>

<span data-ttu-id="7b846-519">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7b846-519">Get a list of web controls that are related to this web control.</span></span>

    public List getRelatedWebControls([boolean firstLevelOnly])

#### <a name="parameters"></a><span data-ttu-id="7b846-520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-520">Parameters</span></span>

<span data-ttu-id="7b846-521">firstLevelOnly</span><span class="sxs-lookup"><span data-stu-id="7b846-521">firstLevelOnly</span></span>  
<span data-ttu-id="7b846-522">Web コントロールの最初のレベルのみがオンになっているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="7b846-522">A value that indicates whether only the first level of web controls is checked.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b846-523">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-523">Return Value</span></span>

<span data-ttu-id="7b846-524">関連する Web コントロールの一覧。</span><span class="sxs-lookup"><span data-stu-id="7b846-524">A list of related web controls.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="7b846-525">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b846-525">Method helpText</span></span>

<span data-ttu-id="7b846-526">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-526">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-527">Parameters</span></span>

<span data-ttu-id="7b846-528">値</span><span class="sxs-lookup"><span data-stu-id="7b846-528">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-529">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-529">Return Value</span></span>

<span data-ttu-id="7b846-530">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b846-530">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-531">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-531">Remarks</span></span>

<span data-ttu-id="7b846-532">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-532">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7b846-533">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7b846-533">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-534">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-534">Method name</span></span>

<span data-ttu-id="7b846-535">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-535">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-536">Parameters</span></span>

<span data-ttu-id="7b846-537">値</span><span class="sxs-lookup"><span data-stu-id="7b846-537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-538">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-538">Return Value</span></span>

<span data-ttu-id="7b846-539">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-539">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-540">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-540">Remarks</span></span>

<span data-ttu-id="7b846-541">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-541">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-542">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-542">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-543">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-543">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-544">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-544">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-545">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-545">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-546">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-546">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-547">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-547">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-548">Parameters</span></span>

<span data-ttu-id="7b846-549">値</span><span class="sxs-lookup"><span data-stu-id="7b846-549">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-550">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-550">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="7b846-551">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="7b846-551">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-552">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-552">Parameters</span></span>

<span data-ttu-id="7b846-553">値</span><span class="sxs-lookup"><span data-stu-id="7b846-553">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-554">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-554">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="7b846-555">メソッド version</span><span class="sxs-lookup"><span data-stu-id="7b846-555">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-556">Parameters</span></span>

<span data-ttu-id="7b846-557">値</span><span class="sxs-lookup"><span data-stu-id="7b846-557">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-558">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-558">Return Value</span></span>

### <a name="method-createfromfile"></a><span data-ttu-id="7b846-559">メソッド createFromFile</span><span class="sxs-lookup"><span data-stu-id="7b846-559">Method createFromFile</span></span>

    public static webControlNode createFromFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="7b846-560">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-560">Parameters</span></span>

<span data-ttu-id="7b846-561">fileName</span><span class="sxs-lookup"><span data-stu-id="7b846-561">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-562">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-562">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="7b846-563">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-563">Method AOTsetSource</span></span>

<span data-ttu-id="7b846-564">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-564">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="7b846-565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-565">Parameters</span></span>

<span data-ttu-id="7b846-566">ソース</span><span class="sxs-lookup"><span data-stu-id="7b846-566">source</span></span>  
<span data-ttu-id="7b846-567">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7b846-567">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="7b846-568">isStatic</span><span class="sxs-lookup"><span data-stu-id="7b846-568">isStatic</span></span>  
<span data-ttu-id="7b846-569">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7b846-569">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-570">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-570">Remarks</span></span>

<span data-ttu-id="7b846-571">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-571">This method is overridden by nodes that have source code.</span></span>

## <a name="class-webdisplaycontentitem"></a><span data-ttu-id="7b846-572">クラス WebDisplayContentItem</span><span class="sxs-lookup"><span data-stu-id="7b846-572">Class WebDisplayContentItem</span></span>
    class WebDisplayContentItem extends WebContentItem

<span data-ttu-id="7b846-573">WebDisplayContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-573">The WebDisplayContentItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-574">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-574">Remarks</span></span>

<span data-ttu-id="7b846-575">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-575">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="7b846-576">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-576">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-577">例</span><span class="sxs-lookup"><span data-stu-id="7b846-577">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-578">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-578">Methods</span></span>

| <span data-ttu-id="7b846-579">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-579">Method</span></span>                    | <span data-ttu-id="7b846-580">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-580">Description</span></span>                          |
|---------------------------|--------------------------------------|
| <span data-ttu-id="7b846-581">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-581">public void new(str name)</span></span> | <span data-ttu-id="7b846-582">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b846-582">Creates a new WebDisplayContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="7b846-583">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-583">Method new</span></span>

<span data-ttu-id="7b846-584">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b846-584">Creates a new WebDisplayContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-585">Parameters</span></span>

<span data-ttu-id="7b846-586">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-586">name</span></span>  

## <a name="class-webletitem"></a><span data-ttu-id="7b846-587">クラス WebletItem</span><span class="sxs-lookup"><span data-stu-id="7b846-587">Class WebletItem</span></span>
    class WebletItem extends SecureNode

<span data-ttu-id="7b846-588">WebletItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-588">The WebletItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-589">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-589">Remarks</span></span>

<span data-ttu-id="7b846-590">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-590">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="7b846-591">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-591">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-592">例</span><span class="sxs-lookup"><span data-stu-id="7b846-592">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-593">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-593">Methods</span></span>

| <span data-ttu-id="7b846-594">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-594">Method</span></span>                                            | <span data-ttu-id="7b846-595">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-595">Description</span></span>                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-596">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-596">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="7b846-597">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-597">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="7b846-598">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-598">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="7b846-599">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-599">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-600">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-600">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="7b846-601">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-601">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-602">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-602">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="7b846-603">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-603">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="7b846-604">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-604">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="7b846-605">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-605">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="7b846-606">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-606">public str creationTime(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="7b846-607">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-607">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="7b846-608">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-608">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                                   |
| <span data-ttu-id="7b846-609">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-609">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="7b846-610">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-610">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="7b846-611">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-611">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="7b846-612">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-612">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="7b846-613">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-613">public str label(\[str value\])</span></span>                   | <span data-ttu-id="7b846-614">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-614">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="7b846-615">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-615">public str name(\[str value\])</span></span>                    | <span data-ttu-id="7b846-616">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-616">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-617">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-617">public str object(\[str value\])</span></span>                  | <span data-ttu-id="7b846-618">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-618">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                     |
| <span data-ttu-id="7b846-619">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-619">public int objectType(\[int value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="7b846-620">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-620">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="7b846-621">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-621">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="7b846-622">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-622">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                        |
| <span data-ttu-id="7b846-623">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-623">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="7b846-624">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-624">public void new(str name)</span></span>                         | <span data-ttu-id="7b846-625">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-625">Microsoft internal use only.</span></span>                                                                                                                  |

### <a name="method-changedby"></a><span data-ttu-id="7b846-626">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-626">Method changedBy</span></span>

<span data-ttu-id="7b846-627">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-627">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-628">Parameters</span></span>

<span data-ttu-id="7b846-629">値</span><span class="sxs-lookup"><span data-stu-id="7b846-629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-630">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-630">Return Value</span></span>

<span data-ttu-id="7b846-631">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-631">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-632">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-632">Method changedDate</span></span>

<span data-ttu-id="7b846-633">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-633">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-634">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-634">Parameters</span></span>

<span data-ttu-id="7b846-635">値</span><span class="sxs-lookup"><span data-stu-id="7b846-635">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-636">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-636">Return Value</span></span>

<span data-ttu-id="7b846-637">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-637">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-638">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-638">Method changedTime</span></span>

<span data-ttu-id="7b846-639">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-639">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-640">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-640">Parameters</span></span>

<span data-ttu-id="7b846-641">値</span><span class="sxs-lookup"><span data-stu-id="7b846-641">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-642">Return Value</span></span>

<span data-ttu-id="7b846-643">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-643">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-644">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-644">Method createdBy</span></span>

<span data-ttu-id="7b846-645">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-645">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-646">Parameters</span></span>

<span data-ttu-id="7b846-647">値</span><span class="sxs-lookup"><span data-stu-id="7b846-647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-648">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-648">Return Value</span></span>

<span data-ttu-id="7b846-649">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-649">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-650">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-650">Method creationDate</span></span>

<span data-ttu-id="7b846-651">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-651">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-652">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-652">Parameters</span></span>

<span data-ttu-id="7b846-653">値</span><span class="sxs-lookup"><span data-stu-id="7b846-653">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-654">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-654">Return Value</span></span>

<span data-ttu-id="7b846-655">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-655">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-656">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-656">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-657">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-657">Parameters</span></span>

<span data-ttu-id="7b846-658">値</span><span class="sxs-lookup"><span data-stu-id="7b846-658">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-659">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="7b846-660">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="7b846-660">Method enumParameter</span></span>

<span data-ttu-id="7b846-661">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-661">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-662">Parameters</span></span>

<span data-ttu-id="7b846-663">値</span><span class="sxs-lookup"><span data-stu-id="7b846-663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-664">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-664">Return Value</span></span>

<span data-ttu-id="7b846-665">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7b846-665">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="7b846-666">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="7b846-666">Method enumTypeParameter</span></span>

<span data-ttu-id="7b846-667">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-667">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="7b846-668">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-668">Parameters</span></span>

<span data-ttu-id="7b846-669">値</span><span class="sxs-lookup"><span data-stu-id="7b846-669">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-670">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-670">Return Value</span></span>

<span data-ttu-id="7b846-671">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7b846-671">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="7b846-672">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b846-672">Method helpText</span></span>

<span data-ttu-id="7b846-673">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-673">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-674">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-674">Parameters</span></span>

<span data-ttu-id="7b846-675">値</span><span class="sxs-lookup"><span data-stu-id="7b846-675">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-676">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-676">Return Value</span></span>

<span data-ttu-id="7b846-677">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b846-677">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-678">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-678">Remarks</span></span>

<span data-ttu-id="7b846-679">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-679">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7b846-680">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7b846-680">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="7b846-681">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b846-681">Method label</span></span>

<span data-ttu-id="7b846-682">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-682">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-683">Parameters</span></span>

<span data-ttu-id="7b846-684">値</span><span class="sxs-lookup"><span data-stu-id="7b846-684">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-685">Return Value</span></span>

<span data-ttu-id="7b846-686">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b846-686">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-687">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-687">Remarks</span></span>

<span data-ttu-id="7b846-688">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-688">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7b846-689">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-689">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-690">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-690">Method name</span></span>

<span data-ttu-id="7b846-691">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-691">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-692">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-692">Parameters</span></span>

<span data-ttu-id="7b846-693">値</span><span class="sxs-lookup"><span data-stu-id="7b846-693">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-694">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-694">Return Value</span></span>

<span data-ttu-id="7b846-695">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-695">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-696">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-696">Remarks</span></span>

<span data-ttu-id="7b846-697">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-697">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-698">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-698">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-699">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-699">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-700">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-700">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-701">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-701">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-702">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-702">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

### <a name="method-object"></a><span data-ttu-id="7b846-703">メソッド object</span><span class="sxs-lookup"><span data-stu-id="7b846-703">Method object</span></span>

<span data-ttu-id="7b846-704">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-704">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-705">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-705">Parameters</span></span>

<span data-ttu-id="7b846-706">値</span><span class="sxs-lookup"><span data-stu-id="7b846-706">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-707">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-707">Return Value</span></span>

<span data-ttu-id="7b846-708">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7b846-708">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-709">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-709">Remarks</span></span>

<span data-ttu-id="7b846-710">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-710">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="7b846-711">フォーム。</span><span class="sxs-lookup"><span data-stu-id="7b846-711">Form.</span></span>
-   <span data-ttu-id="7b846-712">レポート。</span><span class="sxs-lookup"><span data-stu-id="7b846-712">Report.</span></span>
-   <span data-ttu-id="7b846-713">ジョブ。</span><span class="sxs-lookup"><span data-stu-id="7b846-713">Job.</span></span>
-   <span data-ttu-id="7b846-714">クラス。</span><span class="sxs-lookup"><span data-stu-id="7b846-714">Class.</span></span>
-   <span data-ttu-id="7b846-715">クエリ。</span><span class="sxs-lookup"><span data-stu-id="7b846-715">Query.</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="7b846-716">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="7b846-716">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-717">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-717">Parameters</span></span>

<span data-ttu-id="7b846-718">値</span><span class="sxs-lookup"><span data-stu-id="7b846-718">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-719">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-719">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-720">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-720">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-721">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-721">Parameters</span></span>

<span data-ttu-id="7b846-722">値</span><span class="sxs-lookup"><span data-stu-id="7b846-722">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-723">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-723">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="7b846-724">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="7b846-724">Method parameters</span></span>

<span data-ttu-id="7b846-725">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-725">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-726">Parameters</span></span>

<span data-ttu-id="7b846-727">値</span><span class="sxs-lookup"><span data-stu-id="7b846-727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-728">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-728">Return Value</span></span>

<span data-ttu-id="7b846-729">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="7b846-729">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-730">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-730">Remarks</span></span>

<span data-ttu-id="7b846-731">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="7b846-731">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="7b846-732">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="7b846-732">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="7b846-733">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="7b846-733">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-734">Parameters</span></span>

<span data-ttu-id="7b846-735">値</span><span class="sxs-lookup"><span data-stu-id="7b846-735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-736">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-736">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="7b846-737">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-737">Method new</span></span>

<span data-ttu-id="7b846-738">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-738">Microsoft internal use only.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-739">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-739">Parameters</span></span>

<span data-ttu-id="7b846-740">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-740">name</span></span>  

## <a name="class-weblistdefnode"></a><span data-ttu-id="7b846-741">クラス webListDefNode</span><span class="sxs-lookup"><span data-stu-id="7b846-741">Class webListDefNode</span></span>
    class webListDefNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="7b846-742">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-742">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-743">例</span><span class="sxs-lookup"><span data-stu-id="7b846-743">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-744">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-744">Methods</span></span>

| <span data-ttu-id="7b846-745">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-745">Method</span></span>                                                     | <span data-ttu-id="7b846-746">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-746">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-747">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="7b846-747">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="7b846-748">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="7b846-748">Returns the source code of this node.</span></span>                                                                                                     |
| <span data-ttu-id="7b846-749">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-749">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="7b846-750">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-750">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="7b846-751">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-751">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="7b846-752">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-752">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-753">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-753">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="7b846-754">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-754">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-755">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-755">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="7b846-756">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-756">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="7b846-757">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-757">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="7b846-758">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-758">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="7b846-759">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-759">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="7b846-760">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-760">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="7b846-761">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-761">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="7b846-762">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-762">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="7b846-763">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-763">public str name(\[str value\])</span></span>                             | <span data-ttu-id="7b846-764">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-764">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-765">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-765">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="7b846-766">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-766">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="7b846-767">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-767">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="7b846-768">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-768">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="7b846-769">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-769">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="7b846-770">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="7b846-770">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="7b846-771">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-771">Sets the source code of this node.</span></span>                                                                                                        |
| <span data-ttu-id="7b846-772">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-772">public void new(str name)</span></span>                                  | <span data-ttu-id="7b846-773">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-773">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |

### <a name="method-aotgetsource"></a><span data-ttu-id="7b846-774">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-774">Method AOTgetSource</span></span>

<span data-ttu-id="7b846-775">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="7b846-775">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="7b846-776">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-776">Return Value</span></span>

<span data-ttu-id="7b846-777">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="7b846-777">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-778">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-778">Remarks</span></span>

<span data-ttu-id="7b846-779">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-779">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="7b846-780">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-780">Method changedBy</span></span>

<span data-ttu-id="7b846-781">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-781">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-782">Parameters</span></span>

<span data-ttu-id="7b846-783">値</span><span class="sxs-lookup"><span data-stu-id="7b846-783">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-784">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-784">Return Value</span></span>

<span data-ttu-id="7b846-785">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-785">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-786">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-786">Method changedDate</span></span>

<span data-ttu-id="7b846-787">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-787">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-788">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-788">Parameters</span></span>

<span data-ttu-id="7b846-789">値</span><span class="sxs-lookup"><span data-stu-id="7b846-789">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-790">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-790">Return Value</span></span>

<span data-ttu-id="7b846-791">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-791">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-792">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-792">Method changedTime</span></span>

<span data-ttu-id="7b846-793">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-793">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-794">Parameters</span></span>

<span data-ttu-id="7b846-795">値</span><span class="sxs-lookup"><span data-stu-id="7b846-795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-796">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-796">Return Value</span></span>

<span data-ttu-id="7b846-797">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-797">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-798">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-798">Method createdBy</span></span>

<span data-ttu-id="7b846-799">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-799">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-800">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-800">Parameters</span></span>

<span data-ttu-id="7b846-801">値</span><span class="sxs-lookup"><span data-stu-id="7b846-801">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-802">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-802">Return Value</span></span>

<span data-ttu-id="7b846-803">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-803">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-804">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-804">Method creationDate</span></span>

<span data-ttu-id="7b846-805">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-805">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-806">Parameters</span></span>

<span data-ttu-id="7b846-807">値</span><span class="sxs-lookup"><span data-stu-id="7b846-807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-808">Return Value</span></span>

<span data-ttu-id="7b846-809">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-809">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-810">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-810">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-811">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-811">Parameters</span></span>

<span data-ttu-id="7b846-812">値</span><span class="sxs-lookup"><span data-stu-id="7b846-812">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-813">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-813">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="7b846-814">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b846-814">Method helpText</span></span>

<span data-ttu-id="7b846-815">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-815">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-816">Parameters</span></span>

<span data-ttu-id="7b846-817">値</span><span class="sxs-lookup"><span data-stu-id="7b846-817">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-818">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-818">Return Value</span></span>

<span data-ttu-id="7b846-819">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b846-819">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-820">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-820">Remarks</span></span>

<span data-ttu-id="7b846-821">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-821">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="7b846-822">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7b846-822">The help text must not exceed 250 characters.</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="7b846-823">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="7b846-823">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-824">Parameters</span></span>

<span data-ttu-id="7b846-825">値</span><span class="sxs-lookup"><span data-stu-id="7b846-825">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-826">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-827">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-827">Method name</span></span>

<span data-ttu-id="7b846-828">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-828">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-829">Parameters</span></span>

<span data-ttu-id="7b846-830">値</span><span class="sxs-lookup"><span data-stu-id="7b846-830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-831">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-831">Return Value</span></span>

<span data-ttu-id="7b846-832">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-832">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-833">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-833">Remarks</span></span>

<span data-ttu-id="7b846-834">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-834">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-835">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-835">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-836">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-836">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-837">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-837">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-838">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-838">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-839">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-839">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-840">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-840">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-841">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-841">Parameters</span></span>

<span data-ttu-id="7b846-842">値</span><span class="sxs-lookup"><span data-stu-id="7b846-842">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-843">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-843">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="7b846-844">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="7b846-844">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-845">Parameters</span></span>

<span data-ttu-id="7b846-846">値</span><span class="sxs-lookup"><span data-stu-id="7b846-846">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-847">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="7b846-848">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="7b846-848">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-849">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-849">Parameters</span></span>

<span data-ttu-id="7b846-850">値</span><span class="sxs-lookup"><span data-stu-id="7b846-850">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-851">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="7b846-852">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="7b846-852">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-853">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-853">Parameters</span></span>

<span data-ttu-id="7b846-854">値</span><span class="sxs-lookup"><span data-stu-id="7b846-854">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-855">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="7b846-856">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="7b846-856">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-857">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-857">Parameters</span></span>

<span data-ttu-id="7b846-858">値</span><span class="sxs-lookup"><span data-stu-id="7b846-858">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-859">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="7b846-860">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-860">Method AOTsetSource</span></span>

<span data-ttu-id="7b846-861">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-861">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="7b846-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-862">Parameters</span></span>

<span data-ttu-id="7b846-863">ソース</span><span class="sxs-lookup"><span data-stu-id="7b846-863">source</span></span>  
<span data-ttu-id="7b846-864">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7b846-864">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="7b846-865">isStatic</span><span class="sxs-lookup"><span data-stu-id="7b846-865">isStatic</span></span>  
<span data-ttu-id="7b846-866">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7b846-866">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-867">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-867">Remarks</span></span>

<span data-ttu-id="7b846-868">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-868">This method is overridden by nodes that have source code.</span></span>

### <a name="method-new"></a><span data-ttu-id="7b846-869">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-869">Method new</span></span>

<span data-ttu-id="7b846-870">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-870">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-871">Parameters</span></span>

<span data-ttu-id="7b846-872">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-872">name</span></span>  

## <a name="class-webmanagedcontentitem"></a><span data-ttu-id="7b846-873">クラス WebManagedContentItem</span><span class="sxs-lookup"><span data-stu-id="7b846-873">Class WebManagedContentItem</span></span>
    class WebManagedContentItem extends WebContentItem

<span data-ttu-id="7b846-874">このクラスを使用して、コンテンツをページに追加するために EP で使用する webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b846-874">This class is used to create a webManagedContentItem to use in EP for adding content to pages.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-875">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-875">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-876">例</span><span class="sxs-lookup"><span data-stu-id="7b846-876">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-877">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-877">Methods</span></span>

| <span data-ttu-id="7b846-878">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-878">Method</span></span>                    | <span data-ttu-id="7b846-879">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-879">Description</span></span>                                                 |
|---------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7b846-880">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-880">public void new(str name)</span></span> | <span data-ttu-id="7b846-881">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b846-881">Create a new webManagedContentItem with the passed in name.</span></span> |

### <a name="method-new"></a><span data-ttu-id="7b846-882">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-882">Method new</span></span>

<span data-ttu-id="7b846-883">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b846-883">Create a new webManagedContentItem with the passed in name.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-884">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-884">Parameters</span></span>

<span data-ttu-id="7b846-885">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-885">name</span></span>  
<span data-ttu-id="7b846-886">新しい webManagedContentItem に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7b846-886">Name for the new webManagedContentItem.</span></span>

## <a name="class-webmenu"></a><span data-ttu-id="7b846-887">クラス WebMenu</span><span class="sxs-lookup"><span data-stu-id="7b846-887">Class WebMenu</span></span>
    class WebMenu extends TreeNode

<span data-ttu-id="7b846-888">WebMenu クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-888">The WebMenu class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-889">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-889">Remarks</span></span>

<span data-ttu-id="7b846-890">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-890">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-891">例</span><span class="sxs-lookup"><span data-stu-id="7b846-891">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-892">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-892">Methods</span></span>

| <span data-ttu-id="7b846-893">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-893">Method</span></span>                                                                   | <span data-ttu-id="7b846-894">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-894">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-895">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-895">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="7b846-896">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-896">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="7b846-897">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-897">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="7b846-898">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-898">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-899">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-899">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="7b846-900">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-900">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="7b846-902">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-902">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="7b846-903">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-903">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="7b846-904">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-904">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="7b846-905">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-905">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="7b846-906">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-906">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="7b846-907">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-907">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="7b846-908">public boolean highlightSelected(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-908">public boolean highlightSelected(\[boolean value\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="7b846-909">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-909">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="7b846-910">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-910">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="7b846-911">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-911">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="7b846-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                               |
| <span data-ttu-id="7b846-913">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="7b846-913">public str menuName()</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="7b846-914">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-914">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="7b846-915">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-915">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-916">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-916">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="7b846-917">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-917">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="7b846-918">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-918">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b846-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="7b846-920">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-920">public boolean setCompany(\[boolean value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="7b846-921">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-921">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="7b846-922">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-922">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b846-923">public void addSeparator()</span><span class="sxs-lookup"><span data-stu-id="7b846-923">public void addSeparator()</span></span>                                               |                                                                                                                                               |
| <span data-ttu-id="7b846-924">public void makeMenu(Object outputClass)</span><span class="sxs-lookup"><span data-stu-id="7b846-924">public void makeMenu(Object outputClass)</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b846-925">public void addSubmenu(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-925">public void addSubmenu(str name)</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="7b846-926">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="7b846-926">public void new(str Name)</span></span>                                                | <span data-ttu-id="7b846-927">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-927">Initializes a new instance of the TreeNode class.</span></span>                                                                                             |
| <span data-ttu-id="7b846-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="7b846-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="7b846-929">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-929">Method changedBy</span></span>

<span data-ttu-id="7b846-930">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-930">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-931">Parameters</span></span>

<span data-ttu-id="7b846-932">値</span><span class="sxs-lookup"><span data-stu-id="7b846-932">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-933">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-933">Return Value</span></span>

<span data-ttu-id="7b846-934">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-934">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-935">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-935">Method changedDate</span></span>

<span data-ttu-id="7b846-936">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-936">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-937">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-937">Parameters</span></span>

<span data-ttu-id="7b846-938">値</span><span class="sxs-lookup"><span data-stu-id="7b846-938">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-939">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-939">Return Value</span></span>

<span data-ttu-id="7b846-940">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-940">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-941">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-941">Method changedTime</span></span>

<span data-ttu-id="7b846-942">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-942">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-943">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-943">Parameters</span></span>

<span data-ttu-id="7b846-944">値</span><span class="sxs-lookup"><span data-stu-id="7b846-944">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-945">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-945">Return Value</span></span>

<span data-ttu-id="7b846-946">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-946">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="7b846-947">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="7b846-947">Method configurationKey</span></span>

<span data-ttu-id="7b846-948">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-948">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="7b846-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-949">Parameters</span></span>

<span data-ttu-id="7b846-950">値</span><span class="sxs-lookup"><span data-stu-id="7b846-950">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-951">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-951">Return Value</span></span>

<span data-ttu-id="7b846-952">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="7b846-952">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-953">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-953">Remarks</span></span>

<span data-ttu-id="7b846-954">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b846-954">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="7b846-955">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="7b846-955">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-956">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-956">Method createdBy</span></span>

<span data-ttu-id="7b846-957">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-957">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-958">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-958">Parameters</span></span>

<span data-ttu-id="7b846-959">値</span><span class="sxs-lookup"><span data-stu-id="7b846-959">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-960">Return Value</span></span>

<span data-ttu-id="7b846-961">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-961">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-962">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-962">Method creationDate</span></span>

<span data-ttu-id="7b846-963">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-963">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-964">Parameters</span></span>

<span data-ttu-id="7b846-965">値</span><span class="sxs-lookup"><span data-stu-id="7b846-965">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-966">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-966">Return Value</span></span>

<span data-ttu-id="7b846-967">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-967">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-968">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-968">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-969">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-969">Parameters</span></span>

<span data-ttu-id="7b846-970">値</span><span class="sxs-lookup"><span data-stu-id="7b846-970">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-971">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-971">Return Value</span></span>

### <a name="method-highlightselected"></a><span data-ttu-id="7b846-972">メソッド highlightSelected</span><span class="sxs-lookup"><span data-stu-id="7b846-972">Method highlightSelected</span></span>

    public boolean highlightSelected([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-973">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-973">Parameters</span></span>

<span data-ttu-id="7b846-974">値</span><span class="sxs-lookup"><span data-stu-id="7b846-974">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-975">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="7b846-976">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b846-976">Method label</span></span>

<span data-ttu-id="7b846-977">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-977">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-978">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-978">Parameters</span></span>

<span data-ttu-id="7b846-979">値</span><span class="sxs-lookup"><span data-stu-id="7b846-979">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-980">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-980">Return Value</span></span>

<span data-ttu-id="7b846-981">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b846-981">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-982">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-982">Remarks</span></span>

<span data-ttu-id="7b846-983">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-983">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7b846-984">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-984">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="7b846-985">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="7b846-985">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-986">Parameters</span></span>

<span data-ttu-id="7b846-987">値</span><span class="sxs-lookup"><span data-stu-id="7b846-987">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-988">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-988">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="7b846-989">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="7b846-989">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="7b846-990">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-990">Parameters</span></span>

<span data-ttu-id="7b846-991">値</span><span class="sxs-lookup"><span data-stu-id="7b846-991">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-992">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-992">Return Value</span></span>

### <a name="method-menuname"></a><span data-ttu-id="7b846-993">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="7b846-993">Method menuName</span></span>

    public str menuName()

#### <a name="return-value"></a><span data-ttu-id="7b846-994">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-994">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-995">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-995">Method name</span></span>

<span data-ttu-id="7b846-996">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-996">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-997">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-997">Parameters</span></span>

<span data-ttu-id="7b846-998">値</span><span class="sxs-lookup"><span data-stu-id="7b846-998">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-999">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-999">Return Value</span></span>

<span data-ttu-id="7b846-1000">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1000">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1001">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1001">Remarks</span></span>

<span data-ttu-id="7b846-1002">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1002">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-1003">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1003">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-1004">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-1004">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-1005">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1005">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-1006">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1006">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-1007">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1007">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="7b846-1008">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="7b846-1008">Method neededAccessLevel</span></span>

<span data-ttu-id="7b846-1009">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1009">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1010">Parameters</span></span>

<span data-ttu-id="7b846-1011">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1011">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1012">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1012">Return Value</span></span>

<span data-ttu-id="7b846-1013">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b846-1013">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1014">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1014">Remarks</span></span>

<span data-ttu-id="7b846-1015">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7b846-1015">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="7b846-1016">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="7b846-1016">AccessType::NoAccess</span></span>
-   <span data-ttu-id="7b846-1017">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="7b846-1017">AccessType::View</span></span>
-   <span data-ttu-id="7b846-1018">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="7b846-1018">AccessType::Edit</span></span>
-   <span data-ttu-id="7b846-1019">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="7b846-1019">AccessType::Add</span></span>
-   <span data-ttu-id="7b846-1020">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="7b846-1020">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-1021">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-1021">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1022">Parameters</span></span>

<span data-ttu-id="7b846-1023">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1023">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1024">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1024">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="7b846-1025">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="7b846-1025">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1026">Parameters</span></span>

<span data-ttu-id="7b846-1027">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1027">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1028">Return Value</span></span>

### <a name="method-setcompany"></a><span data-ttu-id="7b846-1029">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="7b846-1029">Method setCompany</span></span>

    public boolean setCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1030">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1030">Parameters</span></span>

<span data-ttu-id="7b846-1031">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1031">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1032">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="7b846-1033">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="7b846-1033">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1034">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1034">Parameters</span></span>

<span data-ttu-id="7b846-1035">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1035">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1036">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1036">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="7b846-1037">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="7b846-1037">Method webTarget</span></span>

    public str webTarget([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1038">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1038">Parameters</span></span>

<span data-ttu-id="7b846-1039">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1039">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1040">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1040">Return Value</span></span>

### <a name="method-addseparator"></a><span data-ttu-id="7b846-1041">メソッド addSeparator</span><span class="sxs-lookup"><span data-stu-id="7b846-1041">Method addSeparator</span></span>

    public void addSeparator()

### <a name="method-makemenu"></a><span data-ttu-id="7b846-1042">メソッド makeMenu</span><span class="sxs-lookup"><span data-stu-id="7b846-1042">Method makeMenu</span></span>

    public void makeMenu(Object outputClass)

#### <a name="parameters"></a><span data-ttu-id="7b846-1043">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1043">Parameters</span></span>

<span data-ttu-id="7b846-1044">outputClass</span><span class="sxs-lookup"><span data-stu-id="7b846-1044">outputClass</span></span>  

### <a name="method-addsubmenu"></a><span data-ttu-id="7b846-1045">メソッド addSubmenu</span><span class="sxs-lookup"><span data-stu-id="7b846-1045">Method addSubmenu</span></span>

    public void addSubmenu(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-1046">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1046">Parameters</span></span>

<span data-ttu-id="7b846-1047">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-1047">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="7b846-1048">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-1048">Method new</span></span>

<span data-ttu-id="7b846-1049">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1049">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="7b846-1050">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1050">Parameters</span></span>

<span data-ttu-id="7b846-1051">氏名</span><span class="sxs-lookup"><span data-stu-id="7b846-1051">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="7b846-1052">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="7b846-1052">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="7b846-1053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1053">Parameters</span></span>

<span data-ttu-id="7b846-1054">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b846-1054">webMenuFunction</span></span>  

## <a name="class-webmenufunction"></a><span data-ttu-id="7b846-1055">クラス WebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b846-1055">Class WebMenuFunction</span></span>
    class WebMenuFunction extends SecureNode

<span data-ttu-id="7b846-1056">WebMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1056">The WebMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-1057">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1057">Remarks</span></span>

<span data-ttu-id="7b846-1058">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1058">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1059">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1059">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1060">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1060">Methods</span></span>

| <span data-ttu-id="7b846-1061">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1061">Method</span></span>                                                                                           | <span data-ttu-id="7b846-1062">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1062">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-1063">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1063">public str changedBy(\[str value\])</span></span>                                                              | <span data-ttu-id="7b846-1064">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1064">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="7b846-1065">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1065">public Date changedDate(\[Date value\])</span></span>                                                          | <span data-ttu-id="7b846-1066">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1066">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-1067">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1067">public str changedTime(\[str value\])</span></span>                                                            | <span data-ttu-id="7b846-1068">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1068">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b846-1069">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1069">public str createdBy(\[str value\])</span></span>                                                              | <span data-ttu-id="7b846-1070">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1070">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="7b846-1071">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1071">public Date creationDate(\[Date value\])</span></span>                                                         | <span data-ttu-id="7b846-1072">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1072">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="7b846-1073">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1073">public str creationTime(\[str value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="7b846-1074">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1074">public str helpText(\[str value\])</span></span>                                                               | <span data-ttu-id="7b846-1075">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1075">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="7b846-1076">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1076">public str label(\[str value\])</span></span>                                                                  | <span data-ttu-id="7b846-1077">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1077">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="7b846-1078">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1078">public str name(\[str value\])</span></span>                                                                   | <span data-ttu-id="7b846-1079">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1079">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-1080">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1080">public Guid origin(\[Guid value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="7b846-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span><span class="sxs-lookup"><span data-stu-id="7b846-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span></span> |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="7b846-1082">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1082">Method changedBy</span></span>

<span data-ttu-id="7b846-1083">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1083">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1084">Parameters</span></span>

<span data-ttu-id="7b846-1085">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1085">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1086">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1086">Return Value</span></span>

<span data-ttu-id="7b846-1087">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1087">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-1088">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1088">Method changedDate</span></span>

<span data-ttu-id="7b846-1089">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1089">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1090">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1090">Parameters</span></span>

<span data-ttu-id="7b846-1091">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1091">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1092">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1092">Return Value</span></span>

<span data-ttu-id="7b846-1093">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1093">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-1094">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1094">Method changedTime</span></span>

<span data-ttu-id="7b846-1095">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1095">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1096">Parameters</span></span>

<span data-ttu-id="7b846-1097">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1097">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1098">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1098">Return Value</span></span>

<span data-ttu-id="7b846-1099">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-1099">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-1100">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1100">Method createdBy</span></span>

<span data-ttu-id="7b846-1101">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1101">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1102">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1102">Parameters</span></span>

<span data-ttu-id="7b846-1103">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1103">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1104">Return Value</span></span>

<span data-ttu-id="7b846-1105">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1105">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-1106">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1106">Method creationDate</span></span>

<span data-ttu-id="7b846-1107">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1107">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1108">Parameters</span></span>

<span data-ttu-id="7b846-1109">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1109">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1110">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1110">Return Value</span></span>

<span data-ttu-id="7b846-1111">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1111">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-1112">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1112">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1113">Parameters</span></span>

<span data-ttu-id="7b846-1114">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1114">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1115">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1115">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="7b846-1116">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b846-1116">Method helpText</span></span>

<span data-ttu-id="7b846-1117">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1117">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1118">Parameters</span></span>

<span data-ttu-id="7b846-1119">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1119">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1120">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1120">Return Value</span></span>

<span data-ttu-id="7b846-1121">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b846-1121">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1122">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1122">Remarks</span></span>

<span data-ttu-id="7b846-1123">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1123">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7b846-1124">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1124">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="7b846-1125">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b846-1125">Method label</span></span>

<span data-ttu-id="7b846-1126">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1126">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1127">Parameters</span></span>

<span data-ttu-id="7b846-1128">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1128">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1129">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1129">Return Value</span></span>

<span data-ttu-id="7b846-1130">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b846-1130">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1131">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1131">Remarks</span></span>

<span data-ttu-id="7b846-1132">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1132">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7b846-1133">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1133">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-1134">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-1134">Method name</span></span>

<span data-ttu-id="7b846-1135">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1135">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1136">Parameters</span></span>

<span data-ttu-id="7b846-1137">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1137">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1138">Return Value</span></span>

<span data-ttu-id="7b846-1139">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1139">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1140">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1140">Remarks</span></span>

<span data-ttu-id="7b846-1141">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1141">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-1142">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1142">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-1143">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-1143">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-1144">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1144">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-1145">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1145">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-1146">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1146">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-1147">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-1147">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1148">Parameters</span></span>

<span data-ttu-id="7b846-1149">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1149">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1150">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1150">Return Value</span></span>

### <a name="method-createwebmenufunction"></a><span data-ttu-id="7b846-1151">メソッド createWebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b846-1151">Method createWebMenuFunction</span></span>

    public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)

#### <a name="parameters"></a><span data-ttu-id="7b846-1152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1152">Parameters</span></span>

<span data-ttu-id="7b846-1153">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-1153">name</span></span>  

<!-- -->

<span data-ttu-id="7b846-1154">webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="7b846-1154">webMenuItemType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1155">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1155">Return Value</span></span>

## <a name="class-webmenuitem"></a><span data-ttu-id="7b846-1156">クラス WebMenuItem</span><span class="sxs-lookup"><span data-stu-id="7b846-1156">Class WebMenuItem</span></span>
    class WebMenuItem extends TreeNode

<span data-ttu-id="7b846-1157">WebMenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1157">The WebMenuItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-1158">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1158">Remarks</span></span>

<span data-ttu-id="7b846-1159">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1159">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="7b846-1160">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1160">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1161">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1161">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1162">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1162">Methods</span></span>

| <span data-ttu-id="7b846-1163">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1163">Method</span></span>                                                         | <span data-ttu-id="7b846-1164">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1164">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-1165">public str label()</span><span class="sxs-lookup"><span data-stu-id="7b846-1165">public str label()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="7b846-1166">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1166">public str menuItemName(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="7b846-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="7b846-1168">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1168">public str name(\[str value\])</span></span>                                 | <span data-ttu-id="7b846-1169">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1169">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-1170">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1170">public str parameters(\[str value\])</span></span>                           | <span data-ttu-id="7b846-1171">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1171">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="7b846-1172">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1172">public boolean showParentModule(\[boolean value\])</span></span>             |                                                                                                                                           |

### <a name="method-label"></a><span data-ttu-id="7b846-1173">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b846-1173">Method label</span></span>

    public str label()

#### <a name="return-value"></a><span data-ttu-id="7b846-1174">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1174">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="7b846-1175">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="7b846-1175">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1176">Parameters</span></span>

<span data-ttu-id="7b846-1177">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1177">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1178">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1178">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="7b846-1179">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="7b846-1179">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1180">Parameters</span></span>

<span data-ttu-id="7b846-1181">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1182">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1182">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-1183">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-1183">Method name</span></span>

<span data-ttu-id="7b846-1184">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1184">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1185">Parameters</span></span>

<span data-ttu-id="7b846-1186">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1186">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1187">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1187">Return Value</span></span>

<span data-ttu-id="7b846-1188">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1188">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1189">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1189">Remarks</span></span>

<span data-ttu-id="7b846-1190">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1190">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-1191">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1191">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-1192">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-1192">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-1193">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1193">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-1194">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1194">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-1195">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1195">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-parameters"></a><span data-ttu-id="7b846-1196">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="7b846-1196">Method parameters</span></span>

<span data-ttu-id="7b846-1197">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1197">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1198">Parameters</span></span>

<span data-ttu-id="7b846-1199">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1199">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1200">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1200">Return Value</span></span>

<span data-ttu-id="7b846-1201">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="7b846-1201">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1202">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1202">Remarks</span></span>

<span data-ttu-id="7b846-1203">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1203">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="7b846-1204">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1204">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="7b846-1205">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="7b846-1205">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1206">Parameters</span></span>

<span data-ttu-id="7b846-1207">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1207">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1208">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1208">Return Value</span></span>

## <a name="class-webmodulenode"></a><span data-ttu-id="7b846-1209">クラス webModuleNode</span><span class="sxs-lookup"><span data-stu-id="7b846-1209">Class webModuleNode</span></span>
    class webModuleNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="7b846-1210">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1210">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1211">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1211">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1212">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1212">Methods</span></span>

| <span data-ttu-id="7b846-1213">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1213">Method</span></span>                                                                   | <span data-ttu-id="7b846-1214">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1214">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-1215">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1215">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="7b846-1216">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1216">Gets or sets the name of the user who last changed the application object.</span></span>                                                                     |
| <span data-ttu-id="7b846-1217">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1217">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="7b846-1218">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1218">Gets or sets the date an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="7b846-1219">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1219">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="7b846-1220">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1220">Gets or sets the time an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="7b846-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="7b846-1222">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1222">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                            |
| <span data-ttu-id="7b846-1223">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1223">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="7b846-1224">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1224">Gets or sets the name of the user who created the application object.</span></span>                                                                          |
| <span data-ttu-id="7b846-1225">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1225">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="7b846-1226">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1226">Gets or sets the date an application object was created.</span></span>                                                                                       |
| <span data-ttu-id="7b846-1227">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1227">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="7b846-1228">public boolean extendedDataSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1228">public boolean extendedDataSecurity(\[boolean value\])</span></span>                   |                                                                                                                                                |
| <span data-ttu-id="7b846-1229">public boolean inheritNavigation(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1229">public boolean inheritNavigation(\[boolean value\])</span></span>                      |                                                                                                                                                |
| <span data-ttu-id="7b846-1230">public boolean inheritPermissions(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1230">public boolean inheritPermissions(\[boolean value\])</span></span>                     |                                                                                                                                                |
| <span data-ttu-id="7b846-1231">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1231">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="7b846-1232">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1232">Gets or sets the label for a control.</span></span>                                                                                                          |
| <span data-ttu-id="7b846-1233">public str masterPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1233">public str masterPage(\[str value\])</span></span>                                     |                                                                                                                                                |
| <span data-ttu-id="7b846-1234">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1234">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="7b846-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                                |
| <span data-ttu-id="7b846-1236">public str moduleName()</span><span class="sxs-lookup"><span data-stu-id="7b846-1236">public str moduleName()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="7b846-1237">public str modulePath()</span><span class="sxs-lookup"><span data-stu-id="7b846-1237">public str modulePath()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="7b846-1238">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1238">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="7b846-1239">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1239">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-1240">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1240">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="7b846-1241">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1241">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                        |
| <span data-ttu-id="7b846-1242">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1242">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="7b846-1243">public boolean publicModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1243">public boolean publicModule(\[boolean value\])</span></span>                           |                                                                                                                                                |
| <span data-ttu-id="7b846-1244">public str quickLaunch(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1244">public str quickLaunch(\[str value\])</span></span>                                    |                                                                                                                                                |
| <span data-ttu-id="7b846-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                                |
| <span data-ttu-id="7b846-1246">public boolean showLink(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1246">public boolean showLink(\[boolean value\])</span></span>                               |                                                                                                                                                |
| <span data-ttu-id="7b846-1247">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1247">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                                |
| <span data-ttu-id="7b846-1248">public void addSubModule(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-1248">public void addSubModule(str name)</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="7b846-1249">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="7b846-1249">public void new(str Name)</span></span>                                                | <span data-ttu-id="7b846-1250">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1250">Initializes a new instance of the TreeNode class.</span></span>                                                                                              |
| <span data-ttu-id="7b846-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="7b846-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                                |

### <a name="method-changedby"></a><span data-ttu-id="7b846-1252">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1252">Method changedBy</span></span>

<span data-ttu-id="7b846-1253">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1253">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1254">Parameters</span></span>

<span data-ttu-id="7b846-1255">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1255">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1256">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1256">Return Value</span></span>

<span data-ttu-id="7b846-1257">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1257">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-1258">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1258">Method changedDate</span></span>

<span data-ttu-id="7b846-1259">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1259">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1260">Parameters</span></span>

<span data-ttu-id="7b846-1261">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1261">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1262">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1262">Return Value</span></span>

<span data-ttu-id="7b846-1263">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1263">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-1264">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1264">Method changedTime</span></span>

<span data-ttu-id="7b846-1265">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1265">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1266">Parameters</span></span>

<span data-ttu-id="7b846-1267">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1267">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1268">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1268">Return Value</span></span>

<span data-ttu-id="7b846-1269">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-1269">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="7b846-1270">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="7b846-1270">Method configurationKey</span></span>

<span data-ttu-id="7b846-1271">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1271">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1272">Parameters</span></span>

<span data-ttu-id="7b846-1273">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1273">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1274">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1274">Return Value</span></span>

<span data-ttu-id="7b846-1275">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="7b846-1275">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1276">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1276">Remarks</span></span>

<span data-ttu-id="7b846-1277">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1277">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="7b846-1278">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1278">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-1279">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1279">Method createdBy</span></span>

<span data-ttu-id="7b846-1280">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1280">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1281">Parameters</span></span>

<span data-ttu-id="7b846-1282">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1282">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1283">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1283">Return Value</span></span>

<span data-ttu-id="7b846-1284">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1284">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-1285">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1285">Method creationDate</span></span>

<span data-ttu-id="7b846-1286">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1286">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1287">Parameters</span></span>

<span data-ttu-id="7b846-1288">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1288">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1289">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1289">Return Value</span></span>

<span data-ttu-id="7b846-1290">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1290">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-1291">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1291">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1292">Parameters</span></span>

<span data-ttu-id="7b846-1293">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1293">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1294">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1294">Return Value</span></span>

### <a name="method-extendeddatasecurity"></a><span data-ttu-id="7b846-1295">メソッド extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="7b846-1295">Method extendedDataSecurity</span></span>

    public boolean extendedDataSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1296">Parameters</span></span>

<span data-ttu-id="7b846-1297">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1297">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1298">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1298">Return Value</span></span>

### <a name="method-inheritnavigation"></a><span data-ttu-id="7b846-1299">メソッド inheritNavigation</span><span class="sxs-lookup"><span data-stu-id="7b846-1299">Method inheritNavigation</span></span>

    public boolean inheritNavigation([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1300">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1300">Parameters</span></span>

<span data-ttu-id="7b846-1301">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1301">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1302">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1302">Return Value</span></span>

### <a name="method-inheritpermissions"></a><span data-ttu-id="7b846-1303">メソッド inheritPermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-1303">Method inheritPermissions</span></span>

    public boolean inheritPermissions([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1304">Parameters</span></span>

<span data-ttu-id="7b846-1305">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1305">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1306">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1306">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="7b846-1307">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b846-1307">Method label</span></span>

<span data-ttu-id="7b846-1308">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1308">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1309">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1309">Parameters</span></span>

<span data-ttu-id="7b846-1310">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1310">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1311">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1311">Return Value</span></span>

<span data-ttu-id="7b846-1312">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b846-1312">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1313">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1313">Remarks</span></span>

<span data-ttu-id="7b846-1314">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1314">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7b846-1315">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1315">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-masterpage"></a><span data-ttu-id="7b846-1316">メソッド masterPage</span><span class="sxs-lookup"><span data-stu-id="7b846-1316">Method masterPage</span></span>

    public str masterPage([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1317">Parameters</span></span>

<span data-ttu-id="7b846-1318">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1319">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1319">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="7b846-1320">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="7b846-1320">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1321">Parameters</span></span>

<span data-ttu-id="7b846-1322">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1322">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1323">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1323">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="7b846-1324">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="7b846-1324">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1325">Parameters</span></span>

<span data-ttu-id="7b846-1326">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1326">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1327">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1327">Return Value</span></span>

### <a name="method-modulename"></a><span data-ttu-id="7b846-1328">メソッド moduleName</span><span class="sxs-lookup"><span data-stu-id="7b846-1328">Method moduleName</span></span>

    public str moduleName()

#### <a name="return-value"></a><span data-ttu-id="7b846-1329">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1329">Return Value</span></span>

### <a name="method-modulepath"></a><span data-ttu-id="7b846-1330">メソッド modulePath</span><span class="sxs-lookup"><span data-stu-id="7b846-1330">Method modulePath</span></span>

    public str modulePath()

#### <a name="return-value"></a><span data-ttu-id="7b846-1331">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1331">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-1332">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-1332">Method name</span></span>

<span data-ttu-id="7b846-1333">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1333">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1334">Parameters</span></span>

<span data-ttu-id="7b846-1335">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1335">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1336">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1336">Return Value</span></span>

<span data-ttu-id="7b846-1337">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1337">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1338">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1338">Remarks</span></span>

<span data-ttu-id="7b846-1339">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1339">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-1340">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1340">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-1341">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-1341">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-1342">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1342">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-1343">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1343">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-1344">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1344">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="7b846-1345">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="7b846-1345">Method neededAccessLevel</span></span>

<span data-ttu-id="7b846-1346">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1346">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1347">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1347">Parameters</span></span>

<span data-ttu-id="7b846-1348">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1348">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1349">Return Value</span></span>

<span data-ttu-id="7b846-1350">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b846-1350">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1351">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1351">Remarks</span></span>

<span data-ttu-id="7b846-1352">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7b846-1352">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="7b846-1353">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="7b846-1353">AccessType::NoAccess</span></span>
-   <span data-ttu-id="7b846-1354">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="7b846-1354">AccessType::View</span></span>
-   <span data-ttu-id="7b846-1355">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="7b846-1355">AccessType::Edit</span></span>
-   <span data-ttu-id="7b846-1356">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="7b846-1356">AccessType::Add</span></span>
-   <span data-ttu-id="7b846-1357">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="7b846-1357">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-1358">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-1358">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1359">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1359">Parameters</span></span>

<span data-ttu-id="7b846-1360">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1360">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1361">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1361">Return Value</span></span>

### <a name="method-publicmodule"></a><span data-ttu-id="7b846-1362">メソッド publicModule</span><span class="sxs-lookup"><span data-stu-id="7b846-1362">Method publicModule</span></span>

    public boolean publicModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1363">Parameters</span></span>

<span data-ttu-id="7b846-1364">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1364">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1365">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1365">Return Value</span></span>

### <a name="method-quicklaunch"></a><span data-ttu-id="7b846-1366">メソッド quickLaunch</span><span class="sxs-lookup"><span data-stu-id="7b846-1366">Method quickLaunch</span></span>

    public str quickLaunch([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1367">Parameters</span></span>

<span data-ttu-id="7b846-1368">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1368">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1369">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1369">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="7b846-1370">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="7b846-1370">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1371">Parameters</span></span>

<span data-ttu-id="7b846-1372">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1372">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1373">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1373">Return Value</span></span>

### <a name="method-showlink"></a><span data-ttu-id="7b846-1374">メソッド showLink</span><span class="sxs-lookup"><span data-stu-id="7b846-1374">Method showLink</span></span>

    public boolean showLink([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1375">Parameters</span></span>

<span data-ttu-id="7b846-1376">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1376">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1377">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1377">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="7b846-1378">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="7b846-1378">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1379">Parameters</span></span>

<span data-ttu-id="7b846-1380">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1380">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1381">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1381">Return Value</span></span>

### <a name="method-addsubmodule"></a><span data-ttu-id="7b846-1382">メソッド addSubModule</span><span class="sxs-lookup"><span data-stu-id="7b846-1382">Method addSubModule</span></span>

    public void addSubModule(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-1383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1383">Parameters</span></span>

<span data-ttu-id="7b846-1384">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-1384">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="7b846-1385">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-1385">Method new</span></span>

<span data-ttu-id="7b846-1386">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1386">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="7b846-1387">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1387">Parameters</span></span>

<span data-ttu-id="7b846-1388">氏名</span><span class="sxs-lookup"><span data-stu-id="7b846-1388">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="7b846-1389">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="7b846-1389">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="7b846-1390">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1390">Parameters</span></span>

<span data-ttu-id="7b846-1391">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b846-1391">webMenuFunction</span></span>  

## <a name="class-weboutputcontentitem"></a><span data-ttu-id="7b846-1392">クラス WebOutputContentItem</span><span class="sxs-lookup"><span data-stu-id="7b846-1392">Class WebOutputContentItem</span></span>
    class WebOutputContentItem extends WebContentItem

<span data-ttu-id="7b846-1393">このクラスは、x++ の WebOutputContentItem を表します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1393">This class represents a WebOutputContentItem in x++.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-1394">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1394">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1395">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1395">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1396">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1396">Methods</span></span>

| <span data-ttu-id="7b846-1397">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1397">Method</span></span>                    | <span data-ttu-id="7b846-1398">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1398">Description</span></span>                         |
|---------------------------|-------------------------------------|
| <span data-ttu-id="7b846-1399">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-1399">public void new(str name)</span></span> | <span data-ttu-id="7b846-1400">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1400">Creates a new WebOutputContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="7b846-1401">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-1401">Method new</span></span>

<span data-ttu-id="7b846-1402">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1402">Creates a new WebOutputContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-1403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1403">Parameters</span></span>

<span data-ttu-id="7b846-1404">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-1404">name</span></span>  

## <a name="class-webpagedefnode"></a><span data-ttu-id="7b846-1405">クラス webPageDefNode</span><span class="sxs-lookup"><span data-stu-id="7b846-1405">Class webPageDefNode</span></span>
    class webPageDefNode extends TreeNode

<span data-ttu-id="7b846-1406">webPageDefNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1406">The webPageDefNode class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-1407">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1407">Remarks</span></span>

<span data-ttu-id="7b846-1408">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1408">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="7b846-1409">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1409">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1410">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1410">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1411">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1411">Methods</span></span>

| <span data-ttu-id="7b846-1412">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1412">Method</span></span>                                                     | <span data-ttu-id="7b846-1413">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1413">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-1414">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="7b846-1414">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="7b846-1415">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1415">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="7b846-1416">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1416">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="7b846-1417">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1417">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="7b846-1418">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1418">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="7b846-1419">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1419">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-1420">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1420">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="7b846-1421">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1421">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-1422">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1422">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="7b846-1423">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1423">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="7b846-1424">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1424">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="7b846-1425">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1425">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="7b846-1426">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1426">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="7b846-1427">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1427">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="7b846-1428">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1428">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="7b846-1429">public str imageResource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1429">public str imageResource(\[str value\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="7b846-1430">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1430">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="7b846-1431">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1431">public str name(\[str value\])</span></span>                             | <span data-ttu-id="7b846-1432">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1432">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-1433">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1433">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="7b846-1434">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1434">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="7b846-1435">public str parentPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1435">public str parentPage(\[str value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="7b846-1436">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1436">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="7b846-1437">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1437">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="7b846-1438">public boolean useContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1438">public boolean useContext(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="7b846-1439">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1439">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="7b846-1440">public str wSSHelpTopic(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1440">public str wSSHelpTopic(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="7b846-1441">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-1441">public void new(str name)</span></span>                                  | <span data-ttu-id="7b846-1442">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="7b846-1442">Creates a new webPageDefNode.</span></span>                                                                                                             |
| <span data-ttu-id="7b846-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="7b846-1444">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1444">Set the source of the webPageDefNode to the given string.</span></span>                                                                                 |

### <a name="method-aotgetsource"></a><span data-ttu-id="7b846-1445">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-1445">Method AOTgetSource</span></span>

<span data-ttu-id="7b846-1446">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1446">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="7b846-1447">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1447">Return Value</span></span>

<span data-ttu-id="7b846-1448">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="7b846-1448">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1449">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1449">Remarks</span></span>

<span data-ttu-id="7b846-1450">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1450">This method is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="7b846-1451">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1451">Method changedBy</span></span>

<span data-ttu-id="7b846-1452">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1452">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1453">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1453">Parameters</span></span>

<span data-ttu-id="7b846-1454">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1454">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1455">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1455">Return Value</span></span>

<span data-ttu-id="7b846-1456">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1456">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-1457">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1457">Method changedDate</span></span>

<span data-ttu-id="7b846-1458">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1458">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1459">Parameters</span></span>

<span data-ttu-id="7b846-1460">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1460">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1461">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1461">Return Value</span></span>

<span data-ttu-id="7b846-1462">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1462">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-1463">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1463">Method changedTime</span></span>

<span data-ttu-id="7b846-1464">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1464">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1465">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1465">Parameters</span></span>

<span data-ttu-id="7b846-1466">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1466">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1467">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1467">Return Value</span></span>

<span data-ttu-id="7b846-1468">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-1468">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-1469">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1469">Method createdBy</span></span>

<span data-ttu-id="7b846-1470">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1470">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1471">Parameters</span></span>

<span data-ttu-id="7b846-1472">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1472">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1473">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1473">Return Value</span></span>

<span data-ttu-id="7b846-1474">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1474">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-1475">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1475">Method creationDate</span></span>

<span data-ttu-id="7b846-1476">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1476">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1477">Parameters</span></span>

<span data-ttu-id="7b846-1478">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1478">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1479">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1479">Return Value</span></span>

<span data-ttu-id="7b846-1480">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1480">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-1481">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1481">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1482">Parameters</span></span>

<span data-ttu-id="7b846-1483">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1484">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1484">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="7b846-1485">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b846-1485">Method helpText</span></span>

<span data-ttu-id="7b846-1486">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1486">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1487">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1487">Parameters</span></span>

<span data-ttu-id="7b846-1488">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1488">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1489">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1489">Return Value</span></span>

<span data-ttu-id="7b846-1490">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b846-1490">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1491">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1491">Remarks</span></span>

<span data-ttu-id="7b846-1492">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1492">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7b846-1493">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1493">The help text must not exceed 250 characters.</span></span>

### <a name="method-imageresource"></a><span data-ttu-id="7b846-1494">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="7b846-1494">Method imageResource</span></span>

    public str imageResource([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1495">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1495">Parameters</span></span>

<span data-ttu-id="7b846-1496">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1496">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1497">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1497">Return Value</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="7b846-1498">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="7b846-1498">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1499">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1499">Parameters</span></span>

<span data-ttu-id="7b846-1500">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1500">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1501">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-1502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-1502">Method name</span></span>

<span data-ttu-id="7b846-1503">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1503">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1504">Parameters</span></span>

<span data-ttu-id="7b846-1505">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1505">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1506">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1506">Return Value</span></span>

<span data-ttu-id="7b846-1507">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1507">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1508">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1508">Remarks</span></span>

<span data-ttu-id="7b846-1509">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1509">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-1510">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1510">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-1511">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-1511">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-1512">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1512">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-1513">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1513">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-1514">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1514">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-1515">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-1515">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1516">Parameters</span></span>

<span data-ttu-id="7b846-1517">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1517">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1518">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1518">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="7b846-1519">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="7b846-1519">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1520">Parameters</span></span>

<span data-ttu-id="7b846-1521">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1521">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1522">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1522">Return Value</span></span>

### <a name="method-parentpage"></a><span data-ttu-id="7b846-1523">メソッド parentPage</span><span class="sxs-lookup"><span data-stu-id="7b846-1523">Method parentPage</span></span>

    public str parentPage([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1524">Parameters</span></span>

<span data-ttu-id="7b846-1525">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1525">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1526">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1526">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="7b846-1527">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="7b846-1527">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1528">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1528">Parameters</span></span>

<span data-ttu-id="7b846-1529">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1529">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1530">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1530">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="7b846-1531">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="7b846-1531">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1532">Parameters</span></span>

<span data-ttu-id="7b846-1533">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1533">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1534">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1534">Return Value</span></span>

### <a name="method-usecontext"></a><span data-ttu-id="7b846-1535">メソッド useContext</span><span class="sxs-lookup"><span data-stu-id="7b846-1535">Method useContext</span></span>

    public boolean useContext([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1536">Parameters</span></span>

<span data-ttu-id="7b846-1537">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1538">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1538">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="7b846-1539">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="7b846-1539">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1540">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1540">Parameters</span></span>

<span data-ttu-id="7b846-1541">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1541">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1542">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1542">Return Value</span></span>

### <a name="method-wsshelptopic"></a><span data-ttu-id="7b846-1543">メソッド wSSHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b846-1543">Method wSSHelpTopic</span></span>

    public str wSSHelpTopic([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1544">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1544">Parameters</span></span>

<span data-ttu-id="7b846-1545">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1545">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1546">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1546">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="7b846-1547">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-1547">Method new</span></span>

<span data-ttu-id="7b846-1548">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="7b846-1548">Creates a new webPageDefNode.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-1549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1549">Parameters</span></span>

<span data-ttu-id="7b846-1550">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-1550">name</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="7b846-1551">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-1551">Method AOTsetSource</span></span>

<span data-ttu-id="7b846-1552">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1552">Set the source of the webPageDefNode to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="7b846-1553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1553">Parameters</span></span>

<span data-ttu-id="7b846-1554">ソース</span><span class="sxs-lookup"><span data-stu-id="7b846-1554">source</span></span>  
<span data-ttu-id="7b846-1555">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="7b846-1555">Optional parameter marking if the source provided is static.</span></span>

<!-- -->

<span data-ttu-id="7b846-1556">isStatic</span><span class="sxs-lookup"><span data-stu-id="7b846-1556">isStatic</span></span>  
<span data-ttu-id="7b846-1557">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="7b846-1557">Optional parameter marking if the source provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1558">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1558">Remarks</span></span>

<span data-ttu-id="7b846-1559">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1559">This method is overridden by nodes which have source code.</span></span>

## <a name="class-webstaticfilenode"></a><span data-ttu-id="7b846-1560">クラス webStaticFileNode</span><span class="sxs-lookup"><span data-stu-id="7b846-1560">Class webStaticFileNode</span></span>
    class webStaticFileNode extends TreeNode

<span data-ttu-id="7b846-1561">webStaticFileNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1561">The webStaticFileNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-1562">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1562">Remarks</span></span>

<span data-ttu-id="7b846-1563">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1563">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1564">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1564">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1565">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1565">Methods</span></span>

| <span data-ttu-id="7b846-1566">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1566">Method</span></span>                                                     | <span data-ttu-id="7b846-1567">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1567">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-1568">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="7b846-1568">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="7b846-1569">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1569">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="7b846-1570">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1570">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="7b846-1571">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1571">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="7b846-1572">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1572">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="7b846-1573">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1573">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-1574">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1574">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="7b846-1575">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1575">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="7b846-1576">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1576">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="7b846-1577">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1577">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="7b846-1578">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1578">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="7b846-1579">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1579">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="7b846-1580">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1580">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="7b846-1581">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1581">public str filename(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="7b846-1582">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1582">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="7b846-1583">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1583">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="7b846-1584">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1584">public str name(\[str value\])</span></span>                             | <span data-ttu-id="7b846-1585">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1585">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="7b846-1586">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1586">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="7b846-1587">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1587">public str relativePath(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="7b846-1588">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1588">public str version(\[str value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="7b846-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="7b846-1590">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1590">Sets the source of the static file node to the given string.</span></span>                                                                              |

### <a name="method-aotgetsource"></a><span data-ttu-id="7b846-1591">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-1591">Method AOTgetSource</span></span>

<span data-ttu-id="7b846-1592">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1592">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="7b846-1593">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1593">Return Value</span></span>

<span data-ttu-id="7b846-1594">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="7b846-1594">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1595">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1595">Remarks</span></span>

<span data-ttu-id="7b846-1596">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1596">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="7b846-1597">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1597">Method changedBy</span></span>

<span data-ttu-id="7b846-1598">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1598">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1599">Parameters</span></span>

<span data-ttu-id="7b846-1600">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1600">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1601">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1601">Return Value</span></span>

<span data-ttu-id="7b846-1602">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1602">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="7b846-1603">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1603">Method changedDate</span></span>

<span data-ttu-id="7b846-1604">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1604">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1605">Parameters</span></span>

<span data-ttu-id="7b846-1606">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1606">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1607">Return Value</span></span>

<span data-ttu-id="7b846-1608">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1608">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="7b846-1609">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1609">Method changedTime</span></span>

<span data-ttu-id="7b846-1610">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1610">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1611">Parameters</span></span>

<span data-ttu-id="7b846-1612">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1612">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1613">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1613">Return Value</span></span>

<span data-ttu-id="7b846-1614">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b846-1614">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="7b846-1615">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b846-1615">Method createdBy</span></span>

<span data-ttu-id="7b846-1616">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1616">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1617">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1617">Parameters</span></span>

<span data-ttu-id="7b846-1618">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1618">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1619">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1619">Return Value</span></span>

<span data-ttu-id="7b846-1620">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1620">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="7b846-1621">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b846-1621">Method creationDate</span></span>

<span data-ttu-id="7b846-1622">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1622">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1623">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1623">Parameters</span></span>

<span data-ttu-id="7b846-1624">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1624">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1625">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1625">Return Value</span></span>

<span data-ttu-id="7b846-1626">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b846-1626">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="7b846-1627">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b846-1627">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1628">Parameters</span></span>

<span data-ttu-id="7b846-1629">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1630">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1630">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="7b846-1631">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="7b846-1631">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1632">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1632">Parameters</span></span>

<span data-ttu-id="7b846-1633">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1633">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1634">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1634">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="7b846-1635">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b846-1635">Method helpText</span></span>

<span data-ttu-id="7b846-1636">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1636">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1637">Parameters</span></span>

<span data-ttu-id="7b846-1638">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1638">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1639">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1639">Return Value</span></span>

<span data-ttu-id="7b846-1640">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b846-1640">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1641">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1641">Remarks</span></span>

<span data-ttu-id="7b846-1642">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1642">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7b846-1643">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1643">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="7b846-1644">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b846-1644">Method name</span></span>

<span data-ttu-id="7b846-1645">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1645">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1646">Parameters</span></span>

<span data-ttu-id="7b846-1647">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1648">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1648">Return Value</span></span>

<span data-ttu-id="7b846-1649">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b846-1649">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1650">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1650">Remarks</span></span>

<span data-ttu-id="7b846-1651">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1651">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b846-1652">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1652">Begins with a letter.</span></span>
-   <span data-ttu-id="7b846-1653">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b846-1653">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b846-1654">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1654">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b846-1655">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1655">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b846-1656">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b846-1656">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-1657">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-1657">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1658">Parameters</span></span>

<span data-ttu-id="7b846-1659">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1659">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1660">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1660">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="7b846-1661">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="7b846-1661">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1662">Parameters</span></span>

<span data-ttu-id="7b846-1663">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1664">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1664">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="7b846-1665">メソッド version</span><span class="sxs-lookup"><span data-stu-id="7b846-1665">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1666">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1666">Parameters</span></span>

<span data-ttu-id="7b846-1667">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1667">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1668">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1668">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="7b846-1669">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="7b846-1669">Method AOTsetSource</span></span>

<span data-ttu-id="7b846-1670">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1670">Sets the source of the static file node to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="7b846-1671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1671">Parameters</span></span>

<span data-ttu-id="7b846-1672">ソース</span><span class="sxs-lookup"><span data-stu-id="7b846-1672">source</span></span>  
<span data-ttu-id="7b846-1673">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="7b846-1673">An optional parameter that marks whether the source that is provided is static.</span></span>

<!-- -->

<span data-ttu-id="7b846-1674">isStatic</span><span class="sxs-lookup"><span data-stu-id="7b846-1674">isStatic</span></span>  
<span data-ttu-id="7b846-1675">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="7b846-1675">An optional parameter that marks whether the source that is provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1676">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1676">Remarks</span></span>

<span data-ttu-id="7b846-1677">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1677">This method is overridden by nodes that have source code.</span></span>

## <a name="class-weburlmenufunction"></a><span data-ttu-id="7b846-1678">クラス WebUrlMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b846-1678">Class WebUrlMenuFunction</span></span>
    class WebUrlMenuFunction extends WebMenuFunction

<span data-ttu-id="7b846-1679">WebUrlMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b846-1679">The WebUrlMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="7b846-1680">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1680">Remarks</span></span>

<span data-ttu-id="7b846-1681">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1681">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1682">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1682">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1683">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1683">Methods</span></span>

| <span data-ttu-id="7b846-1684">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1684">Method</span></span>                                                | <span data-ttu-id="7b846-1685">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1685">Description</span></span>                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b846-1686">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1686">public boolean big(\[boolean value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="7b846-1687">public int closeDialogBehavior(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1687">public int closeDialogBehavior(\[int value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="7b846-1688">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1688">public int correctPermissions(\[int value\])</span></span>          |                                                                                                        |
| <span data-ttu-id="7b846-1689">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1689">public int createPermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="7b846-1690">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1690">public int deletePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="7b846-1691">public boolean hideActionPane(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1691">public boolean hideActionPane(\[boolean value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="7b846-1692">public boolean homePage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1692">public boolean homePage(\[boolean value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="7b846-1693">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1693">public int imageLocation(\[int value\])</span></span>               |                                                                                                        |
| <span data-ttu-id="7b846-1694">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1694">public str linkedPermissionObject(\[str value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="7b846-1695">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1695">public str linkedPermissionObjectChild(\[str value\])</span></span> |                                                                                                        |
| <span data-ttu-id="7b846-1696">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1696">public int linkedPermissionType(\[int value\])</span></span>        |                                                                                                        |
| <span data-ttu-id="7b846-1697">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1697">public int maintainUserLicense(\[int value\])</span></span>         | <span data-ttu-id="7b846-1698">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-1698">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="7b846-1699">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1699">public boolean multiSelect(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="7b846-1700">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1700">public boolean needsRecord(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="7b846-1701">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1701">public str normalImage(\[str value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="7b846-1702">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1702">public int normalResource(\[int value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="7b846-1703">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1703">public Guid origin(\[Guid value\])</span></span>                    |                                                                                                        |
| <span data-ttu-id="7b846-1704">public str pageDefinition(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1704">public str pageDefinition(\[str value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="7b846-1705">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1705">public str parameters(\[str value\])</span></span>                  | <span data-ttu-id="7b846-1706">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1706">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span> |
| <span data-ttu-id="7b846-1707">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1707">public int readPermissions(\[int value\])</span></span>             |                                                                                                        |
| <span data-ttu-id="7b846-1708">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1708">public int updatePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="7b846-1709">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1709">public str uRL(\[str value\])</span></span>                         |                                                                                                        |
| <span data-ttu-id="7b846-1710">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1710">public int viewUserLicense(\[int value\])</span></span>             | <span data-ttu-id="7b846-1711">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-1711">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="7b846-1712">public int windowMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1712">public int windowMode(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="7b846-1713">public str windowParameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1713">public str windowParameters(\[str value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="7b846-1714">public int windowSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1714">public int windowSize(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="7b846-1715">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7b846-1715">public void new(str name)</span></span>                             | <span data-ttu-id="7b846-1716">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1716">Initializes a new instance of the TreeNode class.</span></span>                                                      |

### <a name="method-big"></a><span data-ttu-id="7b846-1717">メソッド big</span><span class="sxs-lookup"><span data-stu-id="7b846-1717">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1718">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1718">Parameters</span></span>

<span data-ttu-id="7b846-1719">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1719">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1720">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1720">Return Value</span></span>

### <a name="method-closedialogbehavior"></a><span data-ttu-id="7b846-1721">メソッド closeDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="7b846-1721">Method closeDialogBehavior</span></span>

    public int closeDialogBehavior([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1722">Parameters</span></span>

<span data-ttu-id="7b846-1723">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1723">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1724">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1724">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="7b846-1725">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-1725">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1726">Parameters</span></span>

<span data-ttu-id="7b846-1727">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1728">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1728">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="7b846-1729">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-1729">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1730">Parameters</span></span>

<span data-ttu-id="7b846-1731">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1731">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1732">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1732">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="7b846-1733">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-1733">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1734">Parameters</span></span>

<span data-ttu-id="7b846-1735">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1736">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1736">Return Value</span></span>

### <a name="method-hideactionpane"></a><span data-ttu-id="7b846-1737">メソッド hideActionPane</span><span class="sxs-lookup"><span data-stu-id="7b846-1737">Method hideActionPane</span></span>

    public boolean hideActionPane([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1738">Parameters</span></span>

<span data-ttu-id="7b846-1739">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1739">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1740">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1740">Return Value</span></span>

### <a name="method-homepage"></a><span data-ttu-id="7b846-1741">メソッド homePage</span><span class="sxs-lookup"><span data-stu-id="7b846-1741">Method homePage</span></span>

    public boolean homePage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1742">Parameters</span></span>

<span data-ttu-id="7b846-1743">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1743">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1744">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1744">Return Value</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="7b846-1745">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="7b846-1745">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1746">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1746">Parameters</span></span>

<span data-ttu-id="7b846-1747">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1747">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1748">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1748">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="7b846-1749">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="7b846-1749">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1750">Parameters</span></span>

<span data-ttu-id="7b846-1751">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1751">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1752">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1752">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="7b846-1753">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="7b846-1753">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1754">Parameters</span></span>

<span data-ttu-id="7b846-1755">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1755">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1756">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1756">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="7b846-1757">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="7b846-1757">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1758">Parameters</span></span>

<span data-ttu-id="7b846-1759">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1759">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1760">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1760">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="7b846-1761">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="7b846-1761">Method maintainUserLicense</span></span>

<span data-ttu-id="7b846-1762">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-1762">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1763">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1763">Parameters</span></span>

<span data-ttu-id="7b846-1764">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1764">value</span></span>  
<span data-ttu-id="7b846-1765">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-1765">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b846-1766">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1766">Return Value</span></span>

<span data-ttu-id="7b846-1767">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-1767">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="7b846-1768">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="7b846-1768">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1769">Parameters</span></span>

<span data-ttu-id="7b846-1770">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1770">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1771">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1771">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="7b846-1772">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="7b846-1772">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1773">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1773">Parameters</span></span>

<span data-ttu-id="7b846-1774">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1774">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1775">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1775">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="7b846-1776">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="7b846-1776">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1777">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1777">Parameters</span></span>

<span data-ttu-id="7b846-1778">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1778">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1779">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1779">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="7b846-1780">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="7b846-1780">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1781">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1781">Parameters</span></span>

<span data-ttu-id="7b846-1782">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1782">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1783">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1783">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="7b846-1784">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b846-1784">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1785">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1785">Parameters</span></span>

<span data-ttu-id="7b846-1786">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1786">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1787">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1787">Return Value</span></span>

### <a name="method-pagedefinition"></a><span data-ttu-id="7b846-1788">メソッド pageDefinition</span><span class="sxs-lookup"><span data-stu-id="7b846-1788">Method pageDefinition</span></span>

    public str pageDefinition([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1789">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1789">Parameters</span></span>

<span data-ttu-id="7b846-1790">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1790">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1791">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1791">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="7b846-1792">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="7b846-1792">Method parameters</span></span>

<span data-ttu-id="7b846-1793">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1793">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1794">Parameters</span></span>

<span data-ttu-id="7b846-1795">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1796">Return Value</span></span>

<span data-ttu-id="7b846-1797">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="7b846-1797">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b846-1798">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1798">Remarks</span></span>

<span data-ttu-id="7b846-1799">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="7b846-1799">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="7b846-1800">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1800">Objects will ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="7b846-1801">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-1801">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1802">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1802">Parameters</span></span>

<span data-ttu-id="7b846-1803">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1803">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1804">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1804">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="7b846-1805">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="7b846-1805">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1806">Parameters</span></span>

<span data-ttu-id="7b846-1807">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1808">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1808">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="7b846-1809">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="7b846-1809">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1810">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1810">Parameters</span></span>

<span data-ttu-id="7b846-1811">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1811">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1812">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1812">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="7b846-1813">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="7b846-1813">Method viewUserLicense</span></span>

<span data-ttu-id="7b846-1814">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7b846-1814">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1815">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1815">Parameters</span></span>

<span data-ttu-id="7b846-1816">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1816">value</span></span>  
<span data-ttu-id="7b846-1817">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-1817">A user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b846-1818">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1818">Return Value</span></span>

<span data-ttu-id="7b846-1819">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="7b846-1819">The user license.</span></span>

### <a name="method-windowmode"></a><span data-ttu-id="7b846-1820">メソッド windowMode</span><span class="sxs-lookup"><span data-stu-id="7b846-1820">Method windowMode</span></span>

    public int windowMode([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1821">Parameters</span></span>

<span data-ttu-id="7b846-1822">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1822">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1823">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1823">Return Value</span></span>

### <a name="method-windowparameters"></a><span data-ttu-id="7b846-1824">メソッド windowParameters</span><span class="sxs-lookup"><span data-stu-id="7b846-1824">Method windowParameters</span></span>

    public str windowParameters([str value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1825">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1825">Parameters</span></span>

<span data-ttu-id="7b846-1826">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1826">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1827">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1827">Return Value</span></span>

### <a name="method-windowsize"></a><span data-ttu-id="7b846-1828">メソッド windowSize</span><span class="sxs-lookup"><span data-stu-id="7b846-1828">Method windowSize</span></span>

    public int windowSize([int value])

#### <a name="parameters"></a><span data-ttu-id="7b846-1829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1829">Parameters</span></span>

<span data-ttu-id="7b846-1830">値</span><span class="sxs-lookup"><span data-stu-id="7b846-1830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1831">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1831">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="7b846-1832">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-1832">Method new</span></span>

<span data-ttu-id="7b846-1833">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1833">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="7b846-1834">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1834">Parameters</span></span>

<span data-ttu-id="7b846-1835">名前</span><span class="sxs-lookup"><span data-stu-id="7b846-1835">name</span></span>  

## <a name="class-winapinative"></a><span data-ttu-id="7b846-1836">クラス WinAPINative</span><span class="sxs-lookup"><span data-stu-id="7b846-1836">Class WinAPINative</span></span>
    class WinAPINative extends Object

### <a name="remarks"></a><span data-ttu-id="7b846-1837">備考</span><span class="sxs-lookup"><span data-stu-id="7b846-1837">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="7b846-1838">例</span><span class="sxs-lookup"><span data-stu-id="7b846-1838">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="7b846-1839">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b846-1839">Methods</span></span>

| <span data-ttu-id="7b846-1840">方法</span><span class="sxs-lookup"><span data-stu-id="7b846-1840">Method</span></span>                                                                                                                  | <span data-ttu-id="7b846-1841">説明</span><span class="sxs-lookup"><span data-stu-id="7b846-1841">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="7b846-1842">::public static Int64 createFontIndirect(Binary logfont)</span><span class="sxs-lookup"><span data-stu-id="7b846-1842">::public static Int64 createFontIndirect(Binary logfont)</span></span>                                                                |                                                       |
| <span data-ttu-id="7b846-1843">::public static boolean deleteObject(Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="7b846-1843">::public static boolean deleteObject(Int64 hGDIObject)</span></span>                                                                  |                                                       |
| <span data-ttu-id="7b846-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span><span class="sxs-lookup"><span data-stu-id="7b846-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span></span> |                                                       |
| <span data-ttu-id="7b846-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span><span class="sxs-lookup"><span data-stu-id="7b846-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span></span>                                                                 |                                                       |
| <span data-ttu-id="7b846-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span></span>                              |                                                       |
| <span data-ttu-id="7b846-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span><span class="sxs-lookup"><span data-stu-id="7b846-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span></span>                                                    |                                                       |
| <span data-ttu-id="7b846-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span><span class="sxs-lookup"><span data-stu-id="7b846-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span></span>                                           |                                                       |
| <span data-ttu-id="7b846-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span><span class="sxs-lookup"><span data-stu-id="7b846-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span></span>                                                       |                                                       |
| <span data-ttu-id="7b846-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span><span class="sxs-lookup"><span data-stu-id="7b846-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span></span>                        |                                                       |
| <span data-ttu-id="7b846-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="7b846-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span></span>                                                         |                                                       |
| <span data-ttu-id="7b846-1852">private void new()</span><span class="sxs-lookup"><span data-stu-id="7b846-1852">private void new()</span></span>                                                                                                      | <span data-ttu-id="7b846-1853">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1853">Initializes a new instance of the WinAPINative class.</span></span> |

### <a name="method-createfontindirect"></a><span data-ttu-id="7b846-1854">メソッド createFontIndirect</span><span class="sxs-lookup"><span data-stu-id="7b846-1854">Method createFontIndirect</span></span>

    public static Int64 createFontIndirect(Binary logfont)

#### <a name="parameters"></a><span data-ttu-id="7b846-1855">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1855">Parameters</span></span>

<span data-ttu-id="7b846-1856">logfont</span><span class="sxs-lookup"><span data-stu-id="7b846-1856">logfont</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1857">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1857">Return Value</span></span>

### <a name="method-deleteobject"></a><span data-ttu-id="7b846-1858">メソッド deleteObject</span><span class="sxs-lookup"><span data-stu-id="7b846-1858">Method deleteObject</span></span>

    public static boolean deleteObject(Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="7b846-1859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1859">Parameters</span></span>

<span data-ttu-id="7b846-1860">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="7b846-1860">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1861">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1861">Return Value</span></span>

### <a name="method-getcharabcwidthsi"></a><span data-ttu-id="7b846-1862">メソッド getCharABCWidthsI</span><span class="sxs-lookup"><span data-stu-id="7b846-1862">Method getCharABCWidthsI</span></span>

    public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)

#### <a name="parameters"></a><span data-ttu-id="7b846-1863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1863">Parameters</span></span>

<span data-ttu-id="7b846-1864">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1864">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1865">firstGlyphIndex</span><span class="sxs-lookup"><span data-stu-id="7b846-1865">firstGlyphIndex</span></span>  

<!-- -->

<span data-ttu-id="7b846-1866">glyphIndicesCount</span><span class="sxs-lookup"><span data-stu-id="7b846-1866">glyphIndicesCount</span></span>  

<!-- -->

<span data-ttu-id="7b846-1867">charWidths</span><span class="sxs-lookup"><span data-stu-id="7b846-1867">charWidths</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1868">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1868">Return Value</span></span>

### <a name="method-getdevicecaps"></a><span data-ttu-id="7b846-1869">メソッド getDeviceCaps</span><span class="sxs-lookup"><span data-stu-id="7b846-1869">Method getDeviceCaps</span></span>

    public static int getDeviceCaps(Int64 hDC, int index)

#### <a name="parameters"></a><span data-ttu-id="7b846-1870">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1870">Parameters</span></span>

<span data-ttu-id="7b846-1871">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1871">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1872">指数</span><span class="sxs-lookup"><span data-stu-id="7b846-1872">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1873">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1873">Return Value</span></span>

### <a name="method-getfontdata"></a><span data-ttu-id="7b846-1874">メソッド getFontData</span><span class="sxs-lookup"><span data-stu-id="7b846-1874">Method getFontData</span></span>

    public static int getFontData(Int64 hDC, int dwTable, int dwOffset, [Binary pvBuffer])

#### <a name="parameters"></a><span data-ttu-id="7b846-1875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1875">Parameters</span></span>

<span data-ttu-id="7b846-1876">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1876">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1877">dwTable</span><span class="sxs-lookup"><span data-stu-id="7b846-1877">dwTable</span></span>  

<!-- -->

<span data-ttu-id="7b846-1878">dwOffset</span><span class="sxs-lookup"><span data-stu-id="7b846-1878">dwOffset</span></span>  

<!-- -->

<span data-ttu-id="7b846-1879">pvBuffer</span><span class="sxs-lookup"><span data-stu-id="7b846-1879">pvBuffer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1880">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1880">Return Value</span></span>

### <a name="method-getfontunicoderanges"></a><span data-ttu-id="7b846-1881">メソッド getFontUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="7b846-1881">Method getFontUnicodeRanges</span></span>

    public static int getFontUnicodeRanges(Int64 hDC, [Binary lpgs])

#### <a name="parameters"></a><span data-ttu-id="7b846-1882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1882">Parameters</span></span>

<span data-ttu-id="7b846-1883">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1883">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1884">lpgs</span><span class="sxs-lookup"><span data-stu-id="7b846-1884">lpgs</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1885">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1885">Return Value</span></span>

### <a name="method-getglyphindices"></a><span data-ttu-id="7b846-1886">メソッド getGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="7b846-1886">Method getGlyphIndices</span></span>

    public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)

#### <a name="parameters"></a><span data-ttu-id="7b846-1887">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1887">Parameters</span></span>

<span data-ttu-id="7b846-1888">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1888">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1889">lpstr</span><span class="sxs-lookup"><span data-stu-id="7b846-1889">lpstr</span></span>  

<!-- -->

<span data-ttu-id="7b846-1890">pgi</span><span class="sxs-lookup"><span data-stu-id="7b846-1890">pgi</span></span>  

<!-- -->

<span data-ttu-id="7b846-1891">fl</span><span class="sxs-lookup"><span data-stu-id="7b846-1891">fl</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1892">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1892">Return Value</span></span>

### <a name="method-gettextmetrics"></a><span data-ttu-id="7b846-1893">メソッド getTextMetrics</span><span class="sxs-lookup"><span data-stu-id="7b846-1893">Method getTextMetrics</span></span>

    public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)

#### <a name="parameters"></a><span data-ttu-id="7b846-1894">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1894">Parameters</span></span>

<span data-ttu-id="7b846-1895">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1895">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1896">lpMetrics</span><span class="sxs-lookup"><span data-stu-id="7b846-1896">lpMetrics</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1897">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1897">Return Value</span></span>

### <a name="method-getuniscribeglyphindices"></a><span data-ttu-id="7b846-1898">メソッド getUniscribeGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="7b846-1898">Method getUniscribeGlyphIndices</span></span>

    public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)

#### <a name="parameters"></a><span data-ttu-id="7b846-1899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1899">Parameters</span></span>

<span data-ttu-id="7b846-1900">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1900">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1901">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="7b846-1901">hGDIObject</span></span>  

<!-- -->

<span data-ttu-id="7b846-1902">lpstr</span><span class="sxs-lookup"><span data-stu-id="7b846-1902">lpstr</span></span>  

<!-- -->

<span data-ttu-id="7b846-1903">pgi</span><span class="sxs-lookup"><span data-stu-id="7b846-1903">pgi</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1904">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1904">Return Value</span></span>

### <a name="method-selectobject"></a><span data-ttu-id="7b846-1905">メソッド selectObject</span><span class="sxs-lookup"><span data-stu-id="7b846-1905">Method selectObject</span></span>

    public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="7b846-1906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b846-1906">Parameters</span></span>

<span data-ttu-id="7b846-1907">hDC</span><span class="sxs-lookup"><span data-stu-id="7b846-1907">hDC</span></span>  

<!-- -->

<span data-ttu-id="7b846-1908">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="7b846-1908">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="7b846-1909">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b846-1909">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="7b846-1910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7b846-1910">Method new</span></span>

<span data-ttu-id="7b846-1911">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7b846-1911">Initializes a new instance of the WinAPINative class.</span></span>

    private void new()




