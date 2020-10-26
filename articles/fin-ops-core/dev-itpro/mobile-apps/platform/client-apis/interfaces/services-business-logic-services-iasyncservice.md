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
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 343d5a721dac476bb47ae7c550774cf7c876e3af
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983958"
---
# <a name="asyncservice-type"></a><span data-ttu-id="2043e-103">AsyncService タイプ</span><span class="sxs-lookup"><span data-stu-id="2043e-103">AsyncService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="2043e-104">ビジネス ロジック コードから非同期操作を実行する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2043e-104">Provides ability to perform async operations from business logic code.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="2043e-105">階層</span><span class="sxs-lookup"><span data-stu-id="2043e-105">Hierarchy</span></span>

<span data-ttu-id="2043e-106">AsyncService</span><span class="sxs-lookup"><span data-stu-id="2043e-106">AsyncService</span></span> <br>

## <a name="index"></a><span data-ttu-id="2043e-107">指数</span><span class="sxs-lookup"><span data-stu-id="2043e-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="2043e-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="2043e-108">Methods</span></span>

* [<span data-ttu-id="2043e-109">すべて</span><span class="sxs-lookup"><span data-stu-id="2043e-109">all</span></span>](services-business-logic-services-iasyncservice.md#all)
* [<span data-ttu-id="2043e-110">延期</span><span class="sxs-lookup"><span data-stu-id="2043e-110">defer</span></span>](services-business-logic-services-iasyncservice.md#defer)

## <a name="methods"></a><span data-ttu-id="2043e-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="2043e-111">Methods</span></span>

### <a name="all"></a><span data-ttu-id="2043e-112">すべて</span><span class="sxs-lookup"><span data-stu-id="2043e-112">all</span></span>


<span data-ttu-id="2043e-113">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="2043e-113">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="2043e-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2043e-114">Parameters</span></span>

| <span data-ttu-id="2043e-115">氏名</span><span class="sxs-lookup"><span data-stu-id="2043e-115">Name</span></span> | <span data-ttu-id="2043e-116">種類</span><span class="sxs-lookup"><span data-stu-id="2043e-116">Type</span></span> | <span data-ttu-id="2043e-117">説明</span><span class="sxs-lookup"><span data-stu-id="2043e-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="2043e-118">...args</span><span class="sxs-lookup"><span data-stu-id="2043e-118">...args</span></span>|<span data-ttu-id="2043e-119">any [ ]</span><span class="sxs-lookup"><span data-stu-id="2043e-119">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="2043e-120">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="2043e-120">Returns Promise &lt;any [ ]&gt;</span></span>

### <a name="defer"></a><span data-ttu-id="2043e-121">defer</span><span class="sxs-lookup"><span data-stu-id="2043e-121">defer</span></span>


<span data-ttu-id="2043e-122">defer &lt;T&gt;(): [Deferred](defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="2043e-122">defer &lt;T&gt;(): [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>

<span data-ttu-id="2043e-123">イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを解決/拒否するために使用できる遅延オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2043e-123">Creates a deferred object which can be used to return a promise from event handlers (where applicable) and resolve/reject them asynchronously.</span></span>

#### <a name="returns-deferred-lttgt"></a><span data-ttu-id="2043e-124">[Deferred](defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="2043e-124">Returns [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>

