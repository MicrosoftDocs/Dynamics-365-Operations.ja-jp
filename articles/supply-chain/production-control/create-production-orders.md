---
title: 製造オーダーのライフサイクルの概要
description: 製造オーダーを作成すると、品目の製造開始が要求されます。 製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。 また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79b1866cdca885d408aca07c546ca54aa0c3616b
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865198"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="0ff72-105">製造オーダーのライフサイクルの概要</span><span class="sxs-lookup"><span data-stu-id="0ff72-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ff72-106">製造オーダーを作成すると、品目の製造開始が要求されます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="0ff72-107">製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ff72-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="0ff72-108">また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="0ff72-109">製造オーダーは生産ライフ サイクルの各ステージを通過します。</span><span class="sxs-lookup"><span data-stu-id="0ff72-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="0ff72-110">製造オーダーが作成されると、そのオーダーに**作成済み**ステータスが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="0ff72-111">製造オーダーが終了すると、そのオーダーに**終了済**ステータスが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="0ff72-112">各ステージのパラメーター設定によってユーザーは各ステップをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="0ff72-113">この設定は単一のユーザーまたはすべてのユーザーに設定できます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="0ff72-114">生産部品表および生産工順は、製造オーダーの主要なエンティティです。</span><span class="sxs-lookup"><span data-stu-id="0ff72-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="0ff72-115">これらは、生産される選択した品目および数量に基づいて製造オーダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="0ff72-116">製造オーダーを開始する前に、生産部品表と工順は編集できます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="0ff72-117">製造オーダーは、次のシナリオで作成できます:</span><span class="sxs-lookup"><span data-stu-id="0ff72-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="0ff72-118">材料需要に基づいてマスター プランを実行することによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="0ff72-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="0ff72-119">販売注文明細行から直接作成する場合、または上位レベルの製造オーダーの作成と見積をする (ペギングされた供給) 場合です。</span><span class="sxs-lookup"><span data-stu-id="0ff72-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="0ff72-120">手動で作成します。</span><span class="sxs-lookup"><span data-stu-id="0ff72-120">Created manually.</span></span>




