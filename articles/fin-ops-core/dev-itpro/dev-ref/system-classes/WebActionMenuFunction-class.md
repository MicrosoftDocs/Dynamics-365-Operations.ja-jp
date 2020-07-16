---
title: WebActionMenuFunction クラス
description: このトピックでは、WebActionMenuFunction クラスについて説明します。
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
ms.openlocfilehash: 1d8ec6e7110dcf706ee92d5edfb911801bcc2d66
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502776"
---
# <a name="class-webactionmenufunction"></a><span data-ttu-id="c1178-103">クラス WebActionMenuFunction</span><span class="sxs-lookup"><span data-stu-id="c1178-103">Class WebActionMenuFunction</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class WebActionMenuFunction extends WebMenuFunction
```

<span data-ttu-id="c1178-104">WebActionMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c1178-104">The WebActionMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1178-105">備考</span><span class="sxs-lookup"><span data-stu-id="c1178-105">Remarks</span></span>

<span data-ttu-id="c1178-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c1178-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="c1178-107">例</span><span class="sxs-lookup"><span data-stu-id="c1178-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c1178-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="c1178-108">Methods</span></span>

| <span data-ttu-id="c1178-109">方法</span><span class="sxs-lookup"><span data-stu-id="c1178-109">Method</span></span>                                                   | <span data-ttu-id="c1178-110">説明</span><span class="sxs-lookup"><span data-stu-id="c1178-110">Description</span></span>                                                                                                 |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1178-111">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-111">public boolean big(\[boolean value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="c1178-112">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-112">public int correctPermissions(\[int value\])</span></span>             |                                                                                                             |
| <span data-ttu-id="c1178-113">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-113">public int createPermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="c1178-114">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-114">public int deletePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="c1178-115">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-115">public int enumParameter(\[int value\])</span></span>                  | <span data-ttu-id="c1178-116">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-116">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span> |
| <span data-ttu-id="c1178-117">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-117">public EnumId enumTypeParameter(\[EnumId value\])</span></span>        | <span data-ttu-id="c1178-118">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-118">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                     |
| <span data-ttu-id="c1178-119">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-119">public int imageLocation(\[int value\])</span></span>                  |                                                                                                             |
| <span data-ttu-id="c1178-120">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-120">public str linkedPermissionObject(\[str value\])</span></span>         |                                                                                                             |
| <span data-ttu-id="c1178-121">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-121">public str linkedPermissionObjectChild(\[str value\])</span></span>    |                                                                                                             |
| <span data-ttu-id="c1178-122">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-122">public int linkedPermissionType(\[int value\])</span></span>           |                                                                                                             |
| <span data-ttu-id="c1178-123">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-123">public int maintainUserLicense(\[int value\])</span></span>            | <span data-ttu-id="c1178-124">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="c1178-124">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="c1178-125">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-125">public boolean multiSelect(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="c1178-126">public boolean needsRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-126">public boolean needsRecord(\[boolean value\])</span></span>            |                                                                                                             |
| <span data-ttu-id="c1178-127">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-127">public str normalImage(\[str value\])</span></span>                    |                                                                                                             |
| <span data-ttu-id="c1178-128">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-128">public int normalResource(\[int value\])</span></span>                 |                                                                                                             |
| <span data-ttu-id="c1178-129">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-129">public str object(\[str value\])</span></span>                         | <span data-ttu-id="c1178-130">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-130">Gets or sets the object that the MenuFunction class runs.</span></span>                                                   |
| <span data-ttu-id="c1178-131">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-131">public int objectType(\[int value\])</span></span>                     |                                                                                                             |
| <span data-ttu-id="c1178-132">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-132">public Guid origin(\[Guid value\])</span></span>                       |                                                                                                             |
| <span data-ttu-id="c1178-133">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-133">public str parameters(\[str value\])</span></span>                     | <span data-ttu-id="c1178-134">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-134">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>      |
| <span data-ttu-id="c1178-135">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-135">public int readPermissions(\[int value\])</span></span>                |                                                                                                             |
| <span data-ttu-id="c1178-136">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-136">public str reportDesign(\[str value\])</span></span>                   |                                                                                                             |
| <span data-ttu-id="c1178-137">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-137">public int runOn(\[int value\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="c1178-138">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-138">public int updatePermissions(\[int value\])</span></span>              |                                                                                                             |
| <span data-ttu-id="c1178-139">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1178-139">public int viewUserLicense(\[int value\])</span></span>                | <span data-ttu-id="c1178-140">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="c1178-140">Microsoft internal use only.</span></span>                                                                                |
| <span data-ttu-id="c1178-141">::public static void runCalled(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="c1178-141">::public static void runCalled(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="c1178-142">public void AOTrun(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="c1178-142">public void AOTrun(\[xArgs args\])</span></span>                       | <span data-ttu-id="c1178-143">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="c1178-143">Compiles this node and its sub-tree in the Application Object Tree (AOT).</span></span>             |
| <span data-ttu-id="c1178-144">::public static void runClient(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="c1178-144">::public static void runClient(str name, \[xArgs args\])</span></span> |                                                                                                             |
| <span data-ttu-id="c1178-145">public void run(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="c1178-145">public void run(\[xArgs args\])</span></span>                          |                                                                                                             |
| <span data-ttu-id="c1178-146">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="c1178-146">public void new(str name)</span></span>                                | <span data-ttu-id="c1178-147">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c1178-147">Initializes a new instance of the TreeNode class.</span></span>                                                           |
| <span data-ttu-id="c1178-148">::public static void runServer(str name, \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="c1178-148">::public static void runServer(str name, \[xArgs args\])</span></span> |                                                                                                             |

## <a name="method-big"></a><span data-ttu-id="c1178-149">メソッド big</span><span class="sxs-lookup"><span data-stu-id="c1178-149">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="c1178-150">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="c1178-150">Parameters - big</span></span>

<span data-ttu-id="c1178-151">値</span><span class="sxs-lookup"><span data-stu-id="c1178-151">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="c1178-152">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="c1178-152">Return Value - big</span></span>

## <a name="method-correctpermissions"></a><span data-ttu-id="c1178-153">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-153">Method correctPermissions</span></span>

```xpp
public int correctPermissions([int value])
```

### <a name="parameters---correctpermissions"></a><span data-ttu-id="c1178-154">パラメーター - correctPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-154">Parameters - correctPermissions</span></span>

<span data-ttu-id="c1178-155">値</span><span class="sxs-lookup"><span data-stu-id="c1178-155">value</span></span>  

### <a name="return-value---correctpermissions"></a><span data-ttu-id="c1178-156">戻り値 - correctPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-156">Return Value - correctPermissions</span></span>

## <a name="method-createpermissions"></a><span data-ttu-id="c1178-157">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-157">Method createPermissions</span></span>

```xpp
public int createPermissions([int value])
```

### <a name="parameters---createpermissions"></a><span data-ttu-id="c1178-158">パラメーター - createPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-158">Parameters - createPermissions</span></span>

<span data-ttu-id="c1178-159">値</span><span class="sxs-lookup"><span data-stu-id="c1178-159">value</span></span>  

### <a name="return-value---createpermissions"></a><span data-ttu-id="c1178-160">戻り値 - createPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-160">Return Value - createPermissions</span></span>

## <a name="method-deletepermissions"></a><span data-ttu-id="c1178-161">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-161">Method deletePermissions</span></span>

```xpp
public int deletePermissions([int value])
```

### <a name="parameters---deletepermissions"></a><span data-ttu-id="c1178-162">パラメーター - deletePermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-162">Parameters - deletePermissions</span></span>

<span data-ttu-id="c1178-163">値</span><span class="sxs-lookup"><span data-stu-id="c1178-163">value</span></span>  

### <a name="return-value---deletepermissions"></a><span data-ttu-id="c1178-164">戻り値 - deletePermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-164">Return Value - deletePermissions</span></span>

## <a name="method-enumparameter"></a><span data-ttu-id="c1178-165">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="c1178-165">Method enumParameter</span></span>

<span data-ttu-id="c1178-166">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-166">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

```xpp
public int enumParameter([int value])
```

### <a name="parameters---enumparameter"></a><span data-ttu-id="c1178-167">パラメーター - enumParameter</span><span class="sxs-lookup"><span data-stu-id="c1178-167">Parameters - enumParameter</span></span>

<span data-ttu-id="c1178-168">値</span><span class="sxs-lookup"><span data-stu-id="c1178-168">value</span></span>  

### <a name="return-value---enumparameter"></a><span data-ttu-id="c1178-169">戻り値 - enumParameter</span><span class="sxs-lookup"><span data-stu-id="c1178-169">Return Value - enumParameter</span></span>

<span data-ttu-id="c1178-170">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="c1178-170">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

## <a name="method-enumtypeparameter"></a><span data-ttu-id="c1178-171">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="c1178-171">Method enumTypeParameter</span></span>

<span data-ttu-id="c1178-172">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-172">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

```xpp
public EnumId enumTypeParameter([EnumId value])
```

### <a name="parameters---enumtypeparameter"></a><span data-ttu-id="c1178-173">パラメーター - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="c1178-173">Parameters - enumTypeParameter</span></span>

<span data-ttu-id="c1178-174">値</span><span class="sxs-lookup"><span data-stu-id="c1178-174">value</span></span>  

### <a name="return-value---enumtypeparameter"></a><span data-ttu-id="c1178-175">戻り値 - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="c1178-175">Return Value - enumTypeParameter</span></span>

<span data-ttu-id="c1178-176">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="c1178-176">The enumTypeParameter property for the MenuFunction class.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="c1178-177">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="c1178-177">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="c1178-178">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="c1178-178">Parameters - imageLocation</span></span>

<span data-ttu-id="c1178-179">値</span><span class="sxs-lookup"><span data-stu-id="c1178-179">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="c1178-180">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="c1178-180">Return Value - imageLocation</span></span>

## <a name="method-linkedpermissionobject"></a><span data-ttu-id="c1178-181">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="c1178-181">Method linkedPermissionObject</span></span>

```xpp
public str linkedPermissionObject([str value])
```

### <a name="parameters---linkedpermissionobject"></a><span data-ttu-id="c1178-182">パラメーター - linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="c1178-182">Parameters - linkedPermissionObject</span></span>

<span data-ttu-id="c1178-183">値</span><span class="sxs-lookup"><span data-stu-id="c1178-183">value</span></span>  

### <a name="return-value---linkedpermissionobject"></a><span data-ttu-id="c1178-184">戻り値 - linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="c1178-184">Return Value - linkedPermissionObject</span></span>

## <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="c1178-185">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="c1178-185">Method linkedPermissionObjectChild</span></span>

```xpp
public str linkedPermissionObjectChild([str value])
```

### <a name="parameters---linkedpermissionobjectchild"></a><span data-ttu-id="c1178-186">パラメーター - linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="c1178-186">Parameters - linkedPermissionObjectChild</span></span>

<span data-ttu-id="c1178-187">値</span><span class="sxs-lookup"><span data-stu-id="c1178-187">value</span></span>  

### <a name="return-value---linkedpermissionobjectchild"></a><span data-ttu-id="c1178-188">戻り値 - linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="c1178-188">Return Value - linkedPermissionObjectChild</span></span>

## <a name="method-linkedpermissiontype"></a><span data-ttu-id="c1178-189">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="c1178-189">Method linkedPermissionType</span></span>

```xpp
public int linkedPermissionType([int value])
```

### <a name="parameters---linkedpermissiontype"></a><span data-ttu-id="c1178-190">パラメーター - linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="c1178-190">Parameters - linkedPermissionType</span></span>

<span data-ttu-id="c1178-191">値</span><span class="sxs-lookup"><span data-stu-id="c1178-191">value</span></span>  

### <a name="return-value---linkedpermissiontype"></a><span data-ttu-id="c1178-192">戻り値 - linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="c1178-192">Return Value - linkedPermissionType</span></span>

## <a name="method-maintainuserlicense"></a><span data-ttu-id="c1178-193">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="c1178-193">Method maintainUserLicense</span></span>

<span data-ttu-id="c1178-194">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="c1178-194">Microsoft internal use only.</span></span>

```xpp
public int maintainUserLicense([int value])
```

### <a name="parameters---maintainuserlicense"></a><span data-ttu-id="c1178-195">パラメーター - maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="c1178-195">Parameters - maintainUserLicense</span></span>

<span data-ttu-id="c1178-196">値</span><span class="sxs-lookup"><span data-stu-id="c1178-196">value</span></span>  
<span data-ttu-id="c1178-197">新しいユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="c1178-197">The new user license.</span></span>

### <a name="return-value---maintainuserlicense"></a><span data-ttu-id="c1178-198">戻り値 - maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="c1178-198">Return Value - maintainUserLicense</span></span>

<span data-ttu-id="c1178-199">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="c1178-199">The user license.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="c1178-200">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="c1178-200">Method multiSelect</span></span>

```xpp
public boolean multiSelect([boolean value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="c1178-201">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="c1178-201">Parameters - multiSelect</span></span>

<span data-ttu-id="c1178-202">値</span><span class="sxs-lookup"><span data-stu-id="c1178-202">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="c1178-203">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="c1178-203">Return Value - multiSelect</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="c1178-204">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="c1178-204">Method needsRecord</span></span>

```xpp
public boolean needsRecord([boolean value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="c1178-205">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="c1178-205">Parameters - needsRecord</span></span>

<span data-ttu-id="c1178-206">値</span><span class="sxs-lookup"><span data-stu-id="c1178-206">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="c1178-207">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="c1178-207">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="c1178-208">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="c1178-208">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="c1178-209">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="c1178-209">Parameters - normalImage</span></span>

<span data-ttu-id="c1178-210">値</span><span class="sxs-lookup"><span data-stu-id="c1178-210">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="c1178-211">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="c1178-211">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="c1178-212">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="c1178-212">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="c1178-213">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="c1178-213">Parameters - normalResource</span></span>

<span data-ttu-id="c1178-214">値</span><span class="sxs-lookup"><span data-stu-id="c1178-214">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="c1178-215">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="c1178-215">Return Value - normalResource</span></span>

## <a name="method-object"></a><span data-ttu-id="c1178-216">メソッド object</span><span class="sxs-lookup"><span data-stu-id="c1178-216">Method object</span></span>

<span data-ttu-id="c1178-217">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-217">Gets or sets the object that the MenuFunction class runs.</span></span>

```xpp
public str object([str value])
```

### <a name="parameters---object"></a><span data-ttu-id="c1178-218">パラメーター - object</span><span class="sxs-lookup"><span data-stu-id="c1178-218">Parameters - object</span></span>

<span data-ttu-id="c1178-219">値</span><span class="sxs-lookup"><span data-stu-id="c1178-219">value</span></span>  

### <a name="return-value---object"></a><span data-ttu-id="c1178-220">戻り値 - object</span><span class="sxs-lookup"><span data-stu-id="c1178-220">Return Value - object</span></span>

<span data-ttu-id="c1178-221">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="c1178-221">The object that the MenuFunction class runs.</span></span>

### <a name="remarks---object"></a><span data-ttu-id="c1178-222">備考 - object</span><span class="sxs-lookup"><span data-stu-id="c1178-222">Remarks - object</span></span>

<span data-ttu-id="c1178-223">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="c1178-223">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="c1178-224">フォーム</span><span class="sxs-lookup"><span data-stu-id="c1178-224">Form</span></span>
-   <span data-ttu-id="c1178-225">報告</span><span class="sxs-lookup"><span data-stu-id="c1178-225">Report</span></span>
-   <span data-ttu-id="c1178-226">ジョブ</span><span class="sxs-lookup"><span data-stu-id="c1178-226">Job</span></span>
-   <span data-ttu-id="c1178-227">クラス</span><span class="sxs-lookup"><span data-stu-id="c1178-227">Class</span></span>
-   <span data-ttu-id="c1178-228">クエリ</span><span class="sxs-lookup"><span data-stu-id="c1178-228">Query</span></span>

## <a name="method-objecttype"></a><span data-ttu-id="c1178-229">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="c1178-229">Method objectType</span></span>

```xpp
public int objectType([int value])
```

### <a name="parameters---objecttype"></a><span data-ttu-id="c1178-230">パラメーター - objectType</span><span class="sxs-lookup"><span data-stu-id="c1178-230">Parameters - objectType</span></span>

<span data-ttu-id="c1178-231">値</span><span class="sxs-lookup"><span data-stu-id="c1178-231">value</span></span>  

### <a name="return-value---objecttype"></a><span data-ttu-id="c1178-232">戻り値 - objectType</span><span class="sxs-lookup"><span data-stu-id="c1178-232">Return Value - objectType</span></span>

## <a name="method-origin"></a><span data-ttu-id="c1178-233">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="c1178-233">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="c1178-234">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="c1178-234">Parameters - origin</span></span>

<span data-ttu-id="c1178-235">値</span><span class="sxs-lookup"><span data-stu-id="c1178-235">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="c1178-236">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="c1178-236">Return Value - origin</span></span>

## <a name="method-parameters"></a><span data-ttu-id="c1178-237">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="c1178-237">Method parameters</span></span>

<span data-ttu-id="c1178-238">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c1178-238">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="c1178-239">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="c1178-239">Parameters - parameters</span></span>

<span data-ttu-id="c1178-240">値</span><span class="sxs-lookup"><span data-stu-id="c1178-240">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="c1178-241">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="c1178-241">Return Value - parameters</span></span>

<span data-ttu-id="c1178-242">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="c1178-242">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="c1178-243">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="c1178-243">Remarks - parameters</span></span>

<span data-ttu-id="c1178-244">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="c1178-244">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="c1178-245">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="c1178-245">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-readpermissions"></a><span data-ttu-id="c1178-246">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-246">Method readPermissions</span></span>

```xpp
public int readPermissions([int value])
```

### <a name="parameters---readpermissions"></a><span data-ttu-id="c1178-247">パラメーター - readPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-247">Parameters - readPermissions</span></span>

<span data-ttu-id="c1178-248">値</span><span class="sxs-lookup"><span data-stu-id="c1178-248">value</span></span>  

### <a name="return-value---readpermissions"></a><span data-ttu-id="c1178-249">戻り値 - readPermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-249">Return Value - readPermissions</span></span>

## <a name="method-reportdesign"></a><span data-ttu-id="c1178-250">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="c1178-250">Method reportDesign</span></span>

```xpp
public str reportDesign([str value])
```

### <a name="parameters---reportdesign"></a><span data-ttu-id="c1178-251">パラメーター - reportDesign</span><span class="sxs-lookup"><span data-stu-id="c1178-251">Parameters - reportDesign</span></span>

<span data-ttu-id="c1178-252">値</span><span class="sxs-lookup"><span data-stu-id="c1178-252">value</span></span>  

### <a name="return-value---reportdesign"></a><span data-ttu-id="c1178-253">戻り値 - reportDesign</span><span class="sxs-lookup"><span data-stu-id="c1178-253">Return Value - reportDesign</span></span>

## <a name="method-runon"></a><span data-ttu-id="c1178-254">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="c1178-254">Method runOn</span></span>

```xpp
public int runOn([int value])
```

### <a name="parameters---runon"></a><span data-ttu-id="c1178-255">パラメーター - runOn</span><span class="sxs-lookup"><span data-stu-id="c1178-255">Parameters - runOn</span></span>

<span data-ttu-id="c1178-256">値</span><span class="sxs-lookup"><span data-stu-id="c1178-256">value</span></span>  

### <a name="return-value---runon"></a><span data-ttu-id="c1178-257">戻り値 - runOn</span><span class="sxs-lookup"><span data-stu-id="c1178-257">Return Value - runOn</span></span>

## <a name="method-updatepermissions"></a><span data-ttu-id="c1178-258">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-258">Method updatePermissions</span></span>

```xpp
public int updatePermissions([int value])
```

### <a name="parameters---updatepermissions"></a><span data-ttu-id="c1178-259">パラメーター - updatePermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-259">Parameters - updatePermissions</span></span>

<span data-ttu-id="c1178-260">値</span><span class="sxs-lookup"><span data-stu-id="c1178-260">value</span></span>  

### <a name="return-value---updatepermissions"></a><span data-ttu-id="c1178-261">戻り値 - updatePermissions</span><span class="sxs-lookup"><span data-stu-id="c1178-261">Return Value - updatePermissions</span></span>

## <a name="method-viewuserlicense"></a><span data-ttu-id="c1178-262">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="c1178-262">Method viewUserLicense</span></span>

<span data-ttu-id="c1178-263">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="c1178-263">Microsoft internal use only.</span></span>

```xpp
public int viewUserLicense([int value])
```

### <a name="parameters---viewuserlicense"></a><span data-ttu-id="c1178-264">パラメーター - viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="c1178-264">Parameters - viewUserLicense</span></span>

<span data-ttu-id="c1178-265">値</span><span class="sxs-lookup"><span data-stu-id="c1178-265">value</span></span>  
<span data-ttu-id="c1178-266">表示するユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="c1178-266">The user license to view.</span></span>

### <a name="return-value---viewuserlicense"></a><span data-ttu-id="c1178-267">戻り値 - viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="c1178-267">Return Value - viewUserLicense</span></span>

<span data-ttu-id="c1178-268">ユーザー ライセンス。</span><span class="sxs-lookup"><span data-stu-id="c1178-268">The user license.</span></span>

## <a name="method-runcalled"></a><span data-ttu-id="c1178-269">メソッド runCalled</span><span class="sxs-lookup"><span data-stu-id="c1178-269">Method runCalled</span></span>

```xpp
public static void runCalled(str name, [xArgs args])
```

### <a name="parameters---runcalled"></a><span data-ttu-id="c1178-270">パラメーター - runCalled</span><span class="sxs-lookup"><span data-stu-id="c1178-270">Parameters - runCalled</span></span>

<span data-ttu-id="c1178-271">名前</span><span class="sxs-lookup"><span data-stu-id="c1178-271">name</span></span>  

<!-- -->

<span data-ttu-id="c1178-272">args</span><span class="sxs-lookup"><span data-stu-id="c1178-272">args</span></span>  

## <a name="method-aotrun"></a><span data-ttu-id="c1178-273">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="c1178-273">Method AOTrun</span></span>

<span data-ttu-id="c1178-274">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="c1178-274">Compiles this node and its sub-tree in the Application Object Tree (AOT).</span></span>

```xpp
public void AOTrun([xArgs args])
```

### <a name="parameters---aotrun"></a><span data-ttu-id="c1178-275">パラメーター - AOTrun</span><span class="sxs-lookup"><span data-stu-id="c1178-275">Parameters - AOTrun</span></span>

<span data-ttu-id="c1178-276">args</span><span class="sxs-lookup"><span data-stu-id="c1178-276">args</span></span>  

## <a name="method-runclient"></a><span data-ttu-id="c1178-277">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="c1178-277">Method runClient</span></span>

```xpp
public static void runClient(str name, [xArgs args])
```

### <a name="parameters---runclient"></a><span data-ttu-id="c1178-278">パラメーター - runClient</span><span class="sxs-lookup"><span data-stu-id="c1178-278">Parameters - runClient</span></span>

<span data-ttu-id="c1178-279">名前</span><span class="sxs-lookup"><span data-stu-id="c1178-279">name</span></span>  

<!-- -->

<span data-ttu-id="c1178-280">args</span><span class="sxs-lookup"><span data-stu-id="c1178-280">args</span></span>  

## <a name="method-run"></a><span data-ttu-id="c1178-281">メソッド run</span><span class="sxs-lookup"><span data-stu-id="c1178-281">Method run</span></span>

```xpp
public void run([xArgs args])
```

### <a name="parameters---run"></a><span data-ttu-id="c1178-282">パラメーター - run</span><span class="sxs-lookup"><span data-stu-id="c1178-282">Parameters - run</span></span>

<span data-ttu-id="c1178-283">args</span><span class="sxs-lookup"><span data-stu-id="c1178-283">args</span></span>  

## <a name="method-new"></a><span data-ttu-id="c1178-284">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c1178-284">Method new</span></span>

<span data-ttu-id="c1178-285">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c1178-285">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str name)
```

### <a name="parameters---new"></a><span data-ttu-id="c1178-286">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c1178-286">Parameters - new</span></span>

<span data-ttu-id="c1178-287">名前</span><span class="sxs-lookup"><span data-stu-id="c1178-287">name</span></span>  

## <a name="method-runserver"></a><span data-ttu-id="c1178-288">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="c1178-288">Method runServer</span></span>

```xpp
public static void runServer(str name, [xArgs args])
```

### <a name="parameters---runserver"></a><span data-ttu-id="c1178-289">パラメーター - runServer</span><span class="sxs-lookup"><span data-stu-id="c1178-289">Parameters - runServer</span></span>

<span data-ttu-id="c1178-290">名前</span><span class="sxs-lookup"><span data-stu-id="c1178-290">name</span></span>  

<!-- -->

<span data-ttu-id="c1178-291">args</span><span class="sxs-lookup"><span data-stu-id="c1178-291">args</span></span>  

