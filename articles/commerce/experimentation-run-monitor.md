---
title: 実験の実行と監視
description: このトピックでは、サードパーティ サービスで実験を実行および監視する方法について説明します。 また、実験開始後にバリエーションを変更する方法についても説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: ee86a6761b27f3c08a65a2e250659cdcfd71db44
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413897"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="bbcfb-104">実験の実行と監視</span><span class="sxs-lookup"><span data-stu-id="bbcfb-104">Run and monitor an experiment</span></span>

<span data-ttu-id="bbcfb-105">このトピックでは、サードパーティのアプリケーションで実験を実行および監視し、必要に応じてバリエーションを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="bbcfb-106">このトピックの手順を完了する前に、Commerce の実験を [公開](experimentation-preview-publish.md) しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="bbcfb-107">次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bbcfb-108">追加の手順については、個別のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="bbcfb-109">[![実験ユーザー体験 - 実行と監視](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bbcfb-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="bbcfb-110">バリエーションを公開すると、Commerce で実験を実行するために必要となるすべての手順が完了します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="bbcfb-111">次の手順では、ユーザーがページを要求したときに各ユーザーに表示するバリエーションを決定します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="bbcfb-112">サードパーティ サービスがその決定を行いますが、最初にサービス内で実験を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="bbcfb-113">実験を有効化する手順はサービスによって異なるため、サービスまたはプロバイダーに含まれている手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="bbcfb-114">実験が有効化されていない場合、ユーザーにはページの既定のバージョンのみが表示されます (バリエーションは表示されません)。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="bbcfb-115">統計的に有効な結果を得るには、データを収集するのに十分な期間、実験を実行し続ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="bbcfb-116">サードパーティ サービスを使用して、実験の実行中に実験関連のデータおよび分析を監視します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="bbcfb-117">バリエーションの調整</span><span class="sxs-lookup"><span data-stu-id="bbcfb-117">Adjust your variations</span></span>
<span data-ttu-id="bbcfb-118">何らかの理由でバリエーションを変更する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbcfb-119">Commerce またはサードパーティ サービスの実際の実験に変更を加えた場合、その結果は大きな影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="bbcfb-120">実験でコースを実行し、大きな変更に対して新しい実験を作成することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="bbcfb-121">Commerce のサイト ビルダーで **実験** を選択し、 対象の実験を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="bbcfb-122">ドロップダウン メニューから更新するバリエーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="bbcfb-123">必要な変更を加えた後、バリエーションをプレビューして公開します。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="bbcfb-124">詳細については、[実験をプレビューして公開する](experimentation-preview-publish.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="bbcfb-125">サードパーティ サービスに移動して、実験の設定に関連する変更を行います。</span><span class="sxs-lookup"><span data-stu-id="bbcfb-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="bbcfb-126">前のステップ</span><span class="sxs-lookup"><span data-stu-id="bbcfb-126">Previous step</span></span>
[<span data-ttu-id="bbcfb-127">実験のプレビューと公開</span><span class="sxs-lookup"><span data-stu-id="bbcfb-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="bbcfb-128">次のステップ</span><span class="sxs-lookup"><span data-stu-id="bbcfb-128">Next step</span></span>
[<span data-ttu-id="bbcfb-129">バリエーションのレベルを上げて実験を完了する</span><span class="sxs-lookup"><span data-stu-id="bbcfb-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
