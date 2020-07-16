---
title: xSqlEnumerator クラス
description: このトピックでは、xSqlEnumerator クラスについて説明します。
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
ms.openlocfilehash: 9dea15217df193f6ac20fc55c01453f50cf12c6d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502755"
---
# <a name="class-xsqlenumerator"></a><span data-ttu-id="9bc8a-103">クラス xSqlEnumerator</span><span class="sxs-lookup"><span data-stu-id="9bc8a-103">Class xSqlEnumerator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xSqlEnumerator extends Object
```

## <a name="remarks"></a><span data-ttu-id="9bc8a-104">備考</span><span class="sxs-lookup"><span data-stu-id="9bc8a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9bc8a-105">例</span><span class="sxs-lookup"><span data-stu-id="9bc8a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9bc8a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9bc8a-106">Methods</span></span>

| <span data-ttu-id="9bc8a-107">方法</span><span class="sxs-lookup"><span data-stu-id="9bc8a-107">Method</span></span>                                               | <span data-ttu-id="9bc8a-108">説明</span><span class="sxs-lookup"><span data-stu-id="9bc8a-108">Description</span></span>                                             |
|------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9bc8a-109">public str getConnStr(str database)</span><span class="sxs-lookup"><span data-stu-id="9bc8a-109">public str getConnStr(str database)</span></span>                  |                                                         |
| <span data-ttu-id="9bc8a-110">public List getDatabases(str server, \[str driver\])</span><span class="sxs-lookup"><span data-stu-id="9bc8a-110">public List getDatabases(str server, \[str driver\])</span></span> |                                                         |
| <span data-ttu-id="9bc8a-111">public List getServers(str driver)</span><span class="sxs-lookup"><span data-stu-id="9bc8a-111">public List getServers(str driver)</span></span>                   |                                                         |
| <span data-ttu-id="9bc8a-112">public void new()</span><span class="sxs-lookup"><span data-stu-id="9bc8a-112">public void new()</span></span>                                    | <span data-ttu-id="9bc8a-113">xSqlEnumerator クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9bc8a-113">Initializes a new instance of the xSqlEnumerator class.</span></span> |

## <a name="method-getconnstr"></a><span data-ttu-id="9bc8a-114">メソッド getConnStr</span><span class="sxs-lookup"><span data-stu-id="9bc8a-114">Method getConnStr</span></span>

```xpp
public str getConnStr(str database)
```

### <a name="parameters---getconnstr"></a><span data-ttu-id="9bc8a-115">パラメーター - getConnStr</span><span class="sxs-lookup"><span data-stu-id="9bc8a-115">Parameters - getConnStr</span></span>

<span data-ttu-id="9bc8a-116">データベース</span><span class="sxs-lookup"><span data-stu-id="9bc8a-116">database</span></span>  

### <a name="return-value---getconnstr"></a><span data-ttu-id="9bc8a-117">戻り値 - getConnStr</span><span class="sxs-lookup"><span data-stu-id="9bc8a-117">Return Value - getConnStr</span></span>

## <a name="method-getdatabases"></a><span data-ttu-id="9bc8a-118">メソッド getDatabases</span><span class="sxs-lookup"><span data-stu-id="9bc8a-118">Method getDatabases</span></span>

```xpp
public List getDatabases(str server, [str driver])
```

### <a name="parameters---getdatabases"></a><span data-ttu-id="9bc8a-119">パラメーター - getDatabases</span><span class="sxs-lookup"><span data-stu-id="9bc8a-119">Parameters - getDatabases</span></span>

<span data-ttu-id="9bc8a-120">server</span><span class="sxs-lookup"><span data-stu-id="9bc8a-120">server</span></span>  

<!-- -->

<span data-ttu-id="9bc8a-121">driver</span><span class="sxs-lookup"><span data-stu-id="9bc8a-121">driver</span></span>  

### <a name="return-value---getdatabases"></a><span data-ttu-id="9bc8a-122">戻り値 - getDatabases</span><span class="sxs-lookup"><span data-stu-id="9bc8a-122">Return Value - getDatabases</span></span>

## <a name="method-getservers"></a><span data-ttu-id="9bc8a-123">メソッド getServers</span><span class="sxs-lookup"><span data-stu-id="9bc8a-123">Method getServers</span></span>

```xpp
public List getServers(str driver)
```

### <a name="parameters---getservers"></a><span data-ttu-id="9bc8a-124">パラメーター - getServers</span><span class="sxs-lookup"><span data-stu-id="9bc8a-124">Parameters - getServers</span></span>

<span data-ttu-id="9bc8a-125">driver</span><span class="sxs-lookup"><span data-stu-id="9bc8a-125">driver</span></span>  

### <a name="return-value---getservers"></a><span data-ttu-id="9bc8a-126">戻り値 - getServers</span><span class="sxs-lookup"><span data-stu-id="9bc8a-126">Return Value - getServers</span></span>

## <a name="method-new"></a><span data-ttu-id="9bc8a-127">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9bc8a-127">Method new</span></span>

<span data-ttu-id="9bc8a-128">xSqlEnumerator クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9bc8a-128">Initializes a new instance of the xSqlEnumerator class.</span></span>

```xpp
public void new()
```

