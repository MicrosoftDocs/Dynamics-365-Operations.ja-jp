---
title: DataEntityRuntimeContext クラス
description: このトピックでは、DataEntityRuntimeContext クラスについて説明します。
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
ms.openlocfilehash: 856249f9c477c8600859bb89b3c41b02d47d3678
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502741"
---
# <a name="class-dataentityruntimecontext"></a><span data-ttu-id="54389-103">クラス DataEntityRuntimeContext</span><span class="sxs-lookup"><span data-stu-id="54389-103">Class DataEntityRuntimeContext</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DataEntityRuntimeContext extends Object
```

## <a name="remarks"></a><span data-ttu-id="54389-104">備考</span><span class="sxs-lookup"><span data-stu-id="54389-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="54389-105">例</span><span class="sxs-lookup"><span data-stu-id="54389-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="54389-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="54389-106">Methods</span></span>

| <span data-ttu-id="54389-107">方法</span><span class="sxs-lookup"><span data-stu-id="54389-107">Method</span></span>                                                                                               | <span data-ttu-id="54389-108">説明</span><span class="sxs-lookup"><span data-stu-id="54389-108">Description</span></span> |
|------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="54389-109">public DataEntityDatabaseOperation getDatabaseOperation()</span><span class="sxs-lookup"><span data-stu-id="54389-109">public DataEntityDatabaseOperation getDatabaseOperation()</span></span>                                            |             |
| <span data-ttu-id="54389-110">public AnyType getCustomProperty(str name)</span><span class="sxs-lookup"><span data-stu-id="54389-110">public AnyType getCustomProperty(str name)</span></span>                                                           |             |
| <span data-ttu-id="54389-111">public Common getEntityRecord()</span><span class="sxs-lookup"><span data-stu-id="54389-111">public Common getEntityRecord()</span></span>                                                                      |             |
| <span data-ttu-id="54389-112">public DataEntityDataSourceRuntimeContext getRuntimeContextByName(str datasourceName)</span><span class="sxs-lookup"><span data-stu-id="54389-112">public DataEntityDataSourceRuntimeContext getRuntimeContextByName(str datasourceName)</span></span>                |             |
| <span data-ttu-id="54389-113">public void new(DataEntityDatabaseOperation operation, Common record, DataEntityPersister persister)</span><span class="sxs-lookup"><span data-stu-id="54389-113">public void new(DataEntityDatabaseOperation operation, Common record, DataEntityPersister persister)</span></span> |             |
| <span data-ttu-id="54389-114">public void setCustomProperty(str name, AnyType obj)</span><span class="sxs-lookup"><span data-stu-id="54389-114">public void setCustomProperty(str name, AnyType obj)</span></span>                                                 |             |

## <a name="method-getdatabaseoperation"></a><span data-ttu-id="54389-115">メソッド getDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="54389-115">Method getDatabaseOperation</span></span>

```xpp
public DataEntityDatabaseOperation getDatabaseOperation()
```

### <a name="return-value---getdatabaseoperation"></a><span data-ttu-id="54389-116">戻り値 - getDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="54389-116">Return Value - getDatabaseOperation</span></span>

## <a name="method-getcustomproperty"></a><span data-ttu-id="54389-117">メソッド getCustomProperty</span><span class="sxs-lookup"><span data-stu-id="54389-117">Method getCustomProperty</span></span>

```xpp
public AnyType getCustomProperty(str name)
```

### <a name="parameters---getcustomproperty"></a><span data-ttu-id="54389-118">パラメーター - getCustomProperty</span><span class="sxs-lookup"><span data-stu-id="54389-118">Parameters - getCustomProperty</span></span>

<span data-ttu-id="54389-119">名前</span><span class="sxs-lookup"><span data-stu-id="54389-119">name</span></span>  

### <a name="return-value---getcustomproperty"></a><span data-ttu-id="54389-120">戻り値 - getCustomProperty</span><span class="sxs-lookup"><span data-stu-id="54389-120">Return Value - getCustomProperty</span></span>

## <a name="method-getentityrecord"></a><span data-ttu-id="54389-121">メソッド getEntityRecord</span><span class="sxs-lookup"><span data-stu-id="54389-121">Method getEntityRecord</span></span>

```xpp
public Common getEntityRecord()
```

### <a name="return-value---getentityrecord"></a><span data-ttu-id="54389-122">戻り値 - getEntityRecord</span><span class="sxs-lookup"><span data-stu-id="54389-122">Return Value - getEntityRecord</span></span>

## <a name="method-getruntimecontextbyname"></a><span data-ttu-id="54389-123">メソッド getRuntimeContextByName</span><span class="sxs-lookup"><span data-stu-id="54389-123">Method getRuntimeContextByName</span></span>

```xpp
public DataEntityDataSourceRuntimeContext getRuntimeContextByName(str datasourceName)
```

### <a name="parameters---getruntimecontextbyname"></a><span data-ttu-id="54389-124">パラメーター - getRuntimeContextByName</span><span class="sxs-lookup"><span data-stu-id="54389-124">Parameters - getRuntimeContextByName</span></span>

<span data-ttu-id="54389-125">datasourceName</span><span class="sxs-lookup"><span data-stu-id="54389-125">datasourceName</span></span>  

### <a name="return-value---getruntimecontextbyname"></a><span data-ttu-id="54389-126">戻り値 - getRuntimeContextByName</span><span class="sxs-lookup"><span data-stu-id="54389-126">Return Value - getRuntimeContextByName</span></span>

## <a name="method-new"></a><span data-ttu-id="54389-127">メソッド new</span><span class="sxs-lookup"><span data-stu-id="54389-127">Method new</span></span>

```xpp
public void new(DataEntityDatabaseOperation operation, Common record, DataEntityPersister persister)
```

### <a name="parameters---new"></a><span data-ttu-id="54389-128">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="54389-128">Parameters - new</span></span>

<span data-ttu-id="54389-129">工程</span><span class="sxs-lookup"><span data-stu-id="54389-129">operation</span></span>  

<!-- -->

<span data-ttu-id="54389-130">記録</span><span class="sxs-lookup"><span data-stu-id="54389-130">record</span></span>  

<!-- -->

<span data-ttu-id="54389-131">persister</span><span class="sxs-lookup"><span data-stu-id="54389-131">persister</span></span>  

## <a name="method-setcustomproperty"></a><span data-ttu-id="54389-132">メソッド setCustomProperty</span><span class="sxs-lookup"><span data-stu-id="54389-132">Method setCustomProperty</span></span>

```xpp
public void setCustomProperty(str name, AnyType obj)
```

### <a name="parameters---setcustomproperty"></a><span data-ttu-id="54389-133">パラメーター - setCustomProperty</span><span class="sxs-lookup"><span data-stu-id="54389-133">Parameters - setCustomProperty</span></span>

<span data-ttu-id="54389-134">名前</span><span class="sxs-lookup"><span data-stu-id="54389-134">name</span></span>  

<!-- -->

<span data-ttu-id="54389-135">obj</span><span class="sxs-lookup"><span data-stu-id="54389-135">obj</span></span>  

