--- 
title: "明細書を転記するジョブのコンフィギュレーションおよび実行"
description: "この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 564f628ff082887a0f6476ded76c13d2824abf08
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="2595c-103">明細書を転記するジョブのコンフィギュレーションおよび実行</span><span class="sxs-lookup"><span data-stu-id="2595c-103">Configure and run a job to post statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2595c-104">この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2595c-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="2595c-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="2595c-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2595c-106">すべてのワークスペース > .. に移動します</span><span class="sxs-lookup"><span data-stu-id="2595c-106">Go to All workspaces > ..</span></span> <span data-ttu-id="2595c-107">> 小売店舗の財務。</span><span class="sxs-lookup"><span data-stu-id="2595c-107">> Retail store financials.</span></span>
2. <span data-ttu-id="2595c-108">[明細書の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2595c-108">Click Post statements.</span></span>
    * <span data-ttu-id="2595c-109">組織階層を選択し、次に組織ノード ツリーで、個々の店舗またはノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="2595c-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="2595c-110">店舗グループのバッチ ジョブを作成する場合は、ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="2595c-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="2595c-111">選択した項目を追加するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2595c-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="2595c-112">[バックグラウンドで実行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2595c-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="2595c-113">[バッチ処理] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="2595c-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="2595c-114">[再実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2595c-114">Click Recurrence.</span></span>
6. <span data-ttu-id="2595c-115">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2595c-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="2595c-116">[開始時刻] フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="2595c-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="2595c-117">反復処理に関して、特定の実行回数の後終了させる、特定の日付で終了させる、または終了させないの中から選択します。</span><span class="sxs-lookup"><span data-stu-id="2595c-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="2595c-118">その後、ジョブの実行頻度を定義するためにさまざまなオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2595c-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="2595c-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2595c-119">Click OK.</span></span>
9. <span data-ttu-id="2595c-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2595c-120">Click OK.</span></span>


