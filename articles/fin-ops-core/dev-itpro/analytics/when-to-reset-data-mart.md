---
title: データ マートをリセットするタイミング
description: このトピックでは、データ マートのリセットによって改善される可能性がある状況と、データ マートのリセットが役立つ可能性が低い状況を一覧表示します。
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988995"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="a0988-103">データ マートをリセットするタイミング</span><span class="sxs-lookup"><span data-stu-id="a0988-103">When to reset a data mart</span></span>

<span data-ttu-id="a0988-104">データ マートのリセットは、時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0988-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="a0988-105">状況によっては、このアクションが必要なソリューションではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0988-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="a0988-106">このトピックでは、データ マートのリセットによって改善される可能性がある状況と、データ マートのリセットが役立つ可能性が低い状況を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="a0988-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="a0988-107">データ マート リセットはいつ実行すべきですか。</span><span class="sxs-lookup"><span data-stu-id="a0988-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="a0988-108">データ マートをリセットする前に、次の質問を検討してください。</span><span class="sxs-lookup"><span data-stu-id="a0988-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="a0988-109">1 つ以上の質問に回答すると、データ マートをリセットすることで組織の利益を得る可能性があるという質問が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0988-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="a0988-110">アプリケーション データベースは復元されましたか。</span><span class="sxs-lookup"><span data-stu-id="a0988-110">Was the application database restored?</span></span>
- <span data-ttu-id="a0988-111">サポート インシデントを開き、サポート エンジニアから、トラブルシューティングの手順の一環としてデータ マートをリセットするように指示されたとします。</span><span class="sxs-lookup"><span data-stu-id="a0988-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="a0988-112">データ マートのリセットが適切ではないタイミングはどのようなものですか。</span><span class="sxs-lookup"><span data-stu-id="a0988-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="a0988-113">データ マートのリセットをお勧めできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0988-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="a0988-114">次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="a0988-114">These include the following.</span></span> 

- <span data-ttu-id="a0988-115">データ同期に関連するパフォーマンス問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="a0988-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="a0988-116">次の理由によりリセット パターンが繰り返し発生する場合。</span><span class="sxs-lookup"><span data-stu-id="a0988-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="a0988-117">**欠落しているデータ**</span><span class="sxs-lookup"><span data-stu-id="a0988-117">**Missing data**</span></span> 
  - <span data-ttu-id="a0988-118">**統合の行き詰まり状態**</span><span class="sxs-lookup"><span data-stu-id="a0988-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="a0988-119">**古いレコード** - 自身による古いレコードはデータ マートのリセットを正当化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a0988-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="a0988-120">大規模なデータ セットがある場合、リセット プロセスの実行に時間がかかりますが、改良が行う可能性は低いです。</span><span class="sxs-lookup"><span data-stu-id="a0988-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="a0988-121">データ マート リセットとは何ですか。</span><span class="sxs-lookup"><span data-stu-id="a0988-121">What is a data mart reset?</span></span>
- <span data-ttu-id="a0988-122">リセットは、既存のタスクが完了した場合にのみ開始されます。</span><span class="sxs-lookup"><span data-stu-id="a0988-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="a0988-123">これにより、古いデータが挿入されるのを確実に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0988-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="a0988-124">この時点で、"有効なタスクが原因でデータ マートのリセットを処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0988-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="a0988-125">後でもう一度お試しください。" というメッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a0988-125">Please try again later.”</span></span>
- <span data-ttu-id="a0988-126">リセットを実行すると、統合タスクが無効にされ、すべてのデータ マート データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="a0988-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="a0988-127">この統合の有効化されます。</span><span class="sxs-lookup"><span data-stu-id="a0988-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="a0988-128">データ マートをリセットすると、デザインしたレポートが失われますか。</span><span class="sxs-lookup"><span data-stu-id="a0988-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="a0988-129">いいえ、レポートは、データ マートのリセットの影響を受けない SQL テーブルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a0988-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="a0988-130">デザインしたレポートが失われるのではないかと心配な場合は、失いたくないデザインをバックアップできます。</span><span class="sxs-lookup"><span data-stu-id="a0988-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="a0988-131">バックアップするには、レポート デザイナーを開いて **会社 > 会社 > 構成要素 > エクスポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0988-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="a0988-132">すべてのユーザーがシステムを終了してデータ マートをリセットする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="a0988-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="a0988-133">いいえ、ユーザーはデータ マート リセットしてもシステムで作業を続行できます。</span><span class="sxs-lookup"><span data-stu-id="a0988-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="a0988-134">ただし、リセットが完了するまで、Financial Reporter で作成されたレポートにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="a0988-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
