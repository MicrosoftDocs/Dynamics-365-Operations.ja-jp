---
title: xCompany クラス
description: このトピックでは、xCompany クラスについて説明します。
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
ms.openlocfilehash: 7760ce004fe45ba138e7aa727798d7cbe58ff5bb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502768"
---
# <a name="class-xcompany"></a><span data-ttu-id="3bbb2-103">クラス xCompany</span><span class="sxs-lookup"><span data-stu-id="3bbb2-103">Class xCompany</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xCompany extends Object
```

## <a name="remarks"></a><span data-ttu-id="3bbb2-104">備考</span><span class="sxs-lookup"><span data-stu-id="3bbb2-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3bbb2-105">例</span><span class="sxs-lookup"><span data-stu-id="3bbb2-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3bbb2-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3bbb2-106">Methods</span></span>

| <span data-ttu-id="3bbb2-107">方法</span><span class="sxs-lookup"><span data-stu-id="3bbb2-107">Method</span></span>                                                                              | <span data-ttu-id="3bbb2-108">説明</span><span class="sxs-lookup"><span data-stu-id="3bbb2-108">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="3bbb2-109">public DataAreaId dataArea(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="3bbb2-109">public DataAreaId dataArea(TableId tableId)</span></span>                                         |                                                    |
| <span data-ttu-id="3bbb2-110">public SelectableDataArea ext()</span><span class="sxs-lookup"><span data-stu-id="3bbb2-110">public SelectableDataArea ext()</span></span>                                                     |                                                    |
| <span data-ttu-id="3bbb2-111">public boolean log(DatabaseLogType typeOfLog, TableId tableId, \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="3bbb2-111">public boolean log(DatabaseLogType typeOfLog, TableId tableId, \[FieldId fieldId\])</span></span> |                                                    |
| <span data-ttu-id="3bbb2-112">public boolean logAlways(DatabaseLogType typeOfLog, \[boolean log\])</span><span class="sxs-lookup"><span data-stu-id="3bbb2-112">public boolean logAlways(DatabaseLogType typeOfLog, \[boolean log\])</span></span>                | <span data-ttu-id="3bbb2-113">システム以外のテーブルのログを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="3bbb2-113">Enables or disables logging for non-system tables.</span></span> |
| <span data-ttu-id="3bbb2-114">public boolean reindex(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="3bbb2-114">public boolean reindex(\[TableId tableId\])</span></span>                                         |                                                    |
| <span data-ttu-id="3bbb2-115">public void reloadLog()</span><span class="sxs-lookup"><span data-stu-id="3bbb2-115">public void reloadLog()</span></span>                                                             |                                                    |
| <span data-ttu-id="3bbb2-116">public void new(SelectableDataArea company)</span><span class="sxs-lookup"><span data-stu-id="3bbb2-116">public void new(SelectableDataArea company)</span></span>                                         | <span data-ttu-id="3bbb2-117">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3bbb2-117">Initializes a new instance of the Object class.</span></span>    |
| <span data-ttu-id="3bbb2-118">public void check()</span><span class="sxs-lookup"><span data-stu-id="3bbb2-118">public void check()</span></span>                                                                 |                                                    |
| <span data-ttu-id="3bbb2-119">public void reloadRights()</span><span class="sxs-lookup"><span data-stu-id="3bbb2-119">public void reloadRights()</span></span>                                                          |                                                    |
| <span data-ttu-id="3bbb2-120">public void flushCache(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="3bbb2-120">public void flushCache(TableId tableId)</span></span>                                             |                                                    |
| <span data-ttu-id="3bbb2-121">public void reloadTableCollections()</span><span class="sxs-lookup"><span data-stu-id="3bbb2-121">public void reloadTableCollections()</span></span>                                                |                                                    |

## <a name="method-dataarea"></a><span data-ttu-id="3bbb2-122">メソッド dataArea</span><span class="sxs-lookup"><span data-stu-id="3bbb2-122">Method dataArea</span></span>

```xpp
public DataAreaId dataArea(TableId tableId)
```

### <a name="parameters---dataarea"></a><span data-ttu-id="3bbb2-123">パラメーター - dataArea</span><span class="sxs-lookup"><span data-stu-id="3bbb2-123">Parameters - dataArea</span></span>

<span data-ttu-id="3bbb2-124">tableId</span><span class="sxs-lookup"><span data-stu-id="3bbb2-124">tableId</span></span>  

### <a name="return-value---dataarea"></a><span data-ttu-id="3bbb2-125">戻り値 - dataArea</span><span class="sxs-lookup"><span data-stu-id="3bbb2-125">Return Value - dataArea</span></span>

## <a name="method-ext"></a><span data-ttu-id="3bbb2-126">メソッド ext</span><span class="sxs-lookup"><span data-stu-id="3bbb2-126">Method ext</span></span>

```xpp
public SelectableDataArea ext()
```

### <a name="return-value---ext"></a><span data-ttu-id="3bbb2-127">戻り値 - ext</span><span class="sxs-lookup"><span data-stu-id="3bbb2-127">Return Value - ext</span></span>

## <a name="method-log"></a><span data-ttu-id="3bbb2-128">メソッド log</span><span class="sxs-lookup"><span data-stu-id="3bbb2-128">Method log</span></span>

```xpp
public boolean log(DatabaseLogType typeOfLog, TableId tableId, [FieldId fieldId])
```

### <a name="parameters---log"></a><span data-ttu-id="3bbb2-129">パラメーター - log</span><span class="sxs-lookup"><span data-stu-id="3bbb2-129">Parameters - log</span></span>

<span data-ttu-id="3bbb2-130">typeOfLog</span><span class="sxs-lookup"><span data-stu-id="3bbb2-130">typeOfLog</span></span>  

<!-- -->

<span data-ttu-id="3bbb2-131">tableId</span><span class="sxs-lookup"><span data-stu-id="3bbb2-131">tableId</span></span>  

<!-- -->

<span data-ttu-id="3bbb2-132">fieldId</span><span class="sxs-lookup"><span data-stu-id="3bbb2-132">fieldId</span></span>  

### <a name="return-value---log"></a><span data-ttu-id="3bbb2-133">戻り値 - log</span><span class="sxs-lookup"><span data-stu-id="3bbb2-133">Return Value - log</span></span>

## <a name="method-logalways"></a><span data-ttu-id="3bbb2-134">メソッド logAlways</span><span class="sxs-lookup"><span data-stu-id="3bbb2-134">Method logAlways</span></span>

<span data-ttu-id="3bbb2-135">システム以外のテーブルのログを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="3bbb2-135">Enables or disables logging for non-system tables.</span></span>

```xpp
public boolean logAlways(DatabaseLogType typeOfLog, [boolean log])
```

### <a name="parameters---logalways"></a><span data-ttu-id="3bbb2-136">パラメーター - logAlways</span><span class="sxs-lookup"><span data-stu-id="3bbb2-136">Parameters - logAlways</span></span>

<span data-ttu-id="3bbb2-137">typeOfLog</span><span class="sxs-lookup"><span data-stu-id="3bbb2-137">typeOfLog</span></span>  

<!-- -->

<span data-ttu-id="3bbb2-138">ログ</span><span class="sxs-lookup"><span data-stu-id="3bbb2-138">log</span></span>  

### <a name="return-value---logalways"></a><span data-ttu-id="3bbb2-139">戻り値 - logAlways</span><span class="sxs-lookup"><span data-stu-id="3bbb2-139">Return Value - logAlways</span></span>

<span data-ttu-id="3bbb2-140">呼び出し前の指定された操作のデータベース ロギングの状況。</span><span class="sxs-lookup"><span data-stu-id="3bbb2-140">The status of the database logging for the indicated operation before the call.</span></span>

### <a name="remarks---logalways"></a><span data-ttu-id="3bbb2-141">備考 - logAlways</span><span class="sxs-lookup"><span data-stu-id="3bbb2-141">Remarks - logAlways</span></span>

<span data-ttu-id="3bbb2-142">オプションの typeOfLog パラメーターがない場合、このメソッドは指定されたオペレーションのデータベース ログの状態をレポートします。</span><span class="sxs-lookup"><span data-stu-id="3bbb2-142">Without the optional typeOfLog parameter, this method will report the status of the database logging for the indicated operation.</span></span> <span data-ttu-id="3bbb2-143">オプションのパラメーターを指定する場合は、メソッドは CAS で保護されており、呼び出しコードは SysDatabaselogPermission をアサートする必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3bbb2-143">Note that if the optional parameter is provided, the method is guarded by CAS and the calling code must assert SysDatabaselogPermission.</span></span>

## <a name="method-reindex"></a><span data-ttu-id="3bbb2-144">メソッド reindex</span><span class="sxs-lookup"><span data-stu-id="3bbb2-144">Method reindex</span></span>

```xpp
public boolean reindex([TableId tableId])
```

### <a name="parameters---reindex"></a><span data-ttu-id="3bbb2-145">パラメーター - reindex</span><span class="sxs-lookup"><span data-stu-id="3bbb2-145">Parameters - reindex</span></span>

<span data-ttu-id="3bbb2-146">tableId</span><span class="sxs-lookup"><span data-stu-id="3bbb2-146">tableId</span></span>  

### <a name="return-value---reindex"></a><span data-ttu-id="3bbb2-147">戻り値 - reindex</span><span class="sxs-lookup"><span data-stu-id="3bbb2-147">Return Value - reindex</span></span>

## <a name="method-reloadlog"></a><span data-ttu-id="3bbb2-148">メソッド reloadLog</span><span class="sxs-lookup"><span data-stu-id="3bbb2-148">Method reloadLog</span></span>

```xpp
public void reloadLog()
```

## <a name="method-new"></a><span data-ttu-id="3bbb2-149">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3bbb2-149">Method new</span></span>

<span data-ttu-id="3bbb2-150">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3bbb2-150">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(SelectableDataArea company)
```

### <a name="parameters---new"></a><span data-ttu-id="3bbb2-151">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="3bbb2-151">Parameters - new</span></span>

<span data-ttu-id="3bbb2-152">会社</span><span class="sxs-lookup"><span data-stu-id="3bbb2-152">company</span></span>  

## <a name="method-check"></a><span data-ttu-id="3bbb2-153">メソッド check</span><span class="sxs-lookup"><span data-stu-id="3bbb2-153">Method check</span></span>

```xpp
public void check()
```

## <a name="method-reloadrights"></a><span data-ttu-id="3bbb2-154">メソッド reloadRights</span><span class="sxs-lookup"><span data-stu-id="3bbb2-154">Method reloadRights</span></span>

```xpp
public void reloadRights()
```

## <a name="method-flushcache"></a><span data-ttu-id="3bbb2-155">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="3bbb2-155">Method flushCache</span></span>

```xpp
public void flushCache(TableId tableId)
```

### <a name="parameters---flushcache"></a><span data-ttu-id="3bbb2-156">パラメーター - flushCache</span><span class="sxs-lookup"><span data-stu-id="3bbb2-156">Parameters - flushCache</span></span>

<span data-ttu-id="3bbb2-157">tableId</span><span class="sxs-lookup"><span data-stu-id="3bbb2-157">tableId</span></span>  

## <a name="method-reloadtablecollections"></a><span data-ttu-id="3bbb2-158">メソッド reloadTableCollections</span><span class="sxs-lookup"><span data-stu-id="3bbb2-158">Method reloadTableCollections</span></span>

```xpp
public void reloadTableCollections()
```

