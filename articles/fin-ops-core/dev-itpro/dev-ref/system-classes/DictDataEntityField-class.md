---
title: DictDataEntityField クラス
description: このトピックでは、DictDataEntityField クラスについて説明します。
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
ms.openlocfilehash: 3336006f589102b5abbbae6375edfa69866e7eb1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502989"
---
# <a name="class-dictdataentityfield"></a><span data-ttu-id="fbdc8-103">クラス DictDataEntityField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-103">Class DictDataEntityField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictDataEntityField extends DictField
```

## <a name="remarks"></a><span data-ttu-id="fbdc8-104">備考</span><span class="sxs-lookup"><span data-stu-id="fbdc8-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fbdc8-105">例</span><span class="sxs-lookup"><span data-stu-id="fbdc8-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fbdc8-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="fbdc8-106">Methods</span></span>

| <span data-ttu-id="fbdc8-107">方法</span><span class="sxs-lookup"><span data-stu-id="fbdc8-107">Method</span></span>                                                                | <span data-ttu-id="fbdc8-108">説明</span><span class="sxs-lookup"><span data-stu-id="fbdc8-108">Description</span></span> |
|-----------------------------------------------------------------------|-------------|
| <span data-ttu-id="fbdc8-109">public FieldAccessModifier accessModifier()</span><span class="sxs-lookup"><span data-stu-id="fbdc8-109">public FieldAccessModifier accessModifier()</span></span>                           |             |
| <span data-ttu-id="fbdc8-110">public str dataEntityViewMethod()</span><span class="sxs-lookup"><span data-stu-id="fbdc8-110">public str dataEntityViewMethod()</span></span>                                     |             |
| <span data-ttu-id="fbdc8-111">public str dataField()</span><span class="sxs-lookup"><span data-stu-id="fbdc8-111">public str dataField()</span></span>                                                |             |
| <span data-ttu-id="fbdc8-112">public str dataSource()</span><span class="sxs-lookup"><span data-stu-id="fbdc8-112">public str dataSource()</span></span>                                               |             |
| <span data-ttu-id="fbdc8-113">public str dimensionLegalEntityContextField()</span><span class="sxs-lookup"><span data-stu-id="fbdc8-113">public str dimensionLegalEntityContextField()</span></span>                         |             |
| <span data-ttu-id="fbdc8-114">public str dynamicDimensionEnumerationField()</span><span class="sxs-lookup"><span data-stu-id="fbdc8-114">public str dynamicDimensionEnumerationField()</span></span>                         |             |
| <span data-ttu-id="fbdc8-115">public boolean IsComputedField()</span><span class="sxs-lookup"><span data-stu-id="fbdc8-115">public boolean IsComputedField()</span></span>                                      |             |
| <span data-ttu-id="fbdc8-116">public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fbdc8-116">public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\])</span></span> |             |

## <a name="method-accessmodifier"></a><span data-ttu-id="fbdc8-117">メソッド accessModifier</span><span class="sxs-lookup"><span data-stu-id="fbdc8-117">Method accessModifier</span></span>

```xpp
public FieldAccessModifier accessModifier()
```

### <a name="return-value---accessmodifier"></a><span data-ttu-id="fbdc8-118">戻り値 - accessModifier</span><span class="sxs-lookup"><span data-stu-id="fbdc8-118">Return Value - accessModifier</span></span>

## <a name="method-dataentityviewmethod"></a><span data-ttu-id="fbdc8-119">メソッド dataEntityViewMethod</span><span class="sxs-lookup"><span data-stu-id="fbdc8-119">Method dataEntityViewMethod</span></span>

```xpp
public str dataEntityViewMethod()
```

### <a name="return-value---dataentityviewmethod"></a><span data-ttu-id="fbdc8-120">戻り値 - dataEntityViewMethod</span><span class="sxs-lookup"><span data-stu-id="fbdc8-120">Return Value - dataEntityViewMethod</span></span>

## <a name="method-datafield"></a><span data-ttu-id="fbdc8-121">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-121">Method dataField</span></span>

```xpp
public str dataField()
```

### <a name="return-value---datafield"></a><span data-ttu-id="fbdc8-122">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-122">Return Value - dataField</span></span>

## <a name="method-datasource"></a><span data-ttu-id="fbdc8-123">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="fbdc8-123">Method dataSource</span></span>

```xpp
public str dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="fbdc8-124">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="fbdc8-124">Return Value - dataSource</span></span>

## <a name="method-dimensionlegalentitycontextfield"></a><span data-ttu-id="fbdc8-125">メソッド dimensionLegalEntityContextField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-125">Method dimensionLegalEntityContextField</span></span>

```xpp
public str dimensionLegalEntityContextField()
```

### <a name="return-value---dimensionlegalentitycontextfield"></a><span data-ttu-id="fbdc8-126">戻り値 - dimensionLegalEntityContextField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-126">Return Value - dimensionLegalEntityContextField</span></span>

## <a name="method-dynamicdimensionenumerationfield"></a><span data-ttu-id="fbdc8-127">メソッド dynamicDimensionEnumerationField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-127">Method dynamicDimensionEnumerationField</span></span>

```xpp
public str dynamicDimensionEnumerationField()
```

### <a name="return-value---dynamicdimensionenumerationfield"></a><span data-ttu-id="fbdc8-128">戻り値 - dynamicDimensionEnumerationField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-128">Return Value - dynamicDimensionEnumerationField</span></span>

## <a name="method-iscomputedfield"></a><span data-ttu-id="fbdc8-129">メソッド IsComputedField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-129">Method IsComputedField</span></span>

```xpp
public boolean IsComputedField()
```

### <a name="return-value---iscomputedfield"></a><span data-ttu-id="fbdc8-130">戻り値 - IsComputedField</span><span class="sxs-lookup"><span data-stu-id="fbdc8-130">Return Value - IsComputedField</span></span>

## <a name="method-new"></a><span data-ttu-id="fbdc8-131">メソッド new</span><span class="sxs-lookup"><span data-stu-id="fbdc8-131">Method new</span></span>

```xpp
public void new(TableId tableId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---new"></a><span data-ttu-id="fbdc8-132">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="fbdc8-132">Parameters - new</span></span>

<span data-ttu-id="fbdc8-133">tableId</span><span class="sxs-lookup"><span data-stu-id="fbdc8-133">tableId</span></span>  

<!-- -->

<span data-ttu-id="fbdc8-134">fieldId</span><span class="sxs-lookup"><span data-stu-id="fbdc8-134">fieldId</span></span>  

<!-- -->

<span data-ttu-id="fbdc8-135">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fbdc8-135">arrayIndex</span></span>  

