---
title: DictCompositeDataEntity クラス
description: このトピックでは、DictCompositeDataEntity クラスについて説明します。
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
ms.openlocfilehash: 75ff38b93b57fbbac7673f063f3c43e787b20f1d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502726"
---
# <a name="class-dictcompositedataentity"></a><span data-ttu-id="50e3a-103">クラス DictCompositeDataEntity</span><span class="sxs-lookup"><span data-stu-id="50e3a-103">Class DictCompositeDataEntity</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictCompositeDataEntity extends Object
```

## <a name="remarks"></a><span data-ttu-id="50e3a-104">備考</span><span class="sxs-lookup"><span data-stu-id="50e3a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="50e3a-105">例</span><span class="sxs-lookup"><span data-stu-id="50e3a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="50e3a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="50e3a-106">Methods</span></span>

| <span data-ttu-id="50e3a-107">方法</span><span class="sxs-lookup"><span data-stu-id="50e3a-107">Method</span></span>                                                       | <span data-ttu-id="50e3a-108">説明</span><span class="sxs-lookup"><span data-stu-id="50e3a-108">Description</span></span> |
|--------------------------------------------------------------|-------------|
| <span data-ttu-id="50e3a-109">::public static List listOfCompositeDataEntities()</span><span class="sxs-lookup"><span data-stu-id="50e3a-109">::public static List listOfCompositeDataEntities()</span></span>           |             |
| <span data-ttu-id="50e3a-110">public str label()</span><span class="sxs-lookup"><span data-stu-id="50e3a-110">public str label()</span></span>                                           |             |
| <span data-ttu-id="50e3a-111">public boolean isReadOnly()</span><span class="sxs-lookup"><span data-stu-id="50e3a-111">public boolean isReadOnly()</span></span>                                  |             |
| <span data-ttu-id="50e3a-112">public str modules()</span><span class="sxs-lookup"><span data-stu-id="50e3a-112">public str modules()</span></span>                                         |             |
| <span data-ttu-id="50e3a-113">public str configurationKey()</span><span class="sxs-lookup"><span data-stu-id="50e3a-113">public str configurationKey()</span></span>                                |             |
| <span data-ttu-id="50e3a-114">public str countryRegionCodes()</span><span class="sxs-lookup"><span data-stu-id="50e3a-114">public str countryRegionCodes()</span></span>                              |             |
| <span data-ttu-id="50e3a-115">public str countryRegionContextField()</span><span class="sxs-lookup"><span data-stu-id="50e3a-115">public str countryRegionContextField()</span></span>                       |             |
| <span data-ttu-id="50e3a-116">public str developerDocumentation()</span><span class="sxs-lookup"><span data-stu-id="50e3a-116">public str developerDocumentation()</span></span>                          |             |
| <span data-ttu-id="50e3a-117">public EntityCategory entityCategory()</span><span class="sxs-lookup"><span data-stu-id="50e3a-117">public EntityCategory entityCategory()</span></span>                       |             |
| <span data-ttu-id="50e3a-118">public str formRef()</span><span class="sxs-lookup"><span data-stu-id="50e3a-118">public str formRef()</span></span>                                         |             |
| <span data-ttu-id="50e3a-119">public str singularLabel()</span><span class="sxs-lookup"><span data-stu-id="50e3a-119">public str singularLabel()</span></span>                                   |             |
| <span data-ttu-id="50e3a-120">public str tags()</span><span class="sxs-lookup"><span data-stu-id="50e3a-120">public str tags()</span></span>                                            |             |
| <span data-ttu-id="50e3a-121">public str publicCollectionName()</span><span class="sxs-lookup"><span data-stu-id="50e3a-121">public str publicCollectionName()</span></span>                            |             |
| <span data-ttu-id="50e3a-122">public str publicEntityName()</span><span class="sxs-lookup"><span data-stu-id="50e3a-122">public str publicEntityName()</span></span>                                |             |
| <span data-ttu-id="50e3a-123">public int dataEntityCount()</span><span class="sxs-lookup"><span data-stu-id="50e3a-123">public int dataEntityCount()</span></span>                                 |             |
| <span data-ttu-id="50e3a-124">public DictCompositeChildDataEntity childDataEntityNo(int n)</span><span class="sxs-lookup"><span data-stu-id="50e3a-124">public DictCompositeChildDataEntity childDataEntityNo(int n)</span></span> |             |
| <span data-ttu-id="50e3a-125">public void new(str compositeDataEntityName)</span><span class="sxs-lookup"><span data-stu-id="50e3a-125">public void new(str compositeDataEntityName)</span></span>                 |             |

## <a name="method-listofcompositedataentities"></a><span data-ttu-id="50e3a-126">メソッド listOfCompositeDataEntities</span><span class="sxs-lookup"><span data-stu-id="50e3a-126">Method listOfCompositeDataEntities</span></span>

```xpp
public static List listOfCompositeDataEntities()
```

### <a name="return-value---listofcompositedataentities"></a><span data-ttu-id="50e3a-127">戻り値 - listOfCompositeDataEntities</span><span class="sxs-lookup"><span data-stu-id="50e3a-127">Return Value - listOfCompositeDataEntities</span></span>

## <a name="method-label"></a><span data-ttu-id="50e3a-128">メソッド label</span><span class="sxs-lookup"><span data-stu-id="50e3a-128">Method label</span></span>

```xpp
public str label()
```

### <a name="return-value---label"></a><span data-ttu-id="50e3a-129">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="50e3a-129">Return Value - label</span></span>

## <a name="method-isreadonly"></a><span data-ttu-id="50e3a-130">メソッド isReadOnly</span><span class="sxs-lookup"><span data-stu-id="50e3a-130">Method isReadOnly</span></span>

```xpp
public boolean isReadOnly()
```

### <a name="return-value---isreadonly"></a><span data-ttu-id="50e3a-131">戻り値 - DictDataEntity</span><span class="sxs-lookup"><span data-stu-id="50e3a-131">Return Value - isReadOnly</span></span>

## <a name="method-modules"></a><span data-ttu-id="50e3a-132">メソッド modules</span><span class="sxs-lookup"><span data-stu-id="50e3a-132">Method modules</span></span>

```xpp
public str modules()
```

### <a name="return-value---modules"></a><span data-ttu-id="50e3a-133">戻り値 - modules</span><span class="sxs-lookup"><span data-stu-id="50e3a-133">Return Value - modules</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="50e3a-134">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="50e3a-134">Method configurationKey</span></span>

```xpp
public str configurationKey()
```

### <a name="return-value---configurationkey"></a><span data-ttu-id="50e3a-135">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="50e3a-135">Return Value - configurationKey</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="50e3a-136">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="50e3a-136">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes()
```

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="50e3a-137">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="50e3a-137">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="50e3a-138">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="50e3a-138">Method countryRegionContextField</span></span>

```xpp
public str countryRegionContextField()
```

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="50e3a-139">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="50e3a-139">Return Value - countryRegionContextField</span></span>

## <a name="method-developerdocumentation"></a><span data-ttu-id="50e3a-140">メソッド developerDocumentation</span><span class="sxs-lookup"><span data-stu-id="50e3a-140">Method developerDocumentation</span></span>

```xpp
public str developerDocumentation()
```

### <a name="return-value---developerdocumentation"></a><span data-ttu-id="50e3a-141">戻り値 - developerDocumentation</span><span class="sxs-lookup"><span data-stu-id="50e3a-141">Return Value - developerDocumentation</span></span>

## <a name="method-entitycategory"></a><span data-ttu-id="50e3a-142">メソッド entityCategory</span><span class="sxs-lookup"><span data-stu-id="50e3a-142">Method entityCategory</span></span>

```xpp
public EntityCategory entityCategory()
```

### <a name="return-value---entitycategory"></a><span data-ttu-id="50e3a-143">戻り値 - entityCategory</span><span class="sxs-lookup"><span data-stu-id="50e3a-143">Return Value - entityCategory</span></span>

## <a name="method-formref"></a><span data-ttu-id="50e3a-144">メソッド formRef</span><span class="sxs-lookup"><span data-stu-id="50e3a-144">Method formRef</span></span>

```xpp
public str formRef()
```

### <a name="return-value---formref"></a><span data-ttu-id="50e3a-145">戻り値 - formRef</span><span class="sxs-lookup"><span data-stu-id="50e3a-145">Return Value - formRef</span></span>

## <a name="method-singularlabel"></a><span data-ttu-id="50e3a-146">メソッド singularLabel</span><span class="sxs-lookup"><span data-stu-id="50e3a-146">Method singularLabel</span></span>

```xpp
public str singularLabel()
```

### <a name="return-value---singularlabel"></a><span data-ttu-id="50e3a-147">戻り値 - singularLabel</span><span class="sxs-lookup"><span data-stu-id="50e3a-147">Return Value - singularLabel</span></span>

## <a name="method-tags"></a><span data-ttu-id="50e3a-148">メソッド tags</span><span class="sxs-lookup"><span data-stu-id="50e3a-148">Method tags</span></span>

```xpp
public str tags()
```

### <a name="return-value---tags"></a><span data-ttu-id="50e3a-149">戻り値 - tags</span><span class="sxs-lookup"><span data-stu-id="50e3a-149">Return Value - tags</span></span>

## <a name="method-publiccollectionname"></a><span data-ttu-id="50e3a-150">メソッド publicCollectionName</span><span class="sxs-lookup"><span data-stu-id="50e3a-150">Method publicCollectionName</span></span>

```xpp
public str publicCollectionName()
```

### <a name="return-value---publiccollectionname"></a><span data-ttu-id="50e3a-151">戻り値 - publicCollectionName</span><span class="sxs-lookup"><span data-stu-id="50e3a-151">Return Value - publicCollectionName</span></span>

## <a name="method-publicentityname"></a><span data-ttu-id="50e3a-152">メソッド publicEntityName</span><span class="sxs-lookup"><span data-stu-id="50e3a-152">Method publicEntityName</span></span>

```xpp
public str publicEntityName()
```

### <a name="return-value---publicentityname"></a><span data-ttu-id="50e3a-153">戻り値 - publicEntityName</span><span class="sxs-lookup"><span data-stu-id="50e3a-153">Return Value - publicEntityName</span></span>

## <a name="method-dataentitycount"></a><span data-ttu-id="50e3a-154">メソッド dataEntityCount</span><span class="sxs-lookup"><span data-stu-id="50e3a-154">Method dataEntityCount</span></span>

```xpp
public int dataEntityCount()
```

### <a name="return-value---dataentitycount"></a><span data-ttu-id="50e3a-155">戻り値 - dataEntityCount</span><span class="sxs-lookup"><span data-stu-id="50e3a-155">Return Value - dataEntityCount</span></span>

## <a name="method-childdataentityno"></a><span data-ttu-id="50e3a-156">メソッド childDataEntityNo</span><span class="sxs-lookup"><span data-stu-id="50e3a-156">Method childDataEntityNo</span></span>

```xpp
public DictCompositeChildDataEntity childDataEntityNo(int n)
```

### <a name="parameters---childdataentityno"></a><span data-ttu-id="50e3a-157">パラメーター - childDataEntityNo</span><span class="sxs-lookup"><span data-stu-id="50e3a-157">Parameters - childDataEntityNo</span></span>

<span data-ttu-id="50e3a-158">n</span><span class="sxs-lookup"><span data-stu-id="50e3a-158">n</span></span>  

### <a name="return-value---childdataentityno"></a><span data-ttu-id="50e3a-159">戻り値 - childDataEntityNo</span><span class="sxs-lookup"><span data-stu-id="50e3a-159">Return Value - childDataEntityNo</span></span>

## <a name="method-new"></a><span data-ttu-id="50e3a-160">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50e3a-160">Method new</span></span>

```xpp
public void new(str compositeDataEntityName)
```

### <a name="parameters---new"></a><span data-ttu-id="50e3a-161">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="50e3a-161">Parameters - new</span></span>

<span data-ttu-id="50e3a-162">compositeDataEntityName</span><span class="sxs-lookup"><span data-stu-id="50e3a-162">compositeDataEntityName</span></span>  

