---
title: FormsPreloadingManager クラス
description: このトピックでは、FormsPreloadingManager クラスについて説明します。
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
ms.openlocfilehash: 3aa69c2f21366d18c149773306807f96a7dcdd02
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502908"
---
# <a name="class-formspreloadingmanager"></a><span data-ttu-id="522e0-103">クラス FormsPreloadingManager</span><span class="sxs-lookup"><span data-stu-id="522e0-103">Class FormsPreloadingManager</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormsPreloadingManager extends Object
```

<span data-ttu-id="522e0-104">FormsPreloadingManager クラスは、ワークスペースの関連付けとリソース負荷管理などのフォームのプリロードを管理します。</span><span class="sxs-lookup"><span data-stu-id="522e0-104">The FormsPreloadingManager class manages the preloading of forms, including workspace association and resource pressure management.</span></span>

## <a name="remarks"></a><span data-ttu-id="522e0-105">備考</span><span class="sxs-lookup"><span data-stu-id="522e0-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="522e0-106">例</span><span class="sxs-lookup"><span data-stu-id="522e0-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="522e0-107">方法</span><span class="sxs-lookup"><span data-stu-id="522e0-107">Methods</span></span>

| <span data-ttu-id="522e0-108">方法</span><span class="sxs-lookup"><span data-stu-id="522e0-108">Method</span></span>                                              | <span data-ttu-id="522e0-109">説明</span><span class="sxs-lookup"><span data-stu-id="522e0-109">Description</span></span>                                                                                  |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="522e0-110">::private static FormsPreloadingManager construct()</span><span class="sxs-lookup"><span data-stu-id="522e0-110">::private static FormsPreloadingManager construct()</span></span> |                                                                                              |
| <span data-ttu-id="522e0-111">public void workspaceActivated()</span><span class="sxs-lookup"><span data-stu-id="522e0-111">public void workspaceActivated()</span></span>                    | <span data-ttu-id="522e0-112">プリロード ワークスペース アフィニティを最後にアクティブ化されたワークスペースに設定します。</span><span class="sxs-lookup"><span data-stu-id="522e0-112">Sets the preloading workspace affinity to the last activated workspace.</span></span>                      |
| <span data-ttu-id="522e0-113">private void new()</span><span class="sxs-lookup"><span data-stu-id="522e0-113">private void new()</span></span>                                  | <span data-ttu-id="522e0-114">FormsPreloadingManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="522e0-114">Initializes a new instance of the FormsPreloadingManager class.</span></span>                              |
| <span data-ttu-id="522e0-115">public void updateState()</span><span class="sxs-lookup"><span data-stu-id="522e0-115">public void updateState()</span></span>                           | <span data-ttu-id="522e0-116">読み込みのためにフォームを照会し、リソース使用率の負荷を処理し、その他の内部の状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="522e0-116">Queues forms for loading, handles high resource pressure, and updates other internal states.</span></span> |

## <a name="method-construct"></a><span data-ttu-id="522e0-117">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="522e0-117">Method construct</span></span>

```xpp
private static FormsPreloadingManager construct()
```

### <a name="return-value---construct"></a><span data-ttu-id="522e0-118">戻り値 - construct</span><span class="sxs-lookup"><span data-stu-id="522e0-118">Return Value - construct</span></span>

## <a name="method-workspaceactivated"></a><span data-ttu-id="522e0-119">メソッド workspaceActivated</span><span class="sxs-lookup"><span data-stu-id="522e0-119">Method workspaceActivated</span></span>

<span data-ttu-id="522e0-120">プリロード ワークスペース アフィニティを最後にアクティブ化されたワークスペースに設定します。</span><span class="sxs-lookup"><span data-stu-id="522e0-120">Sets the preloading workspace affinity to the last activated workspace.</span></span>

```xpp
public void workspaceActivated()
```

### <a name="remarks---workspaceactivated"></a><span data-ttu-id="522e0-121">備考 - workspaceActivated</span><span class="sxs-lookup"><span data-stu-id="522e0-121">Remarks - workspaceActivated</span></span>

<span data-ttu-id="522e0-122">このメソッドは、通常、ワークスペースが有効にされた後にタイマーで呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="522e0-122">This method is typically called on a timer after a workspace has been activated.</span></span> <span data-ttu-id="522e0-123">ワークスペースを変更に対してすぐに親和させるには、このメソッドを直接呼び出します。</span><span class="sxs-lookup"><span data-stu-id="522e0-123">Call this method directly to force the workspace affinity to change immediately.</span></span>

## <a name="method-new"></a><span data-ttu-id="522e0-124">メソッド new</span><span class="sxs-lookup"><span data-stu-id="522e0-124">Method new</span></span>

<span data-ttu-id="522e0-125">FormsPreloadingManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="522e0-125">Initializes a new instance of the FormsPreloadingManager class.</span></span>

```xpp
private void new()
```

## <a name="method-updatestate"></a><span data-ttu-id="522e0-126">メソッド updateState</span><span class="sxs-lookup"><span data-stu-id="522e0-126">Method updateState</span></span>

<span data-ttu-id="522e0-127">読み込みのためにフォームを照会し、リソース使用率の負荷を処理し、その他の内部の状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="522e0-127">Queues forms for loading, handles high resource pressure, and updates other internal states.</span></span>

```xpp
public void updateState()
```

### <a name="remarks---updatestate"></a><span data-ttu-id="522e0-128">備考 - updateState</span><span class="sxs-lookup"><span data-stu-id="522e0-128">Remarks - updateState</span></span>

<span data-ttu-id="522e0-129">このメソッドは、通常アイドル状態のときタイマーで呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="522e0-129">This method is typically called on a timer during idle periods.</span></span> <span data-ttu-id="522e0-130">実行時間の長い X++ コードが実行されている場合など、非アイドル時に状態を強制的に更新するには、このメソッドを直接呼び出します。</span><span class="sxs-lookup"><span data-stu-id="522e0-130">Call this method directly to force a state update during non-idle periods, such as when long-running X++ code is running.</span></span>

