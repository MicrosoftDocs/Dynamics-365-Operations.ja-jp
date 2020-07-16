---
title: DataEntityPersister クラス
description: このトピックでは、DataEntityPersister クラスについて説明します。
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
ms.openlocfilehash: 41f78007d70e0f0adb36c343d7344619dc158416
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502742"
---
# <a name="class-dataentitypersister"></a><span data-ttu-id="b4a12-103">クラス DataEntityPersister</span><span class="sxs-lookup"><span data-stu-id="b4a12-103">Class DataEntityPersister</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DataEntityPersister extends Object
```

## <a name="remarks"></a><span data-ttu-id="b4a12-104">備考</span><span class="sxs-lookup"><span data-stu-id="b4a12-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b4a12-105">例</span><span class="sxs-lookup"><span data-stu-id="b4a12-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b4a12-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b4a12-106">Methods</span></span>

| <span data-ttu-id="b4a12-107">方法</span><span class="sxs-lookup"><span data-stu-id="b4a12-107">Method</span></span>                                                                                                                                                                                                            | <span data-ttu-id="b4a12-108">説明</span><span class="sxs-lookup"><span data-stu-id="b4a12-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="b4a12-109">public boolean doSaveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-109">public boolean doSaveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                             |             |
| <span data-ttu-id="b4a12-110">public Common doFindDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-110">public Common doFindDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                              |             |
| <span data-ttu-id="b4a12-111">public boolean hasDataSourceRecordChanged(int dataSourceId, Common originalRecord, Common updatedRecord)</span><span class="sxs-lookup"><span data-stu-id="b4a12-111">public boolean hasDataSourceRecordChanged(int dataSourceId, Common originalRecord, Common updatedRecord)</span></span>                                                                                                          |             |
| <span data-ttu-id="b4a12-112">public str getCompanyForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)</span><span class="sxs-lookup"><span data-stu-id="b4a12-112">public str getCompanyForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)</span></span>                                                                                                                          |             |
| <span data-ttu-id="b4a12-113">public int getValidTimeStateUpdateModeForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)</span><span class="sxs-lookup"><span data-stu-id="b4a12-113">public int getValidTimeStateUpdateModeForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)</span></span>                                                                                                         |             |
| <span data-ttu-id="b4a12-114">public Common findDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-114">public Common findDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                                |             |
| <span data-ttu-id="b4a12-115">public boolean saveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-115">public boolean saveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                               |             |
| <span data-ttu-id="b4a12-116">public void doMapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-116">public void doMapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                         |             |
| <span data-ttu-id="b4a12-117">public void mapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-117">public void mapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                           |             |
| <span data-ttu-id="b4a12-118">public void doMapDataSourceToEntity(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-118">public void doMapDataSourceToEntity(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                         |             |
| <span data-ttu-id="b4a12-119">public void selectDataSourceBufferByRecId(Common dataSourceBuffer, Int64 dataSourceRecId, Boolean explicitlyForUpdate, Boolean fetchActiveRecordOnly)</span><span class="sxs-lookup"><span data-stu-id="b4a12-119">public void selectDataSourceBufferByRecId(Common dataSourceBuffer, Int64 dataSourceRecId, Boolean explicitlyForUpdate, Boolean fetchActiveRecordOnly)</span></span>                                                             |             |
| <span data-ttu-id="b4a12-120">public void doPersistEntity(DataEntityRuntimeContext entityCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-120">public void doPersistEntity(DataEntityRuntimeContext entityCtx)</span></span>                                                                                                                                                   |             |
| <span data-ttu-id="b4a12-121">public void doInitializeDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span><span class="sxs-lookup"><span data-stu-id="b4a12-121">public void doInitializeDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)</span></span>                                                                                          |             |
| <span data-ttu-id="b4a12-122">public void initializeDataSource(DataEntityRuntimeContext entityCtx, str dataSourceName, Common dataSourceBuffer, int dataSourceId, Boolean optional, Boolean readonly, Boolean oneToMany, Boolean dateEffective)</span><span class="sxs-lookup"><span data-stu-id="b4a12-122">public void initializeDataSource(DataEntityRuntimeContext entityCtx, str dataSourceName, Common dataSourceBuffer, int dataSourceId, Boolean optional, Boolean readonly, Boolean oneToMany, Boolean dateEffective)</span></span> |             |

## <a name="method-dosavedatasource"></a><span data-ttu-id="b4a12-123">メソッド doSaveDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-123">Method doSaveDataSource</span></span>

```xpp
public boolean doSaveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---dosavedatasource"></a><span data-ttu-id="b4a12-124">パラメーター - doSaveDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-124">Parameters - doSaveDataSource</span></span>

<span data-ttu-id="b4a12-125">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-125">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-126">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-126">dataSourceCtx</span></span>  

### <a name="return-value---dosavedatasource"></a><span data-ttu-id="b4a12-127">戻り値 - doSaveDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-127">Return Value - doSaveDataSource</span></span>

## <a name="method-dofinddatasource"></a><span data-ttu-id="b4a12-128">メソッド doFindDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-128">Method doFindDataSource</span></span>

```xpp
public Common doFindDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---dofinddatasource"></a><span data-ttu-id="b4a12-129">パラメーター - doFindDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-129">Parameters - doFindDataSource</span></span>

<span data-ttu-id="b4a12-130">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-130">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-131">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-131">dataSourceCtx</span></span>  

### <a name="return-value---dofinddatasource"></a><span data-ttu-id="b4a12-132">戻り値 - doFindDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-132">Return Value - doFindDataSource</span></span>

## <a name="method-hasdatasourcerecordchanged"></a><span data-ttu-id="b4a12-133">メソッド hasDataSourceRecordChanged</span><span class="sxs-lookup"><span data-stu-id="b4a12-133">Method hasDataSourceRecordChanged</span></span>

```xpp
public boolean hasDataSourceRecordChanged(int dataSourceId, Common originalRecord, Common updatedRecord)
```

### <a name="parameters---hasdatasourcerecordchanged"></a><span data-ttu-id="b4a12-134">パラメーター - hasDataSourceRecordChanged</span><span class="sxs-lookup"><span data-stu-id="b4a12-134">Parameters - hasDataSourceRecordChanged</span></span>

<span data-ttu-id="b4a12-135">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="b4a12-135">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="b4a12-136">originalRecord</span><span class="sxs-lookup"><span data-stu-id="b4a12-136">originalRecord</span></span>  

<!-- -->

<span data-ttu-id="b4a12-137">updatedRecord</span><span class="sxs-lookup"><span data-stu-id="b4a12-137">updatedRecord</span></span>  

### <a name="return-value---hasdatasourcerecordchanged"></a><span data-ttu-id="b4a12-138">戻り値 - hasDataSourceRecordChanged</span><span class="sxs-lookup"><span data-stu-id="b4a12-138">Return Value - hasDataSourceRecordChanged</span></span>

## <a name="method-getcompanyfordatasource"></a><span data-ttu-id="b4a12-139">メソッド getCompanyForDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-139">Method getCompanyForDataSource</span></span>

```xpp
public str getCompanyForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)
```

### <a name="parameters---getcompanyfordatasource"></a><span data-ttu-id="b4a12-140">パラメーター - getCompanyForDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-140">Parameters - getCompanyForDataSource</span></span>

<span data-ttu-id="b4a12-141">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-141">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-142">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="b4a12-142">dataSourceId</span></span>  

### <a name="return-value---getcompanyfordatasource"></a><span data-ttu-id="b4a12-143">戻り値 - getCompanyForDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-143">Return Value - getCompanyForDataSource</span></span>

## <a name="method-getvalidtimestateupdatemodefordatasource"></a><span data-ttu-id="b4a12-144">メソッド getValidTimeStateUpdateModeForDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-144">Method getValidTimeStateUpdateModeForDataSource</span></span>

```xpp
public int getValidTimeStateUpdateModeForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)
```

### <a name="parameters---getvalidtimestateupdatemodefordatasource"></a><span data-ttu-id="b4a12-145">パラメーター - getValidTimeStateUpdateModeForDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-145">Parameters - getValidTimeStateUpdateModeForDataSource</span></span>

<span data-ttu-id="b4a12-146">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-146">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-147">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="b4a12-147">dataSourceId</span></span>  

### <a name="return-value---getvalidtimestateupdatemodefordatasource"></a><span data-ttu-id="b4a12-148">戻り値 - getValidTimeStateUpdateModeForDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-148">Return Value - getValidTimeStateUpdateModeForDataSource</span></span>

## <a name="method-finddatasource"></a><span data-ttu-id="b4a12-149">メソッド findDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-149">Method findDataSource</span></span>

```xpp
public Common findDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---finddatasource"></a><span data-ttu-id="b4a12-150">パラメーター - findDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-150">Parameters - findDataSource</span></span>

<span data-ttu-id="b4a12-151">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-151">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-152">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-152">dataSourceCtx</span></span>  

### <a name="return-value---finddatasource"></a><span data-ttu-id="b4a12-153">戻り値 - findDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-153">Return Value - findDataSource</span></span>

## <a name="method-savedatasource"></a><span data-ttu-id="b4a12-154">メソッド saveDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-154">Method saveDataSource</span></span>

```xpp
public boolean saveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---savedatasource"></a><span data-ttu-id="b4a12-155">パラメーター - saveDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-155">Parameters - saveDataSource</span></span>

<span data-ttu-id="b4a12-156">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-156">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-157">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-157">dataSourceCtx</span></span>  

### <a name="return-value---savedatasource"></a><span data-ttu-id="b4a12-158">戻り値 - saveDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-158">Return Value - saveDataSource</span></span>

## <a name="method-domapentitytodatasource"></a><span data-ttu-id="b4a12-159">メソッド doMapEntityToDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-159">Method doMapEntityToDataSource</span></span>

```xpp
public void doMapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---domapentitytodatasource"></a><span data-ttu-id="b4a12-160">パラメーター - doMapEntityToDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-160">Parameters - doMapEntityToDataSource</span></span>

<span data-ttu-id="b4a12-161">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-161">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-162">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-162">dataSourceCtx</span></span>  

## <a name="method-mapentitytodatasource"></a><span data-ttu-id="b4a12-163">メソッド mapEntityToDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-163">Method mapEntityToDataSource</span></span>

```xpp
public void mapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---mapentitytodatasource"></a><span data-ttu-id="b4a12-164">パラメーター - mapEntityToDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-164">Parameters - mapEntityToDataSource</span></span>

<span data-ttu-id="b4a12-165">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-165">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-166">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-166">dataSourceCtx</span></span>  

## <a name="method-domapdatasourcetoentity"></a><span data-ttu-id="b4a12-167">メソッド doMapDataSourceToEntity</span><span class="sxs-lookup"><span data-stu-id="b4a12-167">Method doMapDataSourceToEntity</span></span>

```xpp
public void doMapDataSourceToEntity(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---domapdatasourcetoentity"></a><span data-ttu-id="b4a12-168">パラメーター - doMapDataSourceToEntity</span><span class="sxs-lookup"><span data-stu-id="b4a12-168">Parameters - doMapDataSourceToEntity</span></span>

<span data-ttu-id="b4a12-169">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-169">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-170">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-170">dataSourceCtx</span></span>  

## <a name="method-selectdatasourcebufferbyrecid"></a><span data-ttu-id="b4a12-171">メソッド selectDataSourceBufferByRecId</span><span class="sxs-lookup"><span data-stu-id="b4a12-171">Method selectDataSourceBufferByRecId</span></span>

```xpp
public void selectDataSourceBufferByRecId(Common dataSourceBuffer, Int64 dataSourceRecId, Boolean explicitlyForUpdate, Boolean fetchActiveRecordOnly)
```

### <a name="parameters---selectdatasourcebufferbyrecid"></a><span data-ttu-id="b4a12-172">パラメーター - selectDataSourceBufferByRecId</span><span class="sxs-lookup"><span data-stu-id="b4a12-172">Parameters - selectDataSourceBufferByRecId</span></span>

<span data-ttu-id="b4a12-173">dataSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="b4a12-173">dataSourceBuffer</span></span>  

<!-- -->

<span data-ttu-id="b4a12-174">dataSourceRecId</span><span class="sxs-lookup"><span data-stu-id="b4a12-174">dataSourceRecId</span></span>  

<!-- -->

<span data-ttu-id="b4a12-175">explicitlyForUpdate</span><span class="sxs-lookup"><span data-stu-id="b4a12-175">explicitlyForUpdate</span></span>  

<!-- -->

<span data-ttu-id="b4a12-176">fetchActiveRecordOnly</span><span class="sxs-lookup"><span data-stu-id="b4a12-176">fetchActiveRecordOnly</span></span>  

## <a name="method-dopersistentity"></a><span data-ttu-id="b4a12-177">メソッド doPersistEntity</span><span class="sxs-lookup"><span data-stu-id="b4a12-177">Method doPersistEntity</span></span>

```xpp
public void doPersistEntity(DataEntityRuntimeContext entityCtx)
```

### <a name="parameters---dopersistentity"></a><span data-ttu-id="b4a12-178">パラメーター - doPersistEntity</span><span class="sxs-lookup"><span data-stu-id="b4a12-178">Parameters - doPersistEntity</span></span>

<span data-ttu-id="b4a12-179">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-179">entityCtx</span></span>  

## <a name="method-doinitializedatasource"></a><span data-ttu-id="b4a12-180">メソッド doInitializeDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-180">Method doInitializeDataSource</span></span>

```xpp
public void doInitializeDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---doinitializedatasource"></a><span data-ttu-id="b4a12-181">パラメーター - doInitializeDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-181">Parameters - doInitializeDataSource</span></span>

<span data-ttu-id="b4a12-182">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-182">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-183">dataSourceCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-183">dataSourceCtx</span></span>  

## <a name="method-initializedatasource"></a><span data-ttu-id="b4a12-184">メソッド initializeDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-184">Method initializeDataSource</span></span>

```xpp
public void initializeDataSource(DataEntityRuntimeContext entityCtx, str dataSourceName, Common dataSourceBuffer, int dataSourceId, Boolean optional, Boolean readonly, Boolean oneToMany, Boolean dateEffective)
```

### <a name="parameters---initializedatasource"></a><span data-ttu-id="b4a12-185">パラメーター - initializeDataSource</span><span class="sxs-lookup"><span data-stu-id="b4a12-185">Parameters - initializeDataSource</span></span>

<span data-ttu-id="b4a12-186">entityCtx</span><span class="sxs-lookup"><span data-stu-id="b4a12-186">entityCtx</span></span>  

<!-- -->

<span data-ttu-id="b4a12-187">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="b4a12-187">dataSourceName</span></span>  

<!-- -->

<span data-ttu-id="b4a12-188">dataSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="b4a12-188">dataSourceBuffer</span></span>  

<!-- -->

<span data-ttu-id="b4a12-189">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="b4a12-189">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="b4a12-190">省略可</span><span class="sxs-lookup"><span data-stu-id="b4a12-190">optional</span></span>  

<!-- -->

<span data-ttu-id="b4a12-191">readonly</span><span class="sxs-lookup"><span data-stu-id="b4a12-191">readonly</span></span>  

<!-- -->

<span data-ttu-id="b4a12-192">oneToMany</span><span class="sxs-lookup"><span data-stu-id="b4a12-192">oneToMany</span></span>  

<!-- -->

<span data-ttu-id="b4a12-193">dateEffective</span><span class="sxs-lookup"><span data-stu-id="b4a12-193">dateEffective</span></span>  

