---
title: 仮想を識別して実験のメトリックを決定する
description: このトピックでは、Dynamics 365 Commerce で E コマース Web サイトで実行する実験の仮想および成功メトリックを識別する方法について説明します。
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
ms.openlocfilehash: 43358264a2107fb139c00ce617054be16a74f935
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413890"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="f341d-103">仮想を識別して実験の成功メトリックを決定する</span><span class="sxs-lookup"><span data-stu-id="f341d-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="f341d-104">実験ライフサイクルの第 1 フェーズでは、実験の仮想を識別して、成功を評価するために追跡するメトリックを決定することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f341d-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="f341d-105">次の図は、Dynamics 365 Commerce の E コマース Web サイトでの[実験の設定と実行](experimentation-overview.md)に関連するすべての手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="f341d-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f341d-106">追加の手順については、個別のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="f341d-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="f341d-107">[ ![実験ユーザー体験 - 識別](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f341d-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="f341d-108">仮想とは、実験の結果を予測する明細書です。</span><span class="sxs-lookup"><span data-stu-id="f341d-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="f341d-109">たとえば、ユーザーの行動および収集した Web サイトのデータに関する調査など、仮想の定義には多くの要因があります。</span><span class="sxs-lookup"><span data-stu-id="f341d-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="f341d-110">仮想により、実験で検証する前提および理論を定義します。</span><span class="sxs-lookup"><span data-stu-id="f341d-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="f341d-111">実験の仮想の例としては、「*皆、夏には軽量で明るい色のものを着たいので、夏の期間は、ホーム ページにある白い T シャツの写真は、ネイビーのセーターよりもクリック率が高くなる。*」</span><span class="sxs-lookup"><span data-stu-id="f341d-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="f341d-112">その場合は、白い T シャツとネイビーのセーターを含むバリエーションを作成し、両方を同時に公開します。</span><span class="sxs-lookup"><span data-stu-id="f341d-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="f341d-113">仮想を検証するには、実験の成功または失敗を Web サイトのユーザーがリンクやボタンをクリックするなどのユーザーのアクションに直接関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f341d-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="f341d-114">これらのアクションは、実験を追跡するサード パーティ サービスに報告されるイベントに対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f341d-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="f341d-115">時間の経過と共に、アクションを実行するユーザーの割合は、レポートを生成して分析を実施するために使用できるメトリックとして集計されます。</span><span class="sxs-lookup"><span data-stu-id="f341d-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="f341d-116">使用可能なすべてのイベントおよび属性を確認するには、[診断とトラブルシューティングの Commerce コンポーネント イベント](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f341d-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="f341d-117">前のステップ</span><span class="sxs-lookup"><span data-stu-id="f341d-117">Previous step</span></span>
[<span data-ttu-id="f341d-118">Dynamics 365 Commerce での実験</span><span class="sxs-lookup"><span data-stu-id="f341d-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="f341d-119">次のステップ</span><span class="sxs-lookup"><span data-stu-id="f341d-119">Next step</span></span>
[<span data-ttu-id="f341d-120">実験の設定</span><span class="sxs-lookup"><span data-stu-id="f341d-120">Set up an experiment</span></span>](experimentation-setup.md)
