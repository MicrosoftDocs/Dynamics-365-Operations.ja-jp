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
ms.openlocfilehash: bc8abf5fe95957fc20445140a07a8e47620d27be
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191605"
---
# <a name="w-classes"></a><span data-ttu-id="37a61-103">W クラス</span><span class="sxs-lookup"><span data-stu-id="37a61-103">W classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37a61-104">文字 W で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="37a61-104">System API classes that start with the letter W.</span></span>

<a name="class-webactionmenufunction"></a><span data-ttu-id="37a61-105">クラス WebActionMenuFunction</span><span class="sxs-lookup"><span data-stu-id="37a61-105">Class WebActionMenuFunction</span></span>
---------------------------

    class WebActionMenuFunction extends WebMenuFunction

<span data-ttu-id="37a61-106">WebActionMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-106">The WebActionMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-107">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-107">Remarks</span></span>

<span data-ttu-id="37a61-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-109">例</span><span class="sxs-lookup"><span data-stu-id="37a61-109">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-110">Methods</span></span>

| <span data-ttu-id="37a61-111">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-111">Method</span></span>                                                   | <span data-ttu-id="37a61-112">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-112">Description</span></span>                                                                                                 |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-113">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-113">public boolean big(\[boolean value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="37a61-114">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-114">public int correctPermissions(\[int value\])</span></span>             |                                                                                                             |
| <span data-ttu-id="37a61-115">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-115">public int createPermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="37a61-116">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-116">public int deletePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="37a61-117">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-117">public int enumParameter(\[int value\])</span></span>                  | <span data-ttu-id="37a61-118">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-118">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span> |
| <span data-ttu-id="37a61-119">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-119">public EnumId enumTypeParameter(\[EnumId value\])</span></span>        | <span data-ttu-id="37a61-120">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-120">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                     |
| <span data-ttu-id="37a61-121">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-121">public int imageLocation(\[int value\])</span></span>                  |                                                                                                             |
| <span data-ttu-id="37a61-122">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-122">public str linkedPermissionObject(\[str value\])</span></span>         |                                                                                                             |
| <span data-ttu-id="37a61-123">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-123">public str linkedPermissionObjectChild(\[str value\])</span></span>    |                                                                                                             |
| <span data-ttu-id="37a61-124">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-124">public int linkedPermissionType(\[int value\])</span></span>           |                                                                                                             |
| <span data-ttu-id="37a61-125">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-125">public int maintainUserLicense(\[int value\])</span></span>            | <span data-ttu-id="37a61-126">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-126">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="37a61-127">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-127">public boolean multiSelect(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="37a61-128">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-128">public boolean needsRecord(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="37a61-129">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-129">public str normalImage(\[str value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="37a61-130">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-130">public int normalResource(\[int value\])</span></span>                 |                                                                                                             |
| <span data-ttu-id="37a61-131">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-131">public str object(\[str value\])</span></span>                         | <span data-ttu-id="37a61-132">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-132">Gets or sets the object that the MenuFunction class runs.</span></span>                                                   |
| <span data-ttu-id="37a61-133">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-133">public int objectType(\[int value\])</span></span>                     |                                                                                                             |
| <span data-ttu-id="37a61-134">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-134">public Guid origin(\[Guid value\])</span></span>                       |                                                                                                             |
| <span data-ttu-id="37a61-135">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-135">public str parameters(\[str value\])</span></span>                     | <span data-ttu-id="37a61-136">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-136">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>      |
| <span data-ttu-id="37a61-137">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-137">public int readPermissions(\[int value\])</span></span>                |                                                                                                             |
| <span data-ttu-id="37a61-138">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-138">public str reportDesign(\[str value\])</span></span>                   |                                                                                                             |
| <span data-ttu-id="37a61-139">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-139">public int runOn(\[int value\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="37a61-140">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-140">public int updatePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="37a61-141">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-141">public int viewUserLicense(\[int value\])</span></span>                | <span data-ttu-id="37a61-142">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-142">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="37a61-143">::public static void runCalled(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="37a61-143">::public static void runCalled(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="37a61-144">public void AOTrun(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="37a61-144">public void AOTrun(\[xArgs args\])</span></span>                       | <span data-ttu-id="37a61-145">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="37a61-145">Compiles this node and its sub-tree in the Application Object Tree (AOT).</span></span>             |
| <span data-ttu-id="37a61-146">::public static void runClient(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="37a61-146">::public static void runClient(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="37a61-147">public void run(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="37a61-147">public void run(\[xArgs args\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="37a61-148">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-148">public void new(str name)</span></span>                                | <span data-ttu-id="37a61-149">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-149">Initializes a new instance of the TreeNode class.</span></span>                                                           |
| <span data-ttu-id="37a61-150">::public static void runServer(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="37a61-150">::public static void runServer(str name, \[xArgs args\])</span></span> |                                                                                                             |

### <a name="method-big"></a><span data-ttu-id="37a61-151">メソッド big</span><span class="sxs-lookup"><span data-stu-id="37a61-151">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-152">Parameters</span></span>

<span data-ttu-id="37a61-153">値</span><span class="sxs-lookup"><span data-stu-id="37a61-153">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-154">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="37a61-155">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-155">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-156">Parameters</span></span>

<span data-ttu-id="37a61-157">値</span><span class="sxs-lookup"><span data-stu-id="37a61-157">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-158">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="37a61-159">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-159">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-160">Parameters</span></span>

<span data-ttu-id="37a61-161">値</span><span class="sxs-lookup"><span data-stu-id="37a61-161">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-162">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="37a61-163">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-163">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-164">Parameters</span></span>

<span data-ttu-id="37a61-165">値</span><span class="sxs-lookup"><span data-stu-id="37a61-165">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-166">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="37a61-167">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="37a61-167">Method enumParameter</span></span>

<span data-ttu-id="37a61-168">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-168">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-169">Parameters</span></span>

<span data-ttu-id="37a61-170">値</span><span class="sxs-lookup"><span data-stu-id="37a61-170">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-171">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-171">Return Value</span></span>

<span data-ttu-id="37a61-172">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="37a61-172">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="37a61-173">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="37a61-173">Method enumTypeParameter</span></span>

<span data-ttu-id="37a61-174">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-174">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="37a61-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-175">Parameters</span></span>

<span data-ttu-id="37a61-176">値</span><span class="sxs-lookup"><span data-stu-id="37a61-176">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-177">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-177">Return Value</span></span>

<span data-ttu-id="37a61-178">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="37a61-178">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="37a61-179">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="37a61-179">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-180">Parameters</span></span>

<span data-ttu-id="37a61-181">値</span><span class="sxs-lookup"><span data-stu-id="37a61-181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-182">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="37a61-183">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="37a61-183">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-184">Parameters</span></span>

<span data-ttu-id="37a61-185">値</span><span class="sxs-lookup"><span data-stu-id="37a61-185">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-186">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-186">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="37a61-187">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="37a61-187">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-188">Parameters</span></span>

<span data-ttu-id="37a61-189">値</span><span class="sxs-lookup"><span data-stu-id="37a61-189">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-190">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-190">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="37a61-191">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="37a61-191">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-192">Parameters</span></span>

<span data-ttu-id="37a61-193">値</span><span class="sxs-lookup"><span data-stu-id="37a61-193">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-194">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="37a61-195">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="37a61-195">Method maintainUserLicense</span></span>

<span data-ttu-id="37a61-196">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-196">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-197">Parameters</span></span>

<span data-ttu-id="37a61-198">値</span><span class="sxs-lookup"><span data-stu-id="37a61-198">value</span></span>  
<span data-ttu-id="37a61-199">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-199">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="37a61-200">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-200">Return Value</span></span>

<span data-ttu-id="37a61-201">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-201">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="37a61-202">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="37a61-202">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-203">Parameters</span></span>

<span data-ttu-id="37a61-204">値</span><span class="sxs-lookup"><span data-stu-id="37a61-204">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-205">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="37a61-206">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="37a61-206">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-207">Parameters</span></span>

<span data-ttu-id="37a61-208">値</span><span class="sxs-lookup"><span data-stu-id="37a61-208">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-209">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-209">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="37a61-210">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="37a61-210">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-211">Parameters</span></span>

<span data-ttu-id="37a61-212">値</span><span class="sxs-lookup"><span data-stu-id="37a61-212">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-213">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-213">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="37a61-214">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="37a61-214">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-215">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-215">Parameters</span></span>

<span data-ttu-id="37a61-216">値</span><span class="sxs-lookup"><span data-stu-id="37a61-216">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-217">Return Value</span></span>

### <a name="method-object"></a><span data-ttu-id="37a61-218">メソッド object</span><span class="sxs-lookup"><span data-stu-id="37a61-218">Method object</span></span>

<span data-ttu-id="37a61-219">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-219">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-220">Parameters</span></span>

<span data-ttu-id="37a61-221">値</span><span class="sxs-lookup"><span data-stu-id="37a61-221">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-222">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-222">Return Value</span></span>

<span data-ttu-id="37a61-223">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="37a61-223">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-224">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-224">Remarks</span></span>

<span data-ttu-id="37a61-225">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-225">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="37a61-226">フォーム</span><span class="sxs-lookup"><span data-stu-id="37a61-226">Form</span></span>
-   <span data-ttu-id="37a61-227">レポート </span><span class="sxs-lookup"><span data-stu-id="37a61-227">Report</span></span>
-   <span data-ttu-id="37a61-228">ジョブ</span><span class="sxs-lookup"><span data-stu-id="37a61-228">Job</span></span>
-   <span data-ttu-id="37a61-229">クラス</span><span class="sxs-lookup"><span data-stu-id="37a61-229">Class</span></span>
-   <span data-ttu-id="37a61-230">クエリ</span><span class="sxs-lookup"><span data-stu-id="37a61-230">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="37a61-231">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="37a61-231">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-232">Parameters</span></span>

<span data-ttu-id="37a61-233">値</span><span class="sxs-lookup"><span data-stu-id="37a61-233">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-234">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-235">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-235">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-236">Parameters</span></span>

<span data-ttu-id="37a61-237">値</span><span class="sxs-lookup"><span data-stu-id="37a61-237">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-238">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-238">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="37a61-239">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="37a61-239">Method parameters</span></span>

<span data-ttu-id="37a61-240">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-240">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-241">Parameters</span></span>

<span data-ttu-id="37a61-242">値</span><span class="sxs-lookup"><span data-stu-id="37a61-242">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-243">Return Value</span></span>

<span data-ttu-id="37a61-244">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="37a61-244">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-245">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-245">Remarks</span></span>

<span data-ttu-id="37a61-246">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="37a61-246">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="37a61-247">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="37a61-247">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="37a61-248">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-248">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-249">Parameters</span></span>

<span data-ttu-id="37a61-250">値</span><span class="sxs-lookup"><span data-stu-id="37a61-250">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-251">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-251">Return Value</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="37a61-252">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="37a61-252">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-253">Parameters</span></span>

<span data-ttu-id="37a61-254">値</span><span class="sxs-lookup"><span data-stu-id="37a61-254">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-255">Return Value</span></span>

### <a name="method-runon"></a><span data-ttu-id="37a61-256">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="37a61-256">Method runOn</span></span>

    public int runOn([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-257">Parameters</span></span>

<span data-ttu-id="37a61-258">値</span><span class="sxs-lookup"><span data-stu-id="37a61-258">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-259">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-259">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="37a61-260">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-260">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-261">Parameters</span></span>

<span data-ttu-id="37a61-262">値</span><span class="sxs-lookup"><span data-stu-id="37a61-262">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-263">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="37a61-264">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="37a61-264">Method viewUserLicense</span></span>

<span data-ttu-id="37a61-265">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-265">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-266">Parameters</span></span>

<span data-ttu-id="37a61-267">値</span><span class="sxs-lookup"><span data-stu-id="37a61-267">value</span></span>  
<span data-ttu-id="37a61-268">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-268">The user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="37a61-269">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-269">Return Value</span></span>

<span data-ttu-id="37a61-270">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-270">The user license.</span></span>

### <a name="method-runcalled"></a><span data-ttu-id="37a61-271">メソッド runCalled</span><span class="sxs-lookup"><span data-stu-id="37a61-271">Method runCalled</span></span>

    public static void runCalled(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="37a61-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-272">Parameters</span></span>

<span data-ttu-id="37a61-273">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-273">name</span></span>  

<!-- -->

<span data-ttu-id="37a61-274">args</span><span class="sxs-lookup"><span data-stu-id="37a61-274">args</span></span>  

### <a name="method-aotrun"></a><span data-ttu-id="37a61-275">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="37a61-275">Method AOTrun</span></span>

<span data-ttu-id="37a61-276">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="37a61-276">Compiles this node and its sub-tree in the Application Object Tree (AOT).</span></span>

    public void AOTrun([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="37a61-277">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-277">Parameters</span></span>

<span data-ttu-id="37a61-278">args</span><span class="sxs-lookup"><span data-stu-id="37a61-278">args</span></span>  

### <a name="method-runclient"></a><span data-ttu-id="37a61-279">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="37a61-279">Method runClient</span></span>

    public static void runClient(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="37a61-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-280">Parameters</span></span>

<span data-ttu-id="37a61-281">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-281">name</span></span>  

<!-- -->

<span data-ttu-id="37a61-282">args</span><span class="sxs-lookup"><span data-stu-id="37a61-282">args</span></span>  

### <a name="method-run"></a><span data-ttu-id="37a61-283">メソッド run</span><span class="sxs-lookup"><span data-stu-id="37a61-283">Method run</span></span>

    public void run([xArgs args])

#### <a name="parameters"></a><span data-ttu-id="37a61-284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-284">Parameters</span></span>

<span data-ttu-id="37a61-285">args</span><span class="sxs-lookup"><span data-stu-id="37a61-285">args</span></span>  

### <a name="method-new"></a><span data-ttu-id="37a61-286">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-286">Method new</span></span>

<span data-ttu-id="37a61-287">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-287">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-288">Parameters</span></span>

<span data-ttu-id="37a61-289">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-289">name</span></span>  

### <a name="method-runserver"></a><span data-ttu-id="37a61-290">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="37a61-290">Method runServer</span></span>

    public static void runServer(str name, [xArgs args])

#### <a name="parameters"></a><span data-ttu-id="37a61-291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-291">Parameters</span></span>

<span data-ttu-id="37a61-292">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-292">name</span></span>  

<!-- -->

<span data-ttu-id="37a61-293">args</span><span class="sxs-lookup"><span data-stu-id="37a61-293">args</span></span>  

## <a name="class-webcontentitem"></a><span data-ttu-id="37a61-294">クラス WebContentItem</span><span class="sxs-lookup"><span data-stu-id="37a61-294">Class WebContentItem</span></span>
    class WebContentItem extends SecureNode

<span data-ttu-id="37a61-295">WebContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-295">The WebContentItem class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-296">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-296">Remarks</span></span>

<span data-ttu-id="37a61-297">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-297">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-298">例</span><span class="sxs-lookup"><span data-stu-id="37a61-298">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-299">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-299">Methods</span></span>

| <span data-ttu-id="37a61-300">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-300">Method</span></span>                                            | <span data-ttu-id="37a61-301">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-301">Description</span></span>                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-302">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-302">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="37a61-303">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-303">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="37a61-304">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-304">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="37a61-305">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-305">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-306">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-306">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="37a61-307">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-307">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-308">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-308">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="37a61-309">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-309">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="37a61-310">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-310">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="37a61-311">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-311">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="37a61-312">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-312">public str creationTime(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="37a61-313">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-313">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="37a61-314">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-314">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                               |
| <span data-ttu-id="37a61-315">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-315">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="37a61-316">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-316">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                   |
| <span data-ttu-id="37a61-317">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-317">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="37a61-318">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-318">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="37a61-319">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-319">public str label(\[str value\])</span></span>                   | <span data-ttu-id="37a61-320">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-320">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="37a61-321">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-321">public str name(\[str value\])</span></span>                    | <span data-ttu-id="37a61-322">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-322">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-323">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-323">public str object(\[str value\])</span></span>                  | <span data-ttu-id="37a61-324">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-324">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                 |
| <span data-ttu-id="37a61-325">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-325">public int objectType(\[int value\])</span></span>              |                                                                                                                                           |
| <span data-ttu-id="37a61-326">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-326">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="37a61-327">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-327">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="37a61-328">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-328">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="37a61-329">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-329">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                           |

### <a name="method-changedby"></a><span data-ttu-id="37a61-330">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-330">Method changedBy</span></span>

<span data-ttu-id="37a61-331">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-331">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-332">Parameters</span></span>

<span data-ttu-id="37a61-333">値</span><span class="sxs-lookup"><span data-stu-id="37a61-333">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-334">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-334">Return Value</span></span>

<span data-ttu-id="37a61-335">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-335">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-336">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-336">Method changedDate</span></span>

<span data-ttu-id="37a61-337">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-337">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-338">Parameters</span></span>

<span data-ttu-id="37a61-339">値</span><span class="sxs-lookup"><span data-stu-id="37a61-339">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-340">Return Value</span></span>

<span data-ttu-id="37a61-341">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-341">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-342">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-342">Method changedTime</span></span>

<span data-ttu-id="37a61-343">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-343">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-344">Parameters</span></span>

<span data-ttu-id="37a61-345">値</span><span class="sxs-lookup"><span data-stu-id="37a61-345">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-346">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-346">Return Value</span></span>

<span data-ttu-id="37a61-347">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-347">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-348">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-348">Method createdBy</span></span>

<span data-ttu-id="37a61-349">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-349">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-350">Parameters</span></span>

<span data-ttu-id="37a61-351">値</span><span class="sxs-lookup"><span data-stu-id="37a61-351">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-352">Return Value</span></span>

<span data-ttu-id="37a61-353">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-353">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-354">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-354">Method creationDate</span></span>

<span data-ttu-id="37a61-355">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-355">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-356">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-356">Parameters</span></span>

<span data-ttu-id="37a61-357">値</span><span class="sxs-lookup"><span data-stu-id="37a61-357">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-358">Return Value</span></span>

<span data-ttu-id="37a61-359">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-359">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-360">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-360">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-361">Parameters</span></span>

<span data-ttu-id="37a61-362">値</span><span class="sxs-lookup"><span data-stu-id="37a61-362">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-363">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="37a61-364">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="37a61-364">Method enumParameter</span></span>

<span data-ttu-id="37a61-365">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-365">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-366">Parameters</span></span>

<span data-ttu-id="37a61-367">値</span><span class="sxs-lookup"><span data-stu-id="37a61-367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-368">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-368">Return Value</span></span>

<span data-ttu-id="37a61-369">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="37a61-369">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="37a61-370">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="37a61-370">Method enumTypeParameter</span></span>

<span data-ttu-id="37a61-371">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-371">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="37a61-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-372">Parameters</span></span>

<span data-ttu-id="37a61-373">値</span><span class="sxs-lookup"><span data-stu-id="37a61-373">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-374">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-374">Return Value</span></span>

<span data-ttu-id="37a61-375">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="37a61-375">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="37a61-376">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="37a61-376">Method helpText</span></span>

<span data-ttu-id="37a61-377">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-377">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-378">Parameters</span></span>

<span data-ttu-id="37a61-379">値</span><span class="sxs-lookup"><span data-stu-id="37a61-379">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-380">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-380">Return Value</span></span>

<span data-ttu-id="37a61-381">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="37a61-381">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-382">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-382">Remarks</span></span>

<span data-ttu-id="37a61-383">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-383">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="37a61-384">ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="37a61-384">dialog box.</span></span> <span data-ttu-id="37a61-385">ヘルプ テキストは、250文字以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-385">The The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="37a61-386">メソッド label</span><span class="sxs-lookup"><span data-stu-id="37a61-386">Method label</span></span>

<span data-ttu-id="37a61-387">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-387">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-388">Parameters</span></span>

<span data-ttu-id="37a61-389">値</span><span class="sxs-lookup"><span data-stu-id="37a61-389">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-390">Return Value</span></span>

<span data-ttu-id="37a61-391">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="37a61-391">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-392">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-392">Remarks</span></span>

<span data-ttu-id="37a61-393">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-393">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="37a61-394">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-394">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-395">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-395">Method name</span></span>

<span data-ttu-id="37a61-396">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-396">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-397">Parameters</span></span>

<span data-ttu-id="37a61-398">値</span><span class="sxs-lookup"><span data-stu-id="37a61-398">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-399">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-399">Return Value</span></span>

<span data-ttu-id="37a61-400">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-400">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-401">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-401">Remarks</span></span>

<span data-ttu-id="37a61-402">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-402">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-403">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-403">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-404">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-404">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-405">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-405">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-406">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-406">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-407">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-407">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-object"></a><span data-ttu-id="37a61-408">メソッド object</span><span class="sxs-lookup"><span data-stu-id="37a61-408">Method object</span></span>

<span data-ttu-id="37a61-409">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-409">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-410">Parameters</span></span>

<span data-ttu-id="37a61-411">値</span><span class="sxs-lookup"><span data-stu-id="37a61-411">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-412">Return Value</span></span>

<span data-ttu-id="37a61-413">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="37a61-413">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-414">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-414">Remarks</span></span>

<span data-ttu-id="37a61-415">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-415">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="37a61-416">フォーム</span><span class="sxs-lookup"><span data-stu-id="37a61-416">Form</span></span>
-   <span data-ttu-id="37a61-417">レポート </span><span class="sxs-lookup"><span data-stu-id="37a61-417">Report</span></span>
-   <span data-ttu-id="37a61-418">ジョブ</span><span class="sxs-lookup"><span data-stu-id="37a61-418">Job</span></span>
-   <span data-ttu-id="37a61-419">クラス</span><span class="sxs-lookup"><span data-stu-id="37a61-419">Class</span></span>
-   <span data-ttu-id="37a61-420">クエリ</span><span class="sxs-lookup"><span data-stu-id="37a61-420">Query</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="37a61-421">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="37a61-421">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-422">Parameters</span></span>

<span data-ttu-id="37a61-423">値</span><span class="sxs-lookup"><span data-stu-id="37a61-423">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-424">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-425">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-425">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-426">Parameters</span></span>

<span data-ttu-id="37a61-427">値</span><span class="sxs-lookup"><span data-stu-id="37a61-427">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-428">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-428">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="37a61-429">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="37a61-429">Method parameters</span></span>

<span data-ttu-id="37a61-430">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-430">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-431">Parameters</span></span>

<span data-ttu-id="37a61-432">値</span><span class="sxs-lookup"><span data-stu-id="37a61-432">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-433">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-433">Return Value</span></span>

<span data-ttu-id="37a61-434">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="37a61-434">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-435">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-435">Remarks</span></span>

<span data-ttu-id="37a61-436">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="37a61-436">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="37a61-437">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="37a61-437">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="37a61-438">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="37a61-438">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-439">Parameters</span></span>

<span data-ttu-id="37a61-440">値</span><span class="sxs-lookup"><span data-stu-id="37a61-440">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-441">Return Value</span></span>

## <a name="class-webcontrolnode"></a><span data-ttu-id="37a61-442">クラス webControlNode</span><span class="sxs-lookup"><span data-stu-id="37a61-442">Class webControlNode</span></span>
    class webControlNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="37a61-443">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-443">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-444">例</span><span class="sxs-lookup"><span data-stu-id="37a61-444">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-445">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-445">Methods</span></span>

| <span data-ttu-id="37a61-446">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-446">Method</span></span>                                                        | <span data-ttu-id="37a61-447">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-447">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-448">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="37a61-448">public str AOTgetSource()</span></span>                                     | <span data-ttu-id="37a61-449">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="37a61-449">Returns the source code of this node.</span></span>                                                                                                         |
| <span data-ttu-id="37a61-450">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-450">public str changedBy(\[str value\])</span></span>                           | <span data-ttu-id="37a61-451">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-451">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="37a61-452">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-452">public Date changedDate(\[Date value\])</span></span>                       | <span data-ttu-id="37a61-453">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-453">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-454">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-454">public str changedTime(\[str value\])</span></span>                         | <span data-ttu-id="37a61-455">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-455">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-456">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-456">public str createdBy(\[str value\])</span></span>                           | <span data-ttu-id="37a61-457">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-457">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="37a61-458">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-458">public Date creationDate(\[Date value\])</span></span>                      | <span data-ttu-id="37a61-459">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-459">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="37a61-460">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-460">public str creationTime(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="37a61-461">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-461">public str filename(\[str value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="37a61-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span><span class="sxs-lookup"><span data-stu-id="37a61-462">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span></span> | <span data-ttu-id="37a61-463">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="37a61-463">Get a list of web controls that are related to this web control.</span></span>                                                                              |
| <span data-ttu-id="37a61-464">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-464">public str helpText(\[str value\])</span></span>                            | <span data-ttu-id="37a61-465">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-465">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="37a61-466">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-466">public str name(\[str value\])</span></span>                                | <span data-ttu-id="37a61-467">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-467">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-468">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-468">public Guid origin(\[Guid value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="37a61-469">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-469">public str relativePath(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="37a61-470">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-470">public str version(\[str value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="37a61-471">::public static webControlNode createFromFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="37a61-471">::public static webControlNode createFromFile(str fileName)</span></span>   |                                                                                                                                               |
| <span data-ttu-id="37a61-472">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="37a61-472">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>    | <span data-ttu-id="37a61-473">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-473">Sets the source code of this node.</span></span>                                                                                                            |

### <a name="method-aotgetsource"></a><span data-ttu-id="37a61-474">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-474">Method AOTgetSource</span></span>

<span data-ttu-id="37a61-475">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="37a61-475">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="37a61-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-476">Return Value</span></span>

<span data-ttu-id="37a61-477">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="37a61-477">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-478">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-478">Remarks</span></span>

<span data-ttu-id="37a61-479">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-479">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="37a61-480">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-480">Method changedBy</span></span>

<span data-ttu-id="37a61-481">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-481">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-482">Parameters</span></span>

<span data-ttu-id="37a61-483">値</span><span class="sxs-lookup"><span data-stu-id="37a61-483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-484">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-484">Return Value</span></span>

<span data-ttu-id="37a61-485">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-485">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-486">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-486">Method changedDate</span></span>

<span data-ttu-id="37a61-487">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-487">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-488">Parameters</span></span>

<span data-ttu-id="37a61-489">値</span><span class="sxs-lookup"><span data-stu-id="37a61-489">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-490">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-490">Return Value</span></span>

<span data-ttu-id="37a61-491">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-491">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-492">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-492">Method changedTime</span></span>

<span data-ttu-id="37a61-493">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-493">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-494">Parameters</span></span>

<span data-ttu-id="37a61-495">値</span><span class="sxs-lookup"><span data-stu-id="37a61-495">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-496">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-496">Return Value</span></span>

<span data-ttu-id="37a61-497">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-497">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-498">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-498">Method createdBy</span></span>

<span data-ttu-id="37a61-499">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-499">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-500">Parameters</span></span>

<span data-ttu-id="37a61-501">値</span><span class="sxs-lookup"><span data-stu-id="37a61-501">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-502">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-502">Return Value</span></span>

<span data-ttu-id="37a61-503">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-503">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-504">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-504">Method creationDate</span></span>

<span data-ttu-id="37a61-505">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-505">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-506">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-506">Parameters</span></span>

<span data-ttu-id="37a61-507">値</span><span class="sxs-lookup"><span data-stu-id="37a61-507">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-508">Return Value</span></span>

<span data-ttu-id="37a61-509">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-509">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-510">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-510">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-511">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-511">Parameters</span></span>

<span data-ttu-id="37a61-512">値</span><span class="sxs-lookup"><span data-stu-id="37a61-512">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-513">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="37a61-514">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="37a61-514">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-515">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-515">Parameters</span></span>

<span data-ttu-id="37a61-516">値</span><span class="sxs-lookup"><span data-stu-id="37a61-516">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-517">Return Value</span></span>

### <a name="method-getrelatedwebcontrols"></a><span data-ttu-id="37a61-518">メソッド getRelatedWebControls</span><span class="sxs-lookup"><span data-stu-id="37a61-518">Method getRelatedWebControls</span></span>

<span data-ttu-id="37a61-519">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="37a61-519">Get a list of web controls that are related to this web control.</span></span>

    public List getRelatedWebControls([boolean firstLevelOnly])

#### <a name="parameters"></a><span data-ttu-id="37a61-520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-520">Parameters</span></span>

<span data-ttu-id="37a61-521">firstLevelOnly</span><span class="sxs-lookup"><span data-stu-id="37a61-521">firstLevelOnly</span></span>  
<span data-ttu-id="37a61-522">Web コントロールの最初のレベルのみがオンになっているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="37a61-522">A value that indicates whether only the first level of web controls is checked.</span></span>

#### <a name="return-value"></a><span data-ttu-id="37a61-523">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-523">Return Value</span></span>

<span data-ttu-id="37a61-524">関連する Web コントロールの一覧。</span><span class="sxs-lookup"><span data-stu-id="37a61-524">A list of related web controls.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="37a61-525">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="37a61-525">Method helpText</span></span>

<span data-ttu-id="37a61-526">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-526">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-527">Parameters</span></span>

<span data-ttu-id="37a61-528">値</span><span class="sxs-lookup"><span data-stu-id="37a61-528">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-529">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-529">Return Value</span></span>

<span data-ttu-id="37a61-530">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="37a61-530">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-531">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-531">Remarks</span></span>

<span data-ttu-id="37a61-532">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-532">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="37a61-533">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="37a61-533">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-534">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-534">Method name</span></span>

<span data-ttu-id="37a61-535">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-535">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-536">Parameters</span></span>

<span data-ttu-id="37a61-537">値</span><span class="sxs-lookup"><span data-stu-id="37a61-537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-538">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-538">Return Value</span></span>

<span data-ttu-id="37a61-539">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-539">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-540">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-540">Remarks</span></span>

<span data-ttu-id="37a61-541">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-541">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-542">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-542">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-543">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-543">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-544">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-544">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-545">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-545">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-546">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-546">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-547">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-547">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-548">Parameters</span></span>

<span data-ttu-id="37a61-549">値</span><span class="sxs-lookup"><span data-stu-id="37a61-549">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-550">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-550">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="37a61-551">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="37a61-551">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-552">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-552">Parameters</span></span>

<span data-ttu-id="37a61-553">値</span><span class="sxs-lookup"><span data-stu-id="37a61-553">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-554">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-554">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="37a61-555">メソッド version</span><span class="sxs-lookup"><span data-stu-id="37a61-555">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-556">Parameters</span></span>

<span data-ttu-id="37a61-557">値</span><span class="sxs-lookup"><span data-stu-id="37a61-557">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-558">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-558">Return Value</span></span>

### <a name="method-createfromfile"></a><span data-ttu-id="37a61-559">メソッド createFromFile</span><span class="sxs-lookup"><span data-stu-id="37a61-559">Method createFromFile</span></span>

    public static webControlNode createFromFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="37a61-560">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-560">Parameters</span></span>

<span data-ttu-id="37a61-561">fileName</span><span class="sxs-lookup"><span data-stu-id="37a61-561">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-562">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-562">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="37a61-563">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-563">Method AOTsetSource</span></span>

<span data-ttu-id="37a61-564">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-564">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="37a61-565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-565">Parameters</span></span>

<span data-ttu-id="37a61-566">ソース</span><span class="sxs-lookup"><span data-stu-id="37a61-566">source</span></span>  
<span data-ttu-id="37a61-567">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="37a61-567">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="37a61-568">isStatic</span><span class="sxs-lookup"><span data-stu-id="37a61-568">isStatic</span></span>  
<span data-ttu-id="37a61-569">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="37a61-569">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-570">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-570">Remarks</span></span>

<span data-ttu-id="37a61-571">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-571">This method is overridden by nodes that have source code.</span></span>

## <a name="class-webdisplaycontentitem"></a><span data-ttu-id="37a61-572">クラス WebDisplayContentItem</span><span class="sxs-lookup"><span data-stu-id="37a61-572">Class WebDisplayContentItem</span></span>
    class WebDisplayContentItem extends WebContentItem

<span data-ttu-id="37a61-573">WebDisplayContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-573">The WebDisplayContentItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-574">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-574">Remarks</span></span>

<span data-ttu-id="37a61-575">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-575">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="37a61-576">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-576">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-577">例</span><span class="sxs-lookup"><span data-stu-id="37a61-577">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-578">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-578">Methods</span></span>

| <span data-ttu-id="37a61-579">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-579">Method</span></span>                    | <span data-ttu-id="37a61-580">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-580">Description</span></span>                          |
|---------------------------|--------------------------------------|
| <span data-ttu-id="37a61-581">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-581">public void new(str name)</span></span> | <span data-ttu-id="37a61-582">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="37a61-582">Creates a new WebDisplayContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="37a61-583">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-583">Method new</span></span>

<span data-ttu-id="37a61-584">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="37a61-584">Creates a new WebDisplayContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-585">Parameters</span></span>

<span data-ttu-id="37a61-586">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-586">name</span></span>  

## <a name="class-webletitem"></a><span data-ttu-id="37a61-587">クラス WebletItem</span><span class="sxs-lookup"><span data-stu-id="37a61-587">Class WebletItem</span></span>
    class WebletItem extends SecureNode

<span data-ttu-id="37a61-588">WebletItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-588">The WebletItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-589">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-589">Remarks</span></span>

<span data-ttu-id="37a61-590">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-590">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="37a61-591">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-591">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-592">例</span><span class="sxs-lookup"><span data-stu-id="37a61-592">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-593">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-593">Methods</span></span>

| <span data-ttu-id="37a61-594">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-594">Method</span></span>                                            | <span data-ttu-id="37a61-595">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-595">Description</span></span>                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-596">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-596">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="37a61-597">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-597">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="37a61-598">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-598">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="37a61-599">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-599">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-600">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-600">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="37a61-601">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-601">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-602">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-602">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="37a61-603">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-603">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="37a61-604">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-604">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="37a61-605">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-605">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="37a61-606">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-606">public str creationTime(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="37a61-607">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-607">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="37a61-608">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-608">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                                   |
| <span data-ttu-id="37a61-609">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-609">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="37a61-610">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-610">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="37a61-611">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-611">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="37a61-612">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-612">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="37a61-613">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-613">public str label(\[str value\])</span></span>                   | <span data-ttu-id="37a61-614">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-614">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="37a61-615">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-615">public str name(\[str value\])</span></span>                    | <span data-ttu-id="37a61-616">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-616">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-617">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-617">public str object(\[str value\])</span></span>                  | <span data-ttu-id="37a61-618">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-618">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                     |
| <span data-ttu-id="37a61-619">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-619">public int objectType(\[int value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="37a61-620">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-620">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="37a61-621">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-621">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="37a61-622">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-622">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                        |
| <span data-ttu-id="37a61-623">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-623">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="37a61-624">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-624">public void new(str name)</span></span>                         | <span data-ttu-id="37a61-625">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-625">Microsoft internal use only.</span></span>                                                                                                                  |

### <a name="method-changedby"></a><span data-ttu-id="37a61-626">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-626">Method changedBy</span></span>

<span data-ttu-id="37a61-627">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-627">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-628">Parameters</span></span>

<span data-ttu-id="37a61-629">値</span><span class="sxs-lookup"><span data-stu-id="37a61-629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-630">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-630">Return Value</span></span>

<span data-ttu-id="37a61-631">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-631">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-632">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-632">Method changedDate</span></span>

<span data-ttu-id="37a61-633">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-633">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-634">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-634">Parameters</span></span>

<span data-ttu-id="37a61-635">値</span><span class="sxs-lookup"><span data-stu-id="37a61-635">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-636">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-636">Return Value</span></span>

<span data-ttu-id="37a61-637">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-637">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-638">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-638">Method changedTime</span></span>

<span data-ttu-id="37a61-639">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-639">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-640">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-640">Parameters</span></span>

<span data-ttu-id="37a61-641">値</span><span class="sxs-lookup"><span data-stu-id="37a61-641">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-642">Return Value</span></span>

<span data-ttu-id="37a61-643">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-643">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-644">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-644">Method createdBy</span></span>

<span data-ttu-id="37a61-645">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-645">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-646">Parameters</span></span>

<span data-ttu-id="37a61-647">値</span><span class="sxs-lookup"><span data-stu-id="37a61-647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-648">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-648">Return Value</span></span>

<span data-ttu-id="37a61-649">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-649">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-650">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-650">Method creationDate</span></span>

<span data-ttu-id="37a61-651">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-651">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-652">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-652">Parameters</span></span>

<span data-ttu-id="37a61-653">値</span><span class="sxs-lookup"><span data-stu-id="37a61-653">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-654">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-654">Return Value</span></span>

<span data-ttu-id="37a61-655">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-655">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-656">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-656">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-657">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-657">Parameters</span></span>

<span data-ttu-id="37a61-658">値</span><span class="sxs-lookup"><span data-stu-id="37a61-658">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-659">Return Value</span></span>

### <a name="method-enumparameter"></a><span data-ttu-id="37a61-660">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="37a61-660">Method enumParameter</span></span>

<span data-ttu-id="37a61-661">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-661">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-662">Parameters</span></span>

<span data-ttu-id="37a61-663">値</span><span class="sxs-lookup"><span data-stu-id="37a61-663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-664">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-664">Return Value</span></span>

<span data-ttu-id="37a61-665">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="37a61-665">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="37a61-666">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="37a61-666">Method enumTypeParameter</span></span>

<span data-ttu-id="37a61-667">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-667">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="37a61-668">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-668">Parameters</span></span>

<span data-ttu-id="37a61-669">値</span><span class="sxs-lookup"><span data-stu-id="37a61-669">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-670">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-670">Return Value</span></span>

<span data-ttu-id="37a61-671">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="37a61-671">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="37a61-672">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="37a61-672">Method helpText</span></span>

<span data-ttu-id="37a61-673">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-673">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-674">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-674">Parameters</span></span>

<span data-ttu-id="37a61-675">値</span><span class="sxs-lookup"><span data-stu-id="37a61-675">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-676">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-676">Return Value</span></span>

<span data-ttu-id="37a61-677">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="37a61-677">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-678">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-678">Remarks</span></span>

<span data-ttu-id="37a61-679">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-679">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="37a61-680">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="37a61-680">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="37a61-681">メソッド label</span><span class="sxs-lookup"><span data-stu-id="37a61-681">Method label</span></span>

<span data-ttu-id="37a61-682">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-682">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-683">Parameters</span></span>

<span data-ttu-id="37a61-684">値</span><span class="sxs-lookup"><span data-stu-id="37a61-684">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-685">Return Value</span></span>

<span data-ttu-id="37a61-686">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="37a61-686">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-687">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-687">Remarks</span></span>

<span data-ttu-id="37a61-688">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-688">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="37a61-689">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-689">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-690">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-690">Method name</span></span>

<span data-ttu-id="37a61-691">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-691">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-692">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-692">Parameters</span></span>

<span data-ttu-id="37a61-693">値</span><span class="sxs-lookup"><span data-stu-id="37a61-693">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-694">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-694">Return Value</span></span>

<span data-ttu-id="37a61-695">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-695">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-696">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-696">Remarks</span></span>

<span data-ttu-id="37a61-697">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-697">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-698">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-698">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-699">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-699">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-700">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-700">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-701">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-701">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-702">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-702">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

### <a name="method-object"></a><span data-ttu-id="37a61-703">メソッド object</span><span class="sxs-lookup"><span data-stu-id="37a61-703">Method object</span></span>

<span data-ttu-id="37a61-704">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-704">Gets or sets the object that the MenuFunction class runs.</span></span>

    public str object([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-705">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-705">Parameters</span></span>

<span data-ttu-id="37a61-706">値</span><span class="sxs-lookup"><span data-stu-id="37a61-706">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-707">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-707">Return Value</span></span>

<span data-ttu-id="37a61-708">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="37a61-708">The object that the MenuFunction class runs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-709">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-709">Remarks</span></span>

<span data-ttu-id="37a61-710">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-710">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="37a61-711">フォーム。</span><span class="sxs-lookup"><span data-stu-id="37a61-711">Form.</span></span>
-   <span data-ttu-id="37a61-712">レポート。</span><span class="sxs-lookup"><span data-stu-id="37a61-712">Report.</span></span>
-   <span data-ttu-id="37a61-713">ジョブ。</span><span class="sxs-lookup"><span data-stu-id="37a61-713">Job.</span></span>
-   <span data-ttu-id="37a61-714">クラス。</span><span class="sxs-lookup"><span data-stu-id="37a61-714">Class.</span></span>
-   <span data-ttu-id="37a61-715">クエリ。</span><span class="sxs-lookup"><span data-stu-id="37a61-715">Query.</span></span>

### <a name="method-objecttype"></a><span data-ttu-id="37a61-716">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="37a61-716">Method objectType</span></span>

    public int objectType([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-717">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-717">Parameters</span></span>

<span data-ttu-id="37a61-718">値</span><span class="sxs-lookup"><span data-stu-id="37a61-718">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-719">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-719">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-720">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-720">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-721">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-721">Parameters</span></span>

<span data-ttu-id="37a61-722">値</span><span class="sxs-lookup"><span data-stu-id="37a61-722">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-723">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-723">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="37a61-724">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="37a61-724">Method parameters</span></span>

<span data-ttu-id="37a61-725">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-725">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-726">Parameters</span></span>

<span data-ttu-id="37a61-727">値</span><span class="sxs-lookup"><span data-stu-id="37a61-727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-728">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-728">Return Value</span></span>

<span data-ttu-id="37a61-729">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="37a61-729">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-730">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-730">Remarks</span></span>

<span data-ttu-id="37a61-731">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="37a61-731">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="37a61-732">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="37a61-732">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-reportdesign"></a><span data-ttu-id="37a61-733">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="37a61-733">Method reportDesign</span></span>

    public str reportDesign([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-734">Parameters</span></span>

<span data-ttu-id="37a61-735">値</span><span class="sxs-lookup"><span data-stu-id="37a61-735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-736">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-736">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="37a61-737">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-737">Method new</span></span>

<span data-ttu-id="37a61-738">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-738">Microsoft internal use only.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-739">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-739">Parameters</span></span>

<span data-ttu-id="37a61-740">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-740">name</span></span>  

## <a name="class-weblistdefnode"></a><span data-ttu-id="37a61-741">クラス webListDefNode</span><span class="sxs-lookup"><span data-stu-id="37a61-741">Class webListDefNode</span></span>
    class webListDefNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="37a61-742">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-742">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-743">例</span><span class="sxs-lookup"><span data-stu-id="37a61-743">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-744">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-744">Methods</span></span>

| <span data-ttu-id="37a61-745">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-745">Method</span></span>                                                     | <span data-ttu-id="37a61-746">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-746">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-747">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="37a61-747">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="37a61-748">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="37a61-748">Returns the source code of this node.</span></span>                                                                                                     |
| <span data-ttu-id="37a61-749">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-749">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="37a61-750">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-750">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="37a61-751">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-751">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="37a61-752">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-752">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-753">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-753">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="37a61-754">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-754">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-755">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-755">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="37a61-756">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-756">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="37a61-757">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-757">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="37a61-758">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-758">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="37a61-759">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-759">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="37a61-760">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-760">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="37a61-761">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-761">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="37a61-762">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-762">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="37a61-763">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-763">public str name(\[str value\])</span></span>                             | <span data-ttu-id="37a61-764">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-764">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-765">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-765">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="37a61-766">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-766">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="37a61-767">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-767">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="37a61-768">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-768">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="37a61-769">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-769">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="37a61-770">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="37a61-770">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="37a61-771">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-771">Sets the source code of this node.</span></span>                                                                                                        |
| <span data-ttu-id="37a61-772">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-772">public void new(str name)</span></span>                                  | <span data-ttu-id="37a61-773">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-773">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |

### <a name="method-aotgetsource"></a><span data-ttu-id="37a61-774">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-774">Method AOTgetSource</span></span>

<span data-ttu-id="37a61-775">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="37a61-775">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="37a61-776">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-776">Return Value</span></span>

<span data-ttu-id="37a61-777">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="37a61-777">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-778">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-778">Remarks</span></span>

<span data-ttu-id="37a61-779">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-779">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="37a61-780">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-780">Method changedBy</span></span>

<span data-ttu-id="37a61-781">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-781">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-782">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-782">Parameters</span></span>

<span data-ttu-id="37a61-783">値</span><span class="sxs-lookup"><span data-stu-id="37a61-783">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-784">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-784">Return Value</span></span>

<span data-ttu-id="37a61-785">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-785">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-786">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-786">Method changedDate</span></span>

<span data-ttu-id="37a61-787">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-787">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-788">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-788">Parameters</span></span>

<span data-ttu-id="37a61-789">値</span><span class="sxs-lookup"><span data-stu-id="37a61-789">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-790">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-790">Return Value</span></span>

<span data-ttu-id="37a61-791">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-791">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-792">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-792">Method changedTime</span></span>

<span data-ttu-id="37a61-793">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-793">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-794">Parameters</span></span>

<span data-ttu-id="37a61-795">値</span><span class="sxs-lookup"><span data-stu-id="37a61-795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-796">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-796">Return Value</span></span>

<span data-ttu-id="37a61-797">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-797">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-798">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-798">Method createdBy</span></span>

<span data-ttu-id="37a61-799">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-799">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-800">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-800">Parameters</span></span>

<span data-ttu-id="37a61-801">値</span><span class="sxs-lookup"><span data-stu-id="37a61-801">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-802">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-802">Return Value</span></span>

<span data-ttu-id="37a61-803">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-803">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-804">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-804">Method creationDate</span></span>

<span data-ttu-id="37a61-805">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-805">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-806">Parameters</span></span>

<span data-ttu-id="37a61-807">値</span><span class="sxs-lookup"><span data-stu-id="37a61-807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-808">Return Value</span></span>

<span data-ttu-id="37a61-809">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-809">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-810">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-810">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-811">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-811">Parameters</span></span>

<span data-ttu-id="37a61-812">値</span><span class="sxs-lookup"><span data-stu-id="37a61-812">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-813">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-813">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="37a61-814">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="37a61-814">Method helpText</span></span>

<span data-ttu-id="37a61-815">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-815">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-816">Parameters</span></span>

<span data-ttu-id="37a61-817">値</span><span class="sxs-lookup"><span data-stu-id="37a61-817">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-818">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-818">Return Value</span></span>

<span data-ttu-id="37a61-819">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="37a61-819">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-820">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-820">Remarks</span></span>

<span data-ttu-id="37a61-821">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-821">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="37a61-822">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="37a61-822">The help text must not exceed 250 characters.</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="37a61-823">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="37a61-823">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-824">Parameters</span></span>

<span data-ttu-id="37a61-825">値</span><span class="sxs-lookup"><span data-stu-id="37a61-825">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-826">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-827">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-827">Method name</span></span>

<span data-ttu-id="37a61-828">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-828">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-829">Parameters</span></span>

<span data-ttu-id="37a61-830">値</span><span class="sxs-lookup"><span data-stu-id="37a61-830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-831">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-831">Return Value</span></span>

<span data-ttu-id="37a61-832">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-832">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-833">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-833">Remarks</span></span>

<span data-ttu-id="37a61-834">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-834">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-835">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-835">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-836">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-836">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-837">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-837">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-838">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-838">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-839">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-839">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-840">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-840">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-841">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-841">Parameters</span></span>

<span data-ttu-id="37a61-842">値</span><span class="sxs-lookup"><span data-stu-id="37a61-842">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-843">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-843">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="37a61-844">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="37a61-844">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-845">Parameters</span></span>

<span data-ttu-id="37a61-846">値</span><span class="sxs-lookup"><span data-stu-id="37a61-846">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-847">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="37a61-848">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="37a61-848">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-849">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-849">Parameters</span></span>

<span data-ttu-id="37a61-850">値</span><span class="sxs-lookup"><span data-stu-id="37a61-850">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-851">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="37a61-852">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="37a61-852">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-853">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-853">Parameters</span></span>

<span data-ttu-id="37a61-854">値</span><span class="sxs-lookup"><span data-stu-id="37a61-854">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-855">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="37a61-856">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="37a61-856">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-857">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-857">Parameters</span></span>

<span data-ttu-id="37a61-858">値</span><span class="sxs-lookup"><span data-stu-id="37a61-858">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-859">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="37a61-860">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-860">Method AOTsetSource</span></span>

<span data-ttu-id="37a61-861">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-861">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="37a61-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-862">Parameters</span></span>

<span data-ttu-id="37a61-863">ソース</span><span class="sxs-lookup"><span data-stu-id="37a61-863">source</span></span>  
<span data-ttu-id="37a61-864">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="37a61-864">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="37a61-865">isStatic</span><span class="sxs-lookup"><span data-stu-id="37a61-865">isStatic</span></span>  
<span data-ttu-id="37a61-866">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="37a61-866">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-867">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-867">Remarks</span></span>

<span data-ttu-id="37a61-868">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-868">This method is overridden by nodes that have source code.</span></span>

### <a name="method-new"></a><span data-ttu-id="37a61-869">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-869">Method new</span></span>

<span data-ttu-id="37a61-870">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-870">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-871">Parameters</span></span>

<span data-ttu-id="37a61-872">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-872">name</span></span>  

## <a name="class-webmanagedcontentitem"></a><span data-ttu-id="37a61-873">クラス WebManagedContentItem</span><span class="sxs-lookup"><span data-stu-id="37a61-873">Class WebManagedContentItem</span></span>
    class WebManagedContentItem extends WebContentItem

<span data-ttu-id="37a61-874">このクラスを使用して、コンテンツをページに追加するために EP で使用する webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="37a61-874">This class is used to create a webManagedContentItem to use in EP for adding content to pages.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-875">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-875">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-876">例</span><span class="sxs-lookup"><span data-stu-id="37a61-876">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-877">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-877">Methods</span></span>

| <span data-ttu-id="37a61-878">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-878">Method</span></span>                    | <span data-ttu-id="37a61-879">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-879">Description</span></span>                                                 |
|---------------------------|-------------------------------------------------------------|
| <span data-ttu-id="37a61-880">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-880">public void new(str name)</span></span> | <span data-ttu-id="37a61-881">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="37a61-881">Create a new webManagedContentItem with the passed in name.</span></span> |

### <a name="method-new"></a><span data-ttu-id="37a61-882">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-882">Method new</span></span>

<span data-ttu-id="37a61-883">渡された名前で新しい webManagedContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="37a61-883">Create a new webManagedContentItem with the passed in name.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-884">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-884">Parameters</span></span>

<span data-ttu-id="37a61-885">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-885">name</span></span>  
<span data-ttu-id="37a61-886">新しい webManagedContentItem に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="37a61-886">Name for the new webManagedContentItem.</span></span>

## <a name="class-webmenu"></a><span data-ttu-id="37a61-887">クラス WebMenu</span><span class="sxs-lookup"><span data-stu-id="37a61-887">Class WebMenu</span></span>
    class WebMenu extends TreeNode

<span data-ttu-id="37a61-888">WebMenu クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-888">The WebMenu class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-889">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-889">Remarks</span></span>

<span data-ttu-id="37a61-890">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-890">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-891">例</span><span class="sxs-lookup"><span data-stu-id="37a61-891">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-892">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-892">Methods</span></span>

| <span data-ttu-id="37a61-893">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-893">Method</span></span>                                                                   | <span data-ttu-id="37a61-894">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-894">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-895">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-895">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="37a61-896">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-896">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="37a61-897">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-897">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="37a61-898">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-898">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-899">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-899">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="37a61-900">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-900">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-901">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="37a61-902">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-902">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="37a61-903">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-903">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="37a61-904">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-904">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="37a61-905">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-905">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="37a61-906">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-906">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="37a61-907">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-907">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="37a61-908">public boolean highlightSelected(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-908">public boolean highlightSelected(\[boolean value\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="37a61-909">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-909">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="37a61-910">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-910">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="37a61-911">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-911">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="37a61-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-912">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                               |
| <span data-ttu-id="37a61-913">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="37a61-913">public str menuName()</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="37a61-914">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-914">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="37a61-915">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-915">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-916">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-916">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="37a61-917">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-917">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="37a61-918">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-918">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="37a61-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-919">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="37a61-920">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-920">public boolean setCompany(\[boolean value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="37a61-921">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-921">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="37a61-922">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-922">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="37a61-923">public void addSeparator()</span><span class="sxs-lookup"><span data-stu-id="37a61-923">public void addSeparator()</span></span>                                               |                                                                                                                                               |
| <span data-ttu-id="37a61-924">public void makeMenu(Object outputClass)</span><span class="sxs-lookup"><span data-stu-id="37a61-924">public void makeMenu(Object outputClass)</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="37a61-925">public void addSubmenu(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-925">public void addSubmenu(str name)</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="37a61-926">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="37a61-926">public void new(str Name)</span></span>                                                | <span data-ttu-id="37a61-927">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-927">Initializes a new instance of the TreeNode class.</span></span>                                                                                             |
| <span data-ttu-id="37a61-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="37a61-928">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="37a61-929">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-929">Method changedBy</span></span>

<span data-ttu-id="37a61-930">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-930">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-931">Parameters</span></span>

<span data-ttu-id="37a61-932">値</span><span class="sxs-lookup"><span data-stu-id="37a61-932">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-933">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-933">Return Value</span></span>

<span data-ttu-id="37a61-934">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-934">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-935">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-935">Method changedDate</span></span>

<span data-ttu-id="37a61-936">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-936">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-937">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-937">Parameters</span></span>

<span data-ttu-id="37a61-938">値</span><span class="sxs-lookup"><span data-stu-id="37a61-938">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-939">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-939">Return Value</span></span>

<span data-ttu-id="37a61-940">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-940">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-941">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-941">Method changedTime</span></span>

<span data-ttu-id="37a61-942">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-942">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-943">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-943">Parameters</span></span>

<span data-ttu-id="37a61-944">値</span><span class="sxs-lookup"><span data-stu-id="37a61-944">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-945">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-945">Return Value</span></span>

<span data-ttu-id="37a61-946">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-946">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="37a61-947">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="37a61-947">Method configurationKey</span></span>

<span data-ttu-id="37a61-948">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-948">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="37a61-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-949">Parameters</span></span>

<span data-ttu-id="37a61-950">値</span><span class="sxs-lookup"><span data-stu-id="37a61-950">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-951">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-951">Return Value</span></span>

<span data-ttu-id="37a61-952">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="37a61-952">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-953">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-953">Remarks</span></span>

<span data-ttu-id="37a61-954">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="37a61-954">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="37a61-955">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="37a61-955">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-956">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-956">Method createdBy</span></span>

<span data-ttu-id="37a61-957">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-957">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-958">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-958">Parameters</span></span>

<span data-ttu-id="37a61-959">値</span><span class="sxs-lookup"><span data-stu-id="37a61-959">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-960">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-960">Return Value</span></span>

<span data-ttu-id="37a61-961">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-961">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-962">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-962">Method creationDate</span></span>

<span data-ttu-id="37a61-963">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-963">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-964">Parameters</span></span>

<span data-ttu-id="37a61-965">値</span><span class="sxs-lookup"><span data-stu-id="37a61-965">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-966">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-966">Return Value</span></span>

<span data-ttu-id="37a61-967">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-967">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-968">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-968">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-969">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-969">Parameters</span></span>

<span data-ttu-id="37a61-970">値</span><span class="sxs-lookup"><span data-stu-id="37a61-970">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-971">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-971">Return Value</span></span>

### <a name="method-highlightselected"></a><span data-ttu-id="37a61-972">メソッド highlightSelected</span><span class="sxs-lookup"><span data-stu-id="37a61-972">Method highlightSelected</span></span>

    public boolean highlightSelected([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-973">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-973">Parameters</span></span>

<span data-ttu-id="37a61-974">値</span><span class="sxs-lookup"><span data-stu-id="37a61-974">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-975">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="37a61-976">メソッド label</span><span class="sxs-lookup"><span data-stu-id="37a61-976">Method label</span></span>

<span data-ttu-id="37a61-977">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-977">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-978">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-978">Parameters</span></span>

<span data-ttu-id="37a61-979">値</span><span class="sxs-lookup"><span data-stu-id="37a61-979">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-980">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-980">Return Value</span></span>

<span data-ttu-id="37a61-981">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="37a61-981">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-982">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-982">Remarks</span></span>

<span data-ttu-id="37a61-983">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-983">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="37a61-984">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-984">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="37a61-985">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="37a61-985">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-986">Parameters</span></span>

<span data-ttu-id="37a61-987">値</span><span class="sxs-lookup"><span data-stu-id="37a61-987">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-988">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-988">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="37a61-989">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="37a61-989">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="37a61-990">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-990">Parameters</span></span>

<span data-ttu-id="37a61-991">値</span><span class="sxs-lookup"><span data-stu-id="37a61-991">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-992">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-992">Return Value</span></span>

### <a name="method-menuname"></a><span data-ttu-id="37a61-993">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="37a61-993">Method menuName</span></span>

    public str menuName()

#### <a name="return-value"></a><span data-ttu-id="37a61-994">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-994">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-995">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-995">Method name</span></span>

<span data-ttu-id="37a61-996">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-996">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-997">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-997">Parameters</span></span>

<span data-ttu-id="37a61-998">値</span><span class="sxs-lookup"><span data-stu-id="37a61-998">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-999">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-999">Return Value</span></span>

<span data-ttu-id="37a61-1000">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1000">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1001">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1001">Remarks</span></span>

<span data-ttu-id="37a61-1002">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1002">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-1003">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1003">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-1004">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-1004">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-1005">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1005">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-1006">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1006">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-1007">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1007">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="37a61-1008">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="37a61-1008">Method neededAccessLevel</span></span>

<span data-ttu-id="37a61-1009">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1009">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1010">Parameters</span></span>

<span data-ttu-id="37a61-1011">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1011">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1012">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1012">Return Value</span></span>

<span data-ttu-id="37a61-1013">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="37a61-1013">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1014">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1014">Remarks</span></span>

<span data-ttu-id="37a61-1015">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="37a61-1015">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="37a61-1016">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="37a61-1016">AccessType::NoAccess</span></span>
-   <span data-ttu-id="37a61-1017">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="37a61-1017">AccessType::View</span></span>
-   <span data-ttu-id="37a61-1018">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="37a61-1018">AccessType::Edit</span></span>
-   <span data-ttu-id="37a61-1019">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="37a61-1019">AccessType::Add</span></span>
-   <span data-ttu-id="37a61-1020">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="37a61-1020">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-1021">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-1021">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1022">Parameters</span></span>

<span data-ttu-id="37a61-1023">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1023">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1024">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1024">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="37a61-1025">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="37a61-1025">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1026">Parameters</span></span>

<span data-ttu-id="37a61-1027">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1027">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1028">Return Value</span></span>

### <a name="method-setcompany"></a><span data-ttu-id="37a61-1029">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="37a61-1029">Method setCompany</span></span>

    public boolean setCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1030">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1030">Parameters</span></span>

<span data-ttu-id="37a61-1031">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1031">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1032">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="37a61-1033">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="37a61-1033">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1034">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1034">Parameters</span></span>

<span data-ttu-id="37a61-1035">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1035">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1036">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1036">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="37a61-1037">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="37a61-1037">Method webTarget</span></span>

    public str webTarget([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1038">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1038">Parameters</span></span>

<span data-ttu-id="37a61-1039">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1039">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1040">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1040">Return Value</span></span>

### <a name="method-addseparator"></a><span data-ttu-id="37a61-1041">メソッド addSeparator</span><span class="sxs-lookup"><span data-stu-id="37a61-1041">Method addSeparator</span></span>

    public void addSeparator()

### <a name="method-makemenu"></a><span data-ttu-id="37a61-1042">メソッド makeMenu</span><span class="sxs-lookup"><span data-stu-id="37a61-1042">Method makeMenu</span></span>

    public void makeMenu(Object outputClass)

#### <a name="parameters"></a><span data-ttu-id="37a61-1043">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1043">Parameters</span></span>

<span data-ttu-id="37a61-1044">outputClass</span><span class="sxs-lookup"><span data-stu-id="37a61-1044">outputClass</span></span>  

### <a name="method-addsubmenu"></a><span data-ttu-id="37a61-1045">メソッド addSubmenu</span><span class="sxs-lookup"><span data-stu-id="37a61-1045">Method addSubmenu</span></span>

    public void addSubmenu(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-1046">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1046">Parameters</span></span>

<span data-ttu-id="37a61-1047">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-1047">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="37a61-1048">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-1048">Method new</span></span>

<span data-ttu-id="37a61-1049">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1049">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="37a61-1050">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1050">Parameters</span></span>

<span data-ttu-id="37a61-1051">氏名</span><span class="sxs-lookup"><span data-stu-id="37a61-1051">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="37a61-1052">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="37a61-1052">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="37a61-1053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1053">Parameters</span></span>

<span data-ttu-id="37a61-1054">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="37a61-1054">webMenuFunction</span></span>  

## <a name="class-webmenufunction"></a><span data-ttu-id="37a61-1055">クラス WebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="37a61-1055">Class WebMenuFunction</span></span>
    class WebMenuFunction extends SecureNode

<span data-ttu-id="37a61-1056">WebMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1056">The WebMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-1057">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1057">Remarks</span></span>

<span data-ttu-id="37a61-1058">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1058">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1059">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1059">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1060">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-1060">Methods</span></span>

| <span data-ttu-id="37a61-1061">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1061">Method</span></span>                                                                                           | <span data-ttu-id="37a61-1062">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1062">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-1063">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1063">public str changedBy(\[str value\])</span></span>                                                              | <span data-ttu-id="37a61-1064">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1064">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="37a61-1065">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1065">public Date changedDate(\[Date value\])</span></span>                                                          | <span data-ttu-id="37a61-1066">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1066">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-1067">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1067">public str changedTime(\[str value\])</span></span>                                                            | <span data-ttu-id="37a61-1068">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1068">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="37a61-1069">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1069">public str createdBy(\[str value\])</span></span>                                                              | <span data-ttu-id="37a61-1070">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1070">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="37a61-1071">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1071">public Date creationDate(\[Date value\])</span></span>                                                         | <span data-ttu-id="37a61-1072">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1072">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="37a61-1073">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1073">public str creationTime(\[str value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="37a61-1074">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1074">public str helpText(\[str value\])</span></span>                                                               | <span data-ttu-id="37a61-1075">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1075">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="37a61-1076">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1076">public str label(\[str value\])</span></span>                                                                  | <span data-ttu-id="37a61-1077">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1077">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="37a61-1078">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1078">public str name(\[str value\])</span></span>                                                                   | <span data-ttu-id="37a61-1079">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1079">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-1080">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1080">public Guid origin(\[Guid value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="37a61-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span><span class="sxs-lookup"><span data-stu-id="37a61-1081">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span></span> |                                                                                                                                               |

### <a name="method-changedby"></a><span data-ttu-id="37a61-1082">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1082">Method changedBy</span></span>

<span data-ttu-id="37a61-1083">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1083">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1084">Parameters</span></span>

<span data-ttu-id="37a61-1085">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1085">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1086">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1086">Return Value</span></span>

<span data-ttu-id="37a61-1087">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1087">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-1088">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1088">Method changedDate</span></span>

<span data-ttu-id="37a61-1089">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1089">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1090">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1090">Parameters</span></span>

<span data-ttu-id="37a61-1091">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1091">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1092">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1092">Return Value</span></span>

<span data-ttu-id="37a61-1093">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1093">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-1094">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1094">Method changedTime</span></span>

<span data-ttu-id="37a61-1095">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1095">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1096">Parameters</span></span>

<span data-ttu-id="37a61-1097">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1097">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1098">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1098">Return Value</span></span>

<span data-ttu-id="37a61-1099">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-1099">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-1100">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1100">Method createdBy</span></span>

<span data-ttu-id="37a61-1101">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1101">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1102">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1102">Parameters</span></span>

<span data-ttu-id="37a61-1103">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1103">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1104">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1104">Return Value</span></span>

<span data-ttu-id="37a61-1105">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1105">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-1106">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1106">Method creationDate</span></span>

<span data-ttu-id="37a61-1107">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1107">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1108">Parameters</span></span>

<span data-ttu-id="37a61-1109">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1109">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1110">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1110">Return Value</span></span>

<span data-ttu-id="37a61-1111">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1111">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-1112">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1112">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1113">Parameters</span></span>

<span data-ttu-id="37a61-1114">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1114">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1115">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1115">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="37a61-1116">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="37a61-1116">Method helpText</span></span>

<span data-ttu-id="37a61-1117">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1117">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1118">Parameters</span></span>

<span data-ttu-id="37a61-1119">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1119">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1120">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1120">Return Value</span></span>

<span data-ttu-id="37a61-1121">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="37a61-1121">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1122">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1122">Remarks</span></span>

<span data-ttu-id="37a61-1123">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1123">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="37a61-1124">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1124">The help text must not exceed 250 characters.</span></span>

### <a name="method-label"></a><span data-ttu-id="37a61-1125">メソッド label</span><span class="sxs-lookup"><span data-stu-id="37a61-1125">Method label</span></span>

<span data-ttu-id="37a61-1126">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1126">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1127">Parameters</span></span>

<span data-ttu-id="37a61-1128">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1128">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1129">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1129">Return Value</span></span>

<span data-ttu-id="37a61-1130">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="37a61-1130">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1131">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1131">Remarks</span></span>

<span data-ttu-id="37a61-1132">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1132">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="37a61-1133">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1133">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-1134">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-1134">Method name</span></span>

<span data-ttu-id="37a61-1135">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1135">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1136">Parameters</span></span>

<span data-ttu-id="37a61-1137">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1137">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1138">Return Value</span></span>

<span data-ttu-id="37a61-1139">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1139">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1140">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1140">Remarks</span></span>

<span data-ttu-id="37a61-1141">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1141">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-1142">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1142">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-1143">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-1143">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-1144">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1144">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-1145">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1145">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-1146">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1146">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-1147">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-1147">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1148">Parameters</span></span>

<span data-ttu-id="37a61-1149">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1149">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1150">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1150">Return Value</span></span>

### <a name="method-createwebmenufunction"></a><span data-ttu-id="37a61-1151">メソッド createWebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="37a61-1151">Method createWebMenuFunction</span></span>

    public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)

#### <a name="parameters"></a><span data-ttu-id="37a61-1152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1152">Parameters</span></span>

<span data-ttu-id="37a61-1153">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-1153">name</span></span>  

<!-- -->

<span data-ttu-id="37a61-1154">webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="37a61-1154">webMenuItemType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1155">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1155">Return Value</span></span>

## <a name="class-webmenuitem"></a><span data-ttu-id="37a61-1156">クラス WebMenuItem</span><span class="sxs-lookup"><span data-stu-id="37a61-1156">Class WebMenuItem</span></span>
    class WebMenuItem extends TreeNode

<span data-ttu-id="37a61-1157">WebMenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1157">The WebMenuItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-1158">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1158">Remarks</span></span>

<span data-ttu-id="37a61-1159">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1159">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="37a61-1160">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1160">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1161">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1161">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1162">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-1162">Methods</span></span>

| <span data-ttu-id="37a61-1163">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1163">Method</span></span>                                                         | <span data-ttu-id="37a61-1164">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1164">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-1165">public str label()</span><span class="sxs-lookup"><span data-stu-id="37a61-1165">public str label()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="37a61-1166">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1166">public str menuItemName(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="37a61-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1167">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="37a61-1168">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1168">public str name(\[str value\])</span></span>                                 | <span data-ttu-id="37a61-1169">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1169">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-1170">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1170">public str parameters(\[str value\])</span></span>                           | <span data-ttu-id="37a61-1171">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1171">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="37a61-1172">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1172">public boolean showParentModule(\[boolean value\])</span></span>             |                                                                                                                                           |

### <a name="method-label"></a><span data-ttu-id="37a61-1173">メソッド label</span><span class="sxs-lookup"><span data-stu-id="37a61-1173">Method label</span></span>

    public str label()

#### <a name="return-value"></a><span data-ttu-id="37a61-1174">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1174">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="37a61-1175">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="37a61-1175">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1176">Parameters</span></span>

<span data-ttu-id="37a61-1177">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1177">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1178">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1178">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="37a61-1179">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="37a61-1179">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1180">Parameters</span></span>

<span data-ttu-id="37a61-1181">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1181">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1182">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1182">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-1183">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-1183">Method name</span></span>

<span data-ttu-id="37a61-1184">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1184">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1185">Parameters</span></span>

<span data-ttu-id="37a61-1186">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1186">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1187">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1187">Return Value</span></span>

<span data-ttu-id="37a61-1188">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1188">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1189">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1189">Remarks</span></span>

<span data-ttu-id="37a61-1190">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1190">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-1191">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1191">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-1192">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-1192">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-1193">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1193">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-1194">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1194">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-1195">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1195">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-parameters"></a><span data-ttu-id="37a61-1196">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="37a61-1196">Method parameters</span></span>

<span data-ttu-id="37a61-1197">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1197">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1198">Parameters</span></span>

<span data-ttu-id="37a61-1199">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1199">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1200">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1200">Return Value</span></span>

<span data-ttu-id="37a61-1201">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="37a61-1201">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1202">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1202">Remarks</span></span>

<span data-ttu-id="37a61-1203">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1203">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="37a61-1204">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1204">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="37a61-1205">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="37a61-1205">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1206">Parameters</span></span>

<span data-ttu-id="37a61-1207">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1207">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1208">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1208">Return Value</span></span>

## <a name="class-webmodulenode"></a><span data-ttu-id="37a61-1209">クラス webModuleNode</span><span class="sxs-lookup"><span data-stu-id="37a61-1209">Class webModuleNode</span></span>
    class webModuleNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="37a61-1210">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1210">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1211">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1211">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1212">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-1212">Methods</span></span>

| <span data-ttu-id="37a61-1213">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1213">Method</span></span>                                                                   | <span data-ttu-id="37a61-1214">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1214">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-1215">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1215">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="37a61-1216">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1216">Gets or sets the name of the user who last changed the application object.</span></span>                                                                     |
| <span data-ttu-id="37a61-1217">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1217">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="37a61-1218">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1218">Gets or sets the date an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="37a61-1219">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1219">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="37a61-1220">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1220">Gets or sets the time an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="37a61-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1221">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="37a61-1222">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1222">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                            |
| <span data-ttu-id="37a61-1223">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1223">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="37a61-1224">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1224">Gets or sets the name of the user who created the application object.</span></span>                                                                          |
| <span data-ttu-id="37a61-1225">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1225">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="37a61-1226">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1226">Gets or sets the date an application object was created.</span></span>                                                                                       |
| <span data-ttu-id="37a61-1227">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1227">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="37a61-1228">public boolean extendedDataSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1228">public boolean extendedDataSecurity(\[boolean value\])</span></span>                   |                                                                                                                                                |
| <span data-ttu-id="37a61-1229">public boolean inheritNavigation(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1229">public boolean inheritNavigation(\[boolean value\])</span></span>                      |                                                                                                                                                |
| <span data-ttu-id="37a61-1230">public boolean inheritPermissions(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1230">public boolean inheritPermissions(\[boolean value\])</span></span>                     |                                                                                                                                                |
| <span data-ttu-id="37a61-1231">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1231">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="37a61-1232">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1232">Gets or sets the label for a control.</span></span>                                                                                                          |
| <span data-ttu-id="37a61-1233">public str masterPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1233">public str masterPage(\[str value\])</span></span>                                     |                                                                                                                                                |
| <span data-ttu-id="37a61-1234">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1234">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="37a61-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1235">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                                |
| <span data-ttu-id="37a61-1236">public str moduleName()</span><span class="sxs-lookup"><span data-stu-id="37a61-1236">public str moduleName()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="37a61-1237">public str modulePath()</span><span class="sxs-lookup"><span data-stu-id="37a61-1237">public str modulePath()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="37a61-1238">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1238">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="37a61-1239">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1239">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-1240">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1240">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="37a61-1241">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1241">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                        |
| <span data-ttu-id="37a61-1242">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1242">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="37a61-1243">public boolean publicModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1243">public boolean publicModule(\[boolean value\])</span></span>                           |                                                                                                                                                |
| <span data-ttu-id="37a61-1244">public str quickLaunch(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1244">public str quickLaunch(\[str value\])</span></span>                                    |                                                                                                                                                |
| <span data-ttu-id="37a61-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1245">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                                |
| <span data-ttu-id="37a61-1246">public boolean showLink(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1246">public boolean showLink(\[boolean value\])</span></span>                               |                                                                                                                                                |
| <span data-ttu-id="37a61-1247">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1247">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                                |
| <span data-ttu-id="37a61-1248">public void addSubModule(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-1248">public void addSubModule(str name)</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="37a61-1249">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="37a61-1249">public void new(str Name)</span></span>                                                | <span data-ttu-id="37a61-1250">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1250">Initializes a new instance of the TreeNode class.</span></span>                                                                                              |
| <span data-ttu-id="37a61-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="37a61-1251">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                                |

### <a name="method-changedby"></a><span data-ttu-id="37a61-1252">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1252">Method changedBy</span></span>

<span data-ttu-id="37a61-1253">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1253">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1254">Parameters</span></span>

<span data-ttu-id="37a61-1255">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1255">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1256">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1256">Return Value</span></span>

<span data-ttu-id="37a61-1257">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1257">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-1258">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1258">Method changedDate</span></span>

<span data-ttu-id="37a61-1259">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1259">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1260">Parameters</span></span>

<span data-ttu-id="37a61-1261">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1261">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1262">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1262">Return Value</span></span>

<span data-ttu-id="37a61-1263">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1263">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-1264">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1264">Method changedTime</span></span>

<span data-ttu-id="37a61-1265">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1265">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1266">Parameters</span></span>

<span data-ttu-id="37a61-1267">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1267">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1268">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1268">Return Value</span></span>

<span data-ttu-id="37a61-1269">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-1269">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="37a61-1270">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="37a61-1270">Method configurationKey</span></span>

<span data-ttu-id="37a61-1271">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1271">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1272">Parameters</span></span>

<span data-ttu-id="37a61-1273">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1273">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1274">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1274">Return Value</span></span>

<span data-ttu-id="37a61-1275">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="37a61-1275">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1276">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1276">Remarks</span></span>

<span data-ttu-id="37a61-1277">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1277">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="37a61-1278">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1278">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-1279">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1279">Method createdBy</span></span>

<span data-ttu-id="37a61-1280">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1280">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1281">Parameters</span></span>

<span data-ttu-id="37a61-1282">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1282">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1283">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1283">Return Value</span></span>

<span data-ttu-id="37a61-1284">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1284">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-1285">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1285">Method creationDate</span></span>

<span data-ttu-id="37a61-1286">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1286">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1287">Parameters</span></span>

<span data-ttu-id="37a61-1288">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1288">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1289">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1289">Return Value</span></span>

<span data-ttu-id="37a61-1290">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1290">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-1291">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1291">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1292">Parameters</span></span>

<span data-ttu-id="37a61-1293">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1293">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1294">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1294">Return Value</span></span>

### <a name="method-extendeddatasecurity"></a><span data-ttu-id="37a61-1295">メソッド extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="37a61-1295">Method extendedDataSecurity</span></span>

    public boolean extendedDataSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1296">Parameters</span></span>

<span data-ttu-id="37a61-1297">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1297">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1298">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1298">Return Value</span></span>

### <a name="method-inheritnavigation"></a><span data-ttu-id="37a61-1299">メソッド inheritNavigation</span><span class="sxs-lookup"><span data-stu-id="37a61-1299">Method inheritNavigation</span></span>

    public boolean inheritNavigation([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1300">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1300">Parameters</span></span>

<span data-ttu-id="37a61-1301">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1301">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1302">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1302">Return Value</span></span>

### <a name="method-inheritpermissions"></a><span data-ttu-id="37a61-1303">メソッド inheritPermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-1303">Method inheritPermissions</span></span>

    public boolean inheritPermissions([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1304">Parameters</span></span>

<span data-ttu-id="37a61-1305">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1305">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1306">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1306">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="37a61-1307">メソッド label</span><span class="sxs-lookup"><span data-stu-id="37a61-1307">Method label</span></span>

<span data-ttu-id="37a61-1308">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1308">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1309">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1309">Parameters</span></span>

<span data-ttu-id="37a61-1310">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1310">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1311">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1311">Return Value</span></span>

<span data-ttu-id="37a61-1312">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="37a61-1312">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1313">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1313">Remarks</span></span>

<span data-ttu-id="37a61-1314">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1314">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="37a61-1315">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1315">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-masterpage"></a><span data-ttu-id="37a61-1316">メソッド masterPage</span><span class="sxs-lookup"><span data-stu-id="37a61-1316">Method masterPage</span></span>

    public str masterPage([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1317">Parameters</span></span>

<span data-ttu-id="37a61-1318">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1319">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1319">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="37a61-1320">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="37a61-1320">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1321">Parameters</span></span>

<span data-ttu-id="37a61-1322">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1322">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1323">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1323">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="37a61-1324">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="37a61-1324">Method menuItemType</span></span>

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1325">Parameters</span></span>

<span data-ttu-id="37a61-1326">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1326">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1327">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1327">Return Value</span></span>

### <a name="method-modulename"></a><span data-ttu-id="37a61-1328">メソッド moduleName</span><span class="sxs-lookup"><span data-stu-id="37a61-1328">Method moduleName</span></span>

    public str moduleName()

#### <a name="return-value"></a><span data-ttu-id="37a61-1329">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1329">Return Value</span></span>

### <a name="method-modulepath"></a><span data-ttu-id="37a61-1330">メソッド modulePath</span><span class="sxs-lookup"><span data-stu-id="37a61-1330">Method modulePath</span></span>

    public str modulePath()

#### <a name="return-value"></a><span data-ttu-id="37a61-1331">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1331">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-1332">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-1332">Method name</span></span>

<span data-ttu-id="37a61-1333">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1333">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1334">Parameters</span></span>

<span data-ttu-id="37a61-1335">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1335">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1336">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1336">Return Value</span></span>

<span data-ttu-id="37a61-1337">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1337">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1338">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1338">Remarks</span></span>

<span data-ttu-id="37a61-1339">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1339">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-1340">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1340">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-1341">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-1341">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-1342">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1342">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-1343">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1343">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-1344">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1344">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="37a61-1345">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="37a61-1345">Method neededAccessLevel</span></span>

<span data-ttu-id="37a61-1346">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1346">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1347">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1347">Parameters</span></span>

<span data-ttu-id="37a61-1348">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1348">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1349">Return Value</span></span>

<span data-ttu-id="37a61-1350">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="37a61-1350">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1351">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1351">Remarks</span></span>

<span data-ttu-id="37a61-1352">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="37a61-1352">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="37a61-1353">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="37a61-1353">AccessType::NoAccess</span></span>
-   <span data-ttu-id="37a61-1354">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="37a61-1354">AccessType::View</span></span>
-   <span data-ttu-id="37a61-1355">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="37a61-1355">AccessType::Edit</span></span>
-   <span data-ttu-id="37a61-1356">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="37a61-1356">AccessType::Add</span></span>
-   <span data-ttu-id="37a61-1357">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="37a61-1357">AccessType::Delete</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-1358">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-1358">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1359">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1359">Parameters</span></span>

<span data-ttu-id="37a61-1360">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1360">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1361">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1361">Return Value</span></span>

### <a name="method-publicmodule"></a><span data-ttu-id="37a61-1362">メソッド publicModule</span><span class="sxs-lookup"><span data-stu-id="37a61-1362">Method publicModule</span></span>

    public boolean publicModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1363">Parameters</span></span>

<span data-ttu-id="37a61-1364">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1364">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1365">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1365">Return Value</span></span>

### <a name="method-quicklaunch"></a><span data-ttu-id="37a61-1366">メソッド quickLaunch</span><span class="sxs-lookup"><span data-stu-id="37a61-1366">Method quickLaunch</span></span>

    public str quickLaunch([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1367">Parameters</span></span>

<span data-ttu-id="37a61-1368">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1368">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1369">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1369">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="37a61-1370">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="37a61-1370">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1371">Parameters</span></span>

<span data-ttu-id="37a61-1372">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1372">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1373">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1373">Return Value</span></span>

### <a name="method-showlink"></a><span data-ttu-id="37a61-1374">メソッド showLink</span><span class="sxs-lookup"><span data-stu-id="37a61-1374">Method showLink</span></span>

    public boolean showLink([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1375">Parameters</span></span>

<span data-ttu-id="37a61-1376">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1376">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1377">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1377">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="37a61-1378">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="37a61-1378">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1379">Parameters</span></span>

<span data-ttu-id="37a61-1380">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1380">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1381">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1381">Return Value</span></span>

### <a name="method-addsubmodule"></a><span data-ttu-id="37a61-1382">メソッド addSubModule</span><span class="sxs-lookup"><span data-stu-id="37a61-1382">Method addSubModule</span></span>

    public void addSubModule(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-1383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1383">Parameters</span></span>

<span data-ttu-id="37a61-1384">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-1384">name</span></span>  

### <a name="method-new"></a><span data-ttu-id="37a61-1385">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-1385">Method new</span></span>

<span data-ttu-id="37a61-1386">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1386">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="37a61-1387">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1387">Parameters</span></span>

<span data-ttu-id="37a61-1388">氏名</span><span class="sxs-lookup"><span data-stu-id="37a61-1388">Name</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="37a61-1389">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="37a61-1389">Method addMenuitem</span></span>

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a><span data-ttu-id="37a61-1390">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1390">Parameters</span></span>

<span data-ttu-id="37a61-1391">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="37a61-1391">webMenuFunction</span></span>  

## <a name="class-weboutputcontentitem"></a><span data-ttu-id="37a61-1392">クラス WebOutputContentItem</span><span class="sxs-lookup"><span data-stu-id="37a61-1392">Class WebOutputContentItem</span></span>
    class WebOutputContentItem extends WebContentItem

<span data-ttu-id="37a61-1393">このクラスは、x++ の WebOutputContentItem を表します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1393">This class represents a WebOutputContentItem in x++.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-1394">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1394">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1395">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1395">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1396">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-1396">Methods</span></span>

| <span data-ttu-id="37a61-1397">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1397">Method</span></span>                    | <span data-ttu-id="37a61-1398">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1398">Description</span></span>                         |
|---------------------------|-------------------------------------|
| <span data-ttu-id="37a61-1399">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-1399">public void new(str name)</span></span> | <span data-ttu-id="37a61-1400">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1400">Creates a new WebOutputContentItem.</span></span> |

### <a name="method-new"></a><span data-ttu-id="37a61-1401">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-1401">Method new</span></span>

<span data-ttu-id="37a61-1402">新しい WebOutputContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1402">Creates a new WebOutputContentItem.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-1403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1403">Parameters</span></span>

<span data-ttu-id="37a61-1404">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-1404">name</span></span>  

## <a name="class-webpagedefnode"></a><span data-ttu-id="37a61-1405">クラス webPageDefNode</span><span class="sxs-lookup"><span data-stu-id="37a61-1405">Class webPageDefNode</span></span>
    class webPageDefNode extends TreeNode

<span data-ttu-id="37a61-1406">webPageDefNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1406">The webPageDefNode class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-1407">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1407">Remarks</span></span>

<span data-ttu-id="37a61-1408">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1408">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="37a61-1409">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1409">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1410">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1410">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1411">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-1411">Methods</span></span>

| <span data-ttu-id="37a61-1412">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1412">Method</span></span>                                                     | <span data-ttu-id="37a61-1413">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1413">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-1414">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="37a61-1414">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="37a61-1415">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1415">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="37a61-1416">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1416">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="37a61-1417">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1417">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="37a61-1418">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1418">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="37a61-1419">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1419">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-1420">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1420">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="37a61-1421">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1421">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-1422">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1422">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="37a61-1423">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1423">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="37a61-1424">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1424">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="37a61-1425">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1425">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="37a61-1426">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1426">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="37a61-1427">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1427">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="37a61-1428">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1428">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="37a61-1429">public str imageResource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1429">public str imageResource(\[str value\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="37a61-1430">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1430">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="37a61-1431">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1431">public str name(\[str value\])</span></span>                             | <span data-ttu-id="37a61-1432">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1432">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-1433">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1433">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="37a61-1434">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1434">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="37a61-1435">public str parentPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1435">public str parentPage(\[str value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="37a61-1436">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1436">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="37a61-1437">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1437">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="37a61-1438">public boolean useContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1438">public boolean useContext(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="37a61-1439">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1439">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="37a61-1440">public str wSSHelpTopic(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1440">public str wSSHelpTopic(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="37a61-1441">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-1441">public void new(str name)</span></span>                                  | <span data-ttu-id="37a61-1442">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="37a61-1442">Creates a new webPageDefNode.</span></span>                                                                                                             |
| <span data-ttu-id="37a61-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1443">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="37a61-1444">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1444">Set the source of the webPageDefNode to the given string.</span></span>                                                                                 |

### <a name="method-aotgetsource"></a><span data-ttu-id="37a61-1445">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-1445">Method AOTgetSource</span></span>

<span data-ttu-id="37a61-1446">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1446">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="37a61-1447">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1447">Return Value</span></span>

<span data-ttu-id="37a61-1448">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="37a61-1448">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1449">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1449">Remarks</span></span>

<span data-ttu-id="37a61-1450">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1450">This method is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="37a61-1451">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1451">Method changedBy</span></span>

<span data-ttu-id="37a61-1452">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1452">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1453">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1453">Parameters</span></span>

<span data-ttu-id="37a61-1454">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1454">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1455">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1455">Return Value</span></span>

<span data-ttu-id="37a61-1456">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1456">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-1457">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1457">Method changedDate</span></span>

<span data-ttu-id="37a61-1458">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1458">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1459">Parameters</span></span>

<span data-ttu-id="37a61-1460">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1460">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1461">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1461">Return Value</span></span>

<span data-ttu-id="37a61-1462">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1462">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-1463">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1463">Method changedTime</span></span>

<span data-ttu-id="37a61-1464">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1464">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1465">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1465">Parameters</span></span>

<span data-ttu-id="37a61-1466">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1466">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1467">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1467">Return Value</span></span>

<span data-ttu-id="37a61-1468">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-1468">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-1469">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1469">Method createdBy</span></span>

<span data-ttu-id="37a61-1470">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1470">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1471">Parameters</span></span>

<span data-ttu-id="37a61-1472">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1472">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1473">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1473">Return Value</span></span>

<span data-ttu-id="37a61-1474">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1474">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-1475">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1475">Method creationDate</span></span>

<span data-ttu-id="37a61-1476">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1476">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1477">Parameters</span></span>

<span data-ttu-id="37a61-1478">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1478">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1479">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1479">Return Value</span></span>

<span data-ttu-id="37a61-1480">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1480">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-1481">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1481">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1482">Parameters</span></span>

<span data-ttu-id="37a61-1483">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1483">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1484">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1484">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="37a61-1485">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="37a61-1485">Method helpText</span></span>

<span data-ttu-id="37a61-1486">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1486">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1487">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1487">Parameters</span></span>

<span data-ttu-id="37a61-1488">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1488">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1489">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1489">Return Value</span></span>

<span data-ttu-id="37a61-1490">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="37a61-1490">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1491">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1491">Remarks</span></span>

<span data-ttu-id="37a61-1492">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1492">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="37a61-1493">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1493">The help text must not exceed 250 characters.</span></span>

### <a name="method-imageresource"></a><span data-ttu-id="37a61-1494">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="37a61-1494">Method imageResource</span></span>

    public str imageResource([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1495">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1495">Parameters</span></span>

<span data-ttu-id="37a61-1496">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1496">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1497">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1497">Return Value</span></span>

### <a name="method-mossonly"></a><span data-ttu-id="37a61-1498">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="37a61-1498">Method mOSSOnly</span></span>

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1499">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1499">Parameters</span></span>

<span data-ttu-id="37a61-1500">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1500">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1501">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-1502">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-1502">Method name</span></span>

<span data-ttu-id="37a61-1503">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1503">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1504">Parameters</span></span>

<span data-ttu-id="37a61-1505">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1505">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1506">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1506">Return Value</span></span>

<span data-ttu-id="37a61-1507">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1507">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1508">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1508">Remarks</span></span>

<span data-ttu-id="37a61-1509">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1509">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-1510">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1510">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-1511">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-1511">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-1512">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1512">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-1513">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1513">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-1514">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1514">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-1515">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-1515">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1516">Parameters</span></span>

<span data-ttu-id="37a61-1517">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1517">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1518">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1518">Return Value</span></span>

### <a name="method-pagetitle"></a><span data-ttu-id="37a61-1519">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="37a61-1519">Method pageTitle</span></span>

    public str pageTitle([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1520">Parameters</span></span>

<span data-ttu-id="37a61-1521">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1521">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1522">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1522">Return Value</span></span>

### <a name="method-parentpage"></a><span data-ttu-id="37a61-1523">メソッド parentPage</span><span class="sxs-lookup"><span data-stu-id="37a61-1523">Method parentPage</span></span>

    public str parentPage([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1524">Parameters</span></span>

<span data-ttu-id="37a61-1525">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1525">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1526">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1526">Return Value</span></span>

### <a name="method-publicpage"></a><span data-ttu-id="37a61-1527">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="37a61-1527">Method publicPage</span></span>

    public boolean publicPage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1528">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1528">Parameters</span></span>

<span data-ttu-id="37a61-1529">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1529">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1530">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1530">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="37a61-1531">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="37a61-1531">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1532">Parameters</span></span>

<span data-ttu-id="37a61-1533">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1533">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1534">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1534">Return Value</span></span>

### <a name="method-usecontext"></a><span data-ttu-id="37a61-1535">メソッド useContext</span><span class="sxs-lookup"><span data-stu-id="37a61-1535">Method useContext</span></span>

    public boolean useContext([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1536">Parameters</span></span>

<span data-ttu-id="37a61-1537">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1538">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1538">Return Value</span></span>

### <a name="method-webmodule"></a><span data-ttu-id="37a61-1539">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="37a61-1539">Method webModule</span></span>

    public str webModule([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1540">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1540">Parameters</span></span>

<span data-ttu-id="37a61-1541">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1541">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1542">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1542">Return Value</span></span>

### <a name="method-wsshelptopic"></a><span data-ttu-id="37a61-1543">メソッド wSSHelpTopic</span><span class="sxs-lookup"><span data-stu-id="37a61-1543">Method wSSHelpTopic</span></span>

    public str wSSHelpTopic([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1544">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1544">Parameters</span></span>

<span data-ttu-id="37a61-1545">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1545">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1546">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1546">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="37a61-1547">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-1547">Method new</span></span>

<span data-ttu-id="37a61-1548">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="37a61-1548">Creates a new webPageDefNode.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-1549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1549">Parameters</span></span>

<span data-ttu-id="37a61-1550">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-1550">name</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="37a61-1551">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-1551">Method AOTsetSource</span></span>

<span data-ttu-id="37a61-1552">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1552">Set the source of the webPageDefNode to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="37a61-1553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1553">Parameters</span></span>

<span data-ttu-id="37a61-1554">ソース</span><span class="sxs-lookup"><span data-stu-id="37a61-1554">source</span></span>  
<span data-ttu-id="37a61-1555">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="37a61-1555">Optional parameter marking if the source provided is static.</span></span>

<!-- -->

<span data-ttu-id="37a61-1556">isStatic</span><span class="sxs-lookup"><span data-stu-id="37a61-1556">isStatic</span></span>  
<span data-ttu-id="37a61-1557">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="37a61-1557">Optional parameter marking if the source provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1558">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1558">Remarks</span></span>

<span data-ttu-id="37a61-1559">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1559">This method is overridden by nodes which have source code.</span></span>

## <a name="class-webstaticfilenode"></a><span data-ttu-id="37a61-1560">クラス webStaticFileNode</span><span class="sxs-lookup"><span data-stu-id="37a61-1560">Class webStaticFileNode</span></span>
    class webStaticFileNode extends TreeNode

<span data-ttu-id="37a61-1561">webStaticFileNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1561">The webStaticFileNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-1562">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1562">Remarks</span></span>

<span data-ttu-id="37a61-1563">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1563">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1564">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1564">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1565">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-1565">Methods</span></span>

| <span data-ttu-id="37a61-1566">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1566">Method</span></span>                                                     | <span data-ttu-id="37a61-1567">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1567">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-1568">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="37a61-1568">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="37a61-1569">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1569">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="37a61-1570">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1570">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="37a61-1571">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1571">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="37a61-1572">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1572">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="37a61-1573">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1573">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-1574">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1574">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="37a61-1575">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1575">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="37a61-1576">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1576">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="37a61-1577">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1577">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="37a61-1578">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1578">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="37a61-1579">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1579">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="37a61-1580">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1580">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="37a61-1581">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1581">public str filename(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="37a61-1582">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1582">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="37a61-1583">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1583">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="37a61-1584">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1584">public str name(\[str value\])</span></span>                             | <span data-ttu-id="37a61-1585">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1585">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="37a61-1586">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1586">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="37a61-1587">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1587">public str relativePath(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="37a61-1588">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1588">public str version(\[str value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="37a61-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1589">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="37a61-1590">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1590">Sets the source of the static file node to the given string.</span></span>                                                                              |

### <a name="method-aotgetsource"></a><span data-ttu-id="37a61-1591">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-1591">Method AOTgetSource</span></span>

<span data-ttu-id="37a61-1592">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1592">Gets the source of the node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="37a61-1593">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1593">Return Value</span></span>

<span data-ttu-id="37a61-1594">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="37a61-1594">The source of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1595">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1595">Remarks</span></span>

<span data-ttu-id="37a61-1596">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1596">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="37a61-1597">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1597">Method changedBy</span></span>

<span data-ttu-id="37a61-1598">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1598">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1599">Parameters</span></span>

<span data-ttu-id="37a61-1600">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1600">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1601">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1601">Return Value</span></span>

<span data-ttu-id="37a61-1602">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1602">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="37a61-1603">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1603">Method changedDate</span></span>

<span data-ttu-id="37a61-1604">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1604">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1605">Parameters</span></span>

<span data-ttu-id="37a61-1606">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1606">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1607">Return Value</span></span>

<span data-ttu-id="37a61-1608">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1608">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="37a61-1609">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1609">Method changedTime</span></span>

<span data-ttu-id="37a61-1610">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1610">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1611">Parameters</span></span>

<span data-ttu-id="37a61-1612">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1612">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1613">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1613">Return Value</span></span>

<span data-ttu-id="37a61-1614">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="37a61-1614">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="37a61-1615">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="37a61-1615">Method createdBy</span></span>

<span data-ttu-id="37a61-1616">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1616">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1617">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1617">Parameters</span></span>

<span data-ttu-id="37a61-1618">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1618">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1619">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1619">Return Value</span></span>

<span data-ttu-id="37a61-1620">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1620">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="37a61-1621">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="37a61-1621">Method creationDate</span></span>

<span data-ttu-id="37a61-1622">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1622">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1623">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1623">Parameters</span></span>

<span data-ttu-id="37a61-1624">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1624">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1625">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1625">Return Value</span></span>

<span data-ttu-id="37a61-1626">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="37a61-1626">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="37a61-1627">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="37a61-1627">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1628">Parameters</span></span>

<span data-ttu-id="37a61-1629">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1630">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1630">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="37a61-1631">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="37a61-1631">Method filename</span></span>

    public str filename([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1632">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1632">Parameters</span></span>

<span data-ttu-id="37a61-1633">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1633">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1634">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1634">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="37a61-1635">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="37a61-1635">Method helpText</span></span>

<span data-ttu-id="37a61-1636">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1636">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1637">Parameters</span></span>

<span data-ttu-id="37a61-1638">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1638">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1639">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1639">Return Value</span></span>

<span data-ttu-id="37a61-1640">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="37a61-1640">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1641">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1641">Remarks</span></span>

<span data-ttu-id="37a61-1642">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1642">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="37a61-1643">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1643">The help text must not exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="37a61-1644">メソッド名</span><span class="sxs-lookup"><span data-stu-id="37a61-1644">Method name</span></span>

<span data-ttu-id="37a61-1645">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1645">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1646">Parameters</span></span>

<span data-ttu-id="37a61-1647">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1648">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1648">Return Value</span></span>

<span data-ttu-id="37a61-1649">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="37a61-1649">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1650">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1650">Remarks</span></span>

<span data-ttu-id="37a61-1651">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1651">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="37a61-1652">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1652">Begins with a letter.</span></span>
-   <span data-ttu-id="37a61-1653">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="37a61-1653">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="37a61-1654">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1654">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="37a61-1655">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1655">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="37a61-1656">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="37a61-1656">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-1657">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-1657">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1658">Parameters</span></span>

<span data-ttu-id="37a61-1659">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1659">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1660">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1660">Return Value</span></span>

### <a name="method-relativepath"></a><span data-ttu-id="37a61-1661">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="37a61-1661">Method relativePath</span></span>

    public str relativePath([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1662">Parameters</span></span>

<span data-ttu-id="37a61-1663">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1663">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1664">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1664">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="37a61-1665">メソッド version</span><span class="sxs-lookup"><span data-stu-id="37a61-1665">Method version</span></span>

    public str version([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1666">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1666">Parameters</span></span>

<span data-ttu-id="37a61-1667">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1667">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1668">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1668">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="37a61-1669">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="37a61-1669">Method AOTsetSource</span></span>

<span data-ttu-id="37a61-1670">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1670">Sets the source of the static file node to the given string.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="37a61-1671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1671">Parameters</span></span>

<span data-ttu-id="37a61-1672">ソース</span><span class="sxs-lookup"><span data-stu-id="37a61-1672">source</span></span>  
<span data-ttu-id="37a61-1673">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="37a61-1673">An optional parameter that marks whether the source that is provided is static.</span></span>

<!-- -->

<span data-ttu-id="37a61-1674">isStatic</span><span class="sxs-lookup"><span data-stu-id="37a61-1674">isStatic</span></span>  
<span data-ttu-id="37a61-1675">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="37a61-1675">An optional parameter that marks whether the source that is provided is static.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1676">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1676">Remarks</span></span>

<span data-ttu-id="37a61-1677">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1677">This method is overridden by nodes that have source code.</span></span>

## <a name="class-weburlmenufunction"></a><span data-ttu-id="37a61-1678">クラス WebUrlMenuFunction</span><span class="sxs-lookup"><span data-stu-id="37a61-1678">Class WebUrlMenuFunction</span></span>
    class WebUrlMenuFunction extends WebMenuFunction

<span data-ttu-id="37a61-1679">WebUrlMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37a61-1679">The WebUrlMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="37a61-1680">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1680">Remarks</span></span>

<span data-ttu-id="37a61-1681">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1681">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1682">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1682">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1683">メソッド</span><span class="sxs-lookup"><span data-stu-id="37a61-1683">Methods</span></span>

| <span data-ttu-id="37a61-1684">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1684">Method</span></span>                                                | <span data-ttu-id="37a61-1685">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1685">Description</span></span>                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a61-1686">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1686">public boolean big(\[boolean value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="37a61-1687">public int closeDialogBehavior(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1687">public int closeDialogBehavior(\[int value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="37a61-1688">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1688">public int correctPermissions(\[int value\])</span></span>          |                                                                                                        |
| <span data-ttu-id="37a61-1689">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1689">public int createPermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="37a61-1690">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1690">public int deletePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="37a61-1691">public boolean hideActionPane(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1691">public boolean hideActionPane(\[boolean value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="37a61-1692">public boolean homePage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1692">public boolean homePage(\[boolean value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="37a61-1693">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1693">public int imageLocation(\[int value\])</span></span>               |                                                                                                        |
| <span data-ttu-id="37a61-1694">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1694">public str linkedPermissionObject(\[str value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="37a61-1695">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1695">public str linkedPermissionObjectChild(\[str value\])</span></span> |                                                                                                        |
| <span data-ttu-id="37a61-1696">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1696">public int linkedPermissionType(\[int value\])</span></span>        |                                                                                                        |
| <span data-ttu-id="37a61-1697">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1697">public int maintainUserLicense(\[int value\])</span></span>         | <span data-ttu-id="37a61-1698">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-1698">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="37a61-1699">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1699">public boolean multiSelect(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="37a61-1700">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1700">public boolean needsRecord(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="37a61-1701">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1701">public str normalImage(\[str value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="37a61-1702">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1702">public int normalResource(\[int value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="37a61-1703">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1703">public Guid origin(\[Guid value\])</span></span>                    |                                                                                                        |
| <span data-ttu-id="37a61-1704">public str pageDefinition(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1704">public str pageDefinition(\[str value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="37a61-1705">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1705">public str parameters(\[str value\])</span></span>                  | <span data-ttu-id="37a61-1706">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1706">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span> |
| <span data-ttu-id="37a61-1707">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1707">public int readPermissions(\[int value\])</span></span>             |                                                                                                        |
| <span data-ttu-id="37a61-1708">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1708">public int updatePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="37a61-1709">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1709">public str uRL(\[str value\])</span></span>                         |                                                                                                        |
| <span data-ttu-id="37a61-1710">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1710">public int viewUserLicense(\[int value\])</span></span>             | <span data-ttu-id="37a61-1711">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-1711">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="37a61-1712">public int windowMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1712">public int windowMode(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="37a61-1713">public str windowParameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1713">public str windowParameters(\[str value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="37a61-1714">public int windowSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1714">public int windowSize(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="37a61-1715">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="37a61-1715">public void new(str name)</span></span>                             | <span data-ttu-id="37a61-1716">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1716">Initializes a new instance of the TreeNode class.</span></span>                                                      |

### <a name="method-big"></a><span data-ttu-id="37a61-1717">メソッド big</span><span class="sxs-lookup"><span data-stu-id="37a61-1717">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1718">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1718">Parameters</span></span>

<span data-ttu-id="37a61-1719">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1719">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1720">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1720">Return Value</span></span>

### <a name="method-closedialogbehavior"></a><span data-ttu-id="37a61-1721">メソッド closeDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="37a61-1721">Method closeDialogBehavior</span></span>

    public int closeDialogBehavior([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1722">Parameters</span></span>

<span data-ttu-id="37a61-1723">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1723">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1724">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1724">Return Value</span></span>

### <a name="method-correctpermissions"></a><span data-ttu-id="37a61-1725">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-1725">Method correctPermissions</span></span>

    public int correctPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1726">Parameters</span></span>

<span data-ttu-id="37a61-1727">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1727">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1728">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1728">Return Value</span></span>

### <a name="method-createpermissions"></a><span data-ttu-id="37a61-1729">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-1729">Method createPermissions</span></span>

    public int createPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1730">Parameters</span></span>

<span data-ttu-id="37a61-1731">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1731">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1732">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1732">Return Value</span></span>

### <a name="method-deletepermissions"></a><span data-ttu-id="37a61-1733">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-1733">Method deletePermissions</span></span>

    public int deletePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1734">Parameters</span></span>

<span data-ttu-id="37a61-1735">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1735">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1736">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1736">Return Value</span></span>

### <a name="method-hideactionpane"></a><span data-ttu-id="37a61-1737">メソッド hideActionPane</span><span class="sxs-lookup"><span data-stu-id="37a61-1737">Method hideActionPane</span></span>

    public boolean hideActionPane([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1738">Parameters</span></span>

<span data-ttu-id="37a61-1739">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1739">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1740">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1740">Return Value</span></span>

### <a name="method-homepage"></a><span data-ttu-id="37a61-1741">メソッド homePage</span><span class="sxs-lookup"><span data-stu-id="37a61-1741">Method homePage</span></span>

    public boolean homePage([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1742">Parameters</span></span>

<span data-ttu-id="37a61-1743">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1743">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1744">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1744">Return Value</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="37a61-1745">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="37a61-1745">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1746">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1746">Parameters</span></span>

<span data-ttu-id="37a61-1747">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1747">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1748">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1748">Return Value</span></span>

### <a name="method-linkedpermissionobject"></a><span data-ttu-id="37a61-1749">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="37a61-1749">Method linkedPermissionObject</span></span>

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1750">Parameters</span></span>

<span data-ttu-id="37a61-1751">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1751">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1752">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1752">Return Value</span></span>

### <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="37a61-1753">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="37a61-1753">Method linkedPermissionObjectChild</span></span>

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1754">Parameters</span></span>

<span data-ttu-id="37a61-1755">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1755">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1756">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1756">Return Value</span></span>

### <a name="method-linkedpermissiontype"></a><span data-ttu-id="37a61-1757">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="37a61-1757">Method linkedPermissionType</span></span>

    public int linkedPermissionType([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1758">Parameters</span></span>

<span data-ttu-id="37a61-1759">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1759">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1760">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1760">Return Value</span></span>

### <a name="method-maintainuserlicense"></a><span data-ttu-id="37a61-1761">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="37a61-1761">Method maintainUserLicense</span></span>

<span data-ttu-id="37a61-1762">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-1762">Microsoft internal use only.</span></span>

    public int maintainUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1763">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1763">Parameters</span></span>

<span data-ttu-id="37a61-1764">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1764">value</span></span>  
<span data-ttu-id="37a61-1765">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-1765">The new user license.</span></span>

#### <a name="return-value"></a><span data-ttu-id="37a61-1766">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1766">Return Value</span></span>

<span data-ttu-id="37a61-1767">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-1767">The user license.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="37a61-1768">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="37a61-1768">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1769">Parameters</span></span>

<span data-ttu-id="37a61-1770">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1770">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1771">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1771">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="37a61-1772">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="37a61-1772">Method needsRecord</span></span>

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1773">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1773">Parameters</span></span>

<span data-ttu-id="37a61-1774">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1774">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1775">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1775">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="37a61-1776">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="37a61-1776">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1777">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1777">Parameters</span></span>

<span data-ttu-id="37a61-1778">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1778">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1779">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1779">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="37a61-1780">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="37a61-1780">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1781">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1781">Parameters</span></span>

<span data-ttu-id="37a61-1782">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1782">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1783">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1783">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="37a61-1784">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="37a61-1784">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1785">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1785">Parameters</span></span>

<span data-ttu-id="37a61-1786">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1786">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1787">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1787">Return Value</span></span>

### <a name="method-pagedefinition"></a><span data-ttu-id="37a61-1788">メソッド pageDefinition</span><span class="sxs-lookup"><span data-stu-id="37a61-1788">Method pageDefinition</span></span>

    public str pageDefinition([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1789">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1789">Parameters</span></span>

<span data-ttu-id="37a61-1790">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1790">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1791">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1791">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="37a61-1792">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="37a61-1792">Method parameters</span></span>

<span data-ttu-id="37a61-1793">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1793">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1794">Parameters</span></span>

<span data-ttu-id="37a61-1795">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1796">Return Value</span></span>

<span data-ttu-id="37a61-1797">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="37a61-1797">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="37a61-1798">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1798">Remarks</span></span>

<span data-ttu-id="37a61-1799">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="37a61-1799">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="37a61-1800">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1800">Objects will ignore passed, unrecognized parameters.</span></span>

### <a name="method-readpermissions"></a><span data-ttu-id="37a61-1801">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-1801">Method readPermissions</span></span>

    public int readPermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1802">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1802">Parameters</span></span>

<span data-ttu-id="37a61-1803">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1803">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1804">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1804">Return Value</span></span>

### <a name="method-updatepermissions"></a><span data-ttu-id="37a61-1805">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="37a61-1805">Method updatePermissions</span></span>

    public int updatePermissions([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1806">Parameters</span></span>

<span data-ttu-id="37a61-1807">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1808">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1808">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="37a61-1809">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="37a61-1809">Method uRL</span></span>

    public str uRL([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1810">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1810">Parameters</span></span>

<span data-ttu-id="37a61-1811">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1811">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1812">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1812">Return Value</span></span>

### <a name="method-viewuserlicense"></a><span data-ttu-id="37a61-1813">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="37a61-1813">Method viewUserLicense</span></span>

<span data-ttu-id="37a61-1814">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="37a61-1814">Microsoft internal use only.</span></span>

    public int viewUserLicense([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1815">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1815">Parameters</span></span>

<span data-ttu-id="37a61-1816">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1816">value</span></span>  
<span data-ttu-id="37a61-1817">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-1817">A user license to view.</span></span>

#### <a name="return-value"></a><span data-ttu-id="37a61-1818">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1818">Return Value</span></span>

<span data-ttu-id="37a61-1819">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="37a61-1819">The user license.</span></span>

### <a name="method-windowmode"></a><span data-ttu-id="37a61-1820">メソッド windowMode</span><span class="sxs-lookup"><span data-stu-id="37a61-1820">Method windowMode</span></span>

    public int windowMode([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1821">Parameters</span></span>

<span data-ttu-id="37a61-1822">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1822">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1823">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1823">Return Value</span></span>

### <a name="method-windowparameters"></a><span data-ttu-id="37a61-1824">メソッド windowParameters</span><span class="sxs-lookup"><span data-stu-id="37a61-1824">Method windowParameters</span></span>

    public str windowParameters([str value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1825">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1825">Parameters</span></span>

<span data-ttu-id="37a61-1826">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1826">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1827">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1827">Return Value</span></span>

### <a name="method-windowsize"></a><span data-ttu-id="37a61-1828">メソッド windowSize</span><span class="sxs-lookup"><span data-stu-id="37a61-1828">Method windowSize</span></span>

    public int windowSize([int value])

#### <a name="parameters"></a><span data-ttu-id="37a61-1829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1829">Parameters</span></span>

<span data-ttu-id="37a61-1830">値</span><span class="sxs-lookup"><span data-stu-id="37a61-1830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1831">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1831">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="37a61-1832">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-1832">Method new</span></span>

<span data-ttu-id="37a61-1833">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1833">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name)

#### <a name="parameters"></a><span data-ttu-id="37a61-1834">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1834">Parameters</span></span>

<span data-ttu-id="37a61-1835">名前</span><span class="sxs-lookup"><span data-stu-id="37a61-1835">name</span></span>  

## <a name="class-winapinative"></a><span data-ttu-id="37a61-1836">クラス WinAPINative</span><span class="sxs-lookup"><span data-stu-id="37a61-1836">Class WinAPINative</span></span>
    class WinAPINative extends Object

### <a name="remarks"></a><span data-ttu-id="37a61-1837">備考</span><span class="sxs-lookup"><span data-stu-id="37a61-1837">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="37a61-1838">例</span><span class="sxs-lookup"><span data-stu-id="37a61-1838">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="37a61-1839">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1839">Methods</span></span>

| <span data-ttu-id="37a61-1840">方法</span><span class="sxs-lookup"><span data-stu-id="37a61-1840">Method</span></span>                                                                                                                  | <span data-ttu-id="37a61-1841">説明</span><span class="sxs-lookup"><span data-stu-id="37a61-1841">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="37a61-1842">::public static Int64 createFontIndirect(Binary logfont)</span><span class="sxs-lookup"><span data-stu-id="37a61-1842">::public static Int64 createFontIndirect(Binary logfont)</span></span>                                                                |                                                       |
| <span data-ttu-id="37a61-1843">::public static boolean deleteObject(Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="37a61-1843">::public static boolean deleteObject(Int64 hGDIObject)</span></span>                                                                  |                                                       |
| <span data-ttu-id="37a61-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span><span class="sxs-lookup"><span data-stu-id="37a61-1844">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span></span> |                                                       |
| <span data-ttu-id="37a61-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span><span class="sxs-lookup"><span data-stu-id="37a61-1845">::public static int getDeviceCaps(Int64 hDC, int index)</span></span>                                                                 |                                                       |
| <span data-ttu-id="37a61-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1846">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span></span>                              |                                                       |
| <span data-ttu-id="37a61-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span><span class="sxs-lookup"><span data-stu-id="37a61-1847">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span></span>                                                    |                                                       |
| <span data-ttu-id="37a61-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span><span class="sxs-lookup"><span data-stu-id="37a61-1848">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span></span>                                           |                                                       |
| <span data-ttu-id="37a61-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span><span class="sxs-lookup"><span data-stu-id="37a61-1849">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span></span>                                                       |                                                       |
| <span data-ttu-id="37a61-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span><span class="sxs-lookup"><span data-stu-id="37a61-1850">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span></span>                        |                                                       |
| <span data-ttu-id="37a61-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="37a61-1851">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span></span>                                                         |                                                       |
| <span data-ttu-id="37a61-1852">private void new()</span><span class="sxs-lookup"><span data-stu-id="37a61-1852">private void new()</span></span>                                                                                                      | <span data-ttu-id="37a61-1853">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1853">Initializes a new instance of the WinAPINative class.</span></span> |

### <a name="method-createfontindirect"></a><span data-ttu-id="37a61-1854">メソッド createFontIndirect</span><span class="sxs-lookup"><span data-stu-id="37a61-1854">Method createFontIndirect</span></span>

    public static Int64 createFontIndirect(Binary logfont)

#### <a name="parameters"></a><span data-ttu-id="37a61-1855">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1855">Parameters</span></span>

<span data-ttu-id="37a61-1856">logfont</span><span class="sxs-lookup"><span data-stu-id="37a61-1856">logfont</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1857">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1857">Return Value</span></span>

### <a name="method-deleteobject"></a><span data-ttu-id="37a61-1858">メソッド deleteObject</span><span class="sxs-lookup"><span data-stu-id="37a61-1858">Method deleteObject</span></span>

    public static boolean deleteObject(Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="37a61-1859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1859">Parameters</span></span>

<span data-ttu-id="37a61-1860">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="37a61-1860">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1861">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1861">Return Value</span></span>

### <a name="method-getcharabcwidthsi"></a><span data-ttu-id="37a61-1862">メソッド getCharABCWidthsI</span><span class="sxs-lookup"><span data-stu-id="37a61-1862">Method getCharABCWidthsI</span></span>

    public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)

#### <a name="parameters"></a><span data-ttu-id="37a61-1863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1863">Parameters</span></span>

<span data-ttu-id="37a61-1864">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1864">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1865">firstGlyphIndex</span><span class="sxs-lookup"><span data-stu-id="37a61-1865">firstGlyphIndex</span></span>  

<!-- -->

<span data-ttu-id="37a61-1866">glyphIndicesCount</span><span class="sxs-lookup"><span data-stu-id="37a61-1866">glyphIndicesCount</span></span>  

<!-- -->

<span data-ttu-id="37a61-1867">charWidths</span><span class="sxs-lookup"><span data-stu-id="37a61-1867">charWidths</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1868">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1868">Return Value</span></span>

### <a name="method-getdevicecaps"></a><span data-ttu-id="37a61-1869">メソッド getDeviceCaps</span><span class="sxs-lookup"><span data-stu-id="37a61-1869">Method getDeviceCaps</span></span>

    public static int getDeviceCaps(Int64 hDC, int index)

#### <a name="parameters"></a><span data-ttu-id="37a61-1870">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1870">Parameters</span></span>

<span data-ttu-id="37a61-1871">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1871">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1872">指数</span><span class="sxs-lookup"><span data-stu-id="37a61-1872">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1873">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1873">Return Value</span></span>

### <a name="method-getfontdata"></a><span data-ttu-id="37a61-1874">メソッド getFontData</span><span class="sxs-lookup"><span data-stu-id="37a61-1874">Method getFontData</span></span>

    public static int getFontData(Int64 hDC, int dwTable, int dwOffset, [Binary pvBuffer])

#### <a name="parameters"></a><span data-ttu-id="37a61-1875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1875">Parameters</span></span>

<span data-ttu-id="37a61-1876">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1876">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1877">dwTable</span><span class="sxs-lookup"><span data-stu-id="37a61-1877">dwTable</span></span>  

<!-- -->

<span data-ttu-id="37a61-1878">dwOffset</span><span class="sxs-lookup"><span data-stu-id="37a61-1878">dwOffset</span></span>  

<!-- -->

<span data-ttu-id="37a61-1879">pvBuffer</span><span class="sxs-lookup"><span data-stu-id="37a61-1879">pvBuffer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1880">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1880">Return Value</span></span>

### <a name="method-getfontunicoderanges"></a><span data-ttu-id="37a61-1881">メソッド getFontUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="37a61-1881">Method getFontUnicodeRanges</span></span>

    public static int getFontUnicodeRanges(Int64 hDC, [Binary lpgs])

#### <a name="parameters"></a><span data-ttu-id="37a61-1882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1882">Parameters</span></span>

<span data-ttu-id="37a61-1883">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1883">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1884">lpgs</span><span class="sxs-lookup"><span data-stu-id="37a61-1884">lpgs</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1885">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1885">Return Value</span></span>

### <a name="method-getglyphindices"></a><span data-ttu-id="37a61-1886">メソッド getGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="37a61-1886">Method getGlyphIndices</span></span>

    public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)

#### <a name="parameters"></a><span data-ttu-id="37a61-1887">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1887">Parameters</span></span>

<span data-ttu-id="37a61-1888">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1888">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1889">lpstr</span><span class="sxs-lookup"><span data-stu-id="37a61-1889">lpstr</span></span>  

<!-- -->

<span data-ttu-id="37a61-1890">pgi</span><span class="sxs-lookup"><span data-stu-id="37a61-1890">pgi</span></span>  

<!-- -->

<span data-ttu-id="37a61-1891">fl</span><span class="sxs-lookup"><span data-stu-id="37a61-1891">fl</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1892">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1892">Return Value</span></span>

### <a name="method-gettextmetrics"></a><span data-ttu-id="37a61-1893">メソッド getTextMetrics</span><span class="sxs-lookup"><span data-stu-id="37a61-1893">Method getTextMetrics</span></span>

    public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)

#### <a name="parameters"></a><span data-ttu-id="37a61-1894">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1894">Parameters</span></span>

<span data-ttu-id="37a61-1895">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1895">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1896">lpMetrics</span><span class="sxs-lookup"><span data-stu-id="37a61-1896">lpMetrics</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1897">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1897">Return Value</span></span>

### <a name="method-getuniscribeglyphindices"></a><span data-ttu-id="37a61-1898">メソッド getUniscribeGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="37a61-1898">Method getUniscribeGlyphIndices</span></span>

    public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)

#### <a name="parameters"></a><span data-ttu-id="37a61-1899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1899">Parameters</span></span>

<span data-ttu-id="37a61-1900">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1900">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1901">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="37a61-1901">hGDIObject</span></span>  

<!-- -->

<span data-ttu-id="37a61-1902">lpstr</span><span class="sxs-lookup"><span data-stu-id="37a61-1902">lpstr</span></span>  

<!-- -->

<span data-ttu-id="37a61-1903">pgi</span><span class="sxs-lookup"><span data-stu-id="37a61-1903">pgi</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1904">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1904">Return Value</span></span>

### <a name="method-selectobject"></a><span data-ttu-id="37a61-1905">メソッド selectObject</span><span class="sxs-lookup"><span data-stu-id="37a61-1905">Method selectObject</span></span>

    public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)

#### <a name="parameters"></a><span data-ttu-id="37a61-1906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a61-1906">Parameters</span></span>

<span data-ttu-id="37a61-1907">hDC</span><span class="sxs-lookup"><span data-stu-id="37a61-1907">hDC</span></span>  

<!-- -->

<span data-ttu-id="37a61-1908">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="37a61-1908">hGDIObject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="37a61-1909">戻り値</span><span class="sxs-lookup"><span data-stu-id="37a61-1909">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="37a61-1910">メソッド new</span><span class="sxs-lookup"><span data-stu-id="37a61-1910">Method new</span></span>

<span data-ttu-id="37a61-1911">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37a61-1911">Initializes a new instance of the WinAPINative class.</span></span>

    private void new()



