---
title: 移動平均フォールバック コスト シーケンス
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Managementで移動平均を計算するためのフォールバック コスト シーケンスについて説明します。
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597387"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="c1160-103">移動平均フォールバック コスト シーケンス</span><span class="sxs-lookup"><span data-stu-id="c1160-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="c1160-104">在庫の原価を計算する 1 つの方法は、_移動平均_ を使用することです。</span><span class="sxs-lookup"><span data-stu-id="c1160-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="c1160-105">各在庫品目には、最大 3 つの原価価値を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c1160-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="c1160-106">**最終払出** – 在庫がマイナスになる前に割り当てられた最終払出原価</span><span class="sxs-lookup"><span data-stu-id="c1160-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="c1160-107">**有効な原価** – 原価計算バージョンで有効化された最新の原価</span><span class="sxs-lookup"><span data-stu-id="c1160-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="c1160-108">**品目価格** – リリース済み製品に対して指定されている原価</span><span class="sxs-lookup"><span data-stu-id="c1160-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="c1160-109">これらの原価価値のうちどれを移動平均の計算に使用するかを決定するために、システムでは _フォールバック コスト シーケンス_ を使用して、値の優先順位を決定します。</span><span class="sxs-lookup"><span data-stu-id="c1160-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="c1160-110">優先原価価値が使用できない場合、システムは次に優先される値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1160-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="c1160-111">以前のバージョンのMicrosoft Dynamics 365 Supply Chain Management では、システムは固定のフォールバック コスト シーケンス (_最終払出 – 有効な原価 – 品目価格_) を使用していました。</span><span class="sxs-lookup"><span data-stu-id="c1160-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="c1160-112">バージョン 10.0.11 では、このシーケンスは依然として既定のシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="c1160-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="c1160-113">ただし、使用可能な 3 つのフォールバック コスト シーケンスから選択できる機能を有効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c1160-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="c1160-114">この機能は、マイナス在庫値を定期的に使用する組織で特に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c1160-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="c1160-115">フォールバック コスト シーケンスのセレクターを使用できるようにするには、ユーザー (または管理者) は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して、_移動平均フォールバック コスト シーケンス_ という名前の機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1160-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="c1160-116">移動平均の計算に使用するフォールバック コスト シーケンスを選択するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c1160-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="c1160-117">**パラメーター** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c1160-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="c1160-118">**在庫会計** タブの **移動平均** セクションで、**フォールバック コスト シーケンス** フィールドを次のいずれかの値に設定します:</span><span class="sxs-lookup"><span data-stu-id="c1160-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="c1160-119">**最終払出 – 有効な原価 – 品目価格** – このシーケンスは、既定のシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="c1160-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="c1160-120">_移動平均フォールバック コスト シーケンス_ 機能が有効になっていない場合に使用されるシーケンスと同じです。</span><span class="sxs-lookup"><span data-stu-id="c1160-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="c1160-121">**有効な原価 – 最終払出**</span><span class="sxs-lookup"><span data-stu-id="c1160-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="c1160-122">**有効な原価 – 品目価格** – 在庫が定期的にマイナスになり、同時に、トランザクション量が高い業務プロセスを使用している場合、組織でパフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c1160-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="c1160-123">この設定は、これらのパフォーマンスの問題を軽減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c1160-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="c1160-124">![在庫会計パラメーター](media/inventory-accounting-parameters.png "在庫会計パラメーター")</span><span class="sxs-lookup"><span data-stu-id="c1160-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
