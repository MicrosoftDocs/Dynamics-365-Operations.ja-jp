---
title: xExportToExcelController クラス
description: このトピックでは、xExportToExcelControlle クラスについて説明します。
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
ms.openlocfilehash: 531082acb9efccbfa5b799e1286129a828cee8a7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502681"
---
# <a name="class-xexporttoexcelcontroller"></a><span data-ttu-id="9903f-103">クラス xExportToExcelController</span><span class="sxs-lookup"><span data-stu-id="9903f-103">Class xExportToExcelController</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xExportToExcelController extends Object
```

## <a name="remarks"></a><span data-ttu-id="9903f-104">備考</span><span class="sxs-lookup"><span data-stu-id="9903f-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9903f-105">例</span><span class="sxs-lookup"><span data-stu-id="9903f-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9903f-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9903f-106">Methods</span></span>

| <span data-ttu-id="9903f-107">方法</span><span class="sxs-lookup"><span data-stu-id="9903f-107">Method</span></span>                                                                                                                             | <span data-ttu-id="9903f-108">説明</span><span class="sxs-lookup"><span data-stu-id="9903f-108">Description</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="9903f-109">public boolean export()</span><span class="sxs-lookup"><span data-stu-id="9903f-109">public boolean export()</span></span>                                                                                                            |             |
| <span data-ttu-id="9903f-110">public boolean exportGrid(FormGridControl gridControl, boolean onlyMarkedRows)</span><span class="sxs-lookup"><span data-stu-id="9903f-110">public boolean exportGrid(FormGridControl gridControl, boolean onlyMarkedRows)</span></span>                                                     |             |
| <span data-ttu-id="9903f-111">public boolean performStaticExport(xFormRun formRun, FormGridControl gridControl, System.IO.Stream stream, boolean onlyMarkedRows)</span><span class="sxs-lookup"><span data-stu-id="9903f-111">public boolean performStaticExport(xFormRun formRun, FormGridControl gridControl, System.IO.Stream stream, boolean onlyMarkedRows)</span></span> |             |
| <span data-ttu-id="9903f-112">public void new()</span><span class="sxs-lookup"><span data-stu-id="9903f-112">public void new()</span></span>                                                                                                                  |             |

## <a name="method-export"></a><span data-ttu-id="9903f-113">メソッド export</span><span class="sxs-lookup"><span data-stu-id="9903f-113">Method export</span></span>

```xpp
public boolean export()
```

### <a name="return-value---export"></a><span data-ttu-id="9903f-114">戻り値 - export</span><span class="sxs-lookup"><span data-stu-id="9903f-114">Return Value - export</span></span>

## <a name="method-exportgrid"></a><span data-ttu-id="9903f-115">メソッド exportGrid</span><span class="sxs-lookup"><span data-stu-id="9903f-115">Method exportGrid</span></span>

```xpp
public boolean exportGrid(FormGridControl gridControl, boolean onlyMarkedRows)
```

### <a name="parameters---exportgrid"></a><span data-ttu-id="9903f-116">パラメーター - exportGrid</span><span class="sxs-lookup"><span data-stu-id="9903f-116">Parameters - exportGrid</span></span>

<span data-ttu-id="9903f-117">gridControl</span><span class="sxs-lookup"><span data-stu-id="9903f-117">gridControl</span></span>  

<!-- -->

<span data-ttu-id="9903f-118">onlyMarkedRows</span><span class="sxs-lookup"><span data-stu-id="9903f-118">onlyMarkedRows</span></span>  

### <a name="return-value---exportgrid"></a><span data-ttu-id="9903f-119">戻り値 - exportGrid</span><span class="sxs-lookup"><span data-stu-id="9903f-119">Return Value - exportGrid</span></span>

## <a name="method-performstaticexport"></a><span data-ttu-id="9903f-120">メソッド performStaticExport</span><span class="sxs-lookup"><span data-stu-id="9903f-120">Method performStaticExport</span></span>

```xpp
public boolean performStaticExport(xFormRun formRun, FormGridControl gridControl, System.IO.Stream stream, boolean onlyMarkedRows)
```

### <a name="parameters---performstaticexport"></a><span data-ttu-id="9903f-121">パラメーター - performStaticExport</span><span class="sxs-lookup"><span data-stu-id="9903f-121">Parameters - performStaticExport</span></span>

<span data-ttu-id="9903f-122">formRun</span><span class="sxs-lookup"><span data-stu-id="9903f-122">formRun</span></span>  

<!-- -->

<span data-ttu-id="9903f-123">gridControl</span><span class="sxs-lookup"><span data-stu-id="9903f-123">gridControl</span></span>  

<!-- -->

<span data-ttu-id="9903f-124">stream</span><span class="sxs-lookup"><span data-stu-id="9903f-124">stream</span></span>  

<!-- -->

<span data-ttu-id="9903f-125">onlyMarkedRows</span><span class="sxs-lookup"><span data-stu-id="9903f-125">onlyMarkedRows</span></span>  

### <a name="return-value---performstaticexport"></a><span data-ttu-id="9903f-126">戻り値 - performStaticExport</span><span class="sxs-lookup"><span data-stu-id="9903f-126">Return Value - performStaticExport</span></span>

## <a name="method-new"></a><span data-ttu-id="9903f-127">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9903f-127">Method new</span></span>

```xpp
public void new()
```

