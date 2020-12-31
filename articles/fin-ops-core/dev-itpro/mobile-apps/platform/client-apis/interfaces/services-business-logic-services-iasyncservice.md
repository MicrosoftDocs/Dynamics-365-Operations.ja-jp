---
title: AsyncService タイプ
description: ビジネス ロジック コードから非同期操作を実行する機能を提供します。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 77dfc1ed0144907f1f2b8b8f0baa9a4aaff1bf13
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679241"
---
# <a name="asyncservice-type"></a><span data-ttu-id="a8bd6-103">AsyncService タイプ</span><span class="sxs-lookup"><span data-stu-id="a8bd6-103">AsyncService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="a8bd6-104">ビジネス ロジック コードから非同期操作を実行する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="a8bd6-104">Provides ability to perform async operations from business logic code.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="a8bd6-105">階層</span><span class="sxs-lookup"><span data-stu-id="a8bd6-105">Hierarchy</span></span>

<span data-ttu-id="a8bd6-106">AsyncService</span><span class="sxs-lookup"><span data-stu-id="a8bd6-106">AsyncService</span></span>

## <a name="index"></a><span data-ttu-id="a8bd6-107">指数</span><span class="sxs-lookup"><span data-stu-id="a8bd6-107">Index</span></span>

### <a name="method-list"></a><span data-ttu-id="a8bd6-108">メソッド リスト</span><span class="sxs-lookup"><span data-stu-id="a8bd6-108">Method list</span></span>

* [<span data-ttu-id="a8bd6-109">すべて</span><span class="sxs-lookup"><span data-stu-id="a8bd6-109">all</span></span>](services-business-logic-services-iasyncservice.md#all)
* [<span data-ttu-id="a8bd6-110">延期</span><span class="sxs-lookup"><span data-stu-id="a8bd6-110">defer</span></span>](services-business-logic-services-iasyncservice.md#defer)

## <a name="methods"></a><span data-ttu-id="a8bd6-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="a8bd6-111">Methods</span></span>

### <a name="all"></a><span data-ttu-id="a8bd6-112">すべて</span><span class="sxs-lookup"><span data-stu-id="a8bd6-112">all</span></span>

`all(...args: any [ ]): Promise <any [ ]>`

#### <a name="parameters"></a><span data-ttu-id="a8bd6-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a8bd6-113">Parameters</span></span>

| <span data-ttu-id="a8bd6-114">氏名</span><span class="sxs-lookup"><span data-stu-id="a8bd6-114">Name</span></span> | <span data-ttu-id="a8bd6-115">種類</span><span class="sxs-lookup"><span data-stu-id="a8bd6-115">Type</span></span> | <span data-ttu-id="a8bd6-116">説明</span><span class="sxs-lookup"><span data-stu-id="a8bd6-116">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="a8bd6-117">...args</span><span class="sxs-lookup"><span data-stu-id="a8bd6-117">...args</span></span>|<span data-ttu-id="a8bd6-118">any [ ]</span><span class="sxs-lookup"><span data-stu-id="a8bd6-118">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="a8bd6-119">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="a8bd6-119">Returns Promise &lt;any [ ]&gt;</span></span>

### <a name="defer"></a><span data-ttu-id="a8bd6-120">defer</span><span class="sxs-lookup"><span data-stu-id="a8bd6-120">defer</span></span>

`defer <>(): [Deferred](defer-ideferred.md) <>`

<span data-ttu-id="a8bd6-121">イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを拒否または解決するために使用できる遅延オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8bd6-121">Creates a deferred object that can be used to return a promise from event handlers (where applicable) and resolve/reject them asynchronously.</span></span>

#### <a name="returns-deferred-lttgt"></a><span data-ttu-id="a8bd6-122">[Deferred](defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="a8bd6-122">Returns [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>
