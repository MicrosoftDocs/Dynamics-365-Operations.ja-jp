---
title: PageInteraction クラス
description: このトピックでは、PageInteraction クラスについて説明します。
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
ms.openlocfilehash: f5f7dc807d9e292c6f27b45b22b2dfee2e72153a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502536"
---
# <a name="class-pageinteraction"></a><span data-ttu-id="3c4bc-103">クラス PageInteraction</span><span class="sxs-lookup"><span data-stu-id="3c4bc-103">Class PageInteraction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PageInteraction extends Object
```

<span data-ttu-id="3c4bc-104">PageInteraction クラスは、リスト ページとやり取りするための機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="3c4bc-104">The PageInteraction class provides functionality for interacting with a list page.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c4bc-105">備考</span><span class="sxs-lookup"><span data-stu-id="3c4bc-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3c4bc-106">例</span><span class="sxs-lookup"><span data-stu-id="3c4bc-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3c4bc-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="3c4bc-107">Methods</span></span>

| <span data-ttu-id="3c4bc-108">方法</span><span class="sxs-lookup"><span data-stu-id="3c4bc-108">Method</span></span>                                           | <span data-ttu-id="3c4bc-109">説明</span><span class="sxs-lookup"><span data-stu-id="3c4bc-109">Description</span></span>                                                        |
|--------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3c4bc-110">public Page page()</span><span class="sxs-lookup"><span data-stu-id="3c4bc-110">public Page page()</span></span>                               | <span data-ttu-id="3c4bc-111">ListPage インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="3c4bc-111">Gets the ListPage instance.</span></span>                                        |
| <span data-ttu-id="3c4bc-112">public void tabChanged(container activeTabNames)</span><span class="sxs-lookup"><span data-stu-id="3c4bc-112">public void tabChanged(container activeTabNames)</span></span> |                                                                    |
| <span data-ttu-id="3c4bc-113">public void new(Page page)</span><span class="sxs-lookup"><span data-stu-id="3c4bc-113">public void new(Page page)</span></span>                       | <span data-ttu-id="3c4bc-114">リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c4bc-114">Creates a new PageInteraction object that operates on a list page.</span></span> |

## <a name="method-page"></a><span data-ttu-id="3c4bc-115">メソッド page</span><span class="sxs-lookup"><span data-stu-id="3c4bc-115">Method page</span></span>

<span data-ttu-id="3c4bc-116">ListPage インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="3c4bc-116">Gets the ListPage instance.</span></span>

```xpp
public Page page()
```

### <a name="return-value---page"></a><span data-ttu-id="3c4bc-117">戻り値 - page</span><span class="sxs-lookup"><span data-stu-id="3c4bc-117">Return Value - page</span></span>

<span data-ttu-id="3c4bc-118">この PageInteraction インスタンスの ListPage インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="3c4bc-118">Returns the ListPage instance for this PageInteraction instance.</span></span>

## <a name="method-tabchanged"></a><span data-ttu-id="3c4bc-119">メソッド tabChanged</span><span class="sxs-lookup"><span data-stu-id="3c4bc-119">Method tabChanged</span></span>

```xpp
public void tabChanged(container activeTabNames)
```

### <a name="parameters---tabchanged"></a><span data-ttu-id="3c4bc-120">パラメーター - tabChanged</span><span class="sxs-lookup"><span data-stu-id="3c4bc-120">Parameters - tabChanged</span></span>

<span data-ttu-id="3c4bc-121">activeTabNames</span><span class="sxs-lookup"><span data-stu-id="3c4bc-121">activeTabNames</span></span>  

## <a name="method-new"></a><span data-ttu-id="3c4bc-122">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3c4bc-122">Method new</span></span>

<span data-ttu-id="3c4bc-123">リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c4bc-123">Creates a new PageInteraction object that operates on a list page.</span></span>

```xpp
public void new(Page page)
```

### <a name="parameters---new"></a><span data-ttu-id="3c4bc-124">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="3c4bc-124">Parameters - new</span></span>

<span data-ttu-id="3c4bc-125">ページ</span><span class="sxs-lookup"><span data-stu-id="3c4bc-125">page</span></span>  

