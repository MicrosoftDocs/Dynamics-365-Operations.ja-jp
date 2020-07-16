---
title: DataImportManager クラス
description: このトピックでは、DataImportManager クラスについて説明します。
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
ms.openlocfilehash: e670942d98490cea0e8a505ff32a960eb9ccf284
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502738"
---
# <a name="class-dataimportmanager"></a><span data-ttu-id="3f0be-103">クラス DataImportManager</span><span class="sxs-lookup"><span data-stu-id="3f0be-103">Class DataImportManager</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DataImportManager extends Object
```

## <a name="remarks"></a><span data-ttu-id="3f0be-104">備考</span><span class="sxs-lookup"><span data-stu-id="3f0be-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3f0be-105">例</span><span class="sxs-lookup"><span data-stu-id="3f0be-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3f0be-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3f0be-106">Methods</span></span>

| <span data-ttu-id="3f0be-107">方法</span><span class="sxs-lookup"><span data-stu-id="3f0be-107">Method</span></span>                                                                                        | <span data-ttu-id="3f0be-108">説明</span><span class="sxs-lookup"><span data-stu-id="3f0be-108">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3f0be-109">::public static int commitImportSessionInfo(DataImportSessionInfo impInfo)</span><span class="sxs-lookup"><span data-stu-id="3f0be-109">::public static int commitImportSessionInfo(DataImportSessionInfo impInfo)</span></span>                    |                                                            |
| <span data-ttu-id="3f0be-110">::public static int endTableDataCopy(ImportTableDataInfo dataInfo)</span><span class="sxs-lookup"><span data-stu-id="3f0be-110">::public static int endTableDataCopy(ImportTableDataInfo dataInfo)</span></span>                            |                                                            |
| <span data-ttu-id="3f0be-111">::public static int endTableSchemaCopy(ImportTableSchemaInfo schInfo)</span><span class="sxs-lookup"><span data-stu-id="3f0be-111">::public static int endTableSchemaCopy(ImportTableSchemaInfo schInfo)</span></span>                         |                                                            |
| <span data-ttu-id="3f0be-112">::public static int finishMergeTableData()</span><span class="sxs-lookup"><span data-stu-id="3f0be-112">::public static int finishMergeTableData()</span></span>                                                    |                                                            |
| <span data-ttu-id="3f0be-113">::public static int getImportSessionProgress(DataImportSessionInfo impInfo)</span><span class="sxs-lookup"><span data-stu-id="3f0be-113">::public static int getImportSessionProgress(DataImportSessionInfo impInfo)</span></span>                   |                                                            |
| <span data-ttu-id="3f0be-114">::public static int mergeAllData()</span><span class="sxs-lookup"><span data-stu-id="3f0be-114">::public static int mergeAllData()</span></span>                                                            |                                                            |
| <span data-ttu-id="3f0be-115">::public static int mergeTableData(int mergeStep, TableId tableId, boolean updateHeartbeat)</span><span class="sxs-lookup"><span data-stu-id="3f0be-115">::public static int mergeTableData(int mergeStep, TableId tableId, boolean updateHeartbeat)</span></span>   |                                                            |
| <span data-ttu-id="3f0be-116">::public static int recoverImportSession(DataImportSessionInfo impInfo, boolean fTryToResume)</span><span class="sxs-lookup"><span data-stu-id="3f0be-116">::public static int recoverImportSession(DataImportSessionInfo impInfo, boolean fTryToResume)</span></span> |                                                            |
| <span data-ttu-id="3f0be-117">public void new()</span><span class="sxs-lookup"><span data-stu-id="3f0be-117">public void new()</span></span>                                                                             | <span data-ttu-id="3f0be-118">DataImportManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3f0be-118">Initializes a new instance of the DataImportManager class.</span></span> |

## <a name="method-commitimportsessioninfo"></a><span data-ttu-id="3f0be-119">メソッド commitImportSessionInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-119">Method commitImportSessionInfo</span></span>

```xpp
public static int commitImportSessionInfo(DataImportSessionInfo impInfo)
```

### <a name="parameters---commitimportsessioninfo"></a><span data-ttu-id="3f0be-120">パラメーター - commitImportSessionInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-120">Parameters - commitImportSessionInfo</span></span>

<span data-ttu-id="3f0be-121">impInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-121">impInfo</span></span>  

### <a name="return-value---commitimportsessioninfo"></a><span data-ttu-id="3f0be-122">戻り値 - commitImportSessionInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-122">Return Value - commitImportSessionInfo</span></span>

## <a name="method-endtabledatacopy"></a><span data-ttu-id="3f0be-123">メソッド endTableDataCopy</span><span class="sxs-lookup"><span data-stu-id="3f0be-123">Method endTableDataCopy</span></span>

```xpp
public static int endTableDataCopy(ImportTableDataInfo dataInfo)
```

### <a name="parameters---endtabledatacopy"></a><span data-ttu-id="3f0be-124">パラメーター - endTableDataCopy</span><span class="sxs-lookup"><span data-stu-id="3f0be-124">Parameters - endTableDataCopy</span></span>

<span data-ttu-id="3f0be-125">dataInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-125">dataInfo</span></span>  

### <a name="return-value---endtabledatacopy"></a><span data-ttu-id="3f0be-126">戻り値 - endTableDataCopy</span><span class="sxs-lookup"><span data-stu-id="3f0be-126">Return Value - endTableDataCopy</span></span>

## <a name="method-endtableschemacopy"></a><span data-ttu-id="3f0be-127">メソッド endTableSchemaCopy</span><span class="sxs-lookup"><span data-stu-id="3f0be-127">Method endTableSchemaCopy</span></span>

```xpp
public static int endTableSchemaCopy(ImportTableSchemaInfo schInfo)
```

### <a name="parameters---endtableschemacopy"></a><span data-ttu-id="3f0be-128">パラメーター - endTableSchemaCopy</span><span class="sxs-lookup"><span data-stu-id="3f0be-128">Parameters - endTableSchemaCopy</span></span>

<span data-ttu-id="3f0be-129">schInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-129">schInfo</span></span>  

### <a name="return-value---endtableschemacopy"></a><span data-ttu-id="3f0be-130">戻り値 - endTableSchemaCopy</span><span class="sxs-lookup"><span data-stu-id="3f0be-130">Return Value - endTableSchemaCopy</span></span>

## <a name="method-finishmergetabledata"></a><span data-ttu-id="3f0be-131">メソッド finishMergeTableData</span><span class="sxs-lookup"><span data-stu-id="3f0be-131">Method finishMergeTableData</span></span>

```xpp
public static int finishMergeTableData()
```

### <a name="return-value---finishmergetabledata"></a><span data-ttu-id="3f0be-132">戻り値 - finishMergeTableData</span><span class="sxs-lookup"><span data-stu-id="3f0be-132">Return Value - finishMergeTableData</span></span>

## <a name="method-getimportsessionprogress"></a><span data-ttu-id="3f0be-133">メソッド getImportSessionProgress</span><span class="sxs-lookup"><span data-stu-id="3f0be-133">Method getImportSessionProgress</span></span>

```xpp
public static int getImportSessionProgress(DataImportSessionInfo impInfo)
```

### <a name="parameters---getimportsessionprogress"></a><span data-ttu-id="3f0be-134">パラメーター - getImportSessionProgress</span><span class="sxs-lookup"><span data-stu-id="3f0be-134">Parameters - getImportSessionProgress</span></span>

<span data-ttu-id="3f0be-135">impInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-135">impInfo</span></span>  

### <a name="return-value---getimportsessionprogress"></a><span data-ttu-id="3f0be-136">戻り値 - getImportSessionProgress</span><span class="sxs-lookup"><span data-stu-id="3f0be-136">Return Value - getImportSessionProgress</span></span>

## <a name="method-mergealldata"></a><span data-ttu-id="3f0be-137">メソッド mergeAllData</span><span class="sxs-lookup"><span data-stu-id="3f0be-137">Method mergeAllData</span></span>

```xpp
public static int mergeAllData()
```

### <a name="return-value---mergealldata"></a><span data-ttu-id="3f0be-138">戻り値 - mergeAllData</span><span class="sxs-lookup"><span data-stu-id="3f0be-138">Return Value - mergeAllData</span></span>

## <a name="method-mergetabledata"></a><span data-ttu-id="3f0be-139">メソッド mergeTableData</span><span class="sxs-lookup"><span data-stu-id="3f0be-139">Method mergeTableData</span></span>

```xpp
public static int mergeTableData(int mergeStep, TableId tableId, boolean updateHeartbeat)
```

### <a name="parameters---mergetabledata"></a><span data-ttu-id="3f0be-140">パラメーター - mergeTableData</span><span class="sxs-lookup"><span data-stu-id="3f0be-140">Parameters - mergeTableData</span></span>

<span data-ttu-id="3f0be-141">mergeStep</span><span class="sxs-lookup"><span data-stu-id="3f0be-141">mergeStep</span></span>  

<!-- -->

<span data-ttu-id="3f0be-142">tableId</span><span class="sxs-lookup"><span data-stu-id="3f0be-142">tableId</span></span>  

<!-- -->

<span data-ttu-id="3f0be-143">updateHeartbeat</span><span class="sxs-lookup"><span data-stu-id="3f0be-143">updateHeartbeat</span></span>  

### <a name="return-value---mergetabledata"></a><span data-ttu-id="3f0be-144">戻り値 - mergeTableData</span><span class="sxs-lookup"><span data-stu-id="3f0be-144">Return Value - mergeTableData</span></span>

## <a name="method-recoverimportsession"></a><span data-ttu-id="3f0be-145">メソッド recoverImportSession</span><span class="sxs-lookup"><span data-stu-id="3f0be-145">Method recoverImportSession</span></span>

```xpp
public static int recoverImportSession(DataImportSessionInfo impInfo, boolean fTryToResume)
```

### <a name="parameters---recoverimportsession"></a><span data-ttu-id="3f0be-146">パラメーター - recoverImportSession</span><span class="sxs-lookup"><span data-stu-id="3f0be-146">Parameters - recoverImportSession</span></span>

<span data-ttu-id="3f0be-147">impInfo</span><span class="sxs-lookup"><span data-stu-id="3f0be-147">impInfo</span></span>  

<!-- -->

<span data-ttu-id="3f0be-148">fTryToResume</span><span class="sxs-lookup"><span data-stu-id="3f0be-148">fTryToResume</span></span>  

### <a name="return-value---recoverimportsession"></a><span data-ttu-id="3f0be-149">戻り値 - recoverImportSession</span><span class="sxs-lookup"><span data-stu-id="3f0be-149">Return Value - recoverImportSession</span></span>

## <a name="method-new"></a><span data-ttu-id="3f0be-150">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3f0be-150">Method new</span></span>

<span data-ttu-id="3f0be-151">DataImportManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3f0be-151">Initializes a new instance of the DataImportManager class.</span></span>

```xpp
public void new()
```

