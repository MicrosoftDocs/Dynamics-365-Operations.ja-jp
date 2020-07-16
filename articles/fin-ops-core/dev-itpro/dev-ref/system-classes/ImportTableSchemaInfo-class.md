---
title: ImportTableSchemaInfo クラス
description: このトピックでは、ImportTableSchemaInfo クラスについて説明します。
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
ms.openlocfilehash: fec4c4416668dfb00ea73e46c41cddcb2a00ec44
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502597"
---
# <a name="class-importtableschemainfo"></a><span data-ttu-id="b72af-103">クラス ImportTableSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="b72af-103">Class ImportTableSchemaInfo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ImportTableSchemaInfo extends Object
```

## <a name="remarks"></a><span data-ttu-id="b72af-104">備考</span><span class="sxs-lookup"><span data-stu-id="b72af-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b72af-105">例</span><span class="sxs-lookup"><span data-stu-id="b72af-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b72af-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b72af-106">Methods</span></span>

| <span data-ttu-id="b72af-107">方法</span><span class="sxs-lookup"><span data-stu-id="b72af-107">Method</span></span>                                                                             | <span data-ttu-id="b72af-108">説明</span><span class="sxs-lookup"><span data-stu-id="b72af-108">Description</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="b72af-109">public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)</span><span class="sxs-lookup"><span data-stu-id="b72af-109">public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)</span></span> |                                                 |
| <span data-ttu-id="b72af-110">public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)</span><span class="sxs-lookup"><span data-stu-id="b72af-110">public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)</span></span>        |                                                 |
| <span data-ttu-id="b72af-111">public int hasEqualityCriteria(boolean fHasEqualityCriteria)</span><span class="sxs-lookup"><span data-stu-id="b72af-111">public int hasEqualityCriteria(boolean fHasEqualityCriteria)</span></span>                       |                                                 |
| <span data-ttu-id="b72af-112">public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)</span><span class="sxs-lookup"><span data-stu-id="b72af-112">public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)</span></span>                 |                                                 |
| <span data-ttu-id="b72af-113">public void new(int usTableId)</span><span class="sxs-lookup"><span data-stu-id="b72af-113">public void new(int usTableId)</span></span>                                                     | <span data-ttu-id="b72af-114">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b72af-114">Initializes a new instance of the Object class.</span></span> |

## <a name="method-addcolumninfo"></a><span data-ttu-id="b72af-115">メソッド addColumnInfo</span><span class="sxs-lookup"><span data-stu-id="b72af-115">Method addColumnInfo</span></span>

```xpp
public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)
```

### <a name="parameters---addcolumninfo"></a><span data-ttu-id="b72af-116">パラメーター - addColumnInfo</span><span class="sxs-lookup"><span data-stu-id="b72af-116">Parameters - addColumnInfo</span></span>

<span data-ttu-id="b72af-117">szColName</span><span class="sxs-lookup"><span data-stu-id="b72af-117">szColName</span></span>  

<!-- -->

<span data-ttu-id="b72af-118">eColType</span><span class="sxs-lookup"><span data-stu-id="b72af-118">eColType</span></span>  

<!-- -->

<span data-ttu-id="b72af-119">eColRole</span><span class="sxs-lookup"><span data-stu-id="b72af-119">eColRole</span></span>  

<!-- -->

<span data-ttu-id="b72af-120">lColOrd</span><span class="sxs-lookup"><span data-stu-id="b72af-120">lColOrd</span></span>  

### <a name="return-value---addcolumninfo"></a><span data-ttu-id="b72af-121">戻り値 - addColumnInfo</span><span class="sxs-lookup"><span data-stu-id="b72af-121">Return Value - addColumnInfo</span></span>

## <a name="method-addcolumnmapping"></a><span data-ttu-id="b72af-122">メソッド addColumnMapping</span><span class="sxs-lookup"><span data-stu-id="b72af-122">Method addColumnMapping</span></span>

```xpp
public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)
```

### <a name="parameters---addcolumnmapping"></a><span data-ttu-id="b72af-123">戻り値 - addColumnMapping</span><span class="sxs-lookup"><span data-stu-id="b72af-123">Parameters - addColumnMapping</span></span>

<span data-ttu-id="b72af-124">szRefRecIdColName</span><span class="sxs-lookup"><span data-stu-id="b72af-124">szRefRecIdColName</span></span>  

<!-- -->

<span data-ttu-id="b72af-125">szRefTableIdColName</span><span class="sxs-lookup"><span data-stu-id="b72af-125">szRefTableIdColName</span></span>  

### <a name="return-value---addcolumnmapping"></a><span data-ttu-id="b72af-126">戻り値 - addColumnMapping</span><span class="sxs-lookup"><span data-stu-id="b72af-126">Return Value - addColumnMapping</span></span>

## <a name="method-hasequalitycriteria"></a><span data-ttu-id="b72af-127">メソッド hasEqualityCriteria</span><span class="sxs-lookup"><span data-stu-id="b72af-127">Method hasEqualityCriteria</span></span>

```xpp
public int hasEqualityCriteria(boolean fHasEqualityCriteria)
```

### <a name="parameters---hasequalitycriteria"></a><span data-ttu-id="b72af-128">パラメーター - hasEqualityCriteria</span><span class="sxs-lookup"><span data-stu-id="b72af-128">Parameters - hasEqualityCriteria</span></span>

<span data-ttu-id="b72af-129">fHasEqualityCriteria</span><span class="sxs-lookup"><span data-stu-id="b72af-129">fHasEqualityCriteria</span></span>  

### <a name="return-value---hasequalitycriteria"></a><span data-ttu-id="b72af-130">戻り値 - hasEqualityCriteria</span><span class="sxs-lookup"><span data-stu-id="b72af-130">Return Value - hasEqualityCriteria</span></span>

## <a name="method-shreddedmetadatatable"></a><span data-ttu-id="b72af-131">メソッド shreddedMetadataTable</span><span class="sxs-lookup"><span data-stu-id="b72af-131">Method shreddedMetadataTable</span></span>

```xpp
public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)
```

### <a name="parameters---shreddedmetadatatable"></a><span data-ttu-id="b72af-132">パラメーター - shreddedMetadataTable</span><span class="sxs-lookup"><span data-stu-id="b72af-132">Parameters - shreddedMetadataTable</span></span>

<span data-ttu-id="b72af-133">fIsShreddedMetadataTable</span><span class="sxs-lookup"><span data-stu-id="b72af-133">fIsShreddedMetadataTable</span></span>  

### <a name="return-value---shreddedmetadatatable"></a><span data-ttu-id="b72af-134">戻り値 - shreddedMetadataTable</span><span class="sxs-lookup"><span data-stu-id="b72af-134">Return Value - shreddedMetadataTable</span></span>

## <a name="method-new"></a><span data-ttu-id="b72af-135">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b72af-135">Method new</span></span>

<span data-ttu-id="b72af-136">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b72af-136">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(int usTableId)
```

### <a name="parameters---new"></a><span data-ttu-id="b72af-137">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="b72af-137">Parameters - new</span></span>

<span data-ttu-id="b72af-138">usTableId</span><span class="sxs-lookup"><span data-stu-id="b72af-138">usTableId</span></span>  

