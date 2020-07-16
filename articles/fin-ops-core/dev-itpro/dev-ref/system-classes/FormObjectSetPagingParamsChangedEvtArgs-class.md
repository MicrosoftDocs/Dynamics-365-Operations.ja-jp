---
title: FormObjectSetPagingParamsChangedEvtArgs クラス
description: このトピックでは、FormObjectSetPagingParamsChangedEvtArgs クラスについて説明します。
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
ms.openlocfilehash: 0a71f0871580cdbb2ed5dff255e3163638a5fb6c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502918"
---
# <a name="class-formobjectsetpagingparamschangedevtargs"></a><span data-ttu-id="eef79-103">クラス FormObjectSetPagingParamsChangedEvtArgs</span><span class="sxs-lookup"><span data-stu-id="eef79-103">Class FormObjectSetPagingParamsChangedEvtArgs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSetPagingParamsChangedEvtArgs extends ManagedEventArgs
```

## <a name="remarks"></a><span data-ttu-id="eef79-104">備考</span><span class="sxs-lookup"><span data-stu-id="eef79-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="eef79-105">例</span><span class="sxs-lookup"><span data-stu-id="eef79-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="eef79-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="eef79-106">Methods</span></span>

| <span data-ttu-id="eef79-107">方法</span><span class="sxs-lookup"><span data-stu-id="eef79-107">Method</span></span>                                                                  | <span data-ttu-id="eef79-108">説明</span><span class="sxs-lookup"><span data-stu-id="eef79-108">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="eef79-109">public int pageSize()</span><span class="sxs-lookup"><span data-stu-id="eef79-109">public int pageSize()</span></span>                                                   |                                                           |
| <span data-ttu-id="eef79-110">public boolean pagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="eef79-110">public boolean pagingEnabled()</span></span>                                          |                                                           |
| <span data-ttu-id="eef79-111">public int startRowIndex()</span><span class="sxs-lookup"><span data-stu-id="eef79-111">public int startRowIndex()</span></span>                                              |                                                           |
| <span data-ttu-id="eef79-112">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="eef79-112">public void finalize()</span></span>                                                  |                                                           |
| <span data-ttu-id="eef79-113">public void new(boolean pagingEnabled, int startRowIndex, int pageSize)</span><span class="sxs-lookup"><span data-stu-id="eef79-113">public void new(boolean pagingEnabled, int startRowIndex, int pageSize)</span></span> | <span data-ttu-id="eef79-114">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="eef79-114">Initializes a new instance of the ManagedEventArgs class.</span></span> |

## <a name="method-pagesize"></a><span data-ttu-id="eef79-115">メソッド pageSize</span><span class="sxs-lookup"><span data-stu-id="eef79-115">Method pageSize</span></span>

```xpp
public int pageSize()
```

### <a name="return-value---pagesize"></a><span data-ttu-id="eef79-116">戻り値 - pageSize</span><span class="sxs-lookup"><span data-stu-id="eef79-116">Return Value - pageSize</span></span>

## <a name="method-pagingenabled"></a><span data-ttu-id="eef79-117">メソッド pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="eef79-117">Method pagingEnabled</span></span>

```xpp
public boolean pagingEnabled()
```

### <a name="return-value---pagingenabled"></a><span data-ttu-id="eef79-118">戻り値 - pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="eef79-118">Return Value - pagingEnabled</span></span>

## <a name="method-startrowindex"></a><span data-ttu-id="eef79-119">メソッド startRowIndex</span><span class="sxs-lookup"><span data-stu-id="eef79-119">Method startRowIndex</span></span>

```xpp
public int startRowIndex()
```

### <a name="return-value---startrowindex"></a><span data-ttu-id="eef79-120">戻り値 - startRowIndex</span><span class="sxs-lookup"><span data-stu-id="eef79-120">Return Value - startRowIndex</span></span>

## <a name="method-finalize"></a><span data-ttu-id="eef79-121">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="eef79-121">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="eef79-122">メソッド new</span><span class="sxs-lookup"><span data-stu-id="eef79-122">Method new</span></span>

<span data-ttu-id="eef79-123">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="eef79-123">Initializes a new instance of the ManagedEventArgs class.</span></span>

```xpp
public void new(boolean pagingEnabled, int startRowIndex, int pageSize)
```

### <a name="parameters---new"></a><span data-ttu-id="eef79-124">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="eef79-124">Parameters - new</span></span>

<span data-ttu-id="eef79-125">pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="eef79-125">pagingEnabled</span></span>  

<!-- -->

<span data-ttu-id="eef79-126">startRowIndex</span><span class="sxs-lookup"><span data-stu-id="eef79-126">startRowIndex</span></span>  

<!-- -->

<span data-ttu-id="eef79-127">pageSize</span><span class="sxs-lookup"><span data-stu-id="eef79-127">pageSize</span></span>  

