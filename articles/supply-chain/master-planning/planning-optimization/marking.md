---
title: 計画最適化を使用した在庫マーキング
description: このトピックでは、計画の最適化を使用する場合に、確定された注文の在庫をマークするために使用できるオプションに関する情報を提供します。
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3b139673ddf17e13d6687db485208e1aeb3908dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809497"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="cf5e8-103">計画最適化を使用した在庫マーキング</span><span class="sxs-lookup"><span data-stu-id="cf5e8-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf5e8-104">このトピックでは、計画の最適化を使用する場合に、確定された注文の在庫をマークするために使用できるオプションに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="cf5e8-105">*マーキング* は、供給と需要をリンクするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="cf5e8-106">これは *ペギング* と似ており、マスター プランが需要を補充する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="cf5e8-107">計画の観点から見ると、主な違いは、マーキングがペギングよりも永続的であることです。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="cf5e8-108">マーキングは、先入れ先出し (FIFO) および後入れ先出し (LIFO) の特別な原価シナリオをサポートするために導入されました。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="cf5e8-109">ただし、これは、一部の非原価シナリオでも使用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="cf5e8-110">供給と需要の間のマーキングはオプションで、ほとんど永続的ではありません。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="cf5e8-111">ユーザーによるマーキングは手動で削除することも、**マーキングの削除** オプションが選択されている販売注文明細行の展開を実行することによって削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="cf5e8-112">ペギングは、必要な供給とリンク需要の範囲内でマスター プランによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="cf5e8-113">計画実行ごとにペギングを更新して、需要をカバーするために必要な供給を最適化することができます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="cf5e8-114">マスター プランでペギング情報が更新されるときには、既存のマーキングが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="cf5e8-115">ペギングは、関連するマーキング、手持在庫、および注文中引当を含めることから、次のシーケンスで開始されます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="cf5e8-116">需要と供給の間のマーキング</span><span class="sxs-lookup"><span data-stu-id="cf5e8-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="cf5e8-117">手持在庫の引当</span><span class="sxs-lookup"><span data-stu-id="cf5e8-117">On-hand reservations</span></span>
1. <span data-ttu-id="cf5e8-118">注文中の引当</span><span class="sxs-lookup"><span data-stu-id="cf5e8-118">On-order reservations</span></span>

<span data-ttu-id="cf5e8-119">計画オーダーを確定すると、**確定** ダイアログボックスには、確定中に作成された注文のマーキング オプションを設定するために使用する **マーキングの更新** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="cf5e8-120">次の値からいずれか 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-120">Select one of the following values:</span></span>

- <span data-ttu-id="cf5e8-121">**いいえ** – 在庫のマーキングは適用されません。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="cf5e8-122">**標準** – ペギングに従って在庫のマーキングが更新されます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="cf5e8-123">要求注文 (需要) は、フルフィルメント オーダー (供給) と照らしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="cf5e8-124">フルフィルメント オーダーに一部の数量が残っている場合は、マークされていないため、参照情報は空白のままになっています。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="cf5e8-125">たとえば、100 ea の販売注文が 150 ea の発注書に対してペギングされていない場合、参照情報は販売注文にのみ割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="cf5e8-126">**拡張** – フルフィルメント オーダーの残余数量に関係なく、要求注文 (需要) とフルフィルメント オーダー (供給) の両方がマークされます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="cf5e8-127">たとえば、100 ea の販売注文が 150 ea の発注書に対してペギングされていない場合、参照情報は販売注文と発注書の両方に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="cf5e8-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]