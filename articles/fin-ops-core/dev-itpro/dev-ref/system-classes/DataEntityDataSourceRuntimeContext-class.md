---
title: DataEntityDataSourceRuntimeContext クラス
description: このトピックでは、DataEntityDataSourceRuntimeContext クラスについて説明します。
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
ms.openlocfilehash: 3c16464e20c3245a1a75f4ad82103238ed4e6f46
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502744"
---
# <a name="class-dataentitydatasourceruntimecontext"></a><span data-ttu-id="5413a-103">クラス DataEntityDataSourceRuntimeContext</span><span class="sxs-lookup"><span data-stu-id="5413a-103">Class DataEntityDataSourceRuntimeContext</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class DataEntityDataSourceRuntimeContext extends Object
```

## <a name="remarks"></a><span data-ttu-id="5413a-104">備考</span><span class="sxs-lookup"><span data-stu-id="5413a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="5413a-105">例</span><span class="sxs-lookup"><span data-stu-id="5413a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5413a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5413a-106">Methods</span></span>

| <span data-ttu-id="5413a-107">方法</span><span class="sxs-lookup"><span data-stu-id="5413a-107">Method</span></span>                                                                         | <span data-ttu-id="5413a-108">説明</span><span class="sxs-lookup"><span data-stu-id="5413a-108">Description</span></span> |
|--------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="5413a-109">public str name()</span><span class="sxs-lookup"><span data-stu-id="5413a-109">public str name()</span></span>                                                              |             |
| <span data-ttu-id="5413a-110">public int id()</span><span class="sxs-lookup"><span data-stu-id="5413a-110">public int id()</span></span>                                                                |             |
| <span data-ttu-id="5413a-111">public Common getBuffer()</span><span class="sxs-lookup"><span data-stu-id="5413a-111">public Common getBuffer()</span></span>                                                      |             |
| <span data-ttu-id="5413a-112">public DataEntityDatabaseOperation getDatabaseOperation()</span><span class="sxs-lookup"><span data-stu-id="5413a-112">public DataEntityDatabaseOperation getDatabaseOperation()</span></span>                      |             |
| <span data-ttu-id="5413a-113">public str getCompany()</span><span class="sxs-lookup"><span data-stu-id="5413a-113">public str getCompany()</span></span>                                                        |             |
| <span data-ttu-id="5413a-114">public boolean getDataSaved()</span><span class="sxs-lookup"><span data-stu-id="5413a-114">public boolean getDataSaved()</span></span>                                                  |             |
| <span data-ttu-id="5413a-115">public boolean skipDataMethods(\[boolean skip\])</span><span class="sxs-lookup"><span data-stu-id="5413a-115">public boolean skipDataMethods(\[boolean skip\])</span></span>                               |             |
| <span data-ttu-id="5413a-116">public boolean skipDeleteMethod(\[boolean b\])</span><span class="sxs-lookup"><span data-stu-id="5413a-116">public boolean skipDeleteMethod(\[boolean b\])</span></span>                                 |             |
| <span data-ttu-id="5413a-117">public boolean skipValidateWrite(\[boolean skip\])</span><span class="sxs-lookup"><span data-stu-id="5413a-117">public boolean skipValidateWrite(\[boolean skip\])</span></span>                             |             |
| <span data-ttu-id="5413a-118">public boolean skipValidateDelete(\[boolean skip\])</span><span class="sxs-lookup"><span data-stu-id="5413a-118">public boolean skipValidateDelete(\[boolean skip\])</span></span>                            |             |
| <span data-ttu-id="5413a-119">public boolean skipInitValue(\[boolean skip\])</span><span class="sxs-lookup"><span data-stu-id="5413a-119">public boolean skipInitValue(\[boolean skip\])</span></span>                                 |             |
| <span data-ttu-id="5413a-120">public boolean skipDefaultRow(\[boolean skip\])</span><span class="sxs-lookup"><span data-stu-id="5413a-120">public boolean skipDefaultRow(\[boolean skip\])</span></span>                                |             |
| <span data-ttu-id="5413a-121">public boolean readOnly()</span><span class="sxs-lookup"><span data-stu-id="5413a-121">public boolean readOnly()</span></span>                                                      |             |
| <span data-ttu-id="5413a-122">public boolean oneToMany()</span><span class="sxs-lookup"><span data-stu-id="5413a-122">public boolean oneToMany()</span></span>                                                     |             |
| <span data-ttu-id="5413a-123">public boolean optional()</span><span class="sxs-lookup"><span data-stu-id="5413a-123">public boolean optional()</span></span>                                                      |             |
| <span data-ttu-id="5413a-124">public boolean dateEffective()</span><span class="sxs-lookup"><span data-stu-id="5413a-124">public boolean dateEffective()</span></span>                                                 |             |
| <span data-ttu-id="5413a-125">public boolean conflictDetectionInvoked(\[boolean found\])</span><span class="sxs-lookup"><span data-stu-id="5413a-125">public boolean conflictDetectionInvoked(\[boolean found\])</span></span>                     |             |
| <span data-ttu-id="5413a-126">public void new(Common dataSourceBuffer, str dataSourceName, int dataSourceId)</span><span class="sxs-lookup"><span data-stu-id="5413a-126">public void new(Common dataSourceBuffer, str dataSourceName, int dataSourceId)</span></span> |             |
| <span data-ttu-id="5413a-127">public void setCompany(str company)</span><span class="sxs-lookup"><span data-stu-id="5413a-127">public void setCompany(str company)</span></span>                                            |             |
| <span data-ttu-id="5413a-128">public void setBuffer(Common buffer)</span><span class="sxs-lookup"><span data-stu-id="5413a-128">public void setBuffer(Common buffer)</span></span>                                           |             |
| <span data-ttu-id="5413a-129">public void setDatabaseOperation(DataEntityDatabaseOperation dbOperation)</span><span class="sxs-lookup"><span data-stu-id="5413a-129">public void setDatabaseOperation(DataEntityDatabaseOperation dbOperation)</span></span>      |             |
| <span data-ttu-id="5413a-130">public void setDataSaved(boolean saved)</span><span class="sxs-lookup"><span data-stu-id="5413a-130">public void setDataSaved(boolean saved)</span></span>                                        |             |

## <a name="method-name"></a><span data-ttu-id="5413a-131">メソッド名</span><span class="sxs-lookup"><span data-stu-id="5413a-131">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="5413a-132">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="5413a-132">Return Value - name</span></span>

## <a name="method-id"></a><span data-ttu-id="5413a-133">メソッド id</span><span class="sxs-lookup"><span data-stu-id="5413a-133">Method id</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="5413a-134">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="5413a-134">Return Value - id</span></span>

## <a name="method-getbuffer"></a><span data-ttu-id="5413a-135">メソッド getBuffer</span><span class="sxs-lookup"><span data-stu-id="5413a-135">Method getBuffer</span></span>

```xpp
public Common getBuffer()
```

### <a name="return-value---getbuffer"></a><span data-ttu-id="5413a-136">戻り値 - getBuffer</span><span class="sxs-lookup"><span data-stu-id="5413a-136">Return Value - getBuffer</span></span>

## <a name="method-getdatabaseoperation"></a><span data-ttu-id="5413a-137">メソッド getDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="5413a-137">Method getDatabaseOperation</span></span>

```xpp
public DataEntityDatabaseOperation getDatabaseOperation()
```

### <a name="return-value---getdatabaseoperation"></a><span data-ttu-id="5413a-138">戻り値 - getDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="5413a-138">Return Value - getDatabaseOperation</span></span>

## <a name="method-getcompany"></a><span data-ttu-id="5413a-139">メソッド getCompany</span><span class="sxs-lookup"><span data-stu-id="5413a-139">Method getCompany</span></span>

```xpp
public str getCompany()
```

### <a name="return-value---getcompany"></a><span data-ttu-id="5413a-140">戻り値 - getCompany</span><span class="sxs-lookup"><span data-stu-id="5413a-140">Return Value - getCompany</span></span>

## <a name="method-getdatasaved"></a><span data-ttu-id="5413a-141">メソッド getDataSaved</span><span class="sxs-lookup"><span data-stu-id="5413a-141">Method getDataSaved</span></span>

```xpp
public boolean getDataSaved()
```

### <a name="return-value---getdatasaved"></a><span data-ttu-id="5413a-142">戻り値 - getDataSaved</span><span class="sxs-lookup"><span data-stu-id="5413a-142">Return Value - getDataSaved</span></span>

## <a name="method-skipdatamethods"></a><span data-ttu-id="5413a-143">メソッド skipDataMethods</span><span class="sxs-lookup"><span data-stu-id="5413a-143">Method skipDataMethods</span></span>

```xpp
public boolean skipDataMethods([boolean skip])
```

### <a name="parameters---skipdatamethods"></a><span data-ttu-id="5413a-144">パラメーター - skipDataMethods</span><span class="sxs-lookup"><span data-stu-id="5413a-144">Parameters - skipDataMethods</span></span>

<span data-ttu-id="5413a-145">skip</span><span class="sxs-lookup"><span data-stu-id="5413a-145">skip</span></span>  

### <a name="return-value---skipdatamethods"></a><span data-ttu-id="5413a-146">戻り値 - skipDataMethods</span><span class="sxs-lookup"><span data-stu-id="5413a-146">Return Value - skipDataMethods</span></span>

## <a name="method-skipdeletemethod"></a><span data-ttu-id="5413a-147">メソッド skipDeleteMethod</span><span class="sxs-lookup"><span data-stu-id="5413a-147">Method skipDeleteMethod</span></span>

```xpp
public boolean skipDeleteMethod([boolean b])
```

### <a name="parameters---skipdeletemethod"></a><span data-ttu-id="5413a-148">パラメーター - skipDeleteMethod</span><span class="sxs-lookup"><span data-stu-id="5413a-148">Parameters - skipDeleteMethod</span></span>

<span data-ttu-id="5413a-149">b</span><span class="sxs-lookup"><span data-stu-id="5413a-149">b</span></span>  

### <a name="return-value---skipdeletemethod"></a><span data-ttu-id="5413a-150">戻り値 - skipDeleteMethod</span><span class="sxs-lookup"><span data-stu-id="5413a-150">Return Value - skipDeleteMethod</span></span>

## <a name="method-skipvalidatewrite"></a><span data-ttu-id="5413a-151">メソッド skipValidateWrite</span><span class="sxs-lookup"><span data-stu-id="5413a-151">Method skipValidateWrite</span></span>

```xpp
public boolean skipValidateWrite([boolean skip])
```

### <a name="parameters---skipvalidatewrite"></a><span data-ttu-id="5413a-152">パラメーター - skipValidateWrite</span><span class="sxs-lookup"><span data-stu-id="5413a-152">Parameters - skipValidateWrite</span></span>

<span data-ttu-id="5413a-153">skip</span><span class="sxs-lookup"><span data-stu-id="5413a-153">skip</span></span>  

### <a name="return-value---skipvalidatewrite"></a><span data-ttu-id="5413a-154">戻り値 - skipValidateWrite</span><span class="sxs-lookup"><span data-stu-id="5413a-154">Return Value - skipValidateWrite</span></span>

## <a name="method-skipvalidatedelete"></a><span data-ttu-id="5413a-155">メソッド skipValidateDelete</span><span class="sxs-lookup"><span data-stu-id="5413a-155">Method skipValidateDelete</span></span>

```xpp
public boolean skipValidateDelete([boolean skip])
```

### <a name="parameters---skipvalidatedelete"></a><span data-ttu-id="5413a-156">パラメーター - skipValidateDelete</span><span class="sxs-lookup"><span data-stu-id="5413a-156">Parameters - skipValidateDelete</span></span>

<span data-ttu-id="5413a-157">skip</span><span class="sxs-lookup"><span data-stu-id="5413a-157">skip</span></span>  

### <a name="return-value---skipvalidatedelete"></a><span data-ttu-id="5413a-158">戻り値 - skipValidateDelete</span><span class="sxs-lookup"><span data-stu-id="5413a-158">Return Value - skipValidateDelete</span></span>

## <a name="method-skipinitvalue"></a><span data-ttu-id="5413a-159">メソッド skipInitValue</span><span class="sxs-lookup"><span data-stu-id="5413a-159">Method skipInitValue</span></span>

```xpp
public boolean skipInitValue([boolean skip])
```

### <a name="parameters---skipinitvalue"></a><span data-ttu-id="5413a-160">パラメーター - skipInitValue</span><span class="sxs-lookup"><span data-stu-id="5413a-160">Parameters - skipInitValue</span></span>

<span data-ttu-id="5413a-161">skip</span><span class="sxs-lookup"><span data-stu-id="5413a-161">skip</span></span>  

### <a name="return-value---skipinitvalue"></a><span data-ttu-id="5413a-162">戻り値 - skipInitValue</span><span class="sxs-lookup"><span data-stu-id="5413a-162">Return Value - skipInitValue</span></span>

## <a name="method-skipdefaultrow"></a><span data-ttu-id="5413a-163">メソッド skipDefaultRow</span><span class="sxs-lookup"><span data-stu-id="5413a-163">Method skipDefaultRow</span></span>

```xpp
public boolean skipDefaultRow([boolean skip])
```

### <a name="parameters---skipdefaultrow"></a><span data-ttu-id="5413a-164">パラメーター - skipDefaultRow</span><span class="sxs-lookup"><span data-stu-id="5413a-164">Parameters - skipDefaultRow</span></span>

<span data-ttu-id="5413a-165">skip</span><span class="sxs-lookup"><span data-stu-id="5413a-165">skip</span></span>  

### <a name="return-value---skipdefaultrow"></a><span data-ttu-id="5413a-166">戻り値 - skipDefaultRow</span><span class="sxs-lookup"><span data-stu-id="5413a-166">Return Value - skipDefaultRow</span></span>

## <a name="method-readonly"></a><span data-ttu-id="5413a-167">メソッド readOnly</span><span class="sxs-lookup"><span data-stu-id="5413a-167">Method readOnly</span></span>

```xpp
public boolean readOnly()
```

### <a name="return-value---readonly"></a><span data-ttu-id="5413a-168">戻り値 - readOnly</span><span class="sxs-lookup"><span data-stu-id="5413a-168">Return Value - readOnly</span></span>

## <a name="method-onetomany"></a><span data-ttu-id="5413a-169">メソッド oneToMany</span><span class="sxs-lookup"><span data-stu-id="5413a-169">Method oneToMany</span></span>

```xpp
public boolean oneToMany()
```

### <a name="return-value---onetomany"></a><span data-ttu-id="5413a-170">戻り値 - oneToMany</span><span class="sxs-lookup"><span data-stu-id="5413a-170">Return Value - oneToMany</span></span>

## <a name="method-optional"></a><span data-ttu-id="5413a-171">メソッド optional</span><span class="sxs-lookup"><span data-stu-id="5413a-171">Method optional</span></span>

```xpp
public boolean optional()
```

### <a name="return-value---optional"></a><span data-ttu-id="5413a-172">戻り値 - optional</span><span class="sxs-lookup"><span data-stu-id="5413a-172">Return Value - optional</span></span>

## <a name="method-dateeffective"></a><span data-ttu-id="5413a-173">メソッド dateEffective</span><span class="sxs-lookup"><span data-stu-id="5413a-173">Method dateEffective</span></span>

```xpp
public boolean dateEffective()
```

### <a name="return-value---dateeffective"></a><span data-ttu-id="5413a-174">戻り値 - dateEffective</span><span class="sxs-lookup"><span data-stu-id="5413a-174">Return Value - dateEffective</span></span>

## <a name="method-conflictdetectioninvoked"></a><span data-ttu-id="5413a-175">メソッド conflictDetectionInvoked</span><span class="sxs-lookup"><span data-stu-id="5413a-175">Method conflictDetectionInvoked</span></span>

```xpp
public boolean conflictDetectionInvoked([boolean found])
```

### <a name="parameters---conflictdetectioninvoked"></a><span data-ttu-id="5413a-176">パラメーター - conflictDetectionInvoked</span><span class="sxs-lookup"><span data-stu-id="5413a-176">Parameters - conflictDetectionInvoked</span></span>

<span data-ttu-id="5413a-177">found</span><span class="sxs-lookup"><span data-stu-id="5413a-177">found</span></span>  

### <a name="return-value---conflictdetectioninvoked"></a><span data-ttu-id="5413a-178">戻り値 - conflictDetectionInvoked</span><span class="sxs-lookup"><span data-stu-id="5413a-178">Return Value - conflictDetectionInvoked</span></span>

## <a name="method-new"></a><span data-ttu-id="5413a-179">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5413a-179">Method new</span></span>

```xpp
public void new(Common dataSourceBuffer, str dataSourceName, int dataSourceId)
```

### <a name="parameters---new"></a><span data-ttu-id="5413a-180">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="5413a-180">Parameters - new</span></span>

<span data-ttu-id="5413a-181">dataSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="5413a-181">dataSourceBuffer</span></span>  

<!-- -->

<span data-ttu-id="5413a-182">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="5413a-182">dataSourceName</span></span>  

<!-- -->

<span data-ttu-id="5413a-183">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="5413a-183">dataSourceId</span></span>  

## <a name="method-setcompany"></a><span data-ttu-id="5413a-184">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="5413a-184">Method setCompany</span></span>

```xpp
public void setCompany(str company)
```

### <a name="parameters---setcompany"></a><span data-ttu-id="5413a-185">パラメーター - setCompany</span><span class="sxs-lookup"><span data-stu-id="5413a-185">Parameters - setCompany</span></span>

<span data-ttu-id="5413a-186">会社</span><span class="sxs-lookup"><span data-stu-id="5413a-186">company</span></span>  

## <a name="method-setbuffer"></a><span data-ttu-id="5413a-187">メソッド setBuffer</span><span class="sxs-lookup"><span data-stu-id="5413a-187">Method setBuffer</span></span>

```xpp
public void setBuffer(Common buffer)
```

### <a name="parameters---setbuffer"></a><span data-ttu-id="5413a-188">パラメーター - setBuffer</span><span class="sxs-lookup"><span data-stu-id="5413a-188">Parameters - setBuffer</span></span>

<span data-ttu-id="5413a-189">バッファ</span><span class="sxs-lookup"><span data-stu-id="5413a-189">buffer</span></span>  

## <a name="method-setdatabaseoperation"></a><span data-ttu-id="5413a-190">メソッド setDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="5413a-190">Method setDatabaseOperation</span></span>

```xpp
public void setDatabaseOperation(DataEntityDatabaseOperation dbOperation)
```

### <a name="parameters---setdatabaseoperation"></a><span data-ttu-id="5413a-191">パラメーター - setDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="5413a-191">Parameters - setDatabaseOperation</span></span>

<span data-ttu-id="5413a-192">dbOperation</span><span class="sxs-lookup"><span data-stu-id="5413a-192">dbOperation</span></span>  

## <a name="method-setdatasaved"></a><span data-ttu-id="5413a-193">メソッド setDataSaved</span><span class="sxs-lookup"><span data-stu-id="5413a-193">Method setDataSaved</span></span>

```xpp
public void setDataSaved(boolean saved)
```

### <a name="parameters---setdatasaved"></a><span data-ttu-id="5413a-194">パラメーター - setDataSaved</span><span class="sxs-lookup"><span data-stu-id="5413a-194">Parameters - setDataSaved</span></span>

<span data-ttu-id="5413a-195"> が保存されました</span><span class="sxs-lookup"><span data-stu-id="5413a-195">saved</span></span>  

