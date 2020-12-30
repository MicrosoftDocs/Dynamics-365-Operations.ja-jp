---
title: サービス注文ステージ
description: サービス注文のステージを定義し、作業者に割り当てると、サービス組織内のさまざまな従業員が実行するタスクでのサービス注文の流れを管理します。
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bcb72e8222b378198fcd044428fa1a4a0e8944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431647"
---
# <a name="service-order-stages"></a><span data-ttu-id="bc46a-103">サービス注文ステージ</span><span class="sxs-lookup"><span data-stu-id="bc46a-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bc46a-104">サービス注文のステージを設定して、完了する必要があるタスク、完了する順番、それらの実行を担当する作業者を定義できます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="bc46a-105">サービス注文のステージを定義し、作業者に割り当てると、サービス組織内のさまざまな従業員が実行するタスクでのサービス注文の流れを管理できます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="bc46a-106">ステージ シーケンスには、初期ステージを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc46a-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="bc46a-107">また、各ステージで許可されるアクションを定義できます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="bc46a-108">たとえば、最後のステージを除くすべてのステージの **転記** チェック ボックスをオフにすると、サービス注文がステージの全シーケンスを完了するまで、サービス注文を転記できないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="bc46a-109">サービス注文ステージの分岐</span><span class="sxs-lookup"><span data-stu-id="bc46a-109">Branching in service order stages</span></span>

<span data-ttu-id="bc46a-110">サービス ステージを設定すると、次のサービス ステージ用にそこで選択できる複数の選択肢または分岐を作成できます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="bc46a-111">作成したすべての分岐は、初期ステージが完了したときに選択できます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="bc46a-112">たとえば、初期ステージとして **計画** を設定します。</span><span class="sxs-lookup"><span data-stu-id="bc46a-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="bc46a-113">**処理中** と **キャンセル** という 2 種類のステージを作成し、それらの親として **計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc46a-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="bc46a-114">販売注文に **計画** のステージを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="bc46a-115">販売注文の計画ステージが完了すると、販売注文の作業準備が完了したら **プロセス** ステージ、販売注文がキャンセルされたら **キャンセル** ステージを選択できます。</span><span class="sxs-lookup"><span data-stu-id="bc46a-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc46a-116">参照</span><span class="sxs-lookup"><span data-stu-id="bc46a-116">See also</span></span>

[<span data-ttu-id="bc46a-117">サービス注文ステージを設定します</span><span class="sxs-lookup"><span data-stu-id="bc46a-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="bc46a-118">サービス注文ステージの変更</span><span class="sxs-lookup"><span data-stu-id="bc46a-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


