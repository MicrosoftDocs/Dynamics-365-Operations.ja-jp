---
title: WebUrlMenuFunction クラス
description: このトピックでは、WebUrlMenuFunction クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e758aa9b0251c2e19c329438d438eb74c66f9b43
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502687"
---
# <a name="class-weburlmenufunction"></a><span data-ttu-id="f7a72-103">クラス WebUrlMenuFunction</span><span class="sxs-lookup"><span data-stu-id="f7a72-103">Class WebUrlMenuFunction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WebUrlMenuFunction extends WebMenuFunction
```

<span data-ttu-id="f7a72-104">WebUrlMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7a72-104">The WebUrlMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a72-105">備考</span><span class="sxs-lookup"><span data-stu-id="f7a72-105">Remarks</span></span>

<span data-ttu-id="f7a72-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7a72-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="f7a72-107">例</span><span class="sxs-lookup"><span data-stu-id="f7a72-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f7a72-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7a72-108">Methods</span></span>

| <span data-ttu-id="f7a72-109">方法</span><span class="sxs-lookup"><span data-stu-id="f7a72-109">Method</span></span>                                                | <span data-ttu-id="f7a72-110">説明</span><span class="sxs-lookup"><span data-stu-id="f7a72-110">Description</span></span>                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a72-111">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-111">public boolean big(\[boolean value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="f7a72-112">public int closeDialogBehavior(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-112">public int closeDialogBehavior(\[int value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="f7a72-113">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-113">public int correctPermissions(\[int value\])</span></span>          |                                                                                                        |
| <span data-ttu-id="f7a72-114">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-114">public int createPermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="f7a72-115">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-115">public int deletePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="f7a72-116">public boolean hideActionPane(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-116">public boolean hideActionPane(\[boolean value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="f7a72-117">public boolean homePage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-117">public boolean homePage(\[boolean value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="f7a72-118">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-118">public int imageLocation(\[int value\])</span></span>               |                                                                                                        |
| <span data-ttu-id="f7a72-119">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-119">public str linkedPermissionObject(\[str value\])</span></span>      |                                                                                                        |
| <span data-ttu-id="f7a72-120">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-120">public str linkedPermissionObjectChild(\[str value\])</span></span> |                                                                                                        |
| <span data-ttu-id="f7a72-121">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-121">public int linkedPermissionType(\[int value\])</span></span>        |                                                                                                        |
| <span data-ttu-id="f7a72-122">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-122">public int maintainUserLicense(\[int value\])</span></span>         | <span data-ttu-id="f7a72-123">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="f7a72-123">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="f7a72-124">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-124">public boolean multiSelect(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="f7a72-125">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-125">public boolean needsRecord(\[boolean value\])</span></span>         |                                                                                                        |
| <span data-ttu-id="f7a72-126">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-126">public str normalImage(\[str value\])</span></span>                 |                                                                                                        |
| <span data-ttu-id="f7a72-127">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-127">public int normalResource(\[int value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="f7a72-128">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-128">public Guid origin(\[Guid value\])</span></span>                    |                                                                                                        |
| <span data-ttu-id="f7a72-129">public str pageDefinition(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-129">public str pageDefinition(\[str value\])</span></span>              |                                                                                                        |
| <span data-ttu-id="f7a72-130">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-130">public str parameters(\[str value\])</span></span>                  | <span data-ttu-id="f7a72-131">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7a72-131">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span> |
| <span data-ttu-id="f7a72-132">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-132">public int readPermissions(\[int value\])</span></span>             |                                                                                                        |
| <span data-ttu-id="f7a72-133">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-133">public int updatePermissions(\[int value\])</span></span>           |                                                                                                        |
| <span data-ttu-id="f7a72-134">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-134">public str uRL(\[str value\])</span></span>                         |                                                                                                        |
| <span data-ttu-id="f7a72-135">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-135">public int viewUserLicense(\[int value\])</span></span>             | <span data-ttu-id="f7a72-136">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="f7a72-136">Microsoft internal use only.</span></span>                                                                           |
| <span data-ttu-id="f7a72-137">public int windowMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-137">public int windowMode(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="f7a72-138">public str windowParameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-138">public str windowParameters(\[str value\])</span></span>            |                                                                                                        |
| <span data-ttu-id="f7a72-139">public int windowSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7a72-139">public int windowSize(\[int value\])</span></span>                  |                                                                                                        |
| <span data-ttu-id="f7a72-140">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="f7a72-140">public void new(str name)</span></span>                             | <span data-ttu-id="f7a72-141">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7a72-141">Initializes a new instance of the TreeNode class.</span></span>                                                      |

## <a name="method-big"></a><span data-ttu-id="f7a72-142">メソッド big</span><span class="sxs-lookup"><span data-stu-id="f7a72-142">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="f7a72-143">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="f7a72-143">Parameters - big</span></span>

<span data-ttu-id="f7a72-144">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-144">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="f7a72-145">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="f7a72-145">Return Value - big</span></span>

## <a name="method-closedialogbehavior"></a><span data-ttu-id="f7a72-146">メソッド closeDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="f7a72-146">Method closeDialogBehavior</span></span>

```xpp
public int closeDialogBehavior([int value])
```

### <a name="parameters---closedialogbehavior"></a><span data-ttu-id="f7a72-147">パラメーター - closeDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="f7a72-147">Parameters - closeDialogBehavior</span></span>

<span data-ttu-id="f7a72-148">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-148">value</span></span>  

### <a name="return-value---closedialogbehavior"></a><span data-ttu-id="f7a72-149">戻り値 - closeDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="f7a72-149">Return Value - closeDialogBehavior</span></span>

## <a name="method-correctpermissions"></a><span data-ttu-id="f7a72-150">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-150">Method correctPermissions</span></span>

```xpp
public int correctPermissions([int value])
```

### <a name="parameters---correctpermissions"></a><span data-ttu-id="f7a72-151">パラメーター - correctPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-151">Parameters - correctPermissions</span></span>

<span data-ttu-id="f7a72-152">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-152">value</span></span>  

### <a name="return-value---correctpermissions"></a><span data-ttu-id="f7a72-153">戻り値 - correctPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-153">Return Value - correctPermissions</span></span>

## <a name="method-createpermissions"></a><span data-ttu-id="f7a72-154">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-154">Method createPermissions</span></span>

```xpp
public int createPermissions([int value])
```

### <a name="parameters---createpermissions"></a><span data-ttu-id="f7a72-155">パラメーター - createPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-155">Parameters - createPermissions</span></span>

<span data-ttu-id="f7a72-156">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-156">value</span></span>  

### <a name="return-value---createpermissions"></a><span data-ttu-id="f7a72-157">戻り値 - createPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-157">Return Value - createPermissions</span></span>

## <a name="method-deletepermissions"></a><span data-ttu-id="f7a72-158">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-158">Method deletePermissions</span></span>

```xpp
public int deletePermissions([int value])
```

### <a name="parameters---deletepermissions"></a><span data-ttu-id="f7a72-159">パラメーター - deletePermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-159">Parameters - deletePermissions</span></span>

<span data-ttu-id="f7a72-160">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-160">value</span></span>  

### <a name="return-value---deletepermissions"></a><span data-ttu-id="f7a72-161">戻り値 - deletePermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-161">Return Value - deletePermissions</span></span>

## <a name="method-hideactionpane"></a><span data-ttu-id="f7a72-162">メソッド hideActionPane</span><span class="sxs-lookup"><span data-stu-id="f7a72-162">Method hideActionPane</span></span>

```xpp
public boolean hideActionPane([boolean value])
```

### <a name="parameters---hideactionpane"></a><span data-ttu-id="f7a72-163">パラメーター - hideActionPane</span><span class="sxs-lookup"><span data-stu-id="f7a72-163">Parameters - hideActionPane</span></span>

<span data-ttu-id="f7a72-164">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-164">value</span></span>  

### <a name="return-value---hideactionpane"></a><span data-ttu-id="f7a72-165">戻り値 - hideActionPane</span><span class="sxs-lookup"><span data-stu-id="f7a72-165">Return Value - hideActionPane</span></span>

## <a name="method-homepage"></a><span data-ttu-id="f7a72-166">メソッド homePage</span><span class="sxs-lookup"><span data-stu-id="f7a72-166">Method homePage</span></span>

```xpp
public boolean homePage([boolean value])
```

### <a name="parameters---homepage"></a><span data-ttu-id="f7a72-167">パラメーター - homePage</span><span class="sxs-lookup"><span data-stu-id="f7a72-167">Parameters - homePage</span></span>

<span data-ttu-id="f7a72-168">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-168">value</span></span>  

### <a name="return-value---homepage"></a><span data-ttu-id="f7a72-169">戻り値 - homePage</span><span class="sxs-lookup"><span data-stu-id="f7a72-169">Return Value - homePage</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="f7a72-170">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="f7a72-170">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="f7a72-171">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="f7a72-171">Parameters - imageLocation</span></span>

<span data-ttu-id="f7a72-172">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-172">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="f7a72-173">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="f7a72-173">Return Value - imageLocation</span></span>

## <a name="method-linkedpermissionobject"></a><span data-ttu-id="f7a72-174">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="f7a72-174">Method linkedPermissionObject</span></span>

```xpp
public str linkedPermissionObject([str value])
```

### <a name="parameters---linkedpermissionobject"></a><span data-ttu-id="f7a72-175">パラメーター - linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="f7a72-175">Parameters - linkedPermissionObject</span></span>

<span data-ttu-id="f7a72-176">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-176">value</span></span>  

### <a name="return-value---linkedpermissionobject"></a><span data-ttu-id="f7a72-177">戻り値 - linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="f7a72-177">Return Value - linkedPermissionObject</span></span>

## <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="f7a72-178">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="f7a72-178">Method linkedPermissionObjectChild</span></span>

```xpp
public str linkedPermissionObjectChild([str value])
```

### <a name="parameters---linkedpermissionobjectchild"></a><span data-ttu-id="f7a72-179">パラメーター - linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="f7a72-179">Parameters - linkedPermissionObjectChild</span></span>

<span data-ttu-id="f7a72-180">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-180">value</span></span>  

### <a name="return-value---linkedpermissionobjectchild"></a><span data-ttu-id="f7a72-181">戻り値 - linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="f7a72-181">Return Value - linkedPermissionObjectChild</span></span>

## <a name="method-linkedpermissiontype"></a><span data-ttu-id="f7a72-182">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="f7a72-182">Method linkedPermissionType</span></span>

```xpp
public int linkedPermissionType([int value])
```

### <a name="parameters---linkedpermissiontype"></a><span data-ttu-id="f7a72-183">パラメーター - linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="f7a72-183">Parameters - linkedPermissionType</span></span>

<span data-ttu-id="f7a72-184">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-184">value</span></span>  

### <a name="return-value---linkedpermissiontype"></a><span data-ttu-id="f7a72-185">戻り値 - linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="f7a72-185">Return Value - linkedPermissionType</span></span>

## <a name="method-maintainuserlicense"></a><span data-ttu-id="f7a72-186">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="f7a72-186">Method maintainUserLicense</span></span>

<span data-ttu-id="f7a72-187">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="f7a72-187">Microsoft internal use only.</span></span>

```xpp
public int maintainUserLicense([int value])
```

### <a name="parameters---maintainuserlicense"></a><span data-ttu-id="f7a72-188">パラメーター - maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="f7a72-188">Parameters - maintainUserLicense</span></span>

<span data-ttu-id="f7a72-189">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-189">value</span></span>  
<span data-ttu-id="f7a72-190">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="f7a72-190">The new user license.</span></span>

### <a name="return-value---maintainuserlicense"></a><span data-ttu-id="f7a72-191">戻り値 - maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="f7a72-191">Return Value - maintainUserLicense</span></span>

<span data-ttu-id="f7a72-192">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="f7a72-192">The user license.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="f7a72-193">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="f7a72-193">Method multiSelect</span></span>

```xpp
public boolean multiSelect([boolean value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="f7a72-194">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="f7a72-194">Parameters - multiSelect</span></span>

<span data-ttu-id="f7a72-195">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-195">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="f7a72-196">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="f7a72-196">Return Value - multiSelect</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="f7a72-197">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="f7a72-197">Method needsRecord</span></span>

```xpp
public boolean needsRecord([boolean value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="f7a72-198">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="f7a72-198">Parameters - needsRecord</span></span>

<span data-ttu-id="f7a72-199">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-199">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="f7a72-200">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="f7a72-200">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="f7a72-201">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="f7a72-201">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="f7a72-202">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="f7a72-202">Parameters - normalImage</span></span>

<span data-ttu-id="f7a72-203">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-203">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="f7a72-204">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="f7a72-204">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="f7a72-205">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="f7a72-205">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="f7a72-206">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="f7a72-206">Parameters - normalResource</span></span>

<span data-ttu-id="f7a72-207">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-207">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="f7a72-208">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="f7a72-208">Return Value - normalResource</span></span>

## <a name="method-origin"></a><span data-ttu-id="f7a72-209">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="f7a72-209">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="f7a72-210">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="f7a72-210">Parameters - origin</span></span>

<span data-ttu-id="f7a72-211">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-211">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="f7a72-212">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="f7a72-212">Return Value - origin</span></span>

## <a name="method-pagedefinition"></a><span data-ttu-id="f7a72-213">メソッド pageDefinition</span><span class="sxs-lookup"><span data-stu-id="f7a72-213">Method pageDefinition</span></span>

```xpp
public str pageDefinition([str value])
```

### <a name="parameters---pagedefinition"></a><span data-ttu-id="f7a72-214">パラメーター - pageDefinition</span><span class="sxs-lookup"><span data-stu-id="f7a72-214">Parameters - pageDefinition</span></span>

<span data-ttu-id="f7a72-215">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-215">value</span></span>  

### <a name="return-value---pagedefinition"></a><span data-ttu-id="f7a72-216">戻り値 - pageDefinition</span><span class="sxs-lookup"><span data-stu-id="f7a72-216">Return Value - pageDefinition</span></span>

## <a name="method-parameters"></a><span data-ttu-id="f7a72-217">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="f7a72-217">Method parameters</span></span>

<span data-ttu-id="f7a72-218">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7a72-218">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="f7a72-219">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="f7a72-219">Parameters - parameters</span></span>

<span data-ttu-id="f7a72-220">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-220">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="f7a72-221">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="f7a72-221">Return Value - parameters</span></span>

<span data-ttu-id="f7a72-222">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="f7a72-222">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="f7a72-223">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="f7a72-223">Remarks - parameters</span></span>

<span data-ttu-id="f7a72-224">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="f7a72-224">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="f7a72-225">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="f7a72-225">Objects will ignore passed, unrecognized parameters.</span></span>

## <a name="method-readpermissions"></a><span data-ttu-id="f7a72-226">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-226">Method readPermissions</span></span>

```xpp
public int readPermissions([int value])
```

### <a name="parameters---readpermissions"></a><span data-ttu-id="f7a72-227">パラメーター - readPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-227">Parameters - readPermissions</span></span>

<span data-ttu-id="f7a72-228">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-228">value</span></span>  

### <a name="return-value---readpermissions"></a><span data-ttu-id="f7a72-229">戻り値 - readPermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-229">Return Value - readPermissions</span></span>

## <a name="method-updatepermissions"></a><span data-ttu-id="f7a72-230">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-230">Method updatePermissions</span></span>

```xpp
public int updatePermissions([int value])
```

### <a name="parameters---updatepermissions"></a><span data-ttu-id="f7a72-231">パラメーター - updatePermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-231">Parameters - updatePermissions</span></span>

<span data-ttu-id="f7a72-232">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-232">value</span></span>  

### <a name="return-value---updatepermissions"></a><span data-ttu-id="f7a72-233">戻り値 - updatePermissions</span><span class="sxs-lookup"><span data-stu-id="f7a72-233">Return Value - updatePermissions</span></span>

## <a name="method-url"></a><span data-ttu-id="f7a72-234">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="f7a72-234">Method uRL</span></span>

```xpp
public str uRL([str value])
```

### <a name="parameters---url"></a><span data-ttu-id="f7a72-235">パラメーター - uRL</span><span class="sxs-lookup"><span data-stu-id="f7a72-235">Parameters - uRL</span></span>

<span data-ttu-id="f7a72-236">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-236">value</span></span>  

### <a name="return-value---url"></a><span data-ttu-id="f7a72-237">戻り値 - uRL</span><span class="sxs-lookup"><span data-stu-id="f7a72-237">Return Value - uRL</span></span>

## <a name="method-viewuserlicense"></a><span data-ttu-id="f7a72-238">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="f7a72-238">Method viewUserLicense</span></span>

<span data-ttu-id="f7a72-239">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="f7a72-239">Microsoft internal use only.</span></span>

```xpp
public int viewUserLicense([int value])
```

### <a name="parameters---viewuserlicense"></a><span data-ttu-id="f7a72-240">パラメーター - viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="f7a72-240">Parameters - viewUserLicense</span></span>

<span data-ttu-id="f7a72-241">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-241">value</span></span>  
<span data-ttu-id="f7a72-242">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="f7a72-242">A user license to view.</span></span>

### <a name="return-value---viewuserlicense"></a><span data-ttu-id="f7a72-243">戻り値 - viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="f7a72-243">Return Value - viewUserLicense</span></span>

<span data-ttu-id="f7a72-244">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="f7a72-244">The user license.</span></span>

## <a name="method-windowmode"></a><span data-ttu-id="f7a72-245">メソッド windowMode</span><span class="sxs-lookup"><span data-stu-id="f7a72-245">Method windowMode</span></span>

```xpp
public int windowMode([int value])
```

### <a name="parameters---windowmode"></a><span data-ttu-id="f7a72-246">パラメーター - windowMode</span><span class="sxs-lookup"><span data-stu-id="f7a72-246">Parameters - windowMode</span></span>

<span data-ttu-id="f7a72-247">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-247">value</span></span>  

### <a name="return-value---windowmode"></a><span data-ttu-id="f7a72-248">戻り値 - windowMode</span><span class="sxs-lookup"><span data-stu-id="f7a72-248">Return Value - windowMode</span></span>

## <a name="method-windowparameters"></a><span data-ttu-id="f7a72-249">メソッド windowParameters</span><span class="sxs-lookup"><span data-stu-id="f7a72-249">Method windowParameters</span></span>

```xpp
public str windowParameters([str value])
```

### <a name="parameters---windowparameters"></a><span data-ttu-id="f7a72-250">パラメーター - windowParameters</span><span class="sxs-lookup"><span data-stu-id="f7a72-250">Parameters - windowParameters</span></span>

<span data-ttu-id="f7a72-251">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-251">value</span></span>  

### <a name="return-value---windowparameters"></a><span data-ttu-id="f7a72-252">戻り値 - windowParameters</span><span class="sxs-lookup"><span data-stu-id="f7a72-252">Return Value - windowParameters</span></span>

## <a name="method-windowsize"></a><span data-ttu-id="f7a72-253">メソッド windowSize</span><span class="sxs-lookup"><span data-stu-id="f7a72-253">Method windowSize</span></span>

```xpp
public int windowSize([int value])
```

### <a name="parameters---windowsize"></a><span data-ttu-id="f7a72-254">パラメーター - windowSize</span><span class="sxs-lookup"><span data-stu-id="f7a72-254">Parameters - windowSize</span></span>

<span data-ttu-id="f7a72-255">値</span><span class="sxs-lookup"><span data-stu-id="f7a72-255">value</span></span>  

### <a name="return-value---windowsize"></a><span data-ttu-id="f7a72-256">戻り値 - windowSize</span><span class="sxs-lookup"><span data-stu-id="f7a72-256">Return Value - windowSize</span></span>

## <a name="method-new"></a><span data-ttu-id="f7a72-257">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7a72-257">Method new</span></span>

<span data-ttu-id="f7a72-258">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7a72-258">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str name)
```

### <a name="parameters---new"></a><span data-ttu-id="f7a72-259">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="f7a72-259">Parameters - new</span></span>

<span data-ttu-id="f7a72-260">名前</span><span class="sxs-lookup"><span data-stu-id="f7a72-260">name</span></span>  

