---
title: AsyncService
description: "ビジネス ロジック コードから非同期操作を実行する機能を提供します。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2afb76bc9f1fc7a6004bc3aab8d74460e06d5b3c
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="asyncservice-type"></a><span data-ttu-id="fb57d-103">AsyncService タイプ</span><span class="sxs-lookup"><span data-stu-id="fb57d-103">AsyncService Type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="fb57d-104">ビジネス ロジック コードから非同期操作を実行する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb57d-104">Provides ability to perform async operations from business logic code.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="fb57d-105">階層</span><span class="sxs-lookup"><span data-stu-id="fb57d-105">Hierarchy</span></span>

<span data-ttu-id="fb57d-106">AsyncService</span><span class="sxs-lookup"><span data-stu-id="fb57d-106">AsyncService</span></span> <br>

## <a name="index"></a><span data-ttu-id="fb57d-107">指数</span><span class="sxs-lookup"><span data-stu-id="fb57d-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="fb57d-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="fb57d-108">Methods</span></span>

* [<span data-ttu-id="fb57d-109">すべて</span><span class="sxs-lookup"><span data-stu-id="fb57d-109">all</span></span>](services-business-logic-services-iasyncservice.md#all)
* [<span data-ttu-id="fb57d-110">延期</span><span class="sxs-lookup"><span data-stu-id="fb57d-110">defer</span></span>](services-business-logic-services-iasyncservice.md#defer)

## <a name="methods"></a><span data-ttu-id="fb57d-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="fb57d-111">Methods</span></span>

### <a name="all"></a><span data-ttu-id="fb57d-112">すべて</span><span class="sxs-lookup"><span data-stu-id="fb57d-112">all</span></span>


<span data-ttu-id="fb57d-113">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="fb57d-113">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="fb57d-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fb57d-114">Parameters</span></span>

| <span data-ttu-id="fb57d-115">氏名</span><span class="sxs-lookup"><span data-stu-id="fb57d-115">Name</span></span> | <span data-ttu-id="fb57d-116">種類</span><span class="sxs-lookup"><span data-stu-id="fb57d-116">Type</span></span> | <span data-ttu-id="fb57d-117">説明</span><span class="sxs-lookup"><span data-stu-id="fb57d-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="fb57d-118">...args</span><span class="sxs-lookup"><span data-stu-id="fb57d-118">...args</span></span>|<span data-ttu-id="fb57d-119">any [ ]</span><span class="sxs-lookup"><span data-stu-id="fb57d-119">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="fb57d-120">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="fb57d-120">Returns Promise &lt;any [ ]&gt;</span></span>

### <a name="defer"></a><span data-ttu-id="fb57d-121">defer</span><span class="sxs-lookup"><span data-stu-id="fb57d-121">defer</span></span>


<span data-ttu-id="fb57d-122">defer &lt;T&gt;(): [Deferred](defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="fb57d-122">defer &lt;T&gt;(): [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>

<span data-ttu-id="fb57d-123">イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを解決/拒否するために使用できる遅延オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb57d-123">Creates a deferred object which can be used to return a promise from event handlers (where applicable) and resolve/reject them asynchronously.</span></span>

#### <a name="returns-deferreddefer-ideferredmd-lttgt"></a><span data-ttu-id="fb57d-124">[Deferred](defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="fb57d-124">Returns [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>


