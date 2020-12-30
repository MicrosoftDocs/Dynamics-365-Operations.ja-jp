---
title: 生産フロー活動への先行処理の追加
description: 生産フロー バージョンでは、すべての活動は順番に配列する必要があります。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c39cef1174439b42a072bd7fc1ac29ef31ecf864
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431695"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="6e6cc-103">生産フロー活動への先行処理の追加</span><span class="sxs-lookup"><span data-stu-id="6e6cc-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e6cc-104">生産フロー バージョンでは、すべての活動は順番に配列する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="6e6cc-105">活動には、複数の先行または後続の処理を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="6e6cc-106">この手順は、活動に先行処理を関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="6e6cc-107">この作業を行うには、接続できる2つ以上の活動を有するドラフト バージョンがある生産フローが必要です。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="6e6cc-108">詳細については、 「生産フローおよびリーン生産」というホワイト ペーパーを参照します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="6e6cc-109">生産フロー バージョンを検索する</span><span class="sxs-lookup"><span data-stu-id="6e6cc-109">Find the production flow and version</span></span>
1. <span data-ttu-id="6e6cc-110">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="6e6cc-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6e6cc-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6e6cc-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6e6cc-114">[活動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="6e6cc-115">[活動] を選択して、[先行処理] を追加する</span><span class="sxs-lookup"><span data-stu-id="6e6cc-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="6e6cc-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="6e6cc-117">[先行処理の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="6e6cc-118">[活動] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="6e6cc-119">[サイクル時間の比率] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="6e6cc-120">活動関係の既定のサイクル時間率は 1 です。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="6e6cc-121">これは、活動またはタクト タイムの両方が同じペースで実行されると仮定します。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="6e6cc-122">先行処理がより速いペース (下部タクト タイム) で実行中の場合、比率は1以下にします。先行がそれよりも遅いペース (より大きい)で実行中の場合、サイクル時間率は1以上になります。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="6e6cc-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e6cc-123">Click OK.</span></span>

