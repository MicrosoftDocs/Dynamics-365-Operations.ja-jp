---
title: 実験の設定
description: このトピックでは、サードパーティ サービスで実験を設定する方法について説明します。
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
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097050"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="f83a4-103">実験の設定</span><span class="sxs-lookup"><span data-stu-id="f83a4-103">Set up an experiment</span></span>

<span data-ttu-id="f83a4-104">[仮説を定義し、使用する成功メトリックスを決定](experimentation-identify.md) したら、サードパーティ サービスで実験を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83a4-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="f83a4-105">次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="f83a4-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f83a4-106">追加の手順については、個別のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="f83a4-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="f83a4-107">[![実験ユーザー体験 - 設定](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f83a4-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="f83a4-108">サードパーティ サービスで実験を設定する</span><span class="sxs-lookup"><span data-stu-id="f83a4-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="f83a4-109">この時点で、サードパーティ サービスを選択して実験を実行および監視し、実験コネクタを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83a4-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="f83a4-110">これらの前提条件は、[Dynamics 365 Commerce での実験](experimentation-overview.md) で一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="f83a4-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="f83a4-111">サードパーティ サービスで実験を作成するために必要な手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f83a4-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="f83a4-112">コネクタが適切に構成されている場合、サードパーティ サービスで設定した実験の完全なリストが、約 5 分以内にサイト ビルダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f83a4-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="f83a4-113">成功メトリックスの設定</span><span class="sxs-lookup"><span data-stu-id="f83a4-113">Set up your success metrics</span></span>
<span data-ttu-id="f83a4-114">各実験には、バリエーションの影響を測定し、仮説を検証するためのメトリックスが必要です。</span><span class="sxs-lookup"><span data-stu-id="f83a4-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="f83a4-115">次の手順に従って、Dynamics 365 Commerce からの実際のテレメトリ イベントを使用して、サードパーティ サービスのメトリックスの計算を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f83a4-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f83a4-116">成功したメトリックスを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f83a4-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="f83a4-117">Commerce のサイト ビルダーで、左側のナビゲーション ウィンドウの **ページ** を選択して、メトリックスを収集するページを選択します。</span><span class="sxs-lookup"><span data-stu-id="f83a4-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="f83a4-118">追跡するページまたはモジュールの右側のプロパティ ウィンドウで、 **追跡するイベント ID** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="f83a4-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="f83a4-119">**表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f83a4-119">Select **View**.</span></span> <span data-ttu-id="f83a4-120">すべてのイベント ID の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f83a4-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="f83a4-121">追跡するイベントをコピーし、そのイベント キーをサードパーティ サービスの指定された場所に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f83a4-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="f83a4-122">複数のイベントが必要な場合は、一度に 1 つのキーをコピーします。</span><span class="sxs-lookup"><span data-stu-id="f83a4-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="f83a4-123">ページビューや収益追跡など、使用可能なすべてのイベントと属性を表示する方法については、[診断とトラブルシューティングの Commerce コンポーネント イベント](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f83a4-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="f83a4-124">必要に応じて、サードパーティ サービスで、メトリックスを追跡するためのその他の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f83a4-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="f83a4-125">前のステップ</span><span class="sxs-lookup"><span data-stu-id="f83a4-125">Previous step</span></span>
[<span data-ttu-id="f83a4-126">仮説を識別して実験のメトリックスを決定する</span><span class="sxs-lookup"><span data-stu-id="f83a4-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="f83a4-127">次のステップ</span><span class="sxs-lookup"><span data-stu-id="f83a4-127">Next step</span></span>
[<span data-ttu-id="f83a4-128">実験を接続して編集する</span><span class="sxs-lookup"><span data-stu-id="f83a4-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
