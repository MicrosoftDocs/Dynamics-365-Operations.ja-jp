---
title: AsyncService タイプ
description: ビジネス ロジック コードから非同期操作を実行する機能を提供します。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4b40b40dad7c7c49cb0b073f729f5920a1ec45d3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369310"
---
# <a name="asyncservice-type"></a><span data-ttu-id="2c53b-103">AsyncService タイプ</span><span class="sxs-lookup"><span data-stu-id="2c53b-103">AsyncService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="2c53b-104">ビジネス ロジック コードから非同期操作を実行する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c53b-104">Provides ability to perform async operations from business logic code.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="2c53b-105">階層</span><span class="sxs-lookup"><span data-stu-id="2c53b-105">Hierarchy</span></span>

<span data-ttu-id="2c53b-106">AsyncService</span><span class="sxs-lookup"><span data-stu-id="2c53b-106">AsyncService</span></span> <br>

## <a name="index"></a><span data-ttu-id="2c53b-107">指数</span><span class="sxs-lookup"><span data-stu-id="2c53b-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="2c53b-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="2c53b-108">Methods</span></span>

* [<span data-ttu-id="2c53b-109">すべて</span><span class="sxs-lookup"><span data-stu-id="2c53b-109">all</span></span>](services-business-logic-services-iasyncservice.md#all)
* [<span data-ttu-id="2c53b-110">延期</span><span class="sxs-lookup"><span data-stu-id="2c53b-110">defer</span></span>](services-business-logic-services-iasyncservice.md#defer)

## <a name="methods"></a><span data-ttu-id="2c53b-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="2c53b-111">Methods</span></span>

### <a name="all"></a><span data-ttu-id="2c53b-112">すべて</span><span class="sxs-lookup"><span data-stu-id="2c53b-112">all</span></span>


<span data-ttu-id="2c53b-113">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="2c53b-113">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="2c53b-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c53b-114">Parameters</span></span>

| <span data-ttu-id="2c53b-115">氏名</span><span class="sxs-lookup"><span data-stu-id="2c53b-115">Name</span></span> | <span data-ttu-id="2c53b-116">種類</span><span class="sxs-lookup"><span data-stu-id="2c53b-116">Type</span></span> | <span data-ttu-id="2c53b-117">説明</span><span class="sxs-lookup"><span data-stu-id="2c53b-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="2c53b-118">...args</span><span class="sxs-lookup"><span data-stu-id="2c53b-118">...args</span></span>|<span data-ttu-id="2c53b-119">any [ ]</span><span class="sxs-lookup"><span data-stu-id="2c53b-119">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="2c53b-120">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="2c53b-120">Returns Promise &lt;any [ ]&gt;</span></span>

### <a name="defer"></a><span data-ttu-id="2c53b-121">defer</span><span class="sxs-lookup"><span data-stu-id="2c53b-121">defer</span></span>


<span data-ttu-id="2c53b-122">defer &lt;T&gt;(): [Deferred](defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="2c53b-122">defer &lt;T&gt;(): [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>

<span data-ttu-id="2c53b-123">イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを解決/拒否するために使用できる遅延オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2c53b-123">Creates a deferred object which can be used to return a promise from event handlers (where applicable) and resolve/reject them asynchronously.</span></span>

#### <a name="returns-deferreddefer-ideferredmd-lttgt"></a><span data-ttu-id="2c53b-124">[Deferred](defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="2c53b-124">Returns [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>

