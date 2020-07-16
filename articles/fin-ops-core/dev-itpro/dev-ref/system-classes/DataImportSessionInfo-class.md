---
title: DataImportSessionInfo クラス
description: このトピックでは、DataImportSessionInfo クラスについて説明します。
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
ms.openlocfilehash: 58c63825f075ffe4ea1aa5218bdf4a5ff805b3b0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502737"
---
# <a name="class-dataimportsessioninfo"></a><span data-ttu-id="6b35f-103">クラス DataImportSessionInfo</span><span class="sxs-lookup"><span data-stu-id="6b35f-103">Class DataImportSessionInfo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DataImportSessionInfo extends Object
```

## <a name="remarks"></a><span data-ttu-id="6b35f-104">備考</span><span class="sxs-lookup"><span data-stu-id="6b35f-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="6b35f-105">例</span><span class="sxs-lookup"><span data-stu-id="6b35f-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6b35f-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="6b35f-106">Methods</span></span>

| <span data-ttu-id="6b35f-107">方法</span><span class="sxs-lookup"><span data-stu-id="6b35f-107">Method</span></span>                                                                         | <span data-ttu-id="6b35f-108">説明</span><span class="sxs-lookup"><span data-stu-id="6b35f-108">Description</span></span>                                     |
|--------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="6b35f-109">public int addImportTable(str szTabName, int ulTableId, boolean fAlwaysUpdate)</span><span class="sxs-lookup"><span data-stu-id="6b35f-109">public int addImportTable(str szTabName, int ulTableId, boolean fAlwaysUpdate)</span></span> |                                                 |
| <span data-ttu-id="6b35f-110">public int getCurrentProgress()</span><span class="sxs-lookup"><span data-stu-id="6b35f-110">public int getCurrentProgress()</span></span>                                                |                                                 |
| <span data-ttu-id="6b35f-111">public str getCurrentTable()</span><span class="sxs-lookup"><span data-stu-id="6b35f-111">public str getCurrentTable()</span></span>                                                   |                                                 |
| <span data-ttu-id="6b35f-112">public int setSourceGUID(Guid szSourceGUID)</span><span class="sxs-lookup"><span data-stu-id="6b35f-112">public int setSourceGUID(Guid szSourceGUID)</span></span>                                    |                                                 |
| <span data-ttu-id="6b35f-113">public int setSysDataImpLogId(int sysDataImpLogId)</span><span class="sxs-lookup"><span data-stu-id="6b35f-113">public int setSysDataImpLogId(int sysDataImpLogId)</span></span>                             |                                                 |
| <span data-ttu-id="6b35f-114">public void new(str szInpFileName, boolean fUpdateExistingData)</span><span class="sxs-lookup"><span data-stu-id="6b35f-114">public void new(str szInpFileName, boolean fUpdateExistingData)</span></span>                | <span data-ttu-id="6b35f-115">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6b35f-115">Initializes a new instance of the Object class.</span></span> |

## <a name="method-addimporttable"></a><span data-ttu-id="6b35f-116">メソッド addImportTable</span><span class="sxs-lookup"><span data-stu-id="6b35f-116">Method addImportTable</span></span>

```xpp
public int addImportTable(str szTabName, int ulTableId, boolean fAlwaysUpdate)
```

### <a name="parameters---addimporttable"></a><span data-ttu-id="6b35f-117">パラメーター - addImportTable</span><span class="sxs-lookup"><span data-stu-id="6b35f-117">Parameters - addImportTable</span></span>

<span data-ttu-id="6b35f-118">szTabName</span><span class="sxs-lookup"><span data-stu-id="6b35f-118">szTabName</span></span>  

<!-- -->

<span data-ttu-id="6b35f-119">ulTableId</span><span class="sxs-lookup"><span data-stu-id="6b35f-119">ulTableId</span></span>  

<!-- -->

<span data-ttu-id="6b35f-120">fAlwaysUpdate</span><span class="sxs-lookup"><span data-stu-id="6b35f-120">fAlwaysUpdate</span></span>  

### <a name="return-value---addimporttable"></a><span data-ttu-id="6b35f-121">戻り値 - addImportTable</span><span class="sxs-lookup"><span data-stu-id="6b35f-121">Return Value - addImportTable</span></span>

## <a name="method-getcurrentprogress"></a><span data-ttu-id="6b35f-122">メソッド getCurrentProgress</span><span class="sxs-lookup"><span data-stu-id="6b35f-122">Method getCurrentProgress</span></span>

```xpp
public int getCurrentProgress()
```

### <a name="return-value---getcurrentprogress"></a><span data-ttu-id="6b35f-123">戻り値 - getCurrentProgress</span><span class="sxs-lookup"><span data-stu-id="6b35f-123">Return Value - getCurrentProgress</span></span>

## <a name="method-getcurrenttable"></a><span data-ttu-id="6b35f-124">メソッド getCurrentTable</span><span class="sxs-lookup"><span data-stu-id="6b35f-124">Method getCurrentTable</span></span>

```xpp
public str getCurrentTable()
```

### <a name="return-value---getcurrenttable"></a><span data-ttu-id="6b35f-125">戻り値 - getCurrentTable</span><span class="sxs-lookup"><span data-stu-id="6b35f-125">Return Value - getCurrentTable</span></span>

## <a name="method-setsourceguid"></a><span data-ttu-id="6b35f-126">メソッド setSourceGUID</span><span class="sxs-lookup"><span data-stu-id="6b35f-126">Method setSourceGUID</span></span>

```xpp
public int setSourceGUID(Guid szSourceGUID)
```

### <a name="parameters---setsourceguid"></a><span data-ttu-id="6b35f-127">パラメーター - setSourceGUID</span><span class="sxs-lookup"><span data-stu-id="6b35f-127">Parameters - setSourceGUID</span></span>

<span data-ttu-id="6b35f-128">szSourceGUID</span><span class="sxs-lookup"><span data-stu-id="6b35f-128">szSourceGUID</span></span>  

### <a name="return-value---setsourceguid"></a><span data-ttu-id="6b35f-129">戻り値 - setSourceGUID</span><span class="sxs-lookup"><span data-stu-id="6b35f-129">Return Value - setSourceGUID</span></span>

## <a name="method-setsysdataimplogid"></a><span data-ttu-id="6b35f-130">メソッド setSysDataImpLogId</span><span class="sxs-lookup"><span data-stu-id="6b35f-130">Method setSysDataImpLogId</span></span>

```xpp
public int setSysDataImpLogId(int sysDataImpLogId)
```

### <a name="parameters---setsysdataimplogid"></a><span data-ttu-id="6b35f-131">パラメーター - setSysDataImpLogId</span><span class="sxs-lookup"><span data-stu-id="6b35f-131">Parameters - setSysDataImpLogId</span></span>

<span data-ttu-id="6b35f-132">sysDataImpLogId</span><span class="sxs-lookup"><span data-stu-id="6b35f-132">sysDataImpLogId</span></span>  

### <a name="return-value---setsysdataimplogid"></a><span data-ttu-id="6b35f-133">戻り値 - setSysDataImpLogId</span><span class="sxs-lookup"><span data-stu-id="6b35f-133">Return Value - setSysDataImpLogId</span></span>

## <a name="method-new"></a><span data-ttu-id="6b35f-134">メソッド new</span><span class="sxs-lookup"><span data-stu-id="6b35f-134">Method new</span></span>

<span data-ttu-id="6b35f-135">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6b35f-135">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(str szInpFileName, boolean fUpdateExistingData)
```

### <a name="parameters---new"></a><span data-ttu-id="6b35f-136">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="6b35f-136">Parameters - new</span></span>

<span data-ttu-id="6b35f-137">szInpFileName</span><span class="sxs-lookup"><span data-stu-id="6b35f-137">szInpFileName</span></span>  

<!-- -->

<span data-ttu-id="6b35f-138">fUpdateExistingData</span><span class="sxs-lookup"><span data-stu-id="6b35f-138">fUpdateExistingData</span></span>  

