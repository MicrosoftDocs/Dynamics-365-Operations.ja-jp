---
title: W クラス
description: 文字 W で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 55901
ms.assetid: ca08dc94-1481-4ac0-80f4-d092da5c1c90
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f63f9f14db6ffc70527d99b689fc5244add83fad
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833654"
---
# <a name="w-classes"></a><span data-ttu-id="89dd4-103">W クラス</span><span class="sxs-lookup"><span data-stu-id="89dd4-103">W classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89dd4-104">文字 W で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-104">System API classes that start with the letter W.</span></span>

<a name="class-webactionmenufunction"></a><span data-ttu-id="89dd4-105">クラス WebActionMenuFunction</span><span class="sxs-lookup"><span data-stu-id="89dd4-105">Class WebActionMenuFunction</span></span>
---------------------------

    class WebActionMenuFunction extends WebMenuFunction

<span data-ttu-id="89dd4-106">WebActionMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-106">The WebActionMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-107">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-107">Remarks</span></span>

<span data-ttu-id="89dd4-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-109">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-109">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-110">Methods</span></span>

| <span data-ttu-id="89dd4-111">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-111">Method</span></span>                                                   | <span data-ttu-id="89dd4-112">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-112">Description</span></span>                                                                                                 |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-113">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-113">public boolean big(\[boolean value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="89dd4-114">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-114">public int correctPermissions(\[int value\])</span></span>             |                                                                                                             |
| <span data-ttu-id="89dd4-115">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-115">public int createPermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="89dd4-116">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-116">public int deletePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="89dd4-117">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-117">public int enumParameter(\[int value\])</span></span>                  | <span data-ttu-id="89dd4-118">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-118">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span> |
| <span data-ttu-id="89dd4-119">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-119">public EnumId enumTypeParameter(\[EnumId value\])</span></span>        | <span data-ttu-id="89dd4-120">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-120">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                     |
| <span data-ttu-id="89dd4-121">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-121">public int imageLocation(\[int value\])</span></span>                  |                                                                                                             |
| <span data-ttu-id="89dd4-122">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-122">public str linkedPermissionObject(\[str value\])</span></span>         |                                                                                                             |
| <span data-ttu-id="89dd4-123">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-123">public str linkedPermissionObjectChild(\[str value\])</span></span>    |                                                                                                             |
| <span data-ttu-id="89dd4-124">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-124">public int linkedPermissionType(\[int value\])</span></span>           |                                                                                                             |
| <span data-ttu-id="89dd4-125">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-125">public int maintainUserLicense(\[int value\])</span></span>            | <span data-ttu-id="89dd4-126">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-126">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="89dd4-127">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-127">public boolean multiSelect(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="89dd4-128">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-128">public boolean needsRecord(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="89dd4-129">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-129">public str normalImage(\[str value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="89dd4-130">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-130">public int normalResource(\[int value\])</span></span>                 |                                                                                                             |
| <span data-ttu-id="89dd4-131">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-131">public str object(\[str value\])</span></span>                         | <span data-ttu-id="89dd4-132">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-132">Gets or sets the object that the MenuFunction class runs.</span></span>                                                   |
| <span data-ttu-id="89dd4-133">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-133">public int objectType(\[int value\])</span></span>                     |                                                                                                             |
| <span data-ttu-id="89dd4-134">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-134">public Guid origin(\[Guid value\])</span></span>                       |                                                                                                             |
| <span data-ttu-id="89dd4-135">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-135">public str parameters(\[str value\])</span></span>                     | <span data-ttu-id="89dd4-136">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-136">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>      |
| <span data-ttu-id="89dd4-137">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-137">public int readPermissions(\[int value\])</span></span>                |                                                                                                             |
| <span data-ttu-id="89dd4-138">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-138">public str reportDesign(\[str value\])</span></span>                   |                                                                                                             |
| <span data-ttu-id="89dd4-139">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-139">public int runOn(\[int value\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="89dd4-140">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-140">public int updatePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="89dd4-141">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-141">public int viewUserLicense(\[int value\])</span></span>                | <span data-ttu-id="89dd4-142">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-142">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="89dd4-143">::public static void runCalled(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-143">::public static void runCalled(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="89dd4-144">public void AOTrun(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-144">public void AOTrun(\[xArgs args\])</span></span>                       | <span data-ttu-id="89dd4-145">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="89dd4-145">Compiles this node and its sub-tree in the Finance and Operations Application Object Tree (AOT).</span></span>             |
| <span data-ttu-id="89dd4-146">::public static void runClient(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-146">::public static void runClient(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="89dd4-147">public void run(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-147">public void run(\[xArgs args\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="89dd4-148">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-148">public void new(str name)</span></span>                                | <span data-ttu-id="89dd4-149">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-149">Initializes a new instance of the TreeNode class.</span></span>                                                           |
| <span data-ttu-id="89dd4-150">::public static void runServer(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-150">::public static void runServer(str name, \[xArgs args\])</span></span> |                                                                                                             |

### <a name="method-big"></a><span data-ttu-id="89dd4-151">メソッド big</span><span class="sxs-lookup"><span data-stu-id="89dd4-151">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-152">Parameters</span></span>

<span data-ttu-id="89dd4-153">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-153">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-154">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="89dd4-155">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-155">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-156">Parameters</span></span>

<span data-ttu-id="89dd4-157">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-157">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-158">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="89dd4-159">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-159">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-160">Parameters</span></span>

<span data-ttu-id="89dd4-161">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-161">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-162">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="89dd4-163">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-163">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-164">Parameters</span></span>

<span data-ttu-id="89dd4-165">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-165">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-166">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="89dd4-167">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="89dd4-167">Method enumParameter</span></span>

<span data-ttu-id="89dd4-168">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-168">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-169">Parameters</span></span>

<span data-ttu-id="89dd4-170">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-170">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-171">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-171">Return Value</span></span>

<span data-ttu-id="89dd4-172">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-172">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="89dd4-173">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="89dd4-173">Method enumTypeParameter</span></span>

<span data-ttu-id="89dd4-174">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-174">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-175">Parameters</span></span>

<span data-ttu-id="89dd4-176">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-176">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-177">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-177">Return Value</span></span>

<span data-ttu-id="89dd4-178">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-178">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="89dd4-179">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="89dd4-179">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-180">Parameters</span></span>

<span data-ttu-id="89dd4-181">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-182">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="89dd4-183">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="89dd4-183">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-184">Parameters</span></span>

<span data-ttu-id="89dd4-185">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-185">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-186">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-186">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="89dd4-187">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="89dd4-187">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-188">Parameters</span></span>

<span data-ttu-id="89dd4-189">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-189">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-190">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-190">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="89dd4-191">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="89dd4-191">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-192">Parameters</span></span>

<span data-ttu-id="89dd4-193">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-193">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-194">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="89dd4-195">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="89dd4-195">Method maintainUserLicense</span></span>

<span data-ttu-id="89dd4-196">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-196">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-197">Parameters</span></span>

<span data-ttu-id="89dd4-198">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-198">value</span></span>  
<span data-ttu-id="89dd4-199">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-199">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89dd4-200">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-200">Return Value</span></span>

<span data-ttu-id="89dd4-201">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-201">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="89dd4-202">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="89dd4-202">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-203">Parameters</span></span>

<span data-ttu-id="89dd4-204">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-204">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-205">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="89dd4-206">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="89dd4-206">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-207">Parameters</span></span>

<span data-ttu-id="89dd4-208">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-208">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-209">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-209">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="89dd4-210">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="89dd4-210">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-211">Parameters</span></span>

<span data-ttu-id="89dd4-212">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-212">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-213">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-213">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="89dd4-214">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="89dd4-214">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-215">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-215">Parameters</span></span>

<span data-ttu-id="89dd4-216">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-216">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-217">Return Value</span></span>

### <a name="method-object"></a><span data-ttu-id="89dd4-218">メソッド object</span><span class="sxs-lookup"><span data-stu-id="89dd4-218">Method object</span></span>

<span data-ttu-id="89dd4-219">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-219">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-220">Parameters</span></span>

<span data-ttu-id="89dd4-221">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-221">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-222">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-222">Return Value</span></span>

<span data-ttu-id="89dd4-223">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-223">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-224">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-224">Remarks</span></span>

<span data-ttu-id="89dd4-225">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-225">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="89dd4-226">フォーム</span><span class="sxs-lookup"><span data-stu-id="89dd4-226">Form</span></span>
-   <span data-ttu-id="89dd4-227">レポート </span><span class="sxs-lookup"><span data-stu-id="89dd4-227">Report</span></span>
-   <span data-ttu-id="89dd4-228">ジョブ</span><span class="sxs-lookup"><span data-stu-id="89dd4-228">Job</span></span>
-   <span data-ttu-id="89dd4-229">クラス</span><span class="sxs-lookup"><span data-stu-id="89dd4-229">Class</span></span>
-   <span data-ttu-id="89dd4-230">クエリ</span><span class="sxs-lookup"><span data-stu-id="89dd4-230">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="89dd4-231">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="89dd4-231">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-232">Parameters</span></span>

<span data-ttu-id="89dd4-233">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-233">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-234">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-235">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-235">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-236">Parameters</span></span>

<span data-ttu-id="89dd4-237">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-237">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-238">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-238">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="89dd4-239">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="89dd4-239">Method parameters</span></span>

<span data-ttu-id="89dd4-240">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-240">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-241">Parameters</span></span>

<span data-ttu-id="89dd4-242">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-242">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-243">Return Value</span></span>

<span data-ttu-id="89dd4-244">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-244">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-245">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-245">Remarks</span></span>

<span data-ttu-id="89dd4-246">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-246">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="89dd4-247">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-247">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="89dd4-248">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-248">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-249">Parameters</span></span>

<span data-ttu-id="89dd4-250">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-250">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-251">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-251">Return Value</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="89dd4-252">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="89dd4-252">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-253">Parameters</span></span>

<span data-ttu-id="89dd4-254">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-254">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-255">Return Value</span></span>

### <a name="method-runon"></a><span data-ttu-id="89dd4-256">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="89dd4-256">Method runOn</span></span>

    public int runOn([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-257">Parameters</span></span>

<span data-ttu-id="89dd4-258">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-258">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-259">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-259">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="89dd4-260">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-260">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-261">Parameters</span></span>

<span data-ttu-id="89dd4-262">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-262">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-263">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="89dd4-264">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="89dd4-264">Method viewUserLicense</span></span>

<span data-ttu-id="89dd4-265">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-265">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-266">Parameters</span></span>

<span data-ttu-id="89dd4-267">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-267">value</span></span>  
<span data-ttu-id="89dd4-268">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-268">The user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89dd4-269">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-269">Return Value</span></span>

<span data-ttu-id="89dd4-270">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-270">The user license.</span></span>

### <a name="method-runcalled"></a><span data-ttu-id="89dd4-271">メソッド runCalled</span><span class="sxs-lookup"><span data-stu-id="89dd4-271">Method runCalled</span></span>

    public static void runCalled(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="89dd4-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-272">Parameters</span></span>

<span data-ttu-id="89dd4-273">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-273">name</span></span>  

<!-- -->

<span data-ttu-id="89dd4-274">args</span><span class="sxs-lookup"><span data-stu-id="89dd4-274">args</span></span>  

### <a name="method-aotrun"></a><span data-ttu-id="89dd4-275">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="89dd4-275">Method AOTrun</span></span>

<span data-ttu-id="89dd4-276">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="89dd4-276">Compiles this node and its sub-tree in the Finance and Operations Application Object Tree (AOT).</span></span>

    public void AOTrun([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="89dd4-277">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-277">Parameters</span></span>

<span data-ttu-id="89dd4-278">args</span><span class="sxs-lookup"><span data-stu-id="89dd4-278">args</span></span>  

### <a name="method-runclient"></a><span data-ttu-id="89dd4-279">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="89dd4-279">Method runClient</span></span>

    public static void runClient(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="89dd4-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-280">Parameters</span></span>

<span data-ttu-id="89dd4-281">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-281">name</span></span>  

<!-- -->

<span data-ttu-id="89dd4-282">args</span><span class="sxs-lookup"><span data-stu-id="89dd4-282">args</span></span>  

### <a name="method-run"></a><span data-ttu-id="89dd4-283">メソッド run</span><span class="sxs-lookup"><span data-stu-id="89dd4-283">Method run</span></span>

    public void run([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="89dd4-284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-284">Parameters</span></span>

<span data-ttu-id="89dd4-285">args</span><span class="sxs-lookup"><span data-stu-id="89dd4-285">args</span></span>  

### <a name="method-new"></a><span data-ttu-id="89dd4-286">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-286">Method new</span></span>

<span data-ttu-id="89dd4-287">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-287">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-288">Parameters</span></span>

<span data-ttu-id="89dd4-289">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-289">name</span></span>  

### <a name="method-runserver"></a><span data-ttu-id="89dd4-290">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="89dd4-290">Method runServer</span></span>

    public static void runServer(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="89dd4-291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-291">Parameters</span></span>

<span data-ttu-id="89dd4-292">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-292">name</span></span>  

<!-- -->

<span data-ttu-id="89dd4-293">args</span><span class="sxs-lookup"><span data-stu-id="89dd4-293">args</span></span>  

## <a name="class-webcontentitem"></a><span data-ttu-id="89dd4-294">クラス WebContentItem</span><span class="sxs-lookup"><span data-stu-id="89dd4-294">Class WebContentItem</span></span>
    class WebContentItem extends SecureNode

<span data-ttu-id="89dd4-295">WebContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-295">The WebContentItem class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-296">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-296">Remarks</span></span>

<span data-ttu-id="89dd4-297">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-297">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-298">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-298">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-299">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-299">Methods</span></span>

| <span data-ttu-id="89dd4-300">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-300">Method</span></span>                                            | <span data-ttu-id="89dd4-301">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-301">Description</span></span>                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-302">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-302">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="89dd4-303">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-303">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="89dd4-304">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-304">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="89dd4-305">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-305">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-306">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-306">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="89dd4-307">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-307">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-308">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-308">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="89dd4-309">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-309">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="89dd4-310">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-310">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="89dd4-311">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-311">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="89dd4-312">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-312">public str creationTime(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="89dd4-313">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-313">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="89dd4-314">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-314">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                               |
| <span data-ttu-id="89dd4-315">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-315">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="89dd4-316">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-316">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                   |
| <span data-ttu-id="89dd4-317">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-317">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="89dd4-318">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-318">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="89dd4-319">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-319">public str label(\[str value\])</span></span>                   | <span data-ttu-id="89dd4-320">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-320">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="89dd4-321">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-321">public str name(\[str value\])</span></span>                    | <span data-ttu-id="89dd4-322">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-322">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-323">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-323">public str object(\[str value\])</span></span>                  | <span data-ttu-id="89dd4-324">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-324">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-325">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-325">public int objectType(\[int value\])</span></span>              |                                                                                                                                           |
| <span data-ttu-id="89dd4-326">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-326">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="89dd4-327">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-327">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="89dd4-328">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-328">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="89dd4-329">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-329">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                           |

### <a name="method-changedby"></a><span data-ttu-id="89dd4-330">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-330">Method changedBy</span></span>

<span data-ttu-id="89dd4-331">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-331">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-332">Parameters</span></span>

<span data-ttu-id="89dd4-333">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-333">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-334">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-334">Return Value</span></span>

<span data-ttu-id="89dd4-335">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-335">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-336">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-336">Method changedDate</span></span>

<span data-ttu-id="89dd4-337">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-337">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-338">Parameters</span></span>

<span data-ttu-id="89dd4-339">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-339">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-340">Return Value</span></span>

<span data-ttu-id="89dd4-341">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-341">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-342">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-342">Method changedTime</span></span>

<span data-ttu-id="89dd4-343">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-343">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-344">Parameters</span></span>

<span data-ttu-id="89dd4-345">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-345">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-346">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-346">Return Value</span></span>

<span data-ttu-id="89dd4-347">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-347">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-348">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-348">Method createdBy</span></span>

<span data-ttu-id="89dd4-349">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-349">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-350">Parameters</span></span>

<span data-ttu-id="89dd4-351">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-351">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-352">Return Value</span></span>

<span data-ttu-id="89dd4-353">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-353">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-354">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-354">Method creationDate</span></span>

<span data-ttu-id="89dd4-355">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-355">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-356">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-356">Parameters</span></span>

<span data-ttu-id="89dd4-357">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-357">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-358">Return Value</span></span>

<span data-ttu-id="89dd4-359">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-359">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-360">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-360">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-361">Parameters</span></span>

<span data-ttu-id="89dd4-362">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-362">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-363">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="89dd4-364">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="89dd4-364">Method enumParameter</span></span>

<span data-ttu-id="89dd4-365">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-365">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-366">Parameters</span></span>

<span data-ttu-id="89dd4-367">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-368">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-368">Return Value</span></span>

<span data-ttu-id="89dd4-369">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-369">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="89dd4-370">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="89dd4-370">Method enumTypeParameter</span></span>

<span data-ttu-id="89dd4-371">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-371">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-372">Parameters</span></span>

<span data-ttu-id="89dd4-373">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-373">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-374">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-374">Return Value</span></span>

<span data-ttu-id="89dd4-375">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-375">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="89dd4-376">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="89dd4-376">Method helpText</span></span>

<span data-ttu-id="89dd4-377">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-377">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-378">Parameters</span></span>

<span data-ttu-id="89dd4-379">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-379">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-380">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-380">Return Value</span></span>

<span data-ttu-id="89dd4-381">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="89dd4-381">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-382">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-382">Remarks</span></span>

<span data-ttu-id="89dd4-383">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-383">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="89dd4-384">ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-384">dialog box.</span></span> <span data-ttu-id="89dd4-385">ヘルプ テキストは、250文字以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-385">The The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="89dd4-386">メソッド label</span><span class="sxs-lookup"><span data-stu-id="89dd4-386">Method label</span></span>

<span data-ttu-id="89dd4-387">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-387">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-388">Parameters</span></span>

<span data-ttu-id="89dd4-389">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-389">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-390">Return Value</span></span>

<span data-ttu-id="89dd4-391">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-391">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-392">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-392">Remarks</span></span>

<span data-ttu-id="89dd4-393">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-393">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="89dd4-394">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-394">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-395">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-395">Method name</span></span>

<span data-ttu-id="89dd4-396">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-396">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-397">Parameters</span></span>

<span data-ttu-id="89dd4-398">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-398">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-399">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-399">Return Value</span></span>

<span data-ttu-id="89dd4-400">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-400">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-401">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-401">Remarks</span></span>

<span data-ttu-id="89dd4-402">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-402">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-403">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-403">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-404">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-404">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-405">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-405">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-406">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-406">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-407">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-407">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-object"></a><span data-ttu-id="89dd4-408">メソッド object</span><span class="sxs-lookup"><span data-stu-id="89dd4-408">Method object</span></span>

<span data-ttu-id="89dd4-409">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-409">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-410">Parameters</span></span>

<span data-ttu-id="89dd4-411">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-411">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-412">Return Value</span></span>

<span data-ttu-id="89dd4-413">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-413">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-414">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-414">Remarks</span></span>

<span data-ttu-id="89dd4-415">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-415">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="89dd4-416">フォーム</span><span class="sxs-lookup"><span data-stu-id="89dd4-416">Form</span></span>
-   <span data-ttu-id="89dd4-417">レポート </span><span class="sxs-lookup"><span data-stu-id="89dd4-417">Report</span></span>
-   <span data-ttu-id="89dd4-418">ジョブ</span><span class="sxs-lookup"><span data-stu-id="89dd4-418">Job</span></span>
-   <span data-ttu-id="89dd4-419">クラス</span><span class="sxs-lookup"><span data-stu-id="89dd4-419">Class</span></span>
-   <span data-ttu-id="89dd4-420">クエリ</span><span class="sxs-lookup"><span data-stu-id="89dd4-420">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="89dd4-421">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="89dd4-421">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-422">Parameters</span></span>

<span data-ttu-id="89dd4-423">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-423">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-424">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-425">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-425">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-426">Parameters</span></span>

<span data-ttu-id="89dd4-427">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-427">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-428">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-428">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="89dd4-429">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="89dd4-429">Method parameters</span></span>

<span data-ttu-id="89dd4-430">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-430">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-431">Parameters</span></span>

<span data-ttu-id="89dd4-432">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-432">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-433">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-433">Return Value</span></span>

<span data-ttu-id="89dd4-434">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-434">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-435">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-435">Remarks</span></span>

<span data-ttu-id="89dd4-436">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-436">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="89dd4-437">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-437">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="89dd4-438">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="89dd4-438">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-439">Parameters</span></span>

<span data-ttu-id="89dd4-440">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-440">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-441">Return Value</span></span>

## <a name="class-webcontrolnode"></a><span data-ttu-id="89dd4-442">クラス webControlNode</span><span class="sxs-lookup"><span data-stu-id="89dd4-442">Class webControlNode</span></span>
    class webControlNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="89dd4-443">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-443">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-444">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-444">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-445">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-445">Methods</span></span>

| <span data-ttu-id="89dd4-446">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-446">Method</span></span>                                                        | <span data-ttu-id="89dd4-447">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-447">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-448">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="89dd4-448">public str AOTgetSource()</span></span>                                     | <span data-ttu-id="89dd4-449">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-449">Returns the source code of this node.</span></span>                                                                                                         |
| <span data-ttu-id="89dd4-450">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-450">public str changedBy(\[str value\])</span></span>                           | <span data-ttu-id="89dd4-451">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-451">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="89dd4-452">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-452">public Date changedDate(\[Date value\])</span></span>                       | <span data-ttu-id="89dd4-453">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-453">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-454">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-454">public str changedTime(\[str value\])</span></span>                         | <span data-ttu-id="89dd4-455">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-455">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-456">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-456">public str createdBy(\[str value\])</span></span>                           | <span data-ttu-id="89dd4-457">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-457">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="89dd4-458">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-458">public Date creationDate(\[Date value\])</span></span>                      | <span data-ttu-id="89dd4-459">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-459">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="89dd4-460">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-460">public str creationTime(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="89dd4-461">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-461">public str filename(\[str value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="89dd4-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span></span> | <span data-ttu-id="89dd4-463">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-463">Get a list of web controls that are related to this web control.</span></span>                                                                              |
| <span data-ttu-id="89dd4-464">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-464">public str helpText(\[str value\])</span></span>                            | <span data-ttu-id="89dd4-465">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-465">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="89dd4-466">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-466">public str name(\[str value\])</span></span>                                | <span data-ttu-id="89dd4-467">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-467">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-468">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-468">public Guid origin(\[Guid value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="89dd4-469">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-469">public str relativePath(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="89dd4-470">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-470">public str version(\[str value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="89dd4-471">::public static webControlNode createFromFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="89dd4-471">::public static webControlNode createFromFile(str fileName)</span></span>   |                                                                                                                                               |
| <span data-ttu-id="89dd4-472">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-472">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>    | <span data-ttu-id="89dd4-473">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-473">Sets the source code of this node.</span></span>                                                                                                            |

### <a name="method-aotgetsource"></a><span data-ttu-id="89dd4-474">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-474">Method AOTgetSource</span></span>

<span data-ttu-id="89dd4-475">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-475">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="89dd4-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-476">Return Value</span></span>

<span data-ttu-id="89dd4-477">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="89dd4-477">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-478">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-478">Remarks</span></span>

<span data-ttu-id="89dd4-479">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-479">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="89dd4-480">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-480">Method changedBy</span></span>

<span data-ttu-id="89dd4-481">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-481">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-482">Parameters</span></span>

<span data-ttu-id="89dd4-483">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-484">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-484">Return Value</span></span>

<span data-ttu-id="89dd4-485">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-485">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-486">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-486">Method changedDate</span></span>

<span data-ttu-id="89dd4-487">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-487">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-488">Parameters</span></span>

<span data-ttu-id="89dd4-489">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-489">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-490">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-490">Return Value</span></span>

<span data-ttu-id="89dd4-491">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-491">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-492">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-492">Method changedTime</span></span>

<span data-ttu-id="89dd4-493">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-493">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-494">Parameters</span></span>

<span data-ttu-id="89dd4-495">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-495">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-496">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-496">Return Value</span></span>

<span data-ttu-id="89dd4-497">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-497">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-498">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-498">Method createdBy</span></span>

<span data-ttu-id="89dd4-499">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-499">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-500">Parameters</span></span>

<span data-ttu-id="89dd4-501">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-501">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-502">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-502">Return Value</span></span>

<span data-ttu-id="89dd4-503">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-503">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-504">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-504">Method creationDate</span></span>

<span data-ttu-id="89dd4-505">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-505">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-506">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-506">Parameters</span></span>

<span data-ttu-id="89dd4-507">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-507">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-508">Return Value</span></span>

<span data-ttu-id="89dd4-509">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-509">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-510">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-510">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-511">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-511">Parameters</span></span>

<span data-ttu-id="89dd4-512">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-512">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-513">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="89dd4-514">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="89dd4-514">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-515">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-515">Parameters</span></span>

<span data-ttu-id="89dd4-516">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-516">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-517">Return Value</span></span>

### <a name="method-getrelatedwebcontrols"></a><span data-ttu-id="89dd4-518">メソッド getRelatedWebControls</span><span class="sxs-lookup"><span data-stu-id="89dd4-518">Method getRelatedWebControls</span></span>

<span data-ttu-id="89dd4-519">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-519">Get a list of web controls that are related to this web control.</span></span>

    public List getRelatedWebControls([boolean firstLevelOnly])

#### <a name="parameters"></a><span data-ttu-id="89dd4-520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-520">Parameters</span></span>

<span data-ttu-id="89dd4-521">firstLevelOnly</span><span class="sxs-lookup"><span data-stu-id="89dd4-521">firstLevelOnly</span></span>  
<span data-ttu-id="89dd4-522">Web コントロールの最初のレベルのみがオンになっているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-522">A value that indicates whether only the first level of web controls is checked.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89dd4-523">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-523">Return Value</span></span>

<span data-ttu-id="89dd4-524">関連する Web コントロールの一覧。</span><span class="sxs-lookup"><span data-stu-id="89dd4-524">A list of related web controls.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="89dd4-525">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="89dd4-525">Method helpText</span></span>

<span data-ttu-id="89dd4-526">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-526">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-527">Parameters</span></span>

<span data-ttu-id="89dd4-528">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-528">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-529">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-529">Return Value</span></span>

<span data-ttu-id="89dd4-530">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="89dd4-530">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-531">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-531">Remarks</span></span>

<span data-ttu-id="89dd4-532">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-532">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="89dd4-533">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-533">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-534">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-534">Method name</span></span>

<span data-ttu-id="89dd4-535">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-535">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-536">Parameters</span></span>

<span data-ttu-id="89dd4-537">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-538">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-538">Return Value</span></span>

<span data-ttu-id="89dd4-539">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-539">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-540">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-540">Remarks</span></span>

<span data-ttu-id="89dd4-541">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-541">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-542">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-542">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-543">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-543">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-544">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-544">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-545">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-545">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-546">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-546">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-547">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-547">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-548">Parameters</span></span>

<span data-ttu-id="89dd4-549">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-549">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-550">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-550">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="89dd4-551">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="89dd4-551">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-552">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-552">Parameters</span></span>

<span data-ttu-id="89dd4-553">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-553">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-554">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-554">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="89dd4-555">メソッド version</span><span class="sxs-lookup"><span data-stu-id="89dd4-555">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-556">Parameters</span></span>

<span data-ttu-id="89dd4-557">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-557">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-558">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-558">Return Value</span></span>

### <a name="method-createfromfile"></a><span data-ttu-id="89dd4-559">メソッド createFromFile</span><span class="sxs-lookup"><span data-stu-id="89dd4-559">Method createFromFile</span></span>

    public static webControlNode createFromFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="89dd4-560">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-560">Parameters</span></span>

<span data-ttu-id="89dd4-561">fileName</span><span class="sxs-lookup"><span data-stu-id="89dd4-561">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-562">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-562">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="89dd4-563">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-563">Method AOTsetSource</span></span>

<span data-ttu-id="89dd4-564">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-564">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="89dd4-565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-565">Parameters</span></span>

<span data-ttu-id="89dd4-566">ソース</span><span class="sxs-lookup"><span data-stu-id="89dd4-566">source</span></span>  
<span data-ttu-id="89dd4-567">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="89dd4-567">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="89dd4-568">isStatic</span><span class="sxs-lookup"><span data-stu-id="89dd4-568">isStatic</span></span>  
<span data-ttu-id="89dd4-569">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="89dd4-569">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-570">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-570">Remarks</span></span>

<span data-ttu-id="89dd4-571">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-571">This method is overridden by nodes that have source code.</span></span>

## <a name="class-webdisplaycontentitem"></a><span data-ttu-id="89dd4-572">クラス WebDisplayContentItem</span><span class="sxs-lookup"><span data-stu-id="89dd4-572">Class WebDisplayContentItem</span></span>
    class WebDisplayContentItem extends WebContentItem

<span data-ttu-id="89dd4-573">WebDisplayContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-573">The WebDisplayContentItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-574">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-574">Remarks</span></span>

<span data-ttu-id="89dd4-575">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-575">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="89dd4-576">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-576">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-577">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-577">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-578">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-578">Methods</span></span>

| <span data-ttu-id="89dd4-579">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-579">Method</span></span>                    | <span data-ttu-id="89dd4-580">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-580">Description</span></span>                          |
|---------------------------|--------------------------------------|
| <span data-ttu-id="89dd4-581">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-581">public void new(str name)</span></span> | <span data-ttu-id="89dd4-582">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-582">Creates a new WebDisplayContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="89dd4-583">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-583">Method new</span></span>

<span data-ttu-id="89dd4-584">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-584">Creates a new WebDisplayContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-585">Parameters</span></span>

<span data-ttu-id="89dd4-586">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-586">name</span></span>  

## <a name="class-webletitem"></a><span data-ttu-id="89dd4-587">クラス WebletItem</span><span class="sxs-lookup"><span data-stu-id="89dd4-587">Class WebletItem</span></span>
    class WebletItem extends SecureNode

<span data-ttu-id="89dd4-588">WebletItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-588">The WebletItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-589">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-589">Remarks</span></span>

<span data-ttu-id="89dd4-590">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-590">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="89dd4-591">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-591">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-592">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-592">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-593">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-593">Methods</span></span>

| <span data-ttu-id="89dd4-594">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-594">Method</span></span>                                            | <span data-ttu-id="89dd4-595">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-595">Description</span></span>                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-596">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-596">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="89dd4-597">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-597">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="89dd4-598">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-598">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="89dd4-599">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-599">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-600">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-600">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="89dd4-601">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-601">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-602">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-602">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="89dd4-603">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-603">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="89dd4-604">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-604">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="89dd4-605">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-605">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="89dd4-606">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-606">public str creationTime(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="89dd4-607">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-607">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="89dd4-608">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-608">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                                   |
| <span data-ttu-id="89dd4-609">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-609">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="89dd4-610">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-610">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="89dd4-611">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-611">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="89dd4-612">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-612">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="89dd4-613">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-613">public str label(\[str value\])</span></span>                   | <span data-ttu-id="89dd4-614">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-614">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="89dd4-615">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-615">public str name(\[str value\])</span></span>                    | <span data-ttu-id="89dd4-616">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-616">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-617">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-617">public str object(\[str value\])</span></span>                  | <span data-ttu-id="89dd4-618">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-618">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                     |
| <span data-ttu-id="89dd4-619">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-619">public int objectType(\[int value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="89dd4-620">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-620">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="89dd4-621">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-621">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="89dd4-622">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-622">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                        |
| <span data-ttu-id="89dd4-623">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-623">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="89dd4-624">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-624">public void new(str name)</span></span>                         | <span data-ttu-id="89dd4-625">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-625">Microsoft internal use only.</span></span>                                                                                                                  |

### <a name="method-changedby"></a><span data-ttu-id="89dd4-626">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-626">Method changedBy</span></span>

<span data-ttu-id="89dd4-627">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-627">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-628">Parameters</span></span>

<span data-ttu-id="89dd4-629">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-630">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-630">Return Value</span></span>

<span data-ttu-id="89dd4-631">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-631">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-632">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-632">Method changedDate</span></span>

<span data-ttu-id="89dd4-633">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-633">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-634">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-634">Parameters</span></span>

<span data-ttu-id="89dd4-635">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-635">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-636">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-636">Return Value</span></span>

<span data-ttu-id="89dd4-637">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-637">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-638">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-638">Method changedTime</span></span>

<span data-ttu-id="89dd4-639">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-639">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-640">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-640">Parameters</span></span>

<span data-ttu-id="89dd4-641">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-641">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-642">Return Value</span></span>

<span data-ttu-id="89dd4-643">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-643">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-644">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-644">Method createdBy</span></span>

<span data-ttu-id="89dd4-645">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-645">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-646">Parameters</span></span>

<span data-ttu-id="89dd4-647">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-648">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-648">Return Value</span></span>

<span data-ttu-id="89dd4-649">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-649">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-650">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-650">Method creationDate</span></span>

<span data-ttu-id="89dd4-651">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-651">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-652">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-652">Parameters</span></span>

<span data-ttu-id="89dd4-653">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-653">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-654">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-654">Return Value</span></span>

<span data-ttu-id="89dd4-655">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-655">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-656">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-656">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-657">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-657">Parameters</span></span>

<span data-ttu-id="89dd4-658">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-658">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-659">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="89dd4-660">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="89dd4-660">Method enumParameter</span></span>

<span data-ttu-id="89dd4-661">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-661">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-662">Parameters</span></span>

<span data-ttu-id="89dd4-663">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-664">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-664">Return Value</span></span>

<span data-ttu-id="89dd4-665">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-665">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="89dd4-666">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="89dd4-666">Method enumTypeParameter</span></span>

<span data-ttu-id="89dd4-667">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-667">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-668">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-668">Parameters</span></span>

<span data-ttu-id="89dd4-669">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-669">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-670">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-670">Return Value</span></span>

<span data-ttu-id="89dd4-671">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-671">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="89dd4-672">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="89dd4-672">Method helpText</span></span>

<span data-ttu-id="89dd4-673">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-673">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-674">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-674">Parameters</span></span>

<span data-ttu-id="89dd4-675">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-675">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-676">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-676">Return Value</span></span>

<span data-ttu-id="89dd4-677">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="89dd4-677">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-678">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-678">Remarks</span></span>

<span data-ttu-id="89dd4-679">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-679">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="89dd4-680">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-680">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="89dd4-681">メソッド label</span><span class="sxs-lookup"><span data-stu-id="89dd4-681">Method label</span></span>

<span data-ttu-id="89dd4-682">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-682">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-683">Parameters</span></span>

<span data-ttu-id="89dd4-684">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-684">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-685">Return Value</span></span>

<span data-ttu-id="89dd4-686">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-686">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-687">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-687">Remarks</span></span>

<span data-ttu-id="89dd4-688">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-688">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="89dd4-689">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-689">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-690">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-690">Method name</span></span>

<span data-ttu-id="89dd4-691">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-691">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-692">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-692">Parameters</span></span>

<span data-ttu-id="89dd4-693">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-693">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-694">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-694">Return Value</span></span>

<span data-ttu-id="89dd4-695">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-695">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-696">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-696">Remarks</span></span>

<span data-ttu-id="89dd4-697">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-697">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-698">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-698">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-699">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-699">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-700">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-700">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-701">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-701">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-702">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-702">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

### <a name="method-object"></a><span data-ttu-id="89dd4-703">メソッド object</span><span class="sxs-lookup"><span data-stu-id="89dd4-703">Method object</span></span>

<span data-ttu-id="89dd4-704">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-704">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-705">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-705">Parameters</span></span>

<span data-ttu-id="89dd4-706">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-706">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-707">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-707">Return Value</span></span>

<span data-ttu-id="89dd4-708">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-708">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-709">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-709">Remarks</span></span>

<span data-ttu-id="89dd4-710">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-710">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="89dd4-711">フォーム。</span><span class="sxs-lookup"><span data-stu-id="89dd4-711">Form.</span></span>
-   <span data-ttu-id="89dd4-712">レポート。</span><span class="sxs-lookup"><span data-stu-id="89dd4-712">Report.</span></span>
-   <span data-ttu-id="89dd4-713">ジョブ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-713">Job.</span></span>
-   <span data-ttu-id="89dd4-714">クラス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-714">Class.</span></span>
-   <span data-ttu-id="89dd4-715">クエリ。</span><span class="sxs-lookup"><span data-stu-id="89dd4-715">Query.</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="89dd4-716">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="89dd4-716">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-717">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-717">Parameters</span></span>

<span data-ttu-id="89dd4-718">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-718">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-719">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-719">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-720">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-720">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-721">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-721">Parameters</span></span>

<span data-ttu-id="89dd4-722">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-722">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-723">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-723">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="89dd4-724">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="89dd4-724">Method parameters</span></span>

<span data-ttu-id="89dd4-725">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-725">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-726">Parameters</span></span>

<span data-ttu-id="89dd4-727">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-728">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-728">Return Value</span></span>

<span data-ttu-id="89dd4-729">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-729">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-730">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-730">Remarks</span></span>

<span data-ttu-id="89dd4-731">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-731">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="89dd4-732">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-732">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="89dd4-733">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="89dd4-733">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-734">Parameters</span></span>

<span data-ttu-id="89dd4-735">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-736">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-736">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="89dd4-737">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-737">Method new</span></span>

<span data-ttu-id="89dd4-738">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-738">Microsoft internal use only.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-739">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-739">Parameters</span></span>

<span data-ttu-id="89dd4-740">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-740">name</span></span>  

## <a name="class-weblistdefnode"></a><span data-ttu-id="89dd4-741">クラス webListDefNode</span><span class="sxs-lookup"><span data-stu-id="89dd4-741">Class webListDefNode</span></span>
    class webListDefNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="89dd4-742">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-742">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-743">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-743">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-744">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-744">Methods</span></span>

| <span data-ttu-id="89dd4-745">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-745">Method</span></span>                                                     | <span data-ttu-id="89dd4-746">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-746">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-747">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="89dd4-747">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="89dd4-748">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-748">Returns the source code of this node.</span></span>                                                                                                     |
| <span data-ttu-id="89dd4-749">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-749">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="89dd4-750">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-750">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="89dd4-751">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-751">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="89dd4-752">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-752">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-753">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-753">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="89dd4-754">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-754">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-755">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-755">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="89dd4-756">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-756">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="89dd4-757">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-757">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="89dd4-758">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-758">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="89dd4-759">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-759">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="89dd4-760">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-760">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="89dd4-761">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-761">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="89dd4-762">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-762">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="89dd4-763">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-763">public str name(\[str value\])</span></span>                             | <span data-ttu-id="89dd4-764">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-764">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-765">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-765">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="89dd4-766">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-766">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="89dd4-767">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-767">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="89dd4-768">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-768">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="89dd4-769">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-769">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="89dd4-770">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-770">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="89dd4-771">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-771">Sets the source code of this node.</span></span>                                                                                                        |
| <span data-ttu-id="89dd4-772">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-772">public void new(str name)</span></span>                                  | <span data-ttu-id="89dd4-773">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-773">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |

### <a name="method-aotgetsource"></a><span data-ttu-id="89dd4-774">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-774">Method AOTgetSource</span></span>

<span data-ttu-id="89dd4-775">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-775">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="89dd4-776">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-776">Return Value</span></span>

<span data-ttu-id="89dd4-777">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="89dd4-777">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-778">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-778">Remarks</span></span>

<span data-ttu-id="89dd4-779">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-779">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="89dd4-780">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-780">Method changedBy</span></span>

<span data-ttu-id="89dd4-781">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-781">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-782">Parameters</span></span>

<span data-ttu-id="89dd4-783">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-783">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-784">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-784">Return Value</span></span>

<span data-ttu-id="89dd4-785">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-785">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-786">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-786">Method changedDate</span></span>

<span data-ttu-id="89dd4-787">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-787">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-788">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-788">Parameters</span></span>

<span data-ttu-id="89dd4-789">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-789">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-790">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-790">Return Value</span></span>

<span data-ttu-id="89dd4-791">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-791">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-792">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-792">Method changedTime</span></span>

<span data-ttu-id="89dd4-793">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-793">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-794">Parameters</span></span>

<span data-ttu-id="89dd4-795">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-796">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-796">Return Value</span></span>

<span data-ttu-id="89dd4-797">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-797">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-798">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-798">Method createdBy</span></span>

<span data-ttu-id="89dd4-799">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-799">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-800">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-800">Parameters</span></span>

<span data-ttu-id="89dd4-801">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-801">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-802">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-802">Return Value</span></span>

<span data-ttu-id="89dd4-803">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-803">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-804">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-804">Method creationDate</span></span>

<span data-ttu-id="89dd4-805">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-805">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-806">Parameters</span></span>

<span data-ttu-id="89dd4-807">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-808">Return Value</span></span>

<span data-ttu-id="89dd4-809">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-809">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-810">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-810">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-811">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-811">Parameters</span></span>

<span data-ttu-id="89dd4-812">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-812">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-813">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-813">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="89dd4-814">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="89dd4-814">Method helpText</span></span>

<span data-ttu-id="89dd4-815">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-815">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-816">Parameters</span></span>

<span data-ttu-id="89dd4-817">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-817">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-818">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-818">Return Value</span></span>

<span data-ttu-id="89dd4-819">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="89dd4-819">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-820">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-820">Remarks</span></span>

<span data-ttu-id="89dd4-821">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-821">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="89dd4-822">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-822">The help text must not exceed 250 characters.</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="89dd4-823">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="89dd4-823">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-824">Parameters</span></span>

<span data-ttu-id="89dd4-825">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-825">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-826">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-827">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-827">Method name</span></span>

<span data-ttu-id="89dd4-828">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-828">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-829">Parameters</span></span>

<span data-ttu-id="89dd4-830">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-831">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-831">Return Value</span></span>

<span data-ttu-id="89dd4-832">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-832">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-833">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-833">Remarks</span></span>

<span data-ttu-id="89dd4-834">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-834">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-835">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-835">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-836">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-836">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-837">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-837">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-838">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-838">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-839">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-839">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-840">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-840">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-841">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-841">Parameters</span></span>

<span data-ttu-id="89dd4-842">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-842">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-843">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-843">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="89dd4-844">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="89dd4-844">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-845">Parameters</span></span>

<span data-ttu-id="89dd4-846">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-846">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-847">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="89dd4-848">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="89dd4-848">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-849">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-849">Parameters</span></span>

<span data-ttu-id="89dd4-850">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-850">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-851">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="89dd4-852">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="89dd4-852">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-853">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-853">Parameters</span></span>

<span data-ttu-id="89dd4-854">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-854">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-855">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="89dd4-856">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="89dd4-856">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-857">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-857">Parameters</span></span>

<span data-ttu-id="89dd4-858">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-858">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-859">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="89dd4-860">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-860">Method AOTsetSource</span></span>

<span data-ttu-id="89dd4-861">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-861">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="89dd4-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-862">Parameters</span></span>

<span data-ttu-id="89dd4-863">ソース</span><span class="sxs-lookup"><span data-stu-id="89dd4-863">source</span></span>  
<span data-ttu-id="89dd4-864">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="89dd4-864">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="89dd4-865">isStatic</span><span class="sxs-lookup"><span data-stu-id="89dd4-865">isStatic</span></span>  
<span data-ttu-id="89dd4-866">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="89dd4-866">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-867">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-867">Remarks</span></span>

<span data-ttu-id="89dd4-868">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-868">This method is overridden by nodes that have source code.</span></span>

### <a name="method-new"></a><span data-ttu-id="89dd4-869">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-869">Method new</span></span>

<span data-ttu-id="89dd4-870">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-870">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-871">Parameters</span></span>

<span data-ttu-id="89dd4-872">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-872">name</span></span>  

## <a name="class-webmanagedcontentitem"></a><span data-ttu-id="89dd4-873">クラス WebManagedContentItem</span><span class="sxs-lookup"><span data-stu-id="89dd4-873">Class WebManagedContentItem</span></span>
    class WebManagedContentItem extends WebContentItem

<span data-ttu-id="89dd4-874">このクラスを使用して、コンテンツをページに追加するために EP で使用する webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-874">This class is used to create a webManagedContentItem to use in EP for adding content to pages.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-875">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-875">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-876">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-876">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-877">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-877">Methods</span></span>

| <span data-ttu-id="89dd4-878">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-878">Method</span></span>                    | <span data-ttu-id="89dd4-879">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-879">Description</span></span>                                                 |
|---------------------------|-------------------------------------------------------------|
| <span data-ttu-id="89dd4-880">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-880">public void new(str name)</span></span> | <span data-ttu-id="89dd4-881">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-881">Create a new webManagedContentItem with the passed in name.</span></span> |

### <a name="method-new"></a><span data-ttu-id="89dd4-882">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-882">Method new</span></span>

<span data-ttu-id="89dd4-883">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-883">Create a new webManagedContentItem with the passed in name.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-884">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-884">Parameters</span></span>

<span data-ttu-id="89dd4-885">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-885">name</span></span>  
<span data-ttu-id="89dd4-886">新しい webManagedContentItem に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-886">Name for the new webManagedContentItem.</span></span>

## <a name="class-webmenu"></a><span data-ttu-id="89dd4-887">クラス WebMenu</span><span class="sxs-lookup"><span data-stu-id="89dd4-887">Class WebMenu</span></span>
    class WebMenu extends TreeNode

<span data-ttu-id="89dd4-888">WebMenu クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-888">The WebMenu class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-889">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-889">Remarks</span></span>

<span data-ttu-id="89dd4-890">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-890">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-891">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-891">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-892">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-892">Methods</span></span>

| <span data-ttu-id="89dd4-893">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-893">Method</span></span>                                                                   | <span data-ttu-id="89dd4-894">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-894">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-895">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-895">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="89dd4-896">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-896">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="89dd4-897">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-897">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="89dd4-898">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-898">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-899">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-899">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="89dd4-900">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-900">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="89dd4-902">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-902">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="89dd4-903">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-903">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="89dd4-904">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-904">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="89dd4-905">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-905">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="89dd4-906">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-906">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="89dd4-907">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-907">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="89dd4-908">public boolean highlightSelected(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-908">public boolean highlightSelected(\[boolean value\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="89dd4-909">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-909">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="89dd4-910">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-910">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="89dd4-911">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-911">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="89dd4-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                               |
| <span data-ttu-id="89dd4-913">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="89dd4-913">public str menuName()</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="89dd4-914">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-914">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="89dd4-915">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-915">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-916">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-916">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="89dd4-917">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-917">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="89dd4-918">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-918">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="89dd4-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="89dd4-920">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-920">public boolean setCompany(\[boolean value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="89dd4-921">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-921">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="89dd4-922">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-922">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="89dd4-923">public void addSeparator()</span><span class="sxs-lookup"><span data-stu-id="89dd4-923">public void addSeparator()</span></span>                                               |                                                                                                                                               |
| <span data-ttu-id="89dd4-924">public void makeMenu(Object outputClass)</span><span class="sxs-lookup"><span data-stu-id="89dd4-924">public void makeMenu(Object outputClass)</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="89dd4-925">public void addSubmenu(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-925">public void addSubmenu(str name)</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="89dd4-926">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-926">public void new(str Name)</span></span>                                                | <span data-ttu-id="89dd4-927">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-927">Initializes a new instance of the TreeNode class.</span></span>                                                                                             |
| <span data-ttu-id="89dd4-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="89dd4-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="89dd4-929">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-929">Method changedBy</span></span>

<span data-ttu-id="89dd4-930">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-930">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-931">Parameters</span></span>

<span data-ttu-id="89dd4-932">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-932">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-933">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-933">Return Value</span></span>

<span data-ttu-id="89dd4-934">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-934">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-935">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-935">Method changedDate</span></span>

<span data-ttu-id="89dd4-936">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-936">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-937">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-937">Parameters</span></span>

<span data-ttu-id="89dd4-938">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-938">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-939">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-939">Return Value</span></span>

<span data-ttu-id="89dd4-940">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-940">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-941">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-941">Method changedTime</span></span>

<span data-ttu-id="89dd4-942">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-942">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-943">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-943">Parameters</span></span>

<span data-ttu-id="89dd4-944">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-944">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-945">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-945">Return Value</span></span>

<span data-ttu-id="89dd4-946">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-946">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="89dd4-947">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="89dd4-947">Method configurationKey</span></span>

<span data-ttu-id="89dd4-948">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-948">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-949">Parameters</span></span>

<span data-ttu-id="89dd4-950">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-950">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-951">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-951">Return Value</span></span>

<span data-ttu-id="89dd4-952">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="89dd4-952">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-953">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-953">Remarks</span></span>

<span data-ttu-id="89dd4-954">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-954">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="89dd4-955">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-955">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-956">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-956">Method createdBy</span></span>

<span data-ttu-id="89dd4-957">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-957">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-958">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-958">Parameters</span></span>

<span data-ttu-id="89dd4-959">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-959">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-960">Return Value</span></span>

<span data-ttu-id="89dd4-961">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-961">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-962">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-962">Method creationDate</span></span>

<span data-ttu-id="89dd4-963">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-963">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-964">Parameters</span></span>

<span data-ttu-id="89dd4-965">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-965">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-966">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-966">Return Value</span></span>

<span data-ttu-id="89dd4-967">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-967">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-968">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-968">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-969">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-969">Parameters</span></span>

<span data-ttu-id="89dd4-970">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-970">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-971">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-971">Return Value</span></span>

### <a name="method-highlightselected"></a><span data-ttu-id="89dd4-972">メソッド highlightSelected</span><span class="sxs-lookup"><span data-stu-id="89dd4-972">Method highlightSelected</span></span>

    public boolean highlightSelected([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-973">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-973">Parameters</span></span>

<span data-ttu-id="89dd4-974">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-974">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-975">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="89dd4-976">メソッド label</span><span class="sxs-lookup"><span data-stu-id="89dd4-976">Method label</span></span>

<span data-ttu-id="89dd4-977">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-977">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-978">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-978">Parameters</span></span>

<span data-ttu-id="89dd4-979">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-979">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-980">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-980">Return Value</span></span>

<span data-ttu-id="89dd4-981">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-981">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-982">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-982">Remarks</span></span>

<span data-ttu-id="89dd4-983">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-983">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="89dd4-984">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-984">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="89dd4-985">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="89dd4-985">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-986">Parameters</span></span>

<span data-ttu-id="89dd4-987">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-987">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-988">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-988">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="89dd4-989">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="89dd4-989">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-990">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-990">Parameters</span></span>

<span data-ttu-id="89dd4-991">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-991">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-992">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-992">Return Value</span></span>

### <a name="method-menuname"></a><span data-ttu-id="89dd4-993">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="89dd4-993">Method menuName</span></span>

    public str menuName()

#### <a name="return-value"></a><span data-ttu-id="89dd4-994">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-994">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-995">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-995">Method name</span></span>

<span data-ttu-id="89dd4-996">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-996">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-997">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-997">Parameters</span></span>

<span data-ttu-id="89dd4-998">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-998">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-999">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-999">Return Value</span></span>

<span data-ttu-id="89dd4-1000">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1000">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1001">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1001">Remarks</span></span>

<span data-ttu-id="89dd4-1002">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1002">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-1003">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1003">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-1004">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1004">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-1005">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1005">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-1006">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1006">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-1007">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1007">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="89dd4-1008">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="89dd4-1008">Method neededAccessLevel</span></span>

<span data-ttu-id="89dd4-1009">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1009">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1010">Parameters</span></span>

<span data-ttu-id="89dd4-1011">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1011">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1012">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1012">Return Value</span></span>

<span data-ttu-id="89dd4-1013">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1013">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1014">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1014">Remarks</span></span>

<span data-ttu-id="89dd4-1015">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1015">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="89dd4-1016">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="89dd4-1016">AccessType::NoAccess</span></span>
-   <span data-ttu-id="89dd4-1017">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="89dd4-1017">AccessType::View</span></span>
-   <span data-ttu-id="89dd4-1018">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="89dd4-1018">AccessType::Edit</span></span>
-   <span data-ttu-id="89dd4-1019">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="89dd4-1019">AccessType::Add</span></span>
-   <span data-ttu-id="89dd4-1020">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="89dd4-1020">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-1021">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-1021">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1022">Parameters</span></span>

<span data-ttu-id="89dd4-1023">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1023">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1024">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1024">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="89dd4-1025">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="89dd4-1025">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1026">Parameters</span></span>

<span data-ttu-id="89dd4-1027">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1027">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1028">Return Value</span></span>

### <a name="method-setcompany"></a><span data-ttu-id="89dd4-1029">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="89dd4-1029">Method setCompany</span></span>

    public boolean setCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1030">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1030">Parameters</span></span>

<span data-ttu-id="89dd4-1031">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1031">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1032">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="89dd4-1033">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="89dd4-1033">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1034">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1034">Parameters</span></span>

<span data-ttu-id="89dd4-1035">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1035">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1036">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1036">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="89dd4-1037">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="89dd4-1037">Method webTarget</span></span>

    public str webTarget([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1038">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1038">Parameters</span></span>

<span data-ttu-id="89dd4-1039">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1039">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1040">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1040">Return Value</span></span>

### <a name="method-addseparator"></a><span data-ttu-id="89dd4-1041">メソッド addSeparator</span><span class="sxs-lookup"><span data-stu-id="89dd4-1041">Method addSeparator</span></span>

    public void addSeparator()

### <a name="method-makemenu"></a><span data-ttu-id="89dd4-1042">メソッド makeMenu</span><span class="sxs-lookup"><span data-stu-id="89dd4-1042">Method makeMenu</span></span>

    public void makeMenu(Object outputClass)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1043">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1043">Parameters</span></span>

<span data-ttu-id="89dd4-1044">outputClass</span><span class="sxs-lookup"><span data-stu-id="89dd4-1044">outputClass</span></span>  

### <a name="method-addsubmenu"></a><span data-ttu-id="89dd4-1045">メソッド addSubmenu</span><span class="sxs-lookup"><span data-stu-id="89dd4-1045">Method addSubmenu</span></span>

    public void addSubmenu(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1046">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1046">Parameters</span></span>

<span data-ttu-id="89dd4-1047">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-1047">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="89dd4-1048">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-1048">Method new</span></span>

<span data-ttu-id="89dd4-1049">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1049">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1050">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1050">Parameters</span></span>

<span data-ttu-id="89dd4-1051">氏名</span><span class="sxs-lookup"><span data-stu-id="89dd4-1051">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="89dd4-1052">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="89dd4-1052">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1053">Parameters</span></span>

<span data-ttu-id="89dd4-1054">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="89dd4-1054">webMenuFunction</span></span>  

## <a name="class-webmenufunction"></a><span data-ttu-id="89dd4-1055">クラス WebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="89dd4-1055">Class WebMenuFunction</span></span>
    class WebMenuFunction extends SecureNode

<span data-ttu-id="89dd4-1056">WebMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1056">The WebMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-1057">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1057">Remarks</span></span>

<span data-ttu-id="89dd4-1058">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1058">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1059">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1059">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1060">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-1060">Methods</span></span>

| <span data-ttu-id="89dd4-1061">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1061">Method</span></span>                                                                                           | <span data-ttu-id="89dd4-1062">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1062">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-1063">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1063">public str changedBy(\[str value\])</span></span>                                                              | <span data-ttu-id="89dd4-1064">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1064">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="89dd4-1065">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1065">public Date changedDate(\[Date value\])</span></span>                                                          | <span data-ttu-id="89dd4-1066">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1066">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-1067">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1067">public str changedTime(\[str value\])</span></span>                                                            | <span data-ttu-id="89dd4-1068">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1068">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="89dd4-1069">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1069">public str createdBy(\[str value\])</span></span>                                                              | <span data-ttu-id="89dd4-1070">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1070">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="89dd4-1071">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1071">public Date creationDate(\[Date value\])</span></span>                                                         | <span data-ttu-id="89dd4-1072">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1072">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="89dd4-1073">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1073">public str creationTime(\[str value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="89dd4-1074">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1074">public str helpText(\[str value\])</span></span>                                                               | <span data-ttu-id="89dd4-1075">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1075">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="89dd4-1076">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1076">public str label(\[str value\])</span></span>                                                                  | <span data-ttu-id="89dd4-1077">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1077">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="89dd4-1078">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1078">public str name(\[str value\])</span></span>                                                                   | <span data-ttu-id="89dd4-1079">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1079">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-1080">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1080">public Guid origin(\[Guid value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="89dd4-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span></span> |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="89dd4-1082">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1082">Method changedBy</span></span>

<span data-ttu-id="89dd4-1083">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1083">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1084">Parameters</span></span>

<span data-ttu-id="89dd4-1085">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1085">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1086">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1086">Return Value</span></span>

<span data-ttu-id="89dd4-1087">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1087">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-1088">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1088">Method changedDate</span></span>

<span data-ttu-id="89dd4-1089">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1089">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1090">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1090">Parameters</span></span>

<span data-ttu-id="89dd4-1091">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1091">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1092">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1092">Return Value</span></span>

<span data-ttu-id="89dd4-1093">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1093">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-1094">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1094">Method changedTime</span></span>

<span data-ttu-id="89dd4-1095">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1095">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1096">Parameters</span></span>

<span data-ttu-id="89dd4-1097">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1097">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1098">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1098">Return Value</span></span>

<span data-ttu-id="89dd4-1099">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1099">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-1100">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1100">Method createdBy</span></span>

<span data-ttu-id="89dd4-1101">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1101">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1102">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1102">Parameters</span></span>

<span data-ttu-id="89dd4-1103">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1103">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1104">Return Value</span></span>

<span data-ttu-id="89dd4-1105">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1105">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-1106">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1106">Method creationDate</span></span>

<span data-ttu-id="89dd4-1107">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1107">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1108">Parameters</span></span>

<span data-ttu-id="89dd4-1109">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1109">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1110">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1110">Return Value</span></span>

<span data-ttu-id="89dd4-1111">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1111">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-1112">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1112">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1113">Parameters</span></span>

<span data-ttu-id="89dd4-1114">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1114">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1115">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1115">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="89dd4-1116">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="89dd4-1116">Method helpText</span></span>

<span data-ttu-id="89dd4-1117">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1117">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1118">Parameters</span></span>

<span data-ttu-id="89dd4-1119">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1119">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1120">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1120">Return Value</span></span>

<span data-ttu-id="89dd4-1121">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1121">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1122">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1122">Remarks</span></span>

<span data-ttu-id="89dd4-1123">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1123">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="89dd4-1124">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1124">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="89dd4-1125">メソッド label</span><span class="sxs-lookup"><span data-stu-id="89dd4-1125">Method label</span></span>

<span data-ttu-id="89dd4-1126">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1126">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1127">Parameters</span></span>

<span data-ttu-id="89dd4-1128">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1128">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1129">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1129">Return Value</span></span>

<span data-ttu-id="89dd4-1130">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1130">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1131">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1131">Remarks</span></span>

<span data-ttu-id="89dd4-1132">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1132">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="89dd4-1133">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1133">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-1134">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-1134">Method name</span></span>

<span data-ttu-id="89dd4-1135">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1135">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1136">Parameters</span></span>

<span data-ttu-id="89dd4-1137">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1137">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1138">Return Value</span></span>

<span data-ttu-id="89dd4-1139">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1139">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1140">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1140">Remarks</span></span>

<span data-ttu-id="89dd4-1141">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1141">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-1142">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1142">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-1143">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1143">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-1144">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1144">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-1145">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1145">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-1146">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1146">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-1147">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-1147">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1148">Parameters</span></span>

<span data-ttu-id="89dd4-1149">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1149">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1150">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1150">Return Value</span></span>

### <a name="method-createwebmenufunction"></a><span data-ttu-id="89dd4-1151">メソッド createWebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="89dd4-1151">Method createWebMenuFunction</span></span>

    public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1152">Parameters</span></span>

<span data-ttu-id="89dd4-1153">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-1153">name</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1154">webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="89dd4-1154">webMenuItemType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1155">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1155">Return Value</span></span>

## <a name="class-webmenuitem"></a><span data-ttu-id="89dd4-1156">クラス WebMenuItem</span><span class="sxs-lookup"><span data-stu-id="89dd4-1156">Class WebMenuItem</span></span>
    class WebMenuItem extends TreeNode

<span data-ttu-id="89dd4-1157">WebMenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1157">The WebMenuItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-1158">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1158">Remarks</span></span>

<span data-ttu-id="89dd4-1159">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1159">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="89dd4-1160">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1160">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1161">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1161">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1162">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-1162">Methods</span></span>

| <span data-ttu-id="89dd4-1163">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1163">Method</span></span>                                                         | <span data-ttu-id="89dd4-1164">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1164">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-1165">public str label()</span><span class="sxs-lookup"><span data-stu-id="89dd4-1165">public str label()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="89dd4-1166">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1166">public str menuItemName(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="89dd4-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="89dd4-1168">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1168">public str name(\[str value\])</span></span>                                 | <span data-ttu-id="89dd4-1169">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1169">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-1170">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1170">public str parameters(\[str value\])</span></span>                           | <span data-ttu-id="89dd4-1171">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1171">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="89dd4-1172">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1172">public boolean showParentModule(\[boolean value\])</span></span>             |                                                                                                                                           |

### <a name="method-label"></a><span data-ttu-id="89dd4-1173">メソッド label</span><span class="sxs-lookup"><span data-stu-id="89dd4-1173">Method label</span></span>

    public str label()

#### <a name="return-value"></a><span data-ttu-id="89dd4-1174">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1174">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="89dd4-1175">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="89dd4-1175">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1176">Parameters</span></span>

<span data-ttu-id="89dd4-1177">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1177">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1178">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1178">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="89dd4-1179">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="89dd4-1179">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1180">Parameters</span></span>

<span data-ttu-id="89dd4-1181">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1182">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1182">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-1183">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-1183">Method name</span></span>

<span data-ttu-id="89dd4-1184">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1184">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1185">Parameters</span></span>

<span data-ttu-id="89dd4-1186">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1186">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1187">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1187">Return Value</span></span>

<span data-ttu-id="89dd4-1188">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1188">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1189">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1189">Remarks</span></span>

<span data-ttu-id="89dd4-1190">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1190">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-1191">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1191">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-1192">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1192">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-1193">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1193">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-1194">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1194">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-1195">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1195">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-parameters"></a><span data-ttu-id="89dd4-1196">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="89dd4-1196">Method parameters</span></span>

<span data-ttu-id="89dd4-1197">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1197">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1198">Parameters</span></span>

<span data-ttu-id="89dd4-1199">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1199">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1200">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1200">Return Value</span></span>

<span data-ttu-id="89dd4-1201">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1201">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1202">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1202">Remarks</span></span>

<span data-ttu-id="89dd4-1203">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1203">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="89dd4-1204">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1204">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="89dd4-1205">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="89dd4-1205">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1206">Parameters</span></span>

<span data-ttu-id="89dd4-1207">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1207">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1208">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1208">Return Value</span></span>

## <a name="class-webmodulenode"></a><span data-ttu-id="89dd4-1209">クラス webModuleNode</span><span class="sxs-lookup"><span data-stu-id="89dd4-1209">Class webModuleNode</span></span>
    class webModuleNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="89dd4-1210">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1210">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1211">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1211">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1212">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-1212">Methods</span></span>

| <span data-ttu-id="89dd4-1213">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1213">Method</span></span>                                                                   | <span data-ttu-id="89dd4-1214">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1214">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-1215">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1215">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="89dd4-1216">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1216">Gets or sets the name of the user who last changed the application object.</span></span>                                                                     |
| <span data-ttu-id="89dd4-1217">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1217">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="89dd4-1218">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1218">Gets or sets the date an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="89dd4-1219">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1219">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="89dd4-1220">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1220">Gets or sets the time an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="89dd4-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="89dd4-1222">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1222">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                            |
| <span data-ttu-id="89dd4-1223">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1223">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="89dd4-1224">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1224">Gets or sets the name of the user who created the application object.</span></span>                                                                          |
| <span data-ttu-id="89dd4-1225">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1225">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="89dd4-1226">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1226">Gets or sets the date an application object was created.</span></span>                                                                                       |
| <span data-ttu-id="89dd4-1227">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1227">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="89dd4-1228">public boolean extendedDataSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1228">public boolean extendedDataSecurity(\[boolean value\])</span></span>                   |                                                                                                                                                |
| <span data-ttu-id="89dd4-1229">public boolean inheritNavigation(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1229">public boolean inheritNavigation(\[boolean value\])</span></span>                      |                                                                                                                                                |
| <span data-ttu-id="89dd4-1230">public boolean inheritPermissions(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1230">public boolean inheritPermissions(\[boolean value\])</span></span>                     |                                                                                                                                                |
| <span data-ttu-id="89dd4-1231">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1231">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="89dd4-1232">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1232">Gets or sets the label for a control.</span></span>                                                                                                          |
| <span data-ttu-id="89dd4-1233">public str masterPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1233">public str masterPage(\[str value\])</span></span>                                     |                                                                                                                                                |
| <span data-ttu-id="89dd4-1234">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1234">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="89dd4-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                                |
| <span data-ttu-id="89dd4-1236">public str moduleName()</span><span class="sxs-lookup"><span data-stu-id="89dd4-1236">public str moduleName()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="89dd4-1237">public str modulePath()</span><span class="sxs-lookup"><span data-stu-id="89dd4-1237">public str modulePath()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="89dd4-1238">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1238">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="89dd4-1239">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1239">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-1240">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1240">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="89dd4-1241">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1241">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                        |
| <span data-ttu-id="89dd4-1242">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1242">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="89dd4-1243">public boolean publicModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1243">public boolean publicModule(\[boolean value\])</span></span>                           |                                                                                                                                                |
| <span data-ttu-id="89dd4-1244">public str quickLaunch(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1244">public str quickLaunch(\[str value\])</span></span>                                    |                                                                                                                                                |
| <span data-ttu-id="89dd4-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                                |
| <span data-ttu-id="89dd4-1246">public boolean showLink(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1246">public boolean showLink(\[boolean value\])</span></span>                               |                                                                                                                                                |
| <span data-ttu-id="89dd4-1247">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1247">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                                |
| <span data-ttu-id="89dd4-1248">public void addSubModule(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1248">public void addSubModule(str name)</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="89dd4-1249">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1249">public void new(str Name)</span></span>                                                | <span data-ttu-id="89dd4-1250">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1250">Initializes a new instance of the TreeNode class.</span></span>                                                                                              |
| <span data-ttu-id="89dd4-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                                |

### <a name="method-changedby"></a><span data-ttu-id="89dd4-1252">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1252">Method changedBy</span></span>

<span data-ttu-id="89dd4-1253">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1253">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1254">Parameters</span></span>

<span data-ttu-id="89dd4-1255">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1255">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1256">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1256">Return Value</span></span>

<span data-ttu-id="89dd4-1257">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1257">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-1258">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1258">Method changedDate</span></span>

<span data-ttu-id="89dd4-1259">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1259">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1260">Parameters</span></span>

<span data-ttu-id="89dd4-1261">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1261">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1262">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1262">Return Value</span></span>

<span data-ttu-id="89dd4-1263">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1263">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-1264">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1264">Method changedTime</span></span>

<span data-ttu-id="89dd4-1265">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1265">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1266">Parameters</span></span>

<span data-ttu-id="89dd4-1267">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1267">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1268">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1268">Return Value</span></span>

<span data-ttu-id="89dd4-1269">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1269">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="89dd4-1270">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="89dd4-1270">Method configurationKey</span></span>

<span data-ttu-id="89dd4-1271">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1271">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1272">Parameters</span></span>

<span data-ttu-id="89dd4-1273">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1273">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1274">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1274">Return Value</span></span>

<span data-ttu-id="89dd4-1275">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1275">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1276">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1276">Remarks</span></span>

<span data-ttu-id="89dd4-1277">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1277">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="89dd4-1278">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1278">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-1279">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1279">Method createdBy</span></span>

<span data-ttu-id="89dd4-1280">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1280">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1281">Parameters</span></span>

<span data-ttu-id="89dd4-1282">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1282">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1283">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1283">Return Value</span></span>

<span data-ttu-id="89dd4-1284">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1284">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-1285">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1285">Method creationDate</span></span>

<span data-ttu-id="89dd4-1286">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1286">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1287">Parameters</span></span>

<span data-ttu-id="89dd4-1288">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1288">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1289">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1289">Return Value</span></span>

<span data-ttu-id="89dd4-1290">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1290">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-1291">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1291">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1292">Parameters</span></span>

<span data-ttu-id="89dd4-1293">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1293">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1294">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1294">Return Value</span></span>

### <a name="method-extendeddatasecurity"></a><span data-ttu-id="89dd4-1295">メソッド extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="89dd4-1295">Method extendedDataSecurity</span></span>

    public boolean extendedDataSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1296">Parameters</span></span>

<span data-ttu-id="89dd4-1297">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1297">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1298">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1298">Return Value</span></span>

### <a name="method-inheritnavigation"></a><span data-ttu-id="89dd4-1299">メソッド inheritNavigation</span><span class="sxs-lookup"><span data-stu-id="89dd4-1299">Method inheritNavigation</span></span>

    public boolean inheritNavigation([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1300">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1300">Parameters</span></span>

<span data-ttu-id="89dd4-1301">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1301">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1302">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1302">Return Value</span></span>

### <a name="method-inheritpermissions"></a><span data-ttu-id="89dd4-1303">メソッド inheritPermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-1303">Method inheritPermissions</span></span>

    public boolean inheritPermissions([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1304">Parameters</span></span>

<span data-ttu-id="89dd4-1305">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1305">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1306">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1306">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="89dd4-1307">メソッド label</span><span class="sxs-lookup"><span data-stu-id="89dd4-1307">Method label</span></span>

<span data-ttu-id="89dd4-1308">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1308">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1309">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1309">Parameters</span></span>

<span data-ttu-id="89dd4-1310">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1310">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1311">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1311">Return Value</span></span>

<span data-ttu-id="89dd4-1312">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1312">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1313">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1313">Remarks</span></span>

<span data-ttu-id="89dd4-1314">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1314">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="89dd4-1315">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1315">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-masterpage"></a><span data-ttu-id="89dd4-1316">メソッド masterPage</span><span class="sxs-lookup"><span data-stu-id="89dd4-1316">Method masterPage</span></span>

    public str masterPage([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1317">Parameters</span></span>

<span data-ttu-id="89dd4-1318">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1319">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1319">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="89dd4-1320">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="89dd4-1320">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1321">Parameters</span></span>

<span data-ttu-id="89dd4-1322">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1322">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1323">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1323">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="89dd4-1324">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="89dd4-1324">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1325">Parameters</span></span>

<span data-ttu-id="89dd4-1326">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1326">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1327">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1327">Return Value</span></span>

### <a name="method-modulename"></a><span data-ttu-id="89dd4-1328">メソッド moduleName</span><span class="sxs-lookup"><span data-stu-id="89dd4-1328">Method moduleName</span></span>

    public str moduleName()

#### <a name="return-value"></a><span data-ttu-id="89dd4-1329">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1329">Return Value</span></span>

### <a name="method-modulepath"></a><span data-ttu-id="89dd4-1330">メソッド modulePath</span><span class="sxs-lookup"><span data-stu-id="89dd4-1330">Method modulePath</span></span>

    public str modulePath()

#### <a name="return-value"></a><span data-ttu-id="89dd4-1331">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1331">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-1332">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-1332">Method name</span></span>

<span data-ttu-id="89dd4-1333">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1333">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1334">Parameters</span></span>

<span data-ttu-id="89dd4-1335">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1335">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1336">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1336">Return Value</span></span>

<span data-ttu-id="89dd4-1337">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1337">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1338">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1338">Remarks</span></span>

<span data-ttu-id="89dd4-1339">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1339">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-1340">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1340">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-1341">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1341">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-1342">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1342">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-1343">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1343">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-1344">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1344">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="89dd4-1345">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="89dd4-1345">Method neededAccessLevel</span></span>

<span data-ttu-id="89dd4-1346">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1346">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1347">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1347">Parameters</span></span>

<span data-ttu-id="89dd4-1348">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1348">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1349">Return Value</span></span>

<span data-ttu-id="89dd4-1350">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1350">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1351">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1351">Remarks</span></span>

<span data-ttu-id="89dd4-1352">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1352">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="89dd4-1353">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="89dd4-1353">AccessType::NoAccess</span></span>
-   <span data-ttu-id="89dd4-1354">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="89dd4-1354">AccessType::View</span></span>
-   <span data-ttu-id="89dd4-1355">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="89dd4-1355">AccessType::Edit</span></span>
-   <span data-ttu-id="89dd4-1356">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="89dd4-1356">AccessType::Add</span></span>
-   <span data-ttu-id="89dd4-1357">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="89dd4-1357">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-1358">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-1358">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1359">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1359">Parameters</span></span>

<span data-ttu-id="89dd4-1360">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1360">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1361">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1361">Return Value</span></span>

### <a name="method-publicmodule"></a><span data-ttu-id="89dd4-1362">メソッド publicModule</span><span class="sxs-lookup"><span data-stu-id="89dd4-1362">Method publicModule</span></span>

    public boolean publicModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1363">Parameters</span></span>

<span data-ttu-id="89dd4-1364">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1364">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1365">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1365">Return Value</span></span>

### <a name="method-quicklaunch"></a><span data-ttu-id="89dd4-1366">メソッド quickLaunch</span><span class="sxs-lookup"><span data-stu-id="89dd4-1366">Method quickLaunch</span></span>

    public str quickLaunch([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1367">Parameters</span></span>

<span data-ttu-id="89dd4-1368">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1368">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1369">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1369">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="89dd4-1370">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="89dd4-1370">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1371">Parameters</span></span>

<span data-ttu-id="89dd4-1372">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1372">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1373">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1373">Return Value</span></span>

### <a name="method-showlink"></a><span data-ttu-id="89dd4-1374">メソッド showLink</span><span class="sxs-lookup"><span data-stu-id="89dd4-1374">Method showLink</span></span>

    public boolean showLink([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1375">Parameters</span></span>

<span data-ttu-id="89dd4-1376">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1376">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1377">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1377">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="89dd4-1378">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="89dd4-1378">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1379">Parameters</span></span>

<span data-ttu-id="89dd4-1380">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1380">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1381">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1381">Return Value</span></span>

### <a name="method-addsubmodule"></a><span data-ttu-id="89dd4-1382">メソッド addSubModule</span><span class="sxs-lookup"><span data-stu-id="89dd4-1382">Method addSubModule</span></span>

    public void addSubModule(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1383">Parameters</span></span>

<span data-ttu-id="89dd4-1384">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-1384">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="89dd4-1385">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-1385">Method new</span></span>

<span data-ttu-id="89dd4-1386">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1386">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1387">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1387">Parameters</span></span>

<span data-ttu-id="89dd4-1388">氏名</span><span class="sxs-lookup"><span data-stu-id="89dd4-1388">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="89dd4-1389">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="89dd4-1389">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1390">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1390">Parameters</span></span>

<span data-ttu-id="89dd4-1391">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="89dd4-1391">webMenuFunction</span></span>  

## <a name="class-weboutputcontentitem"></a><span data-ttu-id="89dd4-1392">クラス WebOutputContentItem</span><span class="sxs-lookup"><span data-stu-id="89dd4-1392">Class WebOutputContentItem</span></span>
    class WebOutputContentItem extends WebContentItem

<span data-ttu-id="89dd4-1393">このクラスは、x++ の WebOutputContentItem を表します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1393">This class represents a WebOutputContentItem in x++.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-1394">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1394">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1395">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1395">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1396">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-1396">Methods</span></span>

| <span data-ttu-id="89dd4-1397">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1397">Method</span></span>                    | <span data-ttu-id="89dd4-1398">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1398">Description</span></span>                         |
|---------------------------|-------------------------------------|
| <span data-ttu-id="89dd4-1399">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1399">public void new(str name)</span></span> | <span data-ttu-id="89dd4-1400">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1400">Creates a new WebOutputContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="89dd4-1401">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-1401">Method new</span></span>

<span data-ttu-id="89dd4-1402">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1402">Creates a new WebOutputContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1403">Parameters</span></span>

<span data-ttu-id="89dd4-1404">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-1404">name</span></span>  

## <a name="class-webpagedefnode"></a><span data-ttu-id="89dd4-1405">クラス webPageDefNode</span><span class="sxs-lookup"><span data-stu-id="89dd4-1405">Class webPageDefNode</span></span>
    class webPageDefNode extends TreeNode

<span data-ttu-id="89dd4-1406">webPageDefNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1406">The webPageDefNode class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-1407">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1407">Remarks</span></span>

<span data-ttu-id="89dd4-1408">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1408">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="89dd4-1409">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1409">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1410">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1410">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1411">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-1411">Methods</span></span>

| <span data-ttu-id="89dd4-1412">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1412">Method</span></span>                                                     | <span data-ttu-id="89dd4-1413">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1413">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-1414">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="89dd4-1414">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="89dd4-1415">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1415">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="89dd4-1416">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1416">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="89dd4-1417">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1417">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="89dd4-1418">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1418">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="89dd4-1419">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1419">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-1420">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1420">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="89dd4-1421">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1421">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-1422">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1422">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="89dd4-1423">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1423">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="89dd4-1424">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1424">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="89dd4-1425">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1425">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="89dd4-1426">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1426">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="89dd4-1427">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1427">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="89dd4-1428">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1428">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="89dd4-1429">public str imageResource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1429">public str imageResource(\[str value\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="89dd4-1430">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1430">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="89dd4-1431">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1431">public str name(\[str value\])</span></span>                             | <span data-ttu-id="89dd4-1432">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1432">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-1433">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1433">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="89dd4-1434">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1434">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="89dd4-1435">public str parentPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1435">public str parentPage(\[str value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="89dd4-1436">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1436">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="89dd4-1437">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1437">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="89dd4-1438">public boolean useContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1438">public boolean useContext(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="89dd4-1439">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1439">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="89dd4-1440">public str wSSHelpTopic(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1440">public str wSSHelpTopic(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="89dd4-1441">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1441">public void new(str name)</span></span>                                  | <span data-ttu-id="89dd4-1442">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1442">Creates a new webPageDefNode.</span></span>                                                                                                             |
| <span data-ttu-id="89dd4-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="89dd4-1444">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1444">Set the source of the webPageDefNode to the given string.</span></span>                                                                                 |

### <a name="method-aotgetsource"></a><span data-ttu-id="89dd4-1445">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-1445">Method AOTgetSource</span></span>

<span data-ttu-id="89dd4-1446">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1446">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="89dd4-1447">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1447">Return Value</span></span>

<span data-ttu-id="89dd4-1448">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1448">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1449">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1449">Remarks</span></span>

<span data-ttu-id="89dd4-1450">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1450">This method is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="89dd4-1451">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1451">Method changedBy</span></span>

<span data-ttu-id="89dd4-1452">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1452">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1453">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1453">Parameters</span></span>

<span data-ttu-id="89dd4-1454">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1454">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1455">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1455">Return Value</span></span>

<span data-ttu-id="89dd4-1456">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1456">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-1457">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1457">Method changedDate</span></span>

<span data-ttu-id="89dd4-1458">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1458">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1459">Parameters</span></span>

<span data-ttu-id="89dd4-1460">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1460">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1461">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1461">Return Value</span></span>

<span data-ttu-id="89dd4-1462">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1462">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-1463">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1463">Method changedTime</span></span>

<span data-ttu-id="89dd4-1464">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1464">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1465">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1465">Parameters</span></span>

<span data-ttu-id="89dd4-1466">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1466">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1467">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1467">Return Value</span></span>

<span data-ttu-id="89dd4-1468">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1468">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-1469">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1469">Method createdBy</span></span>

<span data-ttu-id="89dd4-1470">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1470">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1471">Parameters</span></span>

<span data-ttu-id="89dd4-1472">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1472">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1473">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1473">Return Value</span></span>

<span data-ttu-id="89dd4-1474">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1474">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-1475">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1475">Method creationDate</span></span>

<span data-ttu-id="89dd4-1476">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1476">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1477">Parameters</span></span>

<span data-ttu-id="89dd4-1478">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1478">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1479">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1479">Return Value</span></span>

<span data-ttu-id="89dd4-1480">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1480">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-1481">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1481">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1482">Parameters</span></span>

<span data-ttu-id="89dd4-1483">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1484">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1484">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="89dd4-1485">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="89dd4-1485">Method helpText</span></span>

<span data-ttu-id="89dd4-1486">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1486">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1487">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1487">Parameters</span></span>

<span data-ttu-id="89dd4-1488">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1488">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1489">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1489">Return Value</span></span>

<span data-ttu-id="89dd4-1490">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1490">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1491">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1491">Remarks</span></span>

<span data-ttu-id="89dd4-1492">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1492">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="89dd4-1493">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1493">The help text must not exceed 250 characters.</span></span>

### <a name="method-imageresource"></a><span data-ttu-id="89dd4-1494">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="89dd4-1494">Method imageResource</span></span>

    public str imageResource([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1495">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1495">Parameters</span></span>

<span data-ttu-id="89dd4-1496">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1496">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1497">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1497">Return Value</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="89dd4-1498">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="89dd4-1498">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1499">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1499">Parameters</span></span>

<span data-ttu-id="89dd4-1500">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1500">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1501">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-1502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-1502">Method name</span></span>

<span data-ttu-id="89dd4-1503">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1503">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1504">Parameters</span></span>

<span data-ttu-id="89dd4-1505">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1505">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1506">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1506">Return Value</span></span>

<span data-ttu-id="89dd4-1507">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1507">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1508">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1508">Remarks</span></span>

<span data-ttu-id="89dd4-1509">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1509">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-1510">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1510">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-1511">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1511">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-1512">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1512">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-1513">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1513">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-1514">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1514">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-1515">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-1515">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1516">Parameters</span></span>

<span data-ttu-id="89dd4-1517">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1517">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1518">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1518">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="89dd4-1519">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="89dd4-1519">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1520">Parameters</span></span>

<span data-ttu-id="89dd4-1521">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1521">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1522">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1522">Return Value</span></span>

### <a name="method-parentpage"></a><span data-ttu-id="89dd4-1523">メソッド parentPage</span><span class="sxs-lookup"><span data-stu-id="89dd4-1523">Method parentPage</span></span>

    public str parentPage([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1524">Parameters</span></span>

<span data-ttu-id="89dd4-1525">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1525">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1526">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1526">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="89dd4-1527">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="89dd4-1527">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1528">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1528">Parameters</span></span>

<span data-ttu-id="89dd4-1529">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1529">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1530">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1530">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="89dd4-1531">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="89dd4-1531">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1532">Parameters</span></span>

<span data-ttu-id="89dd4-1533">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1533">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1534">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1534">Return Value</span></span>

### <a name="method-usecontext"></a><span data-ttu-id="89dd4-1535">メソッド useContext</span><span class="sxs-lookup"><span data-stu-id="89dd4-1535">Method useContext</span></span>

    public boolean useContext([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1536">Parameters</span></span>

<span data-ttu-id="89dd4-1537">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1538">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1538">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="89dd4-1539">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="89dd4-1539">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1540">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1540">Parameters</span></span>

<span data-ttu-id="89dd4-1541">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1541">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1542">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1542">Return Value</span></span>

### <a name="method-wsshelptopic"></a><span data-ttu-id="89dd4-1543">メソッド wSSHelpTopic</span><span class="sxs-lookup"><span data-stu-id="89dd4-1543">Method wSSHelpTopic</span></span>

    public str wSSHelpTopic([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1544">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1544">Parameters</span></span>

<span data-ttu-id="89dd4-1545">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1545">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1546">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1546">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="89dd4-1547">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-1547">Method new</span></span>

<span data-ttu-id="89dd4-1548">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1548">Creates a new webPageDefNode.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1549">Parameters</span></span>

<span data-ttu-id="89dd4-1550">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-1550">name</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="89dd4-1551">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-1551">Method AOTsetSource</span></span>

<span data-ttu-id="89dd4-1552">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1552">Set the source of the webPageDefNode to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1553">Parameters</span></span>

<span data-ttu-id="89dd4-1554">ソース</span><span class="sxs-lookup"><span data-stu-id="89dd4-1554">source</span></span>  
<span data-ttu-id="89dd4-1555">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1555">Optional parameter marking if the source provided is static.</span></span>

<!-- -->

<span data-ttu-id="89dd4-1556">isStatic</span><span class="sxs-lookup"><span data-stu-id="89dd4-1556">isStatic</span></span>  
<span data-ttu-id="89dd4-1557">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1557">Optional parameter marking if the source provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1558">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1558">Remarks</span></span>

<span data-ttu-id="89dd4-1559">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1559">This method is overridden by nodes which have source code.</span></span>

## <a name="class-webstaticfilenode"></a><span data-ttu-id="89dd4-1560">クラス webStaticFileNode</span><span class="sxs-lookup"><span data-stu-id="89dd4-1560">Class webStaticFileNode</span></span>
    class webStaticFileNode extends TreeNode

<span data-ttu-id="89dd4-1561">webStaticFileNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1561">The webStaticFileNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-1562">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1562">Remarks</span></span>

<span data-ttu-id="89dd4-1563">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1563">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1564">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1564">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1565">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-1565">Methods</span></span>

| <span data-ttu-id="89dd4-1566">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1566">Method</span></span>                                                     | <span data-ttu-id="89dd4-1567">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1567">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-1568">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="89dd4-1568">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="89dd4-1569">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1569">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="89dd4-1570">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1570">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="89dd4-1571">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1571">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="89dd4-1572">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1572">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="89dd4-1573">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1573">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-1574">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1574">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="89dd4-1575">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1575">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="89dd4-1576">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1576">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="89dd4-1577">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1577">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="89dd4-1578">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1578">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="89dd4-1579">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1579">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="89dd4-1580">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1580">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="89dd4-1581">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1581">public str filename(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="89dd4-1582">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1582">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="89dd4-1583">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1583">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="89dd4-1584">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1584">public str name(\[str value\])</span></span>                             | <span data-ttu-id="89dd4-1585">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1585">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="89dd4-1586">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1586">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="89dd4-1587">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1587">public str relativePath(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="89dd4-1588">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1588">public str version(\[str value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="89dd4-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="89dd4-1590">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1590">Sets the source of the static file node to the given string.</span></span>                                                                              |

### <a name="method-aotgetsource"></a><span data-ttu-id="89dd4-1591">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-1591">Method AOTgetSource</span></span>

<span data-ttu-id="89dd4-1592">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1592">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="89dd4-1593">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1593">Return Value</span></span>

<span data-ttu-id="89dd4-1594">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1594">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1595">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1595">Remarks</span></span>

<span data-ttu-id="89dd4-1596">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1596">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="89dd4-1597">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1597">Method changedBy</span></span>

<span data-ttu-id="89dd4-1598">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1598">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1599">Parameters</span></span>

<span data-ttu-id="89dd4-1600">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1600">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1601">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1601">Return Value</span></span>

<span data-ttu-id="89dd4-1602">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1602">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="89dd4-1603">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1603">Method changedDate</span></span>

<span data-ttu-id="89dd4-1604">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1604">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1605">Parameters</span></span>

<span data-ttu-id="89dd4-1606">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1606">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1607">Return Value</span></span>

<span data-ttu-id="89dd4-1608">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1608">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="89dd4-1609">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1609">Method changedTime</span></span>

<span data-ttu-id="89dd4-1610">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1610">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1611">Parameters</span></span>

<span data-ttu-id="89dd4-1612">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1612">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1613">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1613">Return Value</span></span>

<span data-ttu-id="89dd4-1614">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1614">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="89dd4-1615">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="89dd4-1615">Method createdBy</span></span>

<span data-ttu-id="89dd4-1616">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1616">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1617">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1617">Parameters</span></span>

<span data-ttu-id="89dd4-1618">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1618">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1619">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1619">Return Value</span></span>

<span data-ttu-id="89dd4-1620">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1620">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="89dd4-1621">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="89dd4-1621">Method creationDate</span></span>

<span data-ttu-id="89dd4-1622">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1622">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1623">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1623">Parameters</span></span>

<span data-ttu-id="89dd4-1624">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1624">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1625">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1625">Return Value</span></span>

<span data-ttu-id="89dd4-1626">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1626">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="89dd4-1627">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="89dd4-1627">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1628">Parameters</span></span>

<span data-ttu-id="89dd4-1629">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1630">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1630">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="89dd4-1631">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="89dd4-1631">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1632">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1632">Parameters</span></span>

<span data-ttu-id="89dd4-1633">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1633">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1634">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1634">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="89dd4-1635">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="89dd4-1635">Method helpText</span></span>

<span data-ttu-id="89dd4-1636">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1636">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1637">Parameters</span></span>

<span data-ttu-id="89dd4-1638">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1638">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1639">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1639">Return Value</span></span>

<span data-ttu-id="89dd4-1640">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1640">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1641">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1641">Remarks</span></span>

<span data-ttu-id="89dd4-1642">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1642">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="89dd4-1643">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1643">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="89dd4-1644">メソッド名</span><span class="sxs-lookup"><span data-stu-id="89dd4-1644">Method name</span></span>

<span data-ttu-id="89dd4-1645">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1645">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1646">Parameters</span></span>

<span data-ttu-id="89dd4-1647">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1648">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1648">Return Value</span></span>

<span data-ttu-id="89dd4-1649">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1649">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1650">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1650">Remarks</span></span>

<span data-ttu-id="89dd4-1651">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1651">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="89dd4-1652">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1652">Begins with a letter.</span></span>
-   <span data-ttu-id="89dd4-1653">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1653">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="89dd4-1654">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1654">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="89dd4-1655">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1655">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="89dd4-1656">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1656">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-1657">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-1657">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1658">Parameters</span></span>

<span data-ttu-id="89dd4-1659">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1659">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1660">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1660">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="89dd4-1661">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="89dd4-1661">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1662">Parameters</span></span>

<span data-ttu-id="89dd4-1663">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1664">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1664">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="89dd4-1665">メソッド version</span><span class="sxs-lookup"><span data-stu-id="89dd4-1665">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1666">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1666">Parameters</span></span>

<span data-ttu-id="89dd4-1667">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1667">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1668">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1668">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="89dd4-1669">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="89dd4-1669">Method AOTsetSource</span></span>

<span data-ttu-id="89dd4-1670">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1670">Sets the source of the static file node to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1671">Parameters</span></span>

<span data-ttu-id="89dd4-1672">ソース</span><span class="sxs-lookup"><span data-stu-id="89dd4-1672">source</span></span>  
<span data-ttu-id="89dd4-1673">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1673">An optional parameter that marks whether the source that is provided is static.</span></span>

<!-- -->

<span data-ttu-id="89dd4-1674">isStatic</span><span class="sxs-lookup"><span data-stu-id="89dd4-1674">isStatic</span></span>  
<span data-ttu-id="89dd4-1675">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1675">An optional parameter that marks whether the source that is provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1676">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1676">Remarks</span></span>

<span data-ttu-id="89dd4-1677">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1677">This method is overridden by nodes that have source code.</span></span>

## <a name="class-weburlmenufunction"></a><span data-ttu-id="89dd4-1678">クラス WebUrlMenuFunction</span><span class="sxs-lookup"><span data-stu-id="89dd4-1678">Class WebUrlMenuFunction</span></span>
    class WebUrlMenuFunction extends WebMenuFunction

<span data-ttu-id="89dd4-1679">WebUrlMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1679">The WebUrlMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="89dd4-1680">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1680">Remarks</span></span>

<span data-ttu-id="89dd4-1681">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1681">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1682">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1682">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1683">メソッド</span><span class="sxs-lookup"><span data-stu-id="89dd4-1683">Methods</span></span>

| <span data-ttu-id="89dd4-1684">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1684">Method</span></span>                                                | <span data-ttu-id="89dd4-1685">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1685">Description</span></span>                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dd4-1686">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1686">public boolean big(\[boolean value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="89dd4-1687">public int closeDialogBehavior(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1687">public int closeDialogBehavior(\[int value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="89dd4-1688">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1688">public int correctPermissions(\[int value\])</span></span>          |                                                                                                        |
| <span data-ttu-id="89dd4-1689">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1689">public int createPermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="89dd4-1690">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1690">public int deletePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="89dd4-1691">public boolean hideActionPane(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1691">public boolean hideActionPane(\[boolean value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="89dd4-1692">public boolean homePage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1692">public boolean homePage(\[boolean value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="89dd4-1693">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1693">public int imageLocation(\[int value\])</span></span>               |                                                                                                        |
| <span data-ttu-id="89dd4-1694">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1694">public str linkedPermissionObject(\[str value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="89dd4-1695">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1695">public str linkedPermissionObjectChild(\[str value\])</span></span> |                                                                                                        |
| <span data-ttu-id="89dd4-1696">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1696">public int linkedPermissionType(\[int value\])</span></span>        |                                                                                                        |
| <span data-ttu-id="89dd4-1697">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1697">public int maintainUserLicense(\[int value\])</span></span>         | <span data-ttu-id="89dd4-1698">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1698">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="89dd4-1699">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1699">public boolean multiSelect(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="89dd4-1700">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1700">public boolean needsRecord(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="89dd4-1701">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1701">public str normalImage(\[str value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="89dd4-1702">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1702">public int normalResource(\[int value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="89dd4-1703">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1703">public Guid origin(\[Guid value\])</span></span>                    |                                                                                                        |
| <span data-ttu-id="89dd4-1704">public str pageDefinition(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1704">public str pageDefinition(\[str value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="89dd4-1705">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1705">public str parameters(\[str value\])</span></span>                  | <span data-ttu-id="89dd4-1706">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1706">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span> |
| <span data-ttu-id="89dd4-1707">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1707">public int readPermissions(\[int value\])</span></span>             |                                                                                                        |
| <span data-ttu-id="89dd4-1708">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1708">public int updatePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="89dd4-1709">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1709">public str uRL(\[str value\])</span></span>                         |                                                                                                        |
| <span data-ttu-id="89dd4-1710">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1710">public int viewUserLicense(\[int value\])</span></span>             | <span data-ttu-id="89dd4-1711">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1711">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="89dd4-1712">public int windowMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1712">public int windowMode(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="89dd4-1713">public str windowParameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1713">public str windowParameters(\[str value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="89dd4-1714">public int windowSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1714">public int windowSize(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="89dd4-1715">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1715">public void new(str name)</span></span>                             | <span data-ttu-id="89dd4-1716">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1716">Initializes a new instance of the TreeNode class.</span></span>                                                      |

### <a name="method-big"></a><span data-ttu-id="89dd4-1717">メソッド big</span><span class="sxs-lookup"><span data-stu-id="89dd4-1717">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1718">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1718">Parameters</span></span>

<span data-ttu-id="89dd4-1719">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1719">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1720">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1720">Return Value</span></span>

### <a name="method-closedialogbehavior"></a><span data-ttu-id="89dd4-1721">メソッド closeDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="89dd4-1721">Method closeDialogBehavior</span></span>

    public int closeDialogBehavior([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1722">Parameters</span></span>

<span data-ttu-id="89dd4-1723">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1723">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1724">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1724">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="89dd4-1725">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-1725">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1726">Parameters</span></span>

<span data-ttu-id="89dd4-1727">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1728">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1728">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="89dd4-1729">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-1729">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1730">Parameters</span></span>

<span data-ttu-id="89dd4-1731">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1731">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1732">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1732">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="89dd4-1733">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-1733">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1734">Parameters</span></span>

<span data-ttu-id="89dd4-1735">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1736">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1736">Return Value</span></span>

### <a name="method-hideactionpane"></a><span data-ttu-id="89dd4-1737">メソッド hideActionPane</span><span class="sxs-lookup"><span data-stu-id="89dd4-1737">Method hideActionPane</span></span>

    public boolean hideActionPane([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1738">Parameters</span></span>

<span data-ttu-id="89dd4-1739">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1739">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1740">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1740">Return Value</span></span>

### <a name="method-homepage"></a><span data-ttu-id="89dd4-1741">メソッド homePage</span><span class="sxs-lookup"><span data-stu-id="89dd4-1741">Method homePage</span></span>

    public boolean homePage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1742">Parameters</span></span>

<span data-ttu-id="89dd4-1743">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1743">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1744">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1744">Return Value</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="89dd4-1745">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="89dd4-1745">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1746">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1746">Parameters</span></span>

<span data-ttu-id="89dd4-1747">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1747">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1748">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1748">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="89dd4-1749">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="89dd4-1749">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1750">Parameters</span></span>

<span data-ttu-id="89dd4-1751">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1751">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1752">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1752">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="89dd4-1753">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="89dd4-1753">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1754">Parameters</span></span>

<span data-ttu-id="89dd4-1755">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1755">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1756">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1756">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="89dd4-1757">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="89dd4-1757">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1758">Parameters</span></span>

<span data-ttu-id="89dd4-1759">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1759">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1760">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1760">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="89dd4-1761">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="89dd4-1761">Method maintainUserLicense</span></span>

<span data-ttu-id="89dd4-1762">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1762">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1763">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1763">Parameters</span></span>

<span data-ttu-id="89dd4-1764">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1764">value</span></span>  
<span data-ttu-id="89dd4-1765">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1765">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89dd4-1766">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1766">Return Value</span></span>

<span data-ttu-id="89dd4-1767">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1767">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="89dd4-1768">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="89dd4-1768">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1769">Parameters</span></span>

<span data-ttu-id="89dd4-1770">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1770">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1771">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1771">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="89dd4-1772">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="89dd4-1772">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1773">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1773">Parameters</span></span>

<span data-ttu-id="89dd4-1774">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1774">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1775">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1775">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="89dd4-1776">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="89dd4-1776">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1777">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1777">Parameters</span></span>

<span data-ttu-id="89dd4-1778">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1778">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1779">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1779">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="89dd4-1780">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="89dd4-1780">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1781">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1781">Parameters</span></span>

<span data-ttu-id="89dd4-1782">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1782">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1783">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1783">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="89dd4-1784">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="89dd4-1784">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1785">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1785">Parameters</span></span>

<span data-ttu-id="89dd4-1786">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1786">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1787">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1787">Return Value</span></span>

### <a name="method-pagedefinition"></a><span data-ttu-id="89dd4-1788">メソッド pageDefinition</span><span class="sxs-lookup"><span data-stu-id="89dd4-1788">Method pageDefinition</span></span>

    public str pageDefinition([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1789">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1789">Parameters</span></span>

<span data-ttu-id="89dd4-1790">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1790">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1791">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1791">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="89dd4-1792">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="89dd4-1792">Method parameters</span></span>

<span data-ttu-id="89dd4-1793">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1793">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1794">Parameters</span></span>

<span data-ttu-id="89dd4-1795">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1796">Return Value</span></span>

<span data-ttu-id="89dd4-1797">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1797">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89dd4-1798">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1798">Remarks</span></span>

<span data-ttu-id="89dd4-1799">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1799">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="89dd4-1800">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1800">Objects will ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="89dd4-1801">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-1801">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1802">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1802">Parameters</span></span>

<span data-ttu-id="89dd4-1803">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1803">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1804">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1804">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="89dd4-1805">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="89dd4-1805">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1806">Parameters</span></span>

<span data-ttu-id="89dd4-1807">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1808">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1808">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="89dd4-1809">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="89dd4-1809">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1810">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1810">Parameters</span></span>

<span data-ttu-id="89dd4-1811">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1811">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1812">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1812">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="89dd4-1813">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="89dd4-1813">Method viewUserLicense</span></span>

<span data-ttu-id="89dd4-1814">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1814">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1815">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1815">Parameters</span></span>

<span data-ttu-id="89dd4-1816">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1816">value</span></span>  
<span data-ttu-id="89dd4-1817">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1817">A user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89dd4-1818">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1818">Return Value</span></span>

<span data-ttu-id="89dd4-1819">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1819">The user license.</span></span>

### <a name="method-windowmode"></a><span data-ttu-id="89dd4-1820">メソッド windowMode</span><span class="sxs-lookup"><span data-stu-id="89dd4-1820">Method windowMode</span></span>

    public int windowMode([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1821">Parameters</span></span>

<span data-ttu-id="89dd4-1822">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1822">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1823">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1823">Return Value</span></span>

### <a name="method-windowparameters"></a><span data-ttu-id="89dd4-1824">メソッド windowParameters</span><span class="sxs-lookup"><span data-stu-id="89dd4-1824">Method windowParameters</span></span>

    public str windowParameters([str value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1825">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1825">Parameters</span></span>

<span data-ttu-id="89dd4-1826">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1826">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1827">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1827">Return Value</span></span>

### <a name="method-windowsize"></a><span data-ttu-id="89dd4-1828">メソッド windowSize</span><span class="sxs-lookup"><span data-stu-id="89dd4-1828">Method windowSize</span></span>

    public int windowSize([int value])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1829">Parameters</span></span>

<span data-ttu-id="89dd4-1830">値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1831">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1831">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="89dd4-1832">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-1832">Method new</span></span>

<span data-ttu-id="89dd4-1833">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1833">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1834">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1834">Parameters</span></span>

<span data-ttu-id="89dd4-1835">名前</span><span class="sxs-lookup"><span data-stu-id="89dd4-1835">name</span></span>  

## <a name="class-winapinative"></a><span data-ttu-id="89dd4-1836">クラス WinAPINative</span><span class="sxs-lookup"><span data-stu-id="89dd4-1836">Class WinAPINative</span></span>
    class WinAPINative extends Object

### <a name="remarks"></a><span data-ttu-id="89dd4-1837">備考</span><span class="sxs-lookup"><span data-stu-id="89dd4-1837">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="89dd4-1838">例</span><span class="sxs-lookup"><span data-stu-id="89dd4-1838">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="89dd4-1839">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1839">Methods</span></span>

| <span data-ttu-id="89dd4-1840">方法</span><span class="sxs-lookup"><span data-stu-id="89dd4-1840">Method</span></span>                                                                                                                  | <span data-ttu-id="89dd4-1841">説明</span><span class="sxs-lookup"><span data-stu-id="89dd4-1841">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="89dd4-1842">::public static Int64 createFontIndirect(Binary logfont)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1842">::public static Int64 createFontIndirect(Binary logfont)</span></span>                                                                |                                                       |
| <span data-ttu-id="89dd4-1843">::public static boolean deleteObject(Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1843">::public static boolean deleteObject(Int64 hGDIObject)</span></span>                                                                  |                                                       |
| <span data-ttu-id="89dd4-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span></span> |                                                       |
| <span data-ttu-id="89dd4-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span></span>                                                                 |                                                       |
| <span data-ttu-id="89dd4-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span></span>                              |                                                       |
| <span data-ttu-id="89dd4-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span><span class="sxs-lookup"><span data-stu-id="89dd4-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span></span>                                                    |                                                       |
| <span data-ttu-id="89dd4-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span></span>                                           |                                                       |
| <span data-ttu-id="89dd4-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span></span>                                                       |                                                       |
| <span data-ttu-id="89dd4-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span></span>                        |                                                       |
| <span data-ttu-id="89dd4-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="89dd4-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span></span>                                                         |                                                       |
| <span data-ttu-id="89dd4-1852">private void new()</span><span class="sxs-lookup"><span data-stu-id="89dd4-1852">private void new()</span></span>                                                                                                      | <span data-ttu-id="89dd4-1853">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1853">Initializes a new instance of the WinAPINative class.</span></span> |

### <a name="method-createfontindirect"></a><span data-ttu-id="89dd4-1854">メソッド createFontIndirect</span><span class="sxs-lookup"><span data-stu-id="89dd4-1854">Method createFontIndirect</span></span>

    public static Int64 createFontIndirect(Binary logfont)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1855">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1855">Parameters</span></span>

<span data-ttu-id="89dd4-1856">logfont</span><span class="sxs-lookup"><span data-stu-id="89dd4-1856">logfont</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1857">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1857">Return Value</span></span>

### <a name="method-deleteobject"></a><span data-ttu-id="89dd4-1858">メソッド deleteObject</span><span class="sxs-lookup"><span data-stu-id="89dd4-1858">Method deleteObject</span></span>

    public static boolean deleteObject(Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1859">Parameters</span></span>

<span data-ttu-id="89dd4-1860">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="89dd4-1860">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1861">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1861">Return Value</span></span>

### <a name="method-getcharabcwidthsi"></a><span data-ttu-id="89dd4-1862">メソッド getCharABCWidthsI</span><span class="sxs-lookup"><span data-stu-id="89dd4-1862">Method getCharABCWidthsI</span></span>

    public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1863">Parameters</span></span>

<span data-ttu-id="89dd4-1864">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1864">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1865">firstGlyphIndex</span><span class="sxs-lookup"><span data-stu-id="89dd4-1865">firstGlyphIndex</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1866">glyphIndicesCount</span><span class="sxs-lookup"><span data-stu-id="89dd4-1866">glyphIndicesCount</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1867">charWidths</span><span class="sxs-lookup"><span data-stu-id="89dd4-1867">charWidths</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1868">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1868">Return Value</span></span>

### <a name="method-getdevicecaps"></a><span data-ttu-id="89dd4-1869">メソッド getDeviceCaps</span><span class="sxs-lookup"><span data-stu-id="89dd4-1869">Method getDeviceCaps</span></span>

    public static int getDeviceCaps(Int64 hDC, int index)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1870">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1870">Parameters</span></span>

<span data-ttu-id="89dd4-1871">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1871">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1872">指数</span><span class="sxs-lookup"><span data-stu-id="89dd4-1872">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1873">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1873">Return Value</span></span>

### <a name="method-getfontdata"></a><span data-ttu-id="89dd4-1874">メソッド getFontData</span><span class="sxs-lookup"><span data-stu-id="89dd4-1874">Method getFontData</span></span>

    public static int getFontData(Int64 hDC, int dwTable, int dwOffset, [Binary pvBuffer])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1875">Parameters</span></span>

<span data-ttu-id="89dd4-1876">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1876">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1877">dwTable</span><span class="sxs-lookup"><span data-stu-id="89dd4-1877">dwTable</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1878">dwOffset</span><span class="sxs-lookup"><span data-stu-id="89dd4-1878">dwOffset</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1879">pvBuffer</span><span class="sxs-lookup"><span data-stu-id="89dd4-1879">pvBuffer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1880">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1880">Return Value</span></span>

### <a name="method-getfontunicoderanges"></a><span data-ttu-id="89dd4-1881">メソッド getFontUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="89dd4-1881">Method getFontUnicodeRanges</span></span>

    public static int getFontUnicodeRanges(Int64 hDC, [Binary lpgs])

#### <a name="parameters"></a><span data-ttu-id="89dd4-1882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1882">Parameters</span></span>

<span data-ttu-id="89dd4-1883">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1883">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1884">lpgs</span><span class="sxs-lookup"><span data-stu-id="89dd4-1884">lpgs</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1885">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1885">Return Value</span></span>

### <a name="method-getglyphindices"></a><span data-ttu-id="89dd4-1886">メソッド getGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="89dd4-1886">Method getGlyphIndices</span></span>

    public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1887">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1887">Parameters</span></span>

<span data-ttu-id="89dd4-1888">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1888">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1889">lpstr</span><span class="sxs-lookup"><span data-stu-id="89dd4-1889">lpstr</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1890">pgi</span><span class="sxs-lookup"><span data-stu-id="89dd4-1890">pgi</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1891">fl</span><span class="sxs-lookup"><span data-stu-id="89dd4-1891">fl</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1892">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1892">Return Value</span></span>

### <a name="method-gettextmetrics"></a><span data-ttu-id="89dd4-1893">メソッド getTextMetrics</span><span class="sxs-lookup"><span data-stu-id="89dd4-1893">Method getTextMetrics</span></span>

    public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1894">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1894">Parameters</span></span>

<span data-ttu-id="89dd4-1895">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1895">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1896">lpMetrics</span><span class="sxs-lookup"><span data-stu-id="89dd4-1896">lpMetrics</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1897">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1897">Return Value</span></span>

### <a name="method-getuniscribeglyphindices"></a><span data-ttu-id="89dd4-1898">メソッド getUniscribeGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="89dd4-1898">Method getUniscribeGlyphIndices</span></span>

    public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1899">Parameters</span></span>

<span data-ttu-id="89dd4-1900">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1900">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1901">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="89dd4-1901">hGDIObject</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1902">lpstr</span><span class="sxs-lookup"><span data-stu-id="89dd4-1902">lpstr</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1903">pgi</span><span class="sxs-lookup"><span data-stu-id="89dd4-1903">pgi</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1904">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1904">Return Value</span></span>

### <a name="method-selectobject"></a><span data-ttu-id="89dd4-1905">メソッド selectObject</span><span class="sxs-lookup"><span data-stu-id="89dd4-1905">Method selectObject</span></span>

    public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="89dd4-1906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dd4-1906">Parameters</span></span>

<span data-ttu-id="89dd4-1907">hDC</span><span class="sxs-lookup"><span data-stu-id="89dd4-1907">hDC</span></span>  

<!-- -->

<span data-ttu-id="89dd4-1908">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="89dd4-1908">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="89dd4-1909">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dd4-1909">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="89dd4-1910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89dd4-1910">Method new</span></span>

<span data-ttu-id="89dd4-1911">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89dd4-1911">Initializes a new instance of the WinAPINative class.</span></span>

    private void new()



