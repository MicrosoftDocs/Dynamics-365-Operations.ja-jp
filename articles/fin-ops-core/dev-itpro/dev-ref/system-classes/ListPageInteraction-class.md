---
title: ListPageInteraction クラス
description: このトピックでは、ListPageInteraction クラスについて説明します。
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
ms.openlocfilehash: a750d21cc16a0f8282b3b80a6e06e652d31b3e4f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502589"
---
# <a name="class-listpageinteraction"></a><span data-ttu-id="81f2a-103">クラス ListPageInteraction</span><span class="sxs-lookup"><span data-stu-id="81f2a-103">Class ListPageInteraction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ListPageInteraction extends PageInteraction
```

## <a name="remarks"></a><span data-ttu-id="81f2a-104">備考</span><span class="sxs-lookup"><span data-stu-id="81f2a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="81f2a-105">例</span><span class="sxs-lookup"><span data-stu-id="81f2a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="81f2a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="81f2a-106">Methods</span></span>

| <span data-ttu-id="81f2a-107">方法</span><span class="sxs-lookup"><span data-stu-id="81f2a-107">Method</span></span>                                           | <span data-ttu-id="81f2a-108">説明</span><span class="sxs-lookup"><span data-stu-id="81f2a-108">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="81f2a-109">public ListPage listPage()</span><span class="sxs-lookup"><span data-stu-id="81f2a-109">public ListPage listPage()</span></span>                       |                                                               |
| <span data-ttu-id="81f2a-110">public void tabChanged(container activeTabNames)</span><span class="sxs-lookup"><span data-stu-id="81f2a-110">public void tabChanged(container activeTabNames)</span></span> | <span data-ttu-id="81f2a-111">アクティブなタブが変更されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="81f2a-111">Called when the active tab is changed.</span></span>                        |
| <span data-ttu-id="81f2a-112">public void initializing()</span><span class="sxs-lookup"><span data-stu-id="81f2a-112">public void initializing()</span></span>                       |                                                               |
| <span data-ttu-id="81f2a-113">public void initialized()</span><span class="sxs-lookup"><span data-stu-id="81f2a-113">public void initialized()</span></span>                        |                                                               |
| <span data-ttu-id="81f2a-114">public void selectionChanged()</span><span class="sxs-lookup"><span data-stu-id="81f2a-114">public void selectionChanged()</span></span>                   |                                                               |
| <span data-ttu-id="81f2a-115">public void initializeQuery(Query query)</span><span class="sxs-lookup"><span data-stu-id="81f2a-115">public void initializeQuery(Query query)</span></span>         |                                                               |
| <span data-ttu-id="81f2a-116">public void new(ListPage listPage)</span><span class="sxs-lookup"><span data-stu-id="81f2a-116">public void new(ListPage listPage)</span></span>               | <span data-ttu-id="81f2a-117">listPage 上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="81f2a-117">Creates a new PageInteraction object operating on a listPage.</span></span> |

## <a name="method-listpage"></a><span data-ttu-id="81f2a-118">メソッド listPage</span><span class="sxs-lookup"><span data-stu-id="81f2a-118">Method listPage</span></span>

```xpp
public ListPage listPage()
```

### <a name="return-value---listpage"></a><span data-ttu-id="81f2a-119">戻り値 - listPage</span><span class="sxs-lookup"><span data-stu-id="81f2a-119">Return Value - listPage</span></span>

## <a name="method-tabchanged"></a><span data-ttu-id="81f2a-120">メソッド tabChanged</span><span class="sxs-lookup"><span data-stu-id="81f2a-120">Method tabChanged</span></span>

<span data-ttu-id="81f2a-121">アクティブなタブが変更されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="81f2a-121">Called when the active tab is changed.</span></span>

```xpp
public void tabChanged(container activeTabNames)
```

### <a name="parameters---tabchanged"></a><span data-ttu-id="81f2a-122">パラメーター - tabChanged</span><span class="sxs-lookup"><span data-stu-id="81f2a-122">Parameters - tabChanged</span></span>

<span data-ttu-id="81f2a-123">activeTabNames</span><span class="sxs-lookup"><span data-stu-id="81f2a-123">activeTabNames</span></span>  
<span data-ttu-id="81f2a-124">アクティブなタブの名前を含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="81f2a-124">A container containing the names of the active tabs.</span></span>

## <a name="method-initializing"></a><span data-ttu-id="81f2a-125">メソッド initializing</span><span class="sxs-lookup"><span data-stu-id="81f2a-125">Method initializing</span></span>

```xpp
public void initializing()
```

## <a name="method-initialized"></a><span data-ttu-id="81f2a-126">メソッド initialized</span><span class="sxs-lookup"><span data-stu-id="81f2a-126">Method initialized</span></span>

```xpp
public void initialized()
```

## <a name="method-selectionchanged"></a><span data-ttu-id="81f2a-127">メソッド selectionChanged</span><span class="sxs-lookup"><span data-stu-id="81f2a-127">Method selectionChanged</span></span>

```xpp
public void selectionChanged()
```

## <a name="method-initializequery"></a><span data-ttu-id="81f2a-128">メソッド initializeQuery</span><span class="sxs-lookup"><span data-stu-id="81f2a-128">Method initializeQuery</span></span>

```xpp
public void initializeQuery(Query query)
```

### <a name="parameters---initializequery"></a><span data-ttu-id="81f2a-129">パラメーター - initializeQuery</span><span class="sxs-lookup"><span data-stu-id="81f2a-129">Parameters - initializeQuery</span></span>

<span data-ttu-id="81f2a-130">クエリ</span><span class="sxs-lookup"><span data-stu-id="81f2a-130">query</span></span>  

## <a name="method-new"></a><span data-ttu-id="81f2a-131">メソッド new</span><span class="sxs-lookup"><span data-stu-id="81f2a-131">Method new</span></span>

<span data-ttu-id="81f2a-132">listPage 上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="81f2a-132">Creates a new PageInteraction object operating on a listPage.</span></span>

```xpp
public void new(ListPage listPage)
```

### <a name="parameters---new"></a><span data-ttu-id="81f2a-133">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="81f2a-133">Parameters - new</span></span>

<span data-ttu-id="81f2a-134">listPage</span><span class="sxs-lookup"><span data-stu-id="81f2a-134">listPage</span></span>  
<span data-ttu-id="81f2a-135">指定した ListPage オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="81f2a-135">The specified ListPage object.</span></span>

