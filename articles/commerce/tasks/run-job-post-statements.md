---
title: 明細書を転記するジョブの構成および実行
description: この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141180"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="74fc1-103">明細書を転記するジョブの構成および実行</span><span class="sxs-lookup"><span data-stu-id="74fc1-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74fc1-104">この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="74fc1-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="74fc1-106">すべてのワークスペース > .. に移動します</span><span class="sxs-lookup"><span data-stu-id="74fc1-106">Go to All workspaces > ..</span></span> <span data-ttu-id="74fc1-107">> 店舗財務。</span><span class="sxs-lookup"><span data-stu-id="74fc1-107">> Store financials.</span></span>
2. <span data-ttu-id="74fc1-108">明細書のバッチ転記をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74fc1-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="74fc1-109">組織階層を選択し、次に組織ノード ツリーで、個々の店舗またはノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="74fc1-110">店舗グループのバッチ ジョブを作成する場合は、ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="74fc1-111">選択した項目を追加するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74fc1-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="74fc1-112">バックグラウンド タブで実行をクリックします。![バックグラウンドで実行](../dev-itpro/media/runbackground.png "バックグラウンドで実行")</span><span class="sxs-lookup"><span data-stu-id="74fc1-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="74fc1-113">[バッチ処理] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="74fc1-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="74fc1-114">![バッチ処理](../dev-itpro/media/batchprocessing.png "バッチ処理 & 再実行")</span><span class="sxs-lookup"><span data-stu-id="74fc1-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="74fc1-115">[再実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74fc1-115">Click Recurrence.</span></span>
6. <span data-ttu-id="74fc1-116">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="74fc1-117">[開始時刻] フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="74fc1-118">反復処理に関して、特定の実行回数の後終了させる、特定の日付で終了させる、または終了させないの中から選択します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="74fc1-119">その後、ジョブの実行頻度を定義するためにさまざまなオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="74fc1-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="74fc1-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74fc1-120">Click OK.</span></span>
9. <span data-ttu-id="74fc1-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74fc1-121">Click OK.</span></span>

