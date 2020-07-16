---
title: SecurityUtil クラス
description: このトピックでは、SecurityUtil クラスについて説明します。
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
ms.openlocfilehash: 5c464354beec197104248964067d25be851720a7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502810"
---
# <a name="class-securityutil"></a><span data-ttu-id="bfefb-103">クラス SecurityUtil</span><span class="sxs-lookup"><span data-stu-id="bfefb-103">Class SecurityUtil</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityUtil extends Object
```

## <a name="remarks"></a><span data-ttu-id="bfefb-104">備考</span><span class="sxs-lookup"><span data-stu-id="bfefb-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="bfefb-105">例</span><span class="sxs-lookup"><span data-stu-id="bfefb-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="bfefb-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="bfefb-106">Methods</span></span>

| <span data-ttu-id="bfefb-107">方法</span><span class="sxs-lookup"><span data-stu-id="bfefb-107">Method</span></span>                                                                                                                 | <span data-ttu-id="bfefb-108">説明</span><span class="sxs-lookup"><span data-stu-id="bfefb-108">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="bfefb-109">::public static boolean isImplicitFlushMode()</span><span class="sxs-lookup"><span data-stu-id="bfefb-109">::public static boolean isImplicitFlushMode()</span></span>                                                                          | <span data-ttu-id="bfefb-110">暗黙的なセキュリティ フラッシュ モードがオンであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-110">Indicates whether implicit security flushing mode is on.</span></span>                   |
| <span data-ttu-id="bfefb-111">::public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)</span><span class="sxs-lookup"><span data-stu-id="bfefb-111">::public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)</span></span> | <span data-ttu-id="bfefb-112">セキュリティ保護可能なオブジェクトのロール値の有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-112">Retrieves an effective access for role value of securable object.</span></span>          |
| <span data-ttu-id="bfefb-113">::public static container getRolePermissions(Int64 roleID)</span><span class="sxs-lookup"><span data-stu-id="bfefb-113">::public static container getRolePermissions(Int64 roleID)</span></span>                                                             | <span data-ttu-id="bfefb-114">セキュリティ保護可能なオブジェクトのコンテナーおよび有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-114">Gets a container of securable objects and their effective access.</span></span>          |
| <span data-ttu-id="bfefb-115">::public static boolean sysAdminMode(\[boolean active\])</span><span class="sxs-lookup"><span data-stu-id="bfefb-115">::public static boolean sysAdminMode(\[boolean active\])</span></span>                                                               | <span data-ttu-id="bfefb-116">セキュリティ管理者モードを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-116">Gets and sets the security administrator mode.</span></span>                             |
| <span data-ttu-id="bfefb-117">::public static void refreshRolePermissions(Int64 roleID)</span><span class="sxs-lookup"><span data-stu-id="bfefb-117">::public static void refreshRolePermissions(Int64 roleID)</span></span>                                                              | <span data-ttu-id="bfefb-118">セキュリティ保護可能なオブジェクトの指定されたロールの有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-118">Retrieves the effective access of a specified role for a securable object.</span></span> |
| <span data-ttu-id="bfefb-119">::public static void runSecondPassAutoInference()</span><span class="sxs-lookup"><span data-stu-id="bfefb-119">::public static void runSecondPassAutoInference()</span></span>                                                                      | <span data-ttu-id="bfefb-120">2 つ目の合格自動推定が実行されます。</span><span class="sxs-lookup"><span data-stu-id="bfefb-120">Runs the second pass auto inference.</span></span>                                       |
| <span data-ttu-id="bfefb-121">::public static void flushPermissions()</span><span class="sxs-lookup"><span data-stu-id="bfefb-121">::public static void flushPermissions()</span></span>                                                                                | <span data-ttu-id="bfefb-122">アクセス許可をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="bfefb-122">Flushes the permissions.</span></span>                                                   |
| <span data-ttu-id="bfefb-123">public void new()</span><span class="sxs-lookup"><span data-stu-id="bfefb-123">public void new()</span></span>                                                                                                      | <span data-ttu-id="bfefb-124">SecurityUtil クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-124">Initializes a new instance of the SecurityUtil class.</span></span>                      |
| <span data-ttu-id="bfefb-125">::public static void flushAll()</span><span class="sxs-lookup"><span data-stu-id="bfefb-125">::public static void flushAll()</span></span>                                                                                        |                                                                            |

## <a name="method-isimplicitflushmode"></a><span data-ttu-id="bfefb-126">メソッド isImplicitFlushMode</span><span class="sxs-lookup"><span data-stu-id="bfefb-126">Method isImplicitFlushMode</span></span>

<span data-ttu-id="bfefb-127">暗黙的なセキュリティ フラッシュ モードがオンであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-127">Indicates whether implicit security flushing mode is on.</span></span>

```xpp
public static boolean isImplicitFlushMode()
```

### <a name="return-value---isimplicitflushmode"></a><span data-ttu-id="bfefb-128">戻り値 - isImplicitFlushMode</span><span class="sxs-lookup"><span data-stu-id="bfefb-128">Return Value - isImplicitFlushMode</span></span>

<span data-ttu-id="bfefb-129">ブール値。</span><span class="sxs-lookup"><span data-stu-id="bfefb-129">A Boolean value.</span></span>

## <a name="method-getroleeffectiveaccess"></a><span data-ttu-id="bfefb-130">メソッド getRoleEffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="bfefb-130">Method getRoleEffectiveAccess</span></span>

<span data-ttu-id="bfefb-131">セキュリティ保護可能なオブジェクトのロール値の有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-131">Retrieves an effective access for role value of securable object.</span></span>

```xpp
public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)
```

### <a name="parameters---getroleeffectiveaccess"></a><span data-ttu-id="bfefb-132">パラメーター - getRoleEffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="bfefb-132">Parameters - getRoleEffectiveAccess</span></span>

<span data-ttu-id="bfefb-133">roleID</span><span class="sxs-lookup"><span data-stu-id="bfefb-133">roleID</span></span>  

<!-- -->

<span data-ttu-id="bfefb-134">secObjectName</span><span class="sxs-lookup"><span data-stu-id="bfefb-134">secObjectName</span></span>  

<!-- -->

<span data-ttu-id="bfefb-135">secObjectType</span><span class="sxs-lookup"><span data-stu-id="bfefb-135">secObjectType</span></span>  

<!-- -->

<span data-ttu-id="bfefb-136">secObjectChildName</span><span class="sxs-lookup"><span data-stu-id="bfefb-136">secObjectChildName</span></span>  

### <a name="return-value---getroleeffectiveaccess"></a><span data-ttu-id="bfefb-137">戻り値 - getRoleEffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="bfefb-137">Return Value - getRoleEffectiveAccess</span></span>

<span data-ttu-id="bfefb-138">有効なアクセス値。</span><span class="sxs-lookup"><span data-stu-id="bfefb-138">The effective access value.</span></span>

## <a name="method-getrolepermissions"></a><span data-ttu-id="bfefb-139">メソッド getRolePermissions</span><span class="sxs-lookup"><span data-stu-id="bfefb-139">Method getRolePermissions</span></span>

<span data-ttu-id="bfefb-140">セキュリティ保護可能なオブジェクトのコンテナーおよび有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-140">Gets a container of securable objects and their effective access.</span></span>

```xpp
public static container getRolePermissions(Int64 roleID)
```

### <a name="parameters---getrolepermissions"></a><span data-ttu-id="bfefb-141">パラメーター - getRolePermissions</span><span class="sxs-lookup"><span data-stu-id="bfefb-141">Parameters - getRolePermissions</span></span>

<span data-ttu-id="bfefb-142">roleID</span><span class="sxs-lookup"><span data-stu-id="bfefb-142">roleID</span></span>  
<span data-ttu-id="bfefb-143">ロール ID。</span><span class="sxs-lookup"><span data-stu-id="bfefb-143">The role ID.</span></span>

### <a name="return-value---getrolepermissions"></a><span data-ttu-id="bfefb-144">戻り値 - getRolePermissions</span><span class="sxs-lookup"><span data-stu-id="bfefb-144">Return Value - getRolePermissions</span></span>

<span data-ttu-id="bfefb-145">セキュリティ保護可能なオブジェクトのコンテナーと、有効なアクセスです。</span><span class="sxs-lookup"><span data-stu-id="bfefb-145">A container of securable objects and their effective access.</span></span>

## <a name="method-sysadminmode"></a><span data-ttu-id="bfefb-146">メソッド sysAdminMode</span><span class="sxs-lookup"><span data-stu-id="bfefb-146">Method sysAdminMode</span></span>

<span data-ttu-id="bfefb-147">セキュリティ管理者モードを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-147">Gets and sets the security administrator mode.</span></span>

```xpp
public static boolean sysAdminMode([boolean active])
```

### <a name="parameters---sysadminmode"></a><span data-ttu-id="bfefb-148">パラメーター - sysAdminMode</span><span class="sxs-lookup"><span data-stu-id="bfefb-148">Parameters - sysAdminMode</span></span>

<span data-ttu-id="bfefb-149">有効</span><span class="sxs-lookup"><span data-stu-id="bfefb-149">active</span></span>  
<span data-ttu-id="bfefb-150">ブール値。</span><span class="sxs-lookup"><span data-stu-id="bfefb-150">A Boolean value.</span></span>

### <a name="return-value---sysadminmode"></a><span data-ttu-id="bfefb-151">戻り値 - sysAdminMode</span><span class="sxs-lookup"><span data-stu-id="bfefb-151">Return Value - sysAdminMode</span></span>

<span data-ttu-id="bfefb-152">セキュリティ管理者モードの古い状態。</span><span class="sxs-lookup"><span data-stu-id="bfefb-152">The old state of the security administrator mode.</span></span>

## <a name="method-refreshrolepermissions"></a><span data-ttu-id="bfefb-153">メソッド refreshRolePermissions</span><span class="sxs-lookup"><span data-stu-id="bfefb-153">Method refreshRolePermissions</span></span>

<span data-ttu-id="bfefb-154">セキュリティ保護可能なオブジェクトの指定されたロールの有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-154">Retrieves the effective access of a specified role for a securable object.</span></span>

```xpp
public static void refreshRolePermissions(Int64 roleID)
```

### <a name="parameters---refreshrolepermissions"></a><span data-ttu-id="bfefb-155">パラメーター - refreshRolePermissions</span><span class="sxs-lookup"><span data-stu-id="bfefb-155">Parameters - refreshRolePermissions</span></span>

<span data-ttu-id="bfefb-156">roleID</span><span class="sxs-lookup"><span data-stu-id="bfefb-156">roleID</span></span>  

## <a name="method-runsecondpassautoinference"></a><span data-ttu-id="bfefb-157">メソッド runSecondPassAutoInference</span><span class="sxs-lookup"><span data-stu-id="bfefb-157">Method runSecondPassAutoInference</span></span>

<span data-ttu-id="bfefb-158">2 つ目の合格自動推定が実行されます。</span><span class="sxs-lookup"><span data-stu-id="bfefb-158">Runs the second pass auto inference.</span></span>

```xpp
public static void runSecondPassAutoInference()
```

## <a name="method-flushpermissions"></a><span data-ttu-id="bfefb-159">メソッド flushPermissions</span><span class="sxs-lookup"><span data-stu-id="bfefb-159">Method flushPermissions</span></span>

<span data-ttu-id="bfefb-160">アクセス許可をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="bfefb-160">Flushes the permissions.</span></span>

```xpp
public static void flushPermissions()
```

## <a name="method-new"></a><span data-ttu-id="bfefb-161">メソッド new</span><span class="sxs-lookup"><span data-stu-id="bfefb-161">Method new</span></span>

<span data-ttu-id="bfefb-162">SecurityUtil クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bfefb-162">Initializes a new instance of the SecurityUtil class.</span></span>

```xpp
public void new()
```

## <a name="method-flushall"></a><span data-ttu-id="bfefb-163">メソッド flushAll</span><span class="sxs-lookup"><span data-stu-id="bfefb-163">Method flushAll</span></span>

```xpp
public static void flushAll()
```

