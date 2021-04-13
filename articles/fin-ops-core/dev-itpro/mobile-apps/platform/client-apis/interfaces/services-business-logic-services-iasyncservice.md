---
title: AsyncService タイプ
description: ビジネス ロジック コードから非同期操作を実行する機能を提供します。
author: robinarh
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88f4f7fa3996153cebc2eac44d3760b5c5498b4c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745217"
---
# <a name="asyncservice-type"></a><span data-ttu-id="04746-103">AsyncService タイプ</span><span class="sxs-lookup"><span data-stu-id="04746-103">AsyncService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="04746-104">ビジネス ロジック コードから非同期操作を実行する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="04746-104">Provides ability to perform async operations from business logic code.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="04746-105">階層</span><span class="sxs-lookup"><span data-stu-id="04746-105">Hierarchy</span></span>

<span data-ttu-id="04746-106">AsyncService</span><span class="sxs-lookup"><span data-stu-id="04746-106">AsyncService</span></span>

## <a name="index"></a><span data-ttu-id="04746-107">指数</span><span class="sxs-lookup"><span data-stu-id="04746-107">Index</span></span>

### <a name="method-list"></a><span data-ttu-id="04746-108">メソッド リスト</span><span class="sxs-lookup"><span data-stu-id="04746-108">Method list</span></span>

* [<span data-ttu-id="04746-109">すべて</span><span class="sxs-lookup"><span data-stu-id="04746-109">all</span></span>](services-business-logic-services-iasyncservice.md#all)
* [<span data-ttu-id="04746-110">延期</span><span class="sxs-lookup"><span data-stu-id="04746-110">defer</span></span>](services-business-logic-services-iasyncservice.md#defer)

## <a name="methods"></a><span data-ttu-id="04746-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="04746-111">Methods</span></span>

### <a name="all"></a><span data-ttu-id="04746-112">すべて</span><span class="sxs-lookup"><span data-stu-id="04746-112">all</span></span>

`all(...args: any [ ]): Promise <any [ ]>`

#### <a name="parameters"></a><span data-ttu-id="04746-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04746-113">Parameters</span></span>

| <span data-ttu-id="04746-114">氏名</span><span class="sxs-lookup"><span data-stu-id="04746-114">Name</span></span> | <span data-ttu-id="04746-115">種類</span><span class="sxs-lookup"><span data-stu-id="04746-115">Type</span></span> | <span data-ttu-id="04746-116">説明</span><span class="sxs-lookup"><span data-stu-id="04746-116">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="04746-117">...args</span><span class="sxs-lookup"><span data-stu-id="04746-117">...args</span></span>|<span data-ttu-id="04746-118">any [ ]</span><span class="sxs-lookup"><span data-stu-id="04746-118">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="04746-119">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="04746-119">Returns Promise &lt;any [ ]&gt;</span></span>

### <a name="defer"></a><span data-ttu-id="04746-120">defer</span><span class="sxs-lookup"><span data-stu-id="04746-120">defer</span></span>

`defer <>(): [Deferred](defer-ideferred.md) <>`

<span data-ttu-id="04746-121">イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを拒否または解決するために使用できる遅延オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="04746-121">Creates a deferred object that can be used to return a promise from event handlers (where applicable) and resolve/reject them asynchronously.</span></span>

#### <a name="returns-deferred-lttgt"></a><span data-ttu-id="04746-122">[Deferred](defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="04746-122">Returns [Deferred](defer-ideferred.md) &lt;T&gt;</span></span>


[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]