--- 
title: "かんばん状態の更新"
description: "かんばんが誤って空けられるか、または受取済みのかんばんが空けられる必要のある場合、かんばんのステータスを更新する必要があります。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f491558c38a48a47e1477c0140d8d1b5f9c8016
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="update-kanban-status"></a><span data-ttu-id="6d1c8-103">かんばん状態の更新</span><span class="sxs-lookup"><span data-stu-id="6d1c8-103">Update kanban status</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d1c8-104">かんばんが誤って空けられるか、または受取済みのかんばんが空けられる必要のある場合、かんばんのステータスを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="6d1c8-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6d1c8-106">この手順は、現場監督を対象としています。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="6d1c8-107">かんばんを検索します。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-107">Find the kanban.</span></span>
1. <span data-ttu-id="6d1c8-108">[生産管理] > [かんばん] > [かんばん] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="6d1c8-109">[材料取り扱い単位] ステータス列のフィルターを開きます。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="6d1c8-110">[クリア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-110">Click Clear.</span></span>
    * <span data-ttu-id="6d1c8-111">これは、フィルターをリセットします。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-111">This resets the filters.</span></span>  
4. <span data-ttu-id="6d1c8-112">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6d1c8-113">たとえば、「000149」という値で [カード番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="6d1c8-114">空のステータスを受入済ステータスに変更します。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="6d1c8-115">空の材料取り扱い単位の [取り消し] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="6d1c8-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-116">Click OK.</span></span>
    * <span data-ttu-id="6d1c8-117">[材料取り扱い単位] ステータスが受け取られたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="6d1c8-118">受入済ステータスを空のステータスに変更します。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="6d1c8-119">空のかんばんをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="6d1c8-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6d1c8-121">[材料取り扱い単位] ステータスが空になっていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6d1c8-121">Notice that the Handling unit status is Emptied.</span></span>  


