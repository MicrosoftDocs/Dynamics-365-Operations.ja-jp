---
title: "製造オーダーのリリース"
description: "この手順では、製造オーダーのリリース方法を示します。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8c28631adc7a7756b5b9f9a0cd0c43ebe1ce4f48
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="release-a-production-order"></a><span data-ttu-id="37ba3-103">製造オーダーのリリース</span><span class="sxs-lookup"><span data-stu-id="37ba3-103">Release a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37ba3-104">この手順では、製造オーダーのリリース方法を示します。</span><span class="sxs-lookup"><span data-stu-id="37ba3-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="37ba3-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="37ba3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="37ba3-106">これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 4 番目です。</span><span class="sxs-lookup"><span data-stu-id="37ba3-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="37ba3-107">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="37ba3-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="37ba3-108">[スケジュール済] 状態を持つ製造オーダーをグリッドで選択します。</span><span class="sxs-lookup"><span data-stu-id="37ba3-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="37ba3-109">アクション ペインで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ba3-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="37ba3-110">[リリース] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ba3-110">Click Release.</span></span>
    * <span data-ttu-id="37ba3-111">このページで、製造オーダーの選択範囲のリリースを確認できます。</span><span class="sxs-lookup"><span data-stu-id="37ba3-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="37ba3-112">注文を追加する場合は、[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ba3-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="37ba3-113">リリース ステップは、作業現場のオペレーターが生産ジョブの進捗をレポートできるように製造オーダーを生産の作業現場にいつリリースするかを示します。</span><span class="sxs-lookup"><span data-stu-id="37ba3-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="37ba3-114">ジョブの処理に関する情報を含む生産文書は発行できます。</span><span class="sxs-lookup"><span data-stu-id="37ba3-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="37ba3-115">原材料ピッキングの倉庫作業は、倉庫のプロセス用に設定された品目に対して生成されます。</span><span class="sxs-lookup"><span data-stu-id="37ba3-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="37ba3-116">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ba3-116">Click the General tab.</span></span>
    * <span data-ttu-id="37ba3-117">どの生産レポートを印刷するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ba3-117">Select which production reports should be printed.</span></span> <span data-ttu-id="37ba3-118">ジョブ カード レポートでは、スケジュールされた個々のジョブのページが印刷され、製造オーダーがジョブ レベルにスケジュールされることを必要とします。</span><span class="sxs-lookup"><span data-stu-id="37ba3-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="37ba3-119">レポートには、予定された開始時刻と終了時刻、生産数量、どのリソースがジョブを処理するかに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="37ba3-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="37ba3-120">工順ジョブ レポートは、同じページにある同じ情報を収集しますが、各ジョブのページは印刷されません。</span><span class="sxs-lookup"><span data-stu-id="37ba3-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="37ba3-121">工順カード レポートには工程のみが表示され、ジョブは表示されません。</span><span class="sxs-lookup"><span data-stu-id="37ba3-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="37ba3-122">したがって、このレポートは、ジョブのスケジューリングを必要としませんが、製造オーダーが工程レベルでスケジューリングされる時に使用できます。</span><span class="sxs-lookup"><span data-stu-id="37ba3-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="37ba3-123">[工順カードの印刷] チェック ボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ba3-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="37ba3-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ba3-124">Click OK.</span></span>
7. <span data-ttu-id="37ba3-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37ba3-125">Close the page.</span></span>

