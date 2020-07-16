---
title: IISPostedFile クラス
description: このトピックでは、IISPostedFile クラスについて説明します。
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
ms.openlocfilehash: 9bbcdbdbf1b442a9037ae59588849cefbe43407e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502604"
---
# <a name="class-iispostedfile"></a><span data-ttu-id="fe755-103">クラス IISPostedFile</span><span class="sxs-lookup"><span data-stu-id="fe755-103">Class IISPostedFile</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISPostedFile extends Object
```

## <a name="remarks"></a><span data-ttu-id="fe755-104">備考</span><span class="sxs-lookup"><span data-stu-id="fe755-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fe755-105">例</span><span class="sxs-lookup"><span data-stu-id="fe755-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fe755-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="fe755-106">Methods</span></span>

| <span data-ttu-id="fe755-107">方法</span><span class="sxs-lookup"><span data-stu-id="fe755-107">Method</span></span>                                 | <span data-ttu-id="fe755-108">説明</span><span class="sxs-lookup"><span data-stu-id="fe755-108">Description</span></span>                                            |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="fe755-109">public int contentLength()</span><span class="sxs-lookup"><span data-stu-id="fe755-109">public int contentLength()</span></span>             |                                                        |
| <span data-ttu-id="fe755-110">public str contentType()</span><span class="sxs-lookup"><span data-stu-id="fe755-110">public str contentType()</span></span>               |                                                        |
| <span data-ttu-id="fe755-111">public str fileName()</span><span class="sxs-lookup"><span data-stu-id="fe755-111">public str fileName()</span></span>                  |                                                        |
| <span data-ttu-id="fe755-112">public container read(int countToRead)</span><span class="sxs-lookup"><span data-stu-id="fe755-112">public container read(int countToRead)</span></span> |                                                        |
| <span data-ttu-id="fe755-113">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="fe755-113">public void finalize()</span></span>                 |                                                        |
| <span data-ttu-id="fe755-114">public void new()</span><span class="sxs-lookup"><span data-stu-id="fe755-114">public void new()</span></span>                      | <span data-ttu-id="fe755-115">IISPostedFile クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fe755-115">Initializes a new instance of the IISPostedFile class.</span></span> |

## <a name="method-contentlength"></a><span data-ttu-id="fe755-116">メソッド contentLength</span><span class="sxs-lookup"><span data-stu-id="fe755-116">Method contentLength</span></span>

```xpp
public int contentLength()
```

### <a name="return-value---contentlength"></a><span data-ttu-id="fe755-117">戻り値 - contentLength</span><span class="sxs-lookup"><span data-stu-id="fe755-117">Return Value - contentLength</span></span>

## <a name="method-contenttype"></a><span data-ttu-id="fe755-118">メソッド contentType</span><span class="sxs-lookup"><span data-stu-id="fe755-118">Method contentType</span></span>

```xpp
public str contentType()
```

### <a name="return-value---contenttype"></a><span data-ttu-id="fe755-119">戻り値 - contentType</span><span class="sxs-lookup"><span data-stu-id="fe755-119">Return Value - contentType</span></span>

## <a name="method-filename"></a><span data-ttu-id="fe755-120">メソッド fileName</span><span class="sxs-lookup"><span data-stu-id="fe755-120">Method fileName</span></span>

```xpp
public str fileName()
```

### <a name="return-value---filename"></a><span data-ttu-id="fe755-121">戻り値 - fileName</span><span class="sxs-lookup"><span data-stu-id="fe755-121">Return Value - fileName</span></span>

## <a name="method-read"></a><span data-ttu-id="fe755-122">メソッド read</span><span class="sxs-lookup"><span data-stu-id="fe755-122">Method read</span></span>

```xpp
public container read(int countToRead)
```

### <a name="parameters---read"></a><span data-ttu-id="fe755-123">パラメーター - read</span><span class="sxs-lookup"><span data-stu-id="fe755-123">Parameters - read</span></span>

<span data-ttu-id="fe755-124">countToRead</span><span class="sxs-lookup"><span data-stu-id="fe755-124">countToRead</span></span>  

### <a name="return-value---read"></a><span data-ttu-id="fe755-125">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="fe755-125">Return Value - read</span></span>

## <a name="method-finalize"></a><span data-ttu-id="fe755-126">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="fe755-126">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="fe755-127">メソッド new</span><span class="sxs-lookup"><span data-stu-id="fe755-127">Method new</span></span>

<span data-ttu-id="fe755-128">IISPostedFile クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fe755-128">Initializes a new instance of the IISPostedFile class.</span></span>

```xpp
public void new()
```

