---
title: データ マートをリセットするタイミング
description: このトピックでは、データ マートのリセットによって改善される可能性がある状況と、データ マートのリセットが役立つ可能性が低い状況を一覧表示します。
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71324d4aa2d20dd6ae4729412a017d130ab0144f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563737"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="54235-103">データ マートをリセットするタイミング</span><span class="sxs-lookup"><span data-stu-id="54235-103">When to reset a data mart</span></span>

<span data-ttu-id="54235-104">データ マートのリセットは、時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="54235-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="54235-105">状況によっては、このアクションが必要なソリューションではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="54235-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="54235-106">このトピックでは、データ マートのリセットによって改善される可能性がある状況と、データ マートのリセットが役立つ可能性が低い状況を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="54235-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="54235-107">データ マート リセットをいつ実行する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="54235-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="54235-108">データ マートをリセットする前に、次の質問を検討してください。</span><span class="sxs-lookup"><span data-stu-id="54235-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="54235-109">1 つ以上の質問に回答すると、データ マートをリセットすることで組織の利益を得る可能性があるという質問が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="54235-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="54235-110">アプリケーション データベースが復元されましたが、データ マート データベースは復元されませんでした。</span><span class="sxs-lookup"><span data-stu-id="54235-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="54235-111">会計期間に対して誤ったデータが表示される場合は、レポート デザインに問題が生じ、その結果を取り込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="54235-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="54235-112">あるアカウント期間で誤ったデータが表示され、レポート デザイナーの **統合ステータス**  ページの統合実施の下にレコードが表示されます。 (レポート デザイナーを起動し、**ツール > 統合ステータス** を選択します)。</span><span class="sxs-lookup"><span data-stu-id="54235-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="54235-113">サポート インシデントを開いて、サポート エンジニアから、トラブルシューティングの手順の一環としてデータ マートをリセットするように指示されました。</span><span class="sxs-lookup"><span data-stu-id="54235-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="54235-114">データ マートのリセットが適切ではない場合は?</span><span class="sxs-lookup"><span data-stu-id="54235-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="54235-115">データ マートのリセットをお勧めできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="54235-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="54235-116">次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="54235-116">These include the following.</span></span> 

- <span data-ttu-id="54235-117">このトピックに理由の説明が示されていないとき。</span><span class="sxs-lookup"><span data-stu-id="54235-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="54235-118">データ同期に関連するパフォーマンスの問題が発生する可能性があります。この状況では、データ マートのリセットは役立たできない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54235-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="54235-119">次の理由によりリセット パターンが繰り返し発生する場合。</span><span class="sxs-lookup"><span data-stu-id="54235-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="54235-120">**欠落しているデータ** まず、レポート デザインの問題とデータ同期のタイミングの問題を削除します。たとえば、データの欠落が転記された後にファクト マップが実行されたのを観察します。</span><span class="sxs-lookup"><span data-stu-id="54235-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="54235-121">**統合の行き詰まり状態** - 統合の速度が遅い、または問題が解消しない場合、データ マートのリセットが問題を解決できる可能性は低くなります。</span><span class="sxs-lookup"><span data-stu-id="54235-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="54235-122">**リセットの試行に失敗しました** - リセットの実行に失敗した回数が発生し、データの欠落が理由で失敗した場合は、サポート インシデントを開き、サポート エンジニアと一緒に作業して状況を分析してから、データ マートの再リセットを試みすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="54235-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="54235-123">**古いレコード** - 自身による古いレコードはデータ マートのリセットを正当化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="54235-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="54235-124">大規模なデータ セットがある場合、リセット プロセスの実行に時間がかかりますが、改良が行う可能性は低いです。</span><span class="sxs-lookup"><span data-stu-id="54235-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="54235-125">データ マート のリセットで実行されない動作</span><span class="sxs-lookup"><span data-stu-id="54235-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="54235-126">リセットは、既存のタスクが完了した場合にのみ開始されます。</span><span class="sxs-lookup"><span data-stu-id="54235-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="54235-127">これにより、古いデータが挿入されるのを確実に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="54235-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="54235-128">この時点で、"有効なタスクが原因でデータ マートのリセットを処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="54235-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="54235-129">後でもう一度お試しください。" というメッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="54235-129">Please try again later.”</span></span>
- <span data-ttu-id="54235-130">リセットを実行すると、統合タスクが無効にされ、すべてのデータ マート データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="54235-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="54235-131">この統合の有効化されます。</span><span class="sxs-lookup"><span data-stu-id="54235-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="54235-132">次の点で、データ マートのリセットで実行 *しない* 2 つのことを指定します。</span><span class="sxs-lookup"><span data-stu-id="54235-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="54235-133">リセットではレポート デザインはクリアされません。</span><span class="sxs-lookup"><span data-stu-id="54235-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="54235-134">リセットでは、選択しない限り、会社データまたはユーザー データはクリアされません。</span><span class="sxs-lookup"><span data-stu-id="54235-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]