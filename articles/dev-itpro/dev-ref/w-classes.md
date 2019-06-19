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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 55901
ms.assetid: ca08dc94-1481-4ac0-80f4-d092da5c1c90
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62d632a0bc881c3f310de2e0899e66e6d91f0fc8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544185"
---
# <a name="w-classes"></a><span data-ttu-id="49f4a-103">W クラス</span><span class="sxs-lookup"><span data-stu-id="49f4a-103">W classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49f4a-104">文字 W で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-104">System API classes that start with the letter W.</span></span>

<a name="class-webactionmenufunction"></a><span data-ttu-id="49f4a-105">クラス WebActionMenuFunction</span><span class="sxs-lookup"><span data-stu-id="49f4a-105">Class WebActionMenuFunction</span></span>
---------------------------

    class WebActionMenuFunction extends WebMenuFunction

<span data-ttu-id="49f4a-106">WebActionMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-106">The WebActionMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-107">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-107">Remarks</span></span>

<span data-ttu-id="49f4a-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-109">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-109">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-110">Methods</span></span>

| <span data-ttu-id="49f4a-111">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-111">Method</span></span>                                                   | <span data-ttu-id="49f4a-112">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-112">Description</span></span>                                                                                                 |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-113">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-113">public boolean big(\[boolean value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="49f4a-114">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-114">public int correctPermissions(\[int value\])</span></span>             |                                                                                                             |
| <span data-ttu-id="49f4a-115">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-115">public int createPermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="49f4a-116">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-116">public int deletePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="49f4a-117">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-117">public int enumParameter(\[int value\])</span></span>                  | <span data-ttu-id="49f4a-118">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-118">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span> |
| <span data-ttu-id="49f4a-119">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-119">public EnumId enumTypeParameter(\[EnumId value\])</span></span>        | <span data-ttu-id="49f4a-120">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-120">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                     |
| <span data-ttu-id="49f4a-121">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-121">public int imageLocation(\[int value\])</span></span>                  |                                                                                                             |
| <span data-ttu-id="49f4a-122">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-122">public str linkedPermissionObject(\[str value\])</span></span>         |                                                                                                             |
| <span data-ttu-id="49f4a-123">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-123">public str linkedPermissionObjectChild(\[str value\])</span></span>    |                                                                                                             |
| <span data-ttu-id="49f4a-124">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-124">public int linkedPermissionType(\[int value\])</span></span>           |                                                                                                             |
| <span data-ttu-id="49f4a-125">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-125">public int maintainUserLicense(\[int value\])</span></span>            | <span data-ttu-id="49f4a-126">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-126">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="49f4a-127">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-127">public boolean multiSelect(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="49f4a-128">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-128">public boolean needsRecord(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="49f4a-129">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-129">public str normalImage(\[str value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="49f4a-130">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-130">public int normalResource(\[int value\])</span></span>                 |                                                                                                             |
| <span data-ttu-id="49f4a-131">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-131">public str object(\[str value\])</span></span>                         | <span data-ttu-id="49f4a-132">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-132">Gets or sets the object that the MenuFunction class runs.</span></span>                                                   |
| <span data-ttu-id="49f4a-133">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-133">public int objectType(\[int value\])</span></span>                     |                                                                                                             |
| <span data-ttu-id="49f4a-134">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-134">public Guid origin(\[Guid value\])</span></span>                       |                                                                                                             |
| <span data-ttu-id="49f4a-135">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-135">public str parameters(\[str value\])</span></span>                     | <span data-ttu-id="49f4a-136">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-136">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>      |
| <span data-ttu-id="49f4a-137">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-137">public int readPermissions(\[int value\])</span></span>                |                                                                                                             |
| <span data-ttu-id="49f4a-138">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-138">public str reportDesign(\[str value\])</span></span>                   |                                                                                                             |
| <span data-ttu-id="49f4a-139">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-139">public int runOn(\[int value\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="49f4a-140">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-140">public int updatePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="49f4a-141">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-141">public int viewUserLicense(\[int value\])</span></span>                | <span data-ttu-id="49f4a-142">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-142">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="49f4a-143">::public static void runCalled(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-143">::public static void runCalled(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="49f4a-144">public void AOTrun(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-144">public void AOTrun(\[xArgs args\])</span></span>                       | <span data-ttu-id="49f4a-145">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="49f4a-145">Compiles this node and its sub-tree in the Finance and Operations Application Object Tree (AOT).</span></span>             |
| <span data-ttu-id="49f4a-146">::public static void runClient(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-146">::public static void runClient(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="49f4a-147">public void run(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-147">public void run(\[xArgs args\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="49f4a-148">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-148">public void new(str name)</span></span>                                | <span data-ttu-id="49f4a-149">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-149">Initializes a new instance of the TreeNode class.</span></span>                                                           |
| <span data-ttu-id="49f4a-150">::public static void runServer(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-150">::public static void runServer(str name, \[xArgs args\])</span></span> |                                                                                                             |

### <a name="method-big"></a><span data-ttu-id="49f4a-151">メソッド big</span><span class="sxs-lookup"><span data-stu-id="49f4a-151">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-152">Parameters</span></span>

<span data-ttu-id="49f4a-153">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-153">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-154">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="49f4a-155">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-155">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-156">Parameters</span></span>

<span data-ttu-id="49f4a-157">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-157">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-158">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="49f4a-159">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-159">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-160">Parameters</span></span>

<span data-ttu-id="49f4a-161">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-161">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-162">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="49f4a-163">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-163">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-164">Parameters</span></span>

<span data-ttu-id="49f4a-165">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-165">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-166">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="49f4a-167">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="49f4a-167">Method enumParameter</span></span>

<span data-ttu-id="49f4a-168">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-168">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-169">Parameters</span></span>

<span data-ttu-id="49f4a-170">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-170">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-171">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-171">Return Value</span></span>

<span data-ttu-id="49f4a-172">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-172">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="49f4a-173">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="49f4a-173">Method enumTypeParameter</span></span>

<span data-ttu-id="49f4a-174">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-174">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-175">Parameters</span></span>

<span data-ttu-id="49f4a-176">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-176">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-177">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-177">Return Value</span></span>

<span data-ttu-id="49f4a-178">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-178">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="49f4a-179">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="49f4a-179">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-180">Parameters</span></span>

<span data-ttu-id="49f4a-181">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-182">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="49f4a-183">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="49f4a-183">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-184">Parameters</span></span>

<span data-ttu-id="49f4a-185">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-185">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-186">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-186">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="49f4a-187">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="49f4a-187">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-188">Parameters</span></span>

<span data-ttu-id="49f4a-189">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-189">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-190">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-190">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="49f4a-191">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="49f4a-191">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-192">Parameters</span></span>

<span data-ttu-id="49f4a-193">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-193">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-194">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="49f4a-195">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="49f4a-195">Method maintainUserLicense</span></span>

<span data-ttu-id="49f4a-196">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-196">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-197">Parameters</span></span>

<span data-ttu-id="49f4a-198">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-198">value</span></span>  
<span data-ttu-id="49f4a-199">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-199">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="49f4a-200">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-200">Return Value</span></span>

<span data-ttu-id="49f4a-201">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-201">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="49f4a-202">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="49f4a-202">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-203">Parameters</span></span>

<span data-ttu-id="49f4a-204">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-204">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-205">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="49f4a-206">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="49f4a-206">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-207">Parameters</span></span>

<span data-ttu-id="49f4a-208">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-208">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-209">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-209">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="49f4a-210">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="49f4a-210">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-211">Parameters</span></span>

<span data-ttu-id="49f4a-212">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-212">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-213">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-213">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="49f4a-214">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="49f4a-214">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-215">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-215">Parameters</span></span>

<span data-ttu-id="49f4a-216">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-216">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-217">Return Value</span></span>

### <a name="method-object"></a><span data-ttu-id="49f4a-218">メソッド object</span><span class="sxs-lookup"><span data-stu-id="49f4a-218">Method object</span></span>

<span data-ttu-id="49f4a-219">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-219">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-220">Parameters</span></span>

<span data-ttu-id="49f4a-221">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-221">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-222">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-222">Return Value</span></span>

<span data-ttu-id="49f4a-223">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-223">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-224">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-224">Remarks</span></span>

<span data-ttu-id="49f4a-225">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-225">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="49f4a-226">フォーム</span><span class="sxs-lookup"><span data-stu-id="49f4a-226">Form</span></span>
-   <span data-ttu-id="49f4a-227">レポート </span><span class="sxs-lookup"><span data-stu-id="49f4a-227">Report</span></span>
-   <span data-ttu-id="49f4a-228">ジョブ</span><span class="sxs-lookup"><span data-stu-id="49f4a-228">Job</span></span>
-   <span data-ttu-id="49f4a-229">クラス</span><span class="sxs-lookup"><span data-stu-id="49f4a-229">Class</span></span>
-   <span data-ttu-id="49f4a-230">クエリ</span><span class="sxs-lookup"><span data-stu-id="49f4a-230">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="49f4a-231">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="49f4a-231">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-232">Parameters</span></span>

<span data-ttu-id="49f4a-233">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-233">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-234">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-235">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-235">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-236">Parameters</span></span>

<span data-ttu-id="49f4a-237">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-237">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-238">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-238">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="49f4a-239">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="49f4a-239">Method parameters</span></span>

<span data-ttu-id="49f4a-240">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-240">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-241">Parameters</span></span>

<span data-ttu-id="49f4a-242">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-242">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-243">Return Value</span></span>

<span data-ttu-id="49f4a-244">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-244">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-245">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-245">Remarks</span></span>

<span data-ttu-id="49f4a-246">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-246">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="49f4a-247">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-247">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="49f4a-248">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-248">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-249">Parameters</span></span>

<span data-ttu-id="49f4a-250">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-250">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-251">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-251">Return Value</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="49f4a-252">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="49f4a-252">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-253">Parameters</span></span>

<span data-ttu-id="49f4a-254">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-254">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-255">Return Value</span></span>

### <a name="method-runon"></a><span data-ttu-id="49f4a-256">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="49f4a-256">Method runOn</span></span>

    public int runOn([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-257">Parameters</span></span>

<span data-ttu-id="49f4a-258">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-258">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-259">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-259">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="49f4a-260">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-260">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-261">Parameters</span></span>

<span data-ttu-id="49f4a-262">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-262">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-263">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="49f4a-264">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="49f4a-264">Method viewUserLicense</span></span>

<span data-ttu-id="49f4a-265">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-265">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-266">Parameters</span></span>

<span data-ttu-id="49f4a-267">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-267">value</span></span>  
<span data-ttu-id="49f4a-268">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-268">The user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="49f4a-269">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-269">Return Value</span></span>

<span data-ttu-id="49f4a-270">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-270">The user license.</span></span>

### <a name="method-runcalled"></a><span data-ttu-id="49f4a-271">メソッド runCalled</span><span class="sxs-lookup"><span data-stu-id="49f4a-271">Method runCalled</span></span>

    public static void runCalled(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="49f4a-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-272">Parameters</span></span>

<span data-ttu-id="49f4a-273">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-273">name</span></span>  

<!-- -->

<span data-ttu-id="49f4a-274">args</span><span class="sxs-lookup"><span data-stu-id="49f4a-274">args</span></span>  

### <a name="method-aotrun"></a><span data-ttu-id="49f4a-275">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="49f4a-275">Method AOTrun</span></span>

<span data-ttu-id="49f4a-276">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="49f4a-276">Compiles this node and its sub-tree in the Finance and Operations Application Object Tree (AOT).</span></span>

    public void AOTrun([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="49f4a-277">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-277">Parameters</span></span>

<span data-ttu-id="49f4a-278">args</span><span class="sxs-lookup"><span data-stu-id="49f4a-278">args</span></span>  

### <a name="method-runclient"></a><span data-ttu-id="49f4a-279">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="49f4a-279">Method runClient</span></span>

    public static void runClient(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="49f4a-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-280">Parameters</span></span>

<span data-ttu-id="49f4a-281">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-281">name</span></span>  

<!-- -->

<span data-ttu-id="49f4a-282">args</span><span class="sxs-lookup"><span data-stu-id="49f4a-282">args</span></span>  

### <a name="method-run"></a><span data-ttu-id="49f4a-283">メソッド run</span><span class="sxs-lookup"><span data-stu-id="49f4a-283">Method run</span></span>

    public void run([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="49f4a-284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-284">Parameters</span></span>

<span data-ttu-id="49f4a-285">args</span><span class="sxs-lookup"><span data-stu-id="49f4a-285">args</span></span>  

### <a name="method-new"></a><span data-ttu-id="49f4a-286">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-286">Method new</span></span>

<span data-ttu-id="49f4a-287">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-287">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-288">Parameters</span></span>

<span data-ttu-id="49f4a-289">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-289">name</span></span>  

### <a name="method-runserver"></a><span data-ttu-id="49f4a-290">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="49f4a-290">Method runServer</span></span>

    public static void runServer(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="49f4a-291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-291">Parameters</span></span>

<span data-ttu-id="49f4a-292">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-292">name</span></span>  

<!-- -->

<span data-ttu-id="49f4a-293">args</span><span class="sxs-lookup"><span data-stu-id="49f4a-293">args</span></span>  

## <a name="class-webcontentitem"></a><span data-ttu-id="49f4a-294">クラス WebContentItem</span><span class="sxs-lookup"><span data-stu-id="49f4a-294">Class WebContentItem</span></span>
    class WebContentItem extends SecureNode

<span data-ttu-id="49f4a-295">WebContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-295">The WebContentItem class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-296">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-296">Remarks</span></span>

<span data-ttu-id="49f4a-297">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-297">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-298">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-298">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-299">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-299">Methods</span></span>

| <span data-ttu-id="49f4a-300">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-300">Method</span></span>                                            | <span data-ttu-id="49f4a-301">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-301">Description</span></span>                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-302">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-302">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="49f4a-303">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-303">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="49f4a-304">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-304">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="49f4a-305">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-305">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-306">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-306">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="49f4a-307">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-307">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-308">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-308">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="49f4a-309">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-309">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="49f4a-310">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-310">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="49f4a-311">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-311">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="49f4a-312">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-312">public str creationTime(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="49f4a-313">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-313">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="49f4a-314">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-314">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                               |
| <span data-ttu-id="49f4a-315">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-315">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="49f4a-316">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-316">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                   |
| <span data-ttu-id="49f4a-317">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-317">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="49f4a-318">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-318">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="49f4a-319">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-319">public str label(\[str value\])</span></span>                   | <span data-ttu-id="49f4a-320">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-320">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="49f4a-321">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-321">public str name(\[str value\])</span></span>                    | <span data-ttu-id="49f4a-322">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-322">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-323">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-323">public str object(\[str value\])</span></span>                  | <span data-ttu-id="49f4a-324">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-324">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-325">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-325">public int objectType(\[int value\])</span></span>              |                                                                                                                                           |
| <span data-ttu-id="49f4a-326">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-326">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="49f4a-327">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-327">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="49f4a-328">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-328">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="49f4a-329">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-329">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                           |

### <a name="method-changedby"></a><span data-ttu-id="49f4a-330">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-330">Method changedBy</span></span>

<span data-ttu-id="49f4a-331">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-331">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-332">Parameters</span></span>

<span data-ttu-id="49f4a-333">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-333">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-334">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-334">Return Value</span></span>

<span data-ttu-id="49f4a-335">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-335">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-336">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-336">Method changedDate</span></span>

<span data-ttu-id="49f4a-337">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-337">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-338">Parameters</span></span>

<span data-ttu-id="49f4a-339">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-339">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-340">Return Value</span></span>

<span data-ttu-id="49f4a-341">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-341">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-342">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-342">Method changedTime</span></span>

<span data-ttu-id="49f4a-343">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-343">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-344">Parameters</span></span>

<span data-ttu-id="49f4a-345">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-345">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-346">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-346">Return Value</span></span>

<span data-ttu-id="49f4a-347">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-347">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-348">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-348">Method createdBy</span></span>

<span data-ttu-id="49f4a-349">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-349">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-350">Parameters</span></span>

<span data-ttu-id="49f4a-351">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-351">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-352">Return Value</span></span>

<span data-ttu-id="49f4a-353">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-353">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-354">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-354">Method creationDate</span></span>

<span data-ttu-id="49f4a-355">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-355">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-356">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-356">Parameters</span></span>

<span data-ttu-id="49f4a-357">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-357">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-358">Return Value</span></span>

<span data-ttu-id="49f4a-359">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-359">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-360">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-360">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-361">Parameters</span></span>

<span data-ttu-id="49f4a-362">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-362">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-363">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="49f4a-364">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="49f4a-364">Method enumParameter</span></span>

<span data-ttu-id="49f4a-365">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-365">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-366">Parameters</span></span>

<span data-ttu-id="49f4a-367">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-368">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-368">Return Value</span></span>

<span data-ttu-id="49f4a-369">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-369">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="49f4a-370">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="49f4a-370">Method enumTypeParameter</span></span>

<span data-ttu-id="49f4a-371">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-371">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-372">Parameters</span></span>

<span data-ttu-id="49f4a-373">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-373">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-374">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-374">Return Value</span></span>

<span data-ttu-id="49f4a-375">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-375">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="49f4a-376">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="49f4a-376">Method helpText</span></span>

<span data-ttu-id="49f4a-377">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-377">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-378">Parameters</span></span>

<span data-ttu-id="49f4a-379">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-379">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-380">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-380">Return Value</span></span>

<span data-ttu-id="49f4a-381">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="49f4a-381">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-382">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-382">Remarks</span></span>

<span data-ttu-id="49f4a-383">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-383">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="49f4a-384">ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-384">dialog box.</span></span> <span data-ttu-id="49f4a-385">ヘルプ テキストは、250文字以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-385">The The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="49f4a-386">メソッド label</span><span class="sxs-lookup"><span data-stu-id="49f4a-386">Method label</span></span>

<span data-ttu-id="49f4a-387">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-387">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-388">Parameters</span></span>

<span data-ttu-id="49f4a-389">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-389">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-390">Return Value</span></span>

<span data-ttu-id="49f4a-391">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-391">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-392">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-392">Remarks</span></span>

<span data-ttu-id="49f4a-393">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-393">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="49f4a-394">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-394">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-395">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-395">Method name</span></span>

<span data-ttu-id="49f4a-396">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-396">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-397">Parameters</span></span>

<span data-ttu-id="49f4a-398">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-398">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-399">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-399">Return Value</span></span>

<span data-ttu-id="49f4a-400">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-400">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-401">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-401">Remarks</span></span>

<span data-ttu-id="49f4a-402">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-402">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-403">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-403">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-404">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-404">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-405">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-405">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-406">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-406">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-407">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-407">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-object"></a><span data-ttu-id="49f4a-408">メソッド object</span><span class="sxs-lookup"><span data-stu-id="49f4a-408">Method object</span></span>

<span data-ttu-id="49f4a-409">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-409">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-410">Parameters</span></span>

<span data-ttu-id="49f4a-411">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-411">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-412">Return Value</span></span>

<span data-ttu-id="49f4a-413">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-413">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-414">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-414">Remarks</span></span>

<span data-ttu-id="49f4a-415">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-415">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="49f4a-416">フォーム</span><span class="sxs-lookup"><span data-stu-id="49f4a-416">Form</span></span>
-   <span data-ttu-id="49f4a-417">レポート </span><span class="sxs-lookup"><span data-stu-id="49f4a-417">Report</span></span>
-   <span data-ttu-id="49f4a-418">ジョブ</span><span class="sxs-lookup"><span data-stu-id="49f4a-418">Job</span></span>
-   <span data-ttu-id="49f4a-419">クラス</span><span class="sxs-lookup"><span data-stu-id="49f4a-419">Class</span></span>
-   <span data-ttu-id="49f4a-420">クエリ</span><span class="sxs-lookup"><span data-stu-id="49f4a-420">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="49f4a-421">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="49f4a-421">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-422">Parameters</span></span>

<span data-ttu-id="49f4a-423">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-423">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-424">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-425">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-425">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-426">Parameters</span></span>

<span data-ttu-id="49f4a-427">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-427">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-428">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-428">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="49f4a-429">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="49f4a-429">Method parameters</span></span>

<span data-ttu-id="49f4a-430">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-430">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-431">Parameters</span></span>

<span data-ttu-id="49f4a-432">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-432">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-433">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-433">Return Value</span></span>

<span data-ttu-id="49f4a-434">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-434">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-435">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-435">Remarks</span></span>

<span data-ttu-id="49f4a-436">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-436">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="49f4a-437">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-437">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="49f4a-438">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="49f4a-438">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-439">Parameters</span></span>

<span data-ttu-id="49f4a-440">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-440">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-441">Return Value</span></span>

## <a name="class-webcontrolnode"></a><span data-ttu-id="49f4a-442">クラス webControlNode</span><span class="sxs-lookup"><span data-stu-id="49f4a-442">Class webControlNode</span></span>
    class webControlNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="49f4a-443">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-443">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-444">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-444">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-445">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-445">Methods</span></span>

| <span data-ttu-id="49f4a-446">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-446">Method</span></span>                                                        | <span data-ttu-id="49f4a-447">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-447">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-448">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="49f4a-448">public str AOTgetSource()</span></span>                                     | <span data-ttu-id="49f4a-449">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-449">Returns the source code of this node.</span></span>                                                                                                         |
| <span data-ttu-id="49f4a-450">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-450">public str changedBy(\[str value\])</span></span>                           | <span data-ttu-id="49f4a-451">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-451">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="49f4a-452">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-452">public Date changedDate(\[Date value\])</span></span>                       | <span data-ttu-id="49f4a-453">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-453">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-454">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-454">public str changedTime(\[str value\])</span></span>                         | <span data-ttu-id="49f4a-455">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-455">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-456">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-456">public str createdBy(\[str value\])</span></span>                           | <span data-ttu-id="49f4a-457">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-457">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="49f4a-458">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-458">public Date creationDate(\[Date value\])</span></span>                      | <span data-ttu-id="49f4a-459">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-459">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="49f4a-460">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-460">public str creationTime(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="49f4a-461">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-461">public str filename(\[str value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="49f4a-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span></span> | <span data-ttu-id="49f4a-463">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-463">Get a list of web controls that are related to this web control.</span></span>                                                                              |
| <span data-ttu-id="49f4a-464">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-464">public str helpText(\[str value\])</span></span>                            | <span data-ttu-id="49f4a-465">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-465">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="49f4a-466">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-466">public str name(\[str value\])</span></span>                                | <span data-ttu-id="49f4a-467">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-467">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-468">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-468">public Guid origin(\[Guid value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="49f4a-469">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-469">public str relativePath(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="49f4a-470">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-470">public str version(\[str value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="49f4a-471">::public static webControlNode createFromFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="49f4a-471">::public static webControlNode createFromFile(str fileName)</span></span>   |                                                                                                                                               |
| <span data-ttu-id="49f4a-472">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-472">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>    | <span data-ttu-id="49f4a-473">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-473">Sets the source code of this node.</span></span>                                                                                                            |

### <a name="method-aotgetsource"></a><span data-ttu-id="49f4a-474">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-474">Method AOTgetSource</span></span>

<span data-ttu-id="49f4a-475">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-475">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="49f4a-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-476">Return Value</span></span>

<span data-ttu-id="49f4a-477">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="49f4a-477">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-478">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-478">Remarks</span></span>

<span data-ttu-id="49f4a-479">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-479">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="49f4a-480">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-480">Method changedBy</span></span>

<span data-ttu-id="49f4a-481">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-481">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-482">Parameters</span></span>

<span data-ttu-id="49f4a-483">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-484">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-484">Return Value</span></span>

<span data-ttu-id="49f4a-485">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-485">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-486">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-486">Method changedDate</span></span>

<span data-ttu-id="49f4a-487">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-487">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-488">Parameters</span></span>

<span data-ttu-id="49f4a-489">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-489">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-490">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-490">Return Value</span></span>

<span data-ttu-id="49f4a-491">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-491">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-492">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-492">Method changedTime</span></span>

<span data-ttu-id="49f4a-493">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-493">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-494">Parameters</span></span>

<span data-ttu-id="49f4a-495">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-495">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-496">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-496">Return Value</span></span>

<span data-ttu-id="49f4a-497">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-497">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-498">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-498">Method createdBy</span></span>

<span data-ttu-id="49f4a-499">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-499">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-500">Parameters</span></span>

<span data-ttu-id="49f4a-501">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-501">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-502">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-502">Return Value</span></span>

<span data-ttu-id="49f4a-503">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-503">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-504">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-504">Method creationDate</span></span>

<span data-ttu-id="49f4a-505">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-505">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-506">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-506">Parameters</span></span>

<span data-ttu-id="49f4a-507">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-507">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-508">Return Value</span></span>

<span data-ttu-id="49f4a-509">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-509">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-510">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-510">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-511">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-511">Parameters</span></span>

<span data-ttu-id="49f4a-512">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-512">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-513">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="49f4a-514">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="49f4a-514">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-515">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-515">Parameters</span></span>

<span data-ttu-id="49f4a-516">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-516">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-517">Return Value</span></span>

### <a name="method-getrelatedwebcontrols"></a><span data-ttu-id="49f4a-518">メソッド getRelatedWebControls</span><span class="sxs-lookup"><span data-stu-id="49f4a-518">Method getRelatedWebControls</span></span>

<span data-ttu-id="49f4a-519">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-519">Get a list of web controls that are related to this web control.</span></span>

    public List getRelatedWebControls([boolean firstLevelOnly])

#### <a name="parameters"></a><span data-ttu-id="49f4a-520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-520">Parameters</span></span>

<span data-ttu-id="49f4a-521">firstLevelOnly</span><span class="sxs-lookup"><span data-stu-id="49f4a-521">firstLevelOnly</span></span>  
<span data-ttu-id="49f4a-522">Web コントロールの最初のレベルのみがオンになっているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-522">A value that indicates whether only the first level of web controls is checked.</span></span>

#### <a name="return-value"></a><span data-ttu-id="49f4a-523">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-523">Return Value</span></span>

<span data-ttu-id="49f4a-524">関連する Web コントロールの一覧。</span><span class="sxs-lookup"><span data-stu-id="49f4a-524">A list of related web controls.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="49f4a-525">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="49f4a-525">Method helpText</span></span>

<span data-ttu-id="49f4a-526">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-526">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-527">Parameters</span></span>

<span data-ttu-id="49f4a-528">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-528">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-529">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-529">Return Value</span></span>

<span data-ttu-id="49f4a-530">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="49f4a-530">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-531">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-531">Remarks</span></span>

<span data-ttu-id="49f4a-532">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-532">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="49f4a-533">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-533">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-534">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-534">Method name</span></span>

<span data-ttu-id="49f4a-535">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-535">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-536">Parameters</span></span>

<span data-ttu-id="49f4a-537">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-538">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-538">Return Value</span></span>

<span data-ttu-id="49f4a-539">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-539">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-540">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-540">Remarks</span></span>

<span data-ttu-id="49f4a-541">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-541">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-542">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-542">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-543">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-543">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-544">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-544">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-545">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-545">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-546">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-546">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-547">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-547">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-548">Parameters</span></span>

<span data-ttu-id="49f4a-549">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-549">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-550">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-550">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="49f4a-551">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="49f4a-551">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-552">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-552">Parameters</span></span>

<span data-ttu-id="49f4a-553">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-553">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-554">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-554">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="49f4a-555">メソッド version</span><span class="sxs-lookup"><span data-stu-id="49f4a-555">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-556">Parameters</span></span>

<span data-ttu-id="49f4a-557">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-557">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-558">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-558">Return Value</span></span>

### <a name="method-createfromfile"></a><span data-ttu-id="49f4a-559">メソッド createFromFile</span><span class="sxs-lookup"><span data-stu-id="49f4a-559">Method createFromFile</span></span>

    public static webControlNode createFromFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="49f4a-560">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-560">Parameters</span></span>

<span data-ttu-id="49f4a-561">fileName</span><span class="sxs-lookup"><span data-stu-id="49f4a-561">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-562">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-562">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="49f4a-563">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-563">Method AOTsetSource</span></span>

<span data-ttu-id="49f4a-564">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-564">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="49f4a-565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-565">Parameters</span></span>

<span data-ttu-id="49f4a-566">ソース</span><span class="sxs-lookup"><span data-stu-id="49f4a-566">source</span></span>  
<span data-ttu-id="49f4a-567">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="49f4a-567">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="49f4a-568">isStatic</span><span class="sxs-lookup"><span data-stu-id="49f4a-568">isStatic</span></span>  
<span data-ttu-id="49f4a-569">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="49f4a-569">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-570">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-570">Remarks</span></span>

<span data-ttu-id="49f4a-571">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-571">This method is overridden by nodes that have source code.</span></span>

## <a name="class-webdisplaycontentitem"></a><span data-ttu-id="49f4a-572">クラス WebDisplayContentItem</span><span class="sxs-lookup"><span data-stu-id="49f4a-572">Class WebDisplayContentItem</span></span>
    class WebDisplayContentItem extends WebContentItem

<span data-ttu-id="49f4a-573">WebDisplayContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-573">The WebDisplayContentItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-574">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-574">Remarks</span></span>

<span data-ttu-id="49f4a-575">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-575">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="49f4a-576">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-576">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-577">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-577">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-578">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-578">Methods</span></span>

| <span data-ttu-id="49f4a-579">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-579">Method</span></span>                    | <span data-ttu-id="49f4a-580">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-580">Description</span></span>                          |
|---------------------------|--------------------------------------|
| <span data-ttu-id="49f4a-581">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-581">public void new(str name)</span></span> | <span data-ttu-id="49f4a-582">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-582">Creates a new WebDisplayContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="49f4a-583">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-583">Method new</span></span>

<span data-ttu-id="49f4a-584">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-584">Creates a new WebDisplayContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-585">Parameters</span></span>

<span data-ttu-id="49f4a-586">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-586">name</span></span>  

## <a name="class-webletitem"></a><span data-ttu-id="49f4a-587">クラス WebletItem</span><span class="sxs-lookup"><span data-stu-id="49f4a-587">Class WebletItem</span></span>
    class WebletItem extends SecureNode

<span data-ttu-id="49f4a-588">WebletItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-588">The WebletItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-589">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-589">Remarks</span></span>

<span data-ttu-id="49f4a-590">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-590">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="49f4a-591">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-591">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-592">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-592">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-593">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-593">Methods</span></span>

| <span data-ttu-id="49f4a-594">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-594">Method</span></span>                                            | <span data-ttu-id="49f4a-595">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-595">Description</span></span>                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-596">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-596">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="49f4a-597">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-597">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="49f4a-598">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-598">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="49f4a-599">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-599">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-600">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-600">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="49f4a-601">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-601">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-602">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-602">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="49f4a-603">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-603">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="49f4a-604">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-604">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="49f4a-605">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-605">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="49f4a-606">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-606">public str creationTime(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="49f4a-607">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-607">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="49f4a-608">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-608">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                                   |
| <span data-ttu-id="49f4a-609">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-609">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="49f4a-610">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-610">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="49f4a-611">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-611">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="49f4a-612">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-612">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="49f4a-613">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-613">public str label(\[str value\])</span></span>                   | <span data-ttu-id="49f4a-614">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-614">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="49f4a-615">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-615">public str name(\[str value\])</span></span>                    | <span data-ttu-id="49f4a-616">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-616">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-617">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-617">public str object(\[str value\])</span></span>                  | <span data-ttu-id="49f4a-618">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-618">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                     |
| <span data-ttu-id="49f4a-619">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-619">public int objectType(\[int value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="49f4a-620">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-620">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="49f4a-621">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-621">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="49f4a-622">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-622">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                        |
| <span data-ttu-id="49f4a-623">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-623">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="49f4a-624">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-624">public void new(str name)</span></span>                         | <span data-ttu-id="49f4a-625">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-625">Microsoft internal use only.</span></span>                                                                                                                  |

### <a name="method-changedby"></a><span data-ttu-id="49f4a-626">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-626">Method changedBy</span></span>

<span data-ttu-id="49f4a-627">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-627">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-628">Parameters</span></span>

<span data-ttu-id="49f4a-629">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-630">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-630">Return Value</span></span>

<span data-ttu-id="49f4a-631">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-631">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-632">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-632">Method changedDate</span></span>

<span data-ttu-id="49f4a-633">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-633">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-634">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-634">Parameters</span></span>

<span data-ttu-id="49f4a-635">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-635">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-636">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-636">Return Value</span></span>

<span data-ttu-id="49f4a-637">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-637">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-638">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-638">Method changedTime</span></span>

<span data-ttu-id="49f4a-639">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-639">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-640">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-640">Parameters</span></span>

<span data-ttu-id="49f4a-641">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-641">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-642">Return Value</span></span>

<span data-ttu-id="49f4a-643">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-643">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-644">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-644">Method createdBy</span></span>

<span data-ttu-id="49f4a-645">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-645">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-646">Parameters</span></span>

<span data-ttu-id="49f4a-647">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-648">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-648">Return Value</span></span>

<span data-ttu-id="49f4a-649">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-649">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-650">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-650">Method creationDate</span></span>

<span data-ttu-id="49f4a-651">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-651">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-652">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-652">Parameters</span></span>

<span data-ttu-id="49f4a-653">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-653">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-654">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-654">Return Value</span></span>

<span data-ttu-id="49f4a-655">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-655">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-656">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-656">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-657">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-657">Parameters</span></span>

<span data-ttu-id="49f4a-658">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-658">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-659">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="49f4a-660">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="49f4a-660">Method enumParameter</span></span>

<span data-ttu-id="49f4a-661">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-661">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-662">Parameters</span></span>

<span data-ttu-id="49f4a-663">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-664">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-664">Return Value</span></span>

<span data-ttu-id="49f4a-665">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-665">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="49f4a-666">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="49f4a-666">Method enumTypeParameter</span></span>

<span data-ttu-id="49f4a-667">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-667">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-668">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-668">Parameters</span></span>

<span data-ttu-id="49f4a-669">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-669">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-670">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-670">Return Value</span></span>

<span data-ttu-id="49f4a-671">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-671">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="49f4a-672">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="49f4a-672">Method helpText</span></span>

<span data-ttu-id="49f4a-673">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-673">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-674">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-674">Parameters</span></span>

<span data-ttu-id="49f4a-675">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-675">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-676">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-676">Return Value</span></span>

<span data-ttu-id="49f4a-677">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="49f4a-677">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-678">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-678">Remarks</span></span>

<span data-ttu-id="49f4a-679">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-679">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="49f4a-680">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-680">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="49f4a-681">メソッド label</span><span class="sxs-lookup"><span data-stu-id="49f4a-681">Method label</span></span>

<span data-ttu-id="49f4a-682">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-682">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-683">Parameters</span></span>

<span data-ttu-id="49f4a-684">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-684">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-685">Return Value</span></span>

<span data-ttu-id="49f4a-686">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-686">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-687">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-687">Remarks</span></span>

<span data-ttu-id="49f4a-688">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-688">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="49f4a-689">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-689">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-690">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-690">Method name</span></span>

<span data-ttu-id="49f4a-691">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-691">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-692">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-692">Parameters</span></span>

<span data-ttu-id="49f4a-693">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-693">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-694">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-694">Return Value</span></span>

<span data-ttu-id="49f4a-695">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-695">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-696">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-696">Remarks</span></span>

<span data-ttu-id="49f4a-697">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-697">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-698">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-698">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-699">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-699">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-700">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-700">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-701">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-701">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-702">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-702">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

### <a name="method-object"></a><span data-ttu-id="49f4a-703">メソッド object</span><span class="sxs-lookup"><span data-stu-id="49f4a-703">Method object</span></span>

<span data-ttu-id="49f4a-704">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-704">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-705">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-705">Parameters</span></span>

<span data-ttu-id="49f4a-706">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-706">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-707">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-707">Return Value</span></span>

<span data-ttu-id="49f4a-708">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-708">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-709">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-709">Remarks</span></span>

<span data-ttu-id="49f4a-710">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-710">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="49f4a-711">フォーム。</span><span class="sxs-lookup"><span data-stu-id="49f4a-711">Form.</span></span>
-   <span data-ttu-id="49f4a-712">レポート。</span><span class="sxs-lookup"><span data-stu-id="49f4a-712">Report.</span></span>
-   <span data-ttu-id="49f4a-713">ジョブ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-713">Job.</span></span>
-   <span data-ttu-id="49f4a-714">クラス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-714">Class.</span></span>
-   <span data-ttu-id="49f4a-715">クエリ。</span><span class="sxs-lookup"><span data-stu-id="49f4a-715">Query.</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="49f4a-716">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="49f4a-716">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-717">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-717">Parameters</span></span>

<span data-ttu-id="49f4a-718">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-718">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-719">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-719">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-720">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-720">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-721">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-721">Parameters</span></span>

<span data-ttu-id="49f4a-722">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-722">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-723">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-723">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="49f4a-724">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="49f4a-724">Method parameters</span></span>

<span data-ttu-id="49f4a-725">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-725">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-726">Parameters</span></span>

<span data-ttu-id="49f4a-727">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-728">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-728">Return Value</span></span>

<span data-ttu-id="49f4a-729">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-729">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-730">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-730">Remarks</span></span>

<span data-ttu-id="49f4a-731">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-731">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="49f4a-732">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-732">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="49f4a-733">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="49f4a-733">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-734">Parameters</span></span>

<span data-ttu-id="49f4a-735">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-736">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-736">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="49f4a-737">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-737">Method new</span></span>

<span data-ttu-id="49f4a-738">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-738">Microsoft internal use only.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-739">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-739">Parameters</span></span>

<span data-ttu-id="49f4a-740">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-740">name</span></span>  

## <a name="class-weblistdefnode"></a><span data-ttu-id="49f4a-741">クラス webListDefNode</span><span class="sxs-lookup"><span data-stu-id="49f4a-741">Class webListDefNode</span></span>
    class webListDefNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="49f4a-742">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-742">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-743">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-743">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-744">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-744">Methods</span></span>

| <span data-ttu-id="49f4a-745">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-745">Method</span></span>                                                     | <span data-ttu-id="49f4a-746">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-746">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-747">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="49f4a-747">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="49f4a-748">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-748">Returns the source code of this node.</span></span>                                                                                                     |
| <span data-ttu-id="49f4a-749">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-749">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="49f4a-750">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-750">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="49f4a-751">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-751">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="49f4a-752">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-752">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-753">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-753">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="49f4a-754">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-754">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-755">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-755">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="49f4a-756">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-756">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="49f4a-757">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-757">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="49f4a-758">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-758">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="49f4a-759">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-759">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="49f4a-760">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-760">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="49f4a-761">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-761">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="49f4a-762">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-762">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="49f4a-763">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-763">public str name(\[str value\])</span></span>                             | <span data-ttu-id="49f4a-764">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-764">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-765">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-765">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="49f4a-766">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-766">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="49f4a-767">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-767">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="49f4a-768">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-768">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="49f4a-769">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-769">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="49f4a-770">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-770">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="49f4a-771">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-771">Sets the source code of this node.</span></span>                                                                                                        |
| <span data-ttu-id="49f4a-772">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-772">public void new(str name)</span></span>                                  | <span data-ttu-id="49f4a-773">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-773">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |

### <a name="method-aotgetsource"></a><span data-ttu-id="49f4a-774">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-774">Method AOTgetSource</span></span>

<span data-ttu-id="49f4a-775">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-775">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="49f4a-776">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-776">Return Value</span></span>

<span data-ttu-id="49f4a-777">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="49f4a-777">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-778">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-778">Remarks</span></span>

<span data-ttu-id="49f4a-779">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-779">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="49f4a-780">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-780">Method changedBy</span></span>

<span data-ttu-id="49f4a-781">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-781">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-782">Parameters</span></span>

<span data-ttu-id="49f4a-783">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-783">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-784">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-784">Return Value</span></span>

<span data-ttu-id="49f4a-785">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-785">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-786">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-786">Method changedDate</span></span>

<span data-ttu-id="49f4a-787">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-787">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-788">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-788">Parameters</span></span>

<span data-ttu-id="49f4a-789">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-789">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-790">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-790">Return Value</span></span>

<span data-ttu-id="49f4a-791">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-791">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-792">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-792">Method changedTime</span></span>

<span data-ttu-id="49f4a-793">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-793">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-794">Parameters</span></span>

<span data-ttu-id="49f4a-795">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-796">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-796">Return Value</span></span>

<span data-ttu-id="49f4a-797">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-797">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-798">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-798">Method createdBy</span></span>

<span data-ttu-id="49f4a-799">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-799">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-800">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-800">Parameters</span></span>

<span data-ttu-id="49f4a-801">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-801">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-802">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-802">Return Value</span></span>

<span data-ttu-id="49f4a-803">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-803">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-804">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-804">Method creationDate</span></span>

<span data-ttu-id="49f4a-805">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-805">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-806">Parameters</span></span>

<span data-ttu-id="49f4a-807">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-808">Return Value</span></span>

<span data-ttu-id="49f4a-809">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-809">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-810">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-810">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-811">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-811">Parameters</span></span>

<span data-ttu-id="49f4a-812">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-812">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-813">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-813">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="49f4a-814">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="49f4a-814">Method helpText</span></span>

<span data-ttu-id="49f4a-815">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-815">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-816">Parameters</span></span>

<span data-ttu-id="49f4a-817">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-817">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-818">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-818">Return Value</span></span>

<span data-ttu-id="49f4a-819">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="49f4a-819">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-820">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-820">Remarks</span></span>

<span data-ttu-id="49f4a-821">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-821">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="49f4a-822">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-822">The help text must not exceed 250 characters.</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="49f4a-823">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="49f4a-823">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-824">Parameters</span></span>

<span data-ttu-id="49f4a-825">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-825">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-826">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-827">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-827">Method name</span></span>

<span data-ttu-id="49f4a-828">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-828">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-829">Parameters</span></span>

<span data-ttu-id="49f4a-830">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-831">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-831">Return Value</span></span>

<span data-ttu-id="49f4a-832">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-832">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-833">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-833">Remarks</span></span>

<span data-ttu-id="49f4a-834">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-834">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-835">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-835">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-836">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-836">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-837">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-837">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-838">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-838">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-839">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-839">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-840">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-840">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-841">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-841">Parameters</span></span>

<span data-ttu-id="49f4a-842">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-842">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-843">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-843">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="49f4a-844">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="49f4a-844">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-845">Parameters</span></span>

<span data-ttu-id="49f4a-846">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-846">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-847">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="49f4a-848">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="49f4a-848">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-849">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-849">Parameters</span></span>

<span data-ttu-id="49f4a-850">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-850">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-851">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="49f4a-852">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="49f4a-852">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-853">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-853">Parameters</span></span>

<span data-ttu-id="49f4a-854">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-854">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-855">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="49f4a-856">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="49f4a-856">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-857">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-857">Parameters</span></span>

<span data-ttu-id="49f4a-858">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-858">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-859">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="49f4a-860">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-860">Method AOTsetSource</span></span>

<span data-ttu-id="49f4a-861">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-861">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="49f4a-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-862">Parameters</span></span>

<span data-ttu-id="49f4a-863">ソース</span><span class="sxs-lookup"><span data-stu-id="49f4a-863">source</span></span>  
<span data-ttu-id="49f4a-864">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="49f4a-864">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="49f4a-865">isStatic</span><span class="sxs-lookup"><span data-stu-id="49f4a-865">isStatic</span></span>  
<span data-ttu-id="49f4a-866">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="49f4a-866">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-867">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-867">Remarks</span></span>

<span data-ttu-id="49f4a-868">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-868">This method is overridden by nodes that have source code.</span></span>

### <a name="method-new"></a><span data-ttu-id="49f4a-869">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-869">Method new</span></span>

<span data-ttu-id="49f4a-870">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-870">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-871">Parameters</span></span>

<span data-ttu-id="49f4a-872">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-872">name</span></span>  

## <a name="class-webmanagedcontentitem"></a><span data-ttu-id="49f4a-873">クラス WebManagedContentItem</span><span class="sxs-lookup"><span data-stu-id="49f4a-873">Class WebManagedContentItem</span></span>
    class WebManagedContentItem extends WebContentItem

<span data-ttu-id="49f4a-874">このクラスを使用して、コンテンツをページに追加するために EP で使用する webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-874">This class is used to create a webManagedContentItem to use in EP for adding content to pages.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-875">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-875">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-876">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-876">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-877">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-877">Methods</span></span>

| <span data-ttu-id="49f4a-878">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-878">Method</span></span>                    | <span data-ttu-id="49f4a-879">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-879">Description</span></span>                                                 |
|---------------------------|-------------------------------------------------------------|
| <span data-ttu-id="49f4a-880">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-880">public void new(str name)</span></span> | <span data-ttu-id="49f4a-881">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-881">Create a new webManagedContentItem with the passed in name.</span></span> |

### <a name="method-new"></a><span data-ttu-id="49f4a-882">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-882">Method new</span></span>

<span data-ttu-id="49f4a-883">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-883">Create a new webManagedContentItem with the passed in name.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-884">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-884">Parameters</span></span>

<span data-ttu-id="49f4a-885">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-885">name</span></span>  
<span data-ttu-id="49f4a-886">新しい webManagedContentItem に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-886">Name for the new webManagedContentItem.</span></span>

## <a name="class-webmenu"></a><span data-ttu-id="49f4a-887">クラス WebMenu</span><span class="sxs-lookup"><span data-stu-id="49f4a-887">Class WebMenu</span></span>
    class WebMenu extends TreeNode

<span data-ttu-id="49f4a-888">WebMenu クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-888">The WebMenu class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-889">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-889">Remarks</span></span>

<span data-ttu-id="49f4a-890">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-890">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-891">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-891">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-892">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-892">Methods</span></span>

| <span data-ttu-id="49f4a-893">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-893">Method</span></span>                                                                   | <span data-ttu-id="49f4a-894">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-894">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-895">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-895">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="49f4a-896">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-896">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="49f4a-897">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-897">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="49f4a-898">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-898">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-899">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-899">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="49f4a-900">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-900">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="49f4a-902">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-902">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="49f4a-903">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-903">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="49f4a-904">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-904">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="49f4a-905">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-905">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="49f4a-906">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-906">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="49f4a-907">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-907">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="49f4a-908">public boolean highlightSelected(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-908">public boolean highlightSelected(\[boolean value\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="49f4a-909">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-909">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="49f4a-910">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-910">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="49f4a-911">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-911">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="49f4a-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                               |
| <span data-ttu-id="49f4a-913">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="49f4a-913">public str menuName()</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="49f4a-914">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-914">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="49f4a-915">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-915">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-916">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-916">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="49f4a-917">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-917">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="49f4a-918">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-918">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="49f4a-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="49f4a-920">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-920">public boolean setCompany(\[boolean value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="49f4a-921">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-921">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="49f4a-922">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-922">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="49f4a-923">public void addSeparator()</span><span class="sxs-lookup"><span data-stu-id="49f4a-923">public void addSeparator()</span></span>                                               |                                                                                                                                               |
| <span data-ttu-id="49f4a-924">public void makeMenu(Object outputClass)</span><span class="sxs-lookup"><span data-stu-id="49f4a-924">public void makeMenu(Object outputClass)</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="49f4a-925">public void addSubmenu(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-925">public void addSubmenu(str name)</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="49f4a-926">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-926">public void new(str Name)</span></span>                                                | <span data-ttu-id="49f4a-927">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-927">Initializes a new instance of the TreeNode class.</span></span>                                                                                             |
| <span data-ttu-id="49f4a-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="49f4a-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="49f4a-929">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-929">Method changedBy</span></span>

<span data-ttu-id="49f4a-930">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-930">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-931">Parameters</span></span>

<span data-ttu-id="49f4a-932">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-932">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-933">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-933">Return Value</span></span>

<span data-ttu-id="49f4a-934">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-934">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-935">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-935">Method changedDate</span></span>

<span data-ttu-id="49f4a-936">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-936">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-937">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-937">Parameters</span></span>

<span data-ttu-id="49f4a-938">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-938">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-939">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-939">Return Value</span></span>

<span data-ttu-id="49f4a-940">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-940">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-941">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-941">Method changedTime</span></span>

<span data-ttu-id="49f4a-942">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-942">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-943">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-943">Parameters</span></span>

<span data-ttu-id="49f4a-944">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-944">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-945">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-945">Return Value</span></span>

<span data-ttu-id="49f4a-946">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-946">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="49f4a-947">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="49f4a-947">Method configurationKey</span></span>

<span data-ttu-id="49f4a-948">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-948">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-949">Parameters</span></span>

<span data-ttu-id="49f4a-950">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-950">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-951">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-951">Return Value</span></span>

<span data-ttu-id="49f4a-952">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="49f4a-952">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-953">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-953">Remarks</span></span>

<span data-ttu-id="49f4a-954">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-954">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="49f4a-955">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-955">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-956">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-956">Method createdBy</span></span>

<span data-ttu-id="49f4a-957">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-957">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-958">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-958">Parameters</span></span>

<span data-ttu-id="49f4a-959">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-959">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-960">Return Value</span></span>

<span data-ttu-id="49f4a-961">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-961">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-962">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-962">Method creationDate</span></span>

<span data-ttu-id="49f4a-963">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-963">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-964">Parameters</span></span>

<span data-ttu-id="49f4a-965">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-965">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-966">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-966">Return Value</span></span>

<span data-ttu-id="49f4a-967">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-967">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-968">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-968">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-969">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-969">Parameters</span></span>

<span data-ttu-id="49f4a-970">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-970">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-971">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-971">Return Value</span></span>

### <a name="method-highlightselected"></a><span data-ttu-id="49f4a-972">メソッド highlightSelected</span><span class="sxs-lookup"><span data-stu-id="49f4a-972">Method highlightSelected</span></span>

    public boolean highlightSelected([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-973">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-973">Parameters</span></span>

<span data-ttu-id="49f4a-974">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-974">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-975">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="49f4a-976">メソッド label</span><span class="sxs-lookup"><span data-stu-id="49f4a-976">Method label</span></span>

<span data-ttu-id="49f4a-977">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-977">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-978">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-978">Parameters</span></span>

<span data-ttu-id="49f4a-979">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-979">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-980">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-980">Return Value</span></span>

<span data-ttu-id="49f4a-981">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-981">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-982">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-982">Remarks</span></span>

<span data-ttu-id="49f4a-983">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-983">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="49f4a-984">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-984">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="49f4a-985">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="49f4a-985">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-986">Parameters</span></span>

<span data-ttu-id="49f4a-987">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-987">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-988">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-988">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="49f4a-989">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="49f4a-989">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-990">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-990">Parameters</span></span>

<span data-ttu-id="49f4a-991">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-991">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-992">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-992">Return Value</span></span>

### <a name="method-menuname"></a><span data-ttu-id="49f4a-993">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="49f4a-993">Method menuName</span></span>

    public str menuName()

#### <a name="return-value"></a><span data-ttu-id="49f4a-994">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-994">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-995">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-995">Method name</span></span>

<span data-ttu-id="49f4a-996">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-996">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-997">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-997">Parameters</span></span>

<span data-ttu-id="49f4a-998">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-998">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-999">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-999">Return Value</span></span>

<span data-ttu-id="49f4a-1000">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1000">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1001">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1001">Remarks</span></span>

<span data-ttu-id="49f4a-1002">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1002">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-1003">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1003">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-1004">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1004">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-1005">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1005">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-1006">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1006">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-1007">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1007">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="49f4a-1008">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="49f4a-1008">Method neededAccessLevel</span></span>

<span data-ttu-id="49f4a-1009">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1009">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1010">Parameters</span></span>

<span data-ttu-id="49f4a-1011">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1011">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1012">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1012">Return Value</span></span>

<span data-ttu-id="49f4a-1013">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1013">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1014">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1014">Remarks</span></span>

<span data-ttu-id="49f4a-1015">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1015">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="49f4a-1016">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="49f4a-1016">AccessType::NoAccess</span></span>
-   <span data-ttu-id="49f4a-1017">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="49f4a-1017">AccessType::View</span></span>
-   <span data-ttu-id="49f4a-1018">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="49f4a-1018">AccessType::Edit</span></span>
-   <span data-ttu-id="49f4a-1019">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="49f4a-1019">AccessType::Add</span></span>
-   <span data-ttu-id="49f4a-1020">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="49f4a-1020">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-1021">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-1021">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1022">Parameters</span></span>

<span data-ttu-id="49f4a-1023">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1023">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1024">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1024">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="49f4a-1025">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="49f4a-1025">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1026">Parameters</span></span>

<span data-ttu-id="49f4a-1027">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1027">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1028">Return Value</span></span>

### <a name="method-setcompany"></a><span data-ttu-id="49f4a-1029">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="49f4a-1029">Method setCompany</span></span>

    public boolean setCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1030">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1030">Parameters</span></span>

<span data-ttu-id="49f4a-1031">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1031">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1032">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="49f4a-1033">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="49f4a-1033">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1034">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1034">Parameters</span></span>

<span data-ttu-id="49f4a-1035">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1035">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1036">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1036">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="49f4a-1037">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="49f4a-1037">Method webTarget</span></span>

    public str webTarget([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1038">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1038">Parameters</span></span>

<span data-ttu-id="49f4a-1039">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1039">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1040">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1040">Return Value</span></span>

### <a name="method-addseparator"></a><span data-ttu-id="49f4a-1041">メソッド addSeparator</span><span class="sxs-lookup"><span data-stu-id="49f4a-1041">Method addSeparator</span></span>

    public void addSeparator()

### <a name="method-makemenu"></a><span data-ttu-id="49f4a-1042">メソッド makeMenu</span><span class="sxs-lookup"><span data-stu-id="49f4a-1042">Method makeMenu</span></span>

    public void makeMenu(Object outputClass)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1043">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1043">Parameters</span></span>

<span data-ttu-id="49f4a-1044">outputClass</span><span class="sxs-lookup"><span data-stu-id="49f4a-1044">outputClass</span></span>  

### <a name="method-addsubmenu"></a><span data-ttu-id="49f4a-1045">メソッド addSubmenu</span><span class="sxs-lookup"><span data-stu-id="49f4a-1045">Method addSubmenu</span></span>

    public void addSubmenu(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1046">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1046">Parameters</span></span>

<span data-ttu-id="49f4a-1047">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-1047">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="49f4a-1048">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-1048">Method new</span></span>

<span data-ttu-id="49f4a-1049">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1049">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1050">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1050">Parameters</span></span>

<span data-ttu-id="49f4a-1051">氏名</span><span class="sxs-lookup"><span data-stu-id="49f4a-1051">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="49f4a-1052">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="49f4a-1052">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1053">Parameters</span></span>

<span data-ttu-id="49f4a-1054">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="49f4a-1054">webMenuFunction</span></span>  

## <a name="class-webmenufunction"></a><span data-ttu-id="49f4a-1055">クラス WebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="49f4a-1055">Class WebMenuFunction</span></span>
    class WebMenuFunction extends SecureNode

<span data-ttu-id="49f4a-1056">WebMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1056">The WebMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-1057">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1057">Remarks</span></span>

<span data-ttu-id="49f4a-1058">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1058">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1059">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1059">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1060">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-1060">Methods</span></span>

| <span data-ttu-id="49f4a-1061">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1061">Method</span></span>                                                                                           | <span data-ttu-id="49f4a-1062">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1062">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-1063">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1063">public str changedBy(\[str value\])</span></span>                                                              | <span data-ttu-id="49f4a-1064">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1064">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="49f4a-1065">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1065">public Date changedDate(\[Date value\])</span></span>                                                          | <span data-ttu-id="49f4a-1066">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1066">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-1067">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1067">public str changedTime(\[str value\])</span></span>                                                            | <span data-ttu-id="49f4a-1068">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1068">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="49f4a-1069">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1069">public str createdBy(\[str value\])</span></span>                                                              | <span data-ttu-id="49f4a-1070">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1070">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="49f4a-1071">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1071">public Date creationDate(\[Date value\])</span></span>                                                         | <span data-ttu-id="49f4a-1072">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1072">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="49f4a-1073">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1073">public str creationTime(\[str value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="49f4a-1074">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1074">public str helpText(\[str value\])</span></span>                                                               | <span data-ttu-id="49f4a-1075">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1075">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="49f4a-1076">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1076">public str label(\[str value\])</span></span>                                                                  | <span data-ttu-id="49f4a-1077">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1077">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="49f4a-1078">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1078">public str name(\[str value\])</span></span>                                                                   | <span data-ttu-id="49f4a-1079">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1079">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-1080">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1080">public Guid origin(\[Guid value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="49f4a-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span></span> |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="49f4a-1082">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1082">Method changedBy</span></span>

<span data-ttu-id="49f4a-1083">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1083">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1084">Parameters</span></span>

<span data-ttu-id="49f4a-1085">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1085">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1086">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1086">Return Value</span></span>

<span data-ttu-id="49f4a-1087">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1087">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-1088">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1088">Method changedDate</span></span>

<span data-ttu-id="49f4a-1089">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1089">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1090">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1090">Parameters</span></span>

<span data-ttu-id="49f4a-1091">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1091">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1092">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1092">Return Value</span></span>

<span data-ttu-id="49f4a-1093">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1093">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-1094">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1094">Method changedTime</span></span>

<span data-ttu-id="49f4a-1095">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1095">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1096">Parameters</span></span>

<span data-ttu-id="49f4a-1097">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1097">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1098">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1098">Return Value</span></span>

<span data-ttu-id="49f4a-1099">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1099">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-1100">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1100">Method createdBy</span></span>

<span data-ttu-id="49f4a-1101">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1101">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1102">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1102">Parameters</span></span>

<span data-ttu-id="49f4a-1103">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1103">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1104">Return Value</span></span>

<span data-ttu-id="49f4a-1105">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1105">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-1106">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1106">Method creationDate</span></span>

<span data-ttu-id="49f4a-1107">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1107">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1108">Parameters</span></span>

<span data-ttu-id="49f4a-1109">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1109">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1110">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1110">Return Value</span></span>

<span data-ttu-id="49f4a-1111">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1111">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-1112">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1112">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1113">Parameters</span></span>

<span data-ttu-id="49f4a-1114">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1114">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1115">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1115">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="49f4a-1116">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="49f4a-1116">Method helpText</span></span>

<span data-ttu-id="49f4a-1117">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1117">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1118">Parameters</span></span>

<span data-ttu-id="49f4a-1119">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1119">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1120">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1120">Return Value</span></span>

<span data-ttu-id="49f4a-1121">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1121">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1122">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1122">Remarks</span></span>

<span data-ttu-id="49f4a-1123">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1123">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="49f4a-1124">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1124">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="49f4a-1125">メソッド label</span><span class="sxs-lookup"><span data-stu-id="49f4a-1125">Method label</span></span>

<span data-ttu-id="49f4a-1126">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1126">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1127">Parameters</span></span>

<span data-ttu-id="49f4a-1128">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1128">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1129">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1129">Return Value</span></span>

<span data-ttu-id="49f4a-1130">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1130">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1131">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1131">Remarks</span></span>

<span data-ttu-id="49f4a-1132">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1132">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="49f4a-1133">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1133">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-1134">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-1134">Method name</span></span>

<span data-ttu-id="49f4a-1135">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1135">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1136">Parameters</span></span>

<span data-ttu-id="49f4a-1137">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1137">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1138">Return Value</span></span>

<span data-ttu-id="49f4a-1139">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1139">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1140">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1140">Remarks</span></span>

<span data-ttu-id="49f4a-1141">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1141">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-1142">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1142">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-1143">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1143">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-1144">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1144">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-1145">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1145">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-1146">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1146">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-1147">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-1147">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1148">Parameters</span></span>

<span data-ttu-id="49f4a-1149">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1149">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1150">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1150">Return Value</span></span>

### <a name="method-createwebmenufunction"></a><span data-ttu-id="49f4a-1151">メソッド createWebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="49f4a-1151">Method createWebMenuFunction</span></span>

    public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1152">Parameters</span></span>

<span data-ttu-id="49f4a-1153">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-1153">name</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1154">webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="49f4a-1154">webMenuItemType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1155">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1155">Return Value</span></span>

## <a name="class-webmenuitem"></a><span data-ttu-id="49f4a-1156">クラス WebMenuItem</span><span class="sxs-lookup"><span data-stu-id="49f4a-1156">Class WebMenuItem</span></span>
    class WebMenuItem extends TreeNode

<span data-ttu-id="49f4a-1157">WebMenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1157">The WebMenuItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-1158">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1158">Remarks</span></span>

<span data-ttu-id="49f4a-1159">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1159">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="49f4a-1160">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1160">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1161">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1161">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1162">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-1162">Methods</span></span>

| <span data-ttu-id="49f4a-1163">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1163">Method</span></span>                                                         | <span data-ttu-id="49f4a-1164">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1164">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-1165">public str label()</span><span class="sxs-lookup"><span data-stu-id="49f4a-1165">public str label()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="49f4a-1166">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1166">public str menuItemName(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="49f4a-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="49f4a-1168">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1168">public str name(\[str value\])</span></span>                                 | <span data-ttu-id="49f4a-1169">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1169">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-1170">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1170">public str parameters(\[str value\])</span></span>                           | <span data-ttu-id="49f4a-1171">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1171">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="49f4a-1172">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1172">public boolean showParentModule(\[boolean value\])</span></span>             |                                                                                                                                           |

### <a name="method-label"></a><span data-ttu-id="49f4a-1173">メソッド label</span><span class="sxs-lookup"><span data-stu-id="49f4a-1173">Method label</span></span>

    public str label()

#### <a name="return-value"></a><span data-ttu-id="49f4a-1174">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1174">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="49f4a-1175">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="49f4a-1175">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1176">Parameters</span></span>

<span data-ttu-id="49f4a-1177">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1177">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1178">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1178">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="49f4a-1179">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="49f4a-1179">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1180">Parameters</span></span>

<span data-ttu-id="49f4a-1181">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1182">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1182">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-1183">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-1183">Method name</span></span>

<span data-ttu-id="49f4a-1184">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1184">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1185">Parameters</span></span>

<span data-ttu-id="49f4a-1186">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1186">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1187">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1187">Return Value</span></span>

<span data-ttu-id="49f4a-1188">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1188">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1189">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1189">Remarks</span></span>

<span data-ttu-id="49f4a-1190">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1190">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-1191">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1191">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-1192">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1192">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-1193">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1193">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-1194">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1194">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-1195">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1195">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-parameters"></a><span data-ttu-id="49f4a-1196">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="49f4a-1196">Method parameters</span></span>

<span data-ttu-id="49f4a-1197">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1197">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1198">Parameters</span></span>

<span data-ttu-id="49f4a-1199">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1199">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1200">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1200">Return Value</span></span>

<span data-ttu-id="49f4a-1201">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1201">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1202">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1202">Remarks</span></span>

<span data-ttu-id="49f4a-1203">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1203">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="49f4a-1204">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1204">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="49f4a-1205">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="49f4a-1205">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1206">Parameters</span></span>

<span data-ttu-id="49f4a-1207">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1207">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1208">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1208">Return Value</span></span>

## <a name="class-webmodulenode"></a><span data-ttu-id="49f4a-1209">クラス webModuleNode</span><span class="sxs-lookup"><span data-stu-id="49f4a-1209">Class webModuleNode</span></span>
    class webModuleNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="49f4a-1210">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1210">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1211">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1211">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1212">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-1212">Methods</span></span>

| <span data-ttu-id="49f4a-1213">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1213">Method</span></span>                                                                   | <span data-ttu-id="49f4a-1214">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1214">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-1215">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1215">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="49f4a-1216">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1216">Gets or sets the name of the user who last changed the application object.</span></span>                                                                     |
| <span data-ttu-id="49f4a-1217">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1217">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="49f4a-1218">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1218">Gets or sets the date an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="49f4a-1219">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1219">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="49f4a-1220">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1220">Gets or sets the time an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="49f4a-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="49f4a-1222">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1222">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                            |
| <span data-ttu-id="49f4a-1223">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1223">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="49f4a-1224">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1224">Gets or sets the name of the user who created the application object.</span></span>                                                                          |
| <span data-ttu-id="49f4a-1225">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1225">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="49f4a-1226">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1226">Gets or sets the date an application object was created.</span></span>                                                                                       |
| <span data-ttu-id="49f4a-1227">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1227">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="49f4a-1228">public boolean extendedDataSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1228">public boolean extendedDataSecurity(\[boolean value\])</span></span>                   |                                                                                                                                                |
| <span data-ttu-id="49f4a-1229">public boolean inheritNavigation(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1229">public boolean inheritNavigation(\[boolean value\])</span></span>                      |                                                                                                                                                |
| <span data-ttu-id="49f4a-1230">public boolean inheritPermissions(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1230">public boolean inheritPermissions(\[boolean value\])</span></span>                     |                                                                                                                                                |
| <span data-ttu-id="49f4a-1231">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1231">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="49f4a-1232">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1232">Gets or sets the label for a control.</span></span>                                                                                                          |
| <span data-ttu-id="49f4a-1233">public str masterPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1233">public str masterPage(\[str value\])</span></span>                                     |                                                                                                                                                |
| <span data-ttu-id="49f4a-1234">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1234">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="49f4a-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                                |
| <span data-ttu-id="49f4a-1236">public str moduleName()</span><span class="sxs-lookup"><span data-stu-id="49f4a-1236">public str moduleName()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="49f4a-1237">public str modulePath()</span><span class="sxs-lookup"><span data-stu-id="49f4a-1237">public str modulePath()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="49f4a-1238">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1238">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="49f4a-1239">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1239">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-1240">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1240">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="49f4a-1241">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1241">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                        |
| <span data-ttu-id="49f4a-1242">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1242">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="49f4a-1243">public boolean publicModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1243">public boolean publicModule(\[boolean value\])</span></span>                           |                                                                                                                                                |
| <span data-ttu-id="49f4a-1244">public str quickLaunch(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1244">public str quickLaunch(\[str value\])</span></span>                                    |                                                                                                                                                |
| <span data-ttu-id="49f4a-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                                |
| <span data-ttu-id="49f4a-1246">public boolean showLink(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1246">public boolean showLink(\[boolean value\])</span></span>                               |                                                                                                                                                |
| <span data-ttu-id="49f4a-1247">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1247">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                                |
| <span data-ttu-id="49f4a-1248">public void addSubModule(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1248">public void addSubModule(str name)</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="49f4a-1249">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1249">public void new(str Name)</span></span>                                                | <span data-ttu-id="49f4a-1250">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1250">Initializes a new instance of the TreeNode class.</span></span>                                                                                              |
| <span data-ttu-id="49f4a-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                                |

### <a name="method-changedby"></a><span data-ttu-id="49f4a-1252">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1252">Method changedBy</span></span>

<span data-ttu-id="49f4a-1253">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1253">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1254">Parameters</span></span>

<span data-ttu-id="49f4a-1255">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1255">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1256">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1256">Return Value</span></span>

<span data-ttu-id="49f4a-1257">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1257">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-1258">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1258">Method changedDate</span></span>

<span data-ttu-id="49f4a-1259">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1259">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1260">Parameters</span></span>

<span data-ttu-id="49f4a-1261">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1261">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1262">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1262">Return Value</span></span>

<span data-ttu-id="49f4a-1263">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1263">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-1264">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1264">Method changedTime</span></span>

<span data-ttu-id="49f4a-1265">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1265">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1266">Parameters</span></span>

<span data-ttu-id="49f4a-1267">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1267">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1268">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1268">Return Value</span></span>

<span data-ttu-id="49f4a-1269">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1269">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="49f4a-1270">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="49f4a-1270">Method configurationKey</span></span>

<span data-ttu-id="49f4a-1271">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1271">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1272">Parameters</span></span>

<span data-ttu-id="49f4a-1273">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1273">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1274">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1274">Return Value</span></span>

<span data-ttu-id="49f4a-1275">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1275">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1276">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1276">Remarks</span></span>

<span data-ttu-id="49f4a-1277">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1277">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="49f4a-1278">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1278">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-1279">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1279">Method createdBy</span></span>

<span data-ttu-id="49f4a-1280">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1280">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1281">Parameters</span></span>

<span data-ttu-id="49f4a-1282">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1282">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1283">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1283">Return Value</span></span>

<span data-ttu-id="49f4a-1284">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1284">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-1285">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1285">Method creationDate</span></span>

<span data-ttu-id="49f4a-1286">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1286">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1287">Parameters</span></span>

<span data-ttu-id="49f4a-1288">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1288">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1289">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1289">Return Value</span></span>

<span data-ttu-id="49f4a-1290">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1290">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-1291">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1291">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1292">Parameters</span></span>

<span data-ttu-id="49f4a-1293">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1293">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1294">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1294">Return Value</span></span>

### <a name="method-extendeddatasecurity"></a><span data-ttu-id="49f4a-1295">メソッド extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="49f4a-1295">Method extendedDataSecurity</span></span>

    public boolean extendedDataSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1296">Parameters</span></span>

<span data-ttu-id="49f4a-1297">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1297">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1298">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1298">Return Value</span></span>

### <a name="method-inheritnavigation"></a><span data-ttu-id="49f4a-1299">メソッド inheritNavigation</span><span class="sxs-lookup"><span data-stu-id="49f4a-1299">Method inheritNavigation</span></span>

    public boolean inheritNavigation([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1300">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1300">Parameters</span></span>

<span data-ttu-id="49f4a-1301">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1301">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1302">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1302">Return Value</span></span>

### <a name="method-inheritpermissions"></a><span data-ttu-id="49f4a-1303">メソッド inheritPermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-1303">Method inheritPermissions</span></span>

    public boolean inheritPermissions([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1304">Parameters</span></span>

<span data-ttu-id="49f4a-1305">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1305">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1306">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1306">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="49f4a-1307">メソッド label</span><span class="sxs-lookup"><span data-stu-id="49f4a-1307">Method label</span></span>

<span data-ttu-id="49f4a-1308">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1308">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1309">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1309">Parameters</span></span>

<span data-ttu-id="49f4a-1310">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1310">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1311">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1311">Return Value</span></span>

<span data-ttu-id="49f4a-1312">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1312">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1313">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1313">Remarks</span></span>

<span data-ttu-id="49f4a-1314">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1314">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="49f4a-1315">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1315">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-masterpage"></a><span data-ttu-id="49f4a-1316">メソッド masterPage</span><span class="sxs-lookup"><span data-stu-id="49f4a-1316">Method masterPage</span></span>

    public str masterPage([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1317">Parameters</span></span>

<span data-ttu-id="49f4a-1318">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1319">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1319">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="49f4a-1320">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="49f4a-1320">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1321">Parameters</span></span>

<span data-ttu-id="49f4a-1322">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1322">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1323">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1323">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="49f4a-1324">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="49f4a-1324">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1325">Parameters</span></span>

<span data-ttu-id="49f4a-1326">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1326">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1327">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1327">Return Value</span></span>

### <a name="method-modulename"></a><span data-ttu-id="49f4a-1328">メソッド moduleName</span><span class="sxs-lookup"><span data-stu-id="49f4a-1328">Method moduleName</span></span>

    public str moduleName()

#### <a name="return-value"></a><span data-ttu-id="49f4a-1329">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1329">Return Value</span></span>

### <a name="method-modulepath"></a><span data-ttu-id="49f4a-1330">メソッド modulePath</span><span class="sxs-lookup"><span data-stu-id="49f4a-1330">Method modulePath</span></span>

    public str modulePath()

#### <a name="return-value"></a><span data-ttu-id="49f4a-1331">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1331">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-1332">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-1332">Method name</span></span>

<span data-ttu-id="49f4a-1333">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1333">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1334">Parameters</span></span>

<span data-ttu-id="49f4a-1335">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1335">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1336">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1336">Return Value</span></span>

<span data-ttu-id="49f4a-1337">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1337">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1338">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1338">Remarks</span></span>

<span data-ttu-id="49f4a-1339">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1339">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-1340">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1340">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-1341">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1341">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-1342">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1342">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-1343">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1343">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-1344">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1344">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="49f4a-1345">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="49f4a-1345">Method neededAccessLevel</span></span>

<span data-ttu-id="49f4a-1346">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1346">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1347">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1347">Parameters</span></span>

<span data-ttu-id="49f4a-1348">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1348">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1349">Return Value</span></span>

<span data-ttu-id="49f4a-1350">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1350">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1351">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1351">Remarks</span></span>

<span data-ttu-id="49f4a-1352">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1352">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="49f4a-1353">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="49f4a-1353">AccessType::NoAccess</span></span>
-   <span data-ttu-id="49f4a-1354">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="49f4a-1354">AccessType::View</span></span>
-   <span data-ttu-id="49f4a-1355">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="49f4a-1355">AccessType::Edit</span></span>
-   <span data-ttu-id="49f4a-1356">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="49f4a-1356">AccessType::Add</span></span>
-   <span data-ttu-id="49f4a-1357">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="49f4a-1357">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-1358">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-1358">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1359">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1359">Parameters</span></span>

<span data-ttu-id="49f4a-1360">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1360">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1361">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1361">Return Value</span></span>

### <a name="method-publicmodule"></a><span data-ttu-id="49f4a-1362">メソッド publicModule</span><span class="sxs-lookup"><span data-stu-id="49f4a-1362">Method publicModule</span></span>

    public boolean publicModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1363">Parameters</span></span>

<span data-ttu-id="49f4a-1364">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1364">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1365">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1365">Return Value</span></span>

### <a name="method-quicklaunch"></a><span data-ttu-id="49f4a-1366">メソッド quickLaunch</span><span class="sxs-lookup"><span data-stu-id="49f4a-1366">Method quickLaunch</span></span>

    public str quickLaunch([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1367">Parameters</span></span>

<span data-ttu-id="49f4a-1368">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1368">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1369">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1369">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="49f4a-1370">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="49f4a-1370">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1371">Parameters</span></span>

<span data-ttu-id="49f4a-1372">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1372">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1373">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1373">Return Value</span></span>

### <a name="method-showlink"></a><span data-ttu-id="49f4a-1374">メソッド showLink</span><span class="sxs-lookup"><span data-stu-id="49f4a-1374">Method showLink</span></span>

    public boolean showLink([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1375">Parameters</span></span>

<span data-ttu-id="49f4a-1376">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1376">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1377">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1377">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="49f4a-1378">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="49f4a-1378">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1379">Parameters</span></span>

<span data-ttu-id="49f4a-1380">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1380">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1381">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1381">Return Value</span></span>

### <a name="method-addsubmodule"></a><span data-ttu-id="49f4a-1382">メソッド addSubModule</span><span class="sxs-lookup"><span data-stu-id="49f4a-1382">Method addSubModule</span></span>

    public void addSubModule(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1383">Parameters</span></span>

<span data-ttu-id="49f4a-1384">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-1384">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="49f4a-1385">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-1385">Method new</span></span>

<span data-ttu-id="49f4a-1386">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1386">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1387">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1387">Parameters</span></span>

<span data-ttu-id="49f4a-1388">氏名</span><span class="sxs-lookup"><span data-stu-id="49f4a-1388">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="49f4a-1389">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="49f4a-1389">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1390">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1390">Parameters</span></span>

<span data-ttu-id="49f4a-1391">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="49f4a-1391">webMenuFunction</span></span>  

## <a name="class-weboutputcontentitem"></a><span data-ttu-id="49f4a-1392">クラス WebOutputContentItem</span><span class="sxs-lookup"><span data-stu-id="49f4a-1392">Class WebOutputContentItem</span></span>
    class WebOutputContentItem extends WebContentItem

<span data-ttu-id="49f4a-1393">このクラスは、x++ の WebOutputContentItem を表します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1393">This class represents a WebOutputContentItem in x++.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-1394">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1394">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1395">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1395">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1396">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-1396">Methods</span></span>

| <span data-ttu-id="49f4a-1397">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1397">Method</span></span>                    | <span data-ttu-id="49f4a-1398">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1398">Description</span></span>                         |
|---------------------------|-------------------------------------|
| <span data-ttu-id="49f4a-1399">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1399">public void new(str name)</span></span> | <span data-ttu-id="49f4a-1400">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1400">Creates a new WebOutputContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="49f4a-1401">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-1401">Method new</span></span>

<span data-ttu-id="49f4a-1402">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1402">Creates a new WebOutputContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1403">Parameters</span></span>

<span data-ttu-id="49f4a-1404">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-1404">name</span></span>  

## <a name="class-webpagedefnode"></a><span data-ttu-id="49f4a-1405">クラス webPageDefNode</span><span class="sxs-lookup"><span data-stu-id="49f4a-1405">Class webPageDefNode</span></span>
    class webPageDefNode extends TreeNode

<span data-ttu-id="49f4a-1406">webPageDefNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1406">The webPageDefNode class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-1407">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1407">Remarks</span></span>

<span data-ttu-id="49f4a-1408">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1408">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="49f4a-1409">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1409">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1410">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1410">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1411">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-1411">Methods</span></span>

| <span data-ttu-id="49f4a-1412">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1412">Method</span></span>                                                     | <span data-ttu-id="49f4a-1413">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1413">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-1414">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="49f4a-1414">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="49f4a-1415">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1415">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="49f4a-1416">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1416">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="49f4a-1417">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1417">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="49f4a-1418">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1418">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="49f4a-1419">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1419">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-1420">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1420">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="49f4a-1421">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1421">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-1422">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1422">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="49f4a-1423">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1423">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="49f4a-1424">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1424">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="49f4a-1425">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1425">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="49f4a-1426">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1426">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="49f4a-1427">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1427">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="49f4a-1428">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1428">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="49f4a-1429">public str imageResource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1429">public str imageResource(\[str value\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="49f4a-1430">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1430">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="49f4a-1431">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1431">public str name(\[str value\])</span></span>                             | <span data-ttu-id="49f4a-1432">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1432">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-1433">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1433">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="49f4a-1434">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1434">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="49f4a-1435">public str parentPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1435">public str parentPage(\[str value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="49f4a-1436">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1436">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="49f4a-1437">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1437">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="49f4a-1438">public boolean useContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1438">public boolean useContext(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="49f4a-1439">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1439">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="49f4a-1440">public str wSSHelpTopic(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1440">public str wSSHelpTopic(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="49f4a-1441">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1441">public void new(str name)</span></span>                                  | <span data-ttu-id="49f4a-1442">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1442">Creates a new webPageDefNode.</span></span>                                                                                                             |
| <span data-ttu-id="49f4a-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="49f4a-1444">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1444">Set the source of the webPageDefNode to the given string.</span></span>                                                                                 |

### <a name="method-aotgetsource"></a><span data-ttu-id="49f4a-1445">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-1445">Method AOTgetSource</span></span>

<span data-ttu-id="49f4a-1446">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1446">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="49f4a-1447">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1447">Return Value</span></span>

<span data-ttu-id="49f4a-1448">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1448">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1449">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1449">Remarks</span></span>

<span data-ttu-id="49f4a-1450">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1450">This method is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="49f4a-1451">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1451">Method changedBy</span></span>

<span data-ttu-id="49f4a-1452">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1452">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1453">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1453">Parameters</span></span>

<span data-ttu-id="49f4a-1454">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1454">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1455">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1455">Return Value</span></span>

<span data-ttu-id="49f4a-1456">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1456">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-1457">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1457">Method changedDate</span></span>

<span data-ttu-id="49f4a-1458">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1458">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1459">Parameters</span></span>

<span data-ttu-id="49f4a-1460">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1460">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1461">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1461">Return Value</span></span>

<span data-ttu-id="49f4a-1462">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1462">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-1463">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1463">Method changedTime</span></span>

<span data-ttu-id="49f4a-1464">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1464">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1465">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1465">Parameters</span></span>

<span data-ttu-id="49f4a-1466">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1466">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1467">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1467">Return Value</span></span>

<span data-ttu-id="49f4a-1468">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1468">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-1469">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1469">Method createdBy</span></span>

<span data-ttu-id="49f4a-1470">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1470">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1471">Parameters</span></span>

<span data-ttu-id="49f4a-1472">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1472">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1473">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1473">Return Value</span></span>

<span data-ttu-id="49f4a-1474">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1474">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-1475">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1475">Method creationDate</span></span>

<span data-ttu-id="49f4a-1476">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1476">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1477">Parameters</span></span>

<span data-ttu-id="49f4a-1478">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1478">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1479">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1479">Return Value</span></span>

<span data-ttu-id="49f4a-1480">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1480">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-1481">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1481">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1482">Parameters</span></span>

<span data-ttu-id="49f4a-1483">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1484">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1484">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="49f4a-1485">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="49f4a-1485">Method helpText</span></span>

<span data-ttu-id="49f4a-1486">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1486">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1487">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1487">Parameters</span></span>

<span data-ttu-id="49f4a-1488">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1488">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1489">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1489">Return Value</span></span>

<span data-ttu-id="49f4a-1490">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1490">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1491">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1491">Remarks</span></span>

<span data-ttu-id="49f4a-1492">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1492">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="49f4a-1493">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1493">The help text must not exceed 250 characters.</span></span>

### <a name="method-imageresource"></a><span data-ttu-id="49f4a-1494">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="49f4a-1494">Method imageResource</span></span>

    public str imageResource([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1495">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1495">Parameters</span></span>

<span data-ttu-id="49f4a-1496">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1496">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1497">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1497">Return Value</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="49f4a-1498">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="49f4a-1498">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1499">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1499">Parameters</span></span>

<span data-ttu-id="49f4a-1500">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1500">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1501">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-1502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-1502">Method name</span></span>

<span data-ttu-id="49f4a-1503">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1503">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1504">Parameters</span></span>

<span data-ttu-id="49f4a-1505">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1505">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1506">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1506">Return Value</span></span>

<span data-ttu-id="49f4a-1507">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1507">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1508">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1508">Remarks</span></span>

<span data-ttu-id="49f4a-1509">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1509">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-1510">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1510">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-1511">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1511">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-1512">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1512">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-1513">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1513">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-1514">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1514">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-1515">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-1515">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1516">Parameters</span></span>

<span data-ttu-id="49f4a-1517">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1517">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1518">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1518">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="49f4a-1519">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="49f4a-1519">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1520">Parameters</span></span>

<span data-ttu-id="49f4a-1521">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1521">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1522">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1522">Return Value</span></span>

### <a name="method-parentpage"></a><span data-ttu-id="49f4a-1523">メソッド parentPage</span><span class="sxs-lookup"><span data-stu-id="49f4a-1523">Method parentPage</span></span>

    public str parentPage([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1524">Parameters</span></span>

<span data-ttu-id="49f4a-1525">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1525">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1526">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1526">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="49f4a-1527">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="49f4a-1527">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1528">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1528">Parameters</span></span>

<span data-ttu-id="49f4a-1529">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1529">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1530">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1530">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="49f4a-1531">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="49f4a-1531">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1532">Parameters</span></span>

<span data-ttu-id="49f4a-1533">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1533">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1534">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1534">Return Value</span></span>

### <a name="method-usecontext"></a><span data-ttu-id="49f4a-1535">メソッド useContext</span><span class="sxs-lookup"><span data-stu-id="49f4a-1535">Method useContext</span></span>

    public boolean useContext([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1536">Parameters</span></span>

<span data-ttu-id="49f4a-1537">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1538">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1538">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="49f4a-1539">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="49f4a-1539">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1540">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1540">Parameters</span></span>

<span data-ttu-id="49f4a-1541">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1541">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1542">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1542">Return Value</span></span>

### <a name="method-wsshelptopic"></a><span data-ttu-id="49f4a-1543">メソッド wSSHelpTopic</span><span class="sxs-lookup"><span data-stu-id="49f4a-1543">Method wSSHelpTopic</span></span>

    public str wSSHelpTopic([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1544">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1544">Parameters</span></span>

<span data-ttu-id="49f4a-1545">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1545">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1546">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1546">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="49f4a-1547">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-1547">Method new</span></span>

<span data-ttu-id="49f4a-1548">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1548">Creates a new webPageDefNode.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1549">Parameters</span></span>

<span data-ttu-id="49f4a-1550">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-1550">name</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="49f4a-1551">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-1551">Method AOTsetSource</span></span>

<span data-ttu-id="49f4a-1552">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1552">Set the source of the webPageDefNode to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1553">Parameters</span></span>

<span data-ttu-id="49f4a-1554">ソース</span><span class="sxs-lookup"><span data-stu-id="49f4a-1554">source</span></span>  
<span data-ttu-id="49f4a-1555">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1555">Optional parameter marking if the source provided is static.</span></span>

<!-- -->

<span data-ttu-id="49f4a-1556">isStatic</span><span class="sxs-lookup"><span data-stu-id="49f4a-1556">isStatic</span></span>  
<span data-ttu-id="49f4a-1557">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1557">Optional parameter marking if the source provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1558">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1558">Remarks</span></span>

<span data-ttu-id="49f4a-1559">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1559">This method is overridden by nodes which have source code.</span></span>

## <a name="class-webstaticfilenode"></a><span data-ttu-id="49f4a-1560">クラス webStaticFileNode</span><span class="sxs-lookup"><span data-stu-id="49f4a-1560">Class webStaticFileNode</span></span>
    class webStaticFileNode extends TreeNode

<span data-ttu-id="49f4a-1561">webStaticFileNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1561">The webStaticFileNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-1562">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1562">Remarks</span></span>

<span data-ttu-id="49f4a-1563">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1563">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1564">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1564">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1565">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-1565">Methods</span></span>

| <span data-ttu-id="49f4a-1566">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1566">Method</span></span>                                                     | <span data-ttu-id="49f4a-1567">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1567">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-1568">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="49f4a-1568">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="49f4a-1569">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1569">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="49f4a-1570">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1570">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="49f4a-1571">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1571">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="49f4a-1572">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1572">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="49f4a-1573">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1573">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-1574">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1574">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="49f4a-1575">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1575">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="49f4a-1576">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1576">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="49f4a-1577">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1577">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="49f4a-1578">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1578">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="49f4a-1579">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1579">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="49f4a-1580">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1580">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="49f4a-1581">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1581">public str filename(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="49f4a-1582">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1582">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="49f4a-1583">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1583">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="49f4a-1584">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1584">public str name(\[str value\])</span></span>                             | <span data-ttu-id="49f4a-1585">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1585">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="49f4a-1586">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1586">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="49f4a-1587">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1587">public str relativePath(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="49f4a-1588">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1588">public str version(\[str value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="49f4a-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="49f4a-1590">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1590">Sets the source of the static file node to the given string.</span></span>                                                                              |

### <a name="method-aotgetsource"></a><span data-ttu-id="49f4a-1591">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-1591">Method AOTgetSource</span></span>

<span data-ttu-id="49f4a-1592">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1592">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="49f4a-1593">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1593">Return Value</span></span>

<span data-ttu-id="49f4a-1594">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1594">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1595">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1595">Remarks</span></span>

<span data-ttu-id="49f4a-1596">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1596">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="49f4a-1597">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1597">Method changedBy</span></span>

<span data-ttu-id="49f4a-1598">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1598">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1599">Parameters</span></span>

<span data-ttu-id="49f4a-1600">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1600">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1601">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1601">Return Value</span></span>

<span data-ttu-id="49f4a-1602">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1602">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49f4a-1603">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1603">Method changedDate</span></span>

<span data-ttu-id="49f4a-1604">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1604">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1605">Parameters</span></span>

<span data-ttu-id="49f4a-1606">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1606">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1607">Return Value</span></span>

<span data-ttu-id="49f4a-1608">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1608">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49f4a-1609">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1609">Method changedTime</span></span>

<span data-ttu-id="49f4a-1610">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1610">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1611">Parameters</span></span>

<span data-ttu-id="49f4a-1612">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1612">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1613">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1613">Return Value</span></span>

<span data-ttu-id="49f4a-1614">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1614">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49f4a-1615">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49f4a-1615">Method createdBy</span></span>

<span data-ttu-id="49f4a-1616">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1616">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1617">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1617">Parameters</span></span>

<span data-ttu-id="49f4a-1618">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1618">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1619">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1619">Return Value</span></span>

<span data-ttu-id="49f4a-1620">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1620">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49f4a-1621">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49f4a-1621">Method creationDate</span></span>

<span data-ttu-id="49f4a-1622">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1622">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1623">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1623">Parameters</span></span>

<span data-ttu-id="49f4a-1624">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1624">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1625">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1625">Return Value</span></span>

<span data-ttu-id="49f4a-1626">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1626">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49f4a-1627">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49f4a-1627">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1628">Parameters</span></span>

<span data-ttu-id="49f4a-1629">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1630">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1630">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="49f4a-1631">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="49f4a-1631">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1632">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1632">Parameters</span></span>

<span data-ttu-id="49f4a-1633">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1633">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1634">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1634">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="49f4a-1635">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="49f4a-1635">Method helpText</span></span>

<span data-ttu-id="49f4a-1636">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1636">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1637">Parameters</span></span>

<span data-ttu-id="49f4a-1638">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1638">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1639">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1639">Return Value</span></span>

<span data-ttu-id="49f4a-1640">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1640">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1641">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1641">Remarks</span></span>

<span data-ttu-id="49f4a-1642">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1642">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="49f4a-1643">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1643">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="49f4a-1644">メソッド名</span><span class="sxs-lookup"><span data-stu-id="49f4a-1644">Method name</span></span>

<span data-ttu-id="49f4a-1645">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1645">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1646">Parameters</span></span>

<span data-ttu-id="49f4a-1647">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1648">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1648">Return Value</span></span>

<span data-ttu-id="49f4a-1649">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1649">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1650">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1650">Remarks</span></span>

<span data-ttu-id="49f4a-1651">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1651">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="49f4a-1652">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1652">Begins with a letter.</span></span>
-   <span data-ttu-id="49f4a-1653">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1653">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="49f4a-1654">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1654">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="49f4a-1655">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1655">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="49f4a-1656">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1656">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-1657">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-1657">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1658">Parameters</span></span>

<span data-ttu-id="49f4a-1659">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1659">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1660">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1660">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="49f4a-1661">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="49f4a-1661">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1662">Parameters</span></span>

<span data-ttu-id="49f4a-1663">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1664">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1664">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="49f4a-1665">メソッド version</span><span class="sxs-lookup"><span data-stu-id="49f4a-1665">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1666">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1666">Parameters</span></span>

<span data-ttu-id="49f4a-1667">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1667">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1668">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1668">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="49f4a-1669">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="49f4a-1669">Method AOTsetSource</span></span>

<span data-ttu-id="49f4a-1670">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1670">Sets the source of the static file node to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1671">Parameters</span></span>

<span data-ttu-id="49f4a-1672">ソース</span><span class="sxs-lookup"><span data-stu-id="49f4a-1672">source</span></span>  
<span data-ttu-id="49f4a-1673">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1673">An optional parameter that marks whether the source that is provided is static.</span></span>

<!-- -->

<span data-ttu-id="49f4a-1674">isStatic</span><span class="sxs-lookup"><span data-stu-id="49f4a-1674">isStatic</span></span>  
<span data-ttu-id="49f4a-1675">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1675">An optional parameter that marks whether the source that is provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1676">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1676">Remarks</span></span>

<span data-ttu-id="49f4a-1677">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1677">This method is overridden by nodes that have source code.</span></span>

## <a name="class-weburlmenufunction"></a><span data-ttu-id="49f4a-1678">クラス WebUrlMenuFunction</span><span class="sxs-lookup"><span data-stu-id="49f4a-1678">Class WebUrlMenuFunction</span></span>
    class WebUrlMenuFunction extends WebMenuFunction

<span data-ttu-id="49f4a-1679">WebUrlMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1679">The WebUrlMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="49f4a-1680">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1680">Remarks</span></span>

<span data-ttu-id="49f4a-1681">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1681">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1682">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1682">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1683">メソッド</span><span class="sxs-lookup"><span data-stu-id="49f4a-1683">Methods</span></span>

| <span data-ttu-id="49f4a-1684">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1684">Method</span></span>                                                | <span data-ttu-id="49f4a-1685">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1685">Description</span></span>                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f4a-1686">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1686">public boolean big(\[boolean value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="49f4a-1687">public int closeDialogBehavior(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1687">public int closeDialogBehavior(\[int value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="49f4a-1688">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1688">public int correctPermissions(\[int value\])</span></span>          |                                                                                                        |
| <span data-ttu-id="49f4a-1689">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1689">public int createPermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="49f4a-1690">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1690">public int deletePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="49f4a-1691">public boolean hideActionPane(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1691">public boolean hideActionPane(\[boolean value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="49f4a-1692">public boolean homePage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1692">public boolean homePage(\[boolean value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="49f4a-1693">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1693">public int imageLocation(\[int value\])</span></span>               |                                                                                                        |
| <span data-ttu-id="49f4a-1694">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1694">public str linkedPermissionObject(\[str value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="49f4a-1695">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1695">public str linkedPermissionObjectChild(\[str value\])</span></span> |                                                                                                        |
| <span data-ttu-id="49f4a-1696">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1696">public int linkedPermissionType(\[int value\])</span></span>        |                                                                                                        |
| <span data-ttu-id="49f4a-1697">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1697">public int maintainUserLicense(\[int value\])</span></span>         | <span data-ttu-id="49f4a-1698">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1698">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="49f4a-1699">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1699">public boolean multiSelect(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="49f4a-1700">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1700">public boolean needsRecord(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="49f4a-1701">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1701">public str normalImage(\[str value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="49f4a-1702">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1702">public int normalResource(\[int value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="49f4a-1703">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1703">public Guid origin(\[Guid value\])</span></span>                    |                                                                                                        |
| <span data-ttu-id="49f4a-1704">public str pageDefinition(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1704">public str pageDefinition(\[str value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="49f4a-1705">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1705">public str parameters(\[str value\])</span></span>                  | <span data-ttu-id="49f4a-1706">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1706">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span> |
| <span data-ttu-id="49f4a-1707">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1707">public int readPermissions(\[int value\])</span></span>             |                                                                                                        |
| <span data-ttu-id="49f4a-1708">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1708">public int updatePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="49f4a-1709">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1709">public str uRL(\[str value\])</span></span>                         |                                                                                                        |
| <span data-ttu-id="49f4a-1710">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1710">public int viewUserLicense(\[int value\])</span></span>             | <span data-ttu-id="49f4a-1711">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1711">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="49f4a-1712">public int windowMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1712">public int windowMode(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="49f4a-1713">public str windowParameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1713">public str windowParameters(\[str value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="49f4a-1714">public int windowSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1714">public int windowSize(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="49f4a-1715">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1715">public void new(str name)</span></span>                             | <span data-ttu-id="49f4a-1716">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1716">Initializes a new instance of the TreeNode class.</span></span>                                                      |

### <a name="method-big"></a><span data-ttu-id="49f4a-1717">メソッド big</span><span class="sxs-lookup"><span data-stu-id="49f4a-1717">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1718">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1718">Parameters</span></span>

<span data-ttu-id="49f4a-1719">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1719">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1720">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1720">Return Value</span></span>

### <a name="method-closedialogbehavior"></a><span data-ttu-id="49f4a-1721">メソッド closeDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="49f4a-1721">Method closeDialogBehavior</span></span>

    public int closeDialogBehavior([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1722">Parameters</span></span>

<span data-ttu-id="49f4a-1723">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1723">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1724">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1724">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="49f4a-1725">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-1725">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1726">Parameters</span></span>

<span data-ttu-id="49f4a-1727">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1728">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1728">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="49f4a-1729">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-1729">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1730">Parameters</span></span>

<span data-ttu-id="49f4a-1731">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1731">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1732">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1732">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="49f4a-1733">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-1733">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1734">Parameters</span></span>

<span data-ttu-id="49f4a-1735">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1736">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1736">Return Value</span></span>

### <a name="method-hideactionpane"></a><span data-ttu-id="49f4a-1737">メソッド hideActionPane</span><span class="sxs-lookup"><span data-stu-id="49f4a-1737">Method hideActionPane</span></span>

    public boolean hideActionPane([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1738">Parameters</span></span>

<span data-ttu-id="49f4a-1739">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1739">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1740">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1740">Return Value</span></span>

### <a name="method-homepage"></a><span data-ttu-id="49f4a-1741">メソッド homePage</span><span class="sxs-lookup"><span data-stu-id="49f4a-1741">Method homePage</span></span>

    public boolean homePage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1742">Parameters</span></span>

<span data-ttu-id="49f4a-1743">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1743">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1744">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1744">Return Value</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="49f4a-1745">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="49f4a-1745">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1746">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1746">Parameters</span></span>

<span data-ttu-id="49f4a-1747">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1747">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1748">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1748">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="49f4a-1749">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="49f4a-1749">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1750">Parameters</span></span>

<span data-ttu-id="49f4a-1751">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1751">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1752">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1752">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="49f4a-1753">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="49f4a-1753">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1754">Parameters</span></span>

<span data-ttu-id="49f4a-1755">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1755">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1756">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1756">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="49f4a-1757">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="49f4a-1757">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1758">Parameters</span></span>

<span data-ttu-id="49f4a-1759">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1759">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1760">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1760">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="49f4a-1761">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="49f4a-1761">Method maintainUserLicense</span></span>

<span data-ttu-id="49f4a-1762">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1762">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1763">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1763">Parameters</span></span>

<span data-ttu-id="49f4a-1764">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1764">value</span></span>  
<span data-ttu-id="49f4a-1765">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1765">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="49f4a-1766">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1766">Return Value</span></span>

<span data-ttu-id="49f4a-1767">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1767">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="49f4a-1768">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="49f4a-1768">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1769">Parameters</span></span>

<span data-ttu-id="49f4a-1770">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1770">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1771">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1771">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="49f4a-1772">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="49f4a-1772">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1773">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1773">Parameters</span></span>

<span data-ttu-id="49f4a-1774">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1774">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1775">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1775">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="49f4a-1776">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="49f4a-1776">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1777">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1777">Parameters</span></span>

<span data-ttu-id="49f4a-1778">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1778">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1779">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1779">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="49f4a-1780">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="49f4a-1780">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1781">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1781">Parameters</span></span>

<span data-ttu-id="49f4a-1782">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1782">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1783">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1783">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="49f4a-1784">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49f4a-1784">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1785">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1785">Parameters</span></span>

<span data-ttu-id="49f4a-1786">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1786">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1787">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1787">Return Value</span></span>

### <a name="method-pagedefinition"></a><span data-ttu-id="49f4a-1788">メソッド pageDefinition</span><span class="sxs-lookup"><span data-stu-id="49f4a-1788">Method pageDefinition</span></span>

    public str pageDefinition([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1789">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1789">Parameters</span></span>

<span data-ttu-id="49f4a-1790">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1790">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1791">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1791">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="49f4a-1792">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="49f4a-1792">Method parameters</span></span>

<span data-ttu-id="49f4a-1793">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1793">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1794">Parameters</span></span>

<span data-ttu-id="49f4a-1795">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1796">Return Value</span></span>

<span data-ttu-id="49f4a-1797">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1797">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49f4a-1798">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1798">Remarks</span></span>

<span data-ttu-id="49f4a-1799">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1799">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="49f4a-1800">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1800">Objects will ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="49f4a-1801">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-1801">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1802">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1802">Parameters</span></span>

<span data-ttu-id="49f4a-1803">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1803">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1804">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1804">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="49f4a-1805">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="49f4a-1805">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1806">Parameters</span></span>

<span data-ttu-id="49f4a-1807">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1808">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1808">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="49f4a-1809">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="49f4a-1809">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1810">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1810">Parameters</span></span>

<span data-ttu-id="49f4a-1811">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1811">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1812">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1812">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="49f4a-1813">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="49f4a-1813">Method viewUserLicense</span></span>

<span data-ttu-id="49f4a-1814">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1814">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1815">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1815">Parameters</span></span>

<span data-ttu-id="49f4a-1816">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1816">value</span></span>  
<span data-ttu-id="49f4a-1817">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1817">A user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="49f4a-1818">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1818">Return Value</span></span>

<span data-ttu-id="49f4a-1819">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1819">The user license.</span></span>

### <a name="method-windowmode"></a><span data-ttu-id="49f4a-1820">メソッド windowMode</span><span class="sxs-lookup"><span data-stu-id="49f4a-1820">Method windowMode</span></span>

    public int windowMode([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1821">Parameters</span></span>

<span data-ttu-id="49f4a-1822">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1822">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1823">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1823">Return Value</span></span>

### <a name="method-windowparameters"></a><span data-ttu-id="49f4a-1824">メソッド windowParameters</span><span class="sxs-lookup"><span data-stu-id="49f4a-1824">Method windowParameters</span></span>

    public str windowParameters([str value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1825">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1825">Parameters</span></span>

<span data-ttu-id="49f4a-1826">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1826">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1827">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1827">Return Value</span></span>

### <a name="method-windowsize"></a><span data-ttu-id="49f4a-1828">メソッド windowSize</span><span class="sxs-lookup"><span data-stu-id="49f4a-1828">Method windowSize</span></span>

    public int windowSize([int value])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1829">Parameters</span></span>

<span data-ttu-id="49f4a-1830">値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1831">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1831">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="49f4a-1832">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-1832">Method new</span></span>

<span data-ttu-id="49f4a-1833">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1833">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1834">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1834">Parameters</span></span>

<span data-ttu-id="49f4a-1835">名前</span><span class="sxs-lookup"><span data-stu-id="49f4a-1835">name</span></span>  

## <a name="class-winapinative"></a><span data-ttu-id="49f4a-1836">クラス WinAPINative</span><span class="sxs-lookup"><span data-stu-id="49f4a-1836">Class WinAPINative</span></span>
    class WinAPINative extends Object

### <a name="remarks"></a><span data-ttu-id="49f4a-1837">備考</span><span class="sxs-lookup"><span data-stu-id="49f4a-1837">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49f4a-1838">例</span><span class="sxs-lookup"><span data-stu-id="49f4a-1838">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49f4a-1839">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1839">Methods</span></span>

| <span data-ttu-id="49f4a-1840">方法</span><span class="sxs-lookup"><span data-stu-id="49f4a-1840">Method</span></span>                                                                                                                  | <span data-ttu-id="49f4a-1841">説明</span><span class="sxs-lookup"><span data-stu-id="49f4a-1841">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="49f4a-1842">::public static Int64 createFontIndirect(Binary logfont)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1842">::public static Int64 createFontIndirect(Binary logfont)</span></span>                                                                |                                                       |
| <span data-ttu-id="49f4a-1843">::public static boolean deleteObject(Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1843">::public static boolean deleteObject(Int64 hGDIObject)</span></span>                                                                  |                                                       |
| <span data-ttu-id="49f4a-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span></span> |                                                       |
| <span data-ttu-id="49f4a-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span></span>                                                                 |                                                       |
| <span data-ttu-id="49f4a-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span></span>                              |                                                       |
| <span data-ttu-id="49f4a-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span><span class="sxs-lookup"><span data-stu-id="49f4a-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span></span>                                                    |                                                       |
| <span data-ttu-id="49f4a-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span></span>                                           |                                                       |
| <span data-ttu-id="49f4a-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span></span>                                                       |                                                       |
| <span data-ttu-id="49f4a-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span></span>                        |                                                       |
| <span data-ttu-id="49f4a-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="49f4a-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span></span>                                                         |                                                       |
| <span data-ttu-id="49f4a-1852">private void new()</span><span class="sxs-lookup"><span data-stu-id="49f4a-1852">private void new()</span></span>                                                                                                      | <span data-ttu-id="49f4a-1853">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1853">Initializes a new instance of the WinAPINative class.</span></span> |

### <a name="method-createfontindirect"></a><span data-ttu-id="49f4a-1854">メソッド createFontIndirect</span><span class="sxs-lookup"><span data-stu-id="49f4a-1854">Method createFontIndirect</span></span>

    public static Int64 createFontIndirect(Binary logfont)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1855">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1855">Parameters</span></span>

<span data-ttu-id="49f4a-1856">logfont</span><span class="sxs-lookup"><span data-stu-id="49f4a-1856">logfont</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1857">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1857">Return Value</span></span>

### <a name="method-deleteobject"></a><span data-ttu-id="49f4a-1858">メソッド deleteObject</span><span class="sxs-lookup"><span data-stu-id="49f4a-1858">Method deleteObject</span></span>

    public static boolean deleteObject(Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1859">Parameters</span></span>

<span data-ttu-id="49f4a-1860">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="49f4a-1860">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1861">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1861">Return Value</span></span>

### <a name="method-getcharabcwidthsi"></a><span data-ttu-id="49f4a-1862">メソッド getCharABCWidthsI</span><span class="sxs-lookup"><span data-stu-id="49f4a-1862">Method getCharABCWidthsI</span></span>

    public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1863">Parameters</span></span>

<span data-ttu-id="49f4a-1864">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1864">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1865">firstGlyphIndex</span><span class="sxs-lookup"><span data-stu-id="49f4a-1865">firstGlyphIndex</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1866">glyphIndicesCount</span><span class="sxs-lookup"><span data-stu-id="49f4a-1866">glyphIndicesCount</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1867">charWidths</span><span class="sxs-lookup"><span data-stu-id="49f4a-1867">charWidths</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1868">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1868">Return Value</span></span>

### <a name="method-getdevicecaps"></a><span data-ttu-id="49f4a-1869">メソッド getDeviceCaps</span><span class="sxs-lookup"><span data-stu-id="49f4a-1869">Method getDeviceCaps</span></span>

    public static int getDeviceCaps(Int64 hDC, int index)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1870">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1870">Parameters</span></span>

<span data-ttu-id="49f4a-1871">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1871">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1872">指数</span><span class="sxs-lookup"><span data-stu-id="49f4a-1872">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1873">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1873">Return Value</span></span>

### <a name="method-getfontdata"></a><span data-ttu-id="49f4a-1874">メソッド getFontData</span><span class="sxs-lookup"><span data-stu-id="49f4a-1874">Method getFontData</span></span>

    public static int getFontData(Int64 hDC, int dwTable, int dwOffset, [Binary pvBuffer])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1875">Parameters</span></span>

<span data-ttu-id="49f4a-1876">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1876">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1877">dwTable</span><span class="sxs-lookup"><span data-stu-id="49f4a-1877">dwTable</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1878">dwOffset</span><span class="sxs-lookup"><span data-stu-id="49f4a-1878">dwOffset</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1879">pvBuffer</span><span class="sxs-lookup"><span data-stu-id="49f4a-1879">pvBuffer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1880">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1880">Return Value</span></span>

### <a name="method-getfontunicoderanges"></a><span data-ttu-id="49f4a-1881">メソッド getFontUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="49f4a-1881">Method getFontUnicodeRanges</span></span>

    public static int getFontUnicodeRanges(Int64 hDC, [Binary lpgs])

#### <a name="parameters"></a><span data-ttu-id="49f4a-1882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1882">Parameters</span></span>

<span data-ttu-id="49f4a-1883">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1883">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1884">lpgs</span><span class="sxs-lookup"><span data-stu-id="49f4a-1884">lpgs</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1885">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1885">Return Value</span></span>

### <a name="method-getglyphindices"></a><span data-ttu-id="49f4a-1886">メソッド getGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="49f4a-1886">Method getGlyphIndices</span></span>

    public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1887">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1887">Parameters</span></span>

<span data-ttu-id="49f4a-1888">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1888">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1889">lpstr</span><span class="sxs-lookup"><span data-stu-id="49f4a-1889">lpstr</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1890">pgi</span><span class="sxs-lookup"><span data-stu-id="49f4a-1890">pgi</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1891">fl</span><span class="sxs-lookup"><span data-stu-id="49f4a-1891">fl</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1892">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1892">Return Value</span></span>

### <a name="method-gettextmetrics"></a><span data-ttu-id="49f4a-1893">メソッド getTextMetrics</span><span class="sxs-lookup"><span data-stu-id="49f4a-1893">Method getTextMetrics</span></span>

    public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1894">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1894">Parameters</span></span>

<span data-ttu-id="49f4a-1895">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1895">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1896">lpMetrics</span><span class="sxs-lookup"><span data-stu-id="49f4a-1896">lpMetrics</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1897">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1897">Return Value</span></span>

### <a name="method-getuniscribeglyphindices"></a><span data-ttu-id="49f4a-1898">メソッド getUniscribeGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="49f4a-1898">Method getUniscribeGlyphIndices</span></span>

    public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1899">Parameters</span></span>

<span data-ttu-id="49f4a-1900">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1900">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1901">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="49f4a-1901">hGDIObject</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1902">lpstr</span><span class="sxs-lookup"><span data-stu-id="49f4a-1902">lpstr</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1903">pgi</span><span class="sxs-lookup"><span data-stu-id="49f4a-1903">pgi</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1904">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1904">Return Value</span></span>

### <a name="method-selectobject"></a><span data-ttu-id="49f4a-1905">メソッド selectObject</span><span class="sxs-lookup"><span data-stu-id="49f4a-1905">Method selectObject</span></span>

    public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="49f4a-1906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49f4a-1906">Parameters</span></span>

<span data-ttu-id="49f4a-1907">hDC</span><span class="sxs-lookup"><span data-stu-id="49f4a-1907">hDC</span></span>  

<!-- -->

<span data-ttu-id="49f4a-1908">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="49f4a-1908">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49f4a-1909">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f4a-1909">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="49f4a-1910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49f4a-1910">Method new</span></span>

<span data-ttu-id="49f4a-1911">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49f4a-1911">Initializes a new instance of the WinAPINative class.</span></span>

    private void new()



