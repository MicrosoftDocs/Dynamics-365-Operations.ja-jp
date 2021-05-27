---
title: 航海状態の設定
description: このトピックでは、ユーザーが航海に割り当て可能な状態の値を確立する方法について説明します。
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022111"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="099f6-103">航海状態の設定</span><span class="sxs-lookup"><span data-stu-id="099f6-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="099f6-104">**航海状態ページ** では、ユーザーが航海に割り当て可能な一連の状態値を確立します。</span><span class="sxs-lookup"><span data-stu-id="099f6-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="099f6-105">ユーザーは、航海のすべてのレベル: 航海、輸送コンテナ、Folio、発注書、品目 (購買注文明細行および移動オーダー明細行) に航海状態値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="099f6-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="099f6-106">これらは 2 つの目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="099f6-106">They are used for two purposes:</span></span>

- <span data-ttu-id="099f6-107">航海、輸送コンテナ、Folio、発注書、または品目 (購買注文明細行および移動オーダー明細行) の状態をユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="099f6-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="099f6-108">変更または削除を防止することにより、原価領域の使用を制限します。</span><span class="sxs-lookup"><span data-stu-id="099f6-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="099f6-109">航海状態の設定をするには、**陸揚原価 \> 設定 \> 航海状態** に移動します。</span><span class="sxs-lookup"><span data-stu-id="099f6-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="099f6-110">アクション ウィンドウのボタンを使用して、状態を追加、削除、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="099f6-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="099f6-111">各原価領域には、独自の航海状態のセットと階層があります。</span><span class="sxs-lookup"><span data-stu-id="099f6-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="099f6-112">したがって、**航海状態** ページの **原価領域** フィールドで、最初に、航海状態を表示または作成する原価領域を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="099f6-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="099f6-113">その後、各航海状態ごとに、必要に応じて次の表に示されているフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="099f6-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="099f6-114">航海の状況は、追跡コントロール センターを使用して確立されたルールなどのシステム イベントによって自動的に変更されることもあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="099f6-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="099f6-115">フィールド</span><span class="sxs-lookup"><span data-stu-id="099f6-115">Field</span></span> | <span data-ttu-id="099f6-116">説明</span><span class="sxs-lookup"><span data-stu-id="099f6-116">Description</span></span> |
|---|---|
| <span data-ttu-id="099f6-117">航海状態</span><span class="sxs-lookup"><span data-stu-id="099f6-117">Voyage status</span></span> | <span data-ttu-id="099f6-118">航海状態の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="099f6-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="099f6-119">説明</span><span class="sxs-lookup"><span data-stu-id="099f6-119">Description</span></span> | <span data-ttu-id="099f6-120">航海状態の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="099f6-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="099f6-121">変更</span><span class="sxs-lookup"><span data-stu-id="099f6-121">Modify</span></span> | <span data-ttu-id="099f6-122">この状態の航海の変更をユーザーに許可する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="099f6-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="099f6-123">消去</span><span class="sxs-lookup"><span data-stu-id="099f6-123">Delete</span></span> | <span data-ttu-id="099f6-124">この状態の航海の削除をユーザーに許可する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="099f6-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="099f6-125">必須</span><span class="sxs-lookup"><span data-stu-id="099f6-125">Mandatory</span></span> | <span data-ttu-id="099f6-126">このチェックボックスをオンにすると、航海の状態を必須にし、スキップできない状態になります。</span><span class="sxs-lookup"><span data-stu-id="099f6-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="099f6-127">親</span><span class="sxs-lookup"><span data-stu-id="099f6-127">Parent</span></span> | <span data-ttu-id="099f6-128">このフィールドを使用すると、状態値の間の階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="099f6-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="099f6-129">航海状態は、親状態からその子状態の 1 つまで、階層の下位にのみ (手動または自動で) 変更できます。</span><span class="sxs-lookup"><span data-stu-id="099f6-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="099f6-130">組織が使用する特定の航海状態のみを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="099f6-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="099f6-131">一般的な航海状態には、*確認済*、*輸送中の商品*、*入庫済*、*原価設定* および *原価計算済* が含まれます。</span><span class="sxs-lookup"><span data-stu-id="099f6-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="099f6-132">ただし、他の状態が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="099f6-132">However, other statuses might be present.</span></span>
