---
title: 実験のステータスを確認する
description: このトピックでは、Dynamics 365 Commerce の実験のライフサイクルにおける実験の状態について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930233"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="758a9-103">実験のステータスを確認する</span><span class="sxs-lookup"><span data-stu-id="758a9-103">Review the status of an experiment</span></span>
<span data-ttu-id="758a9-104">Dynamics 365 Commerce の実験の設定と実行には、多くの手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="758a9-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="758a9-105">実験のライフサイクルの詳細については、[Dynamics 365 Commerce での実験](experimentation-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="758a9-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="758a9-106">実験がライフサイクルのどこにあるかを知るには、サイト ビルダーの**実験**タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="758a9-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="758a9-107">実験リストは、Commerce と、実験の作成、バリエーションの割り当て、データの分析に使用されているサードパーティ サービスの両方の各実験の状態と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="758a9-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="758a9-108">**Commerce の状態**列に、次の値が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="758a9-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="758a9-109">**ドラフト** - 実験は Commerce のページまたはフラグメントに接続されており、編集中です。</span><span class="sxs-lookup"><span data-stu-id="758a9-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="758a9-110">**公開済** - 実験のバリエーションを Web サイトに表示する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="758a9-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="758a9-111">実験がサードパーティ サービスで実行されている場合、Web サイトのユーザーには、サードパーティ サービスによって選択されたページまたはフラグメントのバリエーションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="758a9-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="758a9-112">**未公開** - この実験は、Web サイトでは使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="758a9-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="758a9-113">実験がサードパーティ サービスで実行されている場合でも、Web サイトのユーザーには、既定のバージョンのページまたはフラグメントのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="758a9-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="758a9-114">**完了** - 実験はコースを実行し、バリエーションはすべての Web サイト ユーザーに公開されるようにレベルが上げられました。</span><span class="sxs-lookup"><span data-stu-id="758a9-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="758a9-115">同様に、**サードパーティの状態**列には、サードパーティ サービスでの実験の状態を示す次の値が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="758a9-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="758a9-116">**ドラフト** - 実験はサードパーティ サービスで設定されていますが、まだ開始されていません。</span><span class="sxs-lookup"><span data-stu-id="758a9-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="758a9-117">**実行中** - 実験はサードパーティ サービスで開始され、データを収集しています。</span><span class="sxs-lookup"><span data-stu-id="758a9-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="758a9-118">**一時停止** - 実験は一時停止され、データを収集していません。</span><span class="sxs-lookup"><span data-stu-id="758a9-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="758a9-119">データを再度収集するには、実験を再開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="758a9-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="758a9-120">**アーカイブ済** - 実験はコースを実行し、将来の参照用にサードパーティ サービスでカタログ化されています。</span><span class="sxs-lookup"><span data-stu-id="758a9-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="758a9-121">次の図は、両方の状態のセットと、それらが互いにどのように関連しているかを示します。</span><span class="sxs-lookup"><span data-stu-id="758a9-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="758a9-122">[![実験の状態](./media/experimentation_statuses.svg)](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="758a9-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
